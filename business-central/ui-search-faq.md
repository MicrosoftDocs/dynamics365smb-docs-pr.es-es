---
title: Preguntas frecuentes sobre Dígame
description: Este artículo proporciona respuestas a las preguntas que nuestros socios y clientes suelen hacer sobre la función Dígame.
author: brentholtorf
ms.topic: conceptual
ms.service: dynamics-365-business-central
ms.search.keywords: 'find, search, Tell Me'
ms.search.form: TellMe
ms.date: 09/21/2023
ms.author: bholtorf
ms.reviewer: bholtorf
ms.custom: bap-template
---
# FAQ acerca de la función Dígame

Este artículo responde las preguntas que nuestros usuarios avanzados suelen hacer sobre la función Dígame qué desea hacer.

## ¿Se pueden ver todas las acciones de mi página actual en la función Dígame?

No. Las acciones en partes, como la parte Líneas de venta o Cuadros de información, no se muestran en la función Dígame.

## ¿Puedo buscar un registro específico?

Sí. Por ejemplo, si desea encontrar rápidamente un pedido de ventas, ingrese su identificador y luego elija la acción **Buscar datos de la empresa**. Si solo conoce el nombre del cliente, ingréselo. Dígame organiza los resultados por tipo, para que pueda encontrar el pedido en la categoría pedidos de venta.

## ¿Los resultados de la función Dígame se filtran por permisos?

Si el usuario no tiene AccessByPermissions, las acciones no se mostrarán. Sin embargo, las páginas y los informes aparecen en los resultados, pero requieren que el usuario tenga permiso para acceder a ellos. Se mostrará un mensaje si el usuario no tiene permiso para ver el objeto.

## ¿La función Dígame muestra el contenido de mis personalizaciones o las extensiones de terceros instaladas?

La función Dígame recoge las acciones, páginas e informes que se originan a partir de extensiones. Para obtener información técnica sobre cómo hacer que las páginas y los informes personalizados sean detectables, consulte [Agregar páginas e informes a la búsqueda](/dynamics365/business-central/dev-itpro/developer/devenv-al-menusuite-functionality).

## ¿Qué diferencia hay con lo que antes se conocía como búsqueda de página?

La Búsqueda de páginas se ha convertido en la función Dígame para ayudarle a realizar el trabajo rápidamente. La búsqueda de páginas solo puede ayudarle a desplazarse por páginas o informes. A nivel técnico, la función Dígame ya no se basa en el concepto heredado de MenuSuite.

## Utilizo [!INCLUDE[prod_short](includes/prod_short.md)] local. ¿Incluye la función Dígame?

Puede usar la función Dígame en el cliente web local para buscar acciones, páginas e informes, pero aplicaciones y servicios de consultoría en AppSource.

## ¿Está disponible para todos los factores de forma?

Sí. Se introdujo en teléfonos y tabletas en el segundo lanzamiento de versiones de Business Central 2023, pero debe habilitarse en [Gestión de funciones](/dynamics365/business-central/dev-itpro/administration/feature-management) utilizando la opción **Característica: busque páginas y datos en la aplicación móvil**. 

<!-- removed in v20 because of Help pane
### Are the documentation results available in any language?
The help articles display in the language you have specified in **My Settings**, if help is available in that language.
-->

## ¿La función Dígame me da ayuda sobre cómo usar páginas, informes y otras cosas?

No, pero puede obtener fácilmente esta información desde el panel de Ayuda. Simplemente seleccione la acción **Buscar Ayuda** la página **Dígame qué desea hacer** o seleccione <kbd>Control</kbd>+<kbd>F1</kbd> en su teclado. Para obtener más información sobre el panel Ayuda, vaya a [Panel Ayuda](product-help-and-support.md#help-pane).

### ¿Por qué no veo un icono de marcador para mis resultados de búsqueda?

El icono de marcador no se muestra en la ventana Dígame cuando la personalización está deshabilitada para un rol de usuario.

## Consulte también  

[Guardar y personalizar vistas de lista](ui-views.md)  
[Búsqueda de páginas e información con Dígame](ui-search.md)  
[Búsqueda de páginas con el explorador de roles](ui-role-explorer.md)  
[Marque una página o informe en su Área de trabajo](ui-bookmarks.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]