---
title: Cree informes financieros con esquemas de cuentas
description: Describe cómo utilizar los esquemas de cuentas para crear varias vistas e informes para analizar los datos de rendimiento financiero.
author: edupont04
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: bi, power BI, analysis, KPI
ms.search.form: 103, 104, 197, 196, 195, 198, 490, 764, 765, 766
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 780034b8c53e7bb1704e13d0b1a00158583c11db
ms.sourcegitcommit: 3acadf94fa34ca57fc137cb2296e644fbabc1a60
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 09/19/2022
ms.locfileid: "9531734"
---
# <a name="prepare-financial-reporting-with-account-schedules-and-account-categories"></a>Preparar informes financieros con esquemas de cuentas y categorías de cuentas

Use esquemas de cuentas para obtener información sobre los datos financieros almacenados en su plan de cuentas. Los esquemas de cuentas analizan cifras en cuentas de contabilidad y comparan los movimientos de contabilidad con los presupuestados. Los resultados se muestran en gráficos e informes en su área de trabajo, como el gráfico de flujo de efectivo y los informes Balance de ingresos y Balance.

Se obtiene acceso a estos dos informes, por ejemplo, con la acción **Estados financieros** en las áreas de trabajo de Business Manager y Contable.  

[!INCLUDE[prod_short](includes/prod_short.md)] proporciona esquemas de cuentas de muestra que puede usar de inmediato. También puede configurar sus propias filas y columnas para especificar las cifras que desea comparar. Por ejemplo, puede crear esquemas de cuentas para calcular márgenes de beneficios en dimensiones, como departamentos o grupos de clientes. El número de resultados financieros personalizados que puede crear es iilmitado.  

Configurar esquemas de cuentas requiere obtener una comprensión de los datos financieros del plan de cuentas. Por ejemplo, puede ver los movimientos de contabilidad como porcentajes de los movimientos de presupuesto, pero eso requiere la creación de presupuestos. Para obtener más información, consulte [Crear presupuestos contables](finance-how-create-budgets.md).

## <a name="account-schedules"></a>Esquemas de cuentas

Los esquemas de cuentas organizan las cuentas de su catálogo de cuentas de manera que facilitan la presentación de los datos. Puede configurar diversas plantillas para definir la información que desea extraer del plan de cuentas. Los esquemas de cuentas proporcionan un lugar para cálculos que no se puedan realizar directamente en el plan de cuentas. Por ejemplo, puede crear subtotales para grupos de cuentas y luego incluir ese total en otros totales. Otro ejemplo es para calcular márgenes de beneficios en dimensiones, como departamentos o grupos de clientes. Además, puede filtrar los movimientos y los movimientos presupuestarios, por ejemplo, por saldo periodo o importe debe.

También puede comparar dos o más esquemas de cuentas y plantillas de columnas mediante el uso de fórmulas, que le permite realizar estas acciones:

* Crear informes financieros personalizados.
* Crear tantos esquemas de cuentas como sean necesarios, cada uno de ellos con un nombre diferente.
* Configurar diversas plantillas de informes e imprimir estos con las cifras actuales.

## <a name="gl-account-categories"></a>Categorías de cuenta

Puede usar categorías de cuentas para cambiar el diseño de sus balances financieros. Después de configurar las categorías de cuentas en la página **Categorías de cuenta** y haya elegido la acción **Generar esquemas de cuentas**, se actualizan los esquemas de cuentas subyacentes para los informes financieros principales. La próxima vez que ejecute uno de estos informes, como el informe **Extracto del saldo**, se agregan los nuevos totales y subtotales en función de los cambios que haya realizado.

> [!NOTE]
> Las categorías de cuentas de nivel superior, como el nodo **Pasivo** son fijas y no puede agregar las suyas. Sin embargo, puede eliminar y agregar categorías de cuenta en niveles inferiores y cambiar su estructura para definir cómo aparece la programación de la cuenta relacionada en los informes.
>
> Se recomienda crear y estructurar sus propias categorías de cuentas de mayor de nivel inferior desde cero, en una jerarquía si es necesario, en lugar de tratar de reorganizar las existentes. Por ejemplo, puede reestructurar el nodo **Pasivo** para contener un nuevo nodo **Capital** seguido por los nodos **Pasivo circulante** y **Pasivos a largo plazo**.

## <a name="to-create-a-new-account-schedule"></a>Para crear un nuevo esquema de cuentas

Usar esquemas de cuentas para analizar cifras en cuentas de contabilidad o comparar los movimientos de contabilidad con los presupuestados. Por ejemplo, puede ver los movimientos de contabilidad como porcentajes de los movimientos de presupuesto.

Los esquemas de cuentas en la versión estándar de [!INCLUDE[prod_short](includes/prod_short.md)] son la base de los informes financieros estándar, que pueden no adaptarse a las necesidades de su empresa. Para crear rápidamente sus propios informes financieros, puede empezar por copiar un esquema de cuentas existente, como se describe en el paso 3.

> [!TIP]
> Después de crear un cuadro de cuenta, puede utilizar la página **Cuenta Descripción general del horario** para obtener una vista previa y validar el informe financiero que define el esquema de cuenta. Para abrir la página, elija la acción **Información general**.  

1. Elija el icono ![Bombilla que abre la característica Dígame 1.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Esquemas de cuentas** y luego elija el enlace relacionado.  
2. En la página **Esquemas de cuentas**, elija la acción **Nuevo** para crear un nuevo nombre de esquema de cuenta.
3. Alternativamente, si desea reutilizar la configuración de un programa de cuenta existente, elija la acción **Copiar programa de cuenta**.
4. Rellene los campos según sea necesario. En el campo **Plantilla columna genér.**, seleccione una disposición existente. Puede cambiarla más adelante si lo desea.

    Las disposiciones de columnas definen columnas para los parámetros mediante los cuales se muestran los datos financieros en las filas. Por ejemplo, una disposición de columnas podría contener cuatro columnas que le permitan comparar el saldo del periodo y el saldo a la fecha del mismo periodo del año actual y del año anterior. Para obtener más información, consulte [Para editar una disposición de columnas](bi-how-work-account-schedule.md#to-edit-a-column-layout).

5. Elija la acción **Editar esquema cuentas**.
6. Dependiendo de lo que desee analizar, elija las acciones **Insertar cuentas de mayor**, **Insertar cuentas CF** e **Insertar tipos de costos** para crear una fila para cada elemento financiero. Por ejemplo, podría tener una fila para activos corrientes y otra fila para activos fijos. Para obtener inspiración, consulte los esquemas de cuentas en la empresa de demostración CRONUS.

    > [!NOTE]
    > En el campo **N.º de fila**, se mostrarán los primeros 10 caracteres de un identificador, por ejemplo, un número de cuenta. Si agrega elementos con identificadores que comienzan con los mismos 10 caracteres, tendrá duplicados en **Nº de fila**. . Si es necesario, puede editar manualmente los identificadores después de insertar los elementos. Los identificadores completos se muestran en el campo **Totales**.

7. Seleccione la acción **Panorama** para ver el informe financiero resultante.
8. En la página **Panorama esq. cta.**, en el campo **Nombre plantilla columna**, seleccione otra plantilla de columnas para ver los datos de notificación por otros parámetros.
9. Elija el botón **Aceptar**.

Ha definido la base del esquema de cuentas, las filas de datos financieros que se visualizarán y una plantilla de columnas existente para mostrar los datos de las filas según diferentes parámetros. Si la plantilla de columnas predeterminada seleccionada en el paso 4 no se adapta a su finalidad, siga el procedimiento siguiente.

### <a name="to-edit-a-column-layout"></a>Para editar una plantilla de columnas

Utilice las plantillas de columnas para determinar qué columnas va a incluir en el informe resultante. Por ejemplo, puede diseñar una plantilla para comparar el saldo del periodo y el saldo a la fecha del mismo periodo del año actual y del año anterior. Puede tener hasta 15 columnas, lo cual es útil, por ejemplo, para ver presupuestos de 12 meses con una columna que muestra el total.

> [!NOTE]
> Una versión impresa, guardada o de vista preliminar de un esquema de cuentas puede mostrar como máximo cinco columnas. Si el esquema de cuentas solo está destinado al análisis en la página **Panorama esq. cta.**, puede crear tantas columnas como desee.

1. En la página **Esquemas de cuentas**, seleccione el esquema de cuentas correspondiente y después seleccione la acción **Editar configuración de disposición de columna**.
2. En la página **Plantillas de columnas**, cree una fila para cada columna por la que los datos financieros se van a mostrar en el informe financiero. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Elija el botón **Aceptar**.
4. Abra la página **Panorama esq. cta.** de vez en cuando para verificar que la nueva disposición de columnas funciona del modo previsto.

> [!NOTE]
> Las columnas definidas en cada fila representan las columnas 3 y posteriores en la página **Panorama esq. cta.**. Las dos primeras columnas, **N.º fila** y **Descripción**, son fijas.  

### <a name="to-create-a-column-that-calculates-percentages"></a>Para crear una columna que calcule porcentajes

En ocasiones, podría desear incluir una columna en un esquema de cuentas para calcular los porcentajes de un total. Por ejemplo, si tiene filas que detallan las ventas por dimensión, podría desear crear una columna para indicar el porcentaje de las ventas totales en cada fila.

1. Elija el icono ![Bombilla que abre la característica Dígame 2.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Esquemas de cuentas** y luego elija el enlace relacionado.
2. En la página **Nombres esquemas de cuentas**, seleccione un esquema de cuenta.  
3. Elija la acción **Editar esquema cuentas** para configurar una fila del esquema de cuentas para calcular el total en el que se basarán los porcentajes.  
4. Inserta una línea justo encima de la primera fila para la que desea que se muestre un porcentaje.  
5. Rellene los campos de la línea como se indica a continuación: en el campo **Tipo sumatorio**, especifique **Fijar base para porcentaje**. En el campo **Sumatorio**, introduzca una fórmula para el total en el que el porcentaje se basará. Por ejemplo, si la fila 11 contiene las ventas totales, escriba **11**.  
6. Elija la acción **Editar configuración de disposición de columna** para configurar una columna.  
7. Rellene los campos de la línea como se indica a continuación: en el campo **Tipo columna**, seleccione **Fórmula**. En el campo **Fórmula**, introduzca una fórmula para el importe para el que desea calcular un porcentaje, seguida de %. Por ejemplo, si el número de columna N contiene los saldos periodos, escriba **N%**.  
8. Repita los pasos del 4 al 7 para cada grupo de filas que desee subdividir por porcentaje.

## <a name="to-set-up-account-schedules-with-overviews"></a>Para configurar esquemas de cuentas con resúmenes

Puede usar un esquema de cuentas para crear un extracto que compare las cifras de contabilidad con las cifras presupuestadas.

1. Elija el icono ![Bombilla que abre la función Dígame 3.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Esquemas de cuentas** y luego elija el enlace relacionado.
2. En la página **Nombres esquemas de cuentas**, seleccione un esquema de cuenta.  
3. Elija la acción **Editar esquema cuentas**  
4. En la ventana **Esquema cuentas**, en el campo **Nombre**, seleccione el nombre del esquema de cuentas predeterminado.
5. Elija la acción **Insertar cuentas de contabilidad**.  
6. Seleccione la cuenta que desea incluir en la declaración y, a continuación, seleccione el botón **Aceptar**.

    Estas cuentas se insertan en el esquema de cuentas. Si lo desea, puede modificar la plantilla de columna.  
7. Seleccione la acción **Resumen**.  
8. En la página **Panorama esq. cta.**, en la ficha desplegable **Filtros dimensión** y asigne al filtro de presupuesto el nombre de filtro que desee usar.  
9. Elija el botón **Aceptar**.  

Ahora puede copiar y pegar el extracto del presupuesto en una hoja de cálculo.  

## <a name="comparing-accounting-periods-using-period-formulas"></a>Comparación de períodos contables usando fórmulas de períodos

El esquema de cuentas puede comparar los resultados de diferentes períodos contables, como este mes en comparación con el mismo mes del año anterior. Para ello, abra la página **Diseño de columna** y personalícela agregando el campo **Fórmula del período de comparación** como columna. Para obtener más información, consulte [Personalizar el área de trabajo](ui-personalization-user.md). A continuación, puede establecer ese campo en una fórmula de período.  

Un período contable no tiene que coincidir con el calendario. Sin embargo, cada año fiscal debe tener el mismo número de periodos contables, aunque cada periodo tenga una duración diferente.  

[!INCLUDE[prod_short](includes/prod_short.md)] utiliza la fórmula de periodo para calcular el importe a partir del periodo comparativo en relación con el periodo representado por el filtro de fecha del informe. El periodo de comparación se basa en el periodo de la fecha de inicio del filtro fecha. Las abreviaturas de las especificaciones del periodo son:

| Siglas | Descripción                                                                           |
| ------------ | ------------------------------------------------------------------------------------- |
| P            | Período                                                                                |
| LP           | Último periodo de un año fiscal, medio año o trimestre.                                   |
| CP           | Periodo actual de un año fiscal, medio año o trimestre. Use CP en fórmulas para establecer el período que comienza o finaliza la fórmula. Por ejemplo, FY\[1..CP\] denota el tiempo desde el comienzo del año fiscal actual hasta el período actual.|
| FY           | Año fiscal. Por ejemplo, FY\[1..3\] indica el primer trimestre del año fiscal actual. |

Ejemplos de fórmulas:

| Fórmula         | Descripción                                                                                     |
| --------------- | ----------------------------------------------------------------------------------------------- |
| \<Blank\>       | Periodo actual                                                                                  |
| \-1P            | Periodo anterior                                                                                 |
| \-1FY\[1..LP\]  | Todo el año fiscal anterior                                                                     |
| \-1FY           | Periodo actual del año fiscal anterior                                                          |
| \-1FY\[1..3\]   | Primer trimestre del año fiscal anterior                                                           |
| \-1FY\[1..CP\]  | Desde el principio del año fiscal anterior hasta el periodo actual en el año fiscal anterior, ambos periodos inclusive. |
| \-1FY\[CP..LP\] | Desde el periodo actual en el año fiscal anterior hasta el último periodo del año fiscal anterior, ambos periodos inclusive.   |

Si desea calcular el importe del periodo de comparación para periodos de tiempo regulares, deberá introducir una fórmula en el campo **Fórmula fecha comparación**. Por ejemplo, si el campo está establecido en -1Y, [!INCLUDE [prod_short](includes/prod_short.md)] compara con el mismo periodo de 1 de año antes.

> [!NOTE]
> No siempre es transparente qué períodos está comparando porque puede establecer un filtro de fecha en un informe que abarca diferentes fechas a los períodos contables que se reflejan en los datos del plan de cuentas. Por ejemplo, cree un esquema de cuentas en el que desee comparar este período con el mismo período del año anterior, por lo que debe establecer el campo **Fórmula fecha comparación** en *-1FY*. Luego, ejecute el informe el 28 de febrero y configure el filtro de fecha en enero y febrero. Como resultado, el calendario de cuentas compara enero y febrero de este año con enero del año pasado, que es el único período contable completado de los dos para el año pasado.  

Para obtener más información sobre las fórmulas de fecha, consulte [Trabajar con fechas y horas del calendario](ui-enter-date-ranges.md).  

## <a name="import-or-export-account-schedules"></a>Importación o exportación de esquemas de cuentas
Puede importar y exportar esquemas de cuentas como paquetes de configuración de RapidStart. Por ejemplo, los paquetes de configuración resultan útiles para compartirlos con otras empresas. El paquete se crea en un archivo .rapidstart, que entrega los contenidos de paquete en un formato comprimido.

### <a name="to-import-and-export-account-schedules"></a>Para importar y exportar esquemas de cuentas
1. Elija el icono ![Bombilla que abre la función Dígame 4.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Esquemas de cuentas** y luego elija el enlace relacionado.
2. Elija el esquema de cuenta y luego las acciones **Importar esquema de cuentas** o **Exportar esquema de cuentas**, dependiendo de lo que desee hacer. 

> [!NOTE]
> Cuando importe esquemas de cuentas, se eliminarán los registros existentes que tengan los mismos nombres que los que está importando.

## <a name="see-related-microsoft-training"></a>Consultar la [formación de Microsoft](/training/modules/configure-financial-reports-dynamics-365-business-central/index) relacionada

## <a name="see-also"></a>Consulte también

[Inteligencia empresarial](bi.md)  
[Finanzas](finance.md)  
[Configurar las finanzas](finance-setup-finance.md)  
[Libro mayor y plan de cuentas](finance-general-ledger.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
