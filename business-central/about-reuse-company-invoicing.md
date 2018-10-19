---
title: Uso de Invoicing y Business Central | Documentos de Microsoft
description: "Solución para tener acceso a Microsoft Invoicing cuando se ha registrado en Dynamics 365 Business Central."
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 917887deae163a76b233e1635344e537806f6215
ms.contentlocale: es-es
ms.lasthandoff: 09/28/2018

---
# <a name="using-the-same-office-365-account-in-included365finincludesd365finlongmdmd-and-microsoft-invoicing"></a><span data-ttu-id="6bd02-103">Con la misma cuenta de Office 365 en [!INCLUDE[d365fin](includes/d365fin_long_md.md)] y Microsoft Invoicing</span><span class="sxs-lookup"><span data-stu-id="6bd02-103">Using the same Office 365 Account in [!INCLUDE[d365fin](includes/d365fin_long_md.md)] and Microsoft Invoicing</span></span>
<span data-ttu-id="6bd02-104">Cuando se registra en una prueba en [!INCLUDE[d365fin](includes/d365fin_md.md)], puede cambiar a una fase de evaluación de 30 días, puede empezar una suscripción o bien puede dejar de usar [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="6bd02-104">When you sign up for a trial with [!INCLUDE[d365fin](includes/d365fin_md.md)], you can move to a 30-day evaluation phase, you can start a subscription, or you can stop using [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="6bd02-105">En todos los casos, si inicia sesión en el portal de Office, es posible que vea un mosaico llamado **Centro de Empresa** y que haga clic en él.</span><span class="sxs-lookup"><span data-stu-id="6bd02-105">In all cases, if you log into the Office Portal, you might see a tile called **Business center** and click it.</span></span> <span data-ttu-id="6bd02-106">Forma parte de la suscripción de Office 365, por lo que no todos los usuarios verán ese mosaico en el portal de Office.</span><span class="sxs-lookup"><span data-stu-id="6bd02-106">This is part of the Office 365 Business Premium subscription, so not everyone will see that tile in the Office Portal.</span></span>  

<span data-ttu-id="6bd02-107">Si tiene acceso al centro de Empresa, aparecerá una sección denominada **Facturación**.</span><span class="sxs-lookup"><span data-stu-id="6bd02-107">If you do access the Business center, you will see a section called **Invoicing**.</span></span> <span data-ttu-id="6bd02-108">Si obtiene acceso a esa sección, verá un mensaje que le indica que no puede tener acceso a Microsoft Invoicing porque la cuenta se utiliza en [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="6bd02-108">If you access that section, you will see a message that you cannot access Microsoft Invoicing because your account is used in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>  

<span data-ttu-id="6bd02-109">Se muestra un mensaje similar si instala la aplicación móvil de Invoicing.</span><span class="sxs-lookup"><span data-stu-id="6bd02-109">You see a similar message if you install the mobile app for Invoicing.</span></span>  

## <a name="workaround"></a><span data-ttu-id="6bd02-110">Solución</span><span class="sxs-lookup"><span data-stu-id="6bd02-110">Workaround</span></span>
<span data-ttu-id="6bd02-111">Invoicing y [!INCLUDE[d365fin](includes/d365fin_md.md)] tienen una plataforma compartida.</span><span class="sxs-lookup"><span data-stu-id="6bd02-111">Invoicing and [!INCLUDE[d365fin](includes/d365fin_md.md)] have a shared platform.</span></span> <span data-ttu-id="6bd02-112">Esto significa que se le reconoce como un usuario existente de [!INCLUDE[d365fin](includes/d365fin_md.md)] al hacer clic en Invoicing en el centro de Empresa.</span><span class="sxs-lookup"><span data-stu-id="6bd02-112">That means that you are recognized as an existing user of [!INCLUDE[d365fin](includes/d365fin_md.md)] when you click Invoicing in the Business center.</span></span> <span data-ttu-id="6bd02-113">La razón es que Invoicing no puede utilizar la misma empresa que [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="6bd02-113">The reason is that Invoicing cannot use the same company as [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>  

<span data-ttu-id="6bd02-114">Por lo tanto, tendrá que iniciar sesión en [!INCLUDE[d365fin](includes/d365fin_md.md)] y cambiar el nombre de su empresa existente, y después crear una empresa nueva que pueda utilizarse en Invoicing.</span><span class="sxs-lookup"><span data-stu-id="6bd02-114">So you will have to log into [!INCLUDE[d365fin](includes/d365fin_md.md)] and rename your existing company, and then create a new company that you can then use in Invoicing.</span></span> <span data-ttu-id="6bd02-115">No se mueven ni sobrescriben datos durante esta solución.</span><span class="sxs-lookup"><span data-stu-id="6bd02-115">No data is moved or overwritten during this workaround.</span></span>

### <a name="to-rename-your-company"></a><span data-ttu-id="6bd02-116">Para cambiar el nombre de su empresa</span><span class="sxs-lookup"><span data-stu-id="6bd02-116">To rename your company</span></span>
1.  <span data-ttu-id="6bd02-117">Inicie sesión en su [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="6bd02-117">Sign in to your [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>  
2.  <span data-ttu-id="6bd02-118">Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Empresas** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="6bd02-118">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Companies**, and then choose the related link.</span></span>  
3.  <span data-ttu-id="6bd02-119">En la ventana **Empresas**, seleccione el botón **Editar lista**.</span><span class="sxs-lookup"><span data-stu-id="6bd02-119">In the **Companies** window, choose the **Edit List** button.</span></span>  
4.  <span data-ttu-id="6bd02-120">Cambiar el nombre de la entrada *Mi empresa* por otro distinto.</span><span class="sxs-lookup"><span data-stu-id="6bd02-120">Change the name of the *My Company* entry to something else.</span></span>  

    <span data-ttu-id="6bd02-121">Espere unos minutos.</span><span class="sxs-lookup"><span data-stu-id="6bd02-121">Wait a number of minutes.</span></span> <span data-ttu-id="6bd02-122">Realizaremos varios cambios en la base de datos subyacente y este proceso suele llevar un tiempo.</span><span class="sxs-lookup"><span data-stu-id="6bd02-122">We’ll be making a number of changes in the underlying database, and that takes a while.</span></span>
5.  <span data-ttu-id="6bd02-123">Cuando el sistema está preparado de nuevo, elija el botón **Crear nueva empresa**.</span><span class="sxs-lookup"><span data-stu-id="6bd02-123">When the system is ready again, choose the **Create New Company** button.</span></span>  
6.  <span data-ttu-id="6bd02-124">En el cuadro de diálogo que aparece, especifique el nombre como *Mi empresa* y elija la opción **Producción - Solo datos de configuración**.</span><span class="sxs-lookup"><span data-stu-id="6bd02-124">In the dialog that appears, specify the name as *My Company*, and choose the **Production – Setup Data Only** option.</span></span>  

<span data-ttu-id="6bd02-125">Esto tarda de nuevo varios minutos.</span><span class="sxs-lookup"><span data-stu-id="6bd02-125">This again takes a number of minutes.</span></span> <span data-ttu-id="6bd02-126">Cuando se complete el proceso, podrá obtener acceso a Invoicing como parte de la experiencia de Office 365 Business Premium.</span><span class="sxs-lookup"><span data-stu-id="6bd02-126">When the process completes, you will be able to access Invoicing as part of your Office 365 Business Premium experience.</span></span>  

### <a name="what-about-my-data"></a><span data-ttu-id="6bd02-127">¿Qué sucede con mis datos?</span><span class="sxs-lookup"><span data-stu-id="6bd02-127">What about my data?</span></span>
<span data-ttu-id="6bd02-128">Al cambiar el nombre Mi empresa original, se cambia el nombre de las tablas de base de datos que almacenan los datos de [!INCLUDE[d365fin](includes/d365fin_md.md)] existentes, pero no se modifican los datos.</span><span class="sxs-lookup"><span data-stu-id="6bd02-128">When you rename the original My Company, the database tables that store your existing [!INCLUDE[d365fin](includes/d365fin_md.md)] data are renamed, but the data itself is not touched.</span></span>  

<span data-ttu-id="6bd02-129">Si utiliza Invoicing y [!INCLUDE[d365fin](includes/d365fin_md.md)], los datos se almacenan en los dos contenedores diferentes (las dos empresas).</span><span class="sxs-lookup"><span data-stu-id="6bd02-129">If you use both Invoicing and [!INCLUDE[d365fin](includes/d365fin_md.md)], the data is stored in two different containers (the two companies).</span></span> <span data-ttu-id="6bd02-130">No se comparte nada, por lo que tendrá que gestionar los clientes y los productos en ambas empresas.</span><span class="sxs-lookup"><span data-stu-id="6bd02-130">Nothing is shared, so you'll have to manage customers and items in both companies.</span></span>  

## <a name="see-also"></a><span data-ttu-id="6bd02-131">Consulte también</span><span class="sxs-lookup"><span data-stu-id="6bd02-131">See Also</span></span>
[<span data-ttu-id="6bd02-132">Preguntas más frecuentes</span><span class="sxs-lookup"><span data-stu-id="6bd02-132">Frequently Asked Questions</span></span>](across-faq.md)  
[<span data-ttu-id="6bd02-133">Administración</span><span class="sxs-lookup"><span data-stu-id="6bd02-133">Administration</span></span>](admin-setup-and-administration.md)  

