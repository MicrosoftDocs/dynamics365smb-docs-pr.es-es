---
title: "Recuento, ajuste y reclasificación de inventario | Documentos de Microsoft"
description: "Describe cómo realizar recuento físico, hacer ajustes negativos o positivos y cómo cambiar la información, como la ubicación o el número de lote, en las entradas de los movimientos o del almacén."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: adjustment, negative, positive, increase, decrease
ms.date: 06/02/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: db79c257585fe89237ef4e8d61fa49ce46ec682f
ms.contentlocale: es-es
ms.lasthandoff: 07/07/2017


---
# <a name="how-to-count-adjust-and-reclassify-inventory"></a>Recuento, ajuste y reclasificación de inventario
Como mínimo una vez cada año fiscal, debe realizar un inventario físico (es decir, contar todos los productos del inventario) para ver si la cantidad registrada en la base de datos es la misma que la cantidad física real en los almacenes. Una vez se sepa la cantidad física, debe registrarse en la contabilidad como parte de la evaluación del inventario de final de periodo.

Aunque cuente todos los productos del inventario una vez al año, puede que haya decidido contar algunos productos con mayor frecuencia, quizás porque son más valiosos o porque se fluctúan muy rápido y forman una gran parte del negocio. Con este fin, puede asignar períodos de recuento especiales a esos elementos. Para obtener más información, consulte la sección “Realizar el recuento cíclico”.

Si es necesario ajustar las cantidades de inventario registradas, por motivos de recuento u otros, puede usar un diario de productos para cambiar las entradas de contabilidad del inventario sin registrar las transacciones de negocio. Como alternativa, puede ajustar un solo artículo en la tarjeta de artículo.

Si necesita cambiar los atributos de las entradas de contabilidad de los productos, así como las cantidades, puede usar el diario de reclasificación de productos. Los atributos susceptibles de reclasificación más habituales son los números de lote/serie, las fechas de caducidad y las dimensiones.

## <a name="to-perform-a-physical-inventory"></a>Realizar un inventario físico
Es necesario llevar un inventario físico, es decir, hacer un recuento de los productos reales disponibles, para comprobar que la cantidad registrada coincida con la cantidad física en stock al final del ejercicio, o con mayor frecuencia. Si existen diferencias, debe registrarlas en las cuentas de producto antes de realizar la valoración de las existencias.

Aparte de la tarea de recuento físico, el proceso completo implica las tres tareas siguientes:

- Calcular el inventario previsto.
- Imprimir el informe que va utilizar para el recuento.
- Introducir y registrar el inventario contado real.

### <a name="to-calculate-the-expected-inventory"></a>Para calcular el inventario previsto
1. Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Diarios de inventario físico** y, a continuación, seleccione el vínculo relacionado.
2. Elija la acción **Calcular inventario**.
3. En la ventana **Calcular inventario**, especifique las condiciones que desea utilizar para crear las líneas de diario, como si desea incluir los productos que tienen un inventario registrado de cero.
4. Establezca filtros si solo desea calcular el inventario para productos, ubicaciones, almacenes o dimensiones determinados.
5. Elija el botón **Aceptar**.

> [!NOTE]  
>   Se procesan los movimientos de producto según los datos especificados y se crean las líneas en el diario de inventario físico. Tenga en cuenta que el campo **Cdad. (stock físico)** se rellena automáticamente con la misma cantidad que figura en el campo **Stock calculado**. Con esta función, no hace falta que especifique el recuento de existencias disponibles para productos cuya cantidad coincida con el stock calculado. Sin embargo, si la cantidad contada difiere de lo que se especifica en el campo **Stock calculado**, debe sobregrabarlo con la cantidad contada realmente.

### <a name="to-print-the-report-used-when-counting"></a>Para imprimir el informe utilizado para el recuento.
1. En la ventana **Diario inventario físico** que contiene el inventario previsto calculado, elija la acción **Imprimir**.
2. En la ventana **Lista inventario físico**, especifique si el informe debe mostrar el stock calculado y si el informe debe indicar los productos de inventario por números de serie o lote.
3. Establezca filtros si solo desea imprimir el informe para productos, ubicaciones, almacenes o dimensiones determinados.
4. Elija el botón **Imprimir**.

Los empleados pueden ahora proceder a contar el inventario y registrar las discrepancias en el informe impreso.

### <a name="to-enter-and-post-the-actual-counted-inventory"></a>Para introducir y registrar el inventario contado real
1. En cada línea de la ventana **Diario inventario físico**, donde el inventario real disponible, según lo determinado por el recuento físico, difiere de la cantidad calculada, introduzca el inventario real disponible en el campo **Cdad. (stock físico)**.

    Los campos relacionados se actualizan según corresponda.

    > [!NOTE]  
>   Si el recuento físico revela diferencias, producidas por productos que se registraron con códigos de almacén incorrectos, no introduzca las diferencias en el diario de inventario físico. En su lugar, utilice el diario de reclasificación o un pedido de transferencia para redirigir los productos a los almacenes correctos. Para obtener más información, consulte Reclasificación producto. Diario o Creación de pedidos de transferencia.

2. Para ajustar las cantidades calculadas a las cantidades contadas reales, elija la acción **Registrar**.

    Se crean los movimientos de producto y los movimientos del inventario físico. Abra la ficha del producto para ver los movimientos del inventario físico resultantes.

3. Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Productos** y, a continuación, seleccione el vínculo relacionado.
4. Para verificar el recuento del inventario, abra la ficha del producto en cuestión y, a continuación, elija la acción **Movimientos del inventario físico**.

# <a name="to-perform-cycle-counting"></a>Realizar el recuento cíclico
Aunque cuente todos los productos del inventario una vez al año, puede que haya decidido contar algunos productos con mayor frecuencia, quizás porque son más valiosos o porque se fluctúan muy rápido y forman una gran parte del negocio. Con este fin, puede asignar períodos de recuento especiales a esos elementos.

> [!NOTE]  
>   Si la ubicación se ha configurado para ubicación y picking directos, utilice en primer lugar la ventana **Almacén. Fís. Invent. diario** y, a continuación, la función **Calcular ajuste almacén** en la ventana **Diario del artículo**.

## <a name="to-set-up-counting-periods"></a>Para configurar periodos de recuento
El inventario físico se realiza normalmente en intervalos de tiempo periódicos, por ejemplo, mensualmente, trimestralmente o anualmente. Puede definir los periodos de recuento de inventario necesario.

Configure los periodos de recuento de inventario que desee utilizar y, a continuación, asigne uno a cada producto. Al realizar un inventario físico y utilizar **Calcular periodo recuento** en el diario de inventario físico, las líneas de los elementos se crean automáticamente.

1. Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Períodos recuento inventario físico** y, a continuación, seleccione el vínculo relacionado.  
2. Rellene los campos según sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-assign-a-counting-period-to-an-item"></a>Asignar un periodo de recuento a un producto  
1. Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Productos** y, a continuación, seleccione el vínculo relacionado.  
2. Seleccione el producto al que desea asignar un periodo de recuento.  
3. En el campo **Cód. perio. recuento inv. fís.**, seleccione el periodo de recuento correspondiente.  
4. Elija el botón **Sí** para cambiar el código y para calcular el primer periodo de recuento del artículo. La próxima vez que seleccione calcular un periodo de recuento en el diario de inventario físico, el producto aparecerá como una línea en la ventana **Selección prod. invent. fís.** Ya puede empezar a contar el producto periódicamente.

## <a name="to-initiate-a-count-based-on-counting-periods"></a>Iniciar un recuento basado en períodos de recuento
1. Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Diario de inventario físico** y, a continuación, seleccione el vínculo relacionado.
2. Elija la acción **Calcular periodo de recuento**.

    Se abrirá la ventana **Selección prod. invent. fís.** y mostrará los productos para los que se han asignado los periodos de recuento que es necesario contar, según sus periodos de recuento.
3. Realizar un inventario físico. Para obtener más información, consulte la sección "Realizar un inventario físico".

## <a name="to-adjust-the-inventory-of-one-item"></a>Ajustar el inventario de un producto
Una vez realizado un recuento físico de un productos en el área de inventario, puede utilizar la función **Ajustar inventario** para registrar la cantidad real del inventario.

1. Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Productos** y, a continuación, seleccione el vínculo relacionado.
2. Seleccione el producto para el que quiere ajustar el inventario y, a continuación, elija la acción **Ajustar inventario**.
3. En el campo **Nuevo inventario**, escriba la cantidad de inventario que desea registrar para el producto.
4. Elija el botón **Aceptar**.

El inventario de producto ahora está ajustado. La nueva cantidad se muestra en el campo **Inventario actual** en la ventana **Ajustar inventario** y en el campo **Inventario** de la ventana **Ficha de producto**.

También puede usar la función **Ajustar inventario** como una manera sencilla de incluir los productos comprados en el inventario si no usa facturas o pedidos de compra para registrar las compras. Para obtener más información, consulte [Procedimiento: Registrar compras](purchasing-how-record-purchases.md).

> [!NOTE]  
>   Una vez que haya ajustado el inventario, debe actualizarlo con el valor calculado actual. Para obtener más información, vea [Revaluación de inventario](inventory-how-revalue-inventory.md).

## <a name="to-adjust-the-inventory-quantity-of-one-or-more-items"></a>Ajustar la cantidad de inventario de uno o varios productos
En la ventana **Diario productos**, puede publicar transacciones de artículos directamente para ajustar el inventario en relación con compras, ventas y ajustes positivos o negativos sin utilizar documentos.

Si utiliza con frecuencia el diario de productos para registrar líneas de diario iguales o parecidas, por ejemplo, relacionadas con el consumo de materiales, puede utilizar la ventana **Diario productos estándar** para hacer más fácil este trabajo repetitivo. Para obtener más información, consulte la sección "Diarios estándar" en [Trabajar con diarios generales](ui-work-general-journals.md).

1. Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Diarios producto** y, a continuación, seleccione el vínculo relacionado.
2. Rellene los campos según sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Seleccione la acción **Registrar** para realizar ajustes de inventario.

> [!NOTE]  
>   Una vez que haya ajustado el inventario, debe actualizarlo con el valor calculado actual. Para obtener más información, vea [Revaluación de inventario](inventory-how-revalue-inventory.md).

## <a name="to-reclassify-an-items-lot-number"></a>Reclasificar el número de lote de un producto
1. Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Diarios reclas. producto** y, a continuación, seleccione el vínculo relacionado.
2. En la ventana **Diarios reclasif. producto**, rellene los campos según sea necesario.
3. En el campo **N.º lote** introduzca el número de lote actual de los productos.
4. En el campo **N.º lote nuevo** introduzca el número de lote nuevo de los productos.
5. Seleccione la acción **Registrar**.

## <a name="see-also"></a>Consulte también
[Inventario](inventory-manage-inventory.md)  
[Ventas](sales-manage-sales.md)  
[Compras](purchasing-manage-purchasing.md)  
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

