---
title: Manejo de tamaños de lote | Documentos de Microsoft
description: Este tema describe diferentes formas de manejar los tamaños de lote.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: bholtorf
ms.openlocfilehash: 6f07828e969d5a8394657bc1e05d44156ada5411
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "4749023"
---
# <a name="handling-lot-sizes-in-production"></a>Manejo de tamaños de lote en producción
En términos de cantidad, la cantidad de artículos que produce en una operación de producción puede no correlacionarse con cómo venderlos. Por ejemplo, puede producir cientos de artículos en un solo lote, pero vender cada artículo individualmente. Cuando configura sus rutas de producción y listas de materiales (LDM), hay algunos matices que debe considerar con respecto a los tamaños de lote. Este tema describe cómo el tamaño de los lotes afecta los cálculos de costos y la planificación de recursos.

## <a name="units-of-measure-in-production-bill-of-materials"></a>Unidades de medida en la lista de materiales de producción
Aunque especifica la unidad de medida base (UOM) para un artículo, su BOM puede usar una UOM diferente para el producto terminado. Por ejemplo, la unidad de medida base de un artículo podría ser PCS, pero su lista de materiales podría requerir paleta o tonelada. Esto resulta útil cuando sus máquinas o componentes en bruto dictan el volumen. Por ejemplo, probablemente no quieras hornear un solo panecillo porque es difícil usar una porción de huevo. En cambio, hornea un lote de muffins para reducir el desperdicio. Para obtener más información, consulte [Crear L.M. de producción](production-how-to-create-production-boms.md).

## <a name="lot-size-on-routing-lines"></a>Tamaño de lote en líneas de enrutamiento
Desde una perspectiva de enrutamiento, puede especificar un tamaño de lote en las líneas de enrutamiento para alinearlo con la capacidad de las máquinas que producen los artículos. El tiempo de ejecución en las líneas de enrutamiento se reduce proporcionalmente al tamaño del lote. 

Esto funciona bien cuando la cantidad en una orden de producción es un factor del tamaño del lote en la ruta. Por ejemplo, si su bandeja para hornear puede contener 10 muffins, debe hornear 10, 20, 30, etc., y no 5 ni 15.  Esto es un problema mucho menor si se trata de grandes cantidades.

El tamaño de lote también es popular en entornos de fabricación donde la producción se mide como la cantidad que puede producir durante un período de tiempo fijo. Por ejemplo, si el volumen por turno de 9 horas es de 25000 pies cúbicos, puede establecer el tiempo de ejecución en 9 horas y el tamaño del lote en 25000.
La cantidad de la orden de producción se vuelve menos importante ya que en la orden de producción el tiempo de ejecución se calcula como el tiempo de ejecución / tamaño del lote para obtener el tiempo de ejecución por pieza.
 
> [!NOTE]
> El valor definido en Tamaño del lote no tiene impacto en el tiempo especificado en el campo **Tiempo de configuración** de la línea de enrutamiento. La configuración ocurrirá solo una vez, incluso si hay varios lotes. Por ejemplo, para que no necesite calentar el horno para el segundo lote de muffins. Para obtener más información, consulte [Crear rutas](production-how-to-create-routings.md).

## <a name="lot-sizes-for-items-and-stockkeeping-units"></a>Tamaños de lote para artículos y unidades de almacenamiento
Los tamaños de lote definidos para las rutas no son los mismos que los tamaños de lote para artículos o unidades de almacenamiento. Estos valores se utilizan para un propósito diferente y no afectan la capacidad de producción. 

## <a name="lot-size-on-item-and-stockkeeping-units"></a>Tamaño de lote en artículos y unidades de almacenamiento
Para artículos y unidades de almacenamiento, los tamaños de lote tienen los siguientes efectos en el cálculo de costos y la planificación de suministros:

* Para el cálculo de costos estándar, si habilita **Configuración de costo incluido** en la página **Configuración de fabricación**, el costo de la instalación se agrega al costo estándar. Si especifica un tamaño de lote, el costo de configuración para la operación de enrutamiento se reducirá de acuerdo con un tamaño de lote. Por ejemplo, si el tamaño de su lote definido en la ficha del artículo es 10 y se tarda 15 minutos en calentar el horno, el costo del combustible se asignará a los 10 muffins como aproximadamente 1,5 minutos. 

> [!NOTE]
> Los costos de instalación se manejan de manera diferente a las perspectivas de asignación de capacidad y costos estándar. Si la cantidad producida no coincide con el tamaño del lote definido en la ficha del artículo, se producirán variaciones. Para obtener más información, vea [Administrar costes de inventario](finance-manage-inventory-costs.md). <!--not sure that I got this part right seems to repeat the first example.-->

Para la planificación de suministros, la configuración del tamaño de lote de los artículos funciona con **% predet. amortiguador** en la página **Configuración de fabricación**. [!INCLUDE[prod_short](includes/prod_short.md)] ignorará los cambios en la demanda que estén por debajo del porcentaje del amortiguador y no creará sugerencias de planificación. Por ejemplo, se especifica 15 en el campo% de amortiguador predeterminado, y tenemos una orden de producción de 20 muffins para alimentar a 20 invitados, pero un invitado no puede asistir. [!INCLUDE[prod_short](includes/prod_short.md)] ignorará al único invitado que falta porque es solo el 10% del tamaño de lote 10 definido en el artículo. Sin embargo, si dos invitados no pueden asistir, [!INCLUDE[prod_short](includes/prod_short.md)] sugerirá que reduzcamos la cantidad del pedido porque dos es el 20 % del tamaño del lote. Para obtener más información sobre la planificación, consulte [Planificación](production-planning.md).

## <a name="see-also"></a>Consulte también
[Crear LM de producción](production-how-to-create-production-boms.md)  
[Trabajar con unidades de medida de lote de fabricación](production-how-to-use-the-manufacturing-batch-unit-of-measure.md)
[Crear enrutamientos](production-how-to-create-routings.md)  
[Gestión de costes de inventario](finance-manage-inventory-costs.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]