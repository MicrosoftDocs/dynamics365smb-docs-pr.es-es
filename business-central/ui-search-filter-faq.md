---
title: Acerca de las acciones de Buscar y Filtrar en Business Central
description: Respuestas a las preguntas más frecuentes sobre las acciones de Buscar y Filtrar.
author: mikebcMSFT
ms.service: dynamics365-business-central
ms.topic: article
ms.reviewer: edupont04
ms.search.keywords: keyboarding, productivity, how do i, filter pane
ms.date: 10/01/2020
ms.author: mikebc
ms.openlocfilehash: 6d59fa53b1896e5b95f909074fbf0d947bd89a3d
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/01/2020
ms.locfileid: "3912001"
---
# <a name="searching-and-filtering-faq"></a>Búsqueda y filtrado de preguntas frecuentes
Este artículo responde a preguntas comunes que puede tener acerca de las acciones buscar y filtrar.

## <a name="is-there-a-difference-between-searching-and-filtering"></a>¿Hay alguna diferencia entre buscar y filtrar?
Sí.
- La búsqueda es simple y amplia: coincide con los registros que contienen el texto de búsqueda en los campos visibles de la página y no distingue entre mayúsculas y minúsculas.
- El filtrado es muy flexible y se puede aplicar a campos específicos, incluidos aquellos que no están visibles en la página: muestra registros con coincidencias exactas, que distinguen entre mayúsculas y minúsculas, pero se puede ajustar con símbolos potentes de búsqueda, tokens y fórmulas. Para obtener más información sobre cómo usar estas funciones, consulte [Ordenar, buscar y filtrar](ui-enter-criteria-filters.md).

## <a name="is-there-a-keyboard-experience-for-search-and-filter"></a>¿Hay alguna experiencia de teclado para buscar y filtrar?
Las acciones de buscar y filtrar se han optimizado para los usuarios que prefieren la interacción sin mouse para trabajar de manera eficiente con sus datos. Hay varias teclas de método abreviado que se pueden usar en secuencia para trabajar a alta velocidad. Para obtener más información, consulte [Métodos abreviados de teclado](keyboard-shortcuts.md#KeyboardFilter).

## <a name="is-the-filter-pane-available-on-all-lists"></a>¿El panel de filtros está disponible en todas las listas?
El panel de filtros está disponible en las páginas donde la lista es el contenido principal de la página, como hojas de cálculo y páginas de lista, incluidas las listas accesibles desde la barra de navegación. El panel de filtro aún no está disponible para las listas que se muestran como partes, como fichas desplegables o partes del área de trabajo. Cuando una lista está incorporada en una página, como líneas de ventas en un pedido de venta, el panel de filtro está disponible cuando esa lista obtiene el enfoque mediante el botón de modo de enfoque. Para obtener más información, consulte [Enfoque en los productos de línea](ui-enter-data.md#Focus).

## <a name="how-can-i-save-my-filters"></a>¿Cómo puedo guardar mis filtros?
Los filtros y ajustes a los filtros predefinidos se recuerdan a lo largo de la sesión (mientras permanece con la sesión iniciada), incluso si sale de la página. Puede guardar filtros permanentemente como una vista con nombre de la lista seleccionando el icono ![Guardar vista](media/save_view_icon.png "Guardar vista") en el panel de filtro. Para obtener más información, consulte [Preguntas frecuentes sobre vistas de lista](ui-views-faq.md). Tenga en cuenta que, a diferencia de los filtros, el texto de búsqueda no se recuerda cuando se sale de una página y no se guarda al guardar una vista.

En las páginas de solicitud de informes, también puede guardar filtros o usar filtros predefinidos. Para obtener más información, consulte [Uso de la configuración guardada](ui-work-report.md#SavedSettings).

## <a name="is-this-the-same-as-advanced-filters-and-limit-totals-in-microsoft-dynamics-nav"></a>¿Es lo mismo que los filtros avanzados y los totales límite de Microsoft Dynamics NAV?
[!INCLUDE[d365fin](includes/d365fin_md.md)] se basa en estas características populares y ofrece una experiencia moderna y muy útil para encontrar y analizar sus datos. Con más métodos abreviados de teclado y la introducción de la búsqueda, [!INCLUDE[d365fin](includes/d365fin_md.md)] supera la funcionalidad provista en Dynamics NAV.  

## <a name="can-i-search-and-filter-using-the-companion-apps-and-outlook-addin"></a>¿Puedo buscar y filtrar con las aplicaciones complementarias y Outlook AddIn?
En la mayoría de casos, en diferentes destinos de visualización, como dispositivos móviles u Outlook, puede buscar en listas pero no puede filtrar campos individuales.

## <a name="will-microsoft-extend-the-filter-pane-experience"></a>¿Extenderá Microsoft la experiencia del panel de filtros?
En Microsoft, escuchamos constantemente los comentarios de nuestra comunidad diversa de usuarios y actuamos siguiendo las mejores sugerencias de la comunidad. Si está interesado en ampliar el panel de filtros a más factores de forma y más tipos de listas, o si tiene una gran idea sobre cómo mejorarlo, agregue una idea nueva o vote las ideas existentes en [aka.ms/BusinessCentralIdeas](https://aka.ms/businesscentralideas).

## <a name="can-i-do-anything-about-the-searching-for-rows-is-taking-too-long-message"></a>¿Puedo hacer algo con el mensaje "La búsqueda de filas está tardando demasiado tiempo"?

Una operación de búsqueda tiene un límite de tiempo para llevarse a cabo. En primer lugar, intente cambiar los criterios de búsqueda y busque de nuevo. Si está utilizando [!INCLUDE[prodshort](includes/prodshort.md)] local, póngase en contacto con el administrador del sistema, ya que un administrador puede aumentar el límite de tiempo para las búsquedas.

Como administrador local, aumente el límite de tiempo en las búsquedas mediante la configuración de **Tiempo de espera de búsqueda** del servidor de [!INCLUDE[prodshort](includes/prodshort.md)]. Para obtener más información, consulte [Configuración de Business Central Server](/dynamics365/business-central/dev-itpro/administration/configure-server-instance?#Database) en la Ayuda de Business Central Developer e IT Pro.

## <a name="see-also"></a>Consulte también .
[Ordenar, buscar y filtrar](ui-enter-criteria-filters.md)  
[Búsqueda de páginas e información con Dígame](ui-search.md)  
[Búsqueda de páginas con el explorador de roles](ui-role-explorer.md)  
[Introducción](product-get-started.md)  
