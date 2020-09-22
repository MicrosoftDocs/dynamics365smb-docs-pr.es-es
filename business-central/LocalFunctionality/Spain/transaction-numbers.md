---
title: Números de transacción
description: Los números de transacción permiten agrupar movimientos con el mismo número y fecha de documento para saldarlos conjuntamente.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: dfa29e25c8fa85335b6eb48400a744dc8eb2117c
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 09/09/2020
ms.locfileid: "3783798"
---
# <a name="transaction-numbers"></a>Números de transacción
Los números de transacción permiten agrupar movimientos con el mismo número y fecha de documento para saldarlos conjuntamente. Los números de transacción empiezan normalmente con el número 2 cada año. El número 1 se reserva para la transacción de apertura, que se crea cada año automáticamente. La única excepción es para el primer periodo contable del primer año, en cuyo caso la transacción de apertura tiene el número 1.  

Cuando se escribe un número de transacción en la primera línea de un diario, el mismo número de transacción se introduce automáticamente en el resto de líneas si los movimientos no se han saldado. De lo contrario, se introduce automáticamente el siguiente número de la secuencia en el resto de líneas.  

Tener un único número de transacción secuencial ordenado por fecha permite identificar cada transacción registrada durante un ejercicio.  

## <a name="see-also"></a>Consulte también  
 [Registrar e imprimir todas las transacciones de un periodo](how-to-post-and-print-all-transactions-for-a-period.md)   
 [Funcionalidad local para España](spain-local-functionality.md)
