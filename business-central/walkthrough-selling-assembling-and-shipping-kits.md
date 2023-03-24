---
title: 'Vender, ensamblar y enviar kits'
description: 'Para usar el inventario puntual, los pedidos de ensamblado pueden crearse y vincularse automáticamente tan pronto como se cree la línea del pedido de venta.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 06/24/2021
ms.author: edupont
---
# Tutorial: vender, ensamblar y enviar kits

<!-- [!INCLUDE[complete_sample_data](includes/complete_sample_data.md)]   -->

Para usar el inventario puntual y la capacidad de personalizar los productos según las solicitudes del cliente, los pedidos de ensamblado pueden crearse y vincularse automáticamente tan pronto como se cree la línea del pedido de venta. El vínculo entre la demanda de venta y suministro de ensamblado permite a los procesadores de pedidos de venta personalizar el elemento del ensamblado y comprometerse con fechas de entrega según la disponibilidad de los componentes. Además, el consumo y la salida del ensamblado se registran automáticamente con el envío del pedido de venta vinculado.  

La funcionalidad especial existe para controlar el envío de las cantidades tipo ensamblar para pedido, en las configuraciones de almacén tanto básicas como avanzadas. Cuando los trabajadores responsables del ensamblado terminan de montar componentes o toda la cantidad de ensamblar para pedido, la registran en el campo **Cdad. a enviar** de la línea de envío de almacén en las configuraciones avanzadas y luego se debe elegir **Registrar envío**. El resultado es que se registra la salida del ensamblado correspondiente, incluido el consumo de componentes relacionado. También se registra albarán de venta para la cantidad del pedido de venta vinculado. En este tutorial se muestra el proceso de almacén avanzado.  

En configuraciones de almacén básicas, cuando una cantidad de ensamblar para pedido está lista para enviarse, el empleado del almacén responsable registra un picking de existencias para las líneas del pedido de venta. Esto crea un movimiento de inventario para los componentes y registra la salida de ensamblado y el envío del pedido de venta. Para obtener más información, consulte [Gestión de productos de ensamblar para pedido en picking de inventario](warehouse-how-to-pick-items-with-inventory-picks.md#handling-assemble-to-order-items-with-inventory-picks).  

## Acerca de este tutorial

En este tutorial, se demuestran las siguientes tareas:  

### Configurar productos de ensamblado

Los elementos del ensamblado se caracterizan según su sistema de reposición y la L.M. de ensamblado. La directiva de ensamblado del producto puede ser ensamblar para pedido (ATO) o ensamblar para stock (ATS). En esta sección se describen las tareas siguientes:  

-   Configuración del sistema de reposición y la directiva de ensamblado apropiados en una nueva ficha de elemento del ensamblado.  
-   Creación de una L.M. de ensamblado que enumera los componentes del ensamblado y el recurso que forman parte del elemento del ensamblado.  

### Vender elementos del ensamblado personalizados

[!INCLUDE[prod_short](includes/prod_short.md)] proporciona la flexibilidad para introducir una cantidad de inventario y una cantidad de ensamblar para pedido en una línea de pedido de venta. En esta sección se describen las tareas siguientes:  

-   Crear una línea de pedido de venta puramente ATO donde la cantidad completa no está disponible y debe ensamblarse antes del envío.  
-   Personalizar los productos ATO.  
-   Volver a calcular precio unitario de un elemento del ensamblado personalizado.  
-   Crear una línea de pedido de venta mezclada donde partes de la cantidad de venta se proporcionan del inventario y la parte restante se debe ensamblar antes del envío.  
-   Descripción de los avisos de disponibilidad ATO.  

### Planificar para los elementos del ensamblado

La demanda y el suministro del ensamblado los gestiona el sistema de planificación, al igual que en el caso de compras, transferencias y producción. En esta sección se describen las tareas siguientes:  

-   Ejecutar un plan regenerativo para los productos con demanda de venta para el aprovisionamiento ensamblado.  
-   Generar un pedido de ensamblado para satisfacer una cantidad de línea de venta antes de la fecha de envío solicitada.  

### Ensamblar productos

Los pedidos de ensamblado funcionan de forma similar a las órdenes de producción, excepto que el consumo y la salida se graban y se registran directamente desde el pedido. Cuando los productos se ensamblan en el inventario, el trabajador del ensamblado tiene acceso completo a todos los campos de cabecera y línea. Cuando los productos se ensamblan en un pedido donde la cantidad y fecha se han prometido al cliente, determinados campos del pedido de ensamblado no se pueden editar. En ese caso, el registro del ensamblado se realiza a partir del envío de almacén para el pedido de venta vinculado. En esta sección se describen las tareas siguientes.  

-   Grabar y registrar el consumo y salida de ensamblado en el inventario.  
-   Acceder una línea de albarán de almacén desde un pedido de ensamblado ATO de graba el trabajo de ensamblado.  
-   Acceder a un pedido de ensamblado ATO desde una línea de albarán de almacén para revisar los datos especificados automáticamente.  

### Enviar elementos del ensamblado, desde el inventario y ensamblado para pedido

Hay una funcionalidad especial para controlar el envío de las cantidades del ensamblar para pedido. En esta sección se describen las tareas siguientes:  

-   Crear un picking de almacén para los elementos del ensamblado de inventario y para los componentes de ensamblado que se deben ensamblar antes del envío.  
-   Registrar los pickings de almacén para los componentes del ensamblado y luego para los elementos del ensamblado.  
-   Acceder a un pedido de ensamblado desde un envío de almacén para revisar los componentes preparados o consumidos.  
-   Enviar cantidades de ensamblar para pedido.  
-   Enviar elementos del ensamblado de inventario.  

## Funciones

En este tutorial, se demuestran las tareas realizadas por los siguientes roles de usuario:  

-   Procesadora de pedidos de ventas  
-   Planificador  
-   Trabajador del ensamblado  
-   Encargado de picking  
-   Responsable de envío  

## Requisitos previos

Para poder realizar las tareas del tutorial, deberá hacer lo siguiente:  

-   Instalar [!INCLUDE[prod_short](includes/prod_short.md)].  
-   Conviértase en un empleado de almacén en el almacén BLANCO. Para ello, realice los pasos siguientes:  

1.  Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Empleados de almacén** y luego elija el enlace relacionado.  
2.  Elija el campo **Id. de usuario** y seleccione su propia cuenta de usuario en la página **Usuarios**.  
3.  En el campo **Cód. almacén**, especifique BLANCO.  
4.  Seleccione el campo de **Predeterminado**.  

> [!NOTE]
> [!INCLUDE [locations-cronus](includes/locations-cronus.md)]

Realice los pasos siguientes para preparar el almacén BLANCO para el procesamiento de ensamblado:  

1.  Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Ubicaciones** y luego elija el enlace relacionado.  
2.  Abra la ficha de almacén para el almacén BLANCO.  
3.  En la ficha desplegable **Ubicaciones**, escriba **W-10-0001** en el campo **Cód. ubic. para ensamblado**.  

    Al especificar este código de ubicación de tipo no picking, todas las líneas del pedido de ensamblado están listas para recibir sus componentes en la ubicación.  

4.  En el campo **Cód. ubic. desde ensamblado**, especifique **W-01-0001**.  

    Al especificar este código de ubicación de picking, los elementos del ensamblado terminados se enviarán a la ubicación.  

Realice los pasos siguientes para quitar el plazo de entrega predeterminada para los procesos internos:  

1.  Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Configuración de fabricación** y luego elija el enlace relacionado.  
2.  En la página **Configuración fabricación**, en la ficha desplegable **Planificación**, elimine el valor del campo **Plazo seguridad genérico**.  

<!-- Create inventory for assembly components by following [Prepare Sample Data](walkthrough-selling-assembling-and-shipping-kits.md#prepare-sample-data).   -->

## Historia

El 23 de enero, Susana, la responsable del procesamiento de pedidos de venta recibe un pedido de La Tienda Aparatos de tres unidades del kit B, que es un producto ATO. Las tres unidades se personalizan y deben incluir la tarjeta gráfica de gran potencia y un bloque de RAM adicional. Las unidades de disco se actualizan a DWD porque las unidades de CD no están disponibles. Susana sabe que las unidades se pueden ensamblar inmediatamente, por lo que deja la fecha de envío sugerida del 23 de enero.  

Al mismo tiempo, el cliente solicita quince unidades del kit A con una solicitud especial; que cinco unidades se personalicen para incluir la tarjeta gráfica de gran potencia. Aunque el equipo A suele ser un producto de tipo ensamblar para stock, la responsable del procesamiento de pedidos combina las cantidades de línea de venta para vender diez unidades desde las existencias y ensamblar cinco unidades personalizadas en el pedido. Las diez unidades del kit A no están disponibles y deben suministrarse primero al inventario mediante un pedido de ensamblado según la directiva de ensamblado del producto. Susana aprende del departamento de ensamblado qué las unidades del kit A no se pueden completar durante la semana actual. Fija la fecha de envío de la segunda línea de pedido de venta, para la cantidad combinada ATO y de inventario, en el 27 de enero y notifica al cliente que las 15 unidades del kit A se enviarán cuatro días después que las tres unidades de kit B. Para señalar al departamento de envío que este pedido de venta requiere el procesamiento de ensamblado, Susana crea el documento de envío de almacén a partir del pedido de venta.  

Eduardo, el planificador, ejecutar la hoja de trabajo de planificación y genera un pedido de ensamblado para las diez unidades estándar del kit A con una fecha de vencimiento interna del 27 de enero.  

Roberto, responsable de los envíos, obtiene tres líneas de envío de almacén para el pedido de venta: una línea para las tres unidades ATO puras, una línea para las cinco unidades ATO en la línea combinada de pedido de venta y una línea para las diez unidades ATS en la línea combinada de pedido de venta. Crea un documento de picking de almacén para todos los componentes del ensamblado que se necesitan para ensamblar el total de ocho unidades ATO en el documento de envío de almacén.  

Juan, el encargado de picking, recupera los componentes para todas las cantidades ATO en el documento de envío de almacén y los lleva al área de ensamblado. Especifica la cantidad para manipular y registra el picking de almacén.  

Elena ensambla las tres unidades ATO del kit B. Los componentes ya se han preparado y no graba las cantidades de salida y consumo, ni registra el pedido, porque ambas acciones se realizan automáticamente a través de las líneas de envío de almacén relacionadas.  

Roberto graba la cantidad ensamblada en la línea de envío de almacén y registra el envío de las tres unidades del kit B. La primera línea en el pedido de venta se actualiza como enviada. El pedido de ensamblado vinculado quedará abierto hasta que el pedido de venta se facture por completo. Las dos líneas de envío de almacén, una ATO y una ATS, para el kit A con fechas de vencimiento del 27 de enero permanecen abiertas.  

El 27 de enero, Linda procesa dos pedidos de ensamblado para el kit A. El primero es el pedido ATO de cinco unidades, que procesa de forma diferente al pedido ATO para el Kit B que procesó el 23 de enero. En este pedido, puede acceder a la línea de envío de almacén para registrar el trabajo de ensamblaje completado. Los componentes necesarios están preparados en el departamento de ensamblado, ya que se prepararon junto con los componentes del kit B.  

El segundo pedido de ensamblado es el pedido ATS de diez unidades creadas mediante el sistema de planificación. En este pedido ATS, Elena realiza todas las acciones relacionadas del pedido de ensamblado. Crea un documento de picking de almacén para los componentes del ensamblado que se necesitan para ensamblar las diez unidades. Cuando los equipos PC están ensamblados, Elena registra el pedido de ensamblado y, de este modo, señala que los productos están disponibles en el inventario y se puede realizar el picking para el envío.  

Roberto crea un documento de picking de almacén para las cantidades que quedan antes de que se pueda registrar el envío de almacén. Se crea un documento de picking para las diez unidades del kit A que se acaban de terminar. Los componentes que se necesitan para ensamblar las cinco unidades del kit A e pedido se prepararon el 23 de enero.  

Juan trae diez unidades del kit A del almacén al área de envío especificada, registra la cantidad que se debe manipular y luego registra el picking.  

Roberto empaqueta las diez unidades ATS con las cinco unidades ATO que Elena ensambló anteriormente. Rellena la cantidad para enviar en ambas líneas y luego registra el último envío para La Tienda Aparatos. El pedido de ensamblado relacionado de cinco unidades del kit A se registra automáticamente. La segunda línea del pedido de venta se actualiza como enviada. Dos pedidos de ensamblado vinculados quedarán abiertos hasta que se facture y se cierre el pedido de venta.  

Cuando el pedido de venta se registra posteriormente como facturado en su totalidad, se quitan el pedido de venta y los pedidos de ensamblado vinculados.  

## Preparar datos de ejemplo

1.  Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Diarios producto almacén**, y luego elija el enlace relacionado.  
2.  Elija el campo **Nombre sección** y seleccione el diario predeterminado.  
3.  Cree los ajustes de inventario positivos en el almacén BLANCO en la fecha de trabajo, el 23 de enero. Para ello, especifique la información siguiente.  

    |**Nº producto**|**Cód. zona**|**Cód. ubicación**|**Cantidad**|  
    |-----------------------------------|---------------------------------------|--------------------------------------|------------------------------------|  
    |80001|PICKING|W-01-0001|20|  
    |80005|PICKING|W-01-0001|20|  
    |80011|PICKING|W-01-0001|nº 20|  
    |80014|PICKING|W-01-0001|nº 20|  
    |80203|PICKING|W-01-0001|nº 20|  
    |80209|PICKING|W-01-0001|nº 20|  

4.  Elija la acción **Registrar** y, a continuación, seleccione el botón **Sí**.  

    A continuación, sincronice los nuevos movimientos de almacén con el inventario.  

5.  Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Diarios de productos**, y luego elija el enlace relacionado. Se abre la página **Diario productos**.  
6.  Seleccione la acción **Calcular ajuste almacén**.  
7.  En la página **Calcular ajuste almacén**, seleccione el botón **Aceptar**.  
8.  En la página **Diario de producto**, elija la acción **Registrar** y el botón **Sí**.  

### Crear elementos del ensamblado  

1.  Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Productos**, y luego elija el enlace relacionado.  
2.  Seleccione la acción **Nuevo**.  
3.  Cree el primer elemento del ensamblado según la información siguiente.  

    |Campo|Valor|  
    |---------------------------------|-----------|  
    |**Descripción**|Kit A: equipo PC básico|  
    |**Unidad de medida base**|UDS|  
    |**Código de categoría de artículo**|Varios|  
    |**Sistema reposición**|Ensamblado|  
    |**Directiva de ensamblado**|Ensamblar para stock|  
    |**Política reaprov.**|Lote a lote|  

    > [!NOTE]  
    >  El kit A suele suministrarse por ensamblado para stock y, por tanto, tiene una directiva de reaprovisionamiento para que forme parte de la planificación de suministros general.  

4.  Elija la acción **Ensamblado** y luego elija **L.M. de ensamblado**.  
5.  Defina una L.M. de ensamblado para el kit A con la siguiente información.  

    |**Escriba**|**Nº**|**Cantidad por**|  
    |-------------------------------|------------------------------|---------------------------------------|  
    |Artículo|80001|1|  
    |Artículo|80011|1|  
    |Artículo|80209|1|  
    |Recurso|Elena|1|  

6.  Cree el segundo elementos del ensamblado según la información siguiente.  

    |Campo|Valor|  
    |---------------------------------|-----------|  
    |**Descripción**|Kit B: equipo PC Pro|  
    |**Unidad de medida base**|UDS|  
    |**Código de categoría de artículo**|Varios|  
    |**Sistema reposición**|Ensamblado|  
    |**Directiva de ensamblado**|Ensamblar para pedido|  

    > [!NOTE]  
    >  El kit B suele suministrarse por ensamblado para pedido y, por tanto, no tiene directiva de reaprovisionamiento, ya que no debería formar parte de la planificación de suministros general.  

7.  Elija la acción **Ensamblado** y luego elija **L.M. de ensamblado**.  
8.  Defina una L.M. de ensamblado para el kit B con la siguiente información.  

    |**Escriba**|**Nº**|**Cantidad por**|  
    |-------------------------------|------------------------------|---------------------------------------|  
    |Artículo|80005|1|  
    |Artículo|80014|1|  
    |Artículo|80210|1|  
    |Recurso|Elena|1|  

### Vender elementos del ensamblado  

1.  Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Pedidos de venta** y, a continuación, elija el vínculo relacionado.  
2.  Seleccione la acción **Nuevo**.  
3.  Cree dos líneas de pedido de venta para el cliente 62000, La Tienda Aparatos, en la fecha de trabajo con la siguiente información.  

    |**Tipo**|**Descripción**|**Cantidad**|Cantidad a ensamblar para pedido|Fecha envío|  
    |--------------|---------------------|------------------|-------------------------------|-------------------|  
    |Producto|Kit B: equipo PC Pro|3|3|23 de enero|  
    |Producto|Kit A: equipo PC básico|15|5|27 de enero|  

    > [!NOTE]  
    >  Existe el siguiente problema de disponibilidad para la línea de pedido de venta del kit B:  
    >   
    >  -   El componente del ensamblado 80210 no está disponible. Esto significa que las tres unidades especificadas del kit B no se pueden ensamblar, indicado por el valor **0** en el campo **Capaz de ensamblar** de la página **Disponibilidad de ensamblado**.  
    >   
    >  Existe el siguiente problema de disponibilidad para la línea de pedido de venta del kit A:  
    >   
    >  -   Las diez unidades del kit A no están disponibles. Esto indica al sistema de planificación que la cantidad se debe ensamblar para inventario.  

    A continuación, personalice el pedido de venta.  

4.  Seleccione la línea de pedido de venta para tres unidades del kit B.  
5.  En la ficha desplegable **Líneas**, seleccione **Línea**, seleccione **Ensamblar para pedido** y, a continuación, elija **Ensamblar para líneas de pedido**.  
6.  En la página **Ensamblar para líneas de pedido**, en la línea del pedido de ensamblado para el producto 80014, introduzca **2** en el campo **Cantidad por**.  
7.  En la línea del pedido de ensamblado para el producto 80210, elija el campo **Nº** y seleccione el producto 80209 en su lugar.  
8.  Cree una nueva línea de pedido de ensamblado con la siguiente información.  

    |Tipo|N.º|Cantidad por|  
    |----------|---------|------------------|  
    |Artículo|80203|1|  

9. Cierre la página **Ensamblar para líneas de pedido**.  

    A continuación, actualice el precio de venta del kit B según la personalización que acaba de realizar. Observe el valor actual en el campo **Precio de venta IVA excl.**.  

10. En la ficha desplegable **Líneas**, seleccione **Línea**, seleccione **Ensamblar para pedido** y, a continuación, elija **Revertir precio**.  
11. Elija el botón **Sí**. Observe el valor aumentado en el campo **Precio de venta IVA excl.**.  
12. Seleccione la línea de pedido de venta para quince unidades del kit A.  
13. En la ficha desplegable **Líneas**, seleccione **Línea**, seleccione **Ensamblar para pedido** y, a continuación, elija **Ensamblar para líneas de pedido**.  
14. En la página **Ensamblar para líneas de pedido**, cree una nueva línea de pedido de ensamblado con la siguiente información.  

    |Escriba|Nº|Cantidad por|  
    |----------|---------|------------------|  
    |Producto|80203|1|  

     A continuación, cambie la fecha de envío de la segunda línea de pedido de venta según la programación del ensamblado.  

15. En la línea de pedido de venta de 15 unidades del kit A, especifique **27-01-2014** en el campo **Fecha envío**.  
16. Seleccione la acción **Liberar**.  
17. Seleccione la acción **Crear envío alm.**  
18. Cierre el pedido de venta.  

### Planificar para producto ATS no disponibles  

1.  Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Hoja planificación** y luego elija el enlace relacionado.  
2.  Seleccione la acción **Calcular planificación regenerativa**.  
3.  En la página **Calcular plan**, establezca los filtros siguientes.  

    |Fecha inicial|Fecha final|N.º|  
    |-------------------|-----------------|---------|  
    |23-01-2014|27-01-2014|Kit A: equipo PC básico|  

4.  Elija el botón **Aceptar**.  

    Se crea una nueva línea de planificación para el pedido de ensamblaje necesario de diez unidades, con fecha 27 de enero. No necesita cambios, por lo que ahora puede crear el pedido.  

5.  Seleccione la acción **Ejecutar mensajes de acción**.  
6.  En la página **Ejecutar mensajes acción**, elija el campo **Pedido de ensamblado** y seleccione **Realizar pedidos de ensamblado**.  
7.  Elija el botón **Aceptar**.  

### Ensamblar y enviar la primera cantidad ATO  

1.  Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Envío almacén** y luego elija el enlace relacionado.  

    > [!NOTE]  
    >  En esta sección, la persona responsable de enviar se encarga de registrar el trabajo de ensamblado ATO completado en la línea de envío de almacén. Este flujo de trabajo puede realizarse en entornos donde el trabajo de ensamblado lo realiza la persona responsable de enviar o los trabajadores de ensamblado en el área de envío.  
    >   
    >  En esta sección, las acciones del pedido de ensamblado se realizan indirectamente desde la línea de envío de almacén. Para obtener más información sobre cómo procesar un pedido de ensamblado directamente, consulte la sección sobre cómo "ensamblar productos para stock" en este tutorial.  

2.  Abra el envío de almacén más reciente que se ha creado en el almacén BLANCO.  

    Observe las tres líneas de envío del almacén: Una línea para la cantidad de ATO del Kit B, con vencimiento el 23 de enero. Una línea para la cantidad de ATO del Kit A, con vencimiento el 27 de enero. Una línea para la cantidad de inventario del Kit A, con vencimiento el 27 de enero.  

    El campo **Ensamblar para pedido** especifica el método de ensamblado.

    A continuación, cree un documento de picking para todos los componentes del ensamblado ATO que se necesitan en el envío de almacén.  

3.  Elija la acción **Crear picking** y, a continuación, seleccione el botón **Aceptar**.  

    A continuación, realice la tarea del encargado de picking.  

4.  Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Picking** y luego elija el enlace relacionado.  
5.  Abra el documento de picking de almacén que se creó en el paso 3 de esta sección.  

    Observe el valor del campo **Documento origen** y que todas las líneas de picking sean para los componentes del ensamblado.  

    A continuación, registre el picking sin cambiar la información predeterminada.  

6.  Seleccione la acción **Autorrellenar el campo Cdad. para manipular**.  
7.  Elija la acción **Registrar picking**.  

    Vuelva al área para realizar las tareas de envío.  

8.  Vuelva a abrir la página **Envío almacén**.  

    Observe que el campo **Cdad. preparada pedido** aún está vacío en todas las líneas. Esto se debe a que aún no ha realizado el picking de los productos que se deben enviar, sino solo los componentes necesarios para ensamblar las cantidades ATO.  

    Empiece a revisar el pedido de ensamblado relacionado.  

9. Seleccione la línea de envío para tres unidades del kit B.  
10. En la ficha desplegable **Líneas**, seleccione **Línea** y elija **Ensamblar para pedido**. Se abrirá la página **Pedido de ensamblado**.  

    Observe que varios campos del pedido de ensamblado no están disponibles porque el pedido está vinculado a un pedido de venta.  

    Observe en las líneas de pedido de ensamblado que el campo **Cdad. preparada pedido** se ha rellenado. Esto se debe al picking registrado en el paso 7 de esta sección.  

11. En el campo **Cantidad a ensamblar**, intente especificar cualquier valor menor que **3**.  

    Lea el mensaje de error que explica la razón por la cual este campo solo se puede rellenar a través del campo **Cdad. a enviar** en el envío relacionado.  

    El campo **Cantidad a ensamblar** se puede editar para las situaciones en las que desea enviar parcialmente una cantidad de inventario en lugar de ensamblar más unidades en el pedido. Para obtener más información, consulte la sección "Escenarios de combinación" en [Conocer Ensamblar para pedido y Ensamblar para stock](assembly-assemble-to-order-or-assemble-to-stock.md).  

12. Cierre la página **Pedido de ensamblado** para volver a la página **Envío almacén**.  
13. En la línea de envío para tres unidades del kit B, en el campo **Ctdad. a enviar**, especifique **3**.  
14. Seleccione la acción **Registrar envío** y, a continuación, el botón **Enviar**.  

    Junto con este registro de envío de almacén, se registran el consumo y las cantidades de salida completos del pedido de ensamblado relacionado y el campo **Cantidad pendiente** está vacío. La línea de pedido de venta del kit B se actualiza para indicar que las tres unidades se han enviado.  

    Las actividades de almacén para cubrir la primera línea de pedido de venta antes del 23 de enero se han completado. A continuación, cumpla las líneas de pedido de venta que han de enviarse el 27 de enero.  

### Ensamblar y registrar la segunda cantidad ATO  

1.  Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Pedidos ensamblado** y luego elija el enlace relacionado.  

    Observe que el pedido ATO para las unidades enviadas del kit B aún se incluye en la lista, aunque el campo **Cantidad pendiente** está vacío. Esto se debe a que el pedido de venta vinculado todavía no se ha facturado por completo.  

    > [!NOTE]  
    >  En esta sección, en trabajador de ensamblado se encarga de registrar el trabajo de ensamblado ATO completado en la línea de envío de almacén. Este flujo de trabajo puede realizarse en entornos donde el trabajo de ensamblado se realiza en un departamento de ensamblado independiente y los trabajadores de ensamblado tienen autorización para cambiar la línea de envío de almacén.  

2.  Abra el pedido de ensamblado ATO para cinco unidades del kit A.  

    Observe que los campos **Cantidad a ensamblar** y **Cantidad a consumir** están vacíos porque no se ha registrado ningún trabajo aún.  

    Observe en las líneas de pedido de ensamblado que el campo **Cdad. preparada pedido** se ha rellenado. Esto se debe al picking que se registró el 23 de enero.  

    A continuación, registre que el pedido de ensamblado se ha completado.  

3.  Elija la acción **Lín. envío almacén ensamblar para pedido**.  
4.  En la página **Lín. envío almacén ensamblar para pedido**, en el campo **Cdad. a enviar**, especifique **5** y, a continuación cierre la página.  

    Observe en la página **Pedido de ensamblado** que los campos **Cantidad a ensamblar** y **Cantidad a consumir** ahora se rellenaron con las cantidades de salida y consumo que se registrarán con el envío.  

5.  Cierre la página **Pedido de ensamblado**.  

### Ensamblar la cantidad ATS  

1.  Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Pedidos ensamblado** y luego elija el enlace relacionado.  
2.  Abra el pedido de ensamblado ATO para diez unidades del kit A.  

    Observe que el campo **Cantidad a ensamblar** se ha rellenado con la cantidad esperada.  

    A continuación, cree un documento de picking para recuperar los componentes necesarios.  

3.  Seleccione la acción **Liberar**.  
4.  Elija la acción **Crear picking alm.** y seleccione el botón **Aceptar**.  

    A continuación, realice la tarea del encargado de picking.  

5.  Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Picking** y luego elija el enlace relacionado.  
6.  Abra el documento de picking de almacén que se creó en el paso 4 de esta sección.  

     Registre el picking sin cambiar la información predeterminada.  

7.  Seleccione la acción **Autorrellenar el campo Cdad. para manipular**.  
8.  Elija la acción **Registrar picking**.  

    Vuelva al pedido de ensamblado para realizar la última tarea de ensamblado.  

9. En **Pedido de ensamblado**, elija la acción **Registrar** y, a continuación, el botón **Sí**.  

    Observe que el pedido de ensamblado se quitó de la lista de pedidos abiertos.  

### Enviar productos restantes, parcialmente de las existencias y parcialmente ensamblado para pedido  

1.  Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Envío almacén** y luego elija el enlace relacionado.  
2.  Abra el envío de almacén más reciente que se ha creado en el almacén BLANCO.  

    Observe en la línea de diez unidades del kit A que los campos **Ctdad a enviar** y **Cdad. preparada pedido** están vacíos.  

    A continuación, realice el picking de los productos restantes.  

3.  Elija la acción **Crear picking** y, a continuación, seleccione el botón **Aceptar**.  

    A continuación, realice la tarea final del encargado de picking para este envío de almacén.  

4.  Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Picking** y luego elija el enlace relacionado.  
5.  Abra el documento de picking de almacén que se creó en el paso 3 de esta sección.  

    Observe que este documento de picking es para el elemento del ensamblado y no para los componentes del ensamblado.  

    A continuación, registre el picking sin cambiar la información predeterminada.  

6.  Seleccione la acción **Autorrellenar el campo Cdad. para manipular**.  
7.  Elija la acción **Registrar picking** y, a continuación, seleccione el botón **Sí**.  

    Vuelva al envío de almacén para realizar la última tarea.  

8.  Vuelva a abrir la página **Envío almacén**.  

    En la página **Envío almacén**, en la línea de diez unidades del kit A, observe que los campos **Ctdad. a enviar** y **Cdad. preparada pedido** ahora contienen el valor **10**.  

9. Seleccione la acción **Registrar envío** y, a continuación, elija **Enviar**.  

    Se elimina el documento de envío de almacén, que indica que se completaron las actividades de almacén correspondientes. A continuación, compruebe que se ha procesado el pedido de venta.  

10. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Pedidos de venta** y, a continuación, elija el vínculo relacionado  
11. Abra el pedido de venta para La Tienda Aparatos.  

    Observe que el campo **Cantidad enviada** contiene la cantidad completa en ambas líneas.  

    Cuando la Tienda Aparatos pague la recepción de los 18 equipos PC de CRONUS, se quitarán el pedido de venta y sus pedidos de ensamblado vinculados.  

## Consultar la [formación de Microsoft](/training/paths/assemble-items-dynamics-365-business-central/) relacionada

## Consulte también .

 [Descripción de ensamblar para pedido y ensamblar para stock](assembly-assemble-to-order-or-assemble-to-stock.md)   
 [Ensamblar artículos](assembly-how-to-assemble-items.md)   
 [Realizar un picking de los artículos para el envío de almacén](warehouse-how-to-pick-items-for-warehouse-shipment.md)   
 [Venta de artículos ensamblados para pedido](assembly-how-to-sell-items-assembled-to-order.md)   
 [Ensamblar artículos](assembly-how-to-assemble-items.md)   
 [Detalles de diseño: Registro de pedidos de ensamblado](design-details-assembly-order-posting.md)   
 [Detalles de diseño: Flujos de almacén internos](design-details-internal-warehouse-flows.md)   
 [Detalles de diseño: Flujo de salida del almacén](design-details-outbound-warehouse-flow.md)   
<!--  [Walkthrough: Planning Supplies Automatically](walkthrough-planning-supplies-automatically.md) -->


[!INCLUDE[footer-include](includes/footer-banner.md)]
