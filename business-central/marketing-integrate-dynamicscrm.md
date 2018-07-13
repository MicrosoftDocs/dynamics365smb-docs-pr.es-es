---
title: Administrar clientes con Dynamics 365 for Sales | Documentos de Microsoft
description: "Puede usar Dynamics 365 for Sales desde Business Central para asignar datos y tener una integración y sincronización fluidas en el proceso de clientes potenciales a efectivo."
documentationcenter: 
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: integration, synchronize, map
ms.date: 07/02/2018
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: 046a42582dc66368fded90a4bb45add71a95d979
ms.openlocfilehash: 33987f37c170af9982b86baf20f0c3e0682de2cd
ms.contentlocale: es-es
ms.lasthandoff: 07/02/2018

---
# <a name="managing-customers-and-sales-created-in-dynamics-365-for-sales"></a>Gestión de clientes y ventas creados en Dynamics 365 for Sales
Si utiliza Dynamics 365 for Sales (Sales) para la interacción con el cliente, puede usar [!INCLUDE[d365fin](includes/d365fin_md.md)] para su procesamiento de pedidos y finanzas, y tener una integración fluida en el proceso de clientes potenciales a efectivo.

Al configurar su aplicación para integrarse con Sales, tendrá acceso a los datos de Sales desde [!INCLUDE[d365fin](includes/d365fin_md.md)] y a la inversa en algunos casos. Esta integración permite trabajar con los tipos de datos y sincronizar los que son comunes a ambos servicios, como clientes, contactos e información de ventas, y mantener los datos actualizados en ambas ubicaciones.  

Por ejemplo, el vendedor en Sales puede utilizar las listas de precios de [!INCLUDE[d365fin](includes/d365fin_md.md)] cuando se crea un pedido de venta. Cuando agrega el producto a la línea del pedido de venta en Sales, también puede ver el nivel de inventario (disponibilidad) del producto desde [!INCLUDE[d365fin](includes/d365fin_md.md)].

Por el contrario, los procesadores de pedidos en [!INCLUDE[d365fin](includes/d365fin_md.md)] pueden manejar las características especiales de las órdenes de venta transferidas automática o manualmente desde Sales, tales como crear automáticamente y publicar líneas de orden de venta válidas para artículos o recursos introducidos en Sales como productos fuera de catálogo. Para obtener más información, consulte la sección "Manejo de datos de pedidos de ventas especiales".

> [!IMPORTANT]  
> [!INCLUDE[d365fin](includes/d365fin_md.md)] se integra con Dynamics 365 for Sales solamente. Otras aplicaciones o soluciones dentro de Dynamics 365 que cambian el flujo de trabajo estándar o el modelo de datos en Sales, por ejemplo, Project Service Automation, pueden romper la integración entre [!INCLUDE[d365fin](includes/d365fin_md.md)] y Sales.

## <a name="standard-sales-entity-mapping-for-synchronization"></a>Asignación de entidad de Sales estándar para la sincronización
Las entidades de Sales, como las cuentas, se integran con tipos de registro de [!INCLUDE[d365fin](includes/d365fin_md.md)] equivalentes, como los clientes. Para trabajar con datos de Sales, se configuran asignaciones, llamadas acoplamientos, entre registros de [!INCLUDE[d365fin](includes/d365fin_md.md)] y registros de entidad de Sales. Por ejemplo, establezca un acoplamiento entre un cliente específico en [!INCLUDE[d365fin](includes/d365fin_md.md)] y una cuenta correspondiente en Sales.

La tabla siguiente enumera los tipos de registro (tablas) de [!INCLUDE[d365fin](includes/d365fin_md.md)] y las entidades correspondientes de Sales que se pueden sincronizar inmediatamente.

|[!INCLUDE[d365fin](includes/d365fin_md.md)]|Ccial|Dirección de la sincronización|Filtro predeterminado|
|-------------------------------------------|-----|-------------------------|--------------|
|Vendedor/Comprador|Usuario|Sales -> Business Central|Filtro de contacto de Sales: **Estado** es **No**, **Usuario con licencia** es **Sí**, Modo de integración de usuario es **No**|
|Cliente|Cuenta|Business Central -> Sales y Sales -> Business Central|Filtro de cuenta de Sales: **Tipo de relación** es **Cliente** y **Estado** es **Activo**.|
|Contacto|Contacto|Business Central -> Sales y Sales -> Business Central|Filtro de contacto de Business Central: **Tipo** es **Persona** y el contacto se asigna a una empresa. Filtro de contacto de Sales: el contacto se asigna a una empresa y el tipo de cliente principal es **Cuenta**.|
|Divisa|Divisa de la transacción|Business Central -> Sales| |
|Unidad de medida|Grupo de unidad|Business Central -> Sales| |
|Artículo|Producto|Business Central -> Sales y Sales -> Business Central|Filtro de contacto de Sales: **Tipo de producto** es **Inventario de ventas**|
|Recurso|Producto|Business Central -> Sales y Sales -> Business Central|Filtro de contacto de Sales: **Tipo de producto** es **Services**|
|Grupo precio cliente|Lista de precios|Business Central -> Sales| |
|Precio venta|Lista de precios de productos|Business Central -> Sales|Filtro central de Business Central: **Código ventas** no está en blanco, **Tipo de ventas** es **Grupo precio cliente**|
|Oportunidad|Oportunidad|Business Central -> Sales y Sales -> Business Central| |
|Histórico cab. factura venta|Facturar|Business Central -> Sales| |
|Histórico lín. factura venta|Producto de facturación|Business Central -> Sales| |

Las entidades de Sales y las tablas de [!INCLUDE[d365fin](includes/d365fin_md.md)] que están sincronizadas se definen mediante entradas de asignación de tablas en la tabla 5335, **Asignación de tablas de integración**. Puede ver las asignaciones y configurar filtros desde la página 5335, **Asignación de tablas de integración**. La asignación entre los campos de los registros de [!INCLUDE[d365fin](includes/d365fin_md.md)] y los campos de las entidades de Sales se definen por movimientos de asignación de campo en la tabla 5336, **Asignación de tablas de integración**, y con la lógica de asignación adicional.

### <a name="field-mapping-for-the-sales-account-option"></a>Asignación de campos para la opción de cuenta de Sales
Tres tablas en [!INCLUDE[d365fin](includes/d365fin_md.md)] se asignan a los campos de opción de la entidad **Cuenta**.   

Los registros de la tabla que no están vinculados a las opciones que existen en Sales se omitirán durante la sincronización. Esto significa que el campo **Opción** aparecerá en blanco en Sales.

La tabla siguiente muestra las asignaciones de las tablas de Business Central para el campo **Opción** en la entidad **Cuenta**.

|Escritorio|Campo de opción en la entidad de cuenta en Sales|
|----------------------|-------------------------------------------|
|Términos de pago|Términos de pago|
|Condiciones de envío|Dirección 1: Condiciones de flete|
|Transportista|Dirección 1: Método de envío|

### <a name="synchronization-rules"></a>Reglas de sincronización
En la tabla siguiente se describen las reglas que controlan la sincronización entre tablas de Business Central y entidades de Sales.

> [!NOTE]  
> Las modificaciones de los datos de Sales que realiza la cuenta de conexión de Sales se ignoran. Los cambios no se sincronizarán. Por lo tanto, se recomienda que no modifique los datos mediante la cuenta de conexión de Sales.

|Escritorio|Regla|
|-----|----|
|Clientes|Para que un cliente pueda sincronizarse a una cuenta, el vendedor que está asignado al cliente debe acoplarse a un usuario de Sales. Por lo tanto, cuando ejecute el proyecto de sincronización CLIENTES - Dynamics 365 for Sales y lo configure para crear nuevos registros, asegúrese de que sincroniza los vendedores con los usuarios de Sales antes de sincronizar los clientes con cuentas de Sales. <br /> <br />El proyecto de sincronización CLIENTES - Dynamics 365 for Sales solo sincroniza cuentas de Sales cuyo tipo de relación es Cliente.|
|Contactos|Solo los contactos de Sales que estén asociados con una cuenta se crearán en Business Central. El valor de Código de vendedor define el propietario de la entidad acoplada en Sales.|
|Divisas|Las divisas se acoplan a divisas de transacción en Sales según los códigos ISO. Solo las divisas que tengan un código ISO estándar se acoplarán y sincronizarán con divisas de transacción.|
|Unidades medida|Las unidades de medida se sincronizan con grupos de unidades en Sales. Solo puede haber una unidad de medida definida en la unidad de venta.|
|Productos|Al sincronizar artículos con los productos de Sales, Business Central crea automáticamente una lista de precios en Sales. Para evitar errores de sincronización, no debe modificar la lista de precios manualmente.|
|Vendedores|Los vendedores están acoplados a los usuarios del sistema en Sales. El usuario debe estar habilitado y con licencia, y no debe ser el usuario de integración. Tenga en cuenta que esta es la primera tabla que debe sincronizarse porque se utiliza en clientes, contactos, oportunidades y facturas de venta.|
|Recursos|Los recursos se sincronizan con los productos de Sales que tienen el tipo de producto Servicio.|
|Grupos precio cliente|Los grupos de precios de cliente se sincronizan con las listas de precios de Sales.|
|Precios ventas|Los precios de Sales que tienen el tipo de venta Grupo precio cliente y tengan un código de venta definido se sincronizan con las líneas de lista de precios de Sales.|
|Oportunidades|Las oportunidades se sincronizan con las oportunidades de Sales. El valor de Código de vendedor define el propietario de la entidad acoplada en Sales.|
|Histórico facturas venta|Las facturas de ventas registradas se sincronizan con las facturas de ventas. Para poder sincronizar una factura, es mejor sincronizar las demás entidades que puedan participar en la factura, desde los vendedores hasta las listas de precios. El valor de Código de vendedor en la cabecera de la factura define el propietario de la entidad acoplada en Sales.|

## <a name="setting-up-the-connection"></a>Configuración de la conexión
Desde Inicio, podrá acceder a la guía de configuración asistida **Configuración de conexión de Microsoft Dynamics 365** que le ayuda a configurar la conexión. Una vez terminada, tendrá un acoplamiento perfecto de los registros de Sales con los registros de [!INCLUDE[d365fin](includes/d365fin_md.md)].  

> [!NOTE]  
>   A continuación se explica la configuración asistida, pero puede efectuar las mismas tareas manualmente en la ventana **Configuración de conexión de Sales**.

En la guía de configuración asistida, puede elegir los datos que se sincronizarán entre los dos servicios. También puede especificar que desea importar la solución existente de Sales. En ese caso, debe especificar una cuenta de usuario administrador.

### <a name="setting-up-the-user-account-for-importing-the-solution"></a>Configuración de la cuenta de usuario para importar la solución
Para importar una solución existente Sales, la guía de configuración utiliza una cuenta administrativa. Esta cuenta debe ser un usuario válido de Sales con los roles de seguridad siguientes:

* Administrador del sistema  
* Personalizador de solución  

Para obtener más información, vea [Crear usuarios en Microsoft Dynamics 365 (en línea) y asignar roles de seguridad](/dynamics365/customer-engagement/admin/create-users-assign-online-security-roles) y [Administrar usuarios y permisos](ui-how-users-permissions.md).  

Esta cuenta solo se utiliza durante la configuración. Una vez que la solución se importa en [!INCLUDE[d365fin](includes/d365fin_md.md)], la cuenta ya no se necesita.

### <a name="setting-up-the-user-account-for-synchronization"></a>Configuración de la cuenta de usuario para la sincronización
La integración se basa en una cuenta de usuario compartida. Por lo tanto, en su suscripción de Office 365 deberá crear un usuario dedicado que se usará para la sincronización entre los dos servicios. Esta cuenta ya debe ser un usuario válido en Sales, pero no es necesario asignar roles de seguridad a la cuenta porque la guía de configuración lo hace automáticamente. Debe especificar esta cuenta de usuario una o varias veces en la guía de configuración, dependiendo de la sincronización que desea activar. Para obtener más información, vea [Crear usuarios en Microsoft Dynamics 365 (en línea) y asignar roles de seguridad](/dynamics365/customer-engagement/admin/create-users-assign-online-security-roles).

Si elige habilitar *Disponibilidad del producto*, la cuenta de usuario de integración debe tener una clave de acceso a los servicios web. Es un proceso de dos pasos en la página [!INCLUDE[d365fin](includes/d365fin_md.md)] para esa cuenta de usuario; debe elegir el botón **Cambiar clave de servicio Web** y, en la guía de configuración de conexión de Sales, debe especificar a dicho usuario como el usuario de servicio web de OData.

Si elige habilitar *Integración de pedido de venta*, deberá especificar un usuario que pueda controlar esta sincronización: el usuario de integración u otra cuenta de usuario.

### <a name="coupling-records"></a>Emparejamiento de registros
En la guía de configuración asistida, puede elegir la sincronización entre los dos servicios. Pero más tarde, también puede configurar determinados tipos de datos. A esto se le conoce como *emparejamiento* y esta sección proporciona recomendaciones de lo que debe tener en cuenta.

Por ejemplo, si desea ver las cuentas de Sales como clientes en [!INCLUDE[d365fin](includes/d365fin_md.md)], debe emparejar los dos tipos de registros. No es muy complicado: abra la ventana **Lista de clientes** en [!INCLUDE[d365fin](includes/d365fin_md.md)] y hay una acción en la cinta para emparejar este datos con Sales. A continuación, especifique qué clientes de [!INCLUDE[d365fin](includes/d365fin_md.md)] coinciden con cada cuenta de Sales.

En determinadas áreas, la funcionalidad se basa en el emparejamiento de determinados conjuntos de datos antes que otros conjuntos de datos como se muestra en la lista siguiente:

* Clientes y cuentas  
  * Emparejar vendedores con usuarios de Sales en primer lugar  
* Productos y recursos  
  * Emparejar unidades de medida con grupos de unidades de Sales en primer lugar  
* Precios de productos y recursos  
  * Emparejar grupos de precios de cliente con precios de Sales en primer lugar  

> [!NOTE]  
>   Si utiliza precios en divisas extranjeras, asegúrese de emparejar las divisas con las divisas de transacción de Sales.

En Sales, los pedidos de venta dependen de información adicional como clientes, unidades de medida, divisas, grupos de precios de cliente, productos o recursos. Para que la integración con los pedidos de venta funcione fluidamente, primero debe emparejar clientes, unidades de medida, divisas, grupos de precios de cliente, productos o recursos.

### <a name="synchronizing-records-fully"></a>Sincronización completa de los registros
Al final de la guía de configuración asistida, puede elegir la acción **Ejecutar sincronización completa** para iniciar la sincronización de todos los registros de [!INCLUDE[d365fin](includes/d365fin_md.md)] con todos los registros relacionados en la solución de Sales conectada. En la ventana **Revisión de sinc. completa de CRM**, elija la acción **Iniciar**. La sincronización comienza a ejecutar los proyectos según las dependencias. Por ejemplo, los registros de divisa se sincronizan antes que los registros de cliente. La sincronización completa puede durar mucho tiempo, por lo que se ejecutará en segundo plano para que pueda seguir trabajando en [!INCLUDE[d365fin](includes/d365fin_md.md)].

Para comprobar el progreso de los proyectos individuales de una sincronización completa, desglose el campo **Estado mov. cola proyecto**, **Estado de proyecto de tabla de integ. de destino** o **Estado de proyecto de tabla de integ. de origen** en la ventana **Revisión de sinc. completa de CRM**.

En la ventana **Configuración de conexión Microsoft Dynamics 365**, puede obtener los detalles acerca de la sincronización completa en cualquier momento. Desde aquí también puede abrir la ventana **Lista de asignaciones de tablas de integración** para ver información detallada acerca de las tablas de [!INCLUDE[d365fin](includes/d365fin_md.md)] y en la solución Sales que se deben sincronizar.

## <a name="handling-special-sales-order-data"></a>Manejar datos de pedidos de ventas especiales
Las órdenes de venta en Sales se transferirán automáticamente a [!INCLUDE[d365fin](includes/d365fin_md.md)] si selecciona la casilla **Crear automáticamente pedidos de venta** en la ventana **Configuración de conexión de Microsoft Dynamics 365**. En dichos pedidos de venta, el campo **Nombre** del pedido original se transfiere y se asigna al campo **Número de documento externo** del pedido de venta en [!INCLUDE[d365fin](includes/d365fin_md.md)].

Esto también puede funcionar si el pedido de cliente original contiene productos fuera de catálogo, es decir, elementos o recursos que no están registrados en ninguno de los productos. En ese caso, debe rellenar los campos **Tipo producto fuera de catálogo** y **N.º producto fuera de catálogo** en la ventana **Conf. ventas y cobros**, para asignar estas ventas de productos no registrados a un número del producto especificado o recurso para el análisis financiero.

Si la descripción del artículo en el pedido de venta original es muy larga, se crea una línea de orden de venta adicional de tipo Comentario para mantener el texto completo en el pedido de cliente en [!INCLUDE[d365fin](includes/d365fin_md.md)].

## <a name="see-also"></a>Consulte también
[Gestión de relaciones](marketing-relationship-management.md)  
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Cambiar las funciones que se muestran](ui-experiences.md)  
[Gestionar usuarios y permisos](ui-how-users-permissions.md)    
[Incorporación de la organización y los usuarios a Dynamics 365 (en línea)](/dynamics365/customer-engagement/admin/onboard-your-organization-and-users-to-dynamics-365-online)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  

