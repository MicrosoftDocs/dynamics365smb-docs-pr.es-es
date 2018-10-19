---
title: "Configurar líneas estándar para ventas y compras periódicas | Documentos de Microsoft"
description: "Puede configurar líneas de ventas y líneas de compras que realice con frecuencia e insertarlas en documentos de venta y compra para rellenar rápidamente las líneas con información estándar."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: trade, sell, replenishment
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: df4f093ded0a55d45c40be15c5888035d6e3b2df
ms.contentlocale: es-es
ms.lasthandoff: 09/28/2018

---
# <a name="create-recurring-sales-and-purchase-lines"></a><span data-ttu-id="335a4-103">Crear líneas de ventas y de compras periódicas</span><span class="sxs-lookup"><span data-stu-id="335a4-103">Create Recurring Sales and Purchase Lines</span></span>
<span data-ttu-id="335a4-104">Si suele necesitar crear líneas de ventas y de compras con información similar, puede configurar líneas estándar que puede insertar en documentos de ventas y compras periódicas, por ejemplo, para órdenes de reposición periódicas.</span><span class="sxs-lookup"><span data-stu-id="335a4-104">If you often need to create sales and purchase lines with similar information, you can set up standard lines that you can then insert on recurring sales and purchase documents, for example, for recurring replenishment orders.</span></span>  

<span data-ttu-id="335a4-105">El siguiente procedimiento muestra cómo trabajar con líneas de ventas estándar.</span><span class="sxs-lookup"><span data-stu-id="335a4-105">The following procedure shows how to work with standard sales lines.</span></span> <span data-ttu-id="335a4-106">Funciona de forma similar para las líneas de compras estándar.</span><span class="sxs-lookup"><span data-stu-id="335a4-106">It works in a similar way for standard purchase lines.</span></span>  

## <a name="to-set-up-standard-sales-lines"></a><span data-ttu-id="335a4-107">Para configurar las líneas de ventas estándar</span><span class="sxs-lookup"><span data-stu-id="335a4-107">To set up standard sales lines</span></span>  
1. <span data-ttu-id="335a4-108">Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Líneas ventas estándar** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="335a4-108">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Standard Sales Lines**, and then choose the related link.</span></span>  
2. <span data-ttu-id="335a4-109">En la ventana **Líneas ventas estándar**, elija la acción **Nuevo**.</span><span class="sxs-lookup"><span data-stu-id="335a4-109">In the **Standard Sales Lines** window, choose the **New** action.</span></span>  
3. <span data-ttu-id="335a4-110">En la ficha desplegable **General**, rellene los campos como sea necesario.</span><span class="sxs-lookup"><span data-stu-id="335a4-110">On the **General** FastTab, fill the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
4. <span data-ttu-id="335a4-111">En la ficha desplegable **Líneas**, introduzca la información en los campos para preparar líneas de ventas que reflejen las líneas estándar que desea utilizar como líneas recurrentes en los documentos de ventas.</span><span class="sxs-lookup"><span data-stu-id="335a4-111">On the **Lines** FastTab, enter information in the fields to prepare sales lines that reflect the standard lines that you expect to use as recurring lines on sales documents.</span></span>  

## <a name="to-insert-standard-sales-lines-on-a-sales-invoice"></a><span data-ttu-id="335a4-112">Para insertar líneas de ventas estándar en una factura de ventas</span><span class="sxs-lookup"><span data-stu-id="335a4-112">To insert standard sales lines on a sales invoice</span></span>
1. <span data-ttu-id="335a4-113">Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Facturas** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="335a4-113">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Invoices**, and then choose the related link.</span></span>
2. <span data-ttu-id="335a4-114">Abra la factura de ventas en la que desee insertar una o varias líneas de ventas estándar.</span><span class="sxs-lookup"><span data-stu-id="335a4-114">Open the sales invoice that you want to insert one or more standard sales lines on.</span></span>
3. <span data-ttu-id="335a4-115">Elija la acción **Obtener líneas de venta periódicas**.</span><span class="sxs-lookup"><span data-stu-id="335a4-115">Choose the **Get Recurring Sales Lines** action.</span></span>
4. <span data-ttu-id="335a4-116">En la ventana **Líneas de ventas periódicas**, elija el botón de búsqueda en el campo **Código** y seleccione un conjunto de líneas de ventas estándar.</span><span class="sxs-lookup"><span data-stu-id="335a4-116">In the **Recurring Sales Lines** window, choose the lookup button in the **Code** field, and then select a set of standard sales lines.</span></span>

    > [!NOTE]
    > <span data-ttu-id="335a4-117">Para usar las líneas de ventas recurrentes establecidas junto con el trabajo por lotes **Crear facturas de ventas periódicas**, también debe completar los campos **Válido desde la fecha** y **Válido hasta la fecha** en la ventana **Líneas de ventas recurrentes**.</span><span class="sxs-lookup"><span data-stu-id="335a4-117">To use the recurring sales lines set together with the **Create Recurring Sales Invoices** batch job, you must also fill in the **Valid From Date** and **Valid To Date** fields in the **Recurring Sales Lines** window.</span></span> <span data-ttu-id="335a4-118">Para obtener más información, consulte la sección "Para crear varias facturas de venta basadas en líneas de ventas estándar".</span><span class="sxs-lookup"><span data-stu-id="335a4-118">For more information, see the "To create multiple sales invoices based on standard sales lines" section.</span></span>

5. <span data-ttu-id="335a4-119">Elija el botón **Aceptar** para insertar las líneas de ventas estándar en la factura, donde puede reutilizar la información tal como está o editarla.</span><span class="sxs-lookup"><span data-stu-id="335a4-119">Choose the **OK** button to insert the standard sales lines on the invoice where you can reuse them as is or edit the information.</span></span>

## <a name="to-create-multiple-sales-invoices-based-on-standard-sales-lines"></a><span data-ttu-id="335a4-120">Para crear varias facturas de venta basadas en líneas de ventas estándar</span><span class="sxs-lookup"><span data-stu-id="335a4-120">To create multiple sales invoices based on standard sales lines</span></span>
<span data-ttu-id="335a4-121">Puede utilizar el trabajo por lotes **Crear facturas de venta periódicas** para crear facturas de venta según las líneas de venta estándar asignadas a los clientes y con fechas de registro dentro de las fechas de inicio y fin de validez que especifique en las líneas de ventas estándar.</span><span class="sxs-lookup"><span data-stu-id="335a4-121">You can use the **Create Recurring Sales Invoices** batch job to create sales invoices according to standard sales lines that are assigned to the customers and with posting dates within the valid-from and valid-to dates that you specify on the standard sales lines.</span></span>

> [!NOTE]
> <span data-ttu-id="335a4-122">En la ventana **Líneas de ventas periódicas**, también puede especificar una forma de pago por adeudo directo y una orden de domiciliación de adeudo directo.</span><span class="sxs-lookup"><span data-stu-id="335a4-122">In the **Recurring Sales Lines** window, you can also specify a direct-debit payment method and a direct-debit mandate.</span></span> <span data-ttu-id="335a4-123">Las facturas de venta que se crean con el trabajo por lotes **Crear facturas de venta periódicas** incluirá la información necesaria para cobrar los pagos por adeudo directo SEPA para las facturas de venta.</span><span class="sxs-lookup"><span data-stu-id="335a4-123">The sales invoices that are created with the **Create Recurring Sales Inv.** batch job will then include information required to collect payment for the sales invoices with SEPA direct debit.</span></span> <span data-ttu-id="335a4-124">Para obtener más información, consulte [Cobro de pagos mediante adeudo directo SEPA](finance-collect-payments-with-sepa-direct-debit.md).</span><span class="sxs-lookup"><span data-stu-id="335a4-124">For more information, see [Collecting Payments with SEPA Direct Debit](finance-collect-payments-with-sepa-direct-debit.md).</span></span>

1. <span data-ttu-id="335a4-125">Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Crear facturas de venta periódicas** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="335a4-125">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Create Recurring Sales Invoices**, and then choose the related link.</span></span>
2. <span data-ttu-id="335a4-126">En la ventana **Crear facturas de venta periódicas**, rellene los campos necesarios.</span><span class="sxs-lookup"><span data-stu-id="335a4-126">In the **Create Recurring Sales Invoices** window, fill in the fields as necessary.</span></span>
3. <span data-ttu-id="335a4-127">En el campo de filtro **Código**, introduzca el código de las líneas de ventas asignadas a un cliente para el que desee crear las facturas de ventas.</span><span class="sxs-lookup"><span data-stu-id="335a4-127">In the **Code** filter field, enter the code for standard sales lines that are assigned to a customer that you want to create sales invoices for.</span></span>
4. <span data-ttu-id="335a4-128">Elija el botón **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="335a4-128">Choose the **OK** button.</span></span>

<span data-ttu-id="335a4-129">Las facturas de venta se crean para los clientes con el código de ventas de cliente estándar especificado y la información de domiciliación especificada, para el registro en la fecha especificada.</span><span class="sxs-lookup"><span data-stu-id="335a4-129">Sales invoices are created for the customers with the specified standard customer sales code, and any specified direct-debit information, for posting on the specified date.</span></span>

## <a name="see-also"></a><span data-ttu-id="335a4-130">Consulte también</span><span class="sxs-lookup"><span data-stu-id="335a4-130">See Also</span></span>  
[<span data-ttu-id="335a4-131">Ventas</span><span class="sxs-lookup"><span data-stu-id="335a4-131">Sales</span></span>](sales-manage-sales.md)  
<span data-ttu-id="335a4-132">[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="335a4-132">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

