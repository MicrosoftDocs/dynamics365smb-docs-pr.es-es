---
title: Administrar presupuestos de activos fijos | Documentos de Microsoft
description: "Puede configurar la información sobre inversiones, ventas/bajas y amortizaciones futuras de activos fijos como ayuda para preparar presupuestos y previsiones."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: forecast
ms.date: 06/02/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 2185a1fc40ddae772e20994f6531b02d7e703e17
ms.contentlocale: es-es
ms.lasthandoff: 07/07/2017


---
# <a name="how-to-manage-budgets-for-fixed-assets"></a>Procedimiento: Gestionar presupuestos de los activos fijos
Puede configurar activos fijos presupuestados. Por ejemplo, esto le permite incluir adquisiciones y ventas anticipadas en los informes.  

Para preparar sus presupuestos de ingresos, presupuestos de cuentas de balance y el presupuesto de caja, necesitará información acerca de las inversiones futuras, ventas/bajas y amortización de activos fijos. Puede obtener esta información desde el informe **A/F - Proyección amort**. Antes de imprimir este informe, debe preparar el presupuesto.  

> [!NOTE]  
>   Esta funcionalidad requiere que la experiencia esté definida en **Conjunto de aplicaciones**. Para obtener más información, consulte [Personalizar la experiencia de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-experiences.md).

## <a name="to-budget-the-acquisition-cost-of-a-fixed-asset"></a>Para presupuestar el coste de un activo
Para preparar presupuestos, necesita configurar fiches de activos para los activos que quiera comprar en el futuro. Los activos fijos presupuestados se configuran como activos normales, pero deben configurarse para que no se registren en el libro mayor.

Al registrar el coste, introduzca el número de activos presupuestados en el campo **A/F N. º pptdo.** . Esto provocará que se registre un coste con signo inverso en el activo presupuestado. Significa que el coste total del activo presupuestado es la diferencia entre el coste presupuestado y el real.

1. Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Activos fijos** y, a continuación, seleccione el vínculo relacionado.
2. Elija la acción **Nuevo** para crear una nueva ficha del activo para el activo presupuestado.
3. Seleccione la casilla **Activo presupuestado** para evitar su registro en el libro mayor.
4. Rellene los campos restantes, asigne un libro de amortización y, a continuación, registre el primer coste con el activo presupuestado especificado en el campo **A/F N. º pptdo.** de la línea del diario. Para obtener más información, vea [Procedimiento: Activos fijos adquiridos](fa-how-acquire.md).

## <a name="to-budget-the-disposal-of-a-fixed-asset"></a>Para presupuestar la venta/baja de un activo fijo
Si desea vender activos en el periodo de presupuesto, puede especificar información acerca del precio y fecha de venta.

1. Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Activos fijos** y, a continuación, seleccione el vínculo relacionado.
2. Seleccione el activo que desee dar de baja o vender y, a continuación, elija la acción **Libros amortización**.
3. En la ventana **Libros amortización A/F**, rellene los campos **Fecha prevista venta/baja** y **Ingresos previstos venta/baja**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-view-projected-disposal-values"></a>Para ver valores venta/baja previstos
Para ver los valores venta/baja previstos y que se calculen las ganancias y pérdidas, puede usar el informe **Proyección de la amortización A/F**.

1. Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Proyección de la amortización A/F** y, a continuación, seleccione el vínculo relacionado.
2. Rellene los campos según sea necesario.
3. Haga clic en el botón **Imprimir** o **Vista previa**.

## <a name="to-budget-depreciation"></a>Para presupuestar amortización
Puede usar el informe **A/F - Proyección amort.** para calcular la amortización futura. El informe muestra el valor neto y la amortización acumulada al principio del periodo seleccionado, los cambios durante el periodo y el valor neto y la amortización acumulada al final del periodo seleccionado.

1. Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Proyección de la amortización A/F** y, a continuación, seleccione el vínculo relacionado.
2. Rellene los campos según sea necesario.
3. Para ver los valores totales de todos los activos, desactive la casilla **Imprimir por activo fijo**.
4. Deje en blanco la ficha desplegable **Activo** para incluir todos los activos. En el campo **Activo presupuestado**, puede especificar **No** para excluir los activos presupuestados o **Sí** para ver solo los activos presupuestados.
5. Haga clic en el botón **Imprimir** o **Vista previa**.

## <a name="see-also"></a>Consulte también
[Activos fijos](fa-manage.md)  
[Configurar activos fijos](fa-setup.md)  
[Finanzas](finance.md)  
[[!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)  
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

