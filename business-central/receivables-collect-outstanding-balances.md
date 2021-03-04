---
title: Cobrar saldos pendientes
description: Aprenda a enviar un recordatorio a un cliente sobre un pago pendiente y los intereses o comisiones generados por el retraso.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: payment due, debt, overdue, fee, charge, reminder
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 81f43ef3f021ef0d348eb14abdffdfda2b3d85fc
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "4758398"
---
# <a name="collect-outstanding-balances"></a>Cobrar saldos pendientes

Gestionar cobros incluye comprobar si los importes vencidos se pagan puntualmente. Si los clientes tienen pagos vencidos, puede empezar enviando el informe de **Extracto de cliente** como recordatorio. También puede emitir recordatorios.

Puede usar recordatorios para recordar a los clientes que tienen importes vencidos. También puede usar recordatorios para calcular intereses o comisiones e incluirlos en el recordatorio. Utilice documentos de interés si desea cargar a los clientes intereses o comisiones sin recordarles que tienen importes vencidos.

## <a name="statements"></a>Extractos

Desde la tarjeta del cliente, puede crear un extracto con las transacciones de ese cliente con usted. Luego, envíe al cliente el archivo PDF generado. Alternativamente, use el informe **Extracto de cliente** para enviar a sus clientes una descripción general de su negocio con usted. El extracto del cliente se puede enviar a Excel para su posterior procesamiento.  

### <a name="to-send-the-customer-statement-report"></a>Enviar el informe de extracto del cliente

1. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), introduzca **Extracto de cliente** y luego elija el enlace relacionado.
2. Rellene los campos según sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. En **Opciones de salida**, seleccione cómo enviar el informe al cliente.

> [!NOTE]
> Si usa varias divisas, el informe de Extracto de cliente siempre se imprime en la divisa del cliente. La última fecha de periodo de un extracto también se usa como la fecha del extracto y la fecha de vencimiento, si el vencimiento está incluido.

## <a name="reminders"></a>Recordatorios

Para poder crear recordatorios, debe configurar términos de recordatorio y asignarlos a sus clientes. Para más información, ver [Configurar términos y niveles de recordatorio](finance-setup-reminders.md). [!INCLUDE [reminder-terms](includes/reminder-terms.md)] El contenido de la página **Términos interés** determina si el interés se calcula en el recordatorio.  

Puede ejecutar de manera periódica el proceso **Crear recordatorios** para crear recordatorios para todos los clientes con saldos vencidos o bien crear manualmente un recordatorio para un determinado cliente y hacer que las líneas se calculen y rellenen automáticamente.  

Después de crear los recordatorios, puede modificarlos. El texto que aparece al principio y al final de un recordatorio viene determinado por los términos del nivel de recordatorio y se puede ver en la columna **Descripción**. Si se ha insertado automáticamente un importe calculado en el texto de comienzo o de fin, el texto no se ajustará si elimina líneas. A continuación, deberá usar la función **Actualizar texto recordatorio**.  

Un movimiento de cliente que tenga el campo **En espera** relleno no solicitará la creación de un recordatorio. Sin embargo, si se crea un recordatorio basándose en otro movimiento, también se incluirá en el recordatorio un movimiento vencido marcado como en espera. El interés no se calcula en líneas con estos movimientos.

Una vez creados recordatorios y realizadas las modificaciones necesarias, puede imprimir informes de test o enviar los recordatorios, normalmente por correo electrónico.

### <a name="to-create-a-reminder-automatically"></a>Para crear un recordatorio automáticamente

Los recordatorios son parecidos a las facturas. Cuando crea un recordatorio, debe rellenar una cabecera de recordatorio y una o varias líneas de recordatorio. Puede utilizar una función para crear recordatorios para todos los clientes de forma automática.

1. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), introduzca **Recordatorios** y luego elija el enlace relacionado.
2. En la página **Recordatorio**, elija la acción **Crear recordatorios**.
3. En la página **Crear recordatorios**, rellene los campos para definir cómo y para quién se crean los recordatorios.
4. Elija el botón **Aceptar**.

### <a name="to-create-a-reminder-manually"></a>Para crear un recordatorio manualmente

En la página **Recordatorio**, puede rellenar la ficha desplegable **General** manualmente y rellenar las líneas automáticamente.

1. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), introduzca **Recordatorios** y luego elija el enlace relacionado.
2. Seleccione la acción **Nuevo**.
3. En la ficha desplegable **General**, rellene los campos como sea necesario.
4. Elija la acción **Proponer líneas recordatorio**.
5. En el proceso **Proponer líneas recordatorio**, rellene los campos para definir cómo y para quién se crean los recordatorios.
6. Si desea que los recordatorios incluyan movimientos vencidos pendientes en espera, seleccione la casilla **Incluir movimientos en espera**.
7. Seleccione la casilla **Sólo movs. con importes vencidos** si desea que los recordatorios incluyan solo movimientos vencidos pendientes. Solo se mostrarán las facturas y los pagos, ya que estos son los movimientos para los cuales los pagos de sus clientes pueden haber vencido.

    > [!Important]
    > Los movimientos pendientes que están en espera se insertarán independientemente del valor de la casilla **Sólo movs. con importes vencidos**.

8. Elija el botón **Aceptar**.

### <a name="to-replace-reminder-texts"></a>Para cambiar los textos de recordatorio

Existen varias formas de definir el texto que aparecerá en el recordatorio impreso. In algunos casos, quizás le convenga cambiar los textos de comienzo o fin definidos para el nivel actual por los de otro nivel.

1. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), introduzca **Recordatorios** y luego elija el enlace relacionado.
2. Abra el recordatorio correspondiente y haga clic en la acción **Actualizar texto recordatorio** .
3. En la página **Actualizar texto recordatorio**, escriba el nivel deseado en el campo **Nivel recordatorio**.
4. Elija el botón **Aceptar** para actualizar los textos de comienzo y fin.

### <a name="to-issue-a-reminder"></a>Emitir un recordatorio

Una vez creados recordatorios y realizadas las modificaciones necesarias, puede imprimir informes de test o enviar los recordatorios.

Al emitir un recordatorio, los datos se transfieren a una página diferente para recordatorios emitidos. Al mismo tiempo, los movimientos de recordatorio se registran. Si se ha calculado interés o una comisión adicional, los movimientos se registran en la contabilidad del cliente y en la contabilidad general.

Cuando se emite un recordatorio, los movimientos se registran según las especificaciones de la página **Recordatorio**. Esta especificación determina si se registra un interés y/o recargos fijos a la cuenta del cliente y a la contabilidad. La configuración de la página **Grupo contable cliente** determina qué cuentas se registran.

Por cada movimiento de cliente del documento de interés, se crea un movimiento en la página **Movs. recordatorio/interés**.

Si las casillas **Registrar interés** o **Registrar recargo fijo** de la página **Recordatorio** están seleccionadas, se crearán también los siguientes movimientos:

- Un movimiento en la página **Movimientos de cliente**
- Un movimiento de cobros en la cuenta correspondiente
- Un movimiento de interés o uno de recargo fijo en la cuenta correspondiente

Por otra parte, la emisión del recordatorio puede afectar a los movimientos de IVA.

1. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), introduzca **Recordatorios** y luego elija el enlace relacionado.
2. Seleccione el recordatorio correspondiente y, a continuación, elija la acción **Emitir**.
3. En la página **Emitir recordatorios**, rellene los campos según sea necesario.
4. Elija el botón **Aceptar**.

El recordatorio está impreso para enviarlo a un correo electrónico específico como un archivo PDF adjunto.

### <a name="to-cancel-an-issued-reminder"></a>Para cancelar un recordatorio emitido

Si se han emitido recordatorios por error, puede cancelarlos antes de enviarlos. Puede hacerlo uno por uno o en lote.

1. En la página **Recordatorios emitidos**, seleccione una o más líneas de los recordatorios emitidos que desea cancelar y, a continuación, elija la acción **Cancelar**.
2. En la página **Cancelar recordatorios emitidos**, rellene los campos según sea necesario y, a continuación, elija el botón **Aceptar**.

## <a name="finance-charges"></a>Cargos financieros

Si un cliente no paga en la fecha de vencimiento, puede calcular automáticamente intereses y añadirlos a los importes vencidos en la cuenta del cliente. Puede informar a los clientes de los cargos añadidos enviando documentos de interés.  

> [!NOTE]  
> Los documentos de interés se utilizan para calcular intereses y para informar a los clientes que tienen intereses sin recordarles que tienen pagos vencidos. De manera alternativa, puede calcular el interés sobre pagos vencidos al crear recordatorios.  

Antes de crear documentos de interés, debe configurar los términos. Para más información, ver [Configurar términos de interés](finance-setup-finance-charges.md).  

Puede crear manualmente un documento de interés para un cliente individual y rellenar las líneas automáticamente. También puede usar la función **Crear documentos interés** para crear documentos de interés para todos o algunos de los clientes con saldos pendientes.  

Después de crear los documentos de interés, puede modificarlos. El texto que aparece al principio y al final del documento de interés viene determinado por los términos de interés y se puede ver en la columna **Descripción** de las líneas. Si se ha insertado automáticamente un importe calculado en el texto de comienzo o de fin, el texto no se ajustará si elimina líneas. A continuación, deberá usar la función **Actualizar texto interés**.  

Después de crear documentos de interés y de realizar las modificaciones necesarias, puede imprimir informes de test o emitir los documentos de interés, normalmente por correo electrónico.

### <a name="to-create-a-finance-charge-memo-manually"></a>Para crear un documento de interés manualmente

Los documentos de interés son parecidos a las facturas. Puede rellenar la cabecera manualmente y que el sistema rellene las líneas, o bien crear los documentos de interés para todos los clientes de forma automática.

1. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), introduzca **Documentos de interés** y luego elija el enlace relacionado.  
2. Elija la acción **Nuevo** y, a continuación, rellene los campos según sea necesario.  
3. Elija la acción **Proponer líneas doc. interés**.
4. En la página **Sugerir documentos financieros de interés**, establezca un filtro en la ficha desplegable **Movimientos contables de cliente** Si desea crear documentos financieros de interés sólo para determinados movimientos.

    > [!NOTE]
    > Aunque están en la lista, seleccionando **Pago** y **Abono** como **Tipo de Documento** los filtros no tendrán ningún efecto porque la función **Sugerir líneas de documento de interés** solo maneja cantidades positivas.
5.  Elija el botón **Aceptar** para iniciar el trabajo por lotes.  

### <a name="to-update-finance-charge-memo-texts"></a>Para actualizar los textos en documentos de interés  
En algunos casos, quizás le interese modificar el texto de comienzo y fin configurado para los recordatorios de interés. Si no hace esto en el momento de crear los documentos de interés aún sin emitir, puede actualizar los documentos con el texto modificado.

1. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), introduzca **Documento de interés** y luego elija el enlace relacionado.  
2. abra el documento de interés para el cual desea modificar el texto, y elija la acción **Actualizar texto interés** .
3. En la página **Actualizar texto interés**, puede definir un filtro si desea actualizar varios documentos de interés.
4. Elija el botón **Aceptar** para actualizar los textos de comienzo y fin.  

### <a name="to-issue-finance-charge-memos"></a>Emitir documentos de interés
Después de crear documentos de interés y de realizar las modificaciones necesarias, puede imprimir informes de test o emitir los documentos de interés.

Cuando se emite un recordatorio, los movimientos se registran según las especificaciones de la página **Términos interés**. Esta especificación determina si se registra un interés y/o recargos fijos a la cuenta del cliente y a la contabilidad. La configuración de la página **Grupo contable cliente** determina qué cuentas se registran.

Por cada movimiento de cliente del documento de interés, se crea un movimiento en la página **Movs. recordatorio/interés**.

Si las casillas **Registrar interés** o **Registrar recargo fijo** de la página **Términos interés** están seleccionadas, se crearán también los siguientes movimientos:

- Un movimiento en la página **Movs. cliente**
- Un movimiento de cobros en la cuenta correspondiente
- Un movimiento de interés o uno de recargo fijo en la cuenta correspondiente

Por otra parte, la emisión del documento de interés puede afectar a los movimientos de IVA.

1. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), introduzca **Documentos de interés** y luego elija el enlace relacionado.
2. Seleccione el documento correspondiente y, a continuación, elija la acción **Emitir**.
3. En la página **Emitir docs. interés**, rellene los campos según sea necesario.
4. Elija el botón **Aceptar**.

El documento de interés está impreso para enviarlo a un correo electrónico específico como un archivo PDF adjunto.

### <a name="to-cancel-an-issued-finance-charge-memo"></a>Para cancelar un documento de interés emitido
Si se han emitido documentos de interés por error, puede cancelarlos antes de enviarlos. Puede hacerlo uno por uno o en lote.
1. En la página **Documentos de interés emitidos**, seleccione una o más líneas de los documentos de interés emitidos que desea cancelar y, a continuación, elija la acción **Cancelar**.
2. En la página **Cancelar docs. de interés emitidos**, rellene los campos según sea necesario y, a continuación, elija el botón **Aceptar**.

### <a name="to-view-reminder-and-finance-charge-entries"></a>Para ver los movimientos de recordatorio y de interés  
Cuando se emite un recordatorio, se crea un movimiento de recordatorio en la página **Movs. recordatorio/interés** para cada línea de recordatorio que contenga un movimiento de cliente. Se puede obtener un resumen de los movimientos de recordatorio creados para un cliente específico.    
1. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Clientes** y luego elija el enlace relacionado.  
2. Abra la ficha de cliente correspondiente y, a continuación, elija la acción **Movimientos**.
3. En la página **Movs. cliente**, seleccione la línea que contenga el movimiento cuyos movimientos de recordatorio desea ver y, a continuación, elija la acción **Movs. recordatorio/interés.**

## <a name="multiple-interest-rates"></a>Tipos múltiples de interés

Cuando configura los términos de interés y los términos de recordatorio, para la penalización por pago atrasado, puede especificar múltiples tasas de interés para que la penalización se calcule a partir de diferentes tasas de interés en diferentes períodos. Si no se configuran los tipos múltiples de interés, se utilizará la tasa de interés y el período que se define en las páginas **Términos interés** y **Términos recordatorio** para el que se usará todo el período de cálculo. Para obtener más información, vea [Configurar tipos múltiples de interés](finance-how-to-set-up-multiple-interest-rates.md).  

## <a name="see-related-training-at-microsoft-learn"></a>Consulte Formación relacionada en [Microsoft Learn](/learn/paths/process-financial-periodic-activities-dynamics-365-business-central/)

## <a name="see-also"></a>Consulte también

[Configurar términos y niveles de recordatorios.](finance-setup-reminders.md)  
[Configurar términos interés](finance-setup-finance-charges.md)  
[Administrar cobros](receivables-manage-receivables.md)  
[Ccial](sales-manage-sales.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]