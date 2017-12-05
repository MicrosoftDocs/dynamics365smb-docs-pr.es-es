---
title: Asignar un nivel de prioridad a un proveedor | Documentos de Microsoft
description: "Puede asignar números a los proveedores para darles prioridad y facilitar las sugerencias de pago en Dynamics 365."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: supplier, payment priority
ms.date: 03/29/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: ba26b354d235981bd7291f9ac6402779f554ac7a
ms.openlocfilehash: d19d0bce7290ce42b37dd1dfbea5213c6580e2da
ms.contentlocale: es-es
ms.lasthandoff: 11/10/2017

---
# <a name="how-to-prioritize-vendors"></a>Asignación de prioridad a proveedores
[!INCLUDE[d365fin](includes/d365fin_md.md)] puede proponer diversos pagos a proveedores, como los pagos que están próximos a vencer o los pagos en los que se pueden realizar descuentos. Para obtener más información, vea [Procedimiento: Proponer pagos a proveedores](payables-how-suggest-vendor-payments.md).

Primero, debe dar prioridad a los proveedores asignándoles números.

## <a name="to-prioritize-vendors"></a>Para dar prioridad a proveedores
1. Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Proveedores** y, a continuación, seleccione el vínculo relacionado.
2. Seleccione el proveedor correspondiente y, a continuación, elija **Editar**.
3. En el campo **Prioridad**, escriba un número.

[!INCLUDE[d365fin](includes/d365fin_md.md)] considera que el número más bajo, excepto el 0, tiene la prioridad más alta. Por ejemplo, si utiliza 1, 2 y 3; 1 tendrá la prioridad más alta.

Si no desea dar prioridad a un proveedor, deje el campo **Prioridad** en blanco. Más adelante, si utiliza la característica de propuesta de pago, el proveedor se mostrará después de todos los proveedores que poseen un número de prioridad. Puede introducir tantos niveles de prioridad como considere necesario.

## <a name="see-also"></a>Consulte también
[Configurar compras](purchasing-setup-purchasing.md)  
[Administrar pagos](payables-manage-payables.md)  
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

