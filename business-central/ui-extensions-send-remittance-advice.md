---
title: Extensión Enviar de aviso de pago | Documentos de Microsoft
description: Describe la extensión Enviar aviso de pago, que permite enviar por correo electrónico y reenviar el aviso de pago desde el diario de pagos y los movimientos de proveedores.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: app, add-in, manifest, customize, stream, remittance, advice
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: e0868a5919f82af9d19dbd692c8d27577e64b6b0
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5376967"
---
# <a name="send-remittance-advice"></a><span data-ttu-id="a475b-103">Enviar aviso de pago</span><span class="sxs-lookup"><span data-stu-id="a475b-103">Send Remittance Advice</span></span>

<span data-ttu-id="a475b-104">Cuando se utiliza el aviso de pago para notificar a los proveedores de los pagos que se están realizando, ahora puede enviar el aviso de pago por correo electrónico en bloque desde el diario de pagos, así como volver a enviarlo después de que se hayan realizado los pagos desde las entradas de proveedores mediante el uso de perfiles de envío de documentos.</span><span class="sxs-lookup"><span data-stu-id="a475b-104">Where remittance advice is used to notify vendors of payments being made, you can now email remittance advice in bulk from the payment journal as well as resend after payments are made from vendor ledger entries by using document sending profiles.</span></span>

> [!NOTE]
> <span data-ttu-id="a475b-105">Esta funcionalidad solo es compatible con Business Central Online y local en los siguientes países: Reino Unido, Estados Unidos, Canadá, Australia, Nueva Zelanda y Sudáfrica.</span><span class="sxs-lookup"><span data-stu-id="a475b-105">This functionality is only supported in Business Central online and on-premises in following countries: United Kingdom, United States, Canada, Australia, New Zealand, and South Africa.</span></span>  

<span data-ttu-id="a475b-106">Puede enviar el aviso de pago de dos maneras diferentes:</span><span class="sxs-lookup"><span data-stu-id="a475b-106">You can send remittance advice in two different ways:</span></span>

* <span data-ttu-id="a475b-107">En la página **Diario de pagos**, seleccione **Relacionado**, **Pagos**, **Enviar aviso de remesa** para enviar por correo electrónico el aviso de remesa para una o varias líneas del diario de pagos</span><span class="sxs-lookup"><span data-stu-id="a475b-107">In the **Payment Journal** page, choose **Related**, **Payments**, **Send Remittance Advice** to email remittance advice for one or multiple payment journal lines</span></span>
* <span data-ttu-id="a475b-108">En la página **Movs. proveedores**, elija **Acciones**, **Funciones**, **Enviar aviso de pago** para enviar por correo electrónico un aviso de pago después de registrar los pagos del proveedor, para uno o varios movimientos de proveedores.</span><span class="sxs-lookup"><span data-stu-id="a475b-108">In the **Vendor Ledger Entries** page, choose **Actions**, **Functions**, **Send Remittance Advice** to email remittance advice after posting of vendor payments, for one or multiple vendor ledger entries</span></span>

## <a name="see-also"></a><span data-ttu-id="a475b-109">Consulte también</span><span class="sxs-lookup"><span data-stu-id="a475b-109">See Also</span></span>

[<span data-ttu-id="a475b-110">Proponer pagos a proveedores</span><span class="sxs-lookup"><span data-stu-id="a475b-110">Suggest Vendor Payments</span></span>](payables-how-suggest-vendor-payments.md)  
<span data-ttu-id="a475b-111">[Personalizar [!INCLUDE[prod_short](includes/prod_short.md)] con extensiones](ui-extensions.md)</span><span class="sxs-lookup"><span data-stu-id="a475b-111">[Customizing [!INCLUDE[prod_short](includes/prod_short.md)] Using Extensions ](ui-extensions.md)</span></span>  
<span data-ttu-id="a475b-112">[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="a475b-112">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="a475b-113">Enviar documentos por correo electrónico</span><span class="sxs-lookup"><span data-stu-id="a475b-113">Send Documents by Email</span></span>](ui-how-send-documents-email.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]