---
title: 'Sugerencias y trucos: RapidStart Services | Documentos de Microsoft'
description: Cuando configura empresas con RapidStart Services, hay algunas sugerencias y trucos que puede aprovechar para facilitar la implementación.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 9e9506697eacfb4bd411266078e4245e59a11353
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/01/2020
ms.locfileid: "3922422"
---
# <a name="tips-and-tricks-rapidstart-services"></a><span data-ttu-id="5aa73-103">Sugerencias y trucos: RapidStart Services</span><span class="sxs-lookup"><span data-stu-id="5aa73-103">Tips and Tricks: RapidStart Services</span></span>

<span data-ttu-id="5aa73-104">Cuando configura empresas con RapidStart Services, hay algunas sugerencias y trucos que puede aprovechar para facilitar la implementación.</span><span class="sxs-lookup"><span data-stu-id="5aa73-104">When you configure companies using RapidStart Services, there are some tips and tricks that you can take advantage of to help your implementation go smoothly.</span></span>  

## <a name="take-advantage-of-configuration-templates"></a><span data-ttu-id="5aa73-105">Aprovechar las plantillas de configuración</span><span class="sxs-lookup"><span data-stu-id="5aa73-105">Take advantage of configuration templates</span></span>

<span data-ttu-id="5aa73-106">Las plantillas de configuración pueden ayudarle a simplificar el proceso de implementación.</span><span class="sxs-lookup"><span data-stu-id="5aa73-106">Configuration templates can help you streamline your implementation process.</span></span> <span data-ttu-id="5aa73-107">Al usarlas, puede incluir clientes similares en los segmentos y, a continuación, desarrollar un protocolo de implementación que trate a todos los clientes de un segmento de forma similar.</span><span class="sxs-lookup"><span data-stu-id="5aa73-107">By using them, you can include similar customers in segments and then develop an implementation protocol that treats all customers in a segment in a similar manner.</span></span> <span data-ttu-id="5aa73-108">De ese modo, puede aplicar un nivel de preconfiguración en cada segmento y continuar con una implementación rápida.</span><span class="sxs-lookup"><span data-stu-id="5aa73-108">In that way, you can apply a level of preconfiguration to each segment and continue with a rapid implementation.</span></span>  

## <a name="configuration-questionnaires"></a><span data-ttu-id="5aa73-109">Cuestionarios de configuración</span><span class="sxs-lookup"><span data-stu-id="5aa73-109">Configuration questionnaires</span></span>

<span data-ttu-id="5aa73-110">Para ayudar al proceso de rellenar un cuestionario de configuración, considere la posibilidad de definir las respuestas predeterminadas para indicar los procedimientos recomendados.</span><span class="sxs-lookup"><span data-stu-id="5aa73-110">To aid the process of filling out a configuration questionnaire, consider defining default answers to indicate best practices.</span></span>  

## <a name="batch-creation-of-journal-lines"></a><span data-ttu-id="5aa73-111">Creación por lotes de líneas de diario</span><span class="sxs-lookup"><span data-stu-id="5aa73-111">Batch creation of journal lines</span></span>

<span data-ttu-id="5aa73-112">Se recomienda usar las herramientas de migración de datos que se ofrecen para migrar los movimientos del diario.</span><span class="sxs-lookup"><span data-stu-id="5aa73-112">We recommend that you use the data migration tools provided to migrate journal entries.</span></span> <span data-ttu-id="5aa73-113">De lo contrario, si usa un trabajo por lotes para crear líneas de diario, eso tiene un ámbito limitado y genera solo los campos predeterminados en un diario.</span><span class="sxs-lookup"><span data-stu-id="5aa73-113">Otherwise, if you use a batch job to create journal lines, that has a limited scope and only generates pre-default fields into a journal.</span></span> <span data-ttu-id="5aa73-114">El resto del diario debe completarse manualmente.</span><span class="sxs-lookup"><span data-stu-id="5aa73-114">The rest of the journal then has to be completed manually.</span></span>  

## <a name="migrating-transactions"></a><span data-ttu-id="5aa73-115">Migración de transacciones</span><span class="sxs-lookup"><span data-stu-id="5aa73-115">Migrating transactions</span></span>

<span data-ttu-id="5aa73-116">Se recomienda migrar los saldos iniciales en el orden siguiente.</span><span class="sxs-lookup"><span data-stu-id="5aa73-116">We recommend that you migrate opening balances in the following order.</span></span> <!--Be aware that you cannot insert ledger entries directly. Instead you must use journals to post the journal lines-->

1. <span data-ttu-id="5aa73-117">Migre los saldos iniciales de contabilidad sin usar los sublibros de la cuenta de contabilidad.</span><span class="sxs-lookup"><span data-stu-id="5aa73-117">Migrate general ledger opening balances without using the general ledger account subledgers.</span></span> <span data-ttu-id="5aa73-118">Use cuentas de compensación de saldos iniciales específicas, una para cada sublibro.</span><span class="sxs-lookup"><span data-stu-id="5aa73-118">Use specific opening balance offsetting accounts, one set up for each subledger.</span></span> <span data-ttu-id="5aa73-119">Configure las cuentas de compensación para habilitar los registros directos.</span><span class="sxs-lookup"><span data-stu-id="5aa73-119">Set up the offsetting accounts to enable direct postings.</span></span>  
2. <span data-ttu-id="5aa73-120">Migre los movimientos de cliente abiertos.</span><span class="sxs-lookup"><span data-stu-id="5aa73-120">Migrate open customer ledger entries.</span></span>  <!--work on these-->
3. <span data-ttu-id="5aa73-121">Migre los movimientos de producto abiertos.</span><span class="sxs-lookup"><span data-stu-id="5aa73-121">Migrate open item ledger entries.</span></span>  
4. <span data-ttu-id="5aa73-122">Migre los movimientos de activos abiertos.</span><span class="sxs-lookup"><span data-stu-id="5aa73-122">Migrate open fixed asset entries.</span></span>  

## <a name="make-each-package-manageable"></a><span data-ttu-id="5aa73-123">Haga que cada paquete sea manejable</span><span class="sxs-lookup"><span data-stu-id="5aa73-123">Make each package manageable</span></span>

<span data-ttu-id="5aa73-124">Cuando utilice paquetes de configuración para migrar datos, separe los datos en paquetes separados para facilitar la portabilidad.</span><span class="sxs-lookup"><span data-stu-id="5aa73-124">When you use configuration packages to migrate data, separate the data into separate packages for easier portability.</span></span> <span data-ttu-id="5aa73-125">Por ejemplo, si desea migrar 20 años de entradas del libro mayor, la importación puede tardar muchas horas y días.</span><span class="sxs-lookup"><span data-stu-id="5aa73-125">For example, if you want to migrate 20 years of ledger entries, the import might take many hours and days.</span></span> <span data-ttu-id="5aa73-126">En su lugar, divida los datos para que cada paquete sea más manejable.</span><span class="sxs-lookup"><span data-stu-id="5aa73-126">Instead, split the data up so that each package becomes more manageable.</span></span> <span data-ttu-id="5aa73-127">Actualmente, no existen reglas firmes sobre lo que hace que un paquete funcione, pero si ve problemas al importar o exportar un paquete, intente hacerlo más pequeño y vea si eso ayuda.</span><span class="sxs-lookup"><span data-stu-id="5aa73-127">Currently, there are no firm rules for what makes a package performant, but if you see problems importing or exporting a package, try making it smaller and see if that helps.</span></span>  

## <a name="see-also"></a><span data-ttu-id="5aa73-128">Consulte también</span><span class="sxs-lookup"><span data-stu-id="5aa73-128">See Also</span></span>

[<span data-ttu-id="5aa73-129">Configurar una empresa con RapidStart Services</span><span class="sxs-lookup"><span data-stu-id="5aa73-129">Setting Up a Company With RapidStart Services</span></span>](admin-set-up-a-company-with-rapidstart.md)  
[<span data-ttu-id="5aa73-130">Administración</span><span class="sxs-lookup"><span data-stu-id="5aa73-130">Administration</span></span>](admin-setup-and-administration.md)  
