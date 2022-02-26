---
title: Conectar los datos con Power Automate | Documentos de Microsoft
description: Puede hacer que los datos de Business Central estén disponibles como un origen de datos y especificar una URL de OData de sus servicios web para generar un flujo de trabajo automatizado.
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: workflow, OData, Power App, SOAP, Entity set not found, workflowWebhookSubscriptions
ms.date: 07/27/2021
ms.author: edupont
author: jswymer
ms.openlocfilehash: fb79c3ab799c5a77ff725ce05d1469f5bec7c9f5
ms.sourcegitcommit: 769d20d299155cba30c35636d02b2ef021e4ecc1
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 07/29/2021
ms.locfileid: "6688375"
---
# <a name="using-prod_short-in-an-automated-workflow"></a>Usar [!INCLUDE[prod_short](includes/prod_short.md)] en un flujo de trabajo automatizado

Puede utilizar sus datos de [!INCLUDE[prod_short](includes/prod_short.md)] como parte de un flujo de trabajo de Microsoft Power Automate.

> [!NOTE]
> Además de Power Automate, puede utilizar la funcionalidad de flujo de trabajo en [!INCLUDE[prod_short](includes/prod_short.md)]. Tenga en cuenta que, aunque son dos sistemas de flujo de trabajo independientes, cualquier plantilla de flujo de trabajo que cree con Power Automate se agrega a la lista de flujos de trabajo en [!INCLUDE[prod_short](includes/prod_short.md)]. Para obtener más información, consulte [Flujo de trabajo](across-workflow.md).  

> [!NOTE]  
> Debe disponer de una cuenta válida con [!INCLUDE[prod_short](includes/prod_short.md)] y con Power Automate.  

## <a name="add-prod_short-as-a-data-source-in-power-automate"></a>Agregar [!INCLUDE[prod_short](includes/prod_short.md)] como origen de datos en Power Automate

1. En el explorador, vaya a [flow.microsoft.com](https://flow.microsoft.com) y, a continuación, inicie sesión.
2. Seleccione **Mis flujos** en la cinta en la parte superior de la página.
3. Hay tres formas de crear un flujo: **Iniciar desde plantilla**, **Iniciar desde cero** e **Iniciar desde un conector**. Una plantilla es un flujo predefinido que se ha creado de forma automática. Para utilizar una plantilla, selecciónela y cree una conexión para cada servicio que la plantilla usa. Con las opciones **Iniciar desde cero** e **Iniciar desde un conector** puede crear un flujo nuevo completamente desde cero.
4. Para crear desde cero, en la página **Mis flujos**, elija las opciones **Iniciar desde cero** y **Flujo automatizado**.
5. Busque el conector de **Microsoft [!INCLUDE[prod_long](includes/prod_long.md)]**.
6. Defina un nombre y elija el activador que desea usar para su flujo.
7. En la lista de disparadores disponibles, seleccione uno de los de [!INCLUDE[prod_short](includes/prod_short.md)] disponibles:  

    - *Cuando se solicite la aprobación de un proveedor*  
    - *Cuando se solicite la aprobación de una línea de diario general* 
    - *Cuando se elimine un registro*
    - *Cuando se cambie un registro*
    - *Cuando se cree un registro*
    - *Cuando se modifique un registro*
    - *Cuando se solicite la aprobación de un lote de diario general* 
    - *Cuando se solicite la aprobación de un cliente*
    - *Cuando se solicite la aprobación de un artículo*
    - *Cuando se solicite la aprobación de un documento de compra*
    - *Cuando se solicite la aprobación de un documento de ventas*

8. Power Automate le solicitará que seleccione un ambiente y una empresa en su suscriptor de [!INCLUDE[prod_short](includes/prod_short.md)], así como las condiciones de los datos que desee escuchar.

    > [!NOTE]
    > El conector de [!INCLUDE[prod_short](includes/prod_short.md)] para Power Automate admite múltiples ambientes de producción y aislados. Si no ha creado múltiples ambientes de producción o aislados, **Producción** es la única opción disponible que puede elegir.  

    Ya se ha conectado correctamente con los datos de Business Central[!INCLUDE[prod_short](includes/prod_short.md)] y está preparado para comenzar a crear su flujo.

9. Para crear desde una plantilla, seleccione la opción **Iniciar desde plantilla**.
10. Busque las plantillas de **Microsoft [!INCLUDE[prod_long](includes/prod_long.md)]**.
11. En la lista de plantillas disponibles, seleccione una de las plantillas y, a continuación, elija **Crear**.  

    - *Solicitar aprobación para pedido de venta de Microsoft [!INCLUDE[prod_long](includes/prod_long.md)]*
    - *Solicitar aprobación para oferta de venta de Microsoft [!INCLUDE[prod_long](includes/prod_long.md)]*
    - *Solicitar aprobación para factura de venta de Microsoft [!INCLUDE[prod_long](includes/prod_long.md)]*,
    - *Solicitar aprobación para abono de venta de Microsoft [!INCLUDE[prod_long](includes/prod_long.md)]*
    - *Solicitar aprobación para cliente de Microsoft [!INCLUDE[prod_long](includes/prod_long.md)]*
    - *Solicitar aprobación para pedido de compra de Microsoft [!INCLUDE[prod_long](includes/prod_long.md)]*
    - *Solicitar aprobación para factura de compra de Microsoft [!INCLUDE[prod_long](includes/prod_long.md)]*
    - *Solicitar aprobación para abono de compra de Microsoft [!INCLUDE[prod_long](includes/prod_long.md)]*  
    - *Solicitar aprobación para producto de Microsoft [!INCLUDE[prod_long](includes/prod_long.md)]*
    - *Solicitar aprobación para proveedor de Microsoft [!INCLUDE[prod_long](includes/prod_long.md)]*
    - *Solicitar aprobación para lote de diario general de Microsoft [!INCLUDE[prod_long](includes/prod_long.md)]*  
    - *Solicitar aprobación para líneas de diario general de Microsoft [!INCLUDE[prod_long](includes/prod_long.md)]*
12. Power Automate mostrará una lista de servicios utilizados en la plantilla de flujo e intentará conectarse automáticamente a esos servicios. Si no se ha conectado previamente a un servicio, se le pedirá que inicie sesión en cada uno de los servicios a los que necesita conectarse. Aparecerá una marca de verificación verde al lado de cada servicio una vez que se haya realizado una conexión correctamente. Seleccione **Continuar**.
13. Power Automate le solicitará que seleccione un ambiente y una empresa en el suscriptor de [!INCLUDE[prod_short](includes/prod_short.md)]. Debido a que cada paso del flujo es independiente del siguiente, es posible que deba definir el ambiente y la empresa varias veces al usar una plantilla de Power Automate de [!INCLUDE[prod_short](includes/prod_short.md)].

Para obtener más información, consulte [Documentación de Power Automate](/power-automate/getting-started).

## <a name="troubleshooting"></a>Solución de problemas

### <a name="entity-set-not-found-error"></a>Error "Conjunto de entidades no encontrado"

#### <a name="problem"></a>Problema

Al crear un nuevo flujo de Power Automate usando un desencadenador de aprobación de [!INCLUDE[prod_short](includes/prod_short.md)], como *Cuando se solicita la aprobación de un documento de compra*, recibe un mensaje de error similar a:

**Conjunto de entidades no encontrado: \<name\>**

donde **\<name\>** es el nombre del servicio del servicio web que falta, como **workflowWebhookSubscriptions** o **workflowPurchaseDocumentLines**.

#### <a name="possible-cause"></a>Causa posible

Usar Power Automate para integrarse con sus solicitudes de [!INCLUDE[prod_short](includes/prod_short.md)] requiere que determinadas páginas y objetos de codeunit se publiquen como servicios web. De forma predeterminada, la mayoría de los objetos necesarios se publican como servicios web para usted. Pero en algunos casos, es posible que su ambiente se haya personalizado para que estos objetos ya no se publiquen.

#### <a name="fix"></a>Corregir

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

[Preparación para hacer negocios](ui-get-ready-business.md)  
[Flujo de trabajo](across-workflow.md)  
[Importar datos de empresa de otros sistemas financieros](across-import-data-configuration-packages.md)  
[Asignar permisos a usuarios y grupos](ui-define-granular-permissions.md)  
[Administrar flujos de trabajo de [!INCLUDE[prod_long](includes/prod_long.md)]](across-use-workflows.md)  
[Config. usuario aprobación](across-how-to-set-up-approval-users.md)  
[Configurar [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md)  
[Finanzas](finance.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]