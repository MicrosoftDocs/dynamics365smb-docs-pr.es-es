---
title: Crear una factura de compra a partir de una factura de venta para comprar productos para una venta | Documentos de Microsoft
description: A partir de una factura de venta, para comprar productos, puede crear una factura de compra de un proveedor.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: supply planning, sales demand, replenish
ms.date: 05/16/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 2d7eb238395a0b1060668996fbbc3e13d9dd8a94
ms.contentlocale: es-es
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-purchase-items-for-a-sale"></a>Comprar productos para una venta
A partir de pedidos y facturas de venta, puede utilizar funciones para crear rápidamente los documentos de compra de las cantidades de productos que faltan que sean necesarias para la venta. Puede utilizar dos funciones distintas dependiendo del tipo de documento.
|Función|Description|
|--------|-----------|
|**Crear pedidos de compra**|A partir de un pedido de compra, esta función crea un pedido de compra para cada proveedor de los productos que hay en el pedido de venta. Puede modificar la cantidad de compra antes de crear los pedidos de compra. Solo se sugieren las cantidades de venta no disponibles.
|**Crear factura de compra**|A partir de un pedido de venta y desde una factura de venta, esta función crea una factura de compra de un proveedor seleccionado para todas las líneas o las líneas seleccionadas del documento de venta. Se sugiere la cantidad de venta completa.|

## <a name="to-create-one-or-more-purchase-orders-from-a-sales-order"></a>Para crear uno o más pedidos de compra a partir de un pedido de venta
Para crear un pedido de compra para cada cantidad de producto no disponible en el pedido de venta, utilice la función **Crear pedidos de compra**. 

> [!NOTE]  
>   Esta funcionalidad requiere que la experiencia esté definida en **Suite**. Para obtener más información, consulte [Personalizar la experiencia de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-experiences.md).

1. En la página Inicio, elija el mosaico **Pedidos de venta en curso**.
2. Abra un pedido de venta para el que desea comprar productos.
3. Elija la acción **Crear pedidos de compra**.

    Se abre la ventana **Crear pedidos de compra** mostrando una línea para cada producto en el pedido de venta. Se muestran de forma predeterminada las líneas para las cantidades de venta totalmente disponibles y las cantidades de venta no disponibles (atenuadas). Puede elegir la acción **Mostrar no disponibles** para ver solo las líneas de las cantidades de venta no disponibles.

    El campo **Cantidad de compra** contiene la cantidad de venta no disponible de forma predeterminada.
4. Para comprar una cantidad distinta de la cantidad de venta no disponible, edite el valor del campo **Cantidad de compra**.

    > [!NOTE]  
>   También puede cambiar el campo **Cantidad de compra** en las líneas atenuadas aunque representen las cantidades de venta totalmente disponibles.
5. Elija el botón **Aceptar**. 
    
    Se crea un pedido de compra para cada proveedor de productos del pedido de venta, incluido cualquier cambio de la cantidad que ha realizado en la ventana **Crear pedidos de compra**.
7. Procese el pedido o los pedidos de compra, por ejemplo, mediante la modificación o la adición de las líneas del pedido de compra. Para obtener más información, consulte [Procedimiento: Registrar compras](purchasing-how-record-purchases.md).


## <a name="to-create-a-purchase-invoice-from-a-sales-order-or-sales-invoice"></a>Para crear una factura de compra a partir de un pedido o pedidos de venta
Para crear una sola factura de compra para una o varias líneas de un documento de ventas seleccionando primero el proveedor al que se compra, utilice la función **Crear factura de compra**. 

> [!NOTE]  
>   Esta función crea una factura de compra para la cantidad exacta de productos en el documento de venta seleccionado. Para cambiar la cantidad de compra, debe modificar la factura de compra después de que se cree.  

1. En la página Inicio, elija el mosaico **Facturas de ventas en curso**.
2. Abra una factura de venta para la que desea comprar productos.
3. Seleccione una o varias líneas de factura de venta que desee usar en la factura de compra. Para usar todas las líneas de factura de venta, selecciónelas todas o no seleccione ninguna.
4. Elija la acción **Crear factura de compra**.
5. Seleccione o **Todas las líneas** o **Líneas seleccionadas** y, a continuación, elija el botón **Aceptar**.  
6. En la lista de proveedores que aparece, seleccione el proveedor al que desea comprar todos los productos y, a continuación, elija el botón **Aceptar**.

    Se crea una factura de compra que contiene una, varias o todas las líneas en la factura de venta.
7. Procese la factura de compra, por ejemplo, mediante la modificación o la adición de las líneas de la factura de compra. Para obtener más información, consulte [Procedimiento: Registrar compras](purchasing-how-record-purchases.md).

## <a name="see-also"></a>Consulte también
[Compras](purchasing-manage-purchasing.md)  
[Registro de compras](purchasing-how-record-purchases.md)  
[Facturación de ventas](sales-how-invoice-sales.md)  
[Registro de proveedores nuevos](purchasing-how-register-new-vendors.md)  
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

