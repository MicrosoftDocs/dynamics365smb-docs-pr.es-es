---
title: 'Solución de problemas: acceso a la cámara y a la ubicación'
description: Este artículo describe cómo solucionar problemas de acceso a la información de la cámara y la ubicación en Business Central.
author: blrobl
ms.author: t-blrobl
ms.date: 10/01/2020
ms.custom: na
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: conceptual
ms.service: dynamics365-business-central
ms.openlocfilehash: 68ec41a42898688cbebea341782f0e0bc265341a
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5393779"
---
# <a name="troubleshooting-accessing-camera-and-location"></a><span data-ttu-id="62bd9-103">Solución de problemas: acceso a la cámara y a la ubicación</span><span class="sxs-lookup"><span data-stu-id="62bd9-103">Troubleshooting: Accessing Camera and Location</span></span>

<span data-ttu-id="62bd9-104">Puede encontrar algunos problemas al intentar acceder a la cámara y a la información de ubicación de un dispositivo desde [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="62bd9-104">You might come across some issues when trying to access the camera and location information of a device from [!INCLUDE[prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="62bd9-105">Puede encontrar las causas posibles de estos problemas y cómo solucionarlos a continuación.</span><span class="sxs-lookup"><span data-stu-id="62bd9-105">You can find the possible causes behind these problems and how to work around them listed below.</span></span>

## <a name="device-must-have-camera-and-location-capabilities"></a><span data-ttu-id="62bd9-106">El dispositivo debe tener capacidades de cámara y ubicación</span><span class="sxs-lookup"><span data-stu-id="62bd9-106">Device must have Camera and Location Capabilities</span></span>

<span data-ttu-id="62bd9-107">Para acceder a la cámara o la ubicación de un usuario desde un dispositivo, el dispositivo debe tener una cámara física o la capacidad de recuperar información de ubicación.</span><span class="sxs-lookup"><span data-stu-id="62bd9-107">In order to access the camera or a user's location from a device, the device must have a physical camera or the capability to retrieve location information, respectively.</span></span>

<span data-ttu-id="62bd9-108">Si su dispositivo tiene capacidades de cámara y ubicación, pero sigue teniendo problemas, es posible que algunos controladores deban actualizarse o reinstalarse.</span><span class="sxs-lookup"><span data-stu-id="62bd9-108">If your device has camera and location capabilities but you still encounter problems, it is possible that some drivers need updating or reinstalling.</span></span> <span data-ttu-id="62bd9-109">Incluso si no está seguro, siempre recomendamos que actualice el sistema operativo, los controladores y el navegador de su dispositivo a la última versión para obtener la mejor experiencia.</span><span class="sxs-lookup"><span data-stu-id="62bd9-109">Even if you are unsure, we always recommend you update your device operating system, drivers, and browser to the latest version for the best experience.</span></span>

## <a name="access-permissions-not-enabled"></a><span data-ttu-id="62bd9-110">Permisos de acceso no habilitados</span><span class="sxs-lookup"><span data-stu-id="62bd9-110">Access Permissions not Enabled</span></span>

<span data-ttu-id="62bd9-111">Debe habilitar el acceso general a la cámara y la ubicación desde la configuración de privacidad de su dispositivo y otorgar permiso explícitamente para [!INCLUDE[prod_short](includes/prod_short.md)] para acceder a ellos.</span><span class="sxs-lookup"><span data-stu-id="62bd9-111">You must enable general access to camera and location from your device's privacy settings and explicitly give permission to  [!INCLUDE[prod_short](includes/prod_short.md)] to access them.</span></span> <span data-ttu-id="62bd9-112">Por ejemplo, para ver o cambiar los permisos de un dispositivo ejecutando Windows, vaya a **Configuración**, elija **Privacidad** y, a continuación, **Permisos de la aplicación**.</span><span class="sxs-lookup"><span data-stu-id="62bd9-112">For example, to see or change permissions for a device running on Windows, go to **Settings**, choose **Privacy**, and then **App permissions**.</span></span> 

<span data-ttu-id="62bd9-113">Para dispositivos móviles, debe dar permisos de acceso a la cámara y a la ubicación para la Aplicación móvil de [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="62bd9-113">For mobile devices, you must give camera and location access permissions to the [!INCLUDE[prod_short](includes/prod_short.md)] Mobile App.</span></span> <span data-ttu-id="62bd9-114">Para hacerlo en un dispositivo iOS, vaya a **Configuración**, elija **Privacidad**, y después a **Cámara** o **Localización**.</span><span class="sxs-lookup"><span data-stu-id="62bd9-114">To do so for an iOS device, go to **Settings**, choose **Privacy**, and then **Camera** or **Location**.</span></span> <span data-ttu-id="62bd9-115">Para los dispositivos Android, vaya a **Configuración**, elija **Aplicaciones y notificaciones**, **Avanzado**, **Administrador de permisos** y después, **Cámara** o **Ubicación**.</span><span class="sxs-lookup"><span data-stu-id="62bd9-115">For Android devices go to **Settings**, choose **Apps & Notifications**, **Advanced**, **Permission Manager**, and then **Camera** or **Location**.</span></span>

<span data-ttu-id="62bd9-116">Además, si está utilizando [!INCLUDE[prod_short](includes/prod_short.md)] en un navegador, también debe dar permiso al sitio de [!INCLUDE[prod_short](includes/prod_short.md)] para acceder a la información de la cámara o ubicación.</span><span class="sxs-lookup"><span data-stu-id="62bd9-116">In addition, if you are using [!INCLUDE[prod_short](includes/prod_short.md)] in a browser, you must also grant the [!INCLUDE[prod_short](includes/prod_short.md)] site permission to access the camera or location information.</span></span> <span data-ttu-id="62bd9-117">Para ver o cambiar los permisos de un sitio en el navegador de Microsoft Edge, vaya a **Configuración**, elija **Permisos del sitio** y después, **Cámara** o **Ubicación**.</span><span class="sxs-lookup"><span data-stu-id="62bd9-117">To see or change a site's permissions in the Microsoft Edge browser, go to **Settings**, choose **Site Permissions**, and then **Camera** or **Location**.</span></span> <span data-ttu-id="62bd9-118">Tenga en cuenta que esto puede ser diferente para otros navegadores.</span><span class="sxs-lookup"><span data-stu-id="62bd9-118">Note that this might be different for other browsers.</span></span>

<span data-ttu-id="62bd9-119">De manera predeterminada, el dispositivo o navegador mostrará una solicitud para acceder a estas características cuando el usuario las active por primera vez.</span><span class="sxs-lookup"><span data-stu-id="62bd9-119">By default, the device or browser will pop up a request to access these capabilities when the user activates them for the first time.</span></span>

> [!NOTE]  
> <span data-ttu-id="62bd9-120">Algunos navegadores antiguos no dan acceso a la cámara ni a la ubicación.</span><span class="sxs-lookup"><span data-stu-id="62bd9-120">Some old browsers do not grant access to camera and location.</span></span> <span data-ttu-id="62bd9-121">Por ejemplo, la cámara no está disponible en Internet Explorer o el navegador Microsoft Edge (versión heredada).</span><span class="sxs-lookup"><span data-stu-id="62bd9-121">For example, camera is not available in Internet Explorer or the legacy Edge browser.</span></span>

## <a name="web-client-connection-not-secure"></a><span data-ttu-id="62bd9-122">La conexión del cliente web no es segura</span><span class="sxs-lookup"><span data-stu-id="62bd9-122">Web Client Connection not Secure</span></span>

<span data-ttu-id="62bd9-123">Las capacidades de cámara y ubicación solo están disponibles cuando se accede al cliente web a través de conexiones HTTP con seguridad SSL, utilizando el esquema de URI `https://`.</span><span class="sxs-lookup"><span data-stu-id="62bd9-123">The camera and location capabilities are only available when accessing the Web Client through SSL secured HTTP connections, using the `https://` URI scheme.</span></span> 

<span data-ttu-id="62bd9-124">La única excepción es conectarse a `http://localhost`, utilizado para fines de desarrollo y prueba.</span><span class="sxs-lookup"><span data-stu-id="62bd9-124">The only exception is connecting to `http://localhost`, used for development and test purposes.</span></span>


## <a name="working-with-virtualization-technologies"></a><span data-ttu-id="62bd9-125">Trabajo con tecnologías de virtualización</span><span class="sxs-lookup"><span data-stu-id="62bd9-125">Working with Virtualization Technologies</span></span>

<span data-ttu-id="62bd9-126">Cuando se conecte a [!INCLUDE[prod_short](includes/prod_short.md)] mediante el Escritorio remoto u otra virtualización, es posible que el acceso a la cámara o la ubicación no esté disponible.</span><span class="sxs-lookup"><span data-stu-id="62bd9-126">When connecting to [!INCLUDE[prod_short](includes/prod_short.md)] through Remote Desktop or another virtualization, the access to camera or location might not be available.</span></span> <span data-ttu-id="62bd9-127">Si este es el caso, use el sistema físico en su lugar.</span><span class="sxs-lookup"><span data-stu-id="62bd9-127">If this is the case, use the physical system instead.</span></span>

## <a name="antivirus-software"></a><span data-ttu-id="62bd9-128">Software antivirus</span><span class="sxs-lookup"><span data-stu-id="62bd9-128">Antivirus Software</span></span>
<span data-ttu-id="62bd9-129">Algunos software antivirus bloquean el acceso a la cámara y la ubicación de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="62bd9-129">Some antivirus software block access to camera and location by default.</span></span> <span data-ttu-id="62bd9-130">Recuerde comprobar la configuración de su software antivirus.</span><span class="sxs-lookup"><span data-stu-id="62bd9-130">Remember to check your antivirus software settings.</span></span>

## <a name="see-also"></a><span data-ttu-id="62bd9-131">Consulte también</span><span class="sxs-lookup"><span data-stu-id="62bd9-131">See Also</span></span>
[<span data-ttu-id="62bd9-132">Implementación de la cámara en AL</span><span class="sxs-lookup"><span data-stu-id="62bd9-132">Implementing the Camera in AL</span></span>](/dynamics365/business-central/dev-itpro/developer/devenv-implement-camera-al)  
[<span data-ttu-id="62bd9-133">Implementación de la ubicación en AL</span><span class="sxs-lookup"><span data-stu-id="62bd9-133">Implementing the Location in AL</span></span>](/dynamics365/business-central/dev-itpro/developer/devenv-implement-location-al)


[!INCLUDE[footer-include](includes/footer-banner.md)]