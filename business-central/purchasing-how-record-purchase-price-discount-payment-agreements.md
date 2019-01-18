---
title: Precios y descuentos especiales y alternativos para proveedores | Documentos de Microsoft'
description: Puede definir precios y acuerdos de descuentos distintos o alternativos, y aplicarlos a los documentos de compra para proveedores.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: special price, alternate price, pricing
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 33b900f1ac9e295921e7f3d6ea72cc93939d8a1b
ms.openlocfilehash: 0a718c45256a1e7cc7fbde794491814f1c26dd4a
ms.contentlocale: es-es
ms.lasthandoff: 11/26/2018

---
# <a name="record-special-purchase-prices-and-discounts"></a>Registrar precios y descuentos de compra especiales
Los diferentes acuerdos de precio y descuentos que se aplican cuando compra a distintos proveedores se deben definir para que las reglas y valores acordados se apliquen a los documentos de compra que se crean para los proveedores.

Cuando haya registrado precios especiales y los descuentos de línea para ventas y compras, [!INCLUDE[d365fin](includes/d365fin_md.md)] garantiza que el beneficio en operaciones comerciales de producto siempre son óptimos calculando automáticamente el mejor precio en los documentos de ventas y compras, y en líneas del diario de proyectos y recursos. Para obtener más información, consulte la sección "Cálculo del mejor precio".

Respecto a los precios, puede tener una precio especial de compra insertado en las líneas de compra si existe una cierta combinación de proveedor, producto, cantidad mínima, unidad de medida o fecha de inicio o de fin.

Respecto a los descuentos, puede configurar y usar dos tipos de descuentos de compra:

| Tipo de descuento | Descripción |
| --- | --- |
| **Descuento línea compra** |Un importe de descuento que está insertado en las líneas de compra si existe una cierta combinación de proveedor, producto, cantidad mínima, unidad de medida o fecha de inicio o de fin. Funciona igual que para los precios de compra. |
| **Descuento en factura** |Un porcentaje de descuento que se resta del total del documento si el importe de todas las líneas de un documento de compra supera cierto límite. |

Puesto que los descuentos de línea y los precios de compra se basan en una combinación de producto y proveedor, también se puede introducir esta combinación desde la ficha de producto en la que se definen las reglas y los valores. Para obtener más información, vea [Registrar nuevos productos](inventory-how-register-new-items.md).

## <a name="to-set-up-a-special-purchase-price-for-a-vendor"></a>Para configurar un precio de compra especial para un proveedor
1. Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Proveedores** y luego elija el enlace relacionado.
2. Abra la ficha de proveedor correspondiente y, a continuación, elija la acción **Precios**.

    El campo **Tipo de compras** se rellena previamente con el campo **Proveedor** y el campo **Código de compre** se rellena con el número del proveedor.
3. Rellene los campos de la línea como sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Rellene una línea para cada combinación por la que el proveedor le garantiza un descuento de compra.

## <a name="to-set-up-a-line-discount-for-a-vendor"></a>Para configurar un descuento de línea para un proveedor
1. Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Proveedores** y luego elija el enlace relacionado.
2. Abra la ficha de proveedor correspondiente y, a continuación, elija la acción **Dto. línea**.

    El campo **Tipo de compras** se rellena previamente con el campo **Proveedor** y el campo **Código de compre** se rellena con el número del proveedor.
3. Rellene los campos de la línea como sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Rellene una línea para cada combinación por la que el proveedor le garantiza un descuento de compra.

## <a name="to-set-up-an-invoice-discount-for-a-vendor"></a>Para configurar términos de descuento en factura para un proveedor:
Una vez su proveedor le haya informado de que descuentos en factura garantizan, introduzca el código de descuento en las fichas de cliente y especifique los términos de cada código.

1. Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Proveedores** y luego elija el enlace relacionado.
2. Abra la ficha de un proveedor que pueda obtener descuentos en factura.
3. En el campo **Código descuento factura**, seleccione un código para los términos relevantes de la factura con descuentos que usará para calcular los descuentos en facturas para el proveedor.

    > [!NOTE]  
    >   Los códigos de descuento en factura se representan por las fichas existentes del proveedor. Lo que permite asignar rápidamente las condiciones de descuento en factura a proveedores realizando el picking del nombre de otros proveedores con los mismos términos.

    Configure de nuevo los términos de descuento en factura para compras.
4. En la página **Ficha proveedor**, seleccione la acción **Descuento factura**. Aparecerá la página **Dtos. factura proveedores**.
5. En el campo **Código divisa**, introduzca el código de una divisa que se aplique a los términos de descuento en factura en la línea. Deje el campo en blanco para establecer condiciones de descuento de factura en la divisa local.
6. En el campo **Importe mínimo**, escriba el importe mínimo que deba tener una factura para optar al descuento.
7. En el campo **% descuento**, introduzca el descuento en la factura como un porcentaje del importe de la factura.
8. Repita los pasos 5 a 7 para cada divisa para la que el proveedor va a recibir un descuento diferente de factura.

El descuento en factura está configurado y asignado el proveedor en cuestión. En el momento que selecciona el código de proveedor en el campo **Código de descuento de factura** en las fichas de proveedores, se asigna el mismo descuento en factura a ese proveedor.

## <a name="to-choose-a-principle-for-posting-purchase-discounts"></a>Para seleccionar un principio de registro para descuentos de compra  
Cuando se registra una factura de compra que incluye uno o varios descuentos, puede escoger entre dos principios de registro de importes de descuento. Puede registrar los descuentos por separado o restar los descuentos de los descuentos en factura.  

Antes de que pueda hacerlo, deberá haber configurado las cuentas necesarias para registrar importes de descuento en el plan de cuentas. También debe comprobar que haya escrito los números de cuenta correctos en la configuración de grupos contables de los campos **Cta. dto. línea compras** y **Cta. dto. factura compras**.

1. Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Configuración compras y pagos** y luego elija el enlace relacionado.
2. En el campo **Registro dto.**, seleccione uno de los siguientes principios de registro de descuentos.

|**Principio de registro de descuento**|**Descuento en factura**|**Descuento en línea**|  
|------------------------------------|--------------------------|-----------------------|  
|**Todos**|Registrado por separado|Registrado por separado|  
|**Dto. factura**|Registrado por separado|Restado|  
|**Dto. línea**|Restado|Registrado por separado|  
|**Ninguno**|Restado|Restado|  

## <a name="purchase-invoice-discounts-and-service-charges"></a>Descuentos y cargos por servicios de la factura de compra
Si aplica términos fijos para los descuentos en factura a algunos proveedores, podrá introducirlos para esos proveedores. Se calculará el descuento cuando rellene una factura de compra.  

 Para poder utilizar descuentos en factura en las compras, deberá especificar los proveedores que le ofrecen los descuentos.  

 Se relacionan los porcentajes de descuento a los importes de factura específicos en las páginas **Dtos. factura proveedores**. Puede introducir un número ilimitado de porcentajes en cada página. Cada proveedor puede tener su propia página o se pueden vincular varios proveedores a la misma página.  

 Además de un porcentaje de descuento, puede vincular un importe de cargo por servicios a un importe facturado específico.  

 Puede definir los términos de los descuentos en factura en DL para los proveedores nacionales y en otras divisas para los proveedores de otros países.  

 Puede optar por que [!INCLUDE[d365fin](includes/d365fin_md.md)] calcule automáticamente los descuentos en factura de ofertas, pedidos abiertos, pedidos, facturas o abonos.  

> [!TIP]  
>  Antes de introducir esta información, se recomienda preparar un esquema de la estructura de descuentos que desea utilizar. De este modo, podrá ver fácilmente los proveedores que se pueden vincular a la misma página de descuentos en factura. Cuantas menos páginas tenga que configurar, más rápido podrá introducir la información básica.

## <a name="best-price-calculation"></a>Cálculo del mejor precio
Cuando haya registrado precios especiales y los descuentos de línea para ventas y compras, [!INCLUDE[d365fin](includes/d365fin_md.md)] garantiza que el beneficio en operaciones comerciales de producto siempre son óptimos calculando automáticamente el mejor precio en los documentos de ventas y compras, y en líneas del diario de proyectos y recursos.

El mejor precio es el precio más bajo permisible con el mayor descuento de línea permisible en una fecha indicada. [!INCLUDE[d365fin](includes/d365fin_md.md)] lo calcula automáticamente al insertar el precio por unidad y el porcentaje de descuento de línea de los productos en las nuevas líneas de documento y diario.

> [!NOTE]  
>   A continuación se describe cómo se calcula el mejor precio para las ventas. El cálculo es igual para las compras.

1. [!INCLUDE[d365fin](includes/d365fin_md.md)] comprueba la combinación de la factura a cliente y el producto, y calcula el precio por unidad y el porcentaje de descuento de línea aplicables utilizando los siguientes criterios:

    - ¿El cliente tiene un acuerdo de precios o descuentos, o el cliente pertenece a un grupo que lo tiene?
    - ¿Está incluido el producto o el grupo de descuento del producto de la línea en alguno de estos acuerdos de precios o descuentos?
    - ¿La fecha de pedido (o la fecha de registro de la factura y abono) está comprendida entre la fecha inicial y la fecha final del acuerdo de precios o descuentos?
    - ¿Se ha especificado un código de unidad de medida? Si es así, [!INCLUDE[d365fin](includes/d365fin_md.md)] comprueba los precios o descuentos con el mismo código de unidad de medida y los precios o descuentos sin un código de unidad de medida.

2. [!INCLUDE[d365fin](includes/d365fin_md.md)] comprueba si se aplican acuerdos de precios o de descuentos a la información de la línea de documento o de diario y, a continuación, inserta el precio unitario y porcentaje de descuento de línea, utilizando el siguiente criterio:

    - ¿Hay un requisito de cantidad mínima en el acuerdo de precios o descuentos que se debe cumplir?
    - ¿Hay un requisito de divisa en el acuerdo de precios o descuentos que se debe cumplir? Si es así, se insertan el precio más bajo y el descuento de línea más alto para esa divisa, incluso si la DL proporciona un precio mejor. Si no existen acuerdos de precios o descuentos para el código de divisa especificado, [!INCLUDE[d365fin](includes/d365fin_md.md)] inserta el menor precio y el mayor descuento de línea en la DL.

Si no se puede calcular ningún precio especial para el producto de la línea, se inserta el último coste directo o el precio unitario de la ficha de producto.

## <a name="see-also"></a>Consulte también
[Configurar compras](purchasing-setup-purchasing.md)  
[Compras](purchasing-manage-purchasing.md)  
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

