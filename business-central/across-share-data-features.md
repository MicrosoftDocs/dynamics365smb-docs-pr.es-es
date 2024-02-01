---
title: Compartir datos
description: Descubra las distintas formas de compartir datos comerciales desde Business Central.
author: jswymer
ms.topic: conceptual
ms.search.keywords: null
ms.date: 09/21/2022
ms.author: jswymer
ms.service: dynamics-365-business-central
---
# Compartir datos comerciales desde Business Central

La colaboración entre personas dentro y fuera de una organización forma parte integral de la mayoría de las empresas. [!INCLUDE[prod_short](includes/prod_short.md)] ofrece varias características para compartir datos comerciales, como una lista de registros, registros específicos o documentos. <!--, with others&mdash;even those people who don't have a Business Central license in some cases.-->

Con todas estas características, el acceso a los datos está protegido por la licencia y los permisos de Business Central.

## Copiar un vínculo

![Admitido](media/check.png) Business Central Online ![Admitido](media/check.png) Business Central local

Desde cualquier página, puede copiar la URL de la página, luego pegarla y distribuirla en otras formas de medios como correos electrónicos, chats de Teams o mensajes de texto. La manera más sencilla de copiar un vínculo es seleccionando **Compartir** > **Copiar vínculo** desde la parte superior de la página. Otra forma es copiar la URL directamente del cuadro de direcciones del navegador.

Cuando pega la URL en un editor de texto enriquecido, como Word, Outlook o Teams, en lugar de mostrar la URL completa, el enlace recibe un nombre más legible que indica claramente el contexto del destino. El nombre y el patrón varían dependiendo de la página a la que esté enlazando. Tenga en cuenta los siguientes ejemplos:

|Patrón|Ejemplo de página|Nombre de enlace|
|-|-|-|
|Páginas de lista|Página de lista **Artículos** | **Artículos**|
|Ver lista| **Abrir** vista filtrada en la lista **Pedidos de venta**|**Pedidos venta - Abiertos**|
| Registro único|Tarjeta de artículo que muestra un registro único|"Tarjeta de artículo - 1896 ∙ Escritorio de ATENAS"|
|Registros de borrador| Nueva ficha de cliente|**Nueva - Ficha de cliente**|
|Empresa que utiliza insignia|Página de lista **Artículos** para empresa con insignia **CRONUS**| **Artículos (CRONUS)**|

> [!TIP]
> Se utiliza una convención de nomenclatura similar en las pestañas del navegador.

### Compartir análisis de datos
Si está viendo una página o consulta en el modo de análisis de datos, puede compartir una pestaña de análisis específica seleccionando la punta de flecha hacia abajo en la pestaña y luego seleccionando **Copiar enlace**. [Obtenga más información sobre el modo de análisis de datos](analysis-mode.md). 

### Modificar el vínculo de la página

Después de copiar un vínculo, antes de enviarlo, puede modificar la URL para manipular lo que se muestra cuando se abre la página. Por ejemplo, puede agregar filtros o especificar una empresa diferente.

[Más información sobre la URL del cliente web](/dynamics365/business-central/dev-itpro/developer/devenv-web-client-urls).

### Acerca de las listas filtradas

Con el panel de filtro en las páginas de lista, puede aplicar filtros para restringir los registros que se muestran en la lista. Si usa la acción **Copiar vínculo** o copia la URL desde el navegador, el vínculo de la página no incluirá los cambios de filtro. Los usuarios que abran el vínculo verán la colección completa. La forma de mantener el filtrado en un vínculo de página de colección es guardar primero la página filtrada como una **Vista**. A continuación, abra la vista y copie el vínculo desde ahí.

[Más información sobre clasificación, búsqueda y filtrado](ui-enter-criteria-filters.md).

## Compartir con Teams

![Admitido](media/check.png) Business Central Online ![No admitido](media/x-icon.png) Business Central local

Directamente desde la mayoría de las páginas de colección y páginas de detalles, puede enviar un vínculo a la página a personas, grupos de chat o canales. Por ejemplo, comparta un vínculo a una vista filtrada de sus registros. Si ha instalado la aplicación [!INCLUDE[prod_short](includes/prod_short.md)] para Teams, el enlace se expandirá automáticamente en una tarjeta compacta para que la incluya con su mensaje. Luego los destinatarios pueden seleccionar el vínculo o la tarjeta para abrir la página en Business Central.

[Más información sobre compartir registros y vínculos de páginas en Teams](across-working-with-teams.md).

## Compartir a través de OneDrive

![Admitido](media/check.png) Business Central Online ![Admitido](media/check.png) Business Central local

Business Central facilita almacenar, administrar y compartir archivos con otras personas a través de OneDrive para la Empresa. En la mayoría de las páginas donde hay archivos disponibles, como la Bandeja de entrada de informes o los archivos adjuntos a los registros, encontrará las acciones **Abrir en OneDrive** y **Compartir**. Ambas acciones guardan una copia de un archivo en OneDrive. Una vez en OneDrive, puede usar sus características de uso compartido y contribución en el archivo. La diferencia en las acciones es que **Abrir en OneDrive** abre el archivo en OneDrive. **Compartir** abre una página que le permite seleccionar con quién desea compartir el archivo. Los destinatarios recibirán una notificación por correo electrónico para acceder al archivo desde su OneDrive.

[Obtenga más información sobre cómo compartir archivos en OneDrive](across-share-onedrive.md).

## Abrir en Excel

![Admitido](media/check.png) Business Central Online ![Admitido](media/check.png) Business Central local

Para páginas de lista y listas insertadas en una página, puede usar la acción **Abrir en Excel**. Esta acción exporta la lista de registros a un libro de Excel (archivo .xlsx), que puede compartir con otros. En el libro, también puede usar la característica Compartir que forma parte de Excel.

[Obtenga más información sobre cómo ver y editar en Excel](across-work-with-excel.md).

## Compartir filas o tablas

![Admitido](media/check.png) Business Central Online ![Admitido](media/check.png) Business Central local

Puede compartir uno o varios registros en una lista. Simplemente seleccione el método abreviado de teclado <kbd>Ctrl</kbd>+<kbd>C</kbd> para copiar al portapapeles. A continuación, pegue lo que copió en otra aplicación pulsando <kbd>Ctrl</kbd>+<kbd>V</kbd>. Por ejemplo, al copiar tres pedidos de venta y pegarlos en un correo electrónico se mostrarán los pedidos en una tabla con un formato agradable.

[Obtenga más información sobre copiar y pegar en las preguntas frecuentes](faq-copy-paste.yml).

## Consulte también

[Integración de Business Central y OneDrive](across-onedrive-overview.md)  
[Administrar la integración de OneDrive con Business Central](admin-onedrive-integration.md)  
[Preguntas más frecuentes de OneDrive](admin-onedrive-faq.md)