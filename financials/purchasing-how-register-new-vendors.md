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
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 78710d796ed73d7b4c2505f6cbb8c7d5f41d7320
ms.contentlocale: es-es
ms.lasthandoff: 09/11/2017

---
# <a name="how-to-register-new-vendors"></a><span data-ttu-id="8885f-103">Registro de proveedores nuevos</span><span class="sxs-lookup"><span data-stu-id="8885f-103">How to: Register New Vendors</span></span>
<span data-ttu-id="8885f-104">Los proveedores proporcionan los productos que vende.</span><span class="sxs-lookup"><span data-stu-id="8885f-104">Vendors provide the products that you sell.</span></span> <span data-ttu-id="8885f-105">Cada proveedor del que compra debe estar registrado como ficha de proveedor.</span><span class="sxs-lookup"><span data-stu-id="8885f-105">Each vendor that you purchase from must be registered as a vendor card.</span></span>

<span data-ttu-id="8885f-106">Antes de que pueda registrar nuevos proveedores, debe configurar varios códigos de compra que pueda seleccionar al rellenar fichas de proveedores.</span><span class="sxs-lookup"><span data-stu-id="8885f-106">Before you can register new vendors, you must set up various purchase codes that you can select from when you fill vendor cards.</span></span> <span data-ttu-id="8885f-107">Una vez creados todos los datos maestros necesarios, se puede efectuar una configuración adicional del proveedor, como priorizar el proveedor para fines de pago y crear una lista de productos que este y otros proveedores pueden suministrar.</span><span class="sxs-lookup"><span data-stu-id="8885f-107">When all of the required master data is created, you can perform additional configuration of the vendor, such as prioritize the vendor for payment purposes and list items that the vendor and other vendors can supply.</span></span> <span data-ttu-id="8885f-108">Otro grupo de tareas de configuración para proveedores es registrar los acuerdos relativos a descuentos, precios y métodos de pago.</span><span class="sxs-lookup"><span data-stu-id="8885f-108">Another group of setup tasks for vendors is to record your agreements concerning discounts, prices, and payment methods.</span></span> <span data-ttu-id="8885f-109">Para obtener más información, consulte [Configurar compras](purchasing-setup-purchasing.md).</span><span class="sxs-lookup"><span data-stu-id="8885f-109">For more information, see [Setting Up Purchasing](purchasing-setup-purchasing.md).</span></span>

<span data-ttu-id="8885f-110">Las fichas de proveedor contienen la información necesaria para comprar productos del proveedor.</span><span class="sxs-lookup"><span data-stu-id="8885f-110">Vendor cards hold the information that is required to buy products from the vendor.</span></span> <span data-ttu-id="8885f-111">Para obtener más información, vea [Registrar compras](purchasing-how-record-purchases.md) y [Registrar nuevos productos](inventory-how-register-new-items.md).</span><span class="sxs-lookup"><span data-stu-id="8885f-111">For more information, see [How to: Record Purchases](purchasing-how-record-purchases.md) and [How to: Register New Items](inventory-how-register-new-items.md).</span></span>

> [!NOTE]  
>   <span data-ttu-id="8885f-112">Si existen plantillas de proveedor para distintos tipos de proveedor, una ventana aparece cuando se crea una nueva ficha de proveedor en la que puede seleccionar una plantilla adecuada.</span><span class="sxs-lookup"><span data-stu-id="8885f-112">If vendor templates exist for different vendor types, then a window appears when you create a new vendor card from where you can select an appropriate template.</span></span> <span data-ttu-id="8885f-113">Si solo existe una plantilla de proveedor, las nuevas fichas de proveedor utilizan siempre esa plantilla.</span><span class="sxs-lookup"><span data-stu-id="8885f-113">If only one vendor template exists, then new vendor cards always use that template.</span></span>

## <a name="to-create-a-new-vendor-card"></a><span data-ttu-id="8885f-114">Para crear una nueva ficha de proveedor</span><span class="sxs-lookup"><span data-stu-id="8885f-114">To create a new vendor card</span></span>
1. <span data-ttu-id="8885f-115">En la página Inicio, seleccione **Proveedores** para abrir la lista de fichas de proveedores existentes.</span><span class="sxs-lookup"><span data-stu-id="8885f-115">On the Home page, choose **Vendors** to open the list of existing vendors.</span></span>  
2. <span data-ttu-id="8885f-116">En la ventana **Proveedores**, seleccione **Nuevo**.</span><span class="sxs-lookup"><span data-stu-id="8885f-116">In the **Vendors** window, Choose **New**.</span></span>

    <span data-ttu-id="8885f-117">Si existe más de una plantilla de proveedor, se abre una ventana desde la que puede seleccionar una plantilla de proveedor.</span><span class="sxs-lookup"><span data-stu-id="8885f-117">If more than one vendor template exists, then a window opens from which you can select a vendor template.</span></span> <span data-ttu-id="8885f-118">En ese caso, siga los dos pasos siguientes.</span><span class="sxs-lookup"><span data-stu-id="8885f-118">In that case, follow the next two steps.</span></span>
3. <span data-ttu-id="8885f-119">En la ventana **Seleccionar una plantilla para un proveedor nuevo**, seleccione la plantilla que quiere usar para la nueva ficha de proveedor.</span><span class="sxs-lookup"><span data-stu-id="8885f-119">In the **Select a template for a new vendor** window, choose the template that you want to use for the new vendor card.</span></span>
4. <span data-ttu-id="8885f-120">Elija el botón **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="8885f-120">Choose the **OK** button.</span></span> <span data-ttu-id="8885f-121">Una nueva ficha de proveedor se abre con algunos campos completados con la información de la plantilla.</span><span class="sxs-lookup"><span data-stu-id="8885f-121">A new vendor card opens with some fields filled with information from the template.</span></span>
5. <span data-ttu-id="8885f-122">Empiece a rellenar o cambiar campos en la ficha de proveedor, según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="8885f-122">Proceed to fill or change fields on the vendor card as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

<span data-ttu-id="8885f-123">El proveedor estará registrado y la ficha de proveedor está lista para usarse en los documentos de compra.</span><span class="sxs-lookup"><span data-stu-id="8885f-123">The vendor is now registered, and the vendor card is ready to be used on purchase documents.</span></span>

<span data-ttu-id="8885f-124">Si desea usar esta ficha de proveedor como plantilla cuando cree nuevas fichas de proveedor, puede guardarla.</span><span class="sxs-lookup"><span data-stu-id="8885f-124">If you want to use this vendor card as a template when you create new vendor cards, you can save it as a vendor template.</span></span> <span data-ttu-id="8885f-125">Para obtener más información, vea la siguiente sección:</span><span class="sxs-lookup"><span data-stu-id="8885f-125">For more information, see the following section.</span></span>

## <a name="to-save-the-vendor-card-as-a-template"></a><span data-ttu-id="8885f-126">Para guardar la ficha de proveedor como una plantilla</span><span class="sxs-lookup"><span data-stu-id="8885f-126">To save the vendor card as a template</span></span>
1. <span data-ttu-id="8885f-127">En la ventana **Ficha de proveedor**, seleccione la acción **Guardar como plantilla**.</span><span class="sxs-lookup"><span data-stu-id="8885f-127">In the **Vendor Card** window, choose the **Save as Template** action.</span></span> <span data-ttu-id="8885f-128">La ventana **Plantilla proveedor** se abre mostrando la ficha de proveedor como plantilla.</span><span class="sxs-lookup"><span data-stu-id="8885f-128">The **Vendor Template** window opens showing the vendor card as a template.</span></span>
2. <span data-ttu-id="8885f-129">Rellene los campos según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="8885f-129">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. <span data-ttu-id="8885f-130">Para volver a usar dimensiones en las plantillas, seleccione la acción **Dimensiones**.</span><span class="sxs-lookup"><span data-stu-id="8885f-130">To reuse dimensions in templates, choose the **Dimensions** action.</span></span> <span data-ttu-id="8885f-131">La ventana **Plantilla de dimensiones** se abre mostrando los códigos de dimensión configurados para el proveedor.</span><span class="sxs-lookup"><span data-stu-id="8885f-131">The **Dimension Templates** window opens showing any dimension codes that are set up for the vendor.</span></span>
4. <span data-ttu-id="8885f-132">Modifique o introduzca los códigos de dimensión que se aplicarán a nuevas fichas de proveedor creadas con la plantilla.</span><span class="sxs-lookup"><span data-stu-id="8885f-132">Edit or enter dimension codes that will apply to new vendor cards created by using the template.</span></span>
5. <span data-ttu-id="8885f-133">Cuando haya finalizado la nueva plantilla de proveedor, seleccione el botón de **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="8885f-133">When you have completed the new vendor template, choose the **OK** button.</span></span>  
   <span data-ttu-id="8885f-134">La plantilla de proveedor se agrega a la lista de plantillas de proveedor, de modo que puede usarla para crear nuevas fichas de proveedor.</span><span class="sxs-lookup"><span data-stu-id="8885f-134">The vendor template is added to the list of vendor templates, so that you can use it to create new vendor cards.</span></span>

## <a name="see-also"></a><span data-ttu-id="8885f-135">Consulte también</span><span class="sxs-lookup"><span data-stu-id="8885f-135">See Also</span></span>
[<span data-ttu-id="8885f-136">Compras</span><span class="sxs-lookup"><span data-stu-id="8885f-136">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="8885f-137">[Registro de compras](purchasing-how-record-purchases.md) </span><span class="sxs-lookup"><span data-stu-id="8885f-137">[How to: Record Purchases](purchasing-how-record-purchases.md) </span></span>  
<span data-ttu-id="8885f-138">[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="8885f-138">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

