---
title: Empezar a crear diseños
description: 'Obtenga información sobre cómo crear sus propios diseños para personalizar el aspecto de un informe cuando se vea, se imprima o se guarde.'
author: jswymer
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'customized report, document layout, logo, personalize'
ms.search.form: '9650, 9652'
ms.date: 03/23/2022
ms.author: jswymer
---
# <a name="get-started-creating-report-layouts"></a>Empezar a crear diseños de informes

Business Central viene con muchos diseños integrados que puede usar en sus informes. Es posible que se hayan agregado otros diseños como parte de otras extensiones. Pero también es posible crear sus propios informes desde cero o basándose en un diseño existente.

> [!IMPORTANT]
> También puede utilizar los diseños de los informes para añadir contenido a los mensajes de correo electrónico. Por ejemplo, los diseños de informes pueden ahorrar tiempo y ayudar a garantizar la coherencia al reutilizar el mismo contenido cuando se comunica con sus clientes. Para usar diseños de informes personalizados con correo electrónico, el tipo de archivo para el diseño debe ser Word. No puede utilizar el tipo de archivo RDLC. Para más información, vea [Configurar textos y diseños de correo electrónico reutilizables](admin-how-setup-email.md#set-up-reusable-email-texts-and-layouts). 

## <a name="overview"></a>Información general

Al trabajar con diseños de informes, resulta útil pensar en el diseño como un archivo que se importa y se asigna a un informe. Independientemente del tipo de diseño, la forma en que administra los diseños en Business Central es básicamente la misma. Por lo general, trabajará desde la página **Diseños de informe**. La principal diferencia es la forma en que se diseña el diseño, que se realiza utilizando el software de aplicación en el que se construye el diseño, como Word, Excel o SQL Server Report Builder.

Con este concepto en mente. Hay básicamente tres o cuatro tareas implicadas en la configuración de un diseño en un informe:

1. Decidir sobre el tipo de diseño.
2. Exportar una copia de un diseño existente para usar como punto de partida.
3. Realizar cambios en el archivo de diseño en la aplicación adecuada.
4. Agregar el nuevo archivo de diseño al informe.

> [!IMPORTANT]
> No puede modificar o reemplazar un diseño de extensión, que es un diseño que se origina en una extensión. Solo puede modificar o sustituir los diseños definidos por el usuario. En la página **Diseños de informe** puede saber si el diseño es un diseño de extensión o un diseño definido por el usuario mirando a la columna **Extensión**. Un diseño de extensión mostrará información sobre la extensión de origen en la columna. La columna **Extensión** estará vacía para un diseño definido por el usuario.
>
> Para conocer la diferencia entre los diseños de extensión y los diseños definidos por el usuario, consulte [Origen de diseño](ui-manage-report-layouts.md#layout-sources).

## <a name="get-started"></a>Introducción

Dependiendo de cuál sea su situación, las tareas reales variarán. Use la siguiente tabla como ayuda para comenzar.

|¿Qué desea hacer?|Consulte...|
|-----------------------|------|
|Averiguar cuál es el mejor tipo de diseño para mi situación|[Decida qué tipo de diseño desea](#decide)|
|Cree un nuevo diseño para un informe que esté basado en un diseño existente, manteniendo el diseño existente tal cual.|[Crear un nuevo diseño](#create)|
|Hacer cambios en un diseño existente que se utiliza en un informe|[Modificar un diseño](#modify)|
|Tengo una nueva versión de un archivo de diseño para un informe. Quiero reemplazar el archivo de diseño existente.|[Reemplazar un diseño](#replace)|
|Cambiar el diseño actual utilizado por un informe a otro diseño|[Establecer el diseño utilizado por un informe](ui-set-report-layout.md)|
|Cambiar el nombre y la descripción de un diseño|[Cambiar el nombre de un diseño](#rename)|

## <a name="decide-what-type-of-layout-you-want"></a><a name="decide"></a>Decida qué tipo de diseño desea

Lo primero al crear un diseño es decidir qué [tipo de diseño](ui-manage-report-layouts.md#layout-types) desea. Puede elegir Word, Excel o RDLC. El tipo de diseño dependerá de cómo quiera que sea el informe generado. Además, depende de su conocimiento del software de aplicación para crear los diseños, como Word, Excel y SQL Server Report Builder.

<!--
* The process for setting up Word, Excel, and RDLC layouts on reports is the same. The main difference is in the way you modify the layouts. Excel and Word layouts are typically easier to create and modify than RDLC layouts because you use Word and Excel. RDLC report layouts are modified by using SQL Server Report builder, which targets more advanced users.-->

* Los diseños de Excel son, por lo general, los más fáciles de crear y modificar, ya que las funciones para resumir los datos, agregar gráficos y aplicar estilos, son características comunes de Excel.

* No todos los informes y documentos tienen un conjunto de datos optimizado para su uso con un diseño de Excel. Por ejemplo, las agregaciones y los cálculos complejos funcionan mejor con diseños RDLC o Word. Lo mismo ocurre con los documentos.

* Si solo va a realizar cambios de estilo como el tipo de letra, el tamaño y los colores, un diseño de Word también es una buena opción.

* Agregar campos de datos o reordenarlos en Word o RDLC es más avanzado que con Excel.

* Los diseños de Word y RDLC son buenos para usarlos en los informes que finalmente se imprimirán.  

* Los conceptos de diseño generales son parecidos en Word y RDLC. Sin embargo, cada tipo tiene determinadas características de diseño que afectan a la forma en que el informe generado aparece en [!INCLUDE[prod_short](includes/prod_short.md)]. El mismo informe puede tener un aspecto diferente cuando se utiliza el diseño de informe de Word en comparación con el diseño de informe de RDLC.

## <a name="create-a-new-layout"></a><a name="create"></a>Crear un nuevo diseño

Hay dos formas de crear un nuevo diseño a partir de un diseño existente. Una forma es guardar el diseño existente en una copia. La otra forma es exportar el diseño existente.

## [Copiar](#tab/copy)

Copiar es una forma rápida de crear un nuevo diseño que sea igual a un diseño existente. Una vez que tenga la copia, podrá realizar modificaciones exportando el diseño. 

[!INCLUDE[open-report-layouts-page](includes/open-report-layouts-page.md)]
2. Seleccione el diseño del que desea una copia para su nuevo diseño, luego elija la acción **Editar información**.

    Si seleccionó un diseño de extensión, se le preguntará si desea editar una copia. Para continuar, seleccione **Sí**.

    > [!TIP]
    > Como ayuda para buscar el diseño, use el cuadro **Buscar**, el panel **Filtro** y la clasificación de columnas.
3. Cambie el **Nombre del diseño**.
4. Ajuste **Guardar cambios en una copia** en **Activar** y, a continuación, seleccione **Aceptar**

   El nuevo diseño se muestra en la página **Diseños de informe**.
5. Si desea realizar cambios en el nuevo diseño, consulte [Modificar un diseño existente](#modify).

### [Exportar/Importar](#tab/export)

[!INCLUDE[open-report-layouts-page](includes/open-report-layouts-page.md)]
2. Seleccione el diseño del que desea una copia para su nuevo diseño, luego elija la acción **Exportar diseño**.

   El archivo de diseño se descarga en su dispositivo. 

    > [!TIP]
    > Como ayuda para buscar el diseño, use el cuadro **Buscar**, el panel **Filtro** y la clasificación de columnas.

3. Abra el archivo de diseño en la aplicación adecuada, como Word (para un archivo .docx) o Excel (para un archivo .xlsx).

   Para obtener más información, consulte:

   * [Trabajar con diseños de Word](ui-how-add-fields-word-report-layout.md)
   * [Trabajar con diseños de Excel](ui-excel-report-layouts.md)
   * [Trabajar con diseños RDLC](ui-rdlc-report-layouts.md)

   Realice cambios en el archivo y guárdelo.

4. De nuevo en **Diseños de informe**, seleccione la acción **Nuevo diseño**.
5. Rellene los campos a continuación:

   |Campo|Descripción|Obligatoria|
   |-----|-----------|---------|
   |Id. informe|Establecido en el identificador asignado al informe|sí|
   |Nombre del diseño| Escriba un breve nombre descriptivo para el diseño que le ayude a identificarlo fácilmente.|sí|
   |Descripción| Escriba información más detallada sobre el diseño. |no|
   |Opciones de formato|Configure este campo para que coincida con el tipo de diseño, como Word, Excel o RDLC.|sí|

6. Seleccione **Aceptar** y luego realice uno de los siguientes pasos para cargar el archivo de diseño del informe:

   [!INCLUDE[file-upload](includes/file-upload.md)]

   El archivo seleccionado se carga en el diseño y vuelve a la página **Diseños de informes**.

Si desea ver cómo se ve el informe con el nuevo diseño, seleccione el diseño en la lista y luego seleccione **Ejecutar informe**.

---

## <a name="modify-a-layout"></a><a name="modify"></a>Modificar un diseño

Siga estos pasos para modificar un diseño definido por el usuario existente.

[!INCLUDE[open-report-layouts-page](includes/open-report-layouts-page.md)]
2. Seleccione el diseño que desee modificar y elija la acción **Exportar diseño**.

   El archivo de diseño se descarga en su dispositivo. 

   > [!TIP]
   > Como ayuda para buscar el diseño, use el cuadro **Buscar**, el panel **Filtro** y la clasificación de columnas.

3. Abra el archivo de diseño en la aplicación adecuada, como Word (para un archivo .docx) o Excel (para un archivo .xlsx).

   Para obtener más información, consulte:

   * [Trabajar con diseños de Word](ui-how-add-fields-word-report-layout.md)
   * [Trabajar con diseños de Excel](ui-excel-report-layouts.md)
   * [Trabajar con diseños RDLC](ui-rdlc-report-layouts.md)

   Realice cambios en el archivo y guárdelo.

4. De nuevo en la página **Diseños de informe**, seleccione el diseño existente y, a continuación, seleccione la acción **Reemplazar diseño**.
5. Seleccione **Aceptar** > **Elegir** para abrir el explorador de archivos en el dispositivo.
6. Busque y seleccione el archivo de Excel y, a continuación, seleccione **Abrir**.

   El archivo seleccionado se carga en el diseño y vuelve a la página **Diseños de informes**.
7. Si desea ver cómo se ve el informe con el nuevo diseño, seleccione el diseño en la lista y luego seleccione **Ejecutar informe**.

## <a name="replace-a-layout"></a><a name="replace"></a>Reemplazar un diseño

Siga estos pasos para reemplazar el archivo de diseño definido por el usuario existente con un nuevo archivo.

[!INCLUDE[open-report-layouts-page](includes/open-report-layouts-page.md)]
2. Seleccione el diseño existente y luego seleccione la acción **Reemplazar diseño**.
3. Seleccione **Aceptar** > **Elegir** para abrir el explorador de archivos en el dispositivo.
4. Busque y seleccione el archivo de Excel y, a continuación, seleccione **Abrir**.

   El archivo seleccionado se carga en el diseño y vuelve a la página **Diseños de informes**.
5. Si desea ver cómo se ve el informe con el nuevo diseño, seleccione el diseño en la lista y luego seleccione **Ejecutar informe**.

## <a name="rename-a-layout"></a><a name="rename"></a>Cambiar el nombre de un diseño

Siga estos pasos si desea cambiar el nombre y la descripción de un diseño definido por el usuario.

[!INCLUDE[open-report-layouts-page](includes/open-report-layouts-page.md)]
2. Seleccione el diseño cuyo nombre desea cambiar y, a continuación, seleccione la acción **Editar información**.

    > [!TIP]
    > Como ayuda para buscar el diseño, use el cuadro **Buscar**, el panel **Filtro** y la clasificación de columnas.
3. Cambie el **Nombre del diseño** y, a continuación, seleccione **Aceptar**.

## <a name="see-also"></a>Consulte también

[Gestión de diseños de informe](ui-manage-report-layouts.md)  
[Trabajo con diseños de Word](ui-how-add-fields-word-report-layout.md)  
[Trabajar con diseños de Excel](ui-excel-report-layouts.md)  
[Trabajar con informes, trabajos por lotes y XMLports](ui-work-report.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
