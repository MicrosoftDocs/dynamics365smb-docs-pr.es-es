---
title: Analizar real frente a presupuesto | Documentos de Microsoft
description: Describe cómo analizar los importes reales frente a los importes presupuestados.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: bi, power BI, analysis, KPI
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: d56801d7bb5f032d6bf0f50816ac2a2a6510ddbd
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/29/2019
ms.locfileid: "1245355"
---
# <a name="analyze-actual-amounts-versus-budgeted-amounts"></a>Analizar importes reales frente a importes presupuestados
Como parte de la recopilación, el análisis y el uso compartido de los datos de la empresa, puede ver importes reales comparados con los importes presupuestados para todas las cuentas y durante varios periodos.

Para analizar los importes presupuestados, primero debe crear presupuestos contables. Para obtener más información, consulte [Crear presupuestos contables](finance-how-create-budgets.md).

## <a name="to-view-a-gl-budget"></a>Para ver un presupuesto contable
En un presupuesto con dimensiones, puede filtrar los movimientos y, por lo tanto, ver presupuestos concretos.

1. Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Presupuestos contables** y luego elija el enlace relacionado.
2. En la página **Presupuestos contables**, abra el presupuesto que desee ver.  
3. En la parte superior de la página rellene los campos según sea necesario para definir lo que se muestra. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!NOTE]  
>   Si ha seleccionado **Periodo** en el campo **Muestra como líneas** o **Muestra como columnas**, debe rellenar el campo **Ver por**. Si no ha seleccionado **Periodo** en el campo **Muestra como líneas** o **Muestra como columnas**, escriba el periodo apropiado en el campo **Filtro fecha**.  

> [!NOTE]  
>   Sólo se incluyen en el cálculo los movimientos del presupuesto que incluyan los códigos de filtro que haya introducido en la ficha desplegable **Filtros**. No se incluirán los movimientos de presupuesto que tengan otros códigos de filtro o que no tengan ninguno. Mientras el filtro aparezca en la página, el presupuesto sólo mostrará los movimientos de presupuesto con dichos códigos de filtro.  

> [!TIP]  
>   Si tiene que modificar el presupuesto, puede editar sus movimientos. Elija un importe para ver los movimientos de contabilidad subyacentes.

## <a name="to-view-actual-and-budgeted-amounts-for-all-accounts"></a>Para ver los importes reales y presupuestados de todas las cuentas  
Puede ver presupuestos y compararlos con las cifras reales de varias áreas de [!INCLUDE[d365fin](includes/d365fin_md.md)].

1. Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Plan de cuentas** y luego elija el enlace relacionado.  
2. En la página **Plan de cuentas**, seleccione la acción **Saldo/Ppto. cuenta**.
3. En la parte superior de la página rellene los campos según sea necesario para definir lo que se muestra.  
4. Para ver una especificación que compone un importe que aparece en pantalla, elija el campo.  

> [!NOTE]  
>   Los filtros que establezca en la cabecera de página se aplicarán a los movimientos de contabilidad y a los movimientos de presupuesto.

Las columnas de la izquierda contienen el plan de cuentas. De las cinco columnas de la derecha, las primeras cuatro muestran los importes del Debe y el Haber reales y presupuestados de cada cuenta. La quinta columna muestra las relaciones proporcionales entre los importes reales y presupuestados de la cuenta.  

> [!TIP]  
>   Utilice el campo **Ver por** en la página **Saldo/Ppto. cuenta** seleccionar la longitud del periodo. Utilice el campo **Ver como** para seleccionar el modo de cálculo de los importes **Saldo periodo** o **Saldo a la fecha**. Elija la acción **Periodo anterior** o **Periodo siguiente** para cambiar el periodo.  

## <a name="to-view-actual-and-budgeted-amounts-for-several-periods"></a>Para ver los importes reales y presupuestados de varios periodos  
En lugar de ver los importes reales y presupuestados de todas las cuentas en un único periodo, puede ver varios periodos de una cuenta.  

1. Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Plan de cuentas** y luego elija el enlace relacionado.  
2. En la página **Plan de cuentas**, seleccione la cuenta contable relevante y, después, seleccione la acción **Saldo cuenta/Presupuesto**.  
3. En la parte superior de la página rellene los campos según sea necesario para definir lo que se muestra.   
4. Para ver una especificación de un importe que aparece en pantalla, elija el campo.  

## <a name="see-also"></a>Consulte también
[Inteligencia empresarial](bi.md)  
[Trabajar con esquemas de cuentas](bi-how-work-account-schedule.md)  
[Finanzas](finance.md)  
[Configurar las finanzas](finance-setup-finance.md)  
[Libro mayor y plan de cuentas](finance-general-ledger.md)  
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
