---
title: "Gestionar la configuración de la empresa en una hoja de trabajo | Documentos de Microsoft"
description: "La hoja de trabajo de configuración es la ubicación central en la que puede planificar, controlar y realizar el trabajo de configuración. Puede crear una hoja de trabajo para cada empresa con la que trabaja o crear una hoja de trabajo de configuración estándar que se puede usar para configurar varias empresas idénticas."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 12/07/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 8a73de1aa2f4a0f633c401ea341bb7bde6579723
ms.openlocfilehash: 1ba27ee0ac252bbe1fd47b900654980df5b18fdf
ms.contentlocale: es-es
ms.lasthandoff: 12/11/2018

---
# <a name="manage-company-configuration-in-a-worksheet"></a>Gestionar la configuración de la empresa en una hoja de trabajo
La hoja de trabajo de configuración es la ubicación central en la que puede planificar, controlar y realizar el trabajo de configuración. Puede crear una hoja de trabajo para cada empresa con la que trabaja o crear una hoja de trabajo de configuración estándar que se puede usar para configurar varias empresas idénticas.  

El primer paso en la preparación de un paquete de configuración es seleccionar una empresa ya configurada y modificada para ajustarse a la mayoría de las necesidades de la solución. Esta empresa sirve como línea base para el trabajo de configuración para las empresas nuevas. En la hoja de trabajo, indica las tablas que desea que la configuración controle y procese. Puesto que la mayoría de las tablas en [!INCLUDE[d365fin](includes/d365fin_md.md)] tienen relaciones y dependencias con otras tablas, también debería incluir esas tablas relacionadas según sea necesario. Juntas, estas tablas servirán como la estructura en torno a la que creará una nueva empresa. Los pasos siguientes le ayudan a empaquetar y luego implementar la configuración.  

Para ayudarle en el seguimiento y la revisión de su trabajo, use el cuadro informativo **Tabla de paquetes de configuración** para ver información acerca de los registros. Utilice el cuadro informativo **Tabla relacionada con la configuración** para controlar las relaciones de tabla.  

En los procedimientos siguientes se muestra cómo agregar y personalizar la información de tabla para la configuración.  

## <a name="to-open-the-configuration-worksheet"></a>Procedimiento para abrir la hoja de trabajo de configuración  
1.  En [!INCLUDE[d365fin](includes/d365fin_md.md)], abra la empresa que servirá de línea base para la configuración, y abra el Área de trabajo del implementador de RapidStart Services.  
2.  Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Hoja de configuración** y luego elija el enlace relacionado.  

## <a name="to-add-a-table-to-the-worksheet"></a>Procedimiento para agregar una tabla a la hoja de trabajo  
1.  En la página **Configurar hoja**, seleccione la acción **Editar lista**.  
2.  En la primera línea, en el campo **Tipo línea**, seleccione **Tabla**.  
4.  En el campo **Id. de tabla**, seleccione la tabla que desee agregar a la configuración.  
5.  En el campo **Id. de página**, especifique el identificador de la página asociado con la tabla. Para las tablas estándar, este valor se rellena automáticamente. Para las tablas personalizadas, debe proporcionar el identificador.
6.  En el campo **Referencia**, especifique la dirección URL de una página de documentación, por ejemplo en Ayuda, que proporciona información o instrucciones sobre prácticas recomendadas o la configuración de la tabla.  
7.  Para agregar las tablas relacionadas, elija la acción de **Obtener tablas relacionadas**.  

    > [!NOTE]  
    > Las tablas relacionadas no se agregarán con la acción **Obtener tablas relacionadas** si se aplica cualquiera de lo siguiente:
    > - La relación es condicional.  
    > Ejemplo: si se obtienen tablas relacionadas para la tabla **Cliente**, entonces la tabla **Almacén** no se agregará, ya que está solo condicionalmente con la tabla **Cliente**, por ejemplo si el campo **Cód. almacén** se ha rellenado en la tabla **Cliente**.  
    > - Se filtra la tabla relacionada.  
    > Ejemplo: un campo de la tabla relacionada tiene la cláusula WHERE. El motivo es que la información sobre las relaciones correspondientes está almacenada en la tabla del sistema **Campo**, que no está totalmente accesible a la aplicación.  
    > Debe agregar dichos tipos de tablas manualmente según el paso 4 de este procedimiento.  

8.  Para modificar la lista de tablas resultante, seleccione una tabla que desee quitar y elija la acción **Eliminar**.  
9. Repita los pasos para cada tabla que desee agregar a la configuración.  
10. Para eliminar información de tabla duplicada, que puede resultar del uso de la acción **Obtener tablas relacionadas**, seleccione la acción **Eliminar líneas duplicadas**. Esto eliminará las tablas duplicadas que tengan el mismo código de paquete.  

## <a name="to-add-multiple-tables-to-the-configuration-worksheet"></a>Procedimiento para agregar varias tablas a la hoja de trabajo de configuración  
1. Seleccione la acción **Obtener tablas**. Se abre la página de proceso **Obtener tablas de configuración**.  
2. En la ficha desplegable **Opciones**, especifique los tipos de tablas que desea agregar a la configuración, como se describe en la siguiente tabla.

    |Opción|Description|  
    |----------------------------------|---------------------------------------|  
    |**Incluir solo con datos**|Active esta casilla para incluir solo las tablas que contengan datos. Por ejemplo, puede incluir una tabla que ya define las condiciones típicas de pago que admite la solución.|  
    |**Incluir tablas relacionadas**|Active la casilla para incluir todas las tablas relacionadas. Para agregar un subconjunto de tablas relacionadas, consulte el paso 3 de este procedimiento.|  
    |**Incluir tablas de dimensión**|Active la casilla para incluir tablas de dimensión.|  
    |**Incluir solo tablas con licencia**|Activa la casilla para incluir solo las tablas para las que la licencia bajo la que se está creando la hoja de trabajo permita acceso.|

3. En la ficha desplegable **Objeto**, establezca filtros según corresponda para especificar los tipos de tablas que desee incluir o excluir.  
4. Elija el botón **Aceptar**. Las tablas de [!INCLUDE[d365fin](includes/d365fin_md.md)] se agregan a la hoja de trabajo. Cada movimiento de la lista tiene un tipo de línea **Tabla**.  
5. Para eliminar información de tabla duplicada, que puede resultar del uso de la acción **Obtener tablas**, seleccione la acción **Eliminar líneas duplicadas**. Esto eliminará las tablas duplicadas que tengan el mismo código de paquete.  
6. Puede agregar a la hoja de trabajo tablas relacionadas con una tabla seleccionada. Revise la información del cuadro informativo **Tablas relacionadas** para ver si hay tablas que faltan. Para agregar tablas relacionadas para una tabla específica, seleccione la tabla de la lista y elija la acción **Traer tablas relacionadas**.  

    > [!NOTE]  
    > Las tablas relacionadas no se agregarán con la acción **Obtener tablas relacionadas** si se aplica cualquiera de lo siguiente:
    > - La relación es condicional.  
    > Ejemplo: si se obtienen tablas relacionadas para la tabla **Cliente**, entonces la tabla **Almacén** no se agregará, ya que está solo condicionalmente con la tabla **Cliente**, por ejemplo si el campo **Cód. almacén** se ha rellenado en la tabla **Cliente**.  
    > - Se filtra la tabla relacionada.  
    > Ejemplo: un campo de la tabla relacionada tiene la cláusula WHERE. El motivo de esto es que la información de las relaciones involucradas está almacenada en la tabla virtual **Campo** y no está disponible en páginas como la hoja de cálculo de la configuración por motivos de rendimiento.  
    > Deberá agregar tablas con estas relaciones complejas manualmente según el paso 4 de la sección "Procedimiento para agregar una tabla a la hoja de cálculo".

7. Para eliminar tablas de la lista de tablas resultante, seleccione una tabla que desee quitar y elija la acción **Eliminar**.  

Use el procedimiento siguiente para especificar los campos de tabla que se deben incluir. Una vez que realice esta especificación, puede exportar la tabla a Excel y usar la estructura de tabla como plantilla para recopilar datos de cliente. Para obtener más información, consulte [Prepararse para migrar datos del cliente](admin-use-templates-to-prepare-customer-data-for-migration.md).  

## <a name="to-specify-a-set-of-fields-and-records-for-a-configuration-table"></a>Procedimiento para especificar un conjunto de campos y registros para una tabla de configuración  
1. Seleccione una tabla de la lista de tablas de configuración y elija la acción **Editar lista**.  
2. Seleccione una tabla para la que desee especificar información de campo y seleccione la acción **Campos**.  
3. Para seleccionar solo los campos que desee incluir, elija la acción **Borrar incluido**. Para agregar todos los campos, elija la acción **Establecer incluidos**.  
4. o especifique que los datos de campo no deben validarse, desactive la casilla **Validar campo** del campo.  
5. Elija el botón **Aceptar**.  
6. Para filtrar y obtener un conjunto determinado de registros que deben incluirse en la hoja de trabajo de configuración, elija la acción **Filtros** y especifique los valores de filtro apropiados.

Puede crear áreas de funcionalidad y grupos de tablas en la hoja de trabajo con el fin de ajuntar funciones similares. Por ejemplo, en la configuración del plan de cuentas de la configuración, puede decidir crear a un grupo de tablas de registro. Normalmente, se usan áreas para agrupar un conjunto de tablas que corresponden a un área funcional. Cada área puede contener grupos. Un grupo se puede usar para organizar y agrupar las tablas con un significado común.  

En el procedimiento siguiente se describe cómo agregar el área y agrupar designaciones después de haber creado la lista inicial de tablas. Después de haber agregado estas categorías, puede seguir agregando y modificando la lista de tablas.  

## <a name="to-categorize-and-group-functionality-in-the-worksheet"></a>Procedimiento para clasificar y agrupar funciones en la hoja de trabajo  
1. Al inicio de un área, inserte una línea nueva en la hoja de trabajo.  
2. En el campo **Tipo línea**, elija **Área**. En el campo **Nombre**, escriba un nombre para el 'area.  
3. Al inicio de una agrupación de tablas, inserte una línea nueva en la hoja de trabajo.  
4. En el campo **Tipo línea**, elija **Grupo**. En el campo **Nombre**, escriba un nombre para el 'area. El nombre del grupo se sangra automáticamente.  
5. Para mover tablas a la categoría adecuada, seleccione una tabla para mover y las acciones **Mover arriba** o **Mover abajo**. Como alternativa, puede eliminar una línea de la hoja de trabajo e insertar la tabla otra vez en la ubicación necesaria.  

Algunas tablas de [!INCLUDE[d365fin](includes/d365fin_md.md)] son estándar y los datos que contienen probablemente no cambiarán de una implementación a otra. Por tanto, para ayudar al cliente, puede quitar estas tablas de la hoja de trabajo después de haberlas incluido en el paquete de configuración. Una vez agregadas, las tablas siguen formando parte del paquete de configuración.  

## <a name="to-remove-a-standard-table-in-the-worksheet"></a>Procedimiento para quitar una tabla estándar de la hoja de trabajo  
Después de haber agregado todas las tablas necesarias a un paquete de configuración, determine cuáles no requerirán la atención del cliente.  
1.  Seleccione las tablas y elimínelas mediante la acción **Eliminar**.  

    > [!NOTE]  
    >  Las tablas permanecen en el paquete aunque se eliminen de la hoja de trabajo.  

## <a name="to-review-and-customize-existing-database-data"></a>Para revisar y personalizar datos de base de datos existentes
A medida que crea un paquete de configuración para una solución, puede ver y personalizar los datos de base de datos disponibles para satisfacer las necesidades del cliente. La tabla de base de datos debe tener una página asociada.  

## <a name="to-customize-data-in-the-database"></a>Procedimiento para personalizar los datos en la base de datos  

1.  En la página **Hoja de trabajo de configuración**, indique las tablas cuyos datos desee ver o personalizar.  

    > [!NOTE]  
    >  Asegúrese de que cada tabla tenga asignado un identificador de página. Para las tablas de [!INCLUDE[d365fin](includes/d365fin_md.md)] estándar, este valor se rellena automáticamente. Para las tablas personalizadas, debe proporcionar el identificador.  

2.  Seleccione la acción **Datos de base de datos**.  

     Se abre la página [!INCLUDE[d365fin](includes/d365fin_md.md)] para la página.  

3.  Revise la información disponible. Modifíquela según sea necesario. Para ello, elimine los registros que no son pertinentes o agregue registros nuevos.

## <a name="see-also"></a>Consulte también  
[Establecer la configuración de una empresa](admin-set-up-company-configuration.md)  
[Configurar una empresa con RapidStart Services](admin-set-up-a-company-with-rapidstart.md)  
[Administración](admin-setup-and-administration.md)

