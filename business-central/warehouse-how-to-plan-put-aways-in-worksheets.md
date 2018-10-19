---
title: "Cómo planificar ubicaciones en la hoja de trabajo | Documentos de Microsoft"
description: "Si el almacén requiere los procesos de ubicación y recepción, y desea planificar instrucciones de ubicación para varias recepciones, en vez de hacer que los empleados sigan las instrucciones que crea el sistema para recepciones registradas independientes, puede utilizar la hoja de trabajo de ubicación."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: f6ef554270c9e2bdef8074b65ba6e3f0de4bd45c
ms.contentlocale: es-es
ms.lasthandoff: 09/28/2018

---
# <a name="plan-put-aways-in-worksheets"></a>Planificar ubicaciones en hojas de trabajo
Si el almacén requiere los procesos de ubicación y recepción, y desea planificar instrucciones de ubicación para varias recepciones, en vez de hacer que los empleados sigan las instrucciones que crea el sistema para recepciones registradas independientes, puede utilizar la hoja de trabajo de ubicación.  

Para configurar el almacén de manera que las líneas de recepción estén disponibles en la hoja de trabajo de ubicación en cuanto se registran, seleccione el campo **Utiliza hoj. trab. ubicación** en la ficha desplegable **Almacén** de la ficha de almacén. Para obtener más información, consulte [Configuración de la administración de almacén](warehouse-setup-warehouse.md).  

Si no selecciona este campo, el programa creará automáticamente instrucciones de ubicación para las recepciones que se registren.  

> [!NOTE]  
>  Independientemente del estado del campo **Utiliza hoj. trab. ubicación** de la ficha de almacén, siempre puede traer líneas de la instrucción de ubicación, es decir, líneas de la recepción registrada, a la hoja de trabajo de ubicación si hace lo siguiente:  
>   
>  1.  En la ventana **Ubicar almacén**, pulse Ctrl+D para eliminar toda la instrucción de ubicación o seleccione las líneas que desea procesar en la hoja de trabajo y elimínelas.  
> 2.  Continúe el proceso de tantas ubicaciones como desee, hasta que haya eliminado todas las líneas con las que no desee trabajar en la hoja de trabajo. Ahora seleccione **Hojas trab. ubicación** y realice la planificación.  

## <a name="to-plan-instructions-in-the-put-away-worksheet"></a>Para planificar instrucciones en la hoja de trabajo de ubicación  
1.  Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Hoja trabajo ubic.** y luego elija el enlace relacionado.  
2.  Seleccione la acción **Traer documentos almacén**. Se abre la ventana **Selección ubicación**.  

    Vea las recepciones registradas y las ubicaciones internas registradas que se han pasado a la función de ubicación, incluidas aquellas para las que ya se han creado instrucciones de ubicación. Los documentos con líneas de ubicación que ya se han ubicado y registrado completamente no se muestran en la lista.  

3. Seleccione los documentos con los que desee trabajar en la hoja de trabajo. Puede trabajar con líneas de distintos documentos al mismo tiempo.  

    > [!NOTE]  
    >  Si intenta seleccionar un documento de recepción o ubicación interna para el que ya ha creado instrucciones para todas sus líneas, el programa le indica que no tiene nada que manipular.  

4. Rellene el campo **Método ordenación** para ordenar las líneas de la forma que prefiera.  

    > [!NOTE]  
    >  La forma de ordenación de las líneas en la hoja de trabajo no se pasa automáticamente a la instrucción de ubicación, pero existen las mismas opciones de ordenación, además del ranking de ubicación. El orden de la línea que planifique en la hoja de trabajo se vuelve a crear fácilmente cuando se crean las instrucciones de ubicación o al ordenar las instrucciones de ubicación.  

5.  Rellene el campo **Cdad. a manipular**. Seleccione la acción **Rellenar cdad. manip. autom.** o rellene los campos manualmente.  
6.  Si es necesario, modifique las líneas manualmente. Puede eliminar líneas si, por ejemplo, es necesario ubicar algunos productos en una ubicación lejos de las ubicaciones de otros productos.  

    > [!NOTE]  
    >  Las líneas eliminadas sólo se borrar de esta hoja de trabajo, no de la lista de selección de ubicación.  

7.  Seleccione la acción **Crear ubicación**. Se abre la ventana **Crear documento**, donde puede agregar más información a la ubicación que está creando de la siguiente forma:  

    -   Puede asignar la ubicación a un empelado determinado.  
    -   Puede ordenar las líneas de la instrucción de ubicación como lo hizo en la hoja de trabajo o por ranking de ubicación. Cuando ordene según el ranking de ubicación, las líneas Traer se muestran primero, ya que las ubicaciones de la mayoría de las recepciones tienen un ranking de ubicación con el valor 0 y las líneas Colocar aparecen al final, empezando con las ubicaciones con el ranking de ubicación inferior. Si ha estructurado el almacén para que las ubicaciones de ranking similar estén unas al lado de otras, la ordenación de las líneas de esta forma finalmente ahorrará muchos pasos a los empleados de almacén.  
    -   Puede optar por no ver las líneas intermedias creadas cuando el sistema divide una unidad de medida grande en otras más pequeñas seleccionando el campo **Define filtro div. bulto**. Para obtener más información, consulte [Habilitar interrupción automática masiva con picking y ubicaciones directas] (warehouse-enable-automatic-breaking-bulk-with-directed-put-away-and-pick.md).  
    -   Puede hacer que no se rellene automáticamente el campo **Cdad. a manipular** en las instrucciones de ubicación.  
    -   También puede elegir imprimir el documento inmediatamente.  

8.  Seleccione **Aceptar** y el sistema creará la ubicación según sus solicitudes.  

## <a name="see-also"></a>Consulte también  
[Gestión almacén](warehouse-manage-warehouse.md)  
[Grupos contables inventario](inventory-manage-inventory.md)  
[Configuración de la gestión del almacén](warehouse-setup-warehouse.md)     
[Gestión de ensamblaje](assembly-assemble-items.md)    
[Detalles de diseño: Gestión de almacén](design-details-warehouse-management.md)  
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

