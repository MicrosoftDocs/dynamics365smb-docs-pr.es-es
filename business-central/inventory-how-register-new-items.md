---
title: Crear fichas de producto para bienes o servicios (contiene vídeo)
description: Cree fichas de productos para servicios que venda por horas y para productos físicos. Los ejemplos incluyen productos de ensamblaje y productos terminados que vende desde su inventario.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'item, finished good, component, raw material, assembly item, item substitution'
ms.search.form: '30, 5717, 31, 32, 346, 9091, 5718, 5716, 5720, 1384, 1383, 35, 5404, 1378, 5719'
ms.date: 11/02/2022
ms.author: bholtorf
---
# <a name="register-new-items"></a>Registro de productos nuevos

Los productos, entre otros elementos, son la base de su empresa, las mercancías o servicios con las que comercializa. Cada producto se debe registrar como una ficha de producto.

Las fichas de producto contienen la información necesaria para comprar, almacenas, vender, entregar y contabilizar productos.

La ficha de producto puede ser del tipo **Inventario**, **Servicio** o **No inventario** para especificar si el producto representa una unidad de inventario físico, una unidad de tiempo de trabajo o una unidad física sin seguimiento en el inventario. Para obtener más información, consulte [unidad física sin seguimiento en el inventario](inventory-about-item-types.md).

Un producto se puede estructurar como un producto principal con productos secundarios subyacentes en una lista de materiales (L.M.). Obtenga más información sobre las L.M. de ensamblado y las L.M. en [Trabajar con listas de materiales](inventory-how-work-BOMs.md).

Si le compra el mismo producto a varios proveedores, puede conectarlos a la ficha de producto. La página **Tarifas de compra productos** muestra a los proveedores, para poder fácilmente seleccionar un proveedor alternativo.

*Productos del catálogo* son productos que ofrece a sus clientes, pero que no desea administrar en su sistema hasta que comience a venderlos. Los productos del catálogo no son artículos normales de tipo **No inventario**. Obtenga más información en [Trabajar con productos del catálogo](inventory-how-work-nonstock-items.md).  

> [!NOTE]  
> Si existen plantillas para distintos tipos de producto, aparece una página automáticamente cuando se crea una nueva ficha de producto en la que puede seleccionar una plantilla de producto apropiada. Si solo existe una plantilla de producto, las nuevas fichas de producto utilizan siempre esa plantilla.

En el siguiente procedimiento se explica cómo crear una ficha de producto desde cero. También puede crear nuevas fichas de producto copiando las existentes. Para obtener más información, consulte [Copiar productos existentes para crear productos nuevos](inventory-how-copy-items.md).  

<br />

> [!Video https://www.microsoft.com/videoplayer/embed/RE47eLx?rel=0]

## <a name="to-create-a-new-item-card"></a>Para crear una nueva ficha de producto.

[!INCLUDE[create_new_item](includes/create_new_item.md)]

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
4. Modifique o introduzca los códigos de dimensión que se aplican a nuevas fichas de producto creadas con la plantilla.
5. Cuando finalice la nueva plantilla de producto, haga clic en el botón **Aceptar**.

La plantilla de producto se agrega a la lista de plantillas de producto, de modo que puede usarla para crear nuevas fichas de producto.

### <a name="items-used-in-production-orders"></a>Productos utilizados en órdenes de producción

Si desea registrar productos que luego se utilicen en órdenes de producción, especifique el sistema de reposición como *Ord. prod.* en la ficha despegable **Reposición**. Para obtener más información, vea [Acerca de las órdenes de producción](production-about-production-orders.md).  

## <a name="to-set-up-multiple-vendors-for-an-item"></a>Para configurar varios proveedores para un producto

Si compra el mismo producto a varios proveedores, deberá introducir información acerca de cada proveedor del producto, como precios, plazo de entrega (días), descuentos, etc.  

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Productos**, y luego elija el enlace relacionado.  
2. Seleccione el elemento correspondiente y, a continuación, elija la acción **Editar**.  
3. Seleccione la acción **Proveedores**.  
4. Elija el campo **Nº proveedor** y, a continuación, seleccione el proveedor que desea configurar para el producto.  
5. Si lo desea, puede rellenar el resto de los campos.  
6. Repita los pasos 2 a 5 para cada proveedor al que desee comprar el producto.

Los proveedores aparecen después en la página **Tarifas de compra productos**, que se abre desde la tarjeta del producto, para poder fácilmente seleccionar un proveedor alternativo.

## <a name="set-up-item-substitutions"></a>Configurar sustituciones de productos

Puede configurar productos para que tengan sustitutos, como otros productos que se pueden utilizar en lugar del producto original.

### <a name="to-make-an-item-substitution"></a>Para identificar la sustitución de un producto

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Productos**, y luego elija el enlace relacionado.  
2. Busque el producto relevante y luego seleccione en **N.º producto** para abrir la ficha del producto.  
3. Elija la acción **Relacionada**, luego elija **Producto**, y, por último, **Sustituciones**, para abrir la página **Mov. sustitución producto**.  
4. Elija el campo **N.º sustitutivo** y seleccione el producto de sustitución en la lista.
5. Rellene o cambie otros campos de la página según sea necesario.

Cuando la cantidad solicitada sobrepasa la cantidad disponible en el inventario, aparece un mensaje para informarle de que existen productos sustitutos.

> [!NOTE]  
> Tenga en cuenta que las sustituciones de productos no harán que un producto sea reemplazado automáticamente por otro producto, por ejemplo, al crear un pedido de cliente o en una lista de materiales. En cambio, se le alertará sobre el hecho de que hay una sustitución disponible para usted.

## <a name="categories-attributes-and-variants"></a>Categorías, atributos y variantes

[!INCLUDE[inventory_variant](includes/inventory_variant.md)]

Obtenga más información sobre las variantes en [Administrar variantes de productos](inventory-item-variants.md).  

## <a name="delete-item-cards"></a>Eliminar fichas de producto

Si registra una transacción para un producto, no puede eliminar la ficha porque los movimientos pueden ser necesarias para la valoración de inventario o auditoría. Para eliminar fichas de producto con movimientos, póngase en contacto con el socio de Microsoft para hacerlo a través del código.  

## <a name="manage-inventory-in-warehouses"></a>Administrar el inventario en almacenes

Cuando registre un nuevo producto, ve campos relacionados con la gestión del almacén, especialmente en la ficha desplegable **Almacén**. Si su organización no utiliza las capacidades de gestión de almacenes de [!INCLUDE [prod_short](includes/prod_short.md)], entonces puede ignorar esos campos.  

Si su organización configura posteriormente la gestión de almacenes, le recomendamos que se asegure de que todos los productos tenga la información adecuada en los distintos campos. De esta manera, los procesos de almacén pueden ejecutarse como se esperaba. Esta información puede incluir campos como **Código de clase de almacén** o **Código de plantilla de ubicación**. Para obtener más información, consulte [Configuración de la administración de almacén](warehouse-setup-warehouse.md).  

## <a name="planning"></a>Planific.

Cuando su empresa utiliza los procesos de planificación de suministro en [!INCLUDE [prod_short](includes/prod_short.md)], debe completar los campos correspondientes en la ficha desplegable **Planificación**. Para obtener una introducción sobre el área de planificación, consulte [Detalles de diseño: conceptos centrales del sistema de planificación](design-details-central-concepts-of-the-planning-system.md).  

Para ver ejemplos de cómo puede utilizar los campos en la ficha desplegable **Planificación**, consulte [Prácticas recomendadas de configuración: parámetros de planificación](setup-best-practices-planning-parameters.md).  

## <a name="see-also"></a>Consulte también

[Grupos contables inventario](inventory-manage-inventory.md)  
[Configurar unidades de medida](inventory-how-setup-units-of-measure.md)  
[Administrar variantes del producto](inventory-item-variants.md)  
[Configuración de Informes de Intrastat](finance-how-setup-report-intrastat.md#other-intrastat-configurations)  
[Conciliar costes de inventario con la contabilidad](finance-how-to-post-inventory-costs-to-the-general-ledger.md)  
[Crear numeración](ui-create-number-series.md)  
[Configurar los grupos contables](finance-posting-groups.md)  
[Compras](purchasing-manage-purchasing.md)  
[Ccial](sales-manage-sales.md)  
[Sobre la funcionalidad de la planificación](production-about-planning-functionality.md)  
[Procedimientos recomendados de configuración: parámetros de la planificación](setup-best-practices-planning-parameters.md)  
[Procedimientos recomendados de configuración: planificación de suministros](setup-best-practices-supply-planning.md)  
[Detalles de diseño: Conceptos centrales del sistema de planificación](design-details-central-concepts-of-the-planning-system.md)  
[Detalles de diseño: Equilibrio de aprovisionamiento y demanda](design-details-balancing-demand-and-supply.md)  
[Detalles de diseño: Parámetros de la planificación](design-details-planning-parameters.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
