---
title: Configuración de divisas
description: Debe configurar cada divisa si compra o vende en divisas que no sean la divisa local (DL) o si registra transacciones contables en distintas divisas.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: multiple currencies
ms.search.form: '5, 118'
ms.date: 06/10/2024
ms.service: dynamics-365-business-central
---
# Configuración de divisas

[!INCLUDE [finance-currencies-def](includes/finance-currencies-def.md)]

Utilice un servicio externo para incluir los últimos tipos de cambio de divisa en la lista **Divisas**. Para obtener más información, vea [Para configurar un servicio de tipo de cambio de divisa](finance-how-update-currencies.md#set-up-a-currency-exchange-rate-service).  

[!INCLUDE [finance-currencies-lcy](includes/finance-currencies-lcy-note.md)]

## <a name="curr"></a>Divisas

En la tabla siguiente se describen los campos de la lista **Divisas**.

|Campo|Descripción|  
|---------------------------------|---------------------------------------|  
|**Código**|El identificador de la divisa.|
|**Descripción**|Una descripción en texto libre de la divisa.|
|**Código ISO**|El código internacional de tres letras para la divisa definida en ISO 4217.|
|**Código numérico ISO**|La referencia numérica internacional para la divisa definida en ISO 4217.|
|**Fecha de tipo cambio**|La última fecha del tipo de cambio real.|
|**Divisa UME**|Especifica si la moneda es una moneda de la UEM (Unión Económica y Monetaria), como el EUR.|
|**Cta. dif. pos. realizadas**|La cuenta donde se contabiliza la ganancia real cuando reciba pagos por cuentas por cobrar o registre el tipo de cambio real en los pagos a cuentas por pagar. Para ver un ejemplo de una transacción de divisa por cobrar, vea el ejemplo debajo de esta tabla. |
|**Cta. dif. pos. realizadas**|La cuenta donde se contabiliza la pérdida real cuando reciba pagos por cuentas por cobrar o registre el tipo de cambio real en los pagos a cuentas por pagar. Para ver un ejemplo de una transacción de divisa por cobrar, vea el ejemplo debajo de esta tabla. |
|**Cta. aj. pos. CG no realizados**|La cuenta donde se contabiliza la ganancia teórica cuando realice un ajuste de divisa.|
|**Cta. dif. pos. no realizadas**|La cuenta donde se contabiliza las pérdidas teóricas cuando realice un ajuste de divisa.|
|**Prec. redondeo importe**|Algunas divisas tienen otros formatos para los importes de las facturas que se definen en la página **Configuración de contabilidad**. Si cambia la precisión del redondeo de importes para una divisa, todos los importes de las facturas en esa divisa se redondean con la precisión actualizada.|
|**N.º decimales para importes**|Algunas divisas tienen otros formatos para los importes de las facturas que se definen en la página **Configuración de contabilidad**. Si cambia los puestos decimales del importe para una divisa, todos los importes de las facturas en esa divisa se redondean con los decimales actualizados|
|**Tipo redondeo factura**|Especifica el método a utilizar si los importes deben redondearse. Las opciones son **Más cercano**, **Hacia arriba**, y **Hacia abajo**.|
|**Precisión de redondeo precio unitario**|Algunas divisas tienen otros formatos para los importes unitarios que se definen en la página **Configuración de contabilidad**. Si cambia la precisión del redondeo de importes de la unidad, todos los importes de la unidad en la divisa se redondean con la precisión actualizada.|
|**N.º decimales para precio-prod.**|Algunas divisas tienen otros formatos para los importes unitarios que se definen en la página **Configuración de contabilidad**. Si cambia los puestos decimales del importe de la unidad todos los importes de la unidad en esa divisa se redondean con los decimales actualizados.|
|**Precisión redondeo liquidación**|Especifica el tamaño del intervalo que se permite como diferencia de redondeo cuando se liquiden movimientos entre sí en distintas divisas.|
|**Conversión DL redondeo. Cuenta débito**|Especifica la información de conversión que debe contener también una cuenta de débito si desea insertar líneas de corrección para las diferencias de redondeo en los diarios generales mediante la acción **Insertar lín. conv. redon. DL**.|
|**Conversión DL redondeo. Cuenta crédito**|Especifica la información de conversión que debe contener también una cuenta de crédito si desea insertar líneas de corrección para las diferencias de redondeo en los diarios generales mediante la acción **Insertar lín. conv. redon. DL**.|
|**Fecha últ. ajuste divisas**|La fecha del último ajuste de la divisa.|
|**Fecha últ. modificación**|La fecha del cambio en la configuración de la divisa.|
|**% tolerancia pago**|El porcentaje máximo de tolerancia de pago % establecido para esta divisa. Para obtener más información, consulte [Tolerancia de pago y tolerancia de descuento por pronto pago](finance-payment-tolerance-and-payment-discount-tolerance.md). |
|**Máx. importe tolerancia pago**|El importe máximo de tolerancia de pago % establecido para esta divisa. Para obtener más información, consulte [Tolerancia de pago y tolerancia de descuento por pronto pago](finance-payment-tolerance-and-payment-discount-tolerance.md). |
|**Factor divisa**|Especifica la relación entre la divisa y la divisa local utilizando el tipo de cambio real.|
|**Cta. aj. pos. C/G realizados**|Especifica la cuenta que se utiliza para registrar beneficios del tipo de cambio para los ajustes de divisa entre la divisa local (DL) y la divisa adicional para informes. Los beneficios del tipo de cambio se calculan cuando se ejecuta el trabajo por lotes Ajustar tipos de cambio para ajustar las cuentas de contabilidad. Es posible que este campo no esté visible de forma predeterminada. Se puede recuperar personalizando la página.|
|**Cta. aj. neg. C/G realizados**|Especifica la cuenta que se utiliza para registrar pérdidas del tipo de cambio para los ajustes de divisa entre la divisa local (DL) y la divisa adicional para informes. Los beneficios del tipo de cambio se calculan cuando se ejecuta el trabajo por lotes Ajustar tipos de cambio para ajustar las cuentas de contabilidad. Es posible que este campo no esté visible de forma predeterminada. Se puede recuperar personalizando la página.|
|**Cta. aj. residual pos.**|Especifica la cuenta que se utiliza para registrar importes de ganancias residuales (diferencias de redondeo) cuando se utiliza una divisa de informe adicional en el área de aplicación de la contabilidad. Es posible que este campo no esté visible de forma predeterminada. Se puede recuperar personalizando la página.|
|**Cta. aj. residual neg.**|Especifica la cuenta que se utiliza para registrar importes de pérdidas residuales (diferencias de redondeo) cuando se utiliza una divisa de informe adicional en el área de aplicación de la contabilidad. Es posible que este campo no esté visible de forma predeterminada. Se puede recuperar personalizando la página.|
|**Máx. diferencia IVA permitida**|El importe máximo permitido por diferencias de IVA en esta divisa. Para obtener más información, consulte [Corrección manual de los importes del IVA en los documentos de ventas y compras](finance-work-with-vat.md#correcting-vat-amounts-manually-on-sales-and-purchase-documents). Es posible que este campo no esté visible de forma predeterminada. Se puede recuperar personalizando la página.|
|**Tipo redondeo IVA**|Especifica el método de redondeo para corregir los importes de IVA manualmente en los documentos de compra y venta. Es posible que este campo no esté visible de forma predeterminada. Se puede recuperar personalizando la página.|

### Funciones de divisa disponibles

La siguiente tabla describe las acciones clave en la página **Divisas**.  

|Menú|Acción|Descripción|
|-------------|--------------|------------------------------|
|**Procesar**|**Sugerir cuentas**|Utilice cuentas de las otras divisas. Se insertan las cuentas más utilizadas.|
||**Cambiar tolerancia pagos**|Cambia la tolerancia de pago máxima o el porcentaje de tolerancia de pago o ambos y filtra por divisa. Para obtener más información, consulte [Tolerancia de pago y tolerancia de descuento por pronto pago](finance-payment-tolerance-and-payment-discount-tolerance.md).|
||**Tipos de cambio**|Permite ver los tipos de cambio actualizados de las divisas que se utilizan.|
||**Ajustar tipos de cambio**|Actualice los saldos de los asientos del libro mayor, de clientes, de proveedores y de cuentas bancarias. La actualización es útil si el tipo de cambio cambió después de que se publicaron las entradas.|
||**Registro de ajuste de tipo de cambio**|Ver los resultados de haber ejecutado el trabajo por lotes **Ajustar tipos de cambio**. Se crea una línea para cada divisa de cada combinación de grupo contable y divisa que se incluya en el ajuste.|
|**Servicio de tipo de cambio**|**Servicio de tipo de cambio**|Permite ver o editar la configuración de los servicios configurados para recuperar los tipos de cambio actualizados cuando se elige la acción **Actualizar tipos de cambio**.|
||**Actualizar tipos de cambio**|Permite obtener los tipos de cambio de divisa más recientes de un proveedor de servicios.|
|**Informes**|**Saldo divisas extranjeras**|Ver los saldos de todos los clientes y los proveedores en divisa extranjera y en la moneda local (DL). El informe muestra dos saldos DL. Uno es el saldo de divisa extranjera convertido a DL utilizando el tipo de cambio en el momento de la transacción. El otro es el saldo de divisa extranjera convertido a DL utilizando el tipo de cambio del día.|

## DL y otras divisas

[!INCLUDE [finance-currencies-lcy-def](includes/finance-currencies-lcy-def.md)]

## Redondeo de divisas

Para administrar las divisas que no utilizan decimales y evitar su uso innecesario en las divisas extranjeras, puede utilizar dos funciones de redondeo diferentes:

- Redondeo precio-producto  

- Redondeo de importe  

Estas funciones pueden utilizarse de forma independiente o combinarse entre sí. También pueden utilizarse con la función de redondeo de facturas.

A diferencia de las funciones de redondeo de facturas, las funciones de redondeo de importe y precio-producto sólo afectan a los importes en divisas extranjeras-no a los importes correspondientes en divisas locales. Estas dos características no contabilizan nada en las cuentas de contabilidad general. Así pues, no es necesario especificar ninguna cuenta en los grupos contables ni en ninguna otra sección.

### Redondeo precio-producto

La característica de redondeo precio-producto controla el modo en que se redondean los precios de venta de los productos y recursos en divisas extranjeras en las líneas de venta y compra. Debe especificar las reglas para cada divisa de forma independiente, en el campo **Prec. redondeo precio-prod.** de la lista **Divisas**.

La característica de redondeo precio-producto se utiliza de forma automática cada vez que introduce un número de producto o de recurso en una línea de ventas. Si la factura corresponde a un cliente con un código de divisa, el precio del producto o recurso se convierte a la divisa del cliente. El precio se redondea según el valor de precisión de redondeo precio-producto especificado para la divisa.

### Redondeo de importe

La característica de redondeo de importe controla el modo en que se redondean los importes en divisas extranjeras en las líneas del diario general, las líneas de ventas y las líneas de compras. Debe especificar las reglas para cada divisa de forma independiente en el campo **Prec. redondeo importe** de la lista **Divisas**.

Los importes en divisas extranjeras se redondean cuando se rellenan y registran líneas de diarios generales, líneas de ventas y líneas de compras.

## Tipos de cambio

Puede registrar tipos de cambio para cada divisa extranjera y especificar a partir de qué fechas se aplicarán estos tipos de cambio. Por ejemplo, puede especificar tipos de cambio diarios, mensuales o trimestrales para cada divisa extranjera.

Puede mantener tipos de cambio históricos en la página **Tipos cambio divisa** para utilizarlos como referencia. Cuando necesite actualizar los tipos de cambio, puede utilizar el botón **Actualizar tipos de cambio** para obtener los últimos tipos de cambio de un proveedor de servicios externo.

## Cuentas contables

No es posible vincular códigos de divisa a las cuentas contables debido a que los importes de dichas cuentas se muestran en la divisa local. Si tiene un préstamo bancario en dólares estadounidenses y efectúa un ingreso en una cuenta bancaria en coronas suecas, deberá configurar sus cuentas bancarias en dólares estadounidenses y en coronas suecas para poder realizar su seguimiento. Mediante los grupos contables, puede vincular las cuentas a las cuentas contables correspondientes. En la contabilidad, el valor de los importes se muestra en la divisa local.

Puede especificar un código de divisa en una línea de un diario general y registrar dicha línea en una cuenta contable. El tipo de cambio correspondiente se utilizará para convertir el importe a la divisa local antes de que se registre en la cuenta contable.  

## Ejemplo de una transacción de divisa por cobrar

[!INCLUDE [finance-currencies-example](includes/finance-currencies-example.md)]

## Consulte también

[Actualizar tipos de cambio de divisa](finance-how-update-currencies.md)  
[Configurar una divisa de informes adicional](finance-how-setup-additional-currencies.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
