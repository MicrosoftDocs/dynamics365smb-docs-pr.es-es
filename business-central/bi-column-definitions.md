---
title: Definiciones de columnas en Financial Reporting
description: Describe cómo funcionan las definiciones de columnas en los informes financieros.
author: kennieNP
ms.author: kepontop
ms.reviewer: bnielse
ms.topic: how-to
ms.date: 03/27/2024
ms.custom: bap-template
ms.search.keywords: 'bi, power BI, analysis, KPI, account schedule, financial report'
ms.search.form: '103, 104, 108, 195, 196, 197, 198, 489, 490, 764, 765, 766'
ms.service: dynamics-365-business-central
---

# <a name="column-definitions-in-financial-reporting"></a>Definiciones de columnas en Financial Reporting

Utilice las definiciones de columnas para especificar las columnas para incluir en un informe. Por ejemplo, puede diseñar una plantilla de informe para comparar el saldo del periodo y el saldo a la fecha del mismo periodo del año actual y del año anterior. Puede tener hasta 15 columnas en una definición de columna. Por ejemplo, las columnas múltiples son útiles para mostrar los presupuestos de 12 meses con una columna que muestre el total.

## <a name="create-or-edit-a-column-definition"></a>Crear o editar una definición de columna

Para crear o editar una definición de columna, siga estos pasos.

> [!NOTE]
> Las versiones impresas, guardadas o de vista preliminar de un informe financiero muestran como máximo cinco columnas. En cambio, si un informe financiero solo está destinado al análisis en la página **Informe financiero**, puede crear tantas columnas como desee.

1. En la página **Informes financieros**, seleccione el informe financiero pertinente y, a continuación, elija la acción **Editar definición de columna**.
1. En la página **Definición de columna**, cree una fila para cada columna de datos financieros mostrada en el informe financiero. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
1. Elija **Aceptar**.
1. Abra la página **Informe financiero** de vez en cuando para verificar que la nueva definición de columna funciona del modo previsto.

## <a name="built-in-column-definitions"></a>Definiciones de columna integradas

[!INCLUDE[prod_short](includes/prod_short.md)] proporciona ejemplos de definiciones de columnas que pueden ayudarle a comenzar rápidamente a configurar informes financieros que se adapten a sus necesidades.

<!-- update this when we release the new templates in 24.1
| Column definition code | Description | How to use this column definition | 
| ------------------- | ----------- | ------------------------------ | 
| TBA 1 | TBA 1 | TBA 1 |
| TBA 2 | TBA 2 | TBA 2 |
| TBA 3 | TBA 3 | TBA 3 |
| TBA 4 | TBA 4 | TBA 4 |
-->

## <a name="example-create-a-column-definition-to-calculate-percentages"></a>Ejemplo: Crear una definición de columna para calcular porcentajes

Podría desear incluir una columna en un informe financiero para calcular los porcentajes de un total. Por ejemplo, si tiene filas que detallan las ventas por dimensión, podría desear crear una columna para indicar el porcentaje de las ventas totales en cada fila.

1. Elija el icono ![Bombilla que abre la característica Dígame 2.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Informes financieros** y luego elija el vínculo relacionado.
1. En la página **Informes financieros**, seleccione un informe financiero.  
1. Elija la acción **Editar informe financiero** para configurar un informe financiero para calcular el total en el que se basarán los porcentajes.  
1. Agregue una línea justo encima de la primera fila para la que desea que se muestre un porcentaje.  
1. Rellene los campos de la línea como se indica a continuación: 
    1. En el campo **Tipo sumatorio**, introduzca **Fijar base para porcentaje**. 
    1. En el campo **Sumatorio**, introduzca una fórmula para el total en el que el porcentaje se basa. Por ejemplo, si la fila 11 contiene las ventas totales, escriba **11**.  
1. Elija la acción **Editar definición de columna** para configurar una columna.  
1. Rellene los campos de la línea como se indica a continuación. 
    1. En el campo **Tipo columna**, seleccione **Fórmula**. 
    1. En el campo **Fórmula**, introduzca una fórmula para el importe para el que desea calcular un porcentaje, seguida del signo de porcentaje (%). Por tanto, si el número de columna N contiene los saldos periodos, escriba **N%**.  
1. Repita los pasos del 4 al 7 para cada grupo de filas que desee subdividir por porcentaje.

## <a name="comparing-accounting-periods-using-period-formulas"></a>Comparación de períodos contables usando fórmulas de períodos

El informe financiero puede comparar los resultados de diferentes períodos contables, como el mes pasado en comparación con el mismo mes del año anterior. Para ello, abra la página **Definición de columna** y personalícela agregando el campo **Fórmula del período de comparación** como columna. Obtenga más información en [Personalizar el área de trabajo](ui-personalization-user.md). A continuación, puede establecer ese campo en una fórmula de período.  

Un período contable no necesita coincidir con el calendario. Sin embargo, cada año fiscal debe tener el mismo número de periodos contables, aunque cada periodo tenga una duración diferente.  

[!INCLUDE[prod_short](includes/prod_short.md)] utiliza la fórmula de periodo para calcular la duración del periodo comparativo en relación con el periodo representado por el filtro de fecha del informe. El periodo de comparación se basa en el periodo de la fecha de inicio del filtro fecha. La siguiente tabla muestra las abreviaturas de las especificaciones de período.

| Siglas | Descripción                                                                           |
| ------------ | ------------------------------------------------------------------------------------- |
| P            | Período.                                                                                |
| LP           | Último periodo de un año fiscal, medio año o trimestre.                                   |
| CP           | Periodo actual de un año fiscal, medio año o trimestre. Use CP en fórmulas para establecer el período que comienza o finaliza la fórmula. Por ejemplo, FY\[1..CP\] denota el tiempo desde el comienzo del año fiscal actual hasta el período actual.|
| FY           | Año fiscal. Por ejemplo, FY\[1..3\] indica el primer trimestre del año fiscal actual. |

Ejemplos de fórmulas:

| Fórmula | Descripción |
|-----|-----|
| \<Blank\>       | Periodo actual. |
| \-1P            | Período anterior.            |
| \-1FY\[1..LP\]  | Todo el año fiscal anterior.                  |
| \-1FY           | Periodo actual del año fiscal anterior.       |
| \-1FY\[1..3\]   | Primer trimestre del año fiscal anterior.        |
| \-1FY\[1..CP\]  | Desde el principio del año fiscal anterior hasta el periodo actual en el año fiscal anterior, ambos periodos inclusive. |
| \-1FY\[CP..LP\] | Desde el periodo actual en el año fiscal anterior hasta el último periodo del año fiscal anterior, ambos periodos inclusive.   |

Para calcular el importe del periodo de comparación para periodos de tiempo regulares, debe introducir una fórmula en el campo **Fórmula fecha comparación**. Por ejemplo, si el campo está establecido en -1Y, [!INCLUDE [prod_short](includes/prod_short.md)] compara con el mismo periodo de un de año antes.

> [!NOTE]
> No siempre es obvio qué períodos está comparando porque puede establecer un filtro de fecha en un informe que abarca diferentes fechas a los períodos contables del plan de cuentas. Por tanto, si crea un informe financiero en el que desee comparar este período con el mismo período del año anterior, por lo que debe establecer el campo **Fórmula fecha comparación** en **-1FY**. Luego, ejecute el informe el **28 de febrero** y configure el filtro de fecha en **enero y febrero**. Como resultado, el informe financiero compara enero y febrero de este año con enero del año pasado, que es el único período contable completado de los dos para el año pasado.  

Obtenga más información en [Trabajar con fechas y horas del calendario](ui-enter-date-ranges.md).

[!INCLUDE [report-best-practices-column-defs](includes/report-best-practices-column-defs.md)]

## <a name="import-or-export-financial-report-column-definitions"></a>Importar o exportar definiciones de columna de informes financieros

A partir del primer lanzamiento de versiones de 2024 (versión 24.1), puede importar y exportar definiciones de columnas de informes financieros como paquetes de configuración de RapidStart. Por ejemplo, los paquetes de configuración resultan útiles para compartir información con otras empresas. El paquete se crea en un archivo .rapidstart, que comprime los contenidos.

> [!NOTE]
> Cuando importe definiciones de columnas de informes financieros, los registros existentes con los mismos nombres que los que está importando se sustituyen por las nuevas definiciones. El paquete de configuración para una definición de informe no sobrescribirá ninguna definición de fila o columna existente que se utilice en la definición de informe.

Para importar o exportar definiciones de columna de informes financieros, siga estos pasos:

1. Elija el icono ![Bombilla que abre la característica Dígame 4.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Definiciones de columna** y luego elija el vínculo relacionado.
1. Seleccione la definición de línea y, a continuación, elija la acción **Importar definición de columna** o **Exportar definición de columna** en función de lo que desee hacer.

## <a name="see-also"></a>Consulte también

[Definiciones de filas en informes financieros](bi-row-definitions.md)  
[Preparar informes financieros](bi-how-work-account-schedule.md)  
[Inteligencia empresarial financiera](bi.md)  
[Finanzas](finance.md)  
[Configurar las finanzas](finance-setup-finance.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
