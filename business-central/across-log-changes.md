---
title: Auditar cambios | Documentos de Microsoft
description: Puede activar el registro de usuario para tener un historial de los cambios realizados en los datos de las tablas de las que se hace el seguimiento. También puede realizar un seguimiento de actividades con ciertos tipos de registros de actividad.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: user log, user activity, tracking
ms.date: 10/01/2019
ms.author: edupont
ms.openlocfilehash: 43aea054ce4e66e9108f408d96c2eb491351b382
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/01/2019
ms.locfileid: "2304940"
---
# <a name="auditing-changes-in-business-central"></a><span data-ttu-id="9bcf0-104">Auditar cambios en Business Central</span><span class="sxs-lookup"><span data-stu-id="9bcf0-104">Auditing Changes in Business Central</span></span>

<span data-ttu-id="9bcf0-105">Puede habilitar el registro de cambios en [!INCLUDE[d365fin](includes/d365fin_md.md)] para tener un historial de actividades.</span><span class="sxs-lookup"><span data-stu-id="9bcf0-105">You can enable the change log in [!INCLUDE[d365fin](includes/d365fin_md.md)] so you have a history of activities.</span></span> <span data-ttu-id="9bcf0-106">El registro se basa en los cambios realizados en los datos en las tablas que se siguen. En la página **Cambiar entradas del registro**, las entradas se ordenan cronológicamente y se muestran los cambios realizados a los campos de las tablas especificadas.</span><span class="sxs-lookup"><span data-stu-id="9bcf0-106">The log is based on changes that are made to data in the tables that you track. On the **Change Log Entries** page, entries are chronologically ordered and show changes that are made to the fields on the specified tables.</span></span> <span data-ttu-id="9bcf0-107">El registro de cambios recopila todos los cambios que se han realizado en la tabla.</span><span class="sxs-lookup"><span data-stu-id="9bcf0-107">The change log collects all changes that are made to the table.</span></span>

> [!Important]
> <span data-ttu-id="9bcf0-108">Los cambios de un usuario no son visibles en **Cambiar entradas del registro** hasta que se reinicia la sesión del usuario, lo que ocurre en los siguientes casos:</span><span class="sxs-lookup"><span data-stu-id="9bcf0-108">A user's changes are not visible in the **Change Log Entries** until the user's session is restarted, which happens in the following cases:</span></span>
<br />
> * <span data-ttu-id="9bcf0-109">La sesión ha caducado y se ha actualizado.</span><span class="sxs-lookup"><span data-stu-id="9bcf0-109">The session expired and was refreshed.</span></span>
> * <span data-ttu-id="9bcf0-110">El usuario seleccionó otra empresa o área de trabajo.</span><span class="sxs-lookup"><span data-stu-id="9bcf0-110">The user selected another company or Role Center.</span></span>
> * <span data-ttu-id="9bcf0-111">El usuario ha salido y ha vuelto a entrar.</span><span class="sxs-lookup"><span data-stu-id="9bcf0-111">The user signed out and back in.</span></span>

## <a name="working-with-the-change-log"></a><span data-ttu-id="9bcf0-112">Trabajar con el registro de cambios</span><span class="sxs-lookup"><span data-stu-id="9bcf0-112">Working with the Change Log</span></span>

<span data-ttu-id="9bcf0-113">Un problema habitual en muchos sistemas financieros es localizar el origen de errores y modificaciones en los datos.</span><span class="sxs-lookup"><span data-stu-id="9bcf0-113">A common problem in many financial systems is to locate the origin of errors and changes in data.</span></span> <span data-ttu-id="9bcf0-114">Podría ser cualquier cosa, desde un número de teléfono incorrecto de un cliente hasta un registro incorrecto en la contabilidad.</span><span class="sxs-lookup"><span data-stu-id="9bcf0-114">It could be anything from an incorrect customer telephone number to an incorrect posting to the general ledger.</span></span> <span data-ttu-id="9bcf0-115">El registro de cambios permite realizar un seguimiento de todas las modificaciones directas que realiza un usuario a los datos de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="9bcf0-115">The change log lets you track all direct modifications a user makes to data in the database.</span></span> <span data-ttu-id="9bcf0-116">Debe especificar para cada tabla y campo lo que desea que el sistema registre y, a continuación, debe activar el registro de cambios.</span><span class="sxs-lookup"><span data-stu-id="9bcf0-116">You must specify each table and field that you want the system to log, and then you must activate the change log.</span></span>  

<span data-ttu-id="9bcf0-117">El registro de cambios se activa y desactiva en la página **Config. log cambio**.</span><span class="sxs-lookup"><span data-stu-id="9bcf0-117">You activate and deactivate the change log on the **Change Log Setup** page.</span></span> <span data-ttu-id="9bcf0-118">Si un usuario activa o desactiva el registro de cambios, se registra esta actividad, de modo que siempre puede ver qué usuario ha activado o reactivado el registro de cambios.</span><span class="sxs-lookup"><span data-stu-id="9bcf0-118">When a user activates or deactivates the change log, this activity is logged, so you can always see which user deactivated or reactivated the change log.</span></span>

<span data-ttu-id="9bcf0-119">En la página **Config. log cambio**, si elige la acción **Tablas**, puede especificar de qué tablas que desea realizar el seguimiento de los cambios y de qué cambios desea efectuar el seguimiento. [!INCLUDE[d365fin](includes/d365fin_md.md)] también realiza el seguimiento de varias tablas del sistema.</span><span class="sxs-lookup"><span data-stu-id="9bcf0-119">On the **Change Log Setup** page, if you choose the **Tables** action, you can specify which tables you want to track changes for, and which changes to track. [!INCLUDE[d365fin](includes/d365fin_md.md)] also tracks a number of system tables.</span></span>

<span data-ttu-id="9bcf0-120">Después de haber configurado el registro de cambios, haberlo activado y alguien haya realizado un cambio en los datos, puede ver y filtrar los cambios en la página **Movs. registro cambios**.</span><span class="sxs-lookup"><span data-stu-id="9bcf0-120">After you have set up the change log, activated it, and made a change to data, you can view and filter the changes on the **Change Log Entries** page.</span></span> <span data-ttu-id="9bcf0-121">Si desea eliminar movimientos, puede hacerlo en la página **Eliminar movs. reg. de cambios**, donde puede definir filtros basados en fechas y horas.</span><span class="sxs-lookup"><span data-stu-id="9bcf0-121">If you want to delete entries, you can do that on the **Delete Change Log Entries** page, where you can set filters based on dates and time.</span></span>  

## <a name="working-with-activity-logs"></a><span data-ttu-id="9bcf0-122">Trabajar con registros de actividad</span><span class="sxs-lookup"><span data-stu-id="9bcf0-122">Working with Activity Logs</span></span>

<span data-ttu-id="9bcf0-123">Desde algunas páginas en [!INCLUDE [prodshort](includes/prodshort.md)], puede ver un registro de actividad que muestra el estado y los errores de los archivos que exporta o importa [!INCLUDE [prodshort](includes/prodshort.md)].</span><span class="sxs-lookup"><span data-stu-id="9bcf0-123">From some pages in [!INCLUDE [prodshort](includes/prodshort.md)], you can view an activity log that shows the status and any errors from files that you export from or import into [!INCLUDE [prodshort](includes/prodshort.md)].</span></span>  

<span data-ttu-id="9bcf0-124">La información se muestra en la ventana **Registro de actividad** según el contexto desde el que se abra.</span><span class="sxs-lookup"><span data-stu-id="9bcf0-124">The information is displayed in the **Activity Log** page, according to the context that it is opened from.</span></span> <span data-ttu-id="9bcf0-125">Puede abrir la ventana desde las páginas **Configuración del servicio de intercambio de documentos**, **Documento entrante**, **Histórico facturas venta** e **Histórico de abonos de venta**, por ejemplo.</span><span class="sxs-lookup"><span data-stu-id="9bcf0-125">You can open the window from the **Document Exchange Service Setup**, **Incoming Document**, **Posted Sales Invoice**, and **Posted Sales Credit Memo** pages, for example.</span></span> <span data-ttu-id="9bcf0-126">Puede vaciar la lista de entradas de registro o simplemente borrar la lista de entradas anteriores a 7 días.</span><span class="sxs-lookup"><span data-stu-id="9bcf0-126">You can empty the list of log entries, or just clear the list of entries older than 7 days.</span></span>  

## <a name="see-also"></a><span data-ttu-id="9bcf0-127">Consulte también</span><span class="sxs-lookup"><span data-stu-id="9bcf0-127">See Also</span></span>
[<span data-ttu-id="9bcf0-128">Cambiar la configuración básica</span><span class="sxs-lookup"><span data-stu-id="9bcf0-128">Change Basic Settings</span></span>](ui-change-basic-settings.md)  
[<span data-ttu-id="9bcf0-129">Ordenación</span><span class="sxs-lookup"><span data-stu-id="9bcf0-129">Sorting</span></span>](ui-sorting.md)  
[<span data-ttu-id="9bcf0-130">Búsqueda de páginas e información con Dígame</span><span class="sxs-lookup"><span data-stu-id="9bcf0-130">Finding Pages and Information with Tell Me</span></span>](ui-search.md)  
<span data-ttu-id="9bcf0-131">[Administrar usuarios y permisos](ui-how-users-permissions.md)  </span><span class="sxs-lookup"><span data-stu-id="9bcf0-131">[Manage Users and Permissions](ui-how-users-permissions.md)  </span></span>  
<span data-ttu-id="9bcf0-132">[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="9bcf0-132">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
