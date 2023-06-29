---
title: Analizar datos por dimensiones
description: Este artículo describe cómo puede analizar los datos comerciales por dimensiones para obtener una mayor comprensión de su negocio.
author: edupont
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'bi, power BI, analysis, KPI'
ms.search.form: '545, 555, 556, 557, 558, 9372, 9370, 9371'
ms.date: 09/22/2022
ms.author: edupont
---
# <a name="analyze-data-by-dimensions"></a><a name="analyze-data-by-dimensions"></a><a name="analyze-data-by-dimensions"></a>Analizar datos por dimensiones

En análisis financiero, una dimensión son datos que agrega a un movimiento como una especie de marcador. Estos datos se utilizan para agrupar movimientos de características similares, como clientes, regiones, productos y vendedor, y así poder recuperar con facilidad estos grupos para su análisis. Las dimensiones se pueden utilizar en movimientos de diarios, documentos y presupuestos. 

Cada "dimensión" describe el foco del análisis. Así, un análisis de dos dimensiones, por ejemplo, sería ventas por área. Mediante el uso de más de dos dimensiones al crear un movimiento, puede efectuar un análisis más complejo, como ventas por campaña de ventas, grupo de clientes y área. Esto le proporciona una mejor perspectiva de su empresa, para así poder evaluar la información, como el desempeño de la empresa, dónde destaca y dónde no, y dónde se deberían asignar más recursos, de modo que pueda tomar decisones más informadas y avanzar. Obtenga más información en [Trabajar con dimensiones](finance-dimensions.md).

> [!TIP]
> Como una forma rápida de analizar datos transaccionales por dimensiones, puede filtrar por dimensiones los totales del plan de cuentas (COA) y movimientos en todas las páginas **Movimientos**. Busque la acción **Establecer filtro de dimensiones**.

> [!NOTE]
> Si descubre que se ha usado un valor de dimensión incorrecto en los movimientos de contabilidad, puede corregirlo y actualizar sus vistas de análisis. Más información en la sección [Solucionar problemas y corregir dimensiones](finance-troubleshooting-correcting-dimensions.md#changing-dimension-assignments-after-posting).

## <a name="set-up-an-analysis-view"></a><a name="set-up-an-analysis-view"></a><a name="set-up-an-analysis-view"></a>Configurar una vista de análisis

Los análisis por dimensiones usan una combinación seleccionada de dimensiones. Almacene, recupere y actualice ese conjunto de dimensiones creando una tarjeta **Vista de análisis**. 

1. Elija el icono ![Bombilla que abre la característica Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Vistas de análisis**, y luego elija el enlace relacionado.  
2. En la página **Lista vista de análisis**, elija la acción **Nuevo**.
3. Rellene los campos según sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Para agregar otros códigos de dimensión además de los cuatro de la ficha desplegable **Dimensiones**, elija la acción **Filtro**, rellene los campos y, a continuación, elija el botón **Aceptar**.  
5. Para actualizar la vista, elija la acción **Actualizar**.

## <a name="analyze-by-dimensions"></a><a name="analyze-by-dimensions"></a><a name="analyze-by-dimensions"></a>Analizar por dimensiones

Utilizar vistas de análisis que ya ha configurado con la matriz **Análisis por dimensiones** para consultar los importes de la contabilidad.   

1. Elija el icono ![Bombilla que abre la característica Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Vistas de análisis**, y luego elija el enlace relacionado.  
2. Seleccione la vista de análisis relevante y, a continuación, elija la acción **Análisis por dimensiones**.
3. En la página **Análisis por dimensiones** rellene los campos para definir qué datos se muestran y cómo.
4. Seleccione la acción **Mostrar matriz** para abrir la página de la matriz correspondiente de la vista de análisis definida.
5. Para ver una especificación de un importe que se muestra en la página, elija el importe que se desglosará.  

- Las columnas de la izquierda contienen información basada en lo que haya seleccionado en el campo **Muestra como líneas** de la cabecera.  
- Las columnas de la derecha contienen información basada en los elementos seleccionados en el campo **Muestra como columnas** del encabezado.

> [!IMPORTANT]  
> No se puede seleccionar una longitud de periodo inferior al periodo especificado para la **Vista de análisis** en la ficha Vista de análisis. Los comandos **Conjunto siguiente** y **Conjunto anterior** están inactivos si ha seleccionado **Periodo** en el campo **Muestra como líneas** o **Muestra como columnas**.  

> [!NOTE]  
> Puede utilizar el informe **Dimensiones - Detalles** para mostrar una clasificación detallada de cómo se han utilizado las dimensiones en los movimientos durante un periodo seleccionado. Puede utilizar el informe **Dimensiones - Total** para mostrar sólo los importes totales.  

> [!TIP]  
> También puede modificar la vista cambiando el contenido de los campos **Muestra como líneas** y **Muestra como columnas**. Para revertir una configuración de vista, elija la acción **Invertir líneas y columnas**.

## <a name="update-an-analysis-view"></a><a name="update-an-analysis-view"></a><a name="update-an-analysis-view"></a>Actualizar una vista de análisis

Los importes que se muestran en la página **Análisis por dimensiones** le ofrecen una imagen del estado de la empresa en el momento de la última actualización. Para obtener una imagen del estado actual, debe actualizar la vista de análisis mediante la ejecución de la función de actualización.

Use el siguiente procedimiento para actualizar una vista de análisis desde la página **Análisis por dimensiones**. Los pasos son parecidos a los de actualizar las páginas **Ficha vista de análisis** y **Lista vista de análisis**.  

1. Elija el icono ![Bombilla que abre la característica Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Vistas de análisis**, y luego elija el enlace relacionado.
2. Seleccione la vista de análisis relevante y, a continuación, elija la acción **Análisis por dimensiones**.
3. En la página **Análisis por dimensiones**, elija el campo **Cód. vista análisis**.  
4. Seleccione la línea con la vista de análisis relevante.  
5. En la página **Vistas de análisis**, seleccione la vista de análisis y, a continuación, la acción **Actualizar**.  

> [!TIP]  
> Si selecciona la casilla **Actualizar al registrar** en una ficha de vista de análisis, la vista se actualiza automáticamente cuando se registra una transacción asociada.

> [!NOTE]  
> Para actualizar varias vistas de análisis al mismo tiempo, debe utilizar el proceso **Actualizar vistas de análisis**.  

## <a name="see-related-training-at-microsoft-learn"></a><a name="see-related-training-at-microsoft-learn"></a><a name="see-related-training-at-microsoft-learn"></a>Consulte la formación relacionada en [Microsoft Learn](/learn/modules/dimensions-financial-reports-dynamics-365-business-central/index)

## <a name="see-also"></a><a name="see-also"></a><a name="see-also"></a>Consulte también .

[Inteligencia empresarial financiera](bi.md)  
[Finanzas](finance.md)  
[Configurar las finanzas](finance-setup-finance.md)  
[Libro mayor y plan de cuentas](finance-general-ledger.md)  
[Trabajar con dimensiones](finance-dimensions.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
