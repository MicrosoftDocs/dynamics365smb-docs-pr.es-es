---
title: Crear una ficha de proveedor para registrar un proveedor nuevo | Documentos de Microsoft
description: Obtenga información sobre cómo crear una ficha de proveedor para registrar un nuevo proveedor.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: supplier
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: e77238b4e0578307a90f80bddfdec64002e7ac27
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/01/2020
ms.locfileid: "3926777"
---
# <a name="register-new-vendors"></a><span data-ttu-id="29d8d-103">Permite registrar nuevos proveedores</span><span class="sxs-lookup"><span data-stu-id="29d8d-103">Register New Vendors</span></span>

<span data-ttu-id="29d8d-104">Los proveedores proporcionan los productos que vende.</span><span class="sxs-lookup"><span data-stu-id="29d8d-104">Vendors provide the products that you sell.</span></span> <span data-ttu-id="29d8d-105">Cada proveedor del que compra debe estar registrado como ficha de proveedor.</span><span class="sxs-lookup"><span data-stu-id="29d8d-105">Each vendor that you purchase from must be registered as a vendor card.</span></span>

<span data-ttu-id="29d8d-106">Antes de que pueda registrar nuevos proveedores, debe configurar varios códigos de compra que pueda seleccionar al rellenar fichas de proveedores.</span><span class="sxs-lookup"><span data-stu-id="29d8d-106">Before you can register new vendors, you must set up various purchase codes that you can select from when you fill vendor cards.</span></span> <span data-ttu-id="29d8d-107">Una vez creados todos los datos maestros necesarios, se puede efectuar una configuración adicional del proveedor, como priorizar el proveedor para fines de pago y crear una lista de productos que este y otros proveedores pueden suministrar.</span><span class="sxs-lookup"><span data-stu-id="29d8d-107">When all of the required master data is created, you can perform additional configuration of the vendor, such as prioritize the vendor for payment purposes and list items that the vendor and other vendors can supply.</span></span> <span data-ttu-id="29d8d-108">Otro grupo de tareas de configuración para proveedores es registrar los acuerdos relativos a descuentos, precios y métodos de pago.</span><span class="sxs-lookup"><span data-stu-id="29d8d-108">Another group of setup tasks for vendors is to record your agreements concerning discounts, prices, and payment methods.</span></span> <span data-ttu-id="29d8d-109">Para obtener más información, consulte [Configurar compras](purchasing-setup-purchasing.md).</span><span class="sxs-lookup"><span data-stu-id="29d8d-109">For more information, see [Setting Up Purchasing](purchasing-setup-purchasing.md).</span></span>

<span data-ttu-id="29d8d-110">Las fichas de proveedor contienen la información necesaria para comprar productos del proveedor.</span><span class="sxs-lookup"><span data-stu-id="29d8d-110">Vendor cards hold the information that is required to buy products from the vendor.</span></span> <span data-ttu-id="29d8d-111">Para obtener más información, vea [Registrar compras](purchasing-how-record-purchases.md) y [Registrar nuevos productos](inventory-how-register-new-items.md).</span><span class="sxs-lookup"><span data-stu-id="29d8d-111">For more information, see [Record Purchases](purchasing-how-record-purchases.md) and [Register New Items](inventory-how-register-new-items.md).</span></span>

> [!NOTE]  
> <span data-ttu-id="29d8d-112">Si existen plantillas de proveedor para distintos tipos de proveedor, una página aparece cuando se crea una nueva ficha de proveedor en la que puede seleccionar una plantilla adecuada.</span><span class="sxs-lookup"><span data-stu-id="29d8d-112">If vendor templates exist for different vendor types, then a page appears when you create a new vendor card from where you can select an appropriate template.</span></span> <span data-ttu-id="29d8d-113">Si solo existe una plantilla de proveedor, las nuevas fichas de proveedor utilizan siempre esa plantilla.</span><span class="sxs-lookup"><span data-stu-id="29d8d-113">If only one vendor template exists, then new vendor cards always use that template.</span></span>
<br><br>  

> [!Video https://www.microsoft.com/videoplayer/embed/RE3PZtd?rel=0]

## <a name="to-create-a-new-vendor-card"></a><span data-ttu-id="29d8d-114">Para crear una nueva ficha de proveedor</span><span class="sxs-lookup"><span data-stu-id="29d8d-114">To create a new vendor card</span></span>

1. <span data-ttu-id="29d8d-115">Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Proveedores** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="29d8d-115">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Vendors**, and then choose the related link.</span></span>  
2. <span data-ttu-id="29d8d-116">En la página **Proveedores**, elija **Nuevo**.</span><span class="sxs-lookup"><span data-stu-id="29d8d-116">On the **Vendors** page, Choose **New**.</span></span>

    <span data-ttu-id="29d8d-117">Si existe más de una plantilla de proveedor, se abre una página desde la que puede seleccionar una plantilla de proveedor.</span><span class="sxs-lookup"><span data-stu-id="29d8d-117">If more than one vendor template exists, then a page opens from which you can select a vendor template.</span></span> <span data-ttu-id="29d8d-118">En ese caso, siga los dos pasos siguientes.</span><span class="sxs-lookup"><span data-stu-id="29d8d-118">In that case, follow the next two steps.</span></span>
3. <span data-ttu-id="29d8d-119">En la página **Seleccionar una plantilla para un proveedor nuevo**, seleccione la plantilla que quiere usar para la nueva ficha de proveedor.</span><span class="sxs-lookup"><span data-stu-id="29d8d-119">On the **Select a template for a new vendor** page, choose the template that you want to use for the new vendor card.</span></span>
4. <span data-ttu-id="29d8d-120">Elija el botón **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="29d8d-120">Choose the **OK** button.</span></span> <span data-ttu-id="29d8d-121">Una nueva ficha de proveedor se abre con algunos campos completados con la información de la plantilla.</span><span class="sxs-lookup"><span data-stu-id="29d8d-121">A new vendor card opens with some fields filled with information from the template.</span></span>
5. <span data-ttu-id="29d8d-122">Empiece a rellenar o cambiar campos en la ficha de proveedor, según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="29d8d-122">Proceed to fill or change fields on the vendor card as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!NOTE]  
> <span data-ttu-id="29d8d-123">Si no conoce de antemano la dirección de facturación que se utilizará para todas las facturas de un proveedor, no rellene el campo **Nº proveedor** de la ficha de proveedor.</span><span class="sxs-lookup"><span data-stu-id="29d8d-123">If you do not know the invoicing address that will be used for every invoice from a vendor, do not fill in the **Vendor No.** field.</span></span> <span data-ttu-id="29d8d-124">En su lugar, elija el número del pago-a proveedor cuando haya configurado una oferta, pedido o encabezado de compra.</span><span class="sxs-lookup"><span data-stu-id="29d8d-124">Instead, choose the pay-to vendor number after you have set up a purchase quote, order, or invoice header.</span></span>

<span data-ttu-id="29d8d-125">El proveedor estará registrado y la ficha de proveedor está lista para usarse en los documentos de compra.</span><span class="sxs-lookup"><span data-stu-id="29d8d-125">The vendor is now registered, and the vendor card is ready to be used on purchase documents.</span></span>

<span data-ttu-id="29d8d-126">Si desea usar esta ficha de proveedor como plantilla cuando cree nuevas fichas de proveedor, puede guardarla.</span><span class="sxs-lookup"><span data-stu-id="29d8d-126">If you want to use this vendor card as a template when you create new vendor cards, you can save it as a vendor template.</span></span> <span data-ttu-id="29d8d-127">Para obtener más información, vea la siguiente sección:</span><span class="sxs-lookup"><span data-stu-id="29d8d-127">For more information, see the following section.</span></span>

### <a name="deleting-vendor-cards"></a><span data-ttu-id="29d8d-128">Eliminar fichas de proveedores</span><span class="sxs-lookup"><span data-stu-id="29d8d-128">Deleting Vendor Cards</span></span>
<span data-ttu-id="29d8d-129">Si ha publicado una transacción para un proveedor, no puede eliminar la ficha porque los movimientos pueden ser necesarias para la auditoría.</span><span class="sxs-lookup"><span data-stu-id="29d8d-129">If you have posted a transaction for a vendor, you cannot delete the card because the ledger entries may be needed for auditing.</span></span> <span data-ttu-id="29d8d-130">Para eliminar fichas de proveedores con movimientos, póngase en contacto con el socio de Microsoft para hacerlo a través del código.</span><span class="sxs-lookup"><span data-stu-id="29d8d-130">To delete vendor cards with ledger entries, contact to Microsoft partner to do so through code.</span></span>

## <a name="to-save-the-vendor-card-as-a-template"></a><span data-ttu-id="29d8d-131">Para guardar la ficha de proveedor como una plantilla</span><span class="sxs-lookup"><span data-stu-id="29d8d-131">To save the vendor card as a template</span></span>
1. <span data-ttu-id="29d8d-132">En la página **Ficha proveedor**, seleccione la acción **Guardar como plantilla**.</span><span class="sxs-lookup"><span data-stu-id="29d8d-132">On the **Vendor Card** page, choose the **Save as Template** action.</span></span> <span data-ttu-id="29d8d-133">La página **Plantilla proveedor** se abre mostrando la ficha de proveedor como plantilla.</span><span class="sxs-lookup"><span data-stu-id="29d8d-133">The **Vendor Template** page opens showing the vendor card as a template.</span></span>
2. <span data-ttu-id="29d8d-134">Rellene los campos según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="29d8d-134">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. <span data-ttu-id="29d8d-135">Para volver a usar dimensiones en las plantillas, seleccione la acción **Dimensiones**.</span><span class="sxs-lookup"><span data-stu-id="29d8d-135">To reuse dimensions in templates, choose the **Dimensions** action.</span></span> <span data-ttu-id="29d8d-136">La página **Plantilla de dimensiones** se abre mostrando los códigos de dimensión configurados para el proveedor.</span><span class="sxs-lookup"><span data-stu-id="29d8d-136">The **Dimension Templates** page opens showing any dimension codes that are set up for the vendor.</span></span>
4. <span data-ttu-id="29d8d-137">Modifique o introduzca los códigos de dimensión que se aplicarán a nuevas fichas de proveedor creadas con la plantilla.</span><span class="sxs-lookup"><span data-stu-id="29d8d-137">Edit or enter dimension codes that will apply to new vendor cards created by using the template.</span></span>
5. <span data-ttu-id="29d8d-138">Cuando haya finalizado la nueva plantilla de proveedor, seleccione el botón de **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="29d8d-138">When you have completed the new vendor template, choose the **OK** button.</span></span>  
   <span data-ttu-id="29d8d-139">La plantilla de proveedor se agrega a la lista de plantillas de proveedor, de modo que puede usarla para crear nuevas fichas de proveedor.</span><span class="sxs-lookup"><span data-stu-id="29d8d-139">The vendor template is added to the list of vendor templates, so that you can use it to create new vendor cards.</span></span>

## <a name="see-also"></a><span data-ttu-id="29d8d-140">Consulte también</span><span class="sxs-lookup"><span data-stu-id="29d8d-140">See Also</span></span>
[<span data-ttu-id="29d8d-141">Combinar registros duplicados</span><span class="sxs-lookup"><span data-stu-id="29d8d-141">Merge Duplicate Records</span></span>](sales-how-merge-duplicate-records.md)  
[<span data-ttu-id="29d8d-142">Crear numeración</span><span class="sxs-lookup"><span data-stu-id="29d8d-142">Create Number Series</span></span>](ui-create-number-series.md)  
[<span data-ttu-id="29d8d-143">Compras</span><span class="sxs-lookup"><span data-stu-id="29d8d-143">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="29d8d-144">[Registrar compras](purchasing-how-record-purchases.md) </span><span class="sxs-lookup"><span data-stu-id="29d8d-144">[Record Purchases](purchasing-how-record-purchases.md) </span></span>  
<span data-ttu-id="29d8d-145">[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="29d8d-145">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
