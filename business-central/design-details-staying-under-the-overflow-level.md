---
title: "Detalles de diseño: Mantenimiento por debajo de los niveles de desbordamiento | Documentos de Microsoft"
description: "Cuando se usa Cdad. máxima y Cdad. fija reaprov., el sistema de planificación se centra en el inventario proyectado únicamente en el ciclo indicado. Esto significa que el sistema de planificación puede sugerir un suministro superfluo cuando se producen cambios de demanda negativa o de suministro positivo fuera del ciclo determinado."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
redirect_url: design-details-handling-reordering-policies
ms.translationtype: HT
ms.sourcegitcommit: caf7cf5afe370af0c4294c794c0ff9bc8ff4c31c
ms.openlocfilehash: a4a35cec571f1a0c7644fe937553d87007a9567e
ms.contentlocale: es-es
ms.lasthandoff: 11/22/2018

---
# <a name="design-details-staying-under-the-overflow-level"></a>Detalles de diseño: Mantenimiento por debajo de los niveles de desbordamiento
Cuando se usan políticas de cantidad máxima y cantidad fija, el sistema de planificación se centra en el inventario proyectado únicamente en el ciclo indicado. Esto significa que el sistema de planificación puede sugerir un suministro superfluo cuando se producen cambios de demanda negativa o de suministro positivo fuera del ciclo determinado. Si, por esta razón, se sugiere un aprovisionamiento superfluo, el sistema de planificación calcula qué cantidad de aprovisionamiento debe disminuirse (o eliminarse) para evitar un aprovisionamiento superfluo. Esta cantidad se denomina “nivel de desbordamiento.” El desbordamiento se comunica como una línea de planificación con una acción de **Cambiar cantidad. (salida)** o **Cancelar** y el mensaje de advertencia siguiente:  

*Atención: El inventario proyectado [xx] es superior al nivel de desbordamiento [xx] en la fecha de vencimiento [xx].*  

![Nivel de desbordamiento de inventario](media/supplyplanning_2_overflow1_new.png "Nivel de desbordamiento de inventario")  

##  <a name="calculating-the-overflow-level"></a>Cálculo del nivel de desbordamiento  
El nivel de desbordamiento se calcula de diferentes modos según la configuración de planificación.  

### <a name="maximum-qty-reordering-policy"></a>Directiva de reaprovisionamiento de cantidad máxima  
Nivel de desbordamiento = stock máximo  

> [!NOTE]  
>  Si existe una cantidad mínima pedido, se agregará de la siguiente forma: nivel de desbordamiento = inventario máximo + cantidad mínima pedido.  

### <a name="fixed-reorder-qty-reordering-policy"></a>Directiva de reaprovisionamiento Cdad. fija reaprov.  
Nivel de desbordamiento = cantidad a pedir + punto de pedido  

> [!NOTE]  
>  Si la cantidad mínima de pedido es más alta que el punto de pedido, se reemplazará de la siguiente forma: nivel de desbordamiento = cantidad a pedir + cantidad mínima de pedido.  

### <a name="order-multiple"></a>Múltiplo de pedido  
Si existe un múltiplo de pedido, se ajustará el nivel de desbordamiento para las directivas de reaprovisionamiento de cantidad máxima y cantidad fija de reaprovisionamiento.  

##  <a name="creating-the-planning-line-with-overflow-warning"></a>Crear la línea de planificación con advertencia de desbordamiento  
Cuando un suministro existente provoca que el inventario proyectado sea superior al nivel de desbordamiento al final de un ciclo, se crea una línea de planificación. Para advertir del posible suministro superfluo, la línea de planificación tiene un mensaje de advertencia, el campo **Aceptar mensaje acción** no está seleccionado y el mensaje de acción es Cancelar o Cambiar cdad.  

### <a name="calculating-the-planning-line-quantity"></a>Cálculo de la cantidad en la línea de planificación  
Cantidad de planificación de línea = cantidad de suministro actual – (inventario proyectado – nivel de desbordamiento)  

> [!NOTE]  
>  Como con todas las líneas de advertencia, se omitirá cualquier cantidad de pedido máximo y mínimo o múltiplo de pedido.  

### <a name="defining-the-action-message-type"></a>Definir el tipo de mensaje de acción  

-   Si la cantidad de la línea de planificación es superior a 0, el mensaje de acción es Cambiar cdad.  
-   Si la cantidad de la línea de planificación es igual o menor a 0, el mensaje de acción es Cancelar.  

### <a name="composing-the-warning-message"></a>Composición del mensaje de advertencia  
En el caso de desbordamiento, la página **Elementos planificación sin seguimiento** muestra un mensaje de advertencia con la siguiente información:  

-   Nivel de inventario proyectado que ha activado la advertencia  
-   Nivel de desbordamiento calculado  
-   Fecha de vencimiento del evento de suministro.  

Ejemplo: "El inventario proyectado 120 es superior al nivel de desbordamiento 60 el 28-01-11".  

## <a name="scenario"></a>Caso  
En este ejemplo, un cliente cambia un pedido de venta de 70 a 40 piezas entre dos ejecuciones de planificación. La característica de desbordamiento empieza a reducir la compra que se ha sugerido para la cantidad de venta inicial.  

### <a name="item-setup"></a>Configuración de producto  

|Política reaprov.|Cdad. máxima|  
|-----------------------|------------------|  
|Cantidad máxima pedido|100|  
|Punto pedido|50|  
|Existencias|80|  

### <a name="situation-before-sales-decrease"></a>Situación antes de la disminución de venta  

|Evento|Cambiar cdad.|Inventario proyectado|  
|-----------|-----------------|-------------------------|  
|Día uno|Ninguno|80|  
|Venta|-70|10|  
|Final del ciclo|Ninguno|10|  
|Sugerir nuevo pedido de compra|+90|100|  

### <a name="situation-after-sales-decrease"></a>Situación después de la disminución de venta  

|Cambiar|Cambiar cdad.|Inventario proyectado|  
|------------|-----------------|-------------------------|  
|Día uno|Ninguno|80|  
|Venta|-40|nº 40|  
|Compra|+90|130|  
|Final del ciclo|Ninguno|130|  
|Sugerir disminución de compra<br /><br /> pedido a partir de 90 a 60|-30|100|  

### <a name="resulting-planning-lines"></a>Líneas de planificación resultantes  
 Se crea una línea de planificación (advertencia) para reducir la compra con 30 de 90 a 60 para mantener el inventario proyectado en 100 según el nivel de desbordamiento.  

![Plan según el nivel de desbordamiento](media/nav_app_supply_planning_2_overflow2.png "Plan según el nivel de desbordamiento")  

> [!NOTE]  
>  Sin la característica de desbordamiento, no se crea ninguna advertencia si el nivel de inventario proyectado está por encima del inventario máximo. Esto podría provocar un suministro superfluo de 30.  

## <a name="see-also"></a>Consulte también  
[Detalles de diseño: Directivas de reaprovisionamiento](design-details-reordering-policies.md)   
[Detalles de diseño: Parámetros de la planificación](design-details-planning-parameters.md)   
[Detalles de diseño: Gestión de directivas de reaprovisionamiento](design-details-handling-reordering-policies.md)   
[Detalles de diseño: Planificación de aprovisionamiento](design-details-supply-planning.md)

