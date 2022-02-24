---
title: Ver bloqueos de base de datos
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 04/01/2020
ms.author: jswymer
ms.openlocfilehash: abee0f31d66f648f4b0be567d8599b31c536a193
ms.sourcegitcommit: 7d54d8abe52e0546378cf760f5082f46e8441b90
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/30/2020
ms.locfileid: "3324107"
---
# <a name="viewing-database-locks"></a>Ver bloqueos de base de datos

## <a name="about-locks"></a>Acerca de los bloqueos

El bloqueo de la base de datos controla el acceso de múltiples usuarios a los mismos datos al mismo tiempo. Para proteger una transacción contra otras transacciones que modifican los mismos datos, la primera transacción bloquea los datos. El bloqueo permanece hasta que se realiza la transacción.

Los usuarios pueden ser bloqueados para completar transacciones en los datos bloqueados. Por lo general, recibirán un mensaje que indica la condición de bloqueo.

## <a name="to-view-database-locks"></a>Para ver bloqueos de base de datos

Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "Icono Buscar página o informe"), introduzca **Bloqueos de base de datos** y, a continuación, seleccione el vínculo relacionado.

La página **Bloqueos de base de datos** proporciona una instantánea de todos los bloqueos de la base de datos actual.

Para obtener más información sobre el bloqueo de base de datos, vea [Supervisión de bloqueos de base de datos](/dynamics365/business-central/dev-itpro/administration/monitor-database-locks) en la ayuda de Business Central Developer e IT Pro.

## <a name="see-also"></a>Consulte también

[Supervisar bloqueos de base de datos](/dynamics365/business-central/dev-itpro/administration/monitor-database-locks) 
