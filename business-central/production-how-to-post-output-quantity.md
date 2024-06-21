---
title: Registrar por lotes el resultado y tiempos de ejecución de producción
description: La cantidad de salida representa el trabajo en curso en términos de cantidad terminada y capacidad utilizada del centro de trabajo o de máquina.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.form: '99000773, 99000778, 99000823, 99000827'
ms.date: 03/08/2023
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# Registrar por lotes el resultado y los tiempos de ejecución

La cantidad de salida representa el trabajo en curso en términos de cantidad terminada y capacidad utilizada del centro de trabajo o de máquina.

Puede usar el diario de salida para:

* Ajustar el inventario en relación con la salida de los productos terminados de producción.
* Registrar las cantidades y el rechazo para cada operación en la ruta de producción.
* Registrar la configuración y el tiempo de ejecución de los centros de trabajo y de máquina.

> [!NOTE]
> Si se usa la ruta de producción, se actualiza solo cuando registra la cantidad de salida en la última operación.

La página **Diario de producción** le permite hacer las mismas tareas que en la página **Diario de salida**, y también hacer tareas de contabilización de consumo. Para obtener más información, consulte [Registrar el consumo y la salida de una línea de orden de producción lanzada](production-how-to-register-consumption-and-output.md).

## Para registrar cantidades de salida y/o registrar tiempos de ejecución en una o varias líneas de la orden de producción

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Diario salida**, y luego elija el enlace relacionado.  
2. Rellene los campos con los datos de las órdenes de producción y los datos de salida y/o tiempo de ejecución. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
  
    Puede usar la función **Desplegar ruta** para generar líneas de diario a partir de órdenes de producción.
  
3. Si la operación se ha completado, seleccione el campo **Terminado**.  
4. Para registrar las operaciones, elija la acción **Registrar**.

    Los movimientos de capacidad se actualizan para los centros de trabajo o de máquinas usados con información sobre el tiempo y la cantidad de salida y rechazo. Si registró la última operación, el producto se agregará al inventario.

    [!INCLUDE [preview-posting-inventory](includes/preview-posting-inventory.md)]

## Consulte también

[Registrar el material de rechazo manualmente](production-how-to-post-scrap.md)
[Revertir el registro de la salida](production-how-to-reverse-output-posting.md)
[Fabricación](production-manage-manufacturing.md)
[Configurar fabricación](production-configure-production-processes.md)  
[Planificación](production-planning.md)  
[Inventario](inventory-manage-inventory.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
