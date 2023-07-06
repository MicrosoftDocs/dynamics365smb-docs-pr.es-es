---
title: Líneas de venta periódicas estándar
description: Configure líneas de ventas que realice con frecuencia para insertarlas en documentos de venta y rellenar rápidamente las líneas con información estándar.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'trade, sell, replenishment'
ms.search.form: 172
ms.date: 07/06/2022
ms.author: edupont
---
# <a name="create-recurring-sales"></a><a name="create-recurring-sales"></a><a name="create-recurring-sales"></a><a name="create-recurring-sales"></a>Crear ventas periódicas

Si suele necesitar crear líneas de ventas con información similar, puede configurar líneas estándar que puede insertar en documentos de ventas periódicas, por ejemplo, para órdenes de reposición periódicas.  

## <a name="set-up-recurring-sales-lines"></a><a name="set-up-recurring-sales-lines"></a><a name="set-up-recurring-sales-lines"></a><a name="set-up-recurring-sales-lines"></a>Configurar las líneas de ventas periódicas

1. Elija el icono ![Bombilla que abre la característica Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Líneas de ventas periódicas** y, a continuación, elija el vínculo relacionado.  
2. En la página **Líneas de ventas periódicas**, elija la acción **Nuevo**.  
3. En la ficha desplegable **General**, rellene los campos como sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
4. En la ficha desplegable **Líneas**, introduzca la información en los campos para preparar líneas de ventas que reflejen las líneas estándar que desea utilizar como líneas recurrentes en los documentos de ventas.  

> [!NOTE]
> No puede definir precios en líneas de ventas periódicas porque los precios, descuentos, etc., se calculan en los documentos de ventas reales después de insertar las líneas de ventas periódicas.

[!INCLUDE [line-no-info](includes/line-no-info.md)]

## <a name="assign-recurring-sales-lines-to-a-customer"></a><a name="assign-recurring-sales-lines-to-a-customer"></a><a name="assign-recurring-sales-lines-to-a-customer"></a><a name="assign-recurring-sales-lines-to-a-customer"></a>Asignar líneas de ventas periódicas a un cliente

Asigne una o varias líneas de ventas periódicas a un cliente para que estén disponibles para insertarlas en documentos de ventas para ese cliente.

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Clientes** y luego elija el enlace relacionado.
2. Abra la ficha de un cliente relevante.
3. Elija la acción **Líneas de ventas periódicas**.
4. En la página **Líneas de ventas periódicas**, seleccione los códigos de las líneas de ventas periódicas que desea insertar en documentos de ventas para el cliente.
5. Rellene los otros campos para definir cuándo, cómo y dónde se deben utilizar las líneas de ventas periódicas.  

    Si planea utilizar las líneas de ventas periódicas establecidas junto con el trabajo por lotes **Crear facturas de venta periódicas**, use los campos **Fecha inicial válida** y **Fecha final válida** para restringir cuándo se utilizan las líneas de ventas periódicas para la creación de facturas. Para obtener más información, consulte [Crear varias facturas de venta basadas en líneas de venta estándar](sales-how-work-standard-lines.md#create-multiple-sales-invoices-based-on-recurring-sales-lines).

    También puede especificar una forma de pago por adeudo directo y una orden de domiciliación de adeudo directo. Las facturas de venta que se crean con el trabajo por lotes **Crear facturas de venta periódicas** incluirá la información necesaria para cobrar los pagos por adeudo directo SEPA. Para obtener más información, consulte [Cobrar pagos mediante adeudo directo SEPA](finance-collect-payments-with-sepa-direct-debit.md).

6. En los cuatro campos donde selecciona cómo se insertan las líneas en cuatro tipos de documentos, seleccione una de las siguientes opciones:

|Opción|Descripción|
|------|-----------|
|**Manual**|Debe buscar manualmente e insertar una línea de venta recurrente que exista para el cliente.|
|**Automática**|Si existen varias líneas de venta recurrentes para el cliente, recibirá una notificación desde donde puede elegir cuál insertar. Si sólo existe una línea de venta recurrente, se insertará automáticamente.<br /><br />Esto solo funciona si el nuevo documento se creó a partir de una lista de documentos, por ejemplo, eligiendo la acción **Nuevo** en la página **Pedidos de venta**. No funciona si el documento se creó a partir de una ficha de cliente, por ejemplo.|
|**Preguntar siempre**|Aparece una notificación y se muestran todas las líneas de venta recurrentes que existen para que pueda seleccionar una.

## <a name="insert-recurring-sales-lines-on-a-sales-invoice"></a><a name="insert-recurring-sales-lines-on-a-sales-invoice"></a><a name="insert-recurring-sales-lines-on-a-sales-invoice"></a><a name="insert-recurring-sales-lines-on-a-sales-invoice"></a>Insertar líneas de ventas periódicas en una factura de ventas

Si existen líneas de ventas periódicas para el cliente, puede insertarlas, o hacer que se inserten, en todos los tipos de documentos de ventas, como una factura de ventas. Si ha activado las opciones de **Preguntar siempre** al asignar líneas de ventas periódicas a los clientes, se le informará de si existen líneas de ventas periódicas.

1. Elija el icono ![Bombilla que abre la característica Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Facturas venta** y luego elija el enlace relacionado.
2. Abra la factura de ventas en la que desee insertar una o varias líneas de ventas estándar.
3. Elija la acción **Obtener líneas de venta periódicas**.
4. En la página **Líneas de ventas periódicas**, elija el botón de búsqueda en el campo **Código** y seleccione un conjunto de líneas de ventas estándar.
5. Elija el botón **Aceptar** para insertar las líneas de ventas estándar en la factura, donde puede reutilizar la información tal como está o editarla.

## <a name="create-multiple-sales-invoices-based-on-recurring-sales-lines"></a><a name="create-multiple-sales-invoices-based-on-recurring-sales-lines"></a><a name="create-multiple-sales-invoices-based-on-recurring-sales-lines"></a><a name="create-multiple-sales-invoices-based-on-recurring-sales-lines"></a>Crear varias facturas de venta basadas en líneas de ventas periódicas

Puede utilizar el trabajo por lotes **Crear facturas de venta periódicas** para crear facturas de venta según las líneas de venta estándar asignadas a los clientes y con fechas de registro dentro de las fechas de inicio y fin de validez que especifique en las líneas de ventas estándar.

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Crear facturas de venta periódicas** y, a continuación, elija el vínculo relacionado.
2. En la página **Crear facturas de venta periódicas**, rellene los campos necesarios.
3. En el campo de filtro **Código**, introduzca el código de las líneas de ventas asignadas a un cliente para el que desee crear las facturas de ventas.
4. Elija el botón **Aceptar**.

Las facturas de venta se crean para los clientes con el código de ventas de cliente estándar especificado y la información de domiciliación especificada, para el registro en la fecha especificada.

## <a name="see-related-microsoft-training"></a><a name="see-related-microsoft-training"></a><a name="see-related-microsoft-training"></a><a name="see-related-microsoft-training"></a>Consultar la [formación de Microsoft](/training/modules/create-sales-documents-dynamics-365-business-central/) relacionada

## <a name="see-also"></a><a name="see-also"></a><a name="see-also"></a><a name="see-also"></a>Consulte también .

[Ccial](sales-manage-sales.md)  
[Configurar ventas](sales-setup-sales.md)  
[Crear líneas de compra periódicas](purchasing-how-work-recurring-purchase-lines.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
