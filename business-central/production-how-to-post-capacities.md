---
title: Cómo registrar capacidades | Documentos de Microsoft
description: En el diario de capacidad, registra las capacidades consumidas que no se asignan a la orden de producción. Por ejemplo, el trabajo de mantenimiento se debe asignar a la capacidad, pero no a una orden de producción.
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
ms.openlocfilehash: 58005b8b4d401f5eab8a934d7b00b610b64b4281
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 03/31/2019
ms.locfileid: "928305"
---
# <a name="post-capacities"></a>Registrar capacidades
En el diario de capacidad, registra las capacidades consumidas que no se asignan a la orden de producción. Por ejemplo, el trabajo de mantenimiento se debe asignar a la capacidad, pero no a una orden de producción.  

## <a name="to-post-capacities"></a>Para registrar capacidades  
1.  Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Diarios de capacidad** y luego elija el enlace relacionado.  
2.  Rellene los campos **Fecha registro** y **Nº documento**.  
3.  En el campo **Tipo**, introduzca el tipo de capacidad, ya sea **Centro máquina** o **Centro trabajo**, que esté registrando.  
4.  En el campo **N.º**, introduzca el número del centro de trabajo o del centro de máquina.  
5.  Introduzca los datos correspondientes en el resto de los campos, como **Hora inicial**, **Hora final**, **Cantidad** y **Rechazo**.  
6.  Para registrar la factura, elija la acción **Registrar**.  

## <a name="to-view-work-center-ledger-entries"></a>Para consultar los movimientos de centros de trabajo  
En las páginas **Ficha de centro de trabajo** y **Ficha de centro de máquina**, puede ver las capacidades registradas como resultado de órdenes de producción terminadas.    
1.  Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Centros trabajo** y luego elija el enlace relacionado.  
2.  Abra la ficha relevante **Centro trabajo** de lista, y seleccione la acción **Movimientos de capacidad**.  

La página **Movs. capacidad** muestra los movimientos registrados desde el centro de trabajo en la orden en que fueron registrados.   

## <a name="see-also"></a>Consulte también  
[Fabricación](production-manage-manufacturing.md)    
[Configuración de fabricación](production-configure-production-processes.md)  
[Planificación](production-planning.md)      
[Grupos contables inventario](inventory-manage-inventory.md)  
[Compras](purchasing-manage-purchasing.md)  
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
