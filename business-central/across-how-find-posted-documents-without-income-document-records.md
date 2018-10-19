---
title: Buscar documentos sin archivos adjuntos | Documentos de Microsoft
Description: You can search for general ledger entries for posted purchase and sales documents that do not have incoming electronic documents, such as imported invoices.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: electronic document, e-invoice, incoming document, OCR, ecommerce, document exchange, import invoice
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: b1cf93c93ac9de204fafce1ada3c3e5687cbd682
ms.contentlocale: es-es
ms.lasthandoff: 09/28/2018

---
# <a name="find-posted-documents-without-incoming-document-records"></a><span data-ttu-id="3f7b0-102">Buscar documentos registrados sin registros de documentos entrantes</span><span class="sxs-lookup"><span data-stu-id="3f7b0-102">Find Posted Documents without Incoming Document Records</span></span>
<span data-ttu-id="3f7b0-103">Desde las ventanas **Plan de cuentas** y **Movs. contabilidad**, podrá usar una función de búsqueda para buscar los movimientos de contabilidad para aquellos documentos de compra y de venta registrados que no tienen registros de documento entrantes y después vincularlos de forma centralizada a registros existentes o crear registros nuevos con archivos de documentos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="3f7b0-103">From the **Chart of Accounts** and **General Ledger Entries** windows, you can use a search function to find general ledger entries for posted purchase and sales documents that do not have incoming document records and then centrally link to existing records or create new ones with attached document files.</span></span>

## <a name="to-find-posted-documents-without-incoming-document-records"></a><span data-ttu-id="3f7b0-104">para buscar documentos registrados sin registros de documentos entrantes</span><span class="sxs-lookup"><span data-stu-id="3f7b0-104">To find posted documents without incoming document records</span></span>
1. <span data-ttu-id="3f7b0-105">Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Plan de cuentas** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="3f7b0-105">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Chart of Accounts**, and then choose the related link.</span></span>
2. <span data-ttu-id="3f7b0-106">Seleccione una línea para una cuenta de contabilidad para la que quiere ver los documentos de ventas y compras registrados de los movimientos de contabilidad sin registros de documentos entrantes y, a continuación, seleccione la acción **Documentos registrados sin documento entrante**.</span><span class="sxs-lookup"><span data-stu-id="3f7b0-106">Select a line for a G/L account for whose general ledger entries you want to see posted purchase and sales documents without incoming document records, and then choose the **Posted Documents without Incoming Document** action.</span></span>
3. <span data-ttu-id="3f7b0-107">De forma alternativa, elija la acción **Movimientos de activos**.</span><span class="sxs-lookup"><span data-stu-id="3f7b0-107">Alternatively, choose the **Ledger Entries** action.</span></span>
4. <span data-ttu-id="3f7b0-108">En la ventana **Movs. contabilidad**, elija la acción **Documentos registrados sin documento entrante**.</span><span class="sxs-lookup"><span data-stu-id="3f7b0-108">In the **General Ledger Entries** window, choose the **Posted Documents without Incoming Documents** action.</span></span>

<span data-ttu-id="3f7b0-109">La ventana **Documentos registrados sin documento entrante** se abre con los documentos registrados de compra y de venta sin registros de documento entrantes representados por los movimientos de contabilidad de la cuenta para la que abrió la ventana.</span><span class="sxs-lookup"><span data-stu-id="3f7b0-109">The **Posted Documents without Incoming Document** window opens showing posted purchase and sales documents without incoming document records represented by general ledger entries on the G/L account that you opened the window for.</span></span> <span data-ttu-id="3f7b0-110">La ventana puede mostrar un máximo de 1000 líneas.</span><span class="sxs-lookup"><span data-stu-id="3f7b0-110">The window can show a maximum of 1000 lines.</span></span> <span data-ttu-id="3f7b0-111">De manera predeterminada, el campo **Filtro de fecha** contiene un filtro que limita las líneas a los movimientos con fechas de registro desde el inicio del periodo contable a la fecha de trabajo.</span><span class="sxs-lookup"><span data-stu-id="3f7b0-111">By default, the **Date Filter** field therefore contains a filter that limits the lines to entries with posting dates from the beginning of the accounting period to the work date.</span></span>

## <a name="to-connect-found-documents-to-existing-incoming-document-records"></a><span data-ttu-id="3f7b0-112">Para vincular los documentos encontrados con registros de documento entrantes existentes</span><span class="sxs-lookup"><span data-stu-id="3f7b0-112">To connect found documents to existing incoming document records</span></span>
1. <span data-ttu-id="3f7b0-113">En la ventana **Documentos registrados sin documento entrante**, seleccione la línea para un documento registrado que desee conectar con un registro de documento entrante existente y, a continuación, elija la acción **Seleccionar documento entrante**.</span><span class="sxs-lookup"><span data-stu-id="3f7b0-113">In the **Posted Documents without Incoming Document** window, select the line for a posted document that you want to connect to an existing incoming document record, and then choose the **Select Incoming Document** action.</span></span>
2. <span data-ttu-id="3f7b0-114">En la ventana **Documentos entrantes**, seleccione el registro de documento entrante que desea agregar para conectarlo con el documento registrado encontrado y, a continuación, elija el botón **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="3f7b0-114">In the **Incoming Documents** window, select the incoming document record that you want to connect to posted document found, and then choose the **OK** button.</span></span>
3. <span data-ttu-id="3f7b0-115">En la ventana **Documentos registrados sin documento entrante**, el registro de documento entrante seleccionado ahora está vinculado con el documento registrado, como se puede ver en el cuadro informativo **Archivos de documento entrante**.</span><span class="sxs-lookup"><span data-stu-id="3f7b0-115">In the **Posted Documents without Incoming Document** window, the selected incoming document record is now connected to the posted document, as you can see in the **Incoming Document Files** FactBox.</span></span>

<span data-ttu-id="3f7b0-116">Si no existe un registro de documento entrante correspondiente en la ventana **Documentos entrantes**, puede crearlo.</span><span class="sxs-lookup"><span data-stu-id="3f7b0-116">If a relevant incoming document record does not exist in the **Incoming Documents** window, then you can create it.</span></span> <span data-ttu-id="3f7b0-117">Para obtener más información, vea [Crear registros de documentos entrantes](across-how-create-income-document-records.md).</span><span class="sxs-lookup"><span data-stu-id="3f7b0-117">For more information, see [Create Incoming Document Records](across-how-create-income-document-records.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="3f7b0-118">Consulte también</span><span class="sxs-lookup"><span data-stu-id="3f7b0-118">See Also</span></span>
[<span data-ttu-id="3f7b0-119">Procesar documentos entrantes</span><span class="sxs-lookup"><span data-stu-id="3f7b0-119">Process Incoming Documents</span></span>](across-process-income-documents.md)  
[<span data-ttu-id="3f7b0-120">Documentos entrantes</span><span class="sxs-lookup"><span data-stu-id="3f7b0-120">Incoming Documents</span></span>](across-income-documents.md)  
[<span data-ttu-id="3f7b0-121">Compras</span><span class="sxs-lookup"><span data-stu-id="3f7b0-121">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="3f7b0-122">[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="3f7b0-122">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

