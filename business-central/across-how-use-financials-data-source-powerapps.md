---
title: Usar los datos para crear una aplicación | Documentos de Microsoft
description: Puede hacer que los datos de Business Central estén disponibles como un origen de datos y especificar una URL de OData de sus servicios web para crear una aplicación empresarial con PowerApps.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Odata, Power App, SOAP
ms.date: 05/13/2019
ms.author: edupont
ms.openlocfilehash: 67d7129e32ccde3154a02dd12b806d712f470833
ms.sourcegitcommit: 92c7b6c5f0a5d8becbef106ab85258906765bc3e
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 05/13/2019
ms.locfileid: "1540274"
---
# <a name="connecting-to-your-business-central-data-to-build-a-business-app-using-powerapps"></a>Cómo conectarse a sus datos de Business Central para crear una aplicación empresarial con PowerApps
Puede convertir los datos de [!INCLUDE[d365fin](includes/d365fin_md.md)] en disponibles como origen de datos en PowerApps.  

> [!NOTE]  
>   Debe disponer de una cuenta válida con [!INCLUDE[d365fin](includes/d365fin_md.md)] y con PowerApps.  

## <a name="to-add-included365finincludesd365finmdmd-as-a-data-source-in-powerapps"></a>Para agregar [!INCLUDE[d365fin](includes/d365fin_md.md)] como origen de datos de PowerApps
1. En el explorador, vaya a [powerapps.microsoft.com](https://powerapps.microsoft.com/en-us/) y, a continuación, inicie sesión.
2. En la página Web, seleccione la plantilla **Iniciar desde datos** para crear una nueva aplicación de lienzo. Esta aplicación se ha diseñado para su uso en un dispositivo móvil, pero también puede seleccionar usar otra plantilla.

    El siguiente paso para crear una PowerApp es seleccionar los datos. Elija el icono de flecha y la opción **Nueva conexión** en la parte superior izquierda de la página.
3. En la lista de conexiones disponibles, elija **Business Central** y, después, seleccione el botón **Crear**.

    PowerApps se conectará a su [!INCLUDE [prodshort](includes/prodshort.md)] con las credenciales con las que ha iniciado sesión. Si no es administrador de su [!INCLUDE [prodshort](includes/prodshort.md)], es posible que tenga que iniciar sesión con otra cuenta.  

4. Si tiene más de una empresa en su [!INCLUDE [prodshort](includes/prodshort.md)], debe elegir la empresa a la que se conectará. Después, PowerApps muestra una lista de *tablas* que están disponibles en [!INCLUDE [prodshort](includes/prodshort.md)]. Estas denominadas tablas forman parte de la API de [!INCLUDE [prodshort](includes/prodshort.md)]. No es necesario que configure los extremos usted mismo, el conector de [!INCLUDE [prodshort](includes/prodshort.md)] para PowerApps hacerlo de forma automática.  

    Si desea incluir datos de otras tablas en [!INCLUDE [prodshort](includes/prodshort.md)] en su aplicación, debe trabajar con un desarrollador para definir una API personalizada en [!INCLUDE [prodshort](includes/prodshort.md)] y, después, consumir esa API personalizada a través de un conector personalizado en PowerApps. Para obtener más información, vea [Crear un conector personalizado desde cero](/connectors/custom-connectors/define-blank).  

Ya se ha conectado correctamente con los datos de [!INCLUDE [prodshort](includes/prodshort.md)] y está preparado para comenzar a crear su PowerApp. Puede agregar pantallas adicionales y conectarse a los datos adicionales de su [!INCLUDE [prodshort](includes/prodshort.md)]. Para obtener más información, consulte [Crear una aplicación de lienzo a partir de una plantilla de PowerApps](/powerapps/maker/canvas-apps/get-started-test-drive).  

Cuando haya diseñado y creado la aplicación, puede compartirla con sus compañeros. Para obtener más información, consulte [Guardar y publicar una aplicación de lienzo en PowerApps](/powerapps/maker/canvas-apps/save-publish-app).  

> [!NOTE]
> Si desea conectarse a [!INCLUDE [prodshort](includes/prodshort.md)] local, deberá elegir el conector **Business Central (local)** en el paso 3.  

## <a name="see-also"></a>Consulte también

[Crear una aplicación de lienzo a partir de una plantilla de PowerApps](/powerapps/maker/canvas-apps/get-started-test-drive)  
[Introducción](product-get-started.md)  
[Importar datos de empresa de otros sistemas financieros](across-import-data-configuration-packages.md)  
[Configurar [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)  
[Finanzas](finance.md)  
[Introducción al desarrollo de aplicaciones de Connect para Dynamics 365 Business Central](/dynamics365/business-central/dev-itpro/developer/devenv-develop-connect-apps)  
