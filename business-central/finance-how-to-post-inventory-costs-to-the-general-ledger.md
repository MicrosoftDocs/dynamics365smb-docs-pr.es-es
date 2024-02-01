---
title: Conciliar costes de inventario con la contabilidad general
description: 'Al finalizar el periodo contable, se llevan a cabo una serie de tareas de control y auditoría de costes con el fin de generar informes correctos y compensados del valor de las existencias.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'warehouse, stock'
ms.search.form: 9297
ms.date: 06/16/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# Conciliar costes de inventario con la contabilidad general

Cuando registra transacciones del inventario, como los envíos de ventas, los albaranes de compra o los ajustes de inventario, los costes de producto cambiados se registran en movimientos de valor de productos. Para reflejar este cambio de valor de inventario en sus libros de finanzas, los costes de inventario se registran automáticamente en las cuentas de inventario relacionadas del libro mayor. Para cada una de las transacciones de inventario que registre, los valores apropiados se contabilizan en la cuenta de inventario, en la cuenta de ajuste y en la cuenta de CV en el módulo de contabilidad.

La contabilización automática de costes se define en el campo **Contabilización automática de costes** en la página **Configuración existencias**.

Aunque se hayan registrado los costes de inventario automáticamente en el libro mayor, seguirá siendo necesario asegurarse de que los costes de los bienes se dirigen a las transacciones de venta de salida relacionadas, especialmente en situaciones donde la venta de bienes se factura antes de la compra de estos bienes. Esto se denomina ajuste de costes. Los costes de los productos se ajustan automáticamente cada vez que registra transacciones de producto, pero también puede ajustar los costes de producto manualmente. Para obtener más información, consulte [Modificar precios de productos](inventory-how-adjust-item-costs.md).

## Para registrar los costes de inventario de forma manual

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Regis. variación existencias**, y luego elija el enlace relacionado.
2. Puede registrar manualmente los costes de inventario en el módulo de contabilidad, si ejecuta el trabajo por lotes. Cuando lo ejecute, se crearán los movimientos de contabilidad según los movimientos de valoración. Es posible registrar los movimientos de forma que estén agrupados por grupos contables.

> [!NOTE]  
> Cuando lo ejecute, es posible que encuentre errores porque faltan datos en la configuración o porque la configuración de dimensión no es compatible. Si el proceso encuentra errores relacionados con la configuración de dimensión, omitirá dichos errores y utilizará las dimensiones del movimiento de valor. Para el resto de errores, el proceso omitirá registrar los movimientos de valores y mostrará una lista de ellos al final del informe, en una sección llamada “Movimientos omitidos”. Para registrar dichos movimientos, deberá primeramente arreglar las causas de los errores.

Para ver una lista con los errores antes de ejecutar el proceso de registro, puede ejecutar el informe **Reg. var. ex. en cont. - Test**. El informe de test muestra un listado con todos los errores encontrados durante un proceso de registro de prueba. A continuación, puede solucionar dichos errores y ejecutar el proceso de registro de costes sin que se omita ningún movimiento.

Si simplemente desea obtener una visión general acerca de qué valores se podrán registrar en el módulo de contabilidad sin que realmente se registren, puede ejecutar el proceso **Regis. variación existencias** sin que se registren los valores en el módulo de contabilidad. Para ello, deberá quitar la marca de verificación del campo **Registrar** en la página de solicitud. De esta forma, cuando ejecute el trabajo por lotes, se genera un informe que muestra los valores que están preparados para ser registrados en el módulo de contabilidad, pero no se registran.

## Auditar la reconciliación entre la contabilidad de inventario y la contabilidad general
La página **Invent. - Conciliación cont.** proporciona lo siguiente:

- Muestra las diferencias de conciliación al comparar los movimientos registrados en la contabilidad general y los movimientos de inventario (movimientos de valoración).
- Muestra los importes de costes no conciliados en los movimientos de valoración del inventario como si estuvieran asignados a cuentas relacionadas con el inventario correspondiente de la contabilidad y los compara con los totales registrados en las mismas cuentas de contabilidad.
- Refleja la doble estructura de movimientos de contabilidad presentando visualmente los datos como tales. Por ejemplo, un movimiento de CV se corresponde con un movimiento de inventario.
- Permite a los usuarios ver la información desglosada y consultar los movimientos que conforman los importes de costes.
- Incluye filtros para limitar el análisis por fecha, producto y ubicación.
- Explica los motivos de las diferencias de conciliación en mensajes informativos.


La columna **Nombre** situada a la izquierda de la cuadrícula muestra los distintos tipos de cuentas asociadas al inventario.

Las columnas **Inventario**, **Inventario (provisional)** e **Inventario WIP** muestran los totales facturados, no facturados y WIP de cada tipo de cuenta. Estos totales se calculan a partir de los movimientos de valoración, es decir, se proyectan en los tipos de cuentas en los que finalizarán cuando se registran finalmente en la contabilidad.

La columna **Total** muestra la suma (en negrita) de los importes de movimientos de valorización en las tres columnas de inventario.

La columna **Total C/G** muestra los importes (en negrita) de cada tipo de cuenta que existe en la contabilidad. Estos importes se calculan a partir de los movimientos de contabilidad, es decir, representan costes de inventario ya registrados en la contabilidad.

La columna **Diferencia** representa la diferencia entre el valor de los campos **Total C/G** y **Total**.

En la parte superior de la página **Invent. - Conciliación cont.**, puede introducir filtros para limitar, por ejemplo, el periodo de tiempo durante el que desea visualizar la información.

Si selecciona la casilla de verificación **Mostrar advertencia**, y existen discrepancias entre los totales del inventario y los totales de contabilidad, la aplicación mostrará mensajes en el campo **Advertencia** de la matriz en los que se explican dichas discrepancias. Si selecciona el campo advertencia, la aplicación mostrará más información acerca del significado de las advertencias.

Cuando haya introducido todos los filtros pertinentes, seleccione la acción **Mostrar matriz**. Se calcularán los datos y aparecerá la página de matriz.

En la columna más a la izquierda de la matriz puede ver los diferentes tipos de cuentas de contabilidad que están asociadas al inventario. La matriz mostrará los totales del inventario facturados, no facturados y WIP para cada uno de esos tipos. Esos totales se calculan a partir de los movimientos de valoración.

Las columnas siguientes muestran los totales para los mismos tipos de cuenta que se calcularon a partir de los los movimientos de contabilidad.

Elija el importe que se encuentra en cualquiera de los campos de totalización para ver los movimientos de informe del inventario que se utilizaron para calcular los totales. Para los totales del inventario, los movimientos de informe del inventario se corresponden con las sumas de los movimientos de valoración para los productos. En el caso de los totales de contabilidad, los movimientos de informe del inventario se corresponden con las sumas de los movimientos.

## Creación de informes de costes y conciliación con la contabilidad
Otros informes, funciones de seguimiento y una herramienta de conciliación especial están disponibles para el auditor o controlador responsable de informar un valor de inventario correcto y equilibrado al departamento de finanzas.

La siguiente tabla los describe.    

|**Para**|**Vea**|  
|------------|-------------|  
|Ver el valor en inventario de los productos seleccionados, incluida información acerca de las cantidades y valores de aumentos y disminuciones en inventario a lo largo de un periodo seleccionado.|Informe **Valorización de inventario**|  
|Ver el valor en inventario de órdenes de producción en el inventario WIP (productos semiterminados), como cantidades y valores de consumo, uso de capacidad y salida en órdenes de producción en curso.|Informe **Valorización de inventario - WIP**|  
|Ver el valor en inventario de los productos seleccionados, incluido su coste real y esperado en la fecha especificada.|Informe **Valorac. exist.-especif. coste**|  
|Usar un informe para analizar los motivos de las evoluciones de los costes o conocer las partes de costes de los productos vendidos (CV).|Informe **Análisis partes costes**|  

## Consulte también  
[Gestión de costes de inventario](finance-manage-inventory-costs.md)  
[Compras](purchasing-manage-purchasing.md)  
[Ventas](sales-manage-sales.md)    
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Funciones empresariales generales](ui-across-business-areas.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]