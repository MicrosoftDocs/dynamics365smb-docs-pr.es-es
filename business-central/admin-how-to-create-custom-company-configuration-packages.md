---
title: Crear paquetes de configuración de empresa personalizados | Documentos de Microsoft
description: A medida que crece su empresa, probablemente confiará en un conjunto de tipos de empresa que utiliza con la mayor parte de los clientes. Puede simplificar el proceso de implementación al convertir estos tipos habituales en paquetes de configuración de empresa disponibles para volver a usarlas.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: 511281b5f4d8c7437324ed123a5a5a62bd4cc51d
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 09/09/2020
ms.locfileid: "3783661"
---
# <a name="create-custom-company-configuration-packages"></a><span data-ttu-id="cd49b-104">Crear paquetes de configuración de empresa personalizados</span><span class="sxs-lookup"><span data-stu-id="cd49b-104">Create Custom Company Configuration Packages</span></span>
<span data-ttu-id="cd49b-105">A medida que crece su empresa, probablemente confiará en un conjunto de tipos de empresa que utiliza con la mayor parte de los clientes.</span><span class="sxs-lookup"><span data-stu-id="cd49b-105">As you grow your business, you will likely come to rely on a set of company types that you use with most of your customers.</span></span> <span data-ttu-id="cd49b-106">Puede simplificar el proceso de implementación al convertir estos tipos habituales en paquetes de configuración de empresa disponibles para volver a usarlas.</span><span class="sxs-lookup"><span data-stu-id="cd49b-106">You can streamline your implementation process by turning these types into company configuration packages that are available for reuse.</span></span>  

<span data-ttu-id="cd49b-107">En general, debería crear un paquete de configuración por área funcional; por ejemplo, cree un paquete la funcionalidad de fabricación.</span><span class="sxs-lookup"><span data-stu-id="cd49b-107">In general, create a configuration package per functional area, for example, create a package for your manufacturing functionality.</span></span> <span data-ttu-id="cd49b-108">Esto le permite aplicar y configurar nuevas áreas en una empresa a medida que las necesita.</span><span class="sxs-lookup"><span data-stu-id="cd49b-108">That lets you apply and set up new areas in a company as you need them</span></span>  

<span data-ttu-id="cd49b-109">Otro método sería crear un paquete que incluya las tablas que definen la configuración, tal como las siguientes:</span><span class="sxs-lookup"><span data-stu-id="cd49b-109">Another approach would be to create a package that includes the tables that define setup, such as the following:</span></span>  

-   <span data-ttu-id="cd49b-110">Configuración activos fijos</span><span class="sxs-lookup"><span data-stu-id="cd49b-110">Fixed Asset Setup</span></span>  
-   <span data-ttu-id="cd49b-111">Configuración de contabilidad</span><span class="sxs-lookup"><span data-stu-id="cd49b-111">General Ledger Setup</span></span>  
-   <span data-ttu-id="cd49b-112">Config. existencias</span><span class="sxs-lookup"><span data-stu-id="cd49b-112">Inventory Setup</span></span>  
-   <span data-ttu-id="cd49b-113">Configuración de fabricación</span><span class="sxs-lookup"><span data-stu-id="cd49b-113">Manufacturing Setup</span></span>  
-   <span data-ttu-id="cd49b-114">Configuración de compras y pagos</span><span class="sxs-lookup"><span data-stu-id="cd49b-114">Purchases and Payables Setup</span></span>  
-   <span data-ttu-id="cd49b-115">Configuración de marketing</span><span class="sxs-lookup"><span data-stu-id="cd49b-115">Marketing Setup</span></span>  
-   <span data-ttu-id="cd49b-116">Configuración del servicio</span><span class="sxs-lookup"><span data-stu-id="cd49b-116">Service Setup</span></span>  
-   <span data-ttu-id="cd49b-117">Configuración de ventas y cobros</span><span class="sxs-lookup"><span data-stu-id="cd49b-117">Sales and Receivables Setup</span></span>  
-   <span data-ttu-id="cd49b-118">Configuración de almacén</span><span class="sxs-lookup"><span data-stu-id="cd49b-118">Warehouse Setup</span></span>  
-   <span data-ttu-id="cd49b-119">Configuración grupos contables</span><span class="sxs-lookup"><span data-stu-id="cd49b-119">General Posting Setup</span></span>  
-   <span data-ttu-id="cd49b-120">Config. grupos registro IVA</span><span class="sxs-lookup"><span data-stu-id="cd49b-120">VAT Posting Setup</span></span>  
-   <span data-ttu-id="cd49b-121">Config. registro inventario</span><span class="sxs-lookup"><span data-stu-id="cd49b-121">Inventory Posting Setup</span></span>  

<span data-ttu-id="cd49b-122">Para ver una lista completa de tablas de configuración, elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Configuración manual** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="cd49b-122">To see a complete list of setup tables, Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Manual Setup**, and then choose the related link.</span></span>  

> [!IMPORTANT]
> <span data-ttu-id="cd49b-123">Tenga cuidado si elige tablas o campos que tienen el mismo nombre temporal pero que se diferencian por caracteres especiales, como %, &, <, >, ( y ).</span><span class="sxs-lookup"><span data-stu-id="cd49b-123">Use caution if you choose tables or fields that have the same temporal name but are differentiated by special characters, such as %, &, <, >, (, and ).</span></span> <span data-ttu-id="cd49b-124">Por ejemplo, la tabla "XYZ" puede contener los campos "Campo 1" y "Campo 1%".</span><span class="sxs-lookup"><span data-stu-id="cd49b-124">For example, table "XYZ" might contain the "Field 1" and "Field 1%" fields.</span></span>
>
> <span data-ttu-id="cd49b-125">El procesador XML acepta solo algunos caracteres especiales y eliminará los que no.</span><span class="sxs-lookup"><span data-stu-id="cd49b-125">The XML processor accepts only some special characters, and will remove those it does not.</span></span> <span data-ttu-id="cd49b-126">Si al eliminar un carácter especial, como el signo % en el "Campo 1%", se obtienen dos o más tablas o campos con el mismo nombre, se producirá un error al exportar o importar un paquete de configuración.</span><span class="sxs-lookup"><span data-stu-id="cd49b-126">If removing a special character, such as the % sign in "Field 1%," results in two or more tables or fields with the same name an error will occur when you export or import a configuration package.</span></span>

## <a name="to-create-a-custom-company-configuration-package"></a><span data-ttu-id="cd49b-127">Crear un paquete de configuración de empresa personalizado</span><span class="sxs-lookup"><span data-stu-id="cd49b-127">To create a custom company configuration package</span></span>  
1.  <span data-ttu-id="cd49b-128">Cree una nueva empresa.</span><span class="sxs-lookup"><span data-stu-id="cd49b-128">Create a new company.</span></span> <span data-ttu-id="cd49b-129">Para obtener más información, consulte [Crear nuevas empresas en Business Central](about-new-company.md).</span><span class="sxs-lookup"><span data-stu-id="cd49b-129">For more information, see [Creating New Companies in Business Central](about-new-company.md).</span></span>  
3.  <span data-ttu-id="cd49b-130">Configure la nueva empresa del modo que necesite.</span><span class="sxs-lookup"><span data-stu-id="cd49b-130">Set up the new company in the way you need.</span></span> <span data-ttu-id="cd49b-131">Rellene todas las tablas de configuración necesarias.</span><span class="sxs-lookup"><span data-stu-id="cd49b-131">Fill in all required setup tables.</span></span>  
4.  <span data-ttu-id="cd49b-132">Abra la nueva empresa.</span><span class="sxs-lookup"><span data-stu-id="cd49b-132">Open the new company.</span></span>
5. <span data-ttu-id="cd49b-133">Abre la página **Hoja de configuración**.</span><span class="sxs-lookup"><span data-stu-id="cd49b-133">Open the **Configuration Worksheet** page.</span></span>  
6.  <span data-ttu-id="cd49b-134">Agregue a la hoja de cálculo las tablas que desee transferir a otra empresa.</span><span class="sxs-lookup"><span data-stu-id="cd49b-134">Add the tables that you want to transfer to another company to the worksheet.</span></span> <span data-ttu-id="cd49b-135">Asigne las líneas de la hoja de trabajo al paquete.</span><span class="sxs-lookup"><span data-stu-id="cd49b-135">Assign the worksheet lines to the package.</span></span>  
7.  <span data-ttu-id="cd49b-136">Cree un cuestionario para las tablas de configuración que se usan con mayor frecuencia.</span><span class="sxs-lookup"><span data-stu-id="cd49b-136">Create a questionnaire for the most frequently used setup tables.</span></span>  
8.  <span data-ttu-id="cd49b-137">Cree plantillas de configuración para facilitar la creación de datos maestros, tales como clientes o productos.</span><span class="sxs-lookup"><span data-stu-id="cd49b-137">Create configuration templates to make it easier to create master data, such as customers or items.</span></span>  
9.  <span data-ttu-id="cd49b-138">Exporte el paquete como un archivo .rapidstart.</span><span class="sxs-lookup"><span data-stu-id="cd49b-138">Export your package as a .rapidstart file.</span></span>  

## <a name="see-also"></a><span data-ttu-id="cd49b-139">Consulte también</span><span class="sxs-lookup"><span data-stu-id="cd49b-139">See Also</span></span>  
[<span data-ttu-id="cd49b-140">Configurar una empresa con RapidStart Services</span><span class="sxs-lookup"><span data-stu-id="cd49b-140">Setting Up a Company With RapidStart Services</span></span>](admin-set-up-a-company-with-rapidstart.md)  
[<span data-ttu-id="cd49b-141">Administración</span><span class="sxs-lookup"><span data-stu-id="cd49b-141">Administration</span></span>](admin-setup-and-administration.md)
