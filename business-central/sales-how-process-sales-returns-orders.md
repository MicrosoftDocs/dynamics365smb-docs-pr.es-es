---
title: Procesar devoluciones ventas
description: Describe cómo crear un pedido de devolución de venta para procesar una devolución, una cancelación o un reembolso de productos o servicios de los que ha recibido el pago.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: undo, credit memo, return, order
ms.search.form: 44, 134, 144, 6629, 6630, 6633, 6662, 9302, 9304, Report_6646
ms.date: 09/08/2021
ms.author: edupont
ms.openlocfilehash: 78b4c6412b24721b52a5c271c0e1c5a4c7ba8775
ms.sourcegitcommit: 3acadf94fa34ca57fc137cb2296e644fbabc1a60
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 09/19/2022
ms.locfileid: "9529115"
---
# <a name="process-sales-return-orders"></a>Procesar devoluciones ventas  

Si necesita más control del proceso de devolución de ventas, como documentos de almacén para el manejo de artículos o una mejor descripción al recibir productos de varios documentos de ventas con una sola devolución de ventas, puede crear órdenes de devolución de ventas. Una orden de devolución de ventas emite automáticamente la nota de crédito de ventas relacionada y otros documentos relacionados con la devolución, como una orden de venta de reemplazo, si es necesario.

Además de la original factura de venta registrada, puede liquidar el abono de venta o el pedido de devolución de ventas a otros documentos de venta, por ejemplo otra factura de venta registrada, porque el cliente también devuelve los productos entregados con dicha factura.

## <a name="create-a-sales-return-order-based-on-one-or-more-posted-sales-documents"></a>Crear un pedido de devolución de ventas basado en uno o más documentos de ventas publicados  

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Pedidos de venta** y, a continuación, elija el vínculo relacionado.
2. Seleccione la acción **Nuevo**.  
3. Rellen los campos de la ficha desplegable **General**.
4. En la ficha desplegable **Líneas**, rellene las líneas manualmente o copie la información de otros documentos para rellenar las líneas automáticamente:

    - Utilice la función **Revertir líneas documentos registrados:** para copiar una o más líneas de documentos registrados de uno o varios documentos registrados. Esta función revierte siempre exactamente los costes a partir de la línea de documento registrada. Esta función se describe en los pasos siguientes.    
    - Utilice la función **Copiar de documento** para copiar un documento existente al pedido de devolución. Utilice esta función para copiar el documento completo. Puede ser un documento registrado o un documento que todavía no se registró. Esta función sólo permite invertir el coste exacto cuando está seleccionada la casilla **Coste exacto devol. obligatorio** en la página **Configuración ventas y cobros**.  

5. Elija la acción **Proceso**, luego elija la acción **Revertir líneas documentos registrados**.
6. En la parte superior de la página **Líneas doc. ventas contabilizadas**, seleccione el campo **Mostrar sólo líneas reversibles** si solo desea ver las líneas con cantidades que aún no se han devuelto. Por ejemplo, si la cantidad de una factura de venta registrada ya se ha devuelto, puede que no desee devolver dicha cantidad en un nuevo documento de devolución de venta.

    > [!NOTE]  
    >  Este campo sólo funciona para envíos y líneas de facturas registrados, no para líneas de abonos o devoluciones registradas.

    En la parte izquierda de la página, se listan los diferentes tipos de documento y el número que aparece entre corchetes muestra el número de documentos que hay disponible del tipo en concreto.

7. En el campo **Filtro de tipo de documento**, seleccione el tipo de líneas de documento registrado que desea utilizar.  
8. Seleccione las líneas que desea copiar en el nuevo documento.  

    > [!NOTE]  
    >  Si utiliza Ctrl+E para seleccionar todas las líneas, se copiarán todas las líneas incluidas en el filtro definido, pero se ignorará el filtro **Mostrar sólo líneas reversibles**. Por ejemplo, imagine que ha filtrado las líneas en un número de documento determinado con dos líneas, una de las cuales ya se ha devuelto. Aunque el campo **Mostrar sólo líneas reversibles** esté seleccionado, si presiona Ctrl+E para copiar todas las líneas, se copiarán las dos líneas, en lugar de copiar solamente aquella que aún no se ha revertido.  

9. Seleccione **Aceptar** para copiar las líneas en el documento nuevo.  

    Tendrán lugar los siguientes procesos:  

    -   Para las líneas de documentos registrados del tipo **Producto**, se crea una nueva línea de documento que es una copia de la línea del documento registrado, con la cantidad que aún no se ha revertido. El campo **Liquid.-de mov. pdto** se rellena según corresponda con el número de movimiento de producto correspondiente a la línea del documento registrado.  

    -   Para las líneas de documentos registrados que no sean del tipo **Producto**, como los cargos de producto, se crea una nueva línea de documento que es una copia de la línea del documento registrado original.  

    -   Calcula el campo **Coste unitario (DL)** de la nueva línea a partir de los costes de los movimientos de producto correspondientes.  

    -   Si el documento copiado es un envío, una recepción, una recepción de devolución o un envío de devolución registrados, el precio de venta se calcula automáticamente a partir de la ficha del producto.  

    -   Si el documento copiado es una factura o un abono registrado, se copian el precio de venta, los descuentos de factura y los descuentos de línea de la línea del documento registrado.  

    -   Si la línea del documento registrado contiene líneas de seguimiento de productos, el programa rellena el campo **Liquid.-de mov. pdto** de dichas líneas de seguimiento con los números de movimiento de producto correspondientes de las líneas de seguimiento de productos registradas.  

     Cuando se copia desde una factura o abono registrados, la aplicación copia los descuentos de factura y de línea válidos en el momento de registrar ese documento desde la línea del documento registrado a la nueva línea de documento. Sin embargo, tenga en cuenta que si se activa la opción **Calc. dto. factura** en la página **Configuración de ventas y cobros**, el descuento en factura se volverá a calcular cuando registre una línea de documento nueva. Por lo tanto, el importe de la nueva línea puede ser distinto del importe de la línea del documento registrado, dependiendo del nuevo cálculo de descuento de factura.  

     > [!NOTE]  
     >  Si ya se ha revertido, vendido o consumido parte de la cantidad de la línea del documento registrado, se crea una línea sólo para la cantidad que queda en inventario o que no se ha devuelto. Si ya se ha revertido toda la cantidad de la línea del documento registrado, no se crea una nueva línea de documento.  
     >   
     >  Si el flujo de los artículos en el documento registrado coincide con el del nuevo documento, se crea una copia de la línea del documento registrado original en el nuevo documento. El campo **Liquid.-de mov. pdto** se ha rellenado porque, en este caso, la reversión de coste exacto no es posible. Por ejemplo, si utiliza la función **Revertir líneas documentos registrados** para obtener una línea de un abono de ventas registrado para un nuevo abono de ventas, sólo se copia la línea del abono registrado original en el nuevo abono.  

10. En la página **Pedido dev. venta**, en el campo **Cód. auditoría dev.** de cada línea, seleccione el motivo de la devolución.
11. Seleccione la acción **Registrar**.

## <a name="to-create-a-replacement-sales-order-from-a-sales-return-order"></a>Para crear un pedido de venta de reposición desde un pedido de devolución de venta
Quizás decida compensar a un cliente por un producto que le vendió cambiando el producto. Puede cambiarlo por el mismo producto o por otro distinto. Esta situación se puede dar, por ejemplo, si por error envió al cliente el producto equivocado,  

1. En la página **Pedido dev. venta** para un proceso de devolución activo, en una línea vacía, haga un movimiento negativo para el producto de reposición insertando un importe negativo en el campo **Cantidad** .  
2. Seleccione la acción **Mover líneas negativas**.
3. En la página **Mover líneas ventas negativas**, rellene los campos en una línea según sea necesario.
4. Elija el botón **Aceptar**. La línea negativa del producto de reposición se borra del pedido de devolución de ventas y se inserta en una nueva página **Pedido venta**. Para obtener más información, vea [Vender productos](sales-how-sell-products.md).

## <a name="to-create-return-related-documents-from-a-sales-return-order"></a>Crear documentos relativos a devoluciones a partir de un pedido de devolución de ventas
Puede crear automáticamente órdenes de venta de reposición, órdenes de devolución de compras y órdenes de compra de sustitución durante el proceso de devolución de ventas. Esto puede ser útil, por ejemplo, en aquellos casos en los que desee controlar productos con garantías proporcionadas por proveedores.

1. En la página **Pedido dev. venta** para un proceso de devolución activo, elija la acción **Crear docs. relacionados-dev.**
2. En el campo **Nº proveedor** , introduzca el número de un proveedor si desea crear documentos de proveedor automáticamente.
3. Si es necesario devolver un producto al proveedor, active la casilla de verificación **Crear devolución compra**.
4. Si es necesario pedir la devolución de un producto al proveedor, active la casilla de verificación **Crear pedido compra**.
5. Si es necesario crear un pedido de venta de reposición, active la casilla de verificación **Crear ped. venta**.

## <a name="to-create-a-restock-charge"></a>Para crear un cargo de reaprovisionamiento
Quizás decida cobrar a su cliente un cargo de reaprovisionamiento para cubrir los costes de manipulación física en la devolución de un producto. Esto podría suceder, por ejemplo, si el cliente pidió por error el producto equivocado o cambió de parecer una vez recibido el producto que le vendió.

Registre este precio aumentado como un cargo de producto en un abono o una devolución y asígnelo al envío registrado. A continuación se describe de un pedido de devolución de ventas, pero los mismos pasos se aplican a un abono de venta.

1. Abra la página **Pedido dev. venta** para un proceso de devolución activo.
2. En una línea nueva, en el campo **Tipo**, seleccione **Cargo (prod.)**.  
3. Rellene los campos según la líneas del coste de producto. Para obtener más información, consulte [Utilizar los cargos de producto a cuenta para los costes comerciales adicionales](payables-how-assign-item-charges.md).  

Cuando registre el pedido de devolución de ventas, se añadirá el cargo de reaprovisionamiento al importe del movimiento de ventas correspondiente. De este modo podrá mantener la precisión de la valoración del inventario.  

## <a name="see-related-microsoft-training"></a>Consultar la [formación de Microsoft](/training/paths/return-items-dynamics-365-business-central/) relacionada

## <a name="see-also"></a>Consulte también

[Ccial](sales-manage-sales.md)  
[Configuración de ventas](sales-setup-sales.md)  
[Administrar pagos](payables-manage-payables.md)  
[Enviar documentos por correo electrónico](ui-how-send-documents-email.md)  
[Procesamiento de devoluciones de compra o cancelaciones](purchasing-how-process-purchase-returns-cancellations.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
