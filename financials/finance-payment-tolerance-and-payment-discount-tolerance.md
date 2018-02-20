---
title: Tolerancia de pago y tolerancia de descuento de pago | Documentos de Microsoft
description: Puede configurar la tolerancia de pago para cerrar una factura cuando el pago no cubre totalmente el importe de la factura.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/10/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 7b8c24469a087c16c2e351b456b015e8fdd65f82
ms.contentlocale: es-es
ms.lasthandoff: 01/30/2018

---
# <a name="work-with-payment-tolerances-and-payment-discount-tolerances"></a>Trabajar con tolerancias de pago y tolerancias de descuento de pago
Puede configurar una tolerancia de pago para cerrar una factura cuando el pago no cubre totalmente el importe de la factura. Puede configurar una tolerancia de descuento P.P. para conceder un descuento P.P. después de que haya pasado la fecha de descuento.  

Puede utilizar las tolerancias de pago para que cada importe pendiente tenga una tolerancia de pago máxima permitida. Si se cumple la tolerancia de pago, el importe de pago se analiza. Si no se ha pagado todo el importe, el importe pendiente se cerrará totalmente con el importe que falta por pagar. Se registra un movimiento detallado para el movimiento de pago para que no exista un importe pendiente en el movimiento de factura liquidado. Si se ha pagado más del importe pendiente, se registra un movimiento detallado para el movimiento de pago para que no exista un importe pendiente en el movimiento de pago.

Puede utilizar tolerancias de descuento de pago para que si acepta un descuento P.P. después de la fecha de descuento, siempre se registre en la cuenta de descuento P.P. o en la cuenta de tolerancia de pagos.

## <a name="applying-payment-tolerance-to-multiple-documents"></a>Aplicar la tolerancia de pagos en varios documentos  
Un documento tendrá las tolerancia de pago si se liquida con él mismo o con otros documentos. La aceptación de un descuento de pago vencido al aplicar la tolerancia de pago a varios documentos se produce automáticamente para cada documento cuando true la siguiente norma es verdadera:  

*fecha de descuento P.P. < fecha de pago del movimiento seleccionado <= fecha de tolerancia de pago*  

Esta regla también aplica para determinar si se muestran las advertencias cuando aplica la tolerancia de pago a varios documentos. La advertencia de tolerancia de descuento de pago se muestra para cada movimiento que cumpla los criterios de fecha. Para obtener más información, consulte la sección "Ejemplo 2: cálculos de tolerancia para varios documentos".

Puede optar por mostrar una advertencia que se base en las distintas situaciones de tolerancia.  

- La primera advertencia es para la tolerancia de descuento. Se le informará que puede aceptar un descuento P.P. vencido. Puede entonces elegir si acepta la tolerancia en la fecha de descuento.  
- La segunda advertencia es para la tolerancia de pago. Se le informará al usuario que se pueden cerrar todos los movimientos ya que la diferencia está dentro de la suma de la máximo tolerancia de pago para los movimientos liquidados. Puede entonces elegir si acepta la tolerancia en el importe del pago.

Para obtener más información, consulte la sección "Activar o desactivar la advertencia de tolerancia de pago".     

## <a name="to-set-up-tolerances"></a>Para configurar las tolerancias  
La tolerancia en días e importes le permite cerrar una factura aunque el pago no se haya realizado todo el pago del importe de la misma, si esto se debe a que se ha superado la fecha de vencimiento del descuento por pronto pago, a que se han realizado deducciones o a causa de un error sin importancia. Esto también se aplica a reembolsos y abonos.  

Para configurar la tolerancia tiene que configurar varias cuentas de tolerancia, especificar la tolerancia de descuento en el pago y los métodos de registro de tolerancia en el pago y, a continuación, ejecute el proceso **Cambiar tolerancia pagos**.  
1. Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), introduzca **Configuración grupos contables** y, a continuación, elija el vínculo relacionado.  
2. En la ventana **Configuración grupos contables**, configure una cuenta de debe y de haber de tolerancia de pago de ventas y una cuenta de debe y de haber de tolerancia de pago de compras  
3. Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Grupos contables clientes** y, a continuación, seleccione el vínculo relacionado.    
4. En la ventana **Grupos contables clientes**, configure una cuenta de debe y de haber de tolerancia de pagos. Para obtener más información, consulte [Configurar los grupos contables](finance-posting-groups.md).  
5. Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Configuración de registro del proveedor** y, a continuación, seleccione el vínculo relacionado.  
6. En la ventana **Grupos contables proveedores**, configure una cuenta de debe y de haber de tolerancia de pagos.  
7. Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), introduzca **Configuración contabilidad** y, a continuación, elija el vínculo relacionado.  
8. Abra la ventana **Configuración contabilidad**.  
9. En la ficha desplegable **Liquidación**, rellene los campos **Registrar tolerancia dto. P.P.**, **Periodo gracia descuento pagos** y **Registrar tolerancia pagos**.   
10. Seleccione la acción **Cambiar tolerancia pagos**.
11. En la ventana **Cambiar tolerancia pagos**, rellene los campos **% Tolerancia pago** y **Máx. importe tolerancia pago** y, a continuación, seleccione **Aceptar**.

> [!IMPORTANT]  
>  Sólo ha configurado la tolerancia para las divisa local. Si desea que [!INCLUDE[d365fin](includes/d365fin_md.md)] controle la tolerancia de pagos, abonos y reembolsos en una divisa extranjera, debe ejecutar el proceso **Cambiar tolerancia pagos** con un valor en el campo **Código divisa**.  

> [!NOTE]  
>  Si desea recibir una advertencia de tolerancia de pagos cada vez que registre una liquidación dentro de la tolerancia, debe activar la advertencia de tolerancia de pagos. Para obtener más información, consulte la sección "Activar o desactivar la advertencia de tolerancia de pago".  
>   
>  Para desactivar la tolerancia de un cliente o proveedor, debe bloquear las tolerancias en la ficha del cliente o proveedor correspondiente. Para obtener más información, consulte la sección "Bloquear la tolerancia de pagos de clientes".  
>   
>  Al configurar la tolerancia, [!INCLUDE[d365fin](includes/d365fin_md.md)] comprueba si existen movimientos pendientes y también calcula la tolerancia de estos movimientos.

## <a name="to-enable-or-disable-payment-tolerance-warnings"></a>Para activar o desactivar las advertencias de tolerancia de pago
La advertencia de tolerancia de pagos aparece cuando registra una liquidación con un saldo dentro de la tolerancia permitida. A continuación, puede elegir cómo desea registrar y documentar el saldo.    
1. Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), introduzca **Configuración contabilidad** y, a continuación, elija el vínculo relacionado.  
2. En la ventana **Configuración contabilidad**, en la ficha desplegable **Liquidación**, active el campo **Advertencia tolerancia pagos** para activar la advertencia. Para desactivar la advertencia, desactive el campo.  

> [!NOTE]  
>  La opción predeterminada para la ventana **Advertencia tolerancia pagos** es **Dejar el saldo como importe pendiente**. La opción predeterminada para la ventana **Advertencia tolerancia dto. P.P.** es **No aceptar el descuento por pago vencido**.

## <a name="to-block-payment-tolerance-for-customers"></a>Para bloquear la tolerancia de pagos de clientes  
El valor predeterminado para la tolerancia de pagos es permitida. Para no permitir la tolerancia de pagos de un cliente o proveedor determinado tiene que bloquear la tolerancia en la ficha del cliente o proveedor correspondiente. A continuación se describe cómo debe hacerlo para un cliente. Los pasos son parecidos para un proveedor.

1. Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Cliente** o **Proveedor** y, a continuación, seleccione el vínculo relacionado.  
2. En la Ficha desplegable **Pagos**, seleccione la casilla **Bloquear tolerancia de pagos**.  

> [!NOTE]  
>  Si el cliente o proveedor tiene movimientos pendientes, primero debe eliminar la tolerancia de pagos de los movimientos que están abiertos actualmente.

## <a name="example-1---tolerance-calculations-for-a-single-document"></a>Ejemplo 1: cálculos de tolerancia para un único documento
A continuación, se presentan algunos ejemplos que muestran los cálculos de tolerancia previstos y los registros que se producen en diferentes situaciones.  

La ventana **Configuración contabilidad** contiene la configuración siguiente:
- Periodo gracia descuento pagos:    5D  
- Máx. tolerancia pagos: 5  

Los ejemplos con la alternativa A o B representan lo siguiente:  

- **A**: en este caso la advertencia tolerancia dto. P.P. se ha desactivado O el usuario tiene activado la advertencia y ha seleccionado permitir el descuento P.P vencido (Registrar el saldo como tolerancia pagos).  
- **B** en este caso, el usuario tiene activada la advertencia y ha seleccionado no permitir el descuento P.P vencido (Dejar el saldo como importe pendiente).  

[!div class="mx-tdBreakAll"]  
|—|Fra.|Dto. P.P.|Máx. tol. pagos|Fecha dto. P.P.|Fecha tol. dto. Fecha|Fecha pago|Tol.|Tipo tolerancia|Todos los movimientos cerrados|Fecha tol. dto. Cb/Cl|tol. pagos Cb.|  
|-------|----------|----------------|-----------------------|---------------------|--------------------------|------------------|----------|--------------------|------------------------|------------------------------|----------------------------|  
|1|1,000|nº 20|5|15/01/03|20/01/03|<=15/01/03|985|Tol. pagos|Sí|0|-5|  
|2|**1,000**|**20**|**5**|**15/01/03**|**20/01/03**|**<=15/01/03**|**980**|**Ninguno**|**Sí**|**0**|**0**|  
|3|1,000|nº 20|5|15/01/03|c|<=15/01/03|975|Tol. pagos|Sí|0|5|  
|4A|1,000|nº 20|5|15/01/03|20/01/03|16/01/03 20/01/03|1005|Tol. dto.|No, 25 en pagos|20/-20|0|  
|5A|1,000|nº 20|5|15/01/03|20/01/03|16/01/03 20/01/03|1000|Tol. dto.|No, 20 en pagos|20/-20|0|  
|6A|1,000|nº 20|5|15/01/03|20/01/03|16/01/03 20/01/03|995|Tol. dto.|No, 15 en pagos|20/-20|0|  
|4B|1,000|nº 20|5|15/01/03|20/01/03|16/01/03 20/01/03|1005|Tol. pagos|Sí|0|-5|  
|**5B**|**1,000**|**20**|**5**|**15/01/03**|**20/01/03**|**16/01/03 20/01/03**|**1000**|**Ninguno**|**Sí**|**0**|**0**|  
|6B|1,000|nº 20|5|15/01/03|20/01/03|16/01/03 20/01/03|995|Tol. pagos|Sí|0|5|  
|7|1,000|nº 20|5|15/01/03|20/01/03|16/01/03 20/01/03|985|Tol. dto. P.P. y Tol. pagos|Sí|20/-20|-5|  
|8|1,000|nº 20|5|15/01/03|20/01/03|16/01/03 20/01/03|980|Tol. dto.|Sí|20/-20|0|  
|9|1,000|nº 20|5|15/01/03|20/01/03|16/01/03 20/01/03|975|Tol. dto. P.P. y Tol. pagos|Sí|20/-20|5|  
|10|1,000|nº 20|5|15/01/03|20/01/03|>20/01/03|1005|Tol. pagos|Sí|0|-5|  
|**11**|**1,000**|**20**|**5**|**15/01/03**|**20/01/03**|**>20/01/03**|**1000**|**Ninguno**|**Sí**|**0**|**0**|  
|12|1,000|nº 20|5|15/01/03|20/01/03|>20/01/03|995|Tol. pagos|Sí|0|5|  
|13|1,000|nº 20|5|15/01/03|20/01/03|>20/01/03|985|Ninguno|No, 15 en la factura|0|0|  
|14|1,000|nº 20|5|15/01/03|20/01/03|>20/01/03|980|Ninguno|No, 20 en la factura|0|0|  
|15|1,000|nº 20|5|15/01/03|20/01/03|>20/01/03|975|Ninguno|No, 25 en la factura|0|0|  

### <a name="payment-range-diagrams"></a>Diagramas de preparación, espera y movimiento de pago  
En relación con el ejemplo anterior, los diagramas de los intervalos de pagos son los siguientes:  

#### <a name="1-payment-date-011503-scenarios-1-3"></a>(1) Fecha pago <=15/01/03 (ejemplos 1 a 3)  
Importe pendiente por  

Reglas de liquidación normales  

![Reglas de tolerancia de pago único (antes del 15/03)](media/singlePmtTolRules(Pre1503).gif "singlePmtTolRules(Pre1503)")  

(1) si el pago no se produce en estos intervalos, todos los movimientos de liquidación se cierran con o sin tolerancia..  

(2) si el pago no se produce en estos intervalos, ningún movimiento de liquidación se puede cerrar aunque tenga tolerancia.  

#### <a name="2-payment-date-is-between-011603-and-012003-scenarios-4-9"></a>(2) La fecha de pago está comprendida entre 16/01/03 y 20/01/03 (ejemplos 4 a 9)  
Importe pendiente por  

Reglas de liquidación normales  

![Reglas de tolerancia de pago único (período de gracia)](media/singlePmtTolRules(GracePeriod).gif "singlePmtTolRules(GracePeriod)")  

(1) si el pago no se produce en estos intervalos, todos los movimientos de liquidación se cierran con o sin tolerancia..  

(2) si el pago no se produce en estos intervalos, ningún movimiento de liquidación se puede cerrar aunque tenga tolerancia.  

#### <a name="3-payment-date-is-after-012003-scenarios-10-15"></a>(3) la fecha de pago es posterior a 20/01/03 (ejemplos 10 a 15)  
Importe pendiente por  

Reglas de liquidación normales  

![Reglas de tolerancia de pago único (antes del 20/01)](media/singlePmtTolRules(Post0120).gif "singlePmtTolRules(Post0120)")  

(1) si el pago no se produce en estos intervalos, todos los movimientos de liquidación se cierran con o sin tolerancia..  

(2) (2) si el pago no se produce en estos intervalos, ningún movimiento de liquidación se puede cerrar aunque tenga tolerancia.  

## <a name="example-2---tolerance-calculations-for-multiple-documents"></a>Ejemplo 2: cálculos de tolerancia para varios documentos
A continuación, se presentan algunos ejemplos que muestran los cálculos de tolerancia previstos y los registros que se producen en diferentes situaciones. Los ejemplos se limitan únicamente a las situaciones que dan como resultado que todos los movimientos de liquidación se cierran.  

La ventana **Configuración contabilidad** contiene la configuración siguiente:
- Periodo gracia descuento pagos 5D  
- Máx. tolerancia pagos 5  

Los ejemplos con la alternativa A, B, C o D representan lo siguiente:  

- **A** en este caso la Advertencia tolerancia dto. P.P. se ha desactivado O el usuario tiene activada la advertencia y ha seleccionado permitir el descuento P.P vencido (Registrar como tolerancia) en una factura.  
- **B** en este caso, el usuario tiene activada la advertencia y ha seleccionado no permitir el descuento P.P vencido en una factura.  
- **C**: en este caso, el usuario tiene activada la advertencia y ha seleccionado permitir el descuento P.P vencido en la primera factura, pero no en la segunda.  
- **D**: en este caso, el usuario tiene activada la advertencia y ha seleccionado no permitir el descuento P.P vencido en la primera factura, pero sí en la segunda.  

[!div class="mx-tdBreakAll"]  

|—|Fra.|Dto. P.P.|Máx. tol. pagos|Fecha dto. P.P.|Fecha tol. dto. Fecha|Fecha pago|Dto. P.P.|Tipo tolerancia|Todos los movimientos cerrados|Fecha tol. dto. Cb/Cl|tol. pagos Cb.|  
|-------|----------|---------------|-------------------|---------------------|--------------------------|------------------|---------|--------------------|------------------------|------------------------------|------------------------|  
|1|1,000 <br />1,000|60 <br />30|5 <br />5|15/01/03 <br />17/01/03|20/01/03 <br />22/01/03|<=15/01/03|1920|Tol. pagos|Sí|0<br /><br /> 0|-5 <br />-5|  
|**2**|**1,000** <br />**1,000**|**60** <br />**30**|**5** <br />**5**|**15/01/03** <br />**17/01/03**|**20/01/03** <br />**22/01/03**|**<=15/01/03**|**1910**|**Ninguno**|**Sí**|**0**<br /><br /> **0**|0 <br />0|  
|3|1,000 <br />1,000|60 <br />30|5 <br />5|15/01/03 <br />17/01/03|20/01/03 <br />22/01/03|<=15/01/03|1900|Tol. pagos|Sí|0<br /><br /> 0|5 <br />5|  
|4B|1,000 <br />1,000|60 <br />30|5 <br />5|15/01/03 <br />17/01/03|20/01/03 <br />22/01/03|16/01/03 17/01/03|1980|Tol. pagos|Sí|0<br /><br /> 0|-5<br /><br /> -5|  
|**5B**|**1,000** <br />**1,000**|**60** <br />**30**|**5** <br />**5**|**15/01/03** <br />**17/01/03**|**20/01/03** <br />**22/01/03**|**16/01/03 17/01/03**|**1970**|**Ninguno**|**Sí**|**0**<br /><br /> **0**|**0**<br /><br /> **0**|  
|6B|1,000 <br />1,000|60 <br />30|5 <br />5|15/01/03 <br />17/01/03|20/01/03 <br />22/01/03|16/01/03 17/01/03|1960|Tol. pagos|Sí|0<br /><br /> 0|5<br /><br /> 5|  
|7A|1,000 <br />1,000|60 <br />30|5 <br />5|15/01/03 <br />17/01/03|20/01/03 <br />22/01/03|16/01/03 17/01/03|1920|Tol. dto. P.P. y Tol. pagos|Sí|60/60<br /><br /> 0/0|-5 <br />-5|  
|8A|1,000 <br />1,000|60 <br />30|5 <br />5|15/01/03 <br />17/01/03|20/01/03 <br />22/01/03|16/01/03 17/01/03|1910|Tol. dto.|Sí|60/60<br /><br /> 0/0|0 <br />0|  
|9A|1,000 <br />1,000|60 <br />30|5 <br />5|15/01/03 <br />17/01/03|20/01/03 <br />22/01/03|16/01/03 17/01/03|1900|Tol. dto. P.P. y Tol. pagos|Sí|60/60|5 <br />5|  
|10B|1,000 <br />1,000|60 <br />30|5 <br />5|15/01/03 <br />17/01/03|20/01/03 <br />22/01/03|18/01/03 20/01/03|2010|Tol. pagos|Sí|0<br /><br /> 0|-5<br /><br /> -5|  
|**11B**|**1,000** <br />**1,000**|**60** <br />**30**|**5** <br />**5**|**15/01/03** <br />**17/01/03**|**20/01/03** <br />**22/01/03**|**18/01/03 20/01/03**|**2000**|**Ninguno**|**Sí**|**0**<br /><br /> **0**|**0**<br /><br /> **0**|  
|12B|1,000 <br />1,000|60 <br />30|5 <br />5|15/01/03 <br />17/01/03|20/01/03 <br />22/01/03|18/01/03 20/01/03|1990|Tol. pagos|Sí|0<br /><br /> 0|5<br /><br /> 5|  
|13D|1,000 <br />1,000|60 <br />30|5 <br />5|15/01/03 <br />17/01/03|20/01/03 <br />22/01/03|18/01/03 20/01/03|1980|Tol. dto. P.P. y Tol. pagos|Sí|0/0<br /><br /> 30/-30|-5 <br />-5|  
|14D|1,000 <br />1,000|60 <br />30|5 <br />5|15/01/03 <br />17/01/03|20/01/03 <br />22/01/03|18/01/03 20/01/03|1970|Tol. dto.|Sí|0/0<br /><br /> 30/-30|0 <br />0|  
|15D|1,000 <br />1,000|60 <br />30|5 <br />5|15/01/03 <br />17/01/03|20/01/03 <br />22/01/03|18/01/03 20/01/03|1960|Tol. dto. P.P. y Tol. pagos|Sí|0/0<br /><br /> 30/-30|5 <br />5|  
|16D|1,000 <br />1,000|60 <br />30|5 <br />5|15/01/03 <br />17/01/03|20/01/03 <br />22/01/03|18/01/03 20/01/03|1950|Tol. dto. P.P. y Tol. pagos|Sí|60/-60<br /><br /> 0/0|-5 <br />-5|  
|17D|1,000 <br />1,000|60 <br />30|5 <br />5|15/01/03 <br />17/01/03|20/01/03 <br />22/01/03|18/01/03 20/01/03|1940|Tol. dto.|Sí|60/-60<br /><br /> 0/0|0 <br />0|  
|18D|1,000 <br />1,000|60 <br />30|5 <br />5|15/01/03 <br />17/01/03|20/01/03 <br />22/01/03|18/01/03 20/01/03|1930|Tol. dto. P.P. y Tol. pagos|Sí|60/-60<br /><br /> 0/0|5 <br />5|  
|19A|1,000 <br />1,000|60 <br />30|5 <br />5|15/01/03 <br />17/01/03|20/01/03 <br />22/01/03|18/01/03 20/01/03|1920|Tol. dto. P.P. y Tol. pagos|Sí|60/-60<br /><br /> 30/-30|-5 <br />-5|  
|20A|1,000 <br />1,000|60 <br />30|5 <br />5|15/01/03 <br />17/01/03|20/01/03 <br />22/01/03|18/01/03 20/01/03|1910|Tol. dto.|Sí|60/-60<br /><br /> 30/-30|0 <br />0|  
|21A|1,000 <br />1,000|60 <br />30|5 <br />5|15/01/03 <br />17/01/03|20/01/03 <br />22/01/03|18/01/03 20/01/03|1900|Tol. dto. P.P. y Tol. pagos|Sí|60/-60<br /><br /> 30/-30|5 <br />5|  
|22B|1,000 <br />1,000|60 <br />30|5 <br />5|15/01/03 <br />17/01/03|20/01/03 <br />22/01/03|21/01/03 22/01/03|2010|Tol. pagos|Sí|0<br /><br /> 0|-5<br /><br /> -5|  
|**23B**|**1,000** <br />**1,000**|**60** <br />**30**|**5** <br />**5**|**15/01/03** <br />**17/01/03**|**20/01/03** <br />**22/01/03**|**21/01/03 22/01/03**|**2000**|**Ninguno**|**Sí**|**0**<br /><br /> **0**|**0**<br /><br /> **0**|  
|24B|1,000 <br />1,000|60 <br />30|5 <br />5|15/01/03 <br />17/01/03|20/01/03 <br />22/01/03|21/01/03 22/01/03|1990|Tol. pagos|Sí|0<br /><br /> 0|5<br /><br /> 5|  
|25A|1,000 <br />1,000|60 <br />30|5 <br />5|15/01/03 <br />17/01/03|20/01/03 <br />22/01/03|21/01/03 22/01/03|1980|Tol. dto. P.P. y Tol. pagos|Sí|0/0<br /><br /> 30/30|-5 <br />-5|  
|26A|1,000 <br />1,000|60 <br />30|5 <br />5|15/01/03 <br />17/01/03|20/01/03 <br />22/01/03|21/01/03 22/01/03|1970|Tol. dto.|Sí|0/0<br /><br /> 30/30|0 <br />0|  
|27A|1,000 <br />1,000|60 <br />30|5 <br />5|15/01/03 <br />17/01/03|20/01/03 <br />22/01/03|21/01/03 22/01/03|1960|Tol. dto. P.P. y Tol. pagos|Sí|0/0<br /><br /> 30/30|5 <br />5|  
|28|1,000 <br />1,000|60 <br />30|5 <br />5|15/01/03 <br />17/01/03|20/01/03 <br />22/01/03|>22/01/03|2010|Tol. pagos|Sí|0|-5|  
|**29**|**1,000** <br />**1,000**|**60** <br />**30**|**5** <br />**5**|**15/01/03** <br />**17/01/03**|**20/01/03** <br />**22/01/03**|**>22/01/03**|**2000**|**Ninguno**|**Sí**|**0**|**0**|  
|30|1,000 <br />1,000|60 <br />30|5 <br />5|15/01/03 <br />17/01/03|20/01/03 <br />22/01/03|>22/01/03|1990|Tol. pagos|Sí|0|5|  

### <a name="payment-range-diagrams"></a>Diagramas de preparación, espera y movimiento de pago  
En relación con el ejemplo anterior, los diagramas de los intervalos de pagos son los siguientes:  

#### <a name="1-payment-date-011503-scenarios-1-3"></a>(1) Fecha pago <=15/01/03 (ejemplos 1 a 3)  
Importe pendiente por  

Reglas de liquidación normales  

![Reglas de tolerancia de pagos múltiples (antes del 15/03)](media/multiplePmtTolRules(Pre1503).gif "multiplePmtTolRules(Pre1503)")  

(1) si el pago no se produce en estos intervalos, todos los movimientos de liquidación se cierran con o sin tolerancia..  

(2) si el pago no se produce en estos intervalos, ningún movimiento de liquidación se puede cerrar aunque tenga tolerancia.  

#### <a name="2-payment-date-is-between-011603-and-011703-scenarios-4-9"></a>(2) La fecha de pago está comprendida entre 16/01/03 y 17.01.03 (ejemplos 4 a 9)  
Importe pendiente por  

Reglas de liquidación normales  

![Reglas de tolerancia de pagos múltiples (período de gracia)](media/multiplePmtTolRules(GracePeriodInv1).gif "multiplePmtTolRules(GracePeriodInv1)")  

(1) si el pago no se produce en estos intervalos, todos los movimientos de liquidación se cierran con o sin tolerancia..  

(2) si el pago no se produce en estos intervalos, ningún movimiento de liquidación se puede cerrar aunque tenga tolerancia.  

#### <a name="3-payment-date-is-between-011803-and-012003-scenarios-10-21"></a>(3) La fecha de pago está comprendida entre 01/18/03 y 20/01/03 (ejemplos 10 a 21)  
Importe pendiente por  

Reglas de liquidación normales  

![Reglas de tolerancia de pagos múltiples (período de gracia)](media/multiplePmtTolRules(GracePeriodInv1-2).gif "multiplePmtTolRules(GracePeriodInv1-2)")  

(1) si el pago no se produce en estos intervalos, todos los movimientos de liquidación se cierran con o sin tolerancia..  

(2) si el pago no se produce en estos intervalos, ningún movimiento de liquidación se puede cerrar aunque tenga tolerancia.  

#### <a name="4-payment-date-is-between-012103-and-012203-scenarios-22-27"></a>(4) La fecha de pago está comprendida entre 21/01/03 y 22/01/03 (ejemplos 22 a 27)  
Importe pendiente por  

Reglas de liquidación normales  

![Reglas de tolerancia de pagos múltiples (período de gracia)](media/multiplePmtTolRules(GracePeriodInv2).gif "multiplePmtTolRules(GracePeriodInv2)")  

(1) si el pago no se produce en estos intervalos, todos los movimientos de liquidación se cierran con o sin tolerancia..  

(2) si el pago no se produce en estos intervalos, ningún movimiento de liquidación se puede cerrar aunque tenga tolerancia.  

#### <a name="5-payment-date-is-after-012203-scenarios-28-30"></a>(5) la fecha de pago es posterior a 22/01/03 (ejemplos 28 a 30)  
Importe pendiente por  

Reglas de liquidación normales  

![Reglas de tolerancia de pagos múltiples (después del 22/01)](media/multiplePmtTolRules(Post0122).gif "multiplePmtTolRules(Post0122)")  

(1) si el pago no se produce en estos intervalos, todos los movimientos de liquidación se cierran con o sin tolerancia..  

(2) (2) si el pago no se produce en estos intervalos, ningún movimiento de liquidación se puede cerrar aunque tenga tolerancia.

## <a name="see-also"></a>Consulte también  
[Finanzas](finance.md)  
[Configurar las finanzas](finance-setup-finance.md)  
[Administrar cobros](receivables-manage-receivables.md)  
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

