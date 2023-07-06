---
title: Utilice la planificación de pedidos para crear y reservar suministros
description: Tutorial para aprender a usar la planificación de pedidos para crear el pedido de producción requerido para el suministro en Business Central.
ms.date: 04/01/2022
ms.topic: article
ms.service: dynamics365-business-central
author: edupont04
ms.author: andreipa
---

# <a name="walkthrough-use-order-planning-to-create-and-reserve-supply"></a><a name="walkthrough-use-order-planning-to-create-and-reserve-supply"></a><a name="walkthrough-use-order-planning-to-create-and-reserve-supply"></a><a name="walkthrough-use-order-planning-to-create-and-reserve-supply"></a>Guía: Utilice la planificación de pedidos para crear y reservar suministros

En este artículo, lo guiaremos a través de los pasos para usar los datos de demostración de Contoso Coffee en la planificación de pedidos.

## <a name="scenario"></a><a name="scenario"></a><a name="scenario"></a><a name="scenario"></a>Caso

Usted es el planificador de producción de Contoso Coffee. Creó una orden de producción para 100 unidades del artículo **SP-SCM1009, Airpot** y desea planificar subensamblajes para este pedido. La planificación de pedidos se utiliza para crear la orden de fabricación necesaria para el suministro. Debido a que está creando la orden de producción para cumplir con los requisitos de una orden específica, decide reservar la salida de la orden de producción.  

## <a name="steps"></a><a name="steps"></a><a name="steps"></a><a name="steps"></a>Pasos

1. Cree la nueva orden de producción liberada para 100 unidades del artículo **SP-SCM1009, Airpot**.

    1. Elija el icono ![Bombilla que abre la función Dígame.](../../media/ui-search/search_small.png "Dígame qué desea hacer") icono, escriba **Orden de producción lanzada** y, a continuación, elija el vínculo relacionado.  

    2. Elija la acción **Nuevo** y, a continuación, rellene los campos tal como se describe en la tabla siguiente.  

        |Campo  |Valor  |
        |---------|---------|
        |**Tipo procedencia mov.** |Producto|
        |**Cód. procedencia mov.** |SP-SCM1009|
        |**Cantidad** |100|
    3. Elija la acción **Actualizar orden producción**.  

    Tenga en cuenta el número de lanzamiento de la orden de producción.

2. Abra la página **Planificación de pedidos** y calcule un nuevo plan.

    1. Seleccione la acción **Planificación**.  

    2. En la página **Planificación de pedidos**, seleccione la acción **Calcular plan**.  

    3. Desplácese hacia abajo hasta la línea de demanda que representa la orden de producción lanzada que creó anteriormente.  

    4. Expanda las línea a para ver los detalles de la línea de demanda. Confirme que es una sugerencia para una orden de producción de 100 unidades del artículo 1001.  

3. Cree una nueva orden de producción para 100 unidades de artículo **SP-BOM2000, Reservoir Assy.** y reserve la salida de esta orden de producción en nombre de la orden principal relacionada.  

    1. Seleccione la casilla de verificación en el campo **Reserva** en la línea de demanda de las 100 unidades del artículo SP-BOM2000.

    2. Seleccione la acción **Crear pedidos**.  

    3. Establezca el campo **Crear pedidos para** a *La Línea Activa*.  

    4. Establezca el campo **Crear orden de producción** a *Planificación firme*.

    5. Elija el botón **Aceptar** para crear la orden de producción.

    6. En la página **Planificación de pedidos**, confirme que se eliminó la línea de demanda de las 100 unidades del artículo 1001.

Eso es todo para la planificación de pedidos en [!INCLUDE [prod_short](../../includes/prod_short.md)].  

## <a name="see-also"></a><a name="see-also"></a><a name="see-also"></a><a name="see-also"></a>Consulte también .

[Introducción a datos de demostración de Contoso Coffee](../contoso-coffee-intro.md)  
[Sobre los pedidos de producción](../../production-about-production-orders.md)  
