---
title: Usar los datos para crear una aplicación | Documentos de Microsoft
description: Puede hacer que los datos de Business Central estén disponibles como un origen de datos y especificar una URL de OData de sus servicios web para crear una aplicación empresarial con Power Apps.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: OData, Power App, SOAP
ms.date: 11/20/2019
ms.author: edupont
ms.openlocfilehash: 9cf587dca8224e742ecbde30bcabc35697bb6f2a
ms.sourcegitcommit: cfc92eefa8b06fb426482f54e393f0e6e222f712
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 12/03/2019
ms.locfileid: "2881005"
---
# <a name="connecting-to-your-business-central-data-to-build-a-business-app-using-power-apps"></a><span data-ttu-id="4cdcd-103">Cómo conectarse a sus datos de Business Central para crear una aplicación empresarial con Power Apps</span><span class="sxs-lookup"><span data-stu-id="4cdcd-103">Connecting to Your Business Central Data to Build a Business App Using Power Apps</span></span>

<span data-ttu-id="4cdcd-104">Puede convertir los datos de [!INCLUDE[prodshort](includes/prodshort.md)] en disponibles como origen de datos en Power Apps.</span><span class="sxs-lookup"><span data-stu-id="4cdcd-104">You can make your [!INCLUDE[prodshort](includes/prodshort.md)] data available as a data source in Power Apps.</span></span>  

> [!NOTE]  
> <span data-ttu-id="4cdcd-105">Debe disponer de una cuenta válida con [!INCLUDE[prodshort](includes/prodshort.md)] y con Power Apps.</span><span class="sxs-lookup"><span data-stu-id="4cdcd-105">You must have a valid account with [!INCLUDE[prodshort](includes/prodshort.md)] and with Power Apps.</span></span>  

## <a name="to-add-includeprodshortincludesprodshortmd-as-a-data-source-in-power-apps"></a><span data-ttu-id="4cdcd-106">Para agregar [!INCLUDE[prodshort](includes/prodshort.md)] como origen de datos de Power Apps</span><span class="sxs-lookup"><span data-stu-id="4cdcd-106">To add [!INCLUDE[prodshort](includes/prodshort.md)] as a data source in Power Apps</span></span>

1. <span data-ttu-id="4cdcd-107">En el explorador, vaya a [powerapps.microsoft.com](https://powerapps.microsoft.com/) y, a continuación, inicie sesión.</span><span class="sxs-lookup"><span data-stu-id="4cdcd-107">In your browser, navigate to [powerapps.microsoft.com](https://powerapps.microsoft.com/), and then sign in.</span></span>
2. <span data-ttu-id="4cdcd-108">En la página Web, elija **Aplicaciones**, **Crear una aplicación** y **Lienzo** para crear una nueva aplicación de lienzo.</span><span class="sxs-lookup"><span data-stu-id="4cdcd-108">On the Home page, choose the **Apps**, **Create an app** and **Canvas** to create a new canvas app.</span></span> <span data-ttu-id="4cdcd-109">Esta aplicación se ha diseñado para su uso en un dispositivo móvil, pero también puede seleccionar usar otra plantilla.</span><span class="sxs-lookup"><span data-stu-id="4cdcd-109">This app will be designed for use on a mobile device, but you can also choose to use another template.</span></span>

    <span data-ttu-id="4cdcd-110">El siguiente paso para crear una Power App es seleccionar los datos.</span><span class="sxs-lookup"><span data-stu-id="4cdcd-110">The next step to create a Power App is to select your data.</span></span> <span data-ttu-id="4cdcd-111">Elija el icono de flecha y la opción **Nueva conexión** en la parte superior izquierda de la página.</span><span class="sxs-lookup"><span data-stu-id="4cdcd-111">Choose the Arrow icon then choose the **New connection** option in the upper left side of the page.</span></span>
3. <span data-ttu-id="4cdcd-112">En la lista de conexiones disponibles, elija **Business Central** y, después, seleccione el botón **Crear**.</span><span class="sxs-lookup"><span data-stu-id="4cdcd-112">In the list of available connections, choose **Business Central**, and then choose the **Create** button.</span></span>

    <span data-ttu-id="4cdcd-113">Power Apps se conectará a su [!INCLUDE [prodshort](includes/prodshort.md)] con las credenciales con las que ha iniciado sesión.</span><span class="sxs-lookup"><span data-stu-id="4cdcd-113">Power Apps will connect to your [!INCLUDE [prodshort](includes/prodshort.md)] using the credentials that you are signed in with.</span></span> <span data-ttu-id="4cdcd-114">Si no es administrador de su [!INCLUDE [prodshort](includes/prodshort.md)], es posible que tenga que iniciar sesión con otra cuenta.</span><span class="sxs-lookup"><span data-stu-id="4cdcd-114">If you are not an administrator of your [!INCLUDE [prodshort](includes/prodshort.md)], you may have to sign in with another account.</span></span>  

4. <span data-ttu-id="4cdcd-115">Power Apps mostrará una lista de *ambientes y empresas* que están disponibles en [!INCLUDE [prodshort](includes/prodshort.md)].</span><span class="sxs-lookup"><span data-stu-id="4cdcd-115">Power Apps will display a list of *Environments and companies* that are available from [!INCLUDE [prodshort](includes/prodshort.md)].</span></span> <span data-ttu-id="4cdcd-116">Elija el ambiente y la empresa que contiene los datos a los que desea conectarse.</span><span class="sxs-lookup"><span data-stu-id="4cdcd-116">Choose the environment and company that contains the data you want to connect to.</span></span> <span data-ttu-id="4cdcd-117">A continuación, se le presentará una lista de API.</span><span class="sxs-lookup"><span data-stu-id="4cdcd-117">Next, you will be presented with a list of APIs.</span></span> <span data-ttu-id="4cdcd-118">Seleccione la **API** a la que desee conectarse.</span><span class="sxs-lookup"><span data-stu-id="4cdcd-118">Select the **API** you want to connect to.</span></span>

<span data-ttu-id="4cdcd-119">Estas denominadas tablas forman parte de la API de [!INCLUDE [prodshort](includes/prodshort.md)].</span><span class="sxs-lookup"><span data-stu-id="4cdcd-119">These so-called tables are part of the [!INCLUDE [prodshort](includes/prodshort.md)] API.</span></span> <span data-ttu-id="4cdcd-120">No es necesario que configure los extremos usted mismo, el conector de [!INCLUDE [prodshort](includes/prodshort.md)] para Power Apps hacerlo de forma automática.</span><span class="sxs-lookup"><span data-stu-id="4cdcd-120">You do not have to configure the end points yourself - the [!INCLUDE [prodshort](includes/prodshort.md)] connector for Power Apps does it for you.</span></span>  

> [!NOTE]
> <span data-ttu-id="4cdcd-121">Si desea incluir datos de otras tablas en [!INCLUDE [prodshort](includes/prodshort.md)] en su aplicación, debe trabajar con un desarrollador para definir una API personalizada en [!INCLUDE [prodshort](includes/prodshort.md)] y, después, consumir esa API personalizada a través de un conector personalizado en Power Apps.</span><span class="sxs-lookup"><span data-stu-id="4cdcd-121">If you want to include data from other tables in [!INCLUDE [prodshort](includes/prodshort.md)] in your app, then you must work with a developer to define a custom API in [!INCLUDE [prodshort](includes/prodshort.md)] and then consume that custom API through a custom connector in Power Apps.</span></span> <span data-ttu-id="4cdcd-122">Para obtener más información, vea [Crear un conector personalizado desde cero](/connectors/custom-connectors/define-blank).</span><span class="sxs-lookup"><span data-stu-id="4cdcd-122">For more information, see [Create a custom connector from scratch](/connectors/custom-connectors/define-blank).</span></span>  

<span data-ttu-id="4cdcd-123">Ya se ha conectado correctamente con los datos de [!INCLUDE [prodshort](includes/prodshort.md)] y está preparado para comenzar a crear su PowerApp.</span><span class="sxs-lookup"><span data-stu-id="4cdcd-123">At this point, you have successfully connected to your [!INCLUDE [prodshort](includes/prodshort.md)] data and are ready to begin building your PowerApp.</span></span> <span data-ttu-id="4cdcd-124">Puede agregar pantallas adicionales y conectarse a los datos adicionales de su [!INCLUDE [prodshort](includes/prodshort.md)].</span><span class="sxs-lookup"><span data-stu-id="4cdcd-124">You can add additional screens and connect to additional data from your [!INCLUDE [prodshort](includes/prodshort.md)].</span></span> <span data-ttu-id="4cdcd-125">Para obtener más información, consulte [Crear una aplicación de lienzo a partir de una plantilla de Power Apps](/powerapps/maker/canvas-apps/get-started-test-drive).</span><span class="sxs-lookup"><span data-stu-id="4cdcd-125">For more information, see [Create a canvas app from a template in Power Apps](/powerapps/maker/canvas-apps/get-started-test-drive).</span></span>  

<span data-ttu-id="4cdcd-126">Cuando haya diseñado y creado la aplicación, puede compartirla con sus compañeros.</span><span class="sxs-lookup"><span data-stu-id="4cdcd-126">When you have designed and built your app, you can share it with your colleagues.</span></span> <span data-ttu-id="4cdcd-127">Para obtener más información, consulte [Guardar y publicar una aplicación de lienzo en Power Apps](/powerapps/maker/canvas-apps/save-publish-app).</span><span class="sxs-lookup"><span data-stu-id="4cdcd-127">For more information, see [Save and publish a canvas app in Power Apps](/powerapps/maker/canvas-apps/save-publish-app).</span></span>  

> [!NOTE]
> <span data-ttu-id="4cdcd-128">Si desea conectarse a [!INCLUDE [prodshort](includes/prodshort.md)] local, deberá elegir el conector **Business Central (local)** en el paso 3.</span><span class="sxs-lookup"><span data-stu-id="4cdcd-128">If you want to connect to [!INCLUDE [prodshort](includes/prodshort.md)] on-premises, then you must choose the **Business Central (on-premises)** connector in step 3.</span></span>  

## <a name="see-also"></a><span data-ttu-id="4cdcd-129">Consulte también</span><span class="sxs-lookup"><span data-stu-id="4cdcd-129">See Also</span></span>

[<span data-ttu-id="4cdcd-130">Crear una aplicación de lienzo a partir de una plantilla de Power Apps</span><span class="sxs-lookup"><span data-stu-id="4cdcd-130">Create a canvas app from a template in Power Apps</span></span>](/powerapps/maker/canvas-apps/get-started-test-drive)  
[<span data-ttu-id="4cdcd-131">Introducción</span><span class="sxs-lookup"><span data-stu-id="4cdcd-131">Getting Started</span></span>](product-get-started.md)  
[<span data-ttu-id="4cdcd-132">Importar datos de empresa de otros sistemas financieros</span><span class="sxs-lookup"><span data-stu-id="4cdcd-132">Importing Business Data from Other Finance Systems</span></span>](across-import-data-configuration-packages.md)  
<span data-ttu-id="4cdcd-133">[Configurar [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)</span><span class="sxs-lookup"><span data-stu-id="4cdcd-133">[Setting Up [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)</span></span>  
[<span data-ttu-id="4cdcd-134">Finanzas</span><span class="sxs-lookup"><span data-stu-id="4cdcd-134">Finance</span></span>](finance.md)  
[<span data-ttu-id="4cdcd-135">Introducción al desarrollo de aplicaciones de Connect para Dynamics 365 Business Central</span><span class="sxs-lookup"><span data-stu-id="4cdcd-135">Getting Started Developing Connect Apps for Dynamics 365 Business Central</span></span>](/dynamics365/business-central/dev-itpro/developer/devenv-develop-connect-apps)  
