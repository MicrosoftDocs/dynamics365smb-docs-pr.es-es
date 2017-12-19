---
title: "Tutorial: Configuración y uso de un flujo de trabajo de aprobación de compra | Documentos de Microsoft"
description: "Puede automatizar el proceso de aprobar nuevos registros o registros modificados, como documentos, líneas de diario y fichas cliente, creando flujos de trabajo con pasos para las aprobaciones en cuestión. Antes de crear flujos de trabajo de aprobación, debe configurar un aprobador y un aprobador sustituto para cada usuario de aprobación. También puede establecer límites de cantidad de aprobadores para definir qué registros de venta y de compra pueden aprobar. Las solicitudes de aprobación y otras notificaciones se pueden enviar como mensajes de correo electrónico o como notas internas. Para cada configuración de usuario de aprobación, también puede configurar cuándo reciben notificaciones."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: a49e50213f808fb72b43dfa22a34833b306ef12d
ms.openlocfilehash: 7ce4b45d740e50bba8256e72fcf43c70ea85922c
ms.contentlocale: es-es
ms.lasthandoff: 12/14/2017

---
# <a name="walkthrough-setting-up-and-using-a-purchase-approval-workflow"></a>Tutorial: Configuración y uso de un flujo de trabajo de aprobación de compra
Puede automatizar el proceso de aprobar nuevos registros o registros modificados, como documentos, líneas de diario y fichas cliente, creando flujos de trabajo con pasos para las aprobaciones en cuestión. Antes de crear flujos de trabajo de aprobación, debe configurar un aprobador y un aprobador sustituto para cada usuario de aprobación. También puede establecer límites de cantidad de aprobadores para definir qué registros de venta y de compra pueden aprobar. Las solicitudes de aprobación y otras notificaciones se pueden enviar como mensajes de correo electrónico o como notas internas. Para cada configuración de usuario de aprobación, también puede configurar cuándo reciben notificaciones.  

 Puede configurar y utilizar flujos de trabajo que vinculen tareas de procesos empresariales realizadas por distintos usuarios. Las tareas de sistema, como registros automáticos, se pueden incluir como pasos en los flujos de trabajo, antes o después de las tareas de usuario. Solicitar y conceder aprobaciones para crear registros nuevos son pasos habituales de un flujo de trabajo. Para obtener más información, consulte [Flujo de trabajo](across-workflow.md).  

## <a name="about-this-walkthrough"></a>Acerca de este tutorial  
En este tutorial se ilustran las siguientes tareas:  

-   Configurar usuarios de aprobación (incluida la configuración de un usuario en Windows y en [!INCLUDE[d365fin](includes/d365fin_md.md)]).  
-   Configurar notificaciones para usuarios de aprobación.  
-   Modificar y activar un flujo de trabajo de aprobación.  
-   Iniciar la cola de proyectos que envía notificaciones.  
-   Solicitar aprobación de un pedido de compra, como Alicia.  
-   Recibir una notificación a continuación aprobar la solicitud, como Pedro.  

## <a name="prerequisites"></a>Requisitos previos  
Para completar este tutorial, necesitará la empresa de demostración CRONUS International Limited.

## <a name="story"></a>Historia  
Sean es un superusuario de CRONUS en su propio ordenador.  

Crea dos usuarios de aprobación. Uno es Alicia, que representa un agente de compras. El otro es él mismo, que representa al aprobador de Alicia. Pedro se concede derechos de aprobación de compra ilimitados y especifica que recibirá las notificaciones por la nota interna en cuanto se produzca un evento relevante. Por último, Pedro crea el flujo de trabajo de aprobación necesario como copia de la plantilla existente de flujo de trabajo de aprobación de pedido de compra, deja todas las condiciones de evento y las opciones de respuesta existentes sin cambiar y, a continuación, activa el flujo de trabajo.  

Para probar el flujo de aprobación, Pedro primero inicia sesión en [!INCLUDE[d365fin](includes/d365fin_md.md)] como Alicia y, a continuación, solicita aprobación de un pedido de compra. Después inicia sesión como él mismo, ve la nota en su área de trabajo, sigue el vínculo a la solicitud de aprobación del pedido de compra y aprueba la solicitud.  

## <a name="setting-up-the-sample-data"></a>Configuración de los datos de ejemplo  
Debe crear un nuevo usuario en el equipo local y en [!INCLUDE[d365fin](includes/d365fin_md.md)] que represente a Alicia, el cual seleccionará posteriormente como usuario de aprobación. Su propia cuenta de usuario representará a Pedro.  

### <a name="to-add-alicia-as-a-user-on-the-local-computer"></a>Para agregar a Alicia como usuario en el equipo local  

1.  Elija **Inicio** y, en el cuadro **Buscar programas y archivos**, introduzca **Editar usuarios y grupos locales** y, a continuación, elija el vínculo relacionado.  
2.  Abra la carpeta **Usuarios**.  
3.  En la pestaña **Acciones**, elija **Nuevo usuario**.  
4.  En el campo **Nombre usuario**, introduzca Alicia.  
5.  En los campos **Contraseña** y **Confirmar contraseña**, introduzca una contraseña válida.  
6.  Anule la selección de la casilla **El usuario debe cambiar la contraseña en el siguiente inicio de sesión**.  
7.  Cierre la ventana **Usuarios y grupos locales**.  

### <a name="to-add-alicia-as-a-user-in-included365finincludesd365finmdmd"></a>Para agregar a Alicia como usuario en [!INCLUDE[d365fin](includes/d365fin_md.md)]  
1.  Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Usuarios** y, a continuación, seleccione el vínculo relacionado.  
2.  En la ventana **Usuarios de Windows**, de la pestaña **Inicio**, del grupo **Nuevo**, elige **Nuevo**.  
3.  En la ventana **Ficha de usuario** , en el campo **Nombre usuario** , introduzca a Alicia.  
4.  En los campos **Nombre de usuario de Windows**, seleccione el botón AssistEdit.  
5.  En la ventana **Seleccionar usuario o grupo**, en el campo **Escriba el nombre de objeto que seleccionar**, introduzca Alicia y seleccione el botón **Comprobar nombres**.  
6.  Cuando [NOMBRE DE EQUIPO]ALICIA aparezca en el campo, seleccione el botón **Aceptar**.  
7.  En la ficha desplegable **Conjuntos de permisos de usuario**, en el campo **Conjunto de permisos**, especifique **SUPER**.  
8.  En el campo **Empresa**, seleccione **CRONUS International Ltd.**  
9. Elija el botón **Aceptar**.  

## <a name="setting-up-approval-users"></a>Configuración de usuarios de aprobación  
Mediante el usuario de Windows que acaba de crear, configure Alicia como usuario de aprobación cuyo aprobador sea usted mismo. Configure sus derechos de aprobación y especifique cómo y cuándo se le notificarán las solicitudes de aprobación.  

### <a name="to-set-up-yourself-and-alicia-as-approval-users"></a>Para configurarse a usted y a Alicia como usuarios de aprobación  
1.  Elija el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Configuración usuario aprobación** y, a continuación, seleccione el vínculo relacionado.  
2.  En la ventana **Config. usuario aprobación**, en la pestaña **Inicio**, en el grupo **Nuevo**, elija **Nuevo**.  

    > [!NOTE]  
    >  Debe configurar un aprobador para poder configurar usuarios que requieren la aprobación del aprobador. Así, antes de configurar a Alicia, debe configurarse a sí mismo.  

3.  Configure a los dos usuarios de aprobación rellenando los campos tal como se describe en la tabla siguiente.  

    |Id. de usuario|Id. aprobador|Aprobación compra ilimitada|  
    |-------------|-----------------|---------------------------------|  
    |[NOMBRE DE EQUIPO][USTED]||Seleccionado|  
    |[NOMBRE DE EQUIPO]ALICIA|[NOMBRE DE EQUIPO][USTED]||  

## <a name="setting-up-notifications"></a>Configuración de notificaciones  
Especifique cómo y cuándo se le notificarán las solicitudes de aprobación.  

### <a name="to-set-up-how-and-when-you-are-notified"></a>Para configurar cómo y cuándo recibirá notificaciones  
1.  En la ventana **Config. usuario aprobación**, seleccione la línea correspondiente a usted y, en la pestaña **Inicio**, en el grupo **Procesar**, seleccione **Configuración de notificación**.  
2.  En la ventana **Configuración de notificación**, en el campo **Tipo de notificación**, especifique **Aprobación**.  
3.  Seleccione el campo **Código plantilla notificación** y después pulse el botón **Avanzado**.  
4.  En la ventana **Plantillas de notificación**, de la pestaña **Inicio**, en el grupo **Administrar**, elija **Editar lista**.  
5.  En la línea de la plantilla de APROBACIÓN, en el campo **Método de notificación**, introduzca **Nota**.  
6.  Elija el botón **Aceptar**.  
7.  En la ventana **Configuración de notificación**, de la pestaña **Inicio**, del grupo **Proceso**, elija **Programación de notificaciones**.  
8.  En la ventana **Programación de notificación**, del campo **Repetición**, elija **Inmediatamente**.  
9. Elija el botón **Aceptar**.  

## <a name="creating-the-approval-workflow"></a>Creación del flujo de aprobación  
 Cree el flujo de aprobación de pedido de compra copiando los pasos de la plantilla de flujo de trabajo de aprobación de pedido de compra. Deje los pasos de flujo de trabajo existentes sin cambiar y, a continuación, active el flujo de trabajo.  

### <a name="to-create-and-enable-a-purchase-order-approval-workflow"></a>Para crear y activar un flujo de trabajo de aprobación de pedido de compra  
1.  Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Flujos de trabajo** y, a continuación, seleccione el vínculo relacionado.  
2.  En la ventana **Flujos de trabajo**, de la pestaña **Acciones**, del grupo **General**, elija **Crear flujo de trabajo desde una plantilla**.  
3.  En la pestaña **Acciones** de la pestaña **General**, elige **Crear flujo de trabajo desde una plantilla**. Se abre la ventana **Plantillas de flujo de trabajo**.  
4.  Selecciona la plantilla de flujo de trabajo denominada Flujo de trabajo de aprobación de pedido de compra y haz clic en el botón **Aceptar**.  

    La ventana **Flujo de trabajo** se abre para un nuevo flujo de trabajo que contiene toda la información de la plantilla seleccionada. El valor del campo **Código** se amplía con “-01” para indicar que este es el primer flujo de trabajo creado a partir de la plantilla de flujo de trabajo denominada Flujo de trabajo de aprobación de pedido de compra.  
5.  En el encabezado de la ventana **Flujo de trabajo**, seleccione la casilla **Habilitado**.  

## <a name="starting-a-notification-job-queue"></a>Inicio de una cola de proyectos de notificación  
Asegúrese de que hay una cola de proyectos configurada en la instalación para gestionar las notificaciones de flujo de trabajo.  

### <a name="to-start-the-notify-job-queue"></a>Para iniciar la cola de proyectos de NOTIFICACIÓN  
1.  Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Colas de proyectos** y, a continuación, seleccione el vínculo relacionado.  
2.  En la ventana **Colas de proyectos**, seleccione la línea de la cola de proyecto de NOTIFICAR y después, en la pestaña **Inicio** del grupo **Proceso**, elija **Iniciar cola de proyecto**.  

## <a name="using-the-approval-workflow"></a>Uso del flujo de trabajo de aprobación  
Utilice el nuevo flujo de trabajo de aprobación de pedido de compra registrándose primero en [!INCLUDE[d365fin](includes/d365fin_md.md)] como Alicia para solicitar la aprobación de un pedido de compra. Después, inicie sesión como usted mismo, consulte la nota en el área de trabajo, siga el vínculo a la solicitud de aprobación y, a continuación, apruebe la solicitud.  

Para iniciar sesión en [!INCLUDE[d365fin](includes/d365fin_md.md)] como diferentes usuarios, utilizará la función **Ejecutar como otro usuario**.  

### <a name="to-log-into-included365finincludesd365finmdmd-as-alicia"></a>Para iniciar sesión en [!INCLUDE[d365fin](includes/d365fin_md.md)] como Alicia  

1.  Para el cliente web [!INCLUDE[d365fin](includes/d365fin_md.md)], en el botón de inicio del explorador de la página web, presione Mayús y haga con el botón secundario al mismo tiempo; a continuación, elija **Ejecutar como otro usuario**.  

    Para el cliente de Windows [!INCLUDE[d365fin](includes/d365fin_md.md)], en el botón de inicio del programa, presione Mayús y haga con el botón secundario al mismo tiempo; a continuación, elija **Ejecutar como otro usuario**.  

2.  En la ventana **Seguridad de Windows**, introduzca [NOMBRE DE EQUIPO]ALICIA y la contraseña requerida.  

### <a name="to-request-approval-of-a-purchase-order-as-alicia"></a>Para solicitar aprobación de un pedido de compra como Alicia  

1.  Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Pedidos de compra** y, a continuación, seleccione el vínculo relacionado.  
2.  Seleccione la línea para el pedido de compra 104001 y, a continuación, en la pestaña **Inicio**, en el grupo **Administrar**, elija **Editar**.  
3.  En la ventana **Pedido de compra**, de la pestaña **Acciones** del grupo **Aprobación**, elija **Enviar solicitud de aprobación**.  

    Observe que el valor del campo **Estado** ha cambiado **Pendiente de aprobación**.  

4.  Cerrar [!INCLUDE[d365fin](includes/d365fin_md.md)]  

### <a name="to-approve-the-purchase-order-as-sean"></a>Para aprobar el pedido de compra como Pedro  

1.  Abra [!INCLUDE[d365fin](includes/d365fin_md.md)] como lo hace generalmente. El programa se abrirá con usted como usuario.  
2.  En el área de trabajo, en la ventana **Mis notificaciones**, busque una nueva nota de Alicia.  

    > [!NOTE]  
    >  Aunque le repetición de notificación está definida en **Inmediatamente**, la nota llegará aproximadamente un minuto después de que Alicia haya enviado la solicitud de aprobación. Esto se debe a la frecuencia de la repetición predeterminada de la función de cola de proyectos.  

3.  Cuando la nota aparezca en la ventana **Mis notificaciones**, elija el valor **Movimiento aprobación: XX, XX** en el campo **Página**. La ventana **Solicitudes para aprobar** se abre con la petición de Alicia del pedido de compra resaltado.  
4.  En la ventana **Solicitudes para aprobar**, en la pestaña **Inicio**, en el grupo **Proceso**, elija **Aprobar**.  

    El valor del campo **Estado** del pedido de compra de Alicia cambia **Lanzado**.  

Ya ha configurado y probado un flujo de trabajo de aprobación sencillo según los dos primeros pasos del flujo de trabajo de aprobación de pedido de compra. Puede ampliar fácilmente este flujo de trabajo para registrar automáticamente el pedido de compra de Alicia cuando Pedro lo apruebe. Para hacerlo, debe activar el flujo de trabajo de factura de compra, en el que la respuesta a una factura de compra lanzada es registrarla. Primero debe cambiar la condición del evento en el primer paso del flujo de trabajo (compra) **Factura** a **Pedido**.  

La versión genérica de [!INCLUDE[d365fin](includes/d365fin_md.md)] incluye varias plantillas de flujo de trabajo para ejemplos compatibles con el código de aplicación. La mayor parte de ellos son de los flujos de trabajo de aprobación. Para obtener más información, consulte Plantilla de flujo de trabajo.  

Las variaciones del flujo de trabajo se definen rellenando los campos de las líneas de flujo de trabajo en listas fijas de valores de evento y respuesta que representan ejemplos de flujo de trabajo que admite el código de aplicación. Para obtener más información, consulte [Procedimiento: Crear flujos de trabajo](across-how-to-create-workflows.md).  

Si una situación de negocio requiere un evento de flujo de trabajo o respuesta no compatibles, un asociado de Microsoft tiene que implementarlos personalizando el código de aplicación. Para obtener más información, consulte [Tutorial: Implementación de nuevos eventos y respuestas de flujo de trabajo](/dynamics-nav/Walkthrough--Implementing-New-Workflow-Events-and-Responses) en la ayuda para desarrolladores e informáticos.  

## <a name="see-also"></a>Consulte también  
[Procedimiento: Configurar usuarios de aprobación](across-how-to-set-up-approval-users.md)   
[Configurar notificaciones de flujo de trabajo](across-setting-up-workflow-notifications.md)   
[Procedimiento: Crear flujos de trabajo](across-how-to-create-workflows.md)   
[Procedimiento: Usar flujos de trabajo de aprobación](across-how-use-approval-workflows.md)   
[Flujo de trabajo](across-workflow.md)

