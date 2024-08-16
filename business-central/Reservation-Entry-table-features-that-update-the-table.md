---
title: 'Tabla de entrada de reservas: características que actualizan la tabla de entrada de reservas | Microsoft Docs'
description: Esto proporciona orientación para ayudarlo a comprender y solucionar problemas de inconsistencia de datos en la tabla de entrada de reserva.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.date: 06/26/2024
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---

# <a name="reservation-entry-table---introduction"></a>Mesa de entrada de reservas - Introducción

Este documento técnico proporciona orientación para ayudarlo a comprender y solucionar problemas de inconsistencia de datos en la tabla de  *Entrada de reserva* (Tabla 337) en Microsoft Dynamics NAV. La primera parte es una introducción a las características que generan o modifican datos en esta tabla. También cubre varios campos en la tabla de  *Entrada de Reserva*  que vale la pena destacar en relación con estas características. La segunda parte demuestra mediante ejemplos cómo se generan, eliminan o modifican las entradas en la tabla  *Entrada de reserva*  cuando se procesan órdenes de transferencia o se ejecutan funciones de planificación.

La tabla de  *Entrada de reserva*  se utiliza para manejar y almacenar información relacionada con reservas, seguimiento de artículos y seguimiento de pedidos.

Al gestionar el seguimiento de artículos con contabilización parcial, la tabla funciona junto con la tabla de  *Especificación de seguimiento*  (Tabla 336). Los datos ingresados en la página  **Líneas de seguimiento de artículos**  por el usuario se crean en una versión temporal de la tabla 336 y se confirman en la tabla 337 y en la tabla de especificaciones de seguimiento cuando se cierra la página.

En términos generales, los datos generados en la tabla de  *Entrada de reserva*  dependen de las funciones que utilice y de los parámetros que haya seleccionado en el artículo tarjeta. Éstas incluyen:

- Política de seguimiento de pedidos
- Política de reservas
- Funciones de planificación ejecutadas
- Política de reordenamiento y fabricación
- Parámetros de planificación del artículo o unidad de stock tarjeta
- Cód. seguim. prod.

## <a name="features-that-update-the-reservation-entry-table"></a>Características que actualizan la tabla de Entrada de Reservas

### <a name="order-tracking-policy"></a>Política de seguimiento de pedidos

Si el campo  **Política de seguimiento de pedidos**  de un artículo está configurado en Ninguno, Microsoft Dynamics NAV nunca se crearán entradas de reserva en la tabla  *Entrada de reserva*, a menos que se ejecute el Plan de cambio neto o el Plan regenerativo, la Reserva o el Seguimiento de artículos. Además, sin el seguimiento de pedidos habilitado, puede tener entradas de reserva al utilizar las políticas de fabricación bajo pedido o de ensamblaje bajo pedido.

Puede considerar establecer la  **Política de seguimiento de pedidos**  en Ninguna si no necesitará rastrear sobre la marcha una demanda contra un suministro o viceversa. El seguimiento de la oferta frente a la demanda se gestiona mediante la funcionalidad de seguimiento de pedidos o el motor de planificación. No recomendamos que utilice el seguimiento de pedidos junto con la funcionalidad de planificación.

Cuando se establece el campo  **Política de seguimiento de pedidos**  en Solo seguimiento, Microsoft Dynamics NAV siempre se crearán entradas en la tabla 337 cada vez que se cree un pedido para el artículo, pero el  **Estado de reserva**  en la tabla 337 no siempre se establece estrictamente en Seguimiento. Consideremos el siguiente escenario:

> [!NOTE]  
> La fecha de trabajo se establece como 23/01/2014 (MM/DD/AAAA) para todos los ejemplos. 
  
1. Cree un artículo con el campo  **Política de seguimiento de pedidos**  establecido en Solo seguimiento.  
1. Cree un pedido de compra. Microsoft Dynamics NAV creará una entrada de reserva con el  **Estado de reserva** de Excedente, ya que la orden de compra aún no está asignada a una demanda.
1. Cree un pedido de ventas. Microsoft Dynamics NAV Ahora creará otra entrada de reserva con un  **Estado de reserva** de Seguimiento.

El  **Estado de la reserva** creado en paso 2 se actualizará a Seguimiento; esto se maneja  Microsoft Dynamics NAV automáticamente. Este concepto se llama seguimiento dinámico.
Al configurar el campo  **Política de seguimiento de pedidos**  en el artículo en Solo seguimiento, un usuario final puede utilizar la función de seguimiento de pedidos para obtener una descripción general de a qué suministro se asigna la demanda y viceversa.

> [!NOTE]  
> La funcionalidad de seguimiento no reemplaza la funcionalidad de planificación, que considera todos los artículos, demandas y suministros juntos para proporcionar propuestas de planificación óptimas para optimizar los niveles de servicio al cliente y equilibrar los niveles de inventario.

### <a name="reservation-policy"></a>Política de reservas

Una reserva consta de un par de registros en la tabla  *Entrada de reserva* con un  **Estado de reserva** de Reserva, que comparte el mismo número de entrada. Un registro tiene el campo Positivo habilitado y apunta al suministro. El otro registro tiene el campo  **Positivo** no habilitado y apunta a la demanda. Los campos **Tipo de fuente**, **N.º de referencia de fuente** y **ID de fuente** resaltan la reserva vincular entre la demanda y la oferta.

La información en el campo **Tipo de fuente** es la tabla con la que está relacionado el campo **Número de entrada**  de reserva. Por ejemplo, si se trata de una entrada de demanda (negativa), entonces podría ser la tabla de  *Órdenes de venta*  (Tabla 37) o el  *Componente de planificación*  (Tabla 99000829).

El campo  **ID de fuente**  contiene el ID del documento en la tabla a la que hace referencia el Tipo de fuente.

La **Fuente Ref. No.** El campo contiene un número de referencia para la línea en la que se realizó la reserva. **Entrada N°**  está relacionado con. Si la entrada está relacionada con una línea de venta o compra, una línea de diario o una línea de requisición, la información en este campo se copia de la **Línea Nro.** . Si está relacionado con una entrada en la tabla  *Entrada de libro mayor de artículos*  (Tabla 32), la información en este campo se copia del campo  **N.º de entrada**  de la tabla  *Entrada de libro mayor de artículos* .

Cuando se utiliza la opción de política de reserva Siempre en combinación con el seguimiento de pedidos, normalmente ambas están sincronizadas. Sin embargo, cuando se elimina la reserva o la fecha de recepción del suministro se adelanta más allá de la fecha de vencimiento de la demanda, se eliminará el seguimiento de pedidos. También puede aparecer un mensaje de error que le pregunta qué hacer con las reservas existentes. Microsoft Dynamics NAV  Este escenario se ilustra en el siguiente ejemplo:

1. Crea un nuevo elemento llamado COMP. Establezca los siguientes campos:
  - **Sistema de reposición**: Compra
  - **Política de seguimiento de pedidos: Solo seguimiento**
  - **Reservar**: Siempre
2. Crea un segundo elemento llamado FG. Establezca los siguientes campos:
  - **Sistema de reposición**: Orden de producción
  - **Política de seguimiento de pedidos: Solo seguimiento**
  - **Reservar**: Siempre
3. Crea un segundo elemento llamado FG. Establezca los siguientes campos:
  - **Artículo**: COMP
  - **Cantidad por**: 1
4. Certificar el BOM de Producción No. BOM FG y asignarlo al Artículo FG.
5. Cree un pedido de compra. Establezca los siguientes campos:
  - **Artículo**: COMP
  - **Cantidad: 10**
  - **Código de ubicación**: AZUL
  - **Fecha de recepción prevista: 24/01/2014**
6. Cree un pedido de ventas. Establezca los siguientes campos:
  - **Fecha de envío: 14/02/2014**
  - **Código de ubicación: AZUL**
  - **Artículo**: COMP
  - **Cantidad: 10**

> [!NOTE]  
> Se ha ejecutado una reserva automática entre la orden de compra y la orden de venta. Además, se ha creado un seguimiento de pedidos entre las órdenes de compra y venta.

7. Crear una orden de producción lanzada manualmente. Establezca los siguientes campos:
  - **Artículo**: 14/02/2014
  - **Cantidad: 10**
  - **Ubicación: AZUL**
  - **Fecha de entrega: 01/02/2014**
8. En la pestaña  **Inicio**, en el grupo Proceso, seleccione  **Actualizar orden de producción**.
9. Abra la lista de componentes y busque el elemento COMP.

> [!NOTE]  
>  Microsoft Dynamics NAV no crea ninguna reserva ni seguimiento de pedidos. El motivo es que ya existe una reserva contra la orden de venta creada en paso 6.

Supongamos que, por razones comerciales, el artículo se necesita con mayor urgencia en la orden de producción liberada creada en paso 7. A continuación, en los siguientes pasos, Listo la reserva de la orden de venta que se creó en paso 6 y observamos cómo se maneja el seguimiento de la orden.

10. Busque la orden de venta del artículo COMP de paso 6 y Cancelar la reserva.
11. Abra la orden de compra de paso 5 y observe que ahora se crea un seguimiento de pedido entre la orden de compra y el componente necesario de la orden de producción lanzada.
12. Recrear la reserva entre el componente necesario de la orden de producción liberada y el suministro de la orden de compra en paso 5.

> [!NOTE]  
> La reserva no se vuelve a crear, por lo que es necesario hacerlo manualmente.

13. Cambie el campo  **Fecha de recepción esperada**  en el encabezado de la orden de compra en paso 5 del 24/01/2014 al 05/02/2014.

Microsoft Dynamics NAV Mostrará el siguiente mensaje de advertencia:

   Existen reservas para esta Orden. Estas reservas se cancelarán si este cambio genera un conflicto de datos. ¿Desea continuar?

14. Elija Sí. Consulte las entradas de reserva y seguimiento de pedidos de la orden de compra.

> [!NOTE]  
> La reserva existente está cancelada y será necesario volver a crearla manualmente. El orden, sin embargo, es dinámico y ha sido recreado para existir entre la orden de compra y la orden de venta. Microsoft Dynamics NAV  El motivo es que la demanda de la orden de producción liberada (01/02/2014) es anterior a la fecha prevista de recepción del suministro.

Con esto concluye la demostración de la interacción entre el uso de reservas automáticas y el seguimiento de pedidos. Los ejemplos también muestran lo que sucede cuando se modifican las fechas de vencimiento y el mensaje de error que se activa cuando hay un conflicto de reserva.

### <a name="planning-calculated"></a>Planificación calculada

La planificación Listo mediante la planificación de pedidos, la hoja de trabajo de requisición o la hoja de trabajo de planificación generará entradas en la tabla  *Entrada de reserva*  con el campo  **Estado de reserva**  establecido en Seguimiento, Reserva o Excedente. Siempre debe haber un par coincidente con el mismo número de entrada de valor positivo y negativo en el campo  **Cantidad (Base)**  cuando el estado sea Seguimiento o Reserva. El campo  **Tipo de fuente**  será el tipo de demanda, es decir, la tabla 37 para la cantidad negativa y una tabla de planificación, por ejemplo, la tabla 246, para la cantidad positiva. El campo  **ID de fuente**  será PLANIFICACIÓN.

En el caso de oferta o demanda no asignada, Microsoft Dynamics NAV establecerá el campo **Estado de reserva**  en Excedente. Por ejemplo, puede tener un estado de reserva de Excedente cuando el inventario existente está por debajo de la cantidad de stock de seguridad o la demanda está vinculada al pronóstico.

La tabla  *Elemento de planificación sin seguimiento*  (Tabla 99000855) contiene información sobre las cantidades sin seguimiento que se muestran cuando el usuario realiza una búsqueda en la página de seguimiento de pedidos para ver las cantidades sin seguimiento o elige un ícono de advertencia en la hoja de cálculo de planificación. La tabla contiene entradas que representan una cantidad excedente no rastreada en la red de seguimiento de pedidos.

Estas entradas se generan durante la ejecución de la planificación y explican la procedencia de dicha cantidad en las líneas de seguimiento de pedido. La procedencia de este excedente sin seguimiento puede ser:

- Previsión de producción
- Pedidos abiertos
- Stock de seguridad
- Punto de pedido
- Stock máximo
- Cantidad a solicitar
- Cantidad máxima pedido
- Cantidad mínima pedido
- Múltiplos de pedido
- Amort. (% tamaño lote)

En la tabla de  *Entrada de Reserva*, al igual que en las órdenes de Compra, Transferencia y Producción, hay un campo de  **Flexibilidad de Planificación** . Este campo de opción define si el suministro representado por estas órdenes de suministro es considerado por el sistema de planificación al calcular los Mensajes de Acción. Si el campo contiene la opción Ilimitado, entonces el sistema de planificación incluye la línea al calcular Mensajes de Acción. Si el campo contiene la opción Ninguna, entonces la línea es firme e inmutable, y el sistema de planificación no incluye la línea al calcular los Mensajes de Acción. La función se administra en la tabla  *Entrada de reserva*  mediante el campo con el mismo nombre.

### <a name="reordering-and-manufacturing-policy"></a>Política de reordenamiento y fabricación

Si se ejecuta una función de planificación para un conjunto de artículos con la Política de reordenamiento establecida en Pedido, se crearán entradas en la tabla de  Microsoft Dynamics NAV Entrada de reserva *con el estado de reserva del tipo Reserva en lugar de Seguimiento.* 

Los campos  **Tipo de fuente** e  **ID de fuente**  tendrán el tratamiento equivalente a otras políticas de reordenamiento. Sin embargo, en el campo  **Enlace**  de la tabla  *Entrada de reserva*, Microsoft Dynamics NAV se ingresará Pedido a pedido.

El campo  **Vinculación**  se completa para controlar las órdenes de suministro que están vinculadas a una demanda específica, por ejemplo, las órdenes de producción que se crean directamente a partir de una orden de venta. El campo muestra Pedido a pedido cuando la entrada está vinculada específicamente a una demanda o un suministro (reserva automática). La demanda puede estar relacionada con las ventas o la necesidad de componentes.

### <a name="item-tracking-and-prospect-reservation-entry"></a>Seguimiento de artículos y entrada de reservas de prospectos

El estado de reserva de Prospecto se puede crear en la tabla  Microsoft Dynamics NAV Entrada de reserva *cuando no esté utilizando ninguna entidad de red de pedidos, es decir, Seguimiento de pedidos.*  Por ejemplo, en una línea del diario de consumo, asigna el seguimiento de artículos al componente. Sin embargo, si el artículo ya tiene seguimiento de pedido, es posible que se creen más entradas de reserva de prospectos. Microsoft Dynamics NAV  Esto se demuestra en el EJEMPLO 2 relacionado con las órdenes de transferencia en la segunda parte de este documento.

Al visualizar o modificar la página  **Líneas de seguimiento de artículos**, el contenido colectivo de la tabla  *Especificación de seguimiento*  (Tabla 336) y la tabla  *Entrada de reserva*  se presentan en una versión temporal de la tabla 336. De este modo se garantiza que se obtiene acceso a los datos de seguimiento de producto históricos y activos como una sola unidad.

Las reservas se dividen en dos categorías: reservas no específicas, en las que los números de lote y serie no se especifican en el momento de la reserva, y reservas específicas, en las que se reservan números de lote o serie específicos del inventario.

En una reserva no específica, el campo  **Número de lote** o **Número de serie**  está en blanco en el  **Número de entrada** de la tabla 337 que apunta a la demanda (por ejemplo, la venta). Debido a la estructura de la lógica de reserva en Microsoft Dynamics NAV, cuando se coloca una reserva no específica en un artículo rastreado en el inventario, Microsoft Dynamics NAV debe, no obstante, Seleccionar entradas específicas del libro mayor del artículo contra el cual reservar.

Dado que las entradas del libro mayor de artículos llevan la información de seguimiento de los artículos, la reserva reserva indirectamente números de serie o lotes específicos, incluso si el usuario no tenía esa intención. Sin embargo, con la vinculación tardía, Microsoft Dynamics NAV aún se reserva para entradas específicas, pero luego se utiliza un mecanismo de reorganización al momento de publicar. Microsoft Dynamics NAV 

Para obtener más información, revise los documentos técnicos que se enumeran en Recursos adicionales al final de este documento. Microsoft Dynamics NAV 

### <a name="source-subtype-suppressed-action-msg-action-message-adjustment-and-disallow-cancellation-fields"></a>Campos Subtipo de origen, Mensaje de acción suprimida, Ajuste del mensaje de acción y No permitir cancelación

En esta sección se describen los campos  **Subtipo de origen**,  **Mensaje de acción suprimida**,  **Ajuste del mensaje de acción** y  **No permitir cancelación**  en la tabla  *Entrada de reserva* . Se proporcionan escenarios para demostrar el uso de los campos  **Mensaje de acción suprimido**,  **Ajuste del mensaje de acción**  y  **No permitir cancelación** . El campo  **Ajuste del mensaje de acción**  se utiliza para la función de política de seguimiento de pedidos Seguimiento y mensaje de acción. El campo  **No permitir cancelación**  se utiliza para la función Ensamblaje bajo pedido en Microsoft Dynamics NAV 2013.

#### <a name="source-subtype"></a>Subtipo origen

El campo  **Subtipo de fuente**  indica con qué subtipo de fuente está relacionada la entrada de reserva. Si la entrada está relacionada con una línea de compra o venta, el campo se copia del campo  **Tipo de documento**  en la línea. Si está relacionado con una línea de diario, el campo se copia del campo  **Tipo de entrada**  en la línea de diario.

#### <a name="suppressed-action-msg"></a>Mensaje acción suprimido

El campo  **Mensaje de acción suprimida**  registra cuándo un suministro existente ya se ha procesado parcialmente, por ejemplo, cuando ya se ha recibido parcialmente una orden de compra o se han registrado consumos en una orden de producción.

Cuando se ejecuta la planificación, Microsoft Dynamics NAV marca este campo y establece el campo **Estado de entrada de reserva**  en *Excedente8. El siguiente ejemplo sirve como ilustración:

1. Artículo abierto 80001. Establezca los siguientes campos:
  - **Política de reordenamiento: lote por lote**
  - **Reserva**: Opcional
  - **Política de seguimiento de pedidos: Ninguna**
2. Cree un pedido de ventas. Establezca los siguientes campos:
  - **Artículo**: 80001
  - **Ubicación**: En blanco/Ninguno
  - **Cantidad: 10**
  - **Fecha de envío: 15/02/2014**
3. Abra las  **Hojas de trabajo de requisición** y ejecute el trabajo por lotes  **Calcular plan** para el artículo 80001.
  - **Fecha de inicio: 23/01/2014**
  - **Fecha de finalización: 01/03/2014**
4. Se da una sugerencia de planificación para reponer la cantidad de 10 con nueva orden de compra y fecha de vencimiento 15/02/2014. **·** 
5. En la pestaña  **Acciones**, en el grupo Funciones, elija  **Ejecutar acción** Mensaje para crear una orden de compra con  **Fecha de recepción prevista** 15/02/2014.
6. Abra la orden de compra de paso 5 y establezca  **Cantidad a recibir**  en 2 y registre solo el Recibo.
7. Abra la orden de venta de paso 2 y cambie la  **Fecha de envío** a 02/10/2014.
8. Abra las  **Hojas de trabajo de requisición** y ejecute  **Calcular plan** para el artículo 80001
  - **Fecha de inicio: 23/01/2014**
  - **Fecha de finalización: 01/03/2014**
9. Se da una sugerencia de planificación para reponer la cantidad de 8 con nueva orden de compra y fecha de vencimiento: 02/10/2014. **·** 

La información de estado de la tabla 337 se muestra en la siguiente ilustración.

La entrada n.° 28 en la tabla 337 tiene el estado de reserva Seguimiento para que coincida con el inventario existente registrado en la entrada n.° 318 del libro mayor de artículos para 2 unidades y la demanda pendiente en la tabla n.° 37 de órdenes de venta. La entrada posterior No. 29 también tiene el estado de reserva Seguimiento y vincula la cantidad restante de 8 unidades entre la demanda en la tabla de órdenes de venta 37 y el suministro sugerido en la tabla de líneas de requisición 246.

La entrada n° 30 es la orden de compra existente que se ha recibido parcialmente con cantidad 2. Como resultado, el campo  **Estado de reserva**  es Excedente y Microsoft Dynamics NAV establece el campo  **Cantidad (Base)**  en  *8* (saldo restante) y el campo  **Mensaje de acción suprimida**  está habilitado.

#### <a name="action-message-adjustment"></a>Ajuste mensajes acción

El campo  **Ajuste del mensaje de acción** muestra el cambio en el lado de suministro del seguimiento de pedidos que se produce cuando acepta los mensajes de acción relacionados. Aquí aparece un valor solo cuando las funciones para el seguimiento de pedidos y los mensajes de acción están activas (la política de seguimiento de pedidos está establecida en Seguimiento y mensajes de acción). El valor se calcula en función de los datos de la tabla  *Entrada de mensaje de acción*  (Tabla 99000849). El siguiente ejemplo sirve como ilustración:
1. Artículo abierto 80002. Establezca el siguiente campo:
 - **Política de seguimiento de pedidos**: Mensaje de seguimiento y acción.
2. Cree un pedido de ventas. Establezca los siguientes campos:
  - **Artículo**: 80002
  - **Ubicación: AZUL**
  - **Cantidad: 100**
3. Abra la página  **Planificación de pedidos**  y ejecute el trabajo por lotes  **Calcular plan** .
4. Seleccionar la orden de venta de paso 2 y ejecute el trabajo por lotes  **Hacer pedidos** .
5. En la orden de venta de paso 2, cambie el campo  **Cantidad**  de 100 a 105.
La información de estado de la tabla 337 se muestra en la siguiente ilustración.
6. La entrada No. 34 tiene el campo  **Ajuste del Mensaje de Acción**  en la tabla 337 habilitado para 5 unidades con estado de reserva Excedente. Como la orden de venta se incrementó en paso 5, Microsoft Dynamics NAV creé esta reserva porque se requiere más suministro.
7. Abra la página  **Hojas de trabajo de planificación**  y en la pestaña  **Inicio**, en el grupo  **Proceso**, seleccione  **Obtener mensajes de acción**. Microsoft Dynamics NAV sugerirá aumentar la cantidad de la orden de compra de 100 a 105.

#### <a name="disallow-cancellation"></a>No permitir cancelación

El campo  **No permitir cancelación** indica que la entrada de reserva representa la vincular entre una línea de orden de venta y una orden de ensamblaje. No puedes eliminar esta reserva porque es necesaria para mantener la sincronización que se produce cuando se ensambla un artículo según el pedido. El siguiente ejemplo sirve como ilustración:

1. Cree un pedido de compra. Establezca los siguientes campos:
  - **Unidad base de medida: PCS**
  - Cualquier grupo de publicación predeterminado
  - **Sistema de reposición: Ensamblaje**
  - **Política de ensamblaje: ensamblaje bajo pedido**
  - **Política de seguimiento de pedidos: Solo seguimiento**
2. Crea un nuevo elemento llamado Ensamblar COMP. Establezca los siguientes campos:
  - **Unidad base de medida: PCS**
  - Cualquier grupo de publicación predeterminado
  - **Sistema de reposición**: Compra
  - **Política de seguimiento de pedidos: Solo seguimiento**
3. Abra el elemento Ensamblar FG y, en la pestaña  **Navegar**, en el grupo  **Ensamblaje/Producción**, seleccione  **Ensamblaje** y, a continuación, seleccione  **L. MAT. de ensamblaje**. En la lista de materiales del ensamblaje, configure los siguientes campos:
  - **Tipo**: Artículo
  - **No.**: Ensamblar COMP
  - **Cantidad por**: 1 Elija el botón **Aceptar** .
4. Abra un diario de artículos y aumente el inventario de Assemble COMP a la cantidad 10 contra la ubicación AZUL y registre la línea del diario.
5. Cree un pedido de ventas. Establezca los siguientes campos:
  - **Artículo**: Ensamblar FG
  - **Ubicación: AZUL**
  - **Cantidad**: 1 La información de estado de la tabla 337 se muestra en la siguiente ilustración.

La entrada n.° 82 tiene estado de reserva excedente como 9 unidades del inventario de ensamblaje completo y no tiene demanda. La entrada n.° 84 son entradas de reserva de seguimiento entre la demanda en la tabla 901 de  *Línea de ensamblaje*  y su suministro en la entrada del libro mayor de artículos 346.

La entrada No. 86 tiene Orden a Orden Vinculante con Estado de Reserva. Además, el campo  **No permitir cancelación**  está habilitado ya que la política de ensamblaje está configurada como Ensamblar según pedido para el artículo Ensamblaje FG. Finalmente, el campo  **Flexibilidad de planificación**  se establece en Ninguno, ya que no permite que la lógica de planificación elimine la reserva. Microsoft Dynamics NAV 

#### <a name="quantity-available-to-pick-and-reservations"></a>Cantidad disponible para recoger y reservas

El campo  **Cantidad reservada de recogida y envío**  en la tabla 337 que existe en versiones anteriores a 2013 controla la disponibilidad de los artículos dentro de un almacén administrado. Microsoft Dynamics NAV  En cualquier instalación de gestión de almacenes, las cantidades de artículos existen tanto como entradas de almacén como entradas de libro mayor de artículos. Microsoft Dynamics NAV  Estos dos tipos de entrada contienen información diferente sobre dónde existen los artículos y si están disponibles. Los movimientos de almacén definen la disponibilidad de un producto por ubicación y tipo de ubicación, lo que se denomina contenido de ubicación. Los movimientos de producto definen la disponibilidad de un producto por sus documentos de reserva a salida. Existe una funcionalidad especial en el algoritmo de selección para calcular la cantidad que está disponible para seleccionar cuando el contenido del contenedor se combina con las reservas. El algoritmo de selección resta las cantidades reservadas para otros documentos de salida, las cantidades en documentos de selección existentes y las cantidades que se seleccionan pero aún no se han enviado ni consumido. El resultado se muestra en el campo  **Cantidad disponible para seleccionar**  en la página  **Hoja de trabajo de selección**, donde el campo se calcula dinámicamente. El valor también se calcula cuando un usuario crea selecciones de almacén directamente a partir de documentos de salida, como pedidos de venta, consumo de producción o transferencias de salida.

*Cantidad disponible para picking = cantidad en contenedores de picking – cantidad en pickings y movimientos – (cantidad reservada en contenedores de picking + cantidad reservada en pickings y movimientos).*

El siguiente ejemplo proporciona una ilustración de cómo se calcula el valor de la cantidad disponible para recoger en Microsoft Dynamics NAV:

1. Crea un nuevo artículo llamado Artículo de almacén. Establezca los siguientes campos:
  - **Unidad base de medida: PCS**
  - Cualquier grupo de publicación predeterminado
  - **Sistema de reposición**: Compra
  - **Política de reserva**: Siempre
  - **Política de seguimiento de pedidos: Solo seguimiento**
2. Crear una orden de compra contra el proveedor 60000. Establezca los siguientes campos:
  - **Artículo**: Artículo de almacén
  - **Ubicación: BLANCO**
  - **Cantidad: 100**
3. Liberar la orden de compra y crear el recibo de almacén.
4. Registrar el recibo de almacén y el almacenamiento en almacén por una cantidad de 100.
5. Cree una segunda orden de compra contra el proveedor 60000. Establezca los siguientes campos:
  - **Artículo**: Artículo de almacén
  - **Ubicación: BLANCO**
  - **Cantidad: 10**
6. Liberar la orden de compra y crear el recibo de almacén.
7. Envíe únicamente el recibo de almacén. No registre el guardado en almacén.
8. Cree un pedido de ventas. Establezca los siguientes campos:
  - **Artículo**: Artículo de almacén
  - **Ubicación: BLANCO**
  - **Cantidad**: 10 La cantidad reservada se establece automáticamente en 10 debido a que la política de reserva está establecida en Siempre.
9. Cree un pedido de ventas. Establezca los siguientes campos:
  - **Artículo**: Artículo de almacén
  - **Ubicación: BLANCA**
  - **Cantidad**: 100 La cantidad reservada se establece automáticamente en 100 debido a que la política de reserva está establecida en Siempre.
10. Libere la primera orden de venta de paso 8 y cree un envío de almacén.
11. Libere el envío del almacén y en la pestaña  **Acciones**, seleccione  **Crear picking**.
Se muestra el siguiente mensaje de error: *No hay nada que manejar.*
  La razón es que la cantidad disponible para recoger es cero. Esto se calcula de la siguiente manera: Cantidad en inventario = 110 Cantidad disponible para recoger = 100

> [!NOTE]  
> La cantidad en el contenedor de almacenamiento o de recepción no está disponible para recoger.
   
   El total reservado para pedidos de venta es 110. Cantidad disponible para recoger = 100 – 110 = cero.

Cuando el almacenamiento en almacén se registra en paso 7, esto habilita la creación del picking en almacén en paso 11. En versiones anteriores a 2013, el campo Cantidad reservada de recogida y envío de la tabla 337 se completa con la reserva de cantidad 10. Microsoft Dynamics NAV  **·** 

La siguiente ilustración está tomada de 2009 R2. Microsoft Dynamics NAV 

## <a name="illustrations-using-transfer-orders-and-planning"></a>Ilustraciones que utilizan órdenes de transferencia y planificación

### <a name="transfer-orders"></a>Pedidos de transferencia

Cuando se utilizan órdenes de transferencia y el artículo se envía pero no se recibe en su totalidad, en la tabla de  *Entrada de reserva*  obtendrá un estado de reserva Excedente. El código de ubicación será la ubicación de transferencia.

La **Fuente Ref. No.** El campo se calcula mediante el último Número de entrada de línea + el Número de entrada de línea del artículo en el envío de transferencia publicado.

Cuando se activa el seguimiento de pedidos y no hay demanda (pedido de venta o consumo), Microsoft Dynamics NAV crea dos entradas en la tabla 337 con estado de reserva Excedente. Uno es contra la tabla 5741 de  *Línea de transferencia*  y el otro es contra la tabla 32 de Entrada de libro mayor de artículos.

Esto se demuestra en el primer ejemplo.

#### <a name="example-1"></a>Ejemplo 1

1. Abra los elementos 80003 y 80004 y establezca el campo  **Política de seguimiento**  en  *Solo seguimiento*. Deje los demás campos como predeterminados.
2. Abra un diario de artículos y aumente el inventario de estos artículos a la cantidad 10 cada uno contra la ubicación ROJA y registre las líneas del diario.
3. Cree una orden de transferencia de la ubicación ROJA a la AZUL para estos dos artículos: Artículo 80003 en la línea de orden de transferencia 10000 y artículo 80004 en la segunda línea 20000, ambos para 10 unidades.
4. Publique solo la parte de envío de la orden de transferencia sin ninguna característica de almacén.
El envío de transferencia publicado se muestra en la siguiente ilustración.
La información de estado de la tabla 337 se muestra en la siguiente ilustración.
5. Compare los resultados del envío de transferencia registrado con las entradas de la tabla 337.

En la siguiente tabla se describe lo que sucede en ciertos campos frente a la entrada de reserva 40.

|Campo|Descripción|  
|---------------------------------|---------------------------------------|  
|**Estado de la reserva**|El excedente como artículo 80003 está configurado con seguimiento de pedido pero no existe demanda.|  
|**Código de almacén**|Ubicación del código de transferencia AZUL.|  
|**Tipo procedencia mov.**|Mesa de línea de transferencia 5741.|  
|**Identificación de la fuente**|Documento No. de la orden de transferencia 1011.|
|**Fuente Ref. No.**|Número total de línea 20000 + Línea Nro. 10000 contra el artículo 80003 = 30000.|

La explicación de los siguientes campos contra la entrada de reserva 43 es la siguiente.

|Campo|Descripción|  
|---------------------------------|---------------------------------------|  
|**Estado de la reserva**|El excedente como artículo 80003 está configurado con seguimiento de pedido pero no existe demanda.|  
|**Código de almacén**|Ubicación en tránsito REGISTRO PROPIO es la ubicación en la que existe el artículo.|  
|**Tipo procedencia mov.**|Tabla de entradas del libro mayor de artículos 32.|  
|**Fuente Ref. No.**|Entrada de artículo abierto número 322.|

#### <a name="example-2"></a>Ejemplo 2

El siguiente ejemplo ilustra lo que sucede cuando un componente se transfiere entre ubicaciones, pero al mismo tiempo se realiza un seguimiento entre una necesidad de demanda y un suministro disponible. Los componentes se transferirán desde la ubicación ROJA a la AZUL, donde se consumirán en una orden de producción liberada. El componente utiliza Seguimiento de pedidos, Planificación de pedidos y Seguimiento de artículos.

El ejemplo resalta el flujo detectado en la tabla 337 en relación con los campos  **Estado de reserva**,  **Código de ubicación**,  **Tipo de fuente**,  **ID de fuente**,  **N.º de referencia de fuente** y tipo de **Enlace**.

1. En la página  **Configuración de fabricación**, establezca el campo  **Componentes en ubicación**  en ROJO.
2. Crear un nuevo componente de artículo. Establezca los siguientes campos:
  - **Unidad base de medida: PCS**
  - Cualquier grupo de publicación predeterminado
  - **Sistema de reposición**: Compra
  - **Política de fabricación: Fabricación contra stock**
  - **Política de seguimiento de pedidos: Solo seguimiento**
  - **Código de seguimiento del artículo: LOTALL**
3. Utilizando el Diario de artículos, aumente el inventario del Componente de artículo en la ubicación ROJA a 100 unidades. Establezca los siguientes números de lote:
  - Número de lote Lote A, Cantidad 30
  - Número de lote Lote B, Cantidad 70
4. Crear un nuevo artículo Producido. Establezca los siguientes campos:
  - **Unidad base de medida: PCS**
  - Cualquier grupo de publicación predeterminado
  - **Sistema de reposición**: Producción
  - **Política de fabricación: Fabricación contra stock**
  - **Política de seguimiento de pedidos: Solo seguimiento**
5. Cree una  **Lista de materiales de producción** con 1 cantidad por cada componente del artículo.
6. Asignar la lista de materiales de producción al artículo producido.
7. Cree un pedido de ventas. Establezca los siguientes campos:
  - **Artículo**: Producido
  - **Ubicación: AZUL**
  - **Cantidad: 100**
8. En la pestaña  **Acciones**  del pedido de venta, en el grupo  **Plan**, seleccione  **Planificación** para crear una orden de producción lanzada vinculada al pedido de venta.
9. Abra la orden de producción liberada/necesidad de componente y observe que la ubicación está configurada como ROJA.
La razón es porque los  **Componentes en la ubicación** están en ROJO en la **Configuración de fabricación** tarjeta.
El artículo producido obtendrá la salida contra la ubicación AZUL.

La información de estado de la tabla 337 se muestra en la siguiente ilustración.

##### <a name="reservation-entries-with-numbers-55-and-56"></a>Entradas de reserva con los números 55 y 56

Para la necesidad de componentes del Lote A y del Lote B, respectivamente, se crean enlaces de seguimiento de pedidos desde la demanda en la tabla 5407, Componente de pedido de producción, hasta el suministro en la tabla 32, Entrada de libro mayor de artículos. El **Estado de la reserva**  El campo contiene seguimiento para las cuatro entradas para indicar que estos enlaces de seguimiento de pedidos dinámicos están entre oferta y demanda.

La demanda en la tabla 5407, Componente de orden de producción, está vinculada al ID de fuente de la orden de producción liberada 101006. El suministro en la tabla 32, Entrada de libro mayor de artículos, está vinculado al N.º de referencia de fuente. Siendo los asientos de libro mayor de artículos números 325 y 326 en los que existen las unidades.

> [!NOTE]  
> El campo **Nº lote** está vacío en las líneas de demanda porque los números de lote no están especificado en las líneas de componente de la orden de producción lanzada.

##### <a name="reservation-entry-with-number-57"></a>Entrada de reserva con el número 57

A partir de la demanda de ventas de la tabla 37, Línea de ventas, se crea un pedido de seguimiento vincular hasta el suministro en la tabla 5406, Línea de pedido de producción. El campo  **Estado de reserva**  contiene Reserva, y el campo  **Vinculación**  contiene Pedido a pedido. Esto se debe a que la orden de producción liberada se generó específicamente para la orden de venta y debe permanecer vinculada, a diferencia de los enlaces de seguimiento de pedidos con estado de reserva de Seguimiento, que se crean y modifican dinámicamente.

> [!NOTE]  
> El campo  **Enlace** también puede contener  *Pedido a pedido*  cuando se utiliza Fabricación a pedido como política de fabricación y/o Pedido como política de reordenamiento.

10. En este apuntar del escenario, las 100 unidades del componente se transfieren de la ubicación ROJA a la ubicación AZUL mediante una orden de transferencia.

Seleccionar Lote A y Lote B para el envío.

Publique la cantidad total pendiente como Enviado SOLAMENTE.

> [!NOTE]  
> Los componentes se pueden consumir en la ubicación ROJA, pero para ilustrar el ejemplo del flujo de entradas de reserva, las unidades se transfieren manualmente a la ubicación AZUL.

La información de estado de la tabla 337 se muestra en la siguiente ilustración.

##### <a name="reservation-entries-with-number-55-and-56"></a>Entradas de reserva con número 55 y 56

Las entradas de seguimiento de pedidos para los dos lotes del componente que reflejan la demanda en la tabla 5407 se cambian de un estado de reserva de Seguimiento a Excedente. El motivo es que los suministros a los que estaban vinculados antes, en la tabla 32, se han usado mediante el envío del pedido de transferencia. Los excedentes verdaderos, como en este caso, reflejan un exceso de aprovisionamiento que permanece sin seguimiento. Es una indicación de desequilibrio en la red de pedidos, que generará un mensaje de acción por parte del sistema de planificación a menos que se resuelva dinámicamente.

##### <a name="reservation-entry-numbers-59-to-63"></a>Números de entrada de reserva del 59 al 63

Debido a que los dos lotes del componente están registrados en la orden de transferencia como enviados pero no recibidos, todas las entradas de seguimiento de orden positivas relacionadas son del tipo de reserva Excedente, lo que indica que no están asignadas a ninguna demanda. Para cada número de lote, una entrada se relaciona con la tabla 5741, Línea de transferencia, y una entrada se relaciona con la entrada del libro mayor de artículos en la ubicación en tránsito donde ahora existen los artículos.

La tabla 5741, **Línea de transferencia**, es el tipo de fuente. **El ID de fuente es el número de documento de orden de transferencia 1012 y el número de referencia de fuente.**  **·** Es 20000 = 10000 + 10000 como se detalla en el Ejemplo 1. La ubicación se establece como AZUL para el código de ubicación de transferencia.

Las dos entradas restantes con  **Estado de reserva** Excedente tienen la tabla 32,  **Entrada de libro mayor de artículos**, como Tipo de fuente y  **N.º de referencia de fuente.** 328 y 330, incluidos sus números de lote ubicados actualmente en la ubicación En tránsito OUT LOG.

11. Registre la orden de transferencia pendiente como Recibida.

La información de estado de la tabla 337 se muestra en la siguiente ilustración.

Las entradas de seguimiento de pedidos ahora son similares a las primeras apuntar en el escenario, antes de que la orden de transferencia se registrara como enviada solamente, excepto que las entradas para el componente ahora tienen el estado de reserva Excedente en lugar de Seguimiento. Esto se debe a que la necesidad del componente aún se encuentra en la ubicación ROJA, lo que refleja que el campo  **Código de ubicación**  en la línea de componente de la orden de producción contiene ROJO tal como se configuró en el campo de configuración  **Componentes en la ubicación** .

El suministro que se asignó a esta demanda anteriormente se había transferido a la ubicación AZUL y ahora no se puede rastrear por completo a menos que la necesidad del componente en la línea de orden de producción se cambie a la ubicación AZUL. Esto se registra en las dos últimas entradas de reserva con los números de lote completados, siendo el campo  **Tipo de fuente**  la Tabla 32 y el  **N.º de referencia de fuente.** Campo que son las entradas del libro mayor de artículos 333 y 334.

12. En la lista de componentes asignada a la orden de producción liberada, cambie la ubicación a AZUL para el componente.

12. Abra el  **Diario de consumo** y ejecute el trabajo por lotes  **Calcular consumo** .
Asigne al lote A la cantidad 30 y al lote B la cantidad 70.

Cerrar el formulario de seguimiento de artículos.

La información de estado de la tabla 337 se muestra en la siguiente ilustración.

##### <a name="reservation-entries-with-numbers-68-and-69"></a>Entradas de reserva con los números 68 y 69

Dado que la necesidad del componente se ha cambiado a la ubicación AZUL y el suministro está disponible como entradas del libro mayor de artículos en la ubicación AZUL, todas las entradas de seguimiento de pedidos para los dos números de lote ahora están completamente rastreadas, lo que se indica mediante el estado de reserva de Seguimiento. Los números de lote no se completan en el campo  **N.º de lote**  contra la demanda en la tabla 5406,  **Línea de orden de producción**, ya que no especificamos números de lote para el componente en la orden de producción lanzada.

##### <a name="reservation-entries-with-numbers-70-and-71"></a>Entradas de reserva con los números 70 y 71

Las entradas con estado de reserva Prospecto se generan en la tabla 337. El motivo es que ambos números de lote están asignados al componente en el diario de consumo, pero el diario no se ha registrado.

Esto completa la sección sobre cómo se generan, modifican y eliminan las entradas de seguimiento de pedidos en la tabla de  **Entrada de reserva**  cuando se utilizan múltiples funciones en combinación con órdenes de transferencia.

### <a name="planning-calculated-1"></a>Planificación calculada

Al utilizar funciones de planificación, es decir, la  **Hoja de trabajo de requisición**, la  **Hoja de trabajo de planificación** o la  **Planificación de pedidos**, las entradas de reserva en la tabla 337 de  **Entrada de reserva**  se pueden modificar o agregar según la sugerencia de planificación proporcionada por la lógica en Microsoft Dynamics NAV. El ejemplo 3 utilizará **Política de reordenamiento**  Ordene con **Política de fabricación**  Fabricación bajo pedido de un artículo producido. El componente utilizará **Política de reordenamiento**  Cantidad de reorden fija.

#### <a name="example-3"></a>Ejemplo 3

1. En el **Configuración de fabricación**  tarjeta, **Componente en la ubicación**  es ROJO del ejemplo anterior.
2. Crear nuevo artículo elemento primario 70061. Establezca los siguientes campos:
  - **Unidad base de medida: PCS**
  - Cualquier grupo de publicación predeterminado
  - **Sistema de reposición**: Orden de producción
  - **Política de fabricación** : Hacer el pedido
  - **Política de reordenamiento** : Orden
  - **Política de reserva** : Opcional
  - **Rastreo de orden** : Ninguno
3. Crear nuevo componente artículo 70062. Establezca los siguientes campos:
  - **Unidad base de medida: PCS**
  - Cualquier grupo de publicación predeterminado
  - **Sistema de reposición** : Compra
  - **Política de reordenamiento** :Cantidad de reorden fija
  - **Política de reserva** : Opcional
  - **Política de seguimiento de pedidos: Ninguna**
  - **Cantidad de stock de seguridad**: 10
  - **Reordenar apuntar**: 25
  - **Cantidad de reorden: 50**
4. Cree una nueva lista de materiales de producción y especifique el componente 70062 con cantidad por 1.
Asigne la lista de materiales de producción al artículo elemento primario 70061.
5. Cree un pedido de ventas. Establezca los siguientes campos:
  - **Artículo**: Cantidad de reorden fija
  - **Ubicación: ROJO**
  - **Cantidad: 40**
  - **Fecha de envío: 15/02/2014**
6. Abra la página  **Hojas de trabajo de planificación**  y ejecute el trabajo por lotes  **Calcular plan regenerativo** .
  - **MPS/MRP**: habilitado
  - **Fecha de inicio: 23/01/2014**
  - **Fecha de finalización: 01/03/2014**
  - Filtrar por artículos 70061 y 70062
  - Sin pronóstico

Se ofrecen las siguientes sugerencias de planificación.

La primera sugerencia de planificación es crear una nueva orden de producción planificada para abastecer la demanda pendiente de la orden de venta por la cantidad 40 del artículo elemento primario 70061. Revise el seguimiento de pedidos y se mostrarán los pedidos de venta pendientes. Microsoft Dynamics NAV  El seguimiento de pedidos se activa a medida que lo genera el motor de planificación.

La segunda línea es para llevar el inventario arriba de Reordenar apuntar (25). Entonces, teniendo en cuenta la cantidad de reorden (50), la lógica de planificación sugiere una cantidad de 50 unidades. La tercera línea es llevar el inventario al nivel de stock de seguridad (10).

La cuarta línea es para reponer el inventario cuando se envía la orden de venta. En ese momento, el inventario es 20 y así sucesivamente. Reordenar apuntar. Como resultado, el motor de planificación propone comprar 50 componentes adicionales teniendo en cuenta la cantidad de reorden. Esta es una cantidad sin seguimiento, por lo que en la tabla de  *Entrada de reserva* 337 estará marcada con el estado de reserva Excedente.

La información de estado de la tabla 337 se muestra en la siguiente ilustración.

El campo  **Estado de reserva**  es Reserva y se crea un enlace de pedido a pedido. La razón es que la política de fabricación de artículos es bajo pedido y la política de reordenamiento está establecida como pedido. Si uno de los dos está configurado en Pedido, entonces el estado de la reserva será Reserva en lugar de Seguimiento y la vinculación se configura en Pedido a pedido.

La demanda de 40 unidades contra el campo **ID de fuente** es el número de orden de venta 1005 y el Tipo de fuente es *Línea de ventas* tabla 37. La entrada de reserva está alineada con la sugerencia de planificación, Fuente Ref. No. 10000, el ID de fuente es PLANIFICACIÓN y el tipo de fuente es  *Línea de requisición* tabla 246. Por lo tanto, existe un equilibrio entre la demanda de la orden de venta y la oferta sugerida por el motor de planificación.

##### <a name="reservation-entry-numbers-73-and-74"></a>Reservación de entradas números 73 y 74

Al ejecutar el trabajo por lotes Calcular plan, las siguientes cuatro entradas se generan con un estado de reserva de Seguimiento debido a la configuración de la política de reordenamiento Cantidad de reorden fija para el componente. El suministro requerido para el componente Artículo 70062 se repone mediante las sugerencias de planificación proporcionadas, Fuente Ref. No. 20000 y 30000, con ID de fuente establecida en PLANIFICACIÓN y Tipo de fuente de la tabla 246 de  *Línea de requisición* . La necesidad del componente se crea para satisfacer la demanda del artículo elemento primario 70061 para una cantidad total (base) de 40. Como resultado de esta demanda, el campo  **Línea de pedido de producción de origen** es 10000, con Tipo de fuente en la tabla  *Necesidad de componente*  99000829.

El estado de la reserva no es Excedente, ya que existe seguimiento del pedido entre la demanda del Artículo elemento primario 70061 y el suministro del Artículo componente 70062.

##### <a name="reservation-entry-numbers-75-and-76"></a>Reservación de entradas números 75 y 76

Las dos últimas entradas tienen un estado de reserva Excedente, ya que son Cantidades sin seguimiento generadas en la hoja de trabajo de planificación relacionada con los parámetros de reordenamiento Reorden apuntar y Cantidad de reordenamiento.

## <a name="see-also"></a>Consulte también
[Detalles de diseño: diseño del seguimiento de productos](design-details-item-tracking-design.md)  
[Detalles de diseño: equilibrio de oferta y demanda](design-details-balancing-demand-and-supply.md)  
[Detalles de diseño: Reserva, seguimiento de pedidos y mensajes de acciones](design-details-reservation-order-tracking-and-action-messaging.md)   
[Detalles de diseño: Planificación de aprovisionamiento](design-details-supply-planning.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
