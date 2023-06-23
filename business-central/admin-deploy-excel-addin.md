---
title: Obtener el complemento Business Central para Excel
description: Obtenga información sobre cómo obtener para los usuarios el complemento Business Central para Excel.
author: jswymer
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.search.form: 1480
ms.search.keywords: 'Excel, add-in, centralized deployment, M365 admin center, individual acquisition, appsource'
ms.date: 10/07/2021
ms.author: jswymer
---
# <a name="get-the-business-central-add-in-for-excel" />Obtener el complemento Business Central para Excel

[!INCLUDE[prod_short](includes/prod_short.md)] incluye un complemento para Excel que permite a los usuarios seleccionar una acción **Editar en Excel** en determinadas páginas para abrir los datos en una hoja de cálculo de Excel. Esta acción es diferente a la acción **Abrir en Excel** porque permite a los usuarios realizar cambios en Excel y luego publicar los cambios en [!INCLUDE[prod_short](includes/prod_short.md)]

## <a name="overview" />Información general

### <a name="about-the-add-in" />Acerca del complemento

El complemento se llama **Complemento de Office de Microsoft Dynamics** y está disponible para su instalación desde la [Tienda Office (AppSource)](https://appsource.microsoft.com/). Con el complemento instalado, la acción **Editar en Excel** está disponible en la mayoría de las páginas de listas y de partes de listas desde el icono **Compartir** ![Compartir una página en otra aplicación.](media/share-icon.png). Para obtener más información sobre el uso del complemento, consulte [Ver y editar en Excel desde Business Central](across-work-with-excel.md).

> [!NOTE]
> El complemento solo funciona en Windows; no en macOS.

### <a name="about-deployment-as-an-admin" />Acerca de la implementación como administrador

Con [!INCLUDE[prod_short](includes/prod_short.md)] en línea, existen algunas opciones de implementación para proporcionar el complemento a los usuarios. Una opción es *adquisición individual*, que permite que los usuarios instalen el complemento ellos mismos. Con esta opción, los usuarios deben tener acceso a la descarga de archivos desde Office Store. Otra opción es configurar *Despliegue centralizado* en el Centro de administración de Microsoft 365 para implementar automáticamente el complemento en toda la organización, grupos o usuarios específicos. La implementación centralizada proporciona una forma de hacer llegar el complemento a los usuarios si su organización no les da acceso a la tienda Office.

Para el usuario final, la experiencia de instalación es diferente para los dos escenarios de implementación:

- Con la adquisición individual, los nuevos usuarios eligen la acción **Editar en Excel**, el panel **Nuevo complemento de Office** se abre en Excel. Para instalar el complemento, el usuario elige **Confía en este complemento**, que a su vez instala el complemento directamente desde la Tienda Office. Luego, los usuarios inician sesión en [!INCLUDE[prod_short](includes/prod_short.md)] utilizando su nombre de usuario y contraseña.

- Con Implementación centralizada, los nuevos usuarios eligen la acción **Editar en Excel**, el complemento se instala automáticamente en Excel desde Implementación centralizada; no la Tienda Office. Lo único que tienen que hacer los usuarios es iniciar sesión en [!INCLUDE[prod_short](includes/prod_short.md)]

Con estas dos opciones de implementación, el complemento se configura automáticamente para conectarse a [!INCLUDE[prod_short](includes/prod_short.md)]. Una tercera opción de implementación es una instalación manual del complemento directamente desde Excel. Con esta opción, los usuarios deberán configurar el complemento para conectarse a [!INCLUDE[prod_short](includes/prod_short.md)]

### <a name="a-nameswitchaswitching-from-individual-acquisition-to-centralized-deployment-or-the-other-way-around" /><a name="switch"></a>Cambiar de adquisición individual a Implementación centralizada o a la inversa

Cuando cambia de adquisición individual del complemento a Implementación centralizada, o viceversa, los archivos de Excel que los usuarios crearon antes de la transición se ven afectados. Después de la transición, los usuarios pueden seguir abriendo cualquier hoja de cálculo de Excel creada previamente usando la acción **Editar en Excel** o creada manualmente mediante la configuración del complemento de Excel. Pero no pueden actualizar los datos en el archivo desde Business Central o insertar actualizaciones a Business Central

Esta condición se debe al hecho de que a cada archivo de Excel se le asigna un identificador de "complemento". En la transición hacia o desde Implementación centralizada, se asigna un identificador diferente, por lo que el identificador anterior se bloquea.

## <a name="preparation-on-premises-only" />Preparación (solo local)

[!INCLUDE[prod_short](includes/prod_short.md)] local requiere que su entorno esté configurado para el complemento. Si no, la acción **Editar en Excel** no estará disponible para los usuarios. Para más información, vea [Configuración del complemento de Excel para editar datos de Business Central](/dynamics365/business-central/dev-itpro/administration/configuring-excel-addin) en la ayuda para desarrolladores y profesionales de TI.

## <a name="deploy-the-add-in-by-using-centralized-deployment" />Implementar el complemento mediante Implementación centralizada

Implementación centralizada es una característica del Centro de administración de Microsoft 365 que se usa para instalar complementos automáticamente en las aplicaciones de Office de los usuarios, como Excel. Para ayudarlo con Implementación centralizada, [!INCLUDE[prod_short](includes/prod_short.md)] incluye la configuración asistida **Implementación centralizada complementos Excel**.

### <a name="before-you-begin" />Antes de empezar

- Para obtener información sobre cómo evitar que los usuarios descarguen desde la Tienda Office, consulte [Administrar complementos en el centro de administración](/microsoft-365/admin/manage/manage-addins-in-the-admin-center).
- Verifique que Implementación centralizada funcione para su organización. Para más información, vea [Determinar si Implementación centralizada de complementos funciona para su organización](/microsoft-365/admin/manage/centralized-deployment-of-add-ins)
- Si está realizando la transición desde adquisición individual, consulte [Cambio de adquisición individual a Implementación centralizada](#switch)

> [!NOTE]
> La habilitación de Implementación centralizada afecta a las funciones que utilizan el complemento de Excel, como la acción **Editar en Excel**. No tiene ningún efecto sobre otras funciones o permisos relacionados con Excel asignados a los usuarios en [!INCLUDE[prod_short](includes/prod_short.md)]

### <a name="set-up-centralized-deployment-of-the-add-in" />Configurar Implementación centralizada del complemento

Usted trabajará en [!INCLUDE[prod_short](includes/prod_short.md)] y el Centro de administración de Microsoft 365.

1. En [!INCLUDE[prod_short](includes/prod_short.md)], elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , entre en **Implementación centralizada complementos Excel**, luego elija el enlace relacionado.
2. Lea la información en la página **Configuración de complementos de Excel de Business Central** y elija **Siguiente**.
3. Inicie sesión en [Centro de administración de Microsoft 365](https://go.microsoft.com/fwlink/?linkid=2163967), y luego vaya a **Aplicaciones integradas**<!--**Add-ins**-->.

    Complete los siguientes pasos para configurar el complemento para implementar desde la Tienda Office: 
    1. Elija **Obtener aplicaciones** para abrir Office Store (AppSource). <!--**Deploy Add-in** 5. In the **Deploy a new add-in**, select **Choose from the store**.-->
    2. Busque **Complemento de Office de Microsoft Dynamics**, luego seleccione **Obtener ahora**. <!--On the **Select add-in** page, search for and select **Microsoft Dynamics Office Add-in** > **Add** > **Continue**.-->
    3. En la página **Agregar usuarios**, especifique los usuarios para los que desea implementar el complemento, luego elija **Siguiente**.<!--On the **Configure add-in**, specify the users that you want to deploy the add-in for.-->
    4. Revise **Aceptar solicitudes de permisos**, luego elija **Siguiente** > **Finalizar implementación**.
    5. Espere a que aparezca la marca de verificación verde junto a **Implementado** para el complemento, luego elija **Hecho**. <!--Select **Deploy** and wait til successful, then **Next** > **Continue**.-->

       El complemento aparece en la página **Complementos**. Para obtener más información sobre la implementación de complementos en el Centro de administración de Microsoft 365, consulte [Implementar complementos en el centro de administración](/power-platform/admin/use-service-admin-role-manage-tenant?azure-portal=true).
4. Vuelva a la configuración asistida de **Implementación centralizada de complementos de Excel** en [!INCLUDE[prod_short](includes/prod_short.md)] y elija **Siguiente**.
5. Active **Utilizar Implementación centralizada** y elija **Terminar**.

    Si no activa este conmutador, [!INCLUDE[prod_short](includes/prod_short.md)] obtendrá el complemento directamente de Tienda Office.

Cuando termine, siempre puede cambiar la implementación en el Centro de administración de Microsoft 365, como asignar más usuarios. Para obtener más información sobre la implementación de complementos en el Centro de administración, consulte [Implementar complementos en el centro de administración](/power-platform/admin/use-service-admin-role-manage-tenant?azure-portal=true).

> [!IMPORTANT]
> Si tiene más de un entorno, debe ejecutar la configuración asistida de **Implementación centralizada de complementos de Excel** en cada entorno en el que desee utilizar Implementación centralizada. Sin embargo, no es necesario que vuelva a configurar Implementación centralizada en Microsoft 365. Lo único que tiene que hacer es activar el conmutador **Utilizar Implementación centralizada** en la configuración asistida. 

> [!NOTE]
> Pueden pasar hasta 24 horas antes de que el complemento se implemente automáticamente en Excel de los usuarios.

## <a name="a-nameinstallaindividual-acquisition-install-the-add-in-manually-for-your-own-use" /><a name="install"></a>Adquisición individual: instale el complemento manualmente para su propio uso

En la mayoría de los casos, cuando abre Excel desde Business Central, el complemento se instalará automáticamente o se le pedirá que lo instale. Sin embargo, puede haber casos en los que tenga que instalar manualmente el complemento.

1. Abra Excel, luego abra cualquier libro de Excel.
2. En el menú **Insertar**, elija **Complementos** > **Obtener complementos**
3. Vaya a **Administrado por el administrador** y busque **Complemento de Office de Microsoft Dynamics**. Si lo ve, selecciónelo, luego elija **Agregar**. Si no lo ve, vaya a **Tienda**, luego busque *Complemento de Office de Microsoft Dynamics* y siga las instrucciones en pantalla para agregarlo.

Cuando se instala el complemento, aparece como un panel en Excel. A continuación, configure la conexión.

### <a name="configure-the-business-central-connection" />Configurar la conexión de Business Central

Si un usuario no puede conectarse automáticamente, puede desbloquearlo pidiéndole que siga estos pasos:

1. En el panel de complementos de **Microsoft Dynamics** en Excel, elija **Agregar información del servidor**. Si no lo ve, elija el icono ![Botón de opción Más en Excel.](media/cogwheel.png) en la parte superior para abrir el cuadro de diálogo de opciones. 
2. Para [!INCLUDE[prod_short](includes/prod_short.md)] en línea, configure **URL del servidor** como `https://exceladdinprovider.smb.dynamics.com`. Para [!INCLUDE[prod_short](includes/prod_short.md)] local, configúrelo como el URL del cliente web, como `https://myBCserver/190`.
3. Elija **Aceptar** y luego confirme que la aplicación se vuelva a cargar.
4. Cuando se le pida, inicie sesión con su nombre de usuario y contraseña de Business Central.
5. Opcionalmente, elija el entorno y la empresa a los que desea conectarse.

El complemento ahora está conectado a [!INCLUDE [prod_short](includes/prod_short.md)] y puede editar datos y publicar los cambios en [!INCLUDE [prod_short](includes/prod_short.md)].  

## <a name="prepare-devices-and-network-for-the-excel-add-in" />Prepare los dispositivos y la red para el complemento de Excel

Los servicios de red, como los servidores proxy o los firewalls, deben permitir el enrutamiento entre cada dispositivo cliente en el que está instalado el complemento y muchos puntos finales de servicio. Para obtener una lista de puntos finales, consulte [Preparar la red para el complemento de Excel](/dynamics365/business-central/dev-itpro/administration/configuring-network-for-addins).

## <a name="troubleshooting" />Solución de problemas

A veces, los usuarios tienen problemas con el complemento de Excel. Esta sección ofrece algunos consejos para desbloquear usuarios en determinadas circunstancias.

|Problema  |Solución o solución alternativa  |Comentarios  |
|---------|---------|---------|
|El complemento no se inicia <br><br>Por ejemplo, el usuario recibe el mensaje "Advertencia de complemento: este complemento ya no está disponible". al intentar usar el complemento. Este problema en particular puede ocurrir si la implementación centralizada está configurada correctamente, pero no se asignó acceso al usuario.|Compruebe si el complemento se implementa de forma centralizada. O verifique si el usuario no puede instalarlo localmente. | El administrador puede configurar Office para que los usuarios no puedan adquirir complementos. En esos casos, el administrador debe implementar el complemento de forma centralizada. Para más información, vea [Implementar complementos en el centro de administración](/microsoft-365/admin/manage/manage-deployment-of-add-ins?view=o365-worldwide&preserve-view=true).|
|Los datos no se cargan en Excel|Pruebe la conexión abriendo otra lista en Excel desde [!INCLUDE [prod_short](includes/prod_short.md)]. O abra el libro en Excel en un navegador.|Si el usuario ha especificado un nombre de empresa que contiene caracteres especiales, el complemento no se puede conectar. |
|Los datos no se pueden volver a publicar en [!INCLUDE [prod_short](includes/prod_short.md)].|Pruebe la conexión abriendo el libro en Excel en un navegador. |A veces, una extensión puede bloquear el trabajo de publicación. Si la página está extendida o personalizada, elimine las extensiones y vuelva a intentarlo.|
|Las fechas están mal  |Excel puede mostrar fechas y horas en un formato diferente que [!INCLUDE [prod_short](includes/prod_short.md)]. Esta situación no significa que sean incorrectos y los datos de [!INCLUDE [prod_short](includes/prod_short.md)] no se desorganizarán.|         |
|Para algunas páginas de lista, la edición de varias líneas en Excel provoca errores de forma constante. Esta condición puede ocurrir si las llamadas de OData incluyen FlowFields y campos fuera del control del repetidor.|En la página **Servicios web**, seleccione las casillas **Excluir FlowFields no editables** y **Excluir campos fuera del repetidor** para la página publicada. Al seleccionar estas casillas se excluyen los FlowFields y campos no editables del cálculo de eTag. |Estas casillas están ocultas de forma predeterminada. Para mostrarlas en la página **Servicios web**, use [personalización](/dynamics365/business-central/ui-personalization-user). |
|Los usuarios ya no pueden iniciar sesión en el complemento. Cuando intentan iniciar sesión, el proceso se detiene sin completarse.| Este problema puede deberse a una actualización que realizamos en el complemento, en algún momento de julio de 2022. Para obtener más información y una solución, consulte [Modificar la configuración del complemento de Excel para admitir la actualización de julio de 2022](/dynamics365/business-central/dev-itpro/administration/update-excel-addin-configuration).|Se aplica solo local a [!INCLUDE [prod_short](includes/prod_short.md)]|

<!--
## <a name="deploy-the-excel-add-in-for-business-central-online" />Deploy the Excel add-in for Business Central online

For [!INCLUDE [prod_short](includes/prod_short.md)] online, the administrator can deploy the add-in for all users. But users can also install the add-in themselves, provided they have permission to configure their Office experience.  

> [!TIP]
> In some organizations, administrators cannot deploy add-ins centrally. For more information, see [Determine if Centralized Deployment of add-ins works for your organization](/microsoft-365/admin/manage/centralized-deployment-of-add-ins?view=o365-worldwide&preserve-view=true).

### <a name="to-deploy-the-excel-add-in-for-all-users" />To deploy the Excel add-in for all users

1. As the administrator, sign in to the Microsoft commercial website and find the add-in at [https://appsource.microsoft.com/product/office/WA104379629](https://appsource.microsoft.com/product/office/WA104379629).
2. Choose the **Get it now** button.

    You'll be redirected to the Microsoft 365 admin center.
3. In the left panel, go to **Settings**, and then choose **Add-ins**.
4. In the **Configure add-in** pane, specify which users to grant access to the add-in.
5. Save your changes.


### <a name="to-add-the-excel-add-in-locally" />To add the Excel add-in locally

1. Open Excel, and then open any Excel workbook.
2. On the **Insert** menu, choose **Office Add-ins**, and then choose **Admin managed** or **Store** as appropriate.
3. Search for *Dynamics Office Add-In*, and then install the add-in.

When the add-in is installed, it shows up as a panel in Excel. Next, you must configure the connection.

> [!TIP]
> If the workbook is not automatically saved to the user's OneDrive, then recommend them to save all workbooks that they export from [!INCLUDE [prod_short](includes/prod_short.md)].When they open the workbook again, the connection is still available, so they do not have to configure the connection again.

> [!NOTE]
> In certain deployments, the administrator must configure network access to unblock the Excel add-in. For more information, see [Preparing Your Network for the Excel Add-In](configuring-network-for-addins.md).-->

## <a name="see-related-microsoft-trainingtrainingmodulesconfigure-powerbi-excel-dynamics-365-business-centralindex" />Consultar la [formación de Microsoft](/training/modules/configure-powerbi-excel-dynamics-365-business-central/index) relacionada

## <a name="see-also" />Consulte también

[Análisis de estados financieros en Microsoft Excel](finance-analyze-excel.md)  
[Trabajar con Business Central](ui-work-product.md)  
[Mejoras en la integración de Excel en el segundo lanzamiento de versiones 2 de 2019](/dynamics365-release-plan/2019wave2/dynamics365-business-central/enhancements-excel-integration)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
