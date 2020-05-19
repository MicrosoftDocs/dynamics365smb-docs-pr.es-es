---
title: Cómo imprimir una lista de picking de inventario a partir de un pedido de venta
description: Puede imprimir una lista de picking de inventario directamente desde un pedido de ventas, ventas, factura y otros documentos de venta de salida.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/27/2020
ms.author: sgroespe
ms.openlocfilehash: d5eaad5279445375ec00fdf42dd48bffa5d03645
ms.sourcegitcommit: 7d54d8abe52e0546378cf760f5082f46e8441b90
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/30/2020
ms.locfileid: "3324477"
---
# <a name="print-the-picking-list"></a><span data-ttu-id="87acc-103">Imprimir la lista de picking</span><span class="sxs-lookup"><span data-stu-id="87acc-103">Print the Picking List</span></span>
<span data-ttu-id="87acc-104">Puede imprimir una lista de picking de inventario directamente desde un pedido de ventas, una factura de venta y otros documentos que inicien el envío de los productos.</span><span class="sxs-lookup"><span data-stu-id="87acc-104">You can print an inventory picking list directly from a sales order, a sales invoice, or any other document that initiates shipment of items.</span></span>

<span data-ttu-id="87acc-105">Este informe se utiliza normalmente en empresas sin funcionalidad dedicada para la gestión de almacenes, de modo que un trabajador de inventario pueda ver o imprimir simplemente la lista de picking del documento de ventas relacionado.</span><span class="sxs-lookup"><span data-stu-id="87acc-105">This report is typically used in companies without dedicated functionality for warehouse management, so that an inventory worker can simply view or print the picking list from the related sales document.</span></span> <span data-ttu-id="87acc-106">En empresas con un volumen más alto o procesos más complejos, el picking se planifica y se realiza en documentos de almacén dedicados.</span><span class="sxs-lookup"><span data-stu-id="87acc-106">In companies with higher volume or more complex processes, picking is planned and performed in dedicated warehouse documents.</span></span> <span data-ttu-id="87acc-107">Para obtener más información, consulte [Elegir productos](warehouse-pick-items.md).</span><span class="sxs-lookup"><span data-stu-id="87acc-107">For more information, see [Pick Items](warehouse-pick-items.md).</span></span>

## <a name="to-print-a-picking-list-from-a-sales-order"></a><span data-ttu-id="87acc-108">Para imprimir una lista de picking a partir de un pedido de venta</span><span class="sxs-lookup"><span data-stu-id="87acc-108">To print a picking list from a sales order</span></span>  
<span data-ttu-id="87acc-109">El procedimiento siguiente se basa en un pedido de venta.</span><span class="sxs-lookup"><span data-stu-id="87acc-109">The following procedure is based on a sales order.</span></span> <span data-ttu-id="87acc-110">Los pasos son similares para todos los documentos de ventas que se pueden usar para iniciar el envío de artículos.</span><span class="sxs-lookup"><span data-stu-id="87acc-110">The steps are similar for all sales documents that can be used to initiate shipment of items.</span></span>

1. <span data-ttu-id="87acc-111">Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "Icono Buscar página o informe"), introduzca **Pedidos de venta** y, a continuación, elija el vínculo relacionado.</span><span class="sxs-lookup"><span data-stu-id="87acc-111">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Sales Orders**, and then choose the related link.</span></span>  
2. <span data-ttu-id="87acc-112">Abra el pedido de venta para el que desea elegir productos.</span><span class="sxs-lookup"><span data-stu-id="87acc-112">Open the sales order that you want to pick items for.</span></span>  
3. <span data-ttu-id="87acc-113">Elija la acción **Informe** y luego elija la acción **Lista de selección por orden**.</span><span class="sxs-lookup"><span data-stu-id="87acc-113">Choose the **Report** action, and then choose the **Picking List by Order** action.</span></span>  
4. <span data-ttu-id="87acc-114">Seleccione el botón de **Imprimir** para imprimir la lista de picking o elija el botón de **Vista previa** para verlo en la pantalla.</span><span class="sxs-lookup"><span data-stu-id="87acc-114">Choose the **Print** button to print the picking list or choose the **Preview** button to view it on the screen.</span></span>

<span data-ttu-id="87acc-115">También puede guardar la lista de picking como un documento, por ejemplo, para enviarla a alguien o para agregarla como un archivo adjunto al pedido de ventas.</span><span class="sxs-lookup"><span data-stu-id="87acc-115">You can also save the picking list as a document, for example, to send to someone or to add as an attachment to the sales order.</span></span> <span data-ttu-id="87acc-116">Para obtener información, consulte [Administrar archivos adjuntos, vínculos y notas en fichas y documentos](ui-how-add-link-to-record.md).</span><span class="sxs-lookup"><span data-stu-id="87acc-116">For more information, see [Manage Attachments, Links, and Notes on Cards and Documents](ui-how-add-link-to-record.md).</span></span>

> [!NOTE]
> <span data-ttu-id="87acc-117">Si ha usado la función **Desplegar L.M.** en el pedido de venta, solo se muestran en el informe los componentes del elemento del ensamblado relacionado.</span><span class="sxs-lookup"><span data-stu-id="87acc-117">If you used the **Explode BOM** function on the sales order, then only the components of the related assembly item are shown in the report.</span></span> <span data-ttu-id="87acc-118">Para obtener más información, consulte [Trabajar con listas de materiales](inventory-how-work-BOMs.md).</span><span class="sxs-lookup"><span data-stu-id="87acc-118">For more information, see [Work with Bills of Material](inventory-how-work-BOMs.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="87acc-119">Consulte también</span><span class="sxs-lookup"><span data-stu-id="87acc-119">See Also</span></span>  
[<span data-ttu-id="87acc-120">Inventario</span><span class="sxs-lookup"><span data-stu-id="87acc-120">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="87acc-121">Elegir productos</span><span class="sxs-lookup"><span data-stu-id="87acc-121">Pick Items</span></span>](warehouse-pick-items.md)  
<span data-ttu-id="87acc-122">[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="87acc-122">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>   
