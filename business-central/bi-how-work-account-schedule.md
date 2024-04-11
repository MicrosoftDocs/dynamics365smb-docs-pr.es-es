---
title: Crear informes financieros con categorías de cuentas y datos financieros
description: Describe cómo utilizar informes financieros para crear varias vistas e informes para analizar los datos de rendimiento financiero.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bnielse
ms.topic: how-to
ms.date: 03/27/2024
ms.custom: bap-template
ms.search.keywords: 'bi, power BI, analysis, KPI, account schedule, financial report'
ms.search.form: '103, 104, 108, 195, 196, 197, 198, 489, 490, 764, 765, 766'
ms.service: dynamics-365-business-central
---
# Preparar informes financieros con datos financieros y categorías de cuentas

La característica **Informes financieros** le permite obtener información sobre los datos financieros que se muestran en su plan de cuentas (COA). Puede configurar informes financieros para analizar cifras en cuentas de contabilidad (G/L) y comparan los movimientos de contabilidad con los presupuestados. Los resultados se muestran en gráficos e informes en su área de trabajo, como el gráfico de flujo de efectivo y los informes Balance de ingresos y Balance. Se obtiene acceso a estos dos informes, por ejemplo, con la acción **Estados financieros** en las páginas de inicio Administrador de negocio y Contable.  

[!INCLUDE[prod_short](includes/prod_short.md)] proporciona informes financieros de muestra que puede usar de inmediato como plantillas. También puede configurar sus propios informes para especificar las cifras que desea comparar. Por ejemplo, puede crear informes financieros para calcular márgenes de beneficios usando dimensiones, como departamentos o grupos de clientes. La cantidad de informes financieros que puede crear es ilimitada y no requiere la participación de un desarrollador.  

## Requisitos previos para informes financieros

Configurar informes financieros requiere obtener una comprensión de los estructura de su plan de cuentas. Hay tres conceptos clave a los que probablemente deba prestar atención antes de diseñar sus informes financieros:

- Asigne cuentas de contabilización del L/M a categorías de cuentas del L/M.
- Diseñe cómo utiliza las dimensiones.
- Configurar presupuestos contables.

Las categorías de cuentas del L/M simplifican las definiciones de sus informes financieros y los hacen más resistentes a los cambios en la estructura del plan de cuentas. Más información en [Usar categorías de cuentas para cambiar el diseño de sus balances financieros](#use-gl-account-categories-to-change-the-layout-of-your-financial-statements).

La configuración de dimensiones le permite dividir sus datos financieros de manera que tengan sentido para su organización. Obtenga más información en [Trabajar con dimensiones](finance-dimensions.md). 

Si desea ver las entradas de contabilidad general como porcentajes de las entradas del presupuesto, debe crear presupuestos de G/L. Obtenga más información en [Crear presupuestos de G/L](finance-how-create-budgets.md).

## Informes financieros

Los informes financieros organizan las cuentas de su catálogo de cuentas de manera que facilitan más la presentación de los datos. Puede configurar diversas plantillas para definir la información que desea extraer del plan de cuentas. Los informes financieros también proporcionan un lugar para cálculos que no se puedan realizar directamente en el plan de cuentas. Por ejemplo, puede crear subtotales para grupos de cuentas y luego incluir ese total en otros totales. Otro ejemplo es para calcular márgenes de beneficios en dimensiones, como departamentos o grupos de clientes. Además, puede filtrar los movimientos y los movimientos presupuestarios, por ejemplo, por saldo periodo o importe debe.

> [!NOTE] 
> Matemáticamente, piense que un informe financiero se define por dos cosas:
>
> - Un vector de definiciones de filas que definen lo que se debe calcular.
> - Un vector de definiciones de columnas que define los datos para el cálculo.
>
> El informe financiero es entonces el producto externo de estos dos vectores, donde el valor de cada celda se calcula según la fórmula de la fila aplicada a la definición de datos de la columna.

:::image type="content" source="media/financial-report-definition.svg" alt-text="Muestra cómo se construye un informe financiero a partir de una definición de fila y una definición de columna." lightbox="media/financial-report-definition.svg":::

La página **Informes financieros** muestra cómo todos los informes financieros siguen un patrón que consta de los siguientes atributos:

* Nombre (código)
* Descripción
* Definición de fila
* Definición de columna

:::image type="content" source="media/financial-reports.png" alt-text="Muestra cómo se construyen todos los informes financieros a partir de una definición de fila y una definición de columna." lightbox="media/financial-reports.png":::

> [!NOTE]
> Los informes financieros de muestra en [!INCLUDE[prod_short](includes/prod_short.md)] no están listos para usarse de inmediato. Dependiendo de la forma en que configure sus cuentas de contabilidad, dimensiones, categorías de cuentas del contabilidad y presupuestos, deberá ajustar las definiciones de filas y columnas de muestra y los informes financieros en los que se utilizan para que coincidan con su configuración.

También puede utilizar fórmulas para comparar dos o más informes financieros y definiciones de columnas. Las comparaciones permiten hacer lo siguiente:

* Crear informes financieros personalizados.
* Crear tantos informes financieros como necesite, cada uno de ellos con un nombre diferente.
* Configurar diversas plantillas de informes e imprimir estos con las cifras actuales.

## Ruta de aprendizaje: Crear informes financieros en Microsoft Dynamics 365 Business Central

¿Quiere aprender a crear presupuestos y luego utilizar informes financieros, dimensiones y definiciones de filas y columnas para generar los informes financieros que normalmente necesitan la mayoría de las empresas?

Comience a aprender en la ruta de aprendizaje [Crear informes financieros en Microsoft Dynamics 365 Business Central](/training/paths/create-financial-reports-dynamics-365-business-central)

## Crear un nuevo informe financiero

Usa informes financieros para analizar cuentas de contabilidad (G/L) o comparar los movimientos de contabilidad con los presupuestados. Por ejemplo, puede ver los movimientos de contabilidad como porcentajes de los movimientos de presupuesto.

Los informes financieros en la versión estándar de [!INCLUDE[prod_short](includes/prod_short.md)] podría no adaptarse a las necesidades de su negocio. Para crear rápidamente sus propios informes financieros, puede empezar por copiar uno existente, como se describe en el paso siguiente.

1. Elija el icono ![Bombilla que abre la característica Dígame 1.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Informes financieros** y luego elija el vínculo relacionado.  
1. En la página **Informes financieros**, elija la acción **Nuevo** para crear un nuevo nombre de informe financiero. Alternativamente, para reutilizar la configuración de un informe financiero existente, elija la acción **Copiar informe financiero**.
1. Rellene el nombre corto del informe (no se puede cambiar) y la descripción.
1. Elija una definición de fila y una definición de columna.
1. Opcionalmente, elija vistas de análisis para las definiciones de filas y columnas.
1. Elija la acción **Editar informe financiero** para tener acceso a más propiedades del informe financiero.
1. En la ficha desplegable **Opciones**, puede editar la descripción del informe, cambiar las definiciones de filas y columnas y definir cómo mostrar las fechas. Las fechas pueden ser una jerarquía Día/Semana/Mes/Trimestre/Año, o utilizar periodos contables. Para obtener más información, vaya a [Comparación de períodos contables usando fórmulas de períodos](#comparing-accounting-periods-using-period-formulas).
1. En la ficha desplegable **Dimensiones**, puede definir filtros de dimensiones para el informe.
1. Puede obtener una vista previa del informe en el área debajo de la pestaña desplegable **Dimensiones**.

> [!TIP]
> Después de crear un informe financiero, puede utilizar la página **Informe financiero** para obtener una vista previa y validarlo. Elija la acción **Ver informe financiero** para abrir la página.  

> [!NOTE]
> Cuando abre un informe financiero en el modo Ver o Editar, el panel Filtro está disponible. No utilice el panel Filtro para establecer filtros para los datos de su informe. Tales filtros pueden causar errores o no filtrar los datos. En su lugar, utilice los campos de las pestañas desplegables **Opciones** y **Dimensiones** para configurar filtros para el informe.

### Crear o editar una definición de fila

Las definiciones de fila en informes financieros proporcionan un lugar para cálculos que no se puedan realizar directamente en el plan de cuentas. Por ejemplo, puede crear subtotales para grupos de cuentas y luego incluir ese total en otros totales. También puede calcular pasos intermedios que no se muestran en el informe final.

1. En la página **Informes financieros**, seleccione el informe financiero pertinente y, a continuación, elija la acción **Editar definición de fila**.
1. Elija las acciones **Insertar cuentas de mayor**, **Insertar cuentas CF** e **Insertar tipos de costos** para crear una fila para cada elemento financiero que desee analizar. Por ejemplo, podría tener una fila para activos corrientes y otra fila para activos fijos. Para obtener inspiración, explore los informes financieros en la empresa de demostración CRONUS.

    > [!NOTE]
    > En el campo **N.º de fila**, se muestran los primeros 10 caracteres de un identificador, como un número de cuenta. Si agrega elementos con identificadores que comienzan con los mismos 10 caracteres, tendrá duplicados en **Nº de fila** . Si es necesario, puede editar manualmente los identificadores después de insertar los elementos. Los identificadores completos se muestran en el campo **Totales**.

> [!NOTE]
> Las columnas que defina en cada línea de la definición de filas representan las columnas tres y superiores de la página **Informe financiero**. Las dos primeras columnas, **N.º fila** y **Descripción**, son fijas.  

### Crear o editar una definición de columna

Utilice las definiciones de columnas para especificar las columnas para incluir en el informe resultante. Por ejemplo, puede diseñar una plantilla de informe para comparar el saldo del periodo y el saldo a la fecha del mismo periodo del año actual y del año anterior. Puede tener hasta 15 columnas en una definición de columna. Por ejemplo, las columnas múltiples son útiles para mostrar los presupuestos de 12 meses con una columna que muestre el total.

> [!NOTE]
> Una versión impresa, guardada o de vista preliminar de un informe financiero puede mostrar como máximo cinco columnas. En cambio, si un informe financiero solo está destinado al análisis en la página **Informe financiero**, puede crear tantas columnas como desee.

1. En la página **Informes financieros**, seleccione el informe financiero pertinente y, a continuación, elija la acción **Editar definición de columna**.
1. En la página **Definición de columna**, cree una fila para cada columna de datos financieros mostrada en el informe financiero. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
1. Elija **Aceptar**.
1. Abra la página **Informe financiero** de vez en cuando para verificar que la nueva definición de columna funciona del modo previsto.

### Crear una definición de columna para calcular porcentajes

Podría desear incluir una columna en un informe financiero para calcular los porcentajes de un total. Por ejemplo, si tiene filas que detallan las ventas por dimensión, podría desear crear una columna para indicar el porcentaje de las ventas totales en cada fila.

1. Elija el icono ![Bombilla que abre la característica Dígame 2.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Informes financieros** y luego elija el vínculo relacionado.
1. En la página **Informes financieros**, seleccione un informe financiero.  
1. Elija la acción **Editar informe financiero** para configurar un informe financiero para calcular el total en el que se basarán los porcentajes.  
1. agregue una línea justo encima de la primera fila para la que desea que se muestre un porcentaje.  
1. Rellene los campos de la línea como se indica a continuación: en el campo **Tipo sumatorio**, especifique **Fijar base para porcentaje**. En el campo **Sumatorio**, introduzca una fórmula para el total en el que el porcentaje se basará. Por ejemplo, si la fila 11 contiene las ventas totales, escriba **11**.  
1. Elija la acción **Editar definición de columna** para configurar una columna.  
1. Rellene los campos de la línea como se indica a continuación. En el campo **Tipo columna**, seleccione **Fórmula**. En el campo **Fórmula**, introduzca una fórmula para el importe para el que desea calcular un porcentaje, seguida del signo de porcentaje (%). Por tanto, si el número de columna N contiene los saldos periodos, escriba **N%**.  
1. Repita los pasos del 4 al 7 para cada grupo de filas que desee subdividir por porcentaje.

## Usar categorías de cuentas para cambiar el diseño de sus balances financieros

Puede usar categorías de cuentas para cambiar el diseño de sus balances financieros. Por ejemplo, una vez configuradas las categorías de cuentas en la página **Categorías de cuenta**, puede elegir la acción **Generar informes financieros** y actualizar los informes financieros subyacentes para los informes financieros principales. La próxima vez que ejecute uno de estos informes, como el informe **Extracto del saldo**, se agregan los nuevos totales y subtotales.

Otro beneficio de utilizar categorías de cuentas del L/M en lugar de las cuentas del L/M sin procesar en las definiciones de filas es que un cambio en la estructura de su plan de cuentas no afecta sus informes financieros.

> [!NOTE]
> Las categorías de cuentas de nivel superior, como el nodo **Pasivo**, son fijas y no puede agregar las suyas. Sin embargo, puede eliminar y agregar categorías de cuenta en niveles inferiores y definir cómo aparece el informe financiero relacionado en los informes.
>
> Debería crear y estructurar sus propias categorías de cuentas de mayor de nivel inferior desde cero, en una jerarquía si es necesario, en lugar de tratar de reorganizar las existentes. Por ejemplo, puede reestructurar el nodo **Pasivo** para contener un nuevo nodo **Capital** seguido por los nodos **Pasivo circulante** y **Pasivos a largo plazo**. Obtenga más información en [Asignación de cuentas del libro mayor a categorías de cuentas](finance-general-ledger.md#account-categories).

## Usar dimensiones en informes financieros

En análisis financiero, una dimensión son datos que agrega a un movimiento como una especie de marcador. Estos datos se utilizan para agrupar movimientos de características similares, como clientes, regiones, productos y vendedor, y así poder recuperar con facilidad estos grupos para su análisis. Puede usar dimensiones en movimientos de diarios, documentos y presupuestos.

Cada dimensión describe el foco del análisis. Así, un análisis de dos dimensiones, por ejemplo, sería ventas por área. Al utilizar más de dos dimensiones cuando se crea una entrada, puede realizar un análisis más complejo. Un ejemplo de análisis complejo es explorar las ventas por campaña de ventas por grupo de clientes por área. Eso le proporciona una mayor visión de su negocio, como por ejemplo, lo bien que está funcionando, dónde está prosperando o no y dónde debería asignar más recursos. Esa información le ayuda a tomar decisiones comerciales más informadas. Obtenga más información en [Trabajar con dimensiones](finance-dimensions.md).

## Configurar informes financieros con resúmenes

Puede usar un informe financiero para crear un extracto que compare las cifras de contabilidad con las cifras presupuestadas.

1. Elija el icono ![Bombilla que abre la función Dígame 3.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Informes financieros** y luego elija el vínculo relacionado.
1. En la página **Informes financieros**, seleccione un informe financiero.  
1. Elija la acción **Editar definición de fila**.  
1. En la página **Definición de fila**, en el campo **Nombre**, seleccione el nombre del informe financiero predeterminado.
1. Elija la acción **Insertar cuentas de contabilidad**.  
1. Seleccione las cuentas que desea incluir en el extracto y, a continuación, elija **Aceptar**.

    Estas cuentas se insertan en el informe financiero. Si lo desea, puede modificar la definición de columna.  
1. Elija la acción **Editar informe financiero**.  
1. En la página **Informe financiero**, en la ficha desplegable **Dimensiones**, asigne al filtro de presupuesto el nombre de filtro que desee usar.  
1. Elija **Aceptar**.  

Ahora puede copiar y pegar el extracto del presupuesto en una hoja de cálculo.  

## Comparación de períodos contables usando fórmulas de períodos

El informe financiero puede comparar los resultados de diferentes períodos contables, como el mes pasado en comparación con el mismo mes del año anterior. Para ello, abra la página **Definición de columna** y personalícela agregando el campo **Fórmula del período de comparación** como columna. Obtenga más información en [Personalizar el área de trabajo](ui-personalization-user.md). A continuación, puede establecer ese campo en una fórmula de período.  

Un período contable no necesita coincidir con el calendario. Sin embargo, cada año fiscal debe tener el mismo número de periodos contables, aunque cada periodo tenga una duración diferente.  

[!INCLUDE[prod_short](includes/prod_short.md)] utiliza la fórmula de periodo para calcular la duración del periodo comparativo en relación con el periodo representado por el filtro de fecha del informe. El periodo de comparación se basa en el periodo de la fecha de inicio del filtro fecha. Las abreviaturas de las especificaciones del periodo son:

| Siglas | Descripción                                                                           |
| ------------ | ------------------------------------------------------------------------------------- |
| P            | Período.                                                                                |
| LP           | Último periodo de un año fiscal, medio año o trimestre.                                   |
| CP           | Periodo actual de un año fiscal, medio año o trimestre. Use CP en fórmulas para establecer el período que comienza o finaliza la fórmula. Por ejemplo, FY\[1..CP\] denota el tiempo desde el comienzo del año fiscal actual hasta el período actual.|
| FY           | Año fiscal. Por ejemplo, FY\[1..3\] indica el primer trimestre del año fiscal actual. |

Ejemplos de fórmulas:

| Fórmula         | Descripción                                                                                     |
| --------------- | ----------------------------------------------------------------------------------------------- |
| \<Blank\>       | Periodo actual.                                                                                  |
| \-1P            | Período anterior.                                                                                 |
| \-1FY\[1..LP\]  | Todo el año fiscal anterior.                                                                     |
| \-1FY           | Periodo actual del año fiscal anterior.                                                          |
| \-1FY\[1..3\]   | Primer trimestre del año fiscal anterior.                                                           |
| \-1FY\[1..CP\]  | Desde el principio del año fiscal anterior hasta el periodo actual en el año fiscal anterior, ambos periodos inclusive. |
| \-1FY\[CP..LP\] | Desde el periodo actual en el año fiscal anterior hasta el último periodo del año fiscal anterior, ambos periodos inclusive.   |

Si desea calcular el importe del periodo de comparación para periodos de tiempo regulares, deberá introducir una fórmula en el campo **Fórmula fecha comparación**. Por ejemplo, si el campo está establecido en -1Y, [!INCLUDE [prod_short](includes/prod_short.md)] compara con el mismo periodo de un de año antes.

> [!NOTE]
> No siempre es transparente qué períodos está comparando porque puede establecer un filtro de fecha en un informe que abarca diferentes fechas a los períodos contables que se reflejan en el plan de cuentas. Por tanto, si crea un informe financiero en el que desee comparar este período con el mismo período del año anterior, por lo que debe establecer el campo **Fórmula fecha comparación** en *-1FY*. Luego, ejecute el informe el 28 de febrero y configure el filtro de fecha en enero y febrero. Como resultado, el informe financiero compara enero y febrero de este año con enero del año pasado, que es el único período contable completado de los dos para el año pasado.  

Obtenga más información en [Trabajar con fechas y horas del calendario](ui-enter-date-ranges.md).

## Imprimir y guardar informes financieros

Puede imprimir informes financieros utilizando los servicios de impresión de su dispositivo. [!INCLUDE[prod_short](includes/prod_short.md)] también ofrece la opción de guardar informes como libros de trabajo de Excel, documentos de Word, archivos PDF y XML.

1. Elija el icono ![Bombilla que abre la función Dígame 4.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Informes financieros** y luego elija el vínculo relacionado.
1. En la página **Informes financieros**, seleccione el informe financiero que desea imprimir y, a continuación, elija la acción **Imprimir**.
1. Rellene los campos según sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
1. En el campo **Impresora**, seleccione el dispositivo al que se enviará el informe.
    1. La opción **(Manejado por el navegador)** indica que no hay una impresora designada para el informe. En este caso, el navegador manejará la impresión y mostrará unos pasos de impresión estándar, donde puede elegir una impresora local conectada a su dispositivo. **(Manejado por el navegador)** no está disponible en la aplicación móvil de [!INCLUDE[prod_short](includes/prod_short.md)] o la aplicación para Teams.
1. Seleccione la acción **Imprimir**.

### Programe un informe financiero o guárdelo como un documento PDF, Word o Excel

Un informe financiero se puede guardar como un archivo en diferentes formatos, como PDF, XML, Word o Excel. Alternativamente, [!INCLUDE[prod_short](includes/prod_short.md)] puede generar informes financieros recurrentes:

1. Elija el icono ![Bombilla que abre la función Dígame 4](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Informes financieros** y luego elija el vínculo relacionado.
1. En la página **Informes financieros**, seleccione la acción **Imprimir**.
1. Configure el informe en consecuencia, luego elija la acción **Enviar a**.
1. Seleccione el formato de archivo o la acción **Calendario** y elija **Aceptar**.
1. Para generar un informe financiero programado o recurrente, complete los campos. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)].<br><br>Para informes financieros recurrentes, configure los campos **Fecha/hora de inicio más temprana** y **Fecha/hora de caducidad** con la primera y última fecha, respectivamente, para generar el informe financiero. Además, seleccione en qué días se genera el informe configurando el campo **Fórmula de fecha de próxima ejecución** siguiendo el formato explicado en la sección [Usar fórmulas de fecha](ui-enter-date-ranges.md#use-date-formulas).

## Importación o exportación de definiciones de informes financieros

Puede importar y exportar definiciones de filas/informes financieros como paquetes de configuración RapidStart, que son útiles para compartir la información con otras empresas, por ejemplo. El paquete se crea en un archivo .rapidstart, que comprime los contenidos.

> [!NOTE]
> Cuando importe definiciones de informes financieros/filas, los registros existentes con los mismos nombres que los que está importando se sustituirán por las nuevas definiciones. Tenga en cuenta que el paquete de configuración para una definición de informe no sobrescribirá ninguna definición de fila o columna existente que se utilice en la definición de informe.

Para importar o exportar definiciones de informes financieros, siga estos pasos:

1. Elija el icono ![Bombilla que abre la función Dígame 4.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Informes financieros** y luego elija el vínculo relacionado.
1. Elija el informe financiero, luego elija la acción **Importar informe financiero** o **Exportar informe financiero**, dependiendo de lo que quiera hacer.

Para importar o exportar definiciones de filas de informes financieros, siga estos pasos:

1. Elija el icono ![Bombilla que abre la característica Dígame 4.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Definiciones de filas** y, a continuación, elija el vínculo relacionado.
1. Seleccione la definición de línea y, a continuación, elija la acción **Importar definición de fila** o **Exportar definición de fila** en función de lo que desee hacer.

## Consulte también

[Ejecutar e imprimir informes](ui-work-report.md)  
[Inteligencia empresarial financiera](bi.md)  
[Finanzas](finance.md)  
[Configurar las finanzas](finance-setup-finance.md)  
[Libro mayor y plan de cuentas](finance-general-ledger.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
