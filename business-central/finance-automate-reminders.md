---
title: Automatizar recordatorios en cobros
description: 'Ahorre tiempo en cobros al automatizar los procesos de creación, emisión y envío de recordatorios a los clientes.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: how-to
ms.search.keywords: 'collection, remindes'
ms.search.form: null
ms.date: 03/12/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# Automatizar recordatorios en cobros

Haga que sus cobros sean más efectivos al automatizar los procesos de creación, emisión y envío de recordatorios a sus clientes. La automatización puede reducir significativamente el tiempo que dedicará a los cobros, brindar una mejor descripción general del proceso y brindarle control total sobre cada paso.

En la página **Automatización de recordatorios**, usted define las acciones individuales (pasos). Puede combinar los pasos para crear, emitir y enviar recordatorios, o puede crear una automatización separada para cada paso si eso es mejor para sus procesos de cobro. Las automatizaciones se basan en términos y niveles de recordatorio. Para obtener más información, vaya a [Configurar términos y niveles de recordatorios](finance-setup-reminders.md). Puede configurar filtros para términos de recordatorio para una automatización en su conjunto y configurar filtros para cada acción en la automatización. También puede adjuntar facturas pendientes a correos electrónicos como archivos PDF.

La automatización se produce a través de una entrada en la cola de trabajos. Cuando configura una automatización, utilice el campo **Cadencia** para especificar cómo y cuándo se ejecuta. Si elige **Manual**, la automatización se ejecuta una vez cuando utiliza la acción **Iniciar**. También puede elegir **Semanal**, **Mensual** o elegir **Personalizado** para configurar una cadencia más detallada. Si elige **Personalizado**, debe introducir una fórmula de datos. Para obtener más información sobre cómo introducir una fórmula de fecha, vaya a [Usar fórmulas de fecha](ui-enter-date-ranges.md#use-date-formulas). Cuando elija una opción que no sea **Manual**, la automatización se ejecuta hasta que la pause para ponerla en espera. Si desea ser aún más específico acerca de cuándo se ejecuta, utilice la acción **Entradas de la cola de trabajos** para abrir la página **Entradas de la cola de trabajos** y ajuste la periodicidad, por ejemplo, a diario o a un día laborable específico.

## Automatizar el flujo de recordatorios

Las siguientes secciones describen cómo configurar recordatorios para crear, emitir y enviar automáticamente.

1. Elija el icono ![Bombilla que abre la característica Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), , escriba **Automatización de recordatorios** y luego elija el vínculo relacionado.
1. Elija **Nuevo** y, a continuación, rellene los campos de la ficha desplegable **General** como sea necesario.
1. En el campo **Filtro de términos de recordatorio**, elija el término o términos de recordatorio para usar esta automatización.
1. En el campo **Cadencia**, elija la frecuencia con la que se ejecuta la automatización.
1. En la pestaña desplegable **Acciones**, elija **Nuevo** y luego elija si la automatización crea, emite o envía recordatorios. Elija **Aceptar**.
1. Dependiendo del tipo de acción que realiza la automatización, complete los campos según sea necesario en la página de configuración. Para obtener más información sobre la configuración, vaya a [Configuración de acciones de recordatorio](#settings-for-reminder-actions).
1. Después de configurar las acciones para la automatización, puede usar las acciones **Mover hacia arriba** y **Mover hacia abajo** para ajustar el orden en que se ejecutan.

## Configuraciones para acciones de recordatorio

Las opciones de configuración difieren para las acciones Crear, Emitir y Enviar recordatorio. En el siguiente apartado se explica cómo usarlas.

### Crear

* Establezca el nivel máximo en todas las líneas de recordatorio.  
* Cree recordatorios para movimientos en espera. Por ejemplo, esta configuración es útil si tiene una disputa en curso con un cliente y desea que vea el panorama general.
* Cree recordatorios para todas las facturas impagadas y no solo para las vencidas. El informe muestra las facturas vencidas y aquellas que simplemente están impagadas pero no vencidas en secciones separadas.
* Configure filtros para que el recordatorio sea más específico.

### Emitir

Cuando emite un recordatorio, crea entradas en el libro mayor de clientes que contienen la fecha de contabilización y la fecha del impuesto. Utilice la configuración en la página **Configuración de recordatorios de problemas** para especificar si se reemplaza esa información en el recordatorio emitido con la información del recordatorio creado. Por ejemplo, si creó el recordatorio ayer y lo emite hoy, la fecha de vencimiento se mueve un día.

### Enviar

> [!NOTE]
> La automatización de envío requiere que haya configurado el correo electrónico en [!INCLUDE [prod_short](includes/prod_short.md)]. Para obtener más información sobre cómo configurar un correo electrónico, vaya a [Configurar correo electrónico](admin-how-setup-email.md).

El contenido de los correos electrónicos, como los textos adjuntos, los textos del cuerpo del correo electrónico y el idioma, provienen de la configuración del término de recordatorio. Para obtener más información sobre la configuración de correo electrónico, vaya a [Configurar términos y niveles de recordatorios](finance-setup-reminders.md).

Utilice la configuración de la página **Enviar configuración de recordatorios** para controlar lo siguiente:

* Configuraciones generales, como la descripción y cuántas veces envía el mismo recordatorio.
* Configuraciones sobre qué incluir en el recordatorio.
* Configuraciones para rastrear los recordatorios que envía mediante la creación de interacciones, ya sea que imprima o envíe el recordatorio por correo electrónico y si desea adjuntar solo facturas vencidas, todas las facturas o ninguna factura. 

## Obtener acceso al historial de un recordatorio

[!INCLUDE [prod_short](includes/prod_short.md)] realiza un seguimiento de cada vez que se ejecuta una automatización. Para tener acceso al historial elija la acción **Entradas de registro**. También puedes utilizar la acción **Recordatorios emitidos** para tener acceso a una lista de los recordatorios que ha emitido.

## Controlar los errores

En la ficha desplegable **Acciones** para cada acción puede especificar si desea que la automatización se detenga si la acción tiene un error. Si lo hace, la automatización no procesará las acciones que vienen después. Para activar o desactivar esta función, utilice las acciones **Establecer detención en caso de error** o **Borrar detención en caso de error**.

## Cambiar la configuración de acción para una automatización

Puede cambiar la configuración de una automatización en cualquier momento. En la ficha desplegable **Acciones**, elija **Configuración** y luego realice los cambios.

## Consulte también

[Configurar términos, niveles y textos de recordatorios](finance-setup-reminders.md)  
[Enviar recordatorios de saldos pendientes](receivables-send-reminders.md)  
