---
title: Configurar rangos de fechas en Finance and Operations, Business edition | Documentos de Microsoft
description: "Obtenga información sobre cómo obtener un informe para mostrar datos de periodos de tiempo específicos mediante rangos de fechas en Finance and Operations, Business edition."
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: dates, reporting, filter
ms.date: 05/29/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 0494a04e67803049df71cfefe779c831c9f31674
ms.contentlocale: es-es
ms.lasthandoff: 03/22/2018

---
# <a name="entering-date-ranges"></a>Introducir rangos de fechas 
Puede establecer filtros que contienen una fecha de inicio y de finalización para mostrar sólo los datos que se incluyen dentro de dicho rango de fechas o intervalo de tiempo. Se aplican reglas especiales a la forma de establecer los rangos de fechas. Tomemos la lista **Los 10 mejores clientes** como ejemplo:

![Configurar un rango de fechas en la página de solicitud de la lista de los 10 mejores clientes](./media/ui-enter-date-ranges/customer-top10-list.png)

Aquí puede limitar el informe a un rango de fechas como las últimas 2 semanas, o un total de 6 semanas, o el rango que desee. Para establecer los rangos de fechas, introduzca las fechas y utilice **..** o **|** para definir el rango. En nuestro ejemplo, para mostrar los 10 mejores clientes de las dos primeras semanas de mayo, definiría el filtro de fecha *05 01 17..05 14 17*.
A continuación le mostramos dos ejemplos más:

| Significado | Ejemplo | Movimientos incluidos |
|---|---|---|
|Igual a| 15 12 16 |Solo los movimientos registrados el 15 de diciembre de 2016.|
|Intervalo| 15 12 16..15 17 17<br /><br />..12 15 16|Registrados entre el 15 de diciembre de 2016 y el 15 de enero de 2017, ambos incluidos.<br /><br />Registrados el 15 de diciembre de 2016 o antes.|
|O|12 15 16&#124;12 16 16|Registrados el 15 de diciembre o el 16 de diciembre de 2016. Si hay movimientos registrados en los dos días, se mostrarán todos.|

También puede combinar los distintos tipos de formato.

| Ejemplo | Movimientos incluidos |
|---|---|
|12 15 16&#124;12 01 16..05 31 17 | Movimientos registrados el 15 de diciembre de 2016, o entre el 01 de diciembre de 2016 y el 31 de mayo de 2017, ambos incluidos. |
|..12 14 16&#124;12 30 16.. | Los movimientos registrados el 14 de diciembre o con anterioridad, o bien los movimientos registrados el 30 de diciembre o posteriormente, es decir, todos los movimientos excepto los registrados en las fechas comprendidas entre el 15 y el 29 de diciembre, ambas inclusive. |

Observe que hemos utilizado el formato de fecha MMDDAA de EE. UU. A medida que [!INCLUDE[d365fin](includes/d365fin_md.md)] esté disponible en otros mercados, podrá utilizar los formatos a los que está acostumbrado.

## <a name="see-also"></a>Consulte también
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_long_md.md)]](ui-work-product.md)  
[Introducir criterios en los filtros](ui-enter-criteria-filters.md)  
[Funciones empresariales generales](ui-across-business-areas.md)

