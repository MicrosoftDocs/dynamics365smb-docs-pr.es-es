---
title: Sincronización e integración de datos | Documentos de Microsoft
description: La sincronización copia los datos entre los movimientos de Dynamics 365 for Sales y los registros de Business Central, y mantiene actualizados los datos de ambos sistemas.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: sales, crm, integration, sync, synchronize
ms.date: 04/01/2019
ms.author: bholtorf
ms.openlocfilehash: e52010384de83d95011cb29a88cad17a5eba817c
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 03/31/2019
ms.locfileid: "940332"
---
# <a name="synchronizing-data-in-business-central-and-dynamics-365-for-sales"></a>Sincronización de datos en Business Central y Dynamics 365 for Sales
Cuando integra [!INCLUDE[crm_md](includes/crm_md.md)] con [!INCLUDE[d365fin](includes/d365fin_md.md)], puede decidir si desea sincronizar los datos de campos seleccionados de los registros de [!INCLUDE[d365fin](includes/d365fin_md.md)] (como clientes, contactos y personal de ventas) con registros equivalentes en [!INCLUDE[d365fin](includes/d365fin_md.md)] (como cuentas, contactos y usuarios). Dependiendo del tipo de registro, puede sincronizar datos de [!INCLUDE[crm_md](includes/crm_md.md)] a [!INCLUDE[d365fin](includes/d365fin_md.md)], o viceversa. Para obtener más información, vea [Integración con Dynamics 365 for Sales](admin-prepare-dynamics-365-for-sales-for-integration.md).  

La sincronización utiliza los siguientes elementos:

* Lista de asignaciones de tablas de integración
* Asignaciones de campo de integración
* Reglas de sincronización
* Registros emparejados

Cuando la sincronización está configurada, puede emparejar registros de [!INCLUDE[d365fin](includes/d365fin_md.md)] con registros de [!INCLUDE[crm_md](includes/crm_md.md)] para sincronizar sus datos. Puede iniciar una sincronización manualmente o según una programación. La tabla siguiente proporciona un resumen de las formas en que puede sincronizar registros.  

|  Escriba  |  Método  |  Vea  |  
|--------|----------|-------|  
|Sincronización manual|Sincronizar en una base de registro por registro.<br /><br /> Puede sincronizar registros individuales en [!INCLUDE[d365fin](includes/d365fin_md.md)], por ejemplo, un cliente, con un registro de [!INCLUDE[crm_md](includes/crm_md.md)] correspondiente, por ejemplo, una cuenta. Normalmente, los usuarios trabajarán de esta manera con los datos de [!INCLUDE[crm_md](includes/crm_md.md)] en [!INCLUDE[d365fin](includes/d365fin_md.md)].|[Emparejar y sincronizar registros manualmente](admin-manual-synchronization-of-table-mappings.md#synchronize-individual-table-mappings)|  
|  |Sincronizar sobre según la asignación de tablas.<br /><br /> Puede sincronizar todos los registros de una tabla de [!INCLUDE[d365fin](includes/d365fin_md.md)] con una entidad de [!INCLUDE[crm_md](includes/crm_md.md)].|[Sincronizar las asignaciones de tablas individuales](admin-manual-synchronization-of-table-mappings.md#synchronize-individual-table-mappings)|  
||Sincronizar todos los registros modificados para todas las asignaciones de tablas.<br /><br /> Puede sincronizar todos los registros que se han modificado en las tablas de [!INCLUDE[d365fin](includes/d365fin_md.md)] desde la última sincronización.|[Sincronización de todos los registros modificados](admin-manual-synchronization-of-table-mappings.md#synchronizing-all-modified-records)|
||Sincronización completa de todos los datos para todas las asignaciones de tablas.<br /><br /> Puede sincronizar todos los datos de las tablas de [!INCLUDE[d365fin](includes/d365fin_md.md)] y entidades de [!INCLUDE[crm_md](includes/crm_md.md)] asignadas y crear nuevos registros en la solución de destino para los registros desemparejados en la solución de origen.<br /><br /> La sincronización completa sincroniza todos los datos y omite el emparejamiento. Normalmente, se realiza una sincronización completa cuando se configura la integración y solo una de las soluciones contiene datos. Una sincronización completa también puede ser útil en un entorno de demostración.|[Ejecutar una sincronización completa](admin-manual-synchronization-of-table-mappings.md#run-a-full-synchronization)|  
|Sincronización programada|Sincronizar todos los cambios en datos para todas las asignaciones de tablas.<br /><br /> Puede sincronizar [!INCLUDE[d365fin](includes/d365fin_md.md)] con [!INCLUDE[crm_md](includes/crm_md.md)] en intervalos programados configurando proyectos en la cola de proyectos.|[Programar una sincronización](admin-scheduled-synchronization-using-the-synchronization-job-queue-entries.md)|  

## <a name="standard-sales-entity-mapping-for-synchronization"></a>Asignación de entidad de Sales estándar para la sincronización
Las entidades en [!INCLUDE[crm_md](includes/crm_md.md)], como las cuentas, se integran con tipos equivalentes de entidades en [!INCLUDE[d365fin](includes/d365fin_md.md)], como los clientes. Para trabajar con datos de [!INCLUDE[crm_md](includes/crm_md.md)] se establecen vínculos, llamados emparejamientos, entre entidades en [!INCLUDE[d365fin](includes/d365fin_md.md)] y [!INCLUDE[crm_md](includes/crm_md.md)].

La siguiente tabla enumera la asignación estándar entre entidades en [!INCLUDE[d365fin](includes/d365fin_md.md)] y [!INCLUDE[crm_md](includes/crm_md.md)] que proporciona [!INCLUDE[d365fin](includes/d365fin_md.md)].

|[!INCLUDE[d365fin](includes/d365fin_md.md)]|[!INCLUDE[crm_md](includes/crm_md.md)]|Dirección de la sincronización|Filtro predeterminado|
|-------------------------------------------|-----|-------------------------|--------------|
|Vendedor/Comprador|Usuario|[!INCLUDE[crm_md](includes/crm_md.md)] -> [!INCLUDE[d365fin](includes/d365fin_md.md)]|Filtro de contacto de Sales: **Estado** es **No**, **Usuario con licencia** es **Sí**, Modo de integración de usuario es **No**|
|Cliente|Cuenta|[!INCLUDE[d365fin](includes/d365fin_md.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] y [!INCLUDE[crm_md](includes/crm_md.md)] -> [!INCLUDE[d365fin](includes/d365fin_md.md)]|Filtro de cuenta de Sales: **Tipo de relación** es **Cliente** y **Estado** es **Activo**.|
|Contacto|Contacto|[!INCLUDE[d365fin](includes/d365fin_md.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] y [!INCLUDE[crm_md](includes/crm_md.md)] -> [!INCLUDE[d365fin](includes/d365fin_md.md)]|Filtro de contacto de [!INCLUDE[d365fin](includes/d365fin_md.md)]: **Tipo** es **Persona** y el contacto se asigna a una empresa. Filtro de contacto de Sales: el contacto se asigna a una empresa y el tipo de cliente principal es **Cuenta**.|
|Divisa|Divisa de la transacción|[!INCLUDE[d365fin](includes/d365fin_md.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)]| |
|Unidad de medida|Grupo de unidad|[!INCLUDE[d365fin](includes/d365fin_md.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)]| |
|Producto|Producto|[!INCLUDE[d365fin](includes/d365fin_md.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] y [!INCLUDE[crm_md](includes/crm_md.md)] -> [!INCLUDE[d365fin](includes/d365fin_md.md)]|Filtro de contacto de Sales: **Tipo de producto** es **Inventario de ventas**|
|Recurso|Producto|[!INCLUDE[d365fin](includes/d365fin_md.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] y [!INCLUDE[crm_md](includes/crm_md.md)] -> [!INCLUDE[d365fin](includes/d365fin_md.md)]|Filtro de contacto de Sales: **Tipo de producto** es **Services**|
|Grupo precio cliente|Lista de precios|[!INCLUDE[d365fin](includes/d365fin_md.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)]| |
|Precio venta|Lista de precios de productos|[!INCLUDE[d365fin](includes/d365fin_md.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)]|Filtro de contacto de [!INCLUDE[d365fin](includes/d365fin_md.md)]: **Código ventas** no está en blanco, **Tipo de ventas** es **Grupo precio cliente**|
|Oportunidad|Oportunidad|[!INCLUDE[d365fin](includes/d365fin_md.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] y [!INCLUDE[crm_md](includes/crm_md.md)] -> [!INCLUDE[d365fin](includes/d365fin_md.md)]| |
|Histórico cab. factura venta|Facturar|[!INCLUDE[d365fin](includes/d365fin_md.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)]| |
|Histórico lín. factura venta|Producto de facturación|[!INCLUDE[d365fin](includes/d365fin_md.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)]| |
|Cabecera de pedido de cliente|Pedido venta|[!INCLUDE[d365fin](includes/d365fin_md.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)]|Filtro de cabecera de venta de [!INCLUDE[d365fin](includes/d365fin_md.md)]: **Tipo de documento** es Pedido, **Estado** es Lanzado|
|Notas de pedido de ventas|Notas de pedido de ventas|[!INCLUDE[d365fin](includes/d365fin_md.md)] -> [!INCLUDE[crm_md](includes/crm_md.md)] y [!INCLUDE[crm_md](includes/crm_md.md)] -> [!INCLUDE[d365fin](includes/d365fin_md.md)]| |

### <a name="tip-for-admins-viewing-entity-mappings"></a>Consejo para administradores: visualización de asignaciones de entidad
Puede ver la asignación entre las entidades en [!INCLUDE[crm_md](includes/crm_md.md)] y las tablas en la página en [!INCLUDE[d365fin](includes/d365fin_md.md)] en la página **Lista de asignaciones de tablas de integración**, donde también puede aplicar filtros. La asignación entre los campos de las tablas de [!INCLUDE[d365fin](includes/d365fin_md.md)] y los campos de las entidades de [!INCLUDE[crm_md](includes/crm_md.md)] se define en la página **Lista de asignaciones de campos de integración**, donde se puede añadir lógica de asignación adicional. Por ejemplo, esto puede ser útil si necesita solucionar problemas de sincronización.

### <a name="tip-for-developers-mapping-fields-in-business-central-to-the-option-sets-in-sales"></a>Consejo para desarrolladores: asignación de campos en Business Central a los conjuntos de opciones en Sales
Si es un desarrollador y desea añadir opciones a los conjuntos de opciones de [!INCLUDE[crm_md](includes/crm_md.md)], debe saber esto. Hay tres tablas en [!INCLUDE[d365fin](includes/d365fin_md.md)] que se asignan a los campos de opción de la entidad **Cuenta** en [!INCLUDE[crm_md](includes/crm_md.md)]. Los registros de las tablas que no están vinculados a las opciones en [!INCLUDE[crm_md](includes/crm_md.md)] no se sincronizarán. Esto significa que el campo **Opción** aparecerá en blanco en [!INCLUDE[crm_md](includes/crm_md.md)].

La tabla siguiente muestra las asignaciones de las tablas de [!INCLUDE[d365fin](includes/d365fin_md.md)] para el campo **Opción** en la entidad **Cuenta** en [!INCLUDE[crm_md](includes/crm_md.md)].

|Escritorio|Campo de opción en la entidad de cuenta|
|----------------------|-------------------------------------------|
|Términos de pago|Términos de pago|
|Condiciones de envío|Dirección 1: Condiciones de flete|
|Transportista|Dirección 1: Método de envío|

### <a name="synchronization-rules"></a>Reglas de sincronización
En la tabla siguiente se describen las reglas que controlan la sincronización entre las aplicaciones.

> [!NOTE]  
> Los cambios en los datos en [!INCLUDE[crm_md](includes/crm_md.md)] realizados por la cuenta de usuario de conexión de [!INCLUDE[crm_md](includes/crm_md.md)] no están sincronizados. Por lo tanto, le recomendamos que no modifique los datos mientras utiliza esa cuenta. Para obtener más información, consulte [Configuración de la integración con Dynamics 365 for Sales](admin-setting-up-integration-with-dynamics-sales.md).

|Escritorio|Regla|
|-----|----|
|Clientes|Para que un cliente pueda sincronizarse a una cuenta, el vendedor que está asignado al cliente debe emparejarse con un usuario de [!INCLUDE[crm_md](includes/crm_md.md)]. Por lo tanto, cuando ejecute el proyecto de sincronización CLIENTES - Dynamics 365 for Sales y lo configure para crear nuevos registros, asegúrese de que sincroniza los vendedores con los usuarios de [!INCLUDE[crm_md](includes/crm_md.md)] antes de sincronizar los clientes con cuentas de [!INCLUDE[crm_md](includes/crm_md.md)]. <br /> <br />El proyecto de sincronización CLIENTES - Dynamics 365 for Sales solo sincroniza cuentas de Sales cuyo tipo de relación es Cliente.|
|Contactos|Solo los contactos de [!INCLUDE[crm_md](includes/crm_md.md)] que estén asociados con una cuenta se crearán en [!INCLUDE[d365fin](includes/d365fin_md.md)]. El valor de Código de vendedor define el propietario de la entidad emparejada en [!INCLUDE[crm_md](includes/crm_md.md)].|
|Divisas|Las divisas se emparejan con divisas de transacción en [!INCLUDE[crm_md](includes/crm_md.md)] según los códigos ISO. Solo las divisas que tengan un código ISO estándar se acoplarán y sincronizarán con divisas de transacción.|
|Unidades medida|Las unidades de medida se sincronizan con grupos de unidades en [!INCLUDE[crm_md](includes/crm_md.md)]. Solo puede haber una unidad de medida definida en la unidad de venta.|
|Productos|Al sincronizar artículos con los productos de [!INCLUDE[crm_md](includes/crm_md.md)], [!INCLUDE[d365fin](includes/d365fin_md.md)] crea automáticamente una lista de precios en [!INCLUDE[crm_md](includes/crm_md.md)]. Para evitar errores de sincronización, no debe modificar la lista de precios manualmente.|
|Vendedores|Los vendedores están emparejados con los usuarios del sistema en [!INCLUDE[crm_md](includes/crm_md.md)]. El usuario debe estar habilitado y con licencia, y no debe ser el usuario de integración. Tenga en cuenta que esta es la primera tabla que debe sincronizarse porque se utiliza en clientes, contactos, oportunidades y facturas de venta.|
|Recursos|Los recursos se sincronizan con los productos de [!INCLUDE[crm_md](includes/crm_md.md)] que tienen el tipo de producto Servicio.|
|Grupos precio cliente|Los grupos de precios de cliente se sincronizan con las listas de precios de Sales.|
|Precios ventas|Los precios de Sales que tienen el tipo de venta Grupo precio cliente y tengan un código de venta definido se sincronizan con las líneas de lista de precios de [!INCLUDE[crm_md](includes/crm_md.md)].|
|Oportunidades|Las oportunidades se sincronizan con las oportunidades de [!INCLUDE[crm_md](includes/crm_md.md)]. El valor de Código de vendedor define el propietario de la entidad emparejada en [!INCLUDE[crm_md](includes/crm_md.md)].|
|Histórico facturas venta|Las facturas de ventas registradas se sincronizan con las facturas de ventas. Para poder sincronizar una factura, es mejor sincronizar las demás entidades que puedan participar en la factura, desde los vendedores hasta las listas de precios. El valor de Código de vendedor en la cabecera de la factura define el propietario de la entidad acoplada en Sales.|
|Pedidos de venta|El pedido de venta lanzado (cabeceras) se sincroniza con el pedido de venta. Para poder sincronizar un pedido, es mejor sincronizar las demás entidades que puedan participar en el pedido, desde los vendedores hasta las listas de precios. El valor de Código de vendedor en la cabecera del pedido define el propietario de la entidad emparejada en Sales.|  

## <a name="see-also"></a>Consulte también  
[Emparejar y sincronizar registros manualmente](admin-how-to-couple-and-synchronize-records-manually.md)   
[Programar una sincronización](admin-scheduled-synchronization-using-the-synchronization-job-queue-entries.md)   
[Integración con Dynamics 365 for Sales](admin-prepare-dynamics-365-for-sales-for-integration.md)
