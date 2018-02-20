---
title: "Cómo conectar Power BI con Finance and Operations, Business edition | Documentos de Microsoft"
description: "Obtener información, inteligencia empresarial, y KPI de sus datos de Finance and Operations, Business edition es fácil con Power BI y los paquetes de contenido de Finance and Operations, Business edition."
author: SusanneWindfeldPedersen
ms.service: dynamics365-financials
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: account schedule, analysis, reporting, financial report, business intelligence, KPI
ms.date: 01/29/2018
ms.author: solsen
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 4a1498e634046e54bdb9a5793731e44808c2f1eb
ms.contentlocale: es-es
ms.lasthandoff: 01/30/2018

---
# <a name="connecting-power-bi-to-finance-and-operations-business-edition-content-packs"></a>Conectar Power BI con los paquetes de contenido de Finance and Operations, Business edition
Obtener información de los datos de Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] resulta muy sencillo con los paquetes de contenido de Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]. Power BI extrae los datos, genera un panel original y envía informes en función de los datos.

> [!NOTE]  
>  Debe disponer de una cuenta válida con Dynamics 365 y con Power BI. Además, deberá descargar [Power BI Desktop](https://powerbi.microsoft.com/en-us/desktop/).  
>  Los paquetes de contenido de Power BI requieren permisos para las tablas desde donde se recuperan los datos. A continuación se describen más detalles sobre los requisitos.  

## <a name="how-to-connect"></a>Cómo conectarse
1. Seleccione **Obtener datos** en la parte inferior del panel de navegación izquierdo.  
![Navegar para obtener datos](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-get-data.png)
2. En el cuadro **Servicios**, seleccione **Obtener**. Se abrirá una ventana con **AppSource** y **aplicaciones para aplicaciones de Power BI**.  
![Seleccionar paquetes de contenidos de servicios en línea](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-online-services-get.png)
3. Seleccione **Aplicaciones** de la pestaña **Aplicaciones para aplicaciones de Power BI** y elija el paquete de contenidos **Microsoft Dynamics 365 for Finance and Operations** que quiera usar, a continuación, seleccione **Obtener ahora**.  
![Seleccione Dynamics 365 for Finance and Operations, Business edition y elija Obtener ahora](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-dynamics365-for-financials-get-it-now.png)
4. Cuando se lo solicite, escriba el nombre de *su empresa* en [!INCLUDE[d365fin_md](includes/d365fin_long_md.md)]. Este no es el nombre para mostrar.  
![Seleccione Dynamics 365 for Finance and Operations, Business edition y elija Obtener ahora](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-connect-to-d365-finance-and-operations-crm.png)
5. Una vez conectado se cargarán automáticamente un panel, un informe y un conjunto de datos en su espacio de trabajo de Power BI. Cuando se haya completado, se actualizarán los mosaicos con datos de la cuenta.
![Seleccione Dynamics 365 for Finance and Operations, Business edition y elija Obtener ahora](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-workspace-dashboard-report-dataset.png)

## <a name="what-now"></a>¿Y ahora qué?

- Intente [hacer una pregunta en el cuadro de preguntas](https://docs.microsoft.com/en-us/power-bi/service-q-and-a) en la parte superior del escritorio.  
- [Cambie los mosaicos](https://docs.microsoft.com/en-us/power-bi/service-dashboard-edit-tile) en el escritorio.  
- [Seleccione un mosaico](https://docs.microsoft.com/en-us/power-bi/service-dashboard-tiles) para abrir el informe subyacente.  
- Mientras que su conjunto de datos se programa para actualizarse diariamente, puede cambiar el programa de actualización o intentar actualizarlo bajo demanda mediante **Actualizar ahora**.

## <a name="system-requirements"></a>Requisitos del sistema
Para importar los datos de [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] en Power BI, necesita permisos para los servicios web utilizados para recuperar datos. Los servicios web necesarios para los contenidos de paquetes incluyen:

**Microsoft Dynamics 365 for Finance and Operations – CRM**
- SalesOpportunities

**Microsoft Dynamics 365 for Finance and Operations – Sales**
- ItemSalesbyCustomer
- Power_BI_Item_Purchase_List
- Power_BI_Item_Sales_List
- SalesDashboard

**Microsoft Dynamics 365 for Finance and Operations – Finance**
- PowerBIFinance

**Microsoft Dynamics 365 for Finance and Operations – Jobs**
- Lista de proyectos
- Líneas planificación proyecto
- Líneas tarea proyecto

## <a name="web-services"></a>Servicios Web
Un modo de fácil de encontrar los servicios web es buscarlos en [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]. En la lista, asegúrese de que el cuadro Publicar esté marcado para los servicios web enumerados anteriormente.

## <a name="troubleshooting"></a>Solución de problemas
El panel de Power BI depende de los servicios web publicados que aparecen en la lista anterior y mostrará los datos de la empresa de demostración o de la suya propia si importa los datos de la solución de finanzas actual. Sin embargo, si se produce algún error, en esta sección se proporcionará una solución para los problemas más habituales.

### <a name="incorrect-company-name"></a>Nombre empresa incorrecto  
Un error común es introducir el nombre para mostrar de empresa en lugar del nombre de la empresa. Para buscar el nombre de la empresa, busque **Empresas**. A continuación, use el campo **Nombre** al introducir el nombre de su empresa.

### <a name="incorrect-user-name-and-password"></a>Nombre de usuario y contraseña incorrectos  
El nombre de usuario y la contraseña utilizados para conectarse deben ser los mismos que se usan para conectarse a su cuenta de Microsoft Office 365.  

Los paquetes de contenido requieren también que tenga una cuenta de Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)].  Una vez que introduzca sus credenciales, descubriremos automáticamente los inquilinos de Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] a los que tenga acceso.  Si no tiene una cuenta de prueba o con licencia de Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)], recibirá un mensaje de error.

## <a name="see-also"></a>Consulte también
[Introducción a Power BI](https://docs.microsoft.com/en-us/power-bi/service-get-started)  
[Power BI - Conceptos básicos](https://docs.microsoft.com/en-us/power-bi/service-basic-concepts)
[Inteligencia empresarial](bi.md)  
[[!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)  
[Importar datos de empresa de otros sistemas financieros](upload-data.md)  
[Configurar [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)  
[Finanzas](finance.md)  
[Informe de configuración de [!INCLUDE[d365fin](includes/d365fin_md.md)] en Power BI](across-how-use-financials-data-source-powerbi.md)  

