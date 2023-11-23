---
title: Preguntas frecuentes para sugerencias de texto de marketing
description: 'Estas preguntas frecuentes brindan información sobre la tecnología de IA utilizada en Business Central, junto con consideraciones clave y detalles sobre cómo se usa la IA, cómo se probó y evaluó y cualquier limitación específica.'
ms.date: 10/07/2023
ms.custom:
  - responsible-ai-faqs
ms.topic: article
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
---

# Preguntas frecuentes para sugerencias de texto de marketing con Copilot

Estas preguntas frecuentes (FAQ) describen el impacto de la función [!INCLUDE[feature-marketing-text-suggestions](includes/feature-marketing-text-suggestions.md)] de IA en [!INCLUDE[prod_short](includes/prod_short.md)].

## ¿Qué son las sugerencias de texto de marketing de productos?

Copilot proporciona asistencia de redacción a los usuarios responsables de la creación de textos de marketing (también conocidos como copia) de los elementos de [!INCLUDE[prod_short](includes/prod_short.md)]. Esta característica se conoce como [!INCLUDE[feature-marketing-text-suggestions](includes/feature-marketing-text-suggestions.md)]. La característica [!INCLUDE[feature-marketing-text-suggestions](includes/feature-marketing-text-suggestions.md)] proporciona asistencia de redacción a los usuarios responsables de la creación de textos de marketing (también conocidos como *copia*) de los elementos de [!INCLUDE[prod_short](includes/prod_short.md)].

La función está disponible en cualquier tarjeta de artículo en [!INCLUDE[prod_short](includes/prod_short.md)]. Para usarlo, simplemente abra un elemento y luego seleccione **Texto de marketing** > **Borrador con Copilot**. Esta acción genera automáticamente una sugerencia de texto atractiva, creativa y específica para el elemento que se muestra. Las sugerencias se basan en diversos aportes, entre ellos:

- Los atributos, la categoría y el nombre del artículo.
- Preferencias personales de estilo de escritura, como tono de voz, calidad enfatizada, formato y extensión.

Puede cambiar el valor de estas opciones de entrada para influir en el resultado del texto generado por IA. Antes de guardar una sugerencia, puede revisarla y editarla fácilmente para verificar su precisión o probar otra sugerencia.

Algunos beneficios clave de esta característica incluyen:

- Disminuye el tiempo utilizado en la redacción de textos publicitarios, lo que puede acelerar el tiempo de comercialización de los artículos que se venden en las tiendas en línea.
- Desbloquea la creatividad para proporcionar descripciones de productos más atractivas.
- Mejora la consistencia del material de marketing para las líneas de productos.

## ¿Cuáles son las capacidades del sistema?

La caracetrística [!INCLUDE[feature-marketing-text-suggestions](includes/feature-marketing-text-suggestions.md)] usa [el Servicio Azure OpenAI de Microsoft](/azure/cognitive-services/openai/overview) para acceder a modelos de lenguaje eficaces que analizan y generan texto basado en lenguaje natural. Estos modelos han sido entrenados en un amplio cuerpo de conjuntos de datos de texto. Como resultado, Copilot puede generar respuestas sugeridas y personalizadas en inglés basadas en una cantidad mínima de datos de entrada, como los atributos, la categoría o la descripción de un artículo. 

## ¿Cuál es el uso previsto del sistema?

Esta función está destinada a ayudar a los usuarios a crear textos de marketing para artículos en [!INCLUDE[prod_short](includes/prod_short.md)]. Los escritores utilizan la función para obtener rápidamente sugerencias de texto atractivas y atractivas, que luego se revisan y editan para garantizar su precisión. 

## ¿Cómo se evaluó el texto de marketing de artículos? ¿Qué métricas se utilizan para medir el rendimiento?

- La función se sometió a pruebas exhaustivas en las que expertos en idiomas evaluaron numerosos textos en diferentes idiomas según varios criterios. Las pruebas se basaron en los datos de demostración de [!INCLUDE[prod_short](includes/prod_short.md)] y otros catálogos de productos ficticios.
- Esta característica está construida de acuerdo con el Estándar de IA Responsable de Microsoft. [Obtenga más información sobre la IA responsable de Microsoft](https://aka.ms/RAI).

## ¿Cómo monitorea Microsoft la calidad del contenido generado?

Microsoft cuenta con varios sistemas para garantizar que las capacidades de Copilot permanezcan operativas y generen contenido de la más alta calidad.

- Los usuarios tienen la oportunidad de proporcionar comentarios para denunciar contenido inapropiado y mejorar la funcionalidad.

  - Si encuentra contenido generado inapropiado, infórmelo a Microsoft mediante este formulario de comentarios: [Informar abuso](https://go.microsoft.com/fwlink/?linkid=2249810). 

    Microsoft podría deshabilitar las funciones controladas por Copilot para clientes seleccionados si se detecta un abuso de la funcionalidad. 

  - Realizamos un seguimiento de los comentarios de los usuarios en [!INCLUDE[feature-marketing-text-suggestions](includes/feature-marketing-text-suggestions.md)] para ayudarnos a mejorar las sugerencias. 

    Para proporcionar comentarios, utilice el ícono Me gusta (pulgar hacia arriba) o No me gusta (pulgar abajo) en la página de **Copilot** en [!INCLUDE[prod_short](includes/prod_short.md)]. Recopilamos la telemetría de estos gestos para cada salida de IA para la que envía comentarios.

    ![Muestra una tarjeta de producto con panel de texto de marketing](media/create-with-copilot-window-feedback.svg)

- El servicio Azure OpenAI almacena indicaciones y finalizaciones del servicio para supervisar el uso abusivo y desarrollar y mejorar la calidad de los sistemas de administración de contenido de Azure OpenAI. [Obtén más información sobre nuestra gestión y filtrado de contenido.](/azure/cognitive-services/openai/concepts/content-filter). Los datos de su empresa no se utilizan para entrenar modelos de IA en el servicio Azure OpenAI.

   Los empleados autorizados de Microsoft pueden acceder a sus datos de solicitud y finalización que han activado nuestros sistemas automatizados con el fin de investigar y comprobar posibles abusos; para los clientes que utilizan [!INCLUDE[prod_short](includes/prod_short.md)] en la Unión Europea, los empleados autorizados de Microsoft están ubicados en la Unión Europea. Estos datos pueden utilizarse para mejorar nuestros sistemas de gestión de contenidos. En caso de que se confirme una infracción de la directiva, es posible que le pidamos que tome medidas inmediatas para remediar el problema y evitar más abusos. Si no se soluciona el problema, es posible que se suspenda o cancele el acceso a los recursos de Azure OpenAI.

   Para obtener más información, consulte [Datos, privacidad y seguridad para Azure OpenAI Service](/legal/cognitive-services/openai/data-privacy#abuse-and-harmful-content-generation).

## ¿Existe un proceso de registro y revisión humana como parte del servicio Azure OpenAI? Si es así, ¿puedo excluirme?  

Como parte de proporcionar las versiones preliminares del servicio Azure OpenAI, Microsoft procesará y almacenará los Datos del cliente enviados al servicio, así como el Contenido de salida, con el fin de supervisar y prevenir usos o resultados abusivos o dañinos del servicio; y desarrollar, probar y mejorar capacidades diseñadas para prevenir el uso abusivo y/o resultados dañinos del servicio. 

El personal autorizado de Microsoft puede revisar los datos que han activado nuestros sistemas automatizados para investigar y comprobar posibles abusos, y puede participar en una muestra aleatoria limitada de términos que no están marcados por nuestros sistemas automatizados para garantizar que los sistemas funcionen correctamente. El personal autorizado de Microsoft también puede acceder y usar estos datos para mejorar nuestros sistemas que supervisan y previenen usos o resultados abusivos o dañinos del servicio. Obtenga más información sobre [términos de versión preliminar](https://dynamics.microsoft.com/legaldocs/supp-dynamics365-preview/).

Para que Microsoft proteja el servicio y a sus clientes, no es posible optar por no participar en los procesos de registro y revisión humana.

## ¿Qué datos recopila la capacidad? ¿Cómo se usan los datos?

La capacidad de sugerencias de textos de marketing recopila los datos mínimos requeridos por Business Central para ofrecer el servicio. Para obtener más información, consulte [Términos de Dynamics 365 para características impulsadas por Azure OpenAI](https://go.microsoft.com/fwlink/?linkid=2236010).

La capacidad también recopila datos de los comentarios que el usuario puede proporcionar usando los íconos Me gusta (pulgar hacia arriba) o No me gusta (pulgar abajo) en la parte superior de la página de **Copilot**. Los datos son anónimos e incluyen la elección de Me gusta o No me gusta, el motivo de la No me gusta, si se proporciona, y la función Copit a la que se aplica el comentario. Usaremos estos datos para evaluar y mejorar la calidad de la capacidad.

## ¿Cuáles son las limitaciones actuales de [!INCLUDE[feature-marketing-text-suggestions](includes/feature-marketing-text-suggestions.md)]? ¿Cómo pueden los usuarios minimizar el impacto de las limitaciones de [!INCLUDE[feature-marketing-text-suggestions](includes/feature-marketing-text-suggestions.md)] cuando usan el sistema?

- Debido a que la tecnología subyacente detrás de la característica utiliza IA que ha sido entrenada en una amplia gama de orígenes, el contenido generado no siempre es real o adecuado. Algunas sugerencias pueden incluso incluir contenido cuestionable o inapropiado. Es su responsabilidad revisar y editar las sugerencias generadas para asegurarse de que sean precisas y apropiadas.
- [!INCLUDE[copilot-supported-languages.md](includes/copilot-supported-languages.md)]

  Es posible que se devuelvan respuestas inexactas cuando los usuarios interactúan con el sistema en los idiomas admitidos. Además, se puede generar texto inexacto cuando el idioma del usuario y el idioma de los datos principales en la base de datos [!INCLUDE[prod_short](includes/prod_short.md)] no son idénticos.


## ¿Qué factores operativos y configuraciones permiten un uso eficaz y responsable del sistema?

Hay algunas cosas que puede hacer para aprovechar al máximo la característica:

- Agregue más atributos a un artículo para promocionar las funciones y características específicas que le interesan.
- Cambie las opciones de tono de voz y énfasis de calidad para que coincidan con sus preferencias personales
- Mejore la descripción del producto.
- Asegúrese de que al artículo se le asigne la categoría más adecuada

Para obtener más información, vaya a [Mejorar y adaptar las sugerencias de texto](item-marketing-text.md#improve-and-tailor-text-suggestions).

> [!TIP]
> Revise siempre la precisión de las sugerencias antes de guardarlas y publicarlas para consumo público.


## Consulte también .

- [Sugerencias de texto de marketing](ai-overview.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]