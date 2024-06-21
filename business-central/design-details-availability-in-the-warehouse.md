---
title: 'Detalles de diseño: Disponibilidad en el almacén'
description: Conozca los diferentes factores que afectan la disponibilidad de artículos en su almacén.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.date: 02/22/2023
ms.custom: bap-template
ms.service: dynamics-365-business-central
---
# <a name="design-details-availability-in-the-warehouse"></a>Detalles de diseño: Disponibilidad en el almacén

Esté al tanto de la disponibilidad de artículos para garantizar que los pedidos salientes fluyan de manera eficiente y que sus tiempos de entrega sean óptimos.  

La disponibilidad puede variar, dependiendo de varios factores. Por ejemplo:

* Asignaciones a nivel de ubicación cuando ocurren actividades de almacén, como selecciones y movimientos.
* Cuando el sistema de reservas de inventario impone restricciones a cumplir.

Antes de asignar cantidades a selecciones para los flujos de salida, [!INCLUDE [prod_short](includes/prod_short.md)] verifica que se cumplan todas las condiciones.

Cuando no se cumplen las condiciones, se muestran mensajes de error. Un mensaje típico es el genérico "No hay nada que manejar". . El mensaje se puede mostrar por muchas razones diferentes, en los flujos de entrada y salida, en los que una línea de documento contiene el campo **Cant. a manipular**.

## <a name="bin-content-and-reservations"></a>Contenido y reservas de ubicación

Las cantidades de artículos existen tanto como asientos de almacén como asientos de artículos en el inventario. Estos dos tipos de movimientos contienen información diversa sobre el lugar donde están los productos y si están disponibles. Los movimientos de almacén definen la disponibilidad de un producto por ubicación y tipo de ubicación, lo que se denomina contenido de ubicación. Los movimientos de producto definen la disponibilidad de un producto por su reserva para documentos de salida.  

[!INCLUDE [prod_short](includes/prod_short.md)] calcula la cantidad que está disponible para recoger cuando el contenido del contenedor se combina con las reservas.  

## <a name="quantity-available-to-pick"></a>Cantidad disponible para picking

[!INCLUDE [prod_short](includes/prod_short.md)] reserva artículos para envíos de órdenes de venta pendientes para que no se seleccionen para otras órdenes de venta que se envíen antes. [!INCLUDE [prod_short](includes/prod_short.md)] resta las cantidades de artículos que ya se están procesando, de la siguiente manera:

* Cantidades reservadas para otros documentos de salida.
* Cantidades en documentos de recolección existentes.
* Cantidades recolectadas pero aún no enviadas o consumidas.  

El resultado se calcula dinámicamente y se muestra en el campo **Cdad. a picking disponible** en la página **Hoja de trabajo de picking**. El valor también se calcula cuando los usuarios crean los picking de almacén directamente para los documentos de salida. Los siguientes son ejemplos de documentos de salida:

* Pedidos de venta
* Consumo de producción
* Transferencias de salida

El resultado está disponible en estos documentos en los campos de cantidad, como **Cantidad a manejar**.  

> [!NOTE]  
> Para la prioridad de las reservas, la cantidad que reservar se resta de la cantidad disponible para seleccionar. Por ejemplo, si la cantidad disponible en las ubicaciones de selección es 5 unidades, pero hay 100 unidades en ubicaciones de colocación, cuando reserve más de 5 unidades para otro pedido, aparecerá un mensaje de error, ya que la cantidad adicional debe estar disponible en ubicaciones de selección.  

### <a name="calculating-the-quantity-available-to-pick"></a>Cálculo de la cantidad disponible para seleccionar

[!INCLUDE [prod_short](includes/prod_short.md)] calcula la cantidad disponible para picking de la manera siguiente:  

cantidad disponible para picking = cantidad en ubicaciones de picking - cantidad en picking y movimientos – (cantidad reservada en ubicaciones de picking + cantidad reservada en picking y movimientos)  

En el diagrama siguiente se muestra los diferentes elementos del cálculo.  

![Disponible para picking con superposición de reservas.](media/design_details_warehouse_management_availability_2.png "Disponible para picking con superposición de reservas")  

## <a name="quantity-available-to-reserve"></a>Cantidad disponible para reservar

Dado que coexisten los conceptos de contenido y de reserva de ubicación, la cantidad de productos disponibles para reservar se debe alinear con las asignaciones hacia documentos de almacén de salida.  

Puede reservar todos los artículos de inventario, excepto los artículos para los que se ha iniciado el procesamiento de salida. La cantidad disponible para reservar se define como la cantidad en todos los documentos y todos los tipos de ubicación. Las siguientes cantidades de salida son excepciones:  

* Cantidad en documentos de picking no registrados  
* Cantidad en ubicaciones de envío  
* Cantidad en ubicaciones para producción  
* Cantidad en ubicaciones de aprovisionamiento manual  
* Cantidad en ubicaciones para ensamblado  
* Cantidad en ubicaciones de ajuste  

El resultado se muestra en el campo**Cantidad total disponible** en la página **Reservas**.  

En una línea de reserva, la cantidad que no se puede reservar, porque está asignada en el almacén, se muestra en el campo **Cant. asignada en Almacén** de la página **Reservas**.  

## <a name="check-whether-items-are-available-for-picking"></a>Verifique si los artículos están disponibles para ser recogidos

[!INCLUDE [inventory-availability-overview](includes/inventory-availability-overview.md)]

### <a name="calculating-the-quantity-available-to-reserve"></a>Cálculo de la cantidad disponible para reservar

[!INCLUDE [prod_short](includes/prod_short.md)] calcula la cantidad disponible para reservar de la manera siguiente:  

cantidad disponible para reserva = cantidad total en inventario - cantidad en picking y movimientos para documentos de origen - cantidad reservada - cantidad en ubicaciones de salida  

En el diagrama siguiente se muestra los diferentes elementos del cálculo.  

![Disponible para reserva por asignaciones de almacén.](media/design_details_warehouse_management_availability_3.png "Disponible para reserva por asignaciones de almacén")  

## <a name="see-also"></a>Consulte también

[Información general de Warehouse Management](design-details-warehouse-management.md)
[Consultar la disponibilidad de los productos](inventory-how-availability-overview.md)
[Realizar picking para producción, ensamblado o proyectos en una configuración avanzada de almacén](warehouse-how-to-pick-for-internal-operations-in-advanced-warehousing.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
