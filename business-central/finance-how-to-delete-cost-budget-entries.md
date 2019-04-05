---
title: Procedimiento para eliminar movimientos de presupuestos de costes | Documentos de Microsoft
description: Utilice el trabajo por lotes Eliminar movimientos presupuesto de costes para anular los movimientos de presupuesto de costes del registro de presupuestos de costes.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2018
ms.author: sgroespe
ms.openlocfilehash: 7a5647bcb5a58cdf0a38ec037994d6cbe7a9504d
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 03/08/2019
ms.locfileid: "806068"
---
# <a name="delete-cost-budget-entries"></a><span data-ttu-id="e9196-103">Eliminar movs. ppto. costes</span><span class="sxs-lookup"><span data-stu-id="e9196-103">Delete Cost Budget Entries</span></span>
<span data-ttu-id="e9196-104">Utilice el trabajo por lotes **Eliminar movimientos presupuesto de costes** para anular los movimientos de presupuesto de costes del registro de presupuestos de costes.</span><span class="sxs-lookup"><span data-stu-id="e9196-104">You use the **Delete Cost Budget Entries** batch job to cancel cost budget entries from the cost budget register.</span></span>  

<span data-ttu-id="e9196-105">Para evitar cualquier discontinuidad en movimientos de presupuesto de costes y movimientos de registro de costes, no puede eliminar un único movimiento o sección de movimientos del centro de la lista de los movimientos de registro.</span><span class="sxs-lookup"><span data-stu-id="e9196-105">To prevent any gaps in the cost budget entries and cost register entries, you cannot delete a single entry or a batch of entries in the middle of the list of register entries.</span></span>  

### <a name="to-delete-a-cost-budget-entry"></a><span data-ttu-id="e9196-106">Para eliminar movimientos de presupuesto de costes</span><span class="sxs-lookup"><span data-stu-id="e9196-106">To delete a cost budget entry</span></span>  

1.  <span data-ttu-id="e9196-107">Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Eliminar movs. ppto. costes** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="e9196-107">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Delete Cost Budget Entries**, and then choose the related link.</span></span>  

    <span data-ttu-id="e9196-108">El campo **Hasta nº registro**</span><span class="sxs-lookup"><span data-stu-id="e9196-108">The **To Register No.**</span></span> <span data-ttu-id="e9196-109">contiene siempre el último número de movimiento de registro, que no se puede cambiar.</span><span class="sxs-lookup"><span data-stu-id="e9196-109">field contains the last register entry number and cannot be changed.</span></span>  

    <span data-ttu-id="e9196-110">Puede usar el campo **Desde nº registro**</span><span class="sxs-lookup"><span data-stu-id="e9196-110">You can use the **From Register No.**</span></span> <span data-ttu-id="e9196-111">para seleccionar un número de movimiento de registro del que debe iniciar la eliminación.</span><span class="sxs-lookup"><span data-stu-id="e9196-111">field to select a register entry number from which the deletion should begin.</span></span>  
2.  <span data-ttu-id="e9196-112">Elija el botón **ACEPTAR** para eliminar los movimientos de presupuestos de costes seleccionados.</span><span class="sxs-lookup"><span data-stu-id="e9196-112">Choose the **OK** button to delete the selected cost budget entries.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="e9196-113">Para evitar una eliminación accidental de los movimientos de presupuesto de coste, puede cerrar movimientos de registro marcando las líneas como **Cerrado** en el campo **Cerrado** en la página **Registro de presupuesto de costes**.</span><span class="sxs-lookup"><span data-stu-id="e9196-113">To avoid an accidental deletion of cost budget entries, you can close register entries by marking the lines as **Closed** in the **Closed** field on the **Cost Budget Registers** page.</span></span>  

## <a name="see-also"></a><span data-ttu-id="e9196-114">Consulte también</span><span class="sxs-lookup"><span data-stu-id="e9196-114">See Also</span></span>  
<span data-ttu-id="e9196-115">[Contabilidad para costes](finance-manage-cost-accounting.md)
[Crear presupuesto coste](finance-create-cost-budgets.md)</span><span class="sxs-lookup"><span data-stu-id="e9196-115">[Accounting for Costs](finance-manage-cost-accounting.md)
[Creating Cost Budgets](finance-create-cost-budgets.md)</span></span>  
<span data-ttu-id="e9196-116">[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="e9196-116">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
