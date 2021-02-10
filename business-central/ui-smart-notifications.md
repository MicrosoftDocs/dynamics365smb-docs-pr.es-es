---
title: Trabajo con notificaciones inteligentes y especificar cuándo aparecen | Documentos de Microsoft
description: Puede recibir notificaciones que le informen sobre los cambios de estado o los eventos, por ejemplo, un saldo pendiente o inventario bajo.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 10/01/2020
ms.author: bholtorf
ms.openlocfilehash: a297fd8381cf0af9de825cdaced658521e0335c8
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "4756647"
---
# <a name="manage-notifications"></a><span data-ttu-id="26f1c-103">Administrar notificaciones</span><span class="sxs-lookup"><span data-stu-id="26f1c-103">Manage Notifications</span></span>

[!INCLUDE[prod_short](includes/prod_short.md)] <span data-ttu-id="26f1c-104">le puede ayudar a trabajar de una forma más inteligente con las notificaciones que le envía sobre determinados eventos o cambios de estado, cuando va a facturar a un cliente que tiene un saldo vencido o cuando el inventario disponible es inferior a la cantidad que va a vender, por ejemplo.</span><span class="sxs-lookup"><span data-stu-id="26f1c-104">can help you work smarter by notifying you about certain events or changes in status, such as when you are about to invoice a customer who has an overdue balance, or the available inventory is lower than the quantity you are about to sell, for example.</span></span> <span data-ttu-id="26f1c-105">Estas notificaciones se muestran como sugerencias discretas en el contexto de la tarea que está llevando acabo, y puede elegir si las ignora o lee más detalles acerca del problema.</span><span class="sxs-lookup"><span data-stu-id="26f1c-105">These notifications are shown as discreet tips in the context of the task you are doing, and you can choose to ignore the notification or to see details about the issue.</span></span>  

<span data-ttu-id="26f1c-106">Si elige ver los detalles de una notificación, puede intentar resolver el problema como, por ejemplo, poniéndose en contacto con el cliente, comprando más artículos para el inventario, etc.</span><span class="sxs-lookup"><span data-stu-id="26f1c-106">If you choose to see details for a notification, you can take action to resolve the issue, such as contacting the customer, buying more inventory, and so on.</span></span> <span data-ttu-id="26f1c-107">Puede decidir qué hacer y [!INCLUDE[prod_short](includes/prod_short.md)] le proporciona consejos y recomendaciones.</span><span class="sxs-lookup"><span data-stu-id="26f1c-107">It's your choice what to do, and [!INCLUDE[prod_short](includes/prod_short.md)] gives you advice and recommendations.</span></span>  

<span data-ttu-id="26f1c-108">Las notificaciones pueden ayudar a los usuarios no experimentados a completar tareas que les resultan difíciles y a los más experimentados, a no reducir la productividad.</span><span class="sxs-lookup"><span data-stu-id="26f1c-108">Notifications can help untrained users complete unfamiliar tasks, and do not reduce productivity for the more trained user.</span></span>  

## <a name="to-turn-notifications-on-or-off-and-control-when-they-are-sent"></a><span data-ttu-id="26f1c-109">Para activar o desactivar notificaciones y controlar cuándo se envían</span><span class="sxs-lookup"><span data-stu-id="26f1c-109">To turn notifications on or off, and control when they are sent</span></span>

<span data-ttu-id="26f1c-110">Al empezar por primera vez con [!INCLUDE[prod_short](includes/prod_short.md)] todas las notificaciones están activadas, pero las puede activar o desactivar, por ejemplo, si no le interesa un determinado evento o estado.</span><span class="sxs-lookup"><span data-stu-id="26f1c-110">When you first start with [!INCLUDE[prod_short](includes/prod_short.md)] all notifications are turned on, but you can turn them on or off, for example, if you aren't interested in a certain event or status.</span></span>  

<span data-ttu-id="26f1c-111">Además, algunas notificaciones le permiten especificar las condiciones en las que se envían.</span><span class="sxs-lookup"><span data-stu-id="26f1c-111">Additionally, some notifications let you specify the conditions under which they are sent.</span></span> <span data-ttu-id="26f1c-112">Por ejemplo, si desea recibir una notificación cuando quede poco inventario, pero solo de los productos que compra a un determinado proveedor.</span><span class="sxs-lookup"><span data-stu-id="26f1c-112">For example, if you want to be notified when inventory is running low, but only for items you buy from a certain vendor.</span></span>  

<span data-ttu-id="26f1c-113">La activación o la desactivación de las notificaciones, y la especificación de las condiciones, solo se aplican a su caso.</span><span class="sxs-lookup"><span data-stu-id="26f1c-113">Turning notifications on or off, and specifying conditions, applies only to you.</span></span>  

1. <span data-ttu-id="26f1c-114">En la esquina superior derecha, elija el icono **Configuración** ![Configuración](media/ui-experience/settings_icon_small.png "Icono de configuración para el área de trabajo") y, a continuación, elija la acción **Mi configuración**.</span><span class="sxs-lookup"><span data-stu-id="26f1c-114">In the top right corner, choose the **Settings** icon ![Settings](media/ui-experience/settings_icon_small.png "Settings icon for role center"), and then choose the **My Settings** action.</span></span>  
2. <span data-ttu-id="26f1c-115">En la página **Mi configuración**, en el campo **Notificaciones**, elija el vínculo *Cambiar cuándo recibo notificaciones*</span><span class="sxs-lookup"><span data-stu-id="26f1c-115">On the **My Settings** page, in the **Notifications** field, choose the *Change when I receive notifications.*</span></span> <span data-ttu-id="26f1c-116">.</span><span class="sxs-lookup"><span data-stu-id="26f1c-116">link.</span></span>  
3. <span data-ttu-id="26f1c-117">En la página que aparece, active o desactive una notificación activando o desactivando la casilla **Habilitado**.</span><span class="sxs-lookup"><span data-stu-id="26f1c-117">In the page that appears, turn on or turn off a notification by selecting or clearing the **Enabled** check box.</span></span>  
4. <span data-ttu-id="26f1c-118">Para especificar las condiciones que activan una notificación, seleccione el vínculo **Ver detalles de filtro** y rellene los campos.</span><span class="sxs-lookup"><span data-stu-id="26f1c-118">To specify conditions that trigger a notification, choose the **View filter details** link, and then fill in the fields.</span></span>  

## <a name="see-also"></a><span data-ttu-id="26f1c-119">Consulte también</span><span class="sxs-lookup"><span data-stu-id="26f1c-119">See Also</span></span>

<span data-ttu-id="26f1c-120">[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="26f1c-120">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>
