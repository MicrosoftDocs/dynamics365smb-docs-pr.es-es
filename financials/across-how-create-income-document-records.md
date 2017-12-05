---
title: Crear registros de documento entrantes | Documentos de Microsoft
description: "Puede crear registros de los documentos entrantes, como facturas electrónicas, y administrar las tareas de OCR, comercio electrónico e intercambio de documentos."
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
ms.sourcegitcommit: ba26b354d235981bd7291f9ac6402779f554ac7a
ms.openlocfilehash: 8642f4d904c9a1e7c46846d790fcb2d0837c4cc2
ms.contentlocale: es-es
ms.lasthandoff: 11/10/2017

---
# <a name="how-to-create-incoming-document-records"></a>Procedimiento: Crear registros de documento entrantes
En la ventana **Documentos entrantes**, puede usar distintas funciones para revisar recibos de gastos, gestionar tareas de OCR y convertir archivos de documentos entrantes, manual o automáticamente en los documentos pertinentes o en líneas de diario. Los archivos externos se pueden adjuntar en cualquier etapa del proceso, incluidos los documentos registrados y los movimientos de proveedor, cliente y de contabilidad resultantes.

Para registrar un documento externo en [!INCLUDE[d365fin](includes/d365fin_md.md)], debe crear o completar un registro de documento entrante. Puede hacerlo manualmente o tomar una foto del documento externo y crear el registro de documento entrante con el archivo de imagen adjunto.

Para poder usar la función Documentos entrantes, debe realizar la configuración necesaria. Para obtener más información, vea [Procedimiento: Configurar documentos entrantes](across-how-setup-income-documents.md).

## <a name="to-approve-or-reject-an-incoming-document"></a>Para aprobar o rechazar un documento entrante
Si desea que los usuarios creen facturas o líneas de diario general a partir de los registros de documento entrante a menos que se aprueben, puede configurar aprobadores que deben aprobar los registros antes de que se puedan procesar.

1. Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Documentos entrantes** y, a continuación, seleccione el vínculo relacionado.
2. Seleccione la línea con el documento que desea aprobar o rechazar y, a continuación, elija las acciones **Aprobar** o **Rechazar**.

Si aprueba el registro de documento entrante, se marca la casilla **Lanzado** de la línea de documento entrante. El usuario responsable de crear, por ejemplo, facturas de compra puede procesar el registro.

## <a name="to-create-an-incoming-document-record-by-taking-a-photo"></a>Para crear un registro de documento entrante tomando una foto
> [!NOTE]  
>   El procedimiento siguiente solo se aplica a los clientes de teléfonos y tabletas de [!INCLUDE[d365fin](includes/d365fin_md.md)].

1. En la barra de aplicaciones, seleccione el mosaico **Crear documento entrante desde la cámara** y, a continuación, vaya al paso 4.
2. O bien, en la barra de aplicaciones, seleccione el botón de opciones, elija **Documentos entrantes** y, a continuación, elija **Todo**.
3. En la ventana **Documentos entrantes**, elija el botón de puntos suspensivos y seleccione **Crear desde la cámara**. La cámara de la tableta o del teléfono se activará.
4. Tome una foto de un documento, como un albarán de compra, que desee procesar como documento entrante y, a continuación, seleccione el botón **Aceptar**.

    Se crea un nuevo registro de documento entrante con la imagen adjunta.

## <a name="to-attach-an-image-to-an-incoming-document-record-by-taking-a-photo"></a>Para adjuntar una imagen en un registro de documento entrante
> [!NOTE]  
>   El procedimiento siguiente solo se aplica a los clientes de teléfonos y tabletas de [!INCLUDE[d365fin](includes/d365fin_md.md)].

1. En la barra de aplicaciones, elija el botón opciones, seleccione **Documentos entrantes** y, a continuación, elija **Todo**.
2. Abra la ficha de un registro entrante de documento entrante existente.
3. En la ventana **Documento entrante**, elija el botón de puntos suspensivos y seleccione **Adjuntar imagen desde la cámara**. La cámara de la tableta o del teléfono se activará.
4. Tome una foto de un documento, como un albarán de compra, que desee procesar como documento entrante y, a continuación, seleccione el botón **Aceptar**.

    La imagen se adjunta al registro de documento entrante.

## <a name="to-create-an-incoming-document-record-manually"></a>Para crear un registro de documento entrante manualmente
1. Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Documentos entrantes** y, a continuación, seleccione el vínculo relacionado.
2. Elija la acción **Crear desde archivo**.  
3. En la ventana **Insertar archivo**, seleccione un archivo y, a continuación, elija **Abrir**. El campo se adjunta automáticamente.
4. De forma alternativa, elija la acción **Nuevo**.
5. Para adjuntar un archivo, elija la acción **Adjuntar archivo**.
6. En la ventana **Insertar archivo**, seleccione el archivo que representa el documento entrante en cuestión y, a continuación, elija el botón **Abrir**.
7. En la ventana **Documento entrante**, rellene los campos según sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="see-also"></a>Consulte también
[Procesar documentos entrantes](across-process-income-documents.md)  
[Documentos entrantes](across-income-documents.md)  
[Compras](purchasing-manage-purchasing.md)  
[Trabajar con [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](ui-work-product.md)

