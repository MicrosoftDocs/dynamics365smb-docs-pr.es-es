---
title: Administre el almacenamiento eliminando documentos o comprimiendo datos
description: Descubra cómo puede mantener sus datos históricos comprimiendo las entradas del libro mayor, o elimínelas.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: c41e4d871740efde811a6bfc6190605aa4e3f573
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 03/31/2021
ms.locfileid: "5781216"
---
# <a name="manage-storage-by-deleting-documents-or-compressing-data"></a>Administrar el almacenamiento eliminando documentos o comprimiendo datos

Un rol central, como el administrador de aplicaciones, debe eliminar o comprimir periódicamente los documentos históricos para gestionar su acumulación.  

> [!TIP]
> Para obtener información sobre otras formas de reducir la cantidad de datos almacenados en una base de datos, consulte [Reducción de datos almacenados en bases de datos de Business Central](/dynamics365/business-central/dev-itpro/administration/database-reduce-data) en la ayuda para desarrolladores y profesionales de TI.

## <a name="delete-documents"></a>Eliminar documentos

En algunos casos, es posible que necesite eliminar pedidos de compra facturados que no se hayan eliminado. [!INCLUDE[prod_short](includes/prod_short.md)] comprueba que se hayan facturado totalmente los pedidos de compra eliminados. No puede eliminar pedidos que no haya facturado y recibido en su totalidad.  

Los pedidos de devolución generalmente se eliminan después de facturados. Cuando registra una factura, ésta se transfiere a la página **Histórico abono compra**. Si ha activado la casilla **Envío dev. en abono** en la página **Conf. compras y pagos**, la factura se transfiere a la página **Histórico envío devolución**. Puede eliminar los documentos a partir de un trabajo por lotes **Borrar ped. dev. compras fact.**. Antes de eliminar, el trabajo por lotes comprueba si los pedidos devueltos de compra han sido enviados y facturados totalmente.  

Los pedidos abiertos de compra no se eliminan una vez que se han procesado y facturado todos los pedidos de compra relacionados. Para eliminar pedidos abiertos de compra, puede utilizar el trabajo por lotes **Eliminar pedidos abiertos compra facturados**.  

Los pedidos de servicios facturados se suelen eliminar automáticamente después de haberse facturado en su totalidad. Cuando se registra una factura, se crea un movimiento correspondiente en la página **Facts. ventas (servicio) regis.** El documento registrado se puede ver en la página **Fact. ventas (servicio) regis.**  

Sin embargo, los pedidos de servicio no se eliminarán de forma automática si la cantidad total de dicho pedido no se ha registrado desde el pedido de servicio en sí, sino desde la página **Factura servicio**. En este caso, puede que tenga que eliminar los pedidos facturados que no se hayan eliminado. Para ello, ejecute el proceso **Eliminar ped. servicio facturados**.  

## <a name="compress-data-with-date-compression"></a>Comprimir datos con compresión de datos

Puede comprimir datos en [!INCLUDE [prod_short](includes/prod_short.md)] para ahorrar espacio en la base de datos, lo que en [!INCLUDE [prod_short](includes/prod_short.md)] en línea también puede ahorrarle dinero. La compresión se basa en fechas y trabajos, fusionando diversos movimientos antiguos en uno solo. Solo podrá comprimir los movimientos de los ejercicios que ya estén cerrados y solo movimientos de proveedores en los que el campo **Abrir** esté establecido en *No*.  

Por ejemplo, los movimientos de proveedores de ejercicios anteriores se pueden comprimir, de forma que sólo haya una entrada al haber y otra al debe cada mes. El importe del nuevo movimiento es la suma de todos los movimientos comprimidos. La fecha asignada es la inicial del periodo que se ha comprimido, como el primer día del mes (si los movimientos están comprimidos por meses). Después de la compresión, aún podrá ver el saldo del periodo de cada cuenta del ejercicio anterior.

El número de movimientos resultante de una compresión de datos dependerá del número de filtros aplicados, de los campos que se combinen y de la longitud del periodo seleccionado. Siempre habrá, al menos, un movimiento. Cuando termine el trabajo por lotes, podrá ver el resultado en la página **Registros de compresión por fechas**.

Puede comprimir los siguientes tipos de datos en [!INCLUDE [prod_short](includes/prod_short.md)] usando trabajos por lotes:

* Movimientos del mayor de bancos

  Después de la compresión, con la utilidad **Guardar contenido campo**, podrá conservar el contenido de los campos **N.º documento, Nuestro contacto**, **Código de dimensión global 1** y **Código de dimensión global 2**.
* Movimientos de proveedores

> [!NOTE]
> Las entradas comprimidas para clientes, proveedores, bancos y libros auxiliares FA se contabilizan de forma ligeramente diferente a la contabilización estándar. Esto es para reducir el número de nuevos movimientos de contabilidad creados por la compresión de fechas, y es especialmente importante cuando mantiene información como dimensiones y números de documentos. La compresión de fechas crea nuevas entradas de la siguiente manera:
>* En la página **Movimientos de contabilidad**, se crean nuevas entradas con nuevos números de entrada para las entradas comprimidas. El campo **Descripción** contiene **Comprimido por fechas** para que las entradas comprimidas sean fáciles de identificar. 
>* En las páginas del libro mayor, como la página **Movimientos de contabilidad**, se crean uno o más movimientos con nuevos números de movimientos. 
> El proceso de contabilización crea espacios en la serie de números para las entradas de la página **Movimientos de contabilidad**. Esos números se asignan solo a las entradas en las páginas del libro mayor. El rango de números que se asignó a los movimientos está disponible en la **Página de registro de P/G**, en los campos **Desde el número de movimiento** y **Hasta el número de movimiento**. 

Después de la compresión, siempre se retiene el contenido de los siguientes campos: **Fecha de registro**, **N.º proveedor**, **Tipo de documento**, **Código de divisa**, **Grupo contable**, **Importe**, **Importe pendiente**, **Importe inicial (DL)**, **Importe pendiente (DL)**, **Importe (DL)**, **Beneficio (DL)**, **Dto. factura (DL)**, **Dto. P.P (DL)** y **Posible descuento P.P.**.

  Mediante la utilidad **Guardar contenido campo** también podrá conservar el contenido de los siguientes campos adicionales: **N.º documento**, **Comprar a N.º proveedor**, **Código de comprador**, **Código de dimensión global 1** y **Código de dimensión global 2**.

> [!NOTE]
> Después de ejecutar la compresión de fechas, todas las cuentas del libro mayor se bloquean. Por ejemplo, no puede anular la aplicación de los asientos del libro mayor de proveedores o bancos para ninguna cuenta durante el período para el que se comprimen las fechas.

<!--* General ledger entries
* Customer ledger entries-->
<!--* Fixed asset ledger entries
* G/L budget entries
* VAT entries

  After the compression the contents of the following fields are always retained: **Posting Date**, **Type**, **Closed**, **Gen. Bus. Posting Group**, **Gen. Prod. Posting Group**, **VAT Calculation Type**, **Base**, and **Amount**.

  With the **Retain Field Contents** facility, you can also retain the contents of the following additional fields: **Document No.**, **Bill-to/Pay-to No.**, **EU 3-Party Trade**, **Country/Region Code**, and **Internal Ref. No.**.
* Insurance ledger entries
* Maintenance ledger entries
* Resource ledger entries

  After the compression, the contents of the following fields are retained: **Posting Date**, **Resource No.**, **Resource Group No.**, **Entry Type**, **Quantity**, **Total Cost**, **Total Price**, and **Chargeable**.

  With the **Retain Field Contents** facility, you can also retain the contents of the following additional fields: **Document No.**, **Work Type Code**, **Job No.**, **Unit of Measure Code**, **Source Type**, **Source No.**. **Chargeable**, **
* Warehouse entries

  After the compression the contents of the following fields are always retained: **Registering Date**, **Location Code**, **Zone Code**, **Bin Code**, **Item No.**, **Quantity**, **Qty. (Base)**, **Bin Type Code**, **Entry Type**, **Variant Code**, **Qty. per Unit of Measure**, **Unit of Measure Code**, **Warranty Date**, **Expiration Date**, **Cubage**, and **Weight**.

  With the **Retain Field Contents** facility, you can also retain the contents of the **Serial No.** and **Lot No.** fields. -->

El número de movimientos resultante de una tarea de compresión por fechas dependerá del número de filtros aplicados, de los campos que se combinen y de la longitud del periodo seleccionada. Siempre habrá, al menos, un movimiento. 

> [!WARNING]
> La compresión por fechas borra movimientos, por tanto es recomendable que haga siempre una copia de seguridad de la base de datos antes de ejecutar el proceso.

La siguiente tabla enumera los campos de la Ficha desplegable **Opciones** que están disponibles en todos los trabajos por lotes. La sección **Guardar contenido campo** incluye campos adicionales que se describen arriba.

|Campo  |Descripción  |
|-------|-------------|
|Fecha inicial     |Introduzca la primera fecha que se incluirá en la compresión por fechas. La compresión afectará a todos los movimientos de IVA hasta la Fecha final.|
|Fecha final     |Introduzca la última fecha que se incluirá en la compresión por fechas. La compresión afectará a todos los movimientos desde la Fecha inicial hasta esta fecha.|
|Longitud del periodo |Seleccione la longitud del periodo cuyos movimientos se combinarán. Seleccione el campo para ver las opciones. Si seleccionó la longitud del periodo *Trimestre*, *Mes* o *Semana*, sólo se comprimirán los movimientos con un periodo contable común.|
|Guardar contenido campo     |Si desea conservar el contenido de determinados campos, aunque los movimientos estén comprimidos, marque las casillas. Cuantos más campos seleccione, más detallados serán los movimientos comprimidos. Si no selecciona ninguno de estos campos, el trabajo por lotes creará un movimiento por día, semana u otro periodo, según haya elegido en el campo **Longitud periodo**. |

## <a name="see-also"></a>Consulte también

[Administración](admin-setup-and-administration.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]