---
title: Ordenar, buscar y filtrar listas | Documentos de Microsoft
description: Trabaje de manera eficiente en las listas buscando en sus datos, clasificando columnas y refinando los resultados utilizando potentes símbolos de filtrado y atajos de teclado.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: delimit, FlowFilter, totals, limit, advanced
ms.date: 04/01/2019
ms.author: jswymer
ms.openlocfilehash: 5cd8bce29b1973274cda673e22dd07e6b50f830f
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/29/2019
ms.locfileid: "1253958"
---
# <a name="sorting-searching-and-filtering-lists"></a><span data-ttu-id="345f9-103">Ordenar, buscar y filtrar listas</span><span class="sxs-lookup"><span data-stu-id="345f9-103">Sorting, Searching, and Filtering Lists</span></span>
<span data-ttu-id="345f9-104">Existen algunos parámetros que puede configurar que le ayudarán a buscar, encontrar y limitar los registros de una lista.</span><span class="sxs-lookup"><span data-stu-id="345f9-104">There are a few things that you can do that will help you scan, find, and limit records in a list.</span></span> <span data-ttu-id="345f9-105">Éstos incluyen la ordenación, busqueda y filtrando.</span><span class="sxs-lookup"><span data-stu-id="345f9-105">These include sorting, searching and filtering.</span></span> <span data-ttu-id="345f9-106">Puede aplicar solo algunos o todos a la vez para encontrar o analizar rápidamente sus datos.</span><span class="sxs-lookup"><span data-stu-id="345f9-106">You can apply some or all of these simultaneously to quickly find or analyze your data.</span></span>

> [!TIP]
> <span data-ttu-id="345f9-107">Al ver los datos como mosaicos, puede buscar y usar el filtrado básico.</span><span class="sxs-lookup"><span data-stu-id="345f9-107">When viewing your data as tiles, you can search and use basic filtering.</span></span> <span data-ttu-id="345f9-108">Para usar el conjunto completo de potentes funciones para ordenar, buscar y filtrar, elija el icono ![Mostrar como lista](media/ui_show_as_list_icon.png "Flecha izquierda para Mostrar como lista") para mostrar como una lista.</span><span class="sxs-lookup"><span data-stu-id="345f9-108">To use the full set of powerful features for sorting, searching and filtering, choose the ![Show as list](media/ui_show_as_list_icon.png "Show as list arrow left") icon to show as a list.</span></span>

<!--
When you want to search for data, such as customer names, addresses, or product groups, you enter criteria. In search criteria you can use all the numbers and letters that you normally use in the specific field. In addition, you can use special symbols to further filter the results. There are two ways to search: using the Quick Filter or column filters.
-->

## <a name="sorting"></a><span data-ttu-id="345f9-109">Ordenación</span><span class="sxs-lookup"><span data-stu-id="345f9-109">Sorting</span></span>
<span data-ttu-id="345f9-110">La ordenación facilita la obtención rápida de un resumen de sus datos.</span><span class="sxs-lookup"><span data-stu-id="345f9-110">Sorting makes it easy for you to get a quick overview of your data.</span></span> <span data-ttu-id="345f9-111">Si hay varios clientes, por ejemplo, puede elegir ordenarlos por **N.º de cliente**, **Grupo contable cliente**, **Cód. divisa**, **Cód. país/región** o **N.º de registro de impuesto sobre las ventas** para disponer de la vista general que desea.</span><span class="sxs-lookup"><span data-stu-id="345f9-111">If you have many customers, for example, you can choose to sort them by **Customer No.**, **Customer Posting Group**, **Currency Code**, **Country Region Code**, or **Sales Tax Registration No.** to get the overview you need.</span></span>

<span data-ttu-id="345f9-112">Para ordenar una lista, puede elegir un texto de cabecera de columna para alternar entre el pedido ascendente y descendente o elegir la flecha pequeña hacia abajo de la cabecera de columna y, a continuación elegir **Ascendente** o **Descendente**.</span><span class="sxs-lookup"><span data-stu-id="345f9-112">To sort a list, you can either choose a column heading text to toggle between ascending and descending order, or choose the small down arrow in the column heading, and then choose **Ascending** or **Descending**.</span></span>  

> [!NOTE]  
>   <span data-ttu-id="345f9-113">El ordenamiento no se admite en imágenes, campos BLOB, FlowFilters ni campos que no pertenecen a una tabla.</span><span class="sxs-lookup"><span data-stu-id="345f9-113">Sorting is not supported on images, BLOB fields, FlowFilters, and fields that do not belong to a table.</span></span>  

## <a name="searching"></a><span data-ttu-id="345f9-114">Búsqueda</span><span class="sxs-lookup"><span data-stu-id="345f9-114">Searching</span></span>
<!--## Searching by using the Quick Filter -->
<span data-ttu-id="345f9-115">En la parte superior de cada página de la lista, hay un icono de ![Buscar en la lista](media/ui-search/search-list.png "icono de Buscar en la lista") **Buscar** que proporciona una manera rápida y fácil de reducir los registros en una lista y muestra solo aquellos registros que contienen los datos que le interesa ver.</span><span class="sxs-lookup"><span data-stu-id="345f9-115">At the top of each list page, there is a ![Search list](media/ui-search/search-list.png "Search list icon") **Search** icon that provides a quick and easy way to reduce the records in a list and display only those records that contain the data that you are interested in seeing.</span></span>

<span data-ttu-id="345f9-116">Para buscar, simplemente seleccione el icono de búsqueda y luego, en el cuadro, escriba el texto que está buscando.</span><span class="sxs-lookup"><span data-stu-id="345f9-116">To search, simply select the search icon, and then in the box, type the text that you are looking for.</span></span> <span data-ttu-id="345f9-117">Puede escribir letras, números y otros símbolos.</span><span class="sxs-lookup"><span data-stu-id="345f9-117">You can enter letters, numbers, and other symbols.</span></span>

### <a name="fine-tune-the-search"></a><span data-ttu-id="345f9-118">Afinar la búsqueda</span><span class="sxs-lookup"><span data-stu-id="345f9-118">Fine-tune the Search</span></span>
<span data-ttu-id="345f9-119">En general, la búsqueda intentará hacer coincidir el texto en todos los campos; no distingue entre mayúsculas y minúsculas y coincidirá con el texto colocado en algún lugar del campo (al principio, al final o en el centro).</span><span class="sxs-lookup"><span data-stu-id="345f9-119">In general, search will attempt to match text across all fields; it does not distinguish between uppercase and lowercase characters (in other words, case insensitive), and will match text placed anwhere in the field (at the beginning, end, or in the middle).</span></span>

<span data-ttu-id="345f9-120">Sin embargo, puede realizar una búsqueda más exacta utilizando los siguientes caracteres especiales:</span><span class="sxs-lookup"><span data-stu-id="345f9-120">However, you can make a more exact search by using the following special characters:</span></span>

- <span data-ttu-id="345f9-121">Para buscar solo valores de campo que coincidan exactamente con el texto completo y el caso, coloque el texto de búsqueda entre comillas simples `''` (por ejemplo, `'man'`).</span><span class="sxs-lookup"><span data-stu-id="345f9-121">To find only field values that match the entire text and case exactly, place the search text between single quotes `''` (for example, `'man'`).</span></span>

- <span data-ttu-id="345f9-122">Para buscar valores de campo que comiencen con un determinado texto y coincidan con el caso, coloque `*` después del texto de búsqueda (por ejemplo, `man*`).</span><span class="sxs-lookup"><span data-stu-id="345f9-122">To find field values that start with a certain text and match the case, place `*` after the search text (for example `man*`).</span></span>

- <span data-ttu-id="345f9-123">Para buscar valores de campo que acaben con un determinado texto y coincidan con el caso, coloque `*` antes del texto de búsqueda (por ejemplo, `*man`).</span><span class="sxs-lookup"><span data-stu-id="345f9-123">To find field values that end with a certain text and match the case, place `*` before the search text (for example `*man`).</span></span>

- <span data-ttu-id="345f9-124">Cuando se utiliza `''` o `*`, la búsqueda distingue entre mayúsculas y minúsculas.</span><span class="sxs-lookup"><span data-stu-id="345f9-124">When using  `''` or `*`, the search is case sensitive.</span></span> <span data-ttu-id="345f9-125">Si desea que la búsqueda no distinga entre mayúsculas y minúsculas, coloque `@` antes del texto de búsqueda (por ejemplo, `@man*`).</span><span class="sxs-lookup"><span data-stu-id="345f9-125">If you want to make the search case insensitive, place `@` before the search text (for example `@man*`).</span></span>

<span data-ttu-id="345f9-126">En la tabla siguiente se muestran algunos ejemplos de cómo puede utilizar la búsqueda.</span><span class="sxs-lookup"><span data-stu-id="345f9-126">The following table provides some examples to explain how you can use the search.</span></span>

|<span data-ttu-id="345f9-127">Criterios de búsqueda</span><span class="sxs-lookup"><span data-stu-id="345f9-127">Search Criteria</span></span>|<span data-ttu-id="345f9-128">Búsquedas…</span><span class="sxs-lookup"><span data-stu-id="345f9-128">Finds...</span></span>|
|---------------|----------|
|`man`<br /><span data-ttu-id="345f9-129">o</span><span class="sxs-lookup"><span data-stu-id="345f9-129">or</span></span> <br />`Man`|<span data-ttu-id="345f9-130">Todos los registros con los campos que contienen el texto **man**, independientemente de las mayúsculas y minúsculas.</span><span class="sxs-lookup"><span data-stu-id="345f9-130">All records with fields that contain the text **man**, regardless of the case.</span></span> <span data-ttu-id="345f9-131">Por ejemplo, **Manchester**, **manual** o **Norman**.</span><span class="sxs-lookup"><span data-stu-id="345f9-131">For example, **Manchester**, **manual**, or **Sportsman**.</span></span> |
|`'Man'`|<span data-ttu-id="345f9-132">Todos los registros con los campos que contienen solo el texto **Man** y coinciden las mayúsculas y minúsculas.</span><span class="sxs-lookup"><span data-stu-id="345f9-132">All records with fields that contain only **Man**, matching the case.</span></span>|
|`Man*`|<span data-ttu-id="345f9-133">Todos los registros con los campos que empiezan por <b>Man</b> y coinciden las mayúsculas y minúsculas.</span><span class="sxs-lookup"><span data-stu-id="345f9-133">All records with fields that start with the text <b>Man</b>, matching the case.</span></span> <span data-ttu-id="345f9-134">Por ejemplo, **Manchester** pero no **manual** o **Norman**.</span><span class="sxs-lookup"><span data-stu-id="345f9-134">For example, **Manchester** but not **manual** or **Sportsman**.</span></span>|
|`@Man*`|<span data-ttu-id="345f9-135">Todos los registros con los campos que empiezan por **man** independientemente de las mayúsculas y minúsculas.</span><span class="sxs-lookup"><span data-stu-id="345f9-135">All records with fields that start with **man**, regardless of the case.</span></span> <span data-ttu-id="345f9-136">Por ejemplo, **Manchester** y **manual** pero no **Norman**.</span><span class="sxs-lookup"><span data-stu-id="345f9-136">For example, **Manchester** and **manual**, but not **Sportsman**.</span></span>|
|`@*man`|<span data-ttu-id="345f9-137">Todos los registros que acaban por **man** independientemente de las mayúsculas y minúsculas.</span><span class="sxs-lookup"><span data-stu-id="345f9-137">All records that end with **man**, regardless of the case.</span></span> <span data-ttu-id="345f9-138">Por ejemplo, **Norman** pero no **Manchester** o **manual**.</span><span class="sxs-lookup"><span data-stu-id="345f9-138">For example **Sportsman**, but not **Manchester** or **manual**.</span></span>|

> [!TIP]
> <span data-ttu-id="345f9-139">Puede presionar F3 para activar y desactivar el cuadro de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="345f9-139">You can press F3 to activate and deactivate the search box.</span></span> <span data-ttu-id="345f9-140">Para obtener más información, consulte [Métodos abreviados de teclado](keyboard-shortcuts.md#KeyboardFilter).</span><span class="sxs-lookup"><span data-stu-id="345f9-140">For more information see [Keyboard Shortcuts](keyboard-shortcuts.md#KeyboardFilter).</span></span>

## <span data-ttu-id="345f9-141"><a name="Filtering"> </a>Filtrado</span><span class="sxs-lookup"><span data-stu-id="345f9-141"><a name="Filtering"> </a>Filtering</span></span>
<span data-ttu-id="345f9-142">El filtrado proporciona una forma más avanzada y versátil de controlar qué registros se muestran en una lista.</span><span class="sxs-lookup"><span data-stu-id="345f9-142">Filtering provides a more advanced and versatile way of controlling which records display in a list.</span></span> <span data-ttu-id="345f9-143">Existen dos diferencias principales entre la búsqueda y el filtrado, como se describe en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="345f9-143">There are two major differences between searching and filtering, as described in the table below.</span></span>

|| <span data-ttu-id="345f9-144">**Búsqueda**</span><span class="sxs-lookup"><span data-stu-id="345f9-144">**Searching**</span></span> | <span data-ttu-id="345f9-145">**Filtrado**</span><span class="sxs-lookup"><span data-stu-id="345f9-145">**Filtering**</span></span> |
|--|----------|------------|
| <span data-ttu-id="345f9-146">**Campos aplicables**</span><span class="sxs-lookup"><span data-stu-id="345f9-146">**Applicable fields**</span></span> | <span data-ttu-id="345f9-147">Busca en todos los campos que están visibles en la página.</span><span class="sxs-lookup"><span data-stu-id="345f9-147">Searches across all fields that are visible on the page.</span></span> | <span data-ttu-id="345f9-148">Filtra uno o más campos individualmente, los selecciona desde cualquier campo de la tabla, incluidos los campos que no están visibles en la página.</span><span class="sxs-lookup"><span data-stu-id="345f9-148">Filters one or more fields individually, selecting from any field on the table, including fields that are not visible on the page.</span></span> |
| <span data-ttu-id="345f9-149">**Coincidencia**</span><span class="sxs-lookup"><span data-stu-id="345f9-149">**Matching**</span></span> | <span data-ttu-id="345f9-150">Muestra registros con campos que coinciden con el texto de búsqueda, independientemente de las mayúsculas o la ubicación de ese texto.</span><span class="sxs-lookup"><span data-stu-id="345f9-150">Displays records with fields that match the search text, irrespective of casing or placement of that text.</span></span> | <span data-ttu-id="345f9-151">Muestra los registros en los que el campo coincide exactamente con el filtro y distingue entre mayúsculas y minúsculas, a menos que se introduzcan símbolos de filtrado especiales.</span><span class="sxs-lookup"><span data-stu-id="345f9-151">Displays records where the field matches the filter exactly and is case sensitive, unless special filter symbols are entered.</span></span>

<span data-ttu-id="345f9-152">El filtrado le permite mostrar registros de cuentas o clientes específicos, fechas, importes y otra información especificando criterios de filtro.</span><span class="sxs-lookup"><span data-stu-id="345f9-152">Filtering enables you to display records for specific accounts or customers, dates, amounts, and other information by specifying filter criteria.</span></span> <span data-ttu-id="345f9-153">Únicamente se mostrarán los registros que coincidan con los criterios.</span><span class="sxs-lookup"><span data-stu-id="345f9-153">Only records that match the criteria are displayed.</span></span> <span data-ttu-id="345f9-154">Si especifica criterios para varios campos, solo se mostrarán los registros que coincidan con todos los criterios.</span><span class="sxs-lookup"><span data-stu-id="345f9-154">If you specify criteria for multiple fields, then only records that match all criteria will be displayed.</span></span>

### <a name="working-in-the-filter-pane"></a><span data-ttu-id="345f9-155">Trabajar en el panel de filtros</span><span class="sxs-lookup"><span data-stu-id="345f9-155">Working in the Filter Pane</span></span>

<span data-ttu-id="345f9-156">Para mostrar el panel de filtros, seleccione ![Icono Panel de filtros](media/open-filter-pane-icon.png "Icono Panel de filtros") en la parte superior de la lista o pulse **Mayús+F3**.</span><span class="sxs-lookup"><span data-stu-id="345f9-156">To display the filter pane, select ![Filter pane icon](media/open-filter-pane-icon.png "Filter pane icon") at the top of the list or press **Shift+F3**.</span></span> <span data-ttu-id="345f9-157">Para las listas del Área de trabajo, también puede elegir la flecha hacia abajo cerca del título de la página en la barra de navegación que se encuentra sobre la lista, y luego seleccionar **Mostrar panel de filtros**, tal como se muestra aquí:</span><span class="sxs-lookup"><span data-stu-id="345f9-157">For lists within the Role Center, you can also choose the down arrow near the page title in the navigation bar above the list, and then choose **Show filter pane** as shown here:</span></span>

<span data-ttu-id="345f9-158">![Mostrar panel de filtros](media/open-filter-pane.png "Mostrar panel de filtros")</span><span class="sxs-lookup"><span data-stu-id="345f9-158">![Show filter pane](media/open-filter-pane.png "Show filter pane")</span></span>

<span data-ttu-id="345f9-159">El panel de filtros muestra los filtros actuales para una lista y le permite configurar sus propios filtros personalizados en uno o más campos.</span><span class="sxs-lookup"><span data-stu-id="345f9-159">The filter pane displays the current filters for a list, and enables you to set your own custom filters on one or more fields.</span></span> <span data-ttu-id="345f9-160">La siguiente ilustración muestra un panel de filtros de ejemplo para una lista de Ofertas de venta.</span><span class="sxs-lookup"><span data-stu-id="345f9-160">The following figure shows an example filter pane for a Sales Quotes list.</span></span>

<span data-ttu-id="345f9-161">![Vista general del panel de filtros ](media/filter-pane-overview.png "Icono de Filtros")</span><span class="sxs-lookup"><span data-stu-id="345f9-161">![Filter pane overview ](media/filter-pane-overview.png "Filter icon")</span></span>

<span data-ttu-id="345f9-162">Un panel de filtros se divide en tres secciones: **Vistas**, **Filtrar lista por** y **Filtrar totales por**:</span><span class="sxs-lookup"><span data-stu-id="345f9-162">A filter pane is divided in three sections: **Views**, **Filter list by**, and **Filter totals by**:</span></span>

- <span data-ttu-id="345f9-163">**Vistas**</span><span class="sxs-lookup"><span data-stu-id="345f9-163">**Views**</span></span>

  <span data-ttu-id="345f9-164">Algunas listas incluyen la sección **Vistas**.</span><span class="sxs-lookup"><span data-stu-id="345f9-164">Some lists will include the **Views** section.</span></span> <span data-ttu-id="345f9-165">Las vistas son variaciones de la lista que se han preconfigurado con filtros.</span><span class="sxs-lookup"><span data-stu-id="345f9-165">Views are variations of the list that have been preconfigured with filters.</span></span> <span data-ttu-id="345f9-166">Para cambiar a una vista diferente de su lista, simplemente seleccione otro enlace.</span><span class="sxs-lookup"><span data-stu-id="345f9-166">To switch to a different view of your list, simply select another link.</span></span> <span data-ttu-id="345f9-167">Puede cambiar temporalmente los filtros en una vista, pero no se guardarán de forma permanente.</span><span class="sxs-lookup"><span data-stu-id="345f9-167">You can temporarily change the filters on a view, but the changes will not be permanently saved.</span></span>

- <span data-ttu-id="345f9-168">**Filtrar lista por**</span><span class="sxs-lookup"><span data-stu-id="345f9-168">**Filter list by**</span></span>

  <span data-ttu-id="345f9-169">La sección **Filtrar lista por** es donde se agregan filtros en campos específicos para reducir el número de registros mostrados.</span><span class="sxs-lookup"><span data-stu-id="345f9-169">The **Filter list by** section is where you add filters on specific fields to reduce the number of displayed records.</span></span> <span data-ttu-id="345f9-170">Para agregar un filtro, seleccione **+ Filtro**, seleccione el campo que desea filtrar desde cualquier campo de la tabla e introduzca los criterios de filtro en el cuadro.</span><span class="sxs-lookup"><span data-stu-id="345f9-170">To add a filter, select **+ Filter**, select the field that you want to filter from any field in the table, and then enter filter criteria in the box.</span></span>

- <span data-ttu-id="345f9-171">**Filtrar totales por**</span><span class="sxs-lookup"><span data-stu-id="345f9-171">**Filter totals by**</span></span>

  <span data-ttu-id="345f9-172">Algunas listas que muestran campos calculados, como cantidades e importes, incluyen la sección **Filtrar totales por**, donde puede ajustar varias dimensiones que influyen en los cálculos.</span><span class="sxs-lookup"><span data-stu-id="345f9-172">Some lists that display calculated fields, such as amounts and quantities, will include the **Filter totals by** section where you can adjust various dimensions that influence calculations.</span></span> <span data-ttu-id="345f9-173">Por ejemplo, puede analizar rápidamente su plan de cuentas filtrando los importes a un período específico, o puede ver los totales de los pedidos de ventas solo de un almacén específico.</span><span class="sxs-lookup"><span data-stu-id="345f9-173">For example, you can quickly analyze your chart of accounts by filtering amounts to a specific period, or you can view the totals for sales orders only from a specific warehouse.</span></span>

  <span data-ttu-id="345f9-174">Para agregar un filtro, seleccione **+ Filtro**, seleccione una de las dimensiones predefinidas y luego agregue los criterios de filtro en el cuadro.</span><span class="sxs-lookup"><span data-stu-id="345f9-174">To add a filter, select **+ Filter**, select one of the predefined dimensions, and then add the filter criteria in the box.</span></span>

  > [!NOTE]
  > <span data-ttu-id="345f9-175">FlowFilters es el encargado de controlar los filtros de la sección **Filtrar totales por** en el diseño de la página.</span><span class="sxs-lookup"><span data-stu-id="345f9-175">Filters in the **Filter totals by** section are controlled by FlowFilters on the page design.</span></span> <span data-ttu-id="345f9-176">Para obtener información técnica, vea [FlowFilters](https://docs.microsoft.com/en-us/dynamics365/business-central/dev-itpro/developer/devenv-flowfilter-overview).</span><span class="sxs-lookup"><span data-stu-id="345f9-176">For technical information, see [FlowFilters](https://docs.microsoft.com/en-us/dynamics365/business-central/dev-itpro/developer/devenv-flowfilter-overview).</span></span>


### <a name="entering-filter-criteria-in-the-filter-pane"></a><span data-ttu-id="345f9-177">Introducción de criterios de filtros en el panel de filtros</span><span class="sxs-lookup"><span data-stu-id="345f9-177">Entering Filter Criteria in the Filter Pane</span></span>
<span data-ttu-id="345f9-178">Para seleccionar un campo para filtrar, realice una de las siguientes acciones:</span><span class="sxs-lookup"><span data-stu-id="345f9-178">To select a field to filter, do one of the following:</span></span>
  - <span data-ttu-id="345f9-179">En el panel de filtros, seleccione **+ Campo**.</span><span class="sxs-lookup"><span data-stu-id="345f9-179">In the filter pane, choose **+ Field**.</span></span> <span data-ttu-id="345f9-180">Escriba el nombre del campo que desea filtrar o elija un campo del menú que muestra todos los campos de la tabla.</span><span class="sxs-lookup"><span data-stu-id="345f9-180">Type the name of the field you wish to filter, or pick a field from the menu that displays all fields in the table.</span></span>

  - <span data-ttu-id="345f9-181">En un encabezado de columna, elija la flecha hacia abajo y luego seleccione **Filtro...**. Se abrirá el panel de filtros y se agregará la columna al panel.</span><span class="sxs-lookup"><span data-stu-id="345f9-181">In a column heading, choose the down arrow, and then choose **Filter...**. This will open the filter pane and add the column to the filter pane.</span></span>

<span data-ttu-id="345f9-182">Ya puede escribir o seleccionar sus criterios de filtro en el cuadro.</span><span class="sxs-lookup"><span data-stu-id="345f9-182">You can now type or select your filter criteria in the box.</span></span> <span data-ttu-id="345f9-183">El tipo de campo que filtra determina qué criterios puede especificar.</span><span class="sxs-lookup"><span data-stu-id="345f9-183">The type of field you filter determines which criteria you can enter.</span></span> <span data-ttu-id="345f9-184">Por ejemplo, filtrar un campo que tiene valores fijos solo le permitirá elegir entre esos valores.</span><span class="sxs-lookup"><span data-stu-id="345f9-184">For example, filtering a field that has fixed values will only let you choose from those values.</span></span> <span data-ttu-id="345f9-185">Para obtener más información sobre símbolos de filtro especiales, consulte [Criterios de filtro](#FilterCriteria) y [Tokens de filtro](#FilterTokens).</span><span class="sxs-lookup"><span data-stu-id="345f9-185">For more information about special filter symbols, see [Filter criteria](#FilterCriteria) and [Filter tokens](#FilterTokens).</span></span>

<span data-ttu-id="345f9-186">Las columnas que ya tienen filtros se indican mediante el ![icono Filtro](media/ui-search/filter-icon.png "icono Filtro") en el encabezado de la columna.</span><span class="sxs-lookup"><span data-stu-id="345f9-186">Columns that already have filters are indicated by the ![Filter icon](media/ui-search/filter-icon.png "Filter icon") in the column heading.</span></span> <span data-ttu-id="345f9-187">Para eliminar un filtro, seleccione el encabezado de la columna, luego elija **Borrar filtro**.</span><span class="sxs-lookup"><span data-stu-id="345f9-187">To remove a filter, select the column heading, then choose **Clear Filter**.</span></span>


### <a name="entering-filter-criteria-without-using-the-filter-pane"></a><span data-ttu-id="345f9-188">Introducción de criterios de filtros sin el panel de filtros</span><span class="sxs-lookup"><span data-stu-id="345f9-188">Entering Filter Criteria Without Using the Filter Pane</span></span>
<span data-ttu-id="345f9-189">Puede especificar filtros simples directamente dentro de la lista sin tener que usar el panel de filtros.</span><span class="sxs-lookup"><span data-stu-id="345f9-189">You can specify simple filters directly within the list without having to use the filter pane.</span></span>
<span data-ttu-id="345f9-190">Con cualquier campo seleccionado en una fila, use el método abreviado de teclado **Alt+F3** para mostrar solo los registros que tienen el mismo valor.</span><span class="sxs-lookup"><span data-stu-id="345f9-190">With any field selected on a row, use the **Alt+F3** keyboard shortcut to display only the records having that same value.</span></span> <span data-ttu-id="345f9-191">A continuación puede seleccionar otro campo y usar el mismo acceso directo nuevamente para continuar refinando los filtros.</span><span class="sxs-lookup"><span data-stu-id="345f9-191">You can then select another field and use the same shortcut again to continue refining your filters.</span></span> <span data-ttu-id="345f9-192">Si el campo seleccionado ya está filtrado, la combinación **Alt+F3** borrará ese filtro.</span><span class="sxs-lookup"><span data-stu-id="345f9-192">If the selected field is already filtered, using **Alt+F3** will clear that filter.</span></span>

> [!TIP]
> <span data-ttu-id="345f9-193">Acelere la búsqueda y el análisis de sus datos utilizando combinaciones de atajos de teclado.</span><span class="sxs-lookup"><span data-stu-id="345f9-193">Accelerate finding and analyzing your data by using combinations of keyboard shortcuts.</span></span> <span data-ttu-id="345f9-194">Por ejemplo, seleccione un campo, use **Mayús+Alt+F3** para agregar ese campo al panel de filtros, escriba los criterios de filtro, use **Ctrl+Intro** para volver a las filas, seleccione otro campo y use **Alt+F3** para filtrar ese valor.</span><span class="sxs-lookup"><span data-stu-id="345f9-194">For example, select a field, use **Shift+Alt+F3** to add that field to the filter pane, type the filter criteria, use **Ctrl+Enter** to return to the rows, select another field, and use **Alt+F3** to filter to that value.</span></span>
<span data-ttu-id="345f9-195">Para obtener más información, consulte [Métodos abreviados de teclado](keyboard-shortcuts.md#KeyboardFilter).</span><span class="sxs-lookup"><span data-stu-id="345f9-195">For more information see [Keyboard Shortcuts](keyboard-shortcuts.md#KeyboardFilter).</span></span>


## <span data-ttu-id="345f9-196"><a name="FilterCriteria"> </a>Criterios y símbolos de filtro</span><span class="sxs-lookup"><span data-stu-id="345f9-196"><a name="FilterCriteria"> </a>Filter Criteria and Symbols</span></span>
<span data-ttu-id="345f9-197">Al introducir criterios, puede usar todos los números y las letras que normalmente se emplean en un campo.</span><span class="sxs-lookup"><span data-stu-id="345f9-197">When you enter criteria, you can use all the numbers and letters that you can normally use in the field.</span></span> <span data-ttu-id="345f9-198">También puede usar símbolos especiales para filtrar aún más los resultados.</span><span class="sxs-lookup"><span data-stu-id="345f9-198">In addition, you can use special symbols to further filter the results.</span></span> <span data-ttu-id="345f9-199">En las tablas siguientes se muestran los símbolos que se pueden usar en los filtros.</span><span class="sxs-lookup"><span data-stu-id="345f9-199">The following tables show the symbols which can be used in filters.</span></span> <span data-ttu-id="345f9-200">Para obtener más información sobre fechas y horas, también puede consultar [Trabajar con fechas y horas del calendario](ui-enter-date-ranges.md).</span><span class="sxs-lookup"><span data-stu-id="345f9-200">For dates and times, you can also refer to [Working with Calendar Dates and Times](ui-enter-date-ranges.md) for more detailed information.</span></span>

> [!IMPORTANT]  
>  <span data-ttu-id="345f9-201">Puede haber instancias donde los valores de campo contengan los siguientes símbolos y desee filtrarlos.</span><span class="sxs-lookup"><span data-stu-id="345f9-201">There may be instances where field values contain these symbols and you want to filter on them.</span></span> <span data-ttu-id="345f9-202">Para ello, debe incluir la expresión de filtro que contiene el símbolo entre comillas (").</span><span class="sxs-lookup"><span data-stu-id="345f9-202">To do this, you must include the filter expression that contains the symbol in quotation marks ('').</span></span> <span data-ttu-id="345f9-203">Por ejemplo, si desea filtrar en los registros que comienzan por el texto *S&R*, la expresión de filtro es `'S&R*'`.</span><span class="sxs-lookup"><span data-stu-id="345f9-203">For example, if you want to filter on records that start with the text *S&R*, the filter expression is `'S&R*'`.</span></span>  

### <a name="-interval"></a><span data-ttu-id="345f9-204">(..) Intervalo</span><span class="sxs-lookup"><span data-stu-id="345f9-204">(..) Interval</span></span>

|<span data-ttu-id="345f9-205">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="345f9-205">Sample Expression</span></span>|<span data-ttu-id="345f9-206">Registros mostrados</span><span class="sxs-lookup"><span data-stu-id="345f9-206">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`1100..2100`|<span data-ttu-id="345f9-207">Números del 1100 al 2100.</span><span class="sxs-lookup"><span data-stu-id="345f9-207">Numbers 1100 through 2100</span></span>|  
|`..2500`|<span data-ttu-id="345f9-208">Hasta la 2500 inclusive</span><span class="sxs-lookup"><span data-stu-id="345f9-208">Up to and including 2500</span></span>|  
|`..12 31 00`|<span data-ttu-id="345f9-209">Fechas hasta el 31 12 00, inclusive.</span><span class="sxs-lookup"><span data-stu-id="345f9-209">Dates up to and including 12 31 00</span></span>|  
|`P8..`|<span data-ttu-id="345f9-210">Información correspondiente al ejercicio económico 8 en adelante</span><span class="sxs-lookup"><span data-stu-id="345f9-210">Information for accounting period 8 and thereafter</span></span>|  
|`..23`|<span data-ttu-id="345f9-211">Desde la fecha inicial hasta 23-mes actual-año actual 23:59:59</span><span class="sxs-lookup"><span data-stu-id="345f9-211">From the beginning date until 23-current month-current year 23:59:59</span></span>|  
|`23..`|<span data-ttu-id="345f9-212">Desde 23-mes actual-año actual 0:00:00 hasta la hora final</span><span class="sxs-lookup"><span data-stu-id="345f9-212">From 23-current month-current year 0:00:00 until the end of time</span></span>|  
|`22..23`|<span data-ttu-id="345f9-213">Desde 22-mes actual-año actual 0:00:00 hasta 23-mes actual-año actual 23:59:59</span><span class="sxs-lookup"><span data-stu-id="345f9-213">From 22-current month-current year 0:00:00 until 23-current month-current year 23:59:59</span></span>|  

### <a name="124-eitheror"></a><span data-ttu-id="345f9-214">(&#124;) O/o</span><span class="sxs-lookup"><span data-stu-id="345f9-214">(&#124;) Either/or</span></span>  

|<span data-ttu-id="345f9-215">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="345f9-215">Sample Expression</span></span>|<span data-ttu-id="345f9-216">Registros mostrados</span><span class="sxs-lookup"><span data-stu-id="345f9-216">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`1200|1300`|<span data-ttu-id="345f9-217">Números con 1200 ó 1300</span><span class="sxs-lookup"><span data-stu-id="345f9-217">Numbers with 1200 or 1300</span></span>|  

### <a name="-not-equal-to"></a><span data-ttu-id="345f9-218">(<>) Distinto</span><span class="sxs-lookup"><span data-stu-id="345f9-218">(<>) Not equal to</span></span>  

|<span data-ttu-id="345f9-219">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="345f9-219">Sample Expression</span></span>|<span data-ttu-id="345f9-220">Registros mostrados</span><span class="sxs-lookup"><span data-stu-id="345f9-220">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`<>0`|<span data-ttu-id="345f9-221">Todos los números, excepto el 0</span><span class="sxs-lookup"><span data-stu-id="345f9-221">All numbers except 0</span></span><br /><br /> <span data-ttu-id="345f9-222">La opción SQL Server permite combinar este símbolo con una expresión de caracteres comodín.</span><span class="sxs-lookup"><span data-stu-id="345f9-222">The SQL Server Option allows you to combine this symbol with a wild card expression.</span></span> <span data-ttu-id="345f9-223">Por ejemplo, <>A\* significa distinto de cualquier texto que empiece por A.</span><span class="sxs-lookup"><span data-stu-id="345f9-223">For example, <>A\* meaning not equal to any text that starts with A.</span></span>|  

### <a name="-greater-than"></a><span data-ttu-id="345f9-224">(>) Mayor de</span><span class="sxs-lookup"><span data-stu-id="345f9-224">(>) Greater than</span></span>  

|<span data-ttu-id="345f9-225">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="345f9-225">Sample Expression</span></span>|<span data-ttu-id="345f9-226">Registros mostrados</span><span class="sxs-lookup"><span data-stu-id="345f9-226">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`>1200`|<span data-ttu-id="345f9-227">Números mayores que 1200</span><span class="sxs-lookup"><span data-stu-id="345f9-227">Numbers greater than 1200</span></span>|  

### <a name="-greater-than-or-equal-to"></a><span data-ttu-id="345f9-228">(>=) Mayor o igual a</span><span class="sxs-lookup"><span data-stu-id="345f9-228">(>=) Greater than or equal to</span></span>  

|<span data-ttu-id="345f9-229">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="345f9-229">Sample Expression</span></span>|<span data-ttu-id="345f9-230">Registros mostrados</span><span class="sxs-lookup"><span data-stu-id="345f9-230">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`>=1200`|<span data-ttu-id="345f9-231">Números mayores o igual que 1200</span><span class="sxs-lookup"><span data-stu-id="345f9-231">Numbers greater than or equal to 1200</span></span>|  

### <a name="-less-than"></a><span data-ttu-id="345f9-232">(<) Menor de</span><span class="sxs-lookup"><span data-stu-id="345f9-232">(<) Less than</span></span>  

|<span data-ttu-id="345f9-233">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="345f9-233">Sample Expression</span></span>|<span data-ttu-id="345f9-234">Registros mostrados</span><span class="sxs-lookup"><span data-stu-id="345f9-234">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`<1200`|<span data-ttu-id="345f9-235">Números menores que 1200</span><span class="sxs-lookup"><span data-stu-id="345f9-235">Numbers less than 1200</span></span>|  

### <a name="-less-than-or-equal-to"></a><span data-ttu-id="345f9-236">(<=) Menor o igual que</span><span class="sxs-lookup"><span data-stu-id="345f9-236">(<=) Less than or equal to</span></span>  

|<span data-ttu-id="345f9-237">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="345f9-237">Sample Expression</span></span>|<span data-ttu-id="345f9-238">Registros mostrados</span><span class="sxs-lookup"><span data-stu-id="345f9-238">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`<=1200`|<span data-ttu-id="345f9-239">Números menores o iguales que 1200</span><span class="sxs-lookup"><span data-stu-id="345f9-239">Numbers less than or equal to 1200</span></span>|  

### <a name="-and"></a><span data-ttu-id="345f9-240">(&) y</span><span class="sxs-lookup"><span data-stu-id="345f9-240">(&) And</span></span>  

|<span data-ttu-id="345f9-241">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="345f9-241">Sample Expression</span></span>|<span data-ttu-id="345f9-242">Registros mostrados</span><span class="sxs-lookup"><span data-stu-id="345f9-242">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`>200&<1200`|<span data-ttu-id="345f9-243">Números mayores de 200 e inferiores a 1200</span><span class="sxs-lookup"><span data-stu-id="345f9-243">Numbers greater than 200 and less than 1200</span></span>|  

### <a name="-an-exact-character-match"></a><span data-ttu-id="345f9-244">(") Una coincidencia exacta de carácter</span><span class="sxs-lookup"><span data-stu-id="345f9-244">('') An exact character match</span></span>  

|<span data-ttu-id="345f9-245">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="345f9-245">Sample Expression</span></span>|<span data-ttu-id="345f9-246">Registros mostrados</span><span class="sxs-lookup"><span data-stu-id="345f9-246">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`'man'`|<span data-ttu-id="345f9-247">Texto que coincide exactamente con man y distingue mayúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="345f9-247">Text that matches man exactly and is case sensitive.</span></span>|  

### <a name="-case-insensitive"></a><span data-ttu-id="345f9-248">(@) Distinción entre mayúsculas y minúsculas</span><span class="sxs-lookup"><span data-stu-id="345f9-248">(@) Case insensitive</span></span>  

|<span data-ttu-id="345f9-249">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="345f9-249">Sample Expression</span></span>|<span data-ttu-id="345f9-250">Registros mostrados</span><span class="sxs-lookup"><span data-stu-id="345f9-250">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`@man*`|<span data-ttu-id="345f9-251">Texto que empieza por man y no distingue mayúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="345f9-251">Text that starts with man and is case insensitive.</span></span>|  

### <a name="-an-indefinite-number-of-unknown-characters"></a><span data-ttu-id="345f9-252">(\*) Un número indefinido de caracteres desconocidos (quizás ninguno)</span><span class="sxs-lookup"><span data-stu-id="345f9-252">(\*) An indefinite number of unknown characters</span></span>

|<span data-ttu-id="345f9-253">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="345f9-253">Sample Expression</span></span>|<span data-ttu-id="345f9-254">Registros mostrados</span><span class="sxs-lookup"><span data-stu-id="345f9-254">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`*Co*`|<span data-ttu-id="345f9-255">Texto que contenga “Co” y es con diferenciación de mayúsculas y minúsculas.</span><span class="sxs-lookup"><span data-stu-id="345f9-255">Text that contains "Co" and is case sensitive.</span></span>|  
|`*Co`|<span data-ttu-id="345f9-256">Texto que termine con “Co” y es con diferenciación de mayúsculas y minúsculas.</span><span class="sxs-lookup"><span data-stu-id="345f9-256">Text that ends with "Co" and is case sensitive.</span></span>|  
|`Co*`|<span data-ttu-id="345f9-257">Texto que empiece por “Co” y es con diferenciación de mayúsculas y minúsculas.</span><span class="sxs-lookup"><span data-stu-id="345f9-257">Text that begins with "Co" and is case sensitive.</span></span>|  

> [!NOTE]  
>   <span data-ttu-id="345f9-258">No puede utilizar `*` al filtrar en los campos de opción (enumeración), como el campo **Estado** en los pedidos de venta.</span><span class="sxs-lookup"><span data-stu-id="345f9-258">You cannot use `*` when filtering on option (enumeration) fields, such as the **Status** field on sales orders.</span></span> <span data-ttu-id="345f9-259">Para especificar un filtro para este tipo de campo, puede especificar el valor numérico como parámetro de filtrado.</span><span class="sxs-lookup"><span data-stu-id="345f9-259">To enter a filter for this type of field, you can enter the numeric value as a filtering parameter.</span></span> <span data-ttu-id="345f9-260">Por ejemplo, en el campo **Estado** de un pedido de venta que tenga los valores **Abierto**, **Lanzado**, **Aprobación pendiente** y **Prepago pendiente**, utilice los valores `0`, `1`, `2` y `3` para filtrar para estas opciones.</span><span class="sxs-lookup"><span data-stu-id="345f9-260">For example, in the **Status** field on a sales order that has the values **Open**, **Released**, **Pending Approval**, and **Pending Prepayment**, use the values `0`, `1`, `2`, and `3` to filter for these options.</span></span>

### <a name="-one-unknown-character"></a><span data-ttu-id="345f9-261">(?) Un carácter desconocido</span><span class="sxs-lookup"><span data-stu-id="345f9-261">(?) One unknown character</span></span>  

|<span data-ttu-id="345f9-262">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="345f9-262">Sample Expression</span></span>|<span data-ttu-id="345f9-263">Registros mostrados</span><span class="sxs-lookup"><span data-stu-id="345f9-263">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`Hans?n`|<span data-ttu-id="345f9-264">Texto como Mendoza o Mendosa</span><span class="sxs-lookup"><span data-stu-id="345f9-264">Text such as Hansen or Hanson</span></span>|  

### <a name="combined-format-expressions"></a><span data-ttu-id="345f9-265">Expresiones de formato combinadas</span><span class="sxs-lookup"><span data-stu-id="345f9-265">Combined Format Expressions</span></span>  

|<span data-ttu-id="345f9-266">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="345f9-266">Sample Expression</span></span>|<span data-ttu-id="345f9-267">Registros mostrados</span><span class="sxs-lookup"><span data-stu-id="345f9-267">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`5999|8100..8490`|<span data-ttu-id="345f9-268">Incluye todos los registros cuyo número sea 5999 o un número entre 8100 y 8490.</span><span class="sxs-lookup"><span data-stu-id="345f9-268">Include any records with the number 5999 or a number from the interval 8100 through 8490.</span></span>|  
|`..1299|1400..`|<span data-ttu-id="345f9-269">Incluye los registros cuyo número sea menor o igual que 1299 o un número igual o mayor que 1400</span><span class="sxs-lookup"><span data-stu-id="345f9-269">Include records with a number less than or equal to 1299 or a number equal to 1400 or greater (all numbers except 1300 through 1399).</span></span>|  
|`>50&<100`|<span data-ttu-id="345f9-270">Incluye los registros cuyo número sea mayor que 50 y menor que 100.</span><span class="sxs-lookup"><span data-stu-id="345f9-270">Include records with numbers that are greater than 50 and less than 100 (numbers 51 through 99).</span></span>|  


## <span data-ttu-id="345f9-271"><a name="FilterTokens"> </a>Tokens de filtro</span><span class="sxs-lookup"><span data-stu-id="345f9-271"><a name="FilterTokens"> </a>Filter Tokens</span></span>
<span data-ttu-id="345f9-272">Al introducir criterios de filtro, también puede escribir palabras que tengan un significado especial, lo que se conoce como tokens de filtro.</span><span class="sxs-lookup"><span data-stu-id="345f9-272">When entering filter criteria, you can also type words that have special meaning, called filter tokens.</span></span> <span data-ttu-id="345f9-273">Después de introducir la palabra token, la palabra se reemplaza por el valor o valores que representa.</span><span class="sxs-lookup"><span data-stu-id="345f9-273">After entering the token word, the word is replaced by the value or values that it represents.</span></span> <span data-ttu-id="345f9-274">Esto facilita el filtrado al reducir la necesidad de ir a otras páginas para buscar los valores que desea agregar a su filtro.</span><span class="sxs-lookup"><span data-stu-id="345f9-274">This makes filtering easier by reducing the need to navigate to other pages to look up values you want to add to your filter.</span></span> <span data-ttu-id="345f9-275">En las tablas siguientes se describen algunos de los tokens que puede escribir como criterios de filtro.</span><span class="sxs-lookup"><span data-stu-id="345f9-275">The tables below describe some of the tokens you can type as filter criteria.</span></span>

> [!TIP]
> <span data-ttu-id="345f9-276">Su organización puede usar tokens personalizados.</span><span class="sxs-lookup"><span data-stu-id="345f9-276">Your organization may use custom tokens.</span></span> <span data-ttu-id="345f9-277">Para obtener información sobre el conjunto completo de tokens disponibles o para agregar más tokens personalizados, hable con su administrador.</span><span class="sxs-lookup"><span data-stu-id="345f9-277">To learn about the complete set of tokens available to you or to add more custom tokens, talk to your administrator.</span></span> <span data-ttu-id="345f9-278">Para obtener información técnica, consulte [Agregar tokens de filtro](/dynamics365/business-central/dev-itpro/developer/devenv-adding-filter-tokens).</span><span class="sxs-lookup"><span data-stu-id="345f9-278">For technical information see [Adding Filter Tokens](/dynamics365/business-central/dev-itpro/developer/devenv-adding-filter-tokens).</span></span>


### <a name="me-or-userid-records-assigned-to-you"></a><span data-ttu-id="345f9-279">(%me o %userid) Registros que se le han asignado</span><span class="sxs-lookup"><span data-stu-id="345f9-279">(%me or %userid) Records Assigned to You</span></span>

<span data-ttu-id="345f9-280">Utilice `%me` o `%userid` cuando filtre campos que contengan el ID de usuario, como el campo **Asignado a ID de usuario**, para mostrar todos los registros que se le asignaron.</span><span class="sxs-lookup"><span data-stu-id="345f9-280">Use `%me` or `%userid` when filtering fields that contain the user ID, such as **Assigned to User ID** field, to display all records that are assigned to you.</span></span>

|<span data-ttu-id="345f9-281">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="345f9-281">Sample Expression</span></span>|<span data-ttu-id="345f9-282">Registros mostrados</span><span class="sxs-lookup"><span data-stu-id="345f9-282">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`%me`<br /><span data-ttu-id="345f9-283">o</span><span class="sxs-lookup"><span data-stu-id="345f9-283">or</span></span><br />`%userid`|<span data-ttu-id="345f9-284">Registros que se han asignado a su cuenta.</span><span class="sxs-lookup"><span data-stu-id="345f9-284">Records that are assigned to your user account.</span></span> |  

### <a name="mycustomers-customers-in-my-customers"></a><span data-ttu-id="345f9-285">(%mycustomers) Clientes en Mis clientes</span><span class="sxs-lookup"><span data-stu-id="345f9-285">(%mycustomers) Customers in My Customers</span></span>

<span data-ttu-id="345f9-286">Use `%mycustomers` en el campo de cliente **No** para mostrar todos los registros de los clientes que se incluyen en la lista **Mis clientes** en su Área de trabajo.</span><span class="sxs-lookup"><span data-stu-id="345f9-286">Use `%mycustomers` in the customer **No** field to display all records for customers that are included in the **My Customers** list on your Role Center.</span></span>

|<span data-ttu-id="345f9-287">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="345f9-287">Sample Expression</span></span>|<span data-ttu-id="345f9-288">Registros mostrados</span><span class="sxs-lookup"><span data-stu-id="345f9-288">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`%mycustomers`|<span data-ttu-id="345f9-289">Clientes en **Mis clientes** en el Área de trabajo.</span><span class="sxs-lookup"><span data-stu-id="345f9-289">Customers in the **My Customers** on your Role Center.</span></span> |  

### <a name="myitems-items-in-my-items"></a><span data-ttu-id="345f9-290">(%myitems) Artículos en Mis artículos</span><span class="sxs-lookup"><span data-stu-id="345f9-290">(%myitems) Items in My Items</span></span>

<span data-ttu-id="345f9-291">Use `%myitems` en el campo de artículo **No** para mostrar todos los registros de los artículos que se incluyen en la lista **Mis artículos** en su Área de trabajo.</span><span class="sxs-lookup"><span data-stu-id="345f9-291">Use `%myitems` in the item **No** field to display all records for items that are included in the **My Items** list on your Role Center.</span></span>

|<span data-ttu-id="345f9-292">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="345f9-292">Sample Expression</span></span>|<span data-ttu-id="345f9-293">Registros mostrados</span><span class="sxs-lookup"><span data-stu-id="345f9-293">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`%myitems`|<span data-ttu-id="345f9-294">Artículos en **Mis artículos** en el Área de trabajo.</span><span class="sxs-lookup"><span data-stu-id="345f9-294">Items in the **My Items** on your Role Center.</span></span> |  

### <a name="myvendors-vendors-in-my-vendors"></a><span data-ttu-id="345f9-295">(%myvendors) Proveedores en Mis proveedores</span><span class="sxs-lookup"><span data-stu-id="345f9-295">(%myvendors) Vendors in My Vendors</span></span>

<span data-ttu-id="345f9-296">Use `%myvendors` en el campo de proveedor **No** para mostrar todos los registros de los proveedores que se incluyen en la lista **Mis proveedores** en su Área de trabajo.</span><span class="sxs-lookup"><span data-stu-id="345f9-296">Use `%myvendors` in the vendor **No** field to display all records for vendors that are included in the **My Vendors** list on your Role Center.</span></span>

|<span data-ttu-id="345f9-297">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="345f9-297">Sample Expression</span></span>|<span data-ttu-id="345f9-298">Registros mostrados</span><span class="sxs-lookup"><span data-stu-id="345f9-298">Records Displayed</span></span>|  
|-----------------------|-----------------------|  
|`%myvendors`|<span data-ttu-id="345f9-299">Proveedores en **Mis proveedores** en el Área de trabajo.</span><span class="sxs-lookup"><span data-stu-id="345f9-299">Vendors in the **My Vendors** on your Role Center.</span></span> |  


## <a name="see-also"></a><span data-ttu-id="345f9-300">Consulte también</span><span class="sxs-lookup"><span data-stu-id="345f9-300">See Also</span></span>
<span data-ttu-id="345f9-301">[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="345f9-301">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="345f9-302">Preguntas comunes acerca de Buscar y filtrar</span><span class="sxs-lookup"><span data-stu-id="345f9-302">Common questions about Searching and Filtering</span></span>](ui-search-filter-faq.md)
