---
title: Uso de plantillas de Word para comunicaciones masivas | Microsoft Docs
description: Las plantillas de Word pueden facilitar la creación masiva de documentos personalizados para entidades específicas.
author: bholtorf
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: document, mail, merge, Word, template, email
ms.date: 04/01/2021
ms.author: bholtorf
ms.openlocfilehash: 9e87e86ea4f267bea0e636f16fab55ae485ee8cf
ms.sourcegitcommit: ef80c461713fff1a75998766e7a4ed3a7c6121d0
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 02/15/2022
ms.locfileid: "8145321"
---
# <a name="using-word-templates-for-bulk-communication"></a>Uso de plantillas de Word para comunicaciones masivas
Las plantillas de Microsoft Word pueden facilitar la comunicación masiva por escrito o por correo con entidades como contactos, clientes y proveedores. Por ejemplo, puede crear folletos para alertar a los clientes sobre una campaña de ventas, cartas para informar a los proveedores sobre una nueva directiva de compras o invitaciones para atraer contactos a un próximo evento.

> [!NOTE]
> Puede usar plantillas de Word solo en dispositivos con Microsoft Word 2019 y el sistema operativo Windows instalado.

Puede usar entidades en [!INCLUDE[prod_short](includes/prod_short.md)] como origen de datos para la plantilla y agregar campos de combinación para personalizar documentos para cada entidad. Los campos de combinación proceden de la entidad en [!INCLUDE[prod_short](includes/prod_short.md)]. Cuando aplica una plantilla de Word a una entidad, los datos de los campos de combinación se insertan en el documento.

En la página **Plantillas de Word**, cuando crea una nueva plantilla, puede usar una guía de configuración asistida para descargar un archivo ZIP que contiene un DataSource.xlsx y un archivo de plantilla de Word para una entidad. El archivo de origen de datos proporciona los campos que puede utilizar en la plantilla. No edite el archivo de origen de datos. Solo puede usar la plantilla de Word y los archivos de origen de datos que descargue desde [!INCLUDE[prod_short](includes/prod_short.md)] y debe almacenar los archivos en la misma ubicación.

Después de configurar la plantilla y agregar campos de combinación, use la misma guía para cargar la plantilla.

## <a name="setting-up-the-template-in-word"></a>Configuración de la plantilla en Word
Cuando está configurando una plantilla en Word, en la pestaña **Correspondencia** puede agregar campos de combinación seleccionando **Insertar campo combinación**. Los campos de combinación que están disponibles provienen del archivo de origen de datos que descargó para la entidad. Actúan como marcadores de posición que le dicen a Word en qué parte del documento colocar la información sobre la entidad. 

:::image type="content" source="media/word-tmpl-merge-field.PNG" alt-text="Agregar campos de combinación en Microsoft Word":::

## <a name="adding-related-entities"></a>Agregar entidades relacionadas
Además de agregar datos para la entidad de origen, es decir, la entidad para la que está creando la plantilla, también puede combinar datos de entidades que están relacionadas con ella. Por ejemplo, si el origen es la entidad Cliente, también puede combinar datos de campos en la entidad Cliente/Comprador porque ambas entidades tienen un campo en común.

Las entidades relacionadas comparten un campo, que a menudo es un identificador, como un nombre, código o id., con la entidad de origen. Cuando configura una plantilla, existen opciones simples y avanzadas para elegir entidades relacionadas:

* Simple: agregue relaciones conocidas que [!INCLUDE[prod_short](includes/prod_short.md)] pone a disposición de forma predeterminada.
* Avanzado: agregue relaciones no estándar, como las que se agregaron mediante extensiones o personalizaciones. Esto requiere que conozca los campos que comparten las entidades.

Cuando agrega una entidad relacionada, debe especificar un prefijo para el nombre del campo. Cuando agrega campos a la plantilla, el prefijo puede facilitar la distinción entre campos de la entidad de origen y campos de entidades relacionadas.

## <a name="to-create-a-word-template-in-business-central"></a>Para crear una plantilla de Word en Business Central
1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Plantillas de Word** y luego elija el enlace relacionado.
2. Elija **Nueva**, luego **Crear una plantilla** y luego siga los pasos de la guía de configuración asistida. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!TIP]
> También puede crear una plantilla directamente desde la página para una entidad eligiendo la acción **Aplicar plantilla de Word** para abrir la guía de configuración asistida, y luego **Nueva plantilla**. Cuando lo haga, el origen de datos se elige según el tipo de entidad.

## <a name="applying-a-template"></a>Aplicar una plantilla
Cuando su plantilla de Word esté lista, en la página **Plantillas de Word** puede elegir **Aplicar** para generar los documentos. Cuando aplica una plantilla de Word a una entidad, los datos de los campos de combinación se insertan en el documento. Puede crear un documento que contenga secciones para cada entidad o eliga **Dividir** para crear un nuevo documento para cada entidad.

Puede aplicar plantillas a una o más entidades del mismo tipo, como un contacto, directamente en el contexto de esa página, o desde la página de plantillas de Word para aplicar la plantilla a todas las entidades de ese tipo.

## <a name="using-word-templates-with-email"></a>Uso de plantillas de Word con correo electrónico
Puede usar plantillas de Word para agregar contenido a los mensajes de correo electrónico. Cuando redacta un correo electrónico, puede elegir la acción **Usar plantilla de Word** para aplicar el contenido de una plantilla al mensaje. Esto requiere que haya creado una o más plantillas para la entidad. Puede usar una plantilla a la vez, y cuando cambia entre plantillas, el mensaje cambia para reflejar el contenido de la plantilla elegida.

Además, puede utilizar la acción **Agregar archivo desde plantilla de Word** para adjuntar el contenido de la plantilla al correo electrónico como un archivo. El archivo utilizará el formato que especificó para la salida de la plantilla.

:::image type="content" source="media/email-word-tmpl.PNG" alt-text="Opciones para usar contenido de una plantilla de Word en un correo electrónico":::

## <a name="see-also"></a>Consulte también
[Administrar diseños de informes y documentos](ui-manage-report-layouts.md)  
