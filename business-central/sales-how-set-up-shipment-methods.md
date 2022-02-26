---
title: Configuración de métodos de envío
description: Puede configurar un código para cada uno de los métodos de envío ofrecidos e introducir información sobre ellos.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: incoterms
ms.search.form: 11, 130
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 032faa6e9266f966f0c6393eb1837e1ca9bc9f55
ms.sourcegitcommit: a9e2aaee735870af566db68532cfa697347d68e0
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 11/04/2021
ms.locfileid: "7752510"
---
# <a name="set-up-shipment-methods"></a>Configurar métodos de envío

Los métodos de envío suelen depender del tipo de producto, de los clientes y de los proveedores. Por ejemplo, si el cliente reside en una isla, puede elegir que le envíen siempre los productos por barco o por avión. Algunos clientes pueden requerir la entrega al día siguiente. Algunos pueden querer recoger el pedido. Puede especificar el tipo de entrega deseado en las fichas de cliente y de proveedor.

En la página **Métodos de envío**, configure la descripción y el código correspondiente a cada método de envío. Por ejemplo, puede configurar el código FAB e introducir Franco a bordo en el campo **Descripción**. A continuación, puede introducir el código en los campos **Código de método de envío** en otra parte del sistema, como en una ficha cliente. A continuación, cuando cree nuevos pedidos, facturas, abonos, etc., el sistema introducirá la descripción incluida en el código. Se puede modificar en el documento según sea necesario.

## <a name="to-set-up-a-shipment-method"></a>Para configurar una forma de envío

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Métodos de envío** y luego elija el enlace relacionado.
2. En la página **Métodos de envío**, seleccione la acción **Nuevo**.
3. En la nueva línea especifique un código y una descripción para el método de envío.

> [!TIP]
> Si usa Incoterms, configure métodos de envío para representar las reglas de Incoterms relevantes.  

## <a name="see-also"></a>Consulte también

[Configurar transportistas](sales-how-to-set-up-shipping-agents.md)  
[Hacer un seguimiento de los paquetes](sales-how-track-packages.md)  
[Gestión de almacenes](warehouse-manage-warehouse.md)  
[Inventario](inventory-manage-inventory.md)  
[Configuración de la gestión del almacén](warehouse-setup-warehouse.md)  
[Gestión de ensamblaje](assembly-assemble-items.md)  
[Detalles de diseño: gestión de almacén](design-details-warehouse-management.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Incoterms en iccwbo.org](https://iccwbo.org/resources-for-business/incoterms-rules)  

[!INCLUDE[footer-include](includes/footer-banner.md)]