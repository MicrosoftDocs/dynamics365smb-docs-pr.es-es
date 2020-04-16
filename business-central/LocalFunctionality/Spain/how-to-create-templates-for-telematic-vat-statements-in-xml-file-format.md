---
title: Crear plantillas para las declaraciones telemáticas de IVA en formato XML
description: Para mostrar las declaraciones de IVA electrónicamente, debe crear plantillas para generar los archivos necesarios. Puede enviar los archivos en formato de texto y en formato XML. Este procedimiento describe cómo crear plantillas para los archivos XML.
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
ms.openlocfilehash: c5d07288a8bfaffc48c569758f81f65a8cc2f793
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/01/2020
ms.locfileid: "3189189"
---
# <a name="create-templates-for-telematic-vat-statements-in-xml-file-format"></a><span data-ttu-id="43f7f-105">Crear plantillas para las declaraciones telemáticas de IVA en formato XML</span><span class="sxs-lookup"><span data-stu-id="43f7f-105">Create Templates for Telematic VAT Statements in XML File Format</span></span>
<span data-ttu-id="43f7f-106">Para mostrar las declaraciones de IVA electrónicamente, debe crear plantillas para generar los archivos necesarios.</span><span class="sxs-lookup"><span data-stu-id="43f7f-106">In order to submit VAT statements electronically, you must create templates to generate the required files.</span></span> <span data-ttu-id="43f7f-107">Puede enviar los archivos en formato de texto y en formato XML.</span><span class="sxs-lookup"><span data-stu-id="43f7f-107">You can submit files in text format and in XML format.</span></span> <span data-ttu-id="43f7f-108">Este procedimiento describe cómo crear plantillas para los archivos XML.</span><span class="sxs-lookup"><span data-stu-id="43f7f-108">This procedure describes how to create templates for XML files.</span></span>  

<span data-ttu-id="43f7f-109">Para obtener más información, consulte el sitio web de la [Agencia Tributaria](https://go.microsoft.com/fwlink/?LinkID=238181).</span><span class="sxs-lookup"><span data-stu-id="43f7f-109">For more information, see the [Spanish Tax Agency](https://go.microsoft.com/fwlink/?LinkID=238181) website.</span></span>  

## <a name="to-create-a-template-for-vat-statements-in-xml-file-format"></a><span data-ttu-id="43f7f-110">Para crear una plantilla para las declaraciones telemáticas de IVA en formato de archivo XML</span><span class="sxs-lookup"><span data-stu-id="43f7f-110">To create a template for VAT statements in XML file format</span></span>  

1.  <span data-ttu-id="43f7f-111">Seleccione el icono ![Buscar página o informe](../../media/ui-search/search_small.png "Icono Buscar página o informe"), introduzca **Declaración IVA** y, a continuación, seleccione el vínculo apropiado.</span><span class="sxs-lookup"><span data-stu-id="43f7f-111">Choose the ![Search for Page or Report](../../media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **VAT Statement**, and then choose the appropriate link.</span></span>  
2.  <span data-ttu-id="43f7f-112">Seleccione la declaración de IVA requerida y después seleccione **Diseñar archivo XML**.</span><span class="sxs-lookup"><span data-stu-id="43f7f-112">Select the required VAT statement, and then choose the **Design XML file** action.</span></span>  
3.  <span data-ttu-id="43f7f-113">En la página **Formato transferencia XML**, rellene los campos tal como se describe en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="43f7f-113">On the **XML Transference Format** page, fill in the fields as described in the following table.</span></span>  

    > [!IMPORTANT]  
    >  <span data-ttu-id="43f7f-114">Los valores de los campos están determinados por las autoridades fiscales.</span><span class="sxs-lookup"><span data-stu-id="43f7f-114">The values for the fields are determined by the tax authorities.</span></span>  
    >   
    >  <span data-ttu-id="43f7f-115">Para obtener más información, consulte el sitio web de la [Agencia Tributaria](https://go.microsoft.com/fwlink/?LinkID=238181).</span><span class="sxs-lookup"><span data-stu-id="43f7f-115">For more information, see the [Spanish Tax Agency](https://go.microsoft.com/fwlink/?LinkID=238181) website.</span></span>  

    |<span data-ttu-id="43f7f-116">Campo</span><span class="sxs-lookup"><span data-stu-id="43f7f-116">Field</span></span>|<span data-ttu-id="43f7f-117">Description</span><span class="sxs-lookup"><span data-stu-id="43f7f-117">Description</span></span>|  
    |---------------------------------|---------------------------------------|  
    |<span data-ttu-id="43f7f-118">**Nombre decl. IVA**</span><span class="sxs-lookup"><span data-stu-id="43f7f-118">**VAT Stmt. Name**</span></span>|<span data-ttu-id="43f7f-119">Especifique el nombre de la declaración del IVA para el que está diseñada esta plantilla.</span><span class="sxs-lookup"><span data-stu-id="43f7f-119">Specify the VAT statement name that this template is for.</span></span>|  
    |<span data-ttu-id="43f7f-120">**Nº**</span><span class="sxs-lookup"><span data-stu-id="43f7f-120">**No.**</span></span>|<span data-ttu-id="43f7f-121">Especifique el número de campo en el archivo de texto.</span><span class="sxs-lookup"><span data-stu-id="43f7f-121">Specify the field number in the text file.</span></span>|  
    |<span data-ttu-id="43f7f-122">**Tipo de línea**</span><span class="sxs-lookup"><span data-stu-id="43f7f-122">**Line Type**</span></span>|<span data-ttu-id="43f7f-123">Especifique si el tipo de línea de la declaración del IVA es un elemento XML o un atributo XML.</span><span class="sxs-lookup"><span data-stu-id="43f7f-123">Specify whether the VAT statement line type is an XML element or an XML attribute.</span></span>|  
    |<span data-ttu-id="43f7f-124">**Nivel sangría**</span><span class="sxs-lookup"><span data-stu-id="43f7f-124">**Indentation Level**</span></span>|<span data-ttu-id="43f7f-125">Especifique el nivel de sangría de la etiqueta.</span><span class="sxs-lookup"><span data-stu-id="43f7f-125">Specify the indentation level for the label.</span></span> <span data-ttu-id="43f7f-126">Este nivel se utiliza para formatear el archivo XML.</span><span class="sxs-lookup"><span data-stu-id="43f7f-126">This level is used to format the XML file.</span></span>|  
    |<span data-ttu-id="43f7f-127">**Nº línea maestro**</span><span class="sxs-lookup"><span data-stu-id="43f7f-127">**Parent Line No.**</span></span>|<span data-ttu-id="43f7f-128">Especifique el número de línea de la línea principal con la que se sangra la línea actual.</span><span class="sxs-lookup"><span data-stu-id="43f7f-128">Specify the line number of the parent line that the current line is indented under.</span></span>|  
    |<span data-ttu-id="43f7f-129">**Tipo de valor**</span><span class="sxs-lookup"><span data-stu-id="43f7f-129">**Value Type**</span></span>|<span data-ttu-id="43f7f-130">Especifique el subtipo del campo.</span><span class="sxs-lookup"><span data-stu-id="43f7f-130">Specify the subtype of the field.</span></span><br /><br /> <span data-ttu-id="43f7f-131">El subtipo especifica si la línea debe mostrar solo la parte entera de un importe, la parte decimal, o el importe total.</span><span class="sxs-lookup"><span data-stu-id="43f7f-131">The subtype specifies if the line must show only the integer part of an amount, the decimal part, or the full amount.</span></span>|  
    |<span data-ttu-id="43f7f-132">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="43f7f-132">**Description**</span></span>|<span data-ttu-id="43f7f-133">Especifique el texto que desea que aparezca en la etiqueta.</span><span class="sxs-lookup"><span data-stu-id="43f7f-133">Specify the text that you want to appear on the label.</span></span>|  
    |<span data-ttu-id="43f7f-134">**Valor**</span><span class="sxs-lookup"><span data-stu-id="43f7f-134">**Value**</span></span>|<span data-ttu-id="43f7f-135">Especifique el valor de la etiqueta.</span><span class="sxs-lookup"><span data-stu-id="43f7f-135">Specify the value for the label.</span></span>|  
    |<span data-ttu-id="43f7f-136">**Caja**</span><span class="sxs-lookup"><span data-stu-id="43f7f-136">**Box**</span></span>|<span data-ttu-id="43f7f-137">Especifique el número de casilla desde donde recuperar los datos.</span><span class="sxs-lookup"><span data-stu-id="43f7f-137">Specify the box number from which to retrieve the data.</span></span>|  
    |<span data-ttu-id="43f7f-138">**Preguntar**</span><span class="sxs-lookup"><span data-stu-id="43f7f-138">**Ask**</span></span>|<span data-ttu-id="43f7f-139">Especifica si el campo **Valor** se puede modificar antes de crear el archivo XML.</span><span class="sxs-lookup"><span data-stu-id="43f7f-139">Specifies if the **Value** field can be changed before you create the XML file.</span></span>|  
    |<span data-ttu-id="43f7f-140">**Existe importe**</span><span class="sxs-lookup"><span data-stu-id="43f7f-140">**Exists Amount**</span></span>|<span data-ttu-id="43f7f-141">Seleccione esta opción para incluir el importe existente.</span><span class="sxs-lookup"><span data-stu-id="43f7f-141">Select to include the existing amount.</span></span>|  

4.  <span data-ttu-id="43f7f-142">Repita el paso anterior para las líneas adicionales en la declaración de IVA.</span><span class="sxs-lookup"><span data-stu-id="43f7f-142">Repeat the previous step for additional lines in the VAT statement.</span></span>  
5.  <span data-ttu-id="43f7f-143">Elija el botón **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="43f7f-143">Choose the **OK** button.</span></span>  

<span data-ttu-id="43f7f-144">Esta acción crea la plantilla.</span><span class="sxs-lookup"><span data-stu-id="43f7f-144">This creates the template.</span></span> <span data-ttu-id="43f7f-145">Ahora puede crear un archivo que luego puede enviar a las autoridades fiscales.</span><span class="sxs-lookup"><span data-stu-id="43f7f-145">Now, you can create a file that you can then submit to the tax authorities.</span></span>  

## <a name="see-also"></a><span data-ttu-id="43f7f-146">Consulte también</span><span class="sxs-lookup"><span data-stu-id="43f7f-146">See Also</span></span>  
 <span data-ttu-id="43f7f-147">[Exportar declaraciones de IVA en formato XML](how-to-export-vat-statements-in-xml-format.md) </span><span class="sxs-lookup"><span data-stu-id="43f7f-147">[Export VAT Statements in XML Format](how-to-export-vat-statements-in-xml-format.md) </span></span>  
 [<span data-ttu-id="43f7f-148">Crear plantillas para las declaraciones telemáticas de IVA en formato de archivo de texto</span><span class="sxs-lookup"><span data-stu-id="43f7f-148">Create Templates for Telematic VAT Statements in Text File Format</span></span>](how-to-create-templates-for-telematic-vat-statements-in-text-file-format.md)
