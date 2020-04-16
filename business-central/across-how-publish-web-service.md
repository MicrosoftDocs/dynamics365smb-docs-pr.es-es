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
# <a name="publish-a-web-service"></a>Publicar un servicio web

Los servicios web son una forma ligera para hacer que la funcionalidad de la aplicación esté disponible para una variedad de sistemas externos y usuarios. [!INCLUDE[d365fin](includes/d365fin_md.md)] incluye un número de objetos que se exponen como servicios Web de forma predeterminada debido a la integración con otros servicios de Microsoft, pero también puede agregar otros servicios Web.  

Configure un servicio web en el cliente de [!INCLUDE[d365fin](includes/d365fin_md.md)]. A continuación debe publicar el servicio web para ponerlo a disposición de las solicitudes de servicio en la red. Los usuarios pueden descubrir servicios Web seleccionando un navegador en la ubicación del servidor y solicitando una lista de servicios disponibles. Al publicar un servicio web, estará disponible inmediatamente a través de la red para los usuarios autenticados. Todo los usuarios autorizados pueden tener acceso a los metadatos de los servicios Web, pero solo los usuarios con permisos suficientes pueden tener acceso a los datos reales.

## <a name="creating-and-publishing-a-web-service"></a>Crear y publicar un servicio web  
Los pasos siguientes explican cómo crear y publicar un servicio web.  

### <a name="to-create-and-publish-a-web-service"></a>Para crear y publicar un servicio web  

1. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Servicios web** y luego elija el enlace relacionado.  
2. En la página **Servicios web**, elija **Nuevo**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

    > [!NOTE]  
    > **Codeunit** y **Página** son tipos válidos para los servicios web de SOAP. **Página** y **Consulta** son tipos válidos para los servicios web de OData.  
    > También, si la base de datos contiene varias empresas, puede elegir un Id. objeto que sea específico de una de las empresas.  
    > Finalmente, el nombre del servicio está visible a los consumidores de su servicio Web y es la base para identificar y distinguir servicios Web, por lo que debería hacer que el nombre tenga sentido.

3. Activa la casilla en la columna **Publicado**.  

Al publicar el servicio web, en los campos **URL de OData** y **URL de SOAP**, puede ver las direcciones URL que se generan para el servicio web. Puede probar el servicio web inmediatamente eligiendo los vínculos de los campos **URL de OData** y **URL de SOAP**. Opcionalmente, puede copiar el valor del campo y guardarlo para su uso posterior.  

> [!IMPORTANT]
> Para las codeunits que se publican como un servicio web SOAP, los métodos expuestos en la codeunit deben estar marcados como `[External]` como en el código.

Una vez publique un servicio Web, está disponible a partes externas. Puede verificar la disponibilidad del servicio web con un explorador o bien, puede elegir el vínculo de los campos **URL de OData** y **URL de SOAP** en la página **Servicios web**. El procedimiento siguiente muestra cómo puede comprobar la disponibilidad del servicio web para uso posterior.  

### <a name="to-verify-the-availability-of-a-web-service"></a>Para verificar la disponibilidad de un servicio web  

1. En el explorador, escriba la dirección URL correspondiente. La tabla siguiente muestra los tipos de direcciones URL que puede introducir para distintos tipos de servicio web.  

    > [!div class="mx-tdBreakAll"]
    > |Escriba|Sintaxis|Ejemplo:|
    > |----------------|------|-------|
    > |SOAP|https://api.businesscentral.dynamics.com/*versión*/*suscriptor*/Production/WS/*NombreEmpresa*/*entidad*/ |https://api.businesscentral.dynamics.com/v2.0/7acc9d3d-d354-4616-8bbd-c4fc9f2b15b3/Production/WS/CRONUS%20USA%2C%20Inc./Page/InvoiceDocument|
    > |OData V4|https://api.businesscentral.dynamics.com/*versión*/*suscriptor*/Production/ODataV4/Company('*NombreEmpresa*')/*entidad*|https://api.businesscentral.dynamics.com/v2.0/7acc9d3d-d354-4616-8bbd-c4fc9f2b15b3/Production/ODataV4/Company('CRONUS%20Estados Unidos%2C%20Inc.')/InvoiceDocument<br/>    El nombre de la empresa distingue entre mayúsculas y minúsculas.|

2. Revise la información que se muestra en el explorador. Compruebe que puede ver el nombre del servicio web que ha creado.  

Cuando obtiene acceso a un servicio web, y desea escribir datos de nuevo en [!INCLUDE[d365fin](includes/d365fin_md.md)], debe especificar el nombre de la empresa. Puede especificar la empresa como parte del URI como se muestra en los ejemplos o bien, puede especificar la empresa como parte de los parámetros de consulta. Por ejemplo, los URI siguientes señalan al mismo servicio web de OData y ambos son URI válidos.  

```
https://api.businesscentral.dynamics.com/v1.0/OData/Company('CRONUS International Ltd.')/Customer  
```

```
https://api.businesscentral.dynamics.com/v1.0/OData/Customer?company='CRONUS International Ltd.'  
```

## <a name="see-also"></a>Consulte también

[Administración](admin-setup-and-administration.md)  
[Servicios web de Business Central para desarrolladores](/dynamics365/business-central/dev-itpro/webservices/web-services)  
