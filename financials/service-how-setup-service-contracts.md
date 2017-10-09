---
title: Configurar contratos de servicio | Documentos de Microsoft
description: "Aprenda cómo configurar contratos de servicio."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: service, cost, service order
ms.date: 08/22/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 3eea1854139de9bdfd5dc992159dbc060c79509d
ms.contentlocale: es-es
ms.lasthandoff: 09/22/2017

---

# <a name="how-to-set-up-service-contracts"></a><span data-ttu-id="0a86a-103">Cómo configurar contratos de servicio</span><span class="sxs-lookup"><span data-stu-id="0a86a-103">How to: Set Up Service Contracts</span></span>
<span data-ttu-id="0a86a-104">Antes de que pueda trabajar con contratos, debe configurar las opciones siguientes:</span><span class="sxs-lookup"><span data-stu-id="0a86a-104">Before you can work with contracts, you must set up the following:</span></span> 

* <span data-ttu-id="0a86a-105">**Grupos contrato servicio**, que reúne contratos de servicio relacionados.</span><span class="sxs-lookup"><span data-stu-id="0a86a-105">**Service contract groups**, which gather service contracts that are related in some way.</span></span>
* <span data-ttu-id="0a86a-106">Los **grupos de cuentas de contratos de servicio**, que se utilizan para agrupar las cuentas de contratos de servicio que se utilizan para agrupar las cuentas de contratos de servicio con las facturas de servicio creadas para los contratos de servicio.</span><span class="sxs-lookup"><span data-stu-id="0a86a-106">**Service contract account groups**, which are used to group the service contract accounts together for service invoices created for service contracts.</span></span> <span data-ttu-id="0a86a-107">Asigne estos grupos a los contratos de servicio.</span><span class="sxs-lookup"><span data-stu-id="0a86a-107">You assign these groups to service contracts.</span></span>  
* <span data-ttu-id="0a86a-108">**Plantillas de contratos** que definen las disposiciones del contrato de contratos que incluyen los detalles del contrato de servicio más utilizados.</span><span class="sxs-lookup"><span data-stu-id="0a86a-108">**Contract templates** that define contract layouts of contracts that include the most commonly used service contract details.</span></span> <span data-ttu-id="0a86a-109">Puede utilizar plantillas cuando cree ofertas de contrato de servicio.</span><span class="sxs-lookup"><span data-stu-id="0a86a-109">When you create service contract quotes, you can create them by using templates.</span></span> <span data-ttu-id="0a86a-110">Al crear una oferta de contrato, los campos contienen automáticamente el contenido de los campos de la plantilla.</span><span class="sxs-lookup"><span data-stu-id="0a86a-110">When you create a contract quote, the fields automatically contain the contents of the template fields.</span></span>
* <span data-ttu-id="0a86a-111">Las **Plantillas de clientes** que le permiten crear ofertas para contactos o clientes potenciales que no están registrados como clientes en [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="0a86a-111">**Customer templates** that let you create quotes for contacts or potential customers who are not registered as customers in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>  

## <a name="to-set-up-a-service-contract-group"></a><span data-ttu-id="0a86a-112">Para configurar un grupo de contratos de servicio</span><span class="sxs-lookup"><span data-stu-id="0a86a-112">To set up a service contract group</span></span>  
1. <span data-ttu-id="0a86a-113">Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Grupos contrato servicio** y, a continuación, seleccione el vínculo relacionado.</span><span class="sxs-lookup"><span data-stu-id="0a86a-113">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Service Contract Groups**, and then choose the related link.</span></span>  
2. <span data-ttu-id="0a86a-114">Rellene los campos según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="0a86a-114">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. <span data-ttu-id="0a86a-115">Elija la casilla **Sólo dto. en pedidos contrat.** si desea que los descuentos de contrato o servicio sean válidos únicamente para pedidos de servicio de contrato, como el mantenimiento.</span><span class="sxs-lookup"><span data-stu-id="0a86a-115">Choose the **Disc. on Contr. Orders Only** check box if you want contract or service discounts to be valid only for contract service orders, such as maintenance.</span></span>  

## <a name="to-set-up-a-service-contract-account-group"></a><span data-ttu-id="0a86a-116">Para configurar un grupo de cuentas de contratos de servicio</span><span class="sxs-lookup"><span data-stu-id="0a86a-116">To set up a service contract account group</span></span>  
1. <span data-ttu-id="0a86a-117">Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Grupos contables contr. serv.** y, a continuación, seleccione el vínculo relacionado.</span><span class="sxs-lookup"><span data-stu-id="0a86a-117">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Serv. Contract Account Groups**, and then choose the related link.</span></span>  
2. <span data-ttu-id="0a86a-118">Cree un grupo de cuentas de contratos de servicio nuevo.</span><span class="sxs-lookup"><span data-stu-id="0a86a-118">Create a new service contract account group.</span></span>   
3. <span data-ttu-id="0a86a-119">Rellene los campos **Código** y **Descripción**.</span><span class="sxs-lookup"><span data-stu-id="0a86a-119">Fill in the **Code** and **Description** fields.</span></span> <span data-ttu-id="0a86a-120">Estos campos describen el grupo de cuentas de servicio.</span><span class="sxs-lookup"><span data-stu-id="0a86a-120">These fields describe the service account group.</span></span>  
4. <span data-ttu-id="0a86a-121">Rellene el campo **Cuenta contrato no prepago**, elija el número de la cuenta contable de no prepago.</span><span class="sxs-lookup"><span data-stu-id="0a86a-121">Fill in the **Non-Prepaid Contract Acc.** field, choose general ledger account number for the non-prepaid account.</span></span>  
5. <span data-ttu-id="0a86a-122">En el campo **Cuenta contrato no prepago**, elija el número de la cuenta contable de prepago.</span><span class="sxs-lookup"><span data-stu-id="0a86a-122">In the **Prepaid Contract Acc.** field, choose the general ledger account number for the prepaid account.</span></span>  

## <a name="to-set-up-a-contract-template"></a><span data-ttu-id="0a86a-123">Para configurar una plantilla de contrato</span><span class="sxs-lookup"><span data-stu-id="0a86a-123">To set up a contract template</span></span>  
1. <span data-ttu-id="0a86a-124">Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Plantillas contrato servicio** y, a continuación, seleccione el vínculo relacionado.</span><span class="sxs-lookup"><span data-stu-id="0a86a-124">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Service Contract Templates**, and then choose the related link.</span></span>  
2. <span data-ttu-id="0a86a-125">Cree una plantilla de contrato de servicio nueva.</span><span class="sxs-lookup"><span data-stu-id="0a86a-125">Create a new service contract template.</span></span>  
3. <span data-ttu-id="0a86a-126">En el campo **N.º**,</span><span class="sxs-lookup"><span data-stu-id="0a86a-126">In the **No.**</span></span> <span data-ttu-id="0a86a-127">introduzca un número para la plantilla de contrato.</span><span class="sxs-lookup"><span data-stu-id="0a86a-127">field, enter a number for the contract template.</span></span>  
  
     <span data-ttu-id="0a86a-128">Si ha configurado series numéricas para plantillas de contrato en la ventana **Config. gestión servicio**, también puede presionar la tecla Enter para especificar el siguiente número de plantilla de contrato disponible.</span><span class="sxs-lookup"><span data-stu-id="0a86a-128">Alternatively, if you have set up number series for contract templates in the **Service Mgt. Setup** window, you can press the Enter key to enter the next available contract template number.</span></span> <span data-ttu-id="0a86a-129">Rellene el resto de los campos en caso necesario.</span><span class="sxs-lookup"><span data-stu-id="0a86a-129">Fill in the other fields if appropriate.</span></span>  
  
4. <span data-ttu-id="0a86a-130">En la ficha desplegable **Factura**, rellene el campo **Código de grupo de cuentas de contrato de servicio**, **Período de factura**, etc.</span><span class="sxs-lookup"><span data-stu-id="0a86a-130">On the **Invoice** FastTab, fill in the **Serv. Contract Acc. Group Code** field, the **Invoice Period**, and so on.</span></span> <span data-ttu-id="0a86a-131">Rellene el resto de los campos en caso necesario.</span><span class="sxs-lookup"><span data-stu-id="0a86a-131">Fill in the other fields if appropriate.</span></span>  
5. <span data-ttu-id="0a86a-132">Elija la acción **Descuentos servicio** para agregar descuentos de contrato.</span><span class="sxs-lookup"><span data-stu-id="0a86a-132">Choose the **Service Discounts** action to add contract discounts.</span></span>  

## <a name="to-set-up-a-customer-template"></a><span data-ttu-id="0a86a-133">Para configurar una plantilla de cliente</span><span class="sxs-lookup"><span data-stu-id="0a86a-133">To set up a customer template</span></span>  
1. <span data-ttu-id="0a86a-134">Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Plantillas cliente** y, a continuación, seleccione el vínculo relacionado.</span><span class="sxs-lookup"><span data-stu-id="0a86a-134">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Customer Templates**, and then choose the related link.</span></span>  
2. <span data-ttu-id="0a86a-135">Cree una ficha de plantilla de cliente nueva.</span><span class="sxs-lookup"><span data-stu-id="0a86a-135">Create a new customer template card.</span></span>  
3. <span data-ttu-id="0a86a-136">En la ficha desplegable **General**, escriba un nombre y una descripción para la plantilla de cliente en los campos **Código** y **Descripción** respectivamente.</span><span class="sxs-lookup"><span data-stu-id="0a86a-136">On the **General** FastTab, enter a code and a description for the customer template in the **Code** and **Description** fields respectively.</span></span> 
4. <span data-ttu-id="0a86a-137">Para definir los criterios de búsqueda, rellene los otros campos, como **Cód. país/región**, **Cód. territorio** y **Cód. idioma**.</span><span class="sxs-lookup"><span data-stu-id="0a86a-137">To define search criteria, fill in the other fields, such as **Country/Region Code**, **Territory Code**, and **Language Code**.</span></span>  
5. <span data-ttu-id="0a86a-138">Rellene los campos **Grupo contable negocio** y **Grupo contable cliente**.</span><span class="sxs-lookup"><span data-stu-id="0a86a-138">Fill in the **Gen. Bus. Posting Group** and **Customer Posting Group** fields.</span></span>  

## <a name="see-also"></a><span data-ttu-id="0a86a-139">Consulte también</span><span class="sxs-lookup"><span data-stu-id="0a86a-139">See Also</span></span>
[<span data-ttu-id="0a86a-140">Configurar la gestión de servicios</span><span class="sxs-lookup"><span data-stu-id="0a86a-140">Setting Up Service Management</span></span>](service-setup-service.md)
