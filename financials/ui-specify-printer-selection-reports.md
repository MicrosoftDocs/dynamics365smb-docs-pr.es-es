---
title: "Configuración informes para imprimir en impresoras específicas | Documentos de Microsoft"
description: "Obtenga información sobre cómo especificar una impresora para un informe y usar la ventana Selección impresoras."
services: project-madeira
documentationcenter: 
author: SusanneWindfeldPedersen
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: online printing
ms.date: 03/29/2017
ms.author: solsen
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 42fb4adbcc01c443722fe90bb59edafceb34ff06
ms.contentlocale: es-es
ms.lasthandoff: 09/22/2017

---
# <a name="specify-printer-selection-for-reports"></a><span data-ttu-id="fbfce-103">Especificar selección de impresora para informes</span><span class="sxs-lookup"><span data-stu-id="fbfce-103">Specify Printer Selection for Reports</span></span>
<span data-ttu-id="fbfce-104">Esta página está vacía porque no puede configurar impresoras específicas para informes específicos.</span><span class="sxs-lookup"><span data-stu-id="fbfce-104">This page is empty because you cannot yet set up specific printers for specific reports.</span></span> <span data-ttu-id="fbfce-105">Estamos trabajando para resolver este problema.</span><span class="sxs-lookup"><span data-stu-id="fbfce-105">We are working on solving this.</span></span>

<span data-ttu-id="fbfce-106">Mientras tanto, si desea imprimir un informe, tiene que descargarlo como documento PDF primero, eligiendo el botón **Enviar**.</span><span class="sxs-lookup"><span data-stu-id="fbfce-106">In the meantime, when you want to print a report, you have to download the report as a PDF document first by choosing the **Send to** button.</span></span> <span data-ttu-id="fbfce-107">A continuación, seleccione el tipo de archivo como se descargará el informe; debe elegir **Documento PDF**.</span><span class="sxs-lookup"><span data-stu-id="fbfce-107">Then you select the type of file to download the report as, and here you should pick **PDF Document**.</span></span> <span data-ttu-id="fbfce-108">Ahora puede abrir el documento de PDF inmediatamente e imprimirlo, o guardarlo e imprimirlo más adelante.</span><span class="sxs-lookup"><span data-stu-id="fbfce-108">Now, you can either open the PDF document right-away and print it, or save it and print it later.</span></span>

<!--

You can set up reports so that they must be printed on a specific printer. The following are some uses of printer selection:

- You can print reports on special company letterhead.
- You can print reports on different paper sizes.
- You can print reports on the default printer of a specified employee.

You use the **Printer Selections** window to set different values to obtain different output. If you set a specific printer selection, then it takes precedence over a more general printer selection. For example, you can set a printer selection that has values in the **User ID**, **Report ID**, and **Printer Name** fields. This printer selection takes precedence over a printer selection that has blank entries in the **User ID** or **Report ID** fields.

The following table describes the combination of values to specify when you set up printer selections for a report.

|To                                                 |Set the following values                                             |
|---------------------------------------------------|---------------------------------------------------------------------|
|Print a report to a specific printer for all users |Specify values in the **Report ID** and **Printer Name** fields and leave the **User ID** field blank.|
|Print all reports to a specific printer for a specific user|Specify values in the **User ID** and **Printer Name** fields and leave the **Report ID** field blank.|
|Set the default printer for all reports|Specify a value in the **Printer Name** field and leave the **User ID** and **Report ID** fields blank.|
|Print a specific report to the user’s default printer|Specify a value in the **Report ID** field and leave the **Printer Name** and **User ID** fields blank.|
|Print a specific report to a specific printer for a specific user|Specify values in all three fields.|
-->

## <a name="see-also"></a><span data-ttu-id="fbfce-109">Consulte también</span><span class="sxs-lookup"><span data-stu-id="fbfce-109">See Also</span></span>
<span data-ttu-id="fbfce-110">[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="fbfce-110">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="fbfce-111">Ejecución de trabajos por lotes</span><span class="sxs-lookup"><span data-stu-id="fbfce-111">How to: Run Batch Jobs</span></span>](ui-how-run-batch-jobs.md)  
[<span data-ttu-id="fbfce-112">Enviar documentos por correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="fbfce-112">How to: Send Documents by Email</span></span>](ui-how-send-documents-email.md)  

