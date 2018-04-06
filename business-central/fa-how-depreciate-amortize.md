---
title: Depreciar o amortizar activos fijos | Documentos de Microsoft
description: "Debe definir cómo se amortizará o depreciará cada uno de sus activos fijos."
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: write down
ms.date: 06/02/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 8d2d583ca649488f9a506362386a511743ed661b
ms.contentlocale: es-es
ms.lasthandoff: 03/22/2018

---
# <a name="depreciate-or-amortize-fixed-assets"></a>Depreciar o amortizar activos fijos
La amortización se utiliza para distribuir el coste de activos, como maquinaria y equipos, a lo largo de su vida amortizable. Debe definir la amortización de cada activo.  

 Existen dos formas de registrar la amortización:  

* Automática, ejecutando el proceso **Calcular amortización** .  
* Manualmente, con el diario de activos.  

[!INCLUDE[d365fin](includes/d365fin_md.md)] puede calcular la amortización diaria, lo que le permitirá calcular la amortización de cualquier periodo. Podrá analizar los resultados actuales de la operación de forma mensual, trimestral o anual. El cálculo utiliza un año de 360 días y un mes de 30 días estándar. Para obtener más información, consulte [Métodos de amortización](fa-depreciation-methods.md).  

Si varios departamentos usan un activo fijo, la amortización periódica se puede distribuir automáticamente en esos departamentos según una tabla de distribución definida por usuario.  

Puede anular movimientos de amortización incorrectos con el proceso **A/F Anular movs.** Después podrá registrar el importe correcto si vuelve a ejecutar el proceso **Calcular amortización**. Los errores que corrija se registran como movimientos A/F anulados.  

El ajuste de valores se utiliza para ajustar los valores a los cambios de niveles generales de precio. Puede usar el proceso **Ajustar valores activos** para volver a calcular el valor de amortización.  

## <a name="to-calculate-depreciation-automatically"></a>Para calcular la amortización de forma manual
Una vez al mes, o cuando desee, puede ejecutar el proceso **Calcular amortización**. El proceso ignora los activos fijos vendidos, bloqueados o inactivos, o usar el método de amortización manual.  

1. Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Calcular amortización** y, a continuación, seleccione el vínculo relacionado.  
2. Rellene los campos según sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
3. Elija el botón **Aceptar**.  

    El proceso calcula la amortización y crea líneas en el diario general de activos fijos.  
4. Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Diarios generales A/F** y, a continuación, seleccione el vínculo relacionado.  

    En la ventana **A/F Diario general**, en el campo **N. º días amortización** puede ver los días de amortización calculados.  
5. Seleccione la acción **Registrar**.  

## <a name="to-post-depreciation-manually-from-the-fixed-asset-gl-journal"></a>Para registrar una apreciación manualmente desde el diario general de activos fijos
1. Elija el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), especifique **A/F Diario general** y elija el vínculo relacionado.  
2. Cree una línea inicial de diario y rellene los campos según sea necesario.  
3. En el campo **A/F Tipo registro**, seleccione **Amortización**.  
4. Elija la acción **Introducir saldo AF**. Se crea una segunda línea de diario para la cuenta contrapartida que se ha configurado para el registro de amortizaciones. Para obtener más información, vea la sección "Para configurar grupos contables de activos fijos" en [Configurar información general del activo fijo](fa-how-setup-general.md).  
5. En la pestaña **Inicio**, elija **Registrar** para registrar el diario.  

Si configuró las claves de distribución de activos para distribuir importes entre varios departamentos o proyectos, los importes se distribuyen durante el registro. Para obtener más información, consulte [Configurar información general de activos fijos](fa-how-setup-general.md).  

## <a name="to-calculate-allocations-in-the-fixed-asset-gl-journal"></a>Para calcular distribuciones en el diario general de activos
Si se utiliza un activo en varios departamentos, la amortización se puede distribuir automáticamente en esos departamentos según una tabla de distribución definida por usuario.  

1. Elija el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), especifique **A/F Diario general** y elija el vínculo relacionado.  
2. Cree una línea inicial y rellene los campos según sea necesario.
3. En el campo **A/F Tipo registro**, seleccione **Distribución**.  
4. Elija la acción **Introducir saldo AF**. Se crea una segunda línea de diario para la cuenta contrapartida que se ha configurado para el registro de distribuciones.  
5. En la pestaña **Inicio**, elija **Registrar** para registrar el diario.  

## <a name="use-duplication-lists-to-prepare-to-post-to-multiple-depreciation-books"></a>Use las listas de duplicados para preparar el registro a varios libros de amortización
Al rellenar las líneas de diario que se van a registrar en un libro de amortización, puede duplicarlas en un diario independiente para poder efectuar registros en otro libro de amortización. Para obtener más información, vea la sección "Para registrar movimientos en distintos libros de amortización".

1. Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Libros amortización** y, a continuación, seleccione el vínculo relacionado.  
2. Abra el libro de amortización y, a continuación, seleccione la casilla **Compone lista duplicados**.  

> [!IMPORTANT]  
>   Si ha seleccionado el campo **Utiliza lista duplicados**, no utilice números de serie en el diario. La razón es que las series numéricas del diario general de activos no corresponden a las series del diario de activos fijos.  

## <a name="to-post-entries-to-different-depreciation-books"></a>Para registrar movimientos en distintos libros de amortización
1. Elija el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), especifique **A/F Diario general** y elija el vínculo relacionado.  
2. En el diario que desee registrar la amortización, seleccione la casilla **Utilizar lista duplicados**.  
3. Rellene los campos restantes según sea necesario.  
4. Seleccione la acción **Registrar**.  
5. Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **A/F Diarios** y, a continuación, seleccione el vínculo relacionado.  

    > [!NOTE]  
    >   La ventana **Diario activos fijos** contiene nuevas líneas para diferentes libros de amortización según la lista de duplicados.  
6. Revise o edite las líneas y, a continuación, seleccione la acción **Registrar**.  

    > [!NOTE]  
    >   Otra forma de duplicar un movimiento en otro libro es especificar un código de libro de amortización en el campo **Duplicado en libro amort.** al rellenar una línea de diario.  

Puede copiar los movimientos de un libro de amortización a otro usando el proceso **Copiar libro amortización**. El proceso crea líneas de diario en el proceso diario especificado en la ventana **Config. diario activos** para el libro de amortización al que desea copiar. Para obtener más información, consulte el procedimiento siguiente.  

## <a name="to-copy-fixed-asset-ledger-entries-between-depreciation-books"></a>Para copiar los movimientos de activos entre los libros de amortización
1. Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Libros amortización** y, a continuación, seleccione el vínculo relacionado.  
2. Abra la ficha de libro de amortización correspondiente y, a continuación, elija la acción **Copiar libro amortización**.  
3. En la ventana **Copiar libro amortización**, rellene los campos según sea necesario.  
4. Elija el botón **Aceptar**.  

Las líneas copiadas se crean en el diario general de activos o en el de activos fijos, según si el libro de amortización que va a copiar tiene integración con el libro mayor.  

## <a name="see-also"></a>Consulte también
[Activos fijos](fa-manage.md)  
[Configurar activos fijos](fa-setup.md)  
[Finanzas](finance.md)  
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

