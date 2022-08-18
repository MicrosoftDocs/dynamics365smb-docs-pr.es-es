---
title: Integración de Business Central y OneDrive para la Empresa
description: Puedes usar OneDrive para la Empresa para almacenar, administrar y compartir archivos, como informes o archivos adjuntos. También si lo escribe One Drive.
author: jswymer
ms.topic: overview
ms.workload: na
ms.search.keywords: ''
ms.date: 02/28/2022
ms.author: jswymer
ms.openlocfilehash: 06adf2a30a7487fa3bc66e1aebec42e6c55184e2
ms.sourcegitcommit: bb9b2b4e693fa326a13d94e5e83f60e6c7ac5b68
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 08/06/2022
ms.locfileid: "9227424"
---
# <a name="business-central-and-onedrive-for-business-integration"></a>Integración de Business Central y OneDrive para la Empresa

OneDrive para la Empresa es un servicio de almacenamiento en la nube que se incluye en Microsoft 365. [!INCLUDE[prod_short](includes/prod_short.md)] facilita almacenar, administrar y compartir archivos con otras personas a través de OneDrive. Cuando un archivo está en su OneDrive puede disfrutar de las ricas experiencias de colaboración de las versiones en línea de los productos de Microsoft, como Word, Excel y PowerPoint. Por ejemplo, puede compartir un documento de Word y luego usted y sus colegas pueden editarlo juntos en tiempo real. OneDrive también le permite abrir otros tipos de archivos, como PDF. 

## <a name="get-started"></a>Comenzar

Hemos creado la conexión entre [!INCLUDE[prod_short](includes/prod_short.md)] en línea y OneDrive, por lo que es fácil comenzar. El único requisito es que los usuarios hayan abierto OneDrive al menos una vez. 

En la mayoría de las páginas donde hay archivos disponibles, como la Bandeja de entrada de informes o los archivos adjuntos a los registros, encontrará las acciones **Abrir en OneDrive** y **Compartir**.

:::image type="content" source="media/onedrive-overview-report-inbox-w-outline.png" alt-text="Las acciones Abrir en OneDrive y Compartir para informes":::


:::image type="content" source="media/one-drive-attachments-w-outline.png" alt-text="Las acciones Abrir en OneDrive y Compartir para archivos adjuntos":::

|Seleccione...|Para...|Ver más información...|
|---------|-----|----------------|
|Abrir en OneDrive|Copie el archivo en una carpeta de Business Central en su OneDrive y abra el archivo.|[Abrir en OneDrive](across-share-onedrive.md#open-in-onedrive) |
|Participación|Copie el archivo en su OneDrive y compártalo con otras personas.|[Compartir en OneDrive](across-share-onedrive.md#share) |

<!--
When you use the **Open in OneDrive** action for the first time, [!INCLUDE[prod_short](includes/prod_short.md)] does the following in your OneDrive:

1. Creates a folder named [!INCLUDE[prod_short](includes/prod_short.md)]. 
2. In the [!INCLUDE[prod_short](includes/prod_short.md)] folder, it creates another folder with the same name as the company you're working in. If you work in more than one company, it will create a folder for the company you're working in when you use the **Open in OneDrive** action. 
3. Puts a copy of the file you selected in the folder, and then opens the file. The next time you use the action, it only copies and opens the file. 

The folder and its content are private until you decide to share them with others. For example, you might decide to share content with one or more of your coworkers, or even people outside of your organization. For more information, see [Share OneDrive files and folders](https://support.microsoft.com/office/share-onedrive-files-and-folders-9fcc2f7d-de0c-4cec-93b0-a82024800c07) in the content for OneDrive.
-->

> [!NOTE]
> También puede conectar su [!INCLUDE[prod_short](includes/prod_short.md)] local con OneDrive. Sin embargo, hay algunas cosas que se pueden hacer para que funcione. Para obtener más información, consulte [Configurar Business Central local](admin-onedrive-integration.md#configuring-business-central-on-premises).

## <a name="see-also"></a>Consulte también .

[Administrar la integración de OneDrive con Business Central](admin-onedrive-integration.md)  
[Abrir archivos de Business Central en OneDrive](across-share-onedrive.md)  
[Preguntas más frecuentes de OneDrive](admin-onedrive-faq.md)