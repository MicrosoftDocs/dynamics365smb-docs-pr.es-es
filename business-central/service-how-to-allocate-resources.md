---
title: Asignar recursos | Documentos de Microsoft
description: Puede cambiar el importe anual del contrato de servicio u oferta de contrato para corregir el importe que se facturará anualmente.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 04/01/2021
ms.author: bholtorf
---

# Asignar recursos
El principal elemento de la gestión del servicio son las personas que lo prestan. Puede configurar [!INCLUDE[prod_short](includes/prod_short.md)] para asignar el personal adecuado a los proyectos correspondientes. Las asignaciones se pueden basar en zonas de servicio donde se encuentran las personas o donde tiene lugar el servicio. Además, puede agrupar los recursos al responder a solicitudes de servicio. Para obtener más información, vea [Asignación de recursos](service-how-setup-resource-allocation.md).

Puede asignar recursos, por ejemplo, para técnicos, mediante **Panel despacho**, o desde una orden de servicio. Puede utilizar la disponibilidad de recursos y asignarlos para ejecutar las tareas de servicio de las órdenes u ofertas.

Puede asignar el mismo recurso, por ejemplo, un técnico, o grupo de recursos a todos los productos de un pedido de servicio. Se crean movimientos de asignación para los otros productos de servicio del pedido que tengan el mismo número de recurso y fecha de asignación que la línea asignada. Las horas asignadas son las horas asignadas divididas por el número de productos de servicio del pedido. El campo **Estado** se establece automáticamente como **Activo** para todos los movimientos creados.

## Para ver un resumen de las ofertas o los pedidos de servicio  
A menudo puede que necesite ver la lista de pedidos de servicio u ofertas de servicio que cumplen determinados requisitos para poder realizar acciones específicas con ellas una a una. Por ejemplo, puede que tenga que asignar recursos a pedidos de servicio que pertenecen a un cliente específico.  

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Panel despacho** y luego elija el enlace relacionado.  
2. En el campo **Filtro documento**, elija el tipo de los documentos que desea ver.
3. Para obtener una lista de documentos que contienen tareas de servicio asignadas a un determinado recurso o grupo de recursos, rellene los campos **Filtro recurso** y **Filtro grupo recurso** y presione <kbd>Entrar</kbd>.  
4. Para obtener una lista de documentos con una fecha de respuesta determinada o con fechas de respuesta en un determinado periodo, rellene el campo **Filtro fecha respuesta** y seleccione <kbd>Entrar</kbd>.  
5. Para obtener una lista de documentos con un estado de documento o asignación determinado, rellene el campo **Filtro asignación o Filtro estado** y seleccione <kbd>Entrar</kbd>.  
6. Para obtener una lista de documentos que pertenecen a una zona, cliente o contrato determinado, rellene el campo **Filtro contrato o Filtro cliente o Filtro zona** y seleccione <kbd>Entrar</kbd>.  
7. Seleccione una línea que corresponda a un pedido de servicio o una oferta de servicio y seleccione la acción **Mostrar documento**.  

    Se abrirá la página **Pedido de servicio** u **Oferta servicio** y podrá trabajar con el documento. Para volver a la página **Panel despacho**, elija **Aceptar**.

## Para asignar un recurso mediante disponibilidad de grupo de recursos o grupos de recursos    
1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Panel despacho** y elija el enlace relacionado.  
2. Elija la orden de servicio y, a continuación, elija la acción **Asignaciones recurso**.  
3. Elija el movimiento que contenga la tarea de servicio a la que desea asignar un recurso.  
4. Seleccione la acción **Disponibilidad recurso** o **Disponibilidad fam. recurso**.  
5. En la página **Disponibilidad recurso (Servicio)**, elija **Mostrar matriz**.  
6. Elija un recurso para asignar. Puede basar la selección en si el recurso está cualificado para realizar la tarea, si está ubicado en la zona del cliente y/o si es un recurso preferido por el cliente.  
7. Especifique una fecha en la que el recurso dispone de horas suficientes para la tarea y que sea cercana a la fecha de respuesta del pedido de servicio.  
8. En el campo **Cadad. a asignar**, introduzca el número de horas durante las que desee asignar el recurso a la tarea de servicio.  
9. Elija la acción **Asignar** para asignar el recurso seleccionado a la fecha seleccionada.  

     El campo de **Estado** se establece automáticamente en **Activo**.  

 Repita estos pasos para cada fecha en la que desee asignar el recurso a la tarea de servicio.  

> [!NOTE]  
>  En el caso de un producto de servicio de un pedido de servicio, sólo pueden existir movimientos de asignación **Activos** con un solo recurso o grupo de recursos a la vez.  

## Para asignar un recurso mediante un pedido de servicio  
Después de crear y rellenar un pedido de servicio o una oferta de servicio, puede asignar recursos (por ejemplo, técnicos) para realizar tareas de servicio registradas como líneas de producto de servicio en el documento.  

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Pedidos de servicio** y luego elija el enlace relacionado.  
2. Elija la orden de servicio y, a continuación, **Editar**.  
3. Elija la línea de producto de servicio correspondiente a la tarea de servicio a la que desea asignar un recurso.  
4. Elija **Asignaciones recurso**.
5. En la página **Asignaciones recurso**, elija un movimiento de asignación no activo con la tarea de servicio a la cual desee asignar el recurso. Si el movimiento de asignación no existe, puede crear uno nuevo seleccionando **Nuevo**.  
7. Especifique la tarea de servicio rellenando el campo de **Nº prod. servicio** en la misma línea.  
8. En el campo **Nº recurso**, elija el recurso. Si el recurso es miembro de un grupo de recursos, se introduce automáticamente el número del grupo de recursos en **Nº grupo recurso**. .  
9. Rellene los campos **Fecha asignación** y **Horas asignadas**. El campo **Estado** se establece como **Activo**. Esto significa que el recurso está asignado a la tarea de servicio.  
10. Opcionalmente, asigne el recurso a todos los productos, elija **Asignar a todos prods. serv.**

> [!NOTE]  
>  En el caso de un producto de servicio de un pedido de servicio, sólo pueden existir movimientos de asignación con el estado Activos con un solo recurso o grupo de recursos a la vez.

## Para reasignar recursos en un pedido de servicio  
Puede reasignar recursos directamente desde un pedido u oferta de servicio cuando está trabajando con ellos. El movimiento original seguirá existiendo, pero su estado se actualizará de la siguiente forma:  

* Si se inició el servicio mientras la asignación estaba **Activa**, es decir, si el estado de reparación del producto de servicio del movimiento se cambió a **En proceso**, el estado de asignación cambia de **Reasignación necesaria** a **Terminado**.  
* Si no se inició el servicio mientras la asignación estaba **Activa**, el estado de asignación cambia de **Reasignación necesaria** a **Cancelado**.  
* Si reasigna un pedido de servicio convertido de una oferta, el estado de los movimientos de asignación registrados para la oferta siempre cambia a **Terminado** cuando se reasignan los productos de servicio del pedido de servicio.  

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Pedidos de servicio** y luego elija el enlace relacionado.  
2. Abra el pedido servicio que corresponda.  
3. Seleccione la línea de producto de servicio correspondiente a la tarea de servicio a la que desea asignar un recurso y, a continuación, elija la acción **Asignaciones recurso**.  
4. En la página **Asignaciones recurso**, seleccione un movimiento de asignación con la tarea de servicio que a la cual desea reasignar el recurso. En el campo **Nº recurso**, seleccione el recurso correspondiente. Esta acción sobrescribe el número de recurso que anteriormente figuraba en el campo.  
5. Seleccione <kbd>Entrar</kbd>. Se abre un cuadro de diálogo en el que se le pregunta si desea reasignar el movimiento. Rellene el campo **Cód. auditoría** si es necesario y elija el botón **Sí** para confirmar la reasignación.  
6. Rellene los campos **Fecha asignación** y **Horas asignadas**. Ahora el movimiento contiene el nuevo recurso y su estado es **Activo**.

## Para reasignar un recurso con el panel despacho  
Si el recurso asignado a una tarea de servicio no puede realizar el trabajo, la tarea de servicio debe reasignarse. Normalmente, se reasignan recursos a una tarea de servicio mediante el **Panel despacho**.  

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Panel despacho** y luego elija el enlace relacionado.  
2. En el campo **Filtro asignación**, seleccione **Reasignación necesaria**. La página **Panel despacho** ahora muestra la lista de los pedidos de servicio que incluyen tareas de servicio que deben reasignarse.  
3. Seleccione la orden de servicio relevante y, a continuación, elija la acción **Asignaciones recurso**. Se abrirá la página **Asignaciones recurso**.  
4. Seleccione el movimiento de asignación con la tarea de servicio que desea reasignar a un recurso.  
5. En el campo **Nº recurso**, seleccione el recurso correspondiente. Se sobrescribe el número de recurso que anteriormente figuraba en el campo.  
6. Seleccione <kbd>Entrar</kbd>. Se abrirá el cuadro de diálogo **Razones reasignación de entrada** para solicitar información sobre si desea reasignar este movimiento. Rellene el campo **Cód. auditoría** si es necesario y elija el botón **Sí** para confirmar la reasignación.  
7.  Rellene los campos **Fecha asignación** y **Horas asignadas**. Ahora el movimiento contiene el nuevo recurso y su estado es **Activo**.  

    > [!NOTE]  
    >  El movimiento anterior todavía existe, pero su estado se actualiza de la siguiente forma:  
    >   
    >  * Si se inició el servicio mientras la asignación estaba **Activa**, es decir, si el estado de reparación del producto de servicio del movimiento se cambió a **En proceso**, el estado de asignación cambia de **Reasignación necesaria** a **Terminado**.  
    > * Si no se inició el servicio mientras la asignación estaba **Activa**, el estado de asignación cambia de **Reasignación necesaria** a **Cancelado**.  
    > * Si reasigna un pedido de servicio convertido de una oferta, el estado de los movimientos de asignación registrados para la oferta siempre cambia a **Terminado** cuando se reasignan los productos de servicio del pedido de servicio.  

## Para registrar horas de recursos  
Al trabajar en productos de servicio de pedidos de servicio, deberá registrar las horas de recursos empleadas en el servicio. El siguiente procedimiento muestra cómo registrar las horas de recursos en la página **Hoja trabajo producto servicio**.  

Puede utilizar el mismo procedimiento para registrar las horas en la página **Líneas servicio**, que podrá abrir desde la página Pedido de servicio. Abra la ficha de servicio correspondiente y elija la acción **Líneas servicio**.  

Si el mismo recurso trabaja en todos los productos de servicio del pedido de servicio, puede registrar el total de horas de recursos para un solo producto de servicio y, a continuación, dividir la línea de recurso para asignar las horas de recursos a los otros productos de servicio.

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Tareas de servicio** y luego elija el enlace relacionado.
2. Elija la línea que contiene el producto de servicio en cuestión y, a continuación, elija la acción **Hoja de producto**.  
3. Rellene los campos según sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## Para asignar recursos a todos los productos de servicio de un pedido
Si el mismo recurso, por ejemplo, un técnico, trabaja en todos los productos de servicio del pedido de servicio, puede registrar el total de horas de recursos para un solo producto de servicio y, a continuación, dividir la línea de recurso para asignar las horas de recursos a las líneas de recurso de los otros productos de servicio.  

El siguiente procedimiento muestra cómo dividir líneas de recurso en la página **Líneas factura servicio**.  

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Pedidos de servicio** y luego elija el enlace relacionado.  
2. Abra el pedido servicio que corresponda.  
3. En la ficha desplegable Líneas, haga clic en **Acciones**, y elija la acción **Líneas servicio**. Se abrirá la página **Líneas servicio**.  
4. Seleccione la línea de recurso que desea dividir. Se divide el contenido del campo **Cantidad** entre todos los productos de servicio del pedido.  
5. Elija la acción **Dividir línea recurso**. Seleccione **Sí** para confirmar.  

    Se crearán líneas de recurso para los otros productos de servicio del pedido que tengan el mismo número de recurso que la línea dividida. La cantidad es la cantidad de la línea dividida entre el número de productos de servicio del pedido.  

## Para cancelar una asignación  
Puede cancelar las asignaciones de recursos para las tareas de servicio sin reasignar las tareas.  

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Panel despacho** y luego elija el enlace relacionado.  
2. Elija la orden de servicio y, a continuación, elija la acción **Asignaciones recurso**.  
3. Seleccione el movimiento de asignación que contiene la tarea de servicio para la que desea cancelar la asignación.  
4. Seleccione la acción **Cancelar asignaciones**.  
5. En el campo **Código de motivo**, seleccione el código de motivo que corresponda.  
6. Elija **Sí** para confirmar la cancelación.  

    > [!NOTE]  
    > En el campo **Estado**, se selecciona automáticamente la opción **Reasignación necesaria**. Si el estado de reparación del producto de servicio del movimiento es **Inicial**, el estado de reparación cambia a **Remitido**, es decir, no se ha iniciado ningún servicio. Si el estado de reparación es **En proceso**, éste cambia a **Parcialmente servido**, es decir, se ha realizado parte del servicio.

## Consulte también
[Configurar asignación de recursos](service-how-setup-resource-allocation.md)  
[Estado de asignación y estado de reparación](service-allocation-status-and-repair-status.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]