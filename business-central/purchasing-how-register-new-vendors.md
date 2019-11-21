---
title: Crear una ficha de proveedor para registrar un proveedor nuevo | Documentos de Microsoft
description: Obtenga información sobre cómo crear una ficha de proveedor para registrar un nuevo proveedor.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: supplier
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 7e8306ad65b41784e853dfc46a41c2deee997180
ms.sourcegitcommit: ab4141739a53ec100d42773f0da863fbeefa384f
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/14/2019
ms.locfileid: "2577236"
---
# <a name="register-new-vendors"></a><span data-ttu-id="390e7-103">Permite registrar nuevos proveedores</span><span class="sxs-lookup"><span data-stu-id="390e7-103">Register New Vendors</span></span>
<span data-ttu-id="390e7-104">Los proveedores proporcionan los productos que vende.</span><span class="sxs-lookup"><span data-stu-id="390e7-104">Vendors provide the products that you sell.</span></span> <span data-ttu-id="390e7-105">Cada proveedor del que compra debe estar registrado como ficha de proveedor.</span><span class="sxs-lookup"><span data-stu-id="390e7-105">Each vendor that you purchase from must be registered as a vendor card.</span></span>

<span data-ttu-id="390e7-106">Antes de que pueda registrar nuevos proveedores, debe configurar varios códigos de compra que pueda seleccionar al rellenar fichas de proveedores.</span><span class="sxs-lookup"><span data-stu-id="390e7-106">Before you can register new vendors, you must set up various purchase codes that you can select from when you fill vendor cards.</span></span> <span data-ttu-id="390e7-107">Una vez creados todos los datos maestros necesarios, se puede efectuar una configuración adicional del proveedor, como priorizar el proveedor para fines de pago y crear una lista de productos que este y otros proveedores pueden suministrar.</span><span class="sxs-lookup"><span data-stu-id="390e7-107">When all of the required master data is created, you can perform additional configuration of the vendor, such as prioritize the vendor for payment purposes and list items that the vendor and other vendors can supply.</span></span> <span data-ttu-id="390e7-108">Otro grupo de tareas de configuración para proveedores es registrar los acuerdos relativos a descuentos, precios y métodos de pago.</span><span class="sxs-lookup"><span data-stu-id="390e7-108">Another group of setup tasks for vendors is to record your agreements concerning discounts, prices, and payment methods.</span></span> <span data-ttu-id="390e7-109">Para obtener más información, consulte [Configurar compras](purchasing-setup-purchasing.md).</span><span class="sxs-lookup"><span data-stu-id="390e7-109">For more information, see [Setting Up Purchasing](purchasing-setup-purchasing.md).</span></span>

<span data-ttu-id="390e7-110">Las fichas de proveedor contienen la información necesaria para comprar productos del proveedor.</span><span class="sxs-lookup"><span data-stu-id="390e7-110">Vendor cards hold the information that is required to buy products from the vendor.</span></span> <span data-ttu-id="390e7-111">Para obtener más información, vea [Registrar compras](purchasing-how-record-purchases.md) y [Registrar nuevos productos](inventory-how-register-new-items.md).</span><span class="sxs-lookup"><span data-stu-id="390e7-111">For more information, see [Record Purchases](purchasing-how-record-purchases.md) and [Register New Items](inventory-how-register-new-items.md).</span></span>

> [!NOTE]  
>   <span data-ttu-id="390e7-112">Si existen plantillas de proveedor para distintos tipos de proveedor, una página aparece cuando se crea una nueva ficha de proveedor en la que puede seleccionar una plantilla adecuada.</span><span class="sxs-lookup"><span data-stu-id="390e7-112">If vendor templates exist for different vendor types, then a page appears when you create a new vendor card from where you can select an appropriate template.</span></span> <span data-ttu-id="390e7-113">Si solo existe una plantilla de proveedor, las nuevas fichas de proveedor utilizan siempre esa plantilla.</span><span class="sxs-lookup"><span data-stu-id="390e7-113">If only one vendor template exists, then new vendor cards always use that template.</span></span>
<br><br>
> [!Video https://www.microsoft.com/en-us/videoplayer/embed/RE3PZtd]

## <a name="to-create-a-new-vendor-card"></a><span data-ttu-id="390e7-114">Para crear una nueva ficha de proveedor</span><span class="sxs-lookup"><span data-stu-id="390e7-114">To create a new vendor card</span></span>
1. <span data-ttu-id="390e7-115">Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Proveedores** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="390e7-115">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Vendors**, and then choose the related link.</span></span>  
2. <span data-ttu-id="390e7-116">En la página **Proveedores**, elija **Nuevo**.</span><span class="sxs-lookup"><span data-stu-id="390e7-116">On the **Vendors** page, Choose **New**.</span></span>

    <span data-ttu-id="390e7-117">Si existe más de una plantilla de proveedor, se abre una página desde la que puede seleccionar una plantilla de proveedor.</span><span class="sxs-lookup"><span data-stu-id="390e7-117">If more than one vendor template exists, then a page opens from which you can select a vendor template.</span></span> <span data-ttu-id="390e7-118">En ese caso, siga los dos pasos siguientes.</span><span class="sxs-lookup"><span data-stu-id="390e7-118">In that case, follow the next two steps.</span></span>
3. <span data-ttu-id="390e7-119">En la página **Seleccionar una plantilla para un proveedor nuevo**, seleccione la plantilla que quiere usar para la nueva ficha de proveedor.</span><span class="sxs-lookup"><span data-stu-id="390e7-119">On the **Select a template for a new vendor** page, choose the template that you want to use for the new vendor card.</span></span>
4. <span data-ttu-id="390e7-120">Elija el botón **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="390e7-120">Choose the **OK** button.</span></span> <span data-ttu-id="390e7-121">Una nueva ficha de proveedor se abre con algunos campos completados con la información de la plantilla.</span><span class="sxs-lookup"><span data-stu-id="390e7-121">A new vendor card opens with some fields filled with information from the template.</span></span>
5. <span data-ttu-id="390e7-122">Empiece a rellenar o cambiar campos en la ficha de proveedor, según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="390e7-122">Proceed to fill or change fields on the vendor card as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!NOTE]  
>   <span data-ttu-id="390e7-123">Si no conoce de antemano la dirección de facturación que se utilizará para todas las facturas de un proveedor, no rellene el campo **Pago a-Nº proveedor** de la ficha de proveedor.</span><span class="sxs-lookup"><span data-stu-id="390e7-123">If you do not know the invoicing address that will be used for every invoice from a vendor, do not fill in the **Pay-to** field.</span></span> <span data-ttu-id="390e7-124">En su lugar, elija el número del pago-a proveedor cuando haya configurado una oferta, pedido o encabezado de compra.</span><span class="sxs-lookup"><span data-stu-id="390e7-124">Instead, choose the pay-to vendor number after you have set up a purchase quote, order, or invoice header.</span></span>

<span data-ttu-id="390e7-125">El proveedor estará registrado y la ficha de proveedor está lista para usarse en los documentos de compra.</span><span class="sxs-lookup"><span data-stu-id="390e7-125">The vendor is now registered, and the vendor card is ready to be used on purchase documents.</span></span>

<span data-ttu-id="390e7-126">Si desea usar esta ficha de proveedor como plantilla cuando cree nuevas fichas de proveedor, puede guardarla.</span><span class="sxs-lookup"><span data-stu-id="390e7-126">If you want to use this vendor card as a template when you create new vendor cards, you can save it as a vendor template.</span></span> <span data-ttu-id="390e7-127">Para obtener más información, vea la siguiente sección:</span><span class="sxs-lookup"><span data-stu-id="390e7-127">For more information, see the following section.</span></span>

## <a name="to-save-the-vendor-card-as-a-template"></a><span data-ttu-id="390e7-128">Para guardar la ficha de proveedor como una plantilla</span><span class="sxs-lookup"><span data-stu-id="390e7-128">To save the vendor card as a template</span></span>
1. <span data-ttu-id="390e7-129">En la página **Ficha proveedor**, seleccione la acción **Guardar como plantilla**.</span><span class="sxs-lookup"><span data-stu-id="390e7-129">On the **Vendor Card** page, choose the **Save as Template** action.</span></span> <span data-ttu-id="390e7-130">La página **Plantilla proveedor** se abre mostrando la ficha de proveedor como plantilla.</span><span class="sxs-lookup"><span data-stu-id="390e7-130">The **Vendor Template** page opens showing the vendor card as a template.</span></span>
2. <span data-ttu-id="390e7-131">Rellene los campos según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="390e7-131">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. <span data-ttu-id="390e7-132">Para volver a usar dimensiones en las plantillas, seleccione la acción **Dimensiones**.</span><span class="sxs-lookup"><span data-stu-id="390e7-132">To reuse dimensions in templates, choose the **Dimensions** action.</span></span> <span data-ttu-id="390e7-133">La página **Plantilla de dimensiones** se abre mostrando los códigos de dimensión configurados para el proveedor.</span><span class="sxs-lookup"><span data-stu-id="390e7-133">The **Dimension Templates** page opens showing any dimension codes that are set up for the vendor.</span></span>
4. <span data-ttu-id="390e7-134">Modifique o introduzca los códigos de dimensión que se aplicarán a nuevas fichas de proveedor creadas con la plantilla.</span><span class="sxs-lookup"><span data-stu-id="390e7-134">Edit or enter dimension codes that will apply to new vendor cards created by using the template.</span></span>
5. <span data-ttu-id="390e7-135">Cuando haya finalizado la nueva plantilla de proveedor, seleccione el botón de **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="390e7-135">When you have completed the new vendor template, choose the **OK** button.</span></span>  
   <span data-ttu-id="390e7-136">La plantilla de proveedor se agrega a la lista de plantillas de proveedor, de modo que puede usarla para crear nuevas fichas de proveedor.</span><span class="sxs-lookup"><span data-stu-id="390e7-136">The vendor template is added to the list of vendor templates, so that you can use it to create new vendor cards.</span></span>

## <a name="see-also"></a><span data-ttu-id="390e7-137">Consulte también</span><span class="sxs-lookup"><span data-stu-id="390e7-137">See Also</span></span>
[<span data-ttu-id="390e7-138">Combinar registros duplicados</span><span class="sxs-lookup"><span data-stu-id="390e7-138">Merge Duplicate Records</span></span>](sales-how-merge-duplicate-records.md)  
[<span data-ttu-id="390e7-139">Crear numeración</span><span class="sxs-lookup"><span data-stu-id="390e7-139">Create Number Series</span></span>](ui-create-number-series.md)  
[<span data-ttu-id="390e7-140">Compras</span><span class="sxs-lookup"><span data-stu-id="390e7-140">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="390e7-141">[Registrar compras](purchasing-how-record-purchases.md) </span><span class="sxs-lookup"><span data-stu-id="390e7-141">[Record Purchases](purchasing-how-record-purchases.md) </span></span>  
<span data-ttu-id="390e7-142">[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="390e7-142">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
