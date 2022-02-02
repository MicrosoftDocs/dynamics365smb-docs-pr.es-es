---
title: Limpiar datos con directivas de retención
description: Puede especificar la frecuencia con la que desea eliminar ciertos tipos de datos.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: delete, data, retention, policy, policies
ms.search.form: 3903, 3901
ms.date: 04/01/2021
ms.author: bholtorf
ms.openlocfilehash: ab16aacb7689287eac259658a8ef6bb355f04842
ms.sourcegitcommit: 8464b37c4f1e5819aed81d9cfdc382fc3d0762fc
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 01/19/2022
ms.locfileid: "8012398"
---
# <a name="define-retention-policies"></a>Definir directivas de retención
Los administradores pueden definir directivas de retención para especificar con qué frecuencia desean que [!INCLUDE[prod_short](includes/prod_short.md)] elimine datos desactualizados en tablas que contienen entradas de registro y registros archivados. Por ejemplo, limpiar las entradas de registro puede facilitar el trabajo con los datos que son realmente relevantes. Las directivas pueden incluir todos los datos de las tablas que superan la fecha de vencimiento, o puede agregar criterios de filtro que incluirán solo ciertos datos vencidos en la directiva. 

## <a name="required-setups-and-permissions"></a>Configuraciones y permisos necesarios
Antes de que pueda crear directivas de retención, debe configurar lo siguiente.

|Configurar  |Descripción  |
|---------|---------|
|**Tablas permitidas**     |Proporcionamos una lista de las tablas que se pueden incluir en las directivas de retención. Sin embargo, si desea agregar tablas desde una extensión a una directiva de retención, un desarrollador debe agregar sus tablas a la lista. Para más información, consulte [Incluir su extensión en una directiva de retención](admin-data-retention-policies.md#including-your-extension-in-a-retention-policy-requires-help-from-a-developer).          |
|**Períodos de retención**     |Especifique períodos de tiempo durante los cuales se conservarán los datos en las tablas de una directiva. Los períodos determinan la frecuencia con la que se eliminarán los datos.         |

Además, debe tener los permisos de usuario SUPER o el permiso de configuración de la directiva de retención establecida. Los usuarios a los que se les concede el conjunto de permisos Configuración de directivas de retención pueden definir directivas de retención para las tablas, incluso si no tienen permisos de lectura y eliminación para esas tablas. La entrada de la cola de trabajos debe ejecutarse como un usuario con permisos para leer y eliminar los datos. Se recomienda que no otorgue el conjunto de permisos de Configuración de la directiva de retención a los usuarios a los que no se les debería permitir eliminar datos.

> [!NOTE]
> Si esta usando [!INCLUDE[prod_short](includes/prod_short.md)] local, y desea probar las directivas de retención en la base de datos de demostración Cronus, hay algunas cosas que debe hacer. La empresa de demostración no contiene tablas que pueda usar con directivas de retención, por lo que debe agregarlas. Para ello, cree una nueva empresa en blanco en la base de datos de demostración. En la nueva empresa, importe el paquete de configuración RapidStart para su país que corresponda al paquete estándar NAV17.0.W1.ENU.STANDARD.rapidstart. Los datos de configuración de las directivas de retención estarán disponibles en la nueva empresa.

### <a name="to-create-retention-periods"></a>Para crear períodos de retención
Los períodos de retención pueden ser tan largos o cortos como desee. Para crear períodos de retención, en la página **Políticas de retención**, utilice la acción **Periodo de retención**. Los períodos que defina estarán disponibles para todas las pólizas.

> [!NOTE]
> Por razones de cumplimiento, hemos definido un período de retención mínimo para algunas tablas. Si establece un período de retención más corto que el mínimo requerido, un mensaje mostrará el período obligatorio.

### <a name="set-up-a-retention-policy"></a>Configurar una directiva retención
1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Directivas de retención** y elija el enlace relacionado.
2. En el campo **Id. de tabla**, seleccione la tabla que desee incluir en la directiva.
3. En el campo **Periodo de retención**, especifique el período de tiempo durante el cual se conservarán los datos en la tabla.
4. Opcional: para aplicar la directiva a datos específicos en una tabla, desactive la opción Aplicar a todos los registros. Aparecerá la Ficha desplegable Política de retención de registros, donde puede establecer filtros para crear subconjuntos de datos para cada línea. Para obtener más información, consulte [Filtrado](ui-enter-criteria-filters.md#filtering).

   > [!NOTE]
   > Cada línea tiene su propio período de retención. Si especifica diferentes períodos de retención para los mismos datos, se utilizará el período más largo. Además, algunas tablas contienen filtros que no puede cambiar ni eliminar. Para ayudarlo a identificar estos filtros, aparecen en una fuente de color más claro.

## <a name="applying-retention-policies"></a>Aplicación de directivas de retención
Puede utilizar una entrada de la cola de trabajos para aplicar directivas de retención para eliminar datos automáticamente, o puede aplicar directivas manualmente.

Para aplicar una directiva de retención automáticamente, simplemente cree y habilite una directiva. Cuando habilita una directiva, se crea una entrada en la cola de trabajos que aplicará directivas de retención de acuerdo con el período de retención que especifique. Todas las directivas de retención utilizarán la misma entrada de cola de trabajos. De forma predeterminada, la entrada de la cola de trabajos aplica la directiva todos los días a las 0200. Puede cambiar el valor predeterminado, pero si lo hace, le recomendamos la ejecución fuera del horario comercial. Para obtener más información, consulte [Uso de colas de proyectos para programar tareas](admin-job-queues-schedule-tasks.md). 

Puede aplicar manualmente una directiva mediante la acción **Aplicar manualmente** en la página **Políticas de retención**. Si desea aplicar siempre una directiva manualmente, active la alternancia **Manual**. La entrada de la cola de trabajos ignorará la directiva cuando se ejecute.

## <a name="viewing-retention-policy-log-entries"></a>Visualización de entradas de registro de directivas de retención
Puede ver la actividad relacionada con las directivas de retención en la página **Registro de directivas de retención**. Por ejemplo, las entradas se crean cuando se aplica una directiva o si ocurrieron errores cuando sucedió. 

## <a name="including-your-extension-in-a-retention-policy-requires-help-from-a-developer"></a>Incluir su extensión en una directiva de retención (requiere ayuda de un desarrollador)
De forma predeterminada, las directivas de retención cubren solo las tablas que están incluidas en la lista de tablas [!INCLUDE[prod_short](includes/prod_short.md)] que proporcionamos. Puede eliminar tablas predeterminadas de la lista y puede agregar tablas de su propiedad. Es decir, no puede agregar una tabla que no haya creado usted mismo. Por ejemplo, no puede agregar otras tablas desde [!INCLUDE[prod_short](includes/prod_short.md)] o desde una extensión que haya comprado.

Para agregar sus tablas a la lista de tablas permitidas, un desarrollador debe agregar algún código, por ejemplo, a la codeunit del instalador para la extensión (una codeunit con el subtipo *instalar*). 

Cuando un desarrollador agrega una tabla, puede especificar filtros obligatorios y predeterminados. Los filtros obligatorios no se pueden eliminar ni modificar más adelante cuando agrega tablas para definir una directiva de retención. Los filtros predeterminados son solo sugerencias cómodas.

Los siguientes son ejemplos de cómo agregar una tabla a la lista de tablas permitidas con y sin filtros obligatorios o predeterminados. Para obtener un ejemplo más complejo, consulte codeunit 3999 "Reten. Pol. Instalar - BaseApp". 

```al
 trigger OnInstallAppPerCompany()
    var
        RetenPolAllowedTables: Codeunit "Reten. Pol. Allowed Tables";
    begin
        RetenPolAllowedTables.AddAllowedTable(Database::"Retention Policy Log Entry");
    end;
```

El siguiente ejemplo incluye un filtro obligatorio.

```al
 trigger OnInstallAppPerCompany()
    var
        ChangeLogEntry: Record "Change Log Entry";
        RetenPolAllowedTables: Codeunit "Reten. Pol. Allowed Tables";
        RetentionPeriod: Enum "Retention Period Enum";
        RecRef: RecordRef;
        TableFilters: JsonArray;
        Enabled: Boolean;
        Mandatory: Boolean;
    begin
        ChangeLogEntry.Reset();
        ChangeLogEntry.SetFilter("Field Log Entry Feature", '%1|%2', ChangeLogEntry."Field Log Entry Feature"::"Monitor Sensitive Fields", ChangeLogEntry."Field Log Entry Feature"::All);
        RecRef.GetTable(ChangeLogEntry);
        Enabled := true;
        Mandatory := true;
        RetenPolAllowedTables.AddTableFilterToJsonArray(TableFilters, RetentionPeriod::"28 Days", ChangeLogEntry.FieldNo(SystemCreatedAt), Enabled, Mandatory, RecRef);
        RetenPolAllowedTables.AddAllowedTable(Database::"Change Log Entry", ChangeLogEntry.FieldNo(SystemCreatedAt), TableFilters);
    end;
```

Una vez que un desarrollador ha agregado tablas a la lista, un administrador puede incluirlas en una directiva de retención. 

## <a name="see-also"></a>Consulte también

[Análisis de la telemetría de seguimiento de la política de retención](/dynamics365/business-central/dev-itpro/administration/telemetry-retention-policy-trace)  
[Auditar cambios en Business Central](across-log-changes.md)  
[Filtrado](ui-enter-criteria-filters.md#filtering)  
[Uso de colas de proyectos para programar tareas](admin-job-queues-schedule-tasks.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]