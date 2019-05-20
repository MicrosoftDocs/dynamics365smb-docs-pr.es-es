---
title: Especificar el diseño de un cheque | Documentos de Microsoft
description: Puede diseñar e imprimir los cheques en diferentes formatos para cumplir los estándares.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: print check, customize
ms.date: 04/24/2019
ms.author: edupont
ms.openlocfilehash: f2b7fa01cff36e3aab335f7d5921954343c69b74
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/29/2019
ms.locfileid: "1243600"
---
# <a name="define-check-layouts"></a><span data-ttu-id="46d5a-103">Definir diseños de cheque</span><span class="sxs-lookup"><span data-stu-id="46d5a-103">Define Check Layouts</span></span>
<span data-ttu-id="46d5a-104">Puede diseñar los cheques conforme a los estándares definidos por las autoridades locales.</span><span class="sxs-lookup"><span data-stu-id="46d5a-104">You can design your checks to conform with the standards set by the local authorities.</span></span> <span data-ttu-id="46d5a-105">Las imágenes de los cheques se pueden imprimir en inglés, francés o español.</span><span class="sxs-lookup"><span data-stu-id="46d5a-105">Check images can be printed in English, French, or Spanish.</span></span>

<span data-ttu-id="46d5a-106">Los cheques se han diseñado para imprimir formatos de imágenes de cheque de Estados Unidos y Canadá en un formato cheque-matriz-cheque o en un formato matriz-matriz-cheque.</span><span class="sxs-lookup"><span data-stu-id="46d5a-106">Checks are designed to print in both the United States and Canadian check image formats in either a check-stub-check format or a stub-stub-check format.</span></span>

## <a name="to-define-check-layouts"></a><span data-ttu-id="46d5a-107">Para definir diseños de cheque</span><span class="sxs-lookup"><span data-stu-id="46d5a-107">To define check layouts</span></span>
1. <span data-ttu-id="46d5a-108">Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Selección informes banco** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="46d5a-108">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Report Selections Bank Account**, and then choose the related link.</span></span>
2. <span data-ttu-id="46d5a-109">En la página **Informe selección - Bancos**, en el campo **Uso**, seleccione **Cheque**.</span><span class="sxs-lookup"><span data-stu-id="46d5a-109">On the **Report Selection - Bank Acc.** page, in the **Usage** field, select **Check**.</span></span>
3. <span data-ttu-id="46d5a-110">Seleccione uno de los identificadores de informes siguientes:</span><span class="sxs-lookup"><span data-stu-id="46d5a-110">Select one of the following report IDs.</span></span>

  | <span data-ttu-id="46d5a-111">Id. informe</span><span class="sxs-lookup"><span data-stu-id="46d5a-111">Report ID</span></span> | <span data-ttu-id="46d5a-112">Nombre informe</span><span class="sxs-lookup"><span data-stu-id="46d5a-112">Report Name</span></span> | <span data-ttu-id="46d5a-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="46d5a-113">Description</span></span> |
  | --- | --- | --- |
  | <span data-ttu-id="46d5a-114">1401</span><span class="sxs-lookup"><span data-stu-id="46d5a-114">1401</span></span> |<span data-ttu-id="46d5a-115">Activar</span><span class="sxs-lookup"><span data-stu-id="46d5a-115">Check</span></span> |<span data-ttu-id="46d5a-116">Es el informe predeterminado.</span><span class="sxs-lookup"><span data-stu-id="46d5a-116">This is the default report.</span></span> |
  | <span data-ttu-id="46d5a-117">10411</span><span class="sxs-lookup"><span data-stu-id="46d5a-117">10411</span></span> |<span data-ttu-id="46d5a-118">Cheque (Matriz/Matriz/Cheque)</span><span class="sxs-lookup"><span data-stu-id="46d5a-118">Check (Stub/Stub/Check)</span></span> |<span data-ttu-id="46d5a-119">Este informe está diseñado para imprimir cheques en un formato matriz/matriz/cheque.</span><span class="sxs-lookup"><span data-stu-id="46d5a-119">This report is designed to print checks in a stub/stub/check format.</span></span> |
  | <span data-ttu-id="46d5a-120">10412</span><span class="sxs-lookup"><span data-stu-id="46d5a-120">10412</span></span> |<span data-ttu-id="46d5a-121">Cheque (Matriz/Cheque/Matriz)</span><span class="sxs-lookup"><span data-stu-id="46d5a-121">Check (Stub/Check/Stub)</span></span> |<span data-ttu-id="46d5a-122">Este informe está diseñado para imprimir cheques en un formato matriz/cheque/matriz.</span><span class="sxs-lookup"><span data-stu-id="46d5a-122">This report is designed to print checks in a stub/check/stub format.</span></span> |
  | <span data-ttu-id="46d5a-123">10413</span><span class="sxs-lookup"><span data-stu-id="46d5a-123">10413</span></span> |<span data-ttu-id="46d5a-124">Tres cheques por página</span><span class="sxs-lookup"><span data-stu-id="46d5a-124">Three Checks per Page</span></span> |<span data-ttu-id="46d5a-125">Este informe está diseñado para imprimir tres cheques por página.</span><span class="sxs-lookup"><span data-stu-id="46d5a-125">This report is designed to print three checks on each page.</span></span> |

<span data-ttu-id="46d5a-126">Cuando haya configurado los diseños de cheques, puede imprimir cheques desde la página **Diario de pagos**.</span><span class="sxs-lookup"><span data-stu-id="46d5a-126">When you have set up check layouts, you can print checks from the **Payment Journal** page.</span></span> <span data-ttu-id="46d5a-127">Para obtener más información, consulte [Trabajar con cheques](payables-how-work-checks.md).</span><span class="sxs-lookup"><span data-stu-id="46d5a-127">For more information, see [Work with Checks](payables-how-work-checks.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="46d5a-128">Consulte también</span><span class="sxs-lookup"><span data-stu-id="46d5a-128">See Also</span></span>
[<span data-ttu-id="46d5a-129">Administrar pagos</span><span class="sxs-lookup"><span data-stu-id="46d5a-129">Managing Payables</span></span>](payables-manage-payables.md)  
<span data-ttu-id="46d5a-130">[Administrar cuentas bancarias](bank-manage-bank-accounts.md) </span><span class="sxs-lookup"><span data-stu-id="46d5a-130">[Managing Bank Accounts](bank-manage-bank-accounts.md) </span></span>  
[<span data-ttu-id="46d5a-131">Completar procesos de fin de periodo</span><span class="sxs-lookup"><span data-stu-id="46d5a-131">Completing Period-End Processes</span></span>](year-how-complete-period-end-processes.md)  
<span data-ttu-id="46d5a-132">[Trabajar con [!INCLUDE[prodshort](includes/prodshort.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="46d5a-132">[Working with [!INCLUDE[prodshort](includes/prodshort.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="46d5a-133">Funciones empresariales generales</span><span class="sxs-lookup"><span data-stu-id="46d5a-133">General Business Functionality</span></span>](ui-across-business-areas.md)
