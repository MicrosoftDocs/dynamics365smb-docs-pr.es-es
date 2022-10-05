---
title: Flujos de trabajo en Dynamics 365 Business Central
description: Use las capacidades de flujo de trabajo integradas para configurar flujos de trabajo de aprobación para complementar los flujos de trabajo automatizados basados en Power Automate. Puede configurar pasos para asignar tareas a diferentes personas como parte de las diferentes tareas del proceso empresarial.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 09/13/2022
ms.author: edupont
ms.openlocfilehash: ecaaf9bbb56e1c1b47f9f617319b32f32a2920fd
ms.sourcegitcommit: 9049f75c86dea374e5bfe297304caa32f579f6e4
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 09/23/2022
ms.locfileid: "9585627"
---
# <a name="workflows-in-dynamics-365-business-central"></a>Flujos de trabajo en Dynamics 365 Business Central

Puede configurar y utilizar flujos de trabajo para vincular tareas de procesos empresariales realizadas por distintos usuarios. Las tareas de sistema, como registros automáticos, se pueden incluir como pasos en los flujos de trabajo, antes o después de las tareas de usuario. Solicitar y conceder aprobaciones para crear registros nuevos son pasos habituales de un flujo de trabajo.

La versión predeterminada de [!INCLUDE [prod_short](includes/prod_short.md)] admite tres tipos de flujos de trabajo:

* Flujos de trabajo de aprobación basados en plantillas de flujo de trabajo integradas

  En la página **Plantillas de flujo de trabajo**, puede ver todos los flujos de trabajo disponibles. La versión de prueba de [!INCLUDE[prod_short](includes/prod_short.md)] incluye muchos flujos de trabajo preconfigurados que están representados por plantillas de flujo de trabajo que puede copiar para crear flujos de trabajo nuevos. Cuando abre una plantilla desde la página **Plantillas de flujo de trabajo** y el nombre del flujo de trabajo comienza por *MS-*, Microsoft agrega la plantilla de flujo de trabajo.
  
* Flujos de Power Automate que usted mismo configura

  Cualquier plantilla de flujo de trabajo que cree con Microsoft Power Automate se agrega a la lista de plantillas de flujo de trabajo en [!INCLUDE[prod_short](includes/prod_short.md)]. Obtenga más información en [Usar [!INCLUDE[prod_short](includes/prod_short.md)] en flujos de Power Automate](across-how-use-financials-data-source-flow.md). 
  
* Flujos instantáneos activados manualmente por la acción **Automatizar** (solo en [!INCLUDE [prod_short](includes/prod_short.md)] en línea).

  Cree y active manualmente un flujo de Power Automate en un registro [!INCLUDE[prod_short](includes/prod_short.md)] como un cliente, un artículo o un pedido de venta, con opciones para manipular la información tanto interna como externamente (utilizando herramientas integradas). Obtenga más información en la sección [Flujos instantáneos](across-how-use-financials-data-source-flow.md#instant-flows).

## <a name="power-automate-flows"></a>Flujos de Power Automate

Usando [!INCLUDE [prod_short](includes/prod_short.md)] en línea, puede registrarse en Power Automate para crear potentes flujos de trabajo automatizados. Puede ejecutar esos flujos de trabajo desde dentro de [!INCLUDE [prod_short](includes/prod_short.md)], conectando fuentes internas y externas de datos y herramientas, sin necesidad de tener conocimientos de codificación.

Los flujos de Power Automate pueden ser activados por eventos (como la creación, modificación o eliminación de un registro o documento) y ejecutarse según una programación definida por el usuario, o bajo demanda (lo que se conoce como un **Flujo instantáneo**).

## <a name="approval-workflows"></a>Flujos de trabajo de aprobación

Puede crear un flujo de trabajo de aprobación haciendo una lista de los pasos utilizados en las líneas. Cada paso consta de un evento del flujo de trabajo, moderado por condiciones de evento, y una respuesta de flujo de trabajo, moderada por las opciones de respuesta. Los pasos del flujo de trabajo se definen rellenando los campos de las líneas de flujo de trabajo usando listas fijas de valores de evento y respuesta que representan los escenarios de flujo de trabajo que admite el código de aplicación.<!--What are the "values"? Can we give an example?-->

Los ejemplos de eventos de flujos de trabajo de aprobación incluyen, entre otros, la creación de pedidos/ofertas/facturas de venta o de compra, cambios de precios y ediciones de proveedores o clientes.

[!INCLUDE[workflow](includes/workflow.md)]

| **Para** | **Vea** |
|--|--|
| Configure usuarios de flujo de trabajo de aprobación, especifique cómo reciben notificaciones los usuarios y cree nuevos flujos de trabajo. (Para crear nuevos flujos de trabajo en situaciones no compatibles, implemente los elementos de flujo de trabajo necesarios personalizando el código de aplicación.) | [Configurar flujos de trabajo de aprobación](across-set-up-workflows.md) |
| Habilite flujos de trabajo de aprobación, actúe al recibir notificaciones de flujos de trabajo, incluida la solicitud y la aprobación de un paso de flujo de trabajo. Archive y elimine flujos de trabajo. | [Usar flujos de trabajo de aprobación](across-use-workflows.md) |
| Integre los datos de la empresa con los flujos de trabajo de Power Automate utilizando fuentes y eventos tanto internos como externos para crear y automatizar tareas o flujos de trabajo. | [Usar flujos de Power Automate en [!INCLUDE[prod_short](includes/prod_short.md)]](across-how-use-financials-data-source-flow.md) |

## <a name="see-related-microsoft-training"></a>Consultar la [formación de Microsoft](/training/modules/create-workflows/) relacionada

## <a name="see-also"></a>Consulte también .

[Ccial](sales-manage-sales.md)  
[Compras](purchasing-manage-purchasing.md)  
[Administrar proyectos](projects-manage-projects.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Solucionar problemas de sus [!INCLUDE[prod_short](includes/prod_short.md)] flujos de trabajo automatizados](across-flow-troubleshoot.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
