---
title: 'Tutorial: planificación manual de suministros'
description: 'Este tutorial demuestra el proceso de planificación de pedidos de suministro para satisfacer la nueva demanda, incluida la planificación de una compra, transferencia y orden de producción.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 06/24/2021
ms.author: bholtorf
---
# Tutorial: planificación manual de suministros

<!-- [!INCLUDE[complete_sample_data](includes/complete_sample_data.md)]   -->

En este tutorial, se demuestra el proceso de planificar pedidos de suministro para cubrir la nueva demanda. Puede iniciar la planificación de suministros a intervalos fijos, por ejemplo, todas las mañanas o todos los lunes, o bien cuando le notifiquen desde ventas o producción, en función del tipo de demanda. En este tutorial, utilizará la página **Planificación de pedidos**, una sencilla herramienta de planificación de suministros basada en la toma manual de decisiones en lugar de en una planificación automática basada en parámetros.  

## Acerca de este tutorial  
 En este tutorial se ilustran las siguientes tareas:  

-   Planificación de un pedido de compra para la fabricación de componentes.  
-   Planificación de un pedido de transferencia para cubrir la demanda de venta.  
-   Planificación de una orden de producción para un producto multinivel.  

## Funciones  
 En este tutorial se demuestran las tareas realizadas por las siguientes funciones de usuarios:  

-   Planificador de producción  
-   Agente de compras  
-   Procesadora de pedidos de ventas  

## Requisitos previos  
 Antes de comenzar este tutorial, debe instalar el [!INCLUDE[prod_short](includes/prod_short.md)]. Se deben realizar las modificaciones siguientes a la base de datos:  

-   Elimine todos los pedidos de ventas existentes para bicicletas.  
-   Cree un pedido de ventas para 10 bicicletas en el almacén EAST.  
-   Elimine todas las órdenes de producción planificadas y planificadas en firme. No elimine las órdenes iniciadas con movimientos que ya se hayan registrado.  

 Como regla, utilice los datos sugeridos en este tutorial pues contiene los registros necesarios.  

## Historia  
 Eduardo, el Planificador de producción de una pequeña empresa de fabricación, va a planificar las órdenes de producción y los pedidos de compra para cubrir una nueva demanda de venta.  

 Teniendo en cuenta que los productos tienen pocos niveles de L.M. y que el flujo de pedidos es relativamente bajo, Eduardo utiliza la página **Planificación de pedidos** para crear pedidos de suministros de forma manual—los niveles de producto de uno en uno.  

 En entornos de fabricación más complejos, se utiliza la hoja de planificación para planificar el suministro basándose en parámetros de productos como ciclo de reprogramación, plazo de seguridad, punto pedido y cálculos por lotes de la demanda consolidada de todos los niveles de productos.  

## Configuración de los datos de ejemplo  
 La empresa de demostración CRONUS estándar tiene en la actualidad gran cantidad de demanda no planificada. Durante las diferentes tareas de planificación de este tutorial, para desviarse del flujo empresarial real, deberá hacer caso omiso de la demanda con fechas de vencimientos próximas y usar en su lugar la demanda con fechas posteriores.  

## Usar la página Planificación de pedidos  

A la página **Planificación de pedidos** se puede acceder desde varias ubicaciones diferentes:  

-   Fabricación, Planificación  
-   Ventas y Marketing, Procesamiento de pedidos  
-   Compra, Planificación  
-   Además, puede abrir esta página para un pedido de producción específico eligiendo la acción **Planificación**.

### Para utilizar la página Planificación de pedidos  

1.  Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Planificación de pedidos** y luego elija el enlace relacionado.  

     Cuando se abre la página **Planificación de pedidos** por primera vez, debe calcularse un plan para mostrar la nueva demanda desde la última vez que se calculó.  

2.  Seleccione la acción **Calcular planificación**.  

     El sistema de planificación analizará la nueva demanda que se haya introducido, como nueva venta, venta modificada u órdenes de producción.  

     En función de la disponibilidad total, se calculará la cantidad necesaria para cada línea de demanda. Este cálculo se realiza pedido por pedido. Esto significa que primero se calculará el pedido que incluya la línea de demanda que presente la primera fecha de vencimiento o de entrega. A continuación, se calcularán las demás líneas de demanda en el mismo orden, independientemente de la fecha de vencimiento o de envío.  

3.  Asegúrese de que la página **Planificación de pedidos** está maximizada y de que se ha reajustado el tamaño de los campos de columnas para que muestren todos los nombres de campos predeterminados.  

     Cuando finalice el cálculo, la página mostrará toda la demanda no cubierta como líneas de cabecera de pedido colapsadas ordenadas según la primera fecha de demanda.  

     Tenga en cuenta que CRONUS tiene varios pedidos con demanda no cubierta. Cada línea de planificación en negrita representa un pedido, un pedido de venta o una orden de producción, incluyendo por lo menos una línea de pedido con disponibilidad insuficiente.  

4.  En el campo **Mostrar demanda como**, seleccione el filtro **Toda la demanda**.  

     Con el campo **Tipo de demanda**, puede elegir los tipos de pedidos que desea mostrar.  

     No se mostrarán los pedidos que no tengan problemas de disponibilidad. Si no hay pedidos cuando se calcula un plan, se mostrará un mensaje y no aparecerá ninguna línea de planificación.  

## Planificación de un pedido de compra para cubrir la demanda de componente  
 En este procedimiento, creará un pedido de compra para los componentes de fabricación necesarios.  

### Para planificar un pedido de compra que cubra la necesidad de componentes en producción  

1.  Expanda la primera línea (elija el símbolo +).  
2.  Seleccione la primera línea de demanda, con el producto **LSU-15**, y después seleccione la acción **Mostrar documento**.  
3.  Cierre la orden de producción abierta para volver a la página **Planificación de pedidos**.  
4.  En el campo **Sistema reposición**, seleccione **Compra**.  

     El valor predeterminado proviene de la ficha producto o de la ficha UA, pero puede cambiarlo a una de las siguientes opciones:  

    -   **Compra**: para crear un pedido de compra.  
    -   **Transferencia**: para crear un pedido de transferencia.  
    -   **Ord. prod.**: para crear un pedido de producción.  

5.  En el campo **Suministrado desde**, seleccione una de las siguientes opciones según el sistema de reposición seleccionado:  

    -   **Proveedor**: Para compras  
    -   **Ubicación** – Para transferencias  

     Si el campo no está relleno, aparecerá un mensaje de error cuando trate de crear los pedidos de suministro.  

    > [!NOTE]  
    >  Si los componentes tienen configurado un número de proveedor predeterminado en las fichas producto, las líneas estarán predefinidas.  

6.  Elija el campo de **Suministrado desde**.  
7.  En la página **Catálogo de productos de proveedor**, elija la acción **Nuevo** y, a continuación, seleccione el proveedor **30000**.  
8.  Elija el botón **Aceptar** para volver a la página **Programación de pedidos**.  
9. Copie el proveedor número **30000** en las otras líneas de componentes de altavoz en esta orden de producción.  

     Ahora puede crear un pedido de compra.  

10. Seleccione la acción **Crear pedidos**. Se abrirá la página **Crear pedidos suministros**.  
11. En la ficha desplegable **Planificación de pedidos**, en el campo **Crear pedidos para**, elija la opción **Pedido activo**.  
12. En la ficha desplegable **Opciones**, en el campo **Crear pedido compra**, elija la opción **Crear ped. compra**.  
13. Elija el botón **Aceptar** para crear pedidos de compra para todos los componentes del pedido.  

     Los pedidos de compra se crean ahora y se guardan como los últimos pedidos de la lista de pedidos de compra.  

## Planificación de un pedido de transferencia para cubrir la demanda de venta  
 En este procedimiento, va a planificar la demanda para un pedido de venta. Las líneas de demanda representan líneas de venta y no líneas de componente, como en la demanda de producción.  

### Para planificar un pedido de transferencia para cubrir la demanda de venta  

1.  Mueva el puntero a la línea de planificación del pedido **2008**.  
2.  Expanda la línea y mueva el puntero a la línea de demanda.  

     El pedido de venta **2008** corresponde a diez altavoces, producto **LS-120**, pedido por Seguros Bella Vista S.A.  

     Aparecerá el sistema de reposición definido del producto y el proveedor predefinido.  

    > [!NOTE]  
    >  En la parte inferior de la página, existen cuatro campos de información. En el campo **Primera fecha posible**, las diez piezas que se necesitan estarán disponibles, en un pedido de suministro de entrada, nueve días más tarde de la fecha de vencimiento actual. Si es demasiado tarde para el cliente, el campo **Disponible para transfer.** muestra 13 piezas del producto en otro almacén. Desea planificar para este stock.  

3.  Elija el campo **Disponible para transfer.** para abrir la página **Obtener suministro alternativo**.  
4.  Elija el botón **Aceptar** para reservar los diez productos que están disponibles.  

    > [!NOTE]  
    >  En la línea de demanda, la compra sugerida se ha cambiado por una transferencia del almacén MAIN. La función **Crear pedidos compra** crea un pedido de transferencia de MAIN al almacén solicitado. El campo **Existen sustitutivos** funciona de la misma manera.  

5.  Seleccione la acción **Crear pedidos**. Se abrirá la página **Crear pedidos suministros**.  
6.  En la ficha desplegable **Planificación de pedidos**, en el campo **Crear pedidos para**, elija la opción **Pedido activo**.  
7.  En la ficha desplegable **Opciones**, en el campo **Crear orden de transferencia**, seleccione la opción **Crear pedid. trans.**.  
8.  Elija el botón **Aceptar** para crear el pedido de transferencia para suministrar el pedido de compra.  

     Ya se ha creado y guardado el pedido de transferencia en la lista como el último pedido en la lista de pedidos de transferencia abiertos.  

## Planificación de una orden de producción multinivel para cubrir la demanda de venta  
 En este procedimiento, planificará para cubrir la demanda de venta de un producto elaborado con varios niveles, cada uno crea una demanda de producción dependiente.  

### Para planificar una producción multinivel para cubrir la demanda de venta  

1.  Seleccione la línea de planificación con la demanda de venta para el pedido **1001**, creado anteriormente como dato de requisitos previos.  

     Esta demanda es una línea de venta, pero el producto tiene definido un sistema de reposición de **Ord. prod.** Continúe para añadir un timbre adicional a los componentes requeridos de cada bicicleta.  

2.  Seleccione la acción **Componentes** para abrir la página **Componentes de planificación**.  
3.  En la línea con el producto Timbre, cambie el campo **Cantidad por** de **1** a **2**.  
4.  En la página **Planificación de pedidos**, considere las alternativas de planificación que tiene. En este caso, no tiene métodos de suministro alternativos, ni transferencia, ni sustitutivo ni entrega posterior. Debe crear el pedido de suministro sugerido: una orden de producción.  
5.  Elija el botón de **Crear pedidos** para crear la orden de producción.  

     En la página **Planificación de pedidos**, observe que la línea de planificación para el pedido de venta **1001** ya no existe y que se ha cubierto la demanda de venta inicial.  

6.  Cierre la página **Planificación de pedidos**.  

     Ahora podría quedarse en esta vista y completar todas las tareas de planificación. Sin embargo, va a asumir la función Planificador de producción accediendo a la orden de producción que acaba de crear y va a acceder a la página **Planificación de pedidos**.  

 Como planificador de producción ahora debe planificar una orden de producción específica.  

### Para planificar una orden de producción específica  

1.  Abra la orden de producción **101001** para diez bicicletas, que acaba de crear con la función **Crear pedidos compra**.  
2.  Abra la página **Componentes orden producción** para comprobar que el timbre adicional está reflejado en la orden de producción.  
3.  Seleccione la acción **Planificación**.  

     La página **Planificación de pedidos** se abre en una vista que siempre se filtra en la demanda de producción específica. La demanda de venta no se muestra. Debe calcular un plan para poder ver la demanda adicional.  

4.  Seleccione la acción **Calcular planificación**.  

     Observe que aparecen cuatro nuevas órdenes de producción como demanda de producción no planificada derivada del pedido **101001**. Las nuevas líneas representan la nueva demanda de producción desde los productos semiterminados que debe crearse para producir el pedido.  

5.  Seleccione la acción **Expandir todo** para obtener un panorama de toda la demanda de producción para las órdenes de producción.  

     Para proporcionar información adicional acerca de las líneas de demanda, puede que desee añadir los campos de **Cdad. demanda** y de **Cdad de demanda. disponible** a su vista.  

     Ahora debe suministrar diez unidades de cada componente.  

     Tenga en cuenta que cuatro de las líneas de demanda tienen el sistema de reposición Orden prod. Estos cuatro productos semiterminados representan el segundo nivel de producto de la bicicleta.  

     La configuración de reposición predeterminada ya está rellena y puede continuar creando pedidos.  

6.  Seleccione la acción **Crear pedidos**.  

     Antes de seleccionar el botón **Aceptar**, observe el texto en la ficha desplegable **Programación de pedidos**. Este texto es importante porque sabe que la bicicleta tiene varios componentes producidos, semiterminados, en su estructura de producto que pueden suponer una demanda cuando cree esta orden de producción.  

7.  En la página **Crear pedidos suministros**, en el campo de **Crear pedidos para**, seleccione la opción **Todas las líneas** y, a continuación, seleccione el botón de **Aceptar** para crear los órdenes de producción para el segundo nivel del producto del pedido.  

     Tenga en cuenta que ya no existe demanda de producción de nivel superior para la orden de producción 101001. Esto significa que se ha planificado la demanda de producción inicial para productos semiterminados.  

     En la página **Planificación de pedidos**, calcule un plan de nuevo para planificar la estructura de la bicicleta.  

8.  Elija la acción **Calcular plan** para recalcular el plan según indica el texto de Ayuda incrustado.  

     Las dos nuevas líneas representan una demanda de producción adicional derivada de los productos semiterminados planificados en los pasos anteriores. Se sugiere que realice dos órdenes de producción para suministrar los bujes de la rueda: una para 10 bujes delanteros y otra para 10 bujes traseros.  

9. Seleccione la acción **Expandir todo** para obtener un panorama de toda la demanda para las dos órdenes de producción.  

     El plan de suministro sugerido indica que se creará un total de cuatro pedidos de compra para los componentes. Decide crear los pedidos propuestos.  

10. Seleccione la acción **Crear pedidos**.  
11. En el campo de **Crear pedidos para**, seleccione la opción de **Todas las líneas** y, a continuación, seleccione el botón de **Aceptar**. Compruebe si existe demanda adicional para la fabricación del producto principal, la bicicleta, que se vende en el pedido de venta 1001.  
12. Seleccione la acción **Calcular planificación**.  

     El mensaje indica que ya se han suministrado todos los productos requeridos. Compruebe los órdenes de producción planificada en firme que se crean.  

13. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **O.P. Planificadas en firme** y, a continuación, elija el vínculo relacionado.  

     En la página **O.P. planif. en firme** revise como están programadas las horas de inicio y finalización de cada pedido según la estructura del producto. Primero se producen los componentes de nivel inferior. Por lo tanto, debe planificar pedidos de varios niveles como se demuestra en este flujo de trabajo de planificación.  

## Consulte también  
 [Tutoriales de procesos empresariales](walkthrough-business-process-walkthroughs.md)   
<!--  [Walkthrough: Planning Supplies Automatically](walkthrough-planning-supplies-automatically.md) -->


[!INCLUDE[footer-include](includes/footer-banner.md)]