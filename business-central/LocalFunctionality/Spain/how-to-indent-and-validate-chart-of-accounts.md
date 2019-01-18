---
title: "Test y validación del plan de cuentas"
description: "En la página **Ficha cuenta**, se puede efectuar el test y la validación del plan de cuentas. Puede escribir 20 números como máximo. Las cuentas se ordenan según la cadena, como se muestran en el siguiente ejemplo."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 33b900f1ac9e295921e7f3d6ea72cc93939d8a1b
ms.openlocfilehash: ff557e9c4bee0c6887e7607ff206f1dfa0af3a39
ms.contentlocale: es-es
ms.lasthandoff: 11/26/2018

---
# <a name="indent-and-validate-chart-of-accounts"></a><span data-ttu-id="fb28f-105">Efectuar el test y la validación del plan de cuentas</span><span class="sxs-lookup"><span data-stu-id="fb28f-105">Indent and Validate Chart of Accounts</span></span>
<span data-ttu-id="fb28f-106">En la página **Ficha cuenta**, se puede efectuar el test y la validación del plan de cuentas.</span><span class="sxs-lookup"><span data-stu-id="fb28f-106">You can indent and validate the chart of accounts on the **G/L Account Card** page.</span></span> <span data-ttu-id="fb28f-107">Puede escribir 20 números como máximo.</span><span class="sxs-lookup"><span data-stu-id="fb28f-107">You can enter a maximum of 20 numbers.</span></span> <span data-ttu-id="fb28f-108">Las cuentas se ordenan según la cadena, como se muestran en el siguiente ejemplo.</span><span class="sxs-lookup"><span data-stu-id="fb28f-108">Accounts are sorted in string order, as shown in the following example.</span></span>  

<span data-ttu-id="fb28f-109">1</span><span class="sxs-lookup"><span data-stu-id="fb28f-109">1</span></span>  
<span data-ttu-id="fb28f-110">10</span><span class="sxs-lookup"><span data-stu-id="fb28f-110">10</span></span>  
<span data-ttu-id="fb28f-111">101</span><span class="sxs-lookup"><span data-stu-id="fb28f-111">101</span></span>  
<span data-ttu-id="fb28f-112">2</span><span class="sxs-lookup"><span data-stu-id="fb28f-112">2</span></span>  
<span data-ttu-id="fb28f-113">20</span><span class="sxs-lookup"><span data-stu-id="fb28f-113">20</span></span>  
<span data-ttu-id="fb28f-114">2100001</span><span class="sxs-lookup"><span data-stu-id="fb28f-114">2100001</span></span>  
<span data-ttu-id="fb28f-115">3</span><span class="sxs-lookup"><span data-stu-id="fb28f-115">3</span></span>  
<span data-ttu-id="fb28f-116">31</span><span class="sxs-lookup"><span data-stu-id="fb28f-116">31</span></span>  

## <a name="to-indent-and-validate-the-chart-of-accounts"></a><span data-ttu-id="fb28f-117">Para efectuar el test y la validación del plan de cuentas</span><span class="sxs-lookup"><span data-stu-id="fb28f-117">To indent and validate the chart of accounts</span></span>  

1.  <span data-ttu-id="fb28f-118">Seleccione el icono ![Buscar página o informe](../../media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Plan de cuentas** y, a continuación, seleccione el vínculo relacionado.</span><span class="sxs-lookup"><span data-stu-id="fb28f-118">Choose the ![Search for Page or Report](../../media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Chart of Accounts**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="fb28f-119">Seleccione la acción **Nuevo**.</span><span class="sxs-lookup"><span data-stu-id="fb28f-119">Choose the **New** action.</span></span>  
3.  <span data-ttu-id="fb28f-120">En la ficha desplegable **General**, en el campo **Nº**</span><span class="sxs-lookup"><span data-stu-id="fb28f-120">On the **General** FastTab, in the **No.**</span></span> <span data-ttu-id="fb28f-121">escriba el número de la cuenta de contabilidad que está configurando.</span><span class="sxs-lookup"><span data-stu-id="fb28f-121">field, enter the number of the general ledger account that you are setting up.</span></span>  
4.  <span data-ttu-id="fb28f-122">En el campo **Tipo mov.**, seleccione **Registro** o **Mayor**.</span><span class="sxs-lookup"><span data-stu-id="fb28f-122">In the **Account type** field, select **Posting** or **Heading**.</span></span> <span data-ttu-id="fb28f-123">**Registro** implica que se pueden registrar movimientos en la cuenta.</span><span class="sxs-lookup"><span data-stu-id="fb28f-123">**Posting** implies that entries can be posted to the account.</span></span> <span data-ttu-id="fb28f-124">**Mayor** implica que no se pueden registrar movimientos en la cuenta.</span><span class="sxs-lookup"><span data-stu-id="fb28f-124">**Heading** implies that entries cannot be posted to the account.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="fb28f-125">Para Portugal, seleccione **Registro** o **Total** en el campo **Tipo mov**.</span><span class="sxs-lookup"><span data-stu-id="fb28f-125">For Portugal, select **Posting** or **Total** in the **Account type** field.</span></span>  

5.  <span data-ttu-id="fb28f-126">En el campo **Cta. regularización**, seleccione la cuenta a la que se enviarán los cambios después de la corrección.</span><span class="sxs-lookup"><span data-stu-id="fb28f-126">In the **Income Stmt. Bal. Acc.** field, select the account to which the changes will be sent after correction.</span></span>  
6.  <span data-ttu-id="fb28f-127">Escriba información en el resto de campos relevantes.</span><span class="sxs-lookup"><span data-stu-id="fb28f-127">Enter information into the other relevant fields.</span></span>  
7.  <span data-ttu-id="fb28f-128">Elija el botón **Aceptar** para cerrar la página **Ficha cuenta**.</span><span class="sxs-lookup"><span data-stu-id="fb28f-128">Choose the **OK** button to close the **G/L Account Card** page.</span></span>  
8.  <span data-ttu-id="fb28f-129">En la página **Plan de cuentas**, seleccione una cuenta y, a continuación, elija **Test plan de cuentas**.</span><span class="sxs-lookup"><span data-stu-id="fb28f-129">On the **Chart of Accounts** page, select an account, and then choose **Indent Chart of Accounts**.</span></span>  
9. <span data-ttu-id="fb28f-130">Para validar el plan de cuentas, elija el botón **Sí** en el cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="fb28f-130">To validate the chart of accounts, choose the **Yes** button in the dialog box.</span></span> <span data-ttu-id="fb28f-131">Una vez validado, se le notificará si el plan de cuentas es correcto.</span><span class="sxs-lookup"><span data-stu-id="fb28f-131">After validation, you will be notified whether the chart of accounts is correct.</span></span>  
10. <span data-ttu-id="fb28f-132">Elija el botón **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="fb28f-132">Choose the **OK** button.</span></span>  

## <a name="to-validate-the-chart-of-accounts-in-portugal"></a><span data-ttu-id="fb28f-133">Para efectuar la validación del plan de cuentas en Portugal</span><span class="sxs-lookup"><span data-stu-id="fb28f-133">To validate the chart of accounts in Portugal</span></span>  

1.  <span data-ttu-id="fb28f-134">En la página **Plan de cuentas**, seleccione la acción **Comprobar Plan de cuentas**.</span><span class="sxs-lookup"><span data-stu-id="fb28f-134">On the **Chart of Accounts** page, choose the **Check Chart of Accounts** action.</span></span>  
2.  <span data-ttu-id="fb28f-135">Elija el botón **Sí**.</span><span class="sxs-lookup"><span data-stu-id="fb28f-135">Choose the **Yes** button.</span></span>  

## <a name="see-also"></a><span data-ttu-id="fb28f-136">Consulte también</span><span class="sxs-lookup"><span data-stu-id="fb28f-136">See Also</span></span>  
[<span data-ttu-id="fb28f-137">Funcionalidad local para España</span><span class="sxs-lookup"><span data-stu-id="fb28f-137">Spain Local Functionality</span></span>](spain-local-functionality.md)

