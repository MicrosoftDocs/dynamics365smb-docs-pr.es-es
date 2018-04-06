---
title: Exportar declaraciones de IVA en formato de texto
description: "Puede exportar una declaración de IVA en formato de texto y después enviarla electrónicamente a las autoridades fiscales."
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
ms.openlocfilehash: 23e3d00321ea181e24568bd72f1522ea1779b3c9
ms.contentlocale: es-es
ms.lasthandoff: 03/22/2018

---
# <a name="export-vat-statements-in-text-format"></a><span data-ttu-id="c34b3-103">Exportar declaraciones de IVA en formato de texto</span><span class="sxs-lookup"><span data-stu-id="c34b3-103">Export VAT Statements in Text Format</span></span>
<span data-ttu-id="c34b3-104">Puede exportar una declaración de IVA en formato de texto y después enviarla electrónicamente a las autoridades fiscales.</span><span class="sxs-lookup"><span data-stu-id="c34b3-104">You can export a VAT statement in text format and then submit it electronically to the tax authorities.</span></span>  

<span data-ttu-id="c34b3-105">Para obtener más información, consulte el sitio web de la [Agencia Tributaria](http://go.microsoft.com/fwlink/?LinkID=238181).</span><span class="sxs-lookup"><span data-stu-id="c34b3-105">For more information, see the [Spanish Tax Agency](http://go.microsoft.com/fwlink/?LinkID=238181) website.</span></span>  

## <a name="to-export-a-vat-statement-in-text-format"></a><span data-ttu-id="c34b3-106">Para exportar declaraciones de IVA en formato de texto</span><span class="sxs-lookup"><span data-stu-id="c34b3-106">To export a VAT statement in text format</span></span>  

1.  <span data-ttu-id="c34b3-107">Seleccione el icono ![Buscar página o informe](../../media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Declaraciones IVA** y, a continuación, seleccione el vínculo relacionado.</span><span class="sxs-lookup"><span data-stu-id="c34b3-107">Choose the ![Search for Page or Report](../../media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **VAT Statements**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="c34b3-108">Seleccione la declaración de IVA requerida y después seleccione **Generar archivo TXT**.</span><span class="sxs-lookup"><span data-stu-id="c34b3-108">Select the required VAT statement, and then choose the **Generate txt file** action.</span></span>  

    > [!IMPORTANT]  
    >  <span data-ttu-id="c34b3-109">El nombre de la declaración de IVA debe ser de tipo de plantilla **Informe 1 columna**.</span><span class="sxs-lookup"><span data-stu-id="c34b3-109">The VAT statement name must be of the template type **One Column Report**.</span></span>  
    >   
    >  <span data-ttu-id="c34b3-110">En la versión estándar de [!INCLUDE[d365fin](../../includes/d365fin_md.md)], el nombre de la declaración del IVA para la declaración telemática 320 es del tipo **Informe 1 columna**.</span><span class="sxs-lookup"><span data-stu-id="c34b3-110">In the standard version of [!INCLUDE[d365fin](../../includes/d365fin_md.md)], the VAT statement name for the 320 telematic statement is of the type **One Column Report**.</span></span>  

4.  <span data-ttu-id="c34b3-111">En la ficha desplegable **Opciones** de la ventana **Declaración telemática IVA**, rellene los campos tal y como se describe en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="c34b3-111">In the **Telematic VAT Declaration** window, on the **Options** FastTab, fill in the fields as described in the following table.</span></span>  

    |<span data-ttu-id="c34b3-112">Campo</span><span class="sxs-lookup"><span data-stu-id="c34b3-112">Field</span></span>|<span data-ttu-id="c34b3-113">Description</span><span class="sxs-lookup"><span data-stu-id="c34b3-113">Description</span></span>|  
    |---------------------------------|---------------------------------------|  
    |<span data-ttu-id="c34b3-114">**Movs. IVA incluidos**</span><span class="sxs-lookup"><span data-stu-id="c34b3-114">**VAT entries included**</span></span>|<span data-ttu-id="c34b3-115">Especifique si la declaración de IVA debe incluir los movimientos pendientes, los cerrados, o ambos.</span><span class="sxs-lookup"><span data-stu-id="c34b3-115">Specify if the VAT statement must include open entries, closed entries, or both open and closed entries.</span></span>|  
    |<span data-ttu-id="c34b3-116">**Movs. IVA incluidos**</span><span class="sxs-lookup"><span data-stu-id="c34b3-116">**VAT entries included**</span></span>|<span data-ttu-id="c34b3-117">Especifique si la declaración de IVA debe incluir únicamente los movimientos del periodo que se especifica en el campo **Filtro fecha** o también movimientos de periodos anteriores.</span><span class="sxs-lookup"><span data-stu-id="c34b3-117">Specify if the VAT statement must include only entries from the period that is specified in the **Date Filter** field, or also entries from previous periods.</span></span>|  
    |<span data-ttu-id="c34b3-118">**Divisa adicional**</span><span class="sxs-lookup"><span data-stu-id="c34b3-118">**Additional Currency**</span></span>|<span data-ttu-id="c34b3-119">Seleccione que se muestren los importes del informe en una divisa adicional de informe.</span><span class="sxs-lookup"><span data-stu-id="c34b3-119">Select to display the report amounts in the additional reporting currency.</span></span>|  

5.  <span data-ttu-id="c34b3-120">En la ficha desplegable **Lín. declaración IVA**, especifique un valor del campo **Filtro fecha**.</span><span class="sxs-lookup"><span data-stu-id="c34b3-120">On the **VAT Statement Line** FastTab, specify a value for the **Date Filter** field.</span></span>  

    <span data-ttu-id="c34b3-121">Opcionalmente, seleccione los filtros adicionales.</span><span class="sxs-lookup"><span data-stu-id="c34b3-121">Optionally, select additional filters.</span></span>  
6.  <span data-ttu-id="c34b3-122">Elija el botón **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="c34b3-122">Choose the **OK** button.</span></span>  
7.  <span data-ttu-id="c34b3-123">En la ventana **Formato de transferencia**, verifique que la declaración de IVA se configura correctamente y después seleccione el botón **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="c34b3-123">In the **Transference Format** window, verify that the VAT statement is set up as required, and then choose the **OK** button.</span></span>  
8.  <span data-ttu-id="c34b3-124">Seleccione el botón **Abrir** o **Guardar**.</span><span class="sxs-lookup"><span data-stu-id="c34b3-124">Choose the **Open** button or choose the **Save** button.</span></span>  

<span data-ttu-id="c34b3-125">Ahora puede enviar la declaración del IVA a las autoridades fiscales.</span><span class="sxs-lookup"><span data-stu-id="c34b3-125">You can now submit the VAT statement to the tax authorities.</span></span>  

## <a name="see-also"></a><span data-ttu-id="c34b3-126">Consulte también</span><span class="sxs-lookup"><span data-stu-id="c34b3-126">See Also</span></span>  
 <span data-ttu-id="c34b3-127">[Informes IVA](vat-reports.md) </span><span class="sxs-lookup"><span data-stu-id="c34b3-127">[VAT Reports](vat-reports.md) </span></span>  
 <span data-ttu-id="c34b3-128">[Crear plantillas para las declaraciones telemáticas de IVA en formato de archivo de texto](how-to-create-templates-for-telematic-vat-statements-in-text-file-format.md) </span><span class="sxs-lookup"><span data-stu-id="c34b3-128">[Create Templates for Telematic VAT Statements in Text File Format](how-to-create-templates-for-telematic-vat-statements-in-text-file-format.md) </span></span>  
 [<span data-ttu-id="c34b3-129">Exportar declaraciones de IVA en formato XML</span><span class="sxs-lookup"><span data-stu-id="c34b3-129">Export VAT Statements in XML Format</span></span>](how-to-export-vat-statements-in-xml-format.md)

