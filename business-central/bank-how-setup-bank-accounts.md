---
title: Configurar cuentas bancarias
description: Aprenda cómo se utilizan las cuentas bancarias en Business Central y cómo puede conciliar los importes con su banco.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'Yodlee, feed, stream'
ms.search.form: '370, 371, 372, 373, 375, 423, 424, 425, 426, 1240, 1280'
ms.date: 05/24/2024
ms.custom: bap-template
ms.service: dynamics-365-business-central
---
# Configurar cuentas bancarias

Utilice cuentas bancarias en [!INCLUDE[prod_short](includes/prod_short.md)] para hacer un seguimiento de las transacciones bancarias. Los bancos pueden expresarse en la divisa local (DL) o en una extranjera. Cuando haya configurado las cuentas bancarias también podrá imprimir cheques. Las cuentas bancarias también ofrecen características para [conciliación de pagos](receivables-apply-payments-auto-reconcile-bank-accounts.md), [conciliación bancaria](bank-how-reconcile-bank-accounts-separately.md) y la importación y exportación de archivos bancarios.

Puede incluir cuentas bancarias en las transacciones del diario general. Cada cuenta bancaria está vinculada a una cuenta en el plan de cuentas a través del grupo contable de la cuenta bancaria asignada. El uso de una cuenta bancaria en una transacción de pago crea automáticamente una entrada tanto en la cuenta bancaria como en la cuenta de contabilidad (G/L) conectada.  

Las cuentas bancarias funcionan de manera diferente dependiendo de si se especifica un código de divisa:

- Si no se especifica un código de moneda, todas las transacciones en la cuenta bancaria se realizan en la divisa local (DL) de la empresa actual. Si realiza una transacción para la cuenta en otra divisa, los importes se contabilizan en la cuenta en DL según el tipo de cambio de la divisa correspondiente. Cualquier cheque que se emita desde esta cuenta debe estar en ML. Si la cuenta bancaria se utiliza en un diario, la línea del diario usa automáticamente el código de divisa en blanco.  
  
- Si se especifica un código de divisa, todas las transacciones realizadas a esta cuenta, y todos los cheques emitidos desde ella, deberán utilizar la misma moneda que la cuenta.

Puede ahorrar tiempo en la introducción de datos haciendo que una cuenta bancaria sea la cuenta predeterminada que se utilizará para la divisa especificada para la cuenta. Si lo hace, la cuenta se asigna a documentos de ventas y servicios que utilicen la divisa. Para hacer que la cuenta sea la predeterminada para documentos de ventas y servicios, en la página **Ficha banco**, active el botón de alternancia **Usar como predeterminada para divisa**. Si es necesario, puede elegir una cuenta diferente cuando esté trabajando en un documento.

Una cuenta bancaria es una parte integral de [!INCLUDE[prod_short](includes/prod_short.md)] y juega un papel en muchas otras capacidades. La siguiente ilustración muestra las relaciones más importantes:

![Ilustración de relaciones de cuentas bancarias.](media/Set-Up-Bank-Accounts/Bank_Account_Relations.png)

La creación de una cuenta bancaria hace que esté disponible en todos los lugares que se muestran en la ilustración, y se reflejan en la cuenta de mayor y en la página **Información empresa**.

Las cuentas bancarias suelen controlarse diariamente para garantizar que los nuevos pagos de los clientes se registran lo antes posible. Registrar los pagos con rapidez ayuda a garantizar que el estado real de un cliente se refleje en [!INCLUDE[prod_short](includes/prod_short.md)]. Mantener al día el estado de los pagos de los clientes ayuda a los comerciales, contables y otros empleados a realizar llamadas innecesarias sobre facturas vencidas o retrasos en los envíos.  

![Ilustración de pago bancario.](media/Set-Up-Bank-Accounts/Bank-payment-flow.png)

Otra tarea es importar los pagos en divisa del proveedor con los tipos de cambio realizados para asegurarse de que el estado real de los proveedores esté actualizado. Usar la capacidad de [conciliación de pagos](receivables-apply-payments-auto-reconcile-bank-accounts.md) es la forma más fácil de hacerlo. En el **Diario de conciliación de pagos** puede importar transacciones bancarias directamente desde una aplicación bancaria en línea y publicarlas de forma más o menos automática. El diario identifica y publica automáticamente las siguientes transacciones:  

- Pagos de adeudo directo de clientes.  
- Pagos de clientes de facturas únicas.  
- Pagos de suma total de clientes.  
- Pagos de clientes en divisas extranjeras.  
- Pagos a proveedores.  
- Pagos a proveedores en divisa extranjera.  
- Pagos a proveedores y suscripciones que son periódicos.  
- Gastos e intereses bancarios.  

La conciliación de pagos proporciona un ahorro significativo de tiempo en la contabilización de pagos entrantes y salientes. Sin embargo, las transacciones en la cuenta bancaria en [!INCLUDE[prod_short](includes/prod_short.md)] no se consideran 100% correctas hasta que ejecute una conciliación bancaria.  

La conciliación bancaria es la forma de asegurarse de que la cuenta bancaria en [!INCLUDE[prod_short](includes/prod_short.md)] coincide con la cuenta externa en el banco.  

 ![Ilustración de la conciliación de cuentas bancarias.](media/Set-Up-Bank-Accounts/BankReconciliation.png)

En la ilustración, el lado izquierdo representa la cuenta bancaria en [!INCLUDE[prod_short](includes/prod_short.md)], y el lado de más a la derecha representa las transacciones importadas del banco a través de la aplicación bancaria en línea. El diagrama del medio muestra las transacciones de ambos lados, que conforman la conciliación bancaria.

De la cuenta bancaria en [!INCLUDE[prod_short](includes/prod_short.md)], la mayoría de las transacciones deben ser conocidas por el banco físico. Las pocas excepciones incluyen los siguientes casos:  

- Correcciones publicadas en [!INCLUDE[prod_short](includes/prod_short.md)].  
- Cheques emitidos que no se cobran.
- Pagos a proveedores que no han sido aprobados por el banco.  

Desde la cuenta física en el banco, llegan todo el tiempo transacciones que no fueron identificadas en el diario de conciliación de pagos, como las siguientes transacciones:  

- Nuevas suscripciones a proveedores  
- Pagos de clientes sin descripción
- Intereses bancarios
- Gastos bancarios
- Cargos de tarjeta de crédito aún no informados

Cuanta mejor información de asignación realice en el diario de conciliación de pagos, más transacciones se registrarán automáticamente y más fácil será la conciliación bancaria periódica.

El siguiente vídeo muestra los pasos básicos para configurar una cuenta bancaria en [!INCLUDE[prod_short](includes/prod_short.md)].

<br /><br />

> [!Video https://www.microsoft.com/videoplayer/embed/RE3Vhpl?rel=0]

> [!WARNING]
> Algunos campos pueden contener datos confidenciales, como los campos **Cód. sucursal banco**, **N.º cuenta bancaria**, **Código SWIFT**, y **Código IBAN**. Más información en [Supervisar campos confidenciales](across-log-changes.md#monitor-sensitive-fields).

## Para configurar bancos

1. Elija el icono ![Bombilla que abre la característica Dígame 1.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Cuentas bancarias** y luego elija el vínculo relacionado.
2. En la página **Cuentas bancarias**, elija la acción **Nuevo**.
3. Rellene los campos según sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    Un ejemplo sería el campo **Grupo de contabilización de cuenta bancaria**, que conecta la cuenta bancaria con la cuenta de mayor subyacente en el balance. Obtenga más información en [Configurar grupos contables](finance-posting-groups.md).

> [!TIP]
> Algunos campos están ocultos hasta que elige la acción **Mostrar más**, normalmente porque se utilizan raramente. Otros deben agregarse mediante personalización. Obtenga más información en [Personalizar el área de trabajo](ui-personalization-user.md).

Puede crear tantas cuentas bancarias como necesite para su negocio. Para cada cuenta bancaria, debe especificar información que haga que la cuenta bancaria sea identificable de forma única. Esta información incluye la dirección geográfica del banco, series de números para diferentes tipos de transacciones, como adeudo directo y transferencias de crédito, la divisa en la que se especifican los importes y la información que se utiliza para importar extractos bancarios. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
<!--
The following table explains key fields.

|Field|Description|  
|---------------------------------|---------------------------------------|  
|**General FastTab**||
|No.|Specifies the number of the bank account, according to the specified number series. If the number series allow manual numbering, any alphanumeric code up to 20 characters can be used.|
|Name|The Name of the bank holding the account.|
|Bank Branch No.|Typically used to identify the bank branch in domestic payments, it's very often considered a sensitive field. Learn more at [Monitoring Sensitive Fields](across-log-changes.md#monitoring-sensitive-fields).|
|Bank Account No.|Typically used to identify the bank account number in domestic payments, it's very often considered a sensitive field. Learn more at [Monitoring Sensitive Fields](across-log-changes.md#monitoring-sensitive-fields).|
|Balance|Shows the bank account balance in the account currency.|
|Balance (LCY)|Shows the bank account balance in the local currency (LCY).|
|Our Contact Code|Specifies a code to identify the employee responsible for this bank account. The employee must be created in the **Salesperson/Purchaser** table.|
|Blocked|Specifies the related record is blocked from being posted in transactions, for example the account is obsolete after a bank change.|
|SEPA Direct Debit Exp. Format|Specifies the single euro payments area (SEPA) format of the bank file to be exported when you choose **Create Direct Debit File** on the **Direct Debit Collect. Entries** page. Learn more at [SEPA Direct Debit in Business Central](finance-collect-payments-with-sepa-direct-debit.md).|
|Credit Transfer Msg. Nos.|Specifies the number series for bank instruction messages created with the export file you create from the **Direct Debit Collect. Entries** page. Learn more at [SEPA Direct Debit in Business Central](finance-collect-payments-with-sepa-direct-debit.md).|
|Direct Debit Msg. Nos.|Specifies the number series to be used on the direct debit file you export for a direct debit collection entry on the **Direct Debit Collect. Entries** page. Learn more at [SEPA Direct Debit in Business Central](finance-collect-payments-with-sepa-direct-debit.md).|
|Creditor No.|Specifies your company as the creditor in connection with payment collection from customers using SEPA direct debit. Learn more at [SEPA Direct Debit in Business Central](finance-collect-payments-with-sepa-direct-debit.md).|
|Bank Clearing Standard|The national bank names register used for the sender bank account.|
|Bank Clearing Code|Specifies the code for bank clearing required according to the format standard you selected in the **Bank Clearing Standard** field. The bank clearing code can be used as an alternative to SWIFT and IBAN to identify your bank as the sender of a bank transfer.|
|Last Date Modified|Date of the latest modification of the bank account.|
|**Payment Matching**||
|Disable Automatic Payment Matching|Specifies whether or not to disable automatic payment matching after importing bank transactions for this bank account. Learn more at [Payment Reconciliation](receivables-apply-payments-auto-reconcile-bank-accounts.md).|
|**Payment Match Tolerance**||
|Match Tolerance Type|Specifies the tolerance the automatic payment application function will use to apply the *Amount Incl. Tolerance Matched* rule for this bank account. Read more in [Payment Reconciliation](receivables-apply-payments-auto-reconcile-bank-accounts.md).|
|Match Tolerance Value|Specifies if the automatic payment application function will apply the *Amount Incl. Tolerance Matched* rule by percentage or amount. Learn more at [Payment Reconciliation](receivables-apply-payments-auto-reconcile-bank-accounts.md).|
|**Hidden Fields**||
|Search Name|Specifies an alternate name you can use to search for the record in question when you can't remember the value in the **Name** field.|
|Min. Balance|Specifies a minimum balance for the bank account. This field is for information purposes only.|
|Positive Pay Export Code|Specifies a code for the data exchange definition managing the export of positive-pay files. Learn more at [Export Positive Pay Files](finance-how-positive-pay.md).|
|**Communication FastTab**||
|Address|The address of the bank branch.|
|Address 2|An additional address field for the bank branch.|
|Post Code|The post code of the bank branch.|
|City|The city of the bank branch.|
|Country/Region Code|The country/region code of the bank branch.|
|Phone No.|The phone number of the bank branch.|
|Mobile Phone No.|The mobile phone number of the bank branch.|
|Contact|The main contact in the bank branch. Additional contacts can be created in the **Contacts** module.|
|Fax No.|The fax number of the bank branch.|
|Email|The email address of the bank branch.|
|Home Page|The home page address of the bank branch website.|
|**Posting FastTab**||
|Currency Code|Specifies the relevant currency code for the bank account. Applying a currency code to a bank account limits all transactions to only using the applied currency code. Leaving the currency code blank allows transactions in all currencies, however, the amount will eventually be converted to the LCY using the applied currency rate. Checks issued from this account follow the same rules.|
|Last Check No.|The number of the latest check issued from this account.|
|Transit No.|Specifies a bank identification number of your own choice.|
|Last Statement No.|The number of the latest bank reconciliation posted to this account. Learn more at [Reconcile Bank Accounts](bank-how-reconcile-bank-accounts-separately.md).|
|Last Payment Statement No.|The number of the latest payment reconciliation posted to this account. Learn more at [Payment Reconciliation](receivables-apply-payments-auto-reconcile-bank-accounts.md).|
|Last Bank Statement|The ending balance of the last bank statement. Learn more at [Reconcile Bank Accounts](bank-how-reconcile-bank-accounts-separately.md).|
|Bank Acc. Posting Group|Specifies a code for the bank account's posting group. The **Bank Acc. Posting Group** connects the bank account to the G/L account in the balance sheet.|
|**Transfer**||
|Transit No.|Specifies a bank identification number of your own choice.|
|SWIFT Code|Specifies the international bank identifier (SWIFT) code of the bank in which you have account. The SWIFT code is very often considered a sensitive field. Learn more at [Monitoring Sensitive Fields](across-log-changes.md#monitoring-sensitive-fields).|
|IBAN|Specifies the bank account's international bank account number (IBAN). The IBAN code is very often considered a sensitive field. Learn more at [Monitoring Sensitive Fields](across-log-changes.md#monitoring-sensitive-fields).|
|Bank Statement Import Format|Specifies the format of the bank statement file imported into this bank account. This format is used in both the payment reconciliation journals and bank account reconciliations.|
|Payment Export Format|Specifies the format of the bank file that is exported when you choose **Export Payments to File** on the **Payment Journal** page.|
-->

## Para introducir un saldo inicial

Para completar el campo **Saldo** con un saldo inicial, debe publicar un movimiento de cuenta bancaria con el importe en cuestión. La entrada se contabiliza mediante una conciliación de cuentas bancarias. Obtenga más información en [Conciliar cuentas bancarias](bank-how-reconcile-bank-accounts-separately.md).  
>
> De forma alternativa, puede implementar el saldo inicial como parte de la creación de datos generales en nuevas compañías mediante la guía de configuración asistida **Migrar datos empresariales**. Obtenga más información en [Preparación para hacer negocios](ui-get-ready-business.md).  

> [!IMPORTANT]
> No registre el saldo de apertura directamente en la contabilidad general. Los asientos en la cuenta de contabilidad que se contabilizaron directamente en ella suelen impedirle conciliar la cuenta bancaria. Con las cuentas bancarias en moneda extranjera, el registro directo genera diferencias que se acumulan a medida que contabiliza más conciliaciones bancarias. Normalmente, contabiliza el saldo bancario inicial directamente en la cuenta bancaria y el importe termina en la cuenta del L/M. Como alternativa, más tarde, puede revertirlo contra una cuenta de contabilidad que utilice para equilibrar el saldo inicial del libro mayor. En cualquier caso, debe equilibrar cualquier registro directo en la cuenta de contabilidad antes de iniciar su primera conciliación bancaria, especialmente si la cuenta bancaria está en una divisa extranjera.

## Para configurar la cuenta para la importación o exportación de archivos bancarios

Los campos relacionados con la importación y la exportación de archivos o fuentes de banco se encuentran en la ficha desplegable **Transferencia** en la página **Ficha banco**. Más información en [Usar la extensión AMC Banking 365 Fundamentals](ui-extensions-amc-banking.md) y [Configurar el servicio Envestnet Yodlee Bank Feeds](bank-how-setup-bank-statement-service.md).

1. Elija el icono ![Bombilla que abre la característica Dígame 2.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Cuentas bancarias** y luego elija el vínculo relacionado.
2. Abra la ficha de un banco del que exportará archivos de banco, o al que los importará.
3. En la ficha desplegable **Transferencia**, rellene los campos como sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!NOTE]  
> Distintos servicios de exportación de archivos y sus formatos requieren valores de configuración diferentes en la página **Ficha banco**. Estará informado sobre valores de configuración incorrectos o que faltan cuando exporte el archivo. Lea las descripciones breves de los campos atentamente o consulte los temas relacionados del procedimiento. Por ejemplo, exportar un archivo de pago para la transferencia electrónica de fondos (EFT) de Norteamérica requiere que tanto el campo **Nº último aviso pago** como el campo **Nº tránsito** estén rellenados. Más información en [Exportar pagos a un archivo bancario](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md#exporting-payments-to-a-bank-file).

Los campos de la ficha desplegable **Tránsito** de la cuenta bancaria tienen diferentes propósitos, dependiendo de si el pago es entrante o saliente.

La siguiente ilustración muestra la ruta de los pagos entrantes. Los números de la descripción corresponden con los números de la ilustración.

:::row:::
    :::column:::

1. Las transacciones se exportan desde la cuenta bancaria en un formato .csv legible por humanos o en el propio formato del banco.
2. La definición de intercambio de datos asigna la información del archivo a los campos en [!INCLUDE[prod_short](includes/prod_short.md)]. Más información en [Configurar intercambio de datos](across-set-up-data-exchange.md)
3. La configuración de exportación/importación de datos define la exportación o la importación y se vincula a la definición de intercambio de datos.
4. El formato de importación de extractos bancarios vincula la configuración de importación a la cuenta bancaria.
5. Los pagos se importan a través del **Diario de conciliación de pagos** o la página **Conciliación de cuentas bancarias**.

  :::column-end:::
  :::column:::

        ![Ilustración de pagos recibidos del banco a cuentas bancarias.](media/Set-Up-Bank-Accounts/payments-in-and-out-1.png)

  :::column-end:::
:::row-end:::

Los pagos entrantes se importan siempre a través del **Diario de conciliación de pagos** o directamente en la página **Conciliación de cuentas bancarias**. Por el contrario, los pagos efectuados pueden originarse en cualquier diario de pagos. El único requisito previo es que se debe seleccionar el campo **Permitir exportación de pagos** en la sección del diario de pagos correspondiente.

La siguiente ilustración muestra la ruta de los pagos salientes. Los números de la descripción corresponden con los números de la ilustración.

:::row:::
    :::column:::

6. Las transacciones rellenan un diario de pagos que se ha preparado para exportar pagos al archivo.
7. El formato de importación de extractos bancarios vincula la configuración de importación a la cuenta bancaria.
8. La configuración de exportación/importación de datos define la exportación o la importación y se vincula a la definición de intercambio de datos.
9. La definición de intercambio de datos asigna la información del archivo a los campos en [!INCLUDE[prod_short](includes/prod_short.md)]. Más información en [Configurar intercambio de datos](across-set-up-data-exchange.md)
10. Los pagos se exportan desde el diario de pagos y se importan en la cuenta bancaria.

  :::column-end:::
  :::column:::

        ![Ilustración de pagos desde cuentas bancarias que se envían al banco.](media/Set-Up-Bank-Accounts/payments-in-and-out-2.png)

  :::column-end:::
:::row-end:::

## Para configurar cuentas bancarias de proveedor para exportar archivos bancarios

Los campos de la ficha desplegable **Transferencia** en la página **Ficha banco proveedor** están relacionados con la exportación de archivos o fuentes de banco. Más información en [Usar la extensión AMC Banking 365 Fundamentals](ui-extensions-amc-banking.md) y [Exportar pagos a un archivo bancario](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md#exporting-payments-to-a-bank-file).

[!INCLUDE[purchase-vendor-bank-account](includes/purchase-vendor-bank-account.md)]

## Cambiar su cuenta bancaria

Para utilizar una cuenta bancaria diferente para su negocio, debe crear la nueva cuenta bancaria en [!INCLUDE[prod_short](includes/prod_short.md)]. Le recomendamos que no reemplace simplemente la información sobre la cuenta que está utilizando actualmente porque puede causar datos incorrectos. Por ejemplo, es posible que su saldo inicial sea incorrecto o que la fuente de su banco deje de funcionar correctamente. Es importante que mantenga separadas las cuentas actual y nueva.

Después de crear la nueva cuenta bancaria, también debe crear un nuevo grupo contable de banco y asignarlo a una nueva cuenta de contabilidad. Puede reutilizar un grupo contable de banco existente y las transacciones bancarias se contabilizan en las mismas cuentas de contabilidad que las otras cuentas bancarias que comparten el grupo contable de banco. Sin embargo, le recomendamos crear un nuevo grupo contable de banco y una cuenta de contabilidad para que las conciliaciones sean más fáciles de realizar.

> [!NOTE]
> Recuerde que la información de cuentas bancarias en las facturas de venta abiertas todavía muestra la cuenta bancaria original. En consecuencia, es probable que los pagos se sigan contabilizando en esa cuenta. Le recomendamos que mantenga activas ambas cuentas durante un período de tiempo después del cambio.

Para obtener una vista más condensada de sus cuentas de caja en los informes financieros, utilice las cuentas **Principio-Total** y **Fin-Total** en su plan de cuentas, las filas **Sumatorio** en informes financieros o categorías de cuentas de contabilidad. Más información en [Inteligencia empresarial y Financial Reporting](bi.md).

## Consulte también .

[Configurar banca](bank-setup-banking.md)  
[Configurar los grupos contables](finance-posting-groups.md)  
[Conciliar bancos](bank-manage-bank-accounts.md)  
[Configurar el servicio Envestnet Yodlee Bank Feeds](bank-how-setup-bank-statement-service.md)  
[Adeudo directo SEPA en Business Central](finance-collect-payments-with-sepa-direct-debit.md)  
[Para configurar su cuenta bancaria para adeudo directo SEPA](finance-collect-payments-with-sepa-direct-debit.md#to-set-up-your-bank-account-for-sepa-direct-debit)  
[Para configurar una cuenta bancaria para transferencia de crédito SEPA](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md#to-set-up-a-bank-account-for-sepa-credit-transfer)  
[Efectúe pagos con la extensión AMC Banking 365 Fundamentals o transferencia de crédito SEPA](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md)  
[Conciliación de pagos](receivables-apply-payments-auto-reconcile-bank-accounts.md)  
[Descripción de contabilidad y plan de cuentas](finance-general-ledger.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
