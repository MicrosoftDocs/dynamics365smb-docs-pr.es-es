---
title: Asignar y administrar tareas | Documentos de Microsoft
description: Obtener información sobre cómo asignar tareas a los usuarios, incluido su contable, en Business Central
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: tasks, work
ms.date: 07/14/2020
ms.author: edupont
ms.openlocfilehash: e1e6520aeb39a77ecfcbf652b8c328d1595d6f6f
ms.sourcegitcommit: 89d0ea903f61ab0628f99329c762d9f1619c49a7
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 07/14/2020
ms.locfileid: "3577206"
---
# <a name="define-user-tasks"></a>Definir tareas de usuario

En [!INCLUDE[d365fin](includes/d365fin_md.md)], puede crear tareas para recordarle que debe realizar el proyecto. Puede crear tareas para usted, pero también puede asignar tareas a otras personas o a otra persona en su organización  

## <a name="managing-user-tasks"></a>Gestionar tareas de usuario

La página **Tareas del usuario** muestra todas las tareas, y podrá crear y asignar fácilmente tareas nuevas. Cuando crea una tarea, puede especificar la fecha de inicio y la fecha de vencimiento, y puede agregar un enlace a la página o al informe en [!INCLUDE[d365fin](includes/d365fin_md.md)], donde el usuario debe realizar el trabajo.  

Por ejemplo, puede crear una tarea para usted o un compañero de trabajo para ver todas las facturas de ventas publicadas. En ese caso, vincule la tarea a la página 143, **Histórico facturas venta**. En la siguiente captura de pantalla, alguien está creando una tarea para que MeganB revise las facturas de ventas registradas.  

:::image type="content" source="media/across-user-tasks/sample-user-task.png" alt-text="Ejemplo de tarea de usuario":::

> [!TIP]  
> Use la búsqueda en el campo **Página** y el campo **Buscar** para encontrar la página que desea.  
>
> Puede vincular a cualquier página, pero no puede vincular a entradas individuales, así que haga la descripción lo más explícita posible, como escribir "Consulte el número de cliente 10000 y asegúrese de que no tenga pagos atrasados".

### <a name="picking-up-user-tasks"></a>Selección de tareas de usuario

En las Áreas de trabajo Administrador de negocio y Contable, un mosaico muestra las tareas pendientes que se asignan a ese usuario. Para elegir una tarea, simplemente selecciónela de la lista de tareas pendientes del usuario. En la cinta de opciones, el vínculo **Ir al elemento de la tarea** abrirá la página en la que puede realizar el trabajo.  

Cuando haya terminado una tarea, simplemente márquela como completada.  

### <a name="deleting-user-tasks"></a>Eliminar tareas de usuario

Si desea eliminar de forma masiva todas o algunas tareas del usuario, puede usar el informe **Eliminar tareas de usuario**. En la página de solicitud, puede establecer filtros para determinar qué tareas deben eliminarse.  

## <a name="see-also"></a>Consulte también

[Buscar una página o informe](ui-search.md)  
[Experiencias contables en [!INCLUDE[d365fin](includes/d365fin_md.md)]](finance-accounting.md)  
