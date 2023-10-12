---
title: Cambiar la configuración básica del usuario actual
description: 'Aprenda a cambiar algunas configuraciones básicas en Business Central, por ejemplo, su rol y centro de roles, empresa, fecha de trabajo y zonas horarias.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'change Role Center, notification, change company, change work date, decimal separator'
ms.search.form: '9022, 9019, 9027, 9020, 9026, 9030, 9000, 9009, 9004, 9005, 9024, 9006, 9007, 9010, 9016, 9017'
ms.date: 08/31/2022
ms.author: bholtorf
---
# <a name="change-basic-settings"></a>Cambiar la configuración básica

En la página **Mi configuración**, puede ver y cambiar la configuración básica de su [!INCLUDE[prod_short](includes/prod_short.md)]. Los cambios que realice sólo afectan a su área de trabajo; no a las áreas de trabajo de otros usuarios.  

[!INCLUDE [about-ui-learn](includes/about-ui-learn.md)]

## <a name="role"></a><a name="role-center"></a>Función

La función determina la página de inicio, una pantalla de inicio que está designada para las necesidades específicas del trabajo en una empresa. Dependiendo de su función, la página de inicio o el área de trabajo le brinda una descripción general del negocio, su departamento o sus tareas personales. También le ayuda a navegar por sus tareas diarias y encontrar el trabajo que le asignaron.

* En la parte superior, la navegación le permite cambiar entre clientes, proveedores, artículos y otras listas importantes de información. Del mismo modo, las acciones le permiten iniciar tareas, como crear una nueva factura de venta, directamente desde la página de inicio.

* En el centro, busque el área **Actividades**, que muestra los datos actuales y se puede seleccionar para ver información más detallada. Los indicadores de rendimiento clave (KPI) pueden configurarse para mostrar un gráfico seleccionado para una representación visual de, por ejemplo, el flujo de efectivo o ingresos y gastos. También puede crear una lista de clientes favoritos en la página de inicio para las cuentas de empresa con las que hace negocios a menudo o a las que necesita prestar especial atención.

### <a name="change-the-role"></a>Cambiar el rol

El rol pedido es **Administrador de negocio**, pero puede seleccionar otro rol para usar un área de trabajo que se adapte mejor a sus necesidades.  

1. En la esquina superior derecha, elija el icono **Configuración** ![Configuración.](media/ui-experience/settings_icon_small.png "Icono de configuración para el área de trabajo") y, a continuación, elija la acción **Mi configuración**.
2. En la página **Mi configuración**, en el campo **Rol**, seleccione el rol que desea usar de forma predeterminada. Por ejemplo, seleccione **Contable**.
3. Elija **Aceptar**.

## <a name="company"></a><a name="company"></a>Compañía

Una empresa funciona como un contenedor de datos en [!INCLUDE[prod_short](includes/prod_short.md)]. Puede haber múltiples empresas en una base de datos, pero solo se puede seleccionar una a la vez. La empresa predeterminada se llama CRONUS y solo contiene datos de demostración.

El campo **Empresa** muestra la empresa en la que trabaja actualmente y puede usarlo para cambiar a otra empresa. El nombre de la empresa siempre se muestra en la esquina superior izquierda y funciona como una acción que puede elegir para volver al área de trabajo.

> [!TIP]
> También puede cambiar la empresa utilizando el conmutador de empresas (Crtl+O). Para obtener más información acerca de esta función y otras formas de cambiar de empresa o entorno, consulte [Cambiar a otra empresa o entorno](ui-organization-switch.md).

La empresa predeterminada se llama CRONUS y solo contiene datos de demostración. Puede crear una nueva empresa con datos personalizados. Para obtener más información, consulte [Crear nuevas empresas](about-new-company.md).

<!--
### <a name="to-change-the-company-name"></a>To change the company name

The company name is always displayed at the top left corner and works as an action that you can choose to go back to the Role Center. You can change this name on the **Company Information** page.

1. Choose the ![Sprocket icon to open the Settings menu.](media/ui-experience/settings_icon_small.png) icon, and then choose the **Company Information** action.
2. In the **Name** field, enter the new company name.
3. Leave the page. The system restarts and displays the new company in the top-left corner.

### <a name="to-display-a-company-badge-for-quick-access-to-company-information"></a><a name="badge"></a>To display a company badge for quick access to company information

You can add a customized badge in the top-right corner, which you can choose to quickly view company name and tenant information in a pop-up box. The company badge is also useful when [!INCLUDE[prod_short](includes/prod_short.md)] is embedded in another application, like Microsoft Teams or in some other web application. In these cases, because the [!INCLUDE[web_client](includes/web_client.md)] displays less surrounding contextual information, the company badge serves as the only way to determine which company or environment a record belongs to.

1. Choose the ![Lightbulb that opens the Tell Me feature.](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Company Information**, and then choose the related link.
2. On the **Company Badge** FastTab, fill in the fields as necessary. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)].

> [!NOTE]
> If a company badge is defined, then you cannot change the company name as described in [To change the company name](ui-change-basic-settings.md#to-change-the-company-name)-->

## <a name="work-date"></a><a name="work-date"></a>Fecha de trabajo

La fecha de trabajo más utilizada es la fecha actual. Es posible que tenga que cambiar temporalmente la fecha de trabajo para realizar tareas como la finalización de las transacciones de una fecha que no sea hoy.

> [!TIP]  
> En todos los campos de fecha, escriba **h**para introducir rápidamente la fecha de hoy y escriba **t** para introducir rápidamente la fecha de trabajo, que es el valor en el campo **Fecha de trabajo** en la página **Mi configuración**.

> [!IMPORTANT]  
> Después de modificar la fecha de trabajo, si cierra la sesión o cambia a otra empresa, los datos de trabajo vuelven a la fecha de trabajo predeterminada. Por lo tanto, la próxima vez que inicie sesión o vuelva a cambiar a la empresa original, es posible que tenga que volver a establecer la fecha de trabajo.

### <a name="work-date-indication"></a>Indicación de la fecha de trabajo

La fecha de trabajo es fundamental en las páginas que se pueden editar. Siempre que la fecha de trabajo no se establezca en la fecha de hoy en una página editable, aparecen dos tipos de indicadores en la página:

* Aparece un recordatorio en la parte superior de la página que le indica cuál es la fecha de trabajo establecida. El recordatorio proporciona un vínculo directo a la configuración de la fecha de trabajo en la página **Mi configuración** para que pueda cambiar la fecha si lo desea. Desde el recordatorio, también puede elegir descartarlo para el resto de la sesión. A menos que cambie la fecha de trabajo a "hoy", el recordatorio aparecerá la próxima vez que inicie sesión.

* Si descarta el recordatorio, la fecha de trabajo aparecerá en el título de la página.  

Si la fecha de trabajo no está establecida en el día actual (hoy), la fecha de trabajo actual aparece en la esquina superior izquierda de todas las páginas donde puede editar datos.

## <a name="region"></a><a name="region"></a>Región

El valor **Región** determina cómo se muestran o se forman las fechas, los tiempos, los números, y divisas. También determina qué carácter se usa como separador decimal cuando se usa un teclado numérico para introducir datos. Obtenga más información en [Introducción de datos](ui-enter-data.md#decimal).

## <a name="language"></a><a name="language"></a>Idioma

Cambia el idioma de la pantalla. Este campo aparece sólo cuando hay más de un idioma a elegir.

El idioma inicial lo determina el administrador o la configuración de su navegador cuando inicia sesión en [!INCLUDE[prod_short](includes/prod_short.md)]. El idioma que establezca se usará en todos los dispositivos desde los que inicie sesión, como un teléfono o una tableta.

Los idiomas adicionales para [!INCLUDE[prod_short](includes/prod_short.md)] se pueden instalar desde AppSource. Si bien todos los idiomas de visualización compatibles se muestran en la lista, el administrador debe instalar la aplicación de idioma pertinente para el suscriptor antes de que los usuarios puedan cambiar al nuevo idioma en [!INCLUDE[prod_short](includes/prod_short.md)].  

## <a name="time-zone"></a>Zona horaria

Define la zona horaria en la que se encuentra. Cuando inicia sesión por primera vez en [!INCLUDE [prod_short](includes/prod_short.md)], la zona horaria se establece en función de la dirección de su empresa. Cámbiela si no se ajusta a su ubicación física.  

## <a name="notifications"></a>Notificaciones

Seleccione el vínculo *Cambiar cuándo recibo notificaciones* para ver o cambiar las notificaciones que recibe sobre determinados eventos o cambios de estado, cuando va a facturar a un cliente que tiene un saldo vencido o cuando el inventario disponible es inferior a la cantidad que va a vender, por ejemplo. Obtenga más información en [Administrar notificaciones](ui-smart-notifications.md).

## <a name="teaching-tips"></a>Consejos didácticos

[!INCLUDE [ua-teachingtips](includes/ua-teachingtips.md)]

## <a name="see-also"></a>Consulte también .

[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Cambiar las funciones que se muestran](ui-experiences.md)  
[Crear nuevas en empresas](about-new-company.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
