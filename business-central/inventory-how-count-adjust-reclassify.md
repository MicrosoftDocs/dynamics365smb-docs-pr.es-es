---
title: Recuento, ajuste y reclasificación de inventario | Documentos de Microsoft
description: Describe cómo realizar recuento físico, hacer ajustes negativos o positivos y cómo cambiar la información, como la ubicación o el número de lote, en las entradas de los movimientos o del almacén.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: adjustment, negative, positive, increase, decrease
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: d8a9ba2f4fc819c1da515a0ace7d8641ec54ffc6
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 03/31/2019
ms.locfileid: "929410"
---
# <a name="count-adjust-and-reclassify-inventory-using-journals"></a>Recuento, ajuste y reclasificación de inventario con diarios
Como mínimo una vez cada año fiscal, debe realizar un inventario físico (es decir, contar todos los productos del inventario) para ver si la cantidad registrada en la base de datos es la misma que la cantidad física real en los almacenes. Una vez se sepa la cantidad física, debe registrarse en la contabilidad como parte de la evaluación del inventario de final de periodo.

Aunque cuente todos los productos del inventario una vez al año, puede que haya decidido contar algunos productos con mayor frecuencia, quizás porque son más valiosos o porque se fluctúan muy rápido y forman una gran parte del negocio. Con este fin, puede asignar períodos de recuento especiales a esos elementos. Para obtener más información, consulte [Realizar el recuento cíclico](inventory-how-count-adjust-reclassify.md#to-perform-cycle-counting).

Si es necesario ajustar las cantidades de inventario registradas, por motivos de recuento u otros, puede usar un diario de productos para cambiar las entradas de contabilidad del inventario sin registrar las transacciones de negocio. Como alternativa, puede ajustar un solo artículo en la tarjeta de artículo.

Si necesita cambiar los atributos de las entradas de contabilidad de los productos, puede usar el diario de reclasificación de productos. Los atributos típicos para reclasificar incluyen dimensiones y códigos de campaña, aunque también realiza el "transferencias del sistema" mediante la reclasificación de códigos de ubicación y de almacén. Se aplican pasos especiales cuando desea reclasificar números de serie o de lote, y sus fechas de caducidad. Para obtener más información, consulte [Trabajar con números de serie y de lote](inventory-how-work-item-tracking.md).

> [!NOTE]
> En configuraciones avanzadas de almacén, los elementos se registran en las ubicaciones como movimientos de almacén, no como movimientos de productos. Por lo tanto, realice el recuento, el ajuste y la reclasificación en diarios especiales de almacén que soportan ubicaciones. A continuación, utilice funciones especiales para sincronizar las entradas de almacén nuevas o modificadas con sus movimientos de productos relacionados para reflejar los cambios en las cantidades y valores de inventario. Esto se describe en los procedimientos específicos que se muestran a continuación cuando es relevante.

## <a name="to-perform-a-physical-inventory"></a>Realizar un inventario físico
Es necesario llevar un inventario físico, es decir, hacer un recuento de los productos reales disponibles, para comprobar que la cantidad registrada coincida con la cantidad física en stock al final del ejercicio, o con mayor frecuencia. Si existen diferencias, debe registrarlas en las cuentas de producto antes de realizar la valoración de las existencias.

> [!NOTE]
> Este procedimiento describe cómo realizar un inventario utilizando un diario, la página **Diario inventario físico**. También puede realizar la tarea utilizando documentos, las páginas **Pedido de inventario físico** y **Registro de inventario físico**, que proporcionan más control y asistencia para distribuir el recuento a varios empleados. Para obtener más información, consulte [Contar inventario mediante documentos](inventory-how-count-inventory-with-documents.md).<br /><br />
> Tenga en cuenta que la funcionalidad basada en documentos no se puede utilizar para contar productos en ubicaciones, movimientos de almacén.

Aparte de la tarea de recuento físico, el proceso completo implica las tres tareas siguientes:

- Calcular el inventario previsto.
- Imprimir el informe que va utilizar para el recuento.
- Introducir y registrar el inventario contado real.

Puede realizar el inventario físico en cualquiera de las siguientes formas en función de la configuración de almacén. Para obtener más información, consulte [Configuración de la administración de almacén](warehouse-setup-warehouse.md).  

-   Si el almacén no utiliza ubicación y picking directos (configuración básica de almacén), utilice la página **Diario de inventario físico** del menú de **Existencias** y siga el procedimiento que es muy parecido al del inventario físico sin recuento cíclico.  
-   Si la ubicación utiliza ubicación y picking directos (configuración avanzada de almacén), utilice en primer lugar la página **Almacén. Fís. Invent. diario** y, a continuación, la página **Diario del artículo** para ejecutar la función **Calcular ajuste almacén**.

### <a name="to-calculate-the-expected-inventory-in-basic-warehouse-configurations"></a>Para calcular el inventario esperado en las configuraciones básicas del almacén
1. Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Diarios de inventario** y luego elija el enlace relacionado.
2. Elija la acción **Calcular inventario**.
3. En la página **Calcular inventario**, especifique las condiciones que desea utilizar para crear las líneas de diario, como si desea incluir los productos que tienen un inventario registrado de cero.
4. Establezca filtros si solo desea calcular el inventario para productos, ubicaciones, almacenes o dimensiones determinados.
5. Elija el botón **Aceptar**.

> [!NOTE]  
>   Se procesan los movimientos de producto según los datos especificados y se crean las líneas en el diario de inventario físico. Tenga en cuenta que el campo **Cdad. (stock físico)** se rellena automáticamente con la misma cantidad que figura en el campo **Stock calculado**. Con esta función, no hace falta que especifique el recuento de existencias disponibles para productos cuya cantidad coincida con el stock calculado. Sin embargo, si la cantidad contada difiere de lo que se especifica en el campo **Stock calculado**, debe sobregrabarlo con la cantidad contada realmente.

### <a name="to-calculate-the-expected-inventory-in-advanced-warehouse-configurations"></a>Para calcular el inventario esperado en las configuraciones avanzadas del almacén
1.  Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Diario de producto** y elija el enlace relacionado.  
2.  Seleccione la acción **Calcular ajuste almacén**.  
3.  Rellene la página del trabajo por lotes con los números de productos que desea contar y con el almacén.
4. Elija el botón **Aceptar** y registre los ajustes, si los hay.

    Si no hace esto antes de realizar el inventario físico de almacén, el resultado de registrar el diario del inventario físico y del diario de productos de la segunda parte del proceso será el resultado del inventario físico combinado con otros ajustes de almacén para los productos que se han contado.  
5.  Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Diario inv. físico alm.** y luego elija el enlace relacionado.  
6. Elija la acción **Calcular inventario**. Se abrirá la página de solicitud del trabajo por lotes **Calcular existencias alm.**  
7.  Defina los filtros para limitar los productos que se contarán en el diario y, a continuación, seleccione **Aceptar**.

    El programa crea una línea para cada ubicación que cumpla los requisitos del filtro. En este momento puede eliminar algunas líneas, pero si desea registrar el resultado como un inventario físico, debe contar el producto en todas las ubicaciones.  

     Si sólo tiene tiempo para contar las existencias del producto en algunas ubicaciones, pero no en todas, puede encontrar diferencias y registrarlas posteriormente en el diario de productos con la función **Calcular ajuste almacén**.  
8.  Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Lista invent. fís. alm.** y luego elija el enlace relacionado.  
9.  Abra la página de solicitud de informes e imprima las listas en las que desea que los empleados registren la cantidad de productos que han contado en cada ubicación.  
10. Una vez realizado el recuento, introduzca las cantidades contadas en el campo **Cdad. (stock físico)** en el diario de inventario físico de almacén.  

    > [!NOTE]  
    >  En el diario de inventario físico de almacén, el campo de **Cdad. (Calculado)** se rellena automáticamente a partir de los registros de la ubicación de almacén y copia estas cantidades al campo **Cdad. (física)** en cada línea. Si la cantidad contada por el empleado de almacén se diferencia de lo que el programa ha introducido en el campo Cdad. (física), debe introducir la cantidad contada realmente.  

11. Cuando haya introducido todas las cantidades contadas, elija la acción **Registrar**.  

    Al registrar el diario, el programa crea dos movimientos de almacén en el registro por cada línea que se ha contado y registrado:  

    -   Si la cantidad calculada y la cantidad física son distintas, se registra una cantidad negativa o positiva en la ubicación y se registra una cantidad de contrapartida en la ubicación de ajuste del almacén.  
    -   Si la cantidad calculada es igual que la cantidad física, el programa registra un movimiento de 0 en la ubicación y en la ubicación de ajuste. Los movimientos se registran en la fecha en que se ha realizado el inventario físico de almacén y no existen diferencias en las existencias del producto.  

Al registrar el inventario físico de almacén, no se registra el diario de productos, el diario de inventario físico o el movimiento de valoración, si no que los registros se colocan ahí para una conciliación inmediata cuando sea necesario. No obstante, si desea mantener registros exactos de lo que sucede en el almacén y ha contado todas las ubicaciones donde estaban registrados los productos, debe registrar inmediatamente el resultado del almacén como un inventario físico en existencias. Para obtener más información, consulte [Para introducir y registrar el inventario contado real en configuraciones avanzadas de almacén](inventory-how-count-adjust-reclassify.md#to-enter-and-post-the-actual-counted-inventory-in-advanced-warehouse-configurations).

### <a name="to-print-the-report-to-be-used-when-counting"></a>Para imprimir el informe que va utilizar para el recuento
1. En la página **Diario inventario físico** que contiene el inventario previsto calculado, elija la acción **Imprimir**.
2. En la página **Lista inventario físico**, especifique si el informe debe mostrar el stock calculado y si el informe debe indicar los productos de inventario por números de serie o lote.
3. Establezca filtros si solo desea imprimir el informe para productos, ubicaciones, almacenes o dimensiones determinados.
4. Elija el botón **Imprimir**.

Los empleados pueden ahora proceder a contar el inventario y registrar las discrepancias en el informe impreso.

### <a name="to-enter-and-post-the-actual-counted-inventory-in-basic-warehouse-configurations"></a>Para introducir y registrar el inventario contado real en configuraciones básicas de almacén
1. En cada línea de la página **Diario inventario físico**, donde el inventario real disponible, según lo determinado por el recuento físico, difiere de la cantidad calculada, introduzca el inventario real disponible en el campo **Cdad. (stock físico)**.

    Los campos relacionados se actualizan según corresponda.

    > [!NOTE]  
    >   Si el recuento físico revela diferencias, producidas por productos que se registraron con códigos de almacén incorrectos, no introduzca las diferencias en el diario de inventario físico. En su lugar, utilice el diario de reclasificación o un pedido de transferencia para redirigir los productos a los almacenes correctos. Para obtener más información, consulte Diario recl. prod. o Creación de pedidos de transferencia.

2. Para ajustar las cantidades calculadas a las cantidades contadas reales, elija la acción **Registrar**.

    Se crean los movimientos de producto y los movimientos del inventario físico. Abra la ficha del producto para ver los movimientos del inventario físico resultantes.

3. Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Productos** y luego elija el enlace relacionado.
4. Para verificar el recuento del inventario, abra la ficha del producto en cuestión y, a continuación, elija la acción **Movimientos del inventario físico**.

### <a name="to-enter-and-post-the-actual-counted-inventory-in-advanced-warehouse-configurations"></a>Para introducir y registrar el inventario contado real en configuraciones avanzadas de almacén

1.  Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Diario de producto** y elija el enlace relacionado.  
2.  Seleccione la acción **Calcular ajuste almacén**.  
3.  Seleccione los mismos artículos que ha contado en el inventario físico de recuento cíclico que acaba de realizar, y los demás artículos que requieran ajuste y, a continuación, seleccione el botón **Aceptar**.  

     Se abrirá la página **Diario inventario** y las líneas creadas para estos artículos. Tenga en cuenta que las cantidades neta que acaba de contar y registrar ubicación por ubicación están ahora listas para consolidarlas y para sincronizarlas como movimientos de producto.  

4.  Registre el diario sin cambiar las cantidades.  

Las cantidades del diario de productos (movimientos de producto) y las cantidades del almacén (movimientos de almacén) son de nuevo las mismas para estos productos y el sistema ha actualizado la última fecha de recuento del producto o unidad de almacenamiento.  

## <a name="to-perform-cycle-counting"></a>Realizar el recuento cíclico
Aunque cuente todos los productos del inventario una vez al año, puede que haya decidido contar algunos productos con mayor frecuencia, quizás porque son más valiosos o porque se fluctúan muy rápido y forman una gran parte del negocio. Con este fin, puede asignar períodos de recuento especiales a esos elementos.

Puede realizar el recuento cíclico en cualquiera de las siguientes formas en función de la configuración de almacén. Para obtener más información, consulte [Configuración de la administración de almacén](warehouse-setup-warehouse.md).  

-   Si el almacén no utiliza ubicación y picking directos (configuración básica de almacén), utilice la página **Diario de inventario físico** del menú de **Existencias** y siga el procedimiento que es muy parecido al del inventario físico sin recuento cíclico.  
-   Si la ubicación utiliza ubicación y picking directos (configuración avanzada de almacén), utilice en primer lugar la página **Almacén. Fís. Invent. diario** y, a continuación, la página **Diario del artículo** para ejecutar la función **Calcular ajuste almacén**.  

### <a name="to-set-up-counting-periods"></a>Para configurar periodos de recuento
El inventario físico se realiza normalmente en intervalos de tiempo periódicos, por ejemplo, mensualmente, trimestralmente o anualmente. Puede definir los periodos de recuento de inventario necesario.

Configure los periodos de recuento de inventario que desee utilizar y, a continuación, asigne uno a cada producto. Al realizar un inventario físico y utilizar **Calcular periodo recuento** en el diario de inventario físico, las líneas de los elementos se crean automáticamente.

1. Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Períodos recuento inv. fís.** y luego elija el enlace relacionado.  
2. Rellene los campos según sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

### <a name="to-assign-a-counting-period-to-an-item"></a>Asignar un periodo de recuento a un producto  
1. Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Productos** y luego elija el enlace relacionado.  
2. Seleccione el producto al que desea asignar un periodo de recuento.  
3. En el campo **Cód. perio. recuento inv. fís.**, seleccione el periodo de recuento correspondiente.  
4. Elija el botón **Sí** para cambiar el código y para calcular el primer periodo de recuento del artículo. La próxima vez que seleccione calcular un periodo de recuento en el diario de inventario físico, el producto aparecerá como una línea en la página **Selección prod. invent. fís.** Ya puede empezar a contar el producto periódicamente.

### <a name="to-initiate-a-count-based-on-counting-periods-in-basic-warehouse-configurations"></a>Para iniciar un recuento basándose en periodos de recuento en las configuraciones básicas de almacén
1. Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Diario de inventario** y luego elija el enlace relacionado.
2. Elija la acción **Calcular periodo de recuento**.

    Se abrirá la página **Selección prod. invent. fís.** y mostrará los productos para los que se han asignado los periodos de recuento que es necesario contar, según sus periodos de recuento.
3. Realizar un inventario físico. Para obtener más información, consulte [Para ejecutar un inventario físico](inventory-how-count-adjust-reclassify.md#to-perform-a-physical-inventory).

### <a name="to-initiate-a-count-based-on-counting-periods-in-advanced-warehouse-configurations"></a>Para iniciar un recuento basándose en periodos de recuento en las configuraciones avanzadas de almacén
1.  Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Diario inv. físico alm.** y luego elija el enlace relacionado.  
2. Elija la acción **Calcular periodo de recuento**.

    Se abrirá la página **Selección prod. invent. fís.** y mostrará los productos para los que se han asignado los periodos de recuento que es necesario contar, según sus periodos de recuento.
3. Realizar un inventario físico. Para obtener más información, consulte [Para ejecutar un inventario físico](inventory-how-count-adjust-reclassify.md#to-perform-a-physical-inventory).  

    > [!NOTE]  
    >  Debe contar el artículo en todas las ubicaciones que contengan el artículo determinado. Si se eliminan algunas de las líneas de la ubicación que el programa ha recuperado para contar en la página **Almacén. fís. inventario**, no contará todos los artículos en el almacén. Si realiza un registro posterior por resultados incompletos en Diario inventario fís., las cantidades registradas serán incorrectas.  

## <a name="to-adjust-the-inventory-of-one-item"></a>Ajustar el inventario de un producto
Una vez realizado un recuento físico de un productos en el área de inventario, puede utilizar la función **Ajustar inventario** para registrar la cantidad real del inventario.

1. Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Productos** y luego elija el enlace relacionado.
2. Seleccione el producto para el que quiere ajustar el inventario y, a continuación, elija la acción **Ajustar inventario**.
3. En el campo **Nuevo inventario**, escriba la cantidad de inventario que desea registrar para el producto.
4. Elija el botón **Aceptar**.

El inventario de producto ahora está ajustado. La nueva cantidad se muestra en el campo **Inventario actual** en la página **Ajustar inventario** y en el campo **Inventario** de la página **Ficha de producto**.

También puede usar la función **Ajustar inventario** como una manera sencilla de incluir los productos comprados en el inventario si no usa facturas o pedidos de compra para registrar las compras. Para obtener más información, consulte [Registrar compras](purchasing-how-record-purchases.md).

> [!NOTE]  
>   Una vez que haya ajustado el inventario, debe actualizarlo con el valor calculado actual. Para obtener más información, vea [Revaluación de inventario](inventory-how-revalue-inventory.md).

### <a name="to-adjust-the-inventory-quantity-of-multiple-items-in-basic-warehouse-configurations"></a>Para ajustar la cantidad de inventario de varios productos en configuraciones básicas de almacén
En la página **Diario productos**, puede publicar transacciones de artículos directamente para ajustar el inventario en relación con compras, ventas y ajustes positivos o negativos sin utilizar documentos.

Si utiliza con frecuencia el diario de productos para registrar líneas de diario iguales o parecidas, por ejemplo, relacionadas con el consumo de materiales, puede utilizar la página **Diario productos estándar** para hacer más fácil este trabajo repetitivo. Para obtener más información, consulte [Trabajar con diarios estándar](ui-work-general-journals.md#working-with-standard-journals).

1. Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Diarios de producto** y luego elija el enlace relacionado.
2. Rellene los campos según sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Seleccione la acción **Registrar** para realizar ajustes de inventario.

> [!NOTE]  
>   Una vez que haya ajustado el inventario, debe actualizarlo con el valor calculado actual. Para obtener más información, vea [Revaluación de inventario](inventory-how-revalue-inventory.md).

### <a name="to-adjust-bin-quantities-in-advanced-warehouse-configurations"></a>Para ajustar las cantidades de la ubicación de configuraciones avanzadas de almacén  
Si su almacén utiliza ubicación y picking directo, utilice el **Diario producto almacén** para registrar, fuera del contexto del inventario físico, todos los ajustes positivos y negativos en la cantidad de productos que sabe que son entradas reales, tales como productos registrados anteriormente como que faltaban que han aparecido inesperadamente, o salidas reales, como la rotura de productos frágiles.  

A diferencia de los ajustes de registro en el diario del artículo de inventario, el uso del diario del artículo de almacén le ofrece un nivel adicional de ajuste que hace que los registros de la cantidad sean aún más exactos siempre. El almacén tiene siempre un registro completo de los artículos que están disponibles y de cuales están almacenados, pero cada registro de ajuste no se registra inmediatamente en el libro mayor del artículo. En el proceso de registro, los créditos o se realizan en la ubicación real con el ajuste de cantidad, y se realiza un movimiento de contrapartida en una ubicación de ajuste, una ubicación virtual sin los artículos reales. Esta ubicación se define en **Cód. ubicación ajuste inventario** en la ficha de almacén.

1.  Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Diario producto almacén** y luego elija el enlace relacionado.  
2.  Rellene la información de la cabecera.  
3.  Rellene el campo **Nº producto** de la línea.  
4.  Introduzca la ubicación en la que va a colocar los productos adicionales o donde ha encontrado los productos que faltan.  
5.  Rellene la cantidad que ha observado como diferencia en el campo **Cantidad**. Si ha encontrado más productos, introduzca una cantidad positiva. Si faltan productos, introduzca una cantidad negativa.  
6.  Elija la acción **Registrar**.

## <a name="to-synchronize-the-adjusted-warehouse-entries-with-the-related-item-ledger-entries"></a>Para sincronizar los movimientos ajustados de almacén con los correspondientes movimientos de producto
En los intervalos adecuados definidos por la política de la empresa, debe registrar los ajustes de ubicaciones de almacén en el diario de productos. Algunas empresas encuentran correcto registrar ajustes en el diario de productos diariamente, mientras que para otras es más conveniente conciliar con frecuencia. 

1.  Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Diario de producto** y luego elija el enlace relacionado.  
2.  Rellene los campos de cada línea del diario.  
3.  Elija la acción **Calcular ajuste almacén**, y rellene los filtros como corresponda en la página de la solicitud del trabajo por lotes. Los ajustes se calculan sólo para las entradas en la ubicación de ajuste que cumplen unos requisitos de filtro.  
4.  En la ficha desplegable **Opciones**, rellene el campo **Nº documento** con un número que introduzca manualmente. Ya que no se han configurado números de serie para este proceso, utilice el esquema de números que ha configurado para el almacén o introduzca la fecha seguida de sus iniciales.  
5.  Elija el botón **Aceptar**. Los ajustes positivos y negativos se totalizan para cada artículo y las líneas se crean en el diario del artículo para cualquier artículo donde la suma sea una cantidad positiva o negativa.  
6.  Registre las líneas del diario para especificar las diferencias de cantidades en el diario de productos. Las existencias en las ubicaciones de almacén se corresponden ahora exactamente con las existencias en el diario de productos.  

## <a name="to-reclassify-an-items-lot-number"></a>Reclasificar el número de lote de un producto
Si necesita cambiar los atributos de las entradas de contabilidad de los productos, puede usar el diario de reclasificación de productos. Los atributos típicos para reclasificar incluyen dimensiones y códigos de campaña, aunque también realiza el "transferencias del sistema" mediante la reclasificación de códigos de ubicación y de almacén.

Se aplican pasos especiales cuando desea reclasificar números de serie o de lote, y sus fechas de caducidad. Para obtener más información, consulte [Trabajar con números de serie y de lote](inventory-how-work-item-tracking.md).

El siguiente ejemplo se basa en un código de almacén. Los pasos son parecidos para otros tipos de atributos de producto.

1. Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Diarios reclasif. producto** y luego elija el enlace relacionado.
2. En la página **Diarios reclasif. producto**, rellene los campos según sea necesario.
3. En el campo **Cód. almacén**, especifique el código de ubicación actual del producto.
4. En el campo **Cód. almacén destino**, especifique el código de ubicación nuevo del producto.
5. Seleccione la acción **Registrar**.

Para obtener información sobre la transferencia de productos con el control total de las cantidades enviadas y recibidas, consulte [Transferir el inventario entre almacenes](inventory-how-transfer-between-locations.md).

## <a name="see-also"></a>Consulte también
[Contar inventario mediante documentos](inventory-how-count-inventory-with-documents.md)  
[Inventario](inventory-manage-inventory.md)
[Gestión almacenes](warehouse-manage-warehouse.md)    
[Ccial](sales-manage-sales.md)  
[Compras](purchasing-manage-purchasing.md)  
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
