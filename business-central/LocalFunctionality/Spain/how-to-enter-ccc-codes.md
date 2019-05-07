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
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: 43bb2b95d26112acdcdd543cfc05987605b4c35c
ms.sourcegitcommit: addfb47612cc2e4e98dfd7e338b6f41cde405d5c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/16/2019
ms.locfileid: "939053"
---
# <a name="enter-ccc-codes"></a><span data-ttu-id="24356-104">Introducir códigos CCC</span><span class="sxs-lookup"><span data-stu-id="24356-104">Enter CCC Codes</span></span>
<span data-ttu-id="24356-105">El Código Cuenta Cliente (CCC) es un código de identificación de cuentas bancarias único.</span><span class="sxs-lookup"><span data-stu-id="24356-105">Código Cuenta Cliente (CCC) is a unique bank account identification code.</span></span> <span data-ttu-id="24356-106">Los siguientes campos de componentes componen la estructura de código CCC de 20 dígitos (España) o 21 dígitos (Portugal).</span><span class="sxs-lookup"><span data-stu-id="24356-106">The following component fields make up the 20-digit (Spain) or 21-digit (Portugal) bank CCC code structure.</span></span>  

<span data-ttu-id="24356-107">Si modifica la estructura del código CCC, el campo **Nº CCC**</span><span class="sxs-lookup"><span data-stu-id="24356-107">If you change the CCC code structure, the **CCC No.**</span></span> <span data-ttu-id="24356-108">se actualiza automáticamente.</span><span class="sxs-lookup"><span data-stu-id="24356-108">field updates automatically.</span></span> <span data-ttu-id="24356-109">De igual forma, si modifica el campo **Nº CCC**</span><span class="sxs-lookup"><span data-stu-id="24356-109">Similarly, if you change the **CCC No.**</span></span> <span data-ttu-id="24356-110">la estructura del código CCC se actualiza automáticamente.</span><span class="sxs-lookup"><span data-stu-id="24356-110">field, the CCC code structure updates automatically.</span></span>  

## <a name="to-enter-ccc-codes"></a><span data-ttu-id="24356-111">Para introducir códigos CCC</span><span class="sxs-lookup"><span data-stu-id="24356-111">To enter CCC codes</span></span>  

1.  <span data-ttu-id="24356-112">Seleccione el icono ![Buscar página o informe](../../media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Información de la empresa** y, a continuación, seleccione el vínculo relacionado.</span><span class="sxs-lookup"><span data-stu-id="24356-112">Choose the ![Search for Page or Report](../../media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Company Information**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="24356-113">Rellene los campos de la ficha desplegable **Pagos**, tal como se describe en la tabla siguiente</span><span class="sxs-lookup"><span data-stu-id="24356-113">On the **Payments** FastTab, fill in the fields as described in the following table</span></span>  

    |<span data-ttu-id="24356-114">Campo</span><span class="sxs-lookup"><span data-stu-id="24356-114">Field</span></span>|<span data-ttu-id="24356-115">Description</span><span class="sxs-lookup"><span data-stu-id="24356-115">Description</span></span>|  
    |---------------------------------|--------------|---------------------------------------|  
    |<span data-ttu-id="24356-116">**CCC Cód. banco**</span><span class="sxs-lookup"><span data-stu-id="24356-116">**CCC Bank No.**</span></span>|<span data-ttu-id="24356-117">1-4</span><span class="sxs-lookup"><span data-stu-id="24356-117">1-4</span></span>|<span data-ttu-id="24356-118">Identifica el banco en el que se ha abierto la cuenta.</span><span class="sxs-lookup"><span data-stu-id="24356-118">Identifies the bank where the account has been opened.</span></span>|  
    |<span data-ttu-id="24356-119">**CCC Cód. oficina**</span><span class="sxs-lookup"><span data-stu-id="24356-119">**CCC Bank Branch No.**</span></span>|<span data-ttu-id="24356-120">5-8</span><span class="sxs-lookup"><span data-stu-id="24356-120">5-8</span></span>|<span data-ttu-id="24356-121">Identifica el código de la oficina.</span><span class="sxs-lookup"><span data-stu-id="24356-121">Identifies the branch code.</span></span> <span data-ttu-id="24356-122">Si el banco no utiliza esta referencia, pueden ser ceros.</span><span class="sxs-lookup"><span data-stu-id="24356-122">If the bank does not use this reference, these can be zeros.</span></span>|  
    |<span data-ttu-id="24356-123">**CCC Dígito control**</span><span class="sxs-lookup"><span data-stu-id="24356-123">**CCC Control Digits**</span></span>|<span data-ttu-id="24356-124">9-10</span><span class="sxs-lookup"><span data-stu-id="24356-124">9-10</span></span>|<span data-ttu-id="24356-125">Identifica los dígitos de control.</span><span class="sxs-lookup"><span data-stu-id="24356-125">Identifies the control digits.</span></span>|  
    |<span data-ttu-id="24356-126">**CCC Nº cuenta**</span><span class="sxs-lookup"><span data-stu-id="24356-126">**CCC Bank Account No.**</span></span>|<span data-ttu-id="24356-127">11-20 (España)</span><span class="sxs-lookup"><span data-stu-id="24356-127">11-20 (Spain)</span></span><br /><br /> <span data-ttu-id="24356-128">11-21 (Portugal)</span><span class="sxs-lookup"><span data-stu-id="24356-128">11-21 (Portugal)</span></span>|<span data-ttu-id="24356-129">Identifica el número de cuenta, que se puede ajustar con ceros a la izquierda.</span><span class="sxs-lookup"><span data-stu-id="24356-129">Identifies the account number, which may be adjusted with preceding zeros.</span></span>|  

## <a name="see-also"></a><span data-ttu-id="24356-130">Consulte también</span><span class="sxs-lookup"><span data-stu-id="24356-130">See Also</span></span>  
[<span data-ttu-id="24356-131">Funcionalidad local para España</span><span class="sxs-lookup"><span data-stu-id="24356-131">Spain Local Functionality</span></span>](spain-local-functionality.md)
