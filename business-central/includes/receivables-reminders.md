---
author: edupont04
ms.topic: include
ms.date: 02/09/2022
ms.author: edupont
ms.openlocfilehash: fc1788acfb1b11a90327ac72ce83d7fa4981e602
ms.sourcegitcommit: ef80c461713fff1a75998766e7a4ed3a7c6121d0
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 02/15/2022
ms.locfileid: "8143353"
---
Puede usar recordatorios para recordar a los clientes que tienen importes vencidos. También puede usar recordatorios para calcular intereses o comisiones e incluirlos en el recordatorio.

Para poder crear recordatorios, debe configurar términos de recordatorio y asignarlos a sus clientes. Para más información, consulte [Configurar términos y niveles de recordatorio](../finance-setup-reminders.md). [!INCLUDE [reminder-terms](reminder-terms.md)] El contenido de la página **Términos de interés** determina si el interés se calcula en el recordatorio.  

Puede ejecutar de manera periódica el proceso **Crear recordatorios** para crear recordatorios para todos los clientes con saldos vencidos o bien crear manualmente un recordatorio para un determinado cliente y hacer que las líneas se calculen y rellenen automáticamente.  

Después de crear los recordatorios, puede modificarlos. El texto que aparece al principio y al final de un recordatorio viene determinado por los términos del nivel de recordatorio y se puede ver en la columna **Descripción**. Si se ha insertado automáticamente un importe calculado en el texto de comienzo o de fin, el texto no se ajustará si elimina líneas. A continuación, deberá usar la función **Actualizar texto recordatorio**.  

Un movimiento de cliente que tenga el campo **En espera** relleno no solicitará la creación de un recordatorio. Sin embargo, si se crea un recordatorio basándose en otro movimiento, también se incluirá en el recordatorio un movimiento vencido marcado como en espera. El interés no se calcula en líneas con estos movimientos.

Una vez creados recordatorios y realizadas las modificaciones necesarias, puede imprimir informes de test o enviar los recordatorios, normalmente por correo electrónico.

### <a name="to-create-a-reminder-automatically"></a>Para crear un recordatorio automáticamente

Los recordatorios son parecidos a las facturas. Cuando crea un recordatorio, debe rellenar una cabecera de recordatorio y una o varias líneas de recordatorio. Puede utilizar una función para crear recordatorios para todos los clientes de forma automática.

1. Elija el icono ![Bombilla que abre la característica Dígame 0.](../media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Recordatorios** y luego elija el enlace relacionado.
2. En la página **Recordatorio**, elija la acción **Crear recordatorios**.
3. En la página **Crear recordatorios**, rellene los campos para definir cómo y para quién se crean los recordatorios.
4. Elija el botón **Aceptar**.

### <a name="to-create-a-reminder-manually"></a>Para crear un recordatorio manualmente

En la página **Recordatorio**, puede rellenar la ficha desplegable **General** manualmente y rellenar las líneas automáticamente.

1. Elija el icono ![Bombilla que abre otra vez la característica Dígame 2.](../media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Recordatorios** y luego elija el vínculo relacionado.
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

1. Elija el icono ![Bombilla que abre otra vez más la característica Dígame 3.](../media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Recordatorios** y luego elija el vínculo relacionado.
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

1. Elija el icono ![Bombilla que abre también aquí la característica Dígame 4.](../media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Recordatorios** y luego elija el vínculo relacionado.
2. Seleccione el recordatorio correspondiente y, a continuación, elija la acción **Emitir**.
3. En la página **Emitir recordatorios**, rellene los campos según sea necesario.
4. Elija el botón **Aceptar**.

El recordatorio está impreso para enviarlo a un correo electrónico específico como un archivo PDF adjunto.

### <a name="to-cancel-an-issued-reminder"></a>Para cancelar un recordatorio emitido

Si se han emitido recordatorios por error, puede cancelarlos antes de enviarlos. Puede hacerlo uno por uno o en lote.

1. En la página **Recordatorios emitidos**, seleccione una o más líneas de los recordatorios emitidos que desea cancelar y, a continuación, elija la acción **Cancelar**.
2. En la página **Cancelar recordatorios emitidos**, rellene los campos según sea necesario y, a continuación, elija el botón **Aceptar**.


