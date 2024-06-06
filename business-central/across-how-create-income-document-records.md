---
title: Crear registros de documento entrantes
description: 'Utilice diferentes funciones en la página Documentos entrantes para revisar recibos de gastos, administrar tareas de OCR, convertir archivos de documentos entrantes y adjuntar archivos externos.'
author: jswymer
ms.topic: how-to
ms-service: dynamics-365-business-central
ms.search.keywords: 'electronic document, e-invoice, incoming document, OCR, ecommerce, document exchange, import invoice'
ms.date: 02/27/2024
ms.author: jswymer
ms.custom: bap-template
ms.reviewer: jswymer
ms.service: dynamics-365-business-central
---
# Crear registros de documento entrantes

En la página **Documentos entrantes**, puede usar distintas funciones para revisar recibos de gastos, gestionar tareas de OCR y convertir archivos de documentos entrantes, manual o automáticamente en los documentos pertinentes o en líneas de diario. Los archivos externos se pueden adjuntar en cualquier etapa del proceso, incluidos los documentos registrados y los movimientos de proveedor, cliente y de contabilidad resultantes.

Para registrar un documento externo en [!INCLUDE[prod_short](includes/prod_short.md)], cree primero un registro de documento entrante. Puede hacer estas tareas manualmente o tomar una foto del documento externo para crear el registro de documento entrante con el archivo de imagen adjunto.

Para poder usar la función **Documentos entrantes**, debe realizar la configuración necesaria. Para obtener más información, vea [Configurar documentos entrantes](across-how-setup-income-documents.md).

## Apruebe o rechace un documento entrante

Si ha configurado la característica **Documentos entrantes** para requerir aprobación para crear documentos, los usuarios con los derechos adecuados deben aprobar los registros antes de que se procesen. Para más información, vea [Configurar aprobadores de registros de documentos entrantes](across-how-setup-income-documents.md#to-set-up-approvers-of-incoming-document-records).

1. Elija el icono ![Bombilla que abre la característica Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Documentos entrantes** y luego elija el enlace relacionado.
2. Seleccione la línea con el documento que desea aprobar o rechazar y, a continuación, elija las acciones **Aprobar** o **Rechazar**.

Si aprueba el registro de documento entrante, se marca la casilla **Lanzado** de la línea de documento entrante. El usuario responsable de crear, por ejemplo, facturas de compra puede procesar el registro.

## Crear un registro de documento entrante tomando una foto

> [!NOTE]  
> El procedimiento siguiente solo se aplica a los clientes de tabletas y teléfonos de [!INCLUDE[prod_short](includes/prod_short.md)].

1. En el centro de roles, seleccione el mosaico **Crear documento entrante desde la cámara** y, a continuación, vaya al paso 4.
2. Alternativamente, elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Documentos entrantes** y luego elija el enlace relacionado.
3. En la página **Documentos entrantes**, elija **Nuevo** y luego **Crear desde la cámara**. La cámara de la tableta o del teléfono se activará.
4. Tome una foto de un documento, como un albarán de compra, que desee procesar como documento entrante y, a continuación, seleccione el botón **Usar**.

    Se crea un nuevo registro de documento entrante con la imagen adjunta.

## Adjuntar una imagen en un registro de documento entrante

> [!NOTE]  
> El procedimiento siguiente solo se aplica a los clientes de tabletas y teléfonos de [!INCLUDE[prod_short](includes/prod_short.md)].

1. Elija el icono ![Bombilla que abre la característica Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Documentos entrantes** y luego elija el enlace relacionado.
2. Abra la ficha de un registro entrante de documento entrante existente.
3. En la página de registro de documentos, elija **Procesar** y, luego, **Adjuntar imagen desde la cámara**. La cámara de la tableta o del teléfono se activará.
4. Tome una foto de un documento, como un albarán de compra, que desee procesar como documento entrante y, a continuación, seleccione el botón **Usar**.

    La imagen se adjunta al registro de documento entrante.

## Crear un registro de documento entrante manualmente

1. Elija el icono ![Bombilla que abre la característica Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Documentos entrantes** y luego elija el enlace relacionado.
2. Elija la acción **Nuevo** y, a continuación, la acción **Crear desde archivo**.  
3. En la página **Insertar archivo**, siga uno de los siguientes pasos y adjunte un archivo que represente el documento entrante:

   [!INCLUDE[file-upload](includes/file-upload.md)]

4. Alternativamente, elija la acción **Nuevo** y luego realice los siguientes pasos:

    1. Para adjuntar un archivo, elija **Proceso** > **Adjuntar archivo**.
    2. En la página **Insertar archivo**, arreste un archivo seleccionado que representa el documento entrante en cuestión o seleccione **pulse aquí para explorar** para encontrar y abrir el archivo.
    3. En la página **Documento entrante**, rellene los campos según sea necesario. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## Consulte también .

[Usar OCR para convertir archivos PDF y de imagen en documentos electrónicos](across-how-use-ocr-pdf-images-files.md)
[Crear registros de documentos entrantes directamente desde documentos y movimientos](across-how-connect-disconnect-income-document-records.md)
[Buscar documentos publicados sin registros de documentos entrantes](across-how-find-posted-documents-without-income-document-records.md)
[Documentos entrantes](across-income-documents.md)  
[Compras](purchasing-manage-purchasing.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
