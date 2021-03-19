---
title: Encontrar entradas | Microsoft Docs
description: Este artículo describe cómo encontrar documentos y entradas que están relacionadas
author: jswymer
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: find
ms.date: 10/01/2020
ms.author: jswymer
ms.openlocfilehash: 437e0c076b664ad35d5819783e98d9e91abee982
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5393979"
---
# <a name="finding-related-entries-for-posted-documents"></a><span data-ttu-id="c24e5-103">Búsqueda de entradas relacionadas para documentos registrados</span><span class="sxs-lookup"><span data-stu-id="c24e5-103">Finding Related Entries for Posted Documents</span></span> 

<span data-ttu-id="c24e5-104">En este artículo, aprenderá a buscar documentos y entradas que estén relacionados entre sí en función de una información común, como:</span><span class="sxs-lookup"><span data-stu-id="c24e5-104">In this article, you learn how to find documents and entries that are related to each other based on a common information, like:</span></span>

- <span data-ttu-id="c24e5-105">Número de documento o fecha de publicación</span><span class="sxs-lookup"><span data-stu-id="c24e5-105">Document number or posting date</span></span>
- <span data-ttu-id="c24e5-106">Tipo de contacto comercial, número o número de documento externo</span><span class="sxs-lookup"><span data-stu-id="c24e5-106">Business contact type, number, or external document number</span></span>
- <span data-ttu-id="c24e5-107">Número de serie del producto o número de lote</span><span class="sxs-lookup"><span data-stu-id="c24e5-107">Item serial number or lot number</span></span>

<span data-ttu-id="c24e5-108">Esta característica es útil para buscar los movimientos originados por ciertas transacciones.</span><span class="sxs-lookup"><span data-stu-id="c24e5-108">This feature is useful for finding the ledger entries that resulted from certain transactions.</span></span> <span data-ttu-id="c24e5-109">Al realizar búsquedas por número de documentos, puede imprimir el resumen desde el informe Listas de documentos.</span><span class="sxs-lookup"><span data-stu-id="c24e5-109">When you search by document number, you can print the summary from the Document Entries report.</span></span>

## <a name="get-started"></a><span data-ttu-id="c24e5-110">Introducción</span><span class="sxs-lookup"><span data-stu-id="c24e5-110">Get started</span></span>

<span data-ttu-id="c24e5-111">La característica de búsqueda de entradas está disponible en la mayoría de las páginas que muestran documentos publicados o entradas de documentos publicados, tanto para listas como para tarjetas.</span><span class="sxs-lookup"><span data-stu-id="c24e5-111">The find entries feature is readily available on most pages that display posted documents or posted documents entries - for both lists and cards.</span></span> <span data-ttu-id="c24e5-112">Por tanto, el primer paso es abrir una de estas páginas.</span><span class="sxs-lookup"><span data-stu-id="c24e5-112">So the first step is open one of these pages.</span></span> <span data-ttu-id="c24e5-113">Luego, elija la acción **Buscar entradas** o presione las teclas Alt + G.</span><span class="sxs-lookup"><span data-stu-id="c24e5-113">Then, either choose the **Find Entries** action or press the Alt+G keys.</span></span>

<span data-ttu-id="c24e5-114">La página **Buscar entradas** incluye todos los documentos relacionados y las entradas basadas en el n.º documento y la fecha de registro.</span><span class="sxs-lookup"><span data-stu-id="c24e5-114">The **Find Entries** page  includes all related documents and entries based on the document no. and posting date.</span></span> <span data-ttu-id="c24e5-115">La página está dividida en tres secciones:</span><span class="sxs-lookup"><span data-stu-id="c24e5-115">The page is divided into three sections:</span></span>

- <span data-ttu-id="c24e5-116">La sección superior muestra los campos y las acciones que utiliza para filtrar su búsqueda.</span><span class="sxs-lookup"><span data-stu-id="c24e5-116">The top section displays fields and actions that you use for filtering your search.</span></span>
- <span data-ttu-id="c24e5-117">La sección central muestra documentos relacionados basados en la búsqueda.</span><span class="sxs-lookup"><span data-stu-id="c24e5-117">The middle section displays related documents based on the search.</span></span>
- <span data-ttu-id="c24e5-118">La sección inferior muestra información sobre el documento de origen que se encontró mediante la búsqueda.</span><span class="sxs-lookup"><span data-stu-id="c24e5-118">The bottom section displays information about the source document that was found by searching.</span></span>


<!--
 There are two ways to open this page:

- Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Find Entries**, and then choose the related link.

    With this way, the **Find Entries** page might be empty, and you'll have to start searching for entries from scratch.
    
- Open a page that displays posted documents or posted documents entries, either a list or a card. Then, locate and select the **Find Entries** action.

    With this way, the **Find Entries**, page will include all related documents and entries based on the document no. and posting date.


    > [!TIP]
    > If you are on a page that has the **Find Entries** action, press crtl+G to open the **Find Entries** page directly. 
-->

## <a name="search-for-entries"></a><span data-ttu-id="c24e5-119">Buscar entradas</span><span class="sxs-lookup"><span data-stu-id="c24e5-119">Search for entries</span></span>

<span data-ttu-id="c24e5-120">Puede buscar entradas basándose en información sobre el documento, el contacto comercial o la referencia del producto.</span><span class="sxs-lookup"><span data-stu-id="c24e5-120">You can search for entries based on information about either the document, business contact, or item reference.</span></span> <span data-ttu-id="c24e5-121">Para cambiar la búsqueda, seleccione **Accione**, **Buscar por** y luego una de las siguientes acciones:</span><span class="sxs-lookup"><span data-stu-id="c24e5-121">To change the search, select **Actions**, **Find By**, then one of the following actions:</span></span>

|<span data-ttu-id="c24e5-122">Acción</span><span class="sxs-lookup"><span data-stu-id="c24e5-122">Action</span></span>|<span data-ttu-id="c24e5-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="c24e5-123">Description</span></span>|
|------|-----------|
|<span data-ttu-id="c24e5-124">Buscar por documento</span><span class="sxs-lookup"><span data-stu-id="c24e5-124">Find by Document</span></span>|<span data-ttu-id="c24e5-125">Vea entradas según un n.º documento específico o una fecha de registro.</span><span class="sxs-lookup"><span data-stu-id="c24e5-125">View entries based on a specific document number or posting date.</span></span>|
|<span data-ttu-id="c24e5-126">Contacto de negocio</span><span class="sxs-lookup"><span data-stu-id="c24e5-126">Business Contact</span></span> |<span data-ttu-id="c24e5-127">Vea entradas basadas en un tipo de contacto específico, número de contacto, y/o n.º documento externo.</span><span class="sxs-lookup"><span data-stu-id="c24e5-127">View entries based on a specific contact type, contact number, anr/or external document number.</span></span> <span data-ttu-id="c24e5-128">Puede introducir información sobre el documento asignado por un proveedor o un cliente.</span><span class="sxs-lookup"><span data-stu-id="c24e5-128">You can enter document information that was assigned by a vendor or a customer.</span></span> <span data-ttu-id="c24e5-129">Utilice los campos disponibles para buscar documentos de proveedor mediante el uso de los números que el proveedor ha asignado a los documentos.</span><span class="sxs-lookup"><span data-stu-id="c24e5-129">Use the available fields to search for vendor documents by using the numbers that the vendor has assigned the documents.</span></span>|
|<span data-ttu-id="c24e5-130">Referencia a producto</span><span class="sxs-lookup"><span data-stu-id="c24e5-130">Item reference</span></span>|<span data-ttu-id="c24e5-131">Ver entradas basadas en un número de serie o número de lote.</span><span class="sxs-lookup"><span data-stu-id="c24e5-131">View entires based on a serial number or lot number.</span></span> <span data-ttu-id="c24e5-132">Puede escribir el número de lote o número de serie, o filtrar en el número de lote o número de serie en el que quiera buscar.</span><span class="sxs-lookup"><span data-stu-id="c24e5-132">You can enter the lot number or serial number, or filter on the lot number or serial number that you want to search for.</span></span> <span data-ttu-id="c24e5-133">Esta acción resulta útil para ver dónde se uso un número de seguimiento de producto concreto, de qué proveedor se obtuvo o a qué cliente se vendió.</span><span class="sxs-lookup"><span data-stu-id="c24e5-133">This action is useful to see where a specific item tracking number was used, what vendor it came from, or what customer it was sold to.</span></span>|

<span data-ttu-id="c24e5-134">Después de hacer una selección, introduzca la información de búsqueda relevante en los campos de la parte superior.</span><span class="sxs-lookup"><span data-stu-id="c24e5-134">After you make a selection, enter the relevant search information in the fields at the top.</span></span> <span data-ttu-id="c24e5-135">Utilice la información de los campos como ayuda.</span><span class="sxs-lookup"><span data-stu-id="c24e5-135">Use the tooltips on the fields to help.</span></span> <span data-ttu-id="c24e5-136">Cuando haya terminado, elija **Buscar** para iniciar la búsqueda.</span><span class="sxs-lookup"><span data-stu-id="c24e5-136">When you're finished, choose **Find** to start the search.</span></span> <span data-ttu-id="c24e5-137">Si cambia cualquiera de los filtros, deberá volver a elegir **Buscar**.</span><span class="sxs-lookup"><span data-stu-id="c24e5-137">If you change any of the filters, you have to choose **Find** again.</span></span>

> [!TIP]
> <span data-ttu-id="c24e5-138">Para ver un par de ejemplos sobre el uso de **Buscar entradas**, consulte [Seguimiento de productos con seguimiento de productos](inventory-how-to-trace-item-tracked-items.md) y [Tutorial: seguimiento de números de lote de serie](walkthrough-tracing-serial-lot-numbers.md).</span><span class="sxs-lookup"><span data-stu-id="c24e5-138">For a couple examples about using **Find Entries**, see [Trace Item-Tracked Items](inventory-how-to-trace-item-tracked-items.md) and [Walkthrough: Tracing Serial-Lot Numbers](walkthrough-tracing-serial-lot-numbers.md).</span></span>

## <a name="see-related-training-at-microsoft-learn"></a><span data-ttu-id="c24e5-139">Consulte Formación relacionada en [Microsoft Learn](/learn/modules/user-interface-dynamics-365-business-central/index)</span><span class="sxs-lookup"><span data-stu-id="c24e5-139">See Related Training at [Microsoft Learn](/learn/modules/user-interface-dynamics-365-business-central/index)</span></span>

## <a name="see-also"></a><span data-ttu-id="c24e5-140">Consulte también</span><span class="sxs-lookup"><span data-stu-id="c24e5-140">See Also</span></span>

[<span data-ttu-id="c24e5-141">Trabajar con Business Central</span><span class="sxs-lookup"><span data-stu-id="c24e5-141">Working with Business Central</span></span>](ui-work-product.md)  
[<span data-ttu-id="c24e5-142">Agregar una acción de página al área de trabajo</span><span class="sxs-lookup"><span data-stu-id="c24e5-142">Add a Page Action to Your Role Center</span></span>](ui-bookmarks.md)  
[<span data-ttu-id="c24e5-143">Realizar seguimiento de productos seguidos</span><span class="sxs-lookup"><span data-stu-id="c24e5-143">Trace Item-Tracked Items</span></span>](inventory-how-to-trace-item-tracked-items.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]