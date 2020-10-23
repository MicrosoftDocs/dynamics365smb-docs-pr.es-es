---
title: Emparejar y sincronizar registros manualmente| Documentos de Microsoft
description: La sincronización de una asignación de tablas de integración permite la sincronización de datos de todos los registros de una tabla de Business Central y de la entidad de Dynamics 365 Sales que están emparejadas.
services: project-madeira
documentationcenter: ''
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: crm, sales, couple, decouple, synchronize
ms.date: 10/01/2020
ms.author: bholtorf
ms.openlocfilehash: d8140f71709208a271eff5c8de415b0e95736072
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/01/2020
ms.locfileid: "3911410"
---
# <a name="couple-and-synchronize-records-manually"></a><span data-ttu-id="f4131-103">Emparejar y sincronizar registros manualmente</span><span class="sxs-lookup"><span data-stu-id="f4131-103">Couple and Synchronize Records Manually</span></span>
<span data-ttu-id="f4131-104">En este tema se describe cómo emparejar uno o más registros de [!INCLUDE[d365fin](includes/d365fin_md.md)] con registros de Common Data Service o [!INCLUDE[crm_md](includes/crm_md.md)].</span><span class="sxs-lookup"><span data-stu-id="f4131-104">This topic describes how to couple one or more records in [!INCLUDE[d365fin](includes/d365fin_md.md)] with records in Common Data Service or [!INCLUDE[crm_md](includes/crm_md.md)].</span></span> <span data-ttu-id="f4131-105">El emparejamiento de registros le permite ver información de Common Data Service desde [!INCLUDE[d365fin](includes/d365fin_md.md)], y viceversa.</span><span class="sxs-lookup"><span data-stu-id="f4131-105">Coupling records lets you view Common Data Service information from [!INCLUDE[d365fin](includes/d365fin_md.md)], and vice versa.</span></span> <span data-ttu-id="f4131-106">El emparejamiento también le permite sincronizar datos entre los registros.</span><span class="sxs-lookup"><span data-stu-id="f4131-106">The coupling also enables you to synchronize data between the records.</span></span> <span data-ttu-id="f4131-107">Puede emparejar registros existentes o crear y emparejar nuevos registros.</span><span class="sxs-lookup"><span data-stu-id="f4131-107">You can couple existing records, or create and couple new records.</span></span>

> [!Note]
> <span data-ttu-id="f4131-108">El emparejamiento y la sincronización de datos solo están disponibles si el administrador del sistema ha creado una conexión entre [!INCLUDE[d365fin](includes/d365fin_md.md)] y Common Data Service o [!INCLUDE[crm_md](includes/crm_md.md)].</span><span class="sxs-lookup"><span data-stu-id="f4131-108">Coupling and synchronizing data is available only if your system administrator has created a connection between [!INCLUDE[d365fin](includes/d365fin_md.md)] and Common Data Service or [!INCLUDE[crm_md](includes/crm_md.md)].</span></span> <span data-ttu-id="f4131-109">Una forma rápida de comprobarlo es abrir la ficha **Cliente** y buscar la acción **Configurar emparejamiento**.</span><span class="sxs-lookup"><span data-stu-id="f4131-109">A quick way to check is to open the **Customer** card and look for the **Set Up Coupling** action.</span></span> <span data-ttu-id="f4131-110">Si la acción está disponible, las aplicaciones se conectan.</span><span class="sxs-lookup"><span data-stu-id="f4131-110">If the action is available, the apps are connected.</span></span>   

## <a name="video-example"></a><span data-ttu-id="f4131-111">Ejemplo de video</span><span class="sxs-lookup"><span data-stu-id="f4131-111">Video Example</span></span>

> [!VIDEO https://go.microsoft.com/fwlink/?linkid=2098376]

## <a name="to-couple-a-record"></a><span data-ttu-id="f4131-112">Para emparejar un registro</span><span class="sxs-lookup"><span data-stu-id="f4131-112">To couple a record</span></span>  
1.  <span data-ttu-id="f4131-113">En [!INCLUDE[d365fin](includes/d365fin_md.md)], abra la tarjeta para el registro que desea emparejar.</span><span class="sxs-lookup"><span data-stu-id="f4131-113">In [!INCLUDE[d365fin](includes/d365fin_md.md)], open the card for the record you want to couple.</span></span> <span data-ttu-id="f4131-114">Por ejemplo, la tarjeta Cliente o Contacto.</span><span class="sxs-lookup"><span data-stu-id="f4131-114">For example, the Customer or Contact card.</span></span>  

    <span data-ttu-id="f4131-115">También puede abrir simplemente la página de lista y seleccionar el registro que desee emparejar.</span><span class="sxs-lookup"><span data-stu-id="f4131-115">You can also just open the list page and select the record that you want to couple.</span></span>  

2.  <span data-ttu-id="f4131-116">Seleccione la acción **Configurar emparejamiento**.</span><span class="sxs-lookup"><span data-stu-id="f4131-116">Choose the **Set Up Coupling** action.</span></span>  
3.  <span data-ttu-id="f4131-117">Rellene los campos y, a continuación, elija **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="f4131-117">Fill in the fields, and then choose **OK**.</span></span>  

## <a name="to-synchronize-a-single-record"></a><span data-ttu-id="f4131-118">Para sincronizar un solo registro</span><span class="sxs-lookup"><span data-stu-id="f4131-118">To synchronize a single record</span></span>  
1.  <span data-ttu-id="f4131-119">En [!INCLUDE[d365fin](includes/d365fin_md.md)], abra la tarjeta para el registro que desea emparejar.</span><span class="sxs-lookup"><span data-stu-id="f4131-119">In [!INCLUDE[d365fin](includes/d365fin_md.md)], open the card for the record you want to couple.</span></span> <span data-ttu-id="f4131-120">Por ejemplo, la tarjeta Cliente o Contacto.</span><span class="sxs-lookup"><span data-stu-id="f4131-120">For example, the Customer or Contact card.</span></span>  
2.  <span data-ttu-id="f4131-121">Seleccione la acción **Sincronizar ahora**.</span><span class="sxs-lookup"><span data-stu-id="f4131-121">Choose the **Synchronize Now** action.</span></span>  
3.  <span data-ttu-id="f4131-122">Si un registro se puede sincronizar en una dirección, seleccione la opción que especifica la dirección de actualización de datos y, a continuación, seleccione **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="f4131-122">If a record can be synchronized in one direction, select the option that specifies the direction of data update, and then choose **OK**.</span></span>  

## <a name="to-synchronize-a-single-record-from-crm_md"></a><span data-ttu-id="f4131-123">Para sincronizar un solo registro en [!INCLUDE[crm_md](includes/crm_md.md)]</span><span class="sxs-lookup"><span data-stu-id="f4131-123">To synchronize a single record from [!INCLUDE[crm_md](includes/crm_md.md)]</span></span>  
1.  <span data-ttu-id="f4131-124">En [!INCLUDE[crm_md](includes/crm_md.md)], abra el formulario para el registro que desea emparejar.</span><span class="sxs-lookup"><span data-stu-id="f4131-124">In [!INCLUDE[crm_md](includes/crm_md.md)], open the form for the record you want to couple.</span></span> <span data-ttu-id="f4131-125">Por ejemplo, el formulario Tarjeta de cuenta o Tarjeta de contacto.</span><span class="sxs-lookup"><span data-stu-id="f4131-125">For example, the Account card or Contact card form.</span></span>  
2.  <span data-ttu-id="f4131-126">Elija la acción **[!INCLUDE[d365fin](includes/d365fin_md.md)]** en la cinta para abrir y emparejar el registro automáticamente.</span><span class="sxs-lookup"><span data-stu-id="f4131-126">Choose the **[!INCLUDE[d365fin](includes/d365fin_md.md)]** action in the ribbon to open and couple record automatically.</span></span>

> [!Note]
> <span data-ttu-id="f4131-127">Puede sincronizar un solo registro desde [!INCLUDE[crm_md](includes/crm_md.md)] automáticamente solo cuando **Sincronizar solo reg. emparejados** está deshabilitado y la dirección de sincronización se establece en Bidireccional o Desde la tabla de integración en la página **Asignación de tabla de integración** para el registro.</span><span class="sxs-lookup"><span data-stu-id="f4131-127">You can synchronize a single record from [!INCLUDE[crm_md](includes/crm_md.md)] automatically only when **Sync. Only Coupled Records** is disabled and the synchronization direction is set to Bidirectional or From Integration Table on the **Integration Table Mapping** page for the record.</span></span> <span data-ttu-id="f4131-128">Para más información, vea [Asignación de tablas y campos para sincronizar](admin-how-to-modify-table-mappings-for-synchronization.md#creating-new-records).</span><span class="sxs-lookup"><span data-stu-id="f4131-128">For more information, see [Mapping the Tables and Fields to Synchronize](admin-how-to-modify-table-mappings-for-synchronization.md#creating-new-records).</span></span>     

## <a name="to-synchronize-multiple-records"></a><span data-ttu-id="f4131-129">Para sincronizar varios registros</span><span class="sxs-lookup"><span data-stu-id="f4131-129">To synchronize multiple records</span></span>  
1.  <span data-ttu-id="f4131-130">En el cliente de [!INCLUDE[d365fin](includes/d365fin_md.md)], abra la página de lista para el registro, como las páginas de lista Clientes o Contactos.</span><span class="sxs-lookup"><span data-stu-id="f4131-130">In [!INCLUDE[d365fin](includes/d365fin_md.md)], open the list page for the record, such as the Customers or Contacts list pages.</span></span>  
2.  <span data-ttu-id="f4131-131">Seleccione los registros que desea sincronizar y, después, seleccione la acción **Sincronizar ahora**.</span><span class="sxs-lookup"><span data-stu-id="f4131-131">Select the records that you want to synchronize, and then choose the **Synchronize Now** action.</span></span>  
3.  <span data-ttu-id="f4131-132">Si los registros se pueden sincronizar en una dirección, seleccione la opción que especifica la dirección y, a continuación, seleccione **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="f4131-132">If records can be synchronized in one direction, select the option that specifies the direction, and then choose **OK**.</span></span>  

## <a name="see-also"></a><span data-ttu-id="f4131-133">Consulte también</span><span class="sxs-lookup"><span data-stu-id="f4131-133">See Also</span></span>  
[<span data-ttu-id="f4131-134">Uso de Dynamics 365 Sales desde Business Central</span><span class="sxs-lookup"><span data-stu-id="f4131-134">Using Dynamics 365 Sales from Business Central</span></span>](marketing-integrate-dynamicscrm.md)
