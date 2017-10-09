---
title: "Detalles de diseño: Disponibilidad seguimiento de productos | Documentos de Microsoft"
description: "En este tema se discute cómo asegurarse de que las personas que procesan los pedidos pueden confiar en la disponibilidad de números de serie o números de lote."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: design, item, tracking, serial number, lot number, outbound documents
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: d196aa3c5176d040440be441e2573eac92891219
ms.contentlocale: es-es
ms.lasthandoff: 09/22/2017

---
# <a name="design-details-item-tracking-availability"></a>Detalles de diseño: Disponibilidad de seguimiento de productos
Las ventanas **Líneas seguimiento producto** y **Resumen seguimiento producto** proporcionan información de disponibilidad dinámica de los números de serie o de lote. El propósito de esto es aumentar la transparencia para los usuarios con respecto a los documentos de salida, como pedidos de venta, mostrándoles qué números de serie o cuántas unidades de un número de lote están asignado actualmente a otros documentos abiertos. De este modo se reduce la incertidumbre que provoca la doble asignación y transmite confianza en los procesadores de pedidos de que se pueden cumplir los números y las fechas de seguimiento de producto que han prometido en los pedidos de venta sin registrar. Para obtener más información, consulte [Detalles de diseño: Ventana de líneas de seguimiento de productos](design-details-item-tracking-lines-window.md).  
  
Al abrir la ventana **Líneas seguimiento producto**, se recuperan los datos de disponibilidad de las tablas **Mov. producto** y **Mov. reserva**, sin filtro de reserva. Cuando elige el campo **Nº serie** o **Nº lote**, se abre la ventana **Resumen seguimiento prod.** y muestra un resumen de la información de seguimiento de producto en la tabla **Mov. reserva**. El resumen contiene la siguiente información sobre cada número de serie o de lote en la línea de seguimiento de producto:  
  
|Campo|Description|  
|---------------------------------|---------------------------------------|  
|**Cantidad total**|La cantidad total del número de serie o lote actualmente en inventario.|  
|**Cdad. solicitada total**|La cantidad total del número de serie o lote solicitada actualmente en todos los documentos.|  
|**Cantidad pendiente actual**|La cantidad que se introduce en la instancia actual de la ventana **Líns. seguim. prod.** todavía no se ha transferido a la base de datos.|  
|**Cantidad total disponible**|Cantidad del número de serie o de lote que está disponible para que la solicite el usuario.<br /><br /> Esta cantidad se calcula a partir de otros campos de la ventana de la siguiente forma:<br /><br /> cantidad total – (cantidad total solicitada + cantidad actual pendiente).|  
  
> [!NOTE]  
>  También puede ver la información de la tabla anterior con la función **Seleccionar movs.** en la ventana **Líneas seguimiento producto**.  
  
Para mantener el rendimiento de la base de datos, los datos de disponibilidad se recuperan solo una vez de la base de datos cuando se abre la ventana **Líneas seguimiento producto** y se usa la función **Actualizar disponibilidad** en la ventana.  
  
## <a name="calculation-formula"></a>Tipo cálculo  
Tal como se describe en la tabla anterior, la disponibilidad de un número de serie o de lote determinado se calcula como sigue:  
  
* cantidad total disponible = cantidad en inventario – (todas las demandas + cantidad sin transferir a la base de datos)  
  
> [!IMPORTANT]  
>  Esta fórmula implica que en el cálculo de disponibilidad de número de serie o de lote solo se tiene en cuenta el inventario y se omiten las recepciones proyectadas. Por consiguiente, el aprovisionamiento que aún no se haya registrado en el inventario no afecta a la disponibilidad del seguimiento de productos, al contrario que la disponibilidad de los productos normal, donde se incluyen las recepciones proyectadas.  
  
## <a name="see-also"></a>Consulte también  
[Detalles de diseño: Seguimiento de productos](design-details-item-tracking.md)
