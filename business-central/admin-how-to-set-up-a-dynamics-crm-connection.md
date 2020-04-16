---
title: Conectar con Dynamics 365 Sales | Documentos de Microsoft
description: Puede integrar otras aplicaciones con Business Central a través de Common Data Service.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: bholtorf
ms.openlocfilehash: 3375db0208d1a0275011f0efbfce4a13102c522e
ms.sourcegitcommit: d67328e1992c9a754b14c7267ab11312c80c38dd
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/01/2020
ms.locfileid: "3196644"
---
# <a name="connect-to-common-data-service"></a>Conectar a Common Data Service
Este tema describe cómo configurar una conexión entre [!INCLUDE[d365fin](includes/d365fin_md.md)] y [!INCLUDE[d365fin](includes/cds_long_md.md)]. Por lo general, las empresas crean la conexión para integrar y sincronizar datos con otra aplicación empresarial de Dynamics 365, como [!INCLUDE[crm_md](includes/crm_md.md)].  

## <a name="before-you-start"></a>Antes de comenzar
Hay algunos datos que debe tener listos para crear la conexión:  

* La dirección URL del entorno de [!INCLUDE[d365fin](includes/cds_long_md.md)] al que desea conectarse. Si usa la guía de configuración asistida **Configuración de conexión de CDS** para crear la conexión descubriremos los entornos, pero también puede introducir la URL de otro entorno en su suscriptor.  
* Un nombre de usuario y una contraseña de una cuenta de usuario que se utilizan solo para la integración. Esta cuenta se conoce como la cuenta de "usuario de integración". 
* El nombre de usuario y la contraseña de una cuenta que tenga permisos de administrador en [!INCLUDE[d365fin](includes/d365fin_md.md)] y [!INCLUDE[d365fin](includes/cds_long_md.md)].  

> [!Note]
> Estos pasos describen el procedimiento para la versión en línea de [!INCLUDE[d365fin](includes/d365fin_md.md)].

## <a name="set-up-a-connection-to-d365fin"></a>Configurar una conexión a [!INCLUDE[d365fin](includes/cds_long_md.md)]  
En todos los tipos de autenticación distintos de la autenticación de Office 365, configure la conexión a [!INCLUDE[d365fin](includes/cds_long_md.md)] en la página **Configuración de la conexión de CDS**. Para la autenticación de Office 365, es recomendable que use la guía de configuración asistida **Configuración de conexión de CDS**. La guía simplifica la configuración de la conexión y permite especificar características avanzadas, como el emparejamiento entre los registros.  

### <a name="to-use-the-cds-connection-setup-assisted-setup-guide"></a>Para usar la guía de configuración asistida Configuración de conexión de CDS 
1. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Configuración asistida** y luego elija el vínculo relacionado.
2. Elija **Configurar conexión de integración base de CDS** para iniciar la guía de configuración asistida.
3. Rellene los campos según sea necesario.

> [!Note]
> La guía de configuración asistida **Configuración de conexión de CDS** asigna automáticamente los roles de seguridad **Administrador de integración** y **Usuario de integración** a la cuenta de usuario utilizada para la integración y establece el modo de acceso para la cuenta en **no interactivo**.

### <a name="to-create-or-maintain-the-connection-manually"></a>Para crear o mantener la conexión manualmente
El procedimiento siguiente describe cómo configurar la conexión manualmente en la página **Configuración de conexión de CDS**. También es la página donde administra los valores para la integración.

1. Elija el icono de ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Configuración de conexión de CDS** y luego elija el enlace relacionado.
2. Escriba la siguiente información para la conexión de [!INCLUDE[d365fin](includes/d365fin_md.md)] a [!INCLUDE[d365fin](includes/cds_long_md.md)].

|Campo|Descripción|
|-----|-----|
|**URL de entorno**|Si posee entornos en [!INCLUDE[d365fin](includes/cds_long_md.md)], los encontraremos cuando ejecute la guía de configuración. Si desea conectarse a un entorno diferente en otro suscriptor, puede introducir las credenciales de administrador del entorno y lo descubriremos. |
|**Nombre de usuario** y **Contraseña**|Las credenciales de la cuenta de usuario que está dedicada para la integración. Para obtener más información, consulte [Configuración de cuentas de usuario para la integración con [!INCLUDE[d365fin](includes/cds_long_md.md)]](admin-setting-up-integration-with-dynamics-sales.md).|
|**Habilitado**|Comience a usar la integración. Si no activa la conexión ahora, la configuración de la conexión se guardará pero los usuarios no podrán tener acceso a los datos de [!INCLUDE[d365fin](includes/cds_long_md.md)] desde [!INCLUDE[d365fin](includes/d365fin_md.md)]. Puede volver a esta página y activar la conexión más adelante.  |

3. En el campo **Modelo de propiedad**, elija si desea una entidad de equipo en [!INCLUDE[d365fin](includes/cds_long_md.md)] para poseer nuevos registros o uno o más usuarios específicos. Si elige **Persona**, debe especificar cada usuario. Si elige **Equipo**, la unidad de negocio predeterminada BCI_Company se mostrará en el campo **Unidad de negocios emparejada**.

<!--Need to verify the details in this table, are these specific to Sales maybe?
Enter the following advanced settings.

|Field|Description|
|-----|-----|
|**[!INCLUDE[d365fin](includes/d365fin_md.md)] Users Must Map to CDS Users**|If you are using the Person ownership model, specify whether [!INCLUDE[d365fin](includes/d365fin_md.md)] user accounts must have a matching user accounts in [!INCLUDE[d365fin](includes/cds_long_md.md)]. The **Office 365 Authentication Email** of the [!INCLUDE[d365fin](includes/d365fin_md.md)] user must be the same as the **Primary Email** of the [!INCLUDE[crm_md](includes/crm_md.md)] user.<br /><br /> If you set the value to **Yes**, [!INCLUDE[d365fin](includes/d365fin_md.md)] users who do not have a matching [!INCLUDE[crm_md](includes/crm_md.md)] user account will not have [!INCLUDE[d365fin](includes/d365fin_md.md)] integration capabilities in the user interface. Access to [!INCLUDE[crm_md](includes/crm_md.md)] data directly from [!INCLUDE[d365fin](includes/d365fin_md.md)] is done on behalf of the [!INCLUDE[crm_md](includes/crm_md.md)] user account.<br /><br /> If you set the value to **No**, all [!INCLUDE[d365fin](includes/d365fin_md.md)] users will have [!INCLUDE[crm_md](includes/crm_md.md)] integration capabilities in the user interface. Access to [!INCLUDE[crm_md](includes/crm_md.md)] data is done on behalf of the [!INCLUDE[crm_md](includes/crm_md.md)] connection (integration) user.|
|**Current Business Central Salesperson is Mapped to a User**|Indicates whether your user account is mapped to an account in [!INCLUDE[crm_md](includes/crm_md.md)] <!--double check the name of this field|-->

4. Para probar la configuración de conexión, elija **Conexión** y luego **Probar conexión**.  

    > [!NOTE]  
    >  Si el cifrado de datos no se ha habilitado en [!INCLUDE[d365fin](includes/d365fin_md.md)], se le preguntará si desea habilitarlo. Si desea habilitar el cifrado de datos, seleccione **Sí** y proporcione la información necesaria. Si no, elija **No**. Puede habilitar el cifrado de datos más adelante. Para obtener más información, consulte [Cifrado de datos en Dynamics 365 Business Central](/dynamics365/business-central/dev-itpro/developer/devenv-encrypting-data.md) en la ayuda para desarrolladores e informáticos.  

5. Si aún no está configurada la sincronización de [!INCLUDE[d365fin](includes/cds_long_md.md)], se le preguntará si desea utilizar la configuración de sincronización predeterminada. Dependiendo de si desea mantener los registros alineados en [!INCLUDE[d365fin](includes/cds_long_md.md)] y [!INCLUDE[d365fin](includes/d365fin_md.md)], elija **Sí** o **No**.

> [!Note]
> La conexión a [!INCLUDE[d365fin](includes/cds_long_md.md)] mediante la página **Configuración de conexión de CDS** puede requerir que asigne los roles de seguridad Administrador de integración y Usuario de integración a la cuenta utilizada para la integración en Dynamics 365 Sales. Para obtener más información, consulte [Asignar un rol de seguridad a un usuario](/dynamics365/customer-engagement/admin/create-users-assign-online-security-roles#assign-a-security-role-to-a-user.md).

### <a name="to-disconnect-from-d365fin"></a>Para desconectar de [!INCLUDE[d365fin](includes/cds_long_md.md)]  
1. Elija el icono de ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Configuración de conexión de CDS** y luego elija el enlace relacionado.
2. En la página **Configuración de conexión de CDS**, desactive **Habilitado**.  

## <a name="see-also"></a>Consulte también  
[Ver el estado de una sincronización](admin-how-to-view-synchronization-status.md)  
