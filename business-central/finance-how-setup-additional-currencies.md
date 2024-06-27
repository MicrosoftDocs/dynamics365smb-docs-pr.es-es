---
title: Configurar divisas adicionales
description: 'La contabilidad se configura con la divisa local (DL), y se configura otra divisa como divisa adicional, a la que se asigna un tipo de cambio.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'multiple currencies, foreign exchange rates'
ms.search.form: '5, 16,118, 483, 495'
ms.date: 06/13/2024
ms.service: dynamics-365-business-central
---
# <a name="set-up-an-additional-reporting-currency"></a>Configurar una divisa de informes adicional

Las empresas trabajan cada vez en un mayor número de países o regiones, por lo que es muy importante que puedan revisar y crear informes de datos financieros en más de una divisa.

> [!NOTE]  
> Si está buscando información en tiempo real sobre tipos de cambio (FX) o tipos de cambio históricos, en [!INCLUDE[prod_short](includes/prod_short.md)] la encontrará como divisa. Además de este artículo, consulte también [Actualizar tipos de cambio de divisa](finance-how-update-currencies.md).

La contabilidad se configura con la divisa local (DL), pero también se puede configurar para usarla en otra divisa a la que se asigna un tipo de cambio. Si designa una segunda divisa como una divisa de informes adicional (ACY), [!INCLUDE[prod_short](includes/prod_short.md)] registrará automáticamente los importes tanto en ML como en DA en cada entrada en cuenta de mayor y en otras entradas, como las entradas de IVA.

> [!Warning]
> No debería utilizar la función DA como base para la conversión de estados financieros a menos que comprenda sus limitaciones. No puede traducir resultados financieros de las subsidiarias extranjeras como parte de la consolidación de una empresa. DA solo puede utilizarse para elaborar informes en otra moneda, como si esa moneda fuera ML de la empresa.
>
> Por ejemplo, tiene una gran cantidad de cuentas por cobrar en libras esterlinas (GBP) y ha configurado su DA como GBP. En este escenario, los importes en las cuentas por cobrar que utilizan libras esterlinas no se ajustan por las ganancias / pérdidas por cambio de divisa en la DA, solo los importes en las cuentas por cobrar que estén en otras divisas. Eso significa que si usa DA para informar de sus estados financieros, podría producir saldos pendientes de cuentas por cobrar subestimados o exagerados.

## <a name="displaying-reports-and-amounts-in-acy"></a>Visualización de informes e importes en DA

El uso de DA puede ayudar al proceso de información de una empresa en los siguientes casos:

- Empresas de países o regiones que no pertenecen a la Unión Europea y tienen un gran volumen de transacciones con empresas de países o regiones de la Unión Europea. En este caso, la empresa que no pertenece a la Unión Europea puede crear informes en euros para que sus informes financieros resulten más útiles a sus socios de la Unión Europea.
- Empresas que desean mostrar sus informes en una divisa de mayor difusión internacional, además de en su divisa local.

Varios informes financieros se basan en movimientos contables. Para visualizar los datos del informe en DA, active la casilla de verificación **Mostrar importes en divisa de informes adicional** en la ficha desplegable **Opciones** del informe de contabilidad correspondiente.

## <a name="adjusting-exchange-rates"></a>Ajustando divisas

Puesto que los tipos de cambio fluctúan constantemente, los equivalentes de DA del sistema se deben ajustar regularmente. Si no se llevan a cabo estos ajustes, los importes que se hayan convertido desde divisas extranjeras (o adicionales) y registrado en contabilidad en la divisa local pueden ser erróneos. Además, los movimientos diarios registrados antes de que se introduzca el tipo de cambio del día en la aplicación se tienen que actualizar una vez que se haya introducido esta información. El proceso **Ajustar tipos de cambio** se usa para ajustar los tipos de cambio de los movimientos de clientes, proveedores y bancos. También sirve para actualizar los importes en DA de los movimientos de contabilidad. Para obtener más información, vea [Actualizar tipos cambio divisa](finance-how-update-currencies.md).

## <a name="setting-up-an-acy"></a>Configuración de DA

Para configurar DA, siga estos pasos:

- Especificar cuentas para registrar los ajustes de tipo de cambio.  
- Especifique el método de ajuste de tipo de cambio para todas las cuentas.  
- Especifique el método de ajuste de tipo de cambio para los movimientos del IVA.  
- Activar DA.  

### <a name="to-specify-general-ledger-accounts-for-posting-exchange-rate-adjustments"></a>Para especificar cuentas para registrar los ajustes de tipo de cambio.

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Divisas** y luego elija el enlace relacionado.  
2. En la página **Divisas**, rellene los siguientes campos para DA.  

|Campo|Descripción|  
|---------------------------------|---------------------------------------|  
|**Cta. aj. pos. CG realizados**|La cuenta en la que desea que el sistema registre las diferencias positivas de cambio de los ajustes de divisa entre la DL y DA.|  
|**Cta. aj. neg. CG realizados**|La cuenta en la que desea que el sistema registre las pérdidas del tipo de cambio de los ajustes de divisa entre ML y DA.|  
|**Cta. aj. residual pos.**|La cuenta en que se registrarán los importes residuales negativos que sean ganancias si se realizan registros en el área de contabilidad de la aplicación en ML y DA.|  
|**Cta. aj. residual neg.**|La cuenta en que se registrarán los importes residuales negativos que sean pérdidas si se realizan registros en el área de contabilidad de la aplicación en ML y DA.|

> [!NOTE]  
> Se pueden producir importes residuales cuando [!INCLUDE[prod_short](includes/prod_short.md)] redondea importes del debe y el haber que se han convertido de ML a DA.  

Debe especificar, para cada cuenta, como se ajustarán los importes de contabilidad de la cuenta en función de las fluctuaciones del tipo de cambio entre ML y la DA.  

### <a name="to-specify-the-exchange-rate-adjustment-method-for-all-general-ledger-accounts"></a>Para especificar el método de ajuste de tipo de cambio para todas las cuentas

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Plan de cuentas** y luego elija el enlace relacionado.  
2. En la página **Plan de cuentas**, seleccione la cuenta correspondiente y, a continuación, la acción **Editar**.  
3. En la página **Ficha cuenta**, seleccione el método correspondiente en el campo **Ajuste tipo cambio**.  

    Si realiza registros en DA, en el campo **Ajuste tipo cambio**, especifique cómo se ajusta esta cuenta en función de las fluctuaciones del tipo de cambio entre la ML y DA. La siguiente tabla describe las opciones.  

    |Campo|Descripción|  
    |----------------------------------|---------------------------------------|  
    |**Sin ajuste**|No se realiza ningún ajuste del tipo de cambio en la cuenta. Esta configuración es la opción predeterminada.<br /><br /> **NOTA:** Seleccione esta opción si el tipo de cambio entre ML y DA siempre es fijo.|  
    |**Ajustar importe**|El importe en DL se ajusta para las ganancias o las pérdidas del tipo de cambio. Las diferencias positivas o negativas en la cuenta en el campo **Importe** y en las cuentas que haya especificado para las diferencias positivas o negativas en los campos **Cta. aj. pos. C/G realizados** o **Cta. aj. neg. C/G** realizados de la página **Divisas**.|  
    |**Ajustar importe divisa adicional**|DA se ajusta para las ganancias o las pérdidas del tipo de cambio. Las diferencias positivas o negativas en la cuenta en el campo **Importe divisa-adicional** y en las cuentas que haya especificado para las diferencias positivas o negativas en los campos **Cta. aj. pos. C/G realizados** o **Cta. aj. neg. C/G** realizados de la página **Divisas**.|  

    Las ganancias y pérdidas por tipo de cambio se registran al ejecutar el proceso **Ajustar tipos de cambio**. En dicho proceso, el tipo de cambio queda definido en la página **Tipos cambio divisa** y, a continuación, compara los importes de los campos **Importe** e **Importe divisa-adicional** del movimiento de contabilidad para determinar si hay una ganancia o una pérdida por el tipo de cambio. En el proceso se usa la opción seleccionada en el campo **Ajuste tipo cambio** para determinar cómo se deben calcular y registrar las pérdidas o ganancias de tipo de cambio de las cuentas.  

4.  Cierre la página **Ficha cuenta**.  

### <a name="to-specify-exchange-rate-adjustment-method-for-vat-entries"></a>Especificar el método de ajuste de tipo de cambio para los movimientos del IVA

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Configuración de contabilidad**, y luego elija el enlace relacionado.  
2. En la página **Configuración de contabilidad**, seleccione el método correspondiente en el campo **Tipo cambio ajuste IVA**.  
3. Si realiza registros en DA, en el campo **Tipo cambio ajuste IVA** puede especificar cómo se ajustarán las cuentas para el registro del IVA de la página **Config. grupos registro IVA** en función de las fluctuaciones del tipo de cambio entre ML y DA.  

    Al ejecutar el proceso **Ajustar tipos de cambio**, el tipo de cambio de ajuste se identifica en la página **Tipo cambio divisa** y, a continuación, se comparan los importes de los campos **Importe** e **Importe divisa-adicional** del movimiento de IVA para determinar si hay ganancias o pérdidas por el tipo de cambio. El proceso usa la opción que seleccione en este campo para determinar cómo se van a registrar las diferencias positivas o negativas en el cambio para las cuentas de IVA.  

    Las opciones son las mismas que para los movimientos de contabilidad, pero en este caso los movimientos que se ajustan son los del IVA. La siguiente tabla describe las opciones.

    |Campo|Descripción|  
    |----------------------------------|---------------------------------------|  
    |**Sin ajuste**|No se realiza ningún ajuste del tipo de cambio en la cuenta. Esta configuración es la opción predeterminada.|  
    |**Ajustar importe**|El importe en DL se ajusta para las ganancias o las pérdidas del tipo de cambio. Las diferencias positivas o negativas en la cuenta en el campo **Importe** y en las cuentas que haya especificado para las diferencias positivas o negativas en los campos **Cta. aj. pos. C/G realizados** o **Cta. aj. neg. C/G** realizados de la página **Divisas**.|  
    |**Ajustar importe divisa adicional**|DA se ajusta para las ganancias o las pérdidas del tipo de cambio. Las diferencias positivas o negativas en la cuenta en el campo **Importe divisa-adicional** y en las cuentas que haya especificado para las diferencias positivas o negativas en los campos **Cta. aj. pos. C/G realizados** o **Cta. aj. neg. C/G** realizados de la página **Divisas**.|  

### <a name="to-activate-the-acy"></a>Para activar DA

1. Elija el icono ![Bombilla que abre la característica Dígame](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Configuración de contabilidad**, y luego elija el enlace relacionado.  
2. En la página **Configuración de contabilidad**, elija el campo **Divisa de informes adicional** para seleccionar la divisa adicional en la que desea informar.  
3. Al salir del campo, [!INCLUDE[prod_short](includes/prod_short.md)] mostrará un mensaje de confirmación con una descripción de los efectos de activar DA.  
4. Elija el botón **Sí** para confirmar que desea activar la divisa.  
5. El trabajo por lotes **Ajustar divisa de informe adicional** se abre.

    Este proceso convierte los importes en la divisa local de los movimientos existentes a DA. El proceso usa un tipo de cambio predeterminado, copiado del que es válido en la fecha de trabajo de la página **Tipos cambio divisa**. La conversión de ML a DA puede producir importes residuales, que se registran en las cuentas de ganancias y pérdidas residuales especificadas en la página **Divisas**. La fecha de registro y el número de documento de estos movimientos son los mismos que los del movimiento de contabilidad original. Después de haber registrado todos los movimientos residuales, el proceso registra un movimiento de redondeo en la fecha de cierre de cada año cerrado en la cuenta de remanentes. Esta contabilización garantiza que el saldo final de las cuentas de resultados de cada ejercicio cerrado sea 0 tanto en ML como en DA.
6. Rellene los campos según sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]      
7. Elija el botón **Aceptar** para iniciar el trabajo por lotes.  

Después de ejecutar el trabajo por lotes, los importes de las siguientes entradas existentes se encuentran tanto en ML como en DA:  

- Movimientos de contabilidad  
- Movimientos de liquidación de producto  
- Movimientos de IVA  
- Movimientos de proyecto  
- Movimientos de valor  
- Líneas de pedido de producción  
- Movimientos de orden de producción  

Además, los importes de todos los movimientos posteriores del mismo tipo se registrarán en ML y en DA.  

> [!NOTE]  
> El campo **Divisa adicional** sólo quedará activada una vez que se haya seleccionado **Aceptar** en el proceso **Ajust. divisa adicional**.  

## <a name="see-also"></a>Consulte también

[Actualizar tipos de cambio de divisa](finance-how-update-currencies.md)  
[Cerrar ejercicios y periodos](year-close-years-periods.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
