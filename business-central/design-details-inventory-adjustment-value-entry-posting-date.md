---
title: Fecha registro en movimientos de valores
description: Aprender cómo el proceso Valorar stock - movs. producto identifica y asigna una fecha de registro a los movimientos de valor que creará.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 08/19/2021
ms.author: edupont
ms.openlocfilehash: 3dcda7f44797f52e50babe4dbec90e3b2be6f19d
ms.sourcegitcommit: e891484daad25f41c37b269f7ff0b97df9e6dbb0
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 08/27/2021
ms.locfileid: "7440743"
---
# <a name="design-details-posting-date-on-adjustment-value-entry"></a>Detalles de diseño: Fecha registro en el movimiento de valor de ajuste  

Este artículo proporciona una guía para los usuarios de la funcionalidad Coste de inventario en [!INCLUDE[prod_short](includes/prod_short.md)]. El artículo específico proporciona una guía de cómo el proceso **Valorar stock - movs. producto** identifica y asigna una fecha de registro a los movimientos de valor que creará.  

Primero se revisa el concepto del proceso, cómo el proceso identifica y asigna una fecha de registro a los movimientos de valor que se crearán. A continuación, se comparten algunos ejemplos que encontramos en el equipo de soporte de vez en cuando y, finalmente, hay un resumen de los conceptos utilizados.  

## <a name="the-concept"></a>El concepto  

El proceso **Valorar stock - movs. producto** asigna una fecha de registro al movimiento de valor que creará en los pasos siguientes:  

1.  Inicialmente, la fecha de registro del movimiento que se creará es la misma que la del movimiento que ajusta.  

2.  La fecha de registro se valida con Periodos de inventario o Configuración de contabilidad.  

3.  Asignación de la fecha de registro; si la fecha inicial no se encuentra dentro del rango de fechas permitidas, el proceso asignará una Fecha de registro permitida en la Configuración de contabilidad o en el Período de inventario. Si en la Configuración de contabilidad se definen tanto los Períodos de inventario como las fechas de registro permitidas, se asignará al Movimiento del valor de ajuste la fecha posterior de los dos.  

 Revisemos este proceso más en la práctica. Supongamos que tenemos un movimiento de producto de venta. El producto se envió el 5 de septiembre de 2020 y se facturó el día después.  


**Mov. producto**  
Formato de fecha YYYY-MM-DD

|Nº mov.  |Nº producto  |Fecha reg.  |Tipo movimiento  | N.º documento |Código de ubicación  |Cantidad  |Importe coste (Real)  |Cantidad facturada  |Cantidad pendiente  |
|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|
|319     |A         |2020-09-05     |  Venta       |102033     |  Azul       | -1    |    -11     |-1     |    0     |

A continuación, el primer movimiento de valor (379) representa el envío y lleva la misma fecha de registro que el movimiento de valor principal.  
  
El segundo movimiento de valor (381) representan la factura.  

El tercer movimiento de valor (391) es un ajuste del movimiento de valor de facturación (381).  
  

|Nº mov.  |Nº producto  |Fecha reg.  |Tipo mov. producto  |Tipo movimiento  |N.º documento  |Nº movimiento contable de producto  |Código de ubicación  |Cantidad mov. producto  |Cantidad facturada  |Importe coste (Real)  |Importe coste (Esperado)  |Ajuste  |Liq. por nº orden  |Cód. origen  |
|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|--------|---------|---------|---------|---------|
|379     |  A       |    2020-09-05     |    Venta     | Coste directo   | 102033        |319     | Azul        | -1       |0         |  0       |     -10   |No   |0    |Ccial          |
|381     |  A       |    2020-09-06     |    Venta     | Coste directo   | 103022        |319     | Azul        |  0       |-1        |-10       |    10     | No  |0      |       Ccial   |
|391     |  A       |    2020-09-10     |    Venta     | Coste directo   | 103022        |319     | Azul        |  0       |0         |-1        |    0     |Sí   |    181   | AJUSINVEN   |

Inicialmente, la fecha de registro del movimiento se establece en la misma fecha que la del movimiento que ajusta.

 Paso 1: El movimiento de valor de ajuste que se creará tiene asignada la misma fecha de registro que el movimiento que ajusta, ilustrada anteriormente con el movimiento de valor 391.  
  
 Paso 2: Validación de la fecha de registro asignada inicial.  

El proceso **Valorar stock - movs. producto** determina si la fecha inicial de registro del movimiento de valor de ajuste está dentro del rango de fechas permitido según los Períodos de inventario o la Configuración de contabilidad.  

Revisemos la venta mencionada anteriormente agregando la configuración de los rangos de fechas de publicación permitidos.  
  
**Periodos inventario**

|Fecha final  |Name  |Cerrada  |
|---------|---------|---------|
|2020-01-31     |2020 de enero      |  Sí    |
|2020-02-28     |Febrero de 2020     |  Sí    |
|2020-03-31     |Marzo de 2020        |  Sí    |
|2020-04-30     |Abril de 2020        |  Sí    |
|2020-05-31     |Mayo de 2020        |  Sí    |
|2020-06-30     |Junio de 2020       |  Sí    |
|2020-07-31     |Julio de 2020        |   Sí   |
|2020-08-31     |Agosto de 2020     |   Sí   |
|2020-09-30     |Septiembre de 2020  |         |
|2020-10-31     |Octubre de 2020    |         |
|2020-11-30     |Noviembre de 2020   |         |
|2020-12-31     |Diciembre de 2020   |         |

La primera fecha de publicación permitida es el primer día del primer período abierto. 1 de septiembre de 2020.  

**Configuración de contabilidad**

|Campo|Valor  |
|---------|---------|
|Permitir registro desde:  |  2020-09-10      |
|Permitir registro hasta:    |  2020-09-30      |
|Registrar tiempo:       |         |
|Formato dirección local:|   C.P.      |  

 La primera fecha de publicación permitida es la fecha indicada en el campo Permitir registro desde: 10 de septiembre de 2020.  
 Si en la Configuración de contabilidad se definen tanto los Períodos de inventario como las fechas de registro permitidas se definirá el rango de fechas de registro permitidas.  

 Paso 3: Asignación de una fecha de registro permitida;  

 La fecha de registro asignada inicial era el 6 de septiembre como se muestra en el paso 1. Sin embargo, en el segundo paso del proceso Valorar stock - movs. producto se identifica que la primera fecha de registro permitida es el 10 de septiembre y, por lo tanto, la asigna en el movimiento de valor de ajuste siguiente.  

   
|Nº mov.  |Nº producto  |Fecha reg.  |Tipo ovimiento contable de producto  |Tipo movimiento  |N.º documento  |Nº movimiento contable de producto  |Código de ubicación  |Cantidad mov. producto  |Cantidad facturada  |Importe coste (Real)  |Importe coste (Esperado)  |Ajuste  |Liq. por nº orden  |Cód. origen  |
|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|
|379     |  A       |    2020-09-05     |    Venta     | Coste directo   | 102033        |319     | Azul        | -1       |0         |  0       |     -10   |No   |0    |Ccial          |
|381     |  A       |    2020-09-06     |    Venta     | Coste directo   | 103022        |319     | Azul        |  0       |-1        |-10       |    10     | No  |0      |       Ccial   |
|391     |  A       |    **2020-09-10**     |    Venta     | Coste directo   | 103022        |319     | Azul        |  0       |0         |-1        |    0     |Sí   |    181   | AJUSINVEN   |

 Ahora hemos revisado el concepto para asignar fechas de registro a los movimientos de valor creados por el proceso Valorar stock - movs. producto.  

 Continuaremos revisando algunos ejemplos que encontramos en el equipo de soporte de vez en cuando en relación con las fechas de registro asignadas al proceso Valorar stock - movs. producto y las configuraciones relacionadas.  

## <a name="scenario-i-posting-date-is-not-within-your-range-of-allowed-posting-dates"></a>Ejemplo I: "La fecha de registro no está comprendida en su periodo de fechas de registro permitidas..."  

 Este es un ejemplo en el que un usuario experimenta el mensaje de error mencionado cuando se ejecuta el proceso Valorar stock - movs. producto.  

 En la sección anterior, que describe el concepto de asignación de fechas de registro, la intención del trabajo Valorar stock - movs. producto es crear un movimiento de valor con la fecha de registro el 10 de septiembre.  

![Mensaje de error sobre la fecha de registro.](media/helene/TechArticleAdjustcost6.png "Mensaje de error sobre la fecha de registro")

 Seguimos con la configuración del usuario:  

**Configuración usuarios**  

Ordenar: ID de usuario  

|Id. de usuario  |Permitir registro desde  | Permitir registro hasta  |
|---------|---------|--------|
|EUROPA  |  2020-09-11      |2020-09-30      |

 El usuario en este caso tiene un rango de fechas de registro permitidas desde el 11 hasta el 30 de septiembre y, por lo tanto, no puede registrar el movimiento de valor de ajuste con fecha de publicación el 10 de septiembre.  

### <a name="overview-of-involved-posting-date-setup"></a>Descripción general de la configuración de la fecha de registro involucrada:

**Periodos inventario**  

|Fecha final  |Name  |Cerrada  |
|---------|---------|---------|
|2020-01-31     |2020 de enero      |  Sí    |
|2020-02-28     |Febrero de 2020     |  Sí    |
|2020-03-31     |Marzo de 2020        |  Sí    |
|2020-04-30     |Abril de 2020        |  Sí    |
|2020-05-31     |Mayo de 2020        |  Sí    |
|2020-06-30     |Junio de 2020       |  Sí    |
|2020-07-31     |Julio de 2020        |   Sí   |
|2020-08-31     |Agosto de 2020     |   Sí   |
|2020-09-30     |Septiembre de 2020  |         |
|2020-10-31     |Octubre de 2020    |         |
|2020-11-30     |Noviembre de 2020   |         |
|2020-12-31     |Diciembre de 2020   |         |  

**Configuración de contabilidad**  

|Campo|Valor|
|---------|---------|
|Permitir registro desde:  |  2020-09-10      |
|Permitir registro hasta:    |  2020-09-30      |
|Registrar tiempo:       |         |
|Formato dirección local:|   C.P.      |  

**Configuración usuarios**    

|Id. de usuario  |Permitir registro desde  | Permitir registro hasta  |
|---------|---------|--------|
|USERNAME |  2020-09-10      |2020-09-30      |

 Al asignar al usuario un rango de fechas de registro permitido más amplio (o el mismo) que en el Período de inventario o la Configuración de contabilidad, se evitará el conflicto mencionado. El movimiento valor de ajuste con fecha de contabilización del 10 de septiembre se contabilizará correctamente con esta configuración.

Un artículo de Knowledge Base antiguo [952996](https://support.microsoft.com/topic/information-about-inventory-adjustment-posting-dates-in-microsoft-dynamics-nav-99e22b2b-5b79-a9b2-3b43-7f3484fa31d9) describe más ejemplos relacionados con el mensaje de error mencionado.  

## <a name="scenario-ii-posting-date-on-adjustment-value-entry-versus-posting-date-on-entry-causing-the-adjustment-such-as-revaluation-or-item-charge"></a>Ejemplo II: La fecha de registro en el movimiento de valor de ajuste frente a la fecha de registro en el movimiento que causa el ajuste, como la revaluación o el cargo de producto.  

### <a name="revaluation-scenario"></a>Ejemplo de revaluación:  

 Requisitos previos:  

 Configuración de inventario:  
me
-   Variación existencias automát. = Sí  

-   Ajuste automático coste = Siempre  

-   Tipo cálculo cte. medio = producto  

-   Periodo coste medio = día  

 Configuración de contabilidad:  

-   Permitir registro desde = 1 de enero de 2021  

-   Permitir registro hasta = vacío  

 Configuración usuarios:  

-   Permitir registro desde = 1 de diciembre de 2020  

-   Permitir registro hasta = vacío  

### <a name="to-test-the-scenario"></a>Para probar el ejemplo  

1.  Crear PRUEBA de producto:  

     Unidad de medida base = PCS  

     Método de coste = promedio  

     Seleccione grupos de registro opcionales.  

2.  El diario de productos abierto crea y registra un línea como se indica a continuación:  

     Fecha registro = 15 de diciembre de 2020  

     Producto = PRODUCTO  

     Tipo movimiento = compra  

     Cantidad = 100  

     Precio unitario = 10  

3.  El diario de productos abierto crea y registra un línea como se indica a continuación:  

     Fecha = 20 de diciembre de 2020  

     Producto = PRODUCTO  

     Tipo movimiento = Ajuste negativo  

     Cantidad = 2  

4.  El diario de productos abierto crea y registra un línea como se indica a continuación:  

     Fecha = 15 de enero de 2021  

     Producto = PRODUCTO  

     Tipo movimiento = Ajuste negativo  

     Cantidad = 3  

5.  El diario de revaluación abierto crea y registra un línea como se indica a continuación:  

     Producto = PRODUCTO  

     Liq. por nº orden = seleccione el movimiento de compra registrado en el paso 2. La fecha de registro de la revaluación será la misma que la del movimiento que ajusta.  

     Prec. coste revaluado = 40  

Se han registrado los siguientes **Movimientos de producto** y **Movimiento de valor**:  

**Movimiento de producto - compra**:  
Formato de fecha YYYY-MM-DD  

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

El proceso Valorar stock - movs. producto ha reconocido un cambio de costes y ha ajustado los ajustes negativos.  

**Revisión de las fechas de registro en los movimientos de valor de ajuste creados:** la primera fecha de registro permitida con la que el proceso Valorar stock - movs. producto tiene que estar relacionado es el 1 de enero de 2021 tal como se indica en Configuración de contabilidad.  

**Ajuste negativo en el paso 3:** la fecha de registro asignada es el 1 de enero, proporcionada por la Configuración de contabilidad. La fecha de registro del movimiento del valor para afrontar es el 20 de diciembre de 2020. Según la configuración de contabilidad, la fecha no se encuentra dentro del rango de fechas permitidas. Por lo tanto, la fecha de registro indicada en el campo Permitir registro desde en la Configuración de contabilidad se asigna al movimiento del valor de ajuste.  

**Ajuste negativo en el paso 4:** la fecha de registro asignada es el 15 de enero. El movimiento de valor para afrontar tiene fecha de registro el 15 de enero, que se encuentra en el rango de fechas permitido en función de la configuración de contabilidad.  

El ajuste realizado para el Ajuste negativo en el paso 3 es el que produce la discusión. La fecha de registro favorable para el movimiento del valor de ajuste habría sido el 20 de diciembre o al menos en diciembre, ya que la revaluación que causaba el cambio en el CV se registró en diciembre.  

Para lograr el ajuste del Ajuste negativo en el paso 3 en diciembre, el campo Configuración de contabilidad, Permitir registro desde, debe indicar una fecha en diciembre.  

**Conclusión:**  

Con las experiencias de este ejemplo y si se tiene en cuenta la configuración más adecuada del rango de fechas de registro permitido para una empresa, la siguiente información le puede resultar útil: siempre que los cambios en el valor de inventario se puedan publicar en un período, en este caso en diciembre, la configuración que usa la empresa para los rangos de fechas de registro permitido debe estar alineada con esta decisión. El campo Permitir registro desde de la Configuración de contabilidad, que comienza el 1 de diciembre, permitirá que la revaluación realizada en diciembre se envíe a los movimientos salientes afectados en el mismo período.  

Los grupos de usuarios a los que no se les permite publicar en diciembre pero sí en enero, que probablemente estaban destinados a estar limitados por la Configuración de contabilidad de este ejemplo, deberían repararse a través de la Configuración del usuario.  

### <a name="item-charge-scenario"></a>Ejemplo cargos producto:  

 Requisitos previos:  

 Configuración de inventario:  

-   Variación existencias automát. = Sí  

-   Ajuste automático coste = Siempre  

-   Tipo cálculo cte. medio = producto  

-   Periodo coste medio = día  

 Configuración de contabilidad:  

-   Permitir registro desde = 1 de diciembre de 2020.  

-   Permitir registro hasta = vacío  

 Configuración usuarios:  

-   Permitir registro desde = 1 de diciembre de 2020.  

-   Permitir registro hasta = vacío  


### <a name="to-test-the-scenario"></a>Para probar el ejemplo  

1.  Crear cargo producto:  

     Unidad de medida base = PCS  

     Método de coste = promedio  

     Seleccione grupos de registro opcionales.  

2.  Crear un nuevo pedido de compra  

     Compra a-N.º proveedor: 10000  

     Fecha registro = 15 de diciembre de 2020

     N.º factura proveedor: 1234  

     En la línea del pedido de compra:  

     Producto = CARGO  

     Cantidad = 1  

     Coste unitario directo = 100  

     Registrar recepción y factura.  

3.  Crear un nuevo pedido de venta:  

     Venta a-Nº cliente: 10000  

     Fecha registro = 16 de diciembre de 2020  

     En la línea del pedido de venta:  

     Producto = CARGO  

     Cantidad = 1  

     Precio venta = 135  

     Registrar, enviar y facturar.  

4.  Configuración de contabilidad:  

     Permitir registro desde = 1 de enero de 2021  

     Permitir registro hasta = en blanco  

5.  Crear un nuevo pedido de compra:  

     Compra a-N.º proveedor: 10000  

     Fecha registro = 2 de enero de 2021  

     N.º factura proveedor: 2345  

     En la línea del pedido de compra:  

     Cargo de producto = JB-FLETE  

     Cantidad = 1  

     Coste unitario directo = 3  

     Asignar cargo de producto al albarán de compra desde el paso 2.  

     Registrar albarán y factura.  


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

     Crear un nuevo pedido de compra:  

     Compra a-N.º proveedor: 10000  

     Fecha registro = 30 de diciembre de 2020  

     N.º factura proveedor: 3456  

     En la línea del pedido de compra:  

     Cargo de producto = JB-FLETE  

     Cantidad = 1  

     Coste unitario directo = 2  

     Asignar cargo de producto al albarán de compra desde el paso 2  

     Registrar albarán y factura.  


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

 El ejemplo descrito termina con un informe de Valoración inventario que demuestra Cantidad = 0 mientras que Valor = 2. El Cargo de producto publicado en el paso 11 es parte del valor de Entrada de existencias de diciembre, mientras que la Salida de existencias del mismo período no se ve afectada.  

 El hecho de tener la Configuración de contabilidad que indicaba Permitir registro desde el 1 de enero, fue ventajoso para el primer Cargo de producto. Los costes de la Entrada y Salida de existencias se registró en el mismo periodo. Sin embargo para el segundo cargo de producto, la configuración de contabilidad produce el cambio en el coste de ventas que se reconocerá en el periodo posterior.  

 **Conclusión:**  

 Es un desafío tener el informe de Valoración inventario para demostrar Cantidad = 0 mientras que Valor <> 0. En este caso, también es más difícil expresar la configuración óptima, ya que las facturas de compra llegan el mismo día pero abordan diferentes períodos e incluso ejercicios. Cambiar a un ejercicio nuevo generalmente requiere un poco de planificación y, como parte de eso, se debe tener en cuenta el conocimiento del proceso Valorar stock - movs. producto, que reconoce el CV.  

 En este ejemplo, una opción podría ser tener en la Configuración de contabilidad, en el campo Permitir registro desde, una fecha indicada en diciembre por un par de días más y posponer el registro del cargo por primer producto para permitir todos los costes del período o ejercicio anterior para que el período al que pertenecen primero los pueda reconocer, mientras se ejecuta el proceso Valorar stock - movs. producto y luego mover la fecha de registro permitida al nuevo período\/ejercicio. El primer cargo de producto con fecha de registro el 2 de enero podría registrarse.  

## <a name="history-of-adjust-cost--item-entries-batch-job"></a>Historial del proceso Valorar stock - movs. producto  

 A continuación, se incluye un resumen del concepto que asigna fechas de registro a los movimientos de valor de ajuste por proceso Valorar stock - movs. producto.  

### <a name="about-the-request-form-posting-date"></a>Acerca de la fecha de registro del formulario de solicitud:  

 Ya no debe introducirse una fecha de registro en el formulario de solicitud del proceso Valorar stock - movs. producto. El proceso ejecuta todos los cambios necesarios y crea movimientos de valor con la fecha de registro del movimiento de valor que ajusta. Si la fecha de registro no se encuentra dentro del rango de fechas permitidas, la fecha del campo Permitir registrar desde en Configuración contabilidad, o si se usan Periodos de inventario, se deberá usar la más reciente de las dos. Vea el concepto descrito anteriormente.  

## <a name="history-of-post-inventory-cost-to-gl-batch-job"></a>Historial del proceso Regis. variación existencias  

 El proceso Registrar variación existencias está estrechamente relacionado con Valorar stock - movs. producto, ya que su historial también se resume y comparte aquí.  
 
![Coste real frente a coste previsto.](media/helene/TechArticleAdjustcost14.png "Coste real frente a coste previsto")

### <a name="about-the-posting-date"></a>Acerca de la fecha de registro  

 Ya no debe introducirse una fecha de registro en el formulario de solicitud del proceso Registrar variación existencias. El movimiento de contabilidad se crea con la misma fecha de registro que los movimientos de valor relacionados. Para completar el proceso, el rango de fechas de registro permitidas debe permitir la Fecha de registro del movimiento de contabilidad creado. De lo contrario, el rango de fechas de registro permitidas debe volver a abrirse temporalmente cambiando o eliminando las fechas en los campos Permitir registro desde y en la Configuración de contabilidad. Para evitar errores de conciliación es necesario que fecha de registro del movimiento de contabilidad se corresponda con la fecha de registro del movimiento de valor.  

 El proceso escanea la Tabla 5811 - Registrar movimiento valor en C/G para identificar los movimientos de valor en el ámbito para registrar en la Contabilidad. Después de una ejecución correcta, la tabla se vacía.

## <a name="see-also"></a>Consulte también  

[Detalles de diseño: Coste de inventario](design-details-inventory-costing.md)  
[Detalles de diseño: Liquidación de productos](design-details-item-application.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
