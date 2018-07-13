---
title: Realizar un seguimiento de los segmentos y las interacciones relacionadas | Documentos de Microsoft
description: "Obtenga información sobre cómo crear segmentos para definir grupos de contactos y especificar interacciones para los segmentos."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, prospect
ms.date: 06/06/2017
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: e3917573a912a4e51416c4e926443c87513728fe
ms.openlocfilehash: 1962bd9d74f7b4d9600de11f85d1e312f6fb8c09
ms.contentlocale: es-es
ms.lasthandoff: 06/01/2018

---
# <a name="managing-interactions-for-segments"></a><span data-ttu-id="d86e5-103">Administrar interacciones para segmentos</span><span class="sxs-lookup"><span data-stu-id="d86e5-103">Managing Interactions for Segments</span></span>
<span data-ttu-id="d86e5-104">La ventana **Segmento** es un tipo de hoja de cálculo con la que puede:</span><span class="sxs-lookup"><span data-stu-id="d86e5-104">The **Segment** window is a type of worksheet where you can:</span></span>

* <span data-ttu-id="d86e5-105">Crear segmentos.</span><span class="sxs-lookup"><span data-stu-id="d86e5-105">Create segments.</span></span>
* <span data-ttu-id="d86e5-106">Guardar los criterios de segmentación usados para seleccionar los contactos.</span><span class="sxs-lookup"><span data-stu-id="d86e5-106">Save the segmentation criteria you have used to select contacts.</span></span>
* <span data-ttu-id="d86e5-107">Grabar el segmento y registrar interacciones relacionadas con los contactos del segmento.</span><span class="sxs-lookup"><span data-stu-id="d86e5-107">Log the segment and record interactions involving the contacts within the segment.</span></span>

## <a name="segmenting"></a><span data-ttu-id="d86e5-108">Segmentar</span><span class="sxs-lookup"><span data-stu-id="d86e5-108">Segmenting</span></span>
<span data-ttu-id="d86e5-109">Hay varias formas de crear segmentos:</span><span class="sxs-lookup"><span data-stu-id="d86e5-109">There are several ways to create segments:</span></span>

* <span data-ttu-id="d86e5-110">Puede introducir manualmente en las líneas del segmento los contactos que desee incluir en el mismo.</span><span class="sxs-lookup"><span data-stu-id="d86e5-110">You can manually enter the contacts you want to include in the segment in the segment lines.</span></span>
* <span data-ttu-id="d86e5-111">Puede seleccionar contactos.</span><span class="sxs-lookup"><span data-stu-id="d86e5-111">You can select contacts.</span></span>
* <span data-ttu-id="d86e5-112">Puede volver a utilizar un segmento grabado como base para crear uno nuevo.</span><span class="sxs-lookup"><span data-stu-id="d86e5-112">You can reuse a logged segment as the basis to create a new one.</span></span>
* <span data-ttu-id="d86e5-113">Puede volver a utilizar los criterios de segmentación guardados.</span><span class="sxs-lookup"><span data-stu-id="d86e5-113">You can reuse saved segmentation criteria.</span></span>

## <a name="interactions"></a><span data-ttu-id="d86e5-114">Interacciones</span><span class="sxs-lookup"><span data-stu-id="d86e5-114">Interactions</span></span>
<span data-ttu-id="d86e5-115">En la ventana **Segmento**, puede crear a la vez interacciones para varios contactos.</span><span class="sxs-lookup"><span data-stu-id="d86e5-115">In the **Segment** window, you can create interactions for several contacts simultaneously.</span></span> <span data-ttu-id="d86e5-116">Por ejemplo, puede combinar un segmento con un documento de Microsoft Word, para poder enviar una carta a todos los contactos del segmento.</span><span class="sxs-lookup"><span data-stu-id="d86e5-116">For example, you can merge a segment with a Microsoft Word document, so that you can send a letter to all the contacts in the segment.</span></span>

<span data-ttu-id="d86e5-117">Puede especificar información acerca de la interacción del segmento en la cabecera de **Segmento**.</span><span class="sxs-lookup"><span data-stu-id="d86e5-117">You can specify information about the interaction for the segment on the **Segment** header.</span></span> <span data-ttu-id="d86e5-118">Por ejemplo, puede elegir la plantilla de interacción que se usará con todos los contactos, especificar una descripción, un tipo de correspondencia, etc.</span><span class="sxs-lookup"><span data-stu-id="d86e5-118">For example, you can decide which interaction template you want to use for all the contacts, specify a description, a correspondence type, and so on.</span></span> <span data-ttu-id="d86e5-119">Sin embargo, puede modificar esta información en la línea de segmento para cada contacto en particular, por ejemplo, si especifica otra descripción de un contacto.</span><span class="sxs-lookup"><span data-stu-id="d86e5-119">However, you can modify this information in the segment line for each particular contact, for example, by specifying another description for one contact.</span></span> <span data-ttu-id="d86e5-120">Si combina un segmento con un documento de Microsoft Word, puede personalizar el documento para que se envíe a uno o más contactos del segmento, por ejemplo, agregando comentarios personalizados al documento.</span><span class="sxs-lookup"><span data-stu-id="d86e5-120">If you are merging a segment with a Microsoft Word document, you can personalize the document to be sent for one or several of the contacts within the segment, for example, by adding individualized comments to the document.</span></span>

## <a name="logging"></a><span data-ttu-id="d86e5-121">Grabar</span><span class="sxs-lookup"><span data-stu-id="d86e5-121">Logging</span></span>
<span data-ttu-id="d86e5-122">En la ventana **Segmento**, si elige **Registrar**, la aplicación registra las interacciones en la ventana **Mov. log de interacción** y registra el segmento.</span><span class="sxs-lookup"><span data-stu-id="d86e5-122">In the **Segment** window, when you choose **Log**, the application records the interactions in the **Interaction Log Entry** window, and logs the segment.</span></span> <span data-ttu-id="d86e5-123">Después de grabar el segmento, solo podrá encontrarlo en la ventana **Segmentos archivados**.</span><span class="sxs-lookup"><span data-stu-id="d86e5-123">After you have logged the segment, you can only find it in the **Logged Segments** window.</span></span>

<span data-ttu-id="d86e5-124">En la ventana **Segmentos archivados**, puede decidir crear un segmento de seguimiento que contenga los mismos contactos que el segmento que ha archivado.</span><span class="sxs-lookup"><span data-stu-id="d86e5-124">In the **Logged Segments** window, you can decide to create a follow-up segment containing the same contacts as the segment you have logged.</span></span>

## <a name="see-also"></a><span data-ttu-id="d86e5-125">Consulte también</span><span class="sxs-lookup"><span data-stu-id="d86e5-125">See Also</span></span>
[<span data-ttu-id="d86e5-126">Crear segmentos</span><span class="sxs-lookup"><span data-stu-id="d86e5-126">Create Segments</span></span>](marketing-how-create-segment.md)  
[<span data-ttu-id="d86e5-127">Crear interacciones de segmentos</span><span class="sxs-lookup"><span data-stu-id="d86e5-127">Create Interactions for Segments</span></span>](marketing-how-create-interactions.md)  
[<span data-ttu-id="d86e5-128">Administrar segmentos</span><span class="sxs-lookup"><span data-stu-id="d86e5-128">Managing Segments</span></span>](marketing-segments.md)  
[<span data-ttu-id="d86e5-129">Registrar interacciones con contactos</span><span class="sxs-lookup"><span data-stu-id="d86e5-129">Recording Interactions With Contacts</span></span>](marketing-interactions.md)  
[<span data-ttu-id="d86e5-130">Administrar oportunidades de venta</span><span class="sxs-lookup"><span data-stu-id="d86e5-130">Managing Sales Opportunities</span></span>](marketing-manage-sales-opportunities.md)  
[<span data-ttu-id="d86e5-131">Creación y administración de contactos</span><span class="sxs-lookup"><span data-stu-id="d86e5-131">Creating and Managing Contacts</span></span>](marketing-contacts.md)  
[<span data-ttu-id="d86e5-132">Trabajar con Business Central</span><span class="sxs-lookup"><span data-stu-id="d86e5-132">Working with Business Central</span></span>](ui-work-product.md)

