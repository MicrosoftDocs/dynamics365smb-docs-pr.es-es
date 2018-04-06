---
title: "Estado asignación y estado de reparación | Documentos de Microsoft"
description: "Obtenga información sobre la relación entre el estado de reparación de los elementos de servicio y el estado de asignación de las entradas de asignación."
services: project-madeira
documentationcenter: 
author: bholtorf
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: resources, allocation, status, repairs
ms.date: 08/28/2017
ms.author: bholtorf
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 4020910008e47fdf5a7e4626aa84e0f64cf0905f
ms.contentlocale: es-es
ms.lasthandoff: 03/22/2018

---
# <a name="allocation-status-and-repair-status-of-service-items"></a>Estado de asignación y estado de reparación de productos de servicio
El estado de reparación y el estado de asignación de los movimientos de asignación de los productos de servicio están relacionados en Gestión de servicios. El estado de asignación cambia cuando se modifica el estado de reparación del producto de servicio a **Terminado** o **Parcialmente servido**, y cuando se convierte una oferta de servicio en un pedido de servicio. El estado de reparación del producto de servicio cambia cuando se cancela la asignación de producto de servicio o se reasigna el producto de servicio a otro recurso. Puede ver el estado de reparación de productos de servicio en la ventana **Tareas servicio** y actualizar el estado de reparación en el campo **Cód. estado reparación** en la ventana **Hoja trabajo prod. serv.** Puede ver el estado de asignación en el campo **Estado** de la ventana **Asignaciones recurso**.  
  
## <a name="changing-repair-status"></a>Modificar el estado de reparación  
Cuando se modifica el estado de reparación de un producto de servicio de una línea de producto de servicio, se realiza una búsqueda del movimiento de asignación correspondiente al producto de servicio cuyo estado sea **Activo**. Si se encuentra el movimiento de asignación, se actualiza su estado en una de las siguientes formas:  
  
* Si cambia el estado de reparación a **Terminado**, se modifica el estado de asignación de **Activo** a **Terminado**.  
* Si cambia el estado de reparación a **Parcialmente servido**, es decir, se ha realizado parte del servicio, o **Remitido**, no se ha realizado ningún servicio, el programa modifica el estado de asignación de **Activo** a **Reasignación necesaria**.  
* Cuando se crea un movimiento de asignación de pedido de servicio que indica que no se ha asignado ningún recurso, se establece el campo **Estado** de la ventana **Asignaciones recurso** como **Inactivo**.  
* Se establece el estado del movimiento de asignación como **Cancelado** cuando se reasigna el producto de servicio remitido en el movimiento de asignación de pedido de servicio, lo que indica que el recurso o grupo de recursos asignado no ha intentado realizar la tarea de servicio.  
  
El estado de asignación indica cuando ha terminado el proceso de servicio o cuando resulta necesario otro recurso para finalizar el servicio del producto de servicio.  
  
## <a name="converting-service-quotes-to-service-orders"></a>Convertir ofertas de servicios a pedidos de servicios  
Cuando se convierte una oferta de servicio en un pedido de servicio, el pedido de servicio, los productos de servicio del pedido y los movimientos de asignación se actualizan de la siguiente forma:  
  
* Se cambia el estado de reparación de los productos de servicio a **Inicial**.  
* El estado de pedido de servicio cambiará a **Pendiente**.  
* Se realiza una búsqueda de movimientos de asignación para todos los productos de servicio del pedido de servicio cuyo estado sea **Activo**. Si se encuentran los movimientos de asignación, el estado de asignación cambia de **Activo** a **Reasignación necesaria**.  
  
## <a name="canceling-allocations"></a>anular asignaciones  
Cuando se cancela una asignación de un producto de servicio, [!INCLUDE[d365fin](includes/d365fin_md.md)] actualiza el estado de asignación del movimiento de asignación correspondiente de **Activo** a **Necesidad de reasignación**.

El estado de reparación del producto de servicio del movimiento de asignación se actualiza de la siguiente forma:  
  
* Si el estado de reparación es **Inicial**, el estado de reparación cambia a **Remitido** (no se ha iniciado ningún servicio).  
* Si el estado de reparación es **En proceso**, el estado de reparación cambia a **Parcialmente servido** (se ha realizado parte del servicio).  
  
## <a name="reallocating-an-active-allocation-entry"></a>Reasignar un movimiento de asignación activo  
Cuando se reasigna un producto de servicio de un movimiento de asignación **Activo**, el movimiento de asignación se actualiza de la siguiente forma:  
  
* Si se inició el servicio cuando estaba **Activa** la asignación (es decir, si el estado de reparación del producto de servicio del movimiento se cambió a **En proceso**), el estado de asignación cambia de **Activo** a **Terminado**.  
* Si no se inició el servicio cuando la asignación era **Activo**, el estado de asignación cambia de **Activo** a **Cancelado**.  
  
El estado de reparación del producto de servicio del movimiento de asignación se actualiza como si se hubiese cancelado la asignación:  
  
* Si el estado de reparación es **Inicial**, el estado de reparación cambia a **Remitido** (no se ha iniciado ningún servicio).  
* Si el estado de reparación es **En proceso**, el estado de reparación cambia a **Parcialmente servido** (se ha realizado parte del servicio).  
  
Se creará una nueva entrada de asignación con el nuevo recurso y con el estado **Activo**.  
  
## <a name="reallocating-a-service-item"></a>Reasignar un artículo de servicio  
Cuando se reasigna un producto de servicio de un movimiento de asignación cuyo estado es **Reasignación necesaria**, el movimiento de asignación se actualiza de la siguiente forma:  
  
* Si se inició el servicio cuando estaba **Activa** la asignación (es decir, si el estado de reparación del producto de servicio del movimiento se cambió a **En proceso**), el estado de asignación cambia de **Reasignación necesaria** a **Terminado**.  
* Si no se inició el servicio cuando la asignación era **Activo**, el estado de asignación cambia de **Reasignación necesaria** a **Cancelado**.  
  
Se creará una nueva entrada de asignación con el nuevo recurso y con el estado **Activo**.  
  
## <a name="see-also"></a>Consulte también  
[Configurar asignaciones de recursos](service-how-setup-resource-allocation.md)  
[Asignar recursos](service-how-to-allocate-resources.md)  


