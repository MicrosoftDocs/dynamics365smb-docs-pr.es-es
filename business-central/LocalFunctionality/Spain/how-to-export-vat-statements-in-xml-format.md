---
title: Exportar declaraciones de IVA en formato XML
description: Puede exportar una declaración de IVA en formato XML y después enviarla electrónicamente a las autoridades fiscales.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2018
ms.author: sgroespe
ms.openlocfilehash: 046563cae01c4ecf016ddc4f89bbb3d4a5d4def1
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 03/08/2019
ms.locfileid: "827131"
---
# <a name="export-vat-statements-in-xml-format"></a><span data-ttu-id="8c465-103">Exportar declaraciones de IVA en formato XML</span><span class="sxs-lookup"><span data-stu-id="8c465-103">Export VAT Statements in XML Format</span></span>
<span data-ttu-id="8c465-104">Puede exportar una declaración de IVA en formato XML y después enviarla electrónicamente a las autoridades fiscales.</span><span class="sxs-lookup"><span data-stu-id="8c465-104">You can export a VAT statement in XML format and then submit it electronically to the tax authorities.</span></span>  

<span data-ttu-id="8c465-105">Para obtener más información, consulte el sitio web de la [Agencia Tributaria](https://go.microsoft.com/fwlink/?LinkID=238181).</span><span class="sxs-lookup"><span data-stu-id="8c465-105">For more information, see the [Spanish Tax Agency](https://go.microsoft.com/fwlink/?LinkID=238181) website.</span></span>  

## <a name="to-export-a-vat-statement-in-xml-format"></a><span data-ttu-id="8c465-106">Para exportar declaraciones de IVA en formato XML</span><span class="sxs-lookup"><span data-stu-id="8c465-106">To export a VAT statement in XML format</span></span>  

1.  <span data-ttu-id="8c465-107">Seleccione el icono ![Buscar página o informe](../../media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Declaración del IVA** y, a continuación, seleccione el vínculo apropiado.</span><span class="sxs-lookup"><span data-stu-id="8c465-107">Choose the ![Search for Page or Report](../../media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **VAT Statement**, and then choose the appropriate link.</span></span>  
2.  <span data-ttu-id="8c465-108">Seleccione la declaración de IVA requerida y después seleccione **Generar archivo XML**.</span><span class="sxs-lookup"><span data-stu-id="8c465-108">Select the required VAT statement, and then choose the **Generate XML file** action.</span></span>  

    > [!IMPORTANT]  
    >  <span data-ttu-id="8c465-109">El nombre de la declaración de IVA debe ser de tipo de plantilla **Informe 1 columna**.</span><span class="sxs-lookup"><span data-stu-id="8c465-109">The VAT statement name must be of the template type **One Column Report**.</span></span>  
    >   
    >  <span data-ttu-id="8c465-110">En la versión estándar de [!INCLUDE[d365fin](../../includes/d365fin_md.md)], el nombre de la declaración del IVA para la declaración telemática 392 es del tipo **Informe 1 columna**.</span><span class="sxs-lookup"><span data-stu-id="8c465-110">In the standard version of [!INCLUDE[d365fin](../../includes/d365fin_md.md)], the VAT statement name for the 392 telematic statement is of the type **One Column Report**.</span></span>  

3.  <span data-ttu-id="8c465-111">En la ficha desplegable **Declaración IVA en XML** de la página **Opciones**, rellene los campos tal y como se describe en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="8c465-111">On the **XML VAT Declaration** page, on the **Options** FastTab, fill in the fields as described in the following table.</span></span>  
  
    |<span data-ttu-id="8c465-112">Campo</span><span class="sxs-lookup"><span data-stu-id="8c465-112">Field</span></span>|<span data-ttu-id="8c465-113">Description</span><span class="sxs-lookup"><span data-stu-id="8c465-113">Description</span></span>|  
    |---------------------------------|---------------------------------------|  
    |<span data-ttu-id="8c465-114">**Movs. IVA incluidos**</span><span class="sxs-lookup"><span data-stu-id="8c465-114">**VAT entries included**</span></span>|<span data-ttu-id="8c465-115">Especifique si la declaración de IVA debe incluir los movimientos pendientes, los cerrados, o ambos.</span><span class="sxs-lookup"><span data-stu-id="8c465-115">Specify if the VAT statement must include open entries, closed entries, or both open and closed entries.</span></span>|  
    |<span data-ttu-id="8c465-116">**Movs. IVA incluidos**</span><span class="sxs-lookup"><span data-stu-id="8c465-116">**VAT entries included**</span></span>|<span data-ttu-id="8c465-117">Especifique si la declaración de IVA debe incluir únicamente los movimientos del periodo que se especifica en el campo **Filtro fecha** o también movimientos de periodos anteriores.</span><span class="sxs-lookup"><span data-stu-id="8c465-117">Specify if the VAT statement must include only entries from the period that is specified in the **Date Filter** field, or also entries from previous periods.</span></span>|  
    |<span data-ttu-id="8c465-118">**Divisa adicional**</span><span class="sxs-lookup"><span data-stu-id="8c465-118">**Additional Currency**</span></span>|<span data-ttu-id="8c465-119">Seleccione que se muestren los importes del informe en una divisa adicional de informe.</span><span class="sxs-lookup"><span data-stu-id="8c465-119">Select to display the report amounts in the additional reporting currency.</span></span>|  

4.  <span data-ttu-id="8c465-120">En la ficha desplegable **Lín. declaración IVA**, especifique un valor del campo **Filtro fecha**.</span><span class="sxs-lookup"><span data-stu-id="8c465-120">On the **VAT Statement Line** FastTab, specify a value for the **Date Filter** field.</span></span>  

    <span data-ttu-id="8c465-121">Opcionalmente, seleccione los filtros adicionales.</span><span class="sxs-lookup"><span data-stu-id="8c465-121">Optionally, select additional filters.</span></span>  
5.  <span data-ttu-id="8c465-122">Elija el botón **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="8c465-122">Choose the **OK** button.</span></span>  
6.  <span data-ttu-id="8c465-123">En la página **Formato de transferencia XML**, verifique que la declaración de IVA se configura correctamente y después seleccione el botón **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="8c465-123">On the **XML Transference Format** page, verify that the VAT statement is set up as required, and then choose the **OK** button.</span></span>  

<span data-ttu-id="8c465-124">Puede abrir o guardar el archivo XML generado.</span><span class="sxs-lookup"><span data-stu-id="8c465-124">You can open or save the generated XML file.</span></span> <span data-ttu-id="8c465-125">Ahora puede enviar la declaración del IVA a las autoridades fiscales.</span><span class="sxs-lookup"><span data-stu-id="8c465-125">You can now submit the VAT statement to the tax authorities.</span></span>  

## <a name="see-also"></a><span data-ttu-id="8c465-126">Consulte también</span><span class="sxs-lookup"><span data-stu-id="8c465-126">See Also</span></span>  
 <span data-ttu-id="8c465-127">[Crear plantillas para las declaraciones telemáticas de IVA en formato XML](how-to-create-templates-for-telematic-vat-statements-in-xml-file-format.md) </span><span class="sxs-lookup"><span data-stu-id="8c465-127">[Create Templates for Telematic VAT Statements in XML File Format](how-to-create-templates-for-telematic-vat-statements-in-xml-file-format.md) </span></span>  
 [<span data-ttu-id="8c465-128">Exportar declaraciones de IVA en formato de texto</span><span class="sxs-lookup"><span data-stu-id="8c465-128">Export VAT Statements in Text Format</span></span>](how-to-export-vat-statements-in-text-format.md)
