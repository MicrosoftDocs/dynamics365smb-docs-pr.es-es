---
title: Crear una ficha de proveedor para registrar un proveedor nuevo | Documentos de Microsoft
description: "Obtenga información sobre cómo crear una ficha de proveedor para registrar un nuevo proveedor."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: supplier
ms.date: 03/29/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 73d23013c97189caf5c75f561896b965dfb64837
ms.contentlocale: es-es
ms.lasthandoff: 01/30/2018

---
# <a name="register-new-vendors"></a><span data-ttu-id="85fc4-103">Permite registrar nuevos proveedores</span><span class="sxs-lookup"><span data-stu-id="85fc4-103">Register New Vendors</span></span>
<span data-ttu-id="85fc4-104">Los proveedores proporcionan los productos que vende.</span><span class="sxs-lookup"><span data-stu-id="85fc4-104">Vendors provide the products that you sell.</span></span> <span data-ttu-id="85fc4-105">Cada proveedor del que compra debe estar registrado como ficha de proveedor.</span><span class="sxs-lookup"><span data-stu-id="85fc4-105">Each vendor that you purchase from must be registered as a vendor card.</span></span>

<span data-ttu-id="85fc4-106">Antes de que pueda registrar nuevos proveedores, debe configurar varios códigos de compra que pueda seleccionar al rellenar fichas de proveedores.</span><span class="sxs-lookup"><span data-stu-id="85fc4-106">Before you can register new vendors, you must set up various purchase codes that you can select from when you fill vendor cards.</span></span> <span data-ttu-id="85fc4-107">Una vez creados todos los datos maestros necesarios, se puede efectuar una configuración adicional del proveedor, como priorizar el proveedor para fines de pago y crear una lista de productos que este y otros proveedores pueden suministrar.</span><span class="sxs-lookup"><span data-stu-id="85fc4-107">When all of the required master data is created, you can perform additional configuration of the vendor, such as prioritize the vendor for payment purposes and list items that the vendor and other vendors can supply.</span></span> <span data-ttu-id="85fc4-108">Otro grupo de tareas de configuración para proveedores es registrar los acuerdos relativos a descuentos, precios y métodos de pago.</span><span class="sxs-lookup"><span data-stu-id="85fc4-108">Another group of setup tasks for vendors is to record your agreements concerning discounts, prices, and payment methods.</span></span> <span data-ttu-id="85fc4-109">Para obtener más información, consulte [Configurar compras](purchasing-setup-purchasing.md).</span><span class="sxs-lookup"><span data-stu-id="85fc4-109">For more information, see [Setting Up Purchasing](purchasing-setup-purchasing.md).</span></span>

<span data-ttu-id="85fc4-110">Las fichas de proveedor contienen la información necesaria para comprar productos del proveedor.</span><span class="sxs-lookup"><span data-stu-id="85fc4-110">Vendor cards hold the information that is required to buy products from the vendor.</span></span> <span data-ttu-id="85fc4-111">Para obtener más información, vea [Registrar compras](purchasing-how-record-purchases.md) y [Registrar nuevos productos](inventory-how-register-new-items.md).</span><span class="sxs-lookup"><span data-stu-id="85fc4-111">For more information, see [Record Purchases](purchasing-how-record-purchases.md) and [Register New Items](inventory-how-register-new-items.md).</span></span>

> [!NOTE]  
>   <span data-ttu-id="85fc4-112">Si existen plantillas de proveedor para distintos tipos de proveedor, una ventana aparece cuando se crea una nueva ficha de proveedor en la que puede seleccionar una plantilla adecuada.</span><span class="sxs-lookup"><span data-stu-id="85fc4-112">If vendor templates exist for different vendor types, then a window appears when you create a new vendor card from where you can select an appropriate template.</span></span> <span data-ttu-id="85fc4-113">Si solo existe una plantilla de proveedor, las nuevas fichas de proveedor utilizan siempre esa plantilla.</span><span class="sxs-lookup"><span data-stu-id="85fc4-113">If only one vendor template exists, then new vendor cards always use that template.</span></span>

## <a name="to-create-a-new-vendor-card"></a><span data-ttu-id="85fc4-114">Para crear una nueva ficha de proveedor</span><span class="sxs-lookup"><span data-stu-id="85fc4-114">To create a new vendor card</span></span>
1. <span data-ttu-id="85fc4-115">En la página Inicio, seleccione **Proveedores** para abrir la lista de fichas de proveedores existentes.</span><span class="sxs-lookup"><span data-stu-id="85fc4-115">On the Home page, choose **Vendors** to open the list of existing vendors.</span></span>  
2. <span data-ttu-id="85fc4-116">En la ventana **Proveedores**, seleccione **Nuevo**.</span><span class="sxs-lookup"><span data-stu-id="85fc4-116">In the **Vendors** window, Choose **New**.</span></span>

    <span data-ttu-id="85fc4-117">Si existe más de una plantilla de proveedor, se abre una ventana desde la que puede seleccionar una plantilla de proveedor.</span><span class="sxs-lookup"><span data-stu-id="85fc4-117">If more than one vendor template exists, then a window opens from which you can select a vendor template.</span></span> <span data-ttu-id="85fc4-118">En ese caso, siga los dos pasos siguientes.</span><span class="sxs-lookup"><span data-stu-id="85fc4-118">In that case, follow the next two steps.</span></span>
3. <span data-ttu-id="85fc4-119">En la ventana **Seleccionar una plantilla para un proveedor nuevo**, seleccione la plantilla que quiere usar para la nueva ficha de proveedor.</span><span class="sxs-lookup"><span data-stu-id="85fc4-119">In the **Select a template for a new vendor** window, choose the template that you want to use for the new vendor card.</span></span>
4. <span data-ttu-id="85fc4-120">Elija el botón **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="85fc4-120">Choose the **OK** button.</span></span> <span data-ttu-id="85fc4-121">Una nueva ficha de proveedor se abre con algunos campos completados con la información de la plantilla.</span><span class="sxs-lookup"><span data-stu-id="85fc4-121">A new vendor card opens with some fields filled with information from the template.</span></span>
5. <span data-ttu-id="85fc4-122">Empiece a rellenar o cambiar campos en la ficha de proveedor, según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="85fc4-122">Proceed to fill or change fields on the vendor card as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!NOTE]  
>   <span data-ttu-id="85fc4-123">Si no conoce de antemano la dirección de facturación que se utilizará para todas las facturas de un proveedor, no rellene el campo **Pago a-Nº proveedor** de la ficha de proveedor.</span><span class="sxs-lookup"><span data-stu-id="85fc4-123">If you do not know the invoicing address that will be used for every invoice from a vendor, do not fill in the **Pay-to** field.</span></span> <span data-ttu-id="85fc4-124">En su lugar, elija el número del pago-a proveedor cuando haya configurado una oferta, pedido o encabezado de compra.</span><span class="sxs-lookup"><span data-stu-id="85fc4-124">Instead, choose the pay-to vendor number after you have set up a purchase quote, order, or invoice header.</span></span>

<span data-ttu-id="85fc4-125">El proveedor estará registrado y la ficha de proveedor está lista para usarse en los documentos de compra.</span><span class="sxs-lookup"><span data-stu-id="85fc4-125">The vendor is now registered, and the vendor card is ready to be used on purchase documents.</span></span>

<span data-ttu-id="85fc4-126">Si desea usar esta ficha de proveedor como plantilla cuando cree nuevas fichas de proveedor, puede guardarla.</span><span class="sxs-lookup"><span data-stu-id="85fc4-126">If you want to use this vendor card as a template when you create new vendor cards, you can save it as a vendor template.</span></span> <span data-ttu-id="85fc4-127">Para obtener más información, vea la siguiente sección:</span><span class="sxs-lookup"><span data-stu-id="85fc4-127">For more information, see the following section.</span></span>

## <a name="to-save-the-vendor-card-as-a-template"></a><span data-ttu-id="85fc4-128">Para guardar la ficha de proveedor como una plantilla</span><span class="sxs-lookup"><span data-stu-id="85fc4-128">To save the vendor card as a template</span></span>
1. <span data-ttu-id="85fc4-129">En la ventana **Ficha de proveedor**, seleccione la acción **Guardar como plantilla**.</span><span class="sxs-lookup"><span data-stu-id="85fc4-129">In the **Vendor Card** window, choose the **Save as Template** action.</span></span> <span data-ttu-id="85fc4-130">La ventana **Plantilla proveedor** se abre mostrando la ficha de proveedor como plantilla.</span><span class="sxs-lookup"><span data-stu-id="85fc4-130">The **Vendor Template** window opens showing the vendor card as a template.</span></span>
2. <span data-ttu-id="85fc4-131">Rellene los campos según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="85fc4-131">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. <span data-ttu-id="85fc4-132">Para volver a usar dimensiones en las plantillas, seleccione la acción **Dimensiones**.</span><span class="sxs-lookup"><span data-stu-id="85fc4-132">To reuse dimensions in templates, choose the **Dimensions** action.</span></span> <span data-ttu-id="85fc4-133">La ventana **Plantilla de dimensiones** se abre mostrando los códigos de dimensión configurados para el proveedor.</span><span class="sxs-lookup"><span data-stu-id="85fc4-133">The **Dimension Templates** window opens showing any dimension codes that are set up for the vendor.</span></span>
4. <span data-ttu-id="85fc4-134">Modifique o introduzca los códigos de dimensión que se aplicarán a nuevas fichas de proveedor creadas con la plantilla.</span><span class="sxs-lookup"><span data-stu-id="85fc4-134">Edit or enter dimension codes that will apply to new vendor cards created by using the template.</span></span>
5. <span data-ttu-id="85fc4-135">Cuando haya finalizado la nueva plantilla de proveedor, seleccione el botón de **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="85fc4-135">When you have completed the new vendor template, choose the **OK** button.</span></span>  
   <span data-ttu-id="85fc4-136">La plantilla de proveedor se agrega a la lista de plantillas de proveedor, de modo que puede usarla para crear nuevas fichas de proveedor.</span><span class="sxs-lookup"><span data-stu-id="85fc4-136">The vendor template is added to the list of vendor templates, so that you can use it to create new vendor cards.</span></span>

## <a name="see-also"></a><span data-ttu-id="85fc4-137">Consulte también</span><span class="sxs-lookup"><span data-stu-id="85fc4-137">See Also</span></span>
[<span data-ttu-id="85fc4-138">Compras</span><span class="sxs-lookup"><span data-stu-id="85fc4-138">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="85fc4-139">[Registrar compras](purchasing-how-record-purchases.md) </span><span class="sxs-lookup"><span data-stu-id="85fc4-139">[Record Purchases](purchasing-how-record-purchases.md) </span></span>  
<span data-ttu-id="85fc4-140">[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="85fc4-140">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

