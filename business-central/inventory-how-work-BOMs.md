---
title: Trabajar con listas de materiales
description: Se crea una L.M. de ensamblado o una L.M. de producción para especificar los componentes o recursos necesarios para elaborar el producto al que representa la L.M.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'bills of material, assembly BOM, production BOM,'
ms.search.form: null
ms.date: 09/26/2022
ms.author: a-reishima
---
# <a name="work-with-bills-of-material" />Trabajar con listas de materiales

Utilice listas de materiales (L.M.) para estructurar los productos principales que se deben montar a partir de otros productos o producir a través de centros de recursos o máquinas de componentes.

## <a name="assembly-boms-or-production-boms" />L.M. de ensamblado o L.M. de producción

[!INCLUDE[prod_short](includes/prod_short.md)] admite dos tipos diferentes de listas de materiales:

| Tipo de L.M. | Categoría general | Ejemplo |
| -------- | ---------------- | ------- |
| [L.M. de ensamblado](assembly-how-work-assembly-boms.md) | Almacén/ensamblado | Productos que están formados por otros productos, ensamblados con recursos básicos o sin recursos. |
| [L.M. de producción](production-how-to-create-production-boms.md) | Fabricación/producción | Productos formados por diferentes componentes y subensamblajes, producidos en un centro de trabajo o máquinas. |

Utilice los pedidos de ensamblado para crear productos finales de los componentes en un proceso sencillo que se pueda realizar por uno o varios recursos básicos, que no sean máquinas o centros de trabajo, o sin ningún recurso. Por ejemplo, un proceso de ensamblado podría ser el picking de dos botellas de vino y un saco de café y, después, empaquetarlo todo como artículo de regalo.  

Un L.M. de ensamblado es los datos maestros que definen qué artículos componentes forman un producto final ensamblado y que recursos se utilizan para ensamblar el artículo de ensamblado. Cuando introduzca un elemento de ensamblado una cantidad en una cabecera de un nuevo pedido de ensamblado, las líneas de pedidos de ensamblado se rellenan automáticamente en las L.M. de ensamblado con una línea de pedido de ensamblado por componente o recurso. Obtenga más información en [Administración de ensamblados](assembly-assemble-items.md).

Utilice las órdenes de producción para crear los productos finales de los componentes en un proceso complejo que requiere una ruta de producción y un proyecto y centros de trabajo o de máquina, que representan las capacidades de producción. Por ejemplo, un proceso de producción podría ser cortar las placas de acero en una operación, soldarlas en la operación siguiente y pintar el producto final en la última operación. Obtenga más información en [Fabricación](production-manage-manufacturing.md).

Un L.M. de producción es los datos maestros que definen un producto y los componentes que entren ellos. Para los artículos de montaje, el L.M. de producción se debe certificar y asignar al producto antes de que se pueda utilizar en una orden de producción. Cuando introduzca el producto en una línea del orden de producción, manualmente o restaurando el pedido, el contenido del L.M. de producción se convertirá en los componentes de la orden de producción. Obtenga más información en [Crear L.M. de producción](production-how-to-create-production-boms.md).

El concepto de recursos de producción es mucho más avanzado que en administración de ensamblados. Los centros de trabajo y los de máquina funcionan como los recursos, y los pasos de una orden de producción se representan por las operaciones que se asignan a los recursos de las rutas de producción. Obtenga más información en el artículo [Creación de rutas](production-how-to-create-routings.md).

Los pedidos de ensamblado y las órdenes de producción se pueden relacionar directamente a los pedidos de venta. Sin embargo, solo podrá los pedidos de ensamblado para personalizar el producto final directamente para una solicitud de cliente con el pedido de venta.

## <a name="see-also" />Consulte también .

[Trabajar con L.M. de ensamblado](assembly-how-work-assembly-boms.md)  
[Crear LM de producción](production-how-to-create-production-boms.md)  
[Registro de productos nuevos](inventory-how-register-new-items.md)  
[Administrar variantes de productos](inventory-item-variants.md)  
[Inventario](inventory-manage-inventory.md)  
[Fabricación](production-manage-manufacturing.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
