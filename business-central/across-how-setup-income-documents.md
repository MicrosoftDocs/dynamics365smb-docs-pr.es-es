---
title: Configurar documentos entrantes | Documentos de Microsoft
description: Use la característica Documentos entrantes para para crear documentos electrónicos, administrar las tareas de OCR, importar facturas y convertir los archivos de imagen.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: electronic document, e-invoice, incoming document, OCR, ecommerce, document exchange, import invoice
ms.date: 12/09/2019
ms.author: sgroespe
ms.openlocfilehash: e67ca1c0b26d7e4a81e53854ca31efc64a366c3f
ms.sourcegitcommit: 3d128a00358668b3fdd105ebf4604ca4e2b6743c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 12/20/2019
ms.locfileid: "2910497"
---
# <a name="set-up-incoming-documents"></a>Configurar documentos entrantes
Si crea líneas de diario general desde registros de documentos entrantes, debe especificar en la página **Configuración de documentos entrantes** qué proceso y plantilla de diario quiere usar.

Si no desea que los usuarios creen facturas o líneas de diario general de los registros de documentos entrantes a menos que los documentos se aprueben primero, debe configurar aprobadores de flujo de trabajo.

Para convertir archivos PDF y de imágenes en documentos electrónicos que pueda convertir, por ejemplo, facturas de compra de [!INCLUDE[d365fin](includes/d365fin_md.md)], primero debe configurar la función OCR y habilitar el servicio.

Al configurar la función Documentos entrantes, puede usar distintas funciones para revisar recibos de gastos, gestionar tareas de OCR y convertir archivos de documentos entrantes, manual o automáticamente en los documentos pertinentes o en líneas de diario. Los archivos externos se pueden adjuntar en cualquier etapa del proceso, incluidos los documentos registrados y los movimientos de proveedor, cliente y de contabilidad resultantes. Para obtener más información, vea [Procesar documentos entrantes](across-process-income-documents.md).

## <a name="to-set-up-the-incoming-documents-feature"></a>Para configurar la característica Documentos entrantes
1. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), introduzca **Configuración de ventas y cobros** y luego elija el enlace relacionado.
2. Rellene los campos según sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-set-up-approvers-of-incoming-document-records"></a>Para configurar aprobadores de registros de documento entrante
Se deben configurar a los aprobadores de documentos entrantes como usuarios de flujo de trabajo de aprobación.

Antes de que puedas crear flujos de trabajo que impliquen pasos de aprobación, tienes que configurar los usuarios del flujo de trabajo implicados en los procesos de aprobación. En la página **Config. usuario aprobación**, también se pueden establecer los límites del importe de tipos específicos de solicitudes y definir aprobadores sustitutos a los que delegar las solicitudes de aprobación cuando el aprobador original está ausente. Para obtener más información, vea [Configurar usuarios de aprobación](across-how-to-set-up-approval-users.md).

## <a name="to-set-up-an-ocr-service"></a>Para configurar un servicio de OCR
1. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), introduzca **Configuración del servicio OCR** y luego elija el enlace relacionado.
2. Rellene los campos según sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!NOTE]  
> Los datos de inicio de sesión se cifran automáticamente.

## <a name="see-also"></a>Consulte también
[Procesar documentos entrantes](across-process-income-documents.md)  
[Documentos entrantes](across-income-documents.md)  
[Compras](purchasing-manage-purchasing.md)  
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
