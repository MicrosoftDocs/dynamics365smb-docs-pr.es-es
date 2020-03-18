---
title: Crear objetos XMLports basados en esquemas XML | Documentos de Microsoft
description: Utilice los esquemas XML para configurar el marco de intercambio de documentos.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 65392cc5f47353b9266d5198b739835fd329c204
ms.sourcegitcommit: d0dc5e5c46b932899e2a9c7183959d0ff37738d6
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 02/20/2020
ms.locfileid: "3076688"
---
# <a name="use-xml-schemas-to-prepare-data-exchange-definitions"></a><span data-ttu-id="e8c3b-103">Uso de esquemas XML para preparar definiciones de intercambio de datos</span><span class="sxs-lookup"><span data-stu-id="e8c3b-103">Use XML Schemas to Prepare Data Exchange Definitions</span></span>
<span data-ttu-id="e8c3b-104">Para habilitar la importación y exportación de datos en archivos XML mediante el marco de intercambio de datos en [!INCLUDE[d365fin](includes/d365fin_md.md)], puede usar esquemas XML de los archivos para definir los elementos de datos que desea intercambiar con [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="e8c3b-104">To enable import/export of data in XML files through the data exchange framework in [!INCLUDE[d365fin](includes/d365fin_md.md)], you can use XML schemas to define which data elements you want to exchange with [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="e8c3b-105">Este trabajo se realiza en la página **Visor de esquema XML** mediante la carga del archivo de esquema XML, la selección de los elementos de datos pertinentes y la inicialización de una definición de intercambio de datos o un objeto XMLport.</span><span class="sxs-lookup"><span data-stu-id="e8c3b-105">You perform this work on the **XML Schema Viewer** page by loading the XML schema file, selecting the relevant data elements, and then initializing either a data exchange definition or an XMLport.</span></span>  

 <span data-ttu-id="e8c3b-106">Cuando haya definido qué elementos de datos se incluirán según el esquema XML, puede usar la acción **Generar XMLport** a fin de crear el objeto XMLport.</span><span class="sxs-lookup"><span data-stu-id="e8c3b-106">When you have defined which data elements to include based on the XML schema, you can use the **Generate XMLport** action to create the XMLport object.</span></span>  

 <span data-ttu-id="e8c3b-107">También puede utilizar la acción **Generar definición de intercambio de datos** para inicializar una definición de intercambio de datos en los datos seleccionados, que después podrá completar en el marco de intercambio de datos.</span><span class="sxs-lookup"><span data-stu-id="e8c3b-107">Alternatively, you can use the **Generate Data Exchange Definition** action to initialize a data exchange definition based on the selected data elements, which you then complete in the Data Exchange Framework.</span></span> <span data-ttu-id="e8c3b-108">Esto crea un registro en la página **Definiciones de intercambio de registro**, donde se continúa con la definición de qué elementos del archivo se asignan a qué campos de [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="e8c3b-108">This creates a record on the **Posting Exchange Definition** page where you continue by defining which elements in the file map to which fields in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="e8c3b-109">Para obtener más información, vea [Configurar las definiciones de intercambio de datos](across-how-to-set-up-data-exchange-definitions.md).</span><span class="sxs-lookup"><span data-stu-id="e8c3b-109">For more information, see [Set Up Data Exchange Definitions](across-how-to-set-up-data-exchange-definitions.md).</span></span>  

 <span data-ttu-id="e8c3b-110">Este tema incluye los siguientes procedimientos:</span><span class="sxs-lookup"><span data-stu-id="e8c3b-110">This topic contains the following procedures:</span></span>  

-   <span data-ttu-id="e8c3b-111">Para cargar un archivo de esquema XML</span><span class="sxs-lookup"><span data-stu-id="e8c3b-111">To load an XML schema file</span></span>  

-   <span data-ttu-id="e8c3b-112">Para seleccionar o borrar nodos en un esquema XML</span><span class="sxs-lookup"><span data-stu-id="e8c3b-112">To select or clear nodes in an XML schema</span></span>  

-   <span data-ttu-id="e8c3b-113">Para generar una definición de intercambio de datos basada en un esquema XML</span><span class="sxs-lookup"><span data-stu-id="e8c3b-113">To generate a data exchange definition that is based on an XML schema</span></span>  

-   <span data-ttu-id="e8c3b-114">Para generar un objeto XMLport para el archivo basado en un esquema XML</span><span class="sxs-lookup"><span data-stu-id="e8c3b-114">To generate an XMLport for the file that is based on an XML schema</span></span>  

-   <span data-ttu-id="e8c3b-115">Para importar un objeto XMLport en Object Designer</span><span class="sxs-lookup"><span data-stu-id="e8c3b-115">To import an XMLport into the Object Designer</span></span>  

### <a name="to-load-an-xml-schema-file"></a><span data-ttu-id="e8c3b-116">Para cargar un archivo de esquema XML</span><span class="sxs-lookup"><span data-stu-id="e8c3b-116">To load an XML schema file</span></span>  

1.  <span data-ttu-id="e8c3b-117">Asegúrese de que esté disponible el archivo de esquema XML.</span><span class="sxs-lookup"><span data-stu-id="e8c3b-117">Make sure that the relevant XML schema file is available.</span></span> <span data-ttu-id="e8c3b-118">La extensión de archivo es .xsd.</span><span class="sxs-lookup"><span data-stu-id="e8c3b-118">The file extension is .xsd.</span></span>  

2.  <span data-ttu-id="e8c3b-119">Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Esquemas XML** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="e8c3b-119">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **XML Schemas**, and then choose the related link.</span></span>  

3.  <span data-ttu-id="e8c3b-120">Seleccione la acción **Nuevo**.</span><span class="sxs-lookup"><span data-stu-id="e8c3b-120">Choose the **New** action.</span></span>  

4.  <span data-ttu-id="e8c3b-121">Rellene los campos tal como se describe en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="e8c3b-121">Fill the fields as described in the following table.</span></span>  

    |<span data-ttu-id="e8c3b-122">Campo</span><span class="sxs-lookup"><span data-stu-id="e8c3b-122">Field</span></span>|<span data-ttu-id="e8c3b-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="e8c3b-123">Description</span></span>|  
    |---------------------------------|---------------------------------------|  
    |<span data-ttu-id="e8c3b-124">**Código**</span><span class="sxs-lookup"><span data-stu-id="e8c3b-124">**Code**</span></span>|<span data-ttu-id="e8c3b-125">Especifique un código para identificar el esquema XML.</span><span class="sxs-lookup"><span data-stu-id="e8c3b-125">Specify a code to identify the XML schema.</span></span>|  
    |<span data-ttu-id="e8c3b-126">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="e8c3b-126">**Description**</span></span>|<span data-ttu-id="e8c3b-127">Especifique una descripción del esquema XML.</span><span class="sxs-lookup"><span data-stu-id="e8c3b-127">Specify a description of the XML schema.</span></span>|  

     <span data-ttu-id="e8c3b-128">El campo **Espacio de nombres de destino** especifica cualquier espacio de nombres del archivo de esquema XML que se ha cargado para la línea.</span><span class="sxs-lookup"><span data-stu-id="e8c3b-128">The **Target Namespace** field specifies any namespace in the XML schema file that has been loaded for the line.</span></span>  

5.  <span data-ttu-id="e8c3b-129">Elija la acción **Cargar esquema** y luego seleccione el archivo de esquema XML.</span><span class="sxs-lookup"><span data-stu-id="e8c3b-129">Choose the **Load Schema** action, and then select the XML schema file.</span></span>  

     <span data-ttu-id="e8c3b-130">Cuando se carga el archivo, los demás campos de la línea se rellenan con la información del archivo y se selecciona la casilla **Esquema cargado**.</span><span class="sxs-lookup"><span data-stu-id="e8c3b-130">When the file is loaded, the rest of the fields on the line are filled with information from the file, and the **Schema is Loaded** check box is selected.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="e8c3b-131">El árbol del esquema XML cargado está contraído de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="e8c3b-131">The tree of the loaded XML schema is collapsed by default.</span></span> <span data-ttu-id="e8c3b-132">Puede ampliar cada nodo eligiendo el botón **+** en el nodo.</span><span class="sxs-lookup"><span data-stu-id="e8c3b-132">You expand each node by choosing the **+** button on the node.</span></span> <span data-ttu-id="e8c3b-133">Para expandir todos los nodos, seleccione **Expandir todo** en la cinta.</span><span class="sxs-lookup"><span data-stu-id="e8c3b-133">To expand all nodes, choose **Expand All** on the ribbon.</span></span>  

### <a name="to-select-or-clear-nodes-in-an-xml-schema"></a><span data-ttu-id="e8c3b-134">Para seleccionar o borrar nodos en un esquema XML</span><span class="sxs-lookup"><span data-stu-id="e8c3b-134">To select or clear nodes in an XML schema</span></span>  

1.  <span data-ttu-id="e8c3b-135">Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Visor de esquemas XML** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="e8c3b-135">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **XML Schema Viewer**, and then choose the related link.</span></span>  

2.  <span data-ttu-id="e8c3b-136">Rellene los campos en la cabecera tal como se describe en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="e8c3b-136">Fill the fields on the header as described in the following table.</span></span>  

    |<span data-ttu-id="e8c3b-137">Campo</span><span class="sxs-lookup"><span data-stu-id="e8c3b-137">Field</span></span>|<span data-ttu-id="e8c3b-138">Descripción</span><span class="sxs-lookup"><span data-stu-id="e8c3b-138">Description</span></span>|  
    |---------------------------------|---------------------------------------|  
    |<span data-ttu-id="e8c3b-139">**Código de esquema XML**</span><span class="sxs-lookup"><span data-stu-id="e8c3b-139">**XML Schema Code**</span></span>|<span data-ttu-id="e8c3b-140">Especifique el archivo de esquema XML que se ha cargado en el paso 5 en la sección “Para cargar un archivo de esquema XML”.</span><span class="sxs-lookup"><span data-stu-id="e8c3b-140">Specify the XML schema file that you loaded in step 5 in the “To load an XML schema file” section.</span></span>|  
    |<span data-ttu-id="e8c3b-141">**Nuevo nº de XMLport**</span><span class="sxs-lookup"><span data-stu-id="e8c3b-141">**New XMLport No.**</span></span>|<span data-ttu-id="e8c3b-142">Especifique el número del objeto XMLport que se crea a partir de este esquema de XML cuando elige la acción **Generar XMLport**.</span><span class="sxs-lookup"><span data-stu-id="e8c3b-142">Specify the number of the XMLport that is created from this XML schema when you choose the **Generate XMLport** action.</span></span>|  

     <span data-ttu-id="e8c3b-143">Las líneas ahora se rellenan con nodos que representan todos los elementos del esquema XML.</span><span class="sxs-lookup"><span data-stu-id="e8c3b-143">The lines are now filled with nodes representing all elements in the XML schema.</span></span> <span data-ttu-id="e8c3b-144">Los nodos de los elementos que son obligatorios según el esquema XML están seleccionados de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="e8c3b-144">Nodes for elements that are mandatory according to the XML schema are selected by default.</span></span>  

3.  <span data-ttu-id="e8c3b-145">En la primera línea, en la columna **Nombre de nodo**, expanda el nodo **Documento** y, a continuación expanda gradualmente los nodos subyacentes que desea revisar.</span><span class="sxs-lookup"><span data-stu-id="e8c3b-145">On the first line, in the **Node Name** column, expand the **Document** node, and then gradually expand underlying nodes that you want to review.</span></span>  

     <span data-ttu-id="e8c3b-146">También puede hacer clic con el botón secundario en un nodo y elegir **Expandir todo**.</span><span class="sxs-lookup"><span data-stu-id="e8c3b-146">Alternatively, right-click on a node and then choose **Expand All**.</span></span>  

4.  <span data-ttu-id="e8c3b-147">Elija cualquiera de las acciones siguientes para cambiar los nodos que se muestran.</span><span class="sxs-lookup"><span data-stu-id="e8c3b-147">Choose either of the following actions to change which nodes are displayed.</span></span>  

    |<span data-ttu-id="e8c3b-148">**Acción**</span><span class="sxs-lookup"><span data-stu-id="e8c3b-148">**Action**</span></span>|<span data-ttu-id="e8c3b-149">Descripción</span><span class="sxs-lookup"><span data-stu-id="e8c3b-149">Description</span></span>|  
    |----------------|---------------------------------------|  
    |<span data-ttu-id="e8c3b-150">**Mostrar todos**</span><span class="sxs-lookup"><span data-stu-id="e8c3b-150">**Show All**</span></span>|<span data-ttu-id="e8c3b-151">Se muestran todos los nodos.</span><span class="sxs-lookup"><span data-stu-id="e8c3b-151">All nodes are shown.</span></span>|  
    |<span data-ttu-id="e8c3b-152">**Ocultar elementos opcionales**</span><span class="sxs-lookup"><span data-stu-id="e8c3b-152">**Hide Non-Mandatory**</span></span>|<span data-ttu-id="e8c3b-153">Solo se muestran los nodos que representan elementos que son obligatorios según el esquema XML.</span><span class="sxs-lookup"><span data-stu-id="e8c3b-153">Only nodes representing elements that are required according to the XML schema are shown.</span></span> <span data-ttu-id="e8c3b-154">Estos nodos normalmente se indican mediante un **1** en el campo **MinOccurs**.</span><span class="sxs-lookup"><span data-stu-id="e8c3b-154">These nodes are typically indicated by a **1** in the **MinOccurs** field.</span></span><br /><br /> <span data-ttu-id="e8c3b-155">Elija **Mostrar todos** para revertir la vista.</span><span class="sxs-lookup"><span data-stu-id="e8c3b-155">Choose **Show All** to reverse the view.</span></span>|  
    |<span data-ttu-id="e8c3b-156">**Ocultar elementos no seleccionados**</span><span class="sxs-lookup"><span data-stu-id="e8c3b-156">**Hide Non-Selected**</span></span>|<span data-ttu-id="e8c3b-157">Solo se muestran los nodos donde está seleccionada la casilla **Seleccionado**.</span><span class="sxs-lookup"><span data-stu-id="e8c3b-157">Only nodes where the **Selected** check box is selected are shown.</span></span><br /><br /> <span data-ttu-id="e8c3b-158">Elija **Mostrar todos** para revertir la vista.</span><span class="sxs-lookup"><span data-stu-id="e8c3b-158">Choose **Show All** to reverse the view.</span></span>|  

5.  <span data-ttu-id="e8c3b-159">Seleccione la acción **Editar**.</span><span class="sxs-lookup"><span data-stu-id="e8c3b-159">Choose the **Edit** action.</span></span>  

6.  <span data-ttu-id="e8c3b-160">En la casilla **Seleccionado**, especifique para cada nodo si desea que el elemento se admita en la definición de intercambio de datos para el archivo bancario SEPA relacionado.</span><span class="sxs-lookup"><span data-stu-id="e8c3b-160">In the **Selected** check box, specify for each node if you want the element to be supported in the data exchange definition for the related SEPA bank file.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="e8c3b-161">Al seleccionar un nodo secundario obligatorio, también se seleccionan todos los nodos principales por encima de él.</span><span class="sxs-lookup"><span data-stu-id="e8c3b-161">When you select a mandatory child node, all parent nodes above it are also selected.</span></span>  

7.  <span data-ttu-id="e8c3b-162">Elija la acción **Seleccionar todos los elementos obligatorios** para reelegir todos los nodos que representen elementos obligatorios según el esquema XML.</span><span class="sxs-lookup"><span data-stu-id="e8c3b-162">Choose the **Select All Mandatory Elements** action to reselect all nodes that represent elements that are mandatory according to the XML schema.</span></span>  

8.  <span data-ttu-id="e8c3b-163">Elija la acción **Anular selección** para borrar todas las selecciones.</span><span class="sxs-lookup"><span data-stu-id="e8c3b-163">Choose the **Deselect All** action to clear all selections.</span></span>  

     <span data-ttu-id="e8c3b-164">El campo **Opción** especifica que el nodo tiene dos o más nodos de hermano que funcionan como opciones.</span><span class="sxs-lookup"><span data-stu-id="e8c3b-164">The **Choice** field specifies that the node has two or more sibling nodes that function as options.</span></span>  

### <a name="to-generate-a-data-exchange-definition-that-is-based-on-an-xml-schema"></a><span data-ttu-id="e8c3b-165">Para generar una definición de intercambio de datos basada en un esquema XML</span><span class="sxs-lookup"><span data-stu-id="e8c3b-165">To generate a data exchange definition that is based on an XML schema</span></span>  

1.  <span data-ttu-id="e8c3b-166">Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Esquemas XML** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="e8c3b-166">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter  **XML Schemas**, and then choose the related link.</span></span>  

2.  <span data-ttu-id="e8c3b-167">Seleccione el esquema XML relevante y luego elija la acción **Abrir Visor de esquema XML**.</span><span class="sxs-lookup"><span data-stu-id="e8c3b-167">Select the relevant XML schema, and then choose the **Open XML Schema Viewer** action.</span></span>  

3.  <span data-ttu-id="e8c3b-168">Asegúrese de que estén seleccionados los nodos correspondientes.</span><span class="sxs-lookup"><span data-stu-id="e8c3b-168">Make sure the relevant nodes are selected.</span></span> <span data-ttu-id="e8c3b-169">Para obtener más información, consulte la sección "Para seleccionar o borrar nodos en un esquema XML".</span><span class="sxs-lookup"><span data-stu-id="e8c3b-169">For more information, see the “To select or clear nodes in an XML schema” section.</span></span>  

4.  <span data-ttu-id="e8c3b-170">En la página **Visor de esquemas XML**, elija la acción **Generar definición de intercambio de datos**.</span><span class="sxs-lookup"><span data-stu-id="e8c3b-170">On the **XML Schema Viewer** page, choose the **Generate Data Exchange Definition** action.</span></span>  

 <span data-ttu-id="e8c3b-171">Se crea una definición de intercambio de datos en la página **Definiciones de intercambio de registro**, que se puede completar especificando qué elementos del archivo de banco SEPA se corresponden con los campos de [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="e8c3b-171">A data exchange definition is created on the **Posting Exchange Definition** page, which you can complete by specifying which elements in the file map to which fields in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="e8c3b-172">Para obtener más información, vea [Configurar las definiciones de intercambio de datos](across-how-to-set-up-data-exchange-definitions.md).</span><span class="sxs-lookup"><span data-stu-id="e8c3b-172">For more information, see [Set Up Data Exchange Definitions](across-how-to-set-up-data-exchange-definitions.md).</span></span>  

> [!NOTE]  
>  <span data-ttu-id="e8c3b-173">También puede utilizar la función **Obtener estructura de archivo** desde la página **Definiciones de intercambio de registro**, la cual utiliza la funcionalidad de la página **Visor esquemas XML** para prellenar la ficha desplegable **Definiciones de columna**.</span><span class="sxs-lookup"><span data-stu-id="e8c3b-173">You can also use the **Get File Structure** function from the **Posting Exchange Definition** page, which uses the functionality of the **XML Schema Viewer** page to prefill the **Column Definitions** TastTab.</span></span>  

### <a name="to-generate-an-xmlport-that-is-based-on-an-xml-schema"></a><span data-ttu-id="e8c3b-174">Para generar un objeto XMLport basado en un esquema XML</span><span class="sxs-lookup"><span data-stu-id="e8c3b-174">To generate an XMLport that is based on an XML schema</span></span>  

1.  <span data-ttu-id="e8c3b-175">Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Esquemas XML** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="e8c3b-175">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter  **XML Schemas**, and then choose the related link.</span></span>  

2.  <span data-ttu-id="e8c3b-176">Seleccione el esquema XML relevante y luego elija la acción **Abrir Visor de esquema XML**.</span><span class="sxs-lookup"><span data-stu-id="e8c3b-176">Select the relevant XML schema, and then choose the **Open XML Schema Viewer** action.</span></span>  

3.  <span data-ttu-id="e8c3b-177">En el campo **N.º XMLport nuevo**</span><span class="sxs-lookup"><span data-stu-id="e8c3b-177">In the **New XMLport No.**</span></span> <span data-ttu-id="e8c3b-178">especifique el número que recibirá el nuevo objeto XMLport cuando se genere.</span><span class="sxs-lookup"><span data-stu-id="e8c3b-178">field, specify the number that the new XMLport object will be given when it is generated.</span></span>  

4.  <span data-ttu-id="e8c3b-179">Asegúrese de que estén seleccionados los nodos correspondientes.</span><span class="sxs-lookup"><span data-stu-id="e8c3b-179">Make sure the relevant nodes are selected.</span></span> <span data-ttu-id="e8c3b-180">Para obtener más información, consulte la sección "Para seleccionar o borrar nodos en un esquema XML".</span><span class="sxs-lookup"><span data-stu-id="e8c3b-180">For more information, see the “To select or clear nodes in an XML schema” section.</span></span>  

5.  <span data-ttu-id="e8c3b-181">Elija la acción **Generar XMLport** y, a continuación, guarde el objeto como un archivo .txt en un almacén adecuado.</span><span class="sxs-lookup"><span data-stu-id="e8c3b-181">Choose the **Generate XMLport** action, and then save the object as a .txt file in an appropriate location.</span></span>  

6. <span data-ttu-id="e8c3b-182">Importe el nuevo XMLport en el entorno de desarrollo de [!INCLUDE[d365fin](includes/d365fin_md.md)] y compílelo.</span><span class="sxs-lookup"><span data-stu-id="e8c3b-182">Import the new XMLport into the [!INCLUDE[d365fin](includes/d365fin_md.md)] development environment and compile it.</span></span>

## <a name="see-also"></a><span data-ttu-id="e8c3b-183">Consulte también</span><span class="sxs-lookup"><span data-stu-id="e8c3b-183">See Also</span></span>  
<span data-ttu-id="e8c3b-184">[Configurar definiciones de intercambio de datos](across-how-to-set-up-data-exchange-definitions.md) </span><span class="sxs-lookup"><span data-stu-id="e8c3b-184">[Set Up Data Exchange Definitions](across-how-to-set-up-data-exchange-definitions.md) </span></span>  
<span data-ttu-id="e8c3b-185">[Exportar pagos a un archivo bancario](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md#exporting-payments-to-a-bank-file) </span><span class="sxs-lookup"><span data-stu-id="e8c3b-185">[Export Payments to a Bank File](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md#exporting-payments-to-a-bank-file) </span></span>  
<span data-ttu-id="e8c3b-186">[Cobrar pagos mediante adeudo directo SEPA](finance-collect-payments-with-sepa-direct-debit.md) </span><span class="sxs-lookup"><span data-stu-id="e8c3b-186">[Collect Payments with SEPA Direct Debit](finance-collect-payments-with-sepa-direct-debit.md) </span></span>  
[<span data-ttu-id="e8c3b-187">Acerca del marco de intercambio de datos</span><span class="sxs-lookup"><span data-stu-id="e8c3b-187">About the Data Exchange Framework</span></span>](across-about-the-data-exchange-framework.md)
