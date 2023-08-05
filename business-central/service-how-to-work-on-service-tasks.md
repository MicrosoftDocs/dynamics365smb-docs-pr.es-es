---
title: Cómo trabajar en tareas de servicio
description: Este tema cubre las diferentes formas de trabajar en tareas de servicio. La página Tareas de servicio proporciona una visión general de todos los productos de servicio que requieren atención.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 06/25/2021
ms.author: edupont
---
# Trabajar en tareas de servicio
Una vez que haya creado un pedido u oferta de servicio, registrado líneas de producto de servicio y asignado recursos a los productos de servicio del pedido u oferta, podrá empezar a reparar y mantener los productos de servicio.  

[!INCLUDE[prod_short](includes/prod_short.md)] dispone de la página **Tareas de servicio**, que proporciona una visión general de todos los productos de servicio que requieren atención. Puede considerarlo como su tablero de mandos de servicio, en el que puede ver los pedidos pendientes, buscar y registrar piezas de repuesto y mantener actualizado el inventario.  

Para realizar un seguimiento de los cambios y obtener una visión gráfica de sus negocios de servicios, utilice las herramientas estadísticas de [!INCLUDE[prod_short](includes/prod_short.md)] para obtener gráficos y análisis rápidos que se generan automáticamente.  

## Para trabajar en una tarea de servicio  
1. Elija el icono ![Bombilla que abre la función Dígame 1.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Tareas de servicio** y luego elija el enlace relacionado.
2. Si desea una lista de tareas de servicio asignadas a un determinado recurso o grupo de recursos, rellene el campo **Filtro recurso** o **Filtro grupo recurso** y seleccione <kbd>Entrar</kbd>.  
3. Si desea obtener una lista de tareas de servicio con una fecha de respuesta determinada o con fechas de respuesta en un determinado periodo de tiempo, rellene el campo **Filtro fecha respuesta** y seleccione <kbd>Entrar</kbd>.  
4. Si desea una lista de tareas de servicio asignadas a un determinado estado de reparación o estado de asignación, rellene el campo **Filtro estado asignación** o **Filtro cód. estado reparación** y seleccione <kbd>Entrar</kbd>.  
5. Seleccione la tarea de servicio en la que desea trabajar. Elija la acción **Hoja de producto**. Se abrirá la página **Hoja trabajo prod. serv**.  
6. Registre textos estándar, componentes, recursos, horas y costes utilizando las opciones correspondientes del campo **Tipo**: \<Blank\>, **Producto**, **Recurso** y **Coste**.  
7. En el campo **Estado reparación**, seleccione el estado adecuado.  

   > [!NOTE]  
   >  Rellene el campo **Estado reparación** con el estado **Terminado** o **Parcialmente servido** si ha finalizado el servicio del producto de servicio u otro recurso continúa el servicio. El estado **Terminado** o **Reasignación necesaria** se especificará automáticamente para el movimiento de asignación de este producto de servicio.  

## Para registrar operaciones de servicio  
Al realizar un servicio de un pedido de servicio, puede registrar los detalles del mismo especificando los productos utilizados, los costes adquiridos y el tiempo invertido. Los datos especificados se almacenan en la página **Hoja trabajo prod. serv.** Puede actualizar los datos siempre que sea necesario.

1. Elija el icono ![Bombilla que abre la función Dígame 2.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Pedidos de servicio** y luego elija el enlace relacionado.  
2. Abra el pedido de servicio para registrar el servicio y elija la línea de producto.  
3. Elija la acción **Hoja prod. servicio**.  
4. En las líneas, especifique los productos utilizados, los costes adquiridos y el tiempo invertido en el servicio.  

   > [!NOTE]  
   >  También puede registrar el servicio directamente en las líneas de servicio vinculadas al pedido de servicio.  

## Para registrar componentes  
Al trabajar en productos de servicio de pedidos de servicio, puede que necesite utilizar componentes para llevar a cabo el servicio. El siguiente procedimiento muestra cómo registrar los componentes utilizados en la página **Hoja trabajo producto servicio**.  

1. Elija el icono ![Bombilla que abre la función Dígame 3.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Tareas de servicio** y luego elija el enlace relacionado.
2. Elija la línea que contiene el producto de servicio en cuestión y, a continuación, elija la acción **Hoja trabajo prod.**.  
3. Introduzca una nueva línea de servicio.  
4. En el campo **Tipo**, elija **Producto**.  
5. En el campo **N.º**, elija la pieza de repuesto relevante.  
6. En el campo **Cantidad**, introduzca la cantidad de productos que desea utilizar.  

 Puede utilizar un procedimiento similar para registrar las piezas de repuesto en la página **Líneas servicio**, que podrá abrir desde la página **Pedido de servicio**.  

## Registrar piezas de repuesto desde un pedido de servicio  
1. Elija el icono ![Bombilla que abre la función Dígame 4.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Pedidos de servicio** y luego elija el enlace relacionado.  
2. Abra el pedido de servicio para el que desee registrar piezas de repuesto.  
3. Elija la línea que contenga el producto de servicio correspondiente. Elija **Acciones**, elija **Pedido** y, a continuación, elija **Líneas servicio**.  
4. introduzca una nueva línea de servicio.  

## Para cambiar un producto de servicio o un componente de producto de servicio  
Cuando se lleva a cabo el servicio de un producto de servicio que incluye componentes, es posible que necesite reemplazar un componente defectuoso con otro nuevo. Cada vez que introduce un componente para un producto de servicio con componentes, se le permite escoger si desea reponer el componente o crear otro nuevo. El nuevo producto no está registrado como componente del producto de servicio hasta que se registra la línea de servicio o el pedido de servicio.

1. Elija el icono ![Bombilla que abre la función Dígame 5.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Tareas de servicio** y luego elija el enlace relacionado.
2. Elija la línea que contiene el producto de servicio y, a continuación, elija la acción **Hoja trabajo prod.**.  
3. Introduzca una nueva línea de servicio.  
4. En el campo **Tipo**, elija **Producto**.  
5. En el campo **N.º**, elija el componente que se debe reemplazar.  
6. Seleccione <kbd>Entrar</kbd>. Se muestra un cuadro de diálogo con tres campos de opciones: **Reponer componente**, **Nuevo componente** e **Ignorar**. La siguiente tabla describe las opciones.  

    |Opción | Description|  
    |----------------------------------|---------------------------------------|  
    |**Reponer componente**|Cambia el estado del componente que está reemplazando a "no activo" y se muestra en la lista de componentes repuestos del producto de servicio.|  
    |**Nuevo componente**|Introduce el nuevo componente en la lista de componentes del producto de servicio.|  
    |**Ignorar**|No modifica la lista de componentes del producto de servicio.|  

7. Elija **Reponer componente**.  
8. Seleccione el componente que se debe reemplazar y, a continuación, seleccione **Aceptar**.  

## Para cambiar la hora de respuesta en líneas de productos de servicio  
Al registrar una línea de producto de servicio en una oferta o pedido de servicio, dependiendo de si el elemento de servicio está en un contrato de servicio se introduce automáticamente la hora de respuesta en horas y se calcula la fecha y la hora de respuesta. Puede cambiar el tiempo de respuesta en horas y la fecha y tiempo de respuesta en caso necesario.  

1. Elija el icono ![Bombilla que abre la función Dígame 6.](media/ui-search/search_small.png "Dígame qué desea hacer") , especifique **Pedidos de servicio** u **Ofertas contrato servicio** y, a continuación, elija el vínculo relacionado.  
2. Elija el pedido de servicio u oferta para abrir la ficha de pedido.  
3. En la línea de producto de vínculo en la que desea cambiar la hora de respuesta, en el campo **Tiempo respuesta (Horas)** o en los campos **Fecha respuesta** y **Hora respuesta**, introduzca las nuevas horas de respuesta o la fecha y la hora de respuesta deseada.  

## Para registrar códigos de defecto/resolución  
Después de reparar un producto de servicio, puede registrar tanto el código de defecto como el de resolución si selecciona una combinación de las relaciones de códigos de defecto/resolución existentes. Los códigos de defecto y resolución se mostrarán en los campos correspondientes de la página **Hoja de producto de servicio**. También puede registrar los códigos directamente en esta página.  

1. Elija el icono ![Bombilla que abre la función Dígame 7.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Tareas de servicio** y luego elija el enlace relacionado.
2. Elija la línea que contiene el producto de servicio en cuestión y, a continuación, elija la acción **Hoja trabajo prod.**.  
3. En la página **Hoja prod. servicio**, elija **Relac. códs. defecto/resol.**. Se abrirá la página **Relación códs. defecto/resol.**  

  >  [!NOTE]
  >  Los filtros se definen para las relaciones mostradas en la página al copiar el grupo de producto de servicio y los códigos de defecto de la página **Hoja trabajo prod. serv.**  

4. Rellene la línea. Seleccione la combinación correcta de códigos de defecto y resolución y, a continuación, selección **Aceptar** para copiarla al producto de servicio. Si no se encuentra una combinación adecuada, puede crear una combinación nueva en la página.  

## Consulte también  
[Configurar informes de defectos](service-how-setup-fault-reporting.md)
[Estado de asignación y estado de reparación](service-allocation-status-and-repair-status.md)  
[Registro de servicio](service-service-posting.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]