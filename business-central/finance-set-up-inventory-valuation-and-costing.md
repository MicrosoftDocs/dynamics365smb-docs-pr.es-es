---
title: "Configuración de valoración de existencias | Documentos de Microsoft"
description: "En la tabla siguiente se indican una serie de tareas con vínculos a los temas que las describen."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 296f660f2ca4dfe7a605d2990e18567c5062a482
ms.contentlocale: es-es
ms.lasthandoff: 09/28/2018

---
# <a name="setting-up-inventory-valuation-and-costing"></a><span data-ttu-id="a550b-103">Configuración de valoración de existencias</span><span class="sxs-lookup"><span data-stu-id="a550b-103">Setting Up Inventory Valuation and Costing</span></span>
<span data-ttu-id="a550b-104">Para asegurarse de que los costes de inventario se registran correctamente, debe configurar varios campos y ventanas antes de comenzar a realizar transacciones de elementos.</span><span class="sxs-lookup"><span data-stu-id="a550b-104">To make sure that inventory costs are recorded correctly, you must set up various fields and windows before you begin to make item transactions.</span></span>

<span data-ttu-id="a550b-105">En la tabla siguiente se indican una serie de tareas con vínculos a los temas que las describen.</span><span class="sxs-lookup"><span data-stu-id="a550b-105">The following table describes a sequence of tasks, with links to the topics that describe them.</span></span>

|<span data-ttu-id="a550b-106">**Para**</span><span class="sxs-lookup"><span data-stu-id="a550b-106">**To**</span></span>|<span data-ttu-id="a550b-107">**Vea**</span><span class="sxs-lookup"><span data-stu-id="a550b-107">**See**</span></span>|  
|------------|-------------|  
|<span data-ttu-id="a550b-108">Configurar una valoración de existencias para cada producto que rija cómo se utilizan sus costes entrantes para evaluar el valor de inventario y el coste de las mercancías vendidas.</span><span class="sxs-lookup"><span data-stu-id="a550b-108">Set a costing method for each item to govern how its incoming cost is used to assess inventory value and the cost of goods sold.</span></span>|[<span data-ttu-id="a550b-109">Registro de productos nuevos</span><span class="sxs-lookup"><span data-stu-id="a550b-109">Register New Items</span></span>](inventory-how-register-new-items.md)|  
|<span data-ttu-id="a550b-110">Asegurar que el coste se registra automáticamente en la contabilidad cada vez que se registra una transacción de inventario.</span><span class="sxs-lookup"><span data-stu-id="a550b-110">Ensure that the cost is automatically posted to the general ledger whenever an inventory transaction is posted.</span></span>|<span data-ttu-id="a550b-111">**Variación existencias automát.** de la ventana **Config. existencias**.</span><span class="sxs-lookup"><span data-stu-id="a550b-111">**Automatic Cost Posting** field in the **Inventory Setup** window</span></span>|  
|<span data-ttu-id="a550b-112">Asegurar que los costes esperados se registran en la contabilidad para ver a partir de las cuentas provisionales una estimación de los importes vencidos y el coste de los productos comercializados antes de que se facturen realmente.</span><span class="sxs-lookup"><span data-stu-id="a550b-112">Ensure that expected costs are posted to the general ledger to see from the interim G/L accounts an estimate of the amounts due and the cost of the traded items before they are actually invoiced.</span></span>|<span data-ttu-id="a550b-113">**Regis. cte. previsto en contab.** de la ventana **Config. existencias**.</span><span class="sxs-lookup"><span data-stu-id="a550b-113">**Expected Cost Posting to G/L** field in the **Inventory Setup** window</span></span>|  
|<span data-ttu-id="a550b-114">Configurar el sistema para ajustar los cambios de coste automáticamente cada vez que se registran transacciones de inventario.</span><span class="sxs-lookup"><span data-stu-id="a550b-114">Set the system up to adjust for any cost changes automatically every time you post inventory transactions.</span></span>|[<span data-ttu-id="a550b-115">Modificar costes de productos</span><span class="sxs-lookup"><span data-stu-id="a550b-115">Adjust Item Costs</span></span>](inventory-how-adjust-item-costs.md)|  
|<span data-ttu-id="a550b-116">Definir si el coste medio debe calcularse por producto solamente o por producto para cada unidad de almacenamiento y para cada variante del producto.</span><span class="sxs-lookup"><span data-stu-id="a550b-116">Define if the average cost is to be calculated per item only or per item for each stockkeping unit and for each variant of the item.</span></span>|<span data-ttu-id="a550b-117">**Tipo cálculo cte. medio** en la ventana **Configuración de inventario**</span><span class="sxs-lookup"><span data-stu-id="a550b-117">**Average Cost Calc. Type** field in the **Inventory Setup** window</span></span>|  
|<span data-ttu-id="a550b-118">Seleccionar el periodo de tiempo que desea que utilice el programa para calcular el coste medio ponderado de los productos que utilizan la valoración de existencias media.</span><span class="sxs-lookup"><span data-stu-id="a550b-118">Select the period of time you would like the program to use for calculating the weighted average cost of items that use the average costing method.</span></span>|<span data-ttu-id="a550b-119">**Periodo cte. medio** en la ventana **Configuración de inventario**</span><span class="sxs-lookup"><span data-stu-id="a550b-119">**Average Cost Period** field in the **Inventory Setup** window</span></span>|  
|<span data-ttu-id="a550b-120">Definir periodos de inventario para controlar el valor del inventario con el tiempo no permitiendo el registro de transacciones en periodos de inventario cerrados.</span><span class="sxs-lookup"><span data-stu-id="a550b-120">Define inventory periods to control inventory value over time by disallowing transaction posting in closed inventory periods.</span></span>|[<span data-ttu-id="a550b-121">Trabajar con periodos de inventario</span><span class="sxs-lookup"><span data-stu-id="a550b-121">Work with Inventory Periods</span></span>](finance-how-to-work-with-inventory-periods.md)|  
|<span data-ttu-id="a550b-122">Asegurar que las devoluciones de ventas se liquidan con la transacción de salida original para conservar el valor del inventario.</span><span class="sxs-lookup"><span data-stu-id="a550b-122">Ensure that sales returns are applied to the original outbound transaction to preserve inventory value.</span></span>|<span data-ttu-id="a550b-123">**Coste exacto devol. obligatorio** en la ventana **Ventas y cobros**</span><span class="sxs-lookup"><span data-stu-id="a550b-123">**Exact Cost Reversing Mandatory** field in the **Sales & Receivables** window</span></span>|  
|<span data-ttu-id="a550b-124">Asegurar que las devoluciones de compras se liquidan con la transacción de entrada original para conservar el valor del inventario.</span><span class="sxs-lookup"><span data-stu-id="a550b-124">Ensure that purchase returns are applied to the original inbound transaction to preserve inventory value.</span></span>|<span data-ttu-id="a550b-125">**Coste exacto devol. obligatorio** en la ventana **Compras y pagos**</span><span class="sxs-lookup"><span data-stu-id="a550b-125">**Exact Cost Reversing Mandatory** field in the **´Purchases & Payables** window</span></span>|
|<span data-ttu-id="a550b-126">Configurar las reglas de redondeo que hay que aplicar al ajustar o sugerir precios de productos y al ajustar o sugerir costes estándar.</span><span class="sxs-lookup"><span data-stu-id="a550b-126">Set up the rounding rules to apply when adjusting or suggesting item prices and when adjusting or suggesting standard costs.</span></span>|<span data-ttu-id="a550b-127">Ventana **Método redondeo**</span><span class="sxs-lookup"><span data-stu-id="a550b-127">**Rounding Method** window</span></span>|  

## <a name="see-also"></a><span data-ttu-id="a550b-128">Consulte también</span><span class="sxs-lookup"><span data-stu-id="a550b-128">See Also</span></span>  
[<span data-ttu-id="a550b-129">Gestión de costes de inventario</span><span class="sxs-lookup"><span data-stu-id="a550b-129">Managing Inventory Costs</span></span>](finance-manage-inventory-costs.md)  
[<span data-ttu-id="a550b-130">Trabajar con Business Central</span><span class="sxs-lookup"><span data-stu-id="a550b-130">Working with Business Central</span></span>](ui-work-product.md)  
[<span data-ttu-id="a550b-131">Finanzas</span><span class="sxs-lookup"><span data-stu-id="a550b-131">Finance</span></span>](finance.md)  

