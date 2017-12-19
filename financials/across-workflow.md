---
title: Flujo de trabajo | Documentos de Microsoft
description: "Puede configurar y utilizar flujos de trabajo que vinculen tareas de procesos empresariales realizadas por distintos usuarios. Las tareas de sistema, como registros automáticos, se pueden incluir como pasos en los flujos de trabajo, antes o después de las tareas de usuario. Solicitar y conceder aprobaciones para crear registros nuevos son pasos habituales de un flujo de trabajo."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: a49e50213f808fb72b43dfa22a34833b306ef12d
ms.openlocfilehash: 58f2aa5a26275820d0fafcc79fec5be118857d78
ms.contentlocale: es-es
ms.lasthandoff: 12/14/2017

---
# <a name="workflow"></a>Flujo de trabajo
Puede configurar y utilizar flujos de trabajo que vinculen tareas de procesos empresariales realizadas por distintos usuarios. Las tareas de sistema, como registros automáticos, se pueden incluir como pasos en los flujos de trabajo, antes o después de las tareas de usuario. Solicitar y conceder aprobaciones para crear registros nuevos son pasos habituales de un flujo de trabajo.  

 En la ventana **Flujo de trabajo** creas un flujo de trabajo haciendo una lista de los pasos utilizados en las líneas. Cada paso consta de un evento del flujo de trabajo, moderado por condiciones de evento, y una respuesta de flujo de trabajo, moderada por las opciones de respuesta. Los pasos del flujo de trabajo se definen rellenando los campos de las líneas de flujo de trabajo en listas fijas de valores de evento y respuesta que representan los escenarios de flujo de trabajo que admite el código de aplicación.  

 La versión genérica de [!INCLUDE[d365fin](includes/d365fin_md.md)] incluye un número de flujos de trabajo preconfigurados que están representados por plantillas de flujo de trabajo que puede copiar para crear flujos de trabajo. El código para las plantillas de flujo de trabajo agregadas por Microsoft llevan el prefijo “MS-“. Para más información, consulta las plantillas de la lista de flujo de trabajo en la ventana Plantillas de flujo de trabajo.  

 Si una situación de negocio requiere un evento de flujo de trabajo o respuesta no compatibles, un asociado de Microsoft tiene que implementarlos personalizando el código de aplicación. Para obtener más información, consulte [Tutorial: Implementación de nuevos eventos y respuestas de flujo de trabajo](/dynamics_nav/Walkthrough--Implementing-New-Workflow-Events-and-Responses) en la ayuda para desarrolladores e informáticos.  

 En la tabla siguiente se indican una serie de tareas con vínculos a los temas que las describen.  

|**Para**|**Consulte**|  
|------------|-------------|  
|Configure usuarios de flujo de trabajo, especifique cómo reciben notificaciones los usuarios y cree nuevos flujos de trabajo. Para nuevos flujos de trabajo en situaciones no compatibles, implemente los elementos de flujo de trabajo necesarios personalizando el código de aplicación.|[Configuración de flujos de trabajo](across-set-up-workflows.md)|  
|Habilite flujos de trabajo, actúe al recibir notificaciones de flujos de trabajo, incluida la aprobación de solicitudes, para realizar un paso del flujo de trabajo. Archive y elimine flujos de trabajo.|[Uso de flujos de trabajo](across-use-workflows.md)|  

## <a name="see-also"></a>Consulte también  
[Ccial](sales-manage-sales.md)  
[Compras](purchasing-manage-purchasing.md)  
[Administrar proyectos](projects-manage-projects.md)  
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

