---
title: Uso de la extensión PayPal Payments Standard
description: Este artículo describe cómo utilizar la extensión estándar para permitir a clientes realizar pagos con PayPal.
author: brentholtorf
ms.author: bholtorf
ms.topic: conceptual
ms.search.keywords: 'app, add-in, manifest, customize'
ms.search.form: '1070, 1071, 1073, 1074'
ms.date: 07/09/2024
ms.custom: bap-template
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# Extensión PayPal Payments Standard

La extensión PayPal Payments Standard puede ayudarle a aumentar sus niveles de servicio al cliente al facilitarles el pago de sus facturas.

Como alternativa al cobro de pagos mediante transferencia bancaria o crédito Tarjetas, los clientes pueden pagar a través de su cuenta PayPal. Cuando envía una factura de venta por correo electrónico, hay un vínculo de PayPal en el cuerpo del correo electrónico y en el documento PDF adjunto. Si el cliente elige vincular, se abre la página de servicio de su cuenta PayPal y muestra los detalles de pago. El cliente podrá pagar la factura como cualquier otro pago de PayPal.

El servicio Paypal Payments Standard proporciona las ventajas siguientes:

* Los pagos del cliente llegan más rápido a su cuenta bancaria.
* El cliente tiene más formas de pagar la factura.
* PayPal ofrece un servicio de pago de confianza que los clientes prefieren para introducir la información de su tarjeta de crédito en sitios web.
* PayPal ofrece varias maneras de gestionar los pagos, incluido el procesamiento de tarjetas de crédito, cuentas de PayPal y otros orígenes.
* El vínculo de PayPal se puede agregar automáticamente a documentos de ventas o lo puede agregar el usuario de forma manual.
* El servicio Paypal Payments Standard no conlleva tarifas mensuales ni tarifas de instalación.
* Como es una extensión, puede habilitar el servicio Paypal Payments Standard fácilmente si su empresa lo requiere.  

Para obtener más información sobre cómo configurar la extensión, vaya a [Habilitar el pago del cliente a través de PayPal](sales-how-enable-payment-service-extensions.md).

## Registre pagos automáticamente para cuentas comerciales

[!INCLUDE [prod_short](includes/prod_short.md)] Puede registrar pagos automáticamente si tiene una cuenta de comerciante comercial para la plataforma de comercio de PayPal. Cuando sus clientes utilizan PayPal vincular para pagar una factura, [!INCLUDE [prod_short](includes/prod_short.md)] publica las entradas y cierra el documento.

Para utilizar esta capacidad, en la página **Configuración de registro de pagos** en [!INCLUDE [prod_short](includes/prod_short.md)], active **Registrar pagos automáticamente.** alterne y verifique las cuentas que utilizará para los pagos. Si decide que no desea registrar pagos automáticamente, puede desactivarlo nuevamente.

> [!TIP]
> Los desarrolladores pueden utilizar cuentas sandbox para probar la configuración. Para hacerlo, cambie la URL de PayPal a **sandbox.paypal.com**. [!INCLUDE [prod_short](includes/prod_short.md)] utiliza la Notificación de pago instantáneo (IPN) de PayPal a través de notify_url.

## Consulte también

[Personalizar [!INCLUDE[prod_short](includes/prod_short.md)] con extensiones](ui-extensions.md)  
[Configuración de ventas](sales-setup-sales.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
