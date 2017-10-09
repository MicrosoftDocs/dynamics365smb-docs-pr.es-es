---
title: "Cómo reestructurar los almacenes | Documentos de Microsoft"
description: "Es posible que desee volver a estructurar el almacén con nuevos códigos y características de ubicación."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/16/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: da5928be8280bad2eac379a5f0e5b19ddc2d12bc
ms.contentlocale: es-es
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-restructure-warehouses"></a>Procedimiento: reestructure los almacenes
Es posible que desee volver a estructurar el almacén con nuevos códigos y características de ubicación. No realizará este tipo de actividad con mucha frecuencia, pero pueden producirse algunos casos en los que sea necesaria una reclasificación para conseguir o mantener una operatividad más eficaz. Por ejemplo:  

- Es posible que desee cambiar los código de ubicación para admitir el uso de sistemas de captura automática de datos, por ejemplo, con dispositivos portátiles.  
- El almacén puede haber comprado un nuevo sistema de estanterías que ofrece nuevas posibilidades para el almacenamiento de productos.  
- La empresa puede haber modificado la clasificación de productos y movido el almacén a un nuevo almacén físico para adaptarse a este cambio.  

Si el almacén está configurado para utilizar ubicaciones, pero no ubicación y picking directos, reestructure el almacén creando las nuevas ubicaciones que desee usar en el futuro.  

## <a name="to-restructure-a-basic-warehouse-that-uses-bins-only"></a>Para reestructurar un almacén básico que utilice sólo las ubicaciones  
1.  Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Almacenes** y, a continuación, seleccione el vínculo relacionado.  
2.  En la ficha desplegable **Almacén**, establezca el campo **Selección ubic. por defecto** en **Última ubic. utiliz.**  
3.  Mueva todo el contenido de sus ubicaciones actuales a las nuevas ubicaciones que acaba de crear.  

    1.  Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Diario reclasificación producto** y, a continuación, seleccione el vínculo relacionado.  
    2.  Seleccione una línea de diario y elija **Traer conten. ubicac.**  
    3.  En la ficha desplegable **Contenido ubicación**, defina los filtros en los campos **Cód. almacén**, **Cód. ubicación** y **Nº producto** para especificar el contenido que desea mover.  
    4.  Elija el botón **Aceptar** para rellenar una línea del diario.  
    5.  En el campo **Nueva ubicación**, seleccione la ubicación a la que se deben mover los productos.  
    6.  Repita los pasos b al e para todo el contenido de la ubicación que desee mover.  
    7.  Seleccione la acción **Registrar**.  

Ahora habrá vaciado las ubicaciones donde solían estar los artículos. Las ubicaciones genéricas de los productos se han cambiado a las nuevas ubicaciones.  

## <a name="to-restructure-an-advanced-warehouse-that-uses-directed-put-away-and-pick"></a>Para reestructurar un almacén avanzado que utilice ubicación y picking directos  

1.  Cree las nuevas ubicaciones que desea utilizar en el futuro. Para obtener más información, vea [Creación de ubicaciones](warehouse-how-to-create-individual-bins.md).  
2.  Mueva todo el contenido de sus ubicaciones actuales a las nuevas ubicaciones que acaba de crear.  

    1.  Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Diario reclasificación almacén** y, a continuación, seleccione el vínculo relacionado.  
    2.  En las ubicaciones donde no exista un movimiento de productos real, cree una línea para cada una de ellas en el **Diario reclasificación almacén** con el código de ubicación anterior, **Desde cód. ubicación**, y el nuevo código de ubicación, **Hasta cód. ubicación**.  
    3.  Si algunos movimientos afectan a movimientos físicos reales que desea que ejecuten los empleados, utilice las **hojas de trabajo de movimiento** para preparar instrucciones de movimiento en vez de utilizar el diario de reclasificación de almacén. Para obtener más información, consulte [Procedimiento: mueva los artículos en las configuraciones avanzadas de almacén](warehouse-how-to-move-items-in-advanced-warehousing.md).  

3.  Cuando se hayan vaciado las ubicaciones antiguas, reclasifíquelas como ubicaciones de tipo **QC** para asegurarse de que no están incluidos en los flujos del artículo.  

    1.  Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Almacenes** y, a continuación, seleccione el vínculo relacionado.  
    2.  Seleccione la línea con la ubicación y, a continuación, elija la acción **Ubicaciones**.  
    3.  En la ventana **Ubicaciones**, en el campo **Cód. tipo ubicación**, escriba **QC** para cada una de las ubicaciones antiguas que se vaciaron en el paso 3 del procedimiento anterior.  

Ahora ha quitado las ubicaciones del flujo de almacén y las ha reclasificado como ubicaciones de control de calidad. Las ubicaciones de control de calidad no tienen ninguno de los campos de la actividad en la ventana **Tipos ubicación** seleccionada y, por lo tanto, el flujo de productos no los tiene en cuenta. Para obtener más información, vea [Cómo configurar tipos de ubicación](warehouse-how-to-set-up-bin-types.md).  

## <a name="to-delete-a-bin"></a>Para eliminar una ubicación  

1.  Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Almacenes** y, a continuación, seleccione el vínculo relacionado.  
2.  Seleccione el almacén que desea que elimine ubicaciones. Elija la acción **Ubicaciones**.  
3.  Seleccione las líneas de las ubicaciones que desee eliminar.  
4.  Elija la acción **Eliminar**.  

Si selecciona **Sí**, la ubicación se elimina para su uso futuro, pero permanece el código de ubicación en todos los movimientos de almacén.  

Si desea cambiar el nombre de una ubicación para que también cambie el nombre de todos los registros asociados con la ubicación, incluidos contenidos de la ubicación, líneas de actividad de almacén, líneas de actividad de almacén registradas, líneas de hojas de trabajo de almacén, líneas de recepción de almacén, líneas de recepción de almacén registradas, líneas de envío de almacén, líneas de envío de almacén registradas y movimientos de almacén; puede hacerlo en la ventana **Ubicaciones**.  

## <a name="to-rename-a-bin-and-change-the-bin-code-in-all-records"></a>Para cambiar el nombre de una ubicación y el código de ubicación en todos los registros  

1.  Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Almacenes** y, a continuación, seleccione el vínculo relacionado.  
2.  Seleccione la ubicación donde desee cambiar el nombre o el código de ubicación y elija la acción **Ubicaciones**.  
3.  Seleccione la ubicación que desee cambiar e introduzca un nuevo código de ubicación en el campo **Código**.  
4.  Elija el botón **Sí**.  

> [!NOTE]  
>  Si elige **Sí** y hay varias entradas relacionadas con esta ubicación, por ejemplo, porque no se han eliminado los documentos de almacén durante algún tiempo, puede tardarse en cambiar todos los registros. Por tanto, si utiliza este método, considere ejecutar el trabajo por lotes **Eliminar documentos de almacenes registrados** antes de empezar el proceso de retitulación. Tenga en cuenta también que los únicos documentos que se eliminan en este trabajo por lotes son ubicaciones, picking y movimientos.  
>   
>  Si está renombrando una ubicación que recibe o una ubicación de envío, se renombran todas las recepciones o envíos registrados que hacen referencia a la ubicación en cuestión.  

## <a name="see-also"></a>Consulte también  
[Gestión almacén](warehouse-manage-warehouse.md)  
[Grupos contables inventario](inventory-manage-inventory.md)  
[Configuración de la gestión del almacén](warehouse-setup-warehouse.md)     
[Gestión de ensamblaje](assembly-assemble-items.md)    
[Detalles de diseño: Gestión de almacén](design-details-warehouse-management.md)  
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

