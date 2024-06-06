---
title: Ensamblar para proyecto
description: Aprenda a utilizar el ensamblar para pedido para proyectos.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'project management, task'
ms.search.form: '88, 275, 276, 1001, 1002, 1003, 1004, 1005, 1006, 1007, 1020'
ms.date: 08/03/2022
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# Ensamblar para proyecto

Ensamblar para proyecto le ayuda a mejorar la gestión de inventario al ensamblar según pedido solo cuando sea necesario.

Cuando elige un artículo ensamblar para pedido en una línea de planificación de proyecto, [!INCLUDE [prod_short](includes/prod_short.md)] crea una orden de montaje. El pedido de ensamblado se basa en la línea de planificación de proyecto y sus líneas se basan en la lista de materiales (L.M.) del ensamblado del artículo. Para obtener más información sobre las LDM de ensamblaje, vaya a [Trabajar con LDM de ensamblaje](assembly-how-work-assembly-boms.md). La cantidad de componentes en la lista de materiales de ensamblaje se multiplica por la cantidad del pedido. La página **Líneas de ensamblaje para pedido** muestra detalles sobre las líneas de pedido de ensamblaje vinculadas. Los detalles pueden ayudarlo a personalizar el elemento de ensamblaje. Al igual que en las ventas, no puede publicar directamente pedidos de ensamblaje vinculados. Para obtener más información sobre las órdenes de ensamblado, vaya a [Vender productos de inventario en los flujos de ensamblar para pedido](assembly-how-to-sell-inventory-items-in-assemble-to-order-flows.md).

Los pedidos de ensamblado están reservados para proyectos, y [!INCLUDE [prod_short](includes/prod_short.md)] sincroniza el seguimiento de artículos entre las líneas de planificación del proyecto y el orden de ensamblaje.

## Integra con Warehouse Management

Ensamblar para proyecto se integra con las funciones de Warehouse Management para facilitar el montaje y el envío. El proceso también ayuda a garantizar que el flujo desde el montaje del proyecto hasta la entrega se desarrolle sin problemas en los procesos internos del almacén. Para obtener más información sobre los flujos de almacén internos para proyectos, vaya a [Flujos de producción, montaje y trabajo](design-details-internal-warehouse-flows.md#flows-to-and-from-assembly-in-a-basic-warehouse-configuration).

La siguiente tabla describe las configuraciones de almacén que admiten ensamblar para pedido.

|Configuración  |Descripción  |
|---------|---------|
|**No hay manipulación de almacén**|Utilice un diario del proyecto para registrar el uso total o parcial. La salida y el consumo de componentes se contabilizan automáticamente para el pedido de montaje.         |
|**Picking inventario**|Utilice un picking de inventario para registrar el uso total o parcial. La salida y el consumo de componentes se contabilizan automáticamente para el pedido de montaje.          |
|**Picking almacén**|Cree y registre selecciones de almacén para componentes y luego use un diario de proyecto para registrar el uso. [!INCLUDE [prod_short](includes/prod_short.md)] verifica si los componentes del ensamblaje consumidos fueron seleccionados. La salida y el consumo de componentes se contabilizan automáticamente para el pedido de montaje.         |

## Limitaciones conocidas

Esta sección describe las limitaciones conocidas para ensamblar en proyecto.

* El campo **Cantidad para ensamblar según pedido** no está disponible para proyectos que están cerrados.
* Para escenarios de selección de almacén, la **Cantidad para ensamblar para pedido** puede ser cero o igual a la cantidad. No se puede combinar ensamblar para pedido y ensamblar para stock en una línea de planificación de proyecto. Debe crear líneas de planificación de proyecto independientes.
* Ensamblar para pedido no afecta las partes facturables de un proyecto. En las facturas de venta se incluye un conjunto, pero no sus componentes. No puede editar el campo **Cantidad para ensamblar para pedido** para líneas facturables.
* La planificación de pedidos y la hoja de trabajo de planificación no se ven afectadas porque el proyecto es la entrada para la planificación. El motor de planificación considera el montaje como demanda.
* No puede ingresar una cantidad negativa en el campo **Cantidad para ensamblar para pedido**.
* No se puede deshacer un ensamblaje.

## Consulte también

[Administración de proyectos](projects-manage-projects.md)  
[Administración de ensamblados](assembly-assemble-items.md)  
[Crear proyectos](projects-how-create-jobs.md)
