---
title: Administrar clientes con Dynamics 365 Sales | Documentos de Microsoft
description: Puede usar Dynamics 365 Sales desde Business Central con integración y sincronización fluidas en el proceso de clientes potenciales a efectivo.
documentationcenter: ''
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'integration, synchronize, map, Sales'
ms.search.forms: '9980, 5341, 5349, 5330, 1817, 5342, 5337, 5336, 5331, 5343, 5334, 5346, 5348, 5329, 5380, 5353, 5381, 5351, 5333, 5360, 5373, 5371, 5340, 5345, 5362, 1313, 5361, 1876, 5339, 5338, 5335, 5332, 6250'
ms.date: 09/16/2022
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# <a name="use-dynamics-365-sales-from-business-central"></a>Usar Dynamics 365 Sales desde Business Central
Si utiliza Dynamics 365 Sales para la interacción con el cliente, puede disfrutar de una integración perfecta en el proceso de clientes potenciales a efectivo mediante el uso de [!INCLUDE[prod_short](includes/prod_short.md)] para las actividades de backend como el procesamiento de pedidos, la gestión de inventario y la gestión de sus finanzas.

Para poder utilizar las capacidades de integración, el administrador del sistema debe configurar la conexión y definir los usuarios en [!INCLUDE[crm_md](includes/crm_md.md)]. Para obtener más información, vea [Integración con Dynamics 365 Sales](admin-prepare-dynamics-365-for-sales-for-integration.md).

> [!NOTE]
> Estos pasos describen el proceso de integración de las versiones en línea de [!INCLUDE[crm_md](includes/crm_md.md)] y [!INCLUDE[prod_short](includes/prod_short.md)]. Para obtener información sobre la configuración local, consulte [Preparación de Dynamics 365 Sales para la integración local](/dynamics365/business-central/dev-itpro/administration/prepare-dynamics-365-for-sales-for-integration).

La integración de las aplicaciones le permite acceder a los datos de Sales desde [!INCLUDE[prod_short](includes/prod_short.md)] y, en algunos casos, al revés. Puede trabajar con los datos y sincronizar los que tienen en común ambos servicios, como clientes, contactos e información de ventas, y mantener los datos actualizados en ambas aplicaciones.  

Por ejemplo, un vendedor en [!INCLUDE[crm_md](includes/crm_md.md)] puede utilizar las listas de precios de [!INCLUDE[prod_short](includes/prod_short.md)] cuando se crea un pedido de venta. Cuando agrega el producto a la línea del pedido de venta en [!INCLUDE[crm_md](includes/crm_md.md)], puede ver el nivel de inventario (disponibilidad) del producto desde [!INCLUDE[prod_short](includes/prod_short.md)].

Por el contrario, los procesadores de pedidos en [!INCLUDE[prod_short](includes/prod_short.md)] pueden gestionar los pedidos de venta que se transfieren de forma automática o manual desde [!INCLUDE[crm_md](includes/crm_md.md)]. Por ejemplo, pueden crear y registrar líneas de pedido de venta para productos o recursos que se introdujeron en [!INCLUDE[crm_md](includes/crm_md.md)] como productos fuera de catálogo. Para obtener más información, consulte [Manejo de datos de pedidos de ventas especiales](marketing-integrate-dynamicscrm.md#handling-sales-order-data).

> [!IMPORTANT]  
> [!INCLUDE[prod_short](includes/prod_short.md)] se integra solo con [!INCLUDE[crm_md](includes/crm_md.md)]. Otras aplicaciones de Dynamics 365 que cambian el flujo de trabajo estándar o el modelo de datos en [!INCLUDE[crm_md](includes/crm_md.md)], por ejemplo, Project Service Automation, pueden romper la integración entre [!INCLUDE[prod_short](includes/prod_short.md)] y [!INCLUDE[crm_md](includes/crm_md.md)].

## <a name="coupling-records"></a>Emparejamiento de registros
La guía de configuración asistida le permite elegir los datos que desea sincronizar. Más tarde, también puede configurar la sincronización de registros específicos. Esto se conoce como *emparejamiento*. Por ejemplo, puede emparejar una cuenta específica en [!INCLUDE[crm_md](includes/crm_md.md)] con un cliente específico en [!INCLUDE[prod_short](includes/prod_short.md)]. Esta sección describe lo que se debe tener en cuenta al emparejar registros.

Por ejemplo, si desea ver las cuentas de [!INCLUDE[crm_md](includes/crm_md.md)] como clientes en [!INCLUDE[prod_short](includes/prod_short.md)], debe emparejar los dos tipos de registros. Para ello, en la página de lista **Clientes** en [!INCLUDE[prod_short](includes/prod_short.md)], utilice la acción **Configurar emparejamiento**. A continuación, especifique qué clientes de [!INCLUDE[prod_short](includes/prod_short.md)] coinciden con cada cuenta de [!INCLUDE[crm_md](includes/crm_md.md)].

También puede crear (y emparejar) una cuenta en [!INCLUDE[crm_md](includes/crm_md.md)] basada, por ejemplo, en el registro de cliente de [!INCLUDE[prod_short](includes/prod_short.md)] mediante **Crear cuenta en Dynamics 365 Sales**, o viceversa, mediante **Crear cliente en [!INCLUDE[prod_short](includes/prod_short.md)]**.

Al configurar el emparejamiento entre dos registros, también puede solicitar manualmente que el registro actual, por ejemplo, un cliente, se sobrescriba inmediatamente con los datos de cuenta desde Sales (o desde [!INCLUDE[prod_short](includes/prod_short.md)]) mediante la acción **Sincronizar ahora**. Acción **Sincronizar ahora** que preguntará si desea sobrescribir los datos de registro de Sales o [!INCLUDE[prod_short](includes/prod_short.md)].

En algunos casos se deben emparejar ciertos conjuntos de datos antes que otros, como se muestra en la siguiente tabla.

|Datos|Qué se debe emparejar primero|
|-----|----|
|Clientes y cuentas|Emparejar vendedores con usuarios de [!INCLUDE[crm_md](includes/crm_md.md)]|
|Productos y recursos|Emparejar unidades de medida con grupos de unidades de [!INCLUDE[crm_md](includes/crm_md.md)]|
|Precios de productos y recursos|Emparejar grupos de precios de cliente con precios de [!INCLUDE[crm_md](includes/crm_md.md)]|

> [!NOTE]  
> Si sus precios o clientes utilizan precios en divisas extranjeras, asegúrese de emparejar las divisas con las divisas de transacción de Sales.

En [!INCLUDE[crm_md](includes/crm_md.md)], los pedidos de venta dependen de información como clientes, unidades de medida, divisas, grupos de precios de cliente, productos o recursos. Para que la integración con los pedidos de venta funcione, debe emparejar clientes, unidades de medida, divisas, grupos de precios de cliente, productos o recursos.

## <a name="fully-synchronizing-records"></a>Sincronización completa de los registros
Al final de la guía de configuración asistida, puede elegir la acción **Ejecutar sincronización completa** para iniciar la sincronización de todos los registros de [!INCLUDE[prod_short](includes/prod_short.md)] con todos los registros relacionados en [!INCLUDE[crm_md](includes/crm_md.md)]. En la página **Revisión de sinc. completa de Dynamics 365 Sales**, elija la acción **Iniciar**. La sincronización completa puede tardar algún tiempo en completarse, pero puede continuar trabajando en [!INCLUDE[prod_short](includes/prod_short.md)] mientras se ejecuta en segundo plano.

Para comprobar el progreso de los trabajos individuales en una sincronización completa, en la página **Revisión de sinc. completa de Dynamics 365 Sales**, seleccione un registro para ver los detalles. Para actualizar el estado durante la sincronización, actualice la página.

En la página **Configuración de conexión de Microsoft Dynamics 365**, puede obtener los detalles acerca de la sincronización completa en cualquier momento. Desde aquí también puede abrir la página **Lista de asignaciones de tablas de integración** para ver información detallada acerca de las tablas de [!INCLUDE[prod_short](includes/prod_short.md)] y en Sales que se deben sincronizar.

## <a name="handling-sales-order-data"></a>Manejar datos de pedidos de venta
Los pedidos de venta que los usuarios envían en [!INCLUDE[crm_md](includes/crm_md.md)] se transferirán automáticamente a [!INCLUDE[prod_short](includes/prod_short.md)] si selecciona la casilla **Crear automáticamente pedidos de venta** en la página **Configuración de conexión de Microsoft Dynamics 365**.
Como alternativa, puede convertir manualmente los pedidos de venta presentados desde [!INCLUDE[crm_md](includes/crm_md.md)] utilizando la acción **Crear en [!INCLUDE[prod_short](includes/prod_short.md)]** disponible en la página **Pedidos de venta - Dynamics 365 for Sales**.
En dichos pedidos de venta, el campo **Nombre** del pedido original se transfiere y se asigna al campo **Número de documento externo** del pedido de venta en [!INCLUDE[prod_short](includes/prod_short.md)].

Esto también puede funcionar si el pedido de cliente original contiene productos fuera de catálogo, es decir, elementos o recursos que no están registrados en ninguna de las aplicaciones. En ese caso, debe rellenar los campos **Tipo producto fuera de catálogo** y **N.º producto fuera de catálogo** en la página **Configuración de ventas y cobros**, para que las ventas de productos no registrados se asignen a un producto o recurso especificado.

> [!NOTE]
> No puede asignar una inserción a un producto o recurso en [!INCLUDE[prod_short](includes/prod_short.md)] que se combina con un producto en [!INCLUDE[crm_md](includes/crm_md.md)]. Para permitir las inserciones, le recomendamos que cree un producto o recurso específicamente para ese propósito y no lo combine con un producto en [!INCLUDE[crm_md](includes/crm_md.md)]. 

Si la descripción del artículo en el pedido de venta original es larga, se crea una línea de orden de venta adicional del tipo **Comentario** para mantener el texto completo en el pedido de cliente en [!INCLUDE[prod_short](includes/prod_short.md)].

Las actualizaciones de los campos de las cabeceras de los pedidos de venta, como los campos Fecha de último envío o Fecha entrega requerida, que se asignan en la asignación de tabla de integración **PEDIDO DE VENTAS-PEDIDO** se sincronizan periódicamente con [!INCLUDE[crm_md](includes/crm_md.md)]. Procesos como la liberación y el envío o facturación de un pedido de venta se registran contabilizan en la escala de tiempo del pedido de venta en [!INCLUDE[crm_md](includes/crm_md.md)]. Para obtener más información, consulte [Introducción a las fuentes de actividades](/dynamics365/sales-enterprise/manage-activities). Para habilitar la contabilización y las actividades de los pedidos en [!INCLUDE[crm_md](includes/crm_md.md)], consulte [Configurar el control de notas para obtener acceso a la información sobre publicaciones para una entidad personalizada](/dynamics365/customerengagement/on-premises/customize/notes-control-legacy) en la documentación de Customer Engagement. El artículo se refiere a Customer Engagement local, pero los pasos son los mismos para la versión en línea. <!--The /dynamics365/sales-enterprise/developer/introduction-activity-feeds link was broken. Should this actually point to /dynamics365/sales-enterprise/manage-activities-->

> [!NOTE]  
> La sincronización periódica basada en la asignación de tablas de integración **PEDIDO DE VENTAS-PEDIDO** solo funcionará cuando la integración de pedidos de venta esté activada. Para más información, vea [Configuración de la conexión en la página Configuración de la conexión de Sales](admin-prepare-dynamics-365-for-sales-for-integration.md). Solo se sincronizan los pedidos de venta creados a partir de los pedidos de venta enviados en [!INCLUDE[crm_md](includes/crm_md.md)]. Para obtener más información, consulte [Activar la integración de procesamiento de pedidos de venta](/dynamics365/sales-enterprise/developer/enable-sales-order-processing-integration).

> [!VIDEO https://go.microsoft.com/fwlink/?linkid=2098170]

## <a name="handling-sales-quotes-data"></a>Manejar datos de ofertas de venta
Las ofertas de venta que se activan en [!INCLUDE[crm_md](includes/crm_md.md)] se transferirán a [!INCLUDE[prod_short](includes/prod_short.md)] si selecciona la casilla **Procesar automáticamente ofertas** en la página **Configuración de conexión de Microsoft Dynamics 365**.
Como alternativa, puede convertir manualmente las ofertas de venta activadas desde [!INCLUDE[crm_md](includes/crm_md.md)] utilizando la acción **Procesar en [!INCLUDE[prod_short](includes/prod_short.md)]** en la página **Ofertas de venta - Dynamics 365 Sales**.
En dichas ofertas de venta, el campo **Nombre** de la oferta original se transfiere y se asigna al campo **Número de documento externo** del pedido de venta en [!INCLUDE[prod_short](includes/prod_short.md)]. También se transfiere el campo **En vigor hasta** de la oferta y se asigna al campo **Oferta válida hasta** en la oferta de venta en [!INCLUDE[prod_short](includes/prod_short.md)].  

Las ofertas de venta pasan por muchas revisiones mientras se están finalizando. El procesamiento manual y automático de las ofertas de venta en [!INCLUDE[prod_short](includes/prod_short.md)] garantiza que las versiones anteriores de las ofertas de venta se archiven antes de procesar nuevas revisiones de ofertas de venta desde [!INCLUDE[crm_md](includes/crm_md.md)].

Cuando elige **Proceso** en [!INCLUDE[prod_short](includes/prod_short.md)] para una oferta que está en estado **Ganada**, se crea un pedido de ventas en [!INCLUDE[prod_short](includes/prod_short.md)] solo si se envía un pedido de venta correspondiente en [!INCLUDE[crm_md](includes/crm_md.md)]. De lo contrario, la oferta solo se publica en [!INCLUDE[prod_short](includes/prod_short.md)]. Si se envía un pedido de venta en [!INCLUDE[crm_md](includes/crm_md.md)] más tarde y se crea un pedido de venta a partir de ahí, el **N.º de oferta** se actualiza en el pedido de venta y se archiva la oferta.

## <a name="handling-posted-sales-invoices-customer-payments-and-statistics"></a>Gestión de histórico de facturas de venta, pagos de cliente y estadísticas
Después de completar un pedido de venta, se crearán las facturas correspondientes. Cuando factura un pedido de venta, puede transferir el histórico de facturas de venta a [!INCLUDE[crm_md](includes/crm_md.md)] si selecciona la casilla **Crear factura en [!INCLUDE[crm_md](includes/crm_md.md)]** en la página **Histórico facturas venta**. Las facturas registradas se transfieren a [!INCLUDE[crm_md](includes/crm_md.md)] con el estado **Facturado**.

Cuando se recibe el pago del cliente para la factura de venta en [!INCLUDE[prod_short](includes/prod_short.md)], el estado de la factura de venta cambiará a **Pagado** con el campo **Motivo de estado** establecido en **Parcial**, si se ha pagado parcialmente, o **Completo**, si se ha pagado completamente, cuando elija la acción **Actualizar estadísticas de cuentas** en la página del cliente en [!INCLUDE[prod_short](includes/prod_short.md)]. La función **Actualizar estadísticas de cuentas** también actualizará valores como los campos **Saldo** y **Total ventas** en el cuadro informativo **Estadísticas de cuentas de [!INCLUDE[prod_short](includes/prod_short.md)]** en [!INCLUDE[crm_md](includes/crm_md.md)]. Alternativamente, puede hacer que los trabajos programados, Estadísticas de clientes y POSTEDSALESINV-INV, ejecuten automáticamente estos dos procesos en segundo plano. 

## <a name="handling-sales-prices"></a>Manejo de precios de venta
> [!NOTE]
> En el segundo lanzamiento de versiones de 2020, lanzamos procesos optimizados para configurar y administrar precios y descuentos. Si es un cliente nuevo que usa esa versión, está usando la nueva experiencia. Si es un cliente existente, si está utilizando o no la nueva experiencia depende de si su administrador ha habilitado la actualización de funciones **Nueva experiencia de precios de venta** en **Administración de características**. Para más información, consulte [Habilitación de las próximas funciones antes de tiempo](/dynamics365/business-central/dev-itpro/administration/feature-management).

Los pasos para completar este proceso difieren, dependiendo de si su administrador ha activado la nueva experiencia de precios. 

> [!NOTE]
> Si la sincronización de precios estándar no funciona para usted, le recomendamos que utilice las capacidades de personalización de integración. Para obtener más información, vea [Peronalización de una integración con Microsoft Dataverse](/dynamics365/business-central/dev-itpro/administration/administration-custom-cds-integration).

#### [Experiencia actual](#tab/current-experience/)
En la experiencia de precios actual, [!INCLUDE[prod_short](includes/prod_short.md)] sincroniza los precios de venta que: 

* Se aplican a todos los clientes. Las listas de precios de venta predeterminadas se crean en función del campo **Precio unitario** en la página **Tarjeta de artículo** de los artículos.
* Aplique a un grupo de precio de cliente específico. Por ejemplo, precios de venta para sus clientes minoristas o mayoristas. Para sincronizar precios basados en un grupo de precios de cliente, haga lo siguiente:

    1. Acople los artículos para los que el grupo de precios del cliente establece los precios.
    2. En la página **Grupos de precios para clientes**, combine el grupo de precios de clientes seleccionando **Relacionados**, luego **Dynamics 365 Sales**, **Emparejamiento** y finalmente **Configurar emparejamiento**. El emparejamiento creará una lista de precios activa en [!INCLUDE[prod_short](includes/prod_short.md)] con el mismo nombre que el grupo de precios del cliente en [!INCLUDE[crm_md](includes/crm_md.md)] y sincronizará automáticamente todos los artículos para los que el grupo de precios del cliente define el precio.

:::image type="content" source="media/customer-price-group.png" alt-text="Página de grupo de precios de clientes.":::

#### [Nueva experiencia](#tab/new-experience/)  

La nueva experiencia de precios sincroniza las listas de precios que cumplen con los siguientes criterios:

* **Permitir actualizar valores predeterminados** está desactivado.
* El tipo de precio es Venta.
* El tipo de importe es Precio.
* El tipo de producto en las líneas debe ser Artículo o Recurso. 
* No se especifica una cantidad mínima.

[!INCLUDE[prod_short](includes/prod_short.md)] sincroniza los precios de venta que se aplican a todos los clientes. Las listas de precios de venta predeterminadas se crean en función del campo **Precio unitario** en la página **Tarjeta de artículo** de los artículos.

Para sincronizar listas de precios, en la página **Lista de precios de venta**, elija **Relacionados**, **Dynamics 365 Sales**, **Emparejamiento** y luego **Configurar acoplamiento**. 

:::image type="content" source="media/sales-price-list.png" alt-text="Página de lista de precios de venta.":::

---


## <a name="see-also"></a>Consulte también
[Integración con Dynamics 365 Sales](admin-prepare-dynamics-365-for-sales-for-integration.md)  
[Gestión de relaciones](marketing-relationship-management.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Cambiar las funciones que se muestran](ui-experiences.md)  
[Asignar permisos a usuarios y grupos](ui-define-granular-permissions.md)    
[Descripción general de Sales y Centro de ventas](/dynamics365/customer-engagement/sales-enterprise/overview)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  


[!INCLUDE[footer-include](includes/footer-banner.md)]
