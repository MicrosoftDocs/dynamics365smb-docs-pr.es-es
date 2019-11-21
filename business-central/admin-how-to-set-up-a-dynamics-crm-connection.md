---
title: Conectar con Dynamics 365 Sales | Documentos de Microsoft
description: Puede efectuar la integración con Dynamics 365 Sales.
services: project-madeira
documentationcenter: ''
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: bholtorf
ms.openlocfilehash: 9e68f62a7fd79188e2461983837586bd4cd2c64b
ms.sourcegitcommit: 319023e53627dbe8e68643908aacc6fd594a4957
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2019
ms.locfileid: "2554379"
---
# <a name="set-up-a-connection-to-dynamics-365-sales"></a>Configurar una conexión a Dynamics 365 Sales
Para integrar con [!INCLUDE[crm_md](includes/crm_md.md)] deberá configurar una conexión entre [!INCLUDE[d365fin](includes/d365fin_md.md)] y [!INCLUDE[crm_md](includes/crm_md.md)].

> [!VIDEO https://go.microsoft.com/fwlink/?linkid=2085501]

## <a name="before-you-start"></a>Antes de comenzar
Antes de comenzar a conectar las aplicaciones, existen cierta información útil para prepararse:  

* Una dirección URL de la aplicación [!INCLUDE[crm_md](includes/crm_md.md)]. Una manera rápida de obtener la dirección URL es abrir [!INCLUDE[crm_md](includes/crm_md.md)] y copiar la URL, y después pegarla en el campo **URL de Dynamics 365 Sales** en [!INCLUDE[d365fin](includes/d365fin_md.md)]. [!INCLUDE[d365fin](includes/d365fin_md.md)] corregirá el formato automáticamente.  
* Un nombre de usuario y una contraseña de una cuenta de usuario que se utilizan solo para la integración.  
* El nombre de usuario y la contraseña de la cuenta que tenga permisos de administrador.  

> [!Note]
> Estos pasos describen el procedimiento para la versión en línea de [!INCLUDE[d365fin](includes/d365fin_md.md)].

## <a name="set-up-test-and-enable-a-connection-to-includecrm_mdincludescrm_mdmd"></a>Configurar, probar y activar una conexión con [!INCLUDE[crm_md](includes/crm_md.md)]  
En todos los tipos de autenticación distintos de la autenticación de Office 365, configure la conexión a Dynamics 365 Sales en la página **Configuración de la conexión de Microsoft Dynamics 365 Sales**. Para la autenticación de Office 365, también puede usar la guía de configuración asistida **Configurar la conexión de Dynamics 365 Sales**, que le ayudará a proporcionar la información necesaria.

### <a name="to-use-an-assisted-setup-guide"></a>Para usar una guía de configuración asistida
La guía de configuración asistida **Configurar la conexión de Dynamics 365 Sales** le puede ayudar a configurar la conexión y a especificar si se activarán características avanzadas, como el emparejamiento entre los registros.

1. Seleccione **Configuración y extensiones** y después seleccione **Configuración asistida**.
2. Elija **Configurar la conexión de Dynamics 365 Sales** para iniciar la guía de configuración asistida.
3. Rellene los campos según sea necesario.
4. Opcionalmente, existen configuraciones avanzadas que pueden mejorar la seguridad y activar funciones de [!INCLUDE[crm_md](includes/crm_md.md)] adicionales, como el procesamiento de pedidos y la visualización de niveles de inventario. La siguiente tabla describe las configuraciones avanzadas.  

|Campo|Descripción|
|-----|-----|
|**Importar la solución de Dynamics 365 Sales**|Active esta opción para instalar y configurar para la detección de integración en [!INCLUDE[crm_md](includes/crm_md.md)]. Para obtener más información, consulte [Acerca de la solución de integración de Business Central](admin-prepare-dynamics-365-for-sales-for-integration.md#about-the-business-central-integration-solution).|
|**Publicar servicio web de disponibilidad de artículo**|Permitir que las personas que utilizan [!INCLUDE[crm_md](includes/crm_md.md)] consulten la disponibilidad de los artículos (productos) en inventario en [!INCLUDE[d365fin](includes/d365fin_md.md)]. Para ello es necesario que la cuenta de usuario de [!INCLUDE[d365fin](includes/d365fin_md.md)] tenga una clave de acceso de los servicios web. La asignación de la clave es un proceso de dos etapas. En la cuenta de usuario en [!INCLUDE[d365fin](includes/d365fin_md.md)] debe elegir la acción **Cambiar clave de servicio Web** . En la guía asistida Configurar la conexión de Dynamics 365 Sales debe especificar ka URL de servicio web OData de Dynamics 365 Business Central y proporcionar las credenciales de usuario de [!INCLUDE[d365fin](includes/d365fin_md.md)] para acceder al servicio. Para obtener más información, consulte [Servicios web OData](/dynamics365/business-central/dev-itpro/webservices/odata-web-services).|
|**URL de servicio web OData de Dynamics 365 Business Central**|Si habilita el servicio web de disponibilidad de producto, la URL del servicio web OData se proporciona automáticamente.|
|**Nombre de usuario de servicio web OData de Dynamics 365 Business Central**|El nombre de la cuenta de usuario de [!INCLUDE[d365fin](includes/d365fin_md.md)] que [!INCLUDE[crm_md](includes/crm_md.md)] usa para recuperar información sobre disponibilidad de productos en [!INCLUDE[d365fin](includes/d365fin_md.md)] a través del servicio web OData.|
|**Clave de acceso de servicio web OData de Dynamics 365 Business Central**|La clave de acceso de la cuenta de usuario que [!INCLUDE[crm_md](includes/crm_md.md)] usa para obtener información sobre disponibilidad de productos en [!INCLUDE[d365fin](includes/d365fin_md.md)] a través del servicio web OData. La clave se asigna al usuario seleccionado en el campo **Nombre de usuario de servicio web OData de Dynamics 365 Business Central**. Para obtener la clave, seleccione el botón **Valor de búsqueda** para el nombre de usuario, elija el usuario, elija **Administrar** y, a continuación **Editar**. En la ficha de usuario, elija **Acciones**, **Autenticación** y después seleccione **Cambiar clave de servicio Web**.|
|**Habilitar integración de pedido de venta**|Cuando los usuarios crean pedidos de venta en [!INCLUDE[crm_md](includes/crm_md.md)] y completan pedidos [!INCLUDE[d365fin](includes/d365fin_md.md)], se integra el proceso en [!INCLUDE[crm_md](includes/crm_md.md)]. Para obtener más información, consulte [Activar la integración de procesamiento de pedidos de venta](https://docs.microsoft.com/en-us/dynamics365/customer-engagement/sales-enterprise/developer/enable-sales-order-processing-integration). Para ello es necesario que proporcione las credenciales de una cuenta de usuario de administrador en [!INCLUDE[crm_md](includes/crm_md.md)]. Para obtener más información, consulte [Manejo de datos de pedidos de ventas especiales](marketing-integrate-dynamicscrm.md#handling-sales-order-data).|
|**Habilitar la conexión de Dynamics 365 for Sales**|Habilitar la conexión a [!INCLUDE[crm_md](includes/crm_md.md)].|
|**Versión de Dynamics 365 SDK**|Solo es relevante si va a realizar la integración con una versión local de [!INCLUDE[crm_md](includes/crm_md.md)]. Se trata del kit de desarrollo de software de Dynamics 365 (también designado Xrm) que se utiliza para conectar [!INCLUDE[d365fin](includes/d365fin_md.md)] a [!INCLUDE[crm_md](includes/crm_md.md)]. La versión debe ser compatible con la versión de SDK que utiliza [!INCLUDE[crm_md](includes/crm_md.md)] e igual o más nueva que la versión que utiliza [!INCLUDE[crm_md](includes/crm_md.md)].|

> [!Note]
> La guía de configuración asistida **Configurar la conexión de Dynamics 365 Sales** asigna automáticamente los roles de seguridad **Administrador de integración** y **Usuario de integración** a la cuenta de usuario utilizada para la integración.

### <a name="to-create-or-maintain-the-connection-manually"></a>Para crear o mantener la conexión manualmente
El procedimiento siguiente describe cómo rellenar los campos en la página **Configuración de la conexión de Microsoft Dynamics 365 Sales** manualmente. También es la página donde administra los valores para la integración.

1. Elija el ![icono bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Configuración de conexión de Microsoft Dynamics 365** y luego elija el enlace relacionado.
2. Escriba la siguiente información para la conexión de [!INCLUDE[d365fin](includes/d365fin_md.md)] a [!INCLUDE[crm_md](includes/crm_md.md)].

|Campo|Descripción|
|-----|-----|
|**URL de Dynamics 365 Sales**|La URL de su instancia de [!INCLUDE[crm_md](includes/crm_md.md)]. Para obtener la URL, abra [!INCLUDE[crm_md](includes/crm_md.md)], copie la dirección URL de la barra de direcciones del explorador y, a continuación, pegue la dirección URL en el campo. [!INCLUDE[d365fin](includes/d365fin_md.md)] se asegurará de que el formato sea correcto.|
|**Nombre de usuario** y **Contraseña**|Las credenciales de la cuenta de usuario que está dedicada para la integración. Para obtener más información, consulte [Configuración de cuentas de usuario para la integración con Dynamics 365 Sales](admin-setting-up-integration-with-dynamics-sales.md).|
|**Habilitado**|Comience a usar la integración. Si no activa la conexión ahora, la configuración de la conexión se guardará pero los usuarios no podrán tener acceso a los datos de [!INCLUDE[crm_md](includes/crm_md.md)] desde [!INCLUDE[d365fin](includes/d365fin_md.md)]. Puede volver a esta página y activar la conexión más adelante.  |
|**Versión de Dynamics 365 SDK**|Si está realizando la integración con una versión local de [!INCLUDE[crm_md](includes/crm_md.md)], este es el kit de desarrollo de software de Microsoft Dynamics 365 (también designado Xrm) que utiliza para conectar [!INCLUDE[d365fin](includes/d365fin_md.md)] a [!INCLUDE[crm_md](includes/crm_md.md)]. La versión que seleccione debe ser compatible con la versión de SDK que utiliza [!INCLUDE[crm_md](includes/crm_md.md)]. Esta versión es igual o más reciente que la versión que utiliza [!INCLUDE[crm_md](includes/crm_md.md)].|

> [!Note]
> Si está conectando una versión local de [!INCLUDE[d365fin](includes/d365fin_md.md)] a [!INCLUDE[crm_md](includes/crm_md.md)] y desea configurar una conexión a una instancia de [!INCLUDE[crm_md](includes/crm_md.md)] con un tipo de autenticación determinado, rellene los campos de la ficha desplegable **Detalles del tipo de autenticación** . Para obtener más información, consulte [Usar las cadenas de conexión de utilidad de XRM para conectarse a Dynamics 365](https://go.microsoft.com/fwlink/?linkid=843055). Este paso no es necesario a conectar una versión en línea de [!INCLUDE[d365fin](includes/d365fin_md.md)].

3. Escriba la siguiente información para la conexión de [!INCLUDE[crm_md](includes/crm_md.md)] a [!INCLUDE[d365fin](includes/d365fin_md.md)].

|Campo|Descripción|
|-----|-----|
|**URL de cliente web de Dynamics 365 Business Central**|La URL de su instancia de [!INCLUDE[d365fin](includes/d365fin_md.md)]. Esto permite a los usuarios de [!INCLUDE[crm_md](includes/crm_md.md)] abrir los registros correspondientes en [!INCLUDE[d365fin](includes/d365fin_md.md)] desde los registros de [!INCLUDE[crm_md](includes/crm_md.md)], como una cuenta o un producto. Los registros de [!INCLUDE[d365fin](includes/d365fin_md.md)] abiertos en [!INCLUDE[d365fin](includes/d365fin_md.md)]. Establezca este campo en la URL de la instancia de [!INCLUDE[d365fin](includes/d365fin_md.md)] que desea utilizar.<br /><br /> Para restablecer el campo a la URL predeterminada para [!INCLUDE[d365fin](includes/d365fin_md.md)], elija la acción **Restablecer URL de cliente web**.<br /><br /> Este campo es relevante solo si la solución de integración de [!INCLUDE[d365fin](includes/d365fin_md.md)] está instalada en [!INCLUDE[crm_md](includes/crm_md.md)].|
|**Servicio web de disponibilidad de artículo activado**|Permitir que las personas que utilizan [!INCLUDE[crm_md](includes/crm_md.md)] consulten la disponibilidad de los artículos (productos) en inventario en [!INCLUDE[d365fin](includes/d365fin_md.md)]. Si habilita esta opción, también debe proporcionar un nombre de usuario y una clave de acceso que use [!INCLUDE[crm_md](includes/crm_md.md)] para consultar en el servicio web OData la disponibilidad de los artículos (productos). Para obtener más información, consulte [Servicios web OData](/dynamics365/business-central/dev-itpro/webservices/odata-web-services.md).|
|**URL de servicio web OData de Dynamics 365 Business Central**|Si habilita el servicio web de disponibilidad de producto, la URL del servicio web OData se proporciona automáticamente.|
|**Nombre de usuario de servicio web OData de Dynamics 365 Business Central**|El nombre de la cuenta de usuario que [!INCLUDE[crm_md](includes/crm_md.md)] usa para obtener información sobre disponibilidad de productos de [!INCLUDE[d365fin](includes/d365fin_md.md)] a través del servicio web OData.|
|**Clave de acceso de servicio web OData de Dynamics 365 Business Central**|La clave de acceso de la cuenta de usuario que [!INCLUDE[crm_md](includes/crm_md.md)] usa para obtener información sobre disponibilidad de productos en [!INCLUDE[d365fin](includes/d365fin_md.md)] a través del servicio web OData. La clave se asigna al usuario seleccionado en el campo **Nombre de usuario de servicio web OData de Dynamics 365 Business Central**. Para obtener la clave, seleccione el botón **Valor de búsqueda** para el nombre de usuario, elija el usuario, elija **Administrar** y, a continuación **Editar**. En la ficha de usuario, elija **Acciones**, **Autenticación** y después seleccione **Cambiar clave de servicio Web**.|

4. Introduzca los valores siguientes para [!INCLUDE[crm_md](includes/crm_md.md)].

|Campo|Descripción|
|-----|-----|
|**La integración de pedidos de venta está habilitada**|Permitir que los usuarios envíen pedidos de venta y ofertas activadas en [!INCLUDE[crm_md](includes/crm_md.md)] y después verlas y procesarlas en [!INCLUDE[d365fin](includes/d365fin_md.md)]. Esto integra el proceso en [!INCLUDE[crm_md](includes/crm_md.md)]. Para obtener más información, consulte [Activar la integración de procesamiento de pedidos de venta](https://docs.microsoft.com/en-us/dynamics365/customer-engagement/sales-enterprise/developer/enable-sales-order-processing-integration).|
|**Crear automáticamente pedidos de ventas**|Crear un pedido de venta en [!INCLUDE[d365fin](includes/d365fin_md.md)] cuando un usuario cree y envíe uno en [!INCLUDE[crm_md](includes/crm_md.md)].|
|**Procesar automáticamente ofertas de venta**|Procesar una oferta de venta cuando en [!INCLUDE[d365fin](includes/d365fin_md.md)] cuando un usuario cree y active una en [!INCLUDE[crm_md](includes/crm_md.md)].|

5. Introduzca los siguientes valores avanzados.

|Campo|Descripción|
|-----|-----|
|**Los usuarios de [!INCLUDE[d365fin](includes/d365fin_md.md)] se deben asignar a los de Dynamics 365 Sales**|Especifique si las cuentas de usuario de [!INCLUDE[d365fin](includes/d365fin_md.md)] deben tener cuentas de usuario coincidentes en [!INCLUDE[crm_md](includes/crm_md.md)]. La **dirección de correo electrónico de autenticación de Office 365** del usuario de [!INCLUDE[d365fin](includes/d365fin_md.md)] debe coincidir con el **correo electrónico principal** del usuario de [!INCLUDE[crm_md](includes/crm_md.md)].<br /><br /> Si establece el valor en **Sí**, los usuarios de [!INCLUDE[d365fin](includes/d365fin_md.md)] que no tienen una cuenta de usuario de [!INCLUDE[crm_md](includes/crm_md.md)] correspondiente no tendrán capacidades de integración de [!INCLUDE[d365fin](includes/d365fin_md.md)] en la interfaz de usuario. El acceso a los datos de [!INCLUDE[crm_md](includes/crm_md.md)] directamente desde [!INCLUDE[d365fin](includes/d365fin_md.md)] se realiza en nombre de la cuenta de usuario de [!INCLUDE[crm_md](includes/crm_md.md)].<br /><br /> Si establece el valor en **No**, todos los usuarios de [!INCLUDE[d365fin](includes/d365fin_md.md)] tendrán capacidades de integración de [!INCLUDE[crm_md](includes/crm_md.md)] en la interfaz de usuario. El acceso a los datos de [!INCLUDE[crm_md](includes/crm_md.md)] directamente se realiza en nombre de la cuenta de usuario de conexión (integración) de [!INCLUDE[crm_md](includes/crm_md.md)].|
|**El usuario de Business Central actual está asignado a un usuario de Dynamics 365 Sales**|Indica si la cuenta de usuario está asignada a una cuenta en [!INCLUDE[crm_md](includes/crm_md.md)]|

6. Para probar los valores de la conexión, elija **Probar conexión**.  

    > [!NOTE]  
    >  Si el cifrado de datos no se ha habilitado en [!INCLUDE[d365fin](includes/d365fin_md.md)], se le preguntará si desea habilitarlo. Si desea habilitar el cifrado de datos, seleccione **Sí** y proporcione la información necesaria. Si no, elija **No**. Puede habilitar el cifrado de datos más adelante. Para obtener más información, consulte [Cifrado de datos en Dynamics 365 Business Central](/dynamics365/business-central/dev-itpro/developer/devenv-encrypting-data) en la ayuda para desarrolladores e informáticos.  

7. Si aún no está configurada la sincronización de [!INCLUDE[crm_md](includes/crm_md.md)], se le preguntará si desea utilizar la configuración de sincronización predeterminada. Dependiendo de si desea mantener los registros alineados en [!INCLUDE[crm_md](includes/crm_md.md)] y [!INCLUDE[d365fin](includes/d365fin_md.md)], elija **Sí** o **No**.

> [!Note]
> La conexión a Dynamics 365 Sales mediante la página **Configuración de la conexión de Microsoft Dynamics 365 Sales** puede requerir que asigne los roles de seguridad Administrador de integración y Usuario de integración a la cuenta utilizada para la integración. Para obtener más información, consulte [Asignar un rol de seguridad a un usuario](https://docs.microsoft.com/en-us/dynamics365/customer-engagement/admin/create-users-assign-online-security-roles#assign-a-security-role-to-a-user).


> [!Note]
> La conexión a Dynamics 365 Sales mediante la página **Configuración de la conexión de Microsoft Dynamics 365 Sales** puede requerir que [asigne los roles de seguridad **Administrador de integración** y **Usuario de integración**](https://docs.microsoft.com/en-us/dynamics365/customer-engagement/admin/create-users-assign-online-security-roles#assign-a-security-role-to-a-user) a la cuenta de usuario utilizada para la integración.


### <a name="to-disconnect-from-includecrm_mdincludescrm_mdmd"></a>Para desconectar de [!INCLUDE[crm_md](includes/crm_md.md)]  
1. Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Configuración de conexión de Microsoft Dynamics 365 Sales** y luego elija el vínculo relacionado.
2. En la página **Configuración de la conexión de Microsoft Dynamics 365 Sales**, desactive la casilla **Activado**.  

<!--## Install the [!INCLUDE[d365fin](includes/d365fin_md.md) Integration Solution
[!INCLUDE[d365fin](includes/d365fin_md.md)] includes a solution that enables users to access coupled records, such as customers and items, from records in [!INCLUDE[crm_md](includes/crm_md.md)], such as accounts and products. The solution adds a link to the pages in [!INCLUDE[crm_md](includes/crm_md.md)] to open the coupled [!INCLUDE[d365fin](includes/d365fin_md.md)] record. The solution also displays information from [!INCLUDE[d365fin](includes/d365fin_md.md)]on certain entities in [!INCLUDE[crm_md](includes/crm_md.md)], such as accounts. Installing this solution is optional. <!--"Solution" sounds old school. Is it an app, or an add-in, or an extension?


1.  From [!INCLUDE[d365fin](includes/d365fin_md.md)] installation media \(DVD\), copy the DynamicsNAVIntegrationSolution.zip file to your computer.  

     The DynamicsNAVIntegrationSolution.zip file is located in the **CrmCustomization** folder. This file is the solution package.   

2.  In [!INCLUDE[crm_md](includes/crm_md.md)], import the DynamicsNAVIntegrationSolution.zip as a solution.  

     This step adds the **[!INCLUDE[d365fin](includes/d365fin_md.md) Connection** entity and **[!INCLUDE[d365fin](includes/d365fin_md.md) Account Statistics** entity in the system and additional items such as [!INCLUDE[d365fin](includes/d365fin_md.md)] integration security roles.  

     For more information about how to manage solutions in [!INCLUDE[crm_md](includes/crm_md.md)], [http://go.microsoft.com/fwlink/?LinkID=616519](http://go.microsoft.com/fwlink/?LinkID=616519).  

3.  Optional: Set up the **[!INCLUDE[d365fin](includes/d365fin_md.md) Connection** entity to display in the **Settings** area of [!INCLUDE[crm_md](includes/crm_md.md)].  

     This enables [!INCLUDE[crm_md](includes/crm_md.md)] users who are assigned the **[!INCLUDE[d365fin](includes/d365fin_md.md) Admin** role to modify the entity in [!INCLUDE[crm_md](includes/crm_md.md)]. For more information about how to modify entities in [!INCLUDE[crm_md](includes/crm_md.md)], see [View or edit entity information](http://go.microsoft.com/fwlink/?LinkID=616521).  

4.  Assign the **[!INCLUDE[d365fin](includes/d365fin_md.md) Integration Administrator** role to the user account for the connection to [!INCLUDE[d365fin](includes/d365fin_md.md)].  

5.  Assign the **Business Central Integration User** role to all users who will use the [!INCLUDE[d365fin](includes/d365fin_md.md)] integration solution.  

If you install the [!INCLUDE[d365fin](includes/d365fin_md.md)] integration solution after you have set up the connection to [!INCLUDE[crm_md](includes/crm_md.md)] in [!INCLUDE[d365fin](includes/d365fin_md.md)], you must modify the connection setup to point to the URL.-->

<!--of the [!INCLUDE[nav_web_md](../developer/includes/nav_web_md.md)]. For more information, see [Set Up a Microsoft Dynamics 365 Sales Connection]() -->

<!--
# View Item Availability - Support Matrix
For most versions of [!INCLUDE[d365fin](includes/d365fin_md.md) and Dynamics 365 Sales, you can view availability figures for items across the integrated products. The following table shows which version combinations support viewing item availability.

| |Dynamics 365 Sales version|2015/Update 1/Online|2016/Update 1/Online|Dynamics 365 Sales|
|-|---------------------|---------------------|--------------------------|-----------------|
|**Dynamics NAV version**|
|**2016**||Not supported|Not supported|Not supported|
|**2017**||Not supported - Install from 2016|Supported|Supported|
|**Dynamics 365 for Financials**||Not supported - Install from 2016|Supported|Supported|


> [Note]
> You can obtain item availability support for combinations of Dynamics CRM 2015 and Business Central by running the DynamicsNAVIntegrationSolution.zip file on the Business Central product DVD.

For more information, see [System Requirements for Business Central](../deployment/system-requirement-business-central.md).

-->

## <a name="see-also"></a>Consulte también  
[Ver el estado de una sincronización](admin-how-to-view-synchronization-status.md)  
