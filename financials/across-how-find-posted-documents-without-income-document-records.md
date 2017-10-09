---
title: Buscar documentos sin archivos adjuntos | Documentos de Microsoft
Description: "Puede buscar movimientos de contabilidad de los documentos de compra y de venta registrados que no tengan documentos electrónicos de entrada, como las facturas importadas."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: electronic document, e-invoice, incoming document, OCR, ecommerce, document exchange, import invoice
ms.date: 06/02/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 263146eca72e4c83b4ad6887a84844e7aa15dd87
ms.contentlocale: es-es
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-find-posted-documents-without-incoming-document-records"></a>Procedimiento: Buscar documentos registrados sin registros de documentos entrantes
Desde las ventanas **Plan de cuentas** y **Movs. contabilidad**, podrá usar una función de búsqueda para buscar los movimientos de contabilidad para aquellos documentos de compra y de venta registrados que no tienen registros de documento entrantes y después vincularlos de forma centralizada a registros existentes o crear registros nuevos con archivos de documentos adjuntos.

## <a name="to-find-posted-documents-without-incoming-document-records"></a>para buscar documentos registrados sin registros de documentos entrantes
1. Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Plan de cuentas** y, a continuación, seleccione el vínculo relacionado.
2. Seleccione una línea para una cuenta de contabilidad para la que quiere ver los documentos de ventas y compras registrados de los movimientos de contabilidad sin registros de documentos entrantes y, a continuación, seleccione la acción **Documentos registrados sin documento entrante**.
3. De forma alternativa, elija la acción **Movimientos de activos**.
4. En la ventana **Movs. contabilidad**, elija la acción **Documentos registrados sin documento entrante**.

La ventana **Documentos registrados sin documento entrante** se abre con los documentos registrados de compra y de venta sin registros de documento entrantes representados por los movimientos de contabilidad de la cuenta para la que abrió la ventana. La ventana puede mostrar un máximo de 1000 líneas. De manera predeterminada, el campo **Filtro de fecha** contiene un filtro que limita las líneas a los movimientos con fechas de registro desde el inicio del periodo contable a la fecha de trabajo.

## <a name="to-connect-found-documents-to-existing-incoming-document-records"></a>Para vincular los documentos encontrados con registros de documento entrantes existentes
1. En la ventana **Documentos registrados sin documento entrante**, seleccione la línea para un documento registrado que desee conectar con un registro de documento entrante existente y, a continuación, elija la acción **Seleccionar documento entrante**.
2. En la ventana **Documentos entrantes**, seleccione el registro de documento entrante que desea agregar para conectarlo con el documento registrado encontrado y, a continuación, elija el botón **Aceptar**.
3. En la ventana **Documentos registrados sin documento entrante**, el registro de documento entrante seleccionado ahora está vinculado con el documento registrado, como se puede ver en el cuadro informativo **Archivos de documento entrante**.

Si no existe un registro de documento entrante correspondiente en la ventana **Documentos entrantes**, puede crearlo. Para obtener más información, vea [Procedimiento: Crear registros de documentos entrantes](across-how-create-income-document-records.md).

## <a name="see-also"></a>Consulte también
[Procesar documentos entrantes](across-process-income-documents.md)  
[Documentos entrantes](across-income-documents.md)  
[Compras](purchasing-manage-purchasing.md)  
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

