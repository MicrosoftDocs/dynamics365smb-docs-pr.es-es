---
title: Realizar el seguimiento de la actividad de usuario en un registro de cambios | Documentos de Microsoft
description: Puede activar el registro de usuario para tener un historial de los cambios realizados en los datos de las tablas de las que se hace el seguimiento.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: user log, user activity, tracking
ms.date: 11/14/2018
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: 59afb06e9d43bdadc5ceacf563a9e6faf7439b7b
ms.openlocfilehash: bc56e07a540c24f53b88651ad2b2ff5e1e56a571
ms.contentlocale: es-es
ms.lasthandoff: 12/05/2018

---
# <a name="auditing-changes-in-business-central"></a><span data-ttu-id="6bec7-103">Auditar cambios en Business Central</span><span class="sxs-lookup"><span data-stu-id="6bec7-103">Auditing Changes in Business Central</span></span>

<span data-ttu-id="6bec7-104">Puede habilitar el registro de cambios en [!INCLUDE[d365fin](includes/d365fin_md.md)] para tener un historial de actividades.</span><span class="sxs-lookup"><span data-stu-id="6bec7-104">You can enable the change log in [!INCLUDE[d365fin](includes/d365fin_md.md)] so you have a history of activities.</span></span> <span data-ttu-id="6bec7-105">El registro se basa en los cambios realizados en los datos en las tablas que se siguen. En la página **Cambiar entradas del registro**, las entradas se ordenan cronológicamente y se muestran los cambios realizados a los campos de las tablas especificadas.</span><span class="sxs-lookup"><span data-stu-id="6bec7-105">The log is based on changes that are made to data in the tables that you track. On the **Change Log Entries** page, entries are chronologically ordered and show changes that are made to the fields on the specified tables.</span></span> <span data-ttu-id="6bec7-106">El registro de cambios recopila todos los cambios que se han realizado en la tabla.</span><span class="sxs-lookup"><span data-stu-id="6bec7-106">The change log collects all changes that are made to the table.</span></span>

> [!Important]
> <span data-ttu-id="6bec7-107">Los cambios de un usuario no son visibles en **Cambiar entradas del registro** hasta que se reinicia la sesión del usuario, lo que ocurre en los siguientes casos:</span><span class="sxs-lookup"><span data-stu-id="6bec7-107">A user's changes are not visible in the **Change Log Entries** until the user's session is restarted, which happens in the following cases:</span></span>
<br />
> * <span data-ttu-id="6bec7-108">La sesión ha caducado y se ha actualizado.</span><span class="sxs-lookup"><span data-stu-id="6bec7-108">The session expired and was refreshed.</span></span>
> * <span data-ttu-id="6bec7-109">El usuario seleccionó otra empresa o área de trabajo.</span><span class="sxs-lookup"><span data-stu-id="6bec7-109">The user selected another company or Role Center.</span></span>
> * <span data-ttu-id="6bec7-110">El usuario ha salido y ha vuelto a entrar.</span><span class="sxs-lookup"><span data-stu-id="6bec7-110">The user signed out and back in.</span></span>

## <a name="working-with-the-change-log"></a><span data-ttu-id="6bec7-111">Trabajar con el registro de cambios</span><span class="sxs-lookup"><span data-stu-id="6bec7-111">Working with the Change Log</span></span>

<span data-ttu-id="6bec7-112">Un problema habitual en muchos sistemas financieros es localizar el origen de errores y modificaciones en los datos.</span><span class="sxs-lookup"><span data-stu-id="6bec7-112">A common problem in many financial systems is to locate the origin of errors and changes in data.</span></span> <span data-ttu-id="6bec7-113">Podría ser cualquier cosa, desde un número de teléfono incorrecto de un cliente hasta un registro incorrecto en la contabilidad.</span><span class="sxs-lookup"><span data-stu-id="6bec7-113">It could be anything from an incorrect customer telephone number to an incorrect posting to the general ledger.</span></span> <span data-ttu-id="6bec7-114">El registro de cambios permite realizar un seguimiento de todas las modificaciones directas que realiza un usuario a los datos de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="6bec7-114">The change log lets you track all direct modifications a user makes to data in the database.</span></span> <span data-ttu-id="6bec7-115">Debe especificar para cada tabla y campo lo que desea que el sistema registre y, a continuación, debe activar el registro de cambios.</span><span class="sxs-lookup"><span data-stu-id="6bec7-115">You must specify each table and field that you want the system to log, and then you must activate the change log.</span></span>  

<span data-ttu-id="6bec7-116">El registro de cambios se activa y desactiva en la página **Config. log cambio**.</span><span class="sxs-lookup"><span data-stu-id="6bec7-116">You activate and deactivate the change log on the **Change Log Setup** page.</span></span> <span data-ttu-id="6bec7-117">Si un usuario activa o desactiva el registro de cambios, se registra esta actividad, de modo que siempre puede ver qué usuario ha activado o reactivado el registro de cambios.</span><span class="sxs-lookup"><span data-stu-id="6bec7-117">When a user activates or deactivates the change log, this activity is logged, so you can always see which user deactivated or reactivated the change log.</span></span>

<span data-ttu-id="6bec7-118">En la página **Config. log cambio**, si elige la acción **Tablas**, puede especificar de qué tablas que desea realizar el seguimiento de los cambios y de qué cambios desea efectuar el seguimiento. [!INCLUDE[d365fin](includes/d365fin_md.md)] también realiza el seguimiento de varias tablas del sistema.</span><span class="sxs-lookup"><span data-stu-id="6bec7-118">On the **Change Log Setup** page, if you choose the **Tables** action, you can specify which tables you want to track changes for, and which changes to track. [!INCLUDE[d365fin](includes/d365fin_md.md)] also tracks a number of system tables.</span></span>

<span data-ttu-id="6bec7-119">Después de haber configurado el registro de cambios, haberlo activado y alguien haya realizado un cambio en los datos, puede ver y filtrar los cambios en la página **Movs. registro cambios**.</span><span class="sxs-lookup"><span data-stu-id="6bec7-119">After you have set up the change log, activated it, and made a change to data, you can view and filter the changes on the **Change Log Entries** page.</span></span> <span data-ttu-id="6bec7-120">Si desea eliminar movimientos, puede hacerlo en la página **Eliminar movs. reg. de cambios**, donde puede definir filtros basados en fechas y horas.</span><span class="sxs-lookup"><span data-stu-id="6bec7-120">If you want to delete entries, you can do that on the **Delete Change Log Entries** page, where you can set filters based on dates and time.</span></span>  

## <a name="see-also"></a><span data-ttu-id="6bec7-121">Consulte también</span><span class="sxs-lookup"><span data-stu-id="6bec7-121">See Also</span></span>
[<span data-ttu-id="6bec7-122">Cambiar la configuración básica</span><span class="sxs-lookup"><span data-stu-id="6bec7-122">Changing Basic Settings</span></span>](ui-change-basic-settings.md)  
[<span data-ttu-id="6bec7-123">Ordenación</span><span class="sxs-lookup"><span data-stu-id="6bec7-123">Sorting</span></span>](ui-sorting.md)  
[<span data-ttu-id="6bec7-124">Buscar página o informe</span><span class="sxs-lookup"><span data-stu-id="6bec7-124">Using Search for Page or Report</span></span>](ui-search.md)  
<span data-ttu-id="6bec7-125">[Gestionar usuarios y permisos](ui-how-users-permissions.md)  </span><span class="sxs-lookup"><span data-stu-id="6bec7-125">[Managing Users and Permissions](ui-how-users-permissions.md)  </span></span>  
<span data-ttu-id="6bec7-126">[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="6bec7-126">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

