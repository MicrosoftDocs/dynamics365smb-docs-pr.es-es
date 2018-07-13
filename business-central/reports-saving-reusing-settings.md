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
ms.date: 09/08/2017
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: 2286b728a464943841b192031cfea13644441013
ms.openlocfilehash: f5225d1f6d0d4ac0020fb073d5df6da83b5c0f5b
ms.contentlocale: es-es
ms.lasthandoff: 06/28/2018

---
# <a name="managing-saved-settings-on-reports"></a><span data-ttu-id="df265-103">Administrar configuración guardada en los informes</span><span class="sxs-lookup"><span data-stu-id="df265-103">Managing Saved Settings on Reports</span></span>
<span data-ttu-id="df265-104">Según el informe que se ejecute, es posible que se le presente una página que permite definir determinadas opciones y filtros para cambiar los datos que se incluyen en el informe generado.</span><span class="sxs-lookup"><span data-stu-id="df265-104">Depending on the report that is run, you might be presented with a page that lets you to set certain options and filters for changing the data that is included in the generated report.</span></span> <span data-ttu-id="df265-105">Esta página se conoce como la página de solicitud de informe.</span><span class="sxs-lookup"><span data-stu-id="df265-105">This page is known as the report request page.</span></span> <span data-ttu-id="df265-106">Un informe puede incluir una o varias *opciones de configuración guardadas* que puede aplicar al informe de la página de solicitud.</span><span class="sxs-lookup"><span data-stu-id="df265-106">A report can include one or more *saved settings* that you can apply to the report from the request page.</span></span> <span data-ttu-id="df265-107">La *configuración guardada* son básicamente opciones y filtros predeterminados.</span><span class="sxs-lookup"><span data-stu-id="df265-107">*Saved settings* are basically predefined options and filters.</span></span> <span data-ttu-id="df265-108">El uso de la configuración guardada es una forma rápida y confiable de generar de forma coherente informes que contienen los datos correctos.</span><span class="sxs-lookup"><span data-stu-id="df265-108">Using saved settings is a fast and reliable way to consistently generate reports that contain the correct data.</span></span>

<span data-ttu-id="df265-109">Puede ver la configuración guardada que están a su disposición para un informe en la sección **Configuración guardada** de la página de solicitud de informe.</span><span class="sxs-lookup"><span data-stu-id="df265-109">You can see the saved settings that are available to you for a report in **Saved Settings** section of the report request page.</span></span>  

## <a name="apply-saved-settings-to-a-report"></a><span data-ttu-id="df265-110">Aplicar la configuración guardada a un informe</span><span class="sxs-lookup"><span data-stu-id="df265-110">Apply saved settings to a report</span></span>
1. <span data-ttu-id="df265-111">Abra el informe.</span><span class="sxs-lookup"><span data-stu-id="df265-111">Open the report.</span></span>

   <span data-ttu-id="df265-112">Aparece la página de solicitud de informe.</span><span class="sxs-lookup"><span data-stu-id="df265-112">The report request page appears.</span></span>    
2. <span data-ttu-id="df265-113">En la sección **Configuración guardada** de la página, configure el campo **Nombre** como la configuración guardada que desea usar.</span><span class="sxs-lookup"><span data-stu-id="df265-113">In the **Saved Settings** section of the page, set the **Name** field  to the saved settings that you want to use.</span></span>

   <span data-ttu-id="df265-114">La sección **Valores guardados** solo aparece si el informe se ha ejecutado antes o si hay configuraciones existentes guardadas.</span><span class="sxs-lookup"><span data-stu-id="df265-114">The **Saved Settings** section only appears if the report has been run before or if there are existing saved settings entries.</span></span> <span data-ttu-id="df265-115">La configuración guardada que se denomina **Filtros y opciones usados por última vez** está siempre disponible.</span><span class="sxs-lookup"><span data-stu-id="df265-115">The saved settings entry called **Last used options and filters** is always available.</span></span> <span data-ttu-id="df265-116">Esta configuración son los valores de opción y filtro que se utilizaron la última vez que ejecutó el informe.</span><span class="sxs-lookup"><span data-stu-id="df265-116">These settings are the option and filter values that were used the last time you ran the report.</span></span>

## <a name="create-and-modify-saved-settings-for-all-users"></a><span data-ttu-id="df265-117">Crear y modificar la configuración guardada para todos los usuarios</span><span class="sxs-lookup"><span data-stu-id="df265-117">Create and modify saved settings for all users</span></span>
<span data-ttu-id="df265-118">Si tiene los permisos adecuados, puede ver, crear y modificar la configuración guardada de todos los informes para todos los usuarios de la empresa.</span><span class="sxs-lookup"><span data-stu-id="df265-118">If you have the proper permissions, you can view, create, and modify the saved settings for all reports for all users in company.</span></span> <span data-ttu-id="df265-119">Puede asignar la configuración guardada de un informe a usuarios individuales o a todos los usuarios de la empresa.</span><span class="sxs-lookup"><span data-stu-id="df265-119">You can assign saved settings for a report to individual users or all users in the company.</span></span>

<span data-ttu-id="df265-120">La configuración guardada se administra en la página 1506 **Configuración del informe**.</span><span class="sxs-lookup"><span data-stu-id="df265-120">You manage saved settings from page 1506 **Reports Settings**.</span></span> <span data-ttu-id="df265-121">Para abrir esta página, elija el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Configuración del informe** y, a continuación, seleccione el vínculo relacionado.</span><span class="sxs-lookup"><span data-stu-id="df265-121">To open this page, choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Report Settings**, and then choose the related link.</span></span>

<span data-ttu-id="df265-122">En la página **Configuración del informe**, puede crear nuevos valores de cero o hacer una copia y modificar la configuración existente.</span><span class="sxs-lookup"><span data-stu-id="df265-122">From the **Report Settings** page, you can create a new settings from scratch or you can make a copy and modify existing settings.</span></span> <span data-ttu-id="df265-123">Para modificar las opciones y los filtros de una configuración, elija la acción **Editar**.</span><span class="sxs-lookup"><span data-stu-id="df265-123">To modify the options and filters for a settings, choose the **Edit** action.</span></span>

> [!NOTE]
> <span data-ttu-id="df265-124">La característica de configuración guardada en informes es relevante únicamente cuando la propiedad SaveValues de la página de solicitud se define en Sí.</span><span class="sxs-lookup"><span data-stu-id="df265-124">The saved settings feature on reports is only relevant when the SaveValues property of the request page is set to Yes.</span></span> <span data-ttu-id="df265-125">La propiedad SaveValues se define en el entorno de desarrollo.</span><span class="sxs-lookup"><span data-stu-id="df265-125">The SaveValues property property is set in the development environment.</span></span>  

> [!Important]
> <span data-ttu-id="df265-126">Si crea un elemento de configuración guardada para todos los usuarios y tiene el mismo nombre que la configuración guardada existente de un usuario determinado, ese usuario no podrá utilizar la configuración guardada que se asigne a todos.</span><span class="sxs-lookup"><span data-stu-id="df265-126">If you create a saved settings item for all users, and it has the same name as an existing saved settings for a specific user, then that user will not be able to use the saved settings that is assigned to everyone.</span></span>  <span data-ttu-id="df265-127">En el campo Configuración guardada de la página de solicitud de informe, el usuario verá dos opciones de configuración guardada con el mismo nombre.</span><span class="sxs-lookup"><span data-stu-id="df265-127">In the Saved Settings field on the report request page, the user will see two saved settings options with the same name.</span></span> <span data-ttu-id="df265-128">Sin embargo, independientemente de la opción que elija, se usará la configuración guardada específica del usuario.</span><span class="sxs-lookup"><span data-stu-id="df265-128">However, no matter which option he chooses, the user-specific saved settings will be used.</span></span>

## <a name="see-also"></a><span data-ttu-id="df265-129">Consulte también</span><span class="sxs-lookup"><span data-stu-id="df265-129">See Also</span></span>
[<span data-ttu-id="df265-130">Trabajar con informes</span><span class="sxs-lookup"><span data-stu-id="df265-130">Working with Reports</span></span>](ui-work-report.md)  

