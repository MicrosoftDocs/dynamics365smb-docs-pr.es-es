---
title: "Definir criterios de búsqueda en filtros | Documentos de Microsoft"
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
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 86ca45493081d9dbd229548f7c560e1df4e1c7c3
ms.contentlocale: es-es
ms.lasthandoff: 07/07/2017


---
# <a name="entering-criteria-in-filters"></a>Introducir criterios en los filtros
Cuando quiera buscar datos, como nombres de cliente, direcciones o grupos de productos, puede introducir los criterios. En los criterios de búsqueda puede usar todos los números y las letras que normalmente se emplean en un campo específico. También puede usar símbolos especiales o expresiones matemáticas para filtrar aún más los resultados.

## <a name="searching-using-the-quick-filter"></a>Búsqueda mediante el filtro rápido
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

## <a name="see-also"></a>Consulte también
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

