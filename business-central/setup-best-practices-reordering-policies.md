---
title: 'Procedimientos recomendados de configuración: políticas de reaprovisionamiento | Documentos de Microsoft'
description: El campo Directiva reaprov. en las fichas de producto ofrece cuatro métodos de planificación distintos que determinan la forma en que interactúan los parámetros individuales de planificación.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.date: 06/13/2024
ms.service: dynamics-365-business-central
---
# <a name="setup-best-practices-reordering-policies"></a>Configurar prácticas recomendadas: directivas de reaprovisionamiento

El campo **Directiva reaprov.** en las fichas de producto tiene métodos de planificación distintos que determinan la forma en que interactúan los parámetros individuales de planificación.  

Un procedimiento recomendado básico para seleccionar una política de reaprovisionamiento es la clasificación ABC del producto. Cuando utiliza la clasificación ABC, gestiona los elementos según tres clases. La clase que utilice depende del valor y el volumen del artículo en relación con el stock total. La siguiente tabla muestra la distribución valor-volumen de las tres clases.

|Clase|Porcentaje de volumen de stock total|Porcentaje de valor de stock total|
|-----|-----------------------------|----------------------------|
|A|10-20|50-70|
|B|nº 20|nº 20|
|C|60-70|10-30|

La clasificación ABC indica que se puede ahorrar esfuerzo y dinero aplicando un control más ligero a los artículos de bajo valor-volumen bajo que a los artículos de alto valor-volumen. Las ilustración siguiente muestra qué directiva de reaprovisionamiento en [!INCLUDE[prod_short](includes/prod_short.md)] es más adecuada para los artículos A, B, y C respectivamente.

![Clasificación ABC.](media/abc_classification.png "abc_classification")

La tabla siguiente proporciona los procedimientos recomendados para seleccionar entre las cuatro políticas.  

|Opción de configuración|Procedimiento recomendado|Comentario|  
|------------------|-------------------|-------------|  
|**Pedido**|Utilice para productos A.<br /><br /> Utilice para productos de fabricación contra pedido.<br /><br /> En la fabricación, utilice para productos de nivel superior y para componentes y semiterminados caros.<br /><br /> Utilice para productos que se compran como envíos directos y pedidos especiales.<br /><br /> No los utilice si no acepta la reserva automática.|Los productos A, como los sofás de piel en una tienda muebles, son productos de alto valor con una velocidad de pedido baja e irregular donde no se acepta el inventario o los atributos necesarios varían. La mejor política de reaprovisionamiento es, por tanto, aquella que planifica específicamente para cada demanda.|  
|**Lote a lote**|Utilice para productos B.<br /><br /> En la fabricación, utilice para los componentes que se producen en varias listas de materiales. Esta directiva garantiza que los pedidos de compra se combinen para el mismo proveedor, por lo que se pueden negociar mejores precios.<br /><br /> Utilice si no está seguro de la política de reaprovisionamiento que debe seleccionar.|Los productos B, como las sillas de comedor, tienen una velocidad de pedido regular y bastante alta, pero también costes de traslado elevados. La mejor política de reaprovisionamiento para los productos B es, por tanto, aquella que es económica y agrupa la demanda en el ciclo de reaprovisionamiento.<br /><br /> El 80 por ciento de los productos pueden utilizar esta política.<br /><br /> Se puede utilizar con éxito sin los parámetros de planificación.|  
|**Cdad. fija reaprov.**|Utilice para productos C.<br /><br /> Combine con parámetros de puntos de pedido.<br /><br /> En la fabricación, utilice para los componentes de nivel inferior.<br /><br /> No utilice si el producto suele ser reservado.|Los productos C, como las tazas de té, son productos de valor inferior con una velocidad de pedido alta y regular. La mejor política de reaprovisionamiento para productos C es, por tanto, aquella que garantiza la disponibilidad constante y permanece siempre por encima de un punto de pedido.<br /><br /> Si el usuario reserva una cantidad para alguna demanda distante, se afectará a la base de la planificación. Aunque el nivel de inventario estimado es aceptable en relación con el punto de nuevo pedido, las cantidades pueden no estar disponibles debido a la reserva.|  
|**Cdad. máxima **|Utilice para productos C con altos costes de traslado o limitaciones de almacenamiento.<br /><br /> Combine con uno o más modificadores de pedidos (cantidad máxima o mínima de pedido o múltiplos de pedido).|Los productos C, como las tazas de té, son productos de valor inferior con una velocidad de pedido alta y regular. La mejor política de reaprovisionamiento para productos C es, por tanto, aquella que garantiza la disponibilidad constante y permanece siempre por encima de un punto de pedido, pero por debajo de un nivel de inventario máximo.<br /><br /> Para modificar el pedido propuesto, tal vez desee reducir la cantidad del pedido a una cantidad máxima especificada de pedido, aumentarla a una cantidad de pedido mínima especificada o redondearla para alcanzar un múltiplo de pedido especificado. **Nota**: Si se utiliza con un punto de pedido, el inventario permanecerá entre el punto de pedido y la cantidad máxima.|  

## <a name="see-also"></a>Consulte también .

 [Configurar prácticas recomendadas: planificación de suministros](setup-best-practices-supply-planning.md)  
 [Detalles de diseño: gestión de directivas de reaprovisionamiento](design-details-handling-reordering-policies.md)  
 [Configurar áreas de aplicación complejas mediante procedimientos recomendados](set-up-complex-application-areas-using-best-practices.md)  
 [Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
