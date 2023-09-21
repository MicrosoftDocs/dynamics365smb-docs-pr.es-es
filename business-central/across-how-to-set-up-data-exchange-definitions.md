---
title: Definir cómo se intercambian los datos electrónicamente
description: 'Defina cómo Business Central intercambia datos con archivos externos como documentos electrónicos, datos bancarios, catálogos de artículos y más.'
author: brentholtorf
ms.topic: conceptual
ms.workload: na
ms.search.keywords: null
ms.search.form: '1210, 1211, 1213, 1214, 1215, 1216, 1217'
ms.date: 11/03/2022
ms.author: bholtorf
---
# <a name="set-up-data-exchange-definitions"></a>Configurar definiciones de intercambio de datos

Puede configurar [!INCLUDE[prod_short](includes/prod_short.md)] para intercambiar datos en tablas específicas con datos en archivos externos. Por ejemplo para enviar y recibir documentos electrónicos, importar y exportar datos bancarios u otros datos, como nóminas y catálogos de artículos. Más información en [Intercambio de datos electrónicamente](across-data-exchange.md).  

Para crear una definición de intercambio de datos de un archivo de datos o una secuencia, puede utilizar los esquemas XML relacionados para definir los datos a incluir en ficha desplegable **Definiciones de columna**. Consulte el paso 6 de la sección [Para describir el formato de las líneas y las columnas en el archivo](across-how-to-set-up-data-exchange-definitions.md#to-describe-the-formatting-of-lines-and-columns-in-the-file). Más información en [Usar esquemas XML para preparar definiciones de intercambio de datos](across-how-to-use-xml-schemas-to-prepare-data-exchange-definitions.md).  

Normalmente, configura las definiciones de intercambio de datos en la página **Definición de intercambio de datos**. Sin embargo, para actualizar los tipos de cambio de moneda, es más rápido utilizar un servicio de tipo de cambio de moneda. Más información en [Actualizar tipos de cambio de divisa](finance-how-update-currencies.md#to-set-up-a-currency-exchange-rate-service).

> [!NOTE]  
> Si el archivo que se va a convertir está en formato XML, el término *"columna"* en este artículo se debe interpretar como un *"elemento XML que contiene datos"*.  

Este artículo incluye los siguientes procedimientos:  

* Crear una definición de intercambio de datos.
* Exportar una definición de intercambio de datos como un archivo XML para que lo utilicen otros usuarios.
* Importar un archivo XML para una definición de intercambio de datos existente.

## <a name="create-a-data-exchange-definition"></a>Crear una definición de intercambio de datos

La creación de una definición de intercambio de datos implica dos tareas:  

1. En la página **Definición de intercambio de datos**, describe el formato de líneas y columnas del archivo. Más información en la sección [Para describir el formato de las líneas y las columnas en el archivo](#formatlinescolumns).  
2. En la página **Asignación de intercambio de datos**, asigne las columnas en el archivo de datos a los campos de [!INCLUDE[prod_short](includes/prod_short.md)]. Más inforamción en la sección [Para asignar columnas en el archivo de datos a los campos de [!INCLUDE[prod_short](includes/prod_short.md)]](#mapfields).  

### <a name="to-describe-the-formatting-of-lines-and-columns-in-the-file"></a><a name=formatlinescolumns></a>Para describir el formato de las líneas y las columnas en el archivo

1. Elija el icono ![Bombilla que abre la característica Dígame 1.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Definiciones de intercambio de datos** y, a continuación, elija el vínculo relacionado.  
2. Seleccione la acción **Nuevo**.  
3. En la ficha desplegable **General**, describa la definición de intercambio de datos y el tipo de archivo de datos; para ello, rellene los campos tal como se describe en la tabla siguiente.  

    |Campo|Definición|  
    |---------------------------------|---------------------------------------|  
    |**Código**|Introduzca un código para identificar la definición de intercambio de datos.|  
    |**Nombre**|Escriba un nombre para la definición de intercambio de datos.|  
    |**Tipo de archivo**|Especifique el tipo de archivo para el que se usa la definición de intercambio de datos. Puede seleccionar cuatro tipos de archivo:<br /><br /> -   **XML**: cadenas de contenido y marcado por niveles entre etiquetas que indican función.<br />-   **Texto variable**: los registros tienen una longitud variable y están separados por un carácter, como una coma o un punto y coma, también denominado *archivo delimitado*.<br />-   **Texto fijo**: registros que tienen la misma longitud (se usan caracteres de relleno) y en el que cada registro se incluye en una línea aparte, también llamado *archivo de ancho fijo*.<br />- **Json**: Cadenas de contenido en JavaScript.|  
    |**Escriba**|Especifique para qué tipo de actividad económica se utiliza la definición de intercambio de datos, por ejemplo **Exportación de pagos**.|  
    |**Codeunit de control de datos**|Especifique la codeunit que transfiere los datos a las tablas de [!INCLUDE[prod_short](includes/prod_short.md)] y desde ellas.|  
    |**Codeunit de validación**|Especifique la codeunit que se usa para validar los datos según las reglas de negocio predefinidas.|  
    |**Codeunit de XMLport de lectura/escritura**|Especifique la codeunit que procesa los datos importados antes de la asignación y los datos exportados después de la asignación.|  
    |**XMLport de lectura/escritura**|Especifique el elemento XMLport a través del cual entra el archivo o el servicio de datos importados antes de que se asigne y desde el que salen los datos exportados cuando un archivo o un servicio de datos se escribe después de su asignación.|  
    |**Codeunit de control de datos ext.**|Especifique la codeunit que transfiere los datos externos al marco de intercambio de datos y desde él.|  
    |**Codeunit de comentario del usuario**|Especifique la codeunit que efectúa la limpieza después de la asignación, como marcar las líneas como exportadas y eliminar los registros temporales exportado.|  
    |**Codificación de archivos**|Especifique la codificación del archivo. **Nota:** Este campo solo es pertinente para la importación.|  
    |**Separador de columnas**|Especifique cómo se separan las columnas del archivo de datos, si es de tipo **Texto variable**.|  
    |**Líneas de encabezado**|Especifique cuántas líneas de encabezado hay en el archivo.<br /><br /> Esta configuración garantiza que no se importan los datos de encabezado. **Nota:** Este campo solo es pertinente para la importación.|  
    |**Etiqueta de encabezado**|Si hay una línea de cabecera en varias posiciones en el archivo, introduzca el texto de la primera columna en la línea de cabecera.<br /><br /> Esta opción garantiza que no se importan los datos de encabezado. **Nota:** Este campo solo es pertinente para la importación.|  
    |**Etiqueta de pie de página**|Si hay una línea de pie de página en varias posiciones en el archivo, introduzca el texto de la primera columna en la línea de pie de página.<br /><br /> Esta opción garantiza que no se importan los datos del pie de página. **Nota:** Este campo solo es pertinente para la importación.|  

   > [!TIP]
   > Para ver qué codeunits utiliza Microsoft en las definiciones existentes en el producto estándar, revise los tres campos **Codeunit** en la cabecera de la página **Asignación de campos** en la ficha desplegable **General**, para cada definición.  

4. En la ficha desplegable **Definiciones de línea**, describa el formato de las líneas del archivo de datos; para ello, rellene los campos tal como se describe en la tabla siguiente.  

    > [!NOTE]  
    > Para importar extractos de banco, solo se crea una línea para el único formato de archivo de extracto bancario que se desee importar.  
    >
    > Para exportar pagos, puede crear una línea para cada tipo de pago que desee exportar. En ese caso, la ficha desplegable **Definiciones de columna** muestra columnas diferentes para cada tipo de pago.  

    |Campo|Descripción|  
    |---------------------------------|---------------------------------------|  
    |**Tipo de línea**|Especifica el tipo de línea del archivo.|  
    |**Código**|Introduzca un código para identificar la línea en el archivo.|  
    |**Nombre**|Introduzca un nombre que describa la línea en el archivo.|  
    |**Recuento de columnas**|Especifique cuántas columnas tiene la línea en el archivo de datos. **Nota:** Este campo solo es pertinente para la importación.|  
    |**Etiqueta de línea de datos**|Especifique la posición en el esquema XML relacionado del elemento que representa la entrada principal del archivo de datos. **Nota:** Este campo solo es pertinente para la importación.|  
    |**Espacios de nombres**|Especifique el espacio de nombres que se espera en el archivo para habilitar la validación de espacio de nombres. Puede dejar este campo en blanco si no desea habilitar la validación de espacio de nombres.|  
    |**Código principal**|Especifique el elemento principal de la línea en el campo **Código** si la configuración de intercambio de datos se realiza en archivos con movimientos principales y secundarios, por ejemplo, la cabecera y las líneas del documento.

5. Repita el paso 4 para crear una línea por cada tipo de datos de archivo que desee exportar.  

     Continúe con la descripción del formato de las columnas en el archivo de datos rellenando los campos de la ficha desplegable **Definiciones de línea**, tal como se describe en la tabla siguiente. Puede utilizar el archivo de estructura, como un archivo .xsd, para que archivo de datos llene previamente la ficha desplegable con los elementos correspondientes. Más información en [Usar esquemas XML para preparar definiciones de intercambio de datos](across-how-to-use-xml-schemas-to-prepare-data-exchange-definitions.md).

6. En la ficha desplegable **Definiciones de columna**, elija la acción **Obtener estructura de archivo**.  
7. En la página **Obtener estructura de archivos**, seleccione el archivo de estructura relacionado y luego elija **Aceptar**. Las líneas de la ficha desplegable **Definiciones de columna** se rellenan según la estructura del archivo de datos.  
8. En la ficha desplegable **Definiciones de columna**, edite o rellene los campos tal como se describe en la tabla siguiente.  

    |Campo|Descripción|  
    |---------------------------------|---------------------------------------|  
    |**Nº columna**|Especifique el número que refleja la posición de la columna en relación con la línea en el archivo.<br /><br /> En el caso de archivos XML, especifique el número que refleja el tipo de elemento en el archivo que contiene los datos.|  
    |**Nombre**|Especifique el nombre de la columna.<br /><br /> En el caso de archivos XML, especifique el marcado de los datos que se intercambiarán.|  
    |**Tipo de datos**|Indique si los datos que se van a intercambiar son de tipo **Texto**, **Fecha** o **Decimal**.|  
    |**Formato de datos**|Especifique el formato de los datos, si lo hay. Por ejemplo, **dd-mm-aaaa** si el tipo de datos es **Fecha**. **Nota:** Para exportar, especifique el formato de datos según [!INCLUDE[prod_short](includes/prod_short.md)]. Para importar, especifique el formato de datos según .Net Framework. Más información en [Cadenas de tiempo y fecha estándar](/dotnet/standard/base-types/standard-date-and-time-format-strings).|  
    |**Referencia cultural de formato de datos**|Especifique el formato de datos regionales, si lo hay. Por ejemplo, **en-US** si el tipo de datos es **Decimal** para garantizar que la coma se utiliza como el separador de .000 según el formato de EE.UU. Más información en [Cadenas de tiempo y fecha estándar](/dotnet/standard/base-types/standard-date-and-time-format-strings). **Nota:** Este campo solo es pertinente para la importación.|  
    |**Longitud**|Especifique la longitud de la línea de ancho fijo que contiene la columna si el archivo de datos es de tipo **Fixed Text**.|  
    |**Descripción**|Especifica una descripción de la columna, para fines informativos.|  
    |**Ruta acceso**|Especifique la posición del elemento en el esquema XML relacionado.|  
    |**Identificador de signo de negativo**|Especifique el valor que se usa en el archivo de datos para identificar importes negativos en los archivos de datos que no pueden contener signos negativos. A continuación, este identificador se usa para revertir los importes identificados al signo negativo durante la importación. **Nota:** Este campo solo es pertinente para la importación.|  
    |**Constante**|Especifique los datos que desea exportar de esta columna, como, por ejemplo, la información adicional sobre el tipo de pago. **Nota:** Este campo solo es pertinente para la exportación.|  
    |**Relleno de datos requerido**|Especifica que los datos deben incluir espaciado de texto.|  
    |**Carácter de almohadilla**|Especifique el carácter de relleno de texto.|  
    |**Justificación**|Especifica si la justificación de la columna está a la izquierda o a la derecha.|  

9. Repita el paso 8 por cada columna o elemento XML del archivo que contiene los datos que desea intercambiar con [!INCLUDE[prod_short](includes/prod_short.md)].  

El paso siguiente en la creación de una definición de intercambio de datos es decidir las columnas o los elementos XML del archivo de datos que se asignarán a los campos de [!INCLUDE[prod_short](includes/prod_short.md)].  

> [!NOTE]  
> La asignación específica depende del objetivo empresarial del archivo de datos que se intercambiará y de las variaciones locales. Incluso el estándar bancario de SEPA presenta variaciones locales. [!INCLUDE[prod_short](includes/prod_short.md)] admite importar archivos de extractos bancarios CAMT SEPA originales. Se representa mediante el código de registro de definición de intercambio de datos de **CAMT de SEPA** en la página **Definiciones intercambio de datos**. Para obtener información acerca de la asignación de campos específicos de esta ayuda de CAMT de SEPA, consulte [Asignación de campos al importar archivos CAMT de SEPA](across-field-mapping-when-importing-sepa-camt-files.md).  

### <a name="to-map-columns-in-the-data-file-to-fields-in-"></a><a name=mapfields></a>Para asignar las columnas en el archivo de datos a los campos de [!INCLUDE[prod_short](includes/prod_short.md)]

> [!TIP]
> A veces, los valores en los campos que desea asignar son diferentes. Por ejemplo, en una aplicación comercial, el código de idioma para Estados Unidos es "U.S.", pero en la otra es "US". Eso significa que debe transformar el valor cuando intercambia datos. Esto sucede por de las reglas de transformación que define para los campos. Obtenga más información en [Reglas de transformación](across-how-to-set-up-data-exchange-definitions.md#transformation-rules).

A partir del segundo lanzamiento de versiones de 2022, también puede agrupar por cualquier campo, usar el índice clave para ordenar los resultados y los nuevos tipos de transformación **Redondeo** y **Búsqueda de campo**.

1. En la ficha desplegable **Definiciones de línea**, seleccione la línea para la que desea asignar columnas a los campos y luego elija **Asignación de campos**. Se abre la página **Asignación de intercambio de datos**.  
2. En la ficha desplegable **General**, especifique la configuración de asignación rellenando los campos tal y como se describe en la tabla siguiente.  

    |Campo|Descripción|  
    |---------------------------------|---------------------------------------|  
    |**Id. tabla**|Especifique la tabla que contiene los campos a los que se intercambian los datos, o desde los que se intercambian, según la asignación.|  
    |**Usar como tabla intermedia**|Especifique si la tabla que seleccionó en el campo **Id. tabla** es una tabla intermedia en la que se almacenan los datos importados antes de asignarlos a la tabla de destino.<br /><br /> Normalmente se usa una tabla intermedia cuando la definición de intercambio de datos se utiliza para importar y para convertir los documentos electrónicos, como facturas de proveedor en facturas de compra en [!INCLUDE[prod_short](includes/prod_short.md)]. Más información en [Intercambio de datos electrónicamente](across-data-exchange.md).|  
    |**Nombre**|Escriba un nombre para la configuración de asignación.|  
    |**Índice de la clave**|Especifique el índice de clave para ordenar los registros de origen antes de la exportación.|
    |**Codeunit de preasignación**|Especifique la codeunit que prepara la asignación entre los campos de [!INCLUDE[prod_short](includes/prod_short.md)] y los datos externos.|  
    |**Codeunit de asignación**|Especifique la codeunit que se usa para asignar las columnas especificadas o los elementos de datos XML a los campos de [!INCLUDE[prod_short](includes/prod_short.md)].|  
    |**Codeunit de postasignación**|Especifique la codeunit que completa la asignación entre los campos de [!INCLUDE[prod_short](includes/prod_short.md)] y los datos externos. **Nota**: Al usar la característica extensión AMC Banking 365 Fundamentals, la codeunit convierte los datos exportados desde [!INCLUDE[prod_short](includes/prod_short.md)] a un formato genérico que está preparado para la exportación. Para importar, la codeunit convierte los datos externos a un formato listo para importar a [!INCLUDE[prod_short](includes/prod_short.md)].|
3. En la ficha desplegable **Mapeo de campos**, especifique qué columnas se asignan a qué campos en [!INCLUDE[prod_short](includes/prod_short.md)] rellenando los campos como se describe en las siguientes tablas, dependiendo de si el campo **Usar como tabla intermedia** estaba habilitado o no.  
   * Con el control de alternancia **Usar como tabla intermedia** desactivado:

     |Campo|Descripción|  
     |--------------------------------- |---------------------------------------|  
     |**Nº columna**|Especifique para qué columna del archivo de datos desea definir una asignación.<br /><br /> Solo puede seleccionar las columnas que se representan con líneas en la ficha desplegable **Definiciones de columna** en la página **Definición de intercambio de datos**.|
     |**Título de columna**|Especifica el título de la columna en el archivo externo que se asigna al campo que se encuentra en el campo **Id. de la tabla de destino**, cuando se usa una tabla intermedia para importar datos.|
     |**Id. de campo**|Especificar a qué campo se asigna la columna del campo **Nº Columna** .<br /><br /> Solo puede seleccionar en los campos que existan en la tabla especificada en el campo **Id. de tabla** en la ficha desplegable **General**.|
     |**Título campo**|Especifica el título del campo en el archivo externo que se asigna al campo que se encuentra en el campo **Id. de la tabla de destino**, cuando se usa una tabla intermedia para importar datos.|
     |**Opcional**|Especifique si se debe omitir la asignación si el campo está vacío. Si no selecciona esta opción, se producirá un error de exportación si el campo está vacío.|  
     |**Regla de transformación**|Especifica la regla que transforma el texto importado en un valor admitido para que se pueda asignar a un campo especificado. Cuando elige un valor en este campo, el mismo valor se introduce en el campo **Regla de transformación** en la tabla **Búfer asignación campo intercambio datos** y viceversa. Consulte la siguiente sección para obtener más información sobre las reglas de transformación disponibles que se pueden aplicar.|
     |**Sobrescribir valor**|Especifica que el valor actual se sobrescribirán con un nuevo valor.|
     |**Prioridad**|Especifique el orden en que se deben procesar las asignaciones de campos. La asignación de campo con el número de mayor prioridad se procesará primero.|
     |**Multiplicador**|Especifique un multiplicador que se aplicará a los datos numéricos, incluidos los valores negativos.|

   * Con el control de alternancia **Usar como tabla intermedia** activado:

     |Campo|Descripción|  
     |---------------------------------|---------------------------------------|  
     |**Nº columna**|Especifique para qué columna del archivo de datos desea definir una asignación.<br /><br /> Solo puede seleccionar las columnas que se representan con líneas en la ficha desplegable **Definiciones de columna** en la página **Definición de intercambio de datos**.|
     |**Título de columna**|Especifica el título de la columna en el archivo externo que se asigna al campo que se encuentra en el campo **Id. de la tabla de destino**, cuando se usa una tabla intermedia para importar datos.|
     |**Id. de la tabla de destino**|Especifique la tabla a la que se asigna el valor del campo **Título columna**, cuando se usa una tabla intermedia para importar datos.|
     |**Título de tabla**|Especifique el nombre de la tabla en el campo **Id. de la tabla de destino**, que es la tabla a la que se asigna el valor del campo **Título columna**, cuando se usa una tabla intermedia para importar datos.|
     |**Id. del campo de destino**|Especifique el campo de la tabla de destino al que se asigna el valor del campo **Título columna**, cuando se usa una tabla intermedia para importar datos.|
     |**Título campo**|Especifique el nombre del campo de la tabla de destino al que se asigna el valor del campo **Título columna**, cuando se usa una tabla intermedia para importar datos.|
     |**Validar solo**|Especifique que el mapa de elemento a campo no se usa para convertir datos, sino solo para validarlos.|
     |**Regla de transformación**|Especifica la regla que transforma el texto importado en un valor admitido para que se pueda asignar a un campo especificado. Cuando elige un valor en este campo, el mismo valor se introduce en el campo **Regla de transformación** en la tabla **Búfer asignación campo intercambio datos** y viceversa. Consulte la siguiente sección para obtener más información sobre las reglas de transformación disponibles que se pueden aplicar.|
     |**Prioridad**|Especifique el orden en que se deben procesar las asignaciones de campos. La asignación de campo con el número de mayor prioridad se procesará primero.|

4. En la ficha desplegable **Agrupación de campos**, especifique las reglas que desea usar para agrupar sus campos cuando cree el archivo completando los campos como se describe en la siguiente tabla.  

     |Campo|Descripción|  
     |--------------------------------- |---------------------------------------|  
     |**Id. de campo**|Especifique el número del campo en el archivo externo que se usa para agrupar y este campo debe configurarlo el usuario.|
     |**Título campo**|Especifique el título del campo en el archivo externo que se usa para agrupación.|

## <a name="transformation-rules"></a>Reglas de transformación

Si los valores en los campos que está asignando difieren, debe usar reglas de transformación para las definiciones de intercambio de datos para que sean iguales. Defina reglas de transformación para las definiciones de intercambio de datos abriendo una definición existente, o creando una nueva definición, y luego en las **Definiciones de línea** FastTab, eligiendo **Gestionar**, y entonces **Mapeo de campo**. Se proporcionan reglas predefinidas, pero también puede crear las suyas propias. La siguiente tabla describe los tipos de transformaciones que puede realizar.

|Opción|Descripción|
|---------|---------|
|**Mayúsculas**|Ponga en mayúscula todas las letras.|
|**Minúsculas**|Ponga todas las letras en minúscula.|
|**Título de caso**|Ponga en mayúscula la primera letra de cada palabra.|
|**Recorte**|Eliminar espacios vacíos antes y después del valor.|
|**Subcadena**|Transforma una parte específica de un valor. Para especificar dónde comenzar la transformación, elija una **Posición de salida** o **Texto de inicio**. La posición inicial es un número que representa el primer carácter a transformar. El texto inicial es la letra inmediatamente anterior a la letra a reemplazar. Si desea comenzar con la primera letra del valor, utilice una posición inicial. Para especificar dónde detener la transformación, elija **Longitud**, que es el número de caracteres a reemplazar, o el **Texto final**, que es el carácter que está inmediatamente después del último carácter a transformar.|
|**Reemplazar**|Encuentre un valor y reemplácelo con otro. Esta transformación es útil para reemplazar valores simples, como una palabra en particular.|
|**Expresión regular - Reemplazar**|Use una expresión regular como parte de una operación de buscar y reemplazar. Esta transformación es útil para reemplazar valores múltiples o quizás más complejos.|
|**Eliminar caracteres no alfanuméricos**|Elimine caracteres que no sean letras o números, como símbolos o caracteres especiales.|
|**Formato de fecha**|Especifique cómo mostrar las fechas. Por ejemplo, puede transformar DD-MM-AAAA a AAAA-MM-DD.|
|**Símbolo decimal**|Defina reglas para la colocación de decimales y la precisión de redondeo.|
|**Coincidencia - expresiones regulares**|Use una expresión regular para encontrar uno o más valores. Esta regla es similar a las opciones de **Subcadena** y **Expresión regular - Reemplazar**.|
|**Personalizado**|Esta regla de transformación es una opción avanzada que requiere asistencia de un desarrollador. Permite un evento de integración al que puede suscribirse si desea usar su propio código de transformación. Si es desarrollador y desea utilizar esta opción, consulte la sección de abajo.|
|**Formato de fecha y hora**|Defina cómo mostrar la fecha actual y la hora del día.|
|**Búsqueda de campo**|Utilice campos de diferentes tablas. Para usarlos, necesita seguir algunas reglas. Primero, use el **Id. de tabla** para especificar el id. de la tabla que contiene el registro para la búsqueda de campos. Después, en el campo **Id. campo origen**, especifique el id. del campo que contiene el registro para la búsqueda de campo. Por último, en el campo **Id. campo destino**, especifique el id. del campo en el que se encuentra el registro para la búsqueda de campo. Opcionalmente, utilice el campo **Regla de búsqueda de campo** para especificar el tipo de búsqueda de campo. Para el campo **Objetivo**, se usa el valor de **Id. campo destino**, incluso si está en blanco. Para el campo **Original si el destino está en blanco**, se utiliza el valor original si el destino está en blanco.|
|**Redondear**|Redondee el valor en este campo usando algunas reglas adicionales. Primero, en el campo **Precisión**, especifique una precisión de redondeo. Después, en el campo **Dirección**, especifique la dirección de redondeo.|

> [!NOTE]  
> Obtenga más información sobre el formato de fecha y hora en [Cadenas de formato de fecha y hora estándar](/dotnet/standard/base-types/standard-date-and-time-format-strings).

### <a name="tip-for-developers-example-of-the-custom-option"></a>Consejo para desarrolladores: ejemplo de la opción personalizada

El siguiente ejemplo muestra cómo implementar su propio código de transformación.

```AL
codeunit 60100 "Hello World"
{
    [EventSubscriber(ObjectType::Table, Database::"Transformation Rule", 'OnTransformation', '', false, false)]
    procedure OnTransformation(TransformationCode: Code[20]; InputText: Text; var OutputText: Text)
    begin
        if TransformationCode = 'CUST' then
            OutputText := InputText + ' testing';
    end;
}
```

Después de definir sus reglas, puede probarlas. En la sección fich desplegable **Prueba**, introduzca un ejemplo de un valor que desea transformar y luego verifique los resultados mediante **Actualizar**.

## <a name="export-a-data-exchange-definition-as-an-xml-file-for-use-by-others"></a>Exportar una definición de intercambio de datos como un archivo XML para que lo utilicen otros usuarios

Cuando haya creado la definición de intercambio de datos para un archivo de datos específico, podrá exportar la definición de intercambio de datos como un archivo XML que podrá importar. Esta tarea se describe en el procedimiento siguiente:  

1. Elija el icono ![Bombilla que abre la característica Dígame 1.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Definiciones de intercambio de datos** y, a continuación, elija el vínculo relacionado.  
2. Seleccione la definición de intercambio de datos que desea exportar.  
3. Seleccione la acción **Exportar definición de intercambio de datos** .  
4. Guarde el archivo XML que representa la definición del intercambio de datos en una ubicación adecuada.  

    Si ya se ha creado una definición de intercambio de datos, solo tiene que importar el archivo XML al marco de intercambio de datos. Esta tarea se describe en el procedimiento siguiente:  

## <a name="import-an-existing-data-exchange-definition"></a>Importar una definición de intercambio de datos existente

1. Guarde el archivo XML que representa la definición del intercambio de datos en una ubicación adecuada.  
2. Elija el icono ![Bombilla que abre la función Dígame 1.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Definiciones de intercambio de datos** y, a continuación, elija el vínculo relacionado.  
3. Seleccione la acción **Importar definición de intercambio de datos**.  
4. Seleccione el archivo que ha guardado en el paso 1.  

## <a name="see-also"></a>Consulte también .

[Configuración del intercambio de datos](across-set-up-data-exchange.md)  
[Configurar el envío y la recepción de documentos electrónicos](across-how-to-set-up-electronic-document-sending-and-receiving.md)  
[Cobrar pagos mediante adeudo directo SEPA](finance-collect-payments-with-sepa-direct-debit.md)  
[Realizar pagos con la extensión AMC Banking 365 Fundamentals o transferencia de crédito SEPA](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md)  
[Documentos entrantes](across-income-documents.md)  
[Funciones empresariales generales](ui-across-business-areas.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
