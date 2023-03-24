---
title: Registrar documentos y diarios de empresas vinculadas
description: Este tema explica cómo utilizar los documentos o diarios de empresas vinculadas sirven para registrar transacciones con empresas vinculadas asociadas.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'IC, group, consolidation, affiliate, subsidiary'
ms.search.form: '600, 610'
ms.date: 03/09/2022
ms.author: edupont
---
# Usar documentos y diarios de empresas vinculadas
Los documentos o diarios de empresas vinculadas sirven para registrar transacciones con empresas vinculadas asociadas. Al registrar un documento o una línea de diario de empresas vinculadas en su empresa, el programa crea un documento o una línea de diario correspondiente en la bandeja de salida entre empresas vinculadas, que puede transferir a su socio. Después, su socio podrá registrar la correspondiente transacción en su empresa, sin tener que volver a introducir los datos.

Para los documentos de ventas y compras, el código de socio entre empresas del cliente o del vendedor involucrados garantiza que todas las órdenes y facturas generadas en relación con las transacciones con estas empresas producirán documentos correspondientes en la empresa asociada, lo que redundará en el equilibrio correcto de las cuentas.

Para las líneas de diario generales de empresas vinculadas, no tiene que especificar las cuentas de cada uno de los grupos de libros, si no que sólo tiene que proporcionar la identificación de la empresa asociada. A continuación, se crean las correspondientes líneas de diario generales de empresas vinculadas en la empresa asociada que hacen que los libros queden cuadrados en las dos empresas implicadas en la transacción.

## Para rellenar y enviar un pedido de venta de empresas vinculadas
Puede enviar pedidos de venta y de compra y devoluciones antes de registrarlos. Las facturas y los abonos no se pueden enviar hasta que se hayan registrado.

El procedimiento siguiente describe cómo rellenar y enviar un pedido de venta de empresas vinculadas. Los mismos pasos se aplican a los pedidos de compras y devoluciones de empresas vinculadas, así como en facturas y abonos de venta registrados de empresas vinculadas.  

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Pedidos de venta** y, a continuación, elija el vínculo relacionado.  
2. Para crear un nuevo pedido de venta, elija **Nuevo**. Para obtener más información, vea [Vender productos](sales-how-sell-products.md).  
3. Rellene los campos según sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Asegúrese de que el cliente es socio de una empresa vinculada.
5. Para enviar el pedido de venta antes de registrarlo, elija la acción **Envío ped. venta IC** .

> [!NOTE]
> Si ejecuta el paso 4, el pedido de venta se pasará a la bandeja de salida de empresas vinculadas donde puede enviarlo más adelante. Para obtener más información, consulte [Administrar la bandeja de entrada y la bandeja de salida de empresas vinculadas](intercompany-how-manage-intercompany-inbox.md).

## Para rellenar y registrar un diario de empresas vinculadas

Al registrar un documento o una línea de diario general en su empresa, el programa crea una línea de diario correspondiente en la bandeja de salida entre empresas vinculadas, que puede transferir a su socio. Con el primer lanzamiento de versiones de 2022, también puede configurar la empresa para la creación automática de transacciones recibidas entre empresas vinculadas de socios de empresas vinculadas, registradas a través del diario general entre empresas vinculadas. Después, su socio podrá registrar la correspondiente transacción en su empresa, sin tener que volver a introducir los datos.

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Diarios generales de empresas vinculadas** y luego elija el enlace relacionado.  
2. Abra la sección del diario correspondiente. Para obtener más información, consulte [Trabajar con diarios generales](ui-work-general-journals.md).
3. Rellene los campos según sea necesario.
4. En el campo **Nº cuenta IC asociada**, introduzca la cuenta de contabilidad IC de empresas vinculadas en la que se registrará el importe de la empresa de su socio.

    > [!NOTE]
    > Este campo debe rellenarse en una línea con una cuenta bancaria o de contabilidad en el campo **Nº cuenta** o en el campo **Cta. contrapartida**.  
5. Seleccione la acción **Registrar**.

Los movimientos correspondientes se registran en su empresa y se creará un diario con los movimientos correspondientes en la bandeja de salida de empresas vinculadas que puede enviar a su empresa asociada. Para obtener más información, consulte [Administrar la bandeja de entrada y la bandeja de salida de empresas vinculadas](intercompany-how-manage-intercompany-inbox.md).

## Consulte también

[Gestión de transacciones entre empresas vinculadas](intercompany-manage.md)  
[Finanzas](finance.md)  
[Configurar las finanzas](finance-setup-finance.md)  
[Trabajar con diarios generales](ui-work-general-journals.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]