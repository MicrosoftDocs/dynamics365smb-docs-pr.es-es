---
title: Preguntas frecuentes sobre IA responsable para Chatear con Copilot (versión preliminar)
description: 'Estas preguntas frecuentes brindan información sobre la tecnología de inteligencia artificial utilizada para chatear con Copilot en Business Central. Incluye las consideraciones clave y detalles sobre cómo se usa la IA, cómo se probó y evaluó, y cualquier limitación específica.'
ms.date: 06/13/2024
ms.custom:
  - responsible-ai-faqs
ms.topic: article
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.search.keywords: 'copilot, AI, chat'
---
# Preguntas frecuentes sobre IA responsable para Chatear con Copilot (versión preliminar)

[!INCLUDE [preview-note](~/../shared-content/shared/preview-includes/production-ready-preview-dynamics365.md)]

Estas preguntas frecuentes (P+F) describen el impacto de Chatear con Copilot en [!INCLUDE[prod_short](includes/prod_short.md)]. Si tiene preguntas generales sobre el uso de la función, consulte [Preguntas frecuentes para chatear con Copilot](chat-with-copilot-faq.md).

## ¿Qué es Chatear con Copilot?

Microsoft Copilot es un asistente impulsado por IA que le ayuda a ser más creativo, productivo y eficiente. Puede chatear con Copilot en Business Central para obtener respuestas y perspectivas sobre [!INCLUDE[prod_short](includes/prod_short.md)] y los datos de su empresa escribiendo lo que desea saber en lenguaje natural.

El chat con Copilot, también llamado chat, es una función interactiva que responde a sus preguntas sin que tenga que navegar por la interfaz de usuario o la documentación del producto. El panel Copilot está disponible desde cualquier lugar del cliente de [!INCLUDE[prod_short](includes/prod_short.md)].

Puede hacer preguntas en lenguaje natural, como "¿Cómo entrego productos a mis clientes directamente desde mis proveedores?" o "¿Tenemos sillas de oficina en stock por menos de 600 $?" En respuesta, Copilot proporciona respuestas en lenguaje natural. Dependiendo de las preguntas, las respuestas pueden incluir solo texto, vínculos a registros o páginas en [!INCLUDE[prod_short](includes/prod_short.md)] y vínculos a artículos de ayuda de [!INCLUDE[prod_short](includes/prod_short.md)] sobre Microsoft Learn.

## ¿Cuáles son las capacidades de Chatear con Copilot?

Puede chatear con Copilot para obtener respuestas a las siguientes clases de preguntas:

### Explicar y guiar

Puede pedirle a Copilot que les explique un concepto específico relacionado con [!INCLUDE[prod_short](includes/prod_short.md)], como qué son las dimensiones, o proporcionar orientación sobre cómo completar una tarea, como cómo publicar un pedido de ventas. Copilot busca la documentación oficial de [!INCLUDE[prod_short](includes/prod_short.md)] publicada por Microsoft y proporciona una respuesta basada en la documentación.

- Copilot utiliza el conocimiento sobre Microsoft Learn (no es una búsqueda web amplia) para buscar semánticamente solo en la documentación de [!INCLUDE[prod_short](includes/prod_short.md)] de Dynamics 365 en Microsoft Learn.

- Copilot no toma medidas, no crea nuevos datos ni modifica ninguna configuración. Simplemente resume cualquier párrafo que encuentre en Microsoft Learn que coincida con la pregunta o el mensaje en el chat.

### Buscar datos comerciales y páginas relacionadas

Puede pedirle a Copilot que ubique páginas por nombre o solicitar registros según sus campos y restricciones. Si Copilot encuentra una coincidencia, responde con un vínculo al registro o la página relevante, que puede seleccionar para abrir.

- Copilot convierte la entrada en lenguaje natural en una consulta que consta de criterios de búsqueda, clasificación y filtrado de tablas.

  La capacidad utiliza las capacidades de búsqueda de datos nativas de [!INCLUDE[prod_short](includes/prod_short.md)] para encontrar datos coincidentes en tablas dentro de la base de datos de las empresas. La búsqueda se ejecuta bajo su propia identidad por motivos de seguridad y cumplimiento. No busca fuera de la base de datos de [!INCLUDE[prod_short](includes/prod_short.md)].

- Copilot no toma medidas, no crea nuevos datos ni modifica ninguna configuración. Sólo resume los registros recibidos de la búsqueda de datos nativos de [!INCLUDE[prod_short](includes/prod_short.md)]. 

## ¿Cuál es el uso previsto de Chatear con Copilot?

El chat está diseñado para uso empresarial y para responder a preguntas relacionadas con [!INCLUDE[prod_short](includes/prod_short.md)] y los datos comerciales que contiene. La característica le ayuda a resolver tareas comunes, como buscar registros u obtener orientación. Puede expresarse con sus propias palabras, haciendo su trabajo más fácil y accesible cuando trabaje con [!INCLUDE[prod_short](includes/prod_short.md)].

## ¿Cómo se evaluó Chatear con Copilot? ¿Qué métricas se utilizan para medir el rendimiento?

- La función se sometió a pruebas exhaustivas durante las cuales se entregaron a Copilot numerosos textos en inglés que cubrían una amplia gama de temas y estilos de expresión de intenciones. Los resultados se evaluaron en función de la precisión, relevancia y seguridad.
  
- La característica está construida de acuerdo con el Estándar de IA Responsable de Microsoft. [Obtenga más información sobre la IA responsable de Microsoft](https://aka.ms/RAI).

## ¿Cómo monitorea Microsoft la calidad del contenido generado?

Microsoft cuenta con varios sistemas para garantizar que el contenido generado por Copilot sea de la más alta calidad, detectar abusos y garantizar la seguridad de nuestros clientes y sus datos.

Puede proporcionar comentarios sobre cada respuesta de Copilot e informar sobre contenido inexacto o inadecuado para ayudar a Microsoft a mejorar esta característica. 

- Para proporcionar comentarios, utilice el ícono Me gusta (pulgar hacia arriba) o No me gusta (pulgar abajo) en el panel **Copilot** en [!INCLUDE[prod_short](includes/prod_short.md)].
  
- Analizamos y utilizamos sus comentarios sobre la función para ayudarnos a mejorar las respuestas.
  
- Si encuentra contenido generado inapropiado, infórmelo a Microsoft mediante este formulario de comentarios: [Informar abuso](https://go.microsoft.com/fwlink/?linkid=2249810).
  
- Microsoft podría deshabilitar las funciones controladas por Copilot para clientes seleccionados si se detecta un abuso de la funcionalidad.

## ¿Cuál son las limitaciones de Chatear con Copilot? ¿Cómo pueden los usuarios minimizar el impacto de las limitaciones de Chatear con Copilot al utilizar el sistema?

- Limitaciones generales de IA

  Los sistemas de IA son herramientas valiosas, pero no deterministas. Es posible que el contenido que generan no sea exacto. Por lo tanto, es importante utilizar su criterio para revisar y verificar las respuestas de Copilot antes de tomar decisiones que podrían afectar a las partes interesadas, como clientes y socios. Para la mayoría de las respuestas, Copilot también incluye citas o vínculos de referencia que puede utilizar para verificar rápidamente si Copilot ha llegado a la respuesta correcta. Por ejemplo, cuando se le pregunta cómo realizar alguna tarea, Copilot incluye vínculos al artículo de origen. Cuando se le pide que busque un registro según criterios específicos, Copilot incluye vínculos que describen la página de la lista que identificó como tema de conversación. También proporciona información sobre los filtros o la clasificación que se aplicó para llegar a una respuesta.

- Limitaciones de idioma

  - El chat solo se admite en inglés para las siguientes configuraciones regionales: en-AU, en-CA, en-GB, en-IE, en-IN, en-NZ, en-PH, en-SG, en-US, en- ZA.

    Si el idioma para mostrar en [!INCLUDE[prod_short](includes/prod_short.md)] no es una de estas configuraciones regionales, el chat no está disponible.

  - La calidad de las respuestas puede ser menor bajo las siguientes condiciones:
    - El idioma local es distinto de en-US.
    - La configuración de idioma para el usuario en [!INCLUDE[prod_short](includes/prod_short.md)] difiere del idioma principal de los datos en la base de datos de [!INCLUDE[prod_short](includes/prod_short.md)].

- Limitaciones específicas del sector, el producto y el tema

   El chat incluye mecanismos de seguridad integrados que evitan la generación no deseada de contenido dañino, como contenido sexual explícito o incitación a la violencia. A veces, los clientes operan en industrias, venden productos y servicios, o trabajan con procesos que naturalmente se superponen con lo que podría considerarse inadecuado en otros contextos, o trabajan con datos que podrían activar estas salvaguardas. Es posible que el chat no funcione tan bien en estos casos.

<!--## What operational factors and settings allow for effective and responsible use of the feature?-->

## ¿Qué datos recopila Chatear con Copilot y cómo se utilizan?

Microsoft no utiliza los datos de su empresa, incluido el texto que envía a Copilot, para entrenar los modelos de IA fundamentales en beneficio de otros. Los administradores de la empresa tienen control total para controlar estos datos que forman parte de su suscripción a Azure. Debido a que los administradores u otras personas de su empresa pueden tener acceso a estos datos según lo determine su empleador, recomendamos que no introduzca datos confidenciales como contraseñas u otros secretos.

## Qué ofrece Chatear con Copilot para seguridad

El chat está diseñado para ser seguro y se ejecuta bajo la identidad del usuario, heredando todos los permisos de seguridad y otras restricciones y nunca operando fuera de la seguridad de la plataforma [!INCLUDE[prod_short](includes/prod_short.md)]. Esto significa que Copilot solo puede obtener acceso a los datos a los que tiene acceso.

Para los usuarios con permiso SUPER, el chat puede localizar más fácilmente datos no seguros a los que normalmente es más difícil tener acceso para otros usuarios. Las organizaciones que no aplican el modelo de seguridad de [!INCLUDE[prod_short](includes/prod_short.md)] para restringir a qué tablas y objetos tiene acceso cada usuario o rol de usuario, pueden correr un riesgo elevado al usar el chat. Por lo tanto, recomendamos que su organización implemente el modelo de seguridad de [!INCLUDE[prod_short](includes/prod_short.md)] o desactive el chat.

## Consulte también

- [Chatear con Copilot (versión preliminar)](chat-with-copilot.md)

