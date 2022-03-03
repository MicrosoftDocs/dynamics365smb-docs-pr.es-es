---
title: Descripción de los tipos de productos
description: Puede ajustar la valoración de inventario de un producto utilizando los métodos de costes FIFO o Promedio cuando los costes de producto cambien por motivos distintos de las transacciones.
documentationcenter: ''
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.search.form: 9297, 5845, 30,
ms.date: 06/16/2021
ms.author: edupont
ms.openlocfilehash: e902068398a636b5e205fa7d808066861059b901
ms.sourcegitcommit: ef80c461713fff1a75998766e7a4ed3a7c6121d0
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 02/15/2022
ms.locfileid: "8131696"
---
# <a name="about-item-types"></a>Acerca de los tipos de productos
En el campo **Tipo** en la página **Ficha de producto**, puede seleccionar para qué se usa el producto en su negocio, lo que afecta al grado en el que puede administrar el producto en el inventario. La siguiente tabla enumera y describe los tres tipos de elementos que están disponibles.

|Opción|Propósito típico|
|------|-----------|
|Inventario|Cosas físicas, como bicicletas, teléfonos y escritorios, para las que desea poder utilizar todos los procesos de inventario. Esto también puede incluir elementos no físicos, como licencias de software y suscripciones, si los elementos tienen números de identificación, como números de serie. Puede realizar un seguimiento completo de los valores y la disponibilidad de los artículos en el inventario.|
|No inventario|Por lo general, los artículos que no están en el inventario son cosas físicas, como tornillos o bolígrafos, que una empresa consume pero que no desea realizar un seguimiento completo en el inventario. Por ejemplo, porque son artículos de bajo coste y solo se usan internamente.|
|Servicio|Una unidad de tiempo de trabajo, como una hora de consultoría, para soporte comercial limitado.|

> [!NOTE]
> Los tipos de **Servicio** y **No inventario** no admiten el seguimiento de la cantidad y el valor del inventario. Solo se admiten los tipos y las características de transacción de los elementos seleccionados.

La siguiente table enumera las características que admiten los tres tipos de productos.

|Tipo de producto|Ccial|Compra|Consumo de proyecto|Consumo de servicio|Consumo de ensamblado|Producción Consumo|Salida de ensamblado|Salida de producción|Transferencia de ubicación|Recuento físico|Revalorización de inventario|Inventario y valoración|Seguim. prod.|Reserva|Gestión de almacén|Planificación|
|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|
|Grupos contables inventario|Sí|Sí|Sí|Sí|Sí|Sí|Sí|Sí|Sí|Sí|Sí|Sí|Sí|Sí|Sí|Sí|
|No inventario|Sí|Sí|Sí|Sí|Sí|Sí|N.º|N.º|N.º|N.º|N.º|N.º|No|No|No|No|
|Servicio|Sí|Sí|Sí|No|No|No|No|No|No|No|No|No|No|No|No|No|

## <a name="costing-methods-for-types-of-items"></a>Valoración de existencias para tipos de productos
Cuando publica transacciones de inventario, las cambios en la cantidad y en los valores del inventario se registran en los movimientos de producto y los movimientos de valores respectivamente. 

Para los artículos de inventario, el coste se registra en el campo **Importe de coste (real)** en la página **Movimientos de valor**, y cuando se concilia con la contabilidad, el coste se mostrará en el campo **Coste regis. en contab.**. Para obtener más información, consulte [Detalles de diseño: valoración de inventario](design-details-inventory-costing.md).

Para los productos que no son de inventario y los productos de servicio, el coste se registra en el campo **Importe coste (No-invent.)** en la página **Movimientos de valor**. Para los productos que no son de inventario y los productos de servicio, el coste se especifica en los documentos y diarios de ventas, ensamblado y producción. El coste predeterminado se puede especificar en el campo **Coste unitario** en las páginas **Ficha de producto** y **Unidad de almacenamiento**. Los costes de este tipo de productos no se concilian con la contabilidad. 

## <a name="catalog-and-service-items"></a>Productos de catálogo y de servicio
Los productos que ofrece a sus clientes pero que no desea administrar en su sistema hasta que comience a venderlos se pueden configurar como productos del catálogo. Los productos del catálogo no deben confundirse con artículos regulares de tipo No inventario. Para obtener más información, consulte [Trabajar con productos del catálogo](inventory-how-work-nonstock-items.md).

Los productos de los clientes con los que realiza el servicio, como una impresora, se denominan productos de servicio. Los productos de servicio no tienen nada que ver con artículos regulares o del catálogo. Sin embargo, los componentes del servicio pueden ser productos regulares. Para obtener más información, consulte [Configurar componentes de servicio y de productos](service-how-setup-service-items.md).

## <a name="see-also"></a>Consulte también
[Registro de productos nuevos](inventory-how-register-new-items.md)  
[Configurar inventario](inventory-setup-inventory.md)  
[Gestión de costes de inventario](finance-manage-inventory-costs.md)  
[Grupos contables inventario](inventory-manage-inventory.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]