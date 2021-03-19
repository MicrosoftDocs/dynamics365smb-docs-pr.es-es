---
title: Configuración del explorador
description: Describe cómo configurar los navegadores para que funcionen con Business Central y los productos que se integran con él.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Teams, web client, troubleshooting, errors
ms.date: 01/08/2021
ms.author: jswymer
ms.openlocfilehash: b5083735be31b635cb3fc3ce404e7f182d04640f
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5384979"
---
# <a name="setting-up-and-troubleshooting-your-browser-to-work-with-business-central-web-client"></a><span data-ttu-id="5caea-103">Configuración y solución de problemas de su navegador para que funcione con Business Central Web Client</span><span class="sxs-lookup"><span data-stu-id="5caea-103">Setting Up and Troubleshooting Your Browser to Work With Business Central Web Client</span></span>

<span data-ttu-id="5caea-104">Este artículo explica cómo configurar su navegador para que [!INCLUDE[web_client](includes/web_client.md)] y todas sus características funcionan correctamente.</span><span class="sxs-lookup"><span data-stu-id="5caea-104">This article explains how to set up your browser so that the [!INCLUDE[web_client](includes/web_client.md)] and all its features work properly.</span></span> <span data-ttu-id="5caea-105">Lea este artículo si tiene problemas para abrir [!INCLUDE[web_client](includes/web_client.md)], porque algunos problemas pueden deberse a la configuración de su navegador.</span><span class="sxs-lookup"><span data-stu-id="5caea-105">Read this article if you're having problems opening the [!INCLUDE[web_client](includes/web_client.md)], because some problems may be caused by your browser's settings.</span></span>

<span data-ttu-id="5caea-106">El artículo proporciona detalles para configurar Microsoft Edge, pero los requisitos para JavaScript, cookies y ventanas emergentes son los mismos para todos los navegadores compatibles.</span><span class="sxs-lookup"><span data-stu-id="5caea-106">The article provides details for setting up Microsoft Edge, but the requirements for JavaScript, cookies, and pop-ups are the same for all supported browsers.</span></span> <span data-ttu-id="5caea-107">Para otros navegadores, consulte las instrucciones proporcionadas por el fabricante.</span><span class="sxs-lookup"><span data-stu-id="5caea-107">For other browsers, refer to the instructions provided by the manufacturer.</span></span>  

## <a name="use-a-supported-browser"></a><span data-ttu-id="5caea-108">Usar un explorador admitido</span><span class="sxs-lookup"><span data-stu-id="5caea-108">Use a supported browser</span></span>

<span data-ttu-id="5caea-109">Asegúrese de utilizar uno de los navegadores compatibles.</span><span class="sxs-lookup"><span data-stu-id="5caea-109">Make sure to use a one of the supported browsers.</span></span> <span data-ttu-id="5caea-110">Vea [Requisitos mínimos para utilizar Business Central](product-requirements.md#recommended-browsers).</span><span class="sxs-lookup"><span data-stu-id="5caea-110">See [Minimum Requirements for Using Business Central](product-requirements.md#recommended-browsers).</span></span>  

## <a name="allow-javascript-from-business-central"></a><span data-ttu-id="5caea-111">Permitir JavaScript desde Business Central</span><span class="sxs-lookup"><span data-stu-id="5caea-111">Allow JavaScript from Business Central</span></span>

<span data-ttu-id="5caea-112">*Problema:*</span><span class="sxs-lookup"><span data-stu-id="5caea-112">*Problem:*</span></span>

<span data-ttu-id="5caea-113">Si el navegador no permite JavaScript, verá **JavaScript no compatible/desactivado** en la barra de direcciones y un mensaje **Error HTTP 404.0: no encontrado** cuando intente abrir [!INCLUDE[prod_short](includes/prod_short.md)] y</span><span class="sxs-lookup"><span data-stu-id="5caea-113">If the browser doesn't allow JavaScript, you'll see **NotSupported/DisabledJavaScript** in the address bar and an **HTTP Error 404.0 - Not Found** message when you try to open [!INCLUDE[prod_short](includes/prod_short.md)], and the</span></span> 

<!-- http://localhost:8080/NotSupported/DisabledJavaScript HTTP Error 404.0 - Not Found
The resource you are looking for has been removed, had its name changed, or is temporarily unavailable. -->

<span data-ttu-id="5caea-114">*Reparar:*</span><span class="sxs-lookup"><span data-stu-id="5caea-114">*Fix:*</span></span>

1. <span data-ttu-id="5caea-115">En Microsoft Edge, vaya a **Configuraciones** > **Cookies y permisos del sitio** > **JavaScript**.</span><span class="sxs-lookup"><span data-stu-id="5caea-115">In Microsoft Edge, go to **Settings** > **Cookies and site permissions** > **JavaScript**.</span></span>
2. <span data-ttu-id="5caea-116">Realice una de los siguientes pasos.</span><span class="sxs-lookup"><span data-stu-id="5caea-116">Do one of the following steps.</span></span> <span data-ttu-id="5caea-117">Elija el paso recomendado por su organización:</span><span class="sxs-lookup"><span data-stu-id="5caea-117">Choose the step that is recommended by your organization:</span></span>

    - <span data-ttu-id="5caea-118">Mueva el control de alternancia **Permitido** a la izquierda (Desactivado).</span><span class="sxs-lookup"><span data-stu-id="5caea-118">Move the **Allowed** toggle to the left (Off).</span></span> <span data-ttu-id="5caea-119">Luego, seleccione **Añadir** y escriba la dirección (URL) para [!INCLUDE[prod_short](includes/prod_short.md)] en el cuadro **Sitio**.</span><span class="sxs-lookup"><span data-stu-id="5caea-119">Then, select **Add** and type the address (URL) for [!INCLUDE[prod_short](includes/prod_short.md)] in the **Site** box.</span></span> <span data-ttu-id="5caea-120">Seleccione **Añadir** cuando termine.</span><span class="sxs-lookup"><span data-stu-id="5caea-120">Select **Add** when done.</span></span>
    - <span data-ttu-id="5caea-121">Mueva el control de alternancia **Permitido** a la derecha (Activado).</span><span class="sxs-lookup"><span data-stu-id="5caea-121">Move the **Allowed** toggle to the right (On).</span></span>

## <a name="allow-cookies-from-business-central"></a><span data-ttu-id="5caea-122">Permitir cookies desde Business Central</span><span class="sxs-lookup"><span data-stu-id="5caea-122">Allow cookies from Business Central</span></span>

<span data-ttu-id="5caea-123">*Problema:*</span><span class="sxs-lookup"><span data-stu-id="5caea-123">*Problem:*</span></span>

<span data-ttu-id="5caea-124">Si el navegador no permite cookies, obtendrá el siguiente error:</span><span class="sxs-lookup"><span data-stu-id="5caea-124">If the browser doesn't allow cookies, you'll get the following error:</span></span>

<span data-ttu-id="5caea-125">**Lo siento, no se pudo encontrar la página. Compruebe la dirección e inténtelo de nuevo.**</span><span class="sxs-lookup"><span data-stu-id="5caea-125">**Sorry, the page could not be found. Please check the address and try again.**</span></span> 

<span data-ttu-id="5caea-126">*Reparar:*</span><span class="sxs-lookup"><span data-stu-id="5caea-126">*Fix:*</span></span>

1. <span data-ttu-id="5caea-127">En Microsoft Edge, vaya a **Configuraciones** > **Cookies y permisos del sitio** > **Cookies y datos del sitio**.</span><span class="sxs-lookup"><span data-stu-id="5caea-127">In Microsoft Edge, go to **Settings** > **Cookies and site permissions** > **Cookies and site data**.</span></span>
2. <span data-ttu-id="5caea-128">Mueva el control de alternancia **Permitir que los sitios guarden y lean datos de cookies** a la derecha (activado).</span><span class="sxs-lookup"><span data-stu-id="5caea-128">Move the **Allow sites to save and read cookie data** toggle to the right (On).</span></span>  

## <a name="allow-pop-ups-from-business-central"></a><a name="popup"></a><span data-ttu-id="5caea-129">Permitir ventanas emergentes desde Business Central</span><span class="sxs-lookup"><span data-stu-id="5caea-129">Allow pop-ups from Business Central</span></span>

[!INCLUDE[prod_short](includes/prod_short.md)] <span data-ttu-id="5caea-130">se integra con varios productos.</span><span class="sxs-lookup"><span data-stu-id="5caea-130">integrates with several products.</span></span> <span data-ttu-id="5caea-131">En algunos casos, como con Microsoft Teams, [!INCLUDE[prod_short](includes/prod_short.md)] se abre, o emerge, dentro del producto.</span><span class="sxs-lookup"><span data-stu-id="5caea-131">In some cases, like with Microsoft Teams, [!INCLUDE[prod_short](includes/prod_short.md)] opens, or "pop-ups", within the product.</span></span> <span data-ttu-id="5caea-132">Esta capacidad requiere que su navegador permita ventanas emergentes de [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="5caea-132">This capability requires that your browser allows pop-ups from [!INCLUDE[prod_short](includes/prod_short.md)].</span></span>

<span data-ttu-id="5caea-133">*Problema:*</span><span class="sxs-lookup"><span data-stu-id="5caea-133">*Problem:*</span></span>

<span data-ttu-id="5caea-134">Si las ventanas emergentes para [!INCLUDE[prod_short](includes/prod_short.md)] están bloqueadas, recibe un mensaje similar al siguiente:</span><span class="sxs-lookup"><span data-stu-id="5caea-134">If pop-ups for [!INCLUDE[prod_short](includes/prod_short.md)] are being blocked, you get a message similar to the following message:</span></span>

<span data-ttu-id="5caea-135">**Algo salió mal. Es posible que su navegador esté bloqueando las ventanas emergentes que necesita Business Central.**</span><span class="sxs-lookup"><span data-stu-id="5caea-135">**Something went wrong. Your browser may be blocking pop-ups needed by Business Central.**</span></span>

<!--
Something went wrong
Your browser may be blocking pop-ups needed by Business Central.

Change your browser settings to allow pop-ups or allow this for trusted domains, then try again.
If these settings are managed for your organization, you should contact your administrator for assistance.

Try again
-->
<span data-ttu-id="5caea-136">*Reparar:*</span><span class="sxs-lookup"><span data-stu-id="5caea-136">*Fix:*</span></span>

1. <span data-ttu-id="5caea-137">En Microsoft Edge, vaya a **Configuraciones** > **Cookies y permisos del sitio** > **Ventanas emergentes y redireccionamientos**.</span><span class="sxs-lookup"><span data-stu-id="5caea-137">In Microsoft Edge, go to **Settings** > **Cookies and site permissions** > **Pop-ups and redirects**.</span></span>
2. <span data-ttu-id="5caea-138">Mueva el control de alternancia **Bloqueado** a la derecha (Activado).</span><span class="sxs-lookup"><span data-stu-id="5caea-138">Move the **Blocked** toggle to the right (On).</span></span>
3. <span data-ttu-id="5caea-139">Seleccione **Añadir**.</span><span class="sxs-lookup"><span data-stu-id="5caea-139">Select **Add**.</span></span> <span data-ttu-id="5caea-140">En el cuadro **Sitio**, escriba `https://businesscentral.dynamics.com`, luego seleccione **Añadir**.</span><span class="sxs-lookup"><span data-stu-id="5caea-140">In the **Site** box, type `https://businesscentral.dynamics.com`, then select **Add**.</span></span>

## <a name="see-also"></a><span data-ttu-id="5caea-141">Consulte también</span><span class="sxs-lookup"><span data-stu-id="5caea-141">See Also</span></span>

[<span data-ttu-id="5caea-142">Consejos para la solución de problemas de Teams</span><span class="sxs-lookup"><span data-stu-id="5caea-142">Troubleshooting Teams</span></span>](admin-teams-troubleshooting.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]