---
title: Crear órdenes de producción desde pedidos de venta
description: Conozca las distintas formas de crear pedidos de producción para productos producidos directamente a partir de pedidos de venta.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.topic: how-to
ms.date: 02/27/2023
ms.custom: bap-template
ms.search.form: '99000883, 99000884,'
---
# Crear órdenes de producción desde pedidos de venta

Puede crear órdenes de producción para artículos producidos directamente desde los pedidos de venta.  

## Para crear una orden de producción desde un pedido de venta  

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Pedidos de venta** y, a continuación, elija el vínculo relacionado.  
2. Seleccione el pedido de venta para el que desea crear una orden de producción.  
3. Seleccione la acción **Planificación**. En la página **Planificación pedido venta**, puede consultar la disponibilidad de un producto.  
4. Seleccione la acción **Orden de producción**.  
5. Seleccione el tipo del estado y orden.  
6. Seleccione el botón **Sí** para crear una o más órdenes de producción para las líneas que tengan **Ord. prod.** en su campo **Sistema de reposición**.

    > [!NOTE]  
    > Las líneas de demanda que disponen de **Prod. Pedido** en el campo **Sistema reposición** representan pedidos de producción subyacentes. Después de generar estos pedidos de producción, recuerde identificar cualquier demanda de componente no satisfecha para ellos. Utilice la página **Planificación de pedidos** o la acción **Replanificar** para detectar la demanda no satisfecha.
    >
    > Cuando crea pedidos de producción para pedidos de venta con la página Planificación de pedidos de venta, se aplican vínculos de pedido a pedido entre la demanda y la oferta. Cuando existen vínculos de pedido contra pedido, el sistema de planificación no incluye la oferta o el inventario vinculado en el procedimiento de contrapartida. Para obtener más información sobre la contrapartida, vaya a [Vínculos de pedido a pedido](design-details-central-concepts-of-the-planning-system.md#order-to-order-links).

## Tipo orden  

La siguiente tabla describe dos formas de crear pedidos de producción.

|Opción|Descripción|
|------|-----------|
|Orden producto|Se crea un pedido de producción para cada producto representado por una línea en la página **Planificación pedido venta**.|
|Orden proyecto|Se crea un pedido de producción multilínea para todos los productos representados por líneas en la página **Planificación pedido venta**. Cuando utiliza pedidos de proyecto, el campo **Tipo procedencia mov.** del pedido de producción contiene **Cab. venta**. El pedido tiene una línea por cada producto de línea de ventas que se debe producir.|

## Consulte también  

[Configuración de fabricación](production-configure-production-processes.md)  
[Fabricación](production-manage-manufacturing.md)  
[Inventario](inventory-manage-inventory.md)  
[Compras](purchasing-manage-purchasing.md)  
[Detalles de diseño: planificación de aprovisionamiento](design-details-supply-planning.md)  
[Procedimientos recomendados de configuración: planificación de suministros](setup-best-practices-supply-planning.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
