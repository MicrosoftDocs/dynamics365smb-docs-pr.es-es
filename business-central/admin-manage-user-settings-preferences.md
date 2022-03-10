---
title: Administrar la configuración y las preferencias del usuario como administrador
description: Administre las configuraciones de usuario y preferencias en Dynamics 365 Business Central.
author: sorenfriisalexandersen
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.reviewer: edupont
ms.search.keywords: user settings, preferences, language, region, time zone, regional settings
ms.search.form: 9204
ms.date: 04/01/2021
ms.author: soalex
ms.openlocfilehash: 779dcea91d2e856bfae847f98695ceed0c0d600e
ms.sourcegitcommit: ef80c461713fff1a75998766e7a4ed3a7c6121d0
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 02/15/2022
ms.locfileid: "8145945"
---
# <a name="manage-user-settings-and-preferences"></a>Administrar configuraciones y preferencias de usuario

Como administrador, puede configurar el usuario en [!INCLUDE[prod_short](includes/prod_short.md)], similar a cómo los usuarios individuales administran sus propias preferencias en la página **Mi configuración**.  

Obtenga un resumen de todos los usuarios en la lista **Usuarios** y cambie la configuración individual seleccionando la acción **Configuración de usuario** para el usuario correspondiente.

> [!TIP]
> La lista **Configuración de usuario** muestra la configuración actual de cada usuario. Para ver o editar usuarios individuales, elija la acción **Ver** o **Editar**.

La página **Tarjeta Configuración usuario** es similar a la página **Mi configuración** a la que cada usuario tiene acceso, y es una potente herramienta para usted como administrador para establecer la configuración predeterminada y borrar páginas personalizadas, por ejemplo.  

## <a name="types-of-user-settings"></a>Tipos de configuraciones de usuario

*Configuraciones de usuario* no es lo mismo que *configuración de usuario*, que se refiere al usuario como entidad y al acceso del usuario en el sistema. Además, la configuración del usuario no tiene nada que ver con la personalización de un usuario, como cambios superficiales en la interfaz de usuario. La configuración del usuario determina la configuración predefinida para cada usuario en varios aspectos de la forma en que la aplicación se presenta al usuario. El siguiente párrafo enumera los cinco tipos de configuraciones y preferencias de usuario que el administrador puede establecer de forma individual o central:

- **Empresa**  

  Este valor de configuración determina la empresa que va a iniciar sesión en el próximo inicio de sesión. Un usuario puede tener acceso a múltiples empresas y puede estar activo en varias compañías.

- **Rol**  

  El rol, o perfil, describe la función del usuario en la empresa, como *Director de ventas*, *Contable* o *Agente de compras*. El perfil determina el área de trabajo del usuario, la página Web que los usuarios verán cuando inicien sesión. El perfil no afecta los derechos de acceso a la funcionalidad en [!INCLUDE[prod_short](includes/prod_short.md)].  

- **Idioma**  

  Define el idioma de la aplicación en el que [!INCLUDE[prod_short](includes/prod_short.md)] presenta texto, subtítulos y mensajes de error. Si los usuarios [!INCLUDE[prod_short](includes/prod_short.md)] están sincronizados desde Microsoft 365, se utiliza el idioma de Microsoft 365, suponiendo que el usuario quiera usar la misma configuración en los productos de Office y [!INCLUDE[prod_short](includes/prod_short.md)]. El administrador puede cambiar la configuración predeterminada y cada usuario puede elegir entre los idiomas disponibles en la página Mi configuración. No obstante, se restablecerán al valor de Microsoft 365 una vez que se realice la siguiente sincronización.

  Si la configuración de idioma de Microsoft 365 coincide con un idioma compatible en [!INCLUDE[prod_short](includes/prod_short.md)], este idioma será elegido para el usuario.  

  > [!NOTE]
  > Es posible que deba instalar una aplicación de idioma para [!INCLUDE[prod_short](includes/prod_short.md)] para mostrar correctamente el idioma. Por lo tanto, se recomienda instalar las aplicaciones de idioma necesarias antes de que cualquier usuario inicie sesión por primera vez para que tengan una buena experiencia desde su primer día. Para obtener más información, vea la lista de [idiomas compatibles](/dynamics365/business-central/dev-itpro/compliance/apptest-countries-and-translations).  
  
- **Región**  

  Define cómo se presentan las fechas y los números en el cliente [!INCLUDE[prod_short](includes/prod_short.md)], como si usar los formatos de fecha europeos o americanos, o cómo mostrar el signo decimal y los separadores de miles en las cantidades. Si los usuarios [!INCLUDE[prod_short](includes/prod_short.md)] están sincronizados desde Microsoft 365, se utiliza la configuración regional de Microsoft 365, suponiendo que el usuario quiera usar la misma configuración en los productos de Office y [!INCLUDE[prod_short](includes/prod_short.md)]. Un administrador o usuario puede cambiar esta configuración manualmente en [!INCLUDE[prod_short](includes/prod_short.md)], pero se restablecerá al valor de Microsoft 365 una vez que se realiza la siguiente sincronización.

- **Zona horaria**  

  Define la zona horaria en la que se encuentra el usuario. Actualmente esto no está sincronizado desde Microsoft 365 y debe configurarse manualmente.  

- **Consejos didácticos**

  [!INCLUDE [ua-teachingtips](includes/ua-teachingtips.md)] Como administrador, puede desactivar los consejos didácticos para todos los usuarios, por ejemplo, si está en proceso de incorporar usuarios que ya están familiarizados con [!INCLUDE [prod_short](includes/prod_short.md)].  

> [!NOTE]
> Si se realiza la sincronización de un usuario de Microsoft 365 mientras que hay usuarios con sesión iniciada en [!INCLUDE[prod_short](includes/prod_short.md)], estos usuarios deben actualizar el navegador o cerrar sesión y volver a iniciar sesión en [!INCLUDE[prod_short](includes/prod_short.md)] para ver un posible idioma diferente que se hubiera establecido a través de la acción de sincronización.

## <a name="overview-of-all-user-specific-changes"></a>Resumen de todos los cambios específicos del usuario

Como administrador, puede obtener una resumen de los cambios individuales en [!INCLUDE [prod_short](includes/prod_short.md)] que cada usuario podría haber hecho en varias páginas en [!INCLUDE [prod_short](includes/prod_short.md)]. A medida que los usuarios realizan cambios en su experiencia en [!INCLUDE [prod_short](includes/prod_short.md)], estos cambios se reflejarán en la lista **Personalizaciones de usuario**. <!--Administrators can also set these settings for users before they log in the first time, so users do not have to do it themselves, providing them a better *getting started* experience.-->

<!-- >[!NOTE]
> User personalizations do not have anything to do with the *personal* lightweight changes a user can make to the user experience.-->

## <a name="to-review-or-delete-user-personalizations"></a>Para revisar o eliminar personalizaciones de usuarios

1. Elija el icono ![Buscar página o informe](media/ui-search/search_small.png "Icono Buscar página o informe") , escriba **Páginas personalizadas** y luego elija el enlace relacionado.
2. Esto muestra la lista de usuarios y sus páginas personalizadas. Para borrar la personalización de un usuario, haga clic en la fila correspondiente o elija **Administrar** y luego **Eliminar**.

Esto elimina la personalización y la experiencia del usuario de la página correspondiente vuelve al estado predeterminado.

## <a name="see-also"></a>Consulte también

[Preparación para hacer negocios](ui-get-ready-business.md)  
[Disponibilidad nacional/regional e idiomas admitidos](/dynamics365/business-central/dev-itpro/compliance/apptest-countries-and-translations)  
[Cambiar idioma y región](about-locale-language.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
