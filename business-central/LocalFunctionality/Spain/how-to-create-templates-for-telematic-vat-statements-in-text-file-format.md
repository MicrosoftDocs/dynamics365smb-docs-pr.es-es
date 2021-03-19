---
title: Crear plantillas para las declaraciones telemáticas de IVA en formato de archivo de texto (ES)
description: Para enviar declaraciones de IVA electrónicamente en formato de texto en la versión en español de Business Central, cree plantillas para administrar los formatos.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: a6aa73cd53f63ff32da47fc6267b7035e87400bc
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5382701"
---
# <a name="create-templates-for-telematic-vat-statements-in-text-file-format"></a><span data-ttu-id="53fd9-103">Crear plantillas para las declaraciones telemáticas de IVA en formato de archivo de texto</span><span class="sxs-lookup"><span data-stu-id="53fd9-103">Create Templates for Telematic VAT Statements in Text File Format</span></span>
<span data-ttu-id="53fd9-104">Para mostrar las declaraciones de IVA electrónicamente, debe crear plantillas para generar los archivos necesarios.</span><span class="sxs-lookup"><span data-stu-id="53fd9-104">In order to submit VAT statements electronically, you must create templates to generate the required files.</span></span> <span data-ttu-id="53fd9-105">Puede enviar los archivos en formato de texto y en formato XML.</span><span class="sxs-lookup"><span data-stu-id="53fd9-105">You can submit files in text format and in XML format.</span></span> <span data-ttu-id="53fd9-106">Este procedimiento describe cómo crear plantillas para los archivos de texto.</span><span class="sxs-lookup"><span data-stu-id="53fd9-106">This procedure describes how to create templates for text files.</span></span>  

<span data-ttu-id="53fd9-107">Para obtener más información, consulte el sitio web de la [Agencia Tributaria](https://go.microsoft.com/fwlink/?LinkID=238181).</span><span class="sxs-lookup"><span data-stu-id="53fd9-107">For more information, see the [Spanish Tax Agency](https://go.microsoft.com/fwlink/?LinkID=238181) website.</span></span>  

## <a name="to-create-a-template-for-vat-statements-in-text-file-format"></a><span data-ttu-id="53fd9-108">Para crear una plantilla para las declaraciones telemáticas de IVA en formato de archivo de texto</span><span class="sxs-lookup"><span data-stu-id="53fd9-108">To create a template for VAT statements in text file format</span></span>  

1.  <span data-ttu-id="53fd9-109">Elija el icono ![Bombilla que abre la función Dígame](../../media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Declaración IVA** y luego elija el vínculo correcto.</span><span class="sxs-lookup"><span data-stu-id="53fd9-109">Choose the ![Lightbulb that opens the Tell Me feature](../../media/ui-search/search_small.png "Tell me what you want to do") icon, enter **VAT Statement**, and then choose the appropriate link.</span></span>  
2.  <span data-ttu-id="53fd9-110">Seleccione la declaración de IVA requerida y después seleccione **Diseñar archivo TXT**.</span><span class="sxs-lookup"><span data-stu-id="53fd9-110">Select the required VAT statement, and then choose the **Design txt file** action.</span></span>  
3.  <span data-ttu-id="53fd9-111">En la página **Formato transferencia**, rellene los campos tal como se describe en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="53fd9-111">On the **Transference Format** page, fill in the fields as described in the following table.</span></span>  

    > [!IMPORTANT]  
    >  <span data-ttu-id="53fd9-112">Los valores de los campos están determinados por las autoridades fiscales.</span><span class="sxs-lookup"><span data-stu-id="53fd9-112">The values for the fields are determined by the tax authorities.</span></span>  
    >   
    >  <span data-ttu-id="53fd9-113">Para obtener más información, consulte el sitio web de la [Agencia Tributaria](https://go.microsoft.com/fwlink/?LinkID=238181).</span><span class="sxs-lookup"><span data-stu-id="53fd9-113">For more information, see the [Spanish Tax Agency](https://go.microsoft.com/fwlink/?LinkID=238181) website.</span></span>  

    |<span data-ttu-id="53fd9-114">Campo</span><span class="sxs-lookup"><span data-stu-id="53fd9-114">Field</span></span>|<span data-ttu-id="53fd9-115">Description</span><span class="sxs-lookup"><span data-stu-id="53fd9-115">Description</span></span>|  
    |---------------------------------|---------------------------------------|  
    |<span data-ttu-id="53fd9-116">**Nombre decl. IVA**</span><span class="sxs-lookup"><span data-stu-id="53fd9-116">**VAT Stmt. Name**</span></span>|<span data-ttu-id="53fd9-117">Especifique el nombre de la declaración del IVA para el que está diseñada esta plantilla.</span><span class="sxs-lookup"><span data-stu-id="53fd9-117">Specify the VAT statement name that this template is for.</span></span>|  
    |<span data-ttu-id="53fd9-118">**Nº**</span><span class="sxs-lookup"><span data-stu-id="53fd9-118">**No.**</span></span>|<span data-ttu-id="53fd9-119">Especifique el número de campo en el archivo de texto.</span><span class="sxs-lookup"><span data-stu-id="53fd9-119">Specify the field number in the text file.</span></span>|  
    |<span data-ttu-id="53fd9-120">**Posición**</span><span class="sxs-lookup"><span data-stu-id="53fd9-120">**Position**</span></span>|<span data-ttu-id="53fd9-121">Especifique la posición de este campo en el archivo de texto.</span><span class="sxs-lookup"><span data-stu-id="53fd9-121">Specify the position of this field in the text file.</span></span>|  
    |<span data-ttu-id="53fd9-122">**Longitud**</span><span class="sxs-lookup"><span data-stu-id="53fd9-122">**Length**</span></span>|<span data-ttu-id="53fd9-123">Especifique la longitud del campo.</span><span class="sxs-lookup"><span data-stu-id="53fd9-123">Specify the length of the field.</span></span>|  
    |<span data-ttu-id="53fd9-124">**Escriba**</span><span class="sxs-lookup"><span data-stu-id="53fd9-124">**Type**</span></span>|<span data-ttu-id="53fd9-125">Especifique el tipo del campo.</span><span class="sxs-lookup"><span data-stu-id="53fd9-125">Specify the type of the field.</span></span> <span data-ttu-id="53fd9-126">Las opciones disponibles son **Alfanumérico**, **Numérico**, **Fijo**, **Preguntar** y **Divisa**.</span><span class="sxs-lookup"><span data-stu-id="53fd9-126">The available options are **Alphanumerical**, **Numerical**, **Fix**, **Ask**, and **Currency**.</span></span>|  
    |<span data-ttu-id="53fd9-127">**Subtipo**</span><span class="sxs-lookup"><span data-stu-id="53fd9-127">**Subtype**</span></span>|<span data-ttu-id="53fd9-128">Especifique el subtipo del campo.</span><span class="sxs-lookup"><span data-stu-id="53fd9-128">Specify the subtype of the field.</span></span><br /><br /> <span data-ttu-id="53fd9-129">El subtipo especifica si la línea debe mostrar solo la parte entera de un importe, la parte decimal, o el importe total.</span><span class="sxs-lookup"><span data-stu-id="53fd9-129">The subtype specifies if the line must show only the integer part of an amount, the decimal part, or the full amount.</span></span>|  
    |<span data-ttu-id="53fd9-130">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="53fd9-130">**Description**</span></span>|<span data-ttu-id="53fd9-131">Especifique el texto que desea que aparezca en la etiqueta.</span><span class="sxs-lookup"><span data-stu-id="53fd9-131">Specify the text that you want to appear on the label.</span></span>|  
    |<span data-ttu-id="53fd9-132">**Valor**</span><span class="sxs-lookup"><span data-stu-id="53fd9-132">**Value**</span></span>|<span data-ttu-id="53fd9-133">Especifique el valor de la etiqueta.</span><span class="sxs-lookup"><span data-stu-id="53fd9-133">Specify the value for the label.</span></span>|  
    |<span data-ttu-id="53fd9-134">**Caja**</span><span class="sxs-lookup"><span data-stu-id="53fd9-134">**Box**</span></span>|<span data-ttu-id="53fd9-135">Especifique el número de casilla desde donde recuperar los datos.</span><span class="sxs-lookup"><span data-stu-id="53fd9-135">Specify the box number from which to retrieve the data.</span></span>|  

4.  <span data-ttu-id="53fd9-136">Repita el paso anterior para las líneas adicionales en la declaración de IVA.</span><span class="sxs-lookup"><span data-stu-id="53fd9-136">Repeat the previous step for additional lines in the VAT statement.</span></span>  
5.  <span data-ttu-id="53fd9-137">Elija el botón **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="53fd9-137">Choose the **OK** button.</span></span>  

<span data-ttu-id="53fd9-138">Esta acción crea la plantilla.</span><span class="sxs-lookup"><span data-stu-id="53fd9-138">This creates the template.</span></span> <span data-ttu-id="53fd9-139">Ahora puede crear un archivo que luego puede enviar a las autoridades fiscales.</span><span class="sxs-lookup"><span data-stu-id="53fd9-139">Now, you can create a file that you can then submit to the tax authorities.</span></span>  

## <a name="see-also"></a><span data-ttu-id="53fd9-140">Consulte también</span><span class="sxs-lookup"><span data-stu-id="53fd9-140">See Also</span></span>  
 <span data-ttu-id="53fd9-141">[Exportar declaraciones de IVA en formato de texto](how-to-export-vat-statements-in-text-format.md) </span><span class="sxs-lookup"><span data-stu-id="53fd9-141">[Export VAT Statements in Text Format](how-to-export-vat-statements-in-text-format.md) </span></span>  
 [<span data-ttu-id="53fd9-142">Crear plantillas para las declaraciones telemáticas de IVA en formato XML</span><span class="sxs-lookup"><span data-stu-id="53fd9-142">Create Templates for Telematic VAT Statements in XML File Format</span></span>](how-to-create-templates-for-telematic-vat-statements-in-xml-file-format.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]