---
title: Usar flujos de Power Automate en Business Central
description: Configure y use flujos de Power Automate para crear o modificar datos de Business Central.
author: jswymer
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: workflow, OData, Power App, SOAP, Power Automate,
ms.search.form: 1500,
ms.date: 09/13/2022
ms.author: edupont
ms.openlocfilehash: 369ee2b4aded272a8a3a21fe810b4b6c62dd1de0
ms.sourcegitcommit: 9049f75c86dea374e5bfe297304caa32f579f6e4
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 09/23/2022
ms.locfileid: "9585465"
---
# <a name="use-power-automate-flows-in-prod_short"></a>Usar flujos de Power Automate en [!INCLUDE[prod_short](includes/prod_short.md)]

Puede utilizar sus datos de [!INCLUDE[prod_short](includes/prod_short.md)] como parte de un flujo de trabajo de Microsoft Power Automate. Cree sus propios flujos y conéctese a sus datos desde orígenes internos y externos con el conector [!INCLUDE [prod_short](includes/prod_short.md)].

> [!NOTE]
> Debe disponer de una cuenta válida con [!INCLUDE[prod_short](includes/prod_short.md)] y con Power Automate.  

> [!TIP]
> Además de Power Automate, puede utilizar las plantillas de flujo de trabajo de aprobación en [!INCLUDE[prod_short](includes/prod_short.md)]. Aunque son dos sistemas de flujo de trabajo independientes, cualquier plantilla de flujo de trabajo de aprobación que cree con Power Automate se agrega a la lista de flujos de trabajo en [!INCLUDE[prod_short](includes/prod_short.md)]. Obtenga más información en [Flujos de trabajo](across-workflow.md).

Los flujos de Power Automate se activan por eventos como la creación, modificación o eliminación de registros y documentos (flujos automatizados). Los flujos también pueden ejecutarse en un horario definido por el usuario (flujos programados) o bajo demanda (flujos instantáneos).

## <a name="power-automate-features-in-prod_short"></a>Funciones de Power Automate en [!INCLUDE[prod_short](includes/prod_short.md)]

Los flujos amplían las características de los flujos de trabajo de aprobación integrados disponibles en [!INCLUDE[prod_short](includes/prod_short.md)] sin necesidad de tener conocimientos de codificación, y pueden asociarse a una amplia gama de eventos y respuestas, como cambios en los registros, actualizaciones de archivos externos, documentos publicados, así como a diferentes servicios de Microsoft y de terceros, como Microsoft Outlook, Microsoft Excel, Microsoft Dataverse, Microsoft Teams, Microsoft SharePoint, Microsoft Power Apps y otros.

Así, por ejemplo, una nueva factura de venta puede activar un flujo de trabajo para una solicitud de aprobación, que puede tener diferentes eventos establecidos en función de la respuesta del aprobador. Una respuesta negativa envía una notificación y un correo electrónico al solicitante de la aprobación. Una respuesta positiva actualiza simultáneamente una hoja de cálculo Excel situada en una carpeta de SharePoint y envía una actualización a un chat de Teams.

Los flujos instantáneos funcionan de forma similar a los accesos directos por lotes, realizando varios pasos largos con unas pocas pulsaciones de botón y se lanzan desde páginas o tablas específicas. Por ejemplo, un flujo puede añadir un botón al menú de acciones de la página **Proveedores** para bloquear los pagos a un proveedor y, al mismo tiempo, enviar correos electrónicos personalizados al contacto del proveedor y a los compradores de su empresa, así como actualizar el contacto en Outlook.

## <a name="automated-workflows"></a>Flujos de trabajo automatizados

Con Power Automate, puede crear flujos comerciales directamente de forma interna y confiar en los desarrolladores locales. Los flujos de trabajo automatizados pueden iniciarse tanto por eventos internos como externos en [!INCLUDE[prod_short](includes/prod_short.md)], y también configurarse para que se ejecuten periódicamente. Obtenga más información e instrucciones sobre cómo crear flujos de trabajo en el artículo [Configurar flujos de trabajo automatizados](/dynamics365/business-central/dev-itpro/powerplatform/automate-workflows) del contenido de administración.

## <a name="instant-flows"></a>Flujos instantáneos

A partir de la versión 1 de 2022 (mayo de 2022), los administradores en línea de [!INCLUDE [prod_short](includes/prod_short.md)] pueden [activar una característica](admin-feature-management.md) para hacer posible la ejecución de un flujo de Power Automate desde la mayoría de las páginas de listas, tarjetas y documentos. Obtenga más información en el artículo [Configurar flujos de trabajo automatizados](/dynamics365/business-central/dev-itpro/powerplatform/automate-workflows) en el contenido de la administración.

Una vez que el administrador se ha conectado a [!INCLUDE [prod_short](includes/prod_short.md)] con Power Automate, verá los flujos que su organización haya agregado cuando elija la acción **Automatizar** en las páginas correspondientes. Los flujos instantáneos se ejecutan sin salir de [!INCLUDE [prod_short](includes/prod_short.md)].

Estos flujos de trabajo instantáneos de una página dentro de [!INCLUDE [prod_short](includes/prod_short.md)] en línea pueden permanecer dentro del contexto del proceso comercial en el que se encontraba. Elija la acción **Automatizar**, en algunas páginas anidada en el menú **Más opciones**, elija la opción de menú **Power Automate** y, a continuación, elija el vínculo relevante para activar el flujo de trabajo. La conexión a Power Automate ya está configurada automáticamente.

La mayoría de los flujos requieren que complete uno o dos campos antes de elegir la acción **Ejecutar flujo**.

> [!TIP]
> Si no ve una acción **Automatizar**, entonces su [!INCLUDE [prod_short](includes/prod_short.md)] probablemente aún no se ha configurado para usar Power Automate. Obtenga más información de su administrador.

## <a name="add-more-automated-flows-and-instant-flows"></a>Agregar más flujos automatizados y flujos instantáneos

Puede crear flujos mediante el sitio web [powerautomate.microsoft.com](https://powerautomate.microsoft.com). Sin embargo, si su administrador ha activado la capacidad de ejecutar flujos de Power Automate desde dentro de [!INCLUDE [prod_short](includes/prod_short.md)] en línea, puede iniciar el proceso de construcción de un flujo desde la acción **Automatizar** en las páginas correspondientes, que se encuentra en el menú **Más opciones** según la página. A continuación, elija la opción de menú **Power Automate** y luego elija la acción **Crear un flujo**. Después, Power Automate se abre en una nueva pestaña del navegador y se inicia sesión automáticamente.

Puede encontrar plantillas de muestra para adaptarlas a su empresa y a todos los eventos de activación disponibles, tanto con [!INCLUDE [prod_short](includes/prod_short.md)] como con herramientas externas, seleccionando el menú **Conectores** en el sitio web de Power Automate. Obtenga más información sobre las plantillas y los disparadores disponibles en el artículo [Configurar flujos de trabajo automatizados](/dynamics365/business-central/dev-itpro/powerplatform/automate-workflows) en el contenido de la administración.

## <a name="manage-automated-workflows"></a>Administrar flujos de trabajo automatizados

Puede crear nuevos flujo o administrar flujos de Power Automate existentes en [!INCLUDE [prod_short](includes/prod_short.md)] en la página **Administrar flujos de Power Automate**. Obtenga más información en el artículo [Administrar flujos de Power Automate](/dynamics365/business-central/dev-itpro/powerplatform/manage-power-automate-flows.md) en el contenido de la administración.

También puede administrar flujos de trabajo de Power Automate disponibles en la página **Flujos de trabajo** en [!INCLUDE[prod_short](includes/prod_short.md)]. La página enumera tanto la aprobación incorporada como los flujos de trabajo de Power Automate con opciones para este último para activar/desactivar, eliminar y ver el flujo de trabajo en el sitio web de Power Automate.

## <a name="see-related-microsoft-training"></a>Consultar la [formación de Microsoft](/training/modules/use-power-automate/) relacionada

## <a name="see-also"></a>Consulte también .

[Solucionar problemas de sus [!INCLUDE[prod_short](includes/prod_short.md)] flujos de trabajo automatizados](across-flow-troubleshoot.md)  
[Prepárese para hacer negocios](ui-get-ready-business.md)  
[Flujos de trabajo](across-workflow.md)  
[Importar datos de empresa de otros sistemas financieros](across-import-data-configuration-packages.md)  
[Asignar permisos a usuarios y grupos](ui-define-granular-permissions.md)  
[Configurar [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md)  
[Finanzas](finance.md)  
[Administrar flujos de Power Automate](/dynamics365/business-central/dev-itpro/powerplatform/manage-power-automate-flows)  
[Configurar flujos de trabajo automatizados](/dynamics365/business-central/dev-itpro/powerplatform/automate-workflows)  
[Activar flujos instantáneos](/dynamics365/business-central/dev-itpro/powerplatform/instant-flows)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
