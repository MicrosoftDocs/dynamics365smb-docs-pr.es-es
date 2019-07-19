---
title: Crear un entorno aislado | Documentos de Microsoft
description: Crear un entorno para explorar, aprender, demostrar, desarrollar y probar.
author: SusanneWindfeldPedersen
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: sandbox, demo, develop
ms.date: 06/26/2019
ms.author: solsen
ms.openlocfilehash: 217310522d7e54eeaa9dbd50df4ff89b0d68517d
ms.sourcegitcommit: 5b6dd8d881c0eb65ece6936a94dfda3185574335
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 06/28/2019
ms.locfileid: "1711088"
---
[!INCLUDE[d365fin_early_release](includes/d365fin_early_release.md.md)]

# <a name="creating-a-sandbox-environment"></a><span data-ttu-id="4cd32-103">Crear un entorno aislado</span><span class="sxs-lookup"><span data-stu-id="4cd32-103">Creating a Sandbox Environment</span></span>
<span data-ttu-id="4cd32-104">Un entorno aislado (vista preliminar) es una instancia de no producción de [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="4cd32-104">A sandbox environment (Preview) is a non-production instance of [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="4cd32-105">Aislado de la producción, un entorno aislado es el lugar para explorar, aprender, demostrar, desarrollar y probar el servicio de forma segura sin el riesgo de afectar los datos y la configuración de su entorno de producción.</span><span class="sxs-lookup"><span data-stu-id="4cd32-105">Isolated from production, a sandbox environment is the place to safely explore, learn, demo, develop, and test the service without the risk of affecting the data and settings of your production environment.</span></span>

## <a name="to-create-a-sandbox-environment"></a><span data-ttu-id="4cd32-106">Para crear un entorno aislado</span><span class="sxs-lookup"><span data-stu-id="4cd32-106">To create a sandbox environment</span></span>
<span data-ttu-id="4cd32-107">Debe tener una suscripción a [!INCLUDE[d365fin](includes/d365fin_md.md)] para poder crear un entorno aislado.</span><span class="sxs-lookup"><span data-stu-id="4cd32-107">You must have a subscription to [!INCLUDE[d365fin](includes/d365fin_md.md)] to be able to create a sandbox environment.</span></span> <span data-ttu-id="4cd32-108">Puede haber solo un entorno aislado por suscripción.</span><span class="sxs-lookup"><span data-stu-id="4cd32-108">There can only be one sandbox environment per subscription.</span></span>

1. <span data-ttu-id="4cd32-109">Inicie sesión en su instancia de producción del servicio [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="4cd32-109">Sign in to your production instance of the [!INCLUDE[d365fin](includes/d365fin_md.md)] service.</span></span>

2. <span data-ttu-id="4cd32-110">Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Entorno de espacio aislado** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="4cd32-110">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Sandbox Environment**, and then choose the related link.</span></span>
<!-- ![Sandbox Environment Setup](./media/across-sandbox/sandbox-environment-setup.png) -->
3. <span data-ttu-id="4cd32-111">Haga clic en el botón **Crear**.</span><span class="sxs-lookup"><span data-stu-id="4cd32-111">Choose the **Create** button.</span></span>  

    <span data-ttu-id="4cd32-112">Se abre otra pestaña con [!INCLUDE[d365fin](includes/d365fin_md.md)] en la que puede terminar la configuración de su entorno aislado.</span><span class="sxs-lookup"><span data-stu-id="4cd32-112">Another tab with [!INCLUDE[d365fin](includes/d365fin_md.md)] opens where you can finish the setup of your sandbox environment.</span></span>

    > [!NOTE]  
    >  <span data-ttu-id="4cd32-113">Si tiene activado el bloqueador de ventanas emergentes en su navegador, cámbielo para permitir las direcciones URL de la dirección \*.businesscentral.dynamics.com.</span><span class="sxs-lookup"><span data-stu-id="4cd32-113">If you have pop-up blocker enabled in your browser, change it to allow URLs from the \*.businesscentral.dynamics.com address.</span></span>

4. <span data-ttu-id="4cd32-114">Cuando el entorno aislado esté listo, se le redirigirá al asistente de bienvenida del entorno aislado.</span><span class="sxs-lookup"><span data-stu-id="4cd32-114">When the sandbox environment is ready, you will be redirected to sandbox environment's Welcome wizard.</span></span>
<!-- ![Sandbox Welcome Wizard](./media/across-sandbox/sandbox-wizard.png) -->

5. <span data-ttu-id="4cd32-115">Seleccione el botón **Más información** para leer acerca de los escenarios que puede probar en un entorno aislado o seleccione el botón **Cerrar** para continuar con el área de trabajo de su instancia aislada de [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="4cd32-115">Choose the **Learn more** button to read about scenarios that you can try in a sandbox environment or choose the **Close** button to continue to the Role Center of your [!INCLUDE[d365fin](includes/d365fin_md.md)] sandbox instance.</span></span>

    <span data-ttu-id="4cd32-116">En la parte superior del Área de trabajo, aparece una notificación para informarle de que se trata de un entorno aislado.</span><span class="sxs-lookup"><span data-stu-id="4cd32-116">At the top of the Role Center, a notification appears to inform you that this is a sandbox environment.</span></span> <span data-ttu-id="4cd32-117">También puede ver el tipo del entorno en la barra de título del cliente.</span><span class="sxs-lookup"><span data-stu-id="4cd32-117">You can also see the type of the environment in the title bar of the client.</span></span>
    <!-- ![Sandbox RoleCenter Notification](./media/across-sandbox/sandbox-rolecenter-notification.png) -->

    > [!NOTE]
    > <span data-ttu-id="4cd32-118">Un entorno aislado creado de esta manera solo contiene los datos de demostración predeterminados para la empresa de CRONUS.</span><span class="sxs-lookup"><span data-stu-id="4cd32-118">A sandbox environment created in this way only contains the default demonstration data for the CRONUS company.</span></span> <span data-ttu-id="4cd32-119">No se copian ni se transfieren datos del entorno de producción.</span><span class="sxs-lookup"><span data-stu-id="4cd32-119">No data is copied or otherwise transferred from the production environment.</span></span><br /><br />
    > <span data-ttu-id="4cd32-120">También puede crear un entorno aislado que contenga los datos de producción.</span><span class="sxs-lookup"><span data-stu-id="4cd32-120">You can also create a sandbox environment containing the production data.</span></span> <span data-ttu-id="4cd32-121">Debe hacerlo a través del centro de administración.</span><span class="sxs-lookup"><span data-stu-id="4cd32-121">You must do this through the administration center.</span></span> <span data-ttu-id="4cd32-122">Para obtener más información, consulte [Administración de entornos](/business-central/dev-itpro/administration/tenant-admin-center-environments) en la Ayuda para desarrolladores y profesionales de TI.</span><span class="sxs-lookup"><span data-stu-id="4cd32-122">For more information, see [Managing Environments](/business-central/dev-itpro/administration/tenant-admin-center-environments) in the Developer and IT-Pro help.</span></span>

6. <span data-ttu-id="4cd32-123">Cuando lo desee puede volver a la página **Entorno aislado** y restablecerlo.</span><span class="sxs-lookup"><span data-stu-id="4cd32-123">At any time, you can return to the **Sandbox Environment** page, and reset the sandbox environment.</span></span>
    > [!NOTE]  
    >  <span data-ttu-id="4cd32-124">Al restablecer el entorno aislado se eliminará completamente y, a continuación, se creará de nuevo con los datos de demostración predeterminados.</span><span class="sxs-lookup"><span data-stu-id="4cd32-124">Resetting the sandbox environment will remove it completely, and then create it again with the default demonstration data.</span></span>  

7. <span data-ttu-id="4cd32-125">Para cambiar entre los entornos de producción y aislado, puede utilizar el lanzador de aplicaciones de Business Central.</span><span class="sxs-lookup"><span data-stu-id="4cd32-125">To switch between your production and sandbox environments, you can use the Business Central app launcher.</span></span>
<!-- ![Sandbox Dynamics365 Menu](./media/across-sandbox/sandbox-dynamics365-menu.png) -->

8. <span data-ttu-id="4cd32-126">Es posible que un administrador u otro usuario limite o incluso bloquee el acceso de algunos usuarios al entorno aislado.</span><span class="sxs-lookup"><span data-stu-id="4cd32-126">It is possible for an administrator or another user to limit or even block access for some users to the sandbox environment.</span></span> <span data-ttu-id="4cd32-127">Esto se puede hacer mediante las características de seguridad estándar del producto, como la tarjeta de usuario, los grupos de usuarios y los conjuntos de permisos.</span><span class="sxs-lookup"><span data-stu-id="4cd32-127">This can be done by using the standard security features of the product, such as the User card, user groups, and permission sets.</span></span>

<!-- ![Sandbox Permission Sets](./media/across-sandbox/sandbox-permission-sets.png) -->

## <a name="advanced-functionality-in-the-sandbox-environment"></a><span data-ttu-id="4cd32-128">Funcionalidad avanzada del entorno aislado</span><span class="sxs-lookup"><span data-stu-id="4cd32-128">Advanced Functionality in the Sandbox Environment</span></span>
### <a name="designer"></a><span data-ttu-id="4cd32-129">Diseñadora</span><span class="sxs-lookup"><span data-stu-id="4cd32-129">Designer</span></span>
<span data-ttu-id="4cd32-130">En un entorno aislado, se encuentra habilitada la función **Diseñador**, que puede activar seleccionando el icono ![Diseñador](./media/across-sandbox/sandbox-inclient-design-icon.png) en una página.</span><span class="sxs-lookup"><span data-stu-id="4cd32-130">In a sandbox environment, you will find the **Designer** enabled, which you can activate by selecting the design icon ![Designer](./media/across-sandbox/sandbox-inclient-design-icon.png) on a page.</span></span>

<!-- ![In-client Designer](./media/across-sandbox/sandbox-inclient-designer.png) -->

### <a name="to-enable-the-advanced-user-experience"></a><span data-ttu-id="4cd32-131">Para activar la experiencia del usuario avanzado</span><span class="sxs-lookup"><span data-stu-id="4cd32-131">To enable the advanced user experience</span></span>
<span data-ttu-id="4cd32-132">Es posible activar y probar la funcionalidad avanzada (completa) de [!INCLUDE[d365fin](includes/d365fin_md.md)] en un suscriptor aislado configurando el campo **Experiencia** en la página **Información de la empresa**.</span><span class="sxs-lookup"><span data-stu-id="4cd32-132">It is possible to enable and try the advanced (full) functionality of [!INCLUDE[d365fin](includes/d365fin_md.md)] in a sandbox tenant by setting the **Experience** field on the **Company Information** page.</span></span>

<!-- ![Sandbox Environment Advanced](./media/across-sandbox/sandbox-advanced.png) -->

<!-- ![Sandbox Production](./media/across-sandbox/sandbox-production.png) -->

<span data-ttu-id="4cd32-133">Después de habilitar la funcionalidad avanzada en un inquilino aislado, obtiene acceso a todos los perfiles y áreas de trabajo estándar.</span><span class="sxs-lookup"><span data-stu-id="4cd32-133">After you’ve enabled the advanced functionality in a sandbox tenant, you get access to all the standard Profiles and Role Centers.</span></span> <span data-ttu-id="4cd32-134">También puede crear una empresa de evaluación que esté completamente configurada, incluyendo datos de demostración y acceso a las áreas avanzadas del producto.</span><span class="sxs-lookup"><span data-stu-id="4cd32-134">You can also create an evaluation company that is fully set up, including demonstration data and access to the advanced areas of the product.</span></span>

<!-- ![Sandbox New Company](./media/across-sandbox/sandbox-newcompany.png) -->


## <a name="see-also"></a><span data-ttu-id="4cd32-135">Consulte también</span><span class="sxs-lookup"><span data-stu-id="4cd32-135">See Also</span></span>
<span data-ttu-id="4cd32-136">[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="4cd32-136">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
