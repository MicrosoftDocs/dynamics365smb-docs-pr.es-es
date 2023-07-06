---
title: 'Detalles de diseño: Tabla de asignación de planificación'
description: Este tema proporciona información sobre lo que sucede cuando un cambio en los patrones de oferta o demanda requiere que calcule cómo planifica un artículo.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 06/15/2021
ms.author: edupont
---
# <a name="design-details-planning-assignment-table"></a><a name="design-details-planning-assignment-table"></a><a name="design-details-planning-assignment-table"></a><a name="design-details-planning-assignment-table"></a>Detalles de diseño: Tabla de asignación de planificación
Todos los productos se deben planificar; no obstante, no hay razón para calcular un plan para un producto a menos que haya habido un cambio en el patrón de demanda o de aprovisionamiento desde la última vez que se calculó un plan.  

Si el usuario ha introducido un nuevo pedido de venta o ha cambiado uno existente, existen motivos para volver a calcular el plan. Entre otros motivos se incluye un cambio en la previsión o en el stock de seguridad deseado. Un cambio en una lista de materiales mediante la adición o eliminación de un componente indicaría probablemente un cambio, pero para el producto componente solo.  

En el caso de ubicaciones múltiples, la asignación se realiza en el nivel de producto por combinación de almacén. Si, por ejemplo, se ha creado un pedido de venta en solo una ubicación, la aplicación asignará el producto a esa ubicación específica para planificar.  

El motivo para seleccionar productos para la planificación es cuestión de rendimiento del sistema. Si no se ha producido ningún cambio en el patrón de demanda-aprovisionamiento de un producto, el sistema de planificación no sugerirá ninguna acción. Sin la asignación de planificación, el sistema tendría que realizar cálculos para todos los productos a fin de averiguar para qué debe planificar y lo que agotaría los recursos del sistema.  

La tabla **Asignar planificación** supervisa los eventos de demanda y aprovisionamiento y asigna los productos adecuados para realizar la planificación. Se supervisan los eventos siguientes:  

* Un nuevo pedido de venta, previsión, componente, pedido de compra, orden de producción, pedido de ensamblado o pedido de transferencia.  
* Cambio de un pedido, cantidad, almacén, variante o fecha en un pedido de venta, previsión, componente, pedido de compra, orden de producción, pedido de ensamblado o pedido de transferencia.  
* Cancelación de un pedido de venta, previsión, componente, pedido de compra, orden de producción, pedido de ensamblado o pedido de transferencia.  
* El consumo de productos distintos de los planificados.  
* Salida de productos distintos de los planificados.  
* Cambios en inventario no planificados.  

Para estas desubicaciones de aprovisionamiento y demanda directos, el sistema de mensajes de acción y de seguimiento de pedidos mantiene la tabla de asignación de planificación e indica una causa de planificación como mensaje de acción.  

Los siguientes cambios en los datos maestros también pueden provocar un desequilibrio de planificación:  

* Cambio del estado a certificado en cabecera de L.M. de producción (para todos los productos con esa cabecera).  
* Línea eliminada (producto secundario).  
* Cambio del estado a certificado en cabecera de ruta (para todos los productos con esa ruta).  
* Cambios en los campos de ficha de producto siguientes.  
* Stock de seguridad o plazo de seguridad.  
* Plazo entrega (días).  
* Punto de pedido.  
* Número de L.M. de producción (y todos los elementos secundarios de referencia de la L.M. anterior).  
* Nº ruta  
* Directiva reaprov.  

En estos casos, una nueva función, la de gestión de planificación de asignaciones, mantiene la tabla e indica la causa de la planificación como Saldos periodo.  

Los siguientes cambios no provocan una asignación de planificación:  

* Calendarios  
* Otros parámetros de planificación en la ficha de producto  

Al calcular un MPS o un MRP, se aplican las siguientes restricciones:  

* MPS: el sistema de planificación comprueba que el producto incluye una previsión de demanda o un pedido de venta. Si no, el producto no se incluye en el plan.  
* MRP: si el sistema de planificación detecta que el producto se repone mediante una línea de planificación MPS o un pedido de suministro MRP, el producto quedará fuera de la planificación. No obstante, se incluyen las demandas de los componentes relevantes.  

## <a name="see-also"></a><a name="see-also"></a><a name="see-also"></a><a name="see-also"></a>Consulte también
[Detalles de diseño: Equilibrio de aprovisionamiento y demanda](design-details-balancing-demand-and-supply.md)   
[Detalles de diseño: Gestión de directivas de reaprovisionamiento](design-details-handling-reordering-policies.md)   
[Detalles de diseño: Transferencias en planificación](design-details-transfers-in-planning.md)   
[Detalles de diseño: Parámetros de la planificación](design-details-planning-parameters.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
