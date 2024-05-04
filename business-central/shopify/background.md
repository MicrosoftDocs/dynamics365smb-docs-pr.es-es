---
title: Ejecutar tareas en segundo plano y de forma recurrente
description: Configure la sincronización de datos entre Business Central y Shopify en segundo plano.
ms.date: 03/26/2024
ms.topic: article
ms.service: dynamics-365-business-central
ms.reviewer: solsen
author: brentholtorf
ms.author: bholtorf
---

# Ejecutar tareas en segundo plano

Es eficiente ejecutar algunas tareas simultáneamente y de forma automatizada. Puede realizar dichas tareas en segundo plano y también puede establecer un cronograma cuando desee que esas tareas se ejecuten automáticamente. Para ejecutar tareas en segundo plano, se admiten dos modos:

- Las tareas activadas manualmente se programan inmediatamente a través de **Movimientos de cola de proyectos**.
- Las tareas recurrentes se programan en **Movimientos de cola de proyectos**.

## Ejecutar tareas en segundo plano para una tienda específica

1. Elija la ![Bombilla que abre la función Dígame.](../media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Tienda de Shopify** y luego elija el vínculo relacionado.
2. Seleccione la tienda para la que desea ejecutar la sincronización en segundo plano para abrir la página **Tarjeta de tienda de Shopify**.
3. Active la alternancia **Permitir sincronizaciones en segundo plano**.

Ahora, cuando se inicia la acción de sincronización, en lugar de ejecutar una tarea en primer plano, le pide que espere. Cuando se haya completado, puede continuar con la siguiente acción. La tarea se crea como un **Movimiento de cola de proyectos** y comienza de inmediato.

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
|**Sincronizar empresas**|Informe 30114 Sincronizar empresas con Shopify (B2B)|
|**Sincronizar pagos**|Informe 30105 Sincronizar pagos con Shopify|
|**Catálogos sincronización**|Informe 30115 Sincronizar catálogos de Shopify (B2B)|
|**Sincronizar precios de catálogos**|Informe 30116 Sincronizar precios de catálogos de Shopify (B2B)|

> [!NOTE]
> Algunos elementos pueden ser actualizados por varias tareas, por ejemplo, cuando importa pedidos, dependiendo de la configuración en la **Tarjeta de tienda de Shopify**, el sistema también puede importar y actualizar datos de clientes y/o productos. Recuerde utilizar la misma categoría de cola de trabajos para evitar conflictos.

Otras tareas que pueden ser útiles para automatizar el procesamiento posterior de los documentos de ventas:

- informe 297 de lote de facturas posterior a la compra
- informe 296 de lote de pedidos posterior al pedido de venta

Puede usar el campo **N.º de pedido de Shopify** para identificar los documentos de ventas que se importaron desde Shopify.

Para obtener más información sobre la publicación de pedidos de venta en un lote, vaya a [Para crear una entrada de cola de trabajos para el registro por lotes de pedidos de venta](../ui-batch-posting.md#to-create-a-job-queue-entry-for-batch-posting-of-sales-orders).

## Para comprobar el estado de la sincronización

En el Área de trabajo **Administrador de negocio**, la parte **Actividades de Shopify** ofrece varias señales que pueden ayudarle a identificar rápidamente si hay problemas con el conector de Shopify.

- **Clientes no asignados**: el cliente de Shopify se importa, pero no está vinculado a una entrada de cliente correspondiente en [!INCLUDE [prod_short](../includes/prod_short.md)].
- **Productos no asignados**: el producto de Shopify se importa, pero no está vinculado a una entrada de cliente correspondiente en [!INCLUDE [prod_short](../includes/prod_short.md)].
- **Pedidos no procesados**: los pedidos de Shopify se importaron, pero los documentos de ventas en [!INCLUDE [prod_short](../includes/prod_short.md)] no se crearon, a menudo debido a productos o clientes no asignados.
- **Envíos sin procesar**: los envíos de ventas registrados se originaron en pedidos de Shopify que no están sincronizados con Shopify.
- **Errores de envíos**: el conector de Shopify no pudo sincronizar los envíos de ventas registrados con Shopify.
- **Errores de sincronización**: hay entradas fallidas en la cola de trabajos relacionadas con la sincronización con Shopify.

## Consulte también

[Comenzar con el conector para Shopify](get-started.md)  
