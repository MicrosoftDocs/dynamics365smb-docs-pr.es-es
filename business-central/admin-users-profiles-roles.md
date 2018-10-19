---
title: Administre usuarios y roles | Documentos de Microsoft
description: "Obtener información sobre cómo administrar usuarios y áreas de trabajo en Business Central."
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: profiles, users
ms.date: 10/01/2018
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 1a94d023424c6eceb93af6e9ca89a90a3a94e996
ms.contentlocale: es-es
ms.lasthandoff: 09/28/2018

---
# <a name="understanding-users-profiles-and-role-centers"></a><span data-ttu-id="9fd8b-103">Comprender usuarios, perfiles y áreas de trabajo</span><span class="sxs-lookup"><span data-stu-id="9fd8b-103">Understanding Users, Profiles, and Role Centers</span></span>

<span data-ttu-id="9fd8b-104">En [!INCLUDE[d365fin](includes/d365fin_md.md)], un administrador añade a los usuarios y también les da acceso a las áreas de [!INCLUDE[d365fin](includes/d365fin_md.md)] que requieren en su trabajo.</span><span class="sxs-lookup"><span data-stu-id="9fd8b-104">In [!INCLUDE[d365fin](includes/d365fin_md.md)], users are added by an administrator who also gives users access to the areas of [!INCLUDE[d365fin](includes/d365fin_md.md)] that they need in their work.</span></span>  

<span data-ttu-id="9fd8b-105">El acceso a la funcionalidad se gestiona a través de *grupos de usuarios* y *perfiles*.</span><span class="sxs-lookup"><span data-stu-id="9fd8b-105">Access to functionality is managed through *user groups* and *profiles*.</span></span> <span data-ttu-id="9fd8b-106">Como administrador, puede agregar y quitar usuarios como parte de su suscripción a [!INCLUDE[d365fin](includes/d365fin_md.md)] y puede asignar permisos de usuario a través de grupos de usuarios.</span><span class="sxs-lookup"><span data-stu-id="9fd8b-106">As an administrator, you can add and remove users as part of your [!INCLUDE[d365fin](includes/d365fin_md.md)] subscription, and you can assign users permissions through user groups.</span></span>  

## <a name="adding-users"></a><span data-ttu-id="9fd8b-107">Añadir usuarios</span><span class="sxs-lookup"><span data-stu-id="9fd8b-107">Adding Users</span></span>

<span data-ttu-id="9fd8b-108">Para agregar usuarios en [!INCLUDE[d365fin](includes/d365fin_md.md)] en línea, el administrador de Office 365 de la empresa primero debe crear los usuarios en el centro de administración de Office 365.</span><span class="sxs-lookup"><span data-stu-id="9fd8b-108">To add users in [!INCLUDE[d365fin](includes/d365fin_md.md)] online, your company's Office 365 administrator must first create the users in the Office 365 Admin Center.</span></span> <span data-ttu-id="9fd8b-109">Para obtener más información, vea [Agregar usuarios a Office 365 para empresas](https://aka.ms/CreateOffice365Users).</span><span class="sxs-lookup"><span data-stu-id="9fd8b-109">For more information, see [Add Users to Office 365 for business](https://aka.ms/CreateOffice365Users).</span></span>

<span data-ttu-id="9fd8b-110">A continuación, el administrador puede asignar permisos a cada usuario y grupos de usuarios.</span><span class="sxs-lookup"><span data-stu-id="9fd8b-110">Then, the administrator can assign permissions to each user and groups of users.</span></span> <span data-ttu-id="9fd8b-111">Para obtener más información, vea [Administración de usuarios y permisos](ui-how-users-permissions.md).</span><span class="sxs-lookup"><span data-stu-id="9fd8b-111">For more information, see [Managing Users and Permissions](ui-how-users-permissions.md).</span></span>  

### <a name="users-of-on-premises-deployments"></a><span data-ttu-id="9fd8b-112">Usuarios de las implementaciones locales</span><span class="sxs-lookup"><span data-stu-id="9fd8b-112">Users of on-premises deployments</span></span>

<span data-ttu-id="9fd8b-113">Para las implementaciones locales de [!INCLUDE[d365fin](includes/d365fin_md.md)], el administrador puede elegir entre diferentes mecanismos de autorización de credenciales para los usuarios.</span><span class="sxs-lookup"><span data-stu-id="9fd8b-113">For on-premises deployments of [!INCLUDE[d365fin](includes/d365fin_md.md)], the administrator can choose between different credential authorization mechanisms for users.</span></span> <span data-ttu-id="9fd8b-114">Cuando cree un usuario, proporcione información distinta según el tipo de credencial que vaya a utilizar en la sesión específica de [!INCLUDE[server](includes/server.md)].</span><span class="sxs-lookup"><span data-stu-id="9fd8b-114">Then, when you create a user, you provide different information depending on the credential type that you are using in the specific [!INCLUDE[server](includes/server.md)] instance.</span></span> <span data-ttu-id="9fd8b-115">Para obtener más información, vea [Tipos de autenticación y credenciales](/dynamics365/business-central/dev-itpro/administration/users-credential-types) en la sección Administración del desarrollador y contenido de ITPro de [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="9fd8b-115">For more information, see the [Authentication and Credential Types](/dynamics365/business-central/dev-itpro/administration/users-credential-types) in the Administration section of the developer and ITPro content for [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>  

## <a name="profiles"></a><span data-ttu-id="9fd8b-116">Perfiles</span><span class="sxs-lookup"><span data-stu-id="9fd8b-116">Profiles</span></span>

<span data-ttu-id="9fd8b-117">La personas de su empresa que tienen acceso a [!INCLUDE[d365fin](includes/d365fin_md.md)] tienen asignado un *perfil* que les da acceso a un *Área de trabajo*.</span><span class="sxs-lookup"><span data-stu-id="9fd8b-117">The people in your company who have access to [!INCLUDE[d365fin](includes/d365fin_md.md)] are all assigned a *profile* that gives them access to a *Role Center*.</span></span>

<span data-ttu-id="9fd8b-118">Los perfiles son colecciones de usuarios de [!INCLUDE[d365fin](includes/d365fin_md.md)] que comparten la misma área de trabajo.</span><span class="sxs-lookup"><span data-stu-id="9fd8b-118">Profiles are collections of [!INCLUDE[d365fin](includes/d365fin_md.md)] users who share the same Role Center.</span></span> <span data-ttu-id="9fd8b-119">Un área de trabajo es el punto de entrada y la página de inicio de [!INCLUDE[d365fin](includes/d365fin_md.md)] que le da acceso rápido a sus tareas más importantes y le muestra varias perspectivas e indicadores de rendimiento clave (KPI) sobre su trabajo.</span><span class="sxs-lookup"><span data-stu-id="9fd8b-119">A Role Center is the entry point and home page for [!INCLUDE[d365fin](includes/d365fin_md.md)] that gives you quick access to your most important tasks and displays various insights and key performance indicators (KPIs) about your work.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="9fd8b-120">En la versión actual de [!INCLUDE[d365fin](includes/d365fin_md.md)] en línea, no puede agregar, editar, o eliminar perfiles.</span><span class="sxs-lookup"><span data-stu-id="9fd8b-120">In the current version of [!INCLUDE[d365fin](includes/d365fin_md.md)] online, you cannot add, edit, or delete profiles.</span></span>  

## <a name="configuration-and-personalization"></a><span data-ttu-id="9fd8b-121">Configuración y personalización</span><span class="sxs-lookup"><span data-stu-id="9fd8b-121">Configuration and Personalization</span></span>
<!--The concept of UI customization in [!INCLUDE[d365fin](includes/d365fin_md.md)] is divided in two:  

-   Configuration, performed by the administrator  

-   Personalization, performed by users  

The administrator configures the user interface for multiple users by customizing the user interface for a profile that the users are assigned to.  -->
<span data-ttu-id="9fd8b-122">Los usuarios personalizan la interfaz de usuario de su versión personal mediante la adaptación de la IU en su propio inicio de sesión de usuario.</span><span class="sxs-lookup"><span data-stu-id="9fd8b-122">Users personalize the user interface of their personal version by customizing the user interface under their own user logon.</span></span> <span data-ttu-id="9fd8b-123">Esta personalización puede ser eliminada por el administrador.</span><span class="sxs-lookup"><span data-stu-id="9fd8b-123">This personalization can be deleted by the administrator.</span></span> <span data-ttu-id="9fd8b-124">Para obtener más información, vea [Personalización del área de trabajo](ui-personalization-user.md).</span><span class="sxs-lookup"><span data-stu-id="9fd8b-124">For more information, see [Personalizing Your Workspace](ui-personalization-user.md).</span></span>  

## <a name="see-also"></a><span data-ttu-id="9fd8b-125">Consulte también</span><span class="sxs-lookup"><span data-stu-id="9fd8b-125">See Also</span></span>  
[<span data-ttu-id="9fd8b-126">Gestionar usuarios y permisos</span><span class="sxs-lookup"><span data-stu-id="9fd8b-126">Managing Users and Permissions</span></span>](ui-how-users-permissions.md)  
[<span data-ttu-id="9fd8b-127">Administrar la personalización como administrador</span><span class="sxs-lookup"><span data-stu-id="9fd8b-127">Managing Personalization as an Administrator</span></span>](ui-personalization-manage.md)  
[<span data-ttu-id="9fd8b-128">Personalización de su área de trabajo</span><span class="sxs-lookup"><span data-stu-id="9fd8b-128">Personalizing Your Workspace</span></span>](ui-personalization-user.md)  

