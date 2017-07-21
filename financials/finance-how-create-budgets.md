---
title: Crear presupuestos | Documentos de Microsoft
description: "Describe cómo crear presupuestos para prever diferentes actividades financieras y asigne dimensiones para fines de inteligencia empresarial."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: postpone
ms.date: 06/16/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 7dfd3cc7efe00b48a39982bb220ccc21b7409da4
ms.contentlocale: es-es
ms.lasthandoff: 07/07/2017


---
# <a name="how-to-create--budgets"></a>Crear presupuestos
Puede tener varios presupuestos para idénticos periodos de tiempo si crea presupuestos con nombres distintos. En primer lugar, debe configurar el nombre del presupuesto e introducir las cifras del presupuesto. El nombre del presupuesto se incluye en todos los movimientos de presupuesto que cree.  

 Al crear un presupuesto, puede definir cuatro dimensiones para cada presupuesto. Estas dimensiones específicas de presupuesto se denominan dimensiones de presupuesto. Seleccione las dimensiones de presupuesto para cada uno de los presupuestos a partir de las dimensiones que ya ha configurado. Es posible utilizar las dimensiones de presupuesto para filtrar en un presupuesto y para agregar información de dimensiones a movimientos de presupuesto. Para obtener más información, consulte [Trabajar con dimensiones](finance-dimensions.md).

 Los presupuestos desempeñan una función importante en la inteligencia empresarial, como los extractos financieros en función de los esquemas de cuentas que incluyen movimientos de presupuesto o al analizar los importes presupuestados frente a los reales en el plan de cuentas. Para obtener más información, consulte [Inteligencia empresarial](bi.md).   

 > [!NOTE]  
>   Esta funcionalidad requiere que la experiencia esté definida en **Conjunto de aplicaciones**. Para obtener más información, consulte [Personalizar la experiencia de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-experiences.md).  

### <a name="to-create-a-new-budget"></a>Para crear un nuevo presupuesto  

1. Elija el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Presupuestos contables** y, a continuación, seleccione el vínculo relacionado.  
2. Elija la acción **Editar lista** y, a continuación, rellene los campos según sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
3. Seleccione la acción **Editar presupuesto**.
4. En la parte superior de la ventana **Presupuesto** rellene los campos según sea necesario para definir lo que se muestra.  

    Solo se mostrarán los movimientos que contengan el nombre del presupuesto que ha introducido en el campo **Nombre presupuesto**. Dado que el nombre de presupuesto acaba de crearse, no hay movimientos que coincidan con el filtro. Por tanto, la ventana está vacía.  
5. Para escribir una cantidad, seleccione la celda correspondiente de la matriz. Se abre la ventana **Movs. pptos. contabilidad**.  
6. Cree una nueva línea y rellene el campo **Importe**. Cierre la ventana **Movs. pptos. contabilidad**.  
7. Repita los pasos de 5 y 6 hasta que escriba todos los importes del presupuesto.  

> [!NOTE]  
>  En la ficha desplegable **Filtros** puede filtrar la información de presupuesto por las dimensiones de presupuesto que haya configurado con ese nombre de presupuesto.   

## <a name="see-also"></a>Consulte también
[Finanzas](finance.md)  
[Inteligencia empresarial](bi.md)  
[Configurar las finanzas](finance-setup-finance.md)  
[Libro mayor y plan de cuentas](finance-general-ledger.md)  
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

