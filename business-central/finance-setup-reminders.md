---
title: Configurar términos y niveles de recordatorios.
description: Aprenda a configurar Business Central para enviar un recordatorio a un cliente sobre un pago pendiente y los intereses o comisiones generados por el retraso.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: payment due, debt, overdue, fee, charge, reminder
ms.date: 01/21/2021
ms.author: edupont
ms.openlocfilehash: 2d8e233fb1796515314c954d883bda7302fdcd9b
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5377042"
---
# <a name="set-up-reminder-terms-and-levels"></a>Configurar términos y niveles de recordatorios.

Puede usar recordatorios para recordar a los clientes que tienen importes vencidos. [!INCLUDE [reminder-terms](includes/reminder-terms.md)]

## <a name="reminder-terms"></a>Términos de recordatorio

Si los clientes tienen pagos vencidos, deberá decidir cómo y cuándo les enviará un recordatorio. Además, puede cargar en sus cuentas intereses o comisiones. Puede configurar un número ilimitado de recordatorios.  

> [!NOTE]
> Si desea calcular intereses sobre pagos vencidos, puede hacerlo al crear recordatorios. Sin embargo, si sólo desea calcular intereses e informar a sus clientes acerca de esto sin enviar recordatorios, debe usar [documentos de interés](finance-setup-finance-charges.md). Para más información, vea [Recordatorios](receivables-collect-outstanding-balances.md#reminders) o [Cargos financieros](receivables-collect-outstanding-balances.md#finance-charges), respectivamente.

### <a name="to-set-up-reminder-terms"></a>Para configurar los recordatorios

1. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Términos recordatorio** y luego elija el enlace relacionado.  
2. Rellene los campos según sea necesario. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]  
3. Para utilizar más de una combinación de recordatorios, configure un código para cada uno.

## <a name="reminder-levels"></a>Niveles de recordatorio

Para cada código de términos de recordatorio, puede definir un número ilimitado de niveles de recordatorio. La primera vez que se crear un recordatorio para un cliente, se utiliza la configuración del nivel 1. Cuando se emite el recordatorio, el número de nivel se registra en los movimientos de recordatorio creados y vinculados a los movimientos del cliente individuales. Si es necesario volver a recordar al cliente, se comprueban todos los movimientos de recordatorio vinculados a movimientos de cliente abiertos para localizar el número de nivel más alto. Para el nuevo recordatorio se utilizarán las condiciones del siguiente número de nivel.

Si crea más recordatorios de aquellos para los que tenga niveles definidos, se utilizarán las condiciones para el nivel más alto. Puede crear tantos recordatorios como permita el campo **Nº máx. recordatorios** en los términos de recordatorio.

### <a name="to-set-up-reminder-levels"></a>Para configurar los niveles de recordatorio

1. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Términos recordatorio** y luego elija el enlace relacionado.  
2. En la página **Términos recordatorio**, seleccione la línea que incluya los términos para los que desea configurar niveles y, a continuación, elija la acción **Niveles**.  
3. Rellene los campos según sea necesario. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]  

    > [!TIP]
    > El escenario del campo **Calcular interés** determina si el interés aparecerá en el recordatorio cuando se emita el recordatorio. Sin embargo, el campo **Publicar interés** de la página **Términos de recordatorio** determina si el interés calculado debe contabilizarse en el mayor y en las cuentas de los clientes.
    >
    > Para indicar que se debe calcular el interés, elija el campo **Calcular interés**.

    Opcionalmente, para cada nivel de recordatorio, especifique tarifas adicionales tanto en LCY como en moneda extranjera. Puede definir muchos recargos adicionales en divisas extranjeras para cada código de la página **Niveles recordatorio**.  

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

    Por ejemplo, si escribe **Tiene una deuda de %9 %7 vencida desde el %2.**, el recordatorio resultante contendrá el siguiente texto: **Tiene una deuda de 1.200,50 USD vencida desde el 02-02-2014**.

    > [!NOTE]
    > La fecha de vencimiento se calcula según la fórmula de fecha que introduzca. Para obtener más información, vea [Uso de fórmulas de fecha](ui-enter-date-ranges.md#using-date-formulas).

Una vez configurados los términos de recordatorio, con niveles y texto adicionales, escriba uno de los códigos en cada una de las fichas de cliente. Para obtener más información, vea [Registrar nuevos clientes](sales-how-register-new-customers.md).  

## <a name="see-also"></a>Consulte también .

[Cobrar saldos pendientes](receivables-collect-outstanding-balances.md)  
[Configurar términos interés](finance-setup-finance-charges.md)  
[Configurar las finanzas](finance-setup-finance.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]