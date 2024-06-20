---
title: Números de transacción
description: Los números de transacción permiten agrupar movimientos con el mismo número y fecha de documento para saldarlos conjuntamente.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.date: 12/11/2023
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# Números de transacción
Los números de transacción permiten agrupar movimientos con el mismo número y fecha de documento para saldarlos conjuntamente. Los números de transacción empiezan normalmente con el número 2 cada año. El número 1 se reserva para la transacción de apertura, que se crea cada año automáticamente. La única excepción es para el primer periodo contable del primer año, en cuyo caso la transacción de apertura tiene el número 1.  

Cuando se escribe un número de transacción en la primera línea de un diario, el mismo número de transacción se introduce automáticamente en el resto de líneas si los movimientos no se han saldado. De lo contrario, se introduce automáticamente el siguiente número de la secuencia en el resto de líneas.  

Tener un único número de transacción secuencial ordenado por fecha permite identificar cada transacción registrada durante un ejercicio.  

## Consulte también  
 [Registrar e imprimir todas las transacciones de un periodo](how-to-post-and-print-all-transactions-for-a-period.md)   
 [Funcionalidad local para España](spain-local-functionality.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]