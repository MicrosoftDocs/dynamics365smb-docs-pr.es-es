---
title: Flujos de trabajo en Dynamics 365 Business Central
description: Use las capacidades de flujo de trabajo integradas para configurar flujos de trabajo de aprobación para complementar los flujos de trabajo automatizados basados en Power Automate. Puede configurar pasos para asignar tareas a diferentes personas como parte de las diferentes tareas del proceso empresarial.
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.date: 10/10/2022
ms.custom: bap-template
---
# Flujos de trabajo en Dynamics 365 Business Central

Puede configurar y utilizar flujos de trabajo para vincular tareas de procesos empresariales realizadas por distintos usuarios. Las tareas del sistema, como la publicación automática, se pueden incluir como pasos de flujos de trabajo. Las tareas del sistema pueden estar precedidas o seguidas por tareas de usuario. Solicitar y conceder aprobaciones para crear registros nuevos son pasos habituales de un flujo de trabajo.

La versión predeterminada de [!INCLUDE [prod_short](includes/prod_short.md)] admite tres tipos de flujos de trabajo:
  
* Flujos de Power Automate

  * Flujos automatizados que se activan por eventos (como la creación, modificación o eliminación de registros) en [!INCLUDE[prod_short](includes/prod_short.md)]. También se incluyen flujos de aprobación creados en Power Automate que se activan cuando se solicita una aprobación en [!INCLUDE[prod_short](includes/prod_short.md)].
  * Flujos instantáneos que son activados manualmente desde el menú de acción **Automatizar** en listas, tarjetas y páginas de documentos.

    Cree y active manualmente un flujo de Power Automate en un registro [!INCLUDE[prod_short](includes/prod_short.md)] como un cliente, un artículo o un pedido de venta, con opciones para manipular la información tanto interna como externamente (utilizando herramientas integradas).

* Flujos de trabajo de aprobación basados en plantillas de flujo de trabajo integradas

  En la página **Plantillas de flujo de trabajo**, puede ver todos los flujos de trabajo disponibles. La versión de prueba de [!INCLUDE[prod_short](includes/prod_short.md)] incluye muchos flujos de trabajo preconfigurados que están representados por plantillas de flujo de trabajo que puede copiar para crear flujos de trabajo nuevos. Cuando abre una plantilla desde la página **Plantillas de flujo de trabajo** y el nombre del flujo de trabajo comienza por *MS-*, Microsoft agrega la plantilla de flujo de trabajo.

## Flujos de Power Automate

Con [!INCLUDE [prod_short](includes/prod_short.md)] en línea, puede registrarse en Power Automate para crear potentes flujos de trabajo automatizados. Usted ejecuta esos flujos de trabajo desde [!INCLUDE [prod_short](includes/prod_short.md)]. Los flujos pueden conectar orígenes de datos internos y externos y herramientas, sin necesidad de tener conocimientos de codificación.

|**Para** |**Consulte**|
|-------|-------|
|Empezar con Power Automate, creando flujos y ejecutando flujos instantáneos|[Usar flujos de Power Automate en [!INCLUDE[prod_short](includes/prod_short.md)]](across-how-use-financials-data-source-flow.md)|
|Obtenga más información sobre cómo crear, editar y administrar flujos|[Configurar flujos automatizados](/dynamics365/business-central/dev-itpro/powerplatform/automate-workflows) y [Configurar flujos instantáneos](/dynamics365/business-central/dev-itpro/powerplatform/instant-flows)|
|Configurar la integración de Power Automate con [!INCLUDE[prod_short](includes/prod_short.md)] para usuarios como administrador|[Configurar la integración de Power Automate](/dynamics365/business-central/dev-itpro/powerplatform/power-automate-setup)|

## Flujos de trabajo de aprobación

Cree un flujo de trabajo de aprobación definiendo qué inicia el flujo de trabajo y qué sucede a continuación, de la siguiente manera:

* Un evento de flujo de trabajo, moderado por las condiciones del evento.
* Una respuesta de flujo de trabajo, que está moderada por las opciones de respuesta.

Para definir los pasos del flujo de trabajo, debe rellenar los campos en las líneas de flujo de trabajo usando el evento y valores de respuesta que representan los escenarios admitidos.

Los ejemplos de eventos de flujos de trabajo de aprobación incluyen la creación de pedidos/ofertas/facturas de venta o de compra, cambios de precios, ediciones de proveedores o clientes, y más.

[!INCLUDE[workflow](includes/workflow.md)]

| **Para** | **Vea** |
|--|--|
| Configure usuarios de flujo de trabajo de aprobación, especifique cómo reciben notificaciones los usuarios y cree nuevos flujos de trabajo. (Para crear nuevos flujos de trabajo en situaciones no compatibles, implemente los elementos de flujo de trabajo necesarios personalizando el código de aplicación.) | [Configurar flujos de trabajo de aprobación](across-set-up-workflows.md) |
| Habilite flujos de trabajo de aprobación, actúe al recibir notificaciones de flujos de trabajo, incluida la solicitud y la aprobación de un paso de flujo de trabajo. Archive y elimine flujos de trabajo. | [Usar flujos de trabajo de aprobación](across-use-workflows.md) |

<!--
| Integrate company data with Power Automate workflows, using both internal and external sources and events to create and automate tasks or workflows. | [Use Power Automate Flows in [!INCLUDE[prod_short](includes/prod_short.md)]](across-how-use-financials-data-source-flow.md) |-->

## Consulte también .

[Ventas](sales-manage-sales.md)  
[Compras](purchasing-manage-purchasing.md)  
[Administrar proyectos](projects-manage-projects.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Solucionar problemas de sus [!INCLUDE[prod_short](includes/prod_short.md)] flujos de trabajo automatizados](across-flow-troubleshoot.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
