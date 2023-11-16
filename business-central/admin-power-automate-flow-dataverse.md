---
title: Utilizar un flujo de Power Automate para alertas de cambios de entidad
description: Aprenda a crear un flujo en Power Automate que le avisará cuando cambie una entidad en el entorno de Dataverse.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'Power Automate, Flow, Dataverse'
ms.search.form: null
ms.date: 09/05/2022
ms.author: bholtorf
---
# <a name="use-a-power-automate-flow-to-timely-synchronize-dataverse-entity-changes"></a>Utilizar un flujo de Power Automate para alertas de cambios de entidad de Dataverse

Los administradores pueden crear un flujo automatizado en Power Automate que notifique su [!INCLUDE[prod_short](includes/prod_short.md)] sobre cambios en registros de su organización de [!INCLUDE [cds_long_md](includes/cds_long_md.md)].

> [!NOTE]
> Este artículo asume que ha conectado su versión en línea de [!INCLUDE[prod_short](includes/prod_short.md)] con [!INCLUDE [cds_long_md](includes/cds_long_md.md)] y la sincronización programada entre las dos aplicaciones.

## <a name="import-the-flow-template"></a>Importar la plantilla de flujo

> [!TIP]
> Para facilitar la configuración del flujo, hemos creado una plantilla que definirá el activador del flujo y la condición del flujo por usted. Para utilizar la plantilla, siga los pasos de esta sección. Para crear el flujo usted mismo, omita esta sección y comience con los pasos en [Definir el desencadenador del flujo](#define-the-flow-trigger).

1. Inicie sesión en [Power Automate](https://powerautomate.microsoft.com).
2. Elija **Plantillas** y luego busque **Notificar a Business Central**.

:::image type="content" source="media/power-automate-import-template.png" alt-text="Palabras clave para encontrar la plantilla del flujo":::
3. Elija la plantilla **Notificar a Business Central cuando cambie una cuenta**.
4. Continúe con los pasos de la sección [Notificar un cambio a Business Central](#notify-business-central-about-a-change).

## <a name="define-the-flow-trigger"></a>Definir el desencadenador del flujo

1. Iniciar sesión en [Power Automate](https://flow.microsoft.com).
2. Cree un flujo de nube automatizado que comience cuando se añada, modifique o elimine una entidad una fila para una entidad de [!INCLUDE [cds_long_md](includes/cds_long_md.md)]. Para más información, vea [Desencadenar flujos cuando se agrega, modifica o elimina una fila](/power-automate/dataverse/create-update-delete-trigger). Este ejemplo utiliza la entidad **Cuentas**. La siguiente imagen muestra la configuración del primer paso para definir un disparador de flujo.

:::image type="content" source="media/power-automate-flow-dataverse-trigger.png" alt-text="Configuración del desencadenador del flujo":::
3. Utilice el botón **AssistEdit (...)** de la esquina superior derecha para agregar la conexión a su entorno de [!INCLUDE [cds_long_md](includes/cds_long_md.md)].
4. Elija **Mostrar opciones avanzadas**, y en el campo **Filtrar filas**, ingrese **customertypecode eq 3** o **customertypecode eq 11** y **statecode eq 0**. Estos valores significan que el desencadenador reaccionará solo cuando se realicen cambios en las cuentas activas del tipo **cliente** o **proveedor**.

## <a name="define-the-flow-condition"></a>Definir la condición del flujo

Los datos se sincronizan entre [!INCLUDE[prod_short](includes/prod_short.md)] y [!INCLUDE [cds_long_md](includes/cds_long_md.md)] a través de una cuenta de usuario de integración. Para ignorar los cambios realizados por la sincronización, cree un paso de condición en su flujo que excluya los cambios realizados por la cuenta de usuario de integración.  

1. Agregue un paso **Obtener una fila por id de Dataverse** después del disparador de flujo con los siguientes ajustes. Para más información, vea [Obtener una fila por id de Dataverse](/power-automate/dataverse/get-row-id).

    1. En el campo **Nombre de tabla**, elija **Usuarios**
    2. En el campo **Id de fila**, elija **Modificado por (valor)** del disparador de flujo.  

2. Agregue un paso de condición con el siguiente ajuste **o** para identificar la cuenta de usuario de integración.
    1. La **Dirección de correo principal** del usuario contiene **contoso.com**
    2. El **Nombre completo** del usuario del usuario **[!INCLUDE[prod_short](includes/prod_short.md)]**.

3. Agregue un control Terminar para detener el flujo si la cuenta de usuario de integración cambió la entidad.

La siguiente imagen muestra cómo definir el desencadenador de flujo y la condición de flujo.

:::image type="content" source="media/power-automate-flow-dataverse.png" alt-text="Descripción general de la configuración de desencadenador y condición del flujo":::

## <a name="notify-business-central-about-a-change"></a>Notificar un cambio a Business Central

Si el flujo no se detiene por la condición, debe notificar [!INCLUDE[prod_short](includes/prod_short.md)] que se produjo un cambio. Utilice el conector de [!INCLUDE[prod_short](includes/prod_short.md)] para ello.

1. En la bifurcación **No** del paso de condición, agregue una acción y busque **Dynamics 365 [!INCLUDE[prod_short](includes/prod_short.md)]**. Elija el icono de conector en la lista.
2. Seleccione la acción **Crear registro (V3)**.

:::image type="content" source="media/power-automate-flow-dataverse-connector.png" alt-text="Configuración para el conector [!INCLUDE[prod_short](includes/prod_short.md)]":::

3. Utilice el botón **assist edit (...)** de la esquina superior derecha para agregar la conexión a su [!INCLUDE[prod_short](includes/prod_short.md)].
4. Cuando esté conectado, rellene los campos **Nombre del entorno** y **Nombre de empresa**.
5. En el campo **Categoría de API**, ingrese **microsoft/dataverse/v1.0**.
6. En el campo **Nombre de tabla**, introduzca **dataverseEntityChanges**.
7. En el campo **entityName**, escriba **cuenta**.
8. Guarde el flujo.

La imagen siguiente muestra el aspector que debería tener el flujo.

:::image type="content" source="media/power-automate-flow-dataverse-summary.png" alt-text="Resumen de todas las configuraciones para el flujo":::

Cuando agrega, elimina o modifica una cuenta de su entorno de [!INCLUDE [cds_long_md](includes/cds_long_md.md)], este flujo realizará las siguientes acciones:

1. Llama al entorno de [!INCLUDE[prod_short](includes/prod_short.md)] que especificó en el conector de [!INCLUDE[prod_short](includes/prod_short.md)].
2. Utilice la API [!INCLUDE[prod_short](includes/prod_short.md)] para insertar un registro con **entityName** ajustado a **cuenta** en la tabla **Cambio de entrada de Dataverse**. Este parámetro es el nombre exacto de la entidad Dataverse para la que está creando el flujo de trabajo.
3. [!INCLUDE[prod_short](includes/prod_short.md)] iniciará la entrada de la cola de trabajos que sincroniza clientes con cuentas.

## <a name="see-also"></a>Consulte también

[Usar Business Central en flujos de Power Automate](across-how-use-financials-data-source-flow.md)  
[Configurar flujos de trabajo automatizados](/dynamics365/business-central/dev-itpro/powerplatform/automate-workflows)  
[Integración con Microsoft Dataverse](admin-common-data-service.md)  
[Sincronización de datos en Business Central con Microsoft Dataverse](admin-synchronizing-business-central-and-sales.md)  
