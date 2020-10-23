---
title: Configurar informes 340 para las empresas pequeñas
description: Utilice el siguiente procedimiento para configurar su negocio para que informe en efectivo, es decir, Criterios de contabilidad de efectivo (CAC). Si aún no lo ha hecho, puede configurar grupos de contabilización para la contabilización del IVA en efectivo para compras y ventas.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 003ee699cb16bc3d72d93ca8ae4643f4cdbd0a15
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/01/2020
ms.locfileid: "3923111"
---
# <a name="set-up-340-reports-for-small-businesses"></a><span data-ttu-id="43ba0-104">Configurar informes 340 para las empresas pequeñas</span><span class="sxs-lookup"><span data-stu-id="43ba0-104">Set Up 340 Reports for Small Businesses</span></span>
<span data-ttu-id="43ba0-105">Utilice el siguiente procedimiento para configurar su negocio para que informe en efectivo, es decir, Criterios de contabilidad de efectivo (CAC).</span><span class="sxs-lookup"><span data-stu-id="43ba0-105">Use the following procedure to set up your business to report on a cash basis, that is, Cash Accounting Criteria (CAC).</span></span> <span data-ttu-id="43ba0-106">Si aún no lo ha hecho, puede configurar grupos de contabilización para la contabilización del IVA en efectivo para compras y ventas.</span><span class="sxs-lookup"><span data-stu-id="43ba0-106">If you have not already done so, you can set up posting groups for cash-based VAT accounting for purchases and sales.</span></span>  

<span data-ttu-id="43ba0-107">Cuando rellena un informe 340, se supone que todas las líneas de transacción que están asociadas con el IVA no liquidado se han llevado a cabo bajo contabilidad de efectivo.</span><span class="sxs-lookup"><span data-stu-id="43ba0-107">When you file a report 340, any transaction lines that are associated with unrealized VAT are assumed to have taken place under cash accounting.</span></span>  

<span data-ttu-id="43ba0-108">Después de que la contabilización del IVA esté configurada para manejar el IVA no liquidado, las órdenes de venta o compra impresas, se modificarán para que la siguiente etiqueta en negrita se agregue al informe justo antes de la sección que informa las líneas del documento: **Régimen especial del criterio de caja**.</span><span class="sxs-lookup"><span data-stu-id="43ba0-108">After VAT posting is set up to handle unrealized VAT, any printed sales order, purchase order, and so forth will be modified to have the following label in bold font added to the report just before the section reporting the document lines: **Régimen especial del criterio de caja**.</span></span>  

## <a name="to-set-up-reporting-under-cac"></a><span data-ttu-id="43ba0-109">Para configurar informes según el CAC</span><span class="sxs-lookup"><span data-stu-id="43ba0-109">To set up reporting under CAC</span></span>  

1.  <span data-ttu-id="43ba0-110">Elija el icono ![Bombilla que abre la función Dígame](../../media/ui-search/search_small.png "Dígame qué desea hacer"), introduzca **Configuración de contabilidad** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="43ba0-110">Choose the ![Lightbulb that opens the Tell Me feature](../../media/ui-search/search_small.png "Tell me what you want to do") icon, enter **General Ledger Setup**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="43ba0-111">En la página **Configuración de contabilidad**, en la ficha desplegable **General**, seleccione la casilla **IVA no realizado**.</span><span class="sxs-lookup"><span data-stu-id="43ba0-111">On the **General** FastTab, select the **Unrealized VAT** check box on the **General Ledger Setup** page.</span></span> <span data-ttu-id="43ba0-112">Elija el botón **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="43ba0-112">Choose the **OK** button.</span></span>  
3.  <span data-ttu-id="43ba0-113">Elija el icono ![Bombilla que abre la función Dígame](../../media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Config. grupos registro IVA** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="43ba0-113">Choose the ![Lightbulb that opens the Tell Me feature](../../media/ui-search/search_small.png "Tell me what you want to do") icon, enter **VAT Posting Setup**, and then choose the related link.</span></span>  
4.  <span data-ttu-id="43ba0-114">En la página **Config. grupos registro IVA**, seleccione un grupo para modificar o crear un grupo de registro que tenga cuentas contables generales para tratar los importes de IVA de las diversas cuentas de IVA no realizado en la configuración de grupos registro IVA y elija la acción **Editar**.</span><span class="sxs-lookup"><span data-stu-id="43ba0-114">On the **VAT Posting Setup** page, select a group to modify or create a posting group that has general ledger accounts to treat the VAT amounts for the various unrealized VAT accounts in your VAT Posting Setup, and then choose the **Edit** action.</span></span>  
5.  <span data-ttu-id="43ba0-115">En la ficha desplegable **General**, defina **Tipo IVA no realizado** a **Porcentaje**.</span><span class="sxs-lookup"><span data-stu-id="43ba0-115">On the **General** FastTab, set the **Unrealized VAT Type** to **Percentage**.</span></span>  
6.  <span data-ttu-id="43ba0-116">En las fichas desplegables **Ventas** y **Compras**, puede especificar cuentas contables para los diversos campos **Cuenta IVA no realizado**.</span><span class="sxs-lookup"><span data-stu-id="43ba0-116">On the **Sales** and **Purchase** FastTabs, specify general ledger accounts for the various **VAT Unreal. Account** fields.</span></span>  

## <a name="see-also"></a><span data-ttu-id="43ba0-117">Consulte también</span><span class="sxs-lookup"><span data-stu-id="43ba0-117">See Also</span></span>  
[<span data-ttu-id="43ba0-118">Crear informes de IVA para las autoridades fiscales</span><span class="sxs-lookup"><span data-stu-id="43ba0-118">Report VAT to Tax Authorities</span></span>](../../finance-how-report-vat.md)
