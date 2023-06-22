---
title: Depreciar o amortizar activos fijos
description: 'Debe definir cómo amortizará o depreciará cada uno de sus activos fijos, como maquinaria y equipo, durante su vida depreciable.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: write down
ms.search.form: '5610, 5611, 5629, 5633, 5659, 5660, 5663, 5619, 5666'
ms.date: 06/15/2021
ms.author: edupont
---
# <a name="depreciate-or-amortize-fixed-assets" />Depreciar o amortizar activos fijos

La amortización se utiliza para distribuir el coste de activos, como maquinaria y equipos, a lo largo de su vida amortizable. Debe definir la amortización de cada activo.  

 Existen dos formas de registrar la amortización:  

* Automática, ejecutando el proceso **Calcular amortización** .  
* Manualmente, con el diario de activos.  

[!INCLUDE[prod_short](includes/prod_short.md)] puede calcular la amortización diaria, lo que le permitirá calcular la amortización de cualquier periodo. Podrá analizar los resultados actuales de la operación de forma mensual, trimestral o anual. El cálculo utiliza un año de 360 días y un mes de 30 días estándar. Para obtener más información, consulte [Métodos de amortización](fa-depreciation-methods.md).  

Si varios departamentos usan un activo fijo, la amortización periódica se puede distribuir automáticamente en esos departamentos según una tabla de distribución definida por usuario.  

Puede anular movimientos de amortización incorrectos con el proceso **A/F Anular movs.** Después podrá registrar el importe correcto si vuelve a ejecutar el proceso **Calcular amortización**. Los errores que corrija se registran como movimientos A/F anulados.  

El ajuste de valores se utiliza para ajustar los valores a los cambios de niveles generales de precio. Puede usar el proceso **Ajustar valores activos** para volver a calcular el valor de amortización.  

## <a name="to-calculate-depreciation-automatically" />Para calcular la amortización de forma manual

Una vez al mes, o cuando desee, puede ejecutar el proceso **Calcular amortización**. El proceso ignora los activos fijos vendidos, bloqueados o inactivos, o usar el método de amortización manual.  

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Calcular amortización** y luego elija el enlace relacionado.  
2. Rellene los campos según sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
3. Elija el botón **Aceptar**.  

    El proceso calcula la amortización y crea líneas en el diario general de activos fijos.

4. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Diarios generales A/F**, y luego elija el enlace relacionado.  

    En la página **A/F Diario general**, en el campo **N.º días amortización** puede ver los días de amortización calculados.  
5. Seleccione la acción **Registrar**.  

> [!NOTE]
> Límite conocido: Si establece el campo **Utilizar forzar nº de días** a Sí y el campo **Forzar nº de días** se establece en un valor donde la **Fecha de registro** menos el **Número de días** da como resultado una fecha del año natural anterior, el sistema no le permitirá registrar la amortización.
> Puede evitarlo si reduce el campo **Forzar nº de días** a no más de los días calculados hasta la fecha de registro usando 30 días/mes O configure la bandera **Ejercicio 365 días** en el libro de amortización.
> Recomendamos la primera opción, ya que es posible que no desee cambiar el uso de 30 días/meses para amortización. Para más información, vea [Amortización de campo Ejercicio 365 días](fa-how-setup-depreciation.md#fiscal-year-365-days-field-depreciation).


## <a name="to-post-depreciation-manually-from-the-fixed-asset-gl-journal" />Para registrar una apreciación manualmente desde el diario general de activos fijos

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **A/F Diario general** y luego elija el enlace relacionado.  
2. Cree una línea inicial de diario y rellene los campos según sea necesario.  
3. En el campo **A/F Tipo registro**, seleccione **Amortización**.  
4. Elija la acción **Introducir saldo AF**. Se crea una segunda línea de diario para la cuenta contrapartida que se ha configurado para el registro de amortizaciones. Para obtener más información, vea [Para configurar los grupos contables de activos fijos](fa-how-setup-general.md#to-set-up-fixed-asset-posting-groups).
5. Elija la acción **Registrar** para registrar el diario.  

El campo **Valor contable** en la página **Ficha activo** se actualiza en consecuencia.

Si configuró las claves de distribución de activos para distribuir importes entre varios departamentos o proyectos, los importes se distribuyen durante el registro. Para obtener más información, consulte [Configurar información general de activos fijos](fa-how-setup-general.md).  

## <a name="to-manage-the-ending-book-value" />Para administrar el valor contable final

En el campo **Valor contable final** en la página **A/F Libro amortización**, puede especificar el valor contable que desea que tenga su activo fijo en el libro de amortización actual después de que se haya amortizado por completo. Puede hacerlo manualmente o puede completar el campo **Valor contable final genérico** en la página **Libro de amortización** relacionada, que luego se utilizará para rellenar automáticamente el campo.

> [!NOTE]
> Si la última amortización hace que el campo **Valor contable** en la página **Ficha activo** sea cero, la última amortización se reduce automáticamente en este importe.<br /><br />
> Si el valor del campo **Valor contable** es superior a cero después de la última amortización debido, por ejemplo, a la existencia de un problema de redondeo o porque hay un valor residual, se ignora el valor del campo **Valor contable final** de la página **Libros amortización A/F**. Para obtener más información, vea [Para registrar el valor residual junto con el coste](fa-how-acquire.md#to-post-the-salvage-value-together-with-the-acquisition-cost).

## <a name="to-calculate-allocations-in-the-fixed-asset-gl-journal" />Para calcular distribuciones en el diario general de activos

Si se utiliza un activo en varios departamentos, la amortización se puede distribuir automáticamente en esos departamentos según una tabla de distribución definida por usuario.  

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **A/F Diario general** y luego elija el enlace relacionado.  
2. Cree una línea inicial y rellene los campos según sea necesario.
3. En el campo **A/F Tipo registro**, seleccione **Distribución**.  
4. Elija la acción **Introducir saldo AF**. Se crea una segunda línea de diario para la cuenta contrapartida que se ha configurado para el registro de distribuciones.  
5. Elija la acción **Registrar** para registrar el diario.  

## <a name="use-duplication-lists-to-prepare-to-post-to-multiple-depreciation-books" />Use las listas de duplicados para preparar el registro a varios libros de amortización

Al rellenar las líneas de diario que se van a registrar en un libro de amortización, puede duplicarlas en un diario independiente para poder efectuar registros en otro libro de amortización. Para obtener más información, vea [Para registrar movimientos en distintos libros de amortización](fa-how-depreciate-amortize.md#to-post-entries-to-different-depreciation-books).

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Libros amortización** y luego elija el enlace relacionado.  
2. Abra el libro de amortización y, a continuación, seleccione la casilla **Compone lista duplicados**.  

> [!IMPORTANT]  
>   Si ha seleccionado el campo **Utiliza lista duplicados**, no utilice números de serie en el diario. La razón es que las series numéricas del diario general de activos no corresponden a las series del diario de activos fijos.  

## <a name="to-post-entries-to-different-depreciation-books" />Para registrar movimientos en distintos libros de amortización

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **A/F Diario general** y luego elija el enlace relacionado.  
2. En el diario que desee registrar la amortización, seleccione la casilla **Utilizar lista duplicados**.  
3. Rellene los campos restantes según sea necesario.  
4. Seleccione la acción **Registrar**.  
5. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **A/F Diarios**, y luego elija el enlace relacionado.  

    > [!NOTE]  
    >   La página **Diario activos fijos** contiene nuevas líneas para diferentes libros de amortización según la lista de duplicados.  
6. Revise o edite las líneas y, a continuación, seleccione la acción **Registrar**.  

    > [!NOTE]  
    >   Otra forma de duplicar un movimiento en otro libro es especificar un código de libro de amortización en el campo **Duplicado en libro amort.** al rellenar una línea de diario.  

Puede copiar los movimientos de un libro de amortización a otro usando el proceso **Copiar libro amortización**. El proceso crea líneas de diario en el proceso diario especificado en la página **Config. diario activos** para el libro de amortización al que desea copiar. Para obtener más información, consulte el procedimiento siguiente.  

## <a name="to-copy-fixed-asset-ledger-entries-between-depreciation-books" />Para copiar los movimientos de activos entre los libros de amortización

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Libros amortización** y luego elija el enlace relacionado.  
2. Abra la ficha de libro de amortización correspondiente y, a continuación, elija la acción **Copiar libro amortización**.  
3. En la página **Copiar libro amortización**, rellene los campos según sea necesario.  
4. Elija el botón **Aceptar**.  

Las líneas copiadas se crean en el diario general de activos o en el de activos fijos, según si el libro de amortización que va a copiar tiene integración con el libro mayor.  

## <a name="see-related-microsoft-trainingtrainingmodulescalculate-post-depreciations" />Consultar la [formación de Microsoft](/training/modules/calculate-post-depreciations/) relacionada

## <a name="see-also" />Consulte también .

[Activos fijos](fa-manage.md)  
[Configuración de activos fijos](fa-setup.md)  
[Finanzas](finance.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
