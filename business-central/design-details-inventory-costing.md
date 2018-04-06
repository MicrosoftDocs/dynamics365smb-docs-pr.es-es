---
title: "Detalles de diseño: Inventario y valoración | Documentos de Microsoft"
description: "En esta documentación se proporciona información técnica detallada de los conceptos y los principios que se usan en las características de valoración de inventario en Business Central."
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: design, inventory, costing
ms.date: 11/23/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 857bb571566f6c20faa5074ef0c81d4ca1f6033b
ms.contentlocale: es-es
ms.lasthandoff: 03/22/2018

---
# <a name="design-details-inventory-costing"></a><span data-ttu-id="1d74a-103">Detalles de diseño: Coste de inventario</span><span class="sxs-lookup"><span data-stu-id="1d74a-103">Design Details: Inventory Costing</span></span>
<span data-ttu-id="1d74a-104">En esta documentación se proporciona información técnica detallada de los conceptos y los principios que se usan en las características de valoración de inventario en [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="1d74a-104">This documentation provides detailed technical insight to the concepts and principles that are used within the Inventory Costing features in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>  

<span data-ttu-id="1d74a-105">La valoración de inventario, también conocida como "gestión de costes", se refiere al registro y la creación de informes sobre los costes operativos de la empresa.</span><span class="sxs-lookup"><span data-stu-id="1d74a-105">Inventory costing, also referred to as cost management, is concerned with recording and reporting business operating costs.</span></span>  

## <a name="in-this-section"></a><span data-ttu-id="1d74a-106">En esta sección</span><span class="sxs-lookup"><span data-stu-id="1d74a-106">In This Section</span></span>  
[<span data-ttu-id="1d74a-107">Detalles de diseño: Métodos de coste</span><span class="sxs-lookup"><span data-stu-id="1d74a-107">Design Details: Costing Methods</span></span>](design-details-costing-methods.md)  
[<span data-ttu-id="1d74a-108">Detalles de diseño: Liquidación de productos</span><span class="sxs-lookup"><span data-stu-id="1d74a-108">Design Details: Item Application</span></span>](design-details-item-application.md)  
[<span data-ttu-id="1d74a-109">Detalles de diseño: Problema de liquidación de producto conocido</span><span class="sxs-lookup"><span data-stu-id="1d74a-109">Design Details: Known Item Application Issue</span></span>](design-details-inventory-zero-level-open-item-ledger-entries.md)  
[<span data-ttu-id="1d74a-110">Detalles de diseño: Ajuste de coste</span><span class="sxs-lookup"><span data-stu-id="1d74a-110">Design Details: Cost Adjustment</span></span>](design-details-cost-adjustment.md)  
[<span data-ttu-id="1d74a-111">Detalles de diseño: Fecha registro en el movimiento de valor de ajuste</span><span class="sxs-lookup"><span data-stu-id="1d74a-111">Design Details: Posting Date on Adjustment Value Entry</span></span>](design-details-inventory-adjustment-value-entry-posting-date.md)  
[<span data-ttu-id="1d74a-112">Detalles de diseño: Registro de coste previsto</span><span class="sxs-lookup"><span data-stu-id="1d74a-112">Design Details: Expected Cost Posting</span></span>](design-details-expected-cost-posting.md)  
[<span data-ttu-id="1d74a-113">Detalles de diseño: Coste medio</span><span class="sxs-lookup"><span data-stu-id="1d74a-113">Design Details: Average Cost</span></span>](design-details-average-cost.md)  
[<span data-ttu-id="1d74a-114">Detalles de diseño: Desviación</span><span class="sxs-lookup"><span data-stu-id="1d74a-114">Design Details: Variance</span></span>](design-details-variance.md)  
[<span data-ttu-id="1d74a-115">Detalles de diseño: Redondeo</span><span class="sxs-lookup"><span data-stu-id="1d74a-115">Design Details: Rounding</span></span>](design-details-rounding.md)  
[<span data-ttu-id="1d74a-116">Detalles de diseño: Componentes de coste</span><span class="sxs-lookup"><span data-stu-id="1d74a-116">Design Details: Cost Components</span></span>](design-details-cost-components.md)  
[<span data-ttu-id="1d74a-117">Detalles de diseño: Periodos de inventario</span><span class="sxs-lookup"><span data-stu-id="1d74a-117">Design Details: Inventory Periods</span></span>](design-details-inventory-periods.md)  
[<span data-ttu-id="1d74a-118">Detalles de diseño: Registro de inventario</span><span class="sxs-lookup"><span data-stu-id="1d74a-118">Design Details: Inventory Posting</span></span>](design-details-inventory-posting.md)  
[<span data-ttu-id="1d74a-119">Detalles de diseño: Registro de órdenes de producción</span><span class="sxs-lookup"><span data-stu-id="1d74a-119">Design Details: Production Order Posting</span></span>](design-details-production-order-posting.md)  
[<span data-ttu-id="1d74a-120">Detalles de diseño: Registro de pedidos de ensamblado</span><span class="sxs-lookup"><span data-stu-id="1d74a-120">Design Details: Assembly Order Posting</span></span>](design-details-assembly-order-posting.md)  
[<span data-ttu-id="1d74a-121">Detalles de diseño: Conciliación con contabilidad</span><span class="sxs-lookup"><span data-stu-id="1d74a-121">Design Details: Reconciliation with the General Ledger</span></span>](design-details-reconciliation-with-the-general-ledger.md)  
[<span data-ttu-id="1d74a-122">Detalles de diseño: cuentas de contabilidad</span><span class="sxs-lookup"><span data-stu-id="1d74a-122">Design Details: Accounts in the General Ledger</span></span>](design-details-accounts-in-the-general-ledger.md)  
[<span data-ttu-id="1d74a-123">Detalles de diseño: Revalorización</span><span class="sxs-lookup"><span data-stu-id="1d74a-123">Design Details: Revaluation</span></span>](design-details-revaluation.md)

