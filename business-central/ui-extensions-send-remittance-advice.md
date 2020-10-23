---
title: Extensión Enviar de aviso de pago | Documentos de Microsoft
description: Describe la extensión Enviar aviso de pago, que permite enviar por correo electrónico y reenviar el aviso de pago desde el diario de pagos y los movimientos de proveedores.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: app, add-in, manifest, customize, stream, remittance, advice
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: f6afaa9ade29c955033914b608806c3fb0f5a310
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/01/2020
ms.locfileid: "3912226"
---
# <a name="send-remittance-advice"></a><span data-ttu-id="6136a-103">Enviar aviso de pago</span><span class="sxs-lookup"><span data-stu-id="6136a-103">Send Remittance Advice</span></span>

<span data-ttu-id="6136a-104">Cuando se utiliza el aviso de pago para notificar a los proveedores de los pagos que se están realizando, ahora puede enviar el aviso de pago por correo electrónico en bloque desde el diario de pagos, así como volver a enviarlo después de que se hayan realizado los pagos desde las entradas de proveedores mediante el uso de perfiles de envío de documentos.</span><span class="sxs-lookup"><span data-stu-id="6136a-104">Where remittance advice is used to notify vendors of payments being made, you can now email remittance advice in bulk from the payment journal as well as resend after payments are made from vendor ledger entries by using document sending profiles.</span></span>

> [!NOTE]
> <span data-ttu-id="6136a-105">Esta funcionalidad solo es compatible con Business Central Online y local en los siguientes países: Reino Unido, Estados Unidos, Canadá, Australia, Nueva Zelanda y Sudáfrica.</span><span class="sxs-lookup"><span data-stu-id="6136a-105">This functionality is only supported in Business Central online and on-premises in following countries: United Kingdom, United States, Canada, Australia, New Zealand, and South Africa.</span></span>  

<span data-ttu-id="6136a-106">Puede enviar el aviso de pago de dos maneras diferentes:</span><span class="sxs-lookup"><span data-stu-id="6136a-106">You can send remittance advice in two different ways:</span></span>

* <span data-ttu-id="6136a-107">En la página **Diario de pagos**, seleccione **Relacionado**, **Pagos**, **Enviar aviso de remesa** para enviar por correo electrónico el aviso de remesa para una o varias líneas del diario de pagos</span><span class="sxs-lookup"><span data-stu-id="6136a-107">In the **Payment Journal** page, choose **Related**, **Payments**, **Send Remittance Advice** to email remittance advice for one or multiple payment journal lines</span></span>
* <span data-ttu-id="6136a-108">En la página **Movs. proveedores**, elija **Acciones**, **Funciones**, **Enviar aviso de pago** para enviar por correo electrónico un aviso de pago después de registrar los pagos del proveedor, para uno o varios movimientos de proveedores.</span><span class="sxs-lookup"><span data-stu-id="6136a-108">In the **Vendor Ledger Entries** page, choose **Actions**, **Functions**, **Send Remittance Advice** to email remittance advice after posting of vendor payments, for one or multiple vendor ledger entries</span></span>

## <a name="see-also"></a><span data-ttu-id="6136a-109">Consulte también</span><span class="sxs-lookup"><span data-stu-id="6136a-109">See Also</span></span>

[<span data-ttu-id="6136a-110">Proponer pagos a proveedores</span><span class="sxs-lookup"><span data-stu-id="6136a-110">Suggest Vendor Payments</span></span>](payables-how-suggest-vendor-payments.md)  
<span data-ttu-id="6136a-111">[Personalizar [!INCLUDE[d365fin](includes/d365fin_md.md)] con extensiones](ui-extensions.md)</span><span class="sxs-lookup"><span data-stu-id="6136a-111">[Customizing [!INCLUDE[d365fin](includes/d365fin_md.md)] Using Extensions ](ui-extensions.md)</span></span>  
<span data-ttu-id="6136a-112">[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="6136a-112">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="6136a-113">Enviar documentos por correo electrónico</span><span class="sxs-lookup"><span data-stu-id="6136a-113">Send Documents by Email</span></span>](ui-how-send-documents-email.md)  
