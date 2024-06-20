---
title: Administre el almacenamiento eliminando documentos o comprimiendo datos
description: Aprenda a lidiar con la acumulación de documentos históricos (y reduzca la cantidad de datos almacenados en una base de datos) eliminándolos o comprimiéndolos.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.form: '107, 9035, 9040'
ms.date: 04/16/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# Administre el almacenamiento eliminando documentos o comprimiendo datos

Un rol central, como el administrador de aplicaciones, debe eliminar o comprimir periódicamente los documentos históricos para gestionar su acumulación.  

> [!TIP]
> Obtenga más información sobre otras formas de reducir la cantidad de datos almacenados en una base de datos en [Reducción de datos almacenados en bases de datos de Business Central](/dynamics365/business-central/dev-itpro/administration/database-reduce-data) en la documentación para desarrolladores y profesionales de TI.

## Eliminar documentos.

En algunos casos, es posible que necesite eliminar pedidos de compra facturados. Sin embargo, no puede eliminarlos a menos que haya facturado por completo y recibido los artículos en las órdenes de compra. [!INCLUDE[prod_short](includes/prod_short.md)] le ayuda comprobando eso.

Las empresas suelen eliminar los pedidos de devolución una vez facturados. Cuando registra una factura, [!INCLUDE [prod_short](includes/prod_short.md)] la transfiere a la página **Histórico abono compra**. Si ha activado la casilla **Envío dev. en abono** en la página **Conf. compras y pagos**, la factura se transfiere a la página **Histórico envío devolución**. Puede eliminar los documentos a partir de un trabajo por lotes **Borrar ped. dev. compras fact.**. Antes de eliminar documentos, el trabajo por lotes comprueba si los pedidos devueltos de compra han sido enviados y facturados totalmente.  

Los pedidos abiertos de compra no se eliminan automáticamente una vez que se han procesado y facturado todos los pedidos de compra relacionados. En su lugar, puede eliminarlos con el trabajo por lotes **Eliminar pedidos abiertos compra facturados**.  

Las empresas suelen eliminar automáticamente los pedidos de servicio facturados después de haberlos facturado en su totalidad. Cuando se registra una factura, se crea un movimiento correspondiente y se puede ver en la página **Facts. ventas (servicio) regis.**  

Sin embargo, los pedidos de servicio no se eliminarán de forma automática si la cantidad total de dicho pedido se ha registrado desde la página **Factura servicio** y no desde el pedido de servicio en sí. Es posible que deba eliminar manualmente dichos pedidos facturados ejecutando el trabajo por lotes **Eliminar órdenes de servicio facturadas**.  

## Comprimir datos con compresión por fechas

Puede comprimir datos en [!INCLUDE [prod_short](includes/prod_short.md)] para ahorrar espacio en la base de datos, lo que en [!INCLUDE [prod_short](includes/prod_short.md)] en línea también puede ahorrarle dinero. La compresión, basada en fechas y trabajos, fusiona diversos movimientos antiguos en uno solo.

Puede comprimir entradas que cumplan todas las siguientes condiciones:

* Son de años fiscales cerrados.
* El campo **Abrir** se establece en **No**.
* Tienen al menos cinco años. Si desea comprimir datos que tengan menos de cinco años, comuníquese con su socio de Microsoft.

Así, por ejemplo, los movimientos de proveedores de ejercicios anteriores se pueden comprimir, de forma que sólo haya una entrada al haber y otra al debe cada mes. El importe del nuevo movimiento es la suma de todos los comprimidos. La fecha asignada es la fecha inicial del periodo a comprimir; por ejemplo, el primer día del mes (si los movimientos se comprimen por meses). Después de la compresión, aún podrá ver el saldo del periodo de cada cuenta del ejercicio anterior.

El número de movimientos resultante de una compresión de datos dependerá del número de filtros aplicados, de los campos que se combinen y de la longitud del periodo seleccionado. Siempre hay, al menos, un movimiento. Cuando termine el trabajo por lotes, podrá ver el resultado en la página **Registros de compresión por fechas**.

Puede comprimir los siguientes tipos de datos usando trabajos por lotes.

* Entradas de finanzas: movimientos de contabilidad (G/L), movimientos de impuesto sobre el valor agregado (IVA), movimientos de banco, movimientos de presupuesto, movimientos de contabilidad de clientes y movimientos de contabilidad de proveedores.
* Movimientos almacén
* Movimientos de recursos
* Movimientos de presupuesto de productos
* Movimientos de activos fijos, movimientos de mantenimiento de activos fijos y movimientos de cobertura de seguro de activos fiojs.

Cuando define criterios para la compresión, puede mantener el contenido de ciertos campos utilizando las opciones de **Guardar contenido campo**. Los campos disponibles dependen de los datos que está comprimiendo.

> [!NOTE]
> Antes de que pueda ejecutar la compresión de fechas, sus vistas de análisis deben estar actualizadas. Más información en la sección [Actualizar una vista de análisis](bi-how-analyze-data-dimension.md#update-an-analysis-view).

Después de la compresión, siempre se retiene el contenido de los siguientes campos: **Fecha de registro**, **N.º proveedor**, **Tipo de documento**, **Código de divisa**, **Grupo contable**, **Importe**, **Importe pendiente**, **Importe inicial (DL)**, **Importe pendiente (DL)**, **Importe (DL)**, **Beneficio (DL)**, **Dto. factura (DL)**, **Dto. P.P (DL)** y **Posible descuento P.P.**.

## Publicar entradas comprimidas

Las entradas comprimidas se publican de forma ligeramente diferente a la publicación estándar. Esta diferencia es para reducir el número de nuevos movimientos de contabilidad creados por la compresión de fechas, y es especialmente importante cuando mantiene información como dimensiones y números de documentos. La compresión de fechas crea nuevas entradas de la siguiente manera:

* En la página **Movimientos de contabilidad**, se crean nuevas entradas para las entradas comprimidas. El campo **Descripción** contiene **Comprimido por fechas** para que las entradas comprimidas sean fáciles de identificar. 
* En las páginas del libro mayor, como la página **Movimientos de contabilidad**, se crean uno o más movimientos nuevos. 

El proceso de contabilización crea espacios en la serie de números para las entradas de la página **Movimientos de contabilidad**. Esos números se asignan solo a las entradas en las páginas del libro mayor. El rango de números que se asignó a los movimientos está disponible en la página **Registro de P/G**, en los campos **Desde el número de movimiento** y **Hasta el número de movimiento**. 

> [!NOTE]
> Después de ejecutar la compresión de fechas, no puede revertir los asientos del proveedor o del banco para ninguna transacción que se vea afectada por la compresión.

El número de movimientos resultante de una compresión de datos dependerá del número de filtros aplicados, de los campos que se combinen y de la longitud del periodo seleccionado. Siempre hay, al menos, un movimiento.

> [!WARNING]
> La compresión por fechas borra movimientos, por tanto es recomendable que haga siempre una copia de seguridad de la base de datos antes de ejecutar el proceso.

### Para ejecutar compresión por fechas

1. Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "Icono Buscar página o informe"), introduzca **Administración de datos** y, a continuación, seleccione el vínculo relacionado.
2. Realice una de las siguientes acciones, en función de sus necesidades:
    * Para utilizar una guía asistida para configurar la compresión de fechas para uno o más tipos de datos, elija **Guía de administración de datos**.
    * Para configurar la compresión para un tipo individual de datos, elija **Compresión de datos**, **Comprimir movimientos** y, a continuación, elija los datos que desee comprimir.

   > [!NOTE]
   > Solo puede comprimir datos que tengan más de cinco años. Si desea comprimir datos que tengan menos de cinco años, comuníquese con su socio de Microsoft. Deben utilizar el evento `OnSetMinimumNumberOfYearsToKeep` en la codeunit "Compresión de fecha" para establecer el umbral.


## Consulte también

[Administración](admin-setup-and-administration.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
