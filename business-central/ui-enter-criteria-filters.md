---
title: Ordenar, buscar y filtrar listas | Documentos de Microsoft
description: Trabaje de manera eficiente en las listas buscando en sus datos, clasificando columnas y refinando los resultados utilizando potentes símbolos de filtrado y atajos de teclado.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: delimit, FlowFilter, totals, limit, advanced
ms.date: 04/01/2019
ms.author: jswymer
ms.openlocfilehash: 5cd8bce29b1973274cda673e22dd07e6b50f830f
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/29/2019
ms.locfileid: "1253958"
---
# <a name="sorting-searching-and-filtering-lists"></a>Ordenar, buscar y filtrar listas
Existen algunos parámetros que puede configurar que le ayudarán a buscar, encontrar y limitar los registros de una lista. Éstos incluyen la ordenación, busqueda y filtrando. Puede aplicar solo algunos o todos a la vez para encontrar o analizar rápidamente sus datos.

> [!TIP]
> Al ver los datos como mosaicos, puede buscar y usar el filtrado básico. Para usar el conjunto completo de potentes funciones para ordenar, buscar y filtrar, elija el icono ![Mostrar como lista](media/ui_show_as_list_icon.png "Flecha izquierda para Mostrar como lista") para mostrar como una lista.

<!--
When you want to search for data, such as customer names, addresses, or product groups, you enter criteria. In search criteria you can use all the numbers and letters that you normally use in the specific field. In addition, you can use special symbols to further filter the results. There are two ways to search: using the Quick Filter or column filters.
-->

## <a name="sorting"></a>Ordenación
La ordenación facilita la obtención rápida de un resumen de sus datos. Si hay varios clientes, por ejemplo, puede elegir ordenarlos por **N.º de cliente**, **Grupo contable cliente**, **Cód. divisa**, **Cód. país/región** o **N.º de registro de impuesto sobre las ventas** para disponer de la vista general que desea.

Para ordenar una lista, puede elegir un texto de cabecera de columna para alternar entre el pedido ascendente y descendente o elegir la flecha pequeña hacia abajo de la cabecera de columna y, a continuación elegir **Ascendente** o **Descendente**.  

> [!NOTE]  
>   El ordenamiento no se admite en imágenes, campos BLOB, FlowFilters ni campos que no pertenecen a una tabla.  

## <a name="searching"></a>Búsqueda
<!--## Searching by using the Quick Filter -->
En la parte superior de cada página de la lista, hay un icono de ![Buscar en la lista](media/ui-search/search-list.png "icono de Buscar en la lista") **Buscar** que proporciona una manera rápida y fácil de reducir los registros en una lista y muestra solo aquellos registros que contienen los datos que le interesa ver.

Para buscar, simplemente seleccione el icono de búsqueda y luego, en el cuadro, escriba el texto que está buscando. Puede escribir letras, números y otros símbolos.

### <a name="fine-tune-the-search"></a>Afinar la búsqueda
En general, la búsqueda intentará hacer coincidir el texto en todos los campos; no distingue entre mayúsculas y minúsculas y coincidirá con el texto colocado en algún lugar del campo (al principio, al final o en el centro).

Sin embargo, puede realizar una búsqueda más exacta utilizando los siguientes caracteres especiales:

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

> [!TIP]
> Puede presionar F3 para activar y desactivar el cuadro de búsqueda. Para obtener más información, consulte [Métodos abreviados de teclado](keyboard-shortcuts.md#KeyboardFilter).

## <a name="Filtering"> </a>Filtrado
El filtrado proporciona una forma más avanzada y versátil de controlar qué registros se muestran en una lista. Existen dos diferencias principales entre la búsqueda y el filtrado, como se describe en la tabla siguiente.

|| **Búsqueda** | **Filtrado** |
|--|----------|------------|
| **Campos aplicables** | Busca en todos los campos que están visibles en la página. | Filtra uno o más campos individualmente, los selecciona desde cualquier campo de la tabla, incluidos los campos que no están visibles en la página. |
| **Coincidencia** | Muestra registros con campos que coinciden con el texto de búsqueda, independientemente de las mayúsculas o la ubicación de ese texto. | Muestra los registros en los que el campo coincide exactamente con el filtro y distingue entre mayúsculas y minúsculas, a menos que se introduzcan símbolos de filtrado especiales.

El filtrado le permite mostrar registros de cuentas o clientes específicos, fechas, importes y otra información especificando criterios de filtro. Únicamente se mostrarán los registros que coincidan con los criterios. Si especifica criterios para varios campos, solo se mostrarán los registros que coincidan con todos los criterios.

### <a name="working-in-the-filter-pane"></a>Trabajar en el panel de filtros

Para mostrar el panel de filtros, seleccione ![Icono Panel de filtros](media/open-filter-pane-icon.png "Icono Panel de filtros") en la parte superior de la lista o pulse **Mayús+F3**. Para las listas del Área de trabajo, también puede elegir la flecha hacia abajo cerca del título de la página en la barra de navegación que se encuentra sobre la lista, y luego seleccionar **Mostrar panel de filtros**, tal como se muestra aquí:

![Mostrar panel de filtros](media/open-filter-pane.png "Mostrar panel de filtros")

El panel de filtros muestra los filtros actuales para una lista y le permite configurar sus propios filtros personalizados en uno o más campos. La siguiente ilustración muestra un panel de filtros de ejemplo para una lista de Ofertas de venta.

![Vista general del panel de filtros ](media/filter-pane-overview.png "Icono de Filtros")

Un panel de filtros se divide en tres secciones: **Vistas**, **Filtrar lista por** y **Filtrar totales por**:

- **Vistas**

  Algunas listas incluyen la sección **Vistas**. Las vistas son variaciones de la lista que se han preconfigurado con filtros. Para cambiar a una vista diferente de su lista, simplemente seleccione otro enlace. Puede cambiar temporalmente los filtros en una vista, pero no se guardarán de forma permanente.

- **Filtrar lista por**

  La sección **Filtrar lista por** es donde se agregan filtros en campos específicos para reducir el número de registros mostrados. Para agregar un filtro, seleccione **+ Filtro**, seleccione el campo que desea filtrar desde cualquier campo de la tabla e introduzca los criterios de filtro en el cuadro.

- **Filtrar totales por**

  Algunas listas que muestran campos calculados, como cantidades e importes, incluyen la sección **Filtrar totales por**, donde puede ajustar varias dimensiones que influyen en los cálculos. Por ejemplo, puede analizar rápidamente su plan de cuentas filtrando los importes a un período específico, o puede ver los totales de los pedidos de ventas solo de un almacén específico.

  Para agregar un filtro, seleccione **+ Filtro**, seleccione una de las dimensiones predefinidas y luego agregue los criterios de filtro en el cuadro.

  > [!NOTE]
  > FlowFilters es el encargado de controlar los filtros de la sección **Filtrar totales por** en el diseño de la página. Para obtener información técnica, vea [FlowFilters](https://docs.microsoft.com/en-us/dynamics365/business-central/dev-itpro/developer/devenv-flowfilter-overview).


### <a name="entering-filter-criteria-in-the-filter-pane"></a>Introducción de criterios de filtros en el panel de filtros
Para seleccionar un campo para filtrar, realice una de las siguientes acciones:
  - En el panel de filtros, seleccione **+ Campo**. Escriba el nombre del campo que desea filtrar o elija un campo del menú que muestra todos los campos de la tabla.

  - En un encabezado de columna, elija la flecha hacia abajo y luego seleccione **Filtro...**. Se abrirá el panel de filtros y se agregará la columna al panel.

Ya puede escribir o seleccionar sus criterios de filtro en el cuadro. El tipo de campo que filtra determina qué criterios puede especificar. Por ejemplo, filtrar un campo que tiene valores fijos solo le permitirá elegir entre esos valores. Para obtener más información sobre símbolos de filtro especiales, consulte [Criterios de filtro](#FilterCriteria) y [Tokens de filtro](#FilterTokens).

Las columnas que ya tienen filtros se indican mediante el ![icono Filtro](media/ui-search/filter-icon.png "icono Filtro") en el encabezado de la columna. Para eliminar un filtro, seleccione el encabezado de la columna, luego elija **Borrar filtro**.


### <a name="entering-filter-criteria-without-using-the-filter-pane"></a>Introducción de criterios de filtros sin el panel de filtros
Puede especificar filtros simples directamente dentro de la lista sin tener que usar el panel de filtros.
Con cualquier campo seleccionado en una fila, use el método abreviado de teclado **Alt+F3** para mostrar solo los registros que tienen el mismo valor. A continuación puede seleccionar otro campo y usar el mismo acceso directo nuevamente para continuar refinando los filtros. Si el campo seleccionado ya está filtrado, la combinación **Alt+F3** borrará ese filtro.

> [!TIP]
> Acelere la búsqueda y el análisis de sus datos utilizando combinaciones de atajos de teclado. Por ejemplo, seleccione un campo, use **Mayús+Alt+F3** para agregar ese campo al panel de filtros, escriba los criterios de filtro, use **Ctrl+Intro** para volver a las filas, seleccione otro campo y use **Alt+F3** para filtrar ese valor.
Para obtener más información, consulte [Métodos abreviados de teclado](keyboard-shortcuts.md#KeyboardFilter).


## <a name="FilterCriteria"> </a>Criterios y símbolos de filtro
Al introducir criterios, puede usar todos los números y las letras que normalmente se emplean en un campo. También puede usar símbolos especiales para filtrar aún más los resultados. En las tablas siguientes se muestran los símbolos que se pueden usar en los filtros. Para obtener más información sobre fechas y horas, también puede consultar [Trabajar con fechas y horas del calendario](ui-enter-date-ranges.md).

> [!IMPORTANT]  
>  Puede haber instancias donde los valores de campo contengan los siguientes símbolos y desee filtrarlos. Para ello, debe incluir la expresión de filtro que contiene el símbolo entre comillas ("). Por ejemplo, si desea filtrar en los registros que comienzan por el texto *S&R*, la expresión de filtro es `'S&R*'`.  

### <a name="-interval"></a>(..) Intervalo

|Ejemplo|Registros mostrados|  
|-----------------------|-----------------------|  
|`1100..2100`|Números del 1100 al 2100.|  
|`..2500`|Hasta la 2500 inclusive|  
|`..12 31 00`|Fechas hasta el 31 12 00, inclusive.|  
|`P8..`|Información correspondiente al ejercicio económico 8 en adelante|  
|`..23`|Desde la fecha inicial hasta 23-mes actual-año actual 23:59:59|  
|`23..`|Desde 23-mes actual-año actual 0:00:00 hasta la hora final|  
|`22..23`|Desde 22-mes actual-año actual 0:00:00 hasta 23-mes actual-año actual 23:59:59|  

### <a name="124-eitheror"></a>(&#124;) O/o  

|Ejemplo|Registros mostrados|  
|-----------------------|-----------------------|  
|`1200|1300`|Números con 1200 ó 1300|  

### <a name="-not-equal-to"></a>(<>) Distinto  

|Ejemplo|Registros mostrados|  
|-----------------------|-----------------------|  
|`<>0`|Todos los números, excepto el 0<br /><br /> La opción SQL Server permite combinar este símbolo con una expresión de caracteres comodín. Por ejemplo, <>A* significa distinto de cualquier texto que empiece por A.|  

### <a name="-greater-than"></a>(>) Mayor de  

|Ejemplo|Registros mostrados|  
|-----------------------|-----------------------|  
|`>1200`|Números mayores que 1200|  

### <a name="-greater-than-or-equal-to"></a>(>=) Mayor o igual a  

|Ejemplo|Registros mostrados|  
|-----------------------|-----------------------|  
|`>=1200`|Números mayores o igual que 1200|  

### <a name="-less-than"></a>(<) Menor de  

|Ejemplo|Registros mostrados|  
|-----------------------|-----------------------|  
|`<1200`|Números menores que 1200|  

### <a name="-less-than-or-equal-to"></a>(<=) Menor o igual que  

|Ejemplo|Registros mostrados|  
|-----------------------|-----------------------|  
|`<=1200`|Números menores o iguales que 1200|  

### <a name="-and"></a>(&) y  

|Ejemplo|Registros mostrados|  
|-----------------------|-----------------------|  
|`>200&<1200`|Números mayores de 200 e inferiores a 1200|  

### <a name="-an-exact-character-match"></a>(") Una coincidencia exacta de carácter  

|Ejemplo|Registros mostrados|  
|-----------------------|-----------------------|  
|`'man'`|Texto que coincide exactamente con man y distingue mayúsculas de minúsculas.|  

### <a name="-case-insensitive"></a>(@) Distinción entre mayúsculas y minúsculas  

|Ejemplo|Registros mostrados|  
|-----------------------|-----------------------|  
|`@man*`|Texto que empieza por man y no distingue mayúsculas de minúsculas.|  

### <a name="-an-indefinite-number-of-unknown-characters"></a>(*) Un número indefinido de caracteres desconocidos (quizás ninguno)

|Ejemplo|Registros mostrados|  
|-----------------------|-----------------------|  
|`*Co*`|Texto que contenga “Co” y es con diferenciación de mayúsculas y minúsculas.|  
|`*Co`|Texto que termine con “Co” y es con diferenciación de mayúsculas y minúsculas.|  
|`Co*`|Texto que empiece por “Co” y es con diferenciación de mayúsculas y minúsculas.|  

> [!NOTE]  
>   No puede utilizar `*` al filtrar en los campos de opción (enumeración), como el campo **Estado** en los pedidos de venta. Para especificar un filtro para este tipo de campo, puede especificar el valor numérico como parámetro de filtrado. Por ejemplo, en el campo **Estado** de un pedido de venta que tenga los valores **Abierto**, **Lanzado**, **Aprobación pendiente** y **Prepago pendiente**, utilice los valores `0`, `1`, `2` y `3` para filtrar para estas opciones.

### <a name="-one-unknown-character"></a>(?) Un carácter desconocido  

|Ejemplo|Registros mostrados|  
|-----------------------|-----------------------|  
|`Hans?n`|Texto como Mendoza o Mendosa|  

### <a name="combined-format-expressions"></a>Expresiones de formato combinadas  

|Ejemplo|Registros mostrados|  
|-----------------------|-----------------------|  
|`5999|8100..8490`|Incluye todos los registros cuyo número sea 5999 o un número entre 8100 y 8490.|  
|`..1299|1400..`|Incluye los registros cuyo número sea menor o igual que 1299 o un número igual o mayor que 1400|  
|`>50&<100`|Incluye los registros cuyo número sea mayor que 50 y menor que 100.|  


## <a name="FilterTokens"> </a>Tokens de filtro
Al introducir criterios de filtro, también puede escribir palabras que tengan un significado especial, lo que se conoce como tokens de filtro. Después de introducir la palabra token, la palabra se reemplaza por el valor o valores que representa. Esto facilita el filtrado al reducir la necesidad de ir a otras páginas para buscar los valores que desea agregar a su filtro. En las tablas siguientes se describen algunos de los tokens que puede escribir como criterios de filtro.

> [!TIP]
> Su organización puede usar tokens personalizados. Para obtener información sobre el conjunto completo de tokens disponibles o para agregar más tokens personalizados, hable con su administrador. Para obtener información técnica, consulte [Agregar tokens de filtro](/dynamics365/business-central/dev-itpro/developer/devenv-adding-filter-tokens).


### <a name="me-or-userid-records-assigned-to-you"></a>(%me o %userid) Registros que se le han asignado

Utilice `%me` o `%userid` cuando filtre campos que contengan el ID de usuario, como el campo **Asignado a ID de usuario**, para mostrar todos los registros que se le asignaron.

|Ejemplo|Registros mostrados|  
|-----------------------|-----------------------|  
|`%me`<br />o<br />`%userid`|Registros que se han asignado a su cuenta. |  

### <a name="mycustomers-customers-in-my-customers"></a>(%mycustomers) Clientes en Mis clientes

Use `%mycustomers` en el campo de cliente **No** para mostrar todos los registros de los clientes que se incluyen en la lista **Mis clientes** en su Área de trabajo.

|Ejemplo|Registros mostrados|  
|-----------------------|-----------------------|  
|`%mycustomers`|Clientes en **Mis clientes** en el Área de trabajo. |  

### <a name="myitems-items-in-my-items"></a>(%myitems) Artículos en Mis artículos

Use `%myitems` en el campo de artículo **No** para mostrar todos los registros de los artículos que se incluyen en la lista **Mis artículos** en su Área de trabajo.

|Ejemplo|Registros mostrados|  
|-----------------------|-----------------------|  
|`%myitems`|Artículos en **Mis artículos** en el Área de trabajo. |  

### <a name="myvendors-vendors-in-my-vendors"></a>(%myvendors) Proveedores en Mis proveedores

Use `%myvendors` en el campo de proveedor **No** para mostrar todos los registros de los proveedores que se incluyen en la lista **Mis proveedores** en su Área de trabajo.

|Ejemplo|Registros mostrados|  
|-----------------------|-----------------------|  
|`%myvendors`|Proveedores en **Mis proveedores** en el Área de trabajo. |  


## <a name="see-also"></a>Consulte también
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Preguntas comunes acerca de Buscar y filtrar](ui-search-filter-faq.md)
