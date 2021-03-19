---
title: Conectar los datos con Power Automate | Documentos de Microsoft
description: Puede hacer que los datos de Business Central estén disponibles como un origen de datos y especificar una URL de OData de sus servicios web para generar un flujo de trabajo automatizado.
author: bmeier90
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.reviewer: edupont
ms.search.keywords: workflow, OData, Power App, SOAP
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 1608330b5d2b2955a144498e5c44d40072b22a8b
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5384204"
---
# <a name="using-prod_short-in-an-automated-workflow"></a>Usar [!INCLUDE[prod_short](includes/prod_short.md)] en un flujo de trabajo automatizado

Puede utilizar sus datos de [!INCLUDE[prod_short](includes/prod_short.md)] como parte de un flujo de trabajo de Microsoft Power Automate.

> [!NOTE]
> Además de Power Automate, puede utilizar la funcionalidad de flujo de trabajo en [!INCLUDE[prod_short](includes/prod_short.md)]. Tenga en cuenta que, aunque son dos sistemas de flujo de trabajo independientes, cualquier plantilla de flujo de trabajo que cree con Power Automate se agrega a la lista de flujos de trabajo en [!INCLUDE[prod_short](includes/prod_short.md)]. Para obtener más información, consulte [Flujo de trabajo](across-workflow.md).  

> [!NOTE]  
> Debe disponer de una cuenta válida con [!INCLUDE[prod_short](includes/prod_short.md)] y con Power Automate.  

## <a name="to-add-prod_short-as-a-data-source-in-power-automate"></a>Para agregar [!INCLUDE[prod_short](includes/prod_short.md)] como origen de datos de Power Automate

1. En el explorador, vaya a [flow.microsoft.com](https://flow.microsoft.com) y, a continuación, inicie sesión.
2. Seleccione **Mis flujos** en la cinta en la parte superior de la página.
3. Hay tres formas de crear un flujo: **Iniciar desde plantilla**, **Iniciar desde cero** e **Iniciar desde un conector**. Una plantilla es un flujo predefinido que se ha creado de forma automática. Para utilizar una plantilla, selecciónela y cree una conexión para cada servicio que la plantilla usa. Con las opciones **Iniciar desde cero** e **Iniciar desde un conector** puede crear un flujo nuevo completamente desde cero.
4. Para crear desde cero, en la página **Mis flujos**, elija las opciones **Iniciar desde cero** y **Flujo automatizado**.
5. Busque el conector de **Microsoft [!INCLUDE[prod_long](includes/prod_long.md)]**.
6. Defina un nombre y elija el activador que desea usar para su flujo.
7. En la lista de disparadores disponibles, seleccione uno de los de [!INCLUDE[prod_short](includes/prod_short.md)] disponibles:  

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

8. Power Automate le solicitará que seleccione un ambiente y una empresa en su suscriptor de [!INCLUDE[prod_short](includes/prod_short.md)], así como las condiciones de los datos que desee escuchar.

    > [!NOTE]
    > El conector de [!INCLUDE[prod_short](includes/prod_short.md)] para Power Automate admite múltiples ambientes de producción y aislados. Si no ha creado múltiples ambientes de producción o aislados, **Producción** es la única opción disponible que puede elegir.  

    Ya se ha conectado correctamente con los datos de Business Central[!INCLUDE[prod_short](includes/prod_short.md)] y está preparado para comenzar a crear su flujo.

9. Para crear desde una plantilla, seleccione la opción **Iniciar desde plantilla**.
10. Busque las plantillas de **Microsoft [!INCLUDE[prod_long](includes/prod_long.md)]**.
11. En la lista de plantillas disponibles, seleccione una de las plantillas y, a continuación, elija **Crear**.  

    *Solicitar aprobación para pedido de [!INCLUDE[prod_long](includes/prod_long.md)]*,  
    *Solicitar aprobación para oferta de venta de [!INCLUDE[prod_long](includes/prod_long.md)]*,  
    *Solicitar aprobación para factura de venta de [!INCLUDE[prod_long](includes/prod_long.md)]*,  
    *Solicitar aprobación para abono de venta de [!INCLUDE[prod_long](includes/prod_long.md)]*,  
    *Solicitar aprobación para cliente de [!INCLUDE[prod_long](includes/prod_long.md)]*,  
    *Solicitar aprobación para pedido de compra de [!INCLUDE[prod_long](includes/prod_long.md)]*,  
    *Solicitar aprobación para factura de compra de [!INCLUDE[prod_long](includes/prod_long.md)]*,  
    *Solicitar aprobación para abono de compra de [!INCLUDE[prod_long](includes/prod_long.md)]*,  
    *Solicitar aprobación para producto de [!INCLUDE[prod_long](includes/prod_long.md)]*,  
    *Solicitar aprobación para proveedor de [!INCLUDE[prod_long](includes/prod_long.md)]*,  
    *Solicitar aprobación para lote de diario general de Microsoft [!INCLUDE[prod_long](includes/prod_long.md)]* o    
    *Solicitar aprobación para líneas de diario general de Microsoft [!INCLUDE[prod_long](includes/prod_long.md)]*.  
12. Power Automate mostrará una lista de servicios utilizados en la plantilla de flujo e intentará conectarse automáticamente a esos servicios. Si no se ha conectado previamente a un servicio, se le pedirá que inicie sesión en cada uno de los servicios a los que necesita conectarse. Aparecerá una marca de verificación verde al lado de cada servicio una vez que se haya realizado una conexión correctamente. Seleccione **Continuar**.
13. Power Automate le solicitará que seleccione un ambiente y una empresa en el suscriptor de [!INCLUDE[prod_short](includes/prod_short.md)]. Debido a que cada paso del flujo es independiente del siguiente, es posible que deba definir el ambiente y la empresa varias veces al usar una plantilla de Power Automate de [!INCLUDE[prod_short](includes/prod_short.md)].

Para obtener más información, consulte [Documentación de Power Automate](/power-automate/getting-started).

## <a name="see-also"></a>Consulte también

[Introducción](product-get-started.md)  
[Flujo de trabajo](across-workflow.md)  
[Importar datos de empresa de otros sistemas financieros](across-import-data-configuration-packages.md)  
[Asignar permisos a usuarios y grupos](ui-define-granular-permissions.md)  
[Administrar flujos de trabajo de [!INCLUDE[prod_long](includes/prod_long.md)]](across-use-workflows.md)  
[Config. usuario aprobación](across-how-to-set-up-approval-users.md)  
[Configurar [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md)  
[Finanzas](finance.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]