---
title: "Cómo crear ofertas de servicio | Documentos de Microsoft"
description: "Puede utilizar la ventana **Oferta servicio** para crear documentos en los que se introduce información acerca de un servicio, como reparación y mantenimiento, de productos de servicio a solicitud del cliente. Puede utilizar una oferta de servicio como borrador de un pedido de servicio y, más adelante, convertir la oferta en un pedido de servicio."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 91928287d24c2b6199ea243bdc00e48e136adcfd
ms.contentlocale: es-es
ms.lasthandoff: 03/22/2018

---
# <a name="create-service-quotes"></a><span data-ttu-id="ce11c-104">Crear ofertas de servicio</span><span class="sxs-lookup"><span data-stu-id="ce11c-104">Create Service Quotes</span></span>
<span data-ttu-id="ce11c-105">Puede pensar en ofertas de servicio como base para los pedidos de servicio.</span><span class="sxs-lookup"><span data-stu-id="ce11c-105">You can think of service quotes as the basis for service orders.</span></span> <span data-ttu-id="ce11c-106">De hecho, son casi idénticos.</span><span class="sxs-lookup"><span data-stu-id="ce11c-106">In fact, they are almost identical.</span></span> <span data-ttu-id="ce11c-107">Ambos contienen información como quién es el cliente, el tipo de pedido, el producto que requiera servicio, información sobre facturación y sobre el envío, e información acerca del proyecto de servicio real.</span><span class="sxs-lookup"><span data-stu-id="ce11c-107">They both contain information such as who the customer is, the type of order, the item that needs service, billing and shipping information, and information about the actual service work.</span></span>
 
<span data-ttu-id="ce11c-108">Puede utilizar una oferta de servicio como borrador de un pedido de servicio y, más adelante, convertir la oferta en un pedido de servicio.</span><span class="sxs-lookup"><span data-stu-id="ce11c-108">You can use a service quote as a preliminary draft for a service order, and then convert the quote to a service order.</span></span>  
  
## <a name="to-create-a-service-quote"></a><span data-ttu-id="ce11c-109">Para crear una oferta de servicio</span><span class="sxs-lookup"><span data-stu-id="ce11c-109">To create a service quote</span></span>  
1. <span data-ttu-id="ce11c-110">Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Ofertas servicios** y, a continuación, seleccione el vínculo relacionado.</span><span class="sxs-lookup"><span data-stu-id="ce11c-110">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Service Quotes**, and then choose the related link.</span></span>  
2. <span data-ttu-id="ce11c-111">Cree una oferta de servicio nueva.</span><span class="sxs-lookup"><span data-stu-id="ce11c-111">Create a new service quote.</span></span>  
3. <span data-ttu-id="ce11c-112">En el campo **N.º**,</span><span class="sxs-lookup"><span data-stu-id="ce11c-112">In the **No.**</span></span> <span data-ttu-id="ce11c-113">introduzca un número para la oferta de servicio.</span><span class="sxs-lookup"><span data-stu-id="ce11c-113">field, enter a number for the service quote.</span></span> <span data-ttu-id="ce11c-114">Si ha configurado números de serie para ofertas de servicio en la ventana **Config. gestión servicio**, también puede presionar Enter para seleccionar el siguiente número de oferta de servicio disponible.</span><span class="sxs-lookup"><span data-stu-id="ce11c-114">Alternatively, if you have set up a number series for service quotes in the **Service Mgt. Setup** window, you can press Enter to select the next available service quote number.</span></span>  
4. <span data-ttu-id="ce11c-115">En el campo **Nº cliente**,</span><span class="sxs-lookup"><span data-stu-id="ce11c-115">In the **Customer No.**</span></span>  <span data-ttu-id="ce11c-116">seleccione el cliente pertinente de la lista.</span><span class="sxs-lookup"><span data-stu-id="ce11c-116">field, select the relevant customer from the list.</span></span>  

  > [!Note]  
  >  <span data-ttu-id="ce11c-117">Los campos del cliente se rellenan automáticamente con información de la pestaña **Cliente**.</span><span class="sxs-lookup"><span data-stu-id="ce11c-117">The customer fields are filled in automatically with information from the **Customer** card.</span></span> <span data-ttu-id="ce11c-118">Si una pestaña **Cliente** no existe para el cliente y ha configurado una plantilla de cliente, podrá crear el cliente que figura en la oferta del servicio.</span><span class="sxs-lookup"><span data-stu-id="ce11c-118">If a **Customer** card does not exist for the customer, and you have set up a customer template, you can create the customer from the service quote.</span></span> <span data-ttu-id="ce11c-119">Rellene los campos relevantes y, a continuación, seleccione la acción **Crear cliente**.</span><span class="sxs-lookup"><span data-stu-id="ce11c-119">Fill in the relevant fields, and then choose the **Create Customer** action.</span></span>  
  
5. <span data-ttu-id="ce11c-120">Dependiendo de la configuración de la ficha desplegable **Campos obligatorios** de la ventana **Configurar gestión servicios**, puede que necesite rellenar el campo **Tipo pedido de servicio** y el campo **Código de vendedor**.</span><span class="sxs-lookup"><span data-stu-id="ce11c-120">Depending on the settings on the **Mandatory Fields** FastTab in the **Service Mgt. Setup** window, you may need to fill in the **Service Order Type** field and the **Salesperson Code** field.</span></span>  
6. <span data-ttu-id="ce11c-121">Rellene las líneas de producto de servicio.</span><span class="sxs-lookup"><span data-stu-id="ce11c-121">Fill in the service item lines.</span></span>  
7. <span data-ttu-id="ce11c-122">Registre los costes previstos en las líneas de servicio.</span><span class="sxs-lookup"><span data-stu-id="ce11c-122">Register estimated costs on the service lines.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ce11c-123">Consulte también</span><span class="sxs-lookup"><span data-stu-id="ce11c-123">See Also</span></span>  
[<span data-ttu-id="ce11c-124">Crear pedidos de servicio</span><span class="sxs-lookup"><span data-stu-id="ce11c-124">Create Service Orders</span></span>](service-how-to-create-service-orders.md)  
[<span data-ttu-id="ce11c-125">Trabajar en tareas de servicio</span><span class="sxs-lookup"><span data-stu-id="ce11c-125">Work on Service tasks</span></span>](service-how-to-work-on-service-tasks.md)  

 
