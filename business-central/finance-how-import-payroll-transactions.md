---
title: "Importar transacciones de nómina | Documentos de Microsoft"
description: "Para administrar los salarios, se importan y registran transacciones financieras desde el proveedor de nóminas a la contabilidad, mediante una extensión de nóminas como Ceridian o Quickbooks."
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Ceridian, Quickbooks, salary
ms.date: 10/01/2018
ms.author: SorenGP
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: fbe6a61cb48a4c26ff3fc15eb0dd61c002a59092
ms.contentlocale: es-es
ms.lasthandoff: 09/28/2018

---
# <a name="import-payroll-transactions"></a><span data-ttu-id="e7da2-103">Importar transacciones de nómina</span><span class="sxs-lookup"><span data-stu-id="e7da2-103">Import Payroll Transactions</span></span>
<span data-ttu-id="e7da2-104">Para contabilizar los pagos de salario y transacciones relacionadas, deberá importar y registrar las transacciones financieras de salario creadas para el proveedor de nóminas al libro mayor.</span><span class="sxs-lookup"><span data-stu-id="e7da2-104">To account for salary payments and related transactions, you must import and post financial transactions made by your payroll provider to the general ledger.</span></span> <span data-ttu-id="e7da2-105">Para hacer esto, primero importe un archivo que recibirá del proveedor de nóminas en la ventana **Diario general**.</span><span class="sxs-lookup"><span data-stu-id="e7da2-105">To do this, you first import a file that you receive from the payroll provider into the **General Journal** window.</span></span> <span data-ttu-id="e7da2-106">A continuación asigne las cuentas externas del archivo de nóminas a las cuentas correspondientes.</span><span class="sxs-lookup"><span data-stu-id="e7da2-106">Then you map the external accounts in the payroll file to the relevant G/L accounts.</span></span> <span data-ttu-id="e7da2-107">Por último, registre operaciones de nóminas según la asignación de cuentas.</span><span class="sxs-lookup"><span data-stu-id="e7da2-107">Lastly, you post the payroll transactions according to the account mapping.</span></span>

> [!NOTE]  
>   <span data-ttu-id="e7da2-108">Para utilizar esta funcionalidad, se debe instalar y habilitar la extensión para importar nóminas.</span><span class="sxs-lookup"><span data-stu-id="e7da2-108">To use this functionality, an extension for payroll import must be installed and enabled.</span></span> <span data-ttu-id="e7da2-109">Las extensiones Nómina de Ceridian e Importación del archivo de nómina de QuickBooks están preinstaladas en [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="e7da2-109">The Ceridian Payroll and the Quickbooks Payroll File Import extensions are pre-installed in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="e7da2-110">Para obtener más información, consulte [Personalizar [!INCLUDE[d365fin](includes/d365fin_md.md)] mediante extensiones](ui-extensions.md).</span><span class="sxs-lookup"><span data-stu-id="e7da2-110">For more information, see [Customizing [!INCLUDE[d365fin](includes/d365fin_md.md)] Using Extensions](ui-extensions.md).</span></span>

## <a name="to-import-a-payroll-file"></a><span data-ttu-id="e7da2-111">Para importar un archivo de nómina</span><span class="sxs-lookup"><span data-stu-id="e7da2-111">To import a payroll file</span></span>
1. <span data-ttu-id="e7da2-112">Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Diarios generales** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="e7da2-112">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **General Journals**, and then choose the related link.</span></span>
2. <span data-ttu-id="e7da2-113">En la sección del diario general correspondiente, elija la acción **Importar transacciones de nómina**.</span><span class="sxs-lookup"><span data-stu-id="e7da2-113">In the relevant general journal batch, choose the **Import Payroll Transactions** action.</span></span> <span data-ttu-id="e7da2-114">Se abre una guía de configuración asistida.</span><span class="sxs-lookup"><span data-stu-id="e7da2-114">An assisted setup guide opens.</span></span>
3. <span data-ttu-id="e7da2-115">Realice los pasos de la ventana **Importar transacciones de nómina**.</span><span class="sxs-lookup"><span data-stu-id="e7da2-115">Follow the steps in the **Import Payroll Transactions** window.</span></span>

    > [!TIP]  
    >   <span data-ttu-id="e7da2-116">En el paso de la asignación de los registros de nóminas externos a sus cuentas de contabilidad, las asignaciones que cree se recordarán la próxima vez que importe los mismos registros.</span><span class="sxs-lookup"><span data-stu-id="e7da2-116">In the step about mapping the external payroll records to your G/L accounts, the mappings that you make will be remembered next time the same records are imported.</span></span> <span data-ttu-id="e7da2-117">Esto le ahorrará tiempo al no tener que rellenar manualmente el campo **Número de cuenta** en el diario general cada vez que haya importado transacciones de nóminas periódicas.</span><span class="sxs-lookup"><span data-stu-id="e7da2-117">This will save you time as you do not have to manually fill in the **Account No.** field in the general journal every time you have imported recurring payroll transactions.</span></span>   

    <span data-ttu-id="e7da2-118">Cuando elige el botón **Aceptar** en la guía de configuración asistida, la ventana **Diario general** incluye las líneas que representan transacciones que contiene el archivo de nóminas y con las cuentas correspondientes rellenadas previamente en los campos **Cuentas G/L** según las asignaciones que ha creado en la guía.</span><span class="sxs-lookup"><span data-stu-id="e7da2-118">When you choose the **OK** button in the assisted setup guide, the **General Journal** window is filled with lines representing the transactions that the payroll file contains and with the relevant accounts prefilled in the **G/L Account** fields according to mappings you made in the guide.</span></span>
4. <span data-ttu-id="e7da2-119">Edite o registre las líneas de diario como cualquier otra transacción de contabilidad.</span><span class="sxs-lookup"><span data-stu-id="e7da2-119">Edit or post the journal lines as for any other general ledger transactions.</span></span> <span data-ttu-id="e7da2-120">Para obtener más información, consulte [Registrar transacciones directamente en la contabilidad](finance-how-post-transactions-directly.md).</span><span class="sxs-lookup"><span data-stu-id="e7da2-120">For more information, see [Post Transactions Directly to the General Ledger](finance-how-post-transactions-directly.md).</span></span>   

## <a name="see-also"></a><span data-ttu-id="e7da2-121">Consulte también</span><span class="sxs-lookup"><span data-stu-id="e7da2-121">See Also</span></span>
[<span data-ttu-id="e7da2-122">Finanzas</span><span class="sxs-lookup"><span data-stu-id="e7da2-122">Finance</span></span>](finance.md)  
<span data-ttu-id="e7da2-123">[Personalizar [!INCLUDE[d365fin](includes/d365fin_md.md)] con extensiones](ui-extensions.md)</span><span class="sxs-lookup"><span data-stu-id="e7da2-123">[Customizing [!INCLUDE[d365fin](includes/d365fin_md.md)] Using Extensions](ui-extensions.md)</span></span>  
[<span data-ttu-id="e7da2-124">Trabajar con diarios generales</span><span class="sxs-lookup"><span data-stu-id="e7da2-124">Working with General Journals</span></span>](ui-work-general-journals.md)  

