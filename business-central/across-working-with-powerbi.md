---
title: Trabajar con informes de Power BI en Business Central | Documentos de Microsoft
description: Obtener información, inteligencia empresarial y KPI de los datos de Business Central con Power BI.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: account schedule, analysis, reporting, financial report, business intelligence, KPI
ms.date: 04/01/2021
ms.author: jswymer
ms.openlocfilehash: 7f2e2fe9719d25e13a33cf1943e7a054a70edffd
ms.sourcegitcommit: c11ad91a389ed72532f5513654fdc7909b20aed9
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/22/2021
ms.locfileid: "5935366"
---
# <a name="working-with-power-bi-reports-in-prod_short"></a>Trabajar con informes de Power BI en [!INCLUDE [prod_short](includes/prod_short.md)]

En este artículo, aprenderá algunos de los conceptos básicos sobre la visualización de informes de Power BI en [!INCLUDE [prod_short](includes/prod_short.md)].

## <a name="overview"></a>Panorama

Los informes de Power BI le brindan información sobre su [!INCLUDE[prod_short](includes/prod_short.md)]. Varias páginas en [!INCLUDE [prod_short](includes/prod_short.md)] incluyen una parte de informes de Power BI que puede mostrar informes de Power BI. El centro de roles es una página típica en la que verá una parte de informes de Power BI. Algunas páginas de lista, como **Artículos**, también incluye una parte de Power BI.

[!INCLUDE [prod_short](includes/prod_short.md)] funciona con con el servicio de Power BI. Los informes para mostrar en [!INCLUDE [prod_short](includes/prod_short.md)] se almacenan en un servicio de Power BI. En [!INCLUDE [prod_short](includes/prod_short.md)], puede cambiar el informe que se muestra en la parte de Power BI a cualquier informe de Power BI disponible en su servicio de Power BI. La primera vez que inicia sesión en [!INCLUDE [prod_short](includes/prod_short.md)] y hasta que se conecta a un servicio de Power BI, las partes estarán vacías, como se muestra aquí:

![Parte de Power BI en Business Central](./media/power-bi-part.png)

## <a name="get-started"></a>Introducción

### <a name="prerequisites"></a>Requisitos previos

Si está usando [!INCLUDE[prod_short](includes/prod_short.md)] local, debe estar habilitado para la integración en Power BI. Esta tarea normalmente la realiza un administrador. Para más información, ver [Preparar [!INCLUDE[prod_short](includes/prod_short.md)] local para la integración de Power BI](admin-powerbi-setup.md#setup).

> [!NOTE]
> [!INCLUDE[prod_short](includes/prod_short.md)] online ya está configurado para integrarse con Power BI.

### <a name="sign-up-power-bi"></a>Registrarse en Power BI

Antes de que pueda usar Power BI con [!INCLUDE[prod_short](includes/prod_short.md)], deberá registrarse en el servicio de Power BI. Si aún no se ha registrado, vaya a [https://powerbi.microsoft.com](https://powerbi.microsoft.com). Cuando se registre, use su dirección de correo electrónico y contraseña del trabajo.

## <a name="connect-to-power-bi---one-time-only"></a><a name="connect"></a>Conectar a Power BI, solo una vez

Cuando inicia sesión por primera vez en [!INCLUDE [prod_short](includes/prod_short.md)], lo más probable es que vea una parte de Power BI vacía (como se muestra en la figura anterior) en varias páginas. Lo primero que debe hacer es conectarse a su cuenta de Power BI. Una vez conectado, puede ver los informes. Solo tiene que hacer este paso una vez.

1. Seleccione el vínculo **Introducción a Power BI** en la parte **Informes de Power BI**.
2. Se inicia la configuración asistida **Configurar informes de Power BI en Business Central**. Seleccione **Siguiente** para continuar.
3. En la página **Comprobar la licencia de Power BI**. Realice uno de los siguientes pasos:

    - Si aún no se ha registrado en Power BI, seleccione [Ir a la página de inicio de Power BI](https://powerbi.microsoft.com). Regístrese para tener una cuenta, luego regrese a [!INCLUDE[prod_short](includes/prod_short.md)] y termine la configuración.

    - Si ya tiene una licencia, seleccione **Siguiente**.
4. En la página siguiente, [!INCLUDE[prod_short](includes/prod_short.md)] ahora cargará un informe de demostración en Power BI. Esto tardará unos minutos, así que se realiza en segundo plano. Para completar la configuración, seleccione **Siguiente** y luego **Terminar**.

Comienza el proceso de conexión. Durante el proceso, [!INCLUDE [prod_short](includes/prod_short.md)] se comunica con el servicio de Power BI para determinar si tiene una cuenta y licencia de Power BI. Una vez verificada la licencia, se mostrarán el informe de Power BI predeterminado en la página. Si no se muestra un informe, puede seleccionar un informe de la parte.

> [!TIP]
> Con [!INCLUDE [prod_short](includes/prod_short.md)] Online, este paso cargará automáticamente por defecto los infomes de Power BI utilizados en [!INCLUDE [prod_short](includes/prod_short.md)] para su espacio de trabajo de Power BI.

#### <a name="from-prod_short-on-premises"></a>Desde [!INCLUDE [prod_short](includes/prod_short.md)] local

Conectarse a Power BI desde [!INCLUDE [prod_short](includes/prod_short.md)] es similar a Online. Sin embargo, se le pedirá en la página **PERMISOS DE SERVICIOS DE AZURE ACTIVE DIRECTORY** que otorgue acceso a servicios de Power BI. Para otorgar acceso, seleccione **Autorizar servicios de Azure** y entonces **Aceptar**.

Una vez conectado, puede seleccionar un informe de la parte de Power BI en las páginas.

## <a name="working-with-power-bi-reports"></a>Trabajar con informes de Power BI

### <a name="show-reports-on-list-pages"></a>Mostrar informes en páginas de lista

[!INCLUDE[prod_long](includes/prod_long.md)] incluye un cuadro informativo de Power BI en varias páginas de lista clave. Este cuadro informativo proporciona información adicional sobre los datos de la lista. A medida que se desplaza por las filas de la lista, el informe se actualiza y se filtra para la entrada seleccionada. Si no ve esta parte, en la barra de acciones, seleccione **Comportamiento** > **Monitor** > **Mostrar/ocultar informes de Power BI**.

Para aprender a crear informes para páginas de lista, consulte [Crear informes de Power BI para mostrar datos de lista en [!INCLUDE[prod_short](includes/prod_short.md)]](across-how-use-powerbi-reports-factbox.md).

### <a name="switch-reports"></a>Cambiar informes

Una parte de Power BI en una página puede mostrar cualquier informe de Power BI que esté disponible para usted. Para cambiar y ver otro informe, elija la acción **Seleccionar informe** en la lista de comandos desplegable en la parte superior de la parte.  

La página **Selección de informes de Power BI** muestra una lista de todos los informes de Power BI a los que tiene acceso. Esta lista se recupera desde su área de trabajo de Power BI. Seleccione la casilla **Habilitar** para cada informe que desee visualizar en la página y, a continuación, seleccione **Aceptar**. Volverá a su página Web y aparecerá el último informe que haya habilitado. Con la lista desplegable de comandos, utilice el comando **Anterior** y **Siguiente** para navegar entre informes.  

### <a name="get-more-reports"></a>Obtener más informes

Si no ve ningún informe en la página **Selección de informes de Power BI** o no ve el informe que desea, elija **Obtener informes**. Esta acción le permite buscar informes en dos ubicaciones: *Mi Organización* o *Servicios*.

- Elija **Mi Organización** para ir a los servicios de Power BI. Desde aquí, puede ver los informes de su organización para los que se le han otorgado derechos para ver. Luego puede agregarlos a su espacio de trabajo.
- Elija **Servicios** para ir a Microsoft AppSource donde pueda instalar aplicaciones de Power BI.  

> [!TIP]
> Si tiene Power BI Desktop, también puede crear nuevos informes de Power BI. Entonces, una vez que esos informes se publiquen en su espacio de trabajo de Power BI, aparecerán en la página página **Selección de informes de Power BI**.  

### <a name="manage-and-modify-reports"></a>Gestionar y modificar informes

Puede realizar cambios en un informe en la parte de Power BI. Los cambios que realice se publicarán en el servicio de Power BI. Si el informe se comparte con otros usuarios, también verán los cambios, a menos que guarde los cambios en un nuevo informe.

Para modificar un informe, seleccione la acción **Gestionar informe** en la lista desplegable de comandos de la parte de Power BI. Entonces comience a hacer cambios. Una vez que termine de hacer cambios, seleccione **Archivo** > **Guardar**. Si es un informe compartido y no desea realizar el cambio para todos los usuarios, seleccione **Guardar como** para evitar realizar este cambio para todos los usuarios.

Al regresar al área de trabajo, aparecerá el informe actualizado. Si usó **Guardar como**, tendrá que elegir **Seleccionar informe** y luego habilitar el nuevo informe para verlo.

> [!NOTE]
> Esta capacidad no está disponible con [!INCLUDE [prod_short](includes/prod_short.md)] local.

### <a name="upload-reports"></a><a name="upload"></a>Cargar informes

Los informes de Power BI se pueden distribuir entre los usuarios como archivos .pbix. Si tiene archivos .pbix, puede cargarlos y compartirlos con todos los usuarios de [!INCLUDE [prod_short](includes/prod_short.md)]. Los informes se comparten dentro de cada empresa en [!INCLUDE [prod_short](includes/prod_short.md)].  

Para cargar un informe, seleccione la acción **Cargar informe** de la lista desplegable de comandos en la parte **Informes de Power BI**. A continuación, localice el archivo .pbix que defina los informes que desea compartir. Puede cambiar el nombre predeterminado del archivo.  

Después de que el informe se cargue en su espacio de trabajo de Power BI, se carga automáticamente en los espacios de trabajo de Power BI de otros usuarios.

> [!NOTE]
> Cargar un informe requiere que tenga permisos de usuario SUPER en [!INCLUDE[prod_short](includes/prod_short.md)]. Además, no puede cargar informes con [!INCLUDE [prod_short](includes/prod_short.md)] local. Con local, carga informes directamente a su espacio de trabajo de Power BI. Para obtener más información, consulte [Trabajar con datos de [!INCLUDE [prod_short](includes/prod_short.md)] en Power BI](across-working-with-business-central-in-powerbi.md)..

## <a name="fixing-problems"></a>Solucionar problemas

Sin embargo, si se produce algún error, en esta sección se proporcionará una solución para los problemas más habituales.  

### <a name="you-dont-have-a-power-bi-account"></a>No tiene una cuenta de Power BI

No se ha configurado una cuenta de Power BI. Para obtener una cuenta de Power BI válida, debe tener una licencia y debe haber iniciado sesión previamente en Power BI, para crear un espacio de trabajo de Power BI.

### <a name="message-there-are-no-enabled-reports-choose-select-report-to-see-a-list-of-reports-that-you-can-display"></a>Mensaje: No hay informes habilitados. Elija Seleccionar informe para ver una lista de informes que se pueden visualizar.

Este mensaje aparece si el informe predeterminado no se pudo implementar en su espacio de trabajo de Power BI. O se implementó pero no se actualizó correctamente. Navegue hasta el informe en su espacio de trabajo de Power BI, seleccione **Conjunto de datos**, **Configuración** y luego actualice manualmente las credenciales. Una vez que el conjunto de datos se actualice correctamente, vuelva a [!INCLUDE[prod_short](includes/prod_short.md)] y seleccione manualmente el informe desde la página **Seleccionar informes**.

#### <a name="you-cant-see-a-report-on-the-select-report-page-on-a-list-page"></a>No puede ver un informe en la página Seleccionar informe en una página de lista

Probablemente se deba a que el nombre del informe no contiene el nombre de la página de la lista. Borre el filtro para obtener una lista completa de los informes de Power BI disponibles.

## <a name="see-related-training-at-microsoft-learn"></a>Consulte la Formación relacionada en [Microsoft Learn](/learn/modules/configure-powerbi-excel-dynamics-365-business-central/index)

## <a name="see-also"></a>Consulte también

[Business Central y Power BI](admin-powerbi.md)  
[Crear informes de Power BI para mostrar datos de [!INCLUDE [prod_long](includes/prod_long.md)]](across-how-use-financials-data-source-powerbi.md)  
[Componente de integración de Power BI e información general de la arquitectura para [!INCLUDE[prod_short](includes/prod_short.md)]](admin-powerbi-overview.md)  
[Trabajar con datos de [!INCLUDE [prod_short](includes/prod_short.md)] en Power BI](across-working-with-business-central-in-powerbi.md)  
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