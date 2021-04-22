---
title: Pagos electrónicos – AEB N34.1
description: Con la funcionalidad de pagos electrónicos, puede pagar a los proveedores mediante pagos electrónicos en lugar de tener que emitir cheques en papel. Los pagos electrónicos se exportan a un formato de archivo AEB N34.1 estándar, utilizado por casi todos los bancos en España.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 408fef3f30fb02ed8a515d1fe29fe0cb83db29a0
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 03/31/2021
ms.locfileid: "5788218"
---
# <a name="electronic-payments--aeb-n341"></a><span data-ttu-id="3fe6f-104">Pagos electrónicos – AEB N34.1</span><span class="sxs-lookup"><span data-stu-id="3fe6f-104">Electronic Payments – AEB N34.1</span></span>
<span data-ttu-id="3fe6f-105">Con la funcionalidad de pagos electrónicos, puede pagar a los proveedores mediante pagos electrónicos en lugar de tener que emitir cheques en papel.</span><span class="sxs-lookup"><span data-stu-id="3fe6f-105">With the electronic payments functionality, you can pay vendors using electronic payments rather than printing paper checks.</span></span> <span data-ttu-id="3fe6f-106">Los pagos electrónicos se exportan a un formato de archivo AEB N34.1 estándar, utilizado por casi todos los bancos en España.</span><span class="sxs-lookup"><span data-stu-id="3fe6f-106">Electronic payments are exported into a standard AEB N34.1 file format used by most banks in Spain.</span></span> <span data-ttu-id="3fe6f-107">Posteriormente, este archivo se transmite al banco.</span><span class="sxs-lookup"><span data-stu-id="3fe6f-107">This file is then transmitted to your bank.</span></span>  

<span data-ttu-id="3fe6f-108">Podrá crear pagos electrónicos desde los diarios de pagos o desde la funcionalidad Cartera (lista de informes).</span><span class="sxs-lookup"><span data-stu-id="3fe6f-108">You can create electronic payments from the payment journals or from the Cartera functionality (report list).</span></span> <span data-ttu-id="3fe6f-109">Su objetivo es ocuparse de los casos siguientes:</span><span class="sxs-lookup"><span data-stu-id="3fe6f-109">This is intended to cover the following cases:</span></span>  

- <span data-ttu-id="3fe6f-110">Facturas y documentos de cartera abiertos y no agrupados.</span><span class="sxs-lookup"><span data-stu-id="3fe6f-110">Invoices and open, non-grouped Cartera documents.</span></span> <span data-ttu-id="3fe6f-111">Si decide pagar mediante pagos electrónicos, el archivo de pago se genera desde el informe **Exportar pagos electrónicos**.</span><span class="sxs-lookup"><span data-stu-id="3fe6f-111">If you select to pay using electronic payments, then the payment file is generated from the **Export Electronic Payments** report.</span></span>  

- <span data-ttu-id="3fe6f-112">Facturas y documentos de cartera agrupados en una orden de pago.</span><span class="sxs-lookup"><span data-stu-id="3fe6f-112">Invoices and Cartera documents that are grouped in a payment order.</span></span> <span data-ttu-id="3fe6f-113">Si decide pagar mediante pagos electrónicos, el archivo de pago se genera desde el informe **Orden pago - Exportar N34.1**, disponible en la lista de informes de cartera.</span><span class="sxs-lookup"><span data-stu-id="3fe6f-113">If you select to pay using electronic payments, the payment file is generated from the **PO - Export N34.1** report, available in the Cartera report list.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="3fe6f-114">Los socios pueden tener que modificar este informe para satisfacer los requisitos concretos del banco de su cliente.</span><span class="sxs-lookup"><span data-stu-id="3fe6f-114">Partners may need to modify this report to meet their customer’s bank individual requirements.</span></span>  

<span data-ttu-id="3fe6f-115">Para poder hacer transferencias de pago electrónicas a un proveedor, tendrá que configurar una cuenta de banco para el proveedor.</span><span class="sxs-lookup"><span data-stu-id="3fe6f-115">Before you can transfer payments electronically to a vendor, you will need to set up a bank account for the vendor.</span></span> <span data-ttu-id="3fe6f-116">También tendrá que configurar los vínculos de pagos electrónicos con el banco y la ficha de cuenta de banco en [!INCLUDE[prod_short](../../includes/prod_short.md)] para que su propio banco controle los pagos electrónicos.</span><span class="sxs-lookup"><span data-stu-id="3fe6f-116">You will also need to set up the electronic payment links with your bank and set up the bank account card in [!INCLUDE[prod_short](../../includes/prod_short.md)] for your own bank to handle the electronic payments.</span></span> <span data-ttu-id="3fe6f-117">El banco debe proporcionar el programa de transmisión.</span><span class="sxs-lookup"><span data-stu-id="3fe6f-117">The bank should provide the transmission program.</span></span>  

## <a name="see-also"></a><span data-ttu-id="3fe6f-118">Consulte también</span><span class="sxs-lookup"><span data-stu-id="3fe6f-118">See Also</span></span>  
 <span data-ttu-id="3fe6f-119">[Configurar cuentas bancarias para realizar pagos electrónicos](how-to-set-up-bank-accounts-for-electronic-payments.md) </span><span class="sxs-lookup"><span data-stu-id="3fe6f-119">[Set Up Bank Accounts for Electronic Payments](how-to-set-up-bank-accounts-for-electronic-payments.md) </span></span>  
 [<span data-ttu-id="3fe6f-120">Pagar a los proveedores mediante pagos electrónicos</span><span class="sxs-lookup"><span data-stu-id="3fe6f-120">Pay Vendors by Using Electronic Payments</span></span>](how-to-pay-vendors-by-using-electronic-payments.md) 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]