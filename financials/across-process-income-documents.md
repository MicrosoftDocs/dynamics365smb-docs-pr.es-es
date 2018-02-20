---
title: Procesar documentos entrantes| Documentos de Microsoft
description: Para registrar un documento externo, como un archivo PDF, en Finance and Operations, Business edition, primero cree o complete un registro de documento entrante.
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
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 9534c847352f8b46aac461c672cd3fe70b5e4ca1
ms.contentlocale: es-es
ms.lasthandoff: 01/30/2018

---
# <a name="processing-incoming-documents"></a>Procesar documentos entrantes
Para registrar un documento externo en [!INCLUDE[d365fin](includes/d365fin_md.md)], debe crear o completar un registro de documento entrante. Puede hacerlo manualmente o tomar una foto del documento externo y crear el registro de documento entrante con el archivo de imagen adjunto.

A partir de archivos PDF o de imagen que reciba desde sus socios comerciales podrá hacer que un servicio externo de OCR (reconocimiento óptico de caracteres) genere documentos electrónicos que se podrán convertir a registros de documentos en [!INCLUDE[d365fin](includes/d365fin_md.md)]. Por ejemplo, cuando recibes una factura de un proveedor en formato PDF, la puedes enviar al servicio de OCR desde la ventana **Documentos entrantes**. De forma alternativa, puede enviar el archivo al servicio OCR por correo electrónico. A continuación, cuando vuelve a recibir el documento electrónico, se crea automáticamente un registro de documento entrante relacionado. Después de algunos segundos, recibirá de vuelta el archivo desde el servicio OCR como una factura electrónica que se podrá convertir a una factura de compra para el proveedor.

| Para | Vea |
| --- | --- |
| Cree registros de documentos entrantes manual o automáticamente tomando una foto de un recibo en papel, por ejemplo. |[Crear registros de documento entrantes](across-how-create-income-document-records.md) |
| Use un servicio OCR para convertir archivos PDF y de imágenes en documentos electrónicos que se pueden convertir en facturas de compra en [!INCLUDE[d365fin](includes/d365fin_md.md)], por ejemplo. Prepare el servicio OCR para evitar errores la próxima vez que procese datos similares. |[Utilizar el servicio OCR para convertir archivos PDF y de imagen en documentos electrónicos](across-how-use-ocr-pdf-images-files.md) |
| Cree o conecte registros de documento entrantes a cualquier documento de compra o venta no registrado y a cualquier movimiento de cliente, proveedor o contabilidad desde el documento o el movimiento. |[Crear registros de documentos entrantes directamente desde documentos y movimientos](across-how-connect-disconnect-income-document-records.md) |
| Desde las ventanas **Plan de cuentas** y **Movs. contabilidad**, podrá usar una función de búsqueda para buscar los movimientos de contabilidad para aquellos documentos registrados que no tienen registros de documento entrantes y, a continuación, vincularlos de forma centralizada a registros existentes o crear registros nuevos con archivos de documentos adjuntos. |[Buscar documentos registrados sin registros de documentos entrantes](across-how-find-posted-documents-without-income-document-records.md) |
| Obtenga un mejor resumen configurando los registros de documento entrante que se procesarán para eliminarlos de la vista por defecto. |[Gestionar varios registros de documento entrantes](across-how-manage-many-income-document-records.md) |

## <a name="see-also"></a>Consulte también
[Documentos entrantes](across-income-documents.md)  
[Compras](purchasing-manage-purchasing.md)  
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

