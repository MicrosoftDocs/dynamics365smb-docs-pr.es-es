---
title: Cambiar a otra empresa o entorno
description: 'Si trabaja para varias organizaciones, puede cambiar rápidamente entre entornos y empresas.'
author: brentholtorf
ms.topic: conceptual
ms.search.keywords: 'environments, companies, tenants, organization'
ms.search.form: '9020, 9022, 9026, 9027, 9030, 9000, 9009, 9004, 9005, 9024, 9006, 9007, 9010, 9016, 9017'
ms.date: 08/16/2022
ms.author: bholtorf
ms.service: dynamics-365-business-central
---

# <a name="switching-to-another-company-or-environment"></a>Cambiar a otra empresa o entorno

[!INCLUDE [prod_short](includes/prod_short.md)] está disponible en muchos países y regiones diferentes y es compatible con muchos tipos diferentes de organizaciones. Su organización puede optar por organizar el trabajo en [!INCLUDE [prod_short](includes/prod_short.md)] en múltiples *compañías* y *entornos*. Este artículo lo ayuda a comprender las diferencias clave y cómo trabajar con ellas.

## <a name="about-companies-and-environments"></a>Acerca de empresas y entornos

[!INCLUDE [company_environment](includes/company_environment.md)]

> [!TIP]
> Si a menudo cambia entre empresas o trabaja con [!INCLUDE[prod_short](includes/prod_short.md)] desde dentro de otra aplicación como Microsoft Teams, puede ser fácil perder la noción de dónde se encuentra. Para ayudarle a realizar un seguimiento, puede agregar un distintivo que mostrará el nombre de la empresa, para que pueda verificar rápidamente que está en el lugar correcto. Para obtener más información, consulte [Mostrar un distintivo de compañía](admin-company-information.md#badge).
> 
> Dependiendo de su navegador, también puede anclar las diferentes empresas a su barra de favoritos.  

<!--
[!INCLUDE [about-ui-learn](includes/about-ui-learn.md)]-->

## <a name="features-for-switching-company-or-environment"></a>Características para cambiar de empresa o entorno

Hay algunas funciones que puede usar para cambiar de empresa o entorno mientras trabaja. La siguiente tabla compara las capacidades de la función, que se explican con más detalle en las secciones siguientes.

|Característica|Cambiar de compañía|Cambiar entorno|Cambiar en una nueva pestaña del navegador| Disponible en local|
|-------|--------------|------------------|-------------------------|----------------------|
|[Cambio de empresa](#use-the-company-switcher)|![marca de verificación](media/check.png "comprobar")|![marca de verificación](media/check.png "comprobar")|![marca de verificación](media/check.png "comprobar")|![marca de verificación](media/check.png "comprobar")|
|[Iniciador de aplicaciones](#use-the-app-launcher)||![marca de verificación](media/check.png "comprobar")|![marca de verificación](media/check.png "comprobar")||
|[Mi configuración](#use-my-settings)|![marca de verificación](media/check.png "comprobar")|||![marca de verificación](media/check.png "comprobar")|
|[Hub de empresas](#use-company-hub)|![marca de verificación](media/check.png "comprobar")|![marca de verificación](media/check.png "comprobar")|![marca de verificación](media/check.png "comprobar")||

## <a name="use-the-company-switcher"></a>Usar el cambio de empresa

Usar el cambio de empresa es probablemente la forma más rápida y versátil de cambiar de empresa. El cambio de empresas es un panel que está disponible desde cualquier página. El panel ofrece una descripción general de todas las empresas en todos los entornos a los que tiene acceso y le permite cambiar directamente a cualquiera de ellos.&mdash;ya sea en la misma pestaña del navegador o en una nueva. Es especialmente útil cuando trabaja en muchas empresas en diferentes entornos.

1. En la esquina superior derecha, cerca del icono de búsqueda, verá el icono estándar de la empresa, como ![Icono de lanzador de empresa.](media/ui-experience/company-icon.png "Muestra el icono de cambio de empresa que se utiliza cuando hay un único entorno") y ![company-icon-mult-env](media/ui-experience/company-icon-multi-env.png "Muestra el icono de cambio de empresa que se utiliza cuando hay varios entornos"), o una [insignia personalizada](admin-company-information.md#badge) para la empresa con la que trabaja actualmente. Seleccione el icono para abrir el panel de cambio de empresa.

   :::image type="content" source="media/ui-experience/company-switch-2.png" alt-text="Muestra el icono de cambio de empresa en el encabezado del cliente de Business Central.":::  

   > [!TIP]
   > También puede utilizar el atajo del teclado <kbd>Crtl</kbd>+<kbd>O</kbd> para abrir el panel.
2. En el panel **Empresas disponibles**, seleccione la empresa a la que desea cambiar, seleccione la flecha **Cambiar**, luego elija una de las siguientes opciones:

   |Opción|Descripción|
   |------|-----------|
   |Cambiar|Abre el centro de funciones de la empresa seleccionada en la misma pestaña del navegador en la que está trabajando. La empresa se convierte en la empresa predeterminada que se abre en Business Central, hasta que cambie de nuevo o cambie la empresa utilizando **Mi configuración**. |
   |Abrir en una nueva pestaña|Abre el centro de funciones para la empresa seleccionada en una nueva pestaña del navegador, manteniendo abierta la empresa original en la otra pestaña.|
   |Abrir en una nueva pestaña e ir a la misma página|Esta opción solo está activa en páginas de lista, como clientes, pedidos de venta o artículos. Abre la misma lista, pero para la empresa seleccionada, en una nueva pestaña del navegador. |

> [!TIP]
> Seleccione <kbd>F5</kbd> para actualizar la lista de entornos y empresas.

## <a name="use-the-app-launcher"></a>Usar el iniciador de aplicaciones

Cuando inicia sesión en [!INCLUDE[prod_short](includes/prod_short.md)], los ambientes a los que puede acceder están disponibles en Office.com.  

1. Seleccione el icono del **Iniciador de aplicaciones** ![Iniciador de aplicaciones.](media/app-launcher-icon.png "El lanzador de aplicaciones proporciona acceso a más funciones").
2. En el panel que se abre, busque y elija [!INCLUDE[prod_short](includes/prod_short.md)]. Si no ve [!INCLUDE[prod_short](includes/prod_short.md)], elija **Todas las aplicaciones**, después introduzca **Business Central** en la ventana de texto **Buscar**.

   :::image type="content" source="media/app-launcher-bc-tile.png" alt-text="El iniciador de aplicaciones de Microsoft 365 muestra el mosaico de Business Central.":::  

3. Si hay más de un entorno, se le pedirá que elija el entorno al que acceder.

<!--
The following image shows tiles for accessing production and sandbox environments on the Dynamics 365 Home page.

:::image type="content" source="media/app-picker-environments.png" alt-text="The Dynamics 365 Home page showing production and sandbox environments.":::
-->
## <a name="use-my-settings"></a>Usar Mi configuración

Cuando ha iniciado sesión en [!INCLUDE[prod_short](includes/prod_short.md)], puede cambiar rápidamente a otra empresa en el mismo entorno. Después de hacer el cambio, la empresa que elija se convierte en su empresa predeterminada y se abrirá la próxima vez que inicie sesión.

1. En la esquina superior derecha, elija el icono **Configuración** ![Configuración.](media/ui-experience/settings_icon_small.png "Icono de configuración para el área de trabajo") y, a continuación, elija la acción **Mi configuración**.

    > [!TIP]
    > También puede utilizar el atajo <kbd>Alt</kbd>+<kbd>T</kbd> para abrir rápidamente la página Mi configuración.

2. En la página **Mi configuración**, en el campo **Empresa**, seleccione la empresa.  
3. Elija el botón **Aceptar**.

> [!TIP]
> Una buena manera de ir directamente a su empresa predeterminada cuando inicia sesión y evitar tener que especificar un entorno, es agregar la URL a su lista de favoritos después de iniciar sesión.

## <a name="use-company-hub"></a>Usar Hub de empresa

*Hub de empresa* es un centro de funciones altamente especializado que ofrece una visión general financiera de todas las empresas y entornos. Disponible como una [extensión](ui-extensions-company-hub.md), el Hub de empresa proporciona un panel con datos resumidos para cada empresa a la que tiene acceso. La página de inicio muestra los KPI financieros, así como un vínculo directo a los entornos individuales y las empresas. Para más información, consulte [Administrar el trabajo de varias empresas en el hub de empresas](company-hub.md).

[![Muestra la página central de la empresa que enumera todas las empresas.](media/company-hub.png)](media/company-hub.png#lightbox)  

## <a name="see-also"></a>Consulte también .

[Crear nuevas en empresas en [!INCLUDE[prod_short](includes/prod_short.md)]](about-new-company.md)  
[Cambiar la configuración básica](ui-change-basic-settings.md)  
[Entornos y empresas (inglés solo)](/dynamics365/business-central/dev-itpro/administration/tenant-environment-topology)  
[Información de empresa](admin-company-information.md)  
[El centro de administración de Business Central](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
