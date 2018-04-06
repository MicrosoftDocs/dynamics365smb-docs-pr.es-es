---
title: Fecha registro en movimientos de valores
description: "Aprender cómo el proceso Valorar stock - movs. producto identifica y asigna una fecha de registro a los movimientos de valor que creará."
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 11/23/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: b34f276a764f0e828fbc1f015429df9852242a4c
ms.openlocfilehash: 254d4451504c06091cd3fc5050f29da09db0de7f
ms.contentlocale: es-es
ms.lasthandoff: 03/22/2018

---
# <a name="design-details-posting-date-on-adjustment-value-entry"></a>Detalles de diseño: Fecha registro en el movimiento de valor de ajuste
Este artículo proporciona una guía para los usuarios de la funcionalidad Coste de inventario en [!INCLUDE[d365fin](includes/d365fin_md.md)]. El artículo específico proporciona una guía de cómo el proceso **Valorar stock - movs. producto** identifica y asigna una fecha de registro a los movimientos de valor que creará.  

Primero se revisa el concepto del proceso, cómo el proceso identifica y asigna una fecha de registro a los movimientos de valor que se crearán. A continuación, se comparten algunos ejemplos que encontramos en el equipo de soporte de vez en cuando y, finalmente, hay un resumen de los conceptos utilizados a partir de la versión 3.0.  

## <a name="the-concept"></a>El concepto  
Desde la versión 5.0, el proceso **Valorar stock - movs. producto** asigna una fecha de registro al movimiento de valor que creará en los pasos siguientes:  

1.  Inicialmente, la fecha de registro del movimiento que se creará es la misma que la del movimiento que ajusta.  

2.  La fecha de registro se valida con Periodos de inventario o Configuración de contabilidad.  

3.  Asignación de la fecha de registro; si la fecha inicial no se encuentra dentro del rango de fechas permitidas, el proceso asignará una Fecha de registro permitida en la Configuración de contabilidad o en el Período de inventario. Si en la Configuración de contabilidad se definen tanto los Períodos de inventario como las fechas de registro permitidas, se asignará al Movimiento del valor de ajuste la fecha posterior de los dos.  

 Revisemos este proceso más en la práctica. Supongamos que tenemos un movimiento de producto de venta. El producto se envió el 5 de septiembre de 2013 y se facturó el día después.  

![Movimiento producto: Formato de fecha: AAAA MM DD](media/helene/TechArticleAdjustcost1.png "TechArticleAdjustcost1")  

A continuación, el primer movimiento de valor (379) representa el envío y lleva la misma fecha de registro que el movimiento de valor principal.  

El segundo movimiento de valor (381) representan la factura.  

 El tercer movimiento de valor (391) es un ajuste del movimiento de valor de facturación (381)  

 ![Movimiento producto: Formato de fecha: AAAA MM DD](media/helene/TechArticleAdjustcost2.png "TechArticleAdjustcost2")  

 Paso 1: El movimiento de valor de ajuste que se creará tiene asignada la misma fecha de registro que el movimiento que ajusta, ilustrada anteriormente con el movimiento de valor 391.  

 Paso 2: Validación de la fecha de registro asignada inicial.  

El proceso **Valorar stock - movs. producto** determina si la fecha inicial de registro del movimiento de valor de ajuste está dentro del rango de fechas permitido según los Períodos de inventario o la Configuración de contabilidad.  

 Revisemos la venta mencionada anteriormente agregando la configuración de los rangos de fechas de publicación permitidos.  

 Periodos inventario:  

![Valorar stock - movs. producto](media/helene/TechArticleAdjustcost3.png "TechArticleAdjustcost3")

 La primera fecha de publicación permitida es el primer día del primer período abierto. 1 de septiembre de 2013.  

 Configuración de contabilidad:  

![Valorar stock - movs. producto](media/helene/TechArticleAdjustcost4.png "TechArticleAdjustcost4")

 La primera fecha de publicación permitida es la fecha indicada en el campo Permitir registro desde: 10 de septiembre de 2013.  

 Si en la Configuración de contabilidad se definen tanto los Períodos de inventario como las fechas de registro permitidas se definirá el rango de fechas de registro permitidas.  

 Paso 3: Asignación de una fecha de registro permitida;  

 La fecha de registro asignada inicial era el 6 de septiembre como se muestra en el paso 1. Sin embargo, en el segundo paso del proceso Valorar stock - movs. producto se identifica que la primera fecha de registro permitida es el 10 de septiembre y, por lo tanto, la asigna en el movimiento de valor de ajuste siguiente.  

 ![Valorar stock - movs. producto](media/helene/TechArticleAdjustcost5.png "TechArticleAdjustcost5")

 Ahora hemos revisado el concepto para asignar fechas de registro a los movimientos de valor creados por el proceso Valorar stock - movs. producto.  

 Continuaremos revisando algunos ejemplos que encontramos en el equipo de soporte de vez en cuando en relación con las fechas de registro asignadas al proceso Valorar stock - movs. producto y las configuraciones relacionadas.  

## <a name="scenarios"></a>Escenarios  

### <a name="scenario-i-posting-date-is-not-within-your-range-of-allowed-posting-dates"></a>Ejemplo I: "La fecha de registro no está comprendida en su periodo de fechas de registro permitidas..."  
 Este es un ejemplo en el que un usuario experimenta el mensaje de error mencionado cuando se ejecuta el proceso Valorar stock - movs. producto.  

 En la sección anterior, que describe el concepto de asignación de fechas de registro, la intención del trabajo Valorar stock - movs. producto es crear un movimiento de valor con la fecha de registro el 10 de septiembre.  

![Valorar stock - movs. producto](media/helene/TechArticleAdjustcost6.png "TechArticleAdjustcost6")

 Seguimos con la configuración del usuario:  

![Valorar stock - movs. producto](media/helene/TechArticleAdjustcost7.png "TechArticleAdjustcost7")

 El usuario en este caso tiene un rango de fechas de registro permitidas desde el 11 hasta el 30 de septiembre y, por lo tanto, no puede registrar el movimiento de valor de ajuste con fecha de publicación el 10 de septiembre.  

![Valorar stock - movs. producto](media/helene/TechArticleAdjustcost8.png "TechArticleAdjustcost8")

 El artículo [952996](https://mbs2.microsoft.com/Knowledgebase/kbdisplay.aspx?WTNTZSMNWUKNTMMYXUPYZQPOUXNXSPSYOQQYYMLUQLOYYMWP) de la Knowledge Base discute ejemplos adicionales relacionados con el mensaje de error mencionado.  

### <a name="scenario-ii-posting-date-on-adjustment-value-entry-versus-posting-date-on-entry-causing-the-adjustment-such-as-revaluation-or-item-charge"></a>Ejemplo II: La fecha de registro en el movimiento de valor de ajuste frente a la fecha de registro en el movimiento que causa el ajuste, como la revaluación o el cargo de producto.  

### <a name="revaluation-scenario"></a>Ejemplo de revaluación:  
 Requisitos previos:  

 Configuración de inventario:  

-   Variación existencias automát. = Sí  

-   Ajuste automático coste = Siempre  

-   Tipo cálculo cte. medio = producto  

-   Periodo coste medio = día  

 Configuración de contabilidad:  

-   Permitir registro desde = 1 de enero de 2014  

-   Permitir registro hasta = vacío  

 Configuración usuarios:  

-   Permitir registro desde = 1 de diciembre de 2013.  

-   Permitir registro hasta = vacío  

##### <a name="to-test-the-scenario"></a>Para probar el ejemplo  

1.  Crear PRUEBA de producto:  

     Unidad de medida base = PCS  

     Método de coste = promedio  

     Seleccione grupos de registro opcionales.  

2.  El diario de productos abierto crea y registra un línea como se indica a continuación:  

     Fecha registro = 15 de diciembre de 2013  

     Producto = PRODUCTO  

     Tipo movimiento = compra  

     Cantidad = 100  

     Precio unitario = 10  

3.  El diario de productos abierto crea y registra un línea como se indica a continuación:  

     Fecha = 20 de diciembre de 2013  

     Producto = PRODUCTO  

     Tipo movimiento = Ajuste negativo  

     Cantidad = 2  

4.  El diario de productos abierto crea y registra un línea como se indica a continuación:  

     Fecha = 15 de enero de 2014  

     Producto = PRODUCTO  

     Tipo movimiento = Ajuste negativo  

     Cantidad = 3  

5.  El diario de revaluación abierto crea y registra un línea como se indica a continuación:  

     Producto = PRODUCTO  

     Liq. por nº orden = seleccione el movimiento de compra registrado en el paso 2. La fecha de registro de la revaluación será la misma que la del movimiento que ajusta.  

     Prec. coste revaluado = 40  

 Se han registrado los siguientes movimientos de productos y de valor:  

![Valorar stock - movs. producto](media/helene/TechArticleAdjustcost9.png "TechArticleAdjustcost9")

 ![Valorar stock - movs. producto](media/helene/TechArticleAdjustcost10.png "TechArticleAdjustcost10")

 El proceso Valorar stock - movs. producto ha reconocido un cambio de costes y ha ajustado los ajustes negativos.  

 **Revisión de las fechas de registro en los movimientos de valor de ajuste creados:** la primera fecha de registro permitida con la que el proceso Valorar stock - movs. producto tiene que estar relacionado es el 1 de enero de 2014 tal como se indica en Configuración de contabilidad.  

 **Ajuste negativo en el paso 3:** la fecha de registro asignada es el 1 de enero, proporcionada por la Configuración de contabilidad. La fecha de registro del movimiento del valor para afrontar es el 20 de diciembre de 2013. Según la configuración de contabilidad, la fecha no se encuentra dentro del rango de fechas permitidas. Por lo tanto, la fecha de registro indicada en el campo Permitir registro desde en la Configuración de contabilidad se asigna al movimiento del valor de ajuste.  

 **Ajuste negativo en el paso 4:** la fecha de registro asignada es el 15 de enero. El movimiento de valor para afrontar tiene fecha de registro el 15 de enero, que se encuentra en el rango de fechas permitido en función de la configuración de contabilidad.  

 El ajuste realizado para el Ajuste negativo en el paso 3 es el que produce la discusión. La fecha de registro favorable para el movimiento del valor de ajuste habría sido el 20 de diciembre o al menos en diciembre, ya que la revaluación que causaba el cambio en el CV se registró en diciembre.  

 Para lograr el ajuste del Ajuste negativo en el paso 3 en diciembre, el campo Configuración de contabilidad, Permitir registro desde, debe indicar una fecha en diciembre.  

 **Conclusión:**  

 Con las experiencias de este ejemplo y si se tiene en cuenta la configuración más adecuada del rango de fechas de registro permitido para una empresa, la siguiente información puede ser útil: siempre que los cambios en el valor de inventario se puedan publicar en un período, en este caso en diciembre, la configuración que usa la empresa para los rangos de fechas de registro permitido debe estar alineada con esta decisión. El campo Permitir registro desde de la Configuración de contabilidad, que comienza el 1 de diciembre, permitirá que la revaluación realizada en diciembre se envíe a los movimientos salientes afectados en el mismo período.  

 Los grupos de usuarios a los que no se les permite publicar en diciembre pero sí en enero, que probablemente estaban destinados a estar limitados por la Configuración de contabilidad de este ejemplo, deberían repararse a través de la Configuración del usuario.  

### <a name="item-charge-scenario"></a>Ejemplo cargos producto:  
 Requisitos previos:  

 Configuración de inventario:  

-   Variación existencias automát. = Sí  

-   Ajuste automático coste = Siempre  

-   Tipo cálculo cte. medio = producto  

-   Periodo coste medio = día  

 Configuración de contabilidad:  

-   Permitir registro desde = 1 de diciembre de 2013.  

-   Permitir registro hasta = vacío  

 Configuración usuarios:  

-   Permitir registro desde = 1 de diciembre de 2013.  

-   Permitir registro hasta = vacío  

##### <a name="to-test-the-scenario"></a>Para probar el ejemplo  

1.  Crear cargo producto:  

     Unidad de medida base = PCS  

     Método de coste = promedio  

     Seleccione grupos de registro opcionales.  

2.  Crear un nuevo pedido de compra  

     Compra a-Nº proveedor: 10000  

     Fecha registro = 15 de diciembre de 2013  

     N.º factura proveedor: 1234  

     En la línea del pedido de compra:  

     Producto = CARGO  

     Cantidad = 1  

     Coste unitario directo = 100  

     Registrar recepción y factura.  

3.  Crear un nuevo pedido de venta:  

     Venta a-Nº cliente: 10000  

     Fecha registro = 16 de diciembre de 2013  

     En la línea del pedido de venta:  

     Producto = CARGO  

     Cantidad = 1  

     Precio venta = 135  

     Registrar, enviar y facturar.  

4.  Configuración de contabilidad:  

     Permitir registro desde = 1 de enero de 2014  

     Permitir registro hasta = en blanco  

5.  Crear un nuevo pedido de compra:  

     Compra a-Nº proveedor: 10000  

     Fecha registro = 2 de enero de 2014  

     N.º factura proveedor: 2345  

     En la línea del pedido de compra:  

     Cargo de producto = JB-FLETE  

     Cantidad = 1  

     Coste unitario directo = 3  

     Asignar cargo de producto al albarán de compra desde el paso 2.  

     Registrar albarán y factura.  

     ![Valorar stock - movs. producto](media/helene/TechArticleAdjustcost11.png "TechArticleAdjustcost11")

6.  En la fecha de trabajo 3 de enero llega una factura de compra que contiene un cargo adicional de producto en la compra realizada en el paso 2. Esta factura tiene fecha de documento el 30 de diciembre y, por lo tanto, se registre con Fecha de registro el 30 de diciembre de 2013.  

     Crear un nuevo pedido de compra:  

     Compra a-Nº proveedor: 10000  

     Fecha registro = 30 de diciembre de 2013  

     N.º factura proveedor: 3456  

     En la línea del pedido de compra:  

     Cargo de producto = JB-FLETE  

     Cantidad = 1  

     Coste unitario directo = 2  

     Asignar cargo de producto al albarán de compra desde el paso 2  

     Registrar albarán y factura.  

   ![Valorar stock - movs. producto](media/helene/TechArticleAdjustcost12.png "TechArticleAdjustcost12")

 El informe Valoración inventario se imprime a partir de fecha 31 de diciembre de 2013  

![Valorar stock - movs. producto](media/helene/TechArticleAdjustcost13.png "TechArticleAdjustcost13")

 **Resumen de ejemplo:**  

 El ejemplo descrito termina con un informe de Valoración inventario que demuestra Cantidad = 0 mientras que Valor = 2. El Cargo de producto publicado en el paso 11 es parte del valor de Entrada de existencias de diciembre, mientras que la Salida de existencias del mismo período no se ve afectada.  

 El hecho de tener la Configuración de contabilidad que indicaba Permitir registro desde el 1 de enero, fue ventajoso para el primer Cargo de producto. Los costes de la Entrada y Salida de existencias se registró en el mismo periodo. Sin embargo para el segundo cargo de producto, la configuración de contabilidad produce el cambio en el coste de ventas que se reconocerá en el periodo posterior.  

 **Conclusión:**  

 Es un desafío tener el informe de Valoración inventario para demostrar Cantidad = 0 mientras que Valor <> 0. En este caso, también es más difícil expresar la configuración óptima, ya que las facturas de compra llegan el mismo día pero abordan diferentes períodos e incluso ejercicios. Cambiar a un ejercicio nuevo generalmente requiere un poco de planificación y, como parte de eso, se debe tener en cuenta el conocimiento del proceso Valorar stock - movs. producto, que reconoce el CV.  

 En este ejemplo, una opción podría ser tener en la Configuración de contabilidad, en el campo Permitir registro desde, una fecha indicada en diciembre por un par de días más y posponer el registro del cargo por primer producto para permitir todos los costes del período o ejercicio anterior para que el período al que pertenecen primero los pueda reconocer, mientras se ejecuta el proceso Valorar stock - movs. producto y luego mover la fecha de registro permitida al nuevo período\/ejercicio. El primer cargo de producto con fecha de registro el 2 de enero podría registrarse.  

## <a name="history-of-adjust-cost--item-entries-batch-job"></a>Historial del proceso Valorar stock - movs. producto  
 A continuación, se incluye un resumen del concepto que asigna fechas de registro a los movimientos de valor de ajuste por proceso Valorar stock - movs. producto desde la versión 3.0.  

### <a name="from-version-30370a"></a>Desde la versión 3.0..3.70.A  
 En el formulario de solicitud del proceso Valorar stock - movs. producto, el usuario debe introducir una fecha de registro. El proceso ejecuta todos los cambios necesarios y crea movimientos de valor con la fecha de registro en el formulario de solicitud. La fecha de registro sugerida es la fecha de hoy.  

### <a name="version-370b40"></a>Versión 3.70.B..4.0  
 En el formulario de solicitud del proceso Valorar stock - movs. producto, el usuario debe introducir una fecha de registro de movimiento de período cerrado. El proceso ejecuta todos los cambios necesarios y crea movimientos de valor con la fecha de registro del movimiento del producto principal (fecha de envío de la venta que dirige el ajuste). Si la fecha de registro del movimiento del producto principal no se encuentra dentro del rango de fechas de registro permitidas, la fecha de registro de movimiento de período cerrado se asignará al movimiento de valor de ajuste. Se considera que una fecha se encuentra en un período cerrado cuando es anterior a la fecha del campo Permitir registro desde de la Configuración de contabilidad.  

### <a name="from-version-50"></a>Desde la versión 5.0:  
 Ya no debe introducirse una fecha de registro en el formulario de solicitud del proceso Valorar stock - movs. producto. El proceso ejecuta todos los cambios necesarios y crea movimientos de valor con la fecha de registro del movimiento de valor que ajusta. Si la fecha de registro no se encuentra dentro del rango de fechas permitidas, la fecha del campo Permitir registrar desde en Configuración contabilidad, o si se usan Periodos de inventario, se deberá usar la más reciente de las dos. Vea el concepto descrito anteriormente.  

## <a name="history-of-post-inventory-cost-to-gl-batch-job"></a>Historial del proceso Regis. variación existencias  
 El proceso Registrar variación existencias está estrechamente relacionado con Valorar stock - movs. producto, ya que su historial también se resume y comparte aquí.  

### <a name="from-version-30370a"></a>Desde la versión 3.0..3.70.A  
 En el formulario de solicitud del proceso Registrar variación existencias, el usuario debe introducir una fecha de registro. El proceso ejecuta todos los movimientos de valor del filtro, si los hay, y crea movimientos de contabilidad con la fecha de registro en el formulario de solicitud.  

### <a name="version-370b40"></a>Versión 3.70.B..4.0  
 En el formulario de solicitud del proceso Registrar variación existencias, está disponible el campo fecha de registro de movimiento de período cerrado. El programa usa la fecha especificada en este campo como la fecha de registro de los movimientos de contabilidad que crea para los movimientos de valor cuyas fechas de registro están en periodos contables cerrados. De lo contrario, los movimientos de contabilidad tendrán la misma fecha de registro que los movimientos de valor originales. Se considera que una fecha se encuentra en un período cerrado cuando es anterior a la fecha del campo Permitir registro desde de la Configuración de contabilidad. Si registran en contabilidad por grupo contable, los movimientos de contabilidad generales tendrán la fecha de registro que se especifica en el campo Fecha registro del formulario de solicitud.  

 En la versión 3 y 4 el proceso se buscan todos los movimientos de valor para averiguar si hay alguno donde el Importe de coste (Real) sea diferente del Coste registrado en contabilidad. Si hay una diferencia, el importe diferente se registrará en un movimiento de contabilidad. Si se utiliza el registro de costes esperado, los campos correspondientes se procesarán del mismo modo.  

![Valorar stock - movs. producto](media/helene/TechArticleAdjustcost14.png "TechArticleAdjustcost14")

### <a name="from-version-50"></a>Desde la versión 5.0:  
 Ya no debe introducirse una fecha de registro en el formulario de solicitud del proceso Registrar variación existencias. El movimiento de contabilidad se crea con la misma fecha de registro que los movimientos de valor relacionados. Para completar el proceso, el rango de fechas de registro permitidas debe permitir la Fecha de registro del movimiento de contabilidad creado. De lo contrario, el rango de fechas de registro permitidas debe volver a abrirse temporalmente cambiando o eliminando las fechas en los campos Permitir registro desde y en la Configuración de contabilidad. Para evitar errores de conciliación es necesario que fecha de registro del movimiento de contabilidad se corresponda con la fecha de registro del movimiento de valor.  

 El proceso escanea la Tabla 5811 - Registrar movimiento valor en C/G para identificar los movimientos de valor en el ámbito para registrar en la Contabilidad. Después de una ejecución correcta, la tabla se vacía.  

 Son bienvenidos todos los comentarios sobre cómo este proceso y la documentación pueden desarrollarse más a fondo.  

 Helene Holmin  

 Ingeniero de escalación de Dynamics NAV  

## <a name="see-also"></a>Consulte también  
[Detalles de diseño: Coste de inventario](design-details-inventory-costing.md)  
[Detalles de diseño: Liquidación de productos](design-details-item-application.md)  

