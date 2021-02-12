---
author: edupont04
ms.service: dynamics365-business-central
ms.topic: include
ms.date: 01/20/2021
ms.author: edupont
ms.openlocfilehash: 718845561c1a18701d20b93ebdc8339308ce7ac8
ms.sourcegitcommit: adf1a87a677b8197c68bb28c44b7a58250d6fc51
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 01/21/2021
ms.locfileid: "5035795"
---
Una vez que se hayan especificado todos los productos en las líneas de pedido de venta, podrá calcular el descuento en factura para todo el documento de venta si hace clic en la acción **Calcular dto. en la factura**.

Si se selecciona el campo **Calc. dto. factura** en la ventana **Config. ventas y cobros**, se calcula el descuento de la factura automáticamente cuando realiza una de las siguientes operaciones en un documento de venta:

* Ver estadísticas
* Ver un test
* Imprimir
* Envíos postales

El descuento se distribuirá proporcionalmente a todas las líneas del documento de venta para productos en los que el campo **Permitir dto. factura** de la línea de pedido de venta contiene **Sí**. Este es el valor predeterminado para los productos.

Las condiciones de descuentao de factura se definen en la página **Descuentos de factura de cliente** para calcular el descuento en factura. El código de divisa del documento de venta se usa para buscar las condiciones de descuento en factura en la divisa correspondiente.

Si no se han definido descuentos facturas para divisas extranjeras, el programa utiliza las condiciones de descuento factura en DL que aparecen en la página **Dto. factura cliente** con importes en la divisa local y el tipo de cambio en la fecha de registro del documento de venta para calcular el descuento en factura en divisa extranjera.
