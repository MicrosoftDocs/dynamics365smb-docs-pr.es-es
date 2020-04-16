---
title: Características de asistencia.
description: Métodos abreviados de teclado y otras características de asistencia.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: 1098e0998369e15bd9484ba33b808b9b435b538c
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/01/2020
ms.locfileid: "3192128"
---
# <a name="accessibility-and-keyboard-shortcuts"></a><span data-ttu-id="753aa-103">Accesibilidad y métodos abreviados de teclado</span><span class="sxs-lookup"><span data-stu-id="753aa-103">Accessibility and Keyboard Shortcuts</span></span>
<span data-ttu-id="753aa-104">Este tema proporciona información acerca de las características que permiten que [!INCLUDE[d365fin](includes/d365fin_md.md)] esté disponible para personas con discapacidades.</span><span class="sxs-lookup"><span data-stu-id="753aa-104">This topic provides information about the features that make [!INCLUDE[d365fin](includes/d365fin_md.md)] readily available to people with disabilities.</span></span> [!INCLUDE[d365fin](includes/d365fin_md.md)] <span data-ttu-id="753aa-105">admite las características de accesibilidad siguientes:</span><span class="sxs-lookup"><span data-stu-id="753aa-105">supports the following accessibility features:</span></span>  

-   <span data-ttu-id="753aa-106">Métodos abreviados</span><span class="sxs-lookup"><span data-stu-id="753aa-106">Keyboard shortcuts</span></span>

    <span data-ttu-id="753aa-107">Para obtener más información, consulte [Métodos abreviados de teclado](keyboard-shortcuts.md)</span><span class="sxs-lookup"><span data-stu-id="753aa-107">For more information, see [Keyboard Shortcuts](keyboard-shortcuts.md)</span></span>

-   <span data-ttu-id="753aa-108">Navegación</span><span class="sxs-lookup"><span data-stu-id="753aa-108">Navigation</span></span>  

-   <span data-ttu-id="753aa-109">Encabezados</span><span class="sxs-lookup"><span data-stu-id="753aa-109">Headings</span></span>  

-   <span data-ttu-id="753aa-110">Texto alternativo para imágenes y vínculos</span><span class="sxs-lookup"><span data-stu-id="753aa-110">Alternative text for images and links</span></span>  

-   <span data-ttu-id="753aa-111">Compatibilidad con tecnologías de asistencia comunes</span><span class="sxs-lookup"><span data-stu-id="753aa-111">Support for common assistive technologies</span></span>  

<!-- moved to separate article
##  <a name="Keyboard"></a> Keyboard Shortcuts in the browser
 [!INCLUDE[d365fin](includes/d365fin_md.md)] supports the keyboard shortcuts that are supported by most web browsers. The keyboard shortcuts described here refer to the U.S. keyboard layout. The layout of the keys on other keyboards may not correspond exactly to the keys on a U.S. keyboard.  

|To do this|Press|  
|----------------|-----------|  
|To move focus to the next or previous control or element on a page, such as buttons, fields, or items in a list.|Tab, Shift+Tab|  
|To enable or access the element or control that is in focus.|Enter|  
|To scroll items up and down in a list.|Up Arrow, Down Arrow|  
|To scroll columns of an item left and right in a list.|Left Arrow, Right Arrow|  
|To open a drop-down list or look up a value for a field.|Alt+Down Arrow|  
|To move focus to the next element outside the list.|Ctrl + Enter|  
|To see the transactions that resulted in a calculated value in a field.|Alt+Right Arrow|  

-->

##  <a name="navigation"></a><a name="Navigation"></a> <span data-ttu-id="753aa-112">Navegación</span><span class="sxs-lookup"><span data-stu-id="753aa-112">Navigation</span></span>  
 <span data-ttu-id="753aa-113">Puede navegar entre las pestañas y las acciones en la cinta, elementos de la barra de navegación y otros controla en las páginas y los informes de [!INCLUDE[d365fin](includes/d365fin_md.md)] usando el teclado.</span><span class="sxs-lookup"><span data-stu-id="753aa-113">You can navigate between the tabs and actions in the ribbon, elements in the navigation bar, and other controls on [!INCLUDE[d365fin](includes/d365fin_md.md)] pages and reports using the keyboard.</span></span> <span data-ttu-id="753aa-114">Para mover el enfoque de una pestaña, acción o control a otro, pulse la tecla Tab para desplazarse hacia delante.</span><span class="sxs-lookup"><span data-stu-id="753aa-114">To move the focus from one tab, action, or control to another, press the Tab key to move forward.</span></span> <span data-ttu-id="753aa-115">Pulse Mayús+Tab para mover hacia atrás.</span><span class="sxs-lookup"><span data-stu-id="753aa-115">Press Shift+Tab to move backward.</span></span>  

 <span data-ttu-id="753aa-116">Con el orden tabulación, también puede cambiar entre la página principal del explorador y los cuadros de diálogo que solicitan confirmación, por ejemplo, o la página de inicio de sesión.</span><span class="sxs-lookup"><span data-stu-id="753aa-116">By using the tab order, you can also switch between the main browser page and dialog boxes that request confirmation, for example, or the login page.</span></span>  

##  <a name="headings"></a><a name="Headings"></a> <span data-ttu-id="753aa-117">Encabezados</span><span class="sxs-lookup"><span data-stu-id="753aa-117">Headings</span></span>  
 <span data-ttu-id="753aa-118">El código fuente HTML para el contenido de [!INCLUDE[d365fin](includes/d365fin_md.md)] utiliza etiquetas para ayudar a los usuarios de tecnología de asistencia a comprender la estructura y el contenido de la página.</span><span class="sxs-lookup"><span data-stu-id="753aa-118">The HTML source for [!INCLUDE[d365fin](includes/d365fin_md.md)] content uses tags to help users of assistive technology to understand the structure and content of the page.</span></span> <span data-ttu-id="753aa-119">Por ejemplo, en las páginas de lista, las columnas se definen en las etiquetas TH y los encabezados de columna se establecen con el atributo TITLE dentro de la etiqueta.</span><span class="sxs-lookup"><span data-stu-id="753aa-119">For example, on list pages, the columns are defined in TH tags and the column headings are set with TITLE attribute inside the tag.</span></span> <span data-ttu-id="753aa-120">Los títulos de los elementos, como fichas desplegables, cuadros informativos y campos, se incluyen en las etiquetas de título (H1, H2, H3 y H4).</span><span class="sxs-lookup"><span data-stu-id="753aa-120">Captions for elements, such as FastTabs, FactBoxes, and fields are included in heading tags (H1, H2, H3, and H4).</span></span>  

##  <a name="image-and-links"></a><a name="Images"></a> <span data-ttu-id="753aa-121">Imagen y vínculos</span><span class="sxs-lookup"><span data-stu-id="753aa-121">Image and Links</span></span>  
 <span data-ttu-id="753aa-122">Un texto descriptivo para las imágenes se establece con el atributo ALT dentro de la etiqueta IMG.</span><span class="sxs-lookup"><span data-stu-id="753aa-122">A descriptive text for images is set with the ALT attribute inside the IMG tag.</span></span> <span data-ttu-id="753aa-123">Un texto descriptivo para los hipervínculos se establece con el atributo title dentro de la etiqueta A.</span><span class="sxs-lookup"><span data-stu-id="753aa-123">A descriptive text for hyperlinks is set with the title attribute inside the A tag.</span></span>  

##  <a name="assistive-technologies"></a><a name="AssistiveTech"></a> <span data-ttu-id="753aa-124">Tecnologías de asistencia</span><span class="sxs-lookup"><span data-stu-id="753aa-124">Assistive Technologies</span></span>  
[!INCLUDE[d365fin](includes/d365fin_md.md)] <span data-ttu-id="753aa-125">admite las diversas tecnologías de asistencia, como contraste alto, lectores de pantalla y software de reconocimiento de voz.</span><span class="sxs-lookup"><span data-stu-id="753aa-125">supports various assistive technologies, such as high contrast, screen readers, and voice recognition software.</span></span> <span data-ttu-id="753aa-126">Es posible que algunas tecnologías de asistencia no funcionen bien con determinados elementos de las páginas de [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="753aa-126">Some assistive technologies may not work well with certain elements in [!INCLUDE[d365fin](includes/d365fin_md.md)] pages.</span></span>  

## <a name="for-more-accessibility-information"></a><span data-ttu-id="753aa-127">Para obtener más información sobre la accesibilidad</span><span class="sxs-lookup"><span data-stu-id="753aa-127">For more accessibility information</span></span>  
<span data-ttu-id="753aa-128">Puede encontrar información adicional acerca de la accesibilidad con los productos de Microsoft y las tecnologías de asistencia en el sitio [Accesibilidad de Microsoft](https://go.microsoft.com/fwlink/?LinkId=262160).</span><span class="sxs-lookup"><span data-stu-id="753aa-128">You can find additional information about accessibility with Microsoft products and assistive technologies on the [Microsoft Accessibility](https://go.microsoft.com/fwlink/?LinkId=262160) site.</span></span>

## <a name="see-also"></a><span data-ttu-id="753aa-129">Consulte también</span><span class="sxs-lookup"><span data-stu-id="753aa-129">See Also</span></span>
[<span data-ttu-id="753aa-130">Introducción</span><span class="sxs-lookup"><span data-stu-id="753aa-130">Getting Started</span></span>](product-get-started.md)  
<span data-ttu-id="753aa-131">[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="753aa-131">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="753aa-132">Preguntas más frecuentes</span><span class="sxs-lookup"><span data-stu-id="753aa-132">Frequently Asked Questions</span></span>](across-faq.md)  
