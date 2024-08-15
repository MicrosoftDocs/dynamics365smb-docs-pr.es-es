---
title: Agregar texto de marketing para productos
description: Escriba textos de marketing para artículos en Business Central.
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.topic: how-to
ms.date: 06/10/2024
ms.custom: bap-template
ms.collection:
  - bap-ai-copilot
---

# <a name="add-marketing-text-to-items"></a>Agregar texto de marketing para productos

Para cualquier producto registrado en Business Central, puede escribir *texto de marketing* sobre el producto. Aunque el texto de marketing es una especie de descripción, es diferente que el campo **Descripción** del producto. El campo **Descripción** se utiliza normalmente como un nombre visible conciso para identificar rápidamente el producto. El texto de marketing, por otro lado, es un texto más rico y descriptivo. Su propósito es agregar contenido promocional y de marketing, también conocido como *copia*. Este texto puede publicarse después con el producto si se publica en una tienda web, como Shopify, o pegarse en correos electrónicos u otras comunicaciones con sus clientes.

Hay dos formas de crear el texto de marketing. La forma más fácil de comenzar es usar Copilot, que sugiere texto generado por IA. La otra forma es empezar de cero. 

## <a name="get-marketing-text-suggestions-with-copilot"></a><a name=copilot></a>Obtener sugerencias de texto de marketing con Copilot

Con Copilot, obtiene rápidamente una sugerencia de texto que se genera automáticamente para usted. El texto generado por IA se adapta al elemento y proporciona un buen punto de partida. El texto se basa en parte en la siguiente información:

- Atributos definidos para el producto&mdash;por ejemplo, como la descripción, el color, las dimensiones, el material, etc. [Más información sobre los atributos de los productos](inventory-how-work-item-attributes.md).
- El campo **Descripción** del producto.
- La categoría del producto. [Más información sobre la categorización de productos](inventory-how-categorize-items.md).
- Preferencias de estilo seleccionables como tono de voz, formato y duración.

Copilot está diseñado para ahorrarle tiempo y ayudarlo a escribir texto creativo y atractivo que refleje su marca y sea consistente en toda su línea de productos. Comience generando una sugerencia, luego cambie el texto sugerido según sea necesario.

### <a name="available-languages"></a>Idiomas disponibles

[!INCLUDE[copilot-supported-languages.md](includes/copilot-supported-languages.md)]

### <a name="prerequisites"></a>Requisitos previos

La función de sugerencias de textos de marketing está activada en su entorno. Esta tarea suele realizarla un administrador. Para obtener más información, vaya a [Configurar Copilot y capacidades de IA](enable-ai.md).

### <a name="create-first-draft-with-copilot"></a>Crear un primer borrador con Copilot

Complete los siguientes pasos para agregar texto de marketing a un artículo existente. Para aprender cómo crear un nuevo elemento, vaya a [Registrar nuevos elementos](inventory-how-register-new-items.md).

1. En Business Central, abra el artículo que desea modificar completando los siguientes pasos:

   - En la esquina superior derecha, seleccione la ![bombilla que abre la característica Tell Me 22.](media/ui-search/search_small.png "Dígame qué desea hacer") icono, escriba **Productos**, y, a continuación, elija el enlace relacionado para mostrar una lista de productos disponibles.

   - Haga doble clic en el elemento o seleccione su valor en **N.º** .

1. Desde la tarjeta de artículo, hay dos formas de comenzar a escribir texto de marketing con Copilot: desde el cuadro informativo **Texto de marketing** o utilizando la acción **Texto de marketing**. Estos métodos se indican en la siguiente figura de una ficha de artículo.  

   [![Muestra una tarjeta de producto con panel de texto de marketing](media/create-with-copilot.svg)](media/create-with-copilot.svg#lightbox)

   Para crear el primer borrador de un elemento, realice uno de los siguientes pasos:

   - En el panel **Texto de marketing** del cuadro informativo en la parte derecha de la página, seleccione **Borrador con Copilot**. 

     Copilot comienza a redactar el texto de marketing.

   - En la parte superior de la página, seleccione la acción **Texto de marketing**, luego seleccione **Borrador con Copilot** en la **Ventana Editar texto de marketing**.  La ventana **Borrador de texto de marketing con Copilot** aparece y enumera todos los atributos disponibles para el elemento.
1. Seleccione los atributos en los que desea que Copilot base las sugerencias y luego seleccione **Generar**. Puede cambiar los atributos seleccionados y otras opciones más adelante. Copilot comienza a redactar el texto de marketing. 

   ![Muestra la ventana de edición de texto de marketing](media/marketing-text-copilot-attributes.svg)

1. Cuando Copilot completa el borrador, el texto aparece en la ventana del editor de Copilot para que lo revise y lo edite.

   [![Muestra la creación con ventanas Copilot](media/create-with-copilot-window.svg)](media/create-with-copilot-window.svg#lightbox)

   Ahora puede obtener más sugerencias, intentar mejorar las sugerencias que recibe, editar texto y más. Vaya a [Revisar, editar y guardar](#review-edit-and-save-text) para obtener más información.

### <a name="review-edit-and-save-text"></a>Revisar, editar y guardar texto

Una vez que tenga el primer borrador, debe revisarlo y hacer cambios en el texto para dejarlo listo para su publicación. Este trabajo se hace desde el editor de Copilot, que le permite obtener más sugerencias, cambiar las preferencias para influir en las sugerencias y realizar cambios y diseñar manualmente el texto.

> [!IMPORTANT]
> El texto generado por IA de Copilot es solo una sugerencia y puede tener errores. Requiere supervisión y revisión humana para garantizar que sea preciso y apropiado. Revise cualquier texto sugerido y edítelo según sea necesario antes de guardarlo y publicarlo para consumo público.

Use las siguientes pautas para finalizar y guardar el texto de marketing.

1. Realice cambios en el texto directamente en el cuadro de texto. Use la barra de herramientas en la parte inferior del cuadro para dar formato y estilo al texto, agregar enlaces y más.
2. Para obtener una nueva sugerencia, seleccione **Regenerar**.
3. Si no está satisfecho con las sugerencias, mejore las sugerencias de texto utilizando las opciones de preferencia de **Tono**, **Formato** y **Énfasis**.

   <!--Select **More Settings**, change the options that are shown under **Choose how Copilot creates suggestions**, then select **Create draft** to get a new suggestion.-->

   Para obtener pautas sobre cómo mejorar las sugerencias, vaya a [Mejore y adapte las sugerencias de texto](#improve-and-tailor-text-suggestions).

4. Para ir y venir a través de sugerencias, utilice los enlaces anterior y siguiente en la parte superior de la página (*x* **de** *y*). <!-- or select the **...** (More formatting options) along the bottom of the window, then select **Undo**. Select **Redo** to go back.-->
5. Revise detenidamente el texto para verificar su precisión y adecuación:

   - Si desea guardar el texto, seleccione **Mantenerlo**. 
   - Si no desea guardar, seleccione el botón de descartar (papelera) ![Muestra el ícono de la papelera para eliminar todas las propuestas de Copilot para la conciliación de cuentas bancarias](media/copilot-delete-trash-can.png).

### <a name="improve-and-tailor-text-suggestions"></a>Mejorar y adaptar las sugerencias de texto

Hay algunos pasos que puede seguir para mejorar las sugerencias de texto y modificarlas para adaptarlas a sus preferencias personales o de empresa.

1. Cambie los atributos del elemento utilizados por Copilot.

   Las sugerencias de Copilot se basan, en parte, en los atributos asignados al producto. Para ver los atributos disponibles y la configuración actual, seleccione el icono de edición ![Muestra el icono de edición en la ventana de Copilot para cambiar los atributos](media/edit-pencil.png) en la esquina superior izquierda. En la página **Atributos de producto**, elija los atributos que mejor se alineen con las características que desea promocionar. Cuantos más atributos relevantes incluya, más rico es el resultado. Si cree que le faltan algunos atributos clave, agregue más. Para más información sobre los atributos, vaya a [Trabajar con atributos de productos](inventory-how-work-item-attributes.md)
1. Cambie su configuración de preferencias para las opciones **Tono**, **Formato** y **Énfasis**.

   |Opción|Descripción|
   |-|-|
   |Tono |Utilice esta opción para influir en qué tipo de palabras, frases y puntuación se utilizan para atraer al público objetivo. Puede elegir entre varios tonos de voz predefinidos, que van desde **Formal** (lo que da como resultado un tono comercial) hasta **Creativo** (lo que resulta en un tono más informal). |
   |Formato y longitud|Utilice esta opción para controlar la estructura general del texto, que consta de tres partes, cubiertas por cuatro opciones diferentes: <ul><li>**Eslogan**: frase pegadiza u oración breve que identifica el producto o la marca.</li><li>**Párrafo**: un solo párrafo de texto fluido y detallado, que consta de varias oraciones completas.</li><li>**Eslogan + Párrafo**: un eslogan seguido de un párrafo</li><li>**Breve**: una oración introductoria, similar a un eslogan, seguida de una lista con viñetas de puntos clave de interés.</li></ul> |
   |Énfasis|Use esta opción para elegir de una lista de cualidades predefinidas que desea enfatizar en el texto. Elija una calidad que mejor se alinee con el tipo de producto sobre el que está escribiendo. Las cualidades no se corresponden directamente con los atributos, la descripción o la categoría del producto. Por ejemplo, **Calidad** podría ser una buena opción tanto para una bicicleta como para un escritorio, mientras que **Velocidad** sería adecuado para una bicicleta., pero no un escritorio.|

1. Mejore el campo **Descripción** en la ficha del producto.

   El texto en el campo **Descripción** se utiliza tal cual en muchos lugares del texto sugerido, por lo que es importante que la descripción refleje mejor cómo desea que se haga referencia al producto en el texto de marketing. 

1. Asegúrese de que el campo **Código de categoría de producto** en la ficha del producto se establece en una categoría adecuada.

   Copilot encuentra palabras y frases relacionadas con la categoría y las trabajará en el texto sugerido.

### <a name="working-with-multiple-languages"></a>Trabajar con varios idiomas

El texto se genera siempre en el idioma definido por su [configuración](ui-change-basic-settings.md#language) de usuario. Si su organización opera e introduce datos en Business Central en otro idioma, o si Business Central está conectado a su tienda en línea, por ejemplo con Shopify, esto podría dar lugar a la publicación de contenidos que no coincidan con contenidos de marketing similares.

## <a name="create-text-from-scratch"></a>Crear texto desde cero

1. En Business Central, abra el producto que desea modificar como sigue:

    1. En la esquina superior derecha, seleccione la ![bombilla que abre la característica Tell Me 22.](media/ui-search/search_small.png "Dígame qué desea hacer") icono, escriba **Productos**, y, a continuación, elija el enlace relacionado para mostrar una lista de productos disponibles.
    2. Para abrir el elemento, haga doble clic en él o seleccione su número en la columna **N.º** .

2. Realice uno de los siguientes pasos:

   - En el panel **Texto de marketing** del cuadro informativo en la parte derecha de la página, seleccione **Editar**.
   - Seleccione la acción **Marketing Text**.
3. Realice cambios en el texto directamente en el cuadro **Texto de marketing**. Use la barra de herramientas en la parte inferior del cuadro para dar formato y estilo al texto, agregar enlaces y más.
4. Seleccione **DE ACUERDO** cuando haya terminado para guardar el texto.

## <a name="see-also"></a>Consulte también

[Resumen de sugerencias de texto de marketing](ai-overview.md)  
[Solucionar problemas de Copilot y capacidades de IA](ai-copilot-troubleshooting.md)  
[Preguntas frecuentes para sugerencias de texto de marketing](faqs-marketing-text.md)  
[Configurar Copilot y capacidades de IA](enable-ai.md)  
[Registro de productos nuevos](inventory-how-register-new-items.md)  
