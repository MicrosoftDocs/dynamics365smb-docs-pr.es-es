---
title: Solucionar problemas de Copilot y capacidades de IA
description: Aprenda cómo solucionar problemas comunes que puede encontrar al trabajar con las capacidades de Copilot y AI en Business Central.
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.topic: troubleshooting
ms.collection: null
ms.date: 11/15/2023
ms.custom: bap-template
---
# <a name="troubleshoot-copilot-and-ai-capabilities"></a>Solucionar problemas de Copilot y capacidades de IA

Copilot es una funcionalidad impulsada por IA en Business Central que ayuda en diversas tareas, como redactar textos de marketing y conciliar cuentas bancarias. Si tiene problemas con Copilot u otras capacidades de IA, este artículo puede ayudarlo a identificar y solucionar problemas comunes.

## <a name="copilot-doesnt-appear-on-pages"></a>Copilot no aparece en las páginas

Si la funcionalidad Copilot, como la acción **Borrador con Copilot** para sugerencias de texto de marketing o la acción **Conciliar con Copilot** para asistencia de conciliación de cuentas bancarias, no aparece en una página como se esperaba, verifique lo siguiente:

- Si la función está controlada en Administración de funciones, asegúrese de que esté habilitada. [Más información acerca de la Administración de características](admin-feature-management.md).

- Asegúrese de que la funcionalidad no esté oculta por la personalización. [Más información sobre la personalización](ui-personalization-user.md).

## <a name="copilot-appears-on-pages-but-you-get-an-error-that-its-not-activated"></a>Copilot aparece en las páginas, pero aparece un error que indica que no está activado

Cuando intentas utilizar Copilot y obtienes un error similar a **Lo sentimos, Copilot no está activado para la \[función\]**, hay un par de cosas que debes verificar :

- Primero, asegúrese de que la función esté activada en la página **Copilot y capacidades de IA**. [Obtenga más información sobre cómo activar las capacidades de Copilot e IA](enable-ai.md#activate-features). 
- A continuación, asegúrese de que la declaración de privacidad para la integración de Azure OpenAI no esté configurada como **No estoy de acuerdo para todos**. Si es así, cámbielo a **Aceptar para todos**. [Obtenga más información sobre los avisos de privacidad](privacy-notices-status.md).

## <a name="see-also"></a>Consulte también .

[Configurar Copilot y capacidades de IA](enable-ai.md)  
[Sugerencias de texto de marketing con Copilot](ai-overview.md)  
[Conciliar cuentas bancarias con Copilot](bank-reconciliation-with-copilot.md)  
