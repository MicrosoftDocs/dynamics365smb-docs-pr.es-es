---
title: Bajar componentes según la salida de la operación
description: Para los productos que se configuran con el método de baja hacia atrás, el comportamiento predeterminado es calcular y registrar el consumo de componentes cuando cambie el estado de una orden de producción lanzada a Terminada.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: d1448b9105426103d70abfb820bd38b6adb41db8
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 03/31/2021
ms.locfileid: "5779258"
---
# <a name="flush-components-according-to-operation-output"></a>Bajar componentes según la salida de la operación
Puede definir diferentes estrategias de baja para automatizar el registro de consumo de componentes. 

Por ejemplo, si una orden de producción para producir 800 metros requiere 8 kg de un componente, cuando se registran 200 metros como salida, se registran automáticamente 2 kg de consumo. 

Esta funcionalidad se útil por los motivos siguientes:  

- **Valoración inventario**

    Los movimientos de valores para la salida y el consumo se crean en paralelo según progresa la orden de producción. Sin los códigos de vínculo de ruta, el valor de inventario aumentará mientras se registra salida y después disminuirá en un momento posterior cuando el valor del consumo de componentes se registra con la orden de producción terminada.  
- **Disponibilidad stock**

    Con el registro gradual del consumo, la disponibilidad de productos de componentes está más actualizado, que es importante para mantener los saldos internos entre la demanda y el suministro. Sin los códigos de vínculo de ruta, otras demandas para el componente pueden creer que está disponible mientras se encuentre pendiente un registro retrasado del consumo.  
- **A tiempo**

    Con la posibilidad de personalizar los productos para las solicitudes de cliente, puede minimizar la pérdida de tiempo de asegurarse de que solo se produzcan cambios de trabajo y del sistema si es necesario.  

Puede lograrlo combinando códigos de vínculo de ruta y baja hacia atrás de modo que la cantidad que se baja para cada operación es proporcional a la salida real de la operación terminada. Para los productos que se configuran con el método de baja hacia atrás, el comportamiento predeterminado es calcular y registrar el consumo de componentes cuando cambie el estado de una orden de producción lanzada a **Terminada**. Si también define los códigos de vínculo de ruta, el cálculo y el registro se producen cuando termina cada operación, y se registra la cantidad realmente consumida en la operación. Para obtener más información, consulte [Crear rutas](production-how-to-create-routings.md).  

## <a name="to-flush-components-according-to-operation-output"></a>Para bajar componentes según la salida de la operación

1.  Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Productos** y luego elija el enlace relacionado.  
2.  Seleccione la acción **Editar**.  
3.  En la ficha desplegable **Reposición**, en el campo **Método de baja**, seleccione **Atrás**.  

    > [!NOTE]  
    >  Seleccione **Pick+ Atrás** si el componente se utiliza en un almacén que está configurado para la ubicación y picking directos.  

4.  Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Rutas** y luego elija el enlace relacionado.  
5.  Defina los códigos de vínculo de ruta para cada operación que consume el componente. Para obtener más información, consulte [Crear rutas](production-how-to-create-routings.md).  
    > [!IMPORTANT]  
    > No use la misma conexión de ruta para diferentes operaciones en la ruta, ya que provocará el registro del consumo de componente para cada operación vinculada.  
6.  Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **L.M. de producción** y luego elija el enlace relacionado.  
7.  Defina los códigos de vínculo de ruta desde cada instancia del componente hasta la operación donde se consume.

El consumo se registrará automáticamente cuando registre la salida. Para obtener más información, consulte [Registro de salida y tiempos de ejecución por lotes](production-how-to-post-output-quantity.md)

## <a name="flushing-methods"></a>Métodos de baja

En la siguiente tabla se describen las opciones de métodos de baja disponibles que puede especificar en las fichas **Producto** y **Unidad de almacenamiento**.

|Opción|Descripción|
|------------|-------------|  
|Manual|Requiere introducir y registrar manualmente el consumo en el diario de consumo.|
|Adelante|Registra el consumo automáticamente según las líneas de componentes de la orden de producción. <br><br>De manera predeterminada, el registro de consumo de componentes tiene lugar cuando se cambia el estado de una orden de producción a **Lanzados**. Sin embargo, si utiliza el campo de **Cód. conexión ruta** de las líneas de componentes de la orden de producción, el registro se realiza para cada operación cuando la operación comienza. Para obtener más información, consulte [Procedimiento: creación de conexiones de ruta](production-how-to-create-routings.md#to-create-routing-links). <br><br> **Nota**<br>Para una baja hacia adelante, el registro operación-específica que se obtiene con códigos de conexión de ruta se basa en la cantidad prevista que se define en la línea de componente. Para obtener información acerca de operación-específico basado en la salida real, vea panorama de **Atrás** en este tema.<br><br>Si el almacén o recursos donde se consume este componente se establece con una estructura de la ubicación predeterminada, en ese caso se consume el producto de **Abre cód. ubic. control planta**. Para obtener más información, consulte [Procedimiento: configurar almacenes básicos con áreas de operaciones](warehouse-how-to-set-up-basic-warehouses-with-operations-areas.md). <br><br> **Importante** <br>La baja futura también tiene lugar cuando elija **Actualizar** en una orden de producción lanzadas que se creó desde cero. En estas órdenes de producción lanzadas creadas directamente, no puede cambiar la información de ubicación porque se generan las líneas de componentes de la orden de producción al actualizar el pedido, que a la vez consume por adelantado los componentes. Por lo tanto, si desea modificar la información de ubicación en las líneas de componente de orden de producción antes de producirse la baja hacia adelante, a continuación el pedido se debería crear tienen el estado *Planificada* o *Planificada en firme*.|
|Atrás|Calcula y registra el consumo automáticamente según las líneas de componentes de la orden de producción.<br><br> De forma predeterminada, el cálculo y registro de consumo de componentes tiene lugar cuando se cambia el estado de una orden de producción lanzada a **Terminada**. Sin embargo, si utiliza el campo de **Cód. conexión ruta** de las líneas de componentes de la orden de producción, el cálculo y registro se realiza cuando cada operación finaliza.<br><br> **Nota** <br>La baja hacia atrás y la ruta de los códigos de conexión pueden combinar de modo que la cantidad de baja por operación sea proporcional a la salida real de esa operación. Para obtener más información, consulte [Procedimiento: bajar componentes según la salida de la operación](#to-flush-components-according-to-operation-output).<br><br> Si el almacén o centro de máquina donde se consume este componente se establece con una estructura de la ubicación predeterminada, en ese caso se consume el producto de **Abre cód. ubic. control planta**.|
|Pick + Adelante|El mismo que para el método de baja hacia adelante, a menos que trabaje solo en almacenes que utilizan ubicación y picking directos.<br><br> El consumo se calcula y se registra de la ubicación que se define en el campo de **Cód. ubic. para producción** de la ubicación o el centro de máquina una vez realizado el picking del componente de almacén.<br><br> **Nota** <br>Si un componente se establece con el método de baja Pick + Adelante, no puede tener un código de conexión de ruta a una operación que se configura con el método de baja hacia adelante. A continuación se realizará automáticamente la baja del componente cuando la operación comienza, lo que hace imposible solicitar la actividad de picking.|
|Pick + Atrás|El mismo que para el método de baja hacia atrás, a menos que trabaje solo en almacenes que usan ubicación y picking directos.<br><br> El consumo se calcula y se registra de la ubicación que se define en el campo de **Cód. ubic. para producción** de la ubicación o el centro de máquina una vez realizado el picking del componente de almacén.|

## <a name="see-also"></a>Consulte también

[Crear LM de producción](production-how-to-create-production-boms.md)  
[Configuración de fabricación](production-configure-production-processes.md)  
[Fabricación](production-manage-manufacturing.md)  
[Planificación](production-planning.md)  
[Inventario](inventory-manage-inventory.md)  
[Compras](purchasing-manage-purchasing.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
