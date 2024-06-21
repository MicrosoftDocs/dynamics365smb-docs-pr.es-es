---
title: Características de asistencia.
description: Este artículo proporciona información sobre los métodos abreviados de teclado y otras funciones de asistencia en Business Central para personas con discapacidad.
author: jswymer
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'accessibility, shortcuts, charts, tooltips, screen reader'
ms.search.form: '9020, 9022, 9026, 9027, 9030, 9000, 9009, 9004, 9005, 9024, 9006, 9007, 9010, 9016, 9017'
ms.date: 06/23/2021
ms.author: jswymer
ms.service: dynamics-365-business-central
ms.reviewer: jswymer
---
# Accesibilidad y métodos abreviados de teclado

Este artículo proporciona información acerca de las características que permiten que [!INCLUDE[prod_short](includes/prod_short.md)] esté disponible con facilidad para personas con discapacidades. [!INCLUDE[prod_short](includes/prod_short.md)] admite las características de accesibilidad siguientes:  

- Métodos abreviados de teclado. Consulte [Métodos abreviados de teclado](keyboard-shortcuts.md).
- Gestos táctiles y con lápiz en tabletas y teléfonos. Consulte [Gestos táctiles y con lápiz](touch-gestures.md).
- Navegación  
- Encabezados  
- Texto alternativo para imágenes y vínculos  
- Compatibilidad con tecnologías de asistencia comunes 
- Acercar o alejar cualquier página
- Sugerencias sobre herramientas en elementos en la interfaz de usuario

[!INCLUDE [about-ui-learn](includes/about-ui-learn.md)]

## <a name="Navigation"></a> Navegación
  
Puede usar diferentes combinaciones de las teclas Tabulador, Mayús y de flechas para moverse entre los elementos de una página. Los elementos incluyen acciones, campos y columnas, partes y otros controles. En general, seleccione <kbd>Tabulación</kbd> o <kbd>Mayúsculas</kbd>+<kbd>Tabulación</kbd> para pasar el siguiente elemento o al anterior.

Cuando se enfoca en un área que contiene acciones, como la barra de navegación de la parte superior del área de trabajo o la barra de acciones en otras páginas, use las teclas de flechas para moverse por las diferentes acciones y grupos. Seleccione <kbd>Enter</kbd> sobre un grupo para abrir sus acciones subyacentes y, a continuación, continúe utilizando las teclas de flecha. Seleccione <kbd>Tabulación</kbd> o <kbd>Mayúsculas</kbd>+<kbd>Tabulación</kbd> para salir de la zona de acción.

Con la orden del tabulador, también puede cambiar entre la página principal del explorador y los cuadros de diálogo que solicitan confirmación, por ejemplo, o la página de inicio de sesión.  

## <a name="Headings"></a> Encabezados en el contenido

El código fuente HTML para el contenido de [!INCLUDE[prod_short](includes/prod_short.md)] utiliza etiquetas para ayudar a los usuarios de tecnología de asistencia a comprender la estructura y el contenido de la página. Por ejemplo, en las páginas de lista, las columnas se definen en las etiquetas TH y los encabezados de columna se establecen con el atributo TITLE dentro de la etiqueta. Los títulos de los elementos, como fichas desplegables, cuadros informativos y campos, se incluyen en las etiquetas de título (H1, H2, H3 y H4).  

## <a name="Images"></a> Imagen y vínculos

Un texto descriptivo para las imágenes se establece con el atributo ALT dentro de la etiqueta IMG. Un texto descriptivo para los hipervínculos se establece con el atributo title dentro de la etiqueta A.  

## <a name="AssistiveTech"></a> Tecnologías de asistencia

[!INCLUDE[prod_short](includes/prod_short.md)] admite las diversas tecnologías de asistencia, como contraste alto, lectores de pantalla y software de reconocimiento de voz. Es posible que algunas tecnologías de asistencia no funcionen bien con determinados elementos de las páginas de [!INCLUDE[prod_short](includes/prod_short.md)].  

## <a name="zoom"></a> Zoom

La mayoría de los navegadores utilizan atajos de teclado estándar para acercar y alejar la página actual. Estos atajos de teclado no son específicos de [!INCLUDE [prod_short](includes/prod_short.md)], pero funcionan al usar [!INCLUDE [prod_short](includes/prod_short.md)] en un navegador. Para obtener una lista de métodos abreviados de teclado compatibles, consulte [Atajos de teclado para acercar y alejar](keyboard-shortcuts.md#zoomshortcuts).

## Sugerencias sobre herramientas

La información sobre herramientas está disponible en la mayoría de los elementos de la interfaz de usuario, como campos y columnas de página, acciones, mosaicos de señales y gráficos. Una sugerencia sobre herramientas proporciona texto adicional que explica un elemento para ayudarle a comprender mejor su propósito. 

Se accede a la información sobre herramientas de diferentes formas, según el cliente (web o móvil) y el dispositivo con el que esté trabajando. Utilice la siguiente tabla a modo de guía. Algunas sugerencias de herramientas pueden leerlas los lectores de pantalla. En este caso, acceda a las sugerencias sobre herramientas como se describe en la tabla, luego use el lector de pantalla para navegar a la sugerencia sobre herramientas, como lo haría con cualquier otro elemento.

#### Acceso a la información sobre herramientas

|Elemento|Acción del mouse para el cliente web|Atajo de teclado para cliente web|Gesto táctil en tableta o teléfono para aplicación móvil|Soporte de lector de pantalla|
|-------|-----------------|------------|--------------------------|---------------------|
|Campos de página y encabezados de columna|Colocar el cursor o hacer clic en el título del campo o el título de la columna|Mueva el foco al campo o encabezado de columna y seleccione <kbd>Alt</kbd>+<kbd>Flecha arriba</kbd>|Tocar en el pie del campo |sí|
|Elementos de gráficos, como una barra, una línea o un sector de tarta|Colocar el cursor sobre el elemento|Mover el foco al elemento, por ejemplo, usando las teclas de flecha|Mantener pulsado el elemento|sí|
|Acciones|Colocar el cursor sobre la acción|ninguno|ninguno |no|
|Azulejos orientativos|Colocar el cursor sobre el mosaico |ninguno|ninguno|no|


<!--
- With a mouse, hover over the element.
- With keyboard, press the Alt+Up Arrow keys.
- On a tablet or phone, tap and hold on the element. To learn about more gestures, see [Touch and Pen Gestures](touch-gestures.md)

-->

## Para obtener más información sobre la accesibilidad

Puede encontrar información adicional acerca de la accesibilidad con los productos de Microsoft y las tecnologías de asistencia en el sitio [Accesibilidad de Microsoft](https://go.microsoft.com/fwlink/?LinkId=262160).

## Consulte también

[Preparación para hacer negocios](ui-get-ready-business.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Preguntas más frecuentes](across-faq.yml)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
