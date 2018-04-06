---
title: "Crear plantillas para las declaraciones telemáticas de IVA en formato de archivo de texto"
description: "Para mostrar las declaraciones de IVA electrónicamente, debe crear plantillas para generar los archivos necesarios. Puede enviar los archivos en formato de texto y en formato XML. Este procedimiento describe cómo crear plantillas para los archivos de texto."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: a6235789d62987e22bef922539689a0c5fad878f
ms.contentlocale: es-es
ms.lasthandoff: 03/22/2018

---
# <a name="create-templates-for-telematic-vat-statements-in-text-file-format"></a><span data-ttu-id="6f78a-105">Crear plantillas para las declaraciones telemáticas de IVA en formato de archivo de texto</span><span class="sxs-lookup"><span data-stu-id="6f78a-105">Create Templates for Telematic VAT Statements in Text File Format</span></span>
<span data-ttu-id="6f78a-106">Para mostrar las declaraciones de IVA electrónicamente, debe crear plantillas para generar los archivos necesarios.</span><span class="sxs-lookup"><span data-stu-id="6f78a-106">In order to submit VAT statements electronically, you must create templates to generate the required files.</span></span> <span data-ttu-id="6f78a-107">Puede enviar los archivos en formato de texto y en formato XML.</span><span class="sxs-lookup"><span data-stu-id="6f78a-107">You can submit files in text format and in XML format.</span></span> <span data-ttu-id="6f78a-108">Este procedimiento describe cómo crear plantillas para los archivos de texto.</span><span class="sxs-lookup"><span data-stu-id="6f78a-108">This procedure describes how to create templates for text files.</span></span>  

<span data-ttu-id="6f78a-109">Para obtener más información, consulte el sitio web de la [Agencia Tributaria](http://go.microsoft.com/fwlink/?LinkID=238181).</span><span class="sxs-lookup"><span data-stu-id="6f78a-109">For more information, see the [Spanish Tax Agency](http://go.microsoft.com/fwlink/?LinkID=238181) website.</span></span>  

## <a name="to-create-a-template-for-vat-statements-in-text-file-format"></a><span data-ttu-id="6f78a-110">Para crear una plantilla para las declaraciones telemáticas de IVA en formato de archivo de texto</span><span class="sxs-lookup"><span data-stu-id="6f78a-110">To create a template for VAT statements in text file format</span></span>  

1.  <span data-ttu-id="6f78a-111">Seleccione el icono ![Buscar página o informe](../../media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Declaración del IVA** y, a continuación, seleccione el vínculo apropiado.</span><span class="sxs-lookup"><span data-stu-id="6f78a-111">Choose the ![Search for Page or Report](../../media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **VAT Statement**, and then choose the appropriate link.</span></span>  
2.  <span data-ttu-id="6f78a-112">Seleccione la declaración de IVA requerida y después seleccione **Diseñar archivo TXT**.</span><span class="sxs-lookup"><span data-stu-id="6f78a-112">Select the required VAT statement, and then choose the **Design txt file** action.</span></span>  
3.  <span data-ttu-id="6f78a-113">En la ventana **Formato transferencia**, rellene los campos tal como se describe en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="6f78a-113">In the **Transference Format** window, fill in the fields as described in the following table.</span></span>  

    > [!IMPORTANT]  
    >  <span data-ttu-id="6f78a-114">Los valores de los campos están determinados por las autoridades fiscales.</span><span class="sxs-lookup"><span data-stu-id="6f78a-114">The values for the fields are determined by the tax authorities.</span></span>  
    >   
    >  <span data-ttu-id="6f78a-115">Para obtener más información, consulte el sitio web de la [Agencia Tributaria](http://go.microsoft.com/fwlink/?LinkID=238181).</span><span class="sxs-lookup"><span data-stu-id="6f78a-115">For more information, see the [Spanish Tax Agency](http://go.microsoft.com/fwlink/?LinkID=238181) website.</span></span>  

    |<span data-ttu-id="6f78a-116">Campo</span><span class="sxs-lookup"><span data-stu-id="6f78a-116">Field</span></span>|<span data-ttu-id="6f78a-117">Description</span><span class="sxs-lookup"><span data-stu-id="6f78a-117">Description</span></span>|  
    |---------------------------------|---------------------------------------|  
    |<span data-ttu-id="6f78a-118">**Nombre decl. IVA**</span><span class="sxs-lookup"><span data-stu-id="6f78a-118">**VAT Stmt. Name**</span></span>|<span data-ttu-id="6f78a-119">Especifique el nombre de la declaración del IVA para el que está diseñada esta plantilla.</span><span class="sxs-lookup"><span data-stu-id="6f78a-119">Specify the VAT statement name that this template is for.</span></span>|  
    |<span data-ttu-id="6f78a-120">**Nº**</span><span class="sxs-lookup"><span data-stu-id="6f78a-120">**No.**</span></span>|<span data-ttu-id="6f78a-121">Especifique el número de campo en el archivo de texto.</span><span class="sxs-lookup"><span data-stu-id="6f78a-121">Specify the field number in the text file.</span></span>|  
    |<span data-ttu-id="6f78a-122">**Posición**</span><span class="sxs-lookup"><span data-stu-id="6f78a-122">**Position**</span></span>|<span data-ttu-id="6f78a-123">Especifique la posición de este campo en el archivo de texto.</span><span class="sxs-lookup"><span data-stu-id="6f78a-123">Specify the position of this field in the text file.</span></span>|  
    |<span data-ttu-id="6f78a-124">**Longitud**</span><span class="sxs-lookup"><span data-stu-id="6f78a-124">**Length**</span></span>|<span data-ttu-id="6f78a-125">Especifique la longitud del campo.</span><span class="sxs-lookup"><span data-stu-id="6f78a-125">Specify the length of the field.</span></span>|  
    |<span data-ttu-id="6f78a-126">**Escriba**</span><span class="sxs-lookup"><span data-stu-id="6f78a-126">**Type**</span></span>|<span data-ttu-id="6f78a-127">Especifique el tipo del campo.</span><span class="sxs-lookup"><span data-stu-id="6f78a-127">Specify the type of the field.</span></span> <span data-ttu-id="6f78a-128">Las opciones disponibles son **Alfanumérico**, **Numérico**, **Fijo**, **Preguntar** y **Divisa**.</span><span class="sxs-lookup"><span data-stu-id="6f78a-128">The available options are **Alphanumerical**, **Numerical**, **Fix**, **Ask**, and **Currency**.</span></span>|  
    |<span data-ttu-id="6f78a-129">**Subtipo**</span><span class="sxs-lookup"><span data-stu-id="6f78a-129">**Subtype**</span></span>|<span data-ttu-id="6f78a-130">Especifique el subtipo del campo.</span><span class="sxs-lookup"><span data-stu-id="6f78a-130">Specify the subtype of the field.</span></span><br /><br /> <span data-ttu-id="6f78a-131">El subtipo especifica si la línea debe mostrar solo la parte entera de un importe, la parte decimal, o el importe total.</span><span class="sxs-lookup"><span data-stu-id="6f78a-131">The subtype specifies if the line must show only the integer part of an amount, the decimal part, or the full amount.</span></span>|  
    |<span data-ttu-id="6f78a-132">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="6f78a-132">**Description**</span></span>|<span data-ttu-id="6f78a-133">Especifique el texto que desea que aparezca en la etiqueta.</span><span class="sxs-lookup"><span data-stu-id="6f78a-133">Specify the text that you want to appear on the label.</span></span>|  
    |<span data-ttu-id="6f78a-134">**Valor**</span><span class="sxs-lookup"><span data-stu-id="6f78a-134">**Value**</span></span>|<span data-ttu-id="6f78a-135">Especifique el valor de la etiqueta.</span><span class="sxs-lookup"><span data-stu-id="6f78a-135">Specify the value for the label.</span></span>|  
    |<span data-ttu-id="6f78a-136">**Caja**</span><span class="sxs-lookup"><span data-stu-id="6f78a-136">**Box**</span></span>|<span data-ttu-id="6f78a-137">Especifique el número de casilla desde donde recuperar los datos.</span><span class="sxs-lookup"><span data-stu-id="6f78a-137">Specify the box number from which to retrieve the data.</span></span>|  

4.  <span data-ttu-id="6f78a-138">Repita el paso anterior para las líneas adicionales en la declaración de IVA.</span><span class="sxs-lookup"><span data-stu-id="6f78a-138">Repeat the previous step for additional lines in the VAT statement.</span></span>  
5.  <span data-ttu-id="6f78a-139">Elija el botón **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="6f78a-139">Choose the **OK** button.</span></span>  

<span data-ttu-id="6f78a-140">Esta acción crea la plantilla.</span><span class="sxs-lookup"><span data-stu-id="6f78a-140">This creates the template.</span></span> <span data-ttu-id="6f78a-141">Ahora puede crear un archivo que luego puede enviar a las autoridades fiscales.</span><span class="sxs-lookup"><span data-stu-id="6f78a-141">Now, you can create a file that you can then submit to the tax authorities.</span></span>  

## <a name="see-also"></a><span data-ttu-id="6f78a-142">Consulte también</span><span class="sxs-lookup"><span data-stu-id="6f78a-142">See Also</span></span>  
 <span data-ttu-id="6f78a-143">[Exportar declaraciones de IVA en formato de texto](how-to-export-vat-statements-in-text-format.md) </span><span class="sxs-lookup"><span data-stu-id="6f78a-143">[Export VAT Statements in Text Format](how-to-export-vat-statements-in-text-format.md) </span></span>  
 [<span data-ttu-id="6f78a-144">Crear plantillas para las declaraciones telemáticas de IVA en formato XML</span><span class="sxs-lookup"><span data-stu-id="6f78a-144">Create Templates for Telematic VAT Statements in XML File Format</span></span>](how-to-create-templates-for-telematic-vat-statements-in-xml-file-format.md)

