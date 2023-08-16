---
title: Información general sobre el texto de marketing de productos impulsado por IA (versión preliminar) con Copilot
description: Obtenga información general de las capacidades de generación de contenido de IA en Business Central.
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.topic: overview
ms.date: 03/16/2023
ms.custom: bap-template
---
# Información general sobre el texto de marketing de productos impulsado por IA (versión preliminar) con Copilot

[!INCLUDE[ai-preview](includes/ai-preview.md)]

Este artículo ofrece una descripción general de la capacidad impulsada por IA proporcionada por Copilot en Business Central.

## ¿Qué es el texto de marketing de productos impulsado por IA con Copilot?

Copilot proporciona asistencia de escritura impulsada por IA para los usuarios de Business Central responsables de la creación de textos de marketing (descripciones de productos) en artículos vendidos en tiendas en línea, como Shopify. Con el clic de un botón, Copilot genera texto que es atractivo y creativo y destaca los atributos clave del elemento específico. Con un poco de revisión y edición, está listo para publicarse.

Copilot usa el [Servicio Microsoft Azure OpenAI](/azure/cognitive-services/openai/overview) para acceder a modelos de lenguaje que reconocen, predicen y generan texto basado en conjuntos de datos entrenados.

<br><br>  

> [!Video https://www.microsoft.com/en-us/videoplayer/embed/RWZdAr]

*El video no refleja exactamente cómo funciona o se ve la característica actualmente en el producto. La característica ha cambiado ligeramente desde que se produjo el vídeo. Pero le da una idea general de la función y para qué puede usarla*.
  
## Dónde se usa

Copilot está disponible en tarjetas de artículos en Business Central. En Business Central, los artículos son como productos en otras aplicaciones y tiendas. Cada artículo se puede administrar desde una tarjeta donde introduce detalles sobre el artículo, como sus dimensiones, coste o imagen. Esta tarjeta también incluye un cuadro para introducir texto de marketing. Este texto de marketing se puede publicar en su tienda en línea para promocionar el artículo. Aquí es donde entra Copilot. Simplemente seleccionando la acción **Crear con Copilot** en la tarjeta del artículo, Copilot generará un borrador de texto inteligente para usted. Una vez que obtenga el primer borrador, puede ejecutar Copilot una y otra vez hasta que obtenga un borrador que le guste. Cuando tiene una sugerencia que le gusta, la revisa y la edita para comprobar su precisión y luego la guarda.

Si Business Central está configurado para conectarse a su tienda en línea en Shopify, puede llevar este texto aún más lejos al publicarlo con el artículo directamente en su tienda seleccionando **Agregar a Shopify**.

## Por qué y cómo usarlo

El texto generado por IA puede ayudarle a acelerar el tiempo de comercialización de los productos en las tiendas en línea, al limitar el tiempo utilizado en la redacción de textos publicitarios. Algunas principales ventajas son:

- Ayuda a los usuarios a superar el bloqueo del escritor al comenzar con un borrador inteligente.
- Desbloquea la creatividad para proporcionar descripciones de productos más atractivas.
- Mejora la consistencia del contenido de marketing para las líneas de productos.

Debe pensar en el texto generado por IA solo como una **sugerencia**. Las sugerencias pueden, en algunos casos, contener errores e incluso texto inapropiado, por lo que se requiere supervisión y revisión humana. Antes de poner el texto a disposición del público, debe revisarlo para comprobar su precisión y realizar los cambios apropiados.

## Limitaciones actuales

Esta sección explica las limitaciones actuales de la capacidad de texto generado por IA proporcionada por Copilot.

- Las sugerencias de texto generadas por IA solo están en inglés.
- Pueden surgir sugerencias deficientes cuando se usan nombres de productos vagos o genéricos y faltan detalles sobre un artículo, como atributos clave o una categoría.
- Copilot solo es compatible con Business Central Online, no con entornos de nube privada ni entornos locales de Business Central.
- Copilot no es compatible a través de conexiones a su propio recurso de Azure OpenAI Service en su suscripción de Azure.
- No se admite la extensibilidad de partners de la capacidad de IA mediante el uso de código AL.

## Pasos siguientes

Para comenzar, necesitará un entorno de Business Central, versión 22, que esté habilitado con Copilot.

- Si ya es cliente de Business Central, su administrador de Business Central tendrá que configurar un entorno de la versión 22 para usted.
- Si no es cliente de Business Central pero desea probarlo, puede registrarse para obtener una prueba gratuita.

Para obtener más información, vaya a [Obtener la versión preliminar de Business Central](ai-preview-getstarted.md).  

## Consulte también .

[Configurar texto de marketing de productos impulsado por IA como administrador](enable-ai.md)  
[Crear texto de marketing con Copilot](item-marketing-text.md)  
[Preguntas frecuentes del texto de marketing de productos impulsado por IA con Copilot](ai-faq.md)  
[Comenzar con el conector Shopify](shopify/get-started.md)  
