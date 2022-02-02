---
title: Ver bloqueos de base de datos
description: Descubra cómo puede ver información sobre cualquier bloqueo de base de datos de clientes directamente desde la interfaz del cliente en Business Central.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: 9511
ms.date: 06/14/2021
ms.author: jswymer
ms.openlocfilehash: 6fe59a57514225a0a03d45770df2329c63fda4af
ms.sourcegitcommit: 8464b37c4f1e5819aed81d9cfdc382fc3d0762fc
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 01/19/2022
ms.locfileid: "8011736"
---
# <a name="viewing-database-locks"></a>Ver bloqueos de base de datos

El bloqueo de la base de datos controla el acceso de múltiples usuarios a los mismos datos al mismo tiempo. Para proteger una transacción contra otras transacciones que modifican los mismos datos, la primera transacción bloquea los datos. El bloqueo permanece hasta que se realiza la transacción.

Los usuarios pueden ser bloqueados para completar transacciones en los datos bloqueados. Por lo general, recibirán un mensaje que indica la condición de bloqueo.

## <a name="to-view-database-locks"></a>Para ver bloqueos de base de datos

Elija el icono ![Buscar página o informe](media/ui-search/search_small.png "Icono Buscar página o informe") , escriba **Bloqueos de base de datos** y luego elija el enlace relacionado.

La página **Bloqueos de base de datos** proporciona una instantánea de todos los bloqueos de la base de datos actual.

Para obtener más información sobre el bloqueo de base de datos, vea [Supervisión de bloqueos de base de datos](/dynamics365/business-central/dev-itpro/administration/monitor-database-locks) en la ayuda de Business Central Developer e IT Pro.

## <a name="see-also"></a>Consulte también

[Supervisar bloqueos de base de datos](/dynamics365/business-central/dev-itpro/administration/monitor-database-locks) 


[!INCLUDE[footer-include](includes/footer-banner.md)]