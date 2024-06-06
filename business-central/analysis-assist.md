---
title: Analizar datos en listas con la ayuda de Copilot (versión preliminar)
description: Aprenda a usar Copilot en Business Central para analizar datos.
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.topic: how-to
ms.date: 03/14/2024
ms.custom: bap-template
ms.service: dynamics-365-business-central
ms.search.form: '456, 457, 458, 459, 460, 461, 16, 22, 25, 26, 27, 31, 143, 144, 9300, 9301, 9303, 9304, 9305, 9306, 9307, 9309, 9310, 9311'
---
# <a name="analyze-data-in-lists-with-help-from-copilot-preview"></a>Analizar datos en listas con la ayuda de Copilot (versión preliminar)

[!INCLUDE[preview-banner](includes/preview-banner.md)]

Este artículo explica cómo utilizar la *asistencia de análisis* para ayudarle a analizar datos en páginas de lista.

[!INCLUDE[production-ready-preview-dynamics365](includes/production-ready-preview-dynamics365.md)]

## <a name="about-analysis-assist"></a>Acerca de la asistencia de análisis

La asistencia de análisis es un Copilot para el [modo de análisis](analysis-mode.md) en las páginas de lista en Business Central. El modo de análisis proporciona una forma interactiva y versátil de calcular, resumir y examinar datos. Para analizar datos en el modo de análisis, cree una pestaña *análisis* donde transforma los datos para mostrar las agregaciones y resúmenes deseados. Por ejemplo, organiza campos en filas y columnas, especifica filtros, ordena columnas y gira sobre campos. Con la asistencia de análisis, en lugar de realizar esta tarea manualmente, logra gran parte de lo mismo &mdash;o al menos para empezar&mdash; utilizando palabras. Al expresar la estructura que desea en lenguaje natural, como "ordenar la cantidad de menor a mayor" o "mostrar el costo promedio por categoría", la asistencia de análisis utiliza IA para generar un diseño sugerido en una pestaña de análisis.


<!-- 

 However, the data analysis mode requires some understanding of how to structure fields to meet the desired aggregations and summarizations. It requires you to move fields around to the appropriate areas within analysis mode pane which data rows and columns to display, specify filters, sorting, grouping, pivoting and totals. Analysis assist minimizes these requirments by enabling you to express the desired layout in words. , like "group which data rows and columns to display, specify filters, sorting, grouping, pivoting and totals
--> 
## <a name="prerequisites"></a>Requisitos previos

- La capacidad de asistencia de análisis está activada y se le otorgan permisos para usarla. Esta tarea suele realizarla un administrador. [Más información sobre la configuración de Copilot y las capacidades de IA](enable-ai.md).
- El idioma de visualización en Business Central está configurado en una de las siguientes configuraciones regionales en inglés: en-AU, en-CA, en-GB, en-IE, en-IN, en-NZ, en-PH, en-SG, en-US, en-ZA. [Obtenga más información sobre cómo cambiar el idioma](ui-change-basic-settings.md#language).
- Su entorno de Business Central se encuentra en cualquier país o región excepto Canadá (esta característica aún no está disponible en Canadá).

<!--
> [!NOTE]
> You may notice some list pages that don't include the **Analyze** switch for changing to the analysis mode. The reason is that developers can disable analysis mode on specific pages by using the [AnalysisModeEnabled property](/dynamics365/business-central/dev-itpro/developer/properties/devenv-analysismodeenabled-property) in AL.-->

## <a name="get-started"></a>Introducción

1. Abra la página de la lista que desee analizar.

   Por ejemplo, para trabajar con la página **Productos**, seleccione el icono de la característica ![Lupa que abre la función Dígame.](media/ui-search/search_small.png) icono (<kbd>Alt</kbd>+<kbd>Q</kbd>), introduzca *productos* y, a continuación, elija el vínculo relacionado.

1. Puede comenzar a analizar datos con Copilot directamente desde la página de lista o entrando primero al modo de análisis. Para empezar, siga uno de los pasos siguientes:

    - En la barra de acciones en la parte superior de la página, seleccione ![Muestra el icono del copiloto.](media/copilot-icon.png) **Copilot** > **Analizar lista**.
    - En la barra de acciones en la parte superior de la página, seleccione ![Muestra el icono de ingreso al modo de análisis](media/analysis-mode-icon.png) **Entrar en el modo de análisis**, luego seleccione ![Muestra el icono del copiloto](media/copilot-icon.png) **Copilot** > **Crear nuevo análisis**.

1. En la ventana **Analizar** con Copilot, introduzca una descripción del diseño que desee. Esta descripción se conoce como *solicitud*.

    ![Muestra Copilot asistente de análisis](media/analysis-assist.png)

    > [!TIP]
    > Para obtener ayuda para escribir un mensaje, seleccione ![Muestra el icono de mensaje de visualización](media/prompt-guide-icon.png) **guía rápida** y elija una de las opciones para comenzar. El texto entre corchetes `[ ]` se muestra solo como ejemplo y no se incluye en la ventana de Copilot.

1. Seleccionar **Generar** y luego espere mientras Copilot genera el diseño en la nueva pestaña de análisis.
1. Revise los resultados en la nueva pestaña de análisis.

   > [!NOTE]
   > Si navega fuera de la nueva pestaña de análisis (como ir a otra pestaña o página de análisis) o realiza cambios de diseño en la pestaña (como ordenar columnas o cambiar la configuración en las pestañas **Columnas** y **Filtros de análisis**), la nueva pestaña de análisis se guarda automáticamente y Copilot se cierra.

1. Si desea cambiar el análisis generado, puede realizar uno de los pasos:

   - Para continuar con las instrucciones anteriores, introduzca la información en el cuadro **Agregar más detalles sobre el análisis**, luego seleccione la flecha ![Mostrar la flecha de ajuste](media/analysis-assist-adjust-button.png) **Ajustar**. Copilot recuerda sus instrucciones anteriores y las utiliza para realizar ajustes.

   - Para comenzar desde cero agregando nuevas instrucciones, seleccione ![Muestra el icono de lápiz del mensaje de edición](media/edit-pencil.png) **Editar mensaje:**, agregue los detalles al mensaje y luego seleccione **Generar**.

1. Si desea guardar la ficha de análisis, seleccione **Mantenerlo**. Si no desea guardarlo, seleccione **Descartar**.

## <a name="prompt-tips-and-examples"></a>Sugerencias y ejemplos de mensajes

Crear mensajes efectivos para Copilot es esencial para obtener sugerencias de análisis precisas y relevantes. También hay formas de minimizar el texto que agrega en las indicaciones para hacerlo más rápido al escribir. A continuación se ofrecen algunos consejos y pautas seguidos de algunos ejemplos:

- Sea conciso y evite oraciones largas o múltiples.
- Asegúrese de que los nombres de los campos utilizados en las solicitudes sean algo parecidos a los nombres de los campos reales de la página.
- Utilice un lenguaje natural, expresando la estructura de datos que desea de manera amigable y conversacional.
- Utilice palabras clave, frases y términos comunes utilizados en el análisis de datos, como `group by`, `sum`, `sort by`, etc.
- Si la respuesta inicial no es la que desea, agregue instrucciones de seguimiento o reformule la última instrucción.
- Se aceptan abreviaturas comunes.
- Las mayúsculas y minúsculas no son importantes.

### <a name="examples"></a>Ejemplos

Los siguientes ejemplos de indicaciones utilizan la asistencia de análisis en la lista **Productos**. La página de productos incluye tres campos sumables para el análisis: **Cantidad disponible**, **Coste unitario** y **Precio unitario**.

Mensaje: `Show items by brand and unit of measure`

Este mensaje intenta mostrar los totales de todos los campos sumables, agrupados por marca y campo **Unidad de medida base**. Pero en este caso, "marca" no coincide con ningún nombre de campo, por lo que Copilot probablemente no pueda encontrar un campo coincidente, por lo que le pedirá que reformule el mensaje y vuelva a intentarlo.

Mensaje: `Show items by type and uom`

Este mensaje muestra los totales de todos los campos sumables, el campo **Tipo** y el campo **Unidad de medida base**. Pero en lugar de escribir "unidad de medida", se utiliza la abreviatura `uom`.

Mensaje: `Show total quantity per type per UoM`

Este mensaje crea una tabla dinámica en el campo **Cantidad disponible** por **Unidad de medida base** por **Tipo**.

## <a name="see-also"></a>Consulte también

[Preguntas frecuentes sobre IA responsable para asistencia en análisis](faqs-analysis-assist.md)  
[Análisis de datos ad hoc](reports-adhoc-analysis.md)  
