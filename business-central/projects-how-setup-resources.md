---
title: 'Configurar costes de recurso, precios y capacidad'
description: 'Para utilizar recursos y facilitar la administración de proyectos, especifique costes y precios para recursos individuales o grupos de recursos, y configure la capacidad de recursos.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'project management, capacity, staff'
ms.search.form: '72, 76, 77, 203, 204'
ms.date: 04/01/2021
ms.author: edupont
---
# <a name="set-up-resources-for-projects"></a><a name="set-up-resources-for-projects"></a>Configurar recursos para proyectos

Para administrar correctamente las actividades de recursos, debe configurar los recursos, y los costes y los precios relacionados. Las reglas de precios, descuentos y factores de coste relacionadas con el proyecto se configuran en la tarjeta respectiva. Puede especificar los costes y los precios de recursos individuales, de grupos de recursos o de todos los recursos disponibles de la empresa.

Si se utilizan o venden recursos en un proyecto, los precios y costes asociados con ellos se recuperan de la información que haya configurado.

Debe especificar el importe predeterminado por hora cuando se crea el recurso. Por ejemplo, si utiliza un equipo específico en un proyecto durante cinco horas, el proyecto se calcularía en función del importe por hora.

> [!NOTE]
> Puede comprar recursos externos, por ejemplo, para facturar a un proveedor por el trabajo entregado. Para obtener más información, consulte [Registrar compras](purchasing-how-record-purchases.md).<br /><br />
> Para recursos externos, recomendamos que los nombre o agrupe de modo que no se confundan con sus recursos internos.
>  
> Si está registrando transacciones de empresas vinculadas, aunque puede asignar un recurso a una línea en un pedido de ventas, si convierte el pedido de ventas en un pedido de compra en el lado receptor, el recurso no se incluirá. Para usar recursos en transacciones de empresas vinculadas, use el campo **Compra de IC. cuenta del L/M No.** en la tarjeta de recursos para especificar la cuenta en la que contabilizar los gastos.

## <a name="to-set-up-a-resource"></a><a name="to-set-up-a-resource"></a>Para configurar un recurso

Cree una ficha por cada recurso que desee utilizar en los proyectos.

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Recursos** y luego elija el enlace relacionado.
2. Seleccione la acción **Nuevo**.
3. Rellene los campos según sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

## <a name="to-set-up-a-resource-group"></a><a name="to-set-up-a-resource-group"></a>Para configurar una familia de recursos

En una familia de recursos se pueden combinar varios recursos. En ellas se agrupan todas las capacidades y presupuestos cada uno de los recursos. Las capacidades de las familias de recursos pueden introducirse también independientemente de los valores acumulados o bien sumándolas a estos.

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Grupos de recursos** y luego elija el enlace relacionado.
2. Seleccione la acción **Nuevo**.
3. Rellene los campos según sea necesario.

## <a name="to-set-capacity-for-a-resource"></a><a name="to-set-capacity-for-a-resource"></a>Para configurar la capacidad de un recurso

Para calcular cuánto tiempo puede dedicar un recurso a los trabajos, su capacidad debe definirse primero como tiempo disponible por periodo en el calendario de trabajo. Utilice esta configuración para rellenar las líneas de planificación del proyecto que contienen el recurso. Para obtener más información, vea [Crear proyectos](projects-how-create-jobs.md).

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Recursos** y luego elija el enlace relacionado.
2. Abra la ficha de recurso correspondiente y, a continuación, elija la acción **Capacidad recurso**.
3. En la página **Capacidad del recurso**, en el campo **Ver**, especifique la duración del periodo, por ejemplo **Día**, que se muestra en columnas en la ficha desplegable **Matriz capacidad recurso**.
4. Para cada recurso de una línea, especifique por cada periodo de las columnas el número de horas que el recurso está disponible.
5. Opcionalmente, para detallar la capacidad semanal de recursos en una fecha inicial y final, elija la acción **Establecer capacidad**.
6. En la página **Config. capacidad recurso**, rellene los campos según sea necesario.
7. Elija la acción **Actualizar capacidad**. La página **Capacidad recurso** se actualiza con la capacidad introducida.
8. Cierre la página.

## <a name="to-set-up-alternate-resource-costs"></a><a name="to-set-up-alternate-resource-costs"></a>Para configurar costes de recursos alternativos

Además del coste especificado en la tarjeta de recurso, puede configurar costes alternativos para cada recurso. Por ejemplo, si paga a un empleado un sueldo por horas distinto para el trabajo en horas extraordinarias, puede configurar un precio de coste de recurso para el sueldo por horas extraordinarias. El coste alternativo que configuró para el recurso anulará el precio de coste de la ficha de recurso cuando utilice el recurso en el diario de recursos.

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Recursos** y luego elija el enlace relacionado.  
2. Seleccione el recurso para el que desee configurar varios costes alternativos y, a continuación, elija la acción **Costes**.  
3. En la página **Precio de coste del recurso**, rellene los campos en una línea según sea necesario.  
4. Repita el paso 3 para cada precio de coste de recurso alternativo que desee configurar.

**Nota**. Para configurar precios de coste de recursos aplicables a todos los recursos y familias de recursos, abra la página **Precio de coste del recurso** y rellene los campos.

## <a name="to-set-up-alternate-resource-prices"></a><a name="to-set-up-alternate-resource-prices"></a>Para configurar precios de recursos alternativos

Además del precio especificado en la tarjeta de recurso, puede configurar precios alternativos para cada recurso. Estos precios alternativos pueden ser condicionales. Pueden depender de si el recurso se consume con un proyecto o tipo de trabajo determinado.

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Recursos** y luego elija el enlace relacionado.
2. Seleccione el recurso para el que desee configurar varios precios alternativos y, a continuación, elija la acción **Precios**.
3. En la página **Precio de venta del recurso**, rellene los campos en una línea según sea necesario.
4. Repita el paso 3 para cada precio de venta de recurso alternativo que desee configurar.

## <a name="see-related-microsoft-training"></a><a name="see-related-microsoft-training"></a>Consultar la [formación de Microsoft](/training/paths/set-up-jobs-resources/) relacionada

## <a name="see-also"></a><a name="see-also"></a>Consulte también .

[Configurar la administración de proyectos](projects-setup-projects.md)  
[Administración de proyectos](projects-manage-projects.md)  
[Finanzas](finance.md)  
[Compras](purchasing-manage-purchasing.md)  
[Ccial](sales-manage-sales.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
