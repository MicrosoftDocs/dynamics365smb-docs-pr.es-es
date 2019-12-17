---
title: Configurar redondeo de facturas | Documentos de Microsoft
description: Puede redondear los importes de las facturas en el momento en que éstas se crean. Además, las normativas o costumbres locales pueden requerir que el redondeo de las facturas se realice de un modo específico, por ejemplo, en una cantidad divisible por 0,05.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: bholtorf
ms.openlocfilehash: bb114e6ea550ca5cc453c8319e72da5b11cec6e8
ms.sourcegitcommit: cfc92eefa8b06fb426482f54e393f0e6e222f712
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 12/03/2019
ms.locfileid: "2882475"
---
# <a name="set-up-invoice-rounding"></a>Configurar redondeo de factura
Si necesita redondear importes de facturas cuando se crean, puede utilizar la función de redondeo automático. Cuando se redondea una factura, se añade una línea adicional en el importe redondeado y se registra con las demás líneas de la factura.

> [!NOTE]  
>  Las normativas o costumbres locales pueden requerir que el redondeo de las facturas se realice de un modo específico, por ejemplo, en una cantidad divisible por 0,05.  

Para utilizar el redondeo de factura automático, debe:  

* Especificar las cuentas contables donde se van a registrar las diferencias de redondeo.  
* Configurar reglas de redondeo de la factura en la divisa local y en la divisa extranjera.  
* Activar la función.  

> [!NOTE]  
>  Además de las funciones de redondeo de facturas, puede redondear los importes de las facturas mediante la función de redondeo de precio-producto y la función de redondeo de importe.  

## <a name="set-up-general-ledger-accounts-for-invoice-rounding-differences"></a>Configurar cuentas para diferencias de redondeo de facturas
Para utilizar la utilidad de redondeo de factura automático, debe configurar la cuenta o las cuentas en las que se registrarán las diferencias. Antes de poder hacerlo, deberá configurar grupos de registro de IVA de producto. Para obtener más información, consulte [Configurar IVA](finance-setup-vat.md).  

### <a name="to-set-up-general-ledger-accounts-for-invoice-rounding-differences"></a>Para configurar cuentas para diferencias de redondeo de facturas  
1. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Plan de cuentas** y luego elija el enlace relacionado.  
2. En la página **Plan de cuentas**, configure la cuenta y denomínela **Redondeo factura** o algo parecido. [!INCLUDE[d365fin](includes/d365fin_md.md)] utilizará el nombre de la cuenta como texto en las facturas que se redondean.  
3. Dependiendo de si utiliza el IVA o impuesto sobre las ventas, en los campos **Grupo registro impuesto prod.** o **Grupo reg. IVA producto**, seleccione un grupo de registro para los importes redondeados. Puede que desee configurar un nuevo código de grupo para usarlo para el redondeo de factura.
4. Deje en blanco los campos **Tipo IVA** y **Grupo registro impuesto neg.** o **Grupo registro IVA neg**. <!-- Why do we say to leave these blank, when there are a lot of other fields we also leave blank but don't mention? -->  

Ya puede asignar la cuenta de redondeo de factura a grupos de registro en la página **Grupo contable proveedor**.  <!-- Why only the vendor posting groups? -->

## <a name="set-up-rounding-for-foreign-and-local-currencies"></a>Configurar redondeo para la divisa extranjera y local
Para poder utilizar la función de redondeo de factura automático, debe configurar reglas de redondeo para las divisas extranjera y local.

### <a name="to-set-up-rounding-for-foreign-currencies"></a>Configurar redondeo para la divisa extranjera  
1. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Divisas** y luego elija el enlace relacionado.  
2. En la página **Divisas**, seleccione la divisa extranjera para abrir **Ficha divisa**, y rellene los campos **Prec. redondeo importe**, **Prec. redondeo precio-prod.**, **Precisión redondeo factura** y **Tipo redondeo factura**.

### <a name="to-set-up-rounding-for-your-local-currency"></a>Configurar redondeo para la divisa local
1. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Configuración de contabilidad** y luego elija el enlace relacionado.  
2. En la página **Configuración de contabilidad**, en la ficha desplegable **General**, rellene los campos **Precisión redondeo fact.** y **Tipo redondeo fact.**.  

## <a name="activate-the-invoice-rounding-function"></a>Activar la función de redondeo de factura  
Para asegurarse de que se redondeen automáticamente las facturas de venta y compra, debe activar la función de redondeo de factura. Active el redondeo de factura de forma independiente en las facturas de venta y en las de compra.

1. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Configuración ventas y cobros** o **Configuración compras y pagos** y luego elija el enlace relacionado.  
2. En la ficha desplegable **General**, elija la casilla de verificación **Redondeo de factura**.  

## <a name="see-also"></a>Consulte también  
[Facturar ventas](sales-how-invoice-sales.md)  
[Registrar compras](purchasing-how-record-purchases.md)
