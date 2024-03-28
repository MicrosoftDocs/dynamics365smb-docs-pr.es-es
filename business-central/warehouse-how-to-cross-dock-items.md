---
title: Productos de tránsito directo
description: Aprenda a recibir y enviar productos sin almacenarlos.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.date: 10/09/2023
ms.custom: bap-template
ms.search.form: '15, 5703, 7302, 7332, 5768'
ms.service: dynamics-365-business-central
---
# Productos de tránsito directo

Los productos de tránsito directo son productos que recibe y envía sin almacenarlos. Los procesos de ubicación y picking requieren un manejo limitado de productos. Puede realizar el tránsito directo de productos para los envíos y los pedidos de producción.

## Ubicaciones de tránsito directo y zonas

Si está utilizando ubicaciones, configure al menos una ubicación de tránsito directo y luego especifique la ubicación en el campo **Cód. ubicac. tránsito directo** en sus ubicaciones. Si utiliza la colocación dirigida y pickings, establezca una zona de tránsito directo.

Cuando se prepara un envío o se realiza un picking de productos para producción y utiliza ubicaciones, se realizará el picking del producto automáticamente desde una ubicación de tránsito directo antes de considerar el picking desde cualquier otra ubicación. Debe comprobar si los productos que necesita están disponibles en el área tránsito directo antes de traerlos a su área de almacenamiento habitual.  

Si ha calculado cantidades de tránsito directo, las líneas de ubicación a la ubicación de tránsito directo para los cálculos de tránsito directo se crean al registrar la recepción. Las otras líneas de ubicación se crean normalmente.  

## Líneas de selección de tránsito directo para un recibo

Si desea registrar los productos de tránsito directo directamente, para hacerlos disponibles para picking, registre también una ubicación para el resto de productos que se originan desde las líneas de recepción, es decir, los que se tienen que almacenar. Si sólo se va a realizar el tránsito directo de algunos productos de la línea de recepción, debe hacer el esfuerzo de ubicar el resto de los productos tan pronto como sea posible. Alternativamente, su política de almacén podría impulsar el tránsito directo de líneas de recepción completas siempre que sea posible.

En la instrucción de almacenamiento, elimine las líneas de instrucción de Traer y colocar para cada línea de recepción de los productos que se van a almacenar. Puede recrear las líneas de instrucción posteriormente como líneas de ubicación desde la hoja de trabajo de ubicación o la recepción registrada. Tras eliminar las líneas de instrucción puede ubicar y registrar las líneas para productos en tránsito directo.  

## Acerca de la página de horas de trabajo de almacenamiento

Si activa el botón de alternancia **Utiliza hoja de trabajo de almacenamiento** de la página **Tarjeta de ubicación** y contabiliza la recepción con tránsitos directos calculados, todas las líneas de la recepción están disponibles en la hoja de trabajo. La información de tránsito directo se pierde y no puede volver a crearse. Por tanto, para utilizar la funcionalidad de tránsito directo, debe pasar las líneas a la hoja de trabajo de ubicación eliminando las instrucciones de ubicación en vez de utilizar la función de paso automático que proporciona el campo **Utiliza hoj. trab. ubicación**.  

Si registra la recepción de almacén y el botón de alternancia **Utilizar hoja de trabajo de almacenamiento** está desactivado, los productos de tránsito directo se convierten en líneas independientes en las instrucciones de almacenamiento. El campo **Información tránsito directo** en cada línea de almacenamiento muestra si la línea contiene lo siguiente:

* Productos de tránsito directo
* Todos los productos de un recibo deben almacenarse.
* Algunos productos de un recibo se deben almacenar y otros se deben cruzar en tránsito.

[!INCLUDE [prod_short](includes/prod_short.md)] no mantiene registros separados para productos con tránsito directo. Las registra como instrucciones de almacenamiento ordinarias.  

## Para configurar el almacén para tránsito directo  

1. Si utiliza ubicaciones configure al menos una ubicación de tránsito directo. Si utiliza la colocación dirigida y pickings, establezca una zona de tránsito directo.  

    Una ubicación de tránsito directo tiene el campo **Contenedor de tránsito cruzado** seleccionado. Para obtener más información sobre los contenedores, vaya a [Crear contenedores](warehouse-how-to-create-individual-bins.md).  

    Si utiliza zonas, cree una para sus ubicaciones de tránsito directo y seleccione el campo **Zona ubicac. tráns. directo**. Si utiliza almacenamiento y selecciones dirigidas, seleccione el tipo de ubicación con **Picking** seleccionado; por ejemplo, puede usar *PICK* o *PUTPICK*. Para obtener más información sobre zonas y tipos de contenedores, vaya a [Configurar ubicaciones para usar contenedores](warehouse-how-to-set-up-locations-to-use-bins.md) y [Configurar tipos de contenedores](warehouse-how-to-set-up-bin-types.md).  

2. Elija el icono ![Bombilla que abre la característica Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), , escriba **Ubicación** y luego elija el enlace relacionado.  
3. En la página **Ubicación**, seleccione la ubicación cuyo tránsito directo del almacén desee configurar y, a continuación, elija la acción **Editar**.  
4. En la ficha desplegable **Almacén**, active el botón de alternancia **Utilizar tránsito directo** y rellene al campo **Calcular fecha vto. tráns. directo** con el periodo de tiempo que el sistema anticipará la búsqueda de oportunidades de tránsito directo.

    La opción **Utiliza tránsito directo** sólo está disponible si ha seleccionado los campos **Recepción requerida**, **Envío requerido**, **Picking requerido** y **Ubicación requerida**.  

5. Si utiliza ubicaciones, en la ficha desplegable **Ubicaciones**, rellene el campo **Código de ubicación de tránsito directo** con el código de la ubicación que desea utilizar como ubicación de tránsito directo genérica.  
6. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Ud. de almacenam.** y, a continuación, elija el vínculo relacionado.  
7. Para cada artículo o unidad de almacenamiento donde desea que se pueda realizar el tránsito directo, seleccione el artículo y, a continuación, elija la acción **Editar**.
8. En la página **Ficha ud. de almacenam.**, active la casilla **Utilizar tránsito directo**.  

> [!NOTE]  
>  La funcionalidad de tránsito directo sólo es posible si el almacén está configurado para requerir los procesos de recepción y ubicación.  

## Para realizar el tránsito directo de productos sin ver las oportunidades  

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Recepciones almacén** y luego elija el enlace relacionado.  
2. Cree una recepción de almacén para un producto que ha llegado y puede tener tránsito directo. Para obtener más información sobre recepción, vaya a [Recibir productos](warehouse-how-receive-items.md).  
3. Rellene el campo **Cdad. para recibir** y, a continuación, elija la acción **Calcular tránsito directo**.  

    Se identifican los documentos de origen de salida que solicitan los productos que están programados para salir del almacén en el periodo de tiempo de la fórmula de fecha. [!INCLUDE[prod_short](includes/prod_short.md)] calcula las cantidades para que pueda realizar el tránsito directo en cuanto sea posible y evitar tener que ubicar los productos sin que se amontonen demasiados en el área de tránsito directo. El valor del campo **Cantidad a tránsito directo** es la suma de todas las líneas de salida para el producto en el periodo anticipado menos la cantidad de productos que ya se han colocado en el área de tránsito directo, o es el valor del campo **Cantidad a recibir** de la línea de la recepción, el que sea menor de ambos. No puede realizar el tránsito directo de más productos de los que ha recibido.  

4. Si desea hacer el tránsito directo de la cantidad sugerida, contabilice la recepción. También es posible que decida cambiar la cantidad de la que se va a hacer el tránsito directo y, a continuación, registrar la recepción.  

    Los importes de los que se va a realizar el tránsito directo aparecen como líneas en la instrucción de ubicación, asumiendo que el campo **Utiliza hoj. trab. ubicación** esté desactivado. Las cantidades que no entran en tránsito directo se convierten en líneas en la instrucción de ubicación.  

    Si tiene ubicaciones, los productos de tránsito directo se habrán asignado a la ubicación de tránsito directo genérica definida en la ficha de almacén.  

5. Elimine las líneas **Traer** y **Colocar** de los productos para los que no hará tránsito directo.  
6. Imprima la instrucción de ubicación del resto de las líneas y coloque las cantidades de la recepción que se tienen que almacenar en las ubicaciones o el área de almacén adecuada. Coloque los productos de tránsito directo en el área o la ubicación diseñada para ellos en la política de almacén. A veces, es posible que la política de almacén le requiera dejarlos en el área de recepción.  
7. Para registrar los productos de tránsito directo que se van a ubicar y hacer disponible para picking, elija la acción **Registrar**.  

## Para realizar el tránsito directo de productos después de ver las oportunidades  

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Recepciones almacén** y luego elija el enlace relacionado.  
2. Cree una recepción de almacén para un producto que ha llegado y puede tener tránsito directo.  

    Debe ver las líneas del documento de origen que solicitan el artículo para poder registrar la recepción.  
3. Elija la acción **Calcular tránsito directo**.  

   En la página **Oportunidad tráns.direc.** puede ver los detalles más importantes de las líneas que solicitan el producto, como el tipo de documento, la cantidad solicitada y la fecha de vencimiento. Esta información puede ayudarle a decidir la cantidad de producto de tránsito directo, dónde colocar los productos en el área de tránsito directo o cómo agruparlos.  

4. Elija la acción **Rellenar cantidad de tránsito directo** para mostrar cómo se calculan las cantidades en las líneas de la recepción. Cuando se modifica el número de productos en el campo **Cantidad en tránsito directo** en cada línea, se actualiza el cálculo. La actualización no significa que el envío o la orden de producción recibirán en realidad los productos sugeridos para tránsito directo. Es solo con fines de prueba. No obstante, el proceso puede ser informativo si está implicada más de una unidad de medida.  
5. Para reservar una cantidad de producto para una línea de pedido determinada, elija la línea y, a continuación, elija la acción **Reservar**. En la página **Reserva**, reserve la cantidad disponible del producto. La reserva es como cualquier otra, y no tiene mayor prioridad porque se haya creado junto con el tránsito directo. Para obtener más información sobre reservas, vaya a [Reservar productos](inventory-how-to-reserve-items.md).   
6. Al terminar el cálculo o la reserva, elija el botón **Aceptar** para traer los cálculos al campo **Cantidad a tránsito directo** de la línea de la recepción, o seleccione el botón **Cancelar** si desea volver a la recepción de almacén, donde puede calcular de nuevo el tránsito directo.  
7. Contabilice la recepción. Puede continuar con las instrucciones de ubicación tal como se describe en los pasos 3 a 7 en la sección [A los productos de tránsito directo sin consultar las oportunidades](#to-cross-dock-items-without-viewing-the-opportunities).  

    [!INCLUDE [preview-posting-inventory](includes/preview-posting-inventory.md)]

    > [!NOTE]  
    > En la ubicación de almacén, puede continuar cambiando las cantidades que se van a ubicar en el almacén o de las que se va a realizar el tránsito directo, según sea necesario. Por ejemplo, es posible que decida realizar un tránsito directo de una cantidad adicional para simplificar el registro de tránsito directo.  

## Para ver productos de tránsito directo en un envío u hoja de trabajo de picking  

Si utiliza ubicaciones, al abrir un envío o una hoja de trabajo de selección, un cálculo actualizado de la cantidad de cada producto en las actualizaciones de ubicaciones de tránsito directo. Al ver que el producto está disponible en la ubicación de tránsito directo, puede crear rápidamente una selección de todos los productos del envío. En la hoja de trabajo de selección, puede editar las líneas según sea necesario.  

Al lanzar una orden de producción, las líneas están disponibles en la hoja de trabajo de selección y el campo **Cantidad en ubicación de tránsito directo** muestra si los productos han llegado y están en las ubicaciones de tránsito directo. Al crear una instrucción de selección, [!INCLUDE [prod_short](includes/prod_short.md)] sugiere que seleccionará primero los productos de tránsito directo. Los productos en ubicaciones de almacenamiento se sugieren después.  

Si no utiliza ubicaciones, recuerde comprobar el área de tránsito directo de vez en cuando o deberá confiar en las notificaciones de recepción de que han llegado productos para producción.  

## Consulte también  

[Inventario](inventory-manage-inventory.md)  
[Configuración de Warehouse Management](warehouse-setup-warehouse.md)     
[Gestión de ensamblaje](assembly-assemble-items.md)    
[Información general de la gestión de almacenes](design-details-warehouse-management.md)
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
