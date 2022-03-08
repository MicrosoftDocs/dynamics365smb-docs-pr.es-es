---
title: Usar los datos para crear una aplicación | Documentos de Microsoft
description: Puede hacer que los datos de Business Central estén disponibles como un origen de datos y especificar una URL de OData de sus servicios web para crear una aplicación empresarial con Power Apps.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: OData, Power App, SOAP
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 718d4378a897b187ba3073449869184fef5cec98
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/01/2020
ms.locfileid: "3924833"
---
# <a name="connecting-to-your-business-central-data-to-build-a-business-app-using-power-apps"></a>Cómo conectarse a sus datos de Business Central para crear una aplicación empresarial con Power Apps

Puede convertir los datos de [!INCLUDE[prodshort](includes/prodshort.md)] en disponibles como origen de datos en Power Apps.  

> [!NOTE]  
> Debe disponer de una cuenta válida con [!INCLUDE[prodshort](includes/prodshort.md)] y con Power Apps.  

## <a name="to-add-prodshort-as-a-data-source-in-power-apps"></a>Para agregar [!INCLUDE[prodshort](includes/prodshort.md)] como origen de datos de Power Apps

1. En el explorador, vaya a [powerapps.microsoft.com](https://powerapps.microsoft.com/) y, a continuación, inicie sesión.
2. En la página de inicio, en la sección **Comenzar a partir de los datos**, elija la ventana **Otros orígenes de datos**.  

    Esto abre Power Apps Studio. En el primer inicio de sesión, debe especificar el país y la región.  
3. En la lista de conexiones disponibles, elija **Business Central** y, después, seleccione el botón **Crear**.

    Power Apps se conectará a su [!INCLUDE[prodshort](includes/prodshort.md)] con las credenciales con las que ha iniciado sesión. Si no es administrador de su [!INCLUDE[prodshort](includes/prodshort.md)], es posible que tenga que iniciar sesión con otra cuenta.  

4. Power Apps mostrará una lista de *ambientes y empresas* que están disponibles en [!INCLUDE[prodshort](includes/prodshort.md)]. Elija el entorno y la empresa que contiene los datos a los que desea conectarse, como *PRODUCCIÓN - Mi empresa*.  

5. A continuación, se le presentará una lista de tablas que están expuestas como parte de la API para su entorno. Seleccione la tabla a la que desea conectarse y luego elija **Conectar**.

Estas denominadas tablas están expuestas como extremos por el contector [!INCLUDE[prodshort](includes/prodshort.md)] para Power Apps.  

> [!NOTE]
> Si desea incluir datos de otras tablas en [!INCLUDE[prodshort](includes/prodshort.md)] en su aplicación, debe trabajar con un desarrollador para definir una API personalizada en [!INCLUDE[prodshort](includes/prodshort.md)] y, después, consumir esa API personalizada a través de un conector personalizado en Power Apps. Para obtener más información, vea [Crear un conector personalizado desde cero](/connectors/custom-connectors/define-blank).  

Ya se ha conectado correctamente con los datos de [!INCLUDE[prodshort](includes/prodshort.md)] y está preparado para comenzar a crear su PowerApp. Puede agregar pantallas adicionales y conectarse a los datos adicionales de su [!INCLUDE[prodshort](includes/prodshort.md)]. Para obtener más información, consulte [Crear una aplicación de lienzo a partir de un ejemplo en Power Apps](/powerapps/maker/canvas-apps/open-and-run-a-sample-app).  

Cuando haya diseñado y creado la aplicación, puede compartirla con sus compañeros. Para obtener más información, consulte [Guardar y publicar una aplicación de lienzo en Power Apps](/powerapps/maker/canvas-apps/save-publish-app).  

> [!NOTE]
> Si desea conectarse a [!INCLUDE[prodshort](includes/prodshort.md)] local, deberá elegir el conector **Business Central (local)** en el paso 3.  

## <a name="see-also"></a>Consulte también

[Crear una aplicación de lienzo a partir de una plantilla de Power Apps](/powerapps/maker/canvas-apps/get-started-test-drive)  
[Importar datos de empresa de otros sistemas financieros](across-import-data-configuration-packages.md)  
[Configurar [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)  
[Introducción al desarrollo de aplicaciones de Connect para Dynamics 365 Business Central](/dynamics365/business-central/dev-itpro/developer/devenv-develop-connect-apps)  
