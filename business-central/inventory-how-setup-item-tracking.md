---
title: 'Configurar el seguimiento de productos con números de serie, de lote y de paquete'
description: 'Configurar el seguimiento de productos con números de serie, de lote y de paquete'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 08/31/2021
ms.author: bholtorf
---
# <a name="set-up-item-tracking-with-serial-lot-and-package-numbers"></a>Configurar el seguimiento de productos con números de serie, de lote y de paquete

Realice un seguimiento de los productos de inventario incluso en configuraciones de almacén complejas con números específicos para cada producto, ya sea como un objeto individual, como un lote o como un paquete. Con el seguimiento de productos, puede realizar un seguimiento de los productos en los movimientos internos del almacén y en los documentos de entrada y salida.

Los números de serie y lote de productos se pueden seguir, ya sea hacia adelante o hacia atrás, en la cadena de suministro. Esto es útil para asegurarse de la calidad general y para la recuperación de productos. Para obtener más información, consulte [Realizar un seguimiento de productos marcados para seguimiento](inventory-how-to-trace-item-tracked-items.md).  

> [!TIP]
> En 2021, el lanzamiento de versiones 1 y posteriores, active la actualización de la característica *Uso de seguimiento por número de paquete en el sistema de reservas y seguimiento* si desea trabajar con números de paquete, así como con números de serie y de lote. Para obtener más información, consulte [Habilitación de las próximas actualizaciones de antemano](admin-feature-management.md). Una vez que la característica está activada, puede asignar números de paquete a documentos de entrada y salida de forma similar a como puede trabajar con números de lote.  

## <a name="numbers-and-item-tracking"></a>Seguimiento de números y productos

Como parte de los procesos de su almacén, puede agrupar sus existencias en paquetes, cajas, contenedores, etc. Pero, para realizar un seguimiento de los productos, asigna números únicos como identificación. Por ejemplo, fabrica y vende una silla que tiene el número de producto *1900-S*. Cada silla individual tiene un número de serie, *1001*, pero también agrupa cuatro sillas en un lote, *LOT0001*, y envía las sillas en un contenedor con el número de paquete *CONTENEDOR010* que también incluye otros productos, como *LOTE0100* con mesas auxiliares, y *LOTE200* con lámparas.  

Dependiendo de su configuración, usa estos números diferentes para realizar un seguimiento del inventario en [!INCLUDE [prod_short](includes/prod_short.md)] en las distintas etapas de compras, ventas, operaciones de almacén, etc.

## <a name="to-set-up-item-tracking-codes"></a>Para configurar códigos de seguimiento de producto

Un código de seguimiento de producto refleja las distintas consideraciones que tiene una empresa en referencia al uso de números de serie y lote de los productos que se mueven en el inventario.  

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Códs. seguim. prod.**, y luego elija el enlace relacionado.  
2. Seleccione la acción **Nuevo**.
3. Rellene los campos según sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
4. En las fichas desplegables **Nº serie**, **Nº lote** y **Nº paquete**, defina las directivas de seguimiento del producto mediante números de serie, lote y paquete, respectivamente.  

> [!NOTE]  
> Si desea rastrear elementos específicos o lotes específicos a lo largo de su vida útil, debe elegir los campos **Seguim. NS específ.** y **Seguim. lote específ.**, respectivamente. Como resultado, al manejar una unidad de salida de un artículo con este código de seguimiento de artículos, siempre debe especificar qué número de serie existente o qué número de lote existente debe gestionar. Esto significa que al vender una unidad del producto, debe liquidarse con un grupo específico de números de serie o de lote en las existencias. Es decir, un número de serie o de lote asignado al producto cuando entra en el inventario debe seguir hasta que sale del mismo.

Ya que este campo cubre todas las transacciones posibles con el producto, los campos de entrada y salida individuales también estarán seleccionados. No obstante, no hay que hacer nada con los campos de entrada y salida individuales en las existencias, ya que sólo definen el flujo de trabajo de su empresa cuando se asignan números de seguimiento de producto.  

> [!NOTE]  
> Para asignar números de seguimiento de producto en las actividades de almacén, los campos de verificación **Seguim. nº serie almacén** y **Control lote almacén** se deben seleccionar en la ficha del código del seguimiento del producto.  

## <a name="to-set-up-expiration-rules-for-serial-or-lot-numbers"></a>Para configurar las reglas de caducidad para números de serie o lote

Con algunos productos es posible que le interese configurar fechas y reglas de caducidad específicas en el código de seguimiento de producto. Esta funcionalidad le permite realizar un seguimiento de la caducidad de determinados números de serie y de lote.

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Códs. seguim. prod.**, y luego elija el enlace relacionado.
2. Seleccione un código de seguimiento de productos existentes, y después la acción **Editar** .  
3. En la ficha desplegable **Varios**, seleccione los campos siguientes.  

    |Campo|Descripción|  
    |---------------------------------|---------------------------------------|  
    |**Registro caducidad requerido**|Especifica que, cuando el producto salga del inventario, debe respetarse la fecha de caducidad asignada al número de seguimiento de producto tal como se introdujo en el inventario.|  
    |**Requerir entrada fecha caducidad**|Especifica que debe introducirse una fecha de caducidad en la línea de seguimiento de producto.|  
    |**Usar fechas de caducidad**|Especifica que desea calcular las fechas de caducidad. |  

## <a name="to-set-up-warranties-for-serial-or-lot-numbers"></a>Para configurar garantías para números de serie o lote

Con algunos productos es posible que le interese configurar garantías específicas en el código de seguimiento de producto. Esta funcionalidad le permite realizar un seguimiento de la caducidad de las garantías de determinados números de serie o lote en inventario.  

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Códs. seguim. prod.**, y luego elija el enlace relacionado.  
2. Seleccione un código de seguimiento de productos existentes, y después la acción **Editar** .  
3. En la ficha desplegable **Varios**, rellene el campo **Fórmula fecha garantía** y seleccione los campos según se indica a continuación:  

    |Campo|Descripción|  
    |---------------------------------|---------------------------------------|  
    |**Fórmula fecha garantía**|Especifica el último día de garantía para el producto.|  
    |**Requerir entrada fecha garantía**|Especifica que debe introducir manualmente una fecha de garantía en la línea de seguimiento del producto.|  


## <a name="to-set-up-items-for-tracking-with-the-correct-item-tracking-codes"></a>Para configurar los productos para el seguimiento con los códigos de seguimiento de productos correctos

Para habilitar el seguimiento de productos, primero debe asignar los códigos de seguimiento de productos a un producto. Hay dos formas de agregar códigos de seguimiento de productos, seleccionando el código de una lista predefinida o asignando un nuevo código único. Pase el cursor sobre los campos para leer una breve descripción.

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Producto**, y luego elija el enlace relacionado.
2. Seleccione un elemento existente de la lista y abra la página **Tarjeta de producto**.  
3. En la ficha desplegable **Seguimiento de producto**, asigne los códigos de seguimiento de productos apropiados y elija el **Código de seguimiento del producto**, los **Números de serie**, y los **Números de lote**.
    1. También puede crear un nuevo código de seguimiento de producto seleccionando la acción **Nuevo**.

## <a name="to-specify-opening-balances-for-the-items-you-track"></a>Para especificar saldos iniciales para los productos que sigue

Puede crear saldos iniciales para los productos que sigue. Dado que puede elegir diferentes configuraciones de almacén, hay dos opciones:

* Habilite lotes específicos en la página **Diario productos** para permitir que las personas ingresen datos de serie, lote y paquete directamente en las líneas del diario.
* Para lugares donde el control de alternancia **ubicación y picking directos** está activado, utilice la página **Diario de inventario físico de almacén** para que todos los campos de seguimiento de artículos estén disponibles. Los campos que están disponibles incluyen los campos **Fecha de garantía** y **Fecha de caducidad**.

### <a name="item-journals"></a>Diarios de productos

1. Elija el icono ![Bombilla que abre la característica Dígame](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Diarios de productos**, y luego elija el enlace relacionado.
2. Seleccione el campo **Nombre** para abrir una lista de secciones del diario de productos.
3. Elija **Nuevo** para crear un nuevo lote y luego active el control de alternancia **Seguim. prod. en líneas**.
4. Elija **Aceptar** para seleccionar el lote que creó.
5. Rellene los campos en la línea del diario de productos según sea necesario. Tenga en cuenta que los campos **Nº lote**, **Nº de serie**, **Fecha de caducidad**, **Fecha de garantía** y **N.° de paquete** están disponibles (si la función está habilitada).
6. Elija la acción **Registrar** para ajustar inventario.

> [!NOTE] 
> [!INCLUDE [prod_short](includes/prod_short.md)] hace algunas validaciones menores cuando ingresa o importa datos. Se produce una comprobación más completa cuando contabiliza o transfiere datos de líneas de diario a la ventana **Líns. seg. prod.**. Esto último sucede automáticamente cuando abre la página **Líns. seg. prod.** desde la línea del diario de productos o si elige la acción **Actualizar líns. seguim. prod.**.

### <a name="warehouse-physical-inventory-journal-for-locations-where-directed-pick-and-put-away-is-turned-on"></a>Diario de inventario físico de almacén para ubicaciones donde están activados la ubicación y el picking directos

1. Elija el icono ![Bombilla que abre la característica Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Diario de inventario físico de almacén** y luego elija el enlace relacionado.
2. Rellene los campos en la línea del diario de productos según sea necesario. Tenga en cuenta que los campos **Nº lote**, **Nº de serie**, **Fecha de caducidad**, **Fecha de garantía** y **N.° de paquete** están disponibles (si la función está habilitada).
3. Seleccione la acción **Registrar** para realizar ajustes de inventario. Recuerde, debe sincronizar los movimientos ajustados de almacén con los correspondientes movimientos de producto. Para obtener más información, vaya a [sincronizar las entradas de almacén ajustadas](/dynamics365/business-central/inventory-how-count-adjust-reclassify#to-synchronize-the-adjusted-warehouse-entries-with-the-related-item-ledger-entries).

Para importaciones masivas, use paquetes de configuración para importar datos a los diarios.

> [!NOTE]
> No puede usar **Editar en Excel** para crear líneas de diario con información de seguimiento.

## <a name="see-also"></a>Consulte también .

[Trabajar con números de lote y de serie](inventory-how-work-item-tracking.md)  
[Seguir producto - Productos seguidos](inventory-how-to-trace-item-tracked-items.md)  
[Inventario](inventory-manage-inventory.md)  
[Detalles de diseño: Seguimiento de productos](design-details-item-tracking.md)  
[Detalles de diseño: Seguimiento de productos y reservas](design-details-item-tracking-and-reservations.md)  
[Reservar artículos](inventory-how-to-reserve-items.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
