---
title: 'Detalles de diseño: estructura de interfaz de registro'
description: Este tema proporciona un resumen de los procedimientos globales y los detalles de diseño en la estructura de la interfaz de registro.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: posting, interface, design
ms.date: 06/15/2021
ms.author: edupont
ms.openlocfilehash: 80805675a3ecb1c847f0a55c2dc50008faa3b21f
ms.sourcegitcommit: e562b45fda20ff88230e086caa6587913eddae26
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 06/30/2021
ms.locfileid: "6318389"
---
# <a name="design-details-posting-interface-structure"></a>Detalles de diseño: estructura de interfaz de registro
En la estructura de interfaz de registro de [!INCLUDE[prod_short](includes/prod_short.md)] existen varios procedimientos globales que utilizan la misma estructura:  
  
* RunWithCheck y RunWithoutCheck llaman al código de procedimiento - interfaz de registro genérica para la línea de diario general.  
* CustPostApplyCustLedgEntry: registrar aplicación de cliente, llamada desde la codeunit 226 Mov. cliente-Liquidar movimientos registrados.  
* VendPostApplyVendLedgEntry: registrar liquidación de proveedor, llamada desde la codeunit 227 Mov. proveedor-Liquidar movimientos registrados.  
* UnapplyCustLedgEntry: registrar desliquidación de liquidación de cliente, llamada desde la codeunit 226 Mov. cliente-Liquidar movimientos registrados.  
* UnapplyVendLedgEntry: registrar desliquidación de liquidación de proveedor, llamada desde la codeunit 227 Mov. proveedor-Liquidar movimientos registrados.  
  
## <a name="see-also"></a>Consulte también  
[Detalles de diseño: estructura de motor de registro](design-details-posting-engine-structure.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]