---
title: Actualizar tipos cambio divisa
description: Realice un seguimiento de los importes en diferentes divisas utilizando códigos de divisa y deje que Business Central le ayude a ajustar los tipos de cambio de los movimientos registrados con un servicio externo.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.search.keywords: multiple currencies, adjust exchange rates
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 9027fe7cb01efe2e06ef52154f30f2fa8fb41b83
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/01/2020
ms.locfileid: "3924133"
---
# <a name="update-currency-exchange-rates"></a>Actualizar tipos cambio divisa

Las empresas trabajan cada vez en un mayor número de países o regiones, por lo que es muy importante que puedan comercializar y crear informes financieros en más de una divisa. Debe configurar un código por cada una de las divisas usadas en caso de que las operaciones de compra y venta se realicen en una divisa que no sea la divisa local (DL), tenga cobros y pagos en otras divisas o registre las transacciones de contabilidad en diferentes divisas.

La contabilidad se configura con la divisa local (DL), pero también se puede configurar para usarla en otra divisa a la que se asigna un tipo de cambio. Mediante la designación de una segunda divisa como la denominada divisa de informes adicional, [!INCLUDE[d365fin](includes/d365fin_md.md)] registrará automáticamente los importes tanto en la divisa local como en la divisa adicional en todos los movimientos de contabilidad y en otros movimientos, por ejemplo los del IVA. Para obtener más información, vea [Configurar una divisa de informes adicional](finance-how-setup-additional-currencies.md).

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
4. Seleccione la casilla de verificación **Activado** para activar el servicio.
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
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
