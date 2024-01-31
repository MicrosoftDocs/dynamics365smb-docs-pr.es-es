---
author: brentholtorf
ms.topic: include
ms.date: 10/05/2022
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
Cuando haya agregado todos los productos en las líneas, podrá calcular el descuento en factura para todo el documento de venta eligiendo la acción **Calcular descuento en factura**.

El descuento se calcula sobre la base de todas las líneas del documento de venta en las que se ha seleccionado la casilla de verificación **Permitir dto. factura**. De forma predeterminada, se permiten descuentos en facturas. Sin embargo, las líneas con cargos de producto, por ejemplo, no se incluyen en el cálculo del descuento de factura. Para aplicar un descuento a dichas líneas, introduzca un valor en el campo **Importe dto. línea** de las líneas.  

> [!NOTE]
> De forma predeterminada, los campos **Permitir dto. factura** y **Importe dto. línea** están ocultos en las líneas. Si los campos no están disponibles, puede agregarlos personalizando la página. Para obtener más información, consulte [Personalizar el área de trabajo](../ui-personalization-user.md#start-personalizing-by-using-the-personalization-mode).

> [!TIP]
> Si se selecciona el campo **Calc. dto. factura** en la página **Conf. ventas y cobros**, el descuento en factura se calculará automáticamente. El momento en que se produce el cálculo difiere, según el tipo de documento de venta que se use.
>
> Si usa un pedido de ventas, el descuento se calcula cuando se agrega una línea. Para todos los demás documentos de venta, como las facturas de venta, el descuento se calcula cuando se realiza alguna de las siguientes acciones:
>
> * Ver estadísticas
> * Ver un test
> * Imprimir
> * Envíos postales

Se definen las condiciones de descuento en factura para un cliente en la página **Descuentos en factura de cliente**. El código de divisa del documento de venta se usa para buscar las condiciones de descuento en factura en la divisa correspondiente.

Si no ha definido los descuentos en factura para las divisas extranjeras, las condiciones de descuento de la página **Dtos. factura cliente** se usan para calcular el descuento. El cálculo utiliza su divisa local y el tipo de cambio vigente en la fecha de contabilización del documento.
