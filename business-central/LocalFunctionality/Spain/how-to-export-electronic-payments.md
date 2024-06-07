---
title: 'Cómo exportar pagos electrónicos [ES]'
description: 'En Business Central, puede utilizar las páginas siguientes para exportar movimientos del diario de pagos a un formato de archivo de acuerdo con cuatro estándares de pago diferentes.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.date: 06/21/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
---

# Exportar pagos electrónicos en la versión en español
En [!INCLUDE[prod_short](../../includes/prod_short.md)], puede exportar movimientos del diario de pagos a un formato de archivo de acuerdo con cuatro estándares de pago diferentes. Utilice las siguientes páginas para exportar según los distintos estándares de pago.  

|Estándar de pago|Página desde la que exportar|  
|----------------------|---------------------------|  
|AEB N34|**Ordenes de pago**|  
|AEB N34.1|**Ordenes de pago**|  
|PAGO ELECTRÓNICO|**Diario de pagos**|  
|SEPA|**Diario de pagos** u **Órdenes pago**|  

> [!IMPORTANT]  
>  Antes de exportar un pago, debe seleccionar un formato de pago en el campo **Formato de exportación de pagos** en la página **Ficha banco**.  

## Para exportar pagos electrónicos mediante la página Órdenes de pago  

1.  Elija el icono ![Bombilla que abre la función Dígame.](../../media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Órdenes pago** y luego elija el enlace relacionado.  
2.  Seleccione los documentos que desea pagar.  
3.  Seleccione la acción **Exportar a archivo**.  

    Los pagos de tipo SEPA se exportarán a un archivo inmediatamente.  

    Los pagos de tipo N34 o N34.1 se exportarán cuando ejecute el informe **Orden pago - Exportar N34** u **Orden pago - Exportar N34.1**, que se muestran automáticamente cuando selecciona **Exportar** en el paso 3.  

4.  En la página **Orden pago - Exportar N34.1**, rellene los campos tal como se describe en la tabla siguiente.  

    |Campo|Description|  
    |---------------------------------|---------------------------------------|  
    |**N.º cuenta bancaria**|Seleccione el código de cuenta desde la que se van a exportar los pagos.|  
    |**Fecha liquidación**|Especifique la fecha en la que la exportación se transmitirá al banco. Esta fecha será la fecha de registro de los movimientos exportados del diario de pagos.|  
    |**Si Fecha registro no coincide con Fecha de emisión**|Especifique si desea que la fecha de liquidación coincida o si desea omitir las líneas de diario de pagos cuya fecha de registro no coincida con la fecha de liquidación.|  
    |**Código gastos**|Especifique el responsable de los gastos de pago.|  
    |**Compartido (sólo transf. internacionales).**|Especifique si desea que el pagador y el beneficiario compartan los gastos. Solo se puede usar en transferencias internacionales.|  
    |**Concepto orden pago.**|Especifique el concepto de orden de pago, **Nómina**, **Nómina pensión** u **Otros**.|  
    |**Relación**|Especifique si desea que el banco le envíe una lista detallada de los cargos por transferencias. Si no selecciona este campo, el banco le enviará el total de todos los cargos de todas las transferencias realizadas.|  
    |**Número copias**|Especifique el número de copias adicionales del aviso de pago que se imprimirán mediante este proceso. Siempre se imprime un documento para que se pueda enviar al beneficiario.|  

5.  Seleccione la acción **Imprimir** o **Vista previa** para ver el archivo de pagos creado.  

    Se exportarán los movimientos del diario de pagos cuyo campo **Tipo pago por banco** esté establecido en **Pago electrónico**. Los datos se exportarán a un archivo con el formato estándar N34 o N34.1. Además, se imprimirá un aviso de pago adecuado para su envío a cada beneficiario.  

    > [!NOTE]  
    >  Solo puede registrar la orden de pago una vez que haya exportado correctamente los pagos electrónicos.  

## Para exportar pagos electrónicos mediante la página Diario de pagos  

1.  Elija el icono ![Bombilla que abre la función Dígame.](../../media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Diarios de pagos** y luego elija el enlace relacionado.  
2.  Seleccione los documentos que desea pagar.  
3.  Elija **Relacionado** > **Pagos** > **Pagos electrónicos** > **Exportar**.  

    Los pagos de tipo SEPA se exportarán a un archivo inmediatamente.  

    Los pagos de tipo E-PAY se exportarán cuando ejecute el informe **Exportar pagos electrónicos**, que se muestran automáticamente cuando selecciona **Exportar** en el paso 3.  

4.  En la página **Exportar pagos electrónicos**, rellene los campos tal como se describe en la tabla siguiente.  

    |Campo|Description|  
    |---------------------------------|---------------------------------------|  
    |**N.º cuenta bancaria**|Seleccione el código de cuenta desde la que se van a exportar los pagos.|  
    |**Fecha liquidación**|Especifique la fecha en la que la exportación se transmitirá al banco. Esta fecha será la fecha de registro de los movimientos exportados del diario de pagos.|  
    |**Si Fecha registro no coincide con Fecha de emisión**|Especifique si desea que la fecha de liquidación coincida o si desea omitir las líneas de diario de pagos cuya fecha de registro no coincida con la fecha de liquidación.|  
    |**Código gastos**|Especifique el responsable de los gastos de pago.|  
    |**Compartido (sólo transf. internacionales).**|Especifique si desea que el pagador y el beneficiario compartan los gastos. Solo se puede usar en transferencias internacionales.|  
    |**Concepto orden pago.**|Especifique el concepto de orden de pago, **Nómina**, **Nómina pensión** u **Otros**.|  
    |**Relación**|Especifique si desea que el banco le envíe una lista detallada de los cargos por transferencias. Si no selecciona este campo, el banco le enviará el total de todos los cargos de todas las transferencias realizadas.|  
    |**Número copias**|Especifique el número de copias adicionales del aviso de pago que se imprimirán mediante este proceso. Siempre se imprime un documento para que se pueda enviar al beneficiario.|  

5.  Seleccione la acción **Imprimir** o **Vista previa** para ver el archivo de pagos creado.  

    Se exportarán los movimientos del diario de pagos cuyo campo **Tipo pago por banco** esté establecido en **Pago electrónico**. Los datos se exportarán a un archivo con el formato estándar del pago seleccionado. Además, se imprimirá un aviso de pago adecuado para su envío a cada beneficiario.  

    > [!NOTE]  
    >  Solo puede registrar la orden de pago una vez que haya exportado correctamente los pagos electrónicos.  

    > [!NOTE]  
    >  En la versión genérica de [!INCLUDE[prod_short](../../includes/prod_short.md)], la página **Diario de pagos** se utiliza de forma similar para exportar pagos electrónicos en el formato de transferencia de crédito SEPA. Para obtener más información, consulte [Hacer pagos con la extensión AMC Banking 365 Fundamentals o Transferencia de crédito SEPA](../../finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md).  

## Para exportar los pagos electrónicos del módulo Cartera  

1.  Elija el icono ![Bombilla que abre la función Dígame.](../../media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Orden pago - Exportar N34.1** y luego elija el enlace relacionado.  
2.  Rellene los campos tal como se describe en la tabla siguiente.  

    |Campo|Description|  
    |---------------------------------|---------------------------------------|  
    |**Fecha de emisión**|Especifique la fecha de entrega de pago electrónico.|  
    |**Código gastos**|Especifique el responsable de los gastos de pago.|  
    |**Concepto orden pago**|Especifique el concepto de orden de pago, **Nómina**, **Nómina pensión** u **Otros**.|  
    |**Relación**|Especifique si desea que el banco le envíe una lista detallada de los cargos por transferencias. Si no selecciona este campo, el banco le enviará el total de todos los cargos de todas las transferencias realizadas.|  
    |**Número copias**|Especifique el número de copias adicionales del aviso de pago que se imprimirán mediante este proceso. Siempre se imprime un documento para que se pueda enviar al beneficiario.|  
    |**Compartido (solo transf. internacionales)**|Especifique si desea que el pagador y el beneficiario compartan los gastos. Solo se puede usar en transferencias internacionales.|  

> [!NOTE]  
>  Solo puede registrar la orden de pago una vez que haya exportado correctamente los pagos electrónicos.  

## Consulte también  
[Pagos electrónicos – AEB N34.1](electronic-payments-aeb-n341.md)  
[Configurar cuentas bancarias para realizar pagos electrónicos](how-to-set-up-bank-accounts-for-electronic-payments.md)  
[Realizar pagos con la extensión AMC Banking 365 Fundamentals o transferencia de crédito SEPA](../../finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md)  


[!INCLUDE[footer-include](../../includes/footer-banner.md)]