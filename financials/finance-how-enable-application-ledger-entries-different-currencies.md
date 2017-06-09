---
title: "Permitir la liquidación de movimientos de cliente en distintas divisas | Documentos de Microsoft"
description: "Obtenga información sobre cómo puede liquidar movimientos contables en distintas divisas."
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: multiple currencies, payment, reconcile
ms.date: 03/24/2017
ms.author: edupont
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 4f904d1600d56a83238581915726a7b7fd6cca38
ms.contentlocale: es-es
ms.lasthandoff: 05/04/2017


---
# <a name="how-to-enable-application-of-ledger-entries-in-different-currencies"></a>Procedimiento: Permitir la liquidación de movimientos de cliente en distintas divisas
Si se realiza una compra a un proveedor en una divisa y se emite el pago en otra divisa, es posible liquidar la compra con el pago.

De igual modo, si vende a un cliente en una divisa y cobra en otra, puede liquidar el pago con la factura de venta.

El procedimiento siguiente describe cómo configurarlo para movimientos de proveedor en la ventana **Configuración de compras y pagos**. La configuración es similar para los movimientos de cliente en la ventana **Configuración de ventas y cobros**.

**Nota**: Esta funcionalidad que requiere que la experiencia esté definida en **Conjunto de aplicaciones**. Para obtener más información, consulte [Personalizar la experiencia de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-experiences.md).

## <a name="to-enable-application-of-vendor-ledger-entries-in-different-currencies"></a>Para permitir la liquidación de movimientos de proveedor en divisas distintas
1. En la esquina superior derecha, seleccione el icono **Buscar página o informe** ![Buscar página o informe](media/ui-search/search_small.png "Icono Buscar página o informe"), especifique **Configuración compras y pagos** y elija el vínculo relacionado.
2. En el campo **Liquidación entre divisas**, seleccione una de las siguientes opciones.

| Opción | Descripción |
| --- | --- |
| Ninguno |No se permite la liquidación entre divisas. |
| UME |Se permite la liquidación entre divisas de la UME. |
| Todo |Se permite la liquidación entre todas las divisas. |

## <a name="see-also"></a>Consulte también
[Administrar pagos](payables-manage-payables.md)  
[Administrar cobros](receivables-manage-receivables.md)  
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)](ui-work-product.md)

