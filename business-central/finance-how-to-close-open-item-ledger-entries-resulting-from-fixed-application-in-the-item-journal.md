---
title: Cómo cerrar los movimientos de producto abiertos que se crean por una liquidación fija en el diario de productos | Documentos de Microsoft
description: Puede utilizar el campo **Liquidar por mov.** en la página **Diario de productos** para crear manualmente una liquidación fija entre una transacción de entrada y la transacción de salida original. Por ejemplo, para corregir la transacción de salida o procesar su devolución.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2018
ms.author: sgroespe
ms.openlocfilehash: e3f210b86168d34ec775f85b416b6d0e365cce88
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 03/08/2019
ms.locfileid: "805862"
---
# <a name="close-open-item-ledger-entries-resulting-from-fixed-application-in-the-item-journal"></a>Cerrar los movimientos de producto abiertos que se crean por una liquidación fija en el diario de productos
Puede utilizar el campo **Liquidar por mov.** en la página **Diario de productos** para crear manualmente una liquidación fija entre una transacción de entrada y la transacción de salida original. Por ejemplo, para corregir la transacción de salida o procesar su devolución. Para obtener más información, consulte Liquidar por mov.  

> [!IMPORTANT]  
>  Las liquidaciones fijas realizadas de esta forma aplican solo al coste, no a la cantidad. Por consiguiente, el movimiento de producto positivo registrado no cerrará la salida liquidado y seguirá abierto. Esto también aplica cuando se registra una liquidación fija para una positivo a un movimiento negativo que no se ha cerrado mediante un movimiento normal positivo, lo cual produce que tanto los movimientos negativos y positivos sigan abiertos.  
>   
>  Esto también significa que no puede cerrar un periodo de inventario si existe tal tipo de movimiento.  

El siguiente procedimiento muestra cómo cerrar los movimientos realizando dos registros correctores en el diario de productos.  

## <a name="to-close-open-item-ledger-entries-that-result-from-a-fixed-application-in-the-item-journal"></a>Para cerrar los movimientos de producto abiertos que se crean por una liquidación fija en el diario de productos  

1.  Utilice el campo **Liquidar por mov.** para registrar un ajuste positivo con la cantidad correspondiente. Esto cierra el movimiento negativo original con una liquidación fija.  
2.  Utilice el campo **Liquidar por mov.** para registrar un ajuste negativo. Esto cierra el movimiento positivo de corrección original con una liquidación fija.  

## <a name="see-also"></a>Consulte también  
[Eliminar y liquidar de nuevo los movimientos contables de producto](finance-how-to-remove-and-reapply-item-entries.md)  
 [Procesamiento de devoluciones de ventas y cancelaciones](sales-how-process-sales-returns-cancellations.md)   
 [Configuración de valoración de existencias](finance-set-up-inventory-valuation-and-costing.md)   
 [Gestión de costes de inventario](finance-manage-inventory-costs.md)   
 [Detalles de diseño: Métodos de coste](design-details-costing-methods.md)
