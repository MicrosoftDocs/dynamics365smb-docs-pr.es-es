---
title: Proceso para vincular desde registros hacia programas o información externa | Documentos de Microsoft
description: Adjuntar un hipervínculo a un documento o un sitio Web a un registro específico, como un documento de cliente.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/12/2019
ms.author: jswymer
ms.openlocfilehash: 781f43daf6482c7e29696dc7a03aa021550cde7d
ms.sourcegitcommit: f2e3b571eab6e01d9f5aa8ef47056b6bd313dcbd
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 06/13/2019
ms.locfileid: "1629762"
---
# <a name="add-links-to-websites-documents-or-programs-on-records"></a>Añadir vínculos a páginas Web, documentos o programas en registros
En un registro específico, como un cliente, documento, o pedido de venta, puede agregar un vínculo a un documento externo, una página Web, o programa. O bien, es posible que desee un vínculo que abra un nuevo mensaje de correo electrónico en blanco a un destinatario específico cuando lo seleccione. La página de fichas para algunos registros, como las fichas de cliente y proveedor, incluyen un campo **Página de inicio**, donde puede especificar una dirección de internet (URL). Para incluir otros en vínculos, puede utilizar el método que se describe en este artículo.  

> [!IMPORTANT]
> Actualmente, esta capacidad solo está disponible en implementaciones locales de [!INCLUDE [prodshort](includes/prodshort.md)] con el cliente Windows de Dynamics NAV heredado.  

Otro ejemplo podría ser cuando recibe facturas impresas de proveedores. Puede buscarlos y almacenarlos como archivos de .pdf en un sitio Web de SharePoint. A continuación, puede establecer un vínculo desde una factura de compra en [!INCLUDE[d365fin_md](includes/d365fin_md.md)] a la factura correspondiente en SharePoint. o bien cree un vínculo de una ficha de producto a la página correspondiente del catálogo en línea del proveedor.

## <a name="to-add-a-link-on-a-record"></a>Para agregar un vínculo a un registro   

1.  Abra el registro al que desea asociar el vínculo. Si desea agregar el vínculo a una línea específica, por ejemplo, a una línea de diario, selecciónela.  

2.  Seleccione la acción **Vínculos** para abrir la página **Vínculos** que muestra todos los vínculos actuales que están agregadas al registro.

3. Para agregar un nuevo vínculo, elija **+nuevo**.

4.  En el campo **Vincular dirección**, especifique

    -   Para vincular un archivo en el equipo o red, introduzca la ruta de acceso completa y el nombre de archivo, como **C:\My Documents\invoice1.doc**.
    -   Para vincular la página Web, especifique la dirección de Internet (URL), por ejemplo **www.microsoft.com**.
    -   Para vincular un programa, escriba una secuencia de caracteres específica para abrir el programa. Por ejemplo, para abrir OneNote con una página específica, escriba **onenote:///C:\My Documents/test.one**. O, para abrir Outlook con un nuevo mensaje de correo electrónico en blanco a un alias específico, escriba **mailto:testalias**.  

5.  Rellene el campo **Descripción** con información sobre el vínculo.  

6.  Haga clic en el botón **Guardar**.  

## <a name="to-delete-a-link-from-a-record"></a>Para eliminar un vínculo de un registro  

Para eliminar un vínculo, en la página **Vínculos** , puede seleccionar **…** y después **Eliminar**.

Si elimina un único registro, por ejemplo, una línea de pedido de venta, un pedido de venta o un cliente, se eliminarán todos los vínculos asociados al registro. Sin embargo, si borra los registros utilizando un trabajo por lotes, como el trabajo por lotes **Eliminar pedidos de ventas facturados**, los vínculos se siguen guardando en la base de datos. Para eliminarlos de la base de datos, ejecute la codeunit **Eliminar vínculos reg. huérfanos**. Para ello, elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Eliminar vínculos reg. huérfanos** y luego elija el enlace relacionado.   

<!-- ### To run delete orphaned record links  

1.  Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Data Deletion**, and then choose the related link.  

2.  On the **Data Deletion** page, choose **Tasks**, and then choose **Delete Orphaned Record Links**.  -->

## <a name="see-also"></a>Consulte también  
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
