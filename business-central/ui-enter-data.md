---
title: Cómo introducir datis eb campos | Documentos de Microsoft
description: Obtenga información sobre las características generales que le ayudan a introducir datos en los campos.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: jswymer
ms.openlocfilehash: 00143454cf0b0da9b111f92bcdb7879c7e6743d2
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 03/31/2019
ms.locfileid: "929078"
---
# <a name="entering-data"></a><span data-ttu-id="c8571-103">Introducción de datos</span><span class="sxs-lookup"><span data-stu-id="c8571-103">Entering Data</span></span>

<span data-ttu-id="c8571-104">Hay muchas características generales que le ayudan a introducir datos de forma más fácil, rápida y precisa.</span><span class="sxs-lookup"><span data-stu-id="c8571-104">There are many general features that help you enter data easier, faster, and more accurate.</span></span> <span data-ttu-id="c8571-105">Las características generales para la introducción de datos se describen en este artículo.</span><span class="sxs-lookup"><span data-stu-id="c8571-105">The general features for entering data are described in this article.</span></span>  

<!-- The examples in this article use the demonstration data.-->

## <a name="keyboard-shortcuts"></a><span data-ttu-id="c8571-106">Métodos abreviados de teclado</span><span class="sxs-lookup"><span data-stu-id="c8571-106">Keyboard Shortcuts</span></span>

<span data-ttu-id="c8571-107">Hay varios métodos abreviados de teclado que le permiten trabajar "sin ratón" y acelerar la entrada de datos, especialmente con movimientos a gran escala y tareas de escritura repetitivas.</span><span class="sxs-lookup"><span data-stu-id="c8571-107">There are several keyboard shortcuts that let you to work "mouse-free" and speed up your data entry, especially with large scale entries and repetitive typing tasks.</span></span>

<span data-ttu-id="c8571-108">Para obtener más información sobre estos métodos abreviados, consulte [Métodos abreviados de teclado](keyboard-shortcuts.md).</span><span class="sxs-lookup"><span data-stu-id="c8571-108">For more information about shortcuts, see [Keyboard Shortcuts](keyboard-shortcuts.md).</span></span> <span data-ttu-id="c8571-109">Algunos de los métodos abreviados se explican en este artículo.</span><span class="sxs-lookup"><span data-stu-id="c8571-109">A few of the shortcuts are discussed in this article.</span></span>

## <a name="QuickEntry"></a><span data-ttu-id="c8571-110">Acelerar la entrada de datos con la entrada rápida</span><span class="sxs-lookup"><span data-stu-id="c8571-110">Accelerating Data Entry Using Quick Entry</span></span>

<span data-ttu-id="c8571-111">La entrada rápida es una característica diseñada para la entrada de datos cuando se utiliza el teclado.</span><span class="sxs-lookup"><span data-stu-id="c8571-111">Quick Entry is a feature designed for data entry when using the keyboard.</span></span> <span data-ttu-id="c8571-112">La entrada rápida funciona en campos (como en las páginas de fichas) y en listas (filas y columnas).</span><span class="sxs-lookup"><span data-stu-id="c8571-112">Quick Entry works on fields (like on card pages) and in lists (rows and columns).</span></span> <span data-ttu-id="c8571-113">Es beneficiosa cuando se realizan tareas de escritura repetitivas que requieren la creación de varios registros en secuencia, como un lote de pedidos de venta o el registro de nuevos productos.</span><span class="sxs-lookup"><span data-stu-id="c8571-113">It is beneficial when performing repetitive typing tasks that require creating multiple records in sequence, such as a batch of sales orders or registering new items.</span></span>

<span data-ttu-id="c8571-114">Es posible que ya esté familiarizado con el uso de la tecla Tab para navegar desde un campo de una página al siguiente campo editable.</span><span class="sxs-lookup"><span data-stu-id="c8571-114">You might already be familiar with using the Tab key to navigate from one field on a page to the next editable field.</span></span> <span data-ttu-id="c8571-115">Una desventaja de usar Tab es que siempre va secuencialmente al siguiente campo.</span><span class="sxs-lookup"><span data-stu-id="c8571-115">A disadvantage of using Tab is that it always goes sequentially to the next field.</span></span> <!-- even if the field is non-editable or seldom filled it in.--><span data-ttu-id="c8571-116">La entrada rápida le permite cambiar esta ruta.</span><span class="sxs-lookup"><span data-stu-id="c8571-116">Quick Entry lets you change this path.</span></span> <span data-ttu-id="c8571-117">Con la entrada rápida, puede utilizar la tecla Entrar para navegar solo por los campos que le interesan, omitiendo los campos no editables y los campos que normalmente no rellena.</span><span class="sxs-lookup"><span data-stu-id="c8571-117">With Quick Entry, you use the Enter key to navigate through only those fields that you are interested in, skipping non-editable fields and fields that you typically do not fill in.</span></span> <span data-ttu-id="c8571-118">Es posible que ya haya observado este comportamiento en algunas páginas.</span><span class="sxs-lookup"><span data-stu-id="c8571-118">You might have already noticed this behavior on some pages.</span></span> <span data-ttu-id="c8571-119">Esto se debe a que la aplicación ya designa los campos que se deben incluir al pulsar Entrar y los que se deben omitir.</span><span class="sxs-lookup"><span data-stu-id="c8571-119">This is because the application already designates which fields to include when pressing Enter and which ones to skip.</span></span> <span data-ttu-id="c8571-120">Puede personalizar la entrada rápida si personaliza su espacio de trabajo y optimiza la forma en que introduce los datos en cada página.</span><span class="sxs-lookup"><span data-stu-id="c8571-120">You can customize Quick Entry by personalizing your workspace and optimizing how you enter data on each page.</span></span>

### <a name="how-quick-entry-works"></a><span data-ttu-id="c8571-121">Cómo funciona la entrada rápida</span><span class="sxs-lookup"><span data-stu-id="c8571-121">How Quick Entry Works</span></span>

<span data-ttu-id="c8571-122">Cada campo puede marcarse como *incluido en la entrada rápida* o como *excluido de la entrada rápida*.</span><span class="sxs-lookup"><span data-stu-id="c8571-122">Every field can be marked as either being *included in Quick Entry* or *excluded from Quick Entry*.</span></span> <span data-ttu-id="c8571-123">Los campos que se incluyen en la entrada rápida se incluirán en la ruta cuando pulse Entrar; los campos que se excluyen de la entrada rápida, no.</span><span class="sxs-lookup"><span data-stu-id="c8571-123">Fields that are included in Quick Entry, will be included in the path when you press Enter; fields that are excluded from Quick Entry, will not.</span></span>

<span data-ttu-id="c8571-124">Cuando haya finalizado de rellenar un campo, pulse Entrar para confirmar los cambios e ir al siguiente campo.</span><span class="sxs-lookup"><span data-stu-id="c8571-124">When you are finished entering data in a field, you simply press Enter to confirm the changes and go to the next field.</span></span> <span data-ttu-id="c8571-125">Si desea invertir la dirección y pasar al campo anterior, pulse Mayús+Entrar.</span><span class="sxs-lookup"><span data-stu-id="c8571-125">If you want to reverse direction, and go the previous field, press Shift+Enter.</span></span> <span data-ttu-id="c8571-126">Para obtener más información sobre estos métodos abreviados, consulte [Métodos abreviados de teclado de entrada rápida](keyboard-shortcuts.md#QuickEntry).</span><span class="sxs-lookup"><span data-stu-id="c8571-126">For more information about shortcuts, see [Quick Entry keyboard shortcuts](keyboard-shortcuts.md#QuickEntry).</span></span>

#### <a name="tips-and-tricks"></a><span data-ttu-id="c8571-127">Sugerencias y trucos</span><span class="sxs-lookup"><span data-stu-id="c8571-127">Tips and tricks</span></span>
<span data-ttu-id="c8571-128">A continuación se ofrece información útil sobre el uso de la entrada rápida.</span><span class="sxs-lookup"><span data-stu-id="c8571-128">The following provides some useful information about using Quick Entry.</span></span>

- <span data-ttu-id="c8571-129">Está disponible para cualquier campo editable.</span><span class="sxs-lookup"><span data-stu-id="c8571-129">It is available for any editable fields.</span></span>
- <span data-ttu-id="c8571-130">También funciona en columnas y filas.</span><span class="sxs-lookup"><span data-stu-id="c8571-130">It also works across columns and rows.</span></span>
- <span data-ttu-id="c8571-131">No impide el acceso a otros elementos de una página, como las acciones.</span><span class="sxs-lookup"><span data-stu-id="c8571-131">It does not prevent accessing other elements of a page, such as actions.</span></span> <span data-ttu-id="c8571-132">Se puede seguir accediendo a ellos utilizando Tab y Mayús+Tab.</span><span class="sxs-lookup"><span data-stu-id="c8571-132">These are still accessible by using Tab and Shift+Tab.</span></span>  
- <span data-ttu-id="c8571-133">Las fichas desplegables no tienen que expandir para que funcione la entrada rápida.</span><span class="sxs-lookup"><span data-stu-id="c8571-133">FastTabs do not have to be expanded for Quick Entry to work.</span></span> <span data-ttu-id="c8571-134">Si el siguiente campo de entrada rápida se encuentra en una ficha desplegable contraída, esa ficha desplegable se expandirá automáticamente y el enfoque estará en el campo designado.</span><span class="sxs-lookup"><span data-stu-id="c8571-134">If the next Quick Entry field is located in a collapsed FastTab, that FastTab will automatically expand and focus on the designated field.</span></span>
- <span data-ttu-id="c8571-135">La entrada rápida funciona independientemente de si los campos son obligatorios.</span><span class="sxs-lookup"><span data-stu-id="c8571-135">Quick Entry works irrespective of whether fields are mandatory.</span></span> <span data-ttu-id="c8571-136">Por lo tanto, es buena idea asegurarse de que los campos obligatorios se incluyan en la entrada rápida.</span><span class="sxs-lookup"><span data-stu-id="c8571-136">So it is a good idea to ensure that mandatory fields are included in Quick Entry.</span></span>
- <span data-ttu-id="c8571-137">De forma predeterminada, la mayoría de los campos se incluyen automáticamente en la entrada rápida.</span><span class="sxs-lookup"><span data-stu-id="c8571-137">By default, most fields are automatically included in Quick Entry.</span></span> <span data-ttu-id="c8571-138">Por lo tanto, al principio, lo más probable es que su tarea sea excluir campos de la entrada rápida.</span><span class="sxs-lookup"><span data-stu-id="c8571-138">So initially your task will most likely be excluding fields from Quick Entry.</span></span>

### <a name="how-to-change-quick-entry-fields"></a><span data-ttu-id="c8571-139">Cómo modificar los campos de entrada rápida</span><span class="sxs-lookup"><span data-stu-id="c8571-139">How to Change Quick Entry Fields</span></span>

<span data-ttu-id="c8571-140">Para cambiar los campos que se incluyen o se excluyen de la entrada rápida de una página, se utiliza la personalización.</span><span class="sxs-lookup"><span data-stu-id="c8571-140">To change which fields are included in or excluded from Quick Entry on a page, you use personalization.</span></span>

1. <span data-ttu-id="c8571-141">Comience la personalización seleccionando el icono ![Configuración](media/ui-experience/settings_icon_small.png "Icono Configuración para el área de trabajo") y **Personalizar**.</span><span class="sxs-lookup"><span data-stu-id="c8571-141">Start personalization by selecting the ![Settings](media/ui-experience/settings_icon_small.png "Settings icon for role center") icon, and then **Personalize**.</span></span>
2. <span data-ttu-id="c8571-142">Seleccione un campo que desee modificar o, en las listas, seleccione la cabecera de columna correspondiente y, a continuación, seleccione **Incluir en entrada rápida** o **Excluir de entrada rápida**.</span><span class="sxs-lookup"><span data-stu-id="c8571-142">Select a field that you want change, or in lists, select the corresponding column heading, and then choose either **Include in Quick Entry** or **Exclude from Quick Entry**.</span></span>

<span data-ttu-id="c8571-143">Para obtener más información sobre la personalización, consulte [Personalización del área de trabajo](ui-personalization-user.md).</span><span class="sxs-lookup"><span data-stu-id="c8571-143">For more information about personalization, see [Personalizing Your Workspace](ui-personalization-user.md).</span></span>

## <a name="mandatory-fields"></a><span data-ttu-id="c8571-144">Campos obligatorios</span><span class="sxs-lookup"><span data-stu-id="c8571-144">Mandatory Fields</span></span>

<span data-ttu-id="c8571-145">Cuando se introducen datos en páginas, determinados campos aparecen marcados con un asterisco de color rojo.</span><span class="sxs-lookup"><span data-stu-id="c8571-145">When you enter data on pages, certain fields are marked with a red asterisk.</span></span> <span data-ttu-id="c8571-146">El asterisco rojo significa que el campo debe rellenarse para completar un determinado proceso que lo utilice, como registrar una transacción que utilice su valor.</span><span class="sxs-lookup"><span data-stu-id="c8571-146">The red asterisk means that the field must be filled to complete a certain process that uses the field, such as posting a transaction that uses the value in the field.</span></span>  

<span data-ttu-id="c8571-147">Aunque el campo contiene un asterisco rojo, no se le obliga a rellenar el campo para ir a otros campos o cerrar la página.</span><span class="sxs-lookup"><span data-stu-id="c8571-147">Even though the field contains a red asterisk, you are not forced to fill the field before you continue to other fields or close the page.</span></span> <span data-ttu-id="c8571-148">El asterisco rojo solo sirve como recordatorio de que se le bloqueará y no podrá terminar un determinado proceso.</span><span class="sxs-lookup"><span data-stu-id="c8571-148">The red asterisk only serves as a reminder that you will be blocked from completing a certain process.</span></span>  

## <a name="finding-data-as-you-type"></a><span data-ttu-id="c8571-149">Buscar datos al escribir</span><span class="sxs-lookup"><span data-stu-id="c8571-149">Finding Data As You Type</span></span>

 <span data-ttu-id="c8571-150">Cuando comience a escribir caracteres en un campo, aparecerá una lista desplegable que muestra los posibles valores de campo.</span><span class="sxs-lookup"><span data-stu-id="c8571-150">When you start to type characters in a field, a drop-down list is displayed and shows possible field values.</span></span> <span data-ttu-id="c8571-151">Esta lista cambia a medida que escriba caracteres adicionales y puede seleccionar el valor correcto cuando aparezca.</span><span class="sxs-lookup"><span data-stu-id="c8571-151">The list changes as you type more characters, and you can select the correct value when it is displayed.</span></span>  

 <span data-ttu-id="c8571-152">Muchos campos tienen un botón de flecha hacia abajo que puede elegir.</span><span class="sxs-lookup"><span data-stu-id="c8571-152">Many fields have a down arrow button that you can choose.</span></span> <span data-ttu-id="c8571-153">Seleccione la flecha para desplegar una lista de datos que están disponibles para su introducción en el campo.</span><span class="sxs-lookup"><span data-stu-id="c8571-153">You choose the arrow to get a list of data that is available to enter in the field.</span></span> <span data-ttu-id="c8571-154">El botón tiene dos funciones, según el tipo de campo:</span><span class="sxs-lookup"><span data-stu-id="c8571-154">The button has two functions depending on the type of field:</span></span>  

-   <span data-ttu-id="c8571-155">Búsqueda: muestra información de otra tabla, que puede introducir en el campo.</span><span class="sxs-lookup"><span data-stu-id="c8571-155">Lookup - Displays information from another table that you can enter in the field.</span></span> <span data-ttu-id="c8571-156">Puede seleccionar un elemento de datos a la vez.</span><span class="sxs-lookup"><span data-stu-id="c8571-156">You can select one piece of data at a time.</span></span>  

-   <span data-ttu-id="c8571-157">Desplegable: muestra el conjunto de opciones que existe para el campo.</span><span class="sxs-lookup"><span data-stu-id="c8571-157">Drop-down - Displays the set of options that exist for the field.</span></span> <span data-ttu-id="c8571-158">Sólo puede seleccionar una de las opciones.</span><span class="sxs-lookup"><span data-stu-id="c8571-158">You can select only one of the options.</span></span>  

## <a name="copying-and-pasting-fields-and-lines"></a><span data-ttu-id="c8571-159">Copia y pegado de campos y líneas</span><span class="sxs-lookup"><span data-stu-id="c8571-159">Copying and Pasting Fields and Lines</span></span>

<span data-ttu-id="c8571-160">Puede copiar una o más filas de una lista o un solo campo en una página y luego pegar lo que ha copiado en la misma página, otra página o un documento externo (como Microsoft Excel y el correo electrónico de Outlook).</span><span class="sxs-lookup"><span data-stu-id="c8571-160">You can copy one or more rows from a list or a single field on a page, and then paste what you copied into the same page, another page, or an external document (like Microsoft Excel and Outlook email).</span></span> <span data-ttu-id="c8571-161">En resumen, para copiar, presione CTRL+C (cmd+C en macOS) en su teclado.</span><span class="sxs-lookup"><span data-stu-id="c8571-161">In short, to copy, you press CTRL+C (cmd+C in macOS) on your keyboard.</span></span> <span data-ttu-id="c8571-162">Para pegar, presione CTRL+V (cmd+V en macOS).</span><span class="sxs-lookup"><span data-stu-id="c8571-162">To paste, you press CTRL+V (cmd+V in macOS).</span></span>

<span data-ttu-id="c8571-163">En una lista, para copiar el campo en la misma columna de la fila anterior y pegarlo en la fila actual, pulse F8.</span><span class="sxs-lookup"><span data-stu-id="c8571-163">In a list, to copy the field in the same column of the row above, and paste it into the current row, just press F8.</span></span>

<span data-ttu-id="c8571-164">Para obtener más información, consulte [Copiar y pegar en Business Central](ui-copy-paste.md).</span><span class="sxs-lookup"><span data-stu-id="c8571-164">For more information, see [Copying and Pasting in Business Central](ui-copy-paste.md).</span></span>

## <a name="Focus"></a><span data-ttu-id="c8571-165">Enfoque en los productos de línea</span><span class="sxs-lookup"><span data-stu-id="c8571-165">Focusing on Line Items</span></span>

<span data-ttu-id="c8571-166">Al trabajar en documentos que incluyen una parte de productos de línea, como una página de pedido de venta o de factura, puede cambiar su vista para centrarse solo en los productos de línea, ampliando esencialmente la parte de productos de línea para que ocupe prácticamente todo el espacio de trabajo y ocultando otras partes de la página excepto el área de acciones en la parte superior.</span><span class="sxs-lookup"><span data-stu-id="c8571-166">When working on documents that include a line items part, like a sales order or invoice page, you can switch your view to focus only on the line items, essentially expanding the line items part so that it occupies pretty much the entire workspace - hiding other parts of the page except the actions area at the top.</span></span> <span data-ttu-id="c8571-167">Esto le proporciona una mejor visión general de los productos de línea y más espacio para trabajar en ellos.</span><span class="sxs-lookup"><span data-stu-id="c8571-167">This gives you a better overview of the lines items, and provides more room to work on them.</span></span> <span data-ttu-id="c8571-168">Esto es muy beneficioso cuando se trabaja con grandes listas de productos de línea y se desea una entrada rápida de los datos.</span><span class="sxs-lookup"><span data-stu-id="c8571-168">This is particularly beneficial when working with large line item lists and fast data entry is desired.</span></span>

<span data-ttu-id="c8571-169">Otra ventaja es que también proporciona capacidad de filtrado avanzado, como en otras listas, de modo que la navegación y la búsqueda a través de los productos de línea resulta aún más fácil.</span><span class="sxs-lookup"><span data-stu-id="c8571-169">Another advantage is that it also provides advanced filtering capability, like on other lists, so browsing and searching through line items becomes even easier.</span></span>

### <a name="switch-the-focus-on-and-off"></a><span data-ttu-id="c8571-170">Activar y desactivar el enfoque</span><span class="sxs-lookup"><span data-stu-id="c8571-170">Switch the Focus On and Off</span></span>

<span data-ttu-id="c8571-171">Para el enfoque en los productos de línea, seleccione cualquier lugar de la parte de producto de línea y, a continuación, seleccione ![icono Modo de enfoque](media/focus-mode.png "Icono Modo de enfoque") en la esquina superior derecha o pulse Ctrl+Mayús+F12.</span><span class="sxs-lookup"><span data-stu-id="c8571-171">To focus on lines items, select anywhere in the line item part, and then choose ![Focus Mode icon](media/focus-mode.png "Focus mode icon") in the upper right corner or press Ctrl+Shift+F12.</span></span>

<span data-ttu-id="c8571-172">Para volver a la vista normal, seleccione ![Icono Modo de enfoque](media/focus-mode.png "Icono Modo de enfoque") o pulse Ctrl+Mayús+F12 de nuevo.</span><span class="sxs-lookup"><span data-stu-id="c8571-172">To switch back to the normal view, choose ![Focus Mode icon](media/focus-mode.png "Focus mode icon") or press Ctrl+Shift+F12 again.</span></span>

### <a name="filtering-the-line-items"></a><span data-ttu-id="c8571-173">Filtrado de los productos de línea</span><span class="sxs-lookup"><span data-stu-id="c8571-173">Filtering the Line Items</span></span>

<span data-ttu-id="c8571-174">Para iniciar el filtrado, seleccione ![Icono Panel de filtros](media/open-filter-pane-icon.png "Icono Panel de filtros") en la parte superior de la lista o pulse **Mayús+F3** para abrir el panel de filtros.</span><span class="sxs-lookup"><span data-stu-id="c8571-174">To start filtering, select ![Filter pane icon](media/open-filter-pane-icon.png "Filter pane icon") at the top of the list or press **Shift+F3** to open the filter pane.</span></span> <span data-ttu-id="c8571-175">Con el panel de filtros se trabaja como en cualquier otra lista.</span><span class="sxs-lookup"><span data-stu-id="c8571-175">You work with the filter pane as you do on any other list.</span></span> <span data-ttu-id="c8571-176">Para obtener más información, consulte [Filtrado](ui-enter-criteria-filters.md#Filtering).</span><span class="sxs-lookup"><span data-stu-id="c8571-176">For more information, see [Filtering](ui-enter-criteria-filters.md#Filtering).</span></span>

<span data-ttu-id="c8571-177">El filtrado es especialmente útil cuando se ven y analizan documentos largos.</span><span class="sxs-lookup"><span data-stu-id="c8571-177">Filtering is especially helpful when viewing and analysing longer documents.</span></span> <span data-ttu-id="c8571-178">Por ejemplo, imagine que abre una factura de ventas registrada y filtra los productos de línea para visualizar todos los productos de línea que tienen un descuento individual superior al 5 %, o bien establece un filtro para visualizar solo los accesorios de bicicleta con "pro" en el nombre.</span><span class="sxs-lookup"><span data-stu-id="c8571-178">For example, imagine you open a posted sales invoice and filter the line items to display all line items that have an individual discount above 5%, or filter to display only bike accessories with 'pro' in the name.</span></span>

## <a name="entering-quantities-by-calculation"></a><span data-ttu-id="c8571-179">Introducir cantidades por cálculo</span><span class="sxs-lookup"><span data-stu-id="c8571-179">Entering Quantities by Calculation</span></span>

<span data-ttu-id="c8571-180">Al introducir números en campos de cantidad, como el campo **Cantidad** de una línea de diario de producto, puede introducir la fórmula en lugar de la cantidad de la suma.</span><span class="sxs-lookup"><span data-stu-id="c8571-180">When entering numbers into quantity fields, such as the **Quantity** field on an item journal line, you can enter the formula instead of the sum quantity.</span></span>  

### <a name="examples"></a><span data-ttu-id="c8571-181">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="c8571-181">Examples</span></span>  

-   <span data-ttu-id="c8571-182">Si introduce 19+19, el campo se calcula para obtener el valor 38.</span><span class="sxs-lookup"><span data-stu-id="c8571-182">If you enter 19+19, the field is calculated to 38.</span></span>  

-   <span data-ttu-id="c8571-183">Si introduce 41-9, el campo se calcula para obtener el valor 32.</span><span class="sxs-lookup"><span data-stu-id="c8571-183">If you enter 41-9, the field is calculated to 32.</span></span>  

-   <span data-ttu-id="c8571-184">Si introduce 12\*4, el campo se calcula para obtener el valor 48.</span><span class="sxs-lookup"><span data-stu-id="c8571-184">If you enter 12\*4, the field is calculated to 48.</span></span>  

-   <span data-ttu-id="c8571-185">Si introduce 12/4, el campo se calcula para obtener el valor 3.</span><span class="sxs-lookup"><span data-stu-id="c8571-185">If you enter 12/4, the field is calculated to 3.</span></span>  

## <a name="entering-negative-numbers"></a><span data-ttu-id="c8571-186">Especificación de números negativos</span><span class="sxs-lookup"><span data-stu-id="c8571-186">Entering Negative Numbers</span></span>

<span data-ttu-id="c8571-187">Puede especificar números negativos de dos formas.</span><span class="sxs-lookup"><span data-stu-id="c8571-187">You can enter negative numbers in two ways.</span></span> <span data-ttu-id="c8571-188">El número -20,5 se puede especificar como:</span><span class="sxs-lookup"><span data-stu-id="c8571-188">The number -20.5 can be entered as:</span></span>  

-   <span data-ttu-id="c8571-189">-20,5</span><span class="sxs-lookup"><span data-stu-id="c8571-189">-20.5</span></span>  

    <span data-ttu-id="c8571-190">O</span><span class="sxs-lookup"><span data-stu-id="c8571-190">or</span></span>
-   <span data-ttu-id="c8571-191">20,5-</span><span class="sxs-lookup"><span data-stu-id="c8571-191">20.5-</span></span>  

 <span data-ttu-id="c8571-192">En ambos casos, el importe se registrará como -20,5.</span><span class="sxs-lookup"><span data-stu-id="c8571-192">In both cases, the amount will be recorded in as -20.5.</span></span>  

 <span data-ttu-id="c8571-193">Si el último carácter de la expresión es **+** o **-**, la expresión completa se registrará con ese signo.</span><span class="sxs-lookup"><span data-stu-id="c8571-193">If the last character of the expression is a **+** or a **-**, the entire expression will be recorded with that sign.</span></span> <span data-ttu-id="c8571-194">Ejemplo, **10-20+** dará como resultado 10 y no -10.</span><span class="sxs-lookup"><span data-stu-id="c8571-194">An example, **10-20+** will result in 10 and not -10.</span></span>  

## <a name="entering-dates-and-times"></a><span data-ttu-id="c8571-195">Introducir fechas y horas</span><span class="sxs-lookup"><span data-stu-id="c8571-195">Entering Dates and Times</span></span>

<span data-ttu-id="c8571-196">Puede especificar fechas y horas en todos los campos diseñados específicamente para las fechas (campos de fecha).</span><span class="sxs-lookup"><span data-stu-id="c8571-196">You can enter dates and times in all the fields that are specifically assigned to dates (date fields).</span></span> <span data-ttu-id="c8571-197">Las fechas pueden escribirse con o sin separadores.</span><span class="sxs-lookup"><span data-stu-id="c8571-197">You can enter dates with or without separators.</span></span>

> [!NOTE]  
> <span data-ttu-id="c8571-198">La forma de especificar las fechas y horas depende de los valores **Región**.</span><span class="sxs-lookup"><span data-stu-id="c8571-198">How you enter dates and times depends on your **Region** settings.</span></span> <span data-ttu-id="c8571-199">Para obtener más información, consulte [Cambiar configuración básica](ui-change-basic-settings.md).</span><span class="sxs-lookup"><span data-stu-id="c8571-199">For more information, see [Changing Basic Settings](ui-change-basic-settings.md).</span></span>  

### <a name="entering-dates"></a><span data-ttu-id="c8571-200">Introducción de fechas</span><span class="sxs-lookup"><span data-stu-id="c8571-200">Entering Dates</span></span>

<span data-ttu-id="c8571-201">Para los campos de fecha, puede utilizar el selector de datos, que le permite seleccionar una fecha de un calendario o puede introducir fechas manualmente.</span><span class="sxs-lookup"><span data-stu-id="c8571-201">For date fields, you can either use the data picker, which lets you select a date from a calender, or you can enter dates manually.</span></span> <span data-ttu-id="c8571-202">Esta sección proporciona un breve resumen de cómo introducir fechas.</span><span class="sxs-lookup"><span data-stu-id="c8571-202">This section provides a brief overview of how to enter dates.</span></span> <span data-ttu-id="c8571-203">Para obtener más detalles, consulte [Trabajar con fechas y horas del calendario](ui-enter-date-ranges.md).</span><span class="sxs-lookup"><span data-stu-id="c8571-203">For more details, see [Working with Calendar Dates and Times](ui-enter-date-ranges.md).</span></span>

<span data-ttu-id="c8571-204">Para la entrada de fecha manual, puede introducir dos, cuatro, seis u ocho dígitos:</span><span class="sxs-lookup"><span data-stu-id="c8571-204">For manually date entry, you can enter two, four, six, or eight digits:</span></span>  

-   <span data-ttu-id="c8571-205">Si introduce solo dos dígitos, se interpretarán como el día y se agregarán el mes y el año de la fecha de trabajo.</span><span class="sxs-lookup"><span data-stu-id="c8571-205">If you enter only two digits, this is interpreted as the day, and it will add the month and the year of the work date.</span></span>  

-   <span data-ttu-id="c8571-206">Si introduce cuatro dígitos, se interpretarán como el día y el mes, y agregará el año de la fecha de trabajo.</span><span class="sxs-lookup"><span data-stu-id="c8571-206">If you enter four digits, this is interpreted as the day and the month, and it will add the year of the work date.</span></span>  

-   <span data-ttu-id="c8571-207">Si la fecha que desea introducir está en el rango comprendido entre el 01/01/1930 y el 31/12/2029, puede introducir el año con dos dígitos; en caso contrario, introduzca el año mediante cuatro dígitos.</span><span class="sxs-lookup"><span data-stu-id="c8571-207">If the date you want to enter is in the range 01/01/1930 through 12/31/2029, you can enter the year with two digits; otherwise, enter the year with four digits.</span></span>  

<span data-ttu-id="c8571-208">También es posible introducir una fecha como un día de la semana, seguido de un número de la semana y, opcionalmente, un año (por ejemplo, Lun25 o lun25 significa lunes de la semana 25).</span><span class="sxs-lookup"><span data-stu-id="c8571-208">You can also enter a date as a weekday followed by a week number and, optionally, a year (for example, Mon25 or mon25 means Monday in week 25).</span></span>  

<span data-ttu-id="c8571-209">En lugar de introducir una fecha específica, puede introducir uno de estos códigos.</span><span class="sxs-lookup"><span data-stu-id="c8571-209">Instead of entering a specific date, you can enter one of these codes.</span></span>  

|<span data-ttu-id="c8571-210">Code</span><span class="sxs-lookup"><span data-stu-id="c8571-210">Code</span></span>|<span data-ttu-id="c8571-211">Resultado</span><span class="sxs-lookup"><span data-stu-id="c8571-211">Result</span></span>|  
|--------------|----------------|  
|<span data-ttu-id="c8571-212">h</span><span class="sxs-lookup"><span data-stu-id="c8571-212">t</span></span>|<span data-ttu-id="c8571-213">Esto especifica la fecha de hoy (la fecha de sistema del equipo).</span><span class="sxs-lookup"><span data-stu-id="c8571-213">This specifies today's date (the system date for the computer).</span></span>|  
|<span data-ttu-id="c8571-214">p</span><span class="sxs-lookup"><span data-stu-id="c8571-214">p</span></span>|<span data-ttu-id="c8571-215">Esto especifica un "período contable, donde `p` significa el primer período contable, `p2` significa el segundo período contable, y así sucesivamente.</span><span class="sxs-lookup"><span data-stu-id="c8571-215">This specifies an accounting period´, where `p`means the first accounting period, `p2` means the second accountin period, and so on.</span></span> |
|<span data-ttu-id="c8571-216">t</span><span class="sxs-lookup"><span data-stu-id="c8571-216">w</span></span>|<span data-ttu-id="c8571-217">Esto especifica la fecha de trabajo que está configurada en la aplicación.</span><span class="sxs-lookup"><span data-stu-id="c8571-217">This specifies the work date that is setup in the application.</span></span> <span data-ttu-id="c8571-218">Para cambiar la fecha de trabajo, vea [Cambiar la configuración básica](ui-change-basic-settings.md).</span><span class="sxs-lookup"><span data-stu-id="c8571-218">To change the work date, see [Changing Basic Settings](ui-change-basic-settings.md).</span></span> <span data-ttu-id="c8571-219">Una fecha de trabajo se puede usar si hay muchas operaciones con una fecha distinta a la activa.</span><span class="sxs-lookup"><span data-stu-id="c8571-219">You may want to use a work date if you have many transactions with a date other than today's date.</span></span>|
|<span data-ttu-id="c8571-220">c</span><span class="sxs-lookup"><span data-stu-id="c8571-220">c</span></span>|<span data-ttu-id="c8571-221">Esto especifica que la fecha después de `c` es una fecha de cierre, por ejemplo, `C123101`.</span><span class="sxs-lookup"><span data-stu-id="c8571-221">This specifies that the date after `c`is a closing date, for example `C123101`.</span></span>|  

## <a name="entering-times"></a><span data-ttu-id="c8571-222">Introducción de horas</span><span class="sxs-lookup"><span data-stu-id="c8571-222">Entering Times</span></span>

<span data-ttu-id="c8571-223">Cuando introduzca horas, puede insertar cualquier signo separador entre las unidades, aunque no es necesario.</span><span class="sxs-lookup"><span data-stu-id="c8571-223">When you enter times, you can insert any separator sign that you want between the units, but it is not required.</span></span> <span data-ttu-id="c8571-224">No necesita escribir los minutos, los segundo ni AM/PM.</span><span class="sxs-lookup"><span data-stu-id="c8571-224">You do not have to write minutes, seconds, or AM/PM.</span></span>  

<span data-ttu-id="c8571-225">En la tabla siguiente se muestran varias formas de introducir horas y cómo se interpretan.</span><span class="sxs-lookup"><span data-stu-id="c8571-225">The following table lists the various ways in which times can be entered and how they are interpreted.</span></span>  

|<span data-ttu-id="c8571-226">Movimiento</span><span class="sxs-lookup"><span data-stu-id="c8571-226">Entry</span></span>|<span data-ttu-id="c8571-227">Interpretación</span><span class="sxs-lookup"><span data-stu-id="c8571-227">Interpretation</span></span>|  
|---------------|------------------------|  
|<span data-ttu-id="c8571-228">5</span><span class="sxs-lookup"><span data-stu-id="c8571-228">5</span></span>|<span data-ttu-id="c8571-229">05:00:00</span><span class="sxs-lookup"><span data-stu-id="c8571-229">05:00:00</span></span>|  
|<span data-ttu-id="c8571-230">5:30</span><span class="sxs-lookup"><span data-stu-id="c8571-230">5:30</span></span>|<span data-ttu-id="c8571-231">05:30:00</span><span class="sxs-lookup"><span data-stu-id="c8571-231">05:30:00</span></span>|  
|<span data-ttu-id="c8571-232">0530</span><span class="sxs-lookup"><span data-stu-id="c8571-232">0530</span></span>|<span data-ttu-id="c8571-233">05:30:00</span><span class="sxs-lookup"><span data-stu-id="c8571-233">05:30:00</span></span>|  
|<span data-ttu-id="c8571-234">5:30:5</span><span class="sxs-lookup"><span data-stu-id="c8571-234">5:30:5</span></span>|<span data-ttu-id="c8571-235">05:30:05</span><span class="sxs-lookup"><span data-stu-id="c8571-235">05:30:05</span></span>|  
|<span data-ttu-id="c8571-236">053005</span><span class="sxs-lookup"><span data-stu-id="c8571-236">053005</span></span>|<span data-ttu-id="c8571-237">05:30:05</span><span class="sxs-lookup"><span data-stu-id="c8571-237">05:30:05</span></span>|  
|<span data-ttu-id="c8571-238">5:30:5.50</span><span class="sxs-lookup"><span data-stu-id="c8571-238">5:30:5,50</span></span>|<span data-ttu-id="c8571-239">05:30:05,5</span><span class="sxs-lookup"><span data-stu-id="c8571-239">05:30:05.5</span></span>|  
|<span data-ttu-id="c8571-240">053005050</span><span class="sxs-lookup"><span data-stu-id="c8571-240">053005050</span></span>|<span data-ttu-id="c8571-241">05:30:05.05</span><span class="sxs-lookup"><span data-stu-id="c8571-241">05:30:05.05</span></span>|  

 <span data-ttu-id="c8571-242">Debe introducir dos dígitos para cada unidad de tiempo si no escribe ningún separador.</span><span class="sxs-lookup"><span data-stu-id="c8571-242">You must enter two digits for each unit of time if you do not enter a separator.</span></span>  

## <a name="entering-datetimes"></a><span data-ttu-id="c8571-243">Introducción de fechas/horas</span><span class="sxs-lookup"><span data-stu-id="c8571-243">Entering Datetimes</span></span>

<span data-ttu-id="c8571-244">Cuando introduzca fechas y horas, debe introducir un espacio en blanco entre la fecha y la hora.</span><span class="sxs-lookup"><span data-stu-id="c8571-244">When you enter datetimes you must enter a space between the date and the time.</span></span>  

<span data-ttu-id="c8571-245">En la tabla siguiente se muestran varias formas de introducir fechas y horas y cómo se interpretan.</span><span class="sxs-lookup"><span data-stu-id="c8571-245">The following table lists the various ways in which you can enter datetimes and how they are interpreted.</span></span>  

|<span data-ttu-id="c8571-246">Movimiento</span><span class="sxs-lookup"><span data-stu-id="c8571-246">Entry</span></span>|<span data-ttu-id="c8571-247">Interpretación</span><span class="sxs-lookup"><span data-stu-id="c8571-247">Interpretation</span></span>|  
|---------------|------------------------|  
|<span data-ttu-id="c8571-248">131202 132455</span><span class="sxs-lookup"><span data-stu-id="c8571-248">131202 132455</span></span>|<span data-ttu-id="c8571-249">13-12-02 13:24:55</span><span class="sxs-lookup"><span data-stu-id="c8571-249">13-12-02 13:24:55</span></span>|  
|<span data-ttu-id="c8571-250">1-12-02 10</span><span class="sxs-lookup"><span data-stu-id="c8571-250">1-12-02 10</span></span>|<span data-ttu-id="c8571-251">01-12-02 10:00:00</span><span class="sxs-lookup"><span data-stu-id="c8571-251">01-12-02 10:00:00</span></span>|  
|<span data-ttu-id="c8571-252">1.12.02 5</span><span class="sxs-lookup"><span data-stu-id="c8571-252">1.12.02 5</span></span>|<span data-ttu-id="c8571-253">01-12-02 05:00:00</span><span class="sxs-lookup"><span data-stu-id="c8571-253">01-12-02 05:00:00</span></span>|  
|<span data-ttu-id="c8571-254">1.12.02</span><span class="sxs-lookup"><span data-stu-id="c8571-254">1.12.02</span></span>|<span data-ttu-id="c8571-255">01-12-02 00:00:00</span><span class="sxs-lookup"><span data-stu-id="c8571-255">01-12-02 00:00:00</span></span>|  
|<span data-ttu-id="c8571-256">11 12</span><span class="sxs-lookup"><span data-stu-id="c8571-256">11 12</span></span>|<span data-ttu-id="c8571-257">11-mes actual-año actual 12:00:00</span><span class="sxs-lookup"><span data-stu-id="c8571-257">11-current month-current year 12:00:00</span></span>|  
|<span data-ttu-id="c8571-258">1112 12</span><span class="sxs-lookup"><span data-stu-id="c8571-258">1112 12</span></span>|<span data-ttu-id="c8571-259">11-12-año actual 12:00:00</span><span class="sxs-lookup"><span data-stu-id="c8571-259">11-12-current year 12:00:00</span></span>|  
|<span data-ttu-id="c8571-260">h u hoy</span><span class="sxs-lookup"><span data-stu-id="c8571-260">t or today</span></span>|<span data-ttu-id="c8571-261">fecha de hoy 00:00:00</span><span class="sxs-lookup"><span data-stu-id="c8571-261">today's date 00:00:00</span></span>|  
|<span data-ttu-id="c8571-262">h hora</span><span class="sxs-lookup"><span data-stu-id="c8571-262">t time</span></span>|<span data-ttu-id="c8571-263">fecha de hoy hora real</span><span class="sxs-lookup"><span data-stu-id="c8571-263">today's date actual time</span></span>|  
|<span data-ttu-id="c8571-264">t 10:30</span><span class="sxs-lookup"><span data-stu-id="c8571-264">t 10:30</span></span>|<span data-ttu-id="c8571-265">fecha de hoy 10:30:00</span><span class="sxs-lookup"><span data-stu-id="c8571-265">today's date 10:30:00</span></span>|  
|<span data-ttu-id="c8571-266">h 3:3:3</span><span class="sxs-lookup"><span data-stu-id="c8571-266">t 3:3:3</span></span>|<span data-ttu-id="c8571-267">fecha de hoy 03:03:03</span><span class="sxs-lookup"><span data-stu-id="c8571-267">today's date 03:03:03</span></span>|  
|<span data-ttu-id="c8571-268">l o fecha de trabajo</span><span class="sxs-lookup"><span data-stu-id="c8571-268">w or workdate</span></span>|<span data-ttu-id="c8571-269">la fecha de trabajo 00:00:00</span><span class="sxs-lookup"><span data-stu-id="c8571-269">the working date 00:00:00</span></span>|  
|<span data-ttu-id="c8571-270">l o lunes</span><span class="sxs-lookup"><span data-stu-id="c8571-270">m or Monday</span></span>|<span data-ttu-id="c8571-271">Lunes de la semana actual 00:00:00</span><span class="sxs-lookup"><span data-stu-id="c8571-271">Monday of the current week 00:00:00</span></span>|  
|<span data-ttu-id="c8571-272">ma o martes</span><span class="sxs-lookup"><span data-stu-id="c8571-272">tu or Tuesday</span></span>|<span data-ttu-id="c8571-273">Martes de la semana actual 00:00:00</span><span class="sxs-lookup"><span data-stu-id="c8571-273">Tuesday of the current week 00:00:00</span></span>|  
|<span data-ttu-id="c8571-274">mi o miércoles</span><span class="sxs-lookup"><span data-stu-id="c8571-274">we or Wednesday</span></span>|<span data-ttu-id="c8571-275">Miércoles de la semana actual 00:00:00</span><span class="sxs-lookup"><span data-stu-id="c8571-275">Wednesday of the current week 00:00:00</span></span>|  
|<span data-ttu-id="c8571-276">ju o jueves</span><span class="sxs-lookup"><span data-stu-id="c8571-276">th or Thursday</span></span>|<span data-ttu-id="c8571-277">Jueves de la semana actual 00:00:00</span><span class="sxs-lookup"><span data-stu-id="c8571-277">Thursday of the current week 00:00:00</span></span>|  
|<span data-ttu-id="c8571-278">v o viernes</span><span class="sxs-lookup"><span data-stu-id="c8571-278">f or Friday</span></span>|<span data-ttu-id="c8571-279">Viernes de la semana actual 00:00:00</span><span class="sxs-lookup"><span data-stu-id="c8571-279">Friday of the current week 00:00:00</span></span>|  
|<span data-ttu-id="c8571-280">s o sábado</span><span class="sxs-lookup"><span data-stu-id="c8571-280">s or Saturday</span></span>|<span data-ttu-id="c8571-281">Sábado de la semana actual 00:00:00</span><span class="sxs-lookup"><span data-stu-id="c8571-281">Saturday of the current week 00:00:00</span></span>|  
|<span data-ttu-id="c8571-282">do o domingo</span><span class="sxs-lookup"><span data-stu-id="c8571-282">su or Sunday</span></span>|<span data-ttu-id="c8571-283">Domingo de la semana actual 00:00:00</span><span class="sxs-lookup"><span data-stu-id="c8571-283">Sunday of the current week 00:00:00</span></span>|  
|<span data-ttu-id="c8571-284">ma 10:30</span><span class="sxs-lookup"><span data-stu-id="c8571-284">tu 10:30</span></span>|<span data-ttu-id="c8571-285">Martes de la semana actual 10:30:00</span><span class="sxs-lookup"><span data-stu-id="c8571-285">Tuesday of the current week 10:30:00</span></span>|  
|<span data-ttu-id="c8571-286">ma 3:3:3</span><span class="sxs-lookup"><span data-stu-id="c8571-286">tu 3:3:3</span></span>|<span data-ttu-id="c8571-287">Martes de la semana actual 03:03:03</span><span class="sxs-lookup"><span data-stu-id="c8571-287">Tuesday of the current week 03:03:03</span></span>|  

## <a name="entering-duration"></a><span data-ttu-id="c8571-288">Introducción de duración</span><span class="sxs-lookup"><span data-stu-id="c8571-288">Entering Duration</span></span>

<span data-ttu-id="c8571-289">Introduzca un periodo de tiempo como un número seguido de su unidad de medida.</span><span class="sxs-lookup"><span data-stu-id="c8571-289">You enter a duration as a number followed by its unit of measure.</span></span>  

<span data-ttu-id="c8571-290">A continuación se muestran algunos ejemplos.</span><span class="sxs-lookup"><span data-stu-id="c8571-290">Here are some examples.</span></span>  

|<span data-ttu-id="c8571-291">Duración</span><span class="sxs-lookup"><span data-stu-id="c8571-291">Duration</span></span>|<span data-ttu-id="c8571-292">Unidad de medida\*\*</span><span class="sxs-lookup"><span data-stu-id="c8571-292">Unit of measure\*\*</span></span>|  
|------------------|-------------------------|  
|<span data-ttu-id="c8571-293">2h</span><span class="sxs-lookup"><span data-stu-id="c8571-293">2h</span></span>|<span data-ttu-id="c8571-294">2 hrs</span><span class="sxs-lookup"><span data-stu-id="c8571-294">2 hrs</span></span>|  
|<span data-ttu-id="c8571-295">6h 30 m</span><span class="sxs-lookup"><span data-stu-id="c8571-295">6h 30 m</span></span>|<span data-ttu-id="c8571-296">6 hrs 30 mins</span><span class="sxs-lookup"><span data-stu-id="c8571-296">6 hrs 30 mins</span></span>|  
|<span data-ttu-id="c8571-297">6,5h</span><span class="sxs-lookup"><span data-stu-id="c8571-297">6.5h</span></span>|<span data-ttu-id="c8571-298">6 h 30 min</span><span class="sxs-lookup"><span data-stu-id="c8571-298">6 hrs 30 mins</span></span>|  
|<span data-ttu-id="c8571-299">90m</span><span class="sxs-lookup"><span data-stu-id="c8571-299">90m</span></span>|<span data-ttu-id="c8571-300">1 hr 30 mins</span><span class="sxs-lookup"><span data-stu-id="c8571-300">1 hr 30 mins</span></span>|  
|<span data-ttu-id="c8571-301">2d 6h 30m</span><span class="sxs-lookup"><span data-stu-id="c8571-301">2d 6h 30m</span></span>|<span data-ttu-id="c8571-302">2 días 6 hrs 30 mins</span><span class="sxs-lookup"><span data-stu-id="c8571-302">2 days 6 hrs 30 mins</span></span>|  
|<span data-ttu-id="c8571-303">2d 6h 30m 56s 600ms</span><span class="sxs-lookup"><span data-stu-id="c8571-303">2d 6h 30m 56s 600ms</span></span>|<span data-ttu-id="c8571-304">2 días 6 hrs 30 mins 56 segs 600 msegs</span><span class="sxs-lookup"><span data-stu-id="c8571-304">2 days 6 hrs 30 mins 56 secs 600 msecs</span></span>|  

 <span data-ttu-id="c8571-305">También puede introducir un número y se convertirá automáticamente en un periodo de tiempo.</span><span class="sxs-lookup"><span data-stu-id="c8571-305">You can also enter a number and it is automatically converted to a duration.</span></span> <span data-ttu-id="c8571-306">El número que introduzca se convierte según la unidad de medida predeterminada que se ha especificado en el campo Duración.</span><span class="sxs-lookup"><span data-stu-id="c8571-306">The number you enter is converted according to the default unit of measure that has been specified for the duration field.</span></span>  

 <span data-ttu-id="c8571-307">Para ver la unidad de medida que se va a usar en un campo Duración, introduzca un número y observe a qué unidad de medida se convierte.</span><span class="sxs-lookup"><span data-stu-id="c8571-307">To see what unit of measure is being used in a duration field, enter a number and see which unit of measure it is converted to.</span></span>  

 <span data-ttu-id="c8571-308">El número 5 se convierte a 5 hrs, si la unidad de medida es horas.</span><span class="sxs-lookup"><span data-stu-id="c8571-308">The number 5 is converted to 5 hrs, if the unit of measure is hours.</span></span>  

<!--OnPrem  ##  <a name="BKMK_SettingDateRanges"></a> Setting Date Ranges  
 You can set filters containing a start date and an end date to display only the data contained in that date range or time interval. Special rules apply to the way you set date ranges.  

|**Meaning**|**Sample expression**|**Entries included**|  
|-----------------|---------------------------|--------------------------|  
|**Equal to**|12 15 00|Only those posted on 12 15 00.|  
|**Interval**|12 15 00..01 15 01<br /><br /> ..12 15 00|Those posted on dates between and including 12 15 00 and 01 15 01.<br /><br /> Those posted on 12 15 00 or earlier.|  
|**Either/or**|12 15 00&#124;12 16 00|Those posted on either 12 15 00 or 12 16 00. If there are entries posted on both days, they will all be displayed.|  

 You can also combine the various format types.  

|**Sample expression**|**Entries included**|  
|---------------------------|--------------------------|  
|12 15 00&#124;12 01 00..12 10 00|Entries posted either on 12 15 00 or on dates between and including 12 01 00 and 12 10 00.|  
|..12 14 00&#124;12 30 00..|Entries posted on 12 14 00 or earlier, or entries posted on 12 30 00 or later - that is, all entries except those posted on dates between and including 12 15 00 and 12 29 00.|

## Using Date Formulas

 A date formula is a short, abbreviated combination of letters and numbers that specifies how to calculate dates. You can enter date formulas in various date calculation fields and in recurring frequency fields in recurring journals.  

> [!NOTE]  
>  In all data formula fields, one day is automatically included to cover today as the day when the period starts. Accordingly, if you enter 1W, for example, then the period is actually eight days because today is included. To specify a period of seven days (one true week) including the period starting date, then you must enter 6D or 1W-1D.  

 Here are some examples of how date formulas can be used:  

-   The date formula in the recurring frequency field in recurring journals determines how often the entry on the journal line will be posted.  

-   The date formula in the Grace Period field for a specified reminder level determines the period of time that must pass from the due date (or from the date of the previous reminder) before a reminder will be created.  

-   The date formula in the Due Date Calculation field determines how to calculate the due date on the reminder.  

 The date calculation formula can contain a maximum of 20 characters, both numbers and letters. You can use the following letters, which are abbreviations for time specifications.  

|||  
|-|-|  
|C|Current|  
|D|Day(s)|  
|W|Week(s)|  
|M|Month(s)|  
|Q|Quarter(s)|  
|Y|Year(s)|  

 You can construct a date formula in three ways.  

 The following example shows how current plus a time unit.  

|||  
|-|-|  
|CW|Current week|  
|CM|Current month|  

 The following example shows how a number and a time unit. A number cannot be larger than 9999.  

|||  
|-|-|  
|10D|10 days from today|  
|2W|2 weeks from today|  

 The following example shows how a time unit and a number.  

|||  
|-|-|  
|D10|The next 10th day of a month|  
|WD4|The next 4th day of a week (Thursday)|  

 The following example shows how you can combine these three forms as needed.  

|||  
|-|-|  
|CM+10D|Current month + 10 days|  

 The following example shows how you can use a minus sign to indicate a date in the past.  

|||  
|-|-|  
|-1Y|1 year ago from today|

[!CAUTION]  
>  If the location uses a base calendar, then the date formula that you enter in, for example, the **Shipping Time** field is interpreted according to the calendar working days. For example, a 1W means seven working days. For more information, see Base Calendar Card.-->

## <a name="see-also"></a><span data-ttu-id="c8571-309">Consulte también</span><span class="sxs-lookup"><span data-stu-id="c8571-309">See Also</span></span>  
 [<span data-ttu-id="c8571-310">Ordenar, buscar y filtrar listas</span><span class="sxs-lookup"><span data-stu-id="c8571-310">Sorting, Searching, and Filtering Lists</span></span>](ui-enter-criteria-filters.md)  
 <span data-ttu-id="c8571-311">[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="c8571-311">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
