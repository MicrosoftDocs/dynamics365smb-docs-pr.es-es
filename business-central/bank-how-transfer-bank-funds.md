---
title: Transferir fondos bancarios
description: Puede transferir importes de una cuenta bancaria a otra, con divisas distintas, registrando la transacción en el diario general.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: bank account transfer, multiple currencies
ms.date: 04/29/2021
ms.author: edupont
ms.openlocfilehash: da9c8711751040cecb267a3b2209bad2534b618b
ms.sourcegitcommit: 08ca5798cf3f04fc3ea38fff40c1860196a70adf
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 05/06/2021
ms.locfileid: "5985392"
---
# <a name="transfer-bank-funds"></a><span data-ttu-id="e7dda-103">Transferir fondos bancarios</span><span class="sxs-lookup"><span data-stu-id="e7dda-103">Transfer Bank Funds</span></span>

<span data-ttu-id="e7dda-104">En ocasiones es necesario transferir un importe desde un banco en [!INCLUDE[prod_short](includes/prod_short.md)] a otro.</span><span class="sxs-lookup"><span data-stu-id="e7dda-104">You may sometimes need to transfer an amount from one bank account in [!INCLUDE[prod_short](includes/prod_short.md)] to another.</span></span> <span data-ttu-id="e7dda-105">Para hacerlo, debe registrar la transacción en la página **Diario general**.</span><span class="sxs-lookup"><span data-stu-id="e7dda-105">To do this, you must post the transaction on the **General Journal** page.</span></span> <span data-ttu-id="e7dda-106">La tarea varía en función de si los bancos usan la misma divisa o distintas divisas.</span><span class="sxs-lookup"><span data-stu-id="e7dda-106">The task varies depending on whether the bank accounts use the same currency or different currencies.</span></span>

## <a name="to-post-a-transfer-between-bank-accounts-with-the-same-currency-code"></a><span data-ttu-id="e7dda-107">Para registrar transferencias entre bancos con el mismo código de divisa</span><span class="sxs-lookup"><span data-stu-id="e7dda-107">To post a transfer between bank accounts with the same currency code</span></span>

1. <span data-ttu-id="e7dda-108">Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), introduzca **Diario general** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="e7dda-108">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **General Journal**, and then choose the related link.</span></span>
2. <span data-ttu-id="e7dda-109">En una línea de diario, rellene los campos **Fecha registro** y **Nº documento**.</span><span class="sxs-lookup"><span data-stu-id="e7dda-109">On a journal line, fill in the **Posting Date** and **Document No.** fields.</span></span>
3. <span data-ttu-id="e7dda-110">En el campo **Tipo mov**, seleccione **Banco**.</span><span class="sxs-lookup"><span data-stu-id="e7dda-110">In the **Account Type** field, select **Bank Account**.</span></span>
4. <span data-ttu-id="e7dda-111">En el campo **N.º de cuenta**, seleccione la cuenta desde la que quiere transferir los fondos.</span><span class="sxs-lookup"><span data-stu-id="e7dda-111">In the **Account No.** field, select the bank from which you want to transfer the funds.</span></span>
5. <span data-ttu-id="e7dda-112">En el campo **Importe**, introduzca el importe que quiere transferir.</span><span class="sxs-lookup"><span data-stu-id="e7dda-112">In the **Amount** field, enter the amount to be transferred.</span></span>

    <span data-ttu-id="e7dda-113">A continuación, debe especificar la cuenta de contrapartida.</span><span class="sxs-lookup"><span data-stu-id="e7dda-113">Next, you must specify the balancing account.</span></span> <span data-ttu-id="e7dda-114">Si no puede ver los campos relevantes, elija la acción **Mostrar más columnas** para ver todos los campos disponibles.</span><span class="sxs-lookup"><span data-stu-id="e7dda-114">If you can't see the relevant fields, then choose the **Show More Columns** action to view all available fields.</span></span>
6. <span data-ttu-id="e7dda-115">En el campo **Tipo contrapartida**, seleccione **Cuenta bancaria**.</span><span class="sxs-lookup"><span data-stu-id="e7dda-115">In the **Bal. Account Type** field, select **Bank Account**.</span></span>
7. <span data-ttu-id="e7dda-116">En el campo **Cta. contrapartida**, seleccione la cuenta a la que quiere transferir los fondos.</span><span class="sxs-lookup"><span data-stu-id="e7dda-116">In the **Bal. Account No.** field, select the bank account to which you want to transfer the funds.</span></span>
8. <span data-ttu-id="e7dda-117">Registre el diario.</span><span class="sxs-lookup"><span data-stu-id="e7dda-117">Post the journal.</span></span>

## <a name="to-post-a-transfer-between-bank-accounts-with-different-currency-codes"></a><span data-ttu-id="e7dda-118">Para registrar transferencias entre bancos con códigos de divisa distintos</span><span class="sxs-lookup"><span data-stu-id="e7dda-118">To post a transfer between bank accounts with different currency codes</span></span>

<span data-ttu-id="e7dda-119">Para transferir fondos entre cuentas bancarias que usan distintas divisas, debe registrar dos líneas de diario general.</span><span class="sxs-lookup"><span data-stu-id="e7dda-119">To transfer funds between bank accounts that use different currencies, you must post two general journal lines.</span></span>

1. <span data-ttu-id="e7dda-120">Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), introduzca **Diario general** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="e7dda-120">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **General Journal**, and then choose the related link.</span></span>
2. <span data-ttu-id="e7dda-121">Cree dos líneas de diario y rellene los campos **Fecha de registro** y **N.º de documento**.</span><span class="sxs-lookup"><span data-stu-id="e7dda-121">Create two journal lines, and fill in the **Posting Date** and **Document No.** fields.</span></span>
3. <span data-ttu-id="e7dda-122">En la primera línea de diario, en el campo **Tipo**, seleccione **Cuenta bancaria**.</span><span class="sxs-lookup"><span data-stu-id="e7dda-122">On the first journal line, in the **Type** field, select **Bank Account**.</span></span>
4. <span data-ttu-id="e7dda-123">En el campo **N.º de cuenta**, seleccione la cuenta desde la que quiere transferir los fondos.</span><span class="sxs-lookup"><span data-stu-id="e7dda-123">In the **Account No.** field, select the bank account from which you want to transfer the funds.</span></span>
5. <span data-ttu-id="e7dda-124">En el campo **Importe**, introduzca el importe en la divisa de la cuenta bancaria, con o sin signo menos.</span><span class="sxs-lookup"><span data-stu-id="e7dda-124">In the **Amount** field, enter the amount in the currency of the bank account with or without a minus sign.</span></span>

    > [!TIP]
    > <span data-ttu-id="e7dda-125">Una cantidad sin signo es un débito y una cantidad con signo menos es un crédito.</span><span class="sxs-lookup"><span data-stu-id="e7dda-125">An amount without a sign is a debit, and an amount with a minus sign is a credit.</span></span>

    > [!NOTE]
    > <span data-ttu-id="e7dda-126">Algunas empresas prefieren realizar transferencias entre cuentas en líneas de diario separadas.</span><span class="sxs-lookup"><span data-stu-id="e7dda-126">Some companies prefer to transfer between accounts on separate journal lines.</span></span> <span data-ttu-id="e7dda-127">Otras empresas prefieren publicar todo en una línea de diario utilizando una cuenta de contrapartida.</span><span class="sxs-lookup"><span data-stu-id="e7dda-127">Other companies prefer to post everything on one journal line by using a balancing account.</span></span> <span data-ttu-id="e7dda-128">Consulte con su experto local si no está seguro de qué hacer.</span><span class="sxs-lookup"><span data-stu-id="e7dda-128">Check with your local expert if you're not sure what to do.</span></span>
    >
    > <span data-ttu-id="e7dda-129">Si su empresa prefiere utilizar una cuenta de contrapartida, establezca el campo **Tipo de cuenta de contrapartida** en **Banco** y establezca el **N.º de cuenta de contrapartida** en el banco al que desea transferir los fondos.</span><span class="sxs-lookup"><span data-stu-id="e7dda-129">If your company prefers to use a balancing account, then set the **Bal. Account Type** field to **Bank Account**, and set the **Bal. Account No.** field to the bank account to which you want to transfer the funds.</span></span> <span data-ttu-id="e7dda-130">Luego continúe con el paso 9 o 10.</span><span class="sxs-lookup"><span data-stu-id="e7dda-130">Then proceed to step 9 or 10.</span></span>
    >
    > <span data-ttu-id="e7dda-131">Si su empresa prefiere utilizar una línea de diario separada, continúe con el siguiente paso.</span><span class="sxs-lookup"><span data-stu-id="e7dda-131">If your company prefers to use a separate journal line, then move on to the next step.</span></span>
6. <span data-ttu-id="e7dda-132">En la segunda línea de diario, en el campo **Tipo**, seleccione **Cuenta bancaria**.</span><span class="sxs-lookup"><span data-stu-id="e7dda-132">On the second journal line, in the **Type** field, select **Bank Account**.</span></span>
7. <span data-ttu-id="e7dda-133">En el campo **N.º cuenta**, seleccione la cuenta a la que quiere transferir los fondos.</span><span class="sxs-lookup"><span data-stu-id="e7dda-133">In the **Account No.** field, select the bank account to which you want to transfer the funds.</span></span>
8. <span data-ttu-id="e7dda-134">En el campo **Importe**, introduzca el importe en la divisa de la cuenta bancaria, con o sin signo menos.</span><span class="sxs-lookup"><span data-stu-id="e7dda-134">In the **Amount** field, enter the amount in the currency of the bank account with or without a minus sign.</span></span>

    > [!TIP]
    > <span data-ttu-id="e7dda-135">Una cantidad sin signo es un débito y una cantidad con signo menos es un crédito.</span><span class="sxs-lookup"><span data-stu-id="e7dda-135">An amount without a sign is a debit, and an amount with a minus sign is a credit.</span></span>
9. <span data-ttu-id="e7dda-136">Si los tipos de cambio usados en el diario son diferentes a los contenidos en la página **Tipos de cambio de divisa**, introduzca una nueva línea del diario para el beneficio o la pérdida del tipo de cambio.</span><span class="sxs-lookup"><span data-stu-id="e7dda-136">If the exchange rates used in the journal are different than the exchange rates on the **Currency Exchange Rates** page, enter a new journal line for the exchange rate gain or loss.</span></span>  

    1. <span data-ttu-id="e7dda-137">Especifique **Cuenta** en el campo **Tipo mov**.</span><span class="sxs-lookup"><span data-stu-id="e7dda-137">Enter **G/L Account** in the **Account Type** field.</span></span>  

    2. <span data-ttu-id="e7dda-138">Especifique el número de cuenta para la pérdida o ganancia de tipo de campo en el campo **Nº cuenta**.</span><span class="sxs-lookup"><span data-stu-id="e7dda-138">Enter the G/L account number for exchange rate gain or loss in the **Account No.** field.</span></span>  

    3. <span data-ttu-id="e7dda-139">Introduzca el beneficio o la pérdida del tipo de cambio en el campo **Importe**, con o sin signo menos.</span><span class="sxs-lookup"><span data-stu-id="e7dda-139">Enter the exchange rate gain or loss in the **Amount** field with or without a minus sign.</span></span>

    > [!TIP]
    > <span data-ttu-id="e7dda-140">Una cantidad sin signo es un débito y una cantidad con signo menos es un crédito.</span><span class="sxs-lookup"><span data-stu-id="e7dda-140">An amount without a sign is a debit, and an amount with a minus sign is a credit.</span></span>
10. <span data-ttu-id="e7dda-141">Registre el diario.</span><span class="sxs-lookup"><span data-stu-id="e7dda-141">Post the journal.</span></span>

## <a name="see-also"></a><span data-ttu-id="e7dda-142">Consulte también</span><span class="sxs-lookup"><span data-stu-id="e7dda-142">See Also</span></span>

[<span data-ttu-id="e7dda-143">Conciliar bancos</span><span class="sxs-lookup"><span data-stu-id="e7dda-143">Reconciling Bank Accounts</span></span>](bank-manage-bank-accounts.md)  
[<span data-ttu-id="e7dda-144">Configurar banca</span><span class="sxs-lookup"><span data-stu-id="e7dda-144">Setting Up Banking</span></span>](bank-setup-banking.md)  
[<span data-ttu-id="e7dda-145">Trabajar con diarios generales</span><span class="sxs-lookup"><span data-stu-id="e7dda-145">Working with General Journals</span></span>](ui-work-general-journals.md)  
<span data-ttu-id="e7dda-146">[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="e7dda-146">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>


[!INCLUDE[footer-include](includes/footer-banner.md)]