---
title: Tipos de facturas SII en los documentos de compra y venta
description: Descubra cómo Business Central es compatible con SII y el resultado de los diversos tipos que se utilizan para las facturas y los abonos en la versión española.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.search.form: 10751, 10752, 10753, 10770, 10771
ms.date: 05/12/2022
ms.author: edupont
ms.openlocfilehash: 5d4e7a692b746395fc57a2242ff23c6c363e9215
ms.sourcegitcommit: bc645e7ecb1940a85b2c433aa894d3494c9b10df
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 05/12/2022
ms.locfileid: "8743637"
---
# <a name="sii---invoice-and-credit-memo-types-in-sales-and-purchase-documents"></a>SII - Tipos de factura y abonos en documentos de compra y venta

[!INCLUDE[prod_short](../../includes/prod_short.md)] admite los requisitos del SII españoles para la declaración del IVA (suministro de información inmediato).  

Para obtener información sobre cómo configurar [!INCLUDE [prod_short](../../includes/prod_short.md)] para SII, consulte [Configurar el SII para la declaración del IVA en la versión en español](sii-setup.md).  

Las siguientes secciones muestran el resultado de los diversos tipos que se utilizan para las facturas y los abonos y cómo se implementan en la versión española de [!INCLUDE[prod_short](../../includes/prod_short.md)].

## <a name="sales-invoices"></a>Facturas venta

|Tipo|Descripción|Implementación|
|--|--|--|
|F1|Facturar|Factura normal|
|F2|Factura simplificada (tique)|Implementado para F1, exceptuando que un bloque no existente se llama `Contraparte` y otros nodos adicionales se llaman `ImporteTotal` y `Macrodato`.|
|F3|Factura emitida para reemplazar facturas simplificadas emitidas y archivadas|Igual que la factura normal.|
|F4|Entrada de resumen de factura|Posible, pero el archivo XML es el mismo que para F1 porque [!INCLUDE[prod_short](../../includes/prod_short.md)] no admite facturas de resumen. <br /><br />Los envíos darán como resultado un error conocido: Falta el elemento `NumSerieFacturaEmisorResumenFin`.|
|R1|Factura corregida (error basado en los artículos 80.1, 80.2 y 80.6 LIVA)|No compatible. Se utiliza solo para abonos.|
|R2|Factura corregida (artículo 80.3)|No compatible. Se utiliza solo para abonos|
|R3|Factura corregida (artículo 80.4)|No compatible. Se utiliza solo para abonos|
|R4|Factura corregida (otro)|No compatible. Se utiliza solo para abonos|
|R5|Factura corregida en facturas simplificadas|No compatible. Se utiliza solo para abonos|

## <a name="sales-credit-memos"></a>Abonos de venta

|Tipo|Description|Implementación|
|--|--|--|
|F1|Facturar|La misma estructura que una factura de venta, tipo F1, pero con valores negativos.|
|F2|Factura simplificada (tique)|La misma estructura que una factura de venta, tipo F2, pero con valores negativos.|
|F3|Factura emitida para reemplazar facturas simplificadas emitidas y archivadas|La misma estructura que una factura de venta, tipo F3, pero con valores negativos.|
|F4|Entrada de resumen de factura|No compatible.|
|R1|Factura corregida (error basado en los artículos 80.1, 80.2 y 80.6 LIVA)|Abono normal|
|R2|Factura corregida (artículo 80.3)|Igual que un abono normal|
|R3|Factura corregida (artículo 80.4)|Igual que un abono normal|
|R4|Factura corregida (otro)|Igual que un abono normal|
|R5|Factura corregida en facturas simplificadas|Igual que un abono normal, excepto que el bloqueo se llama `Contraparte`.|

## <a name="purchase-invoices"></a>Facturas compra

|Tipo|Descripción|Implementación|
|--|--|--|
|F1|Facturar|Factura normal|
|F2|Factura simplificada (tique)|Implementado para F1, exceptuando que un bloque no existente se llama `Contraparte` y otros nodos adicionales se llaman `ImporteTotal` y `Macrodato`.|
|F3|Factura emitida para reemplazar facturas simplificadas emitidas y archivadas|Igual que la factura normal|
|F4|Entrada de resumen de factura|Posible, pero el archivo XML es el mismo que para F1 porque [!INCLUDE[prod_short](../../includes/prod_short.md)] no admite facturas de resumen. <br /><br />Los envíos darán como resultado un error conocido: Falta el elemento `NumSerieFacturaEmisorResumenFin`.|
|F5|Importaciones (DUA)|Igual que la factura normal|
|F6|Material contable de soporte|Igual que la factura normal|
|R1|Factura corregida (error basado en los artículos 80.1, 80.2 y 80.6 LIVA)|No compatible. Se utiliza solo para abonos|
|R2|Factura corregida (artículo 80.3)|No compatible. Se utiliza solo para abonos|
|R3|Factura corregida (artículo 80.4)|No compatible. Se utiliza solo para abonos|
|R4|Factura corregida (otro)|No compatible. Se utiliza solo para abonos|
|R5|Factura corregida en facturas simplificadas|No compatible. Se utiliza solo para abonos|

## <a name="purchase-credit-memos"></a>Abonos de compra

|Tipo|Description|Implementación|
|--|--|--|
|F1|Facturar|La misma estructura que una factura de compra, tipo F1, pero con valores negativos|
|F2|Factura simplificada (tique)|La misma estructura que una factura de compra, tipo F1, pero con valores negativos|
|F3|Factura emitida para reemplazar facturas simplificadas emitidas y archivadas|No posible|
|F4|Entrada de resumen de factura|No posible|
|F5|Importaciones (DUA)|No posible|
|F6|Material contable de soporte|No posible|
|R1|Factura corregida (error basado en los artículos 80.1, 80.2 y 80.6 LIVA)|Abono normal|
|R2|Factura corregida (artículo 80.3)|Igual que un abono normal|
|R3|Factura corregida (artículo 80.4)|Igual que un abono normal|
|R4|Factura corregida (otro)|Igual que un abono normal|
|R5|Factura corregida en facturas simplificadas|Igual que un abono normal, excepto que el bloqueo se llama `Contraparte`|

## <a name="see-also"></a>Consulte también

[Configurar SII para informes de IVA en la versión en español](sii-setup.md)  
[Funcionalidad local para España](spain-local-functionality.md)  
<!--[Setup and user guide for electronic VAT information under SII in the Spanish version of Dynamics NAV](https://aka.ms/SIISetup)  -->


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
