---
title: Configurar calendarios base
description: 'Puede asignar un calendario base a su empresa y sus socios comerciales, para calcular las fechas de entrega y recepción de acuerdo con los días hábiles especificados.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: '7600, 7601, 7602, 5703'
ms.date: 06/11/2021
ms.author: bholtorf
---
# Configurar calendarios base

Puede asignar un calendario base a la empresa y a los socios comerciales, como clientes, proveedores o almacenes. Se calculan las fechas de entrega y de recepción de futuros pedidos de venta, pedidos de compra, pedidos de transferencia y líneas de órdenes de producción según los días laborables especificados en el calendario. La tarea principal en la configuración de un calendario base nuevo es especificar y definir los días no laborables que desea aplicar.  

## Para configurar un calendario base

1.  Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Calendario base** y luego elija el enlace relacionado.  
2.  Seleccione la acción **Nuevo**.  
3.  Rellene el campo **Código**.  
4. Seleccione la acción **Mantener cambios en el calendario base** .
5. En la página **Cambios en el calendario base**, utilice el campo **Sistema periódico** para marcar una fecha o un día determinado como día no laborable periódico. Puede seleccionar la opción **Periódico anual** o **Periódico semanal**.  

    Si selecciona **Periódico anual**, también debe especificar la fecha pertinente en el campo **Fecha**.  

    Si selecciona **Periódico semanal**, deberá seleccionar también el día de la semana correspondiente en el campo **Día**. Si deja el campo en blanco, debe rellenar el campo **Fecha**. El campo **Día** se rellena de forma automática.  

Cuando se realice un movimiento, se selecciona el campo **No laborables**. Puede elegir borrar la marca de verificación para hacerlo un día laborable.  
 Cuando vuelva a la ficha de calendario base, verá que se han actualizado los valores de los días no laborables que ha introducido. Estas entradas aparecen ahora en color rojo y se selecciona el campo de **No laborables**.  

> [!NOTE]  
>  Al configurar un calendario base nuevo, puede seleccionar y copiar líneas de un calendario existente. Hágalo en la página **Cambios calendario base**.  

> [!IMPORTANT]  
>  Los calendarios base definidos para un proveedor o ubicación afecta en cómo se calculan las fechas y se redondea a los días laborables.
Especifica una fórmula de fecha con el tiempo que se tarda en reponer el producto. Se utiliza para calcular el campo **Fecha de recepción planificada**, si se calcula hacia adelante, y el campo **Fecha de pedido**, si calcula hacia atrás. Consulte [Plazo entrega (días)](across-how-to-assign-base-calendars.md#lead-time-calculation).

## Plazo entrega (días)

Los calendarios base definidos para un proveedor o ubicación afecta en cómo se calculan las fechas y se redondea a los días laborables. Del mismo modo, los dos campos clave de fecha de las líneas de pedido de compra se calculan como sigue en distintas condiciones.

|Dirección de cálculo|Calendario de proveedor definido|Calendario de proveedor no definido|
|---------------------|-----------------------|---------------------------|
|Adelante|planned receipt date = order date + vendor lead time (por calendario de proveedor y redondeado al siguiente día laborable en, primero el calendario de proveedor y después el calendario de la ubicación)|planned receipt date = order date + vendor lead time (por el calendario de la ubicación)|
|Atrás|order date = planned receipt date - vendor lead time (por calendario de proveedor y redondeado al anterior día laborable en, primero el calendario de proveedor y después el calendario de la ubicación)|order date = planned receipt date - vendor lead time (por el calendario de la ubicación)|

> [!NOTE]
> Además del plazo de entrega que afecte a la fecha de envío planificada y fecha de pedido, como se muestra en la tabla descritas anteriormente, tiempo de manipulación en almacén y plazo de seguridad se pueden agregar a las fórmulas para conformar el valor del campo **Fecha de recepción esperada**, como se indica a continuación: Fecha de recepción planificada + plazo de seguridad + tiempo de manipulación en el almacén = Fecha de recepción esperada.

> [!Important]
> Si su almacén utiliza un calendario significativamente distinto al de sus proveedores, entonces es importante que se definan los calendarios concretos para esos proveedores, para calcular el plazo de proveedor óptimo. Para obtener información acerca de cómo configurar calendarios de proveedor, consulte [Asignar un calendario base](across-how-to-assign-base-calendars.md#to-assign-a-base-calendar).

El contenido del campo **Cálculo del plazo de entrega** se copia de la ficha de producto o de la ficha SKU, si el plazo se define para el producto, o en la página **Catálogo de productos del proveedor**, si el plazo se define para el proveedor.

## Para personalizar un calendario
La tarea principal en la personalización de un calendario base para su empresa, o uno de sus socios comerciales, es cambiar el estado de los días laborables y días no laborables.

Por ejemplo, mientras que un calendario base normalmente enumeraría todos los sábados como días no laborables, el calendario personalizado de un almacén determinado puede mostrar todos los sábados de los meses de noviembre y diciembre, incluso las vacaciones, como días laborables.

El siguiente procedimiento utiliza este almacén como ejemplo. Tenga en cuenta que en este momento, ya ha asignado a un calendario base al almacén.

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Ubicaciones** y luego elija el enlace relacionado.
2. Abra la ubicación que desea actualizar y seleccione el campo **Calendario personalizado**. Tenga en cuenta que debe seleccionarse un calendario en el campo **Código calendario base**.
3. En la página **Entradas del calendario personalizadas**, seleccionar la acción **Mantener los cambios del calendario personalizado**.
4. En **Cambios personalizados del calendario**, añada líneas para las entradas del calendario personalizadas.

    Cuando se introduce una línea, el cuadro de verificación **No laborables** está seleccionado. Puede quitar la marca de verificación si desea cambiar el estado a día laborable.

    Puede utilizar el campo **Sistema periódico** para definir una fecha o un día determinado como día no laborable periódico. Puede seleccionar la opción **Periódico anual** o **Periódico semanal**.

    Si selecciona **Periódico anual**, también debe especificar la fecha pertinente en el campo **Fecha**. Si selecciona **Periódico semanal**, deberá seleccionar también el día de la semana correspondiente en el campo **Día**. Si deja el campo en blanco, debe rellenar el campo **Fecha**. El campo **Día** se rellena de forma automática. Esto sería útil si deseara marcar una fecha determinada como día no laborable o laborable.

5. Elija el botón **Aceptar**.

La página **Movs. calendario personaliz.**, verá que los movimientos de fechas se actualizan con los cambios que realiza.

En la ficha ubicación, verá que el campo **Calendario personalizado** contiene la palabra **Sí**, lo que indica que se ha configurado un calendario personalizado.

> [!Important]
> Si no rellena el campo **Cód. almacén** de la línea de pedido, se utiliza el calendario de la empresa.


Si no rellena el campo **Cód. transportista** de la línea de pedido, se utiliza el calendario de la empresa.

> [!NOTE]  
> Si realiza cambios en un calendario base para el cual ya hay cambios en el calendario personalizado, se actualizan automáticamente todos los calendarios personalizados existentes.

## Para asignar un calendario base  
Como ejemplo, el siguiente procedimiento programa fechas de entrega en líneas de pedidos de venta para un cliente.

Los calendarios base se asignan a su propia empresa, clientes, proveedores, almacenes, y transportistas de la siguiente forma:  

-   En las fichas **Información de la empresa** y **Cliente**, el calendario base se asigna en la ficha desplegable **Envío**.  
-   En la ficha **Proveedor**, el calendario base se asigna en la ficha desplegable **Recepción**.  
-   En la ficha **Almacén**, el calendario base se asigna en la ficha desplegable **Almacén**.  
-   En la página **Transportistas**, el calendario base se asigna en la página **Servicios transportista**.  

1.  Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Clientes** y luego elija el enlace relacionado.  
2.  Abra la ficha **Cliente** a la que asignará un calendario base.  
3.  En la ficha desplegable **Envío**, en el campo **Código calendario base**, seleccione el calendario base que desea asignar.  

> [!IMPORTANT]  
>  -   Si no asigna un calendario base a una empresa, todas las fechas se calculan como días laborables.  
> -   Si introduce un almacén en blanco en una línea de pedido, todas las fechas se calculan como días laborables.  
> -   Los calendarios base definidos para un proveedor o ubicación afecta en cómo se calculan las fechas y se redondea a los días laborables.

> [!NOTE]  
>  Antes de que pueda introducir valores en un calendario personalizado, primero debe asignar un calendario base a la empresa.  

## Consulte también
[Compras](purchasing-manage-purchasing.md)  
[Fabricación](production-manage-manufacturing.md)    
[Inventario](inventory-manage-inventory.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]