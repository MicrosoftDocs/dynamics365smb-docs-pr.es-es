---
title: 'Detalles de diseño: Cambiar la valoración de existencias para productos'
description: Aprenda a asignar una valoración de existencias diferente a un producto aunque ya lo haya usado en transacciones.
author: bholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: costing methods, costing, item cost
ms.search.form: 8645
ms.date: 06/08/2021
ms.author: bholtorf
ms.openlocfilehash: 5e7bbb28b35f31e21904006b6c595896bdca3f61
ms.sourcegitcommit: ef80c461713fff1a75998766e7a4ed3a7c6121d0
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 02/15/2022
ms.locfileid: "8148625"
---
# <a name="design-details-change-the-costing-method-for-items"></a>Detalles de diseño: Cambiar la valoración de existencias para productos

En [!INCLUDE[prod_short](includes/prod_short.md)], no puede cambiar una valoración de existencias para un producto después de haber incluido el producto en una transacción. Por ejemplo, después de haber comprado o vendido el producto. Si se asignó una valoración de existencias incorrecta al producto o productos, es posible que no identifique el problema hasta que haga su informe financiero.

Este tema describe cómo resolver esta situación. El enfoque recomendado es reemplazar el producto que tiene una valoración de existencias incorrecta con un producto nuevo, y usar un pedido de ensamblado para transferir el inventario del producto antiguo al nuevo.

> [!NOTE]
> El uso de pedidos de ensamblado permite que los costos sigan fluyendo, aunque haya facturas de compra pendientes o cargos de envío para contabilizar. Además, le permite deshacer la conversión y recuperar las cantidades de los productos originales, si es necesario.

> [!TIP]
> Para familiarizarse con el proceso, le recomendamos que comience el proceso de conversión con un solo elemento o un pequeño conjunto de elementos.

## <a name="about-costing-methods"></a>Acerca de la valoración de existencias

Los métodos de valoración de existencias controlan los cálculos de costes cuando se compran bienes, se reciben en inventario y se venden. Los métodos de valoración de existencias afectan a la planificación de las cantidades registradas en CV que afectan a los ingresos brutos. Es este flujo el que calcula el CV. El coste de productos vendidos (CV) y los ingresos se utilizan para determinar los ingresos brutos, de la siguiente manera:

*beneficio bruto* = *ingresos - CV*

Cuando configura productos de inventario, debe asignar una valoración de existencias. La valoración puede variar de una empresa a otra y de un producto a otro, por lo que es importante elegir la correcta. [!INCLUDE[prod_short](includes/prod_short.md)] admite las siguientes valoraciones de existencias:

* Promedio
* FIFO
* LIFO
* Estándar
* Específico

Para obtener más información, consulte [Detalles de diseño: Métodos de coste](design-details-costing-methods.md).

## <a name="using-assembly-orders-to-change-costing-method-assignments"></a>Usar pedidos de ensamblado para cambiar asignaciones de valoraciones de existencias

Esta sección describe los siguientes pasos para cambiar la valoración de existencias asignada a un producto:

1. Defina una valoración de existencias predeterminada.
2. Identifique los productos para los que cambiar la valoración de existencias y vuelva a numerarlos.
3. Cree nuevos productos con el antiguo esquema de numeración y copie los datos maestros en un lote.
4. Copie manualmente los datos maestros relacionados desde el producto existente al nuevo producto.
5. Determine la cantidad de inventario para convertir desde el producto original al nuevo producto.
6. Transfiera el inventario al nuevo producto.
7. Gestione las cantidades de inventario que se asignan a la demanda.
8. Bloquee el artículo original para su uso posterior.  

### <a name="define-a-default-costing-method"></a>Definir una valoración de existencias predeterminada

Para ayudar a evitar futuros errores, puede especificar una valoración de existencias predeterminada para nuevos artículos. Cada vez que alguien crea un nuevo producto, [!INCLUDE[prod_short](includes/prod_short.md)] sugerirá la valoración de existencias predeterminada. Usted especifica el método de valoración predeterminado en el campo **Valoración de existencias predeterminada** en la página **Config. Existencias**. 

### <a name="identify-the-items-to-change-the-costing-method-for-and-renumber-them"></a>Identificar los productos para los que cambiar la valoración de existencias y vuelva a numerarlos

Es posible que desee dar a sus nuevos productos los mismos números que los que están reemplazando. Para hacer eso, cambie los números de los productos existentes. Por ejemplo, si el número del producto existente es "P1000", puede cambiarlo a "X-P1000". Este es un cambio manual que debe realizar para cada producto.

### <a name="create-new-items-with-the-old-numbering-scheme-and-copy-the-master-data-in-a-batch"></a>Crear nuevos productos con el antiguo esquema de numeración y copiar los datos maestros en un lote

Cree los nuevos productos usando el esquema de números actual. Con la excepción del campo **Valoración de existencias**, los nuevos productos deben contener los mismos datos maestros que los productos existentes. Para transferir los datos maestros del producto y los datos relacionados de otras funciones, use la acción **Copiar producto** en la página **Ficha de producto**. Para obtener más información, consulte [Copiar productos existentes para crear productos nuevos](inventory-how-copy-items.md).

Después de crear los nuevos elementos y transferir los datos maestros, asigne la valoración de existencias correcta.

### <a name="manually-copy-related-master-data-from-the-original-item-to-the-new-item"></a>Copie manualmente los datos maestros relacionados desde el producto original al nuevo producto.

Para que los nuevos productos sean completamente útiles, debe copiar manualmente algunos datos maestros de otras áreas, como se describe en la siguiente tabla.

|Área  |Qué copiar  |Cómo copiarlo  |
|---------|---------|---------|
|Inventario |Unidades de almacenamiento (SKU) |Compruebe si se especifica una SKU para el producto original. Si se han introducido parámetros de planificación para cada tarjeta de SKU, debe crear manualmente el SKU para el nuevo producto. Si no se especifican los parámetros, puede usar el trabajo por lotes **Crear unidad de almacenamiento** en la página **Ficha de producto** para crear los datos.|
| |Sustituciones de producto |Compruebe si hay sustituciones de productos definidas para el producto original. Si las hay, transfiera esos datos al nuevo producto. Para ver elementos sustitutos, use la acción **Sustituciones** en la página **Ficha de producto**. |
| |Informes de análisis |Revise los informes Análisis de productos, Análisis de ventas y Análisis de compras. Para aquellos que hacen referencia a los productos originales, puede crear un nuevo informe de análisis con una referencia al nuevo producto (manteniendo el informe de análisis original para usar como historial) o ajustar los informes para que hagan referencia al nuevo producto. |
| |Diarios estándar |Compruebe si los diarios estándar hacen referencia al producto original y transfiera esos datos al nuevo producto cuando sea necesario. Esta información se encuentra en los diarios estándar, que están disponibles en el diario de productos.  |
|Ccial |Porcentajes prepago ventas | Compruebe si los porcentajes de prepago de ventas están definidos para el producto original y transfiera esos datos al nuevo producto. Para ver los porcentajes de prepago, en la página **Ficha de producto**, elija **Ventas** y después, **Porcentajes de prepago**.|
|Compra |Porcentajes prepago compra |Compruebe si los porcentajes de prepago de compras están definidos para el producto original y transfiera esos datos al nuevo producto. Para ver los porcentajes de prepago, en la página **Ficha de producto**, elija **Compras** y después, **Porcentajes de prepago**. |
|Almacén |Contenidos ubicación |Revise el contenido de ubicación definido para el producto original. Si se han especificado de forma individual columnas como Cant. mín, Cant. máx., Predeterminado y Dedicado, debe crear manualmente el contenido del contenido de ubicación para el nuevo producto. Si no es así, no se requiere ninguna acción. [!INCLUDE[prod_short](includes/prod_short.md)] mantendrá los registros cuando registre documentos de almacén y diarios.|
|Proyecto |Precios del proyecto |Compruebe si los precios del proyecto están definidos para el producto original y transfiera esos datos al nuevo producto. Esta información está disponible en la página **Ficha de producto** en a parte **Detalles proyecto - N.º precios** en el panel **Cuadro informativo**. |
|Servicio |Capacidad de recursos de servicio |Compruebe si las capacidades de recursos de servicio están definidas para el producto original y transfiera esos datos al nuevo producto. Para ver las capacidades de recursos del servicio, use la acción **Capacidades de recursos** en la página **Ficha de producto**.  |
| |Componentes del producto de servicio |Compruebe si los componentes están definidos para el producto de servicio original y transfiera esos datos al nuevo producto. Para ver los componentes del producto de servicio, en la página **Ficha de producto**, use la acción **Producto de servicio** para abrir la lista de productos de servicio relacionados y luego elija al acción **Componentes**.  |
|Producción |LM producción |Compruebe si alguna L.M. de producción contiene el producto original y reemplácela con el nuevo producto. Para reemplazar el producto original, en la página **L.M. de producción**, elija la acción **Cambiar producto en L.M. producción**. |
|Ensamblado |L.M. de ensamblado |Compruebe si hay alguna L.M. de producción que contenga el producto original y reemplácela manualmente con el nuevo producto. |

> [!IMPORTANT]
> Si el nuevo método de valoración de existencias es Estándar, debe especificar un valor en el campo **Coste estándar** en la página **Ficha de producto**. Puede usar la página **Hoja trab. coste estándar** para establecer los costes compartidos en consecuencia. Para obtener más información, consulte [Actualizar costes estándar](finance-how-to-update-standard-costs.md).

### <a name="determine-the-inventory-quantity-to-convert-from-the-original-item-to-the-new-item"></a>Determinar la cantidad de inventario para convertir desde el producto original al nuevo producto

> [!NOTE]
> Este paso no tiene en cuenta las cantidades que se incluyen en los pedidos no enviados. Para más información, vea [Gestionar las cantidades de inventario que se asignan a la demanda](design-details-changing-costing-methods.md#handle-inventory-quantities-that-are-allocated-to-demand). 

Use un diario de inventario físico para producir una lista de las cantidades en el inventario. Dependiendo de la configuración de ubicación del almacén, utilice uno de los siguientes:

* Diarios de inventario físico
* Almacén Diarios de inventario físico

Ambos diarios pueden calcular la cantidad de inventario del artículo, incluyendo el almacén, la variante, el contenedor y la ubicación de almacenamiento. Para obtener más información, consulte [Recuento, ajuste y reclasificación de inventario mediante diarios](inventory-how-count-adjust-reclassify.md).

### <a name="transfer-the-inventory-to-the-new-item"></a>Transferir el inventario al nuevo producto

Cree y registre pedidos de ensamblado para transferir el coste y la cantidad de inventario del producto original al nuevo producto. Los pedidos de ensamblado pueden convertir un artículo en otro mientras se conservan los costes. Esto ayuda a garantizar que los totales netos de la cuenta de inventario y los CV no se vean afectados (excepto cuando el nuevo método de valoración de existencias es Estándar, en cuyo caso los costoes pueden distribuirse a las cuentas de desviación). Para obtener más información, consulte [Gestión de ensamblado](assembly-assemble-items.md).

Al crear pedidos de ensamblado, use la información del diario de inventario físico o almacén. Diario de inventario físico Las siguientes tablas describen la información en los informes para especificar en el encabezado y las líneas en el pedido de ensamblado.

#### <a name="header"></a>Cabecera

|Campo  |Valor a especificar  |
|---------|---------|
|Nº producto |El número del producto nuevo. |
|Cantidad |La cantidad en el diario de inventario físico.<br> **NOTA**: Las cantidades calculadas por los diarios de inventario físico no incluyen las cantidades que se encuentran en pedidos que aún no se han enviado.  |
|Cód. variante |Igual que en el diario de inventario físico.  |
|Código de ubicación |Igual que en el diario de inventario físico. |
|Código de unidad de medida |Igual que en el diario de inventario físico. |
|Cód. ubicación |Igual que en el diario de inventario físico. |

#### <a name="lines"></a>Líneas

|Campo  |Valor a especificar  |
|---------|---------|
|Escriba |Producto |
|Nº |El número del producto original. |
|Cantidad por |1 |
|Cód. variante |Igual que en el diario de inventario físico. |
|Código de ubicación |Igual que en el diario de inventario físico. |
|Código de unidad de medida |Igual que en el diario de inventario físico. |

> [!NOTE]
> Un pedido de ensamblado puede gestionar solo un SKU de un artículo a la vez. Debe crear un pedido de ensamblado para cada combinación de SKU que tenga una cantidad en el inventario.

> [!NOTE]
> Para una ubicación de almacén, es posible que deba crear selecciones antes de poder publicar el pedido de ensamblado. Para investigar eso, revise la configuración para el picking en la página **Ficha de almacén**. Para más información, vea [Configurar productos y almacenes para ubicaciones y picking directos](warehouse-how-to-set-up-items-for-directed-put-away-and-pick.md).

### <a name="handle-inventory-quantities-that-are-allocated-to-demand"></a>Gestionar las cantidades de inventario que se asignan a la demanda

Lo idóneo es que el inventario para el producto original debería ponerse en cero después de transferir las cantidades de inventario. Sin embargo, puede haber pedidos pendientes, hojas de trabajo y diarios (consulte la tabla a continuación) que aún requieren una cantidad del producto original. La cantidad también podría bloquearse por una reserva o un seguimiento de producto.

**Ejemplo** Hay 1000 piezas en el inventario y 20 piezas están reservadas para un pedido de venta que aún no se ha enviado. En ese caso, puede decidir conservar las 20 piezas en el producto antiguo para que pueda satisfacer el pedido pendiente.

> [!NOTE]
> Hay áreas funcionales que pueden afectar la cantidad, como se enumera en la tabla a continuación, por lo que puede ser difícil encontrar la cantidad correcta. Para estar seguro, utilizando el ejemplo anterior, puede optar por conservar 100 piezas y transferir las 900 piezas restantes en su lugar. Otra forma de hacerlo sería procesar los documentos y los diarios para que solo queden unos pocos gestionables. Otra alternativa es transferir la cantidad completa al nuevo producto y luego transferir parte de la misma al producto original usando el pedido de ensamblado.

La siguiente tabla enumera áreas funcionales donde puede haber cantidades pendientes.

|Área  |Dónde buscar cantidades pendientes  |
|---------|---------|
|Ccial |Documentos de ventas, incluyendo pedidos, pedidos de devolución, facturas, presupuestos, pedidos abiertos y abonos |
|Inventario |Diarios de productos, reservas, seguimiento de producto y hoja de trabajo de coste estándar |
|Compra |Documentos de compras, incluyendo pedidos, pedidos de devolución, facturas, presupuestos, pedidos abiertos y abonos |
|Planificación |Hoja de demanda, hoja de planificación y planificación de pedidos |
|Almacén |Pedidos de transferencia, envíos de almacén, diarios de almacén y pickings de almacén, ubicaciones y movimientos, ubicación y picking internos y hojas de trabajo de creación de ubicación. |
|Ensamblado |Documentos de ensamblado, incluyendo pedidos, pedidos de devolución y pedidos abiertos |
|Proyectos |Líneas de planificación de proyecto y líneas del diario |
|Servicio |Documentos de servicio y contratos de servicio. |
|Producción |Orden de producción (planificadas, planificadas en firme y lanzadas) |

### <a name="block-the-original-item-from-further-use"></a>Bloquear el producto original para su uso posterior

Cuando el inventario del producto original es cero, puede bloquear el producto para evitar que se use en nuevas transacciones. Para bloquear el producto, en la página **Ficha de producto**, active el control de alternancia a **Bloqueado**. Para más información, vea [Bloquear productos de ventas o compras](inventory-how-block-items.md).

## <a name="summary"></a>Resumen

Cambiar el método valoración de existencias en productos que se han utilizado en transacciones es un proceso y no una acción estándar en [!INCLUDE[prod_short](includes/prod_short.md)]. Puede utilizar los pasos descritos en este tema como plantilla para el proceso.

El proceso puede llevar mucho tiempo porque hay varios pasos manuales. Sin embargo, si se toma su tiempo para completarlo, minimizará el impacto de los errores en su contabilidad.

Se recomienda lo siguiente:

1. Evalúe la viabilidad del proceso seleccionado uno o más productos representativos en todo el proceso.
2. Considere ponerse en contacto con un socio experimentado que pueda ayudarlo con el proceso.

## <a name="see-also"></a>Consulte también

[Detalles de diseño: Métodos de coste](design-details-costing-methods.md)  
[Panorama](design-details-inventory-costing.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]