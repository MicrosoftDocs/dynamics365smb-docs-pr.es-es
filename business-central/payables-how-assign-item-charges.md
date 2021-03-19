---
title: Asignar cargos de producto a ventas y compras | Documentos de Microsoft
description: Si desea que sus productos de inventario carguen costes adicionales, tales como fletes, manipulación física, seguros y transporte en los que incurra al comprar o vender artículos, puede usar la función Gastos de productos.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: transportation, added cost, landed cost
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 7586010a71388f4a9b973387578a388bcdc0b3a0
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5381911"
---
# <a name="use-item-charges-to-account-for-additional-trade-costs"></a>Usar los cargos de producto a cuenta para los costes comerciales adicionales
Para asegurarse de la valoración correcta, sus productos de inventario deben cargar costes adicionales, tales como fletes, manipulación física, seguros y transporte en los que incurra al comprar o vender artículos. Para las compras, el coste de descarga de un producto comprado se compone del precio de compra del proveedor sumado a todos los cargos de producto directos adicionales que se pueden asignar a albaranes o envíos devueltos determinados. Para las compras, conocer el coste de envío de los productos vendidos es tan importante para la empresa como conocer el coste de los productos comprados.

Además de registrar el coste añadido en el valor de inventario, puede usar la función de cargos de producto para:

- Identificar el coste de descarga de un producto para tomar decisiones exactas sobre cómo optimizar la red de distribución.
- Desglosar el coste unitario o el precio de venta de un producto con fines de análisis.
- Incluir las deducciones de compras en el coste unitario y las deducciones de ventas en el precio de venta.

Antes de poder asignar cargos por productos, debe configurar los números de cargos de productos para los diferentes tipos de cargos de productos, incluyendo los costes de cuentas de contables relacionados con ventas, compras y ajustes de inventario. Un número de cargo de producto contiene una combinación de grupo contable de producto, código de grupo de impuesto, grupo de registro IVA producto y cargos de producto. Al introducir el número de coste de producto en un documento de compra o de venta, se obtendrá una cuenta según la configuración del número de coste de producto y la información almacenada en el documento.

Para los documentos de compra y de venta, puede asignar un coste de producto de las siguientes maneras:
- en el documento donde están registrados los productos a los que se refiere el cargo de producto. Esto se suele hacer para los documentos que aún no se han publicado completamente.
- en una factura independiente asociando el cargo de producto a envíos o albaranes registrados en los que figuran los productos a los que se refiere el cargo de producto.

> [!NOTE]  
>   Puede asignar cargos de artículos a pedidos, facturas y abonos para ventas y compras. Los procedimientos siguientes describen cómo gestionar los cargos de producto en una factura de compra. Los pasos son parecidos a los de los documentos de compra y venta.

## <a name="example"></a>Ejemplo:
Este vídeo muestra cómo gestionar un coste de envío adicional como parte de la valoración de existencias.
<br><br>  
> [!Video https://www.microsoft.com/videoplayer/embed/RE4b0SB?rel=0]

## <a name="to-set-up-item-charge-numbers"></a>Configurar números de coste de producto
Los números de cargo de producto sirven para diferenciar los distintos tipos de cargos que se utilizan en la empresa.

1. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Cargos de producto** y luego elija el enlace relacionado.
2. En la página **Cargos producto**, seleccione la acción **Nuevo** para crear una línea nueva.
3. Rellene los campos según sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-assign-an-item-charge-directly-to-the-purchase-invoice-for-the-item"></a>Asignar un coste de producto directamente en la factura de compra del producto
Si conoce el coste de un producto en el momento en que registra la factura de compra, siga este procedimiento.

1. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Facturas de compra** y luego elija el enlace relacionado.
2. Crea una nueva factura de compra. Para obtener más información, consulte [Registrar compras](purchasing-how-record-purchases.md).
3. Asegúrese de que la factura de compra tiene una o más líneas del tipo Producto.
4. En una línea nueva, en el campo **Tipo**, seleccione **Cargo (prod.)**.
5. En el campo **Cantidad**, introduzca las unidades del coste de producto que se han facturado.
6. En el campo **Precio compra**, introduzca el importe del cargo de producto.
7. Rellene los campos restantes según sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    En los siguientes pasos, se efectuará la asignación actual. Hasta que el cargo del producto esté completamente asignado, el valor en el campo **Cdad. para asignar** aparece de color rojo.
8. En la ficha **Líneas**, seleccione la acción **Asignación cargo prod.**.

    La página **Asignación cargos prod.** abre una línea por cada línea del tipo Producto en la factura de compra. Para asignar el cargo de producto a una o más líneas de factura, puede utilizar una función que lo asigne y distribuya automáticamente o puede rellenar manualmente el campo **Cdad. para asignar**. Las siguientes tareas describen cómo utilizar la funcionalidad de la asignación de cargos de producto el menú.

9. En la página **Asignación cargos prod.**, seleccione la acción **Sugerir asignación cargo prod.**
10. Si hay más de una línea de factura del tipo Producto, elija una de las cuatro opciones de distribución.  

El cargo del producto está completamente asignado, el valor de la factura de compra en el campo **Cdad. para asignar** es cero.

El cargo de producto está asignado a la factura de compra. Al registrar la recepción de la factura de compra, los valores de inventario de los elementos se actualizan con el coste del cargo del producto.  

## <a name="to-assign-an-item-charge-from-a-separate-invoice-to-the-purchase-invoice-for-the-item"></a>Asignar un coste de producto de una factura independiente a la factura de compra del producto
Si recibió una factura por el cargo de producto después de haber publicado el recibo de compra original, siga este procedimiento.
1. Repita los pasos del 1 al 8 en [Asignar un coste de producto directamente en la factura de compra del producto](payables-how-assign-item-charges.md#to-assign-an-item-charge-directly-to-the-purchase-invoice-for-the-item).
2. En la página **Asignación cargos prod.**, elija la acción **Traer líns. albarán**.
3. En la página **Líns. recep. compra**, seleccione el albarán de compra registrado para el producto al que desea asignar el cargo de producto y, a continuación, elija el botón **Aceptar**.
4. Seleccione la acción **Sugerir asignación cargo prod.**

El cargo de producto de la factura de compra independiente se asigna al producto en el recibo de compra registrado, y se actualiza el valor de inventario del artículo con el coste del cargo de producto.

## <a name="see-also"></a>Consulte también
[Administrar pagos](payables-manage-payables.md)  
[Registrar compras](purchasing-how-record-purchases.md)  
[Facturar ventas](sales-how-invoice-sales.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]