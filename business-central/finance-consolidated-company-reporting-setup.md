---
title: Configurar la consolidación de empresas
description: Descubra cómo puede configurar cómo se informan los datos de diferentes empresas de Business Central en una empresa de consolidación.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: consolidation, subsidiaries, consolidate
ms.date: 10/01/2020
ms.author: bholtorf
ms.openlocfilehash: d733b8000d5ea476d32a96bcccdceebc32e0f43c
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "4750985"
---
# <a name="set-up-company-consolidation"></a><span data-ttu-id="13c0b-103">Configuración de la consolidación de empresas</span><span class="sxs-lookup"><span data-stu-id="13c0b-103">Set Up Company Consolidation</span></span>

<span data-ttu-id="13c0b-104">Para poder consolidar los movimientos de contabilidad de dos o más empresas separadas (subsidiarias) en una empresa consolidada, debe preparar los planes de cuentas y la empresa de consolidación.</span><span class="sxs-lookup"><span data-stu-id="13c0b-104">Before you can consolidate the general ledger entries of two or more separate companies (subsidiaries) into a consolidated company, you must prepare the charts of accounts and the consolidation company.</span></span>  

<span data-ttu-id="13c0b-105">En función de la complejidad de sus negocios, hay dos formas de configurar la consolidación:</span><span class="sxs-lookup"><span data-stu-id="13c0b-105">Depending on the complexity of your businesses, there are two ways to set up consolidation:</span></span>

* <span data-ttu-id="13c0b-106">Si no necesita configuraciones avanzadas, como incluir una empresa de la que posea sólo una parte, puede utilizar la guía de configuración asistida **Consolidación de la empresa** para crear rápidamente una consolidación.</span><span class="sxs-lookup"><span data-stu-id="13c0b-106">If you do not need advanced settings, such as including a company that you only own part of, you can use the **Company Consolidation** assisted setup guide to quickly set up a consolidation.</span></span> <span data-ttu-id="13c0b-107">La guía le asiste con los pasos básicos.</span><span class="sxs-lookup"><span data-stu-id="13c0b-107">The guide helps you through the basic steps.</span></span>
* <span data-ttu-id="13c0b-108">Si necesita alguna configuraciones más avanzada, puede configurar las empresas consolidadas y las unidades de negocio manualmente.</span><span class="sxs-lookup"><span data-stu-id="13c0b-108">If you do need more advanced settings, you can set up the consolidated company and business units yourself.</span></span>
  * <span data-ttu-id="13c0b-109">En cada empresa, especifique qué cuentas de contabilidad se deben incluir en la consolidación y especifique el método de traducción de consolidación para cada cuenta.</span><span class="sxs-lookup"><span data-stu-id="13c0b-109">In each business unit, specify which general ledger accounts are to be included in the consolidation, and specify the consolidation translation method for each account.</span></span>
  * <span data-ttu-id="13c0b-110">En la empresa consolidada, configure una tarjeta de empresa para cada empresa que se desee incluir en la consolidación.</span><span class="sxs-lookup"><span data-stu-id="13c0b-110">In the consolidation company, set up a business unit card for each company to be included in the consolidation.</span></span> <span data-ttu-id="13c0b-111">La tarjeta de empresa incluye información como las fechas del ejercicio de la empresa y el porcentaje de cada cuenta que debe incluirse en la consolidación.</span><span class="sxs-lookup"><span data-stu-id="13c0b-111">The business unit card includes information, such as the dates of the business unit's fiscal year, and the percentage of each account that must be included in the consolidation.</span></span>

## <a name="simple-consolidation-setup"></a><span data-ttu-id="13c0b-112">Configuración de consolidación sencilla</span><span class="sxs-lookup"><span data-stu-id="13c0b-112">Simple consolidation setup</span></span>

<span data-ttu-id="13c0b-113">Si su consolidación es directa, por ejemplo porque es propietario de la totalidad de las empresas a consolidar, la guía de configuración asistida **Consolidación de la empresa** le ayudará con los pasos siguientes:</span><span class="sxs-lookup"><span data-stu-id="13c0b-113">If your consolidation is straightforward, for example because you wholly-own the business units to consolidate, the **Company Consolidation** assisted setup guide will help you through the following steps:</span></span>

* <span data-ttu-id="13c0b-114">Indique si crear una nueva empresa consolidada, o si consolidar los datos en una empresa que ya haya creado para la consolidación.</span><span class="sxs-lookup"><span data-stu-id="13c0b-114">Choose whether to create a new consolidated company, or whether to consolidate the data in a company that you have already created for the consolidation.</span></span> <span data-ttu-id="13c0b-115">La empresa no debe contener transacciones.</span><span class="sxs-lookup"><span data-stu-id="13c0b-115">The company should not contain transactions.</span></span>
* <span data-ttu-id="13c0b-116">Previsualizar los resultados.</span><span class="sxs-lookup"><span data-stu-id="13c0b-116">Preview the results.</span></span> [!INCLUDE[prod_short](includes/prod_short.md)] <span data-ttu-id="13c0b-117">comprueba que los datos y las transacciones maestros se pueden transferir correctamente a la empresa consolidada.</span><span class="sxs-lookup"><span data-stu-id="13c0b-117">verifies that the master data and transactions can be successfully transferred to the consolidated company.</span></span>

<span data-ttu-id="13c0b-118">Para usar la guía de configuración asistida, realice los pasos siguientes:</span><span class="sxs-lookup"><span data-stu-id="13c0b-118">To use the assisted setup guide, follow these steps:</span></span>

1. <span data-ttu-id="13c0b-119">En el centro de rol **Contador** , seleccione la acción **Configuración asistida** .</span><span class="sxs-lookup"><span data-stu-id="13c0b-119">On the **Accountant** Role Center, choose the **Assisted Setup** action.</span></span>
2. <span data-ttu-id="13c0b-120">Seleccione **Configurar informe de consolidación** y después complete cada paso en la guía de configuración asistida.</span><span class="sxs-lookup"><span data-stu-id="13c0b-120">Choose **Set up consolidation reporting**, and then complete each step in the assisted setup guide.</span></span>

## <a name="advanced-consolidation-setup"></a><span data-ttu-id="13c0b-121">Configuración de consolidación avanzada</span><span class="sxs-lookup"><span data-stu-id="13c0b-121">Advanced consolidation setup</span></span>

<span data-ttu-id="13c0b-122">Si necesita más configuraciones avanzadas para su consolidación, puede configurar la consolidación manualmente.</span><span class="sxs-lookup"><span data-stu-id="13c0b-122">If you need more advanced settings for your consolidation, you can set up consolidation manually.</span></span> <span data-ttu-id="13c0b-123">Por ejemplo, si tiene empresas de las que es propietario sólo parcialmente, o tiene las empresas que no desea incluir en la consolidación.</span><span class="sxs-lookup"><span data-stu-id="13c0b-123">For example, if you have companies that you own only partially, or you have companies that you do not want to include in the consolidation.</span></span>  

### <a name="set-up-the-consolidated-company"></a><span data-ttu-id="13c0b-124">Configurar la empresa consolidada</span><span class="sxs-lookup"><span data-stu-id="13c0b-124">Set up the consolidated company</span></span>

<span data-ttu-id="13c0b-125">Primero, debe configurar la empresa consolidada.</span><span class="sxs-lookup"><span data-stu-id="13c0b-125">First, you must set up the consolidated company.</span></span> <span data-ttu-id="13c0b-126">Configure la empresa consolidada de la misma forma que se configuran las demás empresas.</span><span class="sxs-lookup"><span data-stu-id="13c0b-126">You set up the consolidated company in the same way that you set up other companies.</span></span> <span data-ttu-id="13c0b-127">Para obtener más información, vea [Preparación para hacer negocios](ui-get-ready-business.md).</span><span class="sxs-lookup"><span data-stu-id="13c0b-127">For more information, see [Getting Ready for Doing Business](ui-get-ready-business.md).</span></span>  

<span data-ttu-id="13c0b-128">La siguiente lista ilustra los aspectos clave de la empresa consolidada.</span><span class="sxs-lookup"><span data-stu-id="13c0b-128">The following list illustrates key aspects of the consolidated company.</span></span>

1. <span data-ttu-id="13c0b-129">Configurar el plan de cuentas</span><span class="sxs-lookup"><span data-stu-id="13c0b-129">Set up the chart of accounts</span></span>

    <span data-ttu-id="13c0b-130">Para obtener más información, consulte [Configurar o cambiar el plan de cuentas](finance-setup-chart-accounts.md).</span><span class="sxs-lookup"><span data-stu-id="13c0b-130">For more information, see [Setting Up or Changing the Chart of Accounts](finance-setup-chart-accounts.md).</span></span>  

    <span data-ttu-id="13c0b-131">Los planes de cuentas pueden ser idénticos en una empresa y en la empresa consolidada, o bien la empresa consolidada puede tener un plan de cuentas diferente.</span><span class="sxs-lookup"><span data-stu-id="13c0b-131">The charts of accounts can be identical across a business unit and the consolidated company, or the consolidated company can have a different chart of account.</span></span> <span data-ttu-id="13c0b-132">Si el plan de cuentas de una unidad de negocio es diferente al de la empresa consolidada, debe especificar la asignación entre cuentas de las cuentas de la unidad de negocio.</span><span class="sxs-lookup"><span data-stu-id="13c0b-132">If a business unit's chart of accounts is different from that of the consolidated company, you must specify the mapping between accounts on the accounts in the business unit.</span></span> <span data-ttu-id="13c0b-133">Para obtener más información, consulte la sección [Preparar cuentas de contabilidad para la consolidación](#glacc).</span><span class="sxs-lookup"><span data-stu-id="13c0b-133">For more information, see the [Prepare general ledger accounts for consolidation](#glacc) section.</span></span>

2. <span data-ttu-id="13c0b-134">Agregar unidades de negocio</span><span class="sxs-lookup"><span data-stu-id="13c0b-134">Add business units</span></span>

    <span data-ttu-id="13c0b-135">Para consolidar los datos financieros de varias empresas en una sola empresa consolidada, debe introducir la información sobre las subsidiarias como empresas a incluir y el grado hasta el que se incluirán sus cifras.</span><span class="sxs-lookup"><span data-stu-id="13c0b-135">To consolidate several companies' financial data in a consolidated company, you must enter information about the subsidiary as business units to be included and about how much their figures will be included.</span></span>

    <span data-ttu-id="13c0b-136">Para obtener más información, consulte la sección [Agregar unidades de negocio](#busunit).</span><span class="sxs-lookup"><span data-stu-id="13c0b-136">For more information, see the [Add business units](#busunit) section.</span></span>
3. <span data-ttu-id="13c0b-137">Puede especificar tipos de cambio si va a consolidar los resultados financieros de empresas si dichos resultados están en una divisa extranjera.</span><span class="sxs-lookup"><span data-stu-id="13c0b-137">You can specify exchange rates when consolidating the financial statements of business units if the financial statements are in a foreign currency.</span></span>

    <span data-ttu-id="13c0b-138">Los tres tipos de cambio que se usan son **Tipo de cambio medio (manual)**, **Tipo de cambio al cierre** y **Último cambio al cierre**.</span><span class="sxs-lookup"><span data-stu-id="13c0b-138">The three exchange rates that are used are **Average Rate (Manual)**, **Closing Rate**, and **Last Closing Rate**.</span></span> <span data-ttu-id="13c0b-139">Para obtener más información, consulte la sección [Especificar tipos de cambio para consolidaciones](#exchrates).</span><span class="sxs-lookup"><span data-stu-id="13c0b-139">For more information, see the [Specify exchange rates for consolidations](#exchrates) section.</span></span>
4. <span data-ttu-id="13c0b-140">Puede consolidar información sobre dimensiones y cuentas de contabilidad.</span><span class="sxs-lookup"><span data-stu-id="13c0b-140">You can consolidate dimension information and general ledger accounts.</span></span>

    <span data-ttu-id="13c0b-141">Para obtener más información, consulte la sección [Incluir o excluir dimensiones](#dim).</span><span class="sxs-lookup"><span data-stu-id="13c0b-141">For more information, see the [Include or exclude dimensions](#dim) section.</span></span>

### <a name="add-business-units"></a><a name="busunit"></a><span data-ttu-id="13c0b-142">Agregar empresas</span><span class="sxs-lookup"><span data-stu-id="13c0b-142">Add business units</span></span>

[!INCLUDE[prod_short](includes/prod_short.md)] <span data-ttu-id="13c0b-143">le permite configurar una lista de empresas a consolidar, comprobar los datos contables antes de proceder a la consolidación, importar archivos y generar informes de consolidación.</span><span class="sxs-lookup"><span data-stu-id="13c0b-143">lets you set up a list of business units to consolidate, verify the accounting data before you consolidate it, import files, and generate consolidation reports.</span></span>  

1. <span data-ttu-id="13c0b-144">Inicie sesión en la empresa consolidada.</span><span class="sxs-lookup"><span data-stu-id="13c0b-144">Sign in to the consolidated company.</span></span>
2. <span data-ttu-id="13c0b-145">Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Unidades de negocio** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="13c0b-145">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Business Units**, and then choose the related link.</span></span>  
3. <span data-ttu-id="13c0b-146">Elija **Nuevo** y, a continuación, rellene los campos requeridos.</span><span class="sxs-lookup"><span data-stu-id="13c0b-146">Choose **New**, and then fill in the required fields.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!IMPORTANT]
    > <span data-ttu-id="13c0b-147">Cuando rellene los campos **Fecha inicial** y **Fecha final**, asegúrese de cumplir con las reglas GAAP relacionadas con los periodos fiscales de la unidad de negocio y la empresa principal.</span><span class="sxs-lookup"><span data-stu-id="13c0b-147">When you fill in the **Starting Date** and **Ending Date** fields, make sure you comply with GAAP rules concerning the fiscal periods of the business unit versus the parent company.</span></span>
4. <span data-ttu-id="13c0b-148">Repita el paso 3 para cada empresa adicional</span><span class="sxs-lookup"><span data-stu-id="13c0b-148">Repeat step 3 for each additional business unit</span></span>

<span data-ttu-id="13c0b-149">Si su empresa utiliza una divisa extranjera debe especificar el tipo de cambio que debe utilizarse en la consolidación.</span><span class="sxs-lookup"><span data-stu-id="13c0b-149">If your business unit uses a foreign currency, you must specify the exchange rate to use in the consolidation.</span></span> <span data-ttu-id="13c0b-150">También debe introducir la información de consolidación en las cuentas de la empresa.</span><span class="sxs-lookup"><span data-stu-id="13c0b-150">You must also enter consolidation information about the business unit's general ledger accounts.</span></span> <span data-ttu-id="13c0b-151">Estos procesos se describen en las siguientes secciones.</span><span class="sxs-lookup"><span data-stu-id="13c0b-151">These processes are described in the following sections.</span></span>

### <a name="prepare-general-ledger-accounts-for-consolidation"></a><a name="glacc"></a><span data-ttu-id="13c0b-152">Preparar los libros de contabilidad para la consolidación</span><span class="sxs-lookup"><span data-stu-id="13c0b-152">Prepare general ledger accounts for consolidation</span></span>

<span data-ttu-id="13c0b-153">El plan de cuentas de una empresa a consolidar debe especificar las cuentas para consolidación.</span><span class="sxs-lookup"><span data-stu-id="13c0b-153">The chart of accounts for a company that will be consolidated must specify accounts for consolidation.</span></span> <span data-ttu-id="13c0b-154">Por cada cuenta de contabilidad de cada empresa, debe especificar la cuenta de la empresa consolidada a la que se transferirá el saldo tras la consolidación.</span><span class="sxs-lookup"><span data-stu-id="13c0b-154">For each posting general ledger account in each company, you must specify the general ledger account in the consolidated company to which the balance will be transferred on consolidation.</span></span> <span data-ttu-id="13c0b-155">Esta asignación permitirá que se puedan consolidar empresas con planes de cuentas diferentes.</span><span class="sxs-lookup"><span data-stu-id="13c0b-155">This is a mapping that will allow companies with different chart of accounts to be consolidated together.</span></span>

<span data-ttu-id="13c0b-156">Si el plan de cuentas de la unidad de negocio difiere de la empresa consolidada, debe preparar los libros contables para la consolidación.</span><span class="sxs-lookup"><span data-stu-id="13c0b-156">If the chart of accounts in the business unit differs from the consolidated company, you must prepare general ledger accounts for consolidation.</span></span> <span data-ttu-id="13c0b-157">Puede especificar las cuentas para apuntar debe y haber y el método a utilizar para traducir las divisas en la empresa consolidada.</span><span class="sxs-lookup"><span data-stu-id="13c0b-157">You can specify the accounts to post debits and credits to, and the method to use to translate currencies in the consolidated company.</span></span> <span data-ttu-id="13c0b-158">Por ejemplo, esto es útil en caso de ejecutar con frecuencia el informe.</span><span class="sxs-lookup"><span data-stu-id="13c0b-158">For example, this is useful if you frequently run the report.</span></span>

1. <span data-ttu-id="13c0b-159">En cada empresa de [!INCLUDE [prod_short](includes/prod_short.md)], elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Plan de cuentas** y luego elija el vínculo relacionado.</span><span class="sxs-lookup"><span data-stu-id="13c0b-159">In each business unit's [!INCLUDE [prod_short](includes/prod_short.md)], choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Chart of Accounts**, and then choose the related link.</span></span>  
2. <span data-ttu-id="13c0b-160">Abra la ficha de la cuenta, y rellene los campos de la ficha desplegable **Consolidación**.</span><span class="sxs-lookup"><span data-stu-id="13c0b-160">Open the card for the account, and then fill in the fields on the **Consolidation** FastTab.</span></span> [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]

### <a name="specify-exchange-rates-for-consolidations"></a><a name="exchrates"></a><span data-ttu-id="13c0b-161">Especificar los tipos de cambio para consolidaciones</span><span class="sxs-lookup"><span data-stu-id="13c0b-161">Specify exchange rates for consolidations</span></span>

<span data-ttu-id="13c0b-162">Si una unidad de negocio utiliza una divisa diferente de la empresa consolidada, debe especificar los métodos del tipo de cambio para cada cuenta antes de que se consolide.</span><span class="sxs-lookup"><span data-stu-id="13c0b-162">If a business unit uses a different currency than the consolidated company, you must specify exchange rate methods for each account before you consolidate.</span></span> <span data-ttu-id="13c0b-163">Para cada cuenta, el contenido del campo **Método de traducción Consol.** determina el tipo de cambio.</span><span class="sxs-lookup"><span data-stu-id="13c0b-163">For each account, the content of the **Consol. Translation Method** field determines the exchange rate.</span></span> <span data-ttu-id="13c0b-164">En la empresa consolidada, en cada ficha de unidad de negocio, en el campo **Tabla de tipo de cambio de divisa** debe especificar si la consolidación usará tipos de cambio de la empresa o de la empresa consolidada.</span><span class="sxs-lookup"><span data-stu-id="13c0b-164">In the consolidated company, on each business unit card, in the **Currency Exchange Rate Table** field, you specify whether consolidation will use exchange rates from the business unit or the consolidated company.</span></span> <span data-ttu-id="13c0b-165">Si utiliza tipos de cambio de la empresa consolidada, puede cambiar los tipos de cambios para una empresa.</span><span class="sxs-lookup"><span data-stu-id="13c0b-165">If you use exchange rates from the consolidated company, you can change the exchange rates for a business unit.</span></span> <span data-ttu-id="13c0b-166">Para las unidades de negocio, el campo **Tabla de tipo de cambio de divisas** de la ficha de la unidad de negocio contiene **Local**, puede cambiar el tipo de cambio para la ficha de la unidad de negocio.</span><span class="sxs-lookup"><span data-stu-id="13c0b-166">For business units, if the **Currency Exchange Rate Table** field on the business unit card contains **Local**, you can change the exchange rate from the business unit card.</span></span> <span data-ttu-id="13c0b-167">Los tipos de cambio se copian desde la tabla **Tipo cambio divisa**, pero puede cambiarlos antes de la consolidación.</span><span class="sxs-lookup"><span data-stu-id="13c0b-167">The exchange rates are copied from the **Currency Exchange Rate** table, but you can change them before consolidating.</span></span>

<span data-ttu-id="13c0b-168">En la tabla siguiente se describen los métodos del tipo de cambio que puede utilizar para las cuentas.</span><span class="sxs-lookup"><span data-stu-id="13c0b-168">The following table describes the exchange rate methods you can use for accounts.</span></span>

|<span data-ttu-id="13c0b-169">Tipo cambio</span><span class="sxs-lookup"><span data-stu-id="13c0b-169">Exchange rate</span></span> | <span data-ttu-id="13c0b-170">Uso típico</span><span class="sxs-lookup"><span data-stu-id="13c0b-170">Typical use</span></span> |
|---|---|
|<span data-ttu-id="13c0b-171">Tipo de cambio medio (manual)</span><span class="sxs-lookup"><span data-stu-id="13c0b-171">Average Rate (Manual)</span></span> | <span data-ttu-id="13c0b-172">Calcule manualmente el tipo de cambio medio para el periodo que se va a consolidar.</span><span class="sxs-lookup"><span data-stu-id="13c0b-172">You manually calculate the average rate for the period to consolidate.</span></span> <span data-ttu-id="13c0b-173">Calcule aa media aritmética o aproximada y especifique el resultado para cada unidad de negocio.</span><span class="sxs-lookup"><span data-stu-id="13c0b-173">Calculate the average either as an arithmetic average or as a best estimate, and specify the result for each business unit.</span></span> <span data-ttu-id="13c0b-174">Usado para cuenta de beneficios.</span><span class="sxs-lookup"><span data-stu-id="13c0b-174">Used for income statement accounts.</span></span>|
|<span data-ttu-id="13c0b-175">Tipo de cambio al cierre</span><span class="sxs-lookup"><span data-stu-id="13c0b-175">Closing Rate</span></span> | <span data-ttu-id="13c0b-176">Usado para cuentas del balance.</span><span class="sxs-lookup"><span data-stu-id="13c0b-176">Used for balance sheet accounts.</span></span>|
|<span data-ttu-id="13c0b-177">Último cambio al cierre</span><span class="sxs-lookup"><span data-stu-id="13c0b-177">Last Closing Rate</span></span> | <span data-ttu-id="13c0b-178">El tipo de cambio que era válido en el mercado de divisas en la fecha para la que se está preparando el balance o el estado de resultados.</span><span class="sxs-lookup"><span data-stu-id="13c0b-178">The rate that was valid in the foreign exchange market on the date for which the balance sheet or income statement is being prepared.</span></span> <span data-ttu-id="13c0b-179">Introduzca este tipo de cambio para cada unidad de negocio.</span><span class="sxs-lookup"><span data-stu-id="13c0b-179">You enter this rate for each business unit.</span></span> <span data-ttu-id="13c0b-180">Usado para cuentas del balance.</span><span class="sxs-lookup"><span data-stu-id="13c0b-180">Used for balance sheet accounts.</span></span>|
|<span data-ttu-id="13c0b-181">Tipo de cambio histórico</span><span class="sxs-lookup"><span data-stu-id="13c0b-181">Historical Rate</span></span> | <span data-ttu-id="13c0b-182">El tipo de cambio que era válido cuando ocurrió la transacción.</span><span class="sxs-lookup"><span data-stu-id="13c0b-182">The exchange rate that was valid when the transaction occurred.</span></span>|
|<span data-ttu-id="13c0b-183">Tipo de cambio compuesto</span><span class="sxs-lookup"><span data-stu-id="13c0b-183">Composite Rate</span></span> | <span data-ttu-id="13c0b-184">Los importes del periodo actual se traducen con el tipo de cambio medio y se agregan al saldo anteriormente registrado en la empresa consolidada.</span><span class="sxs-lookup"><span data-stu-id="13c0b-184">The current period amounts are translated at the average rate and added to the previously recorded balance in the consolidated company.</span></span> <span data-ttu-id="13c0b-185">Este método se utiliza por lo general para las cuentas de retención de beneficios porque incluyen importes de distintos periodos y son por tanto un compuesto de importes traducidos con distintos tipos de cambio.</span><span class="sxs-lookup"><span data-stu-id="13c0b-185">This method is typically used for retained earnings accounts because they include amounts from different periods and are therefore a composite of amounts translated with different exchange rates.</span></span>|
|<span data-ttu-id="13c0b-186">Tasa de participación</span><span class="sxs-lookup"><span data-stu-id="13c0b-186">Equity Rate</span></span> | <span data-ttu-id="13c0b-187">Esto es similar a **Compuesto**.</span><span class="sxs-lookup"><span data-stu-id="13c0b-187">This is similar to **Composite**.</span></span> <span data-ttu-id="13c0b-188">Las diferencias se registran para separar libros de contabilidad.</span><span class="sxs-lookup"><span data-stu-id="13c0b-188">Differences are posted to separate general ledger accounts.</span></span>|

<span data-ttu-id="13c0b-189">Para especificar los tipos de cambio para las unidades de negocio, realice los pasos siguientes:</span><span class="sxs-lookup"><span data-stu-id="13c0b-189">To specify exchange rates for business units, follow these steps:</span></span>

1. <span data-ttu-id="13c0b-190">Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Unidades de negocio** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="13c0b-190">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Business Units**, and then choose the related link.</span></span>  
2. <span data-ttu-id="13c0b-191">En la página **Lista de unidades de negocio**, seleccione la unidad de negocio y, después, seleccione la acción **Tipo de cambio medio (manual)**.</span><span class="sxs-lookup"><span data-stu-id="13c0b-191">On the **Business Unit List** page, choose the business unit, and then choose the **Average Rate (Manual)** action.</span></span>  
3. <span data-ttu-id="13c0b-192">En la página **Modificar tipo de cambio**, el contenido del campo **Tipo de cambio relacionado** se ha copiado de la tabla **Tipo de cambio de divisa**, pero se puede modificar.</span><span class="sxs-lookup"><span data-stu-id="13c0b-192">On the **Change Exchange Rate** page, the contents of the **Relational Exch. Rate** field have been copied from the **Currency Exchange Rate** table, but you can modify them.</span></span> <span data-ttu-id="13c0b-193">Cierre la página.</span><span class="sxs-lookup"><span data-stu-id="13c0b-193">Close the page.</span></span>  
4. <span data-ttu-id="13c0b-194">Seleccione la acción **Tipo de cambio al cierre**.</span><span class="sxs-lookup"><span data-stu-id="13c0b-194">Choose the **Closing Rate** action.</span></span>  
5. <span data-ttu-id="13c0b-195">En el campo **Cantidad del tipo de cambio relacionado**, introduzca el tipo de cambio.</span><span class="sxs-lookup"><span data-stu-id="13c0b-195">In the **Relational Exch. Rate Amount** field, enter the exchange rate.</span></span>

### <a name="include-or-exclude-dimensions"></a><a name="dim"></a><span data-ttu-id="13c0b-196">Incluir o excluir dimensiones</span><span class="sxs-lookup"><span data-stu-id="13c0b-196">Include or exclude dimensions</span></span>

<span data-ttu-id="13c0b-197">Puede consolidar información sobre dimensiones y cuentas de contabilidad.</span><span class="sxs-lookup"><span data-stu-id="13c0b-197">You can consolidate dimension information and general ledger accounts.</span></span>

* <span data-ttu-id="13c0b-198">En las dimensiones relevantes, especifique el campo **Código de consolidación** o déjelo en blanco</span><span class="sxs-lookup"><span data-stu-id="13c0b-198">On the relevant dimensions, specify the **Consolidation Code** field, or leave it blank</span></span>
  * <span data-ttu-id="13c0b-199">Para excluir una dimensión en la consolidación, deje el campo **Código de consolidación** en la dimensión, y no elija dimensiones en los campos **Copiar dimensiones** de cualquier función o informe de consolidación.</span><span class="sxs-lookup"><span data-stu-id="13c0b-199">To exclude a dimension in the consolidation, leave the **Consolidation Code** field blank on the dimension, and do not choose dimensions in the **Copy Dimensions** fields in any consolidation functions or reports.</span></span>
  * <span data-ttu-id="13c0b-200">Para incluir información de dimensión en la consolidación, deje el campo **Código de consolidación** en blanco.</span><span class="sxs-lookup"><span data-stu-id="13c0b-200">To include dimension information in the consolidation, leave the **Consolidation Code** field blank.</span></span> <span data-ttu-id="13c0b-201">Sin embargo, la consolidación sólo funcionará si los valores de dimensión de la empresa son iguales que los de la empresa consolidada.</span><span class="sxs-lookup"><span data-stu-id="13c0b-201">However, the consolidation will only work if the dimension values in the business unit are the same as the consolidated company.</span></span>
  * <span data-ttu-id="13c0b-202">Para consolidar el código de valor de dimensión de la empresa con un código de valor de dimensión distinto en la empresa consolidada, rellene el campo **Código de consolidación** en las dimensiones relevantes.</span><span class="sxs-lookup"><span data-stu-id="13c0b-202">To consolidate the dimension value code in the business unit with a different dimension value code in the consolidated company, fill in the **Consolidation Code** field on the relevant dimensions.</span></span>  
* <span data-ttu-id="13c0b-203">Agregue las dimensiones relevantes a las cuentas de contabilidad relevantes</span><span class="sxs-lookup"><span data-stu-id="13c0b-203">Add the relevant dimensions to the relevant general ledger accounts</span></span>

### <a name="exclude-a-company-from-consolidation"></a><a name="exclude"></a><span data-ttu-id="13c0b-204">Excluir una empresa de la consolidación</span><span class="sxs-lookup"><span data-stu-id="13c0b-204">Exclude a company from consolidation</span></span>

<span data-ttu-id="13c0b-205">Si no desea incluir una unidad de negocio en la consolidación, puede excluirla.</span><span class="sxs-lookup"><span data-stu-id="13c0b-205">If you do not want to include a business unit in the consolidation, you can exclude it.</span></span> <span data-ttu-id="13c0b-206">Para hacerlo, vaya a la ficha de unidad de negocio y borre la casilla de verificación **Consolidar**.</span><span class="sxs-lookup"><span data-stu-id="13c0b-206">To do that, go to the business unit card, and clear the **Consolidate** check box.</span></span>

### <a name="include-a-partially-owned-company-in-consolidation"></a><a name="include"></a><span data-ttu-id="13c0b-207">Incluir una empresa poseída parcialmente en la consolidación</span><span class="sxs-lookup"><span data-stu-id="13c0b-207">Include a partially-owned company in consolidation</span></span>

<span data-ttu-id="13c0b-208">Si posee únicamente parte de una empresa, puede incluir un porcentaje de cada transacción que le corresponde al porcentaje de la empresa que le pertenece.</span><span class="sxs-lookup"><span data-stu-id="13c0b-208">If you own only part of a company, you can include a percentage of each transaction that corresponds to the percentage of the company you own.</span></span> <span data-ttu-id="13c0b-209">Por ejemplo, si le pertenece el 70% de la empresa, la consolidación incluirá $70 de una factura de $100.</span><span class="sxs-lookup"><span data-stu-id="13c0b-209">For example, if you own 70% of the company, consolidation will include $70 of an invoice for $100.</span></span> <span data-ttu-id="13c0b-210">Para especificar el porcentaje de la empresa que le pertenece, vaya a la ficha de la unidad de negocio e introduzca el porcentaje en el campo **Consolidación%**.</span><span class="sxs-lookup"><span data-stu-id="13c0b-210">To specify the percentage of the company you own, go to the business unit card, and enter the percentage in the **Consolidation %** field.</span></span>  

## <a name="see-also"></a><span data-ttu-id="13c0b-211">Consulte también</span><span class="sxs-lookup"><span data-stu-id="13c0b-211">See Also</span></span>

[<span data-ttu-id="13c0b-212">Consolidar los datos financieros de varias empresas</span><span class="sxs-lookup"><span data-stu-id="13c0b-212">Consolidating Financial Data from Multiple Companies</span></span>](finance-consolidated-company-reporting.md)  
[<span data-ttu-id="13c0b-213">Gestión de transacciones entre empresas vinculadas</span><span class="sxs-lookup"><span data-stu-id="13c0b-213">Managing Intercompany Transactions</span></span>](intercompany-manage.md)  
<span data-ttu-id="13c0b-214">[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="13c0b-214">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="13c0b-215">Exportar los datos de negocio a Excel</span><span class="sxs-lookup"><span data-stu-id="13c0b-215">Exporting Your Business Data to Excel</span></span>](about-export-data.md)