---
title: Usar Business Central en los informes de Power BI | Microsoft Docs
description: Haga que los datos estén disponibles como origen de datos en Power BI y generar informes eficaces del estado de la empresa.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: business intelligence, KPI, Odata, Power App, SOAP, analysis
ms.date: 10/01/2019
ms.author: edupont
ms.openlocfilehash: b57b87dd8cdc9390ed5b1b7136107639f689c192
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/01/2019
ms.locfileid: "2305001"
---
# <a name="using-include-prodlongincludesprodlongmd-as-power-bi-data-source-for-building-reports"></a>Usar [!INCLUDE [prodlong](includes/prodlong.md)] como fuente de datos de Power BI para generar informes

Puede hacer que los datos de [!INCLUDE[prodlong](includes/prodlong.md)] estén disponibles como origen de datos en Power BI y generar informes eficaces del estado de la empresa.  

Debe disponer de una cuenta válida con [!INCLUDE[prodshort](includes/prodshort.md)] y con Power BI. Además, deberá descargar [Power BI Desktop](https://powerbi.microsoft.com/en-us/desktop/). Para obtener más información, consulte [Inicio rápido: Conectarse a los datos de Power BI Desktop](/power-bi/desktop-quickstart-connect-to-data).  

## <a name="to-add-includeprodshortincludesprodshortmd-as-a-data-source-in-power-bi-desktop"></a>Para agregar [!INCLUDE[prodshort](includes/prodshort.md)] como origen de datos de Power BI Desktop

1. En Power BI Desktop, en el panel de navegador izquierdo, elija **Obtener datos**.
2. En la página **Obtener datos**, **Servicios en línea**, elija **Microsoft Dynamics 365 Business Central** y después seleccione el botón **Conectar**.
3. Power BI muestra un asistente que le guiará por el proceso de conexión. Se le pedirá que inicie sesión en [!INCLUDE [prodshort](includes/prodshort.md)]. Seleccione **Iniciar sesión** y elija la cuenta con la que desea iniciar sesión. Debe ser la misma cuenta con la que inicia sesión en [!INCLUDE [prodshort](includes/prodshort.md)].
4. Elija el botón **Conectar** para continuar. El asistente de Power BI muestra una lista de los ambientes, las empresas y los orígenes de datos de Microsoft [!INCLUDE[d365fin](includes/d365fin_md.md)]. Este origen de datos todos los servicios web que haya publicado desde cada suscriptor/empresa en [!INCLUDE [prodshort](includes/prodshort.md)].
5. Si lo desea, puede crear una nueva dirección URL de servicio Web en [!INCLUDE [prodshort](includes/prodshort.md)] mediante la acción **Crear conjunto de datos** en la página **Servicios web**, utilizando la guía de configuración asistida **Configurar informes** o eligiendo la acción **Editar en Excel** en cualquier lista.
6. Especifique los datos que desea agregar al modelo de datos y después seleccione el botón **Cargar**.
7. Repita los pasos anteriores agregar datos de [!INCLUDE [prodshort](includes/prodshort.md)] adicionales, u otros datos, a su modelo de datos de Power BI.

> [!NOTE]  
> Una vez que se haya conectado correctamente a [!INCLUDE [prodshort](includes/prodshort.md)], no se le volverá a solicitar que inicie sesión.

Una vez que los datos se hayan cargado, aparecerán en el panel de navegación derecho en la página. Ya se ha conectado correctamente con los datos de [!INCLUDE [prodshort](includes/prodshort.md)] y está preparado para comenzar a crear su informe de Power BI.  

Antes de elaborar el informe, le recomendamos que importe el archivo de tema de [!INCLUDE [prodshort](includes/prodshort.md)].  El archivo de tema creará una paleta de colores de forma que pueda crear informes con el mismo estilo de color que las aplicaciones de [!INCLUDE [prodshort](includes/prodshort.md)] sin pedirle que defina colores personalizados para cada elemento visual.

Para obtener más información, consulte la [documentación de Power BI](/power-bi/consumer/power-bi-consumer-landing/).

## <a name="see-also"></a>Consulte también

[Habilitar los datos de negocio para Power BI](admin-powerbi.md)  
[Inteligencia empresarial](bi.md)  
[Introducción](product-get-started.md)  
[Importar datos de empresa de otros sistemas financieros](across-import-data-configuration-packages.md)  
[Configurar [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)  
[Finanzas](finance.md)  
[Inicio rápido: Conectarse a los datos de Power BI Desktop](/power-bi/desktop-quickstart-connect-to-data)  
