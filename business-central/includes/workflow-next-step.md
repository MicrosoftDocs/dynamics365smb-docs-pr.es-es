---
author: brentholtorf
ms.topic: include
ms.date: 03/27/2024
ms.author: bholtorf
ms.service: dynamics-365-business-central
---

> [!IMPORTANT]
> Cuando cambia el evento when para un paso del flujo de trabajo, las respuestas también cambian. A veces, las respuestas de otros cuando los eventos se refieren a estas respuestas como el siguiente paso en el flujo de trabajo. Después de cambiar un evento when, verifique que los siguientes pasos para sus eventos then sean correctos.  
>
> Por ejemplo, la plantilla de flujo de trabajo **Flujo de trabajo de aprobación del proveedor** tiene un evento principal cuando **Se solicita la aprobación de un proveedor**. Este evento when tiene un **Enviar solicitud de aprobación para el registro y crear una notificación** tras la respuesta, que además de las respuestas hace referencia. Si cambia el evento when **Se solicita la aprobación de un proveedor** a, por ejemplo, **Se cambia un registro de proveedor**, la respuesta then se borra junto con las referencias.
>
> Las respuestas then para los eventos when **Se delega una solicitud de aprobación** y **Se aprueba una solicitud de aprobación.** (con **En condición** de **Aprobaciones pendientes >0**) son ejemplos de dónde cambiar un evento primario when puede causar problemas. Luego sus respuestas tienen un siguiente paso que se refiere a la respuesta then **Enviar solicitud de aprobación para el registro y crear una notificación** del evento when **Se solicita la aprobación de un proveedor**. Porque la respuesta then para el evento when **Se solicita la aprobación de un proveedor** ya no está disponible, los eventos when con sangría no funcionarán como se esperaba.
>
> Deberá especificar los siguientes pasos para las respuestas de los eventos when que hicieron referencia al evento when cambiado.