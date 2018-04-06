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
ms.date: 08/31/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 9643e71c29adf4b4be1d9d474832e3e29f2c21d8
ms.contentlocale: es-es
ms.lasthandoff: 03/22/2018

---
# <a name="register-new-items"></a>Registro de productos nuevos
Los productos, entre otros elementos, son la base de su empresa, las mercancías o servicios con las que comercializa. Cada producto se debe registrar como una ficha de producto.

Las fichas de producto contienen la información necesaria para comprar, almacenas, vender, entregar y contabilizar productos.

La ficha de producto puede ser de tipo **Inventario** o **Servicio** para especificar si el producto es una unidad física o una unidad de tiempo de mano de obra. Aparte de algunos campos relacionados con los aspectos físicos de un producto, todos los campos de un producto funcionan de la misma forma para los productos de inventario y los servicios. Para obtener más información acerca de la venta de un producto, vea [Vender productos](sales-how-sell-products.md) o [Facturar ventas](sales-how-invoice-sales.md)

Un producto se puede estructurar como un producto principal con productos secundarios subyacentes en una lista de materiales (L.M.). En [!INCLUDE[d365fin](includes/d365fin_md.md)], una lista de materiales puede ser una L.M. de ensamblado o una L.M. de producción, en función de su uso. Para obtener más información, consulte [Trabajar con listas de materiales](inventory-how-work-BOMs.md).

> [!NOTE]  
>   Si existen plantillas para distintos tipos de producto, aparece una ventana automáticamente cuando se crea una nueva ficha de producto en la que puede seleccionar una plantilla de producto apropiada. Si solo existe una plantilla de producto, las nuevas fichas de producto utilizan siempre esa plantilla.

Si le compra el mismo producto a varios proveedores, puede conectarlos a la ficha de producto. Los proveedores aparecerán después en la ventana **Tarifas de compra productos** , para poder fácilmente seleccionar un proveedor alternativo.

## <a name="to-create-a-new-item-card"></a>Para crear una nueva ficha de producto.
1. Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Productos** y, a continuación, seleccione el vínculo relacionado.  
2. En la ventana **Productos**, seleccione la acción **Nuevo**.

    Si solo existe una plantilla de producto, se abre una nueva ficha de producto con algunos de los campos rellenados con la información de la plantilla.
3. En la ventana **Seleccionar una plantilla para un producto nuevo**, seleccione la plantilla que quiere usar para la nueva ficha de producto.
4. Elija el botón **Aceptar**. Se abre una nueva ficha de producto con algunos de los campos rellenados con la información de la plantilla.
5. Empiece a rellenar o cambiar campos en la ficha de producto según sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!NOTE]
> En el campo **Valoración de existencias**, determinará la forma en que se calcula el coste unitario, presumiendo el flujo de productos físicos por la empresa. Hay cinco métodos de valoración de existencias, según del tipo de producto. Para obtener más información, consulte [Detalles de diseño: Métodos de coste](design-details-costing-methods.md).
>
> Si selecciona **Promedio**, el coste unitario de un producto se calcula como el coste unitario medio en cada momento después de una compra. El inventario se valora con el supuesto de que todos los inventarios se venden simultáneamente. Con este ajuste, puede elegir el campo **Coste unitario** para ver en la ventana **Inf. general cálculo cte. medio** el historial de las transacciones con las que se calcula el coste medio.

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

## <a name="to-set-up-multiple-vendors-for-an-item"></a>Para configurar varios proveedores para un producto  
Si compra el mismo producto a varios proveedores, deberá introducir información acerca de cada proveedor del producto, como precios, plazo de entrega (días), descuentos, etc.  

1.  Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Productos** y, a continuación, seleccione el vínculo relacionado.  
2.  Seleccione el elemento correspondiente y, a continuación, elija la acción **Editar**.  
3.  Seleccione la acción **Proveedores**.  
4.  Elija el campo **Nº proveedor** y, a continuación, seleccione el proveedor que desea configurar para el producto.  
5.  Si lo desea, puede rellenar el resto de los campos.  
6.  Repita los pasos 2 a 5 para cada proveedor al que desee comprar el producto.

Los proveedores aparecerán después en la ventana **Tarifas de compra productos** , que se abre desde la tarjeta del producto, para poder fácilmente seleccionar un proveedor alternativo.

## <a name="see-also"></a>Consulte también
  [Grupos contables inventario](inventory-manage-inventory.md)  
  [Compras](purchasing-manage-purchasing.md)  
  [Ccial](sales-manage-sales.md)  
  [Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

