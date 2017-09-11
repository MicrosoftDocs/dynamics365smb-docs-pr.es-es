---
title: "Configurar la extensión Códigos postales de Reino Unido de GetAddress.io | Documentos de Microsoft"
description: Describe la funcionalidad general que se utiliza para interactuar con los datos en Financials, como introducir valores, ordenar datos y cambiar de vista.
services: project-madeira
documentationcenter: 
author: bholtorf
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: getaddress.io, postcodes, extension
ms.date: 06/02/2017
ms.author: bholtorf
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: c5a99f7a90b2f832bba3eb088d0faa7514c14708
ms.contentlocale: es-es
ms.lasthandoff: 09/11/2017

---
# <a name="how-to-set-up-the-getaddressio-uk-postcodes-extension"></a><span data-ttu-id="b504a-103">Configurar la extensión Códigos postales de Reino Unido de GetAddress.io</span><span class="sxs-lookup"><span data-stu-id="b504a-103">How to: Set Up the GetAddress.io UK Postcodes Extension</span></span>
<span data-ttu-id="b504a-104">Esta extensión facilita la introducción de direcciones del Reino Unido de entidades como clientes, contactos, empleados, proveedores, bancos, etc.</span><span class="sxs-lookup"><span data-stu-id="b504a-104">This extension makes it easy to enter addresses in the UK for entities like customers, contacts, employees, vendors, bank accounts, and so on.</span></span> 

<span data-ttu-id="b504a-105">La extensión Códigos postales de Reino Unido de GetAddress.io utiliza la API de getAddress para buscar direcciones en códigos postales en el Reino Unido.</span><span class="sxs-lookup"><span data-stu-id="b504a-105">The GetAddress.io UK Postcodes extension uses the getAddress API to find addresses in postcodes in the UK.</span></span> <span data-ttu-id="b504a-106">Para usar la extensión, deberá obtener un plan y una clave para la API de getAddress.</span><span class="sxs-lookup"><span data-stu-id="b504a-106">To use the extension, you need to get a plan and an API Key for the getAddress API.</span></span> <span data-ttu-id="b504a-107">Es fácil y le ayudamos a hacerlo cuando configure la extensión Códigos postales de Reino Unido de GetAddress.io.</span><span class="sxs-lookup"><span data-stu-id="b504a-107">That's easy, and we help you do that when you set up the GetAddress.io UK Postcodes extension.</span></span> <span data-ttu-id="b504a-108">Los planes se basan en el uso, o lo que a veces se denominan llamadas.</span><span class="sxs-lookup"><span data-stu-id="b504a-108">Plans are based on use, or what's sometimes referred to as calls.</span></span> <span data-ttu-id="b504a-109">Una llamada, en este caso, se produce cuando [!INCLUDE[d365fin](includes/d365fin_md.md)] muestra una lista de direcciones de un código postal.</span><span class="sxs-lookup"><span data-stu-id="b504a-109">A call, in this case, is when [!INCLUDE[d365fin](includes/d365fin_md.md)] displays a list of addresses in a postcode.</span></span> <span data-ttu-id="b504a-110">Dependiendo de la frecuencia con que agregue direcciones, seleccione el plan que le resulte más adecuado.</span><span class="sxs-lookup"><span data-stu-id="b504a-110">Depending on how often you add addresses, choose the plan that is best for you.</span></span> <span data-ttu-id="b504a-111">Si solo elige **Obtener clave de API** en la página, utilizará el plan **Gratuitos**, que permite añadir 20 direcciones al día y es válido durante 30 días.</span><span class="sxs-lookup"><span data-stu-id="b504a-111">If you just choose **Get API Key** in the page, you'll use the **Free** plan, which lets you add 20 addresses per day, and is valid for 30 days.</span></span> 

##<a name="to-set-up-the-getaddressio-uk-postcodes-extension"></a><span data-ttu-id="b504a-112">Para configurar la extensión Códigos postales de Reino Unido de GetAddress.io</span><span class="sxs-lookup"><span data-stu-id="b504a-112">To set up the GetAddress.io UK Postcodes extension</span></span> 
1. <span data-ttu-id="b504a-113">Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Conexiones de servicio** y, a continuación, seleccione el vínculo relacionado.</span><span class="sxs-lookup"><span data-stu-id="b504a-113">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Service Connections**, and then choose the related link.</span></span>  
2. <span data-ttu-id="b504a-114">En la ventana **Conexiones de servicio**, elija **Servicio de códigos postales de Reino Unido**.</span><span class="sxs-lookup"><span data-stu-id="b504a-114">In the **Service Connections** window, choose **UK Postcode Service**.</span></span>
3. <span data-ttu-id="b504a-115">En la página **Configuración de proveedor de códigos postales**, elija **Desactivado**.</span><span class="sxs-lookup"><span data-stu-id="b504a-115">In the **Postcode provider configuration** page, choose **Disabled**.</span></span>
4. <span data-ttu-id="b504a-116">En la ventana **Selección de servicio de código postal**, elija **GetAddress.io**.</span><span class="sxs-lookup"><span data-stu-id="b504a-116">In the **Postal code service selection** window, choose **GetAddress.io**.</span></span>
5. <span data-ttu-id="b504a-117">En la ventana **Configuración de GetAddress.io**, elija **Obtener clave de API** para abrir la página **Planes** en el sitio web de la API de getAddress.</span><span class="sxs-lookup"><span data-stu-id="b504a-117">In the **GetAddress.io Config** window, choose **Get API Key** to open the **Plans** page on the website for the getAddress API.</span></span>  

    > [!NOTE]  
>   <span data-ttu-id="b504a-118">Puede que sea necesario permitir las ventanas emergentes en el explorador.</span><span class="sxs-lookup"><span data-stu-id="b504a-118">You might need to allow pop-ups in your browser.</span></span>
6. <span data-ttu-id="b504a-119">Compre un plan, o elija **Obtener clave de API** y proporcione la dirección de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="b504a-119">Purchase a plan, or just choose **Get API Key**, and then provide your email address.</span></span>
7. <span data-ttu-id="b504a-120">Abra el correo electrónico de getAddress.io y copie la clave de API.</span><span class="sxs-lookup"><span data-stu-id="b504a-120">Open the email from getAddress.io, and copy the API key.</span></span> <span data-ttu-id="b504a-121">La clave se encuentra en el encabezado **Su clave de API**.</span><span class="sxs-lookup"><span data-stu-id="b504a-121">The key is under the **Your API Key** heading.</span></span>
8. <span data-ttu-id="b504a-122">En la ventana **Configuración de GetAddress.io**, pegue la clave de API en el campo **Clave de API** y, a continuación, elija **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="b504a-122">In the **GetAddress.io Config** window, paste the API key in the **API Key** field, and then choose **OK**.</span></span>
9. <span data-ttu-id="b504a-123">En la página **Conexiones de servicio**, compruebe que el campo **Proveedor de direcciones** muestra **GetAddress.io**.</span><span class="sxs-lookup"><span data-stu-id="b504a-123">In the **Service Connections** page, verify that the **Address Provider** field shows **GetAddress.io**.</span></span> <span data-ttu-id="b504a-124">Si es así, el servicio está habilitado.</span><span class="sxs-lookup"><span data-stu-id="b504a-124">If it does, the service is enabled.</span></span>

## <a name="see-also"></a><span data-ttu-id="b504a-125">Consulte también</span><span class="sxs-lookup"><span data-stu-id="b504a-125">See Also</span></span>
<span data-ttu-id="b504a-126">[Códigos postales de Reino Unido de GetAddress.io](ui-extensions-getaddressio.md)
[Personalizar [!INCLUDE[d365fin](includes/d365fin_md.md)] con extensiones](ui-extensions.md)</span><span class="sxs-lookup"><span data-stu-id="b504a-126">[GetAddress.io UK Postcodes](ui-extensions-getaddressio.md)
[Customizing [!INCLUDE[d365fin](includes/d365fin_md.md)] Using Extensions](ui-extensions.md)</span></span>  
<span data-ttu-id="b504a-127">[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="b504a-127">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
