---
title: Diseños personalizados e integrados para informes y documentos | Documentos de Microsoft
description: Use los diseños de informe para personalizar documentos, por ejemplo, para personalizar la fuente, el logotipo o la configuración de página de los archivos PDF que envía a clientes.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customized report, document layout, logo, personalize
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 9f5bedb69782d77ea64a3779abd26143969925b3
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5390279"
---
# <a name="managing-report-and-document-layouts"></a>Administrar diseños de informes y documentos
Un diseño de informe controla el contenido y el formato del informe, incluidos los campos de datos de un conjunto de datos de informe que aparecen en el informe y la forma en que se organizan, el estilo del texto, las imágenes, etc. Desde [!INCLUDE[prod_short](includes/prod_short.md)] puede cambiar el diseño que se usa en un informe, crear un nuevo diseño o modificar diseños existentes.

> [!NOTE]  
>   En [!INCLUDE[prod_short](includes/prod_short.md)], el término “informe” también afecta a documentos externos, como facturas de venta y las confirmaciones de pedido que envía a los clientes como archivos PDF.

En concreto, un diseño de informe configura lo siguiente:

* Los campos de etiqueta y de datos que incluir desde el conjunto de datos del informe de [!INCLUDE[prod_short](includes/prod_short.md)].
* El formato de texto, como el tipo de fuente, el tamaño y el color.
* El logotipo de la empresa y su posición.
* Configuración de página general, como márgenes e imágenes de fondo.

Un informe se puede configurar con varios diseños de informe, entre los que puede cambiar según sea necesario. Puede utilizar uno de los diseños de informe integrados o puede crear diseños de informe personalizados y asignarlos a sus informes según sea necesario. Para obtener más información, vea [Crear un diseño de informe o documento personalizado](ui-how-create-custom-report-layout.md).

Se pueden usar dos tipos de diseños de informe: Word y RDLC.

## <a name="word-report-layout-overview"></a>Descripción del diseño de informes de Word
Un diseño de informe de Word está basado en un documento de Word (tipo de archivo .docx). Los diseños de informes de Word permiten diseñar diseños de informes con Microsoft Word 2013 o versiones posteriores. Un diseño de informes de Word determina el contenido del informe, controlando la forma en que se organizan estos elementos del contenido y su aspecto. Un documento de diseño de informe de Word normalmente usa tablas para organizar el contenido, donde las celdas pueden incluir campos de datos, texto o imágenes.

 ![Ejemplo de un documento de diseño de informe de Word para NAV](media/nav_wordreportlayout_edit_in_word_example.png "NAV_WordReportLayout_Edit_In_Word_Example")  

## <a name="rdlc-layout-overview"></a>Descripción del diseño de RDLC
Los diseños de RDLC se basan en los diseños de definición de informe de cliente (tipos de archivo .rdlc o .rdl). Estos diseños se crean y modifican con el generador de informes de SQL Server. El concepto del diseño de RDLC es similar al de Word, donde el diseño define el formato general del informe y determina qué campos del conjunto de datos incluir. La elaboración de diseños de RDLC es más avanzada que la de diseños de Word. Para obtener más información, consulte [diseños de informe RDLC](/dynamics-nav/Designing-RDLC-Report-Layouts).

## <a name="built-in-and-custom-report-layouts"></a>Diseños de informe personalizados e integrados
[!INCLUDE[prod_short](includes/prod_short.md)] incluye varios diseños integrados. Los diseños integrados son diseños predefinidos diseñados para informes específicos. Los informes de [!INCLUDE[prod_short](includes/prod_short.md)] tendrán un diseño integrado, como un diseño de informes de RDLC, un diseño de informes de Word o, en algunos casos, ambos. No puede modificar un diseño de informe integrado desde [!INCLUDE[prod_short](includes/prod_short.md)], pero sí se pueden usar como punto de inicio para crear sus propios diseños de informe personalizados.

Los diseños personalizados son diseños de informe que se crean para modificar el aspecto de un informe. Normalmente se crea un diseño personalizado basado en un diseño integrado, si bien se pueden crear desde cero o desde una copia de un diseño personalizado existente. Los diseños personalizados permiten tener varios diseños para el mismo informe, con posibilidad de pasar de uno a otro según sea necesario. Por ejemplo, puede tener distintos diseños para cada empresa de [!INCLUDE[prod_short](includes/prod_short.md)], o puede tener diseños diferentes para la misma empresa para determinadas ocasiones o eventos, como una campaña especial o la temporada de vacaciones.

## <a name="deciding-whether-to-use-a-word-or-rdlc-report-layout"></a>Usar un diseño de informe de Word o uno de RDLC
Un diseño de informe puede basarse en un documento de Word o en un archivo de RDLC. La decisión de si se usará un diseño de informe de Word o de RDLC dependerá del modo en que desea que aparezca el informe generado y de su conocimiento de Word y del generador de informes de SQL Server.

Los conceptos de diseño generales son muy parecidos en Word y RDLC. Sin embargo, cada tipo tiene determinadas características de diseño que afectan a la forma en que el informe generado aparece en [!INCLUDE[prod_short](includes/prod_short.md)]. Esto significa que el mismo informe puede tener un aspecto diferente cuando se utiliza el diseño de informe de Word en comparación con el diseño de informe de RDLC.

El proceso para configurar diseños de informe de Word y de RDLC en informes es el mismo. La diferencia principal es la forma en la que se modifican los diseños. Los diseños de informe Word suelen ser más fáciles de crear y modificar que los diseños de informe de RDLC, ya que se puede utilizar Word para ello. Los diseños de informe de RDLC se modifican mediante el generador de informes de SQL Server, que está dirigido a usuarios más avanzados.

Para obtener información acerca de cómo cambiar el diseño que desea usar, consulte [Cambiar el diseño de informe actual](ui-how-change-layout-currently-used-report.md).

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