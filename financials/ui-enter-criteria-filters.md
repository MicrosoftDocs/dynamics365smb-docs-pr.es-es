---
title: "Definir criterios de búsqueda en filtros | Documentos de Microsoft"
description: "Describe cómo trabajar con filtros, como el filtro rápido, para redefinir los resultados que obtiene al buscar datos."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: delimit, FlowFilter
ms.date: 03/29/2017
ms.author: solsen
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 86ca45493081d9dbd229548f7c560e1df4e1c7c3
ms.contentlocale: es-es
ms.lasthandoff: 09/11/2017

---
# <a name="entering-criteria-in-filters"></a><span data-ttu-id="12010-103">Introducir criterios en los filtros</span><span class="sxs-lookup"><span data-stu-id="12010-103">Entering Criteria in Filters</span></span>
<span data-ttu-id="12010-104">Cuando quiera buscar datos, como nombres de cliente, direcciones o grupos de productos, puede introducir los criterios.</span><span class="sxs-lookup"><span data-stu-id="12010-104">When you want to search for data, such as customer names, addresses, or product groups, you enter criteria.</span></span> <span data-ttu-id="12010-105">En los criterios de búsqueda puede usar todos los números y las letras que normalmente se emplean en un campo específico.</span><span class="sxs-lookup"><span data-stu-id="12010-105">In search criteria you can use all the numbers and letters that you normally use in the specific field.</span></span> <span data-ttu-id="12010-106">También puede usar símbolos especiales o expresiones matemáticas para filtrar aún más los resultados.</span><span class="sxs-lookup"><span data-stu-id="12010-106">In addition, you can use special symbols to further filter the results.</span></span>

## <a name="searching-using-the-quick-filter"></a><span data-ttu-id="12010-107">Búsqueda mediante el filtro rápido</span><span class="sxs-lookup"><span data-stu-id="12010-107">Searching using the Quick Filter</span></span>
<span data-ttu-id="12010-108">Puede agregar filtros a todas las páginas con el filtro rápido.</span><span class="sxs-lookup"><span data-stu-id="12010-108">You can add filters to all pages by using the Quick Filter.</span></span> <span data-ttu-id="12010-109">El filtro rápido se activa al elegir el icono de la lupa que se encuentra en la esquina superior derecha de una página.</span><span class="sxs-lookup"><span data-stu-id="12010-109">The Quick Filter is enabled by choosing the magnifier icon in the top right corner of a page.</span></span> <span data-ttu-id="12010-110">Este tipo de filtro se utiliza para una rápida introducción de criterios.</span><span class="sxs-lookup"><span data-stu-id="12010-110">This filtering type is used for a fast entry of criteria.</span></span>

> [!IMPORTANT]  
>   <span data-ttu-id="12010-111">El acceso Filtro rápido proporciona un acceso sencillo a los datos de filtro mediante la especificación de texto normal, pero también proporciona muchas opciones de criterios de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="12010-111">The Quick Filter provides an easy access to filter data by entering plain text, but does also provide a lot of search criteria options.</span></span> <span data-ttu-id="12010-112">El filtro rápido actúa de distinta forma dependiendo de si introduce texto sin formato o texto con símbolos.</span><span class="sxs-lookup"><span data-stu-id="12010-112">Depending on whether you enter plain text or text including symbols, the Quick Filter behaves differently.</span></span>  

* <span data-ttu-id="12010-113">Si se introduce texto sin formato en los criterios de búsqueda, estos se interpretan como una búsqueda que tendrá en cuenta mayúsculas y minúsculas y que contendrá un determinado texto.</span><span class="sxs-lookup"><span data-stu-id="12010-113">If you enter plain text in the search criteria, the search criteria is interpreted as a case insensitive search that contains certain text.</span></span>  
* <span data-ttu-id="12010-114">Si se introduce texto con símbolos en los criterios de búsqueda, estos se interpretan exactamente como se haya introducido este texto y teniendo en cuenta mayúsculas y minúsculas.</span><span class="sxs-lookup"><span data-stu-id="12010-114">If you enter text including symbols in the search criteria, the search criteria is interpreted exactly as you entered it, and the search is case sensitive.</span></span>

### <a name="quick-filter-criteria"></a><span data-ttu-id="12010-115">Criterios del filtro rápido</span><span class="sxs-lookup"><span data-stu-id="12010-115">Quick filter criteria</span></span>
<!-- html syntax because symbols conflict with MarkDown syntax -->
<TABLE>
  <TR>
    <TH><span data-ttu-id="12010-116">Criterios de búsqueda</span><span class="sxs-lookup"><span data-stu-id="12010-116">Search Criteria</span></span></TH>
    <TH><span data-ttu-id="12010-117">Interpretado como…</span><span class="sxs-lookup"><span data-stu-id="12010-117">Interpreted as...</span></span></TH>
    <TH><span data-ttu-id="12010-118">Devoluciones...</span><span class="sxs-lookup"><span data-stu-id="12010-118">Returns...</span></span></TH>
  </TR>
  <TR>
    <TD><span data-ttu-id="12010-119">man</span><span class="sxs-lookup"><span data-stu-id="12010-119">man</span></span></TD>
    <TD><span data-ttu-id="12010-120">@&#42;man&#42;</span><span class="sxs-lookup"><span data-stu-id="12010-120">@&#42;man&#42;</span></span></TD>
    <TD><span data-ttu-id="12010-121">Todos los registros que contienen el texto <b>man</b> y respetando mayúsculas y minúsculas.</span><span class="sxs-lookup"><span data-stu-id="12010-121">All records that contain the text <b>man</b> and case insensitive.</span></span></TD>
  </TR>
  <TR>
    <TD><span data-ttu-id="12010-122">se</span><span class="sxs-lookup"><span data-stu-id="12010-122">se</span></span></TD>
    <TD><span data-ttu-id="12010-123">@&#42;se&#42;</span><span class="sxs-lookup"><span data-stu-id="12010-123">@&#42;se&#42;</span></span></TD>
    <TD><span data-ttu-id="12010-124">Todos los registros que contienen el texto <b>se</b> y respetando mayúsculas y minúsculas.</span><span class="sxs-lookup"><span data-stu-id="12010-124">All records that contain the text <b>se</b> and case insensitive.</span></span></TD>
  </TR>
  <TR>
    <TD><span data-ttu-id="12010-125">Man&#42;</span><span class="sxs-lookup"><span data-stu-id="12010-125">Man&#42;</span></span></TD>
    <TD><span data-ttu-id="12010-126">Empieza por <b>Man</b> y distingue mayúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="12010-126">Starts with <b>Man</b> and case sensitive.</span></span></TD>
    <TD><span data-ttu-id="12010-127">Todos los registros que empiecen por el texto <b>Man</b>.</span><span class="sxs-lookup"><span data-stu-id="12010-127">All records that start with the text <b>Man</b>.</span></span></TD>
  </TR>
  <TR>
    <TD><span data-ttu-id="12010-128">'man'</span><span class="sxs-lookup"><span data-stu-id="12010-128">'man'</span></span></TD>
    <TD><span data-ttu-id="12010-129">Un texto exacto respetando mayúsculas y minúsculas.</span><span class="sxs-lookup"><span data-stu-id="12010-129">An exact text and case sensitive.</span></span></TD>
    <TD><span data-ttu-id="12010-130">Todos los registros que coincidan exactamente con <b>man</b>.</span><span class="sxs-lookup"><span data-stu-id="12010-130">All records that match <b>man</b> exactly.</span></span></TD>
  </TR>
  <TR>
    <TD><span data-ttu-id="12010-131">@man*</span><span class="sxs-lookup"><span data-stu-id="12010-131">@man*</span></span> </TD>
    <TD><span data-ttu-id="12010-132">Empieza por y distingue mayúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="12010-132">Starts with and case insensitive.</span></span></TD>
    <TD><span data-ttu-id="12010-133">Todos los registros que empiecen por <b>man</b>.</span><span class="sxs-lookup"><span data-stu-id="12010-133">All records that start with <b>man</b>.</span></span></TD>
  </TR>
    <TR>
    <TD><span data-ttu-id="12010-134">@&#42;man</span><span class="sxs-lookup"><span data-stu-id="12010-134">@&#42;man</span></span></TD>
    <TD><span data-ttu-id="12010-135">Termina en y distingue mayúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="12010-135">Ends with and case insensitive.</span></span></TD>
    <TD><span data-ttu-id="12010-136">Todos los registros que terminen en <b>man</b>.</span><span class="sxs-lookup"><span data-stu-id="12010-136">All records that end with <b>man</b>.</span></span></TD>
  </TR>
</TABLE>

> [!NOTE]  
>   <span data-ttu-id="12010-137">No puede usar un carácter comodín al filtrar en los campos de enumeración, como el campo **Estado** en los pedidos de venta.</span><span class="sxs-lookup"><span data-stu-id="12010-137">You cannot use a wildcard when filtering on enumeration fields, such as the **Status** field on sales orders.</span></span> <span data-ttu-id="12010-138">Para especificar un filtro para este tipo de campo, puede especificar el valor numérico como parámetro de filtrado.</span><span class="sxs-lookup"><span data-stu-id="12010-138">To enter a filter for this type of field, you can enter the numeric value as a filtering parameter.</span></span> <span data-ttu-id="12010-139">Por ejemplo, en el campo **Estado** de un pedido de venta que tenga los valores **Abierto**, **Lanzado**, **Aprobación pendiente** y **Prepago pendiente**, utilice los valores **0**, **1**, **2** y **3** para filtrar para estas opciones.</span><span class="sxs-lookup"><span data-stu-id="12010-139">For example, in the **Status** field on a sales order that has the values **Open**, **Released**, **Pending Approval**, and **Pending Prepayment**, use the values **0**, **1**, **2**, and **3** to filter for these options.</span></span>  

## <a name="see-also"></a><span data-ttu-id="12010-140">Consulte también</span><span class="sxs-lookup"><span data-stu-id="12010-140">See Also</span></span>
<span data-ttu-id="12010-141">[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="12010-141">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

