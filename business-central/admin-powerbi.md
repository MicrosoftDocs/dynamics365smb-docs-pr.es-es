---
title: Habilitar los datos de negocio para Power BI| Documentos de Microsoft
description: Obtener información, inteligencia empresarial y KPI de los datos de Business Central resulta muy sencillo con las aplicaciones de Business Central para Power BI.
author: bmeier90
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: account schedule, analysis, reporting, financial report, business intelligence, KPI
ms.reviewer: edupont
ms.date: 10/01/2019
ms.author: bmeier
ms.openlocfilehash: 0750f1724260eb7767757d947f30dcb074ef1aeb
ms.sourcegitcommit: cfc92eefa8b06fb426482f54e393f0e6e222f712
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 12/03/2019
ms.locfileid: "2879111"
---
# <a name="enabling-your-business-data-for-power-bi"></a>Habilitar los datos de negocio para Power BI

Obtener información de los datos de [!INCLUDE[prodshort](includes/prodshort.md)] resulta muy sencillo con las aplicaciones de [!INCLUDE[prodshort](includes/prodshort.md)] para Power BI. Power BI extrae los datos y, a continuación, genera un panel original e informes en función de los datos.  

Debe disponer de una cuenta válida con [!INCLUDE[prodshort](includes/prodshort.md)] y con Power BI. Además, deberá descargar [Power BI Desktop](https://powerbi.microsoft.com/desktop/) si desea crear sus propios informes de Power BI. Las aplicaciones de Power BI requieren permisos para las tablas desde donde se recuperan los datos. A continuación se describen más detalles sobre los requisitos.  

> [!IMPORTANT]
> Las aplicaciones de Power BI que se describen en este artículo están diseñados para utilizar Azure Active Directory como mecanismo de autenticación, a menos que se especifique lo contrario. Para instalar una aplicación de Power BI, también debe tener una licencia de Power BI Pro.  Una vez instalada la aplicación de Power BI, se puede compartir con usuarios de cualquier tipo de licencia.

[!INCLUDE [prodlong](includes/prodlong.md)] ha publicado las siguientes aplicaciones para Power BI:

- [!INCLUDE [prodlong](includes/prodlong.md)] - CRM  
- [!INCLUDE [prodlong](includes/prodlong.md)] - Finance  
- [!INCLUDE [prodlong](includes/prodlong.md)] - Sales  
- [!INCLUDE [prodlong](includes/prodlong.md)](local) - CRM  
- [!INCLUDE [prodlong](includes/prodlong.md)](local) - Finance  
- [!INCLUDE [prodlong](includes/prodlong.md)](local) - Sales  

## <a name="using-the-include-prodshortincludesprodshortmd-dashboards-in-power-bi"></a>Uso de los paneles de [!INCLUDE [prodshort](includes/prodshort.md)] en Power BI

Cada aplicación proporciona informes que puede explorar:

- Seleccione cualquier representación visual del panel para traer uno de los informes subyacentes.  
- Filtre el informe o agregue los campos que desee supervisar.  
- Ancle esta visualización personalizada al panel para continuar con el seguimiento.  
  Puede actualizar los datos manualmente y puede configurar un calendario de actualización. Para obtener más información, vea [Configuración de actualización programada](/power-bi/refresh-scheduled-refresh).  

Las aplicaciones están diseñadas para trabajar con datos de cualquier empresa que tenga en su [!INCLUDE[prodshort](includes/prodshort.md)]. Cuando instala la aplicación Power BI, especifica uno o más parámetros para conectarse a su [!INCLUDE [prodshort](includes/prodshort.md)].  

> [!NOTE]
> También puede crear sus propios informes y paneles en Power BI basándose en sus datos de [!INCLUDE[d365fin](includes/d365fin_md.md)]. Para obtener más información, consulte [Conectar los datos empresariales con Power BI](across-how-use-financials-data-source-powerbi.md).  

### <a name="to-connect-your-data-in-power-bi"></a>Para conectar sus datos en Power BI

1. Abra su explorador, navegue hasta https://powerbi.microsoft.com e inicie sesión en su cuenta.
2. Seleccione **Obtener datos** en la parte inferior del panel de navegación izquierdo.  

    ![Navegar para obtener datos](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-get-data.png)

    También puede empezar desde [!INCLUDE [prodshort](includes/prodshort.md)]. Desde su página Web, vaya a **Selección de informes** en la sección Power BI. Seleccione **Servicio** o **Mi organización** en la cinta. Cuando cualquiera de estas acciones está seleccionada, accederá a la galería de la organización en Power BI o a Microsoft AppSource, que también se filtrarán para mostrar solo las aplicaciones relacionadas con [!INCLUDE[prodshort](includes/prodshort.md)].

3. En el cuadro **Servicios**, seleccione **Obtener**. Se abrirá una página que muestra **AppSource** y **Aplicaciones para Power BI**.  

<!--    ![Choose apps from online services that you use.](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-online-services-get.png)-->
4. Seleccione **Aplicaciones** de la pestaña **Aplicaciones para Power BI** y elija la aplicación **Microsoft Dynamics 365 Business Central** que desee usar; a continuación, seleccione **Obtener ahora**.  
<!--    ![Select Dynamics 365 Business Central and select Get it now](./media/across-how-to-connect-powerbi-d365-content-packspowerbi-dynamics365-for-financials-get-it-now.png)/-->
5. Cuando se le solicite, introduzca el nombre del ambiente y de la empresa en su aplicación de [!INCLUDE[prodshort](includes/prodshort.md)] a la que desee conectarse. Si no ha creado varios ambientes, introduzca **Producción**. Para el parámetro de empresa, asegúrese de introducir el nombre y no el nombre para mostrar. Puede encontrar el nombre de la empresa en la página **Empresas** en su instancia de [!INCLUDE[prodshort](includes/prodshort.md)].  

    > [!NOTE]
    > Si se conecta a [!INCLUDE [prodshort](includes/prodshort.md)] local, debe especificar el parámetro *URL de servicio web*. Puede encontrarlo en la página **Servicios web** en [!INCLUDE [prodshort](includes/prodshort.md)]. Su instancia de [!INCLUDE [server](includes/server.md)] debe estar configurada para la autenticación Básica y debe especificar un usuario y la clave de acceso web de ese usuario como su contraseña. En el siguiente ejemplo, reemplace *myserver:7048* por su nombre de [!INCLUDE [server](includes/server.md)] y *CRONUS%20US* por el nombre de su empresa.  
    > ```https://myserver:7048/BC140/ODataV4/Company('CRONUS%20US')/```

6. Una vez conectado, se añaden un panel e informes a su área de trabajo de Power BI. Cuando se haya completado, se muestran los mosaicos con datos de su empresa de [!INCLUDE[prodshort](includes/prodshort.md)].

    ![Seleccione Dynamics 365 Business Central y Obtener ahora](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-workspace-dashboard-report-dataset.png)

### <a name="what-now"></a>¿Y ahora qué?

- Intente [hacer una pregunta en el cuadro de preguntas](/power-bi/service-q-and-a-tips) en la parte superior del escritorio.
- [Cambie los mosaicos](/power-bi/service-dashboard-edit-tile) en el escritorio.  
- [Seleccione un mosaico](/power-bi/service-dashboard-tiles) para abrir el informe subyacente.  
- De forma predeterminada, su conjunto de datos no está programado para actualizarse. Puede cambiar la programación de actualización o intentar actualizarlo a petición utilizando **Actualizar ahora**. Para obtener más información, vea [Configuración de actualización programada](/power-bi/refresh-scheduled-refresh).

## <a name="power-bi-in-include-prodshortincludesprodshortmd"></a>Power BI en [!INCLUDE [prodshort](includes/prodshort.md)]

Su página Web en [!INCLUDE [prodshort](includes/prodshort.md)] puede incluir un elemento de control de Power BI que se puede configurar para mostrar informes de Power BI en su página Web.

> [!IMPORTANT]
> Debe disponer de una cuenta válida con [!INCLUDE [prodshort](includes/prodshort.md)] y con Power BI. Además, si desea modificar cualquier informe, debe descargar Power BI Desktop. Para obtener más información, consulte [Usar Business Central como origen de datos de Power BI](across-how-use-financials-data-source-powerbi.md).  

### <a name="on-first-login"></a>En el primer inicio de sesión

Cuando inicie sesión por primera vez en [!INCLUDE [prodshort](includes/prodshort.md)], verá una parte de Power BI vacía en su página Web. Para ver los informes, primero debe conectarse a Power BI seleccionando el vínculo *Introducción a Power BI*.

A continuación, [!INCLUDE [prodshort](includes/prodshort.md)] se comunica con el servicio de Power BI para determinar si tiene una cuenta de Power BI válida. Una vez verificada la licencia, se mostrarán los informes de Power BI predeterminados en su página Web.

### <a name="selecting-power-bi-reports"></a>Selección de informes de Power BI

El control de Power BI de su página Web puede mostrar cualquier informe de Power BI. Para ver un informe existente, seleccione la acción **Seleccionar informe** de la lista desplegable de comandos de Power BI.  

La página de selección de informes muestra una lista de todos los informes de Power BI a los que tiene acceso. Esta lista se recupera desde su área de trabajo de Power BI. Habilite cada informe que desee visualizar en la página Web y, a continuación, seleccione Aceptar. Volverá a su página Web y aparecerá el último informe que haya habilitado. Con la lista desplegable de comandos, utilice el comando anterior y el siguiente para navegar entre informes.  

### <a name="get-reports"></a>Obtener informes

Si no ve ningún informe en la página Seleccionar informes o no ve el informe que desea. Puede elegir entre obtener informes de *Mi organización* o de *Servicios*.
Seleccione *Mi organización* para ir a los servicios de Power BI donde puede ver los informes dentro de su organización de los que ha tenido derecho a ver y añádalos a su espacio de trabajo. Elija *Servicios* para ir a Microsoft AppSource donde pueda instalar aplicaciones de Power BI.  

También puede optar por crear nuevos informes de Power BI. Una vez que esos informes se publiquen en su espacio de trabajo de Power BI, aparecerán en esta página.  

### <a name="managing-reports"></a>Administrar informes

En la sección Power BI de su página Web, puede elegir la acción **Administrar informe** de la lista desplegable de comandos para poder modificar el informe que se centraba en el área de trabajo.  

Se pueden hacer modificaciones al informe y guardarlas.  Cualquier cambio realizado en el informe se modificará para cualquier usuario con el que se comparta este informe, ya que está modificando el informe almacenado en el servicio Power BI.  

Una vez que haya completado los cambios, seleccione Guardar. Si se trata de un informe compartido, es recomendable que seleccione Guardar como para evitar realizar este cambio para todos los usuarios.
Regrese al área de trabajo y aparecerá el informe actualizado. Si ha ejecutado un comando Guardar como, deberá abrir la página de selección de informe y habilitar el nuevo informe.

### <a name="uploading-reports"></a>Carga de informes

Puede cargar nuevos informes de Power BI y compartirlos con todos los usuarios de su [!INCLUDE [prodshort](includes/prodshort.md)]. Los informes se comparten dentro de cada empresa en [!INCLUDE [prodshort](includes/prodshort.md)].  

Para cargar un informe, seleccione la acción **Cargar informe** de la lista desplegable de comandos. A continuación, puede cargar un archivo .pbix que defina los informes que desea compartir. Puede cambiar el nombre predeterminado del archivo.  

Una vez que el informe se ha cargado en su espacio de trabajo de Power BI, se carga automáticamente en los espacios de trabajo de Power BI de los demás usuarios de esa empresa en el siguiente inicio de sesión en [!INCLUDE [prodshort](includes/prodshort.md)].

## <a name="system-requirements"></a>Requisitos del sistema

Para importar los datos de [!INCLUDE[prodshort](includes/prodshort.md)] en Power BI, debe tener permisos para los servicios web utilizados para recuperar datos. Los servicios web necesarios para cada aplicación de Power BI incluyen:

### <a name="microsoft-dynamics-365-business-central--crm"></a>Microsoft Dynamics 365 Business Central – CRM

- Oportunidades de venta
- Plantilla de empresa de vista de plantilla de Excel
- Etiquetas de informe del Power BI

### <a name="microsoft-dynamics-365-business-central--finance"></a>Microsoft Dynamics 365 Business Central – Finance

- PowerBIFinance
- Plantilla de empresa de vista de plantilla de Excel
- Etiquetas de informe del Power BI

### <a name="microsoft-dynamics-365-business-central---sales"></a>Microsoft Dynamics 365 Business Central - Sales

- Ventas de productos por cliente
- Panel de ventas
- Empresa de vista de plantilla de Excel
- Etiquetas de informe del Power BI

> [!NOTE]
> [!INCLUDE [prodshort](includes/prodshort.md)] local utiliza los mismos puntos finales de servicio web que [!INCLUDE [prodshort](includes/prodshort.md)] en línea.

## <a name="web-services"></a>Servicios Web

Un modo de fácil de encontrar los servicios web es buscar *servicios web* en [!INCLUDE[prodshort](includes/prodshort.md)]. En la página de **Servicios web**, asegúrese de que el campo **Publicar** esté seleccionado para los servicios web enumerados más arriba.

## <a name="troubleshooting"></a>Solución de problemas

El panel de Power BI depende de los servicios web publicados que aparecen en la lista anterior y mostrará los datos de la empresa de demostración o de la suya propia si importa los datos de la solución de finanzas actual. Sin embargo, si se produce algún error, en esta sección se proporcionará una solución para los problemas más habituales.  

### <a name="you-do-not-have-a-power-bi-account"></a>No tiene una cuenta de Power BI

No se ha configurado una cuenta de Power BI. Para tener una cuenta de Power BI válida, debe tener una licencia y debe haber iniciado sesión previamente en Power BI, para que se haya creado su espacio de trabajo de Power BI.  

### <a name="message-there-are-no-enabled-reports-choose-select-report-to-see-a-list-of-reports-that-you-can-display"></a>Mensaje: No hay informes habilitados. Elija Seleccionar informe para ver una lista de informes que se pueden visualizar.

Este mensaje aparecerá si el informe predeterminado no se ha podido implementar en su espacio de trabajo de Power BI o el informe implementado pero no se ha actualizado correctamente. Si esto sucede, navegue hasta el informe en su espacio de trabajo de Power BI, seleccione **Conjunto de datos**, **Configuración** y luego actualice manualmente las credenciales. Una vez que el conjunto de datos se actualice correctamente, vuelva a Business Central y seleccione manualmente el informe desde la página **Seleccionar informes**. 

### <a name="you-need-a-power-bi-pro-license-to-install-the-include-prodshortincludesprodshortmd-app-in-power-bi"></a>Necesita una licencia Power BI Pro para instalar la aplicación de [!INCLUDE [prodshort](includes/prodshort.md)] en Power BI

Las aplicaciones de Power BI solo las pueden instalar usuarios que tengan una licencia Power BI Pro. Una vez instalada la aplicación de Power BI, puede compartirla con usuarios que no tengan una licencia Power BI Pro.  

### <a name="parameter-validation-failed-please-make-sure-all-parameters-are-valid"></a>"Error en la validación de parámetros, asegúrese de que todos los parámetros sean válidos"

Este error indica que uno o varios de los parámetros no son válidos.

- El parámetro de ambiente especificado no coincide con ningún ambiente de producción o aislado de [!INCLUDE [prodshort](includes/prodshort.md)] existente. 
- El parámetro de empresa especificado no coincide con ninguna empresa de [!INCLUDE [prodshort](includes/prodshort.md)] existente. Verifique el nombre de la empresa en la página **Empresas** en [!INCLUDE [prodshort](includes/prodshort.md)].
- Si se conecta a [!INCLUDE [prodshort](includes/prodshort.md)] local. ha introducido una URL que no es válida. Puede verificar la URL en la página de **Servicios web** en [!INCLUDE [prodshort](includes/prodshort.md)]  
- Un puerto no está abierto para permitir que la petición pase a través de su firewall.

### <a name="login-failed"></a>Error de inicio de sesión

Si obtiene un "error de inicio de sesión" después de usar sus credenciales de usuario de [!INCLUDE [prodshort](includes/prodshort.md)] para iniciar sesión, es probable que esté experimentando uno de los siguientes problemas:

- La cuenta que usa no tiene permisos para recuperar los datos de [!INCLUDE [prodshort](includes/prodshort.md)] de su cuenta. Compruebe que tiene permisos para introducir los datos necesarios en [!INCLUDE [prodshort](includes/prodshort.md)] e inténtelo de nuevo.
- Ha seleccionado un tipo de autenticación distinto de Básico si se conecta con [!INCLUDE [prodshort](includes/prodshort.md)]local.
- No ha introducido un nombre de usuario o una contraseña válidos.

### <a name="incorrect-company-name"></a>Nombre de empresa incorrecto

Un error común es introducir el nombre para mostrar de empresa en lugar del nombre de la empresa. Para buscar el nombre de la empresa, busque **Empresas**. A continuación, use el campo **Nombre** al introducir el nombre de su empresa.

### <a name="the-key-didnt-match-any-rows-in-the-table"></a>La clave no coincidía con ninguna fila de la tabla

Si introduce un nombre de empresa no válido durante el proceso de conexión, puede recibir el mensaje de error "La clave no coincidió con ninguna fila de la tabla". Proporcione el nombre correcto de la empresa e intente conectarse de nuevo.

### <a name="historical-data-appears-to-be-missing"></a>Parece que faltan datos históricos

Una vez que la aplicación de Power BI está instalada y sus datos aparezcan en Power BI, puede observar que no se muestran todos sus datos. Los conjuntos de datos se filtran para que solo se devuelvan los datos de los 365 días anteriores. Este valor predeterminado se utiliza para ayudar a que los informes sean más rápidos.  

### <a name="i-only-see-data-for-a-single-company"></a>Solo veo datos de una sola empresa

La aplicación de Power BI solo mostrará los datos de la empresa de [!INCLUDE [prodshort](includes/prodshort.md)] que se definió cuando se instaló la aplicación de Power BI. Los datos de empresas adicionales se pueden añadir a los informes añadiendo nuevas consultas que utilizan empresas diferentes como origen de datos.  

## <a name="see-also"></a>Consulte también

[Power BI para consumidores](/power-bi/consumer/end-user-consumer)  
[El nuevo aspecto del servicio Power BI](/power-bi/service-new-look)  
[Inicio rápido: Conectarse a los datos de Power BI Desktop](/power-bi/desktop-quickstart-connect-to-data)  
[Documentación de Power BI](/power-bi/)  
[Inteligencia empresarial](bi.md)  
[Introducción](product-get-started.md)  
[Importar datos de empresa de otros sistemas financieros](across-import-data-configuration-packages.md)  
[Configurar [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)  
[Usar [!INCLUDE[d365fin](includes/d365fin_md.md)] como origen de datos de Power BI](across-how-use-financials-data-source-powerbi.md)  
[Usar [!INCLUDE[d365fin](includes/d365fin_md.md)] como origen de datos de Power Apps](across-how-use-financials-data-source-powerapps.md)  
[Usar [!INCLUDE[d365fin](includes/d365fin_md.md)] en Power Automate](across-how-use-financials-data-source-flow.md)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
