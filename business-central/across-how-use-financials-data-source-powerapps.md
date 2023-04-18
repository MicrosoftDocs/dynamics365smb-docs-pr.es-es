---
title: Usar los datos para crear una aplicación | Documentos de Microsoft
description: Puede hacer que los datos de Business Central estén disponibles como un origen de datos y especificar una URL de OData de sus servicios web para crear una aplicación empresarial con Power Apps.
author: jswymer
ms.topic: conceptual
ms.service: dynamics365-business-central
ms.search.keywords: 'OData, Power App, SOAP'
ms.date: 04/01/2023
ms.author: jswymer
---
# Cómo conectarse a sus datos de Business Central para crear una aplicación empresarial con Power Apps

Puede convertir los datos de [!INCLUDE[prod_short](includes/prod_short.md)] en disponibles como origen de datos en Power Apps.  

> [!TIP]  
> La documentación adicional de Power Apps y nuestras muestras de Power App presentadas durante el Evento de lanzamiento de [!INCLUDE[prod_short](includes/prod_short.md)] se publicarán aquí más adelante en la ola 1 de 2023. Obtenga más información en [Empezar con más plantillas de muestra Power Automate y Power Apps](/dynamics365/release-plan/2023wave1/smb/dynamics365-business-central/get-started-more-sample-power-automate-templates-power-apps).

## Requisitos previos

Debe disponer de una cuenta válida con [!INCLUDE[prod_short](includes/prod_short.md)] y con Power Apps.  

## Agregar [!INCLUDE[prod_short](includes/prod_short.md)] como origen de datos de Power Apps

1. En el explorador, vaya a [powerapps.microsoft.com](https://powerapps.microsoft.com/) y, a continuación, inicie sesión.
2. En la página de inicio, en la sección **Comenzar a partir de los datos**, elija la ventana **Otros orígenes de datos**.  

    Este paso abre Power Apps Studio. En el primer inicio de sesión, debe especificar el país o la región.  
3. En la lista de conexiones disponibles, elija **Business Central** y, después, seleccione el botón **Crear**.

    Power Apps se conectará a su [!INCLUDE[prod_short](includes/prod_short.md)] con las credenciales con las que ha iniciado sesión. Si no es administrador de su [!INCLUDE[prod_short](includes/prod_short.md)], es posible que tenga que iniciar sesión con otra cuenta.  

4. Power Apps mostrará una lista de *ambientes y empresas* que están disponibles en [!INCLUDE[prod_short](includes/prod_short.md)]. Elija el entorno y la empresa que contiene los datos a los que desea conectarse, como *PRODUCCIÓN - Mi empresa*.  

5. A continuación, se le presentará una lista de tablas que están expuestas como parte de la API para su entorno. Seleccione la tabla a la que desea conectarse y luego elija **Conectar**.

Estas denominadas tablas están expuestas como extremos por el contector [!INCLUDE[prod_short](includes/prod_short.md)] para Power Apps.  

> [!NOTE]
> Si desea incluir datos de otras tablas de [!INCLUDE[prod_short](includes/prod_short.md)] en su aplicación, debe trabajar con un desarrollador para definir una API personalizada en [!INCLUDE[prod_short](includes/prod_short.md)].  

Ya se ha conectado correctamente con los datos de [!INCLUDE[prod_short](includes/prod_short.md)] y está preparado para comenzar a crear su Power App. Puede agregar más pantallas y conectarse a más datos desde su [!INCLUDE[prod_short](includes/prod_short.md)]. Para obtener más información, consulte [Crear una aplicación de lienzo a partir de un ejemplo en Power Apps](/powerapps/maker/canvas-apps/open-and-run-a-sample-app).  

Cuando haya diseñado y creado la aplicación, puede compartirla con sus compañeros. Para obtener más información, consulte [Guardar y publicar una aplicación de lienzo en Power Apps](/powerapps/maker/canvas-apps/save-publish-app).  

> [!NOTE]
> Si desea conectarse a [!INCLUDE[prod_short](includes/prod_short.md)] local, deberá elegir el conector **Business Central (local)** en el paso 3.  

## Consultar la [formación de Microsoft](/training/paths/power-apps-power-automate-business-central/) relacionada

## Consulte también .

[Crear una aplicación de lienzo a partir de una plantilla de Power Apps](/powerapps/maker/canvas-apps/get-started-test-drive)  
[Importar datos de empresa de otros sistemas financieros](across-import-data-configuration-packages.md)  
[Configurar [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md)  
[Introducción al desarrollo de aplicaciones de Connect para Dynamics 365 Business Central](/dynamics365/business-central/dev-itpro/developer/devenv-develop-connect-apps)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
