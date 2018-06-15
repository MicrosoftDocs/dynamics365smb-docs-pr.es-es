---
title: "Cómo conectar Power BI a Business Central | Documentos de Microsoft"
description: "Obtener información, inteligencia empresarial y KPI de los datos de Business Central resulta muy sencillo con Power BI y los paquetes de contenido de Business Central."
author: SusanneWindfeldPedersen
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: account schedule, analysis, reporting, financial report, business intelligence, KPI
ms.date: 04/03/2018
ms.author: solsen
redirect_url: admin-powerbi
ms.translationtype: HT
ms.sourcegitcommit: ad1b888d475c0523c5a905e804a3f89ab4531b28
ms.openlocfilehash: 0196bff5dedb878884fd3d6e0208022faa968dfd
ms.contentlocale: es-es
ms.lasthandoff: 05/17/2018

---
# <a name="connecting-power-bi-to-dynamics-365-business-central-content-packs"></a>Conectar Power BI con los paquetes de contenido de Dynamics 365 Business Central
Obtener información de los datos de Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] resulta muy sencillo con los paquetes de contenido de Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]. Power BI extrae los datos, genera un panel original y envía informes en función de los datos.

Debe disponer de una cuenta válida con Dynamics 365 y con Power BI. Además, deberá descargar [Power BI Desktop](https://powerbi.microsoft.com/en-us/desktop/) si desea crear sus propios informes de Power BI. Los paquetes de contenido de Power BI requieren permisos para las tablas desde donde se recuperan los datos. A continuación se describen más detalles sobre los requisitos.  

## <a name="how-to-connect"></a>Cómo conectarse
1. Seleccione **Obtener datos** en la parte inferior del panel de navegación izquierdo.  
![Navegar para obtener datos](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-get-data.png)

También puede empezar desde Dynamics 365 Business Edition. En el área de trabajo, vaya a **Selección de informe** de la parte Área de trabajo de Power BI. Seleccione **Servicio** o **Mi organización** en la cinta. Cuando cualquiera de estas acciones está seleccionada, accederá a la galería de la organización en Power BI o a la biblioteca de servicios en Power BI, que también se filtrarán para mostrar solo los paquetes de contenido relacionados con [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)].

2. En el cuadro **Servicios**, seleccione **Obtener**. Se abrirá una ventana con **AppSource** y **aplicaciones para aplicaciones de Power BI**.  
![Seleccionar paquetes de contenidos de servicios en línea](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-online-services-get.png)
3. Seleccione **Aplicaciones** de la pestaña **Aplicaciones para aplicaciones de Power BI** y elija el paquete de contenidos **Microsoft Dynamics 365 Business Central** que quiera usar, a continuación, seleccione **Obtener ahora**.  
![Seleccione Dynamics 365 Business Central y seleccione Obtener ahora](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-dynamics365-for-financials-get-it-now.png)
4. Cuando se lo solicite, escriba el nombre de *su empresa* en [!INCLUDE[d365fin_md](includes/d365fin_long_md.md)]. Este no es el nombre para mostrar. El nombre de la empresa puede encontrarse en la página "Empresas" de su instancia de [!INCLUDE[d365fin_md](includes/d365fin_long_md.md)]. 
![Seleccione Dynamics 365 Business Central y seleccione Obtener ahora](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-connect-to-d365-finance-and-operations-crm.png)
5. Una vez conectado se cargarán automáticamente un panel, un informe y un conjunto de datos en su espacio de trabajo de Power BI. Cuando se haya completado, se actualizarán los mosaicos con datos de su empresa de [!INCLUDE[d365fin_md](includes/d365fin_long_md.md)].
![Seleccione Dynamics 365 Business Central y seleccione Obtener ahora](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-workspace-dashboard-report-dataset.png)

## <a name="what-now"></a>¿Y ahora qué?

- Intente [hacer una pregunta en el cuadro de preguntas](https://docs.microsoft.com/en-us/power-bi/service-q-and-a) en la parte superior del escritorio.
- [Cambie los mosaicos](https://docs.microsoft.com/en-us/power-bi/service-dashboard-edit-tile) en el escritorio.  
- [Seleccione un mosaico](https://docs.microsoft.com/en-us/power-bi/service-dashboard-tiles) para abrir el informe subyacente.  
- Mientras que su conjunto de datos se programa para actualizarse diariamente, puede cambiar el programa de actualización o intentar actualizarlo bajo demanda mediante **Actualizar ahora**.

## <a name="system-requirements"></a>Requisitos del sistema
Para importar los datos de [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] en Power BI, necesita permisos para los servicios web utilizados para recuperar datos. Los servicios web necesarios para los contenidos de paquetes incluyen:

## <a name="role-center-reports"></a>Informes de Área de trabajo

**Microsoft Dynamics 365 Business Central – CRM**
- Oportunidades de venta
- Empresa de vista de plantilla de Excel
- Etiquetas de informe de Power BI

**Microsoft Dynamics 365 Business Central – Finance**
- PowerBIFinance
- Empresa de vista de plantilla de Excel
- Etiquetas de informe de Power BI

**Microsoft Dynamics 365 Business Central – Jobs**
- Lista de proyectos
- Líneas planificación proyecto
- Líneas tarea proyecto
- Etiquetas de informe de Power BI
- Empresa de vista de plantilla de Excel

**Microsoft Dynamics 365 Business Central - Sales**
- Panel de ventas
- Empresa de vista de plantilla de Excel
- Etiquetas de informe de Power BI

## <a name="list-page-reports"></a>Informes de páginas de listas 

**Microsoft Dynamics 365 Business Central – Customers List**
- Ventas de productos por cliente
- Lista de compra del producto Power BI
- Lista de ventas del producto Power BI
- Panel de ventas
- Lista de clientes de Power BI
- ExcelTemplateViewCompany
- Etiquetas de informe de Power BI 

**Microsoft Dynamics 365 Business Central - General Ledger Entries List**
- Lista de importes CG de Power BI
- Cantidad presupuestada CG de Power BI
- ExcelTemplateViewCompany
- Etiquetas de informe de Power BI

**Microsoft Dynamics 365 Business Central – Items List**
- Ventas de productos por cliente
- Lista de compra del producto Power BI
- Lista de ventas del producto Power BI
- Panel de ventas
- ExcelTemplateViewCompany
- Etiquetas de informe de Power BI

**Microsoft Dynamics 365 Business Central – Jobs List**
- Lista de proyectos de Power BI
- ExcelTemplateViewCompany
- Etiquetas de informe de Power BI

**Microsoft Dynamics 365 Business Central – Purchase Invoices List**
- Lista de compras de Power BI
- ExcelTemplateViewCompany
- Etiquetas de informe de Power BI

**Microsoft Dynamics 365 Business Central – Sales Orders List**
- Lista de ventas de Power BI
- ExcelTemplateViewCompany
- Etiquetas de informe de Power BI


**Microsoft Dynamics 365 Business Central – Vendors List**
- Lista de compra del producto Power BI
- Lista de ventas del producto Power BI
- Lista de proveedores de Power BI
- ExcelTemplateViewCompany
- Etiquetas de informe de Power BI

## <a name="web-services"></a>Servicios Web
Un modo de fácil de encontrar los servicios web es buscarlos en [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]. En la lista, asegúrese de que el cuadro Publicar esté marcado para los servicios web enumerados anteriormente.

## <a name="troubleshooting"></a>Solución de problemas
El panel de Power BI depende de los servicios web publicados que aparecen en la lista anterior y mostrará los datos de la empresa de demostración o de la suya propia si importa los datos de la solución de finanzas actual. Sin embargo, si se produce algún error, en esta sección se proporcionará una solución para los problemas más habituales.

### <a name="incorrect-company-name"></a>Nombre empresa incorrecto  
Un error común es introducir el nombre para mostrar de empresa en lugar del nombre de la empresa. Para buscar el nombre de la empresa, busque **Empresas**. A continuación, use el campo **Nombre** al introducir el nombre de su empresa.

### <a name="incorrect-user-name-and-password"></a>Nombre de usuario y contraseña incorrectos  
El nombre de usuario y la contraseña utilizados para conectarse deben ser los mismos que se usan para conectarse a su cuenta de Microsoft Office 365.  

Los paquetes de contenido requieren también que tenga una cuenta de Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]. Una vez que introduzca sus credenciales, descubriremos automáticamente los inquilinos de Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] a los que tenga acceso. Si no tiene una cuenta de prueba o con licencia de Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)], recibirá un mensaje de error.

### <a name="the-key-didnt-match-any-rows-in-the-table"></a>La clave no coincidió con ninguna fila de la tabla
Si introduce un nombre de empresa no válido durante el proceso de conexión, puede recibir el mensaje de error "La clave no coincidió con ninguna fila de la tabla". Proporcione el nombre correcto de la empresa e intente conectarse de nuevo.

## <a name="see-also"></a>Consulte también
[Introducción a Power BI](https://docs.microsoft.com/en-us/power-bi/service-get-started)  
[Power BI - Conceptos básicos](https://docs.microsoft.com/en-us/power-bi/service-basic-concepts)  
[Inteligencia empresarial](bi.md)  
[Introducción](product-get-started.md)  
[Importar datos de empresa de otros sistemas financieros](across-import-data-configuration-packages.md)  
[Configurar [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)  
[Finanzas](finance.md)  
[Informe de configuración de [!INCLUDE[d365fin](includes/d365fin_md.md)] en Power BI](across-how-use-financials-data-source-powerbi.md)  

