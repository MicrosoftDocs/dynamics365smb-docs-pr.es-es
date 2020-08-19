---
title: Configuración de códigos CCC de bancos
description: El Código Cuenta Cliente (CCC) es un código de cuenta único usado por los bancos para identificar a sus clientes. El código CCC se imprime en los documentos bancarios, como cheques y extractos.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: 796f0862a63b2f2f24bc0b86d445fa9c7a5d1bb1
ms.sourcegitcommit: 007b331b6974983ee614db0406f00777da359ecb
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 08/10/2020
ms.locfileid: "3676548"
---
# <a name="set-up-bank-ccc-codes"></a><span data-ttu-id="93b30-104">Configurar códigos CCC de bancos</span><span class="sxs-lookup"><span data-stu-id="93b30-104">Set Up Bank CCC Codes</span></span>
<span data-ttu-id="93b30-105">El Código Cuenta Cliente (CCC) es un código de cuenta único usado por los bancos para identificar a sus clientes.</span><span class="sxs-lookup"><span data-stu-id="93b30-105">Código Cuenta Cliente (CCC) is a unique account code used by banks to identify their customers.</span></span> <span data-ttu-id="93b30-106">El código CCC se imprime en los documentos bancarios, como cheques y extractos.</span><span class="sxs-lookup"><span data-stu-id="93b30-106">The CCC code is printed on bank documents such as checks and statements.</span></span>  

<span data-ttu-id="93b30-107">Se pueden configurar códigos CCC en las siguientes ubicaciones:</span><span class="sxs-lookup"><span data-stu-id="93b30-107">You can set up CCC codes in the following locations:</span></span>  

- <span data-ttu-id="93b30-108">Página **Ficha banco**</span><span class="sxs-lookup"><span data-stu-id="93b30-108">**Bank Account Card** page</span></span>  
- <span data-ttu-id="93b30-109">Página **Información de empresa**</span><span class="sxs-lookup"><span data-stu-id="93b30-109">**Company Information** page</span></span>  
- <span data-ttu-id="93b30-110">Página **Ficha banco cliente**</span><span class="sxs-lookup"><span data-stu-id="93b30-110">**Customer Bank Account Card** page</span></span>  
- <span data-ttu-id="93b30-111">Página **Ficha banco proveedor**</span><span class="sxs-lookup"><span data-stu-id="93b30-111">**Vendor Bank Account Card** page</span></span>  

<span data-ttu-id="93b30-112">El procedimiento siguiente describe cómo configurar códigos CCC de banco para su empresa.</span><span class="sxs-lookup"><span data-stu-id="93b30-112">The following procedure describes how to set up bank CCC codes for your company.</span></span>  

## <a name="to-enter-ccc-codes"></a><span data-ttu-id="93b30-113">Para introducir códigos CCC</span><span class="sxs-lookup"><span data-stu-id="93b30-113">To enter CCC codes</span></span>  

1.  <span data-ttu-id="93b30-114">Elija el icono ![Bombilla que abre la función Dígame](../../media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Información de empresa** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="93b30-114">Choose the ![Lightbulb that opens the Tell Me feature](../../media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Company Information**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="93b30-115">Rellene los campos de la ficha desplegable **Pagos**, tal como se describe en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="93b30-115">On the **Payments** FastTab, fill in the fields as described in the following table.</span></span>  

    |<span data-ttu-id="93b30-116">Campo</span><span class="sxs-lookup"><span data-stu-id="93b30-116">Field</span></span>|<span data-ttu-id="93b30-117">Description</span><span class="sxs-lookup"><span data-stu-id="93b30-117">Description</span></span>|  
    |---------------------------------|--------------|---------------------------------------|  
    |<span data-ttu-id="93b30-118">**CCC Cód. banco**</span><span class="sxs-lookup"><span data-stu-id="93b30-118">**CCC Bank No.**</span></span>|<span data-ttu-id="93b30-119">1-4</span><span class="sxs-lookup"><span data-stu-id="93b30-119">1-4</span></span>|<span data-ttu-id="93b30-120">Identifica el banco en el que se ha abierto la cuenta.</span><span class="sxs-lookup"><span data-stu-id="93b30-120">Identifies the bank where the account has been opened.</span></span>|  
    |<span data-ttu-id="93b30-121">**CCC Cód. oficina**</span><span class="sxs-lookup"><span data-stu-id="93b30-121">**CCC Bank Branch No.**</span></span>|<span data-ttu-id="93b30-122">5-8</span><span class="sxs-lookup"><span data-stu-id="93b30-122">5-8</span></span>|<span data-ttu-id="93b30-123">Identifica el código de la oficina.</span><span class="sxs-lookup"><span data-stu-id="93b30-123">Identifies the branch code.</span></span> <span data-ttu-id="93b30-124">Si el banco no utiliza esta referencia, el código de la oficina pueden ser ceros.</span><span class="sxs-lookup"><span data-stu-id="93b30-124">If the bank does not use this reference, the branch code can be zeros.</span></span>|  
    |<span data-ttu-id="93b30-125">**CCC Dígito control**</span><span class="sxs-lookup"><span data-stu-id="93b30-125">**CCC Control Digits**</span></span>|<span data-ttu-id="93b30-126">9-10</span><span class="sxs-lookup"><span data-stu-id="93b30-126">9-10</span></span>|<span data-ttu-id="93b30-127">Identifica los dígitos de control.</span><span class="sxs-lookup"><span data-stu-id="93b30-127">Identifies the control digits.</span></span>|  
    |<span data-ttu-id="93b30-128">**CCC Nº cuenta**</span><span class="sxs-lookup"><span data-stu-id="93b30-128">**CCC Bank Account No.**</span></span>|<span data-ttu-id="93b30-129">11-20 (España)</span><span class="sxs-lookup"><span data-stu-id="93b30-129">11-20 (Spain)</span></span><br /><br /> <span data-ttu-id="93b30-130">11-21 (Portugal)</span><span class="sxs-lookup"><span data-stu-id="93b30-130">11-21 (Portugal)</span></span>|<span data-ttu-id="93b30-131">Identifica el número de cuenta, que se puede ajustar con ceros a la izquierda.</span><span class="sxs-lookup"><span data-stu-id="93b30-131">Identifies the account number, which may be adjusted with preceding zeros.</span></span>|  

<span data-ttu-id="93b30-132">El siguiente procedimiento describe cómo configurar códigos bancarios CCC para cuentas bancarias de clientes existentes, pero los mismos pasos se aplican a proveedores, cuentas bancarias e información de la compañía.</span><span class="sxs-lookup"><span data-stu-id="93b30-132">The following procedure describes how to set up bank CCC codes for existing customer bank accounts, but the same steps apply to vendors, bank accounts, and company information.</span></span>  

## <a name="to-set-up-bank-ccc-codes-for-a-customer-bank-account"></a><span data-ttu-id="93b30-133">Para configurar códigos CCC de banco de un banco cliente</span><span class="sxs-lookup"><span data-stu-id="93b30-133">To set up bank CCC codes for a customer bank account</span></span>  

1.  <span data-ttu-id="93b30-134">Elija el icono ![Bombilla que abre la función Dígame](../../media/ui-search/search_small.png "Dígame qué desea hacer"), introduzca **Ficha banco cliente** y luego elija el vínculo relacionado.</span><span class="sxs-lookup"><span data-stu-id="93b30-134">Choose the ![Lightbulb that opens the Tell Me feature](../../media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Customer Bank Account Card**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="93b30-135">En la ficha desplegable **Transferencia**, escriba la información en los campos CCC relevantes.</span><span class="sxs-lookup"><span data-stu-id="93b30-135">On the **Transfer** FastTab, enter information into the relevant CCC fields.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="93b30-136">Debe configurar información de la empresa en la ficha desplegable **Pagos**.</span><span class="sxs-lookup"><span data-stu-id="93b30-136">You must set up the company information on the **Payments** FastTab.</span></span>  

3.  <span data-ttu-id="93b30-137">Elija el botón **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="93b30-137">Choose the **OK** button.</span></span>  

## <a name="see-also"></a><span data-ttu-id="93b30-138">Consulte también</span><span class="sxs-lookup"><span data-stu-id="93b30-138">See Also</span></span>  
[<span data-ttu-id="93b30-139">Configurar bancos</span><span class="sxs-lookup"><span data-stu-id="93b30-139">Set Up Bank Accounts</span></span>](../../bank-how-setup-bank-accounts.md) 
