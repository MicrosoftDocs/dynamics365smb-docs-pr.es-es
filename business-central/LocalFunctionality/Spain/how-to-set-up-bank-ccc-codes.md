---
title: Configuración de códigos CCC de bancos
description: El Código Cuenta Cliente (CCC) es un código de cuenta único usado por los bancos para identificar a sus clientes. El código CCC se imprime en los documentos bancarios, como cheques y extractos.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: c879dbdbf21f89d5764a14fed7e313e2501cff42
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 03/31/2021
ms.locfileid: "5775707"
---
# <a name="set-up-bank-ccc-codes"></a><span data-ttu-id="e80b5-104">Configurar códigos CCC de bancos</span><span class="sxs-lookup"><span data-stu-id="e80b5-104">Set Up Bank CCC Codes</span></span>
<span data-ttu-id="e80b5-105">El Código Cuenta Cliente (CCC) es un código de cuenta único usado por los bancos para identificar a sus clientes.</span><span class="sxs-lookup"><span data-stu-id="e80b5-105">Código Cuenta Cliente (CCC) is a unique account code used by banks to identify their customers.</span></span> <span data-ttu-id="e80b5-106">El código CCC se imprime en los documentos bancarios, como cheques y extractos.</span><span class="sxs-lookup"><span data-stu-id="e80b5-106">The CCC code is printed on bank documents such as checks and statements.</span></span>  

<span data-ttu-id="e80b5-107">Se pueden configurar códigos CCC en las siguientes ubicaciones:</span><span class="sxs-lookup"><span data-stu-id="e80b5-107">You can set up CCC codes in the following locations:</span></span>  

- <span data-ttu-id="e80b5-108">Página **Ficha banco**</span><span class="sxs-lookup"><span data-stu-id="e80b5-108">**Bank Account Card** page</span></span>  
- <span data-ttu-id="e80b5-109">Página **Información de empresa**</span><span class="sxs-lookup"><span data-stu-id="e80b5-109">**Company Information** page</span></span>  
- <span data-ttu-id="e80b5-110">Página **Ficha banco cliente**</span><span class="sxs-lookup"><span data-stu-id="e80b5-110">**Customer Bank Account Card** page</span></span>  
- <span data-ttu-id="e80b5-111">Página **Ficha banco proveedor**</span><span class="sxs-lookup"><span data-stu-id="e80b5-111">**Vendor Bank Account Card** page</span></span>  

<span data-ttu-id="e80b5-112">El procedimiento siguiente describe cómo configurar códigos CCC de banco para su empresa.</span><span class="sxs-lookup"><span data-stu-id="e80b5-112">The following procedure describes how to set up bank CCC codes for your company.</span></span>  

## <a name="to-enter-ccc-codes"></a><span data-ttu-id="e80b5-113">Para introducir códigos CCC</span><span class="sxs-lookup"><span data-stu-id="e80b5-113">To enter CCC codes</span></span>  

1.  <span data-ttu-id="e80b5-114">Elija el icono ![Bombilla que abre la función Dígame](../../media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Información de empresa** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="e80b5-114">Choose the ![Lightbulb that opens the Tell Me feature](../../media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Company Information**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="e80b5-115">Rellene los campos de la ficha desplegable **Pagos**, tal como se describe en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="e80b5-115">On the **Payments** FastTab, fill in the fields as described in the following table.</span></span>  

    |<span data-ttu-id="e80b5-116">Campo</span><span class="sxs-lookup"><span data-stu-id="e80b5-116">Field</span></span>|<span data-ttu-id="e80b5-117">Description</span><span class="sxs-lookup"><span data-stu-id="e80b5-117">Description</span></span>|  
    |---------------------------------|--------------|---------------------------------------|  
    |<span data-ttu-id="e80b5-118">**CCC Cód. banco**</span><span class="sxs-lookup"><span data-stu-id="e80b5-118">**CCC Bank No.**</span></span>|<span data-ttu-id="e80b5-119">1-4</span><span class="sxs-lookup"><span data-stu-id="e80b5-119">1-4</span></span>|<span data-ttu-id="e80b5-120">Identifica el banco en el que se ha abierto la cuenta.</span><span class="sxs-lookup"><span data-stu-id="e80b5-120">Identifies the bank where the account has been opened.</span></span>|  
    |<span data-ttu-id="e80b5-121">**CCC Cód. oficina**</span><span class="sxs-lookup"><span data-stu-id="e80b5-121">**CCC Bank Branch No.**</span></span>|<span data-ttu-id="e80b5-122">5-8</span><span class="sxs-lookup"><span data-stu-id="e80b5-122">5-8</span></span>|<span data-ttu-id="e80b5-123">Identifica el código de la oficina.</span><span class="sxs-lookup"><span data-stu-id="e80b5-123">Identifies the branch code.</span></span> <span data-ttu-id="e80b5-124">Si el banco no utiliza esta referencia, el código de la oficina pueden ser ceros.</span><span class="sxs-lookup"><span data-stu-id="e80b5-124">If the bank does not use this reference, the branch code can be zeros.</span></span>|  
    |<span data-ttu-id="e80b5-125">**CCC Dígito control**</span><span class="sxs-lookup"><span data-stu-id="e80b5-125">**CCC Control Digits**</span></span>|<span data-ttu-id="e80b5-126">9-10</span><span class="sxs-lookup"><span data-stu-id="e80b5-126">9-10</span></span>|<span data-ttu-id="e80b5-127">Identifica los dígitos de control.</span><span class="sxs-lookup"><span data-stu-id="e80b5-127">Identifies the control digits.</span></span>|  
    |<span data-ttu-id="e80b5-128">**CCC Nº cuenta**</span><span class="sxs-lookup"><span data-stu-id="e80b5-128">**CCC Bank Account No.**</span></span>|<span data-ttu-id="e80b5-129">11-20 (España)</span><span class="sxs-lookup"><span data-stu-id="e80b5-129">11-20 (Spain)</span></span><br /><br /> <span data-ttu-id="e80b5-130">11-21 (Portugal)</span><span class="sxs-lookup"><span data-stu-id="e80b5-130">11-21 (Portugal)</span></span>|<span data-ttu-id="e80b5-131">Identifica el número de cuenta, que se puede ajustar con ceros a la izquierda.</span><span class="sxs-lookup"><span data-stu-id="e80b5-131">Identifies the account number, which may be adjusted with preceding zeros.</span></span>|  

<span data-ttu-id="e80b5-132">El siguiente procedimiento describe cómo configurar códigos bancarios CCC para cuentas bancarias de clientes existentes, pero los mismos pasos se aplican a proveedores, cuentas bancarias e información de la compañía.</span><span class="sxs-lookup"><span data-stu-id="e80b5-132">The following procedure describes how to set up bank CCC codes for existing customer bank accounts, but the same steps apply to vendors, bank accounts, and company information.</span></span>  

## <a name="to-set-up-bank-ccc-codes-for-a-customer-bank-account"></a><span data-ttu-id="e80b5-133">Para configurar códigos CCC de banco de un banco cliente</span><span class="sxs-lookup"><span data-stu-id="e80b5-133">To set up bank CCC codes for a customer bank account</span></span>  

1.  <span data-ttu-id="e80b5-134">Elija el icono ![Bombilla que abre la función Dígame](../../media/ui-search/search_small.png "Dígame qué desea hacer"), introduzca **Ficha banco cliente** y luego elija el vínculo relacionado.</span><span class="sxs-lookup"><span data-stu-id="e80b5-134">Choose the ![Lightbulb that opens the Tell Me feature](../../media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Customer Bank Account Card**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="e80b5-135">En la ficha desplegable **Transferencia**, escriba la información en los campos CCC relevantes.</span><span class="sxs-lookup"><span data-stu-id="e80b5-135">On the **Transfer** FastTab, enter information into the relevant CCC fields.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="e80b5-136">Debe configurar información de la empresa en la ficha desplegable **Pagos**.</span><span class="sxs-lookup"><span data-stu-id="e80b5-136">You must set up the company information on the **Payments** FastTab.</span></span>  

3.  <span data-ttu-id="e80b5-137">Elija el botón **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="e80b5-137">Choose the **OK** button.</span></span>  

## <a name="see-also"></a><span data-ttu-id="e80b5-138">Consulte también</span><span class="sxs-lookup"><span data-stu-id="e80b5-138">See Also</span></span>  
[<span data-ttu-id="e80b5-139">Configurar bancos</span><span class="sxs-lookup"><span data-stu-id="e80b5-139">Set Up Bank Accounts</span></span>](../../bank-how-setup-bank-accounts.md) 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]