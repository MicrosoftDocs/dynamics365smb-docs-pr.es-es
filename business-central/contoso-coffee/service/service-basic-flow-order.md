---
title: Tutorial de pedidos de servicio para productos de servicio
description: Este artículo lo guía a través de varios procesos principales que involucran artículos y órdenes de servicio.
author: andreipa
ms.author: andreipa
ms.reviewer: andreipa
ms.topic: how-to
ms.date: 05/31/2023
ms.custom: bap-template
ms.service: dynamics-365-business-central
---

# Tutorial de pedidos de servicio para productos de servicio

Este tutorial demuestra varios procesos principales:

- Crear una Orden de Servicio ad hoc y registrar la reparación del Artículo
- Proporcionar un artículo en préstamo al cliente por un tiempo de reparación
- Registrar y facturar el pedido de servicio
    
## Crear un pedido de servicio

### Escenario  

Charles, el gerente de servicio, crea un pedido de servicio para un escenario de reparación y presta un Préstamo al cliente para el momento de la reparación.

### Pasos

1. Cree la Orden de Servicio manualmente para el Artículo que requiere reparación.
   1. Elija el icono ![Bombilla que abre la función Dígame.](../../media/ui-search/search_small.png "Dígame qué desea hacer") Icono, ingrese **Órdenes de servicio**
   2. Seleccione la acción **Nuevo**.
   3. Ingresar **10000** en el N.º de Cliente campo
   4. Seleccione **REPARAR** para el campo **Tipo de orden de servicio**.
   5. En Líneas, seleccione **S-100** como **N.º de artículo**.
2. Opcionalmente
   1. Elija la Línea de acción **Solución de problemas** para comprobar posibles soluciones.
   2. Elija la acción de línea **Fallo/Resol. Relaciones de códigos**
   3. Seleccione *RUIDO* como **Código de síntoma**
   4. Seleccione *5-2 Ruido fuerte durante la preparación* como **Código de error** y cierre la página. El código de error y los códigos de resolución se actualizan en líneas.
3. Prestar un reemplazo mientras se repara el artículo
   1. En Líneas, seleccione **PRÉSTAMO1** como el N.º de préstamo. Confirme la emisión del Préstamo seleccionando **Sí** para prestar el Préstamo. 
   2. Elija la acción Funciones **Obtener Códigos de servicio est.**, seleccione el código estándar asociado con el grupo de servicio y seleccione **Aceptar**.
   
### Resultados

- Se crea un pedido de servicio para el producto
- El Registro de documentos de servicio del pedido de servicio muestra las actividades del producto prestado.
- El producto prestado tiene un movimiento para reflejar el préstamo.
   

## El registrador realizó el trabajo, marque el préstamo como devuelto.

### Escenario  

El técnico de servicio marca el préstamo como devuelto y registra el trabajo realizado.

### Pasos

1. Ubique la tarea de Servicio y registre la hora 
   1. Elija el icono ![Bombilla que abre la función Dígame.](../../media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Tareas de servicio** y luego elija el enlace relacionado.
   2. Localice la orden de servicio para ingresar el tiempo.
   3. Elija la acción **Hoja de producto**.
   4. Escriba la siguiente información

    |Tipo|N.º|Cantidad|
    |----|---|--------|  
    |Artículo|SER102|2|

   4. Seleccione *TERMINADO* en el campo **Código de estado de reparación**
    
2. Marcar préstamo como devuelto
   1. Elija el icono ![Bombilla que abre la función Dígame.](../../media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Productos prestados** y luego elija el enlace relacionado.
   2. Localice el préstamo para marcarlo como devuelto.
   3. Seleccione la acción **Recibir** 
   4. Confirme la devolución del Préstamo seleccionando **Sí** para devolver el Préstamo.
      
### Resultados

- El **Registro de documentos de servicio** del pedido de servicio muestra las actividades del producto prestado.
- El producto prestado tiene un movimiento para reflejar el recibo.


### Escenario  

Charles, el gerente de servicio, publica el pedido de servicio terminado.

1. Ubicar el pedido de servicio 
   1. Elija el icono ![Bombilla que abre la característica Dígame](../../media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Pedidos de servicio** y luego elija el enlace relacionado.
   2. Ubique el pedido de servicio que desee registrar.

2. En el pedido de servicio, registre la factura
   1. Elija la acción **Registrar** para completar la Orden de Servicio, seleccione la acción **Envío y factura** y luego elija el botón **Aceptar**.
   2. Confirme la apertura de la factura registrada seleccionando **Sí**. 
### Resultados

- se creará una **factura de servicio publicada**.
- se crean las **Entradas de libro de servicio** asociadas con el artículo y recurso

## Consulte también
[Tutorial de contratos de servicio para artículos de servicio](service-contract-flow.md)  
[Servicio](../../service-service.md)
