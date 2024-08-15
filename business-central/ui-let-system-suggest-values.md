---
title: Dejar que Business Central sugiera valores
description: 'Para evitar cálculos manuales y completar rápidamente y de forma precisa las tareas, puede configurar la entrada de datos automática de forma que Business Central rellene los campos seleccionados.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.form: '39, 251, 981'
ms.date: 07/16/2024
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# <a name="let--suggest-values"></a>Sugerimos valores [!INCLUDE[prod_short](includes/prod_short.md)]
[!INCLUDE[prod_short](includes/prod_short.md)] puede ayudarle a completar las tareas más rápida y correctamente rellenando previamente los campos o las líneas completas con los datos que, de no ser así, debería calcular e introducir usted. Aunque los datos introducidos automáticamente son siempre correctos, puede cambiarlos si lo desea.

La funcionalidad que introduce los valores del campo por usted, normalmente, se ofrece mediante tareas en las que se introducen grandes volúmenes de datos transaccionales y se desea evitar errores y ahorrar tiempo. Este artículo contiene una selección de dichas funcionalidades. Se agregarán más secciones en futuras actualizaciones de [!INCLUDE[prod_short](includes/prod_short.md)].

## <a name="the-suggest-balancing-amount-check-box-on-the-general-journal-batches-page"></a>Casilla **Sugerir importe de compensación** en la página **Secciones diario general**
Por ejemplo, cuando ingresa líneas de diario general para múltiples gastos que deben registrarse en la misma cuenta bancaria, cada vez que ingresa una nueva línea de diario para un gasto, puede hacer que el campo  **Monto**  en la línea de la cuenta bancaria se actualice automáticamente al monto que equilibra los gastos. Para obtener más información sobre trabajar con diarios generales, vea [Trabajar con diarios generales](ui-work-general-journals.md).

### <a name="to-have-the-amount-field-on-balancing-general-journal-lines-filled-automatically"></a>Para tener el campo **Importe** en la contrapartida de las líneas del diario general rellenado automáticamente
1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Diarios generales**, y luego elija el enlace relacionado.
2. En la línea que aparece el proceso de su diario general preferido, seleccione la casilla **Sugerir importe de compensación**.
3. Abra el diario general y registre las transacciones usando la funcionalidad descrita para la inserción automática del valor de un campo.       

Para obtener información acerca de cómo configurar un proceso personal del diario general, por ejemplo, para el control de gastos, vea [Trabajar con diarios generales](ui-work-general-journals.md).

## <a name="the-automatically-fill-date-received-field-on-the-payment-registration-page"></a>Campo **Rellenar fecha de recepción automáticamente** en la página **Registro de pago**
La página **Registrar pagos de clientes** muestra los pagos entrantes pendientes como líneas que representan documentos de ventas en los que se debe pagar un monto. Para obtener más información acerca de liquidar los pagos de clientes, consulte [Conciliar pagos de cliente desde una lista de documentos de ventas sin abonar](receivables-how-reconcile-customer-payments-list-unpaid-sales-documents.md).

Las acciones principales en la página son completar la casilla de verificación  **Pago realizado** y el campo  **Fecha de recepción** . Puede configurar [!INCLUDE[prod_short](includes/prod_short.md)] para que introduzca la fecha del trabajo automáticamente en el campo **Fecha recepción** cuando selecciona la casilla de verificación **Pago realizado**.

### <a name="to-have-the-date-received-field-on-the-payment-registration-page-filled-automatically"></a>Para tener el campo **Fecha recepción** rellenado automáticamente en la página **Registro de pago**
1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Configuración del registro de pago** y luego elija el enlace relacionado.
2. Seleccione la casilla **Rellenar automáticamente fecha recepción**.
3. Abra la página  **Registrar pagos de clientes**  y proceda a procesar los pagos entrantes de clientes utilizando la funcionalidad descrita para el ingreso automático de un valor de campo.

## <a name="see-also"></a>Consulte también
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Finanzas](finance.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
