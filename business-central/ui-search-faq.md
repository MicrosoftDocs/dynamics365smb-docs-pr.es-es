---
title: Preguntas más frecuentes acerca de la opción Dígame | Documentos de Microsoft
description: Este artículo proporciona respuestas a las preguntas que nuestros socios y clientes suelen hacer sobre la función Dígame.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: find
ms.date: 02/12/2020
ms.author: bholtorf
ms.openlocfilehash: 67dd65491710206245a2ff83dce3d3eb94484770
ms.sourcegitcommit: c78df3aefb3e2ed8c28e5ac8340d56ab787212e8
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "3071915"
---
# <a name="tell-me-faq"></a>FAQ acerca de la función Dígame
Este tema responde las preguntas que nuestros usuarios avanzados suelen hacer sobre la función Dígame.

### <a name="are-all-actions-from-my-current-page-discoverable-in-tell-me"></a>¿Se pueden ver todas las acciones de mi página actual en la función Dígame?
No. Las acciones en partes, como la parte Líneas de venta o Cuadros de información, no se muestran en la función Dígame.

### <a name="are-the-results-in-tell-me-filtered-by-permissions"></a>¿Los resultados de la función Dígame se filtran por permisos?
Si el usuario no tiene AccessByPermissions, las acciones no se mostrarán. Sin embargo, las páginas y los informes aparecen en los resultados, pero requieren que el usuario tenga permiso para acceder a ellos. Se mostrará un mensaje si el usuario no tiene permiso para ver el objeto.

### <a name="does-tell-me-display-content-from-my-customizations-or-installed-third-party-extensions"></a>¿La función Dígame muestra el contenido de mis personalizaciones o las extensiones de terceros instaladas?
La función Dígame recoge las acciones, páginas e informes que se originan a partir de extensiones, pero no la documentación de ayuda personalizada. Para obtener información técnica sobre cómo hacer que las páginas y los informes personalizados sean detectables, consulte [Agregar páginas e informes a la búsqueda](/dynamics365/business-central/dev-itpro/developer/devenv-al-menusuite-functionality).

### <a name="what-makes-this-different-from-what-was-previously-known-as-page-search"></a>¿Qué diferencia hay con lo que antes se conocía como búsqueda de página?
La Búsqueda de páginas se ha convertido en la función Dígame para ayudarle a realizar el trabajo rápidamente. La búsqueda de páginas solo puede ayudarle a desplazarse por páginas o informes. A nivel técnico, la función Dígame ya no se basa en el concepto heredado de MenuSuite.

### <a name="i-use-on-premises-d365fin-does-that-include-tell-me"></a>Utilizo [!INCLUDE[d365fin](includes/d365fin_md.md)] local. ¿Incluye la función Dígame?
Puede usar la función Dígame en el cliente web local para buscar acciones, páginas e informes, pero no documentación, o aplicaciones y servicios de consultoría en AppSource.

### <a name="is-tell-me-available-for-all-form-factors"></a>¿Está disponible para todos los factores de forma?
La función Dígame solo está disponible en el cliente web o en la aplicación de escritorio de Windows.

### <a name="are-the-documentation-results-available-in-any-language"></a>¿Los resultados de la documentación están disponibles en algún idioma?
Los artículos de ayuda se mostrarán en el idioma que ha especificado en **Mi configuración**, si la ayuda está disponible en ese idioma.

### <a name="why-dont-i-see-a-bookmark-icon-for-my-search-results"></a>¿Por qué no veo un icono de marcador para mis resultados de búsqueda?
El icono de marcador no se muestra en la ventana Dígame cuando la personalización está deshabilitada para un rol de usuario.


## <a name="see-also"></a>Consulte también  
[Guardar y personalizar vistas de lista](ui-views.md)  
[Búsqueda de páginas e información con Dígame](ui-search.md)  
[Búsqueda de páginas con el explorador de roles](ui-role-explorer.md)  
[Marque una página o informe en su Área de trabajo](ui-bookmarks.md)
