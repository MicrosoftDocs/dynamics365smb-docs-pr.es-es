---
title: Acerca del cálculo de coste estándar
description: Un sistema de costes estándar determina el coste unitario del inventario en función de costes históricos o esperados razonables.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: 5841
ms.author: edupont
ms.openlocfilehash: c7be7f69c2b5d2c71b54ac3046900474e0c86f5f
ms.sourcegitcommit: 2fa712d0aabe4287ebd4454c28d142d6baf045a0
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 05/09/2022
ms.locfileid: "8729916"
---
# <a name="about-calculating-standard-cost"></a>Acerca del cálculo de coste estándar
Muchas empresas de fabricación eligen una base de valoración de coste estándar. Esto también se aplica a las empresas que llevan a cabo la fabricación ligera, como ensamblado y kitting. Un sistema de costes estándar determina el coste unitario del inventario en función de ciertos costes históricos o esperados razonables. Los estudios sobre costes anteriores y sobre costes futuros previstos pueden ofrecer una base para calcular costes estándar. Dichos costes quedan fijos hasta que se tome la decisión de cambiarlos. El coste real para fabricar un producto puede ser diferente de los costes estándar calculados. Para controlar la gestión, el coste real se compara con el coste estándar de un producto en particular, y se identifican y analizan las diferencias o *variaciones*.  

Los costes estándar se pueden mantener para los productos que se rellenan con la compra, el ensamblado y la producción. Para cada método de reaprovisionamiento, el coste estándar puede constar de los elementos siguientes.  

|Sistema reposición|Elementos de coste estándar|  
|--------------------------|----------------------------|  
|**Compra**|El coste directo de material y el coste general de material son necesarios.|  
|**Ensamblado**|Coste directo del material, coste directo o de mano de obra fija y coste general.|  
|**Ord. prod.**|Coste directo del material, coste de mano de obra, coste de subcontratista y coste general.|  

## <a name="setting-up-standard-costs"></a>Configuración de los costes estándar  
Dado que el coste estándar de un producto fabricado o ensamblado puede incluir diversos elementos de coste, entre ellos, costes de materiales, de capacidad (mano de obra) y de subcontratistas, ya sean directos o generales, deben establecerse los costes estándar para cada uno de estos elementos.  

La tarea contable que debe llevar a cabo una empresa de producción que utilice un sistema de costes estándar es:  

- Calcular un coste estándar del producto acabado y configurarlo en la ficha respectiva.  
- Registrar y asignar el coste real de los elementos de coste clave y considerar las variaciones.  

Para determinar el coste directo de un producto acabado, es necesario totalizar los costes de todos los componentes. Un producto ensamblado o fabricado puede incluir subensamblados, que también constan de varios componentes.  

Los elementos de coste claves siguientes conforman el coste directo total de un producto procesado acabado:  

- Costes de materiales.  
- Costes de capacidad.  
- Costes de subcontratistas para los productos fabricados solo.  

### <a name="material-costs"></a>Costes de materiales

Los costes de materiales son aquellos que se asocian con productos semiterminados y materias prima que se hayan comprado. El coste unitario del material puede estar compuesto por elementos de coste directos e indirectos.  

- El coste directo del material representa la cantidad facturada por las materias primas que se hayan comprado o por el coste de procesamiento de un producto semiterminado.  
- El coste indirecto del material, o *costes generales*, puede representar elementos tales como costes de merma de existencias del producto acabado después de producido.  

La configuración del coste de materiales para los productos comprados que afectan los costes directos e indirectos depende del método de valoración que haya seleccionado para el producto en cuestión. Puede configurar la información relativa al coste para cualquiera de los métodos en la ficha de producto. Para obtener más información, vea [Registrar nuevos productos](inventory-how-register-new-items.md).

El coste del rechazo (solo producción) es un factor adicional que debe tenerse en cuenta cuando se calcula el coste material total. Cuando se rechaza una cierta cantidad de las materias primas al ensamblar o fabricar un producto, normalmente conlleva un aumento en el número de componentes que se requieren para la producción. Esto incrementa el coste de materiales de los componentes que se consumen al fabricar un producto principal. Puede configurar el coste del rechazo de materiales en la L.M. de producción o en la ruta.  

El coste de materiales de un producto fabricado se puede representar de dos formas, que se corresponden con las siguientes bases de cálculo de coste:  

|Base de cálculo de coste|Cálculo de coste de material|  
|----------------------------|-------------------------------|  
|Un nivel|El producto fabricado es igual al coste total de todos los productos comprados o subensamblados en la L.M. de producción de dicho producto.|  
|Nivel o multinivel distribuido|El producto fabricado representa la suma del coste de materiales de todos los productos semiterminados en la L.M. de ese producto y el coste de todos los productos comprados en la L.M. de producción de ese producto.|  

### <a name="capacity-costs"></a>Costes de capacidad  
Los costes de capacidad son aquellos que están asociados con la mano de obra interna y con los costes de maquinaria. Debe configurar estos costes para cada recurso (en la administración de ensamblados) y trabajo o centro de máquina en la ruta (en la producción). Al igual que con los materiales, puede identificar los elementos directos e indirectos de los costes de capacidad. Por ejemplo, el coste directo para un centro de trabajo podría ser la tasa de planta establecida para llevar a cabo una función específica. El coste indirecto para un centro de trabajo puede representar ciertos gastos de la fábrica, como iluminación, calefacción, etc. Al igual que los costes de materiales, puede expresar el coste general de capacidad como un porcentaje de coste indirecto o como una tasa general fija.  

En la configuración de los costes de capacidad de los productos ensamblados, están implicados los siguientes elementos:  

- Coste unitario directo e indirecto del recurso.  
- Tipo fijo o directo de utilización de recursos.  

En la configuración de los costes de capacidad de los productos fabricados, están implicados los siguientes elementos:  

- Coste unitario directo e indirecto del centro de trabajo o de máquina.  
- La configuración del tiempo y del tamaño del lote.  

Para calcular el coste de capacidad estándar, deberá establecer cuáles son las tiempos estándar requeridos para llevar a cabo las operaciones con las máquinas y los trabajos en los centros. Normalmente, el tiempo total necesario para completar una operación consta del tiempo de preparación, de ejecución, y de espera y traslado.  

Puede configurar las tasas para cada tipo de tiempo por cada máquina o centro de trabajo de una ruta en particular.  

> [!NOTE]  
>  Mientras las tasas de tiempo de ejecución se aplican para cada unidad de producto fabricado, las tasas de tiempo de preparación se aplican para cada lote. Por tanto, debe prorratear el tiempo de preparación de la ruta por cada operación en función del tamaño del lote. Puede especificar el tamaño del lote en el campo correspondiente de la ficha desplegable **Reposición** de la página **Ficha de producto**.  

Para especificar el tiempo de preparación en la ruta por motivos de planificación, pero no incluir este gasto en el cálculo del coste estándar, desactive el campo **Coste incl. preparación** de la página **Configuración fabricación**.  

En el caso de un solo nivel, se trata del coste de mano de obra requerido para fabricar el producto final y se especifica en la ruta de producción del producto. En el caso de varios niveles, se trata del coste de capacidad que se especifica para cada producto que se fabrica individualmente que se incluye en la L.M. del producto principal.  

### <a name="subcontractor-costs"></a>Costes de los subcontratistas  
Los costes de subcontratistas son aquellos asociados con los servicios que ofrecen los fabricantes o los subcontratistas externos de una empresa. De forma similar a los materiales y a la capacidad, los costes de subcontratistas pueden estar compuestos por cantidades directas y generales. Los costes directos de subcontratistas representan el cargo efectivo por cada unidad de servicio prestado. Por ejemplo, los costes generales de subcontratistas pueden representar costes de transporte y manipulación en los que incurre la empresa con un pedido que se ha subcontratado.  

Dado que la subcontratación es una capacidad externalizada, puede configurar el coste de los servicios subcontratados tanto directos como indirectos en la ficha del centro de trabajo que representa la operación de subcontratación.  

## <a name="updating-standard-costs"></a>Actualización de los costes estándar  
Para actualizar o calcular el coste estándar de elementos de ensamblado, use la función de la ficha de producto.  

El proceso de actualizar o calcular los costes estándar normalmente consiste en las siguientes tareas:  

1.  La actualización de costes en los niveles de componente y de capacidad. Para obtener más información, consulte los procesos **Sugerir coste estándar prod.** y **Sugerir coste estándar capacidad**.  
2.  Consolidación y distribución de los costes de componentes y de la capacidad para calcular el coste total de fabricación o montaje de los productos. Para obtener más información, consulte la sección [Para calcular el coste estándar de un elemento de ensamblado](inventory-how-work-boms.md#to-calculate-the-standard-cost-of-an-assembly-item).  
3.  La implementación de los costes estándar que se introducen al ejecutar los procesos por lotes anteriores. Los costes estándar no tienen efecto hasta que se implementan. Use el trabajo por lotos **Implementar cambios de coste estándar** que actualiza los cambios en el coste estándar en los artículos con los de la tabla de la Hoja de trabajo de coste estándar.  
4.  Implementación de los cambios para actualizar el campo **Coste unitario** en la ficha del producto y realizar una revalorización de inventario. Para obtener más información, vea [Revaluación de inventario](inventory-how-revalue-inventory.md).

## <a name="see-also"></a>Consulte también  
 [Detalles de diseño: Métodos de coste](design-details-costing-methods.md)   
 [Trabajar con listas de materiales](inventory-how-work-BOMs.md)   
 [Actualizar costes estándar](finance-how-to-update-standard-costs.md)   
 [Detalles de diseño: Coste de inventario](design-details-inventory-costing.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]