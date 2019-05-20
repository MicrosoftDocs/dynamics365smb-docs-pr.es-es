---
title: Procedimiento para configurar unidades de medida de producto | Documentos de Microsoft
description: Puede configurar varias unidades de medida para un producto de forma que pueda asignar las unidades de medida al producto.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: UOM
ms.date: 04/01/2019
ms.author: SorenGP
ms.openlocfilehash: 47d59af91af7c043c98a4db2a5c103b0052e32e2
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/29/2019
ms.locfileid: "1239434"
---
# <a name="set-up-item-units-of-measure"></a>Configurar unidades de medida de producto
Puede configurar varias unidades de medida para un producto de forma que pueda asignar las unidades de medida al producto para los fines siguientes:

- Asigne una unidad de medida base en la ficha de producto para definir cómo se almacena en el inventario y para utilizar como base de conversión para las unidades de medida alternas.
- Asigne las unidades de medida alternas a los documentos de compra, producción o venta para especificar cuántas unidades de la unidad de medida base que se llevarán al mismo tiempo en dichos procesos. Por ejemplo, puede comprar el producto en palés y utilizar solo piezas sueltas en la producción.

Si un producto se almacena en una unidad de medida pero se fabrica en otra, se crea una orden de producción que utiliza una unidad de medida de la sección de fabricación para calcular la cantidad correcta de componentes durante el trabajo por lotes **Actualizar orden producción**. Un ejemplo del cálculo de una unidad de medida de la sección de fabricación es el caso en que un producto fabricado se almacena por piezas pero se produce en toneladas. Para obtener más información, consulte [Trabajar con la unidad de medida de lote de fabricación](production-how-to-use-the-manufacturing-batch-unit-of-measure.md).

## <a name="to-set-up-a-unit-of-measure"></a>Configurar una unidad de medida
1. Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Productos** y luego elija el enlace relacionado.
2. Abra la ficha del producto para el que desea configurar unidades de medida alternas.
3. Elija la acción **Unidades medida**. Se abre la página **Unidades medida producto**.
4. Si el campo **Unidad de medida base** en la ficha de producto se ha rellenado, dicha unidad de medida ya está configurada.
5. Seleccione la acción **Nuevo**. Se insertará una nueva línea vacía.
6. En el campo de **Código**, escriba el nombre de la unidad de medida. También, elija el campo para seleccionar de los códigos de la unidad de medida que figuren en la base de datos.
7. En el campo **Cdad. por unidad medida**, especifique cuántas unidades de la unidad de medida base contiene la nueva unidad de medida.
8. Repita los pasos 5 a 7 para configurar todas las unidades de medida alternas que desea utilizar en distintos procesos para este producto.

Ahora puede utilizar las unidades de medida alternas de los documentos de compra, producción y venta. Para obtener más información, consulte Introducir los códigos de unidad de medida predeterminada para las transacciones de compra y las transacciones de venta o Usar la unidad de medida de lote de fabricación.

## <a name="to-set-up-unit-of-measure-translations"></a>Para configurar traducciones de unidades de medida
Cuando vende productos a clientes extranjeros, quizás le interese especificar la unidad de medida en el idioma del cliente. Para ello, primero debe configurar las traducciones correspondientes de las unidades de medida.

1. Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Uds. de medida** y luego elija el enlace relacionado.
2. Seleccione el código para el que desea configurar las traducciones y, a continuación, elija la acción **Traducciones**.
3. En el campo **Cód. idioma**, seleccione la flecha desplegable para ver una lista de los códigos de idioma disponibles. Seleccione el código de idioma para el que desea especificar una traducción y, a continuación, elija el botón Aceptar para copiarlo en el campo.
4. En el campo **Descripción**, escriba el texto correspondiente.
5. Repita los pasos del 2 al 4 con los códigos de unidad de medida y los idiomas para los que desea especificar traducciones.

## <a name="to-enter-a-default-unit-of-measure-code-for-sales-and-purchasing-transactions"></a>Para introducir un código de unidad de medida predeterminada para las transacciones de compra y venta
Si suele comprar o vender en unidades que no sean la unidad de medida base, especifique unidades de medida diferentes para las compras y las ventas. Para ello, debe configurar las unidades de medida en la página **Unidades medida producto**.

1. Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Productos** y luego elija el enlace relacionado.
2. Abra la ficha de producto relevante para la que desea especificar un código de unidad de medida de compra o venta predeterminado.
3. Para ventas, en la ficha desplegable **Facturación**, en el campo **Unidad medida venta**, abra la página **Unidades medida producto**.
4. En compras, en la ficha desplegable **Reposición**, en el campo **Unidad medida compra**, abra la página **Unidades medida producto**.
5. Seleccione el código que desea configurar como la unidad de medida predeterminada para ventas o compras, respectivamente y elija el botón **Aceptar**.

## <a name="see-also"></a>Consulte también
[Trabajar con la unidad de medida de lote de fabricación](production-how-to-use-the-manufacturing-batch-unit-of-measure.md)  
[Administrar inventario](inventory-manage-inventory.md)  
[Administrar compras](purchasing-manage-purchasing.md)  
[Administrar ventas](sales-manage-sales.md)    
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
