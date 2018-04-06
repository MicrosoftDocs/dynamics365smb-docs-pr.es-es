---
title: Facturar las reservas en Business Central | Documentos de Microsoft
description: "Obtenga información sobre cómo realizar la facturación masiva desde Microsoft Bookings en Business Central."
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: invoicing, bookings
ms.date: 06/14/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 56a41a81bee7084d0f624e6ce9bc4a7138e77ff0
ms.contentlocale: es-es
ms.lasthandoff: 03/22/2018

---
# <a name="bulk-invoicing-for-microsoft-bookings-in-included365finincludesd365finmdmd"></a><span data-ttu-id="af5bd-103">Facturación masiva para Microsoft Bookings en [!INCLUDE[d365fin](includes/d365fin_md.md)]</span><span class="sxs-lookup"><span data-stu-id="af5bd-103">Bulk Invoicing for Microsoft Bookings in [!INCLUDE[d365fin](includes/d365fin_md.md)]</span></span>
<span data-ttu-id="af5bd-104">Si su empresa utiliza la aplicación Bookings en Office 365, puede hacer la facturación masiva para citas.</span><span class="sxs-lookup"><span data-stu-id="af5bd-104">If your company uses the Bookings app in Office 365, you can do bulk invoicing for appointments.</span></span> <span data-ttu-id="af5bd-105">La página **Bookings sin facturar** de [!INCLUDE[d365fin](includes/d365fin_md.md)] ofrece una lista de las reservas completadas de la empresa.</span><span class="sxs-lookup"><span data-stu-id="af5bd-105">The **Uninvoiced Bookings** page in [!INCLUDE[d365fin](includes/d365fin_md.md)] provides a list of the company's completed bookings.</span></span> <span data-ttu-id="af5bd-106">En esta página puede seleccionar rápidamente citas que desea facturar y para crear borradores de factura de los servicios prestados.</span><span class="sxs-lookup"><span data-stu-id="af5bd-106">In this page you can quickly select the appointments that you want to invoice and create draft invoices for the services provided.</span></span>  

## <a name="connect-to-bookings"></a><span data-ttu-id="af5bd-107">Conectarse a Bookings</span><span class="sxs-lookup"><span data-stu-id="af5bd-107">Connect to Bookings</span></span>
<span data-ttu-id="af5bd-108">Para conectarse [!INCLUDE[d365fin](includes/d365fin_md.md)] con Bookings, debe especificar su empresa de Bookings, lo que desea sincronizar con Bookings, la frecuencia con que se realizará la sincronización y las plantillas que se usarán.</span><span class="sxs-lookup"><span data-stu-id="af5bd-108">To connect your [!INCLUDE[d365fin](includes/d365fin_md.md)] with Bookings, you must specify your Bookings company, what to synchronize with Bookings, how often to synchronize, and which templates to use.</span></span> <span data-ttu-id="af5bd-109">Puede configurar esta información en la página **Configuración de sincronización de Bookings**, que puede iniciar desde la página **Configuración de la sincronización de Exchange**, que puede encontrar mediante [Buscar](ui-search.md).</span><span class="sxs-lookup"><span data-stu-id="af5bd-109">You set up this information in the **Booking Sync. Setup** page, which you can launch from the **Exchange Sync. Setup** page, which you can find through [Search](ui-search.md).</span></span>  

<span data-ttu-id="af5bd-110">Por ejemplo, si desea sincronizar clientes entre Bookings y [!INCLUDE[d365fin](includes/d365fin_md.md)], debe especificar la plantilla predeterminada que se usa para agregar a los clientes nuevos en [!INCLUDE[d365fin](includes/d365fin_md.md)] basándose en los clientes en su empresa de Bookings.</span><span class="sxs-lookup"><span data-stu-id="af5bd-110">For example, if you want to synchronize customers between Bookings and [!INCLUDE[d365fin](includes/d365fin_md.md)], you must specify the default template to use to add new customers in [!INCLUDE[d365fin](includes/d365fin_md.md)] based on the customers in your Bookings company.</span></span>  

## <a name="invoice-appointments"></a><span data-ttu-id="af5bd-111">Citas de factura</span><span class="sxs-lookup"><span data-stu-id="af5bd-111">Invoice Appointments</span></span>
<span data-ttu-id="af5bd-112">Cuando sea el momento enviar facturas de las reservas completadas, vaya a la página **Bookings sin facturar**.</span><span class="sxs-lookup"><span data-stu-id="af5bd-112">When it is time to send invoices for the completed bookings, you go to the **Uninvoiced Bookings** page.</span></span> <span data-ttu-id="af5bd-113">Dependiendo de la frecuencia con que se sincroniza la información, la lista es larga o corta.</span><span class="sxs-lookup"><span data-stu-id="af5bd-113">Depending on how often the information is synchronized, the list is long or short.</span></span> <span data-ttu-id="af5bd-114">Puede crear facturas para todas las reservas de la lista o una reserva cada vez.</span><span class="sxs-lookup"><span data-stu-id="af5bd-114">You can create invoices for all bookings in the list or one booking at a time.</span></span> <span data-ttu-id="af5bd-115">Puede seleccionar una o varias entradas de la lista y facturar solo esas.</span><span class="sxs-lookup"><span data-stu-id="af5bd-115">You can select one or more entries in the list and invoice those only.</span></span>  

<span data-ttu-id="af5bd-116">La compatibilidad para facturar citas desde Bookings es más simple que el flujo de trabajo completo para trabajar con ofertas de ventas, pedidos de ventas y facturas de ventas.</span><span class="sxs-lookup"><span data-stu-id="af5bd-116">The support for invoicing appointments from Bookings is simpler than the fuller workflow of working with sales quotes, sales orders, and sales invoices.</span></span> <span data-ttu-id="af5bd-117">Para obtener más información, vea [Facturar ventas](sales-how-invoice-sales.md).</span><span class="sxs-lookup"><span data-stu-id="af5bd-117">For more information, see [Invoice Sales](sales-how-invoice-sales.md).</span></span> <span data-ttu-id="af5bd-118">Puede elegir vender sus servicios utilizando [!INCLUDE[d365fin](includes/d365fin_md.md)] o elegir usar Bookings, en función de sus necesidades empresariales.</span><span class="sxs-lookup"><span data-stu-id="af5bd-118">You can choose to sell your services using [!INCLUDE[d365fin](includes/d365fin_md.md)] or choose to use Bookings, depending on your business needs.</span></span>  

## <a name="see-also"></a><span data-ttu-id="af5bd-119">Consulte también</span><span class="sxs-lookup"><span data-stu-id="af5bd-119">See Also</span></span>
[<span data-ttu-id="af5bd-120">Finanzas</span><span class="sxs-lookup"><span data-stu-id="af5bd-120">Finance</span></span>](finance.md)  
[<span data-ttu-id="af5bd-121">Facturar ventas</span><span class="sxs-lookup"><span data-stu-id="af5bd-121">Invoice Sales</span></span>](sales-how-invoice-sales.md)  
[<span data-ttu-id="af5bd-122">Configuración de ventas</span><span class="sxs-lookup"><span data-stu-id="af5bd-122">Setting Up Sales</span></span>](sales-setup-sales.md)  
[<span data-ttu-id="af5bd-123">Microsoft Bookings</span><span class="sxs-lookup"><span data-stu-id="af5bd-123">Microsoft Bookings</span></span>](https://products.office.com/en-us/business/scheduling-and-booking-app)  

