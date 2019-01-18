---
title: "Crear paquetes de configuración de empresa personalizados | Documentos de Microsoft"
description: "A medida que crece su empresa, probablemente confiará en un conjunto de tipos de empresa que utiliza con la mayor parte de los clientes. Puede simplificar el proceso de implementación al convertir estos tipos habituales en paquetes de configuración de empresa disponibles para volver a usarlas."
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
ms.sourcegitcommit: caf7cf5afe370af0c4294c794c0ff9bc8ff4c31c
ms.openlocfilehash: 868972e4d53d858834ba5985a3de3ffa1d4dcc6b
ms.contentlocale: es-es
ms.lasthandoff: 11/22/2018

---
# <a name="create-custom-company-configuration-packages"></a><span data-ttu-id="2c843-104">Crear paquetes de configuración de empresa personalizados</span><span class="sxs-lookup"><span data-stu-id="2c843-104">Create Custom Company Configuration Packages</span></span>
<span data-ttu-id="2c843-105">A medida que crece su empresa, probablemente confiará en un conjunto de tipos de empresa que utiliza con la mayor parte de los clientes.</span><span class="sxs-lookup"><span data-stu-id="2c843-105">As you grow your business, you will likely come to rely on a set of company types that you use with most of your customers.</span></span> <span data-ttu-id="2c843-106">Puede simplificar el proceso de implementación al convertir estos tipos habituales en paquetes de configuración de empresa disponibles para volver a usarlas.</span><span class="sxs-lookup"><span data-stu-id="2c843-106">You can streamline your implementation process by turning these types into company configuration packages that are available for reuse.</span></span>  

<span data-ttu-id="2c843-107">En general, debería crear un paquete de configuración por área funcional; por ejemplo, cree un paquete la funcionalidad de fabricación.</span><span class="sxs-lookup"><span data-stu-id="2c843-107">In general, create a configuration package per functional area, for example, create a package for your manufacturing functionality.</span></span> <span data-ttu-id="2c843-108">Esto le permite aplicar y configurar nuevas áreas en una empresa a medida que las necesita.</span><span class="sxs-lookup"><span data-stu-id="2c843-108">That lets you apply and set up new areas in a company as you need them</span></span>  

<span data-ttu-id="2c843-109">Otro método sería crear un paquete que incluya las tablas que definen la configuración, tal como las siguientes:</span><span class="sxs-lookup"><span data-stu-id="2c843-109">Another approach would be to create a package that includes the tables that define setup, such as the following:</span></span>  

-   <span data-ttu-id="2c843-110">Configuración activos fijos</span><span class="sxs-lookup"><span data-stu-id="2c843-110">Fixed Asset Setup</span></span>  
-   <span data-ttu-id="2c843-111">Configuración de contabilidad</span><span class="sxs-lookup"><span data-stu-id="2c843-111">General Ledger Setup</span></span>  
-   <span data-ttu-id="2c843-112">Config. existencias</span><span class="sxs-lookup"><span data-stu-id="2c843-112">Inventory Setup</span></span>  
-   <span data-ttu-id="2c843-113">Configuración de fabricación</span><span class="sxs-lookup"><span data-stu-id="2c843-113">Manufacturing Setup</span></span>  
-   <span data-ttu-id="2c843-114">Configuración de compras y pagos</span><span class="sxs-lookup"><span data-stu-id="2c843-114">Purchases and Payables Setup</span></span>  
-   <span data-ttu-id="2c843-115">Configuración de marketing</span><span class="sxs-lookup"><span data-stu-id="2c843-115">Marketing Setup</span></span>  
-   <span data-ttu-id="2c843-116">Configuración del servicio</span><span class="sxs-lookup"><span data-stu-id="2c843-116">Service Setup</span></span>  
-   <span data-ttu-id="2c843-117">Configuración de ventas y cobros</span><span class="sxs-lookup"><span data-stu-id="2c843-117">Sales and Receivables Setup</span></span>  
-   <span data-ttu-id="2c843-118">Configuración de almacén</span><span class="sxs-lookup"><span data-stu-id="2c843-118">Warehouse Setup</span></span>  
-   <span data-ttu-id="2c843-119">Configuración grupos contables</span><span class="sxs-lookup"><span data-stu-id="2c843-119">General Posting Setup</span></span>  
-   <span data-ttu-id="2c843-120">Config. grupos registro IVA</span><span class="sxs-lookup"><span data-stu-id="2c843-120">VAT Posting Setup</span></span>  
-   <span data-ttu-id="2c843-121">Config. registro inventario</span><span class="sxs-lookup"><span data-stu-id="2c843-121">Inventory Posting Setup</span></span>  

<span data-ttu-id="2c843-122">Para ver una lista completa de tablas de configuración, elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Configuración** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="2c843-122">To see a complete list of setup tables, Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Setup**, and then choose the related link.</span></span>  

## <a name="to-create-a-custom-company-configuration-package"></a><span data-ttu-id="2c843-123">Crear un paquete de configuración de empresa personalizado</span><span class="sxs-lookup"><span data-stu-id="2c843-123">To create a custom company configuration package</span></span>  
1.  <span data-ttu-id="2c843-124">Cree un nuevo [!INCLUDE[d365fin](includes/d365fin_md.md)]</span><span class="sxs-lookup"><span data-stu-id="2c843-124">Create a new [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="2c843-125">***NO ES POSIBLE Enlazar para ayudar a "Crear un suscriptor nuevo"***.</span><span class="sxs-lookup"><span data-stu-id="2c843-125">***NOT POSSIBLE Link to help for "Creating a New Tenant"***.</span></span>   
2.  <span data-ttu-id="2c843-126">Cree una nueva empresa para la plantilla de sector o solución.</span><span class="sxs-lookup"><span data-stu-id="2c843-126">Create a new company for the industry or solution template.</span></span> <span data-ttu-id="2c843-127">Para obtener más información sobre cómo crear un proyecto, consulte [Crear una nueva empresa](admin-how-to-create-a-new-company.md).</span><span class="sxs-lookup"><span data-stu-id="2c843-127">For more information, see [Create a New Company](admin-how-to-create-a-new-company.md).</span></span>  
3.  <span data-ttu-id="2c843-128">Configure la nueva empresa del modo que necesite.</span><span class="sxs-lookup"><span data-stu-id="2c843-128">Setup the new company in the way you need.</span></span> <span data-ttu-id="2c843-129">Rellene todas las tablas de configuración necesarias.</span><span class="sxs-lookup"><span data-stu-id="2c843-129">Fill in all required setup tables.</span></span>  
4.  <span data-ttu-id="2c843-130">Abra la nueva empresa.</span><span class="sxs-lookup"><span data-stu-id="2c843-130">Open the new company.</span></span>
5. <span data-ttu-id="2c843-131">Abre la página **Hoja de configuración**.</span><span class="sxs-lookup"><span data-stu-id="2c843-131">Open the **Configuration Worksheet** page.</span></span>  
6.  <span data-ttu-id="2c843-132">Agregue a la hoja de cálculo las tablas que desee transferir a otra empresa.</span><span class="sxs-lookup"><span data-stu-id="2c843-132">Add the tables that you want to transfer to another company to the worksheet.</span></span> <span data-ttu-id="2c843-133">Asigne las líneas de la hoja de trabajo al paquete.</span><span class="sxs-lookup"><span data-stu-id="2c843-133">Assign the worksheet lines to the package.</span></span>  
7.  <span data-ttu-id="2c843-134">Cree un cuestionario para las tablas de configuración que se usan con mayor frecuencia.</span><span class="sxs-lookup"><span data-stu-id="2c843-134">Create a questionnaire for the most frequently used setup tables.</span></span>  
8.  <span data-ttu-id="2c843-135">Cree plantillas de configuración para facilitar la creación de datos maestros, tales como clientes o productos.</span><span class="sxs-lookup"><span data-stu-id="2c843-135">Create configuration templates to make it easier to create master data, such as customers or items.</span></span>  
9.  <span data-ttu-id="2c843-136">Exporte el paquete como un archivo .rapidstart.</span><span class="sxs-lookup"><span data-stu-id="2c843-136">Export your package as a .rapidstart file.</span></span>  

## <a name="see-also"></a><span data-ttu-id="2c843-137">Consulte también</span><span class="sxs-lookup"><span data-stu-id="2c843-137">See Also</span></span>  
[<span data-ttu-id="2c843-138">Configurar una empresa con RapidStart Services</span><span class="sxs-lookup"><span data-stu-id="2c843-138">Setting Up a Company With RapidStart Services</span></span>](admin-set-up-a-company-with-rapidstart.md)  
[<span data-ttu-id="2c843-139">Administración</span><span class="sxs-lookup"><span data-stu-id="2c843-139">Administration</span></span>](admin-setup-and-administration.md)

