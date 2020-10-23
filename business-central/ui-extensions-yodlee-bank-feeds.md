---
title: Conciliación de pagos con la extensión Envestnet Yodlee Bank Feeds | Documentos de Microsoft
description: Describe la extensión Envestnet Yodlee Bank Feeds, que se vincula a las cuentas bancarias para que pueda conciliar pagos rápidamente.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: app, add-in, manifest, customize, stream, bank account link
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 3107c42fd584a58fc13ad2bfeacea0ed14e28de7
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/01/2020
ms.locfileid: "3918593"
---
# <a name="the-envestnet-yodlee-bank-feeds-extension"></a><span data-ttu-id="aaea1-103">Extensión Envestnet Yodlee Bank Feeds</span><span class="sxs-lookup"><span data-stu-id="aaea1-103">The Envestnet Yodlee Bank Feeds Extension</span></span>
<span data-ttu-id="aaea1-104">Para conciliar pagos realizados en sus bancos rápidamente, el servicio Envestnet Yodlee Bank Feeds permite vincular su cuenta bancaria del sistema a su cuenta bancaria en línea.</span><span class="sxs-lookup"><span data-stu-id="aaea1-104">To quickly reconcile payments made to your bank accounts, the Envestnet Yodlee Bank Feeds service allows you to link your system bank account to your online bank account.</span></span> <span data-ttu-id="aaea1-105">Esto significa que el último extracto bancario se introduce manual o automáticamente en el diario de conciliación de pagos, lo que garantiza que siempre procesará sus últimos pagos con el mínimo de errores.</span><span class="sxs-lookup"><span data-stu-id="aaea1-105">This means that the latest bank statement is automatically or manually fed into your reconciliation journal, ensuring that you are always processing the latest payments with minimal risk of errors.</span></span>

<span data-ttu-id="aaea1-106">El servicio Envestnet Yodlee Bank Feeds solo se admite en Estados Unidos y Canadá.</span><span class="sxs-lookup"><span data-stu-id="aaea1-106">The Envestnet Yodlee Bank Feeds service is only supported in the United States and Canada.</span></span>

> [!NOTE]
> <span data-ttu-id="aaea1-107">El servicio Envestnet Yodlee Bank Feeds solo se admite en la versión en línea de Business Central.</span><span class="sxs-lookup"><span data-stu-id="aaea1-107">The Envestnet Yodlee Bank Feeds service is only supported in the online version of Business Central.</span></span> <span data-ttu-id="aaea1-108">Para utilizar esta funcionalidad local, debe obtener una cuenta de cobrand de Envestnet Yodlee.</span><span class="sxs-lookup"><span data-stu-id="aaea1-108">To use this functionality on-premises, you must obtain a cobrand account from Envestnet Yodlee.</span></span><br /><br />
> <span data-ttu-id="aaea1-109">El servicio Envestnet Yodlee Bank Feeds solo se admite en Estados Unidos y Canadá.</span><span class="sxs-lookup"><span data-stu-id="aaea1-109">The Envestnet Yodlee Bank Feeds service is only supported in the United States and Canada.</span></span>
> <span data-ttu-id="aaea1-110">Solo se admiten los bancos que residan en estos países o regiones, aunque los bancos de otros países o regiones puedan aparecer en la ventana de selección de banco de Envestnet Yodlee Bank Feeds en [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="aaea1-110">Only banks residing in these countries are supported, even though banks from other countries may appear in the Envestnet Yodlee Bank Feeds bank selection window in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>

> [!IMPORTANT]
> <span data-ttu-id="aaea1-111">Debido a la nueva directiva sobre servicios de pago en Europa (PSD2), después del 14 de septiembre de 2019 ya no podrá importar automáticamente extractos de cuenta de bancos del Reino Unido a [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="aaea1-111">Due to the new Payment Services Directive in Europe (PSD2), after September 14, 2019, you will no longer be able to automatically import bank statements from banks in the United Kingdom into [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="aaea1-112">Estamos analizando la posibilidad de ofrecer esta función nuevamente en el futuro.</span><span class="sxs-lookup"><span data-stu-id="aaea1-112">We are looking into the possibility of offering this feature again in the future.</span></span>

<span data-ttu-id="aaea1-113">El servicio Envestnet Yodlee Bank Feeds proporciona las siguientes ventajas:</span><span class="sxs-lookup"><span data-stu-id="aaea1-113">The Envestnet Yodlee Bank Feeds service provides the following benefits:</span></span>

* <span data-ttu-id="aaea1-114">Elimina la necesidad de la entrada manual.</span><span class="sxs-lookup"><span data-stu-id="aaea1-114">Removes the need for manual entry.</span></span>
* <span data-ttu-id="aaea1-115">Actualiza la eficacia y la precisión al realizar la conciliación de pagos.</span><span class="sxs-lookup"><span data-stu-id="aaea1-115">Improves efficiency and accuracy when doing payment reconciliation.</span></span>
* <span data-ttu-id="aaea1-116">Admite un gran número de bancos.</span><span class="sxs-lookup"><span data-stu-id="aaea1-116">Supports a large number of banks.</span></span>
* <span data-ttu-id="aaea1-117">Permite información actualizada sobre transacciones bancarias en [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="aaea1-117">Allows up-to-date information about bank transactions from within [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>
* <span data-ttu-id="aaea1-118">Admite fuentes de banco manuales o automáticas.</span><span class="sxs-lookup"><span data-stu-id="aaea1-118">Supports manual as well as automatic bank feeds.</span></span>
* <span data-ttu-id="aaea1-119">Habilita la externalización de la conciliación de pagos a un contable proporcionando acceso a los extractos bancarios.</span><span class="sxs-lookup"><span data-stu-id="aaea1-119">Enables outsourcing of payment reconciliation to an accountant by providing access to bank statements.</span></span>

## <a name="available-bank-feeds"></a><span data-ttu-id="aaea1-120">Fuentes de banco disponibles</span><span class="sxs-lookup"><span data-stu-id="aaea1-120">Available Bank Feeds</span></span>
<span data-ttu-id="aaea1-121">Puede comprobar si un banco es compatible configurando y conectándose al servicio Envestnet Yodlee Bank Feeds.</span><span class="sxs-lookup"><span data-stu-id="aaea1-121">You can check whether a bank is supported by setting up and connecting to the Envestnet Yodlee Bank Feeds service.</span></span> <span data-ttu-id="aaea1-122">El banco aparecerá en la lista si es compatible con Envestnet Yodlee.</span><span class="sxs-lookup"><span data-stu-id="aaea1-122">The bank will appear on the list if it is supported by Envestnet Yodlee.</span></span>

<span data-ttu-id="aaea1-123">Para obtener más información, vea [Configurar el servicio Envestnet Yodlee Bank Feeds](bank-how-setup-bank-statement-service.md).</span><span class="sxs-lookup"><span data-stu-id="aaea1-123">For more information, see [Set Up the Envestnet Yodlee Bank Feeds Service](bank-how-setup-bank-statement-service.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="aaea1-124">Consulte también</span><span class="sxs-lookup"><span data-stu-id="aaea1-124">See Also</span></span>
<span data-ttu-id="aaea1-125">[Personalizar [!INCLUDE[d365fin](includes/d365fin_md.md)] con extensiones ](ui-extensions.md)  </span><span class="sxs-lookup"><span data-stu-id="aaea1-125">[Customizing [!INCLUDE[d365fin](includes/d365fin_md.md)] Using Extensions ](ui-extensions.md)  </span></span>  
[<span data-ttu-id="aaea1-126">Liquidación de pagos automáticamente y conciliación de cuentas bancarias</span><span class="sxs-lookup"><span data-stu-id="aaea1-126">Applying Payments Automatically and Reconciling Bank Accounts</span></span>](receivables-apply-payments-auto-reconcile-bank-accounts.md)  
<span data-ttu-id="aaea1-127">[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="aaea1-127">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
