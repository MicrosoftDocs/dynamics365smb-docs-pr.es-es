---
title: Configuración de días de pago y de periodos no-pago
description: Los días de pago y periodos no-pago se utilizan para calcular fechas de vencimiento. El cálculo de fecha de vencimiento se utiliza para los documentos de compras y ventas.
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
ms.openlocfilehash: 3f39de8a04461adf83660ff8e7d724f155a31a76
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 03/08/2019
ms.locfileid: "827159"
---
# <a name="set-up-payment-days-and-non-payment-periods"></a><span data-ttu-id="a8791-104">Configurar días de pago y de periodos no-pago</span><span class="sxs-lookup"><span data-stu-id="a8791-104">Set Up Payment Days and Non-Payment Periods</span></span>
<span data-ttu-id="a8791-105">Los días de pago y periodos no-pago se utilizan para calcular fechas de vencimiento.</span><span class="sxs-lookup"><span data-stu-id="a8791-105">Payment days and non-payment periods are used to calculate due dates.</span></span> <span data-ttu-id="a8791-106">El cálculo de fecha de vencimiento se utiliza para los documentos de compras y ventas.</span><span class="sxs-lookup"><span data-stu-id="a8791-106">Due date calculation is used for sales and purchase documents.</span></span>  

<span data-ttu-id="a8791-107">Un día de pago es un día en el que se pagan facturas.</span><span class="sxs-lookup"><span data-stu-id="a8791-107">A payment day is a day on which invoices are paid.</span></span>  

<span data-ttu-id="a8791-108">Un periodo no-pago es un intervalo de fechas durante el cual la empresa no realiza pagos.</span><span class="sxs-lookup"><span data-stu-id="a8791-108">A non-payment period is a range of dates during which the company does not make payments.</span></span> <span data-ttu-id="a8791-109">Esta funcionalidad se utiliza con frecuencia para los periodos de vacaciones.</span><span class="sxs-lookup"><span data-stu-id="a8791-109">This functionality is often used for holiday periods.</span></span>  

<span data-ttu-id="a8791-110">Para facturas de compras y ventas, se tienen en cuenta los días de pago y los periodos no-pago del cliente y el proveedor.</span><span class="sxs-lookup"><span data-stu-id="a8791-110">For sales and purchase invoices, the customer and vendor payment days and non-payment periods are taken into account.</span></span>  

## <a name="to-set-up-payment-days-and-non-payment-periods-for-a-company"></a><span data-ttu-id="a8791-111">Para configurar días de pago y periodos no-pago para una empresa</span><span class="sxs-lookup"><span data-stu-id="a8791-111">To set up payment days and non-payment periods for a company</span></span>  

1.  <span data-ttu-id="a8791-112">Seleccione el icono ![Buscar página o informe](../../media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Información de la empresa** y, a continuación, seleccione el vínculo relacionado.</span><span class="sxs-lookup"><span data-stu-id="a8791-112">Choose the ![Search for Page or Report](../../media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Company Information**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="a8791-113">Amplíe la ficha desplegable **Pagos**.</span><span class="sxs-lookup"><span data-stu-id="a8791-113">Expand the **Payments** FastTab.</span></span>  
3.  <span data-ttu-id="a8791-114">Rellene los campos tal como se describe en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="a8791-114">Fill in the fields as described in the following table.</span></span>  

    |<span data-ttu-id="a8791-115">Campo</span><span class="sxs-lookup"><span data-stu-id="a8791-115">Field</span></span>|<span data-ttu-id="a8791-116">Description</span><span class="sxs-lookup"><span data-stu-id="a8791-116">Description</span></span>|  
    |---------------------------------|---------------------------------------|  
    |<span data-ttu-id="a8791-117">**Cód. días pago**</span><span class="sxs-lookup"><span data-stu-id="a8791-117">**Payment Days Code**</span></span>|<span data-ttu-id="a8791-118">Escriba el código de días de pago.</span><span class="sxs-lookup"><span data-stu-id="a8791-118">Enter the payment day code.</span></span>|  
    |<span data-ttu-id="a8791-119">**Cód. periodo no pago**</span><span class="sxs-lookup"><span data-stu-id="a8791-119">**Non-Paymt. Periods Code**</span></span>|<span data-ttu-id="a8791-120">Escriba el código de los periodos no-pago.</span><span class="sxs-lookup"><span data-stu-id="a8791-120">Enter the non-payment periods code.</span></span>|  

4.  <span data-ttu-id="a8791-121">Para abrir la página **Días pago**, elija la acción **Días pago**.</span><span class="sxs-lookup"><span data-stu-id="a8791-121">To open the **Payment Days** page, choose the **Payment Days** action.</span></span>  
5.  <span data-ttu-id="a8791-122">En la página **Días pago**, en el campo **Día pago**, escriba el día de pago de la empresa.</span><span class="sxs-lookup"><span data-stu-id="a8791-122">On the **Payment Days** page, in the **Payment Day** field, enter the payment day for the company.</span></span>  
6.  <span data-ttu-id="a8791-123">Elija el botón **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="a8791-123">Choose the **OK** button.</span></span>  
7.  <span data-ttu-id="a8791-124">Para abrir la página **Periodos no-pago**, elija la acción **Periodos no-pago**.</span><span class="sxs-lookup"><span data-stu-id="a8791-124">To open the **Non-Payment Periods** page, choose the **Non-Payment Periods** action.</span></span>  
8.  <span data-ttu-id="a8791-125">Escriba información en los campos relevantes.</span><span class="sxs-lookup"><span data-stu-id="a8791-125">Enter information into the relevant fields.</span></span>  
9. <span data-ttu-id="a8791-126">Elija el botón **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="a8791-126">Choose the **OK** button.</span></span>  

## <a name="to-set-up-payment-days-for-customers-and-vendors"></a><span data-ttu-id="a8791-127">Para configurar días de pago para clientes y proveedores</span><span class="sxs-lookup"><span data-stu-id="a8791-127">To set up payment days for customers and vendors</span></span>  

1.  <span data-ttu-id="a8791-128">Seleccione el icono ![Buscar página o informe](../../media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Clientes** o **Proveedores** y, a continuación, seleccione el vínculo relacionado.</span><span class="sxs-lookup"><span data-stu-id="a8791-128">Choose the ![Search for Page or Report](../../media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Customers** or enter **Vendors**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="a8791-129">Seleccione el cliente o el proveedor correspondiente y, a continuación, la acción **Días pago** .</span><span class="sxs-lookup"><span data-stu-id="a8791-129">Select the required customer or vendor, and then choose the **Payment Days** action.</span></span>  
3.  <span data-ttu-id="a8791-130">En la página **Días pago**, en el campo **Día pago**, escriba el día de pago del cliente o proveedor.</span><span class="sxs-lookup"><span data-stu-id="a8791-130">On the **Payment Days** page, in the **Payment Day** field, enter the payment day for the customer or vendor.</span></span>  
4.  <span data-ttu-id="a8791-131">Elija el botón **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="a8791-131">Choose the **OK** button.</span></span>  

## <a name="to-set-up-non-payment-periods-for-customers-and-vendors"></a><span data-ttu-id="a8791-132">Para configurar periodos no-pago para clientes y proveedores</span><span class="sxs-lookup"><span data-stu-id="a8791-132">To set up non-payment periods for customers and vendors</span></span>  

1.  <span data-ttu-id="a8791-133">Seleccione el icono ![Buscar página o informe](../../media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Clientes** o **Proveedores** y, a continuación, seleccione el vínculo relacionado.</span><span class="sxs-lookup"><span data-stu-id="a8791-133">Choose the ![Search for Page or Report](../../media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Customers** or enter **Vendors**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="a8791-134">Seleccione el cliente o el proveedor correspondiente y, a continuación, la acción **Periodos no-pago** .</span><span class="sxs-lookup"><span data-stu-id="a8791-134">Select the required customer or vendor, and then choose the **Non-Payment Periods** action.</span></span>  
3.  <span data-ttu-id="a8791-135">Rellene los campos tal como se describe en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="a8791-135">Fill in the fields as described in the following table.</span></span>  

    |<span data-ttu-id="a8791-136">Campo</span><span class="sxs-lookup"><span data-stu-id="a8791-136">Field</span></span>|<span data-ttu-id="a8791-137">Description</span><span class="sxs-lookup"><span data-stu-id="a8791-137">Description</span></span>|  
    |---------------------------------|---------------------------------------|  
    |<span data-ttu-id="a8791-138">**Desde fecha**</span><span class="sxs-lookup"><span data-stu-id="a8791-138">**From Date**</span></span>|<span data-ttu-id="a8791-139">Escriba la fecha de inicio del periodo no-pago.</span><span class="sxs-lookup"><span data-stu-id="a8791-139">Enter the starting date for the non-payment period.</span></span>|  
    |<span data-ttu-id="a8791-140">**Hasta fecha**</span><span class="sxs-lookup"><span data-stu-id="a8791-140">**To Date**</span></span>|<span data-ttu-id="a8791-141">Escriba la fecha de fin del periodo no-pago.</span><span class="sxs-lookup"><span data-stu-id="a8791-141">Enter the ending date for the non-payment period.</span></span>|  
    |<span data-ttu-id="a8791-142">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="a8791-142">**Description**</span></span>|<span data-ttu-id="a8791-143">Escriba una descripción.</span><span class="sxs-lookup"><span data-stu-id="a8791-143">Enter a description.</span></span>|  

4.  <span data-ttu-id="a8791-144">Elija el botón **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="a8791-144">Choose the **OK** button.</span></span>  

## <a name="see-also"></a><span data-ttu-id="a8791-145">Consulte también</span><span class="sxs-lookup"><span data-stu-id="a8791-145">See Also</span></span>  
 [<span data-ttu-id="a8791-146">Funcionalidad local para España</span><span class="sxs-lookup"><span data-stu-id="a8791-146">Spain Local Functionality</span></span>](spain-local-functionality.md)
