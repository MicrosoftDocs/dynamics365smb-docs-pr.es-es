---
title: Configurar términos interés
description: Obtenga información sobre cómo configurar Business Central para poder informar a los clientes de los cargos adicionales mediante el envío de notas de cargos financieros.
author: edupont04
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'payment due, debt, overdue, fee, charge'
ms.search.form: '6, 494'
ms.date: 04/01/2021
ms.author: edupont
---
# Configurar términos interés

Si un cliente no paga en la fecha de vencimiento, puede calcular automáticamente intereses y añadirlos a los importes vencidos en la cuenta del cliente. Puede informar a los clientes de los cargos añadidos enviando documentos de interés. Pero primero debe definir un código que represente cada cálculo de interés financiero. Después puede introducir este código en el campo Cód. interés de las fichas de cliente.  

## Términos interés

Debe configurar los términos del cargo financiero para cada cálculo del cargo financiero y luego asignar los términos al cliente en el campo **Código de condiciones de cargo financiero** en la página **Cliente**.

Puede calcular los intereses utilizando el cálculo por días crédito o bien el cálculo por saldo vencido.

* Días saldo vencido  
  
  Se tiene en cuenta el número de días de vencimiento del pago:  
  *Método del Saldo medio día* - *intereses* = *Saldo vencido* x *(Días vencidos/Periodo de interés)* x *(Tipo interés/100)*

* Saldo vencido  
  
  El interés es una parte porcentual de éste:  
  *Método del Saldo vencido* - *intereses* = *Saldo vencido* x *(Tipo interés / 100)*

Además, cada término de la tabla Términos interés está vinculado a la subtabla Texto interés. Por cada grupo de términos de interés, puede definir un texto inicial y/o final que se incluyen en el documento de interés.

### Configurar términos interés

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Términos interés** y, a continuación, elija el vínculo relacionado.  
2. Rellene los campos según sea necesario.
3. Para utilizar más de una combinación de términos interés, configure un código para cada uno.

    Para cada término de interés, puede especificar condiciones individuales, que pueden incluir comisiones adicionales tanto en la divisa local como en la divisa extranjera. Puede definir muchos recargos adicionales en divisas extranjeras para cada término de la página **Términos interés**.
4. Seleccione la acción **Divisas**.
5. En la página **Divisas por térms. interés**, defina para cada término un código de divisa y un recargo adicional.

    > [!NOTE]  
    > Cuando crea intereses en una divisa extranjera, las condiciones de la divisa extranjera que ha configurado se utilizarán para crear documentos de interés. Si no se han configurado condiciones de interés en divisa extranjera, las condiciones de interés de DL especificadas en la página **Términos interés** se utilizarán y convertirán en la divisa pertinente.

    Para cada interés puede especificar un texto que se imprima antes (**comienzo texto**) o después (**fin texto**) de los movimientos del documento de interés.  
6. Elija las acciones **Comienzo texto** o **Fin texto** respectivamente, y rellene la página **Texto interés**.
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

## Consultar la [formación de Microsoft](/training/modules/send-memos-dynamics-365-business-central/) relacionada

## Consulte también .

[Cobrar saldos pendientes](receivables-collect-outstanding-balances.md)  
[Configurar términos y niveles de recordatorios.](finance-setup-reminders.md)  
[Configurar las finanzas](finance-setup-finance.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
