---
title: Configurar y usar un flujo de trabajo de aprobación de compra
description: Este tutorial lo lleva a través de todas las etapas involucradas en la configuración y el uso de un flujo de trabajo de aprobación de compras en Business Central.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: null
ms.date: 03/11/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# Tutorial: Configurar y usar un flujo de trabajo de aprobación de compra

Puede automatizar el proceso de aprobar nuevos registros o registros modificados, como documentos, líneas de diario y fichas cliente, creando flujos de trabajo con pasos para las aprobaciones en cuestión.

Antes de crear flujos de trabajo de aprobación, debe configurar un aprobador y un aprobador sustituto para cada usuario de aprobación. Para definir qué registros de ventas y compras están cualificados para aprobar, también puede establecer límites de importe para los aprobadores. Las solicitudes de aprobación y otras notificaciones se pueden enviar como mensajes de correo electrónico o como notas internas. Para cada configuración de usuario de aprobación, también puede configurar cuándo reciben notificaciones.

> [!NOTE]
> Además de la funcionalidad de flujo de trabajo en [!INCLUDE[prod_short](includes/prod_short.md)], puede usar Power Automate para definir flujos de trabajo para eventos en [!INCLUDE[prod_short](includes/prod_short.md)]. Tenga en cuenta que, aunque son dos sistemas de flujo de trabajo independientes, cualquier plantilla de flujo de trabajo que cree con Power Automate se agrega a la lista de modelos de flujo de trabajo en la sección [!INCLUDE[prod_short](includes/prod_short.md)]. Obtenga más información en [Usar Business Central en un flujo de trabajo automatizado](across-how-use-financials-data-source-flow.md).  

Puede configurar y utilizar flujos de trabajo que vinculen tareas de procesos empresariales realizadas por distintos usuarios. Las tareas de sistema, como registros automáticos, se pueden incluir como pasos en los flujos de trabajo, antes o después de las tareas de usuario. Solicitar y conceder aprobaciones para crear registros nuevos son pasos habituales de un flujo de trabajo. Obtenga más información en [Flujo de trabajo](across-workflow.md).  

## Acerca de este tutorial

Este tutorial es un escenario que ilustra las siguientes tareas:  

- Configurar usuarios de aprobación  
- Configurar notificaciones para usuarios de aprobación  
- Modificar y activar un flujo de trabajo de aprobación  
- Solicitar aprobación de un pedido de compra (como Alicia)  
- Recibir una notificación a continuación aprobar la solicitud (como Pedro)  

## Historia

Sean es un superusuario en CRONUS y crea dos usuarios de aprobación. Uno es Alicia, que representa un agente de compras. El otro es él mismo Sean, que representa al aprobador de Alicia. Sean les concede a estos derechos de aprobación de compra ilimitados y especifica que recibirán las notificaciones por nota interna en cuanto se produzca un evento relevante. Por último, Pedro crea el flujo de trabajo de aprobación necesario como copia de la plantilla existente *Flujo de trabajo de aprobación de pedido de compra*, deja todas las condiciones de evento y las opciones de respuesta existentes sin cambiar y, a continuación, activa el flujo de trabajo.  

Para probar el flujo de aprobación, Pedro primero inicia sesión en [!INCLUDE[prod_short](includes/prod_short.md)] como Alicia y, a continuación, solicita aprobación de un pedido de compra. Después inicia sesión como él mismo, ve la nota en el Área de trabajo, sigue el vínculo a la solicitud de aprobación del pedido de compra y aprueba la solicitud.  

## Usuarios

Para poder configurar los usuarios de aprobación y su método de notificación, debe asegurarse de que existen esos usuarios en [!INCLUDE[prod_short](includes/prod_short.md)]: un usuario representará a Alicia. El otro usuario, usted, representará a Sean. Obtenga más información en [Crear usuarios de acuerdo con las licencias](ui-how-users-permissions.md).

### Configurar usuarios de aprobación

Cuando inicie sesión como usted mismo, configure a Alicia como un usuario de aprobación cuyo aprobador sea usted mismo. Configure sus derechos de aprobación y especifique cómo y cuándo se le notificarán las solicitudes de aprobación.  

#### Para configurarse a usted y a Alicia como usuarios de aprobación

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Config. usuario aprobación** y luego elija el enlace relacionado.  
2. En la página **Config. usuario aprobación**, seleccione la acción **Nuevo**.  

    > [!NOTE]  
    >  Debe configurar un aprobador para poder configurar usuarios que requieren la aprobación del aprobador. Eso significa que debe prepararse a sí mismo antes de poder preparar a Alicia.  

3. Configure a los dos usuarios de aprobación rellenando los campos tal como se describe en la tabla siguiente.  

    |Id. de usuario|Id. aprobador|Aprobación compra ilimitada|  
    |-------|-----------|---------------------------|  
    |USTED||Seleccionada|
    |ALICIA|USTED||

### Configuración de notificaciones

En este tutorial, el usuario recibe una notificación mediante una nota interna sobre las solicitudes para aprobar. Las notificaciones de aprobación también pueden enviarse por correo electrónico y puede agregar un paso de respuesta de flujo de trabajo que notifique al remitente cuando se aprueba o rechaza una solicitud. Obtenga más información en [Especificar cómo y cuándo recibir notificaciones](across-how-to-specify-when-and-how-to-receive-notifications.md).

#### Para configurar cómo y cuándo recibirá notificaciones

1. En la página **Config. usuario aprobación**, seleccione la línea para usted y después seleccione la acción **Configuración de notificación**.  
2. En la página **Configuración de notificación**, en el campo **Tipo de notificación**, elija **Aprobación**.  
3. En el campo **Método de notificación**, elija **Nota**.  
4. En la página **Configuración de notificación**, seleccione la acción **Programación de notificación**.  
5. En la página **Programación de notificación**, del campo **Periodicidad**, seleccione **Inmediatamente**.  

## Crear el flujo de trabajo de aprobación

Cree el flujo de aprobación de pedido de compra copiando los pasos de la plantilla **Flujo de trabajo de aprobación de pedido de compra**. Deje los pasos de flujo de trabajo existentes sin cambiar y, a continuación, active el flujo de trabajo.  

> [!TIP]
> Opcionalmente, agregue un paso de respuesta de flujo de trabajo para notificar al remitente cuando su solicitud sea aprobada o rechazada. Obtenga más información en [Especificar cómo y cuándo recibir notificaciones](across-how-to-specify-when-and-how-to-receive-notifications.md).

### Para crear y activar un flujo de trabajo de aprobación de pedido de compra

1. Elija el icono ![Bombilla que abre la característica Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Flujos de trabajo** y luego elija el vínculo relacionado.  
2. En la página **Flujos de trabajo**, seleccione **Acciones**, luego seleccione **Nuevo** y luego elija la acción **Nuevo flujo de trabajo de plantilla**.  
3. En la página **Plantillas de flujo de trabajo**, seleccione la plantilla de flujo de trabajo denominada **Flujo de trabajo de aprobación de pedido de compra**.  

   La página **Flujo de trabajo** se abre para un nuevo flujo de trabajo que contiene toda la información de la plantilla seleccionada. El valor del campo **Código** se amplía con *-01* para indicar que este es el primer flujo de trabajo creado a partir de la plantilla **Flujo de trabajo de aprobación de pedido de compra**.  
4. En el encabezado de la página **Flujo de trabajo**, active el control de alternancia **Habilitado**.  

## Usar el flujo de trabajo de aprobación

Utilice el nuevo flujo de trabajo de aprobación de pedido de compra iniciando sesión primero en [!INCLUDE[prod_short](includes/prod_short.md)] como Alicia para solicitar la aprobación de un pedido de compra. Después, inicie sesión como usted mismo, consulte la nota en el área de trabajo, siga el vínculo a la solicitud de aprobación y, a continuación, apruebe la solicitud.  

### Para solicitar aprobación de un pedido de compra como Alicia

1. Inicie sesión como Alicia.
2. Elija el icono ![Bombilla que abre la característica Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") icono, escriba **Pedidos de compra** y, a continuación, elija el vínculo relacionado.  
3. Seleccione la línea para abrir el *pedido de compra 106001*.  
4. En la página **Pedido de compra**, elija **Acciones**, luego, **Solicitar aprobación** y, después, la acción **Enviar solicitud aprobación**.  

Observe que el valor del campo **Estado** ha cambiado **Pendiente de aprobación**.  

### Para aprobar el pedido de compra como Pedro

1. Inicie sesión como Sean.
2. En el área de trabajo, en el área **Autoservicio**, elija **Solicitudes para aprobar**.
3. En la página **Solicitudes para aprobar**, seleccione la línea sobre el pedido de compra de Alicia y luego elija la acción **Aprobar**.  

El valor del campo **Estado** del pedido de compra de Alicia cambia **Lanzado**.  

Ya ha configurado y probado un flujo de trabajo de aprobación sencillo según los dos primeros pasos del **flujo de trabajo de aprobación de pedido de compra**. Puede ampliar fácilmente este flujo de trabajo para registrar automáticamente el pedido de compra de Alicia cuando Pedro lo apruebe. Para hacerlo, debe activar el **flujo de trabajo de factura de compra**, por lo que la respuesta a una factura de compra lanzada es registrarla. Primero debe cambiar la condición del evento en el primer paso del flujo de trabajo (compra) **Factura** a **Pedido**.  

La versión genérica de [!INCLUDE[prod_short](includes/prod_short.md)] incluye muchas plantillas de flujo de trabajo para ejemplos compatibles con el código de aplicación. La mayor parte de estas plantillas son de los flujos de trabajo de aprobación.  

Las variaciones del flujo de trabajo se definen rellenando los campos de las líneas de flujo de trabajo en listas fijas de valores de evento y respuesta que representan ejemplos de flujo de trabajo que admite el código de aplicación. Obtenga más información en [Crear flujos de trabajo](across-how-to-create-workflows.md).  

[!INCLUDE[workflow](includes/workflow.md)]

## Consulte también .

[Configurar usuarios de aprobación](across-how-to-set-up-approval-users.md)  
[Configurar notificaciones de flujo de trabajo](across-setting-up-workflow-notifications.md)  
[Crear flujos de trabajo de aprobación](across-how-to-create-workflows.md)  
[Usar flujos de trabajo de aprobación del producto](across-how-use-approval-workflows.md)  
[Flujo de trabajo](across-workflow.md)  
[Usar Business Central en un flujo de trabajo automatizado](across-how-use-financials-data-source-flow.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
