---
title: "Configurar los orígenes web para empresas de contacto | Documentos de Microsoft"
description: "Puede definir sus orígenes web o de Internet y asignarlos a una empresa de contacto para identificar cómo desea buscar la información de sus contactos."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: internet
ms.date: 06/06/2017
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: b81deefcdf79a93cc988d216f80b08794efb8ab6
ms.contentlocale: es-es
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-set-up-web-sources-for-contact-companies"></a><span data-ttu-id="75817-103">Configurar enlaces web para empresas de contacto</span><span class="sxs-lookup"><span data-stu-id="75817-103">How to: Set Up Web Sources for Contact Companies</span></span>
<span data-ttu-id="75817-104">Puede usar enlaces web con sus empresas de contacto para identificar, por ejemplo, los motores de búsqueda y los sitios web de Internet que quiere usar para buscar información sobre los contactos.</span><span class="sxs-lookup"><span data-stu-id="75817-104">You can use web sources with your contact companies to identify, for example, search engines and web sites, on the Internet that you want to use to search for information about the contacts.</span></span> <span data-ttu-id="75817-105">Al asignar enlaces web, especifica el motor de búsqueda y la palabra clave que la aplicación usará para buscar la información solicitada.</span><span class="sxs-lookup"><span data-stu-id="75817-105">When assigning web sources, you specify which search engine and search word the application will use to find the requested information.</span></span>

<span data-ttu-id="75817-106">El uso de enlaces web en contactos es un proceso que consta de dos pasos.</span><span class="sxs-lookup"><span data-stu-id="75817-106">Using web sources on contacts is a two-step process.</span></span> <span data-ttu-id="75817-107">Primero, debe definir el código del enlace web.</span><span class="sxs-lookup"><span data-stu-id="75817-107">First, you define the web source code.</span></span> <span data-ttu-id="75817-108">Solo debe realizar este paso una vez para cada enlace web.</span><span class="sxs-lookup"><span data-stu-id="75817-108">You only have to perform this step one time for each web source.</span></span> <span data-ttu-id="75817-109">Una vez tenga código de enlace web, puede comenzar a asignar el código a personas de contacto.</span><span class="sxs-lookup"><span data-stu-id="75817-109">Once you have a web source code, you can start to assign the code to contact persons.</span></span>

## <a name="to-define-a-web-source-code"></a><span data-ttu-id="75817-110">Para definir un código de enlace Web</span><span class="sxs-lookup"><span data-stu-id="75817-110">To define a web source code</span></span>
1. <span data-ttu-id="75817-111">Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Enlaces web** y, a continuación, seleccione el vínculo relacionado.</span><span class="sxs-lookup"><span data-stu-id="75817-111">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Web Sources**, and then choose the related link.</span></span>
2. <span data-ttu-id="75817-112">Elija la acción **Nuevo**.</span><span class="sxs-lookup"><span data-stu-id="75817-112">Choose the **New** actions.</span></span>
3. <span data-ttu-id="75817-113">Rellene los campos **Código**, **Descripción** y **URL**.</span><span class="sxs-lookup"><span data-stu-id="75817-113">Fill in the **Code**, **Description**, and **URL** fields.</span></span>

    <span data-ttu-id="75817-114">Escriba %1 en el campo **Dirección URL** para insertar un marcador de posición para una palabra de búsqueda en la URL.</span><span class="sxs-lookup"><span data-stu-id="75817-114">Type %1 in the **URL** field to insert a placeholder for a search word in the URL.</span></span> <span data-ttu-id="75817-115">Al ejecutar al enlace web desde una ficha de contacto, %1 se reemplaza con la palabra de búsqueda, por ejemplo, el nombre de la empresa, especificada en la ventana **Enlaces web de contactos**.</span><span class="sxs-lookup"><span data-stu-id="75817-115">When you launch the web source from a contact, the %1 is replaced with the search word, for example, the name of the company that you have entered in the **Contact Web Sources** window.</span></span>

<span data-ttu-id="75817-116">Repita estos pasos para configurar todos los orígenes web que desee.</span><span class="sxs-lookup"><span data-stu-id="75817-116">Repeat these steps to set up as many web sources as you want.</span></span>

## <a name="to-assign-web-sources-to-a-contact-company"></a><span data-ttu-id="75817-117">Para asignar enlaces Web a una empresa de contacto</span><span class="sxs-lookup"><span data-stu-id="75817-117">To assign web sources to a contact company</span></span>
<span data-ttu-id="75817-118">Al asignar enlaces web, especifica el motor de búsqueda y la palabra clave que la aplicación usará para buscar la información solicitada.</span><span class="sxs-lookup"><span data-stu-id="75817-118">When assigning web sources, you specify which search engine and search word that the application will use to find the requested information.</span></span>

1. <span data-ttu-id="75817-119">Abra el contacto.</span><span class="sxs-lookup"><span data-stu-id="75817-119">Open the contact.</span></span>
2. <span data-ttu-id="75817-120">Elija la acción **Empresa** y, a continuación, elija la acción **Enlaces web**.</span><span class="sxs-lookup"><span data-stu-id="75817-120">Choose the **Company** action, and then choose the **Web Sources** action.</span></span> <span data-ttu-id="75817-121">Se abre la ventana **Enlaces web contacto**.</span><span class="sxs-lookup"><span data-stu-id="75817-121">The **Contact Web Sources** window opens.</span></span>
3. <span data-ttu-id="75817-122">En el campo **Código de enlace web**, elija el enlace web que desea asignar.</span><span class="sxs-lookup"><span data-stu-id="75817-122">In the **Web Source Code** field, choose the web source you want to assign.</span></span>
4. <span data-ttu-id="75817-123">Escriba en el campo **Busca palabra**, escriba la palabra de búsqueda que desea que use el sistema para buscar la información.</span><span class="sxs-lookup"><span data-stu-id="75817-123">In the **Search Word** field, enter the search word that you want to use to find the information.</span></span>

<span data-ttu-id="75817-124">Repita estos pasos para asignar todos los orígenes web que desee.</span><span class="sxs-lookup"><span data-stu-id="75817-124">Repeat these steps to assign as many web sources as you want.</span></span>

<span data-ttu-id="75817-125">También puede asignar enlaces web, con el mismo procedimiento, en la ventana **Lista contactos**.</span><span class="sxs-lookup"><span data-stu-id="75817-125">You can also assign web sources from the **Contact List** window by following the same procedure.</span></span>

## <a name="see-also"></a><span data-ttu-id="75817-126">Consulte también</span><span class="sxs-lookup"><span data-stu-id="75817-126">See Also</span></span>
[<span data-ttu-id="75817-127">Crear empresas de contacto</span><span class="sxs-lookup"><span data-stu-id="75817-127">Creating Contact Companies</span></span>](marketing-create-contact-companies.md)  
<span data-ttu-id="75817-128">[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="75817-128">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

