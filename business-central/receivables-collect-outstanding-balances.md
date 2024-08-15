---
title: Cobrar saldos pendientes
description: 'Aprenda cómo recordar a sus clientes los pagos pendientes. Envíe un extracto de cliente, emita un recordatorio o envíe una nota de cargo financiero.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: how-to
ms.search.keywords: 'payment due, debt, overdue, fee, charge, reminder'
ms.search.form: '6, 25, 440, 443, 448, 452'
ms.date: 07/01/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# <a name="collect-outstanding-balances"></a>Cobrar saldos pendientes

Gestionar cobros incluye comprobar si los importes vencidos se pagan puntualmente. Si los clientes tienen pagos vencidos, puede empezar enviando el informe de **Extracto de cliente** como recordatorio. También puede emitir recordatorios.

Usar recordatorios para avisar a los clientes que tienen importes vencidos. También puede usar recordatorios para calcular intereses o comisiones e incluirlos en el recordatorio. Utilice documentos de interés si desea cargar a los clientes intereses o comisiones sin recordarles que tienen importes vencidos.

## <a name="statements"></a>Extractos

Desde la tarjeta del cliente, puede crear un extracto con las transacciones de ese cliente con usted. Luego, puede generar un archivo PDF y enviarlo al cliente. Alternativamente, use el informe **Extracto de cliente** para enviar a sus clientes una descripción general de su negocio con usted. 

> [!TIP]
> Si es necesario, puede enviar el extracto a Excel para realizar cambios.  

### <a name="to-send-the-customer-statement-report"></a>Enviar el informe de extracto del cliente

1. Elija el icono ![Bombilla que abre la función Dígame 10.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Extracto del cliente** y luego elija el enlace relacionado.
2. Rellene los campos según sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. En **Opciones de salida**, seleccione cómo enviar el informe al cliente.

> [!NOTE]
> Si usa varias divisas, el informe de Extracto de cliente siempre se imprime en la divisa del cliente. La última fecha de periodo de un extracto también se usa como la fecha del extracto y la fecha de vencimiento, si el vencimiento está incluido.

## <a name="reminders"></a>Recordatorios

[!INCLUDE [receivables-reminders](includes/receivables-reminders.md)]

## <a name="finance-charges"></a>Cargos financieros

Cuando un cliente no paga en la fecha de vencimiento, puede hacer que se calculen automáticamente los cargos financieros y agregarlos a los montos vencidos en la cuenta del cliente. Puede informar a los clientes de los cargos añadidos enviando documentos de interés.  

> [!NOTE]  
> Los documentos de interés se utilizan para calcular intereses y para informar a los clientes que tienen intereses sin recordarles que tienen pagos vencidos. De manera alternativa, puede calcular el interés sobre pagos vencidos al crear recordatorios.  

Antes de crear documentos de interés, debe configurar los términos. Para más información, ver [Configurar términos de interés](finance-setup-finance-charges.md).  

Puede crear manualmente un documento de interés para un cliente individual y rellenar las líneas automáticamente. También puede usar la función **Crear documentos interés** para crear documentos de interés para todos o algunos de los clientes con saldos pendientes.  

Después de crear los documentos de interés, puede modificarlos. El texto que aparece al principio y al final del documento de interés viene determinado por los términos de interés y se puede ver en la columna **Descripción** de las líneas. Si se ha insertado automáticamente una cantidad calculada en el texto inicial o final, el texto no se ajustará si elimina líneas. A continuación, deberá usar la función **Actualizar texto interés**.  

Después de crear documentos de interés y de realizar las modificaciones necesarias, puede imprimir informes de test o emitir los documentos de interés, normalmente por correo electrónico.

### <a name="to-create-a-finance-charge-memo-manually"></a>Para crear un documento de interés manualmente

Los documentos de interés son parecidos a las facturas. Puede rellenar la cabecera manualmente y que el sistema rellene las líneas, o bien crear los documentos de interés para todos los clientes de forma automática.

1. Elija el icono ![Bombilla que abre la función Dígame 2.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Emitir docs. interés**, y luego elija el enlace relacionado.  
2. Elija la acción **Nuevo** y, a continuación, rellene los campos según sea necesario.  
3. Elija la acción **Proponer líneas doc. interés**.
4. En la página **Sugerir documentos financieros de interés**, establezca un filtro en la ficha desplegable **Movimientos contables de cliente** Si desea crear documentos financieros de interés sólo para determinados movimientos.

    > [!NOTE]
    > Aunque están en la lista, seleccionando **Pago** y **Abono** como **Tipo de Documento** los filtros no tendrán ningún efecto porque la función **Sugerir líneas de documento de interés** solo maneja cantidades positivas.
5. Elija el botón **Aceptar** para iniciar el trabajo por lotes.  

### <a name="to-update-finance-charge-memo-texts"></a>Para actualizar los textos en documentos de interés

En algunos casos, es posible que desee modificar el texto inicial y final que haya configurado para los términos del cargo financiero. Si no hace esto en el momento de crear los documentos de interés aún sin emitir, puede actualizar los documentos con el texto modificado.

1. Elija el icono ![Bombilla que abre la función Dígame 3.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Documento interés**, y luego elija el enlace relacionado.  
2. abra el documento de interés para el cual desea modificar el texto, y elija la acción **Actualizar texto interés** .
3. En la página **Actualizar texto interés**, puede definir un filtro si desea actualizar varios documentos de interés.
4. Elija el botón **Aceptar** para actualizar los textos de comienzo y fin.  

### <a name="to-issue-finance-charge-memos"></a>Emitir documentos de interés

Después de crear documentos de interés y de realizar las modificaciones necesarias, puede imprimir informes de test o emitir los documentos de interés.

Cuando emite un recordatorio, los movimientos se registran según las especificaciones de la página **Términos interés**. Esta especificación determina si se registra un interés y/o recargos fijos a la cuenta del cliente y a la contabilidad. La configuración en la página **Grupos de publicación de clientes** determina las cuentas en las que se contabilizan los intereses o tarifas.

Por cada movimiento de cliente del documento de interés, se crea un movimiento en la página **Movs. recordatorio/interés**.

Si las casillas **Registrar interés** o **Registrar recargo fijo** de la página **Términos interés** están seleccionadas, se crearán también los siguientes movimientos:

- Un movimiento en la página **Movs. cliente**
- Un movimiento de cobros en la cuenta correspondiente
- Un movimiento de interés o uno de recargo fijo en la cuenta correspondiente

Además, la emisión del documento de interés puede afectar a los movimientos de IVA.

1. Elija el icono ![Bombilla que abre la función Dígame 4.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Emitir docs. interés**, y luego elija el enlace relacionado.
2. Seleccione el documento correspondiente y, a continuación, elija la acción **Emitir**.
3. En la página **Emitir docs. interés**, rellene los campos según sea necesario.
4. Elija el botón **Aceptar**.

La nota de cargo financiero se imprime o se envía a un correo electrónico específico como un archivo PDF adjunto.

### <a name="to-cancel-an-issued-finance-charge-memo"></a>Para cancelar un documento de interés emitido

Si se emitieron notas de cargo financiero por error, puede marcarlas con el código Cancelar antes de enviarlas. Puede hacerlo una por una o en lotes.

1. En la página **Documentos de interés emitidos**, seleccione una o más líneas de los documentos de interés emitidos que desea cancelar y, a continuación, elija la acción **Cancelar**.
2. En la página **Cancelar docs. de interés emitidos**, rellene los campos según sea necesario y, a continuación, elija el botón **Aceptar**.

### <a name="to-view-reminder-and-finance-charge-entries"></a>Para ver los movimientos de recordatorio y de interés

Cuando se emite un recordatorio, se crea un movimiento de recordatorio en la página **Movs. recordatorio/interés** para cada línea de recordatorio que contenga un movimiento de cliente. Se puede obtener un resumen de los movimientos de recordatorio creados para un cliente específico.

1. Elija el icono ![Bombilla que abre la función Dígame 5.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Clientes** y luego elija el enlace relacionado.  
2. Abra la ficha de cliente correspondiente y, a continuación, elija la acción **Movimientos**.
3. En la página **Movs. cliente**, seleccione la línea que contenga el movimiento cuyos movimientos de recordatorio desea ver y, a continuación, elija la acción **Movs. recordatorio/interés.**

## <a name="multiple-interest-rates"></a>Tipos múltiples de interés

[!INCLUDE [multiple-interest-rates-def](includes/multiple-interest-rates-def.md)] Para obtener más información, vea [Configurar tipos múltiples de interés](finance-how-to-set-up-multiple-interest-rates.md).  

## <a name="see-also"></a>Consulte también

[Configurar términos, niveles y textos de recordatorios.](finance-setup-reminders.md)  
[Configurar términos de interés](finance-setup-finance-charges.md)  
[Administrar cobros](receivables-manage-receivables.md)  
[Ccial](sales-manage-sales.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
