---
title: Trabajar con esquemas de cuentas | Documentos de Microsoft
description: "Describe cómo utilizar los esquemas de cuentas para crear varias vistas e informes para analizar los datos de rendimiento financiero."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: bi, power BI, analysis, KPI
ms.date: 01/25/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: d01bd220571b7b87d9e631c8a4d75bef951c7433
ms.contentlocale: es-es
ms.lasthandoff: 03/22/2018

---
# <a name="work-with-account-schedules"></a>Trabajar con esquemas de cuentas
Use esquemas de cuentas para obtener información sobre los datos financieros almacenados en su plan de cuentas. Los esquemas de cuentas analizan cifras en cuentas de contabilidad y comparan los movimientos de contabilidad con los presupuestados. Los resultados se muestran en gráficos en el área de trabajo, como el gráfico Flujo de efectivo.  

[!INCLUDE[d365fin](includes/d365fin_md.md)] proporciona algunos esquemas de cuentas de ejemplo que puede utilizar inmediatamente o puede configurar sus propias filas y columnas para especificar las cifras que se compararán. Por ejemplo, puede crear esquemas de cuentas para calcular márgenes de beneficios en dimensiones como departamentos o grupos de clientes. Puede crear tantos resultados financieros personalizados como desee.  

Configurar esquemas de cuentas requiere obtener una comprensión de los datos financieros del plan de cuentas. Por ejemplo, puede ver los movimientos de contabilidad como porcentajes de los movimientos de presupuesto. Para ello es necesario que se creen presupuestos. Para obtener más información, consulte [Crear presupuestos contables](finance-how-create-budgets.md).

## <a name="account-categories-and-account-schedules"></a>Categorías de cuentas y esquemas de cuentas
Puede usar categorías de cuentas para cambiar el diseño de sus balances financieros. Después de configurar las categorías de cuentas en la ventana **Categorías de cuenta** y haya elegido la acción **Generar esquemas de cuentas**, se actualizan los esquemas de cuentas subyacentes para los informes financieros principales. La próxima vez que ejecute uno de estos informes, como el extracto del saldo, se agregan los nuevos totales y subtotales en función de los cambios que haya realizado. Para obtener más información, consulte [Libro mayor y plan de cuentas](finance-general-ledger.md).  

## <a name="to-create-new-account-schedules"></a>Para crear nuevos esquemas de cuentas  
 Usar esquemas de cuentas para analizar cifras en cuentas de contabilidad o comparar los movimientos de contabilidad con los presupuestados. Por ejemplo, puede ver los movimientos de contabilidad como porcentajes de los movimientos de presupuesto.

1. Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Esquemas de cuentas** y, a continuación, seleccione el vínculo relacionado.  
2. En la ventana **Nombre esquema cuenta**, elija la acción **Nuevo** para crear un nuevo nombre de esquema de cuenta.
3. Rellene los campos según sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Elija la acción **Editar esquema cuentas**.
5. En la ventana **Esquema cuentas** rellene los campos según sea necesario.  

    Cuando haya creado un nuevo esquema de cuentas y haya configurado las filas, debe configurar las columnas. Puede configurarlas manualmente o bien puede asignar una plantilla de columna predefinida al esquema de cuentas.
6. Elija la acción **Editar configuración de disposición de columna**.
7. En la ventana **Plantilla columna** rellene los campos según sea necesario.

> [!NOTE]  
>   Si no ha asignado una plantilla de columna genérica al esquema de cuentas, debe configurar las columnas manualmente.   

### <a name="to-create-a-column-that-calculates-percentages"></a>Para crear una columna que calcule porcentajes  
En ocasiones, podría desear incluir una columna en un esquema de cuentas para calcular los porcentajes de un total. Por ejemplo, si tiene una serie de filas que detallan las ventas por dimensión, podría desear crear una columna para indicar el porcentaje de las ventas totales que representa cada fila.

1. Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Esquemas de cuentas** y, a continuación, seleccione el vínculo relacionado.
2. En la ventana **Nombres de esquema de cuentas**, seleccione un esquema de cuenta.  
3. Elija la acción **Editar esquema cuentas** para configurar una fila del esquema de cuentas para calcular el total en el que se basarán los porcentajes.  
4. Inserta una línea justo encima de la primera fila para la que desea que se muestre un porcentaje.  
5. Rellene los campos de la línea como se indica a continuación: en el campo **Tipo sumatorio**, especifique **Fijar base para porcentaje**. En el campo **Sumatorio**, introduzca una fórmula para el total en el que el porcentaje se basará. Por ejemplo, si la fila 11 contiene las ventas totales, escriba **11**.  
6. Elija la acción **Editar configuración de disposición de columna** para configurar una columna.  
7. Rellene los campos de la línea como se indica a continuación: en el campo **Tipo columna**, seleccione **Fórmula**. En el campo **Fórmula**, introduzca una fórmula para el importe para el que desea calcular un porcentaje, seguida de %. Por ejemplo, si el número de columna N contiene los saldos periodos, escriba **N%**.  
8. Repita los pasos del 4 al 7 para cada grupo de filas que desee subdividir por porcentaje.

## <a name="to-set-up-account-schedules-with-overviews"></a>Para configurar esquemas de cuentas con resúmenes  
Puede usar un esquema de cuentas para crear un extracto que compare las cifras de contabilidad con las cifras presupuestadas.

1. Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Esquemas de cuentas** y, a continuación, seleccione el vínculo relacionado.
2. En la ventana **Nombres de esquema de cuentas**, seleccione un esquema de cuenta.  
3. Elija la acción **Editar esquema cuentas**  
4. En la ventana **Esquema cuentas**, en el campo **Nombre**, seleccione el nombre del esquema de cuentas predeterminado.
5. Elija la acción **Insertar cuentas**.  
6. Seleccione la cuenta que desea incluir en la declaración y, a continuación, seleccione el botón **Aceptar**.

    Estas cuentas se insertan en el esquema de cuentas. Si lo desea, puede modificar la plantilla de columna.  
7. Seleccione la acción **Resumen**.  
8. Haga clic en la ficha desplegable **Filtros dimensión** y asigne al filtro de presupuesto el nombre que desee.  
9. Elija el botón **Aceptar**.  

Ahora puede copiar y pegar el extracto del presupuesto en una hoja de cálculo.

## <a name="see-also"></a>Consulte también
[Inteligencia empresarial](bi.md)  
[Finanzas](finance.md)  
[Configurar las finanzas](finance-setup-finance.md)  
[Libro mayor y plan de cuentas](finance-general-ledger.md)  
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

