---
title: Uso de plantillas de Word para comunicaciones masivas
description: Las plantillas de Word pueden facilitar la creación masiva de documentos personalizados para entidades específicas.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.date: 02/01/2023
ms.custom: bap-template
ms.search.forms: '9989, 13,'
---

# <a name="use-word-templates-for-bulk-communication" />Usar plantillas de Word para comunicaciones masivas

Las plantillas de Microsoft Word pueden facilitar la comunicación masiva por escrito o por correo con entidades como contactos, clientes y proveedores. Por ejemplo, puede crear:

* Folletos para alertar a los clientes sobre una campaña de ventas
* Cartas para informar a los proveedores sobre una nueva directiva de compras
* Invitaciones para atraer contactos a un próximo evento

> [!NOTE]
> Al establecer plantillas de Word, debe usar un dispositivo con Microsoft Word 2019 o posterior y el sistema operativo Windows instalado.

## <a name="set-up-the-source-of-data" />Establecer el origen de los datos

Use entidades en [!INCLUDE[prod_short](includes/prod_short.md)] como origen de datos para la plantilla y agregar campos de combinación para personalizar documentos para cada entidad. Los campos de combinación proceden de la entidad en [!INCLUDE[prod_short](includes/prod_short.md)]. Cuando aplica una plantilla de Word a una entidad, los datos de los campos de combinación se insertan en el documento.

En la página **Plantillas de Word**, cuando crea una nueva plantilla, una guía de configuración asistida le ayudará con los siguientes pasos:

1. Elija una o más entidades para usar como origen de los datos. Por ejemplo, si desea crear un folleto para una campaña de ventas, probablemente elija la entidad Cliente como origen.
2. Elija otras entidades como orígenes adicionales de datos. Obtenga más información en [Agregar entradas relacionadas o no relacionadas con la entidad de origen](#add-entries-that-are-related-or-unrelated-to-the-source-entity).
3. Descargue una plantilla en blanco. Puede configurar la plantilla en Word de inmediato, o puede cargar la plantilla en blanco y terminar la guía. Cuando su plantilla esté lista, use la acción **Subir**, en la página **Plantillas de Word**, para reemplazar la plantilla en blanco con su plantilla terminada. Para obtener más información, vea [Configurar la plantilla en Word](#set-up-the-template-in-word).
4. Suba la plantilla que ha preparado.
5. Introduzca un código y un nombre que identifique la plantilla.

Cuando descarga una plantilla, obtiene un archivo .zip que incluye dos archivos.

|Archivo  |Descripción  |
|---------|---------|
|DataSource.xlsx     | El archivo de origen de datos proporciona los campos que puede utilizar en la plantilla. No edite el archivo de origen de datos. Solo puede usar la plantilla de Word y los archivos de origen de datos que descargue, y debe almacenar los archivos en la misma ubicación.     |
|Plantilla de Word     | Un archivo .docx para usar como plantilla.        |

Para obtener información sobre cómo configurar una plantilla en Word, vaya a [Configurar la plantilla en Word](#set-up-the-template-in-word).

## <a name="add-entries-that-are-related-or-unrelated-to-the-source-entity" />Agregue entradas relacionadas o no relacionadas con la entidad de origen

También puede fusionar datos de otras entidades. Para agregar otras entidades como orígenes de datos, use una de las siguientes acciones en la página **Plantillas de Word** o cuando esté usando la guía de configuración asistida:

|Acción  |Descripción  |
|---------|---------|
|**Agregar entidad relacionada**  | Utilice datos de entidades que estén relacionadas con la entidad de origen. Por ejemplo, para la entidad Cliente también puede fusionar datos de la entidad Contacto. Las entidades están relacionadas cuando un campo de una entidad hace referencia a otra. Un campo de la entidad Cliente hace referencia a un campo de la entidad Contacto, por lo que están relacionados. El campo compartido suele ser un identificador, como un nombre, código o id.        |
|**Agregar entidad no relacionada**| Utilice datos de entidades que no estén relacionadas con la entidad de origen. Por ejemplo, está creando una plantilla para la entidad Cliente. Puede agregar la entidad Información empresa para poder incluir sus datos de contacto. Un beneficio clave es que si cambia su información de contacto, se actualiza automáticamente en su plantilla. Después de agregar una entidad no relacionada, puede agregar entidades relacionadas con ella.         |

Para entradas no relacionadas, elija un registro específico. Debido a que solo puede agregar una entidad una vez, para usar un registro diferente debe eliminar la entidad y agregarla nuevamente con el nuevo registro.

Puede crear una jerarquía de entidades, tanto relacionadas como no relacionadas. La relación se muestra como una estructura de árbol. El campo **Relación de entidad** también muestra información sobre la relación. Para entidades no relacionadas, el campo muestra el registro que crea la relación.

Cuando agregue entidades, use el campo **Prefijo de campo** para especificar un prefijo para los nombres de campo. Más tarde, al agregar campos a la plantilla, el prefijo ayuda a distinguir entre campos de la entidad de origen y de otras.

### <a name="select-the-fields-to-include" />Seleccionar los campos a incluir

Para cada entidad, puede especificar los campos que desea que estén disponibles para la plantilla. Elija el número en la columna **Número de campos seleccionados** para acceder a una lista de campos que están disponibles. En la página **Selección de campo**, utilice la casilla **Incluir** para especificar los campos. Para algunas entidades, los campos que suelen utilizar las empresas se incluyen de forma predeterminada. Puede editar la lista, por ejemplo, para eliminar los campos predeterminados. Sus cambios se aplican solo a la plantilla en la que está trabajando.

> [!NOTE]
> El número total de campos que puede agregar de todas las entidades es 250.

> [!NOTE]
> Usted o su socio de Microsoft pueden agregar campos personalizados a las entidades. Cuando lo haga, ponemos al nombre de los campos el prefijo **CALC** y les asignamos el tipo de campo **Calculado**. El tipo de campo se denomina calculado para indicar que el campo puede mostrar diferentes tipos de valores, como texto, números, fechas, etc.

## <a name="to-create-a-word-template-in-business-central" />Para crear una plantilla de Word en Business Central

1. Elija el icono ![Bombilla que abre la característica Dígame](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Plantillas de Word** y luego elija el enlace relacionado.
2. Elija **Nueva**, luego **Crear una plantilla** y luego siga los pasos de la guía de configuración asistida. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!TIP]
> También puede crear una plantilla directamente desde la página para una entidad eligiendo la acción **Aplicar plantilla de Word** para abrir la guía de configuración asistida, y luego **Nueva plantilla**. Cuando lo haga, el origen de datos se elige según el tipo de entidad.

## <a name="set-up-the-template-in-word" />Configurar la plantilla en Word

Cuando está configurando una plantilla en Word, en la pestaña **Correspondencia** puede agregar campos de combinación seleccionando **Insertar campo de combinación**. Los campos de combinación provienen del archivo de origen de datos que descargó para la entidad. Actúan como marcadores de posición que le dicen a Word en qué parte del documento colocar la información sobre la entidad.

:::image type="content" source="media/word-tmpl-merge-field.PNG" alt-text="Agregar campos de combinación en Microsoft Word":::

## <a name="apply-a-template" />Aplicar a plantilla

Cuando su plantilla de Word esté lista, en la página **Plantillas de Word** puede elegir **Aplicar** para generar los documentos. Cuando aplica una plantilla de Word a una entidad, los datos de los campos de combinación se insertan en el documento. Puede crear un documento que contenga secciones para cada entidad o eliga **Dividir** para crear un nuevo documento para cada entidad.

Puede usar la acción **Aplicar plantillas de Word** para aplicar plantillas a una o más entidades del mismo tipo de entidad, como un cliente, directamente en el contexto de la página para la entidad. Por ejemplo, las páginas **Cliente** o **Proveedor**.

## <a name="use-word-templates-with-email" />Usar plantillas de Word con correo electrónico

Puede usar plantillas de Word para agregar contenido a los mensajes de correo electrónico. Cuando redacta un correo electrónico, puede elegir la acción **Usar plantilla de Word** para aplicar el contenido de una plantilla al mensaje. Debe haber creado plantillas para la entidad. Puede usar una plantilla a la vez, y cuando cambia entre plantillas, el mensaje cambia para reflejar el contenido de la plantilla elegida.

Además, puede utilizar la acción **Agregar archivo desde plantilla de Word** para adjuntar el contenido de la plantilla al correo electrónico como un archivo. El archivo utilizará el formato que especificó para la salida de la plantilla.

:::image type="content" source="media/email-word-tmpl.PNG" alt-text="Opciones para usar contenido de una plantilla de Word en un correo electrónico":::

## <a name="edit-a-word-template" />Editar una plantilla de Word

Puede realizar los siguientes cambios en sus plantillas de Word:

* Para editar el texto del cuerpo o combinar campos incluidos en la plantilla, use la acción **Descargar**, realice los cambios y luego use la acción **Cargar**
* Para cambiar los orígenes de datos, use la acción **Editar entidades relacionadas**
* Para reemplazar la plantilla de Word con una plantilla nueva, use la acción **Subir**
* Eliminar la plantilla

## <a name="see-also" />Consulte también

[Administrar diseños de informes y documentos](ui-manage-report-layouts.md)  
[Configurar correo electrónico](admin-how-setup-email.md)  
