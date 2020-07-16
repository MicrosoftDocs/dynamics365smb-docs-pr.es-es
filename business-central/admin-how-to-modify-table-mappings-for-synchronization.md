---
title: Asignación de tablas y campos para sincronizar | Documentos de Microsoft
description: Aprenda a asignar tablas y campos para sincronizar datos entre Business Central y Common Data Service.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: sales, crm, integration, sync, synchronize, table mapping
ms.date: 04/20/2020
ms.author: bholtorf
ms.openlocfilehash: 0b814c18c328ea0647e38b6a837577b277ca4e63
ms.sourcegitcommit: 3e9c89f90db5eaed599630299353300621fe4007
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 07/01/2020
ms.locfileid: "3527940"
---
# <a name="mapping-the-tables-and-fields-to-synchronize"></a>Asignación de tablas y campos para sincronizar
La base de la sincronización de datos en [!INCLUDE[d365fin](includes/d365fin_md.md)] con datos en [!INCLUDE[d365fin](includes/cds_long_md.md)] es asignar las tablas y campos que contienen los datos entre sí. La asignación ocurre a través de tablas de integración. 

## <a name="mapping-integration-tables"></a>Asignación de tablas de integración
Una tabla de la integración es una tabla [!INCLUDE[d365fin](includes/d365fin_md.md)] de la base de datos que representa una entidad en [!INCLUDE[cds_long_md](includes/cds_long_md.md)]. Las tablas de integración incluyen campos correspondientes a los campos en la tabla de la [!INCLUDE[cds_long_md](includes/cds_long_md.md)] entidad. Por ejemplo, la tabla de integración de Cuenta se conecta a la entidad Cuentas en [!INCLUDE[cds_short_md](includes/cds_long_md.md)]. Debe existir una asignación de tabla de integración correspondiente para cada entidad en [!INCLUDE[cds_short_md](includes/cds_short_md.md)] en la que desee sincronizar los datos [!INCLUDE[prodshort](includes/prodshort.md)].

Cuando cree la conexión entre las aplicaciones, [!INCLUDE[d365fin](includes/d365fin_md.md)] se configuran algunas asignaciones de tabla y campo predeterminadas. Puede modificar la asignación de tablas si lo desea. Para obtener más información, consulte [Asignación de entidad estándar para la sincronización](admin-synchronizing-business-central-and-sales.md#standard-entity-mapping-for-synchronization). Si ha cambiado las asignaciones predeterminadas y desea revertir sus cambios, en la página **Configuración de conexión de [!INCLUDE[d365fin](includes/cds_long_md.md)]** elija **Usar configuración de sincronización predeterminada**.

> [!Note]
> Si está utilizando una versión local, [!INCLUDE[d365fin](includes/d365fin_md.md)] las asignaciones de la tabla de integración se almacenan en la tabla 5335 de Asignaciones de la tabla de integración y se pueden ver y modificar desde la página 5335 de Asignaciones de la tabla de integración. Las asignaciones complejas y las reglas de sincronización se definen en la codeunit 5341. 

### <a name="synchronization-rules"></a>Reglas de sincronización
Una asignación de tabla de integración también incluye reglas que controlan cómo los trabajos de sincronización de integración sincronizan registros en una [!INCLUDE[d365fin](includes/d365fin_md.md)] tabla y una entidad en [!INCLUDE[d365fin](includes/cds_long_md.md)]. <!--For examples of rules for an integration with Sales, see [Synchronization Rules](admin-synchronizing-business-central-and-sales.md#synchronization-rules). need to verify link -->

## <a name="mapping-integration-fields"></a>Asignaciones de campo de integración
La asignación de tablas es solo el primer paso. También debe asignar los campos en las tablas. Las asignaciones de campos de integración vinculan campos en [!INCLUDE[d365fin](includes/d365fin_md.md)] tablas con campos correspondientes en [!INCLUDE[d365fin](includes/cds_long_md.md)]y determinan si se sincronizarán los datos en cada tabla. La asignación de tabla estándar que [!INCLUDE[d365fin](includes/d365fin_md.md)] proporciona incluye asignaciones de campo, pero puede cambiarlas si lo desea. Para obtener más información, consulte [Ver asignaciones de entidad](admin-synchronizing-business-central-and-sales.md#tip-for-admins-viewing-entity-mappings).

> [!Note]
> Si está utilizando una versión local de [!INCLUDE[d365fin](includes/d365fin_md.md)], las asignaciones de campos de integración se definen en la tabla 5336 de Asignación de campos de integración.

### <a name="handling-differences-in-field-values"></a>Administración de diferencias en valores de campo
A veces, los valores en los campos que desea asignar son diferentes. Por ejemplo, en [!INCLUDE[crm_md](includes/crm_md.md)], el código de idioma para Estados Unidos es "U.S.", pero en [!INCLUDE[d365fin](includes/d365fin_md.md)] es "US". Eso significa que debe transformar el valor cuando sincroniza los datos. Esto sucede por de las reglas de transformación que define para los campos. Las reglas de transformación se definen en la página **Asignaciones de tablas de integración**, eligiendo **Asignación** y luego **Campos**. Se proporcionan reglas predefinidas, pero también puede crear las suyas propias. Para obtener más información, vea [Reglas de transformación](across-how-to-set-up-data-exchange-definitions.md#transformation-rules).

### <a name="handling-missing-option-values-in-mapping"></a>Administración de valores de opciones que faltan en la asignación
[!INCLUDE[d365fin](includes/cds_long_md.md)] contiene solo tres campos de conjunto de opciones que proporcionan valores que puede asignar a campos [!INCLUDE[d365fin](includes/d365fin_md.md)] de tipo **Opción** para la sincronización automática. Durante la sincronización, las opciones no asignadas se ignoran y las opciones que faltan se anexan a la tabla [!INCLUDE[d365fin](includes/d365fin_md.md)] relacionada y se agregan la tabla de sistema **Asignación de opciones de CDS** para su administración manual más tarde. Por ejemplo, agregando las opciones que faltan en cualquiera de los productos y luego actualizando la asignación. Para más información, vea [Administración de valores de opciones que faltan](admin-cds-missing-option-values.md).

## <a name="coupling-records"></a>Emparejamiento de registros
Emparejando registros de enlaces en [!INCLUDE[d365fin](includes/cds_long_md.md)] a los registros en [!INCLUDE[d365fin](includes/d365fin_md.md)]. Por ejemplo, las cuentas en [!INCLUDE[d365fin](includes/cds_long_md.md)] normalmente se combinan con los clientes en [!INCLUDE[d365fin](includes/d365fin_md.md)]. Los registros de acoplamiento ofrecen los siguientes beneficios:

* Posibilita la sincronización.
* Los usuarios pueden abrir registros en una aplicación comercial de la otra. Esto requiere que las aplicaciones ya estén integradas.

Los acoplamientos se pueden configurar automáticamente mediante los proyectos de sincronización o manualmente, modificando el registro en el cliente en [!INCLUDE[d365fin](includes/d365fin_md.md)]. Para más información, consulte [Sincronizar datos en [!INCLUDE[d365fin](includes/d365fin_md.md)] y [!INCLUDE[d365fin](includes/cds_long_md.md)]](admin-synchronizing-business-central-and-sales.md) y [Emparejar y sincronizar registros manualmente](admin-manual-synchronization-of-table-mappings.md#synchronize-individual-table-mappings).

## <a name="filtering-records"></a>Filtrar registros  
Si no desea sincronizar todos los registros para una entidad de [!INCLUDE[d365fin](includes/cds_long_md.md)] o una tabla de [!INCLUDE[d365fin](includes/d365fin_md.md)] concreta, puede configurar filtros para limitar los registros que se sincronizan. Los filtros se configuran en la página **Lista de asignaciones de tablas de integración**.  

#### <a name="to-filter-records-for-synchronization"></a>Para filtrar registros para la sincronización  
1. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Asignaciones de tablas de integración** y luego elija el enlace relacionado.

2.  Para filtrar los registros de [!INCLUDE[d365fin](includes/d365fin_md.md)], establezca el campo **Filtro de tabla**.  

3.  Para filtrar los registros de [!INCLUDE[d365fin](includes/cds_long_md.md)], establezca el campo **Filtro de tabla de integración**.  

## <a name="creating-new-records"></a>Crear registros nuevos  
De manera predeterminada, solo los registros de [!INCLUDE[d365fin](includes/d365fin_md.md)] y [!INCLUDE[d365fin](includes/cds_long_md.md)] que están emparejados se sincronizarán mediante proyectos de sincronización de integración. Puede configurar asignaciones de tabla de manera que se creen nuevos registros en el destino (por ejemplo, [!INCLUDE[d365fin](includes/d365fin_md.md)]) para cada registro del origen (por ejemplo, [!INCLUDE[d365fin](includes/cds_long_md.md)]) que aún no está emparejado.  

Por ejemplo, el proyecto de sincronización de Dynamics 365 Sales VENDEDORES usa la asignación de tabla VENDEDORES. El proyecto de sincronización copia los datos de los registros del usuario de [!INCLUDE[d365fin](includes/cds_long_md.md)] en los registros de vendedores de [!INCLUDE[d365fin](includes/d365fin_md.md)]. Si configura la asignación de tabla para crear registros nuevos, para cada usuario de [!INCLUDE[d365fin](includes/cds_long_md.md)] que aún no está acoplado a un vendedor de [!INCLUDE[d365fin](includes/d365fin_md.md)], se crea un registro de vendedor en [!INCLUDE[d365fin](includes/d365fin_md.md)].  

#### <a name="to-create-new-records-during-synchronization"></a>Para crear registros nuevos durante la sincronización  
1. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Asignaciones de tablas de integración** y luego elija el enlace relacionado.

2.  En el movimiento de asignación de tabla de la lista, borre el campo **Sincronizar solo reg. emparejados**.  

## <a name="using-configuration-templates-on-table-mappings"></a>Uso de plantillas de configuración en asignaciones de tabla
Puede asignar plantillas de configuración a asignaciones de tabla para utilizarlas para registros nuevos que se crean en [!INCLUDE[d365fin](includes/d365fin_md.md)] o [!INCLUDE[d365fin](includes/cds_long_md.md)]. Para cada asignación de tabla, puede especificar una plantilla de configuración para utilizarla para los registros nuevos de [!INCLUDE[d365fin](includes/d365fin_md.md)] y otra plantilla para utilizar registros nuevos de [!INCLUDE[d365fin](includes/cds_long_md.md)].  

Si instala la configuración de sincronización predeterminada, la mayoría de las veces, se crearán automáticamente dos plantillas de configuración que se utilizarán en la asignación de tabla para clientes de [!INCLUDE[d365fin](includes/d365fin_md.md)] y cuentas de [!INCLUDE[crm_md](includes/crm_md.md)]: **CDSCUST** y **CDSACCOUNT**.  

-   **CDSCUST** se utiliza para crear y sincronizar clientes nuevos de [!INCLUDE[d365fin](includes/d365fin_md.md)] basándose en una cuenta de [!INCLUDE[crm_md](includes/crm_md.md)].  

     Esta plantilla se crea copiando una plantilla de configuración existente para clientes de la aplicación. **CDSCUST** solo se crea si hay una plantilla de configuración existente y el campo **Código de divisa** de la plantilla está en blanco. Si un campo de la plantilla de la configuración contiene un valor, el valor se utilizará en lugar del valor del campo asignado para la cuenta de [!INCLUDE[d365fin](includes/cds_long_md.md)]. Por ejemplo, si el campo **País/región** de una cuenta de [!INCLUDE[d365fin](includes/cds_long_md.md)] contiene *EE. UU.* y el campo **País/región** de la plantilla de configuración es *ES*, *ES* se utiliza como **País/región** para el cliente en [!INCLUDE[d365fin](includes/d365fin_md.md)].  

-   **CDSACCOUNT** crea y sincroniza cuentas nuevas de [!INCLUDE[d365fin](includes/cds_long_md.md)] basándose en una cuenta de [!INCLUDE[d365fin](includes/d365fin_md.md)].  

#### <a name="to-specify-configuration-templates-on-a-table-mapping"></a>Para especificar plantillas de configuración en una asignación de tabla  
1. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Asignaciones de tablas de integración** y luego elija el enlace relacionado.

2.  En el movimiento de asignación de tabla de la lista, en el campo **Código de plantilla de config. de tabla**, elija la plantilla de configuración que se utilizará para registros nuevos de [!INCLUDE[d365fin](includes/d365fin_md.md)].  

3.  Establezca el campo **Código de plantilla de config. de tab. int.** en la plantilla de configuración que se utilizará para registros nuevos de [!INCLUDE[d365fin](includes/cds_long_md.md)].

## <a name="see-also"></a>Consulte también  
[Acerca de la integración de Dynamics 365 Business Central con [!INCLUDE[d365fin](includes/cds_long_md.md)]](admin-prepare-dynamics-365-for-sales-for-integration.md )   
[Sincronización de Business Central y [!INCLUDE[d365fin](includes/cds_long_md.md)]](admin-synchronizing-business-central-and-sales.md)   
[Programar una sincronización](admin-scheduled-synchronization-using-the-synchronization-job-queue-entries.md)  
