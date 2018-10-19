---
title: Copiar y pegar datos
description: "Copie campos y filas de las páginas de Business Central y péguelos en otro lugar."
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: accessibility, shortcuts, keyboarding
ms.date: 10/01/2018
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: e924eeb10e98b81035837ca498ec4f1a7b28bf60
ms.contentlocale: es-es
ms.lasthandoff: 09/28/2018

---

# <a name="copying-and-pasting-in-included365finincludesd365finmdmd"></a>Copiar y pegar en [!INCLUDE[d365fin](includes/d365fin_md.md)]
Puede copiar una o más filas de una lista o un solo campo en una página y luego pegar lo que ha copiado en la misma página, otra página o un documento externo (como Microsoft Excel y el correo electrónico de Outlook). En resumen, para copiar, presione CTRL+C (cmd+C en macOS) en su teclado. Para pegar, presione CTRL+V (cmd+V en macOS).

Hay otros métodos abreviados de teclado para copiar y pegar que le ayudan a ahorrar tiempo al introducir datos. Para obtener más información, consulte [Métodos abreviados de teclado](keyboard-shortcuts.md#CopyRows).

Este artículo responde a preguntas comunes que puede tener acerca de las acciones copiar y pegar.  

## <a name="what-can-i-copy-and-paste"></a>¿Qué puedo copiar y pegar?
-   Copie una o más filas en [!INCLUDE[d365fin](includes/d365fin_md.md)] a la misma lista o en cualquier lista con columnas idénticas.
-   Copie una o más filas en [!INCLUDE[d365fin](includes/d365fin_md.md)] y péguelas en Excel u otras aplicaciones.
-   Copie una o más filas en Excel y péguelas en una lista de [!INCLUDE[d365fin](includes/d365fin_md.md)].
-   Copie el valor de un campo individual en [!INCLUDE[d365fin](includes/d365fin_md.md)] y péguelo en cualquier lugar.

## <a name="how-do-i-copy-rows"></a>¿Cómo copio las filas?
Para copiar una sola fila, selecciónela y presione Ctrl+C.

Si desea copiar más filas, puede:
-   Presionar Ctrl+Clic en otra fila o Mayús+Clic para seleccionar la fila y todas las filas intermedias. Consulte [Métodos abreviados de teclado](keyboard-shortcuts.md#CopyRows) para obtener más combinaciones de mouse y teclado para seleccionar filas.
-   Seleccione ![Mostrar más opciones](media/show-more-options-icon.png "icono Mostrar más opciones") en la primera columna de una fila, elija **Seleccionar más**, seleccione la casilla de verificación junto a cada fila que desea copiar y luego presione Ctrl+C.

## <a name="how-do-i-paste-rows"></a>¿Cómo pego las filas?
Seleccione una fila vacía y presione Crtl+V. Si desea reemplazar las filas existentes, seleccione las filas y presione Crtl+V. En este caso, solo puede pegar el mismo número de filas que seleccionó.

<!-- Rows are pasted directly where your cursor is located. If you paste into an empty line, any existing subsequent lines will be moved after the pasted lines. If you paste into an existing line or lines, this will be overwritten.-->

## <a name="can-i-paste-rows-into-an-outlook-email-or-onenote"></a>¿Puedo pegar filas en un correo electrónico de Outlook o OneNote?
Sí. Se pega como una tabla bien formateada que conserva la sangría, la alineación numérica y el color, tal como se vería en [!INCLUDE[d365fin](includes/d365fin_md.md)].

## <a name="does-copy-and-paste-work-with-tiles"></a>¿Copiar y pegar funciona con mosaicos?
No. La lista debe verse como filas (Vista de lista) para copiarla y pegarla.

## <a name="in-which-lists-can-i-copy-and-paste-rows"></a>¿En qué listas puedo copiar y pegar filas?
Puede copiar filas en cualquier tipo de lista, incluidas hojas de trabajo, cuadros informativos o listas que están incrustadas en una página (como líneas de un pedido de ventas). Sin embargo, para pegar filas, la lista debe ser editable.

En algunas páginas, el diseño de la aplicación puede evitar que pegue filas. Póngase en contacto con su administrador o desarrollador de aplicaciones para cambiar la [propiedad editable](https://docs.microsoft.com/en-us/dynamics365/business-central/dev-itpro/developer/properties/devenv-editable-property) de la página o la [propiedad PasteIsValid](https://docs.microsoft.com/en-us/dynamics365/business-central/dev-itpro/developer/properties/devenv-pasteisvalid-property) de la tabla de origen.

## <a name="on-which-clients-is-copy-and-paste-available"></a>¿En qué clientes está disponible la acción de copiar y pegar?
Copiar y pegar está disponible en el navegador o en la aplicación [!INCLUDE[d365fin](includes/d365fin_md.md)] para Windows 10.

## <a name="what-is-the-maximum-number-of-rows-that-can-be-copied"></a>¿Cuál es el número máximo de filas que se pueden copiar?
Puede copiar tantas filas como desee. Por ejemplo, para copiar las 1000 filas de una página, primero debe desplazarse a la parte inferior de la página y esperar a que aparezcan las filas antes de copiarlas. El número máximo de filas que puede copiar solo está limitado por la memoria de su dispositivo.

## <a name="must-i-have-the-exact-same-number-of-columns-when-pasting-rows"></a>¿Debo tener el mismo número exacto de columnas al pegar las filas?
Sí. Tanto si está copiando desde [!INCLUDE[d365fin](includes/d365fin_md.md)], desde Excel o desde algún otro origen de tabla, las filas que pegue deben tener las columnas coincidentes exactas, ni más ni menos.

## <a name="why-do-i-get-errors-when-pasting-rows"></a>¿Por qué me aparecen errores al pegar filas? 
Al pegar en [!INCLUDE[d365fin](includes/d365fin_md.md)], se comprueba cada fila para asegurarse de que los valores de cada columna son válidos. Si una columna contiene un valor que no es válido, se detiene el pegado y se muestra un mensaje de error. Para evitar esto, asegúrese de que las columnas tengan valores válidos antes de pegarlos.


## <a name="see-also"></a>Consulte también .
[Características de asistencia](ui-accessibility.md)  
[Introducción](product-get-started.md)  
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Preguntas más frecuentes](across-faq.md)  

