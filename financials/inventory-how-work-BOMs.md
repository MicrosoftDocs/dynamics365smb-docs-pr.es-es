---
title: Trabajar con listas de materiales | Documentos de Microsoft
description: "Las L.M. de ensamblado especifican qué componentes o recursos se requieren para ensamblar el producto que representa dicha lista. Las L.M. de ensamblado contienen productos pero también pueden contener uno o varios recursos que realicen el trabajo de ensamblado."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 05/06/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: ce75a9d292e12c58efc51c4db2fbc5a37b7553c7
ms.openlocfilehash: f55dcf4b391ae42ab46a22b729597a96645d9b71
ms.contentlocale: es-es
ms.lasthandoff: 05/05/2017


---
# <a name="how-to-work-with-bills-of-materials"></a>Trabajar con listas de materiales
**Nota**: La versión actual de [!INCLUDE[d365fin](includes/d365fin_md.md)] solo contiene la primera parte de la función de administración de ensamblados. Por el momento, solo puede crear listas de materiales de ensamblados y gestionar los productos principales relacionados como productos de inventario normales. En una actualización futura, podrá administrar el ensamblado real de productos desde los componentes, en los flujos ensamblar para stock o ensamblar para pedido, y puede vender componentes como kits.

Utilice listas de materiales para estructurar los productos principales que vende como kits que constan de los componentes del principal o que ensamble para pedido o para stock.

En [!INCLUDE[d365fin](includes/d365fin_md.md)], una lista de materiales se denomina "L.M. de ensamblado". Las L.M. de ensamblado especifican los componentes que contienen las líneas principales. En esta documentación, un producto principal se denomina "elemento del ensamblado".

Las L.M. de ensamblado normalmente contienen productos pero también pueden contener uno o varios recursos que son necesarios para que combinar el ensamblado.

Las L.M. de ensamblado pueden tener varios niveles, lo que significa que un componente de la L.M. de ensamblado puede ser un elemento del ensamblado en sí. En ese caso, el campo **L.M. de ensamblado** en la línea de L.M. de producto contiene **Sí**.

Se aplican requisitos especiales a los productos de la L.M. de ensamblado en lo que respecta a la disponibilidad. Para obtener más información, vea la sección "Para consultar la disponibilidad de un producto por su uso en las L.M. de ensamblado" en [Obtener un resumen de disponibilidad](inventory-how-availability-overview.md).

**Nota**: Esta funcionalidad que requiere que la experiencia esté definida en **Conjunto de aplicaciones**. Para obtener más información, consulte [Personalizar la experiencia de Financials](ui-experiences.md).

## <a name="to-create-an-assembly-bom"></a>Para crear una L.M. de ensamblado
Para definir un producto principal que conste de otros productos y, potencialmente, de recursos necesarios para combinar el principal, debe crear una L.M. de ensamblado.  

Existen dos partes para crear una L.M. de ensamblado:
- Configuración de un producto nuevo
- Definición de la estructura de la lista de materiales del elemento del ensamblado.

1. Configure un producto nuevo. Para obtener más información, vea [Registrar nuevos productos](inventory-how-register-new-items.md).

    Continúe para introducir los componentes o recursos en la L.M. de ensamblado.  
2. En la ventana **Ficha producto** de un elemento del ensamblado, elija la acción **Ensamblado** y, a continuación, seleccione la acción **L.M. de ensamblado**.
3. En la ventana **L.M. de ensamblado**, rellene los campos según sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-view-the-components-of-an-assembly-item-indented-according-to-the-bom-structure"></a>Para ver los componentes de un elemento del ensamblado con sangría según la estructura de la L.M.
En la ventana **L.M. de ensamblado** puede abrir una ventana independiente que muestre que los componentes y cualquier recurso con sangría de acuerdo con la posición de la L.M. debajo del elemento del ensamblado.

1. En la esquina superior derecha, seleccione el icono **Buscar página o informe** ![Buscar página o informe](media/ui-search/search_small.png "Icono Buscar página o informe"), especifique **Productos** y elija el vínculo relacionado.
2. Abra la ficha de un elemento del ensamblado. (El campo **L.M. de ensamblado** de la ventana **Productos** contiene **Sí**).
3. En la ventana **Ficha producto**, elija la acción **Ensamblado** y, a continuación, seleccione la acción **L.M. de ensamblado**.
4. En la ventana **L.M. de ensamblado**, elija la acción **Mostrar L.M.**.

## <a name="to-buy-sell-or-transfer-assembly-items"></a>Para comprar, vender o transferir elementos del ensamblado
Como la versión actual de [!INCLUDE[d365fin](includes/d365fin_md.md)] solo contiene la capacidad de definir y asignar la L.M. de ensamblado a productos, puede manipular los elementos del ensamblado en las líneas de documento como productos normales únicamente.

**Precaución**: La cantidad de existencias de los componentes de la L.M. no se ajustará si lo hace así.

## <a name="see-also"></a>Consulte también
[Registro de productos nuevos](inventory-how-register-new-items.md)  
[Obtener un resumen de disponibilidad](inventory-how-availability-overview.md)     
[Grupos contables inventario](inventory-manage-inventory.md)  
[Trabajar con [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)](ui-work-product.md)

