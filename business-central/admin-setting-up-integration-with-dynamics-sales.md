---
title: Configuración de cuentas de usuario para la integración con Dynamics 365 for Sales | Documentos de Microsoft
description: Obtenga información sobre cómo configurar las cuentas de usuario que las aplicaciones usan para intercambiar datos y que los usuarios usan para acceder y sincronizar datos en las aplicaciones.
services: project-madeira
documentationcenter: ''
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: bholtorf
ms.openlocfilehash: 3163389cb0818133fba9ab8c55b8d0cf662130f1
ms.sourcegitcommit: 04581558f6c5488c705a7ac392cf297be10b5f4f
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 06/06/2019
ms.locfileid: "1620958"
---
# <a name="setting-up-user-accounts-for-integrating-with-dynamics-365-for-sales"></a>Configuración de cuentas de usuario para la integración con Dynamics 365 for Sales
Este artículo proporciona una visión general de cómo configurar las cuentas de usuario que se necesitan para integrar [!INCLUDE[crm_md](includes/crm_md.md)] con [!INCLUDE[d365fin](includes/d365fin_md.md)].  

> [!VIDEO https://go.microsoft.com/fwlink/?linkid=2085500]

## <a name="setting-up-the-admininstrator-user-account-in-sales"></a>Configuración de la cuenta de usuario administrador en Sales
Debe agregar su cuenta de usuario administrador para [!INCLUDE[d365fin](includes/d365fin_md.md)] como usuario en [!INCLUDE[crm_md](includes/crm_md.md)] y luego promocionar al usuario a administrador en [!INCLUDE[crm_md](includes/crm_md.md)]. La cuenta de usuario administrador también debe tener el rol Personalizador del sistema y al menos otro rol de usuario no administrativo, como Director de ventas, en [!INCLUDE[crm_md](includes/crm_md.md)].

## <a name="setting-up-the-user-account-for-the-integration"></a>Configuración de la cuenta de usuario para la integración
Debe crear una cuenta de usuario dedicada en su suscripción de Office 365 que [!INCLUDE[d365fin](includes/d365fin_md.md)] y [!INCLUDE[crm_md](includes/crm_md.md)] puedan utilizar para sincronizar datos. Esta cuenta de usuario debe poder iniciar sesión en [!INCLUDE[crm_md](includes/crm_md.md)], lo que significa que este usuario debe tener una licencia para [!INCLUDE[crm_md](includes/crm_md.md)] y al menos un rol seguridad asignado en [!INCLUDE[crm_md](includes/crm_md.md)], tal y como se describe [aquí](https://docs.microsoft.com/en-us/dynamics365/customer-engagement/admin/create-users-assign-online-security-roles#create-a-user-account). Para obtener más información sobre cómo crear usuarios en [!INCLUDE[crm_md](includes/crm_md.md)], consulte [Administrar la seguridad, los usuarios y los equipos](http://go.microsoft.com/fwlink/?LinkID=616518). Una vez establecida la conexión, [!INCLUDE[d365fin](includes/d365fin_md.md)] asignará a la cuenta de usuario los roles de seguridad que necesita en [!INCLUDE[d365fin](includes/d365fin_md.md)] y esta cuenta puede configurarse en [modo de acceso no interactivo](https://docs.microsoft.com/en-us/dynamics365/customer-engagement/admin/create-users-assign-online-security-roles#create-a-non-interactive-user-account) en [!INCLUDE[crm_md](includes/crm_md.md)]

![Guía de configuración asistida que muestra el lugar para introducir las credenciales de usuario de sincronización](media/sync-user-setup.png "Página del asistente de configuración asistida de visualización que muestra el lugar para introducir las credenciales de usuario de sincronización")

> [!IMPORTANT]  
> No utilice la cuenta de administrador de [!INCLUDE[crm_md](includes/crm_md.md)] para la sincronización. Si lo hace, la sincronización se interrumpirá.
> Además, para evitar una sincronización constante, los cambios en los datos realizados por la cuenta de usuario de integración no están sincronizados. <!--What changes would this account make?--> Una vez establecida la conexión, se recomienda configurar el modo de acceso de la cuenta de usuario para la integración en modo no interactivo en [!INCLUDE[crm_md](includes/crm_md.md)]. Para obtener más información, consulte [Crear una cuenta de usuario no interactiva](https://docs.microsoft.com/en-us/dynamics365/customer-engagement/admin/create-users-assign-online-security-roles#create-a-non-interactive-user-account).

## <a name="setting-up-accounts-for-sales-people"></a>Configuración de cuentas para vendedores
Debe crear cuentas de usuario en [!INCLUDE[crm_md](includes/crm_md.md)] para los vendedores desde [!INCLUDE[d365fin](includes/d365fin_md.md)]. Para hacerlo más fácil, el centro de administración de Microsoft 365 ofrece una plantilla de Excel que puede utilizar. En la página **Usuarios activos**, seleccione **Más** y, a continuación, **Importar varios usuarios**. Seleccione **Descargar un archivo CSV solo con cabeceras** y, a continuación, introduzca la información para los vendedores. Para ver un ejemplo, seleccione **Descargar un archivo CSV con cabeceras e información de usuario de ejemplo**. Después de introducir la información sobre los usuarios, el siguiente paso del proceso de importación es asignar las licencias de usuario al plan de Dynamics 365 Customer Engagement.  

Después de importar los usuarios y asignarles licencias para Dynamics 365 Customer Engagement, debe asignar los usuarios al rol **Vendedor** en [!INCLUDE[crm_md](includes/crm_md.md)].

![Emparejamiento de vendedores con usuarios en Dynamics 365 for Sales](media/couple-salespeople.png "Visualización del emparejamiento de vendedores con usuarios en Dynamics 365 for Sales")

## <a name="see-also"></a>Consulte también  
[Integración con Dynamics 365 for Sales](admin-prepare-dynamics-365-for-sales-for-integration.md)  
