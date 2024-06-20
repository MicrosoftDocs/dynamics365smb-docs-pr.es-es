---
title: Configurar términos de pago
description: Utilice los términos de pago para la gestión de las fechas de vencimiento y los descuentos de pago.
author: brentholtorf
ms.topic: conceptual
ms.search.form: '4,'
ms.date: 09/05/2023
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# <a name="set-up-payment-terms"></a>Configurar términos de pago

Los términos de pago determinan cómo administra las fechas de vencimiento y los descuentos de pago. Puede configurar un número ilimitado de términos de pago y utilizar fórmulas de fecha para definirlos. Cuando se registra por primera vez para [!INCLUDE [prod_short](includes/prod_short.md)], la empresa de demostración ofrece algunos métodos de pago que las empresas suelen utilizar. Sin embargo, puede agregar tantas como necesite.  

Si asigna términos de pago a clientes y proveedores, siempre se utilizan los mismos términos en los documentos de compras y ventas que cree para ellos. Las fechas de los documentos de compra y venta, no sus fechas de contabilización, se utilizan para calcular las fechas de vencimiento de los pagos. Si es necesario, puede cambiar los términos del documento de compra o venta, por ejemplo, si desea que un cliente en particular le pague dentro de los 7 días en lugar de los 14 días predeterminados. Cambiar los términos del documento no cambia el plazo de pago predeterminado asignado al cliente. Los mismos términos de pago están disponibles para documentos de venta y compra.

Cuando publica una factura, [!INCLUDE [prod_short](includes/prod_short.md)] calcula los descuentos de pago en función de las condiciones de pago. La fecha de descuento de pago es la útlima fecha en la que el cliente puede obtener un descuento. La fecha también se calcula cuando contabiliza una factura.  

Del mismo modo, cuando publica una nota de crédito, [!INCLUDE [prod_short](includes/prod_short.md)] calcula los descuentos de pago en función de las condiciones de pago. Calcula el descuento en notas de abono según los mismos principios que los descuentos en facturas. Cuando aplica una nota de crédito a una factura, [!INCLUDE [prod_short](includes/prod_short.md)] reduce el monto del descuento de la factura por el monto de descuento de la nota de crédito.  

Si desea enviar a sus clientes recordatorios de pagos vencidos, debe configurar niveles y términos de recordatorio. Para obtener más información sobre los recordatorios, vaya a [Configurar términos y niveles de recordatorios](finance-setup-reminders.md).  

## <a name="to-set-up-payment-terms"></a>Para configurar términos de pago

1. Elija el icono ![Bombilla que abre la característica Dígame](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Términos de pago** y luego elija el enlace relacionado.  
2. Rellene los campos según sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

Después de definir los términos de pago, asígnelos a clientes y proveedores. Opcionalmente, asigne condiciones de pago a sus métodos de pago.  

> [!TIP]
> En la versión base de [!INCLUDE [prod_short](includes/prod_short.md)], no se admiten condiciones de pago con pagos parciales. En su lugar, debe utilizar la función de prepagos. Para obtener más información sobre los prepagos, vaya a [Configurar prepagos](finance-set-up-prepayments.md).
>
> En algunos países o regiones, *puede* establecer condiciones de pago con pagos parciales. Para saber si esta capacidad es compatible en su país o región, vaya a la sección **Funcionalidad local** en la tabla de contenido en el lado izquierdo de un artículo de [Microsoft Learn](about-localization.md).

## <a name="see-also"></a>Consulte también

[Configurar formas de pago](finance-payment-methods.md)  
[Configurar prepagos](finance-set-up-prepayments.md)  
[Configurar las finanzas](finance-setup-finance.md)  
[Permite registrar nuevos clientes](sales-how-register-new-customers.md)  
[Permite registrar nuevos proveedores](purchasing-how-register-new-vendors.md)  
[Ccial](sales-manage-sales.md)  
[Compras](purchasing-manage-purchasing.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
