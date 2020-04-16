---
title: Configurar líneas estándar para ventas y compras periódicas | Documentos de Microsoft
description: Puede configurar líneas de ventas y líneas de compras que realice con frecuencia e insertarlas en documentos de venta y compra para rellenar rápidamente las líneas con información estándar.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: trade, sell, replenishment
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: e85d870c73a4c7e5baec449c63f80cc5a4dadf5e
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/01/2020
ms.locfileid: "3195272"
---
# <a name="create-recurring-sales-and-purchase-lines"></a>Crear líneas de ventas y de compras periódicas
Si suele necesitar crear líneas de ventas y de compras con información similar, puede configurar líneas estándar que puede insertar en documentos de ventas y compras periódicas, por ejemplo, para órdenes de reposición periódicas.  

Los siguientes procedimientos muestran cómo trabajar con líneas de ventas estándar en una factura de venta. Funciona de forma similar a todos los demás documentos de venta y todos los documentos de compras.  

## <a name="to-set-up-recurring-sales-lines"></a>Para configurar las líneas de ventas periódicas  
1. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), introduzca **Líneas de ventas periódicas** y luego elija el enlace relacionado.  
2. En la página **Líneas de ventas periódicas**, elija la acción **Nuevo**.  
3. En la ficha desplegable **General**, rellene los campos como sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
4. En la ficha desplegable **Líneas**, introduzca la información en los campos para preparar líneas de ventas que reflejen las líneas estándar que desea utilizar como líneas recurrentes en los documentos de ventas.  

> [!NOTE]
> No puede definir precios en líneas de ventas periódicas porque los precios, descuentos, etc., se calculan en los documentos de ventas reales después de insertar las líneas de ventas periódicas.

## <a name="to-assign-recurring-sales-lines-to-a-customer"></a>Para asignar líneas de ventas periódicas a un cliente
Asigne una o varias líneas de ventas periódicas a un cliente para que estén disponibles para insertarlas en documentos de ventas para ese cliente.

1. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Clientes** y luego elija el enlace relacionado.
2. Abra la ficha de un cliente relevante.
3. Elija la acción **Líneas de ventas periódicas**.
4. En la página **Líneas de ventas periódicas**, seleccione los códigos de las líneas de ventas periódicas que desea insertar en documentos de ventas para el cliente.
5. Rellene los campos adicionales para definir cuándo, cómo y dónde se deben utilizar las líneas de ventas periódicas.
6. En los cuatro campos donde selecciona cómo se insertan las líneas en cuatro tipos de documentos, seleccione una de las siguientes opciones:

|Opción|Descripción|
|-|-|
|**Manual**|Debe buscar manualmente e insertar una línea de venta recurrente que exista para el cliente.|
|**Automática**|Si existen varias líneas de venta recurrentes para el cliente, recibirá una notificación desde donde puede elegir cuál insertar. Si sólo existe una línea de venta recurrente, se insertará automáticamente.<br /><br />Tenga en cuenta que esto solo funciona si el nuevo documento se creó a partir de una lista de documentos, por ejemplo, eligiendo la acción **Nuevo** en la página **Pedidos de venta**. No funciona si el documento se creó a partir de una ficha de cliente, por ejemplo.|
|**Preguntar siempre**|Aparece una notificación y se muestran todas las líneas de venta recurrentes que existen para que pueda seleccionar una.

## <a name="to-insert-recurring-sales-lines-on-a-sales-invoice"></a>Para insertar líneas de ventas periódicas en una factura de ventas
Si existen líneas de ventas periódicas para el cliente, puede insertarlas, o hacer que se inserten, en todos los tipos de documentos de ventas, como una factura de ventas. Si ha activado las opciones de **Preguntar siempre**, se le informará de si existen líneas de ventas periódicas.
1. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Facturas** y luego elija el enlace relacionado.
2. Abra la factura de ventas en la que desee insertar una o varias líneas de ventas estándar.
3. Elija la acción **Obtener líneas de venta periódicas**.
4. En la página **Líneas de ventas periódicas**, elija el botón de búsqueda en el campo **Código** y seleccione un conjunto de líneas de ventas estándar.

    > [!NOTE]
    > Para usar las líneas de ventas recurrentes establecidas junto con el trabajo por lotes **Crear facturas de ventas periódicas**, también debe completar los campos **Válido desde la fecha** y **Válido hasta la fecha** en la página **Líneas de ventas periódicas**. Para obtener más información, consulte [Crear varias facturas de venta basadas en líneas de venta estándar](sales-how-work-standard-lines.md#to-create-multiple-sales-invoices-based-on-standard-sales-lines).

5. Elija el botón **Aceptar** para insertar las líneas de ventas estándar en la factura, donde puede reutilizar la información tal como está o editarla.

## <a name="to-create-multiple-sales-invoices-based-on-standard-sales-lines"></a>Para crear varias facturas de venta basadas en líneas de ventas estándar
Puede utilizar el trabajo por lotes **Crear facturas de venta periódicas** para crear facturas de venta según las líneas de venta estándar asignadas a los clientes y con fechas de registro dentro de las fechas de inicio y fin de validez que especifique en las líneas de ventas estándar.

> [!NOTE]
> En la página **Líneas de ventas periódicas**, también puede especificar una forma de pago por adeudo directo y una orden de domiciliación de adeudo directo. Las facturas de venta que se crean con el trabajo por lotes **Crear facturas de venta periódicas** incluirá la información necesaria para cobrar los pagos por adeudo directo SEPA para las facturas de venta. Para obtener más información, consulte [Cobrar pagos mediante adeudo directo SEPA](finance-collect-payments-with-sepa-direct-debit.md).

1. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), introduzca **Crear facturas de venta periódicas** y luego elija el enlace relacionado.
2. En la página **Crear facturas de venta periódicas**, rellene los campos necesarios.
3. En el campo de filtro **Código**, introduzca el código de las líneas de ventas asignadas a un cliente para el que desee crear las facturas de ventas.
4. Elija el botón **Aceptar**.

Las facturas de venta se crean para los clientes con el código de ventas de cliente estándar especificado y la información de domiciliación especificada, para el registro en la fecha especificada.

## <a name="see-also"></a>Consulte también  
[Ccial](sales-manage-sales.md)  
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
