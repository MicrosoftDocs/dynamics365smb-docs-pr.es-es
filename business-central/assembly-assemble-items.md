---
title: Gestión de ensamblaje
description: Apoyar a las empresas que suministran productos a sus clientes mediante la combinación de componentes en procesos simples sin necesidad de funcionalidad de fabricación.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: kit, kitting
ms.search.form: 900, 901, 902, 903, 904, 907, 910, 916, 920, 921, 922, 923, 940, 941, 942, 930, 931, 932, 914, 915, 905
ms.date: 06/14/2021
ms.author: edupont
ms.openlocfilehash: c026f7b8374dd78b4c3f06d76d43e3ffac0198b2
ms.sourcegitcommit: 8ad79e0ec6e625796af298f756a142624f514cf3
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 09/30/2022
ms.locfileid: "9607078"
---
# <a name="assembly-management"></a>Gestión de ensamblaje

Para apoyar a las empresas que suministran los productos a sus clientes agrupando los componentes en procesos sencillos sin necesidad de la funcionalidad de fabricación, [!INCLUDE[prod_short](includes/prod_short.md)] incluye las características para ensamblar artículos que se integran con las existentes, como son planificación, reservas y almacén.  

 Un artículo de montaje se define como uno sellable que contenga un L.M. de ensamblado. Para obtener más información, consulte [Trabajar con L.M. de ensamblado](assembly-how-work-assembly-boms.md).

 Los pedidos de ensamblado son pedidos internos, como las órdenes de producción, que se utilizan para gestionar el proceso de ensamblado y para conectar los requisitos de venta con las actividades de almacén correspondientes. Los pedidos de ensamblado difieren de otros tipos de pedido porque implican la salida y el consumo cuando se están registrando. La cabecera del pedido de ensamblado se comporta de modo similar a una línea de diario de salida, y las líneas del pedido de ensamblado se comportan de forma similar a las líneas del diario de consumo.  

 Para utilizar una estrategia de inventario puntual y la capacidad de personalizar los productos según las solicitudes del cliente, los pedidos de ensamblado pueden crearse y vincularse automáticamente tan pronto como se cree la línea del pedido de venta. El vínculo entre la demanda de venta y el suministro del ensamblado permite a los procesadores del pedido de venta personalizar el elemento del ensamblado de forma dinámica, comprometer las fechas de entrega según la disponibilidad del componente, así como registrar la salida el envío del producto ensamblado directamente en la interfaz del pedido de venta. Para obtener más información, consulte [Venta de artículos ensamblados para pedido](assembly-how-to-sell-items-assembled-to-order.md).  

 En una línea del pedido de venta, puede vender una cantidad que está disponible y se debe realizar el picking de las existencias junto con una cantidad que se debe ensamblar para el pedido. Existen ciertas reglas para controlar la distribución de estas cantidades para asegurar que las cantidades de ensamblar para pedido tengan prioridad sobre las cantidades del inventario en un envío parcial. Para obtener más información, consulte la sección "Escenarios de combinación" en [Conocer Ensamblar para pedido y Ensamblar para stock](assembly-assemble-to-order-or-assemble-to-stock.md).  

 Hay una funcionalidad especial para controlar el envío de las cantidades del ensamblar para pedido. Cuando una cantidad de ensamblar para pedido está lista para enviarse, el empleado del almacén responsable registra un picking de existencias para la línea o líneas en cuestión. A cambio, esto crea un movimiento de inventario para los componentes, registra la salida de ensamblado y el envío del pedido de venta. Para obtener más información, vea la sección "Tratamiento de productos de Ensamblar para pedido en los picking de existencias" en [Realizar picking de productos con picking de existencias](warehouse-how-to-pick-items-with-inventory-picks.md).

En la tabla siguiente se indican una serie de tareas con vínculos a los temas que las describen.   

|**Para**|**Vea**|  
|------------|-------------|  
|Saber la diferencia entre los artículos que ensamblan justo antes de los pedidos de venta de envío y los artículos que ensamblan para almacenamiento.|[Descripción de ensamblar para pedido y ensamblar para stock](assembly-assemble-to-order-or-assemble-to-stock.md)|
|Rellene los campos en las fichas de ubicación y en la configuración del inventario para definir cómo fluyen los artículos en el departamento de ensamblaje.|[Configurar almacenes básicos con áreas de operaciones](warehouse-how-to-set-up-basic-warehouses-with-operations-areas.md)|
|Personalizar un producto del ensamblado a la solicitud de un cliente durante el proceso de venta y convertirlo en venta cuando se acepte.|[Oferta de una venta de ensamblar para pedido](assembly-how-to-quote-an-assemble-to-order-sale.md)|
|Agrupe los componentes para crear un artículo en un proceso sencillo, para pedido o para stock.|[Ensamblar artículos](assembly-how-to-assemble-items.md)|  
|Vender elementos de ensamblaje que no están disponibles actualmente mediante una orden de ensamblado vinculada para suministrar la cantidad total o parcial de la orden de venta.|[Venta de artículos ensamblados para pedido](assembly-how-to-sell-items-assembled-to-order.md)|
|Cuando algunos productos de ensamblar para pedido ya se encuentran en el inventario, descuente esa cantidad de pedido de ensamblado y resérvela del inventario.|[Vender productos de inventario en los flujos de ensamblar para pedido](assembly-how-to-sell-inventory-items-in-assemble-to-order-flows.md)|  
|Cuando está vendiendo productos de ensamblado del inventario y ninguno de los productos está disponible, inicie un pedido de ensamblado para suministrar automáticamente una parte o toda la cantidad del pedido de venta.|[Vender productos de ensamblado para pedido y productos de inventario juntos](assembly-how-to-sell-assemble-to-order-items-and-inventory-items-together.md)|
|Cree artículos de ensamblaje personalizados para pedidos de ventas generales antes de realizar periódicamente los pedidos de ventas reales de acuerdo con el acuerdo de pedido abierto.|[Crear pedidos abiertos ensamblados](assembly-how-to-create-blanket-assembly-orders.md)|
|Deshacer un pedido de ensamblado registrado, por ejemplo porque la orden se publicó con errores que deben corregirse.|[Deshacer registro de ensamblado](assembly-how-to-undo-assembly-posting.md)|
|Aprenda a trabajar con listas de materiales de ensamblaje y las principales diferencias con las listas de materiales de producción.|[Trabajar con L.M. de ensamblado](assembly-how-work-assembly-boms.md)|
|Saber cómo se gestiona el consumo de ensamblado y a la salida cuando se registran los pedidos de ensamblado y cómo se procesan y se distribuyen a la contabilidad el artículo y los precios de coste de recurso derivados.|[Detalles de diseño: Registro de pedidos de ensamblado](design-details-assembly-order-posting.md)|  

## <a name="see-related-microsoft-training"></a>Consultar la [formación de Microsoft](/training/paths/assemble-items-dynamics-365-business-central/) relacionada

## <a name="see-also"></a>Consulte también .

[Trabajar con listas de materiales](inventory-how-work-BOMs.md)  
[Inventario](inventory-manage-inventory.md)  
[Detalles de diseño: Warehouse Management](design-details-warehouse-management.md)  
[Detalles de diseño: Planificación de aprovisionamiento](design-details-supply-planning.md)  
<!-- [Walkthrough: Planning Supplies Manually](walkthrough-planning-supplies-manually.md)   -->
<!-- [Walkthrough: Selling, Assembling, and Shipping Kits](walkthrough-selling-assembling-and-shipping-kits.md)   -->
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  

[!INCLUDE[footer-include](includes/footer-banner.md)]
