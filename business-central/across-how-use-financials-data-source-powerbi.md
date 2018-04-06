---
title: "Informes de configuración para Business Central en Power BI | Documentos de Microsoft"
description: "Puede hacer que los datos de Financials estén disponibles como origen de datos en Power BI y generar informes eficaces del estado de la empresa."
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: business intelligence, KPI, Odata, Power App, SOAP, analysis
ms.date: 12/21/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 42939e97d121bd3a2abff91671d9f9571faffbfd
ms.contentlocale: es-es
ms.lasthandoff: 03/22/2018

---
# <a name="using-included365finincludesd365finmdmd-as-power-bi-data-source-for-building-reports"></a>Usar [!INCLUDE[d365fin](includes/d365fin_md.md)] como fuente de datos de Power BI para generar informes
Puede hacer que los datos de [!INCLUDE[d365fin](includes/d365fin_md.md)] estén disponibles como origen de datos en Power BI y generar informes eficaces del estado de la empresa.  

> [!NOTE]  
> Debe disponer de una cuenta válida con [!INCLUDE[d365fin](includes/d365fin_md.md)] y con Power BI. Además, deberá descargar [Power BI Desktop](https://powerbi.microsoft.com/en-us/desktop/).  

## <a name="to-add-included365finincludesd365finmdmd-as-a-data-source-in-power-bi-desktop"></a>Para agregar [!INCLUDE[d365fin](includes/d365fin_md.md)] como origen de datos de Power BI Desktop
1. En Power BI Desktop, en el panel de navegador izquierdo, elija **Obtener datos**.
2. En la ventana **Obtener datos**, **Servicios en línea**, elija **Dynamics 365 Business Central** y después seleccione el botón **Conectar**.
3. Power BI muestra un asistente que le guiará por el [proceso de conexión](across-how-to-connect-powerbi-dynamics-365-content-packs-help.md). El primer paso es iniciar sesión en el servicio. Seleccione **Iniciar sesión** y elija la cuenta con la que desea iniciar sesión. Debe ser la misma cuenta con la que inicia sesión en [!INCLUDE[d365fin](includes/d365fin_md.md)].
4. Elija el botón **Conectar** para continuar. El asistente Power BI muestra una lista de las empresas y los orígenes de datos de [!INCLUDE[d365fin](includes/d365fin_md.md)]. Este origen de datos todos los servicios web que haya publicado desde cada empresa en [!INCLUDE[d365fin](includes/d365fin_md.md)].
5. Si lo desea, puede crear una nueva dirección URL de servicio Web en [!INCLUDE[d365fin](includes/d365fin_md.md)] mediante la acción **Crear conjunto de datos** en la página **Servicios web**, utilizando la guía de configuración asistida **Configurar informes** o eligiendo la acción **Editar en Excel** en cualquier lista.
6. Especifique los datos que desea agregar al modelo de datos y después seleccione el botón **Cargar**.
7. Repita los pasos anteriores agregar datos de [!INCLUDE[d365fin](includes/d365fin_md.md)] adicionales a su modelo de datos de Power BI.

> [!NOTE]  
> Una vez que se haya conectado correctamente a [!INCLUDE[d365fin](includes/d365fin_md.md)], no se le volverá a solicitar que inicie sesión.

Una vez que los datos se hayan cargado, aparecerán en el panel de navegación derecho en la página. Ya se ha conectado correctamente con los datos de Business Central y está preparado para comenzar a crear su informe de Power BI. Para obtener más información, consulte la [documentación de Power BI](https://powerbi.microsoft.com/documentation/powerbi-landing-page/).

## <a name="see-also"></a>Consulte también
[Inteligencia empresarial](bi.md)  
[[!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)  
[Importar datos de empresa de otros sistemas financieros](upload-data.md)  
[Configurar [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)   
[Finanzas](finance.md)  
[Conectar Power BI a [!INCLUDE[d365fin](includes/d365fin_md.md)]](across-how-to-connect-powerbi-dynamics-365-content-packs-help.md)  

