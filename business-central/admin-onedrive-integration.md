---
title: Administrar la integración de OneDrive con Business Central
description: Obtenga información sobre lo que puede hacer para administrar una integración entre Business Central y OneDrive para la Empresa.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: OneDrive, share, browser
ms.date: 05/12/2021
ms.author: bholtorf
ms.openlocfilehash: cceb05c1ad19a95494c188cd2482b45962535c94
ms.sourcegitcommit: 99c705d160451c05b226350ff94b52fb0c3ae7a0
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/06/2021
ms.locfileid: "7606415"
---
# <a name="managing-onedrive-integration-with-business-central"></a>Administrar la integración de OneDrive con Business Central 
Este artículo proporciona una descripción general de lo que puede hacer un administrador para controlar la integración de OneDrive para la Empresa con [!INCLUDE[prod_short](includes/prod_short.md)]. Los clientes de [!INCLUDE[prod_short](includes/prod_short.md)] en línea se benefician de la integración automática, sin necesidad de configuración adicional para utilizar estas funciones. 

## <a name="minimum-requirements"></a>Requisitos mínimos

* Cada usuario debe tener una licencia para [!INCLUDE[prod_short](includes/prod_short.md)] y OneDrive como parte de un plan de Microsoft 365.
* OneDrive debe configurarse para cada usuario.

## <a name="governance"></a>Gobernanza
El centro de administración de SharePoint proporciona un amplio control sobre las políticas que gobiernan el uso de OneDrive en toda la organización. Administradores globales o usuarios que tienen el rol de administrador de SharePoint pueden configurar políticas que determinen quién puede acceder a OneDrive, dónde residen los datos, el ciclo de vida del contenido y mucho más. Los siguientes enlaces proporcionan información sobre las funciones y configuraciones de uso frecuente que pueden mejorar su integración con [!INCLUDE[prod_short](includes/prod_short.md)]. 

* [Administrar la configuración de uso compartido](/sharepoint/turn-external-sharing-on-or-off)
* [Utilizar barreras de información con SharePoint](/sharepoint/information-barriers)
* [Más información sobre la prevención de pérdida de datos](/microsoft-365/compliance/dlp-learn-about-dlp)
* [Establecer el espacio de almacenamiento predeterminado para usuarios de OneDrive](/onedrive/set-default-storage-space)
* [Agregar y quitar administradores para OneDrive de un usuario](/sharepoint/manage-user-profiles#add-and-remove-admins-for-a-users-onedrive)
* [Deshabilitar la creación de OneDrive para algunos usuarios](/sharepoint/manage-user-profiles#disable-onedrive-creation-for-some-users)
* [Capacidades de multigeoárea en OneDrive y SharePoint Online](/microsoft-365/enterprise/multi-geo-capabilities-in-onedrive-and-sharepoint-online-in-microsoft-365)

> [!NOTE]
> Algunas funciones pueden estar disponibles solo para planes específicos.

## <a name="managing-privacy"></a>Gestionar la privacidad
Los administradores y los usuarios finales controlan el contenido almacenado en OneDrive, y estos datos son propiedad exclusiva de su organización. Para más información, vea [Cómo SharePoint y OneDrive salvaguardan sus datos en la nube](/sharepoint/safeguarding-your-data). También puede visitar nuestra [Declaración de privacidad de Microsoft](https://privacy.microsoft.com/en-us/privacystatement), que explica los datos que procesa Microsoft, cómo los procesa Microsoft y con qué fines.

## <a name="restoring-onedrive-and-prod_short"></a>Restaurar OneDrive y [!INCLUDE[prod_short](includes/prod_short.md)]
Como parte de un ejercicio de recuperación ante desastres, los administradores pueden necesitar restaurar un entorno de [!INCLUDE[prod_short](includes/prod_short.md)] a una copia de seguridad de un momento del pasado, y sincronizar el almacenamiento de OneDrive a ese mismo punto en el tiempo. OneDrive proporciona varias herramientas para ello, como restaurar OneDrive de un usuario a un momento anterior, restaurar una versión anterior de un archivo individual o restaurar archivos eliminados. Para obtener más información, consulte los siguientes artículos:

* Para [!INCLUDE[prod_short](includes/prod_short.md)], vea [Restaurar un entorno en el Centro de administración](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-backup-restore).
* Para OneDrive, vea [Restaurar su OneDrive](https://support.microsoft.com/en-us/office/restore-your-onedrive-fa231298-759d-41cf-bcd0-25ac53eb8a15?ui=en-us&rs=en-us&ad=us)

## <a name="configuring-business-central-on-premises"></a>Configurar Business Central local

Un administrador debe configurar la conexión entre [!INCLUDE[prod_short](includes/prod_short.md)] local y OneDrive. A diferencia de [!INCLUDE[prod_short](includes/prod_short.md)] en línea, la conexión no es automática. Si la conexión no se configura, los usuarios no pueden usar las funciones para OneDrive. 

[!INCLUDE[prod_short](includes/prod_short.md)] local solo se puede conectar a OneDrive alojado por Microsoft en la nube. No se admite la conexión de [!INCLUDE[prod_short](includes/prod_short.md)] local al repositorio Mis sitios de SharePoint Server.

> [!IMPORTANT]
> Al configurar esta función, también habilita funciones heredadas que envían archivos a OneDrive.  
>
>* La función Abrir en Excel copiará automáticamente el archivo de Excel a OneDrive, luego ábralo en Excel Online. 
>* Al exportar cualquier informe a un archivo se copiará automáticamente el archivo a OneDrive, luego ábralo en Excel Online, Word Online o OneDrive. 
>* Otras funciones también pueden abrirse automáticamente en OneDrive.

### <a name="to-prepare-prod_short-on-premises-for-connecting-to-onedrive"></a>Para preparar [!INCLUDE[prod_short](includes/prod_short.md)] local para conectarse a OneDrive

<!-- 
1. For the best experience Configure Azure Active Directory (AD) authentication.

   For more information, see [Authenticating Business Central Users with Azure Active Directory](/dynamics365/business-central/dev-itpro/administration/authenticating-users-with-azure-active-directory)-->

Agregue una aplicación registrada para Business Central en su inquilino de Azure AD de su plan Microsoft 365. Como otros servicios de Azure que funcionan con Business Central, OneDrive requiere un registro de aplicación en Azure Active Directory (Azure AD). El registro de la aplicación proporciona servicios de autenticación y autorización entre Business Central y SharePoint, que utiliza OneDrive.

Configure la aplicación registrada con los siguientes permisos delegados a la API de SharePoint:

- AllSites.Write
- MyFiles.Write
- User.Read.All 

Realice este trabajo en el portal de Azure. Asegúrese de copiar el ID de la aplicación (cliente) y el secreto del cliente utilizados por la aplicación registrada. Necesitará esta información en la siguiente tarea.

Para obtener más información sobre cómo registrar una aplicación y configurar permisos, consulte [Registrar una aplicación en Azure Active Directory](/dynamics365/business-central/dev-itpro/administration/register-app-azure#register-an-application-in-azure-active-directory) en la ayuda para desarrolladores y profesionales de TI.

> [!TIP]
> Si ya ha registrado una aplicación como parte de una integración con otro producto de Microsoft, como Power BI, luego puede reutilizar el registro de la aplicación. En este caso, solo tendrá que configurar los permisos de SharePoint.

### <a name="to-set-up-the-connection-in-prod_short-on-premises"></a>Para configurar la conexión en [!INCLUDE[prod_short](includes/prod_short.md)] local

<!--
> [!NOTE]
> This requires the following types of authentication credentials:
>
> * Windows
> * NavUserPassword
> * Azure Active Directory
-->
1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Configuración de conexión de Microsoft SharePoint** y luego elija el enlace relacionado.
2. En el campo **Descripción**, escriba una descripción para la conexión, como **OneDrive**.
3. En el campo **Carpeta**, ingrese **Business Central**.
4. En el campo **Ubicación**, ingrese la URL de su OneDrive.

    La URL de OneDrive suele tener el siguiente formato: `https://<tenant name>-my.sharepoint.com`. Para más información, vea [URL de OneDrive para los usuarios de su organización](/onedrive/list-onedrive-urls) en la documentación de OneDrive.
5. En el campo **Identificación del cliente**, ingrese el ID de cliente del registro de su aplicación.
6. En el campo **Secreto del cliente**, ingrese el secreto del registro de su aplicación. 
   <!-- 
   For information about how to find the URLs, see the following:
   * [How to find your SharePoint server URL]
   * [How to find your OneDrive URL]-->

> [!IMPORTANT]
> La página Configuración de conexión de SharePoint se utiliza para configurar varias funciones heredadas. La sección **General** configura la conexión con OneDrive, y la sección **Documentos compartidos** redirige archivos a SharePoint en su lugar. La función de SharePoint heredada quedará obsoleta en un futuro próximo. Le recomendamos que no configure la sección **Documentos compartidos**.

## <a name="see-also"></a>Consulte también
[Integración de Business Central y OneDrive para la Empresa](across-onedrive-overview.md)  
[Abrir archivos de Business Central en OneDrive](across-share-onedrive.md)  
[Preguntas más frecuentes de OneDrive](admin-onedrive-faq.md)

