---
title: Creación de informes en Power BI Desktop para mostrar datos de Business Central | Documentos de Microsoft
description: Haga que los datos estén disponibles como origen de datos en Power BI y generar informes eficaces del estado de la empresa.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: business intelligence, KPI, Odata, Power App, SOAP, analysis
ms.date: 04/01/2021
ms.author: jswymer
ms.openlocfilehash: ef81b4fd16e66c4ec1453798ae77f947b12c975e
ms.sourcegitcommit: eeaf9651c26e49974254e29b7e2d16200c818dad
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 07/06/2021
ms.locfileid: "6341338"
---
# <a name="building-power-bi-reports-to-display-prod_long-data"></a>Crear informes de Power BI para mostrar datos de [!INCLUDE [prod_long](includes/prod_long.md)]

Puede hacer que los datos de [!INCLUDE[prod_long](includes/prod_long.md)] estén disponibles como origen de datos en Power BI Desktop y generar informes eficaces del estado de la empresa.

Este artículo describe cómo empezar a usar Power BI Desktop para crear informes que muestren datos de [!INCLUDE[prod_long](includes/prod_long.md)].  Después de crear informes, puede publicarlos en su servicio de Power BI o compartirlos con todos los usuarios de su organización. Una vez que estos informes estén en el servicio de Power BI, los usuarios que están configurados para él, pueden ver los informes en [!INCLUDE[prod_long](includes/prod_long.md)].

## <a name="get-ready"></a>Prepararse

- Regístrese para el servicio de Power BI.

  Si aún no se ha registrado, vaya a [https://powerbi.microsoft.com](https://powerbi.microsoft.com). Cuando se registre, use su dirección de correo electrónico y contraseña del trabajo.

- Descargue [Power BI Desktop](https://powerbi.microsoft.com/desktop/).

  Power BI Desktop es una aplicación gratuita que se instala en su computadora local. Para obtener más información, consulte [Inicio rápido: Conectarse a los datos de Power BI Desktop](/power-bi/desktop-quickstart-connect-to-data).

- Asegúrese de que los datos que desea en el informe están disponibles como página API o publicados como servicio web.

  Para más información, vea [Exponer datos a través de páginas API o servicios web OData](admin-powerbi-setup.md#exposedata).

- Para [!INCLUDE[prod_short](includes/prod_short.md)] local, obtenga la siguiente información:

  - La URL de OData para [!INCLUDE[prod_short](includes/prod_short.md)].
  
    Normalmente, esta URL tiene el formato `http[s]://[computer]:[port]/[serverinstance]/ODataV4`, por ejemplo,`https://localhost:7048/BC160/ODataV4`. Si tiene una implementación de múltiples inquilinos, incluya al inquilino en la URL, por ejemplo,`https://localhost:7048/BC160/ODataV4?tenant=tenant1`.
  - Un nombre de usuario y una clave de acceso al servicio web de una cuenta de [!INCLUDE[prod_short](includes/prod_short.md)].

    Para obtener datos de [!INCLUDE[prod_short](includes/prod_short.md)], Power BI utiliza autenticación básica. Por lo tanto, necesitará un nombre de usuario y una clave de acceso al servicio web para conectarse. La cuenta puede ser su propia cuenta de usuario o su organización puede tener una cuenta específica para este propósito.

- Descargue el tema de informe [!INCLUDE [prod_short](includes/prod_short.md)] (opcional).

  Para más información, ver [Usar el tema de informe [!INCLUDE [prod_short](includes/prod_short.md)]](#theme) en este articulo.

## <a name="add-prod_short-as-a-data-source-in-power-bi-desktop"></a><a name="getdata"></a>Agregar [!INCLUDE[prod_short](includes/prod_short.md)] como origen de datos de Power BI Desktop

La primera tarea al crear informes es agregar [!INCLUDE[prod_short](includes/prod_short.md)] como fuente de datos en Power BI Desktop. Una vez conectado, puede comenzar a generar el informe.

1. Inicie Power BI Desktop.
2. Seleccione  **Obtener datos**.

    Si no ve **Obtener datos**, seleccione el menú **Archivo** y luego **Obtener datos**.
3. En la página **Obtener datos**, seleccione **Servicios en línea**.
4. En el panel **Servicios en línea**, realice uno de los siguientes pasos:

    - Para conectarse a [!INCLUDE [prod_short](includes/prod_short.md)] en línea, seleccione **Dynamics 365 Business Central**, luego **Conectar**.
    - Para conectarse a [!INCLUDE [prod_short](includes/prod_short.md)] local, seleccione **Dynamics 365 Business Central (local)**, luego **Conectar**.

5. Inicie sesión en [!INCLUDE [prod_short](includes/prod_short.md)] (solo una vez).

    Si no ha iniciado sesión antes en [!INCLUDE [prod_short](includes/prod_short.md)] desde Power BI Desktop, se le pedirá que inicie sesión.

    - Para [!INCLUDE [prod_short](includes/prod_short.md)] online, seleccione **Iniciar sesión** y luego elija la cuenta pertinente. Use la misma cuenta con la que inicia sesión en [!INCLUDE [prod_short](includes/prod_short.md)]. Cuando termine, seleccione **Conectar**.

    - Para [!INCLUDE [prod_short](includes/prod_short.md)] local, primero ingrese la dirección URL de OData para [!INCLUDE[prod_short](includes/prod_short.md)] y luego seleccione **Aceptar**. Cuando se le solicite, ingrese el nombre de usuario y la contraseña de la cuenta que se usará para conectarse a [!INCLUDE[prod_short](includes/prod_short.md)]. En **Contraseña**, ingrese la clave de acceso al servicio web. Cuando termine, seleccione **Conectar**.

    > [!NOTE]  
    > Una vez que se haya conectado correctamente a [!INCLUDE[prod_short](includes/prod_short.md)], no se le volverá a solicitar que inicie sesión. [¿Cómo cambio o borro la cuenta que estoy usando actualmente para conectarme a Business Central desde Power BI Desktop?](/dynamics365/business-central/power-bi-faq?tabs=designer#perms)

6. Una vez conectado, Power BI se pone en contacto con el servicio Business Central. Aparecen las ventanas **Navegador** y se muestran los orígenes de datos disponibles para generar informes. Seleccione una carpeta para expandirla y ver los orígenes de datos disponibles. 

   Estos orígenes de datos representan todos los servicios web y las páginas API que están publicados para [!INCLUDE [prod_short](includes/prod_short.md)]. Los orígenes de datos están agrupadas por entornos y empresas de Business Central. Con Business Central online, **Navegador** tiene la siguiente estructura:

    - **Nombre de entorno**
      - **Nombre de la empresa**
        - **API avanzadas**

          Esta carpeta enumera las páginas API avanzadas publicadas por Microsoft, como las [API de automatización de Business Central](/dynamics365/business-central/dev-itpro/administration/itpro-introduction-to-automation-apis) y las [páginas API personalizadas para Business Central](/dynamics365/business-central/dev-itpro/developer/devenv-develop-custom-api). Las páginas de API personalizadas se agrupan además en carpetas por las propiedades [APIPublisher](/business-central/dev-itpro/developer/properties/devenv-apipublisher-property)/[APIGroup](/business-central/dev-itpro/developer/properties/devenv-apigroup-property) del código de la página API.

        - **API estándar v2.0**

          Esta carpeta enumera las páginas API expuestas por la [API de Business Central V2.0](/dynamics365/business-central/dev-itpro/api-reference/v2.0/).

        - **Servicios web \(heredado)**

          Esta carpeta enumera las páginas, unidades de código y consultas que se publican como servicios web en Business Central.

    > [!NOTE]
    > La estructura de Business Central local es diferente porque no admite páginas API.

7. Seleccione el origen o los orígenes de datos que desea agregar al modelo de datos y después seleccione el botón **Cargar**.
8. Si más adelante desea agregar más datos de Business Central, puede repetir los pasos anteriores.

Una vez que los datos se hayan cargado, puede verlos en el panel de navegación derecho en la página. Ya se ha conectado correctamente con los datos de [!INCLUDE[prod_short](includes/prod_short.md)] y puede comenzar a crear su informe de Power BI.  

> [!TIP]
> Para obtener más información sobre el uso de Power BI Desktop, vea [Introducción a Power BI Desktop](/power-bi/fundamentals/desktop-getting-started).

## <a name="creating-accessible-reports"></a>Crear informes accesibles

Es importante que sus informes puedan ser utilizados por tantas personas como sea posible. Intente diseñar informes para que no requieran ninguna adaptación especial para satisfacer las necesidades específicas de diferentes usuarios. Asegúrese de que el diseño permita a los usuarios aprovechar las tecnologías de asistencia estándar, como los lectores de pantalla. Power BI incluye varias funciones, herramientas y pautas de accesibilidad para ayudarle a lograr este objetivo. Para más información, [Diseñar informes de Power BI para accesibilidad](/power-bi/create-reports/desktop-accessibility-creating-reports) en la documentación de Power BI.

## <a name="creating-reports-to-display-data-associated-with-a-list"></a>Crear informes para mostrar datos asociados con una lista

Puede crear informes que se muestren en un cuadro informativo de una página de lista [!INCLUDE [prod_short](includes/prod_short.md)]. Los informes pueden contener datos sobre el registro seleccionado en la lista. La creación de estos informes es similar a otros informes, excepto que hay algunas cosas que deberá hacer para asegurarse de que los informes se muestren como se espera. Para más información, ver [Crear informes de Power BI para mostrar datos de lista en [!INCLUDE[prod_short](includes/prod_short.md)]](across-how-use-powerbi-reports-factbox.md).

## <a name="using-the-prod_short-report-theme-optional"></a><a name="theme"></a>Usar el tema de informe [!INCLUDE [prod_short](includes/prod_short.md)] (optional)

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

Una vez que haya creado o modificado un informe, puede publicarlo en su servicio de Power BI y también compartirlo con otros miembros de su organización. Una vez publicado, verá el informe en Power BI. El informe también está disponible para su selección en [!INCLUDE[prod_short](includes/prod_short.md)].

Para publicar un informe, seleccione **Publicar** en la pestaña **Inicio** de la cinta o del menú **Archivo**. Si ha iniciado sesión en el servicio Power BI, el informe se publica en este servicio. De lo contrario, se le pedirá que inicie sesión. 

## <a name="distribute-or-share-a-report"></a>Distribuir o compartir un informe

Hay dos formas de enviar informes a sus compañeros de trabajo y a otras personas:

- Distribuya informes como archivos .pbix.

    Los informes se almacenan en su computadora como archivos .pbix. Puede distribuir el archivo .pbix del informe a los usuarios, como cualquier otro archivo. Luego, los usuarios pueden cargar el archivo en su servicio de Power BI. Ver [Cargar informes desde archivos](across-working-with-business-central-in-powerbi.md#upload).

    > [!NOTE]
    > La distribución de informes de esta manera significa que la actualización de los datos de los informes la realizará cada usuario de forma individual. Esta situación podría impactar el rendimiento de [!INCLUDE[prod_short](includes/prod_short.md)].

- Compartir el informe del servicio de Power BI

    Si tiene una licencia de Power BI Pro, puede compartir el informe con otros, directamente desde su servicio de Power BI. Para más información, ver [Power BI - Compartir un panel o informe](/power-bi/collaborate-share/service-share-dashboards#share-a-dashboard-or-report).

## <a name="see-related-training-at-microsoft-learn"></a>Consulte Formación relacionada en [Microsoft Learn](/learn/modules/configure-powerbi-excel-dynamics-365-business-central/index)

## <a name="see-also"></a>Consulte también

[Habilitar los datos de negocio para Power BI](admin-powerbi.md)  
[Inteligencia empresarial](bi.md)  
[Preparación para hacer negocios](ui-get-ready-business.md)  
[Importar datos de empresa de otros sistemas financieros](across-import-data-configuration-packages.md)  
[Configurar [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md)  
[Finanzas](finance.md)  
[Inicio rápido: Conectarse a los datos de Power BI Desktop](/power-bi/desktop-quickstart-connect-to-data)  


[!INCLUDE[footer-include](includes/footer-banner.md)]