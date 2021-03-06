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
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 7560131ec60d9cf494bdd87884f169e00ec89382
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 03/31/2021
ms.locfileid: "5784720"
---
# <a name="send-remittance-advice"></a>Enviar aviso de pago

Cuando se utiliza el aviso de pago para notificar a los proveedores de los pagos que se están realizando, ahora puede enviar el aviso de pago por correo electrónico en bloque desde el diario de pagos, así como volver a enviarlo después de que se hayan realizado los pagos desde las entradas de proveedores mediante el uso de perfiles de envío de documentos.

> [!NOTE]
> Esta funcionalidad solo es compatible con Business Central Online y local en los siguientes países: Reino Unido, Estados Unidos, Canadá, Australia, Nueva Zelanda y Sudáfrica.  

Puede enviar el aviso de pago de dos maneras diferentes:

* En la página **Diario de pagos**, seleccione **Relacionado**, **Pagos**, **Enviar aviso de remesa** para enviar por correo electrónico el aviso de remesa para una o varias líneas del diario de pagos
* En la página **Movs. proveedores**, elija **Acciones**, **Funciones**, **Enviar aviso de pago** para enviar por correo electrónico un aviso de pago después de registrar los pagos del proveedor, para uno o varios movimientos de proveedores.

## <a name="see-also"></a>Consulte también

[Proponer pagos a proveedores](payables-how-suggest-vendor-payments.md)  
[Personalizar [!INCLUDE[prod_short](includes/prod_short.md)] con extensiones](ui-extensions.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Enviar documentos por correo electrónico](ui-how-send-documents-email.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]