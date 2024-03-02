---
title: Integración con Dynamics 365 Sales
description: Obtenga información sobre cómo preparar Dynamics 365 Business Central para integrarse con Dynamics 365 Sales.
author: brentholtorf
ms.topic: conceptual
ms.search.keywords: 'sales, crm, integration, integrating'
ms.date: 12/15/2023
ms.author: bholtorf
ms.custom: bap-template
ms.service: dynamics-365-business-central
---
# <a name="integrating-with-dynamics-365-sales"></a>Integración con Dynamics 365 Sales

[!INCLUDE[azure-ad-to-microsoft-entra-id](~/../shared-content/shared/azure-ad-to-microsoft-entra-id.md)]

El papel de vendedor se considera a menudo uno de los trabajos más orientados hacia el exterior en una empresa. Sin embargo, puede ser útil para los vendedores poder mirar hacia adentro en la empresa y ver lo que está sucediendo en la trastienda. Al integrar [!INCLUDE[prod_short](includes/prod_short.md)] y [!INCLUDE[crm_md](includes/crm_md.md)], puede darle a su personal de ventas esa perspectiva. La integración permitirá que la gente vea la información en [!INCLUDE[prod_short](includes/prod_short.md)] mientras trabajan en [!INCLUDE[crm_md](includes/crm_md.md)]. Por ejemplo, al preparar una oferta de ventas podría ser útil saber si tiene suficiente inventario para cumplir el pedido. Para obtener más información, consulte [Usar Dynamics 365 Sales desde Business Central](marketing-integrate-dynamicscrm.md).

> [!NOTE]
> Este tema describe el proceso de integración de las versiones en línea de [!INCLUDE[crm_md](includes/crm_md.md)] y [!INCLUDE[prod_short](includes/prod_short.md)] a través de [!INCLUDE[prod_short](includes/cds_long_md.md)]. Para obtener información sobre la configuración local, consulte [Preparación de Dynamics 365 Sales para la integración local](/dynamics365/business-central/dev-itpro/administration/prepare-dynamics-365-for-sales-for-integration).

## <a name="integrate-through-dataverse"></a>Integración a través de Dataverse

Para facilitar la conexión y sincronización de datos con otras aplicaciones de Dynamics 365, [!INCLUDE[prod_short](includes/prod_short.md)] también se integra con [!INCLUDE[prod_short](includes/cds_long_md.md)]. Por ejemplo, puede conectarse a [!INCLUDE[crm_md](includes/crm_md.md)] o a aplicaciones que crea usted mismo. Si está integrando por primera vez, debe hacerlo a través de [!INCLUDE[prod_short](includes/cds_long_md.md)]. Para obtener más información, vea [Integración con Dataverse](admin-common-data-service.md).

Si ya ha integrado [!INCLUDE[crm_md](includes/crm_md.md)] con [!INCLUDE[prod_short](includes/prod_short.md)], puede continuar sincronizando datos utilizando su configuración. Sin embargo, si actualiza o desactiva la integración de [!INCLUDE[crm_md](includes/crm_md.md)], para activarla de nuevo debe conectarse a través de [!INCLUDE[prod_short](includes/cds_long_md.md)]. Para obtener más información, vea [Actualización de una integración con Dynamics 365 Sales](admin-upgrade-sales-to-cds.md).

> [!NOTE]
> La reconexión a través de [!INCLUDE[prod_short](includes/cds_long_md.md)] aplicará la configuración de sincronización predeterminada y sobrescribirá cualquier configuración que tenga. Por ejemplo, se aplicarán las asignaciones de tabla predeterminadas.

## <a name="integration-settings-that-are-specific-to-a--integration"></a>Configuración de integración específica de una integración de [!INCLUDE[crm_md](includes/crm_md.md)]

La integración con [!INCLUDE[prod_short](includes/prod_short.md)] sucede a través de [!INCLUDE[prod_short](includes/cds_long_md.md)] y hay muchas configuraciones y tablas estándar. Además de la configuración estándar, hay algunas que son específicas de [!INCLUDE[crm_md](includes/crm_md.md)]. Esa configuración se enumera en las siguientes secciones.

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
4. Opcionalmente, hay configuraciones avanzadas que pueden mejorar la seguridad y habilitar más capacidades. La siguiente tabla describe las configuraciones avanzadas.  

| Campo | Descripción |
|--|--|
| **Importar la solución de Dynamics 365 Sales** | Instale y configure la solución de integración en [!INCLUDE[crm_md](includes/crm_md.md)]. <!--For more information, see [About the Base CDS Integration Solution](admin-common-data-service.md#about-the-business-central-integration-solution). Need to add a new topic--> |
|**Sincronizar automáticamente la disponibilidad de productos**|Especifica que se programará la cola de proyecto de disponibilidad de producto. La cola de proyecto se ejecuta cada 30 minutos y actualiza la disponibilidad de los productos emparejados.|
| **Habilitar integración de pedido de venta** | Cuando los usuarios crean pedidos de venta en [!INCLUDE[crm_md](includes/crm_md.md)] y completan pedidos [!INCLUDE[prod_short](includes/prod_short.md)], esta configuración integra el proceso en [!INCLUDE[crm_md](includes/crm_md.md)]. Para obtener más información, consulte [Activar la integración de procesamiento de pedidos de venta](/dynamics365/customer-engagement/sales-enterprise/developer/enable-sales-order-processing-integration).<br><br>**Nota:** No puede usar esta opción si usa la opción **Sincronización bidireccional de pedidos de ventas**. Las dos opciones se excluyen mutuamente. Para obtener más información sobre esta opción, vaya a [Sincronización única y bidireccional de pedidos de ventas](#single-and-bi-directional-synchronization-of-sales-orders). |
|**Habilitar la conexión de Dynamics 365 Sales** | Habilitar la conexión a [!INCLUDE[crm_md](includes/crm_md.md)]. |
| **Versión de Dynamics 365 SDK** | Solo es relevante si va a realizar la integración con una versión local de [!INCLUDE[crm_md](includes/crm_md.md)]. Este SDK es el kit de desarrollo de software de Dynamics 365 (también designado Xrm) que se utiliza para conectar [!INCLUDE[prod_short](includes/prod_short.md)] a [!INCLUDE[crm_md](includes/crm_md.md)]. La versión debe ser compatible con la versión de SDK que utiliza [!INCLUDE[crm_md](includes/crm_md.md)] e igual o más nueva que la versión que utiliza [!INCLUDE[crm_md](includes/crm_md.md)]. |
|**Sincronización bidireccional de pedidos de venta**|Sincronice pedidos de venta en ambas direcciones. Para obtener más información sobre esta opción, vaya a [Sincronización única y bidireccional de pedidos de ventas](#single-and-bi-directional-synchronization-of-sales-orders).<br><br>**Nota:** No puede usar esta opción si usa la opción **Habilitar integración de pedido de venta**. Las dos opciones se excluyen mutuamente.|

### <a name="connection-settings-on-the-microsoft-dynamics-365-connection-setup-page"></a>Configuración de conexión en la página de configuración de conexión de Microsoft Dynamics 365

Escriba la siguiente información para la conexión de [!INCLUDE[crm_md](includes/crm_md.md)] a [!INCLUDE[prod_short](includes/prod_short.md)].

| Campo | Descripción |
|--|--|
|**URL de Dynamics 365 Sales**|La URL de su instancia de [!INCLUDE[crm_md](includes/crm_md.md)]. Esta configuración permite a los usuarios abrir los registros en [!INCLUDE[prod_short](includes/prod_short.md)] que se corresponden con registros en [!INCLUDE[crm_md](includes/crm_md.md)]. Por ejemplo, una cuenta o producto. Los registros de [!INCLUDE[prod_short](includes/prod_short.md)] abiertos en [!INCLUDE[prod_short](includes/prod_short.md)].|
|**Sincronizar automáticamente la disponibilidad de productos**|Especifica que se programará la cola de proyecto de disponibilidad de producto. La cola de proyecto se ejecuta cada 30 minutos y actualiza la disponibilidad de los productos emparejados.|
|**Versión de Dynamics 365 SDK**|Si está realizando la integración con una versión local de [!INCLUDE[crm_md](includes/crm_md.md)], este es el kit de desarrollo de software de Microsoft Dynamics 365 (también designado Xrm) que utiliza para conectar [!INCLUDE[prod_short](includes/prod_short.md)] a [!INCLUDE[crm_md](includes/crm_md.md)]. La versión que seleccione debe ser compatible con la versión de SDK que utiliza [!INCLUDE[crm_md](includes/crm_md.md)]. Esta versión es igual o más reciente que la versión que utiliza [!INCLUDE[crm_md](includes/crm_md.md)].|

Además de las configuraciones anteriores, introduzca las siguientes configuraciones para [!INCLUDE[crm_md](includes/crm_md.md)].

| Campo | Descripción |
|--|--|
| **La integración de pedidos de venta está habilitada** | Permitir que los usuarios envíen pedidos de venta y ofertas activadas en [!INCLUDE[crm_md](includes/crm_md.md)] y después verlas y procesarlas en [!INCLUDE[prod_short](includes/prod_short.md)]. Esta configuración integra el proceso en [!INCLUDE[crm_md](includes/crm_md.md)]. Para obtener más información, consulte [Activar la integración de procesamiento de pedidos de venta](/dynamics365/customer-engagement/sales-enterprise/developer/enable-sales-order-processing-integration). |
| **Crear automáticamente pedidos de ventas** | Crear un pedido de venta en [!INCLUDE[prod_short](includes/prod_short.md)] cuando un usuario cree y envíe uno en [!INCLUDE[crm_md](includes/crm_md.md)]. |
| **Procesar automáticamente ofertas de venta** | Procesar una oferta de venta cuando en [!INCLUDE[prod_short](includes/prod_short.md)] cuando un usuario cree y active una en [!INCLUDE[crm_md](includes/crm_md.md)]. Para obtener más información, consulte [Gestión de datos de ofertas de ventas](/dynamics365/business-central/marketing-integrate-dynamicscrm?tabs=new-experience#handling-sales-quotes-data). |
|**Sincronización bidireccional de pedidos de venta**|Sincronice pedidos de venta en ambas direcciones. Para obtener más información sobre esta opción, vaya a [Sincronización única y bidireccional de pedidos de ventas](#single-and-bi-directional-synchronization-of-sales-orders).|
<!--
### <a name="user-account-settings"></a>User Account Settings
Integration with Business Central through Dataverse requires an administrator user account and an account that is used only for the connection between the apps. This account is called the "integration user." When you install the CDS Base Integration Solution, permissions for the integration user account are configured in [!INCLUDE[crm_md](includes/crm_md.md)]. If those permissions are changed you might need to reset them. You can do that by reinstalling the Integration Solution or by manually resetting them. The following tables list the minimum permissions for the user accounts in [!INCLUDE[crm_md](includes/crm_md.md)].  -->
### <a name="single-and-bi-directional-synchronization-of-sales-orders"></a>La sincronización única y bidireccional de pedidos de venta

Cuando configura su integración, ya sea en la guía de configuración o en la página de configuración de conexión de Microsoft Dynamics 365, hay opciones que controlan la dirección en la que sincroniza los pedidos de ventas y cómo los envía.

La opción **Sincronización bidireccional de pedidos de venta** le permite sincronizar pedidos de venta desde Sales a [!INCLUDE [prod_short](includes/prod_short.md)] y viceversa. Por ejemplo, si un cliente cambia de opinión sobre el producto o la cantidad que pidió en [!INCLUDE[crm_md](includes/crm_md.md)], puede archivar el documento de ventas y crear uno nuevo en [!INCLUDE[prod_short](includes/prod_short.md)]. Lo mismo se aplica a los cambios en [!INCLUDE[prod_short](includes/prod_short.md)]. Por ejemplo, cuando cambian los precios, los importes de impuestos o las fechas de envío previstas, los cambios se sincronizan para [!INCLUDE[crm_md](includes/crm_md.md)]. La sincronización bidireccional le ayuda a mantener a sus vendedores al día de los últimos cambios y el estado de los pedidos de venta.

Para la sincronización bidireccional, los pedidos de venta están disponibles para sincronización cuando cambia su estado a **Enviado** en Sales. Cuando establece ese estado, ya no puede cambiar la información en las líneas del pedido. Cuando sincroniza, el pedido se transfiere a [!INCLUDE [prod_short](includes/prod_short.md)] con el estado **Liberado**. Si hay un error, puede revertir el orden a **Abierto** (en [!INCLUDE [prod_short](includes/prod_short.md)]) o **Activo** (en Sales) y luego agregar o eliminar líneas para corregir el error y enviar el pedido nuevamente.

> [!TIP]
> Cuando habilita la opción **Sincronización bidireccional de pedidos de venta**, [!INCLUDE [prod_short](includes/prod_short.md)] crea un registro en la página **Archivos de pedidos de venta** cuando publica o cambia información en un pedido. Por ejemplo, las versiones archivadas pueden resultar útiles para explorar el historial de un pedido.

La opción **Habilitar integración de pedido de venta** se sincroniza sola desde Sales a [!INCLUDE [prod_short](includes/prod_short.md)]. Para esta opción, utilice la acción **Enviar** en Sales para que los pedidos estén disponibles para sincronización. Cuando lo haga, ya no puede cambiar la información en las líneas del pedido. Cuando sincroniza, el pedido se transfiere a [!INCLUDE [prod_short](includes/prod_short.md)] con el estado **Liberado**.

Para usar esta opción, debe proporcionar las credenciales de una cuenta de usuario de administrador en [!INCLUDE[crm_md](includes/crm_md.md)]. Para obtener más información, consulte [Manejo de datos de pedidos de ventas especiales](marketing-integrate-dynamicscrm.md#handling-sales-order-data).

> [!NOTE]
> Las opciones **Sincronización bidireccional de pedido de venta** y **Habilitar integración de pedido de venta** son mutuamente excluyentes. No puede usar ambas opciones al mismo tiempo.

Para ambas opciones, [!INCLUDE [prod_short](includes/prod_short.md)] muestra todos los pedidos de venta con el estado **Enviado** en la página **Pedidos: Microsoft Dynamics 365 Sales**.

### <a name="standard-sales-entity-mapping-for-synchronization"></a>Asignación de entidad de Sales estándar para la sincronización

Las entidades en [!INCLUDE[crm_md](includes/crm_md.md)], como los pedidos, se integran con tipos equivalentes de tablas en [!INCLUDE[prod_short](includes/prod_short.md)], como los pedidos de venta. Para trabajar con datos de [!INCLUDE[crm_md](includes/crm_md.md)] se establecen vínculos, llamados emparejamientos, entre tablas en [!INCLUDE[prod_short](includes/prod_short.md)] y [!INCLUDE[crm_md](includes/crm_md.md)].

La siguiente tabla enumera la asignación estándar entre tablas en [!INCLUDE[prod_short](includes/prod_short.md)] y [!INCLUDE[crm_md](includes/crm_md.md)] que proporciona [!INCLUDE[prod_short](includes/prod_short.md)].

| [!INCLUDE[prod_short](includes/prod_short.md)] | [!INCLUDE[crm_md](includes/crm_md.md)] | Dirección de la sincronización | Filtro predeterminado |
|--|--|--|--|
| Unidad de medida | Grupo de unidad | [!INCLUDE[prod_short](includes/prod_short.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] |  |
| Producto | Producto | [!INCLUDE[prod_short](includes/prod_short.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] y [!INCLUDE[crm_md](includes/crm_md.md)] -> [!INCLUDE[prod_short](includes/prod_short.md)] | Filtro de contacto de Sales: **Tipo de producto** es **Inventario de ventas** |
| Recurso | Producto | [!INCLUDE[prod_short](includes/prod_short.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] y [!INCLUDE[crm_md](includes/crm_md.md)] -> [!INCLUDE[prod_short](includes/prod_short.md)] | Filtro de contacto de Sales: **Tipo de producto** es **Services** |
| Unidad medida producto | CRM UOM |[!INCLUDE[prod_short](includes/prod_short.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)]| |
| Unidad medida recurso | CRM UOM |[!INCLUDE[prod_short](includes/prod_short.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)]||
| Grupo de unidad | CRM Uomschedule | [!INCLUDE[prod_short](includes/prod_short.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] ||
| Grupo precio cliente | Lista de precios | [!INCLUDE[prod_short](includes/prod_short.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] |  |
| Precio venta | Lista de precios de productos | [!INCLUDE[prod_short](includes/prod_short.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] | Filtro de contacto de [!INCLUDE[prod_short](includes/prod_short.md)]: **Código ventas** no está en blanco, **Tipo de ventas** es **Grupo precio cliente** |
| Crear oportunidad | Crear oportunidad | [!INCLUDE[prod_short](includes/prod_short.md)] -> [!INCLUDE[prod_short](includes/cds_long_md.md)] y [!INCLUDE[crm_md](includes/crm_md.md)] -> [!INCLUDE[prod_short](includes/prod_short.md)] |  |
| Histórico cab. factura venta | Facturar | [!INCLUDE[prod_short](includes/prod_short.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] |  |
| Histórico lín. factura venta | Producto de facturación | [!INCLUDE[prod_short](includes/prod_short.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] |  |
| Cabecera de pedido de cliente | Pedido venta | [!INCLUDE[prod_short](includes/prod_short.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] y [!INCLUDE[crm_md](includes/crm_md.md)] -> [!INCLUDE[prod_short](includes/prod_short.md)] <br><br> Para sincronizar en ambas direcciones, debe activar el botón de alternancia **Sincronización bidireccional de pedidos de venta** en la página **Configuración de la conexión de Dynamics 365**.| Filtro de cabecera de venta de [!INCLUDE[prod_short](includes/prod_short.md)]: **Tipo de documento** es Pedido, **Estado** es Lanzado |
| Notas de pedido de ventas | Notas de pedido de ventas | [!INCLUDE[prod_short](includes/prod_short.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] y [!INCLUDE[crm_md](includes/crm_md.md)] -> [!INCLUDE[prod_short](includes/prod_short.md)] |  |

> [!NOTE]
> Las asignaciones para las tablas Unidad de medida de artículo, Unidad de medida de recurso y Grupo de unidades están disponibles solo si su administrador ha activado la opción **Asignación de grupo de unidades** en la página **Configuración de la conexión de Microsoft Dynamics 365**. Para obtener más información, vaya a [Sincronización de artículos y recursos con productos en diferentes unidades de medida](admin-prepare-dynamics-365-for-sales-for-integration.md#synchronize-items-and-resources-with-products-with-different-units-of-measure).

## <a name="synchronize-items-and-resources-with-products-with-different-units-of-measure"></a>Sincfronizar artículos y recursos con productos con diferentes unidades de medida

Las empresas a menudo producen o compran los artículos en una unidad de medida y luego los venden en otra. Para sincronizar elementos que utilizan varias unidades de medida, debe activar la opción **Asignación de grupo de unidades** en la página **Configuración de la conexión de Microsoft Dynamics 365**. 

Cuando activa la actualización de funciones, se crea una nueva tabla de grupo de unidades y se asigna a cada elemento y recurso en [!INCLUDE[prod_short](includes/prod_short.md)]. Las tablas le permiten asignar las tablas Grupo de unidad, Unidad de medida de artículo y Unidad de medida de recurso en [!INCLUDE[prod_short](includes/prod_short.md)] al Grupo de Unidades de Dynamics 365 Sales en [!INCLUDE[crm_md](includes/crm_md.md)]. La siguiente imagen muestra las asignaciones.

:::image type="content" source="media/unit group 1.png" alt-text="Asignaciones de tablas para grupos de unidades":::

Puede crear varias unidades de medida para cada grupo de unidades y asignar los grupos a productos en [!INCLUDE[crm_md](includes/crm_md.md)]. Posteriormente, podrá sincronizar los productos con elementos y recursos en [!INCLUDE[prod_short](includes/prod_short.md)]. Puede acoplar manualmente unidades de medida de artículos o unidades de medida de recursos con un grupo de unidades. Cuando lo haga, si el grupo de unidades para el elemento o recurso no está emparejado con un grupo de unidades en [!INCLUDE[crm_md](includes/crm_md.md)], por ejemplo, porque el grupo unitario no existía, [!INCLUDE[prod_short](includes/prod_short.md)] creará automáticamente el grupo de unidades en [!INCLUDE[crm_md](includes/crm_md.md)].

### <a name="map-items-and-resources-to-products"></a>Asignar elementos y recursos a productos

Cuando activa la opción **Asignación de grupo de unidades** en la página **Configuración de la conexión de Microsoft Dynamics 365**, sucede lo siguiente:

* Se crean nuevas asignaciones para elementos y recursos.
* Se eliminan las asignaciones existentes. <!--which mappings?-->
* Una actualización de datos crea grupos de unidades para artículos y recursos.

Para utilizar las nuevas asignaciones, debe sincronizar los grupos de unidades, la unidad de medida del artículo y la unidad de medida del recurso. También debe resincronizar elementos y recursos. 

> [!NOTE]
> [!INCLUDE[crm_md](includes/crm_md.md)] no le permite cambiar un grupo de unidades para un producto. Por lo tanto, debe retirar sus productos y desacoplar los elementos y recursos y luego sincronizar creando nuevos productos en [!INCLUDE[crm_md](includes/crm_md.md)]. 

Los siguientes pasos describen los pasos para comenzar a asignar grupos de unidades:

1. Asegúrese de que los productos en [!INCLUDE[crm_md](includes/crm_md.md)] no se combinan con elementos o recursos en [!INCLUDE[prod_short](includes/prod_short.md)]. Si lo son, vaya a las páginas **Elementos** y / o **Recursos** y use las opciones de filtro para seleccionar los registros acoplados. Después elija la acción **Dynamics 365 Sales**, y luego elija **Desacoplar**. Esta acción programa un trabajo en segundo plano para desemparejar los registros. Mientras se ejecuta el trabajo, puede comprobar su estado mediante la acción **Registro de sincronización**. Para obtener más información, consulte [Emparejamiento y sincronización](admin-how-to-couple-and-synchronize-records-manually.md). 
2. Debido a que se crearán nuevos productos en [!INCLUDE[crm_md](includes/crm_md.md)] con nuevos grupos de unidades, para evitar nombres duplicados, realice una de las siguientes acciones:
    
  * Cambie el nombre de sus productos y luego retírelos en [!INCLUDE[crm_md](includes/crm_md.md)]. Para más información, ver [Retirar productos (Centro de ventas)](/dynamics365/sales-enterprise/retire-product). Para editar de forma masiva sus productos en Microsoft Excel, iniciar sesión en Power Apps, elija su entorno, vaya a la tabla **Producto** tabla y después elija la pestaña **Datos**. Borre los filtros que se apliquen. En el grupo **Datos** grupo, elija la acción **Editar datos en Excel**. Agregue un prefijo o sufijo a los productos acoplados y luego retírelos.
    * Retire sus productos y elimínelos. 

3. Siga estos pasos para sincronizar **Grupos de unidades**, **Unidad de medidas**, **Elementos** y **Recursos**:
    1. En [!INCLUDE[prod_short](includes/prod_short.md)], abra la página **Configuración de conexión de Dynamics 365 Sales**.
    2. Use la acción **Ejecutar sincronización completa** para abrir la página **Revisión de sincronización completa de Dataverse**.
    3. Para las asignaciones **ARTÍCULO UOM**, **UOM DE RECURSOS**, Y **GRUPO DE UNIDAD**, elija la acción **Recomendar sincronización completa**.
    4. Seleccione la acción **Sincronizar todo**.

    > [!NOTE]
    > Para las asignaciones que aún no se han sincronizado por completo, esta acción las sincronizará por completo. Para evitar que esas asignaciones se sincronicen, elimine las asignaciones de la página. Esto solo los elimina de la sincronización completa actual y no elimina las asignaciones.
    
5. Elija la asignación **ARTÍCULO-PRODUCTO** y luego elija la acción **Reiniciar**. El reinicio crea nuevos productos a partir de los elementos en [!INCLUDE[crm_md](includes/crm_md.md)] y asigna un nuevo grupo de unidades específico para el producto.
6. Elija la asignación **RECURSO-PRODUCTO** y luego elija la acción **Reiniciar**. El reinicio crea nuevos productos a partir de los recursos en [!INCLUDE[crm_md](includes/crm_md.md)] y asigna un nuevo grupo de unidades específico para los recursos.

### <a name="synchronization-rules"></a>Reglas de sincronización

En la tabla siguiente se enumeran las reglas que controlan la sincronización entre [!INCLUDE[crm_md](includes/crm_md.md)] y [!INCLUDE[prod_short](includes/prod_short.md)]. Estas reglas son adicionales a las reglas definidas para Dataverse, que también se aplican. Para obtener más información, consulte [Asignación de entidades estándar](admin-synchronizing-business-central-and-sales.md#standard-table-mapping-for-synchronization).

> [!NOTE]  
> Los cambios en los datos realizados por la cuenta de usuario de integración no se sincronizan. Por lo tanto, le recomendamos que no modifique los datos mientras utiliza esa cuenta. Para obtener más información, consulte [Configuración de cuentas de usuario para la integración con Dynamics 365 Sales](admin-setting-up-integration-with-dynamics-sales.md).

|Escritorio|Regla|
|-----|----|
|Unidades medida|Las unidades de medida se sincronizan con grupos de unidades en [!INCLUDE[crm_md](includes/crm_md.md)]. Solo puede haber una unidad de medida definida en la unidad de venta.|
|Productos|Al sincronizar artículos con los productos de [!INCLUDE[crm_md](includes/crm_md.md)], [!INCLUDE[prod_short](includes/prod_short.md)] crea automáticamente una lista de precios en [!INCLUDE[crm_md](includes/crm_md.md)]. Para evitar errores de sincronización, no debe modificar la lista de precios manualmente.|
|Recursos|Los recursos se sincronizan con los productos de [!INCLUDE[crm_md](includes/crm_md.md)] que tienen el tipo de producto Servicio.|
|Grupos precio cliente|Los grupos de precios de cliente se sincronizan con las listas de precios de Sales.|
|Precios ventas|Los precios de Sales que tienen el tipo de venta Grupo precio cliente y tengan un código de venta definido se sincronizan con las líneas de lista de precios de [!INCLUDE[crm_md](includes/crm_md.md)].|
|Oportunidades|Las oportunidades se sincronizan con las oportunidades de [!INCLUDE[crm_md](includes/crm_md.md)]. El valor de Código de vendedor define el propietario de la tabla emparejada en [!INCLUDE[crm_md](includes/crm_md.md)].|
|Histórico facturas venta|Las facturas de ventas registradas se sincronizan con las facturas de ventas. Para poder sincronizar una factura, es mejor sincronizar las demás tablas que puedan participar en la factura, desde los vendedores hasta las listas de precios. El valor de Código de vendedor en la cabecera de la factura define el propietario de la tabla acoplada en Sales.|
|Pedidos de venta|Cuando se activa la integración de pedidos de venta, los pedidos de venta en [!INCLUDE[prod_short](includes/prod_short.md)] creados a partir de pedidos de venta enviados en [!INCLUDE[crm_md](includes/crm_md.md)] se sincronizan con los pedidos de venta en [!INCLUDE[crm_md](includes/crm_md.md)] cuando se liberan. Antes de sincronizar los pedidos, recomendamos que primero sincronice todas las tablas que intervienen en el pedido, como los vendedores y las listas de precios. El campo Código de vendedor en la cabecera del pedido define el propietario de la tabla emparejada en [!INCLUDE[crm_md](includes/crm_md.md)].|

### <a name="synchronization-jobs-for-a-sales-integration"></a>Trabajos de sincronización para una integración de ventas

Los trabajos se ejecutan en el siguiente orden para evitar dependencias de emparejamiento entre tablas. Hay más trabajos adicionales disponibles en Dataverse. Para obtener más información, consulte [Uso de colas de proyectos para programar tareas](./admin-job-queues-schedule-tasks.md).

1. Proyecto de sincronización de UNITOFMEASURE - Dynamics 365 Sales  
2. Proyecto de sincronización de RECURSO-PRODUCTO - Dynamics 365 Sales  
3. Proyecto de sincronización de ARTÍCULO-PRODUCTO - Dynamics 365 Sales  
4. Proyecto de sincronización de CUSTPRCGRP-PRICE - Dynamics 365 Sales.
5. Proyecto de sincronización de SALESPRC-PRODPRICE - Dynamics 365 Sales.
6. Proyecto de sincronización de POSTEDSALESINV-INV - Dynamics 365 Sales.

### <a name="default-synchronization-job-queue-entries"></a>Entradas de cola de proyectos de sincronización predeterminados

La tabla siguiente describe los proyectos de sincronización predeterminados para [!INCLUDE[crm_md](includes/crm_md.md)].  

|Mov. cola proyecto|Descripción|Dirección|Asignación de tablas de integración|Frecuencia de sincronización predeterminada (minutos)|Tiempo de reposo de inactividad predeterminado (minutos)|  
|---------------------|---------------------------------------|---------------|-------------------------------|-----|-----|  
|Proyecto de sincronización de UNITOFMEASURE - Dynamics 365 Sales|Sincroniza los grupos de unidad de [!INCLUDE[crm_md](includes/crm_md.md)] con las unidades de medida de [!INCLUDE[prod_short](includes/prod_short.md)].|De [!INCLUDE[prod_short](includes/prod_short.md)] a [!INCLUDE[crm_md](includes/crm_md.md)]|UNIDAD DE MEDIDA|30|720<br> (12 h)|
|Proyecto de sincronización de RECURSO-PRODUCTO - Dynamics 365 Sales|Sincroniza los productos de [!INCLUDE[crm_md](includes/crm_md.md)] con los recursos de [!INCLUDE[prod_short](includes/prod_short.md)].|De [!INCLUDE[prod_short](includes/prod_short.md)] a [!INCLUDE[crm_md](includes/crm_md.md)]|RECURSO-PRODUCTO|30|720<br> (12 h)|
|Proyecto de sincronización de ARTÍCULO-PRODUCTO - Dynamics 365 Sales|Sincroniza los productos de [!INCLUDE[crm_md](includes/crm_md.md)] con los artículos de [!INCLUDE[prod_short](includes/prod_short.md)].|De [!INCLUDE[prod_short](includes/prod_short.md)] a [!INCLUDE[crm_md](includes/crm_md.md)]|ARTÍCULO-PRODUCTO|30|1440<br> (24 h)|
|Proyecto de sincronización de CUSTPRCGRP-PRICE - Dynamics 365 Sales|Sincroniza las listas de precios de venta de [!INCLUDE[crm_md](includes/crm_md.md)] con los grupos de precios de los clientes de [!INCLUDE[prod_short](includes/prod_short.md)].| |GRUPOS DE PRECIOS DE CLIENTES-LISTAS DE PRECIOS DE VENTA|30|1440<br> (24 h)|
|Proyecto de sincronización de SALESPRC-PRODUCTPRICE - Dynamics 365 Sales|Sincroniza los precios de producto de [!INCLUDE[crm_md](includes/crm_md.md)] con los precios de venta de [!INCLUDE[prod_short](includes/prod_short.md)].||PRECIO DEL PRODUCTO-PRECIO DE VENTA|30|1440<br> (24 h)|
|Proyecto de sincronización de POSTEDSALESINV-INV - Dynamics 365 Sales|Sincroniza las facturas de [!INCLUDE[crm_md](includes/crm_md.md)] con facturas de ventas registradas de [!INCLUDE[prod_short](includes/prod_short.md)].|De [!INCLUDE[prod_short](includes/prod_short.md)] a [!INCLUDE[crm_md](includes/crm_md.md)]|FACTURAS-FACTURAS DE VENTAS REGISTRADAS|30|1440<br> (24 h)|
|Sincronización de Estadísticas de clientes - Dynamics 365 Sales|Actualiza las cuentas de [!INCLUDE[crm_md](includes/crm_md.md)] con los últimos datos de los clientes de [!INCLUDE[prod_short](includes/prod_short.md)]. En [!INCLUDE[crm_md](includes/crm_md.md)], la información se muestra en el formulario de vista rápida **Estadísticas de la cuenta de Business Central** de cuentas que están emparejadas con los clientes de [!INCLUDE[prod_short](includes/prod_short.md)].<br /><br /> Estos datos también pueden actualizarse manualmente desde cada registro de cliente. Para obtener más información, consulte [Emparejar y sincronizar registros manualmente](admin-how-to-couple-and-synchronize-records-manually.md). </BR></BR>**Nota:** este movimiento de la cola de proyectos es relevante solo si la solución de integración de [!INCLUDE[prod_short](includes/prod_short.md)] está instalada en [!INCLUDE[crm_md](includes/crm_md.md)]. |No aplicable|No aplicable|30|No aplicable| 

## <a name="connect-to-on-premises-versions-of-business-central-2019-release-wave-1-and-microsoft-dynamics-nav-2018"></a>Conectar con las versiones locales de Business Central 2019, lanzamientos de versiones 1 y Microsoft Dynamics NAV 2018

El equipo de Microsoft Power Platform ha [anunciado](/power-platform/important-changes-coming#deprecation-of-office365-authentication-type-and-organizationserviceproxy-class-for-connecting-to-dataverse) que está desaprobando el tipo de autenticación de Office365. Si esta usando una versión de [!INCLUDE[prod_short](includes/prod_short.md)] local anterior a Business Central 2019, lanzamiento de versiones 1, debe usar el tipo de autenticación OAuth para conectarse a [!INCLUDE[crm_md](includes/crm_md.md)] online. Los pasos de esta sección describen cómo conectar las siguientes versiones del producto:

* Business Central 2019 lanzamiento de versiones 1
* Microsoft Dynamics NAV 2018

### <a name="prerequisites"></a>Requisitos previos

* Debe tener una suscripción a Microsoft Azure. Una cuenta de prueba funcionará para el registro de la aplicación.
* [!INCLUDE[crm_md](includes/crm_md.md)] está configurado para usar uno de los siguientes tipos de autenticación:

   * Office365 (heredado)

     > [!IMPORTANT]
     > A partir de abril de 2022, Office365 (heredado) ya no será compatible. Para obtener más información, consulte [Próximos cambios importantes (ceses de uso) en Power Apps, Power Automate y aplicaciones de interacción con el cliente](/power-platform/important-changes-coming#deprecation-of-office365-authentication-type-and-organizationserviceproxy-class-for-connecting-to-dataverse).

   * OAuth

### <a name="connect-business-central-2019-release-wave-1-and-dynamics-nav-2018"></a>Conectar Business Central 2019, lanzamiento de versiones 1, y Dynamics NAV 2018

1. Importe la Solución de integración de Microsoft Dynamics 365 Business Central en su entorno de [!INCLUDE[crm_md](includes/crm_md.md)]. La solución de integración está disponible en la carpeta CrmCustomization del DVD de instalación de [!INCLUDE[prod_short](includes/prod_short.md)] o Dynamics NAV 2018. Dependiendo de la versión de su producto, importe una de las siguientes soluciones:

   * Para [!INCLUDE[prod_short](includes/prod_short.md)], la carpeta contiene las soluciones DynamicsNAVIntegrationSolution_v9 y DynamicsNAVIntegrationSolution_v91. . La solución que debe importar depende de la versión de [!INCLUDE[crm_md](includes/crm_md.md)] a la que se esté conectando. [!INCLUDE[crm_md](includes/crm_md.md)] online requiere la solución de integración DynamicsNAVIntegrationSolution_v91.
   * Para  Dynamics NAV 2018, instale la solución DynamicsNAVIntegrationSolution.

2. Cree un usuario de integración no interactivo en su entorno de [!INCLUDE[crm_md](includes/crm_md.md)] y asigne al usuario los siguientes roles de seguridad. Para obtener más información, consulte [Crear una cuenta de usuario no interactiva](/power-platform/admin/create-users-assign-online-security-roles#create-a-non-interactive-user-account).

   * Administrador de integración de Dynamics 365 Business Central
   * Usuario de integración de Dynamics 365 Business Central

   > [!Important]
   > Este usuario no debe tener la función de seguridad de administrador del sistema. Además, no puede utilizar la cuenta de administrador del sistema como usuario de integración.

3. En Azure Portal, cree un registro de aplicación para [!INCLUDE[prod_short](includes/prod_short.md)]. Para obtener más información, consulte [Registrar una aplicación en Microsoft Entra ID](/powerapps/developer/data-platform/walkthrough-register-app-azure-active-directory). 
  
   > [!NOTE]
   > Le recomendamos que registre la aplicación en el mismo inquilino que su entorno de Dataverse para que no tenga que dar su consentimiento para permitir que la aplicación acceda al entorno. Si registra la aplicación en otro entorno, debe iniciar sesión en Microsoft Entra ID usando la cuenta de administrador para su entorno de Dataverse y dar su consentimiento.
   >
   > Además, la aplicación que registre no debe tener un secreto. La conexión de una aplicación con un secreto con Dataverse solo está disponible en Business Central 2020 lanzamiento de versiones 1 y versiones posteriores.
  
4. Dependiendo de la versión de su producto, realice una de las siguientes operaciones:

    * En [!INCLUDE[prod_short](includes/prod_short.md)], busque **Configuración de la conexión de Microsoft Dynamics 365** y luego elija el enlace relacionado. 
    * En Dynamics NAV 2018, busque **Configuración de la conexión de Microsoft Dynamics 365 for Sales** y luego elija el enlace relacionado.

5. En el campo **Tipo de autenticación**, elija la opción para OAuth. 
6. Elija la versión de CRM SDK que coincida con la versión de la solución que importó en el paso 1.

   > [!NOTE]
   > Este paso solo es relevante para [!INCLUDE[prod_short](includes/prod_short.md)].

7. Escriba la dirección URL de su entorno de [!INCLUDE[crm_md](includes/crm_md.md)] y, a continuación, introduzca el nombre de usuario y la contraseña del usuario de integración. 

   * En [!INCLUDE[prod_short](includes/prod_short.md)], utilice el campo **Dirección del servidor**.
   * En Dynamics NAV 2018, use el campo **URL de Dynamics 365 Sales**.

8. En el campo **Cadena de conexión**, especifique el ID del registro de la aplicación. Este campo tiene dos tokens en los que se debe especificar el ID de su aplicación.

   |Token           |Descripción  |
   |----------------|-------------|
   |**AppId**       |Establecer en el ID de la aplicación.      |
   |**RedirectUri** |Establezca el ID de la aplicación, pero agregue el prefijo **app://**.         |

    **Ejemplo** El siguiente ejemplo muestra una cadena de conexión.

    ```
    AuthType=OAuth;Username=jsmith@contoso.onmicrosoft.com;Password=****;Url=https://contosotest.crm.dynamics.com;AppId=<your AppId>;RedirectUri=app://<your AppId>;TokenCacheStorePath=;LoginPrompt=Auto
    ```
9. Habilitar la conexión.

> [!Note]
> Si desea configurar una conexión a una instancia de [!INCLUDE[crm_md](includes/crm_md.md)] con un tipo de autenticación determinado, rellene los campos de la ficha desplegable **Detalles del tipo de autenticación**. Para obtener más información, consulte [Autenticación con servicios web de Microsoft Dataverse](/powerapps/developer/data-platform/authentication). Este paso no es necesario a conectar una versión en línea de [!INCLUDE[prod_short](includes/prod_short.md)].

## <a name="see-also"></a>Consulte también

[Configuración de cuentas de usuario para la integración con [!INCLUDE[crm_md](includes/crm_md.md)]](admin-setting-up-integration-with-dynamics-sales.md)  
[Configurar una conexión a [!INCLUDE[crm_md](includes/crm_md.md)]](admin-how-to-set-up-a-dynamics-crm-connection.md)  
[Sincronización de Business Central y [!INCLUDE[crm_md](includes/crm_md.md)]](admin-synchronizing-business-central-and-sales.md)  
[Preparación de Dynamics 365 Sales para la integración local](/dynamics365/business-central/dev-itpro/administration/prepare-dynamics-365-for-sales-for-integration)


[!INCLUDE[footer-include](includes/footer-banner.md)]
