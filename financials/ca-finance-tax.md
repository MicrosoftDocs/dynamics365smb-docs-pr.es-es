---
title: "Impuesto de ventas en Canadá | Documentos de Microsoft"
description: "Obtenga información sobre el impuesto de ventas local y el impuesto sobre bienes y servicios en Canadá."
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: sales tax, local
ms.date: 06/02/2017
ms.author: edupont
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 571b11f4f18ffd194bdfe1d1d412bca87df4b868
ms.contentlocale: es-es
ms.lasthandoff: 07/07/2017


---
# <a name="reporting-sales-tax-and-goodsservices-tax-in-canada"></a>Informes del impuesto sobre bienes y servicios e impuesto de ventas en Canadá
En Canadá, cuando un proveedor no tiene una empresa física en la provincia en la que se realizan las compras, el proveedor solo aplicará el impuesto sobre bienes y servicios (GST) y el impuesto armonizado de ventas (HST). Sin embargo, si la provincia tiene un impuesto de ventas provincial (PST), el comprador debe calcular el PST y pagarlo directamente a la provincia. Cuando se selecciona un código de área del impuesto provincial, [!INCLUDE[d365fin](includes/d365fin_md.md)] lo usa para calcular el PST y registrarlo para que haya una deuda tributaria tanto en los registros del libro mayor como en los de los movimientos de impuestos. Por lo tanto, el código de área de impuestos que se seleccione solo debe estar presente cuando se incluya el PST, no el GST.  

Para obtener más información acerca del impuesto de ventas, consulte [Impuesto de ventas y grupos de impuestos en EE. UU. y Canadá](us-finance-sales-tax.md).  

## <a name="submitting-the-gsthst-file"></a>Enviar el archivo de GST o HST
La información de impuestos en documentos de compra se usa para generar una transferencia de archivos en línea de GST o HST que debe proporcionarlo a las autoridades fiscales. Este campo incluye el impuesto sobre bienes y servicios (GST) y el impuesto armonizado de ventas (HST). El archivo se crea en el formato .tax, que se puede transferir en línea.  

## <a name="see-also"></a>Consulte también
[Finanzas](finance.md)  
[Configurar las finanzas](finance-setup-finance.md)  
[Impuesto de ventas y grupos de impuestos en EE. UU. y Canadá](us-finance-sales-tax.md)  
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

