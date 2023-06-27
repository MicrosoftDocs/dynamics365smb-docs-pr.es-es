---
title: Asignar cargos de producto a ventas y compras (contiene vídeo)
description: 'Asigne cargos por productos cuando necesite productos de inventario para generar costes adicionales, como flete y manejo físico.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'transportation, added cost, landed cost'
ms.search.form: '5709, 5800, 5805, 5814'
ms.date: 06/22/2021
ms.author: edupont
---
# <a name="use-item-charges-to-account-for-additional-trade-costs"></a><a name="use-item-charges-to-account-for-additional-trade-costs"></a>Usar los cargos de producto a cuenta para los costes comerciales adicionales

Para asegurarse de la valoración correcta, sus productos de inventario deben cargar costes adicionales, tales como fletes, manipulación física, seguros y transporte en los que incurra al comprar o vender artículos. Para las compras, el coste en destino de un producto comprado se compone del precio de compra del proveedor y de otros cargos de producto directos que se pueden asignar a albaranes o envíos devueltos determinados. Para las compras, conocer el coste de envío de los productos vendidos es tan importante para la empresa como conocer el coste de los productos comprados.

Además de registrar el coste añadido en su valor de inventario, puede usar cargos de productos para las siguientes tareas:

* Identificar el coste de descarga de un producto para tomar decisiones exactas sobre cómo optimizar la red de distribución.
* Desglosar el coste unitario o el precio de venta de un producto con fines de análisis.
* Incluya las deducciones de compras en el coste unitario y las deducciones de ventas en el precio de venta.

Antes de poder asignar cargos de productos, debe configurar números de cargo de productos para los diferentes tipos de cargos de productos. Los números incluyen en qué cuentas contables se contabilizan los costes relacionados con las ventas, las compras y los ajustes de inventario. Un número de cargo de producto contiene una combinación de grupo contable de producto, código de grupo de impuesto, grupo de registro IVA producto y cargos de producto. Cuando introduce el número de cargo del producto en un documento de compra o venta, se recupera la cuenta contable. La cuenta que se recupera se selecciona en función de la configuración del número de cargo del producto y la información del documento.

Para los documentos de compra y de venta, puede asignar un coste de producto de las siguientes maneras:

* En el documento que enumera los productos a los que se refiere el cargo de producto. Típicamente, se suele hacer para los documentos que aún no se han contabilizado completamente.
* en una factura independiente asociando el cargo de producto a envíos o albaranes registrados en los que figuran los productos a los que se refiere el cargo de producto.

> [!NOTE]  
> Puede asignar cargos de artículos a pedidos, facturas y abonos para ventas y compras. Los procedimientos siguientes describen cómo gestionar los cargos de producto en una factura de compra. Los pasos son parecidos a los de los documentos de compra y venta.

## <a name="example"></a><a name="example"></a>Ejemplo:

Este vídeo muestra cómo gestionar un coste de envío adicional como parte de los costes de existencias.
<br><br>  
> [!Video https://www.microsoft.com/videoplayer/embed/RE4b0SB?rel=0]

## <a name="to-set-up-item-charge-numbers"></a><a name="to-set-up-item-charge-numbers"></a>Configurar números de coste de producto

Los números de cargo de producto sirven para diferenciar los distintos tipos de cargos de productos.

1. Elija el icono ![Bombilla que abre la característica Dígame](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Cargos de producto**, y luego elija el enlace relacionado.
2. En la página **Cargos producto**, seleccione la acción **Nuevo** para crear una línea nueva.
3. Rellene los campos según sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-assign-an-item-charge-directly-to-the-purchase-invoice-for-the-item"></a><a name="to-assign-an-item-charge-directly-to-the-purchase-invoice-for-the-item"></a>Asignar un coste de producto directamente en la factura de compra del producto

Si conoce el cargo de un producto en el momento en que registra la factura de compra, siga este procedimiento.

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Facturas compra** y luego elija el enlace relacionado.
2. Crea una nueva factura de compra. Para obtener más información, consulte [Registrar compras](purchasing-how-record-purchases.md).
3. Asegúrese de que la factura de compra tiene una o más líneas del tipo Producto.
4. En una línea nueva, en el campo **Tipo**, seleccione **Cargo (prod.)**.
5. En el campo **Cantidad**, introduzca las unidades del cargo de producto que se le ha facturado.
6. En el campo **Precio compra**, introduzca el importe del cargo de producto.
7. Rellene los campos restantes según sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    Realice los siguientes pasos para efectuar la asignación actual. Hasta que el cargo del producto esté completamente asignado, el valor en el campo **Cdad. para asignar** aparece de color rojo.
8. En la ficha **Líneas**, seleccione la acción **Asignación cargo prod.**.

    La página **Asignación cargos prod.** abre una línea por cada línea del tipo Producto en la factura de compra. Para asignar el cargo de producto a una o más líneas de factura, puede utilizar una función que lo asigne y distribuya automáticamente o puede rellenar manualmente el campo **Cdad. para asignar**. Las siguientes tareas describen cómo utilizar la funcionalidad de la asignación de cargos de producto el menú.

9. En la página **Asignación cargos prod.**, seleccione la acción **Sugerir asignación cargo prod.**
10. Si hay más de una línea de factura del tipo Producto, elija una de las cuatro opciones de distribución.  

El cargo del producto está completamente asignado, el valor de la factura de compra en el campo **Cdad. para asignar** es cero.

El cargo de producto está asignado a la factura de compra. Al registrar la recepción de la factura de compra, los valores de inventario de los elementos se actualizan con el coste del cargo del producto.  

## <a name="to-assign-an-item-charge-from-a-separate-invoice-to-the-purchase-invoice-for-the-item"></a><a name="to-assign-an-item-charge-from-a-separate-invoice-to-the-purchase-invoice-for-the-item"></a>Asignar un coste de producto de una factura independiente a la factura de compra del producto

Si recibió una factura por el cargo de producto después de haber publicado el recibo de compra original, siga este procedimiento.

1. Repita los pasos del 1 al 8 en [Asignar un coste de producto directamente en la factura de compra del producto](payables-how-assign-item-charges.md#to-assign-an-item-charge-directly-to-the-purchase-invoice-for-the-item).
2. En la página **Asignación cargos prod.**, elija la acción **Traer líns. albarán**.
3. En la página **Líns. recep. compra**, seleccione el albarán de compra registrado para el producto al que desea asignar el cargo de producto y, a continuación, elija el botón **Aceptar**.
4. Seleccione la acción **Sugerir asignación cargo prod.**

El cargo de producto de la factura de compra independiente se asigna al producto en el recibo de compra registrado, y se actualiza el valor de inventario del artículo con el coste del cargo de producto.

## <a name="handle-item-charges-for-partial-receipts"></a><a name="handle-item-charges-for-partial-receipts"></a>Manejar cargos de productos para recibos parciales

Exploremos un ejemplo de cómo manejar los cargos de productos para un recibo parcial.

Tiene una orden de compra con tres líneas:

* Dos líneas son para productos.
* Una línea captura los cargos de productos asignados a los productos por importe.

Cuando se entregan los productos, descubre que falta uno de ellos, por lo que no puede marcar esa línea como recibida. Puede recibir y contabilizar la factura de compra solo para el segundo producto y ocuparse del producto que falta más tarde.

Para manejar el coste del producto para el recibo parcial, en la página **Asignación de cargo del producto**, introduzca **0** en el campo **Cantidad a manejar** de la línea del producto que falta. Luego, copie el valor del campo **Cantidad de cargo del producto a manejar** al campo **Cantidad a facturar** en las líneas de la orden de compra.

Cuando esté listo para manejar el producto que faltaba, actualice el campo **Cantidad a manejar** y contabilice el pedido.

## <a name="see-related-microsoft-training"></a><a name="see-related-microsoft-training"></a>Consultar la [formación de Microsoft](/training/modules/post-purchase-item-charges-dynamics-365-business-central/) relacionada

## <a name="see-also"></a><a name="see-also"></a>Consulte también .

[Administrar pagos](payables-manage-payables.md)  
[Registrar compras](purchasing-how-record-purchases.md)  
[Facturar ventas](sales-how-invoice-sales.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
