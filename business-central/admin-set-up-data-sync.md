---
title: Configurar empresas para sincronizar datos maestros
description: Aprenda a configurar una o más empresas para sincronizar datos maestros.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.service: dynamics-365-business-central
ms.topic: conceptual
ms.date: 05/07/2024
ms.custom: bap-template
ms.search.form: '7230, 7233, 5338, 7236, 672, 7234'
---

# Prepararse para sincronizar datos maestros

Cuando dos o más empresas utilizan algunos de los mismos datos maestros, puede sincronizar los datos en lugar de agregarlos manualmente en cada empresa. Por ejemplo, la sincronización de datos es particularmente útil cuando está configurando nuevas empresas filiales.

Los datos maestros incluyen configuraciones e información no transaccional sobre entidades comerciales. Por ejemplo, clientes, proveedores, artículos y empleados. Los datos proporcionan contexto para las transacciones comerciales. Los siguientes son algunos ejemplos de datos maestros para un cliente:

* Name
* Número de identificación
* Dirección
* Condiciones de pago
* Límite de crédito

Establezca la sincronización en las empresas filiales. Usando un modelo de extracción, las filiales extraen los datos de la empresa de origen que necesitan para hacer negocios con ellos. Después de configurar la sincronización y sincronizar los datos por primera vez, ya está todo listo. Los movimientos de cola de proyectos actualizan registros emparejados en las filiales cuando alguien cambia datos en la empresa de origen.

## Solo sincronización unidireccional

Puede sincronizar datos solo de la empresa de origen a las empresas filiales en forma de extracción. Las filiales no pueden enviar datos a la empresa de origen.

> [!NOTE]
> Aunque es posible, no recomendamos que configure la sincronización bidireccional. Es decir, sincronizar datos de la empresa de origen a las filiales y de las filiales a la empresa de origen. La sincronización de datos en ambas direcciones puede generar conflictos o sobrescrituras no deseadas.

## Antes de comenzar

Estos son los requisitos para configurar la sincronización.

* Todas las empresas deben estar en el mismo entorno.
* El usuario que configura la filial debe tener la licencia **Essential**, **Premium** o **Basic ISV**.

> [!NOTE]
> Las licencias de miembro del equipo o administrador interno le permiten acceder pero no modificar registros, por lo que no se pueden usar para configurar la sincronización. La licencia de administrador delegado no le permite programar tareas en segundo plano, por lo que no podrá completar la configuración.

## Especificar la empresa de origen

Los primeros pasos son especificar la empresa que será la fuente de datos y habilitar la sincronización. Las empresas filiales extraen datos de la empresa de origen.

> [!NOTE]
> Cuando habilita la sincronización, [!INCLUDE [prod_short](includes/prod_short.md)] crea y programa las entradas de la cola de trabajos que sincronizan los datos. Puede parecer que las entradas sincronizan inmediatamente los datos, pero ese no es el caso. Las entradas de la cola de trabajos creadas solo sincronizan registros acoplados y, en este momento, aún no lo ha configurado. La sincronización comienza después de que usted [Habilite o deshabilite tablas y campos](#enable-or-disable-tables-and-fields) y [Sincronice por primera vez](#synchronize-for-the-first-time).

1. En una empresa filial, elija el icono ![Bombilla que abre la característica Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Configuración de administración de datos maestros** y luego elija el vínculo relacionado.
1. En el campo **Empresa de origen**, especifique la empresa de la que extraerá los cambios.
1. Active la opción **Habilitar sincronización**.
1. En el cuadro de diálogo de confirmación, elija **Aceptar**. [!INCLUDE [prod_short](includes/prod_short.md)] encontrará las tablas y los campos que están disponibles en la empresa de origen.

El siguiente paso es habilitar tablas y campos para la sincronización.

## Habilitar o deshabilitar tablas y campos

Para ahorrar tiempo, [!INCLUDE [prod_short](includes/prod_short.md)] proporciona una lista de tablas que las empresas suelen sincronizar. De forma predeterminada, estas tablas están habilitadas para sincronización. Puede modificarlas, deshabilitarlas o eliminarlas como mejor le parezca. Para ahorrar tiempo, algunos campos de las tablas ya están deshabilitados, porque probablemente no sean relevantes para la filial.

> [!NOTE]
> Si una o más extensiones están instaladas en la empresa de origen, cuando una filial configura la sincronización, la página **Tablas de sincronización** incluye tablas de las extensiones y puede acceder a sus campos. Sin embargo, si la empresa de origen agrega una extensión después de configurar la sincronización, cada filial debe agregar las tablas manualmente. Para obtener más información sobre cómo agregar tablas, vaya a [Agregar o eliminar tablas de la lista de tablas de sincronización](#add-or-delete-tables-from-the-synchronization-tables-list). Para obtener más información sobre cómo extender [!INCLUDE [prod_short](includes/prod_short.md)], vaya a [Desarrollo de extensiones en Visual Studio Code](/dynamics365/business-central/dev-itpro/developer/devenv-dev-overview#developing-extensions-in-visual-studio-code).

1. Elija el icono ![Bombilla que abre la característica Dígame](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Configuración de administración de datos maestros** y luego elija el vínculo relacionado.
1. Seleccione la acción **Tablas de sincronización**.
1. Rellene los campos según sea necesario. [!INCLUDE [tooltip-inline-tip_md](../archive/SetupAndAdministration/includes/tooltip-inline-tip_md.md)]

> [!TIP]
> El campo **Filtro de tabla** es útil para controlar qué sincronizar para una tabla. Puede configurar filtros para sincronizar solo cuando se cumplan ciertas condiciones. Por ejemplo, puede agregar filtros que especifiquen que sincroniza solo proveedores en una determinada región. O bien, clientes que utilizan una determinada moneda.
>
> Si la filial ya tiene datos en sus tablas, otra buena manera de establecer criterios para la sincronización es configurar un emparejamiento basado en coincidencias. Para obtener más información sobre coincidencias, vaya a [Usar emparejamiento basado en coincidencias](#use-match-based-coupling).

1. Para habilitar campos para una tabla, elija la tabla y luego elija la acción **Campos**.
1. Rellene los campos según sea necesario. [!INCLUDE [tooltip-inline-tip_md](../archive/SetupAndAdministration/includes/tooltip-inline-tip_md.md)]

> [!TIP]
> Una forma rápida de habilitar o deshabilitar varios campos al mismo tiempo es seleccionarlos en la lista y luego usar las acciones **Habilitar** o **Deshabilitar**.

### Usar emparejamiento basado en coincidencias

Puede especificar los datos para sincronizar para una tabla haciendo coincidir los registros según criterios. En la página **Configuración de administración de datos maestros**, elija la acción **Emparejamiento basado en coincidencias** para abrir la página **Seleccionar criterios de emparejamiento**. Puede definir los siguientes criterios para su coincidencia:

* Si desea sincronizar después de emparejar registros.
* Si desea crear un nuevo registro en la empresa filial si se puede encontrar una coincidencia desemparejada única utilizando los criterios de coincidencia. Para activar esta capacidad, active la acción **Crear nuevo si no se encuentra una coincidencia**.
* Los campos que se utilizarán para hacer coincidir los registros y si la coincidencia distingue entre mayúsculas y minúsculas.
* Priorice el orden en el que se buscan los registros especificando un prioridad de coincidencia. [!INCLUDE [prod_short](includes/prod_short.md)] buscará una coincidencia en orden ascendente según la prioridad de coincidencia. Un valor en blanco es igual a la prioridad 0, que es la prioridad más alta. Los campos con la prioridad 0 se consideran en primer lugar.

## Sincronizar por primera vez

Cuando esté listo, en la página **Configuración de administración de datos maestros** , seleccione la acción **Iniciar sincronización inicial**. En la página **Sincronización inicial de datos maestros** elija el tipo de sincronización que desea usar para cada tabla.

* Si ya tiene registros tanto en la empresa de origen como en las filiales, y desea hacer coincidir los registros existentes, elija la acción **Usar emparejamiento basado en coincidencias**. [!INCLUDE [prod_short](includes/prod_short.md)] hace coincidir los registros de la empresa filial con los registros de la empresa de origen. Las coincidencias se basan en los criterios de coincidencia que defina. Para diversas tablas predeterminadas, [!INCLUDE [prod_short](includes/prod_short.md)] ya ha hecho coincidir los registros existentes mediante el uso de su clave principal, pero puede cambiar eso si lo desea. También puede permitir que la sincronización cree nuevos registros en la filial para registros en la empresa de origen que la filial no tiene. Para obtener más información sobre coincidencias, vaya a [Usar emparejamiento basado en coincidencias](#use-match-based-coupling).
* Si elige **Ejecutar sincronización completa**, la sincronización crea nuevos registros para todos los registros de la empresa de origen que aún no están emparejados. Por ejemplo, esta opción es útil en los siguientes escenarios:

    * La filial no tiene datos en la tabla.
    * Desea agregar registros de la empresa de origen sin coincidencias.  

Después de elegir la opción a usar, elija la acción **Iniciar todo** para iniciar la sincronización.

Mientras se ejecuta la sincronización, la columna **Estado del trabajo** de la página **Sincronización completa inicial de datos maestros** muestra el estado de cada entrada de la cola de trabajos. Presione **F5** en el teclado para actualizar el estado.

> [!TIP]
> Las tablas se sincronizan en un orden predefinido. Si la sincronización se atasca en una tabla, seleccione la tabla y luego elija la acción **Reiniciar** para que vuelva a funcionar.

Para acceder a detalles, como el número de registros que se insertan o modifican, elija el valor en la columna **Estado del trabajo** para abrir la página **Ver: trabajos de sincronización de integración**. Para los registros que se insertaron, puede elegir el número en la columna **Insertado** para acceder a más detalles sobre los nuevos registros.

## Agregar o eliminar tablas de la lista de tablas de sincronización

### Agregar una tabla

> [!IMPORTANT]
> Aunque las tablas que contienen datos transaccionales están disponibles en la lista, como las tablas que contienen entradas del libro mayor, no debe elegirlas. La sincronización solo funciona para tablas que contienen datos no transaccionales.

1. Elija el icono ![Bombilla que abre la característica Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Tablas de sincronización** y luego elija el vínculo relacionado.
1. Elija **Nueva** y, a continuación, elija la tabla a agregar.
1. Rellene los campos según sea necesario. [!INCLUDE [tooltip-inline-tip_md](../archive/SetupAndAdministration/includes/tooltip-inline-tip_md.md)]

### Eliminar una tabla

> [!NOTE]
> Si elimina un registro en la empresa de origen, no se elimina también en la filial. Esto ayuda a evitar la pérdida no deseada de datos. La filial puede decidir eliminar la tabla si lo desea.

1. Elija el icono ![Bombilla que abre la característica Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Tablas de sincronización** y luego elija el vínculo relacionado.
1. Elija la acción **Eliminar**.

## Use exportar e importar para compartir una configuración de sincronización

Si está configurando varias filiales que usan la misma configuración de sincronización o una similar, hay un ahorro de tiempo. Configure una empresa filial y luego exporte su configuración a un archivo .xml. El archivo contiene la configuración completa, incluidas las asignaciones de tablas y campos y los criterios de filtro. A continuación, puede importar el archivo a la siguiente filial. Para importar o exportar una configuración, en la página **Configuración de administración de datos maestros**, use las acciones **Importar** o **Exportar**.

## Consulte también

[Administrar la sincronización de datos maestros](admin-sync-master-data.md)