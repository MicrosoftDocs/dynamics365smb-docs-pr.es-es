---
title: Ver bloqueos de base de datos
description: Descubra cómo puede ver información sobre cualquier bloqueo de base de datos directamente desde la interfaz del cliente en Business Central.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 04/01/2021
ms.author: jswymer
ms.openlocfilehash: b53677ab57d6c48b015bb0dd47ea6e315f8e80c3
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 03/31/2021
ms.locfileid: "5776921"
---
# <a name="viewing-database-locks"></a><span data-ttu-id="deeb4-103">Ver bloqueos de base de datos</span><span class="sxs-lookup"><span data-stu-id="deeb4-103">Viewing Database Locks</span></span>

<span data-ttu-id="deeb4-104">El bloqueo de la base de datos controla el acceso de múltiples usuarios a los mismos datos al mismo tiempo.</span><span class="sxs-lookup"><span data-stu-id="deeb4-104">Database locking controls access by multiple users to the same data at the same time.</span></span> <span data-ttu-id="deeb4-105">Para proteger una transacción contra otras transacciones que modifican los mismos datos, la primera transacción bloquea los datos.</span><span class="sxs-lookup"><span data-stu-id="deeb4-105">To protect a transaction against other transactions modifying the same data, the first transaction puts a lock on the data.</span></span> <span data-ttu-id="deeb4-106">El bloqueo permanece hasta que se realiza la transacción.</span><span class="sxs-lookup"><span data-stu-id="deeb4-106">The lock remains until the transaction's done.</span></span>

<span data-ttu-id="deeb4-107">Los usuarios pueden ser bloqueados para completar transacciones en los datos bloqueados.</span><span class="sxs-lookup"><span data-stu-id="deeb4-107">Users may be blocked from completing transactions on the locked data.</span></span> <span data-ttu-id="deeb4-108">Por lo general, recibirán un mensaje que indica la condición de bloqueo.</span><span class="sxs-lookup"><span data-stu-id="deeb4-108">They'll typically get a message that indicates the lock condition.</span></span>

## <a name="to-view-database-locks"></a><span data-ttu-id="deeb4-109">Para ver bloqueos de base de datos</span><span class="sxs-lookup"><span data-stu-id="deeb4-109">To view database locks</span></span>

<span data-ttu-id="deeb4-110">Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "Icono Buscar página o informe"), introduzca **Bloqueos de base de datos** y, a continuación, seleccione el vínculo relacionado.</span><span class="sxs-lookup"><span data-stu-id="deeb4-110">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Database Locks**, and then choose the related link.</span></span>

<span data-ttu-id="deeb4-111">La página **Bloqueos de base de datos** proporciona una instantánea de todos los bloqueos de la base de datos actual.</span><span class="sxs-lookup"><span data-stu-id="deeb4-111">The **Database Locks** page gives snapshot of all current database locks.</span></span>

<span data-ttu-id="deeb4-112">Para obtener más información sobre el bloqueo de base de datos, vea [Supervisión de bloqueos de base de datos](/dynamics365/business-central/dev-itpro/administration/monitor-database-locks) en la ayuda de Business Central Developer e IT Pro.</span><span class="sxs-lookup"><span data-stu-id="deeb4-112">For more information about database locking, see [Monitoring Database Locks](/dynamics365/business-central/dev-itpro/administration/monitor-database-locks) in the Business Central Developer and IT Pro help.</span></span>

## <a name="see-also"></a><span data-ttu-id="deeb4-113">Consulte también</span><span class="sxs-lookup"><span data-stu-id="deeb4-113">See Also</span></span>

[<span data-ttu-id="deeb4-114">Supervisar bloqueos de base de datos</span><span class="sxs-lookup"><span data-stu-id="deeb4-114">Monitor Database Locks</span></span>](/dynamics365/business-central/dev-itpro/administration/monitor-database-locks) 


[!INCLUDE[footer-include](includes/footer-banner.md)]