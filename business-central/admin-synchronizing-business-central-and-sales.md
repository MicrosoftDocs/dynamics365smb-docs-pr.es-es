---
title: Sincronización e integración de datos | Documentos de Microsoft
description: La sincronización copia los datos entre las entidades de Common Data Service y los registros de Business Central, y mantiene actualizados los datos de ambos sistemas.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: sales, crm, integration, sync, synchronize
ms.date: 04/01/2020
ms.author: bholtorf
ms.openlocfilehash: 0763119e323a8bae6d2b7ce3db0780284befa292
ms.sourcegitcommit: 0c6f4382fad994fb6aea9dcde3b2dc25382c5968
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2020
ms.locfileid: "3484114"
---
# <a name="synchronizing-data-in-business-central-with-common-data-service"></a>Sincronización de datos en Business Central con Common Data Service
Cuando integra [!INCLUDE[d365fin](includes/cds_long_md.md)] con [!INCLUDE[d365fin](includes/d365fin_md.md)], puede decidir si desea sincronizar los datos de campos seleccionados de los registros de [!INCLUDE[d365fin](includes/d365fin_md.md)] (como clientes, contactos y personal de ventas) con registros equivalentes en [!INCLUDE[d365fin](includes/cds_long_md.md)] (como cuentas, contactos y usuarios). Dependiendo del tipo de registro, puede sincronizar datos de [!INCLUDE[d365fin](includes/cds_long_md.md)] a [!INCLUDE[d365fin](includes/d365fin_md.md)], o viceversa. Para obtener más información, vea [Integración con Dynamics 365 Sales](admin-prepare-dynamics-365-for-sales-for-integration.md).  

La sincronización utiliza los siguientes elementos:

* Lista de asignaciones de tablas de integración
* Asignaciones de campo de integración
* Reglas de sincronización
* Registros emparejados

Cuando la sincronización está configurada, puede emparejar registros de [!INCLUDE[d365fin](includes/d365fin_md.md)] con registros de [!INCLUDE[d365fin](includes/cds_long_md.md)] para sincronizar sus datos. Puede iniciar una sincronización manualmente o según una programación. La tabla siguiente proporciona un resumen de las formas en que puede sincronizar registros.  

|  Escriba  |  Método  |  Vea  |  
|--------|----------|-------|  
|Sincronización manual|Sincronizar en una base de registro por registro.<br /><br /> Puede sincronizar registros individuales en [!INCLUDE[d365fin](includes/d365fin_md.md)], por ejemplo, un cliente, con un registro de [!INCLUDE[d365fin](includes/cds_long_md.md)] correspondiente, por ejemplo, una cuenta. Normalmente, los usuarios trabajarán de esta manera con los datos de [!INCLUDE[d365fin](includes/cds_long_md.md)] en [!INCLUDE[d365fin](includes/d365fin_md.md)].|[Emparejar y sincronizar registros manualmente](admin-manual-synchronization-of-table-mappings.md#synchronize-individual-table-mappings)|  
|  |Sincronizar sobre según la asignación de tablas.<br /><br /> Puede sincronizar todos los registros de una tabla de [!INCLUDE[d365fin](includes/d365fin_md.md)] con una entidad de [!INCLUDE[d365fin](includes/cds_long_md.md)].|[Sincronizar las asignaciones de tablas individuales](admin-manual-synchronization-of-table-mappings.md#synchronize-individual-table-mappings)|  
||Sincronizar todos los registros modificados para todas las asignaciones de tablas.<br /><br /> Puede sincronizar todos los registros que se han modificado en las tablas de [!INCLUDE[d365fin](includes/d365fin_md.md)] desde la última sincronización.|[Sincronización de todos los registros modificados](admin-manual-synchronization-of-table-mappings.md#synchronizing-all-modified-records)|
||Sincronización completa de todos los datos para todas las asignaciones de tablas.<br /><br /> Puede sincronizar todos los datos de las tablas de [!INCLUDE[d365fin](includes/d365fin_md.md)] y entidades de [!INCLUDE[d365fin](includes/cds_long_md.md)] asignadas y crear nuevos registros en la solución de destino para los registros desemparejados en la solución de origen.<br /><br /> La sincronización completa sincroniza todos los datos y omite el emparejamiento. Normalmente, se realiza una sincronización completa cuando se configura la integración y solo una de las soluciones contiene datos. Una sincronización completa también puede ser útil en un entorno de demostración.|[Ejecutar una sincronización completa](admin-manual-synchronization-of-table-mappings.md#run-a-full-synchronization)|  
|Sincronización programada|Sincronizar todos los cambios en datos para todas las asignaciones de tablas.<br /><br /> Puede sincronizar [!INCLUDE[d365fin](includes/d365fin_md.md)] con [!INCLUDE[d365fin](includes/cds_long_md.md)] en intervalos programados configurando proyectos en la cola de proyectos.|[Programar una sincronización](admin-scheduled-synchronization-using-the-synchronization-job-queue-entries.md)|  

## <a name="standard-entity-mapping-for-synchronization"></a>Asignación de entidades estándar para la sincronización
Las entidades en [!INCLUDE[d365fin](includes/cds_long_md.md)], como las cuentas, se integran con tipos equivalentes de entidades en [!INCLUDE[d365fin](includes/d365fin_md.md)], como los clientes. Para trabajar con datos de [!INCLUDE[d365fin](includes/cds_long_md.md)] se establecen vínculos, llamados emparejamientos, entre entidades en [!INCLUDE[d365fin](includes/d365fin_md.md)] y [!INCLUDE[d365fin](includes/cds_long_md.md)].

La siguiente tabla enumera la asignación estándar entre entidades en [!INCLUDE[d365fin](includes/d365fin_md.md)] y [!INCLUDE[d365fin](includes/cds_long_md.md)] que proporciona [!INCLUDE[d365fin](includes/d365fin_md.md)].

|[!INCLUDE[d365fin](includes/d365fin_md.md)]|[!INCLUDE[d365fin](includes/cds_long_md.md)]|Dirección de la sincronización|Filtro predeterminado|
|-------------------------------------------|-----|-------------------------|--------------|
|Vendedor/Comprador|Usuario|[!INCLUDE[d365fin](includes/cds_long_md.md)] -> [!INCLUDE[d365fin](includes/d365fin_md.md)]|Filtro de contacto de [!INCLUDE[d365fin](includes/cds_long_md.md)]: **Estado** es **No**, **Usuario con licencia** es **Sí**, Modo de integración de usuario es **No**|
|Cliente|Cuenta|[!INCLUDE[d365fin](includes/d365fin_md.md)] -> [!INCLUDE[d365fin](includes/cds_long_md.md)] y [!INCLUDE[d365fin](includes/cds_long_md.md)] -> [!INCLUDE[d365fin](includes/d365fin_md.md)]|Filtro de cuenta de [!INCLUDE[d365fin](includes/cds_long_md.md)]: el **Tipo de relación** es **Cliente** y el **Estado** es **Activo**. Filtro de [!INCLUDE[d365fin](includes/d365fin_md.md)]: **Bloqueado** está vacío (Cliente no está bloqueado).|
|Proveedor|Cuenta|[!INCLUDE[d365fin](includes/d365fin_md.md)] -> [!INCLUDE[d365fin](includes/cds_long_md.md)] y [!INCLUDE[d365fin](includes/cds_long_md.md)] -> [!INCLUDE[d365fin](includes/d365fin_md.md)]|Filtro de cuenta de [!INCLUDE[d365fin](includes/cds_long_md.md)]: el **Tipo de relación** es **Proveedor** y el **Estado** es **Activo**. Filtro de [!INCLUDE[d365fin](includes/d365fin_md.md)]: **Bloqueado** está vacío (Proveedor no está bloqueado).|
|Contacto|Contacto|[!INCLUDE[d365fin](includes/d365fin_md.md)] -> [!INCLUDE[d365fin](includes/cds_long_md.md)] y [!INCLUDE[d365fin](includes/cds_long_md.md)] -> [!INCLUDE[d365fin](includes/d365fin_md.md)]|Filtro de contacto de [!INCLUDE[d365fin](includes/d365fin_md.md)]: el **tipo** es **Persona** y el contacto se asigna una empresa. Filtro de contacto de [!INCLUDE[d365fin](includes/cds_long_md.md)]: el contacto se asigna a una empresa y el tipo de cliente principal es **Cuenta**|
|Divisa|Divisa de la transacción|[!INCLUDE[d365fin](includes/d365fin_md.md)] -> [!INCLUDE[d365fin](includes/cds_long_md.md)]| |


### <a name="tip-for-admins-viewing-entity-mappings"></a>Consejo para administradores: visualización de asignaciones de entidad
Puede ver la asignación entre las entidades en [!INCLUDE[d365fin](includes/cds_long_md.md)] y las tablas en la página en [!INCLUDE[d365fin](includes/d365fin_md.md)] en la página **Lista de asignaciones de tablas de integración**, donde también puede aplicar filtros. La asignación entre los campos de las tablas de [!INCLUDE[d365fin](includes/d365fin_md.md)] y los campos de las entidades de [!INCLUDE[d365fin](includes/cds_long_md.md)] se define en la página **Lista de asignaciones de campos de integración**, donde se puede añadir lógica de asignación adicional. Por ejemplo, esto puede ser útil si necesita solucionar problemas de sincronización.

## <a name="see-also"></a>Consulte también  
[Emparejar y sincronizar registros manualmente](admin-how-to-couple-and-synchronize-records-manually.md)   
[Programar una sincronización](admin-scheduled-synchronization-using-the-synchronization-job-queue-entries.md)   
[Integración con Dynamics 365 Sales](admin-prepare-dynamics-365-for-sales-for-integration.md)
