---
title: "Definir cómo se intercambian los datos electrónicamente | Documentos de Microsoft"
description: "Puede usar el proveedor externo de servicios OCR para convertir documentos PDF o archivos de imagen a documentos electrónicos."
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/21/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 6d5fecae58ec05f3cb3eda4ee2a43a131b267c92
ms.contentlocale: es-es
ms.lasthandoff: 03/22/2018

---
# <a name="set-up-data-exchange-definitions"></a>Configurar definiciones de intercambio de datos
Puede configurar [!INCLUDE[d365fin](includes/d365fin_md.md)] para intercambiar datos de tablas específicas con datos de archivos externos, por ejemplo para enviar y recibir documentos electrónicos, importar o exportar datos de banco u otros datos, como nóminas, tipos de cambio de divisa y catálogos de productos. Para obtener más información, vea [Intercambio de datos electrónicamente](across-data-exchange.md).  

Como preparación para crear una definición de intercambio de datos de un archivo de datos o una secuencia, puede utilizar los esquemas XML relacionados para definir los datos a incluir en ficha desplegable **Definiciones de columna**. Consulte el paso 6 de la sección ""Describa el formato de las líneas y las columnas en el archivo". Para obtener más información, consulte [Uso de esquemas XML para preparar las definiciones de intercambio de datos](across-how-to-use-xml-schemas-to-prepare-data-exchange-definitions.md).  

Las definiciones de intercambio de datos normalmente se configuran en la ventana **Definición de intercambio de datos**. Sin embargo, al configurar una definición de intercambio de datos para el servicio de actualización de tipos de cambio de divisa, el proceso se inicia en la ventana **Tarjeta de configuración de actualización de tipo de cambio** simplificada.  

> [!NOTE]  
>  Si el archivo que se va a convertir está en formato XML, el término *"columna"* en este tema se debe interpretar como un *"elemento XML que contiene datos"*.  

Este tema incluye los siguientes procedimientos:  

* Para crear una definición de intercambio de datos  
* Para exportar una definición de intercambio de datos como un archivo XML para que lo utilicen otros usuarios  
* Para importar un archivo XML para una definición de intercambio de datos existente  

## <a name="to-create-a-data-exchange-definition"></a>Para crear una definición de intercambio de datos  
La creación de una definición de intercambio de datos implica dos tareas:  

1. En la ventana **Definición de intercambio de datos**, describe el formato de líneas y columnas del archivo.  
2. En la ventana **Asignación de intercambio de datos**, asigne las columnas en el archivo de datos a los campos de [!INCLUDE[d365fin](includes/d365fin_md.md)].  

     Esto se describe en los procedimientos siguientes:  

#### <a name="to-describe-the-formatting-of-lines-and-columns-in-the-file"></a>Para describir el formato de las líneas y las columnas en el archivo  
1. En el cuadro **Buscar**, escriba **Definiciones de intercambio de datos** y, a continuación, elija el vínculo relacionado.  
2. Seleccione la acción **Nuevo**.  
3. En la ficha desplegable **General**, describa la definición de intercambio de datos y el tipo de archivo de datos; para ello, rellene los campos tal como se describe en la tabla siguiente.  

    |Campo|Definición|  
    |---------------------------------|---------------------------------------|  
    |**Código**|Introduzca un código para identificar la definición de intercambio de datos.|  
    |**Nombre**|Escriba un nombre para la definición de intercambio de datos.|  
    |**Tipo de archivo**|Especifique el tipo de archivo para el que se usa la definición de intercambio de datos. Puede seleccionar tres tipos de archivo:<br /><br /> -   **XML**: cadenas de contenido y marcado por niveles entre etiquetas que indican función.<br />-   **Texto variable**: los registros tienen una longitud variable y están separados por un carácter, como una coma o un punto y coma. También conocido como *archivo delimitado*.<br />-   **Texto fijo**: registros que tienen la misma longitud (se usan caracteres de relleno) y en el que cada registro se incluye en una línea aparte. También conocido como *archivo de ancho fijo*.|  
    |**Escriba**|Especifique para qué tipo de actividad económica se utiliza la definición de intercambio de datos, por ejemplo **Exportación de pagos**.|  
    |**Codeunit de control de datos**|Especifique la unidad de código que transfiere los datos a las tablas de [!INCLUDE[d365fin](includes/d365fin_md.md)] y desde ellas.|  
    |**Codeunit de validación**|Especifique la unidad de código que se usa para validar los datos según las reglas de negocio predefinidas.|  
    |**Codeunit de XMLport de lectura/escritura**|Especifique el codeunit que procesa los datos importados antes de la asignación y los datos exportados después de la asignación.|  
    |**XMLport de lectura/escritura**|Especifique el objeto XMLport a través del que entra un archivo de datos o un servicio importado antes de la asignación y a través del que salen los datos exportados cuando se escriben en un archivo de datos o servicio después de la asignación.|  
    |**Codeunit de control de datos ext.**|Especifique el codeunit que transfiere los datos externos al marco de intercambio de datos y desde él.|  
    |**Codeunit de comentario del usuario**|Especifique la unidad de código que efectúa la limpieza después de la asignación, como marcar las líneas como exportadas y eliminar los registros temporales exportado.|  
    |**Codificación de archivos**|Especifique la codificación del archivo. **Nota:** Este campo solo es pertinente para la importación.|  
    |**Separador de columnas**|Especifique cómo se separan las columnas del archivo de datos, si es de tipo **Variable Text**.|  
    |**Líneas de encabezado**|Especifique cuántas líneas de encabezado hay en el archivo.<br /><br /> De este modo se garantiza que no se importan los datos de encabezado. **Nota:** Este campo solo es pertinente para la importación.|  
    |**Etiqueta de encabezado**|Si hay una línea de cabecera en varias posiciones en el archivo, introduzca el texto de la primera columna en la línea de cabecera.<br /><br /> De este modo se garantiza que no se importan los datos de encabezado. **Nota:** Este campo solo es pertinente para la importación.|  
    |**Etiqueta de pie de página**|Si hay una línea de pie de página en varias posiciones en el archivo, introduzca el texto de la primera columna en la línea de pie de página.<br /><br /> De este modo se garantiza que no se importan los datos de pie de página. **Nota:** Este campo solo es pertinente para la importación.|  

4. En la ficha desplegable **Definiciones de línea**, describa el formato de las líneas del archivo de datos; para ello, rellene los campos tal como se describe en la tabla siguiente.  

    > [!NOTE]  
    >  Para importar extractos de banco, solo se crea una línea para el único formato de archivo de extracto bancario que se desee importar.  
    >   
    >  Para exportar pagos, puede crear una línea para cada tipo de pago que desee exportar. En ese caso, la ficha desplegable **Definiciones de columna** muestra columnas diferentes para cada tipo de pago.  

    |Campo|Descripción|  
    |---------------------------------|---------------------------------------|  
    |**Código**|Introduzca un código para identificar la línea en el archivo.|  
    |**Nombre**|Introduzca un nombre que describa la línea en el archivo.|  
    |**Recuento de columnas**|Especifique cuántas columnas tiene la línea en el archivo de datos. **Nota:** Este campo solo es pertinente para la importación.|  
    |**Etiqueta de línea de datos**|Especifique la posición en el esquema XML relacionado del elemento que representa la entrada principal del archivo de datos. **Nota:** Este campo solo es pertinente para la importación.|  
    |**Espacios de nombres**|Especifique el espacio de nombres que se espera en el archivo para habilitar la validación de espacio de nombres. Puede dejar este campo en blanco si no desea habilitar la validación de espacio de nombres.|  

5. Repita el paso 4 para crear una línea por cada tipo de datos de archivo que desee exportar.  

     Continúe con la descripción del formato de las columnas en el archivo de datos rellenando los campos de la ficha desplegable **Definiciones de línea**, tal como se describe en la tabla siguiente. Puede utilizar el archivo de estructura, como un archivo .XSD, para que archivo de datos llene previamente la ficha desplegable con los elementos correspondientes. Para obtener más información, consulte [Uso de esquemas XML para preparar las definiciones de intercambio de datos](across-how-to-use-xml-schemas-to-prepare-data-exchange-definitions.md).  

6. En la ficha desplegable **Definiciones de columna**, elija **Obtener estructura de archivo**.  
7. En la ventana **Obtener estructura de archivos**, seleccione el archivo de estructura relacionado y, a continuación, seleccione el botón **Aceptar**. Las líneas de la ficha desplegable **Definiciones de columna** se rellenan según la estructura del archivo de datos.  
8. En la ficha desplegable **Definiciones de columna**, edite o rellene los campos tal como se describe en la tabla siguiente.  

    |Campo|Descripción|  
    |---------------------------------|---------------------------------------|  
    |**Nº columna**|Especifique el número que refleja la posición de la columna en relación con la línea en el archivo.<br /><br /> En el caso de archivos XML, especifique el número que refleja el tipo de elemento en el archivo que contiene los datos.|  
    |**Nombre**|Especifique el nombre de la columna.<br /><br /> En el caso de archivos XML, especifique el marcado de los datos que se intercambiarán.|  
    |**Tipo de datos**|Indique si los datos que se van a intercambiar son de tipo **Texto**, **Fecha** o **Decimal**.|  
    |**Formato de datos**|Especifique el formato de los datos, si lo hay. Por ejemplo, **dd-mm-aaaa** si el tipo de datos es **Fecha**. **Nota:** Para exportar, especifique el formato de datos según [!INCLUDE[d365fin](includes/d365fin_md.md)]. Para importar, especifique el formato de datos según .Net Framework. Para obtener más información, consulte [Cadenas de tiempo y fecha estándar](http://go.microsoft.com/fwlink/?LinkID=323466).|  
    |**Referencia cultural de formato de datos**|Especifique la referencia cultural del formato de datos, si la hay. Por ejemplo, **en-US** si el tipo de datos es **Decimal** para garantizar que la coma se utiliza como el separador de .000 según el formato de EE.UU. Para obtener más información, consulte [Cadenas de tiempo y fecha estándar](http://go.microsoft.com/fwlink/?LinkID=323466). **Nota:** Este campo solo es pertinente para la importación.|  
    |**Longitud**|Especifique la longitud de la línea de ancho fijo que contiene la columna si el archivo de datos es de tipo **Fixed Text**.|  
    |**Descripción**|Escriba una descripción de la columna para fines informativos.|  
    |**Ruta acceso**|Especifique la posición del elemento en el esquema XML relacionado.|  
    |**Identificador de signo de negativo**|Especifique el valor que se usa en el archivo de datos para identificar importes negativos en los archivos de datos que no pueden contener signos negativos. A continuación, este identificador se usa para revertir los importes identificados al signo negativo durante la importación. **Nota:** Este campo solo es pertinente para la importación.|  
    |**Constante**|Especifique los datos que desea exportar de esta columna, como, por ejemplo, la información adicional sobre el tipo de pago. **Nota:** Este campo solo es pertinente para la exportación.|  

9. Repita el paso 8 por cada columna o elemento XML del archivo que contiene los datos que desea intercambiar con [!INCLUDE[d365fin](includes/d365fin_md.md)].  

 El paso siguiente en la creación de una definición de intercambio de datos es decidir las columnas o los elementos XML del archivo de datos que se asignarán a los campos de [!INCLUDE[d365fin](includes/d365fin_md.md)].  

> [!NOTE]  
>  La asignación específica depende del objetivo empresarial del archivo de datos que se intercambiará y de las variaciones locales. Incluso el estándar bancario de SEPA presenta variaciones locales. [!INCLUDE[d365fin](includes/d365fin_md.md)] admite importar archivos de extractos bancarios CAMT SEPA originales. Se representa mediante el código de registro de definición de intercambio de datos de **CAMT de SEPA** en la ventana **Definiciones intercambio de datos**. Para obtener información acerca de la asignación de campos específicos de esta ayuda de CAMT de SEPA, consulte [Asignación de campos al importar archivos CAMT de SEPA](across-field-mapping-when-importing-sepa-camt-files.md).  

#### <a name="to-map-columns-in-the-data-file-to-fields-in-included365finincludesd365finmdmd"></a>Para asignar las columnas en el archivo de datos a los campos de [!INCLUDE[d365fin](includes/d365fin_md.md)]  
1. En la ficha desplegable **Definiciones de línea**, seleccione la línea para la que desea asignar columnas a los campos y, a continuación, elija **Asignación de campos**. Se abre la ventana **Asignación de intercambio de datos**.  
2. En la ficha desplegable **General**, especifique la configuración de asignación rellenando los campos tal y como se describe en la tabla siguiente.  

    |Campo|Descripción|  
    |---------------------------------|---------------------------------------|  
    |**Id. tabla**|Especifique la tabla que contiene los campos a los que se intercambian los datos, o desde los que se intercambian, según la asignación.|  
    |**Usar como tabla intermedia**|Especifique si la tabla que seleccionó en el campo **Id. tabla** es una tabla intermedia en la que se almacenan los datos importados antes de asignarlos a la tabla de destino.<br /><br /> Normalmente se usa una tabla intermedia cuando la definición de intercambio de datos se utiliza para importar y para convertir los documentos electrónicos, como facturas de proveedor en facturas de compra en [!INCLUDE[d365fin](includes/d365fin_md.md)]. Para obtener más información, vea [Intercambio de datos electrónicamente](across-data-exchange.md).|  
    |**Nombre**|Escriba un nombre para la configuración de asignación.|  
    |**Codeunit de preasignación**|Especifique la unidad de código que prepara la asignación entre los campos de [!INCLUDE[d365fin](includes/d365fin_md.md)] y los datos externos.|  
    |**Codeunit de asignación**|Especifique el codeunit que se usa para asignar las columnas especificadas o los elementos de datos XML a los campos de [!INCLUDE[d365fin](includes/d365fin_md.md)].|  
    |**Codeunit de postasignación**|Especifique el codeunit que completa la asignación entre los campos de [!INCLUDE[d365fin](includes/d365fin_md.md)] y los datos externos. **Nota**: Al usar la característica de servicio de conversión de datos de banco, el codeunit convierte los datos exportados desde [!INCLUDE[d365fin](includes/d365fin_md.md)] a un formato genérico que está preparado para la exportación. Para importar, la unidad de código convierte los datos externos a un formato listo para importar a [!INCLUDE[d365fin](includes/d365fin_md.md)].|  

3.  En la ficha desplegable **Asignación de campos**, especifique las columnas que se asignan a cada campo en [!INCLUDE[d365fin](includes/d365fin_md.md)]; para ello, rellene los campos tal como se describe en la tabla siguiente.  

    |Campo|Descripción|  
    |---------------------------------|---------------------------------------|  
    |**Nº columna**|Especifique para qué columna del archivo de datos desea definir una asignación.<br /><br /> Solo puede seleccionar las columnas que se representan con líneas en la ficha desplegable **Definiciones de columna** en la ventana **Definición de intercambio de datos**.|  
    |**Id. de campo**|Especificar a qué campo se asigna la columna del campo **Nº Columna** .<br /><br /> Solo puede seleccionar en los campos que existan en la tabla especificada en el campo **Tabla** en la ficha desplegable **General**.|  
    |**Opcional**|Especifique que se omitirá la asignación si el campo está vacío. **Nota**: Si no selecciona esta casilla, se producirá un error de exportación si el campo está vacío. **Nota:** Este campo solo es pertinente para la exportación.|  
    |**Id. de la tabla de destino**|Solo visible cuando se selecciona la casilla **Usar como tabla intermedia**.<br /><br /> Especifique la tabla a la que se asigna el valor del campo **Título columna**, cuando se usa una tabla intermedia para importar datos.|  
    |**Título de la tabla de destino**|Solo visible cuando se selecciona la casilla **Usar como tabla intermedia**.<br /><br /> Especifique el nombre de la tabla en el campo **Id. de la tabla de destino**, que es la tabla a la que se asigna el valor del campo **Título columna**, cuando se usa una tabla intermedia para importar datos.|  
    |**Id. del campo de destino**|Solo visible cuando se selecciona la casilla **Usar como tabla intermedia**.<br /><br /> Especifique el campo de la tabla de destino al que se asigna el valor del campo **Título columna**, cuando se usa una tabla intermedia para importar datos.|  
    |**Título del campo de destino**|Solo visible cuando se selecciona la casilla **Usar como tabla intermedia**.<br /><br /> Especifique el nombre del campo de la tabla de destino al que se asigna el valor del campo **Título columna**, cuando se usa una tabla intermedia para importar datos.|  
    |**Opcional**|Solo visible cuando se selecciona la casilla **Usar como tabla intermedia**.<br /><br /> Especifique si se debe omitir la asignación si el campo está vacío. Si no selecciona esta casilla, se producirá un error de exportación si el campo está vacío.|  

 La definición de intercambio de datos está preparada para habilitarse para los usuarios. Para obtener más información, consulte [Configurar el envío y la recepción de documentos electrónicos](across-how-to-set-up-electronic-document-sending-and-receiving.md), [Configurar transferencias de crédito SEPA](finance-how-to-set-up-sepa-credit-transfer.md), [Configurar domiciliaciones de adeudo directo SEPA](finance-how-to-set-up-sepa-direct-debit.md) y [Realizar pagos con Servicio de conversión de datos del banco o Transferencia de crédito SEPA](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md).  

    Cuando haya creado la definición de intercambio de datos para un archivo de datos específico, podrá exportarla como un archivo XML que se puede usar para habilitar rápidamente la importación del archivo de datos en cuestión. Esto se describe en el procedimiento siguiente:  

### <a name="to-export-a-data-exchange-definition-as-an-xml-file-for-use-by-others"></a>Para exportar una definición de intercambio de datos como un archivo XML para que lo utilicen otros usuarios  
1. En el cuadro **Buscar**, escriba **Definiciones de intercambio de datos** y, a continuación, elija el vínculo relacionado.  
2. Seleccione la definición de intercambio de datos que desea exportar.  
3. Seleccione la acción **Exportar definición de intercambio de datos** .  
4. Guarde el archivo XML que representa la definición del intercambio de datos en una ubicación adecuada.  

    Si ya se ha creado una definición de intercambio de datos, solo tiene que importar el archivo XML al marco de intercambio de datos. Esto se describe en el procedimiento siguiente:  

### <a name="to-import-an-existing-data-exchange-definition"></a>Para importar una definición de intercambio de datos existente  
1. Guarde el archivo XML que representa la definición del intercambio de datos en una ubicación adecuada.  
2. En el cuadro **Buscar**, escriba **Definiciones de intercambio de datos** y, a continuación, elija el vínculo relacionado.  
3. Seleccione la acción **Nuevo**. Se abre la ventana **Definición de intercambio de datos**.  
4. Seleccione la acción **Importar definición de intercambio de datos**.  
5. Seleccione el archivo que ha guardado en el paso 1.  

## <a name="see-also"></a>Consulte también  
[Configuración del intercambio de datos](across-set-up-data-exchange.md)  
[Configurar el envío y la recepción de documentos electrónicos](across-how-to-set-up-electronic-document-sending-and-receiving.md)  
[Configurar la transferencia de crédito de SEPA](finance-how-to-set-up-sepa-credit-transfer.md)  
[Configuración de domiciliaciones de adeudo directo SEPA](finance-how-to-set-up-sepa-direct-debit.md)  
[Realizar pagos con Servicio de conversión de datos del banco o Transferencia de crédito SEPA](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md)  
[Documentos entrantes](across-income-documents.md)  
[Funciones empresariales generales](ui-across-business-areas.md)  

