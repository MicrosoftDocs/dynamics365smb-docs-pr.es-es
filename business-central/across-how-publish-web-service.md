---
title: Exponga los objetos como servicios Web | Documentos de Microsoft
description: Publique los objetos como servicios web para estén disponibles inmediatamente para la solución Business Central.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: 04af1a52bb0a2e14a2775efe6e3a6ccf77441d29
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/01/2020
ms.locfileid: "3188497"
---
# <a name="publish-a-web-service"></a><span data-ttu-id="371e0-103">Publicar un servicio web</span><span class="sxs-lookup"><span data-stu-id="371e0-103">Publish a Web Service</span></span>

<span data-ttu-id="371e0-104">Los servicios web son una forma ligera para hacer que la funcionalidad de la aplicación esté disponible para una variedad de sistemas externos y usuarios.</span><span class="sxs-lookup"><span data-stu-id="371e0-104">Web services are a lightweight way to make application functionality available to a variety of external systems and users.</span></span> [!INCLUDE[d365fin](includes/d365fin_md.md)] <span data-ttu-id="371e0-105">incluye un número de objetos que se exponen como servicios Web de forma predeterminada debido a la integración con otros servicios de Microsoft, pero también puede agregar otros servicios Web.</span><span class="sxs-lookup"><span data-stu-id="371e0-105">includes an number of objects that are exposed as web services by default due to integration with other Microsoft services, but you can also add other web services.</span></span>  

<span data-ttu-id="371e0-106">Configure un servicio web en el cliente de [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="371e0-106">You set up a web service in the [!INCLUDE[d365fin](includes/d365fin_md.md)] client.</span></span> <span data-ttu-id="371e0-107">A continuación debe publicar el servicio web para ponerlo a disposición de las solicitudes de servicio en la red.</span><span class="sxs-lookup"><span data-stu-id="371e0-107">You must then publish the web service so that it is available to service requests over the network.</span></span> <span data-ttu-id="371e0-108">Los usuarios pueden descubrir servicios Web seleccionando un navegador en la ubicación del servidor y solicitando una lista de servicios disponibles.</span><span class="sxs-lookup"><span data-stu-id="371e0-108">Users can discover web services by pointing a browser at the server location and requesting a list of available services.</span></span> <span data-ttu-id="371e0-109">Al publicar un servicio web, estará disponible inmediatamente a través de la red para los usuarios autenticados.</span><span class="sxs-lookup"><span data-stu-id="371e0-109">When you publish a web service, it is immediately available over the network for authenticated users.</span></span> <span data-ttu-id="371e0-110">Todo los usuarios autorizados pueden tener acceso a los metadatos de los servicios Web, pero solo los usuarios con permisos suficientes pueden tener acceso a los datos reales.</span><span class="sxs-lookup"><span data-stu-id="371e0-110">All authorized users can access metadata for web services, but only users who have sufficient permissions can access actual data.</span></span>

## <a name="creating-and-publishing-a-web-service"></a><span data-ttu-id="371e0-111">Crear y publicar un servicio web</span><span class="sxs-lookup"><span data-stu-id="371e0-111">Creating and Publishing a Web Service</span></span>  
<span data-ttu-id="371e0-112">Los pasos siguientes explican cómo crear y publicar un servicio web.</span><span class="sxs-lookup"><span data-stu-id="371e0-112">The following steps explain how to create and publish a web service.</span></span>  

### <a name="to-create-and-publish-a-web-service"></a><span data-ttu-id="371e0-113">Para crear y publicar un servicio web</span><span class="sxs-lookup"><span data-stu-id="371e0-113">To create and publish a web service</span></span>  

1. <span data-ttu-id="371e0-114">Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Servicios web** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="371e0-114">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Web Services**, and then choose the related link.</span></span>  
2. <span data-ttu-id="371e0-115">En la página **Servicios web**, elija **Nuevo**.</span><span class="sxs-lookup"><span data-stu-id="371e0-115">On the **Web Services** page, choose **New**.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

    > [!NOTE]  
    > <span data-ttu-id="371e0-116">**Codeunit** y **Página** son tipos válidos para los servicios web de SOAP.</span><span class="sxs-lookup"><span data-stu-id="371e0-116">**Codeunit** and **Page** are valid types for SOAP web services.</span></span> <span data-ttu-id="371e0-117">**Página** y **Consulta** son tipos válidos para los servicios web de OData.</span><span class="sxs-lookup"><span data-stu-id="371e0-117">**Page** and **Query** are valid types for OData web services.</span></span>  
    > <span data-ttu-id="371e0-118">También, si la base de datos contiene varias empresas, puede elegir un Id. objeto que sea específico de una de las empresas.</span><span class="sxs-lookup"><span data-stu-id="371e0-118">Also, if the database contains multiple companies, you can choose an object ID that is specific to one of the companies.</span></span>  
    > <span data-ttu-id="371e0-119">Finalmente, el nombre del servicio está visible a los consumidores de su servicio Web y es la base para identificar y distinguir servicios Web, por lo que debería hacer que el nombre tenga sentido.</span><span class="sxs-lookup"><span data-stu-id="371e0-119">Finally, the service name is visible to consumers of your web service and is the basis for identifying and distinguishing web services, so you should make the name meaningful.</span></span>

3. <span data-ttu-id="371e0-120">Activa la casilla en la columna **Publicado**.</span><span class="sxs-lookup"><span data-stu-id="371e0-120">Select the check box in the **Published** column.</span></span>  

<span data-ttu-id="371e0-121">Al publicar el servicio web, en los campos **URL de OData** y **URL de SOAP**, puede ver las direcciones URL que se generan para el servicio web.</span><span class="sxs-lookup"><span data-stu-id="371e0-121">When you publish the web service, in the **OData URL** and **SOAP URL** fields, you can see the URLs that are generated for the web service.</span></span> <span data-ttu-id="371e0-122">Puede probar el servicio web inmediatamente eligiendo los vínculos de los campos **URL de OData** y **URL de SOAP**.</span><span class="sxs-lookup"><span data-stu-id="371e0-122">You can test the web service immediately by choosing the links in the **OData URL** and **SOAP URL** fields.</span></span> <span data-ttu-id="371e0-123">Opcionalmente, puede copiar el valor del campo y guardarlo para su uso posterior.</span><span class="sxs-lookup"><span data-stu-id="371e0-123">Optionally, you can copy the value of the field and save it for later use.</span></span>  

> [!IMPORTANT]
> <span data-ttu-id="371e0-124">Para las codeunits que se publican como un servicio web SOAP, los métodos expuestos en la codeunit deben estar marcados como `[External]` como en el código.</span><span class="sxs-lookup"><span data-stu-id="371e0-124">For codeunits that are published as a SOAP web service, the methods exposed in the codeunit must be marked as `[External]` in the code.</span></span>

<span data-ttu-id="371e0-125">Una vez publique un servicio Web, está disponible a partes externas.</span><span class="sxs-lookup"><span data-stu-id="371e0-125">After you publish a web service, it is available to external parties.</span></span> <span data-ttu-id="371e0-126">Puede verificar la disponibilidad del servicio web con un explorador o bien, puede elegir el vínculo de los campos **URL de OData** y **URL de SOAP** en la página **Servicios web**.</span><span class="sxs-lookup"><span data-stu-id="371e0-126">You can verify the availability of that web service by using a browser, or you can choose the link in the **OData URL** and **SOAP URL** fields on the **Web Services** page.</span></span> <span data-ttu-id="371e0-127">El procedimiento siguiente muestra cómo puede comprobar la disponibilidad del servicio web para uso posterior.</span><span class="sxs-lookup"><span data-stu-id="371e0-127">The following procedure illustrates how you can verify the availability of the web service for later use.</span></span>  

### <a name="to-verify-the-availability-of-a-web-service"></a><span data-ttu-id="371e0-128">Para verificar la disponibilidad de un servicio web</span><span class="sxs-lookup"><span data-stu-id="371e0-128">To verify the availability of a web service</span></span>  

1. <span data-ttu-id="371e0-129">En el explorador, escriba la dirección URL correspondiente.</span><span class="sxs-lookup"><span data-stu-id="371e0-129">In your browser, enter the relevant URL.</span></span> <span data-ttu-id="371e0-130">La tabla siguiente muestra los tipos de direcciones URL que puede introducir para distintos tipos de servicio web.</span><span class="sxs-lookup"><span data-stu-id="371e0-130">The following table illustrates the types of URLs that you can enter for different web service types.</span></span>  

    > [!div class="mx-tdBreakAll"]
    > |<span data-ttu-id="371e0-131">Escriba</span><span class="sxs-lookup"><span data-stu-id="371e0-131">Type</span></span>|<span data-ttu-id="371e0-132">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="371e0-132">Syntax</span></span>|<span data-ttu-id="371e0-133">Ejemplo:</span><span class="sxs-lookup"><span data-stu-id="371e0-133">Example</span></span>|
    > |----------------|------|-------|
    > |<span data-ttu-id="371e0-134">SOAP</span><span class="sxs-lookup"><span data-stu-id="371e0-134">SOAP</span></span>|<span data-ttu-id="371e0-135">https://api.businesscentral.dynamics.com/*versión*/*suscriptor*/Production/WS/*NombreEmpresa*/*entidad*/</span><span class="sxs-lookup"><span data-stu-id="371e0-135">https://api.businesscentral.dynamics.com/*version*/*tenant*/Production/WS/*CompanyName*/*entity*/</span></span> |https://api.businesscentral.dynamics.com/v2.0/7acc9d3d-d354-4616-8bbd-c4fc9f2b15b3/Production/WS/CRONUS%20USA%2C%20Inc./Page/InvoiceDocument|
    > |<span data-ttu-id="371e0-136">OData V4</span><span class="sxs-lookup"><span data-stu-id="371e0-136">OData V4</span></span>|<span data-ttu-id="371e0-137">https://api.businesscentral.dynamics.com/*versión*/*suscriptor*/Production/ODataV4/Company('*NombreEmpresa*')/*entidad*</span><span class="sxs-lookup"><span data-stu-id="371e0-137">https://api.businesscentral.dynamics.com/*version*/*tenant*/Production/ODataV4/Company('*CompanyName*')/*entity*</span></span>|<span data-ttu-id="371e0-138">https://api.businesscentral.dynamics.com/v2.0/7acc9d3d-d354-4616-8bbd-c4fc9f2b15b3/Production/ODataV4/Company('CRONUS%20Estados Unidos%2C%20Inc.')/InvoiceDocument</span><span class="sxs-lookup"><span data-stu-id="371e0-138">https://api.businesscentral.dynamics.com/v2.0/7acc9d3d-d354-4616-8bbd-c4fc9f2b15b3/Production/ODataV4/Company('CRONUS%20USA%2C%20Inc.')/InvoiceDocument</span></span><br/>    <span data-ttu-id="371e0-139">El nombre de la empresa distingue entre mayúsculas y minúsculas.</span><span class="sxs-lookup"><span data-stu-id="371e0-139">The company name is case-sensitive.</span></span>|

2. <span data-ttu-id="371e0-140">Revise la información que se muestra en el explorador.</span><span class="sxs-lookup"><span data-stu-id="371e0-140">Review the information that is displayed in the browser.</span></span> <span data-ttu-id="371e0-141">Compruebe que puede ver el nombre del servicio web que ha creado.</span><span class="sxs-lookup"><span data-stu-id="371e0-141">Verify that you can see the name of the web service that you have created.</span></span>  

<span data-ttu-id="371e0-142">Cuando obtiene acceso a un servicio web, y desea escribir datos de nuevo en [!INCLUDE[d365fin](includes/d365fin_md.md)], debe especificar el nombre de la empresa.</span><span class="sxs-lookup"><span data-stu-id="371e0-142">When you access a web service, and you want to write data back to [!INCLUDE[d365fin](includes/d365fin_md.md)], you must specify the company name.</span></span> <span data-ttu-id="371e0-143">Puede especificar la empresa como parte del URI como se muestra en los ejemplos o bien, puede especificar la empresa como parte de los parámetros de consulta.</span><span class="sxs-lookup"><span data-stu-id="371e0-143">You can specify the company as part of the URI as shown in the examples, or you can specify the company as part of the query parameters.</span></span> <span data-ttu-id="371e0-144">Por ejemplo, los URI siguientes señalan al mismo servicio web de OData y ambos son URI válidos.</span><span class="sxs-lookup"><span data-stu-id="371e0-144">For example, the following URIs point to the same OData web service and are both valid URIs.</span></span>  

```
https://api.businesscentral.dynamics.com/v1.0/OData/Company('CRONUS International Ltd.')/Customer  
```

```
https://api.businesscentral.dynamics.com/v1.0/OData/Customer?company='CRONUS International Ltd.'  
```

## <a name="see-also"></a><span data-ttu-id="371e0-145">Consulte también</span><span class="sxs-lookup"><span data-stu-id="371e0-145">See Also</span></span>

[<span data-ttu-id="371e0-146">Administración</span><span class="sxs-lookup"><span data-stu-id="371e0-146">Administration</span></span>](admin-setup-and-administration.md)  
[<span data-ttu-id="371e0-147">Servicios web de Business Central para desarrolladores</span><span class="sxs-lookup"><span data-stu-id="371e0-147">Business Central Web Services for developers</span></span>](/dynamics365/business-central/dev-itpro/webservices/web-services)  
