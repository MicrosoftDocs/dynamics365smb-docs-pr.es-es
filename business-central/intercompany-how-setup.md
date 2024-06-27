---
title: Configuración de registro de transacciones entre empresas
description: Aprenda a configurar una asociación entre empresas.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: how-to
ms.date: 09/27/2023
ms.custom: bap-template
ms.search.keywords: 'IC, group, consolidation, affiliate, subsidiary'
ms.search.form: '605, 620, 602, 603, 601, 600, 652, 653, 606, 607, 609, 608, 621, 653_Primary'
ms.service: dynamics-365-business-central
---
# <a name="set-up-intercompany-transactions"></a>Configurar transacciones entre empresas vinculadas

Las asociaciones entre empresas facilitan el manejo de los procesos contables cuando dos o más filiales de una empresa hacen negocios entre sí con frecuencia. Los socios pueden intercambiar transacciones, como ventas y compras, y gestionarlas de forma manual o automática. Por ejemplo, cuando un socio envía una línea de diario de ventas a otro socio, se crea una línea de diario de compras para el socio receptor.

El plan de cuentas de empresas vinculadas puede ser, por ejemplo, una versión del plan de cuentas del socio de sincronización. Cada socio asigna sus cuentas al plan de cuentas de empresas vinculadas. Cada socio también asigna sus dimensiones y valores de dimensión a las dimensiones de empresas vinculadas.

> [!NOTE]
> En el primer lanzamiento de versiones de 2023, presentamos una página mejorada de **Configuración de empresas vinculadas**. La nueva página facilita la configuración de una asociación entre empresas al consolidar todas las tareas de configuración en una sola página. Si es nuevo en [!INCLUDE [prod_short](includes/prod_short.md)], ya está usando la nueva experiencia. Si ya es un cliente, su administrador puede activar el conmutador de la característica **Aceptar automáticamente transacciones de diario general entre empresas** en la página **Gestión de funciones**.
>
> Las tareas de este artículo asumen que el interruptor de la característica está activado. Si ya configuró una asociación entre empresas, puede continuar usándola.

## <a name="before-you-start"></a>Antes de comenzar

Antes de comenzar a configurar su asociación entre empresas, hay algunas decisiones que tomar.

|Decisión  |Descripción  |
|---------|---------|
|¿Qué plan de cuentas debe ser la base para el plan de cuentas de empresas vinculadas?     | Todas las empresas de la sociedad deben utilizar el mismo plan de cuentas de empresas vinculadas. Puede basar su plan de cuentas de empresas vinculadas en el plan de cuentas de una de las empresas de la sociedad o crear un nuevo plan de cuentas de empresas vinculadas. Las cuentas que se van a utilizar en la asociación se asignan de ambas maneras, de modo que cada socio envía y recibe transacciones en las cuentas correctas. Obtenga más información sobre cómo configurar el plan de cuentas de empresas vinculadas en [Configurar los planes de cuentas de empresas vinculadas](#set-up-the-intercompany-charts-of-accounts).         |
|¿Qué dimensiones deben ser la base para las dimensiones de empresas vinculadas?     | Si utiliza dimensiones de empresas vinculadas, deben ser las mismas para todas las empresas de la asociación. Después de especificar sus dimensiones de empresas vinculadas, asigne sus valores de dimensión. Obtenga más información sobre la asignación de valores de dimensión en [Configurar dimensiones de empresas vinculadas](#set-up-intercompany-dimensions).        |
|¿Qué socios son clientes o proveedores, o ambos?     |  Obtenga más información sobre cómo configurar las empresas de clientes y proveedores en una asociación entre empresas vinculadas en [Configurar socios entre empresas como clientes y proveedores](#set-up-intercompany-partners-as-customers-and-vendors).       |
|¿Quiere especificar cuentas bancarias para usar en la asociación?| Puede acelerar el proceso de registro de transacciones de pago especificando la cuenta bancaria que se utilizará para cada empresa de socio. Obtenga más información en [Especificar las cuentas bancarias que se usarán para los socios de empresas vinculadas](#specify-the-bank-accounts-to-use-for-intercompany-partners). |
|¿Cómo desea identificar a las empresas en la asociación?     | Todas las partes deben acordar un código de identificación de socio de empresas vinculadas para cada empresa. Asignará el código a las tarjetas de cliente y proveedor, para identificar transacciones relacionadas. Obtenga más información sobre los identificadores en [Crear serie numérica](ui-create-number-series.md).        |
|¿Cómo desea manejar los números de producto?"     | Si las líneas de empresas vinculadas contienen productos, puede utilizar sus propios números de producto o configurar los números de producto de sus socios para cada producto que corresponda, ya sea en el campo **N.º de producto de proveedor** o en el campo **N.º de producto común** en la ficha del producto. También puede usar la acción **Referencia del producto** para asignar los números de sus productos a las descripciones de los productos de sus socios de empresas vinculadas. Para obtener más información sobre las referencias de productos, vaya a [Usar referencias de productos](inventory-how-use-item-cross-refs.md).        |
|¿Están involucrados los recursos?     | Si las transacciones de ventas entre empresas vinculadas van a incluir recursos, debe rellenar el campo **N.º cuenta de contabilidad de compras de IC** en la tarjeta de recurso de cada recurso. El campo contiene el número de la cuenta contable de empresas vinculadas que la cuenta de este recurso contabilizará en la empresa asociada. Para obtener más información sobre rcursos, vaya a [Configurar recursos](projects-how-setup-resources.md).<br><br>**NOTA**<br>Las transacciones de compra entre empresas que incluyen recursos, activos fijos y cargos por artículos no son totalmente compatibles. En la empresa de socio, el campo **Tipo de línea** estará en blanco en las líneas del documento de compra que incluyan estas entidades. Debe actualizar el campo manualmente.        |

## <a name="overview-of-the-steps-to-get-started"></a>Resumen de los pasos a seguir para empezar

Utilice la página **Configuración de empresas vinculadas** para configurar los siguientes componentes de las transacciones de empresas vinculadas:

* La configuración de empresas vinculadas de su empresa.
* La empresa que será el socio de sincronización.
* El plan de cuentas de empresas vinculadas que todos los socios usan para intercambiar transacciones.
* Las asignaciones entre cuentas en el plan de cuentas y el plan de cuentas de empresas vinculadas para transacciones entrantes y salientes para cada socio.
* Las dimensiones y valores de dimensión de empresas vinculadas a usar, y cómo se asignan a las dimensiones para cada socio.
* Las empresas que son los socios de empresas vinculadas.
* Las empresas que son proveedores o clientes, o ambos.

## <a name="set-up-a-synchronization-partner"></a>Configurar un socio de sincronización

Todos los socios deben usar el mismo plan de cuentas de empresas vinculadas y, si es necesario, las mismas dimensiones de empresas vinculadas. Puede ahorrar tiempo al configurar la asociación utilizando el plan de cuentas y las dimensiones de uno de los socios como línea de base para el plan de cuentas y las dimensiones de empresas vinculadas. La empresa que utiliza como referencia se denomina *socio de sincronización*. Por lo general, el socio de sincronización es la empresa central, pero no tiene por qué serlo.

En la página **Configuración de empresas vinculadas**, cada socio especifica el socio de sincronización en el campo **Socio de sincronización** . Posteriormente, el plan de cuentas de empresas vinculadas y las dimensiones de empresas vinculadas se especifican automáticamente para ellos, en función de la configuración del socio de sincronización. A continuación, los socios utilizan las páginas **Asignación de plan de cuentas de empresas vinculadas** y **Asignación de dimensiones de empresas vinculadas** para asignar su plan de cuentas y dimensiones al plan de cuentas y dimensiones de empresas vinculadas, y viceversa. 

> [!NOTE]
> Es importante asignar cuentas y dimensiones en ambas direcciones. Es decir, tanto al plan de cuentas y dimensiones de empresas vinculadas, como de ellos a sus propias cuentas y dimensiones.

### <a name="connect-with-partners-in-another-tenant-or-environment"></a>Conectarse con socios en otro inquilino o entorno

Si uno o más socios [!INCLUDE [prod_short](includes/prod_short.md)] se encuentran en otro inquilino o entorno, existen algunos pasos adicionales para crear la conexión. Los pasos se aplican a todos los socios de otro inquilino o entorno.

* Configure [!INCLUDE [prod_short](includes/prod_short.md)] como una aplicación registrada en Azure Portal.
* Agregue y habilite el registro de la aplicación en [!INCLUDE [prod_short](includes/prod_short.md)].
* Intercambie información sobre sus configuraciones de empresas vinculadas. Cada socio puede obtener esta información en **Configuración entre empresas**, **Acciones**, **Detalles de conexión**.

   |Copiar de la configuración del socio  |Copiar a su configuración  |
   |---------|---------|
   |URL de conexión actual     |URL de conexión de socio IC         |
   |Id. de empresa actual     |Id. empresa socio IC         |
   |Id. empresas vinculadas     |Id. de empresas vinculadas del socio IC         |
   |Nombre de la empresa     |Nombre de empresa de socio IC         |

* Cambie las siguientes configuraciones de autenticación de manera que [!INCLUDE [prod_short](includes/prod_short.md)] pueda autenticarse cuando se conecte. Cada socio puede obtener esta información desde su aplicación registrada. Para obtener más información sobre cómo crear una aplicación registrada, vaya a [Crear una aplicación registrada en Azure Portal](#create-a-registered-app-in-azure-portal).  

  * Id. de cliente
  * Secreto del cliente
  * Extremo de token
  * URL de redireccionamiento

Ejecute **Configuración de empresas vinculadas**, **Acciones**, **Detalles de conexión** en todas las empresas para especificar la información. 

#### <a name="create-a-registered-app-in-azure-portal"></a>Crear una aplicación registrada en Azure Portal

Este proceso solo es necesario si desea conectarse con un socio cuyo [!INCLUDE [prod_short](includes/prod_short.md)] se encuentra en un inquilino o entorno diferente.

> [!TIP]
> Es buena idea tener abierto un editor de texto, como el Bloc de notas, mientras crea su aplicación registrada. Necesitará parte de la información cuando ejecute la **Conf. empresa vinculada**, **Acciones**, **Detalles de conexión**, por lo que es bueno tener la información a mano.

1. Vaya a [Azure Portal](https://portal.azure.com/#home).
2. Elija el servicio **Microsoft Entra ID**.
3. En el panel de navegación, elija **Registros de aplicación**.
4. En la página **Registros de aplicación**, elija **nuevo registro**.
5. Dé un nombre a la aplicación.
6. Elija el tipo de cuenta **Cuentas en cualquier directorio organizacional (cualquier inquilino - multiinquilino de Microsoft Entra)**.
7. Para el URI de redireccionamiento, en el campo **Seleccionar una plataforma** , elija **Web** y luego proporcione el URI. Por ejemplo, \**https://businesscentral.dynamics.com/OAuthLanding.htm**.

  Si está trabajando con un ISV integrado, es posible que necesite un URI diferente.

8. Registre la aplicación.
9. En la página **Aplicación intercompañía**, en el panel de navegación, elija **Permisos de API**.
10. Elija la acción **Agregar un permiso**.
11. En la pestaña **API de Microsoft**, elija **Dynamics 365 Business Central**.
12. En el panel **Solicitar permisos de API**, elija **Permisos de aplicación** y luego elija el permiso **API.ReadWrite.All**.
13. En la página **Aplicación intercompañía | Permisos de API** , elija la acción **Conceder consentimiento de administrador para Contoso** y luego otorgue el consentimiento.
14. En el panel de navegación, elija **Certificados y secretos**.
15. Elija la pestaña **Secretos de cliente** y luego elija **Nuevo secreto de cliente**.
16. En el panel **Agregar un secreto de cliente**, escriba un nombre para el secreto y especifique cuándo caducará.

  > [!NOTE]
  > Todos los socios que se encuentren en entornos diferentes deberán renovar el secreto antes de que caduque.

  > [!IMPORTANT]
  > Copie el id. en el campo **Valor** antes de salir de la página **Aplicación intercompañía | Certificados y secretos**. Lo necesitará en un paso posterior y no estará disponible después de salir de la página. Por ejemplo, pegue el valor en un editor de texto.

17. En el panel de navegación, elija **Información general**.
18. Copie el valor en el campo **Id. de la aplicación (cliente)**. Por ejemplo, pegue el valor en un editor de texto.
19. Elija la acción **Extremos** y luego copie el valor en el campo **Punto de conexión de token OAuth 2.0 (v2)**. Por ejemplo, pegue el valor en un editor de texto.
20. Copie el valor en el campo **Id. de directorio (inquilino)**. Por ejemplo, pegue el valor en un editor de texto.
21. En el valor del token que ha copiado, reemplace **organizaciones** por el valor que ha copiado del campo **Id. de directorio (inquilino)** en el paso anterior.

#### <a name="add-and-enable-your-registered-app-in-business-central"></a>Agregue y habilite su aplicación registrada en Business Central

1. Elija el icono ![Bombilla que abre la característica Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Tarjeta de aplicación de Microsoft Entra** y, a continuación, elija el vínculo relacionado.  
2. Rellene los campos según sea necesario. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]
3. En el campo **Estado**, elija **Habilitado**. 
4. Elija la acción **Conceder consentimiento**. 
5. En el campo **Conjunto de permisos**, elija los conjuntos de permisos **D365 INTERCOMPANY CE & DATA ACCESS IC CE**.

## <a name="set-up-the-intercompany-charts-of-accounts"></a>Configurar los planes de cuentas de las empresas vinculadas

Todos los socios deben utilizar el mismo plan de cuentas de empresas vinculadas y asignarle las cuentas de su propio plan de cuentas. Si el plan de cuentas de su empresa define el plan de cuentas de empresas vinculadas para sus empresas asociadas, siga los pasos de esta sección.

Si usa un archivo XML que contiene el plan de cuentas de empresas vinculadas, siga los pasos de [Importar o exportar un plan de cuentas de empresas vinculadas](intercompany-how-setup.md#import-or-export-an-intercompany-chart-of-accounts).  

1. Elija el icono ![Bombilla que abre la característica Dígame](media/ui-search/search_small.png "Dígame qué desea hacer") icono, escriba **Configuración de empresas vinculadas** y luego elija el enlace relacionado.
2. Elija la acción **Plan de cuentas de empresas vinculadas**.
3. Para agregar cuentas, haga una de las cosas siguientes en la página **Plan de cuentas de empresas vinculadas**:
    * Elija **Nuevo** y luego introduzca cada cuenta en una línea de la página.  
    * Si su plan de cuentas de empresas vinculadas va a ser idéntico o similar al suyo habitual, puede rellenar la página automáticamente mediante la acción **Copiar de Plan de cuentas**. Puede editar las líneas nuevas si es necesario.
    * Si configuró un plan de cuentas de empresas vinculadas para un socio de sincronización, utilice la acción **Configuración de sincronización** para copiar esas cuentas.

    > [!TIP]
    > Si copia el plan de cuentas de empresas vinculadas de un socio de sincronización, puede usar la acción **Configuración de sincronización** para actualizar sus cuentas de empresas vinculadas con cualquier cambio que el socio realice en las suyas.

El próximo paso es asignar su plan de cuentas al plan de cuentas de empresas vinculadas. Más información en [Asignar el plan de cuentas de empresas vinculadas al plan de cuentas de la empresa propia](#map-the-intercompany-chart-of-accounts-to-your-companys-chart-of-accounts).

### <a name="import-or-export-an-intercompany-chart-of-accounts"></a>Importar o exportar el plan de cuentas de empresas vinculadas

La empresa de sincronización puede compartir su plan de cuentas con socios exportándolo a un archivo. Los socios pueden importar el archivo para obtener el plan de cuentas.

1. Elija el icono ![Bombilla que abre la característica Dígame](media/ui-search/search_small.png "Dígame qué desea hacer") icono, escriba **Configuración de empresas vinculadas** y luego elija el enlace relacionado.
2. Elija la acción **Plan de cuentas de empresas vinculadas**.
3. En la página **Plan de cuentas de empresas vinculadas**, seleccione la acción **Importar/Exportar** y, a continuación, **Importar** o **Exportar**.
4. Elija el archivo para importar o exportar.  

La página **Plan de cuentas de empresas vinculadas** se rellena con las líneas de cuentas de contabilidad nuevas o modificadas, según el plan de cuentas de empresas vinculadas del archivo. Las líneas existentes, no relacionadas en la página permanecen sin cambios.

## <a name="map-the-intercompany-chart-of-accounts-to-your-companys-chart-of-accounts"></a>Asignar el plan de cuentas de empresas vinculadas al plan de cuentas de la empresa propia

Cuando haya definido o importado el catálogo de cuentas de empresas vinculadas, asigne cada cuenta de empresas vinculadas a una de sus cuentas. En la página **Plan de cuentas de empresas vinculadas**, puede especificar cómo se transformarán las cuentas de contabilidad de empresas vinculadas en transacciones entrantes, en cuentas del plan de cuentas de su empresa.

Si las cuentas de empresas vinculadas y sus cuentas tienen los mismos números, puede asignar las cuentas automáticamente.

1. Elija el icono ![Bombilla que abre la característica Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") icono, escriba **Configuración de empresas vinculadas** y luego elija el enlace relacionado.  
2. Elija la acción **Plan de cuentas de empresas vinculadas**.

    > [!TIP]
    > Para acceder a las acciones de la página, es posible que deba expandir la página a la vista de diseño amplia.

3. En la página **Plan de cuentas de empresas vinculadas**, seleccione la acción **Asignar plan de cuentas**.
4. Puede asignar las cuentas de forma automática o manual.

    * Para crear manualmente la asignación, en los paneles **Plan de cuentas de empresas vinculadas** y **Plan de cuentas de contabilidad**, seleccione una cuenta y, a continuación, elija una cuenta en el **N.º de contabilidad.** y **N.º de empresa vinculada.** .
    * Para asignar automáticamente cuentas que tienen los mismos números, seleccione las líneas que desea asignar, elija la acción **Asignar a cuenta con mismo N.º** y luego elija el plan de cuentas a actualizar.

    > [!TIP]
    > Si desea asignar muchas o quizás todas las cuentas, elija una línea, elija :::image type="icon" source="media/show-more-options-icon.png" border="false"::: y luego elija **Seleccionar más**.

## <a name="set-up-intercompany-dimensions"></a>Configurar dimensiones de empresas vinculadas

Si los socios van a intercambiar transacciones con dimensiones relacionadas con ellos, debe estar de acuerdo en las dimensiones que todos usarán. Por ejemplo, la empresa de sincronización puede crear una versión simplificada de sus dimensiones, exportarlas a un archivo XML y luego distribuir el archivo a cada socio. Cada socio puede importar el archivo XML en la página **Dimensiones de empresas vinculadas** y luego asignar las dimensiones de empresas vinculadas a sus dimensiones. Más información en [Asignar dimensiones de empresas vinculadas a las dimensiones de su empresa](#map-intercompany-dimensions-to-your-companys-dimensions).

> [!NOTE]
> Cada empresa debe asignar sus dimensiones a las dimensiones de empresas vinculadas para documentos salientes y documentos entrantes. La asignación de cuentas en ambas direcciones es importante y ayuda a mantener la coherencia entre las empresas.

Si los socios utilizarán las dimensiones de empresas vinculadas del socio de sincronización, siga los pasos de esta sección. Si quiere compartir usando un archivo XML que contiene las dimensiones de empresas vinculadas, siga los pasos de [Importar o exportar dimensiones de empresas vinculadas](#import-or-export-intercompany-dimensions).

1. Elija el icono ![Bombilla que abre la característica Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") icono, escriba **Configuración de empresas vinculadas** y luego elija el enlace relacionado.  
2. Seleccione la acción **Dimensiones de empresas vinculadas**.
3. Para agregar dimensiones, haga algo de lo siguiente en la página **Dimensiones de empresas vinculadas**:
    * Elija **Nuevo** y luego introduzca cada dimensión en una línea.  
    * Si sus dimensiones de empresas vinculadas van a ser idénticas o similares a sus dimensiones regulares, puede rellenar la página automáticamente mediante la acción **Copiar de dimensiones**. Luego, puede editar las líneas nuevas si es necesario.
    * Si ha especificado unas dimensiones de empresas vinculadas especificadas para un socio de sincronización, utilice la acción **Configuración de sincronización** para copiar esas dimensiones.

    > [!TIP]
    > Si copia las dimensiones de empresas vinculadas de un socio de sincronización, puede usar la acción **Configuración de sincronización** para actualizarlas dimensiones de las empresas vinculadas con cualquier cambio que el socio realice en las suyas.  

### <a name="import-or-export-intercompany-dimensions"></a>Importar o exportar dimensiones de empresas vinculadas

La empresa de sincronización puede compartir sus dimensiones con socios exportándolas a un archivo. Los socios pueden importar el archivo para obtener las dimensiones.

1. Elija el icono ![Bombilla que abre la característica Dígame](media/ui-search/search_small.png "Dígame qué desea hacer") icono, escriba **Configuración de empresas vinculadas** y luego elija el enlace relacionado.
2. Seleccione la acción **Dimensiones de empresas vinculadas**.  
3. En la página **Dimensiones de empresas vinculadas**, seleccione la acción **Importar/Exportar** y, a continuación, **Importar** o **Exportar**.
4. Elija el archivo para importar o exportar.

El siguiente paso es asignar las dimensiones con las cimensiones de empresas vinculadas. Más información en [Asignar dimensiones de empresas vinculadas a las dimensiones de su empresa](#map-intercompany-dimensions-to-your-companys-dimensions).

### <a name="map-intercompany-dimensions-to-your-companys-dimensions"></a>Asignar dimensiones de empresas vinculadas a las dimensiones de su empresa

Una vez especifique las dimensiones que usará, asigne cada una de las dimensiones de empresas vinculadas a una de las dimensiones de su empresa y a la inversa. Utilice la página **Asignación de dimensiones entre empresas vinculadas** para especificar la asignación. Luego, repita el proceso para los valores de dimensión.

* Especifique cómo se asignan las dimensiones de empresas vinculadas en las transacciones entrantes a las dimensiones de la lista de dimensiones de su empresa.
* Especifique cómo se transformarán sus dimensiones en dimensiones de empresas vinculadas, en *transacciones salientes*.

Si alguna de las dimensiones de empresas vinculadas tiene el mismo código que las dimensiones correspondientes de su empresa, puede dejar que el programa realice automáticamente las asignaciones de dimensión.  

En los siguientes pasos, primero asigna dimensiones de empresas vinculadas a dimensiones para documentos entrantes en el panel **Dimensiones de empresas vinculadas**. Luego, asigna dimensiones a dimensiones de empresas vinculadas para documentos salientes en el panel **Dimensiones de la empresa actual**.

1. Elija el icono ![Bombilla que abre la característica Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") icono, escriba **Configuración de empresas vinculadas** y luego elija el enlace relacionado.
2. Seleccione la acción **Dimensiones de empresas vinculadas**.
3. En la página **Dimensiones de empresas vinculadas**, seleccione la acción **Asignación de dimensiones**.
4. Puede asignar las dimensiones de forma automática o manual.

    * Para crear manualmente la asignación, en los paneles **Dimensiones de empresas vinculadas** y **Dimensiones de la empresa actual** , elija una dimensión y luego elija una dimensión en los campos **Código de dimensión** y **Código de dimensión de empresas vinculadas**.
    * Para asignar automáticamente cuentas que tienen los mismos números, seleccione las líneas que desea asignar, elija la acción **Asignar dimensiones con el mismo código** y luego elija las dimensiones a actualizar. 

    > [!TIP]
    > Si desea asignar muchas o quizás todas las dimensiones, elija una línea, elija :::image type="icon" source="media/show-more-options-icon.png" border="false"::: y luego elija **Seleccionar más**.

5. Seleccione la acción **Asignación de valores de dimensiones**.
6. En la página **Asignación de valores de dimensión de empresas vinculadas** , los pasos para crear la asignación son similares a los que acaba de hacer para las dimensiones.

## <a name="set-up-intercompany-general-journal-templates-and-batches"></a>Configurar plantillas y lotes del diario general de empresas vinculadas

Debe configurar una plantilla de diario general y un lote de diario general para usar de forma predeterminada para las transacciones entre empresas. La plantilla y el lote son especialmente importantes si acepta automáticamente transacciones entre empresas de sus socios. Para obtener más información sobre la aceptación automática de transacciones, vaya a [Aceptación automática de transacciones de socios de empresas vinculadas](#auto-accept-transactions-from-intercompany-partners).   

* Los diarios generales se utilizan para registrar en cuentas contables y otras cuentas, como bancarias, de clientes y de proveedores. Registrar con un diario general siempre crea movimientos en cuentas contables.  Utilice la página **Diario general de empresas vinculadas** para configurar el lote de diario general que se utilizará. La configuración que es específica para las transacciones entre empresas son las cuentas que especifica en los campos **Tipo de cuenta de empresa vinculada** y **Número de cuenta de empresa vinculada**.
* Las plantillas de diario le ofrecen una página de diario diseñada para un propósito específico. O sea, los campos de las plantillas de diario son exactamente las necesarias para una parte particular del programa. Utilice la página **Plantillas de diario general** para configurar una plantilla para usar en transacciones entre empresas.

Para obtener más información sobre las plantillas y lotes de diarios generales, vaya a [Usar plantillas y lotes de diarios](ui-work-general-journals.md#use-journal-templates-and-batches).

## <a name="set-up-a-company-for-intercompany-transactions"></a>Establecer una empresa para transacciones entre empresas vinculadas

Los siguientes pasos asumen que un socio de sincronización está configurado con el plan de cuentas y las dimensiones en las que basará el plan de cuentas y las dimensiones de empresas vinculadas. Puede configurarlos usted mismo, pero normalmente es más rápido comenzar y el mantenimiento es más fácil si utiliza un socio de sincronización. Obtenga más información sobre el socio de sincronización, vaya a [Configurar un socio de sincronización](#set-up-a-synchronization-partner).

> [!TIP]
> Es una buena idea completar los campos de la ficha desplegable **General** en la página **Configuración de empresas vinculadas** para cada socio antes de que usted agregue a sus socios. Cuando agrega empresas asociadas que están en el mismo suscriptor, [!INCLUDE [prod_short](includes/prod_short.md)] obtiene su código de empresa vinculada y el nombre de la empresa de su configuración en la ficha desplegable General. El campo **Nombre de la empresa** verificará que su código IC sea único.

> [!NOTE]
> Si utilizará un socio de sincronización, deje el campo **Socio de sincronización** en blanco cuando configure esa empresa para la asociación.

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") icono, escriba **Configuración de empresas vinculadas** y luego elija el enlace relacionado.  
2. En la página **Configuración de empresas vinculadas**, rellene el resto de los campos de la ficha desplegable **General**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!NOTE]
> En [!INCLUDE[prod_short](includes/prod_short.md)] en línea, no puede utilizar ubicaciones de archivos para transferir transacciones a sus socios porque [!INCLUDE[prod_short](includes/prod_short.md)] no tiene acceso a su red local. Por tanto, si elige **Ubicación del archivo** en el campo **Tipo de transferencia**, el campo **Ruta de la carpeta** no está disponible. En su lugar, el archivo se descargará a la carpeta **Descargas** de su equipo. Luego envía el archivo a alguien de la empresa asociada, por ejemplo, por correo electrónico. Para un proceso más directo, le recomendamos que elija **Correo electrónico**.

El siguiente paso es configurar las empresas de socios.

## <a name="set-up-intercompany-partners"></a>Configurar socios de empresas vinculadas

Cada socio debe agregar todas las demás empresas de la asociación como si fueran un socio.

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") icono, escriba **Configuración de empresas vinculadas** y luego elija el enlace relacionado.
2. En la ficha desplegable **Socios de empresas vinculadas** , elija **Agregar**.
3. En la página **Socio de empresas vinculadas**, rellene los campos. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Repita los pasos 2 y 3 para todas las empresas de la asociación.

> [!NOTE]
> Para la contabilización de empresas vinculadas, si activa la alternancia **Aceptar automáticamente transacciones** en la página **Socio de empresas vinculadas**, [!INCLUDE[prod_short](includes/prod_short.md)] suprime los mensajes de advertencia sobre facturas de compra que duplican el pedido de compra original. Es importante contar con un proceso de empresa para gestionar los duplicados. Por ejemplo, eliminando dichos pedidos de compra cuando se recibe la factura de compra del socio de empresas vinculadas.

### <a name="set-up-intercompany-partners-as-customers-and-vendors"></a>Configurar socios de empresas vinculadas como empresas y proveedores

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") icono, escriba **Configuración de empresas vinculadas** y luego elija el enlace relacionado.
2. En la ficha desplegable **Socios de empresas vinculadas** , abra la página de la tarjeta del socio.
3. Según lo que desee hacer, elija el cliente o socio en los campos **N.º de cliente.** o **N.º de proveedor**.

    > [!NOTE]
    > Si no se ha creado el cliente o proveedor, puede elegir **+Nuevo** en el menú desplegable para configurarlos. Para obtener más información sobre cómo crear clientes y proveedores, vaya a [Registrar nuevos clientes](sales-how-register-new-customers.md) y [Registrar nuevos proveedores](purchasing-how-register-new-vendors.md).

    > [!TIP]
    > También puede especificar un cliente o proveedor como socio de empresas vinculadas, rellenando el campo **Código socio IC** en las páginas **Tarjeta de cliente** y **Tarjeta de proveedor**.

### <a name="set-up-default-intercompany-partner-general-ledger-accounts"></a>Configurar cuentas de contabilidad de socios de empresas vinculadas predeterminadas

Cuando crea una línea de venta o de compra de empresas vinculadas para enviarla como transacción saliente, introduzca una cuenta del plan de cuentas de empresas vinculadas como cuenta predeterminada en la que se contabiliza el importe en la empresa asociada. En la página **Tarjeta de cuenta contable**, para las cuentas que utiliza regularmente en líneas de ventas o compras salientes de empresas intervinculadas, puede especificar una cuenta genérica de empresa vinculada asociada. Por ejemplo, para su cuenta de clientes, puede introducir las cuentas de proveedores correspondientes desde el plan de cuentas de empresas vinculadas. Las cuentas de clientes y proveedores se utilizan como cuenta de compensación para el socio de empresas vinculadas cuando registra transacciones en los diarios generales de empresas vinculadas.  

Ahora, cuando introduzca una cuenta contable en el campo **Cta. contrapartida** en una línea de empresas vinculadas con **Socio de empresas vinculadas** en el campo **Tipo de cuenta** el campo **Cuentas genéricas de empresas vinculadas asociadas** se rellenará automáticamente.  

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Plan de cuentas** y luego elija el enlace relacionado.  
2. Abra la cuenta contable que se utiliza para transacciones entre empresas vinculadas y, en el campo **Cuentas contables predeterminadas de empresas vinculadas asociadas**, introduzca la cuenta de contabilidad general entre empresas vinculadas que su socio contabilizará cuando registre en la cuenta de contabilidad en la línea.
3. Repita el paso 2 para cada cuenta que introduzca a menudo en el campo **Cta. contrapartida** en un diario o documento de empresas vinculadas.

### <a name="auto-accept-transactions-from-intercompany-partners"></a>Aceptación automática de transacciones de socios de empresas vinculadas

Para agilizar el proceso de transacciones de empresas vinculadas, puede especificar si quiere que esta empresa cree automáticamente líneas de diario en función de las contabilizaciones de un socio de empresas vinculadas desde la página **Diario general de empresas vinculadas**. Para crear automáticamente transacciones entrantes y salientes, debe activar las siguientes opciones para cada socio:

* En la página **Configuración de empresas vinculadas**, active la opción **Enviar automáticamente transacciones** para el socio de sincronización. A continuación, especifique dónde crear las transacciones de diario de empresas vinculadas recibidas completando los campos **Plantilla Jnl. general de iC predeterminada** y **Lote Jnl. general de iC predeterminado**.

    > [!TIP]
    > Si el campo **Plantilla Jnl. general de iC predeterminada** está en blanco, debe configurar una plantilla de diario general para usar en sus diarios generales de empresas vinculadas. Para obtener más información sobre plantillas y lotes, vaya a [Configurar plantillas y lotes de diarios generales de empresas vinculadas](#set-up-intercompany-general-journal-templates-and-batches)    

* En la página **Socio de empresas vinculadas**, active la opción **Aceptar automáticamente transacciones** .

Las líneas de diario se crean automáticamente, pero no se contabilizan.

> [!NOTE]
> Si su organización usó características de empresas vinculadas en [!INCLUDE [prod_short](includes/prod_short.md)] antes del lanzamiento de versiones 1 de 2022, para aceptar transacciones automáticamente, su administrador debe activar el conmutador de característica **Aceptar automáticamente transacciones del diario general de empresas vinculadas** en la página **Administración de características**.

### <a name="specify-the-bank-accounts-to-use-for-intercompany-partners"></a>Especificar las cuentas bancarias que se usarán para los socios de empresas vinculadas

Para facilitar los pagos rápidos, especifique una o más cuentas bancarias para usar con socios de empresas vinculadas. Cuando un socio utiliza un diario general de empresas vinculadas para realizar un pago, puede especificar la cuenta bancaria en la línea. La cuenta bancaria se utiliza como cuenta de contrapartida en la empresa receptora, lo que minimiza la necesidad de introducir transacciones manualmente.

* Para especificar la cuenta bancaria a utilizar, en la página **Socios de empresas vinculadas** elija la acción **Cuentas bancarias**. En la **Tarjeta de cuenta bancaria interempresas**, introduzca la información de la cuenta.

## <a name="troubleshoot-your-intercompany-setup"></a>Solucionar problemas de configuración entre empresas

En la página **Configuración de empresas vinculadas**, el panel **Diagnósticos de configuración de empresas vinculadas** contiene mosaicos que indican si ha configurado todos los componentes necesarios para intercambiar transacciones entre empresas. Los mosaicos también están disponibles en el Área de trabajo de Business Manager. Elige los mosaicos para descubrir qué falta. Para obtener una descripción general de los componentes necesarios, vaya a [Descripción general de los pasos para comenzar](#overview-of-the-steps-to-get-started).

## <a name="see-also"></a>Consulte también

[Gestión de transacciones entre empresas vinculadas](intercompany-manage.md)  
[Finanzas](finance.md)  
[Configurar las finanzas](finance-setup-finance.md)  
[Trabajar con diarios generales](ui-work-general-journals.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
