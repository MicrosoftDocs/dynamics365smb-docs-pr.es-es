---
title: Agregar campos a un diseño de informe de Word
description: Este tema describe cómo agregar campos de un conjunto de datos de informe a un diseño de informe de Word para un informe.
author: jswymer
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 11/25/2021
ms.author: jswymer
ms.openlocfilehash: 036b6964b8a0e468bdfc4d2f3e44824b3daac9ee
ms.sourcegitcommit: ef80c461713fff1a75998766e7a4ed3a7c6121d0
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 02/15/2022
ms.locfileid: "8144728"
---
# <a name="add-fields-to-a-word-report-layout"></a>Agregar campos a un diseño de informe de Word
Un conjunto de datos de informe puede constar de campos que muestran etiquetas, datos e imágenes. Este tema describe el procedimiento para agregar campos de un conjunto de datos de informe a un diseño de informe de Word para un informe. Agregue campos al informe mediante el elemento XML personalizado de Word y mediante la adición de controles de contenido que asignen los campos al conjunto de datos del informe. La adición de campos requiere tener conocimientos del conjunto de datos del informe, de forma que pueda identificar los campos que desea agregar al diseño.  
  
> [!NOTE]  
>  No puede modificar diseños de informe integrados<!--Onprem. Built-in layouts can only be modified by using the development environment-->.  

##  <a name="to-open-the-custom-xml-part-for-the-report-in-word"></a><a name="OpenXMLPart"></a> Para abrir el elemento XML personalizado para el informe en Word  
  
1.  Si todavía no está abierto, abra en Word el documento de diseño de informe de Word.  
  
     Para obtener más información, vea [Crear y modificar un diseño de informe personalizado](ui-how-create-custom-report-layout.md).  
  
2.  Mostrar la ficha **Desarrollador** en la cinta de Microsoft Word.  
  
     De forma predeterminada, la pestaña **Desarrollador** no se muestra en la cinta de opciones. Para obtener más información, consulte [Mostrar la pestaña de desarrollador en la cinta de opciones](/visualstudio/vsto/how-to-show-the-developer-tab-on-the-ribbon).  
  
3.  En la pestaña **Desarrollador**, elija **Panel de asignación XML**.  
  
4.  En el panel **Asignación XML**, en la lista desplegable **Elemento XML personalizado**, seleccione el elemento XML personalizado para el informe de [!INCLUDE[prod_short](includes/prod_short.md)], que suele ser el último en la lista. El nombre del elemento XML personalizado tiene el formato siguiente:  
  
     urn:microsoft-dynamics-nav/reports/*report_name*/*ID*  
  
     *report_name* es el nombre asignado al informe<!--OnPrem as specified by the report's [Name Property-duplicate](../FullExperience/nav_dev_long_md.md)]-->.  
  
     *Id.* es el número de identificación del informe.  
  
     Una vez que seleccione el elemento XML personalizado, el panel Asignación XML muestra las etiquetas y los controles de campo que hay disponibles para el informe.  
  
### <a name="to-add-a-label-or-data-field"></a>Para añadir una etiqueta o un campo de datos  
  
1.  Coloque el cursor en el documento donde desea agregar el control.  
  
2.  En el panel **Asignación XML**, haga clic con el botón secundario en el control que desee agregar, elija **Insertar control de contenido** y, a continuación, elija **Texto sin formato**.  
  
    > [!NOTE]  
    >  No puede agregar un campo manualmente escribiendo el nombre del campo de conjunto de datos en el control de contenido. Debe utilizar el panel **Asignación XML** para asignar los campos.  
  
### <a name="to-add-repeating-rows-of-data-fields-to-create-a-list"></a>Para agregar filas repetidas a los campos de datos para crear una lista  
  
1.  En una tabla, agregue una fila de tabla que incluya una columna por cada campo que desee repetir.  
  
     Esta fila actuará como marcador para los campos que se repiten.  
  
2.  Seleccione la fila completa.  
  
3.  En el panel **Asignación XML**, haga clic con el botón secundario en el control correspondiente al elemento de datos de informe que contiene los campos que desea repetir, elija **Insertar control de contenido** y seleccione **Se repite**.  
  
4.  Agregue los campos que se repiten a la fila de la siguiente forma:  
  
    1.  Coloque el puntero en una columna.  
  
    2.  En el panel **Asignación XML**, haga clic con el botón secundario en el control que desee agregar, elija **Insertar control de contenido** y, a continuación, elija **Texto sin formato**.  
  
    3.  Por cada campo, repita los pasos a y b.  
  
## <a name="adding-image-fields"></a>Adición de campos de imagen  
 Un conjunto de datos de informe incluye un campo que contiene una imagen, como un logotipo de empresa o una imagen de un producto. Para agregar una imagen desde el conjunto de datos del informe, inserte un control de contenido **Imagen**.  
  
 Las imágenes se alinean en la esquina superior izquierda del control de contenido y cambian su tamaño automáticamente para ajustarse a los límites del control de contenido.  
  
> [!IMPORTANT]  
>  Puede agregar solo imágenes que tengan formato compatible con Word, como tipos de archivo .bmp, .jpeg y .png. Si agrega una imagen que tenga un formato no admitido en Word, recibirá un error cuando ejecute el informe desde el cliente de [!INCLUDE[prod_short](includes/prod_short.md)].  
  
#### <a name="to-add-an-image"></a>Para agregar una imagen  
  
1.  Coloque el puntero en el documento donde desea agregar el control.  
  
2.  En el panel **Asignación XML**, haga clic con el botón secundario en el control que desee agregar, elija **Insertar control de contenido** y, a continuación, elija **Imagen**.  
  
3.  Para aumentar o reducir el tamaño de la imagen, arrastre un control de tamaño hacia fuera desde el centro del control de contenido, o hacia el centro del mismo.  

## <a name="custom-xml-part-overview"></a>Resumen de Elemento XML
Los diseños de informe de Word se crean sobre *elementos XML personalizados*. Un elemento XML personalizado de un informe consta de los elementos que se corresponden con los elementos de datos, columnas y etiquetas que componen el conjunto de datos del informe. <!--OnPrem The data as defined in the Report Dataset Designer in Microsoft Dynamics NAV Development Environment. -->El elemento XML personalizado se utiliza para asignar datos en un informe cuando este se ejecuta.

  
### <a name="xml-structure-of-custom-xml-part"></a>Estructura XML del elemento XML personalizado  
La tabla siguiente proporciona un resumen simplificado del XML de un elemento XML personalizado.  
  
|Elementos XML|Description|  
|------------------|-----------------|  
|`<?xml version="1.0" encoding="utf-16"?>`|Cabecera|  
|`<WordReportXmlPart xmlns="urn:microsoft-dynamics-365/report/<reportname>/<id>/"`|Especificación del espacio de nombres XML. `<reportname>` es el nombre asignado al informe. `<id>` es el identificador asignado al informe.|  
|`..<Labels>`<br /><br /> `....<ColumnNameCaption>ColumnNameCaption</ColumnNameCaption>`<br /><br /> `....<LabelName>LabelCaption</LabelName>`<br /><br /> `..</Labels>`|Contiene todas las etiquetas del informe.<!--OnPren The element includes labels that are related to columns that have the IncludeCaption Property.--><br />-   Los elementos etiquetados que están relacionadas con las columnas tienen el formato `<ColumnNameCaption>ColumnNameCaption</ColumnNameCaption>`<!--OnPrem where `ColumnName` is determined by the column's Name Property.-->.<br />- Los productos etiquetados tienen el formato `<LabelName>LabelName</LabelName`.<!--OnPrem where LabelName is determined by the label's Name Property.-->.<br />-   Las etiquetas se enumeran en orden alfabético.|  
|`..<DataItem1>`<br /><br /> `....<DataItem1Column1>DataItem1Column1</DataItem1Column1>`|Elementos de datos y columnas de nivel superior. Las columnas se enumeran en orden alfabético.<!--OnPrem <br /><br /> The element names and values are determined by the Name Property of the data item or column.-->|  
|`....<DataItem2>`<br /><br /> `......<DataItem2Column1>DataItem2Column1</DataItem2Column1>`<br /><br /> `....</DataItem2>`<br /><br /> `....<DataItem3>`<br /><br /> `......<DataItem3Column1>DataItem3Column1</DataItem3Column1>`<br /><br /> `....</DataItem3>`|Elementos y columnas de datos que están anidados en el elemento de datos de nivel superior. Las columnas se enumeran en orden alfabético en el elemento de datos correspondiente.|  
|`..</DataItem1>`<br /><br /> `</WordReportXmlPart>`|Elemento de cierre.|  
  
### <a name="custom-xml-part-in-word"></a>Elemento XML personalizado en Word  
 En Word, se abre el elemento XML personalizado en el panel **Asignación XML** y, a continuación, se usa el panel para asignar elementos a los controles de contenido en el documento de Word. El panel **Asignación XML** está disponible desde la pestaña **Desarrollador** (para obtener más información, consulte [Visualizar la pestaña Desarrollador en la cinta de opciones](/visualstudio/vsto/how-to-show-the-developer-tab-on-the-ribbon)).  
  
 Los elementos del panel **Asignación XML** aparecen en una estructura similar a la del origen XML. Los campos de etiqueta están agrupados en un elemento **Etiquetas** y de datos común, y las columnas están organizadas en una estructura jerárquica que corresponde al origen XML, con las columnas enumeradas en orden alfabético. Los elementos se identifican por su nombre de columna tal como se define en el informe del conjunto de datos en el código AL. Para obtener más información, consulte [Definir un conjunto de datos de informe](/dynamics365/business-central/dev-itpro/developer/devenv-report-dataset).  
  
 La ilustración siguiente muestra el elemento XML simple personalizado de la sección anterior en el panel **Asignación XML** de un documento de Word.  
  
 ![Clip del panel Asignación XML en Word.](media/nav_reportlayout_xmlmappingpane.png "NAV_ReportLayout_XMLMappingPane")  
  
-   Para añadir una etiqueta o un campo de datos al diseño, inserte un control de contenido asignado al elemento en el panel **Asignación XML**.  
  
-   Para crear filas de columnas que se repiten, inserte un control de contenido **Se repite** para el elemento de datos principal y, a continuación, agregue el control de contenido para las columnas.  
  
-   Para las etiquetas, el texto real que aparece en el informe generado es el valor de la propiedad **Título** del campo en la tabla de elementos de datos (si la etiqueta está relacionada con la columna en el conjunto de datos de informe) o una etiqueta del Diseñador de etiquetas de informes (si la etiqueta no está relacionada con una columna del conjunto de datos).  
  
-   El idioma de la etiqueta que se muestra al ejecutar el informe depende del valor de idioma del objeto de informe.  
  
## <a name="see-also"></a>Consulte también  
 [Crear y modificar un diseño de informe personalizado](ui-how-create-custom-report-layout.md)   


[!INCLUDE[footer-include](includes/footer-banner.md)]