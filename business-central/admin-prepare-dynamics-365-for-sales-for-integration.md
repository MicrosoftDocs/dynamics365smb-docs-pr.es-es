---
title: Integración con Dynamics 365 Sales | Documentos de Microsoft
description: Obtenga información sobre cómo preparar Dynamics 365 Business Central para integrarse con Dynamics 365 Sales.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: sales, crm, integration, integrating
ms.date: 07/23/2020
ms.author: bholtorf
ms.openlocfilehash: 7132a32a37844078b696af5e8d19bf951460a2e2
ms.sourcegitcommit: 7b5c927ea9a59329daf1b60633b8290b552d6531
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 07/23/2020
ms.locfileid: "3617659"
---
# <a name="integrating-with-dynamics-365-sales"></a>Integración con Dynamics 365 Sales

El papel de vendedor se considera a menudo uno de los trabajos más orientados hacia el exterior en una empresa. Sin embargo, puede ser útil para los vendedores poder mirar hacia adentro en la empresa y ver lo que está sucediendo en la trastienda. Mediante la integración de [!INCLUDE[d365fin](includes/d365fin_md.md)] y [!INCLUDE[crm_md](includes/crm_md.md)], puede dar a sus vendedores esa visión, permitiéndoles ver la información en [!INCLUDE[d365fin](includes/d365fin_md.md)] mientras trabajan en [!INCLUDE[crm_md](includes/crm_md.md)]. Por ejemplo, al preparar una oferta de ventas podría ser útil saber si tiene suficiente inventario para cumplir el pedido. Para obtener más información, consulte [Uso de Dynamics 365 Sales desde Business Central](marketing-integrate-dynamicscrm.md).

> [!NOTE]
> Este tema describe el proceso de integración de las versiones en línea de [!INCLUDE[crm_md](includes/crm_md.md)] y [!INCLUDE[d365fin](includes/d365fin_md.md)] a través de [!INCLUDE[d365fin](includes/cds_long_md.md)]. Para obtener información sobre la configuración local, consulte [Preparación de Dynamics 365 Sales para la integración local](/dynamics365/business-central/dev-itpro/administration/prepare-dynamics-365-for-sales-for-integration).

## <a name="integrating-through-common-data-service"></a>Integración a través de Common Data Service
[!INCLUDE[d365fin](includes/d365fin_md.md)] también se integra con [!INCLUDE[d365fin](includes/cds_long_md.md)], lo que facilita la conexión y sincronización de datos con otras aplicaciones de Dynamics 365, como [!INCLUDE[crm_md](includes/crm_md.md)], o incluso aplicaciones que crea usted mismo. Si está integrando por primera vez, le recomendamos que lo haga a través de [!INCLUDE[d365fin](includes/cds_long_md.md)]. Para obtener más información, vea [Integración con Common Data Service](admin-common-data-service.md).

Si ya ha integrado [!INCLUDE[crm_md](includes/crm_md.md)] con [!INCLUDE[d365fin](includes/d365fin_md.md)], puede continuar sincronizando datos utilizando su configuración. Sin embargo, si actualiza o desactiva la integración de [!INCLUDE[crm_md](includes/crm_md.md)], para activarla de nuevo debe conectarse a través de [!INCLUDE[d365fin](includes/cds_long_md.md)]. Para obtener más información, vea [Actualización de una integración con Dynamics 365 Sales](admin-upgrade-sales-to-cds.md).

> [!NOTE]
> La reconexión a través de [!INCLUDE[d365fin](includes/cds_long_md.md)] aplicará la configuración de sincronización predeterminada y sobrescribirá cualquier configuración que tenga. Por ejemplo, se aplicarán las asignaciones de tabla predeterminadas.

## <a name="integration-settings-that-are-specific-to-a-crm_md-integration"></a>Configuración de integración específica de una integración de [!INCLUDE[crm_md](includes/crm_md.md)]
La integración con [!INCLUDE[d365fin](includes/d365fin_md.md)] sucede a través de [!INCLUDE[d365fin](includes/cds_long_md.md)] y hay muchas configuraciones y entidades estándar proporcionadas por la integración. Además de la configuración estándar, hay algunas que son específicas de [!INCLUDE[crm_md](includes/crm_md.md)]. Se enumeran en las siguientes secciones.

## <a name="permissions-and-security-roles-for-user-accounts-in-sales"></a>Permisos y roles de seguridad para cuentas de usuario en Sales
Cuando instala la solución de integración, se configuran los permisos para la cuenta de usuario de integración. Si se cambian esos permisos, es posible que deba restablecerlos. Puede hacerlo reinstalando la solución de integración seleccionando **Volver a implementar la solución de integración** en la página **Configuración de conexión de Dynamics 365**. Se implementan los siguientes roles de seguridad:

* Administrador de integración de Dynamics 365 Business Central
* Usuario de integración de Dynamics 365 Business Central
* Usuario de disponibilidad de producto de Dynamics 365 Business Central

### <a name="connection-settings-in-the-setup-guide"></a>Configuración de conexión en la Guía de configuración

Puede usar una guía de configuración asistida para configurar rápidamente la conexión y especificar si se activarán características avanzadas, como el emparejamiento entre los registros.

1. Seleccione **Configuración y extensiones** y después seleccione **Configuración asistida**.
2. Elija **Configurar la conexión de Dynamics 365 Sales** para iniciar la guía de configuración asistida.
3. Rellene los campos según sea necesario.
4. Opcionalmente, existen configuraciones avanzadas que pueden mejorar la seguridad y activar funciones adicionales, como el procesamiento de pedidos y la visualización de niveles de inventario. La siguiente tabla describe las configuraciones avanzadas.  

| Campo | Descripción |
|--|--|
| **Importar la solución de Dynamics 365 Sales** | Active esta opción para instalar y configurar para la detección de integración en [!INCLUDE[crm_md](includes/crm_md.md)]. <!--For more information, see [About the Base CDS Integration Solution](admin-common-data-service.md#about-the-business-central-integration-solution). Need to add a new topic--> |
| **Publicar servicio web de disponibilidad de artículo** | Permitir que las personas que utilizan [!INCLUDE[crm_md](includes/crm_md.md)] consulten la disponibilidad de los artículos (productos) en inventario en [!INCLUDE[d365fin](includes/d365fin_md.md)]. Para ello es necesario que una cuenta de usuario de [!INCLUDE[d365fin](includes/d365fin_md.md)] tenga una clave de acceso de los servicios web. La asignación de la clave es un proceso de dos etapas. En la cuenta de usuario en [!INCLUDE[d365fin](includes/d365fin_md.md)] debe elegir la acción **Cambiar clave de servicio Web** . En la guía asistida Configurar la conexión de Dynamics 365 Sales debe especificar ka URL de servicio web OData de Dynamics 365 Business Central y proporcionar las credenciales de usuario de [!INCLUDE[d365fin](includes/d365fin_md.md)] para acceder al servicio. Para obtener más información, consulte [Servicios web OData](/dynamics365/business-central/dev-itpro/webservices/odata-web-services). |
| **URL de servicios web OData de Business Central** | Si habilita el servicio web para ver la disponibilidad de producto, la URL del servicio web OData se proporciona automáticamente. |
| **Nombre de usuario del servicio web OData de Business Central** | El nombre de la cuenta de usuario de [!INCLUDE[d365fin](includes/d365fin_md.md)] que [!INCLUDE[crm_md](includes/crm_md.md)] usa para recuperar información sobre disponibilidad de productos en [!INCLUDE[d365fin](includes/d365fin_md.md)] a través del servicio web OData. |
| **Clave de acceso del servicio web OData de Business Central** | La clave de acceso de la cuenta de usuario que [!INCLUDE[crm_md](includes/crm_md.md)] usa para obtener información sobre disponibilidad de productos en [!INCLUDE[d365fin](includes/d365fin_md.md)] a través del servicio web OData. La clave se asigna al usuario seleccionado en el campo **Nombre de usuario de servicio web OData de Business Central**. Para obtener la clave, seleccione el botón **Valor de búsqueda** para el nombre de usuario, elija el usuario, elija **Administrar** y, a continuación **Editar**. En la ficha de usuario, elija **Acciones**, **Autenticación** y después seleccione **Cambiar clave de servicio Web**. |
| **Habilitar integración de pedido de venta** | Cuando los usuarios crean pedidos de venta en [!INCLUDE[crm_md](includes/crm_md.md)] y completan pedidos [!INCLUDE[d365fin](includes/d365fin_md.md)], se integra el proceso en [!INCLUDE[crm_md](includes/crm_md.md)]. Para obtener más información, consulte [Activar la integración de procesamiento de pedidos de venta](/dynamics365/customer-engagement/sales-enterprise/developer/enable-sales-order-processing-integration). Para ello es necesario que proporcione las credenciales de una cuenta de usuario de administrador en [!INCLUDE[crm_md](includes/crm_md.md)]. Para obtener más información, consulte [Manejo de datos de pedidos de ventas especiales](marketing-integrate-dynamicscrm.md#handling-sales-order-data). |
| **Habilitar la conexión de CDS** | Habilitar la conexión a [!INCLUDE[d365fin](includes/cds_long_md.md)]. |
| **Versión de Dynamics 365 SDK** | Solo es relevante si va a realizar la integración con una versión local de [!INCLUDE[crm_md](includes/crm_md.md)]. Se trata del kit de desarrollo de software de Dynamics 365 (también designado Xrm) que se utiliza para conectar [!INCLUDE[d365fin](includes/d365fin_md.md)] a [!INCLUDE[crm_md](includes/crm_md.md)]. La versión debe ser compatible con la versión de SDK que utiliza [!INCLUDE[crm_md](includes/crm_md.md)] e igual o más nueva que la versión que utiliza [!INCLUDE[crm_md](includes/crm_md.md)]. |

### <a name="connection-settings-on-the-microsoft-dynamics-365-connection-setup-page"></a>Configuración de conexión en la página de configuración de conexión de Microsoft Dynamics 365

Escriba la siguiente información para la conexión de [!INCLUDE[crm_md](includes/crm_md.md)] a [!INCLUDE[d365fin](includes/d365fin_md.md)].

| Campo | Descripción |
|--|--|
| **URL de Dynamics 365 Sales** | La URL de su instancia de [!INCLUDE[crm_md](includes/crm_md.md)]. Esto permite a los usuarios abrir los registros correspondientes en [!INCLUDE[d365fin](includes/d365fin_md.md)] desde los registros de [!INCLUDE[crm_md](includes/crm_md.md)], como una cuenta o un producto. Los registros de [!INCLUDE[d365fin](includes/d365fin_md.md)] abiertos en [!INCLUDE[d365fin](includes/d365fin_md.md)]. |
|**URL de Dynamics 365 Sales**|La URL de su instancia de [!INCLUDE[crm_md](includes/crm_md.md)]. Esto permite a los usuarios abrir los registros correspondientes en [!INCLUDE[d365fin](includes/d365fin_md.md)] desde los registros de [!INCLUDE[crm_md](includes/crm_md.md)], como una cuenta o un producto. Los registros de [!INCLUDE[d365fin](includes/d365fin_md.md)] abiertos en [!INCLUDE[d365fin](includes/d365fin_md.md)].|
|**Servicio web de disponibilidad de artículo activado**|Permitir que las personas que utilizan [!INCLUDE[crm_md](includes/crm_md.md)] consulten la disponibilidad de los artículos (productos) en inventario en [!INCLUDE[d365fin](includes/d365fin_md.md)]. Si habilita esta opción, también debe proporcionar un nombre de usuario y una clave de acceso que use [!INCLUDE[crm_md](includes/crm_md.md)] para consultar en el servicio web OData la disponibilidad de los artículos (productos). Para obtener más información, consulte [Servicios web OData](/dynamics365/business-central/dev-itpro/webservices/odata-web-services).|
|**URL de servicio web OData de Dynamics 365 Business Central**|Si habilita el servicio web de disponibilidad de producto, la URL del servicio web OData se proporciona automáticamente. Establezca este campo en la URL de la instancia de [!INCLUDE[d365fin](includes/d365fin_md.md)] que desea utilizar.<br /><br /> Para restablecer el campo a la URL predeterminada para [!INCLUDE[d365fin](includes/d365fin_md.md)], elija la acción **Restablecer URL de cliente web**.<br /><br /> Este campo es relevante solo si la solución de integración de [!INCLUDE[d365fin](includes/d365fin_md.md)] está instalada en [!INCLUDE[crm_md](includes/crm_md.md)].|
|**Nombre de usuario de servicio web OData de Dynamics 365 Business Central**|El nombre de la cuenta de usuario que [!INCLUDE[crm_md](includes/crm_md.md)] usa para obtener información sobre disponibilidad de productos de [!INCLUDE[d365fin](includes/d365fin_md.md)] a través del servicio web OData.|
|**Clave de acceso de servicio web OData de Dynamics 365 Business Central**|La clave de acceso de la cuenta de usuario que [!INCLUDE[crm_md](includes/crm_md.md)] usa para obtener información sobre disponibilidad de productos en [!INCLUDE[d365fin](includes/d365fin_md.md)] a través del servicio web OData. La clave se asigna al usuario seleccionado en el campo **Nombre de usuario de servicio web OData de Dynamics 365 Business Central**. Para obtener la clave, seleccione el botón **Valor de búsqueda** para el nombre de usuario, elija el usuario, elija **Administrar** y, a continuación **Editar**. En la ficha de usuario, elija **Acciones**, **Autenticación** y después seleccione **Cambiar clave de servicio Web**.|
|**Versión de Dynamics 365 SDK**|Si está realizando la integración con una versión local de [!INCLUDE[crm_md](includes/crm_md.md)], este es el kit de desarrollo de software de Microsoft Dynamics 365 (también designado Xrm) que utiliza para conectar [!INCLUDE[d365fin](includes/d365fin_md.md)] a [!INCLUDE[crm_md](includes/crm_md.md)]. La versión que seleccione debe ser compatible con la versión de SDK que utiliza [!INCLUDE[crm_md](includes/crm_md.md)]. Esta versión es igual o más reciente que la versión que utiliza [!INCLUDE[crm_md](includes/crm_md.md)].|-->

Además de las configuraciones anteriores, introduzca las siguientes configuraciones para [!INCLUDE[crm_md](includes/crm_md.md)].

| Campo | Descripción |
|--|--|
| **La integración de pedidos de venta está habilitada** | Permitir que los usuarios envíen pedidos de venta y ofertas activadas en [!INCLUDE[crm_md](includes/crm_md.md)] y después verlas y procesarlas en [!INCLUDE[d365fin](includes/d365fin_md.md)]. Esto integra el proceso en [!INCLUDE[crm_md](includes/crm_md.md)]. Para obtener más información, consulte [Activar la integración de procesamiento de pedidos de venta](/dynamics365/customer-engagement/sales-enterprise/developer/enable-sales-order-processing-integration). |
| **Crear automáticamente pedidos de ventas** | Crear un pedido de venta en [!INCLUDE[d365fin](includes/d365fin_md.md)] cuando un usuario cree y envíe uno en [!INCLUDE[crm_md](includes/crm_md.md)]. |
| **Procesar automáticamente ofertas de venta** | Procesar una oferta de venta cuando en [!INCLUDE[d365fin](includes/d365fin_md.md)] cuando un usuario cree y active una en [!INCLUDE[crm_md](includes/crm_md.md)]. |

<!--
### User Account Settings
Integrate with Business Central through Common Data Service requires an administrator user account and an account that is used only for the connection between the apps. This account is called the "integration user." When you install the CDS Base Integration Solution, permissions for the integration user account are configured in [!INCLUDE[crm_md](includes/crm_md.md)]. If those permissions are changed you might need to reset them. You can do that by reinstalling the Integration Solution or by manually resetting them. The following tables list the minimum permissions for the user accounts in [!INCLUDE[crm_md](includes/crm_md.md)].  -->

### <a name="standard-sales-entity-mapping-for-synchronization"></a>Asignación de entidad de Sales estándar para la sincronización

Las entidades en [!INCLUDE[crm_md](includes/crm_md.md)], como los pedidos, se integran con tipos equivalentes de entidades en [!INCLUDE[d365fin](includes/d365fin_md.md)], como los pedidos de venta. Para trabajar con datos de [!INCLUDE[crm_md](includes/crm_md.md)] se establecen vínculos, llamados emparejamientos, entre entidades en [!INCLUDE[d365fin](includes/d365fin_md.md)] y [!INCLUDE[crm_md](includes/crm_md.md)].

La siguiente tabla enumera la asignación estándar entre entidades en [!INCLUDE[d365fin](includes/d365fin_md.md)] y [!INCLUDE[crm_md](includes/crm_md.md)] que proporciona [!INCLUDE[d365fin](includes/d365fin_md.md)].

| [!INCLUDE[d365fin](includes/d365fin_md.md)] | [!INCLUDE[crm_md](includes/crm_md.md)] | Dirección de la sincronización | Filtro predeterminado |
|--|--|--|--|
| Unidad medida | Grupo de unidad | [!INCLUDE[d365fin](includes/d365fin_md.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] |  |
| Producto | Producto | [!INCLUDE[d365fin](includes/d365fin_md.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] y [!INCLUDE[crm_md](includes/crm_md.md)] -> [!INCLUDE[d365fin](includes/d365fin_md.md)] | Filtro de contacto de Sales: **Tipo de producto** es **Inventario de ventas** |
| Recurso | Producto | [!INCLUDE[d365fin](includes/d365fin_md.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] y [!INCLUDE[crm_md](includes/crm_md.md)] -> [!INCLUDE[d365fin](includes/d365fin_md.md)] | Filtro de contacto de Sales: **Tipo de producto** es **Services** |
| Grupo precio cliente | Lista de precios | [!INCLUDE[d365fin](includes/d365fin_md.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] |  |
| Precio venta | Lista de precios de productos | [!INCLUDE[d365fin](includes/d365fin_md.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] | Filtro de contacto de [!INCLUDE[d365fin](includes/d365fin_md.md)]: **Código ventas** no está en blanco, **Tipo de ventas** es **Grupo precio cliente** |
| Oportunidad | Oportunidad | [!INCLUDE[d365fin](includes/d365fin_md.md)] -> [!INCLUDE[d365fin](includes/cds_long_md.md)] y [!INCLUDE[crm_md](includes/crm_md.md)] -> [!INCLUDE[d365fin](includes/d365fin_md.md)] |  |
| Histórico cab. factura venta | Facturar | [!INCLUDE[d365fin](includes/d365fin_md.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] |  |
| Histórico lín. factura venta | Producto de facturación | [!INCLUDE[d365fin](includes/d365fin_md.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] |  |
| Cabecera de pedido de cliente | Pedido venta | [!INCLUDE[d365fin](includes/d365fin_md.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] | Filtro de cabecera de venta de [!INCLUDE[d365fin](includes/d365fin_md.md)]: **Tipo de documento** es Pedido, **Estado** es Lanzado |
| Notas de pedido de ventas | Notas de pedido de ventas | [!INCLUDE[d365fin](includes/d365fin_md.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] y [!INCLUDE[crm_md](includes/crm_md.md)] -> [!INCLUDE[d365fin](includes/d365fin_md.md)] |  |

### <a name="synchronization-rules"></a>Reglas de sincronización

En la tabla siguiente se enumeran las reglas que controlan la sincronización entre [!INCLUDE[crm_md](includes/crm_md.md)] y [!INCLUDE[d365fin](includes/d365fin_md.md)]. Estas son adicionales a las reglas definidas para Common Data Service, que también se aplican. Para obtener más información, consulte [Asignación de entidades estándar](/dynamics365/business-central/admin-synchronizing-business-central-and-sales?branch=master-cds-crm#standard-entity-mapping-for-synchronization).

> [!NOTE]  
> Los cambios en los datos realizados por la cuenta de usuario de integración no se sincronizan. Por lo tanto, le recomendamos que no modifique los datos mientras utiliza esa cuenta. Para obtener más información, consulte [Configuración de cuentas de usuario para la integración con Dynamics 365 Sales](admin-setting-up-integration-with-dynamics-sales.md).

|Escritorio|Regla|
|-----|----|
|Unidades medida|Las unidades de medida se sincronizan con grupos de unidades en [!INCLUDE[crm_md](includes/crm_md.md)]. Solo puede haber una unidad de medida definida en la unidad de venta.|
|Productos|Al sincronizar artículos con los productos de [!INCLUDE[crm_md](includes/crm_md.md)], [!INCLUDE[d365fin](includes/d365fin_md.md)] crea automáticamente una lista de precios en [!INCLUDE[crm_md](includes/crm_md.md)]. Para evitar errores de sincronización, no debe modificar la lista de precios manualmente.|
|Recursos|Los recursos se sincronizan con los productos de [!INCLUDE[crm_md](includes/crm_md.md)] que tienen el tipo de producto Servicio.|
|Grupos precio cliente|Los grupos de precios de cliente se sincronizan con las listas de precios de Sales.|
|Precios ventas|Los precios de Sales que tienen el tipo de venta Grupo precio cliente y tengan un código de venta definido se sincronizan con las líneas de lista de precios de [!INCLUDE[crm_md](includes/crm_md.md)].|
|Oportunidades|Las oportunidades se sincronizan con las oportunidades de [!INCLUDE[crm_md](includes/crm_md.md)]. El valor de Código de vendedor define el propietario de la entidad emparejada en [!INCLUDE[crm_md](includes/crm_md.md)].|
|Histórico facturas venta|Las facturas de ventas registradas se sincronizan con las facturas de ventas. Para poder sincronizar una factura, es mejor sincronizar las demás entidades que puedan participar en la factura, desde los vendedores hasta las listas de precios. El valor de Código de vendedor en la cabecera de la factura define el propietario de la entidad acoplada en Sales.|
|Pedidos de venta|Cuando se activa la integración de pedidos de venta, los pedidos de venta creados en [!INCLUDE[d365fin](includes/d365fin_md.md)] a partir de pedidos de venta enviados en [!INCLUDE[crm_md](includes/crm_md.md)] se sincronizan con los pedidos de venta en INCLUIR VENTAS cuando se liberan. Antes de sincronizar los pedidos, recomendamos que primero sincronice todas las entidades que intervienen en el pedido, como los vendedores y las listas de precios. El campo Código de vendedor en la cabecera del pedido define el propietario de la entidad emparejada en [!INCLUDE[crm_md](includes/crm_md.md)].|

### <a name="synchronization-jobs-for-a-sales-integration"></a>Trabajos de sincronización para una integración de ventas

Los trabajos se ejecutan en el siguiente orden para evitar dependencias de emparejamiento entre entidades. Hay trabajos adicionales disponibles de Common Data Service. Para obtener más información, consulte [Uso de colas de proyectos para programar tareas](/dynamics365/business-central/admin-job-queues-schedule-tasks).

1. Proyecto de sincronización de UNITOFMEASURE - Dynamics 365 Sales  
2. Proyecto de sincronización de RECURSO-PRODUCTO - Dynamics 365 Sales  
3. Proyecto de sincronización de ARTÍCULO-PRODUCTO - Dynamics 365 Sales  
4. Proyecto de sincronización de CUSTPRCGRP-PRICE - Dynamics 365 Sales.
5. Proyecto de sincronización de SALESPRC-PRODPRICE - Dynamics 365 Sales.
6. Proyecto de sincronización de POSTEDSALESINV-INV - Dynamics 365 Sales.

### <a name="default-synchronization-job-queue-entries"></a>Movimientos de la cola de proyectos de sincronización predeterminados

La tabla siguiente describe los proyectos de sincronización predeterminados para Sales.  

|Mov. cola proyecto|Descripción|Dirección|Asignación de tablas de integración|Frecuencia de sincronización predeterminada (minutos)|Tiempo de reposo de inactividad predeterminado (minutos)|  
|---------------------|---------------------------------------|---------------|-------------------------------|-----|-----|  
|Proyecto de sincronización de UNITOFMEASURE - Dynamics 365 Sales|Sincroniza los grupos de unidad de [!INCLUDE[crm_md](includes/crm_md.md)] con las unidades de medida de [!INCLUDE[d365fin](includes/d365fin_md.md)].|De [!INCLUDE[d365fin](includes/d365fin_md.md)] a [!INCLUDE[crm_md](includes/crm_md.md)]|UNIDAD DE MEDIDA|30|720<br> (12 h)|
|Proyecto de sincronización de RECURSO-PRODUCTO - Dynamics 365 Sales|Sincroniza los productos de [!INCLUDE[crm_md](includes/crm_md.md)] con los recursos de [!INCLUDE[d365fin](includes/d365fin_md.md)].|De [!INCLUDE[d365fin](includes/d365fin_md.md)] a [!INCLUDE[crm_md](includes/crm_md.md)]|RECURSO-PRODUCTO|30|720<br> (12 h)|
|Proyecto de sincronización de ARTÍCULO-PRODUCTO - Dynamics 365 Sales|Sincroniza los productos de [!INCLUDE[crm_md](includes/crm_md.md)] con los artículos de [!INCLUDE[d365fin](includes/d365fin_md.md)].|De [!INCLUDE[d365fin](includes/d365fin_md.md)] a [!INCLUDE[crm_md](includes/crm_md.md)]|ARTÍCULO-PRODUCTO|30|1440<br> (24 h)|
|Proyecto de sincronización de CUSTPRCGRP-PRICE - Dynamics 365 Sales|Sincroniza las listas de precios de venta de [!INCLUDE[crm_md](includes/crm_md.md)] con los grupos de precios de los clientes de [!INCLUDE[d365fin](includes/d365fin_md.md)].| |GRUPOS DE PRECIOS DE CLIENTES-LISTAS DE PRECIOS DE VENTA|30|1440<br> (24 h)|
|Proyecto de sincronización de SALESPRC-PRODUCTPRICE - Dynamics 365 Sales|Sincroniza los precios de producto de [!INCLUDE[crm_md](includes/crm_md.md)] con los precios de venta de [!INCLUDE[d365fin](includes/d365fin_md.md)].||PRECIO DEL PRODUCTO-PRECIO DE VENTA|30|1440<br> (24 h)|
|Proyecto de sincronización de POSTEDSALESINV-INV - Dynamics 365 Sales|Sincroniza las facturas de [!INCLUDE[crm_md](includes/crm_md.md)] con facturas de ventas registradas de [!INCLUDE[d365fin](includes/d365fin_md.md)].|De [!INCLUDE[d365fin](includes/d365fin_md.md)] a [!INCLUDE[crm_md](includes/crm_md.md)]|FACTURAS-FACTURAS DE VENTAS REGISTRADAS|30|1440<br> (24 h)|
|Sincronización de Estadísticas de clientes - Dynamics 365 Sales|Actualiza las cuentas de [!INCLUDE[crm_md](includes/crm_md.md)] con los últimos datos de los clientes de [!INCLUDE[d365fin](includes/d365fin_md.md)]. En [!INCLUDE[crm_md](includes/crm_md.md)], la información se muestra en el formulario de vista rápida **Estadísticas de la cuenta de Business Central** de cuentas que están emparejadas con los clientes de [!INCLUDE[d365fin](includes/d365fin_md.md)].<br /><br /> Estos datos también pueden actualizarse manualmente desde cada registro de cliente. Para obtener más información, consulte [Emparejar y sincronizar registros manualmente](admin-how-to-couple-and-synchronize-records-manually.md). </BR></BR>**Nota:** este movimiento de la cola de proyectos es relevante solo si la solución de integración de [!INCLUDE[d365fin](includes/d365fin_md.md)] está instalada en [!INCLUDE[crm_md](includes/crm_md.md)]. |No aplicable|No aplicable|30|No aplicable| 

### <a name="note-for-on-premises-versions"></a>Nota para versiones locales

> [!Note]
> Si está conectando una versión local de [!INCLUDE[d365fin](includes/d365fin_md.md)] a [!INCLUDE[crm_md](includes/crm_md.md)] y desea configurar una conexión a una instancia de [!INCLUDE[crm_md](includes/crm_md.md)] con un tipo de autenticación determinado, rellene los campos de la ficha desplegable **Detalles del tipo de autenticación** . Para obtener más información, consulte [Usar las cadenas de conexión de utilidad de XRM para conectarse a Dynamics 365](https://go.microsoft.com/fwlink/?linkid=843055). Este paso no es necesario a conectar una versión en línea de [!INCLUDE[d365fin](includes/d365fin_md.md)].

## <a name="see-also"></a>Consulte también

[Configuración de cuentas de usuario para la integración con [!INCLUDE[crm_md](includes/crm_md.md)]](admin-setting-up-integration-with-dynamics-sales.md)  
[Configurar una conexión a [!INCLUDE[crm_md](includes/crm_md.md)]](admin-how-to-set-up-a-dynamics-crm-connection.md)  
[Sincronización de Business Central y [!INCLUDE[crm_md](includes/crm_md.md)]](admin-synchronizing-business-central-and-sales.md)  
[Preparación de Dynamics 365 Sales para la integración local](/dynamics365/business-central/dev-itpro/administration/prepare-dynamics-365-for-sales-for-integration)
