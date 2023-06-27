---
title: Compartir registros de Business Central en Microsoft Teams
description: Aprenda a usar la aplicación Business Central para Microsoft Teams.
author: jswymer
ms.topic: how-to
ms.service: dynamics365-business-central
ms.reviewer: jswymer
ms.search.keywords: 'Teams, MS Teams, Microsoft Teams, Skype, Link, Microsoft 365, collaborate, collaboration, teamwork, share records'
ms.date: 16/18/2023
ms.author: jswymer
ms.custom: bap-template
---

# <a name="sharing-business-central-records-and-page-links-in-microsoft-teams" />Compartir registros y enlaces de página de Business Central en Microsoft Teams

[!INCLUDE [online_only](includes/online_only.md)]

[!INCLUDE [prod_short](includes/prod_short.md)] ofrece un par de formas de compartir datos de Business Central directamente en una conversación de Microsoft Teams:

<!-- 
## <a name="overview" />Overview
In this article, you'll learn how to use the app to share [!INCLUDE [prod_short](includes/prod_short.md)] records, like a customer, sales order, or invoice, with coworkers in a Teams conversation.
The [!INCLUDE [prod_short](includes/prod_short.md)] app lets you:
[!INCLUDE [prod_short](includes/prod_short.md)] offers an app that connects Microsoft Teams to your business data in [!INCLUDE [prod_short](includes/prod_short.md)], so you can quickly share details across team members and respond faster to inquiries. In this article, you'll learn how to use the app to share [!INCLUDE [prod_short](includes/prod_short.md)] records, like a customer, sales order, or invoice, with coworkers in a Teams conversation.

-->
- Con la aplicación [!INCLUDE [prod_short](includes/prod_short.md)] instalada en Teams, puede incluir una tarjeta interactiva del registro de Business Central en una conversación de Teams.

<!--   Copy a link from any Business Central record, like a customer or sales order, then paste the link into a Teams conversation. The app connects Microsoft Teams to your business data in [!INCLUDE [prod_short](includes/prod_short.md)]. It then expands the link into a compact, interactive card that displays information about the record. Once in the conversation, you and coworkers can view more details about the record, edit data, and take action&mdash;without leaving Teams.

  [![Teams integration with Business Central.](media/teams-intro-v3.png)](media/teams-intro-v3.png#lightbox)-->

- Con o sin la aplicación de [!INCLUDE [prod_short](includes/prod_short.md)] instalada, puede compartir un vínculo desde páginas de Business Central hasta una conversación de Teams.

  <!-- ![!The Share menu displayed on a card.](media/teams-share-link.png "The Share menu displayed on a card.")-->

En las siguientes secciones se describen los distintos métodos en detalle.

## <a name="include-and-view-a-business-central-card-in-a-teams-conversation" />Incluir y ver una tarjeta Business Central en una conversación de Teams

Con la aplicación Business Central para Teams, puede copiar un vínculo de cualquier registro de Business Central, como un cliente o un pedido de ventas, y pegar el vínculo en una conversación de Teams. La aplicación conecta Microsoft Teams a los datos de su empresa en [!INCLUDE [prod_short](includes/prod_short.md)]\. A continuación expande el vínculo para convertirse en una tarjeta compacta e interactiva que muestra información sobre el registro. Una vez en la conversación, usted y sus compañeros de trabajo pueden ver más detalles sobre el registro, editar datos y tomar medidas, sin salir de Teams.

[![Integración de Teams con Business Central.](media/teams-intro-vBC20.png)](media/teams-intro-vBC20.png#lightbox)

### <a name="prerequisites" />Requisitos previos

- Tiene acceso a Microsoft Teams.
- Ha instalado la aplicación [!INCLUDE [prod_short](includes/prod_short.md)] en Teams. Para obtener más información, consulte [Instalar la aplicación [!INCLUDE [prod_short](includes/prod_short.md)] para Microsoft Teams](across-install-app-for-teams.md)

> [!NOTE]
> Todos los participantes de una conversación de Teams podrán ver las tarjetas de los registros de Business Central que envíe a la conversación. Pero, para ver más detalles sobre los registros, usando los botones **Detalles** o **Desplegable** de una tarjeta, necesitarán acceder a [!INCLUDE [prod_short](includes/prod_short.md)]. Para obtener más información, consulte [Administración de integración de Microsoft Teams](admin-teams-integration.md#minimum-requirements-1).

### <a name="include-a-business-central-card-in-a-teams-conversation" />Incluir una tarjeta Business Central en una conversación de Teams

1. Inicie sesión en [!INCLUDE [prod_short](includes/prod_short.md)] usando su navegador.
2. Abra el registro que quiere compartir.

    La aplicación está diseñada para mostrar una ficha para casi cualquier tipo de página de [!INCLUDE [prod_short](includes/prod_short.md)]. Sin embargo, brinda la mejor experiencia cuando se usa para páginas que muestran un solo registro, como un artículo, un cliente o un pedido de ventas.
3. Copie el vínculo a la página.

    Existen dos formas de copiar el vínculo. La forma más sencilla y preferida es seleccionar **Compartir** ![Icono Compartir en Business Central](media/share-icon.png) > **Copiar vínculo**. La otra forma es copiar la URL completa de la barra de direcciones del navegador.

    [![Copiar la URL de Business Central desde el navegador.](media/teams-copy-link.png)](media/teams-copy-link.png#lightbox)
4. Vaya a Teams e inicie una conversación, que puede ser chatear con una persona, un grupo de personas o un canal de equipo.
5. Pegue el vínculo (URL) en el cuadro de mensaje donde redacta los mensajes.

    ![Pegar la URL de Business Central en Teams.](media/teams-paste-url-v2.png)

    > [!TIP]
    > Si recibe un mensaje como: *Business Central quiere mostrar una vista previa de este vínculo.*, significa que no tiene instalada la aplicación Business Central para Teams. Para instalar la aplicación, seleccione **Mostrar vista previa** y siga las instrucciones.

    > [!NOTE]
    > En función de la versión de Business Central, la primera vez que pegue un vínculo en una conversación, se le puede pedir que inicie sesión en [!INCLUDE [prod_short](includes/prod_short.md)] y dé su consentimiento para que la aplicación recupere datos. Simplemente siga las instrucciones en pantalla. Solo tendrá que hacer este paso una vez.
6. Espere un momento mientras se genera una tarjeta en el cuadro de mensajes.
7. Cuando aparezca la tarjeta, revise el contenido de la tarjeta detenidamente en busca de información confidencial antes de enviar el mensaje. Este paso es importante porque, una vez que envía el mensaje, todos los participantes de la conversación pueden ver la tarjeta.
8. Si la tarjeta tiene buen aspecto, seleccione **Enviar** para enviarla a la conversación.

    > [!TIP]
    > Después de que aparezca la tarjeta y antes de seleccionar **Enviar**, puede eliminar la URL pegada si lo desea.
9. Para ver más detalles o realizar cambios en el registro mostrado en la tarjeta, seleccione **Detalles**. Para obtener más información, consulte la sección siguiente.

### <a name="view-card-details" />Ver detalles de tarjeta

Una vez que se ha enviado una tarjeta a una conversación, todos los participantes con los [permisos adecuados](admin-teams-integration.md#permissions) puede seleccionar **Detalles** para abrir una ventana que muestra más información sobre el registro, y posiblemente realizar cambios en el registro. No importa si eres el que envía la tarjeta o el que la recibe. La característica **Detalles** es especialmente útil para los destinatarios, ya que les proporciona rápidamente información concisa y específica sobre el registro.

La ventana de detalles es similar a lo que vería en [!INCLUDE [prod_short](includes/prod_short.md)], pero se centra en la página o el registro del que trata la ficha. Cuando haya terminado de ver y realizar cambios, cierre la ventana para volver a la conversación de Teams.

Aquí hay un par de cosas que debe tener en cuenta al trabajar con los detalles de la tarjeta:

- Para abrir los detalles de la tarjeta, los usuarios deben tener permiso de lectura en la página y sus datos en [!INCLUDE [prod_short](includes/prod_short.md)]\.
- Las tarjetas en los chats de Teams no se actualizan automáticamente a los cambios. Cualquier cambio que guarde en un registro en la ventana de detalles se guarda en [!INCLUDE [prod_short](includes/prod_short.md)]\. Pero la tarjeta en Teams no mostrará los cambios en la conversión hasta que vuelva a pegar el enlace.

Para obtener más información sobre cómo trabajar con tarjetas y detalles de tarjetas, consulte [Preguntas frecuentes de Teams](teams-faq.md).

## <a name="share-a-link-to-page-from-business-central-to-teams" /><a name="share-link"></a>Compartir un vínculo a una página de Business Central a Teams

Directamente desde la mayoría de las páginas de colección, como la página **Productos** y páginas de detalles, como la tarjeta **Productos**, puede enviar un vínculo a la página a destinatarios específicos en una conversación de Teams. Por ejemplo, puede compartir un enlace a una vista filtrada de sus registros. Los destinatarios pueden seleccionar el enlace para abrir la página en [!INCLUDE [prod_short](includes/prod_short.md)]\.

[![!El menú Compartir mostrado en una tarjeta.](media/teams-share-link-v2.png "El menú Compartir mostrado en una tarjeta.")](media/teams-share-link-v2.png#lightbox)

### <a name="prerequisites-1" />Requisitos previos

- Tiene acceso a Microsoft Teams.
- (Opcional) Ha instalado la aplicación [!INCLUDE [prod_short](includes/prod_short.md)] en Teams. 

  Con la aplicación instalada, los mensajes que envíe con el enlace también incluirán una tarjeta compacta para la página. Para obtener más información sobre cómo instalar la aplicación, consulte [Instalar la aplicación [!INCLUDE [prod_short](includes/prod_short.md)] para Microsoft Teams](across-install-app-for-teams.md).

### <a name="share-a-link" />Compartir un enlace

1. En [!INCLUDE [prod_short](includes/prod_short.md)]\,, abra la página que quiera compartir.
2. En la parte superior de la página, elija el icono ![!Acción Compartir con otras aplicaciones en páginas.](media/share-icon.png) , luego **Compartir con Teams**.
3. Si se le solicita, inicie sesión en Teams con su nombre de usuario y contraseña.
4. En la página **Compartir con Teams**, escriba el nombre de una persona, grupo o canal al que desea enviar el mensaje.
5. El cuadro de mensaje incluirá un enlace a la página. Si la aplicación [!INCLUDE [prod_short](includes/prod_short.md)] está instalada para Teams, también aparecerá una tarjeta para el registro o la página vinculados en el cuadro de mensaje.

   Agregue más información si lo desea, luego elija **Compartir**.
6. El enlace ahora se ha compartido. Si quiere ir a la conversación, elija **Ir a Teams**.

## <a name="see-also" />Consulte también .

[Descripción general de la integración de Business Central y Microsoft Teams](across-teams-overview.md)  
[Instalar la aplicación [!INCLUDE [prod_short](includes/prod_short.md)] para Microsoft Teams](across-install-app-for-teams.md)  
[P+F de Teams](teams-faq.md)  
[Búsqueda de clientes, proveedores y otros contactos desde Microsoft Teams](across-search-contacts-teams.md)  
[Cambiar la empresa y otras configuraciones en Teams](across-teams-settings.md)  
[Consejos para la solución de problemas de Teams](admin-teams-troubleshooting.md)  
[Desarrollo para la integración de Teams](/dynamics365/business-central/dev-itpro/developer/devenv-develop-for-teams)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]

[!INCLUDE[footer-include](includes/footer-banner.md)]
