---
title: Administre, elimine, o comprima los documentos | Documentos de Microsoft
description: "Conserve sus datos históricos o eliminelos."
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/01/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 292231a907970de2821daeba87003eca7bf54cdc
ms.contentlocale: es-es
ms.lasthandoff: 03/22/2018

---
# <a name="manage-documents"></a><span data-ttu-id="0d8da-103">Administración de documentos</span><span class="sxs-lookup"><span data-stu-id="0d8da-103">Manage Documents</span></span>
<span data-ttu-id="0d8da-104">Un rol central, como el administrador de aplicaciones, debe eliminar o comprimir periódicamente los documentos históricos para gestionar su acumulación.</span><span class="sxs-lookup"><span data-stu-id="0d8da-104">A central role, such as the application administrator, must regularly deal with accumulating historic documents by deleting or compressing them.</span></span>  

## <a name="delete-documents"></a><span data-ttu-id="0d8da-105">Eliminar documentos</span><span class="sxs-lookup"><span data-stu-id="0d8da-105">Delete Documents</span></span>
<span data-ttu-id="0d8da-106">En algunos casos, es posible que necesite eliminar pedidos de compra facturados que no se hayan eliminado.</span><span class="sxs-lookup"><span data-stu-id="0d8da-106">In certain situations, you may need to delete invoiced purchase orders that have not been deleted.</span></span> [!INCLUDE[d365fin](includes/d365fin_md.md)]<span data-ttu-id="0d8da-107"> comprueba que se hayan facturado totalmente los pedidos de compra eliminados.</span><span class="sxs-lookup"><span data-stu-id="0d8da-107"> checks that you have fully invoiced the deleted purchase orders.</span></span> <span data-ttu-id="0d8da-108">No puede eliminar pedidos que no haya facturado y recibido en su totalidad.</span><span class="sxs-lookup"><span data-stu-id="0d8da-108">You cannot delete orders that you have not fully invoiced and received.</span></span>  

<span data-ttu-id="0d8da-109">Los pedidos de devolución generalmente se eliminan después de facturados.</span><span class="sxs-lookup"><span data-stu-id="0d8da-109">Return orders are usually deleted after they are invoiced.</span></span> <span data-ttu-id="0d8da-110">Cuando registra una factura, ésta se transfiere a la ventana **Histórico abono compra**.</span><span class="sxs-lookup"><span data-stu-id="0d8da-110">When you post an invoice, it is transferred to the **Posted Purchase Credit Memo** window.</span></span> <span data-ttu-id="0d8da-111">Si ha activado la casilla **Envío dev. en abono** en la ventana **Conf. compras y pagos**, la factura se transfiere a la ventana **Histórico envío devolución**.</span><span class="sxs-lookup"><span data-stu-id="0d8da-111">If you selected the **Return Shipment on Credit Memo** check box in the **Purchases & Payable Setup** window, then the invoice is transferred to the **Posted Return Shipment** window.</span></span> <span data-ttu-id="0d8da-112">Puede eliminar los documentos a partir de un trabajo por lotes **Borrar ped. dev. compras fact.**.</span><span class="sxs-lookup"><span data-stu-id="0d8da-112">You can delete the documents using the **Delete Invd Purch. Ret. Orders** batch job.</span></span> <span data-ttu-id="0d8da-113">Antes de eliminar, el trabajo por lotes comprueba si los pedidos devueltos de compra han sido enviados y facturados totalmente.</span><span class="sxs-lookup"><span data-stu-id="0d8da-113">Before deleting, the batch job checks if the purchase return orders are fully shipped and invoiced.</span></span>  

<span data-ttu-id="0d8da-114">Los pedidos abiertos de compra no se eliminan una vez que se han procesado y facturado todos los pedidos de compra relacionados.</span><span class="sxs-lookup"><span data-stu-id="0d8da-114">Blanket purchase orders are not deleted after you have processed and invoiced all the related purchase orders.</span></span> <span data-ttu-id="0d8da-115">Para eliminar pedidos abiertos de compra, puede utilizar el trabajo por lotes **Eliminar pedidos abiertos compra facturados**.</span><span class="sxs-lookup"><span data-stu-id="0d8da-115">You can delete blanket orders with the **Delete Invoiced Blanket Purchase Orders** batch job.</span></span>  

<span data-ttu-id="0d8da-116">Los pedidos de servicios facturados se suelen eliminar automáticamente después de haberse facturado en su totalidad.</span><span class="sxs-lookup"><span data-stu-id="0d8da-116">Invoiced service orders are usually deleted automatically after having been fully invoiced.</span></span> <span data-ttu-id="0d8da-117">Cuando se registra una factura, se crea un movimiento correspondiente en la ventana **Facts. ventas (servicio) regis.**</span><span class="sxs-lookup"><span data-stu-id="0d8da-117">When an invoice is posted, a corresponding entry is created in the **Posted Service Invoices** window.</span></span> <span data-ttu-id="0d8da-118">El documento registrado se puede ver en la ventana **Fact. ventas (servicio) regis.**</span><span class="sxs-lookup"><span data-stu-id="0d8da-118">The posted document can be viewed in the **Posted Service Invoice** window.</span></span>  

<span data-ttu-id="0d8da-119">Sin embargo, los pedidos de servicio no se eliminarán de forma automática si la cantidad total de dicho pedido no se ha registrado desde el pedido de servicio en sí, sino desde la ventana **Factura servicio**.</span><span class="sxs-lookup"><span data-stu-id="0d8da-119">Service orders are not deleted automatically, however, if the total quantity on the order has been posted not from the service order itself, but from the **Service Invoice** window.</span></span> <span data-ttu-id="0d8da-120">En este caso, puede que tenga que eliminar los pedidos facturados que no se hayan eliminado.</span><span class="sxs-lookup"><span data-stu-id="0d8da-120">Then you may need to delete invoiced orders that were not deleted.</span></span> <span data-ttu-id="0d8da-121">Para ello, ejecute el proceso **Eliminar ped. servicio facturados**.</span><span class="sxs-lookup"><span data-stu-id="0d8da-121">You can do this by running the **Delete Invoiced Service Orders** batch job.</span></span>  

## <a name="see-also"></a><span data-ttu-id="0d8da-122">Consulte también</span><span class="sxs-lookup"><span data-stu-id="0d8da-122">See Also</span></span>  
[<span data-ttu-id="0d8da-123">Configuración y administración en Business Central</span><span class="sxs-lookup"><span data-stu-id="0d8da-123">Setup and Administration in Business Central</span></span>](admin-setup-and-administration.md)  

