---
title: Registrar a nuevos clientes creando una ficha cliente (contiene vídeo)
description: Describe cómo crear una ficha de cliente para registrar información acerca de cada cliente nuevo o existente a los que venda productos.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'client, customer, credit'
ms.search.form: '7, 21, 22, 33, 42, 43, 367, 368, 369, 461, 512, 785, 1330, 1380, 1381, 1382, 1627, 2107, 7177, 9080, 9081, 9084, 9301, 9305'
ms.date: 09/01/2022
ms.author: edupont
---
# <a name="register-new-customers" />Permite registrar nuevos clientes

Los clientes son el origen de los ingresos. Debe registrar cada cliente a quien venda como ficha de cliente. Las fichas de cliente contienen la información necesaria para vender productos al cliente. Obtenga más información en [Facturar ventas](sales-how-invoice-sales.md) y [Registrar nuevos productos](inventory-how-register-new-items.md).  

Antes de que pueda registrar nuevos clientes, debe configurar varios códigos de ventas para seleccionar al rellenar fichas de cliente. Obtenga más información en [Configurar ventas](sales-setup-sales.md).


> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE3PZsM]

## <a name="adding-new-customers" />Agregar nuevos clientes

Puede agregar nuevos clientes manualmente, completando la página **Ficha de cliente**, o puede utilizar plantillas que contienen información predefinida. Por ejemplo, puede crear una plantilla para diferentes tipos de perfiles de clientes. El uso de plantillas ahorra tiempo al agregar nuevos clientes y ayuda a garantizar que la información sea correcta en todo momento. 

Si crea:
* Varias plantillas para más de un tipo de cliente, puede elegir la plantilla adecuada cuando agregue un cliente.
* Solo una plantilla, se utilizará para todos los clientes nuevos. 

Después de crear una plantilla, puede usar la acción **Aplicar plantilla** para aplicarla a uno o más clientes seleccionados. Para crear una plantilla, complete la información que desea reutilizar en la página **Ficha de cliente** y luego guárdela como una plantilla. Obtenga más información en la sección [Para guardar la ficha de cliente como plantilla](sales-how-register-new-customers.md#to-save-the-customer-card-as-a-template).

> [!TIP]
> Puede resultar útil personalizar la página **Ficha de cliente** cuando crea una plantilla. Por ejemplo, es posible que desee agregar el campo **Límite de crédito** a una plantilla. Obtenga más información en la sección [Personalizar el área de trabajo](/dynamics365/business-central/ui-personalization-user#to-start-personalizing-a-page-through-the-personalizing-banner).

También puede crear un cliente a partir de un contacto. Obtenga más información en la sección [Para crear un contacto como proveedor, empleado o banco de un contacto](marketing-create-contact-companies.md#to-create-a-customer-vendor-employee-or-bank-account-from-a-contact).  

### <a name="to-create-a-new-customer-card" />Para crear una nueva ficha cliente.

[!INCLUDE[create_new_customer](includes/create_new_customer.md)]

La acción **Precios y descuentos** proporciona opciones para administrar precios especiales o descuentos para un cliente cuando un pedido cumple con ciertos criterios. Por ejemplo, los criterios pueden ser cuándo compran un artículo determinado, solicitan una cantidad mínima o compran antes de una fecha, como, por ejemplo, cuando finaliza una campaña. Obtenga más información en [Registrar acuerdos de pago, descuentos y precios de venta](sales-how-record-sales-price-discount-payment-agreements.md).

El cliente estará registrado y la ficha de cliente está lista para usarse en los documentos de venta.  

### <a name="to-save-the-customer-card-as-a-template" />Para guardar la ficha de cliente como una plantilla

Puede usar una ficha de cliente como plantilla cuando cree nuevas fichas de cliente.

1. En la página **Ficha cliente**, seleccione la acción **Guardar como plantilla**. La página **Plantilla cliente** se abre mostrando la ficha de cliente como plantilla.
2. Rellene los campos según sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Para volver a usar dimensiones en las plantillas, seleccione la acción **Dimensiones**. La página **Plantilla de dimensiones** se abre mostrando los códigos de dimensión configurados para el cliente.
4. Modifique o introduzca los códigos de dimensión que desea aplicará a nuevas fichas de cliente creadas con esta plantilla.  
5. Cuando haya finalizado la nueva plantilla de cliente, seleccione **Aceptar**.

La plantilla de cliente se agrega a la lista de plantillas de cliente y puede usarla para crear nuevas fichas de cliente.

## <a name="deleting-customer-cards" />Eliminar fichas cliente

Si ha publicado una transacción para un cliente, no puede eliminar la ficha de cliente porque los movimientos pueden ser necesarias para la auditoría. Para eliminar fichas de cliente con movimientos, póngase en contacto con su socio de Microsoft para hacerlo mediante código.  

## <a name="managing-credit-limits" />Administrar los límites de crédito

Los límites de crédito, los importes del saldo y las condiciones de pago permiten que [!INCLUDE [prod_short](includes/prod_short.md)] emita advertencias de crédito y deuda vencida al introducir un pedido de venta. Además, los elementos de términos de recordatorio y de intereses le permiten facturar intereses y/o recargos adicionales.  

El campo **Límite de crédito** de una ficha cliente especifica el importe máximo que le permite al cliente exceder el saldo de pago antes de que se emitan las advertencias. Luego, cuando introduce información en diarios, ofertas, pedidos y facturas, [!INCLUDE [prod_short](includes/prod_short.md)] prueba la cabecera de ventas y las líneas de ventas individuales para ver si se ha excedido el límite de crédito.

Puede registrar, aunque se haya rebasado el límite de crédito. Si este campo se deja en blanco, este cliente no tendrá límite de crédito.  

Puede optar por no recibir advertencias que le indiquen que se excedió el límite de crédito del cliente y puede especificar qué tipos de advertencias desea ver.

### <a name="to-specify-credit-limit-warnings" />Para especificar advertencias de límites de crédito

1. Elija el icono ![Bombilla que abre la característica Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Configuración de ventas y cobros** y luego elija el enlace relacionado.

2. En la ficha desplegable **General**, en el campo **Advertencias de crédito**, elija la opción relevante como se describe en la siguiente tabla:

    |Opción| Descripción|
    |------|------------|
    |**Ambos**| El programa comprueba los campos **Límite de crédito** y **Saldo vencido** de la ficha cliente y le avisa si el cliente supera el límite de crédito o si tiene una deuda vencida.|
    |**Límite de crédito**|El valor del campo **Límite de crédito** de la ficha de cliente se compara con el saldo del cliente y se muestra un aviso si dicho saldo supera este importe.|
    |**Deuda vencida**|Se comprueba el campo **Saldo vencido** de la ficha cliente y aparece una advertencia si el cliente tiene una deuda vencida.|
    |**Ninguno**|No se muestra ninguna advertencia acerca del estado del cliente.|

## <a name="see-related-microsoft-trainingtrainingmodulestrade-master-data-dynamics-365-business-central" />Consultar la [formación de Microsoft](/training/modules/trade-master-data-dynamics-365-business-central/) relacionada.

## <a name="see-also" />Consulte también .

[Definir las formas de pago](finance-payment-methods.md)  
[Combinar registros duplicados](sales-how-merge-duplicate-records.md)  
[Crear numeración](ui-create-number-series.md)  
[Permitir envíos parciales con aviso de envío](sales-how-send-partial-shipments.md)  
[Ccial](sales-manage-sales.md)  
[Configuración de ventas](sales-setup-sales.md)  
[Usar Mapas en línea para encontrar ubicaciones e indicaciones](across-online-maps.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
