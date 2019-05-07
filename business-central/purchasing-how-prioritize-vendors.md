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
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: c709539b24aa1f94c86dee26dd63adead39c892b
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 03/31/2019
ms.locfileid: "915605"
---
# <a name="prioritize-vendors"></a>De prioridad a los proveedores
[!INCLUDE[d365fin](includes/d365fin_md.md)] puede proponer diversos pagos a proveedores, como los pagos que están próximos a vencer o los pagos en los que se pueden realizar descuentos. Para obtener más información, vea [Proponer pagos a proveedores](payables-how-suggest-vendor-payments.md).

Primero, debe dar prioridad a los proveedores asignándoles números.

## <a name="to-prioritize-vendors"></a>Para dar prioridad a proveedores
1. Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Proveedores** y luego elija el enlace relacionado.
2. Seleccione el proveedor correspondiente y, a continuación, elija **Editar**.
3. En el campo **Prioridad**, escriba un número.

[!INCLUDE[d365fin](includes/d365fin_md.md)] considera que el número más bajo, excepto el 0, tiene la prioridad más alta. Por ejemplo, si utiliza 1, 2 y 3; 1 tendrá la prioridad más alta.

Si no desea dar prioridad a un proveedor, deje el campo **Prioridad** en blanco. Más adelante, si utiliza la característica de propuesta de pago, el proveedor se mostrará después de todos los proveedores que poseen un número de prioridad. Puede introducir tantos niveles de prioridad como considere necesario.

## <a name="see-also"></a>Consulte también
[Configurar compras](purchasing-setup-purchasing.md)  
[Administrar pagos](payables-manage-payables.md)  
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
