---
author: brentholtorf
ms.topic: include
ms.date: 05/30/2023
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---

Cuando configure usuarios para los flujos de trabajo de aprobación, es importante que un mismo usuario no sea a la vez solicitante y aprobador en un grupo de usuarios de un flujo de trabajo. Cuando un usuario es solicitante y aprobador, las aprobaciones funcionan para él de la siguiente manera:

* Sus solicitudes siempre se aprueban automáticamente.
* Si hay varios aprobadores, solo los aprobadores con un número de secuencia superior en el grupo de usuarios del flujo de trabajo pueden cambiar el estado de una solicitud a Aprobado. Los aprobadores con un número de secuencia inferior pueden aprobar solicitudes; sin embargo, sus aprobaciones no afectarán el estado de una solicitud.