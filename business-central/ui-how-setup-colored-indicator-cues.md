---
title: Personalizar las señales visuales acerca de la actividad de una pila | Documentos de Microsoft
description: Configure un indicador de color en un mosaico Pila para proporcionar una señal visual personalizada de la actividad de la pila.
services: project-madeira
documentationcenter: ''
author: SusanneWindfeldPedersen
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: personalize, customize
ms.date: 10/01/2019
ms.author: solsen
redirect_url: admin-how-set-up-colored-indicator-on-cues
ms.openlocfilehash: 69defdcec64cfaa710af7d3f5b9b35e072c7c3d6
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/01/2019
ms.locfileid: "2315185"
---
# <a name="set-up-a-colored-indicator-on-cues"></a><span data-ttu-id="50be9-103">Configurar un indicador de color en pilas</span><span class="sxs-lookup"><span data-stu-id="50be9-103">Set Up a Colored Indicator on Cues</span></span>
<span data-ttu-id="50be9-104">Puede configurar pilas para que aparezcan en el Área de trabajo de los usuarios a fin de que incluyan un indicador que cambia de color según los valores de datos de las pilas.</span><span class="sxs-lookup"><span data-stu-id="50be9-104">You can set up Cues that appear on the Role Center to include an indicator that changes color based on the data values in the Cues.</span></span>

<span data-ttu-id="50be9-105">El indicador se muestra como una barra de color a lo largo del borde superior del mosaico de la pila.</span><span class="sxs-lookup"><span data-stu-id="50be9-105">The indicator appears as a colored bar along the top border of the Cue tile.</span></span> <span data-ttu-id="50be9-106">Proporciona una guía visual del estado de la actividad de la pila, que puede indicar condiciones favorables o desfavorables para que el usuario actúe en consecuencia.</span><span class="sxs-lookup"><span data-stu-id="50be9-106">It provides a visual signal of the status of the Cue's activity, which can indicate favorable or unfavorable conditions to prompt the user to take action.</span></span> <span data-ttu-id="50be9-107">Por ejemplo, si una pila muestra las facturas de venta en curso, puede configurar que el indicador aparezca de color verde (favorable) si el número total de facturas de venta en curso es inferior a 10 y que aparezca de color rojo (desfavorable) si el total es mayor que 20.</span><span class="sxs-lookup"><span data-stu-id="50be9-107">For example, if a Cue displays ongoing sales invoices, you can set up the indicator to appear green (favorable) when total number of ongoing sales invoices is below 10, and appears red (unfavorable) when the total is greater than 20.</span></span>

<span data-ttu-id="50be9-108">En la página **Configuración de pila** se configuran indicadores para todas las pilas que están disponibles en la base de datos de la empresa.</span><span class="sxs-lookup"><span data-stu-id="50be9-108">From the **Cue Setup** page, you set up indicators for all the Cues that are available in the company database.</span></span>

<span data-ttu-id="50be9-109">Para configurar el indicador, especifique hasta dos valores de umbral que definan tres rangos de valores de datos (bajo, medio y alto) a los que se pueda aplicar otro color (o estilo).</span><span class="sxs-lookup"><span data-stu-id="50be9-109">To set up the indicator, you specify up to two threshold values that define three ranges of data values (low, middle, and high) to which you can apply a different color (or style).</span></span>

## <a name="to-set-up-colored-indicators-on-cues"></a><span data-ttu-id="50be9-110">Para configurar indicadores de color en las pilas</span><span class="sxs-lookup"><span data-stu-id="50be9-110">To set up colored indicators on Cues</span></span>
1. <span data-ttu-id="50be9-111">En **Actividades** en el Área de trabajo, elija **Configurar pilas**.</span><span class="sxs-lookup"><span data-stu-id="50be9-111">Under **Activities** on your Role Center, choose **Set Up Cues**.</span></span>  
   <span data-ttu-id="50be9-112">Aparece la página **Configuración de pila**.</span><span class="sxs-lookup"><span data-stu-id="50be9-112">The **Cue Setup** page appears.</span></span> <span data-ttu-id="50be9-113">La página muestra los indicadores que están actualmente configurados en pilas.</span><span class="sxs-lookup"><span data-stu-id="50be9-113">The page lists the indicators that are currently setup up on Cues.</span></span>
2. <span data-ttu-id="50be9-114">Para modificar un marcador, edite los campos y modifique, por ejemplo, los valores para los distintos umbrales.</span><span class="sxs-lookup"><span data-stu-id="50be9-114">To modify an indicator, edit the fields and modify, for example, the values for the different thresholds.</span></span>  

<span data-ttu-id="50be9-115">La tabla siguiente muestra los colores que corresponden a las opciones de los campos **Estilo de rango bajo**, **Estilo de rango medio** y **Estilo de rango alto**.</span><span class="sxs-lookup"><span data-stu-id="50be9-115">The following table lists the colors that correspond to the options of the **Low Range Style**, **Middle Range Style**, and **High Range Style** fields.</span></span>

| <span data-ttu-id="50be9-116">Opción</span><span class="sxs-lookup"><span data-stu-id="50be9-116">Option</span></span> | <span data-ttu-id="50be9-117">Color</span><span class="sxs-lookup"><span data-stu-id="50be9-117">Color</span></span> |
| --- | --- |
| <span data-ttu-id="50be9-118">**Ninguno**</span><span class="sxs-lookup"><span data-stu-id="50be9-118">**None**</span></span> |<span data-ttu-id="50be9-119">Sin color (mismo color que el mosaico de la pila)</span><span class="sxs-lookup"><span data-stu-id="50be9-119">No color (same color as the Cue tile)</span></span>|
| <span data-ttu-id="50be9-120">**Favorable**</span><span class="sxs-lookup"><span data-stu-id="50be9-120">**Favorable**</span></span> |<span data-ttu-id="50be9-121">Verde</span><span class="sxs-lookup"><span data-stu-id="50be9-121">Green</span></span> |
| <span data-ttu-id="50be9-122">**Desfavorable**</span><span class="sxs-lookup"><span data-stu-id="50be9-122">**Unfavorable**</span></span> |<span data-ttu-id="50be9-123">Rojo</span><span class="sxs-lookup"><span data-stu-id="50be9-123">Red</span></span> |
| <span data-ttu-id="50be9-124">**Ambiguo**</span><span class="sxs-lookup"><span data-stu-id="50be9-124">**Ambiguous**</span></span> |<span data-ttu-id="50be9-125">Amarillo</span><span class="sxs-lookup"><span data-stu-id="50be9-125">Yellow</span></span> |
| <span data-ttu-id="50be9-126">**Subordinado**</span><span class="sxs-lookup"><span data-stu-id="50be9-126">**Subordinate**</span></span> |<span data-ttu-id="50be9-127">Gris</span><span class="sxs-lookup"><span data-stu-id="50be9-127">Gray</span></span> |

## <a name="see-also"></a><span data-ttu-id="50be9-128">Consulte también</span><span class="sxs-lookup"><span data-stu-id="50be9-128">See Also</span></span>
<span data-ttu-id="50be9-129">[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="50be9-129">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
