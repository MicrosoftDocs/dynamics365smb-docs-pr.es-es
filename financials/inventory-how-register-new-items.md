---
title: Crear fichas de producto para bienes o servicios | Documentos de Microsoft
description: "Puede crear fichas de producto para servicios que venda como horas y para productos físicos, como productos de ensamblaje, productos terminados, componentes o materias primas, que venda del inventario."
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: item, finished good, component, raw material, assembly item
ms.date: 06/02/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 719e11f2c8fee3d7e5dd3736754700b68f57379c
ms.contentlocale: es-es
ms.lasthandoff: 07/07/2017


---
# <a name="how-to-register-new-items"></a>Registro de productos nuevos
Los productos, entre otros elementos, son la base de su empresa, las mercancías o servicios con las que comercializa. Cada producto se debe registrar como una ficha de producto.

Las fichas de producto contienen la información necesaria para comprar, almacenas, vender, entregar y contabilizar productos.

La ficha de producto puede ser de tipo **Inventario** o **Servicio** para especificar si el producto es una unidad física o una unidad de tiempo de mano de obra. Aparte de algunos campos relacionados con los aspectos físicos de un producto, todos los campos de un producto funcionan de la misma forma para los productos de inventario y los servicios. Para obtener más información acerca de la venta de un producto, vea [Procedimiento: Vender productos](sales-how-sell-products.md) o [Procedimiento: Facturar ventas](sales-how-invoice-sales.md)

Un producto se puede estructurar como un producto principal con productos secundarios subyacentes en una lista de materiales (L.M.). En [!INCLUDE[d365fin](includes/d365fin_md.md)], una lista de materiales se denomina L.M. de ensamblado. Las L.M. de ensamblado se usan para estructurar los productos principales que vende como kits que constan de los componentes del principal o que ensamble para pedido o para stock. Para obtener más información sobre cómo trabajar con el formulario, consulte [Trabajar con listas de materiales](inventory-how-work-BOMs.md).

> [!NOTE]  
>   Si existen plantillas para distintos tipos de producto, aparece una ventana automáticamente cuando se crea una nueva ficha de producto en la que puede seleccionar una plantilla de producto apropiada. Si solo existe una plantilla de producto, las nuevas fichas de producto utilizan siempre esa plantilla.

## <a name="to-create-a-new-item-card"></a>Para crear una nueva ficha de producto.
1. En la página Inicio, elija la acción **Productos** para abrir la lista de productos existentes.  
2. En la ventana **Productos**, seleccione la acción **Nuevo**.

    Si solo existe una plantilla de producto, se abre una nueva ficha de producto con algunos de los campos rellenados con la información de la plantilla.
3. En la ventana **Seleccionar una plantilla para un producto nuevo**, seleccione la plantilla que quiere usar para la nueva ficha de producto.
4. Elija el botón **Aceptar**. Se abre una nueva ficha de producto con algunos de los campos rellenados con la información de la plantilla.
5. Empiece a rellenar o cambiar campos en la ficha de producto según sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

En la ficha desplegable **Precio y registro**, puede observar los precios especiales o los descuentos que concede al cliente por el producto si se cumplen determinados criterios, como, por ejemplo, el cliente, la cantidad de pedido mínima o la fecha final. Cada fila representa un precio especial o un descuento de línea. Cada columna representa un criterio aplicable para autorizar el precio especial que se introduzca en el campo **Precio de venta**, o el descuento de línea que se introduzca en el campo **% Descuento línea**. Para más información, vea [Registrar acuerdos de pago, descuentos y precios de venta](sales-how-record-sales-price-discount-payment-agreements.md).

El producto quedará registrado y la ficha de producto está lista para usarse en los documentos de compra y venta.

Si desea usar esta ficha de producto como plantilla cuando cree nuevas fichas de producto, puede guardarla. Para obtener más información, vea la siguiente sección:

## <a name="to-save-the-item-card-as-a-template"></a>Para guardar la ficha de producto como plantilla
1. En la ventana **Ficha de producto**, seleccione la acción **Guardar como plantilla**. La ventana **Plantilla de producto** se abre mostrando la ficha de producto como plantilla.
2. Rellene los campos según sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Para volver a usar dimensiones en las plantillas, seleccione la acción **Dimensiones**. La ventana **Plantilla de dimensiones** se abre mostrando los códigos de dimensión configurados para el producto.
4. Modifique o introduzca los códigos de dimensión que se aplicarán a nuevas fichas de producto creadas con la plantilla.
5. Cuando haya finalizado la nueva plantilla de producto, haga clic en el botón **Aceptar**.

La plantilla de producto se agrega a la lista de plantillas de producto, de modo que puede usarla para crear nuevas fichas de producto.

## <a name="see-also"></a>Consulte también
  [Inventario](inventory-manage-inventory.md)  
  [Compras](purchasing-manage-purchasing.md)  
  [Ventas](sales-manage-sales.md)  
  [Trabajar con [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](ui-work-product.md)

## [!INCLUDE[d365fin](includes/free_trial_md.md)]
