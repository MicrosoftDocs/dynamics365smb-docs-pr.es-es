---
author: brentholtorf
ms.topic: include
ms.date: 03/08/2024
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---

> [!NOTE]
> Cuando copia una empresa en un entorno donde Dataverse o la integración de ventas está habilitada, [!INCLUDE [prod_short](prod_short.md)] borra la siguiente configuración mientras copia a la empresa de destino:
>
> * Dataverse y Configuración de conexión dinámica para garantizar que la integración se reinicie correctamente en la empresa de destino.
> * Registros de integración para garantizar que la empresa de destino no apunte a registros que estén acoplados en la empresa de origen.
> * Trabajos de sincronización de integración para detener los trabajos de sincronización en segundo plano.
> * Los errores de sincronización, si existen, porque apuntan a errores en la empresa de origen y se considerarían simplemente ruido en la empresa de destino.