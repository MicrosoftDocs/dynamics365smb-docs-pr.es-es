---
title: 'Procedimiento: Crear saldos iniciales del diario | Documentos de Microsoft'
description: Business Central incluye varios trabajos por lotes que se proporcionen para ayudar en la transferencia de saldos de cuenta heredados a una empresa recién configurada. Puede transferir fácilmente estos datos con registros en los diarios.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 5e1bb8e34e70d1d906850c157107b9b9701c6c50
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 03/31/2021
ms.locfileid: "5779862"
---
# <a name="create-journal-opening-balances"></a><span data-ttu-id="d59e2-104">Crear saldos iniciales del diario</span><span class="sxs-lookup"><span data-stu-id="d59e2-104">Create Journal Opening Balances</span></span>

[!INCLUDE[prod_short](includes/prod_short.md)] <span data-ttu-id="d59e2-105">incluye varios trabajos por lotes que se proporcionen para ayudar en la transferencia de saldos de cuenta heredados a una empresa recién configurada.</span><span class="sxs-lookup"><span data-stu-id="d59e2-105">includes several batch jobs that are provided to help in the transfer of legacy account balances to a newly configured company.</span></span> <span data-ttu-id="d59e2-106">Puede transferir fácilmente estos datos con el diario del cliente, el diario del proveedor, el diario de productos o el diario de contabilidad.</span><span class="sxs-lookup"><span data-stu-id="d59e2-106">You can easily transfer this data with the customer journal, the vendor journal, the item journal, or the G/L journal.</span></span>

<span data-ttu-id="d59e2-107">El primer paso es crear un paquete de configuración que incluya las tablas de configuración para aquellos diarios.</span><span class="sxs-lookup"><span data-stu-id="d59e2-107">The first step is to create a configuration package that includes the setup tables for those journals.</span></span> <span data-ttu-id="d59e2-108">En el procedimiento siguiente se supone que este paso ya se completó.</span><span class="sxs-lookup"><span data-stu-id="d59e2-108">The following procedure assumes that this step is completed.</span></span> <span data-ttu-id="d59e2-109">Para obtener más información, consulte [Establecer la configuración de una empresa](admin-set-up-company-configuration.md).</span><span class="sxs-lookup"><span data-stu-id="d59e2-109">For more information, see [Set Up Company Configuration](admin-set-up-company-configuration.md).</span></span> <span data-ttu-id="d59e2-110">Este procedimiento se describen los pasos subsiguientes, que incluyen la aplicación del paquete que proporciona un socio.</span><span class="sxs-lookup"><span data-stu-id="d59e2-110">This procedure describes the subsequent steps, which include applying the package that is provided by a partner.</span></span>  

<span data-ttu-id="d59e2-111">Antes de comenzar, asegúrese de estar en la página Área de trabajo de la administración ya que proporciona el contexto correcto para su trabajo de configuración.</span><span class="sxs-lookup"><span data-stu-id="d59e2-111">Before you start, make sure that you are using the Administration Role Center page because it provides the correct context for your configuration work.</span></span> <span data-ttu-id="d59e2-112">Para obtener más información, consulte [Cambiar configuración básica](ui-change-basic-settings.md).</span><span class="sxs-lookup"><span data-stu-id="d59e2-112">For more information, see [Change Basic Settings](ui-change-basic-settings.md).</span></span>

## <a name="to-apply-the-entries-in-a-journal-to-a-new-company"></a><span data-ttu-id="d59e2-113">Procedimiento para aplicar movimientos de un diario a una nueva empresa</span><span class="sxs-lookup"><span data-stu-id="d59e2-113">To apply the entries in a journal to a new company</span></span>

1. <span data-ttu-id="d59e2-114">Configure una nueva empresa y aplíquele un paquete de configuración.</span><span class="sxs-lookup"><span data-stu-id="d59e2-114">Configure a new company and apply a configuration package to it.</span></span> <span data-ttu-id="d59e2-115">Para obtener más información, consulte [Configurar una empresa con el asistente de RapidStart](admin-how-to-configure-a-company-with-the-rapidstart-wizard.md).</span><span class="sxs-lookup"><span data-stu-id="d59e2-115">For more information, see [Configure a Company with the RapidStart Wizard](admin-how-to-configure-a-company-with-the-rapidstart-wizard.md).</span></span>  

    <span data-ttu-id="d59e2-116">La nueva empresa no contiene información sobre los saldos iniciales del diario.</span><span class="sxs-lookup"><span data-stu-id="d59e2-116">The new company does not contain information about journal opening balances.</span></span>  

2. <span data-ttu-id="d59e2-117">Abra la hoja de trabajo de configuración e importe los datos existentes acerca de los clientes, los productos, los proveedores y la contabilidad.</span><span class="sxs-lookup"><span data-stu-id="d59e2-117">Open the configuration worksheet and import existing data about customers, items, vendors, and the general ledger.</span></span> <span data-ttu-id="d59e2-118">Para obtener más información, consulte [Migrar datos del cliente](admin-migrate-customer-data.md).</span><span class="sxs-lookup"><span data-stu-id="d59e2-118">For more information, see [Migrate Customer Data](admin-migrate-customer-data.md).</span></span>  

    <span data-ttu-id="d59e2-119">Ahora tiene los datos maestros correctos.</span><span class="sxs-lookup"><span data-stu-id="d59e2-119">Now you have master data in place.</span></span> <span data-ttu-id="d59e2-120">A continuación, agregue los saldos iniciales.</span><span class="sxs-lookup"><span data-stu-id="d59e2-120">Next, you add the opening balances.</span></span> <span data-ttu-id="d59e2-121">Los siguientes pasos describen cómo crear líneas de diario para cuentas de mayor, pero lo mismo se aplica a la creación de líneas de diario para clientes, proveedores y artículos.</span><span class="sxs-lookup"><span data-stu-id="d59e2-121">The following steps describe how to create journal lines for G/L accounts, but the same apply to creating journal lines for customers, vendors, and items.</span></span>  
3. <span data-ttu-id="d59e2-122">Elija, la acción **Crear líneas diario de cuentas general**.</span><span class="sxs-lookup"><span data-stu-id="d59e2-122">Choose the **Create G/L Acct. Journal Lines** action.</span></span>  
4. <span data-ttu-id="d59e2-123">Rellene la ficha desplegable **Opciones** según corresponda y establezca los filtros según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="d59e2-123">Fill in the **Options** FastTab as appropriate, and set filters as needed.</span></span> <span data-ttu-id="d59e2-124">Por ejemplo, en el campo **Libro diario**, especifique un nombre.</span><span class="sxs-lookup"><span data-stu-id="d59e2-124">For example, in the **Journal Template** field, enter a name.</span></span>  
5. <span data-ttu-id="d59e2-125">Elija el botón **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="d59e2-125">Choose the **OK** button.</span></span> <span data-ttu-id="d59e2-126">Los registros ahora están en el diario, pero los importes estarán vacíos.</span><span class="sxs-lookup"><span data-stu-id="d59e2-126">The records are now in the journal, but the amounts are empty.</span></span>  
6. <span data-ttu-id="d59e2-127">Exporte la tabla del diario a Excel y especifique manualmente la información de cuenta de registro y saldo a partir de los datos heredados.</span><span class="sxs-lookup"><span data-stu-id="d59e2-127">Export the journal table to Excel and manually enter the posting and balancing account information from the legacy data.</span></span>
7. <span data-ttu-id="d59e2-128">Importe y aplique la información de la tabla a la nueva empresa.</span><span class="sxs-lookup"><span data-stu-id="d59e2-128">Import and apply the table information into the new company.</span></span> <span data-ttu-id="d59e2-129">Las líneas del diario estarán preparadas para el registro.</span><span class="sxs-lookup"><span data-stu-id="d59e2-129">The journal lines are ready for posting.</span></span>  
8. <span data-ttu-id="d59e2-130">En la hoja de trabajo de configuración, seleccione la tabla de línea de diario y elija la acción **Datos de base de datos**.</span><span class="sxs-lookup"><span data-stu-id="d59e2-130">In the configuration worksheet, select the journal line table, and then choose the **Database Data** action.</span></span>  
9. <span data-ttu-id="d59e2-131">Revise la información y, a continuación, seleccione la acción **Registrar**.</span><span class="sxs-lookup"><span data-stu-id="d59e2-131">Review the information, and then choose the **Post** action.</span></span>  
10. <span data-ttu-id="d59e2-132">Repita los pasos para importar y registrar todos los saldos abiertos.</span><span class="sxs-lookup"><span data-stu-id="d59e2-132">Repeat the steps to import and post any other opening balances.</span></span>  

> [!TIP]
> <span data-ttu-id="d59e2-133">Puede usar los mismos trabajos por lotes para agregar saldos iniciales siempre que registre un nuevo cliente o proveedor con el que haya hecho negocios antes pero que no se haya registrado en [!INCLUDE [prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="d59e2-133">You can use the same batch jobs to add opening balances whenever you register a new customer or vendor that you have done business with before but not registered in [!INCLUDE [prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="d59e2-134">Simplemente busque la tarea pertinente y luego elija el enlace correspondiente.</span><span class="sxs-lookup"><span data-stu-id="d59e2-134">Just search for the relevant task, and then choose the relevant link.</span></span>

## <a name="see-also"></a><span data-ttu-id="d59e2-135">Consulte también</span><span class="sxs-lookup"><span data-stu-id="d59e2-135">See Also</span></span>

[<span data-ttu-id="d59e2-136">Aplicar la configuración a nuevas empresas</span><span class="sxs-lookup"><span data-stu-id="d59e2-136">Apply Configurations to New Companies</span></span>](admin-apply-configuration-to-new-companies.md)  
[<span data-ttu-id="d59e2-137">Configurar una empresa con RapidStart Services</span><span class="sxs-lookup"><span data-stu-id="d59e2-137">Setting Up a Company With RapidStart Services</span></span>](admin-set-up-a-company-with-rapidstart.md)  
[<span data-ttu-id="d59e2-138">Administración</span><span class="sxs-lookup"><span data-stu-id="d59e2-138">Administration</span></span>](admin-setup-and-administration.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]