---
title: "Ejemplo: definición de asignaciones dinámicas basándose en productos vendidos | Documentos de Microsoft"
description: "Este tema muestra un ejemplo de cómo definir asignaciones mediante el método de asignación dinámica."
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
ms.openlocfilehash: d8622d11cd23e506d1b85b18dbe5facb740c7753
ms.contentlocale: es-es
ms.lasthandoff: 01/30/2018

---
# <a name="scenario-example-defining-dynamic-allocations-based-on-items-sold"></a>Ejemplo: definición de asignaciones dinámicas basándose en productos vendidos
Este tema muestra un ejemplo de cómo definir asignaciones mediante el método de asignación dinámica. En el ejemplo, se cambia la asignación dinámica de los costes del centro de coste VENTAS para admitir el nuevo EQUIPO TI del objeto de coste. Los paquetes de EQUIPO TI tienen números de producto en el rango de 8904-W a 8924-W. Utiliza las cifras de ventas del año anterior para calcular el reparto. La asignación se registra al tipo de coste de ayuda 9903.  

> [!NOTE]  
>  El ejemplo utiliza los datos de demostración en [!INCLUDE[d365fin](includes/d365fin_md.md)].  

## <a name="to-define-dynamic-allocations-based-on-items-sold-in-the-previous-year"></a>Para definir las asignaciones dinámicas basándose en los productos vendidos el año anterior  

1.  Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Asignaciones coste** y, a continuación, seleccione el vínculo relacionado.  
2.  En la ventana **Asignación de costes**, elija la acción **Nuevo**.  
3.  En el campo **ID**, presione Entrar o escriba un Id.  
4.  En el campo **Nivel**, introduzca **1**.  
5.  Especifique las fechas del período en los campos **Válido desde** y **Válido hasta**.  
6.  En el campo **Código centro coste**, introduzca **VENTAS**.  
7.  En el campo **Abonar en tipo de coste**, especifique un tipo de coste **9903**.  
8.  En el campo **Tipo coste destino**, especifique un tipo de coste **9903**.  
9. En el campo **Objeto de coste de destino**, seleccione **Nuevo** para crear un nuevo EQUIPO TI de objeto de coste y rellene los campos según sea necesario. Seleccione **EQUIPO TI**. Deje en blanco el campo **Centro de coste de destino**.  
10. En el campo **Tipo destino asignación**, seleccione **Todos los costes** para definir cómo se asignan todos los costes acumulados.  
11. En el campo **Base**, seleccione la base de asignación **Productos vendidos (importe)**.  
12. En el campo **Nº filtro**, especifique **8904-W..8924-W**.  
13. En el campo **Filtro fecha vto.**, especifique **Año anterior**.  
14. Elija la acción **Calcular clave de asignación** para calcular el reparto.  

    > [!IMPORTANT]  
    >  [!INCLUDE[d365fin](includes/d365fin_md.md)]  utiliza las cifras de ventas de ejercicios anteriores para calcular un reparto de 1596,50 DL con el 100 por ciento para los paquetes de EQUIPO TI. Esto significa que todos los productos vendidos el año anterior se asignarán al EQUIPO TI del objeto de coste.  

## <a name="see-also"></a>Consulte también  
 [Configuración de filtros para las bases de la asignación dinámica](finance-setting-filters-for-dynamic-allocation-bases.md)   
 [Configurar origen de asignación y destinos](finance-how-to-set-up-allocation-source-and-targets.md)   
 [Definición y asignación de costes](finance-define-and-allocate-costs.md)   
 [Terminología en contabilidad de costes](finance-terminology-in-cost-accounting.md)   
 [Acerca de la contabilidad de costes](finance-about-cost-accounting.md)

