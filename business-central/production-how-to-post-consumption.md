---
title: Registrar consumibles por lotes
description: 'Si el método de baja es Manual, debe registrar los componentes manualmente con un diario de consumo.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: '99000846, 99000850'
ms.date: 04/01/2021
ms.author: edupont
---
# <a name="batch-post-production-consumption"></a><a name="batch-post-production-consumption"></a><a name="batch-post-production-consumption"></a><a name="batch-post-production-consumption"></a>Registrar consumibles de producción por lotes

Si el método de baja es **Manual**, debe registrar los componentes manualmente con un diario de consumo.  

>[!NOTE]
> Si ha activado el campo **Picking requerido** en la ficha de almacén para indicar que el almacén requiere proceso de picking de existencias, no necesita usar este trabajo por lotes. [!INCLUDE[prod_short](includes/prod_short.md)] manejará el consumo cuando registro el picking de existencias. Para obtener más información, consulte [Recoger para producción en configuraciones básicas de almacén](warehouse-how-to-pick-for-production.md).  

También puede configurar [!INCLUDE[prod_short](includes/prod_short.md)] para que registre (*vaciar*) automáticamente los componentes cuando inicia o finaliza órdenes de producción. Para obtener más información, consulte [Procedimiento: Habilitar el vaciado de componentes según la producción de la operación](production-how-to-flush-components-according-to-operation-output.md).

## <a name="to-post-consumption-for-one-or-more-production-order-lines"></a><a name="to-post-consumption-for-one-or-more-production-order-lines"></a><a name="to-post-consumption-for-one-or-more-production-order-lines"></a><a name="to-post-consumption-for-one-or-more-production-order-lines"></a>Para registrar el consumo en una o varias líneas de la orden de producción

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Diario de consumo** y, a continuación, elija el vínculo relacionado.  
2. Rellene los campos con los datos de las órdenes de producción y del consumo. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

    Use la acción **Calcular consumo** para generar líneas del diario de las órdenes de producción basadas en la salida real (la cantidad de productos terminados sobre la que se ha informado) o en la salida esperada (la cantidad de productos terminados que espera producir).

    > [!NOTE]
    > Si configuró la ficha de almacén para requerir el proceso de picking y envío, en el campo **Cantidad** de la página **Diario de consumo** solo se pueden introducir cantidades que ya se han seleccionado a través de un actividad de almacén , no una cantidad calculada. Para obtener más información, consulte [Realizar picking para ensamblado o producción en una configuración avanzada de almacén](warehouse-how-to-pick-for-internal-operations-in-advanced-warehousing.md)

3. Para registrar el consumo, elija la acción **Registrar**. Los inventarios relacionados se reducen.

## <a name="see-also"></a><a name="see-also"></a><a name="see-also"></a><a name="see-also"></a>Consulte también

[Fabricación](production-manage-manufacturing.md)  
[Configuración de fabricación](production-configure-production-processes.md)  
[Planificación](production-planning.md)  
[Inventario](inventory-manage-inventory.md)  
[Compras](purchasing-manage-purchasing.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
