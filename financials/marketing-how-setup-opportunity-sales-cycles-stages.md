---
title: Configurar ciclos de ventas de oportunidad y etapas de ciclo | Documentos de Microsoft
description: "Describe cómo definir etapas de venta, desde el contacto inicial hasta el cierre, para crear un ciclo de venta y asignarlo a las oportunidades en Finance and Operations, Business edition."
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, prospect
ms.date: 06/06/2017
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: ecff2e9e0705055a514f1726b3223f8196300cb6
ms.contentlocale: es-es
ms.lasthandoff: 03/22/2018

---
# <a name="set-up-opportunity-sales-cycles-and-cycle-stages"></a>Configurar ciclos de ventas de oportunidad y etapas de ciclo
Para poder usar oportunidades de ventas, debe configurar ciclos de ventas y etapas del ciclo de ventas. Un ciclo de ventas se compone de una serie de etapas que van desde el contacto inicial hasta el cierre de una venta. Cada etapa puede tener determinados requisitos que se deben cumplir, por ejemplo, requerir una oferta de venta, antes de que la oportunidad pueda pasar a la siguiente etapa. También puede especificar si se puede omitir una etapa. Puede configurar tantos ciclos de ventas como necesite y tantas etapas del ciclo de ventas como sean necesarias para el ciclo de ventas.

La implementación de ciclos de ventas de oportunidad implica la configuración del ciclo de ventas, que define las diferentes etapas del ciclo, y la asignación del ciclo a oportunidades. La asignación de la actividad o las tareas relevantes para la oportunidad también puede formar parte de la configuración del ciclo de ventas.

Este tema describe también cómo configurar tareas y actividades, y cómo asignar tareas a las actividades. Para obtener más información, consulte la sección "Para configurar actividades con tareas".

## <a name="to-set-up-opportunity-sales-cycle-codes"></a>Para configurar los casilla de selección de ciclo de ventas de oportunidades
1. Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Ciclos venta** y, a continuación, seleccione el vínculo relacionado. Se abre la ventana **Ciclos de ventas** y se muestran todos los ciclos de ventas existentes.
2. Elija la acción **Nuevo** y, a continuación, rellene los campos según sea necesario. [!INCLUDE [tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

Repita estos pasos para configurar todos los ciclos de venta que desee. Después de configurar los ciclos de ventas de oportunidad, puede que quiera configurar las distintas etapas de cada ciclo.

## <a name="to-define-opportunity-sales-cycle-stages"></a>Para definir las etapas del ciclo de ventas de oportunidad
1. En la ventana **Ciclos de ventas**, seleccione el ciclo de ventas de oportunidad para el que quiere configurar etapas y, a continuación, seleccione la acción **Etapas**. Se abre la ventana **Etapas de ciclo de ventas**.
2. Seleccione la acción **Nuevo** para introducir una nueva etapa en el ciclo de ventas.

Repita estos pasos para configurar tantas etapas como desee del ciclo de ventas.

## <a name="to-assign-stage-cycles-to-opportunities"></a>Para asignar ciclos de fase a oportunidades
Cuando haya agregado el ciclo de la etapa de oportunidades, puede empezar a agregar oportunidades de ventas y, a continuación, asignar el ciclo de la etapa a oportunidades configurando el campo **Código de ciclo de ventas**. Para obtener más información, consulte [Crear oportunidades de ventas](marketing-how-create-opportunities.md).

## <a name="to-set-up-activities-with-tasks"></a>Para configurar actividades con tareas
Puede combinar varias tareas, por ejemplo, tareas que cada una represente un paso, en las actividades. Las tareas de actividad están relacionadas entre sí por medio de una fórmula de fecha. Puede asignar actividades a oportunidades, vendedores o contactos.

1. Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Actividades** y, a continuación, seleccione el vínculo relacionado.
2. Elija la acción **Nuevo** y, a continuación, rellene los campos según sea necesario.
3. En la ficha desplegable **Líneas**, rellene los campos según sea necesario para definir una o varias tareas de la actividad.

## <a name="to-assign-tasks-or-activities-of-tasks-to-opportunities"></a>Para asignar tareas o actividades de tareas a oportunidades
Cuando haya configurado una tarea, puede asignarla a una oportunidad de ventas y así asignar la actividad a la tarea a la que pertenece.

> [!NOTE]  
>   Este procedimiento describe cómo asignar tareas de actividad a oportunidades. los pasos son parecidos a la asignación de tareas a vendedores y contactos.

1. Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Oportunidades** y, a continuación, seleccione el vínculo relacionado.
2. Seleccione una oportunidad y, a continuación, elija la acción **Tareas**.
3. En la ventana **Lista tareas**, seleccione la acción **Crear tarea**.
4.  En la ventana **Crear tarea**, rellene los campos según sea necesario.

    Observe el campo **Oportunidad**, que se asigna automáticamente a la oportunidad en cuestión.
5. Elija el botón **Aceptar**.
6. En la ventana **Lista tareas**, seleccione la nueva tarea y, a continuación, seleccione la acción **Asignar actividades**.
7. En la ventana **Asignar actividad**, rellene los campos según sea necesario y, a continuación, elija el botón **Aceptar**.

## <a name="see-also"></a>Consulte también
[Procesar oportunidades de ventas](marketing-processing-sales-opportunities.md)  
[Ventas](sales-manage-sales.md)  
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

