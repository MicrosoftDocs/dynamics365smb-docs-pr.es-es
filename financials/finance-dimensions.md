---
title: Dimensiones | Documentos de Microsoft
description: Usar dimensiones para analizar datos.
services: project-madeira
documentationcenter: 
author: bholtorf
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: analysis, history, track
ms.date: 03/24/2017
ms.author: bholtorf
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 7552ee2b3398c203a7f3295f3203c83914fbb15f
ms.contentlocale: es-es
ms.lasthandoff: 05/04/2017


---
# <a name="dimensions"></a>Dimensiones
Para simplificar la realización de análisis en documentos, como pedidos de venta, puede utilizar dimensiones. Las dimensiones son atributos y valores que clasifican los movimientos de modo que pueda realizar el seguimiento y el análisis de ellos. Por ejemplo, las dimensiones pueden indicar de qué proyecto o departamento procede un movimiento.  

Por ejemplo, en lugar de tener que configurar cuentas contables generales independientes para cada departamento y proyecto puede usar dimensiones. De este modo, dispone de la posibilidad de análisis, sin crear un plan de cuentas complicado.  

Otro ejemplo es configurar una dimensión que se llame *Departamento* y usarla junto con esta dimensión cuando registre documentos de ventas. Así podrá usar herramientas la de inteligencia empresarial para ver qué departamento vende cada producto.
Cuantas más dimensiones use, más detallados serán los informes en los que pueda basar sus decisiones empresariales. Por ejemplo, un movimiento de ventas individual puede incluir información de múltiples dimensiones, por ejemplo:  

* La cuenta en la que se registró la venta del producto  
* Dónde se vendió el producto
* Quién lo vendió
* El tipo de cliente que lo compró  

Puede crear tantas dimensiones con tantos valores como desee.  

**Nota**: Esta funcionalidad que requiere que la experiencia esté definida en **Conjunto de aplicaciones**. Para obtener más información, consulte [Personalizar la experiencia de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-experiences.md).

## <a name="using-dimensions"></a>Usar dimensiones
En un documento como un pedido de ventas, puede agregar información de dimensión de una línea en particular y del mismo documento. Por ejemplo, en la ventana **Pedido de ventas**, puede introducir valores de dimensión para las dos primeras dimensiones abreviadas en las líneas de venta individuales y puede agregar más información de dimensión si elige el botón **Dimensiones**.  

Si trabaja con un diario, puede agregar información de dimensiones a un movimiento del mismo modo, si ha configurado dimensiones abreviadas como campos directamente en las líneas de diario.  

Puede configurar dimensiones predeterminadas para cuentas o tipos de cuenta, para que esas dimensiones o valores de dimensión se completen automáticamente.  

## <a name="dimension-sets"></a>Grupos de dimensiones
Un grupo de dimensiones es una combinación única de valores de dimensión. Se almacena como movimientos de grupo de dimensiones en la base de datos. Cada movimiento de grupo de dimensiones representa un valor de dimensión único. El grupo de dimensiones se identifica por medio de un id común del grupo de dimensiones que está asignado a cada movimiento de grupo de dimensiones que pertenece al grupo de dimensiones.  

Cuando crea una línea de diario, cabecera de documentos o línea de documentos, puede especificar una combinación de valores de dimensión. En lugar de explícitamente guardar cada valor de dimensión en la base de datos, un Id. de grupo de dimensiones se asigna a la línea de diario, cabecera de documentos o línea de documentos para especificar el grupo de dimensiones.  

## <a name="see-also"></a>Consulte también
[Finanzas](finance.md)  
[Configurar dimensiones](finance-setup-dimensions.md)  
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)](ui-work-product.md)  

