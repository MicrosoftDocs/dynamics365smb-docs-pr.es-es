---
title: Trabajar con documentos entrantes| Documentos de Microsoft
description: "Puede administrar documentos empresariales externos entrantes, como recibos de pago o PDF, administrar tareas de OCR y convertir archivos a documentos y registros electrónicos."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: electronic document, e-invoice, incoming document, OCR, ecommerce, document exchange, import invoice
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 33b900f1ac9e295921e7f3d6ea72cc93939d8a1b
ms.openlocfilehash: 989fff07cb0608b8dbf6611a39163fc3cfe31459
ms.contentlocale: es-es
ms.lasthandoff: 11/26/2018

---
# <a name="incoming-documents"></a>Documentos entrantes
Algunas transacciones empresariales no se registran en [!INCLUDE[d365fin](includes/d365fin_md.md)] desde el principio. En su lugar, un documento empresarial externo llega a la empresa como datos adjuntos de correo electrónico o una copia en papel que se digitaliza para archivarla. Esto es habitual en las compras, donde dichos archivos de documentos entrantes representan los recibos de pago de gastos o pequeñas compras.

Desde los archivos PDF o de imagen que representan a los documentos entrantes podrá hacer que un servicio externo del OCR (reconocimiento óptico de caracteres) genere documentos electrónicos que se podrán convertir a registros de documento en [!INCLUDE[d365fin](includes/d365fin_md.md)].

En la página **Documentos entrantes**, puede usar distintas funciones para revisar recibos de gastos, gestionar tareas de OCR y convertir archivos de documentos entrantes, manual o automáticamente en los documentos pertinentes o en líneas de diario. Los archivos externos se pueden adjuntar en cualquier etapa del proceso, incluidos los documentos registrados y los movimientos de proveedor, cliente y de contabilidad resultantes.

El proceso de documento entrante puede constar de las principales actividades siguientes:

* Registrar los documentos externos en [!INCLUDE[d365fin](includes/d365fin_md.md)] creando líneas en la página **Documentos entrantes** de cualquiera de las siguientes formas:
  * Manualmente, usando funciones simples, desde un PC o un dispositivo móvil, de una de las siguientes formas:
    * Use el botón **Crear desde archivo** y, a continuación, rellene los campos en la página **Documento entrante**. El campo se adjunta automáticamente.  
    * Use el botón **Nuevo** y, a continuación, rellene los campos en la página **Documento entrante** y adjunte el archivo relacionado manualmente.
    * Desde una tableta o un teléfono, utilice el botón **Crear desde la cámara** para crear un registro de documento entrante nuevo y, a continuación, envíe la imagen al servicio OCR, por ejemplo.
  * De forma automática, recibiendo el documento del servicio OCR como documento electrónico una vez haya enviado por correo electrónico el PDF o el archivo de imagen relacionado al servicio OCR. La ficha desplegable **Información financiera** se rellena automáticamente en la página **Documento entrante**.
* Utilice el servicio de OCR para convertir documentos PDF o archivos de imagen a documentos electrónicos que se puedan convertir a registros de documento en [!INCLUDE[d365fin](includes/d365fin_md.md)].
* Crear documentos nuevos o líneas de diario general desde registros de documento entrante manualmente especificando la información a medida que la lee de los archivos de documento entrante.
* Adjuntar archivos de documento entrantes a documentos de compra y de venta en cualquier estado, incluidos los movimientos de proveedor, cliente y contabilidad de la operación de registro.
* Ver registros de documento entrantes y sus adjuntos desde cualquier documento o movimiento de compra y venta, o buscar todos los movimientos de contabilidad sin registros de documento entrantes desde la página **Plan de cuentas**.

| Para | Vea |
| --- | --- |
| Configurar la función Documentos entrantes y el servicio OCR. |[Configurar documentos entrantes](across-how-setup-income-documents.md) |
| Crear registros de documentos entrantes, adjuntar archivos, usar OCR para convertir archivos PDF en documentos electrónicos, convertir documentos electrónicos en registros de documentos y auditar registros de documentos entrantes de documentos de compra y venta registrados. |[Procesar documentos entrantes](across-process-income-documents.md) |

## <a name="see-also"></a>Consulte también
[Compras](purchasing-manage-purchasing.md)  
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

