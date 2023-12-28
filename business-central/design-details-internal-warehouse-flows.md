---
title: 'Detalles de diseño: Flujos para producción, ensamblaje y proyectos'
description: 'Aprenda sobre el flujo entre ubicaciones para picking de componentes y ubicación de artículos finales para órdenes de ensamblado, producción o proyecto.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.date: 12/16/2022
ms.custom: bap-template
---
# Flujos para producción, ensamblaje y proyectos

Los flujos internos, como la selección de componentes y el almacenamiento de artículos finales para ensamblaje, trabajos y órdenes de producción, son similares a los flujos de entrada o salida. Por lo tanto, muchos de los procesos pueden parecer familiares. Este artículo proporciona información sobre cómo trabajar con flujos de almacén internos con varios niveles de complejidad.

## Descripción general de las diferentes opciones de configuración

Puede configurar funciones de almacén de varias formas. Es importante que las opciones que elija mejoren sus procesos sin causar gastos generales. Las siguientes tablas describen configuraciones típicas para tratar con bienes físicos para producción, trabajos y órdenes de ensamblaje.

### Flujo de entrada (ubicación)

|Nivel de complejidad|Descripción|Configuración|Cód. ubicación|Flujo de entrada de la orden de producción|Flujo de entrada de la orden de ensamblaje|Flujo de entrada de proyectos|  
|---|----------------|----------|---------|------------------|------------------|------------------|
|No hay ninguna actividad de almacén dedicada.|Registrar desde pedidos y diarios||Opcional. Controlado por el control de alternancia **Código Bin es Obligatorio**.|Diario de producción -> Diario de salida</br><br/> **NOTA**: puede publicar la salida usando **Diario de producción**.|Pedido de ensamblado|La ubicación no se aplica a los trabajos|  
|Básico|Pedido por pedido.|Requerir almacenamiento. </br><br/> **NOTA**: Aunque la configuración se llama **Requerir ubicación**, aún puede publicar la salida de los documentos de origen en las ubicaciones donde seleccione esta casilla de verificación. |Opcional. Controlado por el control de alternancia **Código Bin es Obligatorio**.|Orden de producción -> Ubicación de inventario|Pedido de ensamblado|La ubicación no se aplica a los trabajos|
|Avanzado|Actividades de ubicación consolidadas para múltiples documentos de origen.|Requerir recepción + Requerir ubicación|Opcional. Controlado por el control de alternancia **Código Bin es Obligatorio**.|Orden de producción -> Diario de salida|Órdenes de montaje -> movimientos internos | La ubicación no se aplica a los trabajos|
|Avanzado|Igual que arriba + Actividades de selección/ubicación dirigidas|Selección y ubicación dirigidas (los conmutadores dependientes se habilitarán automáticamente)|Obligatoria|Igual que en el caso anterior.|Igual que en el caso anterior.| La ubicación no se aplica a los trabajos|

Algunas configuraciones no le permiten usar documentos de almacén dedicados para registrar ubicaciones. Sin embargo, si su ubicación usa contenedores, puede usar documentos de movimiento genéricos para mover artículos producidos o ensamblados al almacén. Obtener más información en [Mover productos internamente en configuraciones básicas de almacén](warehouse-how-to-move-items-ad-hoc-in-basic-warehousing.md).

### Flujo de salida (pick)

|Nivel de complejidad|Descripción|Configuración|Cód. ubicación|Flujo de salida de la orden de producción|Flujo de salida de la orden de ensamblaje|Flujo de salida de proyectos|  
|---|----------------|----------|---------|------------------|------------------|------------------|
|No hay ninguna actividad de almacén dedicada.|Registrar desde pedidos y diarios||Opcional. Controlado por el control de alternancia **Código Bin es Obligatorio**.|Diario de producción -> Diario de consumo </br><br/> **NOTA**: puede registrar el consumo usando un **Diario de producción**.|Pedido de ensamblado|Proyecto -> Diario de proyecto|  
|Básico|Pedido por pedido.|Picking requerido. </br><br/> **NOTA**: Aunque la configuración se llama **Picking requerido**, aún puede publicar la salida de los documentos de origen en las ubicaciones donde seleccione esta casilla de verificación. <!-- ToDo Test prod output-->|Opcional. Controlado por el control de alternancia **Código Bin es Obligatorio**.|Pedido de producción -> Picking de inventario|Orden de montaje -> movimiento de inventario</br><br/>El **Movimiento de inventario** solo se puede usar con ubicaciones.|Proyecto -> Picking de inventario|
|Avanzado|Actividades de picking consolidadas para múltiples documentos de origen.|Requerir envío + Requerir picking|Opcional. Controlado por el control de alternancia Código Bin es Obligatorio|Órdenes de producción -> Picking de almacén -> Diario de consumo |Órdenes de montaje -> Selección de almacén| Proyectos -> Picking de almacén -> Diario de proyectos |
|Avanzado|Igual que arriba + Actividades de selección/ubicación dirigidas|Selección y ubicación dirigidas (los conmutadores dependientes se habilitarán automáticamente)|Obligatoria|Igual que en el caso anterior.|Igual que en el caso anterior.| La ubicación y el picking directo no es compatible con los proyectos|

De manera similar al flujo de entrada, algunas configuraciones no le permiten usar documentos de almacén dedicados para registrar ubicaciones. Si su ubicación usa contenedores, puede usar documentos de movimiento genéricos para mover artículos producidos o ensamblados. Obtenga más información en [Mover productos](warehouse-move-items.md).

## Almacenes sin actividad de almacén dedicada

Incluso si no tiene actividades de almacén dedicadas, probablemente aún desee realizar un seguimiento de cosas como el consumo y la producción. Los siguientes artículos proporcionan información sobre cómo procesar recibos para documentos de origen.

* [Registrar el consumo y la salida de una línea de orden de producción lanzada](production-how-to-register-consumption-and-output.md)
* [Ensamblar artículos](assembly-how-to-assemble-items.md)
* [Registrar el consumo o uso para proyectos](projects-how-record-job-usage.md)

## Configuración básica de almacén

Los flujos de entrada y salida en una configuración básica de almacén implican la siguiente configuración en la página **Tarjeta de ubicación** para la ubicación:

* Para el flujo de entrada (ubicación), active la opción **Requerir ubicación**, pero desactive el control de alternancia **Requerir recibo**.
* Para el flujo de salida (picking), active la opción **Requerir picking**, pero desactive el control de alternancia **Requerir envío**.

### Flujos hacia y desde producción en una configuración básica de almacén  

Utilice documentos de **Picking de inventario** para seleccionar componentes de producción en el flujo a producción. Para ubicar los productos que produce, use documentos de **Almacenamiento de inventario**.

Para ubicaciones que usan contenedores, los documentos de movimiento de inventario son especialmente útiles para el vaciado de componentes. Para obtener más información acerca del procedimiento de bajada del consumo de componentes desde las ubicaciones para producción o de aprovisionamiento manual, consulte [Baja de componentes de producción en el almacén](warehouse-how-to-pick-for-production.md#flushing-production-components-in-a-basic-warehouse-configuration).

   > [!NOTE]
   > Los movimientos de inventario son documentos importantes si utiliza los métodos de vaciado **Seleccionar + adelante** o **Seleccionar + retroceder**. Obtenga más información en [Métodos de baja](production-how-to-flush-components-according-to-operation-output.md#flushing-methods).

* Los campos **Cód. ubic. para producción**, **Cód. ubic. desde producción** y **Abre ubic. aprovision. manual** de la ubicación o de la máquina/centro de trabajo definen los flujos predeterminados a las áreas de producción y desde ellas.
* Administre el movimiento de artículos producidos en la página **Movimiento interno** sin una relación con una orden de producción.

### Flujos hacia y desde ensamblado en una configuración básica de almacén  

Publique la producción y el consumo de ensamblaje directamente desde una orden de ensamblaje.

> [!NOTE]
> Los documentos de **selección de inventario** y **ubicación de inventario** no se admiten para órdenes de ensamblado.

Para almacenes que usan ubicaciones:

* Utilice los documentos **Movimiento de inventario** para mover componentes del ensamblado al área de ensamblado.
* Los campos de **Cód. ubic. para ensamblado**, **Cód. ubic. desde ensamblado** de la ficha de ubicación definen los flujos predeterminados a áreas del ensamblado y desde ellas.
* Administre el movimiento de artículos ensamblados en la página **Movimiento interno**, sin una relación con una orden de ensamblado.

[!INCLUDE [prod_short](includes/prod_short.md)] es compatible con los flujos de ensamblado ensamblar para stock y ensamblar para pedido. Obtenga más información en [Descripción de ensamblar para pedido y ensamblar para stock](assembly-assemble-to-order-or-assemble-to-stock.md#understanding-assemble-to-order-and-assemble-to-stock). En relación con la gestión de almacenes, ensamblar para stock es parte del flujo de almacén interno y ensamblar para ordenar está en el flujo de almacén de salida. Obtenga más información en [Tratamiento de productos de ensamblar para pedido con los picking de inventario](warehouse-how-to-pick-items-with-inventory-picks.md#handling-assemble-to-order-items-with-inventory-picks).

### Flujos de gestión de proyectos en una configuración básica de almacén

Utilice documentos de **Picking de inventario** para seleccionar componentes de proyecto en el flujo a la administración de proyectos.

Para una ubicación que utiliza contenedores, el campo **Código de contenedor al trabajo** en la ubicación define los flujos predeterminados para la gestión de proyectos.

## Configuración avanzada de almacén  

Los flujos de entrada y salida en una configuración avanzada de almacén implican la siguiente configuración en la página **Tarjeta de ubicación** para la ubicación:

* Para el flujo de entrada (ubicación), active los controles de alternancia **Requerir recepción** y **Requerir almacenamiento**.
* Para el flujo de salida (picking), active los controles de alternancia **Requerir envío** y **Requerir recepción**.

### Flujos hacia y desde producción en configuraciones avanzadas de almacén

Utilice los documentos **Selección de almacén** y la página **Hoja de trabajo de selección** para seleccionar componentes para producción.

Para almacenes que usan ubicaciones:

* Los documentos **Movimiento de almacén** y la página **Hoja de trabajo de movimiento** son especialmente útiles para el vaciado de componentes. Obtenga más información en [Baja de componentes de producción en el almacén](warehouse-how-to-pick-for-internal-operations-in-advanced-warehousing.md#flushing-production-components-in-an-advanced-warehouse-configuration).
* Los campos **Cód. ubic. para producción**, **Cód. ubic. desde producción** y **Abre ubic. aprovision. manual** de la ubicación o de la máquina/centro de trabajo definen los flujos predeterminados a las áreas de producción y desde ellas. 
* Administre el movimiento de artículos producidos en las páginas **Hoja de trabajo de movimiento** o **Almacenamiento interno de almacén**, sin una relación con una orden de producción.

### Flujos hacia y desde ensamblaje en configuraciones avanzadas de almacén

Utilice los documentos **Selección de almacén** y la página **Hoja de trabajo de selección** para seleccionar componentes para el ensamblaje.

Para almacenes que usan ubicaciones:

* Los campos de **Cód. ubic. para ensamblado** y **Cód. ubic. desde ensamblado** en la ubicación definen los flujos predeterminados a áreas del ensamblado y desde ellas.
* Administre el movimiento de artículos de ensamblaje en las páginas **Hoja de trabajo de movimiento** o **Almacenamiento interno de almacén**, sin una relación con una orden de ensamblaje.

[!INCLUDE [prod_short](includes/prod_short.md)] es compatible con los flujos de ensamblado ensamblar para stock y ensamblar para pedido. Obtenga más información en [Descripción de ensamblar para pedido y ensamblar para stock](assembly-assemble-to-order-or-assemble-to-stock.md#understanding-assemble-to-order-and-assemble-to-stock). 

Ensamblar para stock es parte del flujo de almacén interno y ensamblar para ordenar está en el flujo de almacén de salida. Obtenga más información en [Tratamiento de productos de ensamblar para pedido en los envíos de almacén](warehouse-how-ship-items.md#handling-assemble-to-order-items-in-warehouse-shipments).

### Flujos de gestión de proyectos en configuraciones avanzadas de almacén

Utilice los documentos **Selección de almacén** y la página **Hoja de trabajo de selección** para seleccionar componentes en el flujo para gestión de proyectos.

Para almacenes que utilizan ubicaciones, el campo **Código de contenedor a proyectos** en la ubicación define los flujos predeterminados para el área de proyectos.

## Consulte también  

[Información general de la gestión de almacenes](design-details-warehouse-management.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
