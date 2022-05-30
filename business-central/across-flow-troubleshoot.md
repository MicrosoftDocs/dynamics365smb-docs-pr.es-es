---
title: Solucionar problemas de sus flujos de trabajo automatizados
description: Aprenda a solucionar problemas de conexión entre Business Central y Power Automate cuando crea un flujo de trabajo automatizado.
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 05/12/2022
ms.author: edupont
author: jswymer
ms.openlocfilehash: b8fff95ced93e7ee2a3112969f45525532b19445
ms.sourcegitcommit: e86f0bd15604c2fb327e3182929c44a4172790c7
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 05/20/2022
ms.locfileid: "8786201"
---
# <a name="troubleshoot-your-prod_short-automated-workflows"></a>Solucionar problemas de sus [!INCLUDE[prod_short](includes/prod_short.md)] flujos de trabajo automatizados

Cuando conecta [!INCLUDE [prod_short](includes/prod_short.md)] con Power Automate para crear flujos de trabajo automatizados, es posible que encuentre mensajes de error. Este artículo proporciona soluciones sugeridas para problemas que se repiten con frecuencia.

## <a name="flow-doesnt-run-on-all-records-created-or-changed"></a>El flujo no se ejecuta en todos los registros creados o modificados

### <a name="problem"></a>Problema

Si un evento crea o cambia muchos registros, el flujo no se ejecuta en algunos o en todos los registros.

### <a name="possible-cause"></a>Causa posible

Actualmente, hay un límite en la cantidad de registros que puede procesar un flujo. Si se crean o modifican más de 100 registros en 30 segundos, el flujo no se activará.

> [!NOTE]
> Para los desarrolladores, la activación del flujo se realiza a través de notificaciones de un webhook y esta limitación se debe a la forma en la que el conector de Business Central gestiona las notificaciones de `collection` Para obtener más información, consulte [Trabajando con webhooks en Dynamics 365 Business Central](/dynamics365/business-central/dev-itpro/api-reference/v2.0/dynamics-subscriptions#notes-for-power-automate-flows) en la ayuda para desarrolladores y administradores.

## <a name="entity-set-not-found-error"></a>Error "Conjunto de entidades no encontrado"

### <a name="problem"></a>Problema

Cuando crea un nuevo flujo de Power Automate usando un desencadenador de aprobación de [!INCLUDE[prod_short](includes/prod_short.md)], como *Cuando se solicita la aprobación de un documento de compra*, puede recibir un mensaje de error similar a:

`Entity set not found: \<name\>`

El marcador, `\<name\>`, es el nombre del servicio del servicio web que falta, como *workflowWebhookSubscriptions* o *workflowPurchaseDocumentLines*.

### <a name="possible-cause"></a>Causa posible

Usar Power Automate con sus solicitudes requiere que determinadas páginas y objetos de codeunit se publiquen como servicios web. De forma predeterminada, la mayoría de los objetos necesarios se publican como servicios web para usted. Pero en algunos casos, es posible que su ambiente se haya personalizado para que estos objetos ya no se publiquen.

### <a name="fix"></a>Corregir

Vaya a la página **Servicios web** y asegúrese de que los siguientes objetos se publiquen como servicios web. Debe haber una entrada en la lista para cada objeto, con la casilla de verificación **Publicado** seleccionada.  

|Tipo de objeto|Id. de objeto|Nombre de objeto|Nombre del servicio|
|-----------|---------|-----------|------------|
|Codeunit|  1544    |WorkflowWebhookSubscription|WorkflowActionResponse|
|Página|  6408|   workflowCustomers|  workflowCustomers|
|Página   |6406   |workflowGenJournalBatches| workflowGenJournalBatches|
|Página   |6407   |workflowGenJournalLines|workflowGenJournalLines|
|Página   |6409   |workflowItems| workflowItems|
|Página   |6405   |Entidad de línea de documento de compra|workflowPurchaseDocumentLines|
|Página|  6404    |workflowPurchaseDocuments| workflowPurchaseDocuments|
|Página|  6403    |Entidad de línea de documento de venta |workflowSalesDocumentLines|
|Página|  6402|   workflowSalesDocuments| workflowSalesDocuments|
|Página|  6410    |workflowVendors|   workflowVendors|
|Página|  831 |workflowWebhookSubscriptions|  workflowWebhookSubscriptions|

> [!NOTE]
> El valor **Nombre del Servicio** debe ser exactamente como se muestra en la tabla. No cambie ni traduzca el nombre del servicio.

Para obtener más información sobre la publicación de servicios web, consulte [Publicar un servicio web](across-how-publish-web-service.md).

## <a name="see-also"></a>Consulte también

[Usar [!INCLUDE[prod_short](includes/prod_short.md)] en un flujo de trabajo automatizado](across-how-use-financials-data-source-flow.md)  
[Flujo de trabajo](across-workflow.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]