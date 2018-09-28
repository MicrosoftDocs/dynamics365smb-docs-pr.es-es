---
title: "Detalles de diseño: Estructura de interfaz de registro | Documentos de Microsoft"
description: Este tema proporciona un resumen de los procedimientos globales en la estructura de la interfaz de registro.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: posting, interface, design
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 236cbcc45ccca23905dcb79a491236c80b2bdebf
ms.contentlocale: es-es
ms.lasthandoff: 09/28/2018

---
# <a name="design-details-posting-interface-structure"></a><span data-ttu-id="18b54-103">Detalles de diseño: estructura de interfaz de registro</span><span class="sxs-lookup"><span data-stu-id="18b54-103">Design Details: Posting Interface Structure</span></span>
<span data-ttu-id="18b54-104">En la estructura de interfaz de registro de [!INCLUDE[d365fin](includes/d365fin_md.md)] existen varios procedimientos globales que utilizan la misma estructura:</span><span class="sxs-lookup"><span data-stu-id="18b54-104">In the [!INCLUDE[d365fin](includes/d365fin_md.md)] posting interface structure, there are several global procedures that use the same structure:</span></span>  
  
* <span data-ttu-id="18b54-105">RunWithCheck y RunWithoutCheck llaman al código de procedimiento - interfaz de registro genérica para la línea de diario general.</span><span class="sxs-lookup"><span data-stu-id="18b54-105">RunWithCheck and RunWithoutCheck call procedure Code – generic posting interface for Gen. Jnl Line.</span></span>  
* <span data-ttu-id="18b54-106">CustPostApplyCustLedgEntry: registrar aplicación de cliente, llamada desde la unidad de código 226 Mov. cliente-Liquidar movimientos registrados.</span><span class="sxs-lookup"><span data-stu-id="18b54-106">CustPostApplyCustLedgEntry – post customer application, called from codeunit 226 CustEntry-Apply Posted Entries.</span></span>  
* <span data-ttu-id="18b54-107">VendPostApplyVendLedgEntry: registrar liquidación de proveedor, llamada desde la unidad de código 227 Mov. proveedor-Liquidar movimientos registrados.</span><span class="sxs-lookup"><span data-stu-id="18b54-107">VendPostApplyVendLedgEntry – post vendor application, called from codeunit 227 VendEntry-Apply Posted Entries.</span></span>  
* <span data-ttu-id="18b54-108">UnapplyCustLedgEntry: registrar desliquidación de liquidación de cliente, llamada desde la unidad de código 226 Mov. cliente-Liquidar movimientos registrados.</span><span class="sxs-lookup"><span data-stu-id="18b54-108">UnapplyCustLedgEntry – post unapply of customer application, called from codeunit 226 CustEntry-Apply Posted Entries</span></span>  
* <span data-ttu-id="18b54-109">UnapplyVendLedgEntry: registrar desliquidación de liquidación de proveedor, llamada desde la unidad de código 227 Mov. proveedor-Liquidar movimientos registrados.</span><span class="sxs-lookup"><span data-stu-id="18b54-109">UnapplyVendLedgEntry – post unapply of vendor application, called from codeunit 227 VendEntry-Apply Posted Entries</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="18b54-110">Consulte también</span><span class="sxs-lookup"><span data-stu-id="18b54-110">See Also</span></span>  
[<span data-ttu-id="18b54-111">Detalles de diseño: estructura de motor de registro</span><span class="sxs-lookup"><span data-stu-id="18b54-111">Design Details: Posting Engine Structure</span></span>](design-details-posting-engine-structure.md)
