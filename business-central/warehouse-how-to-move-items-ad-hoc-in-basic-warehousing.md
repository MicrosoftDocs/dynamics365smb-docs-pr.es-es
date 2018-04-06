---
title: "Cómo mover productos ad hoc en configuraciones básicas de almacén | Microsoft Docs"
description: "Puede que necesite de vez en cuando mover los artículos entre las ubicaciones internas, no recibir o enviar ubicaciones, sin una demanda determinada desde un documento de origen. Puede realizar estos movimientos ad hoc, por ejemplo, para reorganizar el almacén, para llevar los artículos a un área de inspección o para mover más artículos a o desde un área de producción sin una relación de sistema con el documento de origen de la orden de producción."
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/16/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 198bd85853ac0cfb4501c412237e9192c55dbc30
ms.contentlocale: es-es
ms.lasthandoff: 03/22/2018

---
# <a name="move-items-ad-hoc-in-basic-warehouse-configurations"></a>Mover productos ad hoc en configuraciones básicas de almacén
Puede que necesite de vez en cuando mover los artículos entre las ubicaciones internas, no recibir o enviar ubicaciones, sin una demanda determinada desde un documento de origen. Puede realizar estos movimientos ad hoc, por ejemplo, para reorganizar el almacén, para llevar los artículos a un área de inspección o para mover más artículos a o desde un área de producción sin una relación de sistema con el documento de origen de la orden de producción.  

En configuraciones de almacén básico, es decir en ubicaciones que utilizan el campo de instalación **Ubicac. obligatoria** y posiblemente los campos de configuración **Picking requerido** y **Ubicación requerida**, puede registrar los movimientos ad hoc sin los documentos de origen de las siguientes formas:  

- Con la ventana **Movimiento interno**.  
- Con la ventana **Diario reclasificación productos**.  

> [!NOTE]  
>  En configuraciones avanzadas de almacén, es decir las ubicaciones que utilizan el campo de configuración **Ubicac. y pick. directo**, utilice las ventanas **Hoja trabajo movimiento**, **Picking almacén interno** o **Ubicación almacén interno** para mover los artículos ad hoc entre ubicaciones.  

## <a name="to-move-items-as-an-internal-movement"></a>Para mover los artículos como movimiento interno  
1.  Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Movimiento interno** y, a continuación, seleccione el vínculo relacionado.  
2.  En la ficha desplegable **General**, rellene el campo **Nº** bien dejando el campo o eligiendo el botón **AssistEdit** para seleccionar de las series de números.  
3.  En el campo de **Cód. almacén**, escriba la ubicación donde tiene lugar el movimiento.  

    Si la ubicación está configurada como predeterminada como empleado de almacén, el código de almacén se insertará automáticamente.  
4.  En el campo **Hasta cód. ubicación**, introduzca un código para la ubicación a la que desea mover el artículo. A efectos de producción, esto podría ser el código de ubicación a producción, por ejemplo, tal como se define en la ficha de almacén o del centro de trabajo.  
5.  En el campo **Fecha vencimiento**, introduzca la fecha en la que debe completarse el movimiento.  
6.  En la ficha desplegable **Líneas**, elija el campo **Nº producto** para abrir la ventana **Lista contenidos ubic.** y seleccione el producto que se debe mover según su disponibilidad en las ubicaciones. También, elija la acción **Traer conten. ubicac.** para rellenar las líneas de movimiento interno basándose en los filtros. Para obtener más información, vea la información sobre herramientas para la acción **Traer conten. ubicac.**.   

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

    Ejecute el resto del movimiento ad hoc en la ventana **Movimiento inventario** de la misma forma que lo haría en un movimiento basado en los documentos de origen. Para obtener más información, consulte, por ejemplo, [Mover componentes a un área de operaciones en las configuraciones básicas de almacén](warehouse-how-to-move-components-to-an-operation-area-in-basic-warehousing.md)  

## <a name="to-move-items-with-the-item-reclassification-journal"></a>Para mover productos con el diario de reclasificación de productos:
En lugar de utilizar documentos de movimiento de almacén, puede registrar el movimiento de productos reclasificando sus códigos de ubicación. Para obtener más información, consulte [Recuento, ajuste, y reclasificación de inventario](inventory-how-count-adjust-reclassify.md).   
1.  Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Diario reclas. producto** y, a continuación, seleccione el vínculo relacionado.  
2.  En cada línea del diario, defina las ubicaciones de las que y a las que desea mover los artículos rellenando los campos **Cód. ubicación** y **Nueva ubicación**.  

    1.  Para mover todo el contenido de una ubicación a otra, elija la acción **Traer conten. ubicac.**.  
    2.  Rellene los filtros para encontrar la ubicación cuyo contenido desea mover y a continuación seleccione **Aceptar**. Las líneas del diario se rellenan con el contenido de la ubicación.  
3.  Rellene el resto de los campos de cada línea del diario.   
4.  Registre el diario de reclasificación.  

    > [!NOTE]  
    >  A diferencia de los documentos de movimiento, un movimiento registrado con el diario de reclasificación no crea una solicitud de almacén para realizar la tarea física.  

## <a name="see-also"></a>Consulte también  
[Gestión almacén](warehouse-manage-warehouse.md)  
[Grupos contables inventario](inventory-manage-inventory.md)  
[Configuración de la gestión del almacén](warehouse-setup-warehouse.md)     
[Gestión de ensamblaje](assembly-assemble-items.md)    
[Detalles de diseño: Gestión de almacén](design-details-warehouse-management.md)  
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

