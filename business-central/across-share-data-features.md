---
title: Compartir datos
description: Descubra las distintas formas de compartir datos comerciales desde Business Central.
author: jswymer
ms.topic: conceptual
ms.workload: na
ms.search.keywords: null
ms.date: 09/21/2022
ms.author: jswymer
---
# <a name="sharing-business-data-from-business-central"></a><a name="sharing-business-data-from-business-central"></a>Compartir datos comerciales desde Business Central

La colaboración entre personas dentro y fuera de una organización forma parte integral de la mayoría de las empresas. [!INCLUDE[prod_short](includes/prod_short.md)] ofrece varias características para compartir datos comerciales, como una lista de registros, registros específicos o documentos. <!--, with others&mdash;even those people who don't have a Business Central license in some cases.-->

Con todas estas características, el acceso a los datos está protegido por la licencia y los permisos de Business Central.

## <a name="copying-a-link"></a><a name="copying-a-link"></a>Copiar un vínculo

![Admitido](media/check.png) Business Central Online ![Admitido](media/check.png) Business Central local

Desde cualquier página, puede copiar la URL de la página, luego pegarla y distribuirla en otras formas de medios como correos electrónicos, chats de Teams o mensajes de texto. La manera más sencilla de copiar un vínculo es seleccionando **Compartir** > **Copiar vínculo** desde la parte superior de la página. Otra forma es copiar la URL directamente del cuadro de direcciones del navegador.

### <a name="modify-the-page-link"></a><a name="modify-the-page-link"></a>Modificar el vínculo de la página

Después de copiar un vínculo, antes de enviarlo, puede modificar la URL para manipular lo que se muestra cuando se abre la página. Por ejemplo, puede agregar filtros o especificar una empresa diferente.

Para obtener más información, consulte [URL de cliente web](/dynamics365/business-central/dev-itpro/developer/devenv-web-client-urls).

### <a name="about-filtered-lists"></a><a name="about-filtered-lists"></a>Acerca de las listas filtradas

Con el panel de filtro en las páginas de lista, puede aplicar filtros para restringir los registros que se muestran en la lista. Si usa la acción **Copiar vínculo** o copia la URL desde el navegador, el vínculo de la página no incluirá los cambios de filtro. Los usuarios que abran el vínculo verán la colección completa. La forma de mantener el filtrado en un vínculo de página de colección es guardar primero la página filtrada como una **Vista**. A continuación, abra la vista y copie el vínculo desde ahí.

Para obtener más información, consulte [Ordenar, buscar y filtrar](ui-enter-criteria-filters.md).

## <a name="sharing-to-teams"></a><a name="sharing-to-teams"></a>Compartir con Teams

![Admitido](media/check.png) Business Central Online ![No admitido](media/x-icon.png) Business Central local

Directamente desde la mayoría de las páginas de colección y páginas de detalles, puede enviar un vínculo a la página a personas, grupos de chat o canales. Por ejemplo, comparta un vínculo a una vista filtrada de sus registros. Si ha instalado la aplicación [!INCLUDE[prod_short](includes/prod_short.md)] para Teams, el enlace se expandirá automáticamente en una tarjeta compacta para que la incluya con su mensaje. Luego los destinatarios pueden seleccionar el vínculo o la tarjeta para abrir la página en Business Central.

Para obtener más información, consulte [Compartir registros y vínculos de páginas en Teams](across-working-with-teams.md).

## <a name="sharing-through-onedrive"></a><a name="sharing-through-onedrive"></a>Compartir a través de OneDrive

![Admitido](media/check.png) Business Central Online ![Admitido](media/check.png) Business Central local

Business Central facilita almacenar, administrar y compartir archivos con otras personas a través de OneDrive para la Empresa. En la mayoría de las páginas donde hay archivos disponibles, como la Bandeja de entrada de informes o los archivos adjuntos a los registros, encontrará las acciones **Abrir en OneDrive** y **Compartir**. Ambas acciones guardan una copia de un archivo en OneDrive. Una vez en OneDrive, puede usar sus características de uso compartido y contribución en el archivo. La diferencia en las acciones es que **Abrir en OneDrive** abre el archivo en OneDrive. **Compartir** abre una página que le permite seleccionar con quién desea compartir el archivo. Los destinatarios recibirán una notificación por correo electrónico para acceder al archivo desde su OneDrive.

Para obtener más información, consulte [Compartir archivos en OneDrive](across-share-onedrive.md).

## <a name="opening-in-excel"></a><a name="opening-in-excel"></a>Abrir en Excel

![Admitido](media/check.png) Business Central Online ![Admitido](media/check.png) Business Central local

Para páginas de lista y listas insertadas en una página, puede usar la acción **Abrir en Excel**. Esta acción exporta la lista de registros a un libro de Excel (archivo .xlsx), que puede compartir con otros. En el libro, también puede usar la característica Compartir que forma parte de Excel.

Para obtener más información, consulte [Ver y editar en Excel](across-work-with-excel.md).

## <a name="sharing-rows-or-tables"></a><a name="sharing-rows-or-tables"></a>Compartir filas o tablas

![Admitido](media/check.png) Business Central Online ![Admitido](media/check.png) Business Central local

Puede compartir uno o varios registros en una lista. Simplemente seleccione el método abreviado de teclado <kbd>Ctrl</kbd>+<kbd>C</kbd> para copiar al portapapeles. A continuación, pegue lo que copió en otra aplicación pulsando <kbd>Ctrl</kbd>+<kbd>V</kbd>. Por ejemplo, al copiar tres pedidos de venta y pegarlos en un correo electrónico se mostrarán los pedidos en una tabla con un formato agradable.

Para obtener más información, consulte [Preguntas frecuentes sobre copiar y pegar](faq-copy-paste.yml).

## <a name="see-also"></a><a name="see-also"></a>Consulte también

[Integración de Business Central y OneDrive](across-onedrive-overview.md)  
[Administrar la integración de OneDrive con Business Central](admin-onedrive-integration.md)  
[Preguntas más frecuentes de OneDrive](admin-onedrive-faq.md)
