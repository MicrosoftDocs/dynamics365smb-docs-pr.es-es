---
title: Configurar documentos entrantes | Documentos de Microsoft
description: Use la característica Documentos entrantes para para crear documentos electrónicos, administrar las tareas de OCR, importar facturas y convertir los archivos de imagen.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: electronic document, e-invoice, incoming document, OCR, ecommerce, document exchange, import invoice
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 3a43c32d90a7c27af56ed55a4625b3dc3faf498b
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "4754897"
---
# <a name="set-up-incoming-documents"></a>Configurar documentos entrantes

Si crea líneas de diario general desde registros de documentos entrantes, debe especificar en la página **Configuración de documentos entrantes** qué proceso y plantilla de diario quiere usar.

Si no desea que los usuarios creen facturas o líneas de diario general de los registros de documentos entrantes a menos que los documentos se aprueben primero, debe configurar aprobadores de flujo de trabajo.

Para convertir archivos PDF y de imágenes en documentos electrónicos que pueda convertir, por ejemplo, facturas de compra de [!INCLUDE[prod_short](includes/prod_short.md)], primero debe configurar la función OCR y habilitar el servicio. Elija un paquete de servicios que sea apropiado para su organización y o el país o la región. Alternativamente, puede crear entradas manualmente para representar los documentos externos.  

Al configurar la función Documentos entrantes, puede usar distintas funciones para revisar recibos de gastos, gestionar tareas de OCR y convertir archivos de documentos entrantes, manual o automáticamente en los documentos pertinentes o en líneas de diario. Los archivos externos se pueden adjuntar en cualquier etapa del proceso, incluidos los documentos registrados y los movimientos de proveedor, cliente y de contabilidad resultantes. Para obtener más información, vea [Procesar documentos entrantes](across-process-income-documents.md).

## <a name="to-set-up-the-incoming-documents-feature"></a>Para configurar la característica Documentos entrantes

1. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), introduzca **Configuración de ventas y cobros** y luego elija el enlace relacionado.
2. Rellene los campos según sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

Como parte de la configuración, debe decidir si desea solicitar la aprobación de los documentos entrantes. Para requerir aprobación, debe configurar aprobadores y flujos de trabajo de aprobación. Si su organización no tiene la intención de requerir aprobación, puede omitir la siguiente sección.  

Finalmente, si utiliza un servicio para convertir archivos PDF o de imagen que representan documentos entrantes, debe configurarlo. De lo contrario, también puede omitir esa sección.  

## <a name="to-set-up-approvers-of-incoming-document-records"></a>Para configurar aprobadores de registros de documento entrante

Opcionalmente, configure un proceso de aprobación para los documentos entrantes. Se deben configurar a los aprobadores de documentos entrantes como usuarios de flujo de trabajo de aprobación.

Antes de que puedas crear flujos de trabajo que impliquen pasos de aprobación, tienes que configurar los usuarios del flujo de trabajo implicados en los procesos de aprobación. En la página **Config. usuario aprobación**, también se pueden establecer los límites del importe de tipos específicos de solicitudes y definir aprobadores sustitutos a los que delegar las solicitudes de aprobación cuando el aprobador original está ausente. Para obtener más información, vea [Configurar usuarios de aprobación](across-how-to-set-up-approval-users.md).

## <a name="to-set-up-an-ocr-service"></a>Para configurar un servicio de OCR

1. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), introduzca **Configuración del servicio OCR** y luego elija el enlace relacionado.
2. Rellene los campos según sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!NOTE]  
> Los datos de inicio de sesión se cifran automáticamente.

Para obtener más información, vea [Usar el servicio OCR para convertir archivos PDF y de imagen en documentos electrónicos](across-how-use-ocr-pdf-images-files.md).  

## <a name="see-also"></a>Consulte también

[Procesar documentos entrantes](across-process-income-documents.md)  
[Documentos entrantes](across-income-documents.md)  
[Compras](purchasing-manage-purchasing.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]