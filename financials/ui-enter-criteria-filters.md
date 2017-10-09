---
title: Buscar datos y especificar criterios de filtrado | Documentos de Microsoft
description: "Describe cómo trabajar con filtros, como el filtro rápido, para redefinir los resultados que obtiene al buscar datos."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: delimit, FlowFilter
ms.date: 03/29/2017
ms.author: solsen
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 11d7ef56e980ba263dba6328b2f2f08b86410242
ms.contentlocale: es-es
ms.lasthandoff: 09/22/2017

---
# <a name="searching-filtering-and-sorting-data"></a>Buscar, filtrar y ordenar datos
Existen algunos parámetros que puede hacer que le ayudarán a encontrar, identificar y a buscar los registros de una lista. Éstos incluyen la ordenación, busqueda y filtrando.

Cuando quiera buscar datos, como nombres de cliente, direcciones o grupos de productos, puede introducir los criterios. En los criterios de búsqueda puede usar todos los números y las letras que normalmente se emplean en un campo específico. También puede usar símbolos especiales para filtrar aún más los resultados. Existen dos formas de buscar: usando filtros rápidos o filtros de columna.

## <a name="sorting"></a>Ordenación
La ordenación facilita la obtención rápida de un resumen de sus datos. Si hay varios clientes, por ejemplo, puede elegir ordenarlos por **N.º de cliente**, **Grupo contable cliente**, **Cód. divisa**, **Cód. país/región** o **N.º de registro de impuesto sobre las ventas** para disponer de la vista general que desea.

Para ordenar una lista, puede elegir o un texto de cabecera de columna para alternar entre la el pedido decreciente y ascendente o elegir la pequeña flecha hacia abajo de la cabecera de columna y, a continuación elegir **Ascendente** o **Descendente**.  

> [!NOTE]  
>   La ordenación no se admite en imágenes, campos BLOB, FlowFilters ni campos que no pertenezcan a una tabla.  

## <a name="searching-by-using-the-quick-filter"></a>Búsqueda mediante el filtro rápido
Puede agregar filtros a todas las páginas con el filtro rápido. El filtro rápido se activa al elegir el icono de la lupa que se encuentra en la esquina superior derecha de una página. Este tipo de filtro se utiliza para una rápida introducción de criterios.

> [!IMPORTANT]  
>   El acceso Filtro rápido proporciona un acceso sencillo a los datos de filtro mediante la especificación de texto normal, pero también proporciona muchas opciones de criterios de búsqueda. El filtro rápido actúa de distinta forma dependiendo de si introduce texto sin formato o texto con símbolos.  

* Si se introduce texto sin formato en los criterios de búsqueda, estos se interpretan como una búsqueda que tendrá en cuenta mayúsculas y minúsculas y que contendrá un determinado texto.  
* Si se introduce texto con símbolos en los criterios de búsqueda, estos se interpretan exactamente como se haya introducido este texto y teniendo en cuenta mayúsculas y minúsculas.

### <a name="quick-filter-criteria"></a>Criterios del filtro rápido
<!-- html syntax because symbols conflict with MarkDown syntax -->
<TABLE>
  <TR>
    <TH>Criterios de búsqueda</TH>
    <TH>Interpretado como…</TH>
    <TH>Devoluciones...</TH>
  </TR>
  <TR>
    <TD>man</TD>
    <TD>@&#42;man&#42;</TD>
    <TD>Todos los registros que contienen el texto <b>man</b> y respetando mayúsculas y minúsculas.</TD>
  </TR>
  <TR>
    <TD>se</TD>
    <TD>@&#42;se&#42;</TD>
    <TD>Todos los registros que contienen el texto <b>se</b> y respetando mayúsculas y minúsculas.</TD>
  </TR>
  <TR>
    <TD>Man&#42;</TD>
    <TD>Empieza por <b>Man</b> y distingue mayúsculas de minúsculas.</TD>
    <TD>Todos los registros que empiecen por el texto <b>Man</b>.</TD>
  </TR>
  <TR>
    <TD>'man'</TD>
    <TD>Un texto exacto respetando mayúsculas y minúsculas.</TD>
    <TD>Todos los registros que coincidan exactamente con <b>man</b>.</TD>
  </TR>
  <TR>
    <TD>@man* </TD>
    <TD>Empieza por y distingue mayúsculas de minúsculas.</TD>
    <TD>Todos los registros que empiecen por <b>man</b>.</TD>
  </TR>
    <TR>
    <TD>@&#42;man</TD>
    <TD>Termina en y distingue mayúsculas de minúsculas.</TD>
    <TD>Todos los registros que terminen en <b>man</b>.</TD>
  </TR>
</TABLE>

> [!NOTE]  
>   No puede usar un carácter comodín al filtrar en los campos de enumeración, como el campo **Estado** en los pedidos de venta. Para especificar un filtro para este tipo de campo, puede especificar el valor numérico como parámetro de filtrado. Por ejemplo, en el campo **Estado** de un pedido de venta que tenga los valores **Abierto**, **Lanzado**, **Aprobación pendiente** y **Prepago pendiente**, utilice los valores **0**, **1**, **2** y **3** para filtrar para estas opciones. 

## <a name="searching-by-using-column-filters"></a>Búsqueda usando filtros de columna
Puede agregar un filtro de una o varias columnas a una lista. El filtrado en columnas es más flexible y ampliado que el filtro rápido. 

### <a name="to-add-a-filter-on-a-column"></a>Para agregar un filtro a una columna
1.  Antes de añadir un filtro, elija el icono ![Mostrar como una lista](media/ui_show_as_list_icon.png "Mostrar como lista de flecha izquierda") para cambiar a la vista de lista.
2. Elija hacia flecha hacia abajo en la cabecera de columna y, a continuación elija **Filtro**.
3. Realice una de las siguientes acciones: 
  -  Seleccione *…* al lado del cuadro para seleccionar un valor de una lista.
  -  Introduzca criterios de filtro en el cuadro. Véase la sección siguiente para obtener información detallada.
4. Elija el botón **Aceptar**.

## <a name="filter-criteria-and-symbols"></a>Filtrar los criterios y símbolos
Al introducir criterios, puede usar todos los números y las letras que normalmente se emplean en un campo. También puede usar símbolos especiales para filtrar aún más los resultados. En las tablas siguientes se muestran los símbolos que se pueden usar en los filtros.  
  
> [!IMPORTANT]  
>  Puede haber instancias donde los valores de campo contengan los siguientes símbolos y desee filtrarlos. Para ello, debe incluir la expresión de filtro que contiene el símbolo entre comillas ("). Por ejemplo, si desea filtrar en los registros que comienzan por el texto *S&R*, la expresión de filtro es **'S&R*'**.  
  
### <a name="-interval"></a>(..) Intervalo  
  
|Ejemplo|Registros mostrados|  
|-----------------------|-----------------------|  
|1100..2100|Números del 1100 al 2100.|  
|..2500|Hasta la 2500 inclusive|  
|..12 31 00|Fechas hasta el 31 12 00, inclusive.|  
|P8..|Información correspondiente al ejercicio económico 8 en adelante|  
|..23|Desde la fecha inicial hasta 23-mes actual-año actual 23:59:59|  
|23..|Desde 23-mes actual-año actual 0:00:00 hasta la hora final|  
|22..23|Desde 22-mes actual-año actual 0:00:00 hasta 23-mes actual-año actual 23:59:59|  
  
### <a name="124-eitheror"></a>(&#124;) O/o  
  
|Ejemplo|Registros mostrados|  
|-----------------------|-----------------------|  
|1200&#124;1300|Números con 1200 ó 1300|  
  
### <a name="-not-equal-to"></a>(<>) Distinto  
  
|Ejemplo|Registros mostrados|  
|-----------------------|-----------------------|  
|<>0|Todos los números, excepto el 0<br /><br /> La opción SQL Server permite combinar este símbolo con una expresión de caracteres comodín. Por ejemplo, <>A* significa distinto de cualquier texto que empiece por A.|  
  
### <a name="-greater-than"></a>(>) Mayor de  
  
|Ejemplo|Registros mostrados|  
|-----------------------|-----------------------|  
|>1200|Números mayores que 1200|  
  
### <a name="-greater-than-or-equal-to"></a>(>=) Mayor o igual a  
  
|Ejemplo|Registros mostrados|  
|-----------------------|-----------------------|  
|>=1200|Números mayores o igual que 1200|  
  
### <a name="-less-than"></a>(<) Menor de  
  
|Ejemplo|Registros mostrados|  
|-----------------------|-----------------------|  
|<1200|Números menores que 1200|  
  
### <a name="-less-than-or-equal-to"></a>(<=) Menor o igual que  
  
|Ejemplo|Registros mostrados|  
|-----------------------|-----------------------|  
|<=1200|Números menores o iguales que 1200|  
  
### <a name="-and"></a>(&) y  
  
|Ejemplo|Registros mostrados|  
|-----------------------|-----------------------|  
|>200&<1200|Números mayores de 200 e inferiores a 1200|  
  
### <a name="-an-exact-character-match"></a>(") Una coincidencia exacta de carácter  
  
|Ejemplo|Registros mostrados|  
|-----------------------|-----------------------|  
|'man'|Texto que coincide exactamente con man y distingue mayúsculas de minúsculas.|  
  
### <a name="-case-insensitive"></a>(@) Distinción entre mayúsculas y minúsculas  
  
|Ejemplo|Registros mostrados|  
|-----------------------|-----------------------|  
|@man*|Texto que empieza por man y no distingue mayúsculas de minúsculas.|  
  
### <a name="-an-indefinite-number-of-unknown-characters"></a>(*) Un número indefinido de caracteres desconocidos (quizás ninguno)  
  
|Ejemplo|Registros mostrados|  
|-----------------------|-----------------------|  
|*Co*|Texto que contenga “Co” y es con diferenciación de mayúsculas y minúsculas.|  
|*Co|Texto que termine con “Co” y es con diferenciación de mayúsculas y minúsculas.|  
|Co*|Texto que empiece por “Co” y es con diferenciación de mayúsculas y minúsculas.|  
  
### <a name="-one-unknown-character"></a>(?) Un carácter desconocido  
  
|Ejemplo|Registros mostrados|  
|-----------------------|-----------------------|  
|Mendo?a|Texto como Mendoza o Mendosa|  
  
### <a name="combined-format-expressions"></a>Expresiones de formato combinadas  
  
|Ejemplo|Registros mostrados|  
|-----------------------|-----------------------|  
|5999&#124;8100..8490|Incluye todos los registros cuyo número sea 5999 o un número entre 8100 y 8490.|  
|..1299&#124;1400..|Incluye los registros cuyo número sea menor o igual que 1299 o un número igual o mayor que 1400|  
|>50&<100|Incluye los registros cuyo número sea mayor que 50 y menor que 100.|  
 
## <a name="see-also"></a>Consulte también
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

