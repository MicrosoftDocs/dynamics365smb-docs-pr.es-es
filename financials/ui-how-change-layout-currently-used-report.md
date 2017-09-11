---
title: "Cambiar el aspecto de un informe seleccionando otro diseño | Documentos de Microsoft"
description: "Puede utilizar diseños distintos para un informe y cambiar de un diseño a otro para cambiar el aspecto de un informe."
services: project-madeira
documentationcenter: 
author: SusanneWindfeldPedersen
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customized report, document layout, logo, personalize
ms.date: 03/29/2017
ms.author: solsen
ms.translationtype: Human Translation
ms.sourcegitcommit: c9eb0f1270a431c0996bffdd610cdebeaf85c216
ms.openlocfilehash: 54cc709845a79f33034ced2e720948733216cc04
ms.contentlocale: es-es
ms.lasthandoff: 09/11/2017

---
# <a name="how-to-change-which-layout-is-currently-used-on-a-report"></a><span data-ttu-id="e1369-103">Cambiar el diseño que se usa actualmente en un informe</span><span class="sxs-lookup"><span data-stu-id="e1369-103">How to: Change Which Layout is Currently Used on a Report</span></span>
<span data-ttu-id="e1369-104">Un informe se puede configurar con varios diseños de informe, entre los que puede cambiar según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="e1369-104">A report can be set up with more than one report layout, which you can then switch among as needed.</span></span>

<span data-ttu-id="e1369-105">Según los diseños disponibles para un informe, puede optar por usar un diseño de informe de RDLC integrado, un diseño de informe de Word integrado o un diseño personalizado.</span><span class="sxs-lookup"><span data-stu-id="e1369-105">Depending on the layouts that are available for a report, you can choose to use a built-in RDLC report layout, a built-in Word report layout, or a custom layout.</span></span> <span data-ttu-id="e1369-106">Para obtener más información acerca de los diseños de informe de RDLC y de Word, diseños personalizados e integrados y otros temas, consulte [Gestionar diseños de informe](ui-manage-report-layouts.md).</span><span class="sxs-lookup"><span data-stu-id="e1369-106">For more information about RDLC and Word report layouts, built-in and custom layouts, and more, see [Manage Report Layouts](ui-manage-report-layouts.md).</span></span>

## <a name="to-change-the-layout-that-is-used-on-a-report"></a><span data-ttu-id="e1369-107">Para cambiar el diseño que se usa en un informe</span><span class="sxs-lookup"><span data-stu-id="e1369-107">To change the layout that is used on a report</span></span>
1. <span data-ttu-id="e1369-108">Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "Search for Page or Report icon"), escriba **Selección de diseño de informes** y, a continuación, seleccione el vínculo relacionado.</span><span class="sxs-lookup"><span data-stu-id="e1369-108">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Report Layout Selection**, and then choose the related link.</span></span>  
   <span data-ttu-id="e1369-109">La ventana **Selección de diseño de informes** muestra todos los informes disponibles en la empresa especificada en el campo Empresa en la parte superior de la ventana.</span><span class="sxs-lookup"><span data-stu-id="e1369-109">The **Report Layout Selection** window lists all the reports that are available for the company that is specified in the Company field at the top of the window.</span></span> <span data-ttu-id="e1369-110">El campo Diseño seleccionado especifica el diseño que actualmente se está usando en el informe.</span><span class="sxs-lookup"><span data-stu-id="e1369-110">The Selected Layout field specifies the layout that is currently used on the report.</span></span>
2. <span data-ttu-id="e1369-111">Establezca el campo **Empresa** en la parte superior de la ventana en la empresa que incluye el informe.</span><span class="sxs-lookup"><span data-stu-id="e1369-111">Set the **Company** field at the top of the window to the company that includes the report.</span></span>
3. <span data-ttu-id="e1369-112">Para cambiar el diseño que se usa en un informe, en la fila del informe en la lista, establezca el campo **Diseño seleccionado** en una de las opciones siguientes:</span><span class="sxs-lookup"><span data-stu-id="e1369-112">To change the layout that is used by a report, in the row for the report in the list, set the **Selected Layout** field to one of the following options:</span></span>
   * <span data-ttu-id="e1369-113">Usa el diseño de informe de RDLC integrado en el informe.</span><span class="sxs-lookup"><span data-stu-id="e1369-113">RDLC (built-in), uses the built-in RDLC report layout on the report.</span></span>
   * <span data-ttu-id="e1369-114">Usa el diseño de informe de Word integrado en el informe.</span><span class="sxs-lookup"><span data-stu-id="e1369-114">Word (built-in), uses the built-in Word report layout on the report.</span></span>
   * <span data-ttu-id="e1369-115">Custom, usa un diseño personalizado en el informe.</span><span class="sxs-lookup"><span data-stu-id="e1369-115">Custom, uses a custom layout on the report.</span></span>  
     <span data-ttu-id="e1369-116">Puede ver qué diseños personalizados estarán disponibles para el informe en el cuadro informativo Parte de diseños de informe.</span><span class="sxs-lookup"><span data-stu-id="e1369-116">You can see which custom layouts are available for the report in the Report Layouts Part FactBox.</span></span> <span data-ttu-id="e1369-117">Si no hay diseños personalizados para el informe, deberá crear uno primero.</span><span class="sxs-lookup"><span data-stu-id="e1369-117">If there are no custom layouts for the report, then you will have to create one first.</span></span> <span data-ttu-id="e1369-118">Si elige esta opción, vaya al procedimiento siguiente para especificar el diseño personalizado que desea usar.</span><span class="sxs-lookup"><span data-stu-id="e1369-118">If you choose this option, go to the next procedure to specify the custom layout that you want to use.</span></span>

    > [!NOTE]  
    >   <span data-ttu-id="e1369-119">Si elige **RDLC (integrado)** o **Word (integrado)** y recibe un mensaje de error en el que se indica que el informe no tiene un diseño del tipo especificado, debe elegir otra opción de diseño o crear un diseño de informe personalizado del tipo que desea usar.</span><span class="sxs-lookup"><span data-stu-id="e1369-119">If you choose **RDLC (built-in)** or **Word (built-in)** and you get an error message that the report does not have a layout of the specified type, then you must choose another layout option or create a custom report layout of the type that you want to use.</span></span>

<span data-ttu-id="e1369-120">Si ha seleccionado un diseño de informe de RDLC o de Word, no se requiere ninguna otra acción y el diseño se utilizará la próxima vez que se ejecute el informe.</span><span class="sxs-lookup"><span data-stu-id="e1369-120">If you selected a built-in RDLC or Word report layout, then no further action is required and the layout will be used the next time the report is run.</span></span>

## <a name="to-specify-a-custom-layout-on-a-report"></a><span data-ttu-id="e1369-121">Para especificar un diseño personalizado en un informe</span><span class="sxs-lookup"><span data-stu-id="e1369-121">To specify a custom layout on a report</span></span>
1. <span data-ttu-id="e1369-122">El diseño personalizado que se usará en el informe se especifica en la ventana **Diseños de informe personalizados**.</span><span class="sxs-lookup"><span data-stu-id="e1369-122">You specify which custom layout to use on the report from the **Custom Report Layouts** window.</span></span> <span data-ttu-id="e1369-123">Si la ventana **Diseños de informes personalizados** no está abierta, seleccione el botón de búsqueda en el campo **Descripción de diseño de informe**.</span><span class="sxs-lookup"><span data-stu-id="e1369-123">If the **Custom Report Layouts** window is not open, then in the **Report Layout Description** field, choose the lookup button.</span></span>
2. <span data-ttu-id="e1369-124">En la ventana **Diseños de informe personalizados**, seleccione la fila del diseño personalizado que desee usar y, a continuación, cierre la ventana.</span><span class="sxs-lookup"><span data-stu-id="e1369-124">In the **Custom Report Layouts** window, select the row for custom layout that you want to use, and then close the window.</span></span>

<span data-ttu-id="e1369-125">Puede volver a la ventana **Selección de diseño de informes**.</span><span class="sxs-lookup"><span data-stu-id="e1369-125">You return to the **Report Layout Selection** window.</span></span> <span data-ttu-id="e1369-126">El nombre del diseño personalizado seleccionado se muestra en el campo **Descripción de diseño personalizado**.</span><span class="sxs-lookup"><span data-stu-id="e1369-126">The name of the selected custom layout displays in the **Custom Layout Description** field.</span></span> <span data-ttu-id="e1369-127">El diseño personalizado se utilizará la siguiente vez que se ejecute el informe.</span><span class="sxs-lookup"><span data-stu-id="e1369-127">The custom layout will be used the next time that you run the report.</span></span>

## <a name="see-also"></a><span data-ttu-id="e1369-128">Consulte también</span><span class="sxs-lookup"><span data-stu-id="e1369-128">See Also</span></span>
[<span data-ttu-id="e1369-129">Gestión de diseños de informe</span><span class="sxs-lookup"><span data-stu-id="e1369-129">Managing Report Layouts</span></span>](ui-manage-report-layouts.md)  
<span data-ttu-id="e1369-130">[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="e1369-130">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

