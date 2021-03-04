---
title: Mostrar informes de Power BI personalizados para datos de Business Central | Documentos de Microsoft
description: Puede usar los informes de Power BI para obtener información adicional sobre los datos en las listas.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: business intelligence, KPI, Odata, Power App, SOAP, analysis
ms.date: 10/01/2020
ms.author: jswymer
ms.openlocfilehash: 069efcef517cd442539f13fad5e5a2c89e1533ff
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "4754472"
---
# <a name="creating-power-bi-reports-for-displaying-list-data-in-prod_short"></a>Crear informes de Power BI para mostrar datos de lista en [!INCLUDE[prod_short](includes/prod_short.md)]

[!INCLUDE[prod_long](includes/prod_long.md)] incluye un elemento de control de cuadro informativo de varias páginas de lista de claves que proporciona información de los datos de la lista. A medida que se desplaza por las filas de la lista, el informe se actualiza y se filtra para la entrada seleccionada. Puede crear informes personalizados para mostrar en este control. Sin embargo, hay algunas reglas a seguir para garantizar que los informes funcionen como se espera.  

## <a name="prerequisites"></a>Requisitos previos

- Una cuenta de Power BI.
- Power BI Desktop.

Para obtener más información sobre cómo empezar, consulte [Usar [!INCLUDE[prod_short](includes/prod_short.md)] como origen de datos de Power BI](across-how-use-financials-data-source-powerbi.md).

## <a name="defining-the-report-data-set"></a>Definición del conjunto de datos del informe

Especifique la fuente de datos que contiene los datos relacionados con la lista. Por ejemplo, para crear un informe para la lista Ventas, asegúrese de que el conjunto de datos contenga información relacionada con ventas.  

## <a name="defining-the-report-filter"></a>Definir el filtro de informe

Para hacer que los datos se actualicen en el registro seleccionado en la lista, agregue un filtro al informe. El filtro debe incluir un campo de la fuente de datos que se utiliza como *Clave primaria*. En la mayoría de los casos, la clave primaria de una lista es **Nº** .

Para definir un filtro para el informe, seleccione la clave primaria en la lista de campos disponibles y, a continuación, arrastre y suelte el campo en la sección **Filtro de informe**. El filtro debe ser un filtro de informe básico definido para todas las páginas. No puede ser un filtro de página, visual o avanzado.

![Configurar el filtro para el informe Actividad de facturas de venta](./media/across-how-use-powerbi-reports-factbox/financials-powerbi-report-filter-v3.png)

## <a name="setting-the-report-size-and-color"></a>Configurar el tamaño y el color del informe

El tamaño del informe se debe configurar en 325 píxeles por 310 píxeles. Este tamaño proporciona el escalado correcto del informe en el espacio disponible del control del cuadro informativo de Power BI en [!INCLUDE[prod_short](includes/prod_short.md)]. Para definir el tamaño del informe, coloque el enfoque fuera del área de diseño de informe y, a continuación, elija el icono de rodillo de pintura.

![Configurar la anchura y la altura para el informe Actividad de facturas de venta](./media/across-how-use-powerbi-reports-factbox/financials-powerbi-report-sizing-v3.png)

Puede cambiar el ancho y el alto del informe eligiendo **Personalizado** en el campo **Tipo**.

Si desea que el fondo del informe se mezcle con el color de fondo del control del cuadro informativo de Power BI, defina un color de fondo de informe personalizado como *#FFFFFF*. 

## <a name="using-reports-with-multiple-pages"></a>Uso de informes con varias páginas

Con Power BI, puede crear un solo informe con varias páginas. Sin embargo, para los informes que se mostrarán con páginas de lista, no recomendamos que tengan más de una página. El cuadro informativo de Power BI solo mostrará la primera página de su informe.

## <a name="naming-the-report"></a>Dar nombre al informe

Asigne al informe un nombre que contenga el nombre de la página de lista asociada con el informe. Por ejemplo, si el informe es para la página de lista **Vendedor**, incluya la palabra *vendedor* en algún lugar del nombre.  

Esta convención de nomenclatura no es un requisito. Sin embargo, hace que la selección de informes en [!INCLUDE[prod_short](includes/prod_short.md)] sea más rápida. Cuando la página de selección de informes se abre desde una página de lista, se filtra automáticamente según el nombre de la página. Este filtrado se realiza para limitar los informes que se muestran. Los usuarios pueden borrar el filtro para obtener una lista completa de los informes disponibles en Power BI.  

## <a name="fixing-problems"></a>Solucionar problemas

En esta sección se proporciona una solución para los problemas más habituales que se produzcan al crear el informe de Power BI.  

#### <a name="you-cant-see-a-report-on-the-select-report-page"></a>No puede ver un informe en la página Seleccionar informe

Probablemente se deba a que el nombre del informe no contiene el nombre de la página de la lista. Borre el filtro para obtener una lista completa de los informes de Power BI disponibles.  

#### <a name="report-is-loaded-but-blank-not-filtered-or-filtered-incorrectly"></a>El informe está cargado pero en blanco, no filtrado o filtrado incorrectamente

Verifique que el filtro de informe contenga la clave primaria correcta. En la mayoría de los casos, este campo es **Nº**, pero en la tabla **Mov. contabilidad**, por ejemplo, debe usar el campo **Nº mov.**.

#### <a name="report-is-loaded-but-it-shows-a-page-you-didnt-expect"></a>El informe está cargado, pero muestra una página que no esperaba

Verifique que la página que desea que se muestre es la primera página de su informe.  

#### <a name="report-appears-with-an-unwanted-gray-boarder-or-its-too-small-or-too-large"></a>El informe aparecerá con un borde gris no deseado o es demasiado pequeño o demasiado grande

Compruebe que el tamaño del informe se ha configurado en 325 píxeles x 310 píxeles. Guarde el informe y, a continuación, actualice la página de listas.  

## <a name="see-related-training-at-microsoft-learn"></a>Consulte Formación relacionada en [Microsoft Learn](/learn/modules/configure-powerbi-excel-dynamics-365-business-central/index)

## <a name="see-also"></a>Consulte también

[Habilitar los datos de negocio para Power BI](admin-powerbi.md)  
[Usar [!INCLUDE[prod_short](includes/prod_short.md)] como origen de datos de Power BI](across-how-use-financials-data-source-powerbi.md)  
[Introducción](product-get-started.md)  
[Configurar [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md)  
[Finanzas](finance.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]