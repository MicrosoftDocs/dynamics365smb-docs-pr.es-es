---
title: Creación de informes en Power BI Desktop para mostrar datos de Business Central
description: Haga que los datos estén disponibles como origen de datos en Power BI y generar informes eficaces del estado de la empresa.
author: jswymer
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'business intelligence, KPI, Odata, Power App, SOAP, analysis'
ms.date: 06/12/2024
ms.author: jswymer
ms.service: dynamics-365-business-central
ms.reviewer: jswymer
---

# <a name="building-power-bi-reports-to-display--data"></a>Crear informes de Power BI para mostrar datos de [!INCLUDE [prod_long](includes/prod_long.md)]

Puede hacer que los datos de [!INCLUDE[prod_long](includes/prod_long.md)] estén disponibles como origen de datos en Power BI Desktop y generar informes eficaces del estado de la empresa.

Este artículo describe cómo empezar a usar Power BI Desktop para crear informes que muestren datos de [!INCLUDE[prod_long](includes/prod_long.md)]. Después de crear informes, puede publicarlos en su servicio de Power BI o compartirlos con todos los usuarios de su organización. Una vez que estos informes estén en el servicio de Power BI, los usuarios que están configurados para él, pueden ver los informes en [!INCLUDE[prod_long](includes/prod_long.md)].

## <a name="get-ready"></a>Prepararse

- Regístrese para el servicio de Power BI.

  Si aún no se ha registrado, vaya a [https://powerbi.microsoft.com](https://powerbi.microsoft.com). Cuando se registre, use su dirección de correo electrónico y contraseña del trabajo.

- Descargue [Power BI Desktop](https://powerbi.microsoft.com/desktop/).

  Power BI Desktop es una aplicación gratuita que se instala en su computadora local. Para obtener más información, consulte [Inicio rápido: Conectarse a los datos de Power BI Desktop](/power-bi/desktop-quickstart-connect-to-data).

- Asegúrese de que los datos que desea en el informe están disponibles como página API o publicados como servicio web. Para más información, vea [Exponer datos a través de páginas API o servicios web OData](admin-powerbi-setup.md#exposedata).

<!--- For [!INCLUDE[prod_short](includes/prod_short.md)] on-premises, get the following information:

  - The OData URL for [!INCLUDE[prod_short](includes/prod_short.md)].
  
    Typically, this URL has the format `http[s]://[computer]:[port]/[serverinstance]/ODataV4`, for example, `https://localhost:7048/BC190/ODataV4`. If you have a multi-tenant deployment, include the tenant in the URL, for example, `https://localhost:7048/BC190/ODataV4?tenant=tenant1`.
  - A user name and web service access key of a [!INCLUDE[prod_short](includes/prod_short.md)] account.

    To get data from [!INCLUDE[prod_short](includes/prod_short.md)], Power BI uses basic authentication. So, you'll need a user name and web service access key to connect. The account might be your own user account, or your organization may have specific account for this purpose.-->

- Descargue el tema de informe [!INCLUDE [prod_short](includes/prod_short.md)] (opcional).

  Para obtener más información, consulte [Usar el tema de informe [!INCLUDE [prod_short](includes/prod_short.md)]](#theme) en este articulo.

[!INCLUDE[note-multicompany-reports](includes/note-multicompany-reports.md)]

## <a name="add--as-a-data-source-in-power-bi-desktop"></a><a name="getdata"></a>Agregar [!INCLUDE[prod_short](includes/prod_short.md)] como origen de datos de Power BI Desktop

La primera tarea al crear informes es agregar [!INCLUDE[prod_short](includes/prod_short.md)] como fuente de datos en Power BI Desktop. Una vez conectado, puede comenzar a generar el informe.

1. Inicie Power BI Desktop.
2. Seleccione  **Obtener datos**.

    Si no ve **Obtener datos**, seleccione el menú **Archivo** y luego **Obtener datos**.
3. En la página **Obtener datos**, seleccione **Servicios en línea**.
4. En el panel **Servicios en línea**, realice uno de los siguientes pasos:

    - Para conectarse a [!INCLUDE [prod_short](includes/prod_short.md)] en línea, seleccione **Dynamics 365 Business Central**, luego **Conectar**.
    <!--- To connect to  [!INCLUDE [prod_short](includes/prod_short.md)] on-premises, select **Dynamics 365 Business Central (on-premises)**, then **Connect**.-->

5. Inicie sesión en [!INCLUDE [prod_short](includes/prod_short.md)] (solo una vez).

    Si no ha iniciado sesión en [!INCLUDE [prod_short](includes/prod_short.md)] desde Power BI Desktop, se le pedirá que inicie sesión.

    - Para [!INCLUDE [prod_short](includes/prod_short.md)] online, seleccione **Iniciar sesión** y luego elija la cuenta pertinente. Use la misma cuenta con la que inicia sesión en [!INCLUDE [prod_short](includes/prod_short.md)]. Cuando termine, seleccione **Conectar**.

    <!--- For [!INCLUDE [prod_short](includes/prod_short.md)] on-premises, first enter the OData URL for [!INCLUDE[prod_short](includes/prod_short.md)], then select **OK**. When prompted, enter the user name and password of the account to use for connecting to [!INCLUDE[prod_short](includes/prod_short.md)]. In the **Password** box, enter the web service access key. When done, select **Connect**.-->

    > [!NOTE]  
    > Una vez que se haya conectado a [!INCLUDE[prod_short](includes/prod_short.md)], no se le volverá a solicitar que inicie sesión. [¿Cómo cambio o borro la cuenta que estoy usando actualmente para conectarme a Business Central desde Power BI Desktop?](/dynamics365/business-central/power-bi-faq?tabs=designer#perms)

6. Cuando está conectado, Power BI contacta con el servicio [!INCLUDE [prod_short](includes/prod_short.md)]. La ventana **Navegador** muestra los orígenes de datos que están disponibles para crear informes. Seleccione una carpeta para expandirla y mostrar los orígenes de datos disponibles.

   Estos orígenes de datos representan todos los servicios web y las páginas API que están publicados para [!INCLUDE [prod_short](includes/prod_short.md)], agrupados por entornos y empresas. Con [!INCLUDE [prod_short](includes/prod_short.md)] en línea, el **Navegador** tiene la siguiente estructura:

    - **Nombre de entorno**
      - **Nombre de la empresa**
        - **API avanzadas**

          Esta carpeta enumera las páginas API avanzadas publicadas por Microsoft, como las [API de automatización de Business Central](/dynamics365/business-central/dev-itpro/administration/itpro-introduction-to-automation-apis) y las [páginas API personalizadas para Business Central](/dynamics365/business-central/dev-itpro/developer/devenv-develop-custom-api). Las páginas de API personalizadas se agrupan además en carpetas por las propiedades [APIPublisher](/dynamics365/business-central/dev-itpro/developer/properties/devenv-apipublisher-property)/[APIGroup](/dynamics365/business-central/dev-itpro/developer/properties/devenv-apigroup-property) del código de la página API.

        - **API estándar v2.0**

          Esta carpeta enumera las páginas API expuestas por la [API de Business Central V2.0](/dynamics365/business-central/dev-itpro/api-reference/v2.0/).

        - **Servicios web \(heredado)**

          Esta carpeta enumera las páginas, unidades de código y consultas que se publican como servicios web en Business Central.

    <!--
    > [!NOTE]
    > The structure for Business Central on-premises is different because it doesn't support API pages.-->

7. Seleccione el origen o los orígenes de datos que desea agregar al modelo de datos y después seleccione el botón **Cargar**.
8. Si más adelante desea agregar más datos de Business Central, puede repetir los pasos anteriores.

Una vez que los datos se hayan cargado, puede verlos en el panel de navegación derecho en la página. Ya se ha conectado con los datos de [!INCLUDE[prod_short](includes/prod_short.md)] y puede comenzar a crear su informe de Power BI.  

> [!TIP]
> Para obtener más información sobre el uso de Power BI Desktop, vea [Introducción a Power BI Desktop](/power-bi/fundamentals/desktop-getting-started).

## <a name="creating-accessible-reports"></a>Crear informes accesibles

Es importante que sus informes puedan ser utilizados por tantas personas como sea posible. Intente diseñar informes para que no requieran ninguna adaptación especial para satisfacer las necesidades específicas de diferentes usuarios. Asegúrese de que el diseño permita a los usuarios aprovechar las tecnologías de asistencia estándar, como los lectores de pantalla. Power BI incluye varias funciones, herramientas y pautas de accesibilidad para ayudarle a lograr este objetivo. Para más información, [Diseñar informes de Power BI para accesibilidad](/power-bi/create-reports/desktop-accessibility-creating-reports) en la documentación de Power BI.

## <a name="creating-reports-to-display-data-associated-with-a-list"></a>Crear informes para mostrar datos asociados con una lista

Puede crear informes que se muestren en un cuadro informativo de una página de lista [!INCLUDE [prod_short](includes/prod_short.md)]. Los informes pueden contener datos sobre el registro seleccionado en la lista. La creación de estos informes es similar a otros informes, excepto que hay algunas cosas que debe hacer para asegurarse de que los informes se muestren como se espera. Para más información, ver [Crear informes de Power BI para mostrar datos de lista en [!INCLUDE[prod_short](includes/prod_short.md)]](across-how-use-powerbi-reports-factbox.md).

## <a name="using-the--report-theme-optional"></a><a name="theme"></a>Usar el tema de informe [!INCLUDE [prod_short](includes/prod_short.md)] (optional)

Antes de elaborar el informe, le recomendamos que descargue e importe el archivo de tema de Microsoft [!INCLUDE [prod_short](includes/prod_short.md)]. El archivo de tema crea una paleta de colores de forma que pueda crear informes con el mismo estilo de color que las aplicaciones de [!INCLUDE [prod_short](includes/prod_short.md)] sin pedirle que defina colores personalizados para cada elemento visual.

> [!NOTE]
> Esta tarea es opcional. Siempre puede crear sus informes y luego descargar y aplicar la plantilla de estilo más tarde.

### <a name="download-the-theme"></a>Descargar el tema

El archivo de tema está disponible como archivo json en la Galería de temas comunitarios de Microsoft Power BI. Para descargar el archivo de tema, siga los siguientes pasos:

1. Ir a la[Galería de temas comunitarios de Microsoft Power BI para Microsoft Dynamics 365 Business Central](https://community.powerbi.com/t5/Themes-Gallery/Microsoft-Dynamics-365-Business-Central/m-p/385875).
2. Seleccione el archivo adjunto de descarga **Microsoft Dynamics Business Central.json**.

### <a name="import-the-theme-on-a-report"></a>Importar el tema en un informe

Después de descargar el tema de informe [!INCLUDE [prod_short](includes/prod_short.md)], puede importarlo a sus informes. Para importar el tema, seleccione **Ver** > **Temas** > **Buscar temas**. Para más información, ver [Power BI Desktop - Importar temas de informes personalizados](/power-bi/create-reports/desktop-report-themes#import-custom-report-theme-files).

## <a name="publish-reports"></a>Publicar informes

Una vez que haya creado o modificado un informe, puede publicarlo en su servicio de Power BI y también compartirlo con otros miembros de su organización. Después de publicar un informe, estará disponible en Power BI. El informe también está disponible para su selección en [!INCLUDE[prod_short](includes/prod_short.md)].

Para publicar un informe, seleccione **Publicar** en la pestaña **Inicio** de la cinta o del menú **Archivo**. Si ha iniciado sesión en el servicio Power BI, el informe se publica en este servicio. De lo contrario, se le pedirá que inicie sesión. 

## <a name="distribute-or-share-a-report"></a>Distribuir o compartir un informe

Hay dos formas de enviar informes a sus compañeros de trabajo y a otras personas:

- Distribuya informes como archivos .pbix.

    Los informes se almacenan en su computadora como archivos .pbix. Puede distribuir el archivo .pbix del informe a los usuarios, como cualquier otro archivo. Luego, los usuarios pueden cargar el archivo en su servicio de Power BI. Ver [Cargar informes desde archivos](across-working-with-powerbi.md#upload).

    > [!NOTE]
    > La distribución de informes de esta manera significa que la actualización de los datos de los informes la realizará cada usuario de forma individual. Esta situación podría impactar el rendimiento de [!INCLUDE[prod_short](includes/prod_short.md)].

- Compartir el informe del servicio de Power BI

    Si tiene una licencia de Power BI Pro, puede compartir el informe con otros, directamente desde su servicio de Power BI. Para más información, ver [Power BI - Compartir un panel o informe](/power-bi/collaborate-share/service-share-dashboards#share-a-dashboard-or-report).

## <a name="how-to-develop-cross-company-or-cross-environment-power-bi-reports"></a>Cómo desarrollar informes de Power BI entre empresas o entornos

Los puntos de conexión de API de [!INCLUDE[prod_short](includes/prod_short.md)] tienen el prefijo `https://api.businesscentral.dynamics.com/v2.0/<environment_name>/api/v2.0` seguido por `/companies({company_id})/accounts({id})` (aquí usamos la API `accounts` como ilustración). Puede utilizar esta estructura para crear consultas de PowerQuery que carguen datos para múltiples empresas o múltiples entornos si el usuario que está leyendo los datos puede tener acceso a ellos.

Para configurar una consulta para cargar datos para varias empresas, siga estos pasos:

1. Realice la consulta de PowerQuery que carga datos para una sola empresa. Conviértala en una función de Power Query personalizada que toma el ID de la empresa (o tal vez el nombre del entorno) como parámetros. Para obtener más información, vaya a [Usar funciones de Power Query personalizadas](/power-query/custom-function).
1. Ahora use la nueva función personalizada en una consulta de PowerQuery, donde asigna la función a una lista de empresas y luego combina los conjuntos de datos usando la función [Table.Combine](/powerquery-m/table-combine) Power Query.

## <a name="fixing-problems"></a>Solucionar problemas

### <a name="cant-insert-a-record-current-connection-intent-is-read-only-error-connecting-to-custom-api-page"></a>"No se puede insertar un registro. La intención de conexión actual es de solo lectura". error al conectarse a página API personalizada

> **SE APLICA A:** Business Central online

A partir de febrero de 2022, los nuevos informes que utilicen datos [!INCLUDE [prod_short](includes/prod_short.md)] se conectarán de manera predeterminada a una réplica de solo lectura de la base de datos [!INCLUDE [prod_short](includes/prod_short.md)]. En casos excepcionales, según el diseño de la página, podría obtener un error cuando intente conectarse y obtener datos de la página.

1. Inicie Power BI Desktop.
2. En la cinta, seleccione **Obtener datos** > **Servicios en línea**.
3. En el panel **Servicios en línea**, seleccione **Dynamics 365 Business Central** y luego **Conectar**.
4. En la ventana **Navegador**, seleccione el punto de conexión de la API desde el que desea cargar los datos.
5. El panel de vista previa muestra el siguiente error:

   *Dynamics365BusinessCentral: Error con la solicitud: El servidor remoto devolvió un error: (400) Solicitud errónea. (No es posible insertar un registro. La intención de la conexión es de Solo lectura. CorrelationId: [...])".*

6. Seleccione **Transformar datos** en vez de **Carga**, como lo haría normalmente.
7. En **Editor de Power Query**, seleccione **Editor avanzado** en la cinta.
8. En la línea que comienza por **Fuente =**, reemplace el siguiente texto:

   ```
   Dynamics365BusinessCentral.ApiContentsWithOptions(null, null, null, null)
   ```

   por:

   ```
   Dynamics365BusinessCentral.ApiContentsWithOptions(null, null, null, [UseReadOnlyReplica = false])
   ```

9. Seleccione **Listo**.
10. Seleccione **Cerrar y aplicar** en la cinta para guardar los cambios y cerrar Editor de Power Query.

## <a name="see-also"></a>Consulte también

[Habilitar los datos de negocio para Power BI](admin-powerbi-setup.md)  
[Inteligencia empresarial](bi.md)  
[Preparación para hacer negocios](ui-get-ready-business.md)  
[Importar datos de empresa de otros sistemas financieros](across-import-data-configuration-packages.md)  
[Configurar [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md)  
[Finanzas](finance.md)  
[Inicio rápido: Conectarse a los datos de Power BI Desktop](/power-bi/desktop-quickstart-connect-to-data)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
