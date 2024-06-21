---
title: Configuración de métodos de envío
description: Puede configurar un código para cada uno de los métodos de envío ofrecidos e introducir información sobre ellos.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: incoterms
ms.search.form: '11, 130'
ms.date: 04/01/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# Configurar métodos de envío

Los métodos de envío suelen depender del tipo de producto, de los clientes y de los proveedores. Por ejemplo, si el cliente reside en una isla, puede elegir que le envíen siempre los productos por barco o por avión. Algunos clientes pueden requerir la entrega al día siguiente. Algunos pueden querer recoger el pedido. Puede especificar el tipo de entrega deseado en las fichas de cliente y de proveedor.

En la página **Métodos de envío**, configure la descripción y el código correspondiente a cada método de envío. Por ejemplo, puede configurar el código FAB e introducir Franco a bordo en el campo **Descripción**. A continuación, puede introducir el código en los campos **Código de método de envío** en otra parte del sistema, como en una ficha cliente. A continuación, cuando cree nuevos pedidos, facturas, abonos, etc., el sistema introducirá la descripción incluida en el código. Se puede modificar en el documento según sea necesario.

## Para configurar una forma de envío

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Métodos de envío** y luego elija el enlace relacionado.
2. En la página **Métodos de envío**, seleccione la acción **Nuevo**.
3. En la nueva línea especifique un código y una descripción para el método de envío.

> [!TIP]
> Si usa Incoterms, configure métodos de envío para representar las reglas de Incoterms relevantes.  

## Consulte también

[Configurar transportistas](sales-how-to-set-up-shipping-agents.md)  
[Hacer un seguimiento de los paquetes](sales-how-track-packages.md)  
[Información general de la gestión de almacenes](design-details-warehouse-management.md)
[Inventario](inventory-manage-inventory.md)  
[Configuración de Warehouse Management](warehouse-setup-warehouse.md)  
[Gestión de ensamblaje](assembly-assemble-items.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Incoterms en iccwbo.org](https://iccwbo.org/resources-for-business/incoterms-rules)  

[!INCLUDE[footer-include](includes/footer-banner.md)]