---
title: "Administrar la personalización como administrador en Business Central | Documentos de Microsoft"
description: Aprenda a personalizar la interfaz de usuario para que se adapte a su forma de trabajar.
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customize, personalize, personalization, hide columns, remove fields, move fields
ms.date: 10/01/2018
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 78eea4df6f25772063cef5770eb1dcb433bee012
ms.contentlocale: es-es
ms.lasthandoff: 09/28/2018

---
# <a name="managing-personalization-as-an-administrator"></a><span data-ttu-id="33420-103">Administrar la personalización como administrador</span><span class="sxs-lookup"><span data-stu-id="33420-103">Managing Personalization as an Administrator</span></span>
<span data-ttu-id="33420-104"><!--NAV in the Web client--> Los usuarios pueden personalizar el área de trabajo para que se adapte a sus preferencias.</span><span class="sxs-lookup"><span data-stu-id="33420-104"><!--NAV in the Web client--> Users can personalize their workspace to suit their own preferences.</span></span> <span data-ttu-id="33420-105">Como administrador, puede controlar y administrar la personalización desactivando la capacidad de los usuarios para personalizar las páginas y borrar las personalizaciones de página que los usuarios hayan realizado.</span><span class="sxs-lookup"><span data-stu-id="33420-105">As an administrator, you can control and manage personalization by disabling the ability for users to personalize pages and clearing any page personalizations that users have made.</span></span>

## <a name="disable-personalization-for-a-profile"></a><span data-ttu-id="33420-106">Deshabilitar la personalización de un perfil</span><span class="sxs-lookup"><span data-stu-id="33420-106">Disable personalization for a profile</span></span>
<span data-ttu-id="33420-107">Puede evitar que todos los usuarios que pertenecen a un perfil específico puedan personalizar sus páginas.</span><span class="sxs-lookup"><span data-stu-id="33420-107">You can prevent all users that belong to a specific profile from being able to personalize their pages.</span></span>
1.  <span data-ttu-id="33420-108">Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Perfiles** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="33420-108">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Profiles**, and then choose the related link.</span></span>
2.  <span data-ttu-id="33420-109">Seleccione el perfil de la lista que desea modificar.</span><span class="sxs-lookup"><span data-stu-id="33420-109">Select the profile in the list that you want to modify.</span></span>
3. <span data-ttu-id="33420-110">Seleccione la casilla **Deshabilitar personalización** y, a continuación, seleccione el botón **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="33420-110">Select the **Disable personalization** check box, and then choose the **OK** button.</span></span>

## <a name="clear-user-personalizations"></a><span data-ttu-id="33420-111">Borrar personalizaciones de usuarios</span><span class="sxs-lookup"><span data-stu-id="33420-111">Clear user personalizations</span></span>

<span data-ttu-id="33420-112">Al borrar la personalización de la página, la página vuelve a su diseño original antes de realizar cualquier personalización.</span><span class="sxs-lookup"><span data-stu-id="33420-112">Clearing page personalization changes the page back to its original layout before any personalization was made.</span></span> <span data-ttu-id="33420-113">Existen dos formas de borrar las personalizaciones que los usuarios han realizado en las páginas: usando la ventana **Eliminar personalización usuario** o la ventana **Tarjeta personalización usuario**.</span><span class="sxs-lookup"><span data-stu-id="33420-113">There are two ways to clear the personalizations that users have made to pages: using the **Delete User Personalization** window and using the **User Personalization Card** window.</span></span>

### <a name="clear-user-personalizations-by-using-the-delete-user-personalization-page"></a><span data-ttu-id="33420-114">Borrar las personalizaciones de los usuarios con la página Eliminar personalización de usuarios.</span><span class="sxs-lookup"><span data-stu-id="33420-114">Clear user personalizations by using the Delete User Personalization page</span></span>

<span data-ttu-id="33420-115">La ventana **Eliminar personalización de usuarios** le permite borrar la personalización por página y por usuario.</span><span class="sxs-lookup"><span data-stu-id="33420-115">The **Delete User Personalization** window enables you to clear personalizations on a per-page basis for each user individually.</span></span>

1.  <span data-ttu-id="33420-116">Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Eliminar personalización usuario** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="33420-116">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Delete User Personalization**, and then choose the related link.</span></span>

    <span data-ttu-id="33420-117">La página enumera todas las páginas que se han personalizado y el usuario al que pertenece.</span><span class="sxs-lookup"><span data-stu-id="33420-117">The page lists all the pages that have been personalized and the user it belongs to.</span></span>

    >[!NOTE]
    > <span data-ttu-id="33420-118">Una marca de verificación en las columnas **Personalización heredada** indica que la personalización se realizó en una versión anterior de [!INCLUDE[d365fin](includes/d365fin_md.md)] que manejaba la personalización de forma diferente a como lo hace ahora.</span><span class="sxs-lookup"><span data-stu-id="33420-118">A check mark in the **Legacy Personalization** columns indicates that the personalization was done in an older version of [!INCLUDE[d365fin](includes/d365fin_md.md)], which handled personalization different than it does now.</span></span> <span data-ttu-id="33420-119">Los usuarios que intentan personalizar estas páginas se bloquean a menos que elijan desbloquear la página.</span><span class="sxs-lookup"><span data-stu-id="33420-119">Users who try to personalize these pages are locked from doing so unless they choose to unlock the page.</span></span> <span data-ttu-id="33420-120">Para obtener más información, consulte [Por qué la página está bloqueada para la personalización](ui-personalization-locked.md).</span><span class="sxs-lookup"><span data-stu-id="33420-120">For more information, see [Why a page is locked from personalizing](ui-personalization-locked.md).</span></span>

2. <span data-ttu-id="33420-121">Seleccione el movimiento que desea eliminar y, después, seleccione **Eliminar**.</span><span class="sxs-lookup"><span data-stu-id="33420-121">Select the entry that you want to delete, and then choose the **Delete** action.</span></span>

    <span data-ttu-id="33420-122">El usuario podrá ver los cambios la próxima vez que inicie sesión.</span><span class="sxs-lookup"><span data-stu-id="33420-122">The user will see the changes the next time they sign-in.</span></span>

### <a name="clear-user-personalizations-by-using-the-user-personalization-card-page"></a><span data-ttu-id="33420-123">Borrar las personalizaciones de los usuarios con la página Tarjeta personalización de usuarios</span><span class="sxs-lookup"><span data-stu-id="33420-123">Clear user personalizations by using the User Personalization Card page</span></span>

<span data-ttu-id="33420-124">La ventana **Tarjeta personalización de usuarios** le permite borrar la personalización en todas las páginas de un usuario específico.</span><span class="sxs-lookup"><span data-stu-id="33420-124">The **User Personalization Card** window enables you to clear the personalization on all pages for specific user.</span></span> <span data-ttu-id="33420-125">Esto requiere permiso de escritura para el **perfil** de tabla 2000000072.</span><span class="sxs-lookup"><span data-stu-id="33420-125">This requires write permission to Table 2000000072 **Profile**.</span></span>

1.  <span data-ttu-id="33420-126">Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Personalización usuario** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="33420-126">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **User Personalization**, and then choose the related link.</span></span>

    <span data-ttu-id="33420-127">La ventana **Personalización usuario** muestra todos los usuarios que potencialmente hayan personalizado las páginas.</span><span class="sxs-lookup"><span data-stu-id="33420-127">The **User Personalization** window lists all users who potentially have personalized pages.</span></span> <span data-ttu-id="33420-128">Si no puede encontrar un usuario en la lista, significa que no tiene páginas personalizadas.</span><span class="sxs-lookup"><span data-stu-id="33420-128">If you cannot find a user in the list, this means that they do not have any personalized pages.</span></span>

2. <span data-ttu-id="33420-129">Seleccione el usuario de la lista y, a continuación, seleccione la acción **Editar**.</span><span class="sxs-lookup"><span data-stu-id="33420-129">Select the user from the list, and then choose the **Edit** action.</span></span>

3.  <span data-ttu-id="33420-130">En la pestaña **Acciones**, elija **Borrar páginas personalizadas**.</span><span class="sxs-lookup"><span data-stu-id="33420-130">On the **Actions** tab, choose **Clear Personalized Pages**.</span></span>

    <span data-ttu-id="33420-131">El usuario podrá ver los cambios la próxima vez que inicie sesión.</span><span class="sxs-lookup"><span data-stu-id="33420-131">The user will see the changes the next time they sign-in.</span></span>

## <a name="see-also"></a><span data-ttu-id="33420-132">Consulte también</span><span class="sxs-lookup"><span data-stu-id="33420-132">See Also</span></span>
[<span data-ttu-id="33420-133">Personalización de su área de trabajo</span><span class="sxs-lookup"><span data-stu-id="33420-133">Personalizing Your Workspace</span></span>](ui-personalization-user.md)  
<span data-ttu-id="33420-134">[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="33420-134">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="33420-135">Cambiar la configuración básica</span><span class="sxs-lookup"><span data-stu-id="33420-135">Changing Basic Settings</span></span>](ui-change-basic-settings.md)  
[<span data-ttu-id="33420-136">Cambiar las funciones que se muestran</span><span class="sxs-lookup"><span data-stu-id="33420-136">Changing Which Features are Displayed</span></span>](ui-experiences.md)  

