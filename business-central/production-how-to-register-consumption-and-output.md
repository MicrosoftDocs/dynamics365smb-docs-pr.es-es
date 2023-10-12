---
title: Registrar salida de consumo para orden de producción
description: Este tema explica cómo registrar el consumo y la salida para una línea de orden de producción liberada que se ve en la página Diario de producción.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: 5510
ms.date: 03/08/2023
ms.author: bholtorf
---
# <a name="register-consumption-and-output-for-one-released-production-order-line"></a>Registrar el consumo y la salida de una línea de orden de producción lanzada

Esta tarea se realiza en la página **Diario de producción**. El diario combina las funciones del diario de consumo y de los diarios de salida en un único diario, al que se tiene acceso directamente desde una orden de producción lanzada. La finalidad principal de este diario es registrar manualmente el consumo de componentes, la cantidad de los productos finales fabricados y el tiempo empleado en las operaciones. Su finalidad principal es registrar manualmente el consumo de componentes, la cantidad de productos finales fabricados y el tiempo dedicado a las operaciones. Los valores se registran en los movimientos de contabilidad bajo la orden de producción lanzada. Las cantidades de consumo se registran como movimientos de producto negativos, las cantidades de salida se registran como movimientos positivos y los tiempos invertidos se registran como movimientos de capacidad. Estos valores registrados se pueden consultar también en la parte inferior del diario como cantidades reales.  

> [!NOTE]  
> Puesto que los datos de consumo se procesan conjuntamente con los datos de salida, este diario permite mostrar componentes y operaciones vinculadas en una estructura de proceso lógica. Los componentes se muestran con sangría bajo la operación respectiva. Esto necesita que utilice códigos de vínculo de ruta.  

> [!NOTE]  
> los componentes sin códigos de conexión aparecen al principio del diario.  

## <a name="to-register-consumption-and-output"></a>Para registrar el consumo y la salida

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **O.P. lanzadas** y, a continuación, elija el vínculo relacionado.  
2. Abra una línea de orden de producción lanzada que esté lista para su registro. En la ficha desplegable **Líneas**, seleccione la acción **Línea** y, a continuación, elija la acción **Diario de producción**.  

    La página **Diario de producción** se abre y muestra las líneas de diario para la línea de orden de producción según las páginas **Componente orden producción** y **Ruta orden producción**. Estas líneas proceden de la L.M. de producción y la ruta asignados al producto que se está fabricando. Para obtener más información, consulte [Crear L.M. de producción](production-how-to-create-routings.md).  

3. En el campo **Fecha registro** situado en la parte superior del diario, especifique una fecha de registro que se aplique a todas las líneas. La fecha de trabajo se especifica de forma predeterminada. Este campo constituye un método rápido de alinear las fechas de registro en todas las líneas, si es necesario.  

    > [!NOTE]  
    >  Las fechas de registro especificadas en líneas individuales reemplazarán a la fecha de este campo.  

4. En el campo **Filtrar por método de baja** situado en la parte superior del diario, puede elegir ver el consumo y la salida registrados automáticamente de acuerdo con los métodos de baja definidos para el producto y el recurso, respectivamente. Para obtener más información, consulte [Procedimiento: Habilitar el vaciado de componentes según la producción de la operación](production-how-to-flush-components-according-to-operation-output.md).

5. Empiece a especificar las cantidades pertinentes de consumo y salida en los campos editables.  
  
    En cada tipo de línea del diario, solo se muestran los campos correspondientes. Los demás están en blanco y protegidos contra escritura.  

    Al abrir el diario, éste se predefine con las cantidades que se van a registrar. Si hasta el momento no se ha registrado nada, todos los campos de cantidad mostrarán de forma predeterminada las cantidades esperadas procedentes de la orden de producción. Si se han realizado registros parciales, los campos de cantidad de las líneas mostrarán las cantidades restantes. Las cantidades y los tiempos ya registrados para la orden se muestran en la parte inferior del diario como movimientos reales.  

    En cuanto a las cantidades del campo **Cantidad salida**, puede configurar los valores que aparecerán predefinidos al abrir por primera vez el diario. Esta operación se realiza en la página **Configuración fabricación**, ficha desplegable **General**, en el campo **Cantidad de salida predefinida**.

    > [!NOTE]  
    >  Al registrar el diario, sólo la cantidad de salida de la última línea del diario con tipo de movimiento **Salida** ajustará el nivel de inventario. Por lo tanto, no registre el diario con la cantidad de salida esperada predefinida en la última línea de salida hasta que se hayan fabricado realmente todos los productos finales.  

6. Seleccione el campo **Terminada** de las líneas de salida para indicar que la operación ha terminado. Este campo se relaciona con **Estado de ruta** de la línea de ruta de una orden de producción.  
7. Seleccione la acción **Registrar** para registrar las cantidades que ha especificado y, a continuación, cierre el diario.  

    [!INCLUDE [preview-posting-inventory](includes/preview-posting-inventory.md)]

    Si quedan valores para registrar, el diario contendrá dichos valores la próxima vez que se abra. Los valores registrados se muestran como valores reales en la parte inferior del diario.  

    > [!NOTE]  
    >   si un producto que se está consumiendo está bloqueado, el diario no registrará las cantidades de consumo de dicho producto. Si un centro de máquina o de trabajo está bloqueado, el diario no registrará las cantidades de salida ni los tiempos de proceso para la línea de salida correspondiente.  

    > [!NOTE]  
    > si cierra el diario sin realizar ningún registro, se perderán los cambios.  

> [!WARNING]  
> La página **Diario de producción** no se puede utilizar por dos usuarios simultáneamente. Esto significa que si el usuario 2 abre la página e introduce datos cuando el usuario 1 ya está trabajando en la página, el usuario 2 puede perder los datos cuando el usuario 1 cierre la página.  

## <a name="see-also"></a>Consulte también

[Fabricación](production-manage-manufacturing.md)  
[Configuración de fabricación](production-configure-production-processes.md)  
[Planificación](production-planning.md)  
[Inventario](inventory-manage-inventory.md)  
[Compras](purchasing-manage-purchasing.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
