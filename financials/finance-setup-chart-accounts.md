---
title: Configurar el plan de cuentas | Documentos de Microsoft
description: Puede cambiar las cuentas predeterminadas en el plan de cuentas (COA) y puede agregar nuevas cuentas.
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: COA, cha of acc
ms.date: 06/02/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 69d4a8d4482999ed9d622d73654c3d8a4c3d8394
ms.contentlocale: es-es
ms.lasthandoff: 09/22/2017

---
# <a name="setting-up-or-changing-the-chart-of-accounts"></a><span data-ttu-id="b9078-103">Configurar o cambiar el plan de cuentas</span><span class="sxs-lookup"><span data-stu-id="b9078-103">Setting Up or Changing the Chart of Accounts</span></span>
<span data-ttu-id="b9078-104">El plan de cuentas muestra las cuentas de contabilidad que almacenan sus datos financieros.</span><span class="sxs-lookup"><span data-stu-id="b9078-104">The chart of accounts shows the ledger accounts that store your financial data.</span></span> [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]<span data-ttu-id="b9078-105"> incluye un gráfico estándar de cuentas que está preparado para respaldar su negocio.</span><span class="sxs-lookup"><span data-stu-id="b9078-105"> includes a standard chart of accounts that is ready to support your business.</span></span>
<span data-ttu-id="b9078-106">Sin embargo, puede cambiar las cuentas predeterminadas y puede agregar nuevas cuentas.</span><span class="sxs-lookup"><span data-stu-id="b9078-106">However, you can change the default accounts, and you can add new accounts.</span></span>  

## <a name="adding-or-changing-accounts"></a><span data-ttu-id="b9078-107">Agregar o cambiar cuentas</span><span class="sxs-lookup"><span data-stu-id="b9078-107">Adding or Changing Accounts</span></span>
<span data-ttu-id="b9078-108">Desde el plan de cuentas, puede abrir cada cuenta de contabilidad y agregar o cambiar la configuración.</span><span class="sxs-lookup"><span data-stu-id="b9078-108">From the chart of accounts, you can open each G/L account and add or change settings.</span></span>

> [!NOTE]  
>   <span data-ttu-id="b9078-109">Puede eliminar una cuenta contable.</span><span class="sxs-lookup"><span data-stu-id="b9078-109">You can delete a general ledger account.</span></span> <span data-ttu-id="b9078-110">Sin embargo, antes de eliminarla, deben cumplirse las condiciones siguientes:</span><span class="sxs-lookup"><span data-stu-id="b9078-110">However, before you delete it, the following must be true:</span></span>  

* <span data-ttu-id="b9078-111">El saldo de la cuenta debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="b9078-111">The balance on the account must be zero.</span></span>  
* <span data-ttu-id="b9078-112">El campo **Permite borrar ctas. anteriores a** se debe configurar en la ventana **Configuración de contabilidad** y la cuenta no debe tener movimientos contables en o después de esa fecha.</span><span class="sxs-lookup"><span data-stu-id="b9078-112">The **Allow G/L Acc. Deletion Before** field must be set in the **General Ledger Setup** window, and the account must not have ledger entries on or after that date.</span></span>  
* <span data-ttu-id="b9078-113">Si se selecciona el campo **Chequear uso ctas. cont.** en la ventana **Configuración de contabilidad**, la cuenta no se debe usar en grupos contables ni en la configuración de grupos contables.</span><span class="sxs-lookup"><span data-stu-id="b9078-113">If the **Check G/L Account Usage** field in the **General Ledger Setup** window is selected, then the account must not be used in any posting groups or posting setup.</span></span>  

[!INCLUDE[d365fin](includes/d365fin_md.md)]<span data-ttu-id="b9078-114"> impedirá que elimine una cuenta de contabilidad que guarde los datos que se necesitan en el plan de cuentas.</span><span class="sxs-lookup"><span data-stu-id="b9078-114"> will prevent you from deleting a general ledger account that stores data that is needed in the chart of accounts.</span></span>  

## <a name="see-also"></a><span data-ttu-id="b9078-115">Consulte también</span><span class="sxs-lookup"><span data-stu-id="b9078-115">See Also</span></span>
[<span data-ttu-id="b9078-116">Libro mayor y plan de cuentas</span><span class="sxs-lookup"><span data-stu-id="b9078-116">The General Ledger and the Chart of Accounts</span></span>](finance-general-ledger.md)  
[<span data-ttu-id="b9078-117">Administrar cuentas bancarias</span><span class="sxs-lookup"><span data-stu-id="b9078-117">Managing Bank Accounts</span></span>](bank-manage-bank-accounts.md)  
[<span data-ttu-id="b9078-118">Trabajar con dimensiones</span><span class="sxs-lookup"><span data-stu-id="b9078-118">Working with Dimensions</span></span>](finance-dimensions.md)  
[<span data-ttu-id="b9078-119">Importar desde otros sistemas financieros</span><span class="sxs-lookup"><span data-stu-id="b9078-119">Importing from Other Finance Systems</span></span>](upload-data.md)  
<span data-ttu-id="b9078-120">[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="b9078-120">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]

