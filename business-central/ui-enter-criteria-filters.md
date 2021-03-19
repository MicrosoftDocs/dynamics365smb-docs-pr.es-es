---
title: Ordenar, buscar y filtrar listas | Documentos de Microsoft
description: Trabaje de manera eficiente en las listas buscando en sus datos, clasificando columnas y refinando los resultados utilizando símbolos de filtrado y atajos de teclado.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: delimit, FlowFilter, totals, limit, advanced
ms.date: 11/16/2020
ms.author: jswymer
ms.openlocfilehash: d682f9e66075348785329cd13a12c3e02d0993c4
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5385854"
---
# <a name="sorting-searching-and-filtering"></a><span data-ttu-id="84f75-103">Ordenar, buscar y filtrar</span><span class="sxs-lookup"><span data-stu-id="84f75-103">Sorting, Searching, and Filtering</span></span>

<span data-ttu-id="84f75-104">Existen algunos parámetros que puede configurar que le ayudarán a buscar, encontrar y limitar los registros de una lista, un informe o un XMLport</span><span class="sxs-lookup"><span data-stu-id="84f75-104">There are a few things that you can do that will help you scan, find, and limit records on a list or in a report or XMLport.</span></span> <span data-ttu-id="84f75-105">Estos incluyen la ordenación, la búsqueda y el filtrado.</span><span class="sxs-lookup"><span data-stu-id="84f75-105">These include sorting, searching, and filtering.</span></span> <span data-ttu-id="84f75-106">Puede aplicar solo algunos o todos a la vez para encontrar o analizar rápidamente sus datos.</span><span class="sxs-lookup"><span data-stu-id="84f75-106">You can apply some or all of these simultaneously to quickly find or analyze your data.</span></span>

<span data-ttu-id="84f75-107">Para informes y XMLports, como en las listas, puede establecer filtros para delimitar qué datos se incluirán en el informe o XMLport, pero no puede ordenar y buscar.</span><span class="sxs-lookup"><span data-stu-id="84f75-107">For reports and XMLports, as on lists, you can set filters to delimit which data to include in the report or XMLport, but you can't sort and search.</span></span>

> [!TIP]
> <span data-ttu-id="84f75-108">Al ver los datos como mosaicos, puede buscar y usar el filtrado.</span><span class="sxs-lookup"><span data-stu-id="84f75-108">When viewing your data as tiles, you can search and use filtering.</span></span> <span data-ttu-id="84f75-109">Para usar el conjunto completo de potentes funciones para ordenar, buscar y filtrar, elija el icono ![Mostrar como lista](media/ui_show_as_list_icon.png "Flecha izquierda de Mostrar como lista") para ver los registros como una lista.</span><span class="sxs-lookup"><span data-stu-id="84f75-109">To use the full set of powerful features for sorting, searching, and filtering, choose the ![Show as list](media/ui_show_as_list_icon.png "Show as list arrow left") icon to view the records as a list.</span></span>

<!--
When you want to search for data, such as customer names, addresses, or product groups, you enter criteria. In search criteria, you can use all the numbers and letters that you normally use in the specific field. In addition, you can use special symbols to further filter the results. There are two ways to search: using the Quick Filter or column filters.
-->

## <a name="sorting"></a><span data-ttu-id="84f75-110">Ordenación</span><span class="sxs-lookup"><span data-stu-id="84f75-110">Sorting</span></span>

<span data-ttu-id="84f75-111">La ordenación facilita la obtención rápida de un resumen de sus datos.</span><span class="sxs-lookup"><span data-stu-id="84f75-111">Sorting makes it easy for you to get a quick overview of your data.</span></span> <span data-ttu-id="84f75-112">Por ejemplo, si hay varios clientes, por ejemplo, podría elegir ordenarlos por **N.º de cliente**, **Cód. divisa** o **Cód. país/región** para disponer de la vista general que desea.</span><span class="sxs-lookup"><span data-stu-id="84f75-112">For example, if you have many customers,  you could sort them by **Customer No.**, **Currency Code**, or **Country Region Code** to get the overview you need.</span></span>

<span data-ttu-id="84f75-113">Para ordenar una lista, puede:</span><span class="sxs-lookup"><span data-stu-id="84f75-113">To sort a list, you can either:</span></span>

- <span data-ttu-id="84f75-114">Elegir un texto de encabezado de columna para alternar entre orden ascendente y descendente, o</span><span class="sxs-lookup"><span data-stu-id="84f75-114">Choose a column heading text to toggle between ascending and descending order, or</span></span>
- <span data-ttu-id="84f75-115">Elegir la flecha desplegable en el encabezado de la columna, luego elija la acción **Ascendente** o **Descendiendo**.</span><span class="sxs-lookup"><span data-stu-id="84f75-115">Choose the drop-down arrow in the column heading, then choose the **Ascending** or **Descending** action.</span></span>  

> [!NOTE]  
> <span data-ttu-id="84f75-116">El ordenamiento no se admite en imágenes, campos BLOB, FlowFilters ni campos que no pertenecen a una tabla.</span><span class="sxs-lookup"><span data-stu-id="84f75-116">Sorting isn't supported on images, BLOB fields, FlowFilters, and fields that do not belong to a table.</span></span>  

## <a name="searching"></a><span data-ttu-id="84f75-117">Búsqueda</span><span class="sxs-lookup"><span data-stu-id="84f75-117">Searching</span></span>

<!--## Searching by using the Quick Filter -->
<span data-ttu-id="84f75-118">En la parte superior de cada página de la lista, hay una acción ![Buscar en la lista](media/ui-search/search-list.png "Icono de lista de búsqueda") **Buscar** Buscar que proporciona una manera rápida y fácil de reducir los registros en una lista y muestra solo aquellos registros que contienen los datos que le interesa ver.</span><span class="sxs-lookup"><span data-stu-id="84f75-118">At the top of each list page, there's a ![Search list](media/ui-search/search-list.png "Search list icon") **Search** action that provides a quick and easy way to reduce the records in a list and display only those records that contain the data that you're interested in seeing.</span></span>

<span data-ttu-id="84f75-119">Para buscar, solo elija la acción **Buscar** y, a continuación, en el cuadro, escriba el texto que está buscando.</span><span class="sxs-lookup"><span data-stu-id="84f75-119">To search, just choose the **Search** action, and then in the box, type the text that you're looking for.</span></span> <span data-ttu-id="84f75-120">Puede escribir letras, números y otros símbolos.</span><span class="sxs-lookup"><span data-stu-id="84f75-120">You can enter letters, numbers, and other symbols.</span></span>

<span data-ttu-id="84f75-121">En general, la búsqueda intentará hacer coincidir el texto en todos los campos.</span><span class="sxs-lookup"><span data-stu-id="84f75-121">In general, search will attempt to match text across all fields.</span></span> <span data-ttu-id="84f75-122">No distingue entre mayúsculas y minúsculas y coincidirá con el texto colocado en algún lugar del campo: al principio, al final o en el centro.</span><span class="sxs-lookup"><span data-stu-id="84f75-122">It doesn't distinguish between uppercase and lowercase characters (case insensitive) and will match text placed anywhere in the field, at the beginning, end, or in the middle.</span></span>

> [!TIP]
> <span data-ttu-id="84f75-123">Puede presionar **F3** para activar y desactivar el cuadro de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="84f75-123">You can press **F3** to activate and deactivate the search box.</span></span> <span data-ttu-id="84f75-124">Para obtener más información, consulte [Métodos abreviados de teclado](keyboard-shortcuts.md#KeyboardFilter).</span><span class="sxs-lookup"><span data-stu-id="84f75-124">For more information, see [Keyboard Shortcuts](keyboard-shortcuts.md#KeyboardFilter).</span></span>

> [!NOTE]  
> <span data-ttu-id="84f75-125">La búsqueda no coincidirá con valores en imágenes, campos BLOB, FlowFilters, FlowFields y otros campos que no forman parte de una tabla.</span><span class="sxs-lookup"><span data-stu-id="84f75-125">Search won't match values in images, BLOB fields, FlowFilters, FlowFields, and other fields that aren't part of a table.</span></span>


### <a name="fine-tuning-the-search-with-filter-criteria"></a><span data-ttu-id="84f75-126">Ajuste de los criterios de búsqueda con filtro</span><span class="sxs-lookup"><span data-stu-id="84f75-126">Fine-tuning the Search with Filter criteria</span></span>

<span data-ttu-id="84f75-127">Puede realizar una búsqueda más exacta utilizando operadores de filtro, expresiones y tokens de filtro.</span><span class="sxs-lookup"><span data-stu-id="84f75-127">You can make a more exact search by using filter operators, expressions, and filter tokens.</span></span> <span data-ttu-id="84f75-128">A diferencia del filtrado, estos se aplican en todos los campos cuando se utilizan en el cuadro de búsqueda, lo que los hace menos eficientes que el filtrado.</span><span class="sxs-lookup"><span data-stu-id="84f75-128">Unlike filtering, these are applied across all fields when used in the search box, making them less efficient than filtering.</span></span>

- <span data-ttu-id="84f75-129">Para buscar solo valores de campo que coincidan exactamente con el texto completo y el caso, coloque el texto de búsqueda entre comillas simples `''` (por ejemplo, `'man'`).</span><span class="sxs-lookup"><span data-stu-id="84f75-129">To find only field values that match the entire text and case exactly, place the search text between single quotes `''` (for example, `'man'`).</span></span>

- <span data-ttu-id="84f75-130">Para buscar valores de campo que comiencen con un determinado texto y coincidan con el caso, coloque `*` después del texto de búsqueda (por ejemplo, `man*`).</span><span class="sxs-lookup"><span data-stu-id="84f75-130">To find field values that start with a certain text and match the case, place `*` after the search text (for example `man*`).</span></span>

- <span data-ttu-id="84f75-131">Para buscar valores de campo que acaben con un determinado texto y coincidan con el caso, coloque `*` antes del texto de búsqueda (por ejemplo, `*man`).</span><span class="sxs-lookup"><span data-stu-id="84f75-131">To find field values that end with a certain text and match the case, place `*` before the search text (for example `*man`).</span></span>

- <span data-ttu-id="84f75-132">Cuando se utiliza `''` o `*`, la búsqueda distingue entre mayúsculas y minúsculas.</span><span class="sxs-lookup"><span data-stu-id="84f75-132">When using  `''` or `*`, the search is case-sensitive.</span></span> <span data-ttu-id="84f75-133">Si desea que la búsqueda no distinga entre mayúsculas y minúsculas, coloque `@` antes del texto de búsqueda (por ejemplo, `@man*`).</span><span class="sxs-lookup"><span data-stu-id="84f75-133">If you want to make the search case insensitive, place `@` before the search text (for example `@man*`).</span></span>

<span data-ttu-id="84f75-134">En la tabla siguiente se muestran algunos ejemplos de cómo puede utilizar la búsqueda.</span><span class="sxs-lookup"><span data-stu-id="84f75-134">The following table provides some examples to explain how you can use the search.</span></span>

|<span data-ttu-id="84f75-135">Criterios de búsqueda</span><span class="sxs-lookup"><span data-stu-id="84f75-135">Search Criteria</span></span>|<span data-ttu-id="84f75-136">Búsquedas…</span><span class="sxs-lookup"><span data-stu-id="84f75-136">Finds...</span></span>|
|---------------|----------|
|`man`<br /><span data-ttu-id="84f75-137">o</span><span class="sxs-lookup"><span data-stu-id="84f75-137">or</span></span> <br />`Man`|<span data-ttu-id="84f75-138">Todos los registros con los campos que contienen el texto **man**, independientemente de las mayúsculas y minúsculas.</span><span class="sxs-lookup"><span data-stu-id="84f75-138">All records with fields that contain the text **man**, regardless of the case.</span></span> <span data-ttu-id="84f75-139">Por ejemplo, **Manchester**, **manual** o **Norman**.</span><span class="sxs-lookup"><span data-stu-id="84f75-139">For example, **Manchester**, **manual**, or **Sportsman**.</span></span> |
|`'Man'`|<span data-ttu-id="84f75-140">Todos los registros con los campos que contienen solo el texto **Man** y coinciden las mayúsculas y minúsculas.</span><span class="sxs-lookup"><span data-stu-id="84f75-140">All records with fields that contain only **Man**, matching the case.</span></span>|
|`Man*`|<span data-ttu-id="84f75-141">Todos los registros con los campos que empiezan por <b>Man</b> y coinciden las mayúsculas y minúsculas.</span><span class="sxs-lookup"><span data-stu-id="84f75-141">All records with fields that start with the text <b>Man</b>, matching the case.</span></span> <span data-ttu-id="84f75-142">Por ejemplo, **Manchester** pero no **manual** o **Norman**.</span><span class="sxs-lookup"><span data-stu-id="84f75-142">For example, **Manchester** but not **manual** or **Sportsman**.</span></span>|
|`@Man*`|<span data-ttu-id="84f75-143">Todos los registros con los campos que empiezan por **man** independientemente de las mayúsculas y minúsculas.</span><span class="sxs-lookup"><span data-stu-id="84f75-143">All records with fields that start with **man**, regardless of the case.</span></span> <span data-ttu-id="84f75-144">Por ejemplo, **Manchester** y **manual** pero no **Norman**.</span><span class="sxs-lookup"><span data-stu-id="84f75-144">For example, **Manchester** and **manual**, but not **Sportsman**.</span></span>|
|`@*man`|<span data-ttu-id="84f75-145">Todos los registros que acaban por **man** independientemente de las mayúsculas y minúsculas.</span><span class="sxs-lookup"><span data-stu-id="84f75-145">All records that end with **man**, regardless of the case.</span></span> <span data-ttu-id="84f75-146">Por ejemplo, **Norman** pero no **Manchester** o **manual**.</span><span class="sxs-lookup"><span data-stu-id="84f75-146">For example **Sportsman**, but not **Manchester** or **manual**.</span></span>|


## <a name="filtering"></a><a name="filtering"></a><span data-ttu-id="84f75-147">Filtrado</span><span class="sxs-lookup"><span data-stu-id="84f75-147">Filtering</span></span>

<span data-ttu-id="84f75-148">El filtrado proporciona una forma más avanzada y versátil de controlar qué registros se incluyen en una lista o se incluyen en un informe o XMLport.</span><span class="sxs-lookup"><span data-stu-id="84f75-148">Filtering provides a more advanced and versatile way to control which records are included in a list, report, or XMLport.</span></span> <span data-ttu-id="84f75-149">Existen dos diferencias principales entre la búsqueda y el filtrado, como se describe en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="84f75-149">There are two major differences between searching and filtering, as described in the table below.</span></span>

|| <span data-ttu-id="84f75-150">**Búsqueda**</span><span class="sxs-lookup"><span data-stu-id="84f75-150">**Searching**</span></span> | <span data-ttu-id="84f75-151">**Filtrado**</span><span class="sxs-lookup"><span data-stu-id="84f75-151">**Filtering**</span></span> |
|--|----------|------------|
| <span data-ttu-id="84f75-152">**Campos aplicables**</span><span class="sxs-lookup"><span data-stu-id="84f75-152">**Applicable Fields**</span></span> | <span data-ttu-id="84f75-153">Busca en todos los campos que están visibles en la página.</span><span class="sxs-lookup"><span data-stu-id="84f75-153">Searches across all fields that are visible on the page.</span></span> | <span data-ttu-id="84f75-154">Filtra uno o más campos individualmente, los selecciona desde cualquier campo de la tabla, incluidos los campos que no están visibles en la página.</span><span class="sxs-lookup"><span data-stu-id="84f75-154">Filters one or more fields individually, selecting from any field on the table, including fields that aren't visible on the page.</span></span> |
| <span data-ttu-id="84f75-155">**Coincidencia**</span><span class="sxs-lookup"><span data-stu-id="84f75-155">**Matching**</span></span> | <span data-ttu-id="84f75-156">Muestra registros con campos que coinciden con el texto de búsqueda, independientemente de las mayúsculas o la ubicación del texto en el campo.</span><span class="sxs-lookup"><span data-stu-id="84f75-156">Displays records with fields that match the search text, no matter the text's case or placement in the field.</span></span> | <span data-ttu-id="84f75-157">Muestra los registros en los que el campo coincide exactamente con el filtro, y distingue entre mayúsculas y minúsculas, a menos que se introduzcan símbolos de filtrado especiales.</span><span class="sxs-lookup"><span data-stu-id="84f75-157">Displays records where the field exactly matches the filter, including the text's case, unless special filter symbols are entered.</span></span>

<span data-ttu-id="84f75-158">El filtrado le permite mostrar registros de cuentas o clientes específicos, fechas, importes y otra información especificando criterios de filtro.</span><span class="sxs-lookup"><span data-stu-id="84f75-158">Filtering enables you to display records for specific accounts or customers, dates, amounts, and other information by specifying filter criteria.</span></span> <span data-ttu-id="84f75-159">Solo los registros que coinciden con los criterios se muestran en la lista o se incluyen en el informe, trabajo por lotes o XMLport.</span><span class="sxs-lookup"><span data-stu-id="84f75-159">Only records that match the criteria are displayed on the list or included in the report, batch job, or XMLport.</span></span> <span data-ttu-id="84f75-160">Si especifica criterios para varios campos, solo se mostrarán los registros que coincidan con todos los criterios.</span><span class="sxs-lookup"><span data-stu-id="84f75-160">If you specify criteria for multiple fields, then only records that match all criteria will be displayed.</span></span>

<span data-ttu-id="84f75-161">Para las listas, los filtros se muestran en un panel de filtro que aparece a la izquierda de la lista cuando lo activa.</span><span class="sxs-lookup"><span data-stu-id="84f75-161">For lists, the filters are displayed on a filter pane that appears to the left of the list when you activate it.</span></span> <span data-ttu-id="84f75-162">Para informes, trabajos por lotes y XMLports, los filtros están visibles directamente en la página de solicitud.</span><span class="sxs-lookup"><span data-stu-id="84f75-162">For reports, batch jobs, and XMLports, the filters are visible directly on the request page.</span></span>

### <a name="filtering-with-option-fields"></a><span data-ttu-id="84f75-163">Filtrado con campos de opción</span><span class="sxs-lookup"><span data-stu-id="84f75-163">Filtering with Option Fields</span></span>

<span data-ttu-id="84f75-164">Para los campos "normales" que contienen datos, fecha de configuración o datos de negocio, puede establecer filtros seleccionando datos y escribiendo valores de filtro, y puede usar símbolos para definir criterios de filtro avanzados.</span><span class="sxs-lookup"><span data-stu-id="84f75-164">For "ordinary" fields that hold data, setup date, or business data, you can set filters both by selecting data and by typing filter values, and you can use symbols to define advanced filter criteria.</span></span> <span data-ttu-id="84f75-165">Para obtener más información, vea [Introducción de criterios de filtros](ui-enter-criteria-filters.md#entering-filter-criteria).</span><span class="sxs-lookup"><span data-stu-id="84f75-165">For more information, see [Entering Filter Criteria](ui-enter-criteria-filters.md#entering-filter-criteria).</span></span>

<span data-ttu-id="84f75-166">Sin embargo, para campos de tipo **Opción**, solo puede establecer un filtro seleccionando una o más opciones de una lista desplegable de las opciones disponibles.</span><span class="sxs-lookup"><span data-stu-id="84f75-166">For fields of type **Option**, however, you can only set a filter by selecting one or more options from a drop-down list of the available options.</span></span> <span data-ttu-id="84f75-167">Un ejemplo de un campo de opción es el campo **Estado** en la página **Pedidos de venta**.</span><span class="sxs-lookup"><span data-stu-id="84f75-167">An example of an option field is the **Status** field on the **Sales Orders** page.</span></span>

> [!NOTE]
> <span data-ttu-id="84f75-168">Cuando selecciona varias opciones como valor de filtro, la relación entre las opciones se define como *O*.</span><span class="sxs-lookup"><span data-stu-id="84f75-168">When you select multiple options as a filter value, the relationship between the options is defined as *OR*.</span></span> <span data-ttu-id="84f75-169">Por ejemplo, si selecciona las casillas **Abierto** y **Lanzado** en el campo de filtro **Estado** en la página **Pedidos de venta**, significa que se muestran los pedidos de venta que están abiertos o lanzados.</span><span class="sxs-lookup"><span data-stu-id="84f75-169">For example, if you select both the **Open** and the **Released** check box in the **Status** filter field on the **Sales Orders** page, it means that sales orders that are either open or released are displayed.</span></span>

### <a name="setting-filters-on-lists"></a><span data-ttu-id="84f75-170">Configuración de filtros en listas</span><span class="sxs-lookup"><span data-stu-id="84f75-170">Setting Filters on Lists</span></span>

<span data-ttu-id="84f75-171">En las listas, los filtros se establecen utilizando el panel de filtro.</span><span class="sxs-lookup"><span data-stu-id="84f75-171">On lists, you set filters by using the filter pane.</span></span> <span data-ttu-id="84f75-172">Para mostrar el panel de filtro de una lista, elija la flecha desplegable situada junto al nombre de la página y luego elija la acción **Mostrar panel de filtros**.</span><span class="sxs-lookup"><span data-stu-id="84f75-172">To display the filter pane for a list, choose the drop-down arrow next to the name of the page, and then choose the **Show filter pane** action.</span></span> <span data-ttu-id="84f75-173">Alternativamente, presione **Mayús+F3**.</span><span class="sxs-lookup"><span data-stu-id="84f75-173">Alternatively, press **Shift+F3**.</span></span>

<span data-ttu-id="84f75-174">Para mostrar el panel de filtro de una columna de una lista, elija la flecha desplegable y luego elija la acción **Filtrar**.</span><span class="sxs-lookup"><span data-stu-id="84f75-174">To display the filter pane for a column on a list, choose the drop-down arrow, and then choose the **Filter** action.</span></span> <span data-ttu-id="84f75-175">Alternativamente, presione **Mayús+F3**.</span><span class="sxs-lookup"><span data-stu-id="84f75-175">Alternatively, press **Shift+F3**.</span></span> <span data-ttu-id="84f75-176">El panel de filtro se abre con la columna seleccionada que se muestra como un campo de filtro en la sección **Filtrar lista por**.</span><span class="sxs-lookup"><span data-stu-id="84f75-176">The filter pane opens with the selected column shown as a filter field in the **Filter list by** section.</span></span>

<span data-ttu-id="84f75-177">El panel de filtro muestra los filtros actuales para una lista y le permite configurar sus propios filtros personalizados en uno o más campos eligiendo la acción **+ Filtrar**.</span><span class="sxs-lookup"><span data-stu-id="84f75-177">The filter pane displays the current filters for a list, and enables you to set your own custom filters on one or more fields by choosing the **+ Filter** action.</span></span>

 <span data-ttu-id="84f75-178">Un panel de filtros se divide en tres secciones: **Vistas**, **Filtrar lista por** y **Filtrar totales por**:</span><span class="sxs-lookup"><span data-stu-id="84f75-178">A filter pane is divided in three sections: **Views**, **Filter list by**, and **Filter totals by**:</span></span>

- <span data-ttu-id="84f75-179">**Vistas**</span><span class="sxs-lookup"><span data-stu-id="84f75-179">**Views**</span></span>

  <span data-ttu-id="84f75-180">Algunas listas incluyen la sección **Vistas**.</span><span class="sxs-lookup"><span data-stu-id="84f75-180">Some lists include the **Views** section.</span></span> <span data-ttu-id="84f75-181">Las vistas son variaciones de la lista que se han preconfigurado con filtros.</span><span class="sxs-lookup"><span data-stu-id="84f75-181">Views are variations of the list that have been preconfigured with filters.</span></span> <span data-ttu-id="84f75-182">Puede definir y guardar tantas vistas como desee por lista.</span><span class="sxs-lookup"><span data-stu-id="84f75-182">You can define and save as many views as you want per list.</span></span> <span data-ttu-id="84f75-183">Las vistas estarán disponibles para usted en cualquier dispositivo en el que inicie sesión.</span><span class="sxs-lookup"><span data-stu-id="84f75-183">The views will be available to you on any device you sign into.</span></span> <span data-ttu-id="84f75-184">Para obtener más información, consulte [Guardar y personalizar vistas de lista](ui-views.md).</span><span class="sxs-lookup"><span data-stu-id="84f75-184">For more information, see [Save and Personalize List Views](ui-views.md).</span></span>

- <span data-ttu-id="84f75-185">**Filtrar lista por**</span><span class="sxs-lookup"><span data-stu-id="84f75-185">**Filter list by**</span></span>

  <span data-ttu-id="84f75-186">Esta sección es donde se agregan filtros en campos específicos para reducir el número de registros mostrados.</span><span class="sxs-lookup"><span data-stu-id="84f75-186">This section is where you add filters on specific fields to reduce the number of displayed records.</span></span> <span data-ttu-id="84f75-187">Para agregar un filtro, elija la acción **Filtro**.</span><span class="sxs-lookup"><span data-stu-id="84f75-187">To add a filter, choose the **+ Filter** action.</span></span> <span data-ttu-id="84f75-188">Después, para agregar un filtro, elija la acción + Filtrar, escriba el nombre del campo por el que desea filtrar la lista o elija un campo de la lista desplegable.</span><span class="sxs-lookup"><span data-stu-id="84f75-188">Then, type the name of the field that you want to filter the list by or pick a field from the drop-down list.</span></span>

- <span data-ttu-id="84f75-189">**Filtrar totales por**</span><span class="sxs-lookup"><span data-stu-id="84f75-189">**Filter totals by**</span></span>

  <span data-ttu-id="84f75-190">Algunas listas que muestran campos calculados, como cantidades e importes, incluyen la sección **Filtrar totales por**, donde puede ajustar varias dimensiones que influyen en los cálculos.</span><span class="sxs-lookup"><span data-stu-id="84f75-190">Some lists that display calculated fields, such as amounts and quantities, will include the **Filter totals by** section where you can adjust various dimensions that influence calculations.</span></span> <span data-ttu-id="84f75-191">Para agregar un filtro, elija la acción **Filtro**.</span><span class="sxs-lookup"><span data-stu-id="84f75-191">To add a filter, choose the **+ Filter** action.</span></span> <span data-ttu-id="84f75-192">Después, para agregar un filtro, elija la acción + Filtrar, escriba el nombre del campo por el que desea filtrar la lista o elija un campo de la lista desplegable.</span><span class="sxs-lookup"><span data-stu-id="84f75-192">Then, type the name of the field that you want to filter the list by or pick a field from the drop-down list.</span></span>

  > [!NOTE]
  > <span data-ttu-id="84f75-193">FlowFilters es el encargado de controlar los filtros de la sección **Filtrar totales por** en el diseño de la página.</span><span class="sxs-lookup"><span data-stu-id="84f75-193">Filters in the **Filter totals by** section are controlled by FlowFilters on the page design.</span></span> <span data-ttu-id="84f75-194">Para obtener información técnica, vea [FlowFilters](/dynamics365/business-central/dev-itpro/developer/devenv-flowfilter-overview).</span><span class="sxs-lookup"><span data-stu-id="84f75-194">For technical information, see [FlowFilters](/dynamics365/business-central/dev-itpro/developer/devenv-flowfilter-overview).</span></span>

<span data-ttu-id="84f75-195">Puede establecer un filtro simple directamente en una lista mediante el panel de filtro, es decir, un filtro que muestra solo registros con el mismo valor que en la celda seleccionada.</span><span class="sxs-lookup"><span data-stu-id="84f75-195">You can set a simple filter directly on a list within using the filter pane, namely a filter that displays only records with the same value as in the selected cell.</span></span> <span data-ttu-id="84f75-196">Seleccione una celda de la lista, elija la flecha desplegable y luego elija la acción **Filtrar a este valor**.</span><span class="sxs-lookup"><span data-stu-id="84f75-196">Select a cell on the list, choose the drop-down arrow, and then choose the **Filter to This Value** action.</span></span> <span data-ttu-id="84f75-197">Alternativamente, presione **Alt+F3**.</span><span class="sxs-lookup"><span data-stu-id="84f75-197">Alternatively, press **Alt+F3**.</span></span>

### <a name="setting-filters-in-reports-batch-jobs-and-xmlports"></a><span data-ttu-id="84f75-198">Configuración de filtros en informes, trabajos por lotes y XMLports</span><span class="sxs-lookup"><span data-stu-id="84f75-198">Setting Filters in Reports, Batch Jobs, and XMLports</span></span>

<span data-ttu-id="84f75-199">Para informes y XMLports, los filtros están visibles directamente en la página de solicitud.</span><span class="sxs-lookup"><span data-stu-id="84f75-199">For reports and XMLports, the filters are visible directly on the request page.</span></span> <span data-ttu-id="84f75-200">La página de solicitud muestra los últimos filtros utilizados de acuerdo con su selección en el campo **Usar valores predeterminados de**.</span><span class="sxs-lookup"><span data-stu-id="84f75-200">The request page displays the last used filters according to your selection in the **Use default values from** field.</span></span> <span data-ttu-id="84f75-201">Para obtener más información, consulte [Uso de la configuración guardada](ui-work-report.md#SavedSettings).</span><span class="sxs-lookup"><span data-stu-id="84f75-201">For more information, see [Using Saved Settings](ui-work-report.md#SavedSettings).</span></span>

<span data-ttu-id="84f75-202">La sección principal **Filtrar** muestra los campos de filtro predeterminados que usa para delimitar qué registros incluir en el informe o XMLport.</span><span class="sxs-lookup"><span data-stu-id="84f75-202">The main **Filter** section shows the default filter fields that you use to delimit which records to include in the report or XMLport.</span></span> <span data-ttu-id="84f75-203">Para agregar un filtro, elija la acción **Filtro**.</span><span class="sxs-lookup"><span data-stu-id="84f75-203">To add a filter, choose the **+ Filter** action.</span></span> <span data-ttu-id="84f75-204">Después, para agregar un filtro, elija la acción + Filtrar, escriba el nombre del campo por el que desea filtrar la lista o elija un campo de la lista desplegable.</span><span class="sxs-lookup"><span data-stu-id="84f75-204">Then, type the name of the field that you want to filter by, or pick a field from the drop-down list.</span></span>

<span data-ttu-id="84f75-205">En la sección **Filtrar totales por**, puede ajustar varias dimensiones que influyen en los cálculos en el informe o XMLport.</span><span class="sxs-lookup"><span data-stu-id="84f75-205">In the **Filter totals by** section, you can adjust various dimensions that influence calculations in the report or XMLport.</span></span> <span data-ttu-id="84f75-206">Para agregar un filtro, elija la acción **Filtro**.</span><span class="sxs-lookup"><span data-stu-id="84f75-206">To add a filter, choose the **+ Filter** action.</span></span> <span data-ttu-id="84f75-207">Después, para agregar un filtro, elija la acción + Filtrar, escriba el nombre del campo por el que desea filtrar la lista o elija un campo de la lista desplegable.</span><span class="sxs-lookup"><span data-stu-id="84f75-207">Then, type the name of the field that you want to filter by, or pick a field from the drop-down list.</span></span>

## <a name="entering-filter-criteria"></a><span data-ttu-id="84f75-208">Introducción de criterios de filtros</span><span class="sxs-lookup"><span data-stu-id="84f75-208">Entering Filter Criteria</span></span>

<span data-ttu-id="84f75-209">Tanto en el panel de filtro como en una página de solicitud, introduzca sus criterios de filtro en el cuadro situado debajo del campo de filtro.</span><span class="sxs-lookup"><span data-stu-id="84f75-209">Both in the filter pane and on a request page, you enter your filter criteria in the box under the filter field.</span></span>

<span data-ttu-id="84f75-210">El tipo de campo de filtro determina qué criterios puede especificar.</span><span class="sxs-lookup"><span data-stu-id="84f75-210">The type of the filter field determines which criteria you can enter.</span></span> <span data-ttu-id="84f75-211">Por ejemplo, filtrar un campo que tiene valores fijos solo le permitirá elegir entre esos valores.</span><span class="sxs-lookup"><span data-stu-id="84f75-211">For example, filtering a field that has fixed values will only let you choose from those values.</span></span> <span data-ttu-id="84f75-212">Para obtener más información sobre símbolos de filtro especiales, consulte [Criterios de filtro](#FilterCriteria) y [Tokens de filtro](#FilterTokens).</span><span class="sxs-lookup"><span data-stu-id="84f75-212">For more information about special filter symbols, see [Filter criteria](#FilterCriteria) and [Filter tokens](#FilterTokens).</span></span>

<span data-ttu-id="84f75-213">Las columnas que ya tienen filtros se indican mediante el icono ![Icono Filtro](media/ui-search/filter-icon.png "Icono de filtro") en el encabezado de la columna.</span><span class="sxs-lookup"><span data-stu-id="84f75-213">Columns that already have filters are indicated by the ![Filter icon](media/ui-search/filter-icon.png "Filter icon") icon in the column heading.</span></span> <span data-ttu-id="84f75-214">Para eliminar un filtro, seleccione la flecha desplegable y, a continuación, elija la acción **Borrar filtro**.</span><span class="sxs-lookup"><span data-stu-id="84f75-214">To remove a filter, choose the drop-down arrow, and then choose the **Clear Filter** action.</span></span>

> [!TIP]
> <span data-ttu-id="84f75-215">Acelere la búsqueda y el análisis de sus datos utilizando combinaciones de atajos de teclado.</span><span class="sxs-lookup"><span data-stu-id="84f75-215">Accelerate finding and analyzing your data by using combinations of keyboard shortcuts.</span></span> <span data-ttu-id="84f75-216">Por ejemplo, seleccione un campo, use **Mayús+Alt+F3** para agregar ese campo al panel de filtros, escriba los criterios de filtro, use **Ctrl+Intro** para volver a las filas, seleccione otro campo y use **Alt+F3** para filtrar ese valor.</span><span class="sxs-lookup"><span data-stu-id="84f75-216">For example, select a field, use **Shift+Alt+F3** to add that field to the filter pane, type the filter criteria, use **Ctrl+Enter** to return to the rows, select another field, and use **Alt+F3** to filter to that value.</span></span> <span data-ttu-id="84f75-217">Para obtener más información, consulte [Métodos abreviados de teclado](keyboard-shortcuts.md#KeyboardFilter).</span><span class="sxs-lookup"><span data-stu-id="84f75-217">For more information, see [Keyboard Shortcuts](keyboard-shortcuts.md#KeyboardFilter).</span></span>

### <a name="filter-criteria-and-operators"></a><span data-ttu-id="84f75-218"><a name="FilterCriteria"> </a>Criterios y operadores de filtro</span><span class="sxs-lookup"><span data-stu-id="84f75-218"><a name="FilterCriteria"> </a>Filter Criteria and Operators</span></span>

<span data-ttu-id="84f75-219">Al introducir criterios, puede usar todos los números y las letras que normalmente se emplean en un campo.</span><span class="sxs-lookup"><span data-stu-id="84f75-219">When you enter criteria, you can use all the numbers and letters that you normally use in the field.</span></span> <span data-ttu-id="84f75-220">Pero también hay un conjunto de símbolos especiales que puede usar como operadores para filtrar aún más los resultados.</span><span class="sxs-lookup"><span data-stu-id="84f75-220">But there's also a set of special symbols that you can use as operators to further filter the results.</span></span> <span data-ttu-id="84f75-221">Las siguientes secciones describen estos símbolos y cómo usarlos como operadores en filtros.</span><span class="sxs-lookup"><span data-stu-id="84f75-221">The following sections describe these symbols and how to use them as operators in filters.</span></span>

> [!TIP]
> <span data-ttu-id="84f75-222">Para obtener más información sobre el filtrado de fecha y hora, consulte [Trabajar con fechas y horas del calendario](ui-enter-date-ranges.md).</span><span class="sxs-lookup"><span data-stu-id="84f75-222">For more information about filtering dates and times, see [Working with Calendar Dates and Times](ui-enter-date-ranges.md).</span></span>

> [!IMPORTANT]
> - <span data-ttu-id="84f75-223">Puede haber situaciones en las que el valor por el que desea filtrar contiene un símbolo que es un operador.</span><span class="sxs-lookup"><span data-stu-id="84f75-223">There may be situations where the value that you want to filter on contains a symbol that's an operator.</span></span> <span data-ttu-id="84f75-224">Para obtener más información sobre cómo manejar estas situaciones, consulte [Filtrado por valores que contienen símbolos](#symbols) para obtener más instrucciones sobre cómo manejar esta situación.</span><span class="sxs-lookup"><span data-stu-id="84f75-224">For more information about handling these situtions, see [Filtering on Values That Contain Symbols](#symbols) for more instructions about handling this situation.</span></span>
>
> - <span data-ttu-id="84f75-225">Si hay más de 200 operadores en un solo filtro, el sistema agrupará automáticamente algunas expresiones entre paréntesis `()` con el fin de procesarlas.</span><span class="sxs-lookup"><span data-stu-id="84f75-225">If there are more than 200 operators in a single filter, the system will automatically group some expressions in parentheses `()` for the purpose of processing.</span></span> <span data-ttu-id="84f75-226">Esto no tiene ningún efecto en el filtro ni en los resultados.</span><span class="sxs-lookup"><span data-stu-id="84f75-226">This has no effect on the filter or the results.</span></span>  

#### <a name="-interval"></a><span data-ttu-id="84f75-227">(..) Intervalo</span><span class="sxs-lookup"><span data-stu-id="84f75-227">(..) Interval</span></span>

|<span data-ttu-id="84f75-228">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="84f75-228">Sample Expression</span></span>|<span data-ttu-id="84f75-229">Registros mostrados</span><span class="sxs-lookup"><span data-stu-id="84f75-229">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`1100..2100`|<span data-ttu-id="84f75-230">Números del 1100 al 2100.</span><span class="sxs-lookup"><span data-stu-id="84f75-230">Numbers 1100 through 2100</span></span>|  
|`..2500`|<span data-ttu-id="84f75-231">Hasta la 2500 inclusive</span><span class="sxs-lookup"><span data-stu-id="84f75-231">Up to and including 2500</span></span>|  
|`..12 31 00`|<span data-ttu-id="84f75-232">Fechas hasta el 31 12 00, inclusive.</span><span class="sxs-lookup"><span data-stu-id="84f75-232">Dates up to and including 12 31 00</span></span>|  
|`P8..`|<span data-ttu-id="84f75-233">Información correspondiente al ejercicio económico 8 y posteriores</span><span class="sxs-lookup"><span data-stu-id="84f75-233">Information for accounting period 8 and after</span></span>|  
|`..23`|<span data-ttu-id="84f75-234">Desde la fecha inicial hasta 23-mes actual-año actual 23:59:59</span><span class="sxs-lookup"><span data-stu-id="84f75-234">From the beginning date until 23-current month-current year 23:59:59</span></span>|  
|`23..`|<span data-ttu-id="84f75-235">Desde 23-mes actual-año actual 0:00:00 hasta la hora final</span><span class="sxs-lookup"><span data-stu-id="84f75-235">From 23-current month-current year 0:00:00 until the end of time</span></span>|  
|`22..23`|<span data-ttu-id="84f75-236">Desde 22-mes actual-año actual 0:00:00 hasta 23-mes actual-año actual 23:59:59</span><span class="sxs-lookup"><span data-stu-id="84f75-236">From 22-current month-current year 0:00:00 until 23-current month-current year 23:59:59</span></span>|  

#### <a name="124-eitheror"></a><span data-ttu-id="84f75-237">(&#124;) O/o</span><span class="sxs-lookup"><span data-stu-id="84f75-237">(&#124;) Either/or</span></span>

|<span data-ttu-id="84f75-238">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="84f75-238">Sample Expression</span></span>|<span data-ttu-id="84f75-239">Registros mostrados</span><span class="sxs-lookup"><span data-stu-id="84f75-239">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`1200|1300`|<span data-ttu-id="84f75-240">Números con 1200 ó 1300</span><span class="sxs-lookup"><span data-stu-id="84f75-240">Numbers with 1200 or 1300</span></span>|  

#### <a name="-not-equal-to"></a><span data-ttu-id="84f75-241">(<>) Distinto</span><span class="sxs-lookup"><span data-stu-id="84f75-241">(<>) Not equal to</span></span>  

|<span data-ttu-id="84f75-242">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="84f75-242">Sample Expression</span></span>|<span data-ttu-id="84f75-243">Registros mostrados</span><span class="sxs-lookup"><span data-stu-id="84f75-243">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`<>0`|<span data-ttu-id="84f75-244">Todos los números, excepto el 0</span><span class="sxs-lookup"><span data-stu-id="84f75-244">All numbers except 0</span></span><br /><br /> <span data-ttu-id="84f75-245">La opción SQL Server permite combinar este símbolo con una expresión de caracteres comodín.</span><span class="sxs-lookup"><span data-stu-id="84f75-245">The SQL Server Option allows you to combine this symbol with a wild-card expression.</span></span> <span data-ttu-id="84f75-246">Por ejemplo, <>A\* significa distinto de cualquier texto que empiece por A.</span><span class="sxs-lookup"><span data-stu-id="84f75-246">For example, <>A\* meaning not equal to any text that starts with A.</span></span>|  

#### <a name="-greater-than"></a><span data-ttu-id="84f75-247">(>) Mayor de</span><span class="sxs-lookup"><span data-stu-id="84f75-247">(>) Greater than</span></span>  

|<span data-ttu-id="84f75-248">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="84f75-248">Sample Expression</span></span>|<span data-ttu-id="84f75-249">Registros mostrados</span><span class="sxs-lookup"><span data-stu-id="84f75-249">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`>1200`|<span data-ttu-id="84f75-250">Números mayores que 1200</span><span class="sxs-lookup"><span data-stu-id="84f75-250">Numbers greater than 1200</span></span>|  

#### <a name="-greater-than-or-equal-to"></a><span data-ttu-id="84f75-251">(>=) Mayor o igual a</span><span class="sxs-lookup"><span data-stu-id="84f75-251">(>=) Greater than or equal to</span></span>  

|<span data-ttu-id="84f75-252">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="84f75-252">Sample Expression</span></span>|<span data-ttu-id="84f75-253">Registros mostrados</span><span class="sxs-lookup"><span data-stu-id="84f75-253">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`>=1200`|<span data-ttu-id="84f75-254">Números mayores o igual que 1200</span><span class="sxs-lookup"><span data-stu-id="84f75-254">Numbers greater than or equal to 1200</span></span>|  

#### <a name="-less-than"></a><span data-ttu-id="84f75-255">(<) Menor de</span><span class="sxs-lookup"><span data-stu-id="84f75-255">(<) Less than</span></span>  

|<span data-ttu-id="84f75-256">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="84f75-256">Sample Expression</span></span>|<span data-ttu-id="84f75-257">Registros mostrados</span><span class="sxs-lookup"><span data-stu-id="84f75-257">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`<1200`|<span data-ttu-id="84f75-258">Números menores que 1200</span><span class="sxs-lookup"><span data-stu-id="84f75-258">Numbers less than 1200</span></span>|  

#### <a name="-less-than-or-equal-to"></a><span data-ttu-id="84f75-259">(<=) Menor o igual que</span><span class="sxs-lookup"><span data-stu-id="84f75-259">(<=) Less than or equal to</span></span>  

|<span data-ttu-id="84f75-260">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="84f75-260">Sample Expression</span></span>|<span data-ttu-id="84f75-261">Registros mostrados</span><span class="sxs-lookup"><span data-stu-id="84f75-261">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`<=1200`|<span data-ttu-id="84f75-262">Números menores o iguales que 1200</span><span class="sxs-lookup"><span data-stu-id="84f75-262">Numbers less than or equal to 1200</span></span>|  

#### <a name="-and"></a><span data-ttu-id="84f75-263">(&) y</span><span class="sxs-lookup"><span data-stu-id="84f75-263">(&) And</span></span>  

|<span data-ttu-id="84f75-264">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="84f75-264">Sample Expression</span></span>|<span data-ttu-id="84f75-265">Registros mostrados</span><span class="sxs-lookup"><span data-stu-id="84f75-265">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`>200&<1200`|<span data-ttu-id="84f75-266">Números mayores de 200 e inferiores a 1200</span><span class="sxs-lookup"><span data-stu-id="84f75-266">Numbers greater than 200 and less than 1200</span></span>|  

#### <a name="-an-exact-character-match"></a><span data-ttu-id="84f75-267">(") Una coincidencia exacta de carácter</span><span class="sxs-lookup"><span data-stu-id="84f75-267">('') An exact character match</span></span>  

|<span data-ttu-id="84f75-268">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="84f75-268">Sample Expression</span></span>|<span data-ttu-id="84f75-269">Registros mostrados</span><span class="sxs-lookup"><span data-stu-id="84f75-269">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`'man'`|<span data-ttu-id="84f75-270">Texto que coincide exactamente con **man** y distingue mayúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="84f75-270">Text that matches **man** exactly and is case-sensitive.</span></span>|  

#### <a name="-case-insensitive"></a><span data-ttu-id="84f75-271">(@) Distinción entre mayúsculas y minúsculas</span><span class="sxs-lookup"><span data-stu-id="84f75-271">(@) Case insensitive</span></span>  

|<span data-ttu-id="84f75-272">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="84f75-272">Sample Expression</span></span>|<span data-ttu-id="84f75-273">Registros mostrados</span><span class="sxs-lookup"><span data-stu-id="84f75-273">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`@man*`|<span data-ttu-id="84f75-274">Texto que empieza por **man** y no distingue mayúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="84f75-274">Text that starts with **man** and is case insensitive.</span></span>|  

#### <a name="-an-indefinite-number-of-unknown-characters"></a><span data-ttu-id="84f75-275">(\*) Un número indefinido de caracteres desconocidos (quizás ninguno)</span><span class="sxs-lookup"><span data-stu-id="84f75-275">(\*) An indefinite number of unknown characters</span></span>

|<span data-ttu-id="84f75-276">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="84f75-276">Sample Expression</span></span>|<span data-ttu-id="84f75-277">Registros mostrados</span><span class="sxs-lookup"><span data-stu-id="84f75-277">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`*Co*`|<span data-ttu-id="84f75-278">Texto que contenga **Co** y es con diferenciación de mayúsculas y minúsculas.</span><span class="sxs-lookup"><span data-stu-id="84f75-278">Text that contains **Co** and is case-sensitive.</span></span>|  
|`*Co`|<span data-ttu-id="84f75-279">Texto que termine con **Co** y es con diferenciación de mayúsculas y minúsculas.</span><span class="sxs-lookup"><span data-stu-id="84f75-279">Text that ends with **Co"** and is case-sensitive.</span></span>|  
|`Co*`|<span data-ttu-id="84f75-280">Texto que empiece por **Co** y es con diferenciación de mayúsculas y minúsculas.</span><span class="sxs-lookup"><span data-stu-id="84f75-280">Text that begins with **Co** and is case-sensitive.</span></span>|  

#### <a name="-one-unknown-character"></a><span data-ttu-id="84f75-281">(?) Un carácter desconocido</span><span class="sxs-lookup"><span data-stu-id="84f75-281">(?) One unknown character</span></span>  

|<span data-ttu-id="84f75-282">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="84f75-282">Sample Expression</span></span>|<span data-ttu-id="84f75-283">Registros mostrados</span><span class="sxs-lookup"><span data-stu-id="84f75-283">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`Hans?n`|<span data-ttu-id="84f75-284">Texto como **Mendoza** o **Mendosa**</span><span class="sxs-lookup"><span data-stu-id="84f75-284">Text such as **Hansen** or **Hanson**</span></span>|  

#### <a name="combined-format-expressions"></a><span data-ttu-id="84f75-285">Expresiones de formato combinadas</span><span class="sxs-lookup"><span data-stu-id="84f75-285">Combined Format Expressions</span></span>  

|<span data-ttu-id="84f75-286">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="84f75-286">Sample Expression</span></span>|<span data-ttu-id="84f75-287">Registros mostrados</span><span class="sxs-lookup"><span data-stu-id="84f75-287">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`5999|8100..8490`|<span data-ttu-id="84f75-288">Incluye todos los registros cuyo número sea 5999 o un número entre 8100 y 8490.</span><span class="sxs-lookup"><span data-stu-id="84f75-288">Include any records with the number 5999 or a number from the interval 8100 through 8490.</span></span>|  
|`..1299|1400..`|<span data-ttu-id="84f75-289">Incluye los registros cuyo número sea menor o igual que 1299 o un número igual o mayor que 1400</span><span class="sxs-lookup"><span data-stu-id="84f75-289">Include records with a number less than or equal to 1299 or a number equal to 1400 or greater (all numbers except 1300 through 1399).</span></span>|  
|`>50&<100`|<span data-ttu-id="84f75-290">Incluye los registros cuyo número sea mayor que 50 y menor que 100.</span><span class="sxs-lookup"><span data-stu-id="84f75-290">Include records with numbers that are greater than 50 and less than 100 (numbers 51 through 99).</span></span>|  

### <a name="filtering-on-values-that-contain-symbols"></a><a name="symbols"></a><span data-ttu-id="84f75-291">Filtrado por valores que contienen símbolos</span><span class="sxs-lookup"><span data-stu-id="84f75-291">Filtering on Values That Contain Symbols</span></span>

<span data-ttu-id="84f75-292">Puede haber casos en los que los valores de campo contengan uno de los siguientes símbolos:</span><span class="sxs-lookup"><span data-stu-id="84f75-292">There may be cases where field values contain the one of the following symbols:</span></span>

- &
- <span data-ttu-id="84f75-293">(</span><span class="sxs-lookup"><span data-stu-id="84f75-293">(</span></span>
- <span data-ttu-id="84f75-294">)</span><span class="sxs-lookup"><span data-stu-id="84f75-294">)</span></span>
- =
- <span data-ttu-id="84f75-295">&#124;</span><span class="sxs-lookup"><span data-stu-id="84f75-295">&#124;</span></span>

<span data-ttu-id="84f75-296">Si desea filtrar por cualquiera de estos símbolos, coloque la expresión de filtro entre comillas ('').</span><span class="sxs-lookup"><span data-stu-id="84f75-296">If you want to filter on any of these symbols, place the filter expression in quotation marks ('').</span></span> <span data-ttu-id="84f75-297">Por ejemplo, si desease filtrar en los registros que comienzan por el texto *J & V*, la expresión de filtro sería `'J & V*'`.</span><span class="sxs-lookup"><span data-stu-id="84f75-297">For example, if you wanted to filter on records that start with the text *J & V*, the filter expression would be `'J & V*'`.</span></span>

<span data-ttu-id="84f75-298">Este requisito no es necesario para otros símbolos.</span><span class="sxs-lookup"><span data-stu-id="84f75-298">This requirement isn't necessary for other symbols.</span></span>

### <a name="filter-tokens"></a><span data-ttu-id="84f75-299"><a name="FilterTokens"> </a>Tokens de filtro</span><span class="sxs-lookup"><span data-stu-id="84f75-299"><a name="FilterTokens"> </a>Filter Tokens</span></span>

<span data-ttu-id="84f75-300">Al introducir criterios de filtro, también puede escribir palabras que tengan un significado especial, lo que se conoce como tokens de filtro.</span><span class="sxs-lookup"><span data-stu-id="84f75-300">When entering filter criteria, you can also type words that have special meaning, called filter tokens.</span></span> <span data-ttu-id="84f75-301">Después de introducir la palabra token, la palabra se reemplaza por el valor o valores que representa.</span><span class="sxs-lookup"><span data-stu-id="84f75-301">After entering the token word, the word is replaced by the value or values that it represents.</span></span> <span data-ttu-id="84f75-302">Los tokens de filtro facilitan el filtrado al reducir la necesidad de ir a otras páginas para buscar los valores que desea agregar a su filtro.</span><span class="sxs-lookup"><span data-stu-id="84f75-302">Filter tokens make filtering easier by reducing the need to navigate to other pages to look up values you want to add to your filter.</span></span> <span data-ttu-id="84f75-303">En las tablas siguientes se describen algunos de los tokens que puede escribir como criterios de filtro.</span><span class="sxs-lookup"><span data-stu-id="84f75-303">The tables below describe some of the tokens you can type as filter criteria.</span></span>

> [!TIP]
> <span data-ttu-id="84f75-304">Su organización puede usar tokens personalizados.</span><span class="sxs-lookup"><span data-stu-id="84f75-304">Your organization may use custom tokens.</span></span> <span data-ttu-id="84f75-305">Para obtener información sobre el conjunto completo de tokens disponibles o para agregar más tokens personalizados, hable con su administrador.</span><span class="sxs-lookup"><span data-stu-id="84f75-305">To learn about the complete set of tokens available to you or to add more custom tokens, talk to your administrator.</span></span> <span data-ttu-id="84f75-306">Para obtener información técnica, consulte [Agregar tokens de filtro](/dynamics365/business-central/dev-itpro/developer/devenv-adding-filter-tokens).</span><span class="sxs-lookup"><span data-stu-id="84f75-306">For technical information see [Adding Filter Tokens](/dynamics365/business-central/dev-itpro/developer/devenv-adding-filter-tokens).</span></span>

#### <a name="me-or-userid-records-assigned-to-you"></a><span data-ttu-id="84f75-307">(%me o %userid) Registros que se le han asignado</span><span class="sxs-lookup"><span data-stu-id="84f75-307">(%me or %userid) Records Assigned to You</span></span>

<span data-ttu-id="84f75-308">Utilice `%me` o `%userid` cuando filtre campos que contengan el ID de usuario, como el campo **Asignado a ID de usuario**, para mostrar todos los registros que se le asignaron.</span><span class="sxs-lookup"><span data-stu-id="84f75-308">Use `%me` or `%userid` when filtering fields that contain the user ID, such as **Assigned to User ID** field, to display all records that are assigned to you.</span></span>

|<span data-ttu-id="84f75-309">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="84f75-309">Sample Expression</span></span>|<span data-ttu-id="84f75-310">Registros mostrados</span><span class="sxs-lookup"><span data-stu-id="84f75-310">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`%me`<br /><span data-ttu-id="84f75-311">o</span><span class="sxs-lookup"><span data-stu-id="84f75-311">or</span></span><br />`%userid`|<span data-ttu-id="84f75-312">Registros que se han asignado a su cuenta.</span><span class="sxs-lookup"><span data-stu-id="84f75-312">Records that are assigned to your user account.</span></span> |  

#### <a name="mycustomers-customers-in-my-customers"></a><span data-ttu-id="84f75-313">(%mycustomers) Clientes en Mis clientes</span><span class="sxs-lookup"><span data-stu-id="84f75-313">(%mycustomers) Customers in My Customers</span></span>

<span data-ttu-id="84f75-314">Use `%mycustomers` en el campo de cliente **No** para mostrar todos los registros de los clientes que se incluyen en la lista **Mis clientes** en su Área de trabajo.</span><span class="sxs-lookup"><span data-stu-id="84f75-314">Use `%mycustomers` in the customer **No** field to display all records for customers that are included in the **My Customers** list on your Role Center.</span></span>

|<span data-ttu-id="84f75-315">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="84f75-315">Sample Expression</span></span>|<span data-ttu-id="84f75-316">Registros mostrados</span><span class="sxs-lookup"><span data-stu-id="84f75-316">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`%mycustomers`|<span data-ttu-id="84f75-317">Clientes en **Mis clientes** en el Área de trabajo.</span><span class="sxs-lookup"><span data-stu-id="84f75-317">Customers in the **My Customers** on your Role Center.</span></span> |  

#### <a name="myitems-items-in-my-items"></a><span data-ttu-id="84f75-318">(%myitems) Artículos en Mis artículos</span><span class="sxs-lookup"><span data-stu-id="84f75-318">(%myitems) Items in My Items</span></span>

<span data-ttu-id="84f75-319">Use `%myitems` en el campo de artículo **No** para mostrar todos los registros de los artículos que se incluyen en la lista **Mis artículos** en su Área de trabajo.</span><span class="sxs-lookup"><span data-stu-id="84f75-319">Use `%myitems` in the item **No** field to display all records for items that are included in the **My Items** list on your Role Center.</span></span>

|<span data-ttu-id="84f75-320">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="84f75-320">Sample Expression</span></span>|<span data-ttu-id="84f75-321">Registros mostrados</span><span class="sxs-lookup"><span data-stu-id="84f75-321">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`%myitems`|<span data-ttu-id="84f75-322">Artículos en **Mis artículos** en el Área de trabajo.</span><span class="sxs-lookup"><span data-stu-id="84f75-322">Items in the **My Items** on your Role Center.</span></span> |  

#### <a name="myvendors-vendors-in-my-vendors"></a><span data-ttu-id="84f75-323">(%myvendors) Proveedores en Mis proveedores</span><span class="sxs-lookup"><span data-stu-id="84f75-323">(%myvendors) Vendors in My Vendors</span></span>

<span data-ttu-id="84f75-324">Use `%myvendors` en el campo de proveedor **No** para mostrar todos los registros de los proveedores que se incluyen en la lista **Mis proveedores** en su Área de trabajo.</span><span class="sxs-lookup"><span data-stu-id="84f75-324">Use `%myvendors` in the vendor **No** field to display all records for vendors that are included in the **My Vendors** list on your Role Center.</span></span>

|<span data-ttu-id="84f75-325">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="84f75-325">Sample Expression</span></span>|<span data-ttu-id="84f75-326">Registros mostrados</span><span class="sxs-lookup"><span data-stu-id="84f75-326">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`%myvendors`|<span data-ttu-id="84f75-327">Proveedores en **Mis proveedores** en el Área de trabajo.</span><span class="sxs-lookup"><span data-stu-id="84f75-327">Vendors in the **My Vendors** on your Role Center.</span></span> |  

## <a name="see-also"></a><span data-ttu-id="84f75-328">Consulte también</span><span class="sxs-lookup"><span data-stu-id="84f75-328">See Also</span></span>

[<span data-ttu-id="84f75-329">Preguntas frecuentes sobre buscar y filtrar</span><span class="sxs-lookup"><span data-stu-id="84f75-329">Searching and Filtering FAQ</span></span>](ui-search-filter-faq.md)  
[<span data-ttu-id="84f75-330">Guardar y personalizar vistas de lista</span><span class="sxs-lookup"><span data-stu-id="84f75-330">Save and Personalize List Views</span></span>](ui-views.md)  
<span data-ttu-id="84f75-331">[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="84f75-331">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>  


[!INCLUDE[footer-include](includes/footer-banner.md)]