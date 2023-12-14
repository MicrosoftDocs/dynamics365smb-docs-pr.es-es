---
title: Fecha registro en movimientos de valores
description: Aprender cómo el proceso Valorar stock - movs. producto identifica y asigna una fecha de registro a los movimientos de valor que creará.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 09/17/2021
ms.author: bholtorf
---
# Detalles de diseño: Fecha registro en el movimiento de valor de ajuste

Este artículo proporciona orientación para los usuarios de la función de cálculo de costes de inventario en [!INCLUDE[prod_short](includes/prod_short.md)], y en particular de cómo el trabajo por lotes **Ajustar coste: movimientos de producto** identifica y asigna una fecha de registro a los registros de valor que el trabajo por lotes está a punto de crear.

## Cómo se asignan las fechas de registro

El proceso **Valorar stock - movs. producto** asigna una fecha de registro al movimiento de valor que creará en los pasos siguientes:  

1. Inicialmente, la fecha de registro del movimiento que se creará es la misma que la del movimiento que ajusta.  

2. La fecha de registro se valida con Periodos de inventario o Configuración de contabilidad.  

3. Asignación de la fecha de registro; si la fecha inicial no se encuentra dentro del rango de fechas permitidas, el proceso asignará una Fecha de registro permitida en la Configuración de contabilidad o en el Período de inventario. Si en la Configuración de contabilidad se definen tanto los Períodos de inventario como las fechas de registro permitidas, se asignará al Movimiento del valor de ajuste la fecha posterior de los dos.  

Revisemos este proceso más en la práctica. Supongamos que tenemos un movimiento de producto de venta. El producto se envió el 5 de septiembre de 2020 y se facturó el día después.  

#### Mov. producto

|Nº mov.  |Nº producto  |Fecha reg.  |Tipo movimiento  | N.º documento |Código de ubicación  |Cantidad  |Importe coste (Real)  |Cantidad facturada  |Cantidad pendiente  |
|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|
|319     |A         |2020-09-05     |  Venta       |102033     |  Azul       | -1    |    -11     |-1     |    0     |

A continuación se muestran los movimientos de valor relacionados:

- El **Movimiento n.º 379** representa el envío y lleva la misma fecha de registro que el movimiento de valor principal.  
- El **Movimiento n.º 381** representa la factura.  
- El **Movimiento n.º 391** es un ajuste del movimiento de valor de facturación (del movimiento n.º 381 en adelante).  

|Nº mov.  |Nº producto  |Fecha reg.  |Tipo ovimiento contable de producto  |Tipo movimiento  |N.º documento  |Nº movimiento contable de producto  |Código de ubicación  |Cantidad mov. producto  |Cantidad facturada  |Importe coste (Real)  |Importe coste (Esperado)  |Ajuste  |Liq. por nº orden  |Cód. origen  |
|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|--------|---------|---------|---------|---------|
|379     |  A       |    2020-09-05     |    Venta     | Coste directo   | 102033        |319     | Azul        | -1       |0         |  0       |     -10   |No   |0    |Ccial          |
|381     |  A       |    2020-09-06     |    Venta     | Coste directo   | 103022        |319     | Azul        |  0       |-1        |-10       |    10     | No  |0      |       Ccial   |
|391     |  A       |    2020-09-10     |    Venta     | Coste directo   | 103022        |319     | Azul        |  0       |0         |-1        |    0     |Sí   |    181   | AJUSINVEN   |

Para asignar la fecha de registro para el **Movimiento n.º 391** se aplicaron los siguientes pasos:

1. El **movimiento de valor de ajuste** que se creará (**Movimiento n.º 391**) tiene asignada la misma **Fecha de registro** que el movimiento que ajusta.

2. El proceso **Valorar stock - movs. producto** determina si la fecha inicial de registro del movimiento de valor de ajuste está dentro del rango de fechas permitido según los Períodos de inventario o la Configuración de contabilidad.  

Revisemos la venta mencionada anteriormente agregando la configuración de los rangos de fechas de publicación permitidos.  
  
#### Periodos de inventario

|Fecha final  |Name  |Cerrada  |
|---------|---------|---------|
|2020-01-31     |2020 de enero      |  Sí    |
|2020-02-28     |Febrero de 2020     |  Sí    |
|2020-03-31     |Marzo de 2020        |  Sí    |
|2020-04-30     |Abril de 2020        |  Sí    |
|2020-05-31     |Mayo de 2020        |  Sí    |
|2020-06-30     |Junio de 2020       |  Sí    |
|2020-07-31     |Julio de 2020        |  Sí    |
|2020-08-31     |Agosto de 2020     |  Sí    |
|2020-09-30     |Septiembre de 2020  |         |
|2020-10-31     |Octubre de 2020    |         |
|2020-11-30     |Noviembre de 2020   |         |
|2020-12-31     |Diciembre de 2020   |         |

La primera fecha de publicación permitida es el primer día del primer periodo abierto, que es el 1 de septiembre de 2020.  

#### Configuración de contabilidad

|Campo|Valor  |
|---------|---------|
|Permitir registro desde:  |  2020-09-10      |
|Permitir registro hasta:    |  2020-09-30      |
|Registrar tiempo:       |         |
|Formato dirección local:|   C.P.      |  

La primera fecha de publicación permitida es la fecha indicada en el campo **Permitir registro desde**: 10 de septiembre de 2020. Si en la **Configuración de contabilidad** se definen tanto los Períodos de inventario como las fechas de registro permitidas se definirá el rango de fechas de registro permitidas.  

**Asignación de una fecha de registro permitida**  

La fecha de registro asignada inicial era el 6 de septiembre como se muestra en el paso 1. Sin embargo, en el segundo paso del proceso Valorar stock - movs. producto se identifica que la primera fecha de registro permitida es el 10 de septiembre y, por lo tanto, la asigna en el movimiento de valor de ajuste (**Movimiento n.º 391**) siguiente.  


|Nº mov.  |Nº producto  |Fecha reg.  |Tipo ovimiento contable de producto  |Tipo movimiento  |N.º documento  |Nº movimiento contable de producto  |Código de ubicación  |Cantidad mov. producto  |Cantidad facturada  |Importe coste (Real)  |Importe coste (Esperado)  |Ajuste  |Liq. por nº orden  |Cód. origen  |
|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|
|379     |  A       |    2020-09-05     |    Venta     | Coste directo   | 102033        |319     | Azul        | -1       |0         |  0       |     -10   |No   |0    |Ccial          |
|381     |  A       |    2020-09-06     |    Venta     | Coste directo   | 103022        |319     | Azul        |  0       |-1        |-10       |    10     | No  |0      |       Ccial   |
|391     |  A       |    **2020-09-10**     |    Venta     | Coste directo   | 103022        |319     | Azul        |  0       |0         |-1        |    0     |Sí   |    181   | AJUSINVEN   |

## Problemas comunes con el trabajo en lote "Ajustar coste: movimientos de producto"

Hay dos escenarios que el equipo de asistencia se encuentra con la frecuencia suficiente para justificar sus propios artículos de resolución de problemas.

### Mensaje de error: "La fecha de registro no está comprendida en su periodo de fechas de registro permitidas"

Si encuentra este error, debe ajustar las fechas en las que el usuario puede publicar movimientos. Para obtener más información, consulte [Mensaje de error: "La fecha de registro no está comprendida en su periodo de fechas de registro permitidas"](design-details-inventory-adjustment-value-entry-allowed-posting-dates.md).

### La fecha de registro en el movimiento de valor de ajuste frente a la fecha de registro en el movimiento que causa el ajuste, como la revaluación o el cargo de producto

Para obtener más información, consulte [Fecha de registro en el movimiento de valor de ajuste en comparación con el movimiento de origen](design-details-inventory-adjustment-value-entry-source-entry.md).

## Consulte también  

[Detalles de diseño: Coste de inventario](design-details-inventory-costing.md)  
[Detalles de diseño: Liquidación de productos](design-details-item-application.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
