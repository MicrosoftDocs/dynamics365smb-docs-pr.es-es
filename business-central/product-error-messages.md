---
title: Advertencias y mensajes de error
description: Descubra cómo puede solucionar problemas y encontrar soluciones a los mensajes de error cuando trabaja en Business Central.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.date: 03/08/2024
ms.service: dynamics-365-business-central
ms.custom: bap-temeplate
---
# <a name="warnings-and-error-messages"></a>Advertencias y mensajes de error

Durante un día de trabajo, es posible que vea notificaciones en [!INCLUDE [prod_short](includes/prod_short.md)] sobre que algo salió mal o que no fue posible publicar algo, por ejemplo. En muchos casos, la notificación facilita la resolución del problema o la reversión de cualquier cambio que haya realizado. En otros casos, es posible que no tenga la información que necesita para el desbloqueo. Este artículo proporciona sugerencias sobre cómo progresar.  

## <a name="in-product-user-assistance"></a>Asistencia al usuario en el producto

La versión predeterminada de [!INCLUDE [prod_short](includes/prod_short.md)] incluye descripciones para la mayoría de los campos, columnas y acciones a las que se puede acceder cuando se elige el nombre. En combinación con consejos didácticos para páginas importantes, estas descripciones emergentes o leyendas son nuestra implementación actual de la *asistencia al usuario integrada*, que es un principio importante en el mundo actual del diseño de software.  

Si tiene una pregunta sobre un campo u otro elemento de la interfaz de usuario, elija el nombre para leer una breve descripción. Elija el vínculo **Preguntar a Copilot** si eso no es suficiente. También puede usar el panel de ayuda del producto para encontrar respuestas a sus preguntas.  

Para más información, vea [Modelo de asistencia al usuario de Dynamics 365 Business Central](/dynamics365/business-central/dev-itpro/user-assistance) en el contenido de administración de [!INCLUDE [prod_short](includes/prod_short.md)].  

## <a name="help-and-support-page"></a>Página Ayuda y soporte técnico

En [!INCLUDE[prod_short](includes/prod_short.md)], el elemento del menú Ayuda (el signo de interrogación en la esquina superior derecha) le da acceso a la página de **Ayuda y soporte técnico**, donde puede encontrar vínculos a recursos que pueden ayudarle a encontrar respuestas a sus preguntas. Para obtener más información, vea [Recursos para ayuda y soporte técnico](product-help-and-support.md).  

## <a name="help-others"></a>Ayuda a otros

Si es administrador o superusuario, puede ayudar a otros buscando mensajes de error en la página **Registro de mensajes de error** o en el centro de administración. En muchos casos, el mensaje de advertencia o error se refiere a la configuración o la falta de permisos y problemas similares con los que el superusuario o el administrador pueden ayudar fácilmente. En otros casos, es posible que deba inspeccionar las páginas para identificar la causa. Para obtener más información, consulte [Encontrar información técnica](/dynamics365/business-central/dev-itpro/administration/manage-technical-support#finding-technical-information) en el contenido de administración para [!INCLUDE [prod_short](includes/prod_short.md)].  

## <a name="share-error-details-for-faster-assistance"></a>Comparta los detalles del error para obtener asistencia más rápida

Para superar los obstáculos y minimizar el tiempo de inactividad, recurra a la experiencia de colegas o expertos en la materia. Cuando está bloqueado por un error, puede compartir fácilmente los detalles del error cuando reciba ayuda.

Los detalles incluyen el mensaje de error, el código de error y otra información que resulta útil a la hora de solucionar un error. Al compartir los detalles del error, puede comunicar de manera efectiva el problema específico que enfrenta, lo que ayuda a sus colegas a ayudarlo.  

Puede copiar detalles eligiendo el **Icono de compartir** en cuadros de diálogo de validación en línea, o el menú **Compartir detalles** en cuadros de diálogo de error.  

Además de copiar los detalles del error, también puede optar por compartir los detalles a través de Microsoft Teams eligiendo **Compartir detalles con Teams** para hacer lo siguiente:

* Copie los detalles del error.
* Abre la ventana **Compartir en Teams**, donde puede pegar los detalles del error que copió y especificar a quién desea pedir ayuda. [!INCLUDE [prod_short](includes/prod_short.md)] agrega un enlace a la página donde experimentó el error para facilitar la solución del problema.

También puede optar por compartir detalles por correo electrónico eligiendo **Compartir detalles por correo electrónico** para hacer lo siguiente:

* Copie los detalles del error.
* Abra su editor de correo electrónico predeterminado, donde puede pegar los detalles del error que copió y especificar a quién desea pedir ayuda. [!INCLUDE [prod_short](includes/prod_short.md)] agrega un enlace a la página donde experimentó.

## <a name="help-yourself"></a>Ayudarse a sí mismo

Los mensajes de error brindan información y acciones que facilitan comprender, acceder y resolver los errores que provienen de la plataforma.

Los mensajes de error que la [!INCLUDE [prod_short](includes/prod_short.md)] plataforma genera contiene todos los detalles técnicos, incluidos los nombres de los campos, en la sección **Mensaje de error detallado**. Seleccione el icono **Copiar detalles** en errores de validación en línea o en un mensaje de error para acceder a la información técnica.

Las acciones sobre los mensajes de error lo llevan directamente a la página donde un campo está causando el error. No es necesario que se tome el tiempo para encontrar la página o el campo usted mismo. Para resolver el error, solo tiene que elegir la acción en el mensaje de error y [!INCLUDE [prod_short](includes/prod_short.md)] le llevará a la ubicación adecuada.

El siguiente video muestra cómo usar mensajes de error procesables para desbloquear.

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RW1l2sM]

### <a name="tip-for-developers"></a>Consejo para desarrolladores

Si es desarrollador, cuando llama al método [TestField](/dynamics365/business-central/dev-itpro/developer/methods-auto/record/record-testfield-joker-joker-errorinfo-method), pero no pasa al |objeto `ErrorInfo`, [!INCLUDE [prod_short](includes/prod_short.md)] genera automáticamente el vínculo a un página donde un usuario puede corregir el problema. [!INCLUDE [prod_short](includes/prod_short.md)] primero obtiene la página de búsqueda o desglose del registro y luego busca la página de la tarjeta o la página de búsqueda y agrega un vínculo de navegación a esa página de la tarjeta. [!INCLUDE [prod_short](includes/prod_short.md)] no agrega un enlace en las siguientes situaciones:

* Si el error está en la página que está abierta actualmente.
* Si el usuario no tiene permiso para modificar el registro subyacente.

## <a name="see-also"></a>Consulte también

[Recursos de ayuda y soporte técnico](product-help-and-support.md)  
[Preguntas frecuentes](across-faq.yml)  
[FAQ acerca de la función Dígame](ui-search-faq.md)  
[Preguntas frecuentes sobre búsqueda y filtrado](ui-search-filter-faq.yml)  
[Preguntas frecuentes sobre copiar y pegar](faq-copy-paste.yml)  
[Cambiar la configuración básica](ui-change-basic-settings.md)  
[Preparación para hacer negocios](ui-get-ready-business.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
