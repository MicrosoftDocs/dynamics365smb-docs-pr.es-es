---
title: Recuento y ajuste de inventario
description: Describe cómo contar el inventario físico y usar documentos de inventario para ajustar el inventario disponible.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: adjustment, status, negative, positive, increase, decrease, inventory
ms.search.forms: 5895, 6561, 6562, 6563, 6564, 6565, 6566, 5892, 5891, 5879, 5880, 5893, 5897, 5882, 5881, 5899, 5875, 5878, 5877, 5876, 5896, 6567, 6568, 6569, 6570, 6571, 6572, 5883, 5886, 884, 5898, 5885, 5890, 5888, 5889, 5887, 5894, 6774, 6775, 6776, 6780, 6781, 6782, 6783
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: af091b33126d4098980c19329d7160ef1789c1b9
ms.sourcegitcommit: ef80c461713fff1a75998766e7a4ed3a7c6121d0
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 02/15/2022
ms.locfileid: "8131592"
---
# <a name="count-and-adjust-inventory-using-documents"></a>Recuento y ajuste de inventario mediante documentos

Puede realizar un inventario físico de los productos utilizando los documentos de pedido de inventario físico y registro de inventario físico. La página **Orden de inventario físico** se usa para organizar el proyecto de recuento de inventario completo, por ejemplo una por almacén. La página **Registro de inventario físico** se usa para comunicar y para capturar el recuento real de productos. Puede crear varias grabaciones para un pedido, por ejemplo, para distribuir grupos de productos a diferentes empleados.

El informe **Registro de inventario físico** se puede imprimir desde cada registro y contiene los campos de cantidad vacíos para introducir el inventario contado. Cuando un usuario termina el recuento, y las cantidades se han introducido en la página **Registro de inventario físico**, elija la acción **Terminar**. Esto transfiere las cantidades a las líneas asociadas en la página **Pedido de inventario físico**. La funcionalidad garantiza que el recuento de productos no se pueda registrar dos veces.  

> [!NOTE]
> El uso de documentos para realizar un inventario físico proporciona más control y admite la distribución del recuento a varios empleados. También puede realizar la tarea con los diarios, como **Diarios de inventario** y las páginas **Diarios de inventario de almacén**. Para obtener más información, consulte [Recuento, ajuste y reclasificación de inventario mediante diarios](inventory-how-count-adjust-reclassify.md). En este artículo se describe cómo realizar un inventario físico con documentos.
>
> Si usa zonas, no puede usar pedidos de inventario físico. En su lugar, use la página **Diario de inventario físico de almacén** para contar las entradas del almacén antes de sincronizarlas con los movimientos de producto.

El recuento de inventario con documentos consta de los pasos generales siguientes:

1. Crear un pedido de inventario físico con las cantidades esperadas de producto llenadas previamente.
2. Generar uno o más registros de inventario físico a partir del pedido.
3. Escriba las cantidades contadas del producto en los registros, tal como se capturan en las copias impresas, por ejemplo, y establezca **Terminada**.
4. Complete y registre el pedido de inventario físico.

## <a name="to-create-a-physical-inventory-order"></a>Para crear un pedido de inventario físico
Un pedido de inventario físico es un documento completo formado por la cabecera del pedido de inventario físico y unas líneas de pedido de inventario físico. La información de la cabecera de inventario físico describe cómo realizar el inventario físico. Las líneas de pedido de inventario físico contienen información acerca de los productos y sus almacenes.

Para crear las líneas de pedido de inventario físico, se suele usar la función **Calcular líneas** para reflejar el inventario actual como líneas del pedido. Opcionalmente, puede utilizar la función **Copiar de documento** para rellenar las líneas con el contenido de otro pedido de inventario físico abierto o registrado. El procedimiento siguiente solo describe cómo utilizar la función **Calcular líneas**.

1. Elija el icono ![Bombilla que abre la característica Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Pedidos de inventario físico** y luego elija el enlace relacionado.
2. Seleccione la acción **Nuevo**.
3. Rellene los campos obligatorios en la ficha desplegable **General**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Elija la acción **Calcular líneas**.
5. Seleccione las opciones según sea necesario.
6. Establezca filtros, por ejemplo, para incluir solo un subconjunto de productos que se contarán con el primer registro.

    > [!TIP]
    > Para planificar que varios empleados cuenten el inventario, es aconsejable definir distintos filtros cada vez que utilice la acción **Calcular líneas** para rellenar solo el pedido con el subconjunto de productos de inventario que un usuario registrará. A continuación, cuando genere varios registros de inventario físico para varios empleados, se minimiza el riesgo de contar productos dos veces. Para obtener más información, consulte la sección [Para crear un registro de inventario físico](#to-create-a-physical-inventory-recording).

7. Elija el botón **Aceptar**.

Una línea para cada producto que exista en el almacén seleccionado y según los filtros y las opciones configurados se inserta en el pedido. Para aquellos productos que está configurado el seguimiento de productos, se selecciona la casilla **Usar seguimiento de producto** e información relativa a la cantidad prevista de números de serie y de lote está disponible eligiendo la acción **Líneas** y después en **Líns. seguim. prod. almacén**. Para obtener más información, vea la sección [Control del seguimiento de productos durante el recuento de inventario](#handling-item-tracking-when-counting-inventory).

Ahora puede empezar a crear uno o más registros, que son instrucciones para los empleados que llevan a cabo el recuento real.  

## <a name="to-create-a-physical-inventory-recording"></a>Para crear un registro de inventario físico
Por cada pedido de inventario físico, puede crear uno o varios documentos de registro de inventario físico en los que los empleados hayan introducido las cantidades contadas, manualmente o a través de un dispositivo de escaneado integrado.

De forma predeterminada, un registro se crea para todas las líneas del pedido de inventario físico relacionadas. Para evitar que dos empleados cuenten los mismos productos en caso de recuento distribuido, se recomienda rellenar gradualmente el pedido de inventario físico definiendo filtros en el proceso **Calcular líneas** (consulte la sección "Para crear un pedido de inventario físico) y después cree el registro de inventario físico a la vez que selecciona la casilla **Solo líneas que no estén en registros**. Estos valores garantizan que cada registro nuevo que cree solo contenga productos diferentes a los que están en otros registros.

En caso de recuento manual, puede imprimir una lista, el informe **Registro inv. fís.**, que tiene una columna en blanco para escribir las cantidades contadas en él. Una vez finalizado el recuento, introduzca las cantidades registradas en las líneas relacionadas de la página **Registro inv. fís.**. Por último, transfiera las cantidades registradas al pedido de inventario físico relacionado definiendo el estado **Terminada**.

1. En la página **Pedido de inventario físico** que contiene líneas de los productos que se contarán en un registro, elija la acción **Crear registro nuevo**.
2. Seleccione opciones y establezca filtros según sea necesario.
3. Elija el botón **Aceptar**.

    Se crea un documento de registro de inventario físico.

4. Para cada grupo de productos que se contarán, cárguelos en el pedido de inventario físico relacionado y repita los pasos 1 a 3 con la casilla de verificación **Solo líneas que no están en registros** seleccionada.

5. Seleccione la acción **Registros** para abrir la página **Lista de registros invent. fís.**
6. Abra el registro que corresponda.
7. En la ficha desplegable **General**, rellene los campos como sea necesario.
8. Para aquellos productos que utilizan seguimiento, cree una línea adicional para cada código de número de lote o de serie eligiendo la acción **Funciones** y, después, la acción **Copiar línea**. Para obtener más información, vea la sección [Control del seguimiento de productos durante el recuento de inventario](#handling-item-tracking-when-counting-inventory).  
9. Seleccione la acción **Imprimir** para preparar el documento físico que los empleados utilizarán para anotar las cantidades contadas.

## <a name="to-finish-a-physical-inventory-recording"></a>Para finalizar un registro de inventario físico
Cuando los empleados hayan contado las cantidades de inventario, debe prepararse para registrarlas en el sistema.

1. En la página **Lista de registros invent. fís.** , seleccione el registro de inventario físico que desea terminar y, a continuación, seleccione la acción **Edición**.
2. En la ficha desplegable **Líneas**, rellene la cantidad contada real en el campo **Cantidad** para cada línea.
3. Para los productos con números de serie o lote (la casilla de verificación **Usar seguimiento de producto** está seleccionada), introduzca las cantidades contadas en las líneas dedicadas de los números de serie y de lote del producto respectivamente. Para obtener más información, vea la sección [Control del seguimiento de productos durante el recuento de inventario](#handling-item-tracking-when-counting-inventory).
4. Seleccione la casilla de verificación **Registrado** en cada línea.
5. Cuando haya introducido todos los datos de un registro de inventario físico, elija la acción **Terminar**. Tenga en cuenta que todas las líneas deben tener la casilla de verificación **Registrado** seleccionada.

> [!NOTE]
> Cuando se termina un registro de inventario físico, cada línea se transfiere a la línea del pedido de inventario físico relacionado que coincide exactamente con él. Para que coincida, los valores de los campos **Nº producto**, **Cód. variante**, **Cód. almacén** y **Cód. ubicación** deben ser los mismos en el registro y en las líneas del pedido.<br /><br />
> Si no existe ninguna línea de pedido de inventario físico coincidente, y si está activada la casilla de verificación **Permitir registro sin pedido**, una nueva línea se insertará automáticamente y se selecciona la casilla de verificación **Registrado sin pedido** en la línea de pedido de inventario físico relacionada. De lo contrario, se mostrará un mensaje de error y se cancelará el proceso.<br /><br />
> Si varias líneas de registro de inventario físico coinciden con una línea de pedido de inventario físico, se mostrará un mensaje y se cancela el proceso. Si, por algún motivo, dos líneas idénticas de inventario físico idénticas terminan en pedido de inventario físico, puede usar una función para resolverlo. Para obtener más información, consulte la sección [Para encontrar líneas de pedido de inventario físico duplicadas](#to-find-duplicate-physical-inventory-order-lines).

## <a name="to-complete-a-physical-inventory-order"></a>Para completar un pedido de inventario físico
Cuando haya terminado un registro de inventario físico, el campo **Cant. registrada (base)** del pedido de inventario físico relacionado se actualiza con los valores contados (registrados) y se selecciona la casilla de verificación **Al registrar**. Si un valor contado es distinto del previsto, esa diferencia se muestra en el campo **Cantidad pos. (base)** y **Cantidad neg. (base)** respectivamente.

Para ver cantidades previstas y cualquier diferencia registrada para los productos con el seguimiento de producto, elija la acción **Líneas** y, a continuación elija **Líns. seguim. prod.** para seleccionar varias vistas de los números de serie y lote implicados en el recuento de inventario físico.

También puede elegir la acción **Dif. pedido invent. físico** para ver las diferencias entre la cantidad esperada y la cantidad contada.

### <a name="to-find-duplicate-physical-inventory-order-lines"></a>Para encontrar líneas de pedido de inventario físico duplicadas

1. Elija el icono ![Bombilla que abre la característica Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Pedidos de inventario físico** y luego elija el enlace relacionado.
2. Abra el inventario físico del que desea ver las líneas duplicadas.
3. Seleccione la acción **Mostrar líneas duplicadas**.

Se muestran las líneas de pedido de inventario físico duplicadas para que pueda eliminarlas y conservar solo una línea con un conjunto único de los valores de los campos **Nº producto**, **Cód. variante**, **Cód. almacén** y **Cód. ubicación**.

### <a name="to-post-a-physical-inventory-order"></a>Para registrar un pedido de inventario físico
Después de completar un inventario físico pedido y cambiar el estado **Terminada**, puede registrarlo. Puede definir solo el estado de un inventario físico pedido en **Terminada** si se cumple lo siguiente:

- Todos los registros de inventario físico relacionados tienen un estado de **Terminada**.
- Cada línea de pedido de inventario físico ha sido contada por al menos una línea de registro de inventario.
- Las casillas de verificación **En líneas de registro** y **Cant. esperada calculada** se han seleccionado para todas las líneas de pedido de inventario físico.

1. Elija el icono ![Bombilla que abre la característica Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Pedidos de inventario físico** y luego elija el enlace relacionado.
2. Seleccione el pedido de inventario físico que desea completar, y después seleccione la acción **Editar**.

    En la página **Pedido de inventario físico**, puede ver la cantidad registrada en el campo **Cant. registrada (base)**.
3. Seleccione la acción **Terminar**.

    El valor del campo **Estado** se cambia a **Terminada** y ahora solo puede cambiar el pedido si primer elige la acción **Volver a abrir**.
4. Para registrar el pedido, elija la acción **Registrar** y el botón **Aceptar**.

Los movimientos de producto correspondientes se actualizan junto con los movimientos de seguimiento de producto relacionados.

### <a name="to-view-posted-physical-inventory-orders"></a>Para ver los pedidos de inventario físico registrados
Después de realizar el registro, el pedido de inventario físico se borrará y podrá ver y evaluar el documento como un pedido de inventario físico con sus registros de inventario físico y cualquier comentario que haya creado.

1. Elija el icono ![Bombilla que abre la característica Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Pedidos inv. fís. registrados** y luego elija el enlace relacionado.
2. En la página **Pedidos inv. fís. registrados**, seleccione el pedido de inventario registrado que desea ver, y después seleccione la acción **Ver**.
3. Para ver una lista de registros de inventario físico relacionados, elija la acción **Registros**.

## <a name="handling-item-tracking-when-counting-inventory"></a>Control del seguimiento de producto al contar el inventario
El seguimiento de producto pertenece a los números de serie o de lote asignados a los productos. Al contar un producto que esté almacenado en el inventario, por ejemplo, 10 números de lote distintos, el empleado debe poder registrar cuáles y cuántas de las unidades de cada número de lote están en inventario. Para obtener más información sobre la función de seguimiento de producto, consulte [Trabajar con números de serie y de lote](inventory-how-work-item-tracking.md).

La casilla de verificación **Usar seguimiento de producto** en líneas de pedido de inventario físico se selecciona automáticamente cuando un código de seguimiento de producto está configurado para el producto, pero también puede seleccionarlo o deseleccionarlo manualmente.

### <a name="example---prepare-a-physical-inventory-recording-for-an-item-tracked-item"></a>Ejemplo: preparar un registro de inventario físico para un producto seguido
Considere un inventario físico del producto A, que está almacenado en inventario como diez números de serie distintos.
1. En la línea de registro del producto, active la casilla de verificación **Usar seguimiento de producto**.
2.  Elija el campo **Nº serie**, seleccione el primer número de serie que existe en el inventario correspondiente al producto y, a continuación, seleccione el botón **Aceptar**.

    Copie la línea del primer producto seguido para insertar líneas adicionales correspondientes al número de números de serie que están almacenados en el inventario.

3. Seleccione la acción **Funciones** y, después, la acción **Copiar línea**.
4. En la página **Copiar línea registro inv. fís.**, escriba 9 en el campo **Nº copias** y después seleccione el botón **Aceptar**.
5. En la primera de las líneas de la copia, seleccione el campo **Nº serie** y seleccione el número de serie siguiente correspondiente al producto.
6. Repita el paso 5 para los ocho números de serie restantes, procurando no seleccionar el mismo dos veces.
7. Seleccione la acción **Imprimir** para preparar la copia impresa que los empleados utilizarán para anotar los productos y números de serie/lote contados.

Observe que el informe **Registro inv. fís.** contiene diez líneas para el producto A, una para cada número de serie.

### <a name="example---record-and-post-counted-lot-number-differences"></a>Ejemplo: registrar y contabilizar diferencias de los números de lote contados
Un producto con seguimiento de lote está almacenado en inventario con la serie de números “LOT”.

**Inventario previsto**:

|Nº lote|Cantidad|
|-|-|
|LOT1001|80|
|LOT1003|30|
|LOT1006|10|
|Total|120|

**Cantidades registradas**:

|Nº lote|Cantidad|
|-|-|
|LOT1001|80|
|LOT0002|12|
|LOT1003|nº 20|
|LOT1006|10|
|Total|112|

**Cantidades para registrar**:

|Nº lote|Cantidad esperada|Cantidad registrada|Cantidad para registrar|
|-|-|-|-|
|LOT1001|80|80|0|
|LOT1002|0|12|+12|
|LOT1003|30|nº 20|-10|
|LOT1006|10|0|-10|
|Total|120|112|-8|

En la página **Pedido de inventario físico**, el campo **Cantidad neg. (base)** contendrá *8*. Para la línea de pedido en cuestión, la página **Lista seguim. prod. inv. fís.** contendrá las cantidades positivas o negativas de los números de lote individuales.

## <a name="inventory-documents"></a>Documentos de inventario
Los siguientes tipos de documentos son útiles para administrar su almacén:

- Use **Recepciones de inventario** para registrar ajustes positivos de productos basados en la calidad, la cantidad y el coste.
- Use **Envíos de inventario** para cancelar bienes perdidos o dañados.

Puede imprimir estos documentos en cualquier etapa, liberarlos y volverlos a abrir, y asignar valores comunes, incluidas dimensiones, en el encabezado. Si desea volver a imprimir los documentos después de que se hayan registrado, puede hacerlo en las páginas **Histórico recepción de inventario** y **Histórico envío inventario**.

> [!NOTE]
> Antes de poder usar estos documentos, debe especificar una serie de números para crear sus identificadores. Para obtener más información, consulte la sección siguiente.

### <a name="to-set-up-numbering-for-inventory-documents"></a>Para configurar la numeración de los documentos de inventario
El siguiente procedimiento muestra cómo configurar la numeración de los documentos de inventario.

1. Elija el icono ![Bombilla que abre la característica Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Config. existencias** y luego elija el enlace relacionado.
2. En la ficha desplegable **Numeración**, especifique en los siguientes campos la serie de números de documentos:
   - **Números recep. inventario**  
   - **Números histórico recepciones de inventario**  
   - **Números envío inventario**  
   - **Números histórico envío inventario**  

### <a name="to-create-and-post-an-inventory-document"></a>Para crear y registrar un documento de inventario
En el siguiente procedimiento se muestra cómo crear, imprimir y registrar una recepción de inventario. Los pasos son parecidos para los envíos de inventario.

1. Elija el icono ![Bombilla que abre la característica Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Recepciones de inventario** y luego elija el enlace relacionado.  
2. En el encabezado de la página **Recepción de inventario**, elija la ubicación en el **Código de almacén** y luego rellene los campos restantes según sea necesario.
3. En la ficha desplegable **Líneas**, en el campo **Producto**, elija el producto de inventario. En el campo **Cantidad**, escriba el número de productos que se van a agregar. 
4. Para imprimir un informe **Recepción de inventario** de la página **Recepción de inventario**, elija la acción **Imprimir**.

Las siguientes funciones están disponibles en la página **Recepción de inventario**:

- Elegir las acciones **Lanzar** o **Volver a abrir** para establecer el estado de la siguiente etapa de procesamiento  
- Elegir la acción **Registrar** para registrar la recepción de inventario o elegir **Registrar e imprimir** para registrar la recepción e imprimir el informe de prueba  

## <a name="printing-inventory-documents"></a>Impresión de documentos de inventario
Puede especificar los informes que deben imprimirse en diferentes etapas eligiendo una de las siguientes opciones en el campo **Uso** de la página **Selección de informes - Inventario**:

- Recepción inventario
- Envío inventario
- Histórico recepción de inventario
- Histórico envío inventario

> [!NOTE]
> Los informes disponibles pueden variar según la localización de su país. La aplicación base no incluye ningún diseño.

## <a name="see-also"></a>Consulte también
[Recuento, ajuste y reclasificación de inventario con diarios](inventory-how-count-adjust-reclassify.md)  
[Trabajar con números de lote y de serie](inventory-how-work-item-tracking.md)  
[Inventario](inventory-manage-inventory.md)  
[Gestión almacén](warehouse-manage-warehouse.md)    
[Ccial](sales-manage-sales.md)  
[Compras](purchasing-manage-purchasing.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]