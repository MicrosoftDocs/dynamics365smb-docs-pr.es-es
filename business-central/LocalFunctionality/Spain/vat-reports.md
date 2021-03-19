---
title: Informes IVA
description: El IVA se aplica a las transacciones que involucran bienes y servicios en España o bienes importados a España. La siguiente información proporciona más detalles sobre la funcionalidad de IVA.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: bca656527f7ba680d39fa76de2bf75db1f180935
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5384035"
---
# <a name="vat-reports-in-the-spanish-version"></a><span data-ttu-id="1b45b-104">Informes de IVA en la versión en español</span><span class="sxs-lookup"><span data-stu-id="1b45b-104">VAT Reports in the Spanish Version</span></span>
<span data-ttu-id="1b45b-105">El IVA se aplica a las transacciones que involucran bienes y servicios en España o bienes importados a España.</span><span class="sxs-lookup"><span data-stu-id="1b45b-105">VAT is charged on transactions that involve goods and services in Spain or goods imported into Spain.</span></span> <span data-ttu-id="1b45b-106">La siguiente información proporciona más detalles sobre la funcionalidad de IVA.</span><span class="sxs-lookup"><span data-stu-id="1b45b-106">The following information provides more details about VAT functionality.</span></span>  

## <a name="equivalence-charge"></a><span data-ttu-id="1b45b-107">Recargo de equivalencia</span><span class="sxs-lookup"><span data-stu-id="1b45b-107">Equivalence Charge</span></span>  
<span data-ttu-id="1b45b-108">El impuesto de recargo de equivalencia (RE) se aplica a las actividades que no siguen las reglas del IVA.</span><span class="sxs-lookup"><span data-stu-id="1b45b-108">Equivalence Charge (EC) tax applies to activities that do not follow VAT rules.</span></span> <span data-ttu-id="1b45b-109">Según las reglas RE, las empresas deben pagar un recargo a sus proveedores además del IVA.</span><span class="sxs-lookup"><span data-stu-id="1b45b-109">According to EC rules, companies must pay a surcharge to their vendors in addition to VAT.</span></span> <span data-ttu-id="1b45b-110">Sin embargo, en las facturas de ventas sólo pueden cargar el IVA sin el recargo.</span><span class="sxs-lookup"><span data-stu-id="1b45b-110">However, they can only charge VAT without the surcharge on sales invoices.</span></span>  

### <a name="vat-with-ec-percentage"></a><span data-ttu-id="1b45b-111">IVA con porcentaje RE</span><span class="sxs-lookup"><span data-stu-id="1b45b-111">VAT with EC Percentage</span></span>  
<span data-ttu-id="1b45b-112">Los grupos de registro general predefinidos tienen un porcentaje RE, además de su porcentaje de IVA.</span><span class="sxs-lookup"><span data-stu-id="1b45b-112">Preset general posting groups have an EC percentage in addition to their VAT percentage.</span></span> <span data-ttu-id="1b45b-113">Aunque el seguimiento del RE se efectúa por separado, los valores de ambos impuestos se fusionan con el IVA siempre que es posible.</span><span class="sxs-lookup"><span data-stu-id="1b45b-113">Although the EC is tracked separately, both tax values are merged with VAT when it is possible.</span></span> <span data-ttu-id="1b45b-114">Si en la tabla de grupo contable el porcentaje RE es un campo independiente, el RE se fusiona con el valor de la columna **%IVA**.</span><span class="sxs-lookup"><span data-stu-id="1b45b-114">If the EC percentage is a separate field in the posting group, the EC is merged with the value in the **VAT %** column.</span></span>  

<span data-ttu-id="1b45b-115">Para imprimir libros de facturas emitidas y recibidas, el porcentaje de IVA y los porcentajes de RE se muestran en la tabla **Mov. IVA** durante el registro.</span><span class="sxs-lookup"><span data-stu-id="1b45b-115">For printing sales and purchase invoice books, the VAT percent and EC percentages are displayed in the **VAT Entry** table during posting.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="1b45b-116">Si el artículo no tiene IVA gravable, se muestra automáticamente el número 0 en el campo **% IVA** en las páginas de información de IVA.</span><span class="sxs-lookup"><span data-stu-id="1b45b-116">If the item has no taxable VAT, 0 is automatically displayed in the **VAT %** field in the VAT information pages.</span></span>  

### <a name="telematic-vat"></a><span data-ttu-id="1b45b-117">IVA Telemático</span><span class="sxs-lookup"><span data-stu-id="1b45b-117">Telematic VAT</span></span>  
<span data-ttu-id="1b45b-118">Mediante el IVA telemático se pueden diseñar y generar los informes fiscales mensuales y anuales como archivos electrónicos o impresos.</span><span class="sxs-lookup"><span data-stu-id="1b45b-118">With telematic VAT you can design and generate monthly and yearly tax reports as electronic files or printed files.</span></span> <span data-ttu-id="1b45b-119">Estos informes se pueden enviar a la administración fiscal a través de un programa externo o de un archivo XML del sitio Web de la administración.</span><span class="sxs-lookup"><span data-stu-id="1b45b-119">You can submit these reports to the tax authorities using a third-party program or an XML file from the tax authorities' website.</span></span>  

### <a name="vat-statement"></a><span data-ttu-id="1b45b-120">Declaración IVA</span><span class="sxs-lookup"><span data-stu-id="1b45b-120">VAT Statement</span></span>  
<span data-ttu-id="1b45b-121">La declaración de IVA muestra los importes e importes base de IVA en columnas diferentes.</span><span class="sxs-lookup"><span data-stu-id="1b45b-121">The VAT statement displays VAT amounts and base amounts in different columns.</span></span>  

<span data-ttu-id="1b45b-122">En la tabla **Nombre declar. IVA** hay dos tipos de plantillas de informe:</span><span class="sxs-lookup"><span data-stu-id="1b45b-122">There are two report template types in the **VAT Statement Name** table:</span></span>  

- <span data-ttu-id="1b45b-123">**Informe 1 columna**</span><span class="sxs-lookup"><span data-stu-id="1b45b-123">**One-Column Report**</span></span>  
- <span data-ttu-id="1b45b-124">**Informe 2 columnas**</span><span class="sxs-lookup"><span data-stu-id="1b45b-124">**Two-Columns Report**</span></span>  

### <a name="vat-vies-declaration"></a><span data-ttu-id="1b45b-125">IVA - declaración VIES</span><span class="sxs-lookup"><span data-stu-id="1b45b-125">VAT-VIES Declaration</span></span>  
<span data-ttu-id="1b45b-126">Mediante IVA - declaración VIES se puede ejecutar un archivo por lotes para generar los informes de ventas de la Union Europea (UE).</span><span class="sxs-lookup"><span data-stu-id="1b45b-126">With VAT-VIES declaration you can run a batch file to generate European Union (EU) sales reports.</span></span> <span data-ttu-id="1b45b-127">El archivo por lotes exporta los movimientos al formato de archivo requerido para enviarlo a la aduana y a la administración fiscal.</span><span class="sxs-lookup"><span data-stu-id="1b45b-127">The batch file exports the entries in the required file format for submission to customs and tax authorities.</span></span>  

## <a name="see-also"></a><span data-ttu-id="1b45b-128">Consulte también</span><span class="sxs-lookup"><span data-stu-id="1b45b-128">See Also</span></span>  
 <span data-ttu-id="1b45b-129">[Funcionalidad local para España](spain-local-functionality.md) </span><span class="sxs-lookup"><span data-stu-id="1b45b-129">[Spain Local Functionality](spain-local-functionality.md) </span></span>  
 <span data-ttu-id="1b45b-130">[Informe 340](report-340.md) </span><span class="sxs-lookup"><span data-stu-id="1b45b-130">[Report 340](report-340.md) </span></span>  
 [<span data-ttu-id="1b45b-131">Informe 347</span><span class="sxs-lookup"><span data-stu-id="1b45b-131">Report 347</span></span>](report-347.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]