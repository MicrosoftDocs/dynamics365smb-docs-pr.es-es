---
title: Configurar formas de pago | Documentos de Microsoft
description: Las formas de pago, por ejemplo, cheque, transferencia bancaria, efectivo o PayPal, se usan para definir cómo se pagarán las facturas de venta y de compra.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: check, bank transfer, cash, PayPal
ms.date: 04/01/2019
ms.author: bholtorf
ms.openlocfilehash: c9eace037f6a30fafdd5bc2a3af0af83da73b3f5
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 03/31/2019
ms.locfileid: "926348"
---
# <a name="defining-payment-methods"></a>Definir las formas de pago
Las formas de pago definen la forma en que prefiere que los clientes le paguen y cómo desea pagar a sus proveedores. El método puede variar para cada cliente o proveedor. Ejemplos de formas de pago habituales son **banco**, **efectivo**, **cheque** o **cuenta**. 

Puede asignar una forma de pago a clientes y proveedores para que siempre se utilice la misma forma en los documentos de compras y ventas que cree para ellos. Si es necesario, puede cambiar la forma en el documento de venta o de compra. Por ejemplo, si desea pagar una determinada factura de compra en efectivo en lugar de hacerlo en cheque. Esto no cambia la forma de pago predeterminada asignada al proveedor.

Se usan mismas formas de pago para documentos de venta y compra. Por ejemplo, se utiliza una forma de pago en _efectivo_ cuando crea pagos y cuando los recibe. [!INCLUDE[d365fin](includes/d365fin_md.md)] sabe que cuando está creando una factura de ventas espera recibir el pago y lo contrario para las facturas de compra. 

Sin embargo, los abonos para devoluciones son excepciones porque el dinero fluye en direcciones opuestas, de usted a su cliente y de su proveedor a usted. Por lo tanto, no se asigna una forma de pago predeterminada a los abonos. Sin embargo, existe una solución alternativa si se ha especificado condiciones de pago para el cliente o el proveedor. Aunque el campo **Calc. dto. P.P. en abonos** no se ha diseñado para este fin, si marca la casilla de la página **Condiciones de pago**, se añadirá una forma de pago predeterminada al crear un abono.

## <a name="to-set-up-a-payment-method"></a>Para configurar una forma de pago
[!INCLUDE[d365fin](includes/d365fin_md.md)] proporciona algunas formas de pago que las empresas utilizan con frecuencia. Sin embargo, puede agregar tantas como necesite.

1. Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Métodos pago** y luego elija el enlace relacionado.
2. Rellene los campos según sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-assign-a-payment-method-to-a-customer-or-vendor"></a>Para asignar una forma de pago a un cliente o proveedor
1. Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Cliente** o **Proveedor** y luego elija el enlace relacionado.
2. En el campo **Forma pago**, seleccione la forma que se usará de forma predeterminada para el cliente o proveedor.

## <a name="see-also"></a>Consulte también
[Finanzas](finance.md)  
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
