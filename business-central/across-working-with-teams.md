---
title: Trabajar con datos de Business Central en Microsoft Teams | Microsoft Docs
description: Aprenda a usar la aplicación Business Central para Microsoft Teams.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Teams, MS Teams, Microsoft Teams, Skype, Link, Microsoft 365, collaborate, collaboration, teamwork
ms.date: 10/08/2020
ms.author: jswymer
ms.openlocfilehash: fbe024f724f018aae6d3aeb5251281bf4c3bfbde
ms.sourcegitcommit: 4bca699d2a5ce182eb5572d72fac4fb478c4f293
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/12/2020
ms.locfileid: "3989431"
---
# <a name="working-with-business-central-data-in-microsoft-teams"></a>Trabajar con datos de Business Central en Microsoft Teams

[!INCLUDE [teams_preview.md](includes/teams_preview.md)]

[!INCLUDE [prodshort](includes/prodshort.md)] ofrece una aplicación que conecta Microsoft Teams a sus datos comerciales de [!INCLUDE [prodshort](includes/prodshort.md)], para que pueda compartir detalles rápidamente entre los miembros del equipo y responder más rápidamente a las consultas. En este artículo, aprenderá a usar la aplicación para compartir datos de [!INCLUDE [prodshort](includes/prodshort.md)] con compañeros de trabajo en una conversación de Teams.

## <a name="overview"></a>Panorama

La aplicación [!INCLUDE [prodshort](includes/prodshort.md)] le permite:

- Copie un vínculo a cualquier registro de Business Central y péguelo en una conversación de Teams para compartirlo con sus compañeros de trabajo. El vínculo lo expandirá para convertirse en una tarjeta compacta e interactiva que muestra información sobre el registro.
- Una vez en la conversación, usted y sus compañeros de trabajo pueden ver más detalles sobre el registro, editar datos y tomar medidas, sin salir de Teams.

[![Integración de Teams con Business Central](media/teams-intro-v3.png)](media/teams-intro-v3.png#lightbox)

## <a name="prerequisites"></a>Requisitos previos

- Tiene acceso a Microsoft Teams.
- Ha instalado la aplicación [!INCLUDE [prodshort](includes/prodshort.md)] en Teams. Para obtener más información, consulte [Instalar la aplicación [!INCLUDE [prodshort](includes/prodshort.md)] para Microsoft Teams](across-install-app-for-teams.md)

> [!NOTE]
> Todos los participantes de una conversación de Teams podrán ver las tarjetas de los registros de Business Central que envíe a la conversación. Pero, para ver más detalles sobre los registros, usando los botones **Detalles** o **Desplegable** de una tarjeta, necesitarán acceder a [!INCLUDE [prodshort](includes/prodshort.md)]. Para obtener más información, consulte [Administración de integración de Microsoft Teams](admin-teams-integration.md#minimum-requirements-1).
<!--
- People You and your coworkers have the following permissions in [!INCLUDE [prodshort](includes/prodshort.md)]
  - To paste a [!INCLUDE [prodshort](includes/prodshort.md)] link into a Teams conversation and have it expand into a card, you have to have at least permission to view the page and its data.
  - Once a card is submitted into a conversation, any user in that conversation can view that card without having permission to Business Central.
  - For other users to view more details from card, they must also have view permission, as a minimum, to the page and its data. If they want to change data, they'll need modify permissions.

  Setting up permissions is typically done by an administrator. For more information, see [Managing Microsoft Teams Integration](admin-teams-integration.md).-->

## <a name="include-a-business-central-card-in-a-teams-conversation"></a>Incluir una tarjeta Business Central en una conversación de Teams

1. Inicie sesión en [!INCLUDE [prodshort](includes/prodshort.md)] usando su navegador.
2. Abra el registro que quiere compartir.

    La aplicación está diseñada para mostrar páginas tipo tarjeta desde [!INCLUDE [prodshort](includes/prodshort.md)]. Por lo tanto, abra una página que muestre un solo registro, como un producto, un cliente o una orden de venta. No puede usarlo para centros de funciones o páginas que muestren varios registros en una lista.

3. Copie la URL completa de la barra de direcciones del navegador.

   ![Copiar la URL de Business Central desde el navegador](media/teams-url.png)
4. Vaya a Teams e inicie una conversación, que puede ser chatear con una persona, un grupo de personas o un canal de equipo.

    <!--Teams imposes a few limitations here eg. you cannot unfurl a link during a Voice/Video call :/ We should probably only mention this in a Troubleshooting section (and i hope it will also be fixed soon)-->
5. Pegue la URL en el cuadro donde agrega un mensaje.

   ![Pegar la URL de Business Central en Teams](media/teams-paste-url.png)
6. La primera vez que pegue un vínculo en una conversación, se le pedirá que inicie sesión en [!INCLUDE [prodshort](includes/prodshort.md)] y dar su consentimiento para que la aplicación recupere datos. Simplemente siga las instrucciones en pantalla.

    > [!NOTE]
    > Solo tiene que realizar este paso una vez.

7. Espere un momento mientras se genera una tarjeta en el cuadro de mensajes.

8. Cuando aparezca la tarjeta, revise el contenido de la tarjeta detenidamente en busca de información confidencial antes de enviar el mensaje. Este paso es importante porque, una vez que envía el mensaje, todos los participantes de la conversación pueden ver la tarjeta.

9. Si la tarjeta tiene buen aspecto, seleccione **Enviar** para enviarla a la conversación.

    > [!TIP]
    > Después de que aparezca la tarjeta y antes de seleccionar **Enviar**, puede eliminar la URL pegada si lo desea.

10. Para ver más detalles o realizar cambios en el registro, seleccione **Detalles**.

    La página de detalles es similar a la que vería en [!INCLUDE [prodshort](includes/prodshort.md)]. Pero está un tanto recortadada para Teams. Cuando haya terminado de ver y realizar cambios, cierre la ventana para volver a la conversación de Teams.

    > [!NOTE]
    > Los cambios que realice no se reflejarán en la tarjeta hasta la próxima vez que pegue su vínculo en una conversación.

## <a name="see-also"></a>Consulte también

[Descripción general de la integración de Business Central y Microsoft Teams](across-teams-overview.md)  
[Instalar la aplicación [!INCLUDE [prodshort](includes/prodshort.md)] para Microsoft Teams](across-install-app-for-teams.md)  
[Desarrollo para la integración de Teams](/dynamics365/business-central/dev-itpro/developer/devenv-develop-for-teams)  
[Introducción](product-get-started.md)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
