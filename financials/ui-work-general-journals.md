---
title: Usar diarios generales para registrar directamente en C/G | Documentos de Microsoft
description: "Obtenga información sobre el uso de diarios generales para registrar transacciones financieras en cuentas generales y otras cuentas, como cuentas bancarias y de proveedor."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 07/02/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: b573bb55c29de329e5d9a804b49a91687dc369ff
ms.contentlocale: es-es
ms.lasthandoff: 09/22/2017

---
# <a name="working-with-general-journals"></a>Trabajar con diarios generales
La mayoría de las transacciones financieras se registran en la contabilidad a través de documentos empresariales dedicados, como facturas de compra y pedidos de ventas. Para las actividades empresariales que no está representadas por un documento en [!INCLUDE[d365fin](includes/d365fin_md.md)], como los gastos o recibos de efectivo más pequeños, puede crear las transacciones relacionadas registrando líneas de diario en la ventana **Diario general**. Para obtener más información, consulte [Registrar transacciones directamente en la contabilidad](finance-how-post-transactions-directly.md).

Por ejemplo, puede registrar el cargo de los empleados de propio dinero de gastos relacionados con el mercado, para su reembolso posterior. Para obtener más información, vea [Procedimiento: registro y reembolso de los costes de los empleados](finance-how-record-reimburse-employee-expenses.md).

Puede usar diarios generales para registrar transacciones financieras directamente en cuentas generales y otras cuentas, como cuentas bancarias, de cliente, proveedor y empleado. Registrar con un diario general siempre crea movimientos en cuentas contables. Esto es así incluso si, por ejemplo, una línea del diario se registra en una cuenta de cliente, pues un movimiento se registra en una cuenta de cobros de contabilidad a través de un grupo de registro.

La información que introduzca en un diario es temporal y se puede modificar mientras se encuentre en el diario. Al registrar el diario, la información se transfiere a movimientos en cuentas individuales, donde no se puede modificar. Sin embargo, puede desliquidar los movimientos registrados y puede registrar movimientos de inversión o correctores. Para obtener más información, consulte [Procedimiento: revertir registros](finance-how-reverse-journal-posting.md).

## <a name="using-journal-templates-and-batches"></a>Usar plantillas y secciones de diario
Existen varias plantillas de diario general. Cada plantilla de diario se representa mediante una ventana específica con funciones particulares y los campos que se requieren para admitir estas funciones, como la ventana **Diario de conciliación de pagos** para procesar pagos bancarios y la ventana **Diario de pagos** para pagar a sus proveedores o reembolsar a sus empleados. Para obtener más información, consulte [Realizar pagos](payables-make-payments.md) y [Conciliar pagos de cliente manualmente](receivables-how-apply-sales-transactions-manually.md).

Para cada plantilla de diario, puede configurar su propio diario personal como una sección de diario. Por ejemplo, puede definir su propia sección de diario del diario de pagos que tiene su diseño y configuración personal. La sugerencia siguiente es un ejemplo de cómo personalizar un diario.

> [!TIP]  
> Si marca la casilla **Proponer importe de compensación** en la línea de su sección en la ventana **Secciones diario general**, a continuación, el campo **Importe**, por ejemplo, las líneas de diario general del mismo número de documento se rellena automáticamente con el valor necesario para incluir el saldo del documento. Para obtener más información, consulte [Permitir que [!INCLUDE[d365fin](includes/d365fin_md.md)] proponga valores](ui-let-system-suggest-values.md).

## <a name="understanding-main-accounts-and-balancing-accounts"></a>Descripción de las cuentas principales y las cuentas de contrapartida
Si ha configurado cuentas de contrapartida predeterminadas para las secciones del diario en la página **Diarios generales**, la cuenta de contrapartida se rellenará automáticamente cuando rellene el campo **Nº cuenta**. En caso contrario, deberá rellenar manualmente tanto el campo **Nº cuenta** como el campo **Cta. contrapartida**. Un importe positivo en el campo **Importe** se adeuda en la cuenta principal y se carga en la cuenta de contrapartida. Un importe negativo se carga en la cuenta principal y se adeuda en la cuenta de contrapartida.

> [!NOTE]  
>   El IVA se calcula de manera independiente para la cuenta principal y la cuenta de contrapartida, para que puedan utilizar diferentes tipos porcentuales de IVA.

## <a name="working-with-recurring-journals"></a>Trabajar con diarios periódicos
Un diario periódico es un diario general con campos especiales para administrar las transacciones que registre frecuentemente con pocos cambios o con ninguno. Al usar estos campos para las transacciones periódicas, puede registrar importes tanto fijos como variables. También puede especificar la movimientos de reversión automática al día siguiente a la fecha de registro y usar claves de asignación con los movimientos periódicos.

## <a name="working-with-standard-journals"></a>Trabajar con diarios estándar
Cuando haya creado líneas de diario que probablemente vaya a volver a crear más adelante, puede guardarlas como un diario estándar antes de registrar el diario. Esta funcionalidad se aplica a los diarios de productos y a los diarios generales.

> [!NOTE]  
>   El siguiente procedimiento se refiere al diario de productos, pero la información también se aplica al diario general.

### <a name="to-save-a-standard-journal"></a>Para guardar un diario estándar
1. Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Diarios producto** y, a continuación, seleccione el vínculo relacionado.
2. Escriba una o varias líneas de diario.
3. Selecciones las líneas del diario que desea reutilizar.
4. Seleccione la acción **Guardar como diario estándar**.
5. En la ventana **Guardar como Diario productos estándar** defina un diario de productos estándar nuevo o ya existente en el que se deben guardar las líneas:

    Si ya ha creado uno o más diarios de productos estándar y desea reemplazar uno de ellos con el nuevo conjunto de líneas de diario, en el campo Código, seleccione el código que desee usar.
6. Elija el botón **Aceptar** para confirmar que desea sobrescribir el diario de productos estándar existente y reemplazar todo el contenido.
7. Seleccione el campo **Guardar precio unitario** si desea guardar los valores del campo **Precio unitario** del diario de productos estándar.
8. Seleccione el campo de **Guardar cantidad** si desea que el programa guarde los valores contenidos en el campo **Cantidad**.
9. Elija el botón **Aceptar** para guardar el diario de productos estándar.

Cuando haya terminado de guardar el diario de productos estándar, se muestra la ventana Diario productos para que pueda registrarlo, sabiendo que puede volver a crearlo fácilmente la siguiente vez que deba registrar líneas iguales o parecidas.

### <a name="to-reuse-a-standard-journal"></a>Para reutilizar un diario estándar
1. Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Diarios producto** y, a continuación, seleccione el vínculo relacionado.
2. Seleccione la acción **Obtener diarios estándar**.

    Se abre la ventana Diarios productos estándar donde se muestran los códigos y las descripciones de todos los diarios de productos estándar.
3. Para revisar el diario de productos estándar antes de volver a utilizarlo, elija la acción **Mostrar diario**.

    Los cambios que realiza en un diario de productos estándar se implementan enseguida. Estarán disponibles la próxima vez que abra o vuelva a utilizar el diario de productos estándar en cuestión. Por tanto, debe estar seguro de que el cambio es lo bastante importante para aplicarlo de forma general. Si no es así, efectúe el cambio concreto en el diario de productos después de haber insertado las líneas del diario de productos estándar. Vea el paso 4 siguiente.
4. En la ventana **Diarios de productos estándar**, seleccione el diario de productos estándar que desea volver a utilizar y, a continuación, elija el botón **Aceptar**.

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

El procedimiento siguiente se basa en la ventana **Diario general**, pero se aplica a todos los demás diarios que se basan en el diario general, como la ventana **Diario de pagos**.

1. Elija el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), especifique **Diarios generales** y elija el vínculo relacionado.
2. Cuando esté listo para registrar el diario, elija la acción **Renumerar los números de documento**.

Cuando sea necesario, los valores del campo **Nº documento** se cambian para que el número de documento en las líneas de diario individuales o agrupadas estén en orden secuencial. Después de que se vuelven a numerar documentos, podrá registrar el diario.

## <a name="see-also"></a>Consulte también
[Procedimiento: registrar transacciones directamente en la contabilidad](finance-how-post-transactions-directly.md)  
[Procedimiento: Revertir registros](finance-how-reverse-journal-posting.md)  
[Procedimiento: asignar costes e ingresos.](year-allocate-costs-income.md)  
[Finanzas](finance.md)  
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

