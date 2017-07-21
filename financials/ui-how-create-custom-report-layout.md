---
title: "Crear diseños personalizados para informes y documentos | Documentos de Microsoft"
description: "Obtenga información sobre cómo crear sus propios diseños personalizados para personalizar el aspecto de un informe cuando se vea, se imprima o se guarde."
services: project-madeira
documentationcenter: 
author: SusanneWindfeldPedersen
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customized report, document layout, logo, personalize
ms.date: 03/29/2017
ms.author: solsen
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 551e838c2896470f9ee620f4ca09a6af3377b458
ms.contentlocale: es-es
ms.lasthandoff: 07/07/2017


---
# <a name="how-to-create-a-custom-report-or-document-layout"></a>Crear un diseño de informe o documento personalizado
De forma predeterminada, un informe tendrá un diseño de informe integrado, bien de RDLC o de Word, o ambos. No puede modificar diseños integrados. No obstante, puede crear sus propios diseños personalizados que le permitan modificar el aspecto del informe cuando se vea, se imprima o se guarde. Puede crear varios diseños de informe personalizados para el mismo informe y, a continuación, cambiar al diseño utilizado por un informe según sea necesario.

> [!NOTE]  
>   En [!INCLUDE[d365fin](includes/d365fin_md.md)], el término “informe” también afecta a documentos externos, como facturas de venta y las confirmaciones de pedido que envía a los clientes como archivos PDF.

Para crear un diseño personalizado, puede hacer una copia de un diseño personalizado existente o agregar un nuevo diseño personalizado, que en la mayoría de los casos se basa en un diseño integrado. Cuando se agrega un nuevo diseño personalizado, puede elegir agregar un tipo de diseño de informe de RDLC, uno de Word, o ambos. El nuevo diseño personalizado se basará automáticamente en el diseño integrado del informe si hay uno disponible. Si no hay ningún diseño integrado para el tipo, se crea un nuevo diseño en blanco que tendrá que modificar y diseñar desde cero. Para obtener más información acerca de los diseños de informe de RDLC y de Word, diseños personalizados e integrados y otros temas, consulte [Gestionar diseños de informe](ui-manage-report-layouts.md).  

## <a name="to-create-a-custom-layout"></a>Para crear un diseño personalizado
1. Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "Search for Page or Report icon"), escriba **Selección de diseño de informes** y, a continuación, seleccione el vínculo relacionado.  
   La ventana **Selección de diseño de informes** muestra todos los informes disponibles en la empresa especificada en el campo Empresa en la parte superior de la ventana.
2. Establezca el campo **Empresa** en la empresa en la que desea crear el diseño del informe.
3. Seleccione la fila para el informe para el cual desee crear el diseño y, a continuación, elija **Diseños personalizados**.  
   La ventana **Diseños de informe personalizados** aparece con todos los diseños personalizados disponibles para el informe seleccionado.
4. Si desea crear una copia de un diseño personalizado existente, seleccione el diseño personalizado existente en la lista y, a continuación, elija **Copiar**.  
   La copia del diseño personalizado aparece en la ventana **Diseños de informe personalizados** e incluye las palabras Copia de en el campo Descripción.
5. Si desea añadir un nuevo diseño personalizado que se base en un diseño integrado, haga lo siguiente:  
   1. Elija **Nuevo**. Aparece la ventana **Insertar diseñado integrado para un informe**. Los campos de **Id.** y **Nombre** se rellenan automáticamente.
   2. Para agregar un tipo de diseño de informe de Word personalizado, seleccione la casilla **Insertar diseño de Word**.
   3. Para agregar un tipo de diseño de informe de RDLC personalizado, seleccione la casilla **Insertar diseño de RDLC**.
   4. Elija el botón **Aceptar**.  
      Los nuevos diseños personalizados aparecen en la ventana **Diseños de informe personalizados**. Si un diseño nuevo se basa en un diseño integrado, tendrá las palabras **Copia de un diseño integrado** en el campo **Descripción**. Si no había diseño integrado para el informe, el nuevo diseño tendrá las palabras **Nuevo diseño** en el campo **Descripción** para indicar que el diseño personalizado está en blanco.
6. De forma predeterminada, el campo **Nombre de la empresa** está en blanco, lo que significa que el diseño personalizado estará disponible para el informe en todas las empresas. Para que el diseño personalizado esté disponible en una empresa específica solo, elija **Editar** y, a continuación, establezca el campo **Nombre de la empresa** en la empresa que quiera.

## <a name="see-also"></a>Consulte también
[Gestión de diseños de informe](ui-manage-report-layouts.md)  
[Cambiar el diseño que se usa actualmente en un informe](ui-how-change-layout-currently-used-report.md)  
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

