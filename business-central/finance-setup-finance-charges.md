---
title: Configurar términos interés
description: Obtenga información sobre cómo configurar Business Central para poder informar a los clientes de los cargos adicionales mediante el envío de notas de cargos financieros.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: payment due, debt, overdue, fee, charge
ms.date: 12/03/2020
ms.author: edupont
ms.openlocfilehash: dad02adfb6cc0a0ebb6d950b67f2e092b3313c59
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5377092"
---
# <a name="set-up-finance-charge-terms"></a><span data-ttu-id="1b982-103">Configurar términos interés</span><span class="sxs-lookup"><span data-stu-id="1b982-103">Set Up Finance Charge Terms</span></span>

<span data-ttu-id="1b982-104">Si un cliente no paga en la fecha de vencimiento, puede calcular automáticamente intereses y añadirlos a los importes vencidos en la cuenta del cliente.</span><span class="sxs-lookup"><span data-stu-id="1b982-104">When a customer does not pay by the due date, you can have finance charges calculated automatically and add them to the overdue amounts on the customer's account.</span></span> <span data-ttu-id="1b982-105">Puede informar a los clientes de los cargos añadidos enviando documentos de interés.</span><span class="sxs-lookup"><span data-stu-id="1b982-105">You can inform customers of the added charges by sending finance charge memos.</span></span> <span data-ttu-id="1b982-106">Pero primero debe definir un código que represente cada cálculo de interés financiero.</span><span class="sxs-lookup"><span data-stu-id="1b982-106">But first, you must set up a code that represents each finance charge calculation.</span></span> <span data-ttu-id="1b982-107">Después puede introducir este código en el campo Cód. interés de las fichas de cliente.</span><span class="sxs-lookup"><span data-stu-id="1b982-107">Then you can enter this code in the Fin. Charge Terms Code field on customer cards.</span></span>  

## <a name="finance-charge-terms"></a><span data-ttu-id="1b982-108">Términos interés</span><span class="sxs-lookup"><span data-stu-id="1b982-108">Finance charge terms</span></span>

<span data-ttu-id="1b982-109">Debe configurar los términos del cargo financiero para cada cálculo del cargo financiero y luego asignar los términos al cliente en el campo **Código de condiciones de cargo financiero** en la página **Cliente**.</span><span class="sxs-lookup"><span data-stu-id="1b982-109">You must set up finance charge terms for each finance charge calculation, and then assign the terms to the customer in the **Fin. Charge Terms Code** field on the **Customer** page.</span></span>

<span data-ttu-id="1b982-110">Puede calcular los intereses utilizando el cálculo por días crédito o bien el cálculo por saldo vencido.</span><span class="sxs-lookup"><span data-stu-id="1b982-110">Finance charges can be calculated using either the average daily balance or the balance due methods.</span></span>

* <span data-ttu-id="1b982-111">Días saldo vencido</span><span class="sxs-lookup"><span data-stu-id="1b982-111">Average daily balance</span></span>  
  
  <span data-ttu-id="1b982-112">Se tiene en cuenta el número de días de vencimiento del pago:</span><span class="sxs-lookup"><span data-stu-id="1b982-112">The number of days the payment is overdue is taken into account:</span></span>  
  <span data-ttu-id="1b982-113">*Método del Saldo medio día* - *intereses* = *Saldo vencido* x *(Días vencidos/Periodo de interés)* x *(Tipo interés/100)*</span><span class="sxs-lookup"><span data-stu-id="1b982-113">*Average Daily Balance method* - *Finance Charge* = *Overdue Amount* x *(Days Overdue / Interest Period)* x *(Interest Rate/100)*</span></span>

* <span data-ttu-id="1b982-114">Saldo vencido</span><span class="sxs-lookup"><span data-stu-id="1b982-114">Balance due</span></span>  
  
  <span data-ttu-id="1b982-115">El interés es una parte porcentual de éste:</span><span class="sxs-lookup"><span data-stu-id="1b982-115">The finance charge is a percentage of the overdue amount:</span></span>  
  <span data-ttu-id="1b982-116">*Método del Saldo vencido* - *intereses* = *Saldo vencido* x *(Tipo interés / 100)*</span><span class="sxs-lookup"><span data-stu-id="1b982-116">*Balance Due method* - *Finance Charge* = *Overdue Amount* x *(Interest Rate / 100)*</span></span>

<span data-ttu-id="1b982-117">Además, cada término de la tabla Términos interés está vinculado a la subtabla Texto interés.</span><span class="sxs-lookup"><span data-stu-id="1b982-117">Additionally, each term in the Finance Charge Terms table is linked to a subtable, the Finance Charge Text table.</span></span> <span data-ttu-id="1b982-118">Por cada grupo de términos de interés, puede definir un texto inicial y/o final que se incluyen en el documento de interés.</span><span class="sxs-lookup"><span data-stu-id="1b982-118">For each set of finance charge terms, you can define a beginning and/or an ending text to include on the finance charge memo.</span></span>

### <a name="to-set-up-finance-charge-terms"></a><span data-ttu-id="1b982-119">Configurar términos interés</span><span class="sxs-lookup"><span data-stu-id="1b982-119">To set up finance charge terms</span></span>

1. <span data-ttu-id="1b982-120">Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Términos interés** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="1b982-120">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Finance Charge Terms**, and then choose the related link.</span></span>  
2. <span data-ttu-id="1b982-121">Rellene los campos según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="1b982-121">Fill in the fields as necessary.</span></span>
3. <span data-ttu-id="1b982-122">Para utilizar más de una combinación de términos interés, configure un código para cada uno.</span><span class="sxs-lookup"><span data-stu-id="1b982-122">To use more than one combination of finance charge terms, set up a code for each one.</span></span>

    <span data-ttu-id="1b982-123">Para cada término de interés, puede especificar condiciones individuales, que pueden incluir comisiones adicionales tanto en la divisa local como en la divisa extranjera.</span><span class="sxs-lookup"><span data-stu-id="1b982-123">For each finance charge term, you can specify individual conditions that can include additional fees in both LCY and in foreign currency.</span></span> <span data-ttu-id="1b982-124">Puede definir muchos recargos adicionales en divisas extranjeras para cada término de la página **Términos interés**.</span><span class="sxs-lookup"><span data-stu-id="1b982-124">You can define additional fees in foreign currencies for each term on the **Finance Charge Terms** page.</span></span>
4. <span data-ttu-id="1b982-125">Seleccione la acción **Divisas**.</span><span class="sxs-lookup"><span data-stu-id="1b982-125">Choose the **Currencies** action.</span></span>
5. <span data-ttu-id="1b982-126">En la página **Divisas por térms. interés**, defina para cada término un código de divisa y un recargo adicional.</span><span class="sxs-lookup"><span data-stu-id="1b982-126">On the **Currencies for Fin. Chrg. Terms** page, define for each term a currency code and an additional fee.</span></span>

    > [!NOTE]  
    > <span data-ttu-id="1b982-127">Cuando crea intereses en una divisa extranjera, las condiciones de la divisa extranjera que ha configurado se utilizarán para crear documentos de interés.</span><span class="sxs-lookup"><span data-stu-id="1b982-127">When you create finance charges in a foreign currency, the foreign currency conditions that you set up here will be used to create finance charge memos.</span></span> <span data-ttu-id="1b982-128">Si no se han configurado condiciones de interés en divisa extranjera, las condiciones de interés de DL especificadas en la página **Términos interés** se utilizarán y convertirán en la divisa pertinente.</span><span class="sxs-lookup"><span data-stu-id="1b982-128">If there are no foreign currency finance charge conditions set up, the LCY finance charge conditions specified on the **Finance Charge Terms** page will be used and then converted to the relevant currency.</span></span>

    <span data-ttu-id="1b982-129">Para cada interés puede especificar un texto que se imprima antes (**comienzo texto**) o después (**fin texto**) de los movimientos del documento de interés.</span><span class="sxs-lookup"><span data-stu-id="1b982-129">For each finance charge term, you can specify text that will be printed before (**Beginning Text**) or after (**Ending Text**) on the entries on the finance charge memo.</span></span>  
6. <span data-ttu-id="1b982-130">Elija las acciones **Comienzo texto** o **Fin texto** respectivamente, y rellene la página **Texto interés**.</span><span class="sxs-lookup"><span data-stu-id="1b982-130">Choose the **Beginning Text** or **Ending Text** actions respectively, and fill on the **Finance Charge Text** page.</span></span>
7. <span data-ttu-id="1b982-131">Para insertar automáticamente valores relacionados en el texto de interés resultante, escriba los siguientes marcadores de posición en el campo **Texto**.</span><span class="sxs-lookup"><span data-stu-id="1b982-131">To automatically insert related values in the resulting finance charge text, enter the following placeholders in the **Text** field.</span></span>

|<span data-ttu-id="1b982-132">Marcador de posición</span><span class="sxs-lookup"><span data-stu-id="1b982-132">Placeholder</span></span>|<span data-ttu-id="1b982-133">Valor</span><span class="sxs-lookup"><span data-stu-id="1b982-133">Value</span></span>|  
|-----------------|-----------|  
|<span data-ttu-id="1b982-134">%1</span><span class="sxs-lookup"><span data-stu-id="1b982-134">%1</span></span>|<span data-ttu-id="1b982-135">Contenido del campo **Fecha emisión documento** en la cabecera del documento de interés</span><span class="sxs-lookup"><span data-stu-id="1b982-135">Content of the **Document Date** field on the finance charge memo header</span></span>|  
|<span data-ttu-id="1b982-136">%2</span><span class="sxs-lookup"><span data-stu-id="1b982-136">%2</span></span>|<span data-ttu-id="1b982-137">Contenido del campo **Fecha de vencimiento** en la cabecera del documento de interés</span><span class="sxs-lookup"><span data-stu-id="1b982-137">Content of the **Due Date** field on the finance charge memo header</span></span>|  
|<span data-ttu-id="1b982-138">%3</span><span class="sxs-lookup"><span data-stu-id="1b982-138">%3</span></span>|<span data-ttu-id="1b982-139">Contenido del campo **Tipo interés** en las condiciones relacionadas con las cargas financieras</span><span class="sxs-lookup"><span data-stu-id="1b982-139">Content of the **Interest Rate** field on the related finance charge terms</span></span>|  
|<span data-ttu-id="1b982-140">%4</span><span class="sxs-lookup"><span data-stu-id="1b982-140">%4</span></span>|<span data-ttu-id="1b982-141">Contenido del campo **Importe pendiente** en la cabecera del documento de interés</span><span class="sxs-lookup"><span data-stu-id="1b982-141">Content of the **Remaining Amount** field on the finance charge memo header</span></span>|  
|<span data-ttu-id="1b982-142">%5</span><span class="sxs-lookup"><span data-stu-id="1b982-142">%5</span></span>|<span data-ttu-id="1b982-143">Contenido del campo **Importe interés** en la cabecera del documento de interés</span><span class="sxs-lookup"><span data-stu-id="1b982-143">Content of the **Interest Amount** field on the finance charge memo header</span></span>|  
|<span data-ttu-id="1b982-144">%6</span><span class="sxs-lookup"><span data-stu-id="1b982-144">%6</span></span>|<span data-ttu-id="1b982-145">Contenido del campo **Recargo adicional** en la cabecera del documento de interés</span><span class="sxs-lookup"><span data-stu-id="1b982-145">Content of the **Additional Fee** field on the finance charge memo header</span></span>|  
|<span data-ttu-id="1b982-146">%7</span><span class="sxs-lookup"><span data-stu-id="1b982-146">%7</span></span>|<span data-ttu-id="1b982-147">Importe total del recordatorio.</span><span class="sxs-lookup"><span data-stu-id="1b982-147">The total amount of the reminder</span></span>|  
|<span data-ttu-id="1b982-148">%8</span><span class="sxs-lookup"><span data-stu-id="1b982-148">%8</span></span>|<span data-ttu-id="1b982-149">Contenido del campo **Código divisa** en la cabecera del documento de interés</span><span class="sxs-lookup"><span data-stu-id="1b982-149">Content of the **Currency Code** field on the finance charge memo header</span></span>|  
|<span data-ttu-id="1b982-150">%9</span><span class="sxs-lookup"><span data-stu-id="1b982-150">%9</span></span>|<span data-ttu-id="1b982-151">Contenido del campo **Fecha registro** en la cabecera del documento de interés</span><span class="sxs-lookup"><span data-stu-id="1b982-151">Content of the **Posting Date** field on the finance charge memo header</span></span>|  

## <a name="see-also"></a><span data-ttu-id="1b982-152">Consulte también .</span><span class="sxs-lookup"><span data-stu-id="1b982-152">See also</span></span>

[<span data-ttu-id="1b982-153">Cobrar saldos pendientes</span><span class="sxs-lookup"><span data-stu-id="1b982-153">Collect Outstanding Balances</span></span>](receivables-collect-outstanding-balances.md)  
[<span data-ttu-id="1b982-154">Configurar términos y niveles de recordatorios.</span><span class="sxs-lookup"><span data-stu-id="1b982-154">Set Up Reminder Terms and Levels</span></span>](finance-setup-reminders.md)  
[<span data-ttu-id="1b982-155">Configurar las finanzas</span><span class="sxs-lookup"><span data-stu-id="1b982-155">Setting Up Finance</span></span>](finance-setup-finance.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]