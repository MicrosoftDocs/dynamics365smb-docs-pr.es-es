---
title: Actualizar los tipos de cambio de divisa (contiene vídeo)
description: Aprenda a usar Business Central para ajustar los tipos de cambio de importes en distintas divisas.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bnielse
ms.topic: conceptual
ms.search.keywords: 'multiple currencies, adjust exchange rates, FX rates'
ms.search.form: '5, 118'
ms.date: 11/13/2023
ms.custom: bap-template
ms.service: dynamics-365-business-central
---
# <a name="update-currency-exchange-rates"></a>Actualizar tipos de cambio de divisa

Si negocia con distintas divisas, debe estar al tanto de las variaciones de los tipos de cambio. [!INCLUDE [prod_short](includes/prod_short.md)] le ayuda a administrar y actualizar los tipos de cambio de forma manual o automática y a establecer un servicio de cambio de divisas.

## <a name="currencies"></a>Divisas

> [!TIP]  
> En [!INCLUDE[prod_short](includes/prod_short.md)], puede encontrar información en tiempo real sobre los tipos de cambio de divisas (FX) o los tipos históricos bajo el término divisa. Para obtener más información, vea [Configurar una divisa de informes adicional](finance-how-setup-additional-currencies.md).

[!INCLUDE [finance-currencies-def](includes/finance-currencies-def.md)]

Puede especificar los códigos de divisa en la lista **Divisas**, incluida la información adicional y los ajustes necesarios para cada código de divisa. Para obtener más información, consulte [Divisas](finance-set-up-currencies.md#curr)

### <a name="example-of-a-receivable-currency-transaction"></a>Ejemplo de una transacción de divisa por cobrar

[!INCLUDE [finance-currencies-example](includes/finance-currencies-example.md)]

## <a name="exchange-rates"></a>Tipos de cambio

Los tipos de cambio son la herramienta para calcular el valor en divisa local (DL) de cada transacción en moneda. La página **Tipos de cambio** incluye los siguientes campos:

|Campo|Descripción|  
|---------------------------------|---------------------------------------|  
|**Fecha inicial**|La fecha en que entró en vigor el tipo de cambio.|  
|**Cód. divisa**|El código de divisa relacionado con este tipo de cambio.|  
|**Cód. divisa relacionada**|Si esta divisa forma parte de un cálculo de divisa triangular, puede configurar aquí el código de divisa relacionado.|  
|**Valor tipo cambio divisa**|El importe del tipo de cambio es el tipo para el código de moneda seleccionado en la línea. Normalmente 1 o 100.|  
|**Valor t.c. divisa relacionada**|El importe del tipo de cambio relacional se asocia al tipo que se utilizará para el código de divisa relacional.|  
|**Valor t. c. ajustes divisa**|El tipo para el código de divisa seleccionado en la línea para usar el trabajo por lotes **Ajustar tipos de cambio**.|  
|**Valor t.c. ajustes divisa rel.**|El tipo para el código de divisa seleccionado en la línea para usar el trabajo por lotes **Ajustar tipos de cambio**.|  
|**Valor tipo cambio fijo**|Especifica si el tipo de cambio de la divisa se podrá cambiar en las facturas y las líneas del diario.|  

En general, los valores de los campos **Importe del tipo de cambio** e **Importe del tipo de cambio relacional** se utilizan como el tipo de cambio predeterminado en todos los documentos nuevos de cuentas por cobrar y cuentas por pagar que se creen en el futuro. Al documento se le asigna el tipo de divisa de acuerdo con la fecha de trabajo actual.  

> [!Note]
> El tipo de cambio real se calcula mediante esta fórmula:
>
> `Currency Amount = Amount / Exchange Rate Amount * Relational Exch. Rate Amount`

El importe del tipo de cambio del ajuste o el importe del tipo de cambio del ajuste relacional actualizará todas las transacciones bancarias abiertas, por cobrar o por pagar.  

> [!Note]
> El tipo de cambio real se calcula mediante esta fórmula:
>
> `Currency Amount = Amount / Adjustment Exch. Rate Amount * Relational Adjmt Exch. Rate Amt`

## <a name="adjust-exchange-rates"></a>Ajustar tipos de cambio

Puesto que los tipos de cambio fluctúan constantemente, los equivalentes de otras divisas se deben ajustar regularmente. Si no lo hace, las cantidades convertidas de monedas extranjeras (u otras) y contabilizadas en el libro mayor en moneda local pueden ser incorrectas. Además, debe actualizar las entradas diarias publicadas antes de ingresar un tipo de cambio diario.

Puede usar el trabajo por lotes **Ajustar tipos de cambio** para ajustar manualmente los tipos de cambio de los movimientos de clientes, proveedores y bancos. El proceso por lotes también puede actualizar otros importes en la divisa adicional de los movimientos de contabilidad.  

> [!TIP]
> Puede utilizar un servicio para actualizar los tipos de cambio en el sistema automáticamente. Para obtener más información, vea [Para configurar un servicio de tipo de cambio de divisa](finance-how-update-currencies.md#set-up-a-currency-exchange-rate-service). Sin embargo, esto no ajusta los tipos de cambio en transacciones ya registradas. Para actualizar los tipos de cambio de las entradas publicadas, utilice el trabajo por lotes **Ajustar tipos de cambio**.

También puede especificar cómo el ajuste gestiona las dimensiones para registros de ganancias y pérdidas no realizadas eligiendo una de las siguientes opciones en el campo **Registro de dimensión**:  

* **Dimensiones de entrada de origen**: transfiere valores de dimensión para movimientos contables para ganancias y pérdidas no realizadas en el movimiento que está ajustando.  
* **Sin dimensiones**: no se transferirán los valores de dimensión para las ganancias y pérdidas no realizadas a entradas del libro mayor. [!INCLUDE [prod_short](includes/prod_short.md)] sigue utilizando la configuración de dimensión predeterminada, por ejemplo, **Código obligatorio**, **Mismo código** o **Sin código**. Si las entradas de transacciones de origen tienen valores de dimensión, el ajuste crea entradas sin valores de dimensión.  
* **Dimensiones de cuenta L/M**: transferir valores de dimensión desde el movimiento de origen de configuración de dimensiones en la cuenta de ganancias y pérdidas no realizadas.

> [!NOTE]
> Para utilizar la capacidad de vista previa, debe activar la función **Actualización de funciones: habilite el uso del nuevo ajuste de tipo de cambio extensible, incluida la función de revisión de publicaciones** en la página **[Gestión de funciones](https://businesscentral.dynamics.com/?page=2610)**.

> [!IMPORTANT]
> Debido a los requisitos locales en Suiza, no recomendamos que habilite **Actualización de funciones: habilite el uso del nuevo ajuste de tipo de cambio extensible, incluida la revisión de publicaciones** en la versión de Suiza (CH).

## <a name="preview-the-effect-of-an-adjustment"></a>Vista previa del efecto de un ajuste

Puede obtener una vista previa del efecto que tiene un ajuste en el de tasa de cambio antes de hacerlo realmente seleccionando la acción **Vista previa de registro** en el informe **Ajustar tipos de cambio** de la página de solicitud (Informe 596). En la página de solicitud, puede especificar qué incluir en la vista previa:

* Obtener un registro detallado del libro mayor por movimiento.
* Obtenga una publicación resumida por divisa. Simplemente seleccione el campo **Ajustar por movimiento** en el informe **Ajuste de tasas de cambio** .

### <a name="effect-on-customers-and-vendors"></a>Efecto en clientes y proveedores

En las cuentas de proveedores y clientes, el proceso usa el tipo de cambio vigente en la fecha de registro especificada en el proceso para ajustar la divisa. El proceso calcula las diferencias de cada uno de los saldos en divisa y registra los importes en la cuenta especificada en el campo **Cta. dif. pos. no realizadas** o en el campo **Cta. dif. neg. no realizadas** de la página **Divisas**. Los movimientos de contrapartida se registran automáticamente en la cuenta de cobros y pagos de la contabilidad.

El proceso utiliza todos los movimientos de clientes y de proveedores. Si hay un tipo de cambio diferente para un movimiento, el proceso crea un nuevo movimiento detallado de cliente o de proveedor. El nuevo asiento refleja el importe ajustado en el asiento contable del cliente o proveedor.

#### <a name="dimensions-on-customer-and-vendor-ledger-entries"></a>Dimensiones en movimientos de clientes y proveedores

[!INCLUDE [prod_short](includes/prod_short.md)] asigna las dimensiones de los movimientos de clientes y proveedores y los ajustes se registran por combinación de valores de dimensiones.

### <a name="effect-on-bank-accounts"></a>Efecto sobre cuentas bancarias

En las cuentas de bancos, el trabajo por lotes ajusta la divisa utilizando el tipo de cambio vigente a la fecha de registro especificada en el trabajo por lotes. El proceso calcula las diferencias de cada banco y registra los importes en la cuenta contable especificada en el campo **Cta. dif. pos. realizadas** o en el campo **Cta. dif. neg. realizadas** de la página **Divisas**. Los movimientos de contrapartida se registran automáticamente en las cuentas de bancos especificadas en los grupos contables de bancos. El proceso calcula un movimiento por divisa por grupo contable.

#### <a name="dimensions-on-bank-account-entries"></a>Dimensiones en movimientos de cuentas bancarias

Los movimientos de ajustes de la cuenta contable del banco y de la cuenta de pérdidas y ganancias se asignan a las dimensiones predeterminadas de la cuenta de banco.

### <a name="effect-on-gl-accounts"></a>Efecto sobre cuentas de L/M

Si registra en otra divisa adicional, puede hacer que el proceso genere movimientos nuevos de contabilidad para realizar ajustes entre la divisa local y otra divisa. El trabajo por lotes calcula las diferencias para cada movimiento del libro mayor. Ajusta el movimiento en función del valor que figure en el campo **Ajuste tipo cambio** para cada cuenta.

#### <a name="dimensions-on-gl-account-entries"></a>Dimensiones en movimientos de cuentas contables

Los movimientos registrados se asignan a las dimensiones predeterminadas de las cuentas donde están registrados.

> [!Important]
> Antes de utilizar el trabajo por lotes, debe introducir los tipos de cambio de ajuste que se usan para ajustar los saldos en divisa extranjera. Debe hacerlo en la página **Tipos cambio divisa**.<br><br>  

> [!Video https://www.microsoft.com/videoplayer/embed/RE3Q24s?rel=0]

## <a name="set-up-a-currency-exchange-rate-service"></a>Configurar un servicio de tipo de cambio de divisa

Puede utilizar un servicio externo para mantener actualizados los tipos de cambio de divisa como FloatRates. 

> [!NOTE]
> La mayoría de los servicios de tipos de cambio proporcionan datos que son compatibles con el proceso de importación en [!INCLUDE[prod_short](includes/prod_short.md)]. Sin embargo, a veces los datos tienen un formato diferente y necesita personalizar su proceso de importación. Puede usar el marco de intercambio de datos para hacerlo agregando su propia codeunit. Probablemente necesite ayuda de un desarrollador para hacer eso. Para obtener más información, vea [Configurar las definiciones de intercambio de datos](across-how-to-set-up-data-exchange-definitions.md).

1. Seleccione el icono ![Bombilla que abre la característica Dígame](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Servicios de tipo de cambio de divisas** y, a continuación, seleccione el vínculo relacionado.
2. Seleccione la acción **Nuevo**.
3. En la página **Servicio de tipo de cambio de divisas**, rellene los campos según sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Active el control de alternancia a **Habilitado** para habilitar el servicio.

> [!NOTE]
> El siguiente vídeo muestra cómo puede conectarse a un servicio de cambio de divisas, usando como ejemplo el Banco Central Europeo. En el segmento que describe cómo configurar asignaciones de campo, la configuración en la columna **Origen** para **Nodo principal para el código de divisa** solo devuelve la primera divisa encontrada. La configuración debería ser `/gesmes:Envelope/Code/Code/Code`.

<br><br>  
  
> [!Video https://www.microsoft.com/en-us/videoplayer/embed/RE4A1jy?rel=0]

## <a name="update-currency-exchange-rates-through-a-service"></a>Actualizar los tipos de cambio de divisa mediante un servicio

Siga los pasos indicados para actualizar los tipos de cambio de divisa a través de un servicio:

1. Seleccione el icono ![Bombilla que abre la característica Dígame](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Divisas** y luego seleccione el enlace relacionado.
2. Seleccione la acción **Actualizar tipos de cambio**.

## <a name="correct-mistakes"></a>Corregir errores

De vez en cuando, es posible que deba corregir un error en una transacción de pago asociado con ajustes a las ganancias y pérdidas de moneda extranjera. Puede utilizar la acción **Transacción inversa** en las páginas **Conciliación movs. bancos**, **Movs. clientes** y **Movs. proveedores** para cancelar la aplicación y revertir la transacción de pago.

> [!NOTE]
> Cuando cancela la aplicación y revierte un pago para una entrada que tenía ajustes de tipo de cambio asociados, la reversión registra entradas de reversión para los ajustes. Es posible que tengas que ejecutar el ajuste del tipo de cambio de moneda nuevamente para obtener el saldo actual correcto.

## <a name="see-also"></a>Consulte también

## <a name="see-also-1"></a>Consulte también

[Divisas en Business Central](finance-currencies.md)  
[Configuración de divisas](finance-set-up-currencies.md)  
[Configurar una divisa de informes adicional](finance-how-setup-additional-currencies.md)  
[Cerrar años y periodos](year-close-years-periods.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
