---
title: Mostrar informes de Power BI personalizados
description: Puedes usar Power BI FactBox para mostrar informes de Power BI y obtener información adicional sobre los datos de los registros en las listas clave.
author: jswymer
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: business intelligence, KPI, Odata, Power App, SOAP, analysis
ms.date: 06/11/2021
ms.author: jswymer
ms.openlocfilehash: ccdcf519d33c9b4ee23526e773ec8eccc9e0ebdd
ms.sourcegitcommit: 8a12074b170a14d98ab7ffdad77d66aed64e5783
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 03/31/2022
ms.locfileid: "8517166"
---
# <a name="creating-power-bi-reports-for-displaying-list-data-in-prod_short"></a>Crear informes de Power BI para mostrar datos de lista en [!INCLUDE[prod_short](includes/prod_short.md)]

[!INCLUDE[prod_long](includes/prod_long.md)] incluye un elemento de control de cuadro informativo de Power BI en muchas páginas de lista clave. El objetivo de este cuadro informativo es mostrar informes de Power BI relacionados con los registros de las listas, lo que ofrece más información sobre los datos. La idea es que a, medida que se desplaza por las filas de la lista, el informe se actualice para la entrada seleccionada.

[!INCLUDE[prod_long](includes/prod_long.md)] viene listo con algunos de estos informes. También puede crear sus propios informes personalizados que se muestran en este cuadro informativo. La creación de estos informes es similar a otros informes. Pero hay algunas reglas de diseño que deberá seguir para asegurarse de que los informes se muestren como se espera. En este artículo se explica estas reglas.

> [!NOTE]
> Para obtener información general sobre la creación y la publicación de informes de Power BI para Business Central, consulte [Creación de informes de Power BI para mostrar datos de [!INCLUDE [prod_long](includes/prod_long.md)]](across-how-use-financials-data-source-powerbi.md). 

## <a name="prerequisites"></a>Requisitos previos

- Una cuenta de Power BI.
- Power BI Desktop.

<!-- 
For more information about getting started, see [Use [!INCLUDE[prod_short](includes/prod_short.md)] as a Power BI Data Source](across-how-use-financials-data-source-powerbi.md).-->

## <a name="create-a-report-for-a-list-page"></a>Crear un informe para una página de lista

1. Inicie Power BI Desktop.
2. Seleccione **Obtener datos** y comience a elegir el origen de datos para el informe.

    Especifique las páginas de lista de Business Central que contienen los datos que desea en el informe. Por ejemplo, para crear un informe para la lista **Facturas de venta**, incluya páginas relacionadas con las ventas.

    Para obtener más información, siga las instrucciones [Agregar [!INCLUDE[prod_short](includes/prod_short.md)] como origen de datos en Power BI Desktop](across-how-use-financials-data-source-powerbi.md#getdata).

3. Establezca el filtro de informe.

    Para hacer que los datos se actualicen en el registro seleccionado en la lista, agregue un filtro al informe. El filtro debe incluir un campo del origen de datos que se usa para identificar cada registro de la lista de forma única. En términos de desarrollador, este campo es la *clave primaria*. En la mayoría de los casos, la clave primaria de una lista es **Nº** .

    Para configurar el filtro, siga los siguientes pasos:

    1. En **Filtros**, seleccione el campo de clave primaria de la lista de campos disponibles.
    2. Arrastre el campo al panel **Filtros** y colóquelo en el cuadro **Filtros en todas las páginas**.
    3. Establezca el **Tipo de filtro** en **Filtrado básico**. No puede ser un filtro de página, visual o avanzado.

    ![Configurar el filtro para el informe Actividad de facturas de venta.](./media/across-how-use-powerbi-reports-factbox/financials-powerbi-report-filter-v3.png)
4. Diseñe el informe.

    Cree el diseño arrastrando campos y agregando visualizaciones. Para obtener más información, consulte [Trabajar con la vista Informe en Power BI Desktop](/power-bi/create-reports/desktop-report-view) en la documentación de Power BI.

5. Consulte las siguientes secciones sobre el tamaño del informe y el uso de varias páginas.

6. Guarde y asigne un nombre al informe.

    Dele al informe un nombre que contenga el nombre de la página de lista asociada con el informe, como esté en el cliente. Sin embargo, el nombre no distingue entre mayúsculas y minúsculas. Suponga que el informe es para la página de lista **Facturas de venta**. En este caso, incluya las palabras **facturas de venta** en algún lugar del nombre, como **mis facturas de venta.pbix** o **mi_lista_facturas_de_venta.pbix**.

    Esta convención de nomenclatura no es un requisito. Sin embargo, hace que la selección de informes en [!INCLUDE[prod_short](includes/prod_short.md)] sea más rápida. Cuando la página de selección de informes se abre desde una página de lista, se aplica automáticamente un filtro según el nombre de la página. El filtro tiene la sintaxis: `@*<caption>*`, como `@*Sales Invoices*`. Este filtrado se realiza para limitar los informes que se muestran. Los usuarios pueden borrar el filtro para obtener una lista completa de los informes disponibles en Power BI.

7. Cuando haya terminado, publique el informe como de costumbre.

    Para obtener más información, consulte [Publicar un informe](across-how-use-financials-data-source-powerbi.md#publish-reports).

8. Pruebe el informe.

    Una vez que el informe se haya publicado en su área de trabajo, debería estar disponible en el cuadro informativo de Power BI en la página de lista en [!INCLUDE[prod_short](includes/prod_short.md)].

    Para probarlo, siga los siguientes pasos.

    1. Abra [!INCLUDE[prod_short](includes/prod_short.md)] y vaya a la página de la lista.
    2. Si no ve el cuadro informativo de Power BI, vaya a la barra de acciones y seleccione **Acciones** > **Mostrar** > **Mostrar/ocultar informes de Power BI**.
    3. En el cuadro informativo de Power BI, seleccione **Seleccionar informes**, seleccione el cuadro **Habilitar** para el informe y, a continuación, **Aceptar**.

    Si está diseñado correctamente, se muestra el informe.  

## <a name="set-the-report-size-and-color"></a>Configurar el tamaño y el color del informe

El tamaño del informe se debe configurar en 325 píxeles por 310 píxeles. Este tamaño proporciona el escalado correcto del informe en el espacio disponible del control del cuadro informativo de Power BI en [!INCLUDE[prod_short](includes/prod_short.md)]. Para definir el tamaño del informe, coloque el enfoque fuera del área de diseño de informe y, a continuación, elija el icono de rodillo de pintura.

![Configurar la anchura y la altura para el informe Actividad de facturas de venta.](./media/across-how-use-powerbi-reports-factbox/financials-powerbi-report-sizing-v3.png)

Puede cambiar el ancho y el alto del informe eligiendo **Personalizado** en el campo **Tipo**.

Si desea que el fondo del informe se mezcle con el color de fondo del control del cuadro informativo de Power BI, defina un color de fondo de informe personalizado como *#FFFFFF* (blanco). 

> [!TIP]
> Use el archivo de tema [!INCLUDE [prod_short](includes/prod_short.md)] para crear informes con el mismo estilo de color que las aplicaciones de [!INCLUDE [prod_short](includes/prod_short.md)]. Para obtener más información, consulte [Usar el tema de informe de [!INCLUDE [prod_short](includes/prod_short.md)]](across-how-use-financials-data-source-powerbi.md#theme).

## <a name="reports-with-multiple-pages"></a>Informes con varias páginas

Con Power BI, puede crear un solo informe con varias páginas. Sin embargo, para los informes que se mostrarán con páginas de lista, no recomendamos que tengan más de una página. El cuadro informativo de Power BI solo mostrará la primera página de su informe.

## <a name="fixing-problems"></a>Solucionar problemas

En esta sección se explica cómo solucionar los problemas que puede encontrar al intentar ver un informe de Power BI para una página de lista en [!INCLUDE[prod_short](includes/prod_short.md)].  

### <a name="you-cant-see-the-power-bi-factbox-on-a-list-page"></a>No puede ver el cuadro informativo de Power BI en una página de lista

De forma predeterminada, el cuadro informativo de Power BI está oculto a la vista. Para mostrar el cuadro informativo en una página, en la barra de acciones, seleccione **Acciones** > **Mostrar** > **Mostrar/ocultar informes de Power BI**.

### <a name="you-cant-see-the-report-in-the-select-report-pane"></a>No puede ver el informe en el panel Seleccionar informe

El nombre del informe no contiene el nombre de la página de la lista que se muestra. Borre el filtro para obtener una lista completa de los informes de Power BI disponibles.  

### <a name="report-is-loaded-but-blank-not-filtered-or-filtered-incorrectly"></a>El informe está cargado pero en blanco, no filtrado o filtrado incorrectamente

Verifique que el filtro de informes contenga la clave principal correcta. En la mayoría de los casos, este campo es **Nº**, pero en la tabla **Mov. contabilidad**, por ejemplo, debe usar el campo **Nº mov.**.

### <a name="report-is-loaded-but-it-shows-a-page-you-didnt-expect"></a>El informe está cargado, pero muestra una página que no esperaba

Verifique que la página que desea que se muestre es la primera página de su informe.  

### <a name="report-appears-with-an-unwanted-gray-boarder-or-its-too-small-or-too-large"></a>El informe aparecerá con un borde gris no deseado o es demasiado pequeño o demasiado grande

Compruebe que el tamaño del informe se ha configurado en 325 píxeles x 310 píxeles. Guarde el informe y, a continuación, actualice la página de listas.  

## <a name="see-related-training-at-microsoft-learn"></a>Consulte la Formación relacionada en [Microsoft Learn](/learn/modules/configure-powerbi-excel-dynamics-365-business-central/index)

## <a name="see-also"></a>Consulte también

[Habilitar los datos de negocio para Power BI](admin-powerbi.md)  
[Usar [!INCLUDE[prod_short](includes/prod_short.md)] como origen de datos de Power BI](across-how-use-financials-data-source-powerbi.md)  
[Preparación para hacer negocios](ui-get-ready-business.md)  
[Configurar [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md)  
[Finanzas](finance.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]