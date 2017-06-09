---
title: Usar Dynamics 365 for Financials como origen de datos de Power BI | Documentos de Microsoft
description: "Puede hacer que los datos de Financials estén disponibles como origen de datos en Power BI y generar informes eficaces del estado de la empresa."
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: business intelligence, KPI, Odata, Power App, SOAP, analysis
ms.date: 12/02/2016
ms.author: edupont
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 5213b515dfdf1f0e538a6d003cf921781ca6b3ff
ms.contentlocale: es-es
ms.lasthandoff: 05/04/2017


---
# <a name="using-dynamics-365-for-financials-as-a-power-bi-data-source"></a>Usar Dynamics 365 for Financials como origen de datos de Power BI
Puede hacer que los datos de [!INCLUDE[d365fin](includes/d365fin_md.md)] estén disponibles como origen de datos en Power BI y generar informes eficaces del estado de la empresa.  

**Nota**: Debe disponer de una cuenta válida con [!INCLUDE[d365fin](includes/d365fin_md.md)] y con Power BI. Además, deberá descargar [Power BI Desktop](https://powerbi.microsoft.com/en-us/desktop/).  

## <a name="to-add-included365finincludesd365finmdmd-as-a-data-source-in-power-bi-desktop"></a>Para agregar [!INCLUDE[d365fin](includes/d365fin_md.md)] como origen de datos de Power BI Desktop
1. En Power BI Desktop, en el panel de navegador izquierdo, elija **Obtener datos**.
2. En la ventana **Obtener datos**, **Servicios en línea**, elija **Dynamics 365 for Financials** y después seleccione el botón **Conectar**.

   Power BI muestra un asistente que le guiará por el proceso de conexión. El primer paso será especificar una dirección URL de OData y el nombre de la empresa que está asociada a la cuenta de [!INCLUDE[d365fin](includes/d365fin_md.md)].  

   Para *URL de OData*, puede copiar la dirección URL de OData V4 de cualquiera de los servicios web que se muestran en la página **Servicios Web** en [!INCLUDE[d365fin](includes/d365fin_md.md)], por ejemplo, `https://mycompany.financials.dynamics.com:7048/MS/ODataV4/`.  

   Para *Nombre empresa*, utilice el nombre que se muestra en el campo **Nombre** de la ventana **Información empresa** en [!INCLUDE[d365fin](includes/d365fin_md.md)]. Si [!INCLUDE[d365fin](includes/d365fin_md.md)] contiene varias empresas, elija el nombre de la empresa pertinente en la lista en la ventana **Empresas**. En ambos casos, asegúrese de que el nombre que especifique en el asistente Power BI coincide exactamente con el texto que se muestra en [!INCLUDE[d365fin](includes/d365fin_md.md)], como `My Company`.
3. Una vez introducidos los datos, elija el botón Aceptar. El siguiente paso en el asistente es introducir su nombre de usuario y contraseña.

   **Nota**: Si hay otras opciones de autenticación disponibles en el panel de navegación izquierdo, elija *Básico*.
4. Introduzca su nombre de usuario y contraseña. Puede encontrar esta información en la ventana **Usuarios** en [!INCLUDE[d365fin](includes/d365fin_md.md)]. Utilice la **Clave de acceso web** como la contraseña.

   Por ejemplo, su nombre de usuario es *ADMIN* y la clave de acceso al servicio Web que actúa de contraseña es *EgzeUFQ9Uv0o5O0lUMyqCzo1ueUW9yRF3SsLU=*.
5. Elija el botón **Conexión** para continuar. El asistente Power BI muestra una lista de los orígenes de datos de [!INCLUDE[d365fin](includes/d365fin_md.md)]. Este origen de datos todos los servicios web que haya publicado desde [!INCLUDE[d365fin](includes/d365fin_md.md)].

   Si lo desea, puede crear una nueva dirección URL de servicio Web en [!INCLUDE[d365fin](includes/d365fin_md.md)] mediante la acción **Crear conjunto de datos** en la página **Servicios web**, utilizando la guía de configuración asistida **Configurar informes** o eligiendo la acción **Editar en Excel** en cualquier lista.
6. Especifique los datos que desea agregar al modelo de datos y después seleccione el botón **Cargar**.
7. Repita los pasos anteriores agregar datos de [!INCLUDE[d365fin](includes/d365fin_md.md)] adicionales a su modelo de datos de Power BI.

   **Nota**: Una vez que haya conectado correctamente con [!INCLUDE[d365fin](includes/d365fin_md.md)], no se le solicitará nuevamente la URL, el nombre de usuario o la contraseña de OData.

Una vez que los datos se hayan cargado, aparecerán en el panel de navegación derecho en la página. Ya se ha conectado correctamente con los datos de Dynamics 365 y está preparado para comenzar a crear su informe de Power BI. Para obtener más información, consulte la [documentación de Power BI](https://powerbi.microsoft.com/documentation/powerbi-landing-page/).

## <a name="see-also"></a>Consulte también
[[!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)  
[Importar datos de empresa de otros sistemas financieros](upload-data.md)  
[Configurar [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)  
[Finanzas](finance.md)  

