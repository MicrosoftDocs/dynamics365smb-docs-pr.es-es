---
title: Cómo bloquear ventas a productos de clientes desde el apartado de Ventas o Compras
description: En Business Central, un producto se puede marcar como bloqueado para ventas, bloqueado para compras o bloqueado para todos los propósitos.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: 832963169f4c81d65b105ca71722435554d8e262
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/01/2020
ms.locfileid: "3193760"
---
# <a name="block-customers"></a>Bloquear clientes
Puede bloquear a un cliente, por ejemplo, por insolvencia, para que el no pueda añadirse a los documentos de ventas o para que no se puedan registrar transacciones para el cliente.

Además de bloquear a un cliente, puede configurar las transacciones por cobrar para que el cliente esté en espera en conexión con los recordatorios. Para obtener más información, vea [Cobrar saldos pendientes](receivables-collect-outstanding-balances.md).   

La siguiente tabla describe las distintas opciones de bloqueo.  

|Opción|Description|  
|--------------------|------------|  
|**En blanco**|Se permiten las transacciones de este cliente.|
|**Envío**|No se pueden crear pedidos y envíos nuevos para este cliente. Los envíos existentes no facturados aún se pueden facturar.|  
|**Factura**|No se pueden crear facturas, pedidos ni envíos nuevos para este cliente. Los envíos existentes no facturados aún no se pueden facturar.|  
|**Todos**|No se permite ninguna transacción para este cliente, incluidos los pagos.|  

## <a name="to-block-a-customer"></a>Para bloquear a un cliente  
1. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Clientes** y luego elija el enlace relacionado.
2. Seleccione un cliente y, a continuación, elija la acción **Editar**.
3. Rellene el campo **Bloqueado** con una de las opciones descritas anteriormente.

## <a name="see-also"></a>Consulte también  
[Permite registrar nuevos clientes](sales-how-register-new-customers.md)  
[Cobrar saldos pendientes](receivables-collect-outstanding-balances.md)  
[Administrar cobros](receivables-manage-receivables.md)  
