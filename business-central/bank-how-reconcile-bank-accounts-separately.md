---
title: Conciliar bancos| Documentos de Microsoft
description: Describe cómo el valor de inventario se concilia con el libro mayor.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: bank account balance, bank statement
ms.date: 06/19/2020
ms.author: sgroespe
ms.openlocfilehash: 4ccd976829fe1d6e3221964cf9ff97aff1d2c19d
ms.sourcegitcommit: 0c6f4382fad994fb6aea9dcde3b2dc25382c5968
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2020
ms.locfileid: "3484089"
---
# <a name="reconcile-bank-accounts"></a>Conciliar cuentas bancarias

Realiza la conciliación bancaria para asegurarse de que sus diversas transacciones comerciales y gastos se reflejen correctamente en los libros de la empresa. Para ello, compare y haga corresponder los movimientos en sus bancos internos con las transacciones bancarias en su banco, y luego registre los saldos en sus bancos internos para que los totales estén disponibles para los directores financieros. La conciliación bancaria también es una forma práctica de descubrir y resolver pagos faltantes y errores de contabilidad.

A continuación se describe cómo realizar la conciliación bancaria con la página **Conciliación banco**.

> [!TIP]
> También puede conciliar bancos en la página **Diario de conciliación de pagos** en relación con el procesamiento de pagos. Todas las cuenta abiertas relacionada con los movimientos de los clientes o los proveedores se cerrarán cuando seleccione la acción **Registrar pagos y conciliar banco**. Eso significa que la cuenta bancaria se concilia automáticamente por los pagos que registró mediante el diario. Para obtener más información, vea [Liquidación de pagos automáticamente y conciliación de cuentas bancarias](receivables-apply-payments-auto-reconcile-bank-accounts.md).

> [!NOTE]  
> En las versiones de EE. UU., también puede realizar este trabajo en la página **Hoja de trabajo de conciliación bancaria**, que es más adecuada para cheques y depósitos, pero no ofrece importación de archivos de extracto bancario. Para usar esta página en lugar de la página **Conciliación banco**, anule la selección del campo **Reconocimiento banc con auto. coinc.** en la página **Configuración de contabilidad**. Para obtener más información, consulte la sección [Conciliar cuentas bancarias](LocalFunctionality/UnitedStates/how-to-reconcile-bank-accounts.md) en Funcionalidad local para Estados Unidos.

Las líneas de la página **Conciliación banco** se dividen en dos paneles. El panel de **Líneas de extracto bancario** muestra tanto las transacciones bancarias como los movimientos con pagos pendientes. El panel **Movimientos bancarios** muestra los movimientos del banco interno.

La actividad de conciliar transacciones bancarias con movimientos de banco interno se denomina *correspondencia*. Puede realizar la correspondencia automáticamente mediante la función **Conciliar automáticamente**. Alternativamente, puede seleccionar manualmente líneas en ambos paneles para vincular cada línea del extracto bancario a uno o más movimientos de banco relacionados y, a continuación, utilizar la función **Conciliar manualmente**. La casilla de verificación **Liquidado** se selecciona en las líneas en las que los movimientos coinciden. Para obtener más información, consulte [Configurar reglas para la liquidación automática de pagos](receivables-how-set-up-payment-application-rules.md).

> [!NOTE]  
> Si las líneas del extracto de cuenta están relacionadas con los movimientos del cheque, no puede utilizar las funciones de correspondencia. En lugar de eso, debe elegir la acción **Liquidar movs.** y, a continuación, seleccionar el movimiento de cheque correspondiente con el que desea relacionar la línea del extracto de cuenta.

Cuando el valor en el campo **Saldo total** en el panel **Líneas de extracto de cuenta** es igual al valor del campo **Saldo a conciliar** en el panel **Movs. bancos**, puede seleccionar la acción **Registrar**. Los movimientos del libro mayor de banco no coincidentes permanecerán en la página, lo que indica alguna discrepancia que debe resolver para conciliar el banco.

Cualquier línea que no pueda coincidir, indicada por un valor en el campo **Diferencia**, permanecerá en la página **Conciliación banco** después de registrar. Representan algún tipo de discrepancia que debe resolver antes de completar la conciliación de banco. Situaciones comerciales típicas que pueden causar diferencias:

|Diferencia|Motivo|Resolución|
|-|-|
|Una transacción en el banco interno no figura en el extracto de cuenta.|La transacción bancaria no se realizó aunque se realizó un registro en [!INCLUDE[d365fin](includes/d365fin_md.md)].|Realice la transacción de dinero que falta (o solicite a un deudor que la haga) y luego vuelva a importar el archivo de extracto de cuenta o introduzca la transacción manualmente.|
|Una transacción en el extracto de cuenta no existe como documento o línea de diario en [!INCLUDE[d365fin](includes/d365fin_md.md)].|Se realizó una transacción bancaria sin un registro correspondiente en [!INCLUDE[d365fin](includes/d365fin_md.md)], por ejemplo, un registro de línea de diario para un gasto.|Crea y registra el movimiento que falta. Para obtener información sobre una forma rápida de iniciar esto, consulte [Para crear movimientos faltantes para que coincidan con las transacciones bancarias con](bank-how-reconcile-bank-accounts-separately.md#to-create-missing-ledger-entries-to-match-bank-statement-lines-with).|
|Una transacción en el banco interno corresponde a una transacción bancaria, pero cierta información es demasiado diferente para dar una coincidencia.|La información, como el importe o el nombre del cliente, se ingresó de manera diferente en relación con la transacción bancaria o el registro interno.|Revise la información y luego haga coincidir manualmente las dos. De manera opcional, corrija la falta de coincidencia de información.||

Debe resolver las diferencias, por ejemplo, creando movimientos que faltan y corrigiendo información que no coincide, o haciendo transacciones de dinero que faltan, hasta que se complete y se registre la conciliación de banco.

Puede rellenar el panel **Líneas de extracto bancario** en la página **Conciliación banco** de la siguiente manera:

* Automáticamente, utilizando la función **Importar extracto de cuenta** para rellenar el panel **Líneas de los extractos de cuenta** con transacciones bancarias basándose en un archivo importado que proporciona el banco.
* Manualmente, usando la función **Proponer líneas** para rellenar el panel de **Líneas del extracto de cuenta** basándose en las facturas en [!INCLUDE[d365fin](includes/d365fin_md.md)] que tienen pagos pendientes.

## <a name="to-fill-bank-reconciliation-lines-by-importing-a-bank-statement"></a>Para rellenar las líneas de conciliación de bancos importando un extracto bancario

El panel de las **Líneas del extracto de cuenta** completará con las transacciones bancarias de acuerdo con un archivo o secuencia importados proporcionados por el banco.

Para habilitar tanto la importación de extractos bancarios como la fuente de banco, primero debe configurar y habilitar el servicio Envestnet Yodlee Bank Feeds y, a continuación, vincular sus cuentas bancarias a las cuentas bancarias en línea relacionadas. Para obtener más información, vea [Configurar el servicio Envestnet Yodlee Bank Feeds](bank-how-setup-bank-statement-service.md).

1. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), introduzca **Conciliación banco** y luego elija el enlace relacionado.
2. Seleccione la acción **Nuevo**.
3. En el campo **Cód. cuenta banco**, seleccione la cuenta de banco que desee. Los movimientos de cuentas bancarias que existan en la cuenta aparecen en el panel **Movs. bancos**.
4. En el campo **Fecha extracto**, escriba la fecha del extracto del banco.
5. En el campo **Saldo final extracto** escriba el saldo del extracto del banco.
6. Si tiene un archivo de extracto bancario seleccione la acción **Importar extracto bancario**.
7. Busque el archivo y haga clic en el botón **Abrir** para importar las transacciones bancarias en el panel de las **Líneas del extracto de cuenta** en la página **Conciliación banco**.

## <a name="to-fill-bank-reconciliation-lines-with-the-suggest-lines-function"></a>Para rellenar las líneas de conciliación bancarias con la función Proponer líneas

El panel de las **Líneas del extracto de cuenta** se completará de acuerdo con las facturas en [!INCLUDE[d365fin](includes/d365fin_md.md)] que tienen pagos pendientes.  

1. En la página **Conciliación banco** seleccione la acción **Proponer líneas**.
2. En el campo **Fecha inicial** escriba la fecha de registro más antigua para la conciliación de los movimientos.
3. En el campo **Fecha final**, escriba la fecha de registro que se usó por última vez para la conciliación de los movimientos.
4. Seleccione la casilla de verificación **Incluir cheques** para proponer movimientos de cheques en lugar de los movimientos correspondientes de la cuenta.
5. Elija el botón **Aceptar**.

## <a name="to-match-bank-statement-lines-with-bank-account-ledger-entries-automatically"></a>Para conciliar automáticamente las líneas de extracto bancario con movimientos de la cuenta

La página **Conciliación banco** ofrece una funcionalidad de correspondencia automática basada en una coincidencia de texto en una línea del extracto de cuenta (panel izquierdo) con texto en uno o más movimientos de contabilidad (panel derecho). Tenga en cuenta que puede sobrescribir correspondencias automáticas sugeridas y puede optar por no utilizar correspondencia automática. Para obtener más información, consulte [Procedimiento: conciliar las líneas de extracto de cuenta con los movimientos de banco manualmente](bank-how-reconcile-bank-accounts-separately.md#to-match-bank-statement-lines-with-bank-account-ledger-entries-manually).

1. En la página **Conciliación banco** seleccione la acción **Conciliar automáticamente**. La página **Conciliar movimientos** se abre.
2. En el campo **Tolerancia de datos de transacción (días)**, especifique el intervalo de días antes y después de la fecha de registro del movimiento del banco dentro de la cual la función buscará las fechas de transacciones coincidentes en el extracto bancario.

    Si especifica cero o deja el campo en blanco la función **Conciliar automáticamente** buscará solo por las fechas de transacción coincidentes en la fecha de registro de movimientos de la cuenta.
3. Elija el botón **Aceptar**.

    Todas las líneas del extracto bancario y los movimientos la cuenta que pueden coincidir cambian a fuente verde y la casilla **Conciliado** queda seleccionada.
4. Para eliminar un coincidencia seleccione la línea de extracto de cuenta y, a continuación, seleccione la acción **Eliminar conciliación**.

## <a name="to-match-bank-statement-lines-with-bank-account-ledger-entries-manually"></a>Para conciliar manualmente las líneas de extracto bancario con movimientos de la cuenta

1. En la página **Conciliar banco** seleccione una línea no conciliada en el panel **Líneas de extracto bancario**.
2. En el panel **Movs. bancos** seleccione uno o más movimientos de la cuenta que pueden coincidir con la línea del extracto bancario seleccionada. Para elegir varias líneas, mantenga presionada la tecla CTRL.
3. Seleccione la acción **Conciliar manualmente**.

    La línea del extracto de cuenta seleccionada y los movimientos de la cuenta de banco seleccionados cambian a fuente verde, y la casilla **Conciliado** en el panel derecho está seleccionado.
4. Repita los pasos 1 a 3 para todas las líneas del extracto de cuenta que no coinciden.
5. Para eliminar un coincidencia seleccione la línea de extracto de cuenta y, a continuación, seleccione la acción **Eliminar conciliación**.

## <a name="to-create-missing-ledger-entries-to-match-bank-statement-lines-with"></a>Para crear movimientos no existentes para coincidir con las líneas del extracto de cuenta

En ocasiones, un extracto bancario contiene importes por los intereses y recargos cobrados. Dichas líneas del extracto de cuenta no pueden conciliarse porque no existen movimientos relacionados en [!INCLUDE[d365fin](includes/d365fin_md.md)]. A continuación, deberá registrar una linea de diario para cada transacción para crear un movimiento relacionado que pueda coincidir.

1. En la página **Conciliación banco** seleccione la acción **Transferir al diario general**.  
2. En la página **Transf. conciliación al diario**, especifique el diario general que se usará y haga clic en **Aceptar**.

    La página **Diario general** se abre una ventana que contiene nuevas líneas del diario para las líneas de extracto bancario con los movimientos que faltan.
3. Complete la línea del diario con la información relevante, como la cuenta de contrapartida. Para obtener más información, consulte [Trabajar con diarios generales](ui-work-general-journals.md).  
4. Para revisar el resultado del registro antes de registrar, seleccione **Informe de prueba**. Se abre el informe **Estado de cuenta bancaria** y muestra los mismos campos que en el encabezado de la página **Conciliación banco**.
5. Seleccione la acción **Registrar**.

    Una vez registrado el movimiento, puede empezar a liquidar la línea del extracto de cuenta.
6. Actualice o reabra la página **Conciliación banco**. El nuevo movimiento aparecerá en el panel **Movs. bancos**.
7. Concilie la línea del extracto bancario al movimiento de la cuenta manual o automáticamente.

## <a name="see-related-training-at-microsoft-learn"></a>Consulte Formación relacionada en [Microsoft Learn](/learn/modules/bank-reconciliation-dynamics-365-business-central/index)

## <a name="see-also"></a>Consulte también

[Conciliar bancos](bank-manage-bank-accounts.md)  
[Liquidación de pagos automáticamente y conciliación de bancos](receivables-apply-payments-auto-reconcile-bank-accounts.md)  
[Configurar banca](bank-setup-banking.md)  
[Configurar reglas para la liquidación automática de los pagos](receivables-how-set-up-payment-application-rules.md)  
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
