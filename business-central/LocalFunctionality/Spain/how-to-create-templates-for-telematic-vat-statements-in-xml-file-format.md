---
title: Crear plantillas para las declaraciones telemáticas de IVA en formato XML (ES)
description: Para enviar declaraciones de IVA electrónicamente en formato XML en la versión en español de Business Central, cree plantillas para administrar los formatos.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 7b82e25d7f6f077f24c238c2e105091883931608
ms.sourcegitcommit: 311e86d6abb9b59a5483324d8bb4cd1be7949248
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 01/15/2021
ms.locfileid: "5013837"
---
# <a name="create-templates-for-telematic-vat-statements-in-xml-file-format"></a><span data-ttu-id="00aa1-103">Crear plantillas para las declaraciones telemáticas de IVA en formato XML</span><span class="sxs-lookup"><span data-stu-id="00aa1-103">Create Templates for Telematic VAT Statements in XML File Format</span></span>
<span data-ttu-id="00aa1-104">Para mostrar las declaraciones de IVA electrónicamente, debe crear plantillas para generar los archivos necesarios.</span><span class="sxs-lookup"><span data-stu-id="00aa1-104">In order to submit VAT statements electronically, you must create templates to generate the required files.</span></span> <span data-ttu-id="00aa1-105">Puede enviar los archivos en formato de texto y en formato XML.</span><span class="sxs-lookup"><span data-stu-id="00aa1-105">You can submit files in text format and in XML format.</span></span> <span data-ttu-id="00aa1-106">Este procedimiento describe cómo crear plantillas para los archivos XML.</span><span class="sxs-lookup"><span data-stu-id="00aa1-106">This procedure describes how to create templates for XML files.</span></span>  

<span data-ttu-id="00aa1-107">Para obtener más información, consulte el sitio web de la [Agencia Tributaria](https://go.microsoft.com/fwlink/?LinkID=238181).</span><span class="sxs-lookup"><span data-stu-id="00aa1-107">For more information, see the [Spanish Tax Agency](https://go.microsoft.com/fwlink/?LinkID=238181) website.</span></span>  

## <a name="to-create-a-template-for-vat-statements-in-xml-file-format"></a><span data-ttu-id="00aa1-108">Para crear una plantilla para las declaraciones telemáticas de IVA en formato de archivo XML</span><span class="sxs-lookup"><span data-stu-id="00aa1-108">To create a template for VAT statements in XML file format</span></span>  

1.  <span data-ttu-id="00aa1-109">Elija el icono ![Bombilla que abre la función Dígame](../../media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Declaración IVA** y luego elija el vínculo correcto.</span><span class="sxs-lookup"><span data-stu-id="00aa1-109">Choose the ![Lightbulb that opens the Tell Me feature](../../media/ui-search/search_small.png "Tell me what you want to do") icon, enter **VAT Statement**, and then choose the appropriate link.</span></span>  
2.  <span data-ttu-id="00aa1-110">Seleccione la declaración de IVA requerida y después seleccione **Diseñar archivo XML**.</span><span class="sxs-lookup"><span data-stu-id="00aa1-110">Select the required VAT statement, and then choose the **Design XML file** action.</span></span>  
3.  <span data-ttu-id="00aa1-111">En la página **Formato transferencia XML**, rellene los campos tal como se describe en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="00aa1-111">On the **XML Transference Format** page, fill in the fields as described in the following table.</span></span>  

    > [!IMPORTANT]  
    >  <span data-ttu-id="00aa1-112">Los valores de los campos están determinados por las autoridades fiscales.</span><span class="sxs-lookup"><span data-stu-id="00aa1-112">The values for the fields are determined by the tax authorities.</span></span>  
    >   
    >  <span data-ttu-id="00aa1-113">Para obtener más información, consulte el sitio web de la [Agencia Tributaria](https://go.microsoft.com/fwlink/?LinkID=238181).</span><span class="sxs-lookup"><span data-stu-id="00aa1-113">For more information, see the [Spanish Tax Agency](https://go.microsoft.com/fwlink/?LinkID=238181) website.</span></span>  

    |<span data-ttu-id="00aa1-114">Campo</span><span class="sxs-lookup"><span data-stu-id="00aa1-114">Field</span></span>|<span data-ttu-id="00aa1-115">Description</span><span class="sxs-lookup"><span data-stu-id="00aa1-115">Description</span></span>|  
    |---------------------------------|---------------------------------------|  
    |<span data-ttu-id="00aa1-116">**Nombre decl. IVA**</span><span class="sxs-lookup"><span data-stu-id="00aa1-116">**VAT Stmt. Name**</span></span>|<span data-ttu-id="00aa1-117">Especifique el nombre de la declaración del IVA para el que está diseñada esta plantilla.</span><span class="sxs-lookup"><span data-stu-id="00aa1-117">Specify the VAT statement name that this template is for.</span></span>|  
    |<span data-ttu-id="00aa1-118">**Nº**</span><span class="sxs-lookup"><span data-stu-id="00aa1-118">**No.**</span></span>|<span data-ttu-id="00aa1-119">Especifique el número de campo en el archivo de texto.</span><span class="sxs-lookup"><span data-stu-id="00aa1-119">Specify the field number in the text file.</span></span>|  
    |<span data-ttu-id="00aa1-120">**Tipo de línea**</span><span class="sxs-lookup"><span data-stu-id="00aa1-120">**Line Type**</span></span>|<span data-ttu-id="00aa1-121">Especifique si el tipo de línea de la declaración del IVA es un elemento XML o un atributo XML.</span><span class="sxs-lookup"><span data-stu-id="00aa1-121">Specify whether the VAT statement line type is an XML element or an XML attribute.</span></span>|  
    |<span data-ttu-id="00aa1-122">**Nivel sangría**</span><span class="sxs-lookup"><span data-stu-id="00aa1-122">**Indentation Level**</span></span>|<span data-ttu-id="00aa1-123">Especifique el nivel de sangría de la etiqueta.</span><span class="sxs-lookup"><span data-stu-id="00aa1-123">Specify the indentation level for the label.</span></span> <span data-ttu-id="00aa1-124">Este nivel se utiliza para formatear el archivo XML.</span><span class="sxs-lookup"><span data-stu-id="00aa1-124">This level is used to format the XML file.</span></span>|  
    |<span data-ttu-id="00aa1-125">**Nº línea maestro**</span><span class="sxs-lookup"><span data-stu-id="00aa1-125">**Parent Line No.**</span></span>|<span data-ttu-id="00aa1-126">Especifique el número de línea de la línea principal con la que se sangra la línea actual.</span><span class="sxs-lookup"><span data-stu-id="00aa1-126">Specify the line number of the parent line that the current line is indented under.</span></span>|  
    |<span data-ttu-id="00aa1-127">**Tipo de valor**</span><span class="sxs-lookup"><span data-stu-id="00aa1-127">**Value Type**</span></span>|<span data-ttu-id="00aa1-128">Especifique el subtipo del campo.</span><span class="sxs-lookup"><span data-stu-id="00aa1-128">Specify the subtype of the field.</span></span><br /><br /> <span data-ttu-id="00aa1-129">El subtipo especifica si la línea debe mostrar solo la parte entera de un importe, la parte decimal, o el importe total.</span><span class="sxs-lookup"><span data-stu-id="00aa1-129">The subtype specifies if the line must show only the integer part of an amount, the decimal part, or the full amount.</span></span>|  
    |<span data-ttu-id="00aa1-130">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="00aa1-130">**Description**</span></span>|<span data-ttu-id="00aa1-131">Especifique el texto que desea que aparezca en la etiqueta.</span><span class="sxs-lookup"><span data-stu-id="00aa1-131">Specify the text that you want to appear on the label.</span></span>|  
    |<span data-ttu-id="00aa1-132">**Valor**</span><span class="sxs-lookup"><span data-stu-id="00aa1-132">**Value**</span></span>|<span data-ttu-id="00aa1-133">Especifique el valor de la etiqueta.</span><span class="sxs-lookup"><span data-stu-id="00aa1-133">Specify the value for the label.</span></span>|  
    |<span data-ttu-id="00aa1-134">**Caja**</span><span class="sxs-lookup"><span data-stu-id="00aa1-134">**Box**</span></span>|<span data-ttu-id="00aa1-135">Especifique el número de casilla desde donde recuperar los datos.</span><span class="sxs-lookup"><span data-stu-id="00aa1-135">Specify the box number from which to retrieve the data.</span></span>|  
    |<span data-ttu-id="00aa1-136">**Preguntar**</span><span class="sxs-lookup"><span data-stu-id="00aa1-136">**Ask**</span></span>|<span data-ttu-id="00aa1-137">Especifica si el campo **Valor** se puede modificar antes de crear el archivo XML.</span><span class="sxs-lookup"><span data-stu-id="00aa1-137">Specifies if the **Value** field can be changed before you create the XML file.</span></span>|  
    |<span data-ttu-id="00aa1-138">**Existe importe**</span><span class="sxs-lookup"><span data-stu-id="00aa1-138">**Exists Amount**</span></span>|<span data-ttu-id="00aa1-139">Seleccione esta opción para incluir el importe existente.</span><span class="sxs-lookup"><span data-stu-id="00aa1-139">Select to include the existing amount.</span></span>|  

4.  <span data-ttu-id="00aa1-140">Repita el paso anterior para las líneas adicionales en la declaración de IVA.</span><span class="sxs-lookup"><span data-stu-id="00aa1-140">Repeat the previous step for additional lines in the VAT statement.</span></span>  
5.  <span data-ttu-id="00aa1-141">Elija el botón **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="00aa1-141">Choose the **OK** button.</span></span>  

<span data-ttu-id="00aa1-142">Esta acción crea la plantilla.</span><span class="sxs-lookup"><span data-stu-id="00aa1-142">This creates the template.</span></span> <span data-ttu-id="00aa1-143">Ahora puede crear un archivo que luego puede enviar a las autoridades fiscales.</span><span class="sxs-lookup"><span data-stu-id="00aa1-143">Now, you can create a file that you can then submit to the tax authorities.</span></span>  

## <a name="see-also"></a><span data-ttu-id="00aa1-144">Consulte también</span><span class="sxs-lookup"><span data-stu-id="00aa1-144">See Also</span></span>  
 <span data-ttu-id="00aa1-145">[Exportar declaraciones de IVA en formato XML](how-to-export-vat-statements-in-xml-format.md) </span><span class="sxs-lookup"><span data-stu-id="00aa1-145">[Export VAT Statements in XML Format](how-to-export-vat-statements-in-xml-format.md) </span></span>  
 [<span data-ttu-id="00aa1-146">Crear plantillas para las declaraciones telemáticas de IVA en formato de archivo de texto</span><span class="sxs-lookup"><span data-stu-id="00aa1-146">Create Templates for Telematic VAT Statements in Text File Format</span></span>](how-to-create-templates-for-telematic-vat-statements-in-text-file-format.md)
