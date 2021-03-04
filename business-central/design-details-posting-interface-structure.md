---
title: 'Detalles de diseño: Estructura de interfaz de registro | Documentos de Microsoft'
description: Este tema proporciona un resumen de los procedimientos globales en la estructura de la interfaz de registro.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: posting, interface, design
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: e306b0caeb58bfe7bd04f93ac64d8b593f70f695
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "4751260"
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