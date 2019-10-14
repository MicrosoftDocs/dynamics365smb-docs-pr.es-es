---
title: Configurar empleados almacén | Documentos de Microsoft
description: Cada usuario que desarrolla actividades en el almacén debe estar configurado como empleado de almacén asignado a una ubicación predeterminada y otras ubicaciones potenciales no predeterminadas.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 2bec5eea1ef95054a9087797b86ee1d9abdbb112
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/01/2019
ms.locfileid: "2310161"
---
# <a name="set-up-warehouse-employees"></a><span data-ttu-id="354f9-103">Configurar los empleados de almacén</span><span class="sxs-lookup"><span data-stu-id="354f9-103">Set Up Warehouse Employees</span></span>
<span data-ttu-id="354f9-104">Cada usuario que desarrolla actividades en el almacén debe estar configurado como empleado de almacén asignado a una ubicación predeterminada y otras ubicaciones potenciales no predeterminadas.</span><span class="sxs-lookup"><span data-stu-id="354f9-104">Each user who performs warehouse activities must be set up as a warehouse employee assigned to one default location and potentially more non-default locations.</span></span> <span data-ttu-id="354f9-105">Esta configuración de usuario filtra todas las actividades del almacén de la base de datos hasta la ubicación del empleado, de modo que éste sólo puede realizar las actividades de almacén de la ubicación predeterminada.</span><span class="sxs-lookup"><span data-stu-id="354f9-105">This user setup filters all warehouse activities across the database to the employee's location so that the employee can only perform the warehouse activities at the default location.</span></span> <span data-ttu-id="354f9-106">Se puede asignar un usuario a otras ubicaciones no predeterminadas para las que el empleado podrá ver las líneas de la actividad, pero no realizar las actividades.</span><span class="sxs-lookup"><span data-stu-id="354f9-106">A user can be assigned to additional non-default locations for which the employee can view activity lines but not perform the activities.</span></span>

## <a name="to-set-up-warehouse-employees"></a><span data-ttu-id="354f9-107">Para configurar los empleados de almacén</span><span class="sxs-lookup"><span data-stu-id="354f9-107">To set up warehouse employees</span></span>  
1.  <span data-ttu-id="354f9-108">Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Empleados de almacén** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="354f9-108">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Warehouse Employees**, and then choose the related link.</span></span>  
2. <span data-ttu-id="354f9-109">Seleccione la acción **Nuevo**.</span><span class="sxs-lookup"><span data-stu-id="354f9-109">Choose the **New** action.</span></span>  
3. <span data-ttu-id="354f9-110">Seleccione el campo **Id. usuario**, y seleccione al usuario que se desea agregar como empleado de almacén.</span><span class="sxs-lookup"><span data-stu-id="354f9-110">Select the **User ID** field, and then select the user to be added as a warehouse employee.</span></span> <span data-ttu-id="354f9-111">Elija el botón **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="354f9-111">Choose the **OK** button.</span></span>  
6.  <span data-ttu-id="354f9-112">En el campo **Cód. almacén**, especifique el código de la ubicación en la que trabajará el usuario.</span><span class="sxs-lookup"><span data-stu-id="354f9-112">In the **Location Code** field, enter the code of the location where the user will be working.</span></span>  
7.  <span data-ttu-id="354f9-113">Seleccione la casilla de verificación **Predeterminada** para definir la ubicación como la única en la que el empleado puede realizar actividades de almacén.</span><span class="sxs-lookup"><span data-stu-id="354f9-113">Select the **Default** check box to define the location as the only location where the employee can perform warehouse activities.</span></span>  
8.  <span data-ttu-id="354f9-114">Repita estos pasos para asignar otros empleados a ubicaciones o para asignar ubicaciones no predeterminadas a empleados de almacén existentes.</span><span class="sxs-lookup"><span data-stu-id="354f9-114">Repeat these steps to assign other employees to locations or assign non-default locations to existing warehouse employees.</span></span>  

## <a name="see-also"></a><span data-ttu-id="354f9-115">Consulte también</span><span class="sxs-lookup"><span data-stu-id="354f9-115">See Also</span></span>  
[<span data-ttu-id="354f9-116">Gestión almacén</span><span class="sxs-lookup"><span data-stu-id="354f9-116">Warehouse Management</span></span>](warehouse-manage-warehouse.md)  
[<span data-ttu-id="354f9-117">Grupos contables inventario</span><span class="sxs-lookup"><span data-stu-id="354f9-117">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="354f9-118">[Configuración de la gestión del almacén](warehouse-setup-warehouse.md)   </span><span class="sxs-lookup"><span data-stu-id="354f9-118">[Setting Up Warehouse Management](warehouse-setup-warehouse.md)   </span></span>  
<span data-ttu-id="354f9-119">[Gestión de ensamblaje](assembly-assemble-items.md)  </span><span class="sxs-lookup"><span data-stu-id="354f9-119">[Assembly Management](assembly-assemble-items.md)  </span></span>  
[<span data-ttu-id="354f9-120">Detalles de diseño: Gestión de almacén</span><span class="sxs-lookup"><span data-stu-id="354f9-120">Design Details: Warehouse Management</span></span>](design-details-warehouse-management.md)  
<span data-ttu-id="354f9-121">[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="354f9-121">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
