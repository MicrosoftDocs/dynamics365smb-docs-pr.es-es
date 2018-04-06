---
title: "Cómo crear pedidos de venta abiertos | Documentos de Microsoft"
description: "Utilice los pedidos abiertos cuando un cliente ha acordado comprar grandes cantidades que se van a entregar en varios envíos más pequeños durante un periodo de tiempo determinado."
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/08/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 89db93227222d79e535f2d18400330aa30566f2f
ms.contentlocale: es-es
ms.lasthandoff: 03/22/2018

---
# <a name="work-with-blanket-sales-orders"></a>Trabajar con pedidos de venta abiertos
Los pedidos abiertos de venta constituyen un marco de trabajo para establecer un acuerdo a largo plazo con un cliente.

Normalmente, un pedido abierto se utiliza cuando un cliente se ha comprometido a comprar grandes cantidades que se van a entregar en varios envíos más pequeños durante un periodo de tiempo determinado. A menudo, los pedidos abiertos sólo incluyen un producto con fechas de entrega predeterminadas. El motivo principal para utilizar un pedido abierto en lugar de un pedido de venta es que las cantidades especificadas en un pedido abierto no afectan a la disponibilidad de los productos y, así, se puede utilizar como hoja de trabajo con fines de supervisión, previsión y planificación.

En un pedido abierto, cada envío independiente se puede definir como una línea de pedido que, posteriormente, puede transformarse en un pedido de venta en el momento del envío.

Un ejemplo en el que se podría utilizar un pedido abierto de venta sería un caso en el que un cliente realiza un pedido de 1000 unidades de un producto y desea que los productos se le envíen en grupos de 250 unidades cada semana durante el mes siguiente.

> [!NOTE]
> Los pedidos de compra abiertos funcionan de manera similar a los pedidos de venta abiertos. Esta documentación no cubre los pedidos de compra abiertos.

## <a name="to-create-a-blanket-sales-order"></a>Para crear un pedido abierto de venta  
1. Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Pedidos de venta abiertos** y, a continuación, seleccione el vínculo relacionado.  
2. Seleccione la acción **Nuevo**.  
3. Rellene los campos según sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4.  Deje el campo **Fecha pedido** en blanco. Cuando se crean pedidos de venta independientes a partir del pedido abierto, la fecha que se definirá para el pedido de venta será igual que la fecha de trabajo real.
5. Cree líneas independientes para cada envío en la ficha desplegable **Líneas**. Por ejemplo, si el cliente desea 1000 unidades repartidas equitativamente en cuatro semanas, debe insertar cuatro líneas distintas con 250 unidades cada una.   

## <a name="to-create-a-sales-order-from-a-blanket-sales-order"></a>Para crear un pedido de venta a partir de un pedido abierto de venta  

1.  Para crear un pedido de cualquiera de las líneas del pedido abierto de ensamblado, elimine la cantidad del campo **Cantidad a enviar** en todas las líneas que no desee enviar en este momento.  
2.  Cuando esté preparado para crear pedidos, haga clic en la acción **Convertir en pedido** y, a continuación, haga clic en **Sí**. Aparecerá un mensaje para informarle de que se ha asignado un número de pedido al pedido abierto. Observe que no se ha eliminado el pedido abierto.  
3.  Elija el botón **Aceptar**.  
4.  Para ver los resultados de los pasos anteriores, elija la acción **Línea**, seleccione **Líneas no registradas** y, finalmente, haga clic en **Pedidos**.  
5.  Seleccione el pedido de venta correspondiente en la ventana **Líns. venta**, elija la línea **Acción** y, finalmente, elija la acción **Mostrar documento**.  

Lo siguiente se aplica a los pedidos de venta después de que se hayan creado a partir de los pedidos abiertos de venta:  

- Una vez que el pedido abierto se convierte en pedido de venta, el segundo contiene todas las líneas del primero. Las líneas en las que se ha eliminado la cantidad del campo **Cantidad a enviar** aparecen, pero el campo **Cantidad** está en blanco. Puede conservar, editar o eliminar las líneas.  
- Debe recordar que la cantidad de la línea del pedido de venta no debe superar la cantidad de la línea asociada del pedido abierto. De lo contrario, no se podrá registrar el pedido de venta.  
- Cuando el pedido de venta se registra como enviado y/o facturado, se actualizan los campos **Cantidad enviada** y **Cantidad facturada** del pedido abierto relacionado.  
- El número de línea y el número de pedido abierto se registran como propiedades de las líneas de venta cuando se crean a partir de un pedido abierto.  
- Si los pedidos de venta no se crean directamente a partir del pedido abierto pero se relacionan con éste, se puede establecer un vínculo entre un pedido de venta y uno abierto especificando el número del pedido abierto asociado en el campo **Nº pedido abierto** de la línea del pedido de venta.  
- Después de que el pedido de venta se haya creado para la cantidad total de una línea de pedido abierto, ningún otro pedido de venta se puede crear para la misma línea. Los usuarios no pueden introducir una cantidad en el campo **Cantidad a enviar**. Sin embargo, si es necesario agregar cantidades adicionales a un pedido abierto, puede incrementarse el valor del campo **Cantidad** y crear, a continuación, nuevos pedidos.  
- El pedido abierto de venta facturado se conserva en el sistema hasta que se elimina, ya sea eliminando pedidos abiertos individuales o ejecutando el proceso **Eliminar pedidos abiertos venta facturados**.  
- Si un cliente también está registrado como contacto en el área de la aplicación Marketing y ha especificado un código de plantilla de interacción para el pedido abierto de venta en la ventana **Configuración de marketing**, al seleccionar **Imprimir** para imprimir el pedido abierto de venta se registrará una interacción en la tabla Movimiento de registro de interacción.

## <a name="to-view-the-status-of-a-blanket-purchase-order"></a>Para ver el estado de un pedido abierto de compra  
Puede ver el estado de los pedidos de abiertos de venta en la ventana **Estad. pedido abierto compras**. Esto puede ser importante cuando empiece a facturar el pedido que se crea a partir del pedido abierto de compra.  

1.  Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Pedidos de venta abiertos** y, a continuación, seleccione el vínculo relacionado.  
2.  Seleccione un pedido abierto de compra, y después seleccione **Estadísticas** .  
3.  En la ficha desplegable **General** de la ventana **Estad. pedido abierto compras**, puede ver información resumida sobre el pedido completo basada en la cantidad total de los distintos **campos Cantidad** de las líneas del pedido abierto de compra.  

    - En la ficha desplegable **Facturación**, puede ver información resumida basada en la cantidad total de los campos **Cdad. a facturar** de las líneas del pedido abierto de compra.  
    - En la ficha desplegable **Envío**, puede ver información resumida basada en la cantidad total de los campos **Cantidad a recibir** de las líneas del pedido abierto de compra.  
    - En la ficha desplegable **Prepago**, puede ver información resumida sobre las importes de prepago.  
    - La ficha desplegable **Proveedor** contiene información básica acerca del proveedor.    

## <a name="to-view-unposted-and-posted-blanket-sales-order-lines"></a>Visualización de líneas de pedido abierto de venta registradas y no registradas   
El vínculo entre el pedido abierto de venta y el pedido de venta de origen, y cualquier otro documento de venta, se mantiene después de registrar como lista de líneas de factura de pedido de venta registradas y sin registrar.  

1. Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Pedidos de venta abiertos** y, a continuación, seleccione el vínculo relacionado.
2. Abra el pedido abierto de venta que desea ver.
3. Para ver los movimientos no registrados, seleccione la acción **Línea** y, a continuación, la acción **Líneas no registradas**. Elija una de las siguientes opciones.  

    <table>
    <tr>
    <th>Opción</th>
    <th>Description</th>
    </tr>
    <tr>
    <td>**Pedidos**</td>
    <td>Especifica los pedidos abiertos asociados a la línea seleccionada.</td>
    </tr>
    <tr>
    <td>**Facturas**</td>
    <td>Especifica las facturas abiertas asociadas a la línea seleccionada. Las facturas abiertas se asocian manualmente a un pedido abierto especificando el número de dicho pedido en la línea de la factura de venta.</td>
    </tr>
    <tr>
    <td>**Devoluciones**</td>
    <td>Especifica las devoluciones abiertas asociadas a la línea seleccionada.</td>
    </tr>
    <tr>
    <td>**Abonos**</td>
    <td>Especifica los abonos abiertos asociados a la línea seleccionada.</td>
    </tr>
    </table>
4.Para ver los movimientos registrados, seleccione la línea en cuestión y elija la acción **Línea** y, a continuación, la acción **Líneas registradas**. Elija una de las siguientes opciones.  

    <table>
    <tr>
    <th>Opción</th>
    <th>Description</th>
    </tr>
    <tr>
    <td>**Envíos**</td>
    <td>Los envíos registrados asociados a la línea seleccionada.</td>
    </tr>
    <tr>
    <td>**Facturas**</td>
    <td>Las facturas registradas asociadas a la línea seleccionada.</td>
    </tr>
    <tr>
    <td>**Recep. devolución**</td>
    <td>Las recepciones de devolución registradas asociadas a la línea seleccionada.</td>
    </tr>
    <tr>
    <td>**Abonos**</td>
    <td>Los abonos registrados asociados a la línea seleccionada.</td>
    </tr>
    </table>
5.En la ventana **Líneas de venta**, seleccione la acción **Mostrar documento** para ver la entrada.

## <a name="see-also"></a>Consulte también
[Ccial](sales-manage-sales.md)  
[Configuración de ventas](sales-setup-sales.md)  
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

