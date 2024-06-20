---
title: Conciliar cuentas bancarias con la asistencia de conciliación
description: Aprenda cómo usar Copilot para conciliar cuentas bancarias en Business Central.
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.topic: how-to
ms.collection:
  - get-started
  - bap-ai-copilot
ms.date: 04/15/2024
ms.custom: bap-template
---

# Conciliar cuentas bancarias con Copilot (versión preliminar)

[!INCLUDE[preview-banner](includes/preview-banner.md)]

Este artículo explica cómo utilizar la asistencia de conciliación de cuentas bancarias para ayudarle a conciliar transacciones bancarias con asientos contables en Business Central.

[!INCLUDE[production-ready-preview-dynamics365](includes/production-ready-preview-dynamics365.md)]

## Acerca de la asistencia de conciliación de cuentas bancarias

La asistencia para la conciliación de cuentas bancarias es un conjunto de funciones impulsadas por IA que le ayudan a conciliar cuentas bancarias. La asistencia de conciliación de cuentas bancarias le ofrece dos tareas distintas a través de Copilot:

- Cotejo mejorado de transacciones con asientos del libro mayor

   Es posible que ya esté familiarizado con la acción **Coincidir automáticamente** en **Cuenta bancaria. Página de conciliación** que relaciona automáticamente la mayoría de las transacciones bancarias con los asientos del libro mayor. Nos referimos a esta operación como *automatización*. Aunque la coincidencia automática funciona bien, los algoritmos que utiliza a veces pueden dar lugar a muchas transacciones no coincidentes. Copilot utiliza tecnología de inteligencia artificial para inspeccionar las transacciones restantes e identificar más coincidencias, según fechas, montos y descripciones. Por ejemplo, si un cliente pagó varias facturas como una suma global, Copilot concilia la línea única del extracto bancario con los múltiples asientos del libro mayor de facturas.

   Vaya a [Conciliar cuentas bancarias con Copilot](#reconcile-bank-accounts-with-copilot).

- Cuentas contables sugeridas

  Para las transacciones bancarias residuales que no pueden cotejarse con ningún asiento del libro mayor, Copilot compara la descripción de la transacción con los nombres de las cuentas del L/M, sugiriendo la cuenta del L/M más probable en la que contabilizar. Por ejemplo, Copilot podría sugerir que las transacciones con la narrativa "Parada de combustible 24" se publiquen en la cuenta "Transporte".
  
   Vaya a [Registrar transacciones bancarias no coincidentes a cuentas del libro mayor sugeridas](#post-unmatched-bank-transaction-amounts-to-suggested-general-ledger-accounts).

## Requisitos previos

- La asistencia de conciliación de cuentas bancarias está activada. Esta tarea la realiza un administrador. [Obtenga más información sobre cómo configurar las capacidades de Copilot e IA](enable-ai.md).
- Las cuentas bancarias en Business Central que desea conciliar están vinculadas a una cuenta bancaria en línea o configuradas con formato de importación de extracto bancario. 
- Está familiarizado con la conciliación de cuentas bancarias en Business Central como se describe en [Conciliar cuentas bancarias](bank-how-reconcile-bank-accounts-separately.md). 

<!--H2s. Required. A how-to article explains how to do a task. The bulk of each H2 should be a procedure.-->
## Conciliar cuentas bancarias con Copilot

<!-- Similar to the **Match Automatically** capability on the **Bank Acc. Reconciliation** page, Bank account reconciliation assist can also automatically matches transactions in banks statements with bank entries. The difference is that **Match Automatically** uses a native rules-based algorithm, while Bank account reconciliation assist is based AI technology though Copilot. Bank account reconciliation assist is intended to supplement the **Match Automatically** capability. While **Match Automatically** is fairly successful at matching transactions, there are some instances where it can't&mdash;which is where Bank account reconciliation assist comes. By using the **Reconcile with Copilot** action on **Bank Acc. Reconciliation** page, you can find even more matches.-->

Copilot en la conciliación de cuentas bancarias está pensado para utilizarse como complemento de la operación de coincidencia automática. Por este motivo, cuando utiliza Copilot, la operación de coincidencia automática se ejecuta primero para realizar las coincidencias iniciales. Luego, Copilot se ejecuta para intentar hacer coincidir las transacciones que la operación de coincidencia automática no manejó.   

Hay dos métodos para conciliar cuentas bancarias con Copilot. Puede utilizar Copilot para iniciar una nueva conciliación en una cuenta bancaria, directamente desde la lista **Conciliación de cuentas bancarias** o puede usar Copilot en una conciliación nueva o existente en la tarjeta **Conciliación de cuenta bancaria**.

# [En la lista de conciliación de cuentas bancarias](#tab/fromlist) 

Con este enfoque, crea y concilia una nueva conciliación de cuenta bancaria desde cero. Este enfoque requiere que seleccione la cuenta bancaria e importe el archivo del extracto bancario, si la cuenta bancaria no está vinculada a una cuenta en línea.

1. Seleccione el icono ![Bombilla que abre la característica Dígame](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Conciliaciones de cuentas bancarias** y luego elija el enlace relacionado. 
1. Seleccione la acción **Conciliar con Copilot** para abrir la ventana **Conciliar con Copilot**.
1. Establezca el campo **Realizar conciliación para esta cuenta bancaria** en la cuenta bancaria que desea conciliar.

   ![Muestra la ventana de conciliación con Copilot para conciliar desde cero](media/reconcile-bank-accounts-new-copilot.svg) 
 
1. Si la cuenta bancaria seleccionada no está vinculada a una cuenta bancaria en línea, debe importar el archivo del extracto bancario. Para importar el archivo, seleccione el valor en el campo **Utilice datos de transacciones de** o seleccione el botón del clip junto al botón **Generar**. Luego, utilice **Seleccionar el archivo a importar** para importar el archivo del extracto bancario arrastrándolo desde su dispositivo o explorando su dispositivo.
1. Para conciliar con Copilot, seleccione **Generar**.

   Copilot comienza a generar coincidencias propuestas. Cuando se completa, la ventana Conciliar con Copilot abre los resultados del proceso de comparación.

1. Revise las coincidencias propuestas como se describe en la siguiente sección.

# [Desde una tarjeta de conciliación de cuenta bancaria](#tab/fromcard) 

Con este enfoque, utiliza Copilot en una nueva conciliación de cuenta bancaria que crea manualmente o editando una conciliación existente. 


1. Seleccione el icono ![Bombilla que abre la característica Dígame](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Conciliaciones de cuentas bancarias** y luego elija el enlace relacionado. 
1. Realice uno de los siguientes pasos:

   - Seleccione **Nuevo** para iniciar una nueva conciliación. 
   - Seleccione y abra una conciliación existente de la lista.
1. En la tarjeta **Conciliación de cuentas bancarias**, seleccione **Conciliar con Copilot**

   ![Muestra la acción de conciliación con copiloto en la cuenta bancaria. tarjeta de reconciliación](media/bank-reconciliation-copilot-card.svg) 

   Copilot comienza a generar coincidencias propuestas. Cuando se completa, la ventana **Conciliar con Copilot** abre los resultados del proceso de comparación. 

1. Revise las coincidencias propuestas como se describe en la siguiente sección. 
---

### Revisar, guardar o descartar coincidencias propuestas

Después de ejecutar Copilot, la ventana **Conciliar con Copilot** muestra los resultados detallados, incluidas las coincidencias propuestas. En este punto, no se han guardado coincidencias propuestas por Copilot, por lo que le brinda la oportunidad de inspeccionar las propuestas y guardarlas o descartarlas como desee.

![Muestra la ventana de conciliación con Copilot con las coincidencias propuestas](media/bank-reconciliation-copilot-window.png) 

La ventana de Copilot se divide en dos secciones. La sección superior proporciona algunos detalles generales sobre el resultado, como se describe en la siguiente tabla.  La sección **Propuesta coincidente** inferior enumera las coincidencias sugeridas por Copilot.

|Campo|Descripción|
|-|-|
|Coincidencia automática|Especifica cuántas líneas del extracto bancario coinciden con la operación de coincidencia automática. Seleccione el valor para ver la tarjeta de conciliación.  |
|Coincidencia por Copilot|Especifica cuántas líneas del extracto bancario tienen coincidencias propuestas por Copilot. Puedes ver los detalles de los partidos en la sección **Partidos propuestos**.|
|Saldo final extracto|Especifica el saldo final que se muestra en el extracto bancario con el que desea hacer la conciliación|
|Registrar si está totalmente liquidado|Active este interruptor si desea publicar automáticamente la conciliación de la cuenta bancaria cuando todas las líneas (100%) coincidan y haya seleccionado **Mantenerlo**.|

#### Guardar o descartar coincidencias propuestas

En la sección **Propuestas coincidentes**, revise las coincidencias sugeridas línea por línea y luego tome la acción adecuada:

- Para descartar una única coincidencia propuesta, selecciónela en la lista y luego seleccione la acción **Eliminar línea**.

- Para descartar todas las coincidencias propuestas y cerrar la ventana de Copilot, seleccione el botón de descartar (papelera) ![Muestra el ícono de la papelera para eliminar todas las propuestas de Copilot para la conciliación de cuentas bancarias](media/copilot-delete-trash-can.png) al lado del botón **Mantenerlo** en la parte inferior de la ventana.

- Para publicar automáticamente la conciliación totalmente coincidente cuando la guarde, active el interruptor **Publicar si se aplica completamente**.  
- Para guardar las coincidencias que se muestran actualmente en la ventana de Copilot, seleccione **Mantenerlo**.

## Registrar transacciones bancarias no coincidentes a cuentas del libro mayor sugeridas

En esta sección, aprenderá a utilizar Copilot para contabilizar importes de líneas de extractos de cuenta bancaria no conciliados (especificados en el campo **Diferencia**) en una cuenta de contabilidad general. Esta tarea sólo se puede realizar a partir de una conciliación existente.

1. Vaya a la lista **Conciliaciones de cuentas bancarias** y abra la conciliación existente que incluye las líneas no conciliadas.

   Comience abriendo una conciliación de cuenta bancaria existente. Este paso le proporciona una visión clara de cualquier línea de extracto bancario no conciliada que deba transferirse a la cuenta del libro mayor.

1. En el panel **Líneas de extracto bancario** , identifique el panel de líneas de extracto bancario que no coinciden y seleccione una o más líneas que desee conciliar.

   Estas líneas son las líneas del extracto en las que se centra Copilot para contabilizar los nuevos pagos en la cuenta del libro mayor.

1. Seleccione **Registrar diferencia en cuenta contable** para iniciar el proceso.

   ![Muestra la acción de transferencia a libro mayor con copilot en la cuenta bancaria. tarjeta de reconciliación](media/bank-reconciliation-transfer-gl-copilot-card.png) 

   Este paso solicita a Copilot que comience a generar propuestas para contabilizar los nuevos pagos.

1. Una vez que Copilot haya terminado de generar propuestas, se abre la ventana **Propuestas de Copilot para el registro de diferencias en cuentas de contabilidad**.

   Esta ventana muestra las propuestas en la sección **Propuesta coincidente**. La experiencia es similar a reconciliarse con Copilot.

   ![Muestra la transferencia al Libro Mayor con la página de coincidencias propuestas por el copiloto para la conciliación de cuentas bancarias](media/bank-reconciliation-gl-transfer-proposed-matches.png) 

1. Revise cada propuesta línea por línea para asegurarse de la exactitud de los pagos sugeridos que deben contabilizarse.

   - Si profundiza en la propuesta seleccionándola en la lista, se le dirigirá a una lista de cuentas. Desde aquí, puedes elegir otra cuenta. Este tipo de corrección manual solo es posible cuando se utiliza el flujo **Registrar diferencia en cuenta contable**, no en el flujo coincidente. 
   - Si selecciona **Guardar...** junto a una propuesta, puede agregar el mapeo a la página **Mapeo de texto a cuenta**, por lo que la próxima vez que aparezca este texto mientras coincide, se asignará a la cuenta propuesta.

1. Descarte o guarde las propuestas.

   - Si desea descartar una propuesta específica, selecciónela en la lista y luego seleccione **Eliminar línea**. Para descartar todas las propuestas y salir de Copilot, seleccione el botón de descartar (papelera) ![Muestra el ícono de la papelera para eliminar todas las propuestas de Copilot para la conciliación de cuentas bancarias](media/copilot-delete-trash-can.png) al lado del botón **Mantenerlo** en la parte inferior de la ventana.

   - Si las propuestas cumplen con sus requisitos y desea guardarlas, seleccione **Mantenerlo**.

      Este paso confirma la transferencia de las propuestas actualmente seleccionadas del libro mayor de la cuenta bancaria a la cuenta del libro mayor. Contabiliza nuevos pagos en las cuentas de mayor propuestas y aplica las líneas correspondientes a los asientos del libro mayor de cuentas bancarias resultantes.

## Pasos siguientes

[Validar la conciliación de cuenta bancaria](bank-how-reconcile-bank-accounts-separately.md#validate-your-bank-reconciliation)  

## Consulte también .
[Solucionar problemas de Copilot y capacidades de IA](ai-copilot-troubleshooting.md)  
[Preguntas frecuentes para IA responsable para asistencia de conciliación bancaria](faqs-bank-reconciliation.md)  
[Configurar banca](bank-setup-banking.md)  
[Conciliar cuentas bancarias](bank-how-reconcile-bank-accounts-separately.md)  
[Liquidación de pagos automáticamente y conciliación de bancos](receivables-apply-payments-auto-reconcile-bank-accounts.md) 
