---
title: Liquidar pagos para los documentos de venta no pagados | Documentos de Microsoft
description: Los importes pagados por clientes se liquidan en los documentos de venta relacionados y se registra el pago para actualizar los movimientos de cliente, contabilidad y banco.
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: payment process, cash receipts, customer payment
ms.date: 09/08/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: aa2accb5b03fd55c96b046ca6b61582ed5b8a142
ms.contentlocale: es-es
ms.lasthandoff: 03/22/2018

---
# <a name="reconcile-customer-payments-manually-from-a-list-of-unpaid-sales-documents"></a>Conciliar pagos manualmente de una lista de documentos de venta sin abonar
Cuando sus clientes han realizado pagos a su cuenta de banco electrónico, debe liquidar cada importe pagado al documento de venta relacionado y después registrar el pago para actualizar los movimientos de cliente, contabilidad y banco.

> [!NOTE]  
>   Puede realizar las mismas tareas, incluidos los pagos de proveedor, en la ventana **Diario de conciliación de pagos** usando las funciones para la importación automática de extractos bancarios y la conciliación de cuentas bancarias. Para obtener más información, vea [Conciliar pagos con liquidación automática](receivables-how-reconcile-payments-auto-application.md).

La ventana **Registro de pago** se ha diseñado para ayudarle en las tareas relacionadas con cuentas de contrapartida internas mediante el uso de cifras de efectivo reales para garantizar que los pagos se cobran por parte de los clientes de manera eficaz. Esta herramienta de procesamiento de pagos le permite verificar y registrar rápidamente los pagos concretos o totales, procesar pagos al descuento y buscar documentos no pagados específicos para los que se realiza el pago.

Los pagos para los diferentes clientes que tienen distintas fechas de pago se deben registrar como pagos individuales. Los pagos para el mismo cliente con la misma fecha de pago se pueden registrar como pago total. Esto puede ser útil, por ejemplo, cuando un cliente ha realizado un pago único que cubre varias facturas de venta.

## <a name="to-set-up-the-payment-registration-journal"></a>Configurar el diario de registros de pago
Dado que puede registrar distintos tipos de pago en diferentes cuentas de saldo, debe seleccionar una cuenta de saldo en la ventana **Configuración de registro de pago** antes de empezar a procesar los pagos de cliente. Si siempre registra en la misma cuenta de saldo, puede definir esa cuenta como la predeterminada y evitar este paso cada vez que abra la ventana **Registro de pago**.  

1. Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Configuración de registro de pago** y, a continuación, seleccione el vínculo relacionado.

    Alternativamente, en la venta **Registro de pago**, seleccione la acción **Configurar**.    
2. Rellene los campos de la ventana **Configuración del registro de pago**. Seleccione un campo para obtener una breve descripción del campo o el enlace a la información relacionada.  

## <a name="to-reconcile-payments-individually"></a>Conciliar pagos individualmente
1. Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Registro de pago** y, a continuación, seleccione el vínculo relacionado.  
2. Seleccione la casilla **Pago realizado** en la línea que representa el documento registrado para el que se ha realizado un pago.

    Si se selecciona la casilla de verificación **Rellenar fecha de recepción automáticamente** de la ventana **Configuración de registro de pago**, la fecha de trabajo se tendrá que introducir en el campo **Fecha de recepción**.  
3. En el campo **Fecha recepción**, especifique la fecha en la que se realizó el pago. Esta fecha puede ser distinta de la fecha de trabajo.  
4. En el campo **Importe recibido**, especifique el importe que se ha pagado.

    Para los pagos completos, este es el mismo que el importe en el campo **Importe pendiente** en la línea. Para los pagos parciales, este inferior que el importe en el campo **Importe pendiente** en la línea.    
5. Repita los pasos 2 a 4 para las demás líneas que representen documentos registrados para los que se realicen pagos.  
6. Seleccione la acción **Registrar pagos**.  

La información de pagos se registra para los documentos representados por las líneas donde la casilla **Pago realizado** está seleccionada.  

Los movimientos de pago se registran en la cuenta contable, la cuenta de banco y las cuentas de cliente. Cada pago se aplica al documento de venta registrado relacionado.  

## <a name="to-reconcile-lump-payments"></a>Conciliar los pagos totales
1. Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Registro de pago** y, a continuación, seleccione el vínculo relacionado.
2. Seleccione la casilla **Pago realizado** en las líneas que representan documentos registrados para el mismo cliente para el que se ha realizado un pago total.  

    > [!NOTE]  
>   El cliente en el campo **Nombre** debe ser igual en todas las líneas que se registrarán como pago total.  

    Si se selecciona la casilla de verificación **Rellenar fecha de recepción automáticamente** de la ventana **Configuración de registro de pago**, la fecha de trabajo se tendrá que introducir en el campo **Fecha de recepción**.  
3. En el campo **Fecha recepción**, especifique la fecha en la que se realizó el pago. Esta fecha puede ser distinta de la fecha de trabajo.  

    > [!NOTE]  
>   Esta fecha debe ser igual en todas las líneas que se registrarán como pago total.  
4. En el campo **Importe recibido**, especifique los importes en varias líneas que suman el importe del pago total.  

    > [!TIP]  
>   Intente registrar el mayor número posible de pagos completos con el importe total. Introduzca los importes cuya cantidad coincida con el importe en el campo **Importe pendiente** en tantas líneas como sea posible.  
5. Repita los pasos 2 a 4 para las demás líneas que representen documentos registrados para el mismo cliente para los que se ha realizado un pago total.  
6. Seleccione la acción **Registrar como pago total**. La información de pagos introducida se registra para los documentos representados por las líneas donde la casilla **Pago realizado** está seleccionada.  

Los movimientos de pago se registran en la cuenta contable, la cuenta de banco y las cuentas de cliente. Cada pago se aplica al documento de venta registrado relacionado.  

Si un pago en el banco no se representa mediante la línea en la ventana **Registro de pago**, puede ser porque el documento relacionado aún no se ha registrado. En ese caso, puede usar una función de búsqueda para buscar rápidamente el documento y registrarlo para procesar el pago. Para obtener más información, vea la sección “Buscar un documento determinado de ventas que no esté totalmente facturado”.  

Si un pago en el banco no se representa mediante ningún documento en [!INCLUDE[d365fin](includes/d365fin_md.md)], puede abrir un diario general previamente rellenado en la ventana **Registro de pago** para registrar el pago directamente en la cuenta de saldo sin liquidar el pago a un documento. Alternativamente, puede que desee registrar el pago en el diario hasta que el origen del pago se haya resuelto. Para obtener más información, consulte la sección "Registrar pagos sin documento relacionado".  

## <a name="to-process-customer-payments-with-discounts-manually"></a>Para procesar pagos de cliente con descuentos manualmente
Si ha acordado un descuento por pronto pago con el cliente, los importes de pago pueden ser inferiores a los importes de factura si el pago se produce antes de la fecha de descuento acordada.  

En los procedimientos siguientes se explican cuatro formas distintas para registrar pagos al descuento en la ventana **Registro de pago**.  

* El importe de pago es igual al importe al descuento restante, y la fecha de pago es antes de la fecha de descuento. Registra el pago tal como está.  
* El importe de pago es igual al importe al descuento restante, pero la fecha de pago es posterior a la fecha de descuento. Registra el pago como parcial. El documento permanece abierto para recopilar o pagar el importe pendiente. Alternativamente, puede definir la fecha de descuento posteriormente para permitir el pago total.  
* El importe del pago es menor que el importe al descuento restante. Registra el pago como parcial. El documento permanece abierto para recopilar o pagar el importe pendiente.  
* El importe del pago es mayor que el importe al descuento restante. Registra los pagos tal como están. Solo se registra el importe pendiente. El importe adicional se acredita al cliente.  

### <a name="to-process-a-payment-amount-that-is-equal-to-the-discounted-amount-and-where-the-payment-date-is-before-the-discount-date"></a>Importar un importe de pago igual al descuento y donde la fecha de pago es antes de la fecha de descuento
1. Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Registro de pago** y, a continuación, seleccione el vínculo relacionado.  
2. Introduzca el importe de pago en el campo **Importe recibido**. El importe es igual al importe en el campo **Importe restante tras descuento**.

    La casilla **Pago realizado** se selecciona automáticamente y el campo **Fecha de recepción** se rellena con la fecha de trabajo.    
3. Introduzca la fecha de pago en el campo **Fecha de recepción**. La fecha es anterior a la fecha del campo **Fecha de descuento del pago**.
4. Compruebe que el campo **Importe pendiente** contenga cero (0).  
5. Seleccione la acción **Registrar pagos** para registrar el pago completo a la cuenta contable, la cuenta de banco y la cuenta de cliente.

### <a name="to-process-a-payment-amount-that-is-equal-to-the-discounted-amount-but-where-the-payment-date-is-after-the-discount-date"></a>Importar un importe de pago igual al descuento ero donde la fecha de pago es posterior a la fecha de descuento
1. Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Registro de pago** y, a continuación, seleccione el vínculo relacionado.  
2. Introduzca el importe de pago en el campo **Importe recibido**. El importe es igual al importe en el campo **Importe restante tras descuento**.

    La casilla **Pago realizado** se selecciona automáticamente y el campo **Fecha de recepción** se rellena con la fecha de trabajo.
3. En el campo **Fecha de recepción**, especifique una fecha de pago que sea posterior a la fecha del campo **Fecha de descuento del pago**. Los campos de fecha cambian a la fuente color rojo, y un mensaje de error se muestra en la parte inferior de la ventana.

    > [!TIP]  
>   Si desea crear una excepción y conceder el descuento aunque el pago haya vencido, realice los pasos siguientes:
4. Seleccione la acción **Detalles**.  
5. En la ventana **Detalles del registro de pago**, en el campo **Fecha de descuento del pago**, en la ficha desplegable **Descuento del pago**, especifique una fecha que sea posterior a la fecha del campo **Fecha de recepción**, en la ventana **Registro de pago**.  

    El mensaje de error y la fuente color rojo desaparecen, y puede empezar a procesar el pago al descuento.    
6. Compruebe que el campo **Importe pendiente** contenga el importe pendiente para pagar el importe total de la factura.  
7. Seleccione la acción **Registrar pagos** para registrar el pago parcial en la cuenta contable, la cuenta de banco y la cuenta de cliente.  

El documento relacionado quedará abierto.

### <a name="to-process-a-payment-that-is-lower-than-the-remaining-discounted-amount"></a>Procesar un pago que es menor que el importe al descuento restante
1. Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Registro de pago** y, a continuación, seleccione el vínculo relacionado.  
2. Introduzca el importe de pago en el campo **Importe recibido**. El importe es inferior al importe del campo **Importe restante tras descuento**.

    La casilla **Pago realizado** se selecciona automáticamente y el campo **Fecha de recepción** se rellena con la fecha de trabajo.  
3. Introduzca la fecha de pago en el campo **Fecha de recepción**. La fecha es anterior a la fecha del campo **Fecha de descuento del pago**.
4. Compruebe que el campo **Importe pendiente** contiene el importe pendiente para pagar el importe al descuento.  
5. Seleccione la acción **Registrar pagos** para registrar el pago parcial en la cuenta contable, la cuenta de banco y la cuenta de cliente.  

El documento relacionado quedará abierto.

### <a name="to-process-a-payment-that-is-more-than-the-remaining-discounted-amount"></a>Procesar un pago que es mayor que el importe al descuento restante
1. Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Registro de pago** y, a continuación, seleccione el vínculo relacionado.  
2. Introduzca el importe de pago en el campo **Importe recibido**. El importe es superior al importe del campo **Importe restante tras descuento**.  

    La casilla **Pago realizado** se selecciona automáticamente y el campo **Fecha de recepción** se rellena con la fecha de trabajo.    
3. Introduzca la fecha de pago en el campo **Fecha de recepción**. La fecha es anterior a la fecha del campo **Fecha de descuento del pago**.
4. Compruebe que el campo **Importe pendiente** contenga cero (0).  
5. Seleccione la acción **Registrar pagos** para registrar el pago completo a la cuenta contable, la cuenta de banco y la cuenta de cliente.  

El documento relacionado está cerrado y al cliente se acredita el importe de pago en exceso.  

## <a name="to-find-a-specific-sales-document-that-is-not-fully-invoiced"></a>Buscar un documento de ventas específico que no está facturado totalmente
La ventana **Registro de pago** le facilita las tareas necesarias para calcular el saldo de las cuentas internas con cifras reales de efectivo para garantizar la colección efectiva de los clientes y el pago debido a los proveedores. Muestra los pagos entrantes pendientes como líneas que representen los documentos de venta donde se debe un importe para el pago.  

Normalmente, cuando un pago se ha realizado, registrado en el banco, etc., el documento de venta o compra relacionado se representa como una línea en la ventana **Registro de pago** porque el documento en cuestión está esperando el registro del pago con el importe pendiente. Sin embargo, a veces un pago que se ha realizado no se representa mediante una línea en la ventana **Registro de pago**, normalmente porque en el documento en cuestión no se registrado la factura totalmente.

En la ventana **Búsqueda de documentos**, podrá buscar entre los documentos que no se han facturado por completo. Puede buscar basado en uno o varios de los siguientes criterios:  

* N.º documento  
* Importe o rango de importes  

En el procedimiento siguiente se explica cómo buscar un documento determinado mediante ambos criterios de búsqueda.  

1. Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Registro de pago** y, a continuación, seleccione el vínculo relacionado.
2. Con el puntero en cualquier línea, seleccione la acción **Buscar documentos**.
3. En la ventana **Búsqueda de documentos**, especifique un valor de búsqueda en el campo **Número de documento**.  

    > [!NOTE]  
>   El valor que especifique en este campo se encierra entre los caracteres comodín ocultos. Esto significa que la función busca todos los números de documento que contengan el valor especificado.    
4. En el campo **Importe**, especifique el importe concreto que existe en el documento que desee buscar.  
5. En el campo **% tolerancia de importe**, especifique un valor de porcentaje para definir el rango de importes que desea buscar para encontrar el documento abierto.  

    Si especifica 10, la función buscará los importes en un rango entre un diez por ciento más bajo y un diez por ciento más alto que el valor del campo **Importe**.    
6. Seleccione la acción **Buscar**.  

La función de búsqueda busca entre los documentos que no se han facturado totalmente según los criterios especificados.  

Si hay documentos que coinciden con los criterios de búsqueda, la ventana **Resultado de la búsqueda de documentos** se abrirá en las líneas de presentación que representan dichos documentos. Cada línea contiene un número de documento, una descripción y un importe para que pueda buscar fácilmente un documento determinado, por ejemplo según la información sobre el extracto de banco.  

Si un pago en el banco no se representa mediante ningún documento en [!INCLUDE[d365fin](includes/d365fin_md.md)], puede abrir un diario general previamente rellenado en la ventana **Registro de pago** para registrar el pago directamente en la cuenta de saldo sin liquidar el pago a un documento. Alternativamente, puede que desee registrar el pago en el diario hasta que el origen del pago se haya resuelto.  

## <a name="to-record-or-post-a-payment-without-a-related-document"></a>Registrar pagos sin documento relacionado
Si un pago en el banco no se representa mediante ningún documento en [!INCLUDE[d365fin](includes/d365fin_md.md)], puede abrir una línea de diario general previamente rellenada en la ventana **Registro de pago** para registrar el pago directamente en la cuenta de saldo sin liquidar el pago a un documento. Alternativamente, puede que desee registrar el pago en el diario hasta que el origen del pago se haya aclarado.  

1. Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Registro de pago** y, a continuación, seleccione el vínculo relacionado.  

Empiece a registrar un pago no documentado.  

1. Seleccione la acción **Diario general**.  

    La ventana **Diario general** se abre con una línea rellenada previamente con la cuenta de saldo de la sección de diario configurada en la ventana **Configuración de registro de pago**.  
2. Rellene los campos restantes de la línea de diario general, como el importe y el número del cliente u otra información del extracto de banco. Para obtener más información, consulte [Registrar transacciones directamente en la contabilidad](finance-how-post-transactions-directly.md).  

Puede registrar la línea del diario para actualizar el total de la cuenta de saldo. Alternativamente, puede dejar la línea del diario sin registrar, y quizás agregarla con una nota que el pago necesita más análisis.  

Si deja la línea del diario sin registrar, agregará al valor del campo **Saldo no registrado** en la parte inferior de la ventana **Registro de pago**.  

## <a name="see-also"></a>Consulte también
[Administrar cobros](receivables-manage-receivables.md)  
[Ventas](sales-manage-sales.md)  
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

