---
title: 'Detalles de diseño: Disponibilidad en el almacén | Documentos de Microsoft'
description: El sistema debe mantener un control constante de la disponibilidad de productos el almacén, para que los pedidos de salida puedan fluir de un modo eficaz y proporcionar las entregas óptimas.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/08/2021
ms.author: edupont
ms.openlocfilehash: 7d23dc10ffb215ee2ac160c9ec9b9fd1ddb5cc2d
ms.sourcegitcommit: a7cb0be8eae6ece95f5259d7de7a48b385c9cfeb
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 07/08/2021
ms.locfileid: "6442540"
---
# <a name="design-details-availability-in-the-warehouse"></a>Detalles de diseño: Disponibilidad en el almacén
El sistema debe mantener un control constante de la disponibilidad de productos el almacén, para que los pedidos de salida puedan fluir de un modo eficaz y proporcionar las entregas óptimas.  

La disponibilidad varía en función de las asignaciones en el nivel de ubicación cuando tienen lugar actividades de almacén, como selección y movimientos, y cuando el programa de reservas de inventario impone restricciones. Un algoritmo bastante complejo comprueba que todas las condiciones se cumplan antes de asignar cantidades a selecciones para los flujos de salida.

Si no se cumplen una o más condiciones, se pueden mostrar diferentes mensajes de error, incluyendo el mensaje genérico "Nada a manipular." . El mensaje "Nada a manipular." puede producirse por muchas razones diferentes, en los flujos de entrada y salida, en los que una línea de documento directa o indirectamente implicada contiene el campo **Cant. a manipular**.

> [!NOTE]
> Pronto se publicará aquí información sobre posibles razones y soluciones para el mensaje "Nada a manipular." .

## <a name="bin-content-and-reservations"></a>Contenido y reservas de ubicación  
 En cualquier instalación de gestión de almacén, hay cantidades de productos, tanto como entradas de almacén, en el área de aplicación del almacén, como entradas contables de productos, en el área de aplicación del inventario. Estos tipos dos tipos de movimiento contienen información diversa sobre el lugar donde están los productos y si están disponibles. Los movimientos de almacén definen la disponibilidad de un producto por ubicación y tipo de ubicación, lo que se denomina contenido de ubicación. Los movimientos de producto definen la disponibilidad de un producto por sus documentos de reserva a salida.  

 Existe una funcionalidad especial en el algoritmo de picking para calcular la cantidad que hay disponible para picking cuando el contenido de ubicación está acoplado con las reservas.  

## <a name="quantity-available-to-pick"></a>Cantidad disponible para picking  
 Si, por ejemplo, el algoritmo de selección no tiene en cuenta las cantidades del producto que están reservadas para un envío de pedido de venta pendiente, entonces los productos se pueden seleccionar para otro pedido de venta que se envíe antes, lo que impide satisfacer las primeras ventas. Para evitar esta situación, el algoritmo de picking resta las cantidades que están reservadas para otros documentos de salida, las cantidades de los documentos de picking existentes y las cantidades de las que se realiza el picking pero aún no se han enviado o consumido.  

 El resultado se muestra en el campo **Cdad. a picking disponible** en la página **Hoja de trabajo de picking**, donde el campo se calcula dinámicamente. El valor también se calcula cuando los usuarios crean los picking de almacén directamente para los documentos de salida. Dichos documentos de salida podrían ser pedidos de venta, consumo de producción o transferencias de salida, donde el resultado se refleja en los campos de cantidad relacionados, **Cdad. a manipular**.  

> [!NOTE]  
>  En relación con la prioridad de las reservas, la cantidad que reservar se resta de la cantidad disponible para seleccionar. Por ejemplo, si la cantidad disponible en las ubicaciones de selección es 5 unidades, pero hay 100 unidades en ubicaciones de colocación, cuando se intente reservar más de 5 unidades para otro pedido, aparecerá un mensaje de error, ya que la cantidad adicional debe estar disponible en ubicaciones de selección.  

### <a name="calculating-the-quantity-available-to-pick"></a>Cálculo de la cantidad disponible para seleccionar  
 La cantidad disponible para picking se calcula de la manera siguiente:  

 cantidad disponible para picking = cantidad en ubicaciones de picking - cantidad en picking y movimientos – (cantidad reservada en ubicaciones de picking + cantidad reservada en picking y movimientos)  

 En el diagrama siguiente se muestra los diferentes elementos del cálculo.  

 ![Disponible para picking con superposición de reservas.](media/design_details_warehouse_management_availability_2.png "Disponible para picking con superposición de reservas")  

## <a name="quantity-available-to-reserve"></a>Cantidad disponible para reservar  
 Dado que coexisten los conceptos de contenido y de reserva de ubicación, la cantidad de productos disponibles para reservar se debe alinear con las asignaciones hacia documentos de almacén de salida.  

 Debe ser posible reservar todos los productos del inventario, excepto los que han iniciado el proceso de salida. Por consiguiente, la cantidad disponible para reservar se define como la cantidad en todos los documentos y todos los tipos de ubicación, excepto las cantidades de salida siguientes:  

-   Cantidad en documentos de picking no registrados  
-   Cantidad en ubicaciones de envío  
-   Cantidad en ubicaciones para producción  
-   Cantidad en ubicaciones de aprovisionamiento manual  
-   Cantidad en ubicaciones para ensamblado  
-   Cantidad en ubicaciones de ajuste  

 El resultado se muestra en el campo **Cantidad total disponible** en la página **Reservas**.  

 En una línea de reserva, la cantidad que no se puede reservar, porque está asignada en el almacén, se muestra en el campo **Cant. asignada en Almacén** de la página **Reservas**.  

### <a name="calculating-the-quantity-available-to-reserve"></a>Cálculo de la cantidad disponible para reservar  
 La cantidad disponible para reservar se calcula de la manera siguiente:  

 cantidad disponible para reserva = cantidad total en inventario - cantidad en picking y movimientos para documentos de origen - cantidad reservada - cantidad en ubicaciones de salida  

 En el diagrama siguiente se muestra los diferentes elementos del cálculo.  

 ![Disponible para reserva por asignaciones de almacén.](media/design_details_warehouse_management_availability_3.png "Disponible para reserva por asignaciones de almacén")  

## <a name="see-also"></a>Consulte también  
 [Detalles de diseño: Warehouse Management](design-details-warehouse-management.md)  
 [Consultar la disponibilidad de los productos](inventory-how-availability-overview.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]