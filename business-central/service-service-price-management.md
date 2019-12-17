---
title: Administración del precio de servicio | Documentos de Microsoft
description: Este tema describe cómo aplicar el mejor precio a los pedidos de servicio, configurar los acuerdos de precios de servicio personalizados, mejorar la eficacia de los empelados de servicio y acelerar el proceso de facturación.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: bholtorf
ms.openlocfilehash: 81670627f8658296da7c6c5b0f3e269b78228b0f
ms.sourcegitcommit: cfc92eefa8b06fb426482f54e393f0e6e222f712
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 12/03/2019
ms.locfileid: "2882307"
---
# <a name="service-price-management"></a>Gestión de precios de servicios
La funcionalidad de gestión de precios de servicio le permite aplicar el mejor precio a los pedidos de servicio, configurar los acuerdos de precios de servicio personalizados, mejorar la eficacia de los empelados de servicio y acelerar el proceso de facturación.  
  
La gestión de precios de servicio permite configurar diferentes grupos de precios de servicio para que pueda tener en cuenta el producto de servicio o grupo de productos de servicio, además del tipo de defecto que implica la tarea de servicio. Puede configurar estos grupos durante un periodo de tiempo limitado o para un cliente o una divisa específica. Puede utilizar las estructuras de cálculo de precios como plantilla para asignar un precio específico a una tarea de servicio determinada.  
  
Por ejemplo, esto permite asignar productos específicos incluidos en el precio de servicio, además del tipo de trabajo incluido. También hace posible utilizar diferentes importes de descuento e IVA para distintos grupos de precios de servicio. Para garantizar que se aplican los precios correctos, puede asignar precios fijos, máximos o mínimos, en función de los acuerdos que tenga con los clientes.  
  
Antes de ajustar el precio de un producto o pedido de servicio, se le proporciona una panorámica de cómo será el resultado del ajuste de precios. Puede aprobar estos resultados, o hacer cambios adicionales si desea tener un resultado diferente. Todo el ajuste se realiza línea a línea, lo que significa que no se crean líneas adicionales.  
  
Finalmente, las estadísticas de grupos de precios de servicio y los informes estándar le permiten realizar un seguimiento de la rentabilidad de cada grupo de precios de servicio.  
  
## <a name="service-price-adjustment-groups"></a>Grupos de ajuste de precio de servicio  
Utilice grupos de ajuste de precio de servicio para configurar los distintos tipos de ajustes de precio. Por ejemplo, puede configurar un grupo de ajuste de precios de servicio que ajuste precios de componentes, otro que ajuste precios de mano de obra, otro que ajuste precios de costes, etc. También puede especificar si el ajuste de precios de servicio debe aplicarse a solo un producto o recurso específico, o a todos los productos o recursos.  
  
Cada grupo de ajuste de precios de servicio tiene información relacionada con el ajuste que desea realizar en las líneas de servicio.  
  
La función de ajuste de precio de servicio no se aplica a productos de servicio que pertenecen a contratos de servicio. Sólo puede ajustar los precios de servicio de los productos que formen parte de un pedido de servicio. No puede ajustar el precio de un producto de servicio si tiene una garantía. No puede ajustar el precio de un producto de servicio que forme parte de un pedido de servicio si la línea de servicio asociada a éste se ha registrado como factura, ya sea de forma total o parcial.  
  
Al ejecutar la función de ajuste de precios de servicio, todos los descuentos del pedido se reemplazarán por los valores del ajuste de precios de servicio.  
  
## <a name="service-price-groups"></a>Grupos precio servicio  
Puede configurar grupos de precios de servicio para crear grupos de productos de servicio que reciben el mismo precio de servicio especial. Cuando haya configurado grupos de precio de servicio, podrá asignarlos a productos de servicio de líneas de productos de servicio. También puede asignar grupos de precio de servicio a grupos de producto de servicio.  
  
Antes de que pueda asignar un grupo de precios de servicio a un producto de servicio, deberá determinar a qué área de defecto, divisa o grupo de ajuste de precios de servicio se aplica el grupo de precios de servicio. Tendrá que determinar el importe que debe ajustar el precio de servicio y si este importe debe incluir el IVA y los descuentos. También debe especificar si este ajuste afecta a un importe fijo o sólo debe aplicarse en determinadas condiciones.  
  
Al asignar un grupo de precios de servicio a un producto de servicio, todos los precios de servicio especiales que haya configurado en este grupo se aplicarán a este producto de servicio.  
  
## <a name="service-pricing"></a>Tarifas de servicio  
Puede configurar los tipos de tarifas de servicio (tipo de ajuste de precio y precio) para una combinación de grupos de precio de servicio y grupos de precio de cliente. Seleccione un grupo de ajuste de precios para cada grupo de ajuste de precios de servicio. También debe especificar el tipo de ajuste de precio de servicio (fijo, máximo o mínimo), y el precio real.  
  
Por ejemplo, puede configurar tipos de tarifas de servicio para un grupo de precio de servicio de radio. En el caso de clientes sin un grupo de precio, puede asignar tarifas de servicio con el precio máximo de mano de obra, que se encuentra en el grupo de ajuste de precio de mano de obra. En el caso de clientes con un grupo de precio determinado, puede asignar tarifas de servicio con el precio fijo de mano de obra, en el mismo grupo de ajuste de precio de mano de obra.  
  
## <a name="service-price-adjustment"></a>Ajuste precio servicio  
El ajuste de precios de servicio le permite ajustar el precio de un producto, recurso, cuenta o coste en un pedido de servicio.  
  
Después de especificar un producto en la línea del producto de servicio, escriba toda la información sobre los costes de este producto en las líneas de servicio. Cuando ejecute la función Ajustar precio servicio, se mostrará una vista previa de los ajustes de precio. Puede hacer modificaciones si lo necesita. Cuando acepte las modificaciones, se calcularán los ajustes y, a continuación, los transferirá a las líneas de servicio. Llegado ese momento, registre el pedido de servicio.  
  
Se calculará el importe total de los ajustes en función del tipo de ajuste de precio de servicio.  
  
La siguiente tabla describe los cálculos.  
  
|Opción | Description |  
|----------------------------------|---------------------------------------|  
|**Precio fijo**|Significa que se carga un precio fijo por el producto de servicio, recurso, cuenta o coste, independientemente de los costes reales o cargos normales. Si selecciona esta opción, el ajuste de precios de servicio llegará al importe exacto especificado en el grupo de precios de servicio.|  
|**Máximo**|Significa que se establece un límite superior en el cargo al cliente, independientemente de los costes reales o cargos normales. Si selecciona esta opción, el ajuste de precio de servicio sólo se realizará si el importe total supera el importe especificado en el grupo de precios de servicio.|  
|**Mínimo**|Significa que se establece un límite inferior en el cargo al cliente, independientemente de los costes reales o cargos normales. Si selecciona esta opción, el ajuste de precio de servicio sólo se realizará si el importe total es menor que importe especificado en el grupo de precios de servicio.|  
  
## <a name="see-also"></a>Consulte también  
[Configurar precios y costes adicionales de servicios](service-how-setup-service-costs-pricing.md)  
[Configurar la gestión de servicios](service-setup-service.md)  
