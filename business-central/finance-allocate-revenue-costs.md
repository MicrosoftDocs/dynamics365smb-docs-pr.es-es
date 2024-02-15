---
title: Asignar ingresos y costos a múltiples cuentas del libro mayor
description: Aprenda cómo asignar costes a una o más cuentas en su libro mayor.
author: brentholtorf
ms.author: bholtorf
ms.date: 09/04/2023
ms.topic: conceptual
ms.search.keywords: 'allocate, allocation, accounts'
ms.search.form: '39, 2673, 2670, 2674,'
ms.custom: bap-template
ms.service: dynamics-365-business-central
---

# Asignar ingresos y costos a múltiples cuentas del libro mayor

Este artículo describe cómo utilizar cuentas de asignación para distribuir importes en documentos de compras y ventas y líneas de diario general a diferentes cuentas del L/M. Puede asignar cantidades a través de una distribución fija o variable.  

La asignación divide una línea del diario general en las líneas definidas en la página **Cuenta de asignación**. Por ejemplo, si divide un gasto de alquiler de tres maneras usando dimensiones, tendrá tres líneas para publicar para la asignación. Por lo tanto, tendrá seis líneas del Libro Mayor (o posiblemente más si utiliza el IVA o el impuesto sobre las ventas). Aunque esto contabiliza más asientos del Libro Mayor de los que podría necesitar, le permite revertir líneas individuales en lugar de revertir toda la asignación.

Las cuentas de asignación también funcionan con aplazamientos. Para obtener más información sobre los fraccionamientos, vaya a [Fraccionar ingresos y gastos](finance-how-defer-revenue-expenses.md).

La siguiente tabla presenta los métodos de asignación que puede utilizar.

|Método de asignación  |Descripción  |
|---------|---------|
|Corregido     | Cuando desee dividir los gastos de una manera que se repita durante un período de tiempo más largo, puede utilizar una asignación fija. Una asignación fija le permite definir la división de la asignación. Esta división solo cambiará cuando cambie la configuración en la página **Cuenta de asignación**.        |
|Variable     | Para distribuir ingresos o gastos en función de valores que cambian con el tiempo, utilice el método de asignación variable. Las asignaciones variables le permiten especificar las fuentes que se utilizarán para calcular los porcentajes de asignación. Este método es útil, por ejemplo, para dividir los costos de los empleados según la cantidad de personal en el departamento o división. Otro ejemplo es la distribución del costo del alquiler en función del metraje del piso de producción, que puede variar según la línea de producción a lo largo del tiempo. Las asignaciones variables utilizan una combinación de dimensiones y cuentas estadísticas para determinar cómo se distribuyen los montos durante un período de tiempo. Para obtener más información sobre las cuentas estadísticas, vaya a [Analizar datos con cuentas estadísticas](bi-use-statistical-accounts.md). Para obtener más información sobre las dimensiones, vaya a [Trabajar con dimensiones](finance-dimensions.md).        |

## Utilice un método de porcentaje o participación fija para asignar cantidades

1. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Asignación de cuenta** y luego elija el enlace relacionado.  
1. En la página **Asignación de cuentas**, seleccione la acción **Nuevo**.
1. Rellene el campo **No.**. y campos **Nombre**.
1. En el campo **Tipo mov.**, elija **Fijo**.
1. En el campo **Tipo de cuenta de destino** , elija **Cuenta L/M** o **Cuenta bancaria**.
1. En el campo **Número de cuenta de destino**, elija la cuenta en la que publicar el valor.
1. Opcional: elija la acción **Dimensiones** y después específique las dimensiones para publicar para la línea.
1. En los campos **Compartir** y **Porcentaje** , especifique cómo distribuir los montos a la cuenta de destino.
  
   > [!TIP]
   > Si ingresa el monto real a asignar para una asignación fija en el campo **Compartir** , el campo **Porcentaje** muestra el porcentaje del importe total.
1. Repita este proceso para cada cuenta que desee incluir en la asignación.

## Utilice un método variable para asignar cantidades

1. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Asignación de cuenta** y luego elija el enlace relacionado.  
1. En la página **Asignación de cuentas**, seleccione la acción **Nuevo**.
1. Rellene el campo **No.**. y campos **Nombre**.
1. En el campo **Tipo mov.**, elija **Variable**.
1. En el campo **Tipo de cuenta de destino**, elija **Cuenta L/M**.
1. En el campo **Número de cuenta de destino**, elija la cuenta en la que publicar el valor.
1. En el campo **Tipo de cuenta de desglose**, elija **Cuenta estadística**.
1. En el campo **Período de cálculo**, elija el período para el cual distribuir los importes.
1. Opcional: para filtrar por valores de dimensiones globales específicos, elija la acción **Filtros de saldo de cuenta desglosado** y luego especifique los valores de filtro.
1. Opcional: elija la acción **Dimensiones** y después específique las dimensiones para publicar para la línea.

## Asignar cantidades sobre la marcha

Cree cuentas de asignación para dividir ingresos y costos para cuentas de mayor y cuentas bancarias. Automatizar la asignación puede ahorrarle mucho tiempo. Sin embargo, si desea utilizar cuentas de asignación, pero no desea crearlas para cada cuenta del L/M, puede ahorrar aún más tiempo.

La opción Heredar del primario le permite utilizar la cuenta de asignación para dividir importes de cualquier cuenta del L/M en una línea de un documento o diario. En el campo **Tipo de cuenta** en un documento o línea de diario, elija una cuenta de L/M y luego elija la cuenta de asignación en el campo **No. de cuenta de asignación**. El monto en la línea se divide para la cuenta del L/M según la configuración en su cuenta de asignación. Es una forma menos transparente de asignación, pero no es necesario crear una cuenta de asignación específicamente para la cuenta del L/M.

Las asignaciones ad hoc son fáciles de configurar. En lugar de especificar un banco o una cuenta de libro mayor en el campo **Tipo de cuenta de destino** en la página **Cuenta de asignación**, elija la opción **Heredar del elemento primario**. Deje el campo **Número de cuenta de destino** en blanco. Cuando elija la cuenta del L/M en el documento o línea del diario, esa cuenta se utiliza para asignar importes.

## Verifique que los montos se distribuyan correctamente antes de publicarlos

Hay un par de formas de verificar que los montos se distribuyan correctamente:

* En la página **Asignación de cuenta**, elija la acción **Probar asignación**. Use el campo **Monto a asignar** para probar diferentes cantidades.
* En la página **Diarios del libro mayor**, elija el diario y utilice la acción **Vista previa de publicación**.

## Ajustar la distribución

Si encuentra algo en una asignación que le gustaría cambiar, puede ajustar la asignación antes de publicarla.  

1. Abra el documento o diario que tiene la asignación que desea cambiar.
1. Seleccione la línea con la asignación y, a continuación, seleccione la acción **Redistribuir asignaciones de cuenta**.
1. En la página **Cambiar asignaciones**, haga su ajuste.

## Publicar una transacción de asignación

Los siguientes pasos describen cómo registrar una transacción de asignación desde un diario general. Los pasos son iguales a todos los documentos de compra y venta.

1. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), introduzca **Diarios generales** y luego elija el enlace relacionado.  
1. Cree una línea nueva. Complete los campos de la misma manera que lo haría con cualquier otro tipo de diario general.
1. Si está utilizando una asignación fija o variable, complete los siguientes campos:
    1. En el campo **Tipo de cuenta**, elija **Cuenta de asignación**.
    1. En el campo **No. de cuenta**, elija la Cuenta de asignación.
1. Si está utilizando una asignación que utiliza la opción Heredar del primario, haga lo siguiente:
    1. En el campo **Tipo de cuenta**, elija **Cuenta de L/M**.
    1. En el campo **No. de cuenta**, elija la cuenta de libro mayor.
    1. En el campo **No. de Cuenta de asignación**, elija la cuenta de asignación que está configurada para usar la opción Heredar del primario. 
1. Elija **Registrar**.

## Consulte también

[Trabajar con diarios generales](ui-work-general-journals.md)  