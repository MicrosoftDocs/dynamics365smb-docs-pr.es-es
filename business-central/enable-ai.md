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
---

# <a name="configure-copilot-and-ai-capabilities"></a>Configurar Copilot y capacidades de IA

<!--[!INCLUDE[ai-preview](includes/ai-preview.md)]-->

<!--This article explains how you can control the ability to create AI-powered item marketing text with Copilot for your organization. This task is done by an admin. There are two requirements that you must fulfill to make the feature available to users:-->

Este artículo explica cómo controlar el acceso de los usuarios a Copilot y otras capacidades de IA en Business Central. Esta tarea la realiza un administrador. Hay tres niveles de control de acceso a las capacidades de Copolit y AI, según la característica:

- Consentimiento a los términos y condiciones de OpenAI [vista previa](https://dynamics.microsoft.com/legaldocs/supp-dynamics365-preview/) y [privacidad](https://go.microsoft.com/fwlink/?LinkId=521839) de Azure.

   Este consentimiento es necesario para que cualquier capacidad de Copilot o IA funcione para los usuarios. El consentimiento es global para todos los usuarios y se aplica a todas las funciones de Copilot y AI. [Más información](#consent-to-preview-and-privacy-terms)

- Permitir el movimiento de datos entre regiones geográficas

  Esta tarea solo es necesaria si su entorno de Business Central se encuentra en una geografía diferente a la del servicio Azure OpenAI que utiliza. [Más información](#allow-data-movement-across-geographies)

- Habilite la función específica, si todavía se rige por **Administración de funciones**.

  En el segundo lanzamiento de versiones de 2023, tanto las sugerencias de textos de marketing como las funciones de asistencia para la conciliación de cuentas bancarias se incluyen en **Administración de funciones**. Sin embargo, las sugerencias de texto de marketing están habilitadas de forma predeterminada. [Más información](#enable-feature-in-feature-management)

- Active la función en la página **Copilot y capacidades de IA**. [Más información](#activate-features)

Si no se cumple alguno de estos requisitos, la característica no está disponible para su uso.

## <a name="prerequisites"></a>Requisitos previos

- Usar Business Central Online, versión 23.1 o posterior. <!--[preview version](ai-preview-getstarted.md) of Business Central that's enabled for Copilot.-->
- Tener permisos de administrador o super en Business Central.  <!--For more information, go to [Configure AI-powered item marketing text with Copilot](enable-ai.md).-->

## <a name="allow-data-movement-across-geographies"></a>Consentimiento a la vista previa y términos de privacidad

Consentimiento a los términos y condiciones de [versión preliminar](https://dynamics.microsoft.com/legaldocs/supp-dynamics365-preview/) y [Declaración de privacidad de Microsoft](https://go.microsoft.com/fwlink/?LinkId=521839) en nombre de la organización. A diferencia de los avisos de privacidad para otras características y servicios, solo los administradores pueden dar su consentimiento para el uso de Azure OpenAI, lo cual lo hacen en nombre de la organización. Los usuarios no pueden decidir por sí mismos.   

1. En Business Central, busque y abra la página **Estado de los avisos de privacidad**.
2. En la columna **Nombre de la integración**, seleccione **Azure OpenAI** y, a continuación, lea las condiciones que se le presentan.
3. En la fila **Azure OpenAI**, seleccione la casilla **Acuerdo para todos** para dar su consentimiento o la casilla **En desacuerdo para todos** para rechazar.

## <a name="activate-features"></a>Habilitar función en Gestión de funciones

**Gestión de funciones** se utiliza para activar o desactivar funciones que están en vista previa, como la conciliación bancaria, y algunas funciones que están disponibles de forma general, como las sugerencias de marketing de artículos. [Más información acerca de la Administración de características](/dynamics365/business-central/dev-itpro/administration/feature-management).

1. En Business Central, busque y abra la página **Gestión de características**.
2. Para habilitar una función, establezca la columna **Habilitado para** en **Todos los usuarios**. Para deshabilitar una función, establezca la columna **Habilitado para** en **Ninguno**. Utilice la siguiente tabla para ayudarle a determinar el interruptor que se aplica a la capacidad Copilot y AO que desea habilitar:

   - **Vista previa de la función: la conciliación de cuentas bancarias con Copilot** pertenece a la función de asistencia para la conciliación de cuentas bancarias.
   - **Vista previa de la función: cree descripciones de productos basadas en IA con Copilot** pertenece a la función de sugerencias de texto de marketing.

   Para más información sobre la gestión de características en general, vaya a [Gestión de características](/dynamics365/business-central/dev-itpro/administration/feature-management).

## <a name="enable-feature-in-feature-management"></a>Permitir el movimiento de datos entre zonas geográficas

Esta tarea se aplica solo si el interruptor **Permitir movimiento de datos** aparece cerca de la parte superior de la página **Copilot y capacidades de IA**. El interruptor **Permitir movimiento de datos** indica que la ubicación de su entorno Business Central&mdash;es decir, la geografía donde se procesan y almacenan los datos&mdash;no es la misma que la geografía del servicio Azure OpenAI utilizada por Copilot. Si desea habilitar Copilot, debe permitir el movimiento de datos entre geografías. Para obtener más información sobre el movimiento de datos, vaya a [Movimiento de datos de Copilot entre geografías](ai-copilot-data-movement.md). 

Para permitir el movimiento de datos fuera de su región geográfica, complete los siguientes pasos:

1. En Business Central, busque y abra la página **Copilot y capacidades de IA**.
1. Active el interruptor **Permitir movimiento de datos**.

   ![![Texto alternativo](allow-data-movement.png)](allow-data-movement.png)

Puede optar por no participar desactivando el interruptor **Permitir movimiento de datos**. Una vez que un servicio Azure OpenAI esté disponible en la geografía de su entorno de Business Central, su entorno se conectará automáticamente a él y el conmutador ya no estará disponible. 


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
## <a name="granting-user-access"></a>Activar las funciones

Usando la página **Copilot y capacidades de IA**, puede activar o desactivar funciones individuales para todos los usuarios.

1. En Business Central, busque y abra la página **Copilot y capacidades de IA**.

1. La página enumera todas las funciones disponibles relacionadas con Copilot y AI y su estado actual, que puede ser activo o inactivo. Las funciones se dividen en dos secciones&mdash;una sección para funciones en vista previa y otra para funciones que están disponibles de forma general. 

   [![Muestra el área de trabajo de Business Central y la lista de comprobación para Copilot](media/copilot-and-ai-capabilties-page.svg)](media/copilot-and-ai-capabilties-page.svg#lightbox)

   - Para activar una función, selecciónela en la lista, luego seleccione **Activar** en la cinta.
   - Para desactivar una función, selecciónela en la lista, luego seleccione **Desactivar** en la cinta. 


## <a name="next-steps"></a>Pasos siguientes

Después de habilitar y dar su consentimiento a las funciones, estará listo para probarlas. Ir a:

- [Agregar texto de marketing para productos](item-marketing-text.md) 
- [Conciliar con la asistencia de conciliación de cuentas bancarias](bank-reconciliation-with-copilot.md) 

## <a name="see-also"></a>Consulte también .

[Resumen de sugerencias de texto de marketing](ai-overview.md)   
[Preguntas frecuentes para sugerencias de texto de marketing](faqs-marketing-text.md)  
