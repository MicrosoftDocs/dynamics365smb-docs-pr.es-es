---
title: Administre usuarios y roles | Documentos de Microsoft
description: "Obtener información sobre cómo administrar usuarios y áreas de trabajo en Business Central."
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.search.keywords: profiles, users
ms.date: 10/24/2018
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: 33b900f1ac9e295921e7f3d6ea72cc93939d8a1b
ms.openlocfilehash: 7ecd8a5ad2b321d4d1683047e70ede90c7ce229f
ms.contentlocale: es-es
ms.lasthandoff: 11/26/2018

---
# <a name="understanding-users-profiles-and-role-centers"></a><span data-ttu-id="058a2-103">Comprender usuarios, perfiles y áreas de trabajo</span><span class="sxs-lookup"><span data-stu-id="058a2-103">Understanding Users, Profiles, and Role Centers</span></span>

<span data-ttu-id="058a2-104">En [!INCLUDE[d365fin](includes/d365fin_md.md)], un administrador añade a los usuarios y también les da acceso a las áreas de [!INCLUDE[d365fin](includes/d365fin_md.md)] que requieren en su trabajo.</span><span class="sxs-lookup"><span data-stu-id="058a2-104">In [!INCLUDE[d365fin](includes/d365fin_md.md)], users are added by an administrator who also gives users access to the areas of [!INCLUDE[d365fin](includes/d365fin_md.md)] that they need in their work.</span></span>  

<span data-ttu-id="058a2-105">El acceso a la funcionalidad se gestiona a través de *grupos de usuarios* y *perfiles*.</span><span class="sxs-lookup"><span data-stu-id="058a2-105">Access to functionality is managed through *user groups* and *profiles*.</span></span> <span data-ttu-id="058a2-106">Como administrador, puede agregar y quitar usuarios como parte de su suscripción a [!INCLUDE[d365fin](includes/d365fin_md.md)] y puede asignar permisos de usuario a través de grupos de usuarios.</span><span class="sxs-lookup"><span data-stu-id="058a2-106">As an administrator, you can add and remove users as part of your [!INCLUDE[d365fin](includes/d365fin_md.md)] subscription, and you can assign users permissions through user groups.</span></span>  

## <a name="adding-users"></a><span data-ttu-id="058a2-107">Añadir usuarios</span><span class="sxs-lookup"><span data-stu-id="058a2-107">Adding Users</span></span>

<span data-ttu-id="058a2-108">Para agregar usuarios en [!INCLUDE[d365fin](includes/d365fin_md.md)] en línea, el administrador de Office 365 de la empresa primero debe crear los usuarios en el centro de administración de Office 365.</span><span class="sxs-lookup"><span data-stu-id="058a2-108">To add users in [!INCLUDE[d365fin](includes/d365fin_md.md)] online, your company's Office 365 administrator must first create the users in the Office 365 Admin Center.</span></span> <span data-ttu-id="058a2-109">Para obtener más información, vea [Agregar usuarios a Office 365 para empresas](https://aka.ms/CreateOffice365Users).</span><span class="sxs-lookup"><span data-stu-id="058a2-109">For more information, see [Add Users to Office 365 for business](https://aka.ms/CreateOffice365Users).</span></span>

<span data-ttu-id="058a2-110">A continuación, el administrador puede asignar permisos a cada usuario y grupos de usuarios.</span><span class="sxs-lookup"><span data-stu-id="058a2-110">Then, the administrator can assign permissions to each user and groups of users.</span></span> <span data-ttu-id="058a2-111">Para obtener más información, vea [Administración de usuarios y permisos](ui-how-users-permissions.md).</span><span class="sxs-lookup"><span data-stu-id="058a2-111">For more information, see [Managing Users and Permissions](ui-how-users-permissions.md).</span></span>  

<span data-ttu-id="058a2-112">Los permisos más potentes que un usuario puede tener es el conjunto de permisos SUPER.</span><span class="sxs-lookup"><span data-stu-id="058a2-112">The most powerful permissions that a user can have is the SUPER permission set.</span></span> <span data-ttu-id="058a2-113">Cada empresa debe tener al menos un usuario con este conjunto de permisos, pero es una práctica recomendada dar a cada usuario permisos que coincidan con sus necesidades de trabajo en [!INCLUDE[prodshort](includes/prodshort.md)] y no más que eso.</span><span class="sxs-lookup"><span data-stu-id="058a2-113">Each company must have at least one user with this permission set, but it is a best practice to give each user permissions that match their work needs in [!INCLUDE[prodshort](includes/prodshort.md)] and not more than that.</span></span> <span data-ttu-id="058a2-114">Esto contribuye a garantizar que los usuarios solo tengan acceso a los datos relevantes para su trabajo, por ejemplo.</span><span class="sxs-lookup"><span data-stu-id="058a2-114">This helps ensure that users only have access to data that is relevant to their work, for example.</span></span>  

> [!TIP]
> <span data-ttu-id="058a2-115">Es una práctica recomendada asegurarse de que el administrador de Office 365 también tiene el permiso SUPER configurado en [!INCLUDE[prodshort](includes/prodshort.md)], ya que esto facilita muchas tareas administrativas, incluida la configuración de la integración con otras aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="058a2-115">It's a best practice to make sure that the Office 365 administrator also has the SUPER permission set in [!INCLUDE[prodshort](includes/prodshort.md)] because that makes many administrative tasks easier, including setting up integration with other apps.</span></span>

### <a name="users-of-on-premises-deployments"></a><span data-ttu-id="058a2-116">Usuarios de las implementaciones locales</span><span class="sxs-lookup"><span data-stu-id="058a2-116">Users of on-premises deployments</span></span>

<span data-ttu-id="058a2-117">Para las implementaciones locales de [!INCLUDE[d365fin](includes/d365fin_md.md)], el administrador puede elegir entre diferentes mecanismos de autorización de credenciales para los usuarios.</span><span class="sxs-lookup"><span data-stu-id="058a2-117">For on-premises deployments of [!INCLUDE[d365fin](includes/d365fin_md.md)], the administrator can choose between different credential authorization mechanisms for users.</span></span> <span data-ttu-id="058a2-118">Cuando cree un usuario, proporcione información distinta según el tipo de credencial que vaya a utilizar en la sesión específica de [!INCLUDE[server](includes/server.md)].</span><span class="sxs-lookup"><span data-stu-id="058a2-118">Then, when you create a user, you provide different information depending on the credential type that you are using in the specific [!INCLUDE[server](includes/server.md)] instance.</span></span> <span data-ttu-id="058a2-119">Para obtener más información, vea [Tipos de autenticación y credenciales](/dynamics365/business-central/dev-itpro/administration/users-credential-types) en la sección Administración del desarrollador y contenido de ITPro de [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="058a2-119">For more information, see the [Authentication and Credential Types](/dynamics365/business-central/dev-itpro/administration/users-credential-types) in the Administration section of the developer and ITPro content for [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>  

## <a name="profiles"></a><span data-ttu-id="058a2-120">Perfiles</span><span class="sxs-lookup"><span data-stu-id="058a2-120">Profiles</span></span>

<span data-ttu-id="058a2-121">La personas de su empresa que tienen acceso a [!INCLUDE[d365fin](includes/d365fin_md.md)] tienen asignado un *perfil* que les da acceso a un *Área de trabajo*.</span><span class="sxs-lookup"><span data-stu-id="058a2-121">The people in your company who have access to [!INCLUDE[d365fin](includes/d365fin_md.md)] are all assigned a *profile* that gives them access to a *Role Center*.</span></span>

<span data-ttu-id="058a2-122">Los perfiles son colecciones de usuarios de [!INCLUDE[d365fin](includes/d365fin_md.md)] que comparten la misma área de trabajo.</span><span class="sxs-lookup"><span data-stu-id="058a2-122">Profiles are collections of [!INCLUDE[d365fin](includes/d365fin_md.md)] users who share the same Role Center.</span></span> <span data-ttu-id="058a2-123">Un área de trabajo es el punto de entrada y la página de inicio de [!INCLUDE[d365fin](includes/d365fin_md.md)] que le da acceso rápido a sus tareas más importantes y le muestra varias perspectivas e indicadores de rendimiento clave (KPI) sobre su trabajo.</span><span class="sxs-lookup"><span data-stu-id="058a2-123">A Role Center is the entry point and home page for [!INCLUDE[d365fin](includes/d365fin_md.md)] that gives you quick access to your most important tasks and displays various insights and key performance indicators (KPIs) about your work.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="058a2-124">En la versión actual de [!INCLUDE[d365fin](includes/d365fin_md.md)] en línea, no puede agregar, editar, o eliminar perfiles.</span><span class="sxs-lookup"><span data-stu-id="058a2-124">In the current version of [!INCLUDE[d365fin](includes/d365fin_md.md)] online, you cannot add, edit, or delete profiles.</span></span>  

### <a name="CreateProfile"></a><span data-ttu-id="058a2-125">Cree un perfil.</span><span class="sxs-lookup"><span data-stu-id="058a2-125">Create a profile</span></span>

1.  <span data-ttu-id="058a2-126">Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Lista de perfiles** y, a continuación, seleccione el vínculo relacionado.</span><span class="sxs-lookup"><span data-stu-id="058a2-126">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Profile List**, and then choose the related link.</span></span>  

2.  <span data-ttu-id="058a2-127">En la página **Lista de perfiles**, seleccione la acción **Nuevo** para abrir la página **Nueva ficha de perfil**.</span><span class="sxs-lookup"><span data-stu-id="058a2-127">On the **Profile List** page, choose the **New** action to open the **New Profile Card** page.</span></span>  

3.  <span data-ttu-id="058a2-128">En el campo **Id. perfil**, escriba un nombre que describa el rol previsto de los usuarios.</span><span class="sxs-lookup"><span data-stu-id="058a2-128">In the **Profile ID** field, enter a name that describes the intended role of the users.</span></span>  

4.  <span data-ttu-id="058a2-129">En el campo **Descripción**, escriba una descripción del identificador de perfil, como por ejemplo, **Procesador de pedidos**.</span><span class="sxs-lookup"><span data-stu-id="058a2-129">In the **Description** field, enter a description of the Profile ID, for example, **Order Processor**.</span></span>  

5.  <span data-ttu-id="058a2-130">Establezca el campo **Id. área de trabajo** al área de trabajo que desea asignar al perfil.</span><span class="sxs-lookup"><span data-stu-id="058a2-130">Set the **Role Center ID** field to the Role Center that you want to assign to the profile.</span></span>  

<span data-ttu-id="058a2-131">El procedimiento para modificar un perfil existente es el mismo, excepto que se selecciona un perfil existente en la página de perfiles **Lista de perfiles** en lugar de elegir la acción **Nuevo**.</span><span class="sxs-lookup"><span data-stu-id="058a2-131">The procedure for modifying an existing profile is the same, except you select an existing profile on the **Profile List** page instead of choosing the **New** action.</span></span>  


### <a name="copy-a-profile"></a><span data-ttu-id="058a2-132">Copiar un perfil</span><span class="sxs-lookup"><span data-stu-id="058a2-132">Copy a profile</span></span>
<span data-ttu-id="058a2-133">Copiar un perfil puede ahorrarle tiempo si desea utilizar una configuración similar en un perfil y solo desea modificar algunos ajustes.</span><span class="sxs-lookup"><span data-stu-id="058a2-133">Copying a profile can save you time if you want to use similar settings on a profile and you only want to change a few settings.</span></span>

1.  <span data-ttu-id="058a2-134">Abra el perfil que desea copiar y elija la acción **Copiar perfil**.</span><span class="sxs-lookup"><span data-stu-id="058a2-134">Open the profile that you want to copy, and then choose the **Copy Profile** action.</span></span>

2.  <span data-ttu-id="058a2-135">En el campo **Nuevo id. de perfil**, introduzca el nombre del perfil que desea copiar.</span><span class="sxs-lookup"><span data-stu-id="058a2-135">In **New Profile ID** field, enter a name for the profile that you want to copy.</span></span>

3.  <span data-ttu-id="058a2-136">Establezca el campo **Nuevo ámbito de perfil** en una de las siguientes opciones:</span><span class="sxs-lookup"><span data-stu-id="058a2-136">Set the **New Profile Scope** field to one of the following:</span></span>

    - <span data-ttu-id="058a2-137">**Sistema** para hacer que el nuevo perfil esté disponible para todas las bases de datos de inquilinos que usan la aplicación.</span><span class="sxs-lookup"><span data-stu-id="058a2-137">**System** to make the new profile available to all tenant databases that use the application.</span></span>
    - <span data-ttu-id="058a2-138">**Suscriptor** para hacer que el nuevo perfil esté disponible para la base de datos actual del suscriptor.</span><span class="sxs-lookup"><span data-stu-id="058a2-138">**Tenant** to make the new profile available to just the current tenant database.</span></span>
4. <span data-ttu-id="058a2-139">Cuando haya finalizado, elija el botón **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="058a2-139">Choose the **OK** button when done.</span></span>

### <a name="ExportImportProfile"></a><span data-ttu-id="058a2-140">Exportar e importar perfiles</span><span class="sxs-lookup"><span data-stu-id="058a2-140">Export and import profiles</span></span>

<span data-ttu-id="058a2-141">Puede exportar e importar perfiles como archivos XML a o desde la base de datos de [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="058a2-141">You can export and import profiles as XML files to and from the a [!INCLUDE[d365fin](includes/d365fin_md.md)] database.</span></span> <span data-ttu-id="058a2-142">La exportación e importación de un perfil puede ahorrarle tiempo al configurar la interfaz de usuario porque reutiliza una configuración de perfil existente en lugar de tener que configurar un perfil desde cero.</span><span class="sxs-lookup"><span data-stu-id="058a2-142">Exporting and importing a profile can save you time when configuring the user interface because you reuse an existing profile configuration instead of having to configure a profile from scratch.</span></span> <span data-ttu-id="058a2-143">Si tiene un perfil configurado en una base de datos de [!INCLUDE[d365fin](includes/d365fin_md.md)] y desea reutilizar todas o algunas de las mismas configuraciones de perfil en otra base de datos, puede exportar el perfil a un archivo XML.</span><span class="sxs-lookup"><span data-stu-id="058a2-143">If you have a profile that is configured in a [!INCLUDE[d365fin](includes/d365fin_md.md)] database and you would like to reuse all or some of the same profile configurations in another database, you can export the profile to an XML file.</span></span> <span data-ttu-id="058a2-144">A continuación, puede importar el archivo XML de perfil a otra base de datos.</span><span class="sxs-lookup"><span data-stu-id="058a2-144">Then, you can import the profile XML file into the other database.</span></span>

-   <span data-ttu-id="058a2-145">Para exportar un perfil, puede elegir la acción **Exportar perfiles** en la página **Lista de perfiles** o **Ficha de perfil**, o puede buscar y abrir la página **Exportar perfiles**.</span><span class="sxs-lookup"><span data-stu-id="058a2-145">To export a profile, you can either choose the **Export Profiles** action from the **Profile List** or **Profile Card** page or you can search for and open the **Export Profiles** page.</span></span> <span data-ttu-id="058a2-146">Guarde el archivo XML en una ubicación del equipo o red.</span><span class="sxs-lookup"><span data-stu-id="058a2-146">Save the XML file to a location on your computer or network.</span></span>

-   <span data-ttu-id="058a2-147">Para importar un perfil, puede elegir la acción **Importar perfil** en la página **Lista de perfiles** o puede buscar y abrir la página **Importar perfiles**.</span><span class="sxs-lookup"><span data-stu-id="058a2-147">To import a profile, you can either choose the **Import Profile** action from the **Profile List** page, or you can search for and open the **Import Profiles** page.</span></span> 

    > [!NOTE]  
    >  <span data-ttu-id="058a2-148">No puede importar un perfil que ya exista en la base de datos, aunque nombre o el contenido del archivo XML sean distintos.</span><span class="sxs-lookup"><span data-stu-id="058a2-148">You cannot import a profile that already exists in the database, even though the XML file is named differently or has different content.</span></span> <span data-ttu-id="058a2-149">Debe eliminar el perfil existente para poder importar el perfil nuevo.</span><span class="sxs-lookup"><span data-stu-id="058a2-149">You must delete the existing profile before you can import the new profile.</span></span>


## <a name="configuration-and-personalization"></a><span data-ttu-id="058a2-150">Configuración y personalización</span><span class="sxs-lookup"><span data-stu-id="058a2-150">Configuration and Personalization</span></span>
<!--The concept of UI customization in [!INCLUDE[d365fin](includes/d365fin_md.md)] is divided in two:  

-   Configuration, performed by the administrator  

-   Personalization, performed by users  

The administrator configures the user interface for multiple users by customizing the user interface for a profile that the users are assigned to.  -->

<span data-ttu-id="058a2-151">Los usuarios personalizan la interfaz de usuario de su versión personal mediante la adaptación de la IU en su propio inicio de sesión de usuario.</span><span class="sxs-lookup"><span data-stu-id="058a2-151">Users personalize the user interface of their personal version by customizing the user interface under their own user logon.</span></span> <span data-ttu-id="058a2-152">Esta personalización puede ser eliminada por el administrador.</span><span class="sxs-lookup"><span data-stu-id="058a2-152">This personalization can be deleted by the administrator.</span></span> <span data-ttu-id="058a2-153">Para obtener más información, vea [Personalización del área de trabajo](ui-personalization-user.md).</span><span class="sxs-lookup"><span data-stu-id="058a2-153">For more information, see [Personalizing Your Workspace](ui-personalization-user.md).</span></span>  

## <a name="see-also"></a><span data-ttu-id="058a2-154">Consulte también</span><span class="sxs-lookup"><span data-stu-id="058a2-154">See Also</span></span>  
[<span data-ttu-id="058a2-155">Gestionar usuarios y permisos</span><span class="sxs-lookup"><span data-stu-id="058a2-155">Managing Users and Permissions</span></span>](ui-how-users-permissions.md)  
[<span data-ttu-id="058a2-156">Administrar la personalización como administrador</span><span class="sxs-lookup"><span data-stu-id="058a2-156">Managing Personalization as an Administrator</span></span>](ui-personalization-manage.md)  
[<span data-ttu-id="058a2-157">Personalización de su área de trabajo</span><span class="sxs-lookup"><span data-stu-id="058a2-157">Personalizing Your Workspace</span></span>](ui-personalization-user.md)  

