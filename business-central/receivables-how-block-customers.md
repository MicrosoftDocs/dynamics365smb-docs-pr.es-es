---
title: Cómo bloquear ventas a clientes
description: Si es necesario, puede bloquear la inclusión de un cliente en documentos de ventas y otras transacciones de ventas.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 8401b02677be48d06de2c3dbd67efd1ea8dd18cd
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5392704"
---
# <a name="block-customers"></a><span data-ttu-id="6cc26-103">Bloquear clientes</span><span class="sxs-lookup"><span data-stu-id="6cc26-103">Block Customers</span></span>
<span data-ttu-id="6cc26-104">Puede bloquear a un cliente, por ejemplo, por insolvencia, para que el no pueda añadirse a los documentos de ventas o para que no se puedan registrar transacciones para el cliente.</span><span class="sxs-lookup"><span data-stu-id="6cc26-104">You can block a customer, for example because of insolvency, so that the customer cannot be added to sales documents or so that no transactions can be posted for the customer.</span></span>

<span data-ttu-id="6cc26-105">Además de bloquear a un cliente, puede configurar las transacciones por cobrar para que el cliente esté en espera en conexión con los recordatorios.</span><span class="sxs-lookup"><span data-stu-id="6cc26-105">In addition to blocking a customer, you can set receivable transactions for the customer to be on hold in connection with reminders.</span></span> <span data-ttu-id="6cc26-106">Para obtener más información, vea [Cobrar saldos pendientes](receivables-collect-outstanding-balances.md).</span><span class="sxs-lookup"><span data-stu-id="6cc26-106">For more information, see [Collect Outstanding Balances](receivables-collect-outstanding-balances.md).</span></span>   

<span data-ttu-id="6cc26-107">La siguiente tabla describe las distintas opciones de bloqueo de clientes.</span><span class="sxs-lookup"><span data-stu-id="6cc26-107">The following table describes the options for blocking customers.</span></span>  

|<span data-ttu-id="6cc26-108">Opción</span><span class="sxs-lookup"><span data-stu-id="6cc26-108">Option</span></span>|<span data-ttu-id="6cc26-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="6cc26-109">Description</span></span>|  
|--------------------|------------|  
|<span data-ttu-id="6cc26-110">**En blanco**</span><span class="sxs-lookup"><span data-stu-id="6cc26-110">**Blank**</span></span>|<span data-ttu-id="6cc26-111">Se permiten las transacciones de este cliente.</span><span class="sxs-lookup"><span data-stu-id="6cc26-111">Transactions are allowed for this customer.</span></span>|
|<span data-ttu-id="6cc26-112">**Envío**</span><span class="sxs-lookup"><span data-stu-id="6cc26-112">**Ship**</span></span>|<span data-ttu-id="6cc26-113">No se pueden crear pedidos y envíos nuevos para este cliente.</span><span class="sxs-lookup"><span data-stu-id="6cc26-113">New orders and new shipments cannot be created for this customer.</span></span> <span data-ttu-id="6cc26-114">Los envíos existentes no facturados aún se pueden facturar.</span><span class="sxs-lookup"><span data-stu-id="6cc26-114">Existing shipments not yet invoiced can be invoiced.</span></span>|  
|<span data-ttu-id="6cc26-115">**Factura**</span><span class="sxs-lookup"><span data-stu-id="6cc26-115">**Invoice**</span></span>|<span data-ttu-id="6cc26-116">No se pueden crear facturas, pedidos ni envíos nuevos para este cliente.</span><span class="sxs-lookup"><span data-stu-id="6cc26-116">New orders, new shipments, and new invoices cannot be created for this customer.</span></span> <span data-ttu-id="6cc26-117">Los envíos existentes no facturados aún no se pueden facturar.</span><span class="sxs-lookup"><span data-stu-id="6cc26-117">Existing shipments not yet invoiced cannot be invoiced.</span></span> <span data-ttu-id="6cc26-118">Aún puede enviar recordatorios y documentos de interés al cliente.</span><span class="sxs-lookup"><span data-stu-id="6cc26-118">You can still send reminders and finance charge memos to the customer.</span></span>|  
|<span data-ttu-id="6cc26-119">**Todo**</span><span class="sxs-lookup"><span data-stu-id="6cc26-119">**All**</span></span>|<span data-ttu-id="6cc26-120">No se permite ninguna transacción para este cliente, incluidos los pagos.</span><span class="sxs-lookup"><span data-stu-id="6cc26-120">No transaction is allowed for this customer, including payments.</span></span>|  

## <a name="to-block-a-customer"></a><span data-ttu-id="6cc26-121">Para bloquear a un cliente</span><span class="sxs-lookup"><span data-stu-id="6cc26-121">To block a customer</span></span>  
1. <span data-ttu-id="6cc26-122">Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Clientes** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="6cc26-122">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Customers**, and then choose the related link.</span></span>
2. <span data-ttu-id="6cc26-123">Seleccione un cliente y, a continuación, elija la acción **Editar**.</span><span class="sxs-lookup"><span data-stu-id="6cc26-123">Select a customer, and then choose the **Edit** action.</span></span>
3. <span data-ttu-id="6cc26-124">En el campo **Bloqueado**, elija qué bloquear, como se describe en la tabla anterior.</span><span class="sxs-lookup"><span data-stu-id="6cc26-124">In the **Blocked** field, choose what to block, as described in the table above.</span></span>

## <a name="see-also"></a><span data-ttu-id="6cc26-125">Consulte también</span><span class="sxs-lookup"><span data-stu-id="6cc26-125">See Also</span></span>  
[<span data-ttu-id="6cc26-126">Permite registrar nuevos clientes</span><span class="sxs-lookup"><span data-stu-id="6cc26-126">Register New Customers</span></span>](sales-how-register-new-customers.md)  
[<span data-ttu-id="6cc26-127">Cobrar saldos pendientes</span><span class="sxs-lookup"><span data-stu-id="6cc26-127">Collect Outstanding Balances</span></span>](receivables-collect-outstanding-balances.md)  
[<span data-ttu-id="6cc26-128">Administrar cobros</span><span class="sxs-lookup"><span data-stu-id="6cc26-128">Managing Receivables</span></span>](receivables-manage-receivables.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]