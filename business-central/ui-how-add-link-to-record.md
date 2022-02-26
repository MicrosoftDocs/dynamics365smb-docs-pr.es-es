---
title: Agregar archivos adjuntos, vínculos y notas en los registros
description: Adjuntar un hipervínculo a un documento o un sitio Web a un registro específico, como un documento de cliente.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/24/2021
ms.author: edupont
ms.openlocfilehash: 76829c832bfde71d46b2fa2a942aa68db9f5701a
ms.sourcegitcommit: 6ad0a834fc225cc27dfdbee4a83cf06bbbcbc1c9
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/01/2021
ms.locfileid: "7588785"
---
# <a name="manage-attachments-links-and-notes-on-cards-and-documents"></a>Administrar archivos adjuntos, vínculos y notas en fichas y documentos

En el cuadro informativo en la mayoría de las fichas y documentos, puede adjuntar archivos, agregar vínculos y escribir notas. Para vínculos y notas, también puede hacer esto en la página de lista seleccionando primero la línea relacionada.

Para ver o cambiar cualquiera de estos tipos de información adjunta, primero debe abrir la pestaña **Archivos adjuntos** en el cuadro informativo. El número situado detrás del título de la pestaña indica cuántos archivos adjuntos, vínculos o notas existen para la ficha o documento.

Los archivos adjuntos, vínculos y notas permanecen adjuntos a medida que la ficha o el documento se procesan en otros estados, por ejemplo, desde un pedido de ventas en curso hasta una factura de ventas registrada. Sin embargo, ninguno de los tipos de archivos adjuntos se envían del sistema, por ejemplo, al imprimir o al guardar en un archivo.

> [!NOTE]
> Cuando envía y factura parcialmente un pedido de venta o de compra, el archivo adjunto solo se adjuntará a la factura final del pedido. Del mismo modo, cuando factura con la característica Fraccionamientos, el archivo adjunto se adjunta a los movimientos contables del documento, pero no para los movimientos de aplazamiento.
>
> Si elimina un pedido antes de que se facture, el archivo adjunto también se elimina. Cuando factura pedidos de compra mediante la acción Traer albaranes de una factura de compra, el archivo adjunto de los pedidos de compra no se agrega a la factura de compra.

## <a name="to-attach-a-file-to-a-purchase-invoice"></a>Para adjuntar un archivo a una factura de compra
Puede adjuntar cualquier tipo de archivo, que contenga texto, imagen o vídeo, a una ficha o documento. Esto es útil, por ejemplo, cuando desea almacenar la factura de un proveedor como un archivo PDF en la factura de compra relacionada en [!INCLUDE[prod_short](includes/prod_short.md)].

> [!NOTE]
> Los archivos adjuntos con la función Documentos entrantes no se incluyen en la pestaña **Anexos**. Para obtener más información, consulte [Documentos entrantes](across-income-documents.md).

El procedimiento siguiente se basa en una factura de compra. Los pasos son parecidos a los de los demás documentos y las fichas admitidos.

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Facturas compra** y luego elija el enlace relacionado.
2. Abra el pedido de venta al que desea adjuntar un archivo.
3. En el cuadro informativo, abra la pestaña **Anexos**.
4. Elija el valor que va detrás del campo **Documentos**, como "0".
5. En la página **Documentos adjuntos**, en el campo **Archivo adjunto**, seleccione la acción **Seleccionar archivo**.
5. Seleccione un archivo de cualquier ubicación y, a continuación, elija el botón **Abrir**.

El archivo se adjunta ahora a la factura de compra.

## <a name="to-view-an-attached-file"></a>Para ver un archivo adjunto.
1. En el cuadro informativo, abra la pestaña **Anexos**.
2. Elija el valor que va detrás del campo **Documentos**, como "1".
3. En la página **Documentos adjuntos**, seleccione la acción **Vista previa**.
4. Abra el archivo descargado.

## <a name="to-save-a-document-as-a-pdf-attachment"></a>Para guardar un documento como un archivo PDF adjunto
Siempre que necesite guardar un documento como un archivo, puede usar la acción **Adjuntar como PDF** para capturar el contenido actual del documento como un archivo PDF adjunto al cuadro informativo del documento. Esto es útil, por ejemplo, cuando los documentos siguen varios pasos de un proceso, como un proceso de ventas o un flujo de trabajo de aprobación, y desea consultar una copia impresa del paso anterior.

El procedimiento siguiente se basa en un pedido de venta. Los pasos son similares para todos los documentos admitidos.

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Pedidos de venta** y, a continuación, elija el vínculo relacionado.
2. Seleccione un pedido de ventas y después seleccione la acción **Adjuntar como PDF** .

Se agrega un archivo PDF con el contenido actual del pedido de cliente a la pestaña **Archivos adjuntos** del cuadro informativo.

## <a name="to-add-a-link-from-an-item-card"></a>Para añadir un enlace de una ficha de producto
Puede añadir un enlace de una ficha o un documento a cualquier URL. Esto es útil, por ejemplo, cuando desea vincular una ficha de producto con el catálogo de producto del proveedor.

El procedimiento siguiente se basa en una ficha de producto. Los pasos son parecidos a los de las demás fichas y documentos admitidos.

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Productos**, y luego elija el enlace relacionado.
2. Seleccione el producto del que desea agregar un vínculo y luego elija la pestaña **Anexos** en el cuadro informativo.
3. En **Vínculos**, elija el icono **+**.
4. En el campo **Vincular dirección**, especifique el vínculo.

    El enlace debe ser una URL válida de Internet o intranet.

5. En el campo **Descripción**, escriba cualquier información sobre el vínculo.  
6. Elija el botón **Aceptar**.

El vínculo ahora está adjunto a la ficha de producto.  

## <a name="to-write-a-note-on-a-sales-order"></a>Para escribir una nota en un pedido de venta
Puede escribir una nota en un documento o ficha, por ejemplo, para comunicar instrucciones especiales a otros usuarios del documento o ficha. Puede incluir vínculos de archivo y URL en las notas.

> [!NOTE]
> Las notas en la pestaña **Anexos** no están relacionadas con la funcionalidad de notas internas, que se utiliza principalmente para comunicarse entre los usuarios del flujo de trabajo. Para obtener más información, consulte [Configurar notificaciones de flujo de trabajo](across-setting-up-workflow-notifications.md).

El procedimiento siguiente se basa en un pedido de venta. Los pasos son parecidos a los de los demás documentos y las fichas admitidos.

1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Pedidos de venta** y, a continuación, elija el vínculo relacionado.
2. Seleccione el pedido de venta del en el que desea escribir una nota y luego elija la pestaña **Anexos** en el cuadro informativo.
3. En la sección **Notas**, elija el icono **+**.
4. En el campo **Nota**, escriba cualquier texto, por ejemplo, "Este pedido es urgente.".
5. Elija el botón **Aceptar**.

La nota ahora está adjuntada al pedido de venta.

## <a name="see-also"></a>Consulte también  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Documentos entrantes](across-income-documents.md)  
[Configurar notificaciones de flujo de trabajo](across-setting-up-workflow-notifications.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
