---
title: Informe 347
description: El Informe 347 es un informe anual obligatorio que todas las empresas deben enviar a la administración fiscal para reflejar las compras o ventas de un periodo determinado. Este informe también incluye entradas como el pago en efectivo que se recibió en el período.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 795882a004f859a30b672a79bbfdd88c256a6d17
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 03/31/2021
ms.locfileid: "5788214"
---
# <a name="report-347"></a><span data-ttu-id="59882-104">Informe 347</span><span class="sxs-lookup"><span data-stu-id="59882-104">Report 347</span></span>
<span data-ttu-id="59882-105">El **Informe 347** es un informe anual obligatorio que todas las empresas deben enviar a la administración fiscal para reflejar las compras o ventas de un periodo determinado.</span><span class="sxs-lookup"><span data-stu-id="59882-105">The **Report 347** report is a required annual report sent by all companies to the tax authorities to reflect the sales or purchases in a given period.</span></span> <span data-ttu-id="59882-106">Este informe también incluye entradas como el pago en efectivo que se recibió en el período.</span><span class="sxs-lookup"><span data-stu-id="59882-106">This report also includes entries such as payment in cash that was received in the period.</span></span> <span data-ttu-id="59882-107">El **informe 347** se genera en un formato que ha aprobado la administración fiscal.</span><span class="sxs-lookup"><span data-stu-id="59882-107">The **Report 347** report is generated in a format that is approved by the tax authorities.</span></span> <span data-ttu-id="59882-108">Este archivo puede cargarse en el sitio web de la Agencia Tributaria o enviarse en CD-ROM.</span><span class="sxs-lookup"><span data-stu-id="59882-108">This file can be uploaded to the Spanish Tax Agency website or submitted on CD-ROM.</span></span> <span data-ttu-id="59882-109">Para obtener más información, consulte el sitio web de la [Agencia Tributaria](https://www.agenciatributaria.es/AEAT.internet/en_gb/Inicio.shtml).</span><span class="sxs-lookup"><span data-stu-id="59882-109">For more information, see the [Spanish Tax Agency](https://www.agenciatributaria.es/AEAT.internet/en_gb/Inicio.shtml) website.</span></span>  

## <a name="file-format-for-report-347"></a><span data-ttu-id="59882-110">Formato de archivo del informe 347</span><span class="sxs-lookup"><span data-stu-id="59882-110">File Format for Report 347</span></span>  
<span data-ttu-id="59882-111">El formato de archivo del **Informe 347** incluye al menos una empresa responsable, un, deponente y un registro de cliente/proveedor.</span><span class="sxs-lookup"><span data-stu-id="59882-111">The file format for **Report 347** includes at least one responsible company, a deponent, and a customer/vendor register.</span></span> <span data-ttu-id="59882-112">Una empresa responsable es una empresa que envía la información a la Agencia Tributaria.</span><span class="sxs-lookup"><span data-stu-id="59882-112">A responsible company is a company that submits the information to the Spanish Tax Agency.</span></span> <span data-ttu-id="59882-113">La información de deponente se obtiene de la tabla **Información empresa** y del formulario de solicitud.</span><span class="sxs-lookup"><span data-stu-id="59882-113">Deponent information comes from the **Company Information** table and the request form.</span></span> <span data-ttu-id="59882-114">La información de cliente se obtiene de las tablas **Cliente**, **Mov. cliente** y **Mov. contabilidad**.</span><span class="sxs-lookup"><span data-stu-id="59882-114">Customer information comes from the **Customer** table, the **Cust. Ledger Entry** table, and the **G/L Entry** table.</span></span> <span data-ttu-id="59882-115">La información de proveedor se obtiene de las tablas **Proveedor** y **Mov. proveedor**.</span><span class="sxs-lookup"><span data-stu-id="59882-115">Vendor information comes from the **Vendor** table and the **Vendor Ledger Entry** table.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="59882-116">Si no hay ningún registro de archivo, el archivo no se crea y se muestra un mensaje de error.</span><span class="sxs-lookup"><span data-stu-id="59882-116">If there are no file records, the file is not created and an error message is displayed.</span></span>  

## <a name="file-format-restrictions-for-report-347"></a><span data-ttu-id="59882-117">Restricciones de formato de archivo del informe 347</span><span class="sxs-lookup"><span data-stu-id="59882-117">File Format Restrictions for Report 347</span></span>  
<span data-ttu-id="59882-118">Antes de crear el **Informe 347**, debe tener en cuenta las siguientes restricciones de formato de archivo:</span><span class="sxs-lookup"><span data-stu-id="59882-118">Before creating **Report 347**, the following file format restrictions will be considered:</span></span>  

- <span data-ttu-id="59882-119">Todos los importes deben ser positivos.</span><span class="sxs-lookup"><span data-stu-id="59882-119">All amounts must be positive.</span></span>  
- <span data-ttu-id="59882-120">Todo el texto deber estar en mayúsculas.</span><span class="sxs-lookup"><span data-stu-id="59882-120">All text must be capitalized.</span></span>  
- <span data-ttu-id="59882-121">Todos los campos alfanuméricos se deben alinear a la izquierda.</span><span class="sxs-lookup"><span data-stu-id="59882-121">All alphanumeric fields must be left-aligned.</span></span>  
- <span data-ttu-id="59882-122">Todos los campos numéricos deben ir alineados a la derecha.</span><span class="sxs-lookup"><span data-stu-id="59882-122">All numeric fields must be right-aligned.</span></span>  
- <span data-ttu-id="59882-123">Si la empresa recibe pagos en efectivo que superan el límite oficial predefinido para estas transacciones, se debe incluir un año de cuatro dígitos.</span><span class="sxs-lookup"><span data-stu-id="59882-123">If the company receives payments in cash that are over the predefined official threshold for these transactions, a four-digit year must be included.</span></span> <span data-ttu-id="59882-124">El año indica cuándo se contabilizaron las facturas relacionadas con cuentas por cobrar.</span><span class="sxs-lookup"><span data-stu-id="59882-124">The year indicates when the invoices that are related to receivables were posted.</span></span>  
- <span data-ttu-id="59882-125">Los caracteres especiales deben convertirse a caracteres estándar.</span><span class="sxs-lookup"><span data-stu-id="59882-125">Special characters must be converted to standard characters.</span></span>  
- <span data-ttu-id="59882-126">Si no contienen ningún valor, los campos alfanuméricos se dejarán en blanco y los campos numéricos se rellenarán con ceros.</span><span class="sxs-lookup"><span data-stu-id="59882-126">If the field has no value, it will be blank for alphanumeric fields and populated with zeros for numeric fields.</span></span>  

## <a name="see-also"></a><span data-ttu-id="59882-127">Consulte también</span><span class="sxs-lookup"><span data-stu-id="59882-127">See Also</span></span>  
 <span data-ttu-id="59882-128">[Funcionalidad local para España](spain-local-functionality.md) </span><span class="sxs-lookup"><span data-stu-id="59882-128">[Spain Local Functionality](spain-local-functionality.md) </span></span>  
 [<span data-ttu-id="59882-129">Crear el informe 347</span><span class="sxs-lookup"><span data-stu-id="59882-129">Create Report 347</span></span>](how-to-create-report-347.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]