---
title: Sincronizar transacciones y pagos
description: Configure y ejecute la importación de transacciones y pagos desde Shopify.
ms.date: 06/06/2023
ms.topic: article
ms.service: dynamics365-business-central
ms.search.form: '30124, 30125, 30130, 30131, 30132, 30133, 30134,'
author: andreipa
ms.author: andreipa
ms.reviewer: bholtorf
---

# <a name="transactions-and-payouts" />Transacciones y pagos

Cuando un cliente completa su pago en la tienda en línea, la información sobre los pagos se guarda como una **Transacción**. Puede haber varias transacciones vinculadas al pedido, como cuando un cliente utiliza una tarjeta de regalo para pagar parte del coste y luego utiliza una tarjeta de crédito o PayPal para el importe restante.

Si utiliza Shopify Payment como proveedor de pagos, además de la información sobre el dinero recibido del cliente por el proveedor de pagos, también puede ver los pagos de Shopify a su cuenta bancaria.

## <a name="transactions" />Transacciones

Las transacciones de pago que tienen lugar en Shopify se sincronizan junto con los pedidos y se pueden ver desde la página **Pedidos de Shopify**.

Para revisar todas las transacciones, elija el icono ![Bombilla que abre la función Dígame 1.](../media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Transacciones**, y luego seleccione el enlace relacionado.

El campo **N.º de factura registrada** puede ser útil en el proceso de conciliación.

Si configuró la asignación de formas de pago, el documento de ventas creado tendrá asignado un Código de forma de pago. Obtenga más información en [Asignación de métodos de pago](#payment-method-mapping).

## <a name="payouts" />Pagos

Si su tienda utiliza Shopify Payment, recibirá los pagos a través de **Pagos de Shopify** cuando un cliente pague utilizando Shopify Payments y finalizaciones de compra aceleradas.

1. Elija el icono ![Bombilla que abre la función Dígame 1.](../media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Tiendas de Shopify** y luego elija el enlace relacionado.
2. Seleccione la tienda para la que desea sincronizar los pagos para abrir la página **Tarjeta de tienda de Shopify**.
3. Seleccione la acción **Sincronizar pagos**.

Para revisar todos los pagos, elija el icono ![Bombilla que abre la función Dígame.](../media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Pagos**, y luego seleccione el enlace relacionado.

Los **pagos** son solo para fines informativos y no afectan a la contabilidad o los movimientos bancarios, aunque pueden ser útiles cuando procesa su estado de cuenta bancaria.

## <a name="payment-method-mapping" />Asignación de método de pago

Para llenar el **Código de método de pago** para documentos de venta importados de Shopify automáticamente, necesita configurar **Asignación de métodos de pago**.

1. Elija el icono ![Bombilla que abre la función Dígame 1.](../media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Tiendas de Shopify** y luego elija el enlace relacionado.
2. Seleccione la tienda para la que desea definir una asignación para abrir la página **Ficha de tienda de Shopify**.
3. Elija la acción **Asignación de métodos de pago**.
4. En los campos **Puerta de enlace** y **Compañía de tarjeta de crédito**, introduzca el nombre del método de pago de Shopify. El registro se crea automáticamente cuando importa pedidos de Shopify.
5. Introduzca el **Código de método de pagoo** con el método de pago correspondiente en [!INCLUDE[prod_short](../includes/prod_short.md)].
6. Seleccione la **Prioridad** para los casos en que el cliente utilice múltiples medios de pago. El método de pago con la prioridad más alta se selecciona en el documento de ventas. Si ambos métodos de pago tienen la misma prioridad, se utiliza el método de pago con el importe más alto.

> [!NOTE]  
> Si el método de pago correspondiente en [!INCLUDE[prod_short](../includes/prod_short.md)] tiene **Tipo contrapartida** y **Bal. Nº cuenta** rellenados, entonces durante la contabilización el sistema de facturas creará un asiento de compensación del tipo *Pago* y lo aplicará al tipo *Factura* en la entrada de movimientos del cliente.

## <a name="use-cases" />Casos de uso
  
Fiestas:

* Comprador - persona que compra bienes en la tienda en línea Shopify.
* Comerciante: identifique a su empresa.
* Proveedor del servicio de pago: empresa que le facilita el procesamiento de pagos. Puede ser Shopify Payments o un tercero.

### <a name="how-money-flows" />Como fluye el dinero

El Comprador compra bienes en la tienda en línea. La última etapa es procesar el pago.

>[!NOTE]
> Este ejemplo no cubre los casos en que el pago se completa fuera de la caja de Shopify, que es válido para escenarios B2B.
  
El Comprador paga con tarjeta de crédito, PayPal o algún método de pago local como MobilePay en Dinamarca. El proveedor de pago toma el monto total del Comprador. En este momento, el dinero de los Compradores se transfiere al Proveedor de pago.

Según el proveedor del servicio de pago, el comerciante puede ver este dinero en su cuenta en el proveedor de servicio de pago, tanto los montos recibidos como las comisiones deducidas. Los proveedores de pago a menudo cobran una comisión por cada transacción y, en algunos casos, también pueden tener una tarifa fija.
  
Según el proveedor de pago, el comerciante activa una transferencia del dinero a su cuenta bancaria (pago) manualmente o automáticamente dentro de un período definido: una vez al día, una vez al mes, etc.
  
Según el banco, el Comerciante puede ver esta transacción entrante en su cuenta bancaria a través de la banca en línea o en el extracto bancario.

Hay varias opciones sobre cómo manejar las transacciones de pago en [!INCLUDE[prod_short](../includes/prod_short.md)]
  
### <a name="option-1-reconcile-incoming-transfers-to-bank-account-against-original-invoices" />Opción 1: conciliar las transferencias entrantes a la cuenta bancaria con las facturas originales
  
El comerciante importa la orden de venta a [!INCLUDE[prod_short](../includes/prod_short.md)] y enviar el envío y la factura.

Resultado: el sistema crea una **Entrada de libro mayor de clientes** de tipo *Factura* con el monto total, **Abierto** está establecido en Sí. El **Importe restante** es igual a la cantidad facturada.

El comerciante importa extractos bancarios utilizando el diario de reconciliación de pagos.

Problemas:

1. Puede ser difícil si hay varias facturas (y notas de crédito), pero un solo pago del proveedor de pago con una suma global.
2. La cantidad generalmente no coincide debido a la comisión. Puede usar la tolerancia de pago o los descuentos de pago para manejar las tarifas.

### <a name="option-2-reconcile-incoming-transfers-to-bank-account-against-interim-account-representing-money-at-the-payment-provider" />Opción 2: conciliar las transferencias entrantes a la cuenta bancaria con la cuenta provisional que representa dinero en el proveedor del servicio de pago
  
El comerciante importa la orden de venta a [!INCLUDE[prod_short](../includes/prod_short.md)] y enviar el envío y la factura.
  
Resultado: el sistema crea una entrada de libro mayor de clientes de tipo **Factura** con el monto total, **Abierto** está establecido en Sí. El **Importe restante** es igual a la cantidad facturada.

Sin embargo, debido a que la orden de venta tiene un código de método de pago donde los campos **Tipo de cuenta bal.** y **Número de cuenta bal.** se completan, el sistema crea automáticamente otro asiento de cliente del tipo **Pago** y lo aplica a la entrada del libro mayor de clientes creada anteriormente.

>[!NOTE]
> El sistema completa el campo Cód. de forma de pago según la asignación del método de pago. Obtenga más información en [Asignación de métodos de pago](#payment-method-mapping).
  
Puede definir cuentas de saldo para métodos de pago de dos maneras:

* **Tipo de cuenta bal.** establecida como *Banco*, y **Nº. cuenta bal** con la cuenta bancaria especial que representa su cuenta en el proveedor de pagos.
* **Tipo de cuenta bal.** establecida como *C/G Cuenta**, y **Nº. cuenta bal** con la cuenta C/G que representa su cuenta en el proveedor del servicio de pago.

Tiene sentido utilizar una cuenta bancaria si el proveedor del servicio de pagos exporta algún tipo de estado de cuenta, que puede importar al diario de conciliación de pagos.

El comerciante importa extractos bancarios utilizando el diario de reconciliación de pagos. El pago entrante se puede procesar:

* Como una transferencia de otro banco. Si la transferencia tarda unos días o implica un cambio de moneda, es posible que desee utilizar una cuenta C/G provisional.
* Como diferencia en la Cuenta C/G que representa su cuenta en el proveedor del servicio de pago.
  
El saldo restante en el C/G o cuenta bancaria que representa su cuenta en el proveedor del servicio de pago se puede cancelar como "Tarifas/Comisiones"

Problemas:

1. Puede crear múltiples cuentas bancarias o C/G si está tratando con múltiples proveedores de pago. Sin embargo, los pedidos de venta en [!INCLUDE[prod_short](../includes/prod_short.md)] admiten solo un código de forma de pago, lo que dificulta la gestión de casos cuando un comprador utiliza múltiples formas de pago para un pedido.

## <a name="see-also" />Consulte también .

[Comenzar con el conector para Shopify](get-started.md)  
