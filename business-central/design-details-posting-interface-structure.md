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
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: 1e80b905d96fc2204b61b03c0970257755b9e105
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 09/09/2020
ms.locfileid: "3787351"
---
# <a name="design-details-posting-interface-structure"></a><span data-ttu-id="377d4-103">Detalles de diseño: estructura de interfaz de registro</span><span class="sxs-lookup"><span data-stu-id="377d4-103">Design Details: Posting Interface Structure</span></span>
<span data-ttu-id="377d4-104">En la estructura de interfaz de registro de [!INCLUDE[d365fin](includes/d365fin_md.md)] existen varios procedimientos globales que utilizan la misma estructura:</span><span class="sxs-lookup"><span data-stu-id="377d4-104">In the [!INCLUDE[d365fin](includes/d365fin_md.md)] posting interface structure, there are several global procedures that use the same structure:</span></span>  
  
* <span data-ttu-id="377d4-105">RunWithCheck y RunWithoutCheck llaman al código de procedimiento - interfaz de registro genérica para la línea</span><span class="sxs-lookup"><span data-stu-id="377d4-105">RunWithCheck and RunWithoutCheck call procedure Code – generic posting interface for Gen.</span></span> <span data-ttu-id="377d4-106">de diario general.</span><span class="sxs-lookup"><span data-stu-id="377d4-106">Jnl Line.</span></span>  
* <span data-ttu-id="377d4-107">CustPostApplyCustLedgEntry: registrar aplicación de cliente, llamada desde la codeunit 226 Mov. cliente-Liquidar movimientos registrados.</span><span class="sxs-lookup"><span data-stu-id="377d4-107">CustPostApplyCustLedgEntry – post customer application, called from codeunit 226 CustEntry-Apply Posted Entries.</span></span>  
* <span data-ttu-id="377d4-108">VendPostApplyVendLedgEntry: registrar liquidación de proveedor, llamada desde la codeunit 227 Mov. proveedor-Liquidar movimientos registrados.</span><span class="sxs-lookup"><span data-stu-id="377d4-108">VendPostApplyVendLedgEntry – post vendor application, called from codeunit 227 VendEntry-Apply Posted Entries.</span></span>  
* <span data-ttu-id="377d4-109">UnapplyCustLedgEntry: registrar desliquidación de liquidación de cliente, llamada desde la codeunit 226 Mov. cliente-Liquidar movimientos registrados.</span><span class="sxs-lookup"><span data-stu-id="377d4-109">UnapplyCustLedgEntry – post unapply of customer application, called from codeunit 226 CustEntry-Apply Posted Entries</span></span>  
* <span data-ttu-id="377d4-110">UnapplyVendLedgEntry: registrar desliquidación de liquidación de proveedor, llamada desde la codeunit 227 Mov. proveedor-Liquidar movimientos registrados.</span><span class="sxs-lookup"><span data-stu-id="377d4-110">UnapplyVendLedgEntry – post unapply of vendor application, called from codeunit 227 VendEntry-Apply Posted Entries</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="377d4-111">Consulte también</span><span class="sxs-lookup"><span data-stu-id="377d4-111">See Also</span></span>  
[<span data-ttu-id="377d4-112">Detalles de diseño: estructura de motor de registro</span><span class="sxs-lookup"><span data-stu-id="377d4-112">Design Details: Posting Engine Structure</span></span>](design-details-posting-engine-structure.md)