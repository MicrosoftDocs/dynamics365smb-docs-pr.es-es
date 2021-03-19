---
title: Crear Rutas | Documentos de Microsoft
description: Una ruta contiene los datos maestros que capturan los requisitos del proceso de un producto fabricado específico. Una vez creada la orden de producción para ese producto principal, la ruta controlará la programación de operaciones tal como se representan en la página Ruta orden producción bajo la orden de producción.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 3f1fd0b3ff6b300586c3932901a900c500172ba8
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5384104"
---
# <a name="create-routings"></a>Creación de rutas

Las empresas con procesos de fabricación utilizan las rutas para visualizar y dirigir el funcionamiento de los mismos.

La ruta es también la base para la programación del proceso, la programación de la capacidad, la programación de la asignación de los materiales necesarios y los documentos de fabricación.  

En función de la L.M. de producción, las rutas se asignan al producto final de fabricación. Una ruta contiene los datos maestros que capturan los requisitos del proceso de un producto fabricado específico. Una vez creada la orden de producción para ese producto principal, la ruta controlará la programación de operaciones tal como se representan en la página **Ruta orden producción** bajo la orden de producción.  

Para poder configurar una ruta, lo siguiente debe existir:  

- Se deben crear fichas de producto para los productos principales que forman parte de la fabricación. Para obtener más información, vea [Registrar nuevos productos](inventory-how-register-new-items.md).
- Se han configurado recursos de producción. Para obtener más información, consulte [Configurar centros de trabajo y centros de máquina](production-how-to-set-up-work-and-machine-centers.md).

## <a name="to-create-a-routing"></a>Para crear una ruta

1. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Rutas** y luego elija el enlace relacionado.  
2. Seleccione la acción **Nuevo**.  
3. Rellene los campos según sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. En el campo de **Tipo**, seleccione **Número de serie** para calcular la ruta de producción según el valor del campo de **Nº operación** .  
    Seleccione **Paralelo** para calcular las operaciones según el valor del campo de **Nº operación siguiente** .  
5. Para editar la ruta, establezca el campo **Estado** en **Nueva** o **En desarrollo**. Para activarla, establezca el campo **Estado** en **Certificada**.  

    Proceda a rellenar las líneas de ruta.
6. En el campo **Nº operación** especifique el número de la primera operación, por ejemplo **10**.  
7. En el campo **Tipo**, especifique qué tipo de recurso se utiliza, por ejemplo **Centro trabajo**.  
8. En el campo **N.º**, seleccione el recurso que se va a utilizar o especifíquelo en el campo.  
9. En el campo **Código de conexión de ruta**, introduzca un código para conectar el componente con una operación específica. Para obtener más información, consulte [Para crear conexiones de ruta](production-how-to-create-routings.md#to-create-routing-links).
10. En los campos **Tiempo ejecución** y **Tiempo preparación**, especifique los tiempos de proceso necesarios para realizar la operación.

     > [!NOTE]
     > El tiempo de preparación se calcula para cada orden de producción, mientras que el tiempo de ejecución se calcula para cada producto fabricado.  

11. En el campo de **Capacidades concurrentes**, especifique cuántas unidades del recurso seleccionado se van a utilizar para realizar la operación. Por ejemplo, dos personas asignadas a una operación de embalaje dividirán por dos el tiempo de ejecución.  
12. Continúe rellenando las líneas para todas las operaciones necesarias para fabricar el producto en cuestión.  
13. Para copiar líneas desde una ruta existente, seleccione la acción **Copiar ruta** para seleccionar las líneas existentes.  
14. Certifique la ruta.  
15. Ahora puede asociar la nueva ruta a la ficha del producto en cuestión, rellenando el campo **Nº de ruta**. Para obtener más información, vea [Registrar nuevos productos](inventory-how-register-new-items.md).  

> [!NOTE]  
> Recuerde también volver a calcular el coste estándar del producto desde la tarjeta **Producto**: Seleccione la acción **Fabricación**, seleccione la acción **Calcular coste estándar** y, a continuación, seleccione la acción **Todos los niveles**.  

## <a name="to-create-routing-links"></a>Para crear conexiones de ruta

Puede crear conexiones de ruta para conectar componentes con operaciones específicas de forma de conservar su relación aunque se modifique la L.M. de producción o la ruta. Estas conexiones permiten también dar de baja puntualmente los componentes, es decir, cuando se inicia la operación conectada específica, no cuando se lanza la orden de producción completa. Para obtener más información, consulte [Bajar componentes según la producción de la operación](production-how-to-flush-components-according-to-operation-output.md).  

Otra ventaja importante es que las operaciones y los componentes conectados se muestran en una estructura de proceso lógica cuando utiliza la página **Diario de producción** para registrar la salida y el consumo.  

1. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Rutas** y luego elija el enlace relacionado.  
2. Abra la ruta que contiene las operaciones que desea conectar.  

    Asegúrese de que el estado de la ruta sea **En desarrollo**.  

3. En la línea de ruta correspondiente, en el campo de **Cód. conexión ruta**, seleccione un código.  
4. Agregue diferentes códigos de conexión de ruta a otras operaciones en la ruta, si procede.  

    > [!NOTE]  
    > No debe utilizar el mismo código de conexión de ruta en operaciones diferentes, ya que se podría conectar de forma incorrecta un componente a dos operaciones distintas y, por tanto, se consumiría dos veces.  
    >
    > Es aconsejable asignar un nombre al código de conexión de ruta detrás de la operación para garantizar que se utilizan conexiones de ruta específicas de la operación.

5. Establezca el estado de la ruta en **Certificada**.  

    Los códigos de vínculo de ruta se asignan ahora a operaciones. Siguiente, debe crear vínculos reales asignando los mismos códigos a los componentes específicos en la L.M. de producción correspondiente.  

6. Abra la **L.M. de producción** que contiene los componentes que desea vincular a las operaciones anteriores. Para obtener más información, consulte [Crear L.M. de producción](production-how-to-create-production-boms.md).
7. Asegúrese de que el estado de la L.M. está **En desarrollo**.  
8. En la línea correspondiente de la L.M. de producción, en el campo de **Cód. conexión ruta**, seleccione el código que se acaba de asignar a la operación correspondiente.  
9. Agregue códigos de conexión de ruta a otros componentes según las operaciones únicas en las que éstos se utilizan.  
10. Establezca el estado de la ruta en **Certificada**.  

    > [!NOTE]  
    > Para activar las conexiones de ruta en una orden de producción existente, debe actualizar la orden de producción. Para obtener más información, consulte [Crear órdenes de producción](production-how-to-create-production-orders.md).  

Los componentes seleccionados se conectarán a las operaciones seleccionadas cuando cree o actualice una orden de producción con la L.M. de producción y ruta en cuestión. Se puede ver en la página **Componentes orden producción** bajo la orden de producción y, en esta misma ventana, puede eliminar y agregar los códigos de conexión de ruta definidos cuando lo desee.

## <a name="to-assign-personnel-tools-and-quality-measures-to-routing-operations"></a>Para asignar personal, herramientas y medidas de calidad a operaciones de ruta

Si necesita personal con una cualificación, conocimiento o autorización especial para una operación, puede asignar este tipo de personal a la operación. Además, puede asignar herramientas y los requisitos de calidad a la operación. Este procedimiento describe cómo asignar personal. Los pasos son parecidos para otros tipos de información de la operación.

1. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Rutas** y luego elija el enlace relacionado.  
2. Abra la ruta pertinente.  
3. En la ficha desplegable **Líneas**, seleccione la línea que desea procesar, elija la acción **Operaciones** y, después, seleccione la acción **Personal**.  
4. Rellene los campos de la página **Personal ruta**.  
5. Elija el botón **Aceptar** para salir de la página. Los valores introducidos se copian y asignan a la operación.  

## <a name="to-create-a-new-versions-of-a-routing"></a>Para crear una versión de ruta nueva

El principio de versión le permite administrar varias versiones de rutas. La estructura de la versión de ruta se corresponde con la de la ruta, la cual se compone de la cabecera y las líneas de la versión de la ruta. La diferencia básica se define mediante la fecha inicial.  

1. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Rutas** y luego elija el enlace relacionado.  
2. Seleccione la ruta a copiar y después seleccione la acción **Versiones**.  
3. En la página **Versiones de rutas**, seleccione la acción **Nuevo**.
4. Rellene los campos según sea necesario.
5. En el campo **Código de versión**, introduzca la identificación única de la versión. Se permite cualquier combinación de letras y números.  

    A la versión que se acaba de crear se le asigna automáticamente el estado **Nueva.**  
6. Para crear líneas de operación, seleccione la primera línea en blanco, y rellene el **Nº de operación** según la secuencia de operaciones.

    Las líneas de operación se ordenan en orden ascendente por número de operación. Para poder realizar cambios posteriormente, se recomienda seleccionar anchos de paso apropiados. El campo **Nº operación siguiente** hace referencia a la siguiente operación. El número de la operación puede escribirse directamente.

7. Cuando la versión de la ruta esté completa, establece el campo **Estado** como **Certificada**.

El periodo de validez de la versión se especifica mediante el campo **Fecha inicial**.  

## <a name="see-also"></a>Consulte también

[Crear LM de producción](production-how-to-create-production-boms.md)  
[Configuración de fabricación](production-configure-production-processes.md)  
[Fabricación](production-manage-manufacturing.md)  
[Planificación](production-planning.md)  
[Inventario](inventory-manage-inventory.md)  
[Compras](purchasing-manage-purchasing.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]