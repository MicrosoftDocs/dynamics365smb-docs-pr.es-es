---
title: Configurar el registro de correo electrónico | Documentos de Microsoft
description: Aprenda a convertir las interacciones de correo electrónico entre vendedores y clientes en oportunidades de venta reales.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, prospect, opportunity, email
ms.date: 07/01/2020
ms.author: bholtorf
ms.openlocfilehash: 9ca381bfebcd6db8e67d8153d4d2bc17eeffad81
ms.sourcegitcommit: f9aec4a72172d9270e14e2938c5550d69508f1aa
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 07/02/2020
ms.locfileid: "3532674"
---
# <a name="track-email-message-exchanges-between-salespeople-and-contacts"></a><span data-ttu-id="c8ad3-103">Realizar un seguimiento de los intercambios de mensajes de correo electrónico entre vendedores y contactos</span><span class="sxs-lookup"><span data-stu-id="c8ad3-103">Track Email Message Exchanges Between Salespeople and Contacts</span></span>

<span data-ttu-id="c8ad3-104">Aproveche al máximo las comunicaciones entre los vendedores y sus clientes actuales o potenciales mediante el seguimiento de los intercambios de correos electrónicos y, a continuación, conviértalos en oportunidades procesables.</span><span class="sxs-lookup"><span data-stu-id="c8ad3-104">Get more out of the communications between salespeople and your existing or potential customers by tracking email exchanges, and then turning them into actionable opportunities.</span></span> [!INCLUDE[d365fin](includes/d365fin_md.md)] <span data-ttu-id="c8ad3-105">puede funcionar con Exchange Online para mantener un registro de los mensajes entrantes y salientes.</span><span class="sxs-lookup"><span data-stu-id="c8ad3-105">can work with Exchange Online to keep a log of the inbound and outbound messages.</span></span> <span data-ttu-id="c8ad3-106">Puede ver y analizar el contenido de cada mensaje en la página **Movimientos del log de interacción**.</span><span class="sxs-lookup"><span data-stu-id="c8ad3-106">You can view and analyze the contents of each message on the **Interaction Log Entries** page.</span></span>

## <a name="set-up-public-folders-and-rules-for-email-logging-in-exchange-online"></a><span data-ttu-id="c8ad3-107">Configurar carpetas públicas y reglas para iniciar sesión por correo electrónico en Exchange Online</span><span class="sxs-lookup"><span data-stu-id="c8ad3-107">Set up Public Folders and Rules for Email Logging in Exchange Online</span></span>

[!INCLUDE[admin-setup-email-public-folder](includes/admin-setup-email-public-folder.md)]

<span data-ttu-id="c8ad3-108">Luego, te conectas [!INCLUDE[prodshort](includes/prodshort.md)] con Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="c8ad3-108">Next, you connect [!INCLUDE[prodshort](includes/prodshort.md)] with Exchange Online.</span></span>

## <a name="setting-up-d365fin-to-log-email-messages"></a><span data-ttu-id="c8ad3-109">Configuración de [!INCLUDE[d365fin](includes/d365fin_md.md)] para registrar los mensajes de correo electrónico</span><span class="sxs-lookup"><span data-stu-id="c8ad3-109">Setting Up [!INCLUDE[d365fin](includes/d365fin_md.md)] to Log Email Messages</span></span>

<span data-ttu-id="c8ad3-110">Comience con el registro de correo electrónico en dos sencillos pasos:</span><span class="sxs-lookup"><span data-stu-id="c8ad3-110">Get started with email logging in two easy steps:</span></span>

1. <span data-ttu-id="c8ad3-111">Conecte [!INCLUDE[d365fin](includes/d365fin_md.md)] con Exchange Online para su suscripción de Office 365.</span><span class="sxs-lookup"><span data-stu-id="c8ad3-111">Connect [!INCLUDE[d365fin](includes/d365fin_md.md)] with Exchange Online for your Office 365 subscription.</span></span> <span data-ttu-id="c8ad3-112">Exchange Online gestiona sus mensajes de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="c8ad3-112">Exchange Online handles your email messages.</span></span> <span data-ttu-id="c8ad3-113">Hemos facilitado este paso al proporcionar una guía de configuración asistida.</span><span class="sxs-lookup"><span data-stu-id="c8ad3-113">We've made this step easy by providing an assisted setup guide.</span></span> <span data-ttu-id="c8ad3-114">Solo necesita sus credenciales de administrador para su cuenta de administrador en Office 365.</span><span class="sxs-lookup"><span data-stu-id="c8ad3-114">You just need your administrator credentials for your administrator account in Office 365.</span></span> <span data-ttu-id="c8ad3-115">Para comenzar la guía, vaya a **Configuración asistida** y, a continuación, elija **Configurar registro de correo electrónico**.</span><span class="sxs-lookup"><span data-stu-id="c8ad3-115">To start the guide, go to **Assisted Setup**, and then choose **Set up email logging**.</span></span>  

2. <span data-ttu-id="c8ad3-116">Asegúrese de que se han introducido direcciones de correo electrónico válidas en [!INCLUDE[d365fin](includes/d365fin_md.md)] para sus vendedores y contactos, dependiendo de si son clientes potenciales o existentes.</span><span class="sxs-lookup"><span data-stu-id="c8ad3-116">Make sure that valid email addresses have been entered in [!INCLUDE[d365fin](includes/d365fin_md.md)] for your sales people and contacts, depending on whether they are potential or existing customers.</span></span> <span data-ttu-id="c8ad3-117">Para ello, para cada cliente o vendedor, abra la ficha **Contacto** o **Vendedor/Comprador** y consulte el campo **Correo electrónico**.</span><span class="sxs-lookup"><span data-stu-id="c8ad3-117">To do that, for each customer or salesperson, open the **Contact** or **Salesperson/Purchaser** card and have a look in the **Email** field.</span></span>

> [!Tip]
> <span data-ttu-id="c8ad3-118">Después de completar los pasos de la guía, puede comprobar si la conexión se ha realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="c8ad3-118">After you complete the steps in the guide you can check whether the connection was successful.</span></span> <span data-ttu-id="c8ad3-119">Busque **Configuración de marketing**, seleccione **Proceso**, **Funciones** y, a continuación, **Validar configuración de registro de correo electrónico**.</span><span class="sxs-lookup"><span data-stu-id="c8ad3-119">Search for **Marketing Setup**, choose **Process**, then **Functions**, and then **Validate Email Logging Setup**.</span></span>

## <a name="viewing-email-message-exchanges-in-the-interaction-log"></a><span data-ttu-id="c8ad3-120">Visualización de los intercambios de mensajes de correo electrónico en el registro de interacciones</span><span class="sxs-lookup"><span data-stu-id="c8ad3-120">Viewing Email Message Exchanges in the Interaction Log</span></span>

[!INCLUDE[d365fin](includes/d365fin_md.md)] <span data-ttu-id="c8ad3-121">crea una entrada en la página **Log de interacción** cada vez que un vendedor y un contacto intercambian un mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="c8ad3-121">creates an entry on the **Interaction Log** page each time a salesperson and a contact exchange an email message.</span></span> <span data-ttu-id="c8ad3-122">Para ver el log de interacción, abra la ficha **Contacto** o **Vendedor/Comprador** correspondiente a la persona y, a continuación, elija **Navegar**, **Historial** y **Movimientos del log de interacción**.</span><span class="sxs-lookup"><span data-stu-id="c8ad3-122">To view the interaction log, open the **Contact** or **Salesperson\*Purchaser** card for the person, and then choose **Navigate**, **History**, and then choose **Interaction Log Entries**.</span></span> <span data-ttu-id="c8ad3-123">Hay algunas cosas que podemos hacer con cada entrada del registro, por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="c8ad3-123">There are a few things we can do with each entry in the log, for example:</span></span>

- <span data-ttu-id="c8ad3-124">Ver el contenido del mensaje de correo electrónico que se ha intercambiado haciendo clic en la acción **Mostrar datos adjuntos**.</span><span class="sxs-lookup"><span data-stu-id="c8ad3-124">View the content of the email message that was exchanged by clicking the **Show Attachments** action.</span></span>
- <span data-ttu-id="c8ad3-125">Convertir un intercambio de correos electrónicos en una oportunidad de ventas. Si una entrada parece prometedora, puede convertirla en una oportunidad y luego administrar su progreso hasta una venta.</span><span class="sxs-lookup"><span data-stu-id="c8ad3-125">Turn an email exchange into a sales opportunity - If an entry looks promising, you can turn it into an opportunity and then manage its progress toward a sale.</span></span> <span data-ttu-id="c8ad3-126">Para hacerlo, seleccione la entrada y, a continuación, seleccione la acción **Crear oportunidad**.</span><span class="sxs-lookup"><span data-stu-id="c8ad3-126">To do that, choose the entry, and then choose the **Create Opportunity** action.</span></span> <span data-ttu-id="c8ad3-127">Para obtener más información, consulte [Administrar oportunidades de venta](marketing-manage-sales-opportunities.md).</span><span class="sxs-lookup"><span data-stu-id="c8ad3-127">For more information, see [Managing Sales Opportunities](marketing-manage-sales-opportunities.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="c8ad3-128">Consulte también</span><span class="sxs-lookup"><span data-stu-id="c8ad3-128">See Also</span></span>
[<span data-ttu-id="c8ad3-129">Gestionar las relaciones</span><span class="sxs-lookup"><span data-stu-id="c8ad3-129">Managing Relationships</span></span>](marketing-relationship-management.md)

