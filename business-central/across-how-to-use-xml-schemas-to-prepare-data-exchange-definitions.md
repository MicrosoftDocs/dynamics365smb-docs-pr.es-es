---
title: Uso de esquemas XML para preparar definiciones de intercambio de datos
description: Utilice los esquemas XML para configurar el marco de intercambio de documentos.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 25073b552644c9ca013a2eae90a0d013ab57e556
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5379428"
---
# <a name="use-xml-schemas-to-prepare-data-exchange-definitions"></a><span data-ttu-id="16ef6-103">Uso de esquemas XML para preparar definiciones de intercambio de datos</span><span class="sxs-lookup"><span data-stu-id="16ef6-103">Use XML Schemas to Prepare Data Exchange Definitions</span></span>

<span data-ttu-id="16ef6-104">Para habilitar la importación y exportación de datos en archivos XML mediante el marco de intercambio de datos en [!INCLUDE[prod_short](includes/prod_short.md)], puede usar esquemas XML de los archivos para definir los elementos de datos que desea intercambiar con [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="16ef6-104">To enable import/export of data in XML files through the data exchange framework in [!INCLUDE[prod_short](includes/prod_short.md)], you can use XML schemas to define which data elements you want to exchange with [!INCLUDE[prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="16ef6-105">Este trabajo se realiza en la página **Visor de esquema XML** mediante la carga del archivo de esquema XML, la selección de los elementos de datos pertinentes y la inicialización de una definición de intercambio de datos.</span><span class="sxs-lookup"><span data-stu-id="16ef6-105">You perform this work on the **XML Schema Viewer** page by loading the XML schema file, selecting the relevant data elements, and then initializing a data exchange definition.</span></span>  

 <span data-ttu-id="16ef6-106">Cuando ha definido qué elementos de datos se van a incluir en función del esquema XML, puede utilizar la acción **Generar definición de intercambio de datos** para inicializar una definición de intercambio de datos en los datos seleccionados, que después podrá completar en el marco de intercambio de datos.</span><span class="sxs-lookup"><span data-stu-id="16ef6-106">When you have defined which data elements to include based on the XML schema, you can use the **Generate Data Exchange Definition** action to initialize a data exchange definition based on the selected data elements, which you then complete in the Data Exchange Framework.</span></span> <span data-ttu-id="16ef6-107">Esto crea un registro en la página **Definiciones de intercambio de registro**, donde se continúa con la definición de qué elementos del archivo se asignan a qué campos de [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="16ef6-107">This creates a record on the **Posting Exchange Definition** page where you continue by defining which elements in the file map to which fields in [!INCLUDE[prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="16ef6-108">Para obtener más información, vea [Configurar las definiciones de intercambio de datos](across-how-to-set-up-data-exchange-definitions.md).</span><span class="sxs-lookup"><span data-stu-id="16ef6-108">For more information, see [Set Up Data Exchange Definitions](across-how-to-set-up-data-exchange-definitions.md).</span></span>  

 <span data-ttu-id="16ef6-109">Este tema incluye los siguientes procedimientos:</span><span class="sxs-lookup"><span data-stu-id="16ef6-109">This topic contains the following procedures:</span></span>  

- <span data-ttu-id="16ef6-110">Para cargar un archivo de esquema XML</span><span class="sxs-lookup"><span data-stu-id="16ef6-110">To load an XML schema file</span></span>  

- <span data-ttu-id="16ef6-111">Para seleccionar o borrar nodos en un esquema XML</span><span class="sxs-lookup"><span data-stu-id="16ef6-111">To select or clear nodes in an XML schema</span></span>  

- <span data-ttu-id="16ef6-112">Para generar una definición de intercambio de datos basada en un esquema XML</span><span class="sxs-lookup"><span data-stu-id="16ef6-112">To generate a data exchange definition that is based on an XML schema</span></span>  

## <a name="to-load-an-xml-schema-file"></a><span data-ttu-id="16ef6-113">Para cargar un archivo de esquema XML</span><span class="sxs-lookup"><span data-stu-id="16ef6-113">To load an XML schema file</span></span>

1. <span data-ttu-id="16ef6-114">Asegúrese de que esté disponible el archivo de esquema XML.</span><span class="sxs-lookup"><span data-stu-id="16ef6-114">Make sure that the relevant XML schema file is available.</span></span> <span data-ttu-id="16ef6-115">La extensión de archivo es .xsd.</span><span class="sxs-lookup"><span data-stu-id="16ef6-115">The file extension is .xsd.</span></span>  

2. <span data-ttu-id="16ef6-116">Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Esquemas XML** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="16ef6-116">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **XML Schemas**, and then choose the related link.</span></span>  

3. <span data-ttu-id="16ef6-117">Seleccione la acción **Nuevo**.</span><span class="sxs-lookup"><span data-stu-id="16ef6-117">Choose the **New** action.</span></span>  

4. <span data-ttu-id="16ef6-118">Rellene los campos tal como se describe en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="16ef6-118">Fill the fields as described in the following table.</span></span>  

    |<span data-ttu-id="16ef6-119">Campo</span><span class="sxs-lookup"><span data-stu-id="16ef6-119">Field</span></span>|<span data-ttu-id="16ef6-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="16ef6-120">Description</span></span>|  
    |---------------------------------|---------------------------------------|  
    |<span data-ttu-id="16ef6-121">**Código**</span><span class="sxs-lookup"><span data-stu-id="16ef6-121">**Code**</span></span>|<span data-ttu-id="16ef6-122">Especifique un código para identificar el esquema XML.</span><span class="sxs-lookup"><span data-stu-id="16ef6-122">Specify a code to identify the XML schema.</span></span>|  
    |<span data-ttu-id="16ef6-123">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="16ef6-123">**Description**</span></span>|<span data-ttu-id="16ef6-124">Especifique una descripción del esquema XML.</span><span class="sxs-lookup"><span data-stu-id="16ef6-124">Specify a description of the XML schema.</span></span>|  

     <span data-ttu-id="16ef6-125">El campo **Espacio de nombres de destino** especifica cualquier espacio de nombres del archivo de esquema XML que se ha cargado para la línea.</span><span class="sxs-lookup"><span data-stu-id="16ef6-125">The **Target Namespace** field specifies any namespace in the XML schema file that has been loaded for the line.</span></span>  

5. <span data-ttu-id="16ef6-126">Elija la acción **Cargar esquema** y luego seleccione el archivo de esquema XML.</span><span class="sxs-lookup"><span data-stu-id="16ef6-126">Choose the **Load Schema** action, and then select the XML schema file.</span></span>  

     <span data-ttu-id="16ef6-127">Cuando se carga el archivo, los demás campos de la línea se rellenan con la información del archivo y se selecciona la casilla **Esquema cargado**.</span><span class="sxs-lookup"><span data-stu-id="16ef6-127">When the file is loaded, the rest of the fields on the line are filled with information from the file, and the **Schema is Loaded** check box is selected.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="16ef6-128">El árbol del esquema XML cargado está contraído de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="16ef6-128">The tree of the loaded XML schema is collapsed by default.</span></span> <span data-ttu-id="16ef6-129">Puede ampliar cada nodo eligiendo el botón **+** en el nodo.</span><span class="sxs-lookup"><span data-stu-id="16ef6-129">You expand each node by choosing the **+** button on the node.</span></span> <span data-ttu-id="16ef6-130">Para expandir todos los nodos, seleccione **Expandir todo** en la cinta.</span><span class="sxs-lookup"><span data-stu-id="16ef6-130">To expand all nodes, choose **Expand All** on the ribbon.</span></span>  

### <a name="to-select-or-clear-nodes-in-an-xml-schema"></a><span data-ttu-id="16ef6-131">Para seleccionar o borrar nodos en un esquema XML</span><span class="sxs-lookup"><span data-stu-id="16ef6-131">To select or clear nodes in an XML schema</span></span>  

1. <span data-ttu-id="16ef6-132">Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Visor de esquemas XML** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="16ef6-132">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **XML Schema Viewer**, and then choose the related link.</span></span>  

2. <span data-ttu-id="16ef6-133">Rellene los campos en la cabecera tal como se describe en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="16ef6-133">Fill the fields on the header as described in the following table.</span></span>  

    |<span data-ttu-id="16ef6-134">Campo</span><span class="sxs-lookup"><span data-stu-id="16ef6-134">Field</span></span>|<span data-ttu-id="16ef6-135">Descripción</span><span class="sxs-lookup"><span data-stu-id="16ef6-135">Description</span></span>|  
    |---------------------------------|---------------------------------------|  
    |<span data-ttu-id="16ef6-136">**Código de esquema XML**</span><span class="sxs-lookup"><span data-stu-id="16ef6-136">**XML Schema Code**</span></span>|<span data-ttu-id="16ef6-137">Especifique el archivo de esquema XML que se ha cargado en el paso 5 en la sección “Para cargar un archivo de esquema XML”.</span><span class="sxs-lookup"><span data-stu-id="16ef6-137">Specify the XML schema file that you loaded in step 5 in the "To load an XML schema file" section.</span></span>|  
    |<span data-ttu-id="16ef6-138">**Nuevo nº de XMLport**</span><span class="sxs-lookup"><span data-stu-id="16ef6-138">**New XMLport No.**</span></span>|<span data-ttu-id="16ef6-139">Especifique el número del objeto XMLport que se crea a partir de este esquema de XML cuando elige la acción **Generar XMLport**.</span><span class="sxs-lookup"><span data-stu-id="16ef6-139">Specify the number of the XMLport that is created from this XML schema when you choose the **Generate XMLport** action.</span></span>|  

     <span data-ttu-id="16ef6-140">Las líneas ahora se rellenan con nodos que representan todos los elementos del esquema XML.</span><span class="sxs-lookup"><span data-stu-id="16ef6-140">The lines are now filled with nodes representing all elements in the XML schema.</span></span> <span data-ttu-id="16ef6-141">Los nodos de los elementos que son obligatorios según el esquema XML están seleccionados de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="16ef6-141">Nodes for elements that are mandatory according to the XML schema are selected by default.</span></span>  

3. <span data-ttu-id="16ef6-142">En la primera línea, en la columna **Nombre de nodo**, expanda el nodo **Documento** y, a continuación expanda gradualmente los nodos subyacentes que desea revisar.</span><span class="sxs-lookup"><span data-stu-id="16ef6-142">On the first line, in the **Node Name** column, expand the **Document** node, and then gradually expand underlying nodes that you want to review.</span></span>  

     <span data-ttu-id="16ef6-143">También puede hacer clic con el botón secundario en un nodo y elegir **Expandir todo**.</span><span class="sxs-lookup"><span data-stu-id="16ef6-143">Alternatively, right-click on a node and then choose **Expand All**.</span></span>  

4. <span data-ttu-id="16ef6-144">Elija cualquiera de las acciones siguientes para cambiar los nodos que se muestran.</span><span class="sxs-lookup"><span data-stu-id="16ef6-144">Choose either of the following actions to change which nodes are displayed.</span></span>  

    |<span data-ttu-id="16ef6-145">**Acción**</span><span class="sxs-lookup"><span data-stu-id="16ef6-145">**Action**</span></span>|<span data-ttu-id="16ef6-146">Descripción</span><span class="sxs-lookup"><span data-stu-id="16ef6-146">Description</span></span>|  
    |----------------|---------------------------------------|  
    |<span data-ttu-id="16ef6-147">**Mostrar todos**</span><span class="sxs-lookup"><span data-stu-id="16ef6-147">**Show All**</span></span>|<span data-ttu-id="16ef6-148">Se muestran todos los nodos.</span><span class="sxs-lookup"><span data-stu-id="16ef6-148">All nodes are shown.</span></span>|  
    |<span data-ttu-id="16ef6-149">**Ocultar elementos opcionales**</span><span class="sxs-lookup"><span data-stu-id="16ef6-149">**Hide Non-Mandatory**</span></span>|<span data-ttu-id="16ef6-150">Solo se muestran los nodos que representan elementos que son obligatorios según el esquema XML.</span><span class="sxs-lookup"><span data-stu-id="16ef6-150">Only nodes representing elements that are required according to the XML schema are shown.</span></span> <span data-ttu-id="16ef6-151">Estos nodos normalmente se indican mediante un **1** en el campo **MinOccurs**.</span><span class="sxs-lookup"><span data-stu-id="16ef6-151">These nodes are typically indicated by a **1** in the **MinOccurs** field.</span></span><br /><br /> <span data-ttu-id="16ef6-152">Elija **Mostrar todos** para revertir la vista.</span><span class="sxs-lookup"><span data-stu-id="16ef6-152">Choose **Show All** to reverse the view.</span></span>|  
    |<span data-ttu-id="16ef6-153">**Ocultar elementos no seleccionados**</span><span class="sxs-lookup"><span data-stu-id="16ef6-153">**Hide Non-Selected**</span></span>|<span data-ttu-id="16ef6-154">Solo se muestran los nodos donde está seleccionada la casilla **Seleccionado**.</span><span class="sxs-lookup"><span data-stu-id="16ef6-154">Only nodes where the **Selected** check box is selected are shown.</span></span><br /><br /> <span data-ttu-id="16ef6-155">Elija **Mostrar todos** para revertir la vista.</span><span class="sxs-lookup"><span data-stu-id="16ef6-155">Choose **Show All** to reverse the view.</span></span>|  

5. <span data-ttu-id="16ef6-156">Seleccione la acción **Editar**.</span><span class="sxs-lookup"><span data-stu-id="16ef6-156">Choose the **Edit** action.</span></span>  

6. <span data-ttu-id="16ef6-157">En la casilla **Seleccionado**, especifique para cada nodo si desea que el elemento se admita en la definición de intercambio de datos para el archivo bancario SEPA relacionado.</span><span class="sxs-lookup"><span data-stu-id="16ef6-157">In the **Selected** check box, specify for each node if you want the element to be supported in the data exchange definition for the related SEPA bank file.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="16ef6-158">Al seleccionar un nodo secundario obligatorio, también se seleccionan todos los nodos principales por encima de él.</span><span class="sxs-lookup"><span data-stu-id="16ef6-158">When you select a mandatory child node, all parent nodes above it are also selected.</span></span>  

7. <span data-ttu-id="16ef6-159">Elija la acción **Seleccionar todos los elementos obligatorios** para reelegir todos los nodos que representen elementos obligatorios según el esquema XML.</span><span class="sxs-lookup"><span data-stu-id="16ef6-159">Choose the **Select All Mandatory Elements** action to reselect all nodes that represent elements that are mandatory according to the XML schema.</span></span>  

8. <span data-ttu-id="16ef6-160">Elija la acción **Anular selección** para borrar todas las selecciones.</span><span class="sxs-lookup"><span data-stu-id="16ef6-160">Choose the **Deselect All** action to clear all selections.</span></span>  

     <span data-ttu-id="16ef6-161">El campo **Opción** especifica que el nodo tiene dos o más nodos de hermano que funcionan como opciones.</span><span class="sxs-lookup"><span data-stu-id="16ef6-161">The **Choice** field specifies that the node has two or more sibling nodes that function as options.</span></span>  

### <a name="to-generate-a-data-exchange-definition-that-is-based-on-an-xml-schema"></a><span data-ttu-id="16ef6-162">Para generar una definición de intercambio de datos basada en un esquema XML</span><span class="sxs-lookup"><span data-stu-id="16ef6-162">To generate a data exchange definition that is based on an XML schema</span></span>  

1. <span data-ttu-id="16ef6-163">Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Esquemas XML** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="16ef6-163">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter  **XML Schemas**, and then choose the related link.</span></span>  

2. <span data-ttu-id="16ef6-164">Seleccione el esquema XML relevante y luego elija la acción **Abrir Visor de esquema XML**.</span><span class="sxs-lookup"><span data-stu-id="16ef6-164">Select the relevant XML schema, and then choose the **Open XML Schema Viewer** action.</span></span>  

3. <span data-ttu-id="16ef6-165">Asegúrese de que estén seleccionados los nodos correspondientes.</span><span class="sxs-lookup"><span data-stu-id="16ef6-165">Make sure the relevant nodes are selected.</span></span> <span data-ttu-id="16ef6-166">Para obtener más información, consulte la sección "Para seleccionar o borrar nodos en un esquema XML".</span><span class="sxs-lookup"><span data-stu-id="16ef6-166">For more information, see the "To select or clear nodes in an XML schema" section.</span></span>  

4. <span data-ttu-id="16ef6-167">En la página **Visor de esquemas XML**, elija la acción **Generar definición de intercambio de datos**.</span><span class="sxs-lookup"><span data-stu-id="16ef6-167">On the **XML Schema Viewer** page, choose the **Generate Data Exchange Definition** action.</span></span>  

 <span data-ttu-id="16ef6-168">Se crea una definición de intercambio de datos en la página **Definiciones de intercambio de registro**, que se puede completar especificando qué elementos del archivo de banco SEPA se corresponden con los campos de [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="16ef6-168">A data exchange definition is created on the **Posting Exchange Definition** page, which you can complete by specifying which elements in the file map to which fields in [!INCLUDE[prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="16ef6-169">Para obtener más información, vea [Configurar las definiciones de intercambio de datos](across-how-to-set-up-data-exchange-definitions.md).</span><span class="sxs-lookup"><span data-stu-id="16ef6-169">For more information, see [Set Up Data Exchange Definitions](across-how-to-set-up-data-exchange-definitions.md).</span></span>  

> [!NOTE]  
> <span data-ttu-id="16ef6-170">También puede utilizar la función **Obtener estructura de archivo** desde la página **Definiciones de intercambio de registro**, la cual utiliza la funcionalidad de la página **Visor esquemas XML** para prellenar la ficha desplegable **Definiciones de columna**.</span><span class="sxs-lookup"><span data-stu-id="16ef6-170">You can also use the **Get File Structure** function from the **Posting Exchange Definition** page, which uses the functionality of the **XML Schema Viewer** page to prefill the **Column Definitions** TastTab.</span></span>  

> [!NOTE]
> <span data-ttu-id="16ef6-171">En la fase de lanzamiento 1 de 2019 y versiones anteriores, podía generar un XMLport basado en el esquema y luego importarlo en su solución.</span><span class="sxs-lookup"><span data-stu-id="16ef6-171">In 2019 release wave 1 and earlier versions, you could generate an XMLport that was based on the schema and then import that into your solution.</span></span> <span data-ttu-id="16ef6-172">Esto ya no es compatible.</span><span class="sxs-lookup"><span data-stu-id="16ef6-172">This is no longer supported.</span></span>

## <a name="see-also"></a><span data-ttu-id="16ef6-173">Consulte también</span><span class="sxs-lookup"><span data-stu-id="16ef6-173">See Also</span></span>

[<span data-ttu-id="16ef6-174">Configurar definiciones de intercambio de datos</span><span class="sxs-lookup"><span data-stu-id="16ef6-174">Set Up Data Exchange Definitions</span></span>](across-how-to-set-up-data-exchange-definitions.md)  
[<span data-ttu-id="16ef6-175">Exportar pagos a un archivo bancario</span><span class="sxs-lookup"><span data-stu-id="16ef6-175">Export Payments to a Bank File</span></span>](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md#exporting-payments-to-a-bank-file)  
[<span data-ttu-id="16ef6-176">Cobrar pagos mediante adeudo directo SEPA</span><span class="sxs-lookup"><span data-stu-id="16ef6-176">Collect Payments with SEPA Direct Debit</span></span>](finance-collect-payments-with-sepa-direct-debit.md)  
[<span data-ttu-id="16ef6-177">Acerca del marco de intercambio de datos</span><span class="sxs-lookup"><span data-stu-id="16ef6-177">About the Data Exchange Framework</span></span>](across-about-the-data-exchange-framework.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]