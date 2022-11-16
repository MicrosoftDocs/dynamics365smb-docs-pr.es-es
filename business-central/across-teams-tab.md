---
title: Agregar una pestaña de Business Central en Microsoft Teams
description: Aprenda a agregar pestañas en Teams que muestran páginas de Business Central.
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.service: dynamics365-business-central
ms.topic: how-to
ms.date: 11/04/2022
ms.custom: bap-template
ms.search.keywords: Teams, MS Teams, Microsoft Teams, Skype, Link, Microsoft 365, collaborate, collaboration, teamwork, share records, tab
ms.openlocfilehash: cff1392b0e4ae622819fa50d4eaf69b98a9a1a52
ms.sourcegitcommit: bef166d75d656f4cc516f5f9a85227e540630344
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 11/07/2022
ms.locfileid: "9748407"
---
# <a name="add-business-central-tab-in-microsoft-teams"></a>Agregar una pestaña de Business Central en Microsoft Teams

[!INCLUDE [online_only](includes/online_only.md)]

En Teams, las pestañas aparecen en la parte superior de los canales y chats, lo que brinda a los participantes un acceso rápido a la información pertinente. Este artículo explica diferentes formas de agregar una pestaña que muestre datos de [!INCLUDE [prod_short](includes/prod_short.md)].

![Pestañas en Teams](media/teams-tabs-border.png)

## <a name="about-business-central-tabs"></a>Sobre las pestañas de Business Central

Una pestaña de [!INCLUDE [prod_short](includes/prod_short.md)] proporciona una vista enfocada de la lista y las páginas de tarjetas de [!INCLUDE [prod_short](includes/prod_short.md)]. La pestaña no muestra el cliente web completo de [!INCLUDE [prod_short](includes/prod_short.md)]. No hay borde del navegador, banner de [!INCLUDE [prod_short](includes/prod_short.md)] (por ejemplo, con Dígame, búsqueda, ayuda) o menú de navegación superior, solo el contenido de la página y sus acciones. El contenido es interactivo, lo que significa que puede seleccionar acciones y vínculos, cambiar datos y más. Está limitado a lo que ve y puede hacer por los mismos permisos asignados a su cuenta en [!INCLUDE [prod_short](includes/prod_short.md)].

Para saber quién puede ver el contenido en una pestaña de [!INCLUDE [prod_short](includes/prod_short.md)], consulte [¿Quién puede ver el contenido de una pestaña?](/dynamics365/business-central/teams-faq?tabs=tabs#who-can-view).

> [!TIP]
> ¿Es desarrollador? También puede agregar pestañas mediante programación mediante la API de Microsoft Graph. Para obtener más información, consulte [Agregar pestañas de Business Central en Teams](/dynamics365/business-central/dev-itpro/developer/devenv-develop-for-teams-tabs).  

## <a name="prerequisites"></a>Requisitos previos

Para agregar una pestaña de [!INCLUDE [prod_short](includes/prod_short.md)], se deben cumplir los siguientes requisitos:

- Tiene acceso a Microsoft Teams.
- Tiene una licencia de [!INCLUDE [prod_short](includes/prod_short.md)].
- Ha instalado la aplicación [!INCLUDE [prod_short](includes/prod_short.md)] en Teams. Para obtener más información, consulte [Instalar la aplicación [!INCLUDE [prod_short](includes/prod_short.md)] para Microsoft Teams](across-install-app-for-teams.md).

Para ver la pestaña [!INCLUDE [prod_short](includes/prod_short.md)] que fue agregada por otro participante en el canal o chat, se deben cumplir los siguientes requisitos:

- Tiene acceso a Microsoft Teams.
- Tiene una licencia de [!INCLUDE [prod_short](includes/prod_short.md)] o acceso limitado a Business Central con una sola licencia de Microsoft 365. Para obtener más información, consulte [Acceso a Business Central con licencias de Microsoft 365](admin-access-with-m365-license.md).
- Ha instalado la aplicación [!INCLUDE [prod_short](includes/prod_short.md)] en Teams.

## <a name="add-tab-using-recommended-content"></a>Agregar pestaña usando contenido recomendado

Siga estos pasos para agregar una pestaña eligiendo qué mostrar de una lista fácilmente disponible de contenido recomendado que se basa en su centro de funciones sin salir de Teams. Para obtener más información sobre el contenido que puede elegir, consulte [¿De dónde viene el contenido recomendado?](/dynamics365/business-central/teams-faq?tabs=tabs#where-does-the-recommended-content-come-from).

1. En la parte superior de un canal o chat en Teams, seleccione **+ Agregar una pestaña**.
2. En el cuadro de **Búsqueda**, escriba *Business Central*, luego seleccione el icono **[!INCLUDE [prod_short](includes/prod_short.md)]** y espere a que aparezca la ventana de configuración de [!INCLUDE [prod_short](includes/prod_short.md)].

   ![Muestra la ventana de configuración de la pestaña Business Central en Teams](media/teams-bc-tab-config-window.png)

3. La opción **Elegir entre el contenido recomendado para** muestra la empresa en [!INCLUDE [prod_short](includes/prod_short.md)] con la que trabaja. Si desea mostrar contenido de otra empresa, seleccione la empresa actual y, a continuación, utilice las opciones **Entorno** y **Empresa** para especificar la empresa con la que desea trabajar.
4. Seleccione la flecha hacia abajo en la opción **Contenido de la pestaña** y elija el contenido que desea mostrar.

   <!-- The list shows all pages that are bookmarked on your role center in [!INCLUDE [prod_short](includes/prod_short.md)]. To learn more about the content that you can choose from, see [Where does the recommended content come from?](teams-faq.md#recommended-content).-->
5. Algunas páginas pueden incluir diferentes vistas, que son variaciones de la página que se filtra para mostrar datos específicos. Para cambiar la vista del contenido, seleccione la flecha hacia abajo para la opción **Vista preferida** y elija la vista de la lista.

   Para obtener más información sobre las vistas, consulte [Guardar y personalizar vistas](ui-views.md).
6. Seleccione **Publicar en el canal sobre esta pestaña** para publicar automáticamente un anuncio en el canal o chat de Teams para que los participantes sepan que ha agregado esta pestaña.
7. Seleccione **Guardar**.

## <a name="add-tab-using-a-page-link"></a>Agregar pestaña usando un vínculo de página

Otra forma de agregar una pestaña mediante un vínculo (URL) a la página que desea mostrar. Esta forma es útil cuando desea mostrar un registro o página de lista de [!INCLUDE [prod_short](includes/prod_short.md)] determinados que no están marcados en su centro de roles.

1. En la parte superior de un canal o chat en Teams, seleccione **+ Agregar una pestaña**.
2. En el cuadro de diálogo de **Búsqueda**, escriba *Business Central*, luego seleccione el icono **[!INCLUDE [prod_short](includes/prod_short.md)]**.
3. Espere a que aparezca la ventana de configuración de pestaña de [!INCLUDE [prod_short](includes/prod_short.md)], luego seleccione la opción **Pegar un vínculo de [!INCLUDE [prod_short](includes/prod_short.md)] en su lugar**.

   ![Muestra la ventana de configuración de la pestaña Business Central en Teams y resalta la opción de vínculo](media/teams-bc-tab-config-window-page-link.png)
4. Vaya a [!INCLUDE [prod_short](includes/prod_short.md)] y abra la página que desea mostrar en la pestaña.
5. Copie el vínculo a la página.

   Existen dos formas de copiar el vínculo. La forma más sencilla y preferida es seleccionar **Compartir** ![Icono Compartir en Business Central](media/share-icon.png) > **Copiar vínculo**. La otra forma es copiar la URL completa de la barra de direcciones del navegador. Para obtener más información sobre este paso, consulte [Compartir registros de Business Central y vínculos de página](across-working-with-teams.md).

6. Vuelva a Teams y pegue el vínculo en el cuadro **URL**.
7. En el cuadro **Nombre de la pestaña**, introduzca un nombre que se mostrará en la pestaña.
8. Seleccione **Publicar en el canal sobre esta pestaña** para publicar automáticamente un anuncio en el canal o chat de Teams para que los participantes sepan que ha agregado esta pestaña.
9. Seleccione **Guardar**.

## <a name="add-tab-by-pinning-card-details"></a>Agregar pestaña fijando los detalles de la tarjeta

Use estos pasos para agregar una pestaña para un registro que se compartió o pegó en un canal o chat de Teams. Para obtener información sobre cómo compartir registros y vínculos de página en Teams, consulte [Compartir registros y vínculos de página en Teams](across-working-with-teams.md).

1. En Teams, seleccione el botón **Detalles** en la tarjeta.
2. En la esquina superior derecha de los detalles de la tarjeta, seleccione el icono **Fijar en la parte superior del chat** ![Icono de fijar para agregar la pestaña Teams en Business Central](media/pin-teams.png).

## <a name="change-a-tab-and-its-content"></a>Cambiar una pestaña y su contenido

Después de agregar una pestaña, puede realizar ciertos cambios en la pestaña. Por ejemplo, puede cambiar el nombre de la pestaña, moverla y eliminarla. Puede encontrar estas acciones en las opciones de la pestaña que están disponibles al seleccionar la flecha hacia abajo en la pestaña.

![Muestra la ventana de configuración de la pestaña Business Central en Teams y el menú de opciones de pestaña](media/teams-bc-tab-config-window-options.png)

En cuanto al contenido de una pestaña, puede modificar los datos, si tiene permiso. Si cambia los datos, los demás no verán los cambios hasta que abandonen la pestaña y regresen. Lo mismo es válido para usted si alguien más realiza cambios en los datos. No puede cambiar la página que se muestra en la pestaña, así que simplemente elimine la pestaña y agregue otra que se adapte.

También puede cambiar su vista de la página y sus datos, como ordenar y cambiar el diseño entre vistas de lista e icono. Cuando realiza este tipo de cambios, no afectarán lo que ven los demás. Verán lo que publicó originalmente, hasta que ellos mismos hagan cambios similares.

## <a name="see-also"></a>Consulte también .

[Descripción general de la integración de Business Central y Microsoft Teams](across-teams-overview.md)  
[Instalar la aplicación [!INCLUDE [prod_short](includes/prod_short.md)] para Microsoft Teams](across-install-app-for-teams.md)  
[Compartir registros y enlaces de página de Business Central en Microsoft Teams](across-working-with-teams.md).
[P+F de Teams](teams-faq.md)  
[Búsqueda de clientes, proveedores y otros contactos desde Microsoft Teams](across-search-contacts-teams.md)  
[Cambiar la empresa y otras configuraciones en Teams](across-teams-settings.md)  
[Consejos para la solución de problemas de Teams](admin-teams-troubleshooting.md)  
[Desarrollo para la integración de Teams](/dynamics365/business-central/dev-itpro/developer/devenv-develop-for-teams)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  

[!INCLUDE[footer-include](includes/footer-banner.md)]
