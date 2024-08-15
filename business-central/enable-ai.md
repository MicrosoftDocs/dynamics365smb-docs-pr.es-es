---
title: Configurar Copilot y capacidades de IA
description: Este artículo explica cómo habilitar Copilot en un entorno.
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.topic: how-to
ms.date: 06/28/2024
ms.custom: bap-template
ms.search.form: 7775
ms.collection:
  - bap-ai-copilot
---

# <a name="configure-copilot-and-ai-capabilities"></a>Configurar Copilot y capacidades de IA

<!--[!INCLUDE[ai-preview](includes/ai-preview.md)]-->

<!--This article explains how you can control the ability to create AI-powered item marketing text with Copilot for your organization. This task is done by an admin. There are two requirements that you must fulfill to make the feature available to users:-->

Este artículo explica cómo controlar Microsoft Copilot y otras capacidades de IA en Dynamics 365 Business Central. Un administrador debe completar estas tareas.

Copilot es una característica del sistema y una parte integral de Business Central. Al igual que con la mayoría de las funciones del sistema, no otorga acceso a usuarios individuales ni puede activar o desactivar Copilot. Sin embargo, Copilot ofrece controles de gobernanza de datos y la opción de desactivar las capacidades individuales de Copilot y AI para cada entorno. Existen diferentes niveles de control de acceso a las capacidades de IA, según la característica:

- Permitir el movimiento de datos entre regiones geográficas.

    Esta tarea solo es necesaria si su entorno de Business Central se encuentra en una geografía diferente a la del servicio Azure OpenAI que utiliza. [Obtenga más información sobre esta tarea](#allow-data-movement-across-geographies).

- Active la función en la página **Copilot y capacidades de IA**. [Obtenga más información sobre esta tarea](#activate-features).

<!-- For 2024 there are no AI features governed by **Feature Management**, so this section is not shown
- Enable the specific feature if it's governed by **Feature Management**.

  Check whether  of 2024 release wave 1, chat with Copilot, marketing text suggestions, and bank account reconciliation assist features are included under **Feature Management**. [Learn more](#enable-feature-in-feature-management)
<!-- 
- Enable the specific feature, if it's still governed by **Feature Management**.

  In 2023 release wave 2, both the marketing text suggestions and bank account reconciliation assist features are included under **Feature Management**. [Learn more](#enable-feature-in-feature-management)-->

Si no se cumple alguno de estos requisitos, la característica no está disponible para su uso.

## <a name="prerequisites"></a>Requisitos previos

- Está usando Business Central Online.
- Usted es un [administrador](#requirements-for-being-an-administrator) en Business Central.

## <a name="allow-data-movement-across-geographies"></a>Permitir el movimiento de datos entre zonas geográficas

Esta tarea se aplica solo si la opción **Permitir movimiento de datos** aparece cerca de la parte superior de la página **Copilot y capacidades de IA**. Si aparece el vínculo **¿Cómo controlo mis datos de copiloto?** en lugar de la opción **Permitir movimiento de datos**, omita esta tarea.

![Captura de pantalla que muestra la opción Permitir movimiento de datos en la página de capacidades de Copilot e IA.](media/allow-data-movement-v2.png)

La presencia de la opción **Permitir movimiento de datos** indica que la ubicación de su entorno Business Central (es decir, la geografía en la que se procesan y almacenan los datos) difiere de la geografía del servicio Azure OpenAI que utiliza Copilot. Para habilitar Copilot, debe permitir el movimiento de datos entre geografías. [Más información sobre el movimiento de datos](ai-copilot-data-movement.md).

Para permitir el movimiento de datos fuera de su región geográfica, siga estos pasos:

1. En Business Central, busque y abra la página **Copilot y capacidades de IA**.
1. Active la opción **Permitir movimiento de datos**.

    > [!NOTE]
    > Para los entornos de las regiones Azure de Europa Occidental y Europa del Norte, la opción **Permitir movimiento de datos** está activada de manera predeterminada.

Para optar por no participar en el movimiento de datos, desactive la opción **Permitir movimiento de datos**.

Una vez que un servicio Azure OpenAI esté disponible en la geografía de su entorno de Business Central, su entorno se conectará automáticamente al mismo. En ese momento, la opción **Permitir movimiento de datos** deja de aparecer en la página **Copilot y capacidades de IA**.

<!-- Don't review
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

## <a name="activate-features"></a>Activar las funciones

Todas las capacidades de Copilot e IA están activas de forma predeterminada cuando están disponibles en versión preliminar o cuando están disponibles de forma general. En la página **Copilot y capacidades de IA**, puede desactivar o activar de nuevo funciones individuales para todos los usuarios.

1. En Business Central, busque y abra la página **Copilot y capacidades de IA**.
1. La página enumera todas las funciones disponibles relacionadas con Copilot y AI y su estado actual. (El estado puede ser *Activo* o *Inactivo*.) Las funciones se dividen en dos secciones: una sección para funciones en vista previa y otra para funciones que están disponibles de forma general.

    - Para activar una función, selecciónela en la lista y luego seleccione **Activar**.
    - Para desactivar una función, selecciónela en la lista y luego seleccione **Desactivar**.

    [![Captura de pantalla que muestra los botones Activar y Desactivar para las listas de funciones en la página de capacidades de Copilot e IA.](media/copilot-and-ai-capabilties-page.svg)](media/copilot-and-ai-capabilties-page.svg#lightbox)

<!-- don't review 

<!-- For 2024 there are no AI features governed by **Feature Management**, so this section is not shown
## <a name="enable-feature-in-feature-management"></a>Enable feature in Feature Management

When individual Copilot capabilities are released in Business Central minor updates, these capabilities are optional until the next major update. **Feature Management** is used to turn on or off features that are in preview, like bank reconciliation, and some features that are generally available, like marketing text suggestions. [Learn more about feature management](/dynamics365/business-central/dev-itpro/administration/feature-management).

1. In Business Central, search for and open the **Feature Management** page.
2. To enable a feature, set the **Enabled for** column to **All users**. To disable a feature, set the **Enabled for** column to **None**. Use the following table to help you determine the switch that applies to the Copilot and AI capability you want to enable:

   - **Feature Preview: Bank account reconciliation with Copilot** enables the bank account reconciliation assist feature.
   - **Feature Preview: Chat with Copilot** enables the chat with Copilot feature.
   - **Feature preview: Create AI-powered product descriptions with Copilot** enables the marketing text suggestions feature.

   For more information about feature management in general, go to [Feature Management](/dynamics365/business-central/dev-itpro/administration/feature-management).-->

## <a name="granting-user-access"></a>Conceder acceso de usuario

Las capacidades de Copilot e IA pueden ofrecer funciones destinadas a cualquier usuario de su organización o a roles de usuario específicos. La mayoría de las capacidades de Copilot e IA ofrecen control de acceso mediante permisos y conjuntos de permisos en el sistema de gestión de permisos de Business Central. [Obtenga más información sobre permisos y conjuntos de permisos](ui-define-granular-permissions.md).

La siguiente tabla enumera los permisos necesarios para utilizar las características de Copilot proporcionadas por Business Central.

| Características de Copilot | Permisos requeridos |
|---|---|
| Asistencia de análisis | Conjunto de permisos **DATA ANALYSIS - EXEC** o permiso de ejecución en el objeto del sistema 9640 **Permitir el modo de análisis de datos**. Estos permisos son los mismos permisos necesarios para tener acceso al modo de análisis. |
| Asistencia de conciliación bancaria | Permiso en la página 7250 **Prop. IA concil. cuent. banc.** y la página 7252 **Trans. a Prop. IA cuenta libro mayor**. |
| Chat | No existen permisos ni conjuntos de permisos que controlen el acceso al chat por usuario. Si el chat está activado, está disponible para todos los usuarios. |
| Asignar documentos electrónicos | Permiso en la página 6166 **E-Doc. PO Copilot Prop**. |
| Sugerencias de texto de marketing | Permiso en la página 5836 **Texto de marketing de Copilot**. |
| Sugerencias de líneas de ventas | Permiso en la página 7275 **Sugerencias de IA de línea de ventas** y página 7276 **Sugerencias secundarias de IA de línea de ventas**. |

Para conceder o denegar el acceso a características que no sean específicas de Microsoft Copilot e IA, consulte la documentación de la característica o al editor para identificar los permisos necesarios.

## <a name="requirements-for-being-an-administrator"></a>Requisitos para ser administrador

Debe tener permisos SUPER en la cuenta de usuario de Business Central o una de las siguientes licencias de Business Central:

- Agente de administración delegada - Socio
- Agente de Helpdesk delegado - Socio
- Administrador interno
- Administrador interno de BC
- Administrador de Dynamics 365

Business Central aún no ofrece permisos granulares a nivel de objeto para que solo administradores específicos puedan configurar Copilot.

## <a name="next-steps"></a>Pasos siguientes

Después de habilitar y dar su consentimiento a las funciones, estará listo para probarlas. Vaya a los siguientes artículos:

- [Agregar texto de marketing para artículos con Copilot](item-marketing-text.md)
- [Analizar datos de listas con la ayuda de Copilot](analysis-assist.md)
- [Chatear con Copilot](chat-with-copilot.md)
- [Asignar documentos electrónicos a líneas de pedido de compra con Copilot](map-edocuments-with-copilot.md)
- [Conciliar cuentas bancarias con Copilot](bank-reconciliation-with-copilot.md)
- [Sugerir líneas en pedidos de venta con Copilot](sales-suggest-sales-lines-with-copilot.md)

## <a name="see-also"></a>Consulte también

[Solucionar problemas de Copilot y capacidades de IA](ai-copilot-troubleshooting.md)  
[Preguntas frecuentes sobre asistencia de análisis](faqs-analysis-assist.md)  
[Preguntas frecuentes para la asistencia de conciliación bancaria](faqs-bank-reconciliation.md)  
[Preguntas frecuentes sobre Chatear con Copilot](faqs-chat-with-copilot.md)  
[Preguntas frecuentes sobre la asignación de documentos electrónicos con pedidos de compra](faqs-map-edocuments.md)  
[Preguntas frecuentes para sugerencias de texto de marketing](faqs-marketing-text.md)  
[Preguntas frecuentes para las sugerencias de líneas de ventas](faq-sales-suggest-sales-lines-with-copilot.md)  
[Resumen de sugerencias de texto de marketing](ai-overview.md)
