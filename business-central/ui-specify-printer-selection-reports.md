---
title: Configuración informes para imprimir en impresoras específicas | Documentos de Microsoft
description: Obtenga información sobre cómo especificar una impresora para un informe y usar la página Selección impresoras.
services: project-madeira
documentationcenter: ''
author: SusanneWindfeldPedersen
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: online printing
ms.date: 10/01/2019
ms.author: solsen
ms.openlocfilehash: 0c3a57906c32751639585e542a60d931174d594b
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/01/2019
ms.locfileid: "2315041"
---
# <a name="specify-printer-selection-for-reports"></a><span data-ttu-id="cfc44-103">Especificar selección de impresora para informes</span><span class="sxs-lookup"><span data-stu-id="cfc44-103">Specify Printer Selection for Reports</span></span>
<span data-ttu-id="cfc44-104">Esta página está vacía porque no puede configurar impresoras específicas para informes específicos.</span><span class="sxs-lookup"><span data-stu-id="cfc44-104">This page is empty because you cannot yet set up specific printers for specific reports.</span></span> <span data-ttu-id="cfc44-105">Estamos trabajando para resolver este problema.</span><span class="sxs-lookup"><span data-stu-id="cfc44-105">We are working on solving this.</span></span>

<span data-ttu-id="cfc44-106">Mientras tanto, si desea imprimir un informe, tiene que descargarlo como documento PDF primero, eligiendo el botón **Enviar**.</span><span class="sxs-lookup"><span data-stu-id="cfc44-106">In the meantime, when you want to print a report, you have to download the report as a PDF document first by choosing the **Send to** button.</span></span> <span data-ttu-id="cfc44-107">A continuación, seleccione el tipo de archivo como se descargará el informe; debe elegir **Documento PDF**.</span><span class="sxs-lookup"><span data-stu-id="cfc44-107">Then you select the type of file to download the report as, and here you should pick **PDF Document**.</span></span> <span data-ttu-id="cfc44-108">Ahora puede abrir el documento de PDF inmediatamente e imprimirlo, o guardarlo e imprimirlo más adelante.</span><span class="sxs-lookup"><span data-stu-id="cfc44-108">Now, you can either open the PDF document right-away and print it, or save it and print it later.</span></span>

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

## <a name="see-also"></a><span data-ttu-id="cfc44-109">Consulte también</span><span class="sxs-lookup"><span data-stu-id="cfc44-109">See Also</span></span>
<span data-ttu-id="cfc44-110">[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="cfc44-110">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="cfc44-111">Ejecutar procesos</span><span class="sxs-lookup"><span data-stu-id="cfc44-111">Run Batch Jobs</span></span>](ui-how-run-batch-jobs.md)  
[<span data-ttu-id="cfc44-112">Enviar documentos por correo electrónico</span><span class="sxs-lookup"><span data-stu-id="cfc44-112">Send Documents by Email</span></span>](ui-how-send-documents-email.md)  
