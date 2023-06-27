---
title: Configurar nueva capacidad
description: Tutorial para aprender a configurar un nuevo centro de trabajo con un calendario de capacidad para un solo turno en Business Central.
ms.date: 04/01/2022
ms.topic: article
ms.service: dynamics365-business-central
author: edupont04
ms.author: andreipa
---

# <a name="walkthrough-set-up-new-capacity"></a><a name="walkthrough-set-up-new-capacity"></a>Guía: Configurar nueva capacidad

En este artículo, lo guiaremos a través de los pasos para usar los datos de demostración de Contoso Coffee en la forma en que administra la capacidad.  

## <a name="scenario"></a><a name="scenario"></a>Caso

Usted es el planificador de producción de Contoso Coffee. En respuesta a los cambios en el taller, debe configurar un nuevo centro de trabajo, Departamento de pruebas. El nuevo centro de trabajo tiene un centro de máquina, Pruebas. Los nuevos centros deberán contar con un calendario de aforo para un solo turno de 08:00:00 AM a 4:00:00 PM, de lunes a viernes.  

## <a name="steps"></a><a name="steps"></a>Pasos

1. Configurar el centro de trabajo.

    1. Elija el icono ![Bombilla que abre la función Dígame.](../../media/ui-search/search_small.png "Dígame qué desea hacer") icono, escriba **Centros de trabajo** y luego elija el enlace relacionado.  

    2. Elija la acción **Nuevo** y, a continuación, rellene los campos tal como se describe en la tabla siguiente.  

        |Campo  |Valor  |
        |---------|---------|
        |**Nº** |700|
        |**Nombre** |Departamento de pruebas|
        |**Cód. grupo centro trab.** |1, Departamento de producción|
        |**Coste unitario directo**|3,25|
        |**Cálculo coste unitario**|Hora|
        |**Método de baja**|Manual|
        |**Grupo contable producto**|NO IVA</br></br>Tenga en cuenta que esta selección depende de su configuración de contabilidad y país.|
        |**Cód. unidad medida** |MINUTOS|
        |**Capacidad** |1|
        |**Eficiencia** |90|
        |**Cód. calend. planta** |1|

        En el campo **Código de calendario de tienda** la configuración 1 significa un turno de lunes a viernes.

    3. Cierre la tarjeta del centro de trabajo.

2. Configurar centro de máquina.

    1. Elija el icono ![Bombilla que abre la función Dígame.](../../media/ui-search/search_small.png "Dígame qué desea hacer") icono, escriba **Centros de máquina** y luego elija el enlace relacionado.  

    2. Elija la acción **Nuevo** y, a continuación, rellene los campos tal como se describe en la tabla siguiente.  

        |Campo  |Valor  |
        |---------|---------|
        |**Nº** |760|
        |**Nombre** |Pruebas|
        |**Nº centro trabajo** |700, Departamento de pruebas|
        |**Coste unitario directo**|3,25|
        |**Método de baja**|Manual|
        |**Grupo contable producto**|NO IVA</br></br>Tenga en cuenta que esta selección depende de su configuración de contabilidad y país.|
        |**Capacidad** |1|
        |**Eficiencia** |90|
    3. Expanda la ficha desplegable **Configuración de enrutamiento** y luego, en el campo **Tiempo de configuración**, introduzca *10*.  

3. Calcular el calendario de capacidad del centro máquina.  

    1. Elija la acción **Calendario**.  

    2. En página **Calendario del centro de máquinas**, en la ficha desplegable **Opciones de matriz**, establezca el campo **Ver por** a *Mes*.  

    3. Elija la acción **Mostrar matriz**.  

    4. En la página **Calendario de matriz de centro máquina**, elija la acción **Calcular**.  

    5. En página **Calc. calendario centro máquina**, en la ficha desplegable **Opciones**, establezca el campo **Fecha inicial** a *Enero 01*.  

    6. Seleccione el campo **Fecha de finalización** al 31 de diciembre.  

    7. En la ficha desplegable **Centro máquina**, rellene el campo **Nº** Campo de filtro, seleccione *760, Prueba*.  

    8. Elija el botón **Aceptar**. Una vez que finaliza el trabajo por lotes, vuelve a la página **Matriz de calendario de centro de máquina**.  

    9. Seleccione la acción **Actualizar**.  

    10. En la línea del centro de máquina 760, Pruebas, profundice en el valor de la columna de enero.  

En la página **Entradas de calendario**, las entradas de capacidad diaria en el campo **Capacidad (Total)** son de 480 minutos. Esto refleja un turno de ocho horas por cada día de trabajo. Además el campo **Capacidad (Efectiva)** muestra 432 minutos. Esto refleja la tasa de eficiencia del 90 por ciento que asignó al centro de máquinas.  

## <a name="see-also"></a><a name="see-also"></a>Consulte también .

[Introducción a datos de demostración de Contoso Coffee](../contoso-coffee-intro.md)  
