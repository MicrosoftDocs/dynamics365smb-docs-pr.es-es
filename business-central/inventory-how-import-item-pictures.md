---
title: Importación de muchas imágenes de productos desde un archivo ZIP| Documentos de Microsoft
description: Puede importar varias imágenes de productos de una sola vez. Simplemente asigne a sus archivos de imagen nombres que correspondan a sus números de producto, comprímalos en un archivo zip y, a continuación, utilice la página Importar imágenes de producto para administrar las imágenes de artículo que desea importar.
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: product, image
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: fa859d3e350cedb845df47521ee58ba8d2e4aade
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 03/31/2019
ms.locfileid: "940327"
---
# <a name="import-multiple-item-pictures"></a>Importar varias imágenes de producto
Puede importar varias imágenes de productos de una sola vez. Simplemente asigne a sus archivos de imagen nombres que correspondan a sus números de producto, comprímalos en un archivo ZIP y, a continuación, utilice la página **Importar imágenes de producto** para administrar las imágenes de artículo que desea importar.

Se admiten todos los formatos de archivo habituales.

## <a name="to-name-picture-files-by-the-item-names-and-prepare-the-zip-file"></a>Para asignar nombres a los archivos de imagen por los nombres de los productos y preparar el archivo ZIP
1. En la ubicación donde se almacenan las imágenes de producto, asigne a cada archivo un nombre de acuerdo con el número del producto relacionado. Por ejemplo:

    |Nº producto|Nombre de archivo|
    |-|-|
    |1000|1000.bmp|
    |1001|1001.bmp|
    |1002|1002.bmp|

2. Reúna todos los archivos en un archivo ZIP. Por ejemplo, en el Explorador de Windows, seleccione los archivos y, a continuación, seleccione **Enviar a**, **Carpeta comprimida (zip)**.     

## <a name="to-import-item-pictures"></a>Para importar imágenes de producto
1. Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Configuración de inventario** y luego elija el enlace relacionado.
2. Seleccione la acción **Importar imágenes de producto**.
3. En el campo **Seleccionar un archivo ZIP**, seleccione la carpeta ZIP correspondiente y, a continuación, seleccione el botón **Abrir**.

    Se crea una línea para cada producto e imagen en la página **Importar imágenes de producto**.

    > [!NOTE]
    > Para las fichas de productos que ya tienen una imagen, la casilla **Ya existe la imagen** está seleccionada. Si no desea que se reemplace ninguna imagen existente, desactive la casilla **Reemplazar imágenes**. Si no desea que se reemplacen las imágenes individuales existentes, elimine las líneas en cuestión.

3. Seleccione la acción **Importar imágenes**.

El campo **Estado de importación** se actualiza para mostrar si la importación de imágenes se ha omitido o completado.       

## <a name="see-also"></a>Consulte también
[Registro de productos nuevos](inventory-how-register-new-items.md)  
[Crear numeración](ui-create-number-series.md)  
[Inventario](inventory-manage-inventory.md)  
[Compras](purchasing-manage-purchasing.md)  
[Ccial](sales-manage-sales.md)  
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
