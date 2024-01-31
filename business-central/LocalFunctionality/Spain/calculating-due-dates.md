---
title: 'Cálculo de fechas de vencimiento [ES]'
description: Leer información sobre cómo presentar un informe anual de compras y ventas de los pagos que se crearon antes o después de la fecha de vencimiento.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.search.form: 7000048
ms.date: 06/21/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# Cálculo de fechas de vencimiento en la versión en español
En España, hay un límite legal para el número de días que un pago se puede retrasar. Debe presentar un informe anual de compras y ventas de los pagos que se crearon antes o después de la fecha de vencimiento. Los requisitos legales dependen de si el cliente es una empresa privada o una gestión pública. Para obtener más información, consulte la declaración oficial [BOE-A-2010-10708](https://go.microsoft.com/fwlink/?LinkId=224630) en la página web del Boletín Oficial del Estado.  

## Condiciones de pago  
Para ayudarle a cumplir los requisitos legales, puede configurar términos de pago para calcular las fechas de vencimiento correctamente. Esto especifica el número máximo de días naturales que un pago se puede retrasar después de la entrega. Por ejemplo, puede crear los términos de pago diferentes para las ventas al sector el público y las ventas a compañías privadas. La siguiente tabla muestra cómo puede configurar los términos de pago.  

|Campo|Sector público|Empresa privada|  
|---------------------------------|-------------------|---------------------|  
|**Código**|**1M(8D) PUB**|**1M(8D) PRI**|  
|**Cálculo de fecha de vencimiento**|**1M**|**1M**|  
|**Nº máx. días hasta fecha vencimiento**|**30**|**60**|  

 Para cada cliente y proveedor, debe seleccionar el código de términos de pago adecuado. A continuación, cuando cree un documento para el cliente o proveedor, [!INCLUDE[prod_short](../../includes/prod_short.md)] calculará una fecha de vencimiento que no exceda el número límite para el término correspondiente de pagos.  

> [!IMPORTANT]  
>  No puede registrar un documento que crea una remesa donde uno o varios plazos tienen una fecha de vencimiento posterior al límite que se especifica en el campo **Nº máx. días hasta fecha vencimiento**.  

 Si una fecha de vencimiento no se puede calcular basándose en el límite, la fecha de vencimiento se establece en blanco. Por ejemplo, si la fecha de vencimiento calculada cae en un período de impago y no hay una fecha disponible antes de ese período, debe especificar una fecha de vencimiento manualmente. No puede registrar un documento que tenga una fecha de vencimiento vacía.  

 Puede cambiar la fecha de vencimiento calculada manualmente, pero no puede establecer una fecha posterior al límite que ha especificado para el término de pago. Por ejemplo, la fecha de vencimiento puede calcularse para que sea muy tarde debido a conflictos con los períodos de falta de pago. En ese caso, puede decidir crear la fecha de vencimiento anterior al periodo de impagos.  

## Pagos vencidos  
 Debe incluir información acerca de pagos vencidos en los informes anuales para el gobierno. [!INCLUDE[prod_short](../../includes/prod_short.md)] incluye dos informes para ayudarle a identificar pagos vencidos de clientes y pagos retrasados.  

 Los informes **Cliente - Pagos vencidos** y **Proveedor - Pagos vencidos** incluyen una sección para cada cliente o proveedor que muestra los pagos con la siguiente información:  

- Número de factura  
- Descripción factura  
- N.º documento  
- Fecha registro  
- Fecha de vencimiento  
- Días después de vencimiento  
- Código divisa  
- Importe  
- Importe expresado en la divisa local (DL)  

Cada sección tiene una sección de resumen que contiene la siguiente información.  

|Información|Description|  
|-----------------|---------------------------------------|  
|Plazo medio ponderado superado|Esta fórmula se calcula en función del número de pagos contabilizados para el período especificado, el número de días del retraso de los pagos y el importe pagado en (DL). Para obtener más información, consulte la declaración oficial [BOE-A-2010-10708](https://go.microsoft.com/fwlink/?LinkId=224630) en la página web del Boletín Oficial del Estado.|  
|Pagos dentro límite legal|Los importes en DL y el porcentaje de pagos totales que se crearon antes de la fecha de vencimiento máxima permitida para cada transacción.|  
|Pagos fuera límite legal|Los importes en DL y el porcentaje de pagos totales que se crearon después de la fecha de vencimiento máxima permitida para cada transacción.|  

 Al final de estos informes, existe una sección que hace un resumen de esta información para todos los pagos. Estos informes mostrarán información basada en los movimientos liquidados detallados de cliente o movimientos liquidados detallados del proveedor. La información se basa en los filtros de fecha especificados. Para obtener más información, consulte el Cliente - pagos vencidos y Proveedor - pagos vencidos.  

## Consulte también  
 [Establecer límites para fechas de vencimiento](how-to-set-limits-for-due-dates.md)   
[Administrar pagos](../../payables-manage-payables.md)  
[Administrar cobros](../../receivables-manage-receivables.md)  
 [Definir las formas de pago](../../finance-payment-methods.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]