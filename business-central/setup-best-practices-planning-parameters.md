---
title: "Procedimientos recomendados de configuración: parámetros de planificación | Documentos de Microsoft"
description: "La ficha desplegable Planificación de la ficha de producto es el centro de la cadena de suministro de una empresa. La configuración de los parámetros correctos de planificación es muy importante para un control de inventario rentable y un servicio al cliente superior."
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: b8a5f4dcfa9a4e3f728c8de3786e7d5716ac82c7
ms.openlocfilehash: 69344bcc4004ce29a58e8475235a97cf9196605d
ms.contentlocale: es-es
ms.lasthandoff: 10/04/2018

---
# <a name="setup-best-practices-planning-parameters"></a>Procedimientos recomendados de configuración: parámetros de la planificación
La ficha desplegable **Planificación** de la ficha de producto es el centro de la cadena de suministro de una empresa. La configuración de los parámetros correctos de planificación es muy importante para un control de inventario rentable y un servicio al cliente superior.  

 La tabla siguiente proporciona prácticas recomendadas sobre cómo configurar los campos de parámetros de planificación seleccionados. Para obtener más información acerca de un campo, elija el vínculo en la columna **Configurar el campo**.  

|Configurar el campo|Procedimiento recomendado|Comentario|  
|-----------------|-------------------|-------------|  
|Directiva reaprov.||Para obtener más información, consulte [Procedimientos recomendados de configuración: políticas de reaprovisionamiento](setup-best-practices-reordering-policies.md).|  
|Reservar|Seleccione **Nunca** cuando el producto se planifique con un punto de nuevo pedido.<br /><br /> En la fabricación, seleccione **Nunca** para que el sistema de planificación cubra todas las demandas.<br /><br /> Seleccione **Opcional** para los productos que puede ser interesante reservar para los clientes de máxima prioridad.<br /><br /> Seleccione **Siempre** para los productos que no sean únicos, como productos de distintos tipo que se reciben para satisfacer demandas concretas.|Las reservas contrarrestan normalmente el objetivo de la planificación, que es equilibrar la demanda y el suministro. Por lo tanto, los productos que se configuran para planificar, por lo general, no deben ser reservados.<br /><br /> Si el usuario reserva una cantidad del inventario para demanda futura, la base de la planificación se verá perturbada y es posible que el punto de nuevo pedido no funcione correctamente. Aunque el nivel de inventario estimado es aceptable en relación con el punto de nuevo pedido, las cantidades pueden no estar disponibles debido a la reserva.|  
|Periodo amortiguador|Establezca en relación con la flexibilidad del proveedor.<br /><br /> Un período más largo le permite brindar un mejor servicio al cliente, pero también provocará más acciones de reprogramación.|Si el proveedor acepta cambios de última hora en los pedidos, utilice un período más largo, pero esté preparado para más acciones de reprogramación. Si el proveedor requiere la planificación en firme, acorte el periodo tanto como sea posible.<br /><br /> Para obtener información sobre el campo **Periodo amortiguador**, consulte [Detalles diseño: Parámetros de planificación](design-details-planning-parameters.md).|  
|Incluir inventario|Seleccione siempre cuando utiliza la política de reaprovisinamiento de lote a lote.|No seleccione solo en situaciones especiales, por ejemplo, cuando los productos del inventario no sean vendibles.|  
|Plazo de seguridad|Establecer entre 1D y 6D.<br /><br /> Establezca un plazo de seguridad de al menos un día para asegurarse de que los suministros están disponibles el día antes de que se necesiten.<br /><br /> Si utiliza un proveedor nuevo, defina un tiempo superior hasta que se conozca su rendimiento de entrega.<br /><br /> Durante la fabricación, defina plazos de seguridad más largos para componentes críticos.|El suministro planeado por el sistema para evitar que se agoten las existencias llegará el mismo día que se agotan las existencias. Esto puede ocurrir varios horas tarde si, por ejemplo, la demanda se necesita por la mañana y el suministro llega por la tarde. **Nota:** El campo **Plazo de seguridad** utiliza el calendario base. Por tanto, 14D no son necesariamente dos semanas.|  
|Stock de seguridad|Utilice con productos con fluctuaciones grandes de demanda.<br /><br /> En la fabricación, utilice para los componentes críticos.<br /><br /> Utilice para productos que están sujetos a contratos de servicio.|Si el campo **Punto pedido** no se rellena, la cantidad del stock de seguridad también funciona como un punto de nuevo pedido.|  
|Periodo de acumulación de lotes|Si solo desea realizar unos pocos pedidos grandes y acepta guardar inventario, establezca un periodo de acumulación de lotes largo.<br /><br /> Si desea realizar varios pedidos pequeños y tener un inventario reducido, establezca un periodo de acumulación de lotes corto.|El periodo de acumulación de lotes es normalmente el periodo más largo en que guardará inventario.|  
|Punto pedido|Base el punto de nuevo pedido en el perfil de demanda del producto.|Si los datos históricos muestran que la demanda media del producto es de 100 unidades durante un plazo de siete días, el punto de nuevo pedido puede definirse en 100 como mínimo.<br /><br /> Esto quiere decir que cuando el nivel de inventario cae por debajo de las 100 unidades, el sistema de planificación sugerirá reponer porque tarda siete días en suministrar el producto y debe haber suficiente para satisfacer la demanda en ese plazo de siete días.|  
|Ciclo|Deje el campo en blanco, lo que significa que el nivel de inventario se comprueba cada día.|Comprobar el nivel de las existencias cada día asegura una planificación de punto de nuevo pedido óptima. **Nota:** Un ciclo de 1S significa que el nivel de inventario puede estar por debajo del punto de nuevo pedido durante una semana antes de que se sugiera un pedido de suministro.|  
|Precisión redondeo|En una fabricación cara, defina en 0,00001.|Las cantidades grandes de redondeo de consumo de residuos o materiales pueden suponer costes de inventario muy elevados. Por lo tanto, es importante definir la precisión de redondeo más pequeña para minimizar este coste potencial.|  

> [!NOTE]  
>  Las prácticas recomendadas para los parámetros de planificación en las fichas de producto también se aplican a los mismos campos de las fichas de UA.  
>   
>  Si las empresas planean la demanda en distintos almacenes, es muy recomendable definir UA para cada almacén y que toda la demanda se cree con un valor en el campo **Cód. almacén**. Para obtener más información, consulte [Detalles de diseño: Demanda en almacén vacío](design-details-demand-at-blank-location.md).  

## <a name="see-also"></a>Consulte también  
 [Procedimientos recomendados de configuración: planificación de suministros](setup-best-practices-supply-planning.md)   
 [Detalles de diseño: planificación de aprovisionamiento](design-details-supply-planning.md)   
 [Configurar áreas de aplicación complejas mediante procedimientos recomendados](set-up-complex-application-areas-using-best-practices.md)  
 [Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

