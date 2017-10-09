---
title: Crear objetos XMLports basados en esquemas XML | Documentos de Microsoft
description: Utilice los esquemas XML para configurar el marco de intercambio de documentos.
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/21/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: c4b53c6a87148990102ba9eca235cf139a48396e
ms.contentlocale: es-es
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-use-xml-schemas-to-prepare-data-exchange-definitions"></a><span data-ttu-id="f7433-103">Procedimiento: Uso de esquemas XML para preparar definiciones de intercambio de datos</span><span class="sxs-lookup"><span data-stu-id="f7433-103">How to: Use XML Schemas to Prepare Data Exchange Definitions</span></span>
<span data-ttu-id="f7433-104">Para habilitar la importación y exportación de datos en archivos XML mediante el marco de intercambio de datos en [!INCLUDE[d365fin](includes/d365fin_md.md)], puede usar esquemas XML de los archivos para definir los elementos de datos que desea intercambiar con [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="f7433-104">To enable import/export of data in XML files through the data exchange framework in [!INCLUDE[d365fin](includes/d365fin_md.md)], you can use XML schemas to define which data elements you want to exchange with [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="f7433-105">Este trabajo se realiza en la ventana **Visor de esquema XML** mediante la carga del archivo de esquema XML, la selección de los elementos de datos pertinentes y la inicialización de una definición de intercambio de datos o un objeto XMLport.</span><span class="sxs-lookup"><span data-stu-id="f7433-105">You perform this work in the **XML Schema Viewer** window by loading the XML schema file, selecting the relevant data elements, and then initializing either a data exchange definition or an XMLport.</span></span>  

 <span data-ttu-id="f7433-106">Cuando haya definido qué elementos de datos se incluirán según el esquema XML, puede usar la acción **Generar XMLport** a fin de crear el objeto XMLport.</span><span class="sxs-lookup"><span data-stu-id="f7433-106">When you have defined which data elements to include based on the XML schema, you can use the **Generate XMLport** action to create the XMLport object.</span></span>  

 <span data-ttu-id="f7433-107">También puede utilizar la acción **Generar definición de intercambio de datos** para inicializar una definición de intercambio de datos en los datos seleccionados, que después podrá completar en el marco de intercambio de datos.</span><span class="sxs-lookup"><span data-stu-id="f7433-107">Alternatively, you can use the **Generate Data Exchange Definition** action to initialize a data exchange definition based on the selected data elements, which you then complete in the Data Exchange Framework.</span></span> <span data-ttu-id="f7433-108">Esto crea un registro en la ventana **Definiciones de intercambio de registro**, donde se continúa con la definición de qué elementos del archivo se asignan a qué campos de [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="f7433-108">This creates a record in the **Posting Exchange Definition** window where you continue by defining which elements in the file map to which fields in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="f7433-109">Para obtener más información, vea [Procedimiento: Configurar las definiciones de intercambio de datos](across-how-to-set-up-data-exchange-definitions.md).</span><span class="sxs-lookup"><span data-stu-id="f7433-109">For more information, see [How to: Set Up Data Exchange Definitions](across-how-to-set-up-data-exchange-definitions.md).</span></span>  

 <span data-ttu-id="f7433-110">Este tema incluye los siguientes procedimientos:</span><span class="sxs-lookup"><span data-stu-id="f7433-110">This topic contains the following procedures:</span></span>  

-   <span data-ttu-id="f7433-111">Para cargar un archivo de esquema XML</span><span class="sxs-lookup"><span data-stu-id="f7433-111">To load an XML schema file</span></span>  

-   <span data-ttu-id="f7433-112">Para seleccionar o borrar nodos en un esquema XML</span><span class="sxs-lookup"><span data-stu-id="f7433-112">To select or clear nodes in an XML schema</span></span>  

-   <span data-ttu-id="f7433-113">Para generar una definición de intercambio de datos basada en un esquema XML</span><span class="sxs-lookup"><span data-stu-id="f7433-113">To generate a data exchange definition that is based on an XML schema</span></span>  

-   <span data-ttu-id="f7433-114">Para generar un objeto XMLport para el archivo basado en un esquema XML</span><span class="sxs-lookup"><span data-stu-id="f7433-114">To generate an XMLport for the file that is based on an XML schema</span></span>  

-   <span data-ttu-id="f7433-115">Para importar un objeto XMLport en Object Designer</span><span class="sxs-lookup"><span data-stu-id="f7433-115">To import an XMLport into the Object Designer</span></span>  

### <a name="to-load-an-xml-schema-file"></a><span data-ttu-id="f7433-116">Para cargar un archivo de esquema XML</span><span class="sxs-lookup"><span data-stu-id="f7433-116">To load an XML schema file</span></span>  

1.  <span data-ttu-id="f7433-117">Asegúrese de que esté disponible el archivo de esquema XML.</span><span class="sxs-lookup"><span data-stu-id="f7433-117">Make sure that the relevant XML schema file is available.</span></span> <span data-ttu-id="f7433-118">La extensión de archivo es .xsd.</span><span class="sxs-lookup"><span data-stu-id="f7433-118">The file extension is .xsd.</span></span>  

2.  <span data-ttu-id="f7433-119">En el cuadro **Buscar**, escriba **Esquemas XML** y, a continuación, elija el vínculo relacionado.</span><span class="sxs-lookup"><span data-stu-id="f7433-119">In the **Search** box, enter **XML Schemas**, and then choose the related link.</span></span>  

3.  <span data-ttu-id="f7433-120">En la pestaña **Inicio**, en el grupo **Nuevo**, seleccione **Nuevo**.</span><span class="sxs-lookup"><span data-stu-id="f7433-120">On the **Home** tab, in the **New** group, choose **New**.</span></span>  

4.  <span data-ttu-id="f7433-121">Rellene los campos tal como se describe en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="f7433-121">Fill the fields as described in the following table.</span></span>  

    |<span data-ttu-id="f7433-122">Campo</span><span class="sxs-lookup"><span data-stu-id="f7433-122">Field</span></span>|<span data-ttu-id="f7433-123">[Description]</span><span class="sxs-lookup"><span data-stu-id="f7433-123">[Description]</span></span>|  
    |---------------------------------|---------------------------------------|  
    |<span data-ttu-id="f7433-124">**Código**</span><span class="sxs-lookup"><span data-stu-id="f7433-124">**Code**</span></span>|<span data-ttu-id="f7433-125">Especifique un código para identificar el esquema XML.</span><span class="sxs-lookup"><span data-stu-id="f7433-125">Specify a code to identify the XML schema.</span></span>|  
    |<span data-ttu-id="f7433-126">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="f7433-126">**Description**</span></span>|<span data-ttu-id="f7433-127">Especifique una descripción del esquema XML.</span><span class="sxs-lookup"><span data-stu-id="f7433-127">Specify a description of the XML schema.</span></span>|  

     <span data-ttu-id="f7433-128">El campo **Espacio de nombres de destino** especifica cualquier espacio de nombres del archivo de esquema XML que se ha cargado para la línea.</span><span class="sxs-lookup"><span data-stu-id="f7433-128">The **Target Namespace** field specifies any namespace in the XML schema file that has been loaded for the line.</span></span>  

5.  <span data-ttu-id="f7433-129">En la pestaña **Inicio**, en el grupo **Proceso**, seleccione **Cargar esquema** y seleccione luego el archivo de esquema XML.</span><span class="sxs-lookup"><span data-stu-id="f7433-129">On the **Home** tab, in the **Process** group, choose **Load Schema**, and then select the XML schema file.</span></span>  

     <span data-ttu-id="f7433-130">Cuando se carga el archivo, los demás campos de la línea se rellenan con la información del archivo y se selecciona la casilla **Esquema cargado**.</span><span class="sxs-lookup"><span data-stu-id="f7433-130">When the file is loaded, the rest of the fields on the line are filled with information from the file, and the **Schema is Loaded** check box is selected.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="f7433-131">El árbol del esquema XML cargado está contraído de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="f7433-131">The tree of the loaded XML schema is collapsed by default.</span></span> <span data-ttu-id="f7433-132">Puede ampliar cada nodo eligiendo el botón **+** en el nodo.</span><span class="sxs-lookup"><span data-stu-id="f7433-132">You expand each node by choosing the **+** button on the node.</span></span> <span data-ttu-id="f7433-133">Para expandir todos los nodos, seleccione **Expandir todo** en la cinta.</span><span class="sxs-lookup"><span data-stu-id="f7433-133">To expand all nodes, choose **Expand All** on the ribbon.</span></span>  

### <a name="to-select-or-clear-nodes-in-an-xml-schema"></a><span data-ttu-id="f7433-134">Para seleccionar o borrar nodos en un esquema XML</span><span class="sxs-lookup"><span data-stu-id="f7433-134">To select or clear nodes in an XML schema</span></span>  

1.  <span data-ttu-id="f7433-135">En el cuadro **Buscar**, escriba **Visor esquemas XML** y, a continuación, elija el vínculo relacionado.</span><span class="sxs-lookup"><span data-stu-id="f7433-135">In the **Search** box, enter **XML Schema Viewer**, and then choose the related link.</span></span>  

2.  <span data-ttu-id="f7433-136">Rellene los campos en la cabecera tal como se describe en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="f7433-136">Fill the fields on the header as described in the following table.</span></span>  

    |<span data-ttu-id="f7433-137">Campo</span><span class="sxs-lookup"><span data-stu-id="f7433-137">Field</span></span>|<span data-ttu-id="f7433-138">Description</span><span class="sxs-lookup"><span data-stu-id="f7433-138">Description</span></span>|  
    |---------------------------------|---------------------------------------|  
    |<span data-ttu-id="f7433-139">**Código de esquema XML**</span><span class="sxs-lookup"><span data-stu-id="f7433-139">**XML Schema Code**</span></span>|<span data-ttu-id="f7433-140">Especifique el archivo de esquema XML que se ha cargado en el paso 5 en la sección “Para cargar un archivo de esquema XML”.</span><span class="sxs-lookup"><span data-stu-id="f7433-140">Specify the XML schema file that you loaded in step 5 in the “To load an XML schema file” section.</span></span>|  
    |<span data-ttu-id="f7433-141">**N.º XMLport nuevo**</span><span class="sxs-lookup"><span data-stu-id="f7433-141">**New XMLport No.**</span></span>|<span data-ttu-id="f7433-142">Especifique el número del objeto XMLport que se crea a partir de este esquema de XML cuando elige la acción **Generar XMLport**.</span><span class="sxs-lookup"><span data-stu-id="f7433-142">Specify the number of the XMLport that is created from this XML schema when you choose the **Generate XMLport** action.</span></span>|  

     <span data-ttu-id="f7433-143">Las líneas ahora se rellenan con nodos que representan todos los elementos del esquema XML.</span><span class="sxs-lookup"><span data-stu-id="f7433-143">The lines are now filled with nodes representing all elements in the XML schema.</span></span> <span data-ttu-id="f7433-144">Los nodos de los elementos que son obligatorios según el esquema XML están seleccionados de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="f7433-144">Nodes for elements that are mandatory according to the XML schema are selected by default.</span></span>  

3.  <span data-ttu-id="f7433-145">En la primera línea, en la columna **Nombre de nodo**, expanda el nodo **Documento** y, a continuación expanda gradualmente los nodos subyacentes que desea revisar.</span><span class="sxs-lookup"><span data-stu-id="f7433-145">On the first line, in the **Node Name** column, expand the **Document** node, and then gradually expand underlying nodes that you want to review.</span></span>  

     <span data-ttu-id="f7433-146">También puede hacer clic con el botón secundario en un nodo y elegir **Expandir todo**.</span><span class="sxs-lookup"><span data-stu-id="f7433-146">Alternatively, right-click on a node and then choose **Expand All**.</span></span>  

4.  <span data-ttu-id="f7433-147">En la pestaña **Inicio**, en el grupo **Ver**, seleccione cualquiera de las acciones siguientes para cambiar los nodos que se muestran.</span><span class="sxs-lookup"><span data-stu-id="f7433-147">On the **Home** tab, in the **View** group, choose either of the following actions to change which nodes are displayed.</span></span>  

    |<span data-ttu-id="f7433-148">**Acción**</span><span class="sxs-lookup"><span data-stu-id="f7433-148">**Action**</span></span>|<span data-ttu-id="f7433-149">Description</span><span class="sxs-lookup"><span data-stu-id="f7433-149">Description</span></span>|  
    |----------------|---------------------------------------|  
    |<span data-ttu-id="f7433-150">**Mostrar todos**</span><span class="sxs-lookup"><span data-stu-id="f7433-150">**Show All**</span></span>|<span data-ttu-id="f7433-151">Se muestran todos los nodos.</span><span class="sxs-lookup"><span data-stu-id="f7433-151">All nodes are shown.</span></span>|  
    |<span data-ttu-id="f7433-152">**Ocultar elementos opcionales**</span><span class="sxs-lookup"><span data-stu-id="f7433-152">**Hide Non-Mandatory**</span></span>|<span data-ttu-id="f7433-153">Solo se muestran los nodos que representan elementos que son obligatorios según el esquema XML.</span><span class="sxs-lookup"><span data-stu-id="f7433-153">Only nodes representing elements that are required according to the XML schema are shown.</span></span> <span data-ttu-id="f7433-154">Estos nodos normalmente se indican mediante un **1** en el campo **MinOccurs**.</span><span class="sxs-lookup"><span data-stu-id="f7433-154">These nodes are typically indicated by a **1** in the **MinOccurs** field.</span></span><br /><br /> <span data-ttu-id="f7433-155">Elija **Mostrar todos** para revertir la vista.</span><span class="sxs-lookup"><span data-stu-id="f7433-155">Choose **Show All** to reverse the view.</span></span>|  
    |<span data-ttu-id="f7433-156">**Ocultar elementos no seleccionados**</span><span class="sxs-lookup"><span data-stu-id="f7433-156">**Hide Non-Selected**</span></span>|<span data-ttu-id="f7433-157">Solo se muestran los nodos donde está seleccionada la casilla **Seleccionado**.</span><span class="sxs-lookup"><span data-stu-id="f7433-157">Only nodes where the **Selected** check box is selected are shown.</span></span><br /><br /> <span data-ttu-id="f7433-158">Elija **Mostrar todos** para revertir la vista.</span><span class="sxs-lookup"><span data-stu-id="f7433-158">Choose **Show All** to reverse the view.</span></span>|  

5.  <span data-ttu-id="f7433-159">En la pestaña **Inicio**, en el grupo **Administrar**, elija **Editar**.</span><span class="sxs-lookup"><span data-stu-id="f7433-159">On the **Home** tab, in the **Manage** group, choose **Edit**.</span></span>  

6.  <span data-ttu-id="f7433-160">En la casilla **Seleccionado**, especifique para cada nodo si desea que el elemento se admita en la definición de intercambio de datos para el archivo bancario SEPA relacionado.</span><span class="sxs-lookup"><span data-stu-id="f7433-160">In the **Selected** check box, specify for each node if you want the element to be supported in the data exchange definition for the related SEPA bank file.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="f7433-161">Al seleccionar un nodo secundario obligatorio, también se seleccionan todos los nodos principales por encima de él.</span><span class="sxs-lookup"><span data-stu-id="f7433-161">When you select a mandatory child node, all parent nodes above it are also selected.</span></span>  

7.  <span data-ttu-id="f7433-162">Elija la acción **Seleccionar todos los elementos obligatorios** para reelegir todos los nodos que representen elementos obligatorios según el esquema XML.</span><span class="sxs-lookup"><span data-stu-id="f7433-162">Choose the **Select All Mandatory Elements** action to reselect all nodes that represent elements that are mandatory according to the XML schema.</span></span>  

8.  <span data-ttu-id="f7433-163">Elija la acción **Anular selección** para borrar todas las selecciones.</span><span class="sxs-lookup"><span data-stu-id="f7433-163">Choose the **Deselect All** action to clear all selections.</span></span>  

     <span data-ttu-id="f7433-164">El campo **Opción** especifica que el nodo tiene dos o más nodos de hermano que funcionan como opciones.</span><span class="sxs-lookup"><span data-stu-id="f7433-164">The **Choice** field specifies that the node has two or more sibling nodes that function as options.</span></span>  

### <a name="to-generate-a-data-exchange-definition-that-is-based-on-an-xml-schema"></a><span data-ttu-id="f7433-165">Para generar una definición de intercambio de datos basada en un esquema XML</span><span class="sxs-lookup"><span data-stu-id="f7433-165">To generate a data exchange definition that is based on an XML schema</span></span>  

1.  <span data-ttu-id="f7433-166">En el cuadro **Buscar**, escriba **Esquemas XML** y, a continuación, elija el vínculo relacionado.</span><span class="sxs-lookup"><span data-stu-id="f7433-166">In the **Search** box, enter  **XML Schemas**, and then choose the related link.</span></span>  

2.  <span data-ttu-id="f7433-167">Seleccione el esquema XML y, a continuación, en la pestaña **Inicio**, en el grupo **Procesar**, elija **Abrir Visor de esquema XML**.</span><span class="sxs-lookup"><span data-stu-id="f7433-167">Select the relevant XML schema, and then on the on the **Home** tab, in the **Process** group, choose **Open XML Schema Viewer**.</span></span>  

3.  <span data-ttu-id="f7433-168">Asegúrese de que estén seleccionados los nodos correspondientes.</span><span class="sxs-lookup"><span data-stu-id="f7433-168">Make sure the relevant nodes are selected.</span></span> <span data-ttu-id="f7433-169">Para obtener más información, consulte la sección "Para seleccionar o borrar nodos en un esquema XML".</span><span class="sxs-lookup"><span data-stu-id="f7433-169">For more information, see the “To select or clear nodes in an XML schema” section.</span></span>  

4.  <span data-ttu-id="f7433-170">En la ventana **Visor de esquema XML**, en la pestaña **Inicio**, en el grupo **Procesar**, seleccione **Generar definición de intercambio de datos**.</span><span class="sxs-lookup"><span data-stu-id="f7433-170">In the **XML Schema Viewer** window, on the **Home** tab, in the **Process** group, choose **Generate Data Exchange Definition**.</span></span>  

 <span data-ttu-id="f7433-171">Se crea una definición de intercambio de datos en la ventana **Definiciones de intercambio de registro**, que se puede completar especificando qué elementos del archivo de banco SEPA se corresponden con los campos de [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="f7433-171">A data exchange definition is created in the **Posting Exchange Definition** window, which you can complete by specifying which elements in the file map to which fields in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="f7433-172">Para obtener más información, vea [Procedimiento: Configurar las definiciones de intercambio de datos](across-how-to-set-up-data-exchange-definitions.md).</span><span class="sxs-lookup"><span data-stu-id="f7433-172">For more information, see [How to: Set Up Data Exchange Definitions](across-how-to-set-up-data-exchange-definitions.md).</span></span>  

> [!NOTE]  
>  <span data-ttu-id="f7433-173">También puede utilizar la función **Obtener estructura de archivo** desde la ventana **Definiciones de intercambio de registro**, la cual utiliza la funcionalidad de la ventana **Visor esquemas XML** para prellenar la ficha desplegable **Definiciones de columna**.</span><span class="sxs-lookup"><span data-stu-id="f7433-173">You can also use the **Get File Structure** function from the **Posting Exchange Definition** window, which uses the functionality of the **XML Schema Viewer** window to prefill the **Column Definitions** TastTab.</span></span>  

### <a name="to-generate-an-xmlport-that-is-based-on-an-xml-schema"></a><span data-ttu-id="f7433-174">Para generar un objeto XMLport basado en un esquema XML</span><span class="sxs-lookup"><span data-stu-id="f7433-174">To generate an XMLport that is based on an XML schema</span></span>  

1.  <span data-ttu-id="f7433-175">En el cuadro **Buscar**, escriba **Esquemas XML** y, a continuación, elija el vínculo relacionado.</span><span class="sxs-lookup"><span data-stu-id="f7433-175">In the **Search** box, enter  **XML Schemas**, and then choose the related link.</span></span>  

2.  <span data-ttu-id="f7433-176">Seleccione el esquema XML y, a continuación, en la pestaña **Inicio**, en el grupo **Procesar**, elija **Abrir Visor de esquema XML**.</span><span class="sxs-lookup"><span data-stu-id="f7433-176">Select the relevant XML schema, and then on the on the **Home** tab, in the **Process** group, choose **Open XML Schema Viewer**.</span></span>  

3.  <span data-ttu-id="f7433-177">En el campo **N.º XMLport nuevo**</span><span class="sxs-lookup"><span data-stu-id="f7433-177">In the **New XMLport No.**</span></span> <span data-ttu-id="f7433-178">especifique el número que recibirá el nuevo objeto XMLport cuando se genere.</span><span class="sxs-lookup"><span data-stu-id="f7433-178">field, specify the number that the new XMLport object will be given when it is generated.</span></span>  

4.  <span data-ttu-id="f7433-179">Asegúrese de que estén seleccionados los nodos correspondientes.</span><span class="sxs-lookup"><span data-stu-id="f7433-179">Make sure the relevant nodes are selected.</span></span> <span data-ttu-id="f7433-180">Para obtener más información, consulte la sección "Para seleccionar o borrar nodos en un esquema XML".</span><span class="sxs-lookup"><span data-stu-id="f7433-180">For more information, see the “To select or clear nodes in an XML schema” section.</span></span>  

5.  <span data-ttu-id="f7433-181">En la pestaña **Inicio**, en el grupo **Procesar**, seleccione **Generar XMLport** y, a continuación, guarde el objeto como un archivo .txt en una ubicación adecuada.</span><span class="sxs-lookup"><span data-stu-id="f7433-181">On the **Home** tab, in the **Process** group, choose **Generate XMLport**, and then save the object as a .txt file in an appropriate location.</span></span>  

6. <span data-ttu-id="f7433-182">Importe el nuevo XMLport en el entorno de desarrollo de [!INCLUDE[d365fin](includes/d365fin_md.md)] y compílelo.</span><span class="sxs-lookup"><span data-stu-id="f7433-182">Import the new XMLport into the [!INCLUDE[d365fin](includes/d365fin_md.md)] development environment and compile it.</span></span>

## <a name="see-also"></a><span data-ttu-id="f7433-183">Consulte también</span><span class="sxs-lookup"><span data-stu-id="f7433-183">See Also</span></span>  
<span data-ttu-id="f7433-184">[Procedimiento: Configurar las definiciones de intercambio de datos](across-how-to-set-up-data-exchange-definitions.md) </span><span class="sxs-lookup"><span data-stu-id="f7433-184">[How to: Set Up Data Exchange Definitions](across-how-to-set-up-data-exchange-definitions.md) </span></span>  
<span data-ttu-id="f7433-185">[Exportación de pagos a un archivo de banco](payables-how-export-payments-bank-file.md) </span><span class="sxs-lookup"><span data-stu-id="f7433-185">[How to: Export Payments to a Bank File](payables-how-export-payments-bank-file.md) </span></span>  
<span data-ttu-id="f7433-186">[Cobrar pagos mediante adeudo directo SEPA](finance-collect-payments-with-sepa-direct-debit.md) </span><span class="sxs-lookup"><span data-stu-id="f7433-186">[Collect Payments with SEPA Direct Debit](finance-collect-payments-with-sepa-direct-debit.md) </span></span>  
[<span data-ttu-id="f7433-187">Acerca del marco de intercambio de datos</span><span class="sxs-lookup"><span data-stu-id="f7433-187">About the Data Exchange Framework</span></span>](across-about-the-data-exchange-framework.md)

