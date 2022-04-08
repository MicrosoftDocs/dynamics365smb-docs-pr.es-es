---
title: Administrar diseños de informes y documentos
description: Use los diseños de informe para personalizar documentos, por ejemplo, para personalizar la fuente, el logotipo o la configuración de página de los archivos PDF que envía a clientes.
author: jswymer
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customized report, document layout, logo, personalize
ms.search.form: 9652, 9650
ms.date: 04/01/2021
ms.author: jswymer
ms.openlocfilehash: 5fed722bb5929da100c1c92e63aebb1f10cf53d0
ms.sourcegitcommit: 8a12074b170a14d98ab7ffdad77d66aed64e5783
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 03/31/2022
ms.locfileid: "8520687"
---
# <a name="report-and-document-layouts-overview"></a>Información general de diseños de informes y documentos

Un diseño de informe controla el contenido y el formato del informe, incluidos los campos de datos de un conjunto de datos de informe que aparecen en el informe y la forma en que se organizan, el estilo del texto, las imágenes, etc. Desde [!INCLUDE[prod_short](includes/prod_short.md)] puede cambiar el diseño que se usa en un informe, crear un nuevo diseño o modificar diseños existentes.

> [!NOTE]  
> En [!INCLUDE[prod_short](includes/prod_short.md)], el término “informe” también afecta a documentos externos, como facturas de venta y las confirmaciones de pedido que envía a los clientes como archivos PDF.

## <a name="introduction"></a>Introducción

En concreto, un diseño de informe configura lo siguiente:

* Los campos de etiqueta y de datos que incluir desde el conjunto de datos del informe de [!INCLUDE[prod_short](includes/prod_short.md)].
* El formato de texto, como el tipo de fuente, el tamaño y el color.
* El logotipo de la empresa y su posición.
* Configuración de página general, como márgenes e imágenes de fondo.

Un informe se puede configurar con varios diseños de informe, entre los que puede cambiar según sea necesario. 

<!--You can use one of the built-in report layouts or you can create custom report layouts and assign them to your reports as needed. For more information, see [Create a Custom Report or Document Layout](ui-how-create-custom-report-layout.md).-->

Hay dos aspectos importantes de los diseños de informes que influirán en cómo trabaja con ellos: el *tipo de diseño* y el *origen del diseño*. El tipo de diseño indica el tipo de archivo en el que se basa el diseño. El origen del diseño indica el origen del diseño.

## <a name="layout-types"></a>Tipos de diseño

Hay cuatro tipos de diseños que puede usar en los informes: Word, RDLC, Excel y externo.

### <a name="word"></a>Word

Los diseños de Word se basan en documentos de Word (tipo de archivo .docx). Los diseños de Word permiten diseñar formatos de informes con Microsoft Word. Un diseño de Word determina el contenido del informe, controlando la forma en que se organizan estos elementos del contenido y su aspecto. Un documento de diseño de Word normalmente usa tablas para organizar el contenido, donde las celdas pueden incluir campos de datos, texto o imágenes.

[![Ejemplo de un documento de diseño de informe de Word para Business Central.](media/word-layout-overview.png)](media/word-layout-overview.png#lightbox) 

<!--![Example of a word report layout document for Business Central.](media/nav_wordreportlayout_edit_in_word_example.png) -->

Para obtener más información, consulte [Trabajar con diseños de Word](ui-how-add-fields-word-report-layout.md).

### <a name="excel"></a>Excel

Los diseños de Excel se basan en libros de Microsoft Excel (tipo de archivo .xlsx). Le permiten crear informes utilizando las características conocidas de Excel para resumir, analizar y presentar datos con herramientas, como las fórmulas, PivotTables, PivotCharts y más.

[![Muestra el ejemplo de un diseño de Excel.](media/excel-layout-2.png)](media/excel-layout-2.png#lightbox)

Para obtener más información, consulte [Trabajar con diseños de Excel](ui-excel-report-layouts.md).

### <a name="rdlc"></a>RDLC

Los diseños de RDLC se basan en los archivos de diseño de definición de informe de cliente (tipos de archivo .rdl o .rdlc). Estos diseños se crean y modifican con el generador de informes de SQL Server o Microsoft RDLC Report Designer. El concepto de diseño para los diseños de RDLC es similar a los diseños de Word, donde el diseño determina qué campos mostrar y cómo se organizan. No obstante, el diseño de RDLC es más avanzada que la de diseños de Word.

[![Muestra el ejemplo de un diseño de RDLC.](media/rdlc-layout-overview.png)](media/rdlc-layout-overview.png#lightbox)

Para obtener más información, consulte [Trabajar con diseños de RDLC](ui-rdlc-report-layouts.md).

### <a name="external"></a>Externo

Un tipo de diseño externo se refiere a un tipo avanzado que está especialmente diseñado para informes específicos. Los informes y los diseños los proporcionan normalmente los socios, no Microsoft. El tipo de archivo real del diseño variará según el proveedor.

Para más información, consulte [Desarrollo de una representación de informe personalizada](/dynamics365/business-central/dev-itpro/developer/devenv-report-custom-render).

## <a name="layout-sources"></a>Orígenes de diseño

Además del tipo, los diseños se dividen en tres categorías, según su fuente u origen.

* Diseños de extensión

   Los diseños de extensión son diseños que forman parte de una extensión que se ha instalado en el entorno. Estos diseños suelen ser diseños estándar proporcionados por Microsoft, por ejemplo, en la aplicación base. O bien, podrían ser diseños incluidos en extensiones de otros proveedores de software. Puede reconocer los diseños de extensión en la página **Diseños de informe** porque el nombre de la extensión y el editor se muestran en la columna **Extensión**.

* Diseños definidos por el usuario

   El otro origen de diseños es el usuario final. Desde dentro de Business Central, un usuario con los permisos adecuados puede agregar nuevos diseños de varias maneras. Por ejemplo, podría comenzar desde un diseño de extensión existente u otro diseño definido por el usuario. En los **Diseños de informe**, el diseño definido por el usuario tendrá una columna **Extensión** vacía.

   Para obtener más información, consulte [Empezar a crear diseños de informes](ui-get-started-layouts.md).

* Diseños personalizados

  Los diseños personalizados también son diseños creados por los usuarios. La diferencia es que estos diseños se crean a partir de la página heredada **Diseños de informe personalizados** y solo pueden ser de tipo Word y RDLC. Aunque todavía puede crear diseños personalizados, se están eliminando gradualmente a favor de los diseños definidos por el usuario.

  Para obtener más información, consulte [(Versión heredada) Crear y modificar diseños de informe personalizados](ui-how-create-custom-report-layout.md).

Para obtener información que le ayudará a decidir qué tipo es mejor para usted, consulte [Decida qué tipo de diseño desea](ui-get-started-layouts.md#decide).

> [!IMPORTANT]
> Una cosa importante que debe recordar es que no puede modificar los diseños de extensión desde el cliente de Business Central. Por ejemplo, no puede cambiar el nombre o el tipo del diseño, ni cargarlo y reemplazarlo con otra versión. Si lo intenta, obtendrá un mensaje de error. En su lugar, tendrá que crear un diseño personalizado o definido por el usuario basado en el diseño de la extensión.

<!--
### Built-in and custom report layouts



[!INCLUDE[prod_short](includes/prod_short.md)] includes several built-in layouts. Built-in layouts are predefined layouts that are designed for specific reports. [!INCLUDE[prod_short](includes/prod_short.md)] reports will have a built-in layout as either an RDLC report layout, Word report layout, or in some cases both. You can’t modify a built-in report layout from [!INCLUDE[prod_short](includes/prod_short.md)] but you use them as a starting point for building your own custom report layouts.

Custom layouts are report layouts that you design to change the appearance of a report. You typically create a custom layout based on a built-in layout, but you can create them from scratch or from a copy of an existing custom layout. Custom layouts enable you to have multiple layouts for the same report, which you switch among as needed. For example, you can have different layouts for each [!INCLUDE[prod_short](includes/prod_short.md)] company, or you can have different layouts for the same company for specific occasions or events, like a special campaign or holiday season.


Deciding on whether to use a Word, Excel, or RDLC layout type will depend on how you want the generated report to look and your knowledge of tools for creating the layouts, like Word, Excel, and SQL Server Report Builder.

* The general design concepts for Word and RDLC layouts are similar. However each type has certain design features that affect how the generated report appears in [!INCLUDE[prod_short](includes/prod_short.md)]. This means that the same report might look different when using the Word report layout compared to the RDLC report layout.

* The process for setting up Word, Excel, and RDLC report layouts on reports is the same. The main difference is in the way you modify the layouts. Word and especially Excel layouts are typically easier to create and modify than RDLC report layouts because you use Word and Excel. RDLC report layouts are modified by using SQL Server Report builder, which targets more advanced users.

* Not all reports and document have a dataset that is optimized for use with an Excel layout. For example, aggregations and complex calculations work best with RDLC or Word layouts. The same is true for documents.

For information about how to switch the layout currently used on a report, see [Set the Layout Used by a Report](ui-set-report-layout.md).

-->



## <a name="see-related-training-at-microsoft-learn"></a>Consulte Formación relacionada en [Microsoft Learn](/learn/modules/change-documents-dynamics-365-business-central/index)

## <a name="see-also"></a>Consulte también

[Actualizar los diseños de informe personalizados](ui-update-report-layouts.md)  
[Crear y modificar diseños de informe personalizados](ui-how-create-custom-report-layout.md)  
[Importar y exportar un diseño de informe o documento personalizado](ui-how-import-and-export-report-layout.md)  
[Definir diseños de documentos especiales para clientes y proveedores](ui-define-customer-vendor-document-layouts.md)  
[Enviar documentos por correo electrónico](ui-how-send-documents-email.md)  
[Trabajar con informes, trabajos por lotes y XMLports](ui-work-report.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]