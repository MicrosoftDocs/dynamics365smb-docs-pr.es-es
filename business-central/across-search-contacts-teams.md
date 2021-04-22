---
title: Buscar contactos desde Microsoft Teams
description: Aprenda a buscar clientes, proveedores y otros contactos de Business Central desde Microsoft Teams.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Teams, MS Teams, Microsoft Teams, Skype, Link, Microsoft 365, contacts, search, messaging extensions
ms.date: 04/12/2021
ms.author: jswymer
ms.openlocfilehash: 77108cab69a05165616ad5e1a44f1a3ddc9d4cd9
ms.sourcegitcommit: e13b80d4e5141f414109e660e0918eae561acb36
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/13/2021
ms.locfileid: "5882501"
---
# <a name="searching-for-customers-vendors-and-other-contacts-from-microsoft-teams"></a><span data-ttu-id="cd97c-103">Búsqueda de clientes, proveedores y otros contactos desde Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="cd97c-103">Searching for Customers, Vendors, and Other Contacts from Microsoft Teams</span></span>

<span data-ttu-id="cd97c-104">[!INCLUDE [online_only](includes/online_only.md)].</span><span class="sxs-lookup"><span data-stu-id="cd97c-104">[!INCLUDE [online_only](includes/online_only.md)].</span></span> <span data-ttu-id="cd97c-105">Se presentó en el lanzamiento de versiones 1 de 2021.</span><span class="sxs-lookup"><span data-stu-id="cd97c-105">Introduced in 2021 release wave 1.</span></span>

<span data-ttu-id="cd97c-106">[!INCLUDE [prod_short](includes/prod_short.md)] tiene un sistema integral de administración de contactos profesionales que es esencial para los usuarios en ventas, operaciones u otros roles departamentales.</span><span class="sxs-lookup"><span data-stu-id="cd97c-106">[!INCLUDE [prod_short](includes/prod_short.md)] has a comprehensive business contact management system that is essential for users in sales, operations, or other departmental roles.</span></span> <span data-ttu-id="cd97c-107">Si es un usuario de uno de estos roles, con frecuencia deberá buscar, reunirse o iniciar una conversación con sus proveedores, clientes y otros contactos.</span><span class="sxs-lookup"><span data-stu-id="cd97c-107">If you're a user in one of these roles, you'll often need to look up, meet, or start a conversation with your vendors, customers, and other contacts.</span></span> <span data-ttu-id="cd97c-108">Con la aplicación [!INCLUDE [prod_short](includes/prod_short.md)] para Teams, puede realizar estas tareas directamente desde Teams, sin tener que cambiar a [!INCLUDE [prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="cd97c-108">With the [!INCLUDE [prod_short](includes/prod_short.md)] app for Teams, you can do these tasks directly from Teams, without having to switch to [!INCLUDE [prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="cd97c-109">Desde dentro de Teams, puede:</span><span class="sxs-lookup"><span data-stu-id="cd97c-109">From within Teams, you can:</span></span>

- <span data-ttu-id="cd97c-110">Buscar contactos de [!INCLUDE [prod_short](includes/prod_short.md)] desde el cuadro de comando de Teams o desde el área de redacción de mensajes.</span><span class="sxs-lookup"><span data-stu-id="cd97c-110">Look up [!INCLUDE [prod_short](includes/prod_short.md)] contacts from the Teams command box or from the message compose area.</span></span> <span data-ttu-id="cd97c-111">Los contactos pueden incluir clientes potenciales, proveedores, clientes u otras relaciones de negocio.</span><span class="sxs-lookup"><span data-stu-id="cd97c-111">Contacts can include prospects, vendors, customers, or other business relationships.</span></span>
- <span data-ttu-id="cd97c-112">Compartir un contacto como una ficha en una conversación de Teams.</span><span class="sxs-lookup"><span data-stu-id="cd97c-112">Share a contact as a card in a Teams conversation.</span></span>
- <span data-ttu-id="cd97c-113">Ver detalles sobre la información de contacto, el historial de interacciones y otra información, como pagos pendientes o documentos abiertos.</span><span class="sxs-lookup"><span data-stu-id="cd97c-113">View details about contact information, interaction history, and other insights like outstanding payments or open documents.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="cd97c-114">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="cd97c-114">Prerequisites</span></span>

- <span data-ttu-id="cd97c-115">Tiene acceso a Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="cd97c-115">You have access to Microsoft Teams.</span></span>
- <span data-ttu-id="cd97c-116">Ha instalado la aplicación [!INCLUDE [prod_short](includes/prod_short.md)] en Teams.</span><span class="sxs-lookup"><span data-stu-id="cd97c-116">You've installed the [!INCLUDE [prod_short](includes/prod_short.md)] app in Teams.</span></span> <span data-ttu-id="cd97c-117">Para obtener más información, consulte [Instalar la aplicación [!INCLUDE [prod_short](includes/prod_short.md)] para Microsoft Teams](across-install-app-for-teams.md)</span><span class="sxs-lookup"><span data-stu-id="cd97c-117">For more information, see [Install the [!INCLUDE [prod_short](includes/prod_short.md)] App for Microsoft Teams](across-install-app-for-teams.md)</span></span>
- <span data-ttu-id="cd97c-118">Tiene una cuenta de [!INCLUDE [prod_short](includes/prod_short.md)] con acceso a contactos en al menos una empresa.</span><span class="sxs-lookup"><span data-stu-id="cd97c-118">You've got a [!INCLUDE [prod_short](includes/prod_short.md)] account with access to contacts in at least one company.</span></span>

> [!NOTE]
> <span data-ttu-id="cd97c-119">Tanto si busca desde el cuadro de comando o el cuadro de redacción del mensaje, es posible que se le pida que inicie sesión o configure la aplicación la primera vez.</span><span class="sxs-lookup"><span data-stu-id="cd97c-119">Whether you searching from the command box or message compose box, you may be asked to sign in or set up the app the first time.</span></span> <span data-ttu-id="cd97c-120">Este paso es necesario para buscar contactos en la empresa de Business Central correcta.</span><span class="sxs-lookup"><span data-stu-id="cd97c-120">This step is necessary to search for contacts in the right Business Central company.</span></span> <span data-ttu-id="cd97c-121">Para obtener información sobre cómo configurar la aplicación para elegir su empresa, consulte [Cambiar la empresa y otras configuraciones en Teams](across-teams-settings.md).</span><span class="sxs-lookup"><span data-stu-id="cd97c-121">For information about setting up the app to choose your company, see [Changing Company and Other Settings in Teams](across-teams-settings.md).</span></span>

## <a name="look-up-contacts-from-the-command-box"></a><span data-ttu-id="cd97c-122">Buscar contactos desde el cuadro de comando</span><span class="sxs-lookup"><span data-stu-id="cd97c-122">Look up contacts from the command box</span></span>

<span data-ttu-id="cd97c-123">El cuadro de comando se encuentra en la parte superior de cada pantalla en Teams.</span><span class="sxs-lookup"><span data-stu-id="cd97c-123">The command box is at the top of every screen in Teams.</span></span> <span data-ttu-id="cd97c-124">Le permite buscar, realizar acciones rápidas o iniciar aplicaciones, como la aplicación [!INCLUDE [prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="cd97c-124">It lets you search, take quick actions, or launch apps, like the [!INCLUDE [prod_short](includes/prod_short.md)] app.</span></span> <span data-ttu-id="cd97c-125">La búsqueda desde el cuadro de comando es ideal para buscar rápidamente contactos y sus datos relacionados para su propio uso.</span><span class="sxs-lookup"><span data-stu-id="cd97c-125">Searching from the command box is great for quickly looking up contacts and their related data for your own use.</span></span> <span data-ttu-id="cd97c-126">Por ejemplo, suponga que desea buscar la dirección de correo electrónico de un proveedor para configurar una reunión en el calendario.</span><span class="sxs-lookup"><span data-stu-id="cd97c-126">For example, suppose you want to look up an email address of a vendor to set up a calendar meeting.</span></span> <span data-ttu-id="cd97c-127">O tal vez desee buscar el historial de interacciones durante una reunión con un cliente.</span><span class="sxs-lookup"><span data-stu-id="cd97c-127">Or maybe you want to look up interaction history during a meeting with a customer.</span></span>

1. <span data-ttu-id="cd97c-128">En el cuadro de comando, escriba **@Business Central** y, a continuación, seleccione la aplicación Business Central de los resultados.</span><span class="sxs-lookup"><span data-stu-id="cd97c-128">In the command box, type **@Business Central**, then select the Business Central app from the results.</span></span>

    ![Abrir la aplicación Business Central para buscar contactos desde el cuadro de comando](media/teams-contacts-command-1.png)

2. <span data-ttu-id="cd97c-130">En el cuadro **Business Central**, empiece a escribir el texto de búsqueda, como un nombre, una dirección o un número de teléfono.</span><span class="sxs-lookup"><span data-stu-id="cd97c-130">In the **Business Central** box, start typing search text, like a name, address, or phone number.</span></span>

    <span data-ttu-id="cd97c-131">A medida que escribe, aparecerán resultados coincidentes.</span><span class="sxs-lookup"><span data-stu-id="cd97c-131">As you type, matching results will appear.</span></span>

    ![Buscar contactos de Business Central desde el cuadro de comando de Teams](media/teams-contacts-command-2.png)
3. <span data-ttu-id="cd97c-133">Seleccione un contacto de los resultados.</span><span class="sxs-lookup"><span data-stu-id="cd97c-133">Select a contact from the results.</span></span>

    <span data-ttu-id="cd97c-134">La ficha de contacto aparece debajo del cuadro de comando.</span><span class="sxs-lookup"><span data-stu-id="cd97c-134">The contact card appears beneath the command box.</span></span>

4. <span data-ttu-id="cd97c-135">Si desea agregar la ficha de contacto a una conversación, vaya a la esquina superior derecha de la ficha, seleccione **... (Mas opciones)** > **Copiar**.</span><span class="sxs-lookup"><span data-stu-id="cd97c-135">If you want to add the contact card into a conversation, go to the upper right corner of the card, select **... (More options)** > **Copy**.</span></span> <span data-ttu-id="cd97c-136">A continuación, pegue la copia en el cuadro de redacción del mensaje de una conversación.</span><span class="sxs-lookup"><span data-stu-id="cd97c-136">Then, paste the copy in the message compose box of a conversation.</span></span>  

<span data-ttu-id="cd97c-137">Para obtener más información general sobre el cuadro de comando en Teams, consulte [Teams: usar el cuadro de comando](https://support.microsoft.com/en-us/office/use-the-command-box-13c4e429-7324-4886-b377-5dbed539193b).</span><span class="sxs-lookup"><span data-stu-id="cd97c-137">For more general information about the command box in Teams, see [Teams - Use the command box](https://support.microsoft.com/en-us/office/use-the-command-box-13c4e429-7324-4886-b377-5dbed539193b).</span></span>

## <a name="look-up-contacts-from-the-message-compose-box"></a><span data-ttu-id="cd97c-138">Buscar contactos desde el cuadro de redacción del mensaje</span><span class="sxs-lookup"><span data-stu-id="cd97c-138">Look up contacts from the message compose box</span></span>

<span data-ttu-id="cd97c-139">La ventaja de usar el cuadro de redacción del mensaje es que puede agregar una ficha de contacto directamente a una conversación para que otros la vean.</span><span class="sxs-lookup"><span data-stu-id="cd97c-139">The advantage of using the message compose box is that you can add a contact card directly to a conversation, for others to see.</span></span>

1. <span data-ttu-id="cd97c-140">Debajo del cuadro de redacción del mensaje, seleccione el icono **Business Central** para iniciar la aplicación.</span><span class="sxs-lookup"><span data-stu-id="cd97c-140">Beneath to message compose box, select the **Business Central** icon to launch the app.</span></span>

    <span data-ttu-id="cd97c-141">Si no ve el icono de **Business Central**, seleccione **... (extensiones de mensajes)**.</span><span class="sxs-lookup"><span data-stu-id="cd97c-141">If you don't see the **Business Central** icon, select **... (Messaging extensions)**.</span></span>

    ![Abrir la aplicación Business Central para buscar contactos desde el cuadro de mensajes](media/teams-contacts-message-box.png)

2. <span data-ttu-id="cd97c-143">En el cuadro **Business Central**, empiece a escribir el texto de búsqueda, como un nombre, una dirección o un número de teléfono.</span><span class="sxs-lookup"><span data-stu-id="cd97c-143">In the **Business Central** box, start typing search text, like a name, address, or phone number.</span></span>

    <span data-ttu-id="cd97c-144">A medida que escribe, aparecerán resultados coincidentes.</span><span class="sxs-lookup"><span data-stu-id="cd97c-144">As you type, matching results will appear.</span></span>

    ![Buscar contactos de Business Central desde el cuadro de mensajes](media/teams-contacts-5.png)
3. <span data-ttu-id="cd97c-146">Seleccione un contacto de los resultados.</span><span class="sxs-lookup"><span data-stu-id="cd97c-146">Select a contact from the results.</span></span>

    <span data-ttu-id="cd97c-147">La ficha de contacto aparece en el cuadro de redacción del mensaje.</span><span class="sxs-lookup"><span data-stu-id="cd97c-147">The contact card appears in the message compose box.</span></span>

    > [!NOTE]
    > <span data-ttu-id="cd97c-148">La ficha de contacto no se envía de inmediato a la conversación para que otros la vean.</span><span class="sxs-lookup"><span data-stu-id="cd97c-148">The contact card isn't sent to the conversation right away for others to see.</span></span> <span data-ttu-id="cd97c-149">Tiene la oportunidad de revisar el contenido de la ficha y agregar texto antes o después de esta como desee.</span><span class="sxs-lookup"><span data-stu-id="cd97c-149">You have the opportunity to review the contents of the card, and add text before or after it as you like.</span></span> <span data-ttu-id="cd97c-150">A continuación, envíe su mensaje al chat cuando esté listo.</span><span class="sxs-lookup"><span data-stu-id="cd97c-150">Then, send your message to the chat when ready.</span></span>

### <a name="heres-another-way"></a><span data-ttu-id="cd97c-151">Aquí hay otra forma</span><span class="sxs-lookup"><span data-stu-id="cd97c-151">Here's another way</span></span>

1. <span data-ttu-id="cd97c-152">En lugar de usar el icono de **Business Central**, escriba **@Business Central** directamente en el cuadro de redacción del mensaje.</span><span class="sxs-lookup"><span data-stu-id="cd97c-152">Instead of using the **Business Central** icon, type **@Business Central** directly in the message compose box.</span></span>
2. <span data-ttu-id="cd97c-153">Introduzca sus términos de búsqueda en el cuadro.</span><span class="sxs-lookup"><span data-stu-id="cd97c-153">Enter your search terms in the box.</span></span>
3. <span data-ttu-id="cd97c-154">Use las teclas de las flecha arriba y abajo en el teclado para elegir un contacto y, a continuación, presione Entrar para seleccionarlo.</span><span class="sxs-lookup"><span data-stu-id="cd97c-154">Use the up and down arrow keys on the keyboard to choose a contact, then press Enter to select it.</span></span>

## <a name="viewing-contact-card-details"></a><span data-ttu-id="cd97c-155">Ver detalles de la ficha de contacto</span><span class="sxs-lookup"><span data-stu-id="cd97c-155">Viewing contact card details</span></span>

<span data-ttu-id="cd97c-156">La ficha de contacto en Teams le ofrece un resumen rápido del cliente, proveedor o contacto.</span><span class="sxs-lookup"><span data-stu-id="cd97c-156">The contact card in Teams gives you a quick overview of the customer, vendor, or contact.</span></span> <span data-ttu-id="cd97c-157">La ficha es interactiva, lo que significa que puede ver más información o incluso modificar un contacto usando los botones **Detalles** o **Desplegable**.</span><span class="sxs-lookup"><span data-stu-id="cd97c-157">The card is interactive&mdash;meaning you can view more information or even modify a contact by using the **Details** or **Pop-out** buttons.</span></span>

<span data-ttu-id="cd97c-158">El botón **Detalles** abre una ventana dentro de Teams que muestra más información sobre el contacto, pero no tanta como vería en [!INCLUDE [prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="cd97c-158">The **Details** button opens a window within Teams that displays more information about the contact, but not as much as you'd see in [!INCLUDE [prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="cd97c-159">Para ver toda la información sobre un contacto en [!INCLUDE [prod_short](includes/prod_short.md)], seleccione **Desplegable**.</span><span class="sxs-lookup"><span data-stu-id="cd97c-159">To see all the information about a contact in [!INCLUDE [prod_short](includes/prod_short.md)], select **Pop-out**.</span></span>

<span data-ttu-id="cd97c-160">La ficha de contacto funciona como fichas para registros, como productos, clientes o pedidos de venta.</span><span class="sxs-lookup"><span data-stu-id="cd97c-160">The contact card works just like cards for records, like items, customers, or sales orders.</span></span> <span data-ttu-id="cd97c-161">Para obtener más información sobre las fichas, consulte [Ver detalles de la ficha](across-working-with-teams.md#view-card-details).</span><span class="sxs-lookup"><span data-stu-id="cd97c-161">For more information about cards, see [View card details](across-working-with-teams.md#view-card-details).</span></span>

> [!NOTE]
> <span data-ttu-id="cd97c-162">Todos los participantes de una conversación de Teams podrán ver las fichas del contacto de Business Central que envíe a una conversación.</span><span class="sxs-lookup"><span data-stu-id="cd97c-162">All participants in a Teams conversation will be able to view cards for Business Central contact that you submit to a conversation.</span></span> <span data-ttu-id="cd97c-163">Pero, para ver más detalles sobre los registros, usando los botones **Detalles** o **Desplegable** de una tarjeta, necesitarán acceder a [!INCLUDE [prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="cd97c-163">But to view more details about records, by using the **Details** or **Pop out** buttons on a card, they'll need access to [!INCLUDE [prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="cd97c-164">Para obtener más información, consulte [Administración de integración de Microsoft Teams](admin-teams-integration.md#minimum-requirements-1).</span><span class="sxs-lookup"><span data-stu-id="cd97c-164">For more information, see [Managing Microsoft Teams Integration](admin-teams-integration.md#minimum-requirements-1).</span></span>

## <a name="see-also"></a><span data-ttu-id="cd97c-165">Consulte también</span><span class="sxs-lookup"><span data-stu-id="cd97c-165">See Also</span></span>

[<span data-ttu-id="cd97c-166">Descripción general de la integración de Business Central y Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="cd97c-166">Business Central and Microsoft Teams Integration Overview</span></span>](across-teams-overview.md)  
<span data-ttu-id="cd97c-167">[Instalar la aplicación [!INCLUDE [prod_short](includes/prod_short.md)] para Microsoft Teams](across-install-app-for-teams.md)</span><span class="sxs-lookup"><span data-stu-id="cd97c-167">[Install the [!INCLUDE [prod_short](includes/prod_short.md)] App for Microsoft Teams](across-install-app-for-teams.md)</span></span>  
[<span data-ttu-id="cd97c-168">P+F de Teams</span><span class="sxs-lookup"><span data-stu-id="cd97c-168">Teams FAQ</span></span>](teams-faq.md)  
[<span data-ttu-id="cd97c-169">Consejos para la solución de problemas de Teams</span><span class="sxs-lookup"><span data-stu-id="cd97c-169">Troubleshooting Teams</span></span>](admin-teams-troubleshooting.md)  
[<span data-ttu-id="cd97c-170">Desarrollo para la integración de Teams</span><span class="sxs-lookup"><span data-stu-id="cd97c-170">Developing for Teams Integration</span></span>](/dynamics365/business-central/dev-itpro/developer/devenv-develop-for-teams)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  


[!INCLUDE[footer-include](includes/footer-banner.md)]