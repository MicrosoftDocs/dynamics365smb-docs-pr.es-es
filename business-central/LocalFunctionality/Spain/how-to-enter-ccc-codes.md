---
title: Introducción de códigos CCC
description: El Código Cuenta Cliente (CCC) es un código de identificación de cuentas bancarias único. Los siguientes campos de componentes componen la estructura de código CCC de 20 dígitos (España) o 21 dígitos (Portugal).
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
ms.openlocfilehash: 784469a998c87cbc59090c56c56e9727e9e961cd
ms.sourcegitcommit: 007b331b6974983ee614db0406f00777da359ecb
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 08/10/2020
ms.locfileid: "3676660"
---
# <a name="enter-ccc-codes"></a><span data-ttu-id="b9b63-104">Introducir códigos CCC</span><span class="sxs-lookup"><span data-stu-id="b9b63-104">Enter CCC Codes</span></span>
<span data-ttu-id="b9b63-105">El Código Cuenta Cliente (CCC) es un código de identificación de cuentas bancarias único.</span><span class="sxs-lookup"><span data-stu-id="b9b63-105">Código Cuenta Cliente (CCC) is a unique bank account identification code.</span></span> <span data-ttu-id="b9b63-106">Los siguientes campos de componentes componen la estructura de código CCC de 20 dígitos (España) o 21 dígitos (Portugal).</span><span class="sxs-lookup"><span data-stu-id="b9b63-106">The following component fields make up the 20-digit (Spain) or 21-digit (Portugal) bank CCC code structure.</span></span>  

<span data-ttu-id="b9b63-107">Si modifica la estructura del código CCC, el campo **Nº CCC**</span><span class="sxs-lookup"><span data-stu-id="b9b63-107">If you change the CCC code structure, the **CCC No.**</span></span> <span data-ttu-id="b9b63-108">se actualiza automáticamente.</span><span class="sxs-lookup"><span data-stu-id="b9b63-108">field updates automatically.</span></span> <span data-ttu-id="b9b63-109">De igual forma, si modifica el campo **Nº CCC**</span><span class="sxs-lookup"><span data-stu-id="b9b63-109">Similarly, if you change the **CCC No.**</span></span> <span data-ttu-id="b9b63-110">la estructura del código CCC se actualiza automáticamente.</span><span class="sxs-lookup"><span data-stu-id="b9b63-110">field, the CCC code structure updates automatically.</span></span>  

## <a name="to-enter-ccc-codes"></a><span data-ttu-id="b9b63-111">Para introducir códigos CCC</span><span class="sxs-lookup"><span data-stu-id="b9b63-111">To enter CCC codes</span></span>  

1.  <span data-ttu-id="b9b63-112">Elija el icono ![Bombilla que abre la función Dígame](../../media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Información de empresa** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="b9b63-112">Choose the ![Lightbulb that opens the Tell Me feature](../../media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Company Information**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="b9b63-113">Rellene los campos de la ficha desplegable **Pagos**, tal como se describe en la tabla siguiente</span><span class="sxs-lookup"><span data-stu-id="b9b63-113">On the **Payments** FastTab, fill in the fields as described in the following table</span></span>  

    |<span data-ttu-id="b9b63-114">Campo</span><span class="sxs-lookup"><span data-stu-id="b9b63-114">Field</span></span>|<span data-ttu-id="b9b63-115">Description</span><span class="sxs-lookup"><span data-stu-id="b9b63-115">Description</span></span>|  
    |---------------------------------|--------------|---------------------------------------|  
    |<span data-ttu-id="b9b63-116">**CCC Cód. banco**</span><span class="sxs-lookup"><span data-stu-id="b9b63-116">**CCC Bank No.**</span></span>|<span data-ttu-id="b9b63-117">1-4</span><span class="sxs-lookup"><span data-stu-id="b9b63-117">1-4</span></span>|<span data-ttu-id="b9b63-118">Identifica el banco en el que se ha abierto la cuenta.</span><span class="sxs-lookup"><span data-stu-id="b9b63-118">Identifies the bank where the account has been opened.</span></span>|  
    |<span data-ttu-id="b9b63-119">**CCC Cód. oficina**</span><span class="sxs-lookup"><span data-stu-id="b9b63-119">**CCC Bank Branch No.**</span></span>|<span data-ttu-id="b9b63-120">5-8</span><span class="sxs-lookup"><span data-stu-id="b9b63-120">5-8</span></span>|<span data-ttu-id="b9b63-121">Identifica el código de la oficina.</span><span class="sxs-lookup"><span data-stu-id="b9b63-121">Identifies the branch code.</span></span> <span data-ttu-id="b9b63-122">Si el banco no utiliza esta referencia, pueden ser ceros.</span><span class="sxs-lookup"><span data-stu-id="b9b63-122">If the bank does not use this reference, these can be zeros.</span></span>|  
    |<span data-ttu-id="b9b63-123">**CCC Dígito control**</span><span class="sxs-lookup"><span data-stu-id="b9b63-123">**CCC Control Digits**</span></span>|<span data-ttu-id="b9b63-124">9-10</span><span class="sxs-lookup"><span data-stu-id="b9b63-124">9-10</span></span>|<span data-ttu-id="b9b63-125">Identifica los dígitos de control.</span><span class="sxs-lookup"><span data-stu-id="b9b63-125">Identifies the control digits.</span></span>|  
    |<span data-ttu-id="b9b63-126">**CCC Nº cuenta**</span><span class="sxs-lookup"><span data-stu-id="b9b63-126">**CCC Bank Account No.**</span></span>|<span data-ttu-id="b9b63-127">11-20 (España)</span><span class="sxs-lookup"><span data-stu-id="b9b63-127">11-20 (Spain)</span></span><br /><br /> <span data-ttu-id="b9b63-128">11-21 (Portugal)</span><span class="sxs-lookup"><span data-stu-id="b9b63-128">11-21 (Portugal)</span></span>|<span data-ttu-id="b9b63-129">Identifica el número de cuenta, que se puede ajustar con ceros a la izquierda.</span><span class="sxs-lookup"><span data-stu-id="b9b63-129">Identifies the account number, which may be adjusted with preceding zeros.</span></span>|  

## <a name="see-also"></a><span data-ttu-id="b9b63-130">Consulte también</span><span class="sxs-lookup"><span data-stu-id="b9b63-130">See Also</span></span>  
[<span data-ttu-id="b9b63-131">Funcionalidad local para España</span><span class="sxs-lookup"><span data-stu-id="b9b63-131">Spain Local Functionality</span></span>](spain-local-functionality.md)
