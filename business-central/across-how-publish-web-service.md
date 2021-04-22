---
title: Exponer los objetos como servicios web
description: Publique los objetos como servicios web para estén disponibles inmediatamente para la solución Business Central.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 59b6febc147687e88f11423b4ad317ab6ee5a408
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 03/31/2021
ms.locfileid: "5775952"
---
# <a name="publish-a-web-service"></a><span data-ttu-id="775fd-103">Publicar un servicio web</span><span class="sxs-lookup"><span data-stu-id="775fd-103">Publish a Web Service</span></span>

<span data-ttu-id="775fd-104">Los servicios web son una forma ligera para hacer que la funcionalidad de la aplicación esté disponible en distintas clases de sistemas externos y usuarios.</span><span class="sxs-lookup"><span data-stu-id="775fd-104">Web services are a lightweight way to make application functionality available to different kinds of external systems and users.</span></span> <span data-ttu-id="775fd-105">Por defecto, [!INCLUDE[prod_short](includes/prod_short.md)] expone una serie de objetos, como servicios web, para una mejor integración con otros servicios de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="775fd-105">By default, [!INCLUDE[prod_short](includes/prod_short.md)] exposes a number of objects as web services for better integration with other Microsoft services.</span></span> <span data-ttu-id="775fd-106">Puede agregar otros servicios web según lo requiera su empresa.</span><span class="sxs-lookup"><span data-stu-id="775fd-106">You can add other web services as your business requires.</span></span>  

<span data-ttu-id="775fd-107">Configure un servicio web en [!INCLUDE[prod_short](includes/prod_short.md)] y luego publique el servicio web para que esté disponible para los usuarios autenticados.</span><span class="sxs-lookup"><span data-stu-id="775fd-107">Set up a web service in [!INCLUDE[prod_short](includes/prod_short.md)], and then publish the web service so that it is available to authenticated users.</span></span> <span data-ttu-id="775fd-108">Todo los usuarios autorizados pueden tener acceso a los metadatos de los servicios Web, pero solo los usuarios con permisos suficientes pueden tener acceso a los datos reales.</span><span class="sxs-lookup"><span data-stu-id="775fd-108">All authorized users can access metadata for web services, but only users who have sufficient permissions can access actual data.</span></span>  

## <a name="creating-and-publishing-a-web-service"></a><span data-ttu-id="775fd-109">Crear y publicar un servicio web</span><span class="sxs-lookup"><span data-stu-id="775fd-109">Creating and Publishing a Web Service</span></span>

<span data-ttu-id="775fd-110">Los pasos siguientes explican cómo crear y publicar un servicio web.</span><span class="sxs-lookup"><span data-stu-id="775fd-110">The following steps explain how to create and publish a web service.</span></span>  

### <a name="to-create-and-publish-a-web-service"></a><span data-ttu-id="775fd-111">Para crear y publicar un servicio web</span><span class="sxs-lookup"><span data-stu-id="775fd-111">To create and publish a web service</span></span>  

1. <span data-ttu-id="775fd-112">Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Servicios web** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="775fd-112">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Web Services**, and then choose the related link.</span></span>  
2. <span data-ttu-id="775fd-113">En la página **Servicios web**, elija **Nuevo**.</span><span class="sxs-lookup"><span data-stu-id="775fd-113">On the **Web Services** page, choose **New**.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

    > [!NOTE]  
    > <span data-ttu-id="775fd-114">**Codeunit** y **Página** son tipos válidos para los servicios web de SOAP.</span><span class="sxs-lookup"><span data-stu-id="775fd-114">**Codeunit** and **Page** are valid types for SOAP web services.</span></span> <span data-ttu-id="775fd-115">**Página** y **Consulta** son tipos válidos para los servicios web de OData.</span><span class="sxs-lookup"><span data-stu-id="775fd-115">**Page** and **Query** are valid types for OData web services.</span></span> <span data-ttu-id="775fd-116">A partir de la versión 16.3, **Codeunit** también es un tipo válido para los servicios web de OData v4, pero no se muestra ninguna URL en la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="775fd-116">Starting with version 16.3, **Codeunit** is also a valid type for OData v4 web services, but then no URL is shown in the user interface.</span></span> <span data-ttu-id="775fd-117">También, si la base de datos contiene varias empresas, puede elegir un Id. objeto que sea específico de una de las empresas.</span><span class="sxs-lookup"><span data-stu-id="775fd-117">Also, if the database contains multiple companies, you can choose an object ID that is specific to one of the companies.</span></span>  
    > <span data-ttu-id="775fd-118">Finalmente, el nombre del servicio está visible a los consumidores de su servicio Web y es la base para identificar y distinguir servicios Web, por lo que debería hacer que el nombre tenga sentido.</span><span class="sxs-lookup"><span data-stu-id="775fd-118">Finally, the service name is visible to consumers of your web service and is the basis for identifying and distinguishing web services, so you should make the name meaningful.</span></span>

3. <span data-ttu-id="775fd-119">Activa la casilla en la columna **Publicado**.</span><span class="sxs-lookup"><span data-stu-id="775fd-119">Select the check box in the **Published** column.</span></span>  

<span data-ttu-id="775fd-120">Cuando publica el servicio web, los campos **URL de OData** y **URL de SOAP** muestran las nuevas URL.</span><span class="sxs-lookup"><span data-stu-id="775fd-120">When you publish the web service, the **OData URL** and **SOAP URL** fields show the new URLs.</span></span> <span data-ttu-id="775fd-121">Sin embargo, para las codeunits que se exponen como acciones independientes de OData v4, los campos de URL no se muestran.</span><span class="sxs-lookup"><span data-stu-id="775fd-121">However, for codeunits that are exposed as OData v4 unbound actions, the URL fields are not shown.</span></span>  

<span data-ttu-id="775fd-122">Puede probar el servicio web inmediatamente eligiendo los vínculos de los campos **URL de OData** y **URL de SOAP**.</span><span class="sxs-lookup"><span data-stu-id="775fd-122">You can test the web service immediately by choosing the links in the **OData URL** and **SOAP URL** fields.</span></span> <span data-ttu-id="775fd-123">Opcionalmente, copie el valor del campo y guárdelo para su uso posterior.</span><span class="sxs-lookup"><span data-stu-id="775fd-123">Optionally, copy the value of the field and save it for later use.</span></span> <span data-ttu-id="775fd-124">Para probar las unidades de código que se exponen como acciones independientes de OData v4, siga las instrucciones de la sección [Verificación de la disponibilidad del servicio web](/dynamics365/business-central/dev-itpro/developer/devenv-creating-and-interacting-with-odatav4-unbound-action#verifying-web-service-availability) del contenido del desarrollador.</span><span class="sxs-lookup"><span data-stu-id="775fd-124">To test codeunits that are exposed as OData v4 unbound actions, follow the instructions in the [Verifying web service availability](/dynamics365/business-central/dev-itpro/developer/devenv-creating-and-interacting-with-odatav4-unbound-action#verifying-web-service-availability) section in the developer content.</span></span>

> [!NOTE]
> <span data-ttu-id="775fd-125">Si los objetos que expone como servicios web no deben ser accesibles desde [!INCLUDE[prod_short](includes/prod_short.md)] en línea, debe marcar los métodos expuestos en el código como `[Scope('OnPrem')]`.</span><span class="sxs-lookup"><span data-stu-id="775fd-125">If the objects that you expose as web services must not be accessible from [!INCLUDE[prod_short](includes/prod_short.md)] online, you must mark the methods exposed in the code as `[Scope('OnPrem')]`.</span></span> <span data-ttu-id="775fd-126">Para obtener más información, consulte [Ámbito de atributo](/dynamics365/business-central/dev-itpro/developer/methods/devenv-scope-attribute).</span><span class="sxs-lookup"><span data-stu-id="775fd-126">For more information, see [Scope Attribute](/dynamics365/business-central/dev-itpro/developer/methods/devenv-scope-attribute).</span></span>

<span data-ttu-id="775fd-127">Una vez publique un servicio Web, está disponible a partes externas.</span><span class="sxs-lookup"><span data-stu-id="775fd-127">After you publish a web service, it is available to external parties.</span></span> <span data-ttu-id="775fd-128">Puede verificar la disponibilidad del servicio web con un explorador o bien, puede elegir el vínculo de los campos **URL de OData** y **URL de SOAP** en la página **Servicios web**.</span><span class="sxs-lookup"><span data-stu-id="775fd-128">You can verify the availability of that web service by using a browser, or choose the link in the **OData URL** and **SOAP URL** fields on the **Web Services** page.</span></span> <span data-ttu-id="775fd-129">El procedimiento siguiente muestra cómo puede comprobar la disponibilidad del servicio web para uso posterior.</span><span class="sxs-lookup"><span data-stu-id="775fd-129">The following procedure illustrates how you can verify the availability of the web service for later use.</span></span>  

### <a name="to-verify-the-availability-of-a-web-service"></a><span data-ttu-id="775fd-130">Para verificar la disponibilidad de un servicio web</span><span class="sxs-lookup"><span data-stu-id="775fd-130">To verify the availability of a web service</span></span>  

1. <span data-ttu-id="775fd-131">En el explorador, escriba la dirección URL correspondiente.</span><span class="sxs-lookup"><span data-stu-id="775fd-131">In your browser, enter the relevant URL.</span></span> <span data-ttu-id="775fd-132">La tabla siguiente muestra los tipos de direcciones URL que puede introducir para distintos tipos de servicio web.</span><span class="sxs-lookup"><span data-stu-id="775fd-132">The following table illustrates the types of URLs that you can enter for different web service types.</span></span>  

    > [!div class="mx-tdBreakAll"]
    > |<span data-ttu-id="775fd-133">Escriba</span><span class="sxs-lookup"><span data-stu-id="775fd-133">Type</span></span>|<span data-ttu-id="775fd-134">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="775fd-134">Syntax</span></span>|<span data-ttu-id="775fd-135">Ejemplo:</span><span class="sxs-lookup"><span data-stu-id="775fd-135">Example</span></span>|
    > |----------------|------|-------|
    > |<span data-ttu-id="775fd-136">SOAP</span><span class="sxs-lookup"><span data-stu-id="775fd-136">SOAP</span></span>|`https://api.businesscentral.dynamics.com/*version*/*tenant*/Production/WS/*CompanyName*/*entity*/` |`https://api.businesscentral.dynamics.com/v2.0/7acc9d3d-d354-4616-8bbd-c4fc9f2b15b3/Production/WS/CRONUS%20USA%2C%20Inc./Page/InvoiceDocument`|
    > |<span data-ttu-id="775fd-137">OData V4</span><span class="sxs-lookup"><span data-stu-id="775fd-137">OData V4</span></span>|`https://api.businesscentral.dynamics.com/*version*/*tenant*/Production/ODataV4/Company('*CompanyName*')/*entity*`|`https://api.businesscentral.dynamics.com/v2.0/7acc9d3d-d354-4616-8bbd-c4fc9f2b15b3/Production/ODataV4/Company('CRONUS%20USA%2C%20Inc.')/InvoiceDocument`<br/>    <span data-ttu-id="775fd-138">El nombre de la empresa distingue entre mayúsculas y minúsculas.</span><span class="sxs-lookup"><span data-stu-id="775fd-138">The company name is case-sensitive.</span></span>|

2. <span data-ttu-id="775fd-139">Revise la información que se muestra en el explorador.</span><span class="sxs-lookup"><span data-stu-id="775fd-139">Review the information that is displayed in the browser.</span></span> <span data-ttu-id="775fd-140">Compruebe que puede ver el nombre del servicio web que ha creado.</span><span class="sxs-lookup"><span data-stu-id="775fd-140">Verify that you can see the name of the web service that you have created.</span></span>  

<span data-ttu-id="775fd-141">Cuando obtiene acceso a un servicio web, y desea escribir datos de nuevo en [!INCLUDE[prod_short](includes/prod_short.md)], debe especificar el nombre de la empresa.</span><span class="sxs-lookup"><span data-stu-id="775fd-141">When you access a web service, and you want to write data back to [!INCLUDE[prod_short](includes/prod_short.md)], you must specify the company name.</span></span> <span data-ttu-id="775fd-142">Puede especificar la empresa como parte del URI como se muestra en los ejemplos o bien; alternativamente, puede especificar la empresa como parte de los parámetros de consulta.</span><span class="sxs-lookup"><span data-stu-id="775fd-142">You can specify the company as part of the URI as shown in the examples; alternatively, specify the company as part of the query parameters.</span></span> <span data-ttu-id="775fd-143">Por ejemplo, los URI siguientes señalan al mismo servicio web de OData y ambos son URI válidos.</span><span class="sxs-lookup"><span data-stu-id="775fd-143">For example, the following URIs point to the same OData web service and are both valid URIs.</span></span>  

```
https://api.businesscentral.dynamics.com/v1.0/OData/Company('CRONUS International Ltd.')/Customer  
```

```
https://api.businesscentral.dynamics.com/v1.0/OData/Customer?company='CRONUS International Ltd.'  
```

## <a name="see-also"></a><span data-ttu-id="775fd-144">Consulte también</span><span class="sxs-lookup"><span data-stu-id="775fd-144">See Also</span></span>

[<span data-ttu-id="775fd-145">Administración</span><span class="sxs-lookup"><span data-stu-id="775fd-145">Administration</span></span>](admin-setup-and-administration.md)  
[<span data-ttu-id="775fd-146">Servicios web de Business Central para desarrolladores</span><span class="sxs-lookup"><span data-stu-id="775fd-146">Business Central Web Services for developers</span></span>](/dynamics365/business-central/dev-itpro/webservices/web-services)  
[<span data-ttu-id="775fd-147">Límites de solicitud de OData</span><span class="sxs-lookup"><span data-stu-id="775fd-147">OData request limits</span></span>](/dynamics365/business-central/dev-itpro/administration/operational-limits-online#ODataServices)  


[!INCLUDE[footer-include](includes/footer-banner.md)]