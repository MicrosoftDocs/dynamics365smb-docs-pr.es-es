---
title: 'Sugerencias y trucos: RapidStart Services | Documentos de Microsoft'
description: "Cuando configura empresas con RapidStart Services, hay algunas sugerencias y trucos que puede aprovechar para facilitar la implementación."
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
ms.openlocfilehash: 875ab6f5875a842fb4c2ab906f39ae95607f6ba8
ms.contentlocale: es-es
ms.lasthandoff: 09/28/2018

---
# <a name="tips-and-tricks-rapidstart-services"></a><span data-ttu-id="4d1dc-103">Sugerencias y trucos: servicios de RapidStart</span><span class="sxs-lookup"><span data-stu-id="4d1dc-103">Tips and Tricks: RapidStart Services</span></span>
<span data-ttu-id="4d1dc-104">Cuando configura empresas con RapidStart Services, hay algunas sugerencias y trucos que puede aprovechar para facilitar la implementación.</span><span class="sxs-lookup"><span data-stu-id="4d1dc-104">When you configure companies using RapidStart Services, there are some tips and tricks that you can take advantage of to help your implementation go smoothly.</span></span>  

## <a name="take-advantage-of-configuration-templates"></a><span data-ttu-id="4d1dc-105">Aprovechar las plantillas de configuración</span><span class="sxs-lookup"><span data-stu-id="4d1dc-105">Take advantage of configuration templates</span></span>  
<span data-ttu-id="4d1dc-106">Las plantillas de configuración pueden ayudarle a simplificar el proceso de implementación.</span><span class="sxs-lookup"><span data-stu-id="4d1dc-106">Configuration templates can help you streamline your implementation process.</span></span> <span data-ttu-id="4d1dc-107">Al usarlas, puede incluir clientes similares en los segmentos y, a continuación, desarrollar un protocolo de implementación que trate a todos los clientes de un segmento de forma similar.</span><span class="sxs-lookup"><span data-stu-id="4d1dc-107">By using them, you can include similar customers in segments and then develop an implementation protocol that treats all customers in a segment in a similar manner.</span></span> <span data-ttu-id="4d1dc-108">De ese modo, puede aplicar un nivel de preconfiguración en cada segmento y continuar con una implementación rápida.</span><span class="sxs-lookup"><span data-stu-id="4d1dc-108">In that way, you can apply a level of preconfiguration to each segment and continue with a rapid implementation.</span></span>  

## <a name="configuration-questionnaires"></a><span data-ttu-id="4d1dc-109">Cuestionarios de configuración</span><span class="sxs-lookup"><span data-stu-id="4d1dc-109">Configuration questionnaires</span></span>  
<span data-ttu-id="4d1dc-110">Para ayudar al proceso de rellenar un cuestionario de configuración, considere la posibilidad de definir las respuestas predeterminadas para indicar los procedimientos recomendados.</span><span class="sxs-lookup"><span data-stu-id="4d1dc-110">To aid the process of filling out a configuration questionnaire, consider defining default answers to indicate best practices.</span></span>  

## <a name="batch-creation-of-journal-lines"></a><span data-ttu-id="4d1dc-111">Creación por lotes de líneas de diario</span><span class="sxs-lookup"><span data-stu-id="4d1dc-111">Batch creation of journal lines</span></span>  
<span data-ttu-id="4d1dc-112">Se recomienda usar las herramientas de migración de datos que se ofrecen para migrar los movimientos del diario.</span><span class="sxs-lookup"><span data-stu-id="4d1dc-112">We recommend that you use the data migration tools provided to migrate journal entries.</span></span> <span data-ttu-id="4d1dc-113">De lo contrario, si usa un trabajo por lotes para crear líneas de diario, eso tiene un ámbito limitado y genera solo los campos predeterminados en un diario.</span><span class="sxs-lookup"><span data-stu-id="4d1dc-113">Otherwise, if you use a batch job to create journal lines, that has a limited scope and only generates pre-default fields into a journal.</span></span> <span data-ttu-id="4d1dc-114">El resto del diario debe completarse manualmente.</span><span class="sxs-lookup"><span data-stu-id="4d1dc-114">The rest of the journal then has to be completed manually.</span></span>  

## <a name="migrating-transactions"></a><span data-ttu-id="4d1dc-115">Migración de transacciones</span><span class="sxs-lookup"><span data-stu-id="4d1dc-115">Migrating transactions</span></span>  
<span data-ttu-id="4d1dc-116">Se recomienda migrar los saldos iniciales en el orden siguiente.</span><span class="sxs-lookup"><span data-stu-id="4d1dc-116">We recommend that you migrate opening balances in the following order.</span></span>  

1.  <span data-ttu-id="4d1dc-117">Migre los saldos iniciales de contabilidad sin usar los sublibros de la cuenta de contabilidad.</span><span class="sxs-lookup"><span data-stu-id="4d1dc-117">Migrate general ledger opening balances without using the general ledger account subledgers.</span></span> <span data-ttu-id="4d1dc-118">Use cuentas de compensación de saldos iniciales específicas, una para cada sublibro.</span><span class="sxs-lookup"><span data-stu-id="4d1dc-118">Use specific opening balance offsetting accounts, one set up for each subledger.</span></span> <span data-ttu-id="4d1dc-119">Configure las cuentas de compensación para habilitar los registros directos.</span><span class="sxs-lookup"><span data-stu-id="4d1dc-119">Set up the offsetting accounts to enable direct postings.</span></span>  
2.  <span data-ttu-id="4d1dc-120">Migre los movimientos de cliente abiertos.</span><span class="sxs-lookup"><span data-stu-id="4d1dc-120">Migrate open customer ledger entries.</span></span>  
3.  <span data-ttu-id="4d1dc-121">Migre los movimientos de producto abiertos.</span><span class="sxs-lookup"><span data-stu-id="4d1dc-121">Migrate open item ledger entries.</span></span>  
4.  <span data-ttu-id="4d1dc-122">Migre los movimientos de activos abiertos.</span><span class="sxs-lookup"><span data-stu-id="4d1dc-122">Migrate open fixed asset entries.</span></span>  

## <a name="see-also"></a><span data-ttu-id="4d1dc-123">Consulte también</span><span class="sxs-lookup"><span data-stu-id="4d1dc-123">See Also</span></span>  
[<span data-ttu-id="4d1dc-124">Configurar una empresa con RapidStart Services</span><span class="sxs-lookup"><span data-stu-id="4d1dc-124">Setting Up a Company With RapidStart Services</span></span>](admin-set-up-a-company-with-rapidstart.md)  
[<span data-ttu-id="4d1dc-125">Administración</span><span class="sxs-lookup"><span data-stu-id="4d1dc-125">Administration</span></span>](admin-setup-and-administration.md)

