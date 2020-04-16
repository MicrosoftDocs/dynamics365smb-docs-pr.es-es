---
title: Importación de muchas imágenes de productos desde un archivo ZIP| Documentos de Microsoft
description: Puede importar varias imágenes de productos de una sola vez. Simplemente asigne a sus archivos de imagen nombres que correspondan a sus números de producto, comprímalos en un archivo zip y, a continuación, utilice la página Importar imágenes de producto para administrar las imágenes de artículo que desea importar.
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: product, image
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: 8478a6fc2a4860f2cd5a2b5a01d6680fbaea3130
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/01/2020
ms.locfileid: "3182185"
---
# <a name="import-multiple-item-pictures"></a><span data-ttu-id="9de89-104">Importar varias imágenes de producto</span><span class="sxs-lookup"><span data-stu-id="9de89-104">Import Multiple Item Pictures</span></span>
<span data-ttu-id="9de89-105">Puede importar varias imágenes de productos de una sola vez.</span><span class="sxs-lookup"><span data-stu-id="9de89-105">You can import multiple item pictures in one go.</span></span> <span data-ttu-id="9de89-106">Simplemente asigne a sus archivos de imagen nombres que correspondan a sus números de producto, comprímalos en un archivo ZIP y, a continuación, utilice la página **Importar imágenes de producto** para administrar las imágenes de artículo que desea importar.</span><span class="sxs-lookup"><span data-stu-id="9de89-106">Simply name your picture files with names corresponding to your item numbers, compress them to a ZIP file, and then use the **Import Item Pictures** page to manage which item pictures to import.</span></span>

<span data-ttu-id="9de89-107">Se admiten todos los formatos de archivo habituales.</span><span class="sxs-lookup"><span data-stu-id="9de89-107">All common file formats are supported.</span></span>

## <a name="to-name-picture-files-by-the-item-names-and-prepare-the-zip-file"></a><span data-ttu-id="9de89-108">Para asignar nombres a los archivos de imagen por los nombres de los productos y preparar el archivo ZIP</span><span class="sxs-lookup"><span data-stu-id="9de89-108">To name picture files by the item names and prepare the ZIP file</span></span>
1. <span data-ttu-id="9de89-109">En la ubicación donde se almacenan las imágenes de producto, asigne a cada archivo un nombre de acuerdo con el número del producto relacionado.</span><span class="sxs-lookup"><span data-stu-id="9de89-109">At the location where your item pictures are stored, name each files according to the number of the related item.</span></span> <span data-ttu-id="9de89-110">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="9de89-110">For example:</span></span>

    |<span data-ttu-id="9de89-111">Nº producto</span><span class="sxs-lookup"><span data-stu-id="9de89-111">Item No.</span></span>|<span data-ttu-id="9de89-112">Nombre de archivo</span><span class="sxs-lookup"><span data-stu-id="9de89-112">File Name</span></span>|
    |-|-|
    |<span data-ttu-id="9de89-113">1000</span><span class="sxs-lookup"><span data-stu-id="9de89-113">1000</span></span>|<span data-ttu-id="9de89-114">1000.bmp</span><span class="sxs-lookup"><span data-stu-id="9de89-114">1000.bmp</span></span>|
    |<span data-ttu-id="9de89-115">1001</span><span class="sxs-lookup"><span data-stu-id="9de89-115">1001</span></span>|<span data-ttu-id="9de89-116">1001.bmp</span><span class="sxs-lookup"><span data-stu-id="9de89-116">1001.bmp</span></span>|
    |<span data-ttu-id="9de89-117">1002</span><span class="sxs-lookup"><span data-stu-id="9de89-117">1002</span></span>|<span data-ttu-id="9de89-118">1002.bmp</span><span class="sxs-lookup"><span data-stu-id="9de89-118">1002.bmp</span></span>|

2. <span data-ttu-id="9de89-119">Reúna todos los archivos en un archivo ZIP.</span><span class="sxs-lookup"><span data-stu-id="9de89-119">Collect all the files in a ZIP file.</span></span> <span data-ttu-id="9de89-120">Por ejemplo, en el Explorador de Windows, seleccione los archivos y, a continuación, seleccione **Enviar a**, **Carpeta comprimida (zip)**.</span><span class="sxs-lookup"><span data-stu-id="9de89-120">For example, in Windows Explorer, select the files, and then choose **Send to**, **Compressed (zipped) folder**.</span></span>     

## <a name="to-import-item-pictures"></a><span data-ttu-id="9de89-121">Para importar imágenes de producto</span><span class="sxs-lookup"><span data-stu-id="9de89-121">To import item pictures</span></span>
1. <span data-ttu-id="9de89-122">Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Config. existencias** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="9de89-122">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Inventory Setup**, and then choose the related link.</span></span>
2. <span data-ttu-id="9de89-123">Seleccione la acción **Importar imágenes de producto**.</span><span class="sxs-lookup"><span data-stu-id="9de89-123">Choose the **Import Item Pictures** action.</span></span>
3. <span data-ttu-id="9de89-124">En el campo **Seleccionar un archivo ZIP**, seleccione la carpeta ZIP correspondiente y, a continuación, seleccione el botón **Abrir**.</span><span class="sxs-lookup"><span data-stu-id="9de89-124">In the **Select a ZIP file** field, select the relevant ZIP folder, and then choose the **Open** button.</span></span>

    <span data-ttu-id="9de89-125">Se crea una línea para cada producto e imagen en la página **Importar imágenes de producto**.</span><span class="sxs-lookup"><span data-stu-id="9de89-125">A line for each item and picture is created on the **Import Item Pictures** page.</span></span>

    > [!NOTE]
    > <span data-ttu-id="9de89-126">Para las fichas de productos que ya tienen una imagen, la casilla **Ya existe la imagen** está seleccionada.</span><span class="sxs-lookup"><span data-stu-id="9de89-126">For item cards that already have a picture, the **Picture Already Exists** check box is selected.</span></span> <span data-ttu-id="9de89-127">Si no desea que se reemplace ninguna imagen existente, desactive la casilla **Reemplazar imágenes**.</span><span class="sxs-lookup"><span data-stu-id="9de89-127">If you do not want any existing pictures to be replaced, deselect the **Replace Pictures** check box.</span></span> <span data-ttu-id="9de89-128">Si no desea que se reemplacen las imágenes individuales existentes, elimine las líneas en cuestión.</span><span class="sxs-lookup"><span data-stu-id="9de89-128">If you do not want individual existing pictures to be replaced, delete the lines in question.</span></span>

3. <span data-ttu-id="9de89-129">Seleccione la acción **Importar imágenes**.</span><span class="sxs-lookup"><span data-stu-id="9de89-129">Choose the **Import Pictures** action.</span></span>

<span data-ttu-id="9de89-130">El campo **Estado de importación** se actualiza para mostrar si la importación de imágenes se ha omitido o completado.</span><span class="sxs-lookup"><span data-stu-id="9de89-130">The **Import Status** field is updated to show if the picture import was skipped or completed.</span></span>       

## <a name="see-also"></a><span data-ttu-id="9de89-131">Consulte también</span><span class="sxs-lookup"><span data-stu-id="9de89-131">See Also</span></span>
[<span data-ttu-id="9de89-132">Registro de productos nuevos</span><span class="sxs-lookup"><span data-stu-id="9de89-132">Register New Items</span></span>](inventory-how-register-new-items.md)  
[<span data-ttu-id="9de89-133">Crear numeración</span><span class="sxs-lookup"><span data-stu-id="9de89-133">Create Number Series</span></span>](ui-create-number-series.md)  
[<span data-ttu-id="9de89-134">Inventario</span><span class="sxs-lookup"><span data-stu-id="9de89-134">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="9de89-135">Compras</span><span class="sxs-lookup"><span data-stu-id="9de89-135">Purchasing</span></span>](purchasing-manage-purchasing.md)  
[<span data-ttu-id="9de89-136">Ccial</span><span class="sxs-lookup"><span data-stu-id="9de89-136">Sales</span></span>](sales-manage-sales.md)  
<span data-ttu-id="9de89-137">[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="9de89-137">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
