---
title: Análisis ad-hoc de datos de inventario
description: Aprenda a usar el modo de análisis de datos para analizar datos de inventario.
author: kennienp
ms.author: kepontop
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'bi, power BI, analysis, KPI'
ms.search.form: '516, 9300, 5119, 9301, 9305'
ms.date: 05/03/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---

# Análisis ad-hoc de datos de inventario

En este artículo se explica cómo usar la característica de **Análisis de datos** para analizar datos de inventario directamente de las páginas de lista y consultas. No es necesario ejecutar un informe ni cambiar a otra aplicación, como Excel. La característica proporciona una forma interactiva y versátil de calcular, resumir y examinar datos. En lugar de ejecutar informes con opciones y filtros, puede agregar varias pestañas que representen diferentes tareas o vistas de los datos. Algunos ejemplos son "existencias a punto de expirar" o "los más vendidos", o cualquier otra vista que pueda imaginar. Para obtener más información sobre cómo utilizar la característica **Análisis de datos**, vaya a [Analizar datos de lista y consulta con el modo de análisis](analysis-mode.md).

Utilice las siguientes páginas de lista para análisis ad hoc de procesos de inventario:

- [Movs. productos](https://businesscentral.dynamics.com/?page=38)

## Escenarios de análisis ad hoc de inventario

Utilice la característica **Análisis de datos** para una verificación rápida de hechos y un análisis ad hoc:

- Si no desea ejecutar un informe.
- Si no existe un informe para su necesidad específica.
- Si desea iterar rápidamente para obtener una buena descripción general de una parte de su negocio.

Las siguientes secciones proporcionan ejemplos de escenarios de inventario en [!INCLUDE [prod_short](includes/prod_short.md)].

| Área | Para... | Abrir esta página en de análisis | Uso de estos campos |
| ---- | ----- | ------------------------------- |------------------- |
| [Inventario disponible](#example-inventory-on-hand) | Obtenga una descripción general de los artículos que están disponibles en su inventario. | [Movs. productos](https://businesscentral.dynamics.com/?page=38) | **N.º producto**, **Cantidad pendiente** |
|[Ejemplo: seguimiento de existencias antiguas o expiradas](#example-track-expiring-or-old-stock) | Obtenga una descripción general de los artículos de su inventario que han estado en existencias durante mucho tiempo y no se venden bien. | [Movs. productos](https://businesscentral.dynamics.com/?page=38) | **Año de fecha de registro**, **Mes de fecha de contabilización**, **N.º producto**, **Fecha de registro**, **Tipo movimiento**, **Cantidad** y **Cantidad pendiente**. |
| [Artículos devueltos por motivo de devolución](#example-returned-items-by-return-reason) | Obtenga una descripción general de los productos que devuelven los clientes, clasificados por el motivo de la devolución. Utilice esto para análisis de control de calidad. | [Movs. productos](https://businesscentral.dynamics.com/?page=38) | **Cód. motivo dev.**, **Mes de fecha de contabilización**, **Cantidad** , **Importe coste**, **Fecha de registro**, **Tipo documento**, **N.º producto** y **N.º de documento**. |
| Rendimiento del inventario | Obtenga una descripción general de las compras y ventas de su inventario por mes o trimestre. | [Movs. productos](https://businesscentral.dynamics.com/?page=38) | **Año de fecha de registro**, **Mes de fecha de contabilización**, **N.º producto**, **Cantidad**, **Importe ventas**, **Importe coste (Real)** y **Mes de fecha de contabilización** |
| [Movimientos de inventario] | Obtenga una descripción general de cómo se mueven los productos de su inventario entre ubicaciones. | [Movs. productos](https://businesscentral.dynamics.com/?page=38) | **Código de ubicación**, **Cantidad**, **Fecha de registro**, **N.º producto** |

## Ejemplo: Inventario disponible

Para analizar los artículos de su inventario que están en stock, siga estos pasos:

1. Abra la lista [Movimientos contables de producto](https://businesscentral.dynamics.com/?page=38) y elija :::image type="content" source="media/analysis-mode-icon.png" alt-text="Entrar en el modo de análisis."::: para activar el modo de análisis.
1. Vaya al menú **Columnas** y elimine todas las columnas (seleccione la casilla junto al campo **Buscar**).
1. Arrastre el campo **N.º producto** al área **Grupos de filas**. Arrastra los campos en ese orden.
1. Arrastre el campo **Cantidad pendiente** al área **Valores**.
1. Establezca un filtro **No es igual** en **0** en **Cantidad pendiente**. Si no permite niveles de stock negativos, establezca un filtro **Mayor de** en **0**.
1. Opcionalmente, agregue otros campos al análisis y tal vez gire en función de la ubicación u otros campos.
1. Cambie el nombre de su pestaña de análisis a **Inventario a mano** o algo que describa este análisis.

La siguiente imagen muestra el resultado de estos pasos.

:::image type="content" source="media/data-analysis-inventory-on-hand.png" alt-text="Ejemplo de cómo hacer un análisis de datos de inventario disponible." lightbox="media/data-analysis-inventory-on-hand.png":::

## Ejemplo: seguimiento de existencias antiguas o expiradas

Para analizar artículos de su inventario que han estado en existencias durante mucho tiempo y no se venden bien, siga estos pasos:

1. Abra la lista [Movimientos contables de producto](https://businesscentral.dynamics.com/?page=38) y elija :::image type="content" source="media/analysis-mode-icon.png" alt-text="Entrar en el modo de análisis."::: para activar el modo de análisis.
1. Vaya al menú **Columnas** y elimine todas las columnas (seleccione la casilla junto al campo **Buscar** a la derecha).
1. Arrastre los campos **Año de fecha de publicación**, **Mes de fecha de contabilización** y **N.º producto** al área **Grupos de filas**. Arrastre los campos en ese orden.
1. En el área **Columnas**, elija los campos **Fecha de registro**, **Tipo movimiento**, **Cantidad**, y **Cantidad pendiente**.
1. Establezca un filtro **Menor de** a **Fecha de registro** para definir lo que quiere decir con "antiguo".
1. Cambie el nombre de su pestaña de análisis a **Existencias antiguas** o algo que describa este análisis.

La siguiente imagen muestra el resultado de estos pasos.

:::image type="content" source="media/data-analysis-inventory-dead-stock.png" alt-text="Ejemplo de cómo realizar análisis de datos de stock muerto en la página Movimientos de productos" lightbox="media/data-analysis-inventory-dead-stock.png":::

## Ejemplo: artículos devueltos por motivo de devolución

Para analizar los artículos devueltos ordenados por los motivos de su devolución, siga estos pasos:

1. Abra la lista [Movs. productos](https://businesscentral.dynamics.com/?page=38).
1. Agregue el campo **Cód. motivo dev.** personalizando la página. En el menú **Configuración**, elija **Personalizar**.
1. Salga del modo de personalización.
1. Elija :::image type="content" source="media/analysis-mode-icon.png" alt-text="Entrar en el modo de análisis."::: para activar el modo de análisis.
1. Vaya al menú **Columnas** y elimine todas las columnas (seleccione la casilla junto al campo **Buscar** a la derecha).
1. Arrastre los campos **Cód. motivo dev.** y **Mes de fecha de contabilización** al área **Grupos de filas**. Arrastre los campos en ese orden.
1. Arrastre los campos **Cantidad** e **Importe coste** al área **Valores**.
1. Agregue cualquier otro campo que desee en el análisis y habilítelo en el área **Columnas**. Por ejemplo, puede agregar **Fecha de registro**, **Tipo documento**, **N.º producto** y **N.º de documento**.
1. Cambie el nombre de su pestaña de análisis a **Artículos devueltos por motivo de devolución** o algo que describa este análisis.  

## Ejemplo: rendimiento del inventario

1. Abra la lista [Movimientos contables de producto](https://businesscentral.dynamics.com/?page=38) y elija :::image type="content" source="media/analysis-mode-icon.png" alt-text="Entrar en el modo de análisis."::: para activar el modo de análisis.
1. Vaya al menú **Columnas** y elimine todas las columnas (seleccione la casilla junto al campo **Buscar** a la derecha).
1. Active la opción **Modo dinámico** (ubicada encima del campo **Buscar** de la derecha).
1. Arrastre los campos **Año de fecha de publicación**, **Mes de fecha de contabilización** y **N.º producto** al área **Grupos de filas**.
1. Arrastre los campos **Cantidad**, **Importe ventas** e **Importe coste (Real)** al área **Valores**.
1. Arrastre el campo **Mes de fecha de contabilización** y arrástrelo al área **Grupos de columnas**.
1. Cambie el nombre de su pestaña de análisis a **Rendimiento de inventario por mes** o algo que describa este análisis para usted.  

## Movimientos de inventario

Para realizar un seguimiento de los movimientos de inventario entre ubicaciones, siga estos pasos:

1. Abra la lista [Movimientos contables de producto](https://businesscentral.dynamics.com/?page=38) y elija :::image type="content" source="media/analysis-mode-icon.png" alt-text="Entrar en el modo de análisis."::: para activar el modo de análisis.
1. Vaya al menú **Columnas** y elimine todas las columnas (seleccione la casilla junto al campo **Buscar** a la derecha).
1. Arrastre el campo **Código de almacén** al área **Grupos de filas**.
1. Arrastre el campo **Cantidad** al área **Valores**.
1. Agregue cualquier otro campo que desee en el análisis y habilítelo en el área **Columnas**. Por ejemplo, puede agregar el campo **N.º producto** .
1. Cambie el nombre de su pestaña de análisis a **Movimientos de inventario** o algo que describa este análisis.  

   > [!TIP]
   > Si agrega el campo Fecha de publicación, también puede realizar un seguimiento de los movimientos a lo largo del tiempo.

## Base de datos para análisis ad hoc de inventario

Cuando se registra un pedido de venta, [!INCLUDE [prod_short](includes/prod_short.md)] actualiza la cuenta del cliente, la contabilidad general y los movimientos de producto.

- Para cada línea de pedido de ventas, se crea un movimiento contable de producto en la tabla **Mov. producto** (si las líneas de ventas contienen números de producto). Además, los pedidos de venta siempre se registran en las tablas **Histórico cab. albarán venta** e **Histórico cab. factura venta**. Para obtener más información sobre el registro de ventas, vaya a [Registro de ventas](ui-post-sales.md).

Cuando registra un documento de compra, [!INCLUDE [prod_short](includes/prod_short.md)] actualiza la cuenta del proveedor, la contabilidad, los movimientos de producto y los movimientos de recursos.

- Para cada línea de compra, según corresponda, se crean asientos en la tabla **Mov. producto** (si la línea de compra es del tipo de producto). Además, los documentos de compra siempre se registran en las tablas **Histórico cab. albarán compra** e **Histórico cab. factura compra**. Obtenga más información, vaya a [Registrar compras](purchasing-how-record-purchases.md#posting-purchases).

## Consulte también

[Analizar datos de lista y consulta con el modo de análisis](analysis-mode.md)  
[Información general de análisis de inventario](inventory-analytics-overview.md)  
[Descripción general de análisis, inteligencia empresarial e informes](reports-bi-reporting.md)  
[Información general de inventario](inventory-manage-inventory.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  

[!INCLUDE[footer-include](includes/footer-banner.md)]