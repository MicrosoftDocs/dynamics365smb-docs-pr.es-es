---
title: Trabajar con dimensiones para rastrear y analizar datos
description: 'Use dimensiones para clasificar movimientos en categorías, por ejemplo, por departamentos o proyecto, para que le sea más fácil realizar un seguimiento de los datos y analizarlos para ayudarle a tomar buenas decisiones empresariales.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.service: dynamics365-business-central
ms.topic: how-to
ms.date: 01/27/2023
ms.custom: bap-template
ms.search.keywords: 'analysis, history, track, business intelligence'
ms.search.form: '408, 479, 480, 481, 484, 536, 537, 538, 539, 540, 541, 542, 543, 544, 545, 548, 560, 562, 564, 567, 568, 577, 578, 580, 699, 1343, 2580, 2581, 2582, 2583, 2584, 2585, 2586, 2587, 2588, 2590, 2591, 2592, 2593, 9083, 9233, 9251, 9252, 9253'
---
# <a name="work-with-dimensions" />Trabajar con dimensiones

Las dimensiones son valores que clasifican los movimientos de modo que pueda realizar el seguimiento y el análisis de los documentos, como pedidos de venta. Las dimensiones pueden, por ejemplo, indicar de qué proyecto o departamento procede un movimiento.  

Así, en lugar de configurar cuentas de libro mayor separadas para cada departamento y proyecto, puede utilizar las dimensiones como base para el análisis y evitar tener que crear un plan de cuentas complicado. Obtenga más información en [Inteligencia de negocios](bi.md).

Otro ejemplo es configurar una dimensión que se llame *Departamento* y luego usarla junto con esta dimensión cuando registre documentos de ventas. De este modo, puede usar herramientas la de inteligencia empresarial para ver qué departamento vende cada producto. Cuantas más dimensiones use, más detallados son los informes en los que pueda basar sus decisiones empresariales. De hecho, un movimiento de ventas individual puede incluir información de múltiples dimensiones, como:  

* La cuenta en la que se registró la venta del producto.  
* Dónde se vendió el producto.
* Quién lo vendió.
* Qué cliente lo compró.

## <a name="analyzing-by-dimensions" />Analizar por dimensiones

Las Dimensiones desempeñan una función importante en la inteligencia empresarial, por ejemplo al definir vistas de análisis. Obtenga más información en [Analizar datos por dimensiones](bi-how-analyze-data-dimension.md).

> [!TIP]
> Una forma rápida de analizar datos transaccionales por dimensiones es usar la acción **Establecer filtro de dimensiones** para filtrar los totales por dimensiones en el plan de cuentas y en páginas de movimientos.

> [!NOTE]
> Las vistas de análisis suelen utilizar datos de dimensiones. Si descubre que se ha usado una dimensión incorrecta en los movimientos de contabilidad (G/L), puede corregir los valores de dimensión y actualizar sus vistas de análisis. Esto ayuda a que sus informes y análisis financieros sean precisos. Obtenga más información en [Resolución de problemas y corrección de dimensiones](finance-troubleshooting-correcting-dimensions.md#changing-dimension-assignments-after-posting).

## <a name="dimension-sets" />Grupos de dimensiones

Un grupo de dimensiones es una combinación única de valores de dimensión. Se almacenan como movimientos de grupo de dimensiones en la base de datos. Cada movimiento de grupo de dimensiones representa un valor de dimensión único. Además, cada conjunto de dimensiones y la entrada de conjunto de dimensiones dentro de él se identifican mediante un ID de conjunto de dimensiones común.  

Cuando crea una línea de diario, cabecera de documentos o línea de documentos, puede especificar una combinación de valores de dimensión. En lugar de explícitamente guardar cada valor de dimensión en la base de datos, un Id. de grupo de dimensiones se asigna a la línea de diario, cabecera de documentos o línea de documentos para especificar el grupo de dimensiones.  

## <a name="setting-up-dimensions" />Configurar dimensiones

Puede definir las dimensiones y los valores de dimensión para clasificar los diarios y los documentos, como pedidos de venta y pedidos de compra. Las dimensiones se configuran en la página **Dimensiones**, donde se crea una línea para cada dimensión, como *Proyecto*, *Departamento*, *Área* y *Vendedor*.

También se configuran los valores de dimensión. Digamos que los valores representan los departamentos de su empresa. Los valores de dimensión se pueden configurar en una estructura jerárquica similar al plan de cuentas. Eso significa que los datos se pueden dividir en varios niveles de granularidad y se pueden totalizar subconjuntos de valores de dimensión. Puede definir tantas dimensiones y valores de dimensión como necesite y cualquier usuario de su empresa puede usarlos.

Cuando se configuran dimensiones y valores, puede definir dimensiones globales y de acceso directo en la página **Configuración de contabilidad**. Estas dimensiones estarán siempre disponibles para que las seleccione como campos en líneas de diario y documento, y asientos contables, sin abrir primero la página **Dimensiones**. Obtenga más información en la sección [Para configurar dimensiones globales y abreviadas](finance-dimensions.md#to-set-up-global-and-shortcut-dimensions).

* Las **dimensiones globales** se usan como filtros, por ejemplo, en informes, trabajos por lotes y XMLports. Solo puede utilizar dos dimensiones globales, por lo que debería elegir las dimensiones que use a menudo.
* Las **dimensiones abreviadas** están disponibles como campos en diarios, líneas de documento y movimienos contables. Puede crear un máximo de ocho.  

> [!NOTE]
> Después de utilizar una nueva dimensión en cualquier entrada, como una línea o un nuevo registro, no puede eliminar la dimensión, incluso si no publica la entrada. Esto es porque [!INCLUDE[prod_short](includes/prod_short.md)] crea inmediatamente un conjunto de dimensiones para la línea o registro. Obtenga más información en la sección [Grupos de dimensiones](finance-dimensions.md#dimension-sets).

### <a name="to-set-up-default-dimensions-for-customers-vendors-and-other-accounts" />Para configurar dimensiones predeterminadas para clientes, proveedores y otras cuentas

Puede asignar una dimensión predeterminada para una determinada cuenta. La dimensión se copia en el diario o el documento cuando introduzca el número de cuenta en una línea, pero puede eliminar o cambiar el código de la línea si es necesario. También puede requerir una dimensión en obligatoria para registrar un movimiento en un tipo de cuenta específico. > 

> [!NOTE]
> Las prioridades de dimensión predeterminadas se abren para escenarios de ventas y compras a los que quizás desee prestar especial atención. Cuando usa prioridades de dimensiones predeterminadas en documentos de compras y ventas, [!INCLUDE [prod_short](includes/prod_short.md)] siempre considera las dimensiones del encabezado como provenientes del cliente o proveedor. Esto es cierto para las dimensiones que establece manualmente o de forma predeterminada, y es especialmente relevante cuando utiliza dimensiones predeterminadas en almacenes y productos, pero no en clientes o proveedores.
>
> **Ejemplo:**
>
> Tiene un escenario con la siguiente configuración de dimensión:
>
> * Un cliente sin dimensiones predeterminadas
> * Un producto con ADM como valor de dimensión para la dimensión DEPARTAMENTO
> * Un almacén con PROD como valor de dimensión para la dimensión DEPARTAMENTO
> * Las prioridades de dimensión predeterminadas se establecen como Cliente > Producto > Almacén
>
> Cuando crea un nuevo documento en este escenario, las dimensiones se utilizan de la siguiente manera:
>
> * Si crea un nuevo documento y agrega un almacén, el valor predeterminado de las nuevas líneas será PROD. Cuando agrega líneas con productos, [!INCLUDE [prod_short](includes/prod_short.md)] mantendrá PROD porque proviene del encabezado del documento.
>
> * Si crea un nuevo documento y agrega productos que tienen el valor de dimensión ADM y luego especifica un almacén en el encabezado del documento, [!INCLUDE [prod_short](includes/prod_short.md)] le preguntará si desea sobrescribir las líneas existentes porque hay un conflicto.
>
> Le recomendamos que pruebe la configuración de dimensiones predeterminada, las prioridades de las dimensiones y el orden en que introduce los datos en los documentos.  

1. Elija el icono ![Bombilla que abre la característica Dígame](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Dimensiones** y luego elija el enlace relacionado.  
2. En la página **Dimensiones**, seleccione la dimensión correspondiente y luego elija la acción **Dimensión predet. tipo cta**.  
3. Rellene una línea para cada nueva dimensión predeterminada que quiera configurar. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!TIP]  
> Si desea requerir una dimensión pero no desea asignar un valor predeterminado a la dimensión, deje el campo **Cód. valor dimensión** en blanco y seleccione **Obligatorio** en el campo **Registro valor**.  

> [!WARNING]  
> Si una cuenta se utiliza en un trabajo por lotes **Ajustar tipo cambio** o **Reg. var. inventario en cont.**, no seleccione **código obligatorio** o **código igual**. Estos procesos no pueden utilizar códigos de dimensión.  

> [!NOTE]  
> Si es necesario tener asignada una dimensión distinta a la dimensión predeterminada para el tipo de cuenta, debe configurar una nueva dimensión predeterminada para la cuenta. La dimensión predeterminada de la cuenta sustituirá a la dimensión predeterminada del tipo de cuenta.  

### <a name="to-set-up-default-dimension-priorities" />Para configurar prioridades de dimensiones predeterminadas

Distintos tipos de cuentas, por ejemplo, una cuenta de cliente y una cuenta de producto, pueden tener dimensiones predeterminadas diferentes. Como resultado, un movimiento podría tener más de una propuesta de dimensión predeterminada. Para evitar este tipo de conflictos, puede aplicar reglas de prioridad a los diversos orígenes.

1. Elija el icono ![Bombilla que abre la característica Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Prioridades de dimensión** y luego elija el enlace relacionado.  
2. En la página **Prioridades dimensión predet.**, en el campo **Cód. origen**, escriba el código de origen para la tabla de movimientos para la que se aplicarán las prioridades de dimensión predeterminadas.  
3. Rellene una línea para cada prioridad de dimensión predeterminada que desee para el código de origen seleccionado.
4. Repita el procedimiento para la cada código de origen para el que quiera configurar prioridades de dimensión predeterminadas.  

> [!IMPORTANT]  
> Si configura dos tablas con la misma prioridad en un mismo código de origen, [!INCLUDE[prod_short](includes/prod_short.md)] selecciona siempre la tabla con el Id. de tabla inferior.  

### <a name="to-set-up-dimension-combinations" />Para configurar combinaciones de dimensión

Para evitar registrar movimientos con dimensiones contradictorias o irrelevantes, puede bloquear o limitar determinadas combinaciones de dos dimensiones. Una dimensión está bloqueada si no es posible registrar ambas dimensiones en el mismo movimiento independientemente de los valores de dimensión. En cambio, una combinación de dimensión limitada impica que puede registrar ambas dimensiones en el mismo movimiento, pero únicamente para determinadas combinaciones de valores de dimensión.

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Combinaciones de dimensiones** y luego elija el enlace relacionado.  
2. En la página **Combinación dimensión**, seleccione el campo de la combinación de dimensión que desee entre las opciones siguientes.  

    |Campo|Descripción|
    |----------------------------------|---------------------------------------|  
    |**Nº limitaciones**|Esta combinación de dimensión no tiene restricciones. Se permiten todos los valores de dimensión.|  
    |**Limitado**|Esta combinación de dimensión tiene determinadas restricciones en función de los valores de dimensión que introduzca. Debe definir las limitaciones en la página **Combinación valor dimensión**.|  
    |**Bloqueado**|Esta combinación de dimensión no está permitida.|  

3. Si selecciona la opción **Limitado**, debe definir las combinaciones de valores de dimensión que están bloqueadas. Para ello, elija el campo para definir la combinación de valores de dimensión.  
4. A continuación, seleccione una combinación de valores de dimensión que esté bloqueada y escriba **Bloqueado** en el campo. Un campo en blanco significa que se permite la combinación de valores de dimensión. Repita el proceso con múltiples dimensiones bloqueadas.  

> [!NOTE]  
> Las mismas dimensiones se repiten tanto en las filas como en las columnas, lo que significa que todas las combinaciones de dimensiones aparecen dos veces. [!INCLUDE[prod_short](includes/prod_short.md)] muestra automáticamente el valor en ambos campos. No puede realizar ninguna selección en los campos de la esquina superior izquierda hacia abajo, ya que esos campos tienen la misma dimensión tanto en las filas como en las columnas.  
>
> La opción seleccionada no será visible hasta que no salga del campo.  
>
> Para mostrar el nombre de la dimensión en lugar del código, seleccione el campo **Muestra nombre columna**.

### <a name="to-set-up-global-and-shortcut-dimensions" />Para configurar dimensiones globales y abreviadas

Las dimensiones globales y abreviadas se pueden utilizar como filtros en cualquier parte de [!INCLUDE[prod_short](includes/prod_short.md)], incluyendo en informes, trabajos por lotes, páginas de movimientos y vistas de análisis. Las dimensiones globales y abreviadas se pueden insertar directamente sin tener que abrir primero la página **Dimensiones**. En las líneas de diario y de documento, puede seleccionar dimensiones globales y abreviadas en un campo de la línea. Puede configurar dos dimensiones globales y ocho abreviadas. Elija las dimensiones que utiliza con más frecuencia.

> [!IMPORTANT]
> La modificación de una dimensión global o abreviada requiere que se actualicen todos los movimientos registrados con la dimensión. Para cambiar una dimensión global, puede usar la función **Cambiar dimen. globales**, pero eso puede llevar mucho tiempo y puede afectar al rendimiento y a las tablas que pueden estar bloqueadas durante la actualización. Asegúrese de que elige cuidadosamente sus dimensiones globales y abreviadas para no tener que cambiarlas más tarde. Para cambiar una dimensión de acceso directo, utilice la acción **Cambiar dimensiones**.
>
> Obtenga más información en la sección [Para cambiar dimensiones globales](finance-dimensions.md#to-change-global-dimensions).

> [!NOTE]
> Al añadir o cambiar una dimensión global o abreviada, se cierra automáticamente la sesión y se vuelve a iniciar para que el nuevo valor esté preparado para su uso.

1. Elija el icono ![Bombilla que abre la característica Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Configuración de contabilidad**, y luego elija el enlace relacionado.
2. En la ficha desplegable **Dimensiones**, rellene los campos. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

#### <a name="to-change-global-dimensions" />Para cambiar las dimensiones globales

Al cambiar una dimensión global o abreviada, se actualizan todos los movimientos registrados con esa dimensión. Debido a que este proceso puede llevar mucho tiempo y afectar al rendimiento, se proporcionan dos modos diferentes de adaptar el proceso al tamaño de la base de datos.  

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Configuración de contabilidad**, y luego elija el enlace relacionado.
2. Elija la acción **Cambiar dimensiones globales**.
3. En la parte superior de la página, seleccione uno de los dos siguientes modos para ejecutar el trabajo por lotes.

    |Opción|Descripción|
    |-|-|
    |**Secuencial**|(Predeterminado) Todo el cambio de dimensión se realiza en una transacción que revierte todos los movimientos a las dimensiones que tenían antes del cambio.<br /><br />Se recomienda esta opción si la empresa tiene relativamente pocos movimientos registrados, en cuyo caso el trabajo por lotes lleva el menor tiempo posible en completarse. El proceso bloquea varias tablas y bloquea a otros usuarios hasta que se realice. Tenga en cuenta que, con bases de datos grandes, el proceso podría no completarse en este modo. En ese caso, use la opción **En paralelo**.|
    |**En paralelo**|El cambio de dimensión ocurre en múltiples sesiones en segundo plano y la operación se divide en múltiples transacciones. Para usar esta opción, active el control de alternancia **Procesamiento en paralelo**. <br /><br />Recomiendamos esta opción para bases de datos grandes o empresas con muchos movimientos registrados porque se tardará el menor tiempo posible en completarse. Tenga en cuenta que, en este modo, el proceso de actualización no se iniciará si hay más de una sesión de base de datos activa.|  

4. En los campos **Cód. dimensión global 1** o **Cód. dimensión global 2**, escriba las nuevas dimensiones. Las dimensiones actuales se muestran en gris detrás de los campos.
5. Según el modo, realice una de las siguientes acciones:
    * En el modo **Secuencial**, elija la acción **Iniciar**.
    * En el modo **Paralelo**, elija la acción **Preparar**.

    La pestaña **Movs. reg.** se rellena con información acerca de las dimensiones que se cambian.
6. Cierre la sesión de [!INCLUDE[prod_short](includes/prod_short.md)] y luego vuelva a iniciar sesión.
7. Elija la acción **Iniciar** para iniciar el procesamiento en paralelo de los cambios de dimensión.

### <a name="example-of-dimension-setup" />Ejemplo de configuración de dimensiones

Supongamos que su empresa desea realizar un seguimiento de las transacciones en función de la estructura organizativa y las ubicaciones geográficas. Para ello, puede configurar dos dimensiones en la página **Dimensiones**:

* **ÁREA**  
* **DEPARTAMENTO**  

| Código | Name | Título código | Título filtro |
| --- | --- | --- | --- |
| ÁREA |Área |Código de área |Filtro Área |
| DPTO |Departamento |Código de departamento |Filtro departamento |

Para **ÁREA**, agregue los siguientes valores de dimensión:

| Código | Nombre | Tipo valor dimensión |
| --- | --- | --- |
| 10 |América |Principio-Total |
| 20 |América del Norte |Estándar |
| 30 |Pacífico |Estándar |
| 40 |Sudamérica |Estándar |
| 50 |América, total |Fin-Total |
| 60 |Europa |Principio-Total |
| 70 |UE |Estándar |
| 80 |No perteneciente a la UE |Estándar |
| 90 |Europa, Total |Fin-Total |

Para las dos áreas geográficas principales, América y Europa, agregue subcategorías para las regiones aplicando sangría a los valores de dimensión. De esta manera podrá elaborar informes sobre ventas o gastos en regiones, y obtener totales de las áreas geográficas más grandes. También puede usar países, regiones, condados o ciudades como valores de dimensión, dependiendo de la empresa.

> [!NOTE]  
> Para configurar una jerarquía, los códigos deben estar en orden alfabético. Esto incluye los códigos de los valores de dimensión que se proporcionan en [!INCLUDE[prod_short](includes/prod_short.md)].  

Para **DEPARTAMENTO**, agregue los siguientes valores de dimensión:

| Código | Nombre | Tipo valor dimensión |
| --- | --- | --- |
| ADMIN |Administración |Estándar |
| PROD |Producción |Estándar |
| CCIAL |Ccial |Estándar |

Con esta configuración, puede agregar las dos dimensiones como las dos dimensiones globales en la página **Configuración de contabilidad**. Esto significa que puede usar ÁREA Y DEPARTAMENTO como filtros para los movimientos de contabilidad, así como en todos los informes. También están disponibles ambas dimensiones globales de forma automática para el uso en líneas de movimientos y cabeceras de documentos, como dimensiones abreviadas.

## <a name="getting-an-overview-of-dimensions-used-multiple-times" />Obtener una visión general de las dimensiones utilizadas varias veces

La página **Dimensiones predet.-Múltiple** especifica cómo un grupo de cuentas usa dimensiones y valores de dimensión. Puede configurar esto resaltando varias cuentas y luego especificando las dimensiones predeterminadas y los valores de dimensión para ellas. Después, la aplicación sugiere estas dimensiones y valores de dimensión siempre que estas cuentas se utilizan, por ejemplo, en una línea del diario. Esto facilita el registro de movimientos, ya que los campos de dimensión se rellenan automáticamente. No obstante, tenga en cuenta también que los valores de dimensión sugeridos se pueden cambiar en, por ejemplo, una línea de diario.

La página **Dimensiones predet.-Múltiple** contiene los campos siguientes:

|Campo|Descripción|
|-----|-----------|  
|**Cód. dimensión**|Muestra todas las dimensiones definidas como dimensiones predeterminadas en una o varias cuentas resaltadas. Seleccionando este campo, puede ver una lista de todas las dimensiones disponibles. Si selecciona una dimensión, esa dimensión se define como la dimensión predeterminada para todas las cuentas resaltadas.|
|**Cód. valor dimensión**|Muestra un valor de dimensión único o el término (Problema). Si en el campo se muestra un valor de dimensión, todas las cuentas resaltadas tendrán el mismo valor de dimensión predeterminado para una dimensión. Si en el campo se muestra el término (Problema), no todas las cuentas resaltadas tendrán el mismo valor de dimensión predeterminado para una dimensión. Al seleccionar el campo **Código de dimensión**, verá una lista de todas las dimensiones que están disponibles para una dimensión. Si selecciona un valor de dimensión, se definirá como el valor de dimensión predeterminado para todas las cuentas resaltadas.|
|**Registro valor**|Muestra una regla de valor al registrar única o el término (Problema). Si en el campo se muestra la regla de valor al registrar, todas las cuentas resaltadas tendrán la misma regla de valor al registrar para un valor de dimensión. Si en el campo se muestra el término (Problema), no todas las cuentas resaltadas tendrán la misma regla de valor al registrar para un valor de dimensión. Al seleccionar el campo **Regisro de valores**, podrá ver una lista de reglas de registro de valores para una dimensión. Si selecciona una regla de registro de valores, se aplicará a todas las cuentas resaltadas.|

## <a name="use-dimensions" />Usar dimensiones

En un documento como un pedido de ventas, puede agregar información de dimensión de una línea en particular y del mismo documento. Así, en la página **Pedido de ventas**, podría introducir valores de dimensión para las dos primeras dimensiones abreviadas en las líneas de venta individuales y luego agregar más información de dimensión si elige el botón **Dimensiones**.  

Si trabaja con un diario, puede agregar información de dimensiones a un movimiento del mismo modo, si ha configurado dimensiones abreviadas como campos directamente en las líneas de diario.  

También puede configurar dimensiones predeterminadas para cuentas o tipos de cuenta, para que esas dimensiones o valores de dimensión se completen automáticamente.

### <a name="to-view-global-dimensions-in-ledger-entry-pages" />Para ver dimensiones globales en páginas de movimientos de contabilidad

El nombre y la definición de las dimensiones globales los establece la empresa. Para ver las dimensiones globales correspondientes a su empresa, abra la página **Configuración contabilidad**.

En una página de movimiento de contabilidad, puede ver si hay dimensiones globales para los movimientos. Las dos dimensiones globales difieren de las otras dimensiones, porque se pueden utilizar como filtros en cualquier lugar de [!INCLUDE[prod_short](includes/prod_short.md)].  

1. Elija el icono ![Bombilla que abre la característica Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Plan de cuentas** y luego elija el vínculo relacionado.  
2. En la página **Plan de cuentas**, seleccione la acción **Movimientos**.  
3. Para ver únicamente los movimientos relevantes, establezca uno o más filtros en la página.  
4. Para ver todas las dimensiones de un movimiento, seleccione el movimiento y luego elija la acción **Dimensiones**.  

> [!NOTE]  
> La página **Dimensiones movimiento** muestra las dimensiones de un movimiento de contabilidad cada vez. Verá que se desplaza por los movimientos de contabilidad, el contenido de la página **Dimensiones movimiento** va cambiando según corresponda.

## <a name="see-related-microsoft-training" />Consultar la [formación de Microsoft](/training/modules/dimensions-dynamics-365-business-central/index) relacionada

## <a name="see-also" />Consulte también .

[Inteligencia empresarial](bi.md)  
[Finanzas](finance.md)  
[Analizar datos por dimensiones](bi-how-analyze-data-dimension.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
