---
title: Mover productos en almacenes que usan almacenamiento y picking dirigidos
description: En este producto se explica cómo mover productos en almacenes que usan almacenamiento y picking dirigidos.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.topic: conceptual
ms.date: 02/22/2023
ms.custom: bap-template
ms.search.form: '7351,'
---

# <a name="move-items-in-advanced-warehouse-configurations-that-use-directed-put-away-and-pick"></a><a name="move-items-in-advanced-warehouse-configurations-that-use-directed-put-away-and-pick"></a>Mover productos en configuraciones avanzadas de almacén que usan almacenamiento y picking dirigidos

Puede mover productos entre ubicaciones sin una demanda de un documento de origen. Por ejemplo, es posible que desee hacerlo como parte de las siguientes actividades:

* Reorganizar el almacén.
* Llevar los productos a una zona de inspección.
* Sacar productos de las ubicaciones de picking de almacén temporalmente para utilizarlos como modelos de demostración en una presentación de ventas.
* Mover productos adicionales al área de producción para componentes configurados con algunos métodos de baja.
* Mover productos producidos o ensamblados desde el área de producción o ensamblaje al almacén.
* Mover productos desde el área de almacenamiento masivo hasta las ubicaciones que utilice para picking.

La forma de mover productos depende de si el almacén se configuró como ubicación. Obtenga más información en [Configuración de Warehouse Management](warehouse-setup-warehouse.md).

En las configuraciones de almacén en las que la opción **Picking in almacenamiento dirigidos** está activada para las ubicaciones, puede registrar movimientos no planificados en las siguientes páginas:  

* Hoja trabajo mov.
* Picking interno de almacén
* Almacenamiento interno de almacén
* Diario de reclasificación de almacén

Las páginas **Hoja trabajo movimiento**, **Picking interno de almacén** y **Almacenamiento interno de almacén** funcionan de la misma manera. Utilice las páginas para preparar las actividades de almacén para empleados de almacén. La diferencia está en la funcionalidad avanzada asociada con cada página y los diferentes tipos de actividades de almacén que probablemente realizan los diferentes empleados:

* La hoja de trabajo de movimientos le permite llenar ubicaciones de picking de alto rango con productos de otras ubicaciones
* Los almacenamientos usan plantillas de ubicación
* El picking utiliza la clasificación y la disponibilidad de los contenedores

## <a name="warehouse-movement-worksheet"></a><a name="warehouse-movement-worksheet"></a>Hoja de trabajo de movimiento de almacén

### <a name="to-move-items-with-the-warehouse-movement-worksheet"></a><a name="to-move-items-with-the-warehouse-movement-worksheet"></a>Para mover los artículos con la hoja de cálculo del movimiento de almacén

1. Elija el icono ![Bombilla que abre la característica Dígame](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Hoja trabajo mov.** y, a continuación, elija el vínculo relacionado.  
2. Rellene los campos de las líneas de la hoja de trabajo manualmente o utilice una de las siguientes acciones para rellenar automáticamente las líneas:

    * **Traer conten. ubicac.** rellena las líneas de la hoja de trabajo con el contenido de la ubicación o las ubicaciones que especifique.
    * **Calcular reposición ubicación** utiliza los rankings de ubicación para sugerir la reposición de ubicaciones de ranking superior desde ubicaciones de ranking inferior.

    > [!NOTE]  
    > Si el elemento cumple los criterios de la lista siguiente, los campos **Desde zona** y **Desde ubicación** estarán en blanco. [!INCLUDE [prod_short](includes/prod_short.md)] calcula desde dónde mover los productos solo cuando utiliza la acción **Crear movimiento**.  
    >  
    > * El producto tiene fecha de caducidad.  
    > * El control de alternancia **Picking según FEFO** es desactivado para el almacén.  
    > * Está utilizando característica **Calcular reposición ubicación**.  

3. Elija la acción **Crear movimiento** para crear el movimiento. Cuando el movimiento se completa, puede registrarlo.  

### <a name="to-register-the-warehouse-movement"></a><a name="to-register-the-warehouse-movement"></a>Para registrar el movimiento de almacén

1. Elija el icono ![Bombilla que abre la característica Dígame](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Movimientos** y luego elija el enlace relacionado.  
2. Abra el documento de movimientos para registrarlo.  
3. En las líneas **Colocar**, especifique dónde, qué y cuándo mover el producto en cuestión eligiendo valores en **Cód. zona**, **Cód. ubicación**, **Cdad. a manipular** o **Fecha vencimiento**.  
4. En las líneas **Traer**, especifique en el campo **Cdad. a manipular** y la cantidad del contenido de la ubicación que desea mover. Solo puede editar este campo en las **Traer**. 

    > [!NOTE]
    > Si es necesario realizar el picking o colocar los productos para otra línea en varias ubicaciones porque la ubicación designada está completa, por ejemplo, utilice la acción **Dividir línea** en la ficha desplegable **Líneas**. La acción crea una línea la cantidad restante que se debe administrar.
 
5. Para registrar todas las cantidades sugeridas según lo especificado en el campo **Cantidad**, elija la acción **Autorrellenar el campo Cdad. para manipular**.  
6. Elija la acción **Registrar**.  

> [!NOTE]  
> En el caso de los almacenes que utilizan el almacenamiento y el picking dirigidos, no puede mover artículos manualmente en ubicaciones del tipo **RECIBIR** porque aún no se consideran como inventario disponible. Debe almacenar los artículos en estas ubicaciones antes de que estén disponibles para movimientos.

## <a name="internal-pick"></a><a name="internal-pick"></a>Picking interno

### <a name="to-create-an-internal-pick"></a><a name="to-create-an-internal-pick"></a>Para crear un picking interno

1. Elija el icono ![Bombilla que abre la característica Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Picking interno alm.** y, a continuación, elija el vínculo relacionado.  
2. Seleccione la acción **Nuevo**.
3. Rellene el campo **No.**. **Código de almacén** y el campo **Hasta código de ubicación** de la ficha desplegable **General**. El campo **Hasta código de ubicación** especifica la ubicación donde deea colocar los productos recogidos. Para producción, esta ubicación sería la ubicación de producción de entrada o la ubicación de planta abierta. Para otros fines, seleccione un código de ubicación de tipo ubicación que no se utilice para recogida, probablemente una ubicación especial, de envío o intermedia.  
4. Seleccione un producto en el campo **Nº producto** y rellene las cantidades que desea realizar el picking.  
5. Elija la acción **Crear picking**. Ahora está preparada una instrucción de picking de almacén para que un empelado la ejecute. También puede elegir la acción **Liberar** y crear pickings de almacén utilizando la página **Hoja de trabajo de picking**. Para obtener más información sobre las hojas de trabajo de picking, vaya a [Crear documentos de picking de forma masiva con la hoja de trabajo de picking](warehouse-how-to-pick-items-for-warehouse-shipment.md#to-create-pick-documents-in-bulk-with-the-pick-worksheet).
6. Cuando el picking se completa, puede registrarlo.  

### <a name="to-register-the-warehouse-pick"></a><a name="to-register-the-warehouse-pick"></a>Para registrar el picking de almacén

1. Elija el icono ![Bombilla que abre la característica Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Picking** y luego elija el enlace relacionado.  

    Para trabajar con un picking determinado, seleccione el picking de la lista o filtre la lista para encontrar los pickings que se le han asignado.  
2. Si el campo **Id. usuario asignado** está vacío, escriba el id. para identificarse si es necesario.  
3. Elija los productos.  

    Dado que el almacén está configurado para utilizar el almacenamiento y picking dirigidos, el ranking determina las ubicaciones que se utilizan para picking. Las ubicaciones se sugieren en las líneas de picking. Las instrucciones contienen como mínimo dos líneas independientes para las acciones Traer y Colocar.  

4. Después de terminar el picking y colocar los productos en el área de o ubicación de envío, elija la acción **Registrar picking**.  

## <a name="internal-put-away"></a><a name="internal-put-away"></a>Almacenamiento interno

### <a name="to-create-an-internal-put-away"></a><a name="to-create-an-internal-put-away"></a>Para crear un ubicación interna

1. Elija el icono ![Bombilla que abre la característica Dígame](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Almacenamientos internos de almacén** y, a continuación, elija el vínculo relacionado.  
2. Seleccione la acción **Nuevo**.
3. Rellene el campo **No.**. y los campos **Código de ubicación**.
4. Rellene una línea por cada producto que desea mover al almacén. Los campos **N.º de producto** y **Cantidad** son obligatorios.

    > [!NOTE]  
    > Al seleccionar un producto en el campo **N.º producto**, se abrirá la página **Contenidos de ubicaciones** en vez de la página **Productos**. Esta página se abre porque está almacenando producto que está asignado a una ubicación determinada, el *contenido de ubicación*, no solo un producto y ya conoce la ubicación desde la que se debe traer el producto. Si rellenó el campo **Desde código de ubicación**, el contenido del contenedor se filtrará por ese valor.

5. Para rellenar las líneas con todo el contenido de la ubicación o la ubicación filtrada de las ubicaciones del almacén, elija la acción **Obtener contenido de ubicación**.  
6. Seleccione la acción **Crear ubicación**. Ahora está preparada una instrucción de ubicación de almacén para un empelado de almacén. También puede elegir la acción **Liberar** para crear almacenamientos de almacén utilizando la página **Hoja de trabajo de almacenamiento**. Para obtener más información sobre las hojas de trabajo de almacenamiento, vaya a [Crear documentos de almacenamiento de forma masiva con la hoja de trabajo de almacenamiento](warehouse-how-to-put-items-away-with-warehouse-put-aways.md#to-create-put-away-documents-in-bulk-with-the-put-away-worksheet).
6. Cuando el almacenamiento se completa, puede registrarlo.  

### <a name="to-register-the-warehouse-put-away"></a><a name="to-register-the-warehouse-put-away"></a>Para registrar el almacenamiento de almacén

1. Elija el icono ![Bombilla que abre la característica Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Ubicaciones** y luego elija el enlace relacionado.
2. Abra el almacén la almacenamiento que está preparado para manipular.  
3. Si es necesario, indique su identificador de usuario cuando comience a trabajar en un almacenamiento.  

    Para optimizar el proceso de almacenamiento, puede ordenar las líneas de almacenamiento según varios criterios. Por ejemplo, por producto, número de estantería o fecha de vencimiento.

    * Si las líneas Traer y Colocar de cada línea de recepción no están una a continuación de otra y desea que lo estén, puede ordenar las líneas seleccionando **Producto** en el campo **Método ordenación**.  
    * Si las clasificaciones de ubicaciones reflejan el diseño físico del almacén, utilice el método de clasificación **Clasificación de ubicaciones** para organizar el trabajo en torno a los almacenes de las ubicaciones.  

4. Efectúe el almacenamiento.

    Cada línea de almacenamiento interno se ha convertido en al menos dos líneas en la ubicación de almacén.  

    * La primera línea, con **Traer** en el campo **Tipo acción**, indica dónde están colocados los productos en el área de recepción. En esta línea no puede cambiar la zona y ubicación.  
    * La siguiente línea, con **Colocar** en el campo **Tipo acción**, muestra dónde debe colocar los productos en el almacén. Si recibe muchos productos en una línea de recepción, quizá deba colocarlos en varias ubicaciones a fin de tener una línea Colocar en cada ubicación.  

5. Cuando haya colocado todos los productos en ubicaciones como se le ha indicado, elija la acción **Registrar ubicación**.  

## <a name="to-register-a-movement-that-has-already-happened"></a><a name="to-register-a-movement-that-has-already-happened"></a>Para registrar un movimiento que ya ha ocurrido

Si debe registrar que los productos ya se han movido a otras ubicaciones sin almacenamiento, picking o movimiento, puede usar la página **Diario reclasificación almacén** para registrar el movimiento.

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Diario reclasificación almacén** y luego elija el enlace relacionado.  
2. Rellene los campos **Nº producto**, **Desde cód. zona**, **Desde cód. ubicación**, **Hasta cód. zona**, **Hasta cód. ubicación**.  
3. Elija la acción **Registrar**.  

## <a name="see-related-microsoft-training"></a><a name="see-related-microsoft-training"></a>Consultar la [formación de Microsoft](/training/modules/manage-internal-warehouse-processes/) relacionada

## <a name="see-also"></a><a name="see-also"></a>Consulte también

[Información general de la gestión de almacenes](design-details-warehouse-management.md)
[Inventario](inventory-manage-inventory.md)  
[Configuración de Warehouse Management](warehouse-setup-warehouse.md)  
[Gestión de ensamblaje](assembly-assemble-items.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
