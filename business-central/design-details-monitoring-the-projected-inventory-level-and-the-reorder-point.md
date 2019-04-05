---
title: 'Detalles de diseño: Supervisión del nivel de inventario proyectado y el punto de pedido | Documentos de Microsoft'
description: Aprender cómo la planificación de inventario distingue entre el inventario estimado y niveles de inventario disponible estimados.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: design, supply, inventory, planning
ms.date: 10/01/2018
ms.author: sgroespe
redirect_url: design-details-handling-reordering-policies
ms.openlocfilehash: d26790c1c48eff8af150a72f5d5d697eb7b9dc2a
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 03/08/2019
ms.locfileid: "805438"
---
# <a name="design-details-monitoring-the-projected-inventory-level-and-the-reorder-point"></a>Detalles de diseño: Supervisión del nivel de inventario proyectado y el punto de pedido
El inventario es un tipo de aprovisionamiento, pero para planificación del inventario, el sistema de planificación diferencia entre dos niveles de inventario:  

* Inventario proyectado  
* Inventario disponible proyectado  

## <a name="projected-inventory"></a>Inventario proyectado  
Inicialmente, el inventario proyectado es la cantidad de inventario bruto, incluidos aprovisionamientos y demandas en el pasado a pesar de no estar registrados, al iniciar el proceso de planificación. En el futuro, este se convertirá en un nivel inventario proyectado desplazado que se mantiene a través de cantidades en bruto del aprovisionamiento y la demanda futuros, porque se introducen a lo largo de la línea de tiempo (tanto reservados como asignados de otra forma).  

El sistema de planificación usa el inventario proyectado para supervisar el punto de pedido y para determinar la cantidad de pedido al usar la directiva de reaprovisionamiento de cantidad máxima.  

## <a name="projected-available-inventory"></a>Inventario disponible proyectado  
El inventario disponible proyectado es la parte del inventario proyectado que en un momento determinado está disponible para satisfacer la demanda. El motor de planificación usa el inventario disponible proyectado al supervisar el nivel de stock de seguridad.  

El sistema de planificación usa el inventario disponible proyectado para supervisar el nivel del stock de seguridad, ya que el stock de seguridad siempre debe estar disponible para atender la demanda inesperada.  

## <a name="time-buckets"></a>Ciclos  
Tener un estrecho control del inventario proyectado es crucial para detectar cuándo se está alcanzando o cruzando el punto de pedido y calcular la cantidad correcta del pedido cuando se utiliza la directiva de reaprovisionamiento de cantidad máxima.  

Como se ha indicado anteriormente, el nivel de inventario proyectado se calcula al principio del periodo de planificación. Es un nivel bruto que no tiene en cuenta las reservas y asignaciones similares. Para supervisar este nivel de inventario durante la secuencia de planificación, el sistema supervisa los cambios agregados durante un periodo de tiempo, un ciclo. El programa garantiza que el ciclo sea al menos de un día, ya que es la unidad de tiempo más precisa para un evento de demanda o de suministro.  

## <a name="determining-the-projected-inventory-level"></a>Determinación del nivel de inventario proyectado  
En la secuencia siguiente se describe cómo se determina el nivel de inventario proyectado:  

* Cuando un evento de suministro, como, por ejemplo, un pedido de compra, se ha planificado totalmente, aumentará el inventario proyectado en su fecha de vencimiento.  
* Cuando se ha satisfecho completamente un evento de demanda, el inventario proyectado no se reducirá inmediatamente. En su lugar, registra un aviso de disminución, que es un registro interno que lleva la fecha y la cantidad de la contribución al inventario proyectado.  
* Cunando un evento de suministro posterior se planifica y se coloca en la línea temporal, los avisos de disminución registrados se investigan uno a uno hasta la fecha planificada del suministro mientras se actualiza el inventario proyectado. Durante este proceso, se puede alcanzar o pasar el nivel del punto de pedido del aviso de aumento interno.  
* Si se introduce un nuevo pedido de aprovisionamiento, el sistema comprueba si se hace antes del aprovisionamiento actual. Si lo es, el nuevo aprovisionamiento se convierte en el aprovisionamiento actual y el procedimiento de contrapartida comienza de nuevo.  

A continuación se muestra una ilustración gráfica de este principio:  

![Determinación del nivel de inventario proyectado](media/nav_app_supply_planning_2_projected_inventory.png "Determinación del nivel de inventario proyectado")  

1. El suministro **Sa** de 4 (fijos) cierra la demanda **Da** de 3.  
2. CloseDemand: crear un aviso de disminución de -3 (no se mostrará).  
3. El suministro **Sa** está cerrado con un exceso de 1 (no hay más demanda).  

     Esto aumenta el nivel de inventario proyectado en +4, mientras que el inventario **disponible** proyectado es -1.  

4. El siguiente suministro **Sb** de 2 (otro pedido) ya se ha colocado en la escala de tiempo.  
5. El sistema comprueba si hay un aviso de disminución que preceda a **Sb** (no lo hay, por lo que no se realiza ninguna acción).  
6. El sistema cierra el suministro **Sb** (no hay más demanda); A: mediante la reducción a 0 (cancelar) o B: dejándolo como está.  

     Esto aumenta el nivel de inventario proyectado (A: +0 => +4 o B: +2 = +6).  

7. El sistema realiza una comprobación final: ¿hay un aviso de disminución? Sí, hay uno con fecha de **Da**.  
8. El programa agrega el aviso de disminución del aviso -3 en el nivel de inventario proyectado, A: +4 -3 = 1 o B: +6 -3 = +3.  
9. En el caso de A, el sistema crea un pedido con programación anticipada en la fecha **Da**.  

     En caso de B, el punto de pedido se alcanza y no se crea ningún pedido nuevo.  

## <a name="see-also"></a>Consulte también  
[Detalles de diseño: Directivas de reaprovisionamiento](design-details-reordering-policies.md)   
[Detalles de diseño: Parámetros de la planificación](design-details-planning-parameters.md)   
[Detalles de diseño: Gestión de directivas de reaprovisionamiento](design-details-handling-reordering-policies.md)   
[Detalles de diseño: Planificación de aprovisionamiento](design-details-supply-planning.md)
