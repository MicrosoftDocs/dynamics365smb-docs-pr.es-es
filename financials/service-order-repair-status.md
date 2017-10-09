---
title: "Configuración de estados para órdenes y reparaciones de servicio | Documentos de Microsoft"
description: "Debe configurar nueve opciones de estado de reparación que identifican el progreso de la reparación y el mantenimiento de productos de servicio de pedidos de servicio."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 36925a08f7fdfffedf13902a5c6feaaa8b0929a4
ms.contentlocale: es-es
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-set-up-statuses-for-service-orders-and-repairs"></a>Configuración de estados para órdenes y reparaciones de servicio
Debe configurar opciones de estado de reparación que identifican el progreso de la reparación y el mantenimiento de productos de servicio de pedidos de servicio. Debe configurar como mínimo nueve opciones de estado de reparación que identifiquen situaciones o acciones realizadas durante el servicio de productos de servicio.  

Puede establecer el nivel de prioridad de las opciones de estado de pedido de servicio. Las cuatro prioridades son: Alta, Media alta, Media baja y Baja.  
  
Cuando se modifica el estado de reparación de un producto de servicio de un pedido de servicio, se actualiza el estado de la orden de servicio. El estado de reparación de cada producto de servicio se encuentra vinculado al estado de pedido de servicio. Si los productos de servicio se encuentran vinculados a dos o más opciones de estado de pedido de servicio, se selecciona el estado de pedido de servicio con la prioridad más alta.  

## <a name="to-set-up-a-repair-status"></a>Para configurar un estado de reparación  
1. Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Estado reparación** y, a continuación, seleccione el vínculo relacionado. 2. Cree un estado de reparación nuevo.  
3. Rellene los campos **Código** y **Descripción**.  
4. En el campo **Estado ped. servicio**, seleccione el estado de pedido para enlazar el estado de reparación. El campo **Prioridad** muestra la prioridad del estado de pedido de servicio seleccionado.  
5. Elegir un estado de reparación. Puede seleccionar solo uno.  
6. Para poder registrar pedidos de servicio que incluyan productos de servicio con este estado de reparación, elija el campo **Registro permitido**.  
7. Para poder cambiar manualmente la opción de estado de pedido de servicio a la opción **Pendiente** en pedidos de servicio que incluyan productos de servicio con este estado de reparación, elija el campo **Estado pendiente permitido**.  
8. Elija las casillas **Estado en proceso permitido**, **Estado terminado permitido** y **Estado en espera permitido** del mismo modo.
  
## <a name="to-set-up-service-status-priorities"></a>Para configurar prioridades de estado de servicio  
1. Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Estado pedido servicio** y, a continuación, seleccione el vínculo relacionado.  
2. Seleccione el estado de pedido de servicio para el que desea establecer la prioridad.  
3. En el campo **Prioridad**, seleccione la prioridad que desea para el estado de pedido de servicio. Repita este paso para cada estado.  
  
## <a name="see-also"></a>Consulte también  
[Descripción del estado de pedido de servicio y estado de reparación]()  
[Configurar la gestión de servicios](service-setup-service.md)  

