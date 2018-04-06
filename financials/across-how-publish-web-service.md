---
title: Exponga los objetos como servicios Web | Documentos de Microsoft
description: "Publique objetos como servicios web para que estén inmediatamente disponibles en la red."
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 11/22/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: b34f276a764f0e828fbc1f015429df9852242a4c
ms.openlocfilehash: 428dc281d34c374940d0c3fd187dd8a1d3d3ad9b
ms.contentlocale: es-es
ms.lasthandoff: 03/22/2018

---
# <a name="publish-a-web-service"></a>Publicar un servicio web
Los servicios web son una forma ligera para hacer que la funcionalidad de la aplicación esté disponible para una variedad de sistemas externos y usuarios. [!INCLUDE[d365fin](includes/d365fin_md.md)] incluye un número de objetos que se exponen como servicios Web de forma predeterminada debido a la integración con otros servicios de Microsoft, pero también puede agregar otros servicios Web.  

Puede configurar un servicio Web del cliente Windows o en el cliente Web. A continuación debe publicar el servicio web para ponerlo a disposición de las solicitudes de servicio en la red. Los usuarios pueden descubrir servicios Web seleccionando un navegador en la ubicación del servidor y solicitando una lista de servicios disponibles. Al publicar un servicio web, estará disponible inmediatamente a través de la red para los usuarios autenticados. Todo los usuarios autorizados pueden tener acceso a los metadatos de los servicios Web, pero solo los usuarios con permisos suficientes pueden tener acceso a los datos reales.

## <a name="creating-and-publishing-a-web-service"></a>Crear y publicar un servicio web  
Los pasos siguientes explican cómo crear y publicar un servicio web.  

### <a name="to-create-and-publish-a-web-service"></a>Para crear y publicar un servicio web  

1.  Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), introduzca **Servicios Web** y, a continuación, seleccione el vínculo relacionado.  
2.  En la página **Servicios web**, elija **Nuevo**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

    > [!NOTE]  
    >  **Unidad de código** y **Página** son tipos válidos para los servicios web de SOAP. **Página** y **Consulta** son tipos válidos para los servicios web de OData.  
    También, si la base de datos contiene varias empresas, puede elegir un Id. objeto que sea específico de una de las empresas.  
    Finalmente, el nombre del servicio está visible a los consumidores de su servicio Web y es la base para identificar y distinguir servicios Web, por lo que debería hacer que el nombre tenga sentido.

3.  Activa la casilla en la columna **Publicado**.  

Al publicar el servicio web, en los campos **URL de OData** y **URL de SOAP**, puede ver las direcciones URL que se generan para el servicio web. Puede probar el servicio web inmediatamente eligiendo los vínculos de los campos **URL de OData** y **URL de SOAP**. Opcionalmente, puede copiar el valor del campo y guardarlo para su uso posterior.  

Una vez publique un servicio Web, está disponible a partes externas. Puede verificar la disponibilidad del servicio web con un explorador o bien, puede elegir el vínculo de los campos **URL de OData** y **URL de SOAP** en la ventana **Servicios web**. El procedimiento siguiente muestra cómo puede comprobar la disponibilidad del servicio web para uso posterior.  

### <a name="to-verify-the-availability-of-a-web-service"></a>Para verificar la disponibilidad de un servicio web  

1.  En el explorador, escriba la dirección URL correspondiente. La tabla siguiente muestra los tipos de direcciones URL que puede introducir para distintos tipos de servicio web.  
> [!div class="mx-tdBreakAll"]
> |Tipo|Sintaxis|Ejemplo|
> |----------------|------|-------|
> |SOAP |https://*Servidor*:*PuertoServicioWebSOAP*/*InstanciaDeServidor*/WS/*NombreEmpresa*/documentosVentas/ |https://mycompany.financials.dynamics.com:7047/MS/WS/MyCompany/Page/salesDocuments?tenant=mycompany.financials.dynamics.com |
> |OData |https://*Servidor*:*PuertoServicioWebOData*/*InstanciaServidor*/OData/Empresa(*'NombreEmpresa*')|[https://MyCompany.financials.dynamics.com:7048/MS/OData/Company('MyCompany')/salesDocuments?tenant=MyCompany.financials.dynamics.com](https://MyCompany.financials.dynamics.com:7048/MS/OData/Company('MyCompany')/salesDocuments?tenant=MyCompany.financials.dynamics.com) <br />    El nombre de la empresa distingue entre mayúsculas y minúsculas.|

2.  Revise la información que se muestra en el explorador. Compruebe que puede ver el nombre del servicio web que ha creado.  

Cuando obtiene acceso a un servicio web, y desea escribir datos de nuevo en [!INCLUDE[d365fin](includes/d365fin_md.md)], debe especificar el nombre de la empresa. Puede especificar la empresa como parte del URI como se muestra en los ejemplos o bien, puede especificar la empresa como parte de los parámetros de consulta. Por ejemplo, los URI siguientes señalan al mismo servicio web de OData y ambos son URI válidos.  

```  
https://localhost:7048/server/OData/Company('CRONUS International Ltd.')/Customer  
```  

```  
https://localhost:7048/server/OData/Customer?company='CRONUS International Ltd.'  
```  

## <a name="see-also"></a>Consulte también  
[Configuración y administración](admin-setup-and-administration.md)  

