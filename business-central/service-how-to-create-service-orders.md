---
title: Cómo crear pedidos de servicio
description: 'Conozca las diferentes tareas involucradas en la creación de órdenes de servicio en Business Central, como crear una nueva orden de servicio u órdenes basadas en un contrato de servicio.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 06/23/2021
ms.author: edupont
---
# <a name="create-service-orders" />Crear pedidos de servicio
Puede utilizar la página **Pedido servicio** para crear documentos en los que se introduce información acerca de un servicio, como reparación y mantenimiento, de productos de servicio a solicitud del cliente.  

Cuando cree un pedido de servicio, solo tendrá que rellenar algunos campos. Algunos campos son opcionales y muchos se rellenarán automáticamente cuando rellene los campos correspondientes.  

## <a name="to-create-a-service-order" />Para crear un pedido de servicio
1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Pedidos de servicio** y luego elija el enlace relacionado.  
2. Cree un pedido de servicio nuevo.  
3. En el campo **N.º**, introduzca un número para el pedido de servicio.  

     Alternativamente, si ha configurado números de serie para pedidos de servicio en la página **Configuración de gestión de servicios**, también puede seleccionar <kbd>Entrar</kbd> para seleccionar el siguiente número de pedido de servicio disponible.  

4. En el campo **Nº cliente**, seleccione el cliente pertinente de la lista. Los campos correspondientes al cliente se rellenan con información de la tabla **Cliente**.  

5. Dependiendo de la configuración de la ficha desplegable **Campos obligatorios** de la página **Configuración de gestión se servicios**, puede que necesite rellenar el campo **Tipo pedido servicio** y el campo **Cód. vendedor**.  
6. Si lo desea, puede rellenar el resto de los campos.  
7. Registre las líneas de producto de servicio.  

## <a name="to-create-a-service-order-from-a-contract" />Para crear un pedido de servicio a partir de un contrato
Puede basarse en contratos de servicio para crear automáticamente ofertas de servicio de mantenimiento de productos de servicio.  

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Crear pedidos serv. contrato** y, a continuación, elija el enlace relacionado.  
2. Defina los filtros que desea aplicar en la ficha desplegable **Cabecera contrato servicio**.  
3. En la ficha desplegable **Opciones**, rellene los campos **Fecha inicial** y **Fecha final** con la fecha inicial y final del periodo para el que desee crear pedidos de servicio de contratos. El proceso crea ofertas de servicio que incluyen productos de servicio de contratos de servicio con las siguientes fechas de servicio planificadas dentro de este periodo.  

    > [!NOTE]  
    >  Existe un límite en el número de días que puede utilizar como rango de fechas cada vez que se ejecuta el trabajo por lotes. Este límite se establece en el campo **Días máx. ped. serv. contrato** de la página **Configuración de gestión de servicios**.  

4. En el campo **Acción**, seleccione **Crear pedido servicio**.  
    > [!NOTE]  
    >  No podrá crear pedidos con varios productos de servicio, si configura el campo **Una línea prod. serv./pedido** en la página **Configuración de gestión de servicios**. 

## <a name="to-convert-a-service-quote-to-a-service-order" />Para convertir una oferta de servicio en un pedido de servicio
Una vez que el cliente ha aceptado la oferta de servicio, puede convertirla en un pedido de servicio. La oferta se elimina y se configura un nuevo pedido de servicio con la misma descripción que la oferta de servicio. Se vuelven a calcular la fecha y el tiempo de respuesta del pedido de servicio y el estado se establece como **Pendiente**. El estado de reparación de los productos de servicio del pedido se cambian a **Inicial**.  

[!INCLUDE[prod_short](includes/prod_short.md)] busca movimientos de asignación para todos los productos de servicio de la oferta de servicio cuyo estado sea **Activo**. Si encuentra los movimientos de asignación, se actualiza su estado de asignación a **Reasignación necesaria**. Cuando se reasignan los productos de servicio del pedido de servicio, se actualiza el estado de los movimientos de asignación registrados para la oferta a **Terminado**.   

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Ofertas de contrato de servicio** y luego elija el enlace relacionado.  
2. Elija la oferta de servicio relevante que desee convertir en pedido de servicio.  
3. Seleccione la acción **Crear pedido**.  

## <a name="to-check-item-availability-for-one-or-more-orders" />Comprobación de la disponibilidad de los artículos para uno o varios pedidos de servicio
Es posible comprobar si el artículo necesario para cubrir un pedido está en existencias y, en caso contrario, averiguar cuándo lo estará. Además, si es posible efectuar la reserva de un artículo, podrá reservarlo para asegurarse de que esté disponible para el uso. Puede activar la disponibilidad de un pedido determinado o de todos los pedidos.  

1.  Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Panel despacho** y luego elija el enlace relacionado.  
2. Realice una de las siguientes acciones:  

    * Para un pedido determinado, selecciónelo y, a continuación, elija la acción **Panorama de demanda**.  
    * En todos los pedidos, elija **Mostrar documento**. Se abrirá la página **Pedido servicio**.  

3. En la página **Panorama de demanda**, expanda el grupo de productos, y consulte la información acerca de la disponibilidad del producto. Por ejemplo, puede ver cuántos productos están en el inventario. También puede ver cuando un artículo estará disponible si se trata de un pedido pendiente, es decir, cuando el tipo de origen = compra o si se ha reservado.

## <a name="to-reserve-an-item-for-a-service-order" />Reservar un artículo para un pedido de servicio
Si necesita asegurarse de que un producto está disponible para el pedido de servicio, puede reservarlo.

1. En el cuadro **Buscar**, escriba **Pedidos de servicio** y, a continuación, elija el vínculo relacionado.  
2. Elija la orden de servicio y, a continuación, **Editar**.  
3. Elija **Acciones**, elija **Pedido** y, a continuación, elija **Líneas servicio**.  
4. En la página **Líneas servicio**, seleccione el producto para reservar y, a continuación, elija la acción **Reserva**.  
5. En la página **Reservas**, elija **Reservar desde línea actual**.

## <a name="to-insert-lines-based-on-standard-service-codes" />Para insertar líneas basadas en el servicio estándar
Si ha configurado códigos de servicio estándar y los ha asignado a grupos de productos de servicio, puede insertar las líneas estándar vinculadas a los códigos de servicio estándar en documentos de servicio. Para obtener más información, consulte [Configurar códigos de servicio estándar](service-how-setup-service-coding.md).   

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Pedidos de servicio** y luego elija el enlace relacionado.  
2. Cree un pedido de servicio nuevo.  
3. Rellene los campos según sea necesario.  
4. Rellene las líneas de producto de servicio con la información requerida.  
5. Elija la línea con el artículo de servicio para el que desea crear las líneas de servicio y elija **Traer cód. servicio estánd**. Se abrirá la página **Códs. grupo prod. serv. est.** con los códigos estándar para el grupo de artículo de servicio especificado en la línea.  
6. Elija el código adecuado y haga clic en **Aceptar** para insertar líneas de servicio estándar.  

> [!NOTE]  
>  Si el campo **Cód. grupo prod. servicio** de la línea de artículo de servicio del documento está en blanco, quiere decir que el artículo de servicio no pertenece a ningún grupo de artículo de servicio. En este caso, la página **Códs. grupo prod. serv. est.** contendrá una lista de todos los códigos de servicio estándar. Debe seleccionar las líneas de la lista para insertar líneas de servicio estándar en el documento. También puede seleccionar de la lista de códigos de servicio estándar asignados a un grupo específico de artículos de servicio. Para ver la lista, seleccione el código correspondiente en el campo **Cód. grupo prod. servicio** de la página **Códs. grupo prod. serv. est.**  

## <a name="to-register-internal-or-public-comments" />Para registrar comentarios internos o públicos
Puede agregar comentarios que se imprimirán en los pedidos y ofertas de servicio para proporcionar información adicional. Puede agregar hasta 80 caracteres, incluso espacios. Si necesita escribir más texto, elija otra línea. Para registrar un comentario, elija una línea y, a continuación, elija la acción **Comentarios**.  

## <a name="to-delete-invoiced-service-orders" />Para eliminar pedidos de servicio facturados
Los pedidos se suelen eliminar automáticamente después de haberse facturado en su totalidad. Cuando se registra una factura, se crea un movimiento correspondiente en la página **Facts. ventas (servicio) regis.** El documento registrado se puede ver en la página **Fact. ventas (servicio) regis.**  

Sin embargo, los pedidos de servicio no se eliminarán de forma automática si la cantidad total de dicho pedido no se ha registrado desde el pedido de servicio en sí, sino desde la página **Factura servicio**. En este caso, puede que tenga que eliminar los pedidos facturados que no se hayan eliminado. Para ello, ejecute el proceso **Eliminar ped. servicio facturados**.  

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Eliminar pedidos de servicio facturados** y, a continuación, elija el enlace relacionado. Se abre la página de solicitud del proceso **Eliminar pedidos de servicio facturados**.  
2. Para seleccionar los pedidos que se van a eliminar, puede definir filtros en los campos **Nº**, **Nº cliente** y **Factura Nº cliente**. .  
3. Elija **Aceptar**.  


## <a name="see-also" />Consulte también
[Registro de servicio](service-service-posting.md)  
[Registrar un ped. serv.](service-how-to-post-service-orders.md)  
[Configurar la gestión de servicios](service-setup-service.md)  
[Trabajar en tareas de servicio](service-how-to-work-on-service-tasks.md)  
[Asignar recursos](service-how-to-allocate-resources.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
