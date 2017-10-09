---
title: Criterios para la transferencia de movimientos de contabilidad a movimientos de coste | Documentos de Microsoft
description: "Es importante entender los criterios para la transferencia de movimientos de contabilidad a movimientos de coste. Durante la transferencia, el proceso de **Transferir movs. contabilidad** a costes utiliza el siguiente criterio para determinar si y cómo se transfieren los movimientos de contabilidad."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 59faad50504bff05e6cdb1c78d00553e85faf47e
ms.contentlocale: es-es
ms.lasthandoff: 09/22/2017

---
# <a name="criteria-for-transferring-general-ledger-entries-to-cost-entries"></a>Criterios para la transferencia de movimientos de contabilidad a movimientos de coste
Es importante entender los criterios para la transferencia de movimientos de contabilidad a movimientos de coste. Durante la transferencia, el proceso de **Transferir movs. contabilidad a costes** utiliza el siguiente criterio para determinar si y cómo se transfieren los movimientos de contabilidad.  

Se transfieren los movimientos de contabilidad si:  

-   Los movimientos tienen valores de dimensión correspondientes a un centro o un objeto de coste.  
-   Los movimientos tienen valores de dimensión que corresponden a un centro de coste y a un objeto de coste. Para estos movimientos, el centro de coste tiene preferencia. Esto ayuda a evitar una situación en la que un tipo de coste aparece en un objeto de coste y un centro de coste y por lo tanto se cuenta dos veces en estadísticas.  
-   El número de documento de los movimientos está vacío, por lo que aparecerá con un número de documento de 0000 en los movimientos de coste.  
-   Los movimientos se transfieren a un tipo de coste que permite los movimientos agrupados y estos movimientos se transfieren como un movimiento combinado mensual o diariamente.  

No se transfieren los movimientos de contabilidad si:  

-   Los movimientos tienen valores de dimensión que no corresponden a un centro de coste ni a un objeto de coste.  
-   Los movimientos tienen un importe de cero.  
-   Los movimientos tienen una cuenta de contabilidad que se ha eliminado.  
-   Los movimientos tienen una cuenta de contabilidad que no es de tipo **Ingresos y gastos**.  
-   Los movimientos tienen una cuenta de contabilidad que no tiene un tipo de coste asignado.  
-   Los movimientos tienen una fecha de registro antes de **Fecha inicio para transferencia C/G**.  
-   Los movimientos se registraron con una fecha de cierre. Éstos son normalmente movimientos que restablecen el saldo de regularización al final del año.  

## <a name="see-also"></a>Consulte también  
[Contabilidad para costes](finance-manage-cost-accounting.md)  
 [Procedimiento: transferencia de movimientos de contabilidad a los movimientos de coste](finance-how-to-transfer-general-ledger-entries-to-cost-entries.md)   
 [Transferencia y registro de movimientos de coste](finance-transfer-and-post-cost-entries.md)   
 [Acerca de la contabilidad de costes](finance-about-cost-accounting.md)  
 [Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

