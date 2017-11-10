---
title: "Crear informes de análisis | Documentos de Microsoft"
description: "Describe cómo crear nuevos informes de análisis para ventas, compras y existencias, así como configurar plantillas de análisis."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: bi, power BI, analysis, KPI
ms.date: 06/16/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: eea34afbee429d14ab150894729cb4ea3843bb2b
ms.openlocfilehash: b96ff2d1f4339b137a6f7d2c2c1266185e2dc69c
ms.contentlocale: es-es
ms.lasthandoff: 09/22/2017

---
#  <a name="how-to-create-analysis-reports"></a>Crear informes de análisis
Los directores de ventas necesitan analizar las facturaciones, los ingresos brutos y otros indicadores clave del rendimiento de las ventas con regularidad. Los compradores están más interesados en la dinámica de los volúmenes de compra, las actuaciones de los proveedores y los precios de compra. A su vez, los directores de inventario/logística necesitan información sobre la rotación de inventarios, sobre los análisis de los movimientos de inventario y sobre las estadísticas de valores de inventario.  

Puede utilizar informes de análisis para crear informes personalizados basados en registros del histórico de transacciones, por ejemplo, ajustes de inventario, transferencias, compras y ventas. En un informe personalizado, los datos de origen, derivados de los movimientos del producto (con los movimientos de valor asociados) se pueden combinar, comparar y presentar de la forma que más convenga al usuario. En este sentido, el informe de análisis es muy similar al informe de tabla dinámica de Microsoft Excel.  

Puede crear un informe personalizado que se centre en las cuentas clave, analizando los importes y las cantidades vendidos y los beneficios brutos y los porcentajes de beneficios brutos del mes actual, y comparando estas cifras con los resultados del mes anterior o con los del mismo mes del año anterior, calculando las desviaciones. Todo esto se puede hacer en una sola vista, con la posibilidad de explorar la causa de los problemas identificados eligiendo el botón desplegable para acceder a los detalles del nivel de transacciones individuales.  

El informe de análisis consta de los objetos que desea analizar, como clientes, grupos de clientes, personal de ventas, etc., representados como líneas, y de los parámetros de análisis, es decir, el modo en que desea analizar los objetos, representados como columnas, como cálculos de beneficios, comparaciones periódicas de los volúmenes e importes de ventas y volúmenes o comparaciones periódicas de cifras reales y presupuestadas.

Además de informes de análisis, puede crear y ver información similar en vistas de análisis, que se basan en dimensiones. Para obtener más información, vea [Analizar datos por dimensiones](bi-how-analyze-data-dimension.md).

## <a name="example"></a>Ejemplo  
Puede configurar líneas como las siguientes:  
- Equipos  
- Pantallas  
- Piezas sueltas  

A continuación, puede configurar las siguientes columnas:  

- Ventas del mes actual  
- Ventas del mes anterior  
- Porcentaje de ventas del mes anterior  

> [!NOTE]  
>   Esta funcionalidad requiere que la experiencia esté definida en **Suite**. Para obtener más información, consulte [Personalizar la experiencia de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-experiences.md).

## <a name="setting-up-line-and-column-layouts"></a>Configuración de plantillas de líneas y columnas  
 En la ventana **Informe de análisis**, puede ver distintas plantillas de líneas y columnas según la configuración definida. Las líneas o las plantillas de línea, se configuran en la ventana **Plantilla de línea de análisis**. En esta ventana puede definir el nombre del informe y los objetos que desea mostrar en las líneas del informe. Las columnas se configuran en la ventana **Plantillas columnas análisis**. En esta ventana puede definir el nombre de la plantilla de columna y los parámetros de análisis que desea mostrar en el informe como columnas. En la ventana **Plantillas columnas análisis**, cada línea representa una columna del informe. Observe que las líneas de análisis y las columnas de análisis son independientes las unas de las otras.  

Basándose en las líneas y columnas definidas, el programa agregará el resultado del informe en la ventana de matriz **Informe de análisis**, como en este ejemplo:  

| |Ventas del mes actual|Ventas del mes anterior|Porcentaje de ventas del mes anterior|  
|-|-|-|-|  
|Equipos| | | |  
|Pantallas| | | |  
|Piezas sueltas| | | |  
|Total| | | |  

 Puede, por ejemplo, configurar un conjunto de líneas y varios conjuntos de plantillas de columna para mostrar los informes mensuales y anuales respectivamente.

 ## <a name="to-set-up-analysis-column-templates"></a>Para configurar plantillas de columnas de análisis
El procedimiento siguiente se basa en vistas de análisis para ventas. Los pasos son similares para las vistas de análisis de compras y de inventario.

En un informe de análisis, los parámetros de análisis se muestran como columnas. Puede definir las columnas que desea incluir en el informe de análisis configurando plantillas de columnas de análisis.  

Una plantilla contiene un conjunto de líneas que representan las columnas de análisis que se ven en el informe de análisis. Para definir una columna debe asignar un código de tipo de análisis a una línea. Este código de tipo de análisis determina el tipo de datos de origen en los movimientos de producto en los que se basa el análisis. Los datos de origen incluyen el coste, el importe de ventas, o la cantidad, y sus movimientos de valor asociados. Puede configurar tantas plantillas de columna como desee y utilizarlas posteriormente para crear nuevos informes de análisis.    

1. Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Plantillas de la columna de ventas** y, a continuación, seleccione el vínculo relacionado.  
2. Seleccione la primera línea vacía y, a continuación, rellene los campos según sea necesario.
3. Seleccione la acción **Columnas**.  
4. En la ventana **Columnas de análisis**, rellene los campos para especificar las columnas que desea incluir en el informe de análisis.  

    > [!NOTE]  
>   Para definir una columna, debe rellenar el campo **Código de tipo de análisis** para todos los tipos de columnas excepto las de **Fórmula**. Configure los códigos de tipo de análisis en la ventana **Tipos de análisis**.  

    **Nota**. En el campo **Tipo mov. cont.**, si selecciona **Movs. prods.** se copian las cifras reales del movimiento del producto. Si selecciona **Movs. ppto. prods.**, se copian las cifras presupuestadas del presupuesto.  
5.  Elija el botón **Aceptar** para guardar los cambios.  

## <a name="to-set-up-analysis-line-templates"></a>Para configurar plantillas de líneas de análisis  
El procedimiento siguiente se basa en informes de análisis para ventas. Los pasos son similares para los informes de análisis de compras y de inventario.

En un informe de análisis los objetos de análisis se muestran en líneas. Puede definir las líneas que desee incluir en el informe de análisis configurando plantillas de líneas de análisis.  

Una plantilla contiene un conjunto de líneas que representan las líneas de análisis que se ven en el informe de análisis. Una línea puede especificar uno o varios productos, clientes, proveedores o grupos. También puede crear una fórmula en una línea para sumar las otras líneas. Puede configurar tantas plantillas de líneas como desee y utilizarlas después para crear nuevos informes de análisis.    

1. Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Plantillas de las líneas de ventas** y, a continuación, seleccione el vínculo relacionado.  
2. Seleccione la primera línea vacía y, a continuación, rellene los campos según sea necesario.
3. Seleccione la acción **Líneas**.  
4. En la ventana **Línea de análisis**, cree líneas para los productos, los clientes, los proveedores o los vendedores cuyas cifras desee consultar en el informe de análisis. Debe rellenar los campos **Tipo**, **Intervalo** y **Descripción**.  

> [!NOTE]  
>   Opcionalmente, si desea crear muchas líneas individuales para cada producto, cliente, etc., puede seleccionar la opción de inserción adecuada para rellenar todos los campos correspondientes en la línea. Posteriormente, si lo necesita, puede editar las líneas manualmente. Para insertar líneas, elija la acción **Insertar productos** o la acción **Insertar grupos de productos**.  

## <a name="to-create-a-new-sales-analysis-report"></a>Para crear un nuevo informe de análisis de ventas
El procedimiento siguiente se basa en informes de análisis para ventas. Los pasos son similares para los informes de análisis de compras y de inventario.

Utilice los informes de análisis para analizar la dinámica de sus ventas según los indicadores de rendimiento de ventas clave que se seleccionen, por ejemplo, el volumen de ventas en los importes y cantidades, el margen de contribución o el progreso de venta real respecto al presupuesto. También puede utilizar el informe para analizar los precios medios de venta y para evaluar el rendimiento de ventas de su equipo de ventas.  

1. Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Informes de análisis de ventas** y, a continuación, seleccione el vínculo relacionado.  
2. En la ventana **Informe de análisis ventas**, elija la acción **Nuevo**.
3. Rellene los campos según sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Elija la acción **Editar informe de análisis**.
5. En la ventana **Informe de análisis de ventas**, elija la acción **Mostrar matriz**.  

> [!NOTE]  
>   La formación de combinaciones de plantillas de línea y de columna para crear informes y la asignación de nombres únicos es opcional. Si lo hace, la selección de un nombre de informe implica que no tendrá que seleccionar plantillas de línea y de columna en la ventana **Informe de análisis de ventas**. Cuando haya elegido un nombre de informe, puede cambiar las plantillas de línea y de columna independientemente y, más tarde, seleccionar de nuevo el nombre de informe para restaurar la combinación original.

## <a name="see-also"></a>Consulte también
[Inteligencia empresarial](bi.md)  
[Finanzas](finance.md)  
[Configurar las finanzas](finance-setup-finance.md)  
[Libro mayor y plan de cuentas](finance-general-ledger.md)  
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

