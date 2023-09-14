---
title: Buscar documentos registrados sin documentos entrantes
description: 'Puede buscar movimientos de contabilidad de los documentos de compra y de venta registrados que no tengan documentos electrónicos de entrada, como las facturas importadas.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'electronic document, e-invoice, incoming document, OCR, ecommerce, document exchange, import invoice'
ms.date: 06/14/2022
ms.author: bholtorf
---
# Buscar documentos registrados sin registros de documentos entrantes

Desde las páginas **Plan de cuentas** y **Movs. contabilidad**, podrá usar una función de búsqueda para buscar los movimientos de contabilidad para aquellos documentos de compra y de venta registrados que no tienen registros de documento entrantes y después vincularlos de forma centralizada a registros existentes o crear registros nuevos con archivos de documentos adjuntos.

## para buscar documentos registrados sin registros de documentos entrantes

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Plan de cuentas** y luego elija el enlace relacionado.
2. Seleccione una línea para una cuenta de contabilidad para la que quiere ver los documentos de ventas y compras registrados de los movimientos de contabilidad sin registros de documentos entrantes y, a continuación, seleccione la acción **Documentos registrados sin documento entrante**.
3. De forma alternativa, elija la acción **Movimientos de activos**.
4. En la página **Movs. contabilidad**, elija la acción **Documentos registrados sin documento entrante**.

La página **Documentos registrados sin documento entrante** se abre con los documentos registrados de compra y de venta sin registros de documento entrantes representados por los movimientos de contabilidad de la cuenta para la que abrió la página. La página puede mostrar un máximo de 1000 líneas. De manera predeterminada, el campo **Filtro de fecha** contiene un filtro que limita las líneas a los movimientos con fechas de registro desde el inicio del periodo contable a la fecha de trabajo.

## Para vincular los documentos encontrados con registros de documento entrantes existentes

1. En la página **Documentos registrados sin documento entrante**, seleccione la línea para un documento registrado que desee conectar con un registro de documento entrante existente y, a continuación, elija la acción **Seleccionar documento entrante**.
2. En la página **Documentos entrantes**, seleccione el registro de documento entrante que desea agregar para conectarlo con el documento registrado encontrado y, a continuación, elija el botón **Aceptar**.
3. En la página **Documentos registrados sin documento entrante**, el registro de documento entrante seleccionado ahora está vinculado con el documento registrado, como se puede ver en el cuadro informativo **Archivos de documento entrante**.

Si no existe un registro de documento entrante correspondiente en la página **Documentos entrantes**, puede crearlo. Para obtener más información, vea [Crear registros de documentos entrantes](across-how-create-income-document-records.md).

## Consultar la [formación de Microsoft](/training/modules/incoming-documents-dynamics-365-business-central/) relacionada

## Consulte también .

[Crear registros de documentos entrantes](across-how-create-income-document-records.md)
[Usar OCR para convertir archivos PDF y de imagen en documentos electrónicos](across-how-use-ocr-pdf-images-files.md)
[Crear registros de documentos entrantes directamente desde documentos y movimientos](across-how-connect-disconnect-income-document-records.md)
[Documentos entrantes](across-income-documents.md)  
[Compras](purchasing-manage-purchasing.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
