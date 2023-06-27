---
title: Abrir archivos de Business Central en OneDrive
description: Descubra cómo puede compartir datos de Business Central a través de OneDrive para empresas.
author: jswymer
ms.topic: conceptual
ms.workload: na
ms.search.keywords: null
ms.date: 08/03/2022
ms.author: jswymer
---
# <a name="opening-and-sharing-business-central-files-in-microsoft-onedrive"></a><a name="opening-and-sharing-business-central-files-in-microsoft-onedrive"></a>Abrir y compartir archivos de Business Central en Microsoft OneDrive

[!INCLUDE[prod_short](includes/prod_short.md)] facilita almacenar, administrar y compartir archivos con otras personas a través de Microsoft OneDrive para la Emprea. En la mayoría de las páginas con archivos disponibles, como la Bandeja de entrada de informes cuando los archivos están adjuntos a los registros, encontrará las acciones **Abrir en OneDrive** y **Compartir**.


:::image type="content" source="media/onedrive-overview-report-inbox-w-outline.png" alt-text="Las acciones Abrir en OneDrive y Compartir para informes":::


:::image type="content" source="media/one-drive-attachments-w-outline.png" alt-text="Las acciones Abrir en OneDrive y Compartir para archivos adjuntos":::


## <a name="open-in-onedrive"></a><a name="open-in-onedrive"></a>Abrir en OneDrive

La acción **Abrir en OneDrive** copia el archivo en su OneDrive y luego abre el archivo en una aplicación como Microsoft Excel en línea, Microsoft Word en línea o Microsoft PowerPoint en línea. 

<!--## Working with different types of files-->

Cuando elige **Abrir en OneDrive**, [!INCLUDE[prod_short](includes/prod_short.md)] identifica archivos de Excel, Word y PowerPoint y los abre en sus aplicaciones en línea, es decir, Excel en línea, Word en línea y PowerPoint en línea. 

Con las versiones en línea de estas aplicaciones, puede anotar, editar y colaborar con otros sin salir del navegador.

Para otros tipos de archivos populares, como PDF, archivos de texto e imágenes, OneDrive proporciona visores de archivos que ofrecen funciones para imprimir, compartir y más. Si un archivo no se puede ver en OneDrive, es posible que se le solicite que lo descargue.

## <a name="share"></a><a name="share"></a>Compartir

La acción **Compartir** copia el archivo a su OneDrive para poder ver con quién lo ha compartido ya así como compartir el archivo con otras personas. Cuando selecciona la acción **Compartir**, se abre la siguiente página.

:::image type="content" source="media/share-to-onedrive-dialog-v2.PNG" alt-text="Compartir archivo en OneDrive":::

Si está familiarizado con OneDrive, es posible que reconozca la página antes referida. Verá que tiene dos opciones para compartir el archivo: **Enviar vínculo** y **Copiar vínculo**.

- **Enviar vínculo** le permite compartir los archivos con personas específicas. Las personas con las que comparta el archivo recibirán un correo electrónico con un vínculo al archivo. El archivo también aparecerá en la sección **Compartido** de su OneDrive. Comience escribiendo las direcciones de correo electrónico o los nombres de los contactos en el **campo Nombre, grupo o correo electrónico**. Incluya un mensaje debajo del **Nombre, grupo o campo de correo electrónico**, si quiere.

  > [!TIP]
  > Si desea redactar su mensaje en Outlook, seleccione el botón **Outlook**. El enlace se insertará en un borrador de correo electrónico y todas las personas con las que ingresó para compartir estarán en la lista **A**. Con esta opción, puede crear correos electrónicos utilizando todas las funciones de Outlook, incluido el formato de texto, la adición de otros archivos adjuntos, la inserción de imágenes o tablas y la adición de destinatarios CC o BCC.

- **Copiar link** copia un enlace de archivo que puede usar para compartir el archivo a través de aplicaciones como Facebook, Twitter o correo electrónico. 

Antes de enviar o copiar un vínculo de archivo, establezca el nivel de permiso para el archivo que desea que tengan las personas. Puede ver la configuración actual en **Enviar vínculo** o **Copiar vínculo**. En la mayoría de los casos, será **Cualquiera que tenga el vínculo puede editar para abrir el vínculo**, dependiendo de la configuración del administrador. Para cambiar los permisos, seleccione el vínculo y haga los cambios en la página **Configuración del vínculo**.

La característica para compartir en Business Central se basa en OneDrive. Más información sobre el uso compartido de OneDrive y los permisos en [Compartir archivos y carpetas de OneDrive](https://support.microsoft.com/en-us/office/share-onedrive-files-and-folders-9fcc2f7d-de0c-4cec-93b0-a82024800c07).

> [!NOTE]
> La acción **Compartir** no está disponible en la aplicación Business Central para dispositivos móviles.

## <a name="first-time-sign-in-from-business-central"></a><a name="first-time-sign-in-from-business-central"></a>Primer inicio de sesión desde Business Central

Cuando usa la acción **Abrir en OneDrive** o **Compartir** por primera vez, [!INCLUDE[prod_short](includes/prod_short.md)] hace lo siguiente:

1. Se abre la página **Revise los términos y condiciones**. Lea la página y, si está de acuerdo con los términos y condiciones, seleccione **Aceptar** para continuar.
2. Crea una carpeta llamada [!INCLUDE[prod_short](includes/prod_short.md)] en OneDrive. 
3. En la carpeta [!INCLUDE[prod_short](includes/prod_short.md)], crea una con el mismo nombre que la empresa en la que está trabajando. Si trabaja en más de una empresa, [!INCLUDE[prod_short](includes/prod_short.md)] crea una carpeta para cada empresa en la que está trabajando cuando utilice la acción **Abrir en OneDrive** o **Compartir**. 
4. Coloca una copia del archivo que seleccionó en la carpeta de nombre de empresa y luego abre el archivo. 

Luego, la próxima vez que use la acción **Abrir en OneDrive** o **Compartir**, [!INCLUDE[prod_short](includes/prod_short.md)] solo copia y abre el archivo. 

## <a name="managing-multiple-copies-of-a-file"></a><a name="managing-multiple-copies-of-a-file"></a>Administrar varias copias de un archivo

Cuando elige **Abrir en OneDrive** o **Compartir**, el archivo se copia de [!INCLUDE[prod_short](includes/prod_short.md)] a su carpeta en OneDrive. Si edita el archivo en OneDrive, ese archivo será diferente del archivo [!INCLUDE[prod_short](includes/prod_short.md)]. Para actualizar [!INCLUDE[prod_short](includes/prod_short.md)] con la versión del archivo más reciente, elimine el archivo existente de [!INCLUDE[prod_short](includes/prod_short.md)] y cargue la última copia.

Si ya existe un archivo con el mismo nombre en OneDrive, se le darán las siguientes opciones:

- **Utilizar existente**

  Esta opción abre o comparte el archivo que ya está almacenado en OneDrive, en lugar de copiar el archivo desde Business Central.
  
- **Reemplazar**
  
  Esta opción reemplaza el archivo existente en OneDrive con el archivo que seleccionó de Business Central. El archivo original no se pierde, puede verlo y restaurarlo usando el historial de versiones en OneDrive. Obtenga más información en [Restaurar una versión anterior de un archivo almacenado en OneDrive](https://support.microsoft.com/office/restore-a-previous-version-of-a-file-stored-in-onedrive).

- **Conservar ambos**
 
  Esta opción mantiene el archivo existente tal cual y guarda el archivo que seleccionó de Business Central con un nombre diferente. El nuevo nombre es similar al nombre existente, excepto que tiene un número de sufijo como "Artículos (2).xlsx".

## <a name="about-your-business-central-folder-on-onedrive"></a><a name="about-your-business-central-folder-on-onedrive"></a>Acerca de su carpeta de Business Central en OneDrive

La carpeta y su contenido son privados hasta que decida compartirlos con otras personas. Por tanto, puede decidir compartir contenido con uno o más de sus compañeros de trabajo, o incluso con personas ajenas a su organización. 

Puede acceder a su OneDrive desde la página **Mi configuración** eligiendo el enlace en el campo **Almacenamiento en la nube**. Obtenga más información en [Compartir archivos y carpetas de OneDrive](https://support.microsoft.com/en-us/office/share-onedrive-files-and-folders-9fcc2f7d-de0c-4cec-93b0-a82024800c07).

:::image type="content" source="media/my-settings-cloud-storage.PNG" alt-text="El campo Almacenamiento en la nube en Mi configuración":::

<!--## Extending the Connection to OneDrive
You can create an extension and connect it to... For more information, see...-->

## <a name="see-also"></a><a name="see-also"></a>Consulte también .

[Integración de Business Central y OneDrive](across-onedrive-overview.md)  
[Administrar la integración de OneDrive con Business Central](admin-onedrive-integration.md)  
[Preguntas más frecuentes de OneDrive](admin-onedrive-faq.md)
