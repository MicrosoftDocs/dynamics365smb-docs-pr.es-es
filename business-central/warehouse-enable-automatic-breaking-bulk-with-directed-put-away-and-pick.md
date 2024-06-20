---
title: Interrupción masiva con picking y ubicaciones directas
description: 'Aprenda a habilitar interrupción automática masiva con ubicación y picking dirigidos, así como interrupción en picking, ubicaciones, movimientos y más.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.search.form: '5703, 7352'
ms.date: 11/04/2022
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# Habilitar interrupción automática masiva con ubicaciones y picking directos

En almacenes que utilizan ubicación y picking directos, [!INCLUDE[prod_short](includes/prod_short.md)] puede dividir unidades de medida grandes en otras unidades de medida más pequeñas, cuando crea instrucciones de almacén que cubren las necesidades de los documentos de origen, órdenes de producción o ubicaciones y picking internos. Dividir también puede significar reunir artículos en unidades de medida más pequeñas para igualar la cantidad de una unidad de medida más grande en un documento de origen o un pedido de producción.

## División en picking  

Si desea almacenar productos en varias unidades de medida distintas en un almacén y permitir que se combinen automáticamente en el proceso de picking, active la alternancia **Permite división bulto** en la página de ficha de almacén. Después, para cumplir una tarea, [!INCLUDE [prod_short](includes/prod_short.md)] buscará un producto en la misma unidad de medida. Si no encuentra uno, [!INCLUDE [prod_short](includes/prod_short.md)] le sugerirá que divida una unidad de medida más grande en la unidad de medida que se necesita.  

Si solo hay unidades de medida pequeñas, [!INCLUDE [prod_short](includes/prod_short.md)] sugerirá que reúna productos para hacer frente a la cantidad de la recepción o la orden de producción. De hecho, divide la unidad de medida grande del documento de origen en unidades menores para el picking.  

## Dividir bultos en almacenes  

En ubicaciones de almacén, [!INCLUDE [prod_short](includes/prod_short.md)] sugiere Colocar líneas de acción en la unidad de medida de ubicación. Por ejemplo, podría sugerir piezas aunque los artículos lleguen en una unidad de medida diferente.  

## Dividir bultos en movimientos  

[!INCLUDE [prod_short](includes/prod_short.md)] también puede dividir en movimientos de reaprovisionamiento si la alternancia **Permitir división bulto** en la página **Calcular reabastecimiento de contenedores** está activada.  

Puede ver el resultado del proceso de conversión de una unidad de medida a otra como líneas de división de bulto intermedias en las instrucciones de movimiento, picking o ubicación.  

> [!NOTE]  
> Si selecciona el campo **Define filtro div. bulto** en la cabecera de instrucciones del almacén, la aplicación ocultará las líneas de división de bultos siempre que se utilice íntegramente la unidad de medida más grande. Por ejemplo, si un palé tiene 12 unidades y va a utilizar esas 12 unidades, el picking indicará que utilice 1 palé y que coloque 12 unidades. Sin embargo, si debe seleccionar solo 9 piezas, las líneas de carga fraccionada no se ocultan, incluso si ha seleccionado el campo **Filtro de carga fraccionada**. Las líneas no están ocultas porque debe colocar las tres piezas restantes en algún lugar del almacén.  

> [!NOTE]  
> Si desea que sus unidades de medida se distribuyan de una forma óptima en el almacén, junto con la funcionalidad de división de bultos, debería intentar:  
>
> - Configurar la unidad de medida base de un producto según la unidad de medida más pequeña que espera manipular en los procesos de almacén.  
> - Configurar unidades de medida alternativas del producto como múltiplos de la unidad de medida base.  

## Consulte también  

[Información general de la gestión de almacenes](design-details-warehouse-management.md)
[Inventario](inventory-manage-inventory.md)  
[Configuración de Warehouse Management](warehouse-setup-warehouse.md) 
[Gestión de ensamblaje](assembly-assemble-items.md)
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]