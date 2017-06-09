---
title: "Usar flujos de trabajo de aprobación | Documentos de Microsoft"
description: "Procedimiento: Usar flujos de trabajo de aprobación"
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: reject, delegate, request
ms.date: 04/25/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: ed08fdb7f78c9f6c338e287cd4ef42d7ce0cb72c
ms.contentlocale: es-es
ms.lasthandoff: 05/04/2017


---
# <a name="how-to-use-approval-workflows"></a>Procedimiento: Usar flujos de trabajo de aprobación
Cuando un registro, como un documento de compra o una ficha de cliente, necesita ser aprobado por alguien de su organización, enviará una solicitud de aprobación como parte de un flujo de trabajo. En función de la configuración del flujo de trabajo, el aprobador adecuado recibirá notificación sobre que el registro requiere su aprobación.

Los flujos de trabajo de aprobación se crean en la ventana **Flujo de trabajo**.

Los flujos de trabajo de aprobación más importantes para los documentos de compras y ventas, los diarios de pago y las fichas de clientes y productos están listos para iniciar como configuración asistida. Para obtener más información, vea [[!INCLUDE[d365fin_long](includes/d365fin_long_md.md)](index.md).

**Nota**: Esta funcionalidad que requiere que la experiencia esté definida en **Conjunto de aplicaciones**. Para obtener más información, consulte [Personalizar la experiencia de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-experiences.md).

## <a name="to-request-approval-of-a-record"></a>Para solicitar la aprobación de un registro
La siguiente tarea se realizado por un usuario de aprobación.

1. En la ventana que presenta el registro, seleccione la acción **Enviar solicitud de aprobación**.
2. Para ver todas las solicitudes de aprobación, en la esquina superior derecha, seleccione el icono **Buscar página o informe** ![Buscar página o informe](media/ui-search/search_small.png "Icono Buscar página o informe"), especifique **Movs. solic. aprobación** y elija el vínculo relacionado.

El estado del movimiento de aprobación se actualiza de **Creado** a **Abierto**. El estado del registro, por ejemplo una factura de compra, se actualiza de **Abierto** a **Pendiente de aprobación** y permanece bloqueado para el procesamiento hasta que todos los aprobadores hayan aprobado el registro.

Cuando el aprobador autoriza el registro, el estado cambia **Lanzados**. Podrá continuar con el resto de tareas del registro.

## <a name="to-cancel-requests-for-approval"></a>Para cancelar solicitudes de aprobación
La siguiente tarea se realizado por un usuario de aprobación con derechos de aprobación.

Puede que un cliente desee cambiar un pedido después de que éste haya sido enviado para su aprobación. En tal caso, puede cancelar el proceso de aprobación y realizar los cambios necesarios en el pedido antes de volver a solicitar aprobación.

- En la ventana que muestra el registro, seleccione la acción **Cancelar solicitud de aprobación**.

Una vez cancelada la solicitud de aprobación, el estado del movimiento de aprobación relacionado cambia a **Cancelado**. El estado del registro también se actualiza de **Aprobación pendiente** a **Abierto**. El proceso de aprobación puede entonces comenzar de nuevo.

## <a name="to-make-minor-changes-to-approved-records"></a>Para realizar cambios menores en los registros aprobados
Si desea realizar un cambio menor en un registro después de que se haya aprobado, puede volver a abrir el registro, realizar el cambio y, a continuación, lanzarlo. En el caso de cambios menores, se puede hacer con los botones **Volver a abrir** y **Lanzar**.

1. Abra la ventana que muestra el registro, por ejemplo una factura de compra, y seleccione la acción **Volver a abrir**.

    El campo **Estado documento** cambia a **Abierto**.
2. Realice los cambios necesarios en el registro, por ejemplo, la dirección del proveedor.
3. Seleccione la acción **Liberar**.

Cuando vuelva a abrir el registro de origen, el estado del movimiento de aprobación relacionado sigue siendo Aprobado en la ventana **Movimientos aprobación**.

## <a name="to-approve-or-reject-requests-for-approval"></a>Para aprobar o rechazar solicitudes de aprobación
La siguiente tarea se realizado por un usuario de aprobación con derechos de aprobación.

Puede procesar solicitudes de aprobación en la ventana **Solicitudes de aprobación**, por ejemplo aprobar múltiples solicitudes a la vez. Alternativamente, puede procesar cada solicitud en el registro relacionado, como en la ventana **Factura de compra**, seleccionando el enlace en la notificación que recibe.

1. En la esquina superior derecha, seleccione el icono **Buscar página o informe** ![Buscar página o informe](media/ui-search/search_small.png "Icono Buscar página o informe"), especifique **Solicitudes para aprobar** y elija el vínculo relacionado.
2. Seleccione una o varias líneas para el registro o los registros que desee aprobar o rechazar.
3. Seleccione las acciones **Aprobar**, **Rechazar** o **Delegar**.

Una vez aprobado o rechazado un registro, el estado de aprobación en el campo **Estado** cambia **Aprobado** o **Rechazado**.

Si hay configurada una jerarquía de aprobadores, el estado de registro será **Pendiente de aprobación** hasta que todos los aprobadores hayan aprobado el registro. El estado de registro cambiará a **Lanzados**.

Al mismo tiempo, el estado de aprobación cambia de **Creado** a **Abrir** en cuanto se cree una solicitud de aprobación para el registro. Si se rechaza la solicitud, el estado de aprobación cambia **Rechazado**. El estado permanece en **Abrir** o **Rechazado** hasta que todos los aprobadores hayan aprobado la solicitud.

## <a name="to-delegate-requests-for-approval"></a>Para delegar solicitudes de aprobación
La siguiente tarea se realizado por un usuario de aprobación con derechos de aprobación.

Para evitar que los documentos se acumulen o bloqueen el flujo de trabajo, el aprobador y el administrador de aprobación pueden delegar una solicitud de aprobación a un aprobador sustituto. El sustituto puede ser un sustituto designado, el aprobador directo o el administrador de aprobaciones, en ese orden de prioridad. Esta característica se utiliza normalmente si un aprobador se encuentra fuera de la oficina y no puede aprobar solicitudes antes de la fecha de vencimiento.

1. En la esquina superior derecha, seleccione el icono **Buscar página o informe** ![Buscar página o informe](media/ui-search/search_small.png "Icono Buscar página o informe"), especifique **Solicitudes para aprobar** y elija el vínculo relacionado.
2. Seleccione una o varias líneas de las solicitudes de aprobación que desea delegar a un aprobador sustituto y, a continuación, seleccione la acción **Delegar**.

Se envía una notificación para aprobar la solicitud al aprobador sustituto.

## <a name="to-manage-overdue-approval-requests"></a>Para gestionar solicitudes de aprobación vencidas
La siguiente tarea se realizado por un usuario de aprobación con derechos de aprobación.

Deberá recordar de forma periódica a los usuarios de flujo de trabajo de aprobación las solicitudes de aprobación vencidas en las que deben realizar alguna acción. Para ello se utiliza la función **Enviar notificaciones de aprobación vencidas**.

La función **Enviar notificaciones de aprobación vencidas** buscará todas las solicitudes de aprobación pendientes que hayan vencido. Cada aprobador que tenga al menos un movimiento de aprobación vencido recibirá una notificación con la lista de todas las solicitudes de aprobación vencidas. Esta notificación también se envía al aprobador y a todos los solicitantes de las aprobaciones vencidas. Esto resulta útil si el movimiento de aprobación vencido se debe delegar a un sustituto.

1. En la esquina superior derecha, seleccione el icono **Buscar página o informe** ![Buscar página o informe](media/ui-search/search_small.png "Icono Buscar página o informe"), especifique **Solicitudes de aprobación vencidas** y elija el vínculo relacionado.
2. En la ventana **Solicitudes de aprobación vencidas**, seleccione la acción **Seleccionar solicitudes de aprobación vencidas**.

## <a name="see-also"></a>Consulte también
[Ventas](sales-manage-sales.md)    
[Documentos entrantes](across-income-documents.md)  
[Compras](purchasing-manage-purchasing.md)  
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)](ui-work-product.md)

