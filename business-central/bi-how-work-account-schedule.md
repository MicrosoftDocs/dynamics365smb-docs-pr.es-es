---
title: Crear informes financieros con categorías de cuentas y datos financieros
description: Describe cómo utilizar informes financieros para crear varias vistas e informes para analizar los datos de rendimiento financiero.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bnielse
ms.topic: how-to
ms.date: 02/27/2023
ms.custom: bap-template
ms.search.keywords: 'bi, power BI, analysis, KPI, account schedule, financial report'
ms.search.form: '103, 104, 108, 195, 196, 197, 198, 489, 490, 764, 765, 766'
---
# <a name="prepare-financial-reporting-with-financial-data-and-account-categories"></a>Preparar Financial Reporting con categorías de cuentas y datos financieros

Los informes financieros permiten obtener información sobre los datos financieros almacenados en su plan de cuentas (COA). Los informes financieros analizan cifras en cuentas de contabilidad (G/L) y comparan los movimientos de contabilidad con los presupuestados. Los resultados se muestran en gráficos e informes en su área de trabajo, como el gráfico de flujo de efectivo y los informes Balance de ingresos y Balance.

Se obtiene acceso a estos dos informes, por ejemplo, con la acción **Estados financieros** en las áreas de trabajo de Administrador de negocio y Contable.  

[!INCLUDE[prod_short](includes/prod_short.md)] proporciona informes financieros de muestra que puede usar de inmediato. También puede configurar sus propias filas y columnas para especificar las cifras que desea comparar. Por ejemplo, puede crear informes financieros para calcular márgenes de beneficios usando dimensiones, como departamentos o grupos de clientes. El número de resultados financieros personalizados que puede crear es iilmitado.  

Configurar informes financieros requiere obtener una comprensión de los datos financieros del plan de cuentas. Por ejemplo, puede ver los movimientos de contabilidad como porcentajes de los movimientos de presupuesto, pero eso requiere tener presupuestos creados. Obtenga más información en [Crear presupuestos de G/L](finance-how-create-budgets.md).

## <a name="financial-reports"></a>Informes financieros

Los informes financieros organizan las cuentas de su catálogo de cuentas de manera que facilitan más la presentación de los datos. Puede configurar diversas plantillas para definir la información que desea extraer del plan de cuentas. Los informes financieros proporcionan un lugar para cálculos que no se puedan realizar directamente en el plan de cuentas. Por ejemplo, puede crear subtotales para grupos de cuentas y luego incluir ese total en otros totales. Otro ejemplo es para calcular márgenes de beneficios en dimensiones, como departamentos o grupos de clientes. Además, puede filtrar los movimientos y los movimientos presupuestarios, por ejemplo, por saldo periodo o importe debe.

También puede comparar dos o más informes financieros y definiciones de columnas mediante el uso de fórmulas, lo que le permite realizar esto:

* Crear informes financieros personalizados.
* Crear tantos informes financieros como necesite, cada uno de ellos con un nombre diferente.
* Configurar diversas plantillas de informes e imprimir estos con las cifras actuales.

## <a name="gl-account-categories"></a>Categorías de cuenta de G/L

Puede usar categorías de cuentas para cambiar el diseño de sus balances financieros. Por ejemplo, una vez configuradas las categorías de cuentas en la página **Categorías de cuenta**, puede elegir la acción **Generar informes financieros** y actualizar los informes financieros subyacentes para los informes financieros principales. Luego, la próxima vez que ejecute uno de estos informes, como el informe **Extracto del saldo**, se agregan los nuevos totales y subtotales.

> [!NOTE]
> Las categorías de cuentas de nivel superior, como el nodo **Pasivo**, son fijas y no puede agregar las suyas. Sin embargo, puede eliminar y agregar categorías de cuenta en niveles inferiores y definir cómo aparece el informe financiero relacionado en los informes.
>
> Debería crear y estructurar sus propias categorías de cuentas de mayor de nivel inferior desde cero, en una jerarquía si es necesario, en lugar de tratar de reorganizar las existentes. Por ejemplo, puede reestructurar el nodo **Pasivo** para contener un nuevo nodo **Capital** seguido por los nodos **Pasivo circulante** y **Pasivos a largo plazo**.

## <a name="create-a-new-financial-report"></a>Crear un nuevo informe financiero

Usa informes financieros para analizar cuentas de contabilidad (G/L) o comparar los movimientos de contabilidad con los presupuestados. Por ejemplo, puede ver los movimientos de contabilidad como porcentajes de los movimientos de presupuesto.

Los informes financieros en la versión estándar de [!INCLUDE[prod_short](includes/prod_short.md)] podría no adaptarse a las necesidades de su negocio. Para crear rápidamente sus propios informes financieros, puede empezar por copiar uno existente, como se describe en el paso siguiente.

> [!TIP]
> Después de crear un informe financiero, puede utilizar la página **Informe financiero** para obtener una vista previa y validar su informe financiero recién definido. Elija la acción **Editar informe financiero** para abrir la página.  

> [!NOTE]
> Cuando abre un informe financiero en el modo Ver o Editar, el panel Filtro está disponible. Sin embargo, no utilice el panel para establecer filtros para los datos de su informe. Los filtros pueden causar errores o no filtrar los datos. En su lugar, utilice los campos de filtro en las fichas desplegables **Opciones** y **Dimensiones**.

1. Elija el icono ![Bombilla que abre la característica Dígame 1.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Informes financieros** y luego elija el vínculo relacionado.  
2. En la página **Informes financieros**, elija la acción **Nuevo** para crear un nuevo nombre de informe financiero.
3. Alternativamente, si desea reutilizar la configuración de un informe financiero existente, elija la acción **Copiar informe financiero**.
4. Rellene los campos según sea necesario. En el campo **Definición de columna**, seleccione una definición existente, que luego puede editar si lo desea.

    Las definiciones de columna espedifican los parámetros mediante los cuales se muestran los datos financieros en las filas. Por ejemplo, una definición de columna podría contener cuatro columnas que puede usar para comparar el saldo del periodo y el saldo a la fecha del mismo periodo del año actual y del año anterior. Obtenga más información en la sección [Editar una definición de columna](bi-how-work-account-schedule.md#edit-a-column-definition).

5. Elija la acción **Editar definición de fila**.
6. Elija las acciones **Insertar cuentas de mayor**, **Insertar cuentas CF** e **Insertar tipos de costos** para crear una fila para cada elemento financiero que desee analizar. Por ejemplo, podría tener una fila para activos corrientes y otra fila para activos fijos. Para obtener inspiración, consulte los informes financieros en la empresa de demostración CRONUS.

    > [!NOTE]
    > En el campo **N.º de fila**, se muestran los primeros 10 caracteres de un identificador, como un número de cuenta. Si agrega elementos con identificadores que comienzan con los mismos 10 caracteres, tendrá duplicados en **Nº de fila**. . Si es necesario, puede editar manualmente los identificadores después de insertar los elementos. Los identificadores completos se muestran en el campo **Totales**.

7. En la página **Informes financieros**, seleccione la acción **Editar informe financiero** para acceder al informe financiero resultante.
8. En la página **Informe financiero**, en el campo **Definición de columna**, seleccione otra definición de columna para explorar los datos financieros por otros parámetros.
9. Elija **Aceptar**.

Ha definido la base del informe financiero siguiente, las filas de datos financieros que se visualizarán y una plantilla de columnas existente para mostrar los datos de las filas usando parámetros personalizados. Si la definición de columnas predeterminada seleccionada en el paso 4 no se adapta a su finalidad, siga los pasos de [Editar una definición de columna](#edit-a-column-definition).

### <a name="edit-a-column-definition"></a>Editar una definición de columna

Utilice las definiciones de columnas para especificar las columnas para incluir en el informe resultante. Por ejemplo, puede diseñar una plantilla para comparar el saldo del periodo y el saldo a la fecha del mismo periodo del año actual y del año anterior. Puede tener hasta 15 columnas, lo cual es útil, por ejemplo, para ver presupuestos de 12 meses con una columna que muestra el total.

> [!NOTE]
> Una versión impresa, guardada o de vista preliminar de un informe financiero puede mostrar como máximo cinco columnas. En cambio, si un informe financiero solo está destinado al análisis en la página **Informe financiero**, puede crear tantas columnas como desee.

1. En la página **Informes financieros**, seleccione el informe financiero pertinente y, a continuación, elija la acción **Editar definición de columna**.
2. En la página **Definición de columna**, cree una fila para cada columna de datos financieros mostrada en el informe financiero. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Elija **Aceptar**.
4. Abra la página **Informe financiero** de vez en cuando para verificar que la nueva definición de columna funciona del modo previsto.

> [!NOTE]
> Las columnas definidas en cada fila representan las columnas tres y posteriores en la página **Informe financiero**. Las dos primeras columnas, **N.º fila** y **Descripción**, son fijas.  

### <a name="create-a-column-that-calculates-percentages"></a>Crear una columna que calcule porcentajes

En ocasiones, podría desear incluir una columna en un informe financiero para calcular los porcentajes de un total. Por ejemplo, si tiene filas que detallan las ventas por dimensión, podría desear crear una columna para indicar el porcentaje de las ventas totales en cada fila.

1. Elija el icono ![Bombilla que abre la característica Dígame 2.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Informes financieros** y luego elija el vínculo relacionado.
2. En la página **Informes financieros**, seleccione un informe financiero.  
3. Elija la acción **Editar informe financiero** para configurar un informe financiero para calcular el total en el que se basarán los porcentajes.  
4. Inserta una línea justo encima de la primera fila para la que desea que se muestre un porcentaje.  
5. Rellene los campos de la línea como se indica a continuación: en el campo **Tipo sumatorio**, especifique **Fijar base para porcentaje**. En el campo **Sumatorio**, introduzca una fórmula para el total en el que el porcentaje se basará. Por ejemplo, si la fila 11 contiene las ventas totales, escriba **11**.  
6. Elija la acción **Editar definición de columna** para configurar una columna.  
7. Rellene los campos de la línea como se indica a continuación: en el campo **Tipo columna**, seleccione **Fórmula**. En el campo **Fórmula**, introduzca una fórmula para el importe para el que desea calcular un porcentaje, seguida del signo de porcentaje (%). Por tanto, si el número de columna N contiene los saldos periodos, escriba **N%**.  
8. Repita los pasos del 4 al 7 para cada grupo de filas que desee subdividir por porcentaje.

## <a name="set-up-financial-reports-with-overviews"></a>Configurar informes financieros con resúmenes

Puede usar un informe financiero para crear un extracto que compare las cifras de contabilidad con las cifras presupuestadas.

1. Elija el icono ![Bombilla que abre la función Dígame 3.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Informes financieros** y luego elija el vínculo relacionado.
2. En la página **Informes financieros**, seleccione un informe financiero.  
3. Elija la acción **Editar definición de fila**.  
4. En la página **Definición de fila**, en el campo **Nombre**, seleccione el nombre del informe financiero predeterminado.
5. Elija la acción **Insertar cuentas de contabilidad**.  
6. Seleccione las cuentas que desea incluir en el extracto y, a continuación, elija **Aceptar**.

    Estas cuentas se insertan en el informe financiero. Si lo desea, puede modificar la definición de columna.  
7. Elija la acción **Editar informe financiero**.  
8. En la página **Informe financiero**, en la ficha desplegable **Dimensiones**, asigne al filtro de presupuesto el nombre de filtro que desee usar.  
9. Elija **Aceptar**.  

Ahora puede copiar y pegar el extracto del presupuesto en una hoja de cálculo.  

## <a name="comparing-accounting-periods-using-period-formulas"></a>Comparación de períodos contables usando fórmulas de períodos

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

## <a name="print-and-save-financial-reports"></a>Imprimir y guardar informes financieros

Puede imprimir informes financieros utilizando los servicios de impresión de su dispositivo. [!INCLUDE[prod_short](includes/prod_short.md)] también ofrece la opción de guardar informes como libros de trabajo de Microsoft Excel, documentos de Microsoft Word, archivos PDF y XML.

1. Elija el icono ![Bombilla que abre la función Dígame 4.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Informes financieros** y luego elija el vínculo relacionado.
2. En la página **Informes financieros**, seleccione el informe financiero que desea imprimir y, a continuación, elija la acción **Imprimir**.
3. Rellene los campos según sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. En el campo **Impresora**, seleccione el dispositivo al que se enviará el informe.
    1. La opción **(Manejado por el navegador)** indica que no hay una impresora designada para el informe. En este caso, el navegador manejará la impresión y mostrará unos pasos de impresión estándar, donde puede elegir una impresora local conectada a su dispositivo. **(Manejado por el navegador)** no está disponible en la aplicación móvil de [!INCLUDE[prod_short](includes/prod_short.md)] o la aplicación para Microsoft Teams.
5. Seleccione la acción **Imprimir**.

### <a name="schedule-a-financial-report-or-save-as-a-pdf-word-or-excel-document"></a>Programe un informe financiero o guárdelo como un documento PDF, Word o Excel

Un informe financiero se puede guardar como un archivo en diferentes formatos, como PDF, XML, Word o Excel. Alternativamente, [!INCLUDE[prod_short](includes/prod_short.md)] se puede configurar para generar informes financieros recurrentes:

1. Elija el icono ![Bombilla que abre la función Dígame 4](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Informes financieros** y luego elija el vínculo relacionado.
2. En la página **Informes financieros**, seleccione la acción **Imprimir**.
3. Configure el informe en consecuencia, luego elija la acción **Enviar a**.
4. Seleccione el formato de archivo o la acción **Calendario** y elija **Aceptar**.
5. Para generar un informe financiero programado o recurrente, complete los campos. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)].
   * Para informes financieros recurrentes, configure los campos **Fecha/hora de inicio más temprana** y **Fecha/hora de caducidad** con la primera y última fecha, respectivamente, para generar el informe financiero. Además, seleccione en qué días se genera el informe configurando el campo **Fórmula de fecha de próxima ejecución** siguiendo el formato explicado en la sección [Usar fórmulas de fecha](ui-enter-date-ranges.md#use-date-formulas).

## <a name="importing-or-exporting-financial-reports"></a>Importación o exportación de informes financieros

Puede importar y exportar informes financieros como paquetes de configuración RapidStart, que son útiles para compartir la información con otras empresas, por ejemplo. El paquete se crea en un archivo .rapidstart, que comprime los contenidos.

### <a name="import-and-export-financial-reports"></a>Importar y exportar informes financieros

1. Elija el icono ![Bombilla que abre la función Dígame 4.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Informes financieros** y luego elija el vínculo relacionado.
2. Elija el informe financiero, luego elija la acción **Importar informe financiero** o **Exportar informe financiero**, dependiendo de lo que quiera hacer.

> [!NOTE]
> Cuando importe informes financieros, se eliminarán los registros existentes con los mismos nombres que los que está importando.

## <a name="see-related-microsoft-training"></a>Consulte la [formación de Microsoft](/training/modules/configure-financial-reports-dynamics-365-business-central/index) relacionada.

## <a name="see-also"></a>Consulte también .

[Ejecutar e imprimir informes](ui-work-report.md)  
[Inteligencia empresarial financiera](bi.md)  
[Finanzas](finance.md)  
[Configurar las finanzas](finance-setup-finance.md)  
[Libro mayor y plan de cuentas](finance-general-ledger.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
