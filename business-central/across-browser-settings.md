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
ms.date: 04/01/2021
ms.author: jswymer
ms.openlocfilehash: 90625ed6d5664efc9605aeacbc66d8174e55799d
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 03/31/2021
ms.locfileid: "5776302"
---
# <a name="setting-up-and-troubleshooting-your-browser-to-work-with-business-central-web-client"></a><span data-ttu-id="0b6d2-103">Configuración y solución de problemas de su navegador para que funcione con Business Central Web Client</span><span class="sxs-lookup"><span data-stu-id="0b6d2-103">Setting Up and Troubleshooting Your Browser to Work With Business Central Web Client</span></span>

<span data-ttu-id="0b6d2-104">Este artículo explica cómo configurar su navegador para que [!INCLUDE[web_client](includes/web_client.md)] y todas sus características funcionan correctamente.</span><span class="sxs-lookup"><span data-stu-id="0b6d2-104">This article explains how to set up your browser so that the [!INCLUDE[web_client](includes/web_client.md)] and all its features work properly.</span></span> <span data-ttu-id="0b6d2-105">Lea este artículo si tiene problemas para abrir [!INCLUDE[web_client](includes/web_client.md)], porque algunos problemas pueden deberse a la configuración de su navegador.</span><span class="sxs-lookup"><span data-stu-id="0b6d2-105">Read this article if you're having problems opening the [!INCLUDE[web_client](includes/web_client.md)], because some problems may be caused by your browser's settings.</span></span>

<span data-ttu-id="0b6d2-106">El artículo proporciona detalles para configurar Microsoft Edge, pero los requisitos para JavaScript, cookies y ventanas emergentes son los mismos para todos los navegadores compatibles.</span><span class="sxs-lookup"><span data-stu-id="0b6d2-106">The article provides details for setting up Microsoft Edge, but the requirements for JavaScript, cookies, and pop-ups are the same for all supported browsers.</span></span> <span data-ttu-id="0b6d2-107">Para otros navegadores, consulte las instrucciones proporcionadas por el fabricante.</span><span class="sxs-lookup"><span data-stu-id="0b6d2-107">For other browsers, refer to the instructions provided by the manufacturer.</span></span>  

## <a name="use-a-supported-browser"></a><span data-ttu-id="0b6d2-108">Usar un explorador admitido</span><span class="sxs-lookup"><span data-stu-id="0b6d2-108">Use a supported browser</span></span>

<span data-ttu-id="0b6d2-109">Asegúrese de utilizar uno de los navegadores compatibles.</span><span class="sxs-lookup"><span data-stu-id="0b6d2-109">Make sure to use a one of the supported browsers.</span></span> <span data-ttu-id="0b6d2-110">Consulte [Requisitos mínimos para usar Business Central](product-requirements.md#browsers).</span><span class="sxs-lookup"><span data-stu-id="0b6d2-110">See [Minimum Requirements for Using Business Central](product-requirements.md#browsers).</span></span>  

## <a name="allow-javascript-from-business-central"></a><span data-ttu-id="0b6d2-111">Permitir JavaScript desde Business Central</span><span class="sxs-lookup"><span data-stu-id="0b6d2-111">Allow JavaScript from Business Central</span></span>

<span data-ttu-id="0b6d2-112">*Problema:*</span><span class="sxs-lookup"><span data-stu-id="0b6d2-112">*Problem:*</span></span>

<span data-ttu-id="0b6d2-113">Si el navegador no permite JavaScript, verá **JavaScript no compatible/desactivado** en la barra de direcciones y un mensaje **Error HTTP 404.0: no encontrado** cuando intente abrir [!INCLUDE[prod_short](includes/prod_short.md)] y</span><span class="sxs-lookup"><span data-stu-id="0b6d2-113">If the browser doesn't allow JavaScript, you'll see **NotSupported/DisabledJavaScript** in the address bar and an **HTTP Error 404.0 - Not Found** message when you try to open [!INCLUDE[prod_short](includes/prod_short.md)], and the</span></span> 

<!-- http://localhost:8080/NotSupported/DisabledJavaScript HTTP Error 404.0 - Not Found
The resource you are looking for has been removed, had its name changed, or is temporarily unavailable. -->

<span data-ttu-id="0b6d2-114">*Reparar:*</span><span class="sxs-lookup"><span data-stu-id="0b6d2-114">*Fix:*</span></span>

1. <span data-ttu-id="0b6d2-115">En Microsoft Edge, vaya a **Configuraciones** > **Cookies y permisos del sitio** > **JavaScript**.</span><span class="sxs-lookup"><span data-stu-id="0b6d2-115">In Microsoft Edge, go to **Settings** > **Cookies and site permissions** > **JavaScript**.</span></span>
2. <span data-ttu-id="0b6d2-116">Realice una de los siguientes pasos.</span><span class="sxs-lookup"><span data-stu-id="0b6d2-116">Do one of the following steps.</span></span> <span data-ttu-id="0b6d2-117">Elija el paso recomendado por su organización:</span><span class="sxs-lookup"><span data-stu-id="0b6d2-117">Choose the step that is recommended by your organization:</span></span>

    - <span data-ttu-id="0b6d2-118">Mueva el control de alternancia **Permitido** a la izquierda (Desactivado).</span><span class="sxs-lookup"><span data-stu-id="0b6d2-118">Move the **Allowed** toggle to the left (Off).</span></span> <span data-ttu-id="0b6d2-119">Luego, seleccione **Añadir** y escriba la dirección (URL) para [!INCLUDE[prod_short](includes/prod_short.md)] en el cuadro **Sitio**.</span><span class="sxs-lookup"><span data-stu-id="0b6d2-119">Then, select **Add** and type the address (URL) for [!INCLUDE[prod_short](includes/prod_short.md)] in the **Site** box.</span></span> <span data-ttu-id="0b6d2-120">Seleccione **Añadir** cuando termine.</span><span class="sxs-lookup"><span data-stu-id="0b6d2-120">Select **Add** when done.</span></span>
    - <span data-ttu-id="0b6d2-121">Mueva el control de alternancia **Permitido** a la derecha (Activado).</span><span class="sxs-lookup"><span data-stu-id="0b6d2-121">Move the **Allowed** toggle to the right (On).</span></span>

## <a name="allow-cookies-from-business-central"></a><span data-ttu-id="0b6d2-122">Permitir cookies desde Business Central</span><span class="sxs-lookup"><span data-stu-id="0b6d2-122">Allow cookies from Business Central</span></span>

<span data-ttu-id="0b6d2-123">*Problema:*</span><span class="sxs-lookup"><span data-stu-id="0b6d2-123">*Problem:*</span></span>

<span data-ttu-id="0b6d2-124">Si el navegador no permite cookies, obtendrá el siguiente error:</span><span class="sxs-lookup"><span data-stu-id="0b6d2-124">If the browser doesn't allow cookies, you'll get the following error:</span></span>

<span data-ttu-id="0b6d2-125">**Lo siento, no se pudo encontrar la página. Compruebe la dirección e inténtelo de nuevo.**</span><span class="sxs-lookup"><span data-stu-id="0b6d2-125">**Sorry, the page could not be found. Please check the address and try again.**</span></span> 

<span data-ttu-id="0b6d2-126">*Reparar:*</span><span class="sxs-lookup"><span data-stu-id="0b6d2-126">*Fix:*</span></span>

1. <span data-ttu-id="0b6d2-127">En Microsoft Edge, vaya a **Configuraciones** > **Cookies y permisos del sitio** > **Cookies y datos del sitio**.</span><span class="sxs-lookup"><span data-stu-id="0b6d2-127">In Microsoft Edge, go to **Settings** > **Cookies and site permissions** > **Cookies and site data**.</span></span>
2. <span data-ttu-id="0b6d2-128">Mueva el control de alternancia **Permitir que los sitios guarden y lean datos de cookies** a la derecha (activado).</span><span class="sxs-lookup"><span data-stu-id="0b6d2-128">Move the **Allow sites to save and read cookie data** toggle to the right (On).</span></span>  

## <a name="allow-pop-ups-from-business-central"></a><a name="popup"></a><span data-ttu-id="0b6d2-129">Permitir ventanas emergentes desde Business Central</span><span class="sxs-lookup"><span data-stu-id="0b6d2-129">Allow pop-ups from Business Central</span></span>

[!INCLUDE[prod_short](includes/prod_short.md)] <span data-ttu-id="0b6d2-130">se integra con varios productos.</span><span class="sxs-lookup"><span data-stu-id="0b6d2-130">integrates with several products.</span></span> <span data-ttu-id="0b6d2-131">En algunos casos, como con Microsoft Teams, [!INCLUDE[prod_short](includes/prod_short.md)] se abre, o emerge, dentro del producto.</span><span class="sxs-lookup"><span data-stu-id="0b6d2-131">In some cases, like with Microsoft Teams, [!INCLUDE[prod_short](includes/prod_short.md)] opens, or "pop-ups", within the product.</span></span> <span data-ttu-id="0b6d2-132">Esta capacidad requiere que su navegador permita ventanas emergentes de [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="0b6d2-132">This capability requires that your browser allows pop-ups from [!INCLUDE[prod_short](includes/prod_short.md)].</span></span>

<span data-ttu-id="0b6d2-133">*Problema:*</span><span class="sxs-lookup"><span data-stu-id="0b6d2-133">*Problem:*</span></span>

<span data-ttu-id="0b6d2-134">Si las ventanas emergentes para [!INCLUDE[prod_short](includes/prod_short.md)] están bloqueadas, recibe un mensaje similar al siguiente:</span><span class="sxs-lookup"><span data-stu-id="0b6d2-134">If pop-ups for [!INCLUDE[prod_short](includes/prod_short.md)] are being blocked, you get a message similar to the following message:</span></span>

<span data-ttu-id="0b6d2-135">**Algo salió mal. Es posible que su navegador esté bloqueando las ventanas emergentes que necesita Business Central.**</span><span class="sxs-lookup"><span data-stu-id="0b6d2-135">**Something went wrong. Your browser may be blocking pop-ups needed by Business Central.**</span></span>

<!--
Something went wrong
Your browser may be blocking pop-ups needed by Business Central.

Change your browser settings to allow pop-ups or allow this for trusted domains, then try again.
If these settings are managed for your organization, you should contact your administrator for assistance.

Try again
-->
<span data-ttu-id="0b6d2-136">*Reparar:*</span><span class="sxs-lookup"><span data-stu-id="0b6d2-136">*Fix:*</span></span>

1. <span data-ttu-id="0b6d2-137">En Microsoft Edge, vaya a **Configuraciones** > **Cookies y permisos del sitio** > **Ventanas emergentes y redireccionamientos**.</span><span class="sxs-lookup"><span data-stu-id="0b6d2-137">In Microsoft Edge, go to **Settings** > **Cookies and site permissions** > **Pop-ups and redirects**.</span></span>
2. <span data-ttu-id="0b6d2-138">Mueva el control de alternancia **Bloqueado** a la derecha (Activado).</span><span class="sxs-lookup"><span data-stu-id="0b6d2-138">Move the **Blocked** toggle to the right (On).</span></span>
3. <span data-ttu-id="0b6d2-139">Seleccione **Añadir**.</span><span class="sxs-lookup"><span data-stu-id="0b6d2-139">Select **Add**.</span></span> <span data-ttu-id="0b6d2-140">En el cuadro **Sitio**, escriba `https://businesscentral.dynamics.com`, luego seleccione **Añadir**.</span><span class="sxs-lookup"><span data-stu-id="0b6d2-140">In the **Site** box, type `https://businesscentral.dynamics.com`, then select **Add**.</span></span>

## <a name="see-also"></a><span data-ttu-id="0b6d2-141">Consulte también</span><span class="sxs-lookup"><span data-stu-id="0b6d2-141">See Also</span></span>

[<span data-ttu-id="0b6d2-142">Consejos para la solución de problemas de Teams</span><span class="sxs-lookup"><span data-stu-id="0b6d2-142">Troubleshooting Teams</span></span>](admin-teams-troubleshooting.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]