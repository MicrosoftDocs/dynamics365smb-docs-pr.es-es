---
title: Buscar documentos sin archivos adjuntos | Documentos de Microsoft
Description: Puede buscar movimientos de contabilidad de los documentos de compra y de venta registrados que no tengan documentos electrónicos de entrada, como las facturas importadas.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: electronic document, e-invoice, incoming document, OCR, ecommerce, document exchange, import invoice
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: b4a72567f470771b8f158f62bd70ef78d41408d6
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 03/31/2021
ms.locfileid: "5776002"
---
# <a name="find-posted-documents-without-incoming-document-records"></a><span data-ttu-id="9ef34-103">Buscar documentos registrados sin registros de documentos entrantes</span><span class="sxs-lookup"><span data-stu-id="9ef34-103">Find Posted Documents without Incoming Document Records</span></span>
<span data-ttu-id="9ef34-104">Desde las páginas **Plan de cuentas** y **Movs. contabilidad**, podrá usar una función de búsqueda para buscar los movimientos de contabilidad para aquellos documentos de compra y de venta registrados que no tienen registros de documento entrantes y después vincularlos de forma centralizada a registros existentes o crear registros nuevos con archivos de documentos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="9ef34-104">From the **Chart of Accounts** and **General Ledger Entries** pages, you can use a search function to find general ledger entries for posted purchase and sales documents that do not have incoming document records and then centrally link to existing records or create new ones with attached document files.</span></span>

## <a name="to-find-posted-documents-without-incoming-document-records"></a><span data-ttu-id="9ef34-105">para buscar documentos registrados sin registros de documentos entrantes</span><span class="sxs-lookup"><span data-stu-id="9ef34-105">To find posted documents without incoming document records</span></span>
1. <span data-ttu-id="9ef34-106">Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Plan de cuentas** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="9ef34-106">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Chart of Accounts**, and then choose the related link.</span></span>
2. <span data-ttu-id="9ef34-107">Seleccione una línea para una cuenta de contabilidad para la que quiere ver los documentos de ventas y compras registrados de los movimientos de contabilidad sin registros de documentos entrantes y, a continuación, seleccione la acción **Documentos registrados sin documento entrante**.</span><span class="sxs-lookup"><span data-stu-id="9ef34-107">Select a line for a G/L account for whose general ledger entries you want to see posted purchase and sales documents without incoming document records, and then choose the **Posted Documents without Incoming Document** action.</span></span>
3. <span data-ttu-id="9ef34-108">De forma alternativa, elija la acción **Movimientos de activos**.</span><span class="sxs-lookup"><span data-stu-id="9ef34-108">Alternatively, choose the **Ledger Entries** action.</span></span>
4. <span data-ttu-id="9ef34-109">En la página **Movs. contabilidad**, elija la acción **Documentos registrados sin documento entrante**.</span><span class="sxs-lookup"><span data-stu-id="9ef34-109">On the **General Ledger Entries** page, choose the **Posted Documents without Incoming Documents** action.</span></span>

<span data-ttu-id="9ef34-110">La página **Documentos registrados sin documento entrante** se abre con los documentos registrados de compra y de venta sin registros de documento entrantes representados por los movimientos de contabilidad de la cuenta para la que abrió la página.</span><span class="sxs-lookup"><span data-stu-id="9ef34-110">The **Posted Documents without Incoming Document** page opens showing posted purchase and sales documents without incoming document records represented by general ledger entries on the G/L account that you opened the page for.</span></span> <span data-ttu-id="9ef34-111">La página puede mostrar un máximo de 1000 líneas.</span><span class="sxs-lookup"><span data-stu-id="9ef34-111">The page can show a maximum of 1000 lines.</span></span> <span data-ttu-id="9ef34-112">De manera predeterminada, el campo **Filtro de fecha** contiene un filtro que limita las líneas a los movimientos con fechas de registro desde el inicio del periodo contable a la fecha de trabajo.</span><span class="sxs-lookup"><span data-stu-id="9ef34-112">By default, the **Date Filter** field therefore contains a filter that limits the lines to entries with posting dates from the beginning of the accounting period to the work date.</span></span>

## <a name="to-connect-found-documents-to-existing-incoming-document-records"></a><span data-ttu-id="9ef34-113">Para vincular los documentos encontrados con registros de documento entrantes existentes</span><span class="sxs-lookup"><span data-stu-id="9ef34-113">To connect found documents to existing incoming document records</span></span>
1. <span data-ttu-id="9ef34-114">En la página **Documentos registrados sin documento entrante**, seleccione la línea para un documento registrado que desee conectar con un registro de documento entrante existente y, a continuación, elija la acción **Seleccionar documento entrante**.</span><span class="sxs-lookup"><span data-stu-id="9ef34-114">On the **Posted Documents without Incoming Document** page, select the line for a posted document that you want to connect to an existing incoming document record, and then choose the **Select Incoming Document** action.</span></span>
2. <span data-ttu-id="9ef34-115">En la página **Documentos entrantes**, seleccione el registro de documento entrante que desea agregar para conectarlo con el documento registrado encontrado y, a continuación, elija el botón **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="9ef34-115">On the **Incoming Documents** page, select the incoming document record that you want to connect to posted document found, and then choose the **OK** button.</span></span>
3. <span data-ttu-id="9ef34-116">En la página **Documentos registrados sin documento entrante**, el registro de documento entrante seleccionado ahora está vinculado con el documento registrado, como se puede ver en el cuadro informativo **Archivos de documento entrante**.</span><span class="sxs-lookup"><span data-stu-id="9ef34-116">On the **Posted Documents without Incoming Document** page, the selected incoming document record is now connected to the posted document, as you can see in the **Incoming Document Files** FactBox.</span></span>

<span data-ttu-id="9ef34-117">Si no existe un registro de documento entrante correspondiente en la página **Documentos entrantes**, puede crearlo.</span><span class="sxs-lookup"><span data-stu-id="9ef34-117">If a relevant incoming document record does not exist on the **Incoming Documents** page, then you can create it.</span></span> <span data-ttu-id="9ef34-118">Para obtener más información, vea [Crear registros de documentos entrantes](across-how-create-income-document-records.md).</span><span class="sxs-lookup"><span data-stu-id="9ef34-118">For more information, see [Create Incoming Document Records](across-how-create-income-document-records.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="9ef34-119">Consulte también</span><span class="sxs-lookup"><span data-stu-id="9ef34-119">See Also</span></span>
[<span data-ttu-id="9ef34-120">Procesar documentos entrantes</span><span class="sxs-lookup"><span data-stu-id="9ef34-120">Process Incoming Documents</span></span>](across-process-income-documents.md)  
[<span data-ttu-id="9ef34-121">Documentos entrantes</span><span class="sxs-lookup"><span data-stu-id="9ef34-121">Incoming Documents</span></span>](across-income-documents.md)  
[<span data-ttu-id="9ef34-122">Compras</span><span class="sxs-lookup"><span data-stu-id="9ef34-122">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="9ef34-123">[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="9ef34-123">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>


[!INCLUDE[footer-include](includes/footer-banner.md)]