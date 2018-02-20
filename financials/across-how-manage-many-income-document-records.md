---
title: "Definir qué documentos entrantes ver | Documentos de Microsoft"
description: "Ajuste la vista predeterminada de los documentos entrantes, como facturas electrónicas, para mejorar el resumen de registros procesados y sin procesar."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: electronic document, e-invoice, incoming document, OCR, ecommerce, document exchange, import invoice
ms.date: 06/02/2016
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 65f3c14b29a5fcf7f855d7ea183445cf2fc1bd95
ms.contentlocale: es-es
ms.lasthandoff: 01/30/2018

---
# <a name="manage-many-incoming-document-records"></a><span data-ttu-id="0a3dc-103">Gestionar varios registros de documento entrantes</span><span class="sxs-lookup"><span data-stu-id="0a3dc-103">Manage Many Incoming Document Records</span></span>
<span data-ttu-id="0a3dc-104">A medida que crea o procesa registros de documento entrantes, el número de líneas en la ventana **Documentos entrantes** puede aumentar hasta el punto de perder la visión general.</span><span class="sxs-lookup"><span data-stu-id="0a3dc-104">As you create or process incoming document records, the number of lines in the **Incoming Documents** window may grow to an extent where you lose overview.</span></span> <span data-ttu-id="0a3dc-105">Por lo tanto, puede establecer los registros de documento entrantes a Procesado para eliminarlos de la vista por defecto.</span><span class="sxs-lookup"><span data-stu-id="0a3dc-105">Therefore, you can set incoming document records to Processed to remove them from the default view.</span></span> <span data-ttu-id="0a3dc-106">Cuando selecciona la acción **Mostrar todos**, puede ver tanto los registros procesados como los que están sin procesar.</span><span class="sxs-lookup"><span data-stu-id="0a3dc-106">When you choose the **Show All** action, you can view both processed and unprocessed records.</span></span>

> [!NOTE]  
>   <span data-ttu-id="0a3dc-107">No puede modificar la información, adjuntar archivos o realizar otros procesos en los registros de documentos entrantes que se hayan establecido en Procesado.</span><span class="sxs-lookup"><span data-stu-id="0a3dc-107">You cannot edit information, attach files, or perform other processes on incoming document records that are set to Processed.</span></span> <span data-ttu-id="0a3dc-108">Primero deberá establecerlos a Sin procesar.</span><span class="sxs-lookup"><span data-stu-id="0a3dc-108">You must first set it to Unprocessed.</span></span>

<span data-ttu-id="0a3dc-109">La casilla de verificación **Procesado** se selecciona automáticamente en los registros de documento entrantes que han sido procesados, pero puede seleccionar o anular la selección de la casilla manualmente.</span><span class="sxs-lookup"><span data-stu-id="0a3dc-109">The **Processed** check box is automatically selected on incoming document records that have been processed, but you can also select or deselect the check box manually.</span></span> <span data-ttu-id="0a3dc-110">Dependiendo de su proceso empresarial, se podrá procesar un registro de documento entrante cuando un documento relacionado haya sido creado para él o se haya adjuntado un archivo.</span><span class="sxs-lookup"><span data-stu-id="0a3dc-110">Depending on your business process, an incoming document record may be processed when a related document has been created for it or a file has been attached.</span></span>

> [!NOTE]  
>   <span data-ttu-id="0a3dc-111">Cuando abre la ventana **Documentos entrantes** con la acción **Mis documentos entrantes** en el área de trabajo, solo se muestran los registros de documento entrantes sin procesar de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="0a3dc-111">When you open the **Incoming Documents** window with the **My Incoming Documents** action on the Role Center, only unprocessed incoming document records are shown by default.</span></span> <span data-ttu-id="0a3dc-112">En este tema se trata como "la vista por defecto".</span><span class="sxs-lookup"><span data-stu-id="0a3dc-112">This is referred to in this topic as "the default view".</span></span>

## <a name="to-remove-incoming-document-records-from-the-default-view"></a><span data-ttu-id="0a3dc-113">Para eliminar los registros de documento entrantes de la vista por defecto</span><span class="sxs-lookup"><span data-stu-id="0a3dc-113">To remove incoming document records from the default view</span></span>
1. <span data-ttu-id="0a3dc-114">En la ventana **Documentos entrantes**, seleccione una o más líneas para los registros de documento entrantes que quiera eliminar de la vista por defecto.</span><span class="sxs-lookup"><span data-stu-id="0a3dc-114">In the **Incoming Documents** window, select one or more lines for incoming document records that you want to remove from the default view.</span></span>
2. <span data-ttu-id="0a3dc-115">Seleccione la acción **Establecer en Procesado**.</span><span class="sxs-lookup"><span data-stu-id="0a3dc-115">Choose the **Set to Processed** action.</span></span>

    <span data-ttu-id="0a3dc-116">Los registros de documento entrantes se eliminan de la vista por defecto y la casilla **Procesado** se selecciona en las líneas.</span><span class="sxs-lookup"><span data-stu-id="0a3dc-116">The incoming document records are removed from the default view, and the **Processed** check box is selected on the lines.</span></span>

> [!NOTE]  
>   <span data-ttu-id="0a3dc-117">También puede realizar esta acción para el registro individual en la ventana **Ficha de documento** entrante.</span><span class="sxs-lookup"><span data-stu-id="0a3dc-117">You can also perform this action for the individual record in the **Incoming Document Card** window.</span></span>

## <a name="to-view-all-incoming-document-records"></a><span data-ttu-id="0a3dc-118">Para ver todos los registros de documento entrantes</span><span class="sxs-lookup"><span data-stu-id="0a3dc-118">To view all incoming document records</span></span>
1. <span data-ttu-id="0a3dc-119">En la ventana **Documentos entrantes**, seleccione la opción **Mostrar todos**.</span><span class="sxs-lookup"><span data-stu-id="0a3dc-119">In the **Incoming Documents** window, choose the **Show All** action.</span></span>

<span data-ttu-id="0a3dc-120">Se muestran todos los registros de documento entrantes, incluyendo aquellos que no tienen seleccionada la casilla **Procesado**.</span><span class="sxs-lookup"><span data-stu-id="0a3dc-120">All incoming document records are displayed, including those where the **Processed** check box is not selected.</span></span>

## <a name="to-add-incoming-document-records-to-the-default-view"></a><span data-ttu-id="0a3dc-121">Para agregar los registros de documento entrantes a la vista por defecto</span><span class="sxs-lookup"><span data-stu-id="0a3dc-121">To add incoming document records to the default view</span></span>
1. <span data-ttu-id="0a3dc-122">En la ventana **Documentos entrantes**, seleccione la opción **Mostrar todos**.</span><span class="sxs-lookup"><span data-stu-id="0a3dc-122">In the **Incoming Documents** window, choose the **Show All** action.</span></span>
2. <span data-ttu-id="0a3dc-123">Seleccione una o más líneas para los registros de documento entrantes que desea que aparezcan en la vista por defecto.</span><span class="sxs-lookup"><span data-stu-id="0a3dc-123">Select one or more lines for incoming document records that you want to appear in the default view.</span></span>
3. <span data-ttu-id="0a3dc-124">Seleccione la acción **Establecer en Sin procesar**.</span><span class="sxs-lookup"><span data-stu-id="0a3dc-124">Choose the **Set to Unprocessed** action.</span></span>  

> [!NOTE]  
>   <span data-ttu-id="0a3dc-125">También puede realizar esta acción para el registro individual en la ventana **Ficha de documento** entrante.</span><span class="sxs-lookup"><span data-stu-id="0a3dc-125">You can also perform this action for the individual record in the **Incoming Document Card** window.</span></span>

## <a name="see-also"></a><span data-ttu-id="0a3dc-126">Consulte también</span><span class="sxs-lookup"><span data-stu-id="0a3dc-126">See Also</span></span>
[<span data-ttu-id="0a3dc-127">Procesar documentos entrantes</span><span class="sxs-lookup"><span data-stu-id="0a3dc-127">Process Incoming Documents</span></span>](across-process-income-documents.md)  
[<span data-ttu-id="0a3dc-128">Documentos entrantes</span><span class="sxs-lookup"><span data-stu-id="0a3dc-128">Incoming Documents</span></span>](across-income-documents.md)  
[<span data-ttu-id="0a3dc-129">Compras</span><span class="sxs-lookup"><span data-stu-id="0a3dc-129">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="0a3dc-130">[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="0a3dc-130">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

