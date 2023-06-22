---
title: Configurar ciclos de ventas de oportunidad y etapas de ciclo
description: 'Describe cómo definir etapas de venta, desde el contacto inicial hasta el cierre, para crear un ciclo de venta y asignarlo a las oportunidades en Business Central.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'relationship, prospect'
ms.search.forms: '5122, 5121, 5120, 5175, 5119, 5098, 5096'
ms.date: 05/27/2022
ms.author: jswymer
---
# <a name="set-up-opportunity-sales-cycles-and-cycle-stages" />Configurar ciclos de ventas de oportunidad y etapas de ciclo

Para usar oportunidades de ventas, debe configurar ciclos de ventas y etapas del ciclo de ventas. Un ciclo de ventas se compone de una serie de etapas que van desde el contacto inicial hasta el cierre de una venta. Para cada etapa, defina determinados requisitos que se deben cumplir, por ejemplo, requerir una oferta de venta, antes de que la oportunidad pueda pasar a la siguiente etapa. También puede especificar si se puede omitir una etapa. Puede definir tantos ciclos de ventas como necesite. Puede configurar tantas etapas del ciclo de ventas como sea necesario dentro de un ciclo de ventas.

Para usas de ciclos de ventas de oportunidad debe configurar el ciclo de ventas, definir las diferentes etapas del ciclo, y asignar el ciclo a oportunidades. La asignación de la actividad o las tareas relevantes para la oportunidad también puede formar parte de la configuración del ciclo de ventas.

Este artículo describe también cómo configurar tareas y actividades, y cómo asignar tareas a las actividades. Para obtener más información, consulte [Para configurar actividades con tareas](marketing-how-setup-opportunity-sales-cycles-stages.md#to-set-up-activities-with-tasks).

## <a name="to-set-up-opportunity-sales-cycle-codes" />Para configurar los casilla de selección de ciclo de ventas de oportunidades

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Ciclos de ventas** y luego elija el enlace relacionado. Se abre la página **Ciclos de ventas** y se muestran todos los ciclos de ventas existentes.
2. Elija la acción **Nuevo** y, a continuación, rellene los campos según sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

Repita estos pasos para configurar todos los ciclos de venta que desee. Después de configurar los ciclos de ventas de oportunidad, puede que quiera configurar las distintas etapas de cada ciclo.

## <a name="to-define-opportunity-sales-cycle-stages" />Para definir las etapas del ciclo de ventas de oportunidad

1. En la página **Ciclos de ventas**, seleccione el ciclo de ventas de oportunidad para el que quiere configurar etapas y, a continuación, seleccione la acción **Etapas**. Se abre la página **Etapas de ciclo de ventas**.
2. Seleccione la acción **Nuevo** para introducir una nueva etapa en el ciclo de ventas.

Repita estos pasos para configurar tantas etapas como desee del ciclo de ventas.

## <a name="to-assign-stage-cycles-to-opportunities" />Para asignar ciclos de fase a oportunidades

Cuando haya agregado el ciclo de la etapa de oportunidades, puede empezar a agregar oportunidades de ventas y, a continuación, asignar el ciclo de la etapa a oportunidades configurando el campo **Código de ciclo de ventas**. Para obtener más información, consulte [Crear oportunidades de ventas](marketing-how-create-opportunities.md).

## <a name="to-set-up-activities-with-tasks" />Para configurar actividades con tareas

Puede combinar varias tareas, como tareas que cada una represente un paso, en las actividades. Las tareas de actividad están relacionadas entre sí por medio de una fórmula de fecha. Puede asignar actividades a oportunidades, vendedores o contactos.

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Actividades** y luego elija el enlace relacionado.
2. Elija la acción **Nuevo** y, a continuación, rellene los campos según sea necesario. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]
3. En la ficha desplegable **Líneas**, rellene los campos según sea necesario para definir una o varias tareas de la actividad.

## <a name="to-assign-tasks-or-activities-of-tasks-to-opportunities" />Para asignar tareas o actividades de tareas a oportunidades

Cuando haya configurado una tarea, puede asignarla a una oportunidad de ventas y así asignar la actividad a la tarea a la que pertenece.

> [!NOTE]
> No puede crear tareas de tipo *Reunión* en línea [!INCLUDE [prod_short](includes/prod_short.md)]. La capacidad requiere acceso a una implementación local.

El siguiente procedimiento describe cómo asignar tareas de actividad a oportunidades. Los pasos son parecidos a la asignación de tareas a vendedores y contactos.

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Oportunidades** y luego elija el enlace relacionado.
2. Seleccione una oportunidad y, a continuación, elija la acción **Tareas**.
3. En la página **Lista tareas**, seleccione la acción **Crear tarea**.
4. En la página **Crear tarea**, rellene los campos según sea necesario. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]

    > [!TIP]
    > Como puede ver en el campo **Oportunidad**, la tarea se asigna automáticamente a la oportunidad correspondiente.
5. Elija el botón **Aceptar**.
6. En la página **Lista tareas**, seleccione la nueva tarea y, a continuación, seleccione la acción **Asignar actividades**.
7. En la página **Asignar actividad**, rellene los campos según sea necesario y, a continuación, elija el botón **Aceptar**.

## <a name="see-also" />Consulte también

[Procesar oportunidades de ventas](marketing-processing-sales-opportunities.md)  
[Ccial](sales-manage-sales.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
