---
title: 'Configurar términos, niveles y textos de recordatorios.'
description: Configure Business Central para poder enviar recordatorios sobre los pagos vencidos y agregar cargos o tarifas debido al retraso.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'payment due, debt, overdue, fee, charge, reminder'
ms.search.form: '431, 432, 436, 478'
ms.date: 03/12/2024
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# <a name="set-up-reminder-terms-and-levels"></a>Configurar términos, niveles y textos de recordatorios

Puede usar recordatorios para informar a los clientes de que tienen importes vencidos y solicitar pagos. [!INCLUDE [reminder-terms](includes/reminder-terms.md)]

> [!TIP]
> Después de configurar los términos y niveles de recordatorios, puede incluirlos en procesos automatizados para crear, emitir y enviar recordatorios. Para obtener más información sobre el proceso automatizado, vaya a [Automatizar recordatorios en cobros](finance-automate-reminders.md).

## <a name="reminder-terms"></a>Términos de recordatorio

Si los clientes tienen pagos vencidos, deberá decidir cómo y cuándo les enviará un recordatorio. Además, puede cargar en sus cuentas intereses o comisiones. Puede configurar un número ilimitado de recordatorios.  

> [!NOTE]
> Si desea calcular intereses sobre pagos vencidos, puede hacerlo al crear recordatorios. Sin embargo, si sólo desea calcular intereses e informar a sus clientes acerca de esto sin enviar recordatorios, use [documentos de interés](finance-setup-finance-charges.md). Para más información, vea [Recordatorios](receivables-collect-outstanding-balances.md#reminders) o [Cargos financieros](receivables-collect-outstanding-balances.md#finance-charges).

### <a name="set-up-attachment-and-email-body-texts-for-communications"></a>Configurar archivos adjuntos y textos del cuerpo del correo electrónico para comunicaciones

En la página **Configuración de términos de recordatorio**, puede configurar textos adjuntos y mensajes de correo electrónico estándar para usarlos en todos los niveles de recordatorio o crear mensajes específicos para cada nivel. Por ejemplo, el mensaje que envía para el primer nivel de recordatorio puede tener un tono o contenido diferente al del segundo o tercer nivel. Para crear archivos adjuntos y textos de mensajes de correo electrónico para todos los niveles, elija **Comunicación con el cliente** en la parte superior de la página. Para crear mensajes para líneas específicas, en la ficha desplegable **Nivel de recordatorio** , elija una línea y luego elija la acción **Comunicación con el cliente** en la ficha desplegable.

De forma predeterminada, los textos adjuntos y de correo electrónico utilizan su configuración de idioma. Sin embargo, si envía recordatorios a clientes de otros países o regiones, es posible que desee comunicarse en diferentes idiomas. Puedes crear textos para cada idioma que [!INCLUDE [prod_short](includes/prod_short.md)] admite usando la acción **Agregar texto para idioma**. Si lo hace, asegúrese de que los idiomas sean los mismos para los textos adjuntos y los textos de correo electrónico. Si no coinciden y el término del recordatorio tiene más de un nivel, es posible que la automatización no pueda personalizar el mensaje para uno o más niveles. Para verificar que los idiomas coincidan, utilice la acción **Resumen de comunicaciones** y compare las comunicaciones de los textos.

Cuando envía un correo electrónico, el recordatorio es un informe que adjunta al correo electrónico. Usted define el informe que genera el recordatorio en la página **Recordatorio de selección de informe/cargo financiero** , donde también selecciona el informe que contiene el texto del cuerpo del correo electrónico en el campo **Nombre del diseño del cuerpo del correo electrónico**. Cuando envía correos electrónicos a sus clientes, los textos de la ficha desplegable **Texto del correo electrónico** se insertan en el informe seleccionado en el campo **Nombre del diseño del cuerpo del correo electrónico**. El informe estándar tiene un campo de texto para este texto. Si lo desea, puede editar este informe, por ejemplo, para agregar o eliminar contenido. Edite el diseño de estos informes en la página **Diseños de informes**. Para obtener más información sobre los diseños de informes, vaya a [Comenzar a crear diseños de informes](ui-get-started-layouts.md).

> [!NOTE]
> Comunicarse por correo electrónico directamente desde [!INCLUDE [prod_short](includes/prod_short.md)] requiere que esté configurado para hacerlo. Para obtener más información sobre cómo conectar cuentas de correo electrónico con [!INCLUDE [prod_short](includes/prod_short.md)], vaya a [Configurar correo electrónico](admin-how-setup-email.md).

### <a name="set-up-reminder-terms"></a>Configurar los recordatorios

1. Elija el icono ![Bombilla que abre la característica Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), , escriba **Términos de recordatorios** y luego elija el enlace relacionado.  
2. Rellene los campos según sea necesario. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]  
3. Para utilizar más de una combinación de recordatorios, configure un código para cada uno.

## <a name="reminder-levels"></a>Niveles de recordatorio

Para cada término de recordatorio, puede definir un número ilimitado de niveles de recordatorio, aunque la mayoría de las empresas utilizan sólo dos o tres niveles. La primera vez que se crear un recordatorio para un cliente, se utiliza la configuración del nivel 1. Cuando se emite el recordatorio, el número de nivel se registra en los movimientos de recordatorio creados y vinculados a los movimientos del cliente individuales. Si es necesario volver a recordar al cliente, se comprueban todos los movimientos de recordatorio vinculados a movimientos de cliente abiertos para localizar el número de nivel más alto. Para el nuevo recordatorio se utilizarán las condiciones del siguiente número de nivel.

Si crea más recordatorios de aquellos para los define niveles, se utilizarán las condiciones para el nivel más alto. Puede crear tantos recordatorios como permita el campo **Nº máx. recordatorios** en los términos de recordatorio.

### <a name="to-set-up-reminder-levels"></a>Para configurar los niveles de recordatorio

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Términos de recordatorios** y luego elija el enlace relacionado.  
2. En la página **Términos recordatorio**, seleccione la línea que incluya los términos para los que desea configurar niveles y, a continuación, elija la acción **Niveles**.  
3. Rellene los campos según sea necesario. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]  

    > [!TIP]
    > El escenario del campo **Calcular interés** determina si el interés aparecerá en el recordatorio cuando se emita el recordatorio. Sin embargo, el campo **Publicar interés** de la página **Términos de recordatorio** determina si el interés calculado debe contabilizarse en el mayor y en las cuentas de los clientes.
    >
    > Para indicar que se debe calcular el interés, elija el campo **Calcular interés**.

    Opcionalmente, para cada nivel de recordatorio, especifique las tasas adicionales tanto en moneda local como extranjera. Puede definir muchos recargos adicionales en divisas extranjeras para cada código de la página **Niveles recordatorio**.  

    Las tarifas adicionales se pueden calcular de tres formas diferentes que se definen por el valor del campo **Añadir tipo de cálculo de tarifa**.  

    - **Fijo**

        Las tarifas se calculan en base a los valores de los campos **Cuota adicional** en la línea para el nivel de recordatorio en sí.  
    - **Dinámico único**

        Las tarifas se calculan en base a los valores de los campos de la línea correspondiente de la página **Configuración de cuota adicional** para ese nivel de recordatorio.
    - **Dinámica acumulada**

        Las tarifas se calculan en base a los valores de los campos las líneas combinadas de la página **Configuración de cuota adicional** para ese nivel de recordatorio.

4. Seleccione la acción **Divisas**.
5. En la página **Divisas por nivel recordatorio**, defina para cada código de nivel de recordatorio y su correspondiente número de nivel de recordatorio un código de divisa y un recargo adicional.

    > [!NOTE]  
    > Cuando crea recordatorios en una divisa extranjera, se utilizarán las condiciones de la divisa extranjera configuradas en esta tabla para crear recordatorios. Si no se han configurado recordatorios en divisa extranjera, se utilizarán los recordatorios de DL configurados en la página **Niveles recordatorio** y se convertirán en la divisa pertinente.

    Para cada nivel de recordatorio, puede especificar el texto que se va a imprimir antes (**Comienzo texto**) o después (**Fin texto**) en las entradas del recordatorio.

6. Elija las acciones **Comienzo texto** o **Fin texto** respectivamente, y rellene la página **Texto recordatorio**.
7. Para insertar automáticamente valores relacionados en el texto de recordatorio, puede introducir los siguientes marcadores de posición en el campo **Texto**.  

    |Marcador de posición|Valor|  
    |-----------------|-----------|  
    |%1|Contenido del campo **Fecha emisión documento** en la cabecera del recordatorio|  
    |%2|Contenido del campo **Fecha de vencimiento** en la cabecera del recordatorio|  
    |%3|Contenido del campo **Tipo interés** en las condiciones relacionadas con las cargas financieras|  
    |%4|Contenido del campo **Importe pendiente** en la cabecera del recordatorio|  
    |%5|Contenido del campo **Importe interés** en la cabecera del recordatorio|  
    |%6|Contenido del campo **Tarifa adicional** en la cabecera del recordatorio|  
    |%7|Importe total del recordatorio.|  
    |%8|Contenido del campo **Nivel recordatorio** en la cabecera del recordatorio|  
    |%9|Contenido del campo **Código divisa** en la cabecera del recordatorio|  
    |%10|Contenido del campo **Fecha registro** en la cabecera del recordatorio|  
    |%11|El nombre de la empresa|  
    |%12|Contenido del campo **Recargo adicional por línea** en la cabecera del recordatorio|  

    Por ejemplo, si escribe **Tiene una deuda de %9 %7 vencida desde el %2.**, el recordatorio contendrá el siguiente texto: **Tiene una deuda de 1200,50 USD vencida desde el 02-02-2024**.

    > [!NOTE]
    > [!INCLUDE [prod_short](includes/prod_short.md)] calcula la fecha de vencimiento se calcula según la fórmula de fecha que introduzca. Para obtener más información, vea [Usar fórmulas de fecha](ui-enter-date-ranges.md#use-date-formulas).

8. Para especificar el idioma de un mensaje de correo electrónico, elija la acción **Agregar texto para idioma**. El campo **Código de idioma** se actualiza para mostrar su selección. En la ficha desplegable **Texto de correo electrónico**, introduzca el contenido del mensaje en el idioma seleccionado.

Una vez que haya configurado los términos del recordatorio, puede asignarlos a los clientes en las páginas de Tarjeta de cliente. Para obtener más información, vea [Registrar nuevos clientes](sales-how-register-new-customers.md).  

## <a name="see-also"></a>Consulte también

[Cobrar saldos pendientes](receivables-collect-outstanding-balances.md)  
[Enviar recordatorios de saldos pendientes](receivables-send-reminders.md)  
[Configurar términos de interés](finance-setup-finance-charges.md)  
[Configurar las finanzas](finance-setup-finance.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
