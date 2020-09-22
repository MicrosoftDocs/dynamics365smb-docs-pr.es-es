---
title: Aplicar y modificar la configuración guardada en los informes | Documentos de Microsoft
description: Describe las opciones y los filtros predefinidos para personalizar un informe y para generar los datos correctos.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customization, personalization
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: d61e599b9e86f28de6edcf4ccff5b245503880fe
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 09/09/2020
ms.locfileid: "3784614"
---
# <a name="manage-saved-settings-for-reports-and-batch-jobs"></a><span data-ttu-id="cf55a-103">Administrar configuraciones guardadas para informes y trabajos por lotes</span><span class="sxs-lookup"><span data-stu-id="cf55a-103">Manage Saved Settings for Reports and Batch jobs</span></span>
<span data-ttu-id="cf55a-104">Cuando se ejecutan informes, a los usuarios normalmente se les presenta una página que les permite seleccionar opciones y establecer filtros para cambiar los datos que se incluyen en el informe generado.</span><span class="sxs-lookup"><span data-stu-id="cf55a-104">When running reports, users are typically presented with a page that lets them select options and set filters to change the data that is included in the generated report.</span></span> <span data-ttu-id="cf55a-105">Esta página se llama página de solicitud.</span><span class="sxs-lookup"><span data-stu-id="cf55a-105">This page is called the request page.</span></span> <span data-ttu-id="cf55a-106">Un informe puede incluir una o varias *opciones de configuración guardadas* que los usuarios pueden aplicar al informe de la página de solicitud.</span><span class="sxs-lookup"><span data-stu-id="cf55a-106">A report can include one or more *saved settings* that users can apply to the report from the request page.</span></span> <span data-ttu-id="cf55a-107">La *configuración guardada* son básicamente opciones y filtros predeterminados.</span><span class="sxs-lookup"><span data-stu-id="cf55a-107">*Saved settings* are basically predefined options and filters.</span></span> <span data-ttu-id="cf55a-108">El uso de la configuración guardada es una forma rápida y confiable de generar de forma coherente informes que contienen los datos correctos.</span><span class="sxs-lookup"><span data-stu-id="cf55a-108">Using saved settings is a fast and reliable way to consistently generate reports that contain the correct data.</span></span> <span data-ttu-id="cf55a-109">Para obtener más información, consulte [Uso de la configuración guardada](ui-work-report.md#SavedSettings).</span><span class="sxs-lookup"><span data-stu-id="cf55a-109">For more information, see [Using Saved Settings](ui-work-report.md#SavedSettings).</span></span>

> [!NOTE]
> <span data-ttu-id="cf55a-110">Este tema hace referencia principalmente al "informe", pero se aplica información similar a los trabajos por lotes.</span><span class="sxs-lookup"><span data-stu-id="cf55a-110">This topic refers mainly to "report", but similar information applies to batch jobs.</span></span>

<span data-ttu-id="cf55a-111">Si tiene los permisos adecuados, puede ver, crear y modificar la configuración guardada de todos los informes para todos los usuarios de una empresa.</span><span class="sxs-lookup"><span data-stu-id="cf55a-111">If you have the proper permissions, you can view, create, and modify the saved settings for all reports for all users in a company.</span></span> <span data-ttu-id="cf55a-112">Puede asignar la configuración guardada de un informe a usuarios individuales o a todos los usuarios de la empresa.</span><span class="sxs-lookup"><span data-stu-id="cf55a-112">You can assign saved settings for a report to individual users or to all users in the company.</span></span>

<!--
## Apply saved settings to a report
1. Open the report.

   The request page appears.    
2. In the **Saved Settings** section of the page, set the **Name** field  to the saved settings that you want to use.

   The **Saved Settings** section only appears if the report has been run before or if there are existing saved settings entries. The saved settings entry called **Last used options and filters** is always available. These settings are the option and filter values that were used the last time you ran the report.

-->

## <a name="to-create-and-modify-saved-settings-for-all-users"></a><span data-ttu-id="cf55a-113">Para crear y modificar la configuración guardada para todos los usuarios</span><span class="sxs-lookup"><span data-stu-id="cf55a-113">To create and modify saved settings for all users</span></span>
<span data-ttu-id="cf55a-114">La configuración guardada se administra en la página **Configuración de informes**.</span><span class="sxs-lookup"><span data-stu-id="cf55a-114">You manage saved settings on the **Reports Settings** page.</span></span> <span data-ttu-id="cf55a-115">Hay dos maneras de abrir esta página:</span><span class="sxs-lookup"><span data-stu-id="cf55a-115">There are two ways to open this page:</span></span>
-   <span data-ttu-id="cf55a-116">Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Configuración del informe** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="cf55a-116">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Report Settings**, and then choose the related link.</span></span>
-   <span data-ttu-id="cf55a-117">Abra un informe, seleccione la búsqueda en el campo **Utilizar valores predeterminado desde** y, a continuación, elija la acción **Seleccionar de la lista completa**.</span><span class="sxs-lookup"><span data-stu-id="cf55a-117">Open a report, choose the lookup in the **Use default values from** field, and then choose the **Select from full list** action.</span></span>

<span data-ttu-id="cf55a-118">La página muestra todas las entradas de configuración guardada de almacenamiento existentes para todos los usuarios.</span><span class="sxs-lookup"><span data-stu-id="cf55a-118">The page displays all the existing saved settings entries for all users.</span></span> <span data-ttu-id="cf55a-119">Si hay un nombre de usuario en el campo **Asignado a**, solo ese usuario puede utilizar los parámetros guardados para el informe asociado.</span><span class="sxs-lookup"><span data-stu-id="cf55a-119">If there is a user name in the **Assigned to** field, only that user can use the saved settings for the associated report.</span></span> <span data-ttu-id="cf55a-120">Si hay una marca de verificación en el campo **Compartir con todos los usuarios**, todos los usuarios pueden utilizar las opciones guardadas para el informe.</span><span class="sxs-lookup"><span data-stu-id="cf55a-120">If there is a check mark in the **Share with all users** field, all users can use the saved settings for the report.</span></span>

<span data-ttu-id="cf55a-121">Desde la página **Configuración del informe**, puede:</span><span class="sxs-lookup"><span data-stu-id="cf55a-121">From the **Report Settings** page, you can:</span></span>
-   <span data-ttu-id="cf55a-122">Seleccione la acción **Nuevo** para crear una nueva entrada de configuración guardada desde cero.</span><span class="sxs-lookup"><span data-stu-id="cf55a-122">Choose the **New** action to create a new saved settings entry from scratch.</span></span>
-   <span data-ttu-id="cf55a-123">Seleccione una entrada de configuración guardada de la lista y seleccione la acción **Copiar** para crear una copia.</span><span class="sxs-lookup"><span data-stu-id="cf55a-123">Select a saved settings entry from the list, and choose the **Copy** action to create a copy.</span></span>
-   <span data-ttu-id="cf55a-124">Seleccione una entrada de configuración guardada de la lista y elija la acción **Editar** para modificar una entrada de configuración guardada.</span><span class="sxs-lookup"><span data-stu-id="cf55a-124">Select a saved settings entry from the list, and choose the **Edit** action to modify a saved settings entry.</span></span>

> [!Important]
> <span data-ttu-id="cf55a-125">Considere el nombre que le asigna a una entrada de configuración guardada.</span><span class="sxs-lookup"><span data-stu-id="cf55a-125">Consider the name that you give a saved settings entry.</span></span> <span data-ttu-id="cf55a-126">Si crea una entrada de configuración guardada para todos los usuarios y le asigna el mismo nombre que la entrada de configuración guardada existente que está asignada a un usuario determinado únicamente, ese usuario no podrá utilizar la entrada de configuración guardada que se asigne a todos.</span><span class="sxs-lookup"><span data-stu-id="cf55a-126">If you create a saved settings entry for all users, and you give it the same name as an existing saved settings entry that is assigned to a specific user only, then that user will not be able to use the saved settings entry that is assigned to everyone.</span></span>  <span data-ttu-id="cf55a-127">En la sección **Configuración guardada** de la página de solicitud, el usuario verá dos entradas de configuración guardada con el mismo nombre.</span><span class="sxs-lookup"><span data-stu-id="cf55a-127">In the **Saved Settings** section on the request page, the user will see two saved settings entries with the same name.</span></span> <span data-ttu-id="cf55a-128">Sin embargo, independientemente de la opción que elija, se usará la entrada de configuración guardada específica del usuario.</span><span class="sxs-lookup"><span data-stu-id="cf55a-128">However, no matter which option they choose, the user-specific saved settings entry will be used.</span></span>

> [!NOTE]
> <span data-ttu-id="cf55a-129">La característica Configuración guardada solo está disponible en los informes en los que la [propiedad SaveValues](/dynamics365/business-central/dev-itpro/developer/properties/devenv-savevalues-property) de la página de solicitud del informe está establecida en **Sí**.</span><span class="sxs-lookup"><span data-stu-id="cf55a-129">The Saved Settings feature is available only on reports where the [SaveValues property](/dynamics365/business-central/dev-itpro/developer/properties/devenv-savevalues-property) of the report's request page is set to **Yes**.</span></span> <span data-ttu-id="cf55a-130">La propiedad **SaveValues** se define en el entorno de desarrollo.</span><span class="sxs-lookup"><span data-stu-id="cf55a-130">The **SaveValues** property is set in the development environment.</span></span>  

## <a name="see-also"></a><span data-ttu-id="cf55a-131">Consulte también</span><span class="sxs-lookup"><span data-stu-id="cf55a-131">See Also</span></span>
[<span data-ttu-id="cf55a-132">Trabajar con informes, trabajos por lotes y XMLports</span><span class="sxs-lookup"><span data-stu-id="cf55a-132">Working with Reports, Batch Jobs, and XMLports</span></span>](ui-work-report.md)  
