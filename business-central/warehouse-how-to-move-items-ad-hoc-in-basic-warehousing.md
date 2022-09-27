---
title: Mover productos ad hoc en configuraciones básicas de almacén
description: Este tema explica los movimientos ad hoc realizados cuando necesita mover artículos entre ubicaciones internas sin una demanda específica de un documento de origen.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.search.form: 393, 7382
ms.date: 06/25/2021
ms.author: edupont
ms.openlocfilehash: 46b6cbd88cf23974e5fd11453c328c1669c8e19c
ms.sourcegitcommit: 3acadf94fa34ca57fc137cb2296e644fbabc1a60
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 09/19/2022
ms.locfileid: "9534432"
---
# <a name="move-items-ad-hoc-in-basic-warehouse-configurations"></a>Mover productos ad hoc en configuraciones básicas de almacén

Puede que necesite de vez en cuando mover los artículos entre las ubicaciones internas, no recibir o enviar ubicaciones, sin una demanda determinada desde un documento de origen. Puede realizar estos movimientos ad hoc, por ejemplo, para reorganizar el almacén, para llevar los artículos a un área de inspección o para mover más artículos a o desde un área de producción sin una relación de sistema con el documento de origen de la orden de producción.  

En configuraciones de almacén básico, es decir en ubicaciones que utilizan el campo de instalación **Ubicac. obligatoria** y posiblemente los campos de configuración **Picking requerido** y **Ubicación requerida**, puede registrar los movimientos ad hoc sin los documentos de origen de las siguientes formas:  

- Con la página **Movimiento interno**.  
- Con la página **Diario reclasificación productos**.  

> [!NOTE]  
>  En configuraciones avanzadas de almacén, es decir las ubicaciones que utilizan el campo de configuración **Ubicac. y pick. directo**, utilice las páginas **Hoja trabajo movimiento**, **Picking almacén interno** o **Ubicación almacén interno** para mover los artículos ad hoc entre ubicaciones.  

## <a name="to-move-items-as-an-internal-movement"></a>Para mover los artículos como movimiento interno

1.  Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Movimiento interno** y, a continuación, elija el vínculo relacionado.  
2.  En la ficha desplegable **General**, rellene el campo **Nº** bien dejando el campo o eligiendo el botón **AssistEdit** para seleccionar de las series de números.  
3.  En el campo de **Cód. almacén**, escriba la ubicación donde tiene lugar el movimiento.  

    Si la ubicación está configurada como predeterminada como empleado de almacén, el código de almacén se insertará automáticamente.  
4.  En el campo **Hasta cód. ubicación**, introduzca un código para la ubicación a la que desea mover el artículo. A efectos de producción, esto podría ser el código de ubicación a producción, por ejemplo, tal como se define en la ficha de almacén o del centro de trabajo.  
5.  En el campo **Fecha vencimiento**, introduzca la fecha en la que debe completarse el movimiento.  
6.  En la ficha desplegable **Líneas**, elija el campo **Nº producto** para abrir la página **Lista contenidos ubic.** y seleccione el producto que se debe mover según su disponibilidad en las ubicaciones. También, elija la acción **Traer conten. ubicac.** para rellenar las líneas de movimiento interno basándose en los filtros. Para obtener más información, vea la información sobre herramientas para la acción **Traer conten. ubicac.**.  

    Cuando haya seleccionado el artículo, el campo **Desde cód. ubicación** se rellena automáticamente según el contenido seleccionado en la ubicación, pero puede cambiarlo por cualquier otra ubicación donde esté disponible el artículo.  

    > [!NOTE]  
    >  Dado que el campo **Nº producto** y el **Desde cód. ubicación** están conectados, los valores pueden cambiar de forma interdependiente cuando se edite el campo.  

    El campo **Hasta cód. ubicación** se rellena con el valor introducido en la cabecera, pero puede cambiarlo en la línea a cualquier otro código de ubicación que no esté bloqueado ni se dedique a fines especiales. Para obtener más información acerca de la fabricación de las ubicaciones dedicadas, consulte Dedicado.  
7.  Cuando haya definido que las ubicaciones desde y a las que desea mover el artículo, introduzca la cantidad para mover en el campo **Cantidad**.  

    > [!NOTE]  
    >  La cantidad debe estar disponible en campo Desde cód. ubicación.  

8.  Cuando vaya para procesar el movimiento interno, elija la acción **Crear movimiento de inventario**.  

    > [!NOTE]  
    >  Cuando se haya creado el movimiento de inventario, se eliminarán las líneas de movimientos internos.  

    Ejecute el resto del movimiento ad hoc en la página **Movimiento inventario** de la misma forma que lo haría en un movimiento basado en los documentos de origen. Para obtener más información, consulte, por ejemplo, [Mover componentes a un área de operaciones en las configuraciones básicas de almacén](warehouse-how-to-move-components-to-an-operation-area-in-basic-warehousing.md)  

## <a name="to-move-items-with-the-item-reclassification-journal"></a>Para mover productos con el diario de reclasificación de productos:

En lugar de utilizar documentos de movimiento de almacén, puede registrar el movimiento de productos reclasificando sus códigos de ubicación. Para obtener más información, consulte [Recuento, ajuste y reclasificación de inventario mediante diarios](inventory-how-count-adjust-reclassify.md).

1.  Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Diarios reclasif. producto**, y luego elija el enlace relacionado.  
2.  En cada línea del diario, defina las ubicaciones de las que y a las que desea mover los artículos rellenando los campos **Cód. ubicación** y **Nueva ubicación**.  

    1.  Para mover todo el contenido de una ubicación a otra, elija la acción **Traer conten. ubicac.**.  
    2.  Rellene los filtros para encontrar la ubicación cuyo contenido desea mover y a continuación seleccione **Aceptar**. Las líneas del diario se rellenan con el contenido de la ubicación.  
3.  Rellene el resto de los campos de cada línea del diario.   
4.  Registre el diario de reclasificación.  

    > [!NOTE]  
    >  A diferencia de los documentos de movimiento, un movimiento registrado con el diario de reclasificación no crea una solicitud de almacén para realizar la tarea física.  

## <a name="see-related-microsoft-training"></a>Consultar la [formación de Microsoft](/training/modules/manage-internal-warehouse-processes/) relacionada

## <a name="see-also"></a>Consulte también .

[Warehouse Management](warehouse-manage-warehouse.md)  
[Inventario](inventory-manage-inventory.md)  
[Configuración de Warehouse Management](warehouse-setup-warehouse.md)  
[Gestión de ensamblaje](assembly-assemble-items.md)  
[Detalles de diseño: Warehouse Management](design-details-warehouse-management.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
