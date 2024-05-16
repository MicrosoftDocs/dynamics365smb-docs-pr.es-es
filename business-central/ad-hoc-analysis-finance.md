---
title: Análisis ad-hoc de datos financieros
description: Aprenda a usar el modo de análisis de datos para analizar datos financieros.
author: kennienp
ms.author: kepontop
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'bi, power BI, analysis, KPI'
ms.search.form: '516, 9300, 5119, 9301, 9305'
ms.date: 05/02/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---

# <a name="ad-hoc-analysis-of-finance-data"></a>Análisis ad-hoc de datos financieros

En este artículo se explica cómo usar la característica de **Análisis de datos** para analizar datos financieros directamente de las páginas de lista y consultas. No es necesario ejecutar un informe ni cambiar a otra aplicación, como Excel. La característica proporciona una forma interactiva y versátil de calcular, resumir y examinar datos. En lugar de ejecutar informes con opciones y filtros, puede agregar varias pestañas que representen diferentes tareas o vistas de los datos. Algunos ejemplos son "Activos totales a lo largo del tiempo", "Clientes", "Proveedores" o cualquier otra vista que pueda imaginar. Para obtener más información sobre cómo utilizar la característica **Análisis de datos**, vaya a [Analizar datos de lista y consulta con el modo de análisis](analysis-mode.md).

Utilice las páginas de la lista siguiente para empezar a realizar análisis ad hoc de los procesos financieros:

- [Movs. contabilidad](https://businesscentral.dynamics.com/?page=20)
- [Movs. clientes](https://businesscentral.dynamics.com/?page=25)
- [Movs. proveedores](https://businesscentral.dynamics.com/?page=29)

## <a name="finance-ad-hoc-analysis-scenarios"></a>Escenarios de análisis ad hoc de finanzas

Utilice la característica **Análisis de datos** para una verificación rápida de hechos y un análisis ad hoc:

- Si no desea ejecutar un informe.
- Si no existe un informe para su necesidad específica.
- Si desea iterar rápidamente para obtener una buena descripción general de una parte de su negocio.

Las siguientes secciones proporcionan ejemplos de escenarios de finanzas en [!INCLUDE [prod_short](includes/prod_short.md)].

| Área | Para... | Abrir esta página en de análisis | Uso de estos campos |
| ---- | ----- | ------------------------------- |------------------- |
| [Finance (Clientes)](#example-finance-accounts-receivables) | Vea lo que sus clientes le deben, por ejemplo, desglosado en intervalos de tiempo para saber cuándo vencen los importes. | [Movs. clientes](https://businesscentral.dynamics.com/?page=25) | **Nombre del cliente**, **Fecha de vencimiento** e **Importe restante** |
| [Finance (Proveedores)](#example-finance-accounts-payable) | Vea lo que debe a sus proveedores, quizás desglosado en intervalos de tiempo para saber cuándo vencen los importes. | [Movs. proveedores](https://businesscentral.dynamics.com/?page=29) | **Nombre del proveedor**, **Tipo de documento**, **N.º de documento**, **Año de fecha de vencimiento**, **Mes de fecha de vencimiento** e **Importe restante**. |
| [Finance (Extracto de ingresos)](#example-finance-income-statement) | Vea sus ingresos en las cuentas de ingresos del plan de cuentas, por ejemplo, desglosados en intervalos de tiempo según los cuales se contabilizaron los importes. | [Movs. contabilidad](https://businesscentral.dynamics.com/?page=20) | **Número de cuenta de mayor**, **Fecha registro** e **Importe**. |
| [Finance (total activo)](#example-finance-total-assets) | Vea sus activos en las cuentas de activos del plan de cuentas, por ejemplo, desglosados en intervalos de tiempo según los cuales se contabilizaron los importes. | [Movs. contabilidad](https://businesscentral.dynamics.com/?page=20) | **Número de cuenta de mayor**, **Fecha registro** e **Importe**. |

### <a name="example-finance-accounts-receivables"></a>Ejemplo: Finance (Cobros)

Para ver lo que sus clientes le deben, quizás desglosado en intervalos de tiempo para saber cuándo vencen los importes, siga estos pasos:

1. Abra la lista [Movimientos de cliente](https://businesscentral.dynamics.com/?page=25) y elija :::image type="content" source="media/analysis-mode-icon.png" alt-text="Entrar en el modo de análisis."::: para activar el modo de análisis.
1. Vaya al menú **Columnas** y elimine todas las columnas (seleccione la casilla junto al campo *Buscar* a la derecha).
1. Active la opción **Modo* dinámico** (ubicada encima del campo **Buscar** de la derecha).
1. Arrastre el campo **Nombre del cliente** al área **Grupos de filas** y arrastre **Importe restante** hacia el área **Valores**.
1. Arrastre el campo **Fecha de vencimiento (mes)** y arrástrelo al área **Etiquetas de columna**.
1. Para realizar el análisis para un año o trimestre determinado, aplique un filtro en el menú **Filtros de análisis** (ubicado debajo del menú **Columnas** de la derecha).
1. Cambie el nombre de su pestaña de análisis a **Cuentas antiguas por mes** o algo que describa este análisis.

### <a name="example-finance-accounts-payable"></a>Ejemplo: Finance (Proveedores)

Para ver lo que debe a sus proveedores, quizás desglosado en intervalos de tiempo para saber cuándo vencen los importes, siga estos pasos:

1. Abra la página de la lista [Movs. proveedores](https://businesscentral.dynamics.com/?page=29) y elija :::image type="content" source="media/analysis-mode-icon.png" alt-text="Entrar en el modo de análisis."::: para activar el modo de análisis.
1. Vaya al menú **Columnas** y elimine todas las columnas (seleccione la casilla junto al campo **Buscar**).
1. Active la opción **Modo dinámico** (ubicada encima del campo **Buscar** de la derecha).
1. Arrastre los campos **Nombre del proveedor**, **Tipo de documento** y **N.º de documento** al área **Grupos de filas** y luego arrastre el campo **Importe restante** al área **Valores**.
1. Arrastre los campos **Año de fecha de vencimiento** y **Mes de fecha de vencimiento** al área **Etiquetas de columna**. Arrastra los campos en ese orden.
1. Para realizar el análisis para un año o trimestre determinado, aplique un filtro en el menú **Filtros de análisis** (ubicado debajo del menú **Columnas** de la derecha).
1. Cambie el nombre de su pestaña de análisis a **Antigüedad de pagos por mes** o algo que describa este análisis.

La siguiente imagen muestra el resultado de estos pasos.

:::image type="content" source="media/data-analysis-vendor-ledger-entries.png" alt-text="Ejemplo de cómo realizar análisis de datos en la página Movimientos de cliente" lightbox="media/data-analysis-vendor-ledger-entries.png":::

### <a name="example-finance-income-statement"></a>Ejemplo: Finance (Extracto de ingresos)

Para ver sus ingresos en las cuentas de ingresos del plan de cuentas, desglosados en intervalos de tiempo según los cuales se contabilizaron los importes, siga estos pasos:

1. Abra la lista [Movs. contabilidad](https://businesscentral.dynamics.com/?page=20) y elija :::image type="content" source="media/analysis-mode-icon.png" alt-text="Entrar en el modo de análisis."::: para activar el modo de análisis.
1. Vaya al menú **Columnas** y elimine todas las columnas (seleccione la casilla junto al campo **Buscar**).
1. Active la opción **Modo dinámico** (ubicada encima del campo **Buscar** de la derecha).
1. Arrastre el campo **Número de cuenta de mayor** al área **Grupos de filas** y arrastre **Importe** hacia el área **Valores**.
1. Arrastre el campo **Mes de fecha de contabilización** y arrástrelo al área **Etiquetas de columna**.
1. Para la cuenta de resultados, filtre las cuentas que utiliza. En los datos de demostración [!INCLUDE [prod_short](includes/prod_short.md)], estas cuentas comienzan con "4", pero su plan de cuentas puede ser diferente. Establezca un filtro en las cuentas en el menú **Filtros de análisis** (que se encuentra debajo del menú **Columnas** de la derecha).

   > [!TIP]
   > Para ver fácilmente qué cuentas se utilizan en su configuración, ejecute el informe [Balance de comprobación por periodo](https://businesscentral.dynamics.com/?report=38).

1. Cambie el nombre de su pestaña de análisis a **Ingresos por mes** o algo que describa este análisis.

### <a name="example-finance-total-assets"></a>Ejemplo: Finance (total activo)

Para ver sus activos en las cuentas de activos del plan de cuentas, desglosados en intervalos de tiempo según los cuales se contabilizaron los importes, haga lo siguiente.

1. Abra la lista [Movs. contabilidad](https://businesscentral.dynamics.com/?page=20) y elija :::image type="content" source="media/analysis-mode-icon.png" alt-text="Entrar en el modo de análisis."::: para activar el modo de análisis.
1. Vaya al menú **Columnas** y elimine todas las columnas (seleccione la casilla junto al campo **Buscar** a la derecha).
1. Active la opción **Modo dinámico** (ubicada encima del campo **Buscar** de la derecha).
1. Arrastre el campo **Número de cuenta de mayor** al área **Grupos de filas** y arrastre **Importe** hacia el área **Valores**.
1. Arrastre el campo **Mes de fecha de contabilización** y arrástrelo al área **Etiquetas de columna**.
1. Para el estado de cuenta de activos totales, filtre las cuentas que utiliza. En los datos de demostración [!INCLUDE [prod_short](includes/prod_short.md)], estas cuentas comienzan con "10", pero su plan de cuentas puede ser diferente. Establezca un filtro en las cuentas apropiadas en el menú **Filtros adicionales** (ubicado debajo del menú **Columnas** de la derecha).

   > [!TIP]
   > Para ver fácilmente qué cuentas se utilizan en su configuración, ejecute el informe [Balance de comprobación por periodo](https://businesscentral.dynamics.com/?report=38).

1. Cambie el nombre de su pestaña de análisis a **Ingresos por mes** o algo que describa este análisis.

## <a name="data-foundation-for-ad-hoc-analysis-on-finance"></a>Base de datos para análisis ad hoc de finanzas

Cuando contabiliza diarios, [!INCLUDE [prod_short](includes/prod_short.md)] crea entradas en la tabla **Mov. contabilidad**. Por lo tanto, el análisis ad hoc sobre finanzas generales generalmente se realiza en la página [Movs. Contabilidad](https://businesscentral.dynamics.com/?page=20) . Para cobros y pagos, puede analizar [Movimiento de clientes](https://businesscentral.dynamics.com/?page=25) y [Movimiento de proveedores](https://businesscentral.dynamics.com/?page=29), respectivamente.

Para obtener más información, vaya a los siguientes artículos:

- [Base de datos para análisis ad hoc de ventas](ad-hoc-analysis-sales.md#data-foundation-for-ad-hoc-analysis-on-sales)
- [Base de datos para análisis ad hoc de compras](ad-hoc-analysis-purchasing.md#data-foundation-for-ad-hoc-analysis-on-purchasing)

## <a name="see-also"></a>Consulte también

[Analizar datos de lista y consulta con el modo de análisis](analysis-mode.md)  
[Información general del análisis financiero](bi.md)  
[Descripción general de análisis, inteligencia empresarial e informes](reports-bi-reporting.md)  
[Información general sobre finanzas](finance.md)   
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  

[!INCLUDE[footer-include](includes/footer-banner.md)]
