---
title: Registrar documentos y diarios de empresas vinculadas
description: Este tema explica cómo utilizar los documentos o diarios de empresas vinculadas sirven para registrar transacciones con empresas vinculadas asociadas.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bnielse
ms.topic: how-to
ms.date: 02/06/2023
ms.custom: bap-template
ms.search.keywords: 'IC, group, consolidation, affiliate, subsidiary, bank-to-bank'
ms.search.form: '600, 610'
---
# <a name="work-with-intercompany-documents-and-journals"></a><a name="work-with-intercompany-documents-and-journals"></a>Usar documentos y diarios de empresas vinculadas

Utilice documentos o diarios de empresas vinculadas para registrar transacciones con empresas vinculadas asociadas. Puede contabilizar transacciones en cuentas de mayor y, si ha configurado cuentas bancarias de empresas vinculadas, también puede contabilizar transacciones de banco a banco. Para obtener más información sobre cómo configurar cuentas bancarias de empresas vinculadas, vaya a [Especifique las cuentas bancarias que se utilizarán para los socios de empresas vinculadas](intercompany-how-setup.md#specify-the-bank-accounts-to-use-for-intercompany-partners).  

Al registrar un documento o una línea de diario de empresas vinculadas en su empresa, el programa crea un documento o una línea de diario correspondiente en la bandeja de salida entre empresas vinculadas. Transfiere la línea de su bandeja de salida a su socio. Después, su socio podrá registrar la correspondiente transacción en su empresa, sin tener que volver a introducir los datos.

Para los documentos de ventas y compras, el código de socio de empresas vinculadas del cliente o del vendedor de empresas vinculadas garantiza que todos los pedidos y facturas generados en relación con las transacciones centre socios producirán documentos correspondientes en las empresas asociadas. Las cuentas de la empresa cuadran correctamente.

Lo mismo se aplica a las líneas de diario general de empresas vinculadas. No necesita especificar cuentas, simplemente elija la empresa asociada. A continuación, se crean las líneas de diario general de empresas vinculadas en la empresa asociada.

## <a name="fill-in-and-send-an-intercompany-sales-order"></a><a name="fill-in-and-send-an-intercompany-sales-order"></a>Rellene y envíe un pedido de venta de empresas vinculadas

Puede enviar pedidos de venta y de compra y devoluciones antes de registrarlos. Las facturas y las notas de abono no se pueden enviar hasta que se hayan contabilizado.

El procedimiento siguiente describe cómo rellenar y enviar un pedido de venta de empresas vinculadas. Los mismos pasos se aplican a los pedidos de compras y devoluciones de empresas vinculadas, así como en facturas y abonos de venta registrados de empresas vinculadas.  

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Pedidos de venta** y, a continuación, elija el vínculo relacionado.  
2. Para crear un nuevo pedido de venta, elija **Nuevo**. Para obtener más información, vea [Vender productos](sales-how-sell-products.md).  
3. Rellene los campos según sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Asegúrese de que el cliente es socio de una empresa vinculada.
5. Para enviar el pedido de venta antes de registrarlo, elija la acción **Envío ped. venta IC** .

> [!NOTE]
> Si ejecuta el paso 5, el pedido de venta se pasa a la bandeja de salida de empresas vinculadas, donde puede enviarlo más adelante. Para obtener más información sobre la bandeja de entrada y la bandeja de salida de empresas vinculadas, vaya a [Administrar la bandeja de entrada y la bandeja de salida de empresas vinculadas](intercompany-how-manage-intercompany-inbox.md).

## <a name="fill-in-and-post-an-intercompany-journal"></a><a name="fill-in-and-post-an-intercompany-journal"></a>Rellenar y registrar un diario de empresas vinculadas

Al registrar un documento o una línea de diario general en su empresa, el programa crea una línea de diario correspondiente en la bandeja de salida entre empresas vinculadas, que puede transferir a su socio. Con el primer lanzamiento de versiones de 2022, también puede configurar la empresa para la creación automática de transacciones recibidas entre empresas vinculadas que los socios de empresas vinculadas contabilizan en diarios generales entre empresas vinculadas. Después, su socio podrá registrar la correspondiente transacción en su empresa, sin tener que volver a introducir los datos.

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Diarios generales de empresas vinculadas** y luego elija el enlace relacionado.  
2. Abra el lote de diario. Para obtener más información, consulte [Trabajar con diarios generales](ui-work-general-journals.md).
3. Rellene los campos según sea necesario. [!INCLUDE [tooltip-inline-tip_md](../archive/invoicing/includes/tooltip-inline-tip_md.md)]
4. En el campo **Nº cuenta IC asociada**, introduzca la cuenta de contabilidad IC de empresas vinculadas en la que se registrará el importe de la empresa de su socio.

    > [!NOTE]
    > Este campo debe rellenarse en una línea con una cuenta bancaria o de contabilidad en el campo **Nº cuenta** o en el campo **Cta. contrapartida**.  
5. Seleccione la acción **Registrar**.

Los movimientos se registran en su empresa y se crea un diario con los movimientos correspondientes en la bandeja de salida de empresas vinculadas, que puede enviar a su empresa asociada.

## <a name="see-also"></a><a name="see-also"></a>Consulte también

[Gestión de transacciones entre empresas vinculadas](intercompany-manage.md)  
[Finanzas](finance.md)  
[Configurar las finanzas](finance-setup-finance.md)  
[Trabajar con diarios generales](ui-work-general-journals.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
