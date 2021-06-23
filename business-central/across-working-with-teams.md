---
title: Compartir registros de Business Central en Microsoft Teams
description: Aprenda a usar la aplicación Business Central para Microsoft Teams.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Teams, MS Teams, Microsoft Teams, Skype, Link, Microsoft 365, collaborate, collaboration, teamwork, share records
ms.date: 05/19/2021
ms.author: jswymer
ms.openlocfilehash: 8add662badbc0d791d6a37d0feb4e3a756519f00
ms.sourcegitcommit: 5a916b0aa0a2eef0c22b5722a0af041757e6d7c2
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 05/19/2021
ms.locfileid: "6074592"
---
# <a name="sharing-business-central-records-in-microsoft-teams"></a>Compartir registros de Business Central en Microsoft Teams

[!INCLUDE [online_only](includes/online_only.md)]

[!INCLUDE [prod_short](includes/prod_short.md)] ofrece una aplicación que conecta Microsoft Teams a sus datos comerciales de [!INCLUDE [prod_short](includes/prod_short.md)], para que pueda compartir detalles rápidamente entre los miembros del equipo y responder más rápidamente a las consultas. En este artículo, aprenderá a usar la aplicación para compartir registros de [!INCLUDE [prod_short](includes/prod_short.md)], como clientes, pedidos de ventas facturas, con compañeros de trabajo en una conversación de Teams.

## <a name="overview"></a>Panorama

La aplicación [!INCLUDE [prod_short](includes/prod_short.md)] le permite:

- Copie un vínculo a cualquier registro de Business Central y péguelo en una conversación de Teams para compartirlo con sus compañeros de trabajo. La aplicación expandirá el vínculo para convertirse en una tarjeta compacta e interactiva que muestra información sobre el registro.
- Una vez en la conversación, usted y sus compañeros de trabajo pueden ver más detalles sobre el registro, editar datos y tomar medidas, sin salir de Teams.

[![Integración de Teams con Business Central](media/teams-intro-v3.png)](media/teams-intro-v3.png#lightbox)

## <a name="prerequisites"></a>Requisitos previos

- Tiene acceso a Microsoft Teams.
- Ha instalado la aplicación [!INCLUDE [prod_short](includes/prod_short.md)] en Teams. Para obtener más información, consulte [Instalar la aplicación [!INCLUDE [prod_short](includes/prod_short.md)] para Microsoft Teams](across-install-app-for-teams.md)

> [!NOTE]
> Todos los participantes de una conversación de Teams podrán ver las tarjetas de los registros de Business Central que envíe a la conversación. Pero, para ver más detalles sobre los registros, usando los botones **Detalles** o **Desplegable** de una tarjeta, necesitarán acceder a [!INCLUDE [prod_short](includes/prod_short.md)]. Para obtener más información, consulte [Administración de integración de Microsoft Teams](admin-teams-integration.md#minimum-requirements-1).

## <a name="include-a-business-central-card-in-a-teams-conversation"></a>Incluir una tarjeta Business Central en una conversación de Teams

1. Inicie sesión en [!INCLUDE [prod_short](includes/prod_short.md)] usando su navegador.
2. Abra el registro que quiere compartir.

    La aplicación está diseñada para mostrar páginas tipo tarjeta desde [!INCLUDE [prod_short](includes/prod_short.md)]. Por lo tanto, abra una página que muestre un solo registro, como un producto, un cliente o una orden de venta. No puede usarlo para centros de funciones o páginas que muestren varios registros en una lista.

3. Copie la URL completa de la barra de direcciones del navegador.

   ![Copiar la URL de Business Central desde el navegador](media/teams-url-v2.png)
4. Vaya a Teams e inicie una conversación, que puede ser chatear con una persona, un grupo de personas o un canal de equipo.

    <!--Teams imposes a few limitations here eg. you cannot unfurl a link during a Voice/Video call :/ We should probably only mention this in a Troubleshooting section (and i hope it will also be fixed soon)-->
5. Pegue la URL en el cuadro de mensaje donde redacta los mensajes.

   ![Pegar la URL de Business Central en Teams](media/teams-paste-url-v2.png)
6. La primera vez que pegue un vínculo en una conversación, se le pedirá que inicie sesión en [!INCLUDE [prod_short](includes/prod_short.md)] y dar su consentimiento para que la aplicación recupere datos. Simplemente siga las instrucciones en pantalla.

    > [!NOTE]
    > Solo tiene que realizar este paso una vez.

7. Espere un momento mientras se genera una tarjeta en el cuadro de mensajes.

8. Cuando aparezca la tarjeta, revise el contenido de la tarjeta detenidamente en busca de información confidencial antes de enviar el mensaje. Este paso es importante porque, una vez que envía el mensaje, todos los participantes de la conversación pueden ver la tarjeta.

9. Si la tarjeta tiene buen aspecto, seleccione **Enviar** para enviarla a la conversación.

    > [!TIP]
    > Después de que aparezca la tarjeta y antes de seleccionar **Enviar**, puede eliminar la URL pegada si lo desea.

10. Para ver más detalles o realizar cambios en el registro mostrado en la tarjeta, seleccione **Detalles**. Para obtener más información, consulte la sección siguiente.

## <a name="view-card-details"></a>Ver detalles de tarjeta

Una vez que se ha enviado una tarjeta a una conversación, todos los participantes con los [permisos adecuados](admin-teams-integration.md#permissions) puede seleccionar **Detalles** para abrir una ventana que muestra más información sobre el registro, y posiblemente realizar cambios en el registro. No importa si eres el que envía la tarjeta o el que la recibe. La función **Detalles** es especialmente útil para los destinatarios, ya que les proporciona rápidamente información concisa y específica sobre el registro, en lugar de tener que escanear el registro completo.

La ventana de detalles es similar a la que vería en el registro de [!INCLUDE [prod_short](includes/prod_short.md)]. Pero está un tanto recortadada para Teams. Cuando haya terminado de ver y realizar cambios, cierre la ventana para volver a la conversación de Teams.

Aquí hay un par de cosas que debe tener en cuenta al trabajar con los detalles de la tarjeta:

- Para abrir los detalles de la tarjeta, los usuarios deben tener permiso de lectura en la página y sus datos en [!INCLUDE [prod_short](includes/prod_short.md)].
- Las tarjetas en los chats de Teams no se actualizan automáticamente a los cambios. Cualquier cambio que guarde en un registro en la ventana de detalles se guarda en [!INCLUDE [prod_short](includes/prod_short.md)]. Pero la tarjeta en Teams no mostrará los cambios en la conversión hasta que vuelva a pegar el enlace.

Para obtener más información sobre cómo trabajar con tarjetas y detalles de tarjetas, consulte [Preguntas frecuentes de Teams](teams-faq.md).

## <a name="see-also"></a>Consulte también

[Descripción general de la integración de Business Central y Microsoft Teams](across-teams-overview.md)  
[Instalar la aplicación [!INCLUDE [prod_short](includes/prod_short.md)] para Microsoft Teams](across-install-app-for-teams.md)  
[P+F de Teams](teams-faq.md)  
[Consejos para la solución de problemas de Teams](admin-teams-troubleshooting.md)  
[Desarrollo para la integración de Teams](/dynamics365/business-central/dev-itpro/developer/devenv-develop-for-teams)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  


[!INCLUDE[footer-include](includes/footer-banner.md)]