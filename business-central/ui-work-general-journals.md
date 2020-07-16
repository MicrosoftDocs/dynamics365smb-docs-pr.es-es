---
title: Usar diarios generales para registrar directamente en C/G | Documentos de Microsoft
description: Obtenga información sobre el uso de diarios para registrar transacciones financieras en cuentas generales y otras cuentas, como cuentas bancarias y de proveedor.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 06/10/2020
ms.author: sgroespe
ms.openlocfilehash: 37a69940d6b449a779a6bf8fb9d9729c99aa9ea4
ms.sourcegitcommit: 0b5f8f68b1c9526288bfcce1a3bdc988d2910040
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 06/15/2020
ms.locfileid: "3454436"
---
# <a name="working-with-general-journals"></a>Trabajar con diarios generales

La mayoría de las transacciones financieras se registran en la contabilidad a través de documentos empresariales dedicados, como facturas de compra y pedidos de ventas. Pero también puede procesar actividades comerciales como comprar, pagar o reembolsar los gastos de los empleados publicando líneas de diario en los diferentes diarios en [!INCLUDE[d365fin](includes/d365fin_md.md)].  

La mayoría de los diarios se basan en el *Diario general* y puede procesar todas las transacciones en la página **Diario general**. Para obtener más información, consulte [Registrar transacciones directamente en la contabilidad](finance-how-post-transactions-directly.md).  

Por ejemplo, puede utilizar los gastos de los empleados registrados de propio dinero de gastos relacionados con el mercado, para su reembolso posterior. Para obtener más información, consulte [Registro y reembolso de los costes de los empleados](finance-how-record-reimburse-employee-expenses.md).

Pero en muchos casos, deseará utilizar los diarios que están optimizados para tipos específicos de transacciones, como el **Diario de pagos** para registrar pagos. Para obtener más información, vea [Registrar pagos y reembolsos en el diario de pagos](payables-how-post-payments-refunds.md).  

Puede usar diarios generales para registrar transacciones financieras directamente en cuentas generales y otras cuentas, como cuentas bancarias, de cliente, proveedor y empleado. Registrar con un diario general siempre crea movimientos en cuentas contables. Esto es así incluso si, por ejemplo, una línea del diario se registra en una cuenta de cliente, pues un movimiento se registra en una cuenta de cobros de contabilidad a través de un grupo de registro.

La información que introduzca en un diario es temporal y se puede modificar mientras se encuentre en el diario. Al registrar el diario, la información se transfiere a movimientos en cuentas individuales, donde no se puede modificar. Sin embargo, puede desliquidar los movimientos registrados y puede registrar movimientos de inversión o correctores. Para obtener más información, vea [Revertir los registros de diario y deshacer los recibos/envíos](finance-how-reverse-journal-posting.md).

> [!NOTE]
> [!INCLUDE[journal-showhide-columns-inline-tip](includes/journal-showhide-columns-inline-tip.md)]  

## <a name="using-journal-templates-and-batches"></a>Usar plantillas y secciones de diario

Existen varias plantillas de diario general. Cada plantilla de diario se representa mediante una página específica con funciones particulares y los campos que se requieren para admitir estas funciones, como la página **Diario de conciliación de pagos** para procesar pagos bancarios y la página **Diario de pagos** para pagar a sus proveedores o reembolsar a sus empleados. Para obtener más información, vea [Realizar pagos](payables-make-payments.md) y [Conciliar los pagos de clientes con el diario de recibos de efectivo o de los movimientos de cliente](receivables-how-apply-sales-transactions-manually.md).

Para cada plantilla de diario, puede configurar su propio diario personal como una sección de diario. Por ejemplo, puede definir su propia sección de diario del diario de pagos que tiene su diseño y configuración personal. La sugerencia siguiente es un ejemplo de cómo personalizar un diario.

> [!TIP]  
> Si marca la casilla **Proponer importe de compensación** en la línea de su sección en la página **Secciones diario general**, a continuación, el campo **Importe**, por ejemplo, las líneas de diario general del mismo número de documento se rellena automáticamente con el valor necesario para incluir el saldo del documento. Para obtener más información, consulte [Permitir que [!INCLUDE[d365fin](includes/d365fin_md.md)] proponga valores](ui-let-system-suggest-values.md).

> [!TIP]
> Para agregar o eliminar campos en revistas, use en el banner **Personalizando**. Para obtener más información, consulte [Personalizar el área de trabajo](ui-personalization-user.md).

## <a name="understanding-main-accounts-and-balancing-accounts"></a>Descripción de las cuentas principales y las cuentas de contrapartida
Si ha configurado cuentas de contrapartida predeterminadas para las secciones del diario en la página **Diarios generales**, la cuenta de contrapartida se rellenará automáticamente cuando rellene el campo **Nº cuenta**. En caso contrario, deberá rellenar manualmente tanto el campo **Nº cuenta** como el campo **Cta. contrapartida**. Un importe positivo en el campo **Importe** se adeuda en la cuenta principal y se carga en la cuenta de contrapartida. Un importe negativo se carga en la cuenta principal y se adeuda en la cuenta de contrapartida.

> [!NOTE]  
>   El IVA se calcula de manera independiente para la cuenta principal y la cuenta de contrapartida, para que puedan utilizar diferentes tipos porcentuales de IVA.

## <a name="working-with-recurring-journals"></a>Trabajar con diarios periódicos
Un diario periódico es un diario general con campos específicos para administrar las transacciones que registre frecuentemente con pocos cambios o con ninguno, como el alquiler, las suscripciones, la electricidad y la calefacción. Al usar estos campos para las transacciones periódicas, puede registrar importes tanto fijos como variables. También puede especificar movimientos de reversión automática para el día posterior a la fecha de registro. También puede usar claves de asignación para dividir los movimientos recurrentes entre varias cuentas. Para obtener más información, consulte [Asignación de importes de diario recurrentes a varias cuentas](ui-work-general-journals.md#allocating-recurring-journal-amounts-to-several-accounts).

En un diario periódico, los movimientos que se van a registrar con regularidad sólo hay que escribirlos una vez. Por tanto, las cuentas, las dimensiones, los valores de dimensiones, etc. que se introduzcan permanecerán en el diario después del registro. Si hay que hacer algún cambio, puede realizarlo en cada registro.

### <a name="recurring-method-field"></a>Campo Periodicidad
Este campo determina la forma en que se tratará el importe en la línea de diario una vez realizado el registro. Por ejemplo, si usa el mismo importe cada vez que se registra la línea, puede permitir que el valor se mantenga. Si usa las mismas cuentas y texto de la línea, pero el importe varía en cada una, puede optar por borrar el importe después de cada registro.

| Para | Vea |
| --- | --- |
|Fijo|El importe de la línea del diario permanecerá una vez realizado el registro.|
|Variable|El importe de la línea del diario se borrará una vez realizado el registro.|
|Saldo|El importe registrado en la cuenta de la línea se distribuirá entre las cuentas especificadas para la línea de la tabla Diario gen. distribución. El saldo de la cuenta se establecerá por lo tanto a cero. No olvide rellenar el campo **% Distribución** en la página **Asignaciones**. Para obtener más información, consulte [Asignación de importes de diario recurrentes a varias cuentas](ui-work-general-journals.md#allocating-recurring-journal-amounts-to-several-accounts).|
|Contraasiento fijo|El importe de la línea del diario se mantendrá después del registro y se registrará un movimiento de contrapartida al día siguiente.|
|Contraasiento variable|El importe de la línea del diario se borrará después del registro y se registrará un movimiento de contrapartida al día siguiente.|
|Contraasiento saldo|El importe registrado en la cuenta de la línea se distribuirá entre las cuentas especificadas para la línea de la página **Asignaciones**. El saldo en la cuenta se establecerá en cero y se contabilizará un movimiento de saldo el día siguiente.|

> [!NOTE]  
>  Los campos de IVA se pueden rellenar en la línea del diario periódico o en la línea del diario de distribución, pero no en ambas. Es decir, sólo se pueden rellenar en la página **Asignaciones** si no se han rellenado las líneas correspondientes en el diario periódico.

### <a name="recurring-frequency-field"></a>Campo Frecuencia repetición
Este campo determina la frecuencia con que se va a registrar el movimiento de la línea del diario. Es un campo de fórmula de fecha y debe rellenarse para líneas periódicas. Para obtener más información, vea [Uso de fórmulas de fecha](ui-enter-date-ranges.md#using-date-formulas).

#### <a name="examples"></a>Ejemplos
Si la línea de diario debe registrarse cada mes, escriba "1M". Después de cada registro, la fecha del campo **Fecha registro** se actualizará con la fecha del mes siguiente.

Si desea registrar un movimiento el último día de cada mes, opte por una de estas posibilidades:

- Registre el primer movimiento el último día del mes y escriba la fórmula 1D+1M-1D (1 día + 1 mes - 1 día). Con esta fórmula, se calcula correctamente la fecha de registro con independencia de los días que tenga el mes.

- Registre el primer movimiento cualquier día del mes e introduzca la fórmula 1M+CM. Con esta fórmula, la fecha de registro será después de un mes completo + los días que faltan del mes actual.

### <a name="expiration-date-field"></a>Campo fecha caducidad
Este campo determina la fecha en que se registrará la línea por última vez. La línea no se registrará después de esta fecha.

La ventaja de utilizar el campo es que la línea no se eliminará inmediatamente del diario y siempre es posible sustituir la fecha de finalización presente con una posterior de manera que pueda utilizar la línea más adelante.

Si el campo se deja en blanco, la línea se registrará cada vez que se registre hasta que se elimine del diario.

### <a name="allocating-recurring-journal-amounts-to-several-accounts"></a>Asignación de importes de diario recurrentes a varias cuentas
En la página **Diario general periódico**, puede elegir la acción **Asignaciones** para ver o administrar cómo los importes de la línea del diario periódico se asignan a varias cuentas y dimensiones. Tenga en cuenta que una asignación funciona como línea de cuenta de contrapartida a la del diario periódico.

Como en el caso del diario periódico, sólo necesita introducir una vez la distribución. Una vez realizado el registro, la distribución permanecerá sin cambios en el diario de distribución, de modo que no necesitará introducir importes y distribuciones cada vez que registre la línea del diario periódico.

Si el método periódico en el diario periódico está establecido en **Saldo** o en **Contraasiento saldo**, no se tendrá en cuenta ningún código de valor de dimensión global en el diario periódico cuando la cuenta esté establecida en cero. Por lo tanto, si asigna una línea periódica a varios valores de dimensión en la página **Asignaciones**, solo se creará una entrada reversible. Por tanto, si asigna una línea del diario periódico que contenga un código de valor de dimensión, no introduzca el mismo código en la página **Asignaciones**. De lo contrario, los valores de dimensión serán incorrectas.

#### <a name="example-allocating-rent-payments-to-different-departments"></a>Ejemplo: Asignación de pagos de alquiler a diferentes departamentos
si usted paga un alquiler cada mes, tendrá que introducir el importe del alquiler en la cuenta de caja en una línea del diario periódico. En la página **Asignaciones** puede dividir el gasto entre varios departamentos (dimensión Departamento) de acuerdo con el número de metros cuadrados que ocupa cada uno. El cálculo se basa en el porcentaje de asignación en cada línea. Puede ingresar varias cuentas en diferentes líneas de asignación (si el alquiler se va a dividir entre varias cuentas), o puede ingresar la misma cuenta pero con varios códigos de valor de dimensión para la dimensión Departamento en cada línea.

## <a name="working-with-standard-journals"></a>Trabajar con diarios estándar
Cuando haya creado líneas de diario que probablemente vaya a volver a crear más adelante, puede guardarlas como un diario estándar antes de registrar el diario. Esta funcionalidad se aplica a los diarios de productos y a los diarios generales.

> [!NOTE]  
>   El siguiente procedimiento se refiere al diario de productos, pero la información también se aplica al diario general.

### <a name="to-save-a-standard-journal"></a>Para guardar un diario estándar
1. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Diarios de productos** y luego elija el enlace relacionado.
2. Escriba una o varias líneas de diario.
3. Selecciones las líneas del diario que desea reutilizar.
4. Seleccione la acción **Guardar como diario estándar**.
5. En la página **Guardar como Diario productos estándar** defina un diario de productos estándar nuevo o ya existente en el que se deben guardar las líneas:

    Si ya ha creado uno o más diarios de productos estándar y desea reemplazar uno de ellos con el nuevo conjunto de líneas de diario, en el campo Código, seleccione el código que desee usar.
6. Elija el botón **Aceptar** para confirmar que desea sobrescribir el diario de productos estándar existente y reemplazar todo el contenido.
7. Seleccione el campo **Guardar precio unitario** si desea guardar los valores del campo **Precio unitario** del diario de productos estándar.
8. Seleccione el campo de **Guardar cantidad** si desea que la aplicación guarde los valores contenidos en el campo **Cantidad**.
9. Elija el botón **Aceptar** para guardar el diario de productos estándar.

Cuando haya terminado de guardar el diario de productos estándar, se muestra la página Diario productos para que pueda registrarlo, sabiendo que puede volver a crearlo fácilmente la siguiente vez que deba registrar líneas iguales o parecidas.

### <a name="to-reuse-a-standard-journal"></a>Para reutilizar un diario estándar
1. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Diarios de productos** y luego elija el enlace relacionado.
2. Seleccione la acción **Obtener diarios estándar**.

    Se abre la página Diarios productos estándar donde se muestran los códigos y las descripciones de todos los diarios de productos estándar.
3. Para revisar el diario de productos estándar antes de volver a utilizarlo, elija la acción **Mostrar diario**.

    Los cambios que realiza en un diario de productos estándar se implementan enseguida. Estarán disponibles la próxima vez que abra o vuelva a utilizar el diario de productos estándar en cuestión. Por tanto, debe estar seguro de que el cambio es lo bastante importante para aplicarlo de forma general. Si no es así, efectúe el cambio concreto en el diario de productos después de haber insertado las líneas del diario de productos estándar. Vea el paso 4 siguiente.
4. En la página **Diarios de productos estándar**, seleccione el diario de productos estándar que desea volver a utilizar y, a continuación, elija el botón **Aceptar**.

    Ahora el diario de productos incluye las líneas guardadas como diario de productos estándar. Si ya existían las líneas del diario en el diario de productos, las líneas insertadas se colocarán debajo de las líneas de diario existentes.

    Si no marcó el campo **Guardar precio unitario** cuando utilizó el trabajo de función **Guardar como Diario productos estándar**, el campo **Precio unitario** de las líneas que se insertan del diario estándar se rellena automáticamente con el valor actual del producto, copiado del campo **Coste unitario** de la ficha de producto.

    > [!NOTE]  
    >   Si seleccionó el campo **Guardar precio unitario** o **Guardar cantidad**, ahora debe asegurarse de que los valores insertados sean correctos para este ajuste de inventario concreto antes de registrar el diario de producto.

    Si las líneas de diario de productos insertadas contienen precios unitarios guardados que no desea registrar, puede ajustarlos rápidamente al valor actual del producto del siguiente modo.

6. Seleccione las líneas del diario de productos que desea ajustar y, a continuación, elija la acción **Volver a calcular precio unitario**. Así se actualizará el campo Precio unitario con el coste unitario actual del producto.
7. Seleccione la acción **Registrar**.

## <a name="to-renumber-document-numbers-in-journals"></a>Para renumerar números de documento en diarios
Para asegurarse de no recibir errores de registro debido al orden de número de documento, puede utilizar la función **Renumerar los números de documento** antes de registrar un diario.

En todos los diarios que se basan en el diario general, el campo **Nº documento** es modificable para que pueda especificar distintos números de documento para distintas líneas de diario o el mismo número de documento para líneas de diario diferentes.

Si el campo **Nº series** de la sección de diario está rellenado, la función de registro en los diarios generales requiere que el número de documento en las líneas de diario individuales o agrupadas estén en orden secuencial. Para asegurarse de no recibir errores de registro debido al orden de número de documento, puede utilizar la función **Renumerar los números de documento** antes de registrar el diario. Si las líneas de diario relacionadas se agruparon por número de documento antes de utilizar la función, permanecerán agrupadas pero es posible que se asignen a un número de documento diferente.

Esta función también funciona en las vistas filtradas.

Cualquier nueva numeración de los números de documento respetará las aplicaciones relacionadas, como una solicitud de pago se ha realizado desde el documento en la línea del diario a una cuenta de proveedor. Por consiguiente, los campos **Liq. por id.** y **Liq. por nº documento** para los movimientos de contabilidad asignados pueden ser actualizados.

El procedimiento siguiente se basa en la página **Diario general**, pero se aplica a todos los demás diarios que se basan en el diario general, como la ventana **Diario de pagos**.

1. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), introduzca **Diarios generales** y luego elija el enlace relacionado.
2. Cuando esté listo para registrar el diario, elija la acción **Renumerar los números de documento**.

Cuando sea necesario, los valores del campo **Nº documento** se cambian para que el número de documento en las líneas de diario individuales o agrupadas estén en orden secuencial. Después de que se vuelven a numerar documentos, podrá registrar el diario.

## <a name="see-related-training-at-microsoft-learn"></a>Consulte Formación relacionada en [Microsoft Learn](/learn/paths/use-journals-dynamics-365-business-central/)

## <a name="see-also"></a>Consulte también

[Registrar transacciones directamente en la contabilidad](finance-how-post-transactions-directly.md)  
[Revertir los registros de diario y deshacer los recibos/envíos](finance-how-reverse-journal-posting.md)  
[Asignar costes e ingresos](year-allocate-costs-income.md)  
[Finanzas](finance.md)  
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Cerrar los movimientos de producto abiertos que se crean por una liquidación fija en el diario de productos](finance-how-to-close-open-item-ledger-entries-resulting-from-fixed-application-in-the-item-journal.md)  
[Revalorizar inventario en el diario de revalorización](inventory-how-revalue-inventory.md)  
[Recuento, ajuste y reclasificación de inventario con diarios](inventory-how-count-adjust-reclassify.md)  
[Concilie los pagos de clientes con el diario de recibos de efectivo o de los movimientos de cliente.](receivables-how-apply-sales-transactions-manually.md)  
[Conciliar pagos a proveedores con el diario de pagos o desde los movimientos de proveedor](payables-how-apply-purchase-transactions-manually.md)  
[Usar documentos y diarios de empresas vinculadas](intercompany-how-work-documents-journals.md)  
