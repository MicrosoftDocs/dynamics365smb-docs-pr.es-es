---
title: Configurar plantillas de API | Documentos de Microsoft
description: Describa los pasos que debe seguir para configurar las plantillas API para Dynamics 365 Business Central.
services: project-madeira
documentationcenter: 
author: SusanneWindfeldPedersen
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: API templates, configuring templates
ms.date: 10/01/2018
ms.author: solsen
ms.translationtype: HT
ms.sourcegitcommit: 33b900f1ac9e295921e7f3d6ea72cc93939d8a1b
ms.openlocfilehash: 7420bd1b8c1c246b608910a35a47ac025eec6b8b
ms.contentlocale: es-es
ms.lasthandoff: 11/26/2018

---

# <a name="configuring-api-templates"></a><span data-ttu-id="78fbd-103">Configuración de plantillas API</span><span class="sxs-lookup"><span data-stu-id="78fbd-103">Configuring API Templates</span></span>
<span data-ttu-id="78fbd-104">La biblioteca API para [!INCLUDE[d365fin_md](includes/d365fin_md.md)] proporciona una representación simplificada de las entidades subyacentes.</span><span class="sxs-lookup"><span data-stu-id="78fbd-104">The API library for [!INCLUDE[d365fin_md](includes/d365fin_md.md)] provides a simplified representation of the underlying entities.</span></span> <span data-ttu-id="78fbd-105">Todas las propiedades de la aplicación no están expuestas a través de la API asociada.</span><span class="sxs-lookup"><span data-stu-id="78fbd-105">All the properties in the application are not exposed through the associated API.</span></span> <span data-ttu-id="78fbd-106">La página **Configuración de API** le permite definir plantillas que se utilizan para llenar propiedades vacías en una entidad cuando crea una acción POST a través de la API.</span><span class="sxs-lookup"><span data-stu-id="78fbd-106">The **API Setup** page allows you to define templates that are used to populate empty properties on an entity when you create a POST action through the API.</span></span> 

<span data-ttu-id="78fbd-107">Por ejemplo, si se define una plantilla de configuración para la entidad del elemento, cuando se crea un nuevo registro del elemento a través de la API de elementos, las propiedades del nuevo elemento que no están definidas en la API se rellenarán a partir de la plantilla seleccionada.</span><span class="sxs-lookup"><span data-stu-id="78fbd-107">For example, if a configuration template is defined for the item entity, when a new item record is created through the items API, any properties for the new item that are not defined in the API call will be populated from the selected template.</span></span> <span data-ttu-id="78fbd-108">Si, por ejemplo, no se define ningún valor para el campo **Grupo contable producto** a través de la API, pero se define un valor en la plantilla seleccionada, el valor del grupo definido en la plantilla se aplicará al nuevo elemento.</span><span class="sxs-lookup"><span data-stu-id="78fbd-108">If, for example, no value is defined for the **Gen. Prod. Posting Group** field through the API, but a value is defined in the selected template, then the posting group value defined in the template will be applied to the new item.</span></span> 

## <a name="setting-up-the-entity-template"></a><span data-ttu-id="78fbd-109">Configuración de la plantilla de entidad</span><span class="sxs-lookup"><span data-stu-id="78fbd-109">Setting up the Entity Template</span></span>
<span data-ttu-id="78fbd-110">Para usar plantillas con la biblioteca API, primero debe configurar y definir propiedades para las plantillas.</span><span class="sxs-lookup"><span data-stu-id="78fbd-110">To use templates with the API library, you must first set up and define properties for the templates.</span></span> <span data-ttu-id="78fbd-111">Puede configurar estas plantillas en la página **Plantillas de configuración**.</span><span class="sxs-lookup"><span data-stu-id="78fbd-111">You can set up these templates on the **Configuration Templates** page.</span></span> <span data-ttu-id="78fbd-112">Para obtener más información, consulte [Prepararse para migrar datos del cliente](admin-use-templates-to-prepare-customer-data-for-migration.md).</span><span class="sxs-lookup"><span data-stu-id="78fbd-112">For more information, see [Prepare to Migrate Customer Data](admin-use-templates-to-prepare-customer-data-for-migration.md).</span></span> 

## <a name="assign-the-template-to-an-api"></a><span data-ttu-id="78fbd-113">Asigne la plantilla a una API</span><span class="sxs-lookup"><span data-stu-id="78fbd-113">Assign the template to an API</span></span>

<span data-ttu-id="78fbd-114">Para asignar una plantilla a una API, debe seguir los siguientes pasos.</span><span class="sxs-lookup"><span data-stu-id="78fbd-114">To assign a template to an API, you must go through the following steps.</span></span>

1. <span data-ttu-id="78fbd-115">Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Configuración de API** y elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="78fbd-115">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **API Setup**, and choose the related link.</span></span>
2. <span data-ttu-id="78fbd-116">Seleccione **Nuevo** y el valor **Orden** para el registro.</span><span class="sxs-lookup"><span data-stu-id="78fbd-116">Choose **New**, and then choose the **Order** value for the record.</span></span>  
<span data-ttu-id="78fbd-117">Si hay más de una plantilla seleccionada para una API (ID de página), las plantillas se aplican en el orden definido en la columna **Pedido**.</span><span class="sxs-lookup"><span data-stu-id="78fbd-117">If there is more than one template selected for an API (Page ID), the templates are applied in the order defined in the **Order** column.</span></span>   
<span data-ttu-id="78fbd-118">Cuando se aplican las plantillas, los valores de campo definidos en la plantilla solo se aplican a los campos que aún no tienen un valor definido, ya sea explícitamente en la API o en una plantilla previamente aplicada en el pedido.</span><span class="sxs-lookup"><span data-stu-id="78fbd-118">When each template is applied, field values defined in the template are only applied to fields that have not already had a value defined, either explicitly in the API, or in a previously applied template in the order.</span></span> 
3. <span data-ttu-id="78fbd-119">Seleccionar un valor de **ID de página**.</span><span class="sxs-lookup"><span data-stu-id="78fbd-119">Select a **Page ID** value.</span></span>  
<span data-ttu-id="78fbd-120">Esta es la página de la API a la que se aplicará la plantilla.</span><span class="sxs-lookup"><span data-stu-id="78fbd-120">This is the page for the API to which the template will be applied.</span></span> <span data-ttu-id="78fbd-121">La búsqueda de **ID de página** proporciona una lista de todas las API disponibles en la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="78fbd-121">The **Page ID** lookup provides a list of all APIs available in the library.</span></span>
4. <span data-ttu-id="78fbd-122">Seleccione un valor en el campo **Código de plantilla**.</span><span class="sxs-lookup"><span data-stu-id="78fbd-122">Select a value in the **Template Code** field.</span></span>  
<span data-ttu-id="78fbd-123">El código de plantilla es el código para la plantilla que se definió en la página **Plantillas de configuración**.</span><span class="sxs-lookup"><span data-stu-id="78fbd-123">The template code is the code for the template that was defined on the **Configuration Templates** page.</span></span> <span data-ttu-id="78fbd-124">Los valores de plantilla definidos se aplican a la API.</span><span class="sxs-lookup"><span data-stu-id="78fbd-124">The template values defined are applied to the API.</span></span> 
5. <span data-ttu-id="78fbd-125">En el campo **Condiciones**, especifique qué plantilla se debe aplicar.</span><span class="sxs-lookup"><span data-stu-id="78fbd-125">In the **Conditions** field, specify which template should be applied.</span></span>  
<span data-ttu-id="78fbd-126">La plantilla definida se aplica a un nuevo registro creado a través de la API si, y únicamente en el caso de que, las condiciones definidas en el campo **Condiciones** se cumplan con los valores ya definidos para la nueva instancia de la entidad.</span><span class="sxs-lookup"><span data-stu-id="78fbd-126">The defined template is applied to a new record created through the API if, and only if, the conditions defined in the **Conditions** field are met by the values already defined for the new instance of the entity.</span></span>

## <a name="see-also"></a><span data-ttu-id="78fbd-127">Consulte también</span><span class="sxs-lookup"><span data-stu-id="78fbd-127">See Also</span></span>
[<span data-ttu-id="78fbd-128">Documentación de la API</span><span class="sxs-lookup"><span data-stu-id="78fbd-128">API Documentation</span></span>](/dynamics-nav/fin-graph)  
<span data-ttu-id="78fbd-129">[Desarrollo de aplicaciones de conexión para [!INCLUDE[d365fin_md](includes/d365fin_md.md)]](/dynamics365/business-central/dev-itpro/developer/devenv-develop-connect-apps)</span><span class="sxs-lookup"><span data-stu-id="78fbd-129">[Developing Connect Apps for [!INCLUDE[d365fin_md](includes/d365fin_md.md)]](/dynamics365/business-central/dev-itpro/developer/devenv-develop-connect-apps)</span></span>  
[<span data-ttu-id="78fbd-130">Activar las API</span><span class="sxs-lookup"><span data-stu-id="78fbd-130">Enabling the APIs</span></span>](/dynamics-nav/enabling-apis-for-dynamics-nav)  
[<span data-ttu-id="78fbd-131">Extremos para las API</span><span class="sxs-lookup"><span data-stu-id="78fbd-131">Endpoints for the APIs</span></span>](/dynamics-nav/endpoints-apis-for-dynamics)  
[<span data-ttu-id="78fbd-132">Configurar una empresa con RapidStart Services</span><span class="sxs-lookup"><span data-stu-id="78fbd-132">Setting Up a Company with RapidStart Services</span></span>](admin-set-up-a-company-with-rapidstart.md)  
[<span data-ttu-id="78fbd-133">Administración</span><span class="sxs-lookup"><span data-stu-id="78fbd-133">Administration</span></span>](admin-setup-and-administration.md)
