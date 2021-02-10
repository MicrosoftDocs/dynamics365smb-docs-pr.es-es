---
title: Crear fichas de producto para bienes o servicios | Documentos de Microsoft
description: Puede crear fichas de producto para servicios que venda como horas y para productos físicos, como productos de ensamblaje, productos terminados, componentes o materias primas, que venda del inventario.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: item, finished good, component, raw material, assembly item
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 6e4bf13885ccd7888e1750f4351741150df7b7df
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "4746221"
---
# <a name="register-new-items"></a>Registro de productos nuevos

Los productos, entre otros elementos, son la base de su empresa, las mercancías o servicios con las que comercializa. Cada producto se debe registrar como una ficha de producto.

Las fichas de producto contienen la información necesaria para comprar, almacenas, vender, entregar y contabilizar productos.

La ficha de producto puede ser del tipo **Inventario**, **Servicio** o **No inventario** para especificar si el producto representa una unidad de inventario físico, una unidad de tiempo de mano de obra o una unidad física sin seguimiento en el inventario. Para obtener más información, consulte [unidad física sin seguimiento en el inventario](inventory-about-item-types.md).

Un producto se puede estructurar como un producto principal con productos secundarios subyacentes en una lista de materiales (L.M.). En [!INCLUDE[prod_short](includes/prod_short.md)], una lista de materiales puede ser una L.M. de ensamblado o una L.M. de producción, en función de su uso. Para obtener más información, consulte [Trabajar con listas de materiales](inventory-how-work-BOMs.md).

Si le compra el mismo producto a varios proveedores, puede conectarlos a la ficha de producto. Los proveedores aparecerán después en la página **Tarifas de compra productos** , para poder fácilmente seleccionar un proveedor alternativo.

Los productos que ofrece a sus clientes pero que no desea administrar en su sistema hasta que comience a venderlos se pueden configurar como productos del catálogo. Los productos del catálogo no deben confundirse con artículos regulares de tipo **No inventario**. Para obtener más información, consulte [Trabajar con productos del catálogo](inventory-how-work-nonstock-items.md).  

> [!NOTE]  
> Si existen plantillas para distintos tipos de producto, aparece una página automáticamente cuando se crea una nueva ficha de producto en la que puede seleccionar una plantilla de producto apropiada. Si solo existe una plantilla de producto, las nuevas fichas de producto utilizan siempre esa plantilla.

En el siguiente procedimiento se explica cómo crear una ficha de producto desde cero. También puede crear nuevas fichas de producto copiando las existentes. Para obtener más información, consulte [Copiar productos existentes para crear productos nuevos](inventory-how-copy-items.md).  

> [!Video https://www.microsoft.com/videoplayer/embed/RE47eLx?rel=0]

## <a name="to-create-a-new-item-card"></a>Para crear una nueva ficha de producto.

1. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Productos** y luego elija el enlace relacionado.  
2. En la página **Productos**, seleccione la acción **Nuevo**.

    Si solo existe una plantilla de producto, se abre una nueva ficha de producto con algunos de los campos rellenados con la información de la plantilla.
3. En la página **Seleccionar una plantilla para un producto nuevo**, seleccione la plantilla que quiere usar para la nueva ficha de producto.
4. Elija el botón **Aceptar**. Se abre una nueva ficha de producto con algunos de los campos rellenados con la información de la plantilla.
5. Empiece a rellenar o cambiar campos en la ficha de producto según sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!NOTE]
> En el campo **Valoración de existencias**, determinará la forma en que se calcula el coste unitario, presumiendo el flujo de productos físicos por la empresa. Hay cinco métodos de valoración de existencias, según del tipo de producto. Para obtener más información, consulte [Detalles de diseño: Métodos de coste](design-details-costing-methods.md).
>
> Si selecciona **Promedio**, el coste unitario de un producto se calcula como el coste unitario medio en cada momento después de una compra. El inventario se valora con el supuesto de que todos los inventarios se venden simultáneamente. Con este ajuste, puede elegir el campo **Coste unitario** para ver en la página **Inf. general cálculo cte. medio** el historial de las transacciones con las que se calcula el coste medio.

Puede ver o editar los precios o los descuentos especiales que concede al cliente, o que le proveedor le concede, por el producto si se cumplen determinados criterios, como, por ejemplo, el cliente, la cantidad de pedido mínima o la fecha final. Para ello, se eligen las acciones **Establecer precios especiales** o **Establecer descuentos especiales**. Por ejemplo, cada fila de la página **Precios ventas** representa un precio especial. Cada columna representa un criterio que debe aplicarse para conceder a un cliente el precio especial que introduzca en el campo **Precio venta** de la página **Precios ventas**. Para obtener más información, consulte [Registrar acuerdos de pago, descuentos y precios de venta](sales-how-record-sales-price-discount-payment-agreements.md) o [Registrar precios y descuentos de compra especiales](purchasing-how-record-purchase-price-discount-payment-agreements.md).

El producto quedará registrado y la ficha de producto está lista para usarse en los documentos de compra y venta.

Si desea usar esta ficha de producto como plantilla cuando cree nuevas fichas de producto, puede guardarla. Para obtener más información, vea la siguiente sección:  

### <a name="to-save-the-item-card-as-a-template"></a>Para guardar la ficha de producto como plantilla

1. En la página **Ficha de producto**, seleccione la acción **Guardar como plantilla**. La página **Plantilla de producto** se abre mostrando la ficha de producto como plantilla.
2. Rellene los campos según sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Para volver a usar dimensiones en las plantillas, seleccione la acción **Dimensiones**. La página **Plantilla de dimensiones** se abre mostrando los códigos de dimensión configurados para el producto.
4. Modifique o introduzca los códigos de dimensión que se aplicarán a nuevas fichas de producto creadas con la plantilla.
5. Cuando haya finalizado la nueva plantilla de producto, haga clic en el botón **Aceptar**.

La plantilla de producto se agrega a la lista de plantillas de producto, de modo que puede usarla para crear nuevas fichas de producto.

### <a name="items-used-in-production-orders"></a>Productos utilizados en órdenes de producción

Si desea registrar productos que luego se utilicen en órdenes de producción, especifique el sistema de reposición como *Ord. prod.* en la ficha despegable **Reposición**. Para obtener más información, vea [Acerca de las órdenes de producción](production-about-production-orders.md).  

## <a name="to-set-up-multiple-vendors-for-an-item"></a>Para configurar varios proveedores para un producto

Si compra el mismo producto a varios proveedores, deberá introducir información acerca de cada proveedor del producto, como precios, plazo de entrega (días), descuentos, etc.  

1. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Productos** y luego elija el enlace relacionado.  
2. Seleccione el elemento correspondiente y, a continuación, elija la acción **Editar**.  
3. Seleccione la acción **Proveedores**.  
4. Elija el campo **Nº proveedor** y, a continuación, seleccione el proveedor que desea configurar para el producto.  
5. Si lo desea, puede rellenar el resto de los campos.  
6. Repita los pasos 2 a 5 para cada proveedor al que desee comprar el producto.

Los proveedores aparecerán después en la página **Tarifas de compra productos** , que se abre desde la tarjeta del producto, para poder fácilmente seleccionar un proveedor alternativo.

## <a name="categories-attributes-and-variants"></a>Categorías, atributos y desviaciones

[!INCLUDE[inventory_variant](includes/inventory_variant.md)]

## <a name="deleting-item-cards"></a>Eliminar fichas de producto

Si ha publicado una transacción para un artículo, no puede eliminar la ficha porque los movimientos pueden ser necesarias para la valoración de inventario o auditoría. Para eliminar fichas de producto con movimientos, póngase en contacto con el socio de Microsoft para hacerlo a través del código.  

## <a name="manage-inventory-in-warehouses"></a>Administrar el inventario en almacenes

Cuando registre un nuevo producto, verá campos relacionados con la gestión del almacén, especialmente en la Ficha desplegable **Almacén**. Si su organización no utiliza las capacidades de gestión de almacenes de [!INCLUDE [prod_short](includes/prod_short.md)], entonces puede ignorar esos campos.  

Si su organización configura posteriormente la gestión del almacén, en la mayoría de los casos, debe volver a cada producto existente para asegurarse de que tenga la información correcta en los distintos campos, de modo que los procesos del almacén se puedan ejecutar como se esperaba. Esta información puede incluir campos como **Código de clase de almacén** o **Código de plantilla de ubicación**. Para obtener más información, consulte [Detalles de diseño: Configuración almacén](design-details-warehouse-setup.md).  

## <a name="see-also"></a>Consulte también

[Inventario](inventory-manage-inventory.md)  
[Configurar unidades de medida](inventory-how-setup-units-of-measure.md)  
[Códigos arancelarios](finance-how-setup-report-intrastat.md#tariff-numbers)  
[Conciliar costes de inventario con la contabilidad general](finance-how-to-post-inventory-costs-to-the-general-ledger.md)  
[Crear numeración](ui-create-number-series.md)  
[Configurar los grupos contables](finance-posting-groups.md)  
[Compras](purchasing-manage-purchasing.md)  
[Ccial](sales-manage-sales.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
