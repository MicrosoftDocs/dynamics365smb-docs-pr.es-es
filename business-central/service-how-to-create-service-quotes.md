---
title: Cómo crear ofertas de servicio | Documentos de Microsoft
description: Puede utilizar la página **Oferta servicio** para crear documentos en los que se introduce información acerca de un servicio, como reparación y mantenimiento, de productos de servicio a solicitud del cliente. Puede utilizar una oferta de servicio como borrador de un pedido de servicio y, más adelante, convertir la oferta en un pedido de servicio.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: 0d4c8bba7814e33eb353ea39b3681aa52be53f40
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/01/2020
ms.locfileid: "3189872"
---
# <a name="create-service-quotes"></a><span data-ttu-id="d7b79-104">Crear ofertas de servicio</span><span class="sxs-lookup"><span data-stu-id="d7b79-104">Create Service Quotes</span></span>
<span data-ttu-id="d7b79-105">Puede pensar en ofertas de servicio como base para los pedidos de servicio.</span><span class="sxs-lookup"><span data-stu-id="d7b79-105">You can think of service quotes as the basis for service orders.</span></span> <span data-ttu-id="d7b79-106">De hecho, son casi idénticos.</span><span class="sxs-lookup"><span data-stu-id="d7b79-106">In fact, they are almost identical.</span></span> <span data-ttu-id="d7b79-107">Ambos contienen información como quién es el cliente, el tipo de pedido, el producto que requiera servicio, información sobre facturación y sobre el envío, e información acerca del proyecto de servicio real.</span><span class="sxs-lookup"><span data-stu-id="d7b79-107">They both contain information such as who the customer is, the type of order, the item that needs service, billing and shipping information, and information about the actual service work.</span></span>
 
<span data-ttu-id="d7b79-108">Puede utilizar una oferta de servicio como borrador de un pedido de servicio y, más adelante, convertir la oferta en un pedido de servicio.</span><span class="sxs-lookup"><span data-stu-id="d7b79-108">You can use a service quote as a preliminary draft for a service order, and then convert the quote to a service order.</span></span>  
  
## <a name="to-create-a-service-quote"></a><span data-ttu-id="d7b79-109">Para crear una oferta de servicio</span><span class="sxs-lookup"><span data-stu-id="d7b79-109">To create a service quote</span></span>  
1. <span data-ttu-id="d7b79-110">Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Ofertas servicio** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="d7b79-110">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Service Quotes**, and then choose the related link.</span></span>  
2. <span data-ttu-id="d7b79-111">Cree una oferta de servicio nueva.</span><span class="sxs-lookup"><span data-stu-id="d7b79-111">Create a new service quote.</span></span>  
3. <span data-ttu-id="d7b79-112">En el campo **N.º**,</span><span class="sxs-lookup"><span data-stu-id="d7b79-112">In the **No.**</span></span> <span data-ttu-id="d7b79-113">introduzca un número para la oferta de servicio.</span><span class="sxs-lookup"><span data-stu-id="d7b79-113">field, enter a number for the service quote.</span></span> <span data-ttu-id="d7b79-114">Si ha configurado números de serie para ofertas de servicio en la página **Config. gestión servicio**, también puede presionar Enter para seleccionar el siguiente número de oferta de servicio disponible.</span><span class="sxs-lookup"><span data-stu-id="d7b79-114">Alternatively, if you have set up a number series for service quotes on the **Service Mgt. Setup** page, you can press Enter to select the next available service quote number.</span></span>  
4. <span data-ttu-id="d7b79-115">En el campo **Nº cliente**,</span><span class="sxs-lookup"><span data-stu-id="d7b79-115">In the **Customer No.**</span></span>  <span data-ttu-id="d7b79-116">seleccione el cliente pertinente de la lista.</span><span class="sxs-lookup"><span data-stu-id="d7b79-116">field, select the relevant customer from the list.</span></span>  

  > [!Note]  
  >  <span data-ttu-id="d7b79-117">Los campos del cliente se rellenan automáticamente con información de la pestaña **Cliente**.</span><span class="sxs-lookup"><span data-stu-id="d7b79-117">The customer fields are filled in automatically with information from the **Customer** card.</span></span> <span data-ttu-id="d7b79-118">Si una pestaña **Cliente** no existe para el cliente y ha configurado una plantilla de cliente, podrá crear el cliente que figura en la oferta del servicio.</span><span class="sxs-lookup"><span data-stu-id="d7b79-118">If a **Customer** card does not exist for the customer, and you have set up a customer template, you can create the customer from the service quote.</span></span> <span data-ttu-id="d7b79-119">Rellene los campos relevantes y, a continuación, seleccione la acción **Crear cliente**.</span><span class="sxs-lookup"><span data-stu-id="d7b79-119">Fill in the relevant fields, and then choose the **Create Customer** action.</span></span>  
  
5. <span data-ttu-id="d7b79-120">Dependiendo de la configuración de la ficha desplegable **Campos obligatorios** de la página **Configurar gestión servicios**, puede que necesite rellenar el campo **Tipo pedido de servicio** y el campo **Código de vendedor**.</span><span class="sxs-lookup"><span data-stu-id="d7b79-120">Depending on the settings on the **Mandatory Fields** FastTab on the **Service Mgt. Setup** page, you may need to fill in the **Service Order Type** field and the **Salesperson Code** field.</span></span>  
6. <span data-ttu-id="d7b79-121">Rellene las líneas de producto de servicio.</span><span class="sxs-lookup"><span data-stu-id="d7b79-121">Fill in the service item lines.</span></span>  
7. <span data-ttu-id="d7b79-122">Registre los costes previstos en las líneas de servicio.</span><span class="sxs-lookup"><span data-stu-id="d7b79-122">Register estimated costs on the service lines.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="d7b79-123">Consulte también</span><span class="sxs-lookup"><span data-stu-id="d7b79-123">See Also</span></span>  
[<span data-ttu-id="d7b79-124">Crear pedidos de servicio</span><span class="sxs-lookup"><span data-stu-id="d7b79-124">Create Service Orders</span></span>](service-how-to-create-service-orders.md)  
[<span data-ttu-id="d7b79-125">Trabajar en tareas de servicio</span><span class="sxs-lookup"><span data-stu-id="d7b79-125">Work on Service tasks</span></span>](service-how-to-work-on-service-tasks.md)  

 