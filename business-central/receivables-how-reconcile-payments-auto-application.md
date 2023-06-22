---
title: Conciliar los pagos con liquidación automática
description: Describe cómo conciliar pagos usando la liquidación automática para liquidar pagos o recibos de efectivo en los movimientos pendientes relacionados.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'payment process, direct payment posting, reconcile payment, expenses, cash receipts'
ms.search.form: '389, 1290, 1294, 1287'
ms.date: 06/22/2022
ms.author: bholtorf
---
# <a name="reconcile-payments-using-automatic-application" />Conciliar los pagos con liquidación automática

La página **Diario de conciliación de pagos** especifica los pagos, ya sean entrantes o salientes, que se han registrado como transacciones en su cuenta bancaria en línea o en un servicio de pago. Puede liquidar los pagos en movimientos abiertos de clientes, proveedores y cuentas bancarias relacionados. Rellene el diario importando un extracto bancario como archivo de información bancaria o introduciendo manualmente las transacciones que realiza a través de su servicio de pago.

> [!NOTE]
> La página ofrece una funcionalidad de correspondencia automática que aplica pagos a sus movimientos pendientes relacionados basados en una correspondencia de datos en una línea de estado bancario (línea de diario) con datos de en uno o más movimientos pendientes. Tenga en cuenta que puede sobrescribir las aplicaciones automáticas sugeridas y puede optar por no utilizar la aplicación automática. Para obtener más información, vea el paso 7 .

Un diario de conciliación de pagos está relacionado con una cuenta bancaria en [!INCLUDE[prod_short](includes/prod_short.md)]. La cuenta bancaria representa la cuenta bancaria en línea donde se registran las transacciones de pago. Todas las cuenta abiertas relacionada con los movimientos de los clientes o los proveedores se cerrarán cuando seleccione la acción **Registrar pagos y conciliar banco**. La cuenta bancaria se conciliará automáticamente para los pagos que registre mediante el diario.

Si usa la página **Diario de conciliación de pagos** para registrar y liquidar los pagos de los clientes, puede configurar el diario para usar una serie de números específica. Después, puede especificar la serie numérica en el campo **Serie numérica conciliación pagos** en una cuenta bancaria. El uso de una serie de números dedicada puede facilitar la identificación de los movimientos que se publicaron a través del diario.

Al igual que en otros diarios, cuando corrige los movimientos registrados, puede revertir los movimientos que se registraron a través del diario de conciliación de pagos desde la página **Registro movs. contabilidad**. Por ejemplo, es posible que desee revertir movimientos de pagos que liquidó en el cliente equivocado. Primero debe cancelar la liquidación de los movimientos del cliente. Luego puede usar la acción **Repetir mov.** de la página **Registro movs. contabilidad** para revertir el diario que registró los pagos. Alternativamente, en la página **Diarios generales registrados**, puede utilizar la acción **Copiar las líneas seleccionadas en el diario** para revertir líneas específicas del diario de conciliación de pagos registrado. 

Cuando utiliza la liquidación automática, [!INCLUDE[prod_short](includes/prod_short.md)] reconoce los movimientos de contabilidad bancarios que ya se han contabilizado, lo que ayuda a evitar la doble contabilización.

Puede importar transacciones bancarias, como archivos bancarios .csv u otro formato que proporcione su banco. Si desea importar tanto extractos bancarios como informaciones de bancos, primero debe habilitar un servicio dedicado de integración bancaria y, a continuación, vincular la cuenta bancaria a su cuenta bancaria en línea relacionada. El diario de conciliación de pagos detectará automáticamente las fuentes de banco cuando seleccione la acción **Importar transacciones de banco**. Además, puede configurar una cuenta bancaria para que importe nuevas fuentes de extractos bancarios cada hora. No se importarán las transacciones para los pagos que ya se hayan registrado como liquidados o conciliados. Puede usar el servicio Envestnet Yodlee Bank Feeds para obtener dichas transacción; está preinstalado en algunas versiones de países de [!INCLUDE[d365fin](includes/d365fin_md.md)]. Para obtener más información, vea [Configurar el servicio Envestnet Yodlee Bank Feeds](bank-how-setup-bank-statement-service.md). Alternativamente, un socio de Microsoft puede ayudarlo a cumplir con los requisitos de su empresa o país.

La acción **Asignar texto a cuenta** le permite configurar asignaciones entre el texto de los pagos y la cuentas de débito, crédito y saldo específicas para que los pagos se contabilicen en las cuentas específicas al contabilizar el diario de conciliación de pagos. Asignar es útil; por ejemplo, para recibos de cobro o gastos periódicos, como las compras frecuentes de combustible para vehículos o comisiones bancarias e intereses que se producen periódicamente en el extracto bancario y no necesitan un documento empresarial relacionado. (Consulte el paso 10). Para más información, consulte [Asignar texto en pagos periódicos a cuentas para conciliación automática](receivables-how-map-text-recurring-payments-accounts-auto-reconcilliation.md).

Es posible que las líneas del diario no tengan una liquidación sugerida, lo que puede suceder por varios motivos. Por ejemplo, debido a que falta un documento o que un cliente pagó en exceso y hay un importe excesivo tras liquidar el pago en otra línea del diario. Para tales casos, puede utilizar la acción **Transferir diferencia a cuenta** para crear y contabilizar el movimiento de contabilidad que falta, por ejemplo, para un reembolso, que es necesario para aplicar el pago. (Consulte el paso 11). Para obtener más información, consulte [Conciliar pagos que no pueden liquidarse](receivables-how-reconcile-payments-cannot-apply-auto.md).

La función **Aplicar automáticamente** se usa automáticamente cuando se importa una información o archivo bancario con transacciones de pago, o cuando se activa para aplicar pagos en sus movimientos pendientes relacionados basados en una correspondencia de texto en una línea de extracto bancario (línea de diario) con texto en una o más movimientos pendientes. Esta automatización se basa en reglas que usted define en la página **Reglas de la aplicación de pago**, donde también define si una sugerencia de aplicación requiere revisión. Para obtener más información, consulte [Configurar reglas para la liquidación automática de pagos](receivables-how-set-up-payment-application-rules.md).

En las líneas de diario en las que un pago se ha aplicado automáticamente a un movimiento pendiente o a varios, el campo **Confianza de la correspondencia** tiene un valor de **Baja**, **Media** o **Alta** para indicar la calidad de la correspondencia de datos en la que se basa la aplicación de pago sugerida.

Algunas aplicaciones de pago requieren su revisión según lo definido por la regla de correspondencia utilizada, como las líneas con confianza de la correspondencia **Baja**. Otras líneas requieren su revisión y cambio manual porque hay un valor en el campo **Diferencia**. Para revisar una o más aplicaciones de pagos, elija el campo **Líneas a revisar** o **Líneas con diferencia** en la parte inferior. La página **Revisión de aplicación de pago** se abre y muestra toda la información relevante sobre el cliente o proveedor al que se aplica el pago, los detalles coincidentes y las acciones para procesar la línea, como la acción **Aceptar aplicación**. (Consulte los pasos 7 y 8)

Para cada línea de diario en la página **Diario de conciliación de pagos** podrá abrir la página **Liquidación de pago** para ver todos los candidatos con movimientos pendientes de pago y podrá ver información detallada para cada movimiento sobre la correspondencia de datos en la que se basa la liquidación de un pago. Aquí puede liquidar manualmente pagos o volver a liquidar pagos que se aplicaron automáticamente en un movimiento incorrecto. (Consulte el paso 10). Para obtener más información, vea [Revisar o liquidar pagos después de una liquidación automática](receivables-how-review-apply-payments-auto-application.md).

> [!NOTE]  
> Puede iniciar la importación de las transacciones bancarias al mismo tiempo que abre la página **Diario de conciliación de pagos** de un diario existente. El procedimiento siguiente describe cómo importar transacciones bancarias a la página **Diario de conciliación de pagos** una vez creado un nuevo diario.

## <a name="to-reconcile-payments-using-automatic-application" />Para conciliar los pagos con liquidación automática
1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Diarios de conciliación de pagos** y luego elija el enlace relacionado.
2. Para trabajar en un nuevo diario de conciliación de pago, seleccione la acción **Nuevo diario**.
3. En la página **Lista cuentas bancarias pago**, seleccione la cuenta bancaria que desee conciliar los pagos y, a continuación, haga clic en **Aceptar**.
   La página **Diario de conciliación de pagos** abre una ventana preparada para la cuenta bancaria seleccionada.
4. Seleccione la acción **Importar transacciones bancarias**.
   Si la cuenta bancaria del diario seleccionado no está configurada para importar transacciones bancarias, [!INCLUDE[d365fin](includes/d365fin_md.md)] lo ayudará a importarlas.
5. En la página **Seleccionar un archivo para importarlo**, seleccione el archivo que contiene las transacciones bancarias para los pagos que desee conciliar y, a continuación, haga clic en **Abrir**.  
6. Si se ha habilitado el servicio Envestnet Yodlee Bank Feeds, en la página **Filtro de extracto bancario** que se abre automáticamente, especifique el intervalo de fechas para que se importen los extractos bancarios.

    La página **Diario de conciliación de pagos** se rellena con líneas para pagos que representan transacciones bancarias en el extracto bancario importado.

     En las líneas de los pagos que se han liquidado automáticamente en sus movimientos pendientes relacionados, el campo **Confianza de la correspondencia** indica la calidad de la correspondencia de datos en la que se basa la liquidación de pago sugerida. Además, los campos **Nombre de cuenta**, **Tipo de cuenta** y **N.º de cuenta** muestran información sobre el cliente o el proveedor al que se liquida el pago.

    Las reglas controlan si las liquidaciones automáticas, las calidades de correspondencia y si las líneas requieren revisión. Puede editar las reglas para ajustar los resultados. Para obtener más información, consulte [Configurar reglas para la liquidación automática de pagos](receivables-how-set-up-payment-application-rules.md).

7. Para revisar, aceptar, eliminar o cambiar manualmente varias aplicaciones de pago que tienen un valor en el campo **Diferencia**, elija la acción **Líneas con diferencia** en la parte inferior.

    Se abre la página **Revisión de liquidación de pago** que muestra la primera liquidación a revisar. La próxima aplicación para revisar se mostrará en la página a medida que procese la anterior. La revisión incluye información sobre el cliente o proveedor al que se liquida el pago, los detalles coincidentes y las acciones para procesar la línea, como las acciones **Aceptar liquidación** y **Liquidar manualmente**.

8. Para revisar, aceptar o eliminar, o cambiar manualmente varias liquidaciones de pago que la regla ha configurado para que se revisen, elija la acción **Líneas para revisar**. 

9. Para cambiar una aplicación automática, seleccione una línea de diario y, a continuación, seleccione la acción **Aplicar manualmente** para volver a aplicar o para aplicar el pago manualmente en la página **Aplicación de pago**. Para obtener más información, vea [Revisar o liquidar pagos después de una liquidación automática](receivables-how-review-apply-payments-auto-application.md).

10. Seleccione una línea de diario desliquidado para un recibo de gasto o cobro periódico, como el de repostar gasolina y, a continuación, elija la acción **Asignar texto a cuenta**. Para más información, consulte [Asignación de texto en pagos periódicos a cuentas para conciliación automática](receivables-how-map-text-recurring-payments-accounts-auto-reconcilliation.md).

    Cuando haya terminado con la asignación de texto de pago a las cuentas, seleccione la acción **Liquidar manualmente**.

    Cuando se configura una correspondencia de texto a cuenta, la liquidación de pago automática resultante contendrá **Asignación de texto a cuenta: alta** en el campo **Confianza de la correspondencia**.

11. Si una línea de diario no tiene una liquidación sugerida porque no existe un movimiento contable en el que se pueda liquidar, elija la acción **Transferir diferencia a cuenta** para crear y contabilizar el movimiento de contabilidad que falta y que se necesita para liquidar el pago. Para obtener más información, vea [Conciliar pagos que no pueden liquidarse](receivables-how-reconcile-payments-cannot-apply-auto.md)

12. Cuando ya no sea necesario revisar más líneas y el campo **Diferencia** está en blanco en todas las líneas, elija la acción **Contabilizar** y luego elija una de las siguientes opciones:

    - **Registrar pagos y conciliar bancos**: para registrar los pagos como liquidados y cerrar los movimientos bancarios de la cuenta relacionada como reconciliados.
    - **Registrar solamente pagos**: para publicar solo los pagos como liquidados pero dejar abiertos los movimientos bancarios de cuentas bancarias relacionadas. Se requiere que concilie el banco por separado, por ejemplo: Para obtener más información, consulte [Conciliar el banco](bank-how-reconcile-bank-accounts-separately.md).
    - **Informe de prueba**: para revisar el resultado del registro antes de registrar. Se abre el informe **Estado de cuenta bancaria** y muestra los mismos campos que en la parte inferior de la página **Diario de conciliación de pagos**.

Cuando registra el diario de conciliación de pagos, se cierran los movimientos pendientes liquidados. Se actualizan las cuentas de cliente, proveedor o contables. En el caso de los pagos en las líneas de diario basados en la asignación de texto a cuenta, se actualizan las cuentas de cliente, proveedor y contabilidad especificadas. Para todas las líneas de diario, se crean movimientos de banco. Si selecciona la acción **Registrar pagos y conciliar banco**, todas las cuenta abiertas relacionadas con los movimientos de los clientes o los proveedores se cerrarán. Eso significa que la cuenta bancaria se concilia automáticamente por los pagos que registró mediante el diario.

Puede comparar el valor del campo **Saldo en cuenta bancaria después del registro** con el valor del campo **Saldo final extracto** para hacer un seguimiento cuando la cuenta bancaria se concilie según los pagos registrados.

> [!NOTE]  
>   Si no desea conciliar la cuenta bancaria de la página **Diario de conciliación de pagos**, debe usar la página **Conciliación banco**. Para obtener más información, consulte [Conciliar bancos](bank-how-reconcile-bank-accounts-separately.md).

## <a name="see-related-microsoft-trainingtrainingmodulesuse-journals-dynamics--business-central" />Consultar la [formación de Microsoft](/training/modules/use-journals-dynamics-365-business-central/) relacionada

## <a name="see-also" />Consulte también .

[Administrar cobros](receivables-manage-receivables.md)  
[Ccial](sales-manage-sales.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
