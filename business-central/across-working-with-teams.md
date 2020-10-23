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
# <a name="working-with-business-central-data-in-microsoft-teams"></a><span data-ttu-id="1cd39-103">Trabajar con datos de Business Central en Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="1cd39-103">Working with Business Central Data in Microsoft Teams</span></span>

[!INCLUDE [teams_preview.md](includes/teams_preview.md)]

<span data-ttu-id="1cd39-104">[!INCLUDE [prodshort](includes/prodshort.md)] ofrece una aplicación que conecta Microsoft Teams a sus datos comerciales de [!INCLUDE [prodshort](includes/prodshort.md)], para que pueda compartir detalles rápidamente entre los miembros del equipo y responder más rápidamente a las consultas.</span><span class="sxs-lookup"><span data-stu-id="1cd39-104">[!INCLUDE [prodshort](includes/prodshort.md)] offers an app that connects Microsoft Teams to your business data in [!INCLUDE [prodshort](includes/prodshort.md)], so you can quickly share details across team members and respond faster to inquiries.</span></span> <span data-ttu-id="1cd39-105">En este artículo, aprenderá a usar la aplicación para compartir datos de [!INCLUDE [prodshort](includes/prodshort.md)] con compañeros de trabajo en una conversación de Teams.</span><span class="sxs-lookup"><span data-stu-id="1cd39-105">In this article, you'll learn how to use the app to share [!INCLUDE [prodshort](includes/prodshort.md)] data with coworkers in a Teams conversation.</span></span>

## <a name="overview"></a><span data-ttu-id="1cd39-106">Panorama</span><span class="sxs-lookup"><span data-stu-id="1cd39-106">Overview</span></span>

<span data-ttu-id="1cd39-107">La aplicación [!INCLUDE [prodshort](includes/prodshort.md)] le permite:</span><span class="sxs-lookup"><span data-stu-id="1cd39-107">The [!INCLUDE [prodshort](includes/prodshort.md)] app lets you:</span></span>

- <span data-ttu-id="1cd39-108">Copie un vínculo a cualquier registro de Business Central y péguelo en una conversación de Teams para compartirlo con sus compañeros de trabajo.</span><span class="sxs-lookup"><span data-stu-id="1cd39-108">Copy a link to any Business Central record and paste it into a Teams conversation to share with your coworkers.</span></span> <span data-ttu-id="1cd39-109">El vínculo lo expandirá para convertirse en una tarjeta compacta e interactiva que muestra información sobre el registro.</span><span class="sxs-lookup"><span data-stu-id="1cd39-109">The link will expand that into a compact, interactive card that displays information about the record.</span></span>
- <span data-ttu-id="1cd39-110">Una vez en la conversación, usted y sus compañeros de trabajo pueden ver más detalles sobre el registro, editar datos y tomar medidas, sin salir de Teams.</span><span class="sxs-lookup"><span data-stu-id="1cd39-110">Once in the conversation, you and coworkers can view more details about the record, edit data, and take action - without leaving Teams.</span></span>

<span data-ttu-id="1cd39-111">[![Integración de Teams con Business Central](media/teams-intro-v3.png)](media/teams-intro-v3.png#lightbox)</span><span class="sxs-lookup"><span data-stu-id="1cd39-111">[![Teams integration with Business Central](media/teams-intro-v3.png)](media/teams-intro-v3.png#lightbox)</span></span>

## <a name="prerequisites"></a><span data-ttu-id="1cd39-112">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="1cd39-112">Prerequisites</span></span>

- <span data-ttu-id="1cd39-113">Tiene acceso a Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="1cd39-113">You have access to Microsoft Teams.</span></span>
- <span data-ttu-id="1cd39-114">Ha instalado la aplicación [!INCLUDE [prodshort](includes/prodshort.md)] en Teams.</span><span class="sxs-lookup"><span data-stu-id="1cd39-114">You've installed the [!INCLUDE [prodshort](includes/prodshort.md)] app in Teams.</span></span> <span data-ttu-id="1cd39-115">Para obtener más información, consulte [Instalar la aplicación [!INCLUDE [prodshort](includes/prodshort.md)] para Microsoft Teams](across-install-app-for-teams.md)</span><span class="sxs-lookup"><span data-stu-id="1cd39-115">For more information, see [Install the [!INCLUDE [prodshort](includes/prodshort.md)] App for Microsoft Teams](across-install-app-for-teams.md)</span></span>

> [!NOTE]
> <span data-ttu-id="1cd39-116">Todos los participantes de una conversación de Teams podrán ver las tarjetas de los registros de Business Central que envíe a la conversación.</span><span class="sxs-lookup"><span data-stu-id="1cd39-116">All participants in a Teams conversation will be able to view cards for Business Central records that you submit to the conversation.</span></span> <span data-ttu-id="1cd39-117">Pero, para ver más detalles sobre los registros, usando los botones **Detalles** o **Desplegable** de una tarjeta, necesitarán acceder a [!INCLUDE [prodshort](includes/prodshort.md)].</span><span class="sxs-lookup"><span data-stu-id="1cd39-117">But to view more details about records, by using the **Details** or **Pop-out** buttons on a card, they'll need access to [!INCLUDE [prodshort](includes/prodshort.md)].</span></span> <span data-ttu-id="1cd39-118">Para obtener más información, consulte [Administración de integración de Microsoft Teams](admin-teams-integration.md#minimum-requirements-1).</span><span class="sxs-lookup"><span data-stu-id="1cd39-118">For more information, see [Managing Microsoft Teams Integration](admin-teams-integration.md#minimum-requirements-1).</span></span>
<!--
- People You and your coworkers have the following permissions in [!INCLUDE [prodshort](includes/prodshort.md)]
  - To paste a [!INCLUDE [prodshort](includes/prodshort.md)] link into a Teams conversation and have it expand into a card, you have to have at least permission to view the page and its data.
  - Once a card is submitted into a conversation, any user in that conversation can view that card without having permission to Business Central.
  - For other users to view more details from card, they must also have view permission, as a minimum, to the page and its data. If they want to change data, they'll need modify permissions.

  Setting up permissions is typically done by an administrator. For more information, see [Managing Microsoft Teams Integration](admin-teams-integration.md).-->

## <a name="include-a-business-central-card-in-a-teams-conversation"></a><span data-ttu-id="1cd39-119">Incluir una tarjeta Business Central en una conversación de Teams</span><span class="sxs-lookup"><span data-stu-id="1cd39-119">Include a Business Central card in a Teams conversation</span></span>

1. <span data-ttu-id="1cd39-120">Inicie sesión en [!INCLUDE [prodshort](includes/prodshort.md)] usando su navegador.</span><span class="sxs-lookup"><span data-stu-id="1cd39-120">Sign in to [!INCLUDE [prodshort](includes/prodshort.md)] using your browser.</span></span>
2. <span data-ttu-id="1cd39-121">Abra el registro que quiere compartir.</span><span class="sxs-lookup"><span data-stu-id="1cd39-121">Open the record that you want to share.</span></span>

    <span data-ttu-id="1cd39-122">La aplicación está diseñada para mostrar páginas tipo tarjeta desde [!INCLUDE [prodshort](includes/prodshort.md)].</span><span class="sxs-lookup"><span data-stu-id="1cd39-122">The app is designed to display card type pages from [!INCLUDE [prodshort](includes/prodshort.md)].</span></span> <span data-ttu-id="1cd39-123">Por lo tanto, abra una página que muestre un solo registro, como un producto, un cliente o una orden de venta.</span><span class="sxs-lookup"><span data-stu-id="1cd39-123">So open a page that displays a single record, like an item, customer, or sales order.</span></span> <span data-ttu-id="1cd39-124">No puede usarlo para centros de funciones o páginas que muestren varios registros en una lista.</span><span class="sxs-lookup"><span data-stu-id="1cd39-124">You can't use it for role centers or pages that display several records in a list.</span></span>

3. <span data-ttu-id="1cd39-125">Copie la URL completa de la barra de direcciones del navegador.</span><span class="sxs-lookup"><span data-stu-id="1cd39-125">Copy the entire URL from the browser's address bar.</span></span>

   ![Copiar la URL de Business Central desde el navegador](media/teams-url.png)
4. <span data-ttu-id="1cd39-127">Vaya a Teams e inicie una conversación, que puede ser chatear con una persona, un grupo de personas o un canal de equipo.</span><span class="sxs-lookup"><span data-stu-id="1cd39-127">Go to Teams and start a conversation, which can be chat with a person, group of persons, or a team channel.</span></span>

    <!--Teams imposes a few limitations here eg. you cannot unfurl a link during a Voice/Video call :/ We should probably only mention this in a Troubleshooting section (and i hope it will also be fixed soon)-->
5. <span data-ttu-id="1cd39-128">Pegue la URL en el cuadro donde agrega un mensaje.</span><span class="sxs-lookup"><span data-stu-id="1cd39-128">Paste the URL into the box where you add a message.</span></span>

   ![Pegar la URL de Business Central en Teams](media/teams-paste-url.png)
6. <span data-ttu-id="1cd39-130">La primera vez que pegue un vínculo en una conversación, se le pedirá que inicie sesión en [!INCLUDE [prodshort](includes/prodshort.md)] y dar su consentimiento para que la aplicación recupere datos.</span><span class="sxs-lookup"><span data-stu-id="1cd39-130">The first time you paste a link into a conversation, you'll be asked to sign in to [!INCLUDE [prodshort](includes/prodshort.md)] and give consent for the app to retrieve data.</span></span> <span data-ttu-id="1cd39-131">Simplemente siga las instrucciones en pantalla.</span><span class="sxs-lookup"><span data-stu-id="1cd39-131">Just follow the on-screen instructions.</span></span>

    > [!NOTE]
    > <span data-ttu-id="1cd39-132">Solo tiene que realizar este paso una vez.</span><span class="sxs-lookup"><span data-stu-id="1cd39-132">You'll only have to do this step once.</span></span>

7. <span data-ttu-id="1cd39-133">Espere un momento mientras se genera una tarjeta en el cuadro de mensajes.</span><span class="sxs-lookup"><span data-stu-id="1cd39-133">Wait a moment while a card is generated in the message box.</span></span>

8. <span data-ttu-id="1cd39-134">Cuando aparezca la tarjeta, revise el contenido de la tarjeta detenidamente en busca de información confidencial antes de enviar el mensaje.</span><span class="sxs-lookup"><span data-stu-id="1cd39-134">When the card appears, review the contents of the card carefully for any sensitive information before sending the message.</span></span> <span data-ttu-id="1cd39-135">Este paso es importante porque, una vez que envía el mensaje, todos los participantes de la conversación pueden ver la tarjeta.</span><span class="sxs-lookup"><span data-stu-id="1cd39-135">This step is important because once you send the message, everyone in the conversation can see the card.</span></span>

9. <span data-ttu-id="1cd39-136">Si la tarjeta tiene buen aspecto, seleccione **Enviar** para enviarla a la conversación.</span><span class="sxs-lookup"><span data-stu-id="1cd39-136">If the card looks good, select **Send** to submit it to the conversation.</span></span>

    > [!TIP]
    > <span data-ttu-id="1cd39-137">Después de que aparezca la tarjeta y antes de seleccionar **Enviar**, puede eliminar la URL pegada si lo desea.</span><span class="sxs-lookup"><span data-stu-id="1cd39-137">After the card appears, and before you select **Send**, you can delete the pasted URL if you like.</span></span>

10. <span data-ttu-id="1cd39-138">Para ver más detalles o realizar cambios en el registro, seleccione **Detalles**.</span><span class="sxs-lookup"><span data-stu-id="1cd39-138">To view more details or make changes to the record, select **Details**.</span></span>

    <span data-ttu-id="1cd39-139">La página de detalles es similar a la que vería en [!INCLUDE [prodshort](includes/prodshort.md)].</span><span class="sxs-lookup"><span data-stu-id="1cd39-139">The details page is similar to what you'd see in [!INCLUDE [prodshort](includes/prodshort.md)].</span></span> <span data-ttu-id="1cd39-140">Pero está un tanto recortadada para Teams.</span><span class="sxs-lookup"><span data-stu-id="1cd39-140">But it's slightly trimmed for Teams.</span></span> <span data-ttu-id="1cd39-141">Cuando haya terminado de ver y realizar cambios, cierre la ventana para volver a la conversación de Teams.</span><span class="sxs-lookup"><span data-stu-id="1cd39-141">When you're finished viewing and making changes, close the window to return to the Teams conversation.</span></span>

    > [!NOTE]
    > <span data-ttu-id="1cd39-142">Los cambios que realice no se reflejarán en la tarjeta hasta la próxima vez que pegue su vínculo en una conversación.</span><span class="sxs-lookup"><span data-stu-id="1cd39-142">Any changes you make won't be reflected in the card until the next time you paste its link in a conversation.</span></span>

## <a name="see-also"></a><span data-ttu-id="1cd39-143">Consulte también</span><span class="sxs-lookup"><span data-stu-id="1cd39-143">See Also</span></span>

[<span data-ttu-id="1cd39-144">Descripción general de la integración de Business Central y Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="1cd39-144">Business Central and Microsoft Teams Integration Overview</span></span>](across-teams-overview.md)  
<span data-ttu-id="1cd39-145">[Instalar la aplicación [!INCLUDE [prodshort](includes/prodshort.md)] para Microsoft Teams](across-install-app-for-teams.md)</span><span class="sxs-lookup"><span data-stu-id="1cd39-145">[Install the [!INCLUDE [prodshort](includes/prodshort.md)] App for Microsoft Teams](across-install-app-for-teams.md)</span></span>  
[<span data-ttu-id="1cd39-146">Desarrollo para la integración de Teams</span><span class="sxs-lookup"><span data-stu-id="1cd39-146">Developing for Teams Integration</span></span>](/dynamics365/business-central/dev-itpro/developer/devenv-develop-for-teams)  
[<span data-ttu-id="1cd39-147">Introducción</span><span class="sxs-lookup"><span data-stu-id="1cd39-147">Getting Started</span></span>](product-get-started.md)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
