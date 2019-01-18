---
title: "Descripción de cómo registrar documentos de compra | Documentos de Microsoft"
description: "Obtenga información sobre las diversas funciones de registro para registrar documentos de compra."
services: project-madeira
documentationcenter: 
author: SusanneWindfeldPedersen
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 10/01/2018
ms.author: solsen
ms.translationtype: HT
ms.sourcegitcommit: 33b900f1ac9e295921e7f3d6ea72cc93939d8a1b
ms.openlocfilehash: 5f3c709e6e2588fe7cf409e44291d331acc09432
ms.contentlocale: es-es
ms.lasthandoff: 11/26/2018

---
# <a name="posting-purchases"></a><span data-ttu-id="c0f90-103">Registrar compras</span><span class="sxs-lookup"><span data-stu-id="c0f90-103">Posting Purchases</span></span>
<span data-ttu-id="c0f90-104">En **Grupo contable** en un documento de compra, puede elegir entre las funciones de registro siguientes:</span><span class="sxs-lookup"><span data-stu-id="c0f90-104">In the **Posting group** on a purchase document, you can choose between the following posting functions:</span></span>

* <span data-ttu-id="c0f90-105">**Registrar**</span><span class="sxs-lookup"><span data-stu-id="c0f90-105">**Post**</span></span>
* <span data-ttu-id="c0f90-106">**Vista previa de registro**</span><span class="sxs-lookup"><span data-stu-id="c0f90-106">**Preview Posting**</span></span>
* <span data-ttu-id="c0f90-107">**Registrar e imprimir**</span><span class="sxs-lookup"><span data-stu-id="c0f90-107">**Post and Print**</span></span>
* <span data-ttu-id="c0f90-108">**Informe de prueba**</span><span class="sxs-lookup"><span data-stu-id="c0f90-108">**Test Report**</span></span>
* <span data-ttu-id="c0f90-109">**Registrar por lotes**</span><span class="sxs-lookup"><span data-stu-id="c0f90-109">**Post Batch**</span></span>

<span data-ttu-id="c0f90-110">Una vez completadas todas las líneas e introducida la información en el pedido de compra, podrá registrarlo; es decir, crear un albarán de compra y una factura.</span><span class="sxs-lookup"><span data-stu-id="c0f90-110">When you have completed all the lines and entered all the information on the purchase order, you can post it, that is, create a receipt and an invoice.</span></span>

<span data-ttu-id="c0f90-111">Cuando se registra un pedido de compra, se actualiza la cuenta del proveedor, la contabilidad y los movimientos de producto.</span><span class="sxs-lookup"><span data-stu-id="c0f90-111">When a purchase order is posted, the vendor's account, the general ledger, and the item ledger entries are updated.</span></span>

<span data-ttu-id="c0f90-112">Por cada pedido de compra, se crea un movimiento de compra en la tabla **Mov. contabilidad**.</span><span class="sxs-lookup"><span data-stu-id="c0f90-112">For each purchase order, a purchase entry is created in the **G/L Entry** table.</span></span> <span data-ttu-id="c0f90-113">Se crea también un movimiento en la cuenta de proveedor de la tabla **Mov. proveedor** y un movimiento de contabilidad en la correspondiente cuenta de pagos.</span><span class="sxs-lookup"><span data-stu-id="c0f90-113">An entry is also created in the vendor's account in the **Vendor Ledger Entry** table and a G/L entry is created in the relevant payables account.</span></span> <span data-ttu-id="c0f90-114">Además, el registro del pedido puede dar como resultado un movimiento de IVA y uno de contabilidad para el importe de descuento.</span><span class="sxs-lookup"><span data-stu-id="c0f90-114">In addition, posting the order may result in a VAT entry and a G/L entry for the discount amount.</span></span> <span data-ttu-id="c0f90-115">El que se registre un movimiento para el descuento depende del contenido del campo **Registro dto.** de la página **Conf. compras y pagos**.</span><span class="sxs-lookup"><span data-stu-id="c0f90-115">Whether an entry for the discount is posted depends on the contents of the **Discount Posting** field on the **Purchases & Payables Setup** page.</span></span>

<span data-ttu-id="c0f90-116">Por cada línea de pedido de compra, se creará un movimiento de producto en la tabla **Mov. producto** (si las líneas de compra contienen números de producto) o un movimiento de contabilidad en la tabla **Mov. contabilidad** (si las líneas de compra contienen una cuenta de contabilidad).</span><span class="sxs-lookup"><span data-stu-id="c0f90-116">For each purchase order line, an item ledger entry will be created in the **Item Ledger Entry** table (if the purchase lines contain item numbers) or a G/L entry will be created in the **G/L Entry** table (if the purchase lines contain a G/L account).</span></span> <span data-ttu-id="c0f90-117">Además, los pedidos de compra siempre se registran en las tablas **Histórico cab. albarán compra** e **Histórico cab. factura compra**.</span><span class="sxs-lookup"><span data-stu-id="c0f90-117">In addition, purchase orders are always recorded in the **Purch. Recpt. Header** and **Purch. Inv. Header** tables.</span></span>

<span data-ttu-id="c0f90-118">Antes de comenzar a registrar, podrá imprimir un informe que contenga toda la información del pedido de compra y que indique cualquier error que pueda existir allí.</span><span class="sxs-lookup"><span data-stu-id="c0f90-118">Before you start to post, you can print a test report that contains all the information in the purchase order and indicates any errors there.</span></span> <span data-ttu-id="c0f90-119">Para imprimir este informe, elija **Registro** y, a continuación, **Informe de prueba**.</span><span class="sxs-lookup"><span data-stu-id="c0f90-119">To print the report, choose **Posting**, and then choose **Test Report**.</span></span>

> [!IMPORTANT]  
>   <span data-ttu-id="c0f90-120">Cuando registre un pedido, podrá crear tanto un albarán de compra como una factura.</span><span class="sxs-lookup"><span data-stu-id="c0f90-120">When you post an order, you can create both a receipt and an invoice.</span></span> <span data-ttu-id="c0f90-121">Esto se puede hacer simultánea o independientemente.</span><span class="sxs-lookup"><span data-stu-id="c0f90-121">These can be done simultaneously or independently.</span></span> <span data-ttu-id="c0f90-122">También puede crear una recepción y una factura parciales completando los campos **Cantidad a recibir** o **Cantidad a facturar** en las líneas individuales del pedido de compra antes de registrar.</span><span class="sxs-lookup"><span data-stu-id="c0f90-122">You can also create a partial receipt and a partial invoice by completing the **Qty. to Receive** and **Qty. to Invoice** fields on the individual purchase order lines before you post.</span></span> <span data-ttu-id="c0f90-123">Tenga en cuenta que no puede crear una factura de algo no se ha recibido.</span><span class="sxs-lookup"><span data-stu-id="c0f90-123">Note that you cannot create an invoice for something that has not been received.</span></span> <span data-ttu-id="c0f90-124">Es decir, antes de poder facturar debe haber registrado un albarán de compra o haber elegido recibir y facturar al mismo tiempo.</span><span class="sxs-lookup"><span data-stu-id="c0f90-124">That is, before you can invoice, you must have recorded a receipt, or you must choose to receive and invoice at the same time.</span></span>

<span data-ttu-id="c0f90-125">Puede registrar o registrar e imprimir.</span><span class="sxs-lookup"><span data-stu-id="c0f90-125">You can either post, or post and print.</span></span> <span data-ttu-id="c0f90-126">Si elije registrar e imprimir, un informe se imprime cuando se registre el pedido.</span><span class="sxs-lookup"><span data-stu-id="c0f90-126">If you choose to post and print, a report is printed when the order is posted.</span></span> <span data-ttu-id="c0f90-127">También puede elegir la función **Registrar por lotes**, que permite registrar varios pedidos a la vez.</span><span class="sxs-lookup"><span data-stu-id="c0f90-127">You can also choose the **Post Batch** function, which lets you post several orders at the same time.</span></span>

<span data-ttu-id="c0f90-128">Una vez finalizado el registro, las líneas de compra registradas se quitan del pedido.</span><span class="sxs-lookup"><span data-stu-id="c0f90-128">When the posting is completed, the posted purchase lines are removed from the order.</span></span> <span data-ttu-id="c0f90-129">Al terminar el registro aparece un mensaje de aviso.</span><span class="sxs-lookup"><span data-stu-id="c0f90-129">A message tells you when the posting is completed.</span></span> <span data-ttu-id="c0f90-130">Después de esto, podrá ver los movimientos registrados en las diferentes páginas que los contienen, como **Movs. proveedores**, **Movs, contabilidad**, **Movs. productos**, **Albaranes compra** e **Histórico facturas compra**.</span><span class="sxs-lookup"><span data-stu-id="c0f90-130">After this, you will be able to see the posted entries in the various pages that contain posted entries, such as the **Vendor Ledger Entries**, **G/L Entries**, **Item Ledger Entries**, **Purchase Receipts**, and **Posted Purchase Invoices** pages.</span></span>

## <a name="see-also"></a><span data-ttu-id="c0f90-131">Consulte también</span><span class="sxs-lookup"><span data-stu-id="c0f90-131">See Also</span></span>
[<span data-ttu-id="c0f90-132">Compras</span><span class="sxs-lookup"><span data-stu-id="c0f90-132">Purchasing</span></span>](purchasing-manage-purchasing.md)  
[<span data-ttu-id="c0f90-133">Registrar documentos y diarios</span><span class="sxs-lookup"><span data-stu-id="c0f90-133">Post Documents and Journals</span></span>](ui-post-documents-journals.md)  
<span data-ttu-id="c0f90-134">[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="c0f90-134">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>


