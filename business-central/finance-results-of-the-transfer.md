---
title: Resultados de transferencia | Documentos de Microsoft
description: "En este tema se describe qué ocurre después de transferir movimientos de contabilidad a los movimientos de coste."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: general ledger, transfer, cost entries
ms.date: 10/01/2018
ms.author: sgroespe
redirect_url: finance-transfer-and-post-cost-entries
ms.translationtype: HT
ms.sourcegitcommit: 67400e424305cc705db5c1bd52a8e4de17ecc5a9
ms.openlocfilehash: 0e17ff5ad60014cba6ce866c9ddae848b1239167
ms.contentlocale: es-es
ms.lasthandoff: 11/20/2018

---
# <a name="results-of-transferring-general-ledger-entries-to-cost-entries"></a>Los resultados de la transferencia de movimientos de contabilidad a movimientos de coste
Durante la transferencia de movimientos de contabilidad a movimientos de coste, [!INCLUDE[d365fin](includes/d365fin_md.md)] crea conexiones en los movimientos de la tabla **Mov. contabilidad**, la tabla **Movimiento de coste** y la tabla **Registro de costes** para permitir realizar un seguimiento de las conexiones entre los movimientos de costes y los movimientos de contabilidad.  

## <a name="general-ledger-entries"></a>Movs. contabilidad  
Para cada movimiento de contabilidad que se transfiere a la contabilidad de costes, [!INCLUDE[d365fin](includes/d365fin_md.md)] rellena el campo de coste **N.º mov.**.  

## <a name="cost-entries"></a>Movs. coste  
Para cada movimiento de coste, [!INCLUDE[d365fin](includes/d365fin_md.md)] guarda el número de movimiento del movimiento de contabilidad correspondiente en el campo **Nº mov. contabilidad** en la tabla **Movimiento de coste**.  

Para movimientos de coste combinados, [!INCLUDE[d365fin](includes/d365fin_md.md)] guarda el número del movimiento del último movimiento de contabilidad, que es el movimiento con el número más alto de movimiento.  

El campo **Cuenta** en la tabla **Movimiento de coste** contiene el número de la cuenta de la que provino el movimiento de coste.  

Para movimientos de coste únicos, [!INCLUDE[d365fin](includes/d365fin_md.md)] transfiere el texto de registro del movimiento de contabilidad al campo de texto **Descripción**. Para movimientos combinados, el campo de texto muestra que estos movimientos se transfieren como movimientos combinados. Por ejemplo, para un movimiento combinado del mes de octubre de 2013, el texto puede ser **Movimientos combinados, octubre de 2013**.  

## <a name="cost-register"></a>Registro costes  
En la tabla **Registro de costes**, [!INCLUDE[d365fin](includes/d365fin_md.md)] crea un movimiento con la transferencia de origen de la contabilidad. El movimiento registra el primer y último número de los movimientos de contabilidad que se transfieren, además del primer y último número de movimientos de coste creados.  

## <a name="see-also"></a>Consulte también  
[Transferencia y registro de movimientos de coste](finance-transfer-and-post-cost-entries.md)   

