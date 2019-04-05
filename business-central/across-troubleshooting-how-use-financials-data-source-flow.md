---
title: Solución de problemas de integración Microsoft Flow| Microsoft Docs
description: Solución de los problemas sobre cómo puede hacer que los datos de Business Central estén disponibles como un origen de datos y especificar una URL de OData de sus servicios web para generar un flujo de trabajo automatizado.
documentationcenter: ''
author: SusanneWindfeldPedersen
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: workflow, Odata, Power App, SOAP
ms.date: 10/01/2018
ms.author: solsen
ms.openlocfilehash: 0818550021bf17e5a269d3e11f8db54b9ff80dfa
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 03/08/2019
ms.locfileid: "806090"
---
# <a name="troubleshooting-integration-with-microsoft-flow---request-url-too-long"></a><span data-ttu-id="e4689-103">Solución de problemas de integración con Microsoft Flow - Solicitud de URL demasiado larga</span><span class="sxs-lookup"><span data-stu-id="e4689-103">Troubleshooting Integration with Microsoft Flow - Request URL Too Long</span></span>
<span data-ttu-id="e4689-104">Puede utilizar sus datos de [!INCLUDE[d365fin](includes/d365fin_md.md)] como parte de un flujo de trabajo de Microsoft Flow.</span><span class="sxs-lookup"><span data-stu-id="e4689-104">You can use your [!INCLUDE[d365fin](includes/d365fin_md.md)] data as part of a workflow in Microsoft Flow.</span></span>  

> [!NOTE]  
>   <span data-ttu-id="e4689-105">Debe disponer de una cuenta válida con [!INCLUDE[d365fin](includes/d365fin_md.md)] y con Flow.</span><span class="sxs-lookup"><span data-stu-id="e4689-105">You must have a valid account with [!INCLUDE[d365fin](includes/d365fin_md.md)] and with Flow.</span></span>  

<span data-ttu-id="e4689-106">Si está creando un Microsoft Flow mediante el conector [!INCLUDE[d365fin](includes/d365fin_md.md)], después de crear el flujo puede recibir un mensaje de error que indique que la URL requerida es demasiado larga, como el siguiente: **RequestUriTooLong**.</span><span class="sxs-lookup"><span data-stu-id="e4689-106">If you are creating a Microsoft Flow using the [!INCLUDE[d365fin](includes/d365fin_md.md)] connector, you may receive an error message stating that the requsted URL is too long after creating the flow, such as the following: **RequestUriTooLong**.</span></span>

## <a name="cause"></a><span data-ttu-id="e4689-107">Causa</span><span class="sxs-lookup"><span data-stu-id="e4689-107">Cause</span></span>
<span data-ttu-id="e4689-108">Para que se active un flujo, este busca cambios en sus datos.</span><span class="sxs-lookup"><span data-stu-id="e4689-108">For a flow to trigger, it looks for changes in your data.</span></span> <span data-ttu-id="e4689-109">Al determinar si sus datos han cambiado, los conectores comparan los datos en caché con los nuevos datos solicitados de la fuente.</span><span class="sxs-lookup"><span data-stu-id="e4689-109">When determining if your data has changed, the connectors compare the cached data to the new data requested from the source.</span></span>  

<span data-ttu-id="e4689-110">Si la solicitud de datos crea una URL que es demasiado larga, fallará.</span><span class="sxs-lookup"><span data-stu-id="e4689-110">If the data request creates a URL that is too long, it will fail.</span></span> <span data-ttu-id="e4689-111">Entre las causas comunes se incluyen:</span><span class="sxs-lookup"><span data-stu-id="e4689-111">Common causes may include:</span></span>
- <span data-ttu-id="e4689-112">Generalmente, cualquier tabla fuente con más de 250 filas</span><span class="sxs-lookup"><span data-stu-id="e4689-112">Generally, any source table with over 250 rows</span></span>
- <span data-ttu-id="e4689-113">Tablas fuente que contienen miles de registros</span><span class="sxs-lookup"><span data-stu-id="e4689-113">Source tables containing multiple thousands of records</span></span>

## <a name="workaround"></a><span data-ttu-id="e4689-114">Solución</span><span class="sxs-lookup"><span data-stu-id="e4689-114">Workaround</span></span>
<span data-ttu-id="e4689-115">Siga estos pasos como una solución.</span><span class="sxs-lookup"><span data-stu-id="e4689-115">Follow these steps as a workaround.</span></span>
1. <span data-ttu-id="e4689-116">Elija modificar el flujo que está fallando.</span><span class="sxs-lookup"><span data-stu-id="e4689-116">Choose to edit the flow that is failing.</span></span>
2. <span data-ttu-id="e4689-117">Amplíe **Mostrar opciones avanzadas** en el activador del flujo.</span><span class="sxs-lookup"><span data-stu-id="e4689-117">Expand the **Show advanced options** on the flow trigger.</span></span>
3. <span data-ttu-id="e4689-118">En el campo **Saltar recuento**, introduzca la cantidad de registros que se va a omitir.</span><span class="sxs-lookup"><span data-stu-id="e4689-118">In the **Skip Count** field, enter the number of records to skip.</span></span>  
<span data-ttu-id="e4689-119">Por ejemplo, si la tabla que está utilizando como fuente de datos tiene 4000 registros, introduzca 4000 como la cantidad de registros que debe omitir.</span><span class="sxs-lookup"><span data-stu-id="e4689-119">For example, if the table that you are using as a data source has 4,000 records, enter 4,000 as the number of records to skip.</span></span>
4. <span data-ttu-id="e4689-120">Actualice el flujo.</span><span class="sxs-lookup"><span data-stu-id="e4689-120">Update your flow.</span></span>

> [!NOTE]  
> <span data-ttu-id="e4689-121">El conector se encuentra actualmente en versión Beta.</span><span class="sxs-lookup"><span data-stu-id="e4689-121">The connector is currently in Beta.</span></span> <span data-ttu-id="e4689-122">Actualizaciones de cómo los cambios de datos están destinados a una versión futura.</span><span class="sxs-lookup"><span data-stu-id="e4689-122">Updates to how data changes are targeted for a future release.</span></span>


## <a name="see-also"></a><span data-ttu-id="e4689-123">Consulte también</span><span class="sxs-lookup"><span data-stu-id="e4689-123">See Also</span></span>
<span data-ttu-id="e4689-124">[Usar [!INCLUDE[d365fin](includes/d365fin_md.md)] en un flujo de trabajo automatizado](across-how-use-financials-data-source-flow.md)</span><span class="sxs-lookup"><span data-stu-id="e4689-124">[Using [!INCLUDE[d365fin](includes/d365fin_md.md)] in an Automated Workflow](across-how-use-financials-data-source-flow.md)</span></span>  
[<span data-ttu-id="e4689-125">Introducción</span><span class="sxs-lookup"><span data-stu-id="e4689-125">Getting Started</span></span>](product-get-started.md)  
[<span data-ttu-id="e4689-126">Importar datos de empresa de otros sistemas financieros</span><span class="sxs-lookup"><span data-stu-id="e4689-126">Importing Business Data from Other Finance Systems</span></span>](across-import-data-configuration-packages.md)  
<span data-ttu-id="e4689-127">[Gestionar usuarios y permisos](ui-how-users-permissions.md)  </span><span class="sxs-lookup"><span data-stu-id="e4689-127">[Managing Users and Permissions](ui-how-users-permissions.md)  </span></span>  
<span data-ttu-id="e4689-128">[Configurar [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)</span><span class="sxs-lookup"><span data-stu-id="e4689-128">[Setting Up [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)</span></span>  
[<span data-ttu-id="e4689-129">Finanzas</span><span class="sxs-lookup"><span data-stu-id="e4689-129">Finance</span></span>](finance.md)  
