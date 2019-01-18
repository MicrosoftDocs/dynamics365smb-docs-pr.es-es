---
title: "Transferencia automática y movimientos combinados | Documentos de Microsoft"
description: "En contabilidad de costes, puede transferir los movimientos de contabilidad a un tipo de coste mediante un registro combinado. Puede especificar si un tipo de coste recibe las movimientos agrupados en el campo **Combinar movimientos** en la definición del tipo de coste. La siguiente tabla describe las distintas opciones."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 11/13/2018
ms.author: sgroespe
redirect_url: finance-transfer-and-post-cost-entries
ms.translationtype: HT
ms.sourcegitcommit: 33b900f1ac9e295921e7f3d6ea72cc93939d8a1b
ms.openlocfilehash: 6f58e569bea6a42a9ee695095ce308e7a69e2a8d
ms.contentlocale: es-es
ms.lasthandoff: 11/26/2018

---
# <a name="automatic-transfer-and-combined-entries"></a>Transferencia automática y movimientos combinados
En contabilidad de costes, puede transferir los movimientos de contabilidad a un tipo de coste mediante un registro combinado. Puede especificar si un tipo de coste recibe las movimientos agrupados en el campo **Combinar movimientos** en la definición del tipo de coste. La siguiente tabla describe las distintas opciones.  

|Combinar movimientos|Descripción|  
|---------------------|-----------------|  
|Ninguno|Cada movimiento de contabilidad se transfiere individualmente al tipo de coste correspondiente.|  
|Día|Los movimientos de contabilidad que tienen la misma fecha de registro se transfieren como un solo movimiento al tipo de coste correspondiente.|  
|Mes|Todos los movimientos de contabilidad general que tienen el mismo mes de calendario se transfieren como un solo movimiento al tipo de coste correspondiente.|  

> [!IMPORTANT]  
>  Si ha seleccionado la casilla **Transf. autom. desde C/G** en la página **Configuración contabilidad costes**, [!INCLUDE[d365fin](includes/d365fin_md.md)] actualiza la contabilidad de costes después de cada registro en la contabilidad. Ya no se pueden realizar movimientos combinados.  

## <a name="see-also"></a>Consulte también  
 [Transferencia y registro de movimientos de coste](finance-transfer-and-post-cost-entries.md)   
 [Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

