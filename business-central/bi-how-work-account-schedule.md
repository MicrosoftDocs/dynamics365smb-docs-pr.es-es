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

Las categorías de cuentas del L/M simplifican las definiciones de sus informes financieros y los hacen más resistentes a los cambios en la estructura del plan de cuentas. Más información en [Usar categorías de cuentas para cambiar el diseño de sus balances financieros](bi-row-definitions.md#use-gl-account-categories-to-change-the-layout-of-your-financial-statements).

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

- Nombre (código)
- Descripción
- Definición de fila
- Definición de columna

:::image type="content" source="media/financial-reports.png" alt-text="Muestra cómo se construyen todos los informes financieros a partir de una definición de fila y una definición de columna." lightbox="media/financial-reports.png":::

> [!NOTE]
> Los informes financieros de muestra en [!INCLUDE[prod_short](includes/prod_short.md)] no están listos para usarse de inmediato. Dependiendo de la forma en que configure sus cuentas de contabilidad, dimensiones, categorías de cuentas del contabilidad y presupuestos, deberá ajustar las definiciones de filas y columnas de muestra y los informes financieros en los que se utilizan para que coincidan con su configuración.

También puede utilizar fórmulas para comparar dos o más informes financieros y definiciones de columnas. Las comparaciones permiten hacer lo siguiente:

- Crear informes financieros personalizados.
- Crear tantos informes financieros como necesite, cada uno de ellos con un nombre diferente.
- Configurar diversas plantillas de informes e imprimir estos con las cifras actuales.

## Ruta de aprendizaje: Crear informes financieros en Microsoft Dynamics 365 Business Central

¿Quiere aprender a crear presupuestos y luego utilizar informes financieros, dimensiones y definiciones de filas y columnas para generar los informes financieros que normalmente necesitan las empresas?

Comience en la siguiente ruta de aprendizaje [Crear informes financieros en Microsoft Dynamics 365 Business Central](/training/paths/create-financial-reports-dynamics-365-business-central).

## Crear un nuevo informe financiero

Usa informes financieros para analizar cuentas de contabilidad (G/L) o comparar los movimientos de contabilidad con los presupuestados. Por ejemplo, puede ver los movimientos de contabilidad como porcentajes de los movimientos de presupuesto.

Los informes financieros en la versión estándar de [!INCLUDE[prod_short](includes/prod_short.md)] podría no adaptarse a las necesidades de su negocio. Para crear rápidamente sus propios informes financieros, puede empezar por copiar uno existente, como se describe en el paso 3 siguiente.

1. Elija el icono ![Bombilla que abre la característica Dígame 1.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Informes financieros** y luego elija el vínculo relacionado.  
1. En la página **Informes financieros**, elija la acción **Nuevo** para crear un nuevo nombre de informe financiero. Alternativamente, para reutilizar la configuración de un informe financiero existente, elija la acción **Copiar informe financiero**.
1. Rellene el nombre corto del informe (no se puede cambiar el nombre posteriormente) y la descripción.
1. Elija una definición de fila y una definición de columna.
1. Opcionalmente, elija vistas de análisis para las definiciones de filas y columnas.
1. Elija la acción **Editar informe financiero** para tener acceso a más propiedades del informe financiero.
1. En la ficha desplegable **Opciones**, puede editar la descripción del informe, cambiar las definiciones de filas y columnas y definir cómo mostrar las fechas. Las fechas pueden ser una jerarquía Día/Semana/Mes/Trimestre/Año, o utilizar periodos contables. Para obtener más información, vaya a [Comparación de períodos contables usando fórmulas de períodos](bi-column-definitions.md#comparing-accounting-periods-using-period-formulas).
1. En la ficha desplegable **Dimensiones**, puede definir filtros de dimensiones para el informe.
1. Puede obtener una vista previa del informe en el área debajo de la pestaña desplegable **Dimensiones**.

> [!TIP]
> Después de crear un informe financiero, puede utilizar la página **Informe financiero** para obtener una vista previa y validarlo. Elija la acción **Ver informe financiero** para abrir la página.  

> [!NOTE]
> Cuando abre un informe financiero en el modo Ver o Editar, el panel Filtro está disponible. No utilice el panel Filtro para establecer filtros para los datos de su informe. Tales filtros pueden causar errores o no filtrar los datos. En su lugar, utilice los campos de las pestañas desplegables **Opciones** y **Dimensiones** para configurar filtros para el informe.

### Crear o editar una definición de fila

Las definiciones de fila en informes financieros proporcionan un lugar para cálculos que no se puedan realizar directamente en el plan de cuentas. Por ejemplo, puede crear subtotales para grupos de cuentas y luego incluir ese total en otros totales. También puede calcular pasos intermedios que no se muestran en el informe final.

Para obtener más información, vaya a [Definiciones de filas en informes financieros](bi-row-definitions.md).

### Crear o editar una definición de columna

Utilice las definiciones de columnas para especificar las columnas para incluir en el informe resultante. Por ejemplo, puede diseñar una plantilla de informe para comparar el saldo del periodo y el saldo a la fecha del mismo periodo del año actual y del año anterior. Puede tener hasta 15 columnas en una definición de columna. Por ejemplo, las columnas múltiples son útiles para mostrar los presupuestos de 12 meses con una columna que muestre el total.

Para obtener más información, vaya a [Definiciones de columna en informes financieros](bi-column-definitions.md).

## Usar dimensiones en informes financieros

En análisis financiero, una dimensión son datos que agrega a un movimiento como una especie de marcador. Estos datos se utilizan para agrupar movimientos de características similares, como clientes, regiones, productos y vendedor, y así poder recuperar con facilidad estos grupos para su análisis. Puede usar dimensiones en movimientos de diarios, documentos y presupuestos.

Cada dimensión describe el foco del análisis. Así, un análisis de dos dimensiones, por ejemplo, sería ventas por área. Al utilizar más de dos dimensiones cuando se crea una entrada, puede realizar un análisis más complejo. Un ejemplo de análisis complejo es explorar las ventas por campaña de ventas por grupo de clientes por área. Eso le proporciona una mayor visión de su negocio, como por ejemplo, lo bien que está funcionando, dónde está prosperando o no y dónde debería asignar más recursos. Esa información le ayuda a tomar decisiones comerciales más informadas. Para obtener más información, vaya a [Trabajar con dimensiones](finance-dimensions.md).

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

## Imprimir y guardar informes financieros

Puede imprimir informes financieros utilizando los servicios de impresión de su dispositivo. [!INCLUDE[prod_short](includes/prod_short.md)] también ofrece opciones para guardar informes como libros de trabajo de Excel, documentos de Word, archivos PDF y XML.

1. Elija el icono ![Bombilla que abre la característica Dígame 4.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Informes financieros** y luego elija el vínculo relacionado.
1. En la página **Informes financieros**, seleccione el informe financiero que desea imprimir y, a continuación, elija la acción **Imprimir**.
1. Rellene los campos según sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
1. En el campo **Impresora**, seleccione el dispositivo al que se envía el informe.
    1. La opción **(Manejado por el navegador)** indica que no hay una impresora designada para el informe. En este caso, el navegador manejará la impresión y mostrará unos pasos de impresión estándar, donde puede elegir una impresora local conectada a su dispositivo. **(Manejado por el navegador)** no está disponible en la aplicación móvil de [!INCLUDE[prod_short](includes/prod_short.md)] o la aplicación para Teams.
1. Seleccione la acción **Imprimir**.

### Programe un informe financiero o guárdelo como un documento PDF, Word o Excel

Puede guardar un informe financiero en formatos de archivo tales como PDF, XML, Word o Excel. [!INCLUDE[prod_short](includes/prod_short.md)] también puede generar informes financieros recurrentes.

1. Elija el icono ![Bombilla que abre la función Dígame 4.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Informes financieros** y luego elija el vínculo relacionado.
1. En la página **Informes financieros**, seleccione la acción **Imprimir**.
1. Configure el informe en consecuencia, luego elija la acción **Enviar a**.
1. Seleccione el formato de archivo o la acción **Calendario** y elija **Aceptar**.
1. Para generar un informe financiero programado o recurrente, complete los campos. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)].<br><br>Para informes financieros recurrentes, configure los campos **Fecha/hora de inicio más temprana** y **Fecha/hora de caducidad** con la primera y última fecha, respectivamente, para generar el informe financiero. Además, seleccione en qué días se genera el informe configurando el campo **Fórmula de fecha de próxima ejecución** siguiendo el formato explicado en la sección [Usar fórmulas de fecha](ui-enter-date-ranges.md#use-date-formulas).

## Procedimientos recomendados para trabajar con definiciones de informes financieros

Las definiciones de informes financieros no tienen versiones. Cuando cambia la definición de un informe, la versión anterior se reemplaza si el cambio se guarda en la base de datos. La siguiente lista contiene algunos procedimientos recomendados para trabajar con definiciones de informes financieros:

- Si agrega definiciones de informes, elija un buen código y complete el campo de descripción con un texto significativo mientras aún sabe para qué usa el informe. Esta información ayuda a sus compañeros de trabajo (y a usted mismo en el futuro) a trabajar con el informe y tal vez a cambiar la definición del informe.
- Antes de cambiar la definición de un informe, considere la posibilidad de hacer una copia de seguridad del mismo, por si acaso su cambio no funciona como esperaba. Puede limitarse a copiar la definición (dándole un buen nombre) o exportarla. Para obtener más información, vaya a [Importar o exportar definiciones de informes financieros](#import-or-export-financial-report-definitions).
- Si necesita una copia nueva de una definición que [!INCLUDE[prod_short](includes/prod_short.md)] proporciona, una manera fácil de obtenerla es crear una nueva empresa que solo contenga datos de configuración. Luego, exporte la definición e impórtela en la empresa donde la definición necesita una actualización.

## Importar o exportar definiciones de informes financieros

Puede importar y exportar definiciones de informes financieros como paquetes de configuración de RapidStart. Por ejemplo, los paquetes de configuración resultan útiles para compartir información con otras empresas. El paquete se crea en un archivo .rapidstart, que comprime los contenidos.

> [!NOTE]
> Cuando importa definiciones de informes financieros/filas, los registros existentes con los mismos nombres que los que está importando se sustituyen por las nuevas definiciones. El paquete de configuración para una definición de informe no sobrescribirá ninguna definición de fila o columna existente que se utilice en la definición de informe.

Para importar o exportar definiciones de informes financieros, siga estos pasos:

1. Elija el icono ![Bombilla que abre la función Dígame 4](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Informes financieros** y luego elija el vínculo relacionado.
1. Elija el informe financiero, luego elija la acción **Importar informe financiero** o **Exportar informe financiero**, dependiendo de lo que quiera hacer.

Para obtener más información sobre cómo importar o exportar definiciones de filas o columnas de informes financieros, consulte los siguientes artículos: 

- [Importar o exportar definiciones de filas en informes financieros](bi-row-definitions.md#import-or-export-financial-reporting-row-definitions) o
- [Importar o exportar definiciones de columnas en informes financieros](bi-column-definitions.md#import-or-export-financial-report-column-definitions)

## Consulte también

[Definiciones de filas en informes financieros](bi-row-definitions.md)  
[Definiciones de columnas en informes financieros](bi-column-definitions.md)  
[Ejecutar e imprimir informes](ui-work-report.md)  
[Inteligencia empresarial financiera](bi.md)  
[Finanzas](finance.md)  
[Configurar las finanzas](finance-setup-finance.md)  
[Libro mayor y plan de cuentas](finance-general-ledger.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
