---
title: Inicio rápido de adquisiciones (contiene vídeo)
description: Aprenda a completar los primeros campos críticos sobre proveedores en Business Central para que pueda comenzar a comprar productos y servicios.
author: jill-kotel-andersson
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: quickstart
ms.search.form: 26, 27, 50, 56
ms.date: 09/29/2021
ms.author: edupont
ms.openlocfilehash: 58476145830438b85e70c03958b2bf997640e2c7
ms.sourcegitcommit: e008b3d7003c256475d6c606e5f7c9866a6bbb72
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 01/10/2022
ms.locfileid: "7953114"
---
# <a name="procurement-quick-start"></a>Inicio rápido de adquisiciones

Para poder comprar productos y servicios, primero debe configurar proveedores. Una vez hecho esto, puede comenzar a registrar órdenes de compra y recibir facturas.  

## <a name="set-up-vendors"></a>Configurar proveedores

El siguiente vídeo le muestra cómo configurar un proveedor en [!INCLUDE[prod_short](includes/prod_short.md)].

<br><br>  

> [!Video https://www.microsoft.com/videoplayer/embed/RE3PZtd?rel=0]

### <a name="set-up-a-new-vendor"></a>Configurar un proveedor nuevo

[!INCLUDE[create_new_vendor](includes/create_new_vendor.md)]

Para obtener más información y detalles adicionales que puede hacer cuando registra proveedores, consulte [Registrar nuevos proveedores](purchasing-how-register-new-vendors.md).  

## <a name="create-new-purchase-orders"></a>Crear nuevos pedidos de compra

Cuando compra algo a un proveedor, tiene dos opciones. La primera, y la más simple, es crear una factura de compra. Sin embargo, debe usar pedidos de compra si el proceso de compra requiere que registre recibos parciales de una cantidad del pedido, por ejemplo, porque el proveedor no disponía de la cantidad total.

El siguiente vídeo le muestra cómo crear un pedido de compra en [!INCLUDE[prod_short](includes/prod_short.md)].

<br><br>

> [!Video https://www.microsoft.com/videoplayer/embed/RE4b3tt?rel=0]

### <a name="to-create-a-purchase-order"></a>Para crear un pedido de compra  

1. Elija el icono ![Bombilla que abre la función Dígame 1.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Pedidos de compra** y, a continuación, elija el vínculo relacionado.  

2. En la página **Pedidos de compra**, seleccione la acción **Nuevo** para crear un nuevo pedido de compra.

3. En el campo **Nombre proveedor**, escriba el nombre de un proveedor existente.

    Otros campos en el **Cab. compra** se rellenarán con la información estándar del proveedor seleccionado.  

4. Rellene los campos en la página **Pedido de compra** según sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    Ya puede empezar a rellenar las líneas del pedido de compra con los productos o recursos que ha comprado del proveedor.

5. En la ficha desplegable **Líneas**, en el campo **Nº producto**, especifique el número de un producto o un servicio de inventario.

6. En el campo **Cantidad**, introduzca el número de productos que se van a comprar.

    El campo **Importe línea** se actualiza para mostrar el valor del campo **Coste unit. directo** multiplicado por el valor del campo **Cantidad**.

7. En el campo **Importe descuento pedido**, especifique un importe que se debe descontar del valor que aparece en el campo **Total IVA incl.** en la parte inferior del pedido.

8. Cuando reciba los productos o servicios comprados, seleccione **Registrar**.

Para obtener más información y detalles adicionales que puede hacer al crear un pedido de compra, consulte [Compras](purchasing-manage-purchasing.md).  

## <a name="create-a-purchase-invoice"></a>Crear una factura de compra  

Cree una factura de compra para registrar el coste de las compras y para realizar el seguimiento de los pagos. Crear una factura de compra es similar a crear un pedido de compra.

### <a name="how-to-create-and-post-a-purchase-invoice"></a>Cómo crear y registrar una factura de compra  

1. Elija el icono ![Bombilla que abre la función Dígame 3.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Facturas compra** y luego elija el enlace relacionado.  
2. En la página **Factura de compra**, seleccione la acción **Nuevo** para crear una nueva factura de compra.
3. En el campo **Proveedor**, escriba el nombre de un proveedor existente.

    Otros campos de la página **Factura de compra** se rellenarán con la información estándar del proveedor seleccionado.

4. Rellene los campos en la página **Factura de compra** según sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    Ya puede empezar a rellenar las líneas de la factura de compra con los productos o recursos que ha comprado del proveedor.

5. En la ficha desplegable **Líneas**, en el campo **Nº producto**, especifique el número de un producto o un servicio de inventario.
6. En el campo **Cantidad**, introduzca el número de productos que se van a comprar.

    El campo **Importe línea** se actualiza para mostrar el valor del campo **Coste unit. directo** multiplicado por el valor del campo **Cantidad**.

7. En el campo **Importe descuento factura**, especifique un importe que se debe descontar del valor que aparece en el campo **Total IVA incl.** en la parte inferior de la factura.

8. Cuando reciba los productos o servicios comprados, seleccione **Registrar**.

La compra ahora se refleja en el inventario, en los movimientos de recursos y en los registros financieros, y se activa el pago al proveedor. La factura de compra se elimina de la lista de facturas de compra y se reemplaza con un nuevo documento de la lista de facturas de compra registradas.  

Para obtener más información y detalles adicionales que puede hacer al crear una factura de compra, consulte [Registrar compras con facturas de compra](purchasing-how-record-purchases.md).

## <a name="see-also"></a>Consulte también

[Inicio rápido de Business Central](quick-start-business-central.md)  
[Resumen de compras](Purchasing-manage-purchasing.md)  
[Registrar compras con facturas de compra](purchasing-how-record-purchases.md)  
