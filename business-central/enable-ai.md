---
title: Configurar Copilot y capacidades de IA
description: Este artículo explica cómo habilitar Copilot en un entorno.
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.topic: how-to
ms.date: 10/29/2023
ms.custom: bap-template
ms.search.form: 7775
ms.collection:
  - bap-ai-copilot
---

# Configurar Copilot y capacidades de IA 

<!--[!INCLUDE[ai-preview](includes/ai-preview.md)]-->

<!--This article explains how you can control the ability to create AI-powered item marketing text with Copilot for your organization. This task is done by an admin. There are two requirements that you must fulfill to make the feature available to users:-->

Este artículo explica cómo controlar Copilot y otras capacidades de IA en Business Central. Esta tarea la realiza un administrador. Copilot es una función del sistema y una parte integral de Business Central. Al igual que con la mayoría de las funciones del sistema, no otorga acceso a usuarios individuales ni puede activar o desactivar Copilot. Sin embargo, Copilot ofrece controles de gobernanza de datos y la opción de desactivar las capacidades individuales de Copilot y AI para cada entorno. Existen diferentes niveles de control de acceso a las capacidades de IA, según la característica:

- Permitir el movimiento de datos entre regiones geográficas

  Esta tarea solo es necesaria si su entorno de Business Central se encuentra en una geografía diferente a la del servicio Azure OpenAI que utiliza. [Más información](#allow-data-movement-across-geographies)

- Active la función en la página **Copilot y capacidades de IA**. [Más información](#activate-features)

- Habilite la función específica, si todavía se rige por **Administración de funciones**.

  En el segundo lanzamiento de versiones de 2023, tanto las sugerencias de textos de marketing como las funciones de asistencia para la conciliación de cuentas bancarias se incluyen en **Administración de funciones**. [Más información](#enable-feature-in-feature-management)

Si no se cumple alguno de estos requisitos, la característica no está disponible para su uso.

## Requisitos previos

- Usar Business Central Online, versión 23.1 o posterior. <!--[preview version](ai-preview-getstarted.md) of Business Central that's enabled for Copilot.-->
- Tener permisos de administrador o super en Business Central.  <!--For more information, go to [Configure AI-powered item marketing text with Copilot](enable-ai.md).-->

## Permitir el movimiento de datos entre zonas geográficas

Esta tarea se aplica solo si el interruptor **Permitir movimiento de datos** aparece cerca de la parte superior de la página **Copilot y capacidades de IA**. Si aparece el vínculo **¿Cómo controlo mis datos de copiloto?** en lugar del interruptor **Permitir movimiento de datos**, omita este paso.

![Muestra una captura de pantalla del interruptor Permitir movimiento de datos en la página Copilot y capacidades de IA.](media/allow-data-movement-v2.png)

El interruptor **Permitir movimiento de datos** indica que la ubicación de su entorno Business Central &mdash;es decir, la geografía donde se procesan y almacenan los datos&mdash; no es la misma que la geografía del servicio Azure OpenAI utilizada por Copilot. Si desea habilitar Copilot, debe permitir el movimiento de datos entre geografías. Para obtener más información sobre el movimiento de datos, vaya a [Movimiento de datos de Copilot entre geografías](ai-copilot-data-movement.md). 

Para permitir el movimiento de datos fuera de su región geográfica, complete los siguientes pasos:

1. En Business Central, busque y abra la página **Copilot y capacidades de IA**.
1. Active el interruptor **Permitir movimiento de datos**.

   El interruptor **Permitir movimiento de datos** está activado de forma predeterminada para entornos en las regiones de Azure de Europa Occidental y Europa del Norte.

Puede optar por no participar en el movimiento de datos desactivando el interruptor **Permitir movimiento de datos**. Una vez que un servicio Azure OpenAI esté disponible en la geografía de su entorno de Business Central, su entorno se conectará automáticamente a él y el conmutador ya no estará disponible.
<!--
| Australia, United Kingdom, United States | Within the respective geographical region |
| Europe, France, Germany, Norway, Switzerland  | Sweden or Switzerland |
| Asia Pacific, Brazil, Canada, India, Japan, Singapore, South Africa, South Korea, United Arab Emirates  | United States |-->



<!--Note

If your environment is hosted in North America, Copilot will use an Azure OpenAI endpoint in North America to process your data.
If your environment is hosted in Europe, Copilot will use an Azure OpenAI endpoint in Europe to process your data.
If your environment is hosted anywhere else, Copilot will use an Azure OpenAI endpoint outside of the region in which the environment is hosted.
To opt in 

Copilot and other AI capabilities use Azure OpenAI Service.  and are provided by default to only those customers with environments that have United States as their geography for data processing and storage. While the Azure OpenAI Service is available in multiple geographies including Australia, Canada, United States, France, Japan and UK, Copilot does not follow the same regional rollout schedule.

Meanwhile, customers with environments outside the United States can use Copilot AI features by opting in to share relevant data with the Azure OpenAI Service in United States or Switzerland.

The information in the following table outlines the Azure OpenAI service that's used by the Copilot services based on the geography of their Dynamics 365 environment when they opt-in to share data.-->
## Activar las funciones

Todas las capacidades de Copilot e IA están activas de forma predeterminada cuando están disponibles en versión preliminar o cuando están disponibles de forma general. Usando la página **Copilot y capacidades de IA**, puede desactivar o activar de nuevo funciones individuales para todos los usuarios.

1. En Business Central, busque y abra la página **Copilot y capacidades de IA**.

1. La página enumera todas las funciones disponibles relacionadas con Copilot y AI y su estado actual, que puede ser activo o inactivo. Las funciones se dividen en dos secciones&mdash;una sección para funciones en vista previa y otra para funciones que están disponibles de forma general. 

   [![Muestra el área de trabajo de Business Central y la lista de comprobación para Copilot](media/copilot-and-ai-capabilties-page.svg)](media/copilot-and-ai-capabilties-page.svg#lightbox)

   - Para activar una función, selecciónela en la lista, luego seleccione la acción **Activar**.
   - Para desactivar una función, selecciónela en la lista, luego seleccione la acción **Desactivar**. 


## Habilitar función en Gestión de funciones

Cuando las capacidades individuales de Copilot se lanzan en actualizaciones menores de Business Central, estas capacidades son opcionales hasta la próxima actualización importante. **Gestión de funciones** se utiliza para activar o desactivar funciones que están en vista previa, como la conciliación bancaria, y algunas funciones que están disponibles de forma general, como las sugerencias de texto de marketing. [Más información acerca de la Administración de características](/dynamics365/business-central/dev-itpro/administration/feature-management).

1. En Business Central, busque y abra la página **Gestión de características**.
2. Para habilitar una función, establezca la columna **Habilitado para** en **Todos los usuarios**. Para deshabilitar una función, establezca la columna **Habilitado para** en **Ninguno**. Utilice la siguiente tabla para ayudarle a determinar el interruptor que se aplica a la capacidad de Copilot e IA que desea habilitar:

   - **Vista previa de la función: la conciliación de cuentas bancarias con Copilot** habilita la característica de asistencia para la conciliación de cuentas bancarias.
   - **Vista previa de la función: cree descripciones de productos basadas en IA con Copilot** habilita la característica de sugerencias de texto de marketing.

   Para más información sobre la gestión de características en general, vaya a [Gestión de características](/dynamics365/business-central/dev-itpro/administration/feature-management).

## Conceder acceso de usuario 

Las capacidades de Copilot e IA pueden ofrecer funciones destinadas a cualquier usuario de su organización o a roles de usuario específicos. La mayoría de las capacidades de Copilot e IA ofrecen control de acceso mediante permisos y conjuntos de permisos en el sistema de gestión de permisos de Business Central. [Obtenga más información sobre permisos y conjuntos de permisos](ui-define-granular-permissions.md).

Para otorgar o denegar el acceso a capacidades específicas de Copilot e IA, consulte la documentación o el editor de esa función para identificar qué permisos se requieren. 

## Pasos siguientes

Después de habilitar y dar su consentimiento a las funciones, estará listo para probarlas. Ir a:

- [Agregar texto de marketing para productos](item-marketing-text.md) 
- [Conciliar con la asistencia de conciliación de cuentas bancarias](bank-reconciliation-with-copilot.md) 

## Consulte también

[Solucionar problemas de Copilot y capacidades de IA](ai-copilot-troubleshooting.md)  
[Resumen de sugerencias de texto de marketing](ai-overview.md)   
[Preguntas frecuentes para sugerencias de texto de marketing](faqs-marketing-text.md)  
