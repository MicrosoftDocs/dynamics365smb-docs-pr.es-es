---
title: 'Procedimientos recomendados de configuración: valoración de existencias | Documentos de Microsoft'
description: La Valoración existencias en la ficha de producto define cómo se registra el flujo de coste del producto y si un el valor real o presupuestado se capitaliza y utiliza en el cálculo del coste.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: f0b2a8467f58f705ecf5b0f124d8627e475b361e
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/01/2019
ms.locfileid: "2315785"
---
# <a name="setup-best-practices-costing-method"></a>Procedimientos recomendados de configuración: valoración de existencias
La **Valoración existencias** en la ficha de producto define cómo se registra el flujo de coste del producto y si un el valor real o presupuestado se capitaliza y utiliza en el cálculo del coste.  

 La configuración de la valoración de existencias correcta según el tipo de producto y el entorno de negocio es importante para garantizar inventarios económicos.  

 En la tabla siguiente se proporcionan prácticas recomendadas sobre cómo configurar el campo **Método registro**. Para obtener más información, consulte [Detalles de diseño: Métodos de coste](design-details-costing-methods.md).  

|Opción de configuración|Procedimiento recomendado|Comentario|  
|------------------|-------------------|-------------|  
|FIFO|Utilice esto donde el coste del producto es estable.<br /><br /> Utilice esto para los productos con una vida útil limitado, porque los productos más antiguos deben venderse antes de que superen su fecha de límite de venta.|El coste unitario de un producto es el valor real de cualquier recepción del producto, seleccionado durante la regla de FIFO.<br /><br /> En la valoración del inventario, se presupone que los primeros productos colocados en el inventario se venden primero. **Nota**: Cuando suben los precios, la hoja de balance muestra el valor mayor. Esto significa que las deudas tributarias aumentan, pero las puntuaciones de crédito y capacidad de pedir efectivo prestado mejoran.|  
|LIFO|Utilice esto donde los niveles de inventarios se mantienen constantes o aumentan en el tiempo.|El coste unitario de un producto es el valor real de cualquier recepción del producto, seleccionado durante la regla de LIFO.<br /><br /> En la valoración del inventario, se presupone que los últimos productos colocados en el inventario se venden primero. **Nota**: Cuando suben los precios, el valor del balance de ingresos disminuye. Esto significa que las deudas tributarias disminuyen, pero la capacidad de pedir efectivo prestado deteriora. **Importante:**  No se permite en muchos países o regiones, ya que puede utilizarse para debilitar las ganancias.|  
|Promedio|Utilice esto donde el coste del producto no es estable.<br /><br /> Utilice esto donde los inventarios se apilan o se mezclan juntos y no pueden ser diferenciados, tal como sustancias químicas.|El coste unitario de un producto es el coste exacto en el que la unidad determinada fue recibida.|  
|Específico|Utilice esto en la producción o el comercio de productos fácilmente identificables con costes unitarios relativamente elevados.<br /><br /> Utilice para productos que están sujetos normativas.<br /><br /> Utilice esto para los productos con números de serie.|El coste unitario de un producto se calcula como el coste unitario medio en cada momento después de una compra.<br /><br /> De la valoración del inventario, se presupone que todos los inventarios se venden simultáneamente.|  
|Estándar|Utilice esto donde el control del coste es crítico.<br /><br /> Utilice esto en la fabricación repetitiva para establecer el valor de los costes de material directo, mano de obra directa y gastos de fabricación.<br /><br /> Utilice esto cuando hay disciplina y personal para mantener los estándares.|El coste unitario de un producto se preestablece basándose en una estimación.<br /><br /> Cuando el coste real se realiza posteriormente, el coste estándar se debe ajustar al coste real a través de valores de varianza.|  

## <a name="see-also"></a>Consulte también  
 [Detalles de diseño: Métodos de coste](design-details-costing-methods.md)   
 [Detalles de diseño: Coste de inventario](design-details-inventory-costing.md)   
 [Configurar áreas de aplicación complejas mediante procedimientos recomendados](set-up-complex-application-areas-using-best-practices.md)  
 [Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
