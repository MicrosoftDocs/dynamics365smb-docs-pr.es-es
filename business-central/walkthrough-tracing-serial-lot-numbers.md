---
title: 'Tutorial: seguimiento de números de serie/lote'
description: Este tema describe las acciones necesarias para evitar la venta de un producto defectuoso y también cómo rastrear y recuperar productos cuando sea necesario.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/24/2021
ms.author: bholtorf
ms.openlocfilehash: b7e2ae55e231cdadf02a0a8e91f6d3ad066a0cb5
ms.sourcegitcommit: 00a8acc82cdc90e0d0db9d1a4f98a908944fd50a
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 06/29/2022
ms.locfileid: "9075229"
---
# <a name="walkthrough-tracing-seriallot-numbers"></a>Tutorial: seguimiento de números de serie/lote

<!-- [!INCLUDE[complete_sample_data](includes/complete_sample_data.md)]   -->

Cuando tienen lugar defectos en los productos, los errores deben identificarse y deberá impedirse que los productos afectados salgan de la empresa. Si ya se han enviado productos defectuosos, debe realizar un seguimiento de la persona que los ha recibido y, en caso necesario, retirarlos.  

La primera tarea en la gestión de defectos es investigar de dónde procedían los productos defectuosos y dónde se han usado. Esta investigación se basa en datos históricos y se facilita mediante la búsqueda en las entradas de seguimiento de productos utilizando la página **Seguimiento productos**.  

La segunda tarea en la gestión de defectos es determinar si los productos supervisados están planificados en documentos pendientes, como pedidos de venta no registrados o en diarios de consumo. Este trabajo se realiza en la página **Buscar movimientos**. Puede utilizar la función Buscar movimientos para buscar todos los tipos de registros de base de datos.  

## <a name="about-this-walkthrough"></a>Acerca de este tutorial

En este tutorial se muestra el modo de identificar qué productos son defectuosos, qué proveedor los ha suministrado y si se han usado, para que los pedidos correspondientes se puedan detener o retirar.  

En este tutorial se ilustran las siguientes tareas:  

- Seguimiento desde el uso hasta el origen.  
- Seguimiento desde el origen hasta el uso.  
- Búsqueda de todos los registros actuales que contienen el número de serie/lote del que se ha realizado un seguimiento.  

## <a name="roles"></a>Funciones

En este tutorial, se demuestran las tareas realizadas por los siguientes roles de usuario:  

- Controlador de calidad  
- Responsable de almacén  
- Procesador de pedidos  
- Agente de compras  

## <a name="prerequisites"></a>Requisitos previos

Para completar este tutorial, necesitará:  

- La empresa de [!INCLUDE[prod_short](includes/prod_short.md)].  
<!-- - To create new items and several business transactions by following the [Prepare Sample Data](walkthrough-tracing-serial-lot-numbers.md#prepare-sample-data).   -->

## <a name="story"></a>Historia

Ricardo, el controlador de calidad, está trabajando en una devolución de venta del producto 1002, Bicicleta de carreras. El cliente, Sellafrio S.L., se ha quejado de que el cuadro tiene costuras de soldadura agrietadas. Los técnicos de control de calidad han confirmado que el cuadro de la bicicleta devuelta está defectuoso. El controlador de calidad debe determinar ahora:  

- Qué lote de cuadros de bicicletas estaba defectuoso.  
- En qué pedido de compra se recibió el lote defectuoso.  

A partir del departamento de ventas, el controlador de calidad averigua que la bicicleta de carreras devuelta, producto 1002, tenía el número de serie NS1. Con esta información básica, debe determinar dónde se utilizó por última vez la bicicleta de carrera terminada y, posteriormente, realizar un seguimiento hasta llegar al origen para establecer de qué número de lote procedía el componente defectuoso (el cuadro de la bicicleta).  

Los resultados de esta primera tarea de seguimiento del productos identifican los cuadros de bicicletas que estaban defectuosos y el proveedor que los suministró. Después, pero dentro del mismo proceso de seguimiento global, el controlador de calidad debe encontrar todas las bicicletas de carreras vendidas que contengan cuadros de bicicletas del lote defectuoso, para poder detener o retirar dichos pedidos. Por último, el controlador de calidad debe encontrar los documentos pendientes en los que se usa el lote defectuoso, para no realizar más transacciones.  

Las dos primeras tareas de gestión de defectos se realizan en la página **Seguimiento productos**. La última tarea se realiza en la página **Buscar movimientos**, en integración con la página **Seguimiento de productos**.  

## <a name="prepare-sample-data"></a>Preparar datos de ejemplo

Debe crear los siguientes productos nuevos:  

- 2000, Cuadro de bicicleta: seguimiento específico de lote, componente de 1002  
- 1002, Bicicleta de carreras: seguimiento específico de número de serie  

A continuación, deberá crear diversas transacciones de compra, producción y venta con los dos productos.  

### <a name="to-create-the-items"></a>Para crear los productos  

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Productos**, y luego elija el enlace relacionado.  
2. Seleccione la acción **Nuevo**.  
3. En el campo **N.º**, escriba **2000** y rellene los siguientes campos.  

    |Descripción|Unidad medida base|Gen. Grupo registro prod.|Grupo registro IVA prod.|Grupo contable existencias|Cód. seguim. prod.|  
    |-----------|--------------------|------------------------|-----------------------|--------------------|------------------|  
    |Cuadro de bicicleta|UDS|MAT. PRIMA|IVA25|MAT. PRIMA|SEGLOTE|  

    > [!NOTE]  
    >  Para especificar la unidad de medida base, haga clic en el botón **Nuevo** y seleccione **UDS** en la página **Unidades medida producto**.  

4. Todos los demás campos tienen datos predeterminados aceptables o no es necesario rellenarlos.  
5. Elija el botón **Aceptar** para crear la primera ficha de producto nueva, 2000.  
6. Elija **Nuevo**.  
7. En el campo **N.º**, escriba **1002** y rellene los siguientes campos.  

    |Descripción|Unidad medida base|Gen. Grupo registro prod.|Grupo registro IVA prod.|Grupo contable existencias|Sistema reposición|Cód. seguim. prod.|  
    |-----------------|--------------------------|------------------------------|-----------------------------|-----------------------------|--------------------------|------------------------|  
    |Bicicleta de carreras|UDS|MERCADERÍA|IVA25|TERMINADA|Or. prod.|SEGNS|  

    > [!NOTE]  
    >  Para especificar la unidad de medida base, haga clic en el botón **Nuevo** y seleccione **UDS** en la página **Unidades medida producto**.  

    A continuación, defina la configuración de fabricación del producto.

8. En la ficha **Reposición**, escriba **1000** en el campo **Nº ruta**.  
9. Elija el campo **L.M. producción Nº** y, a continuación, elija **Avanzado**.  
10. En la página **Lista L.M. producción**, elija la primera línea, **1000**, y seleccione la acción **Editar**.  
11. En la página **L.M. producción**, cambie el valor del campo **Estado** a **En desarrollo**.  
12. Vaya a una línea vacía, escriba **2000** en el campo **Nº** y, a continuación, introduzca **1** en el campo **Cantidad por**.  
13. Cambie el valor en el campo **Estado** de nuevo a **Certificada**.  
14. Haga clic en el botón **Aceptar** para insertar la L.M. de producción en la ficha de producto y cerrar la página **L. MAT de producción**.  

    A continuación, debe comprar cuadros de bicicletas de Custom Metals Incorporated.  

### <a name="to-purchase-components"></a>Para comprar componentes

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Pedidos de compra** y, a continuación, elija el vínculo relacionado.  
2. Seleccione la acción **Nuevo**.  
3. Cree un pedido de compra para el proveedor, Custom Metals Incorporated, rellenando los campos de línea siguientes.  

    |Artículo|Cantidad|Nº lote|  
    |----|--------|-------|  
    |2000|10|LOT1|  

4. Para introducir el número de lote, elija la acción **Líns. seguim. prod.**  
5. En la página **Líns. seguim. prod.**, rellene los campos **Nº lote** y **Cantidad (base)**, y cierre la página.  
6. Rellene el campo **Nº factura proveedor** según corresponda.  
7. Seleccione la acción **Registrar**, elija la opción **Recibir y facturar** y seleccione el botón **Aceptar**.  

    A continuación, compre cuadros de bicicletas de Coolwood Technologies.  
8. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Pedidos de compra** y, a continuación, elija el vínculo relacionado.  
9. Seleccione la acción **Nuevo**.
10. Cree un pedido de compra para el proveedor, Coolwood Technologies, rellenando los siguientes campos de línea.  

    |Producto|Cantidad|Nº lote|  
    |----------|--------------|-------------|  
    |2000|11|LOT2|  

11. Para especificar el número de lote, en la ficha desplegable **Líneas**, en el grupo **Línea**, elija la acción **Líns. seguim. prod.**  
12. En la página **Líns. seguim. prod.**, rellene los campos **Nº lote** y **Cantidad (base)**, y cierre la página.  
13. Rellene el campo **Nº factura proveedor** según corresponda.  
14. Seleccione la acción **Registrar**, elija la opción **Recibir y facturar** y seleccione el botón **Aceptar**.  

    A continuación, fabrique dos bicicletas de carreras, NS1 y NS2.  

### <a name="to-produce-end-items"></a>Para producir los productos finales

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **O.P. lanzadas** y, a continuación, elija el vínculo relacionado.  
2. Seleccione el grupo **Nuevo**.  
3. Cree una nueva orden de producción lanzada rellenando los campos siguientes.  

    |Cód. procedencia mov.|Cantidad|Nº serie|  
    |----------|--------|----------|  
    |1002|2|NS1|  
    |1002|2|NS2|  

4. Seleccione la acción **Actualizar orden producción** y, a continuación, seleccione el botón **Aceptar** para rellenar la línea.  
5. Para introducir los números de serie, elija la acción **Líns. seguim. prod.**  
6. En la página **Líns. seguim. prod.**, rellene los campos **N.º serie** y **Cantidad (base)**, y cierre la página.  

    A continuación, registre el consumo de cuadros de bicicleta de LOT1.  
7. En la página **Orden producción lanzada**, seleccione la acción **Diario de producción**.  
8. En la página **Diario de producción**, seleccione la línea de consumo para el producto 2000, elija la acción **Líns. seguim. prod.**
9. En la página **Líns. seguim. prod.**, haga clic en la flecha desplegable del campo **Nº lote**, seleccione **LOT1** y, a continuación, haga clic en **Aceptar**.  
10. Deje los demás valores predeterminados de la página **Diario de producción** y elija la acción **Registrar**.  

    A continuación, fabrique dos bicicletas de carreras, NS1 y NS2.  

11. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **O.P. lanzadas** y, a continuación, elija el vínculo relacionado.  
12. Seleccione la acción **Nuevo**.  
13. Cree una nueva orden de producción lanzada rellenando los campos siguientes en la cabecera.  

    |Cód. procedencia mov.|Cantidad|Nº serie|  
    |----------------|--------------|----------------|  
    |1002|2|SN3|  
    |1002|2|SN4|  

14. Seleccione la acción **Actualizar orden producción** para rellenar la línea.  
15. Para introducir los números de serie, seleccione la acción **Líns. seguim. prod.** y, a continuación, los números de las dos líneas en el campo **Nº serie** en la página **Líns. seguim. prod.**.  

    A continuación, registre más consumos de cuadros de bicicleta de LOT1.  
16. En la página **Orden producción lanzada**, seleccione la acción **Diario de producción**.  
17. En la página **Diario de producción**, seleccione la línea de consumo para el producto 2000, elija la acción **Líns. seguim. prod.**
18. En la página **Líns. seguim. prod.**, haga clic en la flecha desplegable del campo **Nº lote**, seleccione **LOT1** y, a continuación, haga clic en **Aceptar**.  
19. Deje los demás valores predeterminados de la página **Diario de producción** y elija la acción **Registrar**.  

    Ha producido cuatro bicicletas de carreras, SN1 a SN4 y consumido cuatro de los diez cuadros de bicicletas de LOT1, dos cuadros en cada orden de producción.  

20. Cierre el diario de producción y las órdenes de producción.  

    A continuación, venda bicicletas de carreras. Primero venda la bicicleta de carreras con NS1 a Selangorian Ltd.  

### <a name="to-sell-the-end-items"></a>Para vender los productos finales

1.  Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Pedidos de venta** y, a continuación, elija el vínculo relacionado.  
2.  Elija la acción **Nuevo** y, a continuación, cree un pedido de venta rellenando los campos siguientes.  

    |Cliente|Producto|Cdad.|Nº serie|  
    |--------------|----------|----------|----------------|  
    |Sellafrio S.L.|1002|1|NS1|  

3.  Para introducir el número de serie, seleccione la acción **Líns. seguim. prod.** y, a continuación, el número en el campo **Nº serie** en la página **Líns. seguim. prod.**.  
4.  Seleccione la acción **Registrar**, elija la opción **Enviar y facturar** y seleccione el botón **Aceptar**.  

    A continuación, venda la bicicleta de carreras con NS2 al Cannon Group PLC.  

5.  Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Pedidos de venta** y, a continuación, elija el vínculo relacionado.  
6.  Elija la acción **Nuevo** y, a continuación, cree un pedido de venta rellenando los campos siguientes.  

    |Cliente|Producto|Cdad.|Nº serie|  
    |--------------|----------|----------|----------------|  
    |GDE Distribución S.A.|1002|1|NS2|  

7.  Para introducir el número de serie, seleccione la acción **Líns. seguim. prod.** y, a continuación, el número en el campo **Nº serie** en la página **Líns. seguim. prod.**.  
8.  Seleccione la acción **Registrar**, elija la opción **Enviar y facturar** y seleccione el botón **Aceptar**.  

    Finalmente, venda algunos cuadros de bicicleta por separado. GDE Distribución S.A. también pide cuatro marcos de bicicletas independientes para su propia línea de montaje.  

9. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Pedidos de venta** y, a continuación, elija el vínculo relacionado.  
10. Elija la acción **Nuevo** y, a continuación, cree un pedido de venta rellenando los campos siguientes.  

    |Cliente|Producto|Cdad.|Nº serie|  
    |--------------|----------|----------|----------------|  
    |GDE Distribución S.A.|2000|5|LOT1|  

11. Para introducir el número de serie, en la ficha desplegable **Líneas**, en el grupo **Línea**, seleccione la acción **Líns. seguim. prod.** y, a continuación, el número en el campo **Nº serie** en la página **Líns. seguim. prod.**.  

    > [!NOTE]  
    >  No registre el último pedido de ventas de cinco cuadros.  

    Así finaliza la preparación de datos para demostrar las características Seguimiento de productos y Buscar movimientos.  

## <a name="tracing-from-usage-to-origin"></a>Seguimiento desde el uso hasta el origen

 En el departamento de ventas, el controlador de calidad averigua que la bicicleta de carrera devuelta, producto 1002, tiene el número de serie NS1. Con esta información básica, puede determinar dónde se utilizó por última vez la bicicleta de carreras terminada, en este caso, en el albarán de venta a Selangorian Ltd. A continuación, el controlador de calidad debe realizar un seguimiento hasta llegar al origen para establecer de qué número de lote procedía el cuadro de carreras defectuoso y qué proveedor lo suministró.  

### <a name="to-determine-which-lot-included-the-faulty-frame-and-who-supplied-it"></a>Para determinar qué lote incluía el cuadro defectuoso y quién lo suministró

1.  Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Seguimiento de productos**, y luego elija el enlace relacionado.  
2.  En la página **Seguimiento productos**, escriba **NS1** en el campo **Filtro nº serie** y, a continuación, **1002** en el campo **Filtro producto**.  
3.  Conserve la configuración predeterminada de **Sólo producto seguido** en el campo **Mostrar componentes** y conserve el método de seguimiento predeterminado de **Uso - Origen** en **Método seguimiento**.  
4.  Seleccione la acción **Realizar seguimiento**.  

    Observe que una cabecera de envío de venta coincide con los criterios de búsqueda. Antes de continuar el seguimiento, verifique que el envío es el que se usó para enviar la bicicleta de carrera defectuosa a Sellafrio S.L.  

5.  Seleccione la línea de seguimiento y, a continuación, seleccione la acción **Mostrar documento**.  

    Ahora, continúe realizando el seguimiento del envío de venta de la bicicleta de carreras con el número NS1.  
6.  Elija el icono + de las líneas de seguimiento para expandir gradualmente y realizar el seguimiento hacia atrás en la cadena de transacciones desde la que se origina el envío de venta.  

    Puede realizar un seguimiento del historial siguiente de la transacción:  

    - El primer documento registrado hacia atrás en la cadena de transacciones es el registro de salida de NS1 de la primera orden de producción lanzada.  
    - El siguiente documento registrado hacia atrás después de aquél es el registro de consumo desde la primera orden de producción lanzada. Aquí, el controlador de calidad ve que se ha usado un cuadro de bicicleta de LOT1.  
    - El último documento registrado en esta cadena es el histórico albaranes de compra en el cual los cuadros de bicicletas con LOT1 entraron en el inventario.  

    El controlador de calidad ya ha establecido qué lote de cuadros de bicicletas estaba defectuoso y puede buscar la última línea de seguimiento para ver qué proveedor los suministró; se trata de Custom Metals Incorporated.  

    > [!NOTE]  
    >  No realice más modificaciones en el resultado del seguimiento, pues lo va a utilizar en la próxima sección.  

     De este modo finaliza la primera tarea de gestión de defectos mediante la página **Seguimiento productos**. El controlador de calidad ahora debe determinar si otros documentos registrados han procesado cuadros de bicicleta de LOT1.  

## <a name="tracing-from-origin-to-usage"></a>Seguimiento desde el origen hasta el uso

 El controlador de calidad ha establecido que los cuadros de bicicletas defectuosos procedían de LOT1. Ahora debe buscar otras bicicletas de carrera que contengan cuadros de bicicleta del lote defectuoso, para que se puedan detener o retirar.  

 Un modo de preparar esta tarea de seguimiento en la página **Seguimiento productos** es introducir manualmente LOT1 en el campo de **Filtro nº lote** y 2000 en el campo de **Filtro producto**. Sin embargo, este tutorial utilizará la función de **Realizar seguimiento opuestos - desde línea**.  

### <a name="to-find-all-usage-of-the-faulty-lot"></a>Para buscar todos los usos del lote defectuoso  

1.  En la página **Seguimiento productos**, seleccione la línea del albarán de compra, la última línea de seguimiento, elija **Realizar seguimiento opuestos - desde línea**.  

    El resultado del seguimiento ahora se basa en los filtros de la línea de seguimiento para el albarán de compras, LOT1 y producto 2000, y el resultado se basa en el método de seguimiento **Origen - Uso**.  

    Para obtener una visión general de todos los usos del producto 2000 con LOT1, continúe expandiendo todas las líneas de seguimiento.  

2.  Seleccione la acción **Expandir todo**.  

    Las cuatro primeras líneas de seguimiento hacen referencia al envío de venta a Sellafrio S.L., que ya se ha resuelto. La última línea indica que una bicicleta de carreras más, NS2, se ha producido en la misma orden de producción lanzada y, a continuación, se ha vendido y enviado en otro envío de venta.  

    El controlador de calidad informa inmediatamente al departamento de ventas para que pueda iniciar la retirada de la bicicleta de carreras defectuosa al cliente, GDE Distribución S.A.  

    Al mismo tiempo, puede ver a partir de las tres últimas líneas de seguimiento que otros dos productos, SN3 y SN4, se han producido basándose en cuadros de bicicletas de LOT1. Toma medidas para bloquear los productos finales en existencias.  

    De este modo finaliza la segunda tarea de gestión de defectos mediante la página **Seguimiento productos**. Dado que la página **Seguimiento de productos** se basa únicamente en los movimientos registrados, el controlador de calidad debe continuar hasta la página **Buscar movimientos** para asegurarse de que LOT1 no se utiliza en documentos no registrados.  

## <a name="finding-all-records-of-a-seriallot-number"></a>Búsqueda de un número de serie/lote en todos los registros

 Con la página **Seguimiento productos**, el controlador de calidad ha averiguado que LOT1 contenía los cuadros de bicicletas defectuosos, qué proveedor los suministró y en qué transacción registrada se han usado. Ahora debe determinar si existe LOT1 en algún documento abierto mediante la integración del resultado del seguimiento en la página **Buscar movimientos**, donde puede realizar una búsqueda en todos los registros de la base de datos.  

### <a name="to-find-all-occurrences-of-lot1-in-non-posted-records-such-as-open-orders"></a>Para buscar todas las incidencias de LOT1 en registros no registrados, como pedidos pendientes  

1.  En la página **Seguimiento productos**, seleccione en la primera línea de seguimiento, el albarán de compras de LOT1.  
2.  Seleccione la acción **Buscar movimientos**.  

    La página **Buscar movimientos** está predefinida con filtros de búsqueda basados en el resultado del seguimiento para LOT1. El controlador de calidad reconoce la mayoría de los registros como pertenecientes a documentos ya identificados en la página **Seguimiento productos**. Por ejemplo, la última línea de Buscar movimientos del tipo Orden de producción hace referencia a las dos órdenes de producción emitidas consumieron cuadros de bicicletas de LOT1.  

    Sin embargo, la segunda línea Buscar movimientos del tipo **Línea de venta** es una línea de documento sin registrar, por lo que el controlador de calidad continúa investigando.  

3.  Para abrir el registro de la línea de ventas, seleccione la segunda línea Buscar movimientos y elija la acción **Mostrar**. De manera alternativa, elija el valor en el campo **Nº registros**.  

    Aquí, el controlador de calidad ve una línea de ventas pendiente para los cuadros de bicicletas defectuosos. Sugiere inmediatamente al departamento de ventas que se cancele este pedido y que se inicie una nueva orden de producción basada en cuadros de bicicleta en buenas condiciones.  

 De este modo finaliza el tutorial sobre cómo usar la página **Buscar movimientos** para la gestión de defectos en la integración con la página **Seguimiento de productos**.  

## <a name="see-related-training-at-microsoft-learn"></a>Consulte la formación relacionada en [Microsoft Learn](/learn/paths/use-serial-lot-numbers/)

## <a name="see-also"></a>Consulte también .

[Trabajar con números de lote y de serie](inventory-how-work-item-tracking.md)  
[Realizar seguimiento de productos seguidos](inventory-how-to-trace-item-tracked-items.md)  
[Buscar movimientos](ui-find-entries.md)  
[Tutoriales de procesos empresariales](walkthrough-business-process-walkthroughs.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]