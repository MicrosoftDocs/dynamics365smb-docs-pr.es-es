---
title: Fecha de registro en el movimiento de valor de ajuste en comparación con el movimiento de origen
description: 'Obtenga información sobre el escenario "La fecha de registro en el movimiento de valor de ajuste frente a la fecha de registro en el movimiento que causa el ajuste, como la revaluación o el cargo de producto" al ejecutar el trabajo por lotes Ajustar coste: movimientos de producto.'
author: edupont04
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 09/17/2021
ms.author: edupont
ms.openlocfilehash: 9d77c13cbe60d9e9b5c4d12e55d75f8815a4a5ba
ms.sourcegitcommit: ef80c461713fff1a75998766e7a4ed3a7c6121d0
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 02/15/2022
ms.locfileid: "8138679"
---
# <a name="posting-date-on-adjustment-value-entry-compared-to-the-source-entry"></a>Fecha de registro en el movimiento de valor de ajuste en comparación con el movimiento de origen

Este artículo compara la fecha de registro del movimiento de valor de ajuste con la fecha de registro del movimiento que provoca la ejecución del trabajo por lotes Ajustar coste: movimientos de producto, en particular un escenario de revalorización y un escenario de cargo de producto.

El trabajo por lotes **Ajustar coste: movimientos de producto** procesará sus datos dependiendo de su escenario y configuración de [!INCLUDE[prod_short](includes/prod_short.md)]. En esta sección, describimos dos procesos separados, y para cada uno mostramos el tipo de impacto que el trabajo por lotes Ajustar coste: movimientos de producto tiene en los datos.

## <a name="revaluation-scenario"></a>Ejemplo de revaluación

### <a name="prerequisites"></a>Requisitos previos  

Introduzca los siguientes valores:

**Configuración de inventario**:  

- Variación existencias automát. = Sí  

- Ajuste automático coste = Siempre  

- Tipo cálculo cte. medio = producto  

- Periodo coste medio = día  

**Configuración de contabilidad**:  

- Permitir registro desde = 1 de enero de 2021  

- Permitir registro hasta = vacío  

**Configuración usuarios**:  

- Permitir registro desde = 1 de diciembre de 2020  

- Permitir registro hasta = vacío  

### <a name="to-test-the-scenario"></a>Para probar el ejemplo

Pruebe este escenario realizando los siguientes pasos.

1. Cree un **Producto** llamado TEST con los siguientes valores:  

     - Unidad de medida base = PCS  

     - Método de coste = promedio  

     - Seleccione grupos de registro opcionales.  

2. Abra un **Diario de productos**, después cree una nueva entrada y registre una línea como se indica a continuación:  

     - Fecha registro = 15 de diciembre de 2020  

     - Producto = PRODUCTO  

     - Tipo movimiento = compra  

     - Cantidad = 100  

     - Precio unitario = 10  

3. Abra un **Diario de productos**, después cree una nueva entrada y registre una línea como se indica a continuación:  

     - Fecha = 20 de diciembre de 2020  

     - Producto = PRODUCTO  

     - Tipo movimiento = Ajuste negativo  

     - Cantidad = 2  

4. Abra un **Diario de productos**, después cree una nueva entrada y registre una línea como se indica a continuación:  

     - Fecha = 15 de enero de 2021  

     - Producto = PRODUCTO  

     - Tipo movimiento = Ajuste negativo  

     - Cantidad = 3  

5. Abra un **Diario de revaluación de productos**, después cree una nueva entrada y registre una línea como se indica a continuación:  

     - Producto = PRODUCTO  

     - Liq. por nº orden = seleccione el movimiento de compra registrado en el paso 2. La fecha de registro de la revaluación será la misma que la del movimiento que ajusta.  

     - Prec. coste (revaluado) = 40  

Se han registrado los siguientes **Movimientos de producto** y **Movimiento de valor**:  

**Movimiento de producto - compra**:  

|Número de movimiento  |Nº producto  |Fecha reg.  |Tipo movimiento  |N.º documento  |Cantidad  |Importe coste (Real)  |Cantidad pendiente  |
|---------|---------|---------|---------|---------|---------|---------|---------|
|317     |EXAMINAR         |2020-12-15         |Compra         |T00001         |100         |4000         |95        |

**Movimientos valor**  

|Número de movimiento  |Nº producto  |Fecha reg.  |Nº movimiento contable de producto  |Tipo ovimiento contable de producto  |Tipo movimiento  |N.º documento  |Cantidad mov. número producto  |Importe coste (Real)  |Coste regis. en contab.  |Ajuste  |Se aplica a mov.  |Cód. origen  |
|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|
|376     |EXAMINAR|   2020-12-15    |317         |Compra         |Coste directo         |T00001         |100         |1 000,00          |1 000,00    |No         |0         |ITEMNL         |
|379     |EXAMINAR   |**2020-12-15**    |317         |Compra         |Revaluación         |T04002         |0         |3 000,00         |3 000,00         |No         |0         |REVALINL         |

**Mov. contabilidad producto - ajuste negativo, Paso 3**  

|Nº mov.  |Nº producto  |Fecha reg.  |Tipo movimiento  |N.º documento  |Cantidad  |Importe coste (Real)  |Cantidad pendiente  |
|---------|---------|---------|---------|---------|---------|---------|---------|
|318     |EXAMINAR      |2020-12-20   |Ajuste negativo  |T00002         |-2         |-80         | 0        |

**Movimientos valor**  

|Número de movimiento  |Nº producto  |Fecha reg.  |Nº movimiento contable de producto  |Tipo ovimiento contable de producto  |Tipo movimiento  |N.º documento  |Cantidad mov. número producto  |Importe coste (Real)  |Coste regis. en contab.  |Ajuste  |Se aplica a mov.  |Cód. origen  |
|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|
|377     |EXAMINAR|   2020-12-20    |318         |Ajuste negativo         |Coste directo         |T00002         |-2         |-20          |-20    |No         |0         |ITEMNL         |
|380     |EXAMINAR   |**2021-01-01**    |318         |Ajuste negativo         |Coste directo         |T04002         |0         |-60         |-60         |Sí         |377         |INVTADAMT         |

**Mov. contabilidad producto - ajuste negativo, Paso 4**  

|Nº mov.  |Nº producto  |Fecha reg.  |Tipo movimiento  |N.º documento  |Cantidad  |Importe coste (Real)  |Cantidad pendiente  |
|---------|---------|---------|---------|---------|---------|---------|---------|
|319     |EXAMINAR      |2021-01-15   |Ajuste negativo  |T00003         |-3         |-120         | 0        |

**Movimientos valor**  

|Número de movimiento  |Nº producto  |Fecha reg.  |Nº movimiento contable de producto  |Tipo ovimiento contable de producto  |Tipo movimiento  |N.º documento  |Cantidad mov. número producto  |Importe coste (Real)  |Coste regis. en contab.  |Ajuste  |Se aplica a mov.  |Cód. origen  |
|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|
|378     |EXAMINAR|   2021-01-15    |319         |Ajuste negativo         |Coste directo         |T00003         |-3         |-30          |-30    |No         |0         |ITEMNL         |
|381     |EXAMINAR   |**2021-01-15**    |319         |Ajuste negativo         |Coste directo         |T04003         |0         |-90         |-90         |Sí         |378         |INVTADAMT         |

El proceso **Ajustar coste: movimientos de producto** ha reconocido un cambio de costes y ha ajustado los ajustes negativos.  

**Revisión de las fechas de registro en los movimientos de valor de ajuste creados:** la primera fecha de registro permitida con la que el proceso Valorar stock - movs. producto tiene que estar relacionado es el 1 de enero de 2021 tal como se indica en Configuración de contabilidad.  

**Ajuste negativo en el paso 3:** la fecha de registro asignada es el 1 de enero, proporcionada por la Configuración de contabilidad. La fecha de registro del movimiento del valor para afrontar es el 20 de diciembre de 2020. Según la configuración de contabilidad, la fecha no se encuentra dentro del rango de fechas permitidas. Por lo tanto, la fecha de registro indicada en el campo Permitir registro desde en la Configuración de contabilidad se asigna al movimiento del valor de ajuste.  

**Ajuste negativo en el paso 4:** la fecha de registro asignada es el 15 de enero. El movimiento de valor para afrontar tiene fecha de registro el 15 de enero, que se encuentra en el rango de fechas permitido en función de la configuración de contabilidad.  

El ajuste realizado para el Ajuste negativo en el paso 3 es el que produce la discusión. La fecha de registro favorable para el movimiento del valor de ajuste habría sido el 20 de diciembre o al menos en diciembre, ya que la revaluación que causaba el cambio en el CV se registró en diciembre.  

Para lograr el ajuste del Ajuste negativo en el paso 3 en diciembre, el campo Configuración de contabilidad, Permitir registro desde, debe indicar una fecha en diciembre.  

### <a name="conclusion"></a>Conclusión

Con la experiencia obtenida en este escenario, al tener en cuenta la configuración más adecuada para un rango de fechas de registro permitido para una empresa, es posible que desee tener en cuenta lo siguiente. Siempre que permita que los cambios en el valor del inventario se registren en un periodo, como diciembre en este caso, la configuración que utiliza la empresa para los rangos de fechas de registro permitidos debe estar alineada con esta decisión. El campo Permitir registro desde de la Configuración de contabilidad, que comienza el 1 de diciembre, permitirá que la revaluación realizada en diciembre se envíe a los movimientos salientes afectados en el mismo período.  

Los grupos de usuarios a los que no se les permite publicar en diciembre pero sí en enero, que probablemente estaban destinados a estar limitados por la Configuración de contabilidad de este ejemplo, deberían repararse a través de la Configuración del usuario.  

## <a name="item-charge-scenario"></a>Ejemplo cargos producto  

### <a name="prerequisites"></a>Requisitos previos  

Introduzca los siguientes valores:

**Configuración de inventario**:  

- Variación existencias automát. = Sí  

- Ajuste automático coste = Siempre  

- Tipo cálculo cte. medio = producto  

- Periodo coste medio = día  

**Configuración de contabilidad**:  

- Permitir registro desde = 1 de diciembre de 2020.  

- Permitir registro hasta = vacío  

**Configuración usuarios**:  

- Permitir registro desde = 1 de diciembre de 2020.  

- Permitir registro hasta = vacío  

### <a name="to-test-the-scenario"></a>Para probar el ejemplo  

Pruebe este escenario realizando los siguientes pasos:

1.  Cree un cargo de **Producto** con los siguientes valores:  

     - Unidad de medida base = PCS  

     - Método de coste = promedio  

     - Seleccione grupos de registro opcionales.  

2.  Crear un nuevo **Pedido de compra** con los siguientes valores:  

     - Compra a-N.º proveedor: 10000  

     - Fecha registro = 15 de diciembre de 2020

     - N.º factura proveedor: 1234  

     En la Línea de pedido de compra, seleccione los siguientes valores:  

     - Producto = CARGO  

     - Cantidad = 1  

     - Coste unitario directo = 100  

     Para completar el paso, registre el documento como recibido y facturado.  

3.  Crear un nuevo **Pedido de venta** con los siguientes valores:  

     - Venta a-Nº cliente: 10000  

     - Fecha registro = 16 de diciembre de 2020  

     En la línea del pedido de venta:  

     - Producto = CARGO  

     - Cantidad = 1  

     - Precio venta = 135  

     Para completar el paso, registre el documento como recibido y facturado.  

4.  Introduzca valores para la página **Configuración de contabilidad**:  

     - Permitir registro desde = 1 de enero de 2021  

    -  Permitir registro hasta = en blanco  

5.  Crear un nuevo **Pedido de compra** con los siguientes valores:  

     - Compra a-N.º proveedor: 10000  

     - Fecha registro = 2 de enero de 2021  

     - N.º factura proveedor: 2345  

     En la línea del pedido de compra:  

     - Cargo de producto = JB-FLETE  

     - Cantidad = 1  

     - Coste unitario directo = 3  

     - Asignar cargo de producto al albarán de compra desde el paso 2.  

     Para completar el paso, registre el documento como recibido y facturado.  


**Estado movimiento contabilidad producto compra, paso 2**:  
  
|Número de movimiento  |Nº producto  |Fecha reg.  |Tipo movimiento  |N.º documento  |Cantidad  |Importe coste (Real)  |Cantidad pendiente  |
|---------|---------|---------|---------|---------|---------|---------|---------|
|324     |CARGO         |2020-12-15         |Compra         |107030         |1         |105         |0        |

**Movimientos valor**  

|Número de movimiento |Nº producto  |Fecha reg.  |Nº movimiento contable de producto  |Tipo ovimiento contable de producto  |Tipo movimiento  |N.º documento  | N.º cargo art.    |  Cantidad mov. producto   |Importe coste (Real)     |Coste regis. en contab. |Ajuste |Liq. por nº orden |
|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|
|397      |CARGO|   2020-12-15    |324         |Compra         |Coste directo         |108029         |         |1          |100    |100         |Nº         |0         |
|399      |CARGO   |2021-01-02    |324         |Compra         |Coste directo         |108009         |JBFREIGHT         |0         |3         |3         |Nº         |0         |

**Estado movimiento contabilidad venta**:  
  
|Nº mov.  |Nº producto  |Fecha reg.  |Tipo movimiento  |N.º documento  |Cantidad  |Importe coste (Real)  |Cantidad pendiente  |
|---------|---------|---------|---------|---------|---------|---------|---------|
|325     |CARGO         |2020-12-16         |Venta         |102035         |-1         |-105         |0        |

**Movimientos valor**  

|Número de movimiento |Nº producto  |Fecha reg.  |Nº movimiento contable de producto  |Tipo ovimiento contable de producto  |Tipo movimiento  |N.º documento  | N.º cargo art.    |  Cantidad mov. producto   |Importe coste (Real)     |Coste regis. en contab. |Ajuste |Liq. por nº orden |
|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|
|398      |CARGO|   2020-12-16    |325         |Venta         |Coste directo         |109024         |         |-1          |-100    |-100         |Nº         |0         |
|400      |CARGO   |2021-01-01    |325         |Venta         |Coste directo         |109024         |         |0         |-3         |-3         |Sí         |398         |

6.  En la fecha de trabajo 3 de enero llega una factura de compra que contiene un cargo adicional de producto en la compra realizada en el paso 2. Esta factura tiene fecha de documento el 30 de diciembre y, por lo tanto, se registre con Fecha de registro el 30 de diciembre de 2020.  

     Crear un nuevo **Pedido de compra** con los siguientes valores:  

     - Compra a-N.º proveedor: 10000  

     - Fecha registro = 30 de diciembre de 2020  

     - N.º factura proveedor: 3456  

     En la Línea de pedido de compra, seleccione los siguientes valores:  

     - Cargo de producto = JB-FLETE  

     - Cantidad = 1  

     - Coste unitario directo = 2  

     Asignar cargo de producto al albarán de compra desde el paso 2  

     Para completar el paso, registre el documento como recibido y facturado.  


**Estado movimiento contabilidad producto compra**:  

|Número de movimiento  |Nº producto  |Fecha reg.  |Tipo movimiento  |N.º documento  |Cantidad  |Importe coste (Real)  |Cantidad pendiente  |
|---------|---------|---------|---------|---------|---------|---------|---------|
|324     |CARGO         |2020-12-15         |Compra         |107030         |1         |105         |0        |

**Movimientos valor**  

|Nº mov. |Nº producto  |Fecha reg.  |Nº movimiento contable de producto  |Tipo ovimiento contable de producto  |Tipo movimiento  |N.º documento  | N.º cargo art.    |  Cantidad mov. producto   |Importe coste (Real)     |Coste regis. en contab. |Ajuste |Liq. por nº orden |
|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|
|397      |CARGO   |2020-12-15    |324         |Compra         |Coste directo         |108029         |            |1         |100    |100         |No         |0         |
|399      |CARGO   |2021-01-02    |324         |Compra         |Coste directo         |108030         |JBFREIGHT   |0         |3         |3         |No         |0         |
|401      |CARGO   |**2020-12-30**    |324         |Compra         |Coste directo         |108031         |JBFREIGHT   |0         |2         |2         |No         |0         |

**Estado movimiento contabilidad venta**:  
  
|Número de movimiento  |Nº producto  |Fecha reg.  |Tipo movimiento  |N.º documento  |Cantidad  |Importe coste (Real)  |Cantidad pendiente  |
|---------|---------|---------|---------|---------|---------|---------|---------|
|325     |CARGO         |2020-12-16         |Venta         |102035         |-1         |-105         |0        |

**Movimientos valor**  

|Nº mov. |Nº producto  |Fecha reg.  |Nº movimiento contable de producto  |Tipo ovimiento contable de producto  |Tipo movimiento  |N.º documento  | N.º cargo art.    |  Cantidad mov. producto   |Importe coste (Real)     |Coste regis. en contab. |Ajuste |Liq. por nº orden |
|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|
|398      |CARGO   |2020-12-16        |325         |Venta         |Coste directo         |103024         |            |-1         |-100       |-100         |No         |0         |
|400      |CARGO   |2021-01-01        |325         |Venta         |Coste directo         |103024         |            |0          |-3         |-3         |Sí         |398         |
|402      |CARGO   |**2021-01-01**    |325         |Venta         |Coste directo         |103024         |            |0          |-2         |-2         |Sí         |398         |

El informe Valoración inventario se imprime a partir de fecha 31 de diciembre de 2020

![Contenido del informe de valoración inventario.](media/helene/TechArticleAdjustcost13.png "Contenido del informe de valoración de inventario")

**Resumen de ejemplo:**  

El ejemplo descrito termina con un informe de Valoración inventario que demuestra Cantidad = 0 mientras que Valor = 2. El Cargo de producto publicado en el paso 6 es parte del valor de Entrada de existencias de diciembre, mientras que la Salida de existencias del mismo período no se ve afectada.  

El hecho de tener la Configuración de contabilidad que indicaba Permitir registro desde el 1 de enero, fue ventajoso para el primer Cargo de producto. Los costes de la Entrada y Salida de existencias se registró en el mismo periodo. Sin embargo para el segundo cargo de producto, la configuración de contabilidad produce el cambio en el coste de ventas que se reconocerá en el periodo posterior.  

**Conclusión:**  

Es un desafío tener el informe de Valoración inventario para demostrar Cantidad = 0 mientras que Valor <> 0. En este caso, también es más difícil expresar la configuración óptima, ya que las facturas de compra llegan el mismo día pero abordan diferentes períodos e incluso ejercicios. Cambiar a un ejercicio nuevo generalmente requiere un poco de planificación y, como parte de eso, se debe tener en cuenta el conocimiento del proceso Ajustar coste: movimientos de producto, que reconoce el CV.  

En este ejemplo, una opción podría ser tener en la Configuración de contabilidad, en el campo Permitir registro desde, una fecha indicada en diciembre por un par de días más y posponer el registro del cargo por primer producto para permitir todos los costes del período o ejercicio anterior para que el período al que pertenecen primero los pueda reconocer, mientras se ejecuta el proceso Valorar stock - movs. producto y luego mover la fecha de registro permitida al nuevo período\/ejercicio. El primer cargo de producto con fecha de registro el 2 de enero podría registrarse.  

## <a name="see-also"></a>Consulte también  

[Detalles de diseño: Fecha registro en el movimiento de valor de ajuste](design-details-inventory-adjustment-value-entry-posting-date.md)  
[Detalles de diseño: Coste de inventario](design-details-inventory-costing.md)  
[Detalles de diseño: Liquidación de productos](design-details-item-application.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
