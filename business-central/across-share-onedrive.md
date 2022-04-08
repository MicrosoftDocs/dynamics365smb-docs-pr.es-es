---
title: Abrir archivos de Business Central en OneDrive
description: Descubra cómo puede compartir datos de Business Central a través de OneDrive para empresas.
author: jswymer
ms.topic: conceptual
ms.workload: na
ms.search.keywords: ''
ms.date: 02/28/2022
ms.author: jswymer
ms.openlocfilehash: 2e1cc04d265541c87244dcd6c13b14327f07cc2f
ms.sourcegitcommit: 8a12074b170a14d98ab7ffdad77d66aed64e5783
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 03/31/2022
ms.locfileid: "8516426"
---
# <a name="opening-and-sharing-business-central-files-in-onedrive"></a>Abrir y compartir archivos de Business Central en OneDrive

[!INCLUDE[prod_short](includes/prod_short.md)] facilita almacenar, administrar y compartir archivos con otras personas a través de OneDrive para la Emprea. En la mayoría de las páginas donde hay archivos disponibles, como la Bandeja de entrada de informes o los archivos adjuntos a los registros, encontrará las acciones **Abrir en OneDrive** y **Compartir**.


:::image type="content" source="media/onedrive-overview-report-inbox-w-outline.png" alt-text="Las acciones Abrir en OneDrive y Compartir para informes":::


:::image type="content" source="media/one-drive-attachments-w-outline.png" alt-text="Las acciones Abrir en OneDrive y Compartir para archivos adjuntos":::

<!--
:::image type="content" source="media/Open in OneDrive.PNG" alt-text="The Open in OneDrive action":::

 
:::image type="content" source="media/OneDrive attachment.PNG" alt-text="Share file attachments in OneDrive":::
-->

## <a name="open-in-onedrive"></a>Abrir en OneDrive

La acción **Abrir en OneDrive** copia el archivo en su OneDrive y abre el archivo en sus aplicaciones en línea, como Excel en línea, Word en línea y PowerPoint en línea. 

<!--## Working with Different Types of Files-->

Cuando elige **Abrir en OneDrive**, [!INCLUDE[prod_short](includes/prod_short.md)] identifica archivos de Excel, Word y PowerPoint y los abre en sus aplicaciones en línea, es decir, Excel en línea, Word en línea y PowerPoint en línea. Puede realizar anotaciones, editar y colaborar con otras personas sin salir del navegador.

Para otros tipos de archivos populares, como PDF, archivos de texto e imágenes, OneDrive proporciona visores de archivos que ofrecen funciones para imprimir, compartir y más. Si un archivo no se puede ver en OneDrive, es posible que se le solicite que lo descargue.

## <a name="share"></a>Participación

La acción **Compartir** copia el archivo a su OneDrive y le permite compartir el archivo con otras personas y ver con quién ya ha compartido el archivo. Cuando selecciona la acción **Compartir**, se abre la siguiente página.

:::image type="content" source="media/share-to-onedrive-dialog.PNG" alt-text="Compartir archivo en OneDrive":::

Si está familiarizado con OneDrive, es posible que reconozca la página. Tiene dos opciones para compartir el archivo: **Enviar vínculo** y **Copiar vínculo**.

- **Enviar vínculo** le permite compartir los archivos con personas específicas. Las personas con las que comparta el archivo recibirán un correo electrónico con un vínculo al archivo. El archivo también aparecerá en la sección **Compartido** de su OneDrive. Comience escribiendo las direcciones de correo electrónico o los nombres de los contactos en el **campo Nombre, grupo o correo electrónico**.

- **Copiar vínculo** copia un vínculo al archivo en su OneDrive para que pueda usar el vínculo en otros lugares como Facebook, Twitter o correos electrónicos. 

Antes de enviar o copiar el vínculo, establezca el permiso para el archivo que desea que tengan las personas. Puede ver la configuración actual en **Enviar vínculo** y **Copiar vínculo**. En la mayoría de los casos, será **Cualquiera que tenga el vínculo puede editar para abrir el vínculo**, dependiendo de la configuración establecida por su administrador. Para cambiar los permisos, seleccione el vínculo y haga los cambios en la página **Configuración del vínculo**.

La característica para compartir en Business Central se basa en OneDrive. Por lo tanto, para obtener más información sobre el uso compartido y los permisos, consulte [Compartir archivos y carpetas de OneDrive](https://support.microsoft.com/en-us/office/share-onedrive-files-and-folders-9fcc2f7d-de0c-4cec-93b0-a82024800c07).

> [!NOTE]
> La acción **Compartir** no está disponible en la aplicación Business Central para dispositivos móviles.

## <a name="first-time-sign-in-from-business-central"></a>Primer inicio de sesión desde Business Central

Cuando usa la acción **Abrir en OneDrive** o **Compartir** por primera vez, [!INCLUDE[prod_short](includes/prod_short.md)] hace lo siguiente:

1. Se abre la página **Revise los términos y condiciones**. Lea la página y, si está de acuerdo con los términos y condiciones, seleccione **Aceptar** para continuar.
2. Se abre la página **Elegir una cuenta**  Seleccione su cuenta o **use otra cuenta** si no ve la suya, introduzca el nombre de usuario y la contraseña cuando se le solicite.
3. Crea una carpeta llamada [!INCLUDE[prod_short](includes/prod_short.md)] en OneDrive. 
4. En la carpeta [!INCLUDE[prod_short](includes/prod_short.md)], crea otra carpeta con el mismo nombre que la empresa en la que está trabajando. Si trabaja en más de una empresa, se creará una carpeta para la empresa en la que está trabajando cuando utilice las acciones **Abrir en OneDrive** y **Compartir**. 
5. Coloca una copia del archivo que seleccionó en la carpeta y luego abre el archivo. La próxima vez que use la acción, solo copia y abre el archivo. 

## <a name="managing-multiple-copies-of-a-file"></a>Administrar varias copias de un archivo

Cuando elige **Abrir en OneDrive** o **Compartir**, el archivo se copia de [!INCLUDE[prod_short](includes/prod_short.md)] a su carpeta en OneDrive. Si edita el archivo en OneDrive, las copias del archivo serán diferentes. Para actualizar [!INCLUDE[prod_short](includes/prod_short.md)] con el archivo más reciente, elimine el archivo existente de [!INCLUDE[prod_short](includes/prod_short.md)] y luego cargue la última copia.

Además, cuando ya exista un archivo con el mismo nombre en OneDrive, [!INCLUDE[prod_short](includes/prod_short.md)] proporcionará la opción de reemplazar el archivo o de conservar ambos archivos. Si opta por mantener ambos archivos, el nuevo archivo se copia en OneDrive y se le asigna un nombre de archivo con un número de sufijo, como "Elementos (2).xlsx,". El archivo original no se modifica. 

Si elige reemplazar el archivo, el nuevo archivo se agrega al historial de versiones de ese archivo. El archivo original no se pierde y puede ver o restaurar versiones anteriores del archivo. 

## <a name="about-your-business-central-folder-on-onedrive"></a>Acerca de su carpeta de Business Central en OneDrive

La carpeta y su contenido son privados hasta que decida compartirlos con otras personas. Por ejemplo, puede decidir compartir contenido con uno o más de sus compañeros de trabajo, o incluso con personas ajenas a su organización. Puede acceder a su OneDrive desde la página **Mi configuración** eligiendo el enlace en el campo **Almacenamiento en la nube**. Para obtener más información, consulte [Compartir archivos y carpetas de OneDrive](https://support.microsoft.com/en-us/office/share-onedrive-files-and-folders-9fcc2f7d-de0c-4cec-93b0-a82024800c07).

:::image type="content" source="media/my-settings-cloud-storage.PNG" alt-text="El campo Almacenamiento en la nube en Mi configuración":::

<!--## Extending the Connection to OneDrive
You can create an extension and connect it to... For more information, see...-->

## <a name="see-also"></a>Consulte también
[Integración de Business Central y OneDrive](across-onedrive-overview.md)  
[Administrar la integración de OneDrive con Business Central](admin-onedrive-integration.md)  
[Preguntas más frecuentes de OneDrive](admin-onedrive-faq.md)