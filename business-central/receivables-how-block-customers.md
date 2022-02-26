---
title: Cómo bloquear ventas a clientes
description: Si es necesario, puede bloquear la inclusión de un cliente en documentos de ventas y otras transacciones de ventas.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: a5ac7b1cd9d58c91584c2777442094bace0673fd
ms.sourcegitcommit: a7cb0be8eae6ece95f5259d7de7a48b385c9cfeb
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 07/08/2021
ms.locfileid: "6436028"
---
# <a name="block-customers"></a>Bloquear clientes
Puede bloquear a un cliente, por ejemplo, por insolvencia, para que el no pueda añadirse a los documentos de ventas o para que no se puedan registrar transacciones para el cliente.

Además de bloquear a un cliente, puede configurar las transacciones por cobrar para que el cliente esté en espera en conexión con los recordatorios. Para obtener más información, vea [Cobrar saldos pendientes](receivables-collect-outstanding-balances.md).   

La siguiente tabla describe las distintas opciones de bloqueo de clientes.  

|Opción|Descripción|  
|--------------------|------------|  
|**En blanco**|Se permiten las transacciones de este cliente.|
|**Envío**|No se pueden crear pedidos y envíos nuevos para este cliente. Los envíos existentes no facturados aún se pueden facturar.|  
|**Factura**|No se pueden crear facturas, pedidos ni envíos nuevos para este cliente. Los envíos existentes no facturados aún no se pueden facturar. Aún puede enviar recordatorios y documentos de interés al cliente.|  
|**Todo**|No se permite ninguna transacción para este cliente, incluidos los pagos.|  

## <a name="to-block-a-customer"></a>Para bloquear a un cliente  
1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Clientes** y luego elija el enlace relacionado.
2. Seleccione un cliente y, a continuación, elija la acción **Editar**.
3. En el campo **Bloqueado**, elija qué bloquear, como se describe en la tabla anterior.

## <a name="see-also"></a>Consulte también  
[Permite registrar nuevos clientes](sales-how-register-new-customers.md)  
[Cobrar saldos pendientes](receivables-collect-outstanding-balances.md)  
[Administrar cobros](receivables-manage-receivables.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]