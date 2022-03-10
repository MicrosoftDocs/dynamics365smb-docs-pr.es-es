---
title: Usar los datos para crear una aplicación | Documentos de Microsoft
description: Puede hacer que los datos de Business Central estén disponibles como un origen de datos y especificar una URL de OData de sus servicios web para crear una aplicación empresarial con Power Apps.
author: edupont04
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: OData, Power App, SOAP
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 75dbc465373843327c4ff1c4a8563452d3464d94
ms.sourcegitcommit: ef80c461713fff1a75998766e7a4ed3a7c6121d0
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 02/15/2022
ms.locfileid: "8133309"
---
# <a name="connecting-to-your-business-central-data-to-build-a-business-app-using-power-apps"></a>Cómo conectarse a sus datos de Business Central para crear una aplicación empresarial con Power Apps

Puede convertir los datos de [!INCLUDE[prod_short](includes/prod_short.md)] en disponibles como origen de datos en Power Apps.  

> [!NOTE]  
> Debe disponer de una cuenta válida con [!INCLUDE[prod_short](includes/prod_short.md)] y con Power Apps.  

## <a name="to-add-prod_short-as-a-data-source-in-power-apps"></a>Para agregar [!INCLUDE[prod_short](includes/prod_short.md)] como origen de datos de Power Apps

1. En el explorador, vaya a [powerapps.microsoft.com](https://powerapps.microsoft.com/) y, a continuación, inicie sesión.
2. En la página de inicio, en la sección **Comenzar a partir de los datos**, elija la ventana **Otros orígenes de datos**.  

    Esto abre Power Apps Studio. En el primer inicio de sesión, debe especificar el país y la región.  
3. En la lista de conexiones disponibles, elija **Business Central** y, después, seleccione el botón **Crear**.

    Power Apps se conectará a su [!INCLUDE[prod_short](includes/prod_short.md)] con las credenciales con las que ha iniciado sesión. Si no es administrador de su [!INCLUDE[prod_short](includes/prod_short.md)], es posible que tenga que iniciar sesión con otra cuenta.  

4. Power Apps mostrará una lista de *ambientes y empresas* que están disponibles en [!INCLUDE[prod_short](includes/prod_short.md)]. Elija el entorno y la empresa que contiene los datos a los que desea conectarse, como *PRODUCCIÓN - Mi empresa*.  

5. A continuación, se le presentará una lista de tablas que están expuestas como parte de la API para su entorno. Seleccione la tabla a la que desea conectarse y luego elija **Conectar**.

Estas denominadas tablas están expuestas como extremos por el contector [!INCLUDE[prod_short](includes/prod_short.md)] para Power Apps.  

> [!NOTE]
> Si desea incluir datos de otras tablas en [!INCLUDE[prod_short](includes/prod_short.md)] en su aplicación, debe trabajar con un desarrollador para definir una API personalizada en [!INCLUDE[prod_short](includes/prod_short.md)] y, después, consumir esa API personalizada a través de un conector personalizado en Power Apps. Para obtener más información, vea [Crear un conector personalizado desde cero](/connectors/custom-connectors/define-blank).  

Ya se ha conectado correctamente con los datos de [!INCLUDE[prod_short](includes/prod_short.md)] y está preparado para comenzar a crear su PowerApp. Puede agregar pantallas adicionales y conectarse a los datos adicionales de su [!INCLUDE[prod_short](includes/prod_short.md)]. Para obtener más información, consulte [Crear una aplicación de lienzo a partir de un ejemplo en Power Apps](/powerapps/maker/canvas-apps/open-and-run-a-sample-app).  

Cuando haya diseñado y creado la aplicación, puede compartirla con sus compañeros. Para obtener más información, consulte [Guardar y publicar una aplicación de lienzo en Power Apps](/powerapps/maker/canvas-apps/save-publish-app).  

> [!NOTE]
> Si desea conectarse a [!INCLUDE[prod_short](includes/prod_short.md)] local, deberá elegir el conector **Business Central (local)** en el paso 3.  

## <a name="see-also"></a>Consulte también

[Crear una aplicación de lienzo a partir de una plantilla de Power Apps](/powerapps/maker/canvas-apps/get-started-test-drive)  
[Importar datos de empresa de otros sistemas financieros](across-import-data-configuration-packages.md)  
[Configurar [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md)  
[Introducción al desarrollo de aplicaciones de Connect para Dynamics 365 Business Central](/dynamics365/business-central/dev-itpro/developer/devenv-develop-connect-apps)  


[!INCLUDE[footer-include](includes/footer-banner.md)]