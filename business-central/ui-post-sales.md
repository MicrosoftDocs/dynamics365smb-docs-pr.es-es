---
title: Registro de documentos de ventas | Documentos de Microsoft
description: Obtenga información sobre las diferentes funciones de registro para registrar documentos de ventas y cómo puede actualizar los documentos registrados.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.reviewer: edupont
ms.date: 08/27/2019
ms.author: sgroespe
ms.openlocfilehash: a2eb27a541033b755b9ab9d4ea9156bf7de9cab4
ms.sourcegitcommit: f46793abdb3efd8384c10eb7992e076383251f2c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 08/27/2019
ms.locfileid: "1921435"
---
# <a name="posting-sales"></a><span data-ttu-id="4eef9-103">Registrar ventas</span><span class="sxs-lookup"><span data-stu-id="4eef9-103">Posting Sales</span></span>
<span data-ttu-id="4eef9-104">En el menú **Registro** en un documento de venta, puede elegir entre las funciones de registro siguientes:</span><span class="sxs-lookup"><span data-stu-id="4eef9-104">Under the **Posting** menu in a sales document, you can choose between the following posting functions:</span></span>

* <span data-ttu-id="4eef9-105">**Registrar**</span><span class="sxs-lookup"><span data-stu-id="4eef9-105">**Post**</span></span>
* <span data-ttu-id="4eef9-106">**Registrar y nuevo**</span><span class="sxs-lookup"><span data-stu-id="4eef9-106">**Post and New**</span></span>
* <span data-ttu-id="4eef9-107">**Registrar y enviar**</span><span class="sxs-lookup"><span data-stu-id="4eef9-107">**Post and Send**</span></span>
* <span data-ttu-id="4eef9-108">**Vista previa de registro**</span><span class="sxs-lookup"><span data-stu-id="4eef9-108">**Preview Posting**</span></span>
* <span data-ttu-id="4eef9-109">**Borrador de factura**</span><span class="sxs-lookup"><span data-stu-id="4eef9-109">**Draft Invoice**</span></span>
* <span data-ttu-id="4eef9-110">**Factura proforma**</span><span class="sxs-lookup"><span data-stu-id="4eef9-110">**Pro Forma Invoice**</span></span>
* <span data-ttu-id="4eef9-111">**Informe de prueba**</span><span class="sxs-lookup"><span data-stu-id="4eef9-111">**Test Report**</span></span>

<span data-ttu-id="4eef9-112">Una vez completadas todas las líneas e introducida toda la información en el pedido de venta, puede registrarlo.</span><span class="sxs-lookup"><span data-stu-id="4eef9-112">When you have completed all the lines and entered all the information on the sales order, you can post it.</span></span> <span data-ttu-id="4eef9-113">Esto crea un envío y una factura.</span><span class="sxs-lookup"><span data-stu-id="4eef9-113">This creates a shipment and an invoice.</span></span>

<span data-ttu-id="4eef9-114">Cuando se registra un pedido de venta, se actualiza la cuenta del cliente, la contabilidad y los movimientos de producto.</span><span class="sxs-lookup"><span data-stu-id="4eef9-114">When a sales order is posted, the customer's account, the general ledger, and the item ledger entries are updated.</span></span>

<span data-ttu-id="4eef9-115">Para cada pedido de venta, se crea un movimiento de venta en la tabla **Mov. contabilidad**.</span><span class="sxs-lookup"><span data-stu-id="4eef9-115">For each sales order, a sales entry is created in the **G/L Entry** table.</span></span> <span data-ttu-id="4eef9-116">Se crea también un movimiento en la cuenta de cliente de la tabla **Mov. cliente** y un movimiento de contabilidad en la cuenta de cliente correspondiente.</span><span class="sxs-lookup"><span data-stu-id="4eef9-116">An entry is also created in the customer's account in the **Cust. Ledger Entry** table and a general ledger entry is created in the relevant receivables account.</span></span> <span data-ttu-id="4eef9-117">Además, el registro del pedido puede dar como resultado un movimiento de IVA y uno de contabilidad para el importe de descuento.</span><span class="sxs-lookup"><span data-stu-id="4eef9-117">In addition, posting the order may result in a VAT entry and a general ledger entry for the discount amount.</span></span> <span data-ttu-id="4eef9-118">El registro de un movimiento para el descuento depende del contenido del campo **Registro dto.** de la página **Conf. ventas y cobros**.</span><span class="sxs-lookup"><span data-stu-id="4eef9-118">Whether an entry for the discount is posted depends on the contents of the **Discount Posting** field on the **Sales & Receivables Setup** page.</span></span>

<span data-ttu-id="4eef9-119">Por cada línea de pedido de venta, se creará un movimiento de producto en la tabla **Mov. producto** (si las líneas de venta contienen números de producto) o un movimiento de contabilidad en la tabla **Mov. contabilidad** (si las líneas de venta contienen una cuenta de contabilidad).</span><span class="sxs-lookup"><span data-stu-id="4eef9-119">For each sales order line, an item ledger entry will be created in the **Item Ledger Entry** table (if the sales lines contain item numbers) or a general ledger entry will be created in the **G/L Entry** table (if the sales lines contain a general ledger account).</span></span> <span data-ttu-id="4eef9-120">Además, los pedidos de venta siempre se registran en las tablas **Histórico cab. albarán venta** y **Histórico cab. factura venta**.</span><span class="sxs-lookup"><span data-stu-id="4eef9-120">In addition to this, sales orders are always recorded in the **Sales Shipment Header** and **Sales Invoice Header** tables.</span></span>

> [!IMPORTANT]  
>   <span data-ttu-id="4eef9-121">Cuando registre un pedido, puede crear un albarán de venta y una factura.</span><span class="sxs-lookup"><span data-stu-id="4eef9-121">When you post an order, you can create both a shipment and an invoice.</span></span> <span data-ttu-id="4eef9-122">Esto se puede realizar al mismo tiempo o de manera independiente.</span><span class="sxs-lookup"><span data-stu-id="4eef9-122">These can be done at the same time or independently.</span></span> <span data-ttu-id="4eef9-123">También puede crear un envío y una factura parciales completando los campos **Cantidad a enviar** y **Cantidad a facturar** en las líneas individuales del pedido de venta antes de registrar.</span><span class="sxs-lookup"><span data-stu-id="4eef9-123">You can also create a partial shipment and a partial invoice by completing the **Qty. to Ship** and **Qty. to Invoice** fields on the individual sales order lines before you post.</span></span> <span data-ttu-id="4eef9-124">Tenga en cuenta que no se puede crear una factura de algo que no se ha enviado.</span><span class="sxs-lookup"><span data-stu-id="4eef9-124">Note that you cannot create an invoice for something that is not shipped.</span></span> <span data-ttu-id="4eef9-125">Es decir, para poder facturar, debe haber registrado un envío, o bien debe elegir enviar y facturar al mismo tiempo.</span><span class="sxs-lookup"><span data-stu-id="4eef9-125">That is, before you can invoice, you must have recorded a shipment, or you must choose to ship and invoice at the same time.</span></span>

<span data-ttu-id="4eef9-126">Una vez completado el registro, las líneas de venta registradas se quitan del pedido.</span><span class="sxs-lookup"><span data-stu-id="4eef9-126">When the posting is completed, the posted sales lines are removed from the order.</span></span> <span data-ttu-id="4eef9-127">Al terminar el registro aparece un mensaje de aviso.</span><span class="sxs-lookup"><span data-stu-id="4eef9-127">A message tells you when the posting is completed.</span></span> <span data-ttu-id="4eef9-128">Después de esto, podrá ver los movimientos registrados en las diferentes páginas que los contienen, como **Movs. cliente**, **Movs. contabilidad**, **Movs. producto**, **Histórico albaranes ventas** y **Histórico facturas venta**.</span><span class="sxs-lookup"><span data-stu-id="4eef9-128">After this, you will be able to see the posted entries in the various pages that contain posted entries, such as the **Cust. Ledger Entries**, **G/L Entries**, **Item Ledger Entries**, **Posted Sales Shipments**, and **Posted Sales Invoices** pages.</span></span>  

<span data-ttu-id="4eef9-129">Puede editar determinados campos en documentos de venta registrados, como **Nº seguimiento bulto**.</span><span class="sxs-lookup"><span data-stu-id="4eef9-129">You can edit certain fields on posted sales documents, such as the **Package Tracking No.**</span></span> <span data-ttu-id="4eef9-130">.</span><span class="sxs-lookup"><span data-stu-id="4eef9-130">field.</span></span> <span data-ttu-id="4eef9-131">Para obtener más información, vea [Editar documentos registrados](across-edit-posted-document.md).</span><span class="sxs-lookup"><span data-stu-id="4eef9-131">For more information, see [Edit Posted Documents](across-edit-posted-document.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="4eef9-132">Consulte también</span><span class="sxs-lookup"><span data-stu-id="4eef9-132">See Also</span></span>
[<span data-ttu-id="4eef9-133">Ccial</span><span class="sxs-lookup"><span data-stu-id="4eef9-133">Sales</span></span>](sales-manage-sales.md)  
[<span data-ttu-id="4eef9-134">Editar documentos registrados</span><span class="sxs-lookup"><span data-stu-id="4eef9-134">Edit Posted Documents</span></span>](across-edit-posted-document.md)  
[<span data-ttu-id="4eef9-135">Enviar documentos por correo electrónico</span><span class="sxs-lookup"><span data-stu-id="4eef9-135">Send Documents by Email</span></span>](ui-how-send-documents-email.md)  
[<span data-ttu-id="4eef9-136">Corregir o cancelar facturas de venta sin abonar</span><span class="sxs-lookup"><span data-stu-id="4eef9-136">Correct or Cancel Unpaid Sales Invoices</span></span>](sales-how-correct-cancel-sales-invoice.md)  
[<span data-ttu-id="4eef9-137">Usar la opción Dígame para encontrar características e información</span><span class="sxs-lookup"><span data-stu-id="4eef9-137">Using Tell Me to Find Features and Information</span></span>](ui-search.md)  
<span data-ttu-id="4eef9-138">[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="4eef9-138">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
