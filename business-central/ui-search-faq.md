---
title: Preguntas frecuentes sobre Dígame
description: Este artículo proporciona respuestas a las preguntas que nuestros socios y clientes suelen hacer sobre la función Dígame.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: find
ms.search.form: TellMe
ms.date: 05/23/2022
ms.author: bholtorf
---
# <a name="tell-me-faq" />FAQ acerca de la función Dígame
Este artículo responde las preguntas que nuestros usuarios avanzados suelen hacer sobre la función Dígame.

### <a name="are-all-actions-from-my-current-page-discoverable-in-tell-me" />¿Se pueden ver todas las acciones de mi página actual en la función Dígame?

No. Las acciones en partes, como la parte Líneas de venta o Cuadros de información, no se muestran en la función Dígame.

### <a name="are-the-results-in-tell-me-filtered-by-permissions" />¿Los resultados de la función Dígame se filtran por permisos?

Si el usuario no tiene AccessByPermissions, las acciones no se mostrarán. Sin embargo, las páginas y los informes aparecen en los resultados, pero requieren que el usuario tenga permiso para acceder a ellos. Se mostrará un mensaje si el usuario no tiene permiso para ver el objeto.

### <a name="does-tell-me-display-content-from-my-customizations-or-installed-third-party-extensions" />¿La función Dígame muestra el contenido de mis personalizaciones o las extensiones de terceros instaladas?

La función Dígame recoge las acciones, páginas e informes que se originan a partir de extensiones. Para obtener información técnica sobre cómo hacer que las páginas y los informes personalizados sean detectables, consulte [Agregar páginas e informes a la búsqueda](/dynamics365/business-central/dev-itpro/developer/devenv-al-menusuite-functionality).

### <a name="what-makes-this-different-from-what-was-previously-known-as-page-search" />¿Qué diferencia hay con lo que antes se conocía como búsqueda de página?

La Búsqueda de páginas se ha convertido en la función Dígame para ayudarle a realizar el trabajo rápidamente. La búsqueda de páginas solo puede ayudarle a desplazarse por páginas o informes. A nivel técnico, la función Dígame ya no se basa en el concepto heredado de MenuSuite.

### <a name="i-use-on-premises-includeprodshortincludesprodshortmd-does-that-include-tell-me" />Utilizo [!INCLUDE[prod_short](includes/prod_short.md)] local. ¿Incluye la función Dígame?

Puede usar la función Dígame en el cliente web local para buscar acciones, páginas e informes, pero aplicaciones y servicios de consultoría en AppSource.

### <a name="is-tell-me-available-for-all-form-factors" />¿Está disponible para todos los factores de forma?

La función Dígame solo está disponible en el cliente web o en la aplicación de escritorio de Windows.

<!-- removed in v20 because of Help pane
### <a name="are-the-documentation-results-available-in-any-language" />Are the documentation results available in any language?
The help articles display in the language you have specified in **My Settings**, if help is available in that language.
-->

### <a name="does-tell-me-give-me-help-on-how-to-use-pages-reports-and-other-things" />¿La función Dígame me da ayuda sobre cómo usar páginas, informes y otras cosas?

No, pero puede obtener fácilmente esta información desde el panel de Ayuda. Simplemente seleccione el elemento del menú **Ayuda** (el signo de interrogación en la esquina superior derecha) o seleccione <kbd>Ctrl</kbd>+<kbd>F1</kbd> en su teclado. Para obtener más información, consulte [Help pane](product-help-and-support.md#help-pane).

### <a name="why-dont-i-see-a-bookmark-icon-for-my-search-results" />¿Por qué no veo un icono de marcador para mis resultados de búsqueda?

El icono de marcador no se muestra en la ventana Dígame cuando la personalización está deshabilitada para un rol de usuario.


## <a name="see-also" />Consulte también
[Guardar y personalizar vistas de lista](ui-views.md)  
[Búsqueda de páginas e información con Dígame](ui-search.md)  
[Búsqueda de páginas con el explorador de roles](ui-role-explorer.md)  
[Marque una página o informe en su Área de trabajo](ui-bookmarks.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
