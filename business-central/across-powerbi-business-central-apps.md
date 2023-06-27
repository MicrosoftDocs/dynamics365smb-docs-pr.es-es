---
title: Usar aplicaciones de Business Central en Power BI
description: 'Obtener información, inteligencia empresarial y KPI de los datos de Business Central resulta muy sencillo con las aplicaciones de Business Central para Power BI.'
author: jswymer
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'account schedule, analysis, reporting, financial report, business intelligence, KPI'
ms.date: 04/01/2021
ms.author: jswymer
---
# <a name="use-the--apps-in-power-bi" />Usar aplicaciones de [!INCLUDE [prod_short](includes/prod_short.md)] en Power BI

> **SE APLICA A:**[!INCLUDE [prod_long](includes/prod_long.md)] Online 

[!INCLUDE [prod_long](includes/prod_long.md)] publica las siguientes aplicaciones de Power BI, que proporcionan paneles detallados para ver datos:

- [!INCLUDE [prod_long](includes/prod_long.md)] - CRM  
- [!INCLUDE [prod_long](includes/prod_long.md)] - Finance  
- [!INCLUDE [prod_long](includes/prod_long.md)] - Sales

## <a name="overview" />Panorama

Cada aplicación incluye varios informes en los que puede profundizar en busca de datos, incluidas las siguientes características:

- Seleccione cualquier representación visual del panel para traer uno de los informes subyacentes.  
- Filtre el informe o agregue los campos que desee supervisar.  
- Ancle una visualización personalizada al panel para continuar con el seguimiento.  
  Puede actualizar los datos manualmente y puede configurar un calendario de actualización. Para obtener más información, vea [Configuración de actualización programada](/power-bi/refresh-scheduled-refresh).  

Las aplicaciones están diseñadas para trabajar con datos de cualquier empresa en [!INCLUDE[prod_short](includes/prod_short.md)]. Cuando instala la aplicación Power BI, especifica uno o más parámetros para conectarse a su [!INCLUDE [prod_short](includes/prod_short.md)].  

> [!NOTE]
> También puede crear sus propios informes y paneles en Power BI basándose en sus datos de [!INCLUDE[prod_short](includes/prod_short.md)]. Para obtener más información, consulte [Conectar los datos empresariales con Power BI](across-how-use-financials-data-source-powerbi.md). 

## <a name="prerequisites" />Requisitos previos

Las aplicaciones de Power BI requieren permisos para las tablas de donde se recuperan los datos y los servicios web que se utilizan para recuperar los datos. La siguiente tabla enumera los servicios web necesarios para cada aplicación de Power BI:
    
|App | Servicios Web|
|----|-------------|
|[!INCLUDE[prod_short](includes/prod_short.md)] – CRM| <ul><li>Oportunidades de venta</li><li>Plantilla de empresa de vista de plantilla de Excel</li><li>Etiquetas de informe del Power BI</li></ul>|
|[!INCLUDE[prod_short](includes/prod_short.md)] – Finance| <ul><li>PowerBIFinance</li><li>Plantilla de empresa de vista de plantilla de Excel</li><li>Etiquetas de informe del Power BI</li></ul>|
|[!INCLUDE[prod_short](includes/prod_short.md)] – Sales| <ul><li>Ventas de productos por cliente</li><li>Panel de ventas</li><li>Plantilla de empresa de vista de plantilla de Excel</li><li>Etiquetas de informe del Power BI</li></ul>|

> [!TIP]
> Un modo de fácil de encontrar los servicios web es buscar *servicios web* en [!INCLUDE[prod_short](includes/prod_short.md)]. En la página de **Servicios web**, asegúrese de que el campo **Publicar** esté seleccionado para los servicios web enumerados más arriba. Para obtener más información, consulte [Publicar un servicio web](across-how-publish-web-service.md).

## <a name="get-ready" />Prepararse

Regístrese para el servicio de Power BI. Si aún no se ha registrado, vaya a [https://powerbi.microsoft.com](https://powerbi.microsoft.com). Cuando se registre, use su dirección de correo electrónico y contraseña del trabajo.

## <a name="install-a--app-in-power-bi" />Instale una aplicación de [!INCLUDE[prod_short](includes/prod_short.md)] en Power BI

1. Abra su explorador, navegue hasta [https://powerbi.microsoft.com](https://powerbi.microsoft.com) e inicie sesión en su cuenta.
2. Seleccione **Obtener datos** en la parte inferior del panel de navegación izquierdo.  

    ![Navegar para obtener datos.](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-get-data.png)

    También puede empezar desde [!INCLUDE [prod_short](includes/prod_short.md)]. Desde su página Web, vaya a **Selección de informes** en la sección Power BI. Seleccione **Servicio** o **Mi organización** en la cinta. Se abre la galería de la organización en Power BI o Microsoft AppSource, filtrados para mostrar solo las aplicaciones relacionadas con [!INCLUDE[prod_short](includes/prod_short.md)].

3. En el cuadro **Servicios**, seleccione **Obtener**.

    Este paso abre la página **Aplicaciones de Power BI**, que le permite buscar la aplicación de Power BI disponible en **AppSource**.  

4. En el cuadro de **Buscar**, introduzca **Dynamics 365 Business Central**.
5. Seleccione la aplicación que desea usar, seleccione **Consiguelo ahora** y entonces **Instalar**.  

    Cuando se complete, la aplicación estará disponible en **Aplicaciones** en el menú de navegación en Power BI.

## <a name="connect-the--app-to-your-data" />Conecte la aplicación de [!INCLUDE[prod_short](includes/prod_short.md)] a sus datos

1. Bajo **Aplicaciones**, seleccione la aplicación Business Central, luego **Conectar**.
2. Cuando se le solicite, rellene **Nombre de empresa** y **Entorno** con información sobre la instancia de [!INCLUDE[prod_short](includes/prod_short.md)] a la que desee conectarse.

    - Para**Nombre de empresa**, asegúrese de utilizar el nombre completo, no el nombre para mostrar. Puede encontrar el nombre de la empresa en la página **Empresas** en [!INCLUDE[prod_short](includes/prod_short.md)]. 
    - Para **Entorno**, si no ha creado varios entornos, introduzca **Producción**.

3. Seleccione **Siguiente**.
4. Seleccione **Registrarse**.
5. Cuando se le solicite, ingrese el nombre de usuario y la contraseña para iniciar sesión en [!INCLUDE[prod_short](includes/prod_short.md)].
6. Una vez conectado, se añaden un panel e informes a su área de trabajo de Power BI. Cuando se haya completado, se muestran los mosaicos con datos de su empresa de [!INCLUDE[prod_short](includes/prod_short.md)].

    ![Seleccione Dynamics 365 Business Central y seleccione Obtener ahora.](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-workspace-dashboard-report-dataset.png)

## <a name="fixing-problems" />Solucionar problemas

El panel de Power BI se basa en los servicios web publicados que se enumeran anteriormente. Muestra datos de la empresa de demostración o de su propia empresa si importa datos de su solución financiera actual. Sin embargo, si se produce algún error, en esta sección se proporcionará una solución para los problemas más habituales.  

### <a name="you-dont-have-a-power-bi-account" />No tiene una cuenta de Power BI

No se ha configurado una cuenta de Power BI. Debe tener una licencia para obtener una cuenta de Power BI. Además, debe haber iniciado sesión previamente en Power BI para crear su espacio de trabajo de Power BI.  

### <a name="message-there-are-no-enabled-reports-choose-select-report-to-see-a-list-of-reports-that-you-can-display" />Mensaje: No hay informes habilitados. Elija Seleccionar informe para ver una lista de informes que se pueden visualizar.

Este mensaje aparece si el informe predeterminado no se pudo implementar en su espacio de trabajo de Power BI. O el informe se implementó pero no se actualizó correctamente. Si sucede este problema, navegue hasta el informe en su espacio de trabajo de Power BI, seleccione **Conjunto de datos**, **Configuración** y luego actualice manualmente las credenciales. Una vez que el conjunto de datos se actualice correctamente, vuelva a [!INCLUDE[prod_short](includes/prod_short.md)] y seleccione manualmente el informe desde la página **Seleccionar informes**.

### <a name="you-need-a-power-bi-pro-license-to-install-the--app-in-power-bi" />Necesita una licencia Power BI Pro para instalar la aplicación de [!INCLUDE[prod_short](includes/prod_short.md)] en Power BI

Necesita una [Licencia Pro de Power BI](/power-bi/service-features-license-type) para compartir su contenido y las personas con las que lo comparte también lo hacen. El contenido debe estar en un espacio de trabajo con [capacidad Premium](/power-bi/service-premium-what-is). Para más información, vea [Formas de compartir el trabajo en Power BI](/power-bi/service-how-to-collaborate-distribute-dashboards-reports).  

### <a name="parameter-validation-failed-please-make-sure-all-parameters-are-valid" />"Error en la validación de parámetros, asegúrese de que todos los parámetros sean válidos"

Este error indica que uno o varios de los parámetros no son válidos.

- El parámetro de ambiente especificado no coincide con ningún ambiente de producción o aislado de [!INCLUDE[prod_short](includes/prod_short.md)] existente.
- El parámetro de empresa especificado no coincide con ninguna empresa de [!INCLUDE[prod_short](includes/prod_short.md)] existente. Verifique el nombre de la empresa en la página **Empresas** en [!INCLUDE[prod_short](includes/prod_short.md)].
- Si se conecta a [!INCLUDE[prod_short](includes/prod_short.md)] local, ingresó una URL que no es válida. Puede verificar la URL en la página de **Servicios web** en [!INCLUDE[prod_short](includes/prod_short.md)]  
- Un puerto no está abierto para permitir que la petición pase a través de su firewall.

### <a name="cant-sign-in" />No puede iniciar sesión

Si obtiene un "error de inicio de sesión" después de usar sus credenciales de usuario de [!INCLUDE[prod_short](includes/prod_short.md)] para iniciar sesión, es probable que esté experimentando uno de los siguientes problemas:

- La cuenta que usa no tiene permisos para recuperar los datos de [!INCLUDE[prod_short](includes/prod_short.md)] de su cuenta. Compruebe que tiene permisos para introducir los datos necesarios en [!INCLUDE[prod_short](includes/prod_short.md)] e inténtelo de nuevo.
- Ha seleccionado un tipo de autenticación distinto de Básico si se conecta con [!INCLUDE[prod_short](includes/prod_short.md)]local.
- No ha introducido un nombre de usuario o una contraseña válidos.

### <a name="message-your-data-source-cant-be-refreshed-because-the-credentials-are-invalid-please-update-your-credentials-and-try-again" />Mensaje: Su fuente de datos no se puede actualizar porque las credenciales no son válidas. Actualice sus credenciales y vuelva a intentarlo.

Para [!INCLUDE[prod_short](includes/prod_short.md)] local, el problema podría ser que la URL de OData solo esté expuesta a la red local.

### <a name="incorrect-company-name" />Nombre de empresa incorrecto

Un error común es introducir el nombre para mostrar de empresa en lugar del nombre de la empresa. Para buscar el nombre de la empresa, busque **Empresas**. A continuación, use el campo **Nombre** al introducir el nombre de su empresa.

### <a name="the-key-didnt-match-any-rows-in-the-table" />La clave no coincidía con ninguna fila de la tabla

Si introduce un nombre de empresa no válido durante el proceso de conexión, puede recibir el mensaje de error "La clave no coincidió con ninguna fila de la tabla". Proporcione el nombre correcto de la empresa e intente conectarse de nuevo.

### <a name="historical-data-appears-to-be-missing" />Parece que faltan datos históricos

Una vez que la aplicación de Power BI se instala y sus datos aparecen en Power BI, puede observar que no se muestran todos sus datos. Los conjuntos de datos se filtran para que solo se devuelvan los datos de los 365 días anteriores. Este valor predeterminado se utiliza para ayudar a que los informes sean más rápidos.  

### <a name="i-only-see-data-for-a-single-company" />Solo veo datos de una sola empresa

La aplicación de Power BI solo mostrará los datos de la empresa de [!INCLUDE[prod_short](includes/prod_short.md)] que se definió cuando se instaló la aplicación de Power BI. Los datos de empresas adicionales se pueden añadir a los informes añadiendo nuevas consultas que utilizan empresas diferentes como origen de datos.  

### <a name="what-now" />¿Y ahora qué?

- Intente [hacer una pregunta en el cuadro de preguntas](/power-bi/service-q-and-a-tips) en la parte superior del escritorio.
- [Cambie los mosaicos](/power-bi/service-dashboard-edit-tile) en el escritorio.  
- [Seleccione un mosaico](/power-bi/service-dashboard-tiles) para abrir el informe subyacente.  
- De forma predeterminada, su conjunto de datos no está programado para actualizarse. Puede cambiar la programación de actualización o intentar actualizarlo a petición utilizando **Actualizar ahora**. Para obtener más información, vea [Configuración de actualización programada](/power-bi/refresh-scheduled-refresh).

## <a name="see-related-microsoft-training" />Consultar la [formación de Microsoft](/training/modules/configure-powerbi-excel-dynamics-365-business-central/index) relacionada

## <a name="see-also" />Consulte también

[Business Central y Power BI](admin-powerbi.md)  
[Componente de integración de Power BI e información general de la arquitectura para [!INCLUDE[prod_short](includes/prod_short.md)]](admin-powerbi-overview.md)  
[Trabajar con datos de [!INCLUDE [prod_short](includes/prod_short.md)] en Power BI](across-working-with-business-central-in-powerbi.md)  
[Crear informes de Power BI para mostrar datos de [!INCLUDE [prod_long](includes/prod_long.md)]](across-how-use-financials-data-source-powerbi.md)  
[Inteligencia empresarial](bi.md)  
[Prepárese para hacer negocios](ui-get-ready-business.md)  
[Importar datos de empresa de otros sistemas financieros](across-import-data-configuration-packages.md)  
[Configurar [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md)  
[Usar [!INCLUDE[prod_short](includes/prod_short.md)] como origen de datos de Power BI](across-how-use-financials-data-source-powerbi.md)  
[Usar [!INCLUDE[prod_short](includes/prod_short.md)] como origen de datos de Power Apps](across-how-use-financials-data-source-powerapps.md)  
[Usar [!INCLUDE[prod_short](includes/prod_short.md)] en Power Automate](across-how-use-financials-data-source-flow.md)  
[Documentación de Power BI](/power-bi/)  
[¿Qué es Power BI?](/power-bi/fundamentals/power-bi-overview)  
[Inicio rápido: Conectarse a los datos de Power BI Desktop](/power-bi/desktop-quickstart-connect-to-data)  
[Introducción a los datamarts](/power-bi/transform-model/datamarts/datamarts-overview)  
[Introducción a los flujos de datos y preparación de datos de autoservicio](/power-bi/transform-model/dataflows/dataflows-introduction-self-service)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
