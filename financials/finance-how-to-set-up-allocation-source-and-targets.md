---
title: "Procedimiento: configurar origen y destinos de asignación | Documentos de Microsoft"
description: "Cada asignación está formada por un origen de asignación y uno o varios destinos de asignación. El origen de asignación define qué costes se asignarán. Los destinos de asignación determinan dónde se deben asignar los costes."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: d4dcf5f95d5fc44d4b8fb72b55d905c876989a56
ms.contentlocale: es-es
ms.lasthandoff: 01/30/2018

---
# <a name="set-up-allocation-source-and-targets"></a>Configurar origen de asignación y destinos
Cada asignación está formada por un origen de asignación y uno o varios destinos de asignación. El origen de asignación define qué costes se asignarán. Los destinos de asignación determinan dónde se deben asignar los costes.  

## <a name="to-set-up-cost-allocations"></a>Para configurar asignaciones de coste  
1.  Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Asignación costes** y, a continuación, seleccione el vínculo relacionado.  
2.  En la ventana **Asignación costes**, elija la acción **Editar**.  
3.  Especifique un identificador para el origen de asignación en el campo **ID**.  
4.  Defina un nivel como un número entre 1 y 99 en el campo **Nivel**. El registro de la asignación seguirá el orden de los niveles.  
5.  Escriba un tipo de coste para definir qué tipos de coste se asignarán en el campo **Intervalo tipo coste**. Si todos los costes de un tipo de coste se asignan, no se define ningún intervalo.  
6.  Especifique un centro de coste junto con los costes que se asignarán en el campo **Código centro coste**.  
7.  Especifique un objeto de coste junto con los costes que se asignarán en el campo **Código objeto coste**. Muy a menudo, este campo permanece vacío porque raramente los objetos de coste se asignan a otros objetos de coste.  
8.  Especifique un tipo de coste en el campo **Abonar en tipo de coste**. Los costes que asignen se abonarán en el tipo de coste de origen. El registro de haber se registrará en el tipo de coste que se indique aquí.  
9. En la ficha desplegable **Líneas**, define los destinos de asignación. En la primera línea, escriba un tipo de coste en el campo en el campo **Tipo coste destino**. Define a qué tipo de coste se carga la asignación.  
10. En la primera línea, introduzca el primer destino de asignación en el campo **Centro de coste de destino** o el campo **Objeto de coste de destino**. Estos dos campos definen en qué centro de coste u objeto de coste se carga la asignación. Sólo puede rellenar uno de ellos, pero no los dos.  
11. Repita los mismos pasos en la segunda línea para configurar los destinos de asignación adicionales.  
12. Una vez configurado el destino y los orígenes de asignación, elija la acción **Calcular clave de asignación** para calcular los valores compartidos totales.  

> [!NOTE]  
>  Seleccione la casilla **Bloqueado** para desactivar la configuración de asignación.  

## <a name="see-also"></a>Consulte también  
[Contabilidad para costes](finance-manage-cost-accounting.md)  
 [Configuración de filtros para las bases de la asignación dinámica](finance-setting-filters-for-dynamic-allocation-bases.md)   
 [Ejemplo: definición de asignaciones estáticas basadas en la proporción de asignación](finance-scenario-example-defining-static-allocations-based-on-allocation-ratio.md)   
 [Ejemplo: definición de asignaciones dinámicas basándose en productos vendidos](finance-scenario-example-defining-dynamic-allocations-based-on-items-sold.md)   
 [Definición y asignación de costes](finance-define-and-allocate-costs.md)   
 [Terminología en contabilidad de costes](finance-terminology-in-cost-accounting.md)  
 [Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

