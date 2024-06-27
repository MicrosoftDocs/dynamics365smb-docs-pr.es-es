---
title: Trabajar con Business Central
description: Describe cómo interactuar con datos en Business Central.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.form: 'RoleExplorer, 9020, 9022, 9026, 9027, 9030, 9000, 9009, 9004, 9005, 9024, 9006, 9007, 9010, 9016, 9017'
ms.date: 09/19/2023
ms.custom: bap-template
ms.service: dynamics-365-business-central
---
# Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]

Mientras trabaja en [!INCLUDE [prod_short](includes/prod_short.md)], interactúa con los datos de diferentes maneras. Por ejemplo, crea registros, ingresa datos, ordena y filtra datos, escribe notas y exporta datos a otras aplicaciones.

Hay muchas formas de personalizar la apariencia de las páginas: 

* Ajustar el tamaño y la posición de cualquier página
* Ampliar el ancho de las columnas y aumentar la altura de los encabezados de las columnas
* Cambiar la forma en que ordena los datos en columnas. 

Si quiere usar la barra de desplazamiento horizontal para ver todas las columnas en una página de lista o en líneas de documentos, hay una inmovilización del panel vertical para impedir el desplazamiento de algunas columnas.

[!INCLUDE [about-ui-learn](includes/about-ui-learn.md)]

## <a name="cheatsheet"></a>Sugerencias y trucos

> [!TIP]
> Para obtener un resumen en versión para imprimir de las funciones más usadas, elija la siguiente imagen y descargue el archivo PDF.
>
> [ ![Icono para el archivo PDF.](media/cheat_sheet_inline.png) ](media/cheat_sheet.pdf "Icono que abre un PDF")

## Vínculos para obtener más información

En la tabla siguiente se indican algunas de las funciones generales y vínculos a los artículos en que se describen.

> [!NOTE]
> Además de las funciones generales descritas en esta sección, puede usar otras funciones que estén más relacionadas con el negocio. Para obtener más información, vaya a [Funciones empresariales generales](ui-across-business-areas.md).

| Para  | Ir a |
| --- | --- |
|Encuentre una página, informe, acción, artículo de ayuda o extensión de socio específica. |[Búsqueda de páginas e información con Dígame](ui-search.md) |
|Obtenga una descripción general de las páginas para su rol y para otros roles y vaya a las páginas.|[Búsqueda de páginas con el explorador de roles](ui-role-explorer.md)|
|Filtrar los datos de vistas, informes, o funciones con los símbolos y caracteres especiales. |[Ordenar, buscar y filtrar listas](ui-enter-criteria-filters.md) |
|Obtenga información sobre varias funciones generales que le pueden ayudar a introducir datos de manera rápida y fácil.|[Introducción de fechas](ui-enter-data.md)|
|Obtenga información sobre cómo copiar y pegar datos rápidamente y usar atajos de teclado.|[Preguntas frecuentes sobre copiar y pegar](faq-copy-paste.yml)|
|Acceder o procesar los datos en rangos de fecha específicos. |[Trabajar con fechas y horas del calendario](ui-enter-date-ranges.md) |
|Identificar los campos que debe rellenar. |[Detección de campos obligatorios](ui-mandatory-fields.md) |
|Comprender los efectos de la configuración local. Aprenda cómo cambiar la configuración local y de idioma.|[Cambiar idioma y región](about-locale-language.md)|
|Obtenga información sobre cómo interactuar con Excel desde prácticamente cualquier lugar en [!INCLUDE[prod_short](includes/prod_short.md)]|[Ver y editar en Excel](across-work-with-excel.md)|
|Adjunte archivos, agregue vínculos o escriba notas en fichas y documentos.|[Administrar archivos adjuntos, vínculos y notas en fichas y documentos](ui-how-add-link-to-record.md)|
|Cambiar la configuración básica como la fecha de trabajo o de la empresa y el área de trabajo. |[Cambiar la configuración básica](ui-change-basic-settings.md) |
|Reciba notificaciones sobre ciertos eventos o cambios de estado. Por ejemplo, cuando está a punto de facturar a un cliente que tiene una deuda vencida.|[Administrar notificaciones](ui-smart-notifications.md)|
|Cambie qué acciones y campos están disponibles y dónde se muestran para que se ajusten a sus preferencias.|[Personalizar su área de trabajo](ui-personalization-user.md) |
|Definir, previsualizar, imprimir o guardar los informes y configurar y ejecutar los procesos.|[Trabajar con informes, trabajos por lotes y XMLports](ui-work-report.md)|
|Gestionar el contenido y formato de informes y documentos. Especifique los datos del campo que se incluirán y cómo aparecen. Por ejemplo, elija un estilo de texto, agregue imágenes y más.|[Administrar diseños de informes y documentos](ui-manage-report-layouts.md) |
|Conocer las funciones que hacen que [!INCLUDE[prod_short](includes/prod_short.md)] sea accesible a personas con discapacidades.|[Accesibilidad y métodos abreviados de teclado](ui-accessibility.md)|

## Desplazarse por Business Central

A continuación se muestra un vídeo corto acerca de cómo desplazarse en [!INCLUDE[prod_short](includes/prod_short.md)].

> [!VIDEO https://www.youtube.com/embed/zqz03iMihx0]

## Elegir un navegador de escritorio

[!INCLUDE[prod_short](includes/prod_short.md)] admite múltiples navegadores y cada navegador ofrece varias funciones. El navegador juega un papel importante en la capacidad de respuesta y la fluidez de la interfaz de usuario. Consulte la lista de navegadores compatibles y recomendados para [Business Central Online](./product-requirements.md) y navegadores para [Business Central On-premises](/dynamics365/business-central/dev-itpro/deployment/system-requirement-business-central-v15).

- Siempre que sea posible, evite navegadores antiguos como Internet Explorer. En su lugar, cambie a uno de nuestros navegadores modernos recomendados, como el [nuevo Microsoft Edge](https://www.microsoft.com/edge/).  

    > [!NOTE]
    > Internet Explorer ya no es compatible. Para obtener más información, vaya a la [documentación de Microsoft Edge](https://support.microsoft.com/hub/4337664/microsoft-edge-help).
- Mantenga su navegador actualizado a la última versión.

## Barras de acción

En [!INCLUDE [prod_short](includes/prod_short.md)], usted realiza la mayor parte de su trabajo en una lista, un documento o una tarjeta. Todas las páginas tienen una barra con acciones que son relevantes para ellas. Las acciones son casi las mismas para la tarjeta o documento individual y la lista de entidades. De esta forma, puede gestionar un pedido de cliente individual en la página **Órdenes de venta** y en la **Órdenes de venta**, incluidos su registro y facturación.  

La forma en que abre una página y el contexto de lo que está haciendo afectan la disponibilidad de acciones. Las acciones pueden aparecer de forma diferente, no estar disponibles o incluso no estar presentes. No todas las acciones son relevantes o respaldadas para todos los procesos. Además, algunas acciones requieren que haga una selección. Si una acción no es relevante o no es compatible, la hacemos no disponible. Hacemos esto para ayudar a aclarar lo que puede hacer con sus selecciones.

Específicamente para las páginas de lista, la página de lista que abre desde la página de inicio y la página que se abre cuando usa la ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") Icono para buscarlo no son idénticos.  

Cuando busca una página de lista abierta, como la lista **Órdenes de venta**, está en modo de visualización. Las acciones para editar, ver o eliminar una entidad individual, como una orden de venta, se muestran cuando elige la acción **Administrar**.  

> [!TIP]
> Si sabe que utilizará acciones en este segundo nivel de la barra de acciones con frecuencia, elija el icono :::image type="icon" source="media/pin.png" border="false"::: para anclar la barra de acciones y hacer que las acciones de los distintos menús sean inmediatamente visibles.
>
> Para ocultar el segundo nivel de la barra de acción nuevamente, elija el icono :::image type="icon" source="media/unpin.png" border="false":::.

Cuando abre la misma página de lista desde su página de inicio, la acción **Administrar** no está disponible. En su lugar, para abrir un pedido de cliente individual, elija el campo **Número**. En esta vista, no puede anclar la barra de acción.  

## Consulte también

[Preparación para hacer negocios](ui-get-ready-business.md)  
[Configuración de Business Central](setup.md)  
[Funciones empresariales generales](ui-across-business-areas.md)  
[Consejos de rendimiento para usuarios comerciales](/dynamics365/business-central/dev-itpro/performance/performance-users?toc=/dynamics365/business-central/toc.json)

## [!INCLUDE[prod_short](includes/free_trial_md.md)]

[!INCLUDE[footer-include](includes/footer-banner.md)]
