---
title: Configurar y procesar una operación de subcontratación
description: Tutorial para aprender a configurar y procesar una operación de subcontratación en Business Central.
ms.date: 04/01/2022
ms.topic: article
ms.service: dynamics-365-business-central
author: brentholtorf
ms.author: bholtorf
---

# Configurar y procesar una operación de subcontratación

En este artículo, lo guiaremos a través de los pasos para usar los datos de demostración de Contoso Coffee en la subcontratación.

## Caso

Usted es el planificador de producción de Contoso Coffee. Debido a limitaciones de capacidad, planea usar un subcontratista para producir el artículo **SP-SCM1009, Airpot**.

Aquí, crea una nueva orden de producción liberada para 12 unidades del artículo SP-SCM1009, Airpot, usando Enrutamiento - SP-SCM1009-SUB-2. Utilice la hoja de trabajo de subcontratación para generar una orden de compra para la producción y luego finalice la operación al recibir y facturar la orden de compra.

## Pasos

1. Cree una nueva orden de producción liberada para 12 unidades del artículo SP-SCM1009, Airpot.

    1. Elija el icono ![Bombilla que abre la función Dígame.](../../media/ui-search/search_small.png "Dígame qué desea hacer") icono, escriba **Orden de producción lanzada** y, a continuación, elija el vínculo relacionado.  

    2. Elija la acción **Nuevo** y, a continuación, rellene los campos tal como se describe en la tabla siguiente.  

        |Campo  |Valor  |
        |---------|---------|
        |**Tipo procedencia mov.** |Producto|
        |**Cód. procedencia mov.** |SP-SCM1009|
        |**Cantidad** |100|
    3. Elija la acción **Actualizar orden producción**.  

2. Reemplace la ruta a SP-SCM1009-SUB-2 en la línea de orden de producción y luego actualice la orden de producción pero solo para la ruta.  

    1. Agregue el campo Número de ruta de producción a las Líneas en la Orden de producción emitida.<!--in code, this is marked as visible=false-->

    2. Cambie el campo **Número de ruta** de *SP-SCM1009-SERIAL* a *SP-SCM1009-SUB-2*.  

    3. Elija la acción **Actualizar orden producción**.  

    4. En la página de solicitud **Actualizar orden de producción** borre los campos **Líneas** y **Componente necesario** para que la tarea se ejecute solo para enrutamiento y, a continuación, elija el botón **Aceptar**.

3. Utilice la hoja de trabajo de subcontratación para generar una orden de compra para la operación subcontratada en la orden de producción que creó en el paso 2.  

    1. Elija el icono ![Bombilla que abre la función Dígame.](../../media/ui-search/search_small.png "Dígame qué desea hacer") icono, escriba **Hojas de trabajo de subcontratación** y, a continuación, elija el vínculo relacionado.  

    2. Elija la acción **Calcular subcontrataciones**.

    3. Seleccione el campo **Aceptar mensaje acción** para la línea nueva.

    4. Seleccione la acción **Ejecutar mensajes de acción**.  

    5. En la página de solicitud **Ejecutar mensaje de acción. – Req.**, acepte todos los valores predeterminados y luego elija el botón **Aceptar**.

    6. Cuando termine el trabajo por lotes, elija el botón **Aceptar** para cerrar la hoja de trabajo de subcontratación.  

4. Recibir y facturar la orden de compra.  

    1. Elija el icono ![Bombilla que abre la función Dígame.](../../media/ui-search/search_small.png "Dígame qué desea hacer") icono, escriba **pedidos de compra** y, a continuación, elija el vínculo relacionado.  

    2. En la lista **Ordenes de compra**, busque la orden de compra del proveedor 82000 Subcontratista.

    3. En el campo **Nº factura de proveedor**, introduzca *542349*.

    4. En la ficha desplegable **Líneas**, seleccione la línea y luego configure el campo **Coste directo** a *18*.

    5. Seleccione la acción **Registrar**.  

    6. En el mensaje de solicitud, elija la opción **Recibir y Facturar**.  

La salida del artículo SP-SCM1009 Airpot ahora está registrada.

## Consulte también .

[Introducción a datos de demostración de Contoso Coffee](../contoso-coffee-intro.md)  
