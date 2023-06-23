---
title: Configurar documentos entrantes
description: 'Configure la característica Documentos entrantes para para crear documentos electrónicos, administrar las tareas de OCR, importar facturas y convertir los archivos de imagen.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'electronic document, e-invoice, incoming document, OCR, ecommerce, document exchange, import invoice'
ms.date: 06/14/2022
ms.author: edupont
---
# <a name="set-up-incoming-documents" />Configurar documentos entrantes

Si crea líneas de diario general desde registros de documentos entrantes, debe especificar en la página **Configuración de documentos entrantes** qué proceso y plantilla de diario quiere usar.

Al configurar la función **Documentos entrantes**, puede usar distintas funciones para revisar recibos de gastos, gestionar tareas de OCR y convertir archivos de documentos entrantes, manual o automáticamente, en los documentos pertinentes o en líneas de diario. Los archivos externos se pueden adjuntar en cualquier etapa del proceso, incluidos los documentos registrados y los movimientos de proveedor, cliente y de contabilidad resultantes. Para obtener más información, vea [Crear registros de documentos entrantes](across-how-create-income-document-records.md).

## <a name="to-set-up-the-incoming-documents-feature" />Para configurar la característica Documentos entrantes

1. Elija el icono ![Bombilla que abre la característica Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Configuración de documentos entrantes** y luego elija el enlace relacionado.
2. Rellene los campos según sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

Como parte de la configuración, debe decidir si desea solicitar la aprobación de los documentos entrantes. Para requerir aprobación, debe [configurar aprobadores y flujos de trabajo de aprobación](#to-set-up-approvers-of-incoming-document-records). Si su organización no pretende requerir aprobación, puede omitir la siguiente sección.

Finalmente, si utiliza un servicio OCR para convertir archivos PDF o de imagen que representan documentos entrantes, [debe configurarlo](#to-set-up-an-ocr-service). De lo contrario, también puede omitir esa sección.

## <a name="to-set-up-approvers-of-incoming-document-records" />Para configurar aprobadores de registros de documento entrante

Si no desea que los usuarios creen facturas ni líneas de diario general de los registros de documento entrante a menos que los documentos se aprueben primero, configure un proceso de aprobación para los documentos entrantes. Se deben configurar a los aprobadores de documentos entrantes como usuarios de flujo de trabajo de aprobación.

Antes de que puedas crear flujos de trabajo que impliquen pasos de aprobación, tienes que configurar los usuarios del flujo de trabajo implicados en los procesos de aprobación. En la página **Config. usuario aprobación**, también se pueden establecer los límites del importe de tipos específicos de solicitudes y definir aprobadores sustitutos a los que delegar las solicitudes de aprobación cuando el aprobador original está ausente. Para obtener más información, vea [Configurar usuarios de aprobación](across-how-to-set-up-approval-users.md).

## <a name="to-set-up-an-ocr-service" />Para configurar un servicio de OCR

Para convertir archivos de imagen y PDF en documentos electrónicos que puede convertir en facturas, notas de crédito o líneas de diario, configure la función OCR. Alternativamente, puede crear entradas manualmente para representar los documentos externos.

1. Elija el icono ![Bombilla que abre la característica Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Configuración del servicio OCR** y luego elija el enlace relacionado.
2. Rellene los campos según sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!NOTE]  
> Los datos de inicio de sesión se cifran automáticamente.

Para obtener más información, vea [Usar el servicio OCR para convertir archivos PDF y de imagen en documentos electrónicos](across-how-use-ocr-pdf-images-files.md).  

## <a name="see-related-microsoft-trainingtrainingmodulesincoming-documents-dynamics-365-business-central" />Consultar la [formación de Microsoft](/training/modules/incoming-documents-dynamics-365-business-central/) relacionada

## <a name="see-also" />Consulte también .

[Documentos entrantes](across-income-documents.md)  
[Compras](purchasing-manage-purchasing.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
