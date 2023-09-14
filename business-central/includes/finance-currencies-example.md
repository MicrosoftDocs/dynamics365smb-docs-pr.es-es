---
author: brentholtorf
ms.topic: include
ms.date: 03/15/2022
ms.author: bholtorf
---
Cuando recibe una factura de una empresa en divisa extranjera, es bastante fácil calcular el valor en divisa local (DL) de la factura en función del tipo de cambio actual. Sin embargo, la factura a menudo incluye condiciones de pago para que pueda retrasar el pago a una fecha posterior, lo que implica una tasa de cambio potencialmente diferente. Este problema, en combinación con el hecho de que los tipos de cambio bancarios siempre difieren de los tipos de cambio oficiales, hace imposible anticipar el importe exacto en divisa local (DL) que se requiere para cubrir la factura. Si la fecha de vencimiento de la factura se extiende al mes siguiente, es posible que también deba reevaluar el importe en divisa local (DL) al final del mes. El ajuste de divisa es necesario porque el nuevo valor de DL que se requiere para cubrir el importe de la factura puede ser diferente y la deuda de la empresa con el proveedor ha cambiado potencialmente. El nuevo importe en DL puede ser mayor o menor que el importe anterior y, por tanto, representará una ganancia o una pérdida. Sin embargo, dado que la factura aún no se ha pagado, la ganancia o pérdida se considera *no realizada*. Posteriormente, se paga la factura y el banco regresa con el tipo de cambio real para el pago. No es hasta ahora cuando se calacula la ganancia o la pérdida *realizada*. Esta ganancia o pérdida no realizada se revierte y, en su lugar, se contabiliza la ganancia o pérdida realizada.

En el siguiente ejemplo, se recibe una factura el 1 de enero con el importe en la divisa de 1000. En ese momento, el tipo de cambio es 1,123.

|Fecha|Acción|Importe divisa|Tipo del documento|Importe en DL del documento|Tipo de ajuste|Importe de ventas no realizadas|Tipo del pago|Importe de pérdidas realizadas|  
|-----|----------|------------|-----------|---------|-----------|-------------|---------|---------|
|1/1|**Factura**|1000|1,123|1123|||||
|1/31|**Ajuste**|1000||1125|1,125|2|||
|2/15|**Reversión de ajuste en el pago**|1000||||-2|||
|2/15|**Pago**|1000||1120|||1,120|-3|

Al final del mes, se realiza un ajuste de la divisa cuando el tipo de la divisa de ajuste se ha establecido en 1,125, lo que genera una ganancia no realizada de 2.

En el momento del pago, el tipo de cambio real registrado en la transacción bancaria muestra un tipo de cambio de 1,120.

Aquí hay una transacción no realizada y, por lo tanto, se revertirá junto con el pago.

Finalmente, se registra el pago y la pérdida real se contabiliza en la cuenta de pérdidas realizadas.
