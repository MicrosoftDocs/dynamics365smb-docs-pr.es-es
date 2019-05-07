---
title: Sobre los costes del orden de producción terminada | Documentos de Microsoft
description: La finalización de la orden de producción es una tarea importante para terminar el ciclo de costes del producto que se está fabricando. Los costes finales, incluidas las desviaciones en un entorno de costes estándar, costes reales en un entorno de costes FIFO, medio o LIFO, se calculan mediante el proceso de trabajo por lotes Costes ajustados - movimientos de productos.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: 96cf025bbac137f61f41a65cbd2f9520f2c5e787
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 03/31/2019
ms.locfileid: "925358"
---
# <a name="about-finished-production-order-costs"></a>Sobre los costes del orden de producción terminada
La finalización de la orden de producción es una tarea importante para terminar el ciclo de costes del producto que se está fabricando. Los costes finales, entre los que se incluyen las desviaciones en un entorno de costes estándar y los costes reales en un entorno de costes FIFO, medio o LIFO, se calculan mediante el proceso **Valorar stock - movs. producto**, que permite realizar la conciliación financiera de los costes de la fabricación de productos. Para que una orden de producción se tenga en cuenta en el ajuste de costes, el estado debe ser **Terminada**. Por ello, es esencial que, al terminarla, el estado de una orden de producción se cambie a **Terminada**.  

## <a name="example"></a>Ejemplo:  
 En un entorno de coste estándar, cuando se consume material para fabricar un producto, el coste del producto más la mano de obra y los gastos generales se incluyen en el WIP. Cuando se fabrica el producto, el WIP es reduce en el importe del coste estándar del artículo. Normalmente, estos costes no dan cero como resultado. Para que el resultado pueda ser cero, debe ejecutar el proceso **Valorar stock - movs. producto**, teniendo en cuenta que sólo se tendrán en cuenta en el ajuste las órdenes de producción con el estado de **Terminada**.  

## <a name="see-also"></a>Consulte también  
[Gestión de costes de inventario](finance-manage-inventory-costs.md)  
[Fabricación](production-manage-manufacturing.md)  
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
