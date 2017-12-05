---
title: "Proceso para vincular desde registros hacia programas o información externa | Documentos de Microsoft"
description: "Adjuntar un hipervínculo a un documento o un sitio Web a un registro específico, como un documento de cliente."
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: ba26b354d235981bd7291f9ac6402779f554ac7a
ms.openlocfilehash: 8eee2a93a56c33fd5cefb70c475e237166017606
ms.contentlocale: es-es
ms.lasthandoff: 11/10/2017

---
# <a name="adding-links-to-websites-documents-or-programs-on-records"></a>Agregar vínculos a páginas Web, documentos o programas en registros
En un registro específico, como un cliente, documento, o pedido de venta, puede agregar un vínculo a un documento externo, una página Web, o programa. O bien, es posible que desee un vínculo que abra un nuevo mensaje de correo electrónico en blanco a un destinatario específico cuando lo seleccione. La página de fichas para algunos registros, como las fichas de cliente y proveedor, incluyen un campo **Página de inicio**, donde puede especificar una dirección de internet (URL). Para incluir otros en vínculos, puede utilizar el método que se describe en este artículo.

Otro ejemplo podría ser cuando recibe facturas impresas de proveedores. Puede buscarlos y almacenarlos como archivos de .pdf en un sitio Web de SharePoint. A continuación, puede establecer un vínculo desde una factura de compra en [!INCLUDE[d365fin_md](includes/d365fin_md.md)] a la factura correspondiente en SharePoint. o bien cree un vínculo de una ficha de producto a la página correspondiente del catálogo en línea del proveedor.

## <a name="to-add-a-link-on-a-record"></a>Para agregar un vínculo a un registro   

1.  Abra el registro al que desea asociar el vínculo. Si desea agregar el vínculo a una línea específica, por ejemplo, a una línea de diario, selecciónela.  

2.  Seleccione la acción **Vínculos** para abrir la ventana de **Vínculos** que muestra todos los vínculos actuales que están agregadas al registro.

3. Para agregar un nuevo vínculo, elija **+nuevo**.

4.  En el campo **Vincular dirección**, especifique

    -   Para vincular un archivo en el equipo o red, introduzca la ruta de acceso completa y el nombre de archivo, como **C:Mis Documentsfactura1.doc**.
    -   Para vincular la página Web, especifique la dirección de Internet (URL), por ejemplo **www.microsoft.com**.
    -   Para vincular la página Web, especifique la dirección de Internet (URL), por ejemplo **www.microsoft.com**.
    -   Para vincular un programa, escriba una secuencia de caracteres específica para abrir el programa. Por ejemplo, para abrir OneNote con una página específica, escriba **onenote:///C:Mis documentostest.one**. O, para abrir Outlook con un nuevo mensaje de correo electrónico en blanco a un alias específico, escriba **mailto:testalias**.  

5.  Rellene el campo **Descripción** con información sobre el vínculo.  

6.  Haga clic en el botón **Guardar**.  

## <a name="to-delete-a-link-from-a-record"></a>Para eliminar un vínculo de un registro  

Para eliminar un vínculo, en la ventana **Vínculos** , puede seleccionar **…** y después **Eliminar**.

Si elimina un único registro, por ejemplo, una línea de pedido de venta, un pedido de venta o un cliente, se eliminarán todos los vínculos asociados al registro. Sin embargo, si borra los registros utilizando un trabajo por lotes, como el trabajo por lotes **Eliminar pedidos de ventas facturados**, los vínculos se siguen guardando en la base de datos. Para eliminarlos de la base de datos, ejecute el módulo **Eliminar vínculos reg. huérfanos**. Para hacer esto, seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Eliminar vínculos de registros huérfanos** y, a continuación, seleccione el vínculo relacionado.   

<!-- ### To run delete orphaned record links  

1.  Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Data Deletion**, and then choose the related link.  

2.  On the **Data Deletion** page, choose **Tasks**, and then choose **Delete Orphaned Record Links**.  -->

## <a name="see-also"></a>Consulte también  
[Trabajar con [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](ui-work-product.md)  

