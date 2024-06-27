---
title: Trabajar con informes de Power BI en Business Central | Documentos de Microsoft
description: 'Obtener información, inteligencia empresarial y KPI de los datos de Business Central con Power BI.'
author: jswymer
ms.topic: get-started
ms.devlang: al
ms.search.keywords: 'account schedule, analysis, reporting, financial report, business intelligence, KPI'
ms.date: 04/24/2024
ms.author: jswymer
ms.service: dynamics-365-business-central
ms.reviewer: jswymer
---
# Trabajar con informes de Power BI en [!INCLUDE [prod_short](includes/prod_short.md)]

En este artículo, aprenderá algunos de los conceptos básicos sobre el trabajo con informes. Esto incluye ver informes de Power BI dentro de [!INCLUDE [prod_short](includes/prod_short.md)] (incluidos cuadros de mando y paneles) y editar informes de Power BI que utilizan [!INCLUDE [prod_short](includes/prod_short.md)] como origen de datos. El artículo analiza algunos aspectos que lo ayudarán a comenzar como usuario de [!INCLUDE[prod_short](includes/prod_short.md)]. Para obtener pautas generales e instrucciones sobre el uso de Power BI, ver [Documentación de Power BI para consumidores](/power-bi/consumer).

## Información general

Los informes de Power BI le brindan información sobre su [!INCLUDE[prod_short](includes/prod_short.md)]. Varias páginas en [!INCLUDE [prod_short](includes/prod_short.md)] incluyen una parte de informes de Power BI que puede mostrar informes de Power BI. El centro de roles es una página típica en la que verá una parte de informes de Power BI. Algunas páginas de lista, como **Artículos**, también incluye una parte de Power BI.

[!INCLUDE [prod_short](includes/prod_short.md)] funciona con con el servicio de Power BI. Los informes para mostrar en [!INCLUDE [prod_short](includes/prod_short.md)] se almacenan en un servicio de Power BI. En [!INCLUDE [prod_short](includes/prod_short.md)], puede cambiar el informe que se muestra en la parte de Power BI a cualquier informe de Power BI disponible en su servicio de Power BI. La primera vez que inicia sesión en [!INCLUDE [prod_short](includes/prod_short.md)] y hasta que se conecta a un servicio de Power BI, las partes estarán vacías, como se muestra aquí:

![Parte de Power BI en Business Central.](./media/power-bi-part.png)

## Introducción

> [!NOTE]
> [!INCLUDE [prod_short](includes/prod_short.md)] online ya está configurado para integrarse con Power BI.

### Registrarse en Power BI

Antes de que pueda usar Power BI con [!INCLUDE[prod_short](includes/prod_short.md)], deberá registrarse en el servicio de Power BI. Si aún no se ha registrado, vaya a [https://powerbi.microsoft.com](https://powerbi.microsoft.com). Cuando se registre, use su dirección de correo electrónico y contraseña del trabajo.

Una vez que tenga una cuenta de Power BI, puede iniciar sesión en [https://powerbi.microsoft.com/](https://powerbi.microsoft.com/).

El servicio de Power BI aloja todos los informes disponibles. Para ver un informe en su espacio de trabajo personal, seleccione **Mi espacio de trabajo** > **Informes**. Luego, seleccione el informe que desea ver. Si tiene acceso a uno o más espacios de trabajo de Power BI compartidos, también puede ver informes en esos espacios de trabajo.

Con [!INCLUDE[prod_short](includes/prod_short.md)] Online, automáticamente tendrá un conjunto de informes predeterminados en su espacio de trabajo. Si desea crear sus propios informes, puede utilizar Power BI Desktop para crear informes y luego publicarlos en su espacio de trabajo. Para más información, ver [Introducción a la creación de informes en Power BI Desktop para mostrar datos de [!INCLUDE [prod_long](includes/prod_long.md)]](across-how-use-financials-data-source-powerbi.md).

[!INCLUDE[note-multicompany-reports](includes/note-multicompany-reports.md)]

## <a name="connect"></a>Conectar a Power BI, solo una vez

Cuando inicia sesión por primera vez en [!INCLUDE [prod_short](includes/prod_short.md)], lo más probable es que vea una parte de Power BI vacía (como se muestra en la figura anterior) en varias páginas. Lo primero que debe hacer es conectarse a su cuenta de Power BI. Una vez conectado, puede ver los informes. Solo tiene que hacer este paso una vez.

1. Seleccione el vínculo **Introducción a Power BI** en la parte **Informes de Power BI**.
2. Se inicia la configuración asistida **Configurar informes de Power BI en Business Central**. Seleccione **Siguiente** para continuar.
3. En la página **Comprobar la licencia de Power BI**. Realice uno de los siguientes pasos:

    - Si aún no se ha registrado en Power BI, seleccione [Ir a la página de inicio de Power BI](https://powerbi.microsoft.com). Regístrese para tener una cuenta, luego regrese a [!INCLUDE[prod_short](includes/prod_short.md)] y termine la configuración.

    - Si ya tiene una licencia, seleccione **Siguiente**.
4. En la página siguiente, [!INCLUDE[prod_short](includes/prod_short.md)] ahora cargará un informe de demostración en Power BI. Este paso tardará unos minutos, así que se realiza en segundo plano. Para completar la configuración, seleccione **Siguiente** y luego **Terminar**.

Comienza el proceso de conexión. Durante el proceso, [!INCLUDE [prod_short](includes/prod_short.md)] se comunica con el servicio de Power BI para determinar si tiene una cuenta y licencia de Power BI. Una vez verificada la licencia, se mostrarán el informe de Power BI predeterminado en la página. Si no se muestra un informe, puede seleccionar un informe de la parte.

> [!TIP]
> Con [!INCLUDE [prod_short](includes/prod_short.md)] Online, este paso cargará automáticamente de manera predeterminada los informes de Power BI utilizados en [!INCLUDE [prod_short](includes/prod_short.md)] para su espacio de trabajo de Power BI.

<!--#### From [!INCLUDE [prod_short](includes/prod_short.md)] on-premises

Connecting to Power BI from [!INCLUDE [prod_short](includes/prod_short.md)] is similar to online. However, you might be prompted on the **MICROSOFT ENTRA SERVICE PERMISSIONS** page to grant access to Power BI Services. To grant access, select **Authorize Azure Services**, and then **Accept**.

Once connected, you can select a report from the Power BI part on pages.-->

## Trabajar con informes de Power BI

### Obtener los datos más recientes

Cada informa de Power BI se basa en un conjunto de datos que obtiene datos de los orígenes de [!INCLUDE[prod_short](includes/prod_short.md)]. Quiere asegurarse de que los datos de sus informes de  Power BI están actualizados con los datos de [!INCLUDE[prod_short](includes/prod_short.md)]. Este concepto se conoce como *actualización*.  Dependiendo de cómo haya configurado su organización Power BI, es posible que la actualización no se realice automáticamente. Hay dos formas de actualizar los datos: manualmente o programando una actualización. La actualización manual se realiza a pedido, según sea necesario. La actualización programada le permite actualizar automáticamente a intervalos de tiempo definidos.

#### Actualizar manualmente

En Power BI en línea, en el panel de navegación, bajo **Conjuntos de datos**, seleccione **Más opciones (...)** al lado del conjunto de datos y, a continuación, seleccione **Actualizar ahora**.

#### Programe una actualización

En Power BI en línea, en el panel de navegación, debajo de Conjuntos de datos, seleccione Mas opciones (...) junto al conjunto de datos, luego seleccione **Programar actualización**. Complete la información debajo de la sección **Programar actualización** y seleccione **Aplicar**.

Para obtener más información, vea [Configurar actualización programada](/power-bi/connect-data/refresh-scheduled-refresh)

### Mostrar informes en páginas de lista

[!INCLUDE[prod_long](includes/prod_long.md)] incluye un cuadro informativo de Power BI en varias páginas de lista clave. Este cuadro informativo proporciona información extra sobre los datos de la lista. A medida que se desplaza por las filas de la lista, el informe se actualiza y se filtra para la entrada seleccionada.

Para aprender a crear informes para páginas de lista, consulte [Crear informes de Power BI para mostrar datos de lista en [!INCLUDE[prod_short](includes/prod_short.md)]](across-how-use-powerbi-reports-factbox.md).

> [!TIP]
> Si no ve el cuadro informativo de Power BI, podría estar oculto en su espacio de trabajo por personalización. Seleccione la ![Configuración.](media/ui-experience/settings_icon_small.png "Icono de configuración para el área de trabajo") , y luego la acción **Personalizar**. Para obtener más información, consulte [Personalizar el área de trabajo](ui-personalization-user.md).
>
> O si tiene una versión anterior de Business Central, vaya a la barra de acción, seleccione **Comportamiento** > **Monitor** > **Mostrar/ocultar Informes de Power BI**.

### Cambiar informes

Una parte de Power BI en una página puede mostrar cualquier informe de Power BI que esté disponible para usted. Para cambiar y ver otro informe, elija la acción **Seleccionar informe** en la lista de comandos desplegable en la parte superior de la parte.  

La página **Selección de informes de Power BI** muestra una lista de todos los informes de Power BI a los que tiene acceso. Esta lista se recupera de cualquiera de sus propias áreas de trabajo o áreas de trabajo que se hayan compartido con usted en el servicio de Power BI. Seleccione la casilla **Habilitar** para cada informe que desee visualizar en la página y, a continuación, seleccione **Aceptar**. Volverá a su página Web y aparecerá el último informe que haya habilitado. Con la lista desplegable de comandos, utilice el comando **Anterior** y **Siguiente** para navegar entre informes.  

### Obtener más informes

Si no ve ningún informe en la página **Selección de informes de Power BI** o no ve el informe que desea, elija **Obtener informes**. Esta acción le permite buscar informes en dos ubicaciones: *Mi Organización* o *Servicios*.

- Elija **Mi Organización** para ir a los servicios de Power BI. Desde aquí, puede ver los informes de su organización para los que se le han otorgado derechos para ver. Luego puede agregarlos a su espacio de trabajo.
- Elija **Servicios** para ir a Microsoft AppSource donde pueda instalar aplicaciones de Power BI.  

> [!TIP]
> Si tiene Power BI Desktop, también puede crear nuevos informes de Power BI. Entonces, una vez que esos informes se publiquen en su espacio de trabajo de Power BI, aparecerán en la página página **Selección de informes de Power BI**.  

### Gestionar y modificar informes

Puede realizar cambios en un informe en la parte de Power BI. Los cambios que realice se publicarán en el servicio de Power BI. Si el informe se comparte con otros usuarios, también verán los cambios, a menos que guarde los cambios en un nuevo informe.

Para modificar un informe, seleccione la acción **Gestionar informe** en la lista desplegable de comandos de la parte de Power BI. Entonces comience a hacer cambios. Una vez que termine de hacer cambios, seleccione **Archivo** > **Guardar**. Si es un informe compartido y no desea realizar el cambio para todos los usuarios, seleccione **Guardar como** para evitar realizar este cambio para todos los usuarios.

Al regresar al área de trabajo, aparecerá el informe actualizado. Si usó **Guardar como**, tendrá que elegir **Seleccionar informe** y luego habilitar el nuevo informe para verlo.

> [!NOTE]
> Esta capacidad no está disponible con [!INCLUDE [prod_short](includes/prod_short.md)] local.

### <a name="upload"></a>Cargar informes

Los informes de Power BI se pueden distribuir entre los usuarios como archivos .pbix. Si tiene archivos .pbix, puede cargarlos y compartirlos con todos los usuarios de [!INCLUDE [prod_short](includes/prod_short.md)]. Los informes se comparten dentro de cada empresa en [!INCLUDE [prod_short](includes/prod_short.md)].  

Para cargar un informe, seleccione la acción **Cargar informe** de la lista desplegable de comandos en la parte **Informes de Power BI**. A continuación, localice el archivo .pbix que defina los informes que desea compartir. Puede cambiar el nombre predeterminado del archivo.  

Después de que el informe se cargue en su espacio de trabajo de Power BI, se carga automáticamente en los espacios de trabajo de Power BI de otros usuarios.

> [!NOTE]
> Cargar un informe mediante [!INCLUDE[prod_short](includes/prod_short.md)] requiere que tenga permisos de usuario SUPER en [!INCLUDE[prod_short](includes/prod_short.md)]. No necesita ningún permiso especial para cargar informes en su espacio de trabajo a través del servicio de Power BI.

## <a name="upload"></a>Cargar informes desde archivos

Los informes de Power BI se pueden distribuir entre los usuarios como archivos .pbix. Si tiene un archivo .pbix, puede cargarlo en un espacio de trabajo. Para cargar un informe, siga los siguientes pasos:

1. En su nuevo espacio de trabajo, seleccione **Obtener datos**.

2. En el cuadro Archivos, seleccione **Obtener**.

3. Seleccione **Archivo local**, navegue hasta donde guardó el archivo y seleccione **Abierto**.

Para más información, ver [Sube el informe al servicio](/power-bi/paginated-reports/paginated-reports-quickstart-aw#upload-the-report-to-the-service).

<!--
> [!NOTE]
> Uploading a report requires that you have a [Premium capacity](/power-bi/service-premium-what-is) work space. For more information, see [Managing Premium capacities](/power-bi/admin/service-premium-capacity-manage). -->

> [!TIP]
> Si está usando [!INCLUDE[prod_short](includes/prod_short.md)] online, también puede cargar un informe desde [!INCLUDE[prod_short](includes/prod_short.md)]. Para más información, ver [Trabajar con informes de Power BI en [!INCLUDE [prod_short](includes/prod_short.md)] - Subir informes](across-working-with-powerbi.md#upload).

## <a name="share"></a>Compartir informes con otros

Una vez que un informe está en su espacio de trabajo, puede compartirlo con otras personas de su organización.

Para compartir un informe, en una lista de informes o en un informe abierto, seleccione **Compartir**. En el panel **Compartir informe**, ingrese las direcciones de correo electrónico completas de las personas o grupos de distribución con los que desea compartir. Siga las instrucciones en pantalla para completar el intercambio. Para más información, ver [Compartir un panel o informe.](/power-bi/collaborate-share/service-share-dashboards#share-a-dashboard-or-report).

> [!NOTE]
> Es necesario que tanto usted como las personas con las que comparte el informe tengan una [licencia Pro de Power BI](/power-bi/service-features-license-type). De lo contrario, el contenido debe tener [capacidad Premium](/power-bi/service-premium-what-is). Para más información, vea [Formas de compartir el trabajo en Power BI](/power-bi/service-how-to-collaborate-distribute-dashboards-reports).

## Solucionar problemas

Sin embargo, si se produce algún error, en esta sección se proporcionará una solución para los problemas más habituales.  

### No tiene una cuenta de Power BI

No se ha configurado una cuenta de Power BI. Para obtener una cuenta de Power BI válida, debe tener una licencia y debe haber iniciado sesión previamente en Power BI, para crear un espacio de trabajo de Power BI.

### Mensaje: No hay informes habilitados. Elija Seleccionar informe para ver una lista de informes que se pueden visualizar.

Este mensaje aparece si el informe predeterminado no se pudo implementar en su espacio de trabajo de Power BI. O se implementó pero no se actualizó correctamente. Navegue hasta el informe en su espacio de trabajo de Power BI, seleccione **Conjunto de datos**, **Configuración** y luego actualice manualmente las credenciales. Una vez que el conjunto de datos se actualice correctamente, vuelva a [!INCLUDE[prod_short](includes/prod_short.md)] y seleccione manualmente el informe desde la página **Seleccionar informes**.

#### No puede ver un informe en la página Seleccionar informe en una página de lista

Probablemente se deba a que el nombre del informe no contiene el nombre de la página de la lista. Borre el filtro para obtener una lista completa de los informes de Power BI disponibles.

## Consulte también

[Business Central y Power BI](admin-powerbi.md)    
[Crear informes de Power BI para mostrar datos de [!INCLUDE [prod_long](includes/prod_long.md)]](across-how-use-financials-data-source-powerbi.md)    
[Componente de integración de Power BI e información general de la arquitectura para [!INCLUDE[prod_short](includes/prod_short.md)]](admin-powerbi-overview.md)    
[Conectarse a Power BI desde [!INCLUDE [prod_short](includes/prod_short.md)] local](across-working-with-business-central-in-powerbi.md)    
[Power BI para consumidores](/power-bi/consumer/end-user-consumer)     
[El nuevo aspecto del servicio de Power BI](/power-bi/service-new-look)    
[Inicio rápido: Conectarse a los datos de Power BI Desktop](/power-bi/desktop-quickstart-connect-to-data)    
[Documentación de Power BI](/power-bi/)    
[Inteligencia empresarial](bi.md)    
[Preparación para hacer negocios](ui-get-ready-business.md)    
[Importar datos de empresa de otros sistemas financieros](across-import-data-configuration-packages.md)    
[Configurar [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md)    
[Usar [!INCLUDE[prod_short](includes/prod_short.md)] como origen de datos de Power BI](across-how-use-financials-data-source-powerapps.md)    
[Usar [!INCLUDE[prod_short](includes/prod_short.md)] como origen de datos de Power Apps](across-how-use-financials-data-source-powerapps.md)    
[Usar [!INCLUDE[prod_short](includes/prod_short.md)] en Power Automate](across-how-use-financials-data-source-flow.md)  




[!INCLUDE[footer-include](includes/footer-banner.md)]
