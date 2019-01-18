---
title: Cancelar o retirar activos fijos | Documentos de Microsoft
description: Debe registrar un valor de baja cuando se rechaza, vende o retira un activo fijo.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: scrap
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 33b900f1ac9e295921e7f3d6ea72cc93939d8a1b
ms.openlocfilehash: 10e7939378d222e2e2f915c89f820e000615ac1e
ms.contentlocale: es-es
ms.lasthandoff: 11/26/2018

---
# <a name="dispose-of-or-retire-fixed-assets"></a>Cancelar o retirar activos fijos
En el momento de vender o dar de baja un activo, el valor de venta o baja debe registrarse para calcular y anotar las ganancias o las pérdidas. Un movimiento de venta o baja debe ser el último movimiento registrado de un activo. Puede registrar más de un movimiento de venta o baja en activos fijos que desea dar de baja parcialmente. El total de todos los importes de venta o baja registrados debe ser un abono.  

> [!NOTE]  
>   Si negocia con un activo fijo y lo cambia por otro, deberá registrar la venta del activo anterior (venta/baja) y la compra del nuevo (adquisición). Para obtener más información, vea [Adquirir activos fijos](fa-how-acquire.md).  

## <a name="to-post-a-disposal-from-the-fixed-asset-gl-journal"></a>Para registrar una venta/baja desde el diario general de activos fijos
1. Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Diarios generales A/F** y luego elija el enlace relacionado.  
2. Cree una línea inicial de diario y rellene los campos según sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
3. En el campo **A/F Tipo registro**, seleccione **Venta/baja**.  
4. Elija la acción **Introducir saldo AF**. Se crea una segunda línea de diario para la cuenta contrapartida que se ha configurado para el registro de venta/baja.  

    > [!NOTE]  
    >   El paso 4 solo funciona si ha configurado lo siguiente: en la página **A/F Ficha grupo contable** del grupo contable del activo fijo, el campo **Cuenta de venta/baja** contiene la cuenta de cargo y el campo **Cuenta contrapartida venta/baja** contiene la cuenta contable en la que desea registrar los movimientos de contrapartida para apreciación. Para obtener más información, vea la sección "Para configurar grupos contables de activos fijos" en [Configurar información general del activo fijo](fa-how-setup-general.md).  
5. Seleccione la acción **Registrar**.  

Si vende o dispone de parte de un activo, debe dividir el activo antes de poder grabar la transacción de venta/baja. Para obtener más información, consulte [Transferir, dividir o combinar activos fijos](fa-how-trans-split-combine.md).  

## <a name="to-view-disposal-ledger-entries"></a>Para ver movimientos venta/baja
En el momento de vender o dar de baja un activo, el valor de venta o baja se registra en las cuentas contables en las que puede ver el resultado.  

1. Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Activos fijos** y luego elija el enlace relacionado.  
2. Seleccione el activo en el que desea ver los movimientos y, a continuación, elija la acción **Libros amortización**.  
3. Seleccione el libro de amortización en el que desea ver los movimientos y, a continuación, elija la acción **Movimientos**.  
4. Seleccione una línea con **Venta/baja** en el campo **A/F Categoría registro**, y a continuación seleccione la acción **Navegar**.  
5. En la página **Navegar**, seleccione la línea del movimiento de contabilidad y, a continuación, seleccione la acción **Mostrar**.  

La página **Movs. contabilidad** se abre y puede ver los movimientos que se produjeron al registrar la venta/baja.  

## <a name="see-also"></a>Consulte también
[Activos fijos](fa-manage.md)  
[Configurar activos fijos](fa-setup.md)  
[Finanzas](finance.md)  
[Introducción](product-get-started.md)  
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

