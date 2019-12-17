---
title: Mostrar informes de Power BI personalizados | Documentos de Microsoft
description: Puede usar los informes de Power BI para obtener información adicional sobre los datos en las listas.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: business intelligence, KPI, Odata, Power App, SOAP, analysis
ms.date: 10/01/2019
ms.author: edupont
ms.openlocfilehash: 0506dad5f65766919405dd944d75b014957b509c
ms.sourcegitcommit: cfc92eefa8b06fb426482f54e393f0e6e222f712
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 12/03/2019
ms.locfileid: "2879432"
---
# <a name="viewing-list-data-in-power-bi-reports-in-business-central"></a>Ver datos de listas en informes de Power BI en Business Central

[!INCLUDE[prodlong](includes/prodlong.md)] incluye un elemento de control de cuadro informativo de varias páginas de lista de claves que proporciona información de los datos de la lista. A medida que se desplaza por las filas de la lista, el informe se actualiza y se filtra para la entrada seleccionada. Puede crear informes personalizados para mostrar en este control, pero hay reglas a seguir al crear informes para garantizar que proporcionan el comportamiento deseado.  

> [!NOTE]  
> Debe disponer de una cuenta válida con [!INCLUDE[prodshort](includes/prodshort.md)] y con Power BI. Además, para crear informes personalizados, debe descargar [Power BI Desktop](https://powerbi.microsoft.com/desktop/). Para obtener más información, consulte [Usar [!INCLUDE[d365fin](includes/d365fin_md.md)] como origen de datos de Power BI](across-how-use-financials-data-source-powerbi.md).  

## <a name="report-data-set"></a>Conjunto de datos del informe
Al crear el informe en Power BI Desktop, especifique el origen de datos o un servicio web que contenga los datos relacionados con la lista a la que desea asociar el informe. Por ejemplo, si desea crear un informe para la lista Ventas, asegúrese de que el conjunto de datos contenga información relacionada con ventas.  

Para filtrar los datos de los informes en función del registro seleccionado en la página de listas, se debe usar la clave primaria como filtro de informe. Las claves primarias deben ser parte del conjunto de datos para que los informes se filtren correctamente. En la mayoría de los casos, la clave primaria de una lista es **Nº** .  

## <a name="defining-the-report-filter"></a>Definir el filtro de informe
El informe debe tener un filtro de informe básico (no una página o un filtro visual ni un filtro avanzado) para filtrar correctamente en el cuadro informativo de Power BI. El filtro que se pasa al informe de Power BI desde cada página de lista se basará en la clave primaria tal como se ha descrito en la sección anterior.  

Para definir un filtro para el informe, seleccione la clave primaria en la lista de campos disponibles y, a continuación, arrastre y suelte el campo en la sección **Filtro de informe**.  

![Configurar el filtro para el informe Actividad de facturas de venta](./media/across-how-use-powerbi-reports-factbox/financials-powerbi-report-filter.png)

## <a name="report-size-and-color"></a>Tamaño y color del informe
El tamaño del informe se debe configurar en 325 píxeles por 310 píxeles. Esto es necesario para el escalado correcto del informe en el espacio disponible que permite el control del cuadro informativo de Power BI. Para definir el tamaño del informe, coloque el enfoque fuera del área de diseño de informe y, a continuación, elija el icono de rodillo de pintura.

![Configurar la anchura y la altura para el informe Actividad de facturas de venta](./media/across-how-use-powerbi-reports-factbox/financials-powerbi-report-sizing.png)

Puede cambiar el ancho y el alto del informe eligiendo **Personalizado** en el campo **Tipo**.

Del mismo modo, si desea que el fondo del informe se mezcle con el color de fondo del control del cuadro informativo de Power BI, defina un color de fondo de informe personalizado de *E5E5E5*. Es opcional.  

## <a name="reports-with-multiple-pages"></a>Informes con varias páginas
Con Power BI, puede crear un solo informe con varias páginas. Los elementos visuales que desee ver en las páginas de listas de [!INCLUDE[d365fin](includes/d365fin_md.md)] deben estar en la primera página del informe en Power BI.  

> [!NOTE]  
> El cuadro informativo de Power BI solo puede mostrar la primera página del informe; si desea ver otras páginas, debe expandir el informe y usar las pestañas de la parte inferior del informe para desplazarse a otras páginas.  

## <a name="saving-your-report"></a>Guardar el informe

Cuando guarde el informe, es recomendable que el nombre del informe contenga el nombre de la página de listas en la que desee mostrar el informe. Por ejemplo, la palabra *Proveedor* debe estar en cualquier parte del nombre del informe para los informes que desee que estén disponibles en la lista de proveedores.  

Esto no es un requisito; sin embargo, acelerará el proceso de seleccionar informes. Cuando la página de selección de informe se abra desde una página de lista, pasaremos un filtro basado en el nombre de página para limitar los informes que se muestran.  Puede quitar el filtro para obtener una lista completa de los informes disponibles en Power BI.  

## <a name="troubleshooting"></a>Solución de problemas
En esta sección se proporciona una solución para los problemas más habituales que se produzcan al crear el informe de Power BI.  

**El usuario no ve un informe en la página Seleccionar informe que desea seleccionar** Si no puede seleccionar un informe, una solución posible es comprobar el nombre del informe para asegurarse de que contiene el nombre de la página de listas. También puede borrar el filtro para obtener una lista completa de los informes de Power BI disponibles.  

**El informe se carga pero está en blanco, no se ha filtrado o se ha filtrado incorrectamente** Compruebe que el filtro de informe contenga la clave primaria correcta. En la mayoría de los casos, es el campo **Nº**, pero en la tabla **Mov. contabilidad**, por ejemplo, debe usar el campo **Nº mov.**

**El informe se carga, pero no muestra la página prevista** Compruebe que la página que desea mostrar es la primera página del informe.  

**El informe aparecerá con bordes grises no deseados, es demasiado pequeño o demasiado grande**

Compruebe que el tamaño del informe se ha configurado en 325 píxeles x 310 píxeles. Guarde el informe y, a continuación, actualice la página de listas.  

## <a name="see-also"></a>Consulte también

[Habilitar los datos de negocio para Power BI](admin-powerbi.md)  
[Usar [!INCLUDE[d365fin](includes/d365fin_md.md)] como origen de datos de Power BI](across-how-use-financials-data-source-powerbi.md)  
[Introducción](product-get-started.md)  
[Configurar [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)  
[Finanzas](finance.md)  
