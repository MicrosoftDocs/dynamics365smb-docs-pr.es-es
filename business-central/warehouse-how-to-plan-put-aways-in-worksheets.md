---
title: Planificar ubicaciones en hojas de trabajo
description: Configure su almacén de modo que las líneas de recepción estén disponibles para usted en la hoja de trabajo de ubicación cuando desee planificar las instrucciones de ubicación de las recepciones.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/25/2021
ms.author: edupont
ms.openlocfilehash: b7bd6481c6347cfb9c8d02ba58f38101802a6caa
ms.sourcegitcommit: ef80c461713fff1a75998766e7a4ed3a7c6121d0
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 02/15/2022
ms.locfileid: "8131124"
---
# <a name="plan-put-aways-in-worksheets"></a>Planificar ubicaciones en hojas de trabajo
Si el almacén requiere los procesos de ubicación y recepción, y desea planificar instrucciones de ubicación para varios albaranes, en vez de hacer que los empleados sigan las instrucciones que crea la aplicación para albaranes registrados independientes, puede utilizar la hoja de trabajo de ubicación.  

Para configurar el almacén de manera que las líneas de recepción estén disponibles en la hoja de trabajo de ubicación en cuanto se registran, seleccione el campo **Utiliza hoj. trab. ubicación** en la ficha desplegable **Almacén** de la ficha de almacén. Para obtener más información, consulte [Configuración de la administración de almacén](warehouse-setup-warehouse.md).  

Si no selecciona este campo, la aplicación creará automáticamente instrucciones de ubicación para los albaranes que se registren.  

> [!NOTE]  
>  Independientemente del estado del campo **Utiliza hoj. trab. ubicación** de la ficha de almacén, siempre puede traer líneas de la instrucción de ubicación, es decir, líneas de la recepción registrada, a la hoja de trabajo de ubicación si hace lo siguiente:  
>   
>  1.  En la página **Ubicar almacén**, pulse Ctrl+D para eliminar toda la instrucción de ubicación o seleccione las líneas que desea procesar en la hoja de trabajo y elimínelas.  
> 2.  Continúe el proceso de tantas ubicaciones como desee, hasta que haya eliminado todas las líneas con las que no desee trabajar en la hoja de trabajo. Ahora seleccione **Hojas trab. ubicación** y realice la planificación.  

## <a name="to-plan-instructions-in-the-put-away-worksheet"></a>Para planificar instrucciones en la hoja de trabajo de ubicación  
1.  Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Hoja trabajo ubic.** y luego elija el enlace relacionado.  
2.  Seleccione la acción **Traer documentos almacén**. Se abre la página **Selección ubicación**.  

    Vea las recepciones registradas y las ubicaciones internas registradas que se han pasado a la función de ubicación, incluidas aquellas para las que ya se han creado instrucciones de ubicación. Los documentos con líneas de ubicación que ya se han ubicado y registrado completamente no se muestran en la lista.  

3. Seleccione los documentos con los que desee trabajar en la hoja de trabajo. Puede trabajar con líneas de distintos documentos al mismo tiempo.  

    > [!NOTE]  
    >  Si intenta seleccionar un documento de albarán o ubicación interna para el que ya ha creado instrucciones para todas sus líneas, la aplicación le indica que no tiene nada que manipular.  

4. Rellene el campo **Método ordenación** para ordenar las líneas de la forma que prefiera.  

    > [!NOTE]  
    >  La forma de ordenación de las líneas en la hoja de trabajo no se pasa automáticamente a la instrucción de ubicación, pero existen las mismas opciones de ordenación, además del ranking de ubicación. El orden de la línea que planifique en la hoja de trabajo se vuelve a crear fácilmente cuando se crean las instrucciones de ubicación o al ordenar las instrucciones de ubicación.  

5.  Rellene el campo **Cdad. a manipular**. Seleccione la acción **Rellenar cdad. manip. autom.** o rellene los campos manualmente.  
6.  Si es necesario, modifique las líneas manualmente. Puede eliminar líneas si, por ejemplo, es necesario ubicar algunos productos en una ubicación lejos de las ubicaciones de otros productos.  

    > [!NOTE]  
    >  Las líneas eliminadas sólo se borrar de esta hoja de trabajo, no de la lista de selección de ubicación.  

7.  Seleccione la acción **Crear ubicación**. Se abre la página **Crear documento**, donde puede agregar más información a la ubicación que está creando de la siguiente forma:  

    -   Puede asignar la ubicación a un empelado determinado.  
    -   Puede ordenar las líneas de la instrucción de ubicación como lo hizo en la hoja de trabajo o por ranking de ubicación. Cuando ordene según el ranking de ubicación, las líneas Traer se muestran primero, ya que las ubicaciones de la mayoría de las recepciones tienen un ranking de ubicación con el valor 0 y las líneas Colocar aparecen al final, empezando con las ubicaciones con el ranking de ubicación inferior. Si ha estructurado el almacén para que las ubicaciones de ranking similar estén unas al lado de otras, la ordenación de las líneas de esta forma finalmente ahorrará muchos pasos a los empleados de almacén.  
    -   Puede optar por no ver las líneas intermedias creadas cuando la aplicación divide una unidad de medida grande en otras más pequeñas seleccionando el campo **Define filtro div. bulto**. Para obtener más información, consulte [Habilitar interrupción automática masiva con ubicaciones y picking directos](warehouse-enable-automatic-breaking-bulk-with-directed-put-away-and-pick.md).  
    -   Puede hacer que no se rellene automáticamente el campo **Cdad. a manipular** en las instrucciones de ubicación.  
    -   También puede elegir imprimir el documento inmediatamente.  

8.  Seleccione **Aceptar** y la aplicación creará la ubicación según sus solicitudes.  

## <a name="see-also"></a>Consulte también  
[Gestión de almacenes](warehouse-manage-warehouse.md)  
[Grupos contables inventario](inventory-manage-inventory.md)  
[Configuración de la gestión del almacén](warehouse-setup-warehouse.md)     
[Gestión de ensamblaje](assembly-assemble-items.md)    
[Detalles de diseño: Gestión de almacén](design-details-warehouse-management.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]