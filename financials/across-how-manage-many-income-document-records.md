---
title: Gestionar varios registros de documento entrantes | Documentos de Microsoft
description: 'Procedimiento: Crear registros de documento entrantes'
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: electronic document, e-invoice, incoming document, OCR, ecommerce, document exchange, import invoice
ms.date: 05/12/2016
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 821efd8c95d05fc5d93c79dd75942f61daa91683
ms.contentlocale: es-es
ms.lasthandoff: 05/04/2017


---
# <a name="how-to-manage-many-incoming-document-records"></a>Procedimiento: Gestionar varios registros de documento entrantes
A medida que crea o procesa registros de documento entrantes, el número de líneas en la ventana **Documentos entrantes** puede aumentar hasta el punto de perder la visión general. Por lo tanto, puede establecer los registros de documento entrantes a Procesado para eliminarlos de la vista por defecto. Cuando selecciona la acción **Mostrar todos**, puede ver tanto los registros procesados como los que están sin procesar.

**Nota**: No puede modificar la información, adjuntar archivos o realizar otros procesos en los registros de documentos entrantes que se hayan establecido en Procesado. Primero deberá establecerlos a Sin procesar.

La casilla de verificación **Procesado** se selecciona automáticamente en los registros de documento entrantes que han sido procesados, pero puede seleccionar o anular la selección de la casilla manualmente. Dependiendo de su proceso empresarial, se podrá procesar un registro de documento entrante cuando un documento relacionado haya sido creado para él o se haya adjuntado un archivo.

**Nota**: Cuando abre la ventana **Documentos entrantes** con la acción **Mis documentos entrantes** en el Área de trabajo, solo se muestran por defecto los registros de documento entrantes sin procesar. En este tema se trata como "la vista por defecto".

## <a name="to-remove-incoming-document-records-from-the-default-view"></a>Para eliminar los registros de documento entrantes de la vista por defecto
1. En la ventana **Documentos entrantes**, seleccione una o más líneas para los registros de documento entrantes que quiera eliminar de la vista por defecto.
2. Seleccione la acción **Establecer en Procesado**.

Los registros de documento entrantes se eliminan de la vista por defecto y la casilla **Procesado** se selecciona en las líneas.

**Nota**: También puede realizar esta acción para el registro individual en la ventana **Ficha de documento entrante**.

## <a name="to-view-all-incoming-document-records"></a>Para ver todos los registros de documento entrantes
1. En la ventana **Documentos entrantes**, seleccione la opción **Mostrar todos**.

Se muestran todos los registros de documento entrantes, incluyendo aquellos que no tienen seleccionada la casilla **Procesado**.

## <a name="to-add-incoming-document-records-to-the-default-view"></a>Para agregar los registros de documento entrantes a la vista por defecto
1. En la ventana **Documentos entrantes**, seleccione la opción **Mostrar todos**.
2. Seleccione una o más líneas para los registros de documento entrantes que desea que aparezcan en la vista por defecto.
3. Seleccione la acción **Establecer en Sin procesar**.  

**Nota**: También puede realizar esta acción para el registro individual en la ventana **Ficha de documento entrante**.

## <a name="see-also"></a>Consulte también
[Procesar documentos entrantes](across-process-income-documents.md)  
[Documentos entrantes](across-income-documents.md)  
[Compras](purchasing-manage-purchasing.md)  
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)](ui-work-product.md)

