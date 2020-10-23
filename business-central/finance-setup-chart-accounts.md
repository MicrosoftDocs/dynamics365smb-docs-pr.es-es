---
title: Configurar un plan contable
description: Puede cambiar las cuentas predeterminadas en el plan de cuentas (COA) y puede agregar nuevas cuentas.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: COA, cha of acc
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: cb588d67976a0eb6eee9cac9c66672ac3dd06c69
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/01/2020
ms.locfileid: "3923004"
---
# <a name="setting-up-or-changing-the-chart-of-accounts"></a><span data-ttu-id="72e2d-103">Configurar o cambiar el plan de cuentas</span><span class="sxs-lookup"><span data-stu-id="72e2d-103">Setting Up or Changing the Chart of Accounts</span></span>
<span data-ttu-id="72e2d-104">El plan de cuentas muestra las cuentas de contabilidad que almacenan sus datos financieros.</span><span class="sxs-lookup"><span data-stu-id="72e2d-104">The chart of accounts shows the ledger accounts that store your financial data.</span></span> [!INCLUDE[d365fin](includes/d365fin_md.md)] <span data-ttu-id="72e2d-105">incluye un gráfico estándar de cuentas que está preparado para respaldar su negocio.</span><span class="sxs-lookup"><span data-stu-id="72e2d-105">includes a standard chart of accounts that is ready to support your business.</span></span>
<span data-ttu-id="72e2d-106">Sin embargo, puede cambiar las cuentas predeterminadas y puede agregar nuevas cuentas.</span><span class="sxs-lookup"><span data-stu-id="72e2d-106">However, you can change the default accounts, and you can add new accounts.</span></span>
<br><br>  

> [!Video https://www.microsoft.com/videoplayer/embed/RE43KO9?rel=0]


## <a name="adding-or-changing-accounts"></a><span data-ttu-id="72e2d-107">Agregar o cambiar cuentas</span><span class="sxs-lookup"><span data-stu-id="72e2d-107">Adding or Changing Accounts</span></span>
<span data-ttu-id="72e2d-108">Desde el plan de cuentas, puede abrir cada cuenta de contabilidad y agregar o cambiar la configuración.</span><span class="sxs-lookup"><span data-stu-id="72e2d-108">From the chart of accounts, you can open each G/L account and add or change settings.</span></span>

> [!NOTE]  
>   <span data-ttu-id="72e2d-109">Puede eliminar una cuenta contable.</span><span class="sxs-lookup"><span data-stu-id="72e2d-109">You can delete a general ledger account.</span></span> <span data-ttu-id="72e2d-110">Sin embargo, antes de eliminarla, deben cumplirse las condiciones siguientes:</span><span class="sxs-lookup"><span data-stu-id="72e2d-110">However, before you delete it, the following must be true:</span></span>  
>  
>   * <span data-ttu-id="72e2d-111">El saldo de la cuenta debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="72e2d-111">The balance on the account must be zero.</span></span>  
>   * <span data-ttu-id="72e2d-112">El campo **Permite borrar ctas. anteriores a** se debe configurar en la página **Configuración de contabilidad** y la cuenta no debe tener movimientos contables en o después de esa fecha.</span><span class="sxs-lookup"><span data-stu-id="72e2d-112">The **Allow G/L Acc. Deletion Before** field must be set on the **General Ledger Setup** page, and the account must not have ledger entries on or after that date.</span></span>  
>   * <span data-ttu-id="72e2d-113">Si se selecciona el campo **Chequear uso ctas. cont.** en la página **Configuración de contabilidad**, la cuenta no se debe usar en grupos contables ni en la configuración de grupos contables.</span><span class="sxs-lookup"><span data-stu-id="72e2d-113">If the **Check G/L Account Usage** field on the **General Ledger Setup** page is selected, then the account must not be used in any posting groups or posting setup.</span></span>  

[!INCLUDE[d365fin](includes/d365fin_md.md)] <span data-ttu-id="72e2d-114">impedirá que elimine una cuenta de contabilidad que guarde los datos que se necesitan en el plan de cuentas.</span><span class="sxs-lookup"><span data-stu-id="72e2d-114">will prevent you from deleting a general ledger account that stores data that is needed in the chart of accounts.</span></span>  

## <a name="see-related-training-at-microsoft-learn"></a><span data-ttu-id="72e2d-115">Consulte Formación relacionada en [Microsoft Learn](/learn/modules/chart-accounts-dynamics-365-business-central/index)</span><span class="sxs-lookup"><span data-stu-id="72e2d-115">See Related Training at [Microsoft Learn](/learn/modules/chart-accounts-dynamics-365-business-central/index)</span></span>

## <a name="see-also"></a><span data-ttu-id="72e2d-116">Consulte también</span><span class="sxs-lookup"><span data-stu-id="72e2d-116">See Also</span></span>
[<span data-ttu-id="72e2d-117">Libro mayor y plan de cuentas</span><span class="sxs-lookup"><span data-stu-id="72e2d-117">The General Ledger and the Chart of Accounts</span></span>](finance-general-ledger.md)  
[<span data-ttu-id="72e2d-118">Conciliar bancos</span><span class="sxs-lookup"><span data-stu-id="72e2d-118">Reconciling Bank Accounts</span></span>](bank-manage-bank-accounts.md)  
[<span data-ttu-id="72e2d-119">Trabajar con dimensiones</span><span class="sxs-lookup"><span data-stu-id="72e2d-119">Working with Dimensions</span></span>](finance-dimensions.md)  
[<span data-ttu-id="72e2d-120">Importar datos de otros sistemas financieros</span><span class="sxs-lookup"><span data-stu-id="72e2d-120">Importing Data from Other Finance Systems</span></span>](across-import-data-configuration-packages.md)  
[<span data-ttu-id="72e2d-121">Trabajar con esquemas de cuentas</span><span class="sxs-lookup"><span data-stu-id="72e2d-121">Work with Account Schedules</span></span>](bi-how-work-account-schedule.md)  
<span data-ttu-id="72e2d-122">[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="72e2d-122">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]
