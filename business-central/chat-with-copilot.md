---
title: Chatear con Copilot (versión preliminar)
description: Aprenda cómo usar el chat con Copilot para buscar datos y obtener ayuda en Business Central.
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.topic: how-to
ms.date: 03/18/2024
ms.custom: bap-template
ms.collection:
  - bap-ai-copilot
  - get-started
---

# Chatear con Copilot (versión preliminar)

[!INCLUDE[preview-banner](includes/preview-banner.md)]

Este artículo explica cómo chatear con Copilot para obtener respuestas sobre los datos de su empresa y asistencia con tareas y temas relacionados con Business Central.

[!INCLUDE[production-ready-preview-dynamics365](includes/production-ready-preview-dynamics365.md)]

## Acerca de Chatear con Copilot

Microsoft Copilot es el asistente impulsado por IA que ayuda a despertar la creatividad, aumentar la productividad y eliminar tareas tediosas. Puede chatear con Copilot en Business Central para responder preguntas y encontrar datos comerciales expresando lo que busca en lenguaje natural. Puedes utilizar el chat para:

- Encontrar datos comerciales de la empresa con la que trabaja en Business Central. Usar el chat para buscar (y abrir) datos sobre entidades/registros relacionados con procesos comerciales, como clientes, proveedores, pedidos de ventas y artículos, y más. Por ejemplo, pregúntele a Copilot: "Muéstrame el último pedido de ventas de Adatum".
- Explicar un concepto u obtenga orientación sobre cómo realizar una tarea. Por ejemplo, pregunte "Ayúdame a comprender las dimensiones" o "¿Cómo registro un pedido de ventas?".
- Comprender el propósito y el uso típico de campos individuales. Cuando elige **Preguntar a Copilot** en la información sobre herramientas de un campo, el chat se abre con un mensaje de Explicación para el nombre del campo y Copilot proporciona información al respecto. Copilot enlaza a los artículos a los que hace referencia, por lo que es fácil verificar la descripción.

  Las respuestas que proporciona Copilot se basan únicamente en la documentación oficial de Dynamics 365 Business Central, que está disponible en Microsoft Learn en la [documentación de Dynamics 365 Business Central](/dynamics365/business-central/).

El chat con Copilot evita la necesidad de navegar por la interfaz de usuario o la ayuda del producto, lo que puede ahorrar tiempo y aumentar la productividad.
  
> [Ver vídeo](https://go.microsoft.com/fwlink/?linkid=2250609)

## Requisitos previos

- La capacidad de chatear con Copilot está activada. Esta tarea la realiza un administrador. [Obtenga más información sobre cómo configurar las capacidades de Copilot e IA](enable-ai.md).
- El idioma de visualización en Business Central está configurado en una de las siguientes configuraciones regionales en inglés: en-AU, en-CA, en-GB, en-IE, en-IN, en-NZ, en-PH, en-SG, en-US, en-ZA. [Obtenga más información sobre cómo cambiar el idioma](ui-change-basic-settings.md#language).
- Su entorno de Business Central se encuentra en cualquier país o región excepto Canadá (esta característica aún no está disponible en Canadá).

## Comenzar a usar el chat con Copilot

1. En la esquina superior derecha de la pantalla, seleccione el icono ![Muestra el ícono para chatear con Copilot](media/chat-copilot-icon.png) icono **Copilot** ![ Muestra el color número 1.](media/callout-number-1.svg).

   El panel **Copilot** se muestra a la derecha, como se ilustra en la siguiente figura:

    ![Muestra el ícono para chatear con el panel Copilot con llamadas](media/chat-with-copilot-pane.svg)

1. En el cuadro **Hacer una pregunta** en la parte inferior ![Muestra la leyenda número 2](media/callout-number-2.svg), introduzca su pregunta y luego seleccione la punta de flecha o presione <kbd>Entrar</kbd> para obtener una respuesta.

   El texto que introduce, que a menudo se denomina *solicitud* en términos de Copilot, puede ser en forma de pregunta, declaración u orden.

   > [!TIP]
   > Copilot incluye un par de características que pueden ayudarle a escribir preguntas:
   > - Para comenzar a formular una pregunta, seleccione una de las guías de mensajes &mdash;**Encontrar**, **Explicar**, o **Guía**&mdash; disponibles en la parte superior del panel ![Muestra la leyenda número 3](media/callout-number-3.svg) o desde el ![Muestra el icono de guía rápida](media/prompt-guide-icon.png) el icono **Ver indicaciones** encima del cuadro **Hacer una pregunta** ![Muestra la leyenda número 4](media/callout-number-4.svg). Las guías de menajes son frases cortas predefinidas que comienzan una pregunta o sugerencia. Además de ahorrarle tiempo, están diseñados para guiar las respuestas de Copilot hacia una categoría de respuestas. También le ayudarán a comprender cómo formular preguntas para obtener las mejores respuestas.
   > - Seleccione las sugerencias de mensajes encima del botón **Ver indicaciones** ![Muestra la leyenda número 5](media/callout-number-5.svg) para hacer automáticamente una pregunta predefinida para obtener información sobre cómo funcionan las preguntas y respuestas. Las sugerencias rápidas solo están disponibles cuando está usando la empresa de demostración CRONUS.

1. Revise las respuestas que se muestran en el panel Copilot ![Muestra la leyenda número 6](media/callout-number-6.svg).

   Dependiendo de su pregunta, la respuesta puede contener texto, vínculos a registros o páginas en Business Central y vínculos a artículos de ayuda de Business Central sobre Microsoft Learn.

1. Haga otra pregunta para refinar la respuesta.

   El chat recuerda el contexto, lo que significa que no es necesario repetir los puntos clave de la pregunta original.

## Borrar chat para empezar de nuevo

Si desea cambiar a un tema de conversación diferente con Copilot, seleccione el icono ![Muestra el icono de borrar chat](media/clear-chat-icon.png) **Iniciar una nueva sesión de chat de Copilot** en la parte inferior del panel Copilot encima del cuadro de preguntas. Esta acción borra la memoria de Copilot de sus últimos mensajes. Comenzar de nuevo suele ser útil después de una conversación larga con muchos mensajes y puede ayudar a Copilot a brindar respuestas más precisas.

El chat también se borra si cierra Business Central o cierra su sesión.

## <a name="tips"></a>Aprovechar al máximo las preguntas

Esta sección proporciona formas en las que puede mejorar las respuestas que obtiene de Copilot.

- Formule preguntas claras y concretas.
- Sea conciso y evite oraciones largas o múltiples.
- Haga una pregunta cada vez. <!--Avoid asking about multiple questions in one message.-->
- Utilice un lenguaje natural, expresando las preguntas de manera amigable y conversacional.
- Utilice palabras clave, frases y términos que sepa que se utilizan en Business Central, ya sea en la aplicación o en la documentación.
- Si la respuesta inicial no responde completamente a sus preguntas, haga preguntas de seguimiento o reformule la última pregunta.
- Si está haciendo una pregunta sobre un tema diferente al de la pregunta anterior, borre la sesión de chat actual para comenzar de nuevo.

## Ejemplos de indicaciones

Sus preguntas a Copilot variarán naturalmente en función de su función, de su tarea actual, de los procesos que siga su organización y de cómo se exprese con palabras. Los siguientes son ejemplos que muestran diferentes formas de hacer preguntas en el panel de chat que pueden inspirarle a escribir sus propias preguntas basadas en su situación única.

Mensaje: `Find the Item with Description 'ATHENS Desk'`

En este ejemplo, proporciona instrucciones claras para que Copilot localice un único registro. Por ejemplo, insinúa que el registro se encuentra en la lista de elementos. Indica que el campo "Descripción" debe ser un texto específico que haya escrito entre comillas y con las mayúsculas correctas. Copilot normalmente responde con precisión cuando se le dan algunas pistas precisas, pero también puede utilizar un lenguaje más informal como en el siguiente ejemplo.

Mensaje: `give me the latest invoice for adatum`

En este ejemplo, le pide a Copilot que localice un registro, pero la pregunta es menos precisa y puede dar como resultado una respuesta menos precisa. Copilot a menudo puede entender, o adivinar, que la factura que está buscando no es una factura de compra sino una factura de venta de la lista Factura de venta registrada. Copilot también necesitaría hacer coincidir `adatum` con `Adatum Corporation`, que es el nombre completo y preciso del nombre del Cliente vendedor asociado con la factura.

Mensaje: `Show me customer ledger entries for Adatum from about three weeks ago`

En este ejemplo, le pide al copiloto que resuelva un acertijo de fechas común que normalmente requiere que abra un calendario como referencia o que utilice filtros de rango de fechas avanzados. Por lo general, Copilot puede comprender expresiones y términos comerciales comunes.

Mensaje: `How does I save my filterrings to do them later?`

En este ejemplo, le pide a Copilot orientación sobre cómo realizar alguna tarea en Business Central. Por lo general, Copilot puede comprender la intención de su pregunta, incluso si hay algunos errores gramaticales, ortográficos o abreviaturas.

Mensaje: `Provide feedback on answers`

Puede calificar las respuestas que obtiene de Copilot usando el botón Me gusta (pulgar hacia arriba) para una buena calificación o el botón No me gusta (pulgar hacia abajo) para una calificación baja. Cuando selecciona el botón No me gusta, puede elegir un motivo, incluido inexacto, inadecuado u otro. Esta información nos puede ayudar a mejorar las sugerencias.

<!--
1. If you want help getting you're question started, select the prompts either from the **Find**, **Explain**, or **Guide** buttons at the top of the Coplit pane or use the **View Prompts** menu above **Ask a question** box at the bottom.

   Prompts are predefined short phrases that start a question. Apart from saving you time, they're designed to target responses to specific categories. They also help you undestand how you can phrase questions to get the responses.-->
## Consulte también

[Solucionar problemas de Copilot y capacidades de IA](ai-copilot-troubleshooting.md)  
[Configurar Copilot y capacidades de IA](enable-ai.md)  
[Preguntas frecuentes sobre IA responsable para chatear con Copilot](faqs-chat-with-copilot.md)  
[Recursos de ayuda en Business Central](product-help-and-support.md)  
