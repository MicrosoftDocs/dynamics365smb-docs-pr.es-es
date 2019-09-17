---
title: Administrar la personalización como administrador en Business Central | Documentos de Microsoft
description: Aprenda a personalizar la interfaz de usuario para que se adapte a su forma de trabajar.
services: project-madeira
documentationcenter: ''
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customize, personalize, personalization, hide columns, remove fields, move fields
ms.date: 08/16/2019
ms.author: jswymer
ms.openlocfilehash: 268d61e05f84643abe8eeeb283bd035e0247fe1c
ms.sourcegitcommit: 81b6062194bf04d8052a3cd394cc0b41e3f53e6d
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2019
ms.locfileid: "1887742"
---
# <a name="managing-personalization-as-an-administrator"></a><span data-ttu-id="79e11-103">Administrar la personalización como administrador</span><span class="sxs-lookup"><span data-stu-id="79e11-103">Managing Personalization as an Administrator</span></span>

<span data-ttu-id="79e11-104"> Los usuarios pueden personalizar el área de trabajo para que se adapte a sus preferencias.</span><span class="sxs-lookup"><span data-stu-id="79e11-104">Users can personalize their workspace to suit their own preferences.</span></span> <span data-ttu-id="79e11-105">Como administrador, controla y gestiona la personalización por medio de:</span><span class="sxs-lookup"><span data-stu-id="79e11-105">As an administrator, you control and manage personalization by:</span></span>

-   <span data-ttu-id="79e11-106">Habilitación o deshabilitación de la función de personalización para toda la aplicación (solo para la instalación local).</span><span class="sxs-lookup"><span data-stu-id="79e11-106">Enabling or disabling the personalization feature for the entire the application (on-premises installation only).</span></span>
-   <span data-ttu-id="79e11-107">Habilitación o deshabilitación de la función de personalización para los usuarios de un perfil específico.</span><span class="sxs-lookup"><span data-stu-id="79e11-107">Enabling or disabling the personalization feature for users of a specific profile.</span></span>
-   <span data-ttu-id="79e11-108">Borrado de cualquier personalización de página que los usuarios hayan realizado.</span><span class="sxs-lookup"><span data-stu-id="79e11-108">Clearing any page personalizations that users have made.</span></span>

## <a name="EnablePersonalization"></a><span data-ttu-id="79e11-109">Para habilitar o deshabilitar la personalización (solo local)</span><span class="sxs-lookup"><span data-stu-id="79e11-109">To enable or disable personalization (On-Premises Only)</span></span>

<span data-ttu-id="79e11-110">De forma predeterminada, la personalización no está habilitada en el cliente.</span><span class="sxs-lookup"><span data-stu-id="79e11-110">By default, personalization is not enabled in the client.</span></span> <span data-ttu-id="79e11-111">Puede habilitar o deshabilitar la personalización modificando el archivo de configuración (navsettings.json) de la instancia del servidor web de Business Central que sirve a los clientes.</span><span class="sxs-lookup"><span data-stu-id="79e11-111">You enable or disable personalization by modifying the configuration file (navsettings.json) of the Business Central Web Server instance that serves the clients.</span></span>

1. <span data-ttu-id="79e11-112">Para habilitar la personalización, agregue la siguiente línea al archivo navsettings.json:</span><span class="sxs-lookup"><span data-stu-id="79e11-112">To enable personalization, add the following line in the navsettings.json file:</span></span>

    ```
    "PersonalizationEnabled": "true"
    ```

    <span data-ttu-id="79e11-113">Para deshabilitar la personalización, quite esta línea o cámbiela por:</span><span class="sxs-lookup"><span data-stu-id="79e11-113">To disable personalization, remove this line or change it to:</span></span>

    ```
    "PersonalizationEnabled": "false"
    ```

    <span data-ttu-id="79e11-114">Para obtener más información sobre cómo modificar el archivo navsettings.json, consulte [Modificar el archivo navsettings.json directamente](https://docs.microsoft.com/en-us/dynamics365/business-central/dev-itpro/administration/configure-web-server?branch=master#Settings).</span><span class="sxs-lookup"><span data-stu-id="79e11-114">For more information about how to modify the navsettings.json file, see [Modify the navsettings.json file directly](https://docs.microsoft.com/en-us/dynamics365/business-central/dev-itpro/administration/configure-web-server?branch=master#Settings).</span></span>

2. <span data-ttu-id="79e11-115">Genere y descargue los símbolos de aplicación.</span><span class="sxs-lookup"><span data-stu-id="79e11-115">Generate and download the application symbols.</span></span>

    <span data-ttu-id="79e11-116">Este paso es opcional y no es necesario para habilitar la personalización.</span><span class="sxs-lookup"><span data-stu-id="79e11-116">This step is optional, and not required to enable personalization.</span></span> <span data-ttu-id="79e11-117">Sin embargo, garantiza que las nuevas páginas creadas por los desarrolladores puedan personalizarse.</span><span class="sxs-lookup"><span data-stu-id="79e11-117">However, it ensures that new pages that are created by developers can be personalized.</span></span>

    1. <span data-ttu-id="79e11-118">Primero, genere los símbolos ejecutando finsql.exe con un comando `generatesymbolreference`.</span><span class="sxs-lookup"><span data-stu-id="79e11-118">First, you generate the symbols by running finsql.exe with `generatesymbolreference` command.</span></span> <span data-ttu-id="79e11-119">El archivo finsql.exe se encuentra en la carpeta de instalación para [!INCLUDE[server](includes/server.md)] y el entorno de desarrollo de Dynamics NAV (CSIDE).</span><span class="sxs-lookup"><span data-stu-id="79e11-119">The finsql.exe file is located in the installation folder for the [!INCLUDE[server](includes/server.md)] and Dynamics NAV Development Environment (CSIDE).</span></span> <span data-ttu-id="79e11-120">Para generar los símbolos, abra un símbolo del sistema, cambie al directorio donde está almacenado el archivo y ejecute el siguiente comando:</span><span class="sxs-lookup"><span data-stu-id="79e11-120">To generate the symbols, open a command prompt, change to the directory where the file is store, and the run the following command:</span></span>

        ```
        finsql.exe Command=generatesymbolreference, Database="<Database Name>", ServerName=<SQL Server Name\<Server Instance>
        ```
    <span data-ttu-id="79e11-121">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="79e11-121">For example:</span></span>

        ```
        finsql.exe Command=generatesymbolreference, Database="Demo Database BC", ServerName=MySQLServer\BCDEMO
        ```

    <span data-ttu-id="79e11-122">Para obtener más información, consulte [Ejecución de C/SIDE y AL en paralelo](https://docs.microsoft.com/en-us/dynamics365/business-central/dev-itpro/developer/devenv-running-cside-and-al-side-by-side).</span><span class="sxs-lookup"><span data-stu-id="79e11-122">For more information, see [Running C/SIDE and AL Side-by-Side](https://docs.microsoft.com/en-us/dynamics365/business-central/dev-itpro/developer/devenv-running-cside-and-al-side-by-side).</span></span>

    2. <span data-ttu-id="79e11-123">Configure la instancia de [!INCLUDE[nav_server_md](includes/nav_server_md.md)] en **Habilitar las referencias de los símbolos de la aplicación al iniciar el servidor** (EnableSymbolLoadingAtServerStartup).</span><span class="sxs-lookup"><span data-stu-id="79e11-123">Configure [!INCLUDE[nav_server_md](includes/nav_server_md.md)] instance to **Enable loading application symbol references at server startup** (EnableSymbolLoadingAtServerStartup).</span></span> <span data-ttu-id="79e11-124">Para obtener más información, consulte [Configuración de Business Central Server](https://docs.microsoft.com/en-us/dynamics365/business-central/dev-itpro/administration/configure-server-instance#development-settings).</span><span class="sxs-lookup"><span data-stu-id="79e11-124">For more information, see [Configuring Business Central Server](https://docs.microsoft.com/en-us/dynamics365/business-central/dev-itpro/administration/configure-server-instance#development-settings).</span></span>

## <a name="to-disable-personalization-for-a-profile"></a><span data-ttu-id="79e11-125">Para deshabilitar la personalización de un perfil</span><span class="sxs-lookup"><span data-stu-id="79e11-125">To disable personalization for a profile</span></span>

<span data-ttu-id="79e11-126">Puede evitar que todos los usuarios que pertenecen a un perfil específico puedan personalizar sus páginas.</span><span class="sxs-lookup"><span data-stu-id="79e11-126">You can prevent all users that belong to a specific profile from being able to personalize their pages.</span></span>

1. <span data-ttu-id="79e11-127">Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Perfiles** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="79e11-127">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Profiles**, and then choose the related link.</span></span>
2. <span data-ttu-id="79e11-128">Seleccione el perfil de la lista que desea modificar.</span><span class="sxs-lookup"><span data-stu-id="79e11-128">Select the profile in the list that you want to modify.</span></span>
3. <span data-ttu-id="79e11-129">Seleccione la casilla **Deshabilitar personalización** y, a continuación, seleccione el botón **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="79e11-129">Select the **Disable personalization** check box, and then choose the **OK** button.</span></span>

> [!NOTE]  
> <span data-ttu-id="79e11-130">En Business Central en línea, solo puede deshabilitar la personalización para un perfil de suscriptor, no para los perfiles del sistema.</span><span class="sxs-lookup"><span data-stu-id="79e11-130">In Business Central online, you can only disable personalization for a tenant profile, not for system profiles.</span></span> 

## <a name="to-clear-user-personalizations"></a><span data-ttu-id="79e11-131">Para borrar personalizaciones de usuarios</span><span class="sxs-lookup"><span data-stu-id="79e11-131">To clear user personalizations</span></span>

<span data-ttu-id="79e11-132">Al borrar la personalización de la página, la página vuelve a su diseño original antes de realizar cualquier personalización.</span><span class="sxs-lookup"><span data-stu-id="79e11-132">Clearing page personalization changes the page back to its original layout before any personalization was made.</span></span> <span data-ttu-id="79e11-133">Existen dos formas de borrar las personalizaciones que los usuarios han realizado en las páginas: usando la página **Eliminar personalización usuario** o la página **Tarjeta personalización usuario**.</span><span class="sxs-lookup"><span data-stu-id="79e11-133">There are two ways to clear the personalizations that users have made to pages: using the **Delete User Personalization** page and using the **User Personalization Card** page.</span></span>

### <a name="to-clear-user-personalizations-by-using-the-delete-user-personalization-page"></a><span data-ttu-id="79e11-134">Para borrar las personalizaciones de los usuarios con la página Eliminar personalización de usuarios.</span><span class="sxs-lookup"><span data-stu-id="79e11-134">To clear user personalizations by using the Delete User Personalization page</span></span>

<span data-ttu-id="79e11-135">La página **Eliminar personalización de usuarios** le permite borrar la personalización por página y por usuario.</span><span class="sxs-lookup"><span data-stu-id="79e11-135">The **Delete User Personalization** page enables you to clear personalizations on a per-page basis for each user individually.</span></span>

1. <span data-ttu-id="79e11-136">Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Eliminar personalización usuario** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="79e11-136">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Delete User Personalization**, and then choose the related link.</span></span>

    <span data-ttu-id="79e11-137">La página enumera todas las páginas que se han personalizado y el usuario al que pertenece.</span><span class="sxs-lookup"><span data-stu-id="79e11-137">The page lists all the pages that have been personalized and the user it belongs to.</span></span>

    >[!NOTE]
    > <span data-ttu-id="79e11-138">Una marca de verificación en las columnas **Personalización heredada** indica que la personalización se realizó en una versión anterior de [!INCLUDE[d365fin](includes/d365fin_md.md)] que manejaba la personalización de forma diferente a como lo hace ahora.</span><span class="sxs-lookup"><span data-stu-id="79e11-138">A check mark in the **Legacy Personalization** columns indicates that the personalization was done in an older version of [!INCLUDE[d365fin](includes/d365fin_md.md)], which handled personalization different than it does now.</span></span> <span data-ttu-id="79e11-139">Los usuarios que intentan personalizar estas páginas se bloquean a menos que elijan desbloquear la página.</span><span class="sxs-lookup"><span data-stu-id="79e11-139">Users who try to personalize these pages are locked from doing so unless they choose to unlock the page.</span></span> <span data-ttu-id="79e11-140">Para obtener más información, consulte [Por qué la página está bloqueada para la personalización](ui-personalization-locked.md).</span><span class="sxs-lookup"><span data-stu-id="79e11-140">For more information, see [Why a page is locked from personalizing](ui-personalization-locked.md).</span></span>

2. <span data-ttu-id="79e11-141">Seleccione el movimiento que desea eliminar y, después, seleccione **Eliminar**.</span><span class="sxs-lookup"><span data-stu-id="79e11-141">Select the entry that you want to delete, and then choose the **Delete** action.</span></span>

    <span data-ttu-id="79e11-142">El usuario podrá ver los cambios la próxima vez que inicie sesión.</span><span class="sxs-lookup"><span data-stu-id="79e11-142">The user will see the changes the next time they sign-in.</span></span>

### <a name="to-clear-user-personalizations-by-using-the-user-personalization-card-page"></a><span data-ttu-id="79e11-143">Para borrar las personalizaciones de los usuarios con la página Tarjeta personalización de usuarios</span><span class="sxs-lookup"><span data-stu-id="79e11-143">To clear user personalizations by using the User Personalization Card page</span></span>

<span data-ttu-id="79e11-144">La página **Tarjeta personalización de usuarios** le permite borrar la personalización en todas las páginas de un usuario específico.</span><span class="sxs-lookup"><span data-stu-id="79e11-144">The **User Personalization Card** page enables you to clear the personalization on all pages for specific user.</span></span> <span data-ttu-id="79e11-145">Esto requiere permiso de escritura para el **perfil** de tabla 2000000072.</span><span class="sxs-lookup"><span data-stu-id="79e11-145">This requires write permission to Table 2000000072 **Profile**.</span></span>

1. <span data-ttu-id="79e11-146">Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Personalización usuario** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="79e11-146">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **User Personalization**, and then choose the related link.</span></span>

    <span data-ttu-id="79e11-147">La página **Personalización usuario** muestra todos los usuarios que potencialmente hayan personalizado las páginas.</span><span class="sxs-lookup"><span data-stu-id="79e11-147">The **User Personalization** page lists all users who potentially have personalized pages.</span></span> <span data-ttu-id="79e11-148">Si no puede encontrar un usuario en la lista, significa que no tiene páginas personalizadas.</span><span class="sxs-lookup"><span data-stu-id="79e11-148">If you cannot find a user in the list, this means that they do not have any personalized pages.</span></span>

2. <span data-ttu-id="79e11-149">Seleccione el usuario de la lista y, a continuación, seleccione la acción **Editar**.</span><span class="sxs-lookup"><span data-stu-id="79e11-149">Select the user from the list, and then choose the **Edit** action.</span></span>

3. <span data-ttu-id="79e11-150">En la pestaña **Acciones**, elija **Borrar páginas personalizadas**.</span><span class="sxs-lookup"><span data-stu-id="79e11-150">On the **Actions** tab, choose **Clear Personalized Pages**.</span></span>

    <span data-ttu-id="79e11-151">El usuario podrá ver los cambios la próxima vez que inicie sesión.</span><span class="sxs-lookup"><span data-stu-id="79e11-151">The user will see the changes the next time they sign-in.</span></span>

## <a name="see-also"></a><span data-ttu-id="79e11-152">Consulte también</span><span class="sxs-lookup"><span data-stu-id="79e11-152">See Also</span></span>
[<span data-ttu-id="79e11-153">Personalización de su área de trabajo</span><span class="sxs-lookup"><span data-stu-id="79e11-153">Personalizing Your Workspace</span></span>](ui-personalization-user.md)  
<span data-ttu-id="79e11-154">[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="79e11-154">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="79e11-155">Cambiar la configuración básica</span><span class="sxs-lookup"><span data-stu-id="79e11-155">Changing Basic Settings</span></span>](ui-change-basic-settings.md)  
[<span data-ttu-id="79e11-156">Cambiar las funciones que se muestran</span><span class="sxs-lookup"><span data-stu-id="79e11-156">Changing Which Features are Displayed</span></span>](ui-experiences.md)  
