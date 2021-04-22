---
title: Sincronización e integración de datos | Documentos de Microsoft
description: La sincronización copia los datos entre las tablas de Microsoft Dataverse y los registros de Business Central, y mantiene actualizados los datos de ambos sistemas.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Dataverse, integration, sync, synchronize, mapping
ms.date: 04/01/2021
ms.author: bholtorf
ms.openlocfilehash: 9a912596a71e77a09a7491fe20032056d1a9b808
ms.sourcegitcommit: 8b44a7bcba45ae852cc6dd07b90b9a383c1be488
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/08/2021
ms.locfileid: "5870028"
---
# <a name="synchronizing-data-in-business-central-with-microsoft-dataverse"></a>Sincronización de datos en Business Central con Microsoft Dataverse
[!INCLUDE[prod_short](includes/cc_data_platform_banner.md)]

Cuando integra [!INCLUDE[prod_short](includes/cds_long_md.md)] con [!INCLUDE[prod_short](includes/prod_short.md)], puede decidir si desea sincronizar los datos de campos seleccionados de [!INCLUDE[prod_short](includes/prod_short.md)] (como clientes, contactos y personal de ventas) con las filas equivalentes en [!INCLUDE[prod_short](includes/cds_long_md.md)] (como cuentas, contactos y usuarios). Dependiendo del tipo de fila, puede sincronizar datos de [!INCLUDE[prod_short](includes/cds_long_md.md)] a [!INCLUDE[prod_short](includes/prod_short.md)], o viceversa. Para obtener más información, vea [Integración con Dynamics 365 Sales](admin-prepare-dynamics-365-for-sales-for-integration.md).  

La sincronización utiliza los siguientes elementos:

* Lista de asignaciones de tablas de integración
* Asignaciones de campo de integración
* Reglas de sincronización
* Registros emparejados

Cuando la sincronización está configurada, puede emparejar filas de [!INCLUDE[prod_short](includes/prod_short.md)] con registros de [!INCLUDE[prod_short](includes/cds_long_md.md)] para sincronizar sus datos. Puede iniciar una sincronización manualmente o según una programación. La tabla siguiente proporciona un resumen de las formas en que puede sincronizar.  

|  Escriba  |  Método  |  Vea  |  
|--------|----------|-------|  
|Sincronización manual|Sincronizar en una base de fila a fila.<br /><br /> Puede sincronizar registros individuales en [!INCLUDE[prod_short](includes/prod_short.md)], por ejemplo, un cliente, con una fila de [!INCLUDE[prod_short](includes/cds_long_md.md)] correspondiente, por ejemplo, una cuenta. Normalmente, los usuarios trabajarán de esta manera con los datos de [!INCLUDE[prod_short](includes/cds_long_md.md)] en [!INCLUDE[prod_short](includes/prod_short.md)].|[Emparejar y sincronizar registros manualmente](admin-manual-synchronization-of-table-mappings.md#synchronize-individual-table-mappings)|  
|  |Sincronizar sobre según la asignación de tablas.<br /><br /> Puede sincronizar todos los registros de una tabla de [!INCLUDE[prod_short](includes/prod_short.md)] con una tabla de [!INCLUDE[prod_short](includes/cds_long_md.md)].|[Sincronizar las asignaciones de tablas individuales](admin-manual-synchronization-of-table-mappings.md#synchronize-individual-table-mappings)|  
||Sincronizar todos los registros modificados para todas las asignaciones de tablas.<br /><br /> Puede sincronizar todos los registros que se han modificado en las tablas de [!INCLUDE[prod_short](includes/prod_short.md)] desde la última sincronización.|[Sincronización de todos los registros modificados](admin-manual-synchronization-of-table-mappings.md#synchronizing-all-modified-records)|
||Sincronización completa de todos los datos para todas las asignaciones de tablas.<br /><br /> Puede sincronizar todos los datos de las tablas de [!INCLUDE[prod_short](includes/prod_short.md)] y tablas de [!INCLUDE[prod_short](includes/cds_long_md.md)] asignadas y crear nuevos registros en la solución de destino para los registros o filas desemparejados en la solución de origen.<br /><br /> La sincronización completa sincroniza todos los datos y omite el emparejamiento. Normalmente, se realiza una sincronización completa cuando se configura la integración y solo una de las soluciones contiene datos. Una sincronización completa también puede ser útil en un entorno de demostración.|[Ejecutar una sincronización completa](admin-manual-synchronization-of-table-mappings.md#run-a-full-synchronization)|  
|Sincronización programada|Sincronizar todos los cambios en datos para todas las asignaciones de tablas.<br /><br /> Puede sincronizar [!INCLUDE[prod_short](includes/prod_short.md)] con [!INCLUDE[prod_short](includes/cds_long_md.md)] en intervalos programados configurando proyectos en la cola de proyectos.|[Programar una sincronización](admin-scheduled-synchronization-using-the-synchronization-job-queue-entries.md)|  

## <a name="standard-table-mapping-for-synchronization"></a>Asignación de tablas estándar para la sincronización
Las tablas en [!INCLUDE[prod_short](includes/cds_long_md.md)], como las cuentas, se integran con tipos equivalentes de tablas en [!INCLUDE[prod_short](includes/prod_short.md)], como los clientes. Para trabajar con datos de [!INCLUDE[prod_short](includes/cds_long_md.md)] se establecen vínculos, llamados emparejamientos, entre tablas en [!INCLUDE[prod_short](includes/prod_short.md)] y [!INCLUDE[prod_short](includes/cds_long_md.md)].

La siguiente tabla enumera la asignación estándar entre tablas en [!INCLUDE[prod_short](includes/prod_short.md)] y [!INCLUDE[prod_short](includes/cds_long_md.md)].

> [!TIP]
> Puede restablecer los cambios de configuración realizados en la tabla de integración y las asignaciones de campo a su configuración predeterminada, seleccionando las asignaciones y luego eligiendo **Usar la configuración de sincronización predeterminada**.

| [!INCLUDE[prod_short](includes/prod_short.md)] | [!INCLUDE[prod_short](includes/cds_long_md.md)] | Dirección de la sincronización | Filtro predeterminado |
|---------------------------------------------|----------------------------------------------|---------------------------|----------------|
| Vendedor/Comprador | Usuario | [!INCLUDE[prod_short](includes/cds_long_md.md)] -> [!INCLUDE[prod_short](includes/prod_short.md)] | Filtro de contacto de [!INCLUDE[prod_short](includes/cds_long_md.md)]: **Estado** es **No**, **Usuario con licencia** es **Sí**, Modo de integración de usuario es **No** |
| Cliente | Cuenta | [!INCLUDE[prod_short](includes/prod_short.md)] -> [!INCLUDE[prod_short](includes/cds_long_md.md)] y [!INCLUDE[prod_short](includes/cds_long_md.md)] -> [!INCLUDE[prod_short](includes/prod_short.md)] | Filtro de cuenta de [!INCLUDE[prod_short](includes/cds_long_md.md)]: el **Tipo de relación** es **Cliente** y el **Estado** es **Activo**. Filtro de [!INCLUDE[prod_short](includes/prod_short.md)]: **Bloqueado** está vacío (Cliente no está bloqueado). |
| Proveedor | Cuenta | [!INCLUDE[prod_short](includes/prod_short.md)] -> [!INCLUDE[prod_short](includes/cds_long_md.md)] y [!INCLUDE[prod_short](includes/cds_long_md.md)] -> [!INCLUDE[prod_short](includes/prod_short.md)] | Filtro de cuenta de [!INCLUDE[prod_short](includes/cds_long_md.md)]: el **Tipo de relación** es **Proveedor** y el **Estado** es **Activo**. Filtro de [!INCLUDE[prod_short](includes/prod_short.md)]: **Bloqueado** está vacío (Proveedor no está bloqueado). |
| Contacto | Contacto | [!INCLUDE[prod_short](includes/prod_short.md)] -> [!INCLUDE[prod_short](includes/cds_long_md.md)] y [!INCLUDE[prod_short](includes/cds_long_md.md)] -> [!INCLUDE[prod_short](includes/prod_short.md)] | Filtro de contacto de [!INCLUDE[prod_short](includes/prod_short.md)]: el **tipo** es **Persona** y el contacto se asigna una empresa. Filtro de contacto de [!INCLUDE[prod_short](includes/cds_long_md.md)]: el contacto se asigna a una empresa y el tipo de cliente principal es **Cuenta** |
| Divisa | Divisa de la transacción | [!INCLUDE[prod_short](includes/prod_short.md)] -> [!INCLUDE[prod_short](includes/cds_long_md.md)] |  |


### <a name="tip-for-admins-viewing-table-mappings"></a>Consejo para administradores: visualización de asignaciones de tabla
Puede ver la asignación entre las tablas en [!INCLUDE[prod_short](includes/cds_long_md.md)] y [!INCLUDE[prod_short](includes/prod_short.md)] en la página **Lista de asignaciones de tablas de integración**, donde también puede aplicar filtros. La asignación entre los campos de las tablas de [!INCLUDE[prod_short](includes/prod_short.md)] y las columnas de las tablas de [!INCLUDE[prod_short](includes/cds_long_md.md)] se define en la página **Lista de asignaciones de campos de integración**, donde se puede añadir lógica de asignación adicional. Por ejemplo, esto puede ser útil si necesita solucionar problemas de sincronización.

## <a name="see-also"></a>Consulte también  
[Emparejar y sincronizar registros manualmente](admin-how-to-couple-and-synchronize-records-manually.md)   
[Programar una sincronización](admin-scheduled-synchronization-using-the-synchronization-job-queue-entries.md)   
[Integración con Dynamics 365 Sales](admin-prepare-dynamics-365-for-sales-for-integration.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
