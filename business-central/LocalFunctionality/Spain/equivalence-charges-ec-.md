---
title: 'Recargos de equivalencia (RE) [ES]'
description: Un recargo de equivalencia (RE) es un impuesto que se utiliza en ventas minoristas y en actividades que no siguen las reglas del IVA.
services: project-madeira
documentationcenter: ''
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 11/14/2023
ms.author: bholtorf
---
# <a name="equivalence-charges-ec-in-the-spanish-version"></a>Recargos de equivalencia (RE) en la versión en español
Un recargo de equivalencia (RE) es un impuesto que se utiliza en ventas minoristas y en actividades que no siguen las reglas del IVA. Según las reglas RE, las empresas deben pagar un recargo a sus proveedores al adquirir bienes además del IVA normal. Sin embargo, al vender bienes, solo puede cargarse el IVA. Algunos grupos de registro general deben tener un porcentaje RE, además del porcentaje de IVA. Esta información se efectúa por separado, pero para minimizar los cambios, ambos impuestos se combinan.  

El campo **% RE** es un campo independiente en las tablas **Lín. compra**, **Lín. venta**, **Archivo lín. venta** y **Archivo lín. compra** . No obstante, en las líneas de ventas y compras, se combinan ambos impuestos y el valor se muestra en el campo **% IVA**. Se utiliza el campo **% IVA + RE** cuando se combinan las opciones de configuración. En el momento de la publicación, el porcentaje de IVA y el porcentaje de RE se insertan en la tabla de **Movs. IVA**. Esto permite imprimir el informe **Libro facturas emitidas** y el informe **Libro facturas recibidas**.  

## <a name="see-also"></a>Consulte también
[Funcionalidad local para España](spain-local-functionality.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
