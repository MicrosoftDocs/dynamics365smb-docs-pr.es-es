---
title: Funciones de prueba que se conectan a otros servicios de Microsoft
description: Descripción general de los servicios de Microsoft a los que Business Central se conecta con la versión de prueba.
author: jswymer
ms.topic: overview
ms.service: dynamics365-business-central
ms.search.keywords: 'privacy, trial, Microsoft services'
ms.date: 10/28/2022
ms.author: jswymer
ms.reviewer: jswymer
---
# <a name="trial-features-that-connect-to-other-microsoft-services"></a><a name="trial-features-that-connect-to-other-microsoft-services"></a>Funciones de prueba que se conectan a otros servicios de Microsoft

[!INCLUDE[prod_long](includes/prod_long.md)] es una solución integral de gestión empresarial que está profundamente integrada con aplicaciones de productividad Microsoft 365 y Power Platform. Su versión de prueba gratuita de Business Central puede conectarse a muchos servicios diferentes de Microsoft que primero debe configurar y habilitar. Para aprovechar al máximo su prueba gratuita, algunas de estas funciones se han habilitado automáticamente para usted. Aunque la conexión de [!INCLUDE[prod_short](includes/prod_short.md)] está habilitada, estos servicios no están incluidos con su versión de prueba y deben comprarse por separado a menos que ya los tenga.

La siguiente tabla indica las conexiones a los servicios de Microsoft que se habilitan automáticamente para pruebas de [!INCLUDE[prod_short](includes/prod_short.md)]:

|Nombre del servicio|La conexión está activada automáticamente |Se contacta con el servicio al iniciar sesión en Business Central |Característica de ejemplo que utiliza este servicio | Aprenda a administrar la conexión y las funciones que la utilizan|  
|------------|-------------|--------|------------|-------------|
|Microsoft Teams|Sí|N.º|Acción **Compartir con Teams** en la tarjeta **Artículo** |[Administrar la integración de Teams con Business Central](admin-teams-integration.md)|  
|Microsoft OneDrive para la Empresa|Sí|N.º|Acción **Abrir en OneDrive** acción sobre archivos adjuntos **Artículo** |[Administrar la integración de OneDrive con Business Central](admin-onedrive-integration.md#configure-onedrive-using-onedrive-setup)|  
| Microsoft Power Automate |Sí|No|**Automatizar** acciones en la ficha **Artículo** |[Configurar la integración de Power Automate](/dynamics365/business-central/dev-itpro/powerplatform/power-automate-setup)|
| Microsoft Azure OpenAI Automate |Sí |No|**Copilot (vista previa)** |[Configurar texto de marketing de productos impulsado por IA con Copilot](enable-ai.md)|

> [!NOTE]
> Mediante el uso de funciones que se conectan a estos servicios: 
>
> - Usted acepta que sus datos se compartan con ese servicio de Microsoft. Si su organización ha implementado estos servicios en un país o región diferente, conectarse al servicio puede resultar en que sus datos crucen los límites de residencia de datos. Asegúrese de confirmar las políticas de su organización y los requisitos de cumplimiento del gobierno para la residencia de datos antes de usar estas características. 
> - Puede afectar los servicios que no son pruebas. Si su organización utiliza estos servicios en producción y no se evalúan junto con Business Central, otros usuarios de estos servicios que no participen en esta versión de prueba de [!INCLUDE[prod_short](includes/prod_short.md)] pueden ser afectados.
> - [!INCLUDE[prod_short](includes/prod_short.md)] también puede conectarse a servicios de Microsoft o servicios de terceros según las personalizaciones y extensiones que usted o su administrador hayan instalado en su [!INCLUDE[prod_short](includes/prod_short.md)] prueba. Para obtener información sobre cómo sus extensiones procesan sus datos, contacte con el desarrollador de la extensión o siga el enlace de privacidad para la extensión en AppSource.
> - Para funciones en vista previa, usted acepta los [términos de vista previa](https://powerplatform.microsoft.com/en-us/legaldocs/supp-powerplatform-preview/?wt.mc_id=power-virtual-agents_inproduct).

Su privacidad es importante para nosotros. Puede obtener información sobre cómo Microsoft procesa sus datos en la [Declaración de privacidad de Microsoft](https://go.microsoft.com/fwlink/?linkid=521839).

## [!INCLUDE[prod_short](includes/free_trial_md.md)]

[!INCLUDE[footer-include](includes/footer-banner.md)]
