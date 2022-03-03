---
title: Integración de Business Central y OneDrive para la Empresa
description: Puedes usar OneDrive para la Empresa para almacenar, administrar y compartir archivos, como informes o archivos adjuntos.
author: bholtorf
ms.topic: overview
ms.workload: na
ms.search.keywords: ''
ms.date: 06/11/2021
ms.author: bholtorf
ms.openlocfilehash: f2c8efa4a32ef18ee4db25919c7e4405649d54bb
ms.sourcegitcommit: ef80c461713fff1a75998766e7a4ed3a7c6121d0
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 02/15/2022
ms.locfileid: "8141468"
---
# <a name="business-central-and-onedrive-for-business-integration"></a>Integración de Business Central y OneDrive para la Empresa
OneDrive para la Empresa es un servicio de almacenamiento en la nube que se incluye en Microsoft 365. [!INCLUDE[prod_short](includes/prod_short.md)] facilita almacenar, administrar y compartir archivos con otras personas a través de OneDrive. Cuando un archivo está en su OneDrive puede disfrutar de las ricas experiencias de colaboración de las versiones en línea de los productos de Microsoft, como Word, Excel y PowerPoint. Por ejemplo, puede compartir un documento de Word y luego usted y sus colegas pueden editarlo juntos en tiempo real. OneDrive también le permite abrir otros tipos de archivos, como PDF. 

## <a name="getting-started"></a>Introducción
Hemos creado la conexión entre [!INCLUDE[prod_short](includes/prod_short.md)] en línea y OneDrive, por lo que es fácil comenzar. El único requisito es que los usuarios hayan abierto OneDrive al menos una vez. 

En la mayoría de las páginas donde hay archivos disponibles, como la Bandeja de entrada de informes o los archivos adjuntos a los registros, encontrará una acción **Abrir en OneDrive**.

:::image type="content" source="media/Open in OneDrive.PNG" alt-text="La acción Abrir en OneDrive":::

 
:::image type="content" source="media/OneDrive attachment.PNG" alt-text="Compartir archivos adjuntos en OneDrive":::

Cuando usa la acción **Abrir en OneDrive** por primera vez, [!INCLUDE[prod_short](includes/prod_short.md)] hace lo siguiente en su OneDrive:

1. Crea una carpeta llamada [!INCLUDE[prod_short](includes/prod_short.md)]. 
2. En la carpeta [!INCLUDE[prod_short](includes/prod_short.md)], crea otra carpeta con el mismo nombre que la empresa en la que está trabajando. Si trabaja en más de una empresa, se creará una carpeta para la empresa en la que está trabajando cuando utilice l acción **Abrir en OneDrive**. 
3. Coloca una copia del archivo que seleccionó en la carpeta y luego abre el archivo. La próxima vez que use la acción, solo copia y abre el archivo. 

La carpeta y su contenido son privados hasta que decida compartirlos con otras personas. Por ejemplo, puede decidir compartir contenido con uno o más de sus compañeros de trabajo, o incluso con personas ajenas a su organización. Para obtener más información, consulte [Compartir archivos y carpetas de OneDrive](https://support.microsoft.com/en-us/office/share-onedrive-files-and-folders-9fcc2f7d-de0c-4cec-93b0-a82024800c07).

> [!NOTE]
> También puede conectar su [!INCLUDE[prod_short](includes/prod_short.md)] local con OneDrive. Sin embargo, hay algunas cosas que se pueden hacer para que funcione. Para obtener más información, consulte [Configurar Business Central local](admin-onedrive-integration.md#configuring-business-central-on-premises).

## <a name="see-also"></a>Consulte también
[Administrar la integración de OneDrive con Business Central](admin-onedrive-integration.md)  
[Abrir archivos de Business Central en OneDrive](across-share-onedrive.md)  
[Preguntas más frecuentes de OneDrive](admin-onedrive-faq.md)