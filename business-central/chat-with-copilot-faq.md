---
title: Preguntas frecuentes de Chatear con Copilot
description: Este artículo responde a algunas preguntas habituales sobre el chat con Copilot en Business Central.
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.topic: conceptual
ms.collection:
  - bap-ai-copilot
ms.date: 02/27/2024
ms.custom: bap-template jswymer
---
# Preguntas frecuentes de Chatear con Copilot

[!INCLUDE[preview-banner](includes/preview-banner.md)]

Este artículo responde a algunas preguntas habituales sobre el chat con Copilot en [!INCLUDE[prod_short](includes/prod_short.md)]. Si tiene preguntas relacionadas con la IA y el chat, consulte [Preguntas frecuentes sobre IA responsable para chatear con Copilot](faqs-chat-with-copilot.md).

[!INCLUDE[production-ready-preview-dynamics365](includes/production-ready-preview-dynamics365.md)]

## ¿Pueden los administradores conceder o denegar permisos a usuarios individuales para tener acceso al chat?

No, no hay permiso ni permiso establecido para chatear. Si el chat está activado en la página [Capacidades de Copilot e IA](enable-ai.md), todos los usuarios de un entorno tienen acceso al chat.
 
## ¿El chat está disponible en tableta, teléfono u otros factores de forma?

No, el panel de chat solo está disponible en el cliente web [!INCLUDE[web_client](includes/web_client.md)].

## No uso Business Central en inglés. ¿Cuáles son mis opciones?

En este momento, el chat solo está disponible en inglés. Puede cambiar su idioma de usuario a inglés en [Mi configuración](ui-change-basic-settings.md#language).

## ¿Qué versión de Business Central necesito para experimentar el chat?

El chat está disponible en versión preliminar pública desde la versión 24.0 (lanzamiento de versiones 1 de 2024).

## ¿El chat funciona con mis personalizaciones?

Depende del tipo de pregunta que le haga a Copilot. Por ejemplo:

- Cuando hace preguntas para localizar registros, Copilot puede encontrar registros en sus tablas personalizadas que se identifican mediante campos personalizados.
- Cuando solicita una explicación u orientación, Copilot no tiene acceso a ninguna información sobre sus personalizaciones o documentación para sus complementos.

## Copilot nunca parece abrir el registro o la página que solicité. ¿Qué estoy haciendo mal?

Cuando le pide a Copilot que busque registros en [!INCLUDE[prod_short](includes/prod_short.md)], muestra los registros que encuentra como mosaicos o enlaces seleccionables en el panel de chat. Mientras está en versión preliminar, Copilot no navega automáticamente a ninguna página.

## Las respuestas que recibo de Copilot varían aunque hago la misma pregunta. ¿Es un error?

En ocasiones, Copilot podría responder de diferentes maneras. Las respuestas no son necesariamente idénticas.

## ¿Cuándo debo utilizar la función Copiar en los mensajes de chat?

Puede usar el botón Copiar para copiar un mensaje anterior de su conversación con Copilot, pegarlo en el cuadro de entrada para volver a intentarlo o probar una variación de su mensaje a Copilot.

## ¿Cómo personalizo o extiendo el chat?

Mientras está en la versión preliminar, el panel de chat y las respuestas de Copilot no se pueden modificar de ninguna manera mediante personalización, complementos o personalización.

## ¿Copilot encuentra datos en otras empresas o entornos?

Incluso si su organización utiliza múltiples entornos o empresas para segregar datos, Copilot solo busca registros en la empresa en la que está conectado actualmente.

## El panel de chat de Copilot no se muestra. ¿Qué puedo hacer?

Verifique que su idioma de usuario en Mi configuración esté configurado en inglés y que su entorno sea de la versión 24.0 o posterior. En la página Copilot y capacidades de IA, asegúrese de que los administradores hayan activado el consentimiento para los datos en todas las geografías y hayan activado el chat. Asegúrese de que la localización de su entorno no sea Canadá.

Si aún no ve la función de chat con Copilot, es posible que Microsoft todavía esté implementándola en su región. Copilot se implementará para los clientes de EE. UU. primero en abril de 2024 y luego, en el transcurso de unas semanas, se implementará en localizaciones de otros países o regiones.

## Pasos siguientes

[Chatear con Copilot (versión preliminar)](chat-with-copilot.md)
