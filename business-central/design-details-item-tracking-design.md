---
title: 'Detalles de diseño: Diseño del seguimiento de productos | Documentos de Microsoft'
description: En este tema se describe el diseño subyacente al seguimiento de productos de Business Central.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: design, item, tracking, tracing
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: a0c60381634543f367e85a465c4ee74c3396d5ad
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5391003"
---
# <a name="design-details-item-tracking-design"></a>Detalles de diseño: Diseño de seguimiento de productos
En la primera versión de seguimiento de productos de [!INCLUDE[prod_short](includes/prod_short.md)] 2.60, los números de serie o de lote se registraban directamente en los movimientos de producto. Este diseño proporcionó información de disponibilidad completa y un seguimiento sencillo del historial de movimientos, pero carecía de flexibilidad y funcionalidad.  

A partir de [!INCLUDE[prod_short](includes/prod_short.md)] 3.00, la funcionalidad de seguimiento de productos pasa a ser una estructura de objetos independiente con vínculos complejos a documentos registrados y movimientos de producto. Este diseño era flexible y con muchas funcionalidades, pero los movimientos de seguimiento de producto no intervenían completamente en los cálculos de disponibilidad.  

Desde [!INCLUDE[prod_short](includes/prod_short.md)] 3,60, la funcionalidad del seguimiento de productos está integrada con el sistema de reservas, que controla la reserva, el seguimiento de pedidos y los mensajes de acciones. Para obtener más información, consulte "Detalles de diseño: Reserva, seguimiento de pedidos y mensajes de acciones” en “Detalles de diseño: Planificación de aprovisionamiento”.  

Este último diseño incorporar los movimientos de seguimiento de producto en los cálculos de disponibilidad total en todo el sistema, incluida la planificación, la fabricación y el almacenamiento. El antiguo concepto de transferir los números de serie y de lote a los movimientos de productos se vuelve a introducir para garantizar un acceso sencillo al historial de datos para realizar el seguimiento de productos. En relación con las mejoras del seguimiento de productos en [!INCLUDE[prod_short](includes/prod_short.md)] 3.60, el programa de reservas se ha ampliado a entidades de la red que no son pedidos, como diarios, facturas y abonos.  

Con la adición de los números de serie o de lote, el sistema de reservas controla los atributos de producto permanentes, a la vez que también controla los vínculos intermitentes entre el suministro y la demanda en forma de movimientos de seguimiento de pedidos y movimientos de reserva. Otra característica distinta de los números de serie o de lote comparados con los datos convencionales de reserva es el hecho de que se pueden registrar, tanto parcial como totalmente. Por lo tanto, la tabla **Mov. reserva** (T337) ahora funciona con una tabla relacionada, la tabla **Especificación seguimiento** (T336), que controla y muestra la suma de las cantidades de seguimiento de producto activas y registradas. Para obtener más información, consulte [Detalles de diseño: registros de seguimiento de productos históricos frente a activos](design-details-active-versus-historic-item-tracking-entries.md).  

En el diagrama siguiente se describe el diseño de la funcionalidad de seguimiento de productos en [!INCLUDE[prod_short](includes/prod_short.md)].  

![Ejemplo de flujo de seguimiento de artículos](media/design_details_item_tracking_design.png "Ejemplo de flujo de seguimiento de artículos")  

El objeto de registro central se ha rediseñado para controlar la subclasificación única de una línea de documento con el formato de números de serie o de lote, y se han agregado tablas de relación especiales para crear relaciones de uno a varios entre los documentos registrados y sus movimientos de producto y de valoración divididos.  

La codeunit 22, **Diario de productos – Línea de registro**, divide ahora el registro según los números de seguimiento de producto que se especifican en la línea de documento. Cada número de seguimiento de producto único en la línea crea su propio movimiento para el producto. Esto significa que el vínculo desde la línea de documento registrado a los movimientos de producto asociados ahora es una relación de uno a varios. Esta relación se controla mediante las siguientes tablas de relaciones de seguimiento de producto.  

|Campo|Descripción|  
|---------------|---------------------------------------|  
|**Relación mov. producto** (T6507)|Relaciona las líneas enviadas o recibidas a los movimientos de producto|  
|**Relación mov. valor** (T6508)|Relaciona las líneas facturadas con los movimientos de valoración|  

Para obtener más información, consulte [Detalles de diseño: Estructura de registro de seguimiento de productos](design-details-item-tracking-posting-structure.md).  

## <a name="see-also"></a>Consulte también  
[Detalles de diseño: Seguimiento de productos](design-details-item-tracking.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]