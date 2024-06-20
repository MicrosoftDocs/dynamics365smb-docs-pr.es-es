---
title: Usar los datos para crear una aplicación | Documentos de Microsoft
description: Puede hacer que los datos de Business Central estén disponibles como un origen de datos y especificar una URL de OData de sus servicios web para crear una aplicación empresarial con Power Apps.
author: jswymer
ms.topic: conceptual
ms.service: dynamics-365-business-central
ms.search.keywords: 'OData, Power App, SOAP'
ms.date: 05/15/2023
ms.author: jswymer
ms.reviewer: jswymer
---
# <a name="connecting-to-your-business-central-data-to-build-a-business-app-using-power-apps"></a>Cómo conectarse a sus datos de Business Central para crear una aplicación empresarial con Power Apps

Puede convertir los datos de [!INCLUDE[prod_short](includes/prod_short.md)] en disponibles como origen de datos en Power Apps.  

> [!TIP]  
> Business Central ahora ofrece soporte de desarrollo y operaciones para Power Platform en AL-Go y muestras para que pueda comenzar a crear sus propias aplicaciones Power Apps. Estas características se encuentran actualmente en versión preliminar. Para obtener más información, vaya a [Business Central y Power Apps](/dynamics365/business-central/dev-itpro/powerplatform/power-apps-overview) en la ayuda para desarrolladores y profesionales de TI.

## <a name="prerequisites"></a>Requisitos previos

Debe disponer de una cuenta válida con [!INCLUDE[prod_short](includes/prod_short.md)] y con Power Apps.  

## <a name="add--as-a-data-source-in-power-apps"></a>Agregar [!INCLUDE[prod_short](includes/prod_short.md)] como origen de datos de Power Apps

Estos pasos agregan una tabla de Business Central, como clientes o artículos, como fuente de datos de una aplicación Power Apps.

1. En el explorador, vaya a [powerapps.microsoft.com](https://powerapps.microsoft.com/) y, a continuación, inicie sesión.
2. En el panel de navegación del lado izquierdo, seleccione **+ Crear** y luego seleccione **Más fuentes de datos** en la paçgina **Crear aplicación**.
  
   <!-- This step opens Power Apps canavs. On first sign-in, you must specify the country/region.  -->
3. La lista **Conexiones** muestra las conexiones de datos existentes que tiene.

   - Si ya existe una conexión **Business Central**, selecciónela y luego seleccione **Crear**.

   - Si no ve una conexión de Business Central, seleccione **+ Nueva conexión**, busque y seleccione **Business Central** y luego seleccione **Crear**.

   > [!NOTE]
   > Si desea conectarse a [!INCLUDE[prod_short](includes/prod_short.md)] local, deberá elegir el conector **Business Central (local)**.  
  
4. Power Apps se conecta a su [!INCLUDE[prod_short](includes/prod_short.md)]. Inicie sesión con la cuenta y contrraseña de Business Central. Si no es administrador de su [!INCLUDE[prod_short](includes/prod_short.md)], es posible que tenga que iniciar sesión con otra cuenta.  
5. Una vez iniciada la sesión, Power Apps muestra una lista de *ambientes y empresas* que están disponibles en [!INCLUDE[prod_short](includes/prod_short.md)]. Elija el entorno y la empresa que contiene los datos a los que desea conectarse, como *PRODUCCIÓN - Mi empresa*.  
6. A continuación, se le presenta una lista de tablas que están expuestas como parte de la API para su entorno. Seleccione la tabla a la que desea conectarse y luego elija **Conectar**.

Estas denominadas tablas están expuestas como extremos por el contector [!INCLUDE[prod_short](includes/prod_short.md)] para Power Apps.  

> [!NOTE]
> Si desea incluir datos de otras tablas de [!INCLUDE[prod_short](includes/prod_short.md)] en su aplicación, debe trabajar con un desarrollador para definir una API personalizada en [!INCLUDE[prod_short](includes/prod_short.md)].  

Ya se ha conectado correctamente con los datos de [!INCLUDE[prod_short](includes/prod_short.md)] y está preparado para comenzar a crear su Power App. Siempre puede agregar más pantallas y conectarse a más datos. Más información en [Crear una aplicación de lienzo a partir de un ejemplo en Power Apps](/powerapps/maker/canvas-apps/open-and-run-a-sample-app).  

Cuando haya diseñado y creado la aplicación, puede compartirla con sus compañeros. Para obtener más información, consulte [Guardar y publicar una aplicación de lienzo en Power Apps](/powerapps/maker/canvas-apps/save-publish-app).  

<!--
## <a name="sample-apps-to-get-started"></a>Sample apps to get started

As a preview version, Business Central offers several sample apps that you can use as a starting point for building your own apps that use Business Central data. These sample apps are available in the [Business Central Demos](https://github.com/BusinessCentralDemos) repo on GitHub. For a quick overview on the apps, go to [Power Apps samples for Business Central](/dynamics365/business-central/dev-itpro/powerplatform/power-apps-samples).

## <a name="develop-and-maintain-apps-application-lifecycle-management"></a>Develop and maintain apps application lifecycle management

As an app developer, you may already be familiar with Business Central AL-Go. AL-Go is set of tools on GiHub that enables you to maintain professional DevOps processes for your Business Central AL projects. AL-Go supports source control and activities, like building, testing, and deploying. As a preview, Business Central now offers an Al-Go version that supports for Power Platform solutions. The preview, for example, includes workflows that let you push and pull Power Platfrom changes to and from enviroments. You can access the tools at [https://github.com/BusinessCentralDemos/AL-Go-PTE](https://github.com/BusinessCentralDemos/AL-Go-PTE). For more information, see [Application lifecycle management for Power Apps in Business Central](/dynamics365/business-central/dev-itpro/powerplatform/power-apps-alm).-->

## <a name="see-also"></a>Consulte también .

[Crear una aplicación de lienzo a partir de una plantilla de Power Apps](/powerapps/maker/canvas-apps/get-started-test-drive)  
[Importar datos de empresa de otros sistemas financieros](across-import-data-configuration-packages.md)  
[Configurar [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md)  
[Introducción al desarrollo de aplicaciones de Connect para Dynamics 365 Business Central](/dynamics365/business-central/dev-itpro/developer/devenv-develop-connect-apps)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
