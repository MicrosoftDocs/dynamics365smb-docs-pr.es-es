---
title: Administrar las relaciones con el cliente mediante Dynamics 365 for Sales desde Dynamics 365 for Financials | Documentos de Microsoft
description: "Si utiliza Dynamics 365 for Sales para la interacción con el cliente, puede usar Dynamics 365 for Financials para su procesamiento de pedidos y finanzas, y tener una integración fluida en el proceso de clientes potenciales a efectivo"
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: integration, synchronize, map
ms.date: 03/05/2017
ms.author: edupont
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: c0291cc316b49e1f1f4f2196745914daca158f61
ms.contentlocale: es-es
ms.lasthandoff: 05/04/2017

---
# <a name="managing-your-customer-relationships-using-dynamics-365-for-sales-from-inside-dynamics-365-for-financials"></a>Administrar las relaciones con el cliente mediante Dynamics 365 for Sales desde Dynamics 365 for Financials
Si utiliza Dynamics 365 for Sales para la interacción con el cliente, puede usar [!INCLUDE[d365fin](includes/d365fin_md.md)] para su procesamiento de pedidos y finanzas, y tener una integración fluida en el proceso de clientes potenciales a efectivo

Al configurar su aplicación para integrarse con Dynamics 365 for Sales, tendrá acceso a los datos de ventas desde [!INCLUDE[d365fin](includes/d365fin_md.md)] y a la inversa en algunos casos. Esta integración permite trabajar con los tipos de datos y sincronizar los que son comunes a ambos servicios, como clientes, contactos e información de ventas, y mantener los datos actualizados en ambas ubicaciones.  

**Nota**: En la versión actual de [!INCLUDE[d365fin](includes/d365fin_md.md)], Dynamics 365 for Sales se denomina Dynamics CRM. Para simplificar, en el resto de este producto se utiliza la terminología que se utiliza en [!INCLUDE[d365fin](includes/d365fin_md.md)].  

Por ejemplo, el vendedor en Dynamics CRM puede utilizar las listas de precios de [!INCLUDE[d365fin](includes/d365fin_md.md)] cuando se crea un pedido de venta. Cuando agrega el producto a la línea del pedido de venta en Dynamics CRM, también puede ver el nivel de inventario (disponibilidad) del producto desde [!INCLUDE[d365fin](includes/d365fin_md.md)]. Estos datos se publican como parte de la guía de configuración asistida, **Configuración de conexión de Dynamics CRM**.  

**Nota**: Esta funcionalidad que requiere que la experiencia esté definida en **Conjunto de aplicaciones**. Para obtener más información, consulte [Personalizar la experiencia de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-experiences.md).  

## <a name="setting-up-the-connection"></a>Configuración de la conexión
Desde Inicio, podrá acceder a la guía de configuración asistida **Configuración de conexión de Dynamics CRM** que le ayuda a configurar la conexión. Una vez terminada, tendrá un acoplamiento perfecto de los registros de Dynamics CRM con los registros de [!INCLUDE[d365fin](includes/d365fin_md.md)].  

**Nota**: A continuación se explica la configuración asistida, pero puede efectuar las mismas tareas manualmente en la ventana **Configuración de conexión CRM**.

En la guía de configuración asistida, puede elegir los datos que se sincronizarán entre los dos servicios. También puede especificar que desea importar la solución existente de Dynamics CRM. En ese caso, debe especificar una cuenta de usuario administrador.

### <a name="setting-up-the-user-account-for-importing-the-solution"></a>Configuración de la cuenta de usuario para importar la solución
Para importar una solución existente Dynamics CRM, la guía de configuración utiliza una cuenta administrativa. Esta cuenta debe ser un usuario válido de Dynamics CRM con los roles de seguridad siguientes:

* Administrador del sistema  
* Personalizador de solución  

Para obtener más información, vea [Crear usuarios y asignar roles de seguridad de Microsoft Dynamics 365 (en línea)](https://technet.microsoft.com/library/jj191623.aspx) en techNet y [Administrar usuarios y permisos](ui-how-users-permissions.md).  

Esta cuenta solo se utiliza durante la configuración. Una vez que la solución se importa en [!INCLUDE[d365fin](includes/d365fin_md.md)], la cuenta ya no se necesita.

### <a name="setting-up-the-user-account-for-synchronization"></a>Configuración de la cuenta de usuario para la sincronización
La integración se basa en una cuenta de usuario compartida. Por lo tanto, en su suscripción de Office 365 deberá crear un usuario dedicado que se usará para la sincronización entre los dos servicios. Esta cuenta ya debe ser un usuario válido en Dynamics CRM, pero no es necesario asignar roles de seguridad a la cuenta porque la guía de configuración lo hace automáticamente. Debe especificar esta cuenta de usuario una o varias veces en la guía de configuración, dependiendo de la sincronización que desea activar. Para obtener más información, vea [Crear usuarios y asignar roles de seguridad de Microsoft Dynamics 365 (en línea)](https://technet.microsoft.com/library/jj191623.aspx) en techNet.

Si elige habilitar *Disponibilidad del producto*, la cuenta de usuario de integración debe tener una clave de acceso a los servicios web. Es un proceso de dos pasos en la página [!INCLUDE[d365fin](includes/d365fin_md.md)] para esa cuenta de usuario; debe elegir el botón **Cambiar clave de servicio Web** y, en la guía de configuración de conexión de CRM, debe especificar a dicho usuario como el usuario de servicio web de OData.

Si elige habilitar *Integración de pedido de venta*, deberá especificar un usuario que pueda controlar esta sincronización: el usuario de integración u otra cuenta de usuario.

### <a name="coupling-records"></a>Emparejamiento de registros
En la guía de configuración asistida, puede elegir la sincronización entre los dos servicios. Pero más tarde, también puede configurar determinados tipos de datos. A esto se le conoce como *emparejamiento* y esta sección proporciona recomendaciones de lo que debe tener en cuenta.

Por ejemplo, si desea ver las cuentas de Dynamics CRM como clientes en [!INCLUDE[d365fin](includes/d365fin_md.md)], debe emparejar los dos tipos de registros. No es muy complicado: abra la ventana **Lista de clientes** en [!INCLUDE[d365fin](includes/d365fin_md.md)] y hay una acción en la cinta para emparejar este datos con Dynamics CRM. A continuación, especifique qué clientes de [!INCLUDE[d365fin](includes/d365fin_md.md)] coinciden con cada cuenta de Dynamics CRM.

En determinadas áreas, la funcionalidad se basa en el emparejamiento de determinados conjuntos de datos antes que otros conjuntos de datos como se muestra en la lista siguiente:

* Clientes y cuentas  
  * Emparejar vendedores con usuarios de Dynamics CRM en primer lugar  
* Productos y recursos  
  * Emparejar unidades de medida con grupos de unidades de Dynamics CRM en primer lugar  
* Precios de productos y recursos  
  * Emparejar grupos de precios de cliente con precios de Dynamics CRM en primer lugar  

**Nota**: Si utiliza precios en divisas extranjeras, asegúrese de emparejar las divisas con las divisas de transacción de Dynamics CRM.

Los pedidos de venta de Dynamics CRM dependen de información adicional como clientes, unidades de medida, divisas, grupos de precios de cliente, productos o recursos. Para que los pedidos de venta de Dynamics CRM funcionen fluidamente, primero debe emparejar clientes, unidades de medida, divisas, grupos de precios de cliente, productos o recursos.

### <a name="synchronizing-records-fully"></a>Sincronización completa de los registros
Al final de la guía de configuración asistida, puede elegir la acción **Ejecutar sincronización completa** para iniciar la sincronización de todos los registros de [!INCLUDE[d365fin](includes/d365fin_md.md)] con todos los registros relacionados en la solución de Dynamics CRM conectada. En la ventana **Revisión de sinc. completa de CRM**, elija la acción **Iniciar**. La sincronización comienza a ejecutar los proyectos según las dependencias. Por ejemplo, los registros de divisa se sincronizan antes que los registros de cliente. La sincronización completa puede durar mucho tiempo, por lo que se ejecutará en segundo plano para que pueda seguir trabajando en [!INCLUDE[d365fin](includes/d365fin_md.md)].

Para comprobar el progreso de los proyectos individuales de una sincronización completa, desglose el campo **Estado mov. cola proyecto**, **Estado de proyecto de tabla de integ. de destino** o **Estado de proyecto de tabla de integ. de origen** en la ventana **Revisión de sinc. completa de CRM**.

En la ventana **Configuración de conexión CRM**, puede obtener los detalles acerca de la sincronización completa en cualquier momento. Desde aquí también puede abrir la ventana **Lista de asignaciones de tablas de integración** para ver información detallada acerca de las tablas de Financials y en la solución Dynamics CRM que se deben sincronizar.

## <a name="see-also"></a>Consulte también
[Gestión de relaciones](marketing-relationship-management.md)  
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)](ui-work-product.md)  
[Personalizar la experiencia de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-experiences.md)  
[Administrar usuarios y permisos](ui-how-users-permissions.md)    
[Incorporación de la organización y los usuarios a Dynamics 365 (en línea)](https://www.microsoft.com/en-US/Dynamics/crm-customer-center/onboard-your-organization-and-users-to-dynamics-365-online.aspx)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]
