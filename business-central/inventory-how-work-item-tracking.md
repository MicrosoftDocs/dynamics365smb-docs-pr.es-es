---
title: "Asignar números de serie y de lote a productos para realizar un seguimiento | Microsoft Docs"
description: "Puede agregar números de serie y números de lote a cualquier documento de salida o de entrada, los movimientos de seguimiento de producto registrados se muestran en los correspondientes movimientos de producto."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/22/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: dcfa7f47202472e43f0d57cee53f7c0a954dd12a
ms.contentlocale: es-es
ms.lasthandoff: 03/22/2018

---
# <a name="work-with-serial-and-lot-numbers"></a>Trabajar con números de lote y de serie
Puede asignar números de serie y de lote a cualquier documento de salida o de entrada, los movimientos de seguimiento de producto registrados se muestran en los correspondientes movimientos de producto. El trabajo se realiza en la ventana **Líns. seguim. prod.**.

La matriz de los campos de cantidad del encabezado de la ventana **Líns. seguim. prod.** muestra las cantidades y las sumas de los números de seguimiento de producto que se definen en las líneas. Las cantidades deben corresponder a las de la línea del documento, indicado mediante un 0 en los campos **Indefinido**.

Con el fin de mejorar el rendimiento, el programa recopila la información sobre disponibilidad que se muestra en la ventana **Líns. seguim. prod.** solamente cuando la abre. Esto significa que el sistema no actualiza la información sobre disponibilidad mientras la ventana está abierta, incluso aunque se produzcan cambios en el inventario o en otros documentos durante ese tiempo.

Los números de serie o lote de productos se pueden seguir, ya sea hacia adelante o hacia atrás, en su cadena de suministro. Esto es útil para asegurarse de la calidad general y para la recuperación de productos. Para obtener más información, consulte [Realizar un seguimiento de productos marcados para seguimiento](inventory-how-to-trace-item-tracked-items.md).

## <a name="about-picking-serial-or-lot-numbers-in-the-warehouse"></a>Cómo hacer picking de los números de serie y de lote en el almacén
El control de salidas de números de serie o lote es una tarea común en diferentes procesos del almacén.  

En algunos procesos, los productos de inventario no llevan números del seguimiento de producto y el trabajador de almacén debe asignar uno nuevo durante el control, normalmente a partir de una serie de números predefinidos.

En los procesos simples, los productos de inventario ya contienen los números de serie o de lote, asignados durante la ubicación, por ejemplo, y estos números se transfieren automáticamente con todas las actividades de almacén de salida sin interacción por parte de los trabajadores de almacén.

En las situaciones especiales de inventario de números de serie o de lote, los números específicos se definen en el documento de origen, como un pedido de venta, que el trabajador de almacén debe respetar durante el control del almacén de salida. Esto puede ser porque el cliente ha solicitado un lote interno específico durante el proceso del pedido. Cuando se crea el picking de existencias o documento de picking de almacén a partir de un documento de origen de salida en donde ya están definidos los números de serie o de lote, todos los campos de la ventana **Líns. seguim. prod.** en el picking de existencias están bloqueados para escritura, excepto el **Cdad. a manipular**. En ese caso, Las líneas de picking de inventario especifican los números de seguimiento de producto en las líneas de colocar y recoger individuales. La cantidad ya está dividida en combinaciones de números de serie o lote exclusivos porque el pedido de venta especifica los números de seguimiento de producto que se van a enviar.  

## <a name="item-tracking-availability"></a>Disponibilidad de seguimiento de producto
Cuando trabaja con números de lote o de serie, [!INCLUDE[d365fin](includes/d365fin_md.md)] obtiene información acerca de la disponibilidad de estos números, y la muestra en las diferentes ventanas de seguimiento de productos. Esto le permite comprobar qué parte de un número de lote o de serie se utiliza actualmente en otros documentos. Esto reduce los errores y las incertidumbres provocados por asignaciones duplicadas.

En la ventana **Líns. seguim. prod.**, se muestra un icono de advertencia en el campo **Disponibilidad, Nº lote** o **Disponibilidad, Nº serie** en caso de que algunas o todas las cantidades que ha seleccionado ya estén en uso en otros documentos, o si el número de lote o de serie no estuviera disponible.

En las ventanas **Lista nº lote/Lista nº serie**, **Disponibilidad nº lote/Disponibilidad nº serie** y **Seg. productos - Selec. movs.**, se muestra información acerca de la cantidad usada de un producto. Esto incluye la siguiente información.

|Campo|Description|
|-----|-----------|  
|**Cantidad total**|El número total de productos existentes actualmente en el inventario.|
|**Cdad. solicitada total**|El número total de productos que se han solicitado que se utilizarán en éste y en otros documentos.|
|**Cantidad pendiente actual**|El número de productos que se han solicitado que se utilizarán en el documento actual pero que todavía no se han confirmado en la base de datos.|
|**Cantidad solicitada actual**|El número de productos que se han solicitado que se utilizarán en el documento actual.|
|**Cantidad total disponible**|El número total de productos del inventario menos la cantidad del producto que se ha solicitado para ser utilizada en este y en otros documentos (cdad. solicitada total) y menos la cantidad que se ha solicitado pero que todavía no se ha registrado en este documento (cantidad pendiente actual).|

Si trabaja con la ventana **Líns. seguim. prod.** durante un largo periodo de tiempo o si existe mucha actividad relacionada con el producto sobre el que está trabajando, puede elegir la opción **Actualizar disponibilidad**. Además, el programa volverá a comprobar la disponibilidad del producto cuando cierre la ventana, con el fin de garantizar que no existe ningún problema de disponibilidad.

## <a name="to-set-up-item-tracking-codes"></a>Para configurar códigos de seguimiento de producto
Un código de seguimiento de producto refleja las distintas consideraciones que tiene una empresa en referencia al uso de números de serie y lote de los productos que se mueven en el inventario.  

1. Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Códs. seguim. prod.** y, a continuación, seleccione el vínculo relacionado.  
2. Seleccione la acción **Nuevo**.
3. Rellene los campos según sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
4. En las fichas desplegables **Nº serie** y **Nº lote**, defina las directivas de seguimiento del producto mediante números de serie y lote respectivamente.  

### <a name="to-set-up-expiration-rules-for-serial-or-lot-numbers"></a>Para configurar las reglas de caducidad para números de serie o lote  
Con algunos productos es posible que le interese configurar fechas y reglas de caducidad específicas en el código de seguimiento de producto. Esta funcionalidad le permite realizar un seguimiento de la caducidad de determinados números de serie y de lote.

1. Seleccione un código de seguimiento de productos existentes, y después la acción **Editar** .  
2.  En la ficha desplegable **Varios**, seleccione las casillas de verificación siguientes.  

    |Campo|Description|  
    |---------------------------------|---------------------------------------|  
    |**Registro caducidad requerido**|Especifica que, cuando el producto salga del inventario, debe respetarse la fecha de caducidad asignada al número de seguimiento de producto tal como se introdujo en el inventario.|  
    |**Fecha caducidad manual requerida**|Especifica que debe introducirse manualmente una fecha de caducidad en la línea de seguimiento de producto.|  

### <a name="to-set-up-warranties-for-serial-or-lot-numbers"></a>Para configurar garantías para números de serie o lote  
Con algunos productos es posible que le interese configurar garantías específicas en el código de seguimiento de producto. Esta funcionalidad le permite realizar un seguimiento de la caducidad de las garantías de determinados números de serie o lote en inventario.        
1.  Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Códs. seguim. prod.** y, a continuación, seleccione el vínculo relacionado.  

1. Seleccione un código de seguimiento de productos existentes, y después la acción **Editar** .  
2.  En la ficha desplegable **Varios**, rellene el campo **Fórmula fecha garantía** y active las casillas según se indica a continuación.  

    |Campo|Description|  
    |---------------------------------|---------------------------------------|  
    |**Fórmula fecha garantía**|Especifica el último día de garantía para el producto.|  
    |**Fecha garantía manual requerida**|Especifica que debe introducir manualmente una fecha de garantía en la línea de seguimiento del producto.|  

## <a name="to-record-serial-or-lot-number-information"></a>Para registrar información de números de serie o lote  
Si necesita vincular información especial a un número de seguimiento de producto específico, por ejemplo, para controles de calidad, puede hacerlo en una ficha de información de número de serie o lote.

1. Abra un documento que tenga número de serie y de lote asignados.
2. Abra la ventana **Líns. seguim. prod.** para el documento.
3. Elija, por ejemplo, la acción **Ficha información nº serie**.  

    Los campos **Nº serie** y **Nº lote** se prellenan desde la línea de seguimiento del producto.  
4. Introduzca un texto informativo breve en el campo **Descripción**, por ejemplo, sobre la condición del artículo.  
5. Seleccione la acción **Comentario** para crear un registro de comentarios separado.  
6. Seleccione la casilla de verificación **Bloqueado** para excluir el número de serie o de lote de cualquier transacción.  

## <a name="to-modify-existing-serial-or-lot-number-information"></a>Para modificar la información relativa al número de serie o de lote actuales  
1. Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Productos** y, a continuación, seleccione el vínculo relacionado.  
2. Seleccione un producto que tenga un código de seguimiento de producto e información de número de serie o lote.
3. En la ventana **Ficha producto**, seleccione la acción **Movimientos** y, después, **Movimientos**.
4. Elija los campos **Nº lote** o **Nº serie**. Si hay información referente al número de seguimiento del producto, se abre la ventana **Lista información nº lote** o **Lista información nº serie**.  
5. Seleccione una ficha y después la acción **Ficha información nºlote/Ficha información nº serie** .  
6. Edite el texto de la breve descripción, el registro de comentario o el campo **Bloqueado**.  

No puede modificar los números de serie o lote ni las cantidades. Para ello, deberá reclasificar el movimiento de producto en cuestión. Si desea obtener más información, consulte "Reclasificación de números de lote o de serie".

## <a name="to-assign-serial-or-lot-numbers-during-an-inbound-transaction"></a>Para asignar números de serie o lote en una transacción de entrada  
Es posible que las empresas deseen realizar un seguimiento de productos desde el momento en que éstos entran en la empresa. En esta situación, el pedido de compra normalmente es el documento principal, aunque el seguimiento de productos puede controlarse desde cualquier documento de entrada y sus movimientos registrados que se muestran en los movimientos de productos correspondientes.  

Las reglas exactas para controlar los números de seguimiento de producto en la empresa se rigen por la configuración de la tabla **Ficha cód. seguim. prod.**  

> [!NOTE]  
>  Para utilizar números de seguimiento de productos en las actividades de almacén, se deben seleccionar los campos de configuración **Control lote almacén** y **Seguim. nº serie almacén**, ya que definen los principios especiales para gestionar los números de serie y lote en las actividades de almacén.  

1.  Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Pedidos de compra** y, a continuación, seleccione el vínculo relacionado.  
2.  Seleccione la línea del documento correspondiente en la ficha desplegable **Líneas**, elija la acción **Línea**, y después elija **Líns. seguim. prod**.  

    Puede asignar números de serie o lote de las siguientes maneras:  

    -   Automáticamente, al seleccionar **Asignar nº serie** o **Asignar nº lote** para asignar números de serie o lote de las series numéricas predefinidas.  
    -   Automáticamente, al seleccionar **Crear NS personalizado** para asignar números de serie o lote basados en las series numéricas que ha definido específicamente para los productos recibidos.  
    -   Manualmente, al introducir los números de serie o lote directamente, por ejemplo, los números del proveedor.  
    -   Manualmente, asignando un número específico a cada unidad de producto.  

3. Para asignar automáticamente, elija la acción de **Crear NS personalizado**.  
4. En el campo **NS personalizado**, introduzca el número inicial de una serie de números descriptivos, por ejemplo, **S/N-Prov0001**.  
5. En el campo **Incremento**, introduzca 1 para definir que cada número de secuencia aumente de uno de uno.  

    El campo **Cdad. a crear** contiene, de forma predeterminada, la cantidad de la línea, pero puede modificarla.  

6. Seleccione la casilla **Crear nuevo nº lote** para organizar los nuevos números de serie en un lote distinto.  
7. Elija el botón **Aceptar**.  

Se crea un número de lote con números de serie individuales según la cantidad de productos de la línea del documento, empezando en **S/N-Prov0001**.  

La matriz de los campos de cantidad de la cabecera muestra dinámicamente las cantidades y las sumas de los números de seguimiento de producto que se definen en la ventana. Las cantidades deben corresponder a las de la línea del documento, que se indica como 0 en los campos **Indefinido**.  

Cuando se registra el documento, los movimientos de seguimiento de producto se llevan a los movimientos de producto asociados.

## <a name="to-assign-a-serial-or-lot-number-during-an-outbound-transaction"></a>Para asignar un número de serie o lote en una transacción de salida  
Hay dos formas de agregar números de serie y de lote a las transacciones de salida:  

-   Selección de los números de serie o lote existentes. Se aplica cuando ya se han asignado los números de seguimiento de producto en una transacción de entrada. Para más información, consulte la sección "Seleccionar números de serie o de lote existentes".
-   Asignación de números de serie o lote nuevos en las transacciones de salida. Esto se aplica cuando los números de seguimiento de producto no se asignan a los productos que se venden y están preparados para enviarse.  

Se configuran distintas reglas para los números de seguimiento de producto en la ventana **Ficha cód. seguim. prod.**.  

> [!NOTE]  
>  Para asignar números de seguimiento de producto en las actividades de almacén, las casillas de verificación **Seguim. nº serie almacén** y **Control lote almacén** se deben seleccionar en la ficha del código del seguimiento del producto.    

1. Seleccione el documento correspondiente en la ficha desplegable **Líneas**, elija la acción **Pedido**, y después la acción **Líns. seguim. prod**.  

    Puede asignar números de seguimiento de productos de las siguientes maneras:  
    -   Automáticamente, desde la serie numérica predefinida: elija la acción **Asignar nº serie** o **Asignar nº lote**.  
    -   Automáticamente, en función de los parámetros que ha definido específicamente para el artículo de salida: elija la acción **Crear NS personalizado**.  
    -   Manualmente, introduciendo números de serie o lote sin utilizar una serie numérica.  

2.  Para este procedimiento, asigne un número de serie automáticamente eligiendo **Asignar nº serie**  

    El campo **Cdad. a crear** contiene, de forma predeterminada, la cantidad de la línea, pero puede modificarla.  
3.  Seleccione el campo **Crear nuevo nº lote** para organizar los nuevos números de serie en un lote distinto.  
4.  Elija el botón **Aceptar** para crear un número de lote y nuevos números de serie individuales según la cantidad de productos que se van a controlar en la línea de documento correspondiente.  

La matriz de los campos de cantidad de la parte superior del formulario muestra dinámicamente las cantidades y las sumas de los números de seguimiento de producto que se definen en la ventana. Las cantidades deben corresponder con las de la línea del documento, que se indica como **0** en los campos **Indefinido**.  

Cuando se registra el documento, los movimientos de seguimiento de producto se llevan a los movimientos de producto asociados.  

## <a name="to-select-from-existing-serial-or-lot-numbers"></a>Para seleccionar los números de serie o de lote existentes  
Cuando trabaja con productos que requieren seguimiento y está creando transacciones de salida, donde los productos salen del inventario, normalmente será necesario seleccionar los números de lote o de serie a partir de los que ya existen en el inventario.  

 Las reglas exactas para controlar los números de seguimiento de producto en la empresa se rigen por la configuración de la tabla **Cód. seguim. prod.**.  

> [!NOTE]  
>  Para controlar los números de seguimiento de productos en las actividades de almacén, el producto debe configurarse con Seguim. nº serie y lote almacén, como indican los principios especiales que rigen los números de serie y de lote en el almacén.

1.  En un documento de salida, seleccione la línea para la que desea seleccionar números de serie o de lote.  
2.  En la ficha desplegable **Líneas**, elija la acción **Acciones** seleccione la **Línea** o el **Producto** y, a continuación, **Líns. seguim. prod**.  
3.  En la ventana **Líns. seguim. prod.**, dispone de tres opciones para especificar el número de serie o de lote:  

    -   Seleccione el campo **Nº lote** o **Nº serie** y elija un número en la ventana **Resumen seguimiento prod.**  
    -   Seleccione la acción **Selec. movs.** La ventana **Seleccionar movs.** muestra todos los lotes y números de serie junto con la información de disponibilidad.

4. En el campo **Cantidad seleccionada**, escriba la cantidad de cada número de lote o de serie que desea utilizar.   
5. Elija el botón **Aceptar**, y la información de seguimiento del producto seleccionado se transfiere a la ventana **Líns. seguim. prod.**  
6. Escriba o escanee el número de seguimiento del producto.

La matriz de los campos de cantidad de la cabecera muestra dinámicamente las cantidades y las sumas de los números de seguimiento de producto que se definen en la ventana. Las cantidades deben corresponder con las de la línea del documento, que se indica como **0** en los campos **Indefinido**.  

 Cuando registra la línea del documento, la información de seguimiento del producto se transfiere a los movimientos de producto asociados.

## <a name="to-handle-serial-and-lot-numbers-on-transfer-orders"></a>Para controlar números de serie y lote en los pedidos de transferencia  
Los procedimientos para controlar los números de serie y lote que se van a transferir entre distintos almacenes son parecidos a los que se aplican al comprar o vender productos.  

No obstante, el pedido de transferencia es único en cuanto a que el envío y la recepción se hacen desde la misma línea de transferencia y, por tanto, utilizan la misma instancia de la ventana **Líns. seguim. prod.** Esto quiere decir que los números de seguimiento de productos enviados desde un almacén deben recibirse sin modificaciones en el otro almacén.  

 Las reglas exactas para controlar los números de seguimiento de producto en la empresa se rigen por la configuración de la tabla  **Cód. seguim. prod.**    
1.  Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Pedidos de transferencia** y, a continuación, seleccione el vínculo relacionado.  
2.  Abra el pedido de transferencia que desea procesar. En la ficha desplegable **Líneas**, elija la acción **Línea**, seleccione la acción **Líns. seguim. prod.** y elija la acción **Envío**.  
3.  En la ventana **Líns. seguim. prod.**, asigne o seleccione números de serie o de lote de la misma forma que lo haría para otra transacción de producto de salida.  

    Al controlar los números de serie y de lote para productos de transferencia, los productos normalmente ya los tienen asignados. Por tanto, el proceso normalmente consiste en seleccionar números de serie o de lote existentes.  

4.  Registre el pedido de transferencia, primero el envío y más tarde la recepción, para indicar que los productos se transfieren con sus movimientos de seguimiento de producto específicos.  

Durante la transferencia, la ventana **Líns. seguim. prod.** permanece bloqueada para escritura.  

## <a name="to-handle-serial-and-lot-numbers-when-getting-receipt-lines-from-a-purchase-invoice"></a>Para gestionar números de serie y de lote al obtener las líneas de recepción de una factura de compra  
Cuando se utiliza la funcionalidad para obtener las líneas de envío y recepción registradas de las facturas o los abonos relacionados, las líneas de seguimiento de producto de los documentos de almacén se transfieren automáticamente, sin embargo, se procesan de forma especial.

La funcionalidad utilizan los procesos de entrada siguientes:  
-   **Traer líns. albarán**: de una factura de compra.  
-   **Traer líns. envío dev.**: de un abono de compra.  

La funcionalidad utilizan los procesos de salida siguientes:  
-   **Traer líneas alb. venta**: de una factura de venta o envíos combinados.  
-   **Traer líns. recep. dev.**: de un abono de venta.  

En estas situaciones, las líneas de seguimiento de productos existentes se copian automáticamente en la factura o en el abono, pero la ventana **Líns. seguim. prod.** no permite realizar cambios en los números de serie o de lote. Solo se pueden modificar las cantidades.  

1.  Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Facturas de compra** y, a continuación, seleccione el vínculo relacionado.  
2.  Abra una factura de compra para los productos que se compran con los números de serie o de lote.  
3.  Desde una línea de la factura de compra, en la ficha desplegable **Líneas**, seleccione la acción **Traer líns. recep**.  
4.  En la ventana **Traer líns. albarán**, seleccione una línea de recepción que tenga líneas del seguimiento de producto y, a continuación seleccione el botón **Aceptar**.  

    El documento de origen se copia en la factura de compra como una línea nueva, y las líneas de seguimiento de productos se copian en la ventana **Líns. seguim. prod.** subyacente.  

5.  En la factura de compra, seleccione la línea de recepción transferida.  
6.  En la ficha desplegable **Líneas**, elija **Línea**, y seleccione **Líns. seguim. prod.** para ver las líneas de seguimiento de producto transferidas.  

El contenido de los campos **Nº serie** y **Nº lote** no se puede editar. No obstante, puede eliminar líneas completas o cambiar las cantidades para que coincidan con los cambios que se han hecho en la línea de origen.  

## <a name="to-reclassify-serial-or-lot-numbers"></a>Para reclasificar números de lote o de serie  
El proceso de reclasificar el seguimiento para un producto significa convertir un número de lote o de serie en un nuevo número de lote o de serie, o bien convertir la fecha de caducidad en una nueva. Si está trabajando con lotes, también puede combinar varios lotes en uno. Para llevar a cabo este proceso, deberá utilizar el diario de reclasificación de productos.

1.  Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Diario reclas. producto** y, a continuación, seleccione el vínculo relacionado.  
2.  Rellene la línea con la información correspondiente. Para obtener más información, consulte [Recuento, ajuste, y reclasificación de inventario](inventory-how-count-adjust-reclassify.md).
3.  Seleccione la acción **Líns. seguim. prod.**  
4.  En el campo **Nº serie** o **Nº lote**, seleccione el número de serie o de lote actual.  
5.  Si desea introducir un nuevo número del seguimiento de producto, introdúzcalo en el campo **Nuevo nº serie** o **Nuevo nº lote**. Si lo desea, puede combinar uno o más lotes en un lote nuevo o existente.  

    > [!NOTE]  
    >  Tenga en cuenta que al reclasificar las fechas de caducidad, los productos con las fechas de caducidad más próximas para las transacciones de salida se sugieren primero. Para obtener más información, consulte [Realización de picking por el FEFO](warehouse-picking-by-fefo.md).  

5.  Si desea introducir una nueva fecha de caducidad para el número de serie o lote, escríbala en el campo **Nueva fecha caducidad**.  

    > [!IMPORTANT]  
    >  Si está reclasificando un lote con el mismo número de lote pero con una fecha de caducidad distinta, deberá reclasificar el lote completo utilizando una línea del diario de reclasificación de productos. Si está reclasificando más de un lote con un nuevo número de lote, es decir, si combina varios lotes en un lote nuevo, deberá introducir la misma fecha de caducidad para todos los lotes. Si está reclasificando un lote existente con un segundo lote también existente pero que tiene una fecha de caducidad diferente, deberá utilizar la fecha de caducidad del segundo lote. Si deja en blanco el campo **Nueva fecha caducidad** el número de serie o lote se reclasificará con una fecha de caducidad en blanco.  

6.  Si ya dispone de información acerca del antiguo número de lote o de serie, puede copiarla en el nuevo número de serie o de lote.  

    1.  En la ventana **Líns. seguim. prod.**, elija la acción **Nueva información nº serie** o **Nueva información nº lote**.  
    2.  Para copiar la información a partir del antiguo número de lote o de serie, haga clic en **Copiar info**.  
    3.  En la ventana de lista de información, seleccione el número de lote o de serie que desea copiar y elija el botón **Aceptar**.  

7.  Si desea modificar la información existente relativa al número de lote o de serie, puede registrar la información respectiva.  
8.  Registre el diario para enlazar los números de seguimiento de producto renovados o las fechas de caducidad con los movimientos de producto asociados.

## <a name="see-also"></a>Consulte también
[Realizar seguimiento de productos seguidos](inventory-how-to-trace-item-tracked-items.md)   
[Grupos contables inventario](inventory-manage-inventory.md)  
[Detalles de diseño: seguimiento de productos](design-details-item-tracking.md)
[Detalles de diseño. Seguimiento y reservas de productos](design-details-item-tracking-and-reservations.md)  
[Reservar artículos](inventory-how-to-reserve-items.md)  
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

