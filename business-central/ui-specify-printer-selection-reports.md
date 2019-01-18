---
title: "Configuración informes para imprimir en impresoras específicas | Documentos de Microsoft"
description: "Obtenga información sobre cómo especificar una impresora para un informe y usar la página Selección impresoras."
services: project-madeira
documentationcenter: 
author: SusanneWindfeldPedersen
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: online printing
ms.date: 10/01/2018
ms.author: solsen
ms.translationtype: HT
ms.sourcegitcommit: caf7cf5afe370af0c4294c794c0ff9bc8ff4c31c
ms.openlocfilehash: bc3a7ab7a61e7a51a58494c3f5892c22b6867333
ms.contentlocale: es-es
ms.lasthandoff: 11/22/2018

---
# <a name="specify-printer-selection-for-reports"></a>Especificar selección de impresora para informes
Esta página está vacía porque no puede configurar impresoras específicas para informes específicos. Estamos trabajando para resolver este problema.

Mientras tanto, si desea imprimir un informe, tiene que descargarlo como documento PDF primero, eligiendo el botón **Enviar**. A continuación, seleccione el tipo de archivo como se descargará el informe; debe elegir **Documento PDF**. Ahora puede abrir el documento de PDF inmediatamente e imprimirlo, o guardarlo e imprimirlo más adelante.

<!--

You can set up reports so that they must be printed on a specific printer. The following are some uses of printer selection:

- You can print reports on special company letterhead.
- You can print reports on different paper sizes.
- You can print reports on the default printer of a specified employee.

You use the **Printer Selections** page to set different values to obtain different output. If you set a specific printer selection, then it takes precedence over a more general printer selection. For example, you can set a printer selection that has values in the **User ID**, **Report ID**, and **Printer Name** fields. This printer selection takes precedence over a printer selection that has blank entries in the **User ID** or **Report ID** fields.

The following table describes the combination of values to specify when you set up printer selections for a report.

|To                                                 |Set the following values                                             |
|---------------------------------------------------|---------------------------------------------------------------------|
|Print a report to a specific printer for all users |Specify values in the **Report ID** and **Printer Name** fields and leave the **User ID** field blank.|
|Print all reports to a specific printer for a specific user|Specify values in the **User ID** and **Printer Name** fields and leave the **Report ID** field blank.|
|Set the default printer for all reports|Specify a value in the **Printer Name** field and leave the **User ID** and **Report ID** fields blank.|
|Print a specific report to the user’s default printer|Specify a value in the **Report ID** field and leave the **Printer Name** and **User ID** fields blank.|
|Print a specific report to a specific printer for a specific user|Specify values in all three fields.|
-->

## <a name="see-also"></a>Consulte también
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Ejecutar procesos](ui-how-run-batch-jobs.md)  
[Enviar documentos por correo electrónico](ui-how-send-documents-email.md)  

