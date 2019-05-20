---
title: Administrar la personalización como administrador en Business Central | Documentos de Microsoft
description: Aprenda a personalizar la interfaz de usuario para que se adapte a su forma de trabajar.
services: project-madeira
documentationcenter: ''
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customize, personalize, personalization, hide columns, remove fields, move fields
ms.date: 04/01/2019
ms.author: jswymer
ms.openlocfilehash: 37cdf2d7dcc46b1286cbb7a5ad620547e364309e
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/29/2019
ms.locfileid: "1250600"
---
# <a name="managing-personalization-as-an-administrator"></a>Administrar la personalización como administrador

 Los usuarios pueden personalizar el área de trabajo para que se adapte a sus preferencias. Como administrador, controla y gestiona la personalización por medio de:

-   Habilitación o deshabilitación de la función de personalización para toda la aplicación (solo para la instalación local).
-   Habilitación o deshabilitación de la función de personalización para los usuarios de un perfil específico.
-   Borrado de cualquier personalización de página que los usuarios hayan realizado.

## <a name="EnablePersonalization"></a>Para habilitar o deshabilitar la personalización (solo local)

De forma predeterminada, la personalización no está habilitada en el cliente. Puede habilitar o deshabilitar la personalización modificando el archivo de configuración (navsettings.json) de la instancia del servidor web de Business Central que sirve a los clientes.

1. Para habilitar la personalización, agregue la siguiente línea al archivo navsettings.json:

    ```
    "PersonalizationEnabled": "true"
    ```

    Para deshabilitar la personalización, quite esta línea o cámbiela por:

    ```
    "PersonalizationEnabled": "false"
    ```

    Para obtener más información sobre cómo modificar el archivo navsettings.json, consulte [Modificar el archivo navsettings.json directamente](https://docs.microsoft.com/en-us/dynamics365/business-central/dev-itpro/administration/configure-web-server?branch=master#Settings).

2. Genere y descargue los símbolos de aplicación.

    Este paso es opcional y no es necesario para habilitar la personalización. Sin embargo, garantiza que las nuevas páginas creadas por los desarrolladores puedan personalizarse.

    1. Primero, genere los símbolos ejecutando finsql.exe con un comando `generatesymbolreference`. El archivo finsql.exe se encuentra en la carpeta de instalación para [!INCLUDE[server](includes/server.md)] y el entorno de desarrollo de Dynamics NAV (CSIDE). Para generar los símbolos, abra un símbolo del sistema, cambie al directorio donde está almacenado el archivo y ejecute el siguiente comando:

        ```
        finsql.exe Command=generatesymbolreference, Database="<Database Name>", ServerName=<SQL Server Name\<Server Instance>
        ```
    Por ejemplo:

        ```
        finsql.exe Command=generatesymbolreference, Database="Demo Database BC", ServerName=MySQLServer\BCDEMO
        ```

    Para obtener más información, consulte [Ejecución de C/SIDE y AL en paralelo](https://docs.microsoft.com/en-us/dynamics365/business-central/dev-itpro/developer/devenv-running-cside-and-al-side-by-side).

    2. Configure la instancia de [!INCLUDE[nav_server_md](includes/nav_server_md.md)] en **Habilitar las referencias de los símbolos de la aplicación al iniciar el servidor** (EnableSymbolLoadingAtServerStartup). Para obtener más información, consulte [Configuración de Business Central Server](https://docs.microsoft.com/en-us/dynamics365/business-central/dev-itpro/administration/configure-server-instance#development-settings).

## <a name="to-disable-personalization-for-a-profile"></a>Para deshabilitar la personalización de un perfil

Puede evitar que todos los usuarios que pertenecen a un perfil específico puedan personalizar sus páginas.

1. Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Perfiles** y luego elija el enlace relacionado.
2. Seleccione el perfil de la lista que desea modificar.
3. Seleccione la casilla **Deshabilitar personalización** y, a continuación, seleccione el botón **Aceptar**.

## <a name="to-clear-user-personalizations"></a>Para borrar personalizaciones de usuarios

Al borrar la personalización de la página, la página vuelve a su diseño original antes de realizar cualquier personalización. Existen dos formas de borrar las personalizaciones que los usuarios han realizado en las páginas: usando la página **Eliminar personalización usuario** o la página **Tarjeta personalización usuario**.

### <a name="to-clear-user-personalizations-by-using-the-delete-user-personalization-page"></a>Para borrar las personalizaciones de los usuarios con la página Eliminar personalización de usuarios.

La página **Eliminar personalización de usuarios** le permite borrar la personalización por página y por usuario.

1. Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Eliminar personalización usuario** y luego elija el enlace relacionado.

    La página enumera todas las páginas que se han personalizado y el usuario al que pertenece.

    >[!NOTE]
    > Una marca de verificación en las columnas **Personalización heredada** indica que la personalización se realizó en una versión anterior de [!INCLUDE[d365fin](includes/d365fin_md.md)] que manejaba la personalización de forma diferente a como lo hace ahora. Los usuarios que intentan personalizar estas páginas se bloquean a menos que elijan desbloquear la página. Para obtener más información, consulte [Por qué la página está bloqueada para la personalización](ui-personalization-locked.md).

2. Seleccione el movimiento que desea eliminar y, después, seleccione **Eliminar**.

    El usuario podrá ver los cambios la próxima vez que inicie sesión.

### <a name="to-clear-user-personalizations-by-using-the-user-personalization-card-page"></a>Para borrar las personalizaciones de los usuarios con la página Tarjeta personalización de usuarios

La página **Tarjeta personalización de usuarios** le permite borrar la personalización en todas las páginas de un usuario específico. Esto requiere permiso de escritura para el **perfil** de tabla 2000000072.

1. Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Personalización usuario** y luego elija el enlace relacionado.

    La página **Personalización usuario** muestra todos los usuarios que potencialmente hayan personalizado las páginas. Si no puede encontrar un usuario en la lista, significa que no tiene páginas personalizadas.

2. Seleccione el usuario de la lista y, a continuación, seleccione la acción **Editar**.

3. En la pestaña **Acciones**, elija **Borrar páginas personalizadas**.

    El usuario podrá ver los cambios la próxima vez que inicie sesión.

## <a name="see-also"></a>Consulte también
[Personalización de su área de trabajo](ui-personalization-user.md)  
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Cambiar la configuración básica](ui-change-basic-settings.md)  
[Cambiar las funciones que se muestran](ui-experiences.md)  
