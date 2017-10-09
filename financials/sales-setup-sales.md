---
title: Resumen de tareas para configurar los procesos de venta | Documentos de Microsoft
description: Describe las tareas para configurar reglas y valores para definir las directivas y los procesos de ventas.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: trade, sell, configure
ms.date: 08/23/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: a16201e48cc823e687c9941082d34044d9612a29
ms.contentlocale: es-es
ms.lasthandoff: 09/22/2017

---
# <a name="setting-up-sales"></a><span data-ttu-id="e3e28-103">Configuración de ventas</span><span class="sxs-lookup"><span data-stu-id="e3e28-103">Setting Up Sales</span></span>
<span data-ttu-id="e3e28-104">Para poder administrar procesos de venta, debe configurar las reglas y valores que definen las políticas de venta de la empresa.</span><span class="sxs-lookup"><span data-stu-id="e3e28-104">Before you can manage sales processes, you must configure the rules and values that define the company's sales policies.</span></span>

<span data-ttu-id="e3e28-105">Debe definir la configuración general, como los documentos de venta que se requieren y el modo de registrar sus valores.</span><span class="sxs-lookup"><span data-stu-id="e3e28-105">You must define the general setup, such as which sales documents are required and how their values are posted.</span></span> <span data-ttu-id="e3e28-106">Esta configuración general se efectúa normalmente una vez durante la implementación inicial.</span><span class="sxs-lookup"><span data-stu-id="e3e28-106">This general setup is typically performed once during the initial implementation.</span></span>

<span data-ttu-id="e3e28-107">Una serie de tareas independientes relacionadas con el registro de nuevos clientes es registrar acuerdos de precios especiales o descuentos que tenga con cada cliente.</span><span class="sxs-lookup"><span data-stu-id="e3e28-107">A separate series of tasks related to registering new customers is to record any special price or discount agreements that you have with each customer.</span></span>

<span data-ttu-id="e3e28-108">La configuración de ventas relacionada con las finanzas, como las formas de pago o las divisas, se describe en la sección Configuración de finanzas.</span><span class="sxs-lookup"><span data-stu-id="e3e28-108">Finance-related sales setup, such as payment methods and currencies, are covered in the Finance Setup section.</span></span> <span data-ttu-id="e3e28-109">Para obtener más información, consulte [Configurar finanzas](finance-setup-finance.md).</span><span class="sxs-lookup"><span data-stu-id="e3e28-109">For more information, see [Setting Up Finance](finance-setup-finance.md).</span></span>

| <span data-ttu-id="e3e28-110">Para</span><span class="sxs-lookup"><span data-stu-id="e3e28-110">To</span></span> | <span data-ttu-id="e3e28-111">Vea</span><span class="sxs-lookup"><span data-stu-id="e3e28-111">See</span></span> |
| --- | --- |
| <span data-ttu-id="e3e28-112">Cree una ficha de cliente para cada cliente al que vende.</span><span class="sxs-lookup"><span data-stu-id="e3e28-112">Create a customer card for each customer that you sell to.</span></span> |[<span data-ttu-id="e3e28-113">Registro de clientes nuevos</span><span class="sxs-lookup"><span data-stu-id="e3e28-113">How to: Register New Customers</span></span>](sales-how-register-new-customers.md) |
| <span data-ttu-id="e3e28-114">Permita a los clientes que paguen mediante PayPal eligiendo su logotipo en los documentos de ventas.</span><span class="sxs-lookup"><span data-stu-id="e3e28-114">Enable customers to pay through PayPal by choosing the PayPal logo on sales documents.</span></span> |[<span data-ttu-id="e3e28-115">Permitir el pago de clientes mediante PayPal</span><span class="sxs-lookup"><span data-stu-id="e3e28-115">How to: Enable Customer Payment Through PayPal</span></span>](sales-how-enable-payment-service-extensions.md) |
| <span data-ttu-id="e3e28-116">Especifique los distintos descuentos y precios especiales que ofrece a los clientes en función del producto, cantidades o fecha.</span><span class="sxs-lookup"><span data-stu-id="e3e28-116">Enter the different discounts and special prices that you grant to customers depending on item, quantities, and/or date.</span></span> |[<span data-ttu-id="e3e28-117">Registrar acuerdos de precios de venta, descuentos y pagos</span><span class="sxs-lookup"><span data-stu-id="e3e28-117">How to: Record Sales Price, Discount, and Payment Agreements</span></span>](sales-how-record-sales-price-discount-payment-agreements.md) |
| <span data-ttu-id="e3e28-118">Configure los vendedores para que pueda asignarles contactos de cliente o medir el rendimiento del vendedor como base para calcular la comisión o prima por ventas.</span><span class="sxs-lookup"><span data-stu-id="e3e28-118">Set up salespeople so that you can assign them to customer contacts or measure salespeople's performance as a basis for calculating the sales commission or bonus.</span></span> |[<span data-ttu-id="e3e28-119">Configurar vendedores</span><span class="sxs-lookup"><span data-stu-id="e3e28-119">How to: Set Up Salespeople</span></span>](sales-how-setup-salespeople.md) |
| <span data-ttu-id="e3e28-120">Especifique para clientes individuales o para todos los clientes cómo se envían los documentos de ventas por defecto cuando elige la acción **Registrar y enviar**.</span><span class="sxs-lookup"><span data-stu-id="e3e28-120">Specify for individual customers or for all customers how sales documents are sent by default when you choose the **Post and Send** action.</span></span> |[<span data-ttu-id="e3e28-121">Configurar los perfiles de envío de documentos</span><span class="sxs-lookup"><span data-stu-id="e3e28-121">How to: Set Up Document Sending Profiles</span></span>](sales-how-setup-document-send-profiles.md) |
| <span data-ttu-id="e3e28-122">Configure su correo electrónico para que contenga un resumen de información en el documento de ventas que se está enviando.</span><span class="sxs-lookup"><span data-stu-id="e3e28-122">Set your email up to contain a summary of information in the sales document that is being sent.</span></span> |<span data-ttu-id="e3e28-123">[Enviar documentos por correo electrónico](ui-how-send-documents-email.md).</span><span class="sxs-lookup"><span data-stu-id="e3e28-123">[How to: Send Documents by Email](ui-how-send-documents-email.md).</span></span> |
|<span data-ttu-id="e3e28-124">Utilice un servicio Web de la UE para comprobar el número de CIF/NIF de un cliente.</span><span class="sxs-lookup"><span data-stu-id="e3e28-124">Use an EU web service to verify a customer's VAT registration number.</span></span>|[<span data-ttu-id="e3e28-125">Procedimiento: verificación de números CIF/NIF</span><span class="sxs-lookup"><span data-stu-id="e3e28-125">How to: Verify VAT Registration Numbers</span></span>](sales-how-to-verify-vat-registration-numbers.md)|
|<span data-ttu-id="e3e28-126">Introducir información acerca de los distintos proveedores de transporte empleados, incluyendo un vínculo a su servicio de seguimiento del envío.</span><span class="sxs-lookup"><span data-stu-id="e3e28-126">Enter information about the different transportation vendors you use, including a link to their package tracking service.</span></span>|[<span data-ttu-id="e3e28-127">Cómo configurar transportistas</span><span class="sxs-lookup"><span data-stu-id="e3e28-127">How to: Set Up Shipping Agents</span></span>](sales-how-to-set-up-shipping-agents.md)|

## <a name="see-also"></a><span data-ttu-id="e3e28-128">Consulte también</span><span class="sxs-lookup"><span data-stu-id="e3e28-128">See Also</span></span>
[<span data-ttu-id="e3e28-129">Ccial</span><span class="sxs-lookup"><span data-stu-id="e3e28-129">Sales</span></span>](sales-manage-sales.md)  
<span data-ttu-id="e3e28-130">[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="e3e28-130">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

