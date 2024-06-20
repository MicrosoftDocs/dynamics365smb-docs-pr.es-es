---
author: brentholtorf
ms.topic: include
ms.date: 03/04/2024
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
Si su empresa opera en más de un país o región, probablemente sea importante que pueda hacer negocios en más de una moneda. Usted define su moneda local (LCY) en la página **Configuración del libro mayor**. Posteriormente, su moneda local se representará como moneda en blanco en documentos y transacciones. Cuando el campo **Moneda** está en blanco, la moneda es LCY.

El siguiente vídeo explica cómo configurar su moneda local.

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RW1iM1n]

A continuación, debe configurar códigos de divisa para cada divisa que utilice si compra o vende en divisas diferentes a la suya local (DL). También se pueden crear cuentas bancarias utilizando divisas. Es posible registrar transacciones de contabilidad en diferentes divisas, sin embargo, la transacción del contabilidad siempre se contabilizará en la divisa local (DL).

[!INCLUDE [finance-currencies-lcy](finance-currencies-lcy-note.md)]

La contabilidad se configura con la divisa local (DL), pero también se puede configurar para usarla en otra divisa a la que se asigna un tipo de cambio. Mediante la designación de una segunda divisa como una divisa de informes adicional, [!INCLUDE[prod_short](prod_short.md)] registra automáticamente los importes tanto en la divisa local como en la divisa de notificación adicional en los movimientos de contabilidad y en otros movimientos, por ejemplo los del IVA. Para obtener más información, consulte [Configurar una divisa de informes adicional](../finance-how-setup-additional-currencies.md). La moneda de presentación de informes adicional se utiliza con mayor frecuencia para facilitar la presentación de informes financieros a los propietarios que residen en países o regiones que utilizan divisas diferentes a la divisa local (DL).  

> [!IMPORTANT]
> Si desea utilizar una divisa de informes adicional para informes financieros, asegúrese de comprender las limitaciones. Para obtener más información, consulte [Configurar una divisa de informes adicional](../finance-how-setup-additional-currencies.md).

> [!NOTE]  
> Cuando contabiliza en el libro mayor utilizando una moneda extranjera, [!INCLUDE [prod_short](prod_short.md)] convierte la transacción a LCY utilizando el tipo de cambio de moneda de la fecha de contabilización. La entrada del L/M no contendrá información sobre qué moneda se usó, solo su valor en LCY. Para realizar un seguimiento de la moneda original, use los documentos de compra y venta, y las cuentas bancarias que almacenan la información de moneda para las entradas.
