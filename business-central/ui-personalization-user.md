---
title: Personalización de páginas | Documentos de Microsoft
description: Aprenda a personalizar la interfaz de usuario para que se adapte a su forma de trabajar en Business Central.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customize, personalize, personalization, hide columns, remove fields, move fields
ms.date: 04/01/2019
ms.author: jswymer
ms.openlocfilehash: de7acb10c76acc05fc6e6a5c708a8d412e4d9b30
ms.sourcegitcommit: 6dc83b27ac47f3b39a7b84cfb7446e7f48b8ce63
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 06/17/2019
ms.locfileid: "1632734"
---
# <a name="personalizing-your-workspace"></a>Personalización de su área de trabajo

Puede *personalizar* el área de trabajo para que se adapte a su trabajo y preferencias cambiando las páginas de modo que muestren únicamente la información que necesite y donde la necesite. Los cambios de personalización que realice solo afectarán a su visualización y no a la de otros usuarios.

Dependiendo del tipo de página y qué incluye, puede llevar a cabo varias acciones, como mover u ocultar campos, columnas y acciones, y mover y ocultar completas partes, etc.
<!--
-   Add, move, and remove fields.
-   Add, move, and remove columns in a list.
-   Change the freeze pane of columns in a list. The freeze pane locks one or more columns to the left side of a list so that are always present, even when you scroll horizontally.
-   Adjust the width of columns in a list.
-   Move and remove Cues (tiles).
-   Move and remove parts. Parts are subdivisions or areas on a page that contain things like multiple fields, another page, a chart, or tiles.

-->
> [!NOTE]
> Además de lo que los usuarios pueden personalizar, los administradores y los superusuarios pueden anular la personalización de los usuarios y definir qué funciones están disponibles en todas las empresas o en las empresas específicas. Para obtener más información, consulte [Personalizar Business Central](ui-customizing-overview.md).

## <a name="to-personalize-a-page"></a>Para personalizar una página

1. En la esquina superior derecha, seleccione el icono ![Configuración](media/ui-experience/settings_icon_small.png "Icono Configuración para el área de trabajo") y elija **Personalizar**.

    El banner **Personalización** aparece en la parte superior para indicar que puede empezar a realizar cambios.

    ![Modo Personalizar](media/ui_personalize_mode_small.png "Modo Personalizar")

2. Vaya a una página que desee personalizar.

    Si se muestra ![Bloqueo de personalización](media/personalization-lock-icon.png "Bloqueo de personalización") o ![Personalización bloqueada](media/personalization-blocked-icon.png "Personalización bloqueada") en el banner, no puede personalizar la página. Para obtener más información, vea [Por qué no puedo personalizar la página](ui-personalization-locked.md).

3. Señale un área que desee personalizar, como un encabezado de campo o columna en una lista. Todo lo que se pueda personalizar se resalta inmediatamente con una punta de flecha o un borde. Consulte la [siguiente sección](#What) para obtener más información sobre la acciones que se pueden realizar.

4. Puede seguir realizando cambios en la misma página o abrir otra página. Los cambios se guardan automáticamente a medida que los crea. Cuando haya terminado, en el banner **Personalización**, elija **Hecho**.

## <a name="What"></a>Qué puede personalizar

|Qué desea hacer|Cómo hacerlo|Comentarios|
|----|------------|-------|
|Mover algo, un campo, una columna de la lista, un icono, una acción o una pieza|Señale en cualquier lugar qué desea mover y arrástrelo a su nueva ubicación. La ubicación se indica con una fina línea vertical u horizontal.<br /><br />![Icono No se puede mover aquí](media/personalization-cannot-move-here.png "Modo Personalizar - Icono No se puede mover aquí") indica que no puede mover el elemento a la ubicación seleccionada.|Las piezas son subdivisiones o áreas en una página que contienen elementos como múltiples campos, otra página, un gráfico o iconos.<br /><br />Para obtener más información sobre la personalización de acciones, consulte la [siguiente sección](ui-personalization-user.md#Actions). |
|Ocultar algo, un campo, una columna de la lista, un icono o una pieza.|Seleccione la punta de flecha y elija <b>Ocultar</b>.|Si el campo que oculta también se muestra en el encabezado de la ficha desplegable cuando está contraída, el campo ya no aparecerá allí.|
|Agregar un campo o columna.|En el banner <b>Personalización</b>, elija <b>Más</b> y seleccione <b>Campo</b>.<br /></br>El panel <b>Agregar campo a página</b> se abre a la derecha. Muestra los campos que se pueden agregar a la página.<br /><br />Para agregar un campo, arrástrelo de panel a la ubicación que desee. La ubicación se indica con una fina línea vertical u horizontal.|Cada página incluye un conjunto predefinido de campos que puede mostrar. Siga este procedimiento para agregar campos o columnas que no se han mostrado anteriormente o para mostrar los campos que ha ocultado.|
|Mostrar un campo de la cabecera de una ficha desplegable cuando está contraída.|Seleccione la punta de flecha y seleccione <b>Mostrar cuando se contrae</b>. <br /> <br />Si no hace ve esta opción, significa que ya está establecida. En este caso, para dejar de mostrar el campo del encabezado de la ficha desplegable, elija <b>Mostrar Siempre</b>.|*Ficha desplegable* es el término que se utiliza para un grupo de campos que aparecerán bajo un encabezado común. Utilice la opción <b>Mostrar cuando se contrae</b> para mostrar los campos más importantes. Si selecciona un campo del encabezado, se abrirá la ficha desplegable y con el enfoque en el campo seleccionado.<br /><br />Esta opción solo es aplicable si una página tiene una más de una ficha desplegable. Si hay solo una ficha desplegable, no se puede contraer, por lo que la opción <b>Mostrar cuando se contrae</b> no está disponible.|
|Hacer que un campo se muestre solo cuando seleccione **Mostrar más**.|Seleccione la punta de flecha y seleccione <b>Mostrar en "Mostrar más</b>. <br /> <br />Si no ve la opción <b>Mostrar en "Mostrar más"</b>, significa que ya está establecida. En este caso, para que un campo se muestre siempre, no solo al seleccionar **Mostrar más**, elija <b>Mostrar siempre</b>.||
|Cambiar la inmovilización de panel de una lista a otra columna. |Seleccione la punta de la flecha de la columna que desee establecer como la última de la inmovilización de panel y, a continuación, elija <b>Establecer inmovilización de panel</b>.<br /><br/>Si desea volver a configurar la inmovilización de panel en su ubicación original diseñada, seleccione la punta de flecha para la columna actual y elija <b>Borrar inmovilización de panel</b>. Nota: No puede eliminar la inmovilización de panel.|La inmovilización de panel especifica las columnas que siempre aparecen a la izquierda, incluso durante el desplazamiento horizontal.|  
|Cambiar el ancho de una columna.|En la cabecera de la lista, arrastre el límite entre columnas. <br /><br />Puede hacer doble clic en el límite entre las cabeceras de columna para ajustar automáticamente, lo que ajusta el ancho a un tamaño cómodo para facilitar la lectura.||
|Saltar un campo al presionar Entrar.|Seleccione la punta de flecha junto al campo, o la cabecera de columna en una lista, y seleccione **Excluir de entrada rápida**. <br /><br /> Si no ve esta opción, significa que el campo ya está establecido para saltarlo. En este caso, para dejar de omitir el campo, elija **Incluir en entrada rápida**. |Consulte [Acelerar la entrada de datos con la entrada rápida](ui-enter-data.md#QuickEntry)|

## <a name="Actions"></a>Personalización de acciones

Puede personalizar la barra de acciones que se encuentra en la parte superior de la página, como se indica mediante el área resaltada en el ejemplo siguiente.

![Personalizar barra de acciones](media/personalize-action-bar.png "Personalizar barra de acciones")

La personalización le permite decidir qué acciones se mostrarán en la barra de acciones y dónde se mostrarán. Puede mostrar, ocultar o mover acciones individuales o grupos de acciones. La personalización de la barra de acciones se hace básicamente de la misma forma que con otros productos del área de trabajo. Sin embargo, lo que pueden realizar exactamente con una acción o un grupo depende de dónde se encuentre la acción o el grupo en la barra de acciones. La mejor forma de averiguarlo es probar cosas y dejar que la pantalla le guíe. En las secciones siguientes se explicarán algunos de los matices de la personalización de la barra de acciones.

### <a name="action-bar-overview"></a>Descripción general de la barra de acciones

Hay un par de términos con los que debería estar familiarizado para entender mejor la personalización de las acciones: *grupo de acciones* y *categoría promocionada*.  

Un *grupo de acciones* es un elemento que se expande para mostrar otras acciones o grupos. Por ejemplo, en la ilustración siguiente, **Registro** es un grupo de acciones.

Una *categoría promocionada* es un grupo de acciones que aparece entre las dos líneas verticales `|` en la barra de acciones. Las categorías suelen incluir las acciones más utilizadas, para que pueda encontrarlas rápidamente. Por ejemplo, en el ejemplo siguiente, **Lanzar**, **Registro**, **Facturar** y **Navegar** son categorías promocionadas.

![Personalizar grupo de barra de acciones](media/personalize-action-bar-group-clip.png "Personalizar grupo de barra de acciones ")

### <a name="to-remove-hide-and-show-actions-and-groups"></a>Para eliminar, ocultar y mostrar acciones y grupos

Para mostrar u ocultar una acción o grupo de acciones, selecciónela y, a continuación, elija una de las siguientes opciones:

|Opción|Lo que hace|
|------|------------
|**Eliminar**|Esta opción aparece si la acción seleccionada también se muestra en otro lugar de la barra de acciones. Al seleccionar esta opción se elimina la acción de la ubicación seleccionada para que ya no aparezca. La acción o grupo de acciones permanecerá en otros lugares. |
|**Ocultar**|Esta opción aparece si la acción o el grupo de acciones no se encuentra en otro lugar de la barra de acciones. Como **Eliminar**, al elegir esta opción se provocará que la acción o el grupo de acciones desaparezca de la barra de acciones. No obstante, en el modo de personalización, aún se mostrará la acción o el grupo de acciones en la ubicación actual, excepto que aparece atenuada.|
|**Mostrar**|Esta opción aparece si la acción o grupo de acciones ha sido previamente ocultada (atenuada). Al elegir esta opción se provocará que la acción o el grupo de acciones aparezca en la barra de acciones.|

### <a name="to-move-actions-and-action-groups"></a>Para mover acciones y grupos de acciones

Para mover una acción o grupo de acciones, arrástrelo y suéltelo en la ubicación deseada, igual que con los campos y columnas.

El lugar donde se pueden soltar acciones o grupos de acciones se indica mediante una línea horizontal entre las acciones o un borde alrededor de un grupo de acciones.

- Puede mover acciones individuales a las categorías promocionadas, pero no puede reorganizar el orden de las acciones en la categoría.
- No puede mover un grupo de acciones a una categoría promocionada.
- Para mover una acción o un grupo de acciones a otro grupo de acciones que está vacío, arrastre la acción o el grupo de acciones al nuevo grupo y colóquelo en el cuadro **Colocar aquí una acción** .

## <a name="additional-points-of-interest"></a>Puntos de interés adicionales

Para ayudarle a comprender mejor la personalización, le presentamos algunos consejos.

- Cuando realice cambios en una página de ficha que abre de una lista, los cambios tendrán efecto en todos los registros que abra de esa lista. Por ejemplo, digamos que abre un cliente específico desde la página de la lista Clientes y la personaliza agregando un campo. Cuando abra otros clientes de la lista, también se mostrará el campo que agregó.
- Los cambios realizados tendrán efecto sobre todas las áreas de trabajo. Por ejemplo, si realiza un cambio en la lista Clientes cuando el área de trabajo está configurada en administrador de negocio, también verá el cambio en la lista Clientes cuando el área de trabajo está configurada en Procesador de pedidos de ventas.
- Los cambios de una página realizados en un panel tendrán efecto en la página donde se muestre.  
- Solo puede agregar campos y columnas de una lista predefinida, que está basada en la página. No puede crear campos ni columnas nuevos.

## <a name="to-clear-personalization"></a>Para borrar la personalización

En algún momento, es posible que desee borrar algunos o todos los cambios de personalización que hizo en esta página a lo largo del tiempo. Para ello, en el banner **Personalización**, elija **Más**, **Borrar personalización** y, a continuación, elija una de las opciones siguientes. Tenga en cuenta que el borrado de la personalización no se puede deshacer.

|Opción|Lo que hace|
|------|------------
|Solo acciones|Borra todos los cambios de personalización que haya realizado en la barra de acciones en la página.|
|Todos excepto acciones|Borra todos los cambios de personalización que haya realizado en la página excepto los de la barra de acciones. Esto incluye cambios en los campos, columnas, piezas e iconos. |
|Todo|Borra todos los cambios de personalización que haya realizado en la página para que se parezca a la original. Esto incluye cambios en la barra de acciones, campos, columnas, piezas e iconos.|

## <a name="see-also"></a>Consulte también

[Administrar la personalización](ui-personalization-manage.md)  
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Cambiar la configuración básica](ui-change-basic-settings.md)  
[Cambiar las funciones que se muestran](ui-experiences.md)  
