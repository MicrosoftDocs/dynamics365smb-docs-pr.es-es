---
title: Trabajar con diarios generales para registrar directamente en G/L
description: 'Obtenga información sobre el uso de diarios para registrar transacciones financieras en cuentas generales y otras cuentas, como cuentas bancarias y de proveedor.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.date: 08/29/2023
ms.custom: bap-template
ms.search.keywords: 'journals, recurring, accrual, renumber, bulk-post'
ms.search.form: '39, 101, 102, 182, 184, 185, 201, 207, 250, 251, 253, 255, 256, 261, 262, 283, 519, 750, 751, 752, 753, 754, 755, 12409, 12410, 12411, 1290, 10101, 11400, 11402, 11403, 11405, 11300, 2000000, 2000001, 2000003, 2000020, 2000021, 2000022'
---
# Trabajar con diarios generales

La mayoría de las transacciones financieras se registran en la contabilidad a través de documentos, como facturas de compra y pedidos de ventas. Sin embargo, también puede procesar actividades comerciales como:

* Compras
* Pagos
* Uso de diarios recurrentes para contabilizar acumulaciones
* Reembolso de gastos de empleados mediante la contabilización de líneas de diario en diarios  

La mayoría de los diarios se basan en el diario general y puede procesar todas las transacciones en la página **Diario general**. Más información en [Registrar transacciones directamente en la contabilidad](finance-how-post-transactions-directly.md).  

Por ejemplo, puede utilizar los gastos de empleados de puestos para el reembolso. Más información en [Registro y reembolso de los costes de los empleados](finance-how-record-reimburse-employee-expenses.md).

Sin embargo, [!INCLUDE [prod_short](includes/prod_short.md)] también ofrece los diarios que están optimizados para tipos específicos de transacciones, como el **Diario de pagos** para registrar pagos. Obtenga más información en [Registrar pagos y reembolsos en el diario de pagos](payables-how-post-payments-refunds.md).  

Utiliza diarios generales para registrar transacciones financieras de cuentas de la contabilidad general y otras cuentas. Las otras cuentas incluyen cuentas bancarias, de clientes, de proveedores y de empleados. La contabilización con un diario general crea entradas en las cuentas del libro mayor incluso cuando, por ejemplo, contabiliza una línea de diario en una cuenta de cliente. El asiento se contabiliza en una cuenta de cobros del libro mayor a través de un grupo de contabilización.

La información que introduzca en un diario es temporal y se puede modificar mientras se encuentre en el diario. Al registrar el diario, la información se transfiere a movimientos en cuentas individuales, donde no se puede modificar. Sin embargo, puede desliquidar los movimientos registrados y puede registrar movimientos de inversión o correctores. Obtenga más información en [Revertir los registros de diario y deshacer los recibos/envíos](finance-how-reverse-journal-posting.md).

> [!NOTE]
> [!INCLUDE[journal-showhide-columns-inline-tip](includes/journal-showhide-columns-inline-tip.md)]  

## Agregar contexto a las transacciones del diario general

Cuando crea un diario, puede agregar enlaces que ofrezcan contexto a sus transacciones. Cuando publica el diario, [!INCLUDE [prod_short](includes/prod_short.md)] copia los enlaces al diario publicado y los asientos contables que crea el diario. Por ejemplo, proporcionar enlaces puede facilitarle la vida a su auditor. Si guarda imágenes de sus recibos de gastos en el sitio SharePoint de su empresa, puede agregar enlaces a los archivos. Cuando publica el diario para presentar sus gastos, su auditor puede acceder rápidamente a los archivos de recibos.

## Usar plantillas y secciones del diario

Existen varias plantillas de diario general. Cada plantilla de diario se representa mediante una página específica con funciones particulares y los campos que se requieren para admitir estas funciones, como la página **Diario de conciliación de pagos** para procesar pagos bancarios y la página **Diario de pagos** para pagar a sus proveedores o reembolsar a sus empleados. Obtenga más información en [Realizar pagos](payables-make-payments.md) y [Conciliar los pagos de clientes con el diario de recibos de efectivo o de los movimientos de cliente](receivables-how-apply-sales-transactions-manually.md).

Para cada plantilla de diario, puede configurar su propio diario personal como una sección de diario. Por ejemplo, puede definir su propia sección de diario del diario de pagos que tiene su diseño y configuración personal. La sugerencia siguiente es un ejemplo de cómo personalizar un diario.

> [!TIP]  
> Si marca la casilla **Proponer importe de compensación** en la línea de su sección en la página **Secciones diario general**, a continuación, el campo **Importe**, por ejemplo, las líneas de diario general del mismo número de documento se rellena automáticamente con el valor necesario para incluir el saldo del documento. Obtenga más información en [Permitir que [!INCLUDE[prod_short](includes/prod_short.md)] proponga valores](ui-let-system-suggest-values.md).

> [!TIP]
> Puede agregar o eliminar campos en diarios personalizándolos. Obtenga más información en [Personalizar el área de trabajo](ui-personalization-user.md).

### Validación de lotes de diario general

Puede activar una verificación de antecedentes que ayudará a evitar retrasos al publicar. La comprobación le notificará cuando un error en el diario financiero en el que está trabajando le impida contabilizar el diario. En la página **Lote de diario general** puede elegir **Comprobación de errores de fondo** para hacer que [!INCLUDE[prod_short](includes/prod_short.md)] valide los diarios de finanzas, como los diarios generales o de pagos, mientras trabaja en ellos.

Cuando habilita la validación, el Cuadro informativo **Comprobación de diario** mostrará los problemas en la línea actual y en todo el lote. La validación ocurre cuando carga una sección de diario de finanzas y cuando elige otra línea de diario. La ventana **Total de problemas** del Cuadro informativo muestra el número total de problemas que [!INCLUDE[prod_short](includes/prod_short.md)] ha encontrado y puede elegirla para abrirla y ver una descripción general de los problemas.

Puede usar las acciones **Mostrar líneas con problemas** y **Mostrar todas las líneas** para alternar entre líneas del diario que tienen o no tienen problemas. El cuadro informativo **Detalles de línea del diario** proporciona una descripción general rápida y acceso a los datos desde las líneas del diario, como la cuenta, el cliente o el proveedor, así como la configuración de contabilización para cuentas específicas.

[!INCLUDE [background_doc_journal_check](includes/background_doc_journal_check.md)]  

## Descripción de las cuentas principales y las cuentas de contrapartida

Si ha configurado cuentas de contrapartida predeterminadas para las secciones del diario en la página **Diarios generales**, la cuenta de contrapartida se rellenará automáticamente cuando rellene el campo **Nº cuenta**. En caso contrario, deberá rellenar manualmente los campos **Nº cuenta** y **Cta. contrapartida**. Un importe positivo en el campo **Importe** se adeuda en la cuenta principal y se carga en la cuenta de contrapartida. Un importe negativo se carga en la cuenta principal y se adeuda en la cuenta de contrapartida.

> [!NOTE]  
> El IVA se calcula de manera independiente para la cuenta principal y la cuenta de contrapartida, para que puedan utilizar diferentes tipos porcentuales de IVA.

## Trabajar con diarios periódicos

Un diario periódico es un diario general con campos específicos para administrar las transacciones que registre frecuentemente con pocos cambios o con ninguno. Por ejemplo, transacciones de gastos como alquiler, suscripciones, electricidad y calefacción. El uso de diarios recurrentes le permite contabilizar importes fijos y variables y especificar entradas de reversión automática para el día posterior a la fecha de contabilización. Las claves de asignación le permiten dividir los movimientos periódicos entre varias cuentas. Obtenga más información en [Asignación de importes de diario periódicos a varias cuentas](#allocating-recurring-journal-amounts-to-several-accounts).

En un diario periódico, crea las entradas que se van a registrar con regularidad solo una vez. Por ejemplo, las cuentas, las dimensiones, los valores de dimensiones y demás, permanecen en el diario después del registro. Si se necesitan cambios, puede hacerlos cada vez que publique.

### Campo Periodicidad

El campo **Periodicidad** es importante. Determina la forma en que se tratará el importe en la línea de diario una vez realizado el registro. Por ejemplo, si usa el mismo importe cada vez que se registra la línea, puede permitir que el valor se mantenga. Si usa las mismas cuentas y texto de la línea, pero el importe varía en cada una, puede optar por borrar el importe después de cada registro.

| Para | Vea |
| --- | --- |
|F Fijo|El importe de la línea del diario permanecerá una vez realizado el registro.|
|V Variable|El importe de la línea del diario se borrará una vez realizado el registro.|
|S Saldo|El importe registrado en la cuenta de la línea se distribuirá entre las cuentas especificadas para la línea de la tabla Diario gen. distribución. El saldo de la cuenta se establecerá a cero. No olvide rellenar el campo **% Distribución** en la página **Asignaciones**. Para obtener más información, consulte [Asignación de importes de diario periódicos a varias cuentas](#allocating-recurring-journal-amounts-to-several-accounts).|
|CF Contraasiento fijo|El importe de la línea del diario se mantendrá después del registro y se registrará un movimiento de contrapartida al día siguiente.|
|CV Contraasiento variable|El importe de la línea del diario se borrará después del registro y se registrará un movimiento de contrapartida al día siguiente.|
|CS Contraasiento de saldo|El importe registrado en la cuenta de la línea se distribuirá entre las cuentas especificadas para la línea de la página **Asignaciones**. El saldo en la cuenta se establecerá en cero y se contabilizará un movimiento de saldo el día siguiente.|
|SD Saldo por dimensión|La línea de diario asigna los costes según el saldo de una cuenta por dimensión. Se le pedirá que configure los filtros de dimensión que se utilizarán para calcular el saldo de la cuenta de origen por dimensión desde la que desea asignar los costes. Alternativamente, elija más tarde la acción **Establecer filtros de dimensión**.|
|Contraasiento saldo RBD por dimensión|La línea de diario asigna los costes según el contraasiento una cuenta por dimensión. Se le pedirá que configure los filtros de dimensión que se utilizarán para calcular el saldo de la cuenta de origen por dimensión desde la que desea asignar los costes. También puede elegir más tarde la acción **Establecer filtros de dimensión**.|

> [!NOTE]  
> Los campos de IVA se pueden rellenar en la línea del diario periódico o en la línea del diario de distribución, pero no en ambas. Es decir, sólo se pueden rellenar en la página **Asignaciones** si no se han rellenado las líneas correspondientes en el diario periódico.

### Campo Frecuencia repetición

Este campo de fórmula de fecha determina la frecuencia con la que se registra la entrada en la línea del diario y debe completarse. Obtenga más información en [Usar fórmulas de fecha](ui-enter-date-ranges.md#use-date-formulas).

#### Ejemplos

Si la línea de diario debe registrarse cada mes, escriba "1M". Después de cada registro, la fecha del campo **Fecha registro** se actualizará con la fecha del mes siguiente.

Si desea registrar un movimiento el último día de cada mes, opte por una de estas posibilidades:

* Registre el primer movimiento el último día del mes y escriba la fórmula 1D+1M-1D (1 día + 1 mes - 1 día). Con esta fórmula, se calcula correctamente la fecha de registro con independencia de los días que tenga el mes.

* Registre el primer movimiento de cualquier día del mes e introduzca la fórmula 1M+CM. Con esta fórmula, la fecha de registro será después de un mes completo + los días que faltan del mes actual.

### Campo fecha caducidad

Este campo determina la fecha en que se registrará la línea por última vez. La línea no se registrará después de esta fecha.

La ventaja de usar el campo fecha de caducidad es que la línea no se borrará del diario inmediatamente. Puede introducir una fecha posterior para poder utilizar la línea en el futuro.

Si el campo se deja en blanco, la línea se registrará cada vez que se elimine del diario.

### Asignación de importes de diario periódicos a varias cuentas

En la página **Diario general periódico**, puede elegir la acción **Asignaciones** para especificar cómo asignar importes de la línea del diario periódico a varias cuentas y dimensiones. La asignación funciona como línea de cuenta de contrapartida a la del diario periódico.

Al igual que un diario recurrente, ingresa una asignación una vez y permanece en el diario de asignación después de la publicación. No es necesario que ingrese cantidades y asignaciones cada vez que registre la línea de diario recurrente.

Si el método periódico en el diario periódico está establecido en **Saldo** o en **Contraasiento saldo**, no se tendrá en cuenta ningún código de valor de dimensión global en el diario periódico cuando la cuenta esté establecida en cero. Si asigna una línea periódica a valores de dimensión en la página **Asignaciones**, solo se creará una entrada reversible.

> [!NOTE]
> Si asigna una línea del diario periódico que contenga un código de valor de dimensión, no introduzca el mismo código en la página **Asignaciones**. De lo contrario, los valores de dimensión serán incorrectas.  

Para asignar importes de diario recurrentes según las dimensiones, establezca el campo **Método recurrente** en **Saldo por dimensión** o **Contraasiento de saldo por dimensión**. Si el método periódico del diario periódico está establecido en **Saldo por dimensión** o en **Contraasiento de saldo por dimensión**, no se tendrá en cuenta ningún código de valor de dimensión global en el diario periódico cuando la cuenta esté establecida en cero. Si asigna una línea periódica a valores de dimensión en la página **Asignaciones**, luego se crean contraasientos que coinciden con el número de combinaciones de valores de dimensión que componen el saldo. Si asigna el saldo de la cuenta a través del diario periódico que contiene un código de valor de dimensión, recuerde usar **Saldo por dimensión** o **Contraasiento de saldo por dimensión** para asegurarse de que los valores de dimensión estén correctamente equilibrados o invertidos con respecto a la cuenta de origen.  

Por ejemplo, su empresa tiene un par de unidades de negocio y varios departamentos que sus controladores han configurado como dimensiones. Para acelerar el proceso de entrada de facturas de compra, decide solicitar a los empleados de cuentas de proveedores que introduzcan solo las dimensiones de la unidad de negocio. Dado que cada unidad de negocio tiene claves de asignación específicas para la dimensión Departamento, como en función del número de empleados, puede utilizar los métodos periódicos **SD Saldo por dimensión** o **RSD Contraasiento de saldo por dimensión** para reasignar los gastos de cada unidad de negocio a los departamentos adecuados, según las claves de asignación.  

> [!NOTE]
> Las dimensiones que establezca en las líneas de asignación no se calculan automáticamente y debe especificar qué valores de dimensión deben establecerse en las cuentas de asignación. En caso de que desee conservar el vínculo entre la dimensión de la cuenta de origen y la dimensión de la cuenta de asignación, le recomendamos que utilice las capacidades de [Contabilidad de costos](finance-about-cost-accounting.md) en su lugar.

#### Ejemplo: Asignación de pagos de alquiler a diferentes departamentos

Si usted paga un alquiler mensual, tendrá que introducir el importe en la cuenta de caja en una línea del diario periódico. En la página **Asignaciones** puede usar la dimensión Departamento dividir el gasto entre varios departamentos. Por ejemplo, según la cantidad de metros cuadrados que ocupe cada departamento. El cálculo se basa en el porcentaje de asignación en cada línea. Se pueden ubicar de distintas maneras:

* Ingrese diferentes cuentas en diferentes líneas de asignación para dividir el gasto de alquiler entre varias cuentas.
* Ingrese la misma cuenta pero use diferentes códigos de valor de dimensión para la dimensión Departamento en cada línea.

[!INCLUDE [rev-general-journal](includes/rev-general-journal.md)]

### Cálculo de la fecha de reversión

Al utilizar diarios generales periódicos para contabilizar acumulaciones al final de un período, es importante tener un control total sobre los asientos de reversión. En la página **Diarios generales periódicos**, el campo **Cálculo de la fecha de reversión** le permite controlar la fecha en que se publicarán las entradas de reversión cuando se utilicen métodos periódicos de reversión.

#### Ejemplo

Las acumulaciones generalmente se contabilizan con métodos periódicos **Fijos**, **Variables** o de **Saldo** en la línea del diario. La fecha de registro del importe contabilizado en la cuenta en la línea de diario se calcula utilizando la frecuencia periódica. La fecha de registro del movimiento de contrapartida se calcula utilizando el campo **Cálculo de la fecha de reversión**, como sigue:

* Si el campo está en blanco, el movimiento de contrapartida se contabilizará el día siguiente.
* Si el campo contiene una fórmula de fecha (por ejemplo, **5D**, o sea cinco días), el movimiento de contrapartida se contabilizará con una fecha de registro calculada utilizando el cálculo de la fecha de reversión.

> [!NOTE]
> De manera predeterminada, el campo **Cálculo de la fecha de reversión** no está disponible en la página **Diarios generales periódicos** página. Para usar el campo, debe agregarlo personalizando la página. Para obtener más información, consulte [Personalizar el área de trabajo](ui-personalization-user.md).

## Trabajar con diarios estándar

Cuando haya creado líneas de diario que probablemente vaya a volver a crear más adelante, puede guardarlas como un diario estándar antes de registrar el diario. Lo mismo se aplica a los diarios de productos y a los diarios generales.

> [!NOTE]
> Es posible que los diarios estándar no contengan todos los campos que desea incluir en los movimientos contables resultantes. Por ejemplo, si usa un diario general estándar para registrar un pago, los movimientos no contendrán el campo Cód. forma pago.

> [!NOTE]  
> Los siguientes procedimientos se refieren al diario de productos, pero la información también se aplica al diario general.

### Para guardar un diario estándar

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Diarios de productos**, y luego elija el enlace relacionado.
2. Escriba una o varias líneas de diario.
3. Selecciones las líneas del diario que desea reutilizar.
4. Seleccione la acción **Guardar como diario estándar**.
5. En la página **Guardar como Diario productos estándar** defina un diario de productos estándar nuevo o ya existente en el que se deben guardar las líneas:

    Si ya ha creado uno o más diarios de productos estándar y desea reemplazar uno de ellos con el nuevo conjunto de líneas de diario, en el campo **Código**, seleccione el diario de artículo.
6. Elija el botón **Aceptar** para confirmar que desea sustituir el contenido del diario de productos estándar existente.
7. Para guardar estos valores en el campo **Precio unitario** del diario de productos estándar, elija el campo **Guardar precio unitario**.
8. Para guardar los valores en el campo **Cantidad**, elija el campo **Guardar cantidad**.
9. Elija **Aceptar** para guardar el diario de productos estándar.

Cuando guarda el diario de artículos estándar, se muestra la página Diario de artículos para que pueda registrarlo.

### Para reutilizar un diario estándar

> [!NOTE]
> Los diarios estándar no siempre tienen los mismos campos que los diarios generales. Cuando utiliza la acción Obtener diarios estándar para copiar los campos en el diario general, es posible que el diario general tenga menos información que si lo creara manualmente. 

1. Elija el icono ![Bombilla que abre la característica Dígame](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Diarios de productos**, y luego elija el enlace relacionado.
2. Seleccione la acción **Obtener diarios estándar**.
3. Para revisar el diario de productos estándar antes de volver a utilizarlo, elija la acción **Mostrar diario**.

    Los cambios que realice en un diario de productos estándar se implementan directamente, también estarán disponibles la siguiente vez que abra o vuelva a utilizar el diario de productos estándar. Debe estar seguro de que el cambio es lo bastante importante para aplicarlo de forma general. Si no es así, efectúe el cambio concreto en el diario de productos después de haber agregado las líneas del diario de productos estándar. Consulte el paso 4.
4. En la página **Diarios de productos estándar**, seleccione el diario de productos estándar a utilizar y, a continuación, elija **Aceptar**.

    El diario de artículos contiene las líneas que guardó. Si el diario de artículos ya tiene líneas, las nuevas líneas aparecen después de ellas.

    Si no ha activado la opción **Guardar precio unitario** al guardar el diario, el campo **Precio unitario** en las líneas añadidas desde el diario estándar contiene el valor del campo **Coste unitario** en la ficha del producto.

    > [!NOTE]  
    > Si activó las opciones **Guardar precio unitario** o **Guardar cantidad** al guardar el diario, ahora debe asegurarse de que los nuevos valores sean correctos antes de registrar el diario de producto.
    >
    > Si las líneas de diario de productos insertadas contienen precios unitarios guardados que no desea registrar, puede ajustarlos al valor actual del producto.

5. Seleccione las líneas del diario de productos que desea ajustar y, a continuación, elija la acción **Volver a calcular precio unitario**. Esta acción actualizará el campo Precio unitario con el coste unitario actual del producto.
6. Seleccione la acción **Registrar**.

## Para renumerar números de documento en diarios

Para evitar recibir errores de registro debido al número de documento, puede utilizar la acción **Renumerar los números de documento** antes de registrar un diario.

En todos los diarios que se basan en el diario general, el campo **Nº documento** es modificable para que pueda especificar distintos números de documento para distintas líneas de diario o el mismo número de documento para líneas de diario diferentes.

Si el campo **Nº series** de la sección de diario está rellenado, la función de registro en los diarios generales requiere que el número de documento en las líneas de diario individuales o agrupadas estén en orden secuencial. Basta con elegir la opción **Renumerar los números de documento** y los campos relevantes de **N.º documento** se actualizarán posteriormente. Si las líneas de diario relacionadas se agruparon por número de documento antes de utilizar la función, permanecerán agrupadas pero es posible que se asignen a un número de documento diferente.  

Esta función también funciona en las vistas filtradas.

Cualquier nueva numeración de los números de documento respetará las aplicaciones relacionadas, como una solicitud de pago realizada desde el documento en la línea del diario a una cuenta de proveedor. Por consiguiente, los campos **Liq. por id.** y **Liq. por nº documento** se actualizarán en las entradas contables.

### Para renumerar los documentos en diarios

El procedimiento siguiente se basa en la página **Diario general**, pero se aplica a todos los demás diarios que se basan en el diario general, como la ventana **Diario de pagos**.

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Diarios generales**, y luego elija el enlace relacionado.
2. Cuando esté listo para registrar el diario, elija la acción **Renumerar los números de documento**.

Cuando sea necesario, los valores del campo **Nº documento** se cambian para que el número de documento en las líneas de diario individuales o agrupadas estén en orden secuencial. Después de que se vuelven a numerar documentos, podrá registrar el diario.

## Consultar la [formación de Microsoft](/training/paths/use-journals-dynamics-365-business-central/) relacionada

## Consulte también

[Registrar transacciones directamente en la contabilidad](finance-how-post-transactions-directly.md)  
[Revertir los registros de diario y deshacer los recibos/envíos](finance-how-reverse-journal-posting.md)  
[Asignar costes e ingresos](year-allocate-costs-income.md)  
[Finanzas](finance.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Cerrar los movimientos de producto abiertos que se crean por una liquidación fija en el diario de productos](finance-how-to-close-open-item-ledger-entries-resulting-from-fixed-application-in-the-item-journal.md)  
[Revalorizar inventario en el diario de revalorización](inventory-how-revalue-inventory.md)  
[Recuento, ajuste y reclasificación de inventario con diarios](inventory-how-count-adjust-reclassify.md)  
[Concilie los pagos de clientes con el diario de recibos de efectivo o de los movimientos de cliente.](receivables-how-apply-sales-transactions-manually.md)  
[Conciliar pagos a proveedores con el diario de pagos o desde los movimientos de proveedor](payables-how-apply-purchase-transactions-manually.md)  
[Usar documentos y diarios de empresas vinculadas](intercompany-how-work-documents-journals.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
