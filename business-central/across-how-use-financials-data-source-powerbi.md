---
title: Creación de informes en Power BI Desktop para mostrar datos de Business Central | Documentos de Microsoft
description: Haga que los datos estén disponibles como origen de datos en Power BI y generar informes eficaces del estado de la empresa.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: business intelligence, KPI, Odata, Power App, SOAP, analysis
ms.date: 10/01/2020
ms.author: jswymer
ms.openlocfilehash: ce1ce3039758d5991eb3a770713d2f1e273bbe0c
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "4754522"
---
# <a name="building-power-bi-reports-to-display-prod_long-data"></a>Crear informes de Power BI para mostrar datos de [!INCLUDE [prod_long](includes/prod_long.md)]

Puede hacer que los datos de [!INCLUDE[prod_long](includes/prod_long.md)] estén disponibles como origen de datos en Power BI Desktop y generar informes eficaces del estado de la empresa.

Este artículo describe cómo empezar a usar Power BI Desktop para crear informes que muestren datos de [!INCLUDE[prod_long](includes/prod_long.md)].  Después de crear informes, puede publicarlos en su servicio de Power BI o compartirlos con todos los usuarios de su organización. Una vez que estos informes estén en el servicio de Power BI, los usuarios que están configurados para él, pueden ver los informes en [!INCLUDE[prod_long](includes/prod_long.md)].

## <a name="get-ready"></a>Prepararse

- Regístrese para el servicio de Power BI.

    Si aún no se ha registrado, vaya a [https://powerbi.microsoft.com](https://powerbi.microsoft.com). Cuando se registre, use su dirección de correo electrónico y contraseña del trabajo.

- Descargue [Power BI Desktop](https://powerbi.microsoft.com/desktop/).

   Power BI Desktop es una aplicación gratuita que se instala en su computadora local. Para obtener más información, consulte [Inicio rápido: Conectarse a los datos de Power BI Desktop](/power-bi/desktop-quickstart-connect-to-data).

- Asegúrese de que los datos que desea en el informe se publiquen como un servicio web.
    
    Hay muchos servicios web publicados de forma predeterminada. Un modo de fácil de encontrar los servicios web es buscar *servicios web* en [!INCLUDE[prod_short](includes/prod_short.md)]. En la página **Servicios web**, asegúrese de que el campo **Publicar** está seleccionado. Esta tarea normalmente es administrativa.
    
    Para obtener más información sobre la publicación de servicios web, consulte [Publicar un servicio web](across-how-publish-web-service.md).

- Para [!INCLUDE[prod_short](includes/prod_short.md)] local, obtenga la siguiente información:

    - La URL de OData para [!INCLUDE[prod_short](includes/prod_short.md)]. Normalmente, esta URL tiene el formato `http[s]://[computer]:[port]/[serverinstance]/ODataV4`, por ejemplo,`https://localhost:7048/BC160/ODataV4`. Si tiene una implementación de múltiples inquilinos, incluya al inquilino en la URL, por ejemplo,`https://localhost:7048/BC160/ODataV4?tenant=tenant1`.
    - Un nombre de usuario y una clave de acceso al servicio web de una cuenta de [!INCLUDE[prod_short](includes/prod_short.md)].

      Para obtener datos de [!INCLUDE[prod_short](includes/prod_short.md)], Power BI utiliza autenticación básica. Por lo tanto, necesitará un nombre de usuario y una clave de acceso al servicio web para conectarse. La cuenta puede ser su propia cuenta de usuario o su organización puede tener una cuenta específica para este propósito.

- Descargue el tema de informe [!INCLUDE [prod_short](includes/prod_short.md)] (opcional).

    Para más información, ver [Usar el tema de informe [!INCLUDE [prod_short](includes/prod_short.md)]](#theme) en este articulo.

## <a name="add-prod_short-as-a-data-source-in-power-bi-desktop"></a>Agregar [!INCLUDE[prod_short](includes/prod_short.md)] como origen de datos de Power BI Desktop

La primera tarea al crear informes es agregar [!INCLUDE[prod_short](includes/prod_short.md)] como fuente de datos en Power BI Desktop. Una vez conectado, puede comenzar a generar el informe.

1. Inicie Power BI Desktop.
2. Seleccione  **Obtener datos**.

    Si no ve **Obtener datos**, seleccione el menú **Archivo** y luego **Obtener datos**.
2. En la página **Obtener datos**, seleccione **Servicios en línea**.
3. En el panel **Servicios en línea**, realice uno de los siguientes pasos:

    1. Si se está conectando a [!INCLUDE [prod_short](includes/prod_short.md)] Online, elija **Dynamics 365 Business Central** y luego **Conectar**.
    2. Si se está conectando a [!INCLUDE [prod_short](includes/prod_short.md)] local, elija **Dynamics 365 Business Central (on-premises)** y luego **Conectar**.

4. Power BI muestra un asistente que le guiará por el proceso de conexión, incluido el inicio de sesión en [!INCLUDE [prod_short](includes/prod_short.md)].

    Para la Online, elija **Iniciar sesión** y luego elija la cuenta pertinente. Use la misma cuenta con la que inicia sesión en [!INCLUDE [prod_short](includes/prod_short.md)].
    
    Para local, ingrese la URL de OData para [!INCLUDE[prod_short](includes/prod_short.md)] y, opcionalmente, el nombre de la empresa. Luego, cuando se le solicite, ingrese el nombre de usuario y la contraseña de la cuenta que se usará para conectarse a [!INCLUDE[prod_short](includes/prod_short.md)]. En **Contraseña**, ingrese la clave de acceso al servicio web.

    > [!NOTE]  
    > Una vez que se haya conectado correctamente a [!INCLUDE[prod_short](includes/prod_short.md)], no se le volverá a solicitar que inicie sesión.
    
5. Seleccione **Conectar** para continuar.

    El asistente de Power BI muestra una lista de los entornos, las empresas y los orígenes de datos de Microsoft [!INCLUDE[prod_short](includes/prod_short.md)]. Estos orígenes de datos todos los servicios web que haya publicado desde [!INCLUDE [prod_short](includes/prod_short.md)].
6. Especifique los datos que desea agregar al modelo de datos y después seleccione el botón **Cargar**.
7. Repita los pasos anteriores agregar datos de [!INCLUDE [prod_short](includes/prod_short.md)] adicionales, u otros datos, a su modelo de datos de Power BI.

Una vez que los datos se hayan cargado, puede verlos en el panel de navegación derecho en la página. Ya se ha conectado correctamente con los datos de [!INCLUDE[prod_short](includes/prod_short.md)] y puede comenzar a crear su informe de Power BI.  

> [!TIP]
> Para obtener más información sobre el uso de Power BI Desktop, vea [Introducción a Power BI Desktop](/power-bi/fundamentals/desktop-getting-started).

## <a name="creating-reports-to-display-data-associated-with-a-list"></a>Crear informes para mostrar datos asociados con una lista

Puede crear informes que se muestren en un cuadro informativo de una página de lista [!INCLUDE [prod_short](includes/prod_short.md)]. Los informes pueden contener datos sobre el registro seleccionado en la lista. La creación de estos informes es similar a otros informes, excepto que hay algunas cosas que deberá hacer para asegurarse de que los informes se muestren como se espera. Para más información, ver [Crear informes de Power BI para mostrar datos de lista en [!INCLUDE[prod_short](includes/prod_short.md)]](across-how-use-powerbi-reports-factbox.md).

## <a name="using-the-prod_short-report-theme-optional"></a><a name="theme"></a>Usar el tema de informe [!INCLUDE [prod_short](includes/prod_short.md)] (optional)

Antes de elaborar el informe, le recomendamos que descargue e importe el archivo de tema de Microsoft [!INCLUDE [prod_short](includes/prod_short.md)]. El archivo de tema crea una paleta de colores de forma que pueda crear informes con el mismo estilo de color que las aplicaciones de [!INCLUDE [prod_short](includes/prod_short.md)] sin pedirle que defina colores personalizados para cada elemento visual.

> [!NOTE]
> Esta tarea es opcional. Siempre puede crear sus informes y luego descargar y aplicar la plantilla de estilo más tarde.

### <a name="download-the-theme"></a>Descargar el tema

El archivo de tema está disponible como archivo json en la Galería de temas comunitarios de Microsoft Power BI. Para descargar el archivo de tema, siga los siguientes pasos:

1. Ir a [Galería de temas comunitarios de Microsoft Power BI para Microsoft Dynamics 365 Business Central](https://community.powerbi.com/t5/Themes-Gallery/Microsoft-Dynamics-365-Business-Central/m-p/385875).
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
[Introducción](product-get-started.md)  
[Importar datos de empresa de otros sistemas financieros](across-import-data-configuration-packages.md)  
[Configurar [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md)  
[Finanzas](finance.md)  
[Inicio rápido: Conectarse a los datos de Power BI Desktop](/power-bi/desktop-quickstart-connect-to-data)  
