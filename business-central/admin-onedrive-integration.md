---
title: Administrar la integración de OneDrive con Business Central
description: Obtenga información sobre lo que puede hacer para administrar una integración entre Business Central y OneDrive para la Empresa.
author: jswymer
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'OneDrive, share, browser'
ms.date: 02/28/2022
ms.author: jswymer
ms.service: dynamics-365-business-central
ms.reviewer: jswymer
---
# <a name="managing-onedrive-integration-with-business-central"></a>Administrar la integración de OneDrive con Business Central

Este artículo proporciona una descripción general de lo que puede hacer un administrador para controlar la integración de OneDrive para la Empresa con [!INCLUDE[prod_short](includes/prod_short.md)]. Los clientes de [!INCLUDE[prod_short](includes/prod_short.md)] en línea se benefician de la integración automática, sin necesidad de configuración adicional para utilizar las funciones abrir y compartir en OneDrive. Con la guía de configuración asistida de **Configuración de OneDrive**, puede dar acceso a los usuarios a aún más características de OneDrive, como abrir un archivo de Excel en OneDrive, o incluso desactivar todas las funciones.  

## <a name="configure-onedrive-for-integration-with-business-central"></a>Configurar OneDrive para la integración con Business Central

En esta sección se describen los requisitos que se deben cumplir en OneDrive para la Empresa para configurar la integración con Business Central y la tarea que puede realizar para administrar la integración.

### <a name="minimum-requirements"></a>Requisitos mínimos

* Cada usuario debe tener una licencia para [!INCLUDE[prod_short](includes/prod_short.md)] y OneDrive como parte de un plan de Microsoft 365.
* OneDrive debe configurarse para cada usuario.

### <a name="managing-privacy"></a>Gestionar la privacidad

> [!IMPORTANT]
> Si ha elegido implementar Business Central y OneDrive a diferentes países o regiones, los archivos generados por Business Central y colocados en OneDrive pueden cruzar los límites de residencia de datos. Asegúrese de confirmar las políticas de su organización y los requisitos de cumplimiento del gobierno para la residencia de datos antes de habilitar la conexión a OneDrive.

Los administradores y los usuarios finales controlan el contenido almacenado en OneDrive, y estos datos son propiedad exclusiva de su organización. Para más información, vea [Cómo SharePoint y OneDrive salvaguardan sus datos en la nube](/sharepoint/safeguarding-your-data). También puede visitar nuestra [Declaración de privacidad de Microsoft](https://privacy.microsoft.com/en-us/privacystatement), que explica los datos que procesa Microsoft, cómo los procesa Microsoft y con qué fines.

Al habilitar esta conexión de servicio, acepta:

(a) para compartir datos de Dynamics 365 Business Central con el proveedor de servicios, que los utilizará de acuerdo con los términos y la política de privacidad; (b) los niveles de cumplimiento del proveedor de servicios pueden diferir de Dynamics 365 Business Central; y (c) Microsoft puede compartir su información de contacto con este proveedor de servicios si es necesario para el funcionamiento y la resolución de problemas del servicio.

## <a name="configure-business-central"></a>Configurar Business Central

Con Business Central Online, la conexión entre Business Central y OneDrive se configura automáticamente para usted, y las funciones de OneDrive están disponibles para los usuarios de forma predeterminada. Si desea desactivar algunas o todas las funciones, puede utilizar la guía de configuración asistida de **Configuración de OneDrive** en el cliente de Business Central.

La configuración local de Business Central es diferente porque la conexión entre Business Central y OneDrive no está configurada para usted. Tendrá que hacerlo manualmente. Para obtener más información, consulte [Configurar la integración de OneDrive con Business Central local](admin-onedrive-integration-onpremises.md).

### <a name="about-multiple-environments"></a>Acerca de varios entornos

La integración de OneDrive se configura por entorno, es decir, su configuración se aplicará a todas las empresas en ese entorno. Si su organización tiene más de un entorno, deberá configurar la integración de OneDrive para cada uno.

### <a name="prerequisites"></a>Requisitos previos

- Permiso indirecto, modificar y eliminar (imd) en la tabla **Escenario de servicio de documentos** como minimo

### <a name="configure-onedrive-using-onedrive-setup"></a>Configurar OneDrive usando la configuración de OneDrive

1. Elija el icono ![Bombilla que abre la característica Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Configuración de OneDrive** y luego elija el enlace relacionado. 
2. La primera vez que ejecute la configuración asistida, verá **Su privacidad**. Lea la inforamción de la página y, si está de acuerdo con los términos, seleccione **Aceptar** para continuar.
3. En la página **Configurar el manejo de archivos**, tiene las siguientes opciones para elegir:

   [!INCLUDE[onedrive-feature-options](includes/onedrive-feature-options.md)]
4. Elija **Siguiene**>**Hecho**.

### <a name="switching-to-new-onedrive-integration-after-upgrade"></a>Cambiar a la nueva integración de OneDrive después de la actualización

La configuración asistida de **Configuración de OneDrive** se introdujo en el lanzamiento de versiones 2 de 2022, versión 21.0. Anteriormente, la integración de OneDrive usaba la **Configuración de conexión de SharePoint**, que ha quedado obsoleto y se eliminará en el lanzamiento de versiones 2 de 2023, versión 23.0. Después de actualizar a la versión 21, OneDrive seguirá funcionando como antes. Pero le recomendamos que cambie a la nueva integración de OneDrive. Hacer este cambio ahora hará que sea más fácil cuando la **Configuración de la conexión de SharePoint** finalmente se elimine. Además, le permitirá utilizar la guía de configuración asistida de **Configuración de OneDrive** para administrar las características de OneDrive que son accesibles para los usuarios. La configuración asistida de la **Configuración de OneDrive** hace la transición desde la configuración de SharePoint heredada fácil y sin problemas.

Para cambiar, simplemente abra y ejecute la configuración asistida **Configuración de OneDrive** directamente o abra la página **Configuración de la conexión de SharePoint** y elija **Ir a la nueva configuración de OneDrive** en la notificación en la parte superior de la página. Siga la guía de configuración como se describe en la sección anterior.

## <a name="restoring-onedrive-and-"></a>Restaurar OneDrive y [!INCLUDE[prod_short](includes/prod_short.md)]

Como parte de un ejercicio de recuperación ante desastres, los administradores pueden necesitar restaurar un entorno en línea de [!INCLUDE[prod_short](includes/prod_short.md)] a una copia de seguridad de un momento del pasado, y sincronizar el almacenamiento de OneDrive a ese mismo punto en el tiempo. OneDrive proporciona varias herramientas de recuperación, como restaurar OneDrive de un usuario a un momento anterior, restaurar una versión anterior de un archivo individual o restaurar archivos eliminados. Para obtener más información, consulte los siguientes artículos:

* Para [!INCLUDE[prod_short](includes/prod_short.md)], vea [Restaurar un entorno en el Centro de administración](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-backup-restore).
* Para OneDrive, vea [Restaurar su OneDrive](https://support.microsoft.com/en-us/office/restore-your-onedrive-fa231298-759d-41cf-bcd0-25ac53eb8a15?ui=en-us&rs=en-us&ad=us)

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

## <a name="see-also"></a>Consulte también .

[Integración de Business Central y OneDrive para la Empresa](across-onedrive-overview.md)  
[Abrir archivos de Business Central en OneDrive](across-share-onedrive.md)  
[Preguntas más frecuentes de OneDrive](admin-onedrive-faq.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
