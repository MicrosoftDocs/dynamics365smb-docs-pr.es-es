---
title: 'Detalles de diseño: Seguimiento del producto en el almacén | Documentos de Microsoft'
description: El control de los números de serie y de lote es principalmente una tarea de almacén y, por lo tanto, todos los documentos de almacén de entrada y de salida tienen una funcionalidad estándar para asignar y seleccionar números de seguimiento de productos. No obstante, dado que el programa de reservas se basa en los movimientos de producto, no se admiten totalmente los documentos de actividad del almacén que registren solo movimientos de almacén.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: design, item, tracking, serial number, lot number, outbound documents
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: 02a87bc61fbadae4392800f84adbc176bfb87b23
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/01/2020
ms.locfileid: "3185017"
---
# <a name="design-details-item-tracking-in-the-warehouse"></a>Detalles de diseño: Seguimiento de productos en el almacén
El control de los números de serie y de lote es principalmente una tarea de almacén y, por lo tanto, todos los documentos de almacén de entrada y de salida tienen una funcionalidad estándar para asignar y seleccionar números de seguimiento de productos.  

No obstante, dado que el programa de reservas se basa en los movimientos de producto, no se admiten totalmente los documentos de actividad del almacén que registren solo movimientos de almacén. Dado que las reservas y los números de seguimiento de productos se pueden administrar solo en el nivel de almacén, no en el nivel de ubicación ni de zona, la página **Líns. seguim. prod.** no se puede abrir desde documentos de actividad de almacén. Lo mismo se aplica a la página **Reservas**.  

Después de añadir un número de serie o de lote a un elemento en una ubicación de almacén, puede moverse y volver a clasificarse libremente en el almacén mediante una estructura independiente de seguimiento del producto que esté no relacionado con el programa de reservas. A los campos **Nº serie** y **Nº lote** se obtiene acceso directamente en las líneas del documento de almacén. Cuando el número de serie o de lote participa en el registro de salida, se sincroniza con el sistema de reservas como parte de un ajuste de ubicación normal. Para obtener más información, consulte [Detalles de diseño: Integración con inventario](design-details-integration-with-inventory.md).  

No obstante, el programa de reservas tiene en cuenta las actividades de almacén cuando calcula la disponibilidad. Por ejemplo, los productos que están asignados a selecciones o registrados como seleccionados no se pueden reservar. Para obtener más información, consulte [Detalles de diseño: Disponibilidad en el almacén](design-details-availability-in-the-warehouse.md).

## <a name="see-also"></a>Consulte también  
[Detalles de diseño: Seguimiento de productos](design-details-item-tracking.md)  
[Detalles de diseño: Integración con inventario](design-details-integration-with-inventory.md)  
[Detalles de diseño: Disponibilidad en el almacén](design-details-availability-in-the-warehouse.md)  
[Detalles de diseño: Diseño de seguimiento de productos](design-details-item-tracking-design.md)
