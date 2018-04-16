---
title: "Configurar y usar líneas estándar para ventas y compras periódicas | Documentos de Microsoft"
description: "Puede configurar líneas de ventas y líneas de compras que realice con frecuencia e insertarlas en documentos de venta y compra para rellenar rápidamente las líneas con información estándar."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: trade, sell, replenishment
ms.date: 07/02/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: acef03f32124c5983846bc6ed0c4d332c9c8b347
ms.openlocfilehash: ecb4bdc57f538a17a0149513cef1be318d131a9b
ms.contentlocale: es-es
ms.lasthandoff: 04/16/2018

---
# <a name="create-recurring-sales-and-purchase-lines"></a><span data-ttu-id="c638c-103">Crear líneas de ventas y de compras periódicas</span><span class="sxs-lookup"><span data-stu-id="c638c-103">Create Recurring Sales and Purchase Lines</span></span>
<span data-ttu-id="c638c-104">Si suele necesitar crear líneas de ventas y de compras con información similar, puede configurar líneas estándar que puede insertar en documentos de ventas y compras periódicas, por ejemplo, para órdenes de reposición periódicas.</span><span class="sxs-lookup"><span data-stu-id="c638c-104">If you often need to create sales and purchase lines with similar information, you can set up standard lines that you can then insert on recurring sales and purchase documents, for example, for recurring replenishment orders.</span></span>  

<span data-ttu-id="c638c-105">El siguiente procedimiento muestra cómo trabajar con líneas de ventas estándar.</span><span class="sxs-lookup"><span data-stu-id="c638c-105">The following procedure shows how to work with standard sales lines.</span></span> <span data-ttu-id="c638c-106">Funciona de forma similar para las líneas de compras estándar.</span><span class="sxs-lookup"><span data-stu-id="c638c-106">It works in a similar way for standard purchase lines.</span></span>  

## <a name="to-set-up-standard-sales-lines"></a><span data-ttu-id="c638c-107">Para configurar las líneas de ventas estándar</span><span class="sxs-lookup"><span data-stu-id="c638c-107">To set up standard sales lines</span></span>  
1. <span data-ttu-id="c638c-108">Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Códigos de venta estándar** y, a continuación, seleccione el vínculo relacionado.</span><span class="sxs-lookup"><span data-stu-id="c638c-108">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Standard Sales Codes**, and then choose the related link.</span></span>  
2. <span data-ttu-id="c638c-109">En la ventana **Líneas ventas estándar**, elija la acción **Nuevo**.</span><span class="sxs-lookup"><span data-stu-id="c638c-109">In the **Standard Sales Lines** window, choose the **New** action.</span></span>  
3. <span data-ttu-id="c638c-110">En la ficha desplegable **General**, rellene los campos como sea necesario.</span><span class="sxs-lookup"><span data-stu-id="c638c-110">On the **General** FastTab, fill the fields as necessary.</span></span> [!INCLUDE [tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
4. <span data-ttu-id="c638c-111">En la ficha desplegable **Líneas**, introduzca la información en los campos para preparar líneas de ventas que reflejen las líneas estándar que desea utilizar como líneas recurrentes en los documentos de ventas.</span><span class="sxs-lookup"><span data-stu-id="c638c-111">On the **Lines** FastTab, enter information in the fields to prepare sales lines that reflect the standard lines that you expect to use as recurring lines on sales documents.</span></span>  

## <a name="to-insert-standard-sales-lines-on-a-sales-invoice"></a><span data-ttu-id="c638c-112">Para insertar líneas de ventas estándar en una factura de ventas</span><span class="sxs-lookup"><span data-stu-id="c638c-112">To insert standard sales lines on a sales invoice</span></span>
1. <span data-ttu-id="c638c-113">Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Facturas** y, a continuación, seleccione el vínculo relacionado.</span><span class="sxs-lookup"><span data-stu-id="c638c-113">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Invoices**, and then choose the related link.</span></span>
2. <span data-ttu-id="c638c-114">Abra la factura de ventas en la que desee insertar una o varias líneas de ventas estándar.</span><span class="sxs-lookup"><span data-stu-id="c638c-114">Open the sales invoice that you want to insert one or more standard sales lines on.</span></span>
3. <span data-ttu-id="c638c-115">Elija la acción **Obtener líneas de venta periódicas**.</span><span class="sxs-lookup"><span data-stu-id="c638c-115">Choose the **Get Recurring Sales Lines** action.</span></span>
4. <span data-ttu-id="c638c-116">En la ventana **Líneas de ventas periódicas**, elija el botón de búsqueda en el campo **Código** y seleccione un conjunto de líneas de ventas estándar.</span><span class="sxs-lookup"><span data-stu-id="c638c-116">In the **Recurring Sales Lines** window, choose the lookup button in the **Code** field, and then select a set of standard sales lines.</span></span>
5. <span data-ttu-id="c638c-117">Elija el botón **Acep.** para insertar las líneas de ventas estándar en la factura, donde puede reutilizar la información tal como está o editarla.</span><span class="sxs-lookup"><span data-stu-id="c638c-117">Choose the **OK** button to insert the standard sales lines on the invoice, where you can reuse as is or edit the information.</span></span>

## <a name="to-create-multiple-sales-invoices-based-on-standard-sales-lines"></a><span data-ttu-id="c638c-118">Para crear varias facturas de venta basadas en líneas de ventas estándar</span><span class="sxs-lookup"><span data-stu-id="c638c-118">To create multiple sales invoices based on standard sales lines</span></span>
<span data-ttu-id="c638c-119">Puede utilizar el trabajo por lotes **Crear facturas de venta periódicas** para crear facturas de venta según las líneas de venta estándar asignadas a los clientes y con fechas de registro dentro de las fechas de inicio y fin de validez que especifique en el código de ventas estándar.</span><span class="sxs-lookup"><span data-stu-id="c638c-119">You can use the **Create Recurring Sales Inv.** batch job to create sales invoices according to standard sales lines that are assigned to the customers and with posting dates within the valid-from and valid-to dates that you specify on the standard sales code.</span></span>

<span data-ttu-id="c638c-120">En la ventana **Líneas de ventas periódicas**, también puede especificar una forma de pago por adeudo directo y una orden de domiciliación de adeudo directo.</span><span class="sxs-lookup"><span data-stu-id="c638c-120">In the **Recurring Sales Lines** window, you can also specify a direct-debit payment method and a direct-debit mandate.</span></span> <span data-ttu-id="c638c-121">Las facturas de venta que se crean con el trabajo por lotes **Crear facturas de venta periódicas** incluirá la información necesaria para cobrar los pagos por adeudo directo SEPA para las facturas de venta.</span><span class="sxs-lookup"><span data-stu-id="c638c-121">The sales invoices that are created with the **Create Recurring Sales Inv.** batch job will then include information required to collect payment for the sales invoices with SEPA direct debit.</span></span> <span data-ttu-id="c638c-122">Para obtener más información, consulte [Cobro de pagos mediante adeudo directo SEPA](finance-collect-payments-with-sepa-direct-debit.md).</span><span class="sxs-lookup"><span data-stu-id="c638c-122">For more information, see [Collecting Payments with SEPA Direct Debit](finance-collect-payments-with-sepa-direct-debit.md).</span></span>

1. <span data-ttu-id="c638c-123">Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Crear facturas de venta periódicas** y, a continuación, seleccione el vínculo relacionado.</span><span class="sxs-lookup"><span data-stu-id="c638c-123">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Create Recurring Sales Invoices**, and then choose the related link.</span></span>
2. <span data-ttu-id="c638c-124">En la ventana **Crear facturas de venta periódicas**, rellene los campos necesarios.</span><span class="sxs-lookup"><span data-stu-id="c638c-124">In the **Create Recurring Sales Inv.** window, fill in the fields as necessary.</span></span>
3. <span data-ttu-id="c638c-125">En el campo **Código**, introduzca el código de las líneas de ventas asignadas a un cliente para el que desee crear las facturas de ventas.</span><span class="sxs-lookup"><span data-stu-id="c638c-125">In the **Code** field, enter the code for standard sales lines assigned to a customer that you want to create sales invoices for.</span></span>
4. <span data-ttu-id="c638c-126">Elija el botón **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="c638c-126">Choose the **OK** button.</span></span>

<span data-ttu-id="c638c-127">Las facturas de venta se crean para los clientes con el código de ventas de cliente estándar especificado y la información de domiciliación especificada, para el registro en la fecha especificada.</span><span class="sxs-lookup"><span data-stu-id="c638c-127">Sales invoices are created for the customers with the specified standard customer sales code, and any specified direct-debit information, for posting on the specified date.</span></span>

## <a name="see-also"></a><span data-ttu-id="c638c-128">Consulte también</span><span class="sxs-lookup"><span data-stu-id="c638c-128">See Also</span></span>  
[<span data-ttu-id="c638c-129">Ventas</span><span class="sxs-lookup"><span data-stu-id="c638c-129">Sales</span></span>](sales-manage-sales.md)  
<span data-ttu-id="c638c-130">[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="c638c-130">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

