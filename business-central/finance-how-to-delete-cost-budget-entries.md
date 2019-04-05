---
title: Procedimiento para eliminar movimientos de presupuestos de costes | Documentos de Microsoft
description: Utilice el trabajo por lotes Eliminar movimientos presupuesto de costes para anular los movimientos de presupuesto de costes del registro de presupuestos de costes.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2018
ms.author: sgroespe
ms.openlocfilehash: 7a5647bcb5a58cdf0a38ec037994d6cbe7a9504d
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 03/08/2019
ms.locfileid: "806068"
---
# <a name="delete-cost-budget-entries"></a>Eliminar movs. ppto. costes
Utilice el trabajo por lotes **Eliminar movimientos presupuesto de costes** para anular los movimientos de presupuesto de costes del registro de presupuestos de costes.  

Para evitar cualquier discontinuidad en movimientos de presupuesto de costes y movimientos de registro de costes, no puede eliminar un único movimiento o sección de movimientos del centro de la lista de los movimientos de registro.  

### <a name="to-delete-a-cost-budget-entry"></a>Para eliminar movimientos de presupuesto de costes  

1.  Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Eliminar movs. ppto. costes** y luego elija el enlace relacionado.  

    El campo **Hasta nº registro** contiene siempre el último número de movimiento de registro, que no se puede cambiar.  

    Puede usar el campo **Desde nº registro** para seleccionar un número de movimiento de registro del que debe iniciar la eliminación.  
2.  Elija el botón **ACEPTAR** para eliminar los movimientos de presupuestos de costes seleccionados.  

> [!NOTE]  
>  Para evitar una eliminación accidental de los movimientos de presupuesto de coste, puede cerrar movimientos de registro marcando las líneas como **Cerrado** en el campo **Cerrado** en la página **Registro de presupuesto de costes**.  

## <a name="see-also"></a>Consulte también  
[Contabilidad para costes](finance-manage-cost-accounting.md)
[Crear presupuesto coste](finance-create-cost-budgets.md)  
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
