---
title: Pagos electrónicos – AEB N34.1
description: Con la funcionalidad de pagos electrónicos, puede pagar a los proveedores mediante pagos electrónicos en lugar de tener que emitir cheques en papel. Los pagos electrónicos se exportan a un formato de archivo AEB N34.1 estándar, utilizado por casi todos los bancos en España. Posteriormente, este archivo se transmite al banco.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: dd47e677b0fef1efed1d1d23bf5e4cd5f6cfb30f
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 03/31/2019
ms.locfileid: "911952"
---
# <a name="electronic-payments--aeb-n341"></a><span data-ttu-id="2e820-105">Pagos electrónicos – AEB N34.1</span><span class="sxs-lookup"><span data-stu-id="2e820-105">Electronic Payments – AEB N34.1</span></span>
<span data-ttu-id="2e820-106">Con la funcionalidad de pagos electrónicos, puede pagar a los proveedores mediante pagos electrónicos en lugar de tener que emitir cheques en papel.</span><span class="sxs-lookup"><span data-stu-id="2e820-106">With the electronic payments functionality, you can pay vendors using electronic payments rather than printing paper checks.</span></span> <span data-ttu-id="2e820-107">Los pagos electrónicos se exportan a un formato de archivo AEB N34.1 estándar, utilizado por casi todos los bancos en España.</span><span class="sxs-lookup"><span data-stu-id="2e820-107">Electronic payments are exported into a standard AEB N34.1 file format used by most banks in Spain.</span></span> <span data-ttu-id="2e820-108">Posteriormente, este archivo se transmite al banco.</span><span class="sxs-lookup"><span data-stu-id="2e820-108">This file is then transmitted to your bank.</span></span>  
  
 <span data-ttu-id="2e820-109">Podrá crear pagos electrónicos desde los diarios de pagos o desde la funcionalidad Cartera (lista de informes).</span><span class="sxs-lookup"><span data-stu-id="2e820-109">You can create electronic payments from the payment journals or from the Cartera functionality (report list).</span></span> <span data-ttu-id="2e820-110">Su objetivo es ocuparse de los casos siguientes:</span><span class="sxs-lookup"><span data-stu-id="2e820-110">This is intended to cover the following cases:</span></span>  
  
-   <span data-ttu-id="2e820-111">Facturas y documentos de cartera abiertos y no agrupados.</span><span class="sxs-lookup"><span data-stu-id="2e820-111">Invoices and open, non-grouped Cartera documents.</span></span> <span data-ttu-id="2e820-112">Si decide pagar mediante pagos electrónicos, el archivo de pago se genera desde el informe **Exportar pagos electrónicos**.</span><span class="sxs-lookup"><span data-stu-id="2e820-112">If you select to pay using electronic payments, then the payment file is generated from the **Export Electronic Payments** report.</span></span>  
  
-   <span data-ttu-id="2e820-113">Facturas y documentos de cartera agrupados en una orden de pago.</span><span class="sxs-lookup"><span data-stu-id="2e820-113">Invoices and Cartera documents that are grouped in a payment order.</span></span> <span data-ttu-id="2e820-114">Si decide pagar mediante pagos electrónicos, el archivo de pago se genera desde el informe **Orden pago - Exportar N34.1**, disponible en la lista de informes de cartera.</span><span class="sxs-lookup"><span data-stu-id="2e820-114">If you select to pay using electronic payments, the payment file is generated from the **PO - Export N34.1** report, available in the Cartera report list.</span></span>  
  
> [!NOTE]  
>  <span data-ttu-id="2e820-115">Los socios pueden tener que modificar este informe para satisfacer los requisitos concretos del banco de su cliente.</span><span class="sxs-lookup"><span data-stu-id="2e820-115">Partners may need to modify this report to meet their customer’s bank individual requirements.</span></span>  
  
 <span data-ttu-id="2e820-116">Para poder hacer transferencias de pago electrónicas a un proveedor, tendrá que configurar una cuenta de banco para el proveedor.</span><span class="sxs-lookup"><span data-stu-id="2e820-116">Before you can transfer payments electronically to a vendor, you will need to set up a bank account for the vendor.</span></span> <span data-ttu-id="2e820-117">También tendrá que configurar los vínculos de pagos electrónicos con el banco y la ficha de cuenta de banco en [!INCLUDE[d365fin](../../includes/d365fin_md.md)] para que su propio banco controle los pagos electrónicos.</span><span class="sxs-lookup"><span data-stu-id="2e820-117">You will also need to set up the electronic payment links with your bank and set up the bank account card in [!INCLUDE[d365fin](../../includes/d365fin_md.md)] for your own bank to handle the electronic payments.</span></span> <span data-ttu-id="2e820-118">El banco debe proporcionar el programa de transmisión.</span><span class="sxs-lookup"><span data-stu-id="2e820-118">The bank should provide the transmission program.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="2e820-119">Consulte también</span><span class="sxs-lookup"><span data-stu-id="2e820-119">See Also</span></span>  
 <span data-ttu-id="2e820-120">[Configurar cuentas bancarias para realizar pagos electrónicos](how-to-set-up-bank-accounts-for-electronic-payments.md) </span><span class="sxs-lookup"><span data-stu-id="2e820-120">[Set Up Bank Accounts for Electronic Payments](how-to-set-up-bank-accounts-for-electronic-payments.md) </span></span>  
 <span data-ttu-id="2e820-121">[Pagar a los proveedores mediante pagos electrónicos](how-to-pay-vendors-by-using-electronic-payments.md) </span><span class="sxs-lookup"><span data-stu-id="2e820-121">[Pay Vendors by Using Electronic Payments](how-to-pay-vendors-by-using-electronic-payments.md) </span></span>  
 <span data-ttu-id="2e820-122">Exportar pagos electrónicos</span><span class="sxs-lookup"><span data-stu-id="2e820-122">Export Electronic Payments</span></span>   
 <span data-ttu-id="2e820-123">Orden pago - Exportar N34.1</span><span class="sxs-lookup"><span data-stu-id="2e820-123">PO - Export N34.1</span></span>