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
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: b42437f0759ecb6d977797b31222bfa2b88cdb13
ms.sourcegitcommit: 3e9c89f90db5eaed599630299353300621fe4007
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 07/01/2020
ms.locfileid: "3528467"
---
# <a name="using-prodlong-as-power-bi-data-source-for-building-reports"></a>Usar [!INCLUDE[prodlong](includes/prodlong.md)] como fuente de datos de Power BI para generar informes

Puede hacer que los datos de [!INCLUDE[prodlong](includes/prodlong.md)] estén disponibles como origen de datos en Power BI y generar informes eficaces del estado de la empresa.  

Debe disponer de una cuenta válida con [!INCLUDE[prodshort](includes/prodshort.md)] y con Power BI. Debe descargar también [Power BI Desktop](https://powerbi.microsoft.com/desktop/). Para obtener más información, consulte [Inicio rápido: Conectarse a los datos de Power BI Desktop](/power-bi/desktop-quickstart-connect-to-data).  

## <a name="to-add-prodshort-as-a-data-source-in-power-bi-desktop"></a>Para agregar [!INCLUDE[prodshort](includes/prodshort.md)] como origen de datos de Power BI Desktop

1. En Power BI Desktop, en el panel de navegador izquierdo, elija **Obtener datos**.
2. En la página **Obtener datos**, **Servicios en línea**, elija **Microsoft Dynamics 365 Business Central** y después seleccione el botón **Conectar**.
3. Power BI muestra un asistente que le guiará por el proceso de conexión, incluido el inicio de sesión en [!INCLUDE[prodshort](includes/prodshort.md)]. Elija **Iniciar sesión** y luego elija la cuenta pertinente. Use la misma cuenta con la que inicia sesión en [!INCLUDE[prodshort](includes/prodshort.md)].
4. Elija el botón **Conectar** para continuar. El asistente de Power BI muestra una lista de los entornos, las empresas y los orígenes de datos de Microsoft [!INCLUDE[d365fin](includes/d365fin_md.md)]. Estos orígenes de datos todos los servicios web que haya publicado desde [!INCLUDE[prodshort](includes/prodshort.md)].

    También puede crear una nueva URL de servicio web en [!INCLUDE[prodshort](includes/prodshort.md)] en su lugar. Elija uno de los siguientes métodos:

      - Utilizar la acción **Crear conjunto de datos** en la página **Servicios web**
      - Utilizar la guía de configuración asistida **Configurar informes**
      - Elegir la acción **Editar en Excel** en cualquier lista

5. Especifique los datos que desea agregar al modelo de datos y después seleccione el botón **Cargar**.
6. Repita los pasos anteriores agregar datos de [!INCLUDE[prodshort](includes/prodshort.md)] adicionales, u otros datos, a su modelo de datos de Power BI.

> [!NOTE]  
> Una vez que se haya conectado correctamente a [!INCLUDE[prodshort](includes/prodshort.md)], no se le volverá a solicitar que inicie sesión.

Una vez que los datos se hayan cargado, puede verlos en el panel de navegación derecho en la página. Se ha conectado correctamente con los datos de [!INCLUDE[prodshort](includes/prodshort.md)] y puede comenzar a crear su informe de Power BI.  

Antes de elaborar el informe, le recomendamos que importe el archivo de tema de [!INCLUDE[prodshort](includes/prodshort.md)].  El archivo de tema creará una paleta de colores de forma que pueda crear informes con el mismo estilo de color que las aplicaciones de [!INCLUDE[prodshort](includes/prodshort.md)] sin pedirle que defina colores personalizados para cada elemento visual.

Para obtener más información, consulte la [documentación de Power BI](/power-bi/consumer/).

## <a name="see-related-training-at-microsoft-learn"></a>Consulte Formación relacionada en [Microsoft Learn](/learn/modules/configure-powerbi-excel-dynamics-365-business-central/index)

## <a name="see-also"></a>Consulte también

[Habilitar los datos de negocio para Power BI](admin-powerbi.md)  
[Inteligencia empresarial](bi.md)  
[Introducción](product-get-started.md)  
[Importar datos de empresa de otros sistemas financieros](across-import-data-configuration-packages.md)  
[Configurar [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)  
[Finanzas](finance.md)  
[Inicio rápido: Conectarse a los datos de Power BI Desktop](/power-bi/desktop-quickstart-connect-to-data)  
