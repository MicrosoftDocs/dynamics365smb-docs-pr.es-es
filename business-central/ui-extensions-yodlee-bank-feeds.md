---
title: Conciliación de pagos con la extensión de las fuentes de banco de Envestnet Yodlee | Documentos de Microsoft
description: Describe la extensión de las fuentes de banco de Envestnet Yodlee, que se vincula a las cuentas bancarias para que pueda conciliar pagos rápidamente.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: app, add-in, manifest, customize, stream, bank account link
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: 53ee8bb7ee798c473e1053ea8413be28f9185d1b
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 03/31/2019
ms.locfileid: "911724"
---
# <a name="the-envestnet-yodlee-bank-feeds-extension"></a><span data-ttu-id="fe887-103">Extensión de las fuentes de banco de Envestnet Yodlee</span><span class="sxs-lookup"><span data-stu-id="fe887-103">The Envestnet Yodlee Bank Feeds Extension</span></span>
<span data-ttu-id="fe887-104">Para conciliar pagos realizados en sus cuentas bancarias rápidamente, el servicio de fuentes de banco de Envestnet Yodlee permite vincular su cuenta bancaria del sistema a su cuenta bancaria en línea.</span><span class="sxs-lookup"><span data-stu-id="fe887-104">To quickly reconcile payments made to your bank accounts, the Envestnet Yodlee Bank Feeds service allows you to link your system bank account to your online bank account.</span></span> <span data-ttu-id="fe887-105">Esto significa que el último extracto bancario se introduce manual o automáticamente en el diario de conciliación de pagos, lo que garantiza que siempre procesará sus últimos pagos con el mínimo de errores.</span><span class="sxs-lookup"><span data-stu-id="fe887-105">This means that the latest bank statement is automatically or manually fed into your reconciliation journal, ensuring that you are always processing the latest payments with minimal risk of errors.</span></span>

> [!NOTE]
> <span data-ttu-id="fe887-106">Esta funcionalidad solo se admite en la versión en línea de Business Central.</span><span class="sxs-lookup"><span data-stu-id="fe887-106">This functionality is only supported in the online version of Business Central.</span></span> <span data-ttu-id="fe887-107">Para utilizar esta funcionalidad local, debe obtener una cuenta de cobrand de Envestnet Yodlee.</span><span class="sxs-lookup"><span data-stu-id="fe887-107">To use this functionality on-premise, you must obtain a cobrand account from Envestnet Yodlee.</span></span>

<span data-ttu-id="fe887-108">El servicio de fuentes de banco de Envestnet Yodlee proporciona las ventajas siguientes:</span><span class="sxs-lookup"><span data-stu-id="fe887-108">The Envestnet Yodlee Bank Feeds service provides the following benefits:</span></span>

* <span data-ttu-id="fe887-109">Elimina la necesidad de la entrada manual.</span><span class="sxs-lookup"><span data-stu-id="fe887-109">Removes the need for manual entry.</span></span>
* <span data-ttu-id="fe887-110">Actualiza la eficacia y la precisión al realizar la conciliación de pagos.</span><span class="sxs-lookup"><span data-stu-id="fe887-110">Improves efficiency and accuracy when doing payment reconciliation.</span></span>
* <span data-ttu-id="fe887-111">Admite un gran número de bancos.</span><span class="sxs-lookup"><span data-stu-id="fe887-111">Supports a large number of banks.</span></span>
* <span data-ttu-id="fe887-112">Permite información actualizada sobre transacciones bancarias en [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="fe887-112">Allows up-to-date information about bank transactions from within [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>
* <span data-ttu-id="fe887-113">Admite fuentes de banco manuales o automáticas.</span><span class="sxs-lookup"><span data-stu-id="fe887-113">Supports manual as well as automatic bank feeds.</span></span>
* <span data-ttu-id="fe887-114">Habilita la externalización de la conciliación de pagos a un contable proporcionando acceso a los extractos bancarios.</span><span class="sxs-lookup"><span data-stu-id="fe887-114">Enables outsourcing of payment reconciliation to an accountant by providing access to bank statements.</span></span>

<span data-ttu-id="fe887-115">Para obtener más información, vea [Configuración del servicio de fuente de banco de Envestnet Yodlee](bank-how-setup-bank-statement-service.md)</span><span class="sxs-lookup"><span data-stu-id="fe887-115">For more information, see [Set Up the Envestnet Yodlee Bank Feeds Service](bank-how-setup-bank-statement-service.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="fe887-116">Consulte también</span><span class="sxs-lookup"><span data-stu-id="fe887-116">See Also</span></span>
<span data-ttu-id="fe887-117">[Personalizar [!INCLUDE[d365fin](includes/d365fin_md.md)] con extensiones ](ui-extensions.md)  </span><span class="sxs-lookup"><span data-stu-id="fe887-117">[Customizing [!INCLUDE[d365fin](includes/d365fin_md.md)] Using Extensions ](ui-extensions.md)  </span></span>  
[<span data-ttu-id="fe887-118">Liquidación de pagos automáticamente y conciliación de cuentas bancarias</span><span class="sxs-lookup"><span data-stu-id="fe887-118">Applying Payments Automatically and Reconciling Bank Accounts</span></span>](receivables-apply-payments-auto-reconcile-bank-accounts.md)  
<span data-ttu-id="fe887-119">[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="fe887-119">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
