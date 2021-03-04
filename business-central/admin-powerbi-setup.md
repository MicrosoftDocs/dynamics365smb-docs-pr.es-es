---
title: Habilitar la integración de Power BI con Business Central
description: Aprenda a configurar la conexión a Power BI para que pueda obtener información, inteligencia empresarial y KPI de sus datos de Business Central con las aplicaciones de Business Central para Power BI.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: account schedule, analysis, reporting, financial report, business intelligence, KPI
ms.date: 10/01/2020
ms.author: jswymer
ms.openlocfilehash: dd0974c20f8c038fcc0cac27c9ef165b2aadcd36
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "4752505"
---
# <a name="enabling-power-bi-integration-with-prod_short"></a>Habilitar la integración de Power BI con [!INCLUDE[prod_short](includes/prod_short.md)]

Este artículo describe cómo tener [!INCLUDE[prod_short](includes/prod_short.md)] listo para la integración con Power BI. [!INCLUDE[prod_short](includes/prod_short.md)] online ya está habilitado para la integración, aunque hay cierta información sobre las licencias que quizás desee leer. Para [!INCLUDE[prod_short](includes/prod_short.md)] local, habrá configurado su entorno para conectarse a Power BI antes de que los usuarios puedan trabajar con él.

## <a name="power-bi-licensing"></a><a name="license"></a>Licencias de Power BI

Con [!INCLUDE[prod_short](includes/prod_short.md)], los usuarios obtienen una licencia de Power BI que proporciona acceso a las funciones más comunes en [!INCLUDE[prod_short](includes/prod_short.md)] y Power BI. También puede comprar una licencia de Power BI Pro que brinda acceso a funciones adicionales. La siguiente tabla proporciona una descripción general de las funciones disponibles con cada licencia.

|Licencia Power|Ver informes|Crear informes|Compartir informes|Actualizar informes| Aplicaciones de [!INCLUDE[prod_short](includes/prod_short.md)]|
|-------------|--------||
|Power BI gratis|![una marca de verificación](media/check.png)|![otra marca de verificación](media/check.png)|(limitado)|(limitado)||
|Power BI Pro|![otra marca de verificación más](media/check.png)|![es una marca de verificación](media/check.png)|![otra nueva marca de verificación](media/check.png)|(extensivo)|![última marca de verificación](media/check.png)|

Para más información, ver [Licenciar el servicio de Power BI para los usuarios de su organización](/power-bi/admin/service-admin-licensing-organization) o [Registrarse para el servicio de Power BI como individuo](/power-bi/fundamentals/service-self-service-signup-for-power-bi).

## <a name="set-up-prod_short-on-premises-for-power-bi-integration"></a><a name="setup"></a>Preparación de [!INCLUDE[prod_short](includes/prod_short.md)] para la integración de Power BI

Esta sección explica los requisitos para una implementación de [!INCLUDE[prod_short](includes/prod_short.md)] local para integrarse con Power BI.

1. Los servicios web OData y el punto final ODataV4 están habilitados.

    El servicio web OData debe estar habilitado en [!INCLUDE[server](includes/server.md)] y el puerto OData abierto en el firewall. Para obtener más información, consulte [Configuración de Business Central Server - OData Web Services](/dynamics365/business-central/dev-itpro/administration/configure-server-instance#ODataServices).
    
    El servidor local debe ser accesible desde Internet.

2. Las cuentas de usuario de [!INCLUDE[prod_short](includes/prod_short.md)] tienen una clave de acceso al servicio web.

    Se necesita una clave de acceso al servicio web para ver datos de [!INCLUDE[prod_short](includes/prod_short.md)] en Power BI. Puede asignar una clave de acceso al servicio web a cada cuenta de usuario. O en su lugar, cree una cuenta específica con una clave de acceso al servicio web para que la utilicen todos los usuarios. Para obtener más información, consulte [Autenticación de servicios web](/dynamics365/business-central/dev-itpro/webservices/web-services-authentication#generate-a-web-service-access-key).

3. La autenticación de NavUserPassword Azure Active Directory está configurada.

4. Para ver informes incrustados de Power BI en páginas de [!INCLUDE[prod_short](includes/prod_short.md)], se debe registrar una solicitud para [!INCLUDE[prod_short](includes/prod_short.md)] en Microsoft Azure.

    La aplicación registrada necesita permiso para servicios de Power BI. Para más información, vea [Registro de [!INCLUDE[prod_short](includes/prod_short.md)] local en Azure AD para la integración con otros servicios](/dynamics365/business-central/dev-itpro/administration/register-app-azure).

    > [!NOTE]
    > Si su implementación utiliza la autenticación NavUserPassword, [!INCLUDE[prod_short](includes/prod_short.md)] se conecta al mismo servicio de Power BI para todos los usuarios. Especificará esta cuenta de servicio como parte del registro de la aplicación. Con la autenticación de Azure AD, [!INCLUDE[prod_short](includes/prod_short.md)] se conecta al servicio de Power BI asociado con cuentas de usuario individuales.

    <!-- Windows authentication can also be used but you can't get data from BC in Power BI -->

## <a name="publish-data-as-web-services"></a>Publicar datos como servicios web

Las unidades de código, páginas y consultas que desea utilizar como fuente de datos en informes de Power BI deben publicarse como servicios web. Hay muchos servicios web publicados de forma predeterminada. Un modo de fácil de encontrar los servicios web es buscar *servicios web* en [!INCLUDE[prod_short](includes/prod_short.md)]. En la página de **Servicios web**, asegúrese de que el campo **Publicar** esté seleccionado para los servicios web enumerados más arriba. Esta tarea normalmente es administrativa.

Para obtener más información sobre la publicación de servicios web, consulte [Publicar un servicio web](across-how-publish-web-service.md).

> [!TIP]
> Para obtener más información sobre lo que puede hacer para garantizar el mejor rendimiento de los servicios web, como se ve desde Business Central Server (el punto final) y desde el consumidor (el cliente), lea [Escribir servicios web eficientes](/dynamics365/business-central/dev-itpro/performance/performance-developer#writing-efficient-web-services).




## <a name="see-related-training-at-microsoft-learn"></a>Consulte Formación relacionada en [Microsoft Learn](/learn/modules/Configure-powerbi-excel-dynamics-365-business-central/index)

## <a name="see-also"></a>Consulte también

[Business Central y Power BI](admin-powerbi.md)  
[Componente de integración de Power BI e información general de la arquitectura para [!INCLUDE[prod_short](includes/prod_short.md)]](admin-powerbi-overview.md)  
[Power BI para consumidores](/power-bi/consumer/end-user-consumer)  
[El nuevo aspecto del servicio Power BI](/power-bi/service-new-look)  
[Inicio rápido: Conectarse a los datos de Power BI Desktop](/power-bi/desktop-quickstart-connect-to-data)  
[Documentación de Power BI](/power-bi/)  
[Inteligencia empresarial](bi.md)  
[Introducción](product-get-started.md)  
[Importar datos de empresa de otros sistemas financieros](across-import-data-configuration-packages.md)  
[Configurar [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md)  
[Usar [!INCLUDE[prod_short](includes/prod_short.md)] como origen de datos de Power BI](across-how-use-financials-data-source-powerbi.md)  
[Usar [!INCLUDE[prod_short](includes/prod_short.md)] como origen de datos de Power Apps](across-how-use-financials-data-source-powerapps.md)  
[Usar [!INCLUDE[prod_short](includes/prod_short.md)] en Power Automate](across-how-use-financials-data-source-flow.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  


[!INCLUDE[footer-include](includes/footer-banner.md)]