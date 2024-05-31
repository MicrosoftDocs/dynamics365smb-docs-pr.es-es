---
title: Trabajar con diseños RDLC
description: Obtenga una introducción a los diseños de informe RDLC.
author: jswymer
ms.topic: conceptual
ms.service: dynamics-365-business-central
ms.search.keywords: 'customized report, document layout, logo, personalize'
ms.search.form: '9650, 9652'
ms.date: 12/04/2023
ms.author: jswymer
ms.reviewer: jswymer
---
# Trabajar con diseños RDLC

Los diseños de RDLC se basan en los archivos de diseño de definición de informe (tipos de archivo .rdl o .rdlc). Los conceptos de diseño para los diseños RDLC son similares a otros tipos de diseño. El diseño determina qué campos mostrar y cómo se organizan. No obstante, el diseño de RDLC es más avanzada que la de diseños de Word y Excel.

[![Muestra los diferentes elementos de un diseño de RDLC.](media/rdlc-layout.png)](media/rdlc-layout.png#lightbox)

## Herramientas necesarias

Para modificar diseños RDL, puede usar Microsoft SQL Server Report Builder o Microsoft Visual Studio con la extensión RDLC Report Designer.

- Report Builder es una aplicación independiente que usted o un administrador instalan en su equipo. Con Business Central local, Report Builder se instala automáticamente con la instalación de Business Central Server. Para obtener más información sobre la instalación de Report Builder, consulte [Instalar Report Builder](/sql/reporting-services/install-windows/install-report-builder) en la documentación de SQL Server.

- RDLC Report Designer es una extensión para Visual Studio 2019 y posteriores. Puede descargar e instalar RDLC Report Designer desde [Visual Studio Marketplace](https://marketplace.visualstudio.com/items?itemName=ProBITools.MicrosoftRdlcReportDesignerforVisualStudio-18001).

## Crear y modificar diseños de RDLC

La creación y modificación de diseños de RDLC es una tarea avanzada, que normalmente la realizan usuarios avanzados o desarrolladores. Los conceptos básicos no son específicos de los diseños de informes de Business Central. Por este motivo, le remitimos a la siguiente documentación:

- [Crear informe de diseño RDL](/dynamics365/business-central/dev-itpro/developer/devenv-howto-rdl-report-layout)

   Este artículo explica cómo crear un diseño de informe RDLC a partir del código AL.

- [Informes, partes de informes y definiciones de informes ](/sql/reporting-services/report-design/reports-report-parts-and-report-definitions-report-builder-and-ssrs?)

   Esto lo vincula a la documentación de SQL Server Reporting Services para RDL/RDLC. Este artículo explica los conceptos que subyacen a RDL/RDLC y cómo usar Report Builder.

> [!NOTE]
> Report Builder solo reconoce el tipo de archivo .rdl, no .rdlc. Los archivos de diseño exportados desde Business Central son tipos de archivo .rdlc. Entonces, para modificar estos diseños en Report Builder, cambie el nombre del tipo de archivo a .rdl.

## Consulte también

[Gestión de diseños de informe](ui-manage-report-layouts.md)  
[Establecer el diseño utilizado por un informe](ui-set-report-layout.md)  
[Empezar a crear diseños de informes](ui-get-started-layouts.md)  
[Trabajar con informes, trabajos por lotes y XMLports](ui-work-report.md)  
[Inteligencia empresarial](bi.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Análisis de datos de informes con Excel](report-analyze-excel.md).

[!INCLUDE[footer-include](includes/footer-banner.md)]
