---
title: Actualizar tipos cambio divisa
description: Realice un seguimiento de los importes en diferentes divisas utilizando códigos de divisa y deje que Business Central le ayude a ajustar los tipos de cambio de los movimientos registrados con un servicio externo.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.search.keywords: multiple currencies, adjust exchange rates
ms.date: 06/03/2021
ms.author: edupont
ms.openlocfilehash: 75f8f3ead0bdf0e09ca2484d1a0c91ee771cb837
ms.sourcegitcommit: 1aab52477956bf1aa7376fc7fb984644bc398c61
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 06/04/2021
ms.locfileid: "6184454"
---
# <a name="update-currency-exchange-rates"></a>Actualizar tipos cambio divisa

Las empresas trabajan en más países o regiones, por lo que es vital que puedan intercambiar y generar información financiera en más de una divisa. La divisa local (DL) se define en la página **Configuración de contabilidad** como se describe en el artículo [Configurar las finanzas](finance-setup-finance.md). Una vez que se ha definido la divisa local (DL), se representará como una divisa en blanco, por lo que cuando el campo **Divisa** esté vacío, significa que la divisa es DL.  

A continuación, debe configurar códigos de divisa para cada divisa que utilice si compra o vende en divisas diferentes a la suya local (DL). También se pueden crear cuentas bancarias utilizando divisas. Es posible registrar transacciones de contabilidad en diferentes divisas, sin embargo, la transacción del contabilidad siempre se contabilizará en la divisa local (DL).

> [!Important]
> No cree el código de divisa local en las páginas **Configuración contabilidad** ni **Divisas**. Esto creará confusión entre la divisa en blanco y el código DL en la tabla de divisas, y es posible que se creen accidentalmente cuentas bancarias, clientes o proveedores, algunos con la divisa en blanco y otros con el código DL.

La contabilidad se configura con la divisa local (DL), pero también se puede configurar para usarla en otra divisa a la que se asigna un tipo de cambio. Mediante la designación de una segunda divisa como la denominada divisa de informes adicional, [!INCLUDE[prod_short](includes/prod_short.md)] registrará automáticamente los importes tanto en la divisa local como en la divisa adicional en todos los movimientos de contabilidad y en otros movimientos, por ejemplo los del IVA. Para obtener más información, vea [Configurar una divisa de informes adicional](finance-how-setup-additional-currencies.md). La moneda de presentación de informes adicional se utiliza con mayor frecuencia para facilitar la presentación de informes financieros a los propietarios que residen en países o regiones que utilizan divisas diferentes a la divisa local (DL).

## <a name="currencies"></a>Divisas

Especifique los códigos de moneda en **Divisas**, incluida la información adicional y los ajustes necesarios para cada código de divisa.

> [!TIP]
> Cree las divisas con el código ISO internacional como código para simplificar el trabajo con la divisa en el futuro.

|Campo|Descripción|  
|---------------------------------|---------------------------------------|  
|**Código**|El identificador de la divisa.|
|**Descripción**|Una descripción en texto libre de la divisa.|
|**Código ISO**|El código internacional de tres letras para la divisa definida en ISO 4217.|
|**Código numérico ISO**|La referencia numérica internacional para la divisa definida en ISO 4217.|
|**Fecha de tipo cambio**|La última fecha del tipo de cambio real.|
|**Divisa UME**|Especifica si la moneda es una moneda de la UEM (Unión Económica y Monetaria), como el EUR.|
|**Cta. dif. pos. realizadas**|La cuenta donde se contabilizará la ganancia real cuando reciba pagos por cuentas por cobrar o registre el tipo de cambio real en los pagos a cuentas por pagar. Para ver un ejemplo de una transacción de divisa por cobrar, vea el ejemplo debajo de esta tabla. |
|**Cta. dif. pos. realizadas**|La cuenta donde se contabilizará la pérdida real cuando reciba pagos por cuentas por cobrar o registre el tipo de cambio real en los pagos a cuentas por pagar. Para ver un ejemplo de una transacción de divisa por cobrar, vea el ejemplo debajo de esta tabla. |
|**Cta. aj. pos. CG no realizados**|La cuenta donde se contabilizará la ganancia teórica cuando realice un ajuste de divisa.|
|**Cta. dif. pos. no realizadas**|La cuenta donde se contabilizará las pérdidas teóricas cuando realice un ajuste de divisa.|
|**Prec. redondeo importe**|Algunas divisas tienen otros formatos para los importes de las facturas que se definen en la página **Configuración de contabilidad**. Si cambia la precisión del redondeo de importes para una divisa, todos los importes de las facturas en esa divisa se redondearán con la precisión actualizada.|
|**N.º decimales para importes**|Algunas divisas tienen otros formatos para los importes de las facturas que se definen en la página **Configuración de contabilidad**. Si cambia los puestos decimales del importe para una divisa, todos los importes de las facturas en esa divisa se redondearán con los decimales actualizados.|
|**Tipo redondeo factura**|Especifica el método a utilizar si los importes deben redondearse. Las opciones son **Más cercano**, **Hacia arriba**, y **Hacia abajo**.|
|**Precisión de redondeo precio unitario**|Algunas divisas tienen otros formatos para los importes unitarios que se definen en la página **Configuración de contabilidad**. Si cambia la precisión del redondeo de importes de la unidad, todos los importes de la unidad en la divisa se redondearán con la precisión actualizada.|
|**N.º decimales para precio-prod.**|Algunas divisas tienen otros formatos para los importes unitarios que se definen en la página **Configuración de contabilidad**. Si cambia los puestos decimales del importe de la unidad todos los importes de la unidad en esa divisa se redondearán con los decimales actualizados.|
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
|**Máx. diferencia IVA permitida**|El importe máximo permitido por diferencias de IVA en esta divisa. Para obtener más información, consulte [Corrección manual de los importes del IVA en los documentos de ventas y compras](finance-work-with-vat.md#correcting-vat-amounts-manually-in-sales-and-purchase-documents). Es posible que este campo no esté visible de forma predeterminada. Se puede recuperar personalizando la página.|
|**Tipo redondeo IVA**|Especifica el método de redondeo para corregir los importes de IVA manualmente en los documentos de compra y venta. Es posible que este campo no esté visible de forma predeterminada. Se puede recuperar personalizando la página.|

### <a name="example-of-a-receivable-currency-transaction"></a>Ejemplo de una transacción de divisa por cobrar

En el siguiente ejemplo, se recibe una factura el 1 de enero con el importe en la divisa de 1000. En ese momento, el tipo de cambio es 1,123.

|Fecha|Acción|Importe divisa|Tipo del documento|Importe en DL del documento|Tipo de ajuste|Importe de ventas no realizadas|Tipo del pago|Importe de pérdidas realizadas|  
|-----|----------|------------|-----------|---------|-----------|-------------|---------|---------|
|1/1|**Factura**|1000|1,123|1123|||||
|1/31|**Ajuste**|1000||1125|1,125|2|||
|2/15|**Reversión de ajuste en el pago**|1000||||-2|||
|2/15|**Pago**|1000||1120|||1,120|-3|

Al final del mes, se realiza un ajuste de la divisa cuando el tipo de la divisa de ajuste se ha establecido en 1,125, lo que genera una ganancia no realizada de 2.

En el momento del pago, el tipo de cambio real registrado en la transacción bancaria muestra un tipo de cambio de 1,120.

Aquí hay una transacción no realizada y, por lo tanto, se revertirá junto con el pago.

Finalmente, se registra el pago y la pérdida real se contabiliza en la cuenta de pérdidas realizadas.

## <a name="available-currency-functions"></a>Funciones de divisa disponibles

La siguiente tabla describe las acciones clave en la página **Divisas**. Algunas de las acciones se explican en las siguientes secciones.  

|Menú|Acción|Descripción|
|-------------|--------------|------------------------------|
|**Procesar**|**Sugerir cuentas**|Utilice cuentas de las otras divisas. Se insertarán las cuentas más utilizadas.|
||Cambiar tolerancia pagos|Cambia la tolerancia de pago máxima o el porcentaje de tolerancia de pago o ambos y filtra por divisa. Para obtener más información, consulte [Tolerancia de pago y tolerancia de descuento por pronto pago](finance-payment-tolerance-and-payment-discount-tolerance.md).|
||**Tipos de cambio**|Permite ver los tipos de cambio actualizados de las divisas que se utilizan.|
||**Ajustar tipos de cambio**|Ajusta los movimientos de contabilidad general, clientes, proveedores y bancos para que reflejen un saldo más actualizado si el tipo de cambio ha variado desde que se registraron los movimientos.|
||**Registro ajuste tipo cambio**|Ver los resultados de haber ejecutado el trabajo por lotes **Ajustar tipos de cambio**. Se crea una línea para cada divisa de cada combinación de grupo contable y divisa que se incluya en el ajuste.|
|**Servicio de tipo de cambio**|**Servicio de tipo de cambio**|Permite ver o editar la configuración de los servicios configurados para recuperar los tipos de cambio actualizados cuando se elige la acción **Actualizar tipos de cambio**.|
||**Actualizar tipos de cambio**|Permite obtener los tipos de cambio de divisa más recientes de un proveedor de servicios.|
|**Informes**|**Saldo divisas extranjeras**|Ver los saldos de todos los clientes y los proveedores en divisa extranjera y en la moneda local (DL). El informe muestra dos saldos DL. Uno es el saldo de divisa extranjera convertido a DL utilizando el tipo de cambio en el momento de la transacción. El otro es el saldo de divisa extranjera convertido a DL utilizando el tipo de cambio del día.|

## <a name="exchange-rates"></a>Tipos de cambio

Los tipos de cambio son la herramienta para calcular el valor en divisa local (DL) de cada transacción en moneda. La página **Tipos de cambio** incluye los siguientes campos:

|Campo|Descripción|  
|---------------------------------|---------------------------------------|  
|**Fecha inicial**|La fecha en que se efectuó el tipo de cambio.|  
|**Cód. divisa**|El código de divisa relacionado con este tipo de cambio.|  
|**Cód. divisa relacionada**|Si esta divisa es parte de un cálculo de divisa triangular, entonces el código de divisa relacionado se puede configurar aquí|  
|**Valor tipo cambio divisa**|El importe del tipo de cambio es el tipo que se utilizará para el código de moneda seleccionado en la línea. Normalmente 1 o 100|  
|**Valor t.c. divisa relacionada**|El importe del tipo de cambio relacional se asocia al tipo que se utilizará para el código de divisa relacional|  
|**Valor t. c. ajustes divisa**|El importe del tipo de cambio del ajuste es el tipo que se utilizará para el código de divisa seleccionado en la línea para el uso del trabajo por lotes **Ajustar tipos de cambio**|  
|**Valor t.c. ajustes divisa rel.**|El importe del tipo de cambio del ajuste relacional es el tipo que se utilizará para el código de divisa seleccionado en la línea para el uso del trabajo por lotes **Ajustar tipos de cambio**|  
|**Valor tipo cambio fijo**|Especifica si el tipo de cambio de la divisa se podrá cambiar en las facturas y las líneas del diario.|  

En general, los valores de los campos **Importe del tipo de cambio** e **Importe del tipo de cambio relacional** se utilizan como el tipo de cambio predeterminado en todos los documentos nuevos de cuentas por cobrar y cuentas por pagar que se creen en el futuro. Al documento se le asigna el tipo de divisa de acuerdo con la fecha de trabajo actual.  

> [!Note]
> El tipo de cambio real se calculará mediante esta fórmula:
> 
> `Currency Amount = Amount / Exchange Rate Amount * Relational Exch. Rate Amount`

El importe del tipo de cambio del ajuste o el importe del tipo de cambio del ajuste relacional se utilizará para actualizar todas las transacciones bancarias abiertas, por cobrar o por pagar.  

> [!Note]
> El tipo de cambio real se calculará mediante esta fórmula:
> 
> `Currency Amount = Amount / Adjustment Exch. Rate Amount * Relational Adjmt Exch. Rate Amt`

## <a name="adjusting-exchange-rates"></a>Ajustar los tipos de cambio

Puesto que los tipos de cambio fluctúan constantemente, los equivalentes de la divisa adicional del sistema se deben ajustar regularmente. Si no se llevan a cabo estos ajustes, los importes que se hayan convertido desde divisas extranjeras (o adicionales) y registrado en contabilidad en la divisa local pueden ser erróneos. Además, los movimientos diarios registrados antes de que se introduzca el tipo de cambio del día en la aplicación se tienen que actualizar una vez que se haya introducido esta información.

El proceso **Ajustar tipos de cambio** se usa para ajustar manualmente los tipos de cambio de los movimientos de clientes, proveedores y bancos. También sirve para actualizar los importes en la divisa adicional de los movimientos de contabilidad.  

> [!TIP]
> Puede utilizar un servicio para actualizar los tipos de cambio en el sistema automáticamente. Para obtener más información, vea [Para configurar un servicio de tipo de cambio de divisa](finance-how-update-currencies.md#to-set-up-a-currency-exchange-rate-service). Sin embargo, esto no ajusta los tipos de cambio en transacciones ya registradas. Para actualizar los tipos de cambio de las entradas publicadas, utilice el trabajo por lotes **Ajustar tipos de cambio**.

### <a name="effect-on-customers-and-vendors"></a>Efecto en clientes y proveedores

En las cuentas de proveedores y clientes, el trabajo por lotes ajusta la divisa utilizando el tipo de cambio vigente a la fecha de registro que se especifica en el trabajo por lotes. El proceso calcula las diferencias de cada uno de los saldos en divisa y registra los importes en la cuenta especificada en el campo **Cta. dif. pos. no realizadas** o en el campo **Cta. dif. neg. no realizadas** de la página **Divisas**. Los movimientos de contrapartida se registran automáticamente en la cuenta de cobros y pagos de la contabilidad.

El proceso utiliza todos los movimientos de clientes y de proveedores. Si hay un tipo de cambio diferente para un movimiento, el proceso crea un nuevo movimiento detallado de cliente o de proveedor, que refleja el importe ajustado del movimiento de cliente o de proveedor.

#### <a name="dimensions-on-customer-and-vendor-ledger-entries"></a>Dimensiones en movimientos de clientes y proveedores
Los movimientos de ajuste se asignan a las dimensiones de los movimientos de clientes y proveedores y los ajustes se registran por combinación de valores de dimensiones.

### <a name="effect-on-bank-accounts"></a>Efecto sobre cuentas bancarias
En las cuentas de bancos, el trabajo por lotes ajusta la divisa utilizando el tipo de cambio vigente a la fecha de registro especificada en el trabajo por lotes. El proceso calcula las diferencias de cada banco y registra los importes en la cuenta contable especificada en el campo **Cta. dif. pos. realizadas** o en el campo **Cta. dif. neg. realizadas** de la página **Divisas**. Los movimientos de contrapartida se registran automáticamente en las cuentas de bancos especificadas en los grupos contables de bancos. El proceso calcula un movimiento por divisa por grupo contable.

#### <a name="dimensions-on-bank-account-entries"></a>Dimensiones en movimientos de bancos
Los movimientos de ajustes de la cuenta contable del banco y de la cuenta de pérdidas y ganancias se asignan a las dimensiones predeterminadas de la cuenta de banco.

### <a name="effect-on-gl-accounts"></a>Efecto sobre cuentas
Si registra en una divisa adicional, puede hacer que el proceso genere movimientos nuevos de contabilidad para realizar ajustes de divisas entre la DL y la divisa adicional. El proceso calcula las diferencias de cada movimiento y ajusta el movimiento en función del valor que figure en el campo **Ajuste tipo cambio** para cada cuenta.

##### <a name="dimensions-on-gl-account-entries"></a>Dimensiones en movimientos de cuentas contables
Los movimientos registrados se asignan a las dimensiones predeterminadas de las cuentas donde están registrados.

> [!Important]
> Antes de utilizar el trabajo por lotes, introduzca los tipos de cambio de ajuste que se usan para ajustar los saldos en divisa extranjera. Debe hacerlo en la página **Tipos cambio divisa**.<br><br>  

> [!Video https://www.microsoft.com/videoplayer/embed/RE3Q24s?rel=0]

## <a name="to-set-up-a-currency-exchange-rate-service"></a>Para configurar un servicio de tipo de cambio de divisa
Puede utilizar un servicio externo para mantener actualizados los tipos de cambio de divisa como FloatRates.

1. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Servicios de tipo de cambio de divisas** y luego elija el enlace relacionado.
2. Seleccione la acción **Nuevo**.
3. En la página **Servicio de tipo de cambio de divisas**, rellene los campos según sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Active el control de alternancia a **Habilitado** para habilitar el servicio.

> [!NOTE]
> El siguiente video muestra un ejemplo de cómo conectarse a un servicio de tipo de cambio de divisa, utilizando el Banco Central Europeo como ejemplo. En el segmento que describe cómo configurar asignaciones de campo, la configuración en la columna **Origen** para **Nodo principal para el código de divisa** solo devolverá la primera divisa encontrada. El ajuste debe ser **/gesmes:Envelope/Code/Code/Code**.

<br><br>  
  
> [!Video https://www.microsoft.com/en-us/videoplayer/embed/RE4A1jy?rel=0]

## <a name="to-update-currency-exchange-rates-through-a-service"></a>Para actualizar los tipos de cambio de divisa mediante un servicio
1. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Divisas** y luego elija el enlace relacionado.
2. Seleccione la acción **Actualizar tipos de cambio**.

El valor del campo **Tipo cambio** en la página **Divisas** se actualiza con el último tipo de cambio de divisa.

## <a name="see-related-training-at-microsoft-learn"></a>Consulte Formación relacionada en [Microsoft Learn](/learn/paths/use-multiple-currencies-dynamics-365-business-central/)

## <a name="see-also"></a>Consulte también
[Configurar una divisa de informes adicional](finance-how-setup-additional-currencies.md)  
[Cerrar años y periodos](year-close-years-periods.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
