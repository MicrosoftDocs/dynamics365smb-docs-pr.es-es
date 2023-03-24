---
title: Ejecutar tareas en segundo plano y de forma recurrente
description: Configure la sincronización de datos entre Business Central y Shopify en segundo plano.
ms.date: 05/11/2022
ms.topic: article
ms.service: dynamics365-business-central
ms.reviewer: solsen
author: edupont04
ms.author: andreipa
---

# Ejecutar tareas en segundo plano

Es eficiente ejecutar algunas tareas simultáneamente y de forma automatizada. Puede realizar dichas tareas en segundo plano y también puede establecer un cronograma cuando desee que esas tareas se ejecuten automáticamente. Para ejecutar tareas en segundo plano, se admiten dos modos:

- Las tareas activadas manualmente se programan inmediatamente a través de **Movimientos de cola de proyectos**.
- Las tareas recurrentes se programan en **Movimientos de cola de proyectos**.

## Ejecutar tareas en segundo plano para una tienda específica

1. Elija la ![Bombilla que abre la función Dígame.](../media/ui-search/search_small.png "Dígame qué desea hacer") icono, introduzca el nombre de **Tienda de Shopify** y elija el nombre de la tienda de la lista.
2. Seleccione la tienda para la que desea sincronizar artículos para abrir la página **Tarjeta de tienda de Shopify**.
3. Permitir la alternancia **Permitir sincronizaciones en segundo plano**.

Ahora, cuando se activa la acción de sincronización, en lugar de ejecutar una tarea en primer plano, le pedirá que espere. Cuando se haya completado, puede continuar con la siguiente acción. La tarea se crea como un **Movimiento de cola de proyectos** y comienza instantáneamente sin bloqueos.

## Programar tareas recurrentes

Puede programar las siguientes actividades recurrentes para que se realicen de forma automatizada. Obtenga más información sobre programar tareas en [Cola de trabajo](../admin-job-queues-schedule-tasks.md).

|Tarea|Objeto|
|------|------------|
|**Sincronizar pedidos desde Shopify**|Informe 30104 Sincronizar pedidos de Shopify|
|**Procesar pedidos de Shopify**|Informe 30103 Shopify crea pedidos de venta|
|**Sincronizar envíos con Shopify**|Informe 30109 Sincronizar envíos con Shopify|
|**Sincronizar productos y precios**|Informe 30108 Sincronizar productos de Shopify|
|**Sincronizar inventario**|Informe 30102 Sincronizar existencias con Shopify|
|**Sincronizar imágenes**|Informe 30107 Sincronizar imágenes con Shopify|
|**Sincronizar clientes**|Informe 30100 Sincronizar clientes con Shopify|
|**Sincronizar pagos**|Informe 30105 Sincronizar pagos con Shopify|

> [!NOTE]
> Algunos elementos pueden ser actualizados por varias tareas, por ejemplo, cuando importa pedidos, dependiendo de la configuración en la **Tarjeta de tienda de Shopify**, el sistema también puede importar y actualizar datos de clientes y/o productos. Recuerde utilizar la misma categoría de cola de trabajos para evitar conflictos.

## Consulte también .

[Comenzar con el conector para Shopify](get-started.md)  
