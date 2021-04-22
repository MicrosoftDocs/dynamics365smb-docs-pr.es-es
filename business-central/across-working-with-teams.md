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
ms.date: 04/01/2021
ms.author: jswymer
ms.openlocfilehash: e20208d50eb65f1a92e6661396bf53007ab88eb8
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 03/31/2021
ms.locfileid: "5786887"
---
# <a name="working-with-business-central-data-in-microsoft-teams"></a><span data-ttu-id="6c85a-103">Trabajar con datos de Business Central en Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="6c85a-103">Working with Business Central Data in Microsoft Teams</span></span>

[!INCLUDE [online_only](includes/online_only.md)]

<span data-ttu-id="6c85a-104">[!INCLUDE [prod_short](includes/prod_short.md)] ofrece una aplicación que conecta Microsoft Teams a sus datos comerciales de [!INCLUDE [prod_short](includes/prod_short.md)], para que pueda compartir detalles rápidamente entre los miembros del equipo y responder más rápidamente a las consultas.</span><span class="sxs-lookup"><span data-stu-id="6c85a-104">[!INCLUDE [prod_short](includes/prod_short.md)] offers an app that connects Microsoft Teams to your business data in [!INCLUDE [prod_short](includes/prod_short.md)], so you can quickly share details across team members and respond faster to inquiries.</span></span> <span data-ttu-id="6c85a-105">En este artículo, aprenderá a usar la aplicación para compartir datos de [!INCLUDE [prod_short](includes/prod_short.md)] con compañeros de trabajo en una conversación de Teams.</span><span class="sxs-lookup"><span data-stu-id="6c85a-105">In this article, you'll learn how to use the app to share [!INCLUDE [prod_short](includes/prod_short.md)] data with coworkers in a Teams conversation.</span></span>

## <a name="overview"></a><span data-ttu-id="6c85a-106">Panorama</span><span class="sxs-lookup"><span data-stu-id="6c85a-106">Overview</span></span>

<span data-ttu-id="6c85a-107">La aplicación [!INCLUDE [prod_short](includes/prod_short.md)] le permite:</span><span class="sxs-lookup"><span data-stu-id="6c85a-107">The [!INCLUDE [prod_short](includes/prod_short.md)] app lets you:</span></span>

- <span data-ttu-id="6c85a-108">Copie un vínculo a cualquier registro de Business Central y péguelo en una conversación de Teams para compartirlo con sus compañeros de trabajo.</span><span class="sxs-lookup"><span data-stu-id="6c85a-108">Copy a link to any Business Central record and paste it into a Teams conversation to share with your coworkers.</span></span> <span data-ttu-id="6c85a-109">La aplicación expandirá el vínculo para convertirse en una tarjeta compacta e interactiva que muestra información sobre el registro.</span><span class="sxs-lookup"><span data-stu-id="6c85a-109">The app will then expand the link into a compact, interactive card that displays information about the record.</span></span>
- <span data-ttu-id="6c85a-110">Una vez en la conversación, usted y sus compañeros de trabajo pueden ver más detalles sobre el registro, editar datos y tomar medidas, sin salir de Teams.</span><span class="sxs-lookup"><span data-stu-id="6c85a-110">Once in the conversation, you and coworkers can view more details about the record, edit data, and take action&mdash;without leaving Teams.</span></span>

<span data-ttu-id="6c85a-111">[![Integración de Teams con Business Central](media/teams-intro-v3.png)](media/teams-intro-v3.png#lightbox)</span><span class="sxs-lookup"><span data-stu-id="6c85a-111">[![Teams integration with Business Central](media/teams-intro-v3.png)](media/teams-intro-v3.png#lightbox)</span></span>

## <a name="prerequisites"></a><span data-ttu-id="6c85a-112">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="6c85a-112">Prerequisites</span></span>

- <span data-ttu-id="6c85a-113">Tiene acceso a Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="6c85a-113">You have access to Microsoft Teams.</span></span>
- <span data-ttu-id="6c85a-114">Ha instalado la aplicación [!INCLUDE [prod_short](includes/prod_short.md)] en Teams.</span><span class="sxs-lookup"><span data-stu-id="6c85a-114">You've installed the [!INCLUDE [prod_short](includes/prod_short.md)] app in Teams.</span></span> <span data-ttu-id="6c85a-115">Para obtener más información, consulte [Instalar la aplicación [!INCLUDE [prod_short](includes/prod_short.md)] para Microsoft Teams](across-install-app-for-teams.md)</span><span class="sxs-lookup"><span data-stu-id="6c85a-115">For more information, see [Install the [!INCLUDE [prod_short](includes/prod_short.md)] App for Microsoft Teams](across-install-app-for-teams.md)</span></span>

> [!NOTE]
> <span data-ttu-id="6c85a-116">Todos los participantes de una conversación de Teams podrán ver las tarjetas de los registros de Business Central que envíe a la conversación.</span><span class="sxs-lookup"><span data-stu-id="6c85a-116">All participants in a Teams conversation will be able to view cards for Business Central records that you submit to the conversation.</span></span> <span data-ttu-id="6c85a-117">Pero, para ver más detalles sobre los registros, usando los botones **Detalles** o **Desplegable** de una tarjeta, necesitarán acceder a [!INCLUDE [prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="6c85a-117">But to view more details about records, by using the **Details** or **Pop out** buttons on a card, they'll need access to [!INCLUDE [prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="6c85a-118">Para obtener más información, consulte [Administración de integración de Microsoft Teams](admin-teams-integration.md#minimum-requirements-1).</span><span class="sxs-lookup"><span data-stu-id="6c85a-118">For more information, see [Managing Microsoft Teams Integration](admin-teams-integration.md#minimum-requirements-1).</span></span>

## <a name="include-a-business-central-card-in-a-teams-conversation"></a><span data-ttu-id="6c85a-119">Incluir una tarjeta Business Central en una conversación de Teams</span><span class="sxs-lookup"><span data-stu-id="6c85a-119">Include a Business Central card in a Teams conversation</span></span>

1. <span data-ttu-id="6c85a-120">Inicie sesión en [!INCLUDE [prod_short](includes/prod_short.md)] usando su navegador.</span><span class="sxs-lookup"><span data-stu-id="6c85a-120">Sign in to [!INCLUDE [prod_short](includes/prod_short.md)] using your browser.</span></span>
2. <span data-ttu-id="6c85a-121">Abra el registro que quiere compartir.</span><span class="sxs-lookup"><span data-stu-id="6c85a-121">Open the record that you want to share.</span></span>

    <span data-ttu-id="6c85a-122">La aplicación está diseñada para mostrar páginas tipo tarjeta desde [!INCLUDE [prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="6c85a-122">The app is designed to display card type pages from [!INCLUDE [prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="6c85a-123">Por lo tanto, abra una página que muestre un solo registro, como un producto, un cliente o una orden de venta.</span><span class="sxs-lookup"><span data-stu-id="6c85a-123">So open a page that displays a single record, like an item, customer, or sales order.</span></span> <span data-ttu-id="6c85a-124">No puede usarlo para centros de funciones o páginas que muestren varios registros en una lista.</span><span class="sxs-lookup"><span data-stu-id="6c85a-124">You can't use it for role centers or pages that display several records in a list.</span></span>

3. <span data-ttu-id="6c85a-125">Copie la URL completa de la barra de direcciones del navegador.</span><span class="sxs-lookup"><span data-stu-id="6c85a-125">Copy the entire URL from the browser's address bar.</span></span>

   ![Copiar la URL de Business Central desde el navegador](media/teams-url-v2.png)
4. <span data-ttu-id="6c85a-127">Vaya a Teams e inicie una conversación, que puede ser chatear con una persona, un grupo de personas o un canal de equipo.</span><span class="sxs-lookup"><span data-stu-id="6c85a-127">Go to Teams and start a conversation, which can be chat with a person, group of persons, or a team channel.</span></span>

    <!--Teams imposes a few limitations here eg. you cannot unfurl a link during a Voice/Video call :/ We should probably only mention this in a Troubleshooting section (and i hope it will also be fixed soon)-->
5. <span data-ttu-id="6c85a-128">Pegue la URL en el cuadro de mensaje donde redacta los mensajes.</span><span class="sxs-lookup"><span data-stu-id="6c85a-128">Paste the URL in the message box where you compose a message.</span></span>

   ![Pegar la URL de Business Central en Teams](media/teams-paste-url-v2.png)
6. <span data-ttu-id="6c85a-130">La primera vez que pegue un vínculo en una conversación, se le pedirá que inicie sesión en [!INCLUDE [prod_short](includes/prod_short.md)] y dar su consentimiento para que la aplicación recupere datos.</span><span class="sxs-lookup"><span data-stu-id="6c85a-130">The first time you paste a link into a conversation, you'll be asked to sign in to [!INCLUDE [prod_short](includes/prod_short.md)] and give consent for the app to retrieve data.</span></span> <span data-ttu-id="6c85a-131">Simplemente siga las instrucciones en pantalla.</span><span class="sxs-lookup"><span data-stu-id="6c85a-131">Just follow the on-screen instructions.</span></span>

    > [!NOTE]
    > <span data-ttu-id="6c85a-132">Solo tiene que realizar este paso una vez.</span><span class="sxs-lookup"><span data-stu-id="6c85a-132">You'll only have to do this step once.</span></span>

7. <span data-ttu-id="6c85a-133">Espere un momento mientras se genera una tarjeta en el cuadro de mensajes.</span><span class="sxs-lookup"><span data-stu-id="6c85a-133">Wait a moment while a card is generated in the message box.</span></span>

8. <span data-ttu-id="6c85a-134">Cuando aparezca la tarjeta, revise el contenido de la tarjeta detenidamente en busca de información confidencial antes de enviar el mensaje.</span><span class="sxs-lookup"><span data-stu-id="6c85a-134">When the card appears, review the contents of the card carefully for any sensitive information before sending the message.</span></span> <span data-ttu-id="6c85a-135">Este paso es importante porque, una vez que envía el mensaje, todos los participantes de la conversación pueden ver la tarjeta.</span><span class="sxs-lookup"><span data-stu-id="6c85a-135">This step is important because once you send the message, everyone in the conversation can see the card.</span></span>

9. <span data-ttu-id="6c85a-136">Si la tarjeta tiene buen aspecto, seleccione **Enviar** para enviarla a la conversación.</span><span class="sxs-lookup"><span data-stu-id="6c85a-136">If the card looks good, select **Send** to submit it to the conversation.</span></span>

    > [!TIP]
    > <span data-ttu-id="6c85a-137">Después de que aparezca la tarjeta y antes de seleccionar **Enviar**, puede eliminar la URL pegada si lo desea.</span><span class="sxs-lookup"><span data-stu-id="6c85a-137">After the card appears, and before you select **Send**, you can delete the pasted URL if you like.</span></span>

10. <span data-ttu-id="6c85a-138">Para ver más detalles o realizar cambios en el registro mostrado en la tarjeta, seleccione **Detalles**.</span><span class="sxs-lookup"><span data-stu-id="6c85a-138">To view more details or make changes to the record shown in the card, select **Details**.</span></span> <span data-ttu-id="6c85a-139">Para obtener más información, consulte la sección siguiente.</span><span class="sxs-lookup"><span data-stu-id="6c85a-139">For more information, see the next section.</span></span>

## <a name="view-card-details"></a><span data-ttu-id="6c85a-140">Ver detalles de tarjeta</span><span class="sxs-lookup"><span data-stu-id="6c85a-140">View card details</span></span>

<span data-ttu-id="6c85a-141">Una vez que se ha enviado una tarjeta a una conversación, todos los participantes con los [permisos adecuados](admin-teams-integration.md#permissions) puede seleccionar **Detalles** para abrir una ventana que muestra más información sobre el registro, y posiblemente realizar cambios en el registro.</span><span class="sxs-lookup"><span data-stu-id="6c85a-141">Once a card's been sent to a conversation, all participants with the [proper permissions](admin-teams-integration.md#permissions) can select **Details** to open a window that displays more information about the record&mdash;and possibly make changes to the record.</span></span> <span data-ttu-id="6c85a-142">No importa si eres el que envía la tarjeta o el que la recibe.</span><span class="sxs-lookup"><span data-stu-id="6c85a-142">It doesn't matter if you're the one sending the card or the one receiving the card.</span></span> <span data-ttu-id="6c85a-143">La función **Detalles** es especialmente útil para los destinatarios, ya que les proporciona rápidamente información concisa y específica sobre el registro, en lugar de tener que escanear el registro completo.</span><span class="sxs-lookup"><span data-stu-id="6c85a-143">The **Details** feature is especially useful to recipients, because it quickly provides them with concise, targeted information about the record, as opposed to having to scan the full record.</span></span>

<span data-ttu-id="6c85a-144">La ventana de detalles es similar a la que vería en el registro de [!INCLUDE [prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="6c85a-144">The details window is similar to what you'd see in [!INCLUDE [prod_short](includes/prod_short.md)] the record.</span></span> <span data-ttu-id="6c85a-145">Pero está un tanto recortadada para Teams.</span><span class="sxs-lookup"><span data-stu-id="6c85a-145">But it's slightly trimmed for Teams.</span></span> <span data-ttu-id="6c85a-146">Cuando haya terminado de ver y realizar cambios, cierre la ventana para volver a la conversación de Teams.</span><span class="sxs-lookup"><span data-stu-id="6c85a-146">When you're finished viewing and making changes, close the window to return to the Teams conversation.</span></span>

<span data-ttu-id="6c85a-147">Aquí hay un par de cosas que debe tener en cuenta al trabajar con los detalles de la tarjeta:</span><span class="sxs-lookup"><span data-stu-id="6c85a-147">Here are a couple things to keep in mind when working with the card details:</span></span>

- <span data-ttu-id="6c85a-148">Para abrir los detalles de la tarjeta, los usuarios deben tener permiso de lectura en la página y sus datos en [!INCLUDE [prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="6c85a-148">To open the card details, users must have permission on the page and its data in [!INCLUDE [prod_short](includes/prod_short.md)].</span></span>
- <span data-ttu-id="6c85a-149">Las tarjetas en los chats de Teams no se actualizan automáticamente a los cambios.</span><span class="sxs-lookup"><span data-stu-id="6c85a-149">Cards in Teams chats aren't automatically updated to changes.</span></span> <span data-ttu-id="6c85a-150">Cualquier cambio que guarde en un registro en la ventana de detalles se guarda en [!INCLUDE [prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="6c85a-150">Any changes you save to a record in the details window are saved in [!INCLUDE [prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="6c85a-151">Pero la tarjeta en Teams no mostrará los cambios en la conversión hasta que vuelva a pegar el enlace.</span><span class="sxs-lookup"><span data-stu-id="6c85a-151">But the card in Teams won't show the changes in the conversion, until you paste the link again.</span></span>

<span data-ttu-id="6c85a-152">Para obtener más información sobre cómo trabajar con tarjetas y detalles de tarjetas, consulte [Preguntas frecuentes de Teams](teams-faq.md).</span><span class="sxs-lookup"><span data-stu-id="6c85a-152">To learn more about working with cards and card details, see [Teams FAQ](teams-faq.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="6c85a-153">Consulte también</span><span class="sxs-lookup"><span data-stu-id="6c85a-153">See Also</span></span>

[<span data-ttu-id="6c85a-154">Descripción general de la integración de Business Central y Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="6c85a-154">Business Central and Microsoft Teams Integration Overview</span></span>](across-teams-overview.md)  
<span data-ttu-id="6c85a-155">[Instalar la aplicación [!INCLUDE [prod_short](includes/prod_short.md)] para Microsoft Teams](across-install-app-for-teams.md)</span><span class="sxs-lookup"><span data-stu-id="6c85a-155">[Install the [!INCLUDE [prod_short](includes/prod_short.md)] App for Microsoft Teams](across-install-app-for-teams.md)</span></span>  
[<span data-ttu-id="6c85a-156">P+F de Teams</span><span class="sxs-lookup"><span data-stu-id="6c85a-156">Teams FAQ</span></span>](teams-faq.md)  
[<span data-ttu-id="6c85a-157">Consejos para la solución de problemas de Teams</span><span class="sxs-lookup"><span data-stu-id="6c85a-157">Troubleshooting Teams</span></span>](admin-teams-troubleshooting.md)  
[<span data-ttu-id="6c85a-158">Desarrollo para la integración de Teams</span><span class="sxs-lookup"><span data-stu-id="6c85a-158">Developing for Teams Integration</span></span>](/dynamics365/business-central/dev-itpro/developer/devenv-develop-for-teams)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  


[!INCLUDE[footer-include](includes/footer-banner.md)]