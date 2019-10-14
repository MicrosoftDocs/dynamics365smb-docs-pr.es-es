---
title: Configurar clientes de efectivo | Documentos de Microsoft
description: En este tema se describen los pasos para configurar al cliente que paga en efectivo.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 853784f676ea986cc11754bb5cb006b57d5e72ce
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/01/2019
ms.locfileid: "2306009"
---
# <a name="set-up-cash-customers"></a><span data-ttu-id="057fa-103">Configurar clientes de efectivo</span><span class="sxs-lookup"><span data-stu-id="057fa-103">Set Up Cash Customers</span></span>
<span data-ttu-id="057fa-104">No se puede crear una factura sin un número de cliente.</span><span class="sxs-lookup"><span data-stu-id="057fa-104">You cannot create an invoice without a customer number.</span></span> <span data-ttu-id="057fa-105">Esto es válido, incluso si realiza una venta en efectivo y no tiene nada que registrar en una cuenta de cliente.</span><span class="sxs-lookup"><span data-stu-id="057fa-105">This is true, even if you make a cash sale and do not have anything to record in a customer account.</span></span>  

## <a name="to-set-up-a-cash-customer"></a><span data-ttu-id="057fa-106">Para configurar un cliente de efectivo</span><span class="sxs-lookup"><span data-stu-id="057fa-106">To set up a cash customer</span></span>  
1.  <span data-ttu-id="057fa-107">Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Cliente** y luego elija el enlace relacionado.</span><span class="sxs-lookup"><span data-stu-id="057fa-107">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Customer**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="057fa-108">Cree una ficha **Cliente** nueva.</span><span class="sxs-lookup"><span data-stu-id="057fa-108">Create a new **Customer** card.</span></span> <span data-ttu-id="057fa-109">Para obtener más información, vea [Registrar nuevos clientes](sales-how-register-new-customers.md).</span><span class="sxs-lookup"><span data-stu-id="057fa-109">For more information, see [Register New Customers](sales-how-register-new-customers.md).</span></span>
3.  <span data-ttu-id="057fa-110">En el campo **N.º**,</span><span class="sxs-lookup"><span data-stu-id="057fa-110">In the **No.**</span></span> <span data-ttu-id="057fa-111">introduzca, por ejemplo, **Efectivo**.</span><span class="sxs-lookup"><span data-stu-id="057fa-111">field, enter **Cash**, for example.</span></span>  
4.  <span data-ttu-id="057fa-112">En el campo **Nombre**, escriba **Venta en efectivo**.</span><span class="sxs-lookup"><span data-stu-id="057fa-112">In the **Name** field, enter **Cash Sale**, for example.</span></span>  
5.  <span data-ttu-id="057fa-113">En la ficha desplegable **Facturación**, rellene los campos **Grupo contable cliente** y **Grupo contable negocio**.</span><span class="sxs-lookup"><span data-stu-id="057fa-113">On the **Invoicing** FastTab, fill in the **Customer Posting Group** and the **Gen. Bus. Posting Group** fields.</span></span>  

 <span data-ttu-id="057fa-114">Ya ha configurado un cliente que contiene suficiente información para facturarle.</span><span class="sxs-lookup"><span data-stu-id="057fa-114">Now you have set up a customer that contains sufficient information for invoicing.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="057fa-115">Quizá haya elegido un grupo contable que se utilice también para las ventas a crédito nacionales.</span><span class="sxs-lookup"><span data-stu-id="057fa-115">You may have chosen a posting group that is also used for domestic credit sales.</span></span> <span data-ttu-id="057fa-116">Si desea mantener datos por separado sobre ventas en efectivo, por ejemplo, con una cuenta de cliente o venta especial, configure un grupo contable adicional para ello.</span><span class="sxs-lookup"><span data-stu-id="057fa-116">If you want to maintain separate data on cash sales, for example, with a special sales or receivables account, you can set up an extra posting group for this purpose.</span></span>  
>   
>  <span data-ttu-id="057fa-117">Especifique un número de cuenta de cliente para dicho grupo contable, aunque el saldo de la cuenta quede siempre a 0 después de registrar una factura.</span><span class="sxs-lookup"><span data-stu-id="057fa-117">You must enter a number for a receivables account for the posting group, even though the balance in this account will always be 0 after you post an invoice.</span></span>  

## <a name="see-also"></a><span data-ttu-id="057fa-118">Consulte también</span><span class="sxs-lookup"><span data-stu-id="057fa-118">See Also</span></span>
[<span data-ttu-id="057fa-119">Administrar cobros</span><span class="sxs-lookup"><span data-stu-id="057fa-119">Managing Receivables</span></span>](receivables-manage-receivables.md)  
<span data-ttu-id="057fa-120">[Permite registrar nuevos clientes](sales-how-register-new-customers.md)  </span><span class="sxs-lookup"><span data-stu-id="057fa-120">[Register New Customers](sales-how-register-new-customers.md)  </span></span>  
[<span data-ttu-id="057fa-121">Finanzas</span><span class="sxs-lookup"><span data-stu-id="057fa-121">Finance</span></span>](finance.md)  

