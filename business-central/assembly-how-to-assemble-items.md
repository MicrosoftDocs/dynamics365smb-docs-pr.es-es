---
title: Ensamblar artículos
description: Obtenga más información sobre los procesos de ensamblaje bajo pedido y ensamblaje para existencias en Business Central.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.service: dynamics-365-business-central
ms.topic: how-to
ms.date: 11/23/2022
ms.search.keywords: 'kit, kitting'
ms.search.form: '900, 901, 902, 903, 904, 907, 910, 916, 920, 921, 922, 923, 940, 941, 942, 930, 931, 932, 914, 915, 905'
ms.custom: bap-template
---
# <a name="assemble-items"></a>Ensamblar artículos

Si el campo **Sistema reposición** en la ficha del artículo contiene **Montaje**, el método predeterminado para suministrar el artículo será ensamblarlo de acuerdo con la L.M. de ensamblado y potencialmente por un recurso definido. Obtenga más información en [Trabajar con L.M. de ensamblado](assembly-how-work-assembly-boms.md). Obtenga más información acerca de cómo configurar un elemento del ensamblado en [Comprender Ensamblar para pedido y Ensamblar para stock](assembly-assemble-to-order-or-assemble-to-stock.md).

Puede configurar elementos de ensamblado para dos procesos de ensamblado diferentes.

|Procesar  |Descripción  |
|---------|---------|
|Ensamblar para stock     | Artículos que ensambla y almacena para futuras ventas. Por ejemplo, kits para una próxima campaña de ventas. Los artículos no están relacionados con un pedido de ventas, al menos no todavía. Por lo general, estos elementos no se personalizan para las solicitudes de los clientes.        |
|Ensamblar para pedido     | Artículos que no desea almacenar. Por ejemplo, porque se personalizan según los pedidos de los clientes o para reducir el costo del inventario disponible. |
  
Este artículo describe la configuración estándar para ensamblar para stock. Sin embargo, puede haber otras formas que sean más adecuadas para su negocio. Obtenga más información en [Venta de productos de inventario en los flujos de ensamblar para pedido](assembly-how-to-sell-assemble-to-order-items-and-inventory-items-together.md) y [Venta de productos de ensamblado para pedido y productos de inventario juntos](assembly-how-to-sell-assemble-to-order-items-and-inventory-items-together.md).

> [!NOTE]  
> Los componentes de ensamblaje se manejan de forma especial en configuraciones básicas de almacén. Obtenga más información en [Tratamiento de productos de ensamblar para pedido con los picking de inventario](warehouse-how-to-pick-items-with-inventory-picks.md#handling-assemble-to-order-items-with-inventory-picks).

## <a name="to-assemble-an-item-to-stock"></a>Para ensamblar un artículo para stock

Siga los pasos de este procedimiento para ensamblar un artículo para almacenar. Para obtener más información sobre ensamblar por pedido, vaya a [Vender artículos ensamblados por pedido](assembly-how-to-sell-items-assembled-to-order.md).

1. Elija el icono ![Bombilla que abre la característica Dígame](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Pedidos ensamblado** y luego elija el enlace relacionado.  
2. Seleccione la acción **Nuevo**. Se abrirá la página **Nuevo pedido de ensamblado**.  
3. Rellene los campos según sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. En el campo **Nº producto**, introduzca el número del producto que desea ensamblar. Puede seleccionar artículos que están configurados para ensamblaje y tienen una lista de materiales para ensamblaje o artículos sin una lista de materiales para ensamblaje. Este último es útil para montajes no planificados o escenarios en los que desea utilizar la reclasificación de artículos y realizar un seguimiento de los costos.  
5. En el campo **Cantidad**, especifique cuántas unidades del artículo desea que se ensamblen.  

    > [!NOTE]  
    >  Si uno o más componentes no están disponibles para satisfacer la cantidad en la fecha de vencimiento, se abre la página **Disponibilidad de ensamblaje**. La página muestra cuántos elementos de ensamblaje se pueden ensamblar en función de la disponibilidad de los componentes. Más información en [Consultar la disponibilidad de los productos](inventory-how-availability-overview.md) Cuando se cierra la página, el pedido de ensamblado se crea con las alertas de la disponibilidad de las líneas de los componente afectados.  

    Las líneas contienen el contenido de la lista de materiales para ensamblado y las cantidades especificadas.  

    > [!NOTE]  
    >  Si la página **Disponibilidad de ensamblado** se abre cuando se rellena la cabecera del pedido de ensamblado, cada línea asignado de pedido de ensamblado afectada contiene **Sí** en el campo **Advertencia disp.** con un vínculo a la información detallada de disponibilidad. <!--check whether this field help is useful For more information, see Check Availability.--> Puede resolver un problema de disponibilidad de componentes:

    > * Posponga la fecha inicial.
    > * Sustitución del componente por otro elemento.
    > * Seleccionar una sustitución disponible si se ha definido una.  

6. En el campo **Cantidad a ensamblar**, introduzca cuántas unidades del artículo de ensamblado va a registrar como salida la próxima vez que registre el pedido de ensamblado. Esta cantidad puede ser menor que el valor del campo **Cantidad** para reflejar un registro parcial de salida.  

    > [!NOTE]  
    >  Para garantizar que el registro de consumo del componente cumpla el registro de salida del artículo de ensamblado, los campos de cantidad en las líneas del pedido de ensamblado ajustan automáticamente el valor que se introduce en el campo **Cantidad a ensamblar**.  
7. En líneas de pedido de ensamblado de tipo **Producto** o **Recurso**, en el campo **Cantidad para consumir**, introduzca cuántas unidades va a registrar como consumidas la próxima vez que registre el pedido de ensamblado.
8. Cuando esté listo listas para realizar el registro parcial o completamente, elija la acción **Registrar**.  

    > [!NOTE]  
    >  Si las advertencias todavía están presentes en las líneas del pedido de ensamblado, no puede registrar el pedido. Se muestra un mensaje con el componente o o los componentes que no están en inventario.  

Después de que el registrar se realice correctamente, el artículo de ensamblado se registra como salida al código de almacén y al potencial código de ubicación definidos en el pedido de ensamblado. Para los pedidos de ensamblado creados manualmente, la ubicación se puede copiar desde el campo de instalación **Ubicación pred. pedidos**. Para los flujos de ensamblar para pedido, el código de almacén se copia de la línea del pedido de venta.  

## <a name="see-also"></a>Consulte también .

[Administración de ensamblados](assembly-assemble-items.md)  
[Trabajar con L.M. de ensamblado](assembly-how-work-assembly-boms.md)  
[Grupos contables inventario](inventory-manage-inventory.md)  
[Información general de la gestión de almacenes](design-details-warehouse-management.md)
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
