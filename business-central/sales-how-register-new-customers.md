---
title: Crear una ficha de cliente para registrar clientes nuevos | Documentos de Microsoft
description: Describe cómo crear una ficha de cliente para registrar información acerca de cada cliente nuevo o existente a los que venda productos.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: client
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: e8fd2d876a148c1107b4db1d7c554a79e21bf53d
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/01/2019
ms.locfileid: "2312129"
---
# <a name="register-new-customers"></a>Permite registrar nuevos clientes
Los clientes son el origen de los ingresos. Debe registrar cada cliente a quien venda como ficha de cliente. Las fichas de cliente contienen la información necesaria para vender productos al cliente. Para obtener más información, vea [Facturar ventas](sales-how-invoice-sales.md) y [Registrar nuevos productos](inventory-how-register-new-items.md).  

Antes de que pueda registrar nuevos clientes, debe configurar varios códigos de ventas que pueda seleccionar al rellenar fichas de cliente. Para obtener más información, consulte [Configurar ventas](sales-setup-sales.md).

> [!NOTE]  
>   Si existen plantillas de cliente para distintos tipos de cliente, una página aparece automáticamente cuando se crea una nueva ficha de cliente en la que puede seleccionar una plantilla de cliente correspondiente. Si solo existe una plantilla de cliente, las nuevas fichas de cliente utilizan siempre esa plantilla.

## <a name="to-create-a-new-customer-card"></a>Para crear una nueva ficha cliente.
1. Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Clientes** y luego elija el enlace relacionado.  
2. En la página **Clientes**, seleccione la acción **Nuevo**.

    Si solo existe una plantilla de cliente, una nueva ficha de cliente se abre con algunos campos rellenados con la información de la plantilla.

    Si existe más de una plantilla de cliente, se abre una página desde la que puede seleccionar una plantilla de cliente. En ese caso, siga los dos pasos siguientes.
3. En la página **Seleccionar una plantilla para un cliente nuevo**, seleccione la plantilla que quiere usar para la nueva ficha de cliente.
4. Elija el botón **Aceptar**. Una nueva ficha de cliente se abre con algunos campos completados con la información de la plantilla.  
5. Empiece a rellenar o cambiar campos en la ficha de cliente según sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

En la ficha desplegable **Precios venta y descuentos línea ventas**, puede observar los precios especiales o los descuentos que concede al cliente si se cumplen determinados criterios, como, por ejemplo, el producto, la cantidad de pedido mínima o la fecha final. Cada fila representa un precio especial o un descuento de línea. Cada columna representa un criterio aplicable para autorizar el precio especial que se introduzca en el campo **Precio de venta**, o el descuento de línea que se introduzca en el campo **% Descuento línea**. Para más información, vea [Registrar acuerdos de pago, descuentos y precios de venta](sales-how-record-sales-price-discount-payment-agreements.md).

El cliente estará registrado y la ficha de cliente está lista para usarse en los documentos de venta.

Si desea usar esta ficha de cliente como plantilla cuando cree nuevas fichas de cliente, puede guardarla. Para obtener más información, vea la siguiente sección:

## <a name="to-save-the-customer-card-as-a-template"></a>Para guardar la ficha de cliente como una plantilla
1. En la página **Ficha cliente**, seleccione la acción **Guardar como plantilla**. La página **Plantilla cliente** se abre mostrando la ficha de cliente como plantilla.
2. Rellene los campos según sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Para volver a usar dimensiones en las plantillas, seleccione la acción **Dimensiones**. La página **Plantilla de dimensiones** se abre mostrando los códigos de dimensión configurados para el cliente.
4. Modifique o introduzca los códigos de dimensión que se aplicarán a nuevas fichas de cliente creadas con la plantilla.  
5. Cuando haya finalizado la nueva plantilla de cliente, seleccione el botón de **Aceptar**.

La plantilla de cliente se agrega a la lista de plantillas de cliente, de modo que puede usarla para crear nuevas fichas de cliente.

## <a name="see-also"></a>Consulte también
[Definir las formas de pago](finance-payment-methods.md)  
[Combinar registros duplicados](sales-how-merge-duplicate-records.md)  
[Crear numeración](ui-create-number-series.md)  
[Ventas](sales-manage-sales.md)    
[Configuración de ventas](sales-setup-sales.md)    
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
