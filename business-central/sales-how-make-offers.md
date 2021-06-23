---
title: Crear una oferta de venta a un cliente
description: Describe cómo crear una oferta de venta o un documento de solicitud de propuesta (RFQ) para registrar la oferta a un cliente para vender productos con determinadas condiciones.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: rfq
ms.date: 05/27/2021
ms.author: edupont
ms.openlocfilehash: a538b7099521b10227bf5aeaefad0a9c60971068
ms.sourcegitcommit: f9a190933eadf4608f591e2f1b04c69f1e5c0dc7
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 05/28/2021
ms.locfileid: "6115545"
---
# <a name="make-sales-quotes"></a>Crear ofertas de ventas

Puede crear una oferta de venta para registrar la oferta a un cliente para vender determinados productos según términos de entrega y pago determinados. Puede enviar la oferta de venta al cliente para comunicar la oferta. Puede enviar por correo electrónico el documento como un documento PDF anexo. También puede rellenar previamente el cuerpo del correo electrónico con un resumen de la oferta. Para obtener más información, vea [Enviar documentos por correo electrónico](ui-how-send-documents-email.md).

Mientras negocia con el cliente, puede cambiar y reenviar la oferta de venta el número de veces necesario. Cuando el cliente acepta la oferta, convierte la oferta de venta a una factura de venta o un pedido de venta en el que se procesa la venta. Para obtener más información, consulte [Facturar ventas](sales-how-invoice-sales.md) o [Vender productos](sales-how-sell-products.md).

Puede rellenar los campos de clientes en la oferta de venta de dos formas en función de si el cliente ya está registrado. Consulte los pasos 2 y 3 del siguiente procedimiento.

## <a name="to-create-a-sales-quote"></a>Para crear una oferta de venta

1. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Ofertas de venta** y luego elija el enlace relacionado.
2. En el campo **Cliente**, escriba el nombre de un cliente existente.

   Otros campos de la página **Oferta de venta** contienen información estándar del cliente seleccionado.  

    [!INCLUDE [sales-create-customer](includes/sales-create-customer.md)]

    Muchos campos de la oferta de venta se rellenan con la información especificada en la nueva ficha de cliente.  
3. Rellene los campos en la página **Oferta venta** según sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

    Ahora podrá rellenar las líneas de la factura de pedido de los productos que vende al cliente o para cualquier transacción con el cliente que desee registrar en una cuenta de contabilidad.  

    Si ha configurado líneas de venta periódicas para el cliente, como por ejemplo un pedido de reabastecimiento mensual, puede insertar estas líneas en el pedido seleccionando la acción **Obtener líneas de venta periódicas**.  

4. En la ficha desplegable **Líneas** del campo **Tipo**, seleccione qué tipo de producto, cargo o transacción registrará para el cliente en la línea de venta.
5. En el campo **N.º**, seleccione un registro para registrar según el valor del campo **Tipo**.

    Deje el campo **N.º** vacío en los casos siguientes:
    - Si la línea es de un comentario. Escriba el comentario en el campo **Descripción**.
    - Si la línea es de un producto del catálogo. Elija la acción **Seleccionar artículos del catálogo**. Para obtener más información, consulte [Trabajar con productos del catálogo](inventory-how-work-nonstock-items.md).

6. En el campo **Cantidad**, especifique cuántas unidades de producto, cargo o transacción registrará la línea para el cliente.

    > [!NOTE]  
    >  Si el producto es de tipo **Servicio** o el campo **Tipo** contiene **Recurso**, la cantidad es una unidad de tiempo, por ejemplo horas, según se indica en el campo **Cód. unidad medida** en la línea. Para obtener más información, vea [Configurar unidades de medida de producto](inventory-how-setup-units-of-measure.md)

    El valor del campo **Importe línea** se calculará como *Precio venta* x *Cantidad*.  

    El precio y el importe de las líneas tienen IVA o no, dependiendo de qué seleccione en el campo **Precios incluyendo IVA** en la ficha del cliente.  
7. Si desea ofrecer un descuento, introduzca un porcentaje en el campo **% Descuento línea**. El valor del campo **Importe de línea** se actualiza según corresponde.  

    Si hay configurados precios de producto especiales en la ficha desplegable **Precios venta y descuentos línea ventas** en la ficha del producto o en la del cliente, el precio y el importe de la línea de venta se actualizan automáticamente si se cumplen los criterios acordados para el precio. Para más información, vea [Registrar acuerdos de pago, descuentos y precios de venta](sales-how-record-sales-price-discount-payment-agreements.md).  
8. Repita los pasos 4 a 7 para cada producto que desee ofertar al cliente.

    Los totales por debajo de las líneas se calculan automáticamente cuando se crean o modifican las líneas.  
9. En el campo **Importe descuento factura**, especifique un importe que se debe descontar del valor que aparece en el campo **Total impuesto incl.** en la parte inferior de la factura.

    Si ha configurado descuentos en factura para el cliente, el valor porcentual especificado se inserta automáticamente en el campo **% descuento en factura** si se cumplen los criterios, y el importe relacionado se inserta en el campo **Descuento en factura excluyendo impuesto** . Para más información, vea [Registrar acuerdos de pago, descuentos y precios de venta](sales-how-record-sales-price-discount-payment-agreements.md).

    > [!TIP]
    > Para que la **Oferta válida hasta fecha** se complete automáticamente con un número determinado de días después de la creación de la oferta, puede completar el campo **Cálculo de validez de la oferta** en la página **Ventas y cobros**.

10. Cuando las líneas de la oferta de venta ya estén completas, seleccione la acción **Enviar por correo electrónico**.
11. En la página **Enviar correo electrónico**, rellene los campos restantes y revise la oferta de venta incluida. Para obtener más información, vea [Enviar documentos por correo electrónico](ui-how-send-documents-email.md).
12. Si el cliente acepta la oferta, seleccione la acción **Generar factura** o **Realizar pedido**.

La oferta de venta se quita de la base de datos. Una factura de venta o un pedido de venta se crea a partir de la información en la oferta de venta en la que puede procesar la venta. En el campo **Nº oferta** de la factura de venta o pedido de venta, se muestra el número de la oferta de venta a partir de la que se creó. Para obtener más información, consulte [Facturar ventas](sales-how-invoice-sales.md) o [Vender productos](sales-how-sell-products.md).  

## <a name="external-document-number"></a>Número de documento externo

[!INCLUDE [ext-doc-no-sales](includes/ext-doc-no-sales.md)]

## <a name="see-also"></a>Consulte también

[Ccial](sales-manage-sales.md)  
[Configuración de ventas](sales-setup-sales.md)  
[Enviar documentos por correo electrónico](ui-how-send-documents-email.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]