---
title: Obtener clientes en la experiencia contable de Dynamics 365 | Documentos de Microsoft
description: "Información sobre cómo agregar clientes existentes al Accountant Hub de Dynamics 365."
author: edupont04
ms.service: dynamics365-accountant
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: accountant, accounting, financial report
ms.date: 10/23/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: 75501b9402bb1c14fcfeb2fc6e61f055a2247493
ms.openlocfilehash: 8b8d92e114733d87b1866d66ee3111208e233ad3
ms.contentlocale: es-es
ms.lasthandoff: 05/15/2018

---
# <a name="add-clients-to-your-dashboard-in-include-d365acclongincludesd365acclongmdmd"></a><span data-ttu-id="2104c-103">Agregar clientes al escritorio de [!INCLUDE [d365acc_long](includes/d365acc_long_md.md)]</span><span class="sxs-lookup"><span data-stu-id="2104c-103">Add Clients to Your Dashboard in [!INCLUDE [d365acc_long](includes/d365acc_long_md.md)]</span></span>
[!INCLUDE [d365fin_early_release](includes/d365fin_early_release.md.md)]

<span data-ttu-id="2104c-104">Puede agregar un cliente mediante la ventana **Clientes** que puede abrir con la acción **Administrar clientes** de la cinta.</span><span class="sxs-lookup"><span data-stu-id="2104c-104">You can add a client by using the **Clients** window, which you can open by choosing the **Manage Clients** action in the ribbon.</span></span> <span data-ttu-id="2104c-105">Simplemente, elija **Nuevo** y, a continuación, rellene los campos.</span><span class="sxs-lookup"><span data-stu-id="2104c-105">Simply choose **New** and then fill in the fields.</span></span>  

![Agregar un cliente](./media/accountant-add-client/manage-client.png)

<span data-ttu-id="2104c-107">Los datos de la tarjeta para cada cliente los especifica el usuario, y puede cambiarlos según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="2104c-107">The data in the card for each client is specified by you, and you can change it as needed.</span></span> <span data-ttu-id="2104c-108">Sin embargo, el campo **Dirección URL del cliente** es fundamental ya que así es como puede acceder al [!INCLUDE [d365fin](includes/d365fin_md.md)] de cada cliente.</span><span class="sxs-lookup"><span data-stu-id="2104c-108">However, the **Client URL** field is critical - this is how you can access each client's [!INCLUDE [d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="2104c-109">Utilice la acción **URL de prueba del cliente** de la cinta para comprobar que ha introducido el vínculo correcto.</span><span class="sxs-lookup"><span data-stu-id="2104c-109">Use the **Test Client URL** action in the ribbon to test that you entered the right link.</span></span> <span data-ttu-id="2104c-110">La dirección URL que debe introducir apunta en el [!INCLUDE [d365fin](includes/d365fin_md.md)] del cliente, como *<https://mybusiness.financials.dynamics.com>*.</span><span class="sxs-lookup"><span data-stu-id="2104c-110">The URL that you must enter points at the client's [!INCLUDE [d365fin](includes/d365fin_md.md)], such as *<https://mybusiness.financials.dynamics.com>*.</span></span> <span data-ttu-id="2104c-111">Esta URL se utiliza cuando se elige el elemento de menú **Ir a empresa** en el panel de [!INCLUDE [d365acc](includes/d365acc_md.md)].</span><span class="sxs-lookup"><span data-stu-id="2104c-111">This URL is then used when you choose the **Go To Company** menu item in the [!INCLUDE [d365acc](includes/d365acc_md.md)] dashboard.</span></span>  

### <a name="get-invited-to-a-clients-include-d365finlongincludesd365finlongmdmd"></a><span data-ttu-id="2104c-112">Obtenga una invitación a un [!INCLUDE [d365fin_long](includes/d365fin_long_md.md)] de cliente</span><span class="sxs-lookup"><span data-stu-id="2104c-112">Get Invited to a Client's [!INCLUDE [d365fin_long](includes/d365fin_long_md.md)]</span></span>
<span data-ttu-id="2104c-113">Una empresa que utiliza [!INCLUDE [d365fin](includes/d365fin_md.md)] puede invitarle a [!INCLUDE [d365fin](includes/d365fin_md.md)] como su contable externo.</span><span class="sxs-lookup"><span data-stu-id="2104c-113">A company who use [!INCLUDE [d365fin](includes/d365fin_md.md)] can invite you to [!INCLUDE [d365fin](includes/d365fin_md.md)] as their external accountant.</span></span> <span data-ttu-id="2104c-114">Para recibir una invitación, debe proporcionar el correo electrónico que utiliza con [!INCLUDE [d365acc](includes/d365acc_md.md)], como <em>me@accountant.com</em>. El administrador de su cliente puede agregarlo a su sistema con el asistente **Invitar a contable externo**.</span><span class="sxs-lookup"><span data-stu-id="2104c-114">To get invited, you must give them the email that you use with [!INCLUDE [d365acc](includes/d365acc_md.md)], such as <em>me@accountant.com</em>. Your client's administrator can then add you to their system by running the **Invite External Accountant** wizard.</span></span>  

<span data-ttu-id="2104c-115">Como resultado, recibirá el correo electrónico del cliente con vínculos a [!INCLUDE [d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="2104c-115">As a result, you will receive email from your client with links to their [!INCLUDE [d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="2104c-116">El primer enlace es una invitación para acceder a su empresa: ábralo y acepte los pasos que lo incorporan al [!INCLUDE [d365fin](includes/d365fin_md.md)] de su cliente.</span><span class="sxs-lookup"><span data-stu-id="2104c-116">The first link is an invitation to get access to their company - open the link and accept the steps that adds you to your client's [!INCLUDE [d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="2104c-117">El segundo enlace es para agregar este cliente a su escritorio en [!INCLUDE [d365acc](includes/d365acc_md.md)] como se describe anteriormente.</span><span class="sxs-lookup"><span data-stu-id="2104c-117">The second link is for adding this client to your dashboard in [!INCLUDE [d365acc](includes/d365acc_md.md)] as described above.</span></span>  

<span data-ttu-id="2104c-118">Cuando haya aceptado la invitación, iniciará sesión y podrá acceder a los datos financieros del cliente desde el Área de trabajo **Contable**.</span><span class="sxs-lookup"><span data-stu-id="2104c-118">When you have accepted the invitation, you are logged in and can access the client's financial data from the **Accountant** Role Center.</span></span> <span data-ttu-id="2104c-119">Para obtener más información, vea [Experiencias contables en [!INCLUDE[d365fin](includes/d365fin_md.md)]](/dynamics365/business-central/finance-accounting?toc=/dynamics365/accountants/toc.json).</span><span class="sxs-lookup"><span data-stu-id="2104c-119">For more information, see [Accountant Experiences in [!INCLUDE[d365fin](includes/d365fin_md.md)]](/dynamics365/business-central/finance-accounting?toc=/dynamics365/accountants/toc.json).</span></span>  

## <a name="see-also"></a><span data-ttu-id="2104c-120">Consulte también</span><span class="sxs-lookup"><span data-stu-id="2104c-120">See Also</span></span>
<span data-ttu-id="2104c-121">[Introducción a [!INCLUDE[d365acc](includes/d365acc_md.md)]](get-started.md)</span><span class="sxs-lookup"><span data-stu-id="2104c-121">[Get Started with [!INCLUDE[d365acc](includes/d365acc_md.md)]](get-started.md)</span></span>  
<span data-ttu-id="2104c-122">[Solución de problemas de [!INCLUDE[d365acc](includes/d365acc_md.md)]](troubleshooting.md)</span><span class="sxs-lookup"><span data-stu-id="2104c-122">[Troubleshooting [!INCLUDE[d365acc](includes/d365acc_md.md)]](troubleshooting.md)</span></span>  

