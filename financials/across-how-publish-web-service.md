---
title: Exponga los objetos como servicios Web | Documentos de Microsoft
description: "Publique [!INCLUDE[d365fin](includes/d365fin_md.md)] los objetos como servicios Web, están inmediatamente disponibles en la red."
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/01/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 278515fc479a72957fb52dad71ce2f98d354ee32
ms.contentlocale: es-es
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-publish-a-web-service"></a><span data-ttu-id="98c63-103">Procedimiento: crear y publicar un servicio web</span><span class="sxs-lookup"><span data-stu-id="98c63-103">How to: Publish a Web Service</span></span>
<span data-ttu-id="98c63-104">Los servicios web son una forma ligera para hacer que la funcionalidad de la aplicación esté disponible para una variedad de sistemas externos y usuarios.</span><span class="sxs-lookup"><span data-stu-id="98c63-104">Web services are a lightweight way to make application functionality available to a variety of external systems and users.</span></span> [!INCLUDE[d365fin](includes/d365fin_md.md)]<span data-ttu-id="98c63-105"> incluye un número de objetos que se exponen como servicios Web de forma predeterminada debido a la integración con otros servicios de Microsoft, pero también puede agregar otros servicios Web.</span><span class="sxs-lookup"><span data-stu-id="98c63-105"> includes an number of objects that are exposed as web services by default due to integration with other Microsoft services, but you can also add other web services.</span></span>  

<span data-ttu-id="98c63-106">Puede configurar un servicio Web del cliente Windows o en el cliente Web.</span><span class="sxs-lookup"><span data-stu-id="98c63-106">You can set up a web service in the Windows client or in the Web client.</span></span> <span data-ttu-id="98c63-107">A continuación debe publicar el servicio web para ponerlo a disposición de las solicitudes de servicio en la red.</span><span class="sxs-lookup"><span data-stu-id="98c63-107">You must then publish the web service so that it is available to service requests over the network.</span></span> <span data-ttu-id="98c63-108">Los usuarios pueden descubrir servicios Web seleccionando un navegador en la ubicación del servidor y solicitando una lista de servicios disponibles.</span><span class="sxs-lookup"><span data-stu-id="98c63-108">Users can discover web services by pointing a browser at the server location and requesting a list of available services.</span></span> <span data-ttu-id="98c63-109">Al publicar un servicio web, estará disponible inmediatamente a través de la red para los usuarios autenticados.</span><span class="sxs-lookup"><span data-stu-id="98c63-109">When you publish a web service, it is immediately available over the network for authenticated users.</span></span> <span data-ttu-id="98c63-110">Todo los usuarios autorizados pueden tener acceso a los metadatos de los servicios Web, pero solo los usuarios con permisos suficientes pueden tener acceso a los datos reales.</span><span class="sxs-lookup"><span data-stu-id="98c63-110">All authorized users can access metadata for web services, but only users who have sufficient permissions can access actual data.</span></span>

## <a name="creating-and-publishing-a-web-service"></a><span data-ttu-id="98c63-111">Crear y publicar un servicio web</span><span class="sxs-lookup"><span data-stu-id="98c63-111">Creating and Publishing a Web Service</span></span>  
 <span data-ttu-id="98c63-112">Los pasos siguientes explican cómo crear y publicar un servicio web.</span><span class="sxs-lookup"><span data-stu-id="98c63-112">The following steps explain how to create and publish a web service.</span></span>  

#### <a name="to-create-and-publish-a-web-service"></a><span data-ttu-id="98c63-113">Para crear y publicar un servicio web</span><span class="sxs-lookup"><span data-stu-id="98c63-113">To create and publish a web service</span></span>  

1.  <span data-ttu-id="98c63-114">Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), introduzca **Servicios Web** y, a continuación, seleccione el vínculo relacionado.</span><span class="sxs-lookup"><span data-stu-id="98c63-114">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Web Services**, and then choose the related link.</span></span>  

2.  <span data-ttu-id="98c63-115">En la página **Servicios web**, elija **Nuevo**.</span><span class="sxs-lookup"><span data-stu-id="98c63-115">In the **Web Services** page, choose **New**.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

    > [!NOTE]  
    >  <span data-ttu-id="98c63-116">**Unidad de código** y **Página** son tipos válidos para los servicios web de SOAP.</span><span class="sxs-lookup"><span data-stu-id="98c63-116">**Codeunit** and **Page** are valid types for SOAP web services.</span></span> <span data-ttu-id="98c63-117">**Página** y **Consulta** son tipos válidos para los servicios web de OData.</span><span class="sxs-lookup"><span data-stu-id="98c63-117">**Page** and **Query** are valid types for OData web services.</span></span>  
    <span data-ttu-id="98c63-118">También, si la base de datos contiene varias empresas, puede elegir un Id. objeto que sea específico de una de las empresas.</span><span class="sxs-lookup"><span data-stu-id="98c63-118">Also, if the database contains multiple companies, you can choose an object ID that is specific to one of the companies.</span></span>  
    <span data-ttu-id="98c63-119">Finalmente, el nombre del servicio está visible a los consumidores de su servicio Web y es la base para identificar y distinguir servicios Web, por lo que debería hacer que el nombre tenga sentido.</span><span class="sxs-lookup"><span data-stu-id="98c63-119">Finally, the service name is visible to consumers of your web service and is the basis for identifying and distinguishing web services, so you should make the name meaningful.</span></span>

3.  <span data-ttu-id="98c63-120">Activa la casilla en la columna **Publicado**.</span><span class="sxs-lookup"><span data-stu-id="98c63-120">Select the check box in the **Published** column.</span></span>  

     <span data-ttu-id="98c63-121">Al publicar el servicio web, en los campos **URL de OData** y **URL de SOAP**, puede ver las direcciones URL que se generan para el servicio web.</span><span class="sxs-lookup"><span data-stu-id="98c63-121">When you publish the web service, in the **OData URL** and **SOAP URL** fields, you can see the URLs that are generated for the web service.</span></span> <span data-ttu-id="98c63-122">Puede probar el servicio web inmediatamente eligiendo los vínculos de los campos **URL de OData** y **URL de SOAP**.</span><span class="sxs-lookup"><span data-stu-id="98c63-122">You can test the web service immediately by choosing the links in the **OData URL** and **SOAP URL** fields.</span></span> <span data-ttu-id="98c63-123">Opcionalmente, puede copiar el valor del campo y guardarlo para su uso posterior.</span><span class="sxs-lookup"><span data-stu-id="98c63-123">Optionally, you can copy the value of the field and save it for later use.</span></span>  

<span data-ttu-id="98c63-124">Una vez publique un servicio Web, está disponible a partes externas.</span><span class="sxs-lookup"><span data-stu-id="98c63-124">After you publish a web service, it is available to external parties.</span></span> <span data-ttu-id="98c63-125">Puede verificar la disponibilidad del servicio web con un explorador o bien, puede elegir el vínculo de los campos **URL de OData** y **URL de SOAP** en la ventana **Servicios web**.</span><span class="sxs-lookup"><span data-stu-id="98c63-125">You can verify the availability of that web service by using a browser, or you can choose the link in the **OData URL** and **SOAP URL** fields in the **Web Services** window.</span></span> <span data-ttu-id="98c63-126">El procedimiento siguiente muestra cómo puede comprobar la disponibilidad del servicio web para uso posterior.</span><span class="sxs-lookup"><span data-stu-id="98c63-126">The following procedure illustrates how you can verify the availability of the web service for later use.</span></span>  

#### <a name="to-verify-the-availability-of-a-web-service"></a><span data-ttu-id="98c63-127">Para verificar la disponibilidad de un servicio web</span><span class="sxs-lookup"><span data-stu-id="98c63-127">To verify the availability of a web service</span></span>  

1.  <span data-ttu-id="98c63-128">En el explorador, escriba la dirección URL correspondiente.</span><span class="sxs-lookup"><span data-stu-id="98c63-128">In your browser, enter the relevant URL.</span></span> <span data-ttu-id="98c63-129">La tabla siguiente muestra los tipos de direcciones URL que puede introducir.</span><span class="sxs-lookup"><span data-stu-id="98c63-129">The following table illustrates the types of URLs that you can enter.</span></span> <span data-ttu-id="98c63-130">Para los servicios web SOAP, utilice el formato siguiente para el URI.</span><span class="sxs-lookup"><span data-stu-id="98c63-130">For SOAP web services, use the following format for your URI.</span></span>  

    <table>
    <tr>
    <th><span data-ttu-id="98c63-131">Tipo de servicio web</span><span class="sxs-lookup"><span data-stu-id="98c63-131">Web service type</span></span></th>
    <th><span data-ttu-id="98c63-132">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="98c63-132">Syntax</span></span></th>
    <th><span data-ttu-id="98c63-133">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="98c63-133">Example</span></span></th>
    </tr>
    <tr>
    <td><span data-ttu-id="98c63-134">SOAP</span><span class="sxs-lookup"><span data-stu-id="98c63-134">SOAP</span></span></td>
    <td><span data-ttu-id="98c63-135">https://*Servidor*:*PuertoServicioWebSOAP*/*InstanciaDeServidor*/WS/*NombreEmpresa*/documentosVentas/</span><span class="sxs-lookup"><span data-stu-id="98c63-135">https://*Server*:*SOAPWebServicePort*/*ServerInstance*/WS/*CompanyName*/salesDocuments/</span></span></td>
    <td><span data-ttu-id="98c63-136">https://mycompany.financials.dynamics.com:7047/MS/WS/MyCompany/Page/salesDocuments?tenant=mycompany.financials.dynamics.com</span><span class="sxs-lookup"><span data-stu-id="98c63-136">https://mycompany.financials.dynamics.com:7047/MS/WS/MyCompany/Page/salesDocuments?tenant=mycompany.financials.dynamics.com</span></span></td>
    </tr>
    <tr>
    <td><span data-ttu-id="98c63-137">OData</span><span class="sxs-lookup"><span data-stu-id="98c63-137">OData</span></span></td>
    <td><span data-ttu-id="98c63-138">https://*Servidor*:*PuertoServicioWebOData*/*InstanciaServidor*/OData/Empresa(*'NombreEmpresa*')</span><span class="sxs-lookup"><span data-stu-id="98c63-138">https://*Server*:*ODataWebServicePort*/*ServerInstance*/OData/Company('*CompanyName*')</span></span></td>
    <td><span data-ttu-id="98c63-139">https://MyCompany.financials.dynamics.com:7048/MS/OData/Company('MyCompany')/salesDocuments?tenant=MyCompany.financials.dynamics.com</span><span class="sxs-lookup"><span data-stu-id="98c63-139">https://MyCompany.financials.dynamics.com:7048/MS/OData/Company('MyCompany')/salesDocuments?tenant=MyCompany.financials.dynamics.com</span></span>

         The company name is case-sensitive.</td>
    </tr>
    </table>

2.  <span data-ttu-id="98c63-140">Revise la información que se muestra en el explorador.</span><span class="sxs-lookup"><span data-stu-id="98c63-140">Review the information that is displayed in the browser.</span></span> <span data-ttu-id="98c63-141">Compruebe que puede ver el nombre del servicio web que ha creado.</span><span class="sxs-lookup"><span data-stu-id="98c63-141">Verify that you can see the name of the web service that you have created.</span></span>  

 <span data-ttu-id="98c63-142">Cuando obtiene acceso a un servicio web, y desea escribir datos de nuevo en [!INCLUDE[d365fin](includes/d365fin_md.md)], debe especificar el nombre de la empresa.</span><span class="sxs-lookup"><span data-stu-id="98c63-142">When you access a web service, and you want to write data back to [!INCLUDE[d365fin](includes/d365fin_md.md)], you must specify the company name.</span></span> <span data-ttu-id="98c63-143">Puede especificar la empresa como parte del URI como se muestra en los ejemplos o bien, puede especificar la empresa como parte de los parámetros de consulta.</span><span class="sxs-lookup"><span data-stu-id="98c63-143">You can specify the company as part of the URI as shown in the examples, or you can specify the company as part of the query parameters.</span></span> <span data-ttu-id="98c63-144">Por ejemplo, los URI siguientes señalan al mismo servicio web de OData y ambos son URI válidos.</span><span class="sxs-lookup"><span data-stu-id="98c63-144">For example, the following URIs point to the same OData web service and are both valid URIs.</span></span>  

```  
https://localhost:7048/server/OData/Company('CRONUS International Ltd.')/Customer  
```  

```  
https://localhost:7048/server/OData/Customer?company='CRONUS International Ltd.'  
```  

## <a name="see-also"></a><span data-ttu-id="98c63-145">Consulte también</span><span class="sxs-lookup"><span data-stu-id="98c63-145">See Also</span></span>  
[<span data-ttu-id="98c63-146">Configuración y Administración en Dynamics 365 for Financials</span><span class="sxs-lookup"><span data-stu-id="98c63-146">Setup and Administration in Dynamics 365 for Financials</span></span>](admin-setup-and-administration.md)  

