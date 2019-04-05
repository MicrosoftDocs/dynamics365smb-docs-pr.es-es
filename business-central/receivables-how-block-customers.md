---
title: Cómo bloquear ventas a productos de clientes desde el apartado de Ventas o Compras
description: En Business Central, un producto se puede marcar como bloqueado para ventas, bloqueado para compras o bloqueado para todos los propósitos.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2018
ms.author: sgroespe
ms.openlocfilehash: 268d098318b77cb89a369e8edc14729a44bedae6
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 03/08/2019
ms.locfileid: "806143"
---
# <a name="block-customers"></a><span data-ttu-id="a0de3-103">Bloquear clientes</span><span class="sxs-lookup"><span data-stu-id="a0de3-103">Block Customers</span></span>
<span data-ttu-id="a0de3-104">Puede bloquear a un cliente, por ejemplo, por insolvencia, para que el no pueda añadirse a los documentos de ventas o para que no se puedan registrar transacciones para el cliente.</span><span class="sxs-lookup"><span data-stu-id="a0de3-104">You can block a customer, for example because of insolvency, so that the customer cannot be added to sales documents or so that no transactions can be posted for the customer.</span></span>

<span data-ttu-id="a0de3-105">Además de bloquear a un cliente, puede configurar las transacciones por cobrar para que el cliente esté en espera en conexión con los recordatorios.</span><span class="sxs-lookup"><span data-stu-id="a0de3-105">In addition to blocking a customer, you can set receivable transactions for the customer to be on hold in connection with reminders.</span></span> <span data-ttu-id="a0de3-106">Para obtener más información, vea [Cobrar saldos pendientes](receivables-collect-outstanding-balances.md).</span><span class="sxs-lookup"><span data-stu-id="a0de3-106">For more information, see [Collect Outstanding Balances](receivables-collect-outstanding-balances.md).</span></span>   

<span data-ttu-id="a0de3-107">La siguiente tabla describe las distintas opciones de bloqueo.</span><span class="sxs-lookup"><span data-stu-id="a0de3-107">The following table describes the different blocking options.</span></span>  

|<span data-ttu-id="a0de3-108">Opción</span><span class="sxs-lookup"><span data-stu-id="a0de3-108">Option</span></span>|<span data-ttu-id="a0de3-109">Description</span><span class="sxs-lookup"><span data-stu-id="a0de3-109">Description</span></span>|  
|--------------------|------------|  
|<span data-ttu-id="a0de3-110">**En blanco**</span><span class="sxs-lookup"><span data-stu-id="a0de3-110">**Blank**</span></span>|<span data-ttu-id="a0de3-111">Se permiten las transacciones de este cliente.</span><span class="sxs-lookup"><span data-stu-id="a0de3-111">Transactions are allowed for this customer.</span></span>|
|<span data-ttu-id="a0de3-112">**Envío**</span><span class="sxs-lookup"><span data-stu-id="a0de3-112">**Ship**</span></span>|<span data-ttu-id="a0de3-113">No se pueden crear pedidos y envíos nuevos para este cliente.</span><span class="sxs-lookup"><span data-stu-id="a0de3-113">New orders and new shipments cannot be created for this customer.</span></span> <span data-ttu-id="a0de3-114">Los envíos existentes no facturados aún se pueden facturar.</span><span class="sxs-lookup"><span data-stu-id="a0de3-114">Existing shipments not yet invoiced can be invoiced.</span></span>|  
|<span data-ttu-id="a0de3-115">**Factura**</span><span class="sxs-lookup"><span data-stu-id="a0de3-115">**Invoice**</span></span>|<span data-ttu-id="a0de3-116">No se pueden crear facturas, pedidos ni envíos nuevos para este cliente.</span><span class="sxs-lookup"><span data-stu-id="a0de3-116">New orders, new shipments, and new invoices cannot be created for this customer.</span></span> <span data-ttu-id="a0de3-117">Los envíos existentes no facturados aún no se pueden facturar.</span><span class="sxs-lookup"><span data-stu-id="a0de3-117">Existing shipments not yet invoiced cannot be invoiced.</span></span>|  
|<span data-ttu-id="a0de3-118">**Todos**</span><span class="sxs-lookup"><span data-stu-id="a0de3-118">**All**</span></span>|<span data-ttu-id="a0de3-119">No se permite ninguna transacción para este cliente, incluidos los pagos.</span><span class="sxs-lookup"><span data-stu-id="a0de3-119">No transaction is allowed for this customer, including payments.</span></span>|  

## <a name="to-block-a-customer"></a><span data-ttu-id="a0de3-120">Para bloquear a un cliente</span><span class="sxs-lookup"><span data-stu-id="a0de3-120">To block a customer</span></span>  
1. <span data-ttu-id="a0de3-121">Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Clientes** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="a0de3-121">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Customers**, and then choose the related link.</span></span>
2. <span data-ttu-id="a0de3-122">Seleccione un cliente y, a continuación, elija la acción **Editar**.</span><span class="sxs-lookup"><span data-stu-id="a0de3-122">Select a customer, and then choose the **Edit** action.</span></span>
3. <span data-ttu-id="a0de3-123">Rellene el campo **Bloqueado** con una de las opciones descritas anteriormente.</span><span class="sxs-lookup"><span data-stu-id="a0de3-123">Fill in the **Blocked** field with one of the options described above.</span></span>

## <a name="see-also"></a><span data-ttu-id="a0de3-124">Consulte también</span><span class="sxs-lookup"><span data-stu-id="a0de3-124">See Also</span></span>  
[<span data-ttu-id="a0de3-125">Permite registrar nuevos clientes</span><span class="sxs-lookup"><span data-stu-id="a0de3-125">Register New Customers</span></span>](sales-how-register-new-customers.md)  
[<span data-ttu-id="a0de3-126">Cobrar saldos pendientes</span><span class="sxs-lookup"><span data-stu-id="a0de3-126">Collect Outstanding Balances</span></span>](receivables-collect-outstanding-balances.md)  
[<span data-ttu-id="a0de3-127">Administrar cobros</span><span class="sxs-lookup"><span data-stu-id="a0de3-127">Managing Receivables</span></span>](receivables-manage-receivables.md)  
