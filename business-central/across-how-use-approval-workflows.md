---
title: Aprobar o rechazar documentos en los flujos de trabajo
description: 'Solicite, rechace o delegue una aprobación de, por ejemplo, una compra o venta, como parte de un flujo de trabajo.'
author: SorenGP
ms.topic: conceptual
ms.workload: na
ms.search.keywords: 'reject, delegate, request'
ms.search.form: '654, 662, 1500,'
ms.date: 09/12/2022
ms.author: edupont
---
# <a name="how-to-use-approval-workflows"></a><a name="how-to-use-approval-workflows"></a>Cómo usar flujos de trabajo de aprobación

Cuando un registro, como un documento de compra o una ficha de cliente, necesita ser aprobado por alguien de su organización, enviará una solicitud de aprobación como parte de un flujo de trabajo. En función de la configuración del flujo de trabajo, el aprobador adecuado recibirá notificación sobre que el registro requiere su aprobación.

Los flujos de trabajo de aprobación se crean en la página **Flujo de trabajo**. También debe configurar usuarios de aprobación, incluidos los límites de cantidad relevantes, en la página **Config. usuario aprobación**. Obtenga más información en [Configurar flujos de trabajo de aprobación](across-set-up-workflows.md).  

Además de los flujos de trabajo de aprobación descritos en este artículo, puede realizar otras tareas de flujo de trabajo. Obtenga más información en [Usar flujos de trabajo de aprobación](across-use-workflows.md).

Los flujos de trabajo de aprobación más importantes para los documentos de compras y ventas, los diarios de pago y las fichas de clientes y productos están listos para iniciar como guías. Obtenga más información en [Preparación para hacer negocios](ui-get-ready-business.md).

## <a name="request-a-record-approval"></a><a name="request-a-record-approval"></a>Solicitar una aprobación de registro

La siguiente tarea se realizado por un usuario de aprobación.

1. En la página que presenta el registro, seleccione la acción **Enviar solicitud de aprobación**.
2. Para ver todas sus solicitudes de aprobación, elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Movs. solic. aprobación** y, a continuación, elija el vínculo relacionado.  

El estado del movimiento de aprobación se actualiza de **Creado** a **Abierto**. El estado del registro, por ejemplo una factura de compra, se actualiza de **Abierto** a **Pendiente de aprobación** y permanece bloqueado para el procesamiento hasta que todos los aprobadores hayan aprobado el registro.

Cuando todos los aprobadores necesarios autorizan el registro, el estado cambia **Lanzados**. Podrá continuar trabajando con el registro.

## <a name="cancel-approval-requests"></a><a name="cancel-approval-requests"></a>Cancelar solicitudes de aprobación

La siguiente tarea se realizado por un usuario de aprobación con derechos de aprobación.

Puede que un cliente desee cambiar un pedido después de que éste haya sido enviado para su aprobación. En tal caso, puede cancelar el proceso de aprobación, realizar los cambios necesarios en el pedido y después volver a solicitar aprobación.

- En la página que muestra el registro, seleccione la acción **Cancelar solicitud de aprobación**.

Una vez cancelada la solicitud de aprobación, el estado del movimiento de aprobación relacionado cambia a **Cancelado**. El estado del registro también se actualiza de **Aprobación pendiente** a **Abierto**. En este punto, el proceso de aprobación puede entonces comenzar de nuevo.

## <a name="approve-or-reject-approval-requests"></a><a name="approve-or-reject-approval-requests"></a>Aprobar o rechazar solicitudes de aprobación

La siguiente tarea se realizado por un usuario de aprobación con derechos de aprobación.

Puede procesar solicitudes de aprobación en la página **Solicitudes de aprobación**, incluyendo la aprobación de múltiples solicitudes a la vez. Alternativamente, puede aprobar registros individuales eligiendo el vínculo en la notificación que recibe.

1. Elija el icono ![Bombilla que abre la característica Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Solicitudes para aprobar** y, a continuación, elija el vínculo relacionado.
2. Seleccione una o varias líneas del registro o los registros que desee aprobar o rechazar.
3. Seleccione las acciones **Aprobar**, **Rechazar** o **Delegar**.

Una vez aprobado o rechazado un registro, el estado de aprobación en el campo **Estado** cambia **Aprobado** o **Rechazado** respectivamente.

Si hay configurada una jerarquía de aprobadores, el estado de registro es **Pendiente de aprobación** hasta que todos los aprobadores solicitados hayan aprobado el registro. El estado de registro cambia a **Lanzados**.

Al mismo tiempo, el estado de aprobación cambia de **Creado** a **Abrir** en cuanto se cree una solicitud de aprobación para el registro. Si se rechaza la solicitud, el estado de aprobación cambia **Rechazado**. El estado permanece en **Abrir** o **Rechazado** hasta que todos los aprobadores hayan aprobado la solicitud.

## <a name="delegate-approval-requests"></a><a name="delegate-approval-requests"></a>Delegar solicitudes de aprobación

La siguiente tarea se realizado por un usuario de aprobación con derechos de aprobación.

Para evitar que los registros se acumulen o bloqueen el flujo de trabajo, el aprobador y el administrador de aprobación pueden delegar una solicitud de aprobación a un aprobador sustituto. El sustituto puede ser un sustituto designado, el aprobador directo o el administrador de aprobaciones, en ese orden de prioridad. Esta característica se utiliza normalmente si un aprobador no está disponible o no puede aprobar solicitudes antes de la fecha de vencimiento.

1. Elija el icono ![Bombilla que abre la característica Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Solicitudes para aprobar** y, a continuación, elija el vínculo relacionado.
2. Seleccione una o varias líneas de las solicitudes de aprobación que desea delegar a un aprobador sustituto y, a continuación, seleccione la acción **Delegar**.

Se envía una notificación para aprobar la solicitud al aprobador sustituto.

## <a name="manage-overdue-approval-requests"></a><a name="manage-overdue-approval-requests"></a>Gestionar solicitudes de aprobación vencidas

La siguiente tarea se realizado por un usuario de aprobación con derechos de aprobación.

A intervalos regulares tendrá que recordar a los usuarios del flujo de trabajo de aprobación las solicitudes de aprobación vencidas; para ello debe usar la función **Enviar notificaciones de aprobación vencidas**.

La función **Enviar notificaciones de aprobación vencidas** buscará todas las solicitudes de aprobación pendientes que hayan vencido. Cada aprobador con al menos un movimiento de aprobación vencido recibirá una notificación con la lista de todas las solicitudes de aprobación vencidas. Esta notificación también se envía al aprobador y a todos los solicitantes de las aprobaciones vencidas. Este último paso ayuda si el movimiento de aprobación vencido se debe delegar a un sustituto.

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Solicitudes de aprobación vencidas** y luego elija el enlace relacionado.
2. En la página **Solicitudes de aprobación vencidas**, seleccione la acción **Seleccionar solicitudes de aprobación vencidas**.

## <a name="see-related-microsoft-training"></a><a name="see-related-microsoft-training"></a>Consultar la [formación de Microsoft](/training/modules/use-approval-workflows/) relacionada

## <a name="see-also"></a><a name="see-also"></a>Consulte también .

[Usar flujos de trabajo de aprobación](across-use-workflows.md)  
[Flujo de trabajo](across-workflow.md)  
[Configurar usuarios de aprobación](across-how-to-set-up-approval-users.md)  
[Ccial](sales-manage-sales.md)  
[Documentos entrantes](across-income-documents.md)  
[Compras](purchasing-manage-purchasing.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
