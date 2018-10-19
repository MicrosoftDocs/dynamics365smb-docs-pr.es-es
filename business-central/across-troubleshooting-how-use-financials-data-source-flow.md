---
title: "Solución de problemas de integración con Microsoft Flow | Documentos de Microsoft"
description: "Solución de los problemas sobre cómo puede hacer que los datos de Business Central estén disponibles como un origen de datos y especificar una URL de OData de sus servicios web para generar un flujo de trabajo automatizado."
documentationcenter: 
author: SusanneWindfeldPedersen
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: workflow, Odata, Power App, SOAP
ms.date: 10/01/2018
ms.author: solsen
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 0818550021bf17e5a269d3e11f8db54b9ff80dfa
ms.contentlocale: es-es
ms.lasthandoff: 09/28/2018

---
# <a name="troubleshooting-integration-with-microsoft-flow---request-url-too-long"></a>Solución de problemas de integración con Microsoft Flow - Solicitud de URL demasiado larga
Puede utilizar sus datos de [!INCLUDE[d365fin](includes/d365fin_md.md)] como parte de un flujo de trabajo de Microsoft Flow.  

> [!NOTE]  
>   Debe disponer de una cuenta válida con [!INCLUDE[d365fin](includes/d365fin_md.md)] y con Flow.  

Si está creando un Microsoft Flow mediante el conector [!INCLUDE[d365fin](includes/d365fin_md.md)], después de crear el flujo puede recibir un mensaje de error que indique que la URL requerida es demasiado larga, como el siguiente: **RequestUriTooLong**.

## <a name="cause"></a>Causa
Para que se active un flujo, este busca cambios en sus datos. Al determinar si sus datos han cambiado, los conectores comparan los datos en caché con los nuevos datos solicitados de la fuente.  

Si la solicitud de datos crea una URL que es demasiado larga, fallará. Entre las causas comunes se incluyen:
- Generalmente, cualquier tabla fuente con más de 250 filas
- Tablas fuente que contienen miles de registros

## <a name="workaround"></a>Solución
Siga estos pasos como una solución.
1. Elija modificar el flujo que está fallando.
2. Amplíe **Mostrar opciones avanzadas** en el activador del flujo.
3. En el campo **Saltar recuento**, introduzca la cantidad de registros que se va a omitir.  
Por ejemplo, si la tabla que está utilizando como fuente de datos tiene 4000 registros, introduzca 4000 como la cantidad de registros que debe omitir.
4. Actualice el flujo.

> [!NOTE]  
> El conector se encuentra actualmente en versión Beta. Actualizaciones de cómo los cambios de datos están destinados a una versión futura.


## <a name="see-also"></a>Consulte también
[Usar [!INCLUDE[d365fin](includes/d365fin_md.md)] en un flujo de trabajo automatizado](across-how-use-financials-data-source-flow.md)  
[Introducción](product-get-started.md)  
[Importar datos de empresa de otros sistemas financieros](across-import-data-configuration-packages.md)  
[Gestionar usuarios y permisos](ui-how-users-permissions.md)    
[Configurar [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)  
[Finanzas](finance.md)  

