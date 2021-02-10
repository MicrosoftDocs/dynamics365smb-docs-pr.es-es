---
title: Solución de problemas del hub de empresas
description: Obtenga información sobre cómo solucionar problemas en el hub de empresas de Dynamics 365 Business Central.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: accountant, accounting, troubleshoot
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 3f348de3e8116efd789f85f1b011ecc7013bf2b1
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/01/2020
ms.locfileid: "3927728"
---
# <a name="troubleshooting-your-company-hub"></a><span data-ttu-id="fbe68-103">Solución de problemas del hub de empresas</span><span class="sxs-lookup"><span data-stu-id="fbe68-103">Troubleshooting Your Company Hub</span></span>

<span data-ttu-id="fbe68-104">Agregar empresas al panel del hub de empresas es bastante sencillo, pero este artículo le ayudará a solucionar los problemas que puedan surgirle.</span><span class="sxs-lookup"><span data-stu-id="fbe68-104">Adding companies to the company hub dashboard is easy enough, but this article addresses issues that you may have on the way.</span></span>  

## <a name="check-errors"></a><span data-ttu-id="fbe68-105">Comprobar errores</span><span class="sxs-lookup"><span data-stu-id="fbe68-105">Check errors</span></span>

<span data-ttu-id="fbe68-106">Utilice la acción **Comprobar errores** para ver una lista de errores recientes.</span><span class="sxs-lookup"><span data-stu-id="fbe68-106">Use the **Check Errors** action to view a list of recent errors.</span></span> <span data-ttu-id="fbe68-107">Puede ver detalles adicionales de cada error y puede limpiar el registro eliminando las entradas más antiguas.</span><span class="sxs-lookup"><span data-stu-id="fbe68-107">You can see additional details for each error, and you can clean up the log by deleting older entries.</span></span>  

## <a name="connection-failed"></a><span data-ttu-id="fbe68-108">Error de conexión</span><span class="sxs-lookup"><span data-stu-id="fbe68-108">Connection failed</span></span>

<span data-ttu-id="fbe68-109">Puede haber un par de razones por las que no puede conectarse a una empresa, incluidas las siguientes:</span><span class="sxs-lookup"><span data-stu-id="fbe68-109">There can be a couple of reasons why you cannot connect to a company, including the following:</span></span>

- <span data-ttu-id="fbe68-110">La dirección URL del campo **Vínculo de entorno** no es válida</span><span class="sxs-lookup"><span data-stu-id="fbe68-110">The URL in the **Environment Link** field is not valid</span></span>  

  <span data-ttu-id="fbe68-111">Vaya a la página **Vínculos de entorno**, abra el entorno al que no puede conectarse y luego elija la acción **Probar la conexión**.</span><span class="sxs-lookup"><span data-stu-id="fbe68-111">Go to the **Environment Links** page, open the environment that you cannot connect to, and then choose the **Test the connection** action.</span></span>  
- <span data-ttu-id="fbe68-112">La empresa del cliente está actualmente fuera de línea, por ejemplo, si se está actualizando</span><span class="sxs-lookup"><span data-stu-id="fbe68-112">The client's company is currently offline, for example if it being upgraded</span></span>

  <span data-ttu-id="fbe68-113">En el escritorio, seleccione el elemento de menú **Herramientas** y, a continuación, elija **Comprobar errores**.</span><span class="sxs-lookup"><span data-stu-id="fbe68-113">In your dashboard, choose the **Tools** menu item, and then choose **Check Errors**.</span></span> <span data-ttu-id="fbe68-114">De esta manera se abrirá una lista con detalles técnicos, por lo que es posible que desee ponerse en contacto con su administrador si encuentra errores.</span><span class="sxs-lookup"><span data-stu-id="fbe68-114">This opens a list with technical details, so you might want to contact your administrator if you're seeing errors.</span></span> <span data-ttu-id="fbe68-115">Por ejemplo, el mensaje de error "*El servidor ha rechazado las credenciales del cliente*" sugiere que no tiene acceso.</span><span class="sxs-lookup"><span data-stu-id="fbe68-115">For example, the error message "*The server has rejected the client credentials*" suggests that you do not have access.</span></span>  
- <span data-ttu-id="fbe68-116">No tiene acceso a todas las empresas del entorno a las que intenta conectarse</span><span class="sxs-lookup"><span data-stu-id="fbe68-116">You do not have access to all companies in the environment that you are trying to connect to</span></span>

  <span data-ttu-id="fbe68-117">En [!INCLUDE [prodshort](includes/prodshort.md)], una organización puede tener varias unidades denominadas empresas y es posible que no tenga acceso a todas las empresas.</span><span class="sxs-lookup"><span data-stu-id="fbe68-117">In [!INCLUDE [prodshort](includes/prodshort.md)], an organization can have multiple business units called companies, and you might not have access to all companies.</span></span> <span data-ttu-id="fbe68-118">Trabaje con su administrador o cliente para asegurarse de que tiene acceso a las empresas en las que quiere trabajar.</span><span class="sxs-lookup"><span data-stu-id="fbe68-118">Work with your administrator or client to make sure that you have access to the companies that you have to work in.</span></span>  

## <a name="data-does-not-refresh"></a><span data-ttu-id="fbe68-119">Los datos no se actualizan</span><span class="sxs-lookup"><span data-stu-id="fbe68-119">Data does not refresh</span></span>

<span data-ttu-id="fbe68-120">Cuando agrega una empresa o solicita una actualización de los datos, [!INCLUDE [prodshort](includes/prodshort.md)] busca los datos.</span><span class="sxs-lookup"><span data-stu-id="fbe68-120">When you add a company or request a refresh of the data, [!INCLUDE [prodshort](includes/prodshort.md)] fetches the data.</span></span> <span data-ttu-id="fbe68-121">Pero debe actualizar la página por sí mismo, como mediante la acción **Recargar todas las empresas**, actualice la página del navegador, salga del panel de control y luego vuelva allí, o alguna acción similar.</span><span class="sxs-lookup"><span data-stu-id="fbe68-121">But you must refresh the page yourself, such as choosing the **Reload all companies** action, refresh the browser page, navigate away from the dashboard and then back again, or similar.</span></span>  

<span data-ttu-id="fbe68-122">Si ha agregado una empresa, pero no se muestra en la lista, también puede usar la acción **Recargar todas las empresas** para actualizar la lista.</span><span class="sxs-lookup"><span data-stu-id="fbe68-122">If you've added a company but it is not displaying in the list, you can also use the **Reload all companies** action to update the list.</span></span>

## <a name="see-also"></a><span data-ttu-id="fbe68-123">Consulte también .</span><span class="sxs-lookup"><span data-stu-id="fbe68-123">See also</span></span>

[<span data-ttu-id="fbe68-124">Administrar el trabajo de varias empresas en el hub de empresas</span><span class="sxs-lookup"><span data-stu-id="fbe68-124">Manage Work across Multiple Companies in the Company Hub</span></span>](company-hub.md)  
[<span data-ttu-id="fbe68-125">Agregar empresas al hub de empresas</span><span class="sxs-lookup"><span data-stu-id="fbe68-125">Add companies to your company hub</span></span>](company-hub-add-company.md)  
[<span data-ttu-id="fbe68-126">Experiencias contables en Business Central</span><span class="sxs-lookup"><span data-stu-id="fbe68-126">Accountant Experiences in Business Central</span></span>](finance-accounting.md)  