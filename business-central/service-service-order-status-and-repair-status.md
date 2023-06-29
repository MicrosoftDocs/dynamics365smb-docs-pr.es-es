---
title: Estado de pedido de servicio y estado de reparación
description: El estado de pedido de servicio indica el estado de reparación de todos los productos de servicio del pedido de servicio.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 04/01/2021
ms.author: edupont
---
# <a name="service-order-status-and-repair-status"></a><a name="service-order-status-and-repair-status"></a><a name="service-order-status-and-repair-status"></a>Estado de pedido de servicio y estado de reparación

El campo **Estado** de la página **Pedido servicio** y el estado de reparación del producto de servicio, que se representa en el campo **Código estado reparación** de la página **Pedido servicio** están relacionados en Gestión servicios. El estado de pedido de servicio indica el estado de reparación de todos los productos de servicio del pedido de servicio.  

> [!NOTE]  
> Estos dos campos de estado no están relacionados con el campo **Estado lanzamiento** de la cabecera del pedido de servicio, que determina el modo en que el almacén controla los productos de servicio.  

Cada vez que se modifica el estado de reparación de un producto de servicio en un pedido, se actualiza el estado del pedido. Para mostrar el estado que indica el estado de reparación general de cada producto de servicio, deberá especificar la siguiente información:  

* El estado de pedido de servicio al que está vinculado cada estado de reparación.  
* El nivel de prioridad de cada opción de estado de pedido de servicio.  

Cuando se convierte una oferta de servicio en un pedido, cambia el estado de reparación de cada producto de servicio del pedido a **Inicial** y el estado del pedido de servicio cambia a **Pendiente**.  

> [!NOTE]
> Antes de poder crear órdenes de servicio, debe configurar estados de reparación y prioridades de estado de servicio. Para obtener más información, vea [Configurar estados para pedidos de servicio y reparaciones](service-order-repair-status.md).

## <a name="specifying-service-order-status-for-repair-status"></a><a name="specifying-service-order-status-for-repair-status"></a><a name="specifying-service-order-status-for-repair-status"></a>Especificar el estado de pedido de servicio para el estado de reparación

Cada estado de reparación se encuentra vinculado a un estado de pedido de servicio determinado. Las opciones para el estado de la orden de servicio son las siguientes:

* **Pendiente**
* **En proceso**
* **Esperar**
* **Terminada**

Las opciones de estado de reparación son las siguientes:

* **Inicial**
* **En proceso**
* **Remitido**
* **Parcialmente servido**
* **Oferta terminada**
* **Esperando al cliente**
* **Componente pedido**
* **Componente recibido**
* **Terminada**  

### <a name="pending"></a><a name="pending"></a><a name="pending"></a>Pendiente

El estado de pedido de servicio **Pendiente** indica que el servicio puede iniciarse o continuar en cualquier momento. Por lo tanto, las opciones de estado de reparación **Inicial**, **Remitido**, **Parcialmente servido** y **Componente recibido** pueden vincularse a este estado de pedido de servicio.  

### <a name="in-process"></a><a name="in-process"></a><a name="in-process"></a>En proceso

El estado de pedido de servicio **En proceso** indica que el servicio está en curso. Por lo tanto, las opciones de estado de reparación **En proceso** y **Componente pedido** pueden vincularse a este estado de pedido de servicio. Si vincula el estado **Componente pedido** al estado **En proceso** de un pedido de servicio, también deberá vincular el estado **Componente recibido** a este estado de pedido de servicio.  

### <a name="on-hold"></a><a name="on-hold"></a><a name="on-hold"></a>Esperar

El estado de pedido de servicio **En espera** indica que el servicio se encuentra retenido de forma temporal a la espera de una respuesta del cliente o de componentes para que pueda iniciarse el servicio. Por lo tanto, las opciones de estado de reparación **Oferta terminada**, **Componente pedido** y **Esperando al cliente** pueden vincularse a este estado de pedido de servicio.  

### <a name="finished"></a><a name="finished"></a><a name="finished"></a>Terminada

El estado de pedido de servicio **Terminado** indica que se ha completado el servicio. Por lo tanto, el estado de reparación **Terminado** está vinculado a este estado.  

## <a name="assigning-priority-to-service-order-status"></a><a name="assigning-priority-to-service-order-status"></a><a name="assigning-priority-to-service-order-status"></a>Asignar prioridad al estado de pedido de servicio

Cuando se modifica el estado de reparación de un producto de servicio, se identifican las opciones de estado de pedido de servicio vinculadas a las distintas opciones de estado de reparación de todos los productos de servicio del pedido. Si los productos de servicio se encuentran vinculados a dos o más opciones de estado de pedido de servicio, se selecciona la opción del estado de pedido de servicio con la prioridad más alta.  

Deberá decidir qué estado de pedido de servicio contiene la información más importante acerca del estado del pedido de servicio y asignar la prioridad más alta a ese estado, y así sucesivamente.  

Luego, cuando crea una nueva orden de servicio y le agrega elementos de servicio, el campo **Prioridad** en el encabezado de la orden de servicio se actualiza según las prioridades de los artículos de servicio.  

### <a name="example"></a><a name="example"></a><a name="example"></a>Ejemplo:

Un ejemplo típico de asignación de nivel de prioridad podría ser:  

* En proceso: Alta  
* Pendiente: Media alta  
* En espera: Media baja  
* Terminado: Baja  

Por ejemplo, si un producto de servicio tiene el estado de reparación **Inicial**, vinculado al estado de pedido de servicio **Pendiente**, otro producto tiene el estado **En proceso**, vinculado al estado de pedido de servicio **En proceso**, y el tercer producto tiene el estado **Componente pedido**, vinculado al estado de pedido de servicio **En espera**, el estado de pedido de servicio resultante será **En proceso**, porque tiene la prioridad más alta.  

## <a name="see-also"></a><a name="see-also"></a><a name="see-also"></a>Consulte también

[Configuración de estados para órdenes y reparaciones de servicio](service-order-repair-status.md)  
[Configurar la gestión de servicios](service-setup-service.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
