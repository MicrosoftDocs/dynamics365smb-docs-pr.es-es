---
title: 'Detalles de diseño: Estructura de interfaz de registro | Documentos de Microsoft'
description: Este tema proporciona un resumen de los procedimientos globales en la estructura de la interfaz de registro.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: posting, interface, design
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: b852d6e5d7f96cfba64de219ca414de60cea3a31
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 03/31/2021
ms.locfileid: "5777605"
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