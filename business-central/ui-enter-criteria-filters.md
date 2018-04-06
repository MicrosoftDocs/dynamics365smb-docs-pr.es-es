---
title: Buscar datos y especificar criterios de filtrado | Documentos de Microsoft
description: "Describe cómo trabajar con filtros, como el filtro rápido, para redefinir los resultados que obtiene al buscar datos."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: delimit, FlowFilter
ms.date: 03/29/2017
ms.author: solsen
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: a7fd74ad235e51b1793b02e19834bdb0bd17820b
ms.contentlocale: es-es
ms.lasthandoff: 03/22/2018

---
# <a name="searching-filtering-and-sorting-data"></a><span data-ttu-id="a66c4-103">Buscar, filtrar y ordenar datos</span><span class="sxs-lookup"><span data-stu-id="a66c4-103">Searching, Filtering, and Sorting Data</span></span>
<span data-ttu-id="a66c4-104">Existen algunos parámetros que puede hacer que le ayudarán a encontrar, identificar y a buscar los registros de una lista.</span><span class="sxs-lookup"><span data-stu-id="a66c4-104">There are a few things that you can do that will help you find, pinpoint, and scan records in a list.</span></span> <span data-ttu-id="a66c4-105">Éstos incluyen la ordenación, busqueda y filtrando.</span><span class="sxs-lookup"><span data-stu-id="a66c4-105">These include sorting, searching and filtering.</span></span>

<span data-ttu-id="a66c4-106">Cuando quiera buscar datos, como nombres de cliente, direcciones o grupos de productos, puede introducir los criterios.</span><span class="sxs-lookup"><span data-stu-id="a66c4-106">When you want to search for data, such as customer names, addresses, or product groups, you enter criteria.</span></span> <span data-ttu-id="a66c4-107">En los criterios de búsqueda puede usar todos los números y las letras que normalmente se emplean en un campo específico.</span><span class="sxs-lookup"><span data-stu-id="a66c4-107">In search criteria you can use all the numbers and letters that you normally use in the specific field.</span></span> <span data-ttu-id="a66c4-108">También puede usar símbolos especiales para filtrar aún más los resultados.</span><span class="sxs-lookup"><span data-stu-id="a66c4-108">In addition, you can use special symbols to further filter the results.</span></span> <span data-ttu-id="a66c4-109">Existen dos formas de buscar: usando filtros rápidos o filtros de columna.</span><span class="sxs-lookup"><span data-stu-id="a66c4-109">There are two ways to search: using the Quick Filter or column filters.</span></span>

## <a name="sorting"></a><span data-ttu-id="a66c4-110">Ordenación</span><span class="sxs-lookup"><span data-stu-id="a66c4-110">Sorting</span></span>
<span data-ttu-id="a66c4-111">La ordenación facilita la obtención rápida de un resumen de sus datos.</span><span class="sxs-lookup"><span data-stu-id="a66c4-111">Sorting makes it easy for you to get a quick overview of your data.</span></span> <span data-ttu-id="a66c4-112">Si hay varios clientes, por ejemplo, puede elegir ordenarlos por **N.º de cliente**, **Grupo contable cliente**, **Cód. divisa**, **Cód. país/región** o **N.º de registro de impuesto sobre las ventas** para disponer de la vista general que desea.</span><span class="sxs-lookup"><span data-stu-id="a66c4-112">If you have many customers, for example, you can choose to sort them by **Customer No.**, **Customer Posting Group**, **Currency Code**, **Country Region Code**, or **Sales Tax Registration No.** to get the overview you need.</span></span>

<span data-ttu-id="a66c4-113">Para ordenar una lista, puede elegir o un texto de cabecera de columna para alternar entre la el pedido decreciente y ascendente o elegir la pequeña flecha hacia abajo de la cabecera de columna y, a continuación elegir **Ascendente** o **Descendente**.</span><span class="sxs-lookup"><span data-stu-id="a66c4-113">To sort a list, you can either choose a column heading text to toggle between ascending and descending order, or choose the small downs arrow in the column heading, and then choose **Ascending** or **Descending**.</span></span>  

> [!NOTE]  
>   <span data-ttu-id="a66c4-114">La ordenación no se admite en imágenes, campos BLOB, FlowFilters ni campos que no pertenezcan a una tabla.</span><span class="sxs-lookup"><span data-stu-id="a66c4-114">Sorting is not supported images, BLOB fields, FlowFilters, and fields that do not belong to a table.</span></span>  

## <a name="searching-by-using-the-quick-filter"></a><span data-ttu-id="a66c4-115">Búsqueda mediante el filtro rápido</span><span class="sxs-lookup"><span data-stu-id="a66c4-115">Searching by using the Quick Filter</span></span>
<span data-ttu-id="a66c4-116">Puede agregar filtros a todas las páginas con el filtro rápido.</span><span class="sxs-lookup"><span data-stu-id="a66c4-116">You can add filters to all pages by using the Quick Filter.</span></span> <span data-ttu-id="a66c4-117">El filtro rápido se activa al elegir el icono de la lupa que se encuentra en la esquina superior derecha de una página.</span><span class="sxs-lookup"><span data-stu-id="a66c4-117">The Quick Filter is enabled by choosing the magnifier icon in the top right corner of a page.</span></span> <span data-ttu-id="a66c4-118">Este tipo de filtro se utiliza para una rápida introducción de criterios.</span><span class="sxs-lookup"><span data-stu-id="a66c4-118">This filtering type is used for a fast entry of criteria.</span></span>

> [!IMPORTANT]  
>   <span data-ttu-id="a66c4-119">El acceso Filtro rápido proporciona un acceso sencillo a los datos de filtro mediante la especificación de texto normal, pero también proporciona muchas opciones de criterios de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="a66c4-119">The Quick Filter provides an easy access to filter data by entering plain text, but does also provide a lot of search criteria options.</span></span> <span data-ttu-id="a66c4-120">El filtro rápido actúa de distinta forma dependiendo de si introduce texto sin formato o texto con símbolos.</span><span class="sxs-lookup"><span data-stu-id="a66c4-120">Depending on whether you enter plain text or text including symbols, the Quick Filter behaves differently.</span></span>  

* <span data-ttu-id="a66c4-121">Si se introduce texto sin formato en los criterios de búsqueda, estos se interpretan como una búsqueda que tendrá en cuenta mayúsculas y minúsculas y que contendrá un determinado texto.</span><span class="sxs-lookup"><span data-stu-id="a66c4-121">If you enter plain text in the search criteria, the search criteria is interpreted as a case insensitive search that contains certain text.</span></span>  
* <span data-ttu-id="a66c4-122">Si se introduce texto con símbolos en los criterios de búsqueda, estos se interpretan exactamente como se haya introducido este texto y teniendo en cuenta mayúsculas y minúsculas.</span><span class="sxs-lookup"><span data-stu-id="a66c4-122">If you enter text including symbols in the search criteria, the search criteria is interpreted exactly as you entered it, and the search is case sensitive.</span></span>

### <a name="quick-filter-criteria"></a><span data-ttu-id="a66c4-123">Criterios del filtro rápido</span><span class="sxs-lookup"><span data-stu-id="a66c4-123">Quick filter criteria</span></span>
<!-- html syntax because symbols conflict with MarkDown syntax -->
<TABLE>
  <TR>
    <TH><span data-ttu-id="a66c4-124">Criterios de búsqueda</span><span class="sxs-lookup"><span data-stu-id="a66c4-124">Search Criteria</span></span></TH>
    <TH><span data-ttu-id="a66c4-125">Interpretado como…</span><span class="sxs-lookup"><span data-stu-id="a66c4-125">Interpreted as...</span></span></TH>
    <TH><span data-ttu-id="a66c4-126">Devoluciones...</span><span class="sxs-lookup"><span data-stu-id="a66c4-126">Returns...</span></span></TH>
  </TR>
  <TR>
    <TD><span data-ttu-id="a66c4-127">man</span><span class="sxs-lookup"><span data-stu-id="a66c4-127">man</span></span></TD>
    <TD><span data-ttu-id="a66c4-128">@&#42;man&#42;</span><span class="sxs-lookup"><span data-stu-id="a66c4-128">@&#42;man&#42;</span></span></TD>
    <TD><span data-ttu-id="a66c4-129">Todos los registros que contienen el texto <b>man</b> y respetando mayúsculas y minúsculas.</span><span class="sxs-lookup"><span data-stu-id="a66c4-129">All records that contain the text <b>man</b> and case insensitive.</span></span></TD>
  </TR>
  <TR>
    <TD><span data-ttu-id="a66c4-130">se</span><span class="sxs-lookup"><span data-stu-id="a66c4-130">se</span></span></TD>
    <TD><span data-ttu-id="a66c4-131">@&#42;se&#42;</span><span class="sxs-lookup"><span data-stu-id="a66c4-131">@&#42;se&#42;</span></span></TD>
    <TD><span data-ttu-id="a66c4-132">Todos los registros que contienen el texto <b>se</b> y respetando mayúsculas y minúsculas.</span><span class="sxs-lookup"><span data-stu-id="a66c4-132">All records that contain the text <b>se</b> and case insensitive.</span></span></TD>
  </TR>
  <TR>
    <TD><span data-ttu-id="a66c4-133">Man&#42;</span><span class="sxs-lookup"><span data-stu-id="a66c4-133">Man&#42;</span></span></TD>
    <TD><span data-ttu-id="a66c4-134">Empieza por <b>Man</b> y distingue mayúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="a66c4-134">Starts with <b>Man</b> and case sensitive.</span></span></TD>
    <TD><span data-ttu-id="a66c4-135">Todos los registros que empiecen por el texto <b>Man</b>.</span><span class="sxs-lookup"><span data-stu-id="a66c4-135">All records that start with the text <b>Man</b>.</span></span></TD>
  </TR>
  <TR>
    <TD><span data-ttu-id="a66c4-136">'man'</span><span class="sxs-lookup"><span data-stu-id="a66c4-136">'man'</span></span></TD>
    <TD><span data-ttu-id="a66c4-137">Un texto exacto respetando mayúsculas y minúsculas.</span><span class="sxs-lookup"><span data-stu-id="a66c4-137">An exact text and case sensitive.</span></span></TD>
    <TD><span data-ttu-id="a66c4-138">Todos los registros que coincidan exactamente con <b>man</b>.</span><span class="sxs-lookup"><span data-stu-id="a66c4-138">All records that match <b>man</b> exactly.</span></span></TD>
  </TR>
  <TR>
    <TD><span data-ttu-id="a66c4-139">@man\*</span><span class="sxs-lookup"><span data-stu-id="a66c4-139">@man\*</span></span> </TD>
    <TD><span data-ttu-id="a66c4-140">Empieza por y distingue mayúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="a66c4-140">Starts with and case insensitive.</span></span></TD>
    <TD><span data-ttu-id="a66c4-141">Todos los registros que empiecen por <b>man</b>.</span><span class="sxs-lookup"><span data-stu-id="a66c4-141">All records that start with <b>man</b>.</span></span></TD>
  </TR>
    <TR>
    <TD><span data-ttu-id="a66c4-142">@&#42;man</span><span class="sxs-lookup"><span data-stu-id="a66c4-142">@&#42;man</span></span></TD>
    <TD><span data-ttu-id="a66c4-143">Termina en y distingue mayúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="a66c4-143">Ends with and case insensitive.</span></span></TD>
    <TD><span data-ttu-id="a66c4-144">Todos los registros que terminen en <b>man</b>.</span><span class="sxs-lookup"><span data-stu-id="a66c4-144">All records that end with <b>man</b>.</span></span></TD>
  </TR>
</TABLE>

> [!NOTE]  
>   <span data-ttu-id="a66c4-145">No puede usar un carácter comodín al filtrar en los campos de enumeración, como el campo **Estado** en los pedidos de venta.</span><span class="sxs-lookup"><span data-stu-id="a66c4-145">You cannot use a wildcard when filtering on enumeration fields, such as the **Status** field on sales orders.</span></span> <span data-ttu-id="a66c4-146">Para especificar un filtro para este tipo de campo, puede especificar el valor numérico como parámetro de filtrado.</span><span class="sxs-lookup"><span data-stu-id="a66c4-146">To enter a filter for this type of field, you can enter the numeric value as a filtering parameter.</span></span> <span data-ttu-id="a66c4-147">Por ejemplo, en el campo **Estado** de un pedido de venta que tenga los valores **Abierto**, **Lanzado**, **Aprobación pendiente** y **Prepago pendiente**, utilice los valores **0**, **1**, **2** y **3** para filtrar para estas opciones.</span><span class="sxs-lookup"><span data-stu-id="a66c4-147">For example, in the **Status** field on a sales order that has the values **Open**, **Released**, **Pending Approval**, and **Pending Prepayment**, use the values **0**, **1**, **2**, and **3** to filter for these options.</span></span> 

## <a name="searching-by-using-column-filters"></a><span data-ttu-id="a66c4-148">Búsqueda usando filtros de columna</span><span class="sxs-lookup"><span data-stu-id="a66c4-148">Searching by using column Filters</span></span>
<span data-ttu-id="a66c4-149">Puede agregar un filtro de una o varias columnas a una lista.</span><span class="sxs-lookup"><span data-stu-id="a66c4-149">You can add a filter on one or more columns in a list.</span></span> <span data-ttu-id="a66c4-150">El filtrado en columnas es más flexible y ampliado que el filtro rápido.</span><span class="sxs-lookup"><span data-stu-id="a66c4-150">Filtering on columns is more flexible and enhanced than the Quick Filter.</span></span> 

### <a name="to-add-a-filter-on-a-column"></a><span data-ttu-id="a66c4-151">Para agregar un filtro a una columna</span><span class="sxs-lookup"><span data-stu-id="a66c4-151">To add a filter on a column</span></span>
1.  <span data-ttu-id="a66c4-152">Antes de añadir un filtro, elija el icono ![Mostrar como una lista](media/ui_show_as_list_icon.png "Mostrar como lista de flecha izquierda") para cambiar a la vista de lista.</span><span class="sxs-lookup"><span data-stu-id="a66c4-152">Before you add a filter, choose ![Show as list](media/ui_show_as_list_icon.png "Show as list arrow left") icon to change to the list view.</span></span>
2. <span data-ttu-id="a66c4-153">Elija hacia flecha hacia abajo en la cabecera de columna y, a continuación elija **Filtro**.</span><span class="sxs-lookup"><span data-stu-id="a66c4-153">Choose the downwards arrow in the column heading, and then choose **Filter**.</span></span>
3. <span data-ttu-id="a66c4-154">Realice una de las siguientes acciones:</span><span class="sxs-lookup"><span data-stu-id="a66c4-154">Do one of the following:</span></span> 
  -  <span data-ttu-id="a66c4-155">Seleccione *…* al lado del cuadro para seleccionar un valor de una lista.</span><span class="sxs-lookup"><span data-stu-id="a66c4-155">Choose *...* next to the box to select a value from a list.</span></span>
  -  <span data-ttu-id="a66c4-156">Introduzca criterios de filtro en el cuadro.</span><span class="sxs-lookup"><span data-stu-id="a66c4-156">Enter filter criteria in the box.</span></span> <span data-ttu-id="a66c4-157">Véase la sección siguiente para obtener información detallada.</span><span class="sxs-lookup"><span data-stu-id="a66c4-157">See the next section for details.</span></span>
4. <span data-ttu-id="a66c4-158">Elija el botón **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="a66c4-158">Choose the **OK** button.</span></span>

## <a name="filter-criteria-and-symbols"></a><span data-ttu-id="a66c4-159">Filtrar los criterios y símbolos</span><span class="sxs-lookup"><span data-stu-id="a66c4-159">Filter criteria and symbols</span></span>
<span data-ttu-id="a66c4-160">Al introducir criterios, puede usar todos los números y las letras que normalmente se emplean en un campo.</span><span class="sxs-lookup"><span data-stu-id="a66c4-160">When you enter criteria, you can use all the numbers and letters that you can normally use in the field.</span></span> <span data-ttu-id="a66c4-161">También puede usar símbolos especiales para filtrar aún más los resultados.</span><span class="sxs-lookup"><span data-stu-id="a66c4-161">In addition, you can use special symbols to further filter the results.</span></span> <span data-ttu-id="a66c4-162">En las tablas siguientes se muestran los símbolos que se pueden usar en los filtros.</span><span class="sxs-lookup"><span data-stu-id="a66c4-162">The following tables show the symbols which can be used in filters.</span></span>  
  
> [!IMPORTANT]  
>  <span data-ttu-id="a66c4-163">Puede haber instancias donde los valores de campo contengan los siguientes símbolos y desee filtrarlos.</span><span class="sxs-lookup"><span data-stu-id="a66c4-163">There may be instances where field values contain these symbols and you want to filter on them.</span></span> <span data-ttu-id="a66c4-164">Para ello, debe incluir la expresión de filtro que contiene el símbolo entre comillas (").</span><span class="sxs-lookup"><span data-stu-id="a66c4-164">To do this, you must include the filter expression that contains the symbol in quotation marks ('').</span></span> <span data-ttu-id="a66c4-165">Por ejemplo, si desea filtrar en los registros que comienzan por el texto *S&R*, la expresión de filtro es **'S&R\*'**.</span><span class="sxs-lookup"><span data-stu-id="a66c4-165">For example, if you want to filter on records that start with the text *S&R*, the filter expression is **'S&R\*'**.</span></span>  
  
### <a name="-interval"></a><span data-ttu-id="a66c4-166">(..) Intervalo</span><span class="sxs-lookup"><span data-stu-id="a66c4-166">(..) Interval</span></span>  
  
|<span data-ttu-id="a66c4-167">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="a66c4-167">Sample Expression</span></span>|<span data-ttu-id="a66c4-168">Registros mostrados</span><span class="sxs-lookup"><span data-stu-id="a66c4-168">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|<span data-ttu-id="a66c4-169">1100..2100</span><span class="sxs-lookup"><span data-stu-id="a66c4-169">1100..2100</span></span>|<span data-ttu-id="a66c4-170">Números del 1100 al 2100.</span><span class="sxs-lookup"><span data-stu-id="a66c4-170">Numbers 1100 through 2100</span></span>|  
|<span data-ttu-id="a66c4-171">..2500</span><span class="sxs-lookup"><span data-stu-id="a66c4-171">..2500</span></span>|<span data-ttu-id="a66c4-172">Hasta la 2500 inclusive</span><span class="sxs-lookup"><span data-stu-id="a66c4-172">Up to and including 2500</span></span>|  
|<span data-ttu-id="a66c4-173">..12 31 00</span><span class="sxs-lookup"><span data-stu-id="a66c4-173">..12 31 00</span></span>|<span data-ttu-id="a66c4-174">Fechas hasta el 31 12 00, inclusive.</span><span class="sxs-lookup"><span data-stu-id="a66c4-174">Dates up to and including 12 31 00</span></span>|  
|<span data-ttu-id="a66c4-175">P8..</span><span class="sxs-lookup"><span data-stu-id="a66c4-175">P8..</span></span>|<span data-ttu-id="a66c4-176">Información correspondiente al ejercicio económico 8 en adelante</span><span class="sxs-lookup"><span data-stu-id="a66c4-176">Information for accounting period 8 and thereafter</span></span>|  
|<span data-ttu-id="a66c4-177">..23</span><span class="sxs-lookup"><span data-stu-id="a66c4-177">..23</span></span>|<span data-ttu-id="a66c4-178">Desde la fecha inicial hasta 23-mes actual-año actual 23:59:59</span><span class="sxs-lookup"><span data-stu-id="a66c4-178">From the beginning date until 23-current month-current year 23:59:59</span></span>|  
|<span data-ttu-id="a66c4-179">23..</span><span class="sxs-lookup"><span data-stu-id="a66c4-179">23..</span></span>|<span data-ttu-id="a66c4-180">Desde 23-mes actual-año actual 0:00:00 hasta la hora final</span><span class="sxs-lookup"><span data-stu-id="a66c4-180">From 23-current month-current year 0:00:00 until the end of time</span></span>|  
|<span data-ttu-id="a66c4-181">22..23</span><span class="sxs-lookup"><span data-stu-id="a66c4-181">22..23</span></span>|<span data-ttu-id="a66c4-182">Desde 22-mes actual-año actual 0:00:00 hasta 23-mes actual-año actual 23:59:59</span><span class="sxs-lookup"><span data-stu-id="a66c4-182">From 22-current month-current year 0:00:00 until 23-current month-current year 23:59:59</span></span>|  
  
### <a name="124-eitheror"></a><span data-ttu-id="a66c4-183">(&#124;) O/o</span><span class="sxs-lookup"><span data-stu-id="a66c4-183">(&#124;) Either/or</span></span>  
  
|<span data-ttu-id="a66c4-184">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="a66c4-184">Sample Expression</span></span>|<span data-ttu-id="a66c4-185">Registros mostrados</span><span class="sxs-lookup"><span data-stu-id="a66c4-185">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|<span data-ttu-id="a66c4-186">1200&#124;1300</span><span class="sxs-lookup"><span data-stu-id="a66c4-186">1200&#124;1300</span></span>|<span data-ttu-id="a66c4-187">Números con 1200 ó 1300</span><span class="sxs-lookup"><span data-stu-id="a66c4-187">Numbers with 1200 or 1300</span></span>|  
  
### <a name="-not-equal-to"></a><span data-ttu-id="a66c4-188">(<>) Distinto</span><span class="sxs-lookup"><span data-stu-id="a66c4-188">(<>) Not equal to</span></span>  
  
|<span data-ttu-id="a66c4-189">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="a66c4-189">Sample Expression</span></span>|<span data-ttu-id="a66c4-190">Registros mostrados</span><span class="sxs-lookup"><span data-stu-id="a66c4-190">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|<span data-ttu-id="a66c4-191"><>0</span><span class="sxs-lookup"><span data-stu-id="a66c4-191"><>0</span></span>|<span data-ttu-id="a66c4-192">Todos los números, excepto el 0</span><span class="sxs-lookup"><span data-stu-id="a66c4-192">All numbers except 0</span></span><br /><br /> <span data-ttu-id="a66c4-193">La opción SQL Server permite combinar este símbolo con una expresión de caracteres comodín.</span><span class="sxs-lookup"><span data-stu-id="a66c4-193">The SQL Server Option allows you to combine this symbol with a wild card expression.</span></span> <span data-ttu-id="a66c4-194">Por ejemplo, <>A\* significa distinto de cualquier texto que empiece por A.</span><span class="sxs-lookup"><span data-stu-id="a66c4-194">For example, <>A\* meaning not equal to any text that starts with A.</span></span>|  
  
### <a name="-greater-than"></a><span data-ttu-id="a66c4-195">(>) Mayor de</span><span class="sxs-lookup"><span data-stu-id="a66c4-195">(>) Greater than</span></span>  
  
|<span data-ttu-id="a66c4-196">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="a66c4-196">Sample Expression</span></span>|<span data-ttu-id="a66c4-197">Registros mostrados</span><span class="sxs-lookup"><span data-stu-id="a66c4-197">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|<span data-ttu-id="a66c4-198">>1200</span><span class="sxs-lookup"><span data-stu-id="a66c4-198">>1200</span></span>|<span data-ttu-id="a66c4-199">Números mayores que 1200</span><span class="sxs-lookup"><span data-stu-id="a66c4-199">Numbers greater than 1200</span></span>|  
  
### <a name="-greater-than-or-equal-to"></a><span data-ttu-id="a66c4-200">(>=) Mayor o igual a</span><span class="sxs-lookup"><span data-stu-id="a66c4-200">(>=) Greater than or equal to</span></span>  
  
|<span data-ttu-id="a66c4-201">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="a66c4-201">Sample Expression</span></span>|<span data-ttu-id="a66c4-202">Registros mostrados</span><span class="sxs-lookup"><span data-stu-id="a66c4-202">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|<span data-ttu-id="a66c4-203">>=1200</span><span class="sxs-lookup"><span data-stu-id="a66c4-203">>=1200</span></span>|<span data-ttu-id="a66c4-204">Números mayores o igual que 1200</span><span class="sxs-lookup"><span data-stu-id="a66c4-204">Numbers greater than or equal to 1200</span></span>|  
  
### <a name="-less-than"></a><span data-ttu-id="a66c4-205">(<) Menor de</span><span class="sxs-lookup"><span data-stu-id="a66c4-205">(<) Less than</span></span>  
  
|<span data-ttu-id="a66c4-206">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="a66c4-206">Sample Expression</span></span>|<span data-ttu-id="a66c4-207">Registros mostrados</span><span class="sxs-lookup"><span data-stu-id="a66c4-207">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|<span data-ttu-id="a66c4-208"><1200</span><span class="sxs-lookup"><span data-stu-id="a66c4-208"><1200</span></span>|<span data-ttu-id="a66c4-209">Números menores que 1200</span><span class="sxs-lookup"><span data-stu-id="a66c4-209">Numbers less than 1200</span></span>|  
  
### <a name="-less-than-or-equal-to"></a><span data-ttu-id="a66c4-210">(<=) Menor o igual que</span><span class="sxs-lookup"><span data-stu-id="a66c4-210">(<=) Less than or equal to</span></span>  
  
|<span data-ttu-id="a66c4-211">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="a66c4-211">Sample Expression</span></span>|<span data-ttu-id="a66c4-212">Registros mostrados</span><span class="sxs-lookup"><span data-stu-id="a66c4-212">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|<span data-ttu-id="a66c4-213"><=1200</span><span class="sxs-lookup"><span data-stu-id="a66c4-213"><=1200</span></span>|<span data-ttu-id="a66c4-214">Números menores o iguales que 1200</span><span class="sxs-lookup"><span data-stu-id="a66c4-214">Numbers less than or equal to 1200</span></span>|  
  
### <a name="-and"></a><span data-ttu-id="a66c4-215">(&) y</span><span class="sxs-lookup"><span data-stu-id="a66c4-215">(&) And</span></span>  
  
|<span data-ttu-id="a66c4-216">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="a66c4-216">Sample Expression</span></span>|<span data-ttu-id="a66c4-217">Registros mostrados</span><span class="sxs-lookup"><span data-stu-id="a66c4-217">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|<span data-ttu-id="a66c4-218">>200&<1200</span><span class="sxs-lookup"><span data-stu-id="a66c4-218">>200&<1200</span></span>|<span data-ttu-id="a66c4-219">Números mayores de 200 e inferiores a 1200</span><span class="sxs-lookup"><span data-stu-id="a66c4-219">Numbers greater than 200 and less than 1200</span></span>|  
  
### <a name="-an-exact-character-match"></a><span data-ttu-id="a66c4-220">(") Una coincidencia exacta de carácter</span><span class="sxs-lookup"><span data-stu-id="a66c4-220">('') An exact character match</span></span>  
  
|<span data-ttu-id="a66c4-221">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="a66c4-221">Sample Expression</span></span>|<span data-ttu-id="a66c4-222">Registros mostrados</span><span class="sxs-lookup"><span data-stu-id="a66c4-222">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|<span data-ttu-id="a66c4-223">'man'</span><span class="sxs-lookup"><span data-stu-id="a66c4-223">'man'</span></span>|<span data-ttu-id="a66c4-224">Texto que coincide exactamente con man y distingue mayúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="a66c4-224">Text that matches man exactly and is case sensitive.</span></span>|  
  
### <a name="-case-insensitive"></a><span data-ttu-id="a66c4-225">(@) Distinción entre mayúsculas y minúsculas</span><span class="sxs-lookup"><span data-stu-id="a66c4-225">(@) Case insensitive</span></span>  
  
|<span data-ttu-id="a66c4-226">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="a66c4-226">Sample Expression</span></span>|<span data-ttu-id="a66c4-227">Registros mostrados</span><span class="sxs-lookup"><span data-stu-id="a66c4-227">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|<span data-ttu-id="a66c4-228">@man\*</span><span class="sxs-lookup"><span data-stu-id="a66c4-228">@man\*</span></span>|<span data-ttu-id="a66c4-229">Texto que empieza por man y no distingue mayúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="a66c4-229">Text that starts with man and is case insensitive.</span></span>|  
  
### <a name="-an-indefinite-number-of-unknown-characters"></a><span data-ttu-id="a66c4-230">(\*) Un número indefinido de caracteres desconocidos (quizás ninguno)</span><span class="sxs-lookup"><span data-stu-id="a66c4-230">(\*) An indefinite number of unknown characters</span></span>  
  
|<span data-ttu-id="a66c4-231">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="a66c4-231">Sample Expression</span></span>|<span data-ttu-id="a66c4-232">Registros mostrados</span><span class="sxs-lookup"><span data-stu-id="a66c4-232">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|<span data-ttu-id="a66c4-233">*Co*</span><span class="sxs-lookup"><span data-stu-id="a66c4-233">*Co*</span></span>|<span data-ttu-id="a66c4-234">Texto que contenga “Co” y es con diferenciación de mayúsculas y minúsculas.</span><span class="sxs-lookup"><span data-stu-id="a66c4-234">Text that contains "Co" and is case sensitive.</span></span>|  
|<span data-ttu-id="a66c4-235">\*Co</span><span class="sxs-lookup"><span data-stu-id="a66c4-235">\*Co</span></span>|<span data-ttu-id="a66c4-236">Texto que termine con “Co” y es con diferenciación de mayúsculas y minúsculas.</span><span class="sxs-lookup"><span data-stu-id="a66c4-236">Text that ends with "Co" and is case sensitive.</span></span>|  
|<span data-ttu-id="a66c4-237">Co\*</span><span class="sxs-lookup"><span data-stu-id="a66c4-237">Co\*</span></span>|<span data-ttu-id="a66c4-238">Texto que empiece por “Co” y es con diferenciación de mayúsculas y minúsculas.</span><span class="sxs-lookup"><span data-stu-id="a66c4-238">Text that begins with "Co" and is case sensitive.</span></span>|  
  
### <a name="-one-unknown-character"></a><span data-ttu-id="a66c4-239">(?) Un carácter desconocido</span><span class="sxs-lookup"><span data-stu-id="a66c4-239">(?) One unknown character</span></span>  
  
|<span data-ttu-id="a66c4-240">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="a66c4-240">Sample Expression</span></span>|<span data-ttu-id="a66c4-241">Registros mostrados</span><span class="sxs-lookup"><span data-stu-id="a66c4-241">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|<span data-ttu-id="a66c4-242">Mendo?a</span><span class="sxs-lookup"><span data-stu-id="a66c4-242">Hans?n</span></span>|<span data-ttu-id="a66c4-243">Texto como Mendoza o Mendosa</span><span class="sxs-lookup"><span data-stu-id="a66c4-243">Text such as Hansen or Hanson</span></span>|  
  
### <a name="combined-format-expressions"></a><span data-ttu-id="a66c4-244">Expresiones de formato combinadas</span><span class="sxs-lookup"><span data-stu-id="a66c4-244">Combined format expressions</span></span>  
  
|<span data-ttu-id="a66c4-245">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="a66c4-245">Sample Expression</span></span>|<span data-ttu-id="a66c4-246">Registros mostrados</span><span class="sxs-lookup"><span data-stu-id="a66c4-246">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|<span data-ttu-id="a66c4-247">5999&#124;8100..8490</span><span class="sxs-lookup"><span data-stu-id="a66c4-247">5999&#124;8100..8490</span></span>|<span data-ttu-id="a66c4-248">Incluye todos los registros cuyo número sea 5999 o un número entre 8100 y 8490.</span><span class="sxs-lookup"><span data-stu-id="a66c4-248">Include any records with the number 5999 or a number from the interval 8100 through 8490.</span></span>|  
|<span data-ttu-id="a66c4-249">..1299&#124;1400..</span><span class="sxs-lookup"><span data-stu-id="a66c4-249">..1299&#124;1400..</span></span>|<span data-ttu-id="a66c4-250">Incluye los registros cuyo número sea menor o igual que 1299 o un número igual o mayor que 1400</span><span class="sxs-lookup"><span data-stu-id="a66c4-250">Include records with a number less than or equal to 1299 or a number equal to 1400 or greater (all numbers except 1300 through 1399).</span></span>|  
|<span data-ttu-id="a66c4-251">>50&<100</span><span class="sxs-lookup"><span data-stu-id="a66c4-251">>50&<100</span></span>|<span data-ttu-id="a66c4-252">Incluye los registros cuyo número sea mayor que 50 y menor que 100.</span><span class="sxs-lookup"><span data-stu-id="a66c4-252">Include records with numbers that are greater than 50 and less than 100 (numbers 51 through 99).</span></span>|  
 
## <a name="see-also"></a><span data-ttu-id="a66c4-253">Consulte también</span><span class="sxs-lookup"><span data-stu-id="a66c4-253">See Also</span></span>
<span data-ttu-id="a66c4-254">[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="a66c4-254">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

