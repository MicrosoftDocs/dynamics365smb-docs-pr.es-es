---
title: Administrar la intención de acceso a la base de datos en Business Central | Microsoft Docs
description: Cambie la intención de acceso a la base de datos para informes, páginas API y consultas.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: jswymer
ms.openlocfilehash: 98105cb3e3634169b31a850f20a65a3854b006b4
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/01/2020
ms.locfileid: "3911560"
---
# <a name="managing-database-access-intent"></a><span data-ttu-id="81fc1-103">Gestionar la intención de acceso a la base de datos</span><span class="sxs-lookup"><span data-stu-id="81fc1-103">Managing Database Access Intent</span></span> 

<span data-ttu-id="81fc1-104">Como superusuario o administrador, puede cambiar la intención de acceso a la base de datos en informes, páginas de tipo API y consultas para mejorar el rendimiento del servicio.</span><span class="sxs-lookup"><span data-stu-id="81fc1-104">As a super user or administrator, you can change the database access intent on reports, pages of the type API, and queries to improve performance of the service.</span></span>

## <a name="overview"></a><span data-ttu-id="81fc1-105">Panorama</span><span class="sxs-lookup"><span data-stu-id="81fc1-105">Overview</span></span>

[!INCLUDE[d365fin](includes/d365fin_md.md)] <span data-ttu-id="81fc1-106">se puede configurar para usar réplicas de solo lectura de la base de datos primaria (lectura-escritura).</span><span class="sxs-lookup"><span data-stu-id="81fc1-106">can be set up to use read-only replicas of the primary (read-write) database.</span></span> <span data-ttu-id="81fc1-107">El uso de la réplica de la base de datos reduce la carga en la base de datos primaria.</span><span class="sxs-lookup"><span data-stu-id="81fc1-107">Using the database replica reduces the load on the primary database.</span></span> <span data-ttu-id="81fc1-108">En algunos casos, también mejorará el rendimiento al visualizar datos en el cliente.</span><span class="sxs-lookup"><span data-stu-id="81fc1-108">In some cases, it will also improve the performance when viewing data in the client.</span></span> <span data-ttu-id="81fc1-109">Las réplicas son beneficiosas para los objetos, como informes, consultas y páginas API, que se usan para ver solo datos, no para modificar datos.</span><span class="sxs-lookup"><span data-stu-id="81fc1-109">Replicas are beneficial for objects, like reports, queries, and API pages, that are used for viewing data only, not modifying data.</span></span>

<span data-ttu-id="81fc1-110">Cuando se ejecutan los objetos, la intención de acceso a la base de datos determina si se usa una réplica de solo lectura, si hay una disponible, o la base de datos primaria.</span><span class="sxs-lookup"><span data-stu-id="81fc1-110">When objects run, the database access intent determines whether to use a read-only replica, if one is available, or the primary database.</span></span> <span data-ttu-id="81fc1-111">Los informes, las páginas API y las consultas se desarrollan con una intención de acceso a la base de datos predefinida (consulte [Propiedad DatabaseAccessIntent](/dynamics365/business-central/dev-itpro/developer/properties/devenv-dataaccessintent-property)).</span><span class="sxs-lookup"><span data-stu-id="81fc1-111">Reports, API pages, and queries are developed with a predefined database access intent (see [DatabaseAccessIntent property](/dynamics365/business-central/dev-itpro/developer/properties/devenv-dataaccessintent-property)).</span></span>

<span data-ttu-id="81fc1-112">La página **Lista de intenciones de acceso a la base de datos** permite anular la intención de acceso a la base de datos predefinida para los objetos cuando se ejecutan.</span><span class="sxs-lookup"><span data-stu-id="81fc1-112">The **Database Access Intent List** page lets you override the predefined database access intent for objects when they're run.</span></span>

<span data-ttu-id="81fc1-113">En términos de base de datos, esta característica se conoce comúnmente como *escalado de lectura*. Para obtener más información sobre el escalado de lectura y la intención de acceso a datos en [!INCLUDE[prodshort](includes/prodshort.md)], vea [Utilizar el escalado de lectura para un mejor rendimiento](/dynamics365/business-central/dev-itpro/administration/database-read-scale-out-overview) en la ayuda para desarrolladores y administración de [!INCLUDE[prodshort](includes/prodshort.md)].</span><span class="sxs-lookup"><span data-stu-id="81fc1-113">In database terms, this feature is commonly known as *read scale-out*. For more information about read-scale out and data access intent in [!INCLUDE[prodshort](includes/prodshort.md)], see [Utilizing Read Scale-Out for Better Performance](/dynamics365/business-central/dev-itpro/administration/database-read-scale-out-overview) in the [!INCLUDE[prodshort](includes/prodshort.md)] Developer and Administration help.</span></span>

## <a name="to-change-the-database-access-intent"></a><span data-ttu-id="81fc1-114">Para cambiar la intención de acceso a la base de datos</span><span class="sxs-lookup"><span data-stu-id="81fc1-114">To change the database access intent</span></span>

1. <span data-ttu-id="81fc1-115">Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Lista de intenciones de acceso a la base de datos** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="81fc1-115">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Database Access Intent List**, and then choose the related link.</span></span>

    <span data-ttu-id="81fc1-116">La página enumera todos los informes, páginas y consultas.</span><span class="sxs-lookup"><span data-stu-id="81fc1-116">The page lists all reports, pages, and queries.</span></span> <span data-ttu-id="81fc1-117">La columna **Intento de acceso** incluye uno de los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="81fc1-117">The **Access Intent** column includes one of the following values:</span></span>

    |<span data-ttu-id="81fc1-118">**Configuración**</span><span class="sxs-lookup"><span data-stu-id="81fc1-118">**Setting**</span></span>|<span data-ttu-id="81fc1-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="81fc1-119">**Description**</span></span>|  
    |------------|-------------|  
    |<span data-ttu-id="81fc1-120">**Predet.**</span><span class="sxs-lookup"><span data-stu-id="81fc1-120">**Default**</span></span>|<span data-ttu-id="81fc1-121">Indica que el objeto utiliza la intención de acceso a la base de datos predefinida.</span><span class="sxs-lookup"><span data-stu-id="81fc1-121">Indicates that the object uses the predefined database access intent.</span></span>|
    |<span data-ttu-id="81fc1-122">**Permitir escritura**</span><span class="sxs-lookup"><span data-stu-id="81fc1-122">**Allow Write**</span></span>|<span data-ttu-id="81fc1-123">Establece el objeto para usar la base de datos primaria, lo que permite al usuario modificar datos.</span><span class="sxs-lookup"><span data-stu-id="81fc1-123">Sets the object to use the primary database, allowing the user to modify data.</span></span>|
    |<span data-ttu-id="81fc1-124">**Solo lectura**</span><span class="sxs-lookup"><span data-stu-id="81fc1-124">**Read Only**</span></span>|<span data-ttu-id="81fc1-125">Establece el objeto para usar la réplica de la base de datos, lo que significa que el usuario solo puede ver datos, no cambiarlos.</span><span class="sxs-lookup"><span data-stu-id="81fc1-125">Sets the object to use the database replica, which means that the user can only view data, not change data.</span></span>|

2. <span data-ttu-id="81fc1-126">Seleccione la acción **Editar lista**.</span><span class="sxs-lookup"><span data-stu-id="81fc1-126">Choose the **Edit List** action.</span></span>

3. <span data-ttu-id="81fc1-127">En la página **Editar - Lista de intenciones de acceso a la base de datos**, cambie el campo **Intento de acceso** para los objetos.</span><span class="sxs-lookup"><span data-stu-id="81fc1-127">On the **Edit - Database Access Intent List** page, change the **Access Intent** field for the objects.</span></span>

    > [!NOTE]
    > <span data-ttu-id="81fc1-128">Si un objeto que es editable, como la Tarjeta del cliente, se establece en **Solo lectura**, se seguirá utilizando la base de datos principal, independientemente de la intención de acceso, lo que permitirá a los usuarios realizar cambios de forma normal.</span><span class="sxs-lookup"><span data-stu-id="81fc1-128">If an object that is editable, like the Customer Card, is set to **Read Only**, the primary database will still be used, regardless of the access intent, allowing users to make changes as normal.</span></span>

## <a name="see-related-training-at-microsoft-learn"></a><span data-ttu-id="81fc1-129">Consulte Formación relacionada en [Microsoft Learn](/learn/paths/deploy-configure-dynamics-365-business-central/)</span><span class="sxs-lookup"><span data-stu-id="81fc1-129">See Related Training at [Microsoft Learn](/learn/paths/deploy-configure-dynamics-365-business-central/)</span></span>

## <a name="see-also"></a><span data-ttu-id="81fc1-130">Consulte también</span><span class="sxs-lookup"><span data-stu-id="81fc1-130">See Also</span></span>
[<span data-ttu-id="81fc1-131">Funciones empresariales</span><span class="sxs-lookup"><span data-stu-id="81fc1-131">Business Functionality</span></span>](across-business-functionality.md)  
[<span data-ttu-id="81fc1-132">Funciones empresariales generales</span><span class="sxs-lookup"><span data-stu-id="81fc1-132">General Business Functionality</span></span>](ui-across-business-areas.md)  
<span data-ttu-id="81fc1-133">[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="81fc1-133">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="81fc1-134">Introducción</span><span class="sxs-lookup"><span data-stu-id="81fc1-134">Getting Started</span></span>](product-get-started.md)    

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
