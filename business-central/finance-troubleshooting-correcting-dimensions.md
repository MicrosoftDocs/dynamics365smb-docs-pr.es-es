---
title: Resolución de problemas y corrección de dimensiones
description: Obtenga información sobre cómo solucionar errores de dimensión típicos y cómo corregir las dimensiones después de que se utilicen en transacciones registradas.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'dimension, correction, correct, business intelligence'
ms.search.form: '116, 540, 2588'
ms.date: 04/26/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---

# <a name="troubleshoot-and-correct-dimensions"></a>Resolución de problemas y corrección de dimensiones

Las vistas de análisis e informes financieros a menudo se basan en datos de dimensiones. A pesar de las salvaguardas disponibles, a veces ocurre un error que puede dar lugar a inexactitudes. Este artículo describe algunos de los errores típicos y explica cómo corregir las asignaciones de dimensión en las transacciones registradas para que los informes financieros sean precisos.

## <a name="troubleshooting-dimensions-errors"></a>Solución de errores de dimensiones

Cuando registra documentos o líneas de diario que contienen dimensiones, pueden ocurrir varios errores. Sin embargo, normalmente están relacionados con una configuración o asignación de dimensión incorrecta.

> [!NOTE]
> En la siguiente lista de posibles mensajes de error, los códigos *%X* son marcadores de posición para las variables de datos que el mensaje real contendrá en la interfaz de usuario dependiendo del contexto. Por ejemplo, *%1 %2 está bloqueado.* podría aparecer en la interfaz de usuario como "Código de dimensión ÁREA bloqueado".  

|Problema|Mensaje de error|Solución posible|
|-----|-------------|-----------------|
|Dimensión bloqueada|%1 %2 está bloqueado.|-Busque documentos no registrados que contengan el grupo de dimensiones con la dimensión bloqueada y desbloquéela.<br />-Elimine el grupo de dimensiones para la dimensión bloqueada.|
|Dimensión eliminada|%1 %2 no puede encontrarse.|-Restaure la dimensión que falta.<br />-Busque documentos no registrados que contengan el grupo de dimensiones con la dimensión que falta y agréguela.<br />-Elimine el grupo de dimensiones para la dimensión que falta.|
|Valor de dimensión bloqueada|%1 %2 - %3 está bloqueado.|-Busque documentos no registrados que contengan el grupo de dimensiones con el valor de dimensión bloqueada y desbloquéelo.<br />-Elimine el grupo de dimensiones para el valor de dimensión bloqueada.|
|Valor de dimensión eliminada|    Falta %1 para %2.|-Restaure el valor de dimensión que falta.<br />-Busque documentos no registrados que contengan el grupo de dimensiones con el valor de dimensión que falta y agréguela.<br />-Elimine el grupo de dimensiones para el valor de dimensión que falta.|
|Valor de dimensión no permitido|El tipo de valor de dimensión para %1 %2 - %3 no puede ser %4.|-Cambie el campo **Tipo valor dimensión** en la página **Valores de dimensión** a **Estándar** o **Principio-Total**.<br />-Elimine el grupo de dimensiones para el valor de dimensión bloqueada.|
|Combinación de dimensiones bloqueadas|Las dimensiones %1 y %2 no pueden usarse simultáneamente.|-Busque documentos no registrados que contengan el grupo de dimensiones con la combinación de dimensiones bloqueadas y desbloquéela.<br />-Modifique una de las líneas del conjunto de permisos en conflicto para la combinación de dimensiones.|
|Combinación de valores de dimensiones bloqueadas|Las combinaciones de dimensiones %1 - %2 y %3 - %4 no pueden utilizarse simultáneamente.|-Busque documentos no registrados que contengan el grupo de dimensiones con la combinación de valores de dimensiones bloqueadas y desbloquéela.<br />-Modifique una de las líneas del conjunto de permisos en conflicto para la combinación de valores de dimensiones.|
|Código de valor de dimensión en blanco para la dimensión predeterminada cuando el campo **Registro valor** contiene **Código Obligatorio**|- Seleccione un %1 para el %2 %3.<br />- Seleccione un %1 para el %2 %3 para %4 %5.|-Cambie el campo **Registro valor** en la página **Dimensión predeterminada**.<br />-Introduzca un valor de dimensión no vacío para la dimensión en conflicto en el grupo de dimensiones.|
|Código de valor de dimensión erróneo para la dimensión predeterminada cuando el campo **Registro valor** contiene **Igual código**|- Seleccione %1 %2 para el %3 %4.<br />- Seleccione %1 %2 para el %3 %4 para %5 %6.|-Cambie el campo **Registro valor** en la página **Dimensión predeterminada**.<br />-Introduzca un valor de dimensión requerido para la dimensión en conflicto en el grupo de dimensiones.|
|Código de valor de dimensión no vacío para la dimensión predeterminada en blanco cuando el campo **Registro valor** contiene **Igual código**|-%1 %2 debe estar en blanco.<br />-%1 %2 debe estar en blanco para %3 %4.|-Cambie el campo **Registro valor** en la página **Dimensión predeterminada**.<br />-Introduzca un código de valor de dimensión en blanco para la dimensión en conflicto en el grupo de dimensiones.|
|Valor de dimensión inesperado para la dimensión predeterminada cuando el campo **Registro valor** contiene **Sin código**|-%1 %2 no debe ser mencionado.<br />-%1 %2 no debe ser mencionado para %3 %4|-Cambie el campo **Registro valor** en la página **Dimensión predeterminada**.<br />-Elimine la línea conflictiva del grupo de dimensiones.|
|Una corrección de dimensión no se completa correctamente.||-Elija **Restablecer** para revertir la corrección a un estado de borrador. Esto restablece los cambios y puede ejecutar de nuevo la corrección.|

## <a name="changing-dimension-assignments-after-posting"></a>Cambio de asignaciones de dimensión después del registro

Si descubre una dimensión incorrecta en los movimientos de contabilidad, puede corregir los valores de dimensión y actualizar sus vistas de análisis. La corrección ayuda a que sus informes y análisis financieros sean precisos.

> [!IMPORTANT]
> Las funciones para corregir dimensiones están destinadas únicamente a ayudar a que los informes financieros sean precisos. Las correcciones de dimensión se aplican solo a las entradas de movimientos. No cambian las dimensiones asignadas a los asientos en otros libros mayores para la misma transacción. Habrá una discrepancia entre las dimensiones asignadas en el libro mayor y los libros secundarios.

### <a name="set-up-dimension-corrections"></a>Configuración de correcciones de dimensión

Hay dos cosas a tener en cuenta al configurar correcciones de dimensión:

* ¿Hay dimensiones que no desea que la gente cambie? En la página **Configuración de corrección de dimensión**, especifique las dimensiones que desea bloquear para cambios.
* ¿Quién puede cambiar dimensiones? Para permitir que las personas realicen cambios, asigne el permiso **CORRECCIÓN DIM. D365** a los usuarios. Los permisos les permiten crear correcciones de dimensión, ejecutarlas y deshacerlas si es necesario. También pueden especificar dimensiones bloqueadas. Para obtener más información, consulte [Asignar permisos a usuarios y grupos](ui-define-granular-permissions.md). 

### <a name="correct-a-dimension"></a>Corrección de una dimensión

Puede seleccionar manualmente uno o varios movimientos de contabilidad o usar filtros para seleccionar conjuntos de movimientos. Si es necesario, también puede agregar o eliminar dimensiones. 

1. Para iniciar una corrección de dimensión, use una de las siguientes páginas:

    * En la página **Registro contabilidad**, seleccionando un registro y luego eligiendo la acción **Corregir dimensiones**. Esta acción inicia una corrección para los movimientos en el registro seleccionado.
    * En la página **Movs. contabilidad**, eligiendo la acción **Corrección de dimensión**. 

2. En el campo **Descripción**, introduzca cualquier información sobre el cambio. Otras personas pueden usar esta información más adelante para comprender lo que se hizo.
3. En la ficha desplegable **Movimientos seleccionados**, elija los movimientos pertinentes.

    > [!IMPORTANT]
    > Cuando cambia una selección, se restablecen los valores de la ficha desplegable **Cambios de corrección de dimensión**. Por lo tanto, seleccione siempre los movimientos antes de especificar cambios en el valor de dimensión.

   La siguiente tabla describe las opciones.

   |Opción  |Descripción  |
   |---------|---------|
   |Agregar movimientos relacionados     |Agregue movimientos contables que estén en el mismo registro de movimientos de contabilidad.|   
   |Agregar por filtro     |Use criterios de filtros cuando agregue movimientos de contabilidad.|
   |Selección manual     |Seleccione movimientos de contabilidad específicos.         |
   |Agregar por dimensiones     |Filtre movimientos de contabilidad por dimensiones.         |
   |Quitar movimientos     |Anule la selección de movimientos de contabilidad.         |
   |Administrar criterios de selección     |Realice un seguimiento del proceso de selección y deshaga las selecciones si es necesario.         |

4. En la ficha desplegable **Cambios de corrección de dimensión**, elija la dimensión que desea cambiar en el campo **Código de dimensión** y el nuevo valor en el campo **Nuevo código de valor de dimensión**.
5. Para validar la corrección, elija **Validar cambios de dimensión**. Para obtener más información, consulte [Validación de correcciones de dimensión](finance-troubleshooting-correcting-dimensions.md#validating-dimension-corrections).
6. Elija **Ejecutar**.

### <a name="validate-dimension-corrections"></a>Validación de correcciones de dimensión

Antes de ejecutar una corrección, es una buena idea validarla primero. La validación comprueba las restricciones sobre el valor al registrar para las cuentas de contabilidad, las restricciones para las dimensiones y si los valores de las dimensiones están bloqueados. Durante la validación, el estado de la corrección se establece en **Validación en proceso**. Después de validar una corrección, el resultado se muestra en el campo **Estado de validación**. Si se encontraron errores, puede usar la acción **Ver errores** para investigarlos. Después de corregir un error, debe usar la acción **Reabrir** para ejecutar la corrección o una nueva validación.

Puede ejecutar una corrección inmediatamente o programarla para que se ejecute más adelante. Si está ejecutando correcciones en un conjunto de datos grande, le recomendamos que lo programe para que se ejecute fuera del horario comercial. Para obtener más información, consulte [Correcciones de dimensión en grandes conjuntos de datos](finance-troubleshooting-correcting-dimensions.md#dimension-corrections-on-large-data-sets).

### <a name="undo-a-correction"></a>Deshacer una corrección

Después de corregir una dimensión, si no le gusta lo que ve, puede usar la acción **Deshacer** para restablecer el valor anterior. Sin embargo, solo puede deshacer la corrección más reciente. Antes de deshacer una corrección, puede validar los cambios resultantes de la acción de deshacer. Por ejemplo, la validación resulta útil si las restricciones de dimensión han cambiado después de que se realizase la corrección.

Si la acción Deshacer no está disponible, por ejemplo, porque ha realizado muchas correcciones, puede usar la acción **Copiar a borrador** para iniciar una nueva corrección para las mismas entradas.

### <a name="dimension-corrections-on-large-data-sets"></a>Correcciones de dimensión en grandes conjuntos de datos

Tenga cuidado al corregir grandes conjuntos de entradas, por ejemplo, conjuntos que incluyan más de 10 000 entradas. Si puede, le recomendamos que use los filtros para ejecutar las correcciones en conjuntos de datos más pequeños. También es una buena idea realizar correcciones fuera del horario comercial habitual. 

### <a name="use-analysis-views-with-dimension-corrections"></a>Usar vistas de análisis con correcciones de dimensión

Si **Actualizar al registrar** está habilitado para una vista de análisis, [!INCLUDE[prod_short](includes/prod_short.md)] puede actualizar la vista cuando se registran los documentos y diarios. También puede actualizar las vistas con esta configuración habilitada con los resultados de las correcciones de dimensión. Para ello, active el control de alternancia **Actualizar vistas de análisis**. La actualización de las vistas de análisis puede afectar al rendimiento, especialmente para grandes conjuntos de datos, por lo que le recomendamos que actualice las vistas de análisis solo para conjuntos de datos pequeños.  

### <a name="view-historical-dimension-corrections"></a>Visualización de correcciones de dimensión históricas

Si se ha corregido un movimiento de contabilidad, puede investigar el cambio usando la acción **Historial de correcciones de dimensión**.

### <a name="handle-incomplete-corrections"></a>Gestión de correcciones incompletas

Si una corrección no se completa, aparecerá una advertencia en la ficha de corrección. Si eso sucede, puede usar la acción **Restablecer** para revertir la corrección a un estado de borrador y deshacer los cambios. A continuación, puede volver a ejecutar la corrección.

> [!NOTE]
> Restablecer una corrección incompleta no afectará a las actualizaciones de las vistas de análisis porque se producen al final del proceso de corrección.

### <a name="use-cost-accounting-with-corrected-gl-entries"></a>Usar la contabilidad de costes con movimientos de contabilidad corregidos

Después de corregir las dimensiones, sus datos para la contabilidad de costes no estarán sincronizados. La contabilidad de costes usa dimensiones para agregar cantidades para centros de coste y objetos de coste, y para ejecutar asignaciones de costes. Cambiar las dimensiones para movimientos de contabilidad probablemente signifique volver a ejecutar sus modelos de contabilidad de costes. Dependiendo de los datos que se actualizaron y de cómo estén configuradas sus capacidades de contabilidad de costes, es posible que necesite:

* Eliminar solo algunos registros de costes y volver a ejecutar las asignaciones.
* Eliminar todo y volver a ejecutar todos sus modelos.

Debe identificar manualmente dónde afectarán las correcciones de dimensión a la contabilidad de costes y dónde se necesitan actualizaciones. [!INCLUDE[prod_short](includes/prod_short.md)] no ofrece actualmente una forma automatizada de hacerlo.

## <a name="see-also"></a>Consulte también

[Trabajar con dimensiones](finance-dimensions.md)  
[Analizar datos por dimensiones](bi-how-analyze-data-dimension.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
