---
title: Registrar precios y descuentos de compra especiales | Documentos de Microsoft
description: 'Procedimiento: Registrar precios y descuentos de compra'
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: special price, alternate price, pricing
ms.date: 03/29/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 67625231d62a72bb0a62ab362bce92aa16b8956e
ms.contentlocale: es-es
ms.lasthandoff: 05/04/2017


---
# <a name="how-to-record-special-purchase-prices-and-discounts"></a>Registrar precios y descuentos de compra especiales
Los diferentes acuerdos de precio y descuentos que se aplican cuando compra a distintos proveedores se deben definir para que las reglas y valores acordados se apliquen a los documentos de compra que se crean para los proveedores.

Cuando haya registrado precios especiales y los descuentos de línea para ventas y compras, [!INCLUDE[d365fin](includes/d365fin_md.md)] garantiza que el beneficio en operaciones comerciales de producto siempre son óptimos calculando automáticamente el mejor precio en los documentos de ventas y compras, y en líneas del diario de proyectos y recursos. Para obtener más información, vea [Avanzado: Cálculo del mejor precio](advanced-best-price-calculation.md).

Respecto a los precios, puede tener una precio especial de compra insertado en las líneas de compra si existe una cierta combinación de proveedor, producto, cantidad mínima, unidad de medida o fecha de inicio o de fin.

Respecto a los descuentos, puede configurar y usar dos tipos de descuentos de compra:

| Tipo de descuento | Descripción |
| --- | --- |
| **Descuento línea compra** |Un importe de descuento que está insertado en las líneas de compra si existe una cierta combinación de proveedor, producto, cantidad mínima, unidad de medida o fecha de inicio o de fin. Funciona igual que para los precios de compra. |
| **Descuento en factura** |Un porcentaje de descuento que se resta del total del documento si el importe de todas las líneas de un documento de compra supera cierto límite. |

Puesto que los descuentos de línea y los precios de compra se basan en una combinación de producto y proveedor, también se puede introducir esta combinación desde la ficha de producto en la que se definen las reglas y los valores. Para obtener más información, vea [Registrar nuevos productos](inventory-how-register-new-items.md).

## <a name="to-set-up-a-special-purchase-price-for-a-vendor"></a>Para configurar un precio de compra especial para un proveedor
1. En la esquina superior derecha, seleccione el icono **Buscar página o informe** ![Buscar página o informe](media/ui-search/search_small.png "Icono Buscar página o informe"), especifique **Proveedores** y elija el vínculo relacionado.
2. Abra la ficha de proveedor correspondiente y, a continuación, elija la acción **Precios**.

    El campo **Tipo de compras** se rellena previamente con el campo **Proveedor** y el campo **Código de compre** se rellena con el número del proveedor.
3. Rellene los campos de la línea como sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Rellene una línea para cada combinación por la que el proveedor le garantiza un descuento de compra.

## <a name="to-set-up-a-line-discount-for-a-vendor"></a>Para configurar un descuento de línea para un proveedor
1. En la esquina superior derecha, seleccione el icono **Buscar página o informe** ![Buscar página o informe](media/ui-search/search_small.png "Icono Buscar página o informe"), especifique **Proveedores** y elija el vínculo relacionado.
2. Abra la ficha de proveedor correspondiente y, a continuación, elija la acción **Dto. línea**.

    El campo **Tipo de compras** se rellena previamente con el campo **Proveedor** y el campo **Código de compre** se rellena con el número del proveedor.
3. Rellene los campos de la línea como sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Rellene una línea para cada combinación por la que el proveedor le garantiza un descuento de compra.

## <a name="to-set-up-an-invoice-discount-for-a-vendor"></a>Para configurar términos de descuento en factura para un proveedor:
Una vez su proveedor le haya informado de que descuentos en factura garantizan, introduzca el código de descuento en las fichas de cliente y especifique los términos de cada código.

1. En la esquina superior derecha, seleccione el icono **Buscar página o informe** ![Buscar página o informe](media/ui-search/search_small.png "Icono Buscar página o informe"), especifique **Proveedores** y elija el vínculo relacionado.
2. Abra la ficha de un proveedor que pueda obtener descuentos en factura.
3. En el campo **Código descuento factura**, seleccione un código para los términos relevantes de la factura con descuentos que usará para calcular los descuentos en facturas para el proveedor.

    **Nota**: Los códigos de descuento en factura se representan por las fichas existentes del proveedor. Lo que permite asignar rápidamente las condiciones de descuento en factura a proveedores realizando el picking del nombre de otros proveedores con los mismos términos.

    Configure de nuevo los términos de descuento en factura para compras.
4. En la ventana **Ficha de proveedor**, seleccione la acción **Descuento factura**. Aparecerá la ventana **Dtos. factura proveedor**.
5. En el campo **Código divisa**, introduzca el código de una divisa que se aplique a los términos de descuento en factura en la línea. Deje el campo en blanco para establecer condiciones de descuento de factura en USD.
6. En el campo **Importe mínimo**, escriba el importe mínimo que deba tener una factura para optar al descuento.
7. En el campo **% descuento**, introduzca el descuento en la factura como un porcentaje del importe de la factura.
8. Repita los pasos 5 a 7 para cada divisa para la que el proveedor va a recibir un descuento diferente de factura.

El descuento en factura está configurado y asignado el proveedor en cuestión. En el momento que selecciona el código de proveedor en el campo **Código de descuento de factura** en las fichas de proveedores, se asigna el mismo descuento en factura a ese proveedor.

## <a name="see-also"></a>Consulte también
[Avanzado: Cálculo del mejor precio](advanced-best-price-calculation.md)  
[Configurar compras](purchasing-setup-purchasing.md)  
[Compras](purchasing-manage-purchasing.md)  
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)](ui-work-product.md)

