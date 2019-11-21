---
title: Agregar archivos adjuntos, vínculos y notas en los registros | Documentos de Microsoft
description: Adjuntar un hipervínculo a un documento o un sitio Web a un registro específico, como un documento de cliente.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/21/2019
ms.author: sgroespe
ms.openlocfilehash: 88e6a04a8e4a992b6a5df3fee87104eba7b5510e
ms.sourcegitcommit: be1e2c49a8434d3f440d5a201508af9c3c8cc87f
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/22/2019
ms.locfileid: "2649793"
---
# <a name="manage-attachments-links-and-notes-on-cards-and-documents"></a>Administrar archivos adjuntos, vínculos y notas en fichas y documentos

En el cuadro informativo en la mayoría de las fichas y documentos, puede adjuntar archivos, agregar vínculos y escribir notas. Para vínculos y notas, también puede hacer esto en la página de lista seleccionando primero la línea relacionada.

Para ver o cambiar cualquiera de estos tipos de información adjunta, primero debe abrir la pestaña **Archivos adjuntos** en el cuadro informativo. El número situado detrás del título de la pestaña indica cuántos archivos adjuntos, vínculos o notas existen para la ficha o documento.

Los archivos adjuntos, vínculos y notas permanecen adjuntos a medida que la ficha o el documento se procesan en otros estados, por ejemplo, desde un pedido de ventas en curso hasta una factura de ventas registrada. Sin embargo, tenga en cuenta que ninguno de los tipos de archivos adjuntos se envían del sistema, por ejemplo, al imprimir o al guardar en un archivo.

## <a name="to-attach-a-file-to-a-purchase-invoice"></a>Para adjuntar un archivo a una factura de compra
Puede adjuntar cualquier tipo de archivo, que contenga texto, imagen o vídeo, a una ficha o documento. Esto es útil, por ejemplo, cuando desea almacenar la factura de un proveedor como un archivo PDF en la factura de compra relacionada en [!INCLUDE[d365fin](includes/d365fin_md.md)].

> [!NOTE]
> Los archivos adjuntos con la función Documentos entrantes no se incluyen en la pestaña **Anexos**. Para obtener más información, consulte [Documentos entrantes](across-income-documents.md).

El procedimiento siguiente se basa en un pedido de venta. Los pasos son parecidos a los de los demás documentos y las fichas admitidos.

1. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Facturas de compra** y luego elija el enlace relacionado.
2. Abra el pedido de venta al que desea adjuntar un archivo.
3. En el cuadro informativo, abra la pestaña **Anexos**.
4. Elija el valor que va detrás del campo **Documentos**, como "0".
5. En la página **Documentos adjuntos**, en el campo **Archivo adjunto**, seleccione el botón **Seleccionar archivo**.
5. Seleccione un archivo de cualquier ubicación y, a continuación, elija el botón **Abrir**.

El archivo se adjunta ahora a la factura de compra.

## <a name="to-add-a-link-from-an-item-card"></a>Para añadir un enlace de una ficha de producto
Puede añadir un enlace de una ficha o un documento a cualquier URL o ruta. Esto es útil, por ejemplo, cuando desea vincular una ficha de producto con el catálogo de producto del proveedor.

El procedimiento siguiente se basa en una ficha de producto. Los pasos son parecidos a los de las demás fichas y documentos admitidos.

1. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Productos** y luego elija el enlace relacionado.
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

1. Elija el icono ![Bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame qué desea hacer"), escriba **Pedidos de venta** y luego elija el enlace relacionado.
2. Seleccione el pedido de venta del en el que desea escribir una nota y luego elija la pestaña **Anexos** en el cuadro informativo.
3. En la sección **Notas**, elija el icono **+**.
4. En el campo **Nota**, escriba cualquier texto, por ejemplo, "Este pedido es urgente.".
5. Elija el botón **Aceptar**.

La nota ahora está adjuntada al pedido de venta.

## <a name="see-also"></a>Consulte también  
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Documentos entrantes](across-income-documents.md)  
[Configurar notificaciones de flujo de trabajo](across-setting-up-workflow-notifications.md)  
