---
title: 'Recuento, ajuste y reclasificación de inventario'
description: Aprenda a hacer recuentos físicos y hacer ajustes y reclasificaciones.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.service: dynamics-365-business-central
ms.topic: how-to
ms.date: 12/20/2022
ms.custom: bap-template
---
# Recuento, ajuste y reclasificación de inventario con diarios

Cuente físicamente todos los productos del inventario para asegurarse de que las cantidades sean correctas. Algunas empresas hacen un recuento físico anual y otras cuentan todos o solo algunos productos con más frecuencia. Después de contar los productos, use diarios para registrar las cantidades reales en el libro mayor. Por ejemplo, cuando valora el inventario al final de un período.

Para contar algunos productos con más frecuencia que otros, tal vez debido a su valor, utilice recuentos cíclicos. Este tipo de recuento, asigna períodos de recuento especiales a los productos. Obtenga más información en [Cómo hacer un recuento cíclico](inventory-how-count-adjust-reclassify.md#to-do-cycle-counting).

Para ajustar cantidades después de un recuento físico u otros propósitos, use un diario de productos para cambiar los movimientos del libro mayor de inventario sin registrar transacciones. También puede ajustar la cantidad de un solo producto en una ficha de producto.

Para cambiar atributos de las movimientos de contabilidad de los productos, use un diario de reclasificación de productos. Los atributos típicos que se suelen reclasificar son las dimensiones y códigos de campaña de ventas. Los diarios de reclasificación también se pueden usar para transferencias mediante la reclasificación de códigos de ubicación y almacén. Se aplican pasos especiales cuando desea reclasificar números de serie o de lote, y sus fechas de caducidad. Para obtener más información, consulte [Trabajar con números de serie y de lote](inventory-how-work-item-tracking.md).

> [!NOTE]
> En los procesos de varios pasos, los productos se registran en las ubicaciones como movimientos de almacén, no como movimientos de productos. Por lo tanto, el recuento, el ajuste y la reclasificación se realiza en diarios especiales de almacén que dan soporte a ubicaciones. A continuación, debe sincronizar las entradas de almacén nuevas o modificadas con sus movimientos de productos relacionados para reflejar los cambios en las cantidades y valores de inventario.

[!INCLUDE [edit-in-excel](includes/edit-in-excel.md)]

## Para contar el inventario físico

Cuente el inventario físico, es decir, cuente los productos reales disponibles, para comprobar si la cantidad registrada coincide con la cantidad física en stock. Por lo general, los recuentos se realizan al final del año fiscal, pero a veces se realizan con más frecuencia. Si hay diferencias, registre las cantidades reales en las cuentas de productos <!--accounts, or ledger?--> antes de hacer la valoración del inventario.

> [!NOTE]
> Este procedimiento describe cómo hacer un inventario físico utilizando un diario en la página **Diario inventario físico**. Puede utilizar documentos de las páginas **Pedido de inventario físico** y **Registro de inventario físico**. Estos documentos ofrecen más control y soporte para distribuir el trabajo de recuento a varios empleados. Obtenga más información en [Recuento y ajuste de inventario mediante documentos](inventory-how-count-inventory-with-documents.md).<br /><br />
> Tenga en cuenta que no puede usar la funcionalidad basada en documentos para contar productos en ubicaciones o movimientos de almacén.

El proceso de recuento también cuenta con las siguientes tareas:

- Calcular el inventario previsto.
- Imprimir el informe que se usará en el recuento.
- Introducir y registrar las cantidades reales.

Según la configuración del almacén, cuente el inventario físico según una de las formas siguientes. Para obtener más información, consulte [Configuración de la administración de almacén](warehouse-setup-warehouse.md).  

- Si su ubicación no utiliza el almacenamiento y la recolección dirigidos, use la página **Diario inventario físico**. El procedimiento es similar al inventario físico sin recuento cíclico.  
- Si su ubicación utiliza el almacenamiento y la recolección dirigidos, use la página **Diario de inventario físico de almacén**. Luego use la página **Diarios de productos** para ejecutar la acción **Calcular ajuste almacén**. <!--We should say what to do on each of these pages.-->

### Para calcular el inventario esperado en las configuraciones básicas del almacén

1. Elija el icono ![Bombilla que abre la característica Dígame](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Diarios de inventario físico** y luego elija el enlace relacionado.
2. Elija la acción **Calcular inventario**.
3. En la página **Calcular inventario**, especifique las condiciones que desea utilizar para crear las líneas de diario, como si desea incluir los productos que tienen un inventario registrado de cero.
4. Establezca filtros si solo desea calcular el inventario para productos, ubicaciones, almacenes o dimensiones determinados.
5. Elija el botón **Aceptar**.

> [!NOTE]  
> Se procesan los movimientos de producto según los datos especificados y se crean las líneas en el diario de inventario físico. Tenga en cuenta que el campo **Cdad. (stock físico)** tiene la misma cantidad que figura en el campo **Stock calculado**. No necesita introducir la cantidad de productos contados donde estos valores coincidan. Sin embargo, si la cantidad contada difiere, introduzca la cantidad contada.

### Para imprimir el informe que va utilizar para el recuento

1. En la página **Diario inventario físico** que contiene el inventario previsto calculado, elija la acción **Imprimir**.
2. En la página **Lista del inventario físico almacén**, especifique si el informe mostrará el stock calculado y los productos de inventario por números de serie y lote.
3. Establezca filtros si solo desea imprimir el informe para productos, ubicaciones, almacenes o dimensiones determinados.
4. Elija **Imprimir**.

Ahora los empleados de almacén pueden contar el inventario y registrar las diferencias en el informe impreso.

> [!NOTE]
> Pueden pasar varios días antes de que los informes impresos regresen para su registro y procesamiento finales. Cuando especifica y registra el inventario contado real, el sistema ajusta el inventario para reflejar la diferencia entre el inventario contado esperado y el real. Debe mantener las líneas de diario calculadas originalmente y no volver a calcular el inventario previsto, ya que el inventario previsto puede cambiar y conducir a niveles de inventario incorrectos. Si necesita emitir varios informes, como para diferentes ubicaciones o grupos de productos, debe crear y mantener secciones de diario separados.

### Para introducir y registrar el inventario contado real en configuraciones básicas de almacén

1. En cada línea de la página **Diario inventario físico**, donde el inventario real disponible, según lo determinado por el recuento físico, difiere de la cantidad calculada, introduzca el inventario real disponible en el campo **Cdad. (stock físico)**.
  
  > [!NOTE]  
  > Si el recuento físico revela diferencias producidas por productos que se registraron con almacenes incorrectos, no introduzca las diferencias en el diario de inventario físico. En su lugar, utilice un diario de reclasificación o un pedido de transferencia para redirigir los productos a los almacenes correctos. 

2. Para ajustar las cantidades calculadas a las cantidades contadas reales, elija la acción **Registrar**.

    El registro crea movimientos de productos y movimientos del inventario físico. Abra la página Ficha producto del producto para encontrar sus movimientos del inventario físico. <!--Where are they shown on an item?-->

3. Elija el icono ![Bombilla que abre la característica Dígame](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Productos**, y luego elija el enlace relacionado.
4. Para verificar el recuento, abra la página Ficha producto del producto y elija la acción **Movs. inventario físico**. <!--I don't see this action -->

### Para calcular el inventario esperado en las configuraciones avanzadas del almacén

Sincronice el libro mayor de productos y el almacén <!--warehouse what?--> antes de contar el inventario físico. De lo contrario, lo que publique en el diario de inventario físico y el libro mayor de productos serán los resultados del inventario físico combinados con otros ajustes del almacén para los productos. Obtenga más información en [sincronizar cantidades en el libro mayor de productos y el almacén](inventory-how-count-adjust-reclassify.md#to-synchronize-the-adjusted-warehouse-entries-with-the-related-item-ledger-entries).

1. Elija el icono ![Bombilla que abre la característica Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Diario de inventario físico de almacén** y luego elija el enlace relacionado.  
2. Seleccione la acción **Calcular inventario** para abrir la página **Calcular existencias alm.**  
3. Defina los filtros para especificar los productos que se contarán en el diario y, a continuación, seleccione **Aceptar**.

   [!INCLUDE [prod_short](includes/prod_short.md)] crea una línea para cada ubicación que cumpla los requisitos del filtro. Puede eliminar líneas, pero si desea registrar los resultados como un inventario físico, debe contar el producto en todas las ubicaciones que lo contienen.  

   Si solo cuenta un producto en algunas ubicaciones, pero no en otras, puede introducir diferencias y registrarlas posteriormente en el diario de productos con la acción **Calcular ajuste almacén**. <!--I don't see this action-->  

### Para introducir y registrar el inventario contado real en configuraciones avanzadas de almacén

1. En la página **Diario de inventario físico de almacén**, introduzca las cantidades reales en el campo **Cdad. (stock físico)**.  

    > [!NOTE]  
    >  El campo **Cant. (Calculado)** se rellena en función de los registros de ubicaciones. Esta cantidad se copia en el campo **Cant. (físico)** de cada línea. Si las cantidades de estos campos no coinciden, introduzca la cantidad real.  

2. Una vez que haya introducido todas las cantidades reales, elija la acción **Registrar**.  

    Al registrar el diario, [!INCLUDE [prod_short](includes/prod_short.md)] crea dos movimientos de almacén en el registro del almacén por cada línea que se ha contado y registrado:  

    - Si la cantidad calculada y la cantidad real son distintas, se registra una cantidad negativa o positiva en la ubicación y se registra una cantidad de contrapartida en la ubicación de ajuste del almacén.  
    - Si la cantidad calculada es igual que la cantidad física, [!INCLUDE [prod_short](includes/prod_short.md)] registra **0** en la ubicación y en la ubicación de ajuste. 

Cuando registra el inventario físico, no contabiliza el producto, el inventario físico o los libros mayores de valores. Sin embargo, los registros están disponibles para conciliarlos cuando sea necesario. Para mantener las cantidades precisas, después de contar los productos en todas las ubicaciones, registre los resultados como un inventario físico de inventario <!--physical inventory journal-->. Obtenga más información en [Sincronizar cantidades en el libro mayor de productos y el almacén](inventory-how-count-adjust-reclassify.md#to-synchronize-the-adjusted-warehouse-entries-with-the-related-item-ledger-entries).

## Realizar el recuento cíclico

Puede contar productos con la frecuencia que desee. Por ejemplo, porque son más valiosos o porque tienen una salida rápida y constituyen una gran parte de su negocio. Especifique la frecuencia de recuento asignando períodos de recuento especiales a los productos.

Según cómo esté configurado el almacén, puede realizar el recuento de ciclo de las siguientes maneras. Obtenga más información en [Configuración de Warehouse Management](warehouse-setup-warehouse.md).  

- Si su ubicación no utiliza el almacenamiento y la recolección dirigidos, use la página **Diario inventario físico**. Los pasos son similares al recuento del inventario físico sin el recuento cíclico.  
- Si su ubicación utiliza el almacenamiento y la recolección dirigidos, use la página **Diario de inventario físico de almacén**. Luego use la página **Diarios de productos** para ejecutar la acción **Calcular ajuste almacén**. <!--we should say what to do on each of these pages-->  

### Para configurar periodos de recuento

El recuento del inventario físico es normalmente una tarea periódica, por ejemplo, mensual, trimestral o anual. Puede configurar los periodos de recuento de inventario que necesita y asignar uno a cada producto. Después, ejecute la acción **Calcular periodo recuento** de la página **Diario inventario físico** para crear automáticamente líneas para los productos.

1. Elija el icono ![Bombilla que abre la característica Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") entre en **Periodos de recuento de inventario físico** y luego elija el vínculo relacionado.  
2. Rellene los campos según sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

### Asignar un periodo de recuento a un producto

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Productos**, y luego elija el enlace relacionado.  
2. Seleccione el producto al que desea asignar un periodo de recuento.  
3. En el campo **Cód. perio. recuento inv. fís.**, seleccione el periodo de recuento.  

> [!NOTE]
> Si está cambiando el periodo de recuento, un mensaje mostrará información sobre los resultados del cambio. Elija **Sí** para cambiar el código y para calcular el primer periodo de recuento del artículo. La próxima vez que seleccione calcular un periodo de recuento en el diario de inventario físico, el producto aparecerá como una línea en la página **Selección prod. invent. fís.** A continuación, puede contar el producto periódicamente.

### Para empezar a contar basándose en periodos de recuento en las configuraciones básicas de almacén

1. Elija el icono ![Bombilla que abre la característica Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") entre en **Diario inventario físico** y luego elija el vínculo relacionado.
2. Elija la acción **Calcular periodo de recuento**.

    Se abrirá la página **Selección prod. invent. fís.** y mostrará los productos que deben contarse de acuerdo con los periodos de recuento.
3. Cuente el inventario físico. Obtenga más información en [Para contar el inventario físico](inventory-how-count-adjust-reclassify.md#to-count-physical-inventory).

### Para empezar un recuento basándose en periodos de recuento en las configuraciones avanzadas de almacén

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Diario de inventario físico de almacén** y luego elija el enlace relacionado.  
2. Elija la acción **Calcular periodo de recuento**.

    Se abrirá la página **Selección prod. invent. fís.** y mostrará los productos que deben contarse de acuerdo con los periodos de recuento.
3. Cuente el inventario físico. Obtenga más información en [Para contar el inventario físico](inventory-how-count-adjust-reclassify.md#to-count-physical-inventory).  

   > [!NOTE]  
   > Cuente el producto en todas las ubicaciones que lo contienen. Si se eliminan algunas líneas de ubicación que se recuperaron para contar en la página **Almacén. fís. inventario**, el recuento será incorrecto cuando lo registre en el diario de inventario físico.  

## Para ajustar la cantidad de un producto

Una vez que haya realizado el recuento físico de un producto, utilice la acción **Ajustar inventario** para registrar la cantidad real del inventario.

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Productos**, y luego elija el enlace relacionado.
2. Seleccione el producto para el que quiere ajustar el inventario y, a continuación, elija la acción **Ajustar inventario**.
3. En el campo **Nuevo inventario** del almacén, introduzca el resultado del recuento.
4. Elija el botón **Aceptar**.

<!-- I don't see a "Quantity on Hand" field on the Item Card page. Should this point to the options for viewing availability?

The item’s inventory is adjusted. The new quantity is shown in the **Quantity on Hand** field on the **Item Card** page.-->

También puede usar la acción **Ajustar inventario** como una manera sencilla de agregar al inventario los productos comprados si no usa facturas o pedidos de compra para registrar las compras. Obtenga más información en [Registrar compras](purchasing-how-record-purchases.md).

> [!NOTE]  
> Después de ajustar el inventario, actualice su valor actual. Para obtener más información, vea [Revaluación de inventario](inventory-how-revalue-inventory.md).

### Para ajustar las cantidades de varios productos en configuraciones básicas de almacén

En la página **Diario productos**, puede publicar transacciones de productos directamente para ajustar el inventario en relación con compras, ventas y cambios positivos o negativos sin utilizar documentos.

Si utiliza con frecuencia el diario de productos para registrar líneas de diario iguales o parecidas, por ejemplo, relacionadas con el consumo de materiales, puede utilizar la página **Diario productos estándar** para hacer más fácil este trabajo repetitivo. Para obtener más información, consulte [Trabajar con diarios estándar](ui-work-general-journals.md#work-with-standard-journals).

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Diarios de productos**, y luego elija el enlace relacionado.
2. Rellene los campos según sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Elija la acción **Registrar** para ajustar las cantidades.

### Para ajustar las cantidades de la ubicación de configuraciones avanzadas de almacén

Si el almacén utiliza un almacenamiento y un picking dirigidos, use la página **Diario de productos de almacén** para registrar cambios de cantidad positivos o negativos no planificados. Por ejemplo, productos registrados como faltantes que aparecen inesperadamente o pérdidas debido a roturas.  

Los diarios de productos de almacén le brindan más niveles de ajuste para dar más precisión a las cantidades. El almacén sabe cuántos productos hay disponibles y dónde están almacenados, pero no se registran todos los ajustes en el libro mayor de productos. Se realizan créditos o débitos en la ubicación real con el ajuste de cantidad. Se realiza un movimiento de contrapartida en una ubicación de ajuste. La ubicación de ajuste es una ubicación virtual sin productos reales. Especifique la ubicación virtual en el campo **Cód. ubicación ajuste inventario**, en las páginas **Ficha almacén**.

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , entre en **Diarios de productos de almacén** y luego elija el vínculo relacionado.  
2. Rellene la información de la cabecera.  
3. En el campo **N.º producto** de la línea, elija el producto.  
4. Introduzca la ubicación en la que va a colocar los productos adicionales o donde le falten productos.  
5. En el campo **Cantidad**, si ha encontrado productos adicionales, introduzca una cantidad positiva. Si faltan productos, introduzca una cantidad negativa.  
6. Elija la acción **Registrar**.

## Para sincronizar los movimientos ajustados de almacén con los correspondientes movimientos de producto

Contabilice los registros de las ubicaciones de ajuste en el libro mayor de productos para los períodos que haya definido. Algunas empresas registran ajustes a diario en el libro mayor de productos, mientras que otras concilian con menos frecuencia.

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Diario productos**, y luego elija el enlace relacionado.  
2. Rellene los campos de cada línea del diario.  
3. Elija la acción **Calcular ajuste almacén** y luego agregue filtros en la página **Calcular ajuste almacén**. Los ajustes se calculan solo para los movimientos de la ubicación de ajuste que cumplen los requisitos de filtro.  
4. En la ficha desplegable **Opciones**, rellene el campo **Nº documento** con un número que introduzca manualmente. Ya que no se han configurado números de serie para este proceso, utilice el esquema de números que ha configurado para el almacén o introduzca la fecha seguida de sus iniciales.  
5. Elija **Aceptar**. Los ajustes positivos y negativos se suman para cada producto y se crean líneas en el diario de productos.  
6. Registre las líneas del diario para especificar las diferencias de cantidades en el diario de productos. Los inventarios de las ubicaciones y el libro mayor de productos ahora coinciden.  

## Consulte también .

[Contar inventario mediante documentos](inventory-how-count-inventory-with-documents.md)  
[Grupos contables inventario](inventory-manage-inventory.md)  
[Información general de la administración de almacenes](design-details-warehouse-management.md)  
[Ccial](sales-manage-sales.md)  
[Compras](purchasing-manage-purchasing.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
