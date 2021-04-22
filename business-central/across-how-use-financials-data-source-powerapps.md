---
title: Usar los datos para crear una aplicación | Documentos de Microsoft
description: Puede hacer que los datos de Business Central estén disponibles como un origen de datos y especificar una URL de OData de sus servicios web para crear una aplicación empresarial con Power Apps.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: OData, Power App, SOAP
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 25607473e20bca8cec8cd65e2e808e12dda47869
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 03/31/2021
ms.locfileid: "5774541"
---
# <a name="connecting-to-your-business-central-data-to-build-a-business-app-using-power-apps"></a><span data-ttu-id="5a76d-103">Cómo conectarse a sus datos de Business Central para crear una aplicación empresarial con Power Apps</span><span class="sxs-lookup"><span data-stu-id="5a76d-103">Connecting to Your Business Central Data to Build a Business App Using Power Apps</span></span>

<span data-ttu-id="5a76d-104">Puede convertir los datos de [!INCLUDE[prod_short](includes/prod_short.md)] en disponibles como origen de datos en Power Apps.</span><span class="sxs-lookup"><span data-stu-id="5a76d-104">You can make your [!INCLUDE[prod_short](includes/prod_short.md)] data available as a data source in Power Apps.</span></span>  

> [!NOTE]  
> <span data-ttu-id="5a76d-105">Debe disponer de una cuenta válida con [!INCLUDE[prod_short](includes/prod_short.md)] y con Power Apps.</span><span class="sxs-lookup"><span data-stu-id="5a76d-105">You must have a valid account with [!INCLUDE[prod_short](includes/prod_short.md)] and with Power Apps.</span></span>  

## <a name="to-add-prod_short-as-a-data-source-in-power-apps"></a><span data-ttu-id="5a76d-106">Para agregar [!INCLUDE[prod_short](includes/prod_short.md)] como origen de datos de Power Apps</span><span class="sxs-lookup"><span data-stu-id="5a76d-106">To add [!INCLUDE[prod_short](includes/prod_short.md)] as a data source in Power Apps</span></span>

1. <span data-ttu-id="5a76d-107">En el explorador, vaya a [powerapps.microsoft.com](https://powerapps.microsoft.com/) y, a continuación, inicie sesión.</span><span class="sxs-lookup"><span data-stu-id="5a76d-107">In your browser, navigate to [powerapps.microsoft.com](https://powerapps.microsoft.com/), and then sign in.</span></span>
2. <span data-ttu-id="5a76d-108">En la página de inicio, en la sección **Comenzar a partir de los datos**, elija la ventana **Otros orígenes de datos**.</span><span class="sxs-lookup"><span data-stu-id="5a76d-108">On the Home page, in the **Start from data** section, choose the **Other data sources** tile.</span></span>  

    <span data-ttu-id="5a76d-109">Esto abre Power Apps Studio.</span><span class="sxs-lookup"><span data-stu-id="5a76d-109">This opens Power Apps Studio.</span></span> <span data-ttu-id="5a76d-110">En el primer inicio de sesión, debe especificar el país y la región.</span><span class="sxs-lookup"><span data-stu-id="5a76d-110">On first login, you must specify the country/region.</span></span>  
3. <span data-ttu-id="5a76d-111">En la lista de conexiones disponibles, elija **Business Central** y, después, seleccione el botón **Crear**.</span><span class="sxs-lookup"><span data-stu-id="5a76d-111">In the list of available connections, choose **Business Central**, and then choose the **Create** button.</span></span>

    <span data-ttu-id="5a76d-112">Power Apps se conectará a su [!INCLUDE[prod_short](includes/prod_short.md)] con las credenciales con las que ha iniciado sesión.</span><span class="sxs-lookup"><span data-stu-id="5a76d-112">Power Apps will connect to your [!INCLUDE[prod_short](includes/prod_short.md)] using the credentials that you are signed in with.</span></span> <span data-ttu-id="5a76d-113">Si no es administrador de su [!INCLUDE[prod_short](includes/prod_short.md)], es posible que tenga que iniciar sesión con otra cuenta.</span><span class="sxs-lookup"><span data-stu-id="5a76d-113">If you are not an administrator of your [!INCLUDE[prod_short](includes/prod_short.md)], you may have to sign in with another account.</span></span>  

4. <span data-ttu-id="5a76d-114">Power Apps mostrará una lista de *ambientes y empresas* que están disponibles en [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="5a76d-114">Power Apps will display a list of *Environments and companies* that are available from [!INCLUDE[prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="5a76d-115">Elija el entorno y la empresa que contiene los datos a los que desea conectarse, como *PRODUCCIÓN - Mi empresa*.</span><span class="sxs-lookup"><span data-stu-id="5a76d-115">Choose the environment and company that contains the data you want to connect to, such as *PRODUCTION - My Company*.</span></span>  

5. <span data-ttu-id="5a76d-116">A continuación, se le presentará una lista de tablas que están expuestas como parte de la API para su entorno.</span><span class="sxs-lookup"><span data-stu-id="5a76d-116">Next, you will be presented with a list of tables that are exposed as part of the API for your environment.</span></span> <span data-ttu-id="5a76d-117">Seleccione la tabla a la que desea conectarse y luego elija **Conectar**.</span><span class="sxs-lookup"><span data-stu-id="5a76d-117">Select the table that you want to connect to, and then choose **Connect**.</span></span>

<span data-ttu-id="5a76d-118">Estas denominadas tablas están expuestas como extremos por el contector [!INCLUDE[prod_short](includes/prod_short.md)] para Power Apps.</span><span class="sxs-lookup"><span data-stu-id="5a76d-118">These so-called tables are exposed as endpoints by the [!INCLUDE[prod_short](includes/prod_short.md)] connector for Power Apps.</span></span>  

> [!NOTE]
> <span data-ttu-id="5a76d-119">Si desea incluir datos de otras tablas en [!INCLUDE[prod_short](includes/prod_short.md)] en su aplicación, debe trabajar con un desarrollador para definir una API personalizada en [!INCLUDE[prod_short](includes/prod_short.md)] y, después, consumir esa API personalizada a través de un conector personalizado en Power Apps.</span><span class="sxs-lookup"><span data-stu-id="5a76d-119">If you want to include data from other tables in [!INCLUDE[prod_short](includes/prod_short.md)] in your app, then you must work with a developer to define a custom API in [!INCLUDE[prod_short](includes/prod_short.md)] and then consume that custom API through a custom connector in Power Apps.</span></span> <span data-ttu-id="5a76d-120">Para obtener más información, vea [Crear un conector personalizado desde cero](/connectors/custom-connectors/define-blank).</span><span class="sxs-lookup"><span data-stu-id="5a76d-120">For more information, see [Create a custom connector from scratch](/connectors/custom-connectors/define-blank).</span></span>  

<span data-ttu-id="5a76d-121">Ya se ha conectado correctamente con los datos de [!INCLUDE[prod_short](includes/prod_short.md)] y está preparado para comenzar a crear su PowerApp.</span><span class="sxs-lookup"><span data-stu-id="5a76d-121">At this point, you have successfully connected to your [!INCLUDE[prod_short](includes/prod_short.md)] data and are ready to begin building your PowerApp.</span></span> <span data-ttu-id="5a76d-122">Puede agregar pantallas adicionales y conectarse a los datos adicionales de su [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="5a76d-122">You can add additional screens and connect to additional data from your [!INCLUDE[prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="5a76d-123">Para obtener más información, consulte [Crear una aplicación de lienzo a partir de un ejemplo en Power Apps](/powerapps/maker/canvas-apps/open-and-run-a-sample-app).</span><span class="sxs-lookup"><span data-stu-id="5a76d-123">For more information, see [Create a canvas app from a sample in Power Apps](/powerapps/maker/canvas-apps/open-and-run-a-sample-app).</span></span>  

<span data-ttu-id="5a76d-124">Cuando haya diseñado y creado la aplicación, puede compartirla con sus compañeros.</span><span class="sxs-lookup"><span data-stu-id="5a76d-124">When you have designed and built your app, you can share it with your colleagues.</span></span> <span data-ttu-id="5a76d-125">Para obtener más información, consulte [Guardar y publicar una aplicación de lienzo en Power Apps](/powerapps/maker/canvas-apps/save-publish-app).</span><span class="sxs-lookup"><span data-stu-id="5a76d-125">For more information, see [Save and publish a canvas app in Power Apps](/powerapps/maker/canvas-apps/save-publish-app).</span></span>  

> [!NOTE]
> <span data-ttu-id="5a76d-126">Si desea conectarse a [!INCLUDE[prod_short](includes/prod_short.md)] local, deberá elegir el conector **Business Central (local)** en el paso 3.</span><span class="sxs-lookup"><span data-stu-id="5a76d-126">If you want to connect to [!INCLUDE[prod_short](includes/prod_short.md)] on-premises, then you must choose the **Business Central (on-premises)** connector in step 3.</span></span>  

## <a name="see-also"></a><span data-ttu-id="5a76d-127">Consulte también</span><span class="sxs-lookup"><span data-stu-id="5a76d-127">See Also</span></span>

[<span data-ttu-id="5a76d-128">Crear una aplicación de lienzo a partir de una plantilla de Power Apps</span><span class="sxs-lookup"><span data-stu-id="5a76d-128">Create a canvas app from a template in Power Apps</span></span>](/powerapps/maker/canvas-apps/get-started-test-drive)  
[<span data-ttu-id="5a76d-129">Importar datos de empresa de otros sistemas financieros</span><span class="sxs-lookup"><span data-stu-id="5a76d-129">Importing Business Data from Other Finance Systems</span></span>](across-import-data-configuration-packages.md)  
<span data-ttu-id="5a76d-130">[Configurar [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md)</span><span class="sxs-lookup"><span data-stu-id="5a76d-130">[Setting Up [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md)</span></span>  
[<span data-ttu-id="5a76d-131">Introducción al desarrollo de aplicaciones de Connect para Dynamics 365 Business Central</span><span class="sxs-lookup"><span data-stu-id="5a76d-131">Getting Started Developing Connect Apps for Dynamics 365 Business Central</span></span>](/dynamics365/business-central/dev-itpro/developer/devenv-develop-connect-apps)  


[!INCLUDE[footer-include](includes/footer-banner.md)]