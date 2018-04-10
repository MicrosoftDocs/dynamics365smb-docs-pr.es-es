---
title: Conectar los datos con Flow | Documentos de Microsoft
description: "Puede hacer que los datos de Financials estén disponibles como un origen de datos y especificar una URL de OData de sus servicios web para generar un flujo de trabajo automatizado."
documentationcenter: 
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: workflow, Odata, Power App, SOAP
ms.date: 03/21/2018
ms.author: solsen
ms.translationtype: HT
ms.sourcegitcommit: e7dcdc0935a8793ae226dfc2f9709b5b8f487a62
ms.openlocfilehash: 5d7fa359ee99cd177a445e025ddf8d156c6e2421
ms.contentlocale: es-es
ms.lasthandoff: 03/22/2018

---
# <a name="using-included365finincludesd365finmdmd-in-an-automated-workflow"></a>Usar [!INCLUDE[d365fin](includes/d365fin_md.md)] en un flujo de trabajo automatizado
Puede utilizar sus datos de [!INCLUDE[d365fin](includes/d365fin_md.md)] como parte de un flujo de trabajo de Microsoft Flow.  

> [!NOTE]  
>   Debe disponer de una cuenta válida con [!INCLUDE[d365fin](includes/d365fin_md.md)] y con Flow.  

## <a name="to-add-included365finincludesd365finmdmd-as-a-data-source-in-flow"></a>Para agregar [!INCLUDE[d365fin](includes/d365fin_md.md)] como origen de datos de Flow
1. En el explorador, vaya a [flow.microsoft.com](https://flow.microsoft.com/en-us/) y, a continuación, inicie sesión.
2. Seleccione **Mis flujos** en la cinta en la parte superior de la página.
3. Existen 2 formas de crear un flujo; **Crear desde plantilla** y **Crear desde cero**. Una platilla es un flujo predefinido que se ha creado de forma automática.  Para utilizar una plantilla, selecciónela y cree una conexión para cada servicio que la plantilla usa. Una plantilla en blanco permite crear un nuevo flujo completamente desde cero. 
4. Para crear desde cero, en la ventana **Mis flujos**, elija la opción **Crear desde cero**.
5. Busque el conector de **Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]**.
6. En la lista de disparadores disponibles, seleccione uno de los de [!INCLUDE[d365fin](includes/d365fin_md.md)] disponibles:  
    *Cuando se solicite la aprobación de un cliente*,  
    *Cuando se solicite la aprobación de un lote de diario general*,  
    *Cuando se solicite la aprobación de una línea de diario general*,  
    *Cuando se solicite la aprobación de un artículo*,  
    *Cuando se solicite la aprobación de un documento de compra*,  
    *Cuando se solicite la aprobación de un documento de ventas*, o  
    *Cuando se solicite la aprobación de un proveedor*.
7. El flujo le solicitará que seleccione una empresa en su suscriptor [!INCLUDE[d365fin](includes/d365fin_md.md)], así como las condiciones de los datos que desee escuchar. 

Ya se ha conectado correctamente con los datos de Business Central y está preparado para comenzar a crear su flujo. 

8. Para crear desde una plantilla, seleccione la opción **Crear desde plantilla**.
9. Busque las plantillas de **Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]**. 
10. En la lista de plantillas disponibles, seleccione una de las plantillas.  
    *Solicitar aprobación para pedido de [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]*,  
    *Solicitar aprobación para oferta de venta de [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]*,  
    *Solicitar aprobación para factura de venta de [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]*,  
    *Solicitar aprobación para abono de venta de [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]*,  
    *Solicitar aprobación para cliente de [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]*,  
    *Solicitar aprobación para pedido de compra de [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]*,  
    *Solicitar aprobación para factura de compra de [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]*,  
    *Solicitar aprobación para abono de compra de [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]*,  
    *Solicitar aprobación para producto de [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]*,  
    *Solicitar aprobación para proveedor de [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]*,  
    *Solicitar aprobación para lote de diario general de Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]*,  
    *Solicitar aprobación para líneas de diario general de Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]*.  
11. Flow le solicitará que seleccione una empresa en el suscriptor [!INCLUDE[d365fin_md](includes/d365fin_md.md)]. Debido a que cada paso de Flow es independiente del siguiente, es posible que deba definir la empresa varias veces al usar una plantilla de [!INCLUDE[d365fin_md](includes/d365fin_md.md)].
12. La plantilla de Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] se integra con el motor de flujo de trabajo básico de Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]. Lo que significa que cada vez que utiliza una de estas plantillas para crear un flujo, un flujo de trabajo correspondiente se crea en Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)].  Consulte la documentación de flujo de trabajo de Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)].

Para obtener más información, consulte la [documentación de Flow](https://docs.microsoft.com/en-us/flow/getting-started).

Para solucionar problemas de Microsoft Flow, vea [Solución de problemas de integración con Microsoft Flow](across-troubleshooting-how-use-financials-data-source-flow.md).

## <a name="see-also"></a>Consulte también
[Introducción](product-get-started.md)  
[Importar datos de empresa de otros sistemas financieros](upload-data.md)  
[Gestionar usuarios y permisos](ui-how-users-permissions.md)   
[Administrar flujos de trabajo de [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](across-use-workflows.md)  
[Config. usuario aprobación](across-how-to-set-up-approval-users.md)  
[Configurar [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)  
[Finanzas](finance.md)  

