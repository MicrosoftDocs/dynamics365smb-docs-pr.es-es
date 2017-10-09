---
title: Configurar documentos entrantes | Documentos de Microsoft
description: "Use la característica Documentos entrantes para para crear documentos electrónicos, administrar las tareas de OCR, importar facturas y convertir los archivos de imagen."
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
ms.openlocfilehash: 69cb1037da2f3873ecb9a3f498ce5fadfeabac1d
ms.contentlocale: es-es
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-set-up-incoming-documents"></a>Procedimiento: Configurar documentos entrantes
Si crea líneas de diario general desde registros de documentos entrantes, debe especificar en la ventana **Configuración de documentos entrantes** qué proceso y plantilla de diario quiere usar.

Si no desea que los usuarios creen facturas o líneas de diario general de los registros de documento entrante a menos que los documentos se aprueben primero, debe configurar a los aprobadores en la ventana **Aprobadores de documentos entrantes**.

Para convertir archivos PDF y de imágenes en documentos electrónicos que pueda convertir, por ejemplo, facturas de compra de [!INCLUDE[d365fin](includes/d365fin_md.md)], primero debe configurar la función OCR y habilitar el servicio.

Al configurar la función Documentos entrantes, puede usar distintas funciones para revisar recibos de gastos, gestionar tareas de OCR y convertir archivos de documentos entrantes, manual o automáticamente en los documentos pertinentes o en líneas de diario. Los archivos externos se pueden adjuntar en cualquier etapa del proceso, incluidos los documentos registrados y los movimientos de proveedor, cliente y de contabilidad resultantes. Para obtener más información, vea [Procesar documentos entrantes](across-process-income-documents.md).

## <a name="to-set-up-the-incoming-documents-feature"></a>Para configurar la característica Documentos entrantes
1. Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Configuración de documentos entrantes** y, a continuación, seleccione el vínculo relacionado.
2. Rellene los campos según sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-set-up-approvers-of-incoming-document-records"></a>Para configurar aprobadores de registros de documento entrante
1. Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Configuración de documentos entrantes** y, a continuación, seleccione el vínculo relacionado.  
2. En la ventana **Configuración de documentos entrantes**, seleccione la opción **Aprobadores**.

    La ventana **Aprobadores de documentos entrantes** muestra todos los usuarios configurados en [!INCLUDE[d365fin](includes/d365fin_md.md)].  
3. Seleccione uno o más usuarios que pueden aprobar un documento entrante para que un documento o una línea de diario relacionado se pueda crear.

Cuando se hayan configurado los aprobadores en la ventana **Aprobadores de documentos entrantes**, solo estos usuarios pueden aprobar un documento entrante si la casilla **Requerir aprobación para crear** de la ventana **Configuración de documentos entrantes** está marcada.

> [!NOTE]  
>   Esta configuración de aprobación no está relacionada con flujos de trabajo de aprobación. Para obtener más información, consulte [Procedimiento: Usar flujos de trabajo de aprobación](across-how-use-approval-workflows.md).

## <a name="to-set-up-an-ocr-service"></a>Para configurar un servicio de OCR
1. Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Configuración del servicio OCR** y, a continuación, seleccione el vínculo relacionado.
2. Rellene los campos según sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-encrypt-your-login-information"></a>Para cifrar la información de inicio de sesión
Se recomienda usar esta función para proteger la información de inicio de sesión que se introduce en la ventana **Configuración del servicio OCR**. Puede cifrar datos en el servidor generando claves de cifrado nuevas o importando claves existentes que se activarán en la instancia del servidor que conecta con la base de datos.

1. En la ventana **Configuración del servicio OCR**, seleccione la acción **Administración del cifrado**.
2. En la ventana **Administración del cifrado de datos**, habilite el cifrado de los datos.

## <a name="see-also"></a>Consulte también
[Procesar documentos entrantes](across-process-income-documents.md)  
[Documentos entrantes](across-income-documents.md)  
[Compras](purchasing-manage-purchasing.md)  
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

