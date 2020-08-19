---
title: Crear plantillas para las declaraciones telemáticas de IVA en formato de archivo de texto
description: Para mostrar las declaraciones de IVA electrónicamente, debe crear plantillas para generar los archivos necesarios. Puede enviar los archivos en formato de texto y en formato XML. Este procedimiento describe cómo crear plantillas para los archivos de texto.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: a02113a1809d91aa35b01a510a024e3c19e09bb0
ms.sourcegitcommit: 007b331b6974983ee614db0406f00777da359ecb
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 08/10/2020
ms.locfileid: "3676664"
---
# <a name="create-templates-for-telematic-vat-statements-in-text-file-format"></a><span data-ttu-id="7dc70-105">Crear plantillas para las declaraciones telemáticas de IVA en formato de archivo de texto</span><span class="sxs-lookup"><span data-stu-id="7dc70-105">Create Templates for Telematic VAT Statements in Text File Format</span></span>
<span data-ttu-id="7dc70-106">Para mostrar las declaraciones de IVA electrónicamente, debe crear plantillas para generar los archivos necesarios.</span><span class="sxs-lookup"><span data-stu-id="7dc70-106">In order to submit VAT statements electronically, you must create templates to generate the required files.</span></span> <span data-ttu-id="7dc70-107">Puede enviar los archivos en formato de texto y en formato XML.</span><span class="sxs-lookup"><span data-stu-id="7dc70-107">You can submit files in text format and in XML format.</span></span> <span data-ttu-id="7dc70-108">Este procedimiento describe cómo crear plantillas para los archivos de texto.</span><span class="sxs-lookup"><span data-stu-id="7dc70-108">This procedure describes how to create templates for text files.</span></span>  

<span data-ttu-id="7dc70-109">Para obtener más información, consulte el sitio web de la [Agencia Tributaria](https://go.microsoft.com/fwlink/?LinkID=238181).</span><span class="sxs-lookup"><span data-stu-id="7dc70-109">For more information, see the [Spanish Tax Agency](https://go.microsoft.com/fwlink/?LinkID=238181) website.</span></span>  

## <a name="to-create-a-template-for-vat-statements-in-text-file-format"></a><span data-ttu-id="7dc70-110">Para crear una plantilla para las declaraciones telemáticas de IVA en formato de archivo de texto</span><span class="sxs-lookup"><span data-stu-id="7dc70-110">To create a template for VAT statements in text file format</span></span>  

1.  <span data-ttu-id="7dc70-111">Elija el icono ![Bombilla que abre la función Dígame](../../media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Declaración IVA** y luego elija el vínculo correcto.</span><span class="sxs-lookup"><span data-stu-id="7dc70-111">Choose the ![Lightbulb that opens the Tell Me feature](../../media/ui-search/search_small.png "Tell me what you want to do") icon, enter **VAT Statement**, and then choose the appropriate link.</span></span>  
2.  <span data-ttu-id="7dc70-112">Seleccione la declaración de IVA requerida y después seleccione **Diseñar archivo TXT**.</span><span class="sxs-lookup"><span data-stu-id="7dc70-112">Select the required VAT statement, and then choose the **Design txt file** action.</span></span>  
3.  <span data-ttu-id="7dc70-113">En la página **Formato transferencia**, rellene los campos tal como se describe en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="7dc70-113">On the **Transference Format** page, fill in the fields as described in the following table.</span></span>  

    > [!IMPORTANT]  
    >  <span data-ttu-id="7dc70-114">Los valores de los campos están determinados por las autoridades fiscales.</span><span class="sxs-lookup"><span data-stu-id="7dc70-114">The values for the fields are determined by the tax authorities.</span></span>  
    >   
    >  <span data-ttu-id="7dc70-115">Para obtener más información, consulte el sitio web de la [Agencia Tributaria](https://go.microsoft.com/fwlink/?LinkID=238181).</span><span class="sxs-lookup"><span data-stu-id="7dc70-115">For more information, see the [Spanish Tax Agency](https://go.microsoft.com/fwlink/?LinkID=238181) website.</span></span>  

    |<span data-ttu-id="7dc70-116">Campo</span><span class="sxs-lookup"><span data-stu-id="7dc70-116">Field</span></span>|<span data-ttu-id="7dc70-117">Description</span><span class="sxs-lookup"><span data-stu-id="7dc70-117">Description</span></span>|  
    |---------------------------------|---------------------------------------|  
    |<span data-ttu-id="7dc70-118">**Nombre decl. IVA**</span><span class="sxs-lookup"><span data-stu-id="7dc70-118">**VAT Stmt. Name**</span></span>|<span data-ttu-id="7dc70-119">Especifique el nombre de la declaración del IVA para el que está diseñada esta plantilla.</span><span class="sxs-lookup"><span data-stu-id="7dc70-119">Specify the VAT statement name that this template is for.</span></span>|  
    |<span data-ttu-id="7dc70-120">**Nº**</span><span class="sxs-lookup"><span data-stu-id="7dc70-120">**No.**</span></span>|<span data-ttu-id="7dc70-121">Especifique el número de campo en el archivo de texto.</span><span class="sxs-lookup"><span data-stu-id="7dc70-121">Specify the field number in the text file.</span></span>|  
    |<span data-ttu-id="7dc70-122">**Posición**</span><span class="sxs-lookup"><span data-stu-id="7dc70-122">**Position**</span></span>|<span data-ttu-id="7dc70-123">Especifique la posición de este campo en el archivo de texto.</span><span class="sxs-lookup"><span data-stu-id="7dc70-123">Specify the position of this field in the text file.</span></span>|  
    |<span data-ttu-id="7dc70-124">**Longitud**</span><span class="sxs-lookup"><span data-stu-id="7dc70-124">**Length**</span></span>|<span data-ttu-id="7dc70-125">Especifique la longitud del campo.</span><span class="sxs-lookup"><span data-stu-id="7dc70-125">Specify the length of the field.</span></span>|  
    |<span data-ttu-id="7dc70-126">**Escriba**</span><span class="sxs-lookup"><span data-stu-id="7dc70-126">**Type**</span></span>|<span data-ttu-id="7dc70-127">Especifique el tipo del campo.</span><span class="sxs-lookup"><span data-stu-id="7dc70-127">Specify the type of the field.</span></span> <span data-ttu-id="7dc70-128">Las opciones disponibles son **Alfanumérico**, **Numérico**, **Fijo**, **Preguntar** y **Divisa**.</span><span class="sxs-lookup"><span data-stu-id="7dc70-128">The available options are **Alphanumerical**, **Numerical**, **Fix**, **Ask**, and **Currency**.</span></span>|  
    |<span data-ttu-id="7dc70-129">**Subtipo**</span><span class="sxs-lookup"><span data-stu-id="7dc70-129">**Subtype**</span></span>|<span data-ttu-id="7dc70-130">Especifique el subtipo del campo.</span><span class="sxs-lookup"><span data-stu-id="7dc70-130">Specify the subtype of the field.</span></span><br /><br /> <span data-ttu-id="7dc70-131">El subtipo especifica si la línea debe mostrar solo la parte entera de un importe, la parte decimal, o el importe total.</span><span class="sxs-lookup"><span data-stu-id="7dc70-131">The subtype specifies if the line must show only the integer part of an amount, the decimal part, or the full amount.</span></span>|  
    |<span data-ttu-id="7dc70-132">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="7dc70-132">**Description**</span></span>|<span data-ttu-id="7dc70-133">Especifique el texto que desea que aparezca en la etiqueta.</span><span class="sxs-lookup"><span data-stu-id="7dc70-133">Specify the text that you want to appear on the label.</span></span>|  
    |<span data-ttu-id="7dc70-134">**Valor**</span><span class="sxs-lookup"><span data-stu-id="7dc70-134">**Value**</span></span>|<span data-ttu-id="7dc70-135">Especifique el valor de la etiqueta.</span><span class="sxs-lookup"><span data-stu-id="7dc70-135">Specify the value for the label.</span></span>|  
    |<span data-ttu-id="7dc70-136">**Caja**</span><span class="sxs-lookup"><span data-stu-id="7dc70-136">**Box**</span></span>|<span data-ttu-id="7dc70-137">Especifique el número de casilla desde donde recuperar los datos.</span><span class="sxs-lookup"><span data-stu-id="7dc70-137">Specify the box number from which to retrieve the data.</span></span>|  

4.  <span data-ttu-id="7dc70-138">Repita el paso anterior para las líneas adicionales en la declaración de IVA.</span><span class="sxs-lookup"><span data-stu-id="7dc70-138">Repeat the previous step for additional lines in the VAT statement.</span></span>  
5.  <span data-ttu-id="7dc70-139">Elija el botón **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="7dc70-139">Choose the **OK** button.</span></span>  

<span data-ttu-id="7dc70-140">Esta acción crea la plantilla.</span><span class="sxs-lookup"><span data-stu-id="7dc70-140">This creates the template.</span></span> <span data-ttu-id="7dc70-141">Ahora puede crear un archivo que luego puede enviar a las autoridades fiscales.</span><span class="sxs-lookup"><span data-stu-id="7dc70-141">Now, you can create a file that you can then submit to the tax authorities.</span></span>  

## <a name="see-also"></a><span data-ttu-id="7dc70-142">Consulte también</span><span class="sxs-lookup"><span data-stu-id="7dc70-142">See Also</span></span>  
 <span data-ttu-id="7dc70-143">[Exportar declaraciones de IVA en formato de texto](how-to-export-vat-statements-in-text-format.md) </span><span class="sxs-lookup"><span data-stu-id="7dc70-143">[Export VAT Statements in Text Format](how-to-export-vat-statements-in-text-format.md) </span></span>  
 [<span data-ttu-id="7dc70-144">Crear plantillas para las declaraciones telemáticas de IVA en formato XML</span><span class="sxs-lookup"><span data-stu-id="7dc70-144">Create Templates for Telematic VAT Statements in XML File Format</span></span>](how-to-create-templates-for-telematic-vat-statements-in-xml-file-format.md)
