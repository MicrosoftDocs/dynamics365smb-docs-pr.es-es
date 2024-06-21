---
title: Comprar productos para una venta
description: 'A partir de una factura de venta, para comprar productos, puede crear una factura de compra de un proveedor.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'supply planning, sales demand, replenish'
ms.search.form: '50, 51, 56, 9308'
ms.date: 03/14/2024
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# Compra de artículos para una venta mediante la creación de facturas de compra

A partir de pedidos y facturas de venta, puede utilizar funciones para crear rápidamente los documentos de compra de las cantidades de productos que faltan que sean necesarias para la venta. Puede utilizar dos funciones distintas dependiendo del tipo de documento.

> [!Note]
> Esta funcionalidad sirve para reponer artículos de ventas en su propio inventario. Para comprar productos para la entrega directa de su proveedor a su cliente, debe crear un envío directo. Para obtener más información, vea [Realizar envíos directos](sales-how-drop-shipment.md).   

|Función|Description|
|--------|-----------|
|**Crear pedidos de compra**|A partir de un pedido de compra, esta función crea un pedido de compra para cada proveedor de los productos que hay en el pedido de venta. Puede modificar la cantidad de compra antes de crear los pedidos de compra. Solo se sugieren las cantidades de venta no disponibles.
|**Crear factura de compra**|A partir de un pedido de venta y desde una factura de venta, esta función crea una factura de compra de un proveedor seleccionado para todas las líneas o las líneas seleccionadas del documento de venta. Se sugiere la cantidad de venta completa.|

## Para crear uno o más pedidos de compra a partir de un pedido de venta
Para crear un pedido de compra para cada cantidad de producto no disponible en el pedido de venta, utilice la función **Crear pedidos de compra**.

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Pedidos de venta** y, a continuación, elija el vínculo relacionado.
2. Abra un pedido de venta para el que desea comprar productos.
3. Elija la acción **Crear pedidos de compra**.

    Se abre la página **Crear pedidos de compra** mostrando una línea para cada producto en el pedido de venta. Se muestran de forma predeterminada las líneas para las cantidades de venta totalmente disponibles y las cantidades de venta no disponibles (atenuadas). Puede elegir la acción **Mostrar no disponibles** para ver solo las líneas de las cantidades de venta no disponibles.

    El campo **Cantidad de compra** contiene la cantidad de venta no disponible de forma predeterminada.
4. Para comprar una cantidad distinta de la cantidad de venta no disponible, edite el valor del campo **Cantidad de compra**.

    > [!NOTE]  
    >   También puede cambiar el campo **Cantidad de compra** en las líneas atenuadas aunque representen las cantidades de venta totalmente disponibles.
5. Elija el botón **Aceptar**.

    Se crea un pedido de compra para cada proveedor de productos del pedido de venta, incluido cualquier cambio de la cantidad que ha realizado en la página **Crear pedidos de compra**.
7. Procese el pedido o los pedidos de compra, por ejemplo, mediante la modificación o la adición de las líneas del pedido de compra. Para obtener más información, consulte [Registrar compras](purchasing-how-record-purchases.md).


## Para crear una factura de compra a partir de un pedido o pedidos de venta
Para crear una sola factura de compra para una o varias líneas de un documento de ventas seleccionando primero el proveedor al que se compra, utilice la función **Crear factura de compra**.

> [!NOTE]  
>   Esta función crea una factura de compra para la cantidad exacta de productos en el documento de venta seleccionado. Para cambiar la cantidad de compra, debe modificar la factura de compra después de que se cree.  

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Pedidos de venta** y, a continuación, elija el vínculo relacionado.
2. Abra una factura de venta para la que desea comprar productos.
3. Seleccione una o varias líneas de factura de venta que desee usar en la factura de compra. Para usar todas las líneas de factura de venta, selecciónelas todas o no seleccione ninguna.
4. Elija la acción **Crear factura de compra**.
5. Seleccione o **Todas las líneas** o **Líneas seleccionadas** y, a continuación, elija el botón **Aceptar**.  
6. En la lista de proveedores que aparece, seleccione el proveedor al que desea comprar todos los productos y, a continuación, elija el botón **Aceptar**.

    Se crea una factura de compra que contiene una, más de una o todas las líneas en la factura de venta.
7. Procese la factura de compra, por ejemplo, mediante la modificación o la adición de las líneas de la factura de compra. Para obtener más información, consulte [Registrar compras](purchasing-how-record-purchases.md).

## Consulte también
[Compras](purchasing-manage-purchasing.md)  
[Registrar compras](purchasing-how-record-purchases.md)  
[Facturar ventas](sales-how-invoice-sales.md)  
[Registrar un nuevo proveedor](purchasing-how-register-new-vendors.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]