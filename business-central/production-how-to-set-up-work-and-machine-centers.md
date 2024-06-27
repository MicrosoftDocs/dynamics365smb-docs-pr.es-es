---
title: Configurar centros de trabajo y centros de máquinas
description: 'En la ficha Centro trabajo, se organizan los valores fijos y los requisitos del recurso de producción y, por consiguiente, esta ficha rige la salida de la producción realizada en dicho centro.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.form: '99000754, 99000755, 99000756, 99000758, 99000760, 99000761, 99000762'
ms.date: 06/13/2024
ms.service: dynamics-365-business-central
---
# Configurar centros de trabajo y centros de máquinas

[!INCLUDE [prod_short](includes/prod_short.md)] distingue entre tres tipos de capacidades que se ordenan en una jerarquía en la que cada nivel contiene niveles subordinados.  

El nivel superior es el grupo de centro de trabajo. Los centros de trabajo se asignan a los grupos de centros de trabajo. Cada centro de trabajo sólo puede pertenecer a un grupo de centros de trabajo.

Puede asignar distintos centros de máquina a centros de trabajo. Un centro de máquina sólo puede pertenecer a un centro de trabajo.  

La capacidad planificada de un centro de trabajo se compone de la disponibilidad de los centros de máquina correspondientes y la disponibilidad planificada del centro de trabajo. La disponibilidad planificada del grupo de centros de trabajo es, por tanto, la suma de todas las disponibilidades correspondientes de los centros de máquina y de trabajo. La disponibilidad se almacena en los movimientos de calendario.  

> [!IMPORTANT]
> Para configurar centros de trabajo o de máquina, primero debe configurar calendarios de planta. Para obtener más información, consulte [Crear calendarios de planta](production-how-to-create-work-center-calendars.md).

## Para definir centros de trabajo

Los siguientes pasos describen principalmente cómo configurar un centro de trabajo. Los pasos para configurar un calendario de centro de máquina son parecidos excepto por la ficha desplegable **Configurar ruta**.  

1. Elija el icono ![Bombilla que abre la característica Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), , escriba **Centros de trabajo** y luego elija el enlace relacionado.  
2. Seleccione la acción **Nuevo**.  
3. Rellene los campos según sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. En el campo **Cód. grupo centro trab.**, seleccione el grupo de recursos de nivel superior bajo el que está organizado el centro de trabajo, si es relevante. En la ventana Clientes, seleccione la acción la lista desplegable **Nuevo**.  
5. En el campo **Centro de trabajo alternativo**, seleccione el centro de trabajo que desea usar si este centro de trabajo no está disponible o cuando la demanda excede su capacidad. El centro de trabajo alternativo es solo informativo y no se incluye automáticamente en los procesos de planificación.
6. Seleccione el campo **Bloqueado** si desea evitar que el centro de trabajo se utilice en cualquier procesamiento. Esto significa que la salida no se puede registrar por un artículo producido en el centro de trabajo. Para obtener más información, consulte [Registro de salida de producción](production-how-to-post-output-quantity.md).
7. En el campo **Coste unitario directo**, especifique el coste de producir una unidad de medida en este centro de trabajo, sin tener en cuenta los demás elementos de coste. Este coste se suele denominar *coste directo de mano de obra*.  
8. En el campo **% Coste indirecto**, especifique los costes generales de operación de uso del centro de trabajo como un porcentaje del coste unitario directo. Este importe porcentual se agrega al coste directo al calcular el coste unitario.  
9. En el campo **Tasa costes generales**, especifique todos los costes del centro de trabajo que no sean de explotación, como los gastos de mantenimiento, como una cantidad absoluta.  

    El campo **Coste unitario** contiene el coste unitario calculado de producir una unidad de medida en este centro de trabajo, incluidos todos los elementos de coste, como se indica a continuación:  

    Coste unitario = Coste unitario directo + (Coste unitario directo x % Coste indirecto) + Tasa de costes generales.  

10. En el campo **Cálculo coste unitario**, indique si el cálculo del coste unitario debe basarse en la cantidad de tiempo empleado: Tiempo o en el número de unidades producidas.  
11. Seleccione el campo **Coste unitario específico** si desea definir el coste unitario del centro de trabajo en la línea de ruta donde se va a utilizar. Este ajuste podría ser relevante para operaciones con costes de capacidad diferentes a los que normalmente procesaría en ese centro de trabajo.  
12. En el campo **Método de baja**, seleccione si desea calcular y contabilizar manual o automáticamente la salida en este puesto de trabajo utilizando uno de los métodos siguientes.

    |Opción|Descripción|
    |------|-----------|
    |**Manual**| Contabilice manualmente el tiempo utilizado, la producción y el rechazo en el diario de producción o en el diario de fabricación.|
    |**Anticipada**|Contabilice automáticamente la salida cuando libere la orden de producción.|
    |**Atrás**|Contabilice automáticamente la salida cuando finalice la orden de producción.|

    > [!NOTE]
    > Si es necesario, el método de baja seleccionado aquí, se puede reemplazar por operaciones individuales cambiando la configuración en las líneas de ruta

13. En el campo **Cód. unidad de medida**, especifique la unidad de tiempo en la que se efectúa el cálculo de costes y la planificación de capacidad del centro de trabajo.
    Para poder controlar el consumo constantemente, primero debe configurar un método de medida. Las unidades que se especifican son unidades básicas. Por ejemplo, el tiempo de proceso se mide en horas y minutos.

    > [!NOTE]  
    > Si utiliza Días, recuerde que un día son 24 horas y no una jornada laboral de ocho horas.

14. En el campo **Capacidad**, puede definir si en el centro de trabajo hay más de una máquina o persona trabajando a la vez. Si [!INCLUDE[prod_short](includes/prod_short.md)] no tiene la funcionalidad del centro de máquina, el valor de este campo debe ser **1**.  
15. En el campo **Eficiencia**, especifique el porcentaje de la salida estándar esperada que este centro de trabajo produce realmente. Si especifica **100**, estará indicando que el centro de trabajo tiene una salida real igual que la salida estándar.  
16. Active el botón de alternancia **Calendario consolidado** si también utiliza centros de máquina. Esta configuración asegura que los movimientos de calendario se traspasan desde los calendarios de centro de máquina.  
17. En el campo **Cód. calen. planta**, seleccione un calendario de planta. Para obtener más información, consulte [Crear calendarios de planta](production-how-to-create-work-center-calendars.md).  
18. En el campo **Tiempo cola**, puede especificar el intervalo de tiempo fijo que debe transcurrir antes de que se inicie el trabajo asignado en este centro de trabajo. 

> [!NOTE]
> Utilice tiempos de cola para proporcionar un búfer entre el momento en que un componente llega a una máquina o centro de trabajo y cuando la operación comienza realmente. Por ejemplo, una pieza se entrega a un centro de máquinas a las 10:00, pero se tarda una hora en montarla en la máquina, por lo que la operación no comienza hasta las 11:00. Para tener en cuenta esa hora, el tiempo de espera sería una hora. El valor del campo **Tiempo cola** de la ficha de centro de trabajo o centro de máquina y la suma de los valores de los campos **Tiempo preparación**, **Tiempo ejecución**, **Tiempo espera** y **Tiempo movimiento** de la línea de la línea de ruta se combinan para proporcionar el plazo de producción del producto. Esto ayuda a proporcionar tiempos de producción generales precisos.  

## Consideraciones sobre la capacidad

La capacidad y la eficacia de los puestos de trabajo y de las máquinas no solo afectan a la capacidad disponible. Los valores también afectan al tiempo de producción general que consiste en el tiempo de configuración y el tiempo de ejecución, ambos definidos en la línea de enrutamiento.  

Cuando asigna una línea de enrutamiento a un centro de trabajo o de máquina, [!INCLUDE [prod_short](includes/prod_short.md)] calcula:

- Cuánta capacidad se necesita.
- Cuánto tiempo tarda la operación en completarse.  

### Tiempo ejecución

Para calcular el tiempo de ejecución, el sistema asigna el tiempo exacto que se define en el campo **Tiempo de ejecución** de la línea de enrutamiento. La eficiencia y la capacidad no afectan al tiempo asignado. Por ejemplo, si el tiempo de ejecución se define como 2 horas, entonces el tiempo asignado es de 2 horas, independientemente de los valores en los campos de eficiencia y capacidad en el centro de trabajo.  

> [!NOTE]
> La capacidad que se utiliza en los cálculos se define como el valor mínimo entre la capacidad que se define en el centro de trabajo o máquina y la capacidad concurrente que se define para la línea de enrutamiento. Si un centro de trabajo tiene una capacidad de 100, pero la capacidad simultánea para la línea de enrutamiento es 2, entonces *2* se utilizará en los cálculos.

La *duración* de una operación, por el contrario, considera tanto la eficiencia como la capacidad. La duración se calcula como *Tiempo de ejecución / eficiencia / capacidad*. La siguiente lista muestra algunos ejemplos del cálculo de la duración para el mismo tiempo de ejecución, que se define como 2 horas para la línea de enrutamiento:

- Eficiencia del 80 % significa que necesita 2,5 horas en lugar de dos horas  
- Una eficiencia del 200 % significa que puede completar el trabajo en una hora. Puede cavar el hoyo el doble de rápido si tiene una excavadora del doble de tamaño que la más pequeña  

    Puede obtener el mismo resultado si utiliza dos excavadoras más pequeñas en lugar de una grande. Usar *2* como la capacidad y *100 %* como la eficiencia  

La capacidad fraccionaria es complicada. Lo discutiremos más adelante en este artículo. 

### Tiempo preparación

La asignación de tiempo para el tiempo de preparación depende de la capacidad y se calcula como *Tiempo de preparación x Capacidad*. Por ejemplo, si la capacidad se establece en *2*, el tiempo de configuración asignado se duplica, porque debe configurar dos máquinas para la operación.  

*Duración* del tiempo de configuración depende de la eficiencia y se calcula como *Tiempo de configuración / eficiencia*. 

- Una eficiencia del 80 % significa que necesitará 2,5 horas en lugar de dos horas para instalarse.  
- La eficiencia del 200% significa que puede completar la configuración en 1 hora en lugar de las 2 horas definidas en la línea de enrutamiento  

La capacidad fractal se utiliza solo en casos específicos.

### Centro de trabajo que procesa varios pedidos simultáneamente

Usemos una cabina de pintura como ejemplo. Tiene la misma configuración y tiempo de ejecución para cada lote procesado. Pero cada lote puede contener varios pedidos individuales que se pintan simultáneamente.  

En este caso, el tiempo de preparación y la capacidad simultánea gestionan el coste asignado a los pedidos. Le recomendamos que no utilice el tiempo de ejecución en las líneas de enrutamiento.  

El tiempo de preparación asignado para cada pedido individual será en orden inverso al número de pedidos (cantidades) que se ejecutan simultáneamente. A continuación, se muestran algunos ejemplos más del cálculo del tiempo de configuración cuando se define como dos horas para la línea de enrutamiento:

- Si hay dos órdenes, la capacidad simultánea en la línea de enrutamiento debe establecerse en 0,5.

    Como resultado, la capacidad asignada para cada uno es de una hora, pero la duración de cada pedido es de dos horas.
- Si hay dos pedidos con una cantidad de uno y cuatro, respectivamente, entonces la capacidad concurrente para la línea de enrutamiento del primer pedido es 0,2 y 0,8 para el segundo.  

    Como resultado, la capacidad asignada para el primer pedido es de 24 min y para el segundo de 96. La duración de ambos pedidos sigue siendo de dos horas.  

En ambos casos, el tiempo total asignado para todos los pedidos es de dos horas.


### Los recursos eficientes pueden dedicar solo una parte de su fecha de trabajo al trabajo productivo

> [!NOTE]
> Esto no es un escenario recomendado. Le recomendamos que utilice la eficiencia en su lugar. 

Uno de sus centros de trabajo representa a un trabajador experimentado que trabaja con un 100 % de eficiencia en sus tareas. Pero solo puede dedicar el 50 % de su tiempo de trabajo a tareas porque el resto del tiempo resuelve tareas administrativas. Si bien este trabajador es capaz de completar una tarea de dos horas en exactamente dos horas, en promedio debe esperar otras dos horas mientras la persona se ocupa de otras asignaciones.  

El tiempo de ejecución asignado es de dos horas y la duración es de cuatro horas.  

No utilice el tiempo de configuración para estos escenarios, ya que [!INCLUDE [prod_short](includes/prod_short.md)] asigna solo el 50 % del tiempo. Si el tiempo de configuración se establece en *2*, el tiempo de configuración asignado es de una hora y la duración es de dos horas.

### Calendario consolidado

Cuando el campo **Calendario consolidado** está seleccionado, entonces el centro de trabajo no tiene capacidad propia. En cambio, su capacidad es igual a la suma de las capacidades de todos los centros de máquina que están asignados al centro de trabajo.  

> [!NOTE]
> La eficiencia del centro de máquinas se convierte en la capacidad del centro de trabajo.

Por ejemplo, si tiene dos centros de máquinas con una eficiencia de 80 y 70, respectivamente, la entrada del calendario consolidado tiene:

- Una eficiencia de 100
- Una capacidad de 1,5
- Una capacidad total de 12 horas (turno de ocho horas * 1,5 de capacidad).

> [!NOTE]
> Usar el campo **Calendario consolidado** cuando estructura sus rutas para programar operaciones de producción en el nivel del centro de la máquina, no en el nivel del centro de trabajo. Cuando consolida el calendario, la página **Carga del centro de trabajo** y los informes se convierten en un resumen de la carga agregada en todos los centros de máquinas que están asignados al centro de trabajo.

### Ejemplo: distintos centros de máquina asignados a un centro de trabajo

Es importante planificar qué capacidades van a componer la capacidad total al configurar los centros de máquina y los centros de trabajo.

Si se asignan distintos centros de máquina (como 210 Mesa de empaquetado 1, 310 Cabina de pintura ...) a un centro de trabajo, resulta significativa la consideración de las capacidades únicas del centro de máquina ya que un fallo en el mismo puede interrumpir todo el proceso. Se pueden introducir los grupos de máquina según su capacidad, pero no se incluyen en la planificación. Si desactiva el botón de alternancia **Calendario consolidado**, solo se asigna la capacidad del centro de trabajo en la planificación. Se excluye la capacidad del centro de máquinas.

Sin embargo, si combina centros de mecanizado idénticos (como 210 Tabla de empaquetado 1 y 220 Tabla de empaquetado 2) en un puesto de trabajo, puede considerar el puesto de trabajo como una suma de los centros de mecanizado asignados. Por tanto, el centro de trabajo se muestra con capacidad cero. Si activa el botón de alternancia **Calendario consolidado**, se asigna la capacidad común al centro de trabajo.

Si no desea que las capacidades de los puestos de trabajo contribuyan a la capacidad total, especifique **0** en el campo **Eficiencia**.

## Para configurar una capacidad efectiva de una máquina o de un centro de trabajo

Debe configurar los recursos de producción que considera críticos y señalarlos para aceptar una carga finita en lugar de la carga infinita predeterminada que aceptan otros recursos de producción. Un recurso de capacidad restringida puede ser un centro de trabajo o de máquina que es un cuello de botella y para el que le gustaría establecer una carga limitada y finita.

[!INCLUDE[prod_short](includes/prod_short.md)] no admite el control detallado de la planta. Planea una utilización factible de los recursos al proporcionar una programación preliminar, pero no crea ni mantiene automáticamente las programaciones detalladas basadas en prioridades o reglas de optimización.

En la página **Recursos con capacidad limitada**, puede crear una configuración para evitar que los recursos se sobrecarguen. La configuración también puede garantizar que no se deje capacidad sin asignar si ello pudiera aumentar el plazo de entrega de un pedido de producción. En el campo **Amortiguador (% capdad. total)**, puede agregar tiempo de amortiguación a recursos para minimizar la división de operaciones. Este ajuste permite al sistema programar la carga en el último día posible superando ligeramente el porcentaje de carga crítica. Exceder el porcentaje de carga puede reducir la cantidad de operaciones que se dividen.

Al planificar con recursos de capacidad limitada, [!INCLUDE [prod_short](includes/prod_short.md)] se asegura de que no se carguen recursos por encima de su capacidad (carga crítica). Asigna cada operación a la franja temporal disponible más próxima. Si la franja temporal no es lo suficientemente amplia para completar toda la operación, divide la operación en dos o más partes que se colocarán en las franjas temporales más próximas disponibles.

1. Elija el icono ![Bombilla que abre la característica Dígame](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Recursos capacidad restringida** y, a continuación, elija el enlace relacionado.
2. Seleccione la acción **Nuevo**.
3. Rellene los campos según sea necesario.

> [!NOTE]
> Las operaciones de los centros de máquina o de trabajo que se configuran como recursos restringidos se planifican siempre de serie. Esta planificación significa que si un recurso restringido tiene múltiples capacidades, esas capacidades deben planificarse en secuencia. No se pueden planificar en paralelo como lo harían si el centro de trabajo o de máquinas no estuviera configurado como un recurso limitado. En un recurso limitado, el campo **Capacidad** en el centro de trabajo o el centro de máquina es mayor que **1**.

> En el caso de división de la operación, el tiempo de configuración se asigna solo una vez, pues se presupone que se realiza algún ajuste manual para optimizar la programación.

## Consulte también

[Crear calendarios de planta](production-how-to-create-work-center-calendars.md)  
[Configuración de fabricación](production-configure-production-processes.md)  
[Fabricación](production-manage-manufacturing.md)  
[Planificación](production-planning.md)  
[Inventario](inventory-manage-inventory.md)  
[Compras](purchasing-manage-purchasing.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
