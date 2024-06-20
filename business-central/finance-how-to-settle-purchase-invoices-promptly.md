---
title: Liquidar facturas de compra inmediatamente
description: 'Si necesita pagar al proveedor en efectivo o con cheque, puede hacer que se realice el registro correspondiente cuando se registra la factura.'
author: brentholtorf
ms.topic: conceptual
ms.search.form: '51, 9308'
ms.date: 04/01/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# Liquidar facturas de compra inmediatamente

Si necesita pagar al proveedor en efectivo o con cheque, puede registrar el pago cuando registra la factura.  

> [!NOTE]  
> Si paga a menudo facturas de compra en efectivo, con cheque o por transferencia bancaria, se recomienda que configure una forma de pago específica con una cuenta de contrapartida e introduzca la este método en el campo **Forma de pago** de la tarjeta del proveedor. Se inserta automáticamente el número de cuenta de contrapartida en la cabecera de la factura cada vez que se crea una factura nueva. Para obtener más información, consulte [Definición de formas de pago](finance-payment-methods.md).  

## Para liquidar facturas de compra inmediatamente

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Facturas compra** y luego elija el enlace relacionado.  
2. Seleccione la acción **Nuevo**.  
3. Para pagar en efectivo o mediante transferencia bancaria, introduzca el número de cuenta de caja o de banco en el campo **Cuenta contrapartida**.  

> [!IMPORTANT]  
> Los campos **Tipo contrapartida** y **Cuenta contrapartida** no forman parte del formato estándar de la cabecera de factura. Para contabilizar el pago de una factura, debe comunicarse con un socio de Microsoft que pueda agregar los campos en el código.  
>
> Esta personalización solo es necesaria si no especifica cuentas de contrapartida en los métodos de pago, como se describe anteriormente.

## Consulte también

[Administrar pagos](payables-manage-payables.md)  
[Compras](purchasing-manage-purchasing.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]