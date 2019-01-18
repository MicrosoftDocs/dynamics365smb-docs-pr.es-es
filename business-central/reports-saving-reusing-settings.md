---
title: "Aplicar y modificar la configuración guardada en los informes | Documentos de Microsoft"
description: Describe las opciones y los filtros predefinidos para personalizar un informe y para generar los datos correctos.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customization, personalization
ms.date: 10/01/2018
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: caf7cf5afe370af0c4294c794c0ff9bc8ff4c31c
ms.openlocfilehash: 9fd086831c0d145570d87c33c62a003c166aca87
ms.contentlocale: es-es
ms.lasthandoff: 11/22/2018

---
# <a name="managing-saved-settings-on-reports"></a><span data-ttu-id="01934-103">Administrar configuración guardada en los informes</span><span class="sxs-lookup"><span data-stu-id="01934-103">Managing Saved Settings on Reports</span></span>
<span data-ttu-id="01934-104">Cuando se ejecuta un informe, a los usuarios normalmente se les presenta una página que les permite definir determinados opciones y filtros para cambiar los datos que se incluyen en el informe generado.</span><span class="sxs-lookup"><span data-stu-id="01934-104">When running a reports, users are typically presented with a page that lets them set certain options and filters for changing the data that is included in the generated report.</span></span> <span data-ttu-id="01934-105">Esta página se llama página de solicitud de informe.</span><span class="sxs-lookup"><span data-stu-id="01934-105">This page is called the report request page.</span></span> <span data-ttu-id="01934-106">Un informe puede incluir una o varias *opciones de configuración guardadas* que los usuarios pueden aplicar al informe de la página de solicitud.</span><span class="sxs-lookup"><span data-stu-id="01934-106">A report can include one or more *saved settings* that users can apply to the report from the request page.</span></span> <span data-ttu-id="01934-107">La *configuración guardada* son básicamente opciones y filtros predeterminados.</span><span class="sxs-lookup"><span data-stu-id="01934-107">*Saved settings* are basically predefined options and filters.</span></span> <span data-ttu-id="01934-108">El uso de la configuración guardada es una forma rápida y confiable de generar de forma coherente informes que contienen los datos correctos.</span><span class="sxs-lookup"><span data-stu-id="01934-108">Using saved settings is a fast and reliable way to consistently generate reports that contain the correct data.</span></span> <span data-ttu-id="01934-109">Para obtener más información acerca de cómo se utilizan los ajustes guardados, consulte [Uso de la configuración guardada](ui-work-report.md#SavedSettings).</span><span class="sxs-lookup"><span data-stu-id="01934-109">For more information about how saved settings are used, see [Using Saved Settings](ui-work-report.md#SavedSettings).</span></span>

<span data-ttu-id="01934-110">Si tiene los permisos adecuados, puede ver, crear y modificar la configuración guardada de todos los informes para todos los usuarios de la empresa.</span><span class="sxs-lookup"><span data-stu-id="01934-110">If you have the proper permissions, you can view, create, and modify the saved settings for all reports for all users in company.</span></span> <span data-ttu-id="01934-111">Puede asignar la configuración guardada de un informe a usuarios individuales o a todos los usuarios de la empresa.</span><span class="sxs-lookup"><span data-stu-id="01934-111">You can assign saved settings for a report to individual users or all users in the company.</span></span>

<!-- 
## Apply saved settings to a report
1. Open the report.

   The report request page appears.    
2. In the **Saved Settings** section of the page, set the **Name** field  to the saved settings that you want to use.

   The **Saved Settings** section only appears if the report has been run before or if there are existing saved settings entries. The saved settings entry called **Last used options and filters** is always available. These settings are the option and filter values that were used the last time you ran the report.

-->

## <a name="create-and-modify-saved-settings-for-all-users"></a><span data-ttu-id="01934-112">Crear y modificar la configuración guardada para todos los usuarios</span><span class="sxs-lookup"><span data-stu-id="01934-112">Create and modify saved settings for all users</span></span>
<span data-ttu-id="01934-113">La configuración guardada se administra en la página **Configuración del informe 1560**.</span><span class="sxs-lookup"><span data-stu-id="01934-113">You manage saved settings from page **1560 Reports Settings**.</span></span> <span data-ttu-id="01934-114">Hay dos maneras de abrir esta página:</span><span class="sxs-lookup"><span data-stu-id="01934-114">There are two ways to open this page:</span></span>
-   <span data-ttu-id="01934-115">Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Config. de informe** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="01934-115">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Report Settings**, and then choose the related link.</span></span>
-   <span data-ttu-id="01934-116">Abra un informe, seleccione la búsqueda junto al cuadro **Utilizar valores predeterminado desde:**, elija **Seleccionar de la lista completa**.</span><span class="sxs-lookup"><span data-stu-id="01934-116">Open a report, choose the lookup next to the **Used default values from:** box, choose **Select from full list**.</span></span>

<span data-ttu-id="01934-117">La página muestra todas las entradas de configuración de almacenamiento existentes para todos los usuarios.</span><span class="sxs-lookup"><span data-stu-id="01934-117">The page displays all the existing save settings entries for all users.</span></span> <span data-ttu-id="01934-118">Si hay un nombre de usuario en la columna **Asignado a**, solo ese usuario puede utilizar los parámetros guardados para el informe asociado.</span><span class="sxs-lookup"><span data-stu-id="01934-118">If there is a user name in the **Assigned to** column, only that user can use the saved settings for the associated report.</span></span> <span data-ttu-id="01934-119">Si hay una marca de verificación en la columna **Compartir con todos los usuarios**, todos los usuarios pueden utilizar las opciones guardadas para el informe.</span><span class="sxs-lookup"><span data-stu-id="01934-119">If there is a check mark in the **Share with all users** column, all users can use the saved settings for the report.</span></span>

<span data-ttu-id="01934-120">Desde la página **Configuración del informe**, puede:</span><span class="sxs-lookup"><span data-stu-id="01934-120">From the **Report Settings** page, you can:</span></span>
-   <span data-ttu-id="01934-121">Seleccione **Nuevo** para crear una nueva entrada de configuración guardada desde cero.</span><span class="sxs-lookup"><span data-stu-id="01934-121">Choose **New** to create a new saved settings entry from scratch.</span></span>
-   <span data-ttu-id="01934-122">Seleccione una entrada de configuración guardada de la lista y seleccione **Copiar** para crear una copia.</span><span class="sxs-lookup"><span data-stu-id="01934-122">Select a saved settings entry from the list, and choose **Copy** to create a copy.</span></span>
-   <span data-ttu-id="01934-123">Seleccione una entrada de configuración guardada de la lista y elija **Editar** para modificar una entrada de configuración guardada.</span><span class="sxs-lookup"><span data-stu-id="01934-123">Select a saved settings entry from the list, and choose **Edit** to modify a saved settings entry.</span></span>


> [!Important]
> <span data-ttu-id="01934-124">Considere el nombre que le asigna a una entrada de configuración guardada.</span><span class="sxs-lookup"><span data-stu-id="01934-124">Consider the name that you give a saved settings entry.</span></span> <span data-ttu-id="01934-125">Si crea una entrada de configuración guardada para todos los usuarios y le asigna el mismo nombre que la entrada de configuración guardada existente que está asignada a un usuario determinado únicamente, ese usuario no podrá utilizar la entrada de configuración guardada que se asigne a todos.</span><span class="sxs-lookup"><span data-stu-id="01934-125">If you create a saved settings entry for all users, and you give it the same name as an existing saved settings entry that is assigned to a specific user only, then that user will not be able to use the saved settings entry that is assigned to everyone.</span></span>  <span data-ttu-id="01934-126">En **Configuración guardada** de la página de solicitud de informe, el usuario verá dos entradas de configuración guardada con el mismo nombre.</span><span class="sxs-lookup"><span data-stu-id="01934-126">Under **Saved Settings** on the report request page, the user will see two saved settings entries with the same name.</span></span> <span data-ttu-id="01934-127">Sin embargo, independientemente de la opción que elija, se usará la entrada de configuración guardada específica del usuario.</span><span class="sxs-lookup"><span data-stu-id="01934-127">However, no matter which option he chooses, the user-specific saved settings entry will be used.</span></span>

> [!NOTE]
> <span data-ttu-id="01934-128">La característica de configuración guardada solo está disponible en los informes en los que la [propiedad SaveValues](https://docs.microsoft.com/en-us/dynamics-nav/savevalues-property) de la página de solicitud del informe está establecida en `Yes`.</span><span class="sxs-lookup"><span data-stu-id="01934-128">The saved settings feature is available only on reports where the [SaveValues property](https://docs.microsoft.com/en-us/dynamics-nav/savevalues-property) of the report's request page is set to `Yes`.</span></span> <span data-ttu-id="01934-129">La propiedad **SaveValues** se define en el entorno de desarrollo.</span><span class="sxs-lookup"><span data-stu-id="01934-129">The **SaveValues** property is set in the development environment.</span></span>  

## <a name="see-also"></a><span data-ttu-id="01934-130">Consulte también</span><span class="sxs-lookup"><span data-stu-id="01934-130">See Also</span></span>
[<span data-ttu-id="01934-131">Trabajar con informes</span><span class="sxs-lookup"><span data-stu-id="01934-131">Working with Reports</span></span>](ui-work-report.md)  

