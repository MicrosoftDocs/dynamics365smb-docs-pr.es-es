---
title: Definiciones de filas en Financial Reporting
description: Describe cómo funcionan las definiciones de filas en los informes financieros.
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

# Definiciones de filas en Financial Reporting

Las definiciones de fila en informes financieros proporcionan un lugar para cálculos que no se puedan realizar directamente en el plan de cuentas. Por ejemplo, puede crear subtotales para grupos de cuentas y luego incluir ese total en otros totales. También puede calcular pasos intermedios que no se muestran en el informe final.

## Crear o editar una definición de fila

Para crear o editar una definición de fila, siga estos pasos:

1. En la página **Informes financieros**, seleccione el informe financiero pertinente y, a continuación, elija la acción **Editar definición de fila**.
1. Elija las acciones **Insertar cuentas de mayor**, **Insertar cuentas CF** e **Insertar tipos de costos** para crear una fila para cada elemento financiero que desee analizar. Por ejemplo, podría tener una fila para activos corrientes y otra fila para activos fijos. Para obtener inspiración, explore los informes financieros en la empresa de demostración CRONUS.

    > [!NOTE]
    > En el campo **N.º de fila**, se muestran los primeros 10 caracteres de un identificador, como un número de cuenta. Si agrega elementos con identificadores que comienzan con los mismos 10 caracteres, tendrá duplicados en **Nº de fila** . Si es necesario, puede editar manualmente los identificadores después de insertar los elementos. Los identificadores completos se muestran en el campo **Totales**.

> [!NOTE]
> Las columnas que defina en cada línea de la definición de filas representan las columnas tres y superiores de la página **Informe financiero**. Las dos primeras columnas, **N.º fila** y **Descripción**, son fijas.  

## Definiciones de fila integradas

[!INCLUDE[prod_short](includes/prod_short.md)] proporciona ejemplos de definiciones de fila que pueden ayudarle a comenzar rápidamente a configurar informes financieros que se adapten a sus necesidades.

<!-- update this when we release the new templates in 24.1
| Row definition code | Description | How to use this row definition | 
| ------------------- | ----------- | ------------------------------ | 
| TBA 1 | TBA 1 | TBA 1 |
| TBA 2 | TBA 2 | TBA 2 |
| TBA 3 | TBA 3 | TBA 3 |
| TBA 4 | TBA 4 | TBA 4 | 
-->

> [!NOTE]
> Los informes financieros de muestra en [!INCLUDE[prod_short](includes/prod_short.md)] no están listos para usarse de inmediato. Dependiendo de la forma en que configure sus cuentas de contabilidad, dimensiones, categorías de cuentas del contabilidad y presupuestos, deberá ajustar las definiciones de filas y columnas de muestra y los informes financieros en los que se utilizan para que coincidan con su configuración.

## Usar categorías de cuentas para cambiar el diseño de sus balances financieros

Puede usar categorías de cuentas para cambiar el diseño de sus balances financieros. Por ejemplo, una vez configuradas las categorías de cuentas en la página **Categorías de cuenta**, puede elegir la acción **Generar informes financieros** y actualizar los informes financieros subyacentes para los informes financieros principales. La próxima vez que ejecute uno de estos informes, como el informe **Extracto del saldo**, se agregan los nuevos totales y subtotales.

Otro beneficio de utilizar categorías de cuentas del L/M en lugar de las cuentas del L/M sin procesar en las definiciones de filas es que un cambio en la estructura de su plan de cuentas no afecta sus informes financieros.

> [!NOTE]
> Las categorías de cuentas de nivel superior, como el nodo **Pasivo**, son fijas y no puede agregar las suyas. Sin embargo, puede eliminar y agregar categorías de cuenta en niveles inferiores y definir cómo aparece el informe financiero relacionado en los informes.
>
> Debería crear y estructurar sus propias categorías de cuentas de mayor de nivel inferior desde cero, en una jerarquía si es necesario, en lugar de tratar de reorganizar las existentes. Por ejemplo, puede reestructurar el nodo **Pasivo** para contener un nuevo nodo **Capital** seguido por los nodos **Pasivo circulante** y **Pasivos a largo plazo**. Obtenga más información en [Asignación de cuentas del libro mayor a categorías de cuentas](finance-general-ledger.md#account-categories).

## Procedimientos recomendados para trabajar con definiciones de fila

Las definiciones de filas no tienen versiones. Cuando cambia la definición de una fila, la versión anterior se reemplaza si el cambio se guarda en la base de datos. La siguiente lista contiene algunos procedimientos recomendados para trabajar con definiciones de fila:

- Si agrega definiciones de fila, elija un buen código y complete el campo de descripción con un texto significativo mientras aún sabe para qué usa la definición de fila. Esta información ayuda a sus compañeros de trabajo (y a usted mismo en el futuro) a trabajar con el informe financiero y tal vez a cambiar la definición de fila.
- Antes de cambiar la definición de fila, considere la posibilidad de hacer una copia de seguridad del mismo, por si acaso su cambio no funciona como esperaba. Puede limitarse a copiar la definición (dándole un buen nombre) o exportarla. Para obtener más información, vaya a [Importar o exportar definiciones de fila](#import-or-export-financial-reporting-row-definitions).
- Si necesita una copia nueva de una definición que [!INCLUDE[prod_short](includes/prod_short.md)] proporciona, una manera fácil de obtenerla es crear una nueva empresa que solo contenga datos de configuración. Luego, exporte la definición e impórtela en la empresa donde la definición necesita una actualización.

## Importar o exportar definiciones de filas en informes financieros

Puede importar y exportar definiciones de fila como paquetes de configuración de RapidStart. Por ejemplo, los paquetes de configuración resultan útiles para compartir información con otras empresas. El paquete se crea en un archivo .rapidstart, que comprime los contenidos.

> [!NOTE]
> Cuando importe definiciones de fila de informes financieros, los registros existentes con los mismos nombres que los que está importando se sustituyen por las nuevas definiciones. El paquete de configuración para una definición de informe no sobrescribirá ninguna definición de fila o columna existente que se utilice en la definición de informe.

Para importar o exportar definiciones de filas de informes financieros, siga estos pasos:

1. Elija el icono ![Bombilla que abre la característica Dígame 4.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Definiciones de filas** y, a continuación, elija el vínculo relacionado.
1. Seleccione la definición de línea y, a continuación, elija la acción **Importar definición de fila** o **Exportar definición de fila** en función de lo que desee hacer.

## Consulte también

[Definiciones de columnas en informes financieros](bi-column-definitions.md)  
[Preparar informes financieros](bi-how-work-account-schedule.md)  
[Inteligencia empresarial financiera](bi.md)  
[Finanzas](finance.md)  
[Configurar las finanzas](finance-setup-finance.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
