---
title: Administre el almacenamiento eliminando documentos o comprimiendo datos
description: Aprenda a lidiar con la acumulación de documentos históricos (y reduzca la cantidad de datos almacenados en una base de datos) eliminándolos o comprimiéndolos.
author: edupont04
ms.topic: conceptual
ms.search.form: 107, 9040
ms.date: 06/14/2021
ms.author: edupont
ms.openlocfilehash: a5c79da88ec49f6d9ff763b6712b0777158d2805
ms.sourcegitcommit: ef80c461713fff1a75998766e7a4ed3a7c6121d0
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 02/15/2022
ms.locfileid: "8147914"
---
# <a name="manage-storage-by-deleting-documents-or-compressing-data"></a>Administrar el almacenamiento eliminando documentos o comprimiendo datos

Un rol central, como el administrador de aplicaciones, debe eliminar o comprimir periódicamente los documentos históricos para gestionar su acumulación.  

> [!TIP]
> Para obtener información sobre otras formas de reducir la cantidad de datos almacenados en una base de datos, consulte [Reducción de datos almacenados en bases de datos de Business Central](/dynamics365/business-central/dev-itpro/administration/database-reduce-data) en la documentación para desarrolladores y profesionales de TI.

## <a name="delete-documents"></a>Eliminar documentos

En algunos casos, es posible que necesite eliminar pedidos de compra facturados que no se hayan eliminado. [!INCLUDE[prod_short](includes/prod_short.md)] comprueba que se hayan facturado totalmente los pedidos de compra eliminados. No puede eliminar pedidos que no haya facturado y recibido en su totalidad.  

Los pedidos de devolución generalmente se eliminan después de facturados. Cuando registra una factura, ésta se transfiere a la página **Histórico abono compra**. Si ha activado la casilla **Envío dev. en abono** en la página **Conf. compras y pagos**, la factura se transfiere a la página **Histórico envío devolución**. Puede eliminar los documentos a partir de un trabajo por lotes **Borrar ped. dev. compras fact.**. Antes de eliminar, el trabajo por lotes comprueba si los pedidos devueltos de compra han sido enviados y facturados totalmente.  

Los pedidos abiertos de compra no se eliminan una vez que se han procesado y facturado todos los pedidos de compra relacionados. Para eliminar pedidos abiertos de compra, puede utilizar el trabajo por lotes **Eliminar pedidos abiertos compra facturados**.  

Los pedidos de servicios facturados se suelen eliminar automáticamente después de haberse facturado en su totalidad. Cuando se registra una factura, se crea un movimiento correspondiente en la página **Facts. ventas (servicio) regis.** El documento registrado se puede ver en la página **Fact. ventas (servicio) regis.**  

Sin embargo, los pedidos de servicio no se eliminarán de forma automática si la cantidad total de dicho pedido no se ha registrado desde el pedido de servicio en sí, sino desde la página **Factura servicio**. En este caso, puede que tenga que eliminar los pedidos facturados que no se hayan eliminado. Para ello, ejecute el proceso **Eliminar ped. servicio facturados**.  

## <a name="compress-data-with-date-compression"></a>Comprimir datos con compresión de datos

Puede comprimir datos en [!INCLUDE [prod_short](includes/prod_short.md)] para ahorrar espacio en la base de datos, lo que en [!INCLUDE [prod_short](includes/prod_short.md)] en línea también puede ahorrarle dinero. La compresión se basa en fechas y trabajos, fusionando diversos movimientos antiguos en uno solo. 

Puede comprimir entradas en las siguientes condiciones:

* Son de años fiscales cerrados
* El campo **Abrir** se establece en **No**. 
* Tienen al menos cinco años. Si desea comprimir datos que tengan menos de cinco años, comuníquese con su socio de Microsoft.

Por ejemplo, los movimientos de proveedores de ejercicios anteriores se pueden comprimir, de forma que sólo haya una entrada al haber y otra al debe cada mes. El importe del nuevo movimiento es la suma de todos los movimientos comprimidos. La fecha asignada es la inicial del periodo que se ha comprimido, como el primer día del mes (si los movimientos están comprimidos por meses). Después de la compresión, aún podrá ver el saldo del periodo de cada cuenta del ejercicio anterior.

El número de movimientos resultante de una compresión de datos dependerá del número de filtros aplicados, de los campos que se combinen y de la longitud del periodo seleccionado. Siempre habrá, al menos, un movimiento. Cuando termine el trabajo por lotes, podrá ver el resultado en la página **Registros de compresión por fechas**.

Puede comprimir los siguientes tipos de datos usando trabajos por lotes. Hay un trabajo por lotes para cada tipo de datos.

* Entradas de finanzas: movimientos de contabilidad, movimientos de IVA, movimientos de banco, movimientos de presupuesto, movimientos de contabilidad de clientes, movimientos de contabilidad de proveedores.
* Movimientos almacén 
* Movimientos de recursos
* Movimientos de presupuesto de productos
* Activo fijo: movimientos de activos fijos, movimientos de mantenimiento de activos fijos, movimientos de cobertura de seguro de activos fiojs.

Cuando define criterios para la compresión, puede utilizar las opciones de **Guardar contenido campo** para mantener el contenido de ciertos campos. Los campos que están disponibles dependen de los datos que está comprimiendo.

> [!NOTE]
> Antes de que pueda ejecutar la compresión de fechas, sus vistas de análisis deben estar actualizadas. Para más información, vea [Para actualizar una vista de análisis](bi-how-analyze-data-dimension.md#to-update-an-analysis-view).

Después de la compresión, siempre se retiene el contenido de los siguientes campos: **Fecha de registro**, **N.º proveedor**, **Tipo de documento**, **Código de divisa**, **Grupo contable**, **Importe**, **Importe pendiente**, **Importe inicial (DL)**, **Importe pendiente (DL)**, **Importe (DL)**, **Beneficio (DL)**, **Dto. factura (DL)**, **Dto. P.P (DL)** y **Posible descuento P.P.**.

## <a name="posting-compressed-entries"></a>Publicar entradas comprimidas
Las entradas comprimidas se publican de forma ligeramente diferente a la publicación estándar. Esto es para reducir el número de nuevos movimientos de contabilidad creados por la compresión de fechas, y es especialmente importante cuando mantiene información como dimensiones y números de documentos. La compresión de fechas crea nuevas entradas de la siguiente manera:
* En la página **Movimientos de contabilidad**, se crean nuevas entradas con nuevos números de entrada para las entradas comprimidas. El campo **Descripción** contiene **Comprimido por fechas** para que las entradas comprimidas sean fáciles de identificar. 
* En las páginas del libro mayor, como la página **Movimientos de contabilidad**, se crean uno o más movimientos con nuevos números de movimientos. 

El proceso de contabilización crea espacios en la serie de números para las entradas de la página **Movimientos de contabilidad**. Esos números se asignan solo a las entradas en las páginas del libro mayor. El rango de números que se asignó a los movimientos está disponible en la **Página de registro de P/G**, en los campos **Desde el número de movimiento** y **Hasta el número de movimiento**. 

> [!NOTE]
> Después de ejecutar la compresión de fechas, todas las cuentas del libro mayor se bloquean. Por ejemplo, no puede anular la aplicación de los asientos del libro mayor de proveedores o bancos para ninguna cuenta durante el período para el que se comprimen las fechas.

El número de movimientos resultante de una compresión de datos dependerá del número de filtros aplicados, de los campos que se combinen y de la longitud del periodo seleccionado. Siempre habrá, al menos, un movimiento. 

> [!WARNING]
> La compresión por fechas borra movimientos, por tanto es recomendable que haga siempre una copia de seguridad de la base de datos antes de ejecutar el proceso.

### <a name="to-run-a-date-compression"></a>Para ejecutar compresión por fechas
1. Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "Icono Buscar página o informe"), introduzca **Administración de datos** y, a continuación, seleccione el vínculo relacionado.
2. Realice una de las siguientes acciones:
    * Para utilizar una guía de configuración asistida para configurar la compresión de fechas para uno o más tipos de datos, elija **Guía de administración de datos**.
    * Para configurar la compresión para un tipo individual de datos, elija **Compresión de fecha**, **Comprimir movimientos** y, a continuación, elija los datos que desee comprimir.

   > [!NOTE]
   > Solo puede comprimir datos que tengan más de cinco años. Si desea comprimir datos que tengan menos de cinco años, comuníquese con su socio de Microsoft.

## <a name="see-also"></a>Consulte también

[Administración](admin-setup-and-administration.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]