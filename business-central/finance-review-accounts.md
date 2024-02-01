---
title: Revisar cuentas del libro mayor
description: Puede realizar un seguimiento de su progreso al revisar los importes de las cuentas del libro mayor.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bnielse
ms.topic: conceptual
ms.date: 02/28/2023
ms.custom: bap-template
ms.search.form: '22207,'
ms.service: dynamics-365-business-central
---

# <a name="review-amounts-in-general-ledger-accounts"></a>Revisar importes en cuentas del libro mayor

Es posible que tenga cuentas del libro mayor que vigile con frecuencia. O tal vez desee acelerar el proceso de revisión a fin de mes. Para obtener ayuda con el seguimiento de lo que ha hecho y para acelerar las revisiones, use la acción **Revisar movimientos** en el **Plan de cuentas** o la página **Tarjeta de cuenta de contabilidad general** para cada cuenta. 

## <a name="set-up-accounts-for-reviews"></a>Configurar cuentas para revisiones

En la página **Tarjeta de cuenta de contabilidad general** para cada cuenta, especifique cómo permitir las revisiones en el campo **Directiva de revisión**.

|Revisar directiva  |Descripción  |
|---------|---------|
|Ninguno     | No puede marcar los movimientos de la cuenta como revisados. Por ejemplo, use esta opción para cuentas como proveedores, clientes y de bancos cuando haya otras formas de revisar sus importes.        |
|Permitir revisión     | No tiene que incluir movimientos en una revisión, y las cantidades de los movimientos de débito y crédito no tienen que cuadrar. Elimine una reseña, por ejemplo, si cometió un error.        |
|Permitir revisión y saldo de coincidencia     | Los importes totales de los movimientos de débito y crédito en la revisión deben coincidir. Los campos **Débito** y **Crédito** muestran esos importes, y el campo **Saldo** muestra el total. Esta configuración también le permite eliminar una revisión. Cuando elimina una revisión de uno o más movimientos, los movimientos de débito y crédito aún deben cuadrar.        |

## <a name="mark-entries-as-reviewed"></a>Marcar movimientos como revisados

Elija los movimientos que ha revisado y luego use la acción **Establecer seleccionados como revisados**. Cada vez que marca uno o más movimientos como revisados, los movimientos reciben el mismo número en la columna **Identificador revisado**. El identificador de revisión es una forma práctica de realizar un seguimiento de los movimientos que se revisaron al mismo tiempo. [!INCLUDE [prod_short](includes/prod_short.md)] también registra el usuario que hizo la revisión y cuándo la hizo.

Si marca los movimientos como revisados, pero se arrepiente de hacerlo, use la acción **Establecer seleccionados como no revisados**.

* Si la directiva de revisión permitida está asignada a la cuenta, la acción restablece el identificador revisado a 0 y elimina la persona, la fecha y la hora de la revisión. 
* Si se asigna la directiva de revisar los permitidos y equilibrar el saldo, el crédito y el débito aún deben cuadrar. Por ejemplo, si uno de los movimientos de una revisión es un error, puede elegir otro movimiento con el valor correcto. El movimiento de reemplazo no tiene que tener el mismo identificador revisado.

> [!TIP]
> Una forma rápida de elegir variaos movimientos es mantener presionada la tecla Ctrl o Mayús mientras elige los movimientos. Ctrl le permite seleccionar movimientos específicos y Mayús selecciona todos los movimientos entre el primero y el último que se seleccione.

## <a name="review-accounts-that-have-old-entries"></a>Revisar cuentas que tienen movimientos antiguos

Es posible que tenga movimientos de períodos anteriores que ya revisó o simplemente no necesitan una revisión. Solo desea comenzar a revisar los movimientos desde, por ejemplo, el comienzo del año o el período contable. Puede dejar los movimientos como están. Sin embargo, si desea analizar datos en Excel o mediante el modo de análisis, marque los movimientos como revisados. Para obtener más información sobre análisis de movimientos, vaya a [Analizar movimientos](#analyze-entries). Para marcar los movimientos como revisados, agregue un filtro en el panel Filtro para mostrar solo esos movimientos y luego elija la acción **Marcar los movimientos seleccionados como revisados** .

## <a name="filter-entries"></a>Filtrar movimientos

Para obtener una imagen más clara, hay varias formas de filtrar movimientos en la página **Revisar movimientos de contabilidad general**.

* Use las acciones **Mostrar movimientos revisados** y **Ocultar movimientos revisados** para mostrar solo los movimientos que ha revisado o no. . Para borrar los filtros, utilice la acción **Mostrar todos los movimientos**.
* Use el panel de filtro. Por ejemplo, puede filtrar por número de cuenta o, si tiene movimientos más antiguos y desea marcarlos todos como revisados, por fecha de contabilidad.

## <a name="analyze-entries"></a>Analizar movimientos

Hay un par de formas de analizar los movimientos del libro mayor que ha revisado.

* Active el modo de análisis, por ejemplo, para agrupar los movimientos según su identificador revisado. Para obtener más información sobre el modo de análisis, vaya a [Analizar datos de la página de lista mediante el modo de análisis](analysis-mode.md).
* Exportar los movimientos a Excel.

## <a name="see-also"></a>Consulte también

[Conocer el libro mayor y el plan de cuentas](finance-general-ledger.md)  
[Configurar o cambiar el plan de cuentas](finance-setup-chart-accounts.md)  
