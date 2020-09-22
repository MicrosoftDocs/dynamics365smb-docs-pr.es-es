---
title: Asignar un nivel de prioridad a un proveedor | Documentos de Microsoft
description: Puede asignar números a los proveedores para darles prioridad y facilitar las sugerencias de pago en Business Central.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: supplier, payment priority
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: 6dfa7237cde2a88c8d36baa2daa69f4cde97a4eb
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 09/09/2020
ms.locfileid: "3783104"
---
# <a name="prioritize-vendors"></a>De prioridad a los proveedores
[!INCLUDE[d365fin](includes/d365fin_md.md)] puede proponer diversos pagos a proveedores, como los pagos que están próximos a vencer o los pagos en los que se pueden realizar descuentos. Para obtener más información, vea [Proponer pagos a proveedores](payables-how-suggest-vendor-payments.md).

Primero, debe dar prioridad a los proveedores asignándoles números.
<br><br>
> [!Video https://www.microsoft.com/videoplayer/embed/RE3PRGa?rel=0]

## <a name="to-prioritize-vendors"></a>Para dar prioridad a proveedores
1. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Proveedores** y luego elija el enlace relacionado.
2. Seleccione el proveedor correspondiente y, a continuación, elija **Editar**.
3. En el campo **Prioridad**, escriba un número.

[!INCLUDE[d365fin](includes/d365fin_md.md)] considera que el número más bajo, excepto el 0, tiene la prioridad más alta. Por ejemplo, si utiliza 1, 2 y 3; 1 tendrá la prioridad más alta.

Si no desea dar prioridad a un proveedor, deje el campo **Prioridad** en blanco. Más adelante, si utiliza la característica de propuesta de pago, el proveedor se mostrará después de todos los proveedores que poseen un número de prioridad. Puede introducir tantos niveles de prioridad como considere necesario.

## <a name="see-also"></a>Consulte también
[Configurar compras](purchasing-setup-purchasing.md)  
[Administrar pagos](payables-manage-payables.md)  
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
