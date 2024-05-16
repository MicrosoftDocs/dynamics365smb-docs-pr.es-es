---
title: Auditar cambios
description: Puede activar el registro de usuario para tener un historial de los cambios realizados en los datos de las tablas de las que se hace el seguimiento. También puede realizar un seguimiento de actividades con ciertos tipos de registros de actividad.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'user log, user activity, tracking'
ms.search.form: '592, 593, 594, 595, 710, 1366, 1367, 1368, 1369'
ms.date: 05/03/2024
ms.custom: bap-template
ms.service: dynamics-365-business-central
---
# Auditar cambios

Un desafío común en muchas aplicaciones de gestión empresarial es evitar cambios no deseados en los datos. Podría ser cualquier cosa, desde un número de teléfono incorrecto de un cliente hasta un registro incorrecto en la contabilidad. Este artículo describe las capacidades para averiguar qué cambió, quién lo cambió y cuándo se realizó el cambio.

## Sobre el Registro de cambios

El registro de cambios permite realizar un seguimiento de todas las modificaciones directas que realiza un usuario a los datos de la base de datos. Especifique cada tabla y campo lo que desea que el sistema registre y, a continuación, active el registro de cambios. El registro de cambios se basa en los cambios realizados en los datos en las tablas que se siguen. En la página **Cambiar entradas del registro**, las entradas se ordenan cronológicamente y se muestran todos los cambios realizados en los valores de los campos, de las tablas que especifique.

El seguimiento de cambios puede afectar al rendimiento, lo que puede costarle tiempo, además de aumentar el tamaño de la base de datos, lo que podría costarle dinero. Para reducir esos costes, tenga en cuenta lo siguiente:

- Tenga cuidado al elegir las tablas y las operaciones.
- No agregue asientos contables ni documentos registrados. En su lugar, priorice los campos del sistema como Creado por y Fecha de creación.
- No utilice el tipo de seguimiento **Todos los campos**. En su lugar, elija **Algunos campos** y realice un seguimiento solo de los campos más importantes.

> [!NOTE]
> El Registro de cambios no realiza un seguimiento de los cambios de los campos que utilizan `autoIncrement property`. Un ejemplo de un campo que utiliza la propiedad es el campo Entero en las tablas Mensajes de error y Línea de informe de IVA.

También por motivos de rendimiento, el registro de cambios se desactiva durante el proceso de actualización de [!INCLUDE [prod_short](includes/prod_short.md)] a la próxima versión. Además de acelerar el proceso de actualización, la desactivación del registro también ayuda a reducir el desorden en el registro de oportunidades. Tan pronto como se completa la actualización, el registro comienza a rastrear los cambios nuevamente.

> [!Important]
> Los cambios se muestran en **Cambiar entradas de registro** solo después de reiniciar la sesión del usuario, lo que sucede de la siguiente manera:
>
> - La sesión ha caducado y se ha actualizado.
> - El usuario seleccionó otra empresa o área de trabajo.
> - El usuario ha cerrado sesión y ha vuelto a iniciar sesión.

## Configuración del registro de cambios

En la página **Cambiar configuración de registro** puede activar o desactivar el registro de cambios. Cuando lo hace, la actividad se registra, por lo que siempre podrá ver quién realizó el cambio.

En la página **Config. log cambio**, si elige la acción **Tablas**, puede especificar de qué tablas que desea realizar el seguimiento de los cambios y de qué cambios desea efectuar el seguimiento. [!INCLUDE[prod_short](includes/prod_short.md)] también realiza el seguimiento de varias tablas del sistema.

> [!NOTE]
> Puede monitorear campos específicos para detectar cambios, como campos que contienen datos confidenciales, configurando el monitoreo de campos. Si lo hace, para evitar la redundancia, la tabla que contiene el campo no estará disponible para la configuración del registro de cambios. Para más información, consulte [Supervisar campos confidenciales](across-log-changes.md#monitor-sensitive-fields).

Después de configurar el registro de cambios, haberlo activado y alguien haya realizado un cambio en los datos, puede ver y filtrar los cambios en la página **Movs. registro cambios**. Si desea eliminar entradas, configure una directiva de retención, donde puede establecer filtros basados ​​en fechas y horas. Para obtener más información sobre las directivas de retención en, consulte [Definir directivas de retención](admin-data-retention-policies.md).  

## Analizar datos en el registro de cambios

Puede utilizar la función **Análisis de datos** para analizar datos en el Registro de cambios desde la página [Entradas del registro de cambios](https://businesscentral.dynamics.com/?page=595). No es necesario ejecutar un informe ni abrir otra aplicación, como Excel. La característica proporciona una forma interactiva y versátil de calcular, resumir y examinar datos. En lugar de ejecutar informes con opciones y filtros, puede agregar varias pestañas que representen diferentes tareas o vistas de los datos. Algunos ejemplos son "Quién cambió qué datos y cuándo" o "Los datos cambian por tabla/campo" o cualquier otra vista que pueda imaginar. Para obtener más información sobre cómo utilizar la característica **Análisis de datos**, vaya a [Analizar datos de lista y consulta con el modo de análisis](analysis-mode.md).

### Escenarios de análisis ad hoc del registro de cambios

Las siguientes secciones proporcionan ejemplos de escenarios en los que el análisis del registro de cambios puede ayudarle a supervisar y auditar cambios importantes.

| Área | Para... | Abrir esta página en de análisis | Uso de estos campos |
| ---- | ----- | ------------------------------- |------------------- |
| [¿Quién ha cambiado qué datos y cuándo?](#example-who-changed-what-data-and-when) | Vea quién ha cambiado qué datos. | [Cambiar entradas del registro](https://businesscentral.dynamics.com/?page=595) | **ID de usuario**, **Fecha y hora**, **Título de tabla**, **Título de campo**, **Valor de clave principal 2**, **Valor de clave principal 3**, **Tipo de cambio**, **Valor anterior** y **Nuevo valor**. |
| [Cambios de datos por tabla/campo](#example-data-changes-by-tablefield) | Vea los cambios de datos por tabla/campo y quién realizó el cambio. | [Cambiar entradas del registro](https://businesscentral.dynamics.com/?page=595) | **Título de tabla**, **Título campo**, **Título de tabla**, **Título de campo**, **Valor de clave principal 2**, **Valor de clave principal 3**, **Tipo de cambio**, **Valor anterior** y **Nuevo valor**. |

### Ejemplo: Quién ha cambiado qué datos y cuándo

Para analizar Quién ha cambiado qué datos y cuándo, siga estos pasos:

1. Abra la lista [Cambiar entradas de registro](https://businesscentral.dynamics.com/?page=595) y elija :::image type="content" source="media/analysis-mode-icon.png" alt-text="Entrar en el modo de análisis."::: icono para activar el modo de análisis.
1. En el menú **Columnas**, elimine todas las columnas (seleccione la casilla junto al campo **Buscar** a la derecha).
1. Arrastre el campo **ID de usuario** (quién lo hizo) al área **Grupos de filas**.
1. Ahora elija los siguientes campos:
   - Para mostrar cuándo sucedió, elija **Fecha y hora**.
   - Para mostrar la tabla donde sucedió, elija **Título de la tabla**. 
   - Para mostrar qué campo, elija **Título de campo**.
   - Para mostrar el código de campo, elija **Valor de clave principal 2**. 
   - Para mostrar el nombre de la empresa, elija **Valor de clave principal 3**.
   - Para mostrar si el cambio fue una acción de inserción, actualización o eliminación, elija **Tipo de cambio**.
   - Para mostrar el cambio, elija **Valor antiguo** y **Valor nuevo**.
1. Cambie el nombre de su pestaña de análisis a **Quién ha cambiado qué datos y cuándo** o algo que describa este análisis.

La siguiente imagen muestra el resultado de estos pasos.

:::image type="content" source=" media/data-analysis-change-log-entries-Who-changed-What-data-When.png" alt-text="Ejemplo de cómo realizar un análisis de datos en la página Entradas del registro de cambios (Quién ha cambiado qué datos y cuándo)." lightbox="media/data-analysis-change-log-entries-Who-changed-What-data-When.png":::

### Ejemplo: cambios de datos por tabla/campo

Para analizar los cambios de datos por tabla/campo, siga estos pasos:

1. Abra la lista [Cambiar entradas de registro](https://businesscentral.dynamics.com/?page=595) y elija :::image type="content" source="media/analysis-mode-icon.png" alt-text="Entrar en el modo de análisis."::: icono para activar el modo de análisis.
1. En el menú **Columnas**, elimine todas las columnas (seleccione la casilla junto al campo **Buscar** a la derecha).
1. Arrastre el **Título de la tabla** (en qué mesa) y **Título de campo** (en qué campo) campos al área **Grupos de filas**.
1. Ahora elija los siguientes campos:
   - Para mostrar cuándo sucedió, elija **Fecha y hora**
   - Para mostrar quién realizó el cambio, elija **ID de usuario**.
   - Para mostrar el código para el campo, elija **Valor de clave principal 2**.
   - Para mostrar el nombre de la empresa, elija **Valor de clave principal 3** (normalmente el nombre de la empresa). 
   - Para mostrar si el cambio fue una acción de inserción, actualización o eliminación, elija **Tipo de cambio**.
   - Para mostrar el cambio, elija **Valor antiguo** y **Valor nuevo**.
1. Cambie el nombre de su pestaña de análisis a **Cambios de datos por tabla + campo** o algo que describa este análisis.

La siguiente imagen muestra el resultado de estos pasos.

:::image type="content" source=" media/data-analysis-change-log-entries-data-changes-by-table-field.png" alt-text="Ejemplo de cómo realizar un análisis de datos en la página Entradas del registro de cambios (cambios de datos por tabla/campo)." lightbox="media/data-analysis-change-log-entries-data-changes-by-table-field.png":::

## Acerca de los registros de actividad

Desde algunas páginas en [!INCLUDE [prod_short](includes/prod_short.md)], puede ver un registro de actividad que muestra el estado y los errores de los archivos que exporta o importa [!INCLUDE [prod_short](includes/prod_short.md)].  

### Trabajar con registros de actividad

La información se muestra en la página **Registro de actividad**, según el contexto desde el que se abra. Por ejemplo, puede abrir la página desde las páginas **Configuración del servicio de intercambio de documentos**, **Documento entrante**, **Histórico de facturas de venta** e **Histórico de abonos de venta**. Puede vaciar la lista de entradas de registro o simplemente borrar la lista de entradas anteriores a siete días.  

## Supervisar campos confidenciales

Mantener los datos confidenciales seguros y privados es una preocupación fundamental para la mayoría de las empresas. Para agregar una capa de seguridad, puede monitorear campos importantes y recibir un correo electrónico cuando alguien cambia un valor. Por ejemplo, es posible que desee recibir una notificación si alguien cambia el número IBAN de su empresa.

> [!NOTE]
> El envío de notificaciones por correo electrónico requiere que configure la función de correo electrónico en [!INCLUDE[prod_short](includes/prod_short.md)]. Para obtener más información, consulte [Configurar correo electrónico](admin-how-setup-email.md).

### Configurar supervisión de campos

Puede usar la guía de configuración asistida **Configurar el cambio de campo del monitor** para especificar los campos que desea supervisar en función de los criterios de filtrado, como la clasificación de confidencialidad de datos para los campos. Para obtener más información, consulte [Clasificación de confidencialidad de datos](admin-classifying-data-sensitivity.md). La guía también le permite especificar la persona que recibirá una notificación por correo electrónico cuando se produzca un cambio y la cuenta de correo electrónico que enviará la notificación por correo electrónico. Especifique tanto la notificación del usuario como la cuenta desde la que enviar la notificación. Una vez que termine la guía, puede administrar la configuración para el monitoreo de campo en la página **Configuración de monitoreo de campo**.

> [!NOTE]
> Cuando especifica la cuenta de correo electrónico desde la cual enviar notificaciones, debe agregar los tipos de cuenta **Microsoft 365** o **SMTP**. Las notificaciones deben enviarse desde una cuenta que no esté asociada con un usuario real. Por lo tanto, no puede elegir el tipo de usuario **Usuario actual**. Si lo hace, no se enviarán notificaciones.

Con el tiempo, la lista de entradas de la página **Entradas de registro de campos supervisados** crecerá. Para reducir la cantidad de entradas, puede crear una directiva de retención que eliminará las entradas después de un período de tiempo específico. Para obtener más información, consulte [Definir directivas de retención](admin-data-retention-policies.md).

Cuando configura el monitoreo de campo o cambia algo en la configuración, se crean entradas para sus cambios. Puede especificar si mostrar las entradas relacionadas con la configuración de monitoreo, mostrándolas u ocultándolas.

Puede administrar la configuración para el monitoreo de campo, como enviar una notificación por correo electrónico o simplemente registrar el cambio, para cada campo de la página **Hoja de trabajo de campos monitoreados**. La página también es donde puede agregar o eliminar campos para monitorear.

> [!NOTE]
> Después de agregar uno o más campos y comenzar a monitorear, debe cerrar sesión en [!INCLUDE[prod_short](includes/prod_short.md)] e iniciar sesión nuevamente para aplicar su configuración.

### Trabajar con la supervisión de campos

Las entradas para todos los valores modificados para los campos supervisados están disponibles en la página **Entradas de registro de campos supervisados**. Por ejemplo, las entradas contienen la siguiente información:

- El campo en el que se cambió el valor.
- Los valores originales y nuevos.
- Quién hizo el cambio y cuándo lo hizo.

Para investigar más a fondo un cambio, elija un valor para abrir la página donde se realizó. Para ver una lista de todas las entradas, elija **Entradas de cambio de campo**.

### Ver la telemetría de supervisar de campo

Puede configurar [!INCLUDE[prod_short](includes/prod_short.md)] para enviar la actividad de seguimiento de campo a un recurso de Application Insights en Microsoft Azure. Luego, con Azure Monitor, crea informes y configura alertas sobre los datos recopilados. Para obtener más información, consulte los siguientes artículos en la ayuda para desarrolladores y profesionales de TI de [!INCLUDE[prod_short](includes/prod_short.md)]:

- [Supervisión y análisis de telemetría: habilitación de Application Insights](/dynamics365/business-central/dev-itpro/administration/telemetry-overview?toc=/dynamics365/business-central/toc.json#enable)
- [Análisis de la telemetría de monitoreo de campo](/dynamics365/business-central/dev-itpro/administration/telemetry-field-monitoring-trace?toc=/dynamics365/business-central/toc.json)

## Definir directivas de retención

Puede crear directivas de retención para eliminar los datos innecesarios de los registros después de un período de tiempo que especifique. Por ejemplo, con el tiempo puede crecer el número de entradas en un registro. Al limpiar las entradas antiguas, puede hacer que sea más fácil centrarse en las entradas más recientes y, probablemente, más relevantes. Para obtener más información sobre las directivas de retención en, consulte [Definir directivas de retención](admin-data-retention-policies.md).

## Consulte también

[Supervisar campos confidenciales](across-log-changes.md#monitor-sensitive-fields)  
[Análisis de la telemetría de monitoreo de campo](/dynamics365/business-central/dev-itpro/administration/telemetry-field-monitoring-trace?toc=/dynamics365/business-central/toc.json)  
[Definir directivas de retención](admin-data-retention-policies.md)  
[Cambiar la configuración básica](ui-change-basic-settings.md)  
[Ordenar, buscar y filtrar](ui-enter-criteria-filters.md)  
[Búsqueda de páginas e información con Dígame](ui-search.md)  
[Asignar permisos a usuarios y grupos](ui-define-granular-permissions.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
