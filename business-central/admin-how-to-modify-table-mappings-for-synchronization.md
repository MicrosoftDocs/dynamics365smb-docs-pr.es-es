---
title: Modificar las asignaciones de tablas para la sincronización | Documentos de Microsoft
description: Obtenga información sobre cómo cambiar las asignaciones de tablas que se utilizan al sincronizar datos entre Business Central y Dynamics 365 Sales.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: sales, crm, integration, sync, synchronize, table mapping
ms.date: 10/01/2019
ms.author: bholtorf
ms.openlocfilehash: 505c1427c63a0a6f9e68980ea0ff05c93918ea60
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/01/2019
ms.locfileid: "2308082"
---
# <a name="modify-table-mappings-for-synchronization"></a>Modificar asignaciones de tablas para la sincronización
Una asignación de tabla de integración vincula una tabla en [!INCLUDE[d365fin](includes/d365fin_md.md)] con una tabla de integración para la entidad de [!INCLUDE[crm_md](includes/crm_md.md)]. Para cada entidad de [!INCLUDE[crm_md](includes/crm_md.md)] que desee sincronizar con los datos correspondientes de [!INCLUDE[d365fin](includes/d365fin_md.md)]], debe existir una asignación de tabla de integración correspondiente. Una asignación de tabla de integración incluye varias configuraciones que le permiten controlar cómo se sincronizan los registros de una tabla de [!INCLUDE[d365fin](includes/d365fin_md.md)] y una entidad de [!INCLUDE[crm_md](includes/crm_md.md)] mediante los proyectos de sincronización de integración correspondientes.  

## <a name="filtering-records"></a>Filtrar registros  
 Si no desea sincronizar todos los registros para una entidad de [!INCLUDE[crm_md](includes/crm_md.md)] o una tabla de [!INCLUDE[d365fin](includes/d365fin_md.md)] concreta, puede configurar filtros para limitar los registros que se sincronizan. Los filtros se configuran en la página **Lista de asignaciones de tablas de integración**.  

#### <a name="to-filter-records-for-synchronization"></a>Para filtrar registros para la sincronización  
1. Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Lista de asignaciones de tablas de integración** y luego elija el enlace relacionado.

2.  Para filtrar los registros de [!INCLUDE[d365fin](includes/d365fin_md.md)], establezca el campo **Filtro de tabla**.  

3.  Para filtrar los registros de [!INCLUDE[crm_md](includes/crm_md.md)], establezca el campo **Filtro de tabla de integración**.  

## <a name="creating-new-records"></a>Crear registros nuevos  
 De manera predeterminada, solo los registros de [!INCLUDE[d365fin](includes/d365fin_md.md)] y [!INCLUDE[crm_md](includes/crm_md.md)] que están emparejados se sincronizarán mediante proyectos de sincronización de integración. Puede configurar asignaciones de tabla de manera que se creen nuevos registros en el destino (por ejemplo, [!INCLUDE[d365fin](includes/d365fin_md.md)]) para cada registro del origen (por ejemplo, [!INCLUDE[crm_md](includes/crm_md.md)]) que aún no está emparejado.  

 Por ejemplo, el proyecto de sincronización de Dynamics 365 Sales VENDEDORES usa la asignación de tabla VENDEDORES. El proyecto de sincronización copia los datos de los registros del usuario de [!INCLUDE[crm_md](includes/crm_md.md)] en los registros de vendedores de [!INCLUDE[d365fin](includes/d365fin_md.md)]. Si configura la asignación de tabla para crear registros nuevos, para cada usuario de [!INCLUDE[crm_md](includes/crm_md.md)] que aún no está acoplado a un vendedor de [!INCLUDE[d365fin](includes/d365fin_md.md)], se crea un registro de vendedor en [!INCLUDE[d365fin](includes/d365fin_md.md)].  

#### <a name="to-create-new-records-during-synchronization"></a>Para crear registros nuevos durante la sincronización  
1. Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Lista de asignaciones de tablas de integración** y luego elija el enlace relacionado.

2.  En el movimiento de asignación de tabla de la lista, borre el campo **Sincronizar solo reg. emparejados**.  

## <a name="using-configuration-templates-on-table-mappings"></a>Uso de plantillas de configuración en asignaciones de tabla
Puede asignar plantillas de configuración a asignaciones de tabla para utilizarlas para registros nuevos que se crean en [!INCLUDE[d365fin](includes/d365fin_md.md)] o [!INCLUDE[crm_md](includes/crm_md.md)]. Para cada asignación de tabla, puede especificar una plantilla de configuración para utilizarla para los registros nuevos de [!INCLUDE[d365fin](includes/d365fin_md.md)] y otra plantilla para utilizar registros nuevos de [!INCLUDE[crm_md](includes/crm_md.md)].  

Si instala la configuración de sincronización predeterminada, la mayoría de las veces, se crearán automáticamente dos plantillas de configuración que se utilizarán en la asignación de tabla para clientes de [!INCLUDE[d365fin](includes/d365fin_md.md)] y cuentas de [!INCLUDE[crm_md](includes/crm_md.md)]: **CRMCUST** y **CRMACCOUNT**.  

-   **CRMCUST** se utiliza para crear y sincronizar clientes nuevos de [!INCLUDE[d365fin](includes/d365fin_md.md)] basándose en una cuenta de [!INCLUDE[crm_md](includes/crm_md.md)].  

     Esta plantilla se crea copiando una plantilla de configuración existente para clientes de la aplicación. **CRMCUST** solo se crea si hay una plantilla de configuración existente y el campo **Código de divisa** de la plantilla está en blanco. Si un campo de la plantilla de la configuración contiene un valor, el valor se utilizará en lugar del valor del campo asignado para la cuenta de [!INCLUDE[crm_md](includes/crm_md.md)]. Por ejemplo, si el campo **País/región** de una cuenta de [!INCLUDE[crm_md](includes/crm_md.md)] contiene *EE. UU.* y el campo **País/región** de la plantilla de configuración es *ES*, *ES* se utiliza como **País/región** para el cliente en [!INCLUDE[d365fin](includes/d365fin_md.md)].  

-   **CRMACCOUNT** crea y sincroniza cuentas nuevas de [!INCLUDE[crm_md](includes/crm_md.md)] basándose en una cuenta de [!INCLUDE[d365fin](includes/d365fin_md.md)].  

#### <a name="to-specify-configuration-templates-on-a-table-mapping"></a>Para especificar plantillas de configuración en una asignación de tabla  
1. Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Lista de asignaciones de tablas de integración** y luego elija el enlace relacionado.

2.  En el movimiento de asignación de tabla de la lista, en el campo **Código de plantilla de config. de tabla**, elija la plantilla de configuración que se utilizará para registros nuevos de [!INCLUDE[d365fin](includes/d365fin_md.md)].  

3.  Establezca el campo **Código de plantilla de config. de tab. int.** en la plantilla de configuración que se utilizará para registros nuevos de [!INCLUDE[crm_md](includes/crm_md.md)].

## <a name="see-also"></a>Consulte también  
[Acerca de la integración de Dynamics 365 Business Central con Dynamics 365 Sales](admin-prepare-dynamics-365-for-sales-for-integration.md )   
[Sincronización de Business Central y Dynamics 365 Sales](admin-synchronizing-business-central-and-sales.md)   
[Programar una sincronización](admin-scheduled-synchronization-using-the-synchronization-job-queue-entries.md)  
