---
title: Registro e impresión de todas las transacciones de un periodo
description: Las empresas deben enviar los movimientos de transacciones de su negocio, agrupados por números de transacción, en un informe anual a la administración fiscal.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 586cc25e6c0bae88f302a5940d8b56ed1a2292db
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/01/2020
ms.locfileid: "3919735"
---
# <a name="post-and-print-all-transactions-for-a-period"></a>Registrar e imprimir todas las transacciones de un periodo
Las empresas deben enviar los movimientos de transacciones de su negocio, agrupados por números de transacción, en un informe anual a la administración fiscal. Cada transacción de contabilidad debe tener un número secuencial para el ejercicio. Al registrar las transacciones, se asignarán números de transacción a los movimientos de contabilidad.  

## <a name="to-post-all-transactions-for-a-period"></a>Para registrar todas las transacciones de un periodo  

1.  Elija el icono ![Bombilla que abre la función Dígame](../../media/ui-search/search_small.png "Dígame qué desea hacer"), introduzca **Diario general** y luego elija el enlace relacionado.  
2.  Rellene los campos tal como se describe en la tabla siguiente.  

    |Campo|Description|  
    |---------------------------------|---------------------------------------|  
    |**Nombre sección**|Seleccione el nombre de sección del diario requerido.|  
    |**Nº asiento**|Escriba el número de transacción. **Nota**: Si la transacción está saldada, el siguiente número aparecerá automáticamente y los detalles de transacción relacionados aparecerán en la siguiente fila. Si la transacción no está saldada, aparecerá el mismo número de transacción con detalles de transacción relacionados.|  

3.  Elija la acción **Registrar** y el botón **Sí** para confirmar el registro.  
4.  Elija el botón **Aceptar**.  

    Una vez registrado el diario, se asigna un número de transacción final a los movimientos del diario. Este número es secuencial, sin discontinuidades. Por lo tanto, para cada ejercicio, todos los movimientos agrupados por su número de transacción se clasifican en orden secuencial, sin discontinuidades o espacios en blanco.  

## <a name="to-print-all-transactions-for-a-period"></a>Para imprimir todas las transacciones de un periodo  

1.  Elija el icono ![Bombilla que abre la función Dígame](../../media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Registro movs. contabilidad** y luego elija el enlace relacionado.  
2.  Para definir el campo **Nº asiento periodo** para todos los movimientos de contabilidad del periodo en un orden secuencial, elija **Asignar nº asiento periodo**. .  
3.  Seleccione los filtros apropiados.  
4.  Elija el botón **Aceptar**.  

    > [!NOTE]  
    >  Todas las transacciones se ordenan por fecha de registro y se asigna un número secuencial a cada movimiento del campo **Nº asiento periodo** .  

5.  En la página **Registro movs. contabilidad**, elija la acción **Imprimir página**.  

## <a name="see-also"></a>Consulte también  
 [Números de transacción](transaction-numbers.md)
