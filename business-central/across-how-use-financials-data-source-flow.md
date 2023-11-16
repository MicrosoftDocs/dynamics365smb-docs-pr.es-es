---
title: Usar flujos de Power Automate en Business Central
description: Configure y use flujos de Power Automate para crear o modificar datos de Business Central.
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.search.keywords: 'workflow, OData, Power App, SOAP, Power Automate,'
ms.search.form: '1500,'
ms.date: 08/31/2023
ms.custom: bap-template
---
# <a name="use-power-automate-flows-in-"></a>Usar flujos de Power Automate en [!INCLUDE[prod_short](includes/prod_short.md)]

Con [!INCLUDE[prod_short](includes/prod_short.md)], se le otorga una licencia para Microsoft Power Automate. Esta licencia le permite utilizar sus datos de [!INCLUDE[prod_short](includes/prod_short.md)] como parte de un flujo de trabajo de Microsoft Power Automate. Usted crea sus propios flujos y se conecta a sus datos desde orígenes internos y externos a través del conector [!INCLUDE [prod_short](includes/prod_short.md)].

Los flujos de Power Automate se desencadenan por eventos, como la creación, modificación o eliminación de un registro. También pueden ejecutarse en un horario definido por el usuario o bajo demanda.

> [!NOTE]
> Los administradores pueden restringir el acceso a Power Automate. Si descubre que no tiene acceso a algunas o todas las funciones descritas en este artículo, hable con su administrador. Si quiere aprender cómo puede controlar el acceso a Power Automate como administrador, vea [Configurar la integración de Power Automate](/dynamics365/business-central/dev-itpro/powerplatform/power-automate-setup).

<!-- You must have a valid account with both [!INCLUDE[prod_short](includes/prod_short.md)] and Power Automate. --> 

> [!TIP]
> Además de Power Automate, puede utilizar las plantillas de flujo de trabajo de aprobación en [!INCLUDE[prod_short](includes/prod_short.md)]. Aunque son dos sistemas de flujo de trabajo independientes, cualquier plantilla de flujo de trabajo de aprobación que cree con Power Automate se agrega a la lista de flujos de trabajo en [!INCLUDE[prod_short](includes/prod_short.md)]. Obtenga más información en [Flujos de trabajo](across-workflow.md).

## <a name="about-power-automate-flows"></a>Acerca de los flujos de Power Automate

Power Automate es un servicio que lo ayuda a crear flujos de trabajo (o flujos) automatizados entre aplicaciones y servicios, como [!INCLUDE[prod_short](includes/prod_short.md)]. Los flujos de Power Automate requieren poco o ningún conocimiento de codificación. Se pueden asociar con una amplia gama de eventos y respuestas, tales como:

- Cambios de registros
- Actualizaciones de archivos externos
- Documentos publicados
- Diferentes servicios de Microsoft y de terceros, como Microsoft Outlook, Excel, Dataverse, Teams, SharePoint, Power Apps y más.

Hay tres tipos diferentes de flujo de nube con los que puede trabajar:

|Tipo de flujo|Descripción|
|---------|-----------|
|Flujo automatizado|Este tipo de flujo se ejecuta automáticamente por un evento. En [!INCLUDE[prod_short](includes/prod_short.md)], un evento podría ser cuando se crea, modifica o elimina un registro o documento. Así, por ejemplo, una nueva factura de venta puede activar un flujo para una solicitud de aprobación, que puede tener diferentes eventos establecidos en función de la respuesta del aprobador. Una respuesta negativa envía una notificación y un correo electrónico al solicitante de la aprobación. Una respuesta positiva actualiza simultáneamente una hoja de cálculo Excel situada en una carpeta de SharePoint y envía una actualización a un chat de Teams. Los flujos automatizados pueden ser iniciados por eventos internos y externos en [!INCLUDE[prod_short](includes/prod_short.md)].|
|Flujo de aprobación|Los flujos de aprobación también son flujos automatizados en Power Automate, pero están diseñados específicamente para solicitar aprobación cuando se realizan cambios en registros y datos. Puede utilizar flujos de aprobación en Power Automate como alternativa a la [característica de flujos de trabajo de aprobación](across-use-workflows.md) que es parte de [!INCLUDE[prod_short](includes/prod_short.md)]. |
|Flujo programado|Este tipo de flujo también se ejecuta automáticamente, pero se ejecuta periódicamente en una fecha y hora programadas. |
|Flujo instantáneo|Este tipo de flujo se ejecuta bajo demanda, lo que requiere que el usuario lo ejecute manualmente desde un botón o acción en otra aplicación o dispositivo, en este caso, el cliente de [!INCLUDE[prod_short](includes/prod_short.md)]. Los flujos instantáneos funcionan de forma similar a los accesos directos por lotes, realizando varios pasos largos con unas pocas pulsaciones de botón y se lanzan desde páginas o tablas específicas. Por ejemplo, un flujo puede añadir un botón al menú de acciones de la página **Proveedores** para bloquear los pagos a un proveedor y, al mismo tiempo, enviar correos electrónicos personalizados al contacto del proveedor y a los compradores de su empresa, así como actualizar el contacto en Outlook. |

## <a name="power-automate-features"></a>Características de Power Automate

Puede explorar todos los flujos de Power Automate actualmente disponibles para usted iniciando sesión en [Power Automate](https://powerautomate.com) y seleccionando **Mis flujos** en la barra de navegación de la izquierda. Aquí encontrará los flujos que ya haya creado usted mismo y los flujos compartidos con usted por un administrador o un compañero de trabajo.

- Los flujos instantáneos también están disponibles para ejecutarse directamente desde la mayoría de las páginas de listas, tarjetas y documentos en [!INCLUDE[prod_short](includes/prod_short.md)]. Encontrará los flujos instantáneos en el grupo de acciones **Automatizar** en la barra de acciones de las páginas. Para ejecutar un flujo, selecciónelo y siga las instrucciones que se le presenten. Obtenga más información en las secciones siguientes.

- Con flujos automatizados en [!INCLUDE[prod_short](includes/prod_short.md)], no tiene nada que hacer, a menos que quiera cambiarlos o apagarlos. De lo contrario, solo funcionarán cuando se activen. 
<!--

## <a name="automated-flows"></a>Automated flows

With Power Automate, you can create business flows directly in-house and rely on citizen developers. Automated workflows can be started by both internal and external events in [!INCLUDE[prod_short](includes/prod_short.md)], and also be set to run periodically. Learn more and get instructions on how to create flows in the [Set Up Automated Workflows](/dynamics365/business-central/dev-itpro/powerplatform/automate-workflows) article in the administration content.

-->

## <a name="run-instant-flows"></a>Ejecutar flujos instantáneos

Los flujos instantáneos de una página dentro de [!INCLUDE [prod_short](includes/prod_short.md)] en línea pueden permanecer dentro del contexto del proceso comercial en el que se encontraba. Puede ejecutar un flujo instantáneo desde la mayoría de las listas, tarjetas o documentos.

1. En la barra de acción, seleccione **Automatizar**, luego elija un flujo de la lista de flujos disponibles bajo la acción **Power Automate**

    :::image type="content" source="media/power-automate-instant-menu.svg" alt-text="Muestra la acción Automatizar con acciones de flujo instantáneo.":::

    En alguna página, **Automatizar** está anidado debajo de **Mas opciones (...)**. 
2. En el panel **Ejecutar flujo**, complete los campos obligatorios y, a continuación, seleccione **Continuar** para ejecutar el flujo.

> [!NOTE]
> La primera vez que usa el elemento **Automatizar**, es posible que solo vea la acción **Comenzar con Power Automate**. Ve esta acción porque no ha aceptado el aviso de privacidad de Microsoft Power Automate. Para continuar, seleccione **Comenzar con Power Automate** y siga las instrucciones para estar de acuerdo o en desacuerdo.  
>
> :::image type="content" source="media/power-automate-action.png" alt-text="Muestra el elemento Automatizar en la barra de acción.":::

<!--

[!INCLUDE [prod_short](includes/prod_short.md)] can run a Power Automate flow from most list, card, and document pages. Once the admin has connected [!INCLUDE [prod_short](includes/prod_short.md)] with Power Automate, you'll see any flows your organization has added when you choose the **Automate** action on the relevant pages. Instant flows are run without leaving [!INCLUDE [prod_short](includes/prod_short.md)]. Learn more in the [Set Up Automated Workflows](/dynamics365/business-central/dev-itpro/powerplatform/automate-workflows) article in the administration content.

These instant flows open on a page inside [!INCLUDE [prod_short](includes/prod_short.md)] online so you can remain within the context of the business process you were in the middle of. Choose the **Automate** action—on some pages nested under the **More Options** menu—choose the **Power Automate** menu item, then choose the relevant link to trigger the workflow. The connection to Power Automate is already set up for you.

Most flows require you to fill in a field or two before you choose the **Run flow** action.

> [!TIP]
> If you don't see an **Automate** action, then your [!INCLUDE [prod_short](includes/prod_short.md)] probably hasn't yet been set up to use Power Automate. Learn more from your admin.-->

## <a name="create-edit-and-manage-flows"></a>Crear, editar y administrar flujos

La creación de nuevos flujos, la modificación y la gestión de los existentes (como activarlos o desactivarlos) se pueden realizar directamente en Power Automate. Pero puede iniciar algunas de estas tareas desde el menú de acción Automatizar en [!INCLUDE[prod_short](includes/prod_short.md)]:

:::image type="content" source="media/power-automate-menu.svg" alt-text="Muestra la acción Automatizar en la barra de acciones con acciones expandidas.":::

- Para crear un flujo automatizado a partir de una página de lista, tarjeta o documento, seleccione **Automatizar** > **Crear flujo automatizado**.
- Para crear un flujo de trabajo de aprobación a partir de una página de lista, tarjeta o documento, seleccione **Automatizar** > **Crear flujo de aprobación**.

  > [!TIP]
  > Esta acción sólo está disponible en páginas de tipo tarjeta y documento; no listas.
- Para crear un flujo instantáneo a partir de una página de lista, tarjeta o documento, seleccione **Automatizar** > **Crear acción basada en un flujo**.
- Para abrir Power Automate desde una página de lista, tarjeta o documento, seleccione **Automatizar** > **Administrar flujos**.
<!--- To create new flows or manage existing flows from inside [!INCLUDE[prod_short](includes/prod_short.md)], got to the **Manage Power Automate Flows** page.-->

Estas tareas generalmente las realizan administradores o superusuarios. Las tareas requieren un conocimiento más amplio de los procesos de negocio en [!INCLUDE[prod_short](includes/prod_short.md)]. Para obtener más información, consulte los siguientes artículos en la ayuda para desarrolladores y profesionales de TI de Business Central:

- [Integración de Power Automate](/dynamics365/business-central/dev-itpro/powerplatform/power-automate-overview)
- [Crear flujos automatizados](/dynamics365/business-central/dev-itpro/powerplatform/instant-flows) (también cubre flujos de aprobación)
- [Crear flujos instantáneos](/dynamics365/business-central/dev-itpro/powerplatform/instant-flows)
- [Administrar flujos de Power Automate](/dynamics365/business-central/dev-itpro/powerplatform/manage-power-automate-flows)
<!-- 

## <a name="add-more-automated-flows-and-instant-flows"></a>Add more automated flows and instant flows

You can create flows through the [powerautomate.microsoft.com](https://powerautomate.microsoft.com) website. However, if your admin has switched on the capability to run Power Automate flows from inside [!INCLUDE [prod_short](includes/prod_short.md)] online, you can start the process of building a flow from the **Automate** action on the relevant pages, which can be found under the **More Options** menu depending on the page. Then choose the **Power Automate** menu item, and then choose the **Create a flow** action. Power Automate then opens in a new browser tab, and you're signed in automatically.

You can find sample templates to adapt to your company and all available trigger events, using both [!INCLUDE [prod_short](includes/prod_short.md)] and external tools, by choosing the **Connectors** menu on the Power Automate website. Learn more about available templates and triggers in the [Set Up Automated Workflows](/dynamics365/business-central/dev-itpro/powerplatform/automate-workflows) article in the administration content.

## <a name="create-and-manage-power-automate-flows"></a>Create and manage Power Automate flows

You can create new flows or manage existing Power Automate flows in [!INCLUDE [prod_short](includes/prod_short.md)] on the **Manage Power Automate Flows** page. Learn more in the [Manage Power Automate Flows](/dynamics365/business-central/dev-itpro/powerplatform/manage-power-automate-flows) article in the administration content.

<!--
You can also manage available Power Automate workflows on the **Workflows** page in [!INCLUDE[prod_short](includes/prod_short.md)]. The page lists both the built-in approval and Power Automate workflows, with options for the latter to enable/disable, delete, and view the workflow on the Power Automate website.-->

## <a name="see-also"></a>Consulte también .

[Solucionar problemas de sus [!INCLUDE[prod_short](includes/prod_short.md)] flujos de trabajo automatizados](across-flow-troubleshoot.md)  
[Prepararse para hacer negocios](ui-get-ready-business.md)  
[Flujos de trabajo](across-workflow.md)  
[Importar datos de empresa de otros sistemas financieros](across-import-data-configuration-packages.md)  
[Asignar permisos a usuarios y grupos](ui-define-granular-permissions.md)  
[Configurar [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md)  
[Finanzas](finance.md)  
[Administrar flujos de Power Automate](/dynamics365/business-central/dev-itpro/powerplatform/manage-power-automate-flows)  
[Configurar flujos de trabajo automatizados](/dynamics365/business-central/dev-itpro/powerplatform/automate-workflows)  
[Activar flujos instantáneos](/dynamics365/business-central/dev-itpro/powerplatform/instant-flows)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
