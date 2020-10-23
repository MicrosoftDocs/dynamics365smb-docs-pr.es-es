---
title: Ver bloqueos de base de datos
description: Descubra cómo puede ver información sobre cualquier bloqueo de base de datos directamente desde la interfaz del cliente en Business Central.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 10/01/2020
ms.author: jswymer
ms.openlocfilehash: 6880ffa9a2ab42c1af7c22f9cace64697c9f905b
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/01/2020
ms.locfileid: "3922322"
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
