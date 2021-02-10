---
title: Auditar cambios | Documentos de Microsoft
description: Puede activar el registro de usuario para tener un historial de los cambios realizados en los datos de las tablas de las que se hace el seguimiento. También puede realizar un seguimiento de actividades con ciertos tipos de registros de actividad.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: user log, user activity, tracking
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: bce5c61afd2a1119c25e37ece65081ef0519694e
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "4754347"
---
# <a name="auditing-changes-in-business-central"></a>Auditar cambios en Business Central
Un desafío común en muchas aplicaciones de gestión empresarial es evitar cambios no deseados en los datos. Podría ser cualquier cosa, desde un número de teléfono incorrecto de un cliente hasta un registro incorrecto en la contabilidad. Este tema describe las capacidades para averiguar qué cambió, quién lo cambió y cuándo se realizó el cambio.

## <a name="about-the-change-log"></a>Sobre el Registro de cambios 
El registro de cambios permite realizar un seguimiento de todas las modificaciones directas que realiza un usuario a los datos de la base de datos. Debe especificar para cada tabla y campo lo que desea que el sistema registre y, a continuación, debe activar el registro de cambios.  

El registro de cambios se basa en los cambios realizados en los datos en las tablas que se siguen. En la página **Cambiar entradas del registro**, las entradas se ordenan cronológicamente y se muestran todos los cambios realizados en los valores de los campos, de las tablas que especifique.

> [!Important]
> Los cambios se muestran en **Cambiar entradas de registro** solo después de reiniciar la sesión del usuario, lo que sucede de la siguiente manera:
<br />
> * La sesión ha caducado y se ha actualizado.
> * El usuario seleccionó otra empresa o área de trabajo.
> * El usuario ha salido y ha vuelto a entrar.

### <a name="working-with-the-change-log"></a>Trabajar con el registro de cambios
El registro de cambios se activa y desactiva en la página **Config. log cambio**. Si un usuario activa o desactiva el registro de cambios, se registra esta actividad, de modo que siempre puede ver qué usuario ha activado o reactivado el registro de cambios.

En la página **Config. log cambio**, si elige la acción **Tablas**, puede especificar de qué tablas que desea realizar el seguimiento de los cambios y de qué cambios desea efectuar el seguimiento. [!INCLUDE[prod_short](includes/prod_short.md)] también realiza el seguimiento de varias tablas del sistema.

> [!NOTE]
> Puede monitorear campos específicos para detectar cambios, como campos que contienen datos confidenciales, configurando el monitoreo de campos. Si lo hace, para evitar la redundancia, la tabla que contiene el campo no estará disponible para la configuración del registro de cambios. Para más información, consulte [Supervisión de campos confidenciales](across-log-changes.md#monitoring-sensitive-fields).

Después de haber configurado el registro de cambios, haberlo activado y alguien haya realizado un cambio en los datos, puede ver y filtrar los cambios en la página **Movs. registro cambios**. Si desea eliminar movimientos, puede hacerlo en la página **Eliminar movs. reg. de cambios**, donde puede definir filtros basados en fechas y horas.  

## <a name="about-activity-logs"></a>Acerca de los registros de actividad
Desde algunas páginas en [!INCLUDE [prod_short](includes/prod_short.md)], puede ver un registro de actividad que muestra el estado y los errores de los archivos que exporta o importa [!INCLUDE [prod_short](includes/prod_short.md)].  

### <a name="working-with-activity-logs"></a>Trabajar con registros de actividad
La información se muestra en la página **Registro de actividad**, según el contexto desde el que se abra. Por ejemplo, puede abrir la página desde las páginas **Configuración del servicio de intercambio de documentos**, **Documento entrante**, **Histórico de facturas de venta** e **Histórico de abonos de venta**. Puede vaciar la lista de entradas de registro o simplemente borrar la lista de entradas anteriores a siete días.  

## <a name="monitoring-sensitive-fields"></a>Supervisar campos confidenciales
Mantener los datos confidenciales seguros y privados es una preocupación fundamental para la mayoría de las empresas. Para agregar una capa de seguridad, puede monitorear campos importantes y recibir notificaciones por correo electrónico cuando alguien cambia un valor. Por ejemplo, es posible que desee recibir una notificación si alguien cambia el número IBAN de su empresa.

> [!NOTE]
> El envío de notificaciones por correo electrónico requiere que configure la función de correo electrónico en [!INCLUDE[prod_short](includes/prod_short.md)]. Para obtener más información, consulte [Configurar correo electrónico](admin-how-setup-email.md).

### <a name="setting-up-field-monitoring"></a>Configuración de supervisión de campos
Puede usar la guía de configuración asistida **Configurar el cambio de campo del monitor** para especificar los campos que desea supervisar en función de los criterios de filtrado, como la clasificación de confidencialidad de datos para los campos. Para obtener más información, consulte [Clasificación de confidencialidad de datos](admin-classifying-data-sensitivity.md). La guía también le permite especificar la persona que recibirá una notificación por correo electrónico cuando se produzca un cambio y la cuenta de correo electrónico que enviará la notificación por correo electrónico. Debe especificar tanto la notificación del usuario como la cuenta desde la que enviar la notificación. Una vez que termine la guía, puede administrar la configuración para el monitoreo de campo en la página **Configuración de monitoreo de campo**. 

Con el tiempo, la lista de entradas de la página **Entradas de registro de campos supervisados** crecerá. Para reducir la cantidad de entradas, puede crear una directiva de retención que eliminará las entradas después de un período de tiempo específico. Para obtener más información, consulte [Definir directivas de retención](admin-data-retention-policies.md).

Cuando configura el monitoreo de campo o cambia algo en la configuración, se crean entradas para sus cambios. Puede especificar si mostrar las entradas relacionadas con la configuración de monitoreo, mostrándolas u ocultándolas. 

Puede administrar la configuración para el monitoreo de campo, como enviar una notificación por correo electrónico o simplemente registrar el cambio, para cada campo de la página **Hoja de trabajo de campos monitoreados**. La página también es donde puede agregar o eliminar campos para monitorear.

> [!NOTE]
> Después de agregar uno o más campos y comenzar a monitorear, debe cerrar sesión en [!INCLUDE[prod_short](includes/prod_short.md)] e iniciar sesión nuevamente para aplicar su configuración.

### <a name="working-with-field-monitoring"></a>Trabajar con el monitoreo de campo

Las entradas para todos los valores modificados para los campos supervisados están disponibles en la página **Entradas de registro de campos supervisados**. Por ejemplo, las entradas contienen información como el campo para el que se cambió el valor, los valores originales y nuevos, quién hizo el cambio y cuándo lo hizo. Para investigar más a fondo un cambio, elija un valor para abrir la página donde se realizó. Para ver una lista de todas las entradas, elija **Entradas de cambio de campo**.

### <a name="viewing-field-monitoring-telemetry"></a>Ver la telemetría de monitoreo de campo 

Puede configurar [!INCLUDE[prod_short](includes/prod_short.md)] para enviar la actividad de seguimiento de campo a un recurso de Application Insights en Microsoft Azure. Luego, con Azure Monitor, crea informes y configura alertas sobre los datos recopilados. Para obtener más información, consulte los siguientes artículos en la ayuda para desarrolladores y profesionales de TI de [!INCLUDE[prod_short](includes/prod_short.md)]:

- [Supervisión y análisis de telemetría: habilitación de Application Insights](/dynamics365/business-central/dev-itpro/administration/telemetry-overview#enable)
- [Análisis de la telemetría de monitoreo de campo](/dynamics365/business-central/dev-itpro/administration/telemetry-field-monitoring-trace)

## <a name="defining-retention-policies"></a>Definición de directivas de retención

Puede crear directivas de retención para eliminar los datos innecesarios de los registros después de un período de tiempo que especifique. Por ejemplo, con el tiempo puede crecer el número de entradas en un registro. Al limpiar las entradas antiguas, puede hacer que sea más fácil centrarse en las entradas más recientes y, probablemente, más relevantes. Para obtener más información, consulte [Definir directivas de retención](admin-data-retention-policies.md).

## <a name="see-also"></a>Consulte también
[Cambiar la configuración básica](ui-change-basic-settings.md)  
[Ordenar, buscar y filtrar](ui-enter-criteria-filters.md)  
[Búsqueda de páginas e información con Dígame](ui-search.md)  
[Asignar permisos a usuarios y grupos](ui-define-granular-permissions.md)    
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Definir directivas de retención](admin-data-retention-policies.md)  