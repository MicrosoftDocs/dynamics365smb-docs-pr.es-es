---
title: Liquidar pagos para los documentos de venta no pagados
description: 'Los importes pagados por clientes se liquidan en los documentos de venta relacionados y se registra el pago para actualizar los movimientos de cliente, contabilidad y banco.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'payment process, cash receipts, customer payment'
ms.search.form: '1290, 1294, 1287'
ms.date: 04/01/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# Conciliar pagos de cliente desde una lista de documentos de venta sin abonar

Después de que los clientes realicen pagos electrónicos a su cuenta bancaria, debe realizar las siguientes acciones:

* Aplicar cada importe pagado al documento de venta relacionado.
* Registrar el pago para actualizar los movimientos de cliente, cuenta contable y cuenta bancaria. 

En función de sus necesidades comerciales, puede recibir el pago y registrarlo de diferentes maneras: de forma manual, automática y mediante servicios de pago.  

> [!NOTE]  
> Puede realizar las mismas tareas, incluidos los pagos de proveedor, en la página **Diario de conciliación de pagos** usando las funciones para la importación automática de extractos bancarios y la conciliación de cuentas bancarias. Para obtener más información, vea [Conciliar pagos con liquidación automática](receivables-how-reconcile-payments-auto-application.md).

Utilice las cuentas internas de saldo de la página **Registrar pagos de cliente** usando cifras reales de efectivo para garantizar que se cobren los pagos. Puede verificar y registrar rápidamente pagos individuales o de suma global, procesar pagos con descuento y encontrar los documentos no pagados.

Los pagos para los diferentes clientes que tienen distintas fechas de pago se deben registrar como pagos individuales. Los pagos para el mismo cliente con la misma fecha de pago se pueden registrar como pago de suma total. Los pagos de suma global pueden ser útiles, por ejemplo, cuando un cliente ha realizado un pago único que cubre varias facturas de venta.

## Configurar el diario de registros de pago
Dado que puede registrar distintos tipos de pago en diferentes cuentas de saldo, debe seleccionar una cuenta de saldo en la página **Configuración de registro de pago** antes de empezar a procesar los pagos de cliente. Si siempre registra en la misma cuenta de saldo, puede definir esa cuenta como la predeterminada y evitar este paso cada vez que abra la página **Registrar pagos de cliente**.  

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Configuración del registro de pago** y luego elija el enlace relacionado. Alternativamente, puede elegir la acción **Configurar** en la página **Registrar pagos de cliente**.
2. Rellene los campos de la página **Configuración del registro de pago**. [!INCLUDE [tooltip-inline-tip_md](../archive/SetupAndAdministration/includes/tooltip-inline-tip_md.md)] Seleccione un campo para obtener una breve descripción del campo o el enlace a la información relacionada.  

> [!TIP]
> Para facilitar la identificación posterior de los movimientos que se registraron a través del diario, puede asignar una serie numérica específica al diario. Esto es útil si utiliza diarios de conciliación de pagos para registrar y liquidar pagos.

## Para registrar los pagos del cliente por separado

1. Elija el icono ![Bombilla que abre la característica Dígame](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Registrar pagos de cliente** y luego elija el enlace relacionado.  

    La página **Registrar pagos de cliente** muestra todos los documentos registrados para los que puede registrarse un pago. La página también se puede abrir desde las páginas **Clientes** y **Ficha de cliente** donde se filtrará automáticamente para el cliente especificado.  
2. Seleccione la casilla **Pago realizado** en la línea que representa el documento registrado para el que se ha realizado un pago.

    Si se selecciona la casilla de verificación **Rellenar fecha de recepción automáticamente** de la página **Configuración de registro de pago**, la fecha de trabajo se tendrá que introducir en el campo **Fecha de recepción**.  
3. En el campo **Fecha recepción**, especifique la fecha en la que se realizó el pago. Esta fecha puede ser distinta de la fecha de trabajo.  
4. En el campo **Importe recibido**, especifique el importe que se ha pagado.

    Para los pagos completos, este importe es el mismo que el importe en el campo **Importe pendiente** en la línea. Para los pagos parciales, este importe es inferior al importe del campo **Importe pendiente** en la línea.
5. Repita los pasos 2 a 4 para las demás líneas que representen documentos registrados para los que se realicen pagos.  
6. Seleccione la acción **Registrar pagos**.  

La información de pagos se registra para los documentos representados por las líneas donde la casilla **Pago realizado** está seleccionada.  

Los movimientos de pago se registran en la cuenta contable, la cuenta de banco y las cuentas de cliente. Cada pago se aplica al documento de venta registrado relacionado.  

## Conciliar los pagos de suma totales
1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Registro de pago** y luego elija el enlace relacionado.
2. Seleccione la casilla **Pago realizado** en las líneas que representan documentos registrados para el mismo cliente para el que se ha realizado un pago de suma total.  

    > [!NOTE]  
    >   El cliente en el campo **Nombre** debe ser igual en todas las líneas que se registrarán como pago de suma total.  

    Si se selecciona la casilla de verificación **Rellenar fecha de recepción automáticamente** de la página **Configuración de registro de pago**, la fecha de trabajo se tendrá que rellenar en el campo **Fecha de recepción**.  
3. En el campo **Fecha recepción**, especifique la fecha en la que se realizó el pago. Esta fecha puede ser distinta de la fecha de trabajo.  

    > [!NOTE]  
    >   Esta fecha debe ser igual en todas las líneas que se registrarán como pago de suma total.  
4. En el campo **Importe recibido**, especifique los importes en varias líneas que suman el importe del pago total.  

    > [!TIP]  
    > Intente registrar el mayor número posible de pagos completos con el importe de suma total. Introduzca los importes cuya cantidad coincida con el importe en el campo **Importe pendiente** en tantas líneas como sea posible.  
5. Repita los pasos 2 a 4 para las demás líneas que representen documentos registrados para el mismo cliente para los que se ha realizado un pago de suma total.  
6. Seleccione la acción **Registrar como pago total**. La información de pagos introducida se registra para los documentos representados por las líneas donde la casilla **Pago realizado** está seleccionada.  

Los movimientos de pago se registran en la cuenta contable, la cuenta de banco y las cuentas de cliente. Cada pago se aplica al documento de venta registrado relacionado.  

Si un pago en el banco no se representa mediante una línea en la página **Registro de pago**, puede ser porque el documento relacionado aún no se ha registrado. En ese caso, puede usar una función de búsqueda para buscar rápidamente el documento y registrarlo para procesar el pago. Para obtener más información, consulte [Buscar un documento determinado de ventas que no esté totalmente facturado](#to-find-a-specific-sales-document-that-isnt-fully-invoiced).  

Si un pago en el banco no se representa mediante ningún documento en [!INCLUDE[prod_short](includes/prod_short.md)], puede abrir un diario general previamente rellenado en la página **Registro de pago** para registrar el pago directamente en la cuenta de saldo sin liquidar el pago a un documento. Alternativamente, puede que desee registrar el pago en el diario hasta que el origen del pago se haya resuelto. Para obtener más información, consulte [Registrar pagos sin documento relacionado](receivables-how-reconcile-customer-payments-list-unpaid-sales-documents.md#to-record-or-post-a-payment-without-a-related-document).  

## Para procesar pagos de cliente con descuentos manualmente
Si ha acordado un descuento por pronto pago con el cliente, los importes de pago pueden ser inferiores a los importes de factura si el pago se produce antes de la fecha de descuento acordada.  

En los procedimientos siguientes se explican cuatro formas distintas para registrar pagos al descuento en la página **Registro de pago**.  

* El importe de pago es igual al importe al descuento restante, y la fecha de pago es antes de la fecha de descuento. Registra el pago tal como está.  
* El importe de pago es igual al importe al descuento restante, pero la fecha de pago es posterior a la fecha de descuento. Registra el pago como parcial. El documento permanece abierto para recopilar o pagar el importe pendiente. También puede definir la fecha de descuento posteriormente para permitir el pago total.  
* El importe del pago es menor que el importe al descuento restante. Registra el pago como parcial. El documento permanece abierto para recopilar o pagar el importe pendiente.  
* El importe del pago es mayor que el importe al descuento restante. Registra los pagos tal como están. Solo se registra el importe pendiente. El importe adicional se abona al cliente.  

### Importar un importe de pago igual al descuento y donde la fecha de pago es antes de la fecha de descuento
1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Registro de pago** y luego elija el enlace relacionado.  
2. Introduzca el importe de pago en el campo **Importe recibido**. El importe es igual al importe en el campo **Importe restante tras descuento**.

    La casilla **Pago realizado** se selecciona automáticamente y el campo **Fecha de recepción** se rellena con la fecha de trabajo.    
3. Introduzca la fecha de pago en el campo **Fecha de recepción**. La fecha es anterior a la fecha del campo **Fecha de descuento del pago**.
4. Compruebe que el campo **Importe pendiente** contenga cero (0).  
5. Seleccione la acción **Registrar pagos** para registrar el pago completo a la cuenta contable, la cuenta de banco y la cuenta de cliente.

### Importar un importe de pago igual al descuento ero donde la fecha de pago es posterior a la fecha de descuento
1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Registro de pago** y luego elija el enlace relacionado.  
2. Introduzca el importe de pago en el campo **Importe recibido**. El importe es igual al importe en el campo **Importe restante tras descuento**.

    La casilla **Pago realizado** se selecciona automáticamente y el campo **Fecha de recepción** se rellena con la fecha de trabajo.
3. En el campo **Fecha de recepción**, especifique una fecha de pago que sea posterior a la fecha del campo **Fecha de descuento del pago**. Los campos de fecha cambian a la fuente color rojo, y un mensaje de error se muestra en la parte inferior de la página.

    > [!TIP]  
    >   Si desea crear una excepción y conceder el descuento aunque el pago haya vencido, realice los pasos siguientes:
4. Seleccione la acción **Detalles**.  
5. En la página **Detalles del registro de pago**, en el campo **Fecha de descuento del pago**, en la ficha desplegable **Descuento del pago**, especifique una fecha que sea posterior a la fecha del campo **Fecha de recepción**, en la página **Registro de pago**.  

    El mensaje de error y la fuente de color rojo desaparecen, y puede seguir procesando el pago descontado.    
6. Compruebe que el campo **Importe pendiente** contenga el importe pendiente para pagar el importe total de la factura.  
7. Seleccione la acción **Registrar pagos** para registrar el pago parcial en la cuenta contable, la cuenta de banco y la cuenta de cliente.  

El documento relacionado quedará abierto.

### Procesar un pago que es menor que el importe al descuento restante
1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Registro de pago** y luego elija el enlace relacionado.  
2. Introduzca el importe de pago en el campo **Importe recibido**. El importe es inferior al importe del campo **Importe restante tras descuento**.

    La casilla **Pago realizado** se selecciona automáticamente y el campo **Fecha de recepción** se rellena con la fecha de trabajo.  
3. Introduzca la fecha de pago en el campo **Fecha de recepción**. La fecha es anterior a la fecha del campo **Fecha de descuento del pago**.
4. Compruebe que el campo **Importe pendiente** contiene el importe pendiente para pagar el importe al descuento.  
5. Seleccione la acción **Registrar pagos** para registrar el pago parcial en la cuenta contable, la cuenta de banco y la cuenta de cliente.  

El documento relacionado quedará abierto.

### Procesar un pago que es mayor que el importe al descuento restante
1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Registro de pago** y luego elija el enlace relacionado.  
2. Introduzca el importe de pago en el campo **Importe recibido**. El importe es superior al importe del campo **Importe restante tras descuento**.  

    La casilla **Pago realizado** se selecciona automáticamente y el campo **Fecha de recepción** se rellena con la fecha de trabajo.    
3. Introduzca la fecha de pago en el campo **Fecha de recepción**. La fecha es anterior a la fecha del campo **Fecha de descuento del pago**.
4. Compruebe que el campo **Importe pendiente** contenga cero (0).  
5. Seleccione la acción **Registrar pagos** para registrar el pago completo a la cuenta contable, la cuenta de banco y la cuenta de cliente.  

El documento relacionado está cerrado y al cliente se acredita el importe de pago en exceso.  

## Buscar un documento de ventas específico que no está facturado totalmente
La página **Registro de pago** le facilita las tareas necesarias para calcular el saldo de las cuentas internas con cifras reales de efectivo para garantizar la colección efectiva de los clientes y el pago debido a los proveedores. Muestra los pagos entrantes pendientes como líneas que representen los documentos de venta donde se debe un importe para el pago.  

Normalmente, cuando un pago se ha realizado, registrado en el banco, etc., el documento de venta o compra relacionado se representa como una línea en la página **Registro de pago** porque el documento en cuestión está esperando el registro del pago con el importe pendiente. Sin embargo, a veces un pago que se ha realizado no se representa mediante una línea en la página **Registro de pago**, normalmente porque en el documento en cuestión no se ha registrado la factura por completo.

En la página **Búsqueda de documentos**, podrá buscar entre los documentos que no se han facturado por completo. Puede buscar basado en uno o varios de los siguientes criterios:  

* N.º documento  
* Importe o rango de importes  

En el procedimiento siguiente se explica cómo buscar un documento determinado mediante ambos criterios de búsqueda.  

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Registro de pago** y luego elija el enlace relacionado.
2. Con el puntero en cualquier línea, seleccione la acción **Buscar documentos**.
3. En la página **Búsqueda de documentos**, especifique un valor de búsqueda en el campo **Número de documento**.  

    > [!NOTE]  
    >   El valor que especifique en este campo se encierra entre los caracteres comodín ocultos. Esto significa que la función busca todos los números de documento que contengan el valor especificado.    
4. En el campo **Importe**, especifique el importe concreto que existe en el documento que desee buscar.  
5. En el campo **% tolerancia de importe**, especifique un valor de porcentaje para definir el rango de importes que desea buscar para encontrar el documento abierto.  

    Si especifica 10, la función buscará los importes en un rango entre un diez por ciento más bajo y un diez por ciento más alto que el valor del campo **Importe**.    
6. Seleccione la acción **Buscar**.  

La función de búsqueda busca entre los documentos que no se han facturado totalmente según los criterios especificados.  

Si hay documentos que coinciden con los criterios de búsqueda, la página **Resultado de la búsqueda de documentos** se abrirá en las líneas de presentación que representan dichos documentos. Cada línea contiene un número de documento, una descripción y un importe. Esta información facilita la búsqueda de un documento específico.

Si un pago en el banco no se representa mediante ningún documento en [!INCLUDE[prod_short](includes/prod_short.md)], puede abrir un diario general previamente rellenado en la página **Registro de pago** para registrar el pago directamente en la cuenta de saldo sin liquidar el pago a un documento. Alternativamente, puede que desee registrar el pago en el diario hasta que el origen del pago se haya resuelto.  

## Registrar pagos sin documento relacionado
Si un pago en el banco no se representa mediante ningún documento en [!INCLUDE[prod_short](includes/prod_short.md)], puede abrir una línea de diario general previamente rellenada en la página **Registro de pago** para registrar el pago directamente en la cuenta de saldo sin liquidar el pago a un documento. Alternativamente, puede que desee registrar el pago en el diario hasta que el origen del pago se haya aclarado.  

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Registro de pago** y luego elija el enlace relacionado.
2. Seleccione la acción **Diario general**.  

    La página **Diario general** se abre con una línea que contiene la cuenta de saldo de la sección de diario configurada en la página **Configuración de registro de pago**.  
3. Rellene el resto de los campos de cada línea del diario general. Por ejemplo, proporcione el importe, el número de cliente o la información del extracto bancario. Para obtener más información, consulte [Registrar transacciones directamente en la contabilidad](finance-how-post-transactions-directly.md).  

Puede registrar la línea del diario para actualizar el total de la cuenta de contrapartida. También puede dejar la línea del diario sin registrar, y quizás agregarla con una nota conforme el pago necesita más análisis.  

Si deja la línea del diario sin registrar, agregará al valor del campo **Saldo no registrado** en la parte inferior de la página **Registro de pago**.  

## Consulte también
[Administrar cobros](receivables-manage-receivables.md)  
[Ccial](sales-manage-sales.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]