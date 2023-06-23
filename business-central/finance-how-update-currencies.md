---
title: Actualizar los tipos de cambio de divisa (contiene vídeo)
description: 'Si realiza un seguimiento de los importes en diferentes divisas, puede dejar que Business Central le ayude a ajustar los tipos de cambio FX de los movimientos registrados con un servicio externo.'
author: edupont04
ms.topic: conceptual
ms.search.keywords: 'multiple currencies, adjust exchange rates, FX rates'
ms.search.form: '5, 118'
ms.date: 03/15/2022
ms.author: edupont
---
# <a name="update-currency-exchange-rates" />Actualizar tipos cambio divisa

Puede definir diferentes divisas en [!INCLUDE [prod_short](includes/prod_short.md)], por ejemplo, si opera con divisas distintas a su divisa local. Después, para ayudarle a realizar un seguimiento de los cambios en las tasas de cambio de divisa, puede administrar las divisas manualmente o configurar un servicio de tasa de cambio de diviso.

## <a name="currencies" />Divisas

> [!TIP]  
> Si está buscando información en tiempo real sobre tipos de cambio (FX) o tipos de cambio históricos, en [!INCLUDE[prod_short](includes/prod_short.md)] la encontrará como divisa. Además de este artículo, consulte también [Configurar una divisa de informes adicional](finance-how-setup-additional-currencies.md).

[!INCLUDE [finance-currencies-def](includes/finance-currencies-def.md)]

Especifique los códigos de moneda en la lista **Divisas**, incluida la información adicional y los ajustes necesarios para cada código de divisa. Para obtener más información, consulte [Divisas](finance-set-up-currencies.md#curr)

### <a name="example-of-a-receivable-currency-transaction" />Ejemplo de una transacción de divisa por cobrar

[!INCLUDE [finance-currencies-example](includes/finance-currencies-example.md)]

## <a name="exchange-rates" />Tipos de cambio

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

## <a name="adjusting-exchange-rates" />Ajustar los tipos de cambio

Puesto que los tipos de cambio fluctúan constantemente, los equivalentes de la divisa adicional del sistema se deben ajustar regularmente. Si no se llevan a cabo estos ajustes, los importes que se hayan convertido desde divisas extranjeras (o adicionales) y registrado en contabilidad en la divisa local pueden ser erróneos. Además, los movimientos diarios registrados antes de que se introduzca el tipo de cambio del día en la aplicación se tienen que actualizar una vez que se haya introducido esta información.

El trabajo por lotes **Ajustar tipos de cambio** se usa para ajustar manualmente los tipos de cambio de los movimientos de clientes, proveedores y bancos. También sirve para actualizar los importes en la divisa adicional de los movimientos de contabilidad.  

> [!TIP]
> Puede utilizar un servicio para actualizar los tipos de cambio en el sistema automáticamente. Para obtener más información, vea [Para configurar un servicio de tipo de cambio de divisa](finance-how-update-currencies.md#to-set-up-a-currency-exchange-rate-service). Sin embargo, esto no ajusta los tipos de cambio en transacciones ya registradas. Para actualizar los tipos de cambio de las entradas publicadas, utilice el trabajo por lotes **Ajustar tipos de cambio**.

Puede obtener una vista previa del efecto que tendrá un ajuste en el registro antes de hacerlo realmente seleccionando **Vista previa** en la página **Ajustar tipos de cambio**. Además, puede seleccionar si el registro del libro mayor será detallado (por entrada) o resumido (por moneda) seleccionando **Resumir movimientos**. También puede especificar cómo manejar las dimensiones para registros de ganancias y pérdidas no realizadas eligiendo una de las siguientes opciones en el campo **Transferir valores de dimensión**:  

- **Movimiento de origen**: los movimientos contables para ganancias y pérdidas no realizadas tendrán valores de dimensión transferidos desde el movimiento ajustado.
- **Por cuenta**: los movimientos contables para ganancias y pérdidas no realizadas tendrán valores de dimensión transferidos desde el movimiento de origen de configuración de dimensiones en la cuenta de ganancias y pérdidas no realizadas.
- **Sin transferencia**: los movimientos contables para ganancias y pérdidas no realizadas no tendrán valores de dimensión.

### <a name="effect-on-customers-and-vendors" />Efecto en clientes y proveedores

En las cuentas de proveedores y clientes, el trabajo por lotes ajusta la divisa utilizando el tipo de cambio vigente a la fecha de registro que se especifica en el trabajo por lotes. El proceso calcula las diferencias de cada uno de los saldos en divisa y registra los importes en la cuenta especificada en el campo **Cta. dif. pos. no realizadas** o en el campo **Cta. dif. neg. no realizadas** de la página **Divisas**. Los movimientos de contrapartida se registran automáticamente en la cuenta de cobros y pagos de la contabilidad.

El proceso utiliza todos los movimientos de clientes y de proveedores. Si hay un tipo de cambio diferente para un movimiento, el proceso crea un nuevo movimiento detallado de cliente o de proveedor, que refleja el importe ajustado del movimiento de cliente o de proveedor.

#### <a name="dimensions-on-customer-and-vendor-ledger-entries" />Dimensiones en movimientos de clientes y proveedores

Los movimientos de ajuste se asignan a las dimensiones de los movimientos de clientes y proveedores y los ajustes se registran por combinación de valores de dimensiones.

### <a name="effect-on-bank-accounts" />Efecto sobre cuentas bancarias

En las cuentas de bancos, el trabajo por lotes ajusta la divisa utilizando el tipo de cambio vigente a la fecha de registro especificada en el trabajo por lotes. El proceso calcula las diferencias de cada banco y registra los importes en la cuenta contable especificada en el campo **Cta. dif. pos. realizadas** o en el campo **Cta. dif. neg. realizadas** de la página **Divisas**. Los movimientos de contrapartida se registran automáticamente en las cuentas de bancos especificadas en los grupos contables de bancos. El proceso calcula un movimiento por divisa por grupo contable.

#### <a name="dimensions-on-bank-account-entries" />Dimensiones en movimientos de bancos

Los movimientos de ajustes de la cuenta contable del banco y de la cuenta de pérdidas y ganancias se asignan a las dimensiones predeterminadas de la cuenta de banco.

### <a name="effect-on-gl-accounts" />Efecto sobre cuentas
Si registra en una divisa adicional, puede hacer que el proceso genere movimientos nuevos de contabilidad para realizar ajustes de divisas entre la DL y la divisa adicional. El proceso calcula las diferencias de cada movimiento y ajusta el movimiento en función del valor que figure en el campo **Ajuste tipo cambio** para cada cuenta.

##### <a name="dimensions-on-gl-account-entries" />Dimensiones en movimientos de cuentas contables
Los movimientos registrados se asignan a las dimensiones predeterminadas de las cuentas donde están registrados.

> [!Important]
> Antes de utilizar el trabajo por lotes, introduzca los tipos de cambio de ajuste que se usan para ajustar los saldos en divisa extranjera. Debe hacerlo en la página **Tipos cambio divisa**.<br><br>  

> [!Video https://www.microsoft.com/videoplayer/embed/RE3Q24s?rel=0]

## <a name="to-set-up-a-currency-exchange-rate-service" />Para configurar un servicio de tipo de cambio de divisa
Puede utilizar un servicio externo para mantener actualizados los tipos de cambio de divisa como FloatRates. 

> [!NOTE]
> La mayoría de los servicios de tipos de cambio proporcionan datos que son compatibles con el proceso de importación en [!INCLUDE[prod_short](includes/prod_short.md)]. Sin embargo, a veces los datos tienen un formato diferente y necesitará personalizar su proceso de importación. Puede usar el marco de intercambio de datos para hacerlo agregando su propia codeunit. Probablemente necesite ayuda de un desarrollador para hacer eso. Para obtener más información, vea [Configurar las definiciones de intercambio de datos](across-how-to-set-up-data-exchange-definitions.md).

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Servicios de tipo de cambio de divisas** y, a continuación, elija el vínculo relacionado.
2. Seleccione la acción **Nuevo**.
3. En la página **Servicio de tipo de cambio de divisas**, rellene los campos según sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Active el control de alternancia a **Habilitado** para habilitar el servicio.

> [!NOTE]
> El siguiente video muestra un ejemplo de cómo conectarse a un servicio de tipo de cambio de divisa, utilizando el Banco Central Europeo como ejemplo. En el segmento que describe cómo configurar asignaciones de campo, la configuración en la columna **Origen** para **Nodo principal para el código de divisa** solo devolverá la primera divisa encontrada. La configuración debería ser `/gesmes:Envelope/Code/Code/Code`.

<br><br>  
  
> [!Video https://www.microsoft.com/en-us/videoplayer/embed/RE4A1jy?rel=0]

## <a name="to-update-currency-exchange-rates-through-a-service" />Para actualizar los tipos de cambio de divisa mediante un servicio
1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Divisas** y luego elija el enlace relacionado.
2. Seleccione la acción **Actualizar tipos de cambio**.

El valor del campo **Tipo cambio** en la página **Divisas** se actualiza con el último tipo de cambio de divisa.

## <a name="see-related-microsoft-trainingtrainingpathsuse-multiple-currencies-dynamics-365-business-central" />Consultar la [formación de Microsoft](/training/paths/use-multiple-currencies-dynamics-365-business-central/) relacionada

## <a name="see-also" />Consulte también

[Divisas en Business Central](finance-currencies.md)  
[Configuración de divisas](finance-set-up-currencies.md)  
[Configurar una divisa de informes adicional](finance-how-setup-additional-currencies.md)  
[Cerrar años y periodos](year-close-years-periods.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
