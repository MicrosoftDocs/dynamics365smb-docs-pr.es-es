---
title: Conectar los datos con Flow | Documentos de Microsoft
description: "Puede hacer que los datos de Financials estén disponibles como un origen de datos y especificar una URL de OData de sus servicios web para generar un flujo de trabajo automatizado."
documentationcenter: 
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: workflow, Odata, Power App, SOAP
ms.date: 01/25/2018
ms.author: solsen
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 23e9ebbb75d23595d568d022526e551bf590a979
ms.contentlocale: es-es
ms.lasthandoff: 03/22/2018

---
# <a name="using-included365finincludesd365finmdmd-in-an-automated-workflow"></a><span data-ttu-id="00fff-103">Usar [!INCLUDE[d365fin](includes/d365fin_md.md)] en un flujo de trabajo automatizado</span><span class="sxs-lookup"><span data-stu-id="00fff-103">Using [!INCLUDE[d365fin](includes/d365fin_md.md)] in an Automated Workflow</span></span>
<span data-ttu-id="00fff-104">Puede utilizar sus datos de [!INCLUDE[d365fin](includes/d365fin_md.md)] como parte de un flujo de trabajo de Microsoft Flow.</span><span class="sxs-lookup"><span data-stu-id="00fff-104">You can use your [!INCLUDE[d365fin](includes/d365fin_md.md)] data as part of a workflow in Microsoft Flow.</span></span>  

> [!NOTE]  
>   <span data-ttu-id="00fff-105">Debe disponer de una cuenta válida con [!INCLUDE[d365fin](includes/d365fin_md.md)] y con Flow.</span><span class="sxs-lookup"><span data-stu-id="00fff-105">You must have a valid account with [!INCLUDE[d365fin](includes/d365fin_md.md)] and with Flow.</span></span>  

## <a name="to-add-included365finincludesd365finmdmd-as-a-data-source-in-flow"></a><span data-ttu-id="00fff-106">Para agregar [!INCLUDE[d365fin](includes/d365fin_md.md)] como origen de datos de Flow</span><span class="sxs-lookup"><span data-stu-id="00fff-106">To add [!INCLUDE[d365fin](includes/d365fin_md.md)] as a data source in Flow</span></span>
1. <span data-ttu-id="00fff-107">En el explorador, vaya a [flow.microsoft.com](https://flow.microsoft.com/en-us/) y, a continuación, inicie sesión.</span><span class="sxs-lookup"><span data-stu-id="00fff-107">In your browser, navigate to [flow.microsoft.com](https://flow.microsoft.com/en-us/), and then sign in.</span></span>
2. <span data-ttu-id="00fff-108">Seleccione **Mis flujos** en la cinta en la parte superior de la página.</span><span class="sxs-lookup"><span data-stu-id="00fff-108">Choose **My Flows** from the ribbon at the top of the page.</span></span>
3. <span data-ttu-id="00fff-109">En la ventana **Mis flujos**, elija la opción **Crear desde cero**.</span><span class="sxs-lookup"><span data-stu-id="00fff-109">In the **My Flows** window, choose the **Create from blank** option.</span></span>
4. <span data-ttu-id="00fff-110">En la lista de disparadores disponibles, seleccione uno de los de [!INCLUDE[d365fin](includes/d365fin_md.md)] disponibles:</span><span class="sxs-lookup"><span data-stu-id="00fff-110">From the list of available triggers, select one of the [!INCLUDE[d365fin](includes/d365fin_md.md)] triggers available:</span></span>  
    <span data-ttu-id="00fff-111">*Cuando se solicite la aprobación de un cliente*,</span><span class="sxs-lookup"><span data-stu-id="00fff-111">*When a customer approval is requested*,</span></span>  
    <span data-ttu-id="00fff-112">*Cuando se solicite la aprobación de un lote de diario general*,</span><span class="sxs-lookup"><span data-stu-id="00fff-112">*When a general journal batch approval is requested*,</span></span>  
    <span data-ttu-id="00fff-113">*Cuando se solicite la aprobación de una línea de diario general*,</span><span class="sxs-lookup"><span data-stu-id="00fff-113">*When a general journal line approval is requested*,</span></span>  
    <span data-ttu-id="00fff-114">*Cuando se solicite la aprobación de un artículo*,</span><span class="sxs-lookup"><span data-stu-id="00fff-114">*When an item approval is requested*,</span></span>  
    <span data-ttu-id="00fff-115">*Cuando se solicite la aprobación de un documento de compra*,</span><span class="sxs-lookup"><span data-stu-id="00fff-115">*When a purchase document approval is requested*,</span></span>  
    <span data-ttu-id="00fff-116">*Cuando se solicite la aprobación de un documento de ventas*, o</span><span class="sxs-lookup"><span data-stu-id="00fff-116">*When a sales document approval is requested*, or</span></span>  
    <span data-ttu-id="00fff-117">*Cuando se solicite la aprobación de un proveedor*.</span><span class="sxs-lookup"><span data-stu-id="00fff-117">*When a vendor aproval is requested*.</span></span>
5. <span data-ttu-id="00fff-118">Flow le solicitará que seleccione una empresa en el suscriptor [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="00fff-118">Flow will prompt you to select a company within your [!INCLUDE[d365fin](includes/d365fin_md.md)] tenant.</span></span> <span data-ttu-id="00fff-119">Debido a que cada paso de Flow es independiente del siguiente, es posible que deba definir la empresa varias veces al usar una plantilla de [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="00fff-119">Because each step in the Flow is independent of the next, you may be required to define the company multiple times when using a [!INCLUDE[d365fin](includes/d365fin_md.md)] template.</span></span>

<span data-ttu-id="00fff-120">Ya se ha conectado correctamente con los datos de Business Central y está preparado para comenzar a crear su flujo.</span><span class="sxs-lookup"><span data-stu-id="00fff-120">At this point, you have successfully connected to your Business Central data and are ready to begin building your flow.</span></span> <span data-ttu-id="00fff-121">Para obtener más información, consulte la [documentación de Flow](https://flow.microsoft.com/documentation/getting-started/).</span><span class="sxs-lookup"><span data-stu-id="00fff-121">For more information, see the [Flow documentation](https://flow.microsoft.com/documentation/getting-started/).</span></span>

<span data-ttu-id="00fff-122">Para solucionar problemas de Microsoft Flow, vea [Solución de problemas de integración con Microsoft Flow](across-troubleshooting-how-use-financials-data-source-flow.md).</span><span class="sxs-lookup"><span data-stu-id="00fff-122">For troubleshooting your Microsoft Flow, see [Troubleshooting Integration with Microsoft Flow](across-troubleshooting-how-use-financials-data-source-flow.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="00fff-123">Consulte también</span><span class="sxs-lookup"><span data-stu-id="00fff-123">See Also</span></span>
<span data-ttu-id="00fff-124">[[!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)</span><span class="sxs-lookup"><span data-stu-id="00fff-124">[Welcome to [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)</span></span>  
[<span data-ttu-id="00fff-125">Importar datos de empresa de otros sistemas financieros</span><span class="sxs-lookup"><span data-stu-id="00fff-125">Importing Business Data from Other Finance Systems</span></span>](upload-data.md)  
<span data-ttu-id="00fff-126">[Gestionar usuarios y permisos](ui-how-users-permissions.md)  </span><span class="sxs-lookup"><span data-stu-id="00fff-126">[Manage Users and Permissions](ui-how-users-permissions.md)  </span></span>  
<span data-ttu-id="00fff-127">[Configurar [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)</span><span class="sxs-lookup"><span data-stu-id="00fff-127">[Setting Up [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)</span></span>  
[<span data-ttu-id="00fff-128">Finanzas</span><span class="sxs-lookup"><span data-stu-id="00fff-128">Finance</span></span>](finance.md)  

