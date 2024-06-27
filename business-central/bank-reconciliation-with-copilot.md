---
title: Conciliar cuentas bancarias con Copilot (versión preliminar)
description: Aprenda cómo usar Copilot para conciliar cuentas bancarias en Business Central.
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.topic: how-to
ms.collection:
  - get-started
  - bap-ai-copilot
ms.date: 06/13/2024
ms.custom: bap-template
---

# <a name="reconcile-bank-accounts-with-copilot-preview"></a>Conciliar cuentas bancarias con Copilot (versión preliminar)

[!INCLUDE [preview-banner](~/../shared-content/shared/preview-includes/preview-banner.md)]

Este artículo explica cómo la asistencia de conciliación de cuentas bancarias puede ayudarle a conciliar transacciones bancarias con asientos contables en Microsoft Dynamics 365 Business Central.

[!INCLUDE [preview-note](~/../shared-content/shared/preview-includes/production-ready-preview-dynamics365.md)]

## <a name="about-bank-account-reconciliation-assist"></a>Acerca de la asistencia de conciliación de cuentas bancarias

La asistencia para la conciliación de cuentas bancarias es un conjunto de funciones impulsadas por IA que le ayudan a conciliar cuentas bancarias. Ofrece dos tareas distintas a través de Copilot:

- Cotejo mejorado de transacciones con asientos del libro mayor

    Como ya sabrá, el botón **Coincidir automáticamente** en la **Cuenta bancaria. Página de conciliación** que relaciona automáticamente la mayoría de las transacciones bancarias con los asientos de contabilidad. Nos referimos a esta operación como *automatización*. Aunque la coincidencia automática funciona bien, los algoritmos que utiliza a veces pueden dar lugar a muchas transacciones no coincidentes. Copilot utiliza tecnología de inteligencia artificial para inspeccionar esas transacciones sin coincidencia e identificar más coincidencias, según fechas, montos y descripciones. Por ejemplo, si un cliente pagó varias facturas como una suma global, Copilot concilia la línea única del extracto bancario con los múltiples asientos del libro mayor de facturas.

    [Obtenga más información sobre esta tarea](#reconcile-bank-accounts-with-copilot).

- Cuentas contables (G/L) sugeridas

    Para las transacciones bancarias residuales que no pueden cotejarse con ningún asiento de contabilidad, Copilot compara la descripción de la transacción con los nombres de las cuentas del L/M, sugiriendo la cuenta del L/M más probable en la que contabilizar. Por ejemplo, si las transacciones no coincidentes tienen la narrativa *Parada de combustible 24*, Copilot podría sugerirle que las contabilice en la cuenta *Transporte*.

    [Obtenga más información sobre esta tarea](#post-unmatched-bank-transaction-amounts-to-suggested-gl-accounts).

## <a name="available-languages"></a>Idiomas disponibles

[!INCLUDE[bank-recon-assist-language-support](includes/bank-recon-assist-language-support.md)]

## <a name="prerequisites"></a>Requisitos previos

- La asistencia de conciliación de cuentas bancarias está activada. Un administrador debe completar esta tarea. [Obtenga más información sobre cómo configurar las capacidades de Copilot e IA](enable-ai.md).
- Las cuentas bancarias en Business Central que desea conciliar están vinculadas a una cuenta bancaria en línea o configuradas con formato de importación de extracto bancario.
- Está familiarizado con la conciliación de cuentas bancarias en Business Central como se describe en [Conciliar cuentas bancarias](bank-how-reconcile-bank-accounts-separately.md).

## <a name="reconcile-bank-accounts-with-copilot"></a>Conciliar cuentas bancarias con Copilot

<!-- Similar to the **Match Automatically** capability on the **Bank Acc. Reconciliation** page, Bank account reconciliation assist can also automatically matches transactions in banks statements with bank entries. The difference is that **Match Automatically** uses a native rules-based algorithm, while Bank account reconciliation assist is based AI technology though Copilot. Bank account reconciliation assist is intended to supplement the **Match Automatically** capability. While **Match Automatically** is fairly successful at matching transactions, there are some instances where it can't&mdash;which is where Bank account reconciliation assist comes. By using the **Reconcile with Copilot** action on **Bank Acc. Reconciliation** page, you can find even more matches.-->

Copilot en la conciliación de cuentas bancarias está pensado como complemento de la operación de coincidencia automática. Por este motivo, cuando utiliza Copilot, la operación de coincidencia automática se ejecuta primero para realizar las coincidencias iniciales. Luego, Copilot se ejecuta para intentar hacer coincidir las transacciones que la operación de coincidencia automática no manejó.

Puede utilizar dos enfoques para conciliar cuentas bancarias con Copilot:

- Utilice Copilot para iniciar una nueva conciliación en una cuenta bancaria, directamente desde la lista **Conciliación de cuentas bancarias**.
- Utilice Copilot en una conciliación nueva o existente en una cuenta bancaria **Conciliación banco**.

# [En la lista de conciliación de cuentas bancarias](#tab/fromlist)

Para este enfoque, crea y concilia una nueva conciliación de cuenta bancaria desde cero. Este enfoque requiere que seleccione la cuenta bancaria. Si la cuenta bancaria no está vinculada a una cuenta en línea, también debe importar el archivo del extracto bancario.

1. Seleccione el icono ![Bombilla que abre la característica Dígame](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Conciliaciones de cuentas bancarias** y luego seleccione el vínculo relacionado.
1. Seleccione la acción **Conciliar con Copilot** para abrir la ventana **Conciliar con Copilot**.
1. Establezca el campo **Realizar conciliación para esta cuenta bancaria** en la cuenta bancaria que desea conciliar.

    ![Captura de pantalla que muestra la ventana Conciliar con Copilot para reconciliar desde cero.](media/reconcile-bank-accounts-new-copilot.svg)

1. Si la cuenta bancaria seleccionada no está vinculada a una cuenta bancaria en línea, debe importar el archivo del extracto bancario. Para importar el archivo, seleccione el valor en el campo **Utilice datos de transacciones de** o seleccione el botón del clip junto al botón **Generar**. Luego, utilice **Seleccionar el archivo a importar** para importar el archivo del extracto bancario arrastrándolo desde su dispositivo o explorando su dispositivo.
1. Para conciliar con Copilot, seleccione **Generar**.

    Copilot comienza a generar coincidencias propuestas. Cuando se haya completado, la ventana **Conciliar con Copilot** muestra los resultados del proceso de comparación.

1. Revise las coincidencias propuestas como se describe en la siguiente sección.

# [Tarjeta Desde una tarjeta de conciliación de cuenta bancaria](#tab/fromcard)

Para este enfoque, utiliza Copilot en una nueva conciliación de cuenta bancaria que crea manualmente o editando una conciliación existente.

1. Seleccione el icono ![Bombilla que abre la característica Dígame](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Conciliaciones de cuentas bancarias** y luego seleccione el vínculo relacionado.
1. Siga uno de estos pasos:

    - Seleccione **Nuevo** para iniciar una nueva conciliación.
    - Seleccione y abra una conciliación existente en la lista.

1. En la tarjeta **Conciliación de cuentas bancarias**, seleccione **Conciliar con Copilot**.

    ![Captura de pantalla que muestra el botón Conciliar con Copilot en una tarjeta Conciliación banco.](media/bank-reconciliation-copilot-card.svg)

    Copilot comienza a generar coincidencias propuestas. Cuando se haya completado, la ventana **Conciliar con Copilot** muestra los resultados del proceso de comparación.

1. Revise las coincidencias propuestas como se describe en la siguiente sección.
---

### <a name="review-save-or-discard-proposed-matches"></a>Revisar, guardar o descartar coincidencias propuestas

Después de ejecutar Copilot, la ventana **Conciliar con Copilot** muestra los resultados detallados, incluidas las coincidencias propuestas. En este punto, no se ha guardado ninguna coincidencia propuesta por Copilot. Por lo tanto, tiene la oportunidad de inspeccionar las propuestas y guardarlas o descartarlas como desee.

![Captura de pantalla que muestra las coincidencias propuestas en la ventana Conciliar con Copilot.](media/bank-reconciliation-copilot-window.png)

La ventana **Conciliar con Copilot** se divide en dos secciones. La sección superior proporciona algunos detalles generales sobre el resultado. La sección inferior, **Propuestas de coincidencia**, enumera las coincidencias que Copilot ha sugerido.

En la tabla siguiente se describen los campos de la sección superior.

| Campo | Descripción |
|---|---|
| Coincidencia automática | El número de líneas del extracto bancario con las que coincidió la operación de coincidencia automática. Seleccione el valor para ver la tarjeta de conciliación. |
| Coincidencia por Copilot | El número de líneas de extracto bancario para las que Copilot propuso coincidencias. Puedes ver los detalles de los partidos en la sección **Propuestas de coincidencia**. |
| Saldo final extracto | El saldo final que se muestra en el extracto bancario con el que desea hacer la conciliación. |
| Registrar si está totalmente liquidado | Active esta opción si desea publicar automáticamente la conciliación de la cuenta bancaria cuando todas las líneas (100 por ciento) coincidan y haya seleccionado **Mantenerlo**. |

En la sección **Propuestas de coincidencias**, revise las coincidencias propuestas línea por línea. Luego tome las medidas adecuadas:

- Para descartar una única coincidencia propuesta, selecciónela en la lista y luego seleccione **Eliminar línea**.
- Para descartar todas las coincidencias propuestas y cerrar la ventana **Conciliar con Copilot**, seleccione el botón descartar (papelera) ![Botón Descartar.](media/copilot-delete-trash-can.png) junto al botón **Mantenerlo** en la parte inferior de la ventana.
- Para publicar automáticamente la conciliación totalmente coincidente cuando la guarde, active la opción **Publicar si se aplica completamente**.
- Para guardar las coincidencias que se muestran actualmente en la ventana **Conciliar con Copilot**, seleccione **Mantenerlo**.

## <a name="post-unmatched-bank-transaction-amounts-to-suggested-gl-accounts"></a>Registrar transacciones bancarias no coincidentes a cuentas de contabilidad sugeridas

En esta sección, se explica cómo utilizar Copilot para contabilizar importes de líneas de extractos de cuenta bancaria no conciliados (especificados en el campo **Diferencia**) en una cuenta de contabilidad general. Esta tarea solo se puede realizar a partir de una conciliación existente.

1. Vaya a la lista **Conciliaciones de cuentas bancarias** y abra la conciliación existente que incluye las líneas no conciliadas.

    Este paso le proporciona una visión clara de cualquier línea de extracto bancario no conciliada que deba transferirse a la cuenta de contabilidad.

1. En el panel **Líneas de extracto bancario** , identifique el panel de líneas de extracto bancario que no coinciden y seleccione una o más líneas que desee conciliar.

    Copilot se centra en las líneas seleccionadas para registrar nuevos pagos en la cuenta de contabilidad.

1. Seleccione **Registrar diferencia en cuenta contable** para iniciar el proceso.

    ![Captura de pantalla que muestra el botón Registrar diferencia en cuenta contable en la tarjeta Conciliación banco.](media/bank-reconciliation-transfer-gl-copilot-card.png)

    Copilot comienza a generar propuestas para contabilizar los nuevos pagos.

1. Una vez que Copilot haya terminado de generar propuestas, aparece la ventana **Propuestas de Copilot para el registro de diferencias en cuentas de contabilidad**.

    La sección **Propuestas de coincidencia** de esta ventana muestra las propuestas. La experiencia se asemeja a la de reconciliarse con Copilot.

    ![Captura de pantalla que muestra la ventana Propuestas de Copilot para contabilizar diferencias en cuentas de contabilidad.](media/bank-reconciliation-gl-transfer-proposed-matches.png)

1. Revise las propuestas línea por línea para garantizar la exactitud de los pagos sugeridos para su contabilización.

    - Si profundiza en la propuesta seleccionándola en la lista, se le dirigirá a una lista de cuentas. Desde aquí, puede seleccionar otra cuenta. Puede realizar este tipo de corrección manual sólo cuando utilice el flujo **Registrar diferencia en cuenta contable**, no en el flujo coincidente.
    - Si selecciona **Guardar** junto a una propuesta, puede agregar la asignación a la página **Asignación de texto a cuenta**. Luego, la próxima vez que aparezca este texto durante la comparación, se asignará a la cuenta propuesta.

1. Descarte o guarde las propuestas.

    - Para descartar una propuesta específica, selecciónela en la lista y luego seleccione **Eliminar línea**. Para descartar todas las propuestas y cerrar Copilot, seleccione el botón de descartar (papelera) ![botón Descartar.](media/copilot-delete-trash-can.png) junto al botón **Mantenerlo** en la parte inferior de la ventana.
    - Si las propuestas cumplen con sus requisitos y desea guardarlas, seleccione **Mantenerlo**.

         Este paso confirma la transferencia de las propuestas actualmente seleccionadas del libro mayor de la cuenta bancaria a la cuenta de contabilidad. Contabiliza nuevos pagos en las cuentas de contabilidad propuestas y aplica las líneas correspondientes a los asientos del libro mayor de cuentas bancarias resultantes.

## <a name="next-steps"></a>Pasos siguientes

[Validar la conciliación de cuenta bancaria](bank-how-reconcile-bank-accounts-separately.md#validate-your-bank-reconciliation)

## <a name="see-also"></a>Consulte también .

[Solucionar problemas de Copilot y capacidades de IA](ai-copilot-troubleshooting.md)  
[Preguntas frecuentes para IA responsable para asistencia de conciliación bancaria](faqs-bank-reconciliation.md)  
[Configurar banca](bank-setup-banking.md)  
[Conciliar cuentas bancarias](bank-how-reconcile-bank-accounts-separately.md)  
[Liquidación de pagos automáticamente y conciliación de bancos](receivables-apply-payments-auto-reconcile-bank-accounts.md)
