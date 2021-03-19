---
title: Registrar a nuevos clientes creando una ficha cliente
description: Describe cómo crear una ficha de cliente para registrar información acerca de cada cliente nuevo o existente a los que venda productos.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: client, customer, credit
ms.date: 03/09/2021
ms.author: edupont
ms.openlocfilehash: d873c1546cebfccc6d2549b1de2b9d111589c553
ms.sourcegitcommit: 35f7e24c301926b39094aa64fe608afd04fdb8e1
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 03/10/2021
ms.locfileid: "5573431"
---
# <a name="register-new-customers"></a>Permite registrar nuevos clientes

Los clientes son el origen de los ingresos. Debe registrar cada cliente a quien venda como ficha de cliente. Las fichas de cliente contienen la información necesaria para vender productos al cliente. Para obtener más información, vea [Facturar ventas](sales-how-invoice-sales.md) y [Registrar nuevos productos](inventory-how-register-new-items.md).  

Antes de que pueda registrar nuevos clientes, debe configurar varios códigos de ventas que pueda seleccionar al rellenar fichas de cliente. Para obtener más información, consulte [Configurar ventas](sales-setup-sales.md).

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE3PZsM]

## <a name="adding-new-customers"></a>Agregar nuevos clientes

Para registrar un cliente nueve, debe rellenar una ficha cliente. Puede establecer plantillas para diferentes perfiles de clientes, o puede agregar clientes sin plantillas.  

> [!NOTE]  
> Si existen plantillas de cliente para distintos tipos de cliente, una página aparece automáticamente cuando se crea una nueva ficha de cliente en la que puede seleccionar una plantilla de cliente correspondiente. Si solo existe una plantilla de cliente, las nuevas fichas de cliente utilizan siempre esa plantilla.  

### <a name="to-create-a-new-customer-card"></a>Para crear una nueva ficha cliente.

1. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Clientes** y luego elija el enlace relacionado.  
2. En la página **Clientes**, seleccione la acción **Nuevo**.

    Si solo existe una plantilla de cliente, una nueva ficha de cliente se abre con algunos campos rellenados con la información de la plantilla.

    Si existe más de una plantilla de cliente, se abre una página desde la que puede seleccionar una plantilla de cliente. En ese caso, siga los dos pasos siguientes.
3. En la página **Seleccionar una plantilla para un cliente nuevo**, seleccione la plantilla que quiere usar para la nueva ficha de cliente.
4. Elija el botón **Aceptar**. Una nueva ficha de cliente se abre con algunos campos completados con la información de la plantilla.  
5. Empiece a rellenar o cambiar campos en la ficha de cliente según sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

En la ficha desplegable **Precios venta y descuentos línea ventas**, puede observar los precios especiales o los descuentos que concede al cliente si se cumplen determinados criterios, como, por ejemplo, el producto, la cantidad de pedido mínima o la fecha final. Cada fila representa un precio especial o un descuento de línea. Cada columna representa un criterio aplicable para autorizar el precio especial que se introduzca en el campo **Precio de venta**, o el descuento de línea que se introduzca en el campo **% Descuento línea**. Para más información, vea [Registrar acuerdos de pago, descuentos y precios de venta](sales-how-record-sales-price-discount-payment-agreements.md).

El cliente estará registrado y la ficha de cliente está lista para usarse en los documentos de venta.

Si desea usar esta ficha de cliente como plantilla cuando cree nuevas fichas de cliente, puede guardarla. Para obtener más información, vea la siguiente sección:  

### <a name="to-save-the-customer-card-as-a-template"></a>Para guardar la ficha de cliente como una plantilla

1. En la página **Ficha cliente**, seleccione la acción **Guardar como plantilla**. La página **Plantilla cliente** se abre mostrando la ficha de cliente como plantilla.
2. Rellene los campos según sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Para volver a usar dimensiones en las plantillas, seleccione la acción **Dimensiones**. La página **Plantilla de dimensiones** se abre mostrando los códigos de dimensión configurados para el cliente.
4. Modifique o introduzca los códigos de dimensión que se aplicarán a nuevas fichas de cliente creadas con la plantilla.  
5. Cuando haya finalizado la nueva plantilla de cliente, seleccione el botón de **Aceptar**.

La plantilla de cliente se agrega a la lista de plantillas de cliente, de modo que puede usarla para crear nuevas fichas de cliente.

## <a name="deleting-customer-cards"></a>Eliminar fichas cliente

Si ha publicado una transacción para un cliente, no puede eliminar la ficha porque los movimientos pueden ser necesarias para la auditoría. Para eliminar fichas de cliente con movimientos, póngase en contacto con su socio de Microsoft para hacerlo mediante código.  

## <a name="managing-credit-limits"></a>Administrar los límites de crédito

Los límites de crédito, los importes del saldo y las condiciones de pago permiten que [!INCLUDE [prod_short](includes/prod_short.md)] emita advertencias de crédito y deuda vencida al introducir un pedido de venta.  Además, las instalaciones de términos de recordatorio y de intereses le permiten facturar intereses y/o recargos adicionales.  

El campo **Límite de crédito** de una ficha cliente especifica el importe máximo que le permite al cliente exceder el saldo de pago antes de que se emitan las advertencias. Luego, cuando introduce información en diarios, ofertas, pedidos y facturas, [!INCLUDE [prod_short](includes/prod_short.md)] prueba la cabecera de ventas y las líneas de ventas individuales para ver si se ha excedido el límite de crédito.

Puede registrar, aunque se haya rebasado el límite de crédito. Si este campo se deja en blanco, este cliente no tendrá límite de crédito.  

Puede optar por no recibir advertencias que le indiquen que se excedió el límite de crédito del cliente y puede especificar qué tipos de advertencias desea ver.

### <a name="to-specify-credit-limit-warnings"></a>Para especificar advertencias de límites de crédito

1. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Configuración de ventas y cobros** y luego elija el enlace relacionado.

2. En la ficha desplegable **General**, en el campo **Advertencias de crédito**, elija la opción relevante como se describe en la siguiente tabla:

    |Opción| Descripción|
    |------|------------|
    |**Ambos**| El programa comprueba los campos **Límite de crédito** y **Saldo vencido** de la ficha cliente y le avisa si el cliente ha superado el límite de crédito o si tiene una deuda vencida.|
    |**Límite de crédito**|El valor del campo **Límite de crédito** de la ficha de cliente se compara con el saldo del cliente y se muestra un aviso si dicho saldo supera este importe.|
    |**Deuda vencida**|Se comprueba el campo **Saldo vencido** de la ficha cliente y aparece una advertencia si el cliente tiene una deuda vencida.|
    |**Ninguno**|No se muestra ninguna advertencia acerca del estado del cliente.|

## <a name="see-also"></a>Consulte también

[Definir las formas de pago](finance-payment-methods.md)  
[Combinar registros duplicados](sales-how-merge-duplicate-records.md)  
[Crear numeración](ui-create-number-series.md)  
[Ccial](sales-manage-sales.md)  
[Configuración de ventas](sales-setup-sales.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]