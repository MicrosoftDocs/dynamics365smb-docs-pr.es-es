---
title: Ver el estado de los trabajos de sincronización (contiene vídeo)
description: Utilice la página Errores de sincronización de datos emparejados para ver el estado de los proyectos de sincronización que se han ejecutado para los registros emparejados en integraciones.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'sales, crm, integration, sync, synchronize'
ms.search.form: 6250
ms.date: 06/14/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
---

# Ver el estado de los proyectos de sincronización


Utilice la página **Errores de sincronización de datos emparejados** para ver el estado de los proyectos de sincronización que se han ejecutado para los registros emparejados en una integración de Dataverse o [!INCLUDE[crm_md](includes/crm_md.md)]. Esto incluye proyectos que se han ejecutado desde la cola de proyectos y proyectos manuales de sincronización que se han ejecutado en registros desde [!INCLUDE[prod_short](includes/prod_short.md)]. Por ejemplo, ver su estado es útil para la resolución de problemas, ya que le da acceso a los detalles sobre los errores relacionados con los registros emparejados. Normalmente, estos tipos de errores se deben a acciones del usuario, por ejemplo, cuando:  

* Dos personas han hecho un cambio en los mismos datos en ambas aplicaciones empresariales.
* Alguien ha eliminado datos de una de las aplicaciones, pero no de ambas.

> [!Note]
> La página **Errores de sincronización de datos emparejados** muestra información sobre los proyectos relacionados con los registros emparejados. Si resuelve todos los errores pero los registros siguen sin sincronizarse, es posible que tenga algo que ver con una configuración para la integración. Típicamente, su administrador necesitará resolver esos tipos de errores.   

## Ejemplo:
Este vídeo muestra un ejemplo de cómo solucionar errores que ocurrieron al sincronizar con [!INCLUDE[prod_short](includes/cds_long_md.md)]. El proceso será el mismo para todas las integraciones. 

> [!VIDEO https://go.microsoft.com/fwlink/?linkid=2097304]


## Para ver y resolver los errores de sincronización de los registros emparejados
1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Errores de sincronización de datos emparejados** y luego elija el enlace relacionado.
2. La página **Errores de sincronización de datos emparejados** muestra los problemas que se produjeron al sincronizar registros emparejados. La siguiente tabla incluye acciones que puede utilizar para resolver problemas uno por uno:

|Acción|Descripción|
|----|----|
|**Eliminar emparejamiento**|Desempareja los registros y ya no se sincronizarán. Para reanudar la sincronización, debe emparejarlos de nuevo. |
|**Reintentar** y **Reintentar todo**|Para cada registro en el que se encuentra un error, la sincronización se omite a menos que solucione el problema. Reintentar incluirá el registro seleccionado en la próxima sincronización y **Reintentar todo** incluirá todos los registros.|
|**Sincronizar**|La aplicación intentará resolver un conflicto en el que se haya cambiado datos en ambas aplicaciones empresariales. También puede elegir los datos que se usarán.|
|**Restaurar Registros** y **Eliminar registros**|Son útiles cuando se ha eliminado un registro en una de las aplicaciones empresariales. La opción Eliminar registros elimina el registro o fila en la aplicación donde aún existe. La restauración de registros recrea el registro o la fila en la aplicación empresarial donde se eliminó.|

> [!NOTE]
> Para reducir el número de conflictos que necesita resolver, puede configurar sus asignaciones de tablas de integración para aplicar estas acciones automáticamente. Para obtener más información, consulte [Asignación de tablas de integración](admin-how-to-modify-table-mappings-for-synchronization.md#mapping-integration-tables).

## Para ver el registro de sincronización de un registro específico (sincronizado manualmente)
1. Abrir, por ejemplo, un cliente, un producto o cualquier otro registro que esté sincronizando datos entre [!INCLUDE[prod_short](includes/prod_short.md)] y Dataverse o [!INCLUDE[crm_md](includes/crm_md.md)].
2. Seleccione la acción **Registro de sincronización** para ver el registro de sincronización de un registro seleccionado. Por ejemplo, un cliente específico que ha sincronizado manualmente.

## Eliminar acoplamientos entre registros
Cuando algo sale mal en su integración y necesita desacoplar registros para dejar de sincronizarlos, puede hacerlo para uno o más registros a la vez. Puede desacoplar uno o más registros de las páginas de lista o la página **Errores de sincronización de datos acoplados** eligiendo una o más líneas y eligiendo **Eliminar acoplamiento**. También puede eliminar todos los acoplamientos para una o más asignaciones de tabla en la página **Asignaciones de tablas de integración**. 

Si una entidad con un emparejamiento unidireccional se elimina en [!INCLUDE[prod_short](includes/prod_short.md)], debe eliminar manualmente el emparejamiento roto. Para hacer eso, en la página **Errores de sincronización de datos acoplados**, elija la acción **Buscar eliminado** y, a continuación, elimine los acoplamientos.

## Consulte también  
[Configuración de cuentas de usuario para la integración con Dynamics 365 Sales](admin-setting-up-integration-with-dynamics-sales.md)  
[Usar Dynamics 365 Sales desde Business Central](marketing-integrate-dynamicscrm.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]