---
title: Analizar importes reales frente a importes presupuestados
description: 'Este artículo describe cómo analizar los importes reales frente a los importes presupuestados como un medio para recopilar, analizar y compartir los datos de su empresa.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'bi, power BI, analysis, KPI'
ms.search.form: '120, 121, 422'
ms.date: 09/14/2022
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# <a name="analyze-actual-amounts-versus-budgeted-amounts"></a>Analizar importes reales frente a importes presupuestados

Como parte de la recopilación, el análisis y el uso compartido de los datos de la empresa, puede ver importes reales comparados con los importes presupuestados para todas las cuentas y durante varios periodos.

Para analizar los importes presupuestados, primero debe crear presupuestos contables (G/L). Obtenga más información en [Crear presupuestos de G/L](finance-how-create-budgets.md).

## <a name="view-a-gl-budget"></a>Ver un presupuesto contable

En un presupuesto con dimensiones, puede filtrar los movimientos y, por lo tanto, ver presupuestos concretos.

1. Elija el icono ![Bombilla que abre la característica Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Presupuestos contables** y luego elija el enlace relacionado.
2. En la página **Presupuestos contables**, abra el presupuesto que desee ver.  
3. En la parte superior de la página rellene los campos según sea necesario para definir lo que se muestra. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!NOTE]  
> Si ha seleccionado **Periodo** en el campo **Muestra como líneas** o **Muestra como columnas**, debe rellenar el campo **Ver por**. Si no ha seleccionado **Periodo** en cualquiera de esos campos,escriba el periodo apropiado en el campo **Filtro fecha**.  

> [!NOTE]  
> Sólo se incluyen en el cálculo los movimientos del presupuesto que incluyan los códigos de filtro que haya introducido en la ficha desplegable **Filtros**. No se incluirán los movimientos de presupuesto que tengan otros códigos de filtro o que no tengan ninguno. Mientras el filtro aparezca en la página, el presupuesto sólo mostrará los movimientos de presupuesto con esos códigos de filtro.  

> [!TIP]  
> Utilizar la acción **Editar presupuesto** para modificar el presupuesto. En la página de presupuesto, elija un importe para ver los movimientos de contabilidad subyacentes.

## <a name="view-actual-and-budgeted-amounts-for-all-accounts"></a>Ver los importes reales y presupuestados de todas las cuentas

Puede ver presupuestos y compararlos con las cifras reales de varias áreas de [!INCLUDE[prod_short](includes/prod_short.md)].

1. Elija el icono ![Bombilla que abre la característica Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Plan de cuentas** y luego elija el vínculo relacionado.  
2. En la página **Plan de cuentas**, seleccione la acción **Saldo/Ppto. cuenta**.
3. En la ficha desplegable **Opciones**, rellene los campos según sea necesario para definir lo que se muestra en la tabla.  
4. Pase el cursor sobre un campo en la tabla para leer una breve descripción sobre la cantidad mostrada.

> [!NOTE]  
> Los filtros que establezca en la cabecera de página se aplicarán a los movimientos de contabilidad y a los movimientos de presupuesto.

Las columnas de la izquierda contienen el plan de cuentas. De las cinco columnas de la derecha, las primeras cuatro muestran los importes del Debe y el Haber reales y presupuestados de cada cuenta. La quinta columna muestra las relaciones proporcionales entre los importes reales y presupuestados de la cuenta.  

> [!TIP]  
> Utilice el campo **Ver por** en la página **Saldo/Ppto. cuenta** seleccionar la longitud del periodo. Utilice el campo **Ver como** para seleccionar el modo de cálculo de los importes, **Saldo periodo** o **Saldo a la fecha**. Elija la acción **Periodo anterior** o **Periodo siguiente** para cambiar el periodo.  

## <a name="to-view-actual-and-budgeted-amounts-for-several-periods"></a>Para ver los importes reales y presupuestados de varios periodos

En lugar de ver los importes reales y presupuestados de todas las cuentas en un único periodo, puede ver varios periodos de una cuenta.  

1. Elija el icono ![Bombilla que abre la característica Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Plan de cuentas** y luego elija el vínculo relacionado.  
2. En la página **Plan de cuentas**, seleccione la cuenta contable relevante y, después, seleccione la acción **Saldo cuenta/Presupuesto**.  
3. En la ficha desplegable **Opciones**, rellene los campos según sea necesario para definir lo que se muestra en la tabla.  
4. En la ficha desplegable **Líneas**, pase el cursor sobre un campo en la tabla para leer una breve descripción sobre la cantidad mostrada.  

## <a name="see-also"></a>Consulte también .

[Inteligencia empresarial financiera](bi.md)  
[Trabajar con informes financieros](bi-how-work-account-schedule.md)  
[Finanzas](finance.md)  
[Configurar las finanzas](finance-setup-finance.md)  
[Libro mayor y plan de cuentas](finance-general-ledger.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
