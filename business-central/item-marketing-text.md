---
title: Agregar texto de marketing para productos
description: Escribir texto de marketing para productos en Business Central
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.topic: how-to
ms.date: 03/22/2023
ms.custom: bap-template
---

# Agregar texto de marketing para productos

Para cualquier producto registrado en Business Central, puede escribir *texto de marketing* sobre el producto. Aunque el texto de marketing es una especie de descripción, es diferente del campo **Descripción** del producto. El campo **Descripción** se utiliza normalmente como un nombre visible conciso para identificar rápidamente el producto. El texto de marketing, por otro lado, es un texto más rico y descriptivo. Su propósito es agregar contenido promocional y de marketing, también conocido como *copia*. Este texto se puede publicar con el producto si se publica en una tienda web, como Shopify.

Hay dos formas de crear el texto de marketing. La forma más fácil de comenzar es usar Copilot, que sugiere texto generado por IA. La otra forma es empezar de cero. 

## <a name=copilot></a>Crear texto de marketing generado por IA (vista previa) con Copilot

[!INCLUDE[ai-preview](includes/ai-preview.md)]

Con Copilot, obtiene rápidamente una sugerencia de texto que se genera automáticamente para usted. El texto generado por IA se adapta al elemento y proporciona un buen punto de partida. El texto se basa en parte en la siguiente información:

- Atributos definidos para el producto, por ejemplo, como la descripción, el color, las dimensiones, el material, etc.
- Preferencias de estilo seleccionables como tono de voz, formato y duración.

Copilot está diseñado para ahorrarle tiempo y ayudarlo a escribir texto creativo y atractivo que refleje su marca y sea consistente en toda su línea de productos. Comience generando una sugerencia, luego cambie el texto sugerido según sea necesario.

### Requisitos previos

- Está utilizando una [versión preliminar](ai-preview-getstarted.md) de Business Central que está habilitada para Copilot. La activación de Copilot la realiza un administrador. Para obtener más información, vaya a [Configurar texto de marketing de artículos impulsado por IA con Copilot](enable-ai.md).

- Consulte las [preguntas frecuentes de Copilot](ai-faq.md) para obtener más información sobre las sugerencias de texto generadas por IA de Copilot y cómo debe usarlas.

### Crear un primer borrador con Copilot

1. En Business Central, abra el producto que desea modificar. Para abrir un elemento, siga los pasos siguientes:

   1. En la esquina superior derecha, seleccione la ![bombilla que abre la característica Tell Me 22.](media/ui-search/search_small.png "Dígame qué desea hacer") icono, escriba **Productos**, y, a continuación, elija el enlace relacionado para mostrar una lista de productos disponibles.
   2. Para abrir el elemento, haga doble clic en él o seleccione su valor en la columna **N.º** .

   Para obtener información sobre cómo crear un elemento, vaya a [Registrar nuevos productos](inventory-how-register-new-items.md).

   [![Muestra una tarjeta de producto con panel de texto de marketing](media/create-with-copilot.png)](media/create-with-copilot.png#lightbox)

2. Desde la ficha del producto, hay dos formas de empezar a escribir texto de marketing con Copilot:

   - Una forma es usar el panel **Texto de marketing** en el Cuadro informativo en el lado derecho de la página. Siga estos pasos:

      1. En el panel **Texto de marketing** , seleccione **Crear con Copilot**.

         El texto sugerido aparece en el panel.
      2. Si desea otra sugerencia, seleccione **Crear con Copilot** nuevamente. Si no le gusta una sugerencia, seleccione **Descartar** para borrar el panel.

         Puede realizar este paso una y otra vez hasta que obtenga una sugerencia que crea que es un buen punto de partida. Pero tenga en cuenta que la sugerencia actual se sobrescribirá y no necesariamente podrá recuperarla. Entonces, si le gusta la sugerencia actual, vaya al siguiente paso. Todavía tendrá la oportunidad de obtener más sugerencias e incluso mejorar las sugerencias, si lo desea más adelante.
      3. Seleccione **Revisar y guardar la sugerencia** o **Editar** para revisar, editar y guardar el texto.

         Este paso lo lleva a la página **Crear con Copilot**. Pase a la siguiente sección.

         > [!NOTE]
         > El texto no se guardará hasta que realice este paso.

   - Otra forma es seleccionar la acción **Texto de marketing** en la parte superior de la página de la ficha del producto para ir directamente a la página **Crear con Copilot**.

     En la página **Crear con Copilot**, seleccione **Crear con Copilot** para obtener la primera sugerencia. Luego puede obtener más sugerencias, intentar mejorar las sugerencias que recibe, editar texto y más. Vaya a [Revisar, editar y guardar](#review-edit-and-save-text) para obtener más información.

   > [!TIP]
   > [¿De dónde viene la sugerencia?](ai-faq.md#how-does-copilot-work-where-does-the-suggested-text-come-from)

### Revisar, editar y guardar texto

Una vez que tenga el primer borrador, debe revisarlo y hacer cambios en el texto para dejarlo listo para su publicación. Este trabajo se realiza desde la página **Crear con Copilot**. El texto actual se muestra en el cuadro **Texto de marketing**. La página le permite obtener más sugerencias, cambiar las preferencias para influir en las sugerencias y realizar cambios y diseñar manualmente el texto.

[![Muestra la creación con ventanas Copilot](media/create-with-copilot-window.png)](media/create-with-copilot-window.png#lightbox)

> [!IMPORTANT]
> El texto generado por IA de Copilot es solo una sugerencia y puede tener errores. Requiere supervisión y revisión humana para garantizar que sea preciso y apropiado. Revise cualquier texto sugerido y edítelo según sea necesario antes de guardarlo y publicarlo para consumo público.

Use las siguientes pautas para finalizar y guardar el texto de marketing.

1. Realice cambios en el texto directamente en el cuadro **Texto de marketing**. Use la barra de herramientas en la parte inferior del cuadro para dar formato y estilo al texto, agregar enlaces y más.
2. Para obtener una nueva sugerencia, seleccione **Crear borrador**.
3. Si no está satisfecho con las sugerencias, mejore las sugerencias de texto según sus preferencias.

   Seleccione **Más configuraciones**, cambie las opciones que se muestran debajo de **Elegir cómo Copilot crea sugerencias** y luego seleccione **Crear un borrador** para obtener una nueva sugerencia.

   Para obtener pautas sobre cómo mejorar las sugerencias, vaya a [Mejore y adapte las sugerencias de texto](#improve-and-tailor-text-suggestions).

4. Si desea volver a la sugerencia anterior, seleccione **Deshacer**.
5. Revise detenidamente el texto para verificar su precisión y adecuación, luego seleccione **OK** para guardarlo.

### Mejorar y adaptar las sugerencias de texto

Hay algunos pasos que puede seguir para mejorar las sugerencias de texto y modificarlas para adaptarlas a sus preferencias personales o de empresa.

1. Utilice las opciones en la parte superior de la página **Crear con Copilot** para influir en el resultado del texto generado por IA: 

   |Opción|Descripción|
   |-|-|
   |Atributos que se incluirán|Utilice esta opción para basar las sugerencias, en parte, en los atributos asignados al producto. Elija los atributos que mejor se alineen con las características que desea promocionar. Cuantos más atributos relevantes incluya, más rico será el resultado. Si cree que le faltan algunos atributos clave, agregue más. Para más información sobre los atributos, vaya a [Trabajar con atributos de productos](inventory-how-work-item-attributes.md) |
   |Enfatizar una calidad|Use esta opción para elegir de una lista de cualidades predefinidas que desea enfatizar en el texto. Elija una calidad que mejor se alinee con el tipo de producto sobre el que está escribiendo. Las cualidades no se corresponden directamente con los atributos, la descripción o la categoría del producto. Por ejemplo, **Calidad** podría ser una buena opción tanto para una bicicleta como para un escritorio, mientras que **Velocidad** sería adecuado para una bicicleta., pero no un escritorio.|
   |Tono de voz|Utilice esta opción para influir en qué tipo de palabras, frases y puntuación se utilizan para atraer al público objetivo. Puede elegir entre varios tonos de voz predefinidos, que van desde **Formal** (lo que da como resultado un tono más comercial de las opciones) hasta **Creativo** (lo que resulta en un tono más informal de las elecciones). |
   |Formato y longitud|Utilice esta opción para controlar la estructura general del texto, que consta de tres partes, cubiertas por cuatro opciones diferentes: <ul><li>**Eslogan**: frase pegadiza u oración breve que identifica el producto o la marca.</li><li>**Párrafo**: un solo párrafo de texto fluido y detallado, que consta de varias oraciones completas.</li><li>**Eslogan + Párrafo**: un eslogan seguido de un párrafo</li><li>**Breve**: una oración introductoria, similar a un eslogan, seguida de una lista con viñetas de puntos clave de interés.</li></ul> |

2. Mejore el campo **Descripción** en la ficha del producto.

   El texto en el campo **Descripción** se utilizará tal cual en muchos lugares del texto sugerido, por lo que es importante que la descripción refleje mejor cómo desea que se haga referencia al producto en el texto de marketing. 

3. Asegúrese de que el campo **Código de categoría de producto** en la ficha del producto se establece en una categoría adecuada.

   Copilot encontrará palabras y frases relacionadas con la categoría y las trabajará en el texto sugerido.

## Crear texto de marketing desde cero

1. En Business Central, abra el producto que desea modificar como sigue:

    1. En la esquina superior derecha, seleccione la ![bombilla que abre la característica Tell Me 22.](media/ui-search/search_small.png "Dígame qué desea hacer") icono, escriba **Productos**, y, a continuación, elija el enlace relacionado para mostrar una lista de productos disponibles.
    2. Para abrir el elemento, haga doble clic en él o seleccione su número en la columna **N.º** .

2. Realice uno de los siguientes pasos:

   - En el plane **Texto de marketing** del cuadro informativo en la parte derecha de la página, seleccione **Editar**.
   - Seleccione la acción **Marketing Text**.
3. Realice cambios en el texto directamente en el cuadro **Texto de marketing**. Use la barra de herramientas en la parte inferior del cuadro para dar formato y estilo al texto, agregar enlaces y más.
4. Seleccione **DE ACUERDO** cuando haya terminado para guardar el texto.

## Consulte también .

[Información general sobre el texto de marketing de productos impulsado por IA con Copilot](ai-overview.md)  
[Configurar texto de marketing de productos impulsado por IA con Copilot](enable-ai.md)  
[Preguntas frecuentes del texto de marketing de productos impulsado por IA con Copilot](ai-faq.md)  
[Registro de productos nuevos](inventory-how-register-new-items.md)  