---
title: Buscar contactos desde Microsoft Teams
description: 'Aprenda a buscar clientes, proveedores y otros contactos de Business Central desde Microsoft Teams.'
author: jswymer
ms.topic: get-started
ms.devlang: al
ms.search.keywords: 'Teams, MS Teams, Microsoft Teams, Skype, Link, Microsoft 365, contacts, search, messaging extensions'
ms.date: 04/16/2024
ms.author: jswymer
ms.service: dynamics-365-business-central
ms.reviewer: jswymer
---

# <a name="searching-for-customers-vendors-and-other-contacts-from-microsoft-teams"></a>Búsqueda de clientes, proveedores y otros contactos desde Microsoft Teams

[!INCLUDE [online_only](includes/online_only.md)]. Se presentó en el lanzamiento de versiones 1 de 2021.

[!INCLUDE [prod_short](includes/prod_short.md)] tiene un sistema integral de administración de contactos profesionales que es esencial para los usuarios en ventas, operaciones u otros roles departamentales. Si es un usuario de uno de estos roles, con frecuencia deberá buscar, reunirse o iniciar una conversación con sus proveedores, clientes y otros contactos. Con la aplicación [!INCLUDE [prod_short](includes/prod_short.md)] para Teams, puede realizar estas tareas directamente desde Teams, sin tener que cambiar a [!INCLUDE [prod_short](includes/prod_short.md)]. Desde dentro de Teams, puede:

- Buscar contactos de [!INCLUDE [prod_short](includes/prod_short.md)] desde el cuadro de comando de Teams o desde el área de redacción de mensajes. Los contactos pueden incluir clientes potenciales, proveedores, clientes u otras relaciones de negocio.
- Compartir un contacto como una ficha en una conversación de Teams.
- Vea detalles sobre el contacto, el historial de interacciones y otra información, como pagos pendientes o documentos abiertos.

## <a name="prerequisites"></a>Requisitos previos

- Tiene acceso a Microsoft Teams.
- Ha instalado la aplicación [!INCLUDE [prod_short](includes/prod_short.md)] en Teams. Para obtener más información, consulte [Instalar la aplicación [!INCLUDE [prod_short](includes/prod_short.md)] para Microsoft Teams](across-install-app-for-teams.md)
- Tiene una cuenta de [!INCLUDE [prod_short](includes/prod_short.md)] con acceso a contactos en al menos una empresa.

> [!NOTE]
> Tanto si busca desde el cuadro de comando o el cuadro de redacción del mensaje, es posible que se le pida que inicie sesión o configure la aplicación la primera vez. Este paso es necesario para buscar contactos en la empresa de Business Central correcta. Para obtener información sobre cómo configurar la aplicación para elegir su empresa, consulte [Cambiar la empresa y otras configuraciones en Teams](across-teams-settings.md).

## <a name="look-up-contacts-from-the-command-box"></a>Buscar contactos desde el cuadro de comando

El cuadro de comando se encuentra en la parte superior de cada pantalla en Teams. Le permite buscar, realizar acciones rápidas o iniciar aplicaciones, como la aplicación [!INCLUDE [prod_short](includes/prod_short.md)]. La búsqueda desde el cuadro de comando es ideal para buscar rápidamente contactos y sus datos relacionados para su propio uso. Por ejemplo, suponga que desea buscar la dirección de correo electrónico de un proveedor para configurar una reunión en el calendario. O tal vez desee buscar el historial de interacciones durante una reunión con un cliente.

1. En el cuadro de comando, escriba **/Business Central** y, a continuación, seleccione la aplicación Business Central de los resultados.

    ![Abrir la aplicación Business Central para buscar contactos desde el cuadro de comando.](media/teams-contacts-command-1a.png)

2. En el cuadro **Business Central**, empiece a escribir el texto de búsqueda, como un nombre, una dirección o un número de teléfono.

    A medida que escribe, aparecerán resultados coincidentes.

    ![Buscar contactos de Business Central desde el cuadro de comando de Teams.](media/teams-contacts-command-2.png)
3. Seleccione un contacto de los resultados.

    La ficha de contacto aparece debajo del cuadro de comando.

4. Si desea agregar la ficha de contacto a una conversación, vaya a la esquina superior derecha de la ficha, seleccione **... (Mas opciones)** > **Copiar**. A continuación, pegue la copia en el cuadro de redacción del mensaje de una conversación.  

Para obtener más información general sobre el cuadro de comando en Teams, consulte [Teams: usar el cuadro de comando](https://support.microsoft.com/en-us/office/use-the-command-box-13c4e429-7324-4886-b377-5dbed539193b).

## <a name="look-up-contacts-from-the-message-compose-box"></a>Buscar contactos desde el cuadro de redacción del mensaje

La ventaja de usar el cuadro de redacción del mensaje es que puede agregar una ficha de contacto directamente a una conversación para que otros la vean.

1. Debajo del cuadro de redacción del mensaje, seleccione el icono **Business Central** para iniciar la aplicación.

    Si no ve el icono de **Business Central**, seleccione **... (extensiones de mensajes)**.

    ![Abrir la aplicación Business Central para buscar contactos desde el cuadro de mensajes.](media/teams-contacts-message-box.png)

2. En el cuadro **Business Central**, empiece a escribir el texto de búsqueda, como un nombre, una dirección o un número de teléfono.

    A medida que escribe, aparecerán resultados coincidentes.

    ![Buscar contactos de Business Central desde el cuadro de mensajes.](media/teams-contacts-5.png)
3. Seleccione un contacto de los resultados.

    La ficha de contacto aparece en el cuadro de redacción del mensaje.

    > [!NOTE]
    > La ficha de contacto no se envía de inmediato a la conversación para que otros la vean. Tiene la oportunidad de revisar el contenido de la ficha y agregar texto antes o después de esta como desee. A continuación, envíe su mensaje al chat cuando esté listo.

<!--
### <a name="heres-another-way"></a>Here's another way

1. Instead of using the **Business Central** icon, type **@Business Central** directly in the message compose box.
2. Enter your search terms in the box.
3. Use the up and down arrow keys on the keyboard to choose a contact, then select <kbd>Enter</kbd> to select it.-->

## <a name="viewing-contact-card-details"></a>Ver detalles de la ficha de contacto

La ficha de contacto en Teams le ofrece un resumen rápido del cliente, proveedor o contacto. La ficha es interactiva, lo que significa que puede ver más información o incluso modificar un contacto usando los botones **Detalles** o **Desplegable**.

El botón **Detalles** abre una ventana dentro de Teams que muestra más información sobre el contacto, pero no tanta como vería en [!INCLUDE [prod_short](includes/prod_short.md)]. Para ver toda la información sobre un contacto en [!INCLUDE [prod_short](includes/prod_short.md)], seleccione **Desplegable**.

La ficha de contacto funciona como fichas para registros, como productos, clientes o pedidos de venta. Para obtener más información sobre las fichas, consulte [Ver detalles de la ficha](across-working-with-teams.md#view-card-details).

> [!NOTE]
> Todos los participantes de una conversación de Teams podrán ver las fichas del contacto de Business Central que envíe a una conversación. Pero, para ver más detalles sobre los registros, usando los botones **Detalles** o **Desplegable** de una tarjeta, necesitarán acceder a [!INCLUDE [prod_short](includes/prod_short.md)]. Para obtener más información, consulte [Administración de integración de Microsoft Teams](admin-teams-integration.md#minimum-requirements-1).

## <a name="see-also"></a>Consulte también

[Descripción general de la integración de Business Central y Microsoft Teams](across-teams-overview.md)  
[Instalar la aplicación [!INCLUDE [prod_short](includes/prod_short.md)] para Microsoft Teams](across-install-app-for-teams.md)  
[P+F de Teams](teams-faq.md)  
[Cambiar la empresa y otras configuraciones en Teams](across-teams-settings.md)  
[Compartir registros en Microsoft Teams](across-working-with-teams.md)  
[Consejos para la solución de problemas de Teams](admin-teams-troubleshooting.md)  
[Desarrollo para la integración de Teams](/dynamics365/business-central/dev-itpro/developer/devenv-develop-for-teams)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  


[!INCLUDE[footer-include](includes/footer-banner.md)]
