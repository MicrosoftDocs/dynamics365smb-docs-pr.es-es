---
title: Cómo conectarse a Power BI desde Business Central local | Documentos de Microsoft
description: 'Obtener información, inteligencia empresarial y KPI de los datos de Business Central utilizando Power BI.'
author: jswymer
ms.topic: get-started
ms.devlang: al
ms.search.keywords: 'account schedule, analysis, reporting, financial report, business intelligence, KPI'
ms.date: 01/22/2024
ms.author: jswymer
ms.service: dynamics-365-business-central
---
# Conectarse a Power BI desde Business Central local

<!--In this article, you learn some of the basics about working with reports and dashboards in Power BI that use [!INCLUDE [prod_short](includes/prod_short.md)] as a data source. The article discusses some aspects that will help you get started as a [!INCLUDE[prod_short](includes/prod_short.md)] user. For general guidelines and instructions about using Power BI, see [Power BI documentation for consumers](/power-bi/consumer).

## Get ready

Sign up for the Power BI service. If you haven't already signed up, go to [https://powerbi.microsoft.com](https://powerbi.microsoft.com). When you sign up, use a work email address and password.-->

## Introducción

Para usar [!INCLUDE [prod_short](includes/prod_short.md)] local, debe estar habilitado para la integración en Power BI. Esta tarea normalmente la realiza un administrador. Para obtener más información sobre cómo habilitar la integración de Power BI con Business Central Online, consulte [Configurar Business Central local para la integración de Power BI](admin-powerbi-setup.md).

Algunas funciones solo están disponibles con Business Central online, no local. Para obtener más información, consulte [Introducción a Business Central y Power BI](admin-powerbi.md#what-you-can-do-with-power-bi-and-business-central)

## <a name="setup"></a>Preparación de [!INCLUDE[prod_short](includes/prod_short.md)] para la integración de Power BI

Esta sección explica los requisitos para una implementación de [!INCLUDE[prod_short](includes/prod_short.md)] local para integrarse con Power BI.

1. Configure [NavUserPassword](/dynamics365/business-central/dev-itpro/administration/authenticating-users-with-navuserpassword) o [Microsoft Entra ID](/dynamics365/business-central/dev-itpro/administration/authenticating-users-with-azure-ad-overview) como el método de autenticación para la implementación.  
    
    > [!NOTE]
    > La integración de Power BI no es compatible con la autenticación de Windows y no es compatible con Windows Client.

2. Habilite los servicios web OData y el punto final ODataV4.

    El servicio web OData debe estar habilitado en [!INCLUDE[server](includes/server.md)] y el puerto OData abierto en el firewall. Para obtener más información, consulte [Configuración de Business Central Server - OData Web Services](/dynamics365/business-central/dev-itpro/administration/configure-server-instance#ODataServices).

    El servidor local debe ser accesible desde Internet.

3. Proporcione a las cuentas de usuario de [!INCLUDE[prod_short](includes/prod_short.md)] una clave de acceso al servicio web.

    Se necesita una clave de acceso al servicio web únicamente para ver datos de [!INCLUDE[prod_short](includes/prod_short.md)] en Power BI. Puede asignar una clave de acceso al servicio web a cada cuenta de usuario. O en su lugar, cree una cuenta específica con una clave de acceso al servicio web para que la utilicen todos los usuarios. Para obtener más información, consulte [Autenticación de servicios web](/dynamics365/business-central/dev-itpro/webservices/web-services-authentication#generate-a-web-service-access-key).

4. Cree un registro de aplicación para [!INCLUDE[prod_short](includes/prod_short.md)] en Microsoft Azure.

    Para ver informes incrustados de Power BI en páginas de [!INCLUDE[prod_short](includes/prod_short.md)], se debe registrar una solicitud para [!INCLUDE[prod_short](includes/prod_short.md)] en Microsoft Azure. La aplicación registrada necesita permiso para servicios de Power BI. Como mínimo, la aplicación requiere el permiso **Usuario.ReadWrite.All**. Para que los usuarios vean informes de compartidos de espacios de trabajo Power BI, la aplicación necesita el permiso **Workspace.Read.All**. Para más información, vea [Registro de [!INCLUDE[prod_short](includes/prod_short.md)] local en Microsoft Entra ID para la integración con otros servicios](/dynamics365/business-central/dev-itpro/administration/register-app-azure).

    > [!NOTE]
    > Si su implementación utiliza la autenticación NavUserPassword, [!INCLUDE[prod_short](includes/prod_short.md)] se conecta al mismo servicio de Power BI para todos los usuarios. Especificará esta cuenta de servicio como parte del registro de la aplicación. Con la autenticación de Microsoft Entra, [!INCLUDE[prod_short](includes/prod_short.md)] se conecta al servicio de Power BI asociado con cuentas de usuario individuales.

    <!-- Windows authentication can also be used but you can't get data from BC in Power BI -->
5. Realice la conexión inicial desde Business Central a Power BI.

    Antes de que los usuarios finales puedan usar Power BI en [!INCLUDE[prod_short](includes/prod_short.md)], un administrador de la aplicación de Azure tendrá que dar su consentimiento al servicio de Power BI.

    Para realizar la conexión inicial, abra [!INCLUDE[prod_short](includes/prod_short.md)] y ejecute **Comenzar con Power BI** desde la página principal. Esta acción le guiará a través del proceso de consentimiento y verificará su licencia de Power BI. Cuando se le solicite, inicie sesión con una cuenta de administrador de Microsoft Entra. Para obtener más información, consulte [Conectar a Power BI, solo una vez](across-working-with-powerbi.md#connect).

## Crear informes de Power BI para mostrar datos de [!INCLUDE [prod_long](includes/prod_long.md)]

Puede hacer que los datos de Dynamics 365 Business Central estén disponibles como origen de datos en Power BI Desktop y generar informes eficaces del estado de la empresa.

Usar Power BI Desktop para crear informes para mostrar datos de Dynamics 365 Business Central. Después de crear informes, puede publicarlos en su servicio de Power BI o compartirlos con todos los usuarios de su organización. Una vez que estos informes estén en el servicio de Power BI, los usuarios que están configurados para él, pueden ver los informes en Dynamics 365 Business Central.

- Para [!INCLUDE[prod_short](includes/prod_short.md)] local, obtenga la siguiente información:

  - La URL de OData para [!INCLUDE[prod_short](includes/prod_short.md)].
  
    Normalmente, esta URL tiene el formato `http[s]://[computer]:[port]/[serverinstance]/ODataV4`, por ejemplo, `https://localhost:7048/BC190/ODataV4`. Si tiene una implementación de múltiples inquilinos, incluya al inquilino en la URL, por ejemplo, `https://localhost:7048/BC190/ODataV4?tenant=tenant1`.
  - Un nombre de usuario y una clave de acceso al servicio web de una cuenta de [!INCLUDE[prod_short](includes/prod_short.md)].

    Para obtener datos de [!INCLUDE[prod_short](includes/prod_short.md)], Power BI utiliza autenticación básica. Por lo tanto, necesitará un nombre de usuario y una clave de acceso al servicio web para conectarse. La cuenta puede ser su propia cuenta de usuario o su organización puede tener una cuenta específica para este propósito.

## <a name="getdata"></a>Agregar [!INCLUDE[prod_short](includes/prod_short.md)] como origen de datos de Power BI Desktop

La primera tarea al crear informes es agregar [!INCLUDE[prod_short](includes/prod_short.md)] como fuente de datos en Power BI Desktop. Una vez conectado, puede comenzar a generar el informe.

1. Inicie Power BI Desktop.
2. Seleccione  **Obtener datos**.

    Si no ve **Obtener datos**, seleccione el menú **Archivo** y luego **Obtener datos**.
3. En la página **Obtener datos**, seleccione **Servicios en línea**.
4. En el panel **Servicios en línea**, conéctese a [!INCLUDE [prod_short](includes/prod_short.md)] local, seleccione **Dynamics 365 Business Central (local)** y, después, **Conectar**.
5. Inicie sesión en [!INCLUDE [prod_short](includes/prod_short.md)] (solo una vez).

    Si no ha iniciado sesión antes en [!INCLUDE [prod_short](includes/prod_short.md)] desde Power BI Desktop, se le pedirá que inicie sesión.

   - Para [!INCLUDE [prod_short](includes/prod_short.md)] local, primero ingrese la dirección URL de OData para [!INCLUDE[prod_short](includes/prod_short.md)] y luego seleccione **Aceptar**. Cuando se le solicite, ingrese el nombre de usuario y la contraseña de la cuenta que se usará para conectarse a [!INCLUDE[prod_short](includes/prod_short.md)]. En **Contraseña**, ingrese la clave de acceso al servicio web. Cuando termine, seleccione **Conectar**.
   
    > [!NOTE]  
    > Una vez que se haya conectado correctamente a [!INCLUDE[prod_short](includes/prod_short.md)], no se le volverá a solicitar que inicie sesión. [¿Cómo cambio o borro la cuenta que estoy usando actualmente para conectarme a Business Central desde Power BI Desktop?](/dynamics365/business-central/power-bi-faq?tabs=designer#perms)

6. Una vez conectado, Power BI se pone en contacto con el servicio Business Central. Aparecen las ventanas **Navegador** y se muestran los orígenes de datos disponibles para generar informes. Seleccione una carpeta para expandirla y ver los orígenes de datos disponibles. 

   Estos orígenes de datos representan todos los servicios web y las páginas API que están publicados para [!INCLUDE [prod_short](includes/prod_short.md)]. Los orígenes de datos están agrupadas por entornos y empresas de Business Central.

   > [!NOTE]
    > La estructura de Business Central local es diferente porque no admite páginas API.

7. Seleccione el origen o los orígenes de datos que desea agregar al modelo de datos y después seleccione el botón **Cargar**.
8. Si más adelante desea agregar más datos de Business Central, puede repetir los pasos anteriores.

Una vez que los datos se hayan cargado, puede verlos en el panel de navegación derecho en la página. Ya se ha conectado correctamente con los datos de [!INCLUDE[prod_short](includes/prod_short.md)] y puede comenzar a crear su informe de Power BI.  

> [!TIP]
> Para obtener más información sobre el uso de Power BI Desktop, vea [Introducción a Power BI Desktop](/power-bi/fundamentals/desktop-getting-started).

## Gestionar y modificar informes

> [!NOTE]
> No puede administrar y modificar informes. 

## Cargar informes

Para [!INCLUDE [prod_short](includes/prod_short.md)] local, no hay informes de demostración disponibles, por lo que tendrá que comenzar desde cero usando Power BI Desktop. Como alternativa, los informes de Power BI se pueden distribuir como archivos que puede cargar directamente desde el servicio en línea de Power BI. Para más información, ver [Sube el informe al servicio](/power-bi/paginated-reports/paginated-reports-quickstart-aw#upload-the-report-to-the-service).

<!--
> [!NOTE]
> Uploading a report requires that you have SUPER user permissions in [!INCLUDE[prod_short](includes/prod_short.md)]. Also, you can't upload reports with [!INCLUDE [prod_short](includes/prod_short.md)] on-premises. With on-premises, you upload reports directly to your Power BI workspace. For more information, see [Connect to Power BI from [!INCLUDE [prod_short](includes/prod_short.md)] on-premises](across-working-with-business-central-in-powerbi.md).

<!--Once you have a Power BI account, you can sign in at [https://powerbi.microsoft.com/](https://powerbi.microsoft.com/).

The Power BI service hosts all the reports available to you. To see the report, select **My Workspace** > **Reports**. Then just select the report that you want to view.

With [!INCLUDE[prod_short](includes/prod_short.md)] online, you'll automatically have a set of default reports on your workspace. If you want to create your own reports, you can use Power BI Desktop to create reports, and then publish them to your workspace. For more information, see [Getting Started Building Reports in Power BI Desktop to Display [!INCLUDE [prod_long](includes/prod_long.md)] Data](across-how-use-financials-data-source-powerbi.md).

[!INCLUDE[note-multicompany-reports](includes/note-multicompany-reports.md)]

If you're using [!INCLUDE[prod_short](includes/prod_short.md)] on-premises, you'll have to start from scratch by using Power BI Desktop. Optionally, Power BI reports can be distributed as files, that you can upload.

<!--## Get the latest data

Each Power BI report is based on a dataset that gets data from the [!INCLUDE[prod_short](includes/prod_short.md)] sources. You want to make sure that the data in your Power BI reports is up to date with the data in [!INCLUDE[prod_short](includes/prod_short.md)]. This concept is referred to as *refreshing*.  Depending on how your organization has set up Power BI, refreshing might not happen automatically. There are two ways to refresh data: manually or by scheduling a refresh. Manual refreshing is done on-demand, as needed. Scheduled refreshing lets you refresh automatically at defined time intervals.

### Refresh manually

In the navigation pane, under **Datasets**, select **More options (...)** next to the dataset, then select **Refresh now**.

### Schedule a refresh

In the navigation pane, under Datasets, select More options (...) next to the dataset, then select **Schedule refresh**. Fill in the information under the **Schedule refresh** section, and select **Apply**.

For more information, see [Configure scheduled refresh](/power-bi/connect-data/refresh-scheduled-refresh)-->

<!--## <a name="upload"></a>Upload reports from files

Power BI Reports can be distributed among users as .pbix files. If you have a .pbix file, you can upload the file to a workspace. To upload a report, do the following steps:

1. In your new workspace, select **Get Data**.

2. In the Files box, select **Get**.

3. Select **Local File**, navigate to where you saved the file, and select **Open**.

For more information, see [Upload the report to the service](/power-bi/paginated-reports/paginated-reports-quickstart-aw#upload-the-report-to-the-service).

> [!NOTE]
> Uploading a report requires that you have a [Premium capacity](/power-bi/service-premium-what-is) work space. For more information, see [Managing Premium capacities](/power-bi/admin/service-premium-capacity-manage). 

> [!TIP]
> If you're using [!INCLUDE[prod_short](includes/prod_short.md)] online, you can also upload a report from within [!INCLUDE[prod_short](includes/prod_short.md)]. For more information, see [Work with Power BI Reports in [!INCLUDE [prod_short](includes/prod_short.md)] - Upload Reports](across-working-with-powerbi.md#upload).

## <a name="share"></a>Share reports with others

Once a report is in your workspace, you can share it with others in your organization.

To share a report, in a list reports, or in an open report, select **Share**. In the **Share report** pane, enter the full email addresses for individuals or distribution groups you want to share with. Follow the instructions on screen to complete the sharing. For more information, see [Share a dashboard or report](/power-bi/collaborate-share/service-share-dashboards#share-a-dashboard-or-report).

> [!NOTE]
> You must have  [Power BI Pro license](/power-bi/service-features-license-type), and the people you share with do too. The content must be in a workspace in a [Premium capacity](/power-bi/service-premium-what-is). For more information, see [Ways to share your work in Power BI](/power-bi/service-how-to-collaborate-distribute-dashboards-reports).-->

## Consulte también

[Business Central y Power BI](admin-powerbi.md)  
[Cargar informe desde archivos](across-working-with-powerbi.md#upload-reports)  
 
[!INCLUDE[footer-include](includes/footer-banner.md)]
