---
title: Administrar clientes con Dynamics 365 for Sales | Documentos de Microsoft
description: "Puede usar Dynamics 365 for Sales desde Finance and Operations, Business edition para asignar datos y tener una integración y sincronización fluidas en el proceso de clientes potenciales a efectivo."
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: integration, synchronize, map
ms.date: 01/25/2018
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: b4e2e7bc1c2622d329c73ae5bf47b4accff10aa8
ms.openlocfilehash: cc1ad2ef812c073e570835e4018ce077b3b45494
ms.contentlocale: es-es
ms.lasthandoff: 03/22/2018

---
# <a name="managing-customers-and-sales-created-in-dynamics-365-for-sales"></a>Gestión de clientes y ventas creados en Dynamics 365 for Sales
Si utiliza Dynamics 365 for Sales para la interacción con el cliente, puede usar [!INCLUDE[d365fin](includes/d365fin_md.md)] para su procesamiento de pedidos y finanzas, y tener una integración fluida en el proceso de clientes potenciales a efectivo.

Al configurar su aplicación para integrarse con Dynamics 365 for Sales, tendrá acceso a los datos de ventas desde [!INCLUDE[d365fin](includes/d365fin_md.md)] y a la inversa en algunos casos. Esta integración permite trabajar con los tipos de datos y sincronizar los que son comunes a ambos servicios, como clientes, contactos e información de ventas, y mantener los datos actualizados en ambas ubicaciones.  

Por ejemplo, el vendedor en Dynamics 365 for Sales puede utilizar las listas de precios de [!INCLUDE[d365fin](includes/d365fin_md.md)] cuando se crea un pedido de venta. Cuando agrega el producto a la línea del pedido de venta en Dynamics 365 for Sales, también puede ver el nivel de inventario (disponibilidad) del producto desde [!INCLUDE[d365fin](includes/d365fin_md.md)].

Por el contrario, los procesadores de pedidos en [!INCLUDE[d365fin](includes/d365fin_md.md)] pueden manejar las características especiales de las órdenes de venta transferidas automática o manualmente desde Dynamics 365 for Sales, tales como crear automáticamente y publicar líneas de orden de venta válidas para artículos o recursos introducidos en Sales como productos fuera de catálogo. Para obtener más información, consulte la sección "Manejo de datos de pedidos de ventas especiales".  

## <a name="setting-up-the-connection"></a>Configuración de la conexión
Desde Inicio, podrá acceder a la guía de configuración asistida **Configuración de conexión de Dynamics 365 for Sales** que le ayuda a configurar la conexión. Una vez terminada, tendrá un acoplamiento perfecto de los registros de Dynamics 365 for Sales con los registros de [!INCLUDE[d365fin](includes/d365fin_md.md)].  

> [!NOTE]  
>   A continuación se explica la configuración asistida, pero puede efectuar las mismas tareas manualmente en la ventana **Configuración de conexión Dynamics 365 for Sales**.

En la guía de configuración asistida, puede elegir los datos que se sincronizarán entre los dos servicios. También puede especificar que desea importar la solución existente de Dynamics 365 for Sales. En ese caso, debe especificar una cuenta de usuario administrador.

### <a name="setting-up-the-user-account-for-importing-the-solution"></a>Configuración de la cuenta de usuario para importar la solución
Para importar una solución existente Dynamics 365 for Sales, la guía de configuración utiliza una cuenta administrativa. Esta cuenta debe ser un usuario válido de Dynamics 365 for Sales con los roles de seguridad siguientes:

* Administrador del sistema  
* Personalizador de solución  

Para obtener más información, vea [Crear usuarios y asignar roles de seguridad de Microsoft Finance and Operations, Business edition (en línea)](https://technet.microsoft.com/library/jj191623.aspx) en techNet y [Administrar usuarios y permisos](ui-how-users-permissions.md).  

Esta cuenta solo se utiliza durante la configuración. Una vez que la solución se importa en [!INCLUDE[d365fin](includes/d365fin_md.md)], la cuenta ya no se necesita.

### <a name="setting-up-the-user-account-for-synchronization"></a>Configuración de la cuenta de usuario para la sincronización
La integración se basa en una cuenta de usuario compartida. Por lo tanto, en su suscripción de Office 365 deberá crear un usuario dedicado que se usará para la sincronización entre los dos servicios. Esta cuenta ya debe ser un usuario válido en Dynamics 365 for Sales, pero no es necesario asignar roles de seguridad a la cuenta porque la guía de configuración lo hace automáticamente. Debe especificar esta cuenta de usuario una o varias veces en la guía de configuración, dependiendo de la sincronización que desea activar. Para obtener más información, vea [Crear usuarios y asignar roles de seguridad de Microsoft Finance and Operations, Business edition (en línea)](https://technet.microsoft.com/library/jj191623.aspx) en techNet.

Si elige habilitar *Disponibilidad del producto*, la cuenta de usuario de integración debe tener una clave de acceso a los servicios web. Es un proceso de dos pasos en la página [!INCLUDE[d365fin](includes/d365fin_md.md)] para esa cuenta de usuario; debe elegir el botón **Cambiar clave de servicio Web** y, en la guía de configuración de conexión de Dynamics 365 for Sales, debe especificar a dicho usuario como el usuario de servicio web de OData.

Si elige habilitar *Integración de pedido de venta*, deberá especificar un usuario que pueda controlar esta sincronización: el usuario de integración u otra cuenta de usuario.

### <a name="coupling-records"></a>Emparejamiento de registros
En la guía de configuración asistida, puede elegir la sincronización entre los dos servicios. Pero más tarde, también puede configurar determinados tipos de datos. A esto se le conoce como *emparejamiento* y esta sección proporciona recomendaciones de lo que debe tener en cuenta.

Por ejemplo, si desea ver las cuentas de Dynamics 365 for Sales como clientes en [!INCLUDE[d365fin](includes/d365fin_md.md)], debe emparejar los dos tipos de registros. No es muy complicado: abra la ventana **Lista de clientes** en [!INCLUDE[d365fin](includes/d365fin_md.md)] y hay una acción en la cinta para emparejar este datos con Dynamics 365 for Sales. A continuación, especifique qué clientes de [!INCLUDE[d365fin](includes/d365fin_md.md)] coinciden con cada cuenta de Dynamics 365 for Sales.

En determinadas áreas, la funcionalidad se basa en el emparejamiento de determinados conjuntos de datos antes que otros conjuntos de datos como se muestra en la lista siguiente:

* Clientes y cuentas  
  * Emparejar vendedores con usuarios de Dynamics 365 for Sales en primer lugar  
* Productos y recursos  
  * Emparejar unidades de medida con grupos de unidades de Dynamics 365 for Sales en primer lugar  
* Precios de productos y recursos  
  * Emparejar grupos de precios de cliente con precios de Dynamics 365 for Sales en primer lugar  

> [!NOTE]  
>   Si utiliza precios en divisas extranjeras, asegúrese de emparejar las divisas con las divisas de transacción de Dynamics 365 for Sales.

Los pedidos de venta de Dynamics 365 for Sales dependen de información adicional como clientes, unidades de medida, divisas, grupos de precios de cliente, productos o recursos. Para que los pedidos de venta de Dynamics 365 for Sales funcionen fluidamente, primero debe emparejar clientes, unidades de medida, divisas, grupos de precios de cliente, productos o recursos.

### <a name="synchronizing-records-fully"></a>Sincronización completa de los registros
Al final de la guía de configuración asistida, puede elegir la acción **Ejecutar sincronización completa** para iniciar la sincronización de todos los registros de [!INCLUDE[d365fin](includes/d365fin_md.md)] con todos los registros relacionados en la solución de Dynamics 365 for Sales conectada. En la ventana **Revisión de sinc. completa de CRM**, elija la acción **Iniciar**. La sincronización comienza a ejecutar los proyectos según las dependencias. Por ejemplo, los registros de divisa se sincronizan antes que los registros de cliente. La sincronización completa puede durar mucho tiempo, por lo que se ejecutará en segundo plano para que pueda seguir trabajando en [!INCLUDE[d365fin](includes/d365fin_md.md)].

Para comprobar el progreso de los proyectos individuales de una sincronización completa, desglose el campo **Estado mov. cola proyecto**, **Estado de proyecto de tabla de integ. de destino** o **Estado de proyecto de tabla de integ. de origen** en la ventana **Revisión de sinc. completa de CRM**.

En la ventana **Configuración de conexión Dynamics 365 for Sales**, puede obtener los detalles acerca de la sincronización completa en cualquier momento. Desde aquí también puede abrir la ventana **Lista de asignaciones de tablas de integración** para ver información detallada acerca de las tablas de Finance and Operations, Business edition y en la solución de Dynamics 365 for Sales que se deben sincronizar.  

## <a name="handling-special-sales-order-data"></a>Manejar datos de pedidos de ventas especiales
Las órdenes de venta en Dynamics 365 for Sales se transferirán automáticamente a [!INCLUDE[d365fin](includes/d365fin_md.md)] si selecciona la casilla **Crear automáticamente pedidos de venta** en la ventana **Configuración de conexión de Microsoft Dynamics 365 for Sales**. En dichos pedidos de venta, el campo **Nombre** del pedido original se transfiere y se asigna al campo **Número de documento externo** del pedido de venta en [!INCLUDE[d365fin](includes/d365fin_md.md)].

Esto también puede funcionar si el pedido de cliente original contiene productos fuera de catálogo, es decir, elementos o recursos que no están registrados en ninguno de los productos. En ese caso, debe rellenar los campos **Tipo producto fuera de catálogo** y **N.º producto fuera de catálogo** en la ventana **Conf. ventas y cobros**, para asignar estas ventas de productos no registrados a un número del producto especificado o recurso para el análisis financiero.

Si la descripción del artículo en el pedido de venta original es muy larga, se crea una línea de orden de venta adicional de tipo Comentario para mantener el texto completo en el pedido de cliente en [!INCLUDE[d365fin](includes/d365fin_md.md)].

## <a name="see-also"></a>Consulte también
[Gestión de relaciones](marketing-relationship-management.md)  
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Personalizar la experiencia de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-experiences.md)  
[Gestionar usuarios y permisos](ui-how-users-permissions.md)    
[Incorporación de la organización y los usuarios a Finance and Operations, Business edition (en línea)](https://www.microsoft.com/en-US/Dynamics/crm-customer-center/onboard-your-organization-and-users-to-dynamics-365-online.aspx)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
## [!INCLUDE[d365fin](includes/training_link_md.md)]

