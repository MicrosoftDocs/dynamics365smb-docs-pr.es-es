---
title: Procedimiento para eliminar movimientos de presupuestos de costes | Documentos de Microsoft
description: Utilice el trabajo por lotes Eliminar movimientos presupuesto de costes para anular los movimientos de presupuesto de costes del registro de presupuestos de costes.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: f7ea29f059c3d2ab54e35b731bfe72d42fffd1f1
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "4750710"
---
# <a name="delete-cost-budget-entries"></a><span data-ttu-id="a75d3-103">Eliminar movs. ppto. costes</span><span class="sxs-lookup"><span data-stu-id="a75d3-103">Delete Cost Budget Entries</span></span>
<span data-ttu-id="a75d3-104">Utilice el trabajo por lotes **Eliminar movimientos presupuesto de costes** para anular los movimientos de presupuesto de costes del registro de presupuestos de costes.</span><span class="sxs-lookup"><span data-stu-id="a75d3-104">You use the **Delete Cost Budget Entries** batch job to cancel cost budget entries from the cost budget register.</span></span>  

<span data-ttu-id="a75d3-105">Para evitar cualquier discontinuidad en movimientos de presupuesto de costes y movimientos de registro de costes, no puede eliminar un único movimiento o sección de movimientos del centro de la lista de los movimientos de registro.</span><span class="sxs-lookup"><span data-stu-id="a75d3-105">To prevent any gaps in the cost budget entries and cost register entries, you cannot delete a single entry or a batch of entries in the middle of the list of register entries.</span></span>  

### <a name="to-delete-a-cost-budget-entry"></a><span data-ttu-id="a75d3-106">Para eliminar movimientos de presupuesto de costes</span><span class="sxs-lookup"><span data-stu-id="a75d3-106">To delete a cost budget entry</span></span>  

1.  <span data-ttu-id="a75d3-107">Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Eliminar movs. ppto. costes** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="a75d3-107">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Delete Cost Budget Entries**, and then choose the related link.</span></span>  

    <span data-ttu-id="a75d3-108">El campo **Hasta nº registro**</span><span class="sxs-lookup"><span data-stu-id="a75d3-108">The **To Register No.**</span></span> <span data-ttu-id="a75d3-109">contiene siempre el último número de movimiento de registro, que no se puede cambiar.</span><span class="sxs-lookup"><span data-stu-id="a75d3-109">field contains the last register entry number and cannot be changed.</span></span>  

    <span data-ttu-id="a75d3-110">Puede usar el campo **Desde nº registro**</span><span class="sxs-lookup"><span data-stu-id="a75d3-110">You can use the **From Register No.**</span></span> <span data-ttu-id="a75d3-111">para seleccionar un número de movimiento de registro del que debe iniciar la eliminación.</span><span class="sxs-lookup"><span data-stu-id="a75d3-111">field to select a register entry number from which the deletion should begin.</span></span>  
2.  <span data-ttu-id="a75d3-112">Elija el botón **ACEPTAR** para eliminar los movimientos de presupuestos de costes seleccionados.</span><span class="sxs-lookup"><span data-stu-id="a75d3-112">Choose the **OK** button to delete the selected cost budget entries.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="a75d3-113">Para evitar una eliminación accidental de los movimientos de presupuesto de coste, puede cerrar movimientos de registro marcando las líneas como **Cerrado** en el campo **Cerrado** en la página **Registro de presupuesto de costes**.</span><span class="sxs-lookup"><span data-stu-id="a75d3-113">To avoid an accidental deletion of cost budget entries, you can close register entries by marking the lines as **Closed** in the **Closed** field on the **Cost Budget Registers** page.</span></span>  

## <a name="see-also"></a><span data-ttu-id="a75d3-114">Consulte también</span><span class="sxs-lookup"><span data-stu-id="a75d3-114">See Also</span></span>  
<span data-ttu-id="a75d3-115">[Contabilidad para costes](finance-manage-cost-accounting.md)
[Crear presupuesto coste](finance-create-cost-budgets.md)</span><span class="sxs-lookup"><span data-stu-id="a75d3-115">[Accounting for Costs](finance-manage-cost-accounting.md)
[Creating Cost Budgets](finance-create-cost-budgets.md)</span></span>  
<span data-ttu-id="a75d3-116">[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="a75d3-116">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>
