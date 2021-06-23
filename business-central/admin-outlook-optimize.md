---
title: Optimizar Otulook para la bandeja de entrada de empresa
description: Obtenga información sobre las cosas que puede hacer para mejorar la experiencia con la bandeja de entrada de empresa en Microsoft Outlook.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Outlook, Microsoft 365, inbox, business inbox, WebView2, Edge, addin, add-in
ms.date: 05/12/2021
ms.author: jswymer
ms.openlocfilehash: 2fee1782057d0f45319e4d12d715c2e1e0d3d4a6
ms.sourcegitcommit: 61e279b253370cdf87b7bc1ee0f927e4f0521344
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 05/19/2021
ms.locfileid: "6064861"
---
# <a name="optimizing-outlook-for-your-business-inbox"></a><span data-ttu-id="20a70-103">Optimizar Otulook para la bandeja de entrada de empresa</span><span class="sxs-lookup"><span data-stu-id="20a70-103">Optimizing Outlook for Your Business Inbox</span></span> 

<span data-ttu-id="20a70-104">Este artículo analiza las cosas que puede hacer para obtener la mejor experiencia posible con la bandeja de entrada de empresa en Microsoft Outlook.</span><span class="sxs-lookup"><span data-stu-id="20a70-104">This article discusses things you can do to get the best possible experience with the Business Inbox in Microsoft Outlook.</span></span> 

## <a name="update-outlook"></a><span data-ttu-id="20a70-105">Actualizar Outlook</span><span class="sxs-lookup"><span data-stu-id="20a70-105">Update Outlook</span></span>

<span data-ttu-id="20a70-106">Actualice a la versión 2012 de Outlook o la más reciente.</span><span class="sxs-lookup"><span data-stu-id="20a70-106">Update to Outlook version 2012 or newer.</span></span>

> [!NOTE]
> <span data-ttu-id="20a70-107">Si no puede actualizar Outlook a la versión 2012 o posterior, asegúrese de actualizar al menos a la versión 1905.</span><span class="sxs-lookup"><span data-stu-id="20a70-107">If you are unable to update Outlook to version 2012 or later, make sure that you at least update to version 1905.</span></span> <span data-ttu-id="20a70-108">Esto evita que el complemento de Outlook se ejecute utilizando componentes heredados de Internet Explorer</span><span class="sxs-lookup"><span data-stu-id="20a70-108">This prevents the Outlook Add-in from running using legacy Internet Explorer components</span></span>

### <a name="how-to-check-your-version-of-outlook"></a><span data-ttu-id="20a70-109">Cómo verificar su versión de Outlook</span><span class="sxs-lookup"><span data-stu-id="20a70-109">How to check your version of Outlook</span></span>

<span data-ttu-id="20a70-110">Si utiliza Office 2019 o Microsoft 365, siga esta guía de soporte de Microsoft para verificar qué versión de Outlook tiene:</span><span class="sxs-lookup"><span data-stu-id="20a70-110">Whether you use Office 2019 or Microsoft 365, follow this Microsoft Support guide to check which version of Outlook you have:</span></span>  

[<span data-ttu-id="20a70-111">Acerca de Office: ¿Qué versión de Office estoy usando?</span><span class="sxs-lookup"><span data-stu-id="20a70-111">About Office: What version of Office am I using?</span></span>](https://support.microsoft.com/office/about-office-what-version-of-office-am-i-using-932788b8-a3ce-44bf-bb09-e334518b8b19)

### <a name="how-to-update-outlook"></a><span data-ttu-id="20a70-112">Cómo actualizar Outlook</span><span class="sxs-lookup"><span data-stu-id="20a70-112">How to update Outlook</span></span>

<span data-ttu-id="20a70-113">Para actualizar Outlook a la última versión, siga esta guía de soporte de Microsoft o comuníquese con su administrador:</span><span class="sxs-lookup"><span data-stu-id="20a70-113">To update Outlook to the latest version, follow this Microsoft Support guide or contact your administrator:</span></span>

[<span data-ttu-id="20a70-114">Instalar actualizaciones de Office</span><span class="sxs-lookup"><span data-stu-id="20a70-114">Install Office updates</span></span>](https://support.microsoft.com/office/install-office-updates-2ab296f3-7f03-43a2-8e50-46de917611c5)

## <a name="install-microsoft-edge-webview2"></a><span data-ttu-id="20a70-115">Instalar Microsoft Edge WebView2</span><span class="sxs-lookup"><span data-stu-id="20a70-115">Install Microsoft Edge WebView2</span></span>

<span data-ttu-id="20a70-116">Asegúrese de que Microsoft Edge WebView2 está instalado en su dispositivo.</span><span class="sxs-lookup"><span data-stu-id="20a70-116">Ensure that Microsoft Edge WebView2 is installed on your device.</span></span>

### <a name="how-to-check-if-microsoft-edge-webview2-is-installed"></a><span data-ttu-id="20a70-117">Cómo comprobar si Microsoft Edge WebView2 está instalado</span><span class="sxs-lookup"><span data-stu-id="20a70-117">How to check if Microsoft Edge WebView2 is installed</span></span> 

<span data-ttu-id="20a70-118">Para comprobar si Microsoft Edge WebView2 está instalado en un ordenador, siga los siguientes pasos:</span><span class="sxs-lookup"><span data-stu-id="20a70-118">To check if you have Microsoft Edge WebView2 installed on a computer, do the following steps:</span></span>

<span data-ttu-id="20a70-119">Desde el menú Inicio:</span><span class="sxs-lookup"><span data-stu-id="20a70-119">From Start menu:</span></span>

1. <span data-ttu-id="20a70-120">Seleccione **Inicio** ![Inicio de Windows](media/windows-start-icon.png "Icono de inicio de Windows") > **Ajustes** ![Configuración de Windows](media/windows-settings-icon.png "Icono de configuración de Windows") > **Aplicaciones y funciones**.</span><span class="sxs-lookup"><span data-stu-id="20a70-120">Choose **Start** ![Windows Start](media/windows-start-icon.png "Windows Start icon") > **Settings** ![Windows Settings](media/windows-settings-icon.png "Windows Settings icon") > **Apps & Features**.</span></span>
2. <span data-ttu-id="20a70-121">En el cuadro de búsqueda, escriba **WebView2**.</span><span class="sxs-lookup"><span data-stu-id="20a70-121">In the search box, type **WebView2**.</span></span> <span data-ttu-id="20a70-122">Si Microsoft Edge WebView2 está instalado, verá una entrada llamada **Tiempo de ejecución de Microsoft Edge WebView2**.</span><span class="sxs-lookup"><span data-stu-id="20a70-122">If Microsoft Edge WebView2 is installed, you'll see an entry called **Microsoft Edge WebView2 Runtime**.</span></span>

<span data-ttu-id="20a70-123">Desde el Panel de control:</span><span class="sxs-lookup"><span data-stu-id="20a70-123">From Control Panel:</span></span>

1. <span data-ttu-id="20a70-124">En el cuadro de búsqueda junto a **Inicio** ![Inicio de Windows](media/windows-start-icon.png "Icono de inicio de Windows"), escriba **Panel de control** y luego seleccione el resultado.</span><span class="sxs-lookup"><span data-stu-id="20a70-124">In the search box next to **Start** ![Windows Start](media/windows-start-icon.png "Windows Start icon"), type **Control Panel**, and then select the result.</span></span>
2. <span data-ttu-id="20a70-125">Seleccione **Programas** > **Programas y características**.</span><span class="sxs-lookup"><span data-stu-id="20a70-125">Choose **Programs** > **Programs and Features**.</span></span>
3. <span data-ttu-id="20a70-126">En el cuadro de búsqueda, escriba **WebView2**.</span><span class="sxs-lookup"><span data-stu-id="20a70-126">In the search box, type **WebView2**.</span></span> <span data-ttu-id="20a70-127">Si Microsoft Edge WebView2 está instalado, verá una entrada llamada **Tiempo de ejecución de Microsoft Edge WebView2**.</span><span class="sxs-lookup"><span data-stu-id="20a70-127">If Microsoft Edge WebView2 is installed, you'll see an entry called **Microsoft Edge WebView2 Runtime**.</span></span>

### <a name="how-to-install-microsoft-edge-webview2"></a><span data-ttu-id="20a70-128">Cómo instalar Microsoft Edge WebView2</span><span class="sxs-lookup"><span data-stu-id="20a70-128">How to install Microsoft Edge WebView2</span></span> 

1. <span data-ttu-id="20a70-129">Utilice el navegador para ir a [https://developer.microsoft.com/microsoft-edge/webview2/](https://developer.microsoft.com/microsoft-edge/webview2/).</span><span class="sxs-lookup"><span data-stu-id="20a70-129">Using your browser, go to [https://developer.microsoft.com/microsoft-edge/webview2/](https://developer.microsoft.com/microsoft-edge/webview2/).</span></span>
2. <span data-ttu-id="20a70-130">Seleccione **Descargar**.</span><span class="sxs-lookup"><span data-stu-id="20a70-130">Choose **Download**.</span></span>
3. <span data-ttu-id="20a70-131">Establezca **Seleccionar arquitectura** para que coincida con su sistema.</span><span class="sxs-lookup"><span data-stu-id="20a70-131">Set **Select Architecture** to match your system.</span></span>
4. <span data-ttu-id="20a70-132">Seleccione **Descargar**.</span><span class="sxs-lookup"><span data-stu-id="20a70-132">Choose **Download**.</span></span>

> [!NOTE]
> <span data-ttu-id="20a70-133">Su organización puede tener restricciones sobre qué componentes se pueden instalar en su dispositivo.</span><span class="sxs-lookup"><span data-stu-id="20a70-133">Your organization may have restriction on which components can be installed on your device.</span></span> <span data-ttu-id="20a70-134">Póngase en contacto con su administrador para obtener ayuda.</span><span class="sxs-lookup"><span data-stu-id="20a70-134">Contact your administrator for assistance.</span></span>

## <a name="use-a-supported-browser"></a><span data-ttu-id="20a70-135">Usar un explorador admitido</span><span class="sxs-lookup"><span data-stu-id="20a70-135">Use a supported browser</span></span>

<span data-ttu-id="20a70-136">Considere la posibilidad de utilizar Outlook para la web en uno de los navegadores compatibles con Business Central.</span><span class="sxs-lookup"><span data-stu-id="20a70-136">Consider using Outlook for the Web in one of the browsers supported by Business Central.</span></span> <span data-ttu-id="20a70-137">Para obtener una lista de navegadores compatibles, consulte [Requisitos mínimos para utilizar Business Central](product-requirements.md#browsers).</span><span class="sxs-lookup"><span data-stu-id="20a70-137">For a list of supported browsers, see [Minimum Requirements for Using Business Central](product-requirements.md#browsers).</span></span>

## <a name="see-also"></a><span data-ttu-id="20a70-138">Consulte también</span><span class="sxs-lookup"><span data-stu-id="20a70-138">See Also</span></span>

[<span data-ttu-id="20a70-139">Preparación para hacer negocios</span><span class="sxs-lookup"><span data-stu-id="20a70-139">Getting Ready for Doing Business</span></span>](ui-get-ready-business.md)  
[<span data-ttu-id="20a70-140">Obtener Business Central en mi dispositivo móvil</span><span class="sxs-lookup"><span data-stu-id="20a70-140">Getting Business Central on my Mobile Device</span></span>](install-mobile-app.md)  
[<span data-ttu-id="20a70-141">Enviar documentos por correo electrónico</span><span class="sxs-lookup"><span data-stu-id="20a70-141">Send Documents by Email</span></span>](ui-how-send-documents-email.md)  
[<span data-ttu-id="20a70-142">Finanzas</span><span class="sxs-lookup"><span data-stu-id="20a70-142">Finance</span></span>](finance.md)  
[<span data-ttu-id="20a70-143">Ccial</span><span class="sxs-lookup"><span data-stu-id="20a70-143">Sales</span></span>](sales-manage-sales.md)  
[<span data-ttu-id="20a70-144">Compras</span><span class="sxs-lookup"><span data-stu-id="20a70-144">Purchasing</span></span>](purchasing-manage-purchasing.md)  
[<span data-ttu-id="20a70-145">Requisitos mínimos para Outlook</span><span class="sxs-lookup"><span data-stu-id="20a70-145">Minimum Requirements for Outlook</span></span>](product-requirements.md#outlook)  
[<span data-ttu-id="20a70-146">Usar complementos en Outlook en la web</span><span class="sxs-lookup"><span data-stu-id="20a70-146">Using add-ins in Outlook on the web</span></span>](https://support.office.com/article/Using-Add-ins-in-Outlook-on-the-web-8f2ce816-5df4-44a5-958c-f7f9d6dabdce?appver=OWB150)  


[!INCLUDE[footer-include](includes/footer-banner.md)]