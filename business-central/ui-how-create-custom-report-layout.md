---
title: Crear y modificar diseños personalizados para informes y documentos
description: 'Obtenga información sobre cómo crear sus propios diseños personalizados para personalizar el aspecto de un informe cuando se vea, se imprima o se guarde.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'customized report, document layout, logo, personalize'
ms.search.form: '9650, 9652'
ms.date: 03/06/2022
ms.author: bholtorf
---
# (Versión heredada) Crear y modificar diseños de informe personalizados

[!INCLUDE[legacy-custom-layouts](includes/legacy-custom-layouts.md)]

De forma predeterminada, los informes tienen un diseño integrado. El diseño del informe puede ser un diseño de informe RDLC (lenguaje de definición de informes del lado del cliente), un diseño de informe de Microsoft Word, o ambos. Y aunque no puede modificar diseños integrados, puede crear diseños personalizados. Un informe puede tener varios diseños personalizados.

> [!NOTE]  
> En [!INCLUDE[prod_short](includes/prod_short.md)], el término “informe” también afecta a documentos externos, como facturas de venta y las confirmaciones de pedido que envía a los clientes como archivos PDF.

Para crear un diseño personalizado, copie un diseño personalizado existente o agregue un nuevo diseño personalizado. Los diseños personalizados a menudo se basan en un diseño integrado. Cuando se agrega un nuevo diseño personalizado, puede elegir agregar un tipo de diseño de informe de RDLC, un tipo de diseño de informe de Word o ambos. El nuevo diseño personalizado se basará en el diseño integrado del informe si hay uno disponible. Si no hay un diseño integrado para el tipo de informe, se crea un nuevo diseño en blanco. Tendrá que modificar y diseñar este diseño en blanco desde cero. Para obtener más información acerca de los diseños de informe de RDLC y de Word, diseños personalizados e integrados y otros temas, consulte [Gestionar diseños de informe](ui-manage-report-layouts.md).  

> [!TIP]
> Use informes financieros para obtener información sobre los datos financieros almacenados en su plan de cuentas. Más información en [Preparar Financial Reporting con categorías de cuentas y datos financieros](bi-how-work-account-schedule.md).

Después de definir sus diseños de informes personalizados, puede seleccionarlos en las páginas Tarjeta de cliente y Tarjeta de proveedor. Los diseños se utilizarán cuando cree documentos para el cliente o proveedor. Más información en [Definir diseños de documentos para clientes y proveedores](ui-define-customer-vendor-document-layouts.md).

También puede utilizar los diseños de los informes personalizados para añadir contenido a los mensajes de correo electrónico. Los diseños de informes pueden ahorrar tiempo y ayudar a garantizar la coherencia al reutilizar el mismo contenido cuando se comunica con sus clientes. Para usar diseños de informes personalizados con correo electrónico, el tipo de archivo para el diseño debe ser Word; no puede usar el tipo de archivo RDLC. Más información en [Configurar textos y diseños de correo electrónico reutilizables](admin-how-setup-email.md#set-up-reusable-email-texts-and-layouts).

## Crear un diseño personalizado

1. Elija el icono ![Bombilla que abre la característica Dígame](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Selección de diseño de informes** y luego elija el enlace relacionado.

    La página **Selección de diseño de informes** muestra todos los informes disponibles en la empresa especificada en el campo **Nombre de la empresa** en la parte superior de la página.
2. En el campo **Nombre de la empresa**, elija la empresa para la que desea crear el diseño del informe.
3. Seleccione la fila para el informe para el cual desee crear el diseño y, a continuación, elija la acción **Diseños personalizados**.  

   La página **Diseños de informe personalizados** aparece con todos los diseños personalizados disponibles para el informe seleccionado.
4. Si desea crear una copia de un diseño personalizado existente, seleccione el diseño personalizado existente en la lista y, a continuación, elija la acción **Copiar**.  

   La copia del diseño personalizado aparece en la página **Diseños de informe personalizados** e incluye las palabras *Copia de* en el campo **Descripción**.
5. Si desea añadir un nuevo diseño personalizado que se base en un diseño integrado, siga estos pasos:  
   1. Seleccione la acción **Nuevo**. Aparece la página **Insertar diseño integrado para un informe** con los campos **Id.** y **Nombre** rellenados automáticamente.
   2. Active la opción **Insertar diseño de Word** para agregar un tipo de diseño de informe de Word personalizado O active la opción **Insertar diseño RDLC** para agregar un tipo de diseño de informe RDLC personalizado.
   4. Elija el botón **Aceptar**.  

    El nuevo diseño personalizado aparece en la página **Diseños de informe personalizados**. Si un diseño nuevo se basa en un diseño integrado, las palabras **Copia de un diseño integrado** aparecen en el campo **Descripción**. Si no había diseño integrado para el informe, el nuevo diseño tendrá las palabras **Nuevo diseño** en el campo **Descripción** para indicar que el diseño personalizado está en blanco.
6. De forma predeterminada, el campo **Nombre de la empresa** está en blanco, y el diseño personalizado estará disponible para informes de todas las empresas. Para que el diseño personalizado esté disponible en una empresa específica solo, elija **Editar** y, a continuación, establezca el campo **Nombre de la empresa** en la empresa que quiera.

Se ha creado el diseño personalizado y puede modificarlo como desee.

> [!TIP]
> Puede exportar los resultados del informe a un archivo de Microsoft Excel para ver el conjunto de datos completo, incluidas todas las columnas, pero sin el diseño. El archivo de Excel puede ayudarle a validar que el informe devuelve los datos esperados o diagnosticar problemas. Para más información, consulte [Analizar datos de informes con Excel](report-analyze-excel.md).

## <a name="ModifyCustomLayout"></a>Modificación de un diseño personalizado

Para modificar el diseño de un informe personalizado, primero debe exportar el diseño del informe como archivo a una ubicación en su equipo o red. Luego, abra el documento exportado y realice los cambios. Cuando haya terminado de realizar los cambios, importe el diseño de informe.

### Modificar un diseño personalizado

1. Exportar un diseño personalizado desde la página **Diseños de informe personalizados**. Si esta página no es ya abierta, busque y abra la página **Selección de diseño de informes**, seleccione el informe que tiene el diseño que quiere modificar y haga clic en la acción **Diseños personalizados**.  
2. En la página **Diseños de informe personalizados**, seleccione el diseño que desea modificar, seleccione la acción **Exportar diseño** y, después, seleccione **Guardar** o **Guardar como** para guardar el documento de diseño del informe en una ubicación del equipo o red.  
3. Abra el documento de diseño de informe que guardó y realice las modificaciones.

   Si está cambiando una plantilla de Word, abra el documento de diseño en Word. Obtenga más información sobre cómo editar informes de Word en [Trabajar con diseños de Word](ui-how-add-fields-word-report-layout.md)<!--the next section [Making Changes to the Report Layout](ui-how-create-custom-report-layout.md#MakeChangesToLayout)-->.

   Los diseños de informe RDLC son más avanzados que plantillas de informe de Word. Para obtener más información acerca de cómo modificar un diseño de informe de RDLC, consulte [Diseñar diseños de informes RDLC](/dynamics-nav/Designing-RDLC-Report-Layouts).

   No olvide guardar los cambios cuando termine.

4. Vuelva a la página **Diseños de informe personalizados**, seleccione la plantilla del informe que se exportó y modificó y después seleccione **Importar diseño**.  

5. En el cuadro de diálogo **Importar**, seleccione **Seleccionar** para buscar y seleccionar el documento de diseño de informe modificado y, a continuación, elija **Abrir**.

> [!IMPORTANT]
> Recuerde importar el documento de diseño de informe que modificó. De lo contrario, el nuevo diseño del informe no estará disponible.

<!--
##  <a name="MakeChangesToLayout"></a> Create and modify custom report layouts

To make general formatting and layout changes, such as changing text font, adding and modifying a table, or removing a data field, just use the basic editing features of Word like you do with any Word document.

If you're designing a Word report layout from scratch or adding new data fields, then start by adding a table that includes rows and columns that will eventually hold the data fields.

> [!TIP]  
> Show the table gridlines so that you see the boundaries of table cells. Remember to hide the gridlines when you're done editing. To show or hide table gridlines, select the table, and then under **Layout** on the **Table** tab, choose **View Gridlines**.

### Embedding fonts in Word layouts for consistency

To ensure that reports always display and print with the intended fonts, wherever users open or print the reports, you can embed the fonts in the Word document. However, embedding fonts can significantly increase the size of the Word files. Learn more about embedding fonts in Word at [Embed fonts in Word, PowerPoint, or Excel](https://support.office.com/article/Embed-fonts-in-Word-PowerPoint-or-Excel-cb3982aa-ea76-4323-b008-86670f222dbc).

###  <a name="RemoveField"></a> Removing label and data fields in Word layouts

 Label and data fields of a report are contained in content controls in Word. The following figure illustrates a content control when it's selected in the Word document.  

 ![Content control for field in Word report layout.](media/nav_wordreportlayouts_contentcontrol.png "NAV_WordReportLayouts_ContentControl")  

 The name of the label or data field name displays in the content control. In the example, the field name is CompanyAddr1.  

### To remove a label or data field  

1. Right-click the field you want to delete, then choose **Remove Content Control**.  

     The content control is removed, but the field name remains as text.  

2. Delete the remaining text as needed.  

### Adding data fields

Adding data fields from a report dataset is more advanced and requires some knowledge of the report dataset. Learn more about adding fields for data, labels, and images at [Add Fields to a Word Report Layout](ui-how-add-fields-word-report-layout.md).  -->

## Consulte también .

[Gestión de diseños de informe](ui-manage-report-layouts.md)  
[Cambiar el diseño de informe actual](ui-how-change-layout-currently-used-report.md)  
[Importar y exportar un diseño de informe o documento personalizado](ui-how-import-and-export-report-layout.md)  
[Trabajar con informes, trabajos por lotes y XMLports](ui-work-report.md)  
[Preparar Financial Reporting con categorías de cuentas y datos financieros](bi-how-work-account-schedule.md)  
[Inteligencia empresarial](bi.md)  
[Trabajar con [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
