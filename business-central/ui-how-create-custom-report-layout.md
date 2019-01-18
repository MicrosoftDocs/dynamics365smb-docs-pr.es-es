---
title: "Crear y modificar diseños personalizados para informes y documentos | Documentos de Microsoft"
description: "Obtenga información sobre cómo crear sus propios diseños personalizados para personalizar el aspecto de un informe cuando se vea, se imprima o se guarde."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customized report, document layout, logo, personalize
ms.date: 10/01/2018
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: 33b900f1ac9e295921e7f3d6ea72cc93939d8a1b
ms.openlocfilehash: 39e4c310e3de5f16066408b96b54042c44c753fd
ms.contentlocale: es-es
ms.lasthandoff: 11/26/2018

---
# <a name="create-and-modify-a-custom-report-or-document-layout"></a>Crear y modificar un diseño de informe o documento personalizado
De forma predeterminada, un informe tendrá un diseño de informe integrado, bien de RDLC o de Word, o ambos. No puede modificar diseños integrados. No obstante, puede crear sus propios diseños personalizados que le permitan modificar el aspecto del informe cuando se vea, se imprima o se guarde. Puede crear varios diseños de informe personalizados para el mismo informe y, a continuación, cambiar al diseño utilizado por un informe según sea necesario.

> [!NOTE]  
>   En [!INCLUDE[d365fin](includes/d365fin_md.md)], el término “informe” también afecta a documentos externos, como facturas de venta y las confirmaciones de pedido que envía a los clientes como archivos PDF.

Para crear un diseño personalizado, puede hacer una copia de un diseño personalizado existente o agregar un nuevo diseño personalizado, que en la mayoría de los casos se basa en un diseño integrado. Cuando se agrega un nuevo diseño personalizado, puede elegir agregar un tipo de diseño de informe de RDLC, uno de Word, o ambos. El nuevo diseño personalizado se basará automáticamente en el diseño integrado del informe si hay uno disponible. Si no hay ningún diseño integrado para el tipo, se crea un nuevo diseño en blanco que tendrá que modificar y diseñar desde cero. Para obtener más información acerca de los diseños de informe de RDLC y de Word, diseños personalizados e integrados y otros temas, consulte [Gestionar diseños de informe](ui-manage-report-layouts.md).  

## <a name="to-create-a-custom-layout"></a>Para crear un diseño personalizado
1. Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Selección de diseño de informes** y luego elija el enlace relacionado.

    La página **Selección de diseño de informes** muestra todos los informes disponibles en la empresa especificada en el campo **Empresa** en la parte superior de la página.
2. Establezca el campo **Empresa** en la empresa en la que desea crear el diseño del informe.
3. Seleccione la fila para el informe para el cual desee crear el diseño y, a continuación, elija la acción **Diseños personalizados**.  
   La página **Diseños de informe personalizados** aparece con todos los diseños personalizados disponibles para el informe seleccionado.
4. Si desea crear una copia de un diseño personalizado existente, seleccione el diseño personalizado existente en la lista y, a continuación, elija la acción **Copiar**.  
   La copia del diseño personalizado aparece en la página **Diseños de informe personalizados** e incluye las palabras *Copia de* en el campo **Descripción**.
5. Si desea añadir un nuevo diseño personalizado que se base en un diseño integrado, haga lo siguiente:  
   1. Seleccione la acción **Nuevo**. Aparece la página **Insertar diseñado integrado para un informe**. Los campos de **Id.** y **Nombre** se rellenan automáticamente.
   2. Para agregar un tipo de diseño de informe de Word personalizado, seleccione la casilla **Insertar diseño de Word**.
   3. Para agregar un tipo de diseño de informe de RDLC personalizado, seleccione la casilla **Insertar diseño de RDLC**.
   4. Elija el botón **Aceptar**.  
      Los nuevos diseños personalizados aparecen en la página **Diseños de informe personalizados**. Si un diseño nuevo se basa en un diseño integrado, tendrá las palabras **Copia de un diseño integrado** en el campo **Descripción**. Si no había diseño integrado para el informe, el nuevo diseño tendrá las palabras **Nuevo diseño** en el campo **Descripción** para indicar que el diseño personalizado está en blanco.
6. De forma predeterminada, el campo **Nombre de la empresa** está en blanco, lo que significa que el diseño personalizado estará disponible para el informe en todas las empresas. Para que el diseño personalizado esté disponible en una empresa específica solo, elija **Editar** y, a continuación, establezca el campo **Nombre de la empresa** en la empresa que quiera.

El diseño personalizado se ha creado. Ahora puede modificar el diseño personalizado según sea necesario.

## <a name="ModifyCustomLayout"></a>Modificación de un diseño personalizado
Para modificar un diseño de informe, primero deberá exportar el diseño de informe como archivo a una ubicación en su equipo o red y después abrir el documento exportado y realizar los cambios. Cuando haya terminado de realizar los cambios, importe el diseño de informe.

### <a name="to-modify-a-custom-layout"></a>Para modificar un diseño personalizado
1.  Puede exportar un diseño personalizado desde la página **Diseños de informe personalizados**. Si esta página no es ya abierta, busque y abra la página **Selección de diseño de informes**, seleccione el informe que tiene el diseño que quiere modificar y haga clic en la acción **Diseños personalizados**.  
2.  En la página **Diseños de informe personalizados**, seleccione el diseño que desea modificar, seleccione la acción **Exportar diseño** y, después, seleccione **Guardar** o **Guardar como** para guardar el documento de diseño del informe en una ubicación del equipo o red.  

3.  Abra el documento de diseño de informe que acaba de guardar y realice las modificaciones.

      Si está cambiando una plantilla de Word, abra el documento de diseño en Word. Para editar los detalles, vea la sección siguiente [Realizar cambios en el diseño del informe](ui-how-create-custom-report-layout.md#MakeChangesToLayout).

      Los diseños de informe RDLC son más avanzados que plantillas de informe de Word. Para obtener más información acerca de cómo modificar un diseño de informe de RDLC, consulte [Diseñar diseños de informes RDLC](/dynamics-nav/Designing-RDLC-Report-Layouts).

      No olvide guardar los cambios cuando termine.

4.  Vuelva a la página **Diseños de informe personalizados**, seleccione la plantilla del informe que se exportó y modificó y después seleccione **Importar diseño**.  

5. En el cuadro de diálogo **Importar**, seleccione **Seleccionar** para buscar y seleccionar un documento de diseño y, a continuación, elija **Abrir**.

##  <a name="MakeChangesToLayout"></a> Realizar cambios en un diseño de informe de Word  
Para realizar cambios generales de formato y diseño, como cambiar la fuente del texto, agregar y modificar una tabla o eliminar un campo de datos, simplemente use las funciones de edición básicas de Word, como con cualquier documento de Word.

Si está creando un diseño de informe de Word desde cero o agregando nuevos campos de datos, empiece sumando una tabla que incluya las filas y columnas que llevarán los campos de datos.

> [!TIP]  
>  Mostrar las líneas de cuadrícula de la tabla de manera que se vean los límites de las celdas de la tabla. No se olvide de ocultar las líneas de cuadrícula cuando termine la edición. Para mostrar u ocultar líneas de cuadrícula de tabla, seleccione la tabla y, a continuación, en **Diseño** en la pestaña **Escritorio**, elija **Ver líneas de cuadrícula**. 

### <a name="embedding-fonts-in-word-layouts-for-consistency"></a>Inserción de fuentes en disposiciones de Word para mayor consistencia 

Para garantizar que los informes siempre se muestren e impriman con las fuentes deseadas, independientemente del lugar donde los usuarios abran o impriman los informes, puede insertar las fuentes en el documento de Word. Sin embargo, tenga en cuenta que la inserción de fuentes puede aumentar significativamente el tamaño de los archivos de Word. Para obtener más información acerca de la inserción de fuentes en Word, consulte [Insertar fuentes en Word, PowerPoint o Excel](https://support.office.com/en-us/article/Embed-fonts-in-Word-PowerPoint-or-Excel-cb3982aa-ea76-4323-b008-86670f222dbc). 

###  <a name="RemoveField"></a> Quitar los campos de etiqueta y de datos en los diseños de Word  
 Los campos de etiqueta y datos de un informe están incluidos en los controles de contenido en Word. La ilustración siguiente muestra un control de contenido seleccionado en el documento de Word.  

 ![Control de contenido del campo en el diseño de informe de Word](media/nav_wordreportlayouts_contentcontrol.png "NAV_WordReportLayouts_ContentControl")  

 El nombre del campo de etiqueta o de datos se muestra en el control de contenido. En el ejemplo, el nombre de campo es CompanyAddr1.  

### <a name="to-remove-a-label-or-data-field"></a>Para eliminar una etiqueta o un campo de datos  

1.  Haga clic con el botón secundario en el campo que desee eliminar y seleccione **Eliminar control de contenido**.  

     El control de contenido se elimina, pero el nombre del campo permanece como texto.  

2.  Elimine el texto restante según sea necesario.  

### <a name="adding-data-fields"></a>Añadir campos de datos
La adición de campos de datos de un conjunto de datos de informe es una operación más avanzada y necesita conocimientos del conjunto de datos de informe. Para obtener información acerca de la adición campos para datos, etiquetas, datos e imágenes, consulte [Añadir campos a un diseño de informe de Word](ui-how-add-fields-word-report-layout.md).  

### 


## <a name="see-also"></a>Consulte también
[Gestión de diseños de informe](ui-manage-report-layouts.md)  
[Cambiar el diseño que se usa actualmente en un informe](ui-how-change-layout-currently-used-report.md)  
[Importar y exportar un diseño de informe o documento personalizado](ui-how-import-and-export-report-layout.md)  
[Trabajar con informes](ui-work-report.md)  
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

