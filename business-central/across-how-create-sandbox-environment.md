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
ms.date: 04/01/2020
ms.author: solsen
ms.openlocfilehash: 59b659ca458e6cfe7c13ef5094dbbf80a144c369
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/01/2020
ms.locfileid: "3188569"
---
# <a name="creating-a-sandbox-environment-in-prodshort"></a><span data-ttu-id="a203b-103">Crear un entorno aislado en [!INCLUDE [prodshort](includes/prodshort.md)]</span><span class="sxs-lookup"><span data-stu-id="a203b-103">Creating a Sandbox Environment in [!INCLUDE [prodshort](includes/prodshort.md)]</span></span>

<span data-ttu-id="a203b-104">Con [!INCLUDE [prodshort](includes/prodshort.md)], puede crear fácilmente un entorno seguro donde puede probar, formar o solucionar problemas sin alterar los procesos de trabajo o los datos de negocio de su empresa.</span><span class="sxs-lookup"><span data-stu-id="a203b-104">With [!INCLUDE [prodshort](includes/prodshort.md)], you can easily create a safe environment where you can test, train, or troubleshoot without disturbing your company's work processes or business data.</span></span> <span data-ttu-id="a203b-105">Tal entorno de no producción se llama *entorno aislado*.</span><span class="sxs-lookup"><span data-stu-id="a203b-105">Such a non-production environment is called a *sandbox*.</span></span> <span data-ttu-id="a203b-106">Aislado de la producción, un entorno aislado es el lugar para explorar, aprender, demostrar, desarrollar y probar el servicio de forma segura sin el riesgo de afectar los datos y la configuración de su entorno de producción.</span><span class="sxs-lookup"><span data-stu-id="a203b-106">Isolated from production, a sandbox environment is the place to safely explore, learn, demo, develop, and test the service without the risk of affecting the data and settings of your production environment.</span></span>  

<span data-ttu-id="a203b-107">Su administrador puede crear entornos aislados en el [centro de administración](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-environments?toc=/dynamics365/business-central/toc.json), pero si desea probar algo rápidamente, puede crear un entorno aislado desde dentro de [!INCLUDE [prodshort](includes/prodshort.md)].</span><span class="sxs-lookup"><span data-stu-id="a203b-107">Your administrator can create sandbox environments in the [administration center](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-environments?toc=/dynamics365/business-central/toc.json), but if you want to quickly test something, you can create a sandbox environment from inside [!INCLUDE [prodshort](includes/prodshort.md)].</span></span>  

> [!NOTE]
> <span data-ttu-id="a203b-108">Técnicamente, los entornos aislados son muy diferentes de los entornos de producción, incluso si su administrador crea un entorno aislado que incluye datos de producción.</span><span class="sxs-lookup"><span data-stu-id="a203b-108">Technically, sandbox environments are very different from production environments, even if your administrator creates a sandbox that includes production data.</span></span> <span data-ttu-id="a203b-109">No puede usar un entorno aislado para un banco de pruebas y no puede solicitar una exportación de base de datos, por ejemplo.</span><span class="sxs-lookup"><span data-stu-id="a203b-109">You cannot use a sandbox for benchmarking, and you cannot request a database export, for example.</span></span> <span data-ttu-id="a203b-110">Si desea crear un entorno aislado para banco de pruebas, su administrador puede crear un entorno de producción dedicado en el centro de administración.</span><span class="sxs-lookup"><span data-stu-id="a203b-110">If you want to create a sandbox for benchmarking, your administrator can create a dedicated production environment in the administration center.</span></span> <span data-ttu-id="a203b-111">Para obtener más información, consulte [Tipos de entornos](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-environments#types-of-environments).</span><span class="sxs-lookup"><span data-stu-id="a203b-111">For more information, see [Types of environments](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-environments#types-of-environments).</span></span>

## <a name="to-create-a-sandbox-environment-in-your-prodshort"></a><span data-ttu-id="a203b-112">Para crear un entorno aislado en su [!INCLUDE [prodshort](includes/prodshort.md)]</span><span class="sxs-lookup"><span data-stu-id="a203b-112">To create a sandbox environment in your [!INCLUDE [prodshort](includes/prodshort.md)]</span></span>

1. <span data-ttu-id="a203b-113">Inicie sesión en su instancia de producción de [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="a203b-113">Sign in to your production instance of [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>

2. <span data-ttu-id="a203b-114">Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Entorno aislado** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="a203b-114">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Sandbox Environment**, and then choose the related link.</span></span>
    <!-- ![Sandbox Environment Setup](./media/across-sandbox/sandbox-environment-setup.png) -->
3. <span data-ttu-id="a203b-115">Haga clic en el botón **Crear**.</span><span class="sxs-lookup"><span data-stu-id="a203b-115">Choose the **Create** button.</span></span>  

    <span data-ttu-id="a203b-116">Se abre otra pestaña con [!INCLUDE[d365fin](includes/d365fin_md.md)] en la que puede terminar la configuración de su entorno aislado.</span><span class="sxs-lookup"><span data-stu-id="a203b-116">Another tab with [!INCLUDE[d365fin](includes/d365fin_md.md)] opens where you can finish the setup of your sandbox environment.</span></span>

    > [!NOTE]  
    >  <span data-ttu-id="a203b-117">Si tiene activado el bloqueador de ventanas emergentes en su navegador, cámbielo para permitir las direcciones URL de la dirección \*.businesscentral.dynamics.com.</span><span class="sxs-lookup"><span data-stu-id="a203b-117">If you have pop-up blocker enabled in your browser, change it to allow URLs from the \*.businesscentral.dynamics.com address.</span></span>

<span data-ttu-id="a203b-118">Cuando el entorno aislado esté listo, se le redirigirá al asistente de bienvenida del entorno aislado.</span><span class="sxs-lookup"><span data-stu-id="a203b-118">When the sandbox environment is ready, you will be redirected to sandbox environment's Welcome wizard.</span></span>
<!-- ![Sandbox Welcome Wizard](./media/across-sandbox/sandbox-wizard.png) -->

<span data-ttu-id="a203b-119">Puede elegir el botón **Más información** para leer acerca de los escenarios de desarrollador que puede probar en un entorno aislado o seleccione el botón **Cerrar** para continuar con el área de trabajo de su instancia aislada de [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="a203b-119">You can choose the **Learn more** button to read about developer scenarios that you can try in a sandbox environment or choose the **Close** button to continue to the Role Center of your [!INCLUDE[d365fin](includes/d365fin_md.md)] sandbox instance.</span></span>

<span data-ttu-id="a203b-120">En la parte superior del Área de trabajo, aparece una notificación para informarle de que se trata de un entorno aislado.</span><span class="sxs-lookup"><span data-stu-id="a203b-120">At the top of the Role Center, a notification appears to inform you that this is a sandbox environment.</span></span> <span data-ttu-id="a203b-121">También puede ver el tipo del entorno en la barra de título del cliente.</span><span class="sxs-lookup"><span data-stu-id="a203b-121">You can also see the type of the environment in the title bar of the client.</span></span>
    <!-- ![Sandbox RoleCenter Notification](./media/across-sandbox/sandbox-rolecenter-notification.png) -->

> [!NOTE]
> <span data-ttu-id="a203b-122">Un entorno aislado creado de esta manera solo contiene los datos de demostración predeterminados para la empresa de CRONUS.</span><span class="sxs-lookup"><span data-stu-id="a203b-122">A sandbox environment created in this way only contains the default demonstration data for the CRONUS company.</span></span> <span data-ttu-id="a203b-123">No se copian ni se transfieren datos del entorno de producción.</span><span class="sxs-lookup"><span data-stu-id="a203b-123">No data is copied or otherwise transferred from the production environment.</span></span><br /><br />
> <span data-ttu-id="a203b-124">También puede crear un entorno aislado que contenga los datos de producción.</span><span class="sxs-lookup"><span data-stu-id="a203b-124">You can also create a sandbox environment containing the production data.</span></span> <span data-ttu-id="a203b-125">Debe hacerlo a través del centro de administración.</span><span class="sxs-lookup"><span data-stu-id="a203b-125">You must do this through the administration center.</span></span> <span data-ttu-id="a203b-126">Para obtener más información, consulte [Administración de entornos](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-environments) en la Ayuda para desarrolladores y profesionales de TI.</span><span class="sxs-lookup"><span data-stu-id="a203b-126">For more information, see [Managing Environments](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-environments) in the Developer and IT-Pro help.</span></span>

<span data-ttu-id="a203b-127">Cuando lo desee puede volver a la página **Entorno aislado** y restablecerlo.</span><span class="sxs-lookup"><span data-stu-id="a203b-127">At any time, you can return to the **Sandbox Environment** page, and reset the sandbox environment.</span></span>

> [!NOTE]  
> <span data-ttu-id="a203b-128">Al restablecer el entorno aislado se eliminará completamente y, a continuación, se creará de nuevo con los datos de demostración predeterminados.</span><span class="sxs-lookup"><span data-stu-id="a203b-128">Resetting the sandbox environment will remove it completely, and then create it again with the default demonstration data.</span></span>  

<!--To switch between your production and sandbox environments, you can use the Business Central app launcher.
    ![Sandbox Dynamics365 Menu](./media/across-sandbox/sandbox-dynamics365-menu.png) -->

<span data-ttu-id="a203b-129">Un administrador puede limitar o incluso bloquear el acceso de algunos usuarios al entorno aislado.</span><span class="sxs-lookup"><span data-stu-id="a203b-129">An administrator can limit or even block access for some users to the sandbox environment.</span></span> <span data-ttu-id="a203b-130">Esto se puede hacer mediante las características de seguridad estándar del producto, como la tarjeta de usuario, los grupos de usuarios y los conjuntos de permisos.</span><span class="sxs-lookup"><span data-stu-id="a203b-130">This can be done by using the standard security features of the product, such as the User card, user groups, and permission sets.</span></span> <span data-ttu-id="a203b-131">Para obtener más información, vea [Asignar permisos a usuarios y grupos](ui-define-granular-permissions.md).</span><span class="sxs-lookup"><span data-stu-id="a203b-131">For more information, see [Assign Permissions to Users and Groups](ui-define-granular-permissions.md).</span></span>  

<!-- ![Sandbox Permission Sets](./media/across-sandbox/sandbox-permission-sets.png) -->

## <a name="advanced-functionality-in-the-sandbox-environment"></a><span data-ttu-id="a203b-132">Funcionalidad avanzada del entorno aislado</span><span class="sxs-lookup"><span data-stu-id="a203b-132">Advanced Functionality in the Sandbox Environment</span></span>

<span data-ttu-id="a203b-133">El entorno aislado no es menos útil porque incluye un par de características útiles.</span><span class="sxs-lookup"><span data-stu-id="a203b-133">The sandbox environment is not least useful because it includes a couple of handy features.</span></span>

### <a name="designer"></a><span data-ttu-id="a203b-134">Diseñadora</span><span class="sxs-lookup"><span data-stu-id="a203b-134">Designer</span></span>

<span data-ttu-id="a203b-135">En un entorno aislado, encontrará el **Diseñador** habilitado</span><span class="sxs-lookup"><span data-stu-id="a203b-135">In a sandbox environment, you will find the **Designer** enabled.</span></span> <span data-ttu-id="a203b-136">Puede activar el Diseñador seleccionando el icono de diseño ![Diseñador](./media/across-sandbox/sandbox-inclient-design-icon.png) en una página o eligiendo el elemento de menú **Diseño** en el menú ![Configuración](media/ui-experience/settings_icon_small.png) Configuración.</span><span class="sxs-lookup"><span data-stu-id="a203b-136">You can activate Designer by selecting the design icon ![Designer](./media/across-sandbox/sandbox-inclient-design-icon.png) on a page, or by choosing the **Design** menu item in the ![Settings](media/ui-experience/settings_icon_small.png) Settings menu.</span></span>

<!-- ![In-client Designer](./media/across-sandbox/sandbox-inclient-designer.png) -->

### <a name="to-enable-the-advanced-user-experience"></a><span data-ttu-id="a203b-137">Para activar la experiencia del usuario avanzado</span><span class="sxs-lookup"><span data-stu-id="a203b-137">To enable the advanced user experience</span></span>
<span data-ttu-id="a203b-138">Es posible activar y probar la función avanzada (completa) de la versión estándar [!INCLUDE[d365fin](includes/d365fin_md.md)] de un suscriptor aislado configurando el campo **Experiencia** en la página **Información de la empresa**.</span><span class="sxs-lookup"><span data-stu-id="a203b-138">It is possible to enable and try the full functionality of the standard version of [!INCLUDE[d365fin](includes/d365fin_md.md)] in a sandbox tenant by setting the **Experience** field on the **Company Information** page.</span></span>

<!-- ![Sandbox Environment Advanced](./media/across-sandbox/sandbox-advanced.png) -->

<!-- ![Sandbox Production](./media/across-sandbox/sandbox-production.png) -->

<span data-ttu-id="a203b-139">Después de habilitar la experiencia de usuario *Premium*, obtendrá acceso a todos los perfiles estándar (roles) y áreas de trabajo en la versión estándar.</span><span class="sxs-lookup"><span data-stu-id="a203b-139">After you have enabled the *Premium* user experience, you get access to all the standard profiles (roles) and Role Centers in the standard version.</span></span> <span data-ttu-id="a203b-140">También puede crear una empresa de evaluación que esté completamente configurada, incluyendo datos de demostración y acceso a las áreas avanzadas del producto.</span><span class="sxs-lookup"><span data-stu-id="a203b-140">You can also create an evaluation company that is fully set up, including demonstration data and access to the advanced areas of the product.</span></span> <span data-ttu-id="a203b-141">Alternativamente, póngase en contacto con un distribuidor para una demostración de las capacidades.</span><span class="sxs-lookup"><span data-stu-id="a203b-141">Alternatively, contact a reselling partner for a demonstration of the capabilities.</span></span> <span data-ttu-id="a203b-142">Para obtener más información, vea [¿Cómo encuentro un socio distribuidor?](across-faq.md#findpartner)</span><span class="sxs-lookup"><span data-stu-id="a203b-142">For more information, see [How do I find a reselling partner?](across-faq.md#findpartner).</span></span>  

<!-- ![Sandbox New Company](./media/across-sandbox/sandbox-newcompany.png) -->

## <a name="see-also"></a><span data-ttu-id="a203b-143">Consulte también</span><span class="sxs-lookup"><span data-stu-id="a203b-143">See Also</span></span>

<span data-ttu-id="a203b-144">[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="a203b-144">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
<span data-ttu-id="a203b-145">[Versiones de prueba y suscripciones de [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](across-preview.md)</span><span class="sxs-lookup"><span data-stu-id="a203b-145">[[!INCLUDE[d365fin_long](includes/d365fin_long_md.md)] Trials and Subscriptions](across-preview.md)</span></span>  
[<span data-ttu-id="a203b-146">Administración de entornos en el centro de administración de Business Central</span><span class="sxs-lookup"><span data-stu-id="a203b-146">Managing Environments in the Business Central administration center</span></span>](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-environments)  
