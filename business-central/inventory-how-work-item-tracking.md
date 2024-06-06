---
title: 'Seguimiento de productos con números de serie, de lote y de paquete'
description: 'Puede agregar números de serie, números de lote y números de paquete a cualquier documento de salida o de entrada, los movimientos de seguimiento de producto registrados se muestran en los correspondientes movimientos de producto.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.forms: '6503, 6515, 6513, 6512, 6502, 6506, 6501, 6510, 6507, 6500, 6505, 6508, 9126, 6526, 6516, 6511, 6504, 6509, 163, 6550,'
ms.date: 03/13/2024
ms.custom: bap-template
ms.service: dynamics-365-business-central
---
# <a name="track-items-with-serial-lot-and-package-numbers"></a>Seguir productos con números de serie, de lote y de paquete

Puede asignar números de serie, números de lote y números de paquete a cualquier documento de salida o de entrada, los movimientos de seguimiento de producto registrados se muestran en los correspondientes movimientos de producto. Realice el seguimiento de productos en la página **Líns. seguim. prod.**, que puede abrir desde documentos de entrada o salida.

Los campos de cantidad del encabezado de la página **Líns. seguim. prod.** muestra las cantidades y las sumas de los números de seguimiento de producto que se definen en las líneas. Las cantidades deben corresponder a las de las líneas del documento, indicado mediante un 0 en los campos **Indefinido**.

[!INCLUDE [prod_short](includes/prod_short.md)] actualiza la información de disponibilidad en la página **Líneas de seguimiento de artículos** al abrir la página. No actualiza la información mientras tenga la página abierta, aunque se produzcan cambios en el inventario o en otros documentos durante ese tiempo.

> [!NOTE]  
> Para que las funciones descritas en este artículo funcionen, debe configurar el seguimiento de productos. Para obtener más información, vaya a [Configurar el seguimiento de productos con números de serie, lote y paquete](inventory-how-setup-item-tracking.md).

## <a name="item-tracking-availability"></a>Disponibilidad de seguimiento de productos

Cuando trabaja con números de serie, de lote o de paquete, [!INCLUDE[prod_short](includes/prod_short.md)] obtiene información acerca de la disponibilidad y la muestra en las diferentes páginas de seguimiento de productos. Muestra la cantidad de un lote, paquete o número de serie que se utiliza en otros documentos. Esta información ayuda a reducir los errores y las incertidumbres provocados por asignaciones duplicadas.

En la página **Líneas de seguimiento de productos**, es posible que aparezca un icono de advertencia en **Disponibilidad, Número de lote** o **Disponibilidad, N.º de serie** por los siguientes motivos:

* Si una parte o la totalidad de la cantidad que ha seleccionado ya se utiliza en otros documentos.
* Si el número de lote o de serie no está disponible.

Las páginas **Lista nº lote/Lista nº serie**, **Disponibilidad nº lote/Disponibilidad nº serie** y **Seg. productos - Selec. movs.** muestran información acerca de la cantidad usada de un producto. La siguiente tabla enumera los campos relevantes.

|Campo|Descripción|
|-----|-----------|  
|**Cantidad total**|El número total de un producto existente actualmente en el inventario.|
|**Cdad. solicitada total**|El número total de productos que se solicitan en este y otros documentos.|
|**Cantidad pendiente actual**|El número de productos que se han solicitado en el documento actual pero que no se contabilizan.|
|**Cantidad solicitada actual**|El número de productos que se han solicitado que se utilizarán en el documento actual.|
|**Cantidad total disponible**|El número total de productos del inventario menos la cantidad del producto que se ha solicitado para ser utilizada en este y en otros documentos (cdad. solicitada total) y menos la cantidad que se ha solicitado pero que todavía no se ha contabilizado en este documento (cantidad pendiente actual).|

Si trabaja con la página **Líns. seguim. prod.** durante un largo periodo de tiempo o si existe mucha actividad relacionada con el producto sobre el que está trabajando, puede elegir la opción **Actualizar disponibilidad**. Además, el programa volverá a comprobar la disponibilidad del producto cuando cierre la página, con el fin de garantizar que no existe ningún problema de disponibilidad.

## <a name="to-assign-serial-or-lot-numbers-during-an-inbound-transaction"></a>Para asignar números de serie o lote en una transacción de entrada

Es posible que desee realizar un seguimiento de los productos desde el momento en que llegan. En ese caso, el pedido de compra suele ser el documento central. Sin embargo, puede realizar el seguimiento de los productos desde cualquier documento de entrada y sus entradas contabilizadas se muestran en las entradas del libro mayor de artículos relacionados.

Los números de seguimiento se transfieren automáticamente a todas las actividades de salida del almacén.

1. Elija el icono ![Bombilla que abre la característica Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), , escriba **Pedidos de compra** y, a continuación, elija el vínculo relacionado.  
2. Abra un pedido de compra existente o cree uno nuevo.
3. Seleccione la línea del documento en la ficha desplegable **Líneas**, elija la acción **Línea**, y después elija **Líns. seguim. prod.** para abrir la página **Editar: Líns. seguim. prod**.  

   Puede asignar números de serie o lote de las siguientes maneras:  
   * Automáticamente, al seleccionar **Proceso** y, después, eligiendo **Asignar nº serie** o **Asignar nº lote** para asignar números de serie o lote de las series numéricas predefinidas.  
   * Automáticamente, al seleccionar **Proceso** y, después, eligiendo **Crear NS personalizado** para asignar números de serie o lote basados en las series numéricas que ha definido específicamente para los productos recibidos.  
   * Manualmente, al introducir los números de serie o lote directamente, por ejemplo, los números del proveedor.  
   * Manualmente, asignando un número específico a cada unidad de producto.  

4. Para asignar automáticamente, elija la acción de **Crear NS personalizado**.  
5. En el campo **NS personalizado**, introduzca el número inicial de una serie de números de serie descriptivos. Por ejemplo **N/S-Vend0001**.  
6. En el campo **Incremento**, introduzca 1 para definir que cada número de secuencia aumente de uno de uno.  

    El campo **Cdad. a crear** contiene, de forma predeterminada, la cantidad de la línea, pero puede modificarla.  

7. Seleccione la casilla **Crear nuevo nº lote** para organizar los nuevos números de serie en un lote distinto.  
8. Elija el botón **Aceptar**.  

[!INCLUDE [prod_short](includes/prod_short.md)] crea un número de lote con números de serie individuales según la cantidad de artículos en la línea del documento. El número tiene como prefijo el valor que introdujo en el campo **NS personalizado** . Por ejemplo, empezando desde **N/S-Vend0001**.  

Los campos de cantidad de la cabecera muestran dinámicamente las cantidades y las sumas de los números de seguimiento de producto que se definen en la página. Las cantidades deben corresponder a las de las líneas del documento, indicado mediante un **0** en el campo **Indefinido**.  

Al contabilizar el documento, las entradas de seguimiento de artículos se transfieren a movimientos de productos.

### <a name="to-handle-serial-and-lot-numbers-when-getting-receipt-lines-from-a-purchase-invoice"></a>Para gestionar números de serie y de lote al obtener las líneas de recepción de una factura de compra

Cuando se contabilizan líneas de recepción o envío de facturas o abonos relacionados, las líneas de seguimiento de artículos de los documentos de almacén se transfieren automáticamente. Sin embargo, se procesan de una manera especial.

La funcionalidad utilizan los procesos de entrada siguientes:  

* **Traer líns. albarán**: de una factura de compra.  
* **Traer líns. envío dev.**: de un abono de compra.  

La funcionalidad utilizan los procesos de salida siguientes:  

* **Traer líneas alb. venta**: de una factura de venta o envíos combinados.  
* **Traer líns. recep. dev.**: de un abono de venta.  

En estos casos, las líneas de seguimiento de artículos se transfieren a la factura o al abono, pero la página **Líns. seguim. prod.** no le permite cambiar los números de serie o de lote. Solo puede modificar las cantidades.  

1. Elija el icono ![Bombilla que abre la característica Dígame](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Facturas compra** y, a continuación, elija el vínculo relacionado.  
2. Abra una factura de compra para los productos que se compran con los números de serie o de lote.  
3. Desde una línea de la factura de compra, en la ficha desplegable **Líneas**, seleccione la acción **Traer líns. recep**.  
4. En la página **Traer líns. albarán**, seleccione una línea de recepción que tenga líneas del seguimiento de producto y, a continuación seleccione el botón **Aceptar**.  

    El documento de origen se copia en la factura de compra como una línea nueva, y las líneas de seguimiento de productos se copian en la página **Líns. seguim. prod.** subyacente.  

5. En la factura de compra, seleccione la línea de recepción transferida.  
6. En la ficha desplegable **Líneas**, elija **Línea**, y seleccione **Líns. seguim. prod.** para buscar las líneas de seguimiento de producto transferidas.  

No puede cambiar los campos **Nº serie** y **Nº lote** . No obstante, puede eliminar líneas completas o cambiar las cantidades para que coincidan con los cambios de la línea de origen.  

## <a name="to-assign-a-serial-or-lot-number-during-an-outbound-transaction"></a>Para asignar un número de serie o lote en una transacción de salida

El control de salidas de números de serie o lote es una tarea común en diferentes procesos del almacén. Hay dos formas de agregar números de serie y de lote a las transacciones de salida:  

- Seleccione los números de serie o de lote existentes. Se aplica cuando ya se han asignado los números de seguimiento de producto en una transacción de entrada.
- Asigne números de serie o lote nuevos para las transacciones de salida. Esto se aplica cuando los números de seguimiento de producto no se asignan a los productos que se venden y están preparados para enviarse.

### <a name="to-select-from-existing-serial-or-lot-numbers"></a>Para seleccionar los números de serie o de lote existentes

Cuando trabaja con productos que requieren seguimiento y está creando transacciones de salida, normalmente será necesario seleccionar los números de lote o de serie que ya existen.

1. En un documento de salida, seleccione la línea para la que desea seleccionar números de serie o de lote.  
2. En la ficha desplegable, elija **Líneas**, la acción **Línea** y, después, **Información relacionada** y luego seleccione **Líns. seguim. prod.**.  
3. En la página **Líns. seguim. prod.**, dispone de tres opciones para especificar el número de serie o de lote:  

   * Seleccione el campo **Nº serie** y elija un número en la página **Lista de N.º de serie**.
   * Seleccione el campo **N.º lote** y elija un número en la página **Lista de N.º de lote**. A continuación, seleccione el campo **Nº serie** y elija un número en la página **Lista de N.º de serie**.
   * Seleccione la acción **Proceso** y luego elija **Seleccionar entradas**. La página **Seleccionar movs.** muestra todos los lotes y números de serie junto con la información de disponibilidad.

4. En el campo **Cantidad seleccionada**, escriba la cantidad de cada número de lote o de serie que desea utilizar.
5. Elija el botón **Aceptar**. La información de seguimiento de productos se transfiere a la página **Líns. seguim. prod.** .  

Los campos de cantidad de la cabecera muestran dinámicamente las cantidades y las sumas de los números de seguimiento de producto que se definen en la página. Las cantidades deben corresponder a las de la línea del documento, indicado mediante un **0** en el campo **Indefinido**.  

Cuando registra la línea del documento, la información de seguimiento del producto se transfiere a los movimientos de producto asociados.

### <a name="to-assign-new-serial-or-lot-numbers"></a>Para asignar números de lote o de serie nuevos

Este proceso se aplica cuando los productos no tienen números de serie o de lote mientras están en el inventario. En su lugar, usted asigna los números de seguimiento de los productos cuando estos se venden y están listos para su envío. En este caso, normalmente asignará números de una serie numérica predefinida.

1. Seleccione el documento relevante, por ejemplo, una factura de venta o un pedido de venta, y en la ficha desplegable **Línea**, elija la acción **Línea**, después **Información relacionada** y luego elija la acción **Líneas de seguimiento de productos**.  

    Puede asignar números de seguimiento de productos de las siguientes maneras:  
    * Automáticamente, desde la serie numérica predefinida: elija la acción **Asignar nº serie** o **Asignar nº lote**.  
    * Automáticamente, en función de los parámetros que ha definido específicamente para el artículo de salida: elija la acción **Crear NS personalizado**.  
    * Manualmente, introduciendo números de serie o lote sin utilizar una serie numérica.  

2. Para este procedimiento, asigne un número de serie automáticamente eligiendo **Asignar nº serie**  

    El campo **Cdad. a crear** contiene, de forma predeterminada, la cantidad de la línea, pero puede modificarla.  
3. Seleccione el campo **Crear nuevo nº lote** para organizar los nuevos números de serie en un lote distinto.  
4. Elija el botón **Aceptar** para crear un número de lote y nuevos números de serie individuales según la cantidad de productos que se van a controlar en la línea de documento correspondiente.  

Los campos de cantidad de la parte superior del formulario muestran dinámicamente las cantidades y las sumas de los números de seguimiento de producto que se definen en la página. Las cantidades deben corresponder a las de la línea del documento, indicado mediante un **0** en el campo **Indefinido**.  

Al contabilizar el documento, las entradas de seguimiento de artículos se transfieren a movimientos de productos.

### <a name="assign-tracking-numbers-on-source-documents"></a>Asignar números de seguimiento en documentos de origen

Algunas empresas definen números de serie o de lote específicos en el documento fuente, como los pedidos de venta. Por ejemplo, si un cliente solicita un lote específico. Cuando crea el documento de picking de inventario o de almacén a partir de un documento fuente de salida en el que ya están definidos los números de serie o de lote, no puede modificar ningún campo de la página **Líns. seguim. prod.** bajo el picking de inventario. La única excepción es el campo **Cdad. a manipular**. En ese caso, Las líneas de picking de inventario especifican los números de seguimiento de producto en las líneas de colocar y recoger individuales. La cantidad ya está dividida en combinaciones de números de serie o lote exclusivos porque el pedido de venta especifica los números de seguimiento de producto que se van a enviar.

## <a name="to-handle-serial-and-lot-numbers-on-transfer-orders"></a>Para controlar números de serie y lote en los pedidos de transferencia

Los procedimientos para controlar los números de serie y lote que se van a transferir entre distintos almacenes son parecidos a los que se aplican al comprar o vender productos.  

No obstante, los pedidos de transferencia es único en el sentido de que tanto el envío como la recepción se hacen desde la misma línea de transferencia y, por tanto, utilizan la misma instancia de la página **Líns. seguim. prod.** Los números de seguimiento de productos enviados desde un almacén deben recibirse sin modificaciones en el otro almacén.

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Pedidos de transferencia** y luego elija el enlace relacionado.  
2. Abra el pedido de transferencia que desea procesar. En la ficha desplegable **Líneas**, elija la acción **Línea**, seleccione la acción **Líns. seguim. prod.** y elija la acción **Envío**.  
3. En la página **Líns. seguim. prod.**, asigne o seleccione números de serie o lote de la misma forma que lo haría para otra transacción de producto de salida.  

    Al controlar los números de serie y de lote para productos de transferencia, los números normalmente son números ya asignados. Por lo tanto, a menudo elegirá entre números de serie o de lote existentes.  

4. Registre el pedido de transferencia, primero el envío y más tarde la recepción, para indicar que los productos se transfieren con sus movimientos de seguimiento de producto específicos.  

Durante la transferencia, no puede cambiar los valores de la página **Líns. seguim. prod.**.  

## <a name="to-record-additional-serial-or-lot-number-information"></a>Para registrar información adicional de números de serie o lote

Si necesita vincular información especial a un número de seguimiento de producto, por ejemplo, para controles de calidad, puede hacerlo en una ficha de información de número de serie o lote.

1. Abra un documento que tenga número de serie y de lote asignados.
2. Abra la página **Líneas de seguimiento de productos** para el producto para el que desea especificar información.
3. Elija la acción **Línea** y luego, por ejemplo, la acción **Tarjeta de información del número de serie**.  
4. Elija el signo más **(+)** en la parte superior de la lista para crear una nueva entrada. Los campos **Nº serie** y **Nº lote** se prellenan desde la línea de seguimiento del producto.
5. Introduzca un texto informativo breve en el campo **Descripción**, por ejemplo, sobre la condición del artículo.  
6. Elija la acción **Relacionado**, elija la acción **Número de serie** y luego elija la acción **Comentario** para crear un registro de comentarios separado.  
7. Seleccione el campo **Bloqueado** para excluir el número de serie o de lote de cualquier transacción.  

<!--If you create serial numbers in bulk by using the **Create Customized SN** or **Assign Serial No.** actions, you can enable **Create SN Information** and an information card will be created for each tracking line.

Alternatively, you can create an information card when you post journals or documents. On the **Item Tracking Code** page, turn on the **Create SN Info. on posting** or **Create SN Info. on posting** toggles. -->

Puede modificar las tarjetas de información de lote o de serie creadas más tarde.

## <a name="to-modify-existing-serial-or-lot-number-information"></a>Para modificar la información relativa al número de serie o de lote actuales

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Productos**, y luego elija el enlace relacionado.  
2. Seleccione un producto que tenga un código de seguimiento de producto e información de número de serie o lote.
3. En la página **Ficha producto**, seleccione la acción **Movimientos** y, después, **Movimientos**.
4. Elija los campos **Nº lote** o **Nº serie**. Si hay información referente al número de seguimiento del producto, se abre la página **Lista información nº lote** o **Lista información nº serie**.  
5. Seleccione una ficha y después la acción **Ficha información nºlote/Ficha información nº serie** .  
6. Edite el texto de la breve descripción, el registro de comentario o el campo **Bloqueado**.  

No puede modificar los números de serie o lote ni las cantidades. Para ello, deberá reclasificar el movimiento de producto. Para obtener más información sobre cómo reclasificar, vaya a [Para reclasificar de números de lote o de serie](inventory-how-work-item-tracking.md#to-reclassify-serial-or-lot-numbers).

## <a name="to-reclassify-serial-or-lot-numbers"></a>Para reclasificar números de lote o de serie

El proceso de reclasificar el seguimiento para un producto significa convertir un número de lote o de serie en un nuevo número de lote o de serie, o bien convertir la fecha de caducidad en una nueva. Si utiliza lotes, también puede combinar varios lotes en uno. Utilice un diario de reclasificación de productos para realizar estas tareas.

> [!NOTE]
> [!INCLUDE [prod_short](includes/prod_short.md)] verifica que cada línea tenga una combinación única de números de serie, lote y/o paquete. Si desea dividir un lote, un paquete o un lote y empaquetar en varios lotes o paquetes, debe utilizar varias líneas de diario.

1. Elija el icono ![Bombilla que abre la característica Dígame](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Diarios reclasif. producto**, y luego elija el enlace relacionado.  
2. Rellene la línea con la información correspondiente. Para obtener más información, consulte [Contar inventario mediante documentos](inventory-how-count-inventory-with-documents.md) o [Recuento, ajuste y reclasificación de inventario mediante diarios](inventory-how-count-adjust-reclassify.md).
3. Seleccione la acción **Líns. seguim. prod.**  
4. En el campo **Nº serie** o **Nº lote**, seleccione el número de serie o de lote actual.  
5. Si desea introducir un nuevo número del seguimiento de producto, introdúzcalo en el campo **Nuevo nº serie** o **Nuevo nº lote**. Si lo desea, puede combinar uno o más lotes en un lote nuevo o existente.  

    > [!NOTE]  
    > Cuando reclasifique las fechas de caducidad, los productos con las fechas de caducidad más próximas para las transacciones de salida se sugieren primero. Para obtener más información, vaya a [Realización de picking por el FEFO](warehouse-picking-by-fefo.md).  

6. Para especificar una nueva fecha de caducidad para el número de serie o lote, escríbala en el campo **Nueva fecha caducidad**.  

    > [!IMPORTANT]  
    > * Si está reclasificando un lote con el mismo número de lote pero con una fecha de caducidad distinta, deberá reclasificar el lote completo utilizando una línea del diario de reclasificación de productos.
    > * Si está reclasificando más de un lote con un nuevo número de lote, es decir, si combina varios lotes en un lote nuevo, deberá introducir la misma fecha de caducidad para todos los lotes. 
    > * Si está reclasificando un lote existente con un segundo lote también existente pero que tiene una fecha de caducidad diferente, deberá utilizar la fecha de caducidad del segundo lote. 
    > * Si deja en blanco el campo **Nueva fecha caducidad** el número de serie o lote se reclasificará con una fecha de caducidad en blanco.  

7. Si ya dispone de información acerca del antiguo número de lote o de serie, puede copiarla en el nuevo número de serie o de lote.  

    1. En la página **Líns. seguim. prod.**, elija la acción **Nueva información nº serie** o **Nueva información nº lote**.  
    2. Para copiar la información a partir del antiguo número de lote o de serie, haga clic en **Copiar info**.  
    3. En la página de lista de información, seleccione el número de lote o de serie que desea copiar y elija el botón **Aceptar**.  

8. Si desea modificar la información existente relativa al número de lote o de serie, puede registrar la información respectiva.  
9. Registre el diario para enlazar los números de seguimiento de producto renovados o las fechas de caducidad con los movimientos de producto asociados.

## <a name="scan-barcodes-with-the-business-central-mobile-app"></a>Escanear códigos de barras con la aplicación móvil Business Central

[!INCLUDE [barcode-mobile-app](includes/barcode-mobile-app.md)]

En la página **Líns. seguim. prod.** si desea escanear varios códigos de barras de serie, lote o paquete, puede utilizar la acción **Escanear múltiples**. Después de escanear un código de barras, su valor se introduce en el campo de la página y el siguiente campo de entrada rápida pasa a estar disponible. También puede utilizar el icono del escáner de código de barras para completar un campo específico.

La siguiente tabla enumera las páginas que admiten el escaneado de códigos de barras para el seguimiento de productos desde la aplicación móvil [!INCLUDE [prod_short](includes/prod_short.md)].

|Página  |Valores del campo que puede escanear  |
|---------|---------|
|Líns. seguim. prod.     |* N.º serie<br><br>* Nuevo nº serie<br><br>* N.º lote<br><br>* Nuevo nº lote<br><br>* N.º paquete<br><br>* N.º de nuevo paquete|
|Almacén Líns. seguim. prod.     |* N.º serie<br><br>* Nuevo nº serie<br><br>* N.º lote<br><br>* Nuevo nº lote<br><br>* N.º paquete<br><br>* N.º de nuevo paquete|
|Seguim. prod.     |* Filtro nº serie<br><br>* Filtro n.º lote<br><br>* N.º paquete Filtro |
|Diario de producto     |* N.º serie<br><br>* N.º lote<br><br>* N.º paquete     |
|Lín.actividad almacén     |* N.º serie<br><br>* N.º lote<br><br>* N.º paquete<br><br>**Nota**: Las siguientes páginas utilizan la página Lín. actividad almacén:<br><br>* página 5780 “Subformulario de picking de almacén"<br><br>* página 7378 "Subformulario de selección inv."<br><br>* página 5771 “Subformulario de almac. de almacén"<br><br>* página 7316 "Subformulario de movimiento de almacén"<br><br>* página 7376 "Subformulario de almac. de inv."<br><br>* página 7383 "Subformulario de movimiento de inv."        |
|Almacén Diario de inventario físico     |* N.º serie<br><br>* N.º lote<br><br>* N.º paquete         |

## <a name="see-also"></a>Consulte también .

[Configurar el seguimiento de productos con números de serie, de lote y de paquete](inventory-how-setup-item-tracking.md)  
[Realizar seguimiento de productos seguidos](inventory-how-to-trace-item-tracked-items.md)  
[Inventario](inventory-manage-inventory.md)  
[Detalles de diseño: Seguimiento de productos](design-details-item-tracking.md)  
[Detalles de diseño: Seguimiento de productos y reservas](design-details-item-tracking-and-reservations.md)  
[Reservar artículos](inventory-how-to-reserve-items.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
