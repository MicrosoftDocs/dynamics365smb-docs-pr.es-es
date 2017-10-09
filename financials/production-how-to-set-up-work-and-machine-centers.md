---
title: "Configurar centros de trabajo y de máquina | Documentos de Microsoft"
description: "Una ficha **Centro de trabajo**, organiza los valores fijos y los requisitos del recurso de producción y, por consiguiente, esta ficha rige la salida de la producción realizada en dicho centro de trabajo."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/04/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 8a7af6821affcef2c81499e904f2ed9520086323
ms.contentlocale: es-es
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-set-up-work-centers-and-machine-centers"></a>Procedimiento: Configuración de centros de trabajo y centros de máquinas
El programa distingue entre tres tipos de capacidad. Éstas se organizan de manera jerárquica. Cada nivel contiene los niveles subordinados.  

El nivel superior es el grupo de centro de trabajo. Los centros de trabajo se asignan a los grupos de centros de trabajo. Cada centro de trabajo sólo puede pertenecer a un grupo de centros de trabajo.

Puede asignar distintos centros de máquina a cada centro de trabajo. Un centro de máquina sólo puede pertenecer a un centro de trabajo.  

La capacidad planificada de un centro de trabajo se compone de la disponibilidad de los centros de máquina correspondientes y la disponibilidad planificada adicional del centro de trabajo. La disponibilidad planificada del grupo de centros de trabajo es, por tanto, la suma de todas las disponibilidades correspondientes de los centros de máquina y de trabajo.  

La disponibilidad se almacena en los movimientos de calendario. Para configurar centros de trabajo o de máquina, primero debe configurar calendarios de planta. Para obtener más información, consulte [Procedimiento: Crear calendarios de planta](production-how-to-create-work-center-calendars.md).  

## <a name="to-set-up-a-work-center"></a>Para definir centros de trabajo
A continuación se describe principalmente cómo configurar un centro de trabajo. Los pasos para configurar un calendario de centro de máquina son parecidos excepto por la ficha desplegable **Configurar ruta**.  

1.  Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Centros de trabajo** y, a continuación, seleccione el vínculo relacionado.  
2.  Seleccione la acción **Nuevo**.  
3. Rellene los campos según sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4.  En el campo **Grupo de centro de trabajo**, seleccione el grupo de recursos de nivel superior bajo el que está organizado el centro de trabajo, si es relevante. En la ventana Clientes, seleccione la acción la lista desplegable **Nuevo**.  
5.  Seleccione el campo **Bloqueado** si desea evitar que el centro de trabajo se utilice en cualquier procesamiento. Esto significa que la salida no se puede registrar por un artículo producido en el centro de trabajo. Para obtener más información, consulte [Registro de salida de producción](production-how-to-post-output-quantity.md).
6.  En el campo **Coste unitario directo**, especifique el coste de producir una unidad de medida en este centro de trabajo, sin tener en cuenta los demás elementos de coste. Este coste se suele denominar *coste directo de mano de obra*.  
7.  En el campo **% Coste indirecto**, especifique los costes generales de operación de uso del centro de trabajo como un porcentaje del coste unitario directo. Este importe porcentual se agrega al coste directo al calcular el coste unitario.  
8.  En el campo **Tasa costes generales**, especifique todos los costes del centro de trabajo que no sean de explotación, como los gastos de mantenimiento, como una cantidad absoluta.  

    El campo **Coste unitario** contiene el coste unitario calculado de producir una unidad de medida en este centro de trabajo, incluidos todos los elementos de coste, como se indica a continuación:  

    Coste unitario = Coste unitario directo + (Coste unitario directo x % Coste indirecto) + Tasa de costes generales.  

9.  En el campo **Cálculo coste unitario**, indique si el cálculo anterior debe basarse en la cantidad de tiempo empleado: **Tiempo** o en el número de unidades producidas: **Unidades**.  
10.  Seleccione el campo **Coste unitario específico** si desea definir el coste unitario del centro de trabajo en la línea de ruta donde se va a utilizar. Esto se aplica a las operaciones con unos costes de capacidad radicalmente diferentes de los procesados normalmente en el centro de trabajo.  
11.  En el campo **Método de baja**, seleccione si el registro de salida de este centro de trabajo se debe calcular y registrar manualmente o automáticamente con alguno de los métodos siguientes.  

    |Opción|Description|  
    |----------------------------------|---------------------------------------|  
    |**Manual**|El consumo se registra manualmente en el diario de salida o en el diario de producción.|
    |**Anticipada**|El consumo se calcula y se registra automáticamente al lanzar la orden de producción.|  
    |**Atrás**|El consumo se calcula y se registra automáticamente cuando se finaliza la orden de producción.|  

    > [!NOTE]  
    >  Si es necesario, se puede reemplazar el método de baja seleccionado aquí y en la ficha **Producto** para operaciones individuales; para ello, deberá cambiar la configuración en las líneas de ruta.

12.  En el campo **Cód. unidad de medida**, especifique la unidad de tiempo en la que se efectúa el cálculo de costes y la planificación de capacidad del centro de trabajo.
    Para poder controlar el consumo constantemente, primero debe configurar un método de medida. Las unidades que se especifican son unidades básicas. Por ejemplo, el tiempo de proceso se mide en horas y minutos.

    > [!NOTE]  
    > Si decide utilizar Días, recuerde que 1 día = 24 horas, y no 8 (jornada laboral).

13.  En el campo **Capacidad**, puede definir si en el centro de trabajo hay más de una máquina o persona trabajando a la vez. Si la instalación de **Nombre producto** no incluye la funcionalidad del centro de máquina, el valor de este campo debe ser **1**).  
14.  En el campo **Eficiencia**, especifique el porcentaje de la salida estándar esperada que este centro de trabajo produce realmente. Si especifica **100**, estará indicando que el centro de trabajo tiene una salida real igual que la salida estándar.  
15. Seleccione la casilla verificación **Calendario consolidado** si también utiliza centros de máquina. Esto asegura que los movimientos de calendario se traspasan desde los calendarios de centro de máquina.  
16.  En el campo **Cód. calen. planta**, seleccione un calendario de planta. Para obtener más información, consulte [Procedimiento: Crear calendarios de planta](production-how-to-create-work-center-calendars.md).  
17.  En el campo **Tiempo cola**, puede especificar el intervalo de tiempo fijo que debe transcurrir antes de que se inicie el trabajo asignado en este centro de trabajo. Tenga en cuenta que el tiempo de cola se agrega a otros elementos de tiempo no productivos, como el tiempo de espera y el tiempo de movimiento, que haya definido en las líneas de ruta que utilizan este centro de trabajo.  

## <a name="example---different-machine-centers-assigned-to-a-work-center"></a>Ejemplo: distintos centros de máquina asignados a un centro de trabajo.
Es importante planificar qué capacidades van a componer la capacidad total al configurar los centros de máquina y los centros de trabajo.

Si se asignan distintos centros de máquina (como 210 Mesa de empaquetado 1, 310 Cabina de pintura ...) a un centro de trabajo, resulta significativa la consideración de las capacidades únicas del centro de máquina ya que un fallo en el mismo puede interrumpir todo el proceso. Se pueden introducir los grupos de máquina según su capacidad, pero podrían no incluirse en la planificación. A desactivar el campo **Calendario consolidado**, sólo se asigna la capacidad del centro de trabajo en la planificación y no la del centro de máquina.

Si, no obstante, se combinan centros de máquina idénticos (como 210 Mesa de empaquetado 1 y 220 Mesa de empaquetado 2) en un centro de trabajo, resulta interesante la consideración del centro de trabajo como la suma de los centros de máquina asignados. Por tanto, el centro de trabajo se mostrará con capacidad cero. Al activar el campo **Calendario consolidado**, se asigna la capacidad común al centro de trabajo.

Si las capacidades de los centros de trabajo no van a contribuir a la capacidad total, puede conseguir que lo hagan mediante un factor de eficiencia igual a cero.

## <a name="see-also"></a>Consulte también  
[Cómo crear calendarios de planta](production-how-to-create-work-center-calendars.md)  
[Configuración de fabricación](production-configure-production-processes.md)  
[Fabricación](production-manage-manufacturing.md)    
[Planificación](production-planning.md)   
[Grupos contables inventario](inventory-manage-inventory.md)  
[Compras](purchasing-manage-purchasing.md)  
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

