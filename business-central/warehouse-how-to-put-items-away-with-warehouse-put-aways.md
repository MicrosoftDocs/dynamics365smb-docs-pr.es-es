---
title: Almacenar productos con almacenamientos de almacén
description: Obtenga información sobre las diferentes formas de usar los almacenamientos de almacén para almacenar los productos recibidos.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.service: dynamics365-business-central
ms.topic: how-to
ms.date: 01/24/2023
ms.custom: bap-template
ms.search.forms: '7352, 7333'
---
# <a name="put-items-away-with-warehouse-put-aways"></a>Ubicar productos con ubic. exist. almacén

En [!INCLUDE[prod_short](includes/prod_short.md)], la recepción y la ubicación se realizan mediante uno de los cuatro métodos, como se describe en la siguiente tabla.

|Método|Proceso de salida|Recepciones requeridas|Ubicaciones requeridas|Nivel de complejidad (Obtenga más información en [Descripción general de la gestión de almacenes](design-details-warehouse-management.md))|  
|------------|---------------------|--------------|----------------|------------|  
|A|Registro de la recepción y ubicación desde la línea de pedido|||No hay ninguna actividad de almacén dedicada.|  
|B|Registro de la recepción y ubicación desde un documento de ubicación del inventario||Activado|Básico: Pedido por pedido|  
|P|Registro de la recepción y ubicación desde un documento de recepción de almacén|Activado||Básico: Publicación consolidada de recepción/envío para múltiples pedidos.|  
|D|Registro de la recepción desde un documento de recepción de almacén y registro de ubicación desde un documento de ubicación de almacén|Activado|Activado|Avanzado|  

Obtenga más información en [Flujo de entrada en almacén](design-details-inbound-warehouse-flow.md).

Este artículo hace referencia al método D de la tabla y supone que ya se ha efectuado la recepción. Obtenga más información en [Recibir productos](warehouse-how-receive-items.md).

Si un almacén está configurado para requerir el procesamiento de almacenamiento de almacén y recepción de almacén, utilice la función de documentos de almacenamiento almacén para controlar cómo se almacenan los productos. Cuando registra una recepción de almacén, se actualizan los documentos de origen, como la compra, la transferencia entrante o los pedidos de devolución de ventas. La cantidad recibida se registra en el libro mayor de productos y las líneas de los productos recibidos se envían a la función de almacenamiento en el almacén.

Según el valor del campo **Usar hoja de trabajo de almacenamiento** en la **Tarjeta de almacenamiento**, las líneas bien estarán disponibles para la hoja de trabajo del almacenamiento o se usarán para generar documentos de almacenamiento inmediatamente. Obtenga más información en [Configuración de Warehouse Management](warehouse-setup-warehouse.md).  

Además de las formas estándar de crear los almacenamientos de almacén que se describen en este artículo, puede crear los almacenamientos desde la recepción de almacén registrada relacionada. Esta acción es útil si tiene líneas de almacenamiento eliminadas y ha decidido no utilizar la hoja de trabajo de almacenamiento, porque crear o volver a crear las instrucciones de almacenamiento desde líneas de recepción registradas.

## <a name="zone-and-bin-codes"></a>Códigos de zona y ubicación

En los almacenes que se configuran para utilizar el almacenamiento y el picking dirigidos, se requieren los parámetros siguientes para determinar el mejor lugar para colocar los productos:  

* Se configura una plantilla de ubicación. Para obtener más información, vea [Configurar plantillas de almacenamiento](warehouse-how-to-set-up-put-away-templates.md).  
* Se define el peso, cubicaje y requisitos especiales de almacenamiento del producto o la unidad de almacenamiento.
* Se definen para las ubicaciones la capacidad, tipo de ubicación y ranking de las ubicaciones.  

El ranking de las ubicaciones se usa cuando más de una ubicación coincide con el criterio de una plantilla de almacenamiento. Si los criterios de la plantilla de ubicación y el ranking de ubicación son los mismos para varias ubicaciones, se selecciona la ubicación con el número más alto.

## <a name="to-create-put-away-documents-in-bulk-with-the-put-away-worksheet"></a>Para crear documentos de almacenamiento de forma masiva con la hoja de trabajo de almacenamiento

Puede crear documentos de almacenamiento para varias recepciones al mismo tiempo en la página **Hoja de trabajo de almacenamiento**.  

1. Elija el icono ![Bombilla que abre la característica Dígame](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Hojas de trabajo de almacenamientos** y luego elija el enlace relacionado.  
2. Seleccione la acción **Traer documentos almacén**. Se abre la página **Selección ubicación**.  

    La lista contiene todas las recepciones registradas que están listas para el almacenamiento, incluidas aquellas para las que ya se han creado instrucciones de almacenamiento. Los documentos con líneas de ubicación que ya se han ubicado y registrado completamente no se muestran en la lista.  
3. Seleccione los documentos en los que desea trabajar. Puede trabajar con líneas de distintos documentos al mismo tiempo.  

    > [!NOTE]  
    >  Si selecciona un documento de recepción o almacenamiento interno para el que ya ha creado instrucciones para todas sus líneas, [!INCLUDE[prod_short](includes/prod_short.md)] le indica que no tiene nada que manipular.  

4. Rellene el campo **Método ordenación** para ordenar las líneas.  

    > [!NOTE]  
    >  La forma en que se ordenan las líneas en la hoja de trabajo no se traslada automáticamente a la instrucción de almacenamiento. Sin embargo, existen las mismas oportunidades de ordenación y clasificación de ubicaciones. Puede crear orden de la línea que planifique en la hoja de trabajo cuando crea las instrucciones de almacenamiento o clasificación en las instrucciones de almacenamiento.

5. Rellene el campo **Cdad. a manipular**. Seleccione la acción **Rellenar cdad. manip. autom.** o rellene los campos manualmente.  
6. Si es necesario, edite las líneas manualmente. Puede eliminar líneas si, por ejemplo, es necesario almacenar algunos productos en una ubicación lejos de las ubicaciones de otros productos.  

    > [!NOTE]  
    > Cuando elimina líneas, solo se eliminan de esta hoja de trabajo. No se eliminan de la lista de selección de almacenamiento.  

7. Seleccione la acción **Crear ubicación**. Se abre la página **Crear documento**, donde puede agregar más información al almacenamiento que está creando.  

    * Puede asignar la ubicación a un empelado determinado.  
    * Puede ordenar las líneas de la instrucción de ubicación como lo hizo en la hoja de trabajo o por ranking de ubicación. Cuando efectúa el orden según la clasificación de la ubicación, las líneas *Traer* aparecen primero, porque la mayoría de las ubicaciones de recepción tienen una clasificación de ubicación 0. Las líneas *Colocar* aparecen al final, comenzando con las ubicaciones con la clasificación de ubicación más baja. Si ha estructurado el almacén para que las ubicaciones de ranking similar estén unas al lado de otras, la ordenación de las líneas de esta forma ahorrará muchos pasos a los empleados de almacén.  
    * Puede optar por no incluir las líneas que [!INCLUDE[prod_short](includes/prod_short.md)] creó cuando convirtió una unidad de medida grande en otras más pequeñas seleccionando el campo **Define filtro div. bulto**. Obtenga más información sobre la carga fraccionada en [Habilitar interrupción automática masiva con almacenamiento y picking dirigidos](warehouse-enable-automatic-breaking-bulk-with-directed-put-away-and-pick.md).  
    * Puede hacer que no se rellene automáticamente el campo **Cdad. a manipular** en las instrucciones de ubicación.  
    * También puede elegir imprimir el documento inmediatamente.  

8. Seleccione **Aceptar** para crear el almacenamiento.  

## <a name="to-create-a-put-away-from-a-posted-receipt"></a>Para crear una ubicación desde una recepción registrada

Si el almacén usa el procesamiento de almacenamiento y de recepción y ha eliminado las líneas de almacenamiento, o si utiliza almacenamiento y picking dirigidos y ha decidido no utilizar la hoja de trabajo de almacenamiento, puede crear o volver a crear las instrucciones de almacenamiento para líneas de recepción registradas.

1. Elija el icono ![Bombilla que abre la característica Dígame](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Recepciones de almacenamiento registradas** y, a continuación, elija el vínculo relacionado.  
2. Seleccione una recepción registrada para almacenar.  
3. Seleccione la acción **Ficha**.  

    Si el campo **Estado documento** está en blanco, la recepción aún no se ha ubicado. En caso contrario, el campo indica si la recepción se ha almacenado parcial o completamente.  

4. Si el albarán se ha ubicado parcialmente o no se ha ubicado, elija la acción **Crear ubicación**.  
5. Rellene los campos según sea necesario y, a continuación, haga clic en **Aceptar**.  

## <a name="to-put-items-away"></a>Para almacenar productos

1. Elija el icono ![Bombilla que abre la característica Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Almacenamientos de almacén** y luego elija el enlace relacionado.

2. Abra el almacén la almacenamiento que está preparado para manipular.  
3. Si el almacén lo necesita, indique su identificador de usuario cuando comience a trabajar en un almacenamiento.  

    Puede ordenar las líneas de almacenamiento por varios criterios, por ejemplo, por producto, número de estante o fecha de vencimiento. La clasificación puede ayudar a optimizar el proceso de almacenamiento, por ejemplo:

    * Si las líneas Traer y Colocar de cada línea de recepción no están una a continuación de otra y desea que lo estén, puede ordenar las líneas seleccionando **Producto** en el campo **Método ordenación**.  
    * Si las clasificaciones de almacenamientos reflejan el diseño físico del almacén, utilice el método de clasificación **Clasificación de ubicaciones** para organizar el trabajo en torno a los almacenes de las ubicaciones.

4. Realizar las acciones.

    Si un código de ubicación es obligatorio para los almacenes, cada línea de recepción se convierte en al menos dos líneas en el almacenamiento almacén de la siguiente manera.  

    * La primera línea, con **Traer** en el campo **Tipo acción**, indica dónde están colocados los productos en el área de recepción. En esta línea no puede cambiar la zona y ubicación.  
    * La siguiente línea, con **Colocar** en el campo **Tipo acción**, muestra dónde debe colocar los productos en el almacén. Si recibe muchos productos en una línea de recepción, quizá deba colocarlos en varias ubicaciones a fin de tener una línea Colocar en cada ubicación. 

    > [!NOTE]
    > Si es necesario colocar los productos para otra línea en varias ubicaciones porque la ubicación designada está completa, por ejemplo, utilice la acción **Dividir línea** en la ficha desplegable **Líneas**. La acción crea una línea la cantidad restante que se debe administrar.

5. Cuando haya colocado todos los productos en ubicaciones como se le ha indicado, elija la acción **Registrar ubicación**.  

## <a name="see-also"></a>Consulte también .

[Información general de la gestión de almacenes](design-details-warehouse-management.md)
[Inventario](inventory-manage-inventory.md)  
[Configuración de Warehouse Management](warehouse-setup-warehouse.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
