---
title: 'Procedimiento: Crear saldos iniciales del diario | Documentos de Microsoft'
description: "Business Central incluye varios trabajos por lotes que se proporcionen para ayudar en la transferencia de saldos de cuenta heredados a una empresa recién configurada. Puede transferir fácilmente estos datos con registros en los diarios."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 03/06/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: fc8e8f34220643b7cd3fd357aea3807641cee911
ms.contentlocale: es-es
ms.lasthandoff: 03/22/2018

---
# <a name="create-journal-opening-balances"></a><span data-ttu-id="4917f-104">Crear saldos iniciales del diario</span><span class="sxs-lookup"><span data-stu-id="4917f-104">Create Journal Opening Balances</span></span>
[!INCLUDE[d365fin](includes/d365fin_md.md)]<span data-ttu-id="4917f-105"> incluye varios trabajos por lotes que se proporcionen para ayudar en la transferencia de saldos de cuenta heredados a una empresa recién configurada.</span><span class="sxs-lookup"><span data-stu-id="4917f-105"> includes several batch jobs that are provided to help in the transfer of legacy account balances to a newly configured company.</span></span> <span data-ttu-id="4917f-106">Puede transferir fácilmente estos datos con el diario del cliente, el diario del proveedor, el diario de productos o el diario de contabilidad.</span><span class="sxs-lookup"><span data-stu-id="4917f-106">You can easily transfer this data with the customer journal, the vendor journal, the item journal, or the G/L journal.</span></span>

<span data-ttu-id="4917f-107">El primer paso es crear un paquete de configuración que incluya las tablas de configuración para aquellos diarios.</span><span class="sxs-lookup"><span data-stu-id="4917f-107">The first step is to create a configuration package that includes the setup tables for those journals.</span></span> <span data-ttu-id="4917f-108">En el procedimiento siguiente se supone que este paso ya se completó.</span><span class="sxs-lookup"><span data-stu-id="4917f-108">The following procedure assumes that this step is completed.</span></span> <span data-ttu-id="4917f-109">Para obtener más información, consulte [Establecer la configuración de una empresa](admin-set-up-company-configuration.md).</span><span class="sxs-lookup"><span data-stu-id="4917f-109">For more information, see [Set Up Company Configuration](admin-set-up-company-configuration.md).</span></span> <span data-ttu-id="4917f-110">Este procedimiento se describen los pasos subsiguientes, que incluyen la aplicación del paquete que proporciona un socio.</span><span class="sxs-lookup"><span data-stu-id="4917f-110">This procedure describes the subsequent steps, which include applying the package that is provided by a partner.</span></span>  

<span data-ttu-id="4917f-111">Antes de comenzar, asegúrese de estar en la página Área de trabajo del implementador de RapidStart Services ya que proporciona el contexto correcto para su trabajo de configuración.</span><span class="sxs-lookup"><span data-stu-id="4917f-111">Before you start, make sure that you are on the RapidStart Services Implementer Role Center page as it provides the correct context for your configuration work.</span></span> <span data-ttu-id="4917f-112">Para obtener más información, consulte [Cambiar configuración básica](ui-change-basic-settings.md).</span><span class="sxs-lookup"><span data-stu-id="4917f-112">For more information, see [Changing Basic Settings](ui-change-basic-settings.md).</span></span>

## <a name="to-apply-the-entries-in-a-journal-to-a-new-company"></a><span data-ttu-id="4917f-113">Procedimiento para aplicar movimientos de un diario a una nueva empresa</span><span class="sxs-lookup"><span data-stu-id="4917f-113">To apply the entries in a journal to a new company</span></span>  
1. <span data-ttu-id="4917f-114">Configure una nueva empresa y aplíquele un paquete de configuración.</span><span class="sxs-lookup"><span data-stu-id="4917f-114">Configure a new company and apply a configuration package to it.</span></span> <span data-ttu-id="4917f-115">Para obtener más información, consulte [Configurar una empresa con el asistente de RapidStart](admin-how-to-configure-a-company-with-the-rapidstart-wizard.md).</span><span class="sxs-lookup"><span data-stu-id="4917f-115">For more information, see [Configure a Company with the RapidStart Wizard](admin-how-to-configure-a-company-with-the-rapidstart-wizard.md).</span></span>  

    <span data-ttu-id="4917f-116">La nueva empresa no contiene información sobre los saldos iniciales del diario.</span><span class="sxs-lookup"><span data-stu-id="4917f-116">The new company does not contain information about journal opening balances.</span></span>  

2. <span data-ttu-id="4917f-117">Abra la hoja de trabajo de configuración e importe los datos existentes acerca de los clientes, los productos, los proveedores y la contabilidad.</span><span class="sxs-lookup"><span data-stu-id="4917f-117">Open the configuration worksheet and import existing data about customers, items, vendors, and the general ledger.</span></span> <span data-ttu-id="4917f-118">Para obtener más información, consulte [Migrar datos del cliente](admin-migrate-customer-data.md).</span><span class="sxs-lookup"><span data-stu-id="4917f-118">For more information, see [Migrate Customer Data](admin-migrate-customer-data.md).</span></span>  
3. <span data-ttu-id="4917f-119">Elija, por ejemplo, la acción **Crear líneas diario general**.</span><span class="sxs-lookup"><span data-stu-id="4917f-119">Choose, for example, the **Create G/L Journal Lines** action.</span></span>  
4. <span data-ttu-id="4917f-120">Rellene la ficha desplegable **Opciones** según corresponda y establezca los filtros según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="4917f-120">Fill in the **Options** FastTab as appropriate, and set filters as needed.</span></span> <span data-ttu-id="4917f-121">Por ejemplo, en el campo **Libro diario**, especifique un nombre.</span><span class="sxs-lookup"><span data-stu-id="4917f-121">For example, in the **Journal Template** field, enter a name.</span></span>  
5. <span data-ttu-id="4917f-122">Elija el botón **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="4917f-122">Choose the **OK** button.</span></span> <span data-ttu-id="4917f-123">Los registros ahora están en el diario, pero los importes estarán vacíos.</span><span class="sxs-lookup"><span data-stu-id="4917f-123">The records are now in the journal, but the amounts are empty.</span></span>  
6. <span data-ttu-id="4917f-124">Exporte la tabla del diario a Excel y especifique manualmente la información de cuenta de registro y saldo a partir de los datos heredados.</span><span class="sxs-lookup"><span data-stu-id="4917f-124">Export the journal table to Excel and manually enter the posting and balancing account information from the legacy data.</span></span>
7. <span data-ttu-id="4917f-125">Importe y aplique la información de la tabla a la nueva empresa.</span><span class="sxs-lookup"><span data-stu-id="4917f-125">Import and apply the table information into the new company.</span></span> <span data-ttu-id="4917f-126">Las líneas del diario estarán preparadas para el registro.</span><span class="sxs-lookup"><span data-stu-id="4917f-126">The journal lines are ready for posting.</span></span>  
8. <span data-ttu-id="4917f-127">En la hoja de trabajo de configuración, seleccione la tabla de línea de diario y elija la acción **Datos de base de datos**.</span><span class="sxs-lookup"><span data-stu-id="4917f-127">In the configuration worksheet, select the journal line table, and then choose the **Database Data** action.</span></span>  
9. <span data-ttu-id="4917f-128">Revise la información y, a continuación, seleccione la acción **Registrar**.</span><span class="sxs-lookup"><span data-stu-id="4917f-128">Review the information, and then choose the **Post** action.</span></span>  
10. <span data-ttu-id="4917f-129">Repita los pasos para importar y registrar todos los saldos abiertos.</span><span class="sxs-lookup"><span data-stu-id="4917f-129">Repeat the steps to import and post any other opening balances.</span></span>  

## <a name="see-also"></a><span data-ttu-id="4917f-130">Consulte también</span><span class="sxs-lookup"><span data-stu-id="4917f-130">See Also</span></span>  
[<span data-ttu-id="4917f-131">Aplicar la configuración a nuevas empresas</span><span class="sxs-lookup"><span data-stu-id="4917f-131">Apply Configurations to New Companies</span></span>](admin-apply-configuration-to-new-companies.md)  
[<span data-ttu-id="4917f-132">Configurar una empresa con RapidStart Services</span><span class="sxs-lookup"><span data-stu-id="4917f-132">Setting Up a Company With RapidStart Services</span></span>](admin-set-up-a-company-with-rapidstart.md)  
[<span data-ttu-id="4917f-133">Administración</span><span class="sxs-lookup"><span data-stu-id="4917f-133">Administration</span></span>](admin-setup-and-administration.md)

