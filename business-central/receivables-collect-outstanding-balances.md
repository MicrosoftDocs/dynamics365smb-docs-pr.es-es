---
title: Recordatorios y clientes con pagos vencidos | Documentos de Microsoft
description: "Describe cómo enviar un recordatorio a un cliente sobre un pago atrasado y los intereses o comisiones generados por el retraso."
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: payment due, debt, overdue, fee, charge, reminder
ms.date: 07/05/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7664360941313da6ea0b797ef00df2e9810ad62
ms.openlocfilehash: 566594f04a1b189fe2263a945d8bd7d565539930
ms.contentlocale: es-es
ms.lasthandoff: 07/09/2018

---
# <a name="collect-outstanding-balances"></a>Cobrar saldos pendientes
Gestionar cobros incluye comprobar si los importes vencidos se pagan puntualmente. Si los clientes tienen pagos vencidos, puede empezar enviando el informe de Extracto de cliente como recordatorio. También puede emitir recordatorios.

Puede usar recordatorios para recordar a los clientes que tienen importes vencidos. También puede usar recordatorios para calcular intereses o comisiones e incluirlos en el recordatorio. Utilice documentos de interés si desea cargar a los clientes intereses o comisiones sin recordarles que tienen importes vencidos.

## <a name="reminders"></a>Recordatorios
Para poder crear recordatorios, debe configurar términos de recordatorio y asignarlos a sus clientes. Cada recordatorio tiene niveles de recordatorio predefinidos. Cada nivel de recordatorio incluye reglas acerca de cuándo se debe emitir el recordatorio, por ejemplo, los días transcurridos desde la fecha de vencimiento de la factura o la fecha del recordatorio anterior. El contenido de la ventana **Términos interés** determina si el interés se calcula en el recordatorio.  

Puede ejecutar de manera periódica el proceso **Crear recordatorios** para crear recordatorios para todos los clientes con saldos vencidos o bien crear manualmente un recordatorio para un determinado cliente y hacer que las líneas se calculen y rellenen automáticamente.  

Después de crear los recordatorios, puede modificarlos. El texto que aparece al principio y al final de un recordatorio viene determinado por los términos del nivel de recordatorio y se puede ver en la columna **Descripción**. Si se ha insertado automáticamente un importe calculado en el texto de comienzo o de fin, el texto no se ajustará si elimina líneas. A continuación, deberá usar la función **Actualizar texto recordatorio**.  

Un movimiento de cliente que tenga el campo **En espera** relleno no solicitará la creación de un recordatorio. Sin embargo, si se crea un recordatorio basándose en otro movimiento, también se incluirá en el recordatorio un movimiento vencido marcado como en espera. El interés no se calcula en líneas con estos movimientos.

Una vez creados recordatorios y realizadas las modificaciones necesarias, puede imprimir informes de test o enviar los recordatorios, normalmente por correo electrónico.

## <a name="finance-charges"></a>Cargos financieros
Si un cliente no paga en la fecha de vencimiento, puede calcular automáticamente intereses y añadirlos a los importes vencidos en la cuenta del cliente. Puede informar a los clientes de los cargos añadidos enviando documentos de interés.  

> [!NOTE]  
> Los documentos de interés se utilizan para calcular intereses y para informar a los clientes que tienen intereses sin recordarles que tienen pagos vencidos. De manera alternativa, puede calcular el interés sobre pagos vencidos al crear recordatorios.  

Puede crear manualmente un documento de interés para un cliente individual y rellenar las líneas automáticamente. También puede usar la función **Crear documentos interés** para crear documentos de interés para todos o algunos de los clientes con saldos pendientes.  

Después de crear los documentos de interés, puede modificarlos. El texto que aparece al principio y al final del documento de interés viene determinado por los términos de interés y se puede ver en la columna **Descripción** de las líneas. Si se ha insertado automáticamente un importe calculado en el texto de comienzo o de fin, el texto no se ajustará si elimina líneas. A continuación, deberá usar la función **Actualizar texto interés**.  

Después de crear documentos de interés y de realizar las modificaciones necesarias, puede imprimir informes de test o emitir los documentos de interés, normalmente por correo electrónico.

## <a name="multiple-interest-rates"></a>Tipos múltiples de interés
Cuando configura los términos de interés y los términos de recordatorio, para la penalización por pago atrasado, puede especificar múltiples tasas de interés para que la penalización se calcule a partir de diferentes tasas de interés en diferentes períodos. Si no se configuran los tipos múltiples de interés, se utilizará la tasa de interés y el período que se define en las ventanas de **Términos interés** y **Términos recordatorio** para el que se usará todo el período de cálculo. Para obtener más información, vea [Configurar tipos múltiples de interés](finance-how-to-set-up-multiple-interest-rates.md).  

## <a name="to-send-the-customer-statement-report"></a>Enviar el informe de extracto del cliente
1. Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Extracto de cliente** y, a continuación, seleccione el vínculo relacionado.
2. Rellene los campos según sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. En **Opciones de salida**, seleccione cómo enviar el informe al cliente.

> [!NOTE]  
>   Si usa varias divisas, el informe de Extracto de cliente siempre se imprime en la divisa del cliente. La última fecha de periodo de un extracto también se usa como la fecha del extracto y la fecha de vencimiento, si el vencimiento está incluido.

## <a name="to-set-up-reminder-terms"></a>Para configurar los recordatorios
Si los clientes tienen pagos vencidos, deberá decidir cómo y cuándo les enviará un recordatorio. Además, puede cargar en sus cuentas intereses o comisiones. Puede configurar un número ilimitado de recordatorios. Para cada código de términos de recordatorio, puede definir un número ilimitado de niveles de recordatorio.

1. Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Recordatorio** y, a continuación, seleccione el vínculo relacionado.  
2. Rellene los campos según sea necesario.  
3. Para utilizar más de una combinación de recordatorios, configure un código para cada uno.

## <a name="to-set-up-reminder-levels"></a>Para configurar los niveles de recordatorio
La primera vez que se crear un recordatorio para un cliente, se utiliza la configuración del nivel 1. Cuando se emite el recordatorio, el número de nivel se registra en los movimientos de recordatorio creados y vinculados a los movimientos del cliente individuales. Si es necesario volver a recordar al cliente, se comprueban todos los movimientos de recordatorio vinculados a movimientos de cliente abiertos para localizar el número de nivel más alto. Para el nuevo recordatorio se utilizarán las condiciones del siguiente número de nivel.

Si crea más recordatorios de aquellos para los que tenga niveles definidos, se utilizarán las condiciones para el nivel más alto. Puede crear tantos recordatorios como permita el campo **Nº máx. recordatorios** en los términos de recordatorio.

1. Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Recordatorio** y, a continuación, seleccione el vínculo relacionado.  
2. En la ventana **Términos recordatorio**, seleccione la línea que incluya los términos para los que desea configurar niveles y, a continuación, elija la acción **Niveles**.  
3. Rellene los campos según sea necesario.  

    Para cada nivel de recordatorio, puede especificar condiciones individuales, que pueden incluir comisiones adicionales tanto en la divisa local como en la divisa extranjera. Puede definir muchos recargos fijos en divisas extranjeras para cada código de la ventana **Niveles recordatorio**.
4. Seleccione la acción **Divisas**.
5. En la ventana **Divisas por nivel recordatorio**, defina para cada código de nivel de recordatorio y su correspondiente número de nivel de recordatorio un código de divisa y un recargo adicional.

    > [!NOTE]  
    > Cuando crea recordatorios en una divisa extranjera, se utilizarán las condiciones de la divisa extranjera configuradas en esta tabla para crear recordatorios. Si no se han configurado recordatorios en divisa extranjera, se utilizarán los recordatorios de DL configurados en la ventana **Niveles recordatorio** y se convertirán en la divisa pertinente.

    Para cada nivel de recordatorio, puede especificar el texto que se va a imprimir antes (**Comienzo texto**) o después (**Fin texto**) en las entradas del recordatorio.

6. Elija las acciones **Comienzo texto** o **Fin texto** respectivamente, y rellene la ventana **Texto recordatorio** .
7. Para insertar automáticamente valores relacionados en el texto de recordatorio resultante, escriba los siguientes marcadores de posición en el campo **Texto**.  

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

Por ejemplo, si escribe **Tiene una deuda de %9 %7 vencida desde el %2.**, el recordatorio resultante contendrá el siguiente texto: **Tiene una deuda de USD DL vencida desde el 02-02-2014**.

> [!NOTE]
> La fecha de vencimiento se calcula según la fórmula de fecha que introduzca. Para obtener más información, consulte la sección sobre el uso de fórmulas de fecha en [Introducir rangos de fechas](ui-enter-date-ranges.md).

Una vez configurados los términos de recordatorio, con niveles y texto adicionales, escriba uno de los códigos en cada una de las fichas de cliente. Para obtener más información, vea [Registrar nuevos clientes](sales-how-register-new-customers.md).

## <a name="to-create-a-reminder-automatically"></a>Para crear un recordatorio automáticamente
Los recordatorios son parecidos a las facturas. Cuando crea un recordatorio, debe rellenar una cabecera de recordatorio y una o varias líneas de recordatorio. Puede utilizar una función para crear recordatorios para todos los clientes de forma automática.

1. Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Recordatorios** y, a continuación, seleccione el vínculo relacionado.
2. En la ventana **Recordatorio**, elija la acción **Crear recordatorios**.
3. En la ventana **Crear recordatorios** , rellene los campos para definir cómo y para quién se crean los recordatorios.
4. Elija el botón **Aceptar**.

## <a name="to-create-a-reminder-manually"></a>Para crear un recordatorio manualmente
En la ventana **Recordatorio** , puede rellenar la ficha desplegable **General** manualmente y rellenar las líneas automáticamente.

1. Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Recordatorios** y, a continuación, seleccione el vínculo relacionado.
2. Seleccione la acción **Nuevo**.
3. En la ficha desplegable **General**, rellene los campos como sea necesario.
4. Elija la acción **Proponer líneas recordatorio**.
5. En el proceso **Proponer líneas recordatorio**, rellene los campos para definir cómo y para quién se crean los recordatorios.
6. Si desea que los recordatorios incluyan movimientos vencidos pendientes en espera, seleccione la casilla **Incluir movimientos en espera**.

    > [!Important]
    > Los movimientos pendientes que están en espera se insertarán independientemente del valor de la casilla Sólo movs. con importes vencidos.

7. Elija el botón **Aceptar**.

## <a name="to-replace-reminder-texts"></a>Para cambiar los textos de recordatorio  
Existen varias formas de definir el texto que aparecerá en el recordatorio impreso. In algunos casos, quizás le convenga cambiar los textos de comienzo o fin definidos para el nivel actual por los de otro nivel.

1. Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Recordatorios** y, a continuación, seleccione el vínculo relacionado.
2. Abra el recordatorio correspondiente y haga clic en la acción **Actualizar texto recordatorio** .
3. En la ventana **Actualizar texto recordatorio**, escriba el nivel deseado en el campo **Nivel recordatorio**.
3. Elija el botón **Aceptar** para actualizar los textos de comienzo y fin.

## <a name="to-issue-a-reminder"></a>Emitir un recordatorio
Una vez creados recordatorios y realizadas las modificaciones necesarias, puede imprimir informes de test o enviar los recordatorios.

Al emitir un recordatorio, los datos se transfieren a una ventana diferente para recordatorios emitidos. Al mismo tiempo, los movimientos de recordatorio se registran. Si se ha calculado interés o una comisión adicional, los movimientos se registran en la contabilidad del cliente y en la contabilidad general.

Cuando se emite un recordatorio, los movimientos se registran según las especificaciones de la ventana **Recordatorio**. Esta especificación determina si se registra un interés y/o recargos fijos a la cuenta del cliente y a la contabilidad. La configuración de la ventana **Grupo contable cliente** determina qué cuentas se registran.

Por cada movimiento de cliente del documento de interés, se crea un movimiento en la ventana  **Movs. recordatorio/interés**.

Si las casillas **Registrar interés** o **Registrar recargo fijo** de la ventana **Recordatorio** están seleccionadas, se crearán también los siguientes movimientos:

- Un movimiento en la ventana **Movs. cliente**
- Un movimiento de cobros en la cuenta correspondiente
- Un movimiento de interés o uno de recargo fijo en la cuenta correspondiente

Por otra parte, la emisión del recordatorio puede afectar a los movimientos de IVA.

1. Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Recordatorios** y, a continuación, seleccione el vínculo relacionado.
2. Seleccione el recordatorio correspondiente y, a continuación, elija la acción **Emitir**.
3. En la ventana **Emitir recordatorios**, rellene los campos según sea necesario.
4. Elija el botón **Aceptar**.

El recordatorio está impreso para enviarlo a un correo electrónico específico como un archivo PDF adjunto.

## <a name="to-set-up-finance-charge-terms"></a>Configurar términos interés
Debe definir un código para cada cálculo de interés. Después puede introducir este código en el campo **Cód. interés** de las fichas de cliente o proveedor.

Puede calcular los intereses utilizando el cálculo por días crédito o bien el cálculo por saldo vencido.

* El método del Saldo vencido

    El interés es tan solo una parte porcentual de éste:  
    *Método del Saldo vencido* - *intereses* = *Saldo vencido* x *(Tipo interés / 100)*

*   El método del Saldo medio día

    Se tiene en cuenta el número de días de vencimiento del pago:  
    *Método del Saldo medio día* - *intereses* = *Saldo vencido* x *(Días vencidos/Periodo de interés)* x *(Tipo interés/100)*

Además, cada código de la tabla Términos interés está vinculado a la subtabla Texto interés. Por cada grupo de términos de interés, puede definir un texto inicial y/o final que se incluirán en el documento de interés.

1. Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Términos interés** y, a continuación, seleccione el vínculo relacionado.  
2. Rellene los campos según sea necesario.  
3. Para utilizar más de una combinación de términos interés, configure un código para cada uno.

    Para cada término de interés, puede especificar condiciones individuales, que pueden incluir comisiones adicionales tanto en la divisa local como en la divisa extranjera. Puede definir muchos recargos adicionales en divisas extranjeras para cada código de la ventana **Términos interés**.
4. Seleccione la acción **Divisas**.
5. En la ventana **Divisas por térms. interés**, defina para cada término un código de divisa y un recargo adicional.

    > [!NOTE]  
    > Cuando crea intereses en una divisa extranjera, las condiciones de la divisa extranjera que ha configurado se utilizarán para crear documentos de interés. Si no se han configurado condiciones de interés en divisa extranjera, las condiciones de interés de DL configuradas en la ventana **Términos interés** se utilizarán y convertirán en la divisa pertinente.

    Para cada interés puede especificar un texto que se imprima antes (**comienzo texto**) o después (**fin texto**) de los movimientos del documento de interés.  
6. Elija las acciones **Comienzo texto** o **Fin texto** respectivamente, y rellene la ventana **Texto interés** .
7. Para insertar automáticamente valores relacionados en el texto de interés resultante, escriba los siguientes marcadores de posición en el campo **Texto**.

|Marcador de posición|Valor|  
|-----------------|-----------|  
|%1|Contenido del campo **Fecha emisión documento** en la cabecera del documento de interés|  
|%2|Contenido del campo **Fecha de vencimiento** en la cabecera del documento de interés|  
|%3|Contenido del campo **Tipo interés** en las condiciones relacionadas con las cargas financieras|  
|%4|Contenido del campo **Importe pendiente** en la cabecera del documento de interés|  
|%5|Contenido del campo **Importe interés** en la cabecera del documento de interés|  
|%6|Contenido del campo **Recargo adicional** en la cabecera del documento de interés|  
|%7|Importe total del recordatorio.|  
|%8|Contenido del campo **Código divisa** en la cabecera del documento de interés|  
|%9|Contenido del campo **Fecha registro** en la cabecera del documento de interés|  

## <a name="to-create-a-finance-charge-memo-manually"></a>Para crear un documento de interés manualmente  
Los documentos de interés son parecidos a las facturas. Puede rellenar la cabecera manualmente y que el sistema rellene las líneas, o bien crear los documentos de interés para todos los clientes de forma automática.

1. Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Documentos interés** y, a continuación, seleccione el vínculo relacionado.  
2. Elija la acción **Nuevo** y, a continuación, rellene los campos según sea necesario.  
3. Elija la acción **Proponer líneas doc. interés**.
4. En la ventana **Sugerir documentos financieros de interés**, establezca un filtro en la ficha desplegable **Movimientos contables de cliente** Si desea crear documentos financieros de interés sólo para determinados movimientos.  
5.  Elija el botón **Aceptar** para iniciar el trabajo por lotes.  

## <a name="to-update-finance-charge-memo-texts"></a>Para actualizar los textos en documentos de interés  
En algunos casos, quizás le interese modificar el texto de comienzo y fin configurado para los recordatorios de interés. Si no hace esto en el momento de crear los documentos de interés aún sin emitir, puede actualizar los documentos con el texto modificado.

1. Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Documento interés** y, a continuación, seleccione el vínculo relacionado.  
2. abra el documento de interés para el cual desea modificar el texto, y elija la acción **Actualizar texto interés** .
3. En la ventana **Actualizar texto interés**, puede definir un filtro si desea actualizar varios documentos de interés.
4. Elija el botón **Aceptar** para actualizar los textos de comienzo y fin.  

## <a name="to-issue-finance-charge-memos"></a>Emitir documentos de interés
Después de crear documentos de interés y de realizar las modificaciones necesarias, puede imprimir informes de test o emitir los documentos de interés.

Cuando se emite un recordatorio, los movimientos se registran según las especificaciones de la ventana **Términos interés**. Esta especificación determina si se registra un interés y/o recargos fijos a la cuenta del cliente y a la contabilidad. La configuración de la ventana **Grupo contable cliente** determina qué cuentas se registran.

Por cada movimiento de cliente del documento de interés, se crea un movimiento en la ventana  **Movs. recordatorio/interés**.

Si las casillas **Registrar interés** o **Registrar recargo fijo** de la ventana **Términos interés** están seleccionadas, se crearán también los siguientes movimientos:

- Un movimiento en la ventana **Movs. cliente**
- Un movimiento de cobros en la cuenta correspondiente
- Un movimiento de interés o uno de recargo fijo en la cuenta correspondiente

Por otra parte, la emisión del documento de interés puede afectar a los movimientos de IVA.

1. Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Documentos interés** y, a continuación, seleccione el vínculo relacionado.
2. Seleccione el documento correspondiente y, a continuación, elija la acción **Emitir**.
3. En la ventana **Emitir docs. interés**, rellene los campos según sea necesario.
4. Elija el botón **Aceptar**.

El documento de interés está impreso para enviarlo a un correo electrónico específico como un archivo PDF adjunto.

## <a name="to-view-reminder-and-finance-charge-entries"></a>Para ver los movimientos de recordatorio y de interés  
Cuando se emite un recordatorio, se crea un movimiento de recordatorio en la ventana **Movs. recordatorio/interés** para cada línea de recordatorio que contenga un movimiento de cliente. Se puede obtener un resumen de los movimientos de recordatorio creados para un cliente específico.    
1. Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Clientes** y, a continuación, seleccione el vínculo relacionado.  
2. Abra la ficha de cliente correspondiente y, a continuación, elija la acción **Movimientos**.
3. En la ventana **Movs. cliente**, seleccione la línea que contenga el movimiento cuyos movimientos de recordatorio desea ver y, a continuación, elija la acción **Movs. recordatorio/interés.**

## <a name="see-also"></a>Consulte también
[Administrar cobros](receivables-manage-receivables.md)  
[Ventas](sales-manage-sales.md)  
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

