---
title: Preparar un paquete de configuración | Documentos de Microsoft
description: Cuando se configura una nueva empresa, se reconocen y se procesan las relaciones de tabla. Los datos se importan y se aplican en el orden correcto. Si en el paquete de configuración se incluyen tablas de dimensión, estas también se importan.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: fde77f873897d801e6bf06d55d57e9406f352eed
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/29/2019
ms.locfileid: "1245864"
---
# <a name="prepare-a-configuration-package"></a>Preparar un paquete de configuración
Cuando se configura una nueva empresa, se reconocen y se procesan las relaciones de tabla. Los datos se importan y se aplican en el orden correcto. Si en el paquete de configuración se incluyen tablas de dimensión, estas también se importan. Para obtener más información, consulte [Para importar datos del cliente](admin-migrate-customer-data.md#to-import-customer-data). 

Para ayudar al cliente a usar el paquete de configuración, puede agregar un cuestionario o un conjunto de cuestionarios al paquete. El cuestionario puede ayudar al cliente a comprender las distintas opciones de configuración. Normalmente, los cuestionarios se crean para las tablas de configuración principales cuando un cliente pueda requerir asistencia adicional sobre cómo seleccionar una configuración adecuada. Para obtener más información, vea [Recopilación de valores de configuración de cliente](admin-gather-customer-setup-values.md).

Asegúrese de que se encuentra en el Área de trabajo del implementador de RapidStart Services. Para obtener más información, vea [Usar el Área de trabajo del implementador de RapidStart Services](admin-how-to-use-the-rapidstart-services-role-center-to-track-progress.md)

> [!IMPORTANT]  
>  Al exportar e importar los paquetes de configuración entre dos bases de datos de empresa, las bases de datos deben tener el mismo esquema para garantizar que todos los datos se transferirán correctamente. Esto significa que las bases de datos deben tener la misma estructura de tablas y campos, en la que las tablas con las mismas claves principales y campos tienen los mismos identificadores y tipos de datos.  
>   
>  Puede importar un paquete de configuración que se ha exportado desde una base de datos con un esquema distinto al de la base de datos de destino. Sin embargo, no se importarán las tablas o los campos del paquete de configuración que falten en la base de datos de destino. Tampoco se importarán las tablas con diferentes claves principales ni los campos con distintos tipos de datos. Por ejemplo, si el paquete de configuración incluye la tabla **50000, Cliente** que tiene la clave principal **Code20** y la base de datos a la que importa el paquete incluye la tabla **50000, Banco cliente** que tiene la clave principal **Code20 + Código 20**, no se importarán los datos.  

## <a name="to-create-a-configuration-package"></a>Procedimiento para crear un paquete de configuración  
1. Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Paquetes de configuración** y luego elija el enlace relacionado.  
2. Seleccione la acción **Nuevo**.  
3. En la ficha desplegable **General**, rellene el resto de los campos según corresponda. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
4. Para excluir del paquete los cuestionarios de configuración, las plantillas de configuración y las tablas de la hoja de trabajo de configuración, active la casilla **Excluir tablas de configuración**. De lo contrario, estas tablas se agregarán automáticamente a la lista de tablas del paquete cuando este se exporte.  
5. Seleccione la acción **Obtener tablas**. Se abre la página de proceso **Traer tablas de paquete**.  
6. Elija el campo **Seleccionar tablas**. Se abre la página **Selección config**.  
7. Elija la acción **Seleccionar todo** para agregar todas las tablas al paquete, o bien active la casilla **Seleccionado** para cada tabla de la lista que desee agregar.
8. Elija el botón **Aceptar**. El número de tablas seleccionado se indica en el campo **Seleccionar tablas**. Especifique las opciones adicionales y, a continuación, seleccione el botón **Aceptar**. Las tablas de [!INCLUDE[d365fin](includes/d365fin_md.md)] se agregan a las líneas de la página **Config. paquete**.  

    > [!NOTE]  
    >  También puede hacer esta operación en la hoja de trabajo de configuración. Seleccione las tablas que desea incluir en el paquete y seleccione la acción **Asignar paquete**.

9. Para seleccionar los campos que desee incluir de una tabla, seleccione la tabla y en la pestaña **Líneas** elija la acción **Campos**.
Especifique los campos que se incluyen en el paquete. De manera predeterminada, se incluyen todos los campos.

    - Para seleccionar solo los campos que desee incluir, elija la acción **Borrar incluido**. Para agregar todos los campos, elija la acción **Establecer incluidos**.  
    - Para especificar que los datos de campo no deben validarse, desactive la casilla **Validar campo** del campo.  

10. Determine si ha introducido errores potenciales y elija la acción **Validar paquete**. Esto puede suceder cuando no incluye tablas en las que depende la configuración.  
11. Elija el botón **Aceptar**.  

Cuando haya ajustado la lista de campos que se deben incluir de una tabla, puede comprobar los resultados en Excel.  

### <a name="to-filter-and-review-your-dataset"></a>Procedimiento ara filtrar y revisar el conjunto de datos  
1. Para filtrar y obtener un conjunto determinado de registros que deben incluirse en el paquete, en la pestaña **Líneas**, elija la acción **Filtros** y especifique los valores de filtro apropiados.  
2. En la ficha del paquete, en la pestaña **Líneas**, seleccione la acción **Exportar a Excel**.  
3. Confirme los mensajes que permiten la exportación de los datos a Excel. Se abre el archivo .xlsx indicado. Revise los registros que se exportaron.  
4. Cierre Excel.  

### <a name="to-include-a-template-for-application-to-a-table"></a>Procedimiento para incluir una plantilla aplicarla a una tabla  
Para determinadas tablas, tal como una tabla que contendrá datos maestros, puede especificar una plantilla para aplicar a los datos. La plantilla puede incluir los campos obligatorios que desee aplicar a todos los datos maestros y que nunca deben variar. Por ejemplo, puede crear una plantilla que se usará con los datos de cliente. La plantilla puede incluir todos los campos obligatorios, lo que permitirá la importación coherente de información estandarizada. La información que no se puede estandarizar, tal como el nombre del cliente, se procesa cuando se realiza una importación de los datos de cliente.

1. En la página **Configurar tarjeta de paquete**, seleccione una tabla y, a continuación, elija el campo **Plantilla datos**. Se muestra una lista de plantillas basadas en la tabla.
2. Seleccione una plantilla y haga clic en el botón **Aceptar**.  

Una vez finalizado el paquete, siga el procedimiento siguiente para guardarlo en un archivo. A continuación, proporcione el paquete a un cliente o un socio.

### <a name="to-save-and-export-a-configuration-package"></a>Procedimiento para guardar y exportar un paquete de configuración  
- En la página **Configurar tarjeta de paquete**, seleccione la acción **Exportar paquete**.  

El paquete se crea en un archivo .rapidstart, que entrega los contenidos de paquete en un formato comprimido. Los cuestionarios de configuración, las plantillas de configuración y la hoja de trabajo de configuración se agregan al paquete automáticamente, a menos que decida excluirlos específicamente.  

Puede guardar el archivo con un nombre que tenga significado para usted, pero no puede modificar la extensión de archivo. Debe ser .rapidstart.  

### <a name="to-copy-a-configuration-package"></a>Procedimiento para copiar un paquete de configuración  
Una vez que haya creado un paquete que satisfaga la mayoría de sus necesidades, puede emplearlo como base para crear paquetes similares. Esto puede agilizar el tiempo de implementación y mejora la capacidad de repetición de RapidStart Services.

1. Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Paquetes de configuración** y luego elija el enlace relacionado.  
2. Seleccione un paquete de la lista y, a continuación, seleccione la acción **Copiar paquete**.  
3. Escriba un código para el nuevo paquete en el campo **Nuevo código paquete**.  
4. Active la casilla **Copiar datos** si también desea copiar los datos de base de datos del paquete existente.  
5. Elija el botón **Aceptar**.

## <a name="to-customize-a-configuration-package"></a>Procedimiento para personalizar un paquete de configuración
Use la hoja de trabajo de configuración para recopilar y clasificar la información que desea usar para configurar una nueva empresa, y organice las tablas de manera lógica. El formato de la hoja de trabajo se basa en una jerarquía sencilla: las áreas contienen grupos que, a su vez, contienen tablas. Las áreas y los grupos son opcionales, pero son necesarios para activar un resumen del proceso de configuración en el Área de trabajo de RapidStart Services.

1.  Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Hoja de configuración** y luego elija el enlace relacionado.  
2.  En el campo **Tipo línea**, elija **Área**. Especifique un nombre descriptivo en el campo **Nombre**.  
3.  En el campo **Tipo línea**, elija **Grupo**. Especifique un nombre descriptivo en el campo **Nombre**.  
4.  En el campo **Tipo línea**, elija **Tabla**. En el campo **Id. tabla**, seleccione la tabla que desee incluir en la hoja de trabajo.  

Ahora puede asignar las tablas a paquetes de configuración específicos que se ha creado o tiene previsto crear. Para obtener más información sobre cómo crear un proyecto, consulte [Para asignar una tabla a un paquete de configuración](admin-how-to-prepare-a-configuration-package.md#to-assign-a-table-to-a-configuration-package).

## <a name="to-work-with-promoted-tables"></a>Procedimiento para trabajar con tablas promocionadas  
1. Active la casilla **Tabla promocionada** para indicar una tabla que un cliente típico usará con frecuencia durante el proceso de configuración, por ejemplo, la tabla **Cuenta**. Cuando una tabla tiene esta designación, un cliente podrá filtrar fácilmente su hoja de trabajo para ver solo la lista de tablas promocionadas que necesitan atención.  
2. Para ver la vista filtrada, elija la acción **Solo promocionados**. La lista de tablas contiene solo las tablas con la casilla activada.  

## <a name="to-assign-a-table-to-a-configuration-package"></a>Procedimiento para asignar una tabla a un paquete de configuración  
Una vez definidas las tablas que se deben procesar como parte de la configuración, puede asignarlas fácilmente a los paquetes de configuración. Puede asignar una tabla únicamente a un solo paquete. En el procedimiento siguiente, asignará el paquete dentro de la hoja de trabajo de configuración.  

> [!NOTE]  
>  También puede crear un paquete directamente y agregarle tablas. Para obtener más información sobre cómo crear un proyecto, consulte [Para crear un paquete de configuración](admin-how-to-prepare-a-configuration-package.md#to-create-a-configuration-package).

1. Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Hoja de configuración** y luego elija el enlace relacionado.
2. En la hoja de trabajo de configuración, seleccione una línea o un grupo de líneas que desee asignar a un paquete de configuración y elija la acción **Asignar paquete**.  
3.  Seleccione un paquete de la lista o elija la acción **Nuevo** para crear un nuevo paquete y, a continuación, elija el botón **Aceptar**.  

    Si una tabla todavía no está incluida en el paquete, ahora se agregará. El campo del código de paquete en la línea de hoja de trabajo se rellenará con el código del paquete al que está asignada la tabla.  
4. Si elige un paquete existente, para ver cuántas tablas se incluyen en él, consulte la información del campo **Nº de tablas**.

## <a name="to-review-or-customize-existing-database-data"></a>Revisar o personalizar datos de base de datos existentes
A medida que crea un paquete de configuración para una solución, puede ver y personalizar los datos de base de datos disponibles para satisfacer las necesidades del cliente. La tabla de base de datos debe tener una página asociada.  

1. Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Hoja de configuración** y luego elija el enlace relacionado.
2. En la hoja de trabajo de configuración, indique las tablas cuyos datos desee ver o personalizar.  

    > [!NOTE]  
    >  Asegúrese de que cada tabla tenga asignado un identificador de página. Para las tablas de [!INCLUDE[d365fin](includes/d365fin_md.md)] estándar, este valor se rellena automáticamente. Para las tablas personalizadas, debe proporcionar el identificador.

3. Seleccione la acción **Datos de base de datos**. Se abre la página relacionada para la página.
4. Revise la información disponible. Modifíquela según sea necesario. Para ello, elimine los registros que no son pertinentes o agregue registros nuevos.    

## <a name="to-copy-data-from-a-test-environment-to-a-production-environment"></a>Copiar datos desde el entorno de prueba al entorno de producción  
Una vez que haya revisado y probado toda la información de configuración, puede comenzar a copiar datos al entorno de producción. Crea una nueva empresa en la misma base de datos.

1. Abra e inicializa la nueva empresa.  
2. Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Hoja de configuración** y luego elija el enlace relacionado.  
3. Seleccione la acción **Copiar datos desde empresa**.  
4. En la página **Copiar datos de empresa**, elija el campo **Copiar de**. Se abre la página **Empresas**.  
5. Seleccione la empresa desde la que desea copiar datos y elija el botón **Aceptar**. Aparece una lista de tablas seleccionadas en la hoja de trabajo de configuración. Solo las tablas que contienen registros se incluyen en la lista.
6. Seleccione las tablas desde las que desea copiar datos y elija la acción **Copiar datos**. En la página **Copiar datos de empresa**, elija el botón **Aceptar**.  

## <a name="see-also"></a>Consulte también  
[Recopilación de valores de configuración de cliente](admin-gather-customer-setup-values.md)  
[Establecer la configuración de una empresa](admin-set-up-company-configuration.md)  
[Configurar una empresa con RapidStart Services](admin-set-up-a-company-with-rapidstart.md)  
[Administración](admin-setup-and-administration.md)
