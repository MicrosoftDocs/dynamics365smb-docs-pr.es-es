---
title: Acerca del cálculo de coste estándar
description: Un sistema de costes estándar determina el coste unitario del inventario en función de costes históricos o esperados razonables.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.form: 5841
ms.author: bholtorf
ms.date: 10/10/2023
ms.service: dynamics-365-business-central
---
# Acerca del cálculo de coste estándar

Muchas empresas de fabricación eligen una base de valoración de coste estándar. Esto también se aplica a las empresas que llevan a cabo la fabricación ligera, como ensamblado y kitting. Un sistema de costes estándar determina el coste unitario del inventario en función de ciertos costes históricos o esperados razonables. Los estudios sobre costes anteriores y sobre costes futuros previstos pueden ofrecer una base para calcular costes estándar. Dichos costes quedan fijos hasta que se tome la decisión de cambiarlos. El coste real para fabricar un producto puede ser diferente de los costes estándar calculados. Para controlar la gestión, el coste real se compara con el coste estándar de un producto en particular, y se identifican y analizan las diferencias o *variaciones*.  

Los costes estándar se pueden mantener para los productos que se rellenan con la compra, el ensamblado y la producción. Para cada método de reaprovisionamiento, el coste estándar puede constar de los elementos siguientes.  

|Sistema reposición|Elementos de coste estándar|  
|--------------------------|----------------------------|  
|**Compras**|El coste directo de material y el coste general de material son necesarios.|  
|**Ensamblado**|Coste directo del material, coste directo o de mano de obra fija y coste general.|  
|**Ord. prod.**|Coste directo del material, coste de mano de obra, coste de subcontratista y coste general.|  

## Configuración de los costes estándar

Dado que el coste estándar de un producto fabricado o ensamblado puede incluir diversos elementos de coste, entre ellos, costes de materiales, de capacidad (mano de obra) y de subcontratistas, ya sean directos o generales, deben establecerse los costes estándar para cada uno de estos elementos.  

La tarea contable que debe llevar a cabo una empresa de producción que utilice un sistema de costes estándar es:  

- Calcular un coste estándar del producto acabado y configurarlo en la ficha respectiva.  
- Registrar y asignar el coste real de los elementos de coste clave y considerar las variaciones.  

Para determinar el coste directo de un producto acabado, es necesario totalizar los costes de todos los componentes. Un producto ensamblado o fabricado puede incluir subensamblados, que también constan de varios componentes.  

Los elementos de coste claves siguientes conforman el coste directo total de un producto procesado acabado:  

- Costes de materiales.  
- Costes de capacidad.  
- Costes de subcontratistas para los productos fabricados solo.  

### Costes materiales

Los costes de materiales son aquellos que se asocian con productos semiterminados y materias prima que se hayan comprado. El coste unitario del material puede estar compuesto por elementos de coste directos e indirectos.  

- El coste directo del material representa la cantidad facturada por las materias primas que se hayan comprado o por el coste de procesamiento de un producto semiterminado.  
- El coste indirecto del material, o *costes generales*, puede representar elementos tales como costes de merma de existencias del producto acabado después de producido.  

La configuración del coste de materiales para los productos comprados que afectan los costes directos e indirectos depende del método de valoración que haya seleccionado para el producto en cuestión. Puede configurar la información relativa al coste para cualquiera de los métodos en la ficha de producto. Para obtener más información, vea [Registrar nuevos productos](inventory-how-register-new-items.md).

El coste del rechazo (solo producción) es un factor adicional que debe tenerse en cuenta cuando se calcula el coste material total. Cuando se rechaza una cierta cantidad de las materias primas al ensamblar o fabricar un producto, normalmente conlleva un aumento en el número de componentes que se requieren para la producción. Esto incrementa el coste de materiales de los componentes que se consumen al fabricar un producto principal. Puede configurar el coste del rechazo de materiales en la L.M. de producción o en la ruta.  

El coste de materiales de un producto fabricado se puede representar de dos formas, que se corresponden con las siguientes bases de cálculo de coste:  

|Base de cálculo de coste|Cálculo de coste de material|  
|----------------------------|-------------------------------|  
|Un nivel|El producto fabricado es igual al coste total de todos los productos comprados o subensamblados en la L.M. de producción de dicho producto.|  
|Nivel o multinivel distribuido|El producto fabricado representa la suma del coste de materiales de todos los productos semiterminados en la L.M. de ese producto y el coste de todos los productos comprados en la L.M. de producción de ese producto.|  

### Costes de capacidad

Los costes de capacidad son aquellos que están asociados con la mano de obra interna y con los costes de maquinaria. Debe configurar estos costes para cada recurso (en la administración de ensamblados) y trabajo o centro de máquina en la ruta (en la producción). Al igual que con los materiales, puede identificar los elementos directos e indirectos de los costes de capacidad. Por ejemplo, el coste directo para un centro de trabajo podría ser la tasa de planta establecida para llevar a cabo una función específica. El coste indirecto para un centro de trabajo puede representar ciertos gastos de la fábrica, como iluminación, calefacción, etc. Al igual que los costes de materiales, puede expresar el coste general de capacidad como un porcentaje de coste indirecto o como una tasa general fija.  

En la configuración de los costes de capacidad de los productos ensamblados, están implicados los siguientes elementos:  

- Coste unitario directo e indirecto del recurso.  
- Tipo fijo o directo de utilización de recursos.  

En la configuración de los costes de capacidad de los productos fabricados, están implicados los siguientes elementos:  

- Coste unitario directo e indirecto del centro de trabajo o de máquina.  
- La configuración del tiempo y del tamaño del lote.  

Para calcular el coste de capacidad estándar, deberá establecer cuáles son las tiempos estándar requeridos para llevar a cabo las operaciones con las máquinas y los trabajos en los centros. Normalmente, el tiempo total necesario para completar una operación consta del tiempo de preparación, de ejecución, y de espera y traslado.  

Puede configurar las tasas para cada tipo de tiempo por cada máquina o centro de trabajo de una ruta en particular.  

> [!NOTE]  
>  Mientras las tasas de tiempo de ejecución se aplican para cada unidad de producto fabricado, las tasas de tiempo de preparación se aplican para cada lote. Por tanto, debe prorratear el tiempo de preparación de la ruta por cada operación en función del tamaño del lote. Puede especificar el tamaño del lote en el campo correspondiente de la ficha desplegable **Reposición** de la página **Ficha de producto**.  

Para especificar el tiempo de preparación en la ruta por motivos de planificación, pero no incluir este gasto en el cálculo del coste estándar, desactive el campo **Coste incl. preparación** de la página **Configuración fabricación**.  

En el caso de un solo nivel, se trata del coste de mano de obra requerido para fabricar el producto final y se especifica en la ruta de producción del producto. En el caso de varios niveles, se trata del coste de capacidad que se especifica para cada producto que se fabrica individualmente que se incluye en la L.M. del producto principal.  

### Costes de los subcontratistas

Los costes de subcontratistas son aquellos asociados con los servicios que ofrecen los fabricantes o los subcontratistas externos de una empresa. De forma similar a los materiales y a la capacidad, los costes de subcontratistas pueden estar compuestos por cantidades directas y generales. Los costes directos de subcontratistas representan el cargo efectivo por cada unidad de servicio prestado. Por ejemplo, los costes generales de subcontratistas pueden representar costes de transporte y manipulación en los que incurre la empresa con un pedido que se ha subcontratado.  

Dado que la subcontratación es una capacidad externalizada, puede configurar el coste de los servicios subcontratados tanto directos como indirectos en la ficha del centro de trabajo que representa la operación de subcontratación.  

## Actualización de los costes estándar

Para actualizar o calcular el coste estándar de elementos de ensamblado, use la función de la ficha de producto.  

El proceso de actualizar o calcular los costes estándar normalmente consiste en las siguientes tareas:  

1.  La actualización de costes en los niveles de componente y de capacidad. Para obtener más información, consulte los procesos **Sugerir coste estándar prod.** y **Sugerir coste estándar capacidad**.  
2.  Consolidación y distribución de los costes de componentes y de la capacidad para calcular el coste total de fabricación o montaje de los productos. Para obtener más información, consulte la sección [Para calcular el coste estándar de un elemento de ensamblado](assembly-how-work-assembly-boms.md#to-calculate-the-standard-cost-of-an-assembly-item).  
3.  La implementación de los costes estándar que se introducen al ejecutar los procesos por lotes anteriores. Los costes estándar no tienen efecto hasta que se implementan. Use el trabajo por lotos **Implementar cambios de coste estándar** que actualiza los cambios en el coste estándar en los artículos con los de la tabla de la Hoja de trabajo de coste estándar.  
4.  Implementación de los cambios para actualizar el campo **Coste unitario** en la ficha del producto y realizar una revalorización de inventario. Para obtener más información, vea [Revaluación de inventario](inventory-how-revalue-inventory.md).

## Usar trabajos por lotes para actualizar los costes estándar
Las siguientes secciones describen los trabajos por lotes que puede utilizar para actualizar los costes estándar.
### Sugerir coste estándar prod.

 Crea propuestas para modificar los costes y el reparto de costes de los costes estándar en las fichas de producto. Una vez finalizado el proceso, podrá ver el resultado en la ventana Hoja trab. coste estándar.

> [!NOTE]  
> Este trabajo por lotes está pensado para los productos comprados solamente. Si desea actualizar un producto con una L.M. de producción o una L.M. de ensamblado, primero deberá rellenar la hoja de trabajo con todos los componentes y, a continuación, ejecutar el trabajo por lotes Distribuir coste estándar.

Este proceso sólo crea sugerencias. No procesa los cambios sugeridos. Si está de acuerdo con dichas sugerencias y desea aplicarlas, es decir, actualizarlas en las fichas de producto e insertarlas en el Diario de revalorización, seleccione en Implementar cambios de coste estándar en la ventana Hoja trab. coste estándar.
#### Opciones

**Coste estándar**: Introduzca el factor de ajuste que desea utilizar para actualizar el coste estándar. También puede seleccionar un método de redondeo para el nuevo coste estándar. Tiene que rellenar el campo con un valor decimal para el aumento de porcentaje, por ejemplo 1,1.

**% Coste indirecto**: especifique el factor de ajuste que desea utilizar para actualizar el % de coste indirecto. También puede seleccionar un método de redondeo para el nuevo % de coste indirecto. Tiene que rellenar el campo con un valor decimal para el aumento de porcentaje, por ejemplo 1,1.

**Tasa costes generales**: especifique el factor de ajuste que desea utilizar para actualizar la tasa de costes generales. También puede seleccionar un método de redondeo para la nueva tasa de costes generales. Tiene que rellenar el campo con un valor decimal para el aumento de porcentaje, por ejemplo 1,1.

### Sugerir coste estánd. c. trab./máq.

Crea propuestas para modificar los costes y el reparto de costes de los costes estándar en el centro de trabajo, centro de máquina o tarjetas de recursos. Una vez finalizado el proceso, podrá ver el resultado en la ventana **Hoja trab. coste estándar**.

Este proceso sólo crea sugerencias. No procesa los cambios sugeridos. Si está de acuerdo con dichas sugerencias y desea aplicarlas, es decir, actualizarlas en las fichas de recurso y el centro de trabajo/máquina e insertarlas en la ventana del Diario de revalorización, seleccione en **Implementar cambios de coste estándar** en la ventana **Hoja trab. coste estándar**.

Una vez ejecutado el trabajo por lotes, si desea ver el impacto en su producción o en los departamentos de ensamblado, puede ejecutar el trabajo por lotes **Distribuir coste estándar** para actualizar los costes estándar en los centros de trabajo, los centros de máquina, los recursos de ensamblado, las L.M. de producción y las L.M. de ensamblado.
#### Opciones
**Coste estándar**: Introduzca el factor de ajuste que desea utilizar para actualizar el coste estándar. También puede seleccionar un **método de redondeo** para el nuevo coste estándar. Tiene que rellenar el campo con un valor decimal para el aumento de porcentaje, por ejemplo 1,1.

**% Coste indirecto**: especifique el factor de ajuste que desea utilizar para actualizar el % de coste indirecto. También puede seleccionar un método de redondeo para el nuevo % de coste indirecto. Tiene que rellenar el campo con un valor decimal para el aumento de porcentaje, por ejemplo 1,1.

**Tasa costes generales**: especifique el factor de ajuste que desea utilizar para actualizar la tasa de costes generales. También puede seleccionar un método de redondeo para la nueva tasa de costes generales. Tiene que rellenar el campo con un valor decimal para el aumento de porcentaje, por ejemplo 1,1.

### Regis. variación existencias

 Registra los cambios de cantidad y valor del inventario en los movimientos de producto y en los movimientos de valor, respectivamente, al registrar transacciones de inventario, como albaranes de ventas o recibos de compra.

A menos que haya activado la casilla **Variación existencias automát.** en la ventana **Configuración del inventario**, los costes de inventario no se registran dinámicamente en la contabilidad y el CV no se calcula en relación con una venta. Por tanto, debe registrar a la contabilidad manualmente mediante la ejecución del trabajo por lotes **Reg. var. inventario en cont.** para actualizar la contabilidad y potencialmente de imprimir un informe de los movimientos de valor que se registran.

El proceso utiliza movimientos de valor como base. Para calcular el valor que se debe registrar, usa la diferencia entre el campo **Importe coste (real)** e **Imp. registrado contabilidad** de los movimientos de valor. Si activó la casilla **Registro de coste previsto en contabilidad** en la ventana **Configuración del inventario**, el trabajo por lotes también registra la diferencia entre el campo **Importe coste (Esperado)** y el campo **Exp. Coste registrado en la contabilidad** en cuentas provisionales de la contabilidad.

> [!NOTE]
> Si no activó la casilla **Registro de coste previsto en contabilidad** en el campo de la ventana **Configuración del inventario**, la sección última del informe enumerará los movimientos de valor que se omiten porque representan costes esperados.

> [!NOTE] 
> Si el trabajo por lotes encuentra algún error relacionado con las dimensiones o la configuración de las dimensiones, éste invalidará el error y registrará el movimiento en la contabilidad con las dimensiones del movimiento de valor.

Si desea asegurarse de que el trabajo por lotes no encuentre ningún error mientras se ejecuta el trabajo por lotes, puede ejecutar el informe **Reg. var. ex. en cont. - Test** para ver todos los errores que se podrían encontrar. Así, puede corregirlos y ejecutar el proceso **Regis. variación existencias**, sabiendo que será capaz de procesar todos los movimientos.
 
> [!IMPORTANT]  
> Antes de ejecutarlo, debería utilizar el proceso **Ajustar coste: movimientos de producto**. Esto garantiza que, al ejecutarlo, los costes que se registrarán en el módulo de contabilidad estarán actualizados.
#### Opciones

|Opción  |Descripción  |
|--------------|---------|
|**Método registro**|el proceso puede registrar los valores del inventario en el módulo de contabilidad por grupo contable o por movimiento registrado. Si decide registrar por movimiento, conseguirá unas especificaciones detalladas acerca de cómo el inventario afecta al módulo de contabilidad, aunque también obtendrá numerosos movimientos de contabilidad. Si decide registrar por grupo contable, el trabajo por lotes creará un movimiento de contabilidad por cada combinación de fecha de registro y grupo contable. Esto significa que se crea un movimiento de contabilidad por cada combinación de fecha de registro, grupo contable del negocio, grupo contable del producto, grupo contable del inventario y código de almacén. Además, el trabajo por lotes creará movimientos de contabilidad separados para aquellos costes que tengan un signo diferente.|
|**Nº documento**|introduzca en este campo un número de documento si ha elegido la opción Por grupo contable stock. El número de documento aparecerá en los movimientos registrados.|
|**Registrar**|Active este campo si desea que el trabajo por lotes registre automáticamente en la contabilidad. Si no desea registrar la variación de existencias, el proceso sólo imprimirá un informe de test que mostrará los valores que se pueden registrar en el módulo de contabilidad y en el informe aparecerá: **Informe test (no registrado)**.|

### Distribuir coste estándar

Distribuye los costes estándar de productos montados y fabricados. En ellos influirá el cambio en los costes estándar de componentes sugeridos por el trabajo por lotes **Sugerir coste estándar prod.**. Además, también influirán en ellos el cambio del coste estándar de los recursos de la capacidad de producción y de ensamblado sugeridos por el proceso **Sugerir coste estánd. c. trab./máq.**.

Una vez ejecutado uno o ambos trabajos por lote, y realizada la distribución, todos los cambios en los costes estándar de la hoja de trabajo se introducen en las listas de materiales de ensamblado o producción asociadas, y los costes se aplican a cada nivel de la lista de materiales.

> [!NOTE] 
> Esta característica solo distribuye el coste estándar en fichas de productos, no en las fichas SKU.

Este proceso sólo crea sugerencias. No procesa los cambios sugeridos. Si está de acuerdo con dichas sugerencias y desea aplicarlas, es decir, actualizarlas en las fichas de producto e insertarlas en la ventana del **diario de revalorización**, puede utilizar el trabajo por lotes **Implementar cambio coste estándar**. Tiene acceso a este trabajo por lotes desde la ventana de **Hoja trab. coste estándar**.
#### Opciones

**Fecha cálculo**: Introduzca la fecha que corresponda a la versión de la lista de materiales de producción para la que desea realizar la distribución.
 
### Implementar cambio coste estándar

Actualiza los cambios de coste estándar de la tabla **Producto** con los de la tabla **Hoja trab. coste estándar**. Se pueden crear y modificar las sugerencias de cambios de coste utilizando el proceso **Sugerir coste estándar prod.** o **Sugerir coste estánd. c. trab./máq.** Se transfiere el contenido de todos los campos de las sugerencias de cambio de coste estándar. Al aplicar sugerencias de cambios de costes estándares, puede verlos en la ficha de producto y/o en las fichas de centro de trabajo o centro de máquina. También se crea un diario de revalorización para actualizar el valor de existencias existente.
#### Opciones

**Fecha registro**: Introduzca la fecha en que debe realizarse la revalorización.

**N.º de documento**: Introduzca el número de las líneas del diario de revalorización. Si hay un número de serie configurado en el nombre de sección del diario de productos, el número de documento seguirá a los movimientos realizados mediante el registro del diario de revalorización. En caso contrario, puede introducir un número de forma manual.

**Libros diario producto**: Introduzca el nombre del libro diario de revalorización.

**Nombre secc. diario prod.**: Introduzca el nombre del diario de revalorización actual.

Elija **Aceptar** para iniciar el trabajo por lotes. Si no desea ejecutar el proceso en este momento, seleccione **Cancelar** para cerrar la ventana.

## Consulte también .

[Detalles de diseño: métodos de coste](design-details-costing-methods.md)  
[Actualizar costes estándar](finance-how-to-update-standard-costs.md)  
[Detalles de diseño: Coste de inventario](design-details-inventory-costing.md)  
[Trabajar con L.M. de ensamblado](assembly-how-work-assembly-boms.md)  
[Crear LM de producción](production-how-to-create-production-boms.md)  
[Trabajar con listas de materiales](inventory-how-work-BOMs.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
