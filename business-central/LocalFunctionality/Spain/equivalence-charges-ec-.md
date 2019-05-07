---
title: Recargo de equivalencia (RE)
description: Un recargo de equivalencia (RE) es un impuesto que se utiliza en ventas minoristas y en actividades que no siguen las reglas del IVA. Según las reglas RE, las empresas deben pagar un recargo a sus proveedores al adquirir bienes además del IVA normal.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: 77e1bc46c1ad11fb15e87646f4674299e3e07a72
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 03/31/2019
ms.locfileid: "919794"
---
# <a name="equivalence-charges-ec"></a>Recargo de equivalencia (RE)
Un recargo de equivalencia (RE) es un impuesto que se utiliza en ventas minoristas y en actividades que no siguen las reglas del IVA. Según las reglas RE, las empresas deben pagar un recargo a sus proveedores al adquirir bienes además del IVA normal. Sin embargo, al vender bienes, solo puede cargarse el IVA. Algunos grupos de registro general deben tener un porcentaje RE, además del porcentaje de IVA. Esta información se efectúa por separado, pero para minimizar los cambios, ambos impuestos se combinan.  

El campo **% RE** es un campo independiente en las tablas **Lín. compra**, **Lín. venta**, **Archivo lín. venta** y **Archivo lín. compra** . No obstante, en las líneas de ventas y compras, se combinan ambos impuestos y el valor se muestra en el campo **% IVA**. Se utiliza el campo **% IVA + RE** cuando se combinan las opciones de configuración. En el momento de la publicación, el porcentaje de IVA y el porcentaje de RE se insertan en la tabla de **Movs. IVA**. Esto permite imprimir el informe **Libro facturas emitidas** y el informe **Libro facturas recibidas**.  

## <a name="see-also"></a>Consulte también  
[Funcionalidad local para España](spain-local-functionality.md)
