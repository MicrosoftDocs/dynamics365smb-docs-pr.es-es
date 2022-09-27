---
title: Trabajar con documentos entrantes
description: Puede administrar documentos empresariales externos entrantes, como recibos de pago o PDF, administrar tareas de OCR y convertir archivos a documentos y registros electrónicos.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: electronic document, e-invoice, incoming document, OCR, ecommerce, document exchange, import invoice
ms.date: 06/14/2022
ms.author: edupont
ms.openlocfilehash: 8b84e6f832ca5ab7908d7ed00ff7976b073df082
ms.sourcegitcommit: 3acadf94fa34ca57fc137cb2296e644fbabc1a60
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 09/19/2022
ms.locfileid: "9529763"
---
# <a name="incoming-documents"></a>Documentos entrantes

Los documentos empresariales externos pueden llegar a la empresa como datos adjuntos de correo electrónico o como una copia en papel que se digitaliza para archivarla. Este escenario es habitual en las compras, donde dichos archivos de documentos entrantes representan los recibos de pago de gastos o pequeñas compras.

En la página **Documentos entrantes**, puede usar distintas funciones para revisar recibos de gastos, gestionar tareas de OCR y convertir archivos de documentos entrantes, manual o automáticamente en los documentos pertinentes o en líneas de diario. Los archivos externos se pueden adjuntar en cualquier etapa del proceso, incluidos los documentos registrados y los movimientos de proveedor, cliente y de contabilidad resultantes.

## <a name="usage-scenario"></a>Escenario de uso

Puede registrar archivos o copias en papel recibidas de sus socios comerciales en [!INCLUDE[prod_short](includes/prod_short.md)] y crear un registro de documento. Por ejemplo, una factura de compra o venta, una nota de crédito o una línea de diario.

Cargue los archivos recibidos, o use la cámara del dispositivo para tomar una foto, y cree entradas para representar los documentos externos. Opcionalmente, con archivos PDF o de imagen podrá hacer que un servicio externo OCR (Reconocimiento óptico de caracteres) genere documentos electrónicos que se podrán convertir a registros de documento en [!INCLUDE[prod_short](includes/prod_short.md)].

> [!NOTE]
> La característica OCR la proporcionan proveedores externos. Elija un paquete de servicios que sea apropiado para su organización y o el país o la región. Encuentre servicios compatibles con [!INCLUDE[prod_short](includes/prod_short.md)] y detalles sobre las características disponibles en [AppSource.microsoft.com ](https://go.microsoft.com/fwlink/?linkid=2081646).

Por ejemplo, cuando recibes una factura de un proveedor en formato PDF, la puedes enviar al servicio de OCR desde la página **Documentos entrantes**. Alternativamente, algunos proveedores de OCR ofrecen la opción de procesar archivos enviados a una dirección de correo electrónico dedicada, que luego crea automáticamente un registro de documento entrante relacionado. Después de algunos segundos, recibirá de vuelta el archivo desde el servicio OCR como una factura electrónica que se podrá convertir a una factura de compra para el proveedor.

> [!TIP]
> Cree registros de documentos entrantes en [!INCLUDE[prod_short](includes/prod_short.md)] directamente desde los correos electrónicos enviados por los proveedores mediante el complemento de Outlook. Para obtener más información, consulte [Usar Business Central como su bandeja de entrada de empresa en Outlook](work-outlook-addin.md).

## <a name="incoming-document-features"></a>Características de documentos entrantes

El proceso de documento entrante puede constar de las principales actividades siguientes:

* Registrar los documentos externos en [!INCLUDE[prod_short](includes/prod_short.md)] creando líneas en la página **Documentos entrantes** de cualquiera de las siguientes formas:
  * Manualmente, desde un PC o un dispositivo móvil, de una de las siguientes formas:
    * Use el botón **Crear desde archivo**, cargue un archivo y, a continuación, rellene los campos de la página **Documento entrante**.
    * Use el botón **Nuevo**, rellene los campos en la página **Documento entrante** y adjunte el archivo relacionado manualmente.
    * Desde una tableta o un teléfono, utilice el botón **Crear desde la cámara** para crear un registro de documento entrante con la cámara integrada en el dispositivo.
  * De forma automática, recibiendo el documento del servicio OCR como documento electrónico una vez haya cargado o enviado por correo electrónico el PDF o el archivo de imagen relacionado a un servicio OCR. La ficha desplegable **Información financiera** se rellena automáticamente en la página **Documento entrante**.
* Utilice un servicio de OCR externo para convertir documentos PDF o archivos de imagen a documentos electrónicos que se puedan convertir a registros de documento en [!INCLUDE[prod_short](includes/prod_short.md)].
* Crear documentos nuevos o líneas de diario general desde registros de documento entrante manualmente especificando la información a medida que la lee de los archivos de documento entrante.
* Adjuntar archivos de documento entrantes a documentos de compra y de venta en cualquier estado, incluidos los movimientos de proveedor, cliente y contabilidad de la operación de registro.
* Ver registros de documento entrantes y sus adjuntos desde cualquier documento o movimiento de compra y venta, o buscar todos los movimientos de contabilidad sin registros de documento entrantes desde la página **Plan de cuentas**.

> [!NOTE]
> Los archivos adjuntos a tarjetas y documentos de la pestaña **Anexos** no se incluyen en la página **Documentos entrantes**. Para obtener información, consulte [Administrar archivos adjuntos, vínculos y notas en fichas y documentos](ui-how-add-link-to-record.md).

| Para | Vea |
| --- | --- |
| Configure la característica **Documentos entrantes** y configure el servicio OCR. |[Configurar documentos entrantes](across-how-setup-income-documents.md) |
| Cree registros de documentos entrantes manual o automáticamente tomando una foto de un recibo en papel, por ejemplo. |[Crear registros de documento entrantes](across-how-create-income-document-records.md) |
| Use un servicio OCR para convertir archivos PDF y de imágenes en documentos electrónicos que se pueden convertir en facturas de compra en [!INCLUDE[prod_short](includes/prod_short.md)], por ejemplo. Prepare el servicio OCR para evitar errores la próxima vez que procese datos similares. |[Utilizar el servicio OCR para convertir archivos PDF y de imagen en documentos electrónicos](across-how-use-ocr-pdf-images-files.md) |
| Cree o conecte registros de documento entrantes a cualquier documento de compra o venta no registrado y a cualquier movimiento de cliente, proveedor o contabilidad desde el documento o el movimiento. |[Crear registros de documentos entrantes directamente desde documentos y movimientos](across-how-connect-disconnect-income-document-records.md) |
| Desde las páginas **Plan de cuentas** y **Movs. contabilidad**, podrá usar una función de búsqueda para buscar los movimientos de contabilidad para aquellos documentos registrados que no tienen registros de documento entrantes y, a continuación, vincularlos de forma centralizada a registros existentes o crear registros nuevos con archivos de documentos adjuntos. |[Buscar documentos registrados sin registros de documentos entrantes](across-how-find-posted-documents-without-income-document-records.md) |
| Obtenga un mejor resumen estableciendo los registros de documentos entrantes en *Procesado* y retirándolos de la vista por defecto. |[Gestionar varios registros de documento entrantes](across-how-manage-many-income-document-records.md) |

## <a name="see-related-microsoft-training"></a>Consultar la [formación de Microsoft](/training/modules/incoming-documents-dynamics-365-business-central/) relacionada

## <a name="see-also"></a>Consulte también .

[Compras](purchasing-manage-purchasing.md)  
[Edición de documentos registrados](across-edit-posted-document.md)  
[Intercambio de datos electrónicamente](across-data-exchange.md)  
[Integración de Business Central y OneDrive para la Empresa](across-onedrive-overview.md)  
[Usar Business Central como su bandeja de entrada en Outlook](work-outlook-addin.md)  
[Enviar documentos y correos electrónicos](ui-how-send-documents-email.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
