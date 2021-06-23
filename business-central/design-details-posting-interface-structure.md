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
ms.date: 06/08/2021
ms.author: edupont
ms.openlocfilehash: 529a0e42d814f0754e62fcc4b93b793d44b8daa7
ms.sourcegitcommit: 0953171d39e1232a7c126142d68cac858234a20e
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 06/09/2021
ms.locfileid: "6215833"
---
# <a name="design-details-posting-interface-structure"></a><span data-ttu-id="4df83-103">Detalles de diseño: estructura de interfaz de registro</span><span class="sxs-lookup"><span data-stu-id="4df83-103">Design Details: Posting Interface Structure</span></span>
<span data-ttu-id="4df83-104">En la estructura de interfaz de registro de [!INCLUDE[prod_short](includes/prod_short.md)] existen varios procedimientos globales que utilizan la misma estructura:</span><span class="sxs-lookup"><span data-stu-id="4df83-104">In the [!INCLUDE[prod_short](includes/prod_short.md)] posting interface structure, there are several global procedures that use the same structure:</span></span>  
  
* <span data-ttu-id="4df83-105">RunWithCheck y RunWithoutCheck llaman al código de procedimiento - interfaz de registro genérica para la línea</span><span class="sxs-lookup"><span data-stu-id="4df83-105">RunWithCheck and RunWithoutCheck call procedure Code – generic posting interface for Gen.</span></span> <span data-ttu-id="4df83-106">de diario general.</span><span class="sxs-lookup"><span data-stu-id="4df83-106">Jnl Line.</span></span>  
* <span data-ttu-id="4df83-107">CustPostApplyCustLedgEntry: registrar aplicación de cliente, llamada desde la codeunit 226 Mov. cliente-Liquidar movimientos registrados.</span><span class="sxs-lookup"><span data-stu-id="4df83-107">CustPostApplyCustLedgEntry – post customer application, called from codeunit 226 CustEntry-Apply Posted Entries.</span></span>  
* <span data-ttu-id="4df83-108">VendPostApplyVendLedgEntry: registrar liquidación de proveedor, llamada desde la codeunit 227 Mov. proveedor-Liquidar movimientos registrados.</span><span class="sxs-lookup"><span data-stu-id="4df83-108">VendPostApplyVendLedgEntry – post vendor application, called from codeunit 227 VendEntry-Apply Posted Entries.</span></span>  
* <span data-ttu-id="4df83-109">UnapplyCustLedgEntry: registrar desliquidación de liquidación de cliente, llamada desde la codeunit 226 Mov. cliente-Liquidar movimientos registrados.</span><span class="sxs-lookup"><span data-stu-id="4df83-109">UnapplyCustLedgEntry – post unapply of customer application, called from codeunit 226 CustEntry-Apply Posted Entries</span></span>  
* <span data-ttu-id="4df83-110">UnapplyVendLedgEntry: registrar desliquidación de liquidación de proveedor, llamada desde la codeunit 227 Mov. proveedor-Liquidar movimientos registrados.</span><span class="sxs-lookup"><span data-stu-id="4df83-110">UnapplyVendLedgEntry – post unapply of vendor application, called from codeunit 227 VendEntry-Apply Posted Entries</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="4df83-111">Consulte también</span><span class="sxs-lookup"><span data-stu-id="4df83-111">See Also</span></span>  
[<span data-ttu-id="4df83-112">Detalles de diseño: estructura de motor de registro</span><span class="sxs-lookup"><span data-stu-id="4df83-112">Design Details: Posting Engine Structure</span></span>](design-details-posting-engine-structure.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]