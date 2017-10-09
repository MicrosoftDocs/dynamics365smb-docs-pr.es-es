---
title: Configurar precio y costes de servicios | Documentos de Microsoft
description: "Más información sobre cómo configurar precios y costes adicionales de servicios."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: service, cost, service order
ms.date: 08/22/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: d0f0fcdff4a67df7542c5acb6d44f804997d1a2c
ms.contentlocale: es-es
ms.lasthandoff: 09/22/2017

---

# <a name="how-to-set-up-pricing-and-additional-costs-for-services"></a>Configurar precios y costes adicionales de servicios
Puede utilizar las funciones de precios de [!INCLUDE[d365fin](includes/d365fin_md.md)] para configurar y personalizar su aplicación de modo que aplique y ajuste precios sobre productos de servicio, reparaciones y pedidos. Estas decisiones de precios se transmiten con facilidad al proceso de facturación.  
  
Según requiera su implementación, puede configurar grupos de precios y asignarlos a periodos de tiempo, clientes o divisa específicos. Puede configurar precios fijos, mínimos o máximos, en función de los contratos de servicio que tenga con los clientes. Finalmente, al ajustar los precios, puede ver y aprobar los cambios antes de asignarlos en la contabilidad.  

## <a name="to-set-up-a-service-price-group"></a>Para configurar un grupo de precio de servicio
Puede configurar grupos que contienen productos de servicio que desee que reciban el mismo precio de servicio especial. Los grupos de precio de servicio se asignan a productos de servicio de líneas de producto de servicio. También puede asignar grupos de precio de servicio a grupos de producto de servicio.  

1. Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Grupos precio servicios** y, a continuación, seleccione el vínculo relacionado.  
2. Cree un grupo de precios de servicios nuevo.  
3. Rellene los campos **Código** y **Descripción**.  
4. Seleccione la acción **Configurar**.  
2. Rellene los campos según sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

 > [!Tip]
 > El **Tipo de ajuste** y el campo **Importe** trabajan juntos para especificar si un ajuste afecta a un importe fijo o sólo se aplica cuando el precio total del servicio supera o es menor que el importe del campo **Importe**.  

## <a name="to-set-up-a-service-price-adjustment-group"></a>Para configurar un grupo de ajuste de precios de servicio  
Puede configurar grupos de ajuste de precios para ajustar los precios de servicio de los productos de servicio. Por ejemplo, puede configurar grupos de ajuste de precio para ajustar el precio del flete o de piezas de repuesto.  
  
1. Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Grupos de ajuste de precios servicio** y, a continuación, seleccione el vínculo relacionado.  
2. Cree un grupo de ajuste de precios de servicio nuevo.  
3. Rellene los campos **Código** y **Descripción**.  
4. En el campo **Tipo**, especifique el tipo de entrada que desea ajustar.  
  
    * Para ajustar un movimiento específico, introduzca el número del movimiento en el campo **Nº** . Al dejar este campo en blanco, el grupo de ajuste ajustará todos los movimientos del tipo definido en el campo **Tipo**.  
    * Para ajustar los precios de servicio correspondientes a un servicio específico, rellene el campo **Tipo trabajo**. Cuando deje este campo en blanco, será ignorado.  
  
5. En el campo **Descripción**, introduzca una breve descripción del ajuste de precios de servicio.  
6. Para ajustar los precios de servicio relacionados con un grupo contable de producto general específico, rellene el campo **Grupo contable producto**.

> [!Tip]
> Puede elegir **Detalles** para agregar información adicional acerca del grupo de ajuste. Por ejemplo, puede especificar qué artículos pertenecen al grupo de ajuste de precio de servicio y si se trata de un artículo un recurso, un grupo de recursos o un cargo por servicio.  

## <a name="to-set-up-additional-costs-for-services"></a>Para configurar costes adicionales de servicios
Cuando trabaje con productos y órdenes de servicio, puede que tenga que registrar costes adicionales, como costes de viaje para determinadas zonas de servicio o tarifas iniciales. Cuando cree un pedido de servicio, puede insertar estos costes y se sumará una línea con el tipo **Coste** al pedido. Por otra parte, si desea liquidar el coste a todos los pedidos de servicio, puede configurar un coste predeterminado. Por ejemplo, si desea que siempre se liquide un gasto inicial.
  
### <a name="to-set-up-service-costs"></a>Para configurar costes de servicio
1. Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Costes de servicio** y, a continuación, seleccione el vínculo relacionado. 
2. Rellene los campos según sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

### <a name="to-specify-a-default-cost-for-service-orders"></a>Para especificar un coste predeterminado de los pedidos de servicio
1. Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Configuración del servicio** y, a continuación, seleccione el vínculo relacionado. 
2. En el campo **Cargo inicio ped. servicio**, seleccione el coste de servicio correspondiente.

## <a name="see-also"></a>Consulte también
[Configurar la gestión de servicios](service-setup-service.md)  
[Gestión de servicios](service-service.md)  

