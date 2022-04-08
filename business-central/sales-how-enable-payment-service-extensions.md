---
title: Permitir los pagos de clientes con servicios de pago
description: Facilite a los clientes el pago de las facturas habilitando servicios de pago.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: online payment
ms.search.forms: 1060, 1061, 1062
ms.date: 06/25/2021
ms.author: edupont
ms.openlocfilehash: 872b261e482a1d54839443f02a25fac8f191855c
ms.sourcegitcommit: 8a12074b170a14d98ab7ffdad77d66aed64e5783
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 03/31/2022
ms.locfileid: "8520713"
---
# <a name="enable-customer-payments-through-payment-services"></a>Permitir los pagos de clientes mediante servicios de pago
Como alternativa a cobrar pagos a través de transferencia bancaria o tarjetas de crédito, los clientes pueden pagarle a través de su cuenta en servicios de pago, como PayPal o WorldPay.  

Al habilitar un servicio de pago en [!INCLUDE[prod_short](includes/prod_short.md)], hay disponible un vínculo al servicio en los documentos de venta que envíe por correo electrónico a los clientes. Los clientes pueden utilizar el vínculo para ir al servicio de pago y pagar la factura, directamente desde el documento de venta. Si no desea incluir el vínculo, por ejemplo, si un cliente paga en efectivo, puede quitar el servicio de pago de la factura antes de registrarla.  

Las extensiones Paypal Payments Standard y WorldPay Payments Standard están instaladas en [!INCLUDE[prod_short](includes/prod_short.md)] y están preparadas para que las habilite.  

## <a name="to-enable-a-payment-service-in-prod_short"></a>Para activar un servicio de pago en [!INCLUDE[prod_short](includes/prod_short.md)]
1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Servicios de pago** y luego elija el enlace relacionado.  
2. En la página **Servicios de pago**, seleccione la acción **Nuevo**.  
3. Seleccione el servicio de pago y luego cierre la página.  
4. En la página **Servicios de pago**, seleccione la acción **Configuración**.  
5. Rellene los campos según sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
6. Cierre la página.  

## <a name="to-select-a-payment-service-on-a-sales-invoice"></a>Para seleccionar un servicio de pago en una factura de ventas
1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Facturas venta** y luego elija el enlace relacionado.  
2. Abra la factura de venta que desee pagar mediante el servicio de pago.  
3. En el campo **Servicio de pago**, elija el servicio de pago.  

    > [!NOTE]  
    > El campo **Servicio de pago** solo está disponible si ha activado el servicio de pago.  

## <a name="see-also"></a>Consulte también  
[Configuración de ventas](sales-setup-sales.md)  
[Ccial](sales-manage-sales.md)  
[Personalizar [!INCLUDE[prod_short](includes/prod_short.md)] con extensiones](ui-extensions.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]