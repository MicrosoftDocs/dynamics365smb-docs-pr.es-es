---
title: Definir una directiva de publicación de facturas para usuarios
description: Utilice directivas de registro de facturas para controlar si un usuario puede registrar facturas de compra y venta.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.topic: conceptual
ms.date: 03/09/2023
ms.custom: bap-template
ms.search.forms: '119, 9807,'
---

# <a name="define-an-invoice-posting-policy-for-users"></a><a name="define-an-invoice-posting-policy-for-users"></a><a name="define-an-invoice-posting-policy-for-users"></a><a name="define-an-invoice-posting-policy-for-users"></a>Definir una directiva de registro de facturas para usuarios

Las empresas a menudo tienen procesos únicos para contabilizar envíos y facturas de compra y venta. Por ejemplo, los procesos pueden variar desde una persona que registra todo en un pedido de compra hasta varios empleados. Puede impedir que los usuarios registren facturas o solicitar que las facturas se registren junto con los envíos o las recepciones.

## <a name="to-specify-a-posting-policy"></a><a name="to-specify-a-posting-policy"></a><a name="to-specify-a-posting-policy"></a><a name="to-specify-a-posting-policy"></a>Para especificar una directiva de registro

En la página **Configuración de usuario**, en los campos **Directiva de publicación de facturas de ventas** y **Directiva de publicación de facturas de compras** , elija una de las siguientes opciones:

* **Permitido** (Predeterminado): mantiene el comportamiento actual, donde un usuario puede elegir la opción de publicación que desea usar, como **Enviar**, **Factura** y **Envío y Factura**. 
* **Prohibido**: impide que el usuario registre facturas. Business Central mostrará un cuadro de diálogo de confirmación que proporciona solo las opciones **Enviar** o **Recibir**.
* **Obligatorio**: permite al usuario registrar facturas junto con recibos o envíos. Business Central mostrará un cuadro de diálogo de confirmación con las opciones **Enviar y facturar** o **Recibir y facturar**.

## <a name="effect-on-documents"></a><a name="effect-on-documents"></a><a name="effect-on-documents"></a><a name="effect-on-documents"></a>Efecto en documentos

La siguiente tabla describe cómo las directivas de registro de facturas afectan a los documentos.

|Documento | Opción 1: permitir <br>Muestra una serie de opciones| Opción 2: prohibido <br>Cuadro de diálogo de confirmación | Opción 3: obligatorio <br>Cuadro de diálogo de confirmación|
|--|--|--|--|
|Pedido venta |- Enviar <br>- Facturar <br>- Enviar y facturar |¿Confirma que desea registrar el envío? |¿Confirma que desea registrar el envío y la factura?|
|Pedido devolución venta |- Recibir <br>- Facturar <br>- Recibir y facturar |¿Confirma que desea registrar la recepción? |¿Confirma que desea registrar la recepción y la factura?|
|Picking inventario |- Enviar <br>- Enviar y facturar |¿Confirma que desea registrar el envío? |¿Confirma que desea registrar el envío y la factura?|
|Pedido compra |- Recibir <br>- Facturar <br>- Recibir y facturar |¿Confirma que desea registrar la recepción? |¿Confirma que desea registrar la recepción y la factura?|
|Pedido devolución compra |- Enviar <br>- Facturar <br>- Enviar y facturar |¿Confirma que desea registrar el envío? |¿Confirma que desea registrar el envío y la factura?|
|Ubicación existencias |- Recibir <br>- Recibir y facturar |¿Confirma que desea registrar la recepción? |¿Confirma que desea registrar la recepción y la factura?|
|Envío almacén |- Enviar <br>- Enviar y facturar | ¿Confirma que desea registrar el envío? |¿Confirma que desea registrar el envío y la factura?|

   > [!Note]
   > La configuración no afecta al registro de líneas de diario generales donde puede seleccionar **Factura** en el campo **Tipo de documento**.

## <a name="see-also"></a><a name="see-also"></a><a name="see-also"></a><a name="see-also"></a>Consulte también

[Facturar ventas](sales-how-invoice-sales.md)  
[Registrar compras con facturas de compra y pedidos](purchasing-how-record-purchases.md)  
[Comprar productos para una venta mediante la creación de facturas de compra](purchasing-how-purchase-products-sale.md)
[Preparación para hacer negocios](ui-get-ready-business.md)  
