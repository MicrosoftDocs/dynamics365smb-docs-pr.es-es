---
title: Informe 347
description: "El Informe 347 es un informe anual obligatorio que todas las empresas deben enviar a la administración fiscal para reflejar las compras o ventas de un periodo determinado. Este informe también incluye entradas como el pago en efectivo que se recibió en el período."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: ca4375f7f15b99a799ef5b95abd54bd878532a99
ms.contentlocale: es-es
ms.lasthandoff: 03/22/2018

---
# <a name="report-347"></a><span data-ttu-id="bfa1d-104">Informe 347</span><span class="sxs-lookup"><span data-stu-id="bfa1d-104">Report 347</span></span>
<span data-ttu-id="bfa1d-105">El **Informe 347** es un informe anual obligatorio que todas las empresas deben enviar a la administración fiscal para reflejar las compras o ventas de un periodo determinado.</span><span class="sxs-lookup"><span data-stu-id="bfa1d-105">The **Report 347** report is a required annual report sent by all companies to the tax authorities to reflect the sales or purchases in a given period.</span></span> <span data-ttu-id="bfa1d-106">Este informe también incluye entradas como el pago en efectivo que se recibió en el período.</span><span class="sxs-lookup"><span data-stu-id="bfa1d-106">This report also includes entries such as payment in cash that was received in the period.</span></span> <span data-ttu-id="bfa1d-107">El **informe 347** se genera en un formato que ha aprobado la administración fiscal.</span><span class="sxs-lookup"><span data-stu-id="bfa1d-107">The **Report 347** report is generated in a format that is approved by the tax authorities.</span></span> <span data-ttu-id="bfa1d-108">Este archivo puede cargarse en el sitio web de la Agencia Tributaria o enviarse en CD-ROM.</span><span class="sxs-lookup"><span data-stu-id="bfa1d-108">This file can be uploaded to the Spanish Tax Agency website or submitted on CD-ROM.</span></span> <span data-ttu-id="bfa1d-109">Para obtener más información, consulte el sitio web de la [Agencia Tributaria](http://www.aeat.es/wps/portal/Home?channel=1af861cd949a1010VgnVCM100000d7005a80____&ver=L&site=56d8237c0bc1ff00VgnVCM100000d7005a80____&idioma=es_ES&menu=0&img=0).</span><span class="sxs-lookup"><span data-stu-id="bfa1d-109">For more information, see the [Spanish Tax Agency](http://www.aeat.es/wps/portal/Home?channel=1af861cd949a1010VgnVCM100000d7005a80____&ver=L&site=56d8237c0bc1ff00VgnVCM100000d7005a80____&idioma=es_ES&menu=0&img=0) website.</span></span>  

## <a name="file-format-for-report-347"></a><span data-ttu-id="bfa1d-110">Formato de archivo del informe 347</span><span class="sxs-lookup"><span data-stu-id="bfa1d-110">File Format for Report 347</span></span>  
<span data-ttu-id="bfa1d-111">El formato de archivo del **Informe 347** incluye al menos una empresa responsable, un, deponente y un registro de cliente/proveedor.</span><span class="sxs-lookup"><span data-stu-id="bfa1d-111">The file format for **Report 347** includes at least one responsible company, a deponent, and a customer/vendor register.</span></span> <span data-ttu-id="bfa1d-112">Una empresa responsable es una empresa que envía la información a la Agencia Tributaria.</span><span class="sxs-lookup"><span data-stu-id="bfa1d-112">A responsible company is a company that submits the information to the Spanish Tax Agency.</span></span> <span data-ttu-id="bfa1d-113">La información de deponente se obtiene de la tabla **Información empresa** y del formulario de solicitud.</span><span class="sxs-lookup"><span data-stu-id="bfa1d-113">Deponent information comes from the **Company Information** table and the request form.</span></span> <span data-ttu-id="bfa1d-114">La información de cliente se obtiene de las tablas **Cliente**, **Mov. cliente** y **Mov. contabilidad**.</span><span class="sxs-lookup"><span data-stu-id="bfa1d-114">Customer information comes from the **Customer** table, the **Cust. Ledger Entry** table, and the **G/L Entry** table.</span></span> <span data-ttu-id="bfa1d-115">La información de proveedor se obtiene de las tablas **Proveedor** y **Mov. proveedor**.</span><span class="sxs-lookup"><span data-stu-id="bfa1d-115">Vendor information comes from the **Vendor** table and the **Vendor Ledger Entry** table.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="bfa1d-116">Si no hay ningún registro de archivo, el archivo no se crea y se muestra un mensaje de error.</span><span class="sxs-lookup"><span data-stu-id="bfa1d-116">If there are no file records, the file is not created and an error message is displayed.</span></span>  

## <a name="file-format-restrictions-for-report-347"></a><span data-ttu-id="bfa1d-117">Restricciones de formato de archivo del informe 347</span><span class="sxs-lookup"><span data-stu-id="bfa1d-117">File Format Restrictions for Report 347</span></span>  
<span data-ttu-id="bfa1d-118">Antes de crear el **Informe 347**, debe tener en cuenta las siguientes restricciones de formato de archivo:</span><span class="sxs-lookup"><span data-stu-id="bfa1d-118">Before creating **Report 347**, the following file format restrictions will be considered:</span></span>  

- <span data-ttu-id="bfa1d-119">Todos los importes deben ser positivos.</span><span class="sxs-lookup"><span data-stu-id="bfa1d-119">All amounts must be positive.</span></span>  
- <span data-ttu-id="bfa1d-120">Todo el texto deber estar en mayúsculas.</span><span class="sxs-lookup"><span data-stu-id="bfa1d-120">All text must be capitalized.</span></span>  
- <span data-ttu-id="bfa1d-121">Todos los campos alfanuméricos se deben alinear a la izquierda.</span><span class="sxs-lookup"><span data-stu-id="bfa1d-121">All alphanumeric fields must be left-aligned.</span></span>  
- <span data-ttu-id="bfa1d-122">Todos los campos numéricos deben ir alineados a la derecha.</span><span class="sxs-lookup"><span data-stu-id="bfa1d-122">All numeric fields must be right-aligned.</span></span>  
- <span data-ttu-id="bfa1d-123">Si la empresa recibe pagos en efectivo que superan el límite oficial predefinido para estas transacciones, se debe incluir un año de cuatro dígitos.</span><span class="sxs-lookup"><span data-stu-id="bfa1d-123">If the company receives payments in cash that are over the predefined official threshold for these transactions, a four-digit year must be included.</span></span> <span data-ttu-id="bfa1d-124">El año indica cuándo se contabilizaron las facturas relacionadas con cuentas por cobrar.</span><span class="sxs-lookup"><span data-stu-id="bfa1d-124">The year indicates when the invoices that are related to receivables were posted.</span></span>  
- <span data-ttu-id="bfa1d-125">Los caracteres especiales deben convertirse a caracteres estándar.</span><span class="sxs-lookup"><span data-stu-id="bfa1d-125">Special characters must be converted to standard characters.</span></span>  
- <span data-ttu-id="bfa1d-126">Si no contienen ningún valor, los campos alfanuméricos se dejarán en blanco y los campos numéricos se rellenarán con ceros.</span><span class="sxs-lookup"><span data-stu-id="bfa1d-126">If the field has no value, it will be blank for alphanumeric fields and populated with zeros for numeric fields.</span></span>  

## <a name="see-also"></a><span data-ttu-id="bfa1d-127">Consulte también</span><span class="sxs-lookup"><span data-stu-id="bfa1d-127">See Also</span></span>  
 <span data-ttu-id="bfa1d-128">[Funcionalidad local para España](spain-local-functionality.md) </span><span class="sxs-lookup"><span data-stu-id="bfa1d-128">[Spain Local Functionality](spain-local-functionality.md) </span></span>  
 [<span data-ttu-id="bfa1d-129">Crear el informe 347</span><span class="sxs-lookup"><span data-stu-id="bfa1d-129">Create Report 347</span></span>](how-to-create-report-347.md)

