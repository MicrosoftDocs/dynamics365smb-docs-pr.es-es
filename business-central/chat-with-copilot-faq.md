---
title: Preguntas frecuentes de Chatear con Copilot
description: 'Aprenda a chatear con Copilot, un asistente virtual que le ayuda a usar Business Central. Encuentre respuestas a preguntas comunes sobre funciones, configuraciones y limitaciones del chat.'
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.topic: conceptual
ms.collection:
  - bap-ai-copilot
ms.date: 06/13/2024
ms.custom: bap-template jswymer
---
# Preguntas frecuentes de Chatear con Copilot

[!INCLUDE [preview-banner](~/../shared-content/shared/preview-includes/preview-banner.md)]

Este artículo responde a algunas preguntas habituales sobre el chat con Copilot en [!INCLUDE[prod_short](includes/prod_short.md)]. Si tiene preguntas relacionadas con la IA y el chat, consulte [Preguntas frecuentes sobre IA responsable para chatear con Copilot](faqs-chat-with-copilot.md).

[!INCLUDE [preview-note](~/../shared-content/shared/preview-includes/production-ready-preview-dynamics365.md)]

## ¿Pueden los administradores conceder o denegar permisos a usuarios individuales para tener acceso al chat?

No, no hay permiso ni permiso establecido para chatear. Si el chat está activado en la página [Capacidades de Copilot e IA](enable-ai.md), todos los usuarios de un entorno tienen acceso al chat.
 
## ¿El chat está disponible en tableta, teléfono u otros factores de forma?

No, el panel de chat solo está disponible en el cliente web [!INCLUDE[web_client](includes/web_client.md)].

## No uso Business Central en inglés. ¿Cuáles son mis opciones?

En este momento, el chat solo está disponible en inglés. Puede cambiar su idioma de usuario a inglés en [Mi configuración](ui-change-basic-settings.md#language).

## ¿Qué versión de Business Central necesito para el chat?

El chat está disponible en versión preliminar pública desde la versión 24.0 (lanzamiento de versiones 1 de 2024).

## ¿El chat funciona con mis personalizaciones?

Depende del tipo de pregunta que le haga a Copilot. Por ejemplo:

- Si hace preguntas para buscar registros, puede encontrarlos en sus tablas personalizadas que usan campos personalizados.
- Si solicita una explicación u orientación a Copilot, no tiene acceso a ninguna información sobre sus personalizaciones o documentación para sus complementos.

## ¿Cómo abro un registro o página con chat?

Cuando le pide a Copilot que busque registros en [!INCLUDE[prod_short](includes/prod_short.md)], muestra los registros que encuentra como mosaicos o vínculos seleccionables en el panel de chat. Mientras está en versión preliminar, Copilot no navega automáticamente a ninguna página.

## ¿Por qué recibo diferentes respuestas de Copilot para la misma pregunta?

En ocasiones, Copilot podría responder de diferentes maneras. Las respuestas no son siempre idénticas.

## ¿Cómo debo utilizar la función Copiar en los mensajes de chat?

Puede usar el botón Copiar para copiar un mensaje anterior de su conversación con Copilot, pegarlo en el cuadro de entrada para volver a intentarlo o probar una variación de su mensaje a Copilot.

## ¿Puede personalizar o extender el chat?

Mientras está en la versión preliminar, el panel de chat y las respuestas de Copilot no se pueden modificar de ninguna manera mediante personalización, complementos o personalización.

## ¿Copilot busca datos en otras empresas o entornos?

Copilot solo busca registros en la empresa en la que ha iniciado sesión actualmente. No busca datos en múltiples entornos o empresas.

## ¿Qué puedo hacer si no se muestra el panel de chat?

Verifique que su idioma de usuario en **Mi configuración** esté configurado en inglés y que su entorno sea de la versión 24.0 o posterior. En la página Copilot y capacidades de IA, asegúrese de que el administrador haya activado el consentimiento para los datos en todas las geografías y hayan activado el chat. Asegúrese también de que la localización de su entorno no sea Canadá.

Si aún no ve la función de chat con Copilot, es posible que Microsoft todavía esté implementándola en su región. Copilot se ha implementado para los clientes de EE. UU. primero en abril de 2024 y luego, en el transcurso de unas semanas, se implementará en localizaciones de otros países o regiones.

## ¿Por qué Copilot solo muestra tres registros en el panel de Chat?

Cuando le pide a Copilot que busque registros, la forma en que formula la pregunta determina cómo Copilot identifica y aplica filtros en las páginas para encontrar lo que está buscando. Para mantener las respuestas concisas, el panel Chat muestra un máximo de tres mosaicos de registros, incluso cuando Copilot encuentra registros más relevantes.

## ¿Por qué Copilot da respuestas incorrectas a los cálculos?

Mientras está en versión preliminar, Chat con Copilot puede ayudarle a encontrar registros, explicar conceptos y guiarle sobre cómo completar tareas en Business Central. No se admiten otros casos de uso, como sumar un campo entre registros o calcular el importe mensual promedio. Esperamos agregar habilidades matemáticas básicas a Copilot en el futuro.

## ¿Puedo usar la voz en lugar de escribir mis indicaciones?

Puede chatear con Copilot usando la escritura por voz para hablar en lugar de escribir sus palabras en el panel de chat. La escritura por voz utiliza reconocimiento de voz en línea y está disponible con Windows. Para usar la voz, active el cuadro de mensajes de chat, luego use el método abreviado <kbd>Windows</kbd>+<kbd>H</kbd> y empiece a hablar. Para más información, consulte [Usar la escritura por voz para hablar en lugar de escribir en su PC](https://support.microsoft.com/windows/use-voice-typing-to-talk-instead-of-type-on-your-pc-fec94565-c4bd-329d-e59a-af033fa5689f).

## Pasos siguientes

- [Chatear con Copilot (versión preliminar)](chat-with-copilot.md)
