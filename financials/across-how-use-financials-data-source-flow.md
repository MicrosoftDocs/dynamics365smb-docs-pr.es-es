---
title: Conectar los datos con Flow | Documentos de Microsoft
description: "Puede hacer que los datos de Financials estén disponibles como un origen de datos y especificar una URL de OData de sus servicios web para generar un flujo de trabajo automatizado."
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: workflow, Odata, Power App, SOAP
ms.date: 01/25/2018
ms.author: solsen
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: ef4d841723b6bb0af37695a8c3ed1d805319be78
ms.contentlocale: es-es
ms.lasthandoff: 01/30/2018

---
# <a name="using-included365finincludesd365finmdmd-in-an-automated-workflow"></a>Usar [!INCLUDE[d365fin](includes/d365fin_md.md)] en un flujo de trabajo automatizado
Puede utilizar sus datos de [!INCLUDE[d365fin](includes/d365fin_md.md)] como parte de un flujo de trabajo de Microsoft Flow.  

> [!NOTE]  
>   Debe disponer de una cuenta válida con [!INCLUDE[d365fin](includes/d365fin_md.md)] y con Flow.  

## <a name="to-add-included365finincludesd365finmdmd-as-a-data-source-in-flow"></a>Para agregar [!INCLUDE[d365fin](includes/d365fin_md.md)] como origen de datos de Flow
1. En el explorador, vaya a [flow.microsoft.com](https://flow.microsoft.com/en-us/) y, a continuación, inicie sesión.
2. Seleccione **Mis flujos** en la cinta en la parte superior de la página.
3. En la ventana **Mis flujos**, elija la opción **Crear desde cero**.
4. En la lista de disparadores disponibles, seleccione uno de los de [!INCLUDE[d365fin](includes/d365fin_md.md)] disponibles:  
    *Cuando se cree un registro*,  
    *Cuando se elimine un registro*,  
    *Cuando se modifique un registro*,  
    *Cuando se solicite la aprobación de un cliente*,  
    *Cuando se solicite la aprobación de un lote de diario general*,  
    *Cuando se solicite la aprobación de una línea de diario general*,  
    *Cuando se solicite la aprobación de un artículo*,  
    *Cuando se solicite la aprobación de un documento de compra*,  
    *Cuando se solicite la aprobación de un documento de ventas*, o  
    *Cuando se solicite la aprobación de un proveedor*.
5. Flow le solicitará la información necesaria para conectarse con los datos de [!INCLUDE[d365fin](includes/d365fin_md.md)]. Si ha seleccionado uno de los disparadores siguientes: *Cuando se cree un registro*, *Cuando se modifique un registro* o *Cuando se elimine un registro*, debe seleccionar un nombre de la empresa y un nombre de la tabla. Si utiliza otro disparador, únicamente será necesario el nombre de la empresa para conectarse.

   Flow mostrará una lista de empresas y tablas que están disponibles en [!INCLUDE[d365fin](includes/d365fin_md.md)]. Estas tablas, o extremos, representan todos los servicios web que haya publicado desde [!INCLUDE[d365fin](includes/d365fin_md.md)].

   Si lo desea, puede crear una nueva dirección URL de servicio Web en [!INCLUDE[d365fin](includes/d365fin_md.md)] mediante la acción **Crear conjunto de datos** en la página **Servicios web**, utilizando la guía de configuración asistida **Configurar informes** o eligiendo la acción **Editar en Excel** en cualquier lista.

Ya se ha conectado correctamente con los datos de Finance and Operations, Business edition y está preparado para comenzar a crear su flujo. Para obtener más información, consulte la [documentación de Flow](https://flow.microsoft.com/documentation/getting-started/).

Para solucionar problemas de Microsoft Flow, vea [Solución de problemas de integración con Microsoft Flow](across-troubleshooting-how-use-financials-data-source-flow.md).

## <a name="see-also"></a>Consulte también
[[!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)  
[Importar datos de empresa de otros sistemas financieros](upload-data.md)  
[Gestionar usuarios y permisos](ui-how-users-permissions.md)    
[Configurar [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)  
[Finanzas](finance.md)  

