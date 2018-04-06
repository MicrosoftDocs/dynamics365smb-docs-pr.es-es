---
title: "Contratos múltiples | Documentos de Microsoft"
description: "Dependiendo de los acuerdos de nivel de servicio con un cliente, es posible que tenga que gestionar un producto de servicio en más de un contrato de servicio."
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
ms.openlocfilehash: 6e4f0bad058bd928f65214f04f978bf3b387cbb8
ms.contentlocale: es-es
ms.lasthandoff: 03/22/2018

---
# <a name="multiple-contracts"></a><span data-ttu-id="b5890-103">Contratos múltiples</span><span class="sxs-lookup"><span data-stu-id="b5890-103">Multiple Contracts</span></span>
<span data-ttu-id="b5890-104">Dependiendo de los acuerdos de nivel de servicio con un cliente, es posible que tenga que gestionar un producto de servicio en más de un contrato de servicio.</span><span class="sxs-lookup"><span data-stu-id="b5890-104">Depending on your service level agreements with a customer, you may have to handle a service item under more than one service contract.</span></span>  
  
<span data-ttu-id="b5890-105">El control de artículos de servicio de múltiples contratos permite hacer lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="b5890-105">By handling a service item under multiple contracts, you can do the following:</span></span>  
  
* <span data-ttu-id="b5890-106">Emitir diferentes contratos para el mismo producto de servicio.</span><span class="sxs-lookup"><span data-stu-id="b5890-106">Issue different contracts for the same service item.</span></span>  
* <span data-ttu-id="b5890-107">Dar servicio a sus componentes por separado.</span><span class="sxs-lookup"><span data-stu-id="b5890-107">Service parts separately.</span></span>  
* <span data-ttu-id="b5890-108">Considerar las diferentes cualificaciones solicitadas para dar servicio a distintos aspectos de un producto de servicio, como los componentes mecánicos y el software.</span><span class="sxs-lookup"><span data-stu-id="b5890-108">Consider different skills that are required to service different aspects of a service item, such as mechanical components and software.</span></span>  
* <span data-ttu-id="b5890-109">Especificar diferentes tiempos y frecuencias de respuesta al dar servicio a distintos componentes de un producto.</span><span class="sxs-lookup"><span data-stu-id="b5890-109">Specify different response times and frequencies in servicing different parts of a service item.</span></span>  
* <span data-ttu-id="b5890-110">Dirigir los diferentes tipos de actividades que se van a realizar en un producto de servicio cuando requiera distintos tipos de servicio en periodos diferentes.</span><span class="sxs-lookup"><span data-stu-id="b5890-110">Address different kinds of activities to be performed on a service item when the service item requires different types of service in different time periods.</span></span>  
* <span data-ttu-id="b5890-111">Seleccionar y asignar un número de contrato adecuado a una línea de producto de servicio al crear un pedido de servicio.</span><span class="sxs-lookup"><span data-stu-id="b5890-111">Select and assign an appropriate contract number to a service item line when you are creating a service order.</span></span>  
* <span data-ttu-id="b5890-112">Gestionar información financiera importante sobre productos de servicio y acuerdos de nivel de servicio.</span><span class="sxs-lookup"><span data-stu-id="b5890-112">Handle relevant financial information about service items and service level agreements.</span></span>  
  
<span data-ttu-id="b5890-113">Puede considerar los siguientes ejemplos de uso de la funcionalidad de múltiples contratos.</span><span class="sxs-lookup"><span data-stu-id="b5890-113">You can consider the following examples of using the multiple contracts functionality.</span></span>  
  
## <a name="creating-multiple-contracts-per-service-item"></a><span data-ttu-id="b5890-114">Creación de múltiples contratos por producto de servicio</span><span class="sxs-lookup"><span data-stu-id="b5890-114">Creating Multiple Contracts per Service Item</span></span>  
<span data-ttu-id="b5890-115">Puede crear manualmente un contrato de servicio u oferta de contrato para productos de servicio registrados en contratos no cancelados propiedad del mismo cliente.</span><span class="sxs-lookup"><span data-stu-id="b5890-115">You can manually create a service contract or contract quote for service items already registered in non-canceled contracts owned by the same customer.</span></span> <span data-ttu-id="b5890-116">Para hacerlo, siga el procedimiento estándar para crear contratos de servicio y ofertas de contrato de servicio.</span><span class="sxs-lookup"><span data-stu-id="b5890-116">To do this, follow the standard procedure of creating service contracts and service contract quotes.</span></span> <span data-ttu-id="b5890-117">Para obtener más información, consulte [Trabajar con contratos de servicio y ofertas de contrato de servicio](service-how-to-create-service-contracts-and-service-contract-quotes.md).</span><span class="sxs-lookup"><span data-stu-id="b5890-117">For more information, see [Work with Service Contracts and Service Contract Quotes](service-how-to-create-service-contracts-and-service-contract-quotes.md).</span></span>  
  
<span data-ttu-id="b5890-118">Cuando se agrega un producto de servicio a una línea de contrato que ya está registrado en otro contrato de servicio u oferta de contrato, se muestra un mensaje de advertencia que indica que el producto de servicio ya pertenece a uno o varios contratos de servicio u ofertas de contrato.</span><span class="sxs-lookup"><span data-stu-id="b5890-118">When you add a service item on a contract line that is registered in other service contracts or contract quotes, a warning message is displayed stating that the service item already belongs to one or more service contracts or contract quotes.</span></span> <span data-ttu-id="b5890-119">Si confirma este mensaje, toda la información pertinente del producto de servicio se copiará en la línea de contrato recién creada.</span><span class="sxs-lookup"><span data-stu-id="b5890-119">If you confirm this message, all relevant service item information is copied to a newly created contract line.</span></span>  
  
## <a name="copying-documents"></a><span data-ttu-id="b5890-120">Copiar documentos</span><span class="sxs-lookup"><span data-stu-id="b5890-120">Copying Documents</span></span>  
<span data-ttu-id="b5890-121">Puede crear automáticamente un contrato de servicio u oferta de contrato para productos de servicio ya registrados en otros contratos de servicio u ofertas de contratos mediante la acción **Copiar documento**.</span><span class="sxs-lookup"><span data-stu-id="b5890-121">You can automatically create a service contract or contract quote for service items that are already registered in other service contracts or contract quotes by using the **Copy Document** action.</span></span>  
  
## <a name="creating-service-orders-for-multiple-contracts"></a><span data-ttu-id="b5890-122">Creación de pedidos de servicios para múltiples contratos</span><span class="sxs-lookup"><span data-stu-id="b5890-122">Creating Service Orders for Multiple Contracts</span></span>  
<span data-ttu-id="b5890-123">Puede crear un pedido de servicio manualmente para un producto de servicio que esté registrado en múltiples contratos activos.</span><span class="sxs-lookup"><span data-stu-id="b5890-123">You can manually create a service order for a service item that is registered in multiple active contracts.</span></span> <span data-ttu-id="b5890-124">Un contrato de servicio está activo cuando está firmado y no ha caducado.</span><span class="sxs-lookup"><span data-stu-id="b5890-124">A service contract is active when it is signed and not expired.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="b5890-125">Consulte también</span><span class="sxs-lookup"><span data-stu-id="b5890-125">See Also</span></span>  
[<span data-ttu-id="b5890-126">Cumplimiento de contratos de servicio</span><span class="sxs-lookup"><span data-stu-id="b5890-126">Fulfilling Service Contracts</span></span>](service-fulfill-service-contracts.md)  
[<span data-ttu-id="b5890-127">Crear pedidos de servicio</span><span class="sxs-lookup"><span data-stu-id="b5890-127">Create Service Orders</span></span>](service-how-to-create-service-orders.md)  

