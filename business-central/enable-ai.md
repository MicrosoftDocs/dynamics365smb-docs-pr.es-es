---
title: Configure el texto de marketing de artículos basado en IA (vista previa) con Copilot
description: Este artículo explica cómo obtener una versión de prueba de Copilot de Business Central y habilitar Copilot en un entorno
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.topic: how-to
ms.date: 03/22/2023
ms.custom: bap-template
---

# Configure el texto de marketing de artículos basado en IA (vista previa) con Copilot

[!INCLUDE[ai-preview](includes/ai-preview.md)]

Este artículo explica cómo puede controlar la capacidad de crear textos de marketing de artículos impulsados por IA con Copilot para su organización. Esta tarea la realiza un administrador. Hay dos requisitos que debe cumplir para que la función esté disponible para los usuarios:

- Habilite la característica **Crear descripciones de productos basadas en IA con Copilot**.
- Consentimiento a los términos y condiciones de [versión preliminar](https://dynamics.microsoft.com/legaldocs/supp-dynamics365-preview/) y [Declaración de privacidad de Microsoft](https://go.microsoft.com/fwlink/?LinkId=521839) en nombre de la organización.

Si no se cumple alguno de estos requisitos, la característica no estará disponible para su uso.

## Requisitos previos

Está utilizando una [versión preliminar](ai-preview-getstarted.md) de Business Central que está habilitada para Copilot. La activación de Copilot la realiza un administrador. Para obtener más información, vaya a [Configurar texto de marketing de artículos impulsado por IA con Copilot](enable-ai.md).

## Habilite o deshabilite la característica "Crear descripciones de productos impulsadas por IA con Copilot"

1. En Business Central, busque y abra la página **Gestión de características**.
2. Establezca la columna **Habilitada para** para la característica **Vista previa de características: Crear descripciones de productos potenciadas por IA con Copilot** a **Todos los usuarios** para activar la característica o **Ninguno** para deshabilitarla.

   Para más información sobre la gestión de características en general, vaya a [Gestión de características](/dynamics365/business-central/dev-itpro/administration/feature-management).

## Consentir o rechazar la vista previa y los términos y condiciones de privacidad para todos los usuarios

1. En Business Central, busque y abra la página **Estado de los avisos de privacidad**.
2. En la columna **Nombre de la integración**, seleccione **Azure OpenAI**, a continuación, lea las condiciones que se le presentan.
3. En la fila **Azure OpenAI**, seleccione la casilla **Acuerdo para todos** para dar su consentimiento o la casilla **En desacuerdo para todos** para rechazar.

## Pasos siguientes

Una vez que habilite y dé su conformidad con la característica, estará listo para probar Copilot en los productos de Business Central. Vaya a [Agregar texto de marketing a los artículos](item-marketing-text.md).  

## Consulte también .

[Información general sobre el texto de marketing de productos impulsado por IA con Copilot](ai-overview.md)  
[Cree texto de marketing para artículos usando Copilot](item-marketing-text.md)  
[Preguntas frecuentes del texto de marketing de productos impulsado por IA con Copilot](ai-faq.md)  