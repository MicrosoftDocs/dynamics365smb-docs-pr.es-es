---
title: Ver bloqueos de base de datos
description: Descubra cómo puede ver información sobre cualquier bloqueo de base de datos directamente desde la interfaz del cliente en Business Central.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 10/01/2020
ms.author: jswymer
ms.openlocfilehash: 640608b810f3ad9812decc493ad4e35bcc316f98
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5388154"
---
# <a name="viewing-database-locks"></a>Ver bloqueos de base de datos

El bloqueo de la base de datos controla el acceso de múltiples usuarios a los mismos datos al mismo tiempo. Para proteger una transacción contra otras transacciones que modifican los mismos datos, la primera transacción bloquea los datos. El bloqueo permanece hasta que se realiza la transacción.

Los usuarios pueden ser bloqueados para completar transacciones en los datos bloqueados. Por lo general, recibirán un mensaje que indica la condición de bloqueo.

## <a name="to-view-database-locks"></a>Para ver bloqueos de base de datos

Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "Icono Buscar página o informe"), introduzca **Bloqueos de base de datos** y, a continuación, seleccione el vínculo relacionado.

La página **Bloqueos de base de datos** proporciona una instantánea de todos los bloqueos de la base de datos actual.

Para obtener más información sobre el bloqueo de base de datos, vea [Supervisión de bloqueos de base de datos](/dynamics365/business-central/dev-itpro/administration/monitor-database-locks) en la ayuda de Business Central Developer e IT Pro.

## <a name="see-also"></a>Consulte también

[Supervisar bloqueos de base de datos](/dynamics365/business-central/dev-itpro/administration/monitor-database-locks) 


[!INCLUDE[footer-include](includes/footer-banner.md)]