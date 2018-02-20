---
title: Conciliar cuentas bancarias | Documentos de Microsoft
description: "Describe cómo el valor de inventario se concilia con el libro mayor."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: bank account balance, bank statement
ms.date: 06/02/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: fa1225e8467ab805fc14afdd39eef556dc7ad5fc
ms.contentlocale: es-es
ms.lasthandoff: 01/30/2018

---
# <a name="reconcile-bank-accounts-separately"></a>Conciliar cuentas bancarias
Para conciliar las cuentas bancarias en [!INCLUDE[d365fin](includes/d365fin_md.md)] con los extractos recibidos del banco, primero deberá rellenar las líneas de la ventana **Conciliación banco**.

> [!NOTE]  
>   También puede conciliar las cuentas bancarias en la ventana **Diario de conciliación de pagos**. Todas las cuenta abiertas relacionada con los movimientos de los clientes o los proveedores se cerrarán cuando seleccione la acción **Registrar pagos y conciliar banco**. Eso significa que la cuenta bancaria se concilia automáticamente por los pagos que registró mediante el diario. Para obtener más información, vea [Conciliar pagos con liquidación automática](receivables-how-reconcile-payments-auto-application.md).

Para habilitar tanto la importación de extractos bancarios como la fuente de banco, primero debe configurar y habilitar el servicio de fuente de banco de Envestnet Yodlee y, a continuación, vincular sus cuentas bancarias a las cuentas bancarias en línea relacionadas. Para obtener más información, vea [Configuración del servicio de fuente de banco de Envestnet Yodlee](bank-how-setup-bank-statement-service.md)

Las líneas de la ventana **Conciliación banco** se dividen en dos paneles. El panel de **Líneas de extracto bancario** muestra tanto las transacciones bancarias como los movimientos con pagos pendientes. El panel **Movs. bancos** muestra los movimientos de la cuenta bancaria.

La actividad de búsqueda y liquidación de los movimientos que hay que conciliar se denomina *coincidencia*. Puede realizar la correspondencia automáticamente mediante la función **Conciliar automáticamente**. Alternativamente, puede seleccionar manualmente líneas en ambos paneles para vincular cada línea del extracto bancario a uno o más movimientos de banco relacionados y, a continuación, utilizar la función **Conciliar manualmente**. La casilla de verificación **Liquidado** se selecciona en las líneas en las que los movimientos coinciden.

Puede rellenar el panel **Líneas de extracto bancario** en la ventana **Conciliación banco** de la siguiente manera:

* Automáticamente, utilizando la función **Importar extracto banco** para rellenar las líneas según los extractos de banco reales basándose en un archivo que proporciona el banco.
* Manualmente, usando la función **Proponer líneas** para rellenar las líneas con los movimientos de las facturas que tienen pagos pendientes.

Cuando el valor en el campo **Saldo total** en el panel **Líneas de extracto bancario** es igual al valor del campo **Saldo a conciliar** en el panel **Movs. bancos**, puede seleccionar la acción **Registrar** para conciliar los movimientos de la cuenta bancaria liquidados. Los movimientos no liquidados de la cuenta permanecerán en la ventana, lo que indica que los pagos procesados para el banco no están reflejados en el último extracto bancario o que algunos pagos se han recibido en cheques.

> [!NOTE]  
>   Si las líneas del extracto bancario están relacionadas con los movimientos del cheque, no puede utilizar las funciones de correspondencia. En lugar de eso, debe elegir la acción **Liquidar movs.** y, a continuación, seleccionar el movimiento de cheque correspondiente con el que desea relacionar la línea del extracto de cuenta.

## <a name="to-fill-bank-reconciliation-lines-by-importing-a-bank-statement"></a>Para rellenar las líneas de conciliación de bancos importando un extracto bancario
1. Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Conciliación banco** y, a continuación, seleccione el vínculo relacionado.
2. Seleccione la acción **Nuevo**.
3. En el campo **Cód. cuenta banco**, seleccione la cuenta de banco que desee. Los movimientos de cuentas bancarias que existan en la cuenta aparecen en el panel **Movs. bancos**.
4. En el campo **Fecha extracto**, escriba la fecha del extracto del banco.
5. En el campo **Saldo final extracto** escriba el saldo del extracto del banco.
6. Si tiene un archivo de extracto bancario seleccione la acción **Importar extracto bancario**.
7. Busque el archivo y haga clic en el botón **Abrir** para importar las transacciones bancarias en las líneas de la ventana **Conciliación banco**.

## <a name="to-fill-bank-reconciliation-lines-with-the-suggest-lines-function"></a>Para rellenar las líneas de conciliación bancarias con la función Proponer líneas
1. En la ventana **Conciliación banco** seleccione la acción **Proponer líneas**.
2. En el campo **Fecha inicial** escriba la fecha de registro más antigua para la conciliación de los movimientos.
3. En el campo **Fecha final**, escriba la fecha de registro que se usó por última vez para la conciliación de los movimientos.
4. Seleccione la casilla de verificación **Incluir cheques** para proponer movimientos de cheques en lugar de los movimientos correspondientes de la cuenta.
5. Elija el botón **Aceptar**.

## <a name="to-match-bank-statement-lines-with-bank-account-ledger-entries-automatically"></a>Para conciliar automáticamente las líneas de extracto bancario con movimientos de la cuenta
1. En la ventana **Conciliación banco** seleccione la acción **Conciliar automáticamente**. La ventana **Conciliar movimientos** se abre.
2. En el campo **Tolerancia de datos de transacción (días)**, especifique el intervalo de días antes y después de la fecha de registro del movimiento del banco dentro de la cual la función buscará las fechas de transacciones coincidentes en el extracto bancario.

    Si especifica cero o deja el campo en blanco la función **Conciliar automáticamente** buscará solo por las fechas de transacción coincidentes en la fecha de registro de movimientos de la cuenta.
3. Elija el botón **Aceptar**.

    Todas las líneas del extracto bancario y los movimientos la cuenta que pueden coincidir cambian a fuente verde y la casilla **Conciliado** queda seleccionada.
4. Para eliminar un coincidencia seleccione la línea de extracto de cuenta y, a continuación, seleccione la acción **Eliminar conciliación**.

## <a name="to-match-bank-statement-lines-with-bank-account-ledger-entries-manually"></a>Para conciliar manualmente las líneas de extracto bancario con movimientos de la cuenta
1. En la ventana **Conciliar banco** seleccione una línea no conciliada en el panel **Líneas de extracto bancario**.
2. En el panel **Movs. bancos** seleccione uno o más movimientos de la cuenta que pueden coincidir con la línea del extracto bancario seleccionada. Para elegir varias líneas, mantenga presionada la tecla CTRL.
3. Seleccione la acción **Conciliar manualmente**.

    La línea del extracto de cuenta seleccionada y los movimientos de la cuenta de banco seleccionados cambian a fuente verde, y la casilla **Conciliado** en el panel derecho está seleccionado.
4. Repita los pasos 1 a 3 para todas las líneas del extracto de cuenta que no coinciden.
5. Para eliminar un coincidencia seleccione la línea de extracto de cuenta y, a continuación, seleccione la acción **Eliminar conciliación**.

## <a name="to-create-missing-ledger-entries-to-match-bank-transactions-with"></a>Para crear movimientos no existentes para coincidir con las transacciones de banco
En ocasiones, un extracto bancario contiene importes por los intereses y recargos cobrados. Dichas transacciones bancarias no pueden conciliarse porque no existen movimientos relacionados en [!INCLUDE[d365fin](includes/d365fin_md.md)]. A continuación, deberá registrar una linea de diario para cada transacción para crear un movimiento relacionado que pueda coincidir.

1. En la ventana **Conciliación banco** seleccione la acción **Transferir al diario general**.  
2. En la ventana **Transf. conciliación al diario**, especifique el diario general que se usará y haga clic en **Aceptar**.

    La ventana **Diario general** se abre una ventana que contiene nuevas líneas del diario para las líneas de extracto bancario con los movimientos que faltan.
3. Complete la línea del diario con la información relevante, como la cuenta de contrapartida. Para obtener más información, consulte [Trabajar con diarios generales](ui-work-general-journals.md).  
4. Seleccione la acción **Registrar**.

    Una vez registrado el movimiento, puede empezar a liquidar la transacción de extracto bancario:
5. Actualice o reabra la ventana **Conciliación banco**. El nuevo movimiento aparecerá en el panel **Movs. bancos**.
6. Concilie la línea del extracto bancario al movimiento de la cuenta manual o automáticamente.

## <a name="see-also"></a>Consulte también
[Administrar cuentas bancarias](bank-manage-bank-accounts.md)  
[Configurar banca](bank-setup-banking.md)  
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

