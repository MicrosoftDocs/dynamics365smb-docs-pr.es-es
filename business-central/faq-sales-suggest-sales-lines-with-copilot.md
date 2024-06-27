---
title: Preguntas frecuentes para sugerir líneas de venta con Copilot
description: Estas preguntas frecuentes proporcionan información sobre la tecnología de IA utilizada en Business Central.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: article
ms.search.form: null
ms.date: 02/02/2024
ms.service: dynamics-365-business-central
ms.collection: bap-ai-copilot
ms.custom: responsible-ai-faqs
---

# Preguntas frecuentes sobre sugerencias de líneas de ventas con Copilot (versión preliminar)

[!INCLUDE [preview-banner](~/../shared-content/shared/preview-includes/preview-banner.md)]

Estas preguntas frecuentes (P+F) describen el impacto de la característica de IA en la característica de sugerencias de líneas de venta en [!INCLUDE [prod_short](includes/prod_short.md)].

[!INCLUDE [preview-note](~/../shared-content/shared/preview-includes/production-ready-preview-dynamics365.md)]

## ¿Qué son las sugerencias de líneas de ventas con Copilot?

La sugerencia de líneas de ventas con Copilot puede ayudar a crear líneas en documentos de ventas, como cotizaciones de ventas, pedidos y facturas, basadas en entradas estructuradas o lenguaje natural. La función no es un chat de propósito general, sino una experiencia altamente específica e integrada que puede utilizar en documentos de ventas. La función ofrece dos capacidades distintas que le ayudan a encontrar datos sobre productos individuales o documentos completos.

## ¿Cuáles son las capacidades de las sugerencias de líneas de ventas con Copilot?

* Encontrar productos

  La información que describe los productos se almacena en varios lugares de [!INCLUDE [prod_short](includes/prod_short.md)]. Por ejemplo, los números de artículo y las descripciones se almacenan en la tabla **Artículo**, se almacenan varios códigos de barras en la tabla **Referencia del artículo** y las propiedades del producto se almacenan en la tabla **Atributos del artículo**. Si bien puede solicitar *bicicleta roja*, el producto real podría ser *turismo carmesí*, dónde *Bicicleta* es una categoría de producto y *rojo* es un atributo.

* Buscar un documento por referencia

  La gente suele repetir un pedido anterior, o al menos utilizarlo como punto de partida. Pero puede resultar complicado encontrar el orden correcto en una pila de pedidos. Es posible que recuerde parte del ID del pedido, que puede ser un número asignado por la empresa o un número de referencia recibido de un cliente. Ser capaz de utilizar indicaciones como *Necesita la última factura de abril* debería ayudarle a encontrar un pedido más rápido.

## ¿Cuál es el uso previsto de las sugerencias de líneas de ventas con Copilot?

* Encontrar productos

  Diseñado para responder a las solicitudes de los usuarios para encontrar productos basados en descripciones vagas, incompletas o inexactas.

  Debido a que el número promedio de artículos (productos/servicios) para clientes de [!INCLUDE [prod_short](includes/prod_short.md)] es 10.000, encontrar los correctos puede ser difícil sin experiencia o conocimientos previos. La forma en que se almacenan los datos en [!INCLUDE [prod_short](includes/prod_short.md)] no facilita las cosas, porque es necesario realizar múltiples búsquedas o ejercicios de filtrado en las diferentes páginas que almacenan datos de productos.

  Copilot extrae los productos y las cantidades solicitados e identifica el término y los atributos de búsqueda principales, para que pueda introducir su mensaje más rápidamente. Luego, Copilot realiza una búsqueda avanzada a través de múltiples tablas relacionadas, aplica sinónimos, corrige errores tipográficos y evalúa la calidad del resultado de la búsqueda.

* Buscar un documento por referencia

  Destinado a responder consultas de los usuarios para encontrar documentos de venta existentes para un cliente específico utilizando información parcial o aproximada.

  En entornos B2B, las personas suelen lidiar con solicitudes recurrentes y los procesadores de pedidos pueden recibir consultas para repetir un documento anterior o al menos usarlo como punto de partida. Pero puede resultar complicado encontrar uno por varias razones:

  - A lo largo de su ciclo de vida, un documento de ventas puede evolucionar desde una cotización hasta un pedido, una factura contabilizada o un envío. Los documentos también se pueden archivar.
  - Es posible que tenga un identificador exacto, pero no pueda decir qué representa. Por ejemplo, ¿es el número de pedido, el número de factura o la referencia externa?
  - A veces se tiene una fecha o un período, pero no un documento de identidad.

  Para encontrar un documento fuente manualmente, deberá abrir varias páginas y utilizar la búsqueda y el filtro varias veces. Sin embargo, Copilot puede simplificar esto en una única consulta en lenguaje natural que le permite expresar lo que está buscando a su manera. 

  * *Obtener productos del pedido 103031*
  * *Necesito productos de la última factura en agosto*

## ¿Cómo se evaluaron las sugerencias de líneas de ventas con Copilot? ¿Qué métricas se utilizan para medir el rendimiento?

La característica se sometió a pruebas exhaustivas en las que se incluyeron numerosos mensajes en inglés de EE. UU. que representan tanto el uso típico como el uso por parte de malos actores. Las pruebas se basaron en los datos de demostración de [!INCLUDE [prod_short](includes/prod_short.md)] y en un gran catálogo de productos etiquetados disponible como código abierto.

Esta característica está construida de acuerdo con el Estándar de IA Responsable de Microsoft. [Obtenga más información sobre la IA responsable de Microsoft](https://aka.ms/RAI).

## ¿Cuáles son las limitaciones de las sugerencias de líneas de ventas con Copilot? ¿Cómo pueden los usuarios minimizar el impacto de las sugerencias de la línea de ventas con las limitaciones de Copilot al utilizar el sistema?

* Encontrar productos
  
  La búsqueda de productos funciona mejor en idioma inglés. Si bien puede utilizar esta característica en cualquiera de los idiomas que [!INCLUDE [prod_short](includes/prod_short.md)] admite, las búsquedas de artículos en otros idiomas pueden ser menos precisas.

Si su industria o dominio se superpone con lo que Microsoft considera temas delicados (como drogas, violencia, entretenimiento para adultos, etc.), Copilot podría optar por respuestas neutrales y seleccionadas o dar respuestas inexactas.

Las sugerencias de líneas de ventas solo completan los campos **Tipo** como **Producto**, **N.º** y **Cantidad** como se describe. Otros campos, incluyendo **Unidad de medida**, **Precio unitario**, y **Ubicación** utilizan la lógica actual y se completan en función de la configuración del elemento o de los valores heredados del encabezado del documento.

Actualmente no se admite el **Código variante**. Si puede enviar un producto en dos colores diferentes, por ejemplo, Copilot encontrará el producto necesario pero dejará el campo **Cód. variante** vacío. Tendrá que rellenar el campo manualmente.

El nombre que dé a sus productos puede afectar a los resultados Por ejemplo, el uso de abreviaturas crípticas en lugar de nombres descriptivos puede reducir la calidad de la salida.

Para los productos, la siguiente tabla enumera las tablas y campos que busca Copilot.

|Escritorio  |Campos  |
|---------|---------|
|**Artículos**     |  * N.º<br>* Descripción<br>* Descripción 2<br>* Alias<br>* GTIN<br>* Número de producto de proveedor       |
|**Variante producto**     | * Código<br>* Descripción<br>* Descripción 2          |
|**Referencia artículo**     | * N.º referencia<br>* Descripción<br>* Descripción 2        |
|**Atributos de producto**     | * Nombre<br>* Valor        |
|**Categoría producto**     |  * Código<br>* Descripción<br>* Categoría principal: nivel 1           |
|**Traducción producto**     | * Idioma<br>* Descripción<br>* Descripción 2          |
|**Identificador producto**     |  * Código       |
|**Lín. texto adicional**     |  * Texto      |

* Encontrar documentos por referencia

  Actualmente, puede iniciar la sugerencia de líneas de ventas a partir de pedidos de venta, facturas y cotizaciones, y buscar en los siguientes documentos:

  * Pedidos de venta
  * Ofertas de venta
  * Facturas de venta
  * Facturas venta reg.
  * Históricos albaranes venta

  Copilot busca en los siguientes campos

  * N.º de documento
  * N.º documento externo
  * Su ref.
  * N.º oferta
  * Fecha emisión documento
  * N.º de cliente de venta

  Copilot no devuelve todas las líneas del tipo Producto. Solo se transfieren números de productos, códigos de variante y cantidades. Las cantidades del documento fuente se convierten a la **Unidad de medida de ventas**.

## ¿En qué geografías e idiomas están disponibles las sugerencias de líneas de venta?

- Geografías disponibles

   La característica de Copilot está disponible en todos los [países o regiones de Business Central](/dynamics365/business-central/dev-itpro/compliance/apptest-countries-and-translations) admitidos. No obstante, para que los entornos de clientes ubicados en países o regiones donde el servicio Azure OpenAI no está implementado, los administradores primero deben dar su consentimiento para permitir el movimiento de datos a través de las fronteras para que [!INCLUDE [prod_short](includes/prod_short.md)] se conecte al servicio Azure OpenAI y para que esta capacidad esté disponible. Obtenga más información sobre el [movimiento de datos de Copilot entre geografías](ai-copilot-data-movement.md).

- Idiomas disponibles

   [!INCLUDE[sales-lines-suggestions-language-support](includes/sales-lines-suggestions-language-support.md)]

## ¿Qué factores operativos y configuraciones permiten un uso eficaz y responsable de la característica?

Las sugerencias basadas en IA a veces pueden ser incorrectas o incompletas. Siempre debe revisar la exactitud de las sugerencias de Copilot antes de decidir si desea conservarlas. Las sugerencias de Copilot no se guardan en la base de datos de [!INCLUDE [prod_short](includes/prod_short.md)] hasta que elija el botón **Conservar** y salga de la ventana de Copilot. Puede editar y corregir cualquier sugerencia antes de decidir conservarla o después de insertarla en un documento de ventas.

### ¿Qué se espera de los administradores y usuarios finales cuando usan sugerencias de líneas de venta?

Cada usuario individual elige si utilizar o no **Sugerencias de líneas de venta**. Incluso cuando la función está habilitada por los administradores y está disponible, puede elegir usarla siempre, a veces o nunca.  

Los administradores toman la decisión general sobre si utilizar las capacidades de Copilot en [!INCLUDE [prod_short](includes/prod_short.md)]. Si los administradores habilitan Copilot, deben asegurarse de otorgar acceso a los usuarios adecuados.

> [!NOTE]
> - No admitimos esta función en [!INCLUDE [prod_short](includes/prod_short.md)] local o en una nube privada.
> - Los socios no pueden ampliar esta característica. Eso significa que los desarrolladores asociados no pueden modificarlo, reemplazarlo ni ampliarlo.

## ¿Es Copilot el único medio para crear líneas de ventas?  

No, el uso de Copilot es opcional. [!INCLUDE [prod_short](includes/prod_short.md)] ofrece formas sin tecnología de inteligencia artificial para insertar líneas de ventas o copiar documentos. Las organizaciones pueden utilizar ambos enfoques al mismo tiempo.  

## ¿Cómo doy comentarios sobre el contenido generado por IA?  

Cada vez que Copilot proporciona sugerencias, puede proporcionar comentarios a Microsoft directamente desde la ventana de Copilot, utilizando los controles Me gusta y No me gusta. Sus comentarios permanecen anónimos y utilizamos estos datos para mejorar la calidad del servicio.  

## Consulte también

[Sugerir líneas en pedidos de venta con Copilot](sales-suggest-sales-lines-with-copilot.md)  
[Configurar Copilot y capacidades de IA](enable-ai.md)  
[Preguntas frecuentes sobre IA responsable para Dynamics 365 Business Central](responsible-ai-overview.md)  
