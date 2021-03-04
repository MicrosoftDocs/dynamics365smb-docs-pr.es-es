---
title: Personalización de páginas | Documentos de Microsoft
description: Aprenda a personalizar la interfaz de usuario para que se adapte a su forma de trabajar en Business Central.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customize, personalize, personalization, hide columns, remove fields, move fields, resize column, change column width
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 4b112bf05c1bbc6110ce3b5a439c81a96759d1bf
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "4756772"
---
# <a name="personalize-your-workspace"></a>Personalice su área de trabajo
Puede personalizar su área de trabajo para que se adapte a su trabajo y preferencias cambiando las páginas de modo que muestren únicamente la información que necesite y donde la necesite. Los cambios de personalización que realice solo afectarán a su visualización y no a la de otros usuarios.

Puede personalizar todo tipo de páginas, incluida la página Área de trabajo. Para obtener más información sobre las áreas de trabajo, consulte [Área de trabajo](ui-change-basic-settings.md#role-center).

Dependiendo del tipo de página y qué incluye, puede realizar varios cambios, como mover u ocultar campos, columnas, acciones y partes completas, y agregar nuevos campos. La mayor parte de la personalización debe hacerse activando primero el banner **Personalizando**, pero se pueden realizar ajustes muy simples, como el ancho de columna, inmediatamente en cualquier lista.

> [!NOTE]
> Los administradores pueden realizar los mismos cambios de diseño que los usuarios al personalizar el espacio de trabajo para un perfil que se asigna a múltiples usuarios. Para obtener más información, consulte [Personalizar las páginas para los roles](ui-personalization-manage.md).<br /><br />
Los administradores también pueden anular o deshabilitar la personalización de los usuarios y pueden definir qué características están incluso disponibles para que los usuarios las vean en todas las empresas o en empresas específicas. Para obtener más información, consulte [Personalizar Business Central](ui-customizing-overview.md).

## <a name="video-overview"></a>Resumen en vídeo
El siguiente video muestra algunas de las formas en que puede personalizar su área de trabajo.

> [!Video https://www.microsoft.com/en-us/videoplayer/embed/RE4ArUB?rel=0]

## <a name="to-change-the-width-of-a-column"></a>Para cambiar el ancho de una columna
Puede cambiar fácilmente el tamaño de las columnas en cualquier lista arrastrando el límite entre dos columnas hacia la izquierda o hacia la derecha.
1. En la cabecera de una lista, seleccione y arrastre el límite entre dos columnas.
2. También puede hacer doble clic en el límite entre dos columnas para ajustar automáticamente el ancho de la columna. Esto establece el ancho al tamaño óptimo para facilitar la lectura.

En cuanto a otra personalización, los cambios que efectúe en el ancho de columna se almacenan en su cuenta y le siguen sin importar en qué dispositivo inicie sesión.

## <a name="to-start-personalizing-a-page-through-the-personalizing-banner"></a>Para empezar a personalizar una página a través del banner **Personalización**
1. Abra cualquier página que quiera personalizar.
2. En la esquina superior derecha, seleccione el icono ![Configuración](media/ui-experience/settings_icon_small.png "Icono de configuración para el área de trabajo") y, a continuación, elija la acción **Personalizar**.

    El banner **Personalización** aparece en la parte superior para indicar que puede empezar a realizar cambios.

    > [!NOTE]
    > Para navegar durante la personalización, use Ctrl + clic en una acción si está resaltada por la punta de flecha.

    Si se muestra ![Bloqueo de personalización](media/personalization-lock-icon.png "Bloqueo de personalizacion") o ![Personalización bloqueada](media/personalization-blocked-icon.png "Personalización bloqueada") en el banner, no puede personalizar la página. Para obtener más detalles, consulte [Por qué la página está bloqueada para la personalización](ui-personalization-locked.md).

3. Para agregar un campo, elija la acción **+ Campo**.
4. Desde el panel **Agregar campo a página**, arrastre y suelte un campo en la posición deseada en la página.
5. Para cambiar un elemento de la interfaz de usuario, señale el elemento, como una acción, un campo o una parte. El elemento se resalta inmediatamente con una punta de flecha o borde.
6. Elija el elemento y, a continuación, seleccione **Mover**, **Eliminar**, **Ocultar**, **Mostrar**, **Mostrar en "Mostrar más"**, **Mostrar cuando se contrae**, **Mostrar siempre**, **Establecer/Borrar inmovilización de panel** o **Incluir/Excluir de entrada rápida**, según el tipo y el estado del elemento de la interfaz de usuario. Para obtener más información, consulte [Qué puede personalizar](#What).
7. Cuando haya terminado de cambiar el diseño de una o más páginas, elija el botón **Listo** en el banner **Personalización**.

## <a name="what-you-can-personalize"></a><a name="What"></a>Qué puede personalizar

|Qué desea hacer|Cómo hacerlo|Comentarios|
|----|------------|-------|
|Mover algo, un campo, una columna de la lista, un icono, una acción o una pieza|Señale en cualquier lugar qué desea mover y arrástrelo a su nueva posición. La posición se indica con una fina línea vertical u horizontal.<br /><br />![Icono No se puede mover aquí](media/personalization-cannot-move-here.png "Modo de personalización: icono No se puede mover aquí") indica que no puede mover el elemento a la posición seleccionada.|Las piezas son subdivisiones o áreas en una página que contienen elementos como múltiples campos, otra página, un gráfico o iconos.<br /><br />Para obtener más información sobre la personalización de acciones, consulte [Personalización de acciones](ui-personalization-user.md#Actions). |
|Ocultar algo, un campo, una columna de la lista, un icono, una acción o una pieza.|Elija la punta de flecha y elija <b>Ocultar</b>.|El elemento aparece en gris cuando está en modo de personalización. Si el campo que oculta también se muestra en el encabezado de la ficha desplegable cuando está contraída, el campo ya no aparecerá allí.|
|Mostrar acciones y partes ocultas.|Para un elemento atenuado (oculto), elija la punta de flecha y luego elija <b>Mostrar</b>.|El elemento oculto vuelve a estar visible.|
|Agregar un campo o columna.|En el banner <b>Personalización</b>, elija la acción <b>+ Campo</b>.<br /></br>El panel <b>Agregar campo a página</b> se abre a la derecha. Muestra los campos que se pueden agregar a la página.<br /><br />Para agregar un campo, arrástrelo de panel a la posición que desee. La posición se indica con una fina línea vertical u horizontal.|Cada página incluye un conjunto predefinido de campos que puede mostrar. Siga este procedimiento para agregar campos o columnas que no se han mostrado anteriormente o para mostrar los campos que ha ocultado.|
|Mostrar un campo de la cabecera de una ficha desplegable cuando está contraída.|Elija la punta de flecha y, a continuación, seleccione <b>Mostrar cuando se contrae</b>. <br /> <br />Si no hace ve esta opción, significa que ya está establecida. En este caso, para dejar de mostrar el campo del encabezado de la ficha desplegable, elija <b>Mostrar siempre</b>.|*Ficha desplegable* es el término que se utiliza para un grupo de campos que aparecerán bajo un encabezado común. Utilice la opción <b>Mostrar cuando se contrae</b> para mostrar los campos más importantes. Si selecciona un campo del encabezado, se abrirá la ficha desplegable y con el enfoque en el campo seleccionado.<br /><br />Esta opción solo es aplicable si una página tiene una más de una ficha desplegable. Si hay solo una ficha desplegable, no se puede contraer, por lo que la opción <b>Mostrar cuando se contrae</b> no está disponible.|
|Hacer que un campo se muestre solo cuando seleccione **Mostrar más**.|Elija la punta de flecha y, a continuación, seleccione <b>Mostrar en "Mostrar más"</b>. <br /> <br />Si no ve la opción <b>Mostrar en "Mostrar más"</b>, significa que ya está establecida. En este caso, para que un campo se muestre siempre, no solo al seleccionar **Mostrar más**, elija <b>Mostrar siempre</b>.||
|Cambiar la inmovilización de panel de una lista a otra columna. |Elija la punta de la flecha de la columna que desee establecer como la última de la inmovilización de panel y, a continuación, elija <b>Establecer inmovilización de panel</b>.<br /><br/>Si desea volver a configurar la inmovilización de panel en su posición original diseñada, elija la punta de flecha para la columna actual y elija <b>Borrar inmovilización de panel</b>. Nota: No puede eliminar la inmovilización de panel.|La inmovilización de panel especifica las columnas que siempre aparecen a la izquierda, incluso durante el desplazamiento horizontal.|  
|Saltar un campo al presionar Entrar.|Elija la punta de flecha junto al campo, o la cabecera de columna en una lista y seleccione **Excluir de entrada rápida**. <br /><br /> Si no ve esta opción, significa que el campo ya está establecido para saltarlo. En este caso, para dejar de omitir el campo, elija **Incluir en entrada rápida**. |Consulte [Acelerar la entrada de datos con la entrada rápida](ui-enter-data.md#QuickEntry)|
|Reordenar y eliminar vistas que representan listas filtradas.|Elija la punta de flecha situada junto a una vista y luego elija **Mover**, **Eliminar** u **Ocultar**.|Consulte [Guardar y personalizar vistas de lista](ui-views.md)|  
|Agregue una nueva acción a una página o informe en su Área de trabajo.|Desde la página de destino, la página de solicitud de informe o la ventana Avisarme, elija el icono de marcador.|Consulte [Marcar una página o informe en su Área de trabajo](ui-bookmarks.md)|
|Siempre empiece una lista como expandida o contraída|Elija el botón Expandir todo o Contraer todo en la esquina superior izquierda de la lista, o elija la acción Expandir todo o Contraer todo en el menú de la primera columna. |Se aplica a las listas jerárquicas contraíbles.|

## <a name="personalizing-actions"></a><a name="Actions"></a>Personalización de acciones

La personalización le permite decidir qué acciones se mostrarán en las barras de navegación y acciones y en las áreas de trabajo y dónde se mostrarán. Puede mostrar, ocultar o mover acciones individuales o grupos de acciones. La personalización de las barras de navegación y acciones se hace básicamente de la misma forma que con otros elementos de la interfaz de usuario. Sin embargo, lo que puede realizar con una acción o un grupo depende de dónde se encuentre la acción o el grupo. La mejor forma de averiguarlo es cambiar al modo de personalización y dejar que le guíen las puntas de flecha.

Hay un par de términos con los que debería estar familiarizado para entender mejor la personalización de las acciones: *grupo de acciones* y *categoría promocionada*.  

Un *grupo de acciones* es un elemento que se expande para mostrar otras acciones o grupos. Por ejemplo, en la página **Pedidos de venta**, la acción **Funciones** que aparece cuando elige la acción **Acciones** es un grupo de acciones.

Una *categoría promocionada* es un grupo de acciones que antes de la línea vertical `|` en la barra de acciones. Las categorías suelen incluir las acciones más utilizadas, para que pueda encontrarlas rápidamente. Por ejemplo, en la página **Pedidos de venta**, las acciones **Pedido**, **Lanzamiento** y **Registro** son categorías promocionadas.

> [!NOTE]
> No puede personalizar la barra de acción que aparece en partes de la página (por ejemplo, las líneas de ventas parte en la página **Pedidos de venta**).

### <a name="to-remove-hide-and-show-actions-and-action-groups"></a>Para eliminar, ocultar y mostrar acciones y grupos de acciones
Cuando desee mostrar u ocultar una acción, las opciones situadas debajo de la punta de flecha definen lo que puede hacer dependiendo del estado de la acción.
1. Elija la punta de flecha de una acción o grupo de acciones.
2. Elija de una de las siguientes opciones:

|Opción|Lo que hace|
|------|------------
|**Eliminar**|Esta opción aparece si la acción seleccionada también se muestra en otro lugar de la barra de navegación o barra de acciones. Al seleccionar esta opción se elimina la acción de la ubicación seleccionada para que ya no aparezca. La acción o grupo de acciones permanecerá en otros lugares. |
|**Ocultar**|Esta opción aparece si la acción o el grupo de acciones no se encuentra en otro lugar de la barra de navegación o barra de acciones. Como **Eliminar**, al elegir esta opción se provocará que la acción o el grupo de acciones desaparezca de la barra de navegación o barra de acciones. No obstante, en el modo de personalización, aún se mostrará la acción o el grupo de acciones en la posición actual, excepto que aparece atenuada.|
|**Mostrar**|Esta opción aparece si la acción o grupo de acciones ha sido previamente ocultada (atenuada). Al elegir esta opción se provocará que la acción o el grupo de acciones aparezca en la barra de navegación o barra de acciones.|

### <a name="to-move-actions-and-action-groups"></a>Para mover acciones y grupos de acciones
El lugar donde se pueden soltar acciones o grupos de acciones se indica mediante una línea horizontal entre dos acciones o un borde alrededor de un grupo de acciones. Existen las siguientes limitaciones:

- Puede mover acciones individuales a las categorías promocionadas, pero no puede reorganizar el orden de las acciones en la categoría.
- No puede mover un grupo de acciones a una categoría promocionada.

1. Para mover una acción o grupo de acciones, arrástrelo y suéltelo en la posición deseada, igual que hace con los campos y columnas.
2. Para mover una acción o un grupo de acciones a otro grupo de acciones que está vacío, arrastre la acción o el grupo de acciones al nuevo grupo y colóquelo en el cuadro **Colocar aquí una acción** .


## <a name="personalizing-parts"></a><a name="Parts"></a>Personalizar partes

Las partes son áreas de una página que generalmente se componen de múltiples campos, gráficos u otro contenido, y se pueden identificar mediante un borde de color al establecer el foco en la parte. Por ejemplo, una pantalla de inicio del Área de trabajo tiene varias partes. Debido a su límite bien definido, puede personalizar toda la parte, así como su contenido.

- Para mover una parte, arrástrela y suéltela en la posición deseada. Una línea de color indica las posiciones válidas en la pantalla. Por ejemplo, los cuadros informativos solo se pueden mover junto a otros cuadros informativos en el panel Cuadro informativo.
- Puede ocultar una parte eligiendo la opción **Ocultar** bajo la punta de flecha.
- Cuando comience a personalizar o navegue a una nueva página, cualquier parte que esté actualmente oculta aparecerá en la página con imágenes distintivas para indicar que están ocultas. Puede mostrar la parte eligiendo la opción **Mostrar** bajo la punta de flecha.

Puede borrar todos los cambios de personalización que haya realizado en una sola parte seleccionando la opción **Borrar personalización** bajo la punta de flecha de la parte. Borrar la personalización de una parte solo afecta a los cambios en el contenido de la parte, no a la ubicación ni a la visibilidad de la parte en la página.  


## <a name="to-clear-personalization"></a>Para borrar la personalización
En algún momento, es posible que desee borrar algunos o todos los cambios de personalización que hizo en esta página a lo largo del tiempo.

1. En el banner **Personalización**, elija la acción **Borrar personalización**.
2. Elija una de las siguientes opciones. Tenga en cuenta que el borrado de la personalización no se puede deshacer.

|Opción|Lo que hace|
|------|------------
|**Solo menú de navegación**|Borra cualquier cambio de personalización que haya realizado en el menú de navegación que se comparte en el Área de trabajo y otras páginas. Esto incluye cualquier acción nueva que se haya agregado como marcador y cualquier cambio en los enlaces y grupos en el menú.|  
|**Solo acciones**|Borra todos los cambios de personalización que haya realizado en las barras de navegación o acciones en la página.|
|**Solo campos, columnas y partes**|Borra todos los cambios de personalización que haya realizado en la página excepto los de la barra de navegación o de acciones. Esto incluye cambios en los campos, columnas, piezas e iconos. |
|**Todo**|Borra todos los cambios de personalización que haya realizado para que se parezca a la original. Esto incluye cambios en las barras de navegación y de acciones, campos, columnas, partes e iconos.|

## <a name="additional-points-of-interest"></a>Puntos de interés adicionales
Para ayudarle a comprender mejor la personalización, le presentamos algunos consejos.

- Cuando realice cambios en una página de ficha que abre de una lista, los cambios tendrán efecto en todos los registros que abra de esa lista. Por ejemplo, digamos que abre un cliente específico desde la página de la lista Clientes y la personaliza agregando un campo. Cuando abra otros clientes de la lista, también se mostrará el campo que agregó.
- Los cambios realizados tendrán efecto sobre todas las áreas de trabajo. Por ejemplo, si realiza un cambio en la lista Clientes cuando el área de trabajo está configurada en administrador de negocio, también verá el cambio en la página **Clientes** cuando el área de trabajo está configurada en Procesador de pedidos de ventas.
- Los cambios de una página realizados en un panel tendrán efecto en la página donde se muestre.  
- Solo puede agregar campos y columnas de una lista predefinida, que está basada en la página. No puede crear campos ni columnas nuevos.

## <a name="see-related-training-at-microsoft-learn"></a>Consulte Formación relacionada en [Microsoft Learn](/learn/modules/personalize-ui-dynamics-365-business-central/index)

## <a name="see-also"></a>Consulte también
[Personalizar páginas para perfiles](ui-personalization-manage.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Cambiar la configuración básica](ui-change-basic-settings.md)  
[Cambiar las funciones que se muestran](ui-experiences.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]