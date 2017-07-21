---
title: Cancelar o retirar activos fijos | Documentos de Microsoft
description: Debe registrar un valor de baja cuando se rechaza, vende o retira un activo fijo.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: scrap
ms.date: 06/02/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 5fc65c97e7c95a37d54b4084aaf8616169b625db
ms.contentlocale: es-es
ms.lasthandoff: 07/07/2017


---
# <a name="how-to-dispose-of-or-retire-fixed-assets"></a>Procedimiento: Cancelar o retirar activos fijos
En el momento de vender o dar de baja un activo, el valor de venta o baja debe registrarse para calcular y anotar las ganancias o las pérdidas. Un movimiento de venta o baja debe ser el último movimiento registrado de un activo. Puede registrar más de un movimiento de venta o baja en activos fijos que desea dar de baja parcialmente. El total de todos los importes de venta o baja registrados debe ser un abono.  

> [!NOTE]  
>   Si negocia con un activo fijo y lo cambia por otro, deberá registrar la venta del activo anterior (venta/baja) y la compra del nuevo (adquisición). Para obtener más información, vea [Procedimiento: Activos fijos adquiridos](fa-how-acquire.md).  

## <a name="to-post-a-disposal-from-the-fixed-asset-gl-journal"></a>Para registrar una venta/baja desde el diario general de activos fijos
1. Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Diarios generales A/F** y, a continuación, seleccione el vínculo relacionado.  
2. Cree una línea inicial de diario y rellene los campos según sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
3. En el campo **A/F Tipo registro**, seleccione **Venta/baja**.  
4. Elija la acción **Introducir saldo AF**. Se crea una segunda línea de diario para la cuenta contrapartida que se ha configurado para el registro de venta/baja.  

    > [!NOTE]  
>   El paso 4 solo funciona si ha configurado lo siguiente: en la ventana **A/F Ficha grupo contable** del grupo contable del activo fijo, el campo **Cuenta de venta/baja** contiene la cuenta de cargo y el campo **Cuenta contrapartida venta/baja** contiene la cuenta contable en la que desea registrar los movimientos de contrapartida para apreciación. Para obtener más información, vea la sección "Para configurar grupos contables de activos fijos" en [Procedimiento: Configurar información general del activo fijo](fa-how-setup-general.md).  
5. Seleccione la acción **Registrar**.  

    Si vende o dispone de parte de un activo, debe dividir el activo antes de poder grabar la transacción de venta/baja. Para obtener más información, consulte [Procedimiento: Transferir, dividir o combinar activos fijos](fa-how-trans-split-combine.md).  

## <a name="to-view-disposal-ledger-entries"></a>Para ver movimientos venta/baja
En el momento de vender o dar de baja un activo, el valor de venta o baja se registra en las cuentas contables en las que puede ver el resultado.  

1. Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Activos fijos** y, a continuación, seleccione el vínculo relacionado.  
2. Seleccione el activo en el que desea ver los movimientos y, a continuación, elija la acción **Libros amortización**.  
3. Seleccione el libro de amortización en el que desea ver los movimientos y, a continuación, elija la acción **Movimientos**.  
4. Seleccione una línea con **Venta/baja** en el campo **A/F Categoría registro**, y a continuación seleccione la acción **Navegar**.  
5. En la ventana **Navegar**, seleccione la línea del movimiento de contabilidad y, a continuación, seleccione la acción **Mostrar**.  

La ventana **Movs. contabilidad** se abre y puede ver los movimientos que se produjeron al registrar la venta/baja.  

## <a name="see-also"></a>Consulte también
[Activos fijos](fa-manage.md)  
[Configurar activos fijos](fa-setup.md)  
[Finanzas](finance.md)  
[[!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)  
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

