---
title: Preguntas frecuentes de Chatear con Copilot
description: Este artículo responde a algunas preguntas habituales sobre el chat con Copilot en Business Central.
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.topic: conceptual
ms.collection:
  - bap-ai-copilot
ms.date: 05/17/2024
ms.custom: bap-template jswymer
---
# <a name="chat-with-copilot-faq"></a>Preguntas frecuentes de Chatear con Copilot

[!INCLUDE[preview-banner](includes/preview-banner.md)]

Este artículo responde a algunas preguntas habituales sobre el chat con Copilot en [!INCLUDE[prod_short](includes/prod_short.md)]. Si tiene preguntas relacionadas con la IA y el chat, consulte [Preguntas frecuentes sobre IA responsable para chatear con Copilot](faqs-chat-with-copilot.md).

[!INCLUDE[production-ready-preview-dynamics365](includes/production-ready-preview-dynamics365.md)]

## <a name="can-admins-grant-or-deny-permission-to-individual-users-to-get-access-to-chat"></a>¿Pueden los administradores conceder o denegar permisos a usuarios individuales para tener acceso al chat?

No, no hay permiso ni permiso establecido para chatear. Si el chat está activado en la página [Capacidades de Copilot e IA](enable-ai.md), todos los usuarios de un entorno tienen acceso al chat.
 
## <a name="is-chat-available-on-tablet-phone-or-other-form-factors"></a>¿El chat está disponible en tableta, teléfono u otros factores de forma?

No, el panel de chat solo está disponible en el cliente web [!INCLUDE[web_client](includes/web_client.md)].

## <a name="i-dont-use-business-central-in-english-what-are-my-options"></a>No uso Business Central en inglés. ¿Cuáles son mis opciones?

En este momento, el chat solo está disponible en inglés. Puede cambiar su idioma de usuario a inglés en [Mi configuración](ui-change-basic-settings.md#language).

## <a name="what-version-of-business-central-do-i-need-for-chat"></a>¿Qué versión de Business Central necesito para experimentar el chat?

El chat está disponible en versión preliminar pública desde la versión 24.0 (lanzamiento de versiones 1 de 2024).

## <a name="does-chat-work-with-my-customizations"></a>¿El chat funciona con mis personalizaciones?

Depende del tipo de pregunta que le haga a Copilot. Por ejemplo:

- Cuando hace preguntas para localizar registros, Copilot puede encontrar registros en sus tablas personalizadas que se identifican mediante campos personalizados.
- Cuando solicita una explicación u orientación, Copilot no tiene acceso a ninguna información sobre sus personalizaciones o documentación para sus complementos.

## <a name="how-do-i-open-a-record-or-page-with-chat"></a>Copilot nunca parece abrir el registro o la página que solicité. ¿Qué estoy haciendo mal?

Cuando le pide a Copilot que busque registros en [!INCLUDE[prod_short](includes/prod_short.md)], muestra los registros que encuentra como mosaicos o enlaces seleccionables en el panel de chat. Mientras está en versión preliminar, Copilot no navega automáticamente a ninguna página.

## <a name="why-do-i-get-different-answers-from-copilot-for-the-same-question"></a>Las respuestas que recibo de Copilot varían aunque hago la misma pregunta. ¿Es un error?

En ocasiones, Copilot podría responder de diferentes maneras. Las respuestas no son necesariamente idénticas.

## <a name="how-do-i-use-the-copy-function-on-chat-messages"></a>¿Cuándo debo utilizar la función Copiar en los mensajes de chat?

Puede usar el botón Copiar para copiar un mensaje anterior de su conversación con Copilot, pegarlo en el cuadro de entrada para volver a intentarlo o probar una variación de su mensaje a Copilot.

## <a name="can-i-customize-or-extend-chat"></a>¿Cómo personalizo o extiendo el chat?

Mientras está en la versión preliminar, el panel de chat y las respuestas de Copilot no se pueden modificar de ninguna manera mediante personalización, complementos o personalización.

## <a name="does-copilot-search-for-data-in-other-companies-or-environments"></a>¿Copilot encuentra datos en otras empresas o entornos?

Copilot solo busca registros en la empresa en la que está conectado actualmente&mdash; incluso si su organización utiliza múltiples entornos o empresas para segregar datos.

## <a name="what-can-i-do-if-the-chat-pane-doesnt-show"></a>El panel de chat de Copilot no se muestra. ¿Qué puedo hacer?

Verifique que su idioma de usuario en Mi configuración esté configurado en inglés y que su entorno sea de la versión 24.0 o posterior. En la página Copilot y capacidades de IA, asegúrese de que los administradores hayan activado el consentimiento para los datos en todas las geografías y hayan activado el chat. Asegúrese de que la localización de su entorno no sea Canadá.

Si aún no ve la función de chat con Copilot, es posible que Microsoft todavía esté implementando la función en su región. Copilot se implementará para los clientes de EE. UU. primero en abril de 2024 y luego, en el transcurso de unas semanas, se implementará en otras localizaciones de países o regiones.

## <a name="why-does-copilot-only-show-three-records-in-the-chat-pane"></a>¿Por qué Copilot solo muestra tres registros en el panel de Chat?

Cuando le pide a Copilot que recupere registros, la forma en que formula la pregunta determina cómo Copilot identifica y aplica filtros en las páginas para encontrar lo que está buscando. Para mantener las respuestas compactas y concisas, el panel Chat muestra un máximo de tres mosaicos de registros, incluso cuando Copilot encuentra una mayor cantidad de registros relevantes.

## <a name="why-does-copilot-give-incorrect-answers-to-calculations"></a>Copilot devuelve respuestas incorrectas a totales y otros cálculos

Mientras está en versión preliminar, Chat with Copilot puede ubicar registros, explicar conceptos y guiarlo sobre cómo completar tareas en Business Central. No se admiten otros casos de uso, como sumar un campo entre registros o calcular el monto mensual promedio. Esperamos agregar habilidades matemáticas básicas a Copilot en el futuro.

## <a name="can-i-use-speech-instead-of-typing-my-prompts"></a>¿Puedo usar la voz en lugar de escribir mis indicaciones?

Puede chatear con Copilot usando la escritura por voz para hablar en lugar de escribir sus palabras en el panel de chat. La escritura por voz utiliza reconocimiento de voz en línea y está disponible con Windows. Para usar la voz, active el cuadro de mensajes del chat, luego use el acceso directo <kbd>Windows</kbd>+<kbd>H</kbd> y comience a hablar. Para obtener más información, consulte [Usar la escritura por voz para hablar en lugar de escribir en su PC](https://support.microsoft.com/windows/use-voice-typing-to-talk-instead-of-type-on-your-pc-fec94565-c4bd-329d-e59a-af033fa5689f).

## <a name="next-steps"></a>Pasos siguientes

[Chatear con Copilot (versión preliminar)](chat-with-copilot.md)
