---
title: Descripción de los tipos de productos
description: Conozca los tipos de artículos que puede gestionar en el inventario y cómo le afectan los tipos. Puede ajustar la valoración de inventario de un producto utilizando los métodos de costes FIFO o Promedio cuando los costes de producto cambien por motivos distintos de las transacciones.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: null
ms.search.form: '9297, 5845, 30,'
ms.date: 05/24/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# Acerca de los tipos de productos

En el campo **Tipo** en la página **Ficha de producto**, puede seleccionar para qué se usa el producto en su negocio, lo que afecta al grado en el que puede administrar el producto en el inventario. La siguiente tabla enumera y describe los tres tipos de elementos que están disponibles.

|Opción|Propósito típico|
|------|-----------|
|Inventario|Cosas físicas, como bicicletas, teléfonos y escritorios, para las que desea poder utilizar todos los procesos de inventario. Los artículos de inventario puede incluir elementos no físicos, como licencias de software y suscripciones, si los elementos tienen números de identificación, como números de serie. Puede realizar un seguimiento completo de los valores y la disponibilidad de los artículos en el inventario.|
|No inventariado|Por lo general, los artículos que no están en el inventario son cosas físicas, como tornillos o bolígrafos, que una empresa consume pero que no desea realizar un seguimiento completo en el inventario. Por ejemplo, porque son artículos de bajo coste y solo se usan internamente.|
|Servicio|Una unidad de tiempo de trabajo, como una hora de consultoría, para soporte comercial limitado.|

> [!NOTE]
> Los tipos de **Servicio** y **No inventario** no le permiten realizar un seguimiento de la cantidad y el valor del inventario. Solo se admiten los tipos y las características de transacción de los elementos seleccionados. La siguiente table enumera las características que admiten los tres tipos de productos.

|Tipo de producto|Ccial|Compra|Consumo de proyecto|Consumo de servicio|Consumo de ensamblado|Producción Consumo|Salida de ensamblado|Salida de producción|Transferencia de ubicación|Recuento físico|Revalorización de inventario|Inventario y valoración|Seguim. prod.|Reserva|Gestión de almacén|Planific.|Planificación de pedidos|
|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|
|Grupos contables inventario|Sí|Sí|Sí|Sí|Sí|Sí|Sí|Sí|Sí|Sí|Sí|Sí|Sí|Sí|Sí|Sí|Sí|
|No inventariado|Sí|Sí|Sí|Sí|Sí|Sí|No|No|No|No|No|No|No|No|No|No|Sí|
|Servicio|Sí|Sí|Sí|N.º|N.º|N.º|N.º|N.º|N.º|N.º|N.º|N.º|N.º|N.º|N.º|N.º|Sí|

## Valoración de existencias para tipos de productos

Cuando publica transacciones de inventario, las cambios en la cantidad y en los valores del inventario se registran en los movimientos de producto y los movimientos de valores respectivamente.

Puede registrar el coste de productos de inventario en el campo **Importe coste (Real)** en la página **Movimientos de valor**. Cuando concilia la entrada en el libro mayor, el coste se muestra en el campo **Coste regis. en contab**. Para obtener más información sobre el coste de las existencias, vaya a [Detalles de diseño: coste de inventario](design-details-inventory-costing.md).

Para los productos que no son de inventario y los productos de servicio, el coste se registra en el campo **Importe coste (No-invent.)** en la página **Movimientos de valor**. Para los productos que no son de inventario y los productos de servicio, especifique el coste en los documentos y diarios de ventas, ensamblado y producción. Especifique el coste predeterminado en el campo **Coste unitario** en las páginas **Ficha de producto** y **Unidad de almacenamiento**. Los costes de este tipo de productos no se concilian con la contabilidad.

## Productos de catálogo y de servicio

Puede configurar productos que ofrezca a sus clientes pero que no administre hasta que los venda como productos de catálogo. Aunque los artículos del catálogo son similares a los productos normales del tipo **Sin inventario** en este sentido, no los confunda porque existen diferencias. Para obtener más información, vaya a [Trabajar con productos del catálogo](inventory-how-work-nonstock-items.md).

Los productos de los clientes con los que realiza el servicio, como una impresora, se denominan productos de servicio. Los productos de servicio no tienen nada que ver con artículos regulares o del catálogo. Sin embargo, los componentes del servicio pueden ser productos regulares. Para obtener más información, vaya a [Configurar componentes de servicio y de productos](service-how-setup-service-items.md).

## Consulte también

[Registro de productos nuevos](inventory-how-register-new-items.md)  
[Configurar inventario](inventory-setup-inventory.md)  
[Gestión de costes de inventario](finance-manage-inventory-costs.md)  
[Inventario](inventory-manage-inventory.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
