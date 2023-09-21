---
title: Crear informes de análisis
description: 'Describe cómo crear nuevos informes de análisis para ventas, compras y existencias, así como configurar plantillas de análisis.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'bi, power BI, analysis, KPI'
ms.search.form: '555, 556, 557, 558, 9372, 9370, 9371'
ms.date: 09/22/2022
ms.author: bholtorf
---
# Crear informes de análisis

Los directores de ventas necesitan analizar las facturaciones, los ingresos brutos y otros indicadores clave del rendimiento de las ventas con regularidad. Los compradores están más interesados en la dinámica de los volúmenes de compra, las actuaciones de los proveedores y los precios de compra. A su vez, los directores de inventario/logística necesitan información sobre la rotación de inventarios, sobre los análisis de los movimientos de inventario y sobre las estadísticas de valores de inventario. Por lo tanto, no existe un informe de análisis único para todos.

Puede personalizar informes de análisis basados en registros del histórico de transacciones, por ejemplo, ajustes de inventario, transferencias, compras y ventas. En un informe personalizado, los datos de origen, derivados de los movimientos del producto (con los movimientos de valor asociados) se pueden combinar, comparar y presentar de la forma que más convenga al usuario. En este sentido, el informe de análisis es muy similar al informe de tabla dinámica de Microsoft Excel.  

Entonces, por ejemplo, puede crear un informe personalizado que se centre en sus cuentas clave en términos de rotación total de productos en cantidades y cantidades vendidas, ganancia bruta y porcentaje de ganancia bruta durante el mes actual. Luego puede hacer que compare esas cifras con los resultados de meses anteriores o el mismo mes del año pasado y calcule las desviaciones. Todo esto se puede hacer en una sola vista, lo que permite explorar la causa de los problemas identificados e incluso elegir el desplegable para profundizar hasta los detalles del nivel de transacciones individuales.  

El informe de análisis consta de los objetos que desea analizar, como clientes, grupos de clientes, personal de ventas, etc., representados como líneas, y de los parámetros de análisis, que es el modo en que desea analizar los objetos, como cálculos de beneficios, comparaciones periódicas de los volúmenes e importes de ventas y volúmenes o comparaciones periódicas de cifras reales y presupuestadas, representados como columnas. 

Además de informes de análisis, puede crear y ver información similar en vistas de análisis, que se basan en dimensiones. Obtenga más información en [Analizar datos por dimensiones](bi-how-analyze-data-dimension.md).

## Ejemplo

Puede configurar estas líneas (objetos que desea analizar):  

- Equipos  
- Pantallas  
- Piezas repuesto  

Luego puede configurar estas columnas (cómo desea que se analicen los objetos):  

- Ventas del mes actual  
- Ventas del mes anterior  
- Porcentaje de ventas del mes anterior  

## Configuración de plantillas de líneas y columnas

En la página **Informe de análisis**, puede ver distintas plantillas de líneas y columnas que configura en:

* La página **Plantillas líneas de análisis**, donde puede definir el nombre del informe y los objetos que desea mostrar en las líneas del informe y la
* página **Plantillas columnas análisis**, donde define el nombre de la plantilla de columna y los parámetros de análisis que se muestran en el informe como columnas. Cada línea de esta página representa una columna del informe. 

Observe que las líneas de análisis y las columnas de análisis son independientes las unas de las otras.  

Basándose en las líneas y columnas definidas, [!INCLUDE[prod_short](includes/prod_short.md)] agrega el resultado del informe en la página **Informe de análisis**, como se muestra en la siguiente tabla.  

|- |Ventas del mes actual|Ventas del mes anterior|Porcentaje de ventas del mes anterior|  
|-|-|-|-|  
|Equipos| | | |  
|Pantallas| | | |  
|Piezas sueltas| | | |  
|Total| | | |  

Puede, por ejemplo, configurar un grupo de líneas y varios grupos de plantillas de columna para mostrar los informes mensuales y anuales respectivamente.

## Configurar plantillas de columnas de análisis

El procedimiento siguiente se basa en vistas de análisis de ventas. Los pasos son similares para las vistas de análisis de compras y de inventario.

Una plantilla de columna de análisis contiene un conjunto de líneas donde cada una representa una columna de análisis que quiere en el informe de análisis. Para definir una columna debe asignar un código de tipo de análisis a una línea. Este código de tipo de análisis determina el tipo de datos de origen en los movimientos de producto en los que se basa el análisis. Los datos de origen pueden incluir el coste, el importe de ventas, o la cantidad, y sus movimientos de valor asociados. Puede configurar tantas plantillas de columna como desee y luego utilizarlas posteriormente para crear nuevos informes de análisis.    

1. Elija el icono ![Bombilla que abre la característica Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Plantillas de la columna de ventas** y luego elija el enlace relacionado.  
2. Seleccione la primera línea vacía y, a continuación, rellene los campos según sea necesario.
3. Seleccione la acción **Columnas**.  
4. En la página **Columnas de análisis**, rellene los campos para especificar las columnas que desea incluir en el informe de análisis.  

    > [!NOTE]  
    > Para definir una columna, debe rellenar el campo **Código de tipo de análisis** para todos los tipos de columnas excepto las de **Fórmula**. Configure los códigos de tipo de análisis en la página **Tipos de análisis**.  
    
    Además, en el campo **Tipo mov. cont.**, si selecciona **Movs. prods.**, se copian las cifras reales del movimiento del producto. Si selecciona **Movs. ppto. prods.**, se copian las cifras presupuestadas del presupuesto.  
5. Para guardar los cambios, elija **Aceptar**.  

## Configurar plantillas de líneas de análisis

El procedimiento siguiente se basa en informes de análisis para ventas. Los pasos son similares para los informes de análisis de compras y de inventario.

Una plantilla de línea de análisis contiene un conjunto de líneas donde cada una representa una línea de análisis que quiere en el informe de análisis. Una línea puede especificar uno o varios productos, clientes, proveedores o grupos. También puede crear una fórmula en una línea para sumar las otras líneas. Puede configurar tantas plantillas de líneas como desee y utilizarlas después para crear nuevos informes de análisis.   

1. Elija el icono ![Bombilla que abre la característica Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Plantillas de la línea de ventas** y luego elija el enlace relacionado.  
2. Seleccione la primera línea vacía y, a continuación, rellene los campos según sea necesario.
3. Seleccione la acción **Líneas**.  
4. En la página **Línea de análisis**, cree líneas para los productos, los clientes, los proveedores o los vendedores cuyas cifras desee consultar en el informe de análisis. Debe rellenar los campos **Tipo**, **Intervalo** y **Descripción**.  

> [!NOTE]  
> Opcionalmente, para crear muchas líneas individuales para cada producto, cliente, etc., puede seleccionar la opción de inserción adecuada para rellenar todos los campos correspondientes en la línea. Posteriormente, si lo necesita, puede editar las líneas manualmente. Para insertar líneas, elija la acción **Insertar productos** o **Insertar grupos de productos**.  

## Crear un nuevo informe de análisis de ventas

El procedimiento siguiente se basa en informes de análisis para ventas. Los pasos son similares para los informes de análisis de compras y de inventario.

Con los informes de análisis, puede analizar la dinámica de sus ventas según los indicadores de rendimiento de ventas clave, como el volumen de ventas en los importes y cantidades, el margen de contribución o el progreso de venta real respecto al presupuesto. También puede utilizar informes de análisis para analizar los precios medios de venta y para evaluar el rendimiento de ventas de su equipo de ventas.  

1. Elija el icono ![Bombilla que abre la característica Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Informes de análisis de ventas** y luego elija el enlace relacionado.  
2. En la página **Informe de análisis ventas**, elija la acción **Nuevo**.
3. Rellene los campos según sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Elija la acción **Editar informe de análisis**.
5. En la página **Informe de análisis de ventas**, elija la acción **Mostrar matriz**.  

> [!NOTE]  
> La formación de combinaciones de plantillas de línea y de columna para crear informes y la asignación de nombres únicos es opcional. Si lo hace, no necesitará seleccionar plantillas de línea y de columna en la página **Informe de análisis de ventas**. Cuando haya elegido un nombre de informe, puede cambiar las plantillas de línea y de columna independientemente y, más tarde, seleccionar de nuevo el nombre de informe para restaurar la combinación original.

## Consulte también .

[Inteligencia empresarial financiera](bi.md)  
[Finanzas](finance.md)  
[Configurar las finanzas](finance-setup-finance.md)  
[Libro mayor y plan de cuentas](finance-general-ledger.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
