---
title: Establecer límites para fechas de vencimiento
description: Puede modificar los términos de pago para que tengan límites para la cantidad máxima de días que puede transcurrir entre una entrega y el pago correspondiente.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: 94c4cc107be612e7358f5b9c645bdd3dd3455b40
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 09/09/2020
ms.locfileid: "3778319"
---
# <a name="set-limits-for-due-dates"></a>Establecer límites para fechas de vencimiento
Puede modificar los términos de pago para que tengan límites para la cantidad máxima de días que puede transcurrir entre una entrega y el pago correspondiente.  

Los límites legales del espacio entre su entrega y pago determinan cómo se calculan las fechas de vencimiento. Por ejemplo, si crea un término de pago que se utilizará para ventas al sector público, el campo **Nº máx. días hasta fecha vencimiento** para ese plazo de pago debe establecerse en 30 días.  

## <a name="to-set-limits-for-due-dates-on-payment-terms"></a>Para definir los límites para las fechas de vencimiento en términos de pago  

1.  Elija el icono ![Bombilla que abre la función Dígame](../../media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Términos de pago** y luego elija el enlace relacionado.  
2.  Seleccione el término de pago que desea modificar y, a continuación, en el campo **Nº máx. días hasta fecha vencimiento**, especifique el número de días naturales permitidos entre su entrega y el pago.  

A continuación, debe asegurarse de especificar los términos de pago adecuados para sus clientes y proveedores públicos y privados. Cuando crea un documento para ese cliente o proveedor, la fecha de vencimiento del pago se calcula a partir del día en que el cliente recibió los artículos o servicios. A continuación, debe actualizar el campo **Fecha del documento** con la fecha del recibo. Por ejemplo, si actualiza una factura de ventas cuando se le informa de la entrega, la fecha de vencimiento se calcula en función de la nueva fecha del documento que especificó. La fecha de vencimiento calculada no puede superar el límite que especificó para el plazo de pago.  

> [!IMPORTANT]  
>  No puede registrar un documento que crea una remesa donde uno o varios plazos tienen una fecha de vencimiento posterior al límite que se especifica en el campo **Nº máx. días hasta fecha vencimiento**.  

## <a name="see-also"></a>Consulte también  
 [Cálculo de fechas de vencimiento](calculating-due-dates.md)
