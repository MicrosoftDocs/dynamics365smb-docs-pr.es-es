---
title: Administrar clientes con Dynamics 365 for Sales | Documentos de Microsoft
description: Puede usar Dynamics 365 for Sales desde Business Central para asignar datos y tener una integración y sincronización fluidas en el proceso de clientes potenciales a efectivo.
documentationcenter: ''
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: integration, synchronize, map, Sales
ms.date: 04/01/2019
ms.author: bholtorf
ms.openlocfilehash: 3cc053158581d4fc9b87dc3e505a23ed809c1c8f
ms.sourcegitcommit: 04581558f6c5488c705a7ac392cf297be10b5f4f
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 06/06/2019
ms.locfileid: "1620866"
---
# <a name="using-dynamics-365-for-sales-from-business-central"></a>Uso de Dynamics 365 for Sales desde Business Central
Si lo utiliza Dynamics 365 for Sales para la interacción con el cliente, puede disfrutar de una integración perfecta en el proceso de clientes potenciales a efectivo mediante el uso de [!INCLUDE[d365fin](includes/d365fin_md.md)] para las actividades de backend como el procesamiento de pedidos, la gestión de inventario y la gestión de sus finanzas.

> [!NOTE]
> Este tema se supone que está utilizando las versiones en línea de [!INCLUDE[d365fin](includes/d365fin_md.md)] y Sales. Puede mezclar versiones en línea y locales, pero eso requiere una configuración especial. Para obtener más información, vea [Preparación para integrar al Dynamics 365 for Sales On-Premises](/dynamics365/business-central/dev-itpro/administration/prepare-dynamics-365-for-sales-for-integration).

La integración de las aplicaciones le permite acceder a los datos de Sales desde [!INCLUDE[d365fin](includes/d365fin_md.md)] y, en algunos casos, al revés. Puede trabajar con los datos y sincronizar los que tienen en común ambos servicios, como clientes, contactos e información de ventas, y mantener los datos actualizados en ambas aplicaciones.  

Por ejemplo, un vendedor en Sales puede utilizar las listas de precios de [!INCLUDE[d365fin](includes/d365fin_md.md)] cuando se crea un pedido de venta. Cuando agrega el producto a la línea del pedido de venta en Sales, puede ver el nivel de inventario (disponibilidad) del producto desde [!INCLUDE[d365fin](includes/d365fin_md.md)].

Por el contrario, los procesadores de pedidos en [!INCLUDE[d365fin](includes/d365fin_md.md)] pueden gestionar los pedidos de venta que se transfieren de forma automática o manual desde ventas. Por ejemplo, pueden crear y registrar líneas de pedido de venta para productos o recursos que se introdujeron en Sales como productos fuera de catálogo. Para obtener más información, consulte [Manejo de datos de pedidos de ventas especiales](marketing-integrate-dynamicscrm.md#handling-sales-order-data).

> [!IMPORTANT]  
> [!INCLUDE[d365fin](includes/d365fin_md.md)] se integra solo con Dynamics 365 for Sales. Otras aplicaciones de Dynamics 365 que cambian el flujo de trabajo estándar o el modelo de datos en Sales, por ejemplo, Project Service Automation, pueden romper la integración entre [!INCLUDE[d365fin](includes/d365fin_md.md)] y Sales.

### <a name="coupling-records"></a>Emparejamiento de registros
La guía de configuración asistida le permite elegir los datos que desea sincronizar. Más tarde, también puede configurar la sincronización de registros específicos. Esto se conoce como *emparejamiento*. Por ejemplo, puede emparejar una cuenta específica en Sales con un cliente específico en [!INCLUDE[d365fin](includes/d365fin_md.md)]. Esta sección describe lo que se debe tener en cuenta al emparejar registros.

Por ejemplo, si desea ver las cuentas de Sales como clientes en [!INCLUDE[d365fin](includes/d365fin_md.md)], debe emparejar los dos tipos de registros. Para ello, en la página de lista **Clientes** en [!INCLUDE[d365fin](includes/d365fin_md.md)], utilice la acción **Configurar emparejamiento**. A continuación, especifique qué clientes de [!INCLUDE[d365fin](includes/d365fin_md.md)] coinciden con cada cuenta de Sales.

También puede crear (y emparejar) una cuenta en Sales basada, por ejemplo, en el registro de cliente de [!INCLUDE[d365fin](includes/d365fin_md.md)] mediante **Crear cuenta en Dynamics 365 for Sales**, o viceversa, mediante **Crear cliente en [!INCLUDE[d365fin](includes/d365fin_md.md)]**.

Al configurar el emparejamiento entre dos registros, también puede solicitar manualmente que el registro actual, por ejemplo, un cliente, se sobrescriba inmediatamente con los datos de cuenta desde Sales (o desde [!INCLUDE[d365fin](includes/d365fin_md.md)]) mediante la acción **Sincronizar ahora**. Acción **Sincronizar ahora** que preguntará si desea sobrescribir los datos de registro de Sales o [!INCLUDE[d365fin](includes/d365fin_md.md)].

En algunos casos se deben emparejar ciertos conjuntos de datos antes que otros, como se muestra en la siguiente tabla.

|Datos|Qué se debe emparejar primero|
|-----|----|
|Clientes y cuentas|Emparejar vendedores con usuarios de Sales|
|Productos y recursos|Emparejar unidades de medida con grupos de unidades de Sales|
|Precios de productos y recursos|Emparejar grupos de precios de cliente con precios de Sales|

> [!NOTE]  
> Si sus precios o clientes utilizan precios en divisas extranjeras, asegúrese de emparejar las divisas con las divisas de transacción de Sales.

En Sales, los pedidos de venta dependen de información como clientes, unidades de medida, divisas, grupos de precios de cliente, productos o recursos. Para que la integración con los pedidos de venta funcione, debe emparejar clientes, unidades de medida, divisas, grupos de precios de cliente, productos o recursos.

### <a name="fully-synchronizing-records"></a>Sincronización completa de los registros
Al final de la guía de configuración asistida, puede elegir la acción **Ejecutar sincronización completa** para iniciar la sincronización de todos los registros de [!INCLUDE[d365fin](includes/d365fin_md.md)] con todos los registros relacionados en Sales. En la página **Revisión de sinc. completa de Dynamics 365 for Sales**, elija la acción **Iniciar**. La sincronización de relleno puede tardar algún tiempo en completarse, pero puede continuar trabajando en [!INCLUDE[d365fin](includes/d365fin_md.md)] mientras se ejecuta en segundo plano.

Para comprobar el progreso de los trabajos individuales en una sincronización completa, en la página **Revisión de sinc. completa de Dynamics 365 for Sales**, seleccione un registro para ver los detalles. Para actualizar el estado durante la sincronización, actualice la página.

En la página **Configuración de conexión de Microsoft Dynamics 365**, puede obtener los detalles acerca de la sincronización completa en cualquier momento. Desde aquí también puede abrir la página **Lista de asignaciones de tablas de integración** para ver información detallada acerca de las tablas de [!INCLUDE[d365fin](includes/d365fin_md.md)] y en Sales que se deben sincronizar.

## <a name="handling-sales-order-data"></a>Manejar datos de pedidos de venta
Los pedidos de venta que los usuarios envían en [!INCLUDE[crm_md](includes/crm_md.md)] se transferirán a [!INCLUDE[d365fin](includes/d365fin_md.md)] si selecciona la casilla **Crear automáticamente pedidos de venta** en la página **Configuración de conexión de Microsoft Dynamics 365**.
Como alternativa, puede convertir manualmente los pedidos de venta presentados desde [!INCLUDE[crm_md](includes/crm_md.md)] utilizando la acción **Crear en [!INCLUDE[d365fin](includes/d365fin_md.md)]** disponible en la página **Pedidos de venta - Dynamics 365 for Sales**.
En dichos pedidos de venta, el campo **Nombre** del pedido original se transfiere y se asigna al campo **Número de documento externo** del pedido de venta en [!INCLUDE[d365fin](includes/d365fin_md.md)].

Esto también puede funcionar si el pedido de cliente original contiene productos fuera de catálogo, es decir, elementos o recursos que no están registrados en ninguna de las aplicaciones. En ese caso, debe rellenar los campos **Tipo producto fuera de catálogo** y **N.º producto fuera de catálogo** en la página **Conf. ventas y cobros**, para asignar estas ventas de productos no registrados a un número del producto especificado o recurso para el análisis financiero.

Si la descripción del artículo en el pedido de venta original es larga, se crea una línea de orden de venta adicional del tipo **Comentario** para mantener el texto completo en el pedido de cliente en [!INCLUDE[d365fin](includes/d365fin_md.md)].

Las actualizaciones de los campos de cabecera de pedido de venta, como Fecha de último envío o Fecha entrega requerida, que se asignan en **Asignación de tablas de integración** de PEDIDODEVENTA-PEDIDO se sincronizan periódicamente con [!INCLUDE[crm_md](includes/crm_md.md)]. Procesos como la liberación de un pedido de venta y el envío o facturación de un pedido de venta se registran contabilizan en la escala de tiempo del pedido de venta en [!INCLUDE[crm_md](includes/crm_md.md)]. Para obtener más información, consulte [Introducción a las fuentes de actividades](https://docs.microsoft.com/en-us/dynamics365/customer-engagement/developer/introduction-activity-feeds).

## <a name="handling-sales-quotes-data"></a>Manejar datos de ofertas de venta
Las ofertas de venta que se activan en [!INCLUDE[crm_md](includes/crm_md.md)] se transferirán a [!INCLUDE[d365fin](includes/d365fin_md.md)] si selecciona la casilla **Procesar automáticamente ofertas** en la página **Configuración de conexión de Microsoft Dynamics 365**.
Como alternativa, puede convertir manualmente las ofertas de venta activadas desde [!INCLUDE[crm_md](includes/crm_md.md)] utilizando la acción **Procesar en [!INCLUDE[d365fin](includes/d365fin_md.md)]** en la página **Ofertas de venta - Dynamics 365 for Sales**.
En dichas ofertas de venta, el campo **Nombre** de la oferta original se transfiere y se asigna al campo **Número de documento externo** del pedido de venta en [!INCLUDE[d365fin](includes/d365fin_md.md)]. También se transfiere el campo **En vigor hasta** de la oferta y se asigna al campo **Oferta válida hasta** en la oferta de venta en [!INCLUDE[d365fin](includes/d365fin_md.md)].  

Las ofertas de venta pasan por muchas revisiones mientras se están finalizando. El procesamiento manual y automático de las ofertas de venta en [!INCLUDE[d365fin](includes/d365fin_md.md)] garantiza que las versiones anteriores de las ofertas de venta se archiven antes de procesar nuevas revisiones de ofertas de venta desde [!INCLUDE[crm_md](includes/crm_md.md)]. 

## <a name="handling-posted-sales-invoices-customer-payments-and-statistics"></a>Gestión de histórico de facturas de venta, pagos de cliente y estadísticas
Después de completar el pedido de venta, se crearán las facturas correspondientes. Cuando se factura un pedido de venta, se puede transferir el histórico de facturas de venta a [!INCLUDE[crm_md](includes/crm_md.md)] si selecciona **Crear factura en [!INCLUDE[crm_md](includes/crm_md.md)]** en la página de histórico de facturas de venta. Las facturas registradas se transfieren a [!INCLUDE[crm_md](includes/crm_md.md)] con el estado **Facturado**. Una vez recibido el pago del cliente para la factura de venta en [!INCLUDE[d365fin](includes/d365fin_md.md)], el estado de la factura de venta cambiará a **Pagado** con el motivo del estado establecido en **Parcial**, si se ha pagado parcialmente, o **Completo**, si se ha pagado completamente, cuando ejecute **Actualizar estadísticas de cuentas** en la página del cliente en [!INCLUDE[d365fin](includes/d365fin_md.md)]. **Actualizar estadísticas de cuenta** también actualizará valores como Saldo y Total ventas en el cuadro informativo de estadísticas de cuentas de [!INCLUDE[d365fin](includes/d365fin_md.md)] en [!INCLUDE[crm_md](includes/crm_md.md)].
Alternativamente, puede hacer que los trabajos programados (Estadísticas de clientes y POSTEDSALESINV-INV) ejecuten automáticamente estos dos procesos en segundo plano. 

## <a name="see-also"></a>Consulte también
[Preparación para integrar en Dynamics 365 for Sales On-Premises](/dynamics365/business-central/dev-itpro/administration/prepare-dynamics-365-for-sales-for-integration)  
[Gestión de relaciones](marketing-relationship-management.md)  
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Cambiar las funciones que se muestran](ui-experiences.md)  
[Gestionar usuarios y permisos](ui-how-users-permissions.md)    
[Incorporación de la organización y los usuarios a Dynamics 365 (online)](/dynamics365/customer-engagement/admin/onboard-your-organization-and-users-to-dynamics-365-online)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
