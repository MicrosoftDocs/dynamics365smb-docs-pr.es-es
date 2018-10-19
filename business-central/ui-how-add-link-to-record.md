---
title: "Proceso para vincular desde registros hacia programas o información externa | Documentos de Microsoft"
description: "Adjuntar un hipervínculo a un documento o un sitio Web a un registro específico, como un documento de cliente."
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: c2e70ad534a28cf5062e9e54a2dfbd3af6afaa39
ms.contentlocale: es-es
ms.lasthandoff: 09/28/2018

---
# <a name="adding-links-to-websites-documents-or-programs-on-records"></a><span data-ttu-id="3f332-103">Agregar vínculos a páginas Web, documentos o programas en registros</span><span class="sxs-lookup"><span data-stu-id="3f332-103">Adding Links to Websites, Documents, or Programs on Records</span></span>
<span data-ttu-id="3f332-104">En un registro específico, como un cliente, documento, o pedido de venta, puede agregar un vínculo a un documento externo, una página Web, o programa.</span><span class="sxs-lookup"><span data-stu-id="3f332-104">On a specific record, such as a customer, document, or sales order, you can add a link to an external document, website, or program.</span></span> <span data-ttu-id="3f332-105">O bien, es posible que desee un vínculo que abra un nuevo mensaje de correo electrónico en blanco a un destinatario específico cuando lo seleccione.</span><span class="sxs-lookup"><span data-stu-id="3f332-105">Or, you may want a link that opens a new empty email to a specific recipient when you select it.</span></span> <span data-ttu-id="3f332-106">La página de fichas para algunos registros, como las fichas de cliente y proveedor, incluyen un campo **Página de inicio**, donde puede especificar una dirección de internet (URL).</span><span class="sxs-lookup"><span data-stu-id="3f332-106">The card page for some records, such as customer and vendor cards, include a **Home Page** field where you can enter an Internet address (URL).</span></span> <span data-ttu-id="3f332-107">Para incluir otros en vínculos, puede utilizar el método que se describe en este artículo.</span><span class="sxs-lookup"><span data-stu-id="3f332-107">To include other links, you can use the method described in this article.</span></span>

<span data-ttu-id="3f332-108">Otro ejemplo podría ser cuando recibe facturas impresas de proveedores.</span><span class="sxs-lookup"><span data-stu-id="3f332-108">Another example could be when you receive printed invoices from vendors.</span></span> <span data-ttu-id="3f332-109">Puede buscarlos y almacenarlos como archivos de .pdf en un sitio Web de SharePoint.</span><span class="sxs-lookup"><span data-stu-id="3f332-109">You can scan them and store them as .pdf files on a SharePoint site.</span></span> <span data-ttu-id="3f332-110">A continuación, puede establecer un vínculo desde una factura de compra en [!INCLUDE[d365fin_md](includes/d365fin_md.md)] a la factura correspondiente en SharePoint.</span><span class="sxs-lookup"><span data-stu-id="3f332-110">Then you can make a link from a purchase invoice in [!INCLUDE[d365fin_md](includes/d365fin_md.md)] to the corresponding invoice on  SharePoint.</span></span> <span data-ttu-id="3f332-111">o bien cree un vínculo de una ficha de producto a la página correspondiente del catálogo en línea del proveedor.</span><span class="sxs-lookup"><span data-stu-id="3f332-111">Or, you can make a link from an item card to the corresponding page in your vendor's online catalog.</span></span>

## <a name="to-add-a-link-on-a-record"></a><span data-ttu-id="3f332-112">Para agregar un vínculo a un registro</span><span class="sxs-lookup"><span data-stu-id="3f332-112">To add a link on a record</span></span>   

1.  <span data-ttu-id="3f332-113">Abra el registro al que desea asociar el vínculo.</span><span class="sxs-lookup"><span data-stu-id="3f332-113">Open the record that you want to attach the link to, such as a customer card or sales order.</span></span> <span data-ttu-id="3f332-114">Si desea agregar el vínculo a una línea específica, por ejemplo, a una línea de diario, selecciónela.</span><span class="sxs-lookup"><span data-stu-id="3f332-114">If you want to attach the link to a specific line, such as a journal line, select the line.</span></span>  

2.  <span data-ttu-id="3f332-115">Seleccione la acción **Vínculos** para abrir la ventana de **Vínculos** que muestra todos los vínculos actuales que están agregadas al registro.</span><span class="sxs-lookup"><span data-stu-id="3f332-115">Choose the **Links** action to open the **Links** windows that shows all the current links that are added to the record.</span></span>

3. <span data-ttu-id="3f332-116">Para agregar un nuevo vínculo, elija **+nuevo**.</span><span class="sxs-lookup"><span data-stu-id="3f332-116">To add a new link, choose **+new**.</span></span>

4.  <span data-ttu-id="3f332-117">En el campo **Vincular dirección**, especifique</span><span class="sxs-lookup"><span data-stu-id="3f332-117">In the **Link Address** field, enter</span></span>

    -   <span data-ttu-id="3f332-118">Para vincular un archivo en el equipo o red, introduzca la ruta de acceso completa y el nombre de archivo, como **C:Mis Documentsfactura1.doc**.</span><span class="sxs-lookup"><span data-stu-id="3f332-118">To link to a file on your computer or network, enter the full path and file name, such as  **C:My Documentsinvoice1.doc**.</span></span>
    -   <span data-ttu-id="3f332-119">Para vincular la página Web, especifique la dirección de Internet (URL), por ejemplo **www.microsoft.com**.</span><span class="sxs-lookup"><span data-stu-id="3f332-119">To link to website, enter the Internet address (URL), such as **www.microsoft.com**.</span></span>
    -   <span data-ttu-id="3f332-120">Para vincular la página Web, especifique la dirección de Internet (URL), por ejemplo **www.microsoft.com**.</span><span class="sxs-lookup"><span data-stu-id="3f332-120">To link to website, enter the Internet address (URL), such as **www.microsoft.com**.</span></span>
    -   <span data-ttu-id="3f332-121">Para vincular un programa, escriba una secuencia de caracteres específica para abrir el programa.</span><span class="sxs-lookup"><span data-stu-id="3f332-121">To link to a program, enter a specific string to open the program.</span></span> <span data-ttu-id="3f332-122">Por ejemplo, para abrir OneNote con una página específica, escriba **onenote:///C:Mis documentostest.one**.</span><span class="sxs-lookup"><span data-stu-id="3f332-122">For example, to open OneNote with a specific page, enter **onenote:///C:My Documentstest.one**.</span></span> <span data-ttu-id="3f332-123">O, para abrir Outlook con un nuevo mensaje de correo electrónico en blanco a un alias específico, escriba **mailto:testalias**.</span><span class="sxs-lookup"><span data-stu-id="3f332-123">Or, to open Outlook with a new empty email to a specific alias, enter **mailto:testalias**.</span></span>  

5.  <span data-ttu-id="3f332-124">Rellene el campo **Descripción** con información sobre el vínculo.</span><span class="sxs-lookup"><span data-stu-id="3f332-124">Fill in the **Description** field with information about the link.</span></span>  

6.  <span data-ttu-id="3f332-125">Haga clic en el botón **Guardar**.</span><span class="sxs-lookup"><span data-stu-id="3f332-125">Choose the **Save** button.</span></span>  

## <a name="to-delete-a-link-from-a-record"></a><span data-ttu-id="3f332-126">Para eliminar un vínculo de un registro</span><span class="sxs-lookup"><span data-stu-id="3f332-126">To delete a link from a record</span></span>  

<span data-ttu-id="3f332-127">Para eliminar un vínculo, en la ventana **Vínculos** , puede seleccionar **…** y después **Eliminar**.</span><span class="sxs-lookup"><span data-stu-id="3f332-127">To delete a link, in the **Links** window, you can select **...** and then **Delete**.</span></span>

<span data-ttu-id="3f332-128">Si elimina un único registro, por ejemplo, una línea de pedido de venta, un pedido de venta o un cliente, se eliminarán todos los vínculos asociados al registro.</span><span class="sxs-lookup"><span data-stu-id="3f332-128">If you delete a single record, such as a sales order line, a sales order, or a customer, then all the links attached to the record are deleted.</span></span> <span data-ttu-id="3f332-129">Sin embargo, si borra los registros utilizando un trabajo por lotes, como el trabajo por lotes **Eliminar pedidos de ventas facturados**, los vínculos se siguen guardando en la base de datos.</span><span class="sxs-lookup"><span data-stu-id="3f332-129">However, if you delete records using a batch job, such as the **Delete Invoiced Sales Orders** batch job, then the links are still stored in the database.</span></span> <span data-ttu-id="3f332-130">Para eliminarlos de la base de datos, ejecute el módulo **Eliminar vínculos reg. huérfanos**.</span><span class="sxs-lookup"><span data-stu-id="3f332-130">To delete the links from the database, run the **Delete Orphaned Record Links** codeunit.</span></span> <span data-ttu-id="3f332-131">Para ello, elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Eliminar vínculos reg. huérfanos** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="3f332-131">To do this, choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Delete Orphaned Record Links**, and then choose the related link.</span></span>   

<!-- ### To run delete orphaned record links  

1.  Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Data Deletion**, and then choose the related link.  

2.  In the **Data Deletion** window, choose **Tasks**, and then choose **Delete Orphaned Record Links**.  -->

## <a name="see-also"></a><span data-ttu-id="3f332-132">Consulte también</span><span class="sxs-lookup"><span data-stu-id="3f332-132">See Also</span></span>  
<span data-ttu-id="3f332-133">[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="3f332-133">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

