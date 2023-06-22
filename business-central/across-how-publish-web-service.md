---
title: Exponer los objetos como servicios web
description: Publique los objetos como servicios web para estén disponibles inmediatamente para la solución Business Central.
author: edupont04
ms.topic: conceptual
ms.search.form: 810
ms.date: 04/01/2021
ms.author: edupont
---
# <a name="publish-a-web-service" />Publicar un servicio web

Los servicios web son una forma ligera para hacer que la funcionalidad de la aplicación esté disponible en distintas clases de sistemas externos y usuarios. Por defecto, [!INCLUDE[prod_short](includes/prod_short.md)] expone una serie de objetos, como servicios web, para una mejor integración con otros servicios de Microsoft. Puede agregar otros servicios web según lo requiera su empresa.  

Configure un servicio web en [!INCLUDE[prod_short](includes/prod_short.md)] y luego publique el servicio web para que esté disponible para los usuarios autenticados. Todo los usuarios autorizados pueden tener acceso a los metadatos de los servicios Web, pero solo los usuarios con permisos suficientes pueden tener acceso a los datos reales.  

## <a name="creating-and-publishing-a-web-service" />Crear y publicar un servicio web

Los pasos siguientes explican cómo crear y publicar un servicio web.  

### <a name="to-create-and-publish-a-web-service" />Para crear y publicar un servicio web

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Servicios web** y luego elija el enlace relacionado.  
2. En la página **Servicios web**, elija **Nuevo**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

    > [!NOTE]  
    > **Codeunit** y **Página** son tipos válidos para los servicios web de SOAP. **Página** y **Consulta** son tipos válidos para los servicios web de OData. A partir de la versión 16.3, **Codeunit** también es un tipo válido para los servicios web de OData v4, pero no se muestra ninguna URL en la interfaz de usuario. También, si la base de datos contiene varias empresas, puede elegir un Id. objeto que sea específico de una de las empresas.  
    > Finalmente, el nombre del servicio está visible a los consumidores de su servicio Web y es la base para identificar y distinguir servicios Web, por lo que debería hacer que el nombre tenga sentido.

3. Activa la casilla en la columna **Publicado**.  

Cuando publica el servicio web, los campos **URL de OData** y **URL de SOAP** muestran las nuevas URL. Sin embargo, para las codeunits que se exponen como acciones independientes de OData v4, los campos de URL no se muestran.  

Puede probar el servicio web inmediatamente eligiendo los vínculos de los campos **URL de OData** y **URL de SOAP**. Opcionalmente, copie el valor del campo y guárdelo para su uso posterior. Para probar las unidades de código que se exponen como acciones independientes de OData v4, siga las instrucciones de la sección [Verificación de la disponibilidad del servicio web](/dynamics365/business-central/dev-itpro/developer/devenv-creating-and-interacting-with-odatav4-unbound-action#verifying-web-service-availability) del contenido del desarrollador.

> [!NOTE]
> Si los objetos que expone como servicios web no deben ser accesibles desde [!INCLUDE[prod_short](includes/prod_short.md)] en línea, debe marcar los métodos expuestos en el código como `[Scope('OnPrem')]`. Para obtener más información, consulte [Ámbito de atributo](/dynamics365/business-central/dev-itpro/developer/methods/devenv-scope-attribute).

Una vez publique un servicio Web, está disponible a partes externas. Puede verificar la disponibilidad del servicio web con un explorador o bien, puede elegir el vínculo de los campos **URL de OData** y **URL de SOAP** en la página **Servicios web**. El procedimiento siguiente muestra cómo puede comprobar la disponibilidad del servicio web para uso posterior.  

### <a name="to-verify-the-availability-of-a-web-service" />Para verificar la disponibilidad de un servicio web

1. En el explorador, escriba la dirección URL correspondiente. La tabla siguiente muestra los tipos de direcciones URL que puede introducir para distintos tipos de servicio web.  

    > [!div class="mx-tdBreakAll"]
    > |Escriba|Sintaxis|Ejemplo:|
    > |----------------|------|-------|
    > |SOAP|`https://api.businesscentral.dynamics.com/*version*/*tenant*/Production/WS/*CompanyName*/*entity*/` |`https://api.businesscentral.dynamics.com/v2.0/7acc9d3d-d354-4616-8bbd-c4fc9f2b15b3/Production/WS/CRONUS%20USA%2C%20Inc./Page/InvoiceDocument`|
    > |OData V4|`https://api.businesscentral.dynamics.com/*version*/*tenant*/Production/ODataV4/Company('*CompanyName*')/*entity*`|`https://api.businesscentral.dynamics.com/v2.0/7acc9d3d-d354-4616-8bbd-c4fc9f2b15b3/Production/ODataV4/Company('CRONUS%20USA%2C%20Inc.')/InvoiceDocument`<br/>    El nombre de la empresa distingue entre mayúsculas y minúsculas.|

2. Revise la información que se muestra en el explorador. Compruebe que puede ver el nombre del servicio web que ha creado.  

Cuando obtiene acceso a un servicio web, y desea escribir datos de nuevo en [!INCLUDE[prod_short](includes/prod_short.md)], debe especificar el nombre de la empresa. Puede especificar la empresa como parte del URI como se muestra en los ejemplos o bien; alternativamente, puede especificar la empresa como parte de los parámetros de consulta. Por ejemplo, los URI siguientes señalan al mismo servicio web de OData y ambos son URI válidos.  

```
https://api.businesscentral.dynamics.com/v1.0/OData/Company('CRONUS International Ltd.')/Customer  
```

```
https://api.businesscentral.dynamics.com/v1.0/OData/Customer?company='CRONUS International Ltd.'  
```

## <a name="see-also" />Consulte también

[Administración](admin-setup-and-administration.md)  
[Servicios web de Business Central para desarrolladores](/dynamics365/business-central/dev-itpro/webservices/web-services)  
[Límites de solicitud de OData](/dynamics365/business-central/dev-itpro/administration/operational-limits-online#ODataServices)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
