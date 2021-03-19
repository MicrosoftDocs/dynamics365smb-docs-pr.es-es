---
title: Solución de problemas del hub de empresas
description: Aprenda a solucionar cualquier problema cuando la empresa se concentre en Dynamics 365 Business Central para gestionar el trabajo en varias empresas.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: accountant, accounting, troubleshoot
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: d75c6ceb27c7e1ee101b23bbc18f3eac0db4ced7
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5389129"
---
# <a name="troubleshooting-your-company-hub"></a><span data-ttu-id="adfde-103">Solución de problemas del hub de empresas</span><span class="sxs-lookup"><span data-stu-id="adfde-103">Troubleshooting Your Company Hub</span></span>

<span data-ttu-id="adfde-104">Agregar empresas al panel del hub de empresas es bastante sencillo, pero este artículo le ayudará a solucionar los problemas que puedan surgirle.</span><span class="sxs-lookup"><span data-stu-id="adfde-104">Adding companies to the company hub dashboard is easy enough, but this article addresses issues that you may have on the way.</span></span>  

## <a name="check-errors"></a><span data-ttu-id="adfde-105">Comprobar errores</span><span class="sxs-lookup"><span data-stu-id="adfde-105">Check errors</span></span>

<span data-ttu-id="adfde-106">Utilice la acción **Comprobar errores** para ver una lista de errores recientes.</span><span class="sxs-lookup"><span data-stu-id="adfde-106">Use the **Check Errors** action to view a list of recent errors.</span></span> <span data-ttu-id="adfde-107">Puede ver detalles adicionales de cada error y puede limpiar el registro eliminando las entradas más antiguas.</span><span class="sxs-lookup"><span data-stu-id="adfde-107">You can see additional details for each error, and you can clean up the log by deleting older entries.</span></span>  

## <a name="connection-failed"></a><span data-ttu-id="adfde-108">Error de conexión</span><span class="sxs-lookup"><span data-stu-id="adfde-108">Connection failed</span></span>

<span data-ttu-id="adfde-109">Puede haber un par de razones por las que no puede conectarse a una empresa, incluidas las siguientes:</span><span class="sxs-lookup"><span data-stu-id="adfde-109">There can be a couple of reasons why you cannot connect to a company, including the following:</span></span>

- <span data-ttu-id="adfde-110">La dirección URL del campo **Vínculo de entorno** no es válida</span><span class="sxs-lookup"><span data-stu-id="adfde-110">The URL in the **Environment Link** field is not valid</span></span>  

  <span data-ttu-id="adfde-111">Vaya a la página **Vínculos de entorno**, abra el entorno al que no puede conectarse y luego elija la acción **Probar la conexión**.</span><span class="sxs-lookup"><span data-stu-id="adfde-111">Go to the **Environment Links** page, open the environment that you cannot connect to, and then choose the **Test the connection** action.</span></span>  
- <span data-ttu-id="adfde-112">La empresa del cliente está actualmente fuera de línea, por ejemplo, si se está actualizando</span><span class="sxs-lookup"><span data-stu-id="adfde-112">The client's company is currently offline, for example if it being upgraded</span></span>

  <span data-ttu-id="adfde-113">En el escritorio, seleccione el elemento de menú **Herramientas** y, a continuación, elija **Comprobar errores**.</span><span class="sxs-lookup"><span data-stu-id="adfde-113">In your dashboard, choose the **Tools** menu item, and then choose **Check Errors**.</span></span> <span data-ttu-id="adfde-114">De esta manera se abrirá una lista con detalles técnicos, por lo que es posible que desee ponerse en contacto con su administrador si encuentra errores.</span><span class="sxs-lookup"><span data-stu-id="adfde-114">This opens a list with technical details, so you might want to contact your administrator if you're seeing errors.</span></span> <span data-ttu-id="adfde-115">Por ejemplo, el mensaje de error "*El servidor ha rechazado las credenciales del cliente*" sugiere que no tiene acceso.</span><span class="sxs-lookup"><span data-stu-id="adfde-115">For example, the error message "*The server has rejected the client credentials*" suggests that you do not have access.</span></span>  
- <span data-ttu-id="adfde-116">No tiene acceso a todas las empresas del entorno a las que intenta conectarse</span><span class="sxs-lookup"><span data-stu-id="adfde-116">You do not have access to all companies in the environment that you are trying to connect to</span></span>

  <span data-ttu-id="adfde-117">En [!INCLUDE [prod_short](includes/prod_short.md)], una organización puede tener varias unidades denominadas empresas y es posible que no tenga acceso a todas las empresas.</span><span class="sxs-lookup"><span data-stu-id="adfde-117">In [!INCLUDE [prod_short](includes/prod_short.md)], an organization can have multiple business units called companies, and you might not have access to all companies.</span></span> <span data-ttu-id="adfde-118">Trabaje con su administrador o cliente para asegurarse de que tiene acceso a las empresas en las que quiere trabajar.</span><span class="sxs-lookup"><span data-stu-id="adfde-118">Work with your administrator or client to make sure that you have access to the companies that you have to work in.</span></span>  

## <a name="data-does-not-refresh"></a><span data-ttu-id="adfde-119">Los datos no se actualizan</span><span class="sxs-lookup"><span data-stu-id="adfde-119">Data does not refresh</span></span>

<span data-ttu-id="adfde-120">Cuando agrega una empresa o solicita una actualización de los datos, [!INCLUDE [prod_short](includes/prod_short.md)] busca los datos.</span><span class="sxs-lookup"><span data-stu-id="adfde-120">When you add a company or request a refresh of the data, [!INCLUDE [prod_short](includes/prod_short.md)] fetches the data.</span></span> <span data-ttu-id="adfde-121">Pero debe actualizar la página por sí mismo, como mediante la acción **Recargar todas las empresas**, actualice la página del navegador, salga del panel de control y luego vuelva allí, o alguna acción similar.</span><span class="sxs-lookup"><span data-stu-id="adfde-121">But you must refresh the page yourself, such as choosing the **Reload all companies** action, refresh the browser page, navigate away from the dashboard and then back again, or similar.</span></span>  

<span data-ttu-id="adfde-122">Si ha agregado una empresa, pero no se muestra en la lista, también puede usar la acción **Recargar todas las empresas** para actualizar la lista.</span><span class="sxs-lookup"><span data-stu-id="adfde-122">If you've added a company but it is not displaying in the list, you can also use the **Reload all companies** action to update the list.</span></span>

## <a name="see-also"></a><span data-ttu-id="adfde-123">Consulte también .</span><span class="sxs-lookup"><span data-stu-id="adfde-123">See also</span></span>

[<span data-ttu-id="adfde-124">Administrar el trabajo de varias empresas en el hub de empresas</span><span class="sxs-lookup"><span data-stu-id="adfde-124">Manage Work across Multiple Companies in the Company Hub</span></span>](company-hub.md)  
[<span data-ttu-id="adfde-125">Agregar empresas al hub de empresas</span><span class="sxs-lookup"><span data-stu-id="adfde-125">Add companies to your company hub</span></span>](company-hub-add-company.md)  
[<span data-ttu-id="adfde-126">Experiencias contables en Business Central</span><span class="sxs-lookup"><span data-stu-id="adfde-126">Accountant Experiences in Business Central</span></span>](finance-accounting.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]