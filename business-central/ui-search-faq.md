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
ms.date: 04/01/2019
ms.author: bholtorf
ms.openlocfilehash: d04f78b31b9fb0403201cb9e5cb1f98f1ef935e1
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/29/2019
ms.locfileid: "1248022"
---
# <a name="tell-me-faq"></a>FAQ acerca de la función Dígame
Este tema responde a las preguntas que nuestros usuarios avanzados suelen hacer sobre la nueva función Dígame que ha reemplazado la función anterior de búsqueda de páginas conocida como **Buscar páginas e informes**.

### <a name="are-all-actions-from-my-current-page-discoverable-in-tell-me"></a>¿Se pueden ver todas las acciones de mi página actual en la función Dígame?
No. Las acciones en partes, como la parte Líneas de venta o Cuadros de información, no se muestran en la función Dígame.

### <a name="are-the-results-in-tell-me-filtered-by-permissions"></a>¿Los resultados de la función Dígame se filtran por permisos?
Si el usuario no tiene AccessByPermissions, las acciones no se mostrarán. Sin embargo, las páginas y los informes aparecen en los resultados, pero requieren que el usuario tenga permiso para acceder a ellos. Se mostrará un mensaje si el usuario no tiene permiso para ver el objeto.

### <a name="does-tell-me-display-content-from-my-customizations-or-installed-third-party-extensions"></a>¿La función Dígame muestra el contenido de mis personalizaciones o las extensiones de terceros instaladas?
La función Dígame recoge las acciones, páginas e informes que se originan a partir de extensiones, pero no la documentación de ayuda personalizada. Para obtener información técnica sobre cómo hacer que las páginas y los informes personalizados sean detectables, consulte [Agregar páginas e informes a la búsqueda](/dynamics365/business-central/dev-itpro/developer/devenv-al-menusuite-functionality).

### <a name="what-makes-this-different-from-what-was-previously-known-as-page-search"></a>¿Qué diferencia hay con lo que antes se conocía como búsqueda de página?
La Búsqueda de páginas se ha convertido en la función Dígame para ayudarle a realizar el trabajo rápidamente. La búsqueda de páginas solo puede ayudarle a desplazarse por páginas o informes. A nivel técnico, la función Dígame ya no se basa en el concepto heredado de MenuSuite.

### <a name="i-use-on-premises-included365finincludesd365finmdmd-does-that-include-tell-me"></a>Utilizo [!INCLUDE[d365fin](includes/d365fin_md.md)] local. ¿Incluye la función Dígame?
Puede usar la función Dígame en el cliente web local para buscar acciones, páginas e informes, pero no documentación, o aplicaciones y servicios de consultoría en AppSource. Los usuarios que se conectan a [!INCLUDE[d365fin](includes/d365fin_md.md)] desde el cliente de Dynamics NAV continúan usando la Búsqueda de páginas.

### <a name="is-tell-me-available-for-all-form-factors"></a>¿Está disponible para todos los factores de forma?
La función Dígame solo está disponible en el cliente web o en la aplicación de escritorio de Windows.

### <a name="are-the-documentation-results-available-in-any-language"></a>¿Los resultados de la documentación están disponibles en algún idioma?
Los artículos de ayuda se mostrarán en el idioma que ha especificado en **Mi configuración**, si la ayuda está disponible en ese idioma.

## <a name="see-also"></a>Consulte también  
[Encontrar características e información](ui-search.md)
