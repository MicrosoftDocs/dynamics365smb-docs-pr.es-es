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
ms.lasthandoff: 09/11/2017

---
# <a name="reporting-sales-tax-and-goodsservices-tax-in-canada"></a><span data-ttu-id="69b1c-103">Informes del impuesto sobre bienes y servicios e impuesto de ventas en Canadá</span><span class="sxs-lookup"><span data-stu-id="69b1c-103">Reporting Sales Tax and Goods/Services Tax in Canada</span></span>
<span data-ttu-id="69b1c-104">En Canadá, cuando un proveedor no tiene una empresa física en la provincia en la que se realizan las compras, el proveedor solo aplicará el impuesto sobre bienes y servicios (GST) y el impuesto armonizado de ventas (HST).</span><span class="sxs-lookup"><span data-stu-id="69b1c-104">In Canada, when a vendor does not have a business presence in the province in which purchases are made, the vendor will charge the Goods and Services Tax (GST) or Harmonized Sales Tax (HST) only.</span></span> <span data-ttu-id="69b1c-105">Sin embargo, si la provincia tiene un impuesto de ventas provincial (PST), el comprador debe calcular el PST y pagarlo directamente a la provincia.</span><span class="sxs-lookup"><span data-stu-id="69b1c-105">However, if the province has a Provincial Sales Tax (PST), then the purchaser must still calculate the PST and pay it directly to the province.</span></span> <span data-ttu-id="69b1c-106">Cuando se selecciona un código de área del impuesto provincial, [!INCLUDE[d365fin](includes/d365fin_md.md)] lo usa para calcular el PST y registrarlo para que haya una deuda tributaria tanto en los registros del libro mayor como en los de los movimientos de impuestos.</span><span class="sxs-lookup"><span data-stu-id="69b1c-106">When a Provincial Tax Area Code is selected, [!INCLUDE[d365fin](includes/d365fin_md.md)] uses it to calculate the PST and post it so that there is a tax liability in both the general ledger and the tax entry records.</span></span> <span data-ttu-id="69b1c-107">Por lo tanto, el código de área de impuestos que se seleccione solo debe estar presente cuando se incluya el PST, no el GST.</span><span class="sxs-lookup"><span data-stu-id="69b1c-107">Therefore, the tax area code selected here should be one where only the PST is included, not the GST.</span></span>  

<span data-ttu-id="69b1c-108">Para obtener más información acerca del impuesto de ventas, consulte [Impuesto de ventas y grupos de impuestos en EE. UU. y Canadá](us-finance-sales-tax.md).</span><span class="sxs-lookup"><span data-stu-id="69b1c-108">For more information about sales tax, see [Sales Tax and Tax Groups in the US and Canada](us-finance-sales-tax.md).</span></span>  

## <a name="submitting-the-gsthst-file"></a><span data-ttu-id="69b1c-109">Enviar el archivo de GST o HST</span><span class="sxs-lookup"><span data-stu-id="69b1c-109">Submitting the GST/HST File</span></span>
<span data-ttu-id="69b1c-110">La información de impuestos en documentos de compra se usa para generar una transferencia de archivos en línea de GST o HST que debe proporcionarlo a las autoridades fiscales.</span><span class="sxs-lookup"><span data-stu-id="69b1c-110">The tax information in purchase documents is used to generate a GST/HST online file transfer that you must provide to the tax authorities.</span></span> <span data-ttu-id="69b1c-111">Este campo incluye el impuesto sobre bienes y servicios (GST) y el impuesto armonizado de ventas (HST).</span><span class="sxs-lookup"><span data-stu-id="69b1c-111">This file includes goods and services tax (GST) and harmonized sales tax (HST).</span></span> <span data-ttu-id="69b1c-112">El archivo se crea en el formato .tax, que se puede transferir en línea.</span><span class="sxs-lookup"><span data-stu-id="69b1c-112">The file is created in a .tax file format, which can be transferred online.</span></span>  

## <a name="see-also"></a><span data-ttu-id="69b1c-113">Consulte también</span><span class="sxs-lookup"><span data-stu-id="69b1c-113">See Also</span></span>
[<span data-ttu-id="69b1c-114">Finanzas</span><span class="sxs-lookup"><span data-stu-id="69b1c-114">Finance</span></span>](finance.md)  
[<span data-ttu-id="69b1c-115">Configurar las finanzas</span><span class="sxs-lookup"><span data-stu-id="69b1c-115">Setting Up Finance</span></span>](finance-setup-finance.md)  
[<span data-ttu-id="69b1c-116">Impuesto de ventas y grupos de impuestos en EE. UU. y Canadá</span><span class="sxs-lookup"><span data-stu-id="69b1c-116">Sales Tax and Tax Groups in the US and Canada</span></span>](us-finance-sales-tax.md)  
<span data-ttu-id="69b1c-117">[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="69b1c-117">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

