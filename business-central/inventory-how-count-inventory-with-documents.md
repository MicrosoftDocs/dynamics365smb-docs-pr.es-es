---
title: Recuento y ajuste de inventario
description: Describe cómo contar el inventario físico y usar documentos de inventario para ajustar el inventario disponible.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.topic: how-to
ms.search.keywords: 'adjustment, status, negative, positive, increase, decrease, inventory'
ms.search.forms: '5895, 6561, 6562, 6563, 6564, 6565, 6566, 5892, 5891, 5879, 5880, 5893, 5897, 5882, 5881, 5899, 5875, 5878, 5877, 5876, 5896, 6567, 6568, 6569, 6570, 6571, 6572, 5883, 5886, 884, 5898, 5885, 5890, 5888, 5889, 5887, 5894, 6774, 6775, 6776, 6780, 6781, 6782, 6783'
ms.date: 03/11/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# Recuento y ajuste de inventario mediante documentos

Puede realizar un inventario físico de los productos utilizando los documentos de pedido de inventario físico y registro de inventario físico. La página **Orden de inventario físico** se usa para organizar el proyecto de recuento de inventario completo, por ejemplo una por almacén. La página **Registro de inventario físico** se usa para comunicar y para capturar el recuento real de productos. Puede crear varias grabaciones para un pedido, por ejemplo, para distribuir grupos de productos a diferentes empleados.

Puede imprimir el informe **Registro de inventario físico** desde cada registro y contiene los campos de cantidad vacíos en los que puede introducir el inventario contado. Cuando termine el recuento y las cantidades se han introducido en la página **Registro de inventario físico**, elija la acción **Terminar**. Esta acción transfiere las cantidades a las líneas asociadas en la página **Pedido de inventario físico**. [!INCLUDE [prod_short](includes/prod_short.md)] garantiza que no se pueda registrar un recuento de elementos dos veces.  

> [!NOTE]
> El uso de documentos para realizar un recuento de inventario físico proporciona más control y admite la distribución del recuento a varios empleados. También puede usar diarios para realizar la tarea, como **Diarios de inventario** y las páginas **Diarios de inventario físico de almacén**. Obtenga más información en [Recuento, ajuste y reclasificación de inventario con diarios](inventory-how-count-adjust-reclassify.md). En este artículo se describe cómo usar documentos para realizar un recuento de inventario físico.
>
> Si usa zonas en su almacén, no puede usar pedidos de inventario físico. En su lugar, use la página **Diario de inventario físico de almacén** para contar las entradas del almacén antes de sincronizarlas con los movimientos de producto.

El recuento de inventario con documentos consta de los pasos generales siguientes:

1. Crear un pedido de inventario físico con las cantidades esperadas de producto llenadas previamente.
2. Generar uno o más registros de inventario físico a partir del pedido.
3. Escriba las cantidades contadas del producto en los registros, tal como se capturan en las copias impresas, por ejemplo, y establezca **Terminada**.
4. Complete y registre el pedido de inventario físico.

## Para crear un pedido de inventario físico

Un pedido de inventario físico es un documento completo formado por la cabecera del pedido de inventario físico y líneas de pedido. La información de la cabecera de inventario físico describe cómo realizar el inventario físico. Las líneas de pedido contienen información acerca de los productos y sus almacenes.

Para crear las líneas de pedido de inventario físico, se suele usar la acción **Calcular líneas** para agregar el inventario actual como líneas del pedido. Opcionalmente, puede utilizar la acción **Copiar desde documento** para rellenar las líneas con el contenido de otro pedido de inventario físico abierto o registrado. El procedimiento siguiente solo describe cómo utilizar la acción **Calcular líneas**.

1. Elija el icono ![Bombilla que abre la característica Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), , escriba **Pedidos de inventario físico** y luego elija el enlace relacionado.
2. Seleccione la acción **Nuevo**.
3. Rellene los campos obligatorios en la ficha desplegable **General**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Elija la acción **Calcular líneas**.
5. Seleccione las opciones según sea necesario.
6. Establezca filtros, por ejemplo, para incluir solo un subconjunto de productos que se contarán con el primer registro.

    > [!TIP]
    > Para planificar que varios empleados cuenten el inventario, establezca distintos filtros cada vez que utilice la acción **Calcular líneas** para rellenar el pedido con el subconjunto de productos de inventario que un usuario registrará. A continuación, cuando genere varios registros de inventario físico para varios empleados, se minimiza el riesgo de contar productos dos veces. Para obtener más información, vaya a [Para crear un registro de inventario físico](#to-create-a-physical-inventory-recording).

7. Elija el botón **Aceptar**.

Una línea para cada producto que exista en el almacén seleccionado y según los filtros y las opciones configurados se agrega al pedido. Para aquellos productos que está configurado el seguimiento de productos, se selecciona la casilla **Usar seguimiento de producto** e información relativa a la cantidad prevista de números de serie y de lote está disponible eligiendo **Líneas** y después en **Líns. seguim. prod. almacén**. Para obtener más información, vaya a [Gestionar el seguimiento de artículos al contar el inventario](#handle-item-tracking-when-counting-inventory).

Ahora puede crear uno o más registros, que son instrucciones para los empleados que llevan a cabo el recuento.  

> [!NOTE]
> Si utiliza el seguimiento específico de paquetes, también puede utilizar documentos para contar y ajustar el inventario con números de paquetes. Para comenzar a usar esta función, debe activar **Actualización de funciones: habilitar el uso del seguimiento de paquetes en pedidos de inventario físico** en la página **Administración de funciones**. Los pedidos de inventario físico existentes se actualizan; sin embargo, [!INCLUDE [prod_short](includes/prod_short.md)] no puede completar el **N.º de paquete.** . Debe recrear estas líneas usando la acción **Calcular líneas** en la página **Orden de inventario físico**.
>
> Puede introducir el número de paquete para los artículos donde se necesita seguimiento del paquete en la página **Líneas de registro de inventario físico**. Elija **Finalizar** para finalizar la grabación.
>
> Después de elegir **Finalizar** en la página **Orden de inventario físico**, [!INCLUDE [prod_short](includes/prod_short.md)] calcula las diferencias con respecto al paquete y otros detalles de seguimiento del artículo, y realiza ajustes positivos o negativos.

## Para crear un registro de inventario físico

Para cada orden de inventario físico, puede crear uno o más documentos de registro de inventario físico en los que los empleados introducen las cantidades contadas. Los empleados pueden introducir cantidades manualmente o con un dispositivo de escaneo.

De forma predeterminada, un registro se crea para todas las líneas del pedido de inventario físico relacionadas. Para evitar que dos empleados cuenten los mismos artículos si distribuye el recuento, complete gradualmente el orden del inventario físico configurando filtros en el trabajo por lotes **Calcular líneas**. Luego cree el registro de inventario físico con la casilla de verificación **Solo líneas que no están en registros** marcada. Esta configuración garantiza que cada registro nuevo solo contenga productos diferentes a los que están en otros registros.

En caso de recuento manual, puede imprimir una lista, el informe **Registro inv. fís.**, que tiene una columna en blanco en la que los empleados pueden escribir las cantidades contadas. Una vez finalizado el recuento, introduzca las cantidades registradas en las líneas relacionadas de la página **Registro inv. fís.**. Por último, transfiera las cantidades registradas al pedido de inventario físico relacionado definiendo el estado **Terminada**.

1. En la página **Pedido de inventario físico** que contiene líneas de los productos que se contarán en un registro, elija la acción **Crear registro nuevo**.
2. Seleccione opciones y establezca filtros según sea necesario.
3. Elija el botón **Aceptar**.
4. Para cada grupo de productos que se contarán, cárguelos en el pedido de inventario físico relacionado y repita los pasos 1 a 3 con la casilla de verificación **Solo líneas que no están en registros** seleccionada.
5. Seleccione la acción **Registros** para abrir la página **Lista de registros invent. fís.**
6. Abra el registro que corresponda.
7. En la ficha desplegable **General**, rellene los campos como sea necesario.
8. Para aquellos productos que utilizan seguimiento, cree una línea adicional para cada código de número de lote o de serie eligiendo la acción **Funciones** y, después, la acción **Copiar línea**. Para obtener más información, vaya a [Gestionar el seguimiento de artículos al contar el inventario](#handle-item-tracking-when-counting-inventory).  
9. Seleccione la acción **Imprimir** para preparar el documento físico que los empleados pueden usar para anotar las cantidades que cuenten.

## Para finalizar un registro de inventario físico

Después de que los empleados cuenten las cantidades, registre las cantidades en [!INCLUDE [prod_short](includes/prod_short.md)].

1. En la página **Lista de registros invent. fís.** , seleccione el registro de inventario físico que desea terminar y, a continuación, seleccione la acción **Edición**.
2. En la ficha desplegable **Líneas**, rellene la cantidad contada real en el campo **Cantidad** para cada línea.
3. Para los productos con números de serie o lote (la casilla de verificación **Usar seguimiento de producto** está seleccionada), introduzca las cantidades contadas en las líneas de los números de serie y de lote del producto respectivamente. Para obtener más información, vaya a [Gestionar el seguimiento de artículos al contar el inventario](#handle-item-tracking-when-counting-inventory).
4. Seleccione la casilla de verificación **Registrado** en cada línea.
5. Cuando haya introducido todos los datos de un registro de inventario físico, elija la acción **Terminar**. Tenga en cuenta que todas las líneas deben tener la casilla de verificación **Registrado** seleccionada.

    > [!NOTE]
    > Cuando se termina un registro de inventario físico, cada línea se transfiere a la línea del pedido de inventario físico relacionado que coincide exactamente con él. Para que coincida, los valores de los campos **Nº producto**, **Cód. variante**, **Cód. almacén** y **Cód. ubicación** deben ser los mismos en el registro y en las líneas del pedido.>
    > 
    > Si no existe ninguna línea de pedido de inventario físico coincidente, y si está activada la casilla de verificación **Permitir registro sin pedido**, una nueva línea se agrega y se selecciona la casilla de verificación **Registrado sin pedido** en la línea de pedido de inventario físico relacionada. De lo contrario, aparece un mensaje de error y el proceso se cancela.> Si varias líneas de registro de inventario físico coinciden con una línea de pedido de inventario físico, se muestra un mensaje y se cancela el proceso. Si, por algún motivo, dos líneas idénticas de inventario físico idénticas terminan en pedido de inventario físico, puede usar una acción para resolverlo. Para obtener más información, vaya a [Para buscar líneas de pedido de inventario físico duplicadas](#to-find-duplicate-physical-inventory-order-lines).

## Para completar un pedido de inventario físico

Cuando haya terminado un registro de inventario físico, el campo **Cant. registrada (base)** del pedido de inventario físico relacionado se actualiza con los valores contados (registrados) y se selecciona la casilla de verificación **Al registrar**. Si un valor contado es distinto del previsto, esa diferencia se muestra en los campos **Cantidad pos. (base)** y **Cantidad neg. (base)**.

Para acceder a cantidades previstas y cualquier diferencia registrada para los productos con el seguimiento de producto, elija la acción **Líneas** y, a continuación elija **Líns. seguim. prod.** para seleccionar varias vistas de los números de serie y lote en el recuento de inventario físico.

También puede elegir la acción **Dif. pedido invent. físico** para ver las diferencias entre la cantidad esperada y la cantidad contada.

### Para encontrar líneas de pedido de inventario físico duplicadas

1. Elija el icono ![Bombilla que abre la característica Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Pedidos de inventario físico** y luego elija el enlace relacionado.
2. Abra el inventario físico para ver las líneas duplicadas.
3. Seleccione la acción **Mostrar líneas duplicadas**.

Las líneas de pedido de inventario físico duplicadas se muestran para que pueda eliminarlas y conservar solo una línea con un conjunto único de los valores de los campos **N.º producto**, **Código de variante**, **Código de almacén** y **Código de ubicación**.

### Para registrar un pedido de inventario físico

Después de completar un inventario físico pedido y cambiar el estado **Terminada**, puede registrarlo. Puede definir solo el estado de un inventario físico pedido en **Terminada** si se cumplen las condiciones siguientes:

- Todos los registros de inventario físico relacionados tienen un estado de **Terminada**.
- Cada línea de pedido de inventario físico ha sido contada por al menos una línea de registro de inventario.
- Las casillas de verificación **En líneas de registro** y **Cant. esperada calculada** se han seleccionado para todas las líneas de pedido de inventario físico.

1. Elija el icono ![Bombilla que abre la característica Dígame](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Pedidos de inventario físico** y luego elija el enlace relacionado.
2. Seleccione el pedido de inventario físico que desea completar, y después seleccione la acción **Editar**.

    En la página **Pedido de inventario físico**, puede ver la cantidad registrada en el campo **Cant. registrada (base)**.
3. Seleccione la acción **Terminar**.

    El valor del campo **Estado** es **Completado**. Ahora solo puede cambiar el orden eligiendo la acción **Reabrir**.
4. Para registrar el pedido, elija la acción **Registrar** y el botón **Aceptar**.

    Los movimientos contables de producto se actualizan junto con los movimientos de seguimiento de producto relacionados.

    [!INCLUDE [preview-posting-inventory](includes/preview-posting-inventory.md)]

### Para ver los pedidos de inventario físico registrados

Después de realizar el registro, el pedido de inventario físico se borrará y podrá ver y evaluar el documento como un pedido de inventario físico registrado. El pedido publicado incluye los registros de su inventario físico y cualquier comentario realizado.

1. Elija el icono ![Bombilla que abre la característica Dígame](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Pedidos inv. fís. registrados** y luego elija el enlace relacionado.
2. En la página **Pedidos inv. fís. registrados**, seleccione el pedido de inventario registrado que desea ver, y después seleccione la acción **Ver**.
3. Para ver una lista de registros de inventario físico relacionados, elija la acción **Registros**.

## Gestión de seguimiento de productos en el recuento de inventario

El seguimiento de producto pertenece a los números de serie o de lote asignados a los productos. Al contar un producto que esté almacenado en el inventario, por ejemplo, 10 números de lote distintos, el empleado debe poder registrar cuáles y cuántas de las unidades de cada número de lote están en inventario. Obtenga más información en [Trabajar con números de serie y de lote](inventory-how-work-item-tracking.md).

La casilla de verificación **Usar seguimiento de producto** en líneas de pedido de inventario físico se selecciona automáticamente cuando un código de seguimiento de producto está configurado para el producto. Puede seleccionar o borrar la casilla de verificación manualmente.

### Ejemplo: preparar un registro de inventario físico para un producto seguido

Considere un inventario físico del producto A, que está almacenado en inventario como diez números de serie distintos.

1. En la línea de registro del producto, active la casilla de verificación **Usar seguimiento de producto**.
2. Elija el campo **Nº serie**, seleccione el primer número de serie que existe en el inventario correspondiente al producto y, a continuación, seleccione el botón **Aceptar**.

    Copie la línea del primer producto seguido para insertar líneas adicionales correspondientes al número de números de serie que están almacenados en el inventario.

3. Seleccione la acción **Funciones** y, después, elija **Copiar línea**.
4. En la página **Copiar línea registro inv. fís**., escriba **9** en el campo **N.º copias** y después seleccione el botón **Aceptar**.
5. En la primera línea, en el campo **Nº serie** seleccione el número de serie siguiente correspondiente al producto.
6. Repita el paso 5 para los ocho números de serie restantes. Asegúrese de no seleccionar el mismo número dos veces.
7. Seleccione la acción **Imprimir** para preparar la copia impresa que los empleados utilizarán para anotar los productos y números de serie/lote contados.

Observe que el informe **Registro inv. fís.** contiene diez líneas para el producto A, una para cada número de serie.

### Ejemplo: registrar y contabilizar diferencias de los números de lote contados

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

En la página **Pedido de inventario físico**, el campo **Cantidad neg. (base)** contendrá **8**. Para la línea de pedido , la página **Lista seguim. prod. inv. fís.** muestra las cantidades positivas o negativas de cada número de lote.

## Documentos de inventario

Los siguientes tipos de documentos son útiles para administrar su almacén:

* Use **Recepciones de inventario** para registrar ajustes positivos de productos basados en la calidad, la cantidad y el coste.
* Use **Envíos de inventario** para cancelar bienes perdidos o dañados.

Puede imprimir estos documentos en cualquier etapa, liberarlos y volverlos a abrir, y asignar valores comunes, como dimensiones, en el encabezado. Para reimprimir los documentos después de su publicación, utilice las páginas **Recibo de inventario publicado** y **Envío de inventario publicado** .

> [!NOTE]
> Antes de poder usar estos documentos, debe especificar una serie de números para crear sus identificadores. Para obtener más información, vaya a [Para configurar la numeración de documentos de inventario](#to-set-up-numbering-for-inventory-documents).

### Para configurar la numeración de los documentos de inventario

El siguiente procedimiento muestra cómo configurar la numeración de los documentos de inventario.

1. Elija el icono ![Bombilla que abre la característica Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Config. existencias** y luego elija el enlace relacionado.
2. En la ficha desplegable **Numeración**, especifique en los siguientes campos la serie de números de documentos:

   - **Números recep. inventario**  
   - **Números histórico recepciones de inventario**  
   - **Números envío inventario**  
   - **Números histórico envío inventario**  

### Para crear y registrar un documento de inventario

En el siguiente procedimiento se muestra cómo crear, imprimir y registrar una recepción de inventario. Los pasos son parecidos para los envíos de inventario.

1. Elija el icono ![Bombilla que abre la característica Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Recepciones de inventario** y luego elija el enlace relacionado.  
2. En el encabezado de la página **Recepción de inventario**, elija la ubicación en el **Código de almacén** y luego rellene los campos restantes según sea necesario.
3. En la ficha desplegable **Líneas**, en el campo **Producto**, elija el producto de inventario. En el campo **Cantidad**, escriba el número de productos que se van a agregar.
4. Para imprimir un informe **Recepción de inventario** de la página **Recepción de inventario**, elija la acción **Imprimir**.

Las siguientes funciones están disponibles en la página **Recepción de inventario**:

- Elegir las acciones **Lanzar** o **Volver a abrir** para establecer el estado de la siguiente etapa de procesamiento.  
- Elija la acción **Registrar** para registrar la recepción de inventario o elegir **Registrar e imprimir** para registrar la recepción e imprimir el informe de prueba.  

    [!INCLUDE [preview-posting-inventory](includes/preview-posting-inventory.md)]

## Impresión de documentos de inventario

Puede especificar los informes que deben imprimirse en diferentes etapas eligiendo una de las siguientes opciones en el campo **Uso** de la página **Selección de informes - Inventario**:

* Recep. inventario
* Envío inventario
* Histórico recepción de inventario
* Histórico envío inventario

> [!NOTE]
> Los informes disponibles pueden variar según la localización de su país o región. La aplicación base no incluye ningún diseño.

## Consulte también .

[Recuento, ajuste y reclasificación de inventario con diarios](inventory-how-count-adjust-reclassify.md)  
[Trabajar con números de lote y de serie](inventory-how-work-item-tracking.md)  
[Inventario](inventory-manage-inventory.md)  
[Información general de la gestión de almacenes](design-details-warehouse-management.md)  
[Ccial](sales-manage-sales.md)  
[Compras](purchasing-manage-purchasing.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
