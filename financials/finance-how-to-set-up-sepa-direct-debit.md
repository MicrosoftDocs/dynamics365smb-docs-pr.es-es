---
title: Configurar adeudo directo SEPA | Documentos de Microsoft
description: "Información sobre cómo configurar el adeudo directo SEPA en Finance and Operations, Business edition."
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/21/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 28958f1f090e5adad69cb21d30727fcbd6a7fef8
ms.contentlocale: es-es
ms.lasthandoff: 03/22/2018

---
# <a name="set-up-sepa-direct-debit"></a>Configuración de domiciliaciones de adeudo directo SEPA
Desde la ventana **Cobros por adeudo directo** puede exportar instrucciones al banco electrónico para realizar recaudar un adeudo directo desde el banco del cliente a su cuenta bancaria. [!INCLUDE[d365fin](includes/d365fin_md.md)] admite el formato de adeudo directo SEPA, pero en su país o región, es posible que haya otros formatos para pagos electrónicos.  

Para habilitar la exportación de formatos de archivos bancarios no compatibles originales en [!INCLUDE[d365fin](includes/d365fin_md.md)], puede configurar una definición de intercambio de datos mediante el marco de intercambio de datos. Para obtener más información, vea [Configurar las definiciones de intercambio de datos](across-how-to-set-up-data-exchange-definitions.md).  

Para poder procesar pagos de clientes electrónicamente exportando instrucciones de adeudo directo en formato de adeudo directo SEPA, debe realizar los pasos de configuración siguientes:  

* Configure el formato de exportación del archivo bancario que indica a su banco que debe recaudar un adeudo directo desde el banco del cliente a cuenta bancaria.  
* Configure la forma de pago del cliente.  
* Establezca la orden de adeudo directo que refleja el acuerdo con el cliente para cobrar sus pagos en un período de acuerdo determinado.  

### <a name="to-set-up-your-bank-account-for-sepa-direct-debit"></a>Configuración del banco para adeudo directo SEPA  
1. En el cuadro **Buscar**, escriba **Cuentas bancarias** y, a continuación, elija el vínculo relacionado.  
2. Abra el banco que desea utilizar para el adeudo directo.  
3. En la ficha desplegable **Transferencia**, en el campo **Formato exportación de adeudo directo SEPA**, elija la opción para adeudo directo SEPA.  

### <a name="to-set-up-the-customers-payment-method-for-sepa-direct-debit"></a>Configuración de la forma de pago del cliente para adeudo directo SEPA  
1. En el cuadro **Buscar**, escriba **Formas de pago** y, a continuación, elija el vínculo relacionado.  
2. Seleccione la acción **Nuevo**.  
3. Configure una forma de pago. Rellene los campos específicos del adeudo directo tal como se describe en la tabla siguiente.  

    |Campo|Descripción|  
    |---------------------------------|---------------------------------------|  
    |**Adeudo directo**|Especifique si la forma de pago es para el cobro por adeudo directo SEPA.|  
    |**Código términos pago adeudo directo**|Especifique los términos de pago, tal como NO PAGAR, que se muestran en las facturas de venta que paguen mediante adeudo directo SEPA para indicar al cliente que el pago se cobrará automáticamente. Como alternativa, deje el campo en blanco.|  

    > [!NOTE]  
    >  No especifique ningún valor en el campo **Bal. Nº cuenta**.  

4. Elija el botón **Aceptar** para cerrar la ventana **Métodos pago**.  
5. En el cuadro **Buscar**, escriba **Clientes**, y a continuación, elija el vínculo relacionado.  
6. Abra la ficha del cliente que desee configurar para los cobros por adeudo directo SEPA.  
7. Elija el campo **Código método pago** y seleccione el código de la forma de pago que especificó en el paso 3.  
8. Repita los pasos 6 a 7 para todos los clientes que desea configurar para el cobro por adeudo directo SEPA.  

#### <a name="to-set-up-the-direct-debit-mandate-that-represents-the-customer-agreement"></a>Configuración de la orden de domiciliación de adeudo directo que representa el acuerdo del cliente  
1. En el cuadro **Buscar**, escriba **Clientes**, y a continuación, elija el vínculo relacionado.  
2. Abra la ficha del cliente que desee configurar para adeudos directos SEPA.  
3. Elija la acción **Cuentas bancarias**.  
4. En la ventana **Lista bancos cliente**, seleccione el banco de cliente que utilizará domiciliaciones y, a continuación, en la pestaña **Inicio**, en el grupo **Procesara**, elija **Órdenes de domiciliación de adeudo directo**.  
5. En la ventana **Órdenes de domiciliación de adeudo directo SEPA**, rellene los campos tal como se describe en la tabla siguiente.  

    |Campo|Descripción|  
    |---------------------------------|---------------------------------------|  
    |**Código banco cliente**|Especifica el banco desde el que se cobran los pagos por domiciliación. Este campo se rellena automáticamente.|  
    |**Válido desde**|Especifique la fecha en que inicia la orden de domiciliación de adeudo directo.|  
    |**Válido hasta**|Especifique la fecha en que finaliza la orden de domiciliación de adeudo directo.|  
    |**Fecha de firma**|Especifique la fecha en que el cliente firmó la orden de domiciliación de adeudo directo.|  
    |**Tipo de pago**|Especifica si el contrato cubre varios (**Pago recurrente**) cobros por adeudo directo o uno solo (**Pago único**).|  
    |**Número de debe esperado**|Especifica el número de cobros por adeudo directo que espera efectuar. Este campo solo es pertinente si ha seleccionado **Pago recurrente** en el campo **Tipo de pago**.|  
    |**Contador debe**|Especifica el número de cobros por adeudo directo que se realizaron con esta orden de domiciliación de adeudo directo. Este campo se actualiza automáticamente.|  
    |**Bloqueado**|Especifique que los cobros por adeudo directo no se pueden realizar con esta orden de domiciliación de adeudo directo.|  

6.  Repita los pasos 1 a 5 para todos los clientes que desea configurar para adeudos directos SEPA.  

 La orden de domiciliación de adeudo directo se inserta automáticamente en el campo **Id. de orden de domiciliación** de adeudo directo cuando se crea una factura de venta para el cliente que ha seleccionado en el paso 2. Para obtener más información, vea [Crear líneas de ventas y de compras periódicas](sales-how-work-standard-lines.md).  

## <a name="see-also"></a>Consulte también  
[Cobro de pagos mediante adeudo directo SEPA](finance-collect-payments-with-sepa-direct-debit.md)  
[Configurar las definiciones de intercambio de datos](across-how-to-set-up-data-exchange-definitions.md)
[Crear líneas de ventas y de compras periódicas](sales-how-work-standard-lines.md)
[Intercambio de datos electrónicamente](across-data-exchange.md)

