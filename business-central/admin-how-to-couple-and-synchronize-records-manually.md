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
ms.date: 10/01/2019
ms.author: bholtorf
ms.openlocfilehash: 0c70b1ba34af32b7cf542149c8f15cb191761358
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/01/2019
ms.locfileid: "2308121"
---
# <a name="couple-and-synchronize-records-manually"></a><span data-ttu-id="6b5f1-103">Emparejar y sincronizar registros manualmente</span><span class="sxs-lookup"><span data-stu-id="6b5f1-103">Couple and Synchronize Records Manually</span></span>
<span data-ttu-id="6b5f1-104">En este tema se describe cómo emparejar uno o más registros de [!INCLUDE[d365fin](includes/d365fin_md.md)] con registros de [!INCLUDE[crm_md](includes/crm_md.md)].</span><span class="sxs-lookup"><span data-stu-id="6b5f1-104">This topic describes how to couple one or more records in [!INCLUDE[d365fin](includes/d365fin_md.md)] with records in [!INCLUDE[crm_md](includes/crm_md.md)].</span></span> <span data-ttu-id="6b5f1-105">El emparejamiento de registros le permite ver información de [!INCLUDE[crm_md](includes/crm_md.md)] desde [!INCLUDE[d365fin](includes/d365fin_md.md)], y viceversa.</span><span class="sxs-lookup"><span data-stu-id="6b5f1-105">Coupling records lets you view [!INCLUDE[crm_md](includes/crm_md.md)] information from [!INCLUDE[d365fin](includes/d365fin_md.md)], and vice versa.</span></span> <span data-ttu-id="6b5f1-106">El emparejamiento también le permite sincronizar datos entre los registros.</span><span class="sxs-lookup"><span data-stu-id="6b5f1-106">The coupling also enables you to synchronize data between the records.</span></span> <span data-ttu-id="6b5f1-107">Puede emparejar registros existentes o crear y emparejar nuevos registros.</span><span class="sxs-lookup"><span data-stu-id="6b5f1-107">You can couple existing records, or create and couple new records.</span></span>

> [!Note]
> <span data-ttu-id="6b5f1-108">El emparejamiento y la sincronización de datos con [!INCLUDE[crm_md](includes/crm_md.md)] solo están disponibles si el administrador del sistema ha creado una conexión entre [!INCLUDE[d365fin](includes/d365fin_md.md)] y [!INCLUDE[crm_md](includes/crm_md.md)].</span><span class="sxs-lookup"><span data-stu-id="6b5f1-108">Coupling and synchronizing data with [!INCLUDE[crm_md](includes/crm_md.md)] is available only if your system administrator has created a connection between [!INCLUDE[d365fin](includes/d365fin_md.md)] and [!INCLUDE[crm_md](includes/crm_md.md)].</span></span> <span data-ttu-id="6b5f1-109">Una forma rápida de comprobarlo es abrir la ficha **Cliente** y buscar la acción **Configurar emparejamiento**.</span><span class="sxs-lookup"><span data-stu-id="6b5f1-109">A quick way to check is to open the **Customer** card and look for the **Set Up Coupling** action.</span></span> <span data-ttu-id="6b5f1-110">Si la acción está disponible, las aplicaciones se conectan.</span><span class="sxs-lookup"><span data-stu-id="6b5f1-110">If the action is available, the apps are connected.</span></span>   

> [!VIDEO https://go.microsoft.com/fwlink/?linkid=2098376]

## <a name="to-couple-a-record"></a><span data-ttu-id="6b5f1-111">Para emparejar un registro</span><span class="sxs-lookup"><span data-stu-id="6b5f1-111">To couple a record</span></span>  
1.  <span data-ttu-id="6b5f1-112">En [!INCLUDE[d365fin](includes/d365fin_md.md)], abra la tarjeta para el registro que desea emparejar.</span><span class="sxs-lookup"><span data-stu-id="6b5f1-112">In [!INCLUDE[d365fin](includes/d365fin_md.md)], open the card for the record you want to couple.</span></span> <span data-ttu-id="6b5f1-113">Por ejemplo, la tarjeta Cliente o Contacto.</span><span class="sxs-lookup"><span data-stu-id="6b5f1-113">For example, the Customer or Contact card.</span></span>  

    <span data-ttu-id="6b5f1-114">También puede abrir simplemente la página de lista y seleccionar el registro que desee emparejar.</span><span class="sxs-lookup"><span data-stu-id="6b5f1-114">You can also just open the list page and select the record that you want to couple.</span></span>  

2.  <span data-ttu-id="6b5f1-115">Seleccione la acción **Configurar emparejamiento**.</span><span class="sxs-lookup"><span data-stu-id="6b5f1-115">Choose the **Set Up Coupling** action.</span></span>  
3.  <span data-ttu-id="6b5f1-116">Rellene los campos y, a continuación, elija **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="6b5f1-116">Fill in the fields, and then choose **OK**.</span></span>  

## <a name="to-synchronize-a-single-record"></a><span data-ttu-id="6b5f1-117">Para sincronizar un solo registro</span><span class="sxs-lookup"><span data-stu-id="6b5f1-117">To synchronize a single record</span></span>  
1.  <span data-ttu-id="6b5f1-118">En [!INCLUDE[d365fin](includes/d365fin_md.md)], abra la tarjeta para el registro que desea emparejar.</span><span class="sxs-lookup"><span data-stu-id="6b5f1-118">In [!INCLUDE[d365fin](includes/d365fin_md.md)], open the card for the record you want to couple.</span></span> <span data-ttu-id="6b5f1-119">Por ejemplo, la tarjeta Cliente o Contacto.</span><span class="sxs-lookup"><span data-stu-id="6b5f1-119">For example, the Customer or Contact card.</span></span>  
2.  <span data-ttu-id="6b5f1-120">Seleccione la acción **Sincronizar ahora**.</span><span class="sxs-lookup"><span data-stu-id="6b5f1-120">Choose the **Synchronize Now** action.</span></span>  
3.  <span data-ttu-id="6b5f1-121">Si un registro se puede sincronizar desde [!INCLUDE[d365fin](includes/d365fin_md.md)] a [!INCLUDE[crm_md](includes/crm_md.md)] o desde [!INCLUDE[crm_md](includes/crm_md.md)] a [!INCLUDE[d365fin](includes/d365fin_md.md)], seleccione la opción que especifica la dirección de actualización de datos y, a continuación, seleccione **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="6b5f1-121">If a record can be synchronized either from [!INCLUDE[d365fin](includes/d365fin_md.md)] to [!INCLUDE[crm_md](includes/crm_md.md)] or from [!INCLUDE[crm_md](includes/crm_md.md)] to [!INCLUDE[d365fin](includes/d365fin_md.md)], select the option that specifies the direction of data update, and then choose **OK**.</span></span>  

## <a name="to-synchronize-multiple-records"></a><span data-ttu-id="6b5f1-122">Para sincronizar varios registros</span><span class="sxs-lookup"><span data-stu-id="6b5f1-122">To synchronize multiple records</span></span>  
1.  <span data-ttu-id="6b5f1-123">En el cliente de [!INCLUDE[d365fin](includes/d365fin_md.md)], abra la página de lista para el registro, como las páginas de lista Clientes o Contactos.</span><span class="sxs-lookup"><span data-stu-id="6b5f1-123">In [!INCLUDE[d365fin](includes/d365fin_md.md)], open the list page for the record, such as the Customers or Contacts list pages.</span></span>  
2.  <span data-ttu-id="6b5f1-124">Seleccione los registros que desea sincronizar y, después, seleccione la acción **Sincronizar ahora**.</span><span class="sxs-lookup"><span data-stu-id="6b5f1-124">Select the records that you want to synchronize, and then choose the **Synchronize Now** action.</span></span>  
3.  <span data-ttu-id="6b5f1-125">Si los registros se pueden sincronizar desde [!INCLUDE[d365fin](includes/d365fin_md.md)] a [!INCLUDE[crm_md](includes/crm_md.md)] o desde [!INCLUDE[crm_md](includes/crm_md.md)] a [!INCLUDE[d365fin](includes/d365fin_md.md)], seleccione la opción que especifica la dirección de actualización de datos y, a continuación, seleccione **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="6b5f1-125">If records can be synchronized either from [!INCLUDE[d365fin](includes/d365fin_md.md)] to [!INCLUDE[crm_md](includes/crm_md.md)] or from [!INCLUDE[crm_md](includes/crm_md.md)] to [!INCLUDE[d365fin](includes/d365fin_md.md)], select the option that specifies the direction of data update, and then choose **OK**.</span></span>  

## <a name="see-also"></a><span data-ttu-id="6b5f1-126">Consulte también</span><span class="sxs-lookup"><span data-stu-id="6b5f1-126">See Also</span></span>  
[<span data-ttu-id="6b5f1-127">Uso de Dynamics 365 Sales desde Business Central</span><span class="sxs-lookup"><span data-stu-id="6b5f1-127">Using Dynamics 365 Sales from Business Central</span></span>](marketing-integrate-dynamicscrm.md)
