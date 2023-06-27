---
title: Desarrollo de diseños de informes y conjuntos de datos
description: Proporciona una descripción general de los datos de Business Central.
author: kennieNP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.reviewer: edupont
ms.search.keywords: feature overview
ms.date: 02/03/2022
ms.author: kepontop
---

# <a name="developing-business-central-report-layouts-and-datasets"></a>Desarrollo de diseños de informes y conjuntos de datos de Business Central

Un informe de [!INCLUDE[prod_short](includes/prod_short.md)] consta de un objeto de informe que define el _conjunto de datos_ del informe (qué datos están disponibles) y una serie de _diseños de informes_ (cómo se presentan los datos).  

## <a name="developing-report-layouts"></a>Desarrollo de diseños de informe

¿Tal vez desee modificar los diseños de informes existentes proporcionados en [!INCLUDE[prod_short](includes/prod_short.md)]? Dependiendo de la tecnología utilizada para el diseño, esto es algo que podría hacer usted mismo (diseños de Excel y tal vez también de Word), o tal vez necesite un desarrollador para hacerlo (diseños RDLC con pixelación perfecta).

| Para | Vea |
|--|--|
| Obtenga más información sobre los diferentes tipos de diseño (Word, Excel y RDLC) | [Tipos de diseño (Word, Excel y RDLC)](ui-manage-report-layouts.md) |
| Obtenga información sobre cómo puede crear un nuevo diseño de informe. | [Crear un nuevo diseño](ui-how-create-custom-report-layout.md) |
| Más información sobre qué fuentes están instaladas en [!INCLUDE[prod_short](includes/prod_short.md)] en línea, para poder usarlas en diseños de informes. | [Uso de fuentes en diseños](ui-fonts.md) |
| Para aprender a trabajar con diseños de Word. | [Trabajar con diseños de Word](ui-how-add-fields-word-report-layout.md) |
| Para aprender a importar/exportar archivos de diseños. | [Importar/exportar un diseño](ui-how-import-and-export-report-layout.md) |
| Para aprender a actualizar una definición de diseño en [!INCLUDE[prod_short](includes/prod_short.md)] con un nuevo archivo de diseño. | [Importar/exportar un diseño](ui-how-import-and-export-report-layout.md) |
| para aprender a cambiar el diseño predeterminado de un informe. | [Cambiar el diseño predeterminado](ui-how-change-layout-currently-used-report.md) |
<!-- | Para aprender a trabajar con diseños de Excel | [Trabajar con diseños de Excel](ui-how-add-fields-word-report-layout.md) | -->

## <a name="developing-report-datasets"></a>Desarrollo de conjuntos de datos de informes

 Para cambiar las definiciones de conjuntos de datos que definen qué datos están disponibles en el informe, necesita un desarrollador que conozca el lenguaje de programación AL y las herramientas para desarrollar objetos de informe y extensiones de informe.

| Para | Vea |
|--|--|
| Aprender a programar reportes en AL | [Guía de desarrollo de informes](/dynamics365/business-central/dev-itpro/developer/devenv-reports) |
| Aprender a hacer que los informes funcionen | [Guía de ajuste del rendimiento de los informes](/dynamics365/business-central/dev-itpro/performance/performance-developer#writing-efficient-reports) |

## <a name="see-also"></a>Consulte también

[Descripción general de Inteligencia empresarial e informes](reports-use-reports.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
