---
title: Instalar extensiones para personalizar Business Central | Documentos de Microsoft
description: Obtenga información sobre cómo agregar funcionalidad y personalizar Business Central mediante la instalación de extensiones.
documentationcenter: ''
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: app, add-in, manifest, customize
ms.date: 08/12/2020
ms.author: edupont
ms.openlocfilehash: 2011728e8e036442418c6a2d8b51477b45b02d1e
ms.sourcegitcommit: 43284728c34b72ad1984a516273dc80e4cdc99ab
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 09/04/2020
ms.locfileid: "3765926"
---
# <a name="customizing-business-central-using-extensions"></a><span data-ttu-id="47e84-103">Personalizar Business Central con extensiones</span><span class="sxs-lookup"><span data-stu-id="47e84-103">Customizing Business Central Using Extensions</span></span>

<span data-ttu-id="47e84-104">Puede cambiar [!INCLUDE[d365fin](includes/d365fin_md.md)] instalando extensiones que agregan funciones, cambian el comportamiento o proporcionan acceso a nuevos servicios en línea, por ejemplo.</span><span class="sxs-lookup"><span data-stu-id="47e84-104">You can change [!INCLUDE[d365fin](includes/d365fin_md.md)] by installing extensions that add functionality, changes behavior, or gives you access to new online services, for example.</span></span>

> [!NOTE]
> <span data-ttu-id="47e84-105">Para instalar extensiones desde AppSource o añadir extensiones por suscriptor, debe tener los permisos adecuados.</span><span class="sxs-lookup"><span data-stu-id="47e84-105">To install extensions from AppSource or add per-tenant extensions, you must have the right permissions.</span></span> <span data-ttu-id="47e84-106">Debe ser miembro del grupo de usuarios ADMIN EXTENSIÓN D365 o debe tener el conjunto de permisos de ADMIN EXTENSIÓN D365.</span><span class="sxs-lookup"><span data-stu-id="47e84-106">You must either be a member of the D365 EXTENSION MGMT user group or you must have the D365 EXTENSION MGMT permission set.</span></span> <span data-ttu-id="47e84-107">Si es administrador, puede asignar grupos de usuarios y permisos a otros usuarios de su empresa.</span><span class="sxs-lookup"><span data-stu-id="47e84-107">If you are an administrator, you can assign user groups and permissions to other users in your company.</span></span><br /><br />
<span data-ttu-id="47e84-108">Para utilizar la funcionalidad que proporciona una extensión, como abrir páginas, ejecutar informes, seleccionar acciones, etc., se le deben asignar los conjuntos de permisos que se instalan como parte de la extensión.</span><span class="sxs-lookup"><span data-stu-id="47e84-108">To use the functionality that is provided by an extension, such as opening pages, running reports, selecting actions, and so on, you must be assigned the permission sets that are installed as part of the extension.</span></span>

> [!IMPORTANT]  
> <span data-ttu-id="47e84-109">No se admite la carga de extensiones por inquilino y la instalación de extensiones de AppSource a través de la página **Administración de extensiones** para instalaciones locales.</span><span class="sxs-lookup"><span data-stu-id="47e84-109">The upload of per-tenant extensions and the installation of AppSource extensions is not supported through the **Extension Management** page for on-premise installations.</span></span>

<span data-ttu-id="47e84-110">Cuando inicia [!INCLUDE[d365fin](includes/d365fin_md.md)] por primera vez, ya están instaladas algunas extensiones.</span><span class="sxs-lookup"><span data-stu-id="47e84-110">When you first launch [!INCLUDE[d365fin](includes/d365fin_md.md)], some extensions are already installed for you.</span></span> <span data-ttu-id="47e84-111">Con el tiempo, tendrá disponibles más extensiones y puede elegir si desea usar la extensión o no.</span><span class="sxs-lookup"><span data-stu-id="47e84-111">Over time, more extensions will be made available to you, and you can then choose if you want to use the extension or not.</span></span>

<span data-ttu-id="47e84-112">Por ejemplo, Microsoft ofrece una extensión que proporciona integración con PayPal Payments Standard.</span><span class="sxs-lookup"><span data-stu-id="47e84-112">For example, Microsoft provides an extension that provides integration with PayPal Payments Standard.</span></span> <span data-ttu-id="47e84-113">Esta extensión se instala por omisión.</span><span class="sxs-lookup"><span data-stu-id="47e84-113">This extension is installed by default.</span></span>
<span data-ttu-id="47e84-114">Pero si está disponible otra extensión que ofrece integración con otro servicio de pago, puede instalar la nueva extensión y seleccionar cuál de los dos servicios quiere usar.</span><span class="sxs-lookup"><span data-stu-id="47e84-114">But if another extension is made available that offers integration with another payment service, you can install the new extension and then choose which of the two services to use.</span></span>  

<span data-ttu-id="47e84-115">Puede administrar las extensiones en la página **Administración de extensiones**.</span><span class="sxs-lookup"><span data-stu-id="47e84-115">You manage the extensions on the **Extension Management** page.</span></span> <span data-ttu-id="47e84-116">Puede acceder a esta página desde Inicio.</span><span class="sxs-lookup"><span data-stu-id="47e84-116">You can access this page from Home.</span></span> <span data-ttu-id="47e84-117">De forma alternativa, seleccione el icono **Buscar página o informe** ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer") en la esquina superior derecha, escriba **Extensión** y, a continuación, seleccione el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="47e84-117">Alternatively, choose the **Search for Page or Report** icon ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") in the top right corner, enter **Extension**, and then choose the related link.</span></span> <span data-ttu-id="47e84-118">Para más información, ver [Instalación y desinstalación de extensiones](ui-extensions-install-uninstall.md).</span><span class="sxs-lookup"><span data-stu-id="47e84-118">For more information, see [Installing and Uninstalling Extensions](ui-extensions-install-uninstall.md).</span></span>

> [!NOTE]  
> <span data-ttu-id="47e84-119">Si cree que debería tener acceso a una extensión pero no encuentra la funcionalidad, consulte la página **Administración de extensiones**; si la extensión no aparece, puede instalarla tal como se describe en la sección siguiente.</span><span class="sxs-lookup"><span data-stu-id="47e84-119">If you think you should have access to an extension but you cannot find its functionality, check the **Extension Management** page - if the extension is not listed there, you can install it as described in the following section.</span></span>  

> [!NOTE]  
> <span data-ttu-id="47e84-120">Las nuevas extensiones no están disponibles en AppSource inmediatamente después anunciar una actualización.</span><span class="sxs-lookup"><span data-stu-id="47e84-120">New extensions are not available in AppSource immediately after we announce an update.</span></span> <span data-ttu-id="47e84-121">Puede estar atento a las extensiones en [AppSource.microsoft.com](https://go.microsoft.com/fwlink/?linkid=2081646).</span><span class="sxs-lookup"><span data-stu-id="47e84-121">You can keep an eye out for the extensions at  [AppSource.microsoft.com](https://go.microsoft.com/fwlink/?linkid=2081646).</span></span>

## <a name="see-also"></a><span data-ttu-id="47e84-122">Consulte también</span><span class="sxs-lookup"><span data-stu-id="47e84-122">See Also</span></span>

[<span data-ttu-id="47e84-123">Ampliación de Dynamics 365 Business Central</span><span class="sxs-lookup"><span data-stu-id="47e84-123">Extending Dynamics 365 Business Central</span></span>](about-develop-extensions.md)  
[<span data-ttu-id="47e84-124">Extensiones de Business Central de otros proveedores</span><span class="sxs-lookup"><span data-stu-id="47e84-124">Business Central Extensions by Other Providers</span></span>](ui-extensions-other.md)  
[<span data-ttu-id="47e84-125">Configurar el servicio Envestnet Yodlee Bank Feeds</span><span class="sxs-lookup"><span data-stu-id="47e84-125">Set Up the Envestnet Yodlee Bank Feeds Service</span></span>](bank-how-setup-bank-statement-service.md)  
[<span data-ttu-id="47e84-126">Permitir el pago de clientes mediante PayPal</span><span class="sxs-lookup"><span data-stu-id="47e84-126">Enable Customer Payment Through PayPal</span></span>](sales-how-enable-payment-service-extensions.md)  
[<span data-ttu-id="47e84-127">Migrar datos de empresa de otros sistemas financieros</span><span class="sxs-lookup"><span data-stu-id="47e84-127">Migrating Business Data from Other Finance Systems</span></span>](across-import-data-configuration-packages.md)  
[<span data-ttu-id="47e84-128">Configurar la extensión Códigos postales de Reino Unido de GetAddress.io</span><span class="sxs-lookup"><span data-stu-id="47e84-128">Setting Up the GetAddress.io UK Postal Code extension</span></span>](LocalFunctionality/UnitedKingdom/uk-setup-postal-code-service.md)  
<span data-ttu-id="47e84-129">[[!INCLUDE[d365fin](includes/d365fin_md.md)] Extensiones de otros proveedores](ui-extensions-other.md)</span><span class="sxs-lookup"><span data-stu-id="47e84-129">[[!INCLUDE[d365fin](includes/d365fin_md.md)] Extensions by Other Providers](ui-extensions-other.md)</span></span>  
[<span data-ttu-id="47e84-130">Introducción</span><span class="sxs-lookup"><span data-stu-id="47e84-130">Getting Started</span></span>](product-get-started.md)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
