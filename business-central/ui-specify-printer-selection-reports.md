---
title: Especificar una impresora predeterminada
description: Conozca las distintas formas de configurar las impresoras para que se utilicen por defecto para los trabajos de impresión.
author: jswymer
ms.topic: how-to
ms.reviewer: na
ms.service: dynamics365-business-central
ms.custom: bap-template
ms.search.keywords: 'online printing, email printing, cloud printing, Universal Print'
ms.search.form: '2650, 2750, 2752, 2753, 2754, 8900,'
ms.date: 02/09/2023
ms.author: jswymer
---
# <a name="specify-a-default-printer"></a><a name="default"></a>Especificar una impresora predeterminada

Después de configurar las impresoras en Business Central, puede especificar qué impresora desea usar de forma predeterminada. Hay un par de maneras de especificar las impresoras que se utilizarán por defecto para los informes y otros trabajos de impresión. Una impresora predeterminada es útil si trabaja con diferentes informes que requieren impresoras diferentes debido a su ubicación en la empresa o sus capacidades de salida.

> [!IMPORTANT]
> Las únicas impresoras que puede especificar como predeterminadas son **Microsoft Print to PDF** y las impresoras en la nube que ya se configuraron para su uso en Business Central, como las impresoras de correo electrónico y las impresoras Universal Print. Las impresoras en la nube generalmente las configura un administrador. Para obtener más información, consulte [Configuración y administración de la impresora](admin-printer-setup-overview.md).   

## <a name="set-a-printer-as-a-default-printer-for-all-print-jobs"></a>Configurar una impresora como impresora predeterminada para todos los trabajos de impresión

Mediante la página **Administración de impresoras** puede configurar una impresora como impresora predeterminada para todos los trabajos de impresión. Puede especificar la impresora como predeterminada solo para usted o para todos los usuarios.

1. Elija el icono ![Bombilla que abre la característica Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Administración de impresoras** y, a continuación, elija el vínculo relacionado.

    > [!TIP]
    > También puede abrir la página **Administración de impresoras** desde la página **Selecciones de impresora** eligiendo **Administración de impresoras**.  
2. En la página **Administración de impresoras**, seleccione una impresora de la lista, elija **Administrar** y, a continuación, **Establecer como mi impresora predeterminada** o **Establecer como impresora predeterminada para todos los usuarios**.

> [!NOTE]
> La configuración de una impresora predeterminada desde el **Administración de impresoras** agregará una entrada en las **Selecciones de impresora**.

## <a name="set-a-default-printer-for-specific-reports"></a>Establecer una impresora predeterminada para informes específicos

La página **Selecciones de impresora** le permite especificar la impresora que usará un informe de forma predeterminada. Las impresoras predeterminadas se configuran por cuenta de usuario. Puede configurar una impresora predeterminada solo para usted, para otro usuario o para todos los usuarios.

1. Elija el icono ![Bombilla que abre la característica Dígame](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Selecciones de impresora** y, a continuación, elija el vínculo relacionado. Alternativamente, desde la página **Administración de impresoras**, seleccione una impresora y luego elija la acción **Selecciones de impresoras**.
2. Elija la acción **Nuevo** para agregar una selección de impresora para un informe específico.
3. Rellene los campos según sea necesario.

El informe especificado estará ahora configurado para imprimirse en la impresora seleccionada de manera predeterminada.

> [!NOTE]
> Cuando imprime el informe en cuestión, puede seleccionar uno diferente usando el campo **Imprimir** en la página de solicitud de informe.

> [!NOTE]
> Si no configura un informe para una impresora específica en la página **Selecciones de impresora**, se imprimirá en la impresora predeterminada de la empresa, tal como se define en la página **Administración de impresoras**.

Usted o el administrador también pueden usar la página **Selecciones de impresora** para definir otras variaciones de impresión para usuarios e informes. La tabla siguiente describe la combinación de valores para especificar una configuración de impresión diferente para un informe.

|Para                                                 |Establecer los valores siguientes                                             |
|---------------------------------------------------|---------------------------------------------------------------------|
|Imprimir un informe en una impresora específica para todos los usuarios |Especifique los valores de los campos **Id. informe** y **Nombre impresora** y deje en blanco el campo **Id. usuario**.|
|Imprimir todos los informes en una impresora específica para un usuario específico|Especifique los valores de los campos **Id. usuario** y **Nombre impresora** y deje en blanco el campo **Id. informe**. Esta entrada hace lo mismo que la acción **Establecer como mi impresora predeterminada** en la página **Administración de impresión**.|
|Establecer la impresora predeterminada para todos los informes de todos los usuarios|Especifique un valor en el campo **Nombre impresora** y deje en blanco los campos **Id. usuario** e **Id. informe**. Esta entrada hace lo mismo que la acción **Establecer como impresora predeterminada para todos los usuarios** en la página **Administración de impresión**.|
|Imprimir un informe específico en la impresora predeterminada del usuario|Especifique un valor en el campo **Id. informe** y deje en blanco los campos **Id. usuario** y **Nombre impresora**.|
|Imprimir un informe específico en una impresora concreta para un usuario específico|Especifique los valores de los tres campos.|

> [!NOTE]
> Las selecciones de impresora más específicas tienen preferencia sobre las selecciones de impresora más generales. Por ejemplo, una selección de impresora que tenga valores en **ID de usuario**, **ID de informe** y **Nombre de impresora** tiene prioridad sobre una selección de impresora que tenga entradas en blanco en los campos **ID de usuario** o **ID de informe**.

## <a name="choosing-the-printer-when-running-a-report"></a>Elección de la impresora al generar un informe

En lugar de utilizar la impresora predeterminada al ejecutar un informe, puede anular esta configuración desde la página de solicitud. Simplemente elija la impresora que desea utilizar para esta generación del informe en el menú desplegable **Impresora**.

## <a name="sizing-print-jobs"></a>Cambio de tamaño de los trabajos de impresión

La impresión en la nube se ha diseñado para documentos de un tamaño razonable. La mayoría de los servicios en la nube, incluidos PrintNode y HP ePrint, tienen un límite de 10 MB por trabajo. Si necesita imprimir informes más grandes, es posible que deba dividirlos en varias copias impresas.

[Formación de Microsoft](/training/modules/change-documents-dynamics-365-business-central/)

## <a name="see-also"></a>Consulte también .

[Administración de impresoras](admin-printer-setup-overview.md)  
[Configurar impresoras de Impresión universal](admin-printer-setup-universal-print.md)  
[Configurar impresoras por correo electrónico](admin-printer-setup-email.md)  
[Imprimir un informe](ui-work-report.md#PrintReport)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Ejecutar procesos](ui-how-run-batch-jobs.md)  
[Enviar documentos por correo electrónico](ui-how-send-documents-email.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
