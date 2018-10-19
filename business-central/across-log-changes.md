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
ms.date: 10/01/2018
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: ab9696a3cc14970def764b2741d50dbcd5207460
ms.contentlocale: es-es
ms.lasthandoff: 09/28/2018

---
# <a name="logging-changes-in-business-central"></a><span data-ttu-id="47ff6-103">Registrar cambios en Business Central</span><span class="sxs-lookup"><span data-stu-id="47ff6-103">Logging Changes in Business Central</span></span>
<span data-ttu-id="47ff6-104">Puede habilitar el registro de cambios en [!INCLUDE[d365fin](includes/d365fin_md.md)] para tener un historial de actividades.</span><span class="sxs-lookup"><span data-stu-id="47ff6-104">You can enable the change log in [!INCLUDE[d365fin](includes/d365fin_md.md)] so you have a history of activities.</span></span> <span data-ttu-id="47ff6-105">El registro se basa en los cambios realizados en los datos en las tablas que se siguen. En el registro de cambios, los movimientos se ordenan cronológicamente y se muestran los cambios realizados a los campos de las tablas especificadas.</span><span class="sxs-lookup"><span data-stu-id="47ff6-105">The log is based on changes that are made to data in the tables that you track. In the change log, entries are chronologically ordered and show changes that are made to the fields on the specified tables.</span></span> <span data-ttu-id="47ff6-106">El registro de cambios recopila todos los cambios que se han realizado en la tabla.</span><span class="sxs-lookup"><span data-stu-id="47ff6-106">The change log collects all changes that are made to the table.</span></span>  

## <a name="working-with-the-change-log"></a><span data-ttu-id="47ff6-107">Trabajar con el registro de cambios</span><span class="sxs-lookup"><span data-stu-id="47ff6-107">Working with the Change Log</span></span>
<span data-ttu-id="47ff6-108">Un problema habitual en muchos sistemas financieros es localizar el origen de errores y modificaciones en los datos.</span><span class="sxs-lookup"><span data-stu-id="47ff6-108">A common problem in many financial systems is to locate the origin of errors and changes in data.</span></span> <span data-ttu-id="47ff6-109">Podría ser cualquier cosa, desde un número de teléfono incorrecto de un cliente hasta un registro incorrecto en la contabilidad.</span><span class="sxs-lookup"><span data-stu-id="47ff6-109">It could be anything from an incorrect customer telephone number to an incorrect posting to the general ledger.</span></span> <span data-ttu-id="47ff6-110">El registro de cambios permite realizar un seguimiento de todas las modificaciones directas que realiza un usuario a los datos de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="47ff6-110">The change log lets you track all direct modifications a user makes to data in the database.</span></span> <span data-ttu-id="47ff6-111">Debe especificar para cada tabla y campo lo que desea que el sistema registre y, a continuación, debe activar el registro de cambios.</span><span class="sxs-lookup"><span data-stu-id="47ff6-111">You must specify each table and field that you want the system to log, and then you must activate the change log.</span></span>  

<span data-ttu-id="47ff6-112">El registro de cambios se activa y desactiva en la ventana **Config. log cambio**.</span><span class="sxs-lookup"><span data-stu-id="47ff6-112">You activate and deactivate the change log in the **Change Log Setup** window.</span></span> <span data-ttu-id="47ff6-113">Al activar o desactivar el registro de cambios, se registra esta actividad, de modo que siempre puede ver qué usuario ha activado o reactivado el registro de cambios.</span><span class="sxs-lookup"><span data-stu-id="47ff6-113">When you activate or deactivate the change log, this activity is logged, so you can always see which user deactivated or reactivated the change log.</span></span> <span data-ttu-id="47ff6-114">Esto no puede desactivarse.</span><span class="sxs-lookup"><span data-stu-id="47ff6-114">This cannot be turned off.</span></span>  

<span data-ttu-id="47ff6-115">En la ventana **Config. log cambio**, si elige la acción **Tablas**, puede especificar de qué tablas que desea realizar el seguimiento de los cambios y de qué cambios desea efectuar el seguimiento. [!INCLUDE[d365fin](includes/d365fin_md.md)] también realiza el seguimiento de varias tablas del sistema.</span><span class="sxs-lookup"><span data-stu-id="47ff6-115">In the **Change Log Setup** window, if you choose the **Tables** action, you can specify which tables you want to track changes for, and which changes to track. [!INCLUDE[d365fin](includes/d365fin_md.md)] also tracks a number of system tables.</span></span>

<span data-ttu-id="47ff6-116">Después de haber configurado el registro de cambios, haberlo activado y alguien haya realizado un cambio en los datos, puede ver y filtrar los cambios en la ventana **Movs. registro cambios**.</span><span class="sxs-lookup"><span data-stu-id="47ff6-116">After you have set up the change log, activated it, and made a change to data, you can view and filter the changes in the **Change Log Entries** window.</span></span> <span data-ttu-id="47ff6-117">Si desea eliminar movimientos, puede hacerlo en la ventana **Eliminar movs. reg. de cambios**, donde puede definir filtros basados en fechas y horas.</span><span class="sxs-lookup"><span data-stu-id="47ff6-117">If you want to delete entries, you can do that in the **Delete Change Log Entries** window, where you can set filters based on dates and time.</span></span>  

## <a name="see-also"></a><span data-ttu-id="47ff6-118">Consulte también</span><span class="sxs-lookup"><span data-stu-id="47ff6-118">See Also</span></span>
[<span data-ttu-id="47ff6-119">Cambiar la configuración básica</span><span class="sxs-lookup"><span data-stu-id="47ff6-119">Changing Basic Settings</span></span>](ui-change-basic-settings.md)  
[<span data-ttu-id="47ff6-120">Ordenación</span><span class="sxs-lookup"><span data-stu-id="47ff6-120">Sorting</span></span>](ui-sorting.md)  
[<span data-ttu-id="47ff6-121">Buscar página o informe</span><span class="sxs-lookup"><span data-stu-id="47ff6-121">Using Search for Page or Report</span></span>](ui-search.md)  
<span data-ttu-id="47ff6-122">[Gestionar usuarios y permisos](ui-how-users-permissions.md)  </span><span class="sxs-lookup"><span data-stu-id="47ff6-122">[Managing Users and Permissions](ui-how-users-permissions.md)  </span></span>  
<span data-ttu-id="47ff6-123">[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="47ff6-123">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

