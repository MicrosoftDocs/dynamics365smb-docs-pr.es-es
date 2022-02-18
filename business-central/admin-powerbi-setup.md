---
title: Habilitar la integración de Power BI con Business Central
description: Aprenda a configurar la conexión a Power BI. Con los informes de Power BI puede obtener información, inteligencia empresarial y KPI de los datos de Business Central.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Power BI, setup, analysis, reporting, financial report, business intelligence, KPI
ms.date: 04/01/2021
ms.author: jswymer
ms.openlocfilehash: c8f12e98196d8dd22ff63c73ffd3967cf256244c
ms.sourcegitcommit: 1508643075dafc25e9c52810a584b8df1d14b1dc
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 01/28/2022
ms.locfileid: "8049879"
---
# <a name="enabling-power-bi-integration-with-prod_short"></a>Habilitar la integración de Power BI con [!INCLUDE[prod_short](includes/prod_short.md)]

Este artículo describe cómo tener [!INCLUDE[prod_short](includes/prod_short.md)] listo para la integración con Power BI. [!INCLUDE[prod_short](includes/prod_short.md)] online ya está habilitado para la integración, aunque hay cierta información sobre las licencias que quizás desee leer. Para [!INCLUDE[prod_short](includes/prod_short.md)] local, habrá configurado su entorno para conectarse a Power BI antes de que los usuarios puedan trabajar con él.

## <a name="power-bi-licensing"></a><a name="license"></a>Licencias de Power BI

Con [!INCLUDE[prod_short](includes/prod_short.md)], los usuarios obtienen una licencia de Power BI que proporciona acceso a las funciones más comunes en [!INCLUDE[prod_short](includes/prod_short.md)] y Power BI. También puede comprar una licencia de Power BI Pro que brinda acceso a funciones adicionales. La siguiente tabla proporciona una descripción general de las funciones disponibles con cada licencia.

|Licencia Power|Ver informes|Crear informes|Compartir informes|Actualizar informes| Aplicaciones de [!INCLUDE[prod_short](includes/prod_short.md)]|
|-------------|--------||
|Power BI gratis|![una marca de verificación.](media/check.png)|![otra marca de verificación](media/check.png)|(limitado)|(limitado)||
|Power BI Pro|![otra marca de verificación más.](media/check.png)|![es una marca de verificación](media/check.png)|![otra nueva marca de verificación](media/check.png)|(extensivo)|![última marca de verificación](media/check.png)|

Para más información, ver [Licenciar el servicio de Power BI para los usuarios de su organización](/power-bi/admin/service-admin-licensing-organization) o [Registrarse para el servicio de Power BI como individuo](/power-bi/fundamentals/service-self-service-signup-for-power-bi).

## <a name="expose-data-through-api-pages-or-odata-web-services"></a><a name="exposedata"></a>Exponer datos a través de páginas API o servicios web OData

Business Central ofrece dos formas de exponer datos que pueden ser consumidos por informes de Power BI: páginas API y servicios web Open Data Protocol (OData).

### <a name="api-pages"></a>Páginas API

> **SE APLICA A:** Business Central online solo 

Una página API es un tipo de página específico creado en código AL que proporciona acceso a las tablas de la base de datos a través de un servicio REST compatible con webhook y habilitado para OData v4. Este tipo de página no se puede mostrar en la interfaz de usuario, pero está diseñado para crear servicios de integración confiables.

Business Central online está disponible con un conjunto de API integradas, que puede usar para obtener datos de las entidades comerciales más comunes, como clientes, artículos, pedidos de venta y más. No se requiere trabajo adicional o configuración para usar estas API como fuente de datos para informes de Power BI. Para obtener más información sobre estas API, consulte [API de Business Central V2.0](/dynamics365/business-central/dev-itpro/api-reference/v2.0/).

Business Central online también admite API personalizadas. Los desarrolladores de aplicaciones de las soluciones Business Central pueden crear sus propias páginas de API y empaquetarlas en extensiones. Luego puede instalar las extensiones en su suscriptor. Una vez instaladas, utilice las páginas de la API para sus informes de Power BI, como lo haría con las API integradas (v2.0). Para obtener más información sobre cómo crear páginas de API, consulte [Desarrollar una API personalizada](/dynamics365/business-central/dev-itpro/developer/devenv-develop-custom-api).

> [!IMPORTANT]
> A partir de febrero de 2022, los informes de Power BI para [!INCLUDE[prod_short](includes/prod_short.md)] en línea provienen de una réplica secundaria de la base de datos de solo lectura, por razones de rendimiento. Como consecuencia, los desarrolladores de AL deben evitar diseñar páginas de API que realicen modificaciones en la base de datos mientras las páginas se abren o cargan registros. En particular, considere el código en los desencadenadores AL: OnInit, OnOpenPage, OnFindRecord, OnNextRecord, OnAfterGetRecord y OnAfterGetCurrRecord. Estas modificaciones de la base de datos, en algunos casos, pueden causar problemas de rendimiento y evitar que el informe actualice los datos. Para más información, consulte [Artículos de rendimiento para desarrolladores](/dynamics365/business-central/dev-itpro/performance/performance-developer?branch=main#writing-efficient-web-services) en la ayuda para el desarrollo de Business Central.
>
> En casos excepcionales, el comportamiento provocará un error cuando un usuario intente obtener datos de la página API para un informe en Power BI Desktop. Sin embargo, si las modificaciones de la base de datos son necesarias en la página de la API personalizada, los usuarios de Power BI Desktop pueden forzar el comportamiento. Para más información, consulte [Creación de informes de Power BI para mostrar datos de Business Central](across-how-use-financials-data-source-powerbi.md#fixing-problems).

### <a name="odata-web-services"></a>Servicios web OData

Puede publicar objetos de aplicación de Business Central, como unidades de código, páginas y consultas, como [Servicios web OData](/dynamics365/business-central/dev-itpro/webservices/odata-web-services). Con Business Central online hay muchos servicios web publicados de forma predeterminada. Un modo de fácil de encontrar los servicios web es buscar *servicios web* en [!INCLUDE[prod_short](includes/prod_short.md)]. En la página de **Servicios web**, asegúrese de que el campo **Publicar** esté seleccionado para los servicios web enumerados más arriba. Para obtener más información sobre la publicación de servicios web, consulte [Publicar un servicio web](across-how-publish-web-service.md).

Para obtener más información sobre lo que puede hacer para garantizar el mejor rendimiento de los servicios web, como se ve desde Business Central Server (el punto final) y desde el consumidor (el cliente), lea [Escribir servicios web eficientes](/dynamics365/business-central/dev-itpro/performance/performance-developer#writing-efficient-web-services).

### <a name="choosing-whether-to-use-api-pages-or-odata-web-services"></a>Elegir si usar páginas API o servicios web OData

Siempre que sea posible, le recomendamos que utilice páginas API en lugar del servicio web OData. Las páginas API son generalmente más rápidas para cargar datos en informes de Power BI que los servicios web OData. Además, son más flexibles porque le permiten obtener datos de campos de tabla que no están definidos en un objeto de página.

## <a name="set-up-prod_short-on-premises-for-power-bi-integration"></a><a name="setup"></a>Preparación de [!INCLUDE[prod_short](includes/prod_short.md)] para la integración de Power BI

Esta sección explica los requisitos para una implementación de [!INCLUDE[prod_short](includes/prod_short.md)] local para integrarse con Power BI.

1. Configure NavUserPassword o Azure Active Directory Autenticación para la implementación.

    La integración de Power BI no es compatible con la autenticación de Windows.  

2. Habilite los servicios web OData y el punto final ODataV4.

    El servicio web OData debe estar habilitado en [!INCLUDE[server](includes/server.md)] y el puerto OData abierto en el firewall. Para obtener más información, consulte [Configuración de Business Central Server - OData Web Services](/dynamics365/business-central/dev-itpro/administration/configure-server-instance#ODataServices).

    El servidor local debe ser accesible desde Internet.

3. Proporcione a las cuentas de usuario de [!INCLUDE[prod_short](includes/prod_short.md)] una clave de acceso al servicio web.

    Se necesita una clave de acceso al servicio web únicamente para ver datos de [!INCLUDE[prod_short](includes/prod_short.md)] en Power BI. Puede asignar una clave de acceso al servicio web a cada cuenta de usuario. O en su lugar, cree una cuenta específica con una clave de acceso al servicio web para que la utilicen todos los usuarios. Para obtener más información, consulte [Autenticación de servicios web](/dynamics365/business-central/dev-itpro/webservices/web-services-authentication#generate-a-web-service-access-key).

    <!--
    > [!IMPORTANT]
    > With [!INCLUDE[prod_short](../developer/includes/prod_short.md)] online, the use of access keys (Basic Auth) for web service authentication is [deprecated](/dynamics365/business-central/dev-itpro/upgrade/deprecated-features-w1#accesskeys). We recommend that you use OAuth2 instead. For more information, see [Using OAuth to Authorize Business Central Web Services](/dynamics365/business-central/dev-itpro/webservices/authenticate-web-services-using-oauth).-->

4. Cree un registro de aplicación para [!INCLUDE[prod_short](includes/prod_short.md)] en Microsoft Azure.

    Para ver informes incrustados de Power BI en páginas de [!INCLUDE[prod_short](includes/prod_short.md)], se debe registrar una aplicación para [!INCLUDE[prod_short](includes/prod_short.md)] en Microsoft Azure, teniendo en cuenta que la aplicación registrada necesita permiso para servicios de Power BI. Para más información, vea [Registro de [!INCLUDE[prod_short](includes/prod_short.md)] local en Azure AD para la integración con otros servicios](/dynamics365/business-central/dev-itpro/administration/register-app-azure).

    > [!NOTE]
    > Si su implementación utiliza la autenticación NavUserPassword, [!INCLUDE[prod_short](includes/prod_short.md)] se conecta al mismo servicio de Power BI para todos los usuarios. Especificará esta cuenta de servicio como parte del registro de la aplicación. Con la autenticación de Azure AD, [!INCLUDE[prod_short](includes/prod_short.md)] se conecta al servicio de Power BI asociado con cuentas de usuario individuales.

    <!-- Windows authentication can also be used but you can't get data from BC in Power BI -->
5. Realice la conexión inicial desde Business Central a Power BI.

    Antes de que los usuarios finales puedan usar Power BI en [!INCLUDE[prod_short](includes/prod_short.md)], un administrador de la aplicación de Azure tendrá que dar su consentimiento al servicio de Power BI.

    Para realizar la conexión inicial, abra [!INCLUDE[prod_short](includes/prod_short.md)] y ejecute **Comenzar con Power BI** desde el centro de roles. Esta acción le guiará a través del proceso de consentimiento y verificará su licencia de Power BI. Cuando se le solicite, inicie sesión con una cuenta de administrador de Azure. Para obtener más información, consulte [Conectar a Power BI, solo una vez](across-working-with-powerbi.md#connect).


## <a name="see-related-training-at-microsoft-learn"></a>Consulte Formación relacionada en [Microsoft Learn](/learn/modules/Configure-powerbi-excel-dynamics-365-business-central/index)

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