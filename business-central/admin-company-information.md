---
title: Resumen de la información de la empresa
description: 'La página Información empresa especifica la información básica de una entidad comerciales, como el nombre, las direcciones y la información de envío.'
author: jswymer
ms.topic: conceptual
ms.search.form: 1
ms.date: 09/24/2023
ms.author: jswymer
ms.reviewer: jswymer
ms.service: dynamics-365-business-central
ms.custom: bap-template
---

# <a name="company-information-overview"></a>Resumen de la información de la empresa

[!INCLUDE[prod_short](includes/prod_short.md)] organiza entidades comerciales en *empresas*. Para cada empresa, debe completar algunos de los detalles básicos de la empresa y la información pertinente en la página **Información de la empresa**. La información de la página [**Información empresa**](https://businesscentral.dynamics.com/?page=1) se utiliza en documentos, como las cabeceras de factura. Se puede configurar más de una empresa, por ejemplo, una empresa matriz y una subsidiaria.  

Si el almacén de existencias de la empresa se encuentra ubicado en una dirección distinta a la oficina central de la empresa, puede completar los diversos campos de la dirección de envío y el campo **Cód. almacén** en la ficha desplegable **Envío**. La información contenida en estos campos se imprime luego en los pedidos de compra, por ejemplo, para que los proveedores envíen los productos al lugar correcto.  

Para cada empresa que configure, debe completar la página **Información empresa**, junto con la página **Configuración de contabilidad**. También debe configurar cada área en [!INCLUDE [prod_short](includes/prod_short.md)], como la página **Configuración de ventas y cobros**, para cada empresa. Más información en [Resumen de tareas para configurar [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md).  

La página **Información empresa** contiene diferentes campos y fichas desplegables, según su país o región. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)] En la siguiente tabla se describen las fichas desplegables más comunes.

[!INCLUDE [admin-company-info-fasttabs](includes/admin-company-info-fasttabs.md)]

Una vez que haya terminado de rellenar la información, puede cerrar la página.  

## <a name="working-with-multiple-companies"></a>Trabajar con varias empresas

Si su [!INCLUDE [prod_short](includes/prod_short.md)] incluye varias empresas, es posible que sus usuarios deseen utilizar *insignias de la empresa* para ayudarles a identificar rápidamente y realizar un seguimiento de la empresa en la que están trabajando actualmente. Para obtener más información, consulte [Mostrar un distintivo de compañía](#badge).

Hay algunas funciones que puede usar para cambiar entre empresas mientras trabaja, como el cambiador de empresas (<kbd>Ctrl</kbd>+<kbd>O</kbd>). Más información en [Cambiar a otra empresa o entorno](ui-organization-switch.md).

## <a name="display-a-company-badge"></a><a name="badge"></a>Mostrar una insignia de la empresa

Cuando hay más de una empresa o entorno, verá el selector de empresas en la parte superior derecha de la barra de la aplicación, cerca del icono de búsqueda en la barra de la aplicación. De forma predeterminada, el conmutador de empresa utiliza un icono de empresa estándar, como ![Lanzador de iconos de empresa.](media/ui-experience/company-icon.png "Muestra el icono de cambio de empresa que se utiliza cuando hay un único entorno") y ![company-icon-mult-env](media/ui-experience/company-icon-multi-env.png "Muestra el icono de cambio de empresa que se utiliza cuando hay varios entornos").

:::image type="content" source="media/ui-experience/company-switch-2.png" alt-text="Muestra el icono de cambio de empresa en el encabezado del cliente de Business Central.":::  

A partir del segundo lanzamiento de versiones de 2023, versión 23, la insignia de la empresa aparece en la pestaña del navegador cuando se utiliza el cliente web. También se incluye en los enlaces de páginas que puede [copiar y pegar](across-share-data-features.md#copying-a-link) en editores de texto enriquecido, como Word, Outlook y Teams.
 
### <a name="set-the-company-badge"></a>Establecer la insignia de empresa

En la página **Información de la empresa**, puede reemplazar el icono estándar de la empresa con una insignia personalizada por empresa si la insignia de la empresa facilita a los usuarios la identificación de la empresa en la que están trabajando.

1. En la ficha desplegable **Distintivo de la empresa**, rellene los campos según sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
2. Cuando haya terminado, actualice el navegador (seleccione <kbd>Ctrl</kbd>+<kbd>F5</kbd>) para actualizar la insignia en el cliente.  

> [!NOTE]
> El selector de empresas se introdujo en el lanzamiento de versiones 2 de 2022, versión 21. En versiones anteriores, la insignia de empresa no se utiliza para cambiar de empresa. Se muestra en la esquina superior derecha de la mayoría de las páginas, incluso cuando solo hay una empresa. Al seleccionarlo, se mostrará el nombre completo de la empresa y el nombre del entorno.

## <a name="change-company-display-name"></a>Cambiar el nombre para mostrar de la empresa

El nombre de la empresa siempre se muestra en la esquina superior izquierda y funciona como una acción que puede elegir para volver al área de trabajo. Puede cambiar este nombre en la página **Información de empresa**.

1. Elija el ![icono de rueda dentada para abrir el menú Configuración.](media/ui-experience/settings_icon_small.png) , y luego elija la acción **Información empresa**.
2. En el campo **Nombre**, introduzca el nuevo nombre de empresa.
3. Salga de la página. El sistema se reinicia y muestra la nueva empresa en la esquina superior izquierda.

## <a name="experience"></a>Experiencia

La experiencia de usuario predeterminada en una prueba de [!INCLUDE [prod_short](includes/prod_short.md)] no revela todas las capacidades. Puede activar la experiencia completa en la página **Información de la empresa**.  

Para obtener más información, vaya a [Cambiar las funciones que se muestran](ui-experiences.md).  

## <a name="see-also"></a>Consulte también

[Resumen de tareas para configurar [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md)  
[Inicio rápido Información empresa](quick-start-company-information.md)  
[Configurar la información de la empresa en Italia](LocalFunctionality/Italy/how-to-set-up-company-information.md)  
[Cambiar la configuración básica](ui-change-basic-settings.md)  
[Cambiar las funciones que se muestran](ui-experiences.md)  
[Crear nuevas en empresas](about-new-company.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
