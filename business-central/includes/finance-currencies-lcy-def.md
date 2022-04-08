---
author: edupont04
ms.topic: include
ms.date: 03/15/2022
ms.author: edupont
ms.openlocfilehash: c391e7d6492a722de10801212ccd04a532f8a971
ms.sourcegitcommit: 521735f8e27d8bff2d2dfbe94d240c09dcdaec29
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2022
ms.locfileid: "8419618"
---
Las empresas trabajan en más países o regiones, por lo que es vital que puedan intercambiar y generar información financiera en más de una divisa. La divisa local (DL) se define en la página **Configuración de contabilidad** como se describe en el artículo [Descripción de contabilidad y plan de cuentas](../finance-general-ledger.md). Una vez que se ha definido la divisa local (DL), se representará como una divisa en blanco, por lo que cuando el campo **Divisa** esté vacío, significa que la divisa es DL.  

A continuación, debe configurar códigos de divisa para cada divisa que utilice si compra o vende en divisas diferentes a la suya local (DL). También se pueden crear cuentas bancarias utilizando divisas. Es posible registrar transacciones de contabilidad en diferentes divisas, sin embargo, la transacción del contabilidad siempre se contabilizará en la divisa local (DL).

[!INCLUDE [finance-currencies-lcy](finance-currencies-lcy-note.md)]

La contabilidad se configura con la divisa local (DL), pero también se puede configurar para usarla en otra divisa a la que se asigna un tipo de cambio. Mediante la designación de una segunda divisa como la denominada divisa de informes adicional, [!INCLUDE[prod_short](prod_short.md)] registrará automáticamente los importes tanto en la divisa local como en la divisa adicional en todos los movimientos de contabilidad y en otros movimientos, por ejemplo los del IVA. Para obtener más información, consulte [Configurar una divisa de informes adicional](../finance-how-setup-additional-currencies.md). La moneda de presentación de informes adicional se utiliza con mayor frecuencia para facilitar la presentación de informes financieros a los propietarios que residen en países o regiones que utilizan divisas diferentes a la divisa local (DL).  

> [!IMPORTANT]
> Si desea utilizar una divisa de informes adicional para informes financieros, asegúrese de comprender las limitaciones. Para obtener más información, consulte [Configurar una divisa de informes adicional](../finance-how-setup-additional-currencies.md).

> [!NOTE]  
> Cuando contabiliza en el L/M usando un código de moneda, como registrar un gasto en un diario general usando un código de moneda, la transacción se convierte a LCY usando la tasa de cambio de moneda para la fecha de registro. La entrada del L/M no contendrá información de qué moneda se usó, solo su valor en LCY. Si desea realizar un seguimiento de la moneda original, por ejemplo, para una factura, debe usar los documentos de compra y venta, así como las cuentas bancarias que almacenan la información del código de moneda para las entradas.
