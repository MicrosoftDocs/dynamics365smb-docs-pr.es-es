---
title: Acoplamiento y sincronización | Documentos de Microsoft
description: La sincronización de una asignación de tablas de integración permite la sincronización de datos de todos los registros de una tabla de Business Central y de la tabla de Dynamics 365 Sales que están emparejadas.
services: project-madeira
documentationcenter: ''
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: crm, sales, couple, decouple, synchronize
ms.date: 10/01/2020
ms.author: bholtorf
ms.openlocfilehash: b9ea85ea320aea35d1df661be9a9d16502d33776
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5378353"
---
# <a name="coupling-and-synchronizing"></a><span data-ttu-id="6cb7b-103">Acoplamiento y sincronización</span><span class="sxs-lookup"><span data-stu-id="6cb7b-103">Coupling and Synchronizing</span></span>
<span data-ttu-id="6cb7b-104">En este tema se describe cómo emparejar uno o más registros de [!INCLUDE[prod_short](includes/prod_short.md)] con registros de Dataverse o [!INCLUDE[crm_md](includes/crm_md.md)].</span><span class="sxs-lookup"><span data-stu-id="6cb7b-104">This topic describes how to couple one or more records in [!INCLUDE[prod_short](includes/prod_short.md)] with records in Dataverse or [!INCLUDE[crm_md](includes/crm_md.md)].</span></span> <span data-ttu-id="6cb7b-105">El emparejamiento de registros le permite ver información de Dataverse desde [!INCLUDE[prod_short](includes/prod_short.md)], y viceversa.</span><span class="sxs-lookup"><span data-stu-id="6cb7b-105">Coupling records lets you view Dataverse information from [!INCLUDE[prod_short](includes/prod_short.md)], and vice versa.</span></span> <span data-ttu-id="6cb7b-106">El emparejamiento también le permite sincronizar datos entre los registros.</span><span class="sxs-lookup"><span data-stu-id="6cb7b-106">The coupling also enables you to synchronize data between the records.</span></span> <span data-ttu-id="6cb7b-107">Puede emparejar registros existentes o crear y emparejar nuevos registros.</span><span class="sxs-lookup"><span data-stu-id="6cb7b-107">You can couple existing records, or create and couple new records.</span></span>

> [!Note]
> <span data-ttu-id="6cb7b-108">El emparejamiento y la sincronización de datos solo están disponibles si el administrador del sistema ha creado una conexión entre [!INCLUDE[prod_short](includes/prod_short.md)] y Dataverse o [!INCLUDE[crm_md](includes/crm_md.md)].</span><span class="sxs-lookup"><span data-stu-id="6cb7b-108">Coupling and synchronizing data is available only if your system administrator has created a connection between [!INCLUDE[prod_short](includes/prod_short.md)] and Dataverse or [!INCLUDE[crm_md](includes/crm_md.md)].</span></span> <span data-ttu-id="6cb7b-109">Una forma rápida de comprobarlo es abrir la ficha **Cliente** y buscar la acción **Configurar emparejamiento**.</span><span class="sxs-lookup"><span data-stu-id="6cb7b-109">A quick way to check is to open the **Customer** card and look for the **Set Up Coupling** action.</span></span> <span data-ttu-id="6cb7b-110">Si la acción está disponible, las aplicaciones se conectan.</span><span class="sxs-lookup"><span data-stu-id="6cb7b-110">If the action is available, the apps are connected.</span></span>   

## <a name="video-example"></a><span data-ttu-id="6cb7b-111">Ejemplo de video</span><span class="sxs-lookup"><span data-stu-id="6cb7b-111">Video Example</span></span>

> [!VIDEO https://go.microsoft.com/fwlink/?linkid=2098376]

## <a name="to-couple-a-record"></a><span data-ttu-id="6cb7b-112">Para emparejar un registro</span><span class="sxs-lookup"><span data-stu-id="6cb7b-112">To couple a record</span></span>  
1.  <span data-ttu-id="6cb7b-113">En [!INCLUDE[prod_short](includes/prod_short.md)], abra la tarjeta para el registro que desea emparejar.</span><span class="sxs-lookup"><span data-stu-id="6cb7b-113">In [!INCLUDE[prod_short](includes/prod_short.md)], open the card for the record you want to couple.</span></span> <span data-ttu-id="6cb7b-114">Por ejemplo, la tarjeta Cliente o Contacto.</span><span class="sxs-lookup"><span data-stu-id="6cb7b-114">For example, the Customer or Contact card.</span></span>  

    <span data-ttu-id="6cb7b-115">También puede abrir simplemente la página de lista y seleccionar el registro que desee emparejar.</span><span class="sxs-lookup"><span data-stu-id="6cb7b-115">You can also just open the list page and select the record that you want to couple.</span></span>  

2.  <span data-ttu-id="6cb7b-116">Seleccione la acción **Configurar emparejamiento**.</span><span class="sxs-lookup"><span data-stu-id="6cb7b-116">Choose the **Set Up Coupling** action.</span></span>  
3.  <span data-ttu-id="6cb7b-117">Rellene los campos y, a continuación, elija **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="6cb7b-117">Fill in the fields, and then choose **OK**.</span></span>  

## <a name="to-synchronize-a-single-record"></a><span data-ttu-id="6cb7b-118">Para sincronizar un solo registro</span><span class="sxs-lookup"><span data-stu-id="6cb7b-118">To synchronize a single record</span></span>  
1.  <span data-ttu-id="6cb7b-119">En [!INCLUDE[prod_short](includes/prod_short.md)], abra la tarjeta para el registro que desea emparejar.</span><span class="sxs-lookup"><span data-stu-id="6cb7b-119">In [!INCLUDE[prod_short](includes/prod_short.md)], open the card for the record you want to couple.</span></span> <span data-ttu-id="6cb7b-120">Por ejemplo, la tarjeta Cliente o Contacto.</span><span class="sxs-lookup"><span data-stu-id="6cb7b-120">For example, the Customer or Contact card.</span></span>  
2.  <span data-ttu-id="6cb7b-121">Seleccione la acción **Sincronizar ahora**.</span><span class="sxs-lookup"><span data-stu-id="6cb7b-121">Choose the **Synchronize Now** action.</span></span>  
3.  <span data-ttu-id="6cb7b-122">Si un registro se puede sincronizar en una dirección, seleccione la opción que especifica la dirección de actualización de datos y, a continuación, seleccione **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="6cb7b-122">If a record can be synchronized in one direction, select the option that specifies the direction of data update, and then choose **OK**.</span></span>  

## <a name="to-synchronize-a-single-record-from-crm_md"></a><span data-ttu-id="6cb7b-123">Para sincronizar un solo registro en [!INCLUDE[crm_md](includes/crm_md.md)]</span><span class="sxs-lookup"><span data-stu-id="6cb7b-123">To synchronize a single record from [!INCLUDE[crm_md](includes/crm_md.md)]</span></span>  
1.  <span data-ttu-id="6cb7b-124">En [!INCLUDE[crm_md](includes/crm_md.md)], abra el formulario para el registro que desea emparejar.</span><span class="sxs-lookup"><span data-stu-id="6cb7b-124">In [!INCLUDE[crm_md](includes/crm_md.md)], open the form for the record you want to couple.</span></span> <span data-ttu-id="6cb7b-125">Por ejemplo, el formulario Tarjeta de cuenta o Tarjeta de contacto.</span><span class="sxs-lookup"><span data-stu-id="6cb7b-125">For example, the Account card or Contact card form.</span></span>  
2.  <span data-ttu-id="6cb7b-126">Elija la acción **[!INCLUDE[prod_short](includes/prod_short.md)]** en la cinta para abrir y emparejar el registro automáticamente.</span><span class="sxs-lookup"><span data-stu-id="6cb7b-126">Choose the **[!INCLUDE[prod_short](includes/prod_short.md)]** action in the ribbon to open and couple record automatically.</span></span>

> [!Note]
> <span data-ttu-id="6cb7b-127">Puede sincronizar un solo registro desde [!INCLUDE[crm_md](includes/crm_md.md)] automáticamente solo cuando **Sincronizar solo reg. emparejados** está deshabilitado y la dirección de sincronización se establece en Bidireccional o Desde la tabla de integración en la página **Asignación de tabla de integración** para el registro.</span><span class="sxs-lookup"><span data-stu-id="6cb7b-127">You can synchronize a single record from [!INCLUDE[crm_md](includes/crm_md.md)] automatically only when **Sync. Only Coupled Records** is disabled and the synchronization direction is set to Bidirectional or From Integration Table on the **Integration Table Mapping** page for the record.</span></span> <span data-ttu-id="6cb7b-128">Para más información, vea [Asignación de tablas y campos para sincronizar](admin-how-to-modify-table-mappings-for-synchronization.md#creating-new-records).</span><span class="sxs-lookup"><span data-stu-id="6cb7b-128">For more information, see [Mapping the Tables and Fields to Synchronize](admin-how-to-modify-table-mappings-for-synchronization.md#creating-new-records).</span></span>     

## <a name="to-synchronize-multiple-records"></a><span data-ttu-id="6cb7b-129">Para sincronizar varios registros</span><span class="sxs-lookup"><span data-stu-id="6cb7b-129">To synchronize multiple records</span></span>  
1.  <span data-ttu-id="6cb7b-130">En el cliente de [!INCLUDE[prod_short](includes/prod_short.md)], abra la página de lista para el registro, como las páginas de lista Clientes o Contactos.</span><span class="sxs-lookup"><span data-stu-id="6cb7b-130">In [!INCLUDE[prod_short](includes/prod_short.md)], open the list page for the record, such as the Customers or Contacts list pages.</span></span>  
2.  <span data-ttu-id="6cb7b-131">Seleccione los registros que desea sincronizar y, después, seleccione la acción **Sincronizar ahora**.</span><span class="sxs-lookup"><span data-stu-id="6cb7b-131">Select the records that you want to synchronize, and then choose the **Synchronize Now** action.</span></span>  
3.  <span data-ttu-id="6cb7b-132">Si los registros se pueden sincronizar en una dirección, seleccione la opción que especifica la dirección y, a continuación, seleccione **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="6cb7b-132">If records can be synchronized in one direction, select the option that specifies the direction, and then choose **OK**.</span></span>  

## <a name="uncoupling-records"></a><span data-ttu-id="6cb7b-133">Desemparejamiento de registros</span><span class="sxs-lookup"><span data-stu-id="6cb7b-133">Uncoupling Records</span></span>
<span data-ttu-id="6cb7b-134">Puede desacoplar uno o más registros de las páginas de lista o la página **Errores de sincronización de datos acoplados** eligiendo una o más líneas y eligiendo **Eliminar acoplamiento**.</span><span class="sxs-lookup"><span data-stu-id="6cb7b-134">You can uncouple one or more records from list pages or the **Coupled Data Synchronization Errors** page by choosing one or more lines and choosing **Delete Coupling**.</span></span> <span data-ttu-id="6cb7b-135">También puede eliminar todos los acoplamientos para una o más asignaciones de tabla en la página **Asignaciones de tablas de integración**.</span><span class="sxs-lookup"><span data-stu-id="6cb7b-135">You can also remove all couplings for one or more table mappings on the **Integration Table Mappings** page.</span></span>

## <a name="see-also"></a><span data-ttu-id="6cb7b-136">Consulte también</span><span class="sxs-lookup"><span data-stu-id="6cb7b-136">See Also</span></span>  
[<span data-ttu-id="6cb7b-137">Uso de Dynamics 365 Sales desde Business Central</span><span class="sxs-lookup"><span data-stu-id="6cb7b-137">Using Dynamics 365 Sales from Business Central</span></span>](marketing-integrate-dynamicscrm.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]