---
title: Habilitar la integración de Power BI con Business Central
description: 'Aprenda a configurar la conexión a Power BI. Con los informes de Power BI puede obtener información, inteligencia empresarial y KPI de los datos de Business Central.'
author: jswymer
ms.topic: get-started
ms.search.keywords: 'Power BI, setup, analysis, reporting, financial report, business intelligence, KPI'
ms.date: 01/28/2024
ms.author: jswymer
ms.service: dynamics-365-business-central
ms.custom: bap-template
ms.reviewer: jswymer
---
# <a name="enabling-power-bi-integration-with-"></a>Habilitar la integración de Power BI con [!INCLUDE[prod_short](includes/prod_short.md)]

[!INCLUDE[azure-ad-to-microsoft-entra-id](~/../shared-content/shared/azure-ad-to-microsoft-entra-id.md)]

Este artículo describe cómo tener [!INCLUDE[prod_short](includes/prod_short.md)] listo para la integración con Power BI. [!INCLUDE[prod_short](includes/prod_short.md)] online ya está habilitado para la integración, aunque hay cierta información sobre las licencias que quizás desee leer. Para [!INCLUDE[prod_short](includes/prod_short.md)] local, habrá configurado su entorno para conectarse a Power BI antes de que los usuarios puedan trabajar con él.

## <a name="power-bi-licensing"></a><a name="license"></a>Licencias de Power BI

Con [!INCLUDE[prod_short](includes/prod_short.md)], los usuarios obtienen una licencia de Power BI que proporciona acceso a las funciones más comunes en [!INCLUDE[prod_short](includes/prod_short.md)] y Power BI. También puede comprar una licencia de Power BI Pro que brinda acceso a funciones adicionales. La siguiente tabla proporciona una descripción general de las funciones disponibles con cada licencia.

|Licencia Power|Ver informes|Crear informes|Compartir informes|Actualizar informes| Aplicaciones de [!INCLUDE[prod_short](includes/prod_short.md)]|
|-------------|--------||
|Power BI gratis|![una marca de verificación.](media/check.png)|![otra marca de verificación](media/check.png)|(limitado)|(limitado)||
|Power BI Pro|![otra marca de verificación más.](media/check.png)|![es una marca de verificación](media/check.png)|![otra nueva marca de verificación](media/check.png)|(extensivo)|![última marca de verificación](media/check.png)|

Para más información, ver [Licenciar el servicio de Power BI para los usuarios de su organización](/power-bi/admin/service-admin-licensing-organization) o [Registrarse para el servicio de Power BI como individuo](/power-bi/fundamentals/service-self-service-signup-for-power-bi).

## <a name="expose-data-through-api-or-odata-web-services"></a><a name="exposedata"></a>Exponer datos a través de API o servicios web OData

Business Central ofrece dos formas de exponer datos que pueden ser consumidos por informes de Power BI: páginas API o consultas y servicios web Open Data Protocol (OData).

### <a name="api-pages-and-queries"></a>Páginas API y consultas

> **SE APLICA A:** Business Central online solo

Los desarrolladores pueden definir objetos de página y objetos de consulta que son del tipo *API*. De esta manera, pueden exponer los datos de las tablas de la base de datos a través de un servicio REST compatible con webhook y habilitado para OData v4. Este tipo de datos no se puede mostrar en la interfaz de usuario, pero está diseñado para crear servicios de integración confiables.

Business Central online está disponible con un conjunto de API integradas, que puede usar para obtener datos de las entidades comerciales más comunes, como clientes, artículos, pedidos de venta y más. No se requiere trabajo adicional o configuración para usar estas API como fuente de datos para informes de Power BI. Para obtener más información sobre estas API, consulte [API de Business Central V2.0](/dynamics365/business-central/dev-itpro/api-reference/v2.0/).

Business Central online también admite API personalizadas. Los desarrolladores de aplicaciones de las soluciones Business Central pueden crear sus propias páginas de API y consultas, y empaquetarlas en aplicaciones. Luego puede instalar las aplicaciones en su suscriptor. Una vez instaladas, utilice las páginas de la API para sus informes de Power BI, como lo haría con las API integradas (v2.0). Para obtener más información sobre cómo crear páginas de API exponiendo páginas o consultas, consulte [Desarrollar una API personalizada](/dynamics365/business-central/dev-itpro/developer/devenv-develop-custom-api).

> [!IMPORTANT]
> A partir de febrero de 2022, los informes de Power BI para [!INCLUDE[prod_short](includes/prod_short.md)] en línea provienen de una réplica secundaria de la base de datos de solo lectura, por razones de rendimiento. Como consecuencia, los desarrolladores de AL deben evitar diseñar páginas de API que realicen modificaciones en la base de datos mientras las páginas se abren o cargan registros. En particular, considere el código en los desencadenadores AL: OnInit, OnOpenPage, OnFindRecord, OnNextRecord, OnAfterGetRecord y OnAfterGetCurrRecord. Estas modificaciones de la base de datos, en algunos casos, pueden causar problemas de rendimiento y evitar que el informe actualice los datos. Para más información, consulte [Artículos de rendimiento para desarrolladores](/dynamics365/business-central/dev-itpro/performance/performance-developer?branch=main#writing-efficient-web-services) en el contenido de desarrollo de Business Central.
>
> En casos excepcionales, el comportamiento provocará un error cuando un usuario intente obtener datos de la API para un informe en Power BI Desktop. Sin embargo, si las modificaciones de la base de datos son necesarias en la API personalizada, los usuarios de Power BI Desktop pueden forzar el comportamiento. Para más información, consulte [Creación de informes de Power BI para mostrar datos de Business Central](across-how-use-financials-data-source-powerbi.md#fixing-problems).

### <a name="odata-web-services"></a>Servicios web OData

Puede publicar objetos de aplicación de Business Central, como unidades de código, páginas y consultas, como [Servicios web OData](/dynamics365/business-central/dev-itpro/webservices/odata-web-services). Con Business Central online hay muchos servicios web publicados de forma predeterminada. Un modo de fácil de encontrar los servicios web es buscar *servicios web* en [!INCLUDE[prod_short](includes/prod_short.md)]. En la página de **Servicios web**, asegúrese de que el campo **Publicar** esté seleccionado para los servicios web enumerados más arriba. Para obtener más información sobre la publicación de servicios web, consulte [Publicar un servicio web](across-how-publish-web-service.md).

Para obtener más información sobre lo que puede hacer para garantizar el mejor rendimiento de los servicios web, como se ve desde Business Central Server (el punto final) y desde el consumidor (el cliente), lea [Escribir servicios web eficientes](/dynamics365/business-central/dev-itpro/performance/performance-developer#writing-efficient-web-services).

### <a name="choosing-whether-to-use-api-pages-or-odata-web-services"></a>Elegir si usar páginas API o servicios web OData

Siempre que sea posible, le recomendamos que utilice páginas API en lugar del servicio web OData. Las páginas API son más rápidas para cargar datos en informes de Power BI que los servicios web OData. Además, son más flexibles porque le permiten obtener datos de campos de tabla que no están definidos en un objeto de página.

<!--## <a name="setup"></a>Set up [!INCLUDE[prod_short](includes/prod_short.md)] on-premises for Power BI integration

This section explains the requirements for a [!INCLUDE[prod_short](includes/prod_short.md)] on-premises deployment to integrate with Power BI.

1. Configure either [NavUserPassword](/dynamics365/business-central/dev-itpro/administration/authenticating-users-with-navuserpassword) or [Microsoft Entra ID](/dynamics365/business-central/dev-itpro/administration/authenticating-users-with-azure-ad-overview) as the authentication method for the deployment.  
    
    > [!NOTE]
    > Power BI integration doesn't support Windows authentication and is not supported on Windows Client.

2. Enable OData web services and the ODataV4 endpoint.

    OData web service must be enabled on the [!INCLUDE[server](includes/server.md)], and OData port opened in firewall. For more information, see [Configuring Business Central Server - OData Web Services](/dynamics365/business-central/dev-itpro/administration/configure-server-instance#ODataServices).

    The local server must be accessible from the Internet.

3. Give [!INCLUDE[prod_short](includes/prod_short.md)] user accounts a web service access key.

    A web service access key is only needed to view [!INCLUDE[prod_short](includes/prod_short.md)] data in Power BI. You can assign a web service access key to each user account. Or instead, create a specific account with a web service access key for use by all users. For more information, see [Web Services Authentication](/dynamics365/business-central/dev-itpro/webservices/web-services-authentication#generate-a-web-service-access-key).

    <!--
    > [!IMPORTANT]
    > With [!INCLUDE[prod_short](../developer/includes/prod_short.md)] online, the use of access keys (Basic Auth) for web service authentication is [deprecated](/dynamics365/business-central/dev-itpro/upgrade/deprecated-features-w1#accesskeys). We recommend that you use OAuth2 instead. For more information, see [Use OAuth to Authorize Business Central Web Services](/dynamics365/business-central/dev-itpro/webservices/authenticate-web-services-using-oauth).-->

<!--4. Create an application registration for [!INCLUDE[prod_short](includes/prod_short.md)] in Microsoft Azure.

    To view Power BI reports embedded in [!INCLUDE[prod_short](includes/prod_short.md)] pages, an application must be registered for [!INCLUDE[prod_short](includes/prod_short.md)] in Microsoft Azure. The registered application needs permission to Power BI services. At a minimum, the app requires  **User.ReadWrite.All** permission. For users to view reports from shared Power BI workspaces, the app requires **Workspace.Read.All** permission. For more information, see [Registering [!INCLUDE[prod_short](includes/prod_short.md)] On-Premises in Microsoft Entra ID for Integrating with Other Services](/dynamics365/business-central/dev-itpro/administration/register-app-azure).

    > [!NOTE]
    > If your deployment uses NavUserPassword authentication, [!INCLUDE[prod_short](includes/prod_short.md)] connects to the same Power BI service for all users. You'll specify this service account as part of registering the application. With Microsoft Entra authentication, [!INCLUDE[prod_short](includes/prod_short.md)] connects to the Power BI service associated with the individual user accounts.

    <!-- Windows authentication can also be used but you can't get data from BC in Power BI -->
<!--5. Make the initial connection from Business Central to Power BI.

    Before end-users can use Power BI in [!INCLUDE[prod_short](includes/prod_short.md)], an Azure application administrator will have to give consent to the Power BI service.

    To make the initial connection, open [!INCLUDE[prod_short](includes/prod_short.md)], and run **Get Started with Power BI** from the Home page. This action will lead you through the consent process, and check your Power BI license. When prompted sign in using an Microsoft Entra admin account. For more information, see [Connect to Power BI - one time only](across-working-with-powerbi.md#connect).-->

## <a name="setting-up-dataflows"></a>Configuración de flujos de datos

Los flujos de datos le permiten ingerir, transformar y cargar datos en un espacio de trabajo de Power BI y luego utilizar los datos como base para sus informes. En algunos casos, estos flujos de datos pueden experimentar errores transitorios mientras realizan una actualización programada. El mensaje de error se ve así: `DataSource.Error: OData: Unable to read data from the transport connection: An existing connection was forcibly closed by the remote host.` 

Con PowerAutomate, puede configurar reintentos para esta situación. Para obtener más información, consulte [Reintentar automáticamente un flujo de datos en caso de error](/power-query/dataflows/automatically-retry-dataflow).

## <a name="see-also"></a>Consulte también

[Business Central y Power BI](admin-powerbi.md)  
[Componente de integración de Power BI e información general de la arquitectura para [!INCLUDE[prod_short](includes/prod_short.md)]](admin-powerbi-overview.md)  
[Power BI para consumidores](/power-bi/consumer/end-user-consumer)  
[El nuevo aspecto del servicio Power BI](/power-bi/service-new-look)  
[Inicio rápido: Conectarse a los datos de Power BI Desktop](/power-bi/desktop-quickstart-connect-to-data)  
[Documentación de Power BI](/power-bi/)  
[Inteligencia empresarial](bi.md)  
[Preparación para hacer negocios](ui-get-ready-business.md)  
[Importar datos de empresa de otros sistemas financieros](across-import-data-configuration-packages.md)  
[Configurar [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md)  
[Usar [!INCLUDE[prod_short](includes/prod_short.md)] como origen de datos de Power BI](across-how-use-financials-data-source-powerbi.md)  
[Usar [!INCLUDE[prod_short](includes/prod_short.md)] como origen de datos de Power Apps](across-how-use-financials-data-source-powerapps.md)  
[Usar [!INCLUDE[prod_short](includes/prod_short.md)] en Power Automate](across-how-use-financials-data-source-flow.md)  




[!INCLUDE[footer-include](includes/footer-banner.md)]
