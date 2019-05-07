---
title: Analizar datos por dimensiones | Documentos de Microsoft
description: Describe cómo analizar varios datos empresariales por dimensiones.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: bi, power BI, analysis, KPI
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: 59624b1308d8a8d4fda78d440a48d4138a687691
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 03/31/2019
ms.locfileid: "932580"
---
#  <a name="analyze-data-by-dimensions"></a>Analizar datos por dimensiones
En análisis financiero, una dimensión son datos que puede agregar a un movimiento como una especie de marcador. Estos datos se utilizan para agrupar movimientos de características similares, como clientes, regiones, productos y vendedor, y así poder recuperar con facilidad estos grupos para su análisis. Las dimensiones se pueden utilizar en movimientos de diarios, documentos y presupuestos. El término dimensión describe cómo tiene lugar el análisis. Un análisis de dos dimensiones, por ejemplo, sería ventas por área. Sin embargo, mediante el uso de más de dos dimensiones al crear un movimiento, puede efectuar un análisis más complejo, como ventas por campaña de ventas, grupo de clientes y área. Para obtener más información, consulte [Trabajar con dimensiones](finance-dimensions.md).

Analizar datos por dimensiones le proporciona una mejor perspectiva de su empresa, para así poder evaluar la información, como el desempeño de la empresa, dónde destaca y dónde no, y dónde se deberían asignar más recursos.

> [!TIP]
> Como una forma rápida de analizar datos transaccionales por dimensiones, puede filtrar por dimensiones los totales del plan de cuentas y movimientos en todas las páginas **Movimientos**. Busque la acción **Establecer filtro de dimensiones**.

## <a name="to-set-up-an-analysis-view"></a>Para configurar una vista de análisis  
Los análisis por dimensiones muestran una combinación seleccionada de dimensiones. Puede almacenar y recuperar cada análisis que haya configurado. La información de configuración de un análisis se guarda en una ficha **Vista de análisis** para simplificar futuros análisis.  

1. Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Vistas de análisis** y luego elija el enlace relacionado.  
2. En la página **Lista vista de análisis**, elija la acción **Nuevo**.
3. Rellene los campos según sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Para agregar otros códigos de dimensión además de los cuatro de la ficha desplegable **Dimensiones**, elija la acción **Filtro**, rellene los campos y, a continuación, elija el botón **Aceptar**.  
5. Para actualizar la vista, elija la acción **Actualizar**.

## <a name="to-analyze-by-dimensions"></a>Para analizar por dimensiones
Puede utilizar la matriz **Análisis por dimensiones** para consultar los importes de la contabilidad mediante las vistas de análisis que haya configurado. Rellene la página **Análisis por dimensiones** para definir lo que se mostrará en la matriz y, a continuación, elija la acción **Mostrar matriz** para ver la matriz.  

1. Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Vistas de análisis** y luego elija el enlace relacionado.  
2. Seleccione la vista de análisis relevante y, a continuación, elija la acción **Análisis por dimensiones**.
3. En la página **Análisis por dimensiones** rellene los campos para definir qué datos se muestran y cómo.
4. Seleccione la acción **Mostrar matriz** para abrir la página de la matriz correspondiente de la vista de análisis definida.
5. Para ver una especificación de un importe que se muestra en la página, elija el importe que se desglosará.  

- Las columnas de la izquierda contienen información basada en lo que haya seleccionado en el campo **Muestra como líneas** de la cabecera.  
- Las columnas de la derecha contienen información basada en los elementos seleccionados en el campo **Muestra como columnas** del encabezado.

> [!IMPORTANT]  
>   No se puede seleccionar una longitud de periodo inferior al periodo especificado para la **Vista de análisis** en la ficha Vista de análisis. Los comandos **Conjunto siguiente** y **Conjunto anterior** están inactivos si ha seleccionado **Periodo** en el campo **Muestra como líneas** o **Muestra como columnas**.  

> [!NOTE]  
>   Puede utilizar el informe **Dimensiones - Detalles** para mostrar una clasificación detallada de cómo se han utilizado las dimensiones en los movimientos durante un periodo seleccionado. Puede utilizar el informe **Dimensiones - Total** para mostrar sólo los importes totales.  

> [!TIP]  
>   También puede modificar la vista cambiando el contenido del campo **Muestra como líneas** y del campo **Muestra como columnas**. Para revertir una configuración de vista, elija la acción **Invertir líneas y columnas**.

## <a name="to-update-an-analysis-view"></a>Para actualizar una vista de análisis  
Los importes que aparecen en la página **Análisis por dimensiones** le ofrecen una imagen del estado de la empresa en el momento de la última actualización. Para obtener una imagen del estado actual, debe actualizar la vista de análisis mediante la ejecución de la función de actualización.

El siguiente procedimiento permite actualizar una vista de análisis desde la página **Análisis por dimensiones**. Los pasos son parecidos desde las páginas **Ficha vista de análisis** y **Lista vista de análisis**.  

1. Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Vistas de análisis** y luego elija el enlace relacionado.
2. Seleccione la vista de análisis relevante y, a continuación, elija la acción **Análisis por dimensiones**.
2. En la página **Análisis por dimensiones**, elija el campo **Cód. vista análisis**.  
3. Seleccione la línea con la vista de análisis relevante.  
4. En la página **Vistas de análisis**, seleccione la vista de análisis y, a continuación, la acción **Actualizar**.  

> [!TIP]  
>   Si selecciona la casilla **Actualizar al registrar** en una ficha de vista de análisis, la vista se actualiza automáticamente cuando se registra una transacción implicada.

> [!NOTE]  
>   Para actualizar varias vistas de análisis al mismo tiempo, debe utilizar el proceso **Actualizar vistas de análisis**.  

## <a name="see-also"></a>Consulte también
[Inteligencia empresarial](bi.md)  
[Finanzas](finance.md)  
[Configurar las finanzas](finance-setup-finance.md)  
[Libro mayor y plan de cuentas](finance-general-ledger.md)  
[Trabajar con dimensiones](finance-dimensions.md)  
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
