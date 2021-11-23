---
title: Cómo hacer el seguimiento de los paquetes
description: Utilice el servicio de rastreo de transportistas en Internet para rastrear paquetes y seguir el progreso de una entrega.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.search.keywords: rfq
ms.search.form: 103, 142, 800, 806
ms.date: 06/23/2021
ms.author: edupont
ms.openlocfilehash: 8c05c4a86e0bf9ace996dfc879b719324dc99593
ms.sourcegitcommit: a9e2aaee735870af566db68532cfa697347d68e0
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 11/04/2021
ms.locfileid: "7752371"
---
# <a name="track-packages"></a>Hacer un seguimiento de los paquetes
La mayoría de los agentes de envío brindan un servicio web que le permite rastrear el estado de sus paquetes mientras están en ruta. Esa información puede ser útil en muchos procesos comerciales, por ejemplo, al ofrecer servicio al cliente. Si utiliza uno o más de estos transportistas, puede introducir cierta información básica sobre ellos y utilizar su servicio de seguimiento directamente desde las páginas Histórico albaranes ventas, Histórico facturas ventas, Notas de abono de ventas registradas y Recibo de devolución registrado. Para obtener más información, vea [Configurar transportistas](sales-how-to-set-up-shipping-agents.md). 

El siguiente procedimiento muestra cómo rastrear un paquete desde un histórico albaranes venta, pero se aplican los mismos pasos para habilitar el seguimiento del paquete desde las páginas Factura de ventas registrada, Abono venta registrado e Histórico de recepción de devolución.  

## <a name="to-track-a-package"></a>Para hacer el seguimiento de un paquete

> [!NOTE]
> El siguiente procedimiento utiliza la página Histórico albaranes venta como ejemplo. Los pasos para rastrear un paquete son los mismos en las páginas Histórico facturas venta, Notas de abono de ventas registradas y Recibo de devolución registrado.

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Histórico albaranes venta** y luego elija el enlace relacionado.
2. Abra el envío que quiera seguir y, a continuación, seleccione la acción **Actualizar documento**.
3. En el campo **Nº seguimiento bulto** especifique el número de paquete que le ha dado el transportista. 
4. Asegúrese de que el agente de envío correcto y el nivel de servicio sean los correctos y luego cierre la página.
5. Elija la acción **Seguir envío** para abrir el servicio de seguimiento del paquete del transportista.

## <a name="see-also"></a>Consulte también

[Configurar transportistas](sales-how-to-set-up-shipping-agents.md)  
[Ccial](sales-manage-sales.md)  
[Configuración de ventas](sales-setup-sales.md)  
[Enviar documentos por correo electrónico](ui-how-send-documents-email.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]