---
title: Transferir fondos bancarios | Documentos de Microsoft
description: "Puede transferir importes de una cuenta bancaria a otra, con divisas distintas, registrando la transacción en el diario general."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: bank account transfer, multiple currencies
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 758833e146c03cde3f892ec24d43143bcdce655c
ms.contentlocale: es-es
ms.lasthandoff: 09/28/2018

---
# <a name="transfer-bank-funds"></a><span data-ttu-id="6bf89-103">Transferir fondos bancarios</span><span class="sxs-lookup"><span data-stu-id="6bf89-103">Transfer Bank Funds</span></span>
<span data-ttu-id="6bf89-104">En ocasiones es necesario transferir un importe desde una cuenta bancaria a otra.</span><span class="sxs-lookup"><span data-stu-id="6bf89-104">You may sometimes need to transfer an amount from one bank account to another.</span></span> <span data-ttu-id="6bf89-105">Para hacerlo, debe registrar una transacción en el diario general.</span><span class="sxs-lookup"><span data-stu-id="6bf89-105">To do this, you must post the a transaction in the general journal.</span></span> <span data-ttu-id="6bf89-106">La tarea varía en función de si los bancos usan la misma divisa o distintas divisas.</span><span class="sxs-lookup"><span data-stu-id="6bf89-106">The task varies depending on whether the bank accounts use the same currency or different currencies.</span></span>

## <a name="to-post-a-transfer-between-bank-accounts-with-the-same-currency-code"></a><span data-ttu-id="6bf89-107">Para registrar transferencias entre bancos con el mismo código de divisa</span><span class="sxs-lookup"><span data-stu-id="6bf89-107">To post a transfer between bank accounts with the same currency code</span></span>
1. <span data-ttu-id="6bf89-108">Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Diario general** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="6bf89-108">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **General Journal**, and then choose the related link.</span></span>
2. <span data-ttu-id="6bf89-109">En una línea de diario, rellene los campos **Fecha registro** y **Nº documento**.</span><span class="sxs-lookup"><span data-stu-id="6bf89-109">On a journal line, fill in the **Posting Date** and **Document No.** fields.</span></span>
3. <span data-ttu-id="6bf89-110">En el campo **Tipo mov**, seleccione **Banco**.</span><span class="sxs-lookup"><span data-stu-id="6bf89-110">In the **Account Type** field, select **Bank Account**.</span></span>
4. <span data-ttu-id="6bf89-111">En el campo **N.º de cuenta**, seleccione la cuenta desde la que quiere transferir los fondos.</span><span class="sxs-lookup"><span data-stu-id="6bf89-111">In the **Account No.** field, select the bank from which you want to transfer the funds.</span></span>
5. <span data-ttu-id="6bf89-112">En el campo **Importe**, introduzca el importe que quiere transferir.</span><span class="sxs-lookup"><span data-stu-id="6bf89-112">In the **Amount** field, enter the amount to be transferred.</span></span>
6. <span data-ttu-id="6bf89-113">En el campo **Tipo contrapartida**, seleccione **Cuenta bancaria**.</span><span class="sxs-lookup"><span data-stu-id="6bf89-113">In the **Bal. Account Type** field, select **Bank Account**.</span></span>
7. <span data-ttu-id="6bf89-114">En el campo **Cta. contrapartida**, seleccione la cuenta a la que quiere transferir los fondos.</span><span class="sxs-lookup"><span data-stu-id="6bf89-114">In the **Bal. Account No.** field, select the bank account to which you want to transfer the funds.</span></span>
8. <span data-ttu-id="6bf89-115">Registre el diario.</span><span class="sxs-lookup"><span data-stu-id="6bf89-115">Post the journal.</span></span>

## <a name="to-post-a-transfer-between-bank-accounts-with-different-currency-codes"></a><span data-ttu-id="6bf89-116">Para registrar transferencias entre bancos con códigos de divisa distintos</span><span class="sxs-lookup"><span data-stu-id="6bf89-116">To post a transfer between bank accounts with different currency codes</span></span>
<span data-ttu-id="6bf89-117">Para transferir fondos entre cuentas bancarias que usan distintas divisas, debe registrar dos líneas de diario general.</span><span class="sxs-lookup"><span data-stu-id="6bf89-117">To transfer funds between bank accounts that use different currencies, you must post two general journal lines.</span></span>

1. <span data-ttu-id="6bf89-118">Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Diario general** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="6bf89-118">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **General Journal**, and then choose the related link.</span></span>
2. <span data-ttu-id="6bf89-119">Cree dos líneas de diario y rellene los campos **Fecha de registro** y **N.º de documento**.</span><span class="sxs-lookup"><span data-stu-id="6bf89-119">Create two journal lines, and fill in the **Posting Date** and **Document No.** fields.</span></span>
3. <span data-ttu-id="6bf89-120">En la primera línea de diario, en el campo **Tipo**, seleccione **Cuenta bancaria**.</span><span class="sxs-lookup"><span data-stu-id="6bf89-120">On the first journal line, in the **Type** field, select **Bank Account**.</span></span>
4. <span data-ttu-id="6bf89-121">En el campo **N.º de cuenta**, seleccione la cuenta desde la que quiere transferir los fondos.</span><span class="sxs-lookup"><span data-stu-id="6bf89-121">In the **Account No.** field, select the bank account from which you want to transfer the funds.</span></span>
5. <span data-ttu-id="6bf89-122">En el campo **Importe**, introduzca el importe en la divisa de la cuenta bancaria.</span><span class="sxs-lookup"><span data-stu-id="6bf89-122">In the **Amount** field, enter the amount in the currency of the bank account.</span></span> <span data-ttu-id="6bf89-123">Escriba los importes de crédito con un signo menos.</span><span class="sxs-lookup"><span data-stu-id="6bf89-123">Enter credit amounts with a minus sign.</span></span> <span data-ttu-id="6bf89-124">Escriba los importes de débito sin el signo menos.</span><span class="sxs-lookup"><span data-stu-id="6bf89-124">Enter debit amounts without a minus sign.</span></span>
6. <span data-ttu-id="6bf89-125">En el campo **Tipo contrapartida**, seleccione **Cuenta bancaria**.</span><span class="sxs-lookup"><span data-stu-id="6bf89-125">In the **Bal. Account Type** field, select **Bank Account**.</span></span>
7. <span data-ttu-id="6bf89-126">En el campo **Cta. contrapartida**, seleccione la cuenta a la que quiere transferir los fondos.</span><span class="sxs-lookup"><span data-stu-id="6bf89-126">In the **Bal. Account No.** field, select the bank account to which you want to transfer the funds.</span></span>
8. <span data-ttu-id="6bf89-127">En la segunda línea de diario, en el campo **Tipo**, seleccione **Cuenta bancaria**.</span><span class="sxs-lookup"><span data-stu-id="6bf89-127">On the second journal line, in the **Type** field, select **Bank Account**.</span></span>
9. <span data-ttu-id="6bf89-128">En el campo **N.º cuenta**, seleccione la cuenta a la que quiere transferir los fondos.</span><span class="sxs-lookup"><span data-stu-id="6bf89-128">In the **Account No.** field, select the bank account to which you want to transfer the funds.</span></span>
10. <span data-ttu-id="6bf89-129">En el campo **Importe**, introduzca el importe en la divisa de la cuenta bancaria.</span><span class="sxs-lookup"><span data-stu-id="6bf89-129">In the **Amount** field, enter the amount in the currency of the bank account.</span></span> <span data-ttu-id="6bf89-130">Escriba los importes de crédito con un signo menos.</span><span class="sxs-lookup"><span data-stu-id="6bf89-130">Enter credit amounts with a minus sign.</span></span> <span data-ttu-id="6bf89-131">Escriba los importes de débito sin el signo menos.</span><span class="sxs-lookup"><span data-stu-id="6bf89-131">Enter debit amounts without a minus sign.</span></span>
11. <span data-ttu-id="6bf89-132">En el campo **Tipo contrapartida**, seleccione **Cuenta bancaria**.</span><span class="sxs-lookup"><span data-stu-id="6bf89-132">In the **Bal. Account Type** field, select **Bank Account**.</span></span>  
12. <span data-ttu-id="6bf89-133">En el campo **Cta. contrapartida**, seleccione la cuenta desde la que quiere transferir los fondos.</span><span class="sxs-lookup"><span data-stu-id="6bf89-133">In the **Bal. Account No.** field, select the bank account from which you want to transfer the funds.</span></span>

    > [!NOTE]  
    > <span data-ttu-id="6bf89-134">Si los tipos de cambio usados en el diario son diferentes a los contenidos en la ventana **Tipos de cambio de divisa**, introduzca una tercera línea para las diferencias positivas o negativas del cambio.</span><span class="sxs-lookup"><span data-stu-id="6bf89-134">If the exchange rates used in the journal are different than the exchange rates in the **Currency Exchange Rates** window, enter a third line for the exchange rate gain or loss.</span></span> <span data-ttu-id="6bf89-135">Especifique **Cuenta** en el campo **Tipo mov**.</span><span class="sxs-lookup"><span data-stu-id="6bf89-135">Enter **G/L Account** in the **Account Type** field.</span></span> <span data-ttu-id="6bf89-136">Especifique el número de cuenta para la pérdida o ganancia de tipo de campo en el campo **Nº cuenta**.</span><span class="sxs-lookup"><span data-stu-id="6bf89-136">Enter the G/L account number for exchange rate gain or loss in the **Account No.** field.</span></span> <span data-ttu-id="6bf89-137">Introduzca la diferencia positiva o negativa del tipo de cambio en el campo **Importe** con o sin el signo menos para los créditos y los débitos respectivamente.</span><span class="sxs-lookup"><span data-stu-id="6bf89-137">Enter the exchange rate gain or loss in the **Amount** field with or without a minus sign for credits and debits respectively.</span></span>
13. <span data-ttu-id="6bf89-138">Registre el diario.</span><span class="sxs-lookup"><span data-stu-id="6bf89-138">Post the journal.</span></span>

## <a name="see-also"></a><span data-ttu-id="6bf89-139">Consulte también</span><span class="sxs-lookup"><span data-stu-id="6bf89-139">See Also</span></span>
[<span data-ttu-id="6bf89-140">Administrar cuentas bancarias</span><span class="sxs-lookup"><span data-stu-id="6bf89-140">Managing Bank Accounts</span></span>](bank-manage-bank-accounts.md)  
[<span data-ttu-id="6bf89-141">Configurar banca</span><span class="sxs-lookup"><span data-stu-id="6bf89-141">Setting Up Banking</span></span>](bank-setup-banking.md)  
[<span data-ttu-id="6bf89-142">Trabajar con diarios generales</span><span class="sxs-lookup"><span data-stu-id="6bf89-142">Working with General Journals</span></span>](ui-work-general-journals.md)  
<span data-ttu-id="6bf89-143">[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="6bf89-143">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

