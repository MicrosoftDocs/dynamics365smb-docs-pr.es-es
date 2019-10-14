---
title: Conectar los datos con Flow | Documentos de Microsoft
description: Puede hacer que los datos de Business Central estén disponibles como un origen de datos y especificar una URL de OData de sus servicios web para generar un flujo de trabajo automatizado.
documentationcenter: ''
author: bmeier90
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.reviewer: edupont
ms.search.keywords: workflow, Odata, Power App, SOAP
ms.date: 10/01/2019
ms.author: bmeier
ms.openlocfilehash: 86178bafa806fb8cba531d5b78157437c242d432
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/01/2019
ms.locfileid: "2305038"
---
# <a name="using-included365finincludesd365fin_mdmd-in-an-automated-workflow"></a>Usar [!INCLUDE[d365fin](includes/d365fin_md.md)] en un flujo de trabajo automatizado
Puede utilizar sus datos de [!INCLUDE[d365fin](includes/d365fin_md.md)] como parte de un flujo de trabajo de Microsoft Flow.

> [!NOTE]
> Además de Microsoft Flow, puede utilizar la funcionalidad de flujo de trabajo en [!INCLUDE[d365fin](includes/d365fin_md.md)]. Tenga en cuenta que, aunque son dos sistemas de flujo de trabajo independientes, cualquier plantilla de flujo de trabajo que cree con Microsoft Flow se agrega a la lista de flujos de trabajo en la sección [!INCLUDE[d365fin](includes/d365fin_md.md)]. Para obtener más información, consulte [Flujo de trabajo](across-workflow.md).  

> [!NOTE]  
> Debe disponer de una cuenta válida con [!INCLUDE[d365fin](includes/d365fin_md.md)] y con Flow.  

## <a name="to-add-included365finincludesd365fin_mdmd-as-a-data-source-in-flow"></a>Para agregar [!INCLUDE[d365fin](includes/d365fin_md.md)] como origen de datos de Flow
1. En el explorador, vaya a [flow.microsoft.com](https://flow.microsoft.com/en-us/) y, a continuación, inicie sesión.
2. Seleccione **Mis flujos** en la cinta en la parte superior de la página.
3. Hay tres formas de crear un flujo: **Iniciar desde plantilla**, **Iniciar desde cero** e **Iniciar desde un conector**. Una platilla es un flujo predefinido que se ha creado de forma automática. Para utilizar una plantilla, selecciónela y cree una conexión para cada servicio que la plantilla usa. Con las opciones **Iniciar desde cero** e **Iniciar desde un conector** puede crear un flujo nuevo completamente desde cero.
4. Para crear desde cero, en la página **Mis flujos**, elija las opciones **Iniciar desde cero** y **Flujo automatizado**.
5. Busque el conector de **Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]**.
6. Defina un nombre y elija el activador que desea usar para su flujo.
7. En la lista de disparadores disponibles, seleccione uno de los de [!INCLUDE[d365fin](includes/d365fin_md.md)] disponibles:  
    
    *Cuando se solicite la aprobación de un proveedor*,    
    *Cuando se solicite la aprobación de una línea de diario general*,    
    *Cuando se elimine un registro*,    
    *Cuando se cambie un registro*,    
    *Cuando se cree un registro*,    
    *Cuando se modifique un registro*,    
    *Cuando se solicite la aprobación de un lote de diario general*,   
    *Cuando se solicite la aprobación de un cliente*,   
    *Cuando se solicite la aprobación de un artículo*,    
    *Cuando se solicite la aprobación de un documento de compra* o     
     *Cuando se solicite la aprobación de un documento de ventas*.
     
8. Flow le solicitará que seleccione un ambiente y una empresa en su suscriptor de [!INCLUDE[d365fin](includes/d365fin_md.md)], así como las condiciones de los datos que desee escuchar.

> [!NOTE]  
>   El conector de [!INCLUDE[d365fin](includes/d365fin_md.md)] para Microsoft Flow admite múltiples ambientes de producción y aislados. Si no ha creado múltiples ambientes de producción o aislados, **Producción** es la única opción disponible que puede elegir. 

Ya se ha conectado correctamente con los datos de Business Central y está preparado para comenzar a crear su flujo.

9. Para crear desde una plantilla, seleccione la opción **Iniciar desde plantilla**.
10. Busque las plantillas de **Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]**.
11. En la lista de plantillas disponibles, seleccione una de las plantillas y, a continuación, elija **Crear**.  

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
    *Solicitar aprobación para lote de diario general de Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]* o    
    *Solicitar aprobación para líneas de diario general de Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]*.  
12. Flow mostrará una lista de servicios utilizados en la plantilla de Flow e intentará conectarse automáticamente a esos servicios. Si no se ha conectado previamente a un servicio, se le pedirá que inicie sesión en cada uno de los servicios a los que necesita conectarse. Aparecerá una marca de verificación verde al lado de cada servicio una vez que se haya realizado una conexión correctamente. Seleccione **Continuar**.
13. Flow le solicitará que seleccione un ambiente y una empresa en el suscriptor de [!INCLUDE[d365fin_md](includes/d365fin_md.md)]. Debido a que cada paso del flujo es independiente del siguiente, es posible que deba definir el ambiente y la empresa varias veces al usar una plantilla de Flow de [!INCLUDE[d365fin_md](includes/d365fin_md.md)].

Para obtener más información, consulte la [documentación de Flow](/flow/getting-started).

## <a name="see-also"></a>Consulte también
[Introducción](product-get-started.md)  
[Flujo de trabajo](across-workflow.md)  
[Importar datos de empresa de otros sistemas financieros](across-import-data-configuration-packages.md)  
[Administrar usuarios y permisos](ui-how-users-permissions.md)   
[Administrar flujos de trabajo de [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](across-use-workflows.md)  
[Config. usuario aprobación](across-how-to-set-up-approval-users.md)  
[Configurar [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)  
[Finanzas](finance.md)  
