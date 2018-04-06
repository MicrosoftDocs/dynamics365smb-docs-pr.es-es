---
title: Crear un entorno aislado | Documentos de Microsoft
description: Crear un entorno para explorar, aprender, demostrar, desarrollar y probar.
author: SusanneWindfeldPedersen
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: sandbox, demo, develop
ms.date: 08/18/2017
ms.author: solsen
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: b3ee160e2c38107aea1342b51d729aa172bbbc3e
ms.contentlocale: es-es
ms.lasthandoff: 03/22/2018

---
[!INCLUDE[d365fin_early_release](includes/d365fin_early_release.md.md)]

# <a name="create-a-sandbox-environment"></a><span data-ttu-id="91ef1-103">Crear un entorno aislado</span><span class="sxs-lookup"><span data-stu-id="91ef1-103">Create a Sandbox Environment</span></span>
<span data-ttu-id="91ef1-104">Un entorno aislado (vista preliminar) es una instancia de no producción de [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="91ef1-104">A sandbox environment (Preview) is a non-production instance of [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="91ef1-105">Aislado de la producción, un entorno aislado es el lugar para explorar, aprender, demostrar, desarrollar y probar el servicio de forma segura sin el riesgo de afectar los datos y la configuración de su entorno de producción.</span><span class="sxs-lookup"><span data-stu-id="91ef1-105">Isolated from production, a sandbox environment is the place to safely explore, learn, demo, develop, and test the service without the risk of affecting the data and settings of your production environment.</span></span>

## <a name="to-create-a-sandbox-environment"></a><span data-ttu-id="91ef1-106">Para crear un entorno aislado</span><span class="sxs-lookup"><span data-stu-id="91ef1-106">To create a sandbox environment</span></span>
<span data-ttu-id="91ef1-107">Debe tener una suscripción a [!INCLUDE[d365fin](includes/d365fin_md.md)] para poder crear un entorno aislado.</span><span class="sxs-lookup"><span data-stu-id="91ef1-107">You must have a subscription to [!INCLUDE[d365fin](includes/d365fin_md.md)] to be able to create a sandbox environment.</span></span> <span data-ttu-id="91ef1-108">Puede haber solo un entorno aislado por suscripción.</span><span class="sxs-lookup"><span data-stu-id="91ef1-108">There can only be one sandbox environment per subscription.</span></span>

1. <span data-ttu-id="91ef1-109">Inicie sesión en su instancia de producción del servicio [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="91ef1-109">Sign in to your production instance of the [!INCLUDE[d365fin](includes/d365fin_md.md)] service.</span></span>
2. <span data-ttu-id="91ef1-110">Elija el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), introduzca **Entorno aislado** y elija el vínculo relacionado.</span><span class="sxs-lookup"><span data-stu-id="91ef1-110">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Sandbox Environment**, and then choose the related link.</span></span>
<span data-ttu-id="91ef1-111">![Configuración de un entorno aislado](./media/across-sandbox/sandbox-environment-setup.png)</span><span class="sxs-lookup"><span data-stu-id="91ef1-111">![Sandbox Environment Setup](./media/across-sandbox/sandbox-environment-setup.png)</span></span>
3. <span data-ttu-id="91ef1-112">Seleccione **Crear**.</span><span class="sxs-lookup"><span data-stu-id="91ef1-112">Select **Create**.</span></span>  
  <span data-ttu-id="91ef1-113">Se abrirá otra pestaña en el navegador para finalizar la configuración del entorno aislado.</span><span class="sxs-lookup"><span data-stu-id="91ef1-113">Another tab in your browser will open for finishing the setup of your sandbox environment.</span></span>
> [!NOTE]  
>  <span data-ttu-id="91ef1-114">Si tiene activado el bloqueador de ventanas emergentes en su navegador, cámbielo para permitir las direcciones URL de la dirección \*.financials.dynamics.com.</span><span class="sxs-lookup"><span data-stu-id="91ef1-114">If you have pop-up blocker enabled in your browser, change it to allow URLs from the \*.financials.dynamics.com address.</span></span>   

4. <span data-ttu-id="91ef1-115">Cuando el entorno aislado esté listo, se le redirigirá al asistente de bienvenida del entorno aislado.</span><span class="sxs-lookup"><span data-stu-id="91ef1-115">When the sandbox environment is ready, you will be redirected to sandbox environment's Welcome wizard.</span></span>
<span data-ttu-id="91ef1-116">![Asistente de bienvenida del entorno aislado](./media/across-sandbox/sandbox-wizard.png)</span><span class="sxs-lookup"><span data-stu-id="91ef1-116">![Sandbox Welcome Wizard](./media/across-sandbox/sandbox-wizard.png)</span></span>

5. <span data-ttu-id="91ef1-117">Seleccione **Más información** para consultar información sobre los escenarios que puede probar en un entorno aislado.</span><span class="sxs-lookup"><span data-stu-id="91ef1-117">Choose **Learn more** to read about scenarios that you can try in a sandbox environment.</span></span> <span data-ttu-id="91ef1-118">O bien, elija **Cerrar** para continuar con el Área de trabajo de la instancia aislada de [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="91ef1-118">Or, choose **Close** to continue to the Role Center of your [!INCLUDE[d365fin](includes/d365fin_md.md)] sandbox instance.</span></span>
6. <span data-ttu-id="91ef1-119">En la parte superior del Área de trabajo, aparece una notificación para informarle de que se trata de un entorno aislado.</span><span class="sxs-lookup"><span data-stu-id="91ef1-119">At the top of the Role Center, a notification appears to inform you that this is a sandbox environment.</span></span> <span data-ttu-id="91ef1-120">También puede ver el tipo del entorno en la barra de título del cliente.</span><span class="sxs-lookup"><span data-stu-id="91ef1-120">You can also see the type of the environment in the title bar of the client.</span></span>
<span data-ttu-id="91ef1-121">![Notificaciones del Área de trabajo del entorno aislado](./media/across-sandbox/sandbox-rolecenter-notification.png)</span><span class="sxs-lookup"><span data-stu-id="91ef1-121">![Sandbox RoleCenter Notification](./media/across-sandbox/sandbox-rolecenter-notification.png)</span></span>  
<span data-ttu-id="91ef1-122">En el entorno aislado, se ha creado un nuevo suscriptor.</span><span class="sxs-lookup"><span data-stu-id="91ef1-122">In the sandbox environment, a brand-new tenant has been created.</span></span> <span data-ttu-id="91ef1-123">Este suscriptor se carga con datos de demostración predeterminados para la empresa CRONUS.</span><span class="sxs-lookup"><span data-stu-id="91ef1-123">This tenant is loaded with default demonstration data for the CRONUS company.</span></span> <span data-ttu-id="91ef1-124">No se copian ni se transfieren datos del entorno de producción durante la creación del entorno aislado.</span><span class="sxs-lookup"><span data-stu-id="91ef1-124">No data is copied or otherwise transferred from the production environment during the sandbox creation.</span></span>
7.  <span data-ttu-id="91ef1-125">Cuando lo desee puede volver a la página **Entorno aislado** y restablecerlo.</span><span class="sxs-lookup"><span data-stu-id="91ef1-125">At any time, you can return to the **Sandbox Environment** page, and reset the sandbox environment.</span></span>
> [!NOTE]  
>  <span data-ttu-id="91ef1-126">Al restablecer el entorno aislado se eliminará completamente y, a continuación, se creará de nuevo con los datos de demostración predeterminados.</span><span class="sxs-lookup"><span data-stu-id="91ef1-126">Resetting the sandbox environment will remove it completely, and then create it again with the default demonstration data.</span></span>  

8.  <span data-ttu-id="91ef1-127">Para cambiar entre los entornos de producción y aislado, puede utilizar el lanzador de aplicaciones de Finance and Operations, Business edition.</span><span class="sxs-lookup"><span data-stu-id="91ef1-127">To switch between your production and sandbox environments, you can use the Finance and Operations, Business edition app launcher.</span></span>
<span data-ttu-id="91ef1-128">![Menú del espacio aislado de Dynamics365](./media/across-sandbox/sandbox-dynamics365-menu.png)</span><span class="sxs-lookup"><span data-stu-id="91ef1-128">![Sandbox Dynamics365 Menu](./media/across-sandbox/sandbox-dynamics365-menu.png)</span></span>

9.  <span data-ttu-id="91ef1-129">Es posible que un administrador u otro usuario limite o incluso bloquee el acceso de algunos usuarios al entorno aislado.</span><span class="sxs-lookup"><span data-stu-id="91ef1-129">It is possible for an administrator or another user to limit or even block access for some users to the sandbox environment.</span></span> <span data-ttu-id="91ef1-130">Esto se puede hacer mediante las características de seguridad estándar del producto, como la tarjeta de usuario, los grupos de usuarios y los conjuntos de permisos.</span><span class="sxs-lookup"><span data-stu-id="91ef1-130">This can be done by using the standard security features of the product, such as the User card, User Groups, and Permission Sets.</span></span>

![Conjuntos de permisos del entorno aislado](./media/across-sandbox/sandbox-permission-sets.png)

## <a name="advanced-functionality-in-the-sandbox-environment"></a><span data-ttu-id="91ef1-132">Funcionalidad avanzada del entorno aislado</span><span class="sxs-lookup"><span data-stu-id="91ef1-132">Advanced functionality in the sandbox environment</span></span>
### <a name="the-in-client-designer"></a><span data-ttu-id="91ef1-133">El diseñador del cliente</span><span class="sxs-lookup"><span data-stu-id="91ef1-133">The in-client designer</span></span>
<span data-ttu-id="91ef1-134">En un entorno aislado, se encuentra habilitada la función de diseñador en el cliente, que puede activar seleccionando el icono de diseño</span><span class="sxs-lookup"><span data-stu-id="91ef1-134">In a sandbox environment, you will find the in-client designer feature enabled, which you can activate by selecting the design icon</span></span> ![Diseñadora](./media/across-sandbox/sandbox-inclient-design-icon.png) <span data-ttu-id="91ef1-136">en una página.</span><span class="sxs-lookup"><span data-stu-id="91ef1-136">on a page.</span></span>

![Diseñador del cliente](./media/across-sandbox/sandbox-inclient-designer.png)

### <a name="enable-the-advanced-user-experience"></a><span data-ttu-id="91ef1-138">Activar la experiencia del usuario avanzado</span><span class="sxs-lookup"><span data-stu-id="91ef1-138">Enable the advanced user experience</span></span>
<span data-ttu-id="91ef1-139">Es posible activar y probar la funcionalidad avanzada (completa) de [!INCLUDE[d365fin](includes/d365fin_md.md)] en un suscriptor aislado configurando el campo **Experiencia** en la página **Información de la empresa**.</span><span class="sxs-lookup"><span data-stu-id="91ef1-139">It is possible to enable and try the advanced (full) functionality of [!INCLUDE[d365fin](includes/d365fin_md.md)] in a sandbox tenant by setting the **Experience** field on the **Company Information** page.</span></span>

![Entorno aislado avanzado](./media/across-sandbox/sandbox-advanced.png)

![Producción de entorno aislado](./media/across-sandbox/sandbox-production.png)

<span data-ttu-id="91ef1-142">Después de habilitar la funcionalidad avanzada en un inquilino aislado, obtiene acceso a todos los perfiles y áreas de trabajo estándar.</span><span class="sxs-lookup"><span data-stu-id="91ef1-142">After you’ve enabled the advanced functionality in a sandbox tenant, you get access to all the standard Profiles and Role Centers.</span></span> <span data-ttu-id="91ef1-143">También puede crear una empresa de evaluación que esté completamente configurada, incluyendo datos de demostración y acceso a las áreas avanzadas del producto.</span><span class="sxs-lookup"><span data-stu-id="91ef1-143">You can also create an evaluation company that is fully set up, including demonstration data and access to the advanced areas of the product.</span></span>

![Nueva empresa aislada](./media/across-sandbox/sandbox-newcompany.png)


## <a name="see-also"></a><span data-ttu-id="91ef1-145">Consulte también</span><span class="sxs-lookup"><span data-stu-id="91ef1-145">See Also</span></span>
<span data-ttu-id="91ef1-146">[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="91ef1-146">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

