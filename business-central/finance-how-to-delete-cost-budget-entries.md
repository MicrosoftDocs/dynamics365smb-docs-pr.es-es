---
title: Procedimiento para eliminar movimientos de presupuestos de costes | Documentos de Microsoft
description: Utilice el trabajo por lotes **Eliminar movimientos presupuesto de costes** para anular los movimientos de presupuesto de costes del registro de presupuestos de costes.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: cdd7f7cfb2645d780df47bfb75ec7392c1739843
ms.contentlocale: es-es
ms.lasthandoff: 09/28/2018

---
# <a name="delete-cost-budget-entries"></a>Eliminar movs. ppto. costes
Utilice el trabajo por lotes **Eliminar movimientos presupuesto de costes** para anular los movimientos de presupuesto de costes del registro de presupuestos de costes.  

Para evitar cualquier discontinuidad en movimientos de presupuesto de costes y movimientos de registro de costes, no puede eliminar un único movimiento o sección de movimientos del centro de la lista de los movimientos de registro.  

### <a name="to-delete-a-cost-budget-entry"></a>Para eliminar movimientos de presupuesto de costes  

1.  Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Eliminar movs. ppto. costes** y luego elija el enlace relacionado.  

    El campo **Hasta nº registro** contiene siempre el último número de movimiento de registro, que no se puede cambiar.  

    Puede usar el campo **Desde nº registro** para seleccionar un número de movimiento de registro del que debe iniciar la eliminación.  
2.  Elija el botón **ACEPTAR** para eliminar los movimientos de presupuestos de costes seleccionados.  

> [!NOTE]  
>  Para evitar una eliminación accidental de los movimientos de presupuesto de coste, puede cerrar movimientos de registro marcando las líneas como **Cerrado** en el campo **Cerrado** en la ventana **Registro de presupuesto de costes**.  

## <a name="see-also"></a>Consulte también  
[Contabilidad para costes](finance-manage-cost-accounting.md)
[Crear presupuesto coste](finance-create-cost-budgets.md)  
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

