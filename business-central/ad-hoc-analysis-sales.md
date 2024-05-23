---
title: Análisis ad-hoc de datos de ventas
description: Aprenda a usar el modo de análisis de datos para analizar datos de ventas.
author: brentholtorf
ms.author: kepontop
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'bi, power BI, analysis, KPI'
ms.search.form: '516, 9300, 5119, 9301, 9305'
ms.date: 04/28/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---

# Análisis ad-hoc de datos de ventas

En este artículo se explica cómo usar la característica de **Análisis de datos** para analizar datos de ventas directamente de las páginas de lista y consultas. No es necesario ejecutar un informe ni cambiar a otra aplicación, como Excel. La característica proporciona una forma interactiva y versátil de calcular, resumir y examinar datos. En lugar de ejecutar informes con opciones y filtros, puede agregar varias pestañas que representen diferentes tareas o vistas de los datos. Algunos ejemplos son "Mis clientes" o "Estadísticas de ventas", o cualquier otra vista que pueda imaginar. Para obtener más información sobre cómo utilizar la característica **Análisis de datos**, vaya a [Analizar datos de lista y consulta con el modo de análisis](analysis-mode.md).

Utilice las siguientes páginas de lista para análisis ad hoc de procesos de ventas:

- [Pedidos de venta](https://businesscentral.dynamics.com/?page=9305)
- Movs. contabilidad
- [Movs. clientes](https://businesscentral.dynamics.com/?page=25)
- Movs. productos
- Hist. facturas venta
- Pedidos devolución venta

## Escenarios de análisis ad hoc de ventas

Utilice la característica **Análisis de datos** para una verificación rápida de hechos y un análisis ad hoc:

- Si no desea ejecutar un informe.
- Si no existe un informe para su necesidad específica.
- Si desea iterar rápidamente para obtener una buena descripción general de una parte de su negocio.

Las siguientes secciones proporcionan ejemplos de escenarios de ventas en [!INCLUDE [prod_short](includes/prod_short.md)].

| Área | Para... | Abrir esta página en de análisis | Uso de estos campos |
| ---- | ----- | ------------------------------- |------------------- |
| [Ventas (volumen de ventas esperado)](#example-sales-expected-sales-volume) | Analice su volumen de ventas esperado. | [Pedidos de venta](https://businesscentral.dynamics.com/?page=9305) | **Nombre cliente de venta**, **N.º de cliente de venta**, **N.º** , **Importe**, **Año de fecha de documento** y **Mes de fecha de documento**. |
| [Ventas (ventas de clientes por volumen)](#example-sales-customer-sales-by-volume) | Obtenga una rápida visión de los clientes que más compran o que más deben. | [Movs. clientes](https://businesscentral.dynamics.com/?page=25) | **Nombre del cliente**, **Documento núm.:**, **Importe** e **Importe pendiente**. |
| [Finance (Cobros)](#example-finance-accounts-receivables) | Vea lo que sus clientes le deben, por ejemplo, desglosado en intervalos de tiempo para saber cuándo vencen los importes. | [Movs. clientes](https://businesscentral.dynamics.com/?page=25) | **Nombre del cliente**, **Fecha de vencimiento** e **Importe restante**. |

## Ejemplo: Ventas (volumen de ventas esperado)

Para analizar el volumen de ventas esperado y los importes de ventas de pedidos no enviados para cada cliente por año o mes, siga estos pasos:

1. Abra la lista [Pedidos de venta](https://businesscentral.dynamics.com/?page=9305) y active el modo de análisis.
1. Vaya al menú **Columnas** y elimine todas las columnas (seleccione la casilla junto al campo **Buscar**).
1. Active el modo **Dinámico** (ubicado directamente encima del campo **Buscar**).
1. Arrastre los campos **Nombre cliente de venta**, **N.º de cliente de venta** y **N.º** al área **Grupos de filas**. Arrastra los campos en ese orden.
1. Arrastre el campo **Importe** al área **Valores**.
1. Arrastre los campos **Año de fecha de documento** y **Mes de fecha de documento** al área **Etiquetas de columna**. Arrastra los campos en ese orden.
1. Para hacer el análisis para un año o trimestre determinado, aplique un filtro en el menú **Filtros adicionales**. El menú está a la derecha de la página, justo debajo del menú **Columnas**.
1. Cambie el nombre de su pestaña de análisis a **Volumen de ventas previsto** o algo que describa este análisis para usted.

## Ejemplo: Ventas (ventas de clientes por volumen)

Para obtener una visión general de los clientes que más compran o que más deben, siga estos pasos:

1. Abre la lista [Movimientos de cliente](https://businesscentral.dynamics.com/?page=25) y active el modo de análisis.
1. Vaya al menú **Columnas** y elimine todas las columnas (seleccione la casilla junto al campo **Buscar**).
1. Arrastre el campo **Nombre del cliente** al área **Grupos de filas** y el campo **N.º de documento** debajo del mismo.
1. Elija los campos **Importe** e **Importe pendiente**.
1. Para hacer el análisis para un año o trimestre determinado, aplique un filtro en el menú **Filtros adicionales**. El menú está a la derecha de la página, justo debajo del menú **Columnas**.
1. Cambie el nombre de su pestaña de análisis a **Cliente por volumen de ventas** o algo que describa este análisis para usted.

La siguiente imagen muestra el resultado de estos pasos.

:::image type="content" source="media/data-analysis-customer-ledger-entries.png" alt-text="Ejemplo de cómo realizar análisis de datos en la página Movimientos de cliente" lightbox="media/data-analysis-customer-ledger-entries.png":::

## Ejemplo: Finance (Cobros)

Para ver lo que sus clientes le deben, quizás desglosado en intervalos de tiempo para saber cuándo vencen los importes, siga estos pasos:

1. Abre la lista [Movimientos de cliente](https://businesscentral.dynamics.com/?page=25) y active el modo de análisis.
1. En el menú **Columnas**, elimine todas las columnas (seleccione la casilla junto al campo **Buscar**).
1. Active el modo **Dinámico** (ubicado directamente encima del campo **Buscar**).
1. Arrastre el campo **Nombre del cliente** al área **Grupos de filas** y arrastre **el campo Importe restante** hacia el área **Valores**.
1. Arrastre el campo **Fecha de vencimiento (mes)** y arrástrelo al área **Etiquetas de columna**.
1. Para hacer el análisis para un año o trimestre determinado, aplique un filtro en el menú **Filtros adicionales**. El menú está a la derecha de la página, justo debajo del menú **Columnas**.
1. Cambie el nombre de su pestaña de análisis a **Cuentas antiguas por mes** o algo que describa este análisis para usted.

## Base de datos para análisis ad hoc de ventas

Después de introducir la información de un pedido de cliente y añadir todas las líneas del mismo, puede contabilizar el registro. El registro crea un envío y una factura. [!INCLUDE [prod_short](includes/prod_short.md)] actualiza la cuenta del cliente, la cuenta contable y los movimientos de productos:

- Para cada pedido de venta, se crea un movimiento de venta en la tabla **Mov. contabilidad**. Se crea también un movimiento en la cuenta de cliente de la tabla **Mov. cliente** y un movimiento de contabilidad en la cuenta de cliente correspondiente. Además, el registro del pedido puede dar como resultado un movimiento de IVA y uno de contabilidad para el importe de descuento.
- Por cada línea de pedido de venta, se creará un movimiento de producto en la tabla **Mov. producto** (si las líneas de venta contienen números de producto) o un movimiento de contabilidad en la tabla **Mov. contabilidad** (si las líneas de venta contienen una cuenta de contabilidad). Además, los pedidos de venta siempre se registran en las tablas **Histórico cab. albarán venta** e **Histórico cab. factura venta**.

Para obtener más información sobre el registro de ventas, vaya a [Registro de ventas](ui-post-sales.md).

## Consulte también

[Registro de ventas](ui-post-sales.md)  
[Analizar datos de lista y consulta con el modo de análisis](analysis-mode.md)  
[Información general de análisis de ventas](sales-analytics-overview.md)  
[Descripción general de análisis, inteligencia empresarial e informes](reports-bi-reporting.md)  
[Información general de ventas](sales-manage-sales.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  

[!INCLUDE[footer-include](includes/footer-banner.md)]