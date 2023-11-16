---
title: 'Ordenar, buscar y filtrar listas'
description: 'Trabaje de manera eficiente en las listas buscando en sus datos, clasificando columnas y refinando los resultados utilizando símbolos de filtrado y atajos de teclado.'
author: jswymer
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'delimit, FlowFilter, totals, limit, advanced'
ms.search.form: null
ms.date: 10/30/2023
ms.author: jswymer
---
# Ordenar, buscar y filtrar

Existen algunos parámetros que puede configurar que le ayudarán a buscar, encontrar y limitar los registros de una lista, un informe o un XMLport Estos incluyen la ordenación, la búsqueda y el filtrado. Puede aplicar solo algunos o todos a la vez para encontrar o analizar rápidamente sus datos.

[!INCLUDE [about-ui-learn](includes/about-ui-learn.md)]

Para informes y XMLports, como en las listas, puede establecer filtros para delimitar qué datos se incluirán en el informe o XMLport, pero no puede ordenar y buscar.

> [!TIP]
> Al ver los datos como mosaicos, puede buscar y usar el filtrado. Para usar el conjunto completo de potentes funciones para ordenar, buscar y filtrar, elija el icono ![Mostrar como lista.](media/ui_show_as_list_icon.png "Flecha izquierda de Mostrar como lista") para ver los registros como una lista.

<!--
When you want to search for data, such as customer names, addresses, or product groups, you enter criteria. In search criteria, you can use all the numbers and letters that you normally use in the specific field. In addition, you can use special symbols to further filter the results. There are two ways to search: using the Quick Filter or column filters.
-->

## Ordenación

La ordenación facilita la obtención rápida de un resumen de sus datos. Por ejemplo, si hay varios clientes, por ejemplo, podría elegir ordenarlos por **N.º de cliente**, **Cód. divisa** o **Cód. país/región** para disponer de la vista general que desea.

Para ordenar una lista, puede:

- Elegir un texto de encabezado de columna para alternar entre orden ascendente y descendente, o
- Elegir la flecha desplegable en el encabezado de la columna, luego elija la acción **Ascendente** o **Descendiendo**.  

> [!NOTE]  
> El ordenamiento no se admite en imágenes, campos BLOB, FlowFilters ni campos que no pertenecen a una tabla.  

## Búsqueda

<!--## Searching by using the Quick Filter -->
En la parte superior de cada página de lista, hay una ![Lista de búsqueda.](media/ui-search/search-list.png "Icono de lista de búsqueda") acción **Buscar** que proporciona una manera rápida y fácil de reducir los registros en una lista y muestra solo aquellos registros que contienen los datos que le interesa ver.

Para buscar, solo elija la acción **Buscar** y, a continuación, en el cuadro, escriba el texto que está buscando. Puede escribir letras, números y otros símbolos.

En general, la búsqueda intentará hacer coincidir el texto en todos los campos. No distingue entre mayúsculas y minúsculas y coincidirá con el texto colocado en algún lugar del campo: al principio, al final o en el centro.

> [!TIP]
> Puede seleccionar <kbd>F3</kbd> para activar y desactivar el cuadro de búsqueda. Para obtener más información, consulte [Métodos abreviados de teclado](keyboard-shortcuts.md#KeyboardFilter).

> [!NOTE]  
> La búsqueda no coincidirá con valores en imágenes, campos BLOB, FlowFilters, FlowFields y otros campos que no forman parte de una tabla.


### Ajuste de los criterios de búsqueda con filtro

Puede realizar una búsqueda más exacta utilizando operadores de filtro, expresiones y tokens de filtro. A diferencia del filtrado, estos se aplican en todos los campos cuando se utilizan en el cuadro de búsqueda, lo que los hace menos eficientes que el filtrado.

- Para buscar solo valores de campo que coincidan exactamente con el texto completo y el caso, coloque el texto de búsqueda entre comillas simples `''` (por ejemplo, `'man'`).

- Para buscar valores de campo que comiencen con un determinado texto y coincidan con el caso, coloque `*` después del texto de búsqueda (por ejemplo, `man*`).

- Para buscar valores de campo que acaben con un determinado texto y coincidan con el caso, coloque `*` antes del texto de búsqueda (por ejemplo, `*man`).

- Cuando se utiliza `''` o `*`, la búsqueda distingue entre mayúsculas y minúsculas. Si desea que la búsqueda no distinga entre mayúsculas y minúsculas, coloque `@` antes del texto de búsqueda (por ejemplo, `@man*`).

En la tabla siguiente se muestran algunos ejemplos de cómo puede utilizar la búsqueda.

|Criterios de búsqueda|Búsquedas…|
|---------------|----------|
|`man`<br />o <br />`Man`|Todos los registros con los campos que contienen el texto **man**, independientemente de las mayúsculas y minúsculas. Por ejemplo, **Manchester**, **manual** o **Norman**. |
|`'Man'`|Todos los registros con los campos que contienen solo el texto **Man** y coinciden las mayúsculas y minúsculas.|
|`Man*`|Todos los registros con los campos que empiezan por <b>Man</b> y coinciden las mayúsculas y minúsculas. Por ejemplo, **Manchester** pero no **manual** o **Norman**.|
|`@Man*`|Todos los registros con los campos que empiezan por **man** independientemente de las mayúsculas y minúsculas. Por ejemplo, **Manchester** y **manual** pero no **Norman**.|
|`@*man`|Todos los registros que acaban por **man** independientemente de las mayúsculas y minúsculas. Por ejemplo, **Norman** pero no **Manchester** o **manual**.|


## <a name="filtering"></a>Filtrado

El filtrado proporciona una forma más avanzada y versátil de controlar qué registros se incluyen en una lista o se incluyen en un informe o XMLport. Existen dos diferencias principales entre la búsqueda y el filtrado, como se describe en la tabla siguiente.

|| **Búsqueda** | **Filtrado** |
|--|----------|------------|
| **Campos aplicables** | Busca en todos los campos que están visibles en la página. | Filtra uno o más campos individualmente, los selecciona desde cualquier campo de la tabla, incluidos los campos que no están visibles en la página. |
| **Coincidencia** | Muestra registros con campos que coinciden con el texto de búsqueda, independientemente de las mayúsculas o la ubicación del texto en el campo. | Muestra los registros en los que el campo coincide exactamente con el filtro, y distingue entre mayúsculas y minúsculas, a menos que se introduzcan símbolos de filtrado especiales.

El filtrado le permite mostrar registros de cuentas o clientes específicos, fechas, importes y otra información especificando criterios de filtro. Solo los registros que coinciden con los criterios se muestran en la lista o se incluyen en el informe, trabajo por lotes o XMLport. Si especifica criterios para varios campos, solo se mostrarán los registros que coincidan con todos los criterios.

Para las listas, los filtros se muestran en un panel de filtro que aparece a la izquierda de la lista cuando lo activa. Para informes, trabajos por lotes y XMLports, los filtros están visibles directamente en la página de solicitud.

### Filtrado con campos de opción

Para los campos "normales" que contienen datos, fecha de configuración o datos de negocio, puede establecer filtros seleccionando datos y escribiendo valores de filtro, y puede usar símbolos para definir criterios de filtro avanzados. Para obtener más información, vea [Introducción de criterios de filtros](ui-enter-criteria-filters.md#entering-filter-criteria).

Sin embargo, para campos de tipo **Opción**, solo puede establecer un filtro seleccionando una o más opciones de una lista desplegable de las opciones disponibles. Un ejemplo de un campo de opción es el campo **Estado** en la página **Pedidos de venta**.

> [!NOTE]
> Cuando selecciona varias opciones como valor de filtro, la relación entre las opciones se define como *O*. Por ejemplo, si selecciona las casillas **Abierto** y **Lanzado** en el campo de filtro **Estado** en la página **Pedidos de venta**, significa que se muestran los pedidos de venta que están abiertos o lanzados.

### Configuración de filtros en listas

En las listas, los filtros se establecen utilizando el panel de filtro. Para mostrar el panel de filtro de una lista, elija la flecha desplegable situada junto al nombre de la página y luego elija la acción **Mostrar panel de filtros**. Alternativamente, seleccione <kbd>Mayús</kbd>+<kbd>F3</kbd>.

Para mostrar el panel de filtro de una columna de una lista, elija la flecha desplegable y luego elija la acción **Filtrar**. Alternativamente, seleccione <kbd>Mayús</kbd>+<kbd>F3</kbd>. El panel de filtro se abre con la columna seleccionada que se muestra como un campo de filtro en la sección **Filtrar lista por**.

El panel de filtro muestra los filtros actuales para una lista y le permite configurar sus propios filtros personalizados en uno o más campos eligiendo la acción **+ Filtrar**.

 Un panel de filtros se divide en tres secciones: **Vistas**, **Filtrar lista por** y **Filtrar totales por**:

- **Vistas**

  Algunas listas incluyen la sección **Vistas**. Las vistas son variaciones de la lista que se han preconfigurado con filtros. Puede definir y guardar tantas vistas como desee por lista. Las vistas estarán disponibles para usted en cualquier dispositivo en el que inicie sesión. Para obtener más información, consulte [Guardar y personalizar vistas de lista](ui-views.md).

- **Filtrar lista por**

  Esta sección es donde se agregan filtros en campos específicos para reducir el número de registros mostrados. Para agregar un filtro, elija la acción **Filtro**. Después, para agregar un filtro, elija la acción + Filtrar, escriba el nombre del campo por el que desea filtrar la lista o elija un campo de la lista desplegable.

- **Filtrar totales por**

  Algunas listas que muestran campos calculados, como cantidades e importes, incluyen la sección **Filtrar totales por**, donde puede ajustar varias dimensiones que influyen en los cálculos. Para agregar un filtro, elija la acción **Filtro**. Después, para agregar un filtro, elija la acción + Filtrar, escriba el nombre del campo por el que desea filtrar la lista o elija un campo de la lista desplegable.

  > [!NOTE]
  > FlowFilters es el encargado de controlar los filtros de la sección **Filtrar totales por** en el diseño de la página. Para obtener información técnica, vea [FlowFilters](/dynamics365/business-central/dev-itpro/developer/devenv-flowfilter-overview).

Puede establecer un filtro simple directamente en una lista mediante el panel de filtro, es decir, un filtro que muestra solo registros con el mismo valor que en la celda seleccionada. Seleccione una celda de la lista, elija la flecha desplegable y luego elija la acción **Filtrar a este valor**. Alternativamente, seleccione <kbd>Alt</kbd>+<kbd>F3</kbd>.

### Configuración de filtros en informes, trabajos por lotes y XMLports

Para informes y XMLports, los filtros están visibles directamente en la página de solicitud. La página de solicitud muestra los últimos filtros utilizados de acuerdo con su selección en el campo **Usar valores predeterminados de**. Para obtener más información, consulte [Usar la configuración guardada](ui-work-report.md#SavedSettings).

La sección principal **Filtrar** muestra los campos de filtro predeterminados que usa para delimitar qué registros incluir en el informe o XMLport. Para agregar un filtro, elija la acción **Filtro**. Después, para agregar un filtro, elija la acción + Filtrar, escriba el nombre del campo por el que desea filtrar la lista o elija un campo de la lista desplegable.

En la sección **Filtrar totales por**, puede ajustar varias dimensiones que influyen en los cálculos en el informe o XMLport. Para agregar un filtro, elija la acción **Filtro**. Después, para agregar un filtro, elija la acción + Filtrar, escriba el nombre del campo por el que desea filtrar la lista o elija un campo de la lista desplegable.

## Introducción de criterios de filtros

Tanto en el panel de filtro como en una página de solicitud, introduzca sus criterios de filtro en el cuadro situado debajo del campo de filtro.

El tipo de campo de filtro determina qué criterios puede especificar. Por ejemplo, filtrar un campo que tiene valores fijos solo le permitirá elegir entre esos valores. Para obtener más información sobre símbolos de filtro especiales, consulte [Criterios de filtro](#FilterCriteria) y [Tokens de filtro](#FilterTokens).

Las columnas que ya tienen filtros se indican mediante el icono ![Icono Filtro.](media/ui-search/filter-icon.png "Icono de filtro") el encabezado de la columna. Para eliminar un filtro, seleccione la flecha desplegable y, a continuación, elija la acción **Borrar filtro**.

> [!TIP]
> Acelere la búsqueda y el análisis de sus datos utilizando combinaciones de atajos de teclado. Por ejemplo, seleccione un campo, use <kbd>Mayús</kbd>+<kbd>Alt</kbd>+<kbd>F3</kbd> para agregar ese campo al panel de filtros, escriba los criterios de filtro, use <kbd>Ctrl</kbd>+<kbd>Entrar</kbd> para volver a las filas, seleccione otro campo y use <kbd>Alt</kbd>+<kbd>F3</kbd> para filtrar ese valor. Para obtener más información, consulte [Métodos abreviados de teclado](keyboard-shortcuts.md#KeyboardFilter).

### <a name="FilterCriteria"> </a>Criterios y operadores de filtro

Al introducir criterios, puede usar todos los números y las letras que normalmente se emplean en un campo. Pero también hay un conjunto de símbolos especiales que puede usar como operadores para filtrar aún más los resultados. Las siguientes secciones describen estos símbolos y cómo usarlos como operadores en filtros.

> [!TIP]
> Para obtener más información sobre el filtrado de fecha y hora, consulte [Trabajar con fechas y horas del calendario](ui-enter-date-ranges.md).

> [!IMPORTANT]
> - Puede haber situaciones en las que el valor por el que desea filtrar contiene un símbolo que es un operador. Para obtener más información sobre cómo manejar estas situaciones, consulte [Filtrado por valores que contienen símbolos](#symbols) para obtener más instrucciones sobre cómo manejar esta situación.
>
> - Si hay más de 200 operadores en un solo filtro, el sistema agrupará automáticamente algunas expresiones entre paréntesis `()` con el fin de procesarlas. Esto no tiene ningún efecto en el filtro ni en los resultados.  

#### (..) Intervalo

|Ejemplo|Registros mostrados|  
|-----------------------|-----------------------|  
|`1100..2100`|Números del 1100 al 2100.|  
|`..2500`|Hasta la 2500 inclusive|  
|`..12 31 00`|Fechas hasta el 31 12 00, inclusive.|  
|`P8..`|Información correspondiente al ejercicio económico 8 y posteriores|  
|`..23`|Desde la fecha inicial hasta 23-mes actual-año actual 23:59:59|  
|`23..`|Desde 23-mes actual-año actual 0:00:00 hasta la hora final|  
|`22..23`|Desde 22-mes actual-año actual 0:00:00 hasta 23-mes actual-año actual 23:59:59| 

> [!TIP]
> Si está usando un teclado numérico, la tecla del separador decimal puede emitir un carácter distinto al punto (.). Para pasar a un punto, seleccione las teclas <kbd>Alt</kbd>+<kbd>Separador decimal</kbd> del teclado numérico. Cuando quiera volver a cambiar, seleccione de nuevo <kbd>Alt</kbd>+<kbd>Separador decimal</kbd>. Para más información, consulte [Configurar el separador decimal utilizado por los teclados numéricos](ui-enter-data.md#decimal).

#### (&#124;) O/o

|Ejemplo|Registros mostrados|  
|-----------------------|-----------------------|  
|`1200|1300`|Números con 1200 ó 1300|  

#### (<>) Distinto  

|Ejemplo|Registros mostrados|  
|-----------------------|-----------------------|  
|`<>0`|Todos los números, excepto el 0<br /><br /> La opción SQL Server permite combinar este símbolo con una expresión de caracteres comodín. Por ejemplo, <>A* significa distinto de cualquier texto que empiece por A.|  

#### (>) Mayor de  

|Ejemplo|Registros mostrados|  
|-----------------------|-----------------------|  
|`>1200`|Números mayores que 1200|  

#### (>=) Mayor o igual a  

|Ejemplo|Registros mostrados|  
|-----------------------|-----------------------|  
|`>=1200`|Números mayores o igual que 1200|  

#### (<) Menor de  

|Ejemplo|Registros mostrados|  
|-----------------------|-----------------------|  
|`<1200`|Números menores que 1200|  

#### (<=) Menor o igual que  

|Ejemplo|Registros mostrados|  
|-----------------------|-----------------------|  
|`<=1200`|Números menores o iguales que 1200|  

#### (&) y  

|Ejemplo|Registros mostrados|  
|-----------------------|-----------------------|  
|`>200&<1200`|Números mayores de 200 e inferiores a 1200|  

#### (") Una coincidencia exacta de carácter  

|Ejemplo|Registros mostrados|  
|-----------------------|-----------------------|  
|`'man'`|Texto que coincide exactamente con **man** y distingue mayúsculas de minúsculas.|  
|`''`|Texto que está vacío.|  

#### (@) Distinción entre mayúsculas y minúsculas  

|Ejemplo|Registros mostrados|  
|-----------------------|-----------------------|  
|`@man*`|Texto que empieza por **man** y no distingue mayúsculas de minúsculas.|  

#### (*) Un número indefinido de caracteres desconocidos (quizás ninguno)

|Ejemplo|Registros mostrados|  
|-----------------------|-----------------------|  
|`*Co*`|Texto que contenga **Co** y es con diferenciación de mayúsculas y minúsculas.|  
|`*Co`|Texto que termine con **Co** y es con diferenciación de mayúsculas y minúsculas.|  
|`Co*`|Texto que empiece por **Co** y es con diferenciación de mayúsculas y minúsculas.|  

#### (?) Un carácter desconocido  

|Ejemplo|Registros mostrados|  
|-----------------------|-----------------------|  
|`Hans?n`|Texto como **Mendoza** o **Mendosa**|  

#### Expresiones de formato combinadas  

|Ejemplo|Registros mostrados|  
|-----------------------|-----------------------|  
|`5999|8100..8490`|Incluye todos los registros cuyo número sea 5999 o un número entre 8100 y 8490.|  
|`..1299|1400..`|Incluye los registros cuyo número sea menor o igual que 1299 o un número igual o mayor que 1400|  
|`>50&<100`|Incluye los registros cuyo número sea mayor que 50 y menor que 100.|  

### <a name="symbols"></a>Filtrado por valores que contienen símbolos

Puede haber casos en los que los valores de campo contengan uno de los siguientes símbolos:

- &
- (
- )
- =
- &#124;

Si desea filtrar por cualquiera de estos símbolos, coloque la expresión de filtro entre comillas sencillas (`'<expression with symbol>'`). Por ejemplo, si desease filtrar en los registros que comienzan por el texto *J & V*, la expresión de filtro sería `'J & V*'`.

Este requisito no es necesario para otros símbolos.

### <a name="FilterTokens"> </a>Tokens de filtro

Al introducir criterios de filtro, también puede escribir palabras que tengan un significado especial, lo que se conoce como tokens de filtro. Después de introducir la palabra token, la palabra se reemplaza por el valor o valores que representa. Los tokens de filtro facilitan el filtrado al reducir la necesidad de ir a otras páginas para buscar los valores que desea agregar a su filtro. En las tablas siguientes se describen algunos de los tokens que puede escribir como criterios de filtro.

> [!TIP]
> Su organización puede usar tokens personalizados. Para obtener información sobre el conjunto completo de tokens disponibles o para agregar más tokens personalizados, hable con su administrador. Para obtener información técnica, consulte [Agregar tokens de filtro](/dynamics365/business-central/dev-itpro/developer/devenv-adding-filter-tokens).

#### (%me o %userid) Registros que se le han asignado

Utilice `%me` o `%userid` cuando filtre campos que contengan el ID de usuario, como el campo **Asignado a ID de usuario**, para mostrar todos los registros que se le asignaron.

|Ejemplo|Registros mostrados|  
|-----------------------|-----------------------|  
|`%me`<br />o<br />`%userid`|Registros que se han asignado a su cuenta. |  

#### (%mycustomers) Clientes en Mis clientes

Use `%mycustomers` en el campo de cliente **No** para mostrar todos los registros de los clientes que se incluyen en la lista **Mis clientes** en su Área de trabajo.

|Ejemplo|Registros mostrados|  
|-----------------------|-----------------------|  
|`%mycustomers`|Clientes en **Mis clientes** en el Área de trabajo. |  

#### (%myitems) Artículos en Mis artículos

Use `%myitems` en el campo de artículo **No** para mostrar todos los registros de los artículos que se incluyen en la lista **Mis artículos** en su Área de trabajo.

|Ejemplo|Registros mostrados|  
|-----------------------|-----------------------|  
|`%myitems`|Artículos en **Mis artículos** en el Área de trabajo. |  

#### (%myvendors) Proveedores en Mis proveedores

Use `%myvendors` en el campo de proveedor **No** para mostrar todos los registros de los proveedores que se incluyen en la lista **Mis proveedores** en su Área de trabajo.

|Ejemplo|Registros mostrados|  
|-----------------------|-----------------------|  
|`%myvendors`|Proveedores en **Mis proveedores** en el Área de trabajo. |  

## Consulte también .

[Preguntas frecuentes sobre búsqueda y filtrado](ui-search-filter-faq.yml)  
[Guardar y personalizar vistas de lista](ui-views.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
