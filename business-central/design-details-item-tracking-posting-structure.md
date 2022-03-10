---
title: 'Detalles de diseño: Estructura de registro de seguimiento de productos'
description: Aprender a usar movimientos de productos como soporte principal de los números de seguimiento de producto en la Estructura de registro de seguimiento de productos.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: design, item tracking, posting, inventory
ms.date: 06/15/2021
ms.author: edupont
ms.openlocfilehash: b568e62a71b907e8d2f9cbc8eba43773be655b44
ms.sourcegitcommit: ef80c461713fff1a75998766e7a4ed3a7c6121d0
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 02/15/2022
ms.locfileid: "8136327"
---
# <a name="design-details-item-tracking-posting-structure"></a>Detalles de diseño: Estructura de registro de seguimiento de productos
Para establecer la correspondencia con la funcionalidad de valoración de existencias y obtener una solución más simple y robusta, se usan los movimientos de producto como el soporte principal de los números de seguimiento de producto.  
  
Los números de seguimiento de producto en las entidades de la red de pedidos y las entidades de red que no realizan pedidos se especifican en la tabla **Mov. reserva** (T337). Los números de seguimiento de producto que están relacionados con la información histórica se recuperan directamente de los movimientos de producto relacionados con la transacción en cuestión. Esto significa que los movimientos de producto reflejan la especificación de seguimiento de producto de la línea de pedido registrada.  
  
La página **Líns. seguim. prod.** recupera la información de T337 y de los movimientos de producto, y la muestra a través de la tabla temporal **Especificación seguimiento** (T336). T336 también contiene los datos temporales de la página **Líns. seguim. prod.** para las cantidades de seguimiento de producto que se deben facturar.  
  
## <a name="one-to-many-relation"></a>Relación de uno a varios  
La tabla **Relación mov. producto**, que se usa para vincular una línea de documento registrado con sus movimientos de producto relacionados, consta de dos partes principales:  
  
* Un puntero a la línea de documento registrado, el **Nº línea pedido**. .  
* Un número de entrada que apunta a un movimiento de producto, el campo **Nº mov. producto**.  
  
La funcionalidad del campo **Nº mov.** existente, que relaciona un movimiento de producto con una línea de documento registrado, controla la relación uno a uno habitual cuando no hay números de seguimiento de producto en la línea de documento registrada. Si hay números de seguimiento de productos, el campo **Nº mov.** se deja en blanco, y la relación de uno a muchos se gestiona a través de la tabla **Relación mov. producto**. Si la línea de documento registrada lleva números de seguimiento de productos pero hace referencia a un único movimiento de producto, el campo **Nº mov.** administrará la relación, y no se creará ningún registro en la tabla **Relación mov. producto**.  
  
## <a name="codeunits-80-and-90"></a>Codeunits 80 y 90  
Para dividir los movimientos de producto durante el registro, el código de codeunit 80 y codeunit 90, se encuentra entre bucles que recorren las variables de registro temporales globales. Este código llama a la codeunit 22 con una línea de diario de productos. Estas variables se inicializan cuando hay números de seguimiento de producto para la línea de documento. Para simplificar el código, siempre se usa esta estructura de bucle. Si no hay números de seguimiento para la línea del documento, se insertará un único registro y el bucle se ejecutará solo una vez.  
  
## <a name="posting-the-item-journal"></a>Registro del diario de productos  
Los números de seguimiento de producto se transfieren mediante los movimientos de reserva relacionados con el movimiento de producto y el recorrido en bucle por los números de seguimiento de producto se realiza en la codeunit 22. Este concepto funciona del mismo modo cuando una línea del diario de productos se usa indirectamente para registrar un pedido de compra o de venta que cuando una línea del diario de productos se usa directamente. Cuando el diario de producto se usa directamente, el campo **IdLínea origen** indica la línea del diario de producto.  
  
## <a name="code-unit-22"></a>Codeunit 22  
Las codeunits 80 y 90 examinan la llamada de la codeunit 22 durante el registro de factura de los números de seguimiento de productos y durante la facturación de envíos o recepciones existentes.  
  
Durante el registro de la cantidad de números de seguimiento de productos, la codeunit 22 recupera los números de seguimiento de productos a partir de las entradas en T337 relativas al registro. Estos movimientos se colocan directamente en la línea de diario de productos.  
  
La codeunit 22 examina los números de seguimiento de producto y divide el registro en los movimientos correspondientes con ese número de seguimiento. Se devuelve a T337 información sobre qué movimientos de producto se crean con un registro temporal T336, al cual llama un procedimiento en la codeunit 22. Este procedimiento se desencadena cuando la codeunit 22 ha terminado su ejecución porque en ese momento el objeto con codeunit 22 contiene información. Cuando se recupera el registro T336 temporal, las codeunits 80 y 90 crean registros en la tabla **Relación mov. producto** para vincular los movimientos de producto con la línea de envío o recepción creada. Las codeunits 80 o 90 a continuación convierten los registros temporales T336 en registros reales T336 relacionados con la línea en cuestión. No obstante, esta conversión solo tienen lugar si la línea de documento registrada no se elimina, porque se registra solo parcialmente.  
  
## <a name="see-also"></a>Consulte también  
[Detalles de diseño: Seguimiento de productos](design-details-item-tracking.md)   
[Detalles de diseño: Diseño de seguimiento de productos](design-details-item-tracking-design.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]