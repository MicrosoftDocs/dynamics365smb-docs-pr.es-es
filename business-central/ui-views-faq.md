---
title: Preguntas frecuentes sobre las vistas de lista
description: Información detallada sobre cómo guardar filtros como vistas de lista.
author: mikebcMSFT
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: list, filter, pane, views
ms.date: 04/01/2020
ms.author: mikebc
ms.openlocfilehash: 1433e22f232b032242a4464730b07df376cadaf3
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/01/2020
ms.locfileid: "3189320"
---
# <a name="list-views-faq"></a>Preguntas frecuentes sobre vistas de lista
Este tema responde preguntas que nuestros usuarios avanzados hacen a menudo sobre cómo trabajar con vistas de lista y guardar filtros.  

### <a name="how-do-views-handle-expressions"></a>¿Cómo gestionan las vistas las expresiones?
Al guardar una vista que incluye filtros con expresiones, como rangos de fechas, operadores, palabras clave o tokens de filtro, se guarda la expresión y no los valores resultantes. Por ejemplo, guardar una vista filtrada por el campo **Fecha de creación** con la expresión **-1S..hoy** siempre encontrará registros relativos a la fecha actual, incluso cuando se acceda a la vista el próximo mes.

### <a name="where-are-list-views-saved"></a>¿Dónde se guardan las vistas de lista?
De manera similar a ocultar un campo o reordenar su menú de navegación, las vistas de lista forman parte de la personalización del usuario y se almacenan en la base de datos. Al borrar toda la personalización en una lista también se eliminarán permanentemente sus vistas personales y se borrará la personalización adicional, como la reordenación de las vistas. Para obtener más información, consulte [Personalizar el área de trabajo](ui-personalization-user.md).

### <a name="why-dont-i-have-a-save-icon"></a>¿Por qué no tengo un icono Guardar?
El icono Guardar y el menú de opciones no se muestran junto a las vistas en el panel de filtro si la personalización está deshabilitada para un rol de usuario. Los usuarios que no tienen habilitada la personalización pueden acceder a las vistas del sistema que son una parte estándar de la página, modificar o crear más filtros.

### <a name="on-which-page-types-can-i-use-list-views"></a>¿En qué tipos de página puedo usar vistas de lista?
Las vistas solo están disponibles en la lista y en las páginas de la hoja de trabajo.

### <a name="are-views-also-available-on-other-form-factors"></a>¿Las vistas también están disponibles en otros factores de forma?
Sí. Cualquier vista que guarde en su explorador o aplicación de escritorio también estará disponible en su tableta o smartphone. No puede modificar ni personalizar vistas en los dispositivos móviles.

### <a name="are-my-personal-views-always-accessible"></a>¿Mis vistas personales están siempre accesibles?
Las mismas vistas están disponibles en una página de listas si accede a ella desde el menú de navegación, a través de la ventana **Dígame** o mediante un vínculo de URL a la página de la lista. Las vistas no están disponibles en partes de lista, búsquedas o cuando una página de lista se muestra como un cuadro de diálogo.

### <a name="how-do-i-return-a-view-to-its-original-filters-after-modifying-them"></a>¿Cómo devuelvo una vista a sus filtros originales después de modificarlos?
En la parte inferior del panel de filtro, elija la acción **Restablecer filtros** para borrar los cambios de filtro que ha realizado en la vista y devolverla a sus campos filtrados y criterios de filtro originales.

### <a name="what-is-the-difference-between-hiding-and-removing-views"></a>¿Cuál es la diferencia entre ocultar y quitar vistas?
Al quitar una vista, se eliminará permanentemente. Ocultar una vista le permite ocultarla temporalmente del panel de filtro, pero puede volver a mostrarla más tarde seleccionando la acción **Mostrar**.

### <a name="how-can-i-share-my-views-with-others"></a>¿Cómo puedo compartir mis vistas con otros usuarios?
[!INCLUDE[d365fin](includes/d365fin_md.md)] no proporciona una forma de compartir la vista de lista precisa, pero puede compartir sus filtros actuales para que otros usuarios puedan ver una lista similar de registros. En su explorador de escritorio, copie la URL y compártala con sus colegas. No se garantiza que compartir filtros proporcione al destinatario un conjunto idéntico de filtros que ve en su explorador.

### <a name="can-i-search-for-views-in-the-tell-me-window"></a>¿Puedo buscar vistas en la ventana Dígame?
Nº La ventana **Dígame** solo muestra los resultados de búsqueda de la página, pero está a solo un paso de llegar a su vista favorita una vez que navegue a la página.

### <a name="what-is-shared-layout"></a>¿Qué es el diseño compartido?
Todas las vistas de una página de lista comparten un diseño de columnas común que incluye qué columnas se muestran, su secuencia, ancho, inmovilización de panel y configuración de entrada rápida. La personalización de cualquiera de los diseños de columna también afectará a otras vistas que compartan el mismo diseño en la página de lista.

Algunas vistas del sistema pueden tener diseños únicos de las columnas de la lista. Por ejemplo, podrían reorganizar las columnas para mostrar solo las columnas más relevantes para esa vista. Puede identificar qué vistas tienen diseños únicos eligiendo el icono ![Mostrar más opciones](media/show-more-options-icon.png "Mostrar más opciones") y observando que la casilla **Diseño compartido** no está seleccionada. Como usuario, puede personalizar el diseño de columnas para una vista con un diseño único sin que afecte a ninguna de las demás vistas en la página de lista. Solo los desarrolladores pueden definir un diseño de columna único para una vista que inicialmente tiene un diseño compartido.

### <a name="what-does-the-show-system-filters-link-do"></a>¿Qué hace el vínculo Mostrar filtros del sistema?
En algunas páginas de lista, se mostrará el panel de filtro **Mostrar filtros del sistema** en la parte inferior del panel de filtro cuando la página incluye filtros especificados por el sistema. Por lo general, estos filtros especiales se usan para mostrar registros basados en el contexto actual, por ejemplo, cuando se debe filtrar una lista de pedidos para un cliente específico.

Los desarrolladores establecen los filtros del sistema utilizando el grupo de filtros 0. Para obtener detalles técnicos sobre los filtros del sistema, consulte [Método de grupo de filtros](/dynamics365/business-central/dev-itpro/developer/methods-auto/record/record-filtergroup-method)

### <a name="i-see-multiple-views-on-my-page-but-i-did-not-create-them-where-did-they-come-from"></a>Veo varias vistas en mi página, pero yo no las creé. ¿De dónde proceden?
Las vistas que ve en cualquier lista son una combinación de sus vistas personales junto con las vistas del sistema. Las vistas del sistema pueden originarse desde la aplicación de negocio, desde extensiones o pueden ser específicas del rol si la lista se ha personalziado para su rol.

### <a name="why-do-some-views-provide-fewer-options"></a>¿Por qué algunas vistas ofrecen menos opciones?
Algunas vistas solo ofrecen la opción de guardar una copia de la vista, mientras que otras no permiten guardar los cambios en la vista. La forma en que se creó la vista determina las opciones disponibles para esa vista. Las vistas se pueden crear de varias maneras:
- Vistas personales que ha guardado
- Vistas del sistema que son una parte estándar de la aplicación de negocio o las han agregado extensiones o vistas específicas de rol. A diferencia de las vistas personales, no puede guardar cambios en los filtros en esa vista del sistema.
- Vistas de sistema heredadas que son una parte estándar de la aplicación de negocio pero que se crearon utilizando versiones anteriores de [!INCLUDE[d365fin](includes/d365fin_md.md)]. Estas vistas ofrecen considerablemente menos opciones. Solo puede guardarlas como una nueva vista y tampoco puede ocultarlas ni reordenarlas. Tenga en cuenta que las vistas de sistema heredadas dejarán de estar operativas en una actualización futura de [!INCLUDE[d365fin](includes/d365fin_md.md)].

### <a name="how-do-i-convert-legacy-system-views"></a>¿Cómo convierto las vistas de sistema heredadas?
Las vistas de sistema heredadas son vistas de lista creadas por desarrolladores en versiones anteriores de [!INCLUDE[d365fin](includes/d365fin_md.md)] colocándolas en la página Área de trabajo. Estas vistas ahora se muestran directamente en la página de lista, pero ofrecen una experiencia degradada y considerablemente menos opciones. Puede convertir una vista de sistema heredada en una vista personal que sea totalmente personalizable, simplemente guardándola como una nueva vista. Del mismo modo, los administradores pueden optar por convertir las vistas de sistema heredadas específicas del rol personalizando el rol del usuario y guardando la vista heredada como una nueva vista específica del rol.

Tenga en cuenta que las vistas de sistema heredadas dejarán de estar operativas en una actualización futura de [!INCLUDE[d365fin](includes/d365fin_md.md)].

### <a name="others-in-my-organization-need-similar-list-views-as-standard-what-can-i-do"></a>Otros usuarios de mi organización necesitan vistas de lista similares de forma estándar. ¿Qué puedo hacer?
Trabajar con vistas personales es rápido y efectivo, pero [!INCLUDE[d365fin](includes/d365fin_md.md)] proporciona herramientas adicionales para definir vistas de lista necesarias para roles de usuario específicos o para todos los usuarios de la organización.
 - Los desarrolladores pueden personalizar el ambiente y crear vistas de lista en extensiones para todos los usuarios de la organización.
 - Los usuarios que no son codificadores, como los administradores o los responsables de departamento, pueden crear vistas de lista específicas de roles al personalizar un rol desde la página **Perfiles (roles)**.

### <a name="i-work-with-multiple-languages-how-do-i-translate-the-name-of-the-view"></a>Trabajo con varios idiomas: ¿cómo traduzco el nombre de la vista?
Al guardar una nueva vista o cambiar el nombre de una vista existente, debe introducir un nombre reconocible y significativo para esa vista. El nombre se guarda para su idioma actual y se mostrará también cuando usted u otros usuarios trabajen con [!INCLUDE[d365fin](includes/d365fin_md.md)] en diferentes idiomas. Para proporcionar nombres de vista traducidos, debe cambiar el idioma utilizando la página **Mi configuración**; después, cambie el nombre de la vista, que almacenará el nombre traducido en el nuevo idioma.

### <a name="do-views-with-expressions-work-in-all-languages"></a>¿Las vistas con expresiones funcionan en todos los idiomas?
Las expresiones que solo usan símbolos, como '**|**' o **..**, se consideran seguras para el acceso de los usuarios en cualquier idioma. Cualquier vista con expresiones que incluyan letras, palabras clave o tokens de filtro solo funcionará para el idioma en el que se creó.


### <a name="see-also"></a>Consulte también  
[Guardar y personalizar vistas de lista](ui-views.md)  
[Encontrar características e información](ui-search.md)    
[Ordenar, buscar y filtrar](ui-enter-criteria-filters.md)  