---
title: Gestión de ensamblaje
description: Aprenda a suministrar productos a sus clientes mediante la combinación de componentes en procesos simples sin usar funciones de fabricación.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.topic: conceptual
ms.date: 02/21/2023
ms.custom: bap-template
ms.search.keywords: 'kit, kitting'
ms.search.form: '900, 901, 902, 903, 904, 907, 910, 916, 920, 921, 922, 923, 940, 941, 942, 930, 931, 932, 914, 915, 905'
---
# <a name="assembly-management"></a>Gestión de ensamblaje

Las empresas pueden suministrar productos a sus clientes mediante la combinación de componentes sin usar funciones de fabricación. Las funciones para ensamblar artículos se integran con funciones relacionadas, como ventas, planificación, reservas y almacenamiento.  

Un artículo de montaje se define como uno vendible que contenga un L.M. de ensamblado. Para obtener más información sobre las LDM de ensamblaje, vaya a [Trabajar con LDM de ensamblaje](assembly-how-work-assembly-boms.md).

Las órdenes de montaje son órdenes internas, al igual que las órdenes de producción. Utilice órdenes de montaje para gestionar el proceso de montaje y conectar los requisitos de ventas con las actividades del almacén. Las órdenes de ensamblado implican tanto la salida como el consumo cuando se contabilizan. Los encabezados de órdenes de ensamblaje son similares a las líneas del diario de salida. Las líneas de órdenes de ensamblaje son similares a las líneas del diario de consumo.  

Puede utilizar una estrategia de inventario justo a tiempo y personalizar los productos para satisfacer las solicitudes de los clientes. Los pedidos de ensamblado se peuden crear y vincular automáticamente cuando se cree una línea de pedido de venta. El vínculo entre la demanda de ventas y el suministro de ensamblaje abre varias oportunidades cuando procesa órdenes de venta:

* Personalice elementos de ensamblado sobre la marcha.
* Prometa fechas de entrega según disponibilidad de componentes.
* Publique la salida y el envío del artículo ensamblado directamente desde sus órdenes de venta.

Para obtener más información sobre la venta de artículos de ensamblaje, vaya a [Vender artículos ensamblados por pedido](assembly-how-to-sell-items-assembled-to-order.md).  

Las líneas de los pedidos de venta pueden contener artículos para recoger del stock y artículos para ensamblar para el pedido. Las cantidades ensambladas a pedido tienen prioridad sobre las cantidades de inventario en envíos parciales. Para obtener más información sobre la venta de artículos de ensamblaje y stock, vaya a [Escenarios de combinación](assembly-assemble-to-order-or-assemble-to-stock.md#combination-scenarios).  

Cuando una cantidad de ensamblar para pedido está lista para enviarse, un empleado de almacén puede registrar un picking de existencias para las líneas de pedido de ventas. Publicar una selección de inventario hace un par de cosas:

* Crear un movimiento de inventario para los componentes
* Registrar la salida del conjunto y el envío del pedido de venta.

Para obtener más información sobre artículos de ensamblado para pedido y picking de inventario, vaya a [Tratamiento de productos para ensamblar para pedido en los pickings de inventario](warehouse-how-to-pick-items-with-inventory-picks.md#handling-assemble-to-order-items-with-inventory-picks).

En la tabla siguiente se indican una serie de tareas con vínculos a los artículos que las describen.

|**Para**|**Vea**|  
|------------|-------------|  
|Aprenda a ensamblar artículos para órdenes de venta y almacenamiento.|[Descripción de ensamblar para pedido y ensamblar para stock](assembly-assemble-to-order-or-assemble-to-stock.md)|
|Use fichas de ubicación y la configuración del inventario para definir cómo fluyen los artículos en el ensamblaje.|[Configurar almacenes básicos con áreas de operaciones](warehouse-how-to-set-up-basic-warehouses-with-operations-areas.md)|
|Cotice un artículo de ensamblaje personalizado y luego convierta la cotización en una venta cuando el cliente la acepte.|[Oferta de una venta de ensamblar para pedido](assembly-how-to-quote-an-assemble-to-order-sale.md)|
|Agrupe los componentes para crear un artículo para pedido o para stock.|[Ensamblar artículos](assembly-how-to-assemble-items.md)|  
|Vender elementos de ensamblaje que no están disponibles actualmente mediante una orden de ensamblado vinculada para suministrar la cantidad total o parcial de la orden de venta.|[Venta de artículos ensamblados para pedido](assembly-how-to-sell-items-assembled-to-order.md)|
|Cuando algunos productos de ensamblar para pedido ya se encuentran en el inventario, descuente esa cantidad de pedido de ensamblado y resérvela del inventario.|[Vender productos de inventario en los flujos de ensamblar para pedido](assembly-how-to-sell-inventory-items-in-assemble-to-order-flows.md)|  
|Cuando los artículos de ensamblado no están en el inventario, use una orden de ensamblado para suministrar una parte o la totalidad de la cantidad.|[Vender productos de ensamblado para pedido y productos de inventario juntos](assembly-how-to-sell-assemble-to-order-items-and-inventory-items-together.md)|
|Cree artículos de ensamblaje personalizados para pedidos de venta abiertos antes de crear los pedidos de venta.|[Crear pedidos abiertos ensamblados](assembly-how-to-create-blanket-assembly-orders.md)|
|Deshacer un pedido de ensamblado registrado, por ejemplo porque la orden se publicó con errores.|[Deshacer registro de ensamblado](assembly-how-to-undo-assembly-posting.md)|
|Aprenda a trabajar con listas de materiales de ensamblaje y sus diferencias con las listas de materiales de producción.|[Trabajar con L.M. de ensamblado](assembly-how-work-assembly-boms.md)|
|Aprenda a registrar el consumo y la salida del ensamblaje, y cómo [!INCLUDE [prod_short](includes/prod_short.md)] distribuye los costos de artículos y recursos en el libro mayor.|[Detalles de diseño: Registro de pedidos de ensamblado](design-details-assembly-order-posting.md)|  

## <a name="see-related-microsoft-training"></a>Consultar la [formación de Microsoft](/training/paths/assemble-items-dynamics-365-business-central/) relacionada

## <a name="see-also"></a>Consulte también .

[Trabajar con listas de materiales](inventory-how-work-BOMs.md)  
[Inventario](inventory-manage-inventory.md)  
[Descripción general de la gestión de almacenes](design-details-warehouse-management.md)
[Detalles de diseño: Planificación de suministro](design-details-supply-planning.md)  
<!-- [Walkthrough: Planning Supplies Manually](walkthrough-planning-supplies-manually.md)   -->
<!-- [Walkthrough: Selling, Assembling, and Shipping Kits](walkthrough-selling-assembling-and-shipping-kits.md)   -->
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  

[!INCLUDE[footer-include](includes/footer-banner.md)]
