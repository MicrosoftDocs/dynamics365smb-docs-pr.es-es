---
title: Preguntas frecuentes sobre la asignación de documentos electrónicos con pedidos de compra
description: 'Estas preguntas frecuentes brindan información sobre la tecnología de IA utilizada en Business Central, junto con consideraciones clave y detalles sobre cómo se usa la IA, cómo se probó y evaluó y cualquier limitación específica.'
ms.date: 02/23/2024
ms.custom:
  - responsible-ai-faqs
ms.topic: article
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.collection:
  - bap-ai-copilot
---

# Preguntas frecuentes sobre la asignación de documentos electrónicos con pedidos de compra mediante Copilot (versión preliminar)

[!INCLUDE [preview-banner](~/../shared-content/shared/preview-includes/preview-banner.md)]

Estas preguntas frecuentes (P+F) describen el impacto de la característica **Asistencia para la concordancia de documentos electrónicos** en [!INCLUDE [prod_short](includes/prod_short.md)].

[!INCLUDE [preview-note](~/../shared-content/shared/preview-includes/production-ready-preview-dynamics365.md)]

## ¿Qué es la asistencia para la concordancia de documentos electrónicos?

Los documentos electrónicos sirven como base para transacciones comerciales modernas. Representan trámites críticos, como facturas y recibos, que fluyen en ambas direcciones a través de la entrega y la recepción. Puede generar y transmitir facturas electrónicas de forma digital en un formato estructurado que facilita el procesamiento automatizado de facturas. Sin embargo, el manejo de facturas digitales entrantes puede resultar más complicado para los equipos de cuentas por pagar.  

En las pequeñas y medianas empresas (PYMES), el equipo de cuentas por pagar desempeña un papel fundamental en el seguimiento preciso de las obligaciones de los proveedores. Su principal responsabilidad es registrar con precisión las facturas entrantes. Lograr precisión puede requerir esfuerzo, particularmente cuando concilian facturas externas de proveedores con órdenes de compra existentes. Las discrepancias en códigos, descripciones y unidades de medida a menudo presentan desafíos porque estos elementos pueden no coincidir en diferentes sistemas y empresas. Además, los costes inesperados, como las tarifas de transporte, pueden aparecer como partidas separadas que necesitan ajuste manual. Los contables también deben incluir números y fechas de factura en los documentos. Es importante destacar que la relación entre las órdenes de compra y las facturas externas no siempre es uno a uno. Es posible que reciba varias facturas externas por la misma orden de compra.

Históricamente, [!INCLUDE [prod_short](includes/prod_short.md)] podría generar nuevas facturas de compra basadas en las facturas electrónicas recibidas. Sin embargo, cotejar manualmente las facturas con las órdenes de compra existentes era un proceso que requería mucho tiempo y era propenso a errores.

**Asistencia para la concordancia de documentos electrónicos** utiliza IA generativa para agilizar este proceso automatizando el análisis de facturas electrónicas externas. La función permite a los contadores pedirle a Copilot que haga coincidir las líneas de las facturas electrónicas entrantes con las líneas de las órdenes de compra en [!INCLUDE [prod_short](includes/prod_short.md)].

## ¿Cuáles son las capacidades de la asistencia para la concordancia de documentos electrónicos?

Copilot brinda asistencia basada en inteligencia artificial para hacer coincidir la factura digital recibida con las órdenes de compra existentes [!INCLUDE [prod_short](includes/prod_short.md)]. Copilot relaciona líneas basándose en lo siguiente:

- Similitud de descripciones
- Unidades de medida
- Cantidades disponibles para facturar
- Cantidades

Copilot identifica descripciones similares si tienen la unidad de medida y los precios adecuados, pero también puede encontrar coincidencias en casos más complejos. Por ejemplo, puede identificar si una factura electrónica tiene dos líneas con una variante del mismo artículo, y solo una línea en la orden de compra; [!INCLUDE [prod_short](includes/prod_short.md)] coincide con estas líneas siempre que las descripciones sean similares y los precios sean los mismos.

Copilot no se conecta a su servicio de punto final de documentos electrónicos para recuperar o enviar comprobantes digitales. Esta tarea permanece totalmente bajo su control y es un requisito previo para utilizar la asistencia de Copilot. Esto es cierto, independientemente de si los documentos digitales se agregan a [!INCLUDE [prod_short](includes/prod_short.md)] mediante una conexión con un servicio de punto final o se introducen manualmente.  

## ¿Cuál es el uso previsto de la asistencia para la concordancia de documentos electrónicos?  

El objetivo de la característica **Asistencia para la concordancia de documentos electrónicos** es ayudar al equipo de cuentas por pagar a cotejar las órdenes de compra existentes con las facturas electrónicas entrantes. Gran parte de esta actividad gira en torno a la coincidencia de cadenas. [!INCLUDE [prod_short](includes/prod_short.md)] ofrece una característica que automatiza parte de esta actividad, y los LLM se han identificado como una oportunidad para complementar esa función y reducir aún más el esfuerzo manual.  

## ¿Cómo se evaluó la asistencia para la concordancia de documentos electrónicos? ¿Qué métricas se utilizan para medir el rendimiento?

Esta característica se probó utilizando combinaciones de la siguiente información:

- Descripciones de elementos externos
- Unidades de medida
- Cantidades e importes
- Descripción de productos estándar
- Idiomas diferentes
- Otros parámetros que cubren las variaciones típicas y límites de datos para cada campo 

Los datos de prueba representan tanto el uso típico como el uso por parte de malos actores. Se midió el rendimiento en comparación con la comparación manual de los mismos datos en facturas electrónicas y órdenes de compra.

## ¿Cuáles son las limitaciones de la asistencia para la concordancia de documentos electrónicos? ¿Cómo pueden los usuarios minimizar el impacto de las limitaciones de asistencia para la concordancia de documentos electrónicos?

La **Asistencia para la concordancia de documentos electrónicos** funciona mejor cuando las descripciones de elementos externas (factura electrónica) e internas ([!INCLUDE [prod_short](includes/prod_short.md)]) y las unidades de medidas están en el mismo idioma. Los idiomas mixtos o el lenguaje mixto de las descripciones de productos a menudo resultan en menos coincidencias y sugerencias.  

La combinación sugerida de artículos de facturas electrónicas con artículos de órdenes de compra funciona mejor en inglés. Aunque puede utilizar esta función en cualquier idioma compatible [!INCLUDE [prod_short](includes/prod_short.md)], es posible que experimente menos coincidencias de elementos en otros idiomas. Para más información sobre el idioma, vaya a [¿En qué geografías e idiomas está disponible la asistencia para la concordancia de documentos electrónicos?](#in-which-geographies-and-languages-is-e-documents-matching-assistance-available).

## ¿En qué geografías e idiomas está disponible la asistencia para la concordancia de documentos electrónicos?

- Geografías disponibles

   La característica de Copilot está disponible en todos los [países o regiones de Business Central](/dynamics365/business-central/dev-itpro/compliance/apptest-countries-and-translations) admitidos. No obstante, para que los entornos de clientes ubicados en países o regiones donde el servicio Azure OpenAI no está implementado, los administradores primero deben dar su consentimiento para permitir el movimiento de datos a través de las fronteras para que [!INCLUDE [prod_short](includes/prod_short.md)] se conecte al servicio Azure OpenAI y para que esta capacidad esté disponible. Obtenga más información sobre el [movimiento de datos de Copilot entre geografías](ai-copilot-data-movement.md).

- Idiomas disponibles

   [!INCLUDE[e-docs-matching-language-support](includes/e-docs-matching-language-support.md)]

## ¿Qué factores operativos y configuraciones permiten un uso eficaz y responsable de la característica?

Copilot complementa el algoritmo de asignación que [!INCLUDE [prod_short](includes/prod_short.md)] ya proporciona y asigna las líneas que el algoritmo no proporcionó.

### ¿Qué se espera de los usuarios al utilizar la asistencia para la concordancia de documentos electrónicos?

<!--Not sure that this is the right content for this section. Seems like it belongs more in the overview article because it's more related to how to use the feature-->

Después de asignar facturas electrónicas entrantes a órdenes de compra, debe asignar las líneas de los documentos.

La página **Asignación de órdenes de compra** muestra todas las líneas de ambos documentos. Aquí puede realizar la asignación manualmente, lo que puede resultar difícil si hay muchas líneas.

Puede utilizar **Asistencia para la concordancia de documentos electrónicos** para asignar líneas según los siguientes criterios:

- Similitud de sus descripciones
- Unidades de medida
- Cantidades disponibles para facturar
- Cantidades

Las coincidencias de Copilot pueden ser incorrectas o incompletas. Siempre debe revisar su exactitud antes de decidir conservarlas. Las coincidencias y sugerencias de Copilot se guardan en [!INCLUDE [prod_short](includes/prod_short.md)] cuando elige **Mantenerlo** y sale de Copilot. También puede editar y corregir cualquier coincidencia o sugerencia antes de optar por conservarla. 

### ¿Qué se espera de los administradores y usuarios cuando operan la asistencia para la concordancia de documentos electrónicos?

Los usuarios, como contables, tesoreros u otras personas que reciben facturas electrónicas, siempre deben revisar la exactitud de las coincidencias y sugerencias proporcionadas por Copilot antes de optar por conservarlas. Le recomendamos que revise las líneas de la orden de compra para verificar su exactitud y encontrar cualquier discrepancia. Usted decide si desea utilizar la **Asistencia para la concordancia de documentos electrónicos**. Incluso cuando la **Asistencia para la concordancia de documentos electrónicos** está activada por los administradores y disponible, puede elegir utilizarla siempre, a veces o nunca.  

Los administradores toman la decisión general sobre si utilizar Copilot en [!INCLUDE [prod_short](includes/prod_short.md)]. Si habilitan Copilot, los administradores deben asegurarse de que conceden el acceso a las personas adecuadas.

> [¡NOTA!]
> - No admitimos esta característica para [!INCLUDE [prod_short](includes/prod_short.md)] local o en nubes privadas.
> - Los partners no pueden ampliar esta característica. Los desarrolladores asociados no pueden modificar, reemplazar ni ampliar esta característica. 

## ¿Es Copilot la única manera de hacer coincidir los documentos electrónicos con las órdenes de compra?  

No, usted decide si utiliza Copilot. [!INCLUDE [prod_short](includes/prod_short.md)] ofrece formas sin tecnología de IA para relacionar artículos de la factura electrónica recibida con artículos de órdenes de compra en [!INCLUDE [prod_short](includes/prod_short.md)]. Las organizaciones también pueden utilizar ambos enfoques al mismo tiempo.  

## ¿Cómo doy comentarios sobre el contenido generado por IA?  

Cada vez que Copilot proporciona coincidencias o sugerencias, puede proporcionar comentarios a Microsoft directamente desde la ventana de Copilot, utilizando los controles **Me gusta** y **No me gusta**. Sus comentarios permanecen anónimos y utilizamos estos datos para mejorar la calidad del servicio.  

## Consulte también

[Información general de documentos electrónicos](finance-edocuments-overview.md)  
[Asignar documentos electrónicos a líneas de pedido de compra con Copilot](map-edocuments-with-copilot.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
