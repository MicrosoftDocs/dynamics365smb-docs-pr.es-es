---
title: Combinar la baja automática y la manual
description: Tutorial para un planificador de producción de Contoso Coffee que quiere combinar la baja automática y la manual.
ms.date: 04/01/2022
ms.topic: article
ms.service: dynamics365-business-central
author: edupont04
ms.author: andreipa
---

# <a name="walkthrough-combine-automatic-and-manual-flushing" />Tutorial: Combinar la baja automática y la manual

En este artículo, le guiaremos a través de los pasos para usar los datos de demostración de Contoso Coffee en la baja.  

## <a name="scenario" />Caso

Usted es el planificador de producción de Contoso Coffee. Debe crear una nueva orden de producción para diez unidades del artículo SP-SCM1004, AutoDrip. Algunos componentes y operaciones se consumirán hacia adelante y otros hacia atrás en función de diferentes condiciones.

## <a name="steps" />Pasos

> [¡Nota!] Recuerde ajustar el inventario registrando el diario de artículos con saldos iniciales.

1. Cree una orden de producción planificada en firme para cinco unidades del artículo **SP-SCM1004, AutoDrip** en la ubicación *NORTE*. Para obtener orientación, consulte [Tutorial: Crear una nueva orden de producción planificada en firme y cambiarla](create-firm-planned-production-order-change.md).  

2. Lance la orden de producción.

    1. Seleccione la acción **Cambiar estado**.  

    2. En la página que aparece, establezca el campo **Nuevo estado** en *Lanzada* y, a continuación, elija el botón **Sí**.  

        Aparece un mensaje que tiene una barra de estado y hace referencia al consumo automático. A continuación, aparece un mensaje de confirmación de que la orden ha pasado a tener el estado *Lanzada*.  

    3. Elija el botón **Aceptar** para cerrar el mensaje de confirmación.

3. Revise los movimientos de producto y de capacidad para la orden de producción.

    1. Elija el icono ![Bombilla que abre la función Dígame.](../../media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Orden de producción lanzada** y, a continuación, elija el vínculo relacionado.  

    2. Abra la orden de producción con las 5 unidades de la cafetera AutoDrip.  

    3. Seleccione la acción **Movs. productos**.  

        El producto **SP-BOM1305 Tornillo hexagonal M3, zinc** se baja inmediatamente con la cantidad completa esperada. Cierre la página **Movs. productos**.  

    4. Elija la acción **Movs. capacidad**.  Tenga en cuenta que, en el momento de la liberación del pedido, también se completó una entrada de operaciones de ensamblado de cuerpo. Cierre la ventana **Movs. capacidad**.

    Puede bajar manualmente los productos de componentes mediante el diario de consumo o producción. La baja manual le permite ajustar la cantidad antes de registrar. Por ejemplo, si es necesaria una cantidad adicional para cubrir materias primas de baja calidad.
4. Baje los componentes de forma manual.  
    1. Elija el icono ![Bombilla que abre la función Dígame.](../../media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Diario de consumo** y, a continuación, elija el vínculo relacionado.  

    2. Elija la acción **Calcular consumo**.  

    3. En la página de solicitud **Calcular consumo**, en la ficha desplegable **Orden de producción**, defina un filtro para la orden específica en el campo **Nº orden** y luego seleccione el botón **Aceptar**. Después de que se cierre la página de solicitud de trabajo por lotes, tenga en cuenta que la página **Diario de consumo** se completa con los componentes que requieren consumo manual.

    4. Elija la acción **Registrar**. Cierre el diario de consumo.

5. Registre manualmente la salida para el cableado eléctrico.  

    Debe rellenar manualmente los campos **Tiempo preparación** y **Tiempo ejecución**. También puede especificar la cantidad realmente producida y el rechazo. Introduzca *3* como la cantidad de salida y registre la salida.

    1. Elija el icono ![Bombilla que abre la función Dígame.](../../media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Diario salida**, y luego elija el enlace relacionado.  

    2. En la página **Diario salida**, cree una nueva línea de diario.  

    3. En el campo **Nº orden**, especifique la orden.  

    4. Elija la acción **Desplegar ruta**.  

        La página **Diario salida** se completa con la línea de operación solo para el cableado eléctrico.

    5. Establezca el campo **Tiempo ejecución** en *10*.  

    6. Cambie el campo **Cantidad** de *5* a *3*.

    7. Elija **Registrar**.  
    8. Cierre el libro de salida.

6. Revise los movimientos de producto para la orden de producción.

    1. En la página de la orden de fabricación, seleccione la acción **Movs. productos**.  

    El producto **SP-BOM1302, Pantalla del panel de control** se registra con una cantidad de *3*, basado en la salida real, mientras que **SP-BOM1303, Botón** se registra con la cantidad total esperada. Cierre la página **Movs. productos**.

7. Finalice la orden de producción.  

    1. Seleccione la acción **Cambiar estado**.
    2. En la página que aparece, establezca el campo **Nuevo estado** en *Finalizada* y, a continuación, elija el botón **Sí**.  

        Aparece un mensaje con una barra de estado que refleja el consumo automático. A continuación, aparece un mensaje de confirmación de que la orden ha pasado a tener el estado *Finalizada*. La orden de producción terminada tiene el mismo número que tenía con el estado *Lanzada*.
    3. Elija el botón **Aceptar** para cerrar el mensaje de confirmación.

8. Vuelva a revisar los movimientos de producto y de capacidad para la orden de producción.

    1. Elija la acción **Movs. capacidad**.  

        La entrada de operaciones de ensamblado se completó en el momento en que se lanzó la orden. La cantidad producida (salida) es *5*, independientemente de la salida del paso anterior. Cierre la página **Movs. capacidad**.

    2. Seleccione la acción **Movs. productos**.  

        La cantidad en el movimiento de producto del tipo *Salida* es igual a la cantidad de salida en el movimiento de capacidad. La cantidad consumida de **SP-BOM1301, Alojamiento AutoDrip** y **SP-BOM1304, Jarra térmica fija acero inox.** es 5 para ambos porque la salida esperada y la salida real son las mismas. 

    3. Cierre la página **Movs. productos**.  

Eso es todo para la baja manual y automática de componentes.

## <a name="see-also" />Consulte también .

[Bajar componentes según la salida de la operación](../../production-how-to-flush-components-according-to-operation-output.md)  
[Introducción a datos de demostración de Contoso Coffee](contoso-coffee-manufacturing-intro.md)  
