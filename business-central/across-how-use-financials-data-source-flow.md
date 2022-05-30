---
title: Usar Business Central en flujos de Power Automate
description: Configure y use flujos de Power Automate que crean o modifican datos de Business Central.
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: workflow, OData, Power App, SOAP, Entity set not found, workflowWebhookSubscriptions
ms.date: 05/12/2022
ms.author: edupont
author: jswymer
ms.openlocfilehash: 93eb177ff9ba102277a50f9686ea941df33d5563
ms.sourcegitcommit: 13ac10624bee47c73989b2b20942a01c849b4a6a
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 05/12/2022
ms.locfileid: "8744115"
---
# <a name="use-prod_short-in-power-automate-flows"></a>Usar [!INCLUDE[prod_short](includes/prod_short.md)] en flujos de Power Automate

Puede utilizar sus datos de [!INCLUDE[prod_short](includes/prod_short.md)] como parte de un flujo de trabajo de Microsoft Power Automate. Cree sus propios flujos y conéctese a sus datos con el conector de [!INCLUDE [prod_short](includes/prod_short.md)].  

> [!NOTE]  
> Debe disponer de una cuenta válida con [!INCLUDE[prod_short](includes/prod_short.md)] y con Power Automate.  

> [!TIP]
> Además de Power Automate, puede utilizar las plantillas de flujo de trabajo de aprobación en [!INCLUDE[prod_short](includes/prod_short.md)]. Aunque son dos sistemas de flujo de trabajo independientes, cualquier plantilla de flujo de trabajo de aprobación que cree con Power Automate se agrega a la lista de flujos de trabajo en [!INCLUDE[prod_short](includes/prod_short.md)]. Para obtener más información, consulte [Flujos de trabajo](across-workflow.md).  

## <a name="automated-workflows"></a>Flujos de trabajo automatizados

Con Power Automate, puede crear flujos comerciales directamente de forma interna y confiar en los desarrolladores locales. Para más información, consulte [Configurar flujos de trabajo automatizados](/dynamics365/business-central/dev-itpro/powerplatform/automate-workflows) en el contenido de la administración.  

## <a name="manual-instant-flows"></a>Flujos instantáneos manuales

A partir de mayo de 2022, un administrador en línea de [!INCLUDE [prod_short](includes/prod_short.md)] puede [activar una característica](admin-feature-management.md) para hacer posible la ejecución de un flujo de Power Automate de la mayoría de las páginas. Para más información, consulte [Configurar flujos de trabajo automatizados](/dynamics365/business-central/dev-itpro/powerplatform/automate-workflows) en el contenido de la administración.  

Una vez que el administrador se ha conectado a [!INCLUDE [prod_short](includes/prod_short.md)] con Power Automate, verá los flujos que su organización haya agregado cuando elija la acción **Automatizar** en las páginas correspondientes. Ejecute los flujos sin salir [!INCLUDE [prod_short](includes/prod_short.md)].  

Estos flujos de trabajo automatizados se abren en un panel de [!INCLUDE [prod_short](includes/prod_short.md)] en línea para que permanezca dentro del contexto del proceso comercial en el que se encontraba. En algunas páginas, la acción **Automatizar** se esconde bajo el menú **Más opciones**, pero encuéntralo, elija el elemento del menú **Power Automate** y, a continuación, elija el vínculo correspondiente para activar el flujo de trabajo. La conexión a Power Automate ya está configurada automáticamente.  

La mayoría de los flujos requerirán que complete uno o dos campos antes de elegir la acción **Ejecutar flujo**.  

> [!TIP]
> Si no ve una acción **Automatizar**, entonces su [!INCLUDE [prod_short](includes/prod_short.md)] probablemente aún no se ha configurado para usar Power Automate. Para obtener más información, pregunte a su administrador.

## <a name="add-more-automated-flows-and-manual-instant-flows"></a>Agregar más flujos automatizados y flujos instantáneos manuales

Puede crear flujos en el sitio web [powerautomate.microsoft.com](https://powerautomate.microsoft.com). Sin embargo, si su administrador ha activado la capacidad de ejecutar flujos de Power Automate desde dentro de [!INCLUDE [prod_short](includes/prod_short.md)] en línea, puede iniciar el proceso de creación de un flujo desde la acción **Automatizar** en las páginas correspondientes. En algunas páginas, la acción **Automatizar** se esconde bajo el menú **Más opciones**, pero encuéntrala, elija el elemento del menú **Power Automate** y, a continuación, la acción **Crear flujo**. Después, Power Automate se abre en una nueva pestaña del navegador y se inicia sesión automáticamente.

## <a name="manage-workflows"></a>Administrar flujos de trabajo

Puede obtener una descripción general de todos los flujos de trabajo a los que tiene acceso eligiendo la acción **Administrar flujos de trabajo** en el menú **Power Automate**. La lista se abre en una nueva pestaña del navegador y se inicia sesión automáticamente en Power Automate. Ahí, puede ver cuándo se ejecutó cada flujo más recientemente.  

## <a name="see-also"></a>Consulte también

[Solucionar problemas de sus [!INCLUDE[prod_short](includes/prod_short.md)] flujos de trabajo automatizados](across-flow-troubleshoot.md)  
[Prepárese para hacer negocios](ui-get-ready-business.md)  
[Flujos de trabajo](across-workflow.md)  
[Importar datos de empresa de otros sistemas financieros](across-import-data-configuration-packages.md)  
[Asignar permisos a usuarios y grupos](ui-define-granular-permissions.md)  
[Configurar [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md)  
[Finanzas](finance.md)  
[Configurar flujos de trabajo automatizados](/dynamics365/business-central/dev-itpro/powerplatform/automate-workflows)  

[!INCLUDE[footer-include](includes/footer-banner.md)]