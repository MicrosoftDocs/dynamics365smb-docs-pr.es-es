---
title: Establecer el diseño de informe
description: Aprenda a configurar el diseño que se usa en un informe al obtener una vista previa e imprimir.
author: jswymer
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'customized report, document layout, logo, personalize'
ms.search.form: '9652, 9650'
ms.date: 08/12/2022
ms.author: jswymer
---
# <a name="setting-the-layout-used-by-a-report" />Establecer el diseño utilizado por un informe

> **SE APLICA A:** Business Central Online, Business Central local, lanzamiento de versiones 1 de 2022 y posteriores. Para versiones anteriores, vaya [aquí](ui-how-change-layout-currently-used-report.md).

El diseño de un informe determina el aspecto de un informe. Controla qué campos de datos de un conjunto de datos de informe aparecen, cómo se organizan, cómo se diseñan y más. Un informe puede tener más de un diseño, entre los que puede cambiar según sea necesario.

Cuando hay varias empresas en la aplicación, los diseños se establecen por empresa. Así, el mismo informe en una empresa puede tener un diseño diferente en otra.

## <a name="get-started" />Comenzar

Hay varias formas de establecer qué diseño usa un informe. Cada forma tiene ventajas, dependiendo de lo que estés buscando hacer: 

- Desde la página de solicitud de informe

  Al configurar la ejecución de un informe, la página de solicitud de informe incluye el campo **Diseño de informes** que muestra el diseño predeterminado actual utilizado por el informe. Puede usar este campo para cambiar temporalmente a otro diseño disponible el informe que está ejecutando. Después de ejecutar el informe, el diseño volverá al diseño predeterminado. Para más información, vea [Ejecutar e imprimir informes](ui-work-report.md#switching-the-report-layout).

- Desde la página **Selección de diseño de informes**

  La página **Selección de diseño de informes** muestra una lista de todos los informes. Esta página indica cuál es el diseño actual de un informe predeterminado. Le permite establecer diseños en diferentes empresas, sin tener que cambiar la empresa con la que está trabajando.

- Desde la página **Diseños de informe** La página **Diseños de informes** muestra todos los diseños disponibles para cada informe en la empresa actual. También se utiliza para especificar el diseño predeterminado de los informes. Es fácil encontrar un diseño específico ordenando o filtrando la lista. Una vez que haya encontrado el diseño, puede configurarlo para un informe con una sola selección.

  > [!NOTE]
  > No puede usar la página **Diseños de informe** para diseños de Word y RDLC que se crearon usando la función heredada **Diseños personalizados**. De hecho, ni siquiera verá estos diseños personalizados en la lista de la página **Diseños de informe**. Para estos diseños, solo puede configurarlos usando la página **Selección de diseño de informes**.

## <a name="set-the-layout-from-the-report-layouts-page" />Establecer el diseño desde la página Diseños de informe

[!INCLUDE[open-report-layouts-page](includes/open-report-layouts-page.md)]
2. Busque el diseño en la lista, selecciónelo y, a continuación, seleccione la acción **Establecer valor predeterminado** en la parte superior de la página.

## <a name="set-the-layout-from-report-layout-selection-page" />Establecer el diseño desde la página Selección de diseño de informes

1. Elija el icono ![Bombilla que abre la característica Dígame 1.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Selección de diseño de informes** y luego elija el enlace relacionado.
  
   La página muestra una lista de todos los informes que están disponible para la empresa que está especificada en el campo **Empresa** en la parte superior de la página. El campo **Descripción de diseño** especifica el diseño que el informe está usando actualmente.
2. Establezca el campo **Empresa** en la parte superior en la empresa que incluye el informe.
3. Busque y seleccione el informe en la lista y realice uno de los siguientes pasos:

   - Si el diseño al que desea cambiar es de un tipo diferente al diseño actual, seleccione el campo **Tipo de diseño** y luego elija el tipo de diseño que desea establecer en el informe. 
   - Si el diseño que desea cambiar al mismo tipo que el diseño actual, seleccione la acción **Seleccionar diseño** en la parte superior.

4. En la página **Diseños de informe**, seleccione el diseño, luego seleccione **Aceptar**.

## <a name="revert-to-the-original-default-layout" />Revertir al diseño predeterminado original

Los informes están diseñados para usar un diseño de forma predeterminada. Puede volver al diseño predeterminado original desde la página **Selección de diseño de informes**. Simplemente seleccione el informe, luego seleccione la acción **Restaurar la selección predeterminada** en la parte superior de la página.

## <a name="see-related-microsoft-trainingtrainingmoduleschange-documents-dynamics--business-centralindex" />Consultar la [formación de Microsoft](/training/modules/change-documents-dynamics-365-business-central/index) relacionada

## <a name="see-also" />Consulte también

[Gestión de diseños de informe](ui-manage-report-layouts.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
