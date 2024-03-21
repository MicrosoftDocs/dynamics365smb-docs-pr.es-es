---
title: Cancelar o retirar activos fijos
description: 'En el momento de vender o dar de baja un activo, el valor de venta o baja debe registrarse para calcular y anotar las ganancias o las pérdidas.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: scrap
ms.search.form: '5628, 5610, 5611, 5629, 5633'
ms.date: 06/15/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# <a name="dispose-of-or-retire-fixed-assets"></a>Cancelar o retirar activos fijos

En el momento de vender o dar de baja un activo, el valor de venta o baja debe registrarse para calcular y anotar las ganancias o las pérdidas. Un movimiento de venta o baja debe ser el último movimiento registrado de un activo. Puede registrar más de un movimiento de venta o baja en activos fijos que desea dar de baja parcialmente. El total de todos los importes de venta o baja registrados debe ser un abono.  

> [!NOTE]  
> Si negocia con un activo fijo y lo cambia por otro, deberá registrar la venta del activo anterior (venta/baja) y la compra del nuevo (adquisición). Para obtener más información, vea [Adquirir activos fijos](fa-how-acquire.md).  

Los siguientes pasos suponen que ya ha configurado los grupos contables relevantes en la página **Grupos registro A/F**. Para obtener más información, vea [Para configurar los grupos contables de activos fijos](fa-how-setup-general.md#to-set-up-fixed-asset-posting-groups).  

## <a name="to-post-a-disposal-from-the-fixed-asset-gl-journal"></a>Para registrar una venta/baja desde el diario general de activos fijos

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Diarios generales de activos fijos** y luego elija el enlace relacionado.  
2. Cree una línea inicial de diario y rellene los campos según sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
3. En el campo **A/F Tipo registro**, seleccione **Venta/baja**.  
4. Elija la acción **Introducir saldo AF**. Se crea una segunda línea de diario para la cuenta contrapartida que se ha configurado para el registro de venta/baja.  

    > [!NOTE]  
    >  El paso 4 solo funciona si ha configurado lo siguiente: en la página **A/F Ficha grupo contable** del grupo contable del activo fijo, el campo **Cuenta de venta/baja** contiene la cuenta de cargo y el campo **Cuenta contrapartida venta/baja** contiene la cuenta contable en la que desea registrar los movimientos de contrapartida para apreciación. Para obtener más información, vea [Para configurar los grupos contables de activos fijos](fa-how-setup-general.md#to-set-up-fixed-asset-posting-groups).  
5. Seleccione la acción **Registrar**.  

Si vende o dispone de parte de un activo, debe dividir el activo antes de poder grabar la transacción de venta/baja. Para obtener más información, consulte [Transferir, dividir o combinar activos fijos](fa-how-trans-split-combine.md).  

## <a name="to-view-disposal-ledger-entries"></a>Para ver movimientos venta/baja

En el momento de vender o dar de baja un activo, el valor de venta o baja se registra en las cuentas contables en las que puede ver el resultado.  

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Activos fijos** y luego elija el enlace relacionado.  
2. Seleccione el activo en el que desea ver los movimientos y, a continuación, elija la acción **Libros amortización**.  
3. Seleccione el libro de amortización en el que desea ver los movimientos y, a continuación, elija la acción **Movimientos**.  
4. Seleccione una línea con **Venta/baja** en el campo **A/F Categoría registro**, y a continuación elija la acción **Buscar entradas**.  
5. En la página **Buscar movimientos**, seleccione la línea del movimiento de contabilidad y, a continuación, seleccione la acción **Mostrar movimientos relacionados**.  

La página **Movs. contabilidad** se abre y puede ver los movimientos que se produjeron al registrar la venta/baja.  

## <a name="see-also"></a>Consulte también .

[Activos fijos](fa-manage.md)  
[Configuración de activos fijos](fa-setup.md)  
[Para configurar los grupos contables de activos fijos](fa-how-setup-general.md#to-set-up-fixed-asset-posting-groups).  
[Finanzas](finance.md)  
[Preparación para hacer negocios](ui-get-ready-business.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Buscar movimientos](ui-find-entries.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
