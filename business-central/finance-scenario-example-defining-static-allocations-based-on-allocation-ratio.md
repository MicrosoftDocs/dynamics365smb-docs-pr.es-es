---
title: Definición de asignaciones estáticas basadas en la proporción de asignación | Documentos de Microsoft
description: El método de asignaciones estáticas se basa en un valor definido, por ejemplo los metros cuadrados utilizados, o una proporción de asignación establecida de 5:2:4.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
redirect_url: finance-define-and-allocate-costs
ms.openlocfilehash: bd17923913355f883d14beb24136e97a839116e3
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 03/31/2019
ms.locfileid: "914854"
---
# <a name="scenario-example-defining-static-allocations-based-on-allocation-ratio"></a>Ejemplo: definición de asignaciones estáticas basadas en la proporción de asignación
El método de asignaciones estáticas se basa en un valor definido, por ejemplo los metros cuadrados utilizados, o una proporción de asignación establecida de 5:2:4.  

Este tema describe cómo definir tres nuevos objetos de coste de destino de asignación para el centro de coste PROD del origen de asignación mediante la proporción 5:2:4 de asignación establecida. Los tres objetos de coste de destino son ACCESORIOS, PINTURA y COLOCACIONES.  

> [!NOTE]  
>  El ejemplo utiliza los datos de demostración en [!INCLUDE[d365fin](includes/d365fin_md.md)].  

## <a name="to-define-the-allocation-source-prod-cost-center-on-the-general-fasttab"></a>Para definir el centro de coste PROD de origen de asignación en la ficha desplegable General  

1.  Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Asignación costes** y luego elija el enlace relacionado.  
2.  En la página **Asignación costes**, elija la acción **Nuevo**.  
3.  En el campo **ID**, presione Entrar o escriba un Id.  
4.  En el campo **Nivel**, introduzca **1**.  
5.  Especifique las fechas del período en los campos **Válido desde** y **Válido hasta**.  
6.  En el campo **Código centro coste**, introduzca **PROD**.  
7.  En el campo **Abonar en tipo de coste**, especifique un tipo de coste **9903**.  

## <a name="to-define-the-allocation-target-cost-objects-on-the-lines-fasttab"></a>Para definir los objetos de coste de destino de asignación en la Ficha desplegable Líneas  

1.  En la primera línea, en el campo **Tipo coste destino**, especifique **9903**.  
2.  En la primera línea, en el campo **Objeto de coste de destino**, seleccione **ACCESORIOS**.  
3.  En la primera línea, en el campo **Tipo destino asignación**, seleccione **Todos los costes** para definir cómo se asignan todos los costes acumulados.  
4.  En la primera línea, en el campo **Base**, seleccione **Estático** para utilizar el método de asignación estática.  
5.  En la primera línea, en el campo **Compartir**, especifique la proporción de asignación **5**.  
6.  En la segunda línea, en el campo **Tipo coste destino**, especifique **9903**.  
7.  En la segunda línea, en el campo **Objeto de coste de destino**, seleccione **PINTURA**.  
8.  En la segunda línea, en el campo **Tipo destino asignación**, seleccione **Todos los costes** para definir cómo se asignan todos los costes acumulados.  
9. En la segunda línea, en el campo **Base**, seleccione **Estático** para utilizar el método de asignación estática.  
10. En la segunda línea, en el campo **Compartir**, especifique la proporción de asignación **2**.  
11. En la tercera línea, en el campo **Tipo coste destino**, especifique **9903**.  
12. En la tercera línea, en el campo **Objeto de coste de destino**, seleccione **COMPLEM**.  
13. En la tercera línea, en el campo **Tipo destino asignación**, seleccione **Todos los costes** para definir cómo se asignan todos los costes acumulados.  
14. En la tercera línea, en el campo **Base**, seleccione **Estático** para utilizar el método de asignación estática.  
15. En la tercera línea, en el campo **Compartir**, especifique la proporción de asignación **4**.  

> [!IMPORTANT]  
>  [!INCLUDE[d365fin](includes/d365fin_md.md)] calcula automáticamente el campo **Porcentaje** con un porcentaje que depende de las tres relaciones de asignación que se han introducido en el campo **Compartir** para las tres líneas.  

## <a name="see-also"></a>Consulte también  
[Definición y asignación de costes](finance-define-and-allocate-costs.md)   
