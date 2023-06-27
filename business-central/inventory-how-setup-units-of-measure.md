---
title: Procedimiento para configurar unidades de medida de producto | Documentos de Microsoft
description: Puede configurar varias unidades de medida para un producto de forma que pueda asignar las unidades de medida al producto.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: UOM
ms.date: 04/01/2021
ms.author: edupont
---
# <a name="set-up-units-of-measure"></a><a name="set-up-units-of-measure"></a>Configurar unidades de medida

Como parte de la configuración de su [!INCLUDE [prod_short](includes/prod_short.md)], configura unidades de medida generales en la página **Unidades de medida**. Luego, cuando registra nuevos artículos, especifica la unidad de medida base en la **Ficha de producto**. Pero también puede agregar unidades de medida más adelante.  

Puede configurar varias unidades de medida para un producto de forma que pueda asignar las unidades de medida al producto para los fines siguientes:

- Asigne una unidad de medida base en la ficha de producto para definir cómo se almacena en el inventario y para utilizar como base de conversión para las unidades de medida alternas.
- Asigne las unidades de medida alternas a los documentos de compra, producción o venta para especificar cuántas unidades de la unidad de medida base que se llevarán al mismo tiempo en dichos procesos. Por ejemplo, puede comprar el producto en palés y utilizar solo piezas sueltas en la producción.

Si un producto se almacena en una unidad de medida pero se fabrica en otra, se crea una orden de producción que utiliza una unidad de medida de la sección de fabricación para calcular la cantidad correcta de componentes durante el trabajo por lotes **Actualizar orden producción**. Un ejemplo del cálculo de una unidad de medida de la sección de fabricación es el caso en que un producto fabricado se almacena por piezas pero se produce en toneladas. Para obtener más información, consulte [Trabajar con la unidad de medida de lote de fabricación](production-how-to-use-the-manufacturing-batch-unit-of-measure.md).  

Otra herramienta que facilita el trabajo con varias unidades de medida para elementos es la capacidad de especificar una precisión de redondeo para las unidades de medida base. La especificación de una precisión de redondeo proporciona una guía sobre lo que alguien debe introducir para un proceso empresarial determinado y ayuda a reducir los problemas de redondeo. Cuando usa unidades de medida alternativas, el valor en el campo **Cant. por unidad de medida** ayuda a calcular la cantidad en la unidad de medida base, lo que puede generar problemas de redondeo. Por ejemplo, imagina que estás recibiendo una caja que contiene seis productos. Cuando la caja llega a su almacén, descubre que falta uno de los seis productos. Decide no publicar el recibo de una caja, sino cambiar la cantidad recibida a cinco de seis piezas. Eso llevaría a recibir 4,99998 piezas, en lugar de cinco. En la página **Unidades medida producto**, el campo **Precisión de redondeo de cantidad** le permite especificar un valor que convertirá la cantidad en un número más fácil de entender. Continuando con el ejemplo, introduciríamos **1** en el campo para redondear hasta cinco piezas iguales.

## <a name="to-set-up-units-of-measure"></a><a name="to-set-up-units-of-measure"></a>Para configurar unidades de medida

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Unidades de medida** y luego elija el enlace relacionado.  
2. Seleccione la acción **Nuevo**. Se insertará una nueva línea vacía.  
3. Rellene los campos. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]  
4. Si sabe que su organización va a vender productos con esta unidad de medida a clientes en otros países o regiones, puede agregar traducciones.  
    1. Seleccione el código para el que desea configurar las traducciones y, a continuación, elija la acción **Traducciones**.
    2. En el campo **Cód. idioma**, seleccione la flecha desplegable para ver una lista de los códigos de idioma disponibles. Seleccione el código de idioma para el que desea especificar una traducción y, a continuación, elija el botón Aceptar para copiarlo en el campo.
    3. En el campo **Descripción**, escriba el texto correspondiente.
5. Repita los pasos anteriores para cualquier unidad de medida adicional que desee agregar.  

Cuando registre un nuevo elemento, puede elegir la unidad medida base de la lista de unidades de medida que ha configurado. También puede configurar múltiples unidades de medida para un producto.  

## <a name="to-set-up-multiple-item-units-of-measure"></a><a name="to-set-up-multiple-item-units-of-measure"></a>Para configurar múltiples unidades medida producto

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Productos**, y luego elija el enlace relacionado.
2. Abra la ficha del producto para el que desea configurar unidades de medida alternas.
3. Elija la acción **Unidades medida**. Se abre la página **Unidades medida producto**.
4. Si el campo **Unidad de medida base** en la ficha de producto se ha rellenado, dicha unidad de medida ya está configurada.
5. Seleccione la acción **Nuevo**. Se insertará una nueva línea vacía.
6. En el campo de **Código**, escriba el nombre de la unidad de medida. También, elija el campo para seleccionar de los códigos de la unidad de medida que figuren en la base de datos.
7. En el campo **Cdad. por unidad medida**, especifique cuántas unidades de la unidad de medida base contiene la nueva unidad de medida.
8. Opcionalmente, en los campos **Alto**, **Ancho**, **Longitud**y **Peso**, puede especificar información exacta acerca del tamaño de una unidad de medida para que [!INCLUDE [prod_short](includes/prod_short.md)] pueda calcular cuántas unidades de cada producto pueden colocarse en una ubicación determinada. El campo **Cubicaje** se calcula automáticamente en función de **Altura**, **Ancho** y **Longitud**.

    Si alguno de estos campos contiene un valor distinto de 0, esa medida se utiliza durante todos los procesos que implican colocar productos en una ubicación: almacenamiento, movimientos, recibos, envíos, picking y ajustes. [!INCLUDE [prod_short](includes/prod_short.md)] comprueba la suma del cubicaje de cada medida física de los productos que se van a ubicar y los productos que ya están en una ubicación con el tamaño máximo u otra medida que puede contener una ubicación, según la política de capacidad de ubicación que ha seleccionado en la ficha de almacén para este producto. En otras palabras, debe usar la misma unidad de medida para cada dimensión en todas las unidades de medida producto: use kilogramos o libras para el peso, por ejemplo, pero sea consistente.
9. Repita los pasos 5 a 7 para configurar todas las unidades de medida alternas que desea utilizar en distintos procesos para este producto.

    En el campo **Unidad medida base** en la parte inferior de la ventana, puede ver o modificar la unidad de medida base del producto. También puede modificar la unidad de medida base en el campo **Unidad medida base** de la ficha de producto. En la página **Unidades medida producto**, la unidad medida base debe tener el valor **1** en el campo **Cant. por unidad de medida**.

Ahora puede utilizar las unidades de medida alternas de los documentos de compra, producción y venta. Para obtener más información, consulte [Para introducir un código de unidad de medida predeterminada para las transacciones de compra y venta](#to-enter-a-default-unit-of-measure-code-for-sales-and-purchasing-transactions).  

## <a name="to-set-up-unit-of-measure-translations"></a><a name="to-set-up-unit-of-measure-translations"></a>Para configurar traducciones de unidades de medida

Cuando vende productos a clientes extranjeros, quizás le interese especificar la unidad de medida en el idioma del cliente. Puede hacerlo especificando traducciones para unidades de medida.

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Unidades de medida** y luego elija el enlace relacionado.
2. Seleccione el código para el que desea configurar las traducciones y, a continuación, elija la acción **Traducciones**.
3. En el campo **Cód. idioma**, seleccione la flecha desplegable para ver una lista de los códigos de idioma disponibles. Seleccione el código de idioma para el que desea especificar una traducción y, a continuación, elija el botón Aceptar para copiarlo en el campo.
4. En el campo **Descripción**, escriba el texto correspondiente.
5. Repita los pasos del 2 al 4 con los códigos de unidad de medida y los idiomas para los que desea especificar traducciones.

## <a name="to-enter-a-default-unit-of-measure-code-for-sales-and-purchasing-transactions"></a><a name="to-enter-a-default-unit-of-measure-code-for-sales-and-purchasing-transactions"></a>Para introducir un código de unidad de medida predeterminada para las transacciones de compra y venta

Si suele comprar o vender en unidades que no sean la unidad de medida base, especifique unidades de medida diferentes para las compras y las ventas. Para ello, debe configurar las unidades de medida en la página **Unidades medida producto**.

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Productos**, y luego elija el enlace relacionado.
2. Abra la ficha de producto relevante para la que desea especificar un código de unidad de medida de compra o venta predeterminado.
3. Para ventas, en la ficha desplegable **Facturación**, en el campo **Unidad medida venta**, abra la página **Unidades medida producto**.
4. En compras, en la ficha desplegable **Reposición**, en el campo **Unidad medida compra**, abra la página **Unidades medida producto**.
5. Seleccione el código que desea configurar como la unidad de medida predeterminada para ventas o compras, respectivamente y elija el botón **Aceptar**.

## <a name="see-related-microsoft-training"></a><a name="see-related-microsoft-training"></a>Consultar la [formación de Microsoft](/training/modules/trade-master-data-dynamics-365-business-central/) relacionada

## <a name="see-also"></a><a name="see-also"></a>Consulte también .

[Trabajar con la unidad de medida de lote de fabricación](production-how-to-use-the-manufacturing-batch-unit-of-measure.md)  
[Registro de productos nuevos](inventory-how-register-new-items.md)  
[Administrar inventario](inventory-manage-inventory.md)  
[Administrar compras](purchasing-manage-purchasing.md)  
[Administrar ventas](sales-manage-sales.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
