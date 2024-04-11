---
title: Sugerir líneas de venta con Copilot
description: Aprenda a sugerir líneas en pedidos de venta con Copilot.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.topic: how-to
ms.search.keywords: 'Copilot, AI, sell'
ms.search.form: null
ms.date: 02/02/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
ms.collection: bap-ai-copilot
---

# <a name="suggest-lines-on-sales-documents-with-copilot-preview"></a>Sugerir líneas en documentos de venta con Copilot (versión preliminar)

[!INCLUDE[preview-banner](includes/preview-banner.md)]

Este artículo explica cómo crear documentos de ventas más rápido al permitir que Copilot sugiera los elementos para agregar a las líneas de los documentos de ventas para sus clientes.

[!INCLUDE[production-ready-preview-dynamics365](includes/production-ready-preview-dynamics365.md)]

## <a name="about-sales-line-suggestions-with-copilot"></a>Información sobre sugerencias de líneas de ventas con Copilot

La sugerencia de líneas de ventas con Copilot puede ayudar a crear líneas en documentos de ventas, como cotizaciones de ventas, pedidos y facturas, basadas en entradas estructuradas o lenguaje natural. La función no es un chat de propósito general, sino una experiencia altamente específica e integrada que puede utilizar en documentos de ventas. La función ofrece dos capacidades distintas que le ayudan a encontrar datos sobre productos individuales o documentos completos.

* Encontrar productos

  La información que describe los productos se almacena en varios lugares de [!INCLUDE [prod_short](includes/prod_short.md)]. Por ejemplo, los números de artículo y las descripciones se almacenan en la tabla **Artículo**, se almacenan varios códigos de barras en la tabla **Referencia del artículo** y las propiedades del producto se almacenan en la tabla **Atributos del artículo**. Si bien puede solicitar *bicicleta roja*, el producto real podría ser *turismo carmesí*, dónde *Bicicleta* es una categoría de producto y *rojo* es un atributo.

* Encontrar documentos por referencia

  La gente suele repetir un pedido anterior, o al menos utilizarlo como punto de partida. Pero puede resultar complicado encontrar el orden correcto en una pila de pedidos. Es posible que recuerde parte del ID del pedido, que puede ser un número asignado por la empresa o un número de referencia recibido de un cliente. Ser capaz de utilizar indicaciones como *Necesita la última factura de abril* debería ayudarle a encontrar un pedido más rápido.

## <a name="prerequisites"></a>Requisitos previos

* La sugerencia de línea de ventas con Copilot es habilitada y activada por un administrador. Para obtener más información sobre cómo habilitar las capacidades de IA, vaya a [Configurar Copilot y las capacidades de IA](enable-ai.md).
* Está familiarizado con la creación de pedidos de venta.

## <a name="geographic-availability"></a>Disponibilidad geográfica

La siguiente tabla muestra las áreas geográficas de Microsoft Azure en las que esta función está disponible.

|Región de Azure del entorno  |Geografía de Azure OpenAI Service   |Se requiere una acción del administrador para desbloquear Copilot  |
|---------|---------|---------|
|Alemania (Norte, Oeste central)     | Suecia o Suiza        |  Sí       |
|Noruega (Este, Oeste)     | Suecia o Suiza        | Sí     |
|Singapur     |         |         |
|Sudáfrica (Norte, Oeste)     |   Estados Unidos      |   Sí      |
|Suiza (Norte, Oeste)     |  Suecia o Suiza       |    Sí     |
|Emiratos Árabes Unidos (Norte, Oeste)     |    Estados Unidos     |   Sí     |
|Estados Unidos (centro, este, centro norte, centro sur, oeste)     |   Estados Unidos      |   N.º      |
|Europa (Oeste, Norte)     |   Suecia o Suiza      |   Sí      |
|Asia Pacífico     |         |         |
|Australia (Sureste)     |   Estados Unidos      |    Sí     |
|Sudamérica     |         |         |
|India (Centro, Sur)     |    Estados Unidos     |   Sí      |
|Japón (Este, Oeste)     |    Estados Unidos     |    Sí     |
|Francia (Centro, Sur)     |    Suecia o Suiza     |    Sí     |
|Corea (Centro, Sur)     |    Estados Unidos     |    Sí     |

## <a name="examples-of-prompts"></a>Ejemplos de indicaciones

Las líneas de ventas sugeridas con Copilot pueden manejar una amplia variedad de entradas rápidas. Esta sección ofrece algunos ejemplos de indicaciones para varios escenarios que hemos probado.

### <a name="sample-inquiry-to-repeat-the-past-document"></a>Ejemplo de consulta para repetir el documento anterior

Mensaje: *Necesita todos los productos de la factura 103031*

### <a name="during-phone-call-user-quickly-types-list-of-required-products-and-quantities-not-always-accurate-enough-or-using-internal-product-names"></a>Durante la llamada telefónica, el usuario escribe rápidamente una lista de productos y cantidades requeridas, no siempre lo suficientemente precisa o usando nombres de productos internos

Mensaje: *2 biciicletas rojas para niños*

Tenga en cuenta que el mensaje funciona, incluso con varios errores tipográficos.

### <a name="a-user-copies-an-inquiry-from-an-inbound-communication-and-pastes-it-to-the-sales-lines-suggestions-page"></a>Un usuario copia una consulta de una comunicación entrante y la pega en la página Sugerencias de líneas de ventas

Mensaje: *Hola, estoy interesado en comprar algunos accesorios para mi computadora portátil XXXX, como un ratón inalámbrico, una funda para teclado y una bolsa para ordenador portátil. Me pregunto si tiene alguna recomendación o sugerencia para estos artículos. ¿Tiene alguna oferta especial o descuento para clientes leales como yo? Saludos cordiales, M.*

Tenga en cuenta que XXXX Laptop no está incluido en la búsqueda.

## <a name="suggest-lines-on-a-sales-document"></a>Sugerir líneas en un documento de venta

Este proceso describe cómo sugerir líneas en un pedido de ventas. Los pasos son iguales a todos presupuestos y facturas de ventas.

1. Seleccione el icono ![Bombilla que abre la característica Dígame](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Pedido venta** y, a continuación, elija el vínculo relacionado.
1. Abra el pedido de venta.
1. En la ficha desplegable **Líneas**, elija **Obtener sugerencias de línea**.
1. En la ventana **Sugerir líneas con Copilot**, introduzca su mensaje o seleccione uno de las guías de mensajes.

## <a name="review-save-discard-or-regenerate-suggestions"></a>Revisar, guardar, descartar o regenerar sugerencias

Después de que Copilot sugiera los elementos para agregar a las líneas, revise sus sugerencias y decida si son lo que desea:

* Para descartar una única línea propuesta, selecciónela en la lista y luego elija la acción **Eliminar línea**.
* Para descartar todas las líneas propuestas y cerrar la ventana de Copilot, elija el botón Descartar (papelera) al lado del botón **Conservarlo**.
* Para transferir las líneas que se muestran en la ventana de Copilot, elija **Mantenerlo**. 

Hay un campo **Fiabilidad** que muestra puntuaciones **Alta (80+)**, **Media ( 60-80)** y **Baja (60-)** y le señalan líneas que necesitan atención.

Este paso confirma que desea transferir las líneas a un documento de ventas. También puede eliminar o editar las líneas transferidas allí o eliminar todo el documento.

## <a name="see-also"></a>Consulte también

[Preguntas frecuentas de sugerencias de líneas de ventas con Copilot](faq-sales-suggest-sales-lines-with-copilot.md)
[Configurar Copilot y las capacidades de IA](enable-ai.md)
