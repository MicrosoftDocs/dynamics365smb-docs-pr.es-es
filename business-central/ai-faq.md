---
title: Preguntas frecuentes sobre el texto de marketing de productos impulsado por IA (versión preliminar) con Copilot
description: Obtenga respuestas a preguntas frecuentes sobre las capacidades de texto generado por IA con Copilot.
ms.author: jswymer
ms.reviewer: jswymer
ms.topic: faq
ms.date: 04/03/2023
ms.custom: bap-template
author: jswymer
ms.service: dynamics365-business-central
---

# <a name="ai-powered-item-marketing-text-preview-with-copilot-faq"></a>Preguntas frecuentes sobre el texto de marketing de productos impulsado por IA (versión preliminar) con Copilot

[!INCLUDE[ai-preview](includes/ai-preview.md)]

Este artículo usa preguntas y respuestas para explicar aspectos importantes sobre la tecnología de IA detrás de Copilot y el texto que genera.

## [General](#tab/general)

### <a name="what-is-copilot"></a>¿Qué es Copilot?

Copilot proporciona sugerencias de texto generadas por IA para artículos en Business Central. Está destinado a los usuarios que escriben texto de marketing para artículos para ayudarlos a producir contenido atractivo y convincente. Algunas principales ventajas son:

- Disminuye el tiempo utilizado en la redacción de textos publicitarios, lo que puede acelerar el tiempo de comercialización de los artículos que se venden en las tiendas en línea.
- Desbloquea la creatividad para proporcionar descripciones de productos más atractivas.
- Mejora la consistencia del material de marketing para las líneas de productos.

Los usuarios deben considerar el texto generado por IA como una sugerencia que debe revisarse y editarse para garantizar su precisión antes de que esté disponible públicamente.

### <a name="why-isnt-copilot-available-for-marketing-text-on-my-items-in-business-central"></a>¿Por qué Copilot no está disponible para texto de marketing en mis artículos en Business Central?

Para que Copilot esté disponible, se deben cumplir los siguientes requisitos:

- El idioma que usa en Business Central debe ser el inglés. Cualquiera de las configuraciones regionales disponibles en inglés servirá, como inglés (Estados Unidos), inglés (Reino Unido) o inglés (Sudáfrica).

  Para cambiar el idioma, en la esquina superior derecha, seleccione el icono **Configuración** ![Configuración](media/ui-experience/settings_icon_small.png "Icono de configuración para el área de trabajo") > **Mi configuración** > **Idioma**. Para obtener más información, vaya a [Cambiar configuración básica](ui-change-basic-settings.md#language).
- Debe usar Business Central Online, versión 22 o posterior (si se trata de un cliente existente) o una versión de prueba.  <!--**22.0.54157.54311 (Preview - Copilot edition)**-->

   Para comprobar la versión, seleccione el signo de interrogación en la esquina superior derecha, luego seleccione **Ayuda y soporte técnico**. En **Solución de problemas**, busque la versión de la aplicación. Para obtener información sobre cómo obtener la versión de versión preliminar correcta, vaya a [Comenzar con una versión preliminar de Business Central](ai-preview-getstarted.md).
- La característica en versión preliminar **Crear descripciones de productos con tecnología de IA con Copilot** debe estar habilitada.

   Para obtener más información, vaya a [Habilitar o deshabilitar la característica "Crear descripciones de productos con tecnología de IA con Copilot"](enable-ai.md#enable-or-disable-create-ai-powered-product-descriptions-with-copilot).
- Un administrador ha aceptado los términos y condiciones.

   Para obtener más información, vaya a [Aceptar o rechazar los términos y condiciones de versión preliminar y privacidad para todos los usuarios](enable-ai.md#consent-to-or-reject-preview-and-privacy-terms-and-conditions-for-all-users).

### <a name="is-copilot-available-for-preview-in-business-central-on-premises"></a>¿Copilot está disponible para versión preliminar en Business Central local?

No, no se admite actualmente en Business Central local.

### <a name="how-does-copilot-work-where-does-the-suggested-text-come-from"></a>¿Cómo funciona Copilot, de dónde viene el texto sugerido?

Copilot utiliza [el servicio Azure OpenAI de Microsoft](/azure/cognitive-services/openai/overview) para acceder a potentes modelos de lenguaje que analizan y generan lenguaje natural. Estos modelos han sido entrenados en un amplio cuerpo de conjuntos de datos de texto. Como resultado, Copilot puede generar respuestas sugeridas y personalizadas en inglés basadas en una cantidad mínima de datos de entrada, como los atributos, la categoría o la descripción de un artículo. 

### <a name="whats-the-quality-of-the-text-suggested-by-copilot"></a>¿Cuál es la calidad del texto sugerido por Copilot?

Debido a que la tecnología subyacente detrás de Copilot utiliza IA que ha sido entrenada en una amplia gama de orígenes, el contenido generado no siempre es real o adecuado. Algunas sugerencias pueden incluso incluir contenido cuestionable o inapropiado. Es su responsabilidad revisar y editar las sugerencias generadas para asegurarse de que sean precisas y apropiadas.

Para obtener información sobre sugerencias inapropiadas, vaya a [¿Qué se hace con las sugerencias de texto abusivas y dañinas?](/dynamics365/business-central/ai-faq?&tabs=oversight#whats-done-about-abusive-and-harmful-text-suggestions).

### <a name="how-can-i-improve-the-suggestions-i-get-from-copilot"></a>¿Cómo puedo mejorar las sugerencias que recibo de Copilot?

Hay algunas cosas que puede hacer para aprovechar al máximo las sugerencias de Copilot:

- Agregue más atributos a un artículo para promocionar las funciones y características específicas que le interesan.
- Cambie las opciones de tono de voz y énfasis de calidad para que coincidan con sus preferencias personales
- Mejore la descripción del producto.
- Asegúrese de que al artículo se le asigne la categoría más adecuada

Para obtener más información, vaya a [Mejorar y adaptar las sugerencias de texto](item-marketing-text.md#improve-and-tailor-text-suggestions).

### <a name="what-if-im-not-satisfied-with-the-generated-text"></a>¿Qué pasa si no estoy satisfecho con el texto generado?

Para ayudarnos a mejorar el texto, seleccione **¿Es una buena sugerencia?** en la página **Crear con Copilot**, que puede responder con un pulgar hacia arriba (Me gusta) o un pulgar hacia abajo (Necesita mejorar).

![Muestra una tarjeta de producto con panel de texto de marketing](media/create-with-copilot-window-feedback.png)

### <a name="can-admins-disable-copilot-if-so-how"></a>¿Pueden los administradores deshabilitar Copilot? Si es así, ¿cómo?

Business Central ofrece a los administradores dos formas de desactivar Copilot en la versión preliminar:

- No aceptar el aviso de privacidad de Azure OpenAI para todos los usuarios.

  O

- Desactivar la característica **Crear descripciones de productos con tecnología de IA con Copilot** en la página **Administración de características**.

Para obtener más información, vaya a [Configurar texto de marketing de artículos con tecnología de IA (versión preliminar) con Copilot como administrador](enable-ai.md).

## [Legitimidad](#tab/fairness)

### <a name="does-copilot-work-with-languages-other-than-english"></a>¿Copilot trabaja con otros idiomas además del inglés?

Actualmente, Copilot solo admite inglés. Es posible que se devuelvan respuestas inexactas cuando los usuarios conversan con el sistema en idiomas distintos al inglés.

## [Supervisión humana](#tab/oversight)

### <a name="whats-done-about-abusive-and-harmful-text-suggestions"></a>¿Qué se ha hecho con las sugerencias de texto abusivas y dañinas?

El servicio Azure OpenAI almacena indicaciones y finalizaciones del servicio para supervisar el uso abusivo y desarrollar y mejorar la calidad de los sistemas de administración de contenido de Azure OpenAI. [Obtén más información sobre nuestra gestión y filtrado de contenido.](/azure/cognitive-services/openai/concepts/content-filter)

Los empleados autorizados de Microsoft pueden acceder a sus datos de solicitud y finalización que han activado nuestros sistemas automatizados con el fin de investigar y comprobar posibles abusos; para los clientes que han implementado Azure OpenAI Service en la Unión Europea, los empleados autorizados de Microsoft estarán ubicados en la Unión Europea. Estos datos pueden utilizarse para mejorar nuestros sistemas de gestión de contenidos. En caso de que se confirme una infracción de la directiva, es posible que le pidamos que tome medidas inmediatas para remediar el problema y evitar más abusos. Si no se soluciona el problema, es posible que se suspenda o cancele el acceso a los recursos de Azure OpenAI.

Para obtener más información, consulte [Datos, privacidad y seguridad para Azure OpenAI Service](/legal/cognitive-services/openai/data-privacy#abuse-and-harmful-content-generation).

### <a name="can-i-opt-out-of-the-logging-and-human-review-process"></a>¿Puedo optar por no participar en el proceso de registro y revisión humana?

Como parte de proporcionar las versiones preliminares de Azure OpenAI, Microsoft procesará y almacenará los Datos del cliente enviados al servicio, así como el Contenido de salida, con el fin de supervisar y prevenir usos o resultados abusivos o dañinos del servicio; y desarrollar, probar y mejorar capacidades diseñadas para prevenir el uso abusivo y/o resultados dañinos del servicio. 

El personal autorizado de Microsoft puede revisar los datos que han activado nuestros sistemas automatizados para investigar y comprobar posibles abusos, y puede participar en una muestra aleatoria limitada de términos que no están marcados por nuestros sistemas automatizados para garantizar que los sistemas funcionen correctamente. El personal autorizado de Microsoft también puede acceder y usar estos datos para mejorar nuestros sistemas que supervisan y previenen usos o resultados abusivos o dañinos del servicio. Obtenga más información sobre [términos de versión preliminar](https://dynamics.microsoft.com/legaldocs/supp-dynamics365-preview/).

## [Privacidad](#tab/privacy)

### <a name="what-data-does-the-capability-collect-how-is-the-data-used"></a>¿Qué datos recopila la capacidad? ¿Cómo se usan los datos?

La capacidad recopila su respuesta a la pregunta **¿Es una buena sugerencia?** en la página **Crear con Copilot**, que puede responder con un pulgar hacia arriba (Me gusta) o un pulgar hacia abajo (Necesita mejorar).

Usaremos estos datos para evaluar y mejorar la calidad de la capacidad. Más información sobre qué datos se recopilan está disponible en los [términos de versión preliminar](https://dynamics.microsoft.com/legaldocs/supp-dynamics365-preview/).

![Muestra una tarjeta de producto con panel de texto de marketing](media/create-with-copilot-window-feedback.png)

---

## <a name="see-also"></a>Consulte también .

[Información general sobre el texto de marketing de productos impulsado por IA con Copilot](ai-overview.md)  
[Configurar texto de marketing de productos impulsado por IA con Copilot como administrador](enable-ai.md)  
[Cree texto de marketing para artículos usando Copilot](item-marketing-text.md)  

