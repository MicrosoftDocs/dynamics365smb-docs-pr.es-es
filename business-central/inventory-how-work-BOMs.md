---
title: Trabajar con listas de materiales para administrar componentes
description: Se crea una L.M. de ensamblado o una L.M. de producción para especificar los componentes o recursos necesarios para elaborar el producto al que representa la L.M.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.forms: 36, 5872, 5870, 5874, 911, 917, 912
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 1b0b3aa0813a4ede91232235b319e8bf72961e6c
ms.sourcegitcommit: 3acadf94fa34ca57fc137cb2296e644fbabc1a60
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 09/19/2022
ms.locfileid: "9529715"
---
# <a name="work-with-bills-of-material"></a>Trabajar con listas de materiales

Utilice listas de materiales (L.M.) para estructurar los productos principales que se deben montar o producir por los recursos o centros de máquinas de componentes. Una L.M. de ensamblado también se puede utilizar para vender un producto principal como un kit formado por sus componentes.

## <a name="assembly-boms-or-production-boms"></a>L.M. de ensamblado o L.M. de producción

Utilice los pedidos de ensamblado para crear productos finales de los componentes en un proceso sencillo que se pueda realizar por uno o varios recursos básicos, que no sean máquinas o centros de trabajo, o sin ningún recurso. Por ejemplo, un proceso de ensamblado podría ser el picking de dos botellas de vino y un saco de café y, después, empaquetarlo todo como artículo de regalo.  

Un L.M. de ensamblado es los datos maestros que definen qué artículos componentes forman un producto final ensamblado y que recursos se utilizan para ensamblar el artículo de ensamblado. Cuando introduzca un elemento de ensamblado una cantidad en una cabecera de un nuevo pedido de ensamblado, las líneas de pedidos de ensamblado se rellenan automáticamente en las L.M. de ensamblado con una línea de pedido de ensamblado por componente o recurso. Para obtener más información, consulte [Gestión de ensamblado](assembly-assemble-items.md).

Las L.M. de ensamblado se describen en este tema.

Utilice las órdenes de producción para crear los productos finales de los componentes en un proceso complejo que requiere una ruta de producción y un proyecto y centros de trabajo o de máquina, que representan las capacidades de producción. Por ejemplo, un proceso de producción podría ser cortar las placas de acero en una operación, soldarlas en la operación siguiente y pintar el producto final en la última operación. Para obtener más información, consulte [Fabricación](production-manage-manufacturing.md).  

Un L.M. de producción es los datos maestros que definen un producto y los componentes que entren ellos. Para los artículos de montaje, el L.M. de producción se debe certificar y asignar al producto antes de que se pueda utilizar en una orden de producción. Cuando introduzca el producto en una línea del orden de producción, manualmente o restaurando el pedido, el contenido del L.M. de producción se convertirá en los componentes de la orden de producción. Para obtener más información, consulte [Crear L.M. de producción](production-how-to-create-production-boms.md).  

El concepto de recursos de producción es mucho más avanzado que en administración de ensamblados. Los centros de trabajo y los de máquina funcionan como los recursos, y los pasos de una orden de producción se representan por las operaciones que se asignan a los recursos de las rutas de producción. Para obtener más información, consulte [Crear rutas](production-how-to-create-routings.md).

Los pedidos de ensamblado y las órdenes de producción se pueden relacionar directamente a los pedidos de venta. Sin embargo, solo podrá los pedidos de ensamblado para personalizar el producto final directamente para una solicitud de cliente con el pedido de venta.

## <a name="to-create-an-assembly-bom"></a>Para crear una L.M. de ensamblado

Para definir un producto principal que conste de otros productos y, potencialmente, de recursos necesarios para combinar el principal, debe crear una L.M. de ensamblado.  

Las L.M. de ensamblado normalmente contienen productos pero también pueden contener uno o varios recursos que son necesarios para que combinar el ensamblado.

Las L.M. de ensamblado pueden tener varios niveles, lo que significa que un componente de la L.M. de ensamblado puede ser un elemento del ensamblado en sí. En ese caso, el campo **L.M. de ensamblado** en la línea de L.M. de producto contiene **Sí**.

Se aplican requisitos especiales a los productos de la L.M. de ensamblado en lo que respecta a la disponibilidad. Para obtener más información, vea [Para consultar la disponibilidad de un producto por su uso en las L.M. de ensamblado](inventory-how-availability-overview.md#to-view-the-availability-of-an-item-by-its-use-in-assembly-or-production-boms).

Existen dos partes para crear una L.M. de ensamblado:
- Configuración de un producto nuevo
- Definición de la estructura de la lista de materiales del elemento del ensamblado.

1. Configure un producto nuevo. Para obtener más información, vea [Registrar nuevos productos](inventory-how-register-new-items.md).

    Continúe para introducir los componentes o recursos en la L.M. de ensamblado.  
2. En la página **Ficha producto** de un elemento del ensamblado, elija la acción **Ensamblado** y, a continuación, seleccione la acción **L.M. de ensamblado**.
3. En la página **L.M. de ensamblado**, rellene los campos según sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-edit-assembly-boms"></a>Para editar listas de materiales de ensamblado

Puede editar las líneas en una lista de materiales de ensamblado en cualquier momento. Pero tenga en cuenta que la lista de materiales puede estar en uso en ventas en curso o en ensamblados del elementos principal, que pueden verse afectados por el cambio. Elija la acción **Puntos-de-uso** para ver en qué productos se está utilizando y si los pedidos de venta o ensamblado pueden verse afectados.

1. Elija el icono ![Bombilla que abre la característica Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Productos**, y luego elija el enlace relacionado.
2. Elija el valor **Sí** valor en la columna **L.M. de ensamblado**.
3. En la página **L.M. de ensamblado** elija la acción **Editar lista** y luego cambie cualquier campo según sea necesario.

## <a name="to-view-components-and-resources-indented-according-to-the-bom-structure"></a>Para ver los componentes y recursos con sangría según la estructura de la L.M.

En la página **L.M. de ensamblado** puede abrir una página independiente que muestre que los componentes y cualquier recurso con sangría de acuerdo con la posición de la L.M. debajo del elemento del ensamblado.

1. Elija el icono ![Bombilla que abre la característica Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Productos**, y luego elija el enlace relacionado.
2. Abra la ficha de un elemento del ensamblado. (El campo **L.M. de ensamblado** de la página **Productos** contiene **Sí**).
3. En la página **Ficha producto**, elija la acción **Ensamblado** y, a continuación, seleccione la acción **L.M. de ensamblado**.
4. En la página **L.M. de ensamblado**, elija la acción **Mostrar L.M.**.

## <a name="to-replace-the-assembly-item-with-its-components-on-document-lines"></a>Para reponer el elemento del ensamblado por sus componentes en líneas de documento

Desde cualquier documento de venta y de compra que contenga el elemento de montaje, puede utilizar una función especial para reemplazar la línea del elemento de montaje con nuevas líneas para sus componentes. Esta función es útil, por ejemplo, si desea vender componentes como un kit que representa el elemento del ensamblado.

La acción **Pormenorizar L.M.** también está disponible en la página **L.M. de ensamblado** como método para ver elementos de subensamblado de una L.M. de ensamblado.

> [!CAUTION]  
>  Cuando haya utilizado la función **Desplegar L.M.**, no puede deshacerla fácilmente. Debe eliminar las líneas de pedido de venta que representan los componentes y después volver a introducir una línea de pedido de venta para el elemento del ensamblado.

El procedimiento siguiente se basa en una factura de ventas. Los mismos pasos se aplican a otros documentos de venta y a todos los documentos de compra.

1. Elija el icono ![Bombilla que abre la característica Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Facturas venta** y luego elija el enlace relacionado.
2. Abra una factura de venta que contenga una línea de elemento de ensamblado.
3. Seleccione la línea del elemento del ensamblado y, después, la acción de línea **Desplegar L.M.** 

Se vacían todos los campos de la línea de factura de ventas para el elemento de ensamblaje, salvo los campos **Producto** y **Descripción**. Se insertan las líneas completas de la factura de venta para los componentes y recursos posibles que componen el elemento de ensamblado.

> [!NOTE]
> El informe **Lista de picking por orden** también se cambia para mostrar solo los componentes. Esto significa que un trabajador de almacén que selecciona el artículo principal, el elemento del ensamblado, no lo verá en la lista de picking. Para más información, consulte [Imprimir la lista de selección](sales-how-print-picking-list.md).

## <a name="to-calculate-the-standard-cost-of-an-assembly-item"></a>Para calcular el coste estándar de un elemento de ensamblado

Se calcula el coste unitario de un elemento de ensamblado distribuyendo el coste unitario de cada componente y recurso de la L.M. de ensamblado del producto.

También puede calcular y actualizar el coste estándar de uno o varios productos en la página **Hoja trab. coste estándar**. Para obtener más información, consulte [Actualizar costes estándar](finance-how-to-update-standard-costs.md).  

El coste unitario de una L.M. de ensamblado equivale siempre al total de los costes unitarios de sus componentes, incluidas las L.M. de otros ensamblados y cualquier recurso.  

> [!NOTE]
> [!INCLUDE [bom-standard-cost](includes/bom-standard-cost.md)]

1. En la esquina superior derecha, seleccione el icono **Buscar página o informe**, escriba **Productos** y, a continuación, seleccione el enlace relacionado.
2. Abra la ficha de un elemento del ensamblado. (El campo **L.M. de ensamblado** de la página **Productos** contiene **Sí**).
3. En la página **Ficha producto**, elija la acción **Ensamblado** y, a continuación, seleccione la acción **L.M. de ensamblado**.
4. En la página **L.M. de ensamblado**, seleccione la acción **Calc. Coste estándar**.
5. Seleccione una de las siguientes opciones y haga clic en el botón **Aceptar**.

|Opción |Description |
|-------|------------|
|**Nivel superior**|Calcula el coste estándar del elemento de ensamblado como el coste total de todos los productos comprados o ensamblados en esta L.M. de ensamblado sin importar cualquier L.M de ensamblado subyacente.|
|**Todos los niveles**|Calcula el coste estándar prod producto como la suma de: 1) El coste calculado de todas las L.M. de ensamblados subyacentes de la L.M. de ensamblado. 2) El coste de todos los productos comprados de la L.M. de ensamblado.|



Los costes de los productos que conforman la L.M. de ensamblado se copian de las fichas de productos componente. El coste de cada producto se multiplica por la cantidad, y el coste total se muestra en el campo **Coste unitario** en la ficha elemento de ensamblado.

## <a name="see-related-microsoft-training"></a>Consultar la [formación de Microsoft](/training/modules/set-up-assembly-items-dynamics-365-business-central/) relacionada

## <a name="see-also"></a>Consulte también .

[Registro de productos nuevos](inventory-how-register-new-items.md)  
[Consultar la disponibilidad de los productos](inventory-how-availability-overview.md)  
[Inventario](inventory-manage-inventory.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
