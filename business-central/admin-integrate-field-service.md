---
title: Integrar con Microsoft Dynamics 365 Field Service
description: Integre Business Central con Field Service.
ms.date: 02/21/2024
ms.topic: article
author: brentholtorf
ms.author: bholtorf
ms.reviewer: ivkoleti
ms.custom: bap-template
---

# Integrar con Microsoft Dynamics 365 Field Service

Las organizaciones de servicios requieren una aplicación integral en la que las finanzas, el inventario y las adquisiciones estén estrechamente vinculados con la prestación de servicios. Generan datos financieros con cada transacción. Cada orden de trabajo representa costes e ingresos, y cada recurso genera pérdidas y ganancias. Las interacciones con los clientes agregan movimientos en la contabilidad general. La integración entre [!INCLUDE [prod_short](includes/prod_short.md)] y [!INCLUDE [field-service-short](includes/field-service-short.md)] agiliza el proceso de extremo a extremo de gestión de operaciones de servicios y garantiza un flujo fluido de información entre los dos sistemas.  

Puede crear y administrar fácilmente órdenes de trabajo en [!INCLUDE [field-service-short](includes/field-service-short.md)], realizar un seguimiento del progreso de las tareas de servicio, asignar recursos y capturar detalles de consumo. Cuando completa una orden de trabajo en [!INCLUDE [field-service-short](includes/field-service-short.md)], la integración permite la transferencia fluida de datos a [!INCLUDE [prod_short](includes/prod_short.md)] para su posterior procesamiento.  

La integración también facilita la facturación y el cumplimiento de órdenes de trabajo en [!INCLUDE [prod_short](includes/prod_short.md)]. Puede generar facturas precisas basadas en las actividades de servicio y el consumo registrado en [!INCLUDE [field-service-short](includes/field-service-short.md)].  

Al integrar [!INCLUDE [prod_short](includes/prod_short.md)] con [!INCLUDE [field-service-short](includes/field-service-short.md)], no es necesario introducir datos manualmente ni duplicar esfuerzos. La integración también proporciona una visión integral de las operaciones y las finanzas del servicio, lo que permite una mejor toma de decisiones y eficiencia operativa.

## Requisitos previos

Debido a que [!INCLUDE [field-service-short](includes/field-service-short.md)] está construido sobre Dynamics 365 Sales, debe [configurar una conexión a Dataverse](/dynamics365/business-central/admin-how-to-set-up-a-dynamics-crm-connection#to-use-the-dataverse-connection-setup-assisted-setup-guide) y [habilitar la integración con Dynamics 365 Sales](/dynamics365/business-central/admin-prepare-dynamics-365-for-sales-for-integration#connection-settings-in-the-setup-guide).

### Permisos y roles de seguridad para cuentas de usuario

Cuando instala la solución de integración, se configuran los permisos para la cuenta de usuario de integración. Si se cambian esos permisos, es posible que deba restablecerlos. Para ello, reinstale la solución de integración desde la página **Configuración de conexión de Dynamics 365** eligiendo **Volver a implementar la solución de integración**. Las siguientes secciones enumeran los permisos y roles de seguridad que la solución implementa para cada aplicación.

#### Venta

* Administrador de integración de Dynamics 365 [!INCLUDE [prod_short](includes/prod_short.md)]
* Usuario de integración de Dynamics 365 [!INCLUDE [prod_short](includes/prod_short.md)]
* Usuario de disponibilidad de producto de Dynamics 365 [!INCLUDE [prod_short](includes/prod_short.md)]

#### Business Central

Los usuarios que publiquen diarios de proyectos deben tener el siguiente conjunto de permisos:

* Integración de Dynamics 365 Sales

#### Especialidad serv.

Para utilizar los datos integrados, los usuarios deben tener el siguiente rol de seguridad:

* Integración de Business Central Field Service

Por ejemplo, los usuarios deben tener este rol para conectar órdenes de trabajo a [!INCLUDE [prod_short](includes/prod_short.md)] para su procesamiento.

> [!NOTE]
> Asegúrese de que los usuarios estén asignados a los roles y perfiles de seguridad estándar en [!INCLUDE [field-service-short](includes/field-service-short.md)].  
>
> Para obtener más información sobre los perfiles de seguridad de las columnas en [!INCLUDE [field-service-short](includes/field-service-short.md)], vaya a [Roles de seguridad de Field Service](/dynamics365/field-service/users-licenses-permissions#field-service-security-roles).
>
> Los administradores deben agregar uno de los perfiles de seguridad de columna adecuados a los usuarios en Power Platform. Para obtener más información, vaya a [Agregar equipos o usuarios a un perfil de seguridad de columna para controlar el acceso](/power-platform/admin/add-teams-users-field-security-profile).

> [!NOTE]
> Para utilizar la acción **Abrir en Business Central** en Ventas, debe tener los siguientes privilegios para las siguientes tablas:
>
> * Debe tener permisos de **lectura** para la tabla Conexión de **Dynamics 365 Business Central** (nav_connection).
> * Debe tener permisos de **lectura**, **escritura** y **eliminación** para la tabla **Conexión de Dynamics 365 Business Central predeterminada** (nav_defaultconnection).

### Otras configuraciones en Field Service

En la página **Configuración de Field Service**, realice los siguientes cambios:

* En la pestaña **Compra**, borre el campo **Uso de productos agotados**. De lo contrario, es posible que reciba una advertencia de "agotado" cuando elija un producto que está agotado en [!INCLUDE [field-service-short](includes/field-service-short.md)], pero que está en stock en [!INCLUDE [prod_short](includes/prod_short.md)].
* En la pestaña **Orden de trabajo/Reserva**, desactive los conmutadores **Calcular precio** y **Calcular coste**. En el campo **Creación de la factura de la orden de trabajo**, elija **Nunca**.

> [!NOTE]
> Configurar una conexión con [!INCLUDE [field-service-short](includes/field-service-short.md)] elimina el emparejamiento entre recursos y productos. Para que los productos de [!INCLUDE [prod_short](includes/prod_short.md)] estén disponibles en [!INCLUDE [field-service-short](includes/field-service-short.md)], actualice el campo **Tipo de producto de Field Service** para que coincida con el campo **Tipo** en los elementos de [!INCLUDE [prod_short](includes/prod_short.md)]. Para obtener más información, vaya a [Crear un producto o servicio](/dynamics365/field-service/create-product-or-service#create-a-product-or-service).

## Configurar la integración en Business Central

Después de tener una conexión con Dataverse y Sales, puede configurar su integración con [!INCLUDE [field-service-short](includes/field-service-short.md)]. En la página **Configuración asistida** en [!INCLUDE [prod_short](includes/prod_short.md)], elija **Configurar integración en Dynamics 365 Field Service** para ejecutar la Guía de configuración asistida. Esta sección describe las configuraciones clave en la guía.

Para permitir que las personas publiquen el consumo de artículos y servicios en órdenes de trabajo de [!INCLUDE [field-service-short](includes/field-service-short.md)], especifique la **Plantilla de diario de proyecto** y el **Lote de diario de proyecto** que se usará para publicar el consumo de productos y servicios.

Dado que los servicios se expresan en duración en [!INCLUDE [field-service-short](includes/field-service-short.md)], especifique la **Unidad de medida de horas** que se utilizará para convertir duraciones en cantidades en [!INCLUDE [prod_short](includes/prod_short.md)].

También puede especificar cuándo se sincronizan los productos de la orden de trabajo y las líneas de servicio a [!INCLUDE [prod_short](includes/prod_short.md)]. Por ejemplo, pueden sincronizarse cuando se utilizan líneas de orden de trabajo o cuando alguien completa una orden de trabajo. Elija la opción apropiada en el campo **Sincronizar productos/servicios de órdenes de trabajo**.

Los productos y servicios de la orden de trabajo posterior se sincronizan con los diarios del proyecto en [!INCLUDE [prod_short](includes/prod_short.md)], puede elegir si desea publicar los diarios del proyecto manualmente. Elija la opción adecuada en el campo **Publicar automáticamente líneas de diarios de proyectos**:

* Cuando se completa una orden de trabajo.
* Cuando se utilizan productos o servicios de la orden de trabajo.

Después de finalizar la configuración, ejecute una sincronización completa desde la página **Configuración de integración de Dynamics 365 Field Service**. Esta acción sincroniza asignaciones de tablas para cosas como:

* Tareas de proyecto para proyectos con el conjunto **Aplicar vínculo de uso**. Esta sincronización hace que haya proyectos de [!INCLUDE [prod_short](includes/prod_short.md)] disponibles para selección en [!INCLUDE [field-service-short](includes/field-service-short.md)].
* Los recursos que no están bloqueados, no tienen **Usar hoja de tiempo** seleccionado, y tienen **Horas** especificadas como unidad de medida en la página **Configuración de integración de Dynamics 365 Field Service**.
* Productos de servicio (requiere que esté usando la experiencia Premium en [!INCLUDE [prod_short](includes/prod_short.md)]).

## Asignación de entidad de Field Service estándar para la sincronización

La base de la sincronización de datos es asignar las tablas y campos en [!INCLUDE [prod_short](includes/prod_short.md)] con las tablas y columnas en Dataverse para que puedan intercambiar los datos. La asignación ocurre a través de tablas de integración. Para obtener más información sobre las asignaciones de tablas, vaya a [Asignación de tablas y campos para sincronizar](/dynamics365/business-central/admin-how-to-modify-table-mappings-for-synchronization).

La integración con [!INCLUDE [field-service-short](includes/field-service-short.md)] presenta las siguientes asignaciones de tablas de integración estándar:

* **PJLINE-WORDERPRODUCT**: asigna productos de orden de trabajo en [!INCLUDE [field-service-short](includes/field-service-short.md)] para proyectar líneas de diario en [!INCLUDE [prod_short](includes/prod_short.md)].
* **PJLINE-WORDERSERVICE**: asigna servicios de orden de trabajo en [!INCLUDE [field-service-short](includes/field-service-short.md)] para proteger líneas de diario en [!INCLUDE [prod_short](includes/prod_short.md)].
* **PROJECTTASK** : asigna proyectos y tareas de proyecto en [!INCLUDE [prod_short](includes/prod_short.md)] a productos en proyectos externos en [!INCLUDE [field-service-short](includes/field-service-short.md)].
* **RESOURCE-BOOKABLERSC**: asigna recursos en [!INCLUDE [prod_short](includes/prod_short.md)] a recursos reservables en [!INCLUDE [field-service-short](includes/field-service-short.md)].
* **SVCITEM-CUSTASSET**: (solo experiencia Premium) asigna elementos de servicio en [!INCLUDE [prod_short](includes/prod_short.md)] a activos del cliente en [!INCLUDE [field-service-short](includes/field-service-short.md)].

## Usar datos en ambas aplicaciones

Las siguientes secciones describen las funciones donde puede utilizar los datos que provienen de [!INCLUDE [prod_short](includes/prod_short.md)] y [!INCLUDE [field-service-short](includes/field-service-short.md)].

### Especialidad serv.

Puede [crear órdenes de trabajo](/dynamics365/field-service/create-work-order) usando la **Cuenta de servicio** y **Cuenta de facturación** de [!INCLUDE [prod_short](includes/prod_short.md)]. En las órdenes de trabajo, debe seleccionar la **Tarea de proyecto de Business Central** en el campo **Proyecto externo** . Seleccionar un proyecto le permite sincronizar los productos y servicios de la orden de trabajo con la tarea del proyecto adecuada en [!INCLUDE [prod_short](includes/prod_short.md)].

Puede agregar artículos de inventario y no inventario como **Productos de orden de trabajo** en órdenes de trabajo y obtener la cantidad disponible y los costes y precios de [!INCLUDE [prod_short](includes/prod_short.md)]. Para obtener más información, vaya a [Crear una orden de trabajo desde el formulario de orden de trabajo y la lista de registros](/dynamics365/field-service/create-work-order#create-a-work-order-from-the-work-order-form-and-record-list).

Puede agregar productos del tipo servicio como **Servicios de orden de trabajo** y obtener costes y precios de [!INCLUDE [prod_short](includes/prod_short.md)]. Para obtener más información, vaya a [Pestaña Productos y servicios](/dynamics365/field-service/work-order-experience#products-and-services-tab).

> [!NOTE]
> Cuando el estado del producto o servicio en una orden de trabajo cambia de **Estimado** a **Usado** en [!INCLUDE [field-service-short](includes/field-service-short.md)], se sincronizarán con las líneas del diario del proyecto en [!INCLUDE [prod_short](includes/prod_short.md)].

Puede reservar un recurso y relacionar las **Reservas** con los servicios de órdenes de trabajo utilizando un **Recurso reservable** de [!INCLUDE [prod_short](includes/prod_short.md)].

### Business Central

Dependiendo de su configuración en la página **Configuración de integración de servicios de campo**, cuando las órdenes de trabajo incluyen productos y servicios, la información de consumo se transfiere y publica mediante un **Diario de proyecto** en [!INCLUDE [prod_short](includes/prod_short.md)].

Los valores **Cantidad a facturar** y **Duración a facturar** se copian en la carpeta **Cantidad. para transferir al campo Factura**. Según esos valores, puede crear y registrar facturas de ventas en [!INCLUDE [prod_short](includes/prod_short.md)] para facturar al cliente. Una vez contabilizada la factura o procesado el consumo en [!INCLUDE [prod_short](includes/prod_short.md)], la cantidad facturada y la cantidad consumida se muestran en la pestaña [!INCLUDE [prod_short](includes/prod_short.md)] en las páginas **Producto de orden de trabajo** y **Servicio de órdenes de trabajo**.  

Utilice la página **Líneas de planificación de proyecto** para realizar un seguimiento de la publicación y facturación del consumo en las órdenes de trabajo. Desde la página **Líneas de planificación de proyecto**, puede crear y registrar facturas de ventas en [!INCLUDE [prod_short](includes/prod_short.md)]. Luego, podrá sincronizarlas con [!INCLUDE [field-service-short](includes/field-service-short.md)] y realizar un seguimiento del estado de las facturas.

> [!NOTE]
> Los servicios de pedido de trabajo con una reserva que utiliza un recurso reservable que está acoplado a un recurso [!INCLUDE [prod_short](includes/prod_short.md)] se sincronizan con dos líneas del diario del proyecto: una línea de tipo **Presupuesto** para el recurso acoplado y otra línea de tipo **Facturable** para el producto que se está atendiendo.
>
> El producto que se elige en el servicio de orden de trabajo debe estar acoplado a un artículo del tipo **Servicio** en [!INCLUDE [prod_short](includes/prod_short.md)]. Además, la unidad de medida base para el artículo debe establecerse en la **Unidad de medida de horas** que se elige en la página **Configuración de integración de Dynamics 365 Field Service**.
>
> Puede crear una factura para un artículo del tipo **Servicio** desde la línea de planificación de proyecto facturable y utilizar la línea de planificación de proyecto presupuestario para registrar el coste con el recurso.

## Consulte también

[Integrar con Microsoft Dataverse mediante la sincronización de datos](admin-common-data-service.md)  
[Asignación de tablas y campos para sincronizar](admin-how-to-modify-table-mappings-for-synchronization.md)