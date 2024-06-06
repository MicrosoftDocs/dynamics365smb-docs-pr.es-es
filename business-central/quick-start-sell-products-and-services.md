---
title: Inicio rápido de ventas (contiene vídeo)
description: Aprenda a completar los primeros campos críticos sobre productos y clientes en Business Central para que pueda comenzar sus procesos de ventas.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: quickstart
ms.date: 09/29/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
---

# Inicio rápido de ventas

Para poder vender productos y servicios, primero debe configurar productos y clientes. Una vez hecho esto, puede comenzar a registrar pedidos de ventas y enviar facturas.

## Configurar productos para vender

Este vídeo muestra cómo configurar un producto para vender en [!INCLUDE[prod_short](includes/prod_short.md)].

<br>

> [!Video https://www.microsoft.com/en-us/videoplayer/embed/RE47eLx?rel=0]

### Configurar un producto nuevo

[!INCLUDE[create_new_item](includes/create_new_item.md)]

Para obtener más información y detalles adicionales que puede hacer cuando configura productos, consulte [Registrar nuevos productos](inventory-how-register-new-items.md).  

## Configurar clientes

Este vídeo muestra cómo configurar un nuevo cliente en [!INCLUDE[prod_short](includes/prod_short.md)].  

<br>

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE3PZsM]

### Configurar un cliente nuevo

[!INCLUDE[create_new_customer](includes/create_new_customer.md)]

Para obtener más información y detalles adicionales que puede hacer cuando configura cientes, consulte [Registrar nuevos clientes](sales-how-register-new-customers.md)

## Crear un pedido de ventas  

Cuando vende algo a un cliente, tiene dos opciones. La primera, y la más simple, es crear una factura de venta. Sin embargo, si su proceso de ventas es más complejo, por ejemplo, si tiene situaciones en las que solo envía partes de una cantidad de pedido, utilice un pedido de venta.

### Para crear un pedido de ventas  

1. Elija el icono ![Bombilla que abre la función Dígame 10.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Pedidos de venta** y, a continuación, elija el vínculo relacionado.
2. Seleccione **Nuevo** para crear una entrada nueva.
3. En el campo **Cliente**, escriba el nombre de un cliente existente.

    Otros campos de la página **Pedido de venta** se rellenarán con la información estándar del cliente seleccionado.  

4. Rellene los campos en la página **Pedido venta** según sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

5. En la ficha desplegable **Líneas** del campo **Tipo**, seleccione qué tipo de producto, cargo o transacción registrará para el cliente en la línea de venta.

6. En el campo **N.º**, introduzca el número de un producto de inventario o servicio.

7. En el campo **Cantidad**, escriba el número de productos que se van a vender.

8. En el campo **% Descuento línea**, especifique un porcentaje si desea conceder al cliente un descuento para el producto.

9. Para agregar un comentario acerca de la línea de pedido que el cliente puede ver en el pedido de venta impreso, escriba un comentario en el campo **Descripción** en una línea vacía.

10. Repita los pasos 5 a 9 para cada producto que desee vender al cliente.

11. Para enviar únicamente una parte de la cantidad del pedido, escriba dicha cantidad en el campo **Cantidad a enviar**. El calor se copia en el campo **Cantidad a facturar**.

12. Para facturar únicamente una parte de la cantidad enviada, escriba dicha cantidad en el campo **Cantidad a facturar**. La cantidad debe ser inferior al valor del campo **Cantidad a enviar**.

13. Cuando las líneas del pedido de venta ya estén completas, seleccione la acción **Registrar y enviar**.

Para obtener más información y detalles adicionales que puede hacer al crear pedidos de venta de cliente, consulte [Vender productos con un pedido de venta de cliente](sales-how-sell-products.md).  

## Crear una factura de venta

Cuando crea y registra una factura de venta, no solo crea el documento de factura que envía al cliente, sino que también crea los movimientos de cantidad y valor relacionados en [!INCLUDE[prod_short](includes/prod_short.md)].

### Para crear y registrar una factura de venta  

1. Elija el icono ![Bombilla que abre la función Dígame 20.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Facturas venta** y luego elija el enlace relacionado.  

2. Seleccione **Nuevo** para crear una entrada nueva.

3. En el campo **Cliente**, escriba el nombre de un cliente existente.

4. Rellene los campos en la página **Factura venta** según sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

5. En la ficha desplegable **Líneas** del campo **Tipo**, seleccione qué tipo de producto, cargo o transacción registrará para el cliente en la línea de venta.

6. En el campo **N.º**, seleccione un registro para registrar según el valor del campo **Tipo**.

7. En el campo **Cantidad**, especifique cuántas unidades de producto, cargo o transacción registrará la línea para el cliente.  

8. Si desea ofrecer un descuento, introduzca un porcentaje en el campo **% Descuento línea**. El valor del campo **Importe de línea** se actualiza según corresponde.  

9. Repita los pasos 5 a 8 para cada producto o cargo que desee facturar al cliente.  

10. En el campo **Importe descuento factura**, especifique un importe que se debe descontar del valor que aparece en el campo **Total impuesto incl.** en la parte inferior de la factura.

11. Cuando las líneas de la factura de venta ya estén completas, seleccione la acción **Registrar y enviar**.  

Para obtener más información y detalles adicionales que puede hacer al crear una factura de venta de cliente, consulte [Facturar ventas](sales-how-invoice-sales.md)

## Consulte también

[Inicio rápido de Business Central](quick-start-business-central.md)  
[Información general de ventas](sales-manage-sales.md)  
[Vender productos con un pedido de venta de cliente](sales-how-sell-products.md)  
[Facturar ventas](sales-how-invoice-sales.md)  
