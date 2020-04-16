---
title: 'Detalles de diseño: Inventario y valoración | Documentos de Microsoft'
description: En esta documentación se proporciona información técnica detallada de los conceptos y los principios que se usan en las características de valoración de inventario en Business Central.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: design, inventory, costing
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: 8dc7f7ac1e9f1d6b9919ecf7401d5cadf69a56c0
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/01/2020
ms.locfileid: "3185305"
---
# <a name="design-details-inventory-costing"></a><span data-ttu-id="c6d80-103">Detalles de diseño: Coste de inventario</span><span class="sxs-lookup"><span data-stu-id="c6d80-103">Design Details: Inventory Costing</span></span>
<span data-ttu-id="c6d80-104">En esta documentación se proporciona información técnica detallada de los conceptos y los principios que se usan en las características de valoración de inventario en [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="c6d80-104">This documentation provides detailed technical insight to the concepts and principles that are used within the Inventory Costing features in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>  

<span data-ttu-id="c6d80-105">La valoración de inventario, también conocida como "gestión de costes", se refiere al registro y la creación de informes sobre los costes operativos de la empresa.</span><span class="sxs-lookup"><span data-stu-id="c6d80-105">Inventory costing, also referred to as cost management, is concerned with recording and reporting business operating costs.</span></span>  

## <a name="in-this-section"></a><span data-ttu-id="c6d80-106">En esta sección</span><span class="sxs-lookup"><span data-stu-id="c6d80-106">In This Section</span></span>  
[<span data-ttu-id="c6d80-107">Detalles de diseño: Métodos de coste</span><span class="sxs-lookup"><span data-stu-id="c6d80-107">Design Details: Costing Methods</span></span>](design-details-costing-methods.md)  
[<span data-ttu-id="c6d80-108">Detalles de diseño: Liquidación de productos</span><span class="sxs-lookup"><span data-stu-id="c6d80-108">Design Details: Item Application</span></span>](design-details-item-application.md)  
[<span data-ttu-id="c6d80-109">Detalles de diseño: Problema de liquidación de producto conocido</span><span class="sxs-lookup"><span data-stu-id="c6d80-109">Design Details: Known Item Application Issue</span></span>](design-details-inventory-zero-level-open-item-ledger-entries.md)  
[<span data-ttu-id="c6d80-110">Detalles de diseño: Ajuste de coste</span><span class="sxs-lookup"><span data-stu-id="c6d80-110">Design Details: Cost Adjustment</span></span>](design-details-cost-adjustment.md)  
[<span data-ttu-id="c6d80-111">Detalles de diseño: Fecha registro en el movimiento de valor de ajuste</span><span class="sxs-lookup"><span data-stu-id="c6d80-111">Design Details: Posting Date on Adjustment Value Entry</span></span>](design-details-inventory-adjustment-value-entry-posting-date.md)  
[<span data-ttu-id="c6d80-112">Detalles de diseño: Registro de coste previsto</span><span class="sxs-lookup"><span data-stu-id="c6d80-112">Design Details: Expected Cost Posting</span></span>](design-details-expected-cost-posting.md)  
[<span data-ttu-id="c6d80-113">Detalles de diseño: Coste medio</span><span class="sxs-lookup"><span data-stu-id="c6d80-113">Design Details: Average Cost</span></span>](design-details-average-cost.md)  
[<span data-ttu-id="c6d80-114">Detalles de diseño: Desviación</span><span class="sxs-lookup"><span data-stu-id="c6d80-114">Design Details: Variance</span></span>](design-details-variance.md)  
[<span data-ttu-id="c6d80-115">Detalles de diseño: Redondeo</span><span class="sxs-lookup"><span data-stu-id="c6d80-115">Design Details: Rounding</span></span>](design-details-rounding.md)  
[<span data-ttu-id="c6d80-116">Detalles de diseño: Componentes de coste</span><span class="sxs-lookup"><span data-stu-id="c6d80-116">Design Details: Cost Components</span></span>](design-details-cost-components.md)  
[<span data-ttu-id="c6d80-117">Detalles de diseño: Periodos de inventario</span><span class="sxs-lookup"><span data-stu-id="c6d80-117">Design Details: Inventory Periods</span></span>](design-details-inventory-periods.md)  
[<span data-ttu-id="c6d80-118">Detalles de diseño: Registro de inventario</span><span class="sxs-lookup"><span data-stu-id="c6d80-118">Design Details: Inventory Posting</span></span>](design-details-inventory-posting.md)  
[<span data-ttu-id="c6d80-119">Detalles de diseño: Registro de órdenes de producción</span><span class="sxs-lookup"><span data-stu-id="c6d80-119">Design Details: Production Order Posting</span></span>](design-details-production-order-posting.md)  
[<span data-ttu-id="c6d80-120">Detalles de diseño: Registro de pedidos de ensamblado</span><span class="sxs-lookup"><span data-stu-id="c6d80-120">Design Details: Assembly Order Posting</span></span>](design-details-assembly-order-posting.md)  
[<span data-ttu-id="c6d80-121">Detalles de diseño: Conciliación con contabilidad</span><span class="sxs-lookup"><span data-stu-id="c6d80-121">Design Details: Reconciliation with the General Ledger</span></span>](design-details-reconciliation-with-the-general-ledger.md)  
[<span data-ttu-id="c6d80-122">Detalles de diseño: cuentas de contabilidad</span><span class="sxs-lookup"><span data-stu-id="c6d80-122">Design Details: Accounts in the General Ledger</span></span>](design-details-accounts-in-the-general-ledger.md)  
[<span data-ttu-id="c6d80-123">Detalles de diseño: Valoración de inventario</span><span class="sxs-lookup"><span data-stu-id="c6d80-123">Design Details: Inventory Valuation</span></span>](design-details-inventory-valuation.md)  
[<span data-ttu-id="c6d80-124">Detalles de diseño: Revalorización</span><span class="sxs-lookup"><span data-stu-id="c6d80-124">Design Details: Revaluation</span></span>](design-details-revaluation.md)
