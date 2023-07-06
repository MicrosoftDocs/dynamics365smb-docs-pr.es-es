---
title: Compartir y exportar informes con la bandeja de entrada de informes
description: 'Utilice la página Bandeja de entrada de informes para descargar, compartir y exportar informes en Business Central.'
author: rubenseishima
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'task, process, report, print, schedule, save, Excel, PDF, dataset, export, report inbox, onedrive,'
ms.search.form: 680
ms.date: 08/08/2022
ms.author: a-reishima
---
# <a name="share-and-export-reports-with-the-report-inbox"></a><a name="share-and-export-reports-with-the-report-inbox"></a><a name="share-and-export-reports-with-the-report-inbox"></a><a name="share-and-export-reports-with-the-report-inbox"></a>Compartir y exportar informes con la bandeja de entrada de informes

La página **Bandeja de entrada de informes** enumera los informes programados generados por el usuario en [!INCLUDE[prod_short](includes/prod_short.md)], y se puede utilizar no solo para acceder a los informes generados, sino también para compartir y abrir los archivos en OneDrive for Business.

> [!TIP]
> Las siguientes acciones también están disponibles en la parte **Bandeja de entrada de informes** en el Área de trabajo. Si la parte no se muestra en su interfaz, aprenda cómo personalizar su área de trabajo aquí: [Personalice su espacio de trabajo](ui-personalization-user.md).

## <a name="download-generated-reports"></a><a name="download-generated-reports"></a><a name="download-generated-reports"></a><a name="download-generated-reports"></a>Descargar informes generados

Para guardar informes anteriores, abra la página **Bandeja de entrada de informes** siguiendo estos pasos:

1. Elija el icono ![Bombilla que abre la característica Dígame 1.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Bandeja de entrada de informes** y luego elija el vínculo relacionado.  
2. En la página **Bandeja de entrada de informes**, elija el informe deseado.

> [!NOTE]
> La página no enumera los informes anteriores generados con la acción **Imprimir** o guardado como un archivo en el menú **Informes**.
>
> Los archivos generados se guardan en el formato definido al programar el informe y se pueden cambiar en la página **Entradas de la cola de trabajos**, junto con la recurrencia y otras configuraciones. Obtenga información sobre cómo cambiar el formato del archivo de informe y establecer opciones adicionales en [Administrar informes recurrentes programados](ui-work-report.md#manage-scheduled-recurring-reports).

## <a name="open-generated-reports-in-onedrive"></a><a name="open-generated-reports-in-onedrive"></a><a name="open-generated-reports-in-onedrive"></a><a name="open-generated-reports-in-onedrive"></a>Abrir informes generados en OneDrive

Para exportar el archivo de informe a Microsoft OneDrive para la Empresa, seleccione el informe en la página **Bandeja de entrada de informes** y elija la acción **Abrir en OneDrive**. A continuación, el informe se copia en la carpeta [!INCLUDE[prod_short](includes/prod_short.md)] en OneDrive y abierto en una nueva ventana del navegador, donde puede imprimir y administrar el archivo del documento.

> [!IMPORTANT]
>
> Informes programados para expirar en la página **Programar un informe** y copiados en OneDrive no se eliminan automáticamente de la carpeta compartida.

## <a name="share-scheduled-reports"></a><a name="share-scheduled-reports"></a><a name="share-scheduled-reports"></a><a name="share-scheduled-reports"></a>Compartir informes programados

Compartir informes con colaboradores también es posible en la página **Bandeja de entrada de informes**. Seleccione el informe y elija la acción **Compartir** . En la página **Enviar enlace**, seleccione quién puede abrir el archivo, defina permisos de edición, luego elija **Enviar** para enviar un enlace para acceder al informe guardado.

> [!NOTE]
> Para aprender más sobre la integración de OneDrive y características en [!INCLUDE[prod_short](includes/prod_short.md)], incluida la configuración por primera vez y las opciones para tratar los conflictos de nombres de archivo, lea el artículo[Abrir y compartir archivos en OneDrive](across-share-onedrive.md).
>
> Usar la acción **Compartir** hace que el archivo de informe generado esté disponible para otros usuarios solo en OneDrive para la Empresa y no incluye el informe programado en su **Bandeja de entrada de informes**.

## <a name="see-related-training-at-microsoft-learn"></a><a name="see-related-training-at-microsoft-learn"></a><a name="see-related-training-at-microsoft-learn"></a><a name="see-related-training-at-microsoft-learn"></a>Consulte la formación relacionada en [Microsoft Learn](/learn/paths/build-reports/)

## <a name="see-also"></a><a name="see-also"></a><a name="see-also"></a><a name="see-also"></a>Consulte también .

[Ejecutar e imprimir informes](ui-work-report.md)  
[Informes disponibles en [!INCLUDE[prod_short](includes/prod_short.md)]](reports-available-reports.md)  
[Usar informes en el trabajo diario](reports-use-reports.md)  
[Descripción general de Inteligencia empresarial e informes](reports-bi-reporting.md)  
[Configuración de impresoras](ui-specify-printer-selection-reports.md)  
[Trabajar con fechas y horas del calendario](ui-enter-date-ranges.md)  
[Administrar diseños de informes y documentos](ui-manage-report-layouts.md)  
Integración de [[!INCLUDE[prod_short](includes/prod_short.md)] y OneDrive](across-onedrive-overview.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
