---
title: Configurar términos de pago
description: En la versión básica de Business Central, utilice las condiciones de pago para administrar las fechas de vencimiento y los descuentos de pago.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 10ae5c1932e21b452efd41a1212f1840101a277b
ms.sourcegitcommit: a7cb0be8eae6ece95f5259d7de7a48b385c9cfeb
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 07/08/2021
ms.locfileid: "6437321"
---
# <a name="set-up-payment-terms"></a>Configurar términos de pago

Los términos de pago determinan cómo administra las fechas de vencimiento y los descuentos de pago. Puede configurar un número ilimitado de términos de pago y utilizar fórmulas de fecha para definirlos. Cuando se registra por primera vez para [!INCLUDE [prod_short](includes/prod_short.md)], la empresa de demostración ofrece algunos métodos de pago que las empresas suelen utilizar. Sin embargo, puede agregar tantas como necesite.  

Puede asignar términos de pago a clientes y proveedores para que siempre se utilice los mismos términos en los documentos de compras y ventas que cree para ellos. Si es necesario, puede cambiar los términos del documento de compra o venta, por ejemplo, si desea que un cliente en particular le pague dentro de los 7 días en lugar de los 14 días predeterminados. Esto no cambia el término de de pago predeterminado asignado al cliente. Los mismos términos de pago están disponibles para documentos de venta y compra.

Luego, cuando publica una factura, [!INCLUDE [prod_short](includes/prod_short.md)] calcula los descuentos de pago en función de las condiciones de pago. La fecha del descuento por pronto pago, es decir, la última fecha en la que el cliente puede pagar y recibir un descuento en el pago, también será calculada en aquella época.  

Del mismo modo, cuando publica una nota de crédito, [!INCLUDE [prod_short](includes/prod_short.md)] calcula los posibles descuentos de pago en función de las condiciones de pago. El descuento por pronto pago en abonos se calcula según los mismos principios que los descuentos por pronto pago en facturas. Cuando se aplica un abono a una factura, el importe del posible descuento por pronto pago de la factura se reducirá restando el importe de descuento por pronto pago del abono.  

Si desea enviar a sus clientes recordatorios de pagos vencidos, debe configurar niveles y términos de recordatorio. Para más información, ver [Configurar términos y niveles de recordatorio](finance-setup-reminders.md).  

## <a name="to-set-up-payment-terms"></a>Para configurar términos de pago

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Términos de pago** y luego elija el enlace relacionado.  
2. Rellene los campos según sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

Después de definir los términos de pago, asígnelos a clientes y proveedores. Opcionalmente, asigne condiciones de pago a sus métodos de pago.  

> [!TIP]
> En la versión base de [!INCLUDE [prod_short](includes/prod_short.md)], no se admiten condiciones de pago con pagos parciales. En su lugar, debe utilizar la función de prepagos. Para obtener más información, consulte [Configurar prepagos](finance-set-up-prepayments.md).
>
> En ciertos países o regiones, *pueden* establecer condiciones de pago con pagos parciales. Para saber si esta capacidad es compatible en su país o región, consulte la sección **Funcionalidad local** en el panel de navegación en el lado izquierdo en el sitio [Docs.microsoft.com](about-localization.md).

## <a name="see-also"></a>Consulte también

[Configure formas de pago](finance-payment-methods.md)  
[Configurar prepagos](finance-set-up-prepayments.md)  
[Configurar las finanzas](finance-setup-finance.md)  
[Permite registrar nuevos clientes](sales-how-register-new-customers.md)  
[Permite registrar nuevos proveedores](purchasing-how-register-new-vendors.md)  
[Ccial](sales-manage-sales.md)  
[Compras](purchasing-manage-purchasing.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]