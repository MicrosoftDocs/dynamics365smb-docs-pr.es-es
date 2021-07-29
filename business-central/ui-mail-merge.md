---
title: Uso de plantillas de Word para comunicaciones masivas | Microsoft Docs
description: Las plantillas de Word pueden facilitar la creación masiva de documentos personalizados para entidades específicas.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: document, mail, merge, Word, template, email
ms.date: 04/01/2021
ms.author: bholtorf
ms.openlocfilehash: 84b6a9fa74cea99f8b939edcf0cd883e39eb6937
ms.sourcegitcommit: a7cb0be8eae6ece95f5259d7de7a48b385c9cfeb
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 07/08/2021
ms.locfileid: "6445977"
---
# <a name="using-word-templates-for-bulk-communication"></a>Uso de plantillas de Word para comunicaciones masivas
Las plantillas de Microsoft Word pueden facilitar la comunicación masiva con entidades como clientes y proveedores. Por ejemplo, puede crear folletos para alertar a los clientes sobre una campaña de ventas, cartas para informar a los proveedores sobre una nueva directiva de compras o invitaciones para atraer contactos a un próximo evento.

> [!NOTE]
> Puede usar plantillas de Word solo en dispositivos con Microsoft Word 2019 y el sistema operativo Windows instalado.

Puede usar entidades en [!INCLUDE[prod_short](includes/prod_short.md)] como origen de datos para la plantilla y agregar campos de combinación para personalizar documentos para cada entidad. Los campos de combinación proceden de la entidad en [!INCLUDE[prod_short](includes/prod_short.md)]. Cuando aplica una plantilla de Word a una entidad, los datos de los campos de combinación se insertan en el documento.

En la página **Plantillas de Word**, puede usar una guía de configuración asistida para descargar un archivo ZIP que contiene un DataSource.txt y un archivo de plantilla de Word para una entidad. Después de configurar la plantilla y agregar campos de combinación, use la misma guía para cargar la plantilla. Solo puede usar la plantilla de Word y los archivos de origen de datos que descargue desde [!INCLUDE[prod_short](includes/prod_short.md)] y debe almacenar los archivos en la misma ubicación.

> [!NOTE]
> Cuando elige una entidad para la que crear una plantilla, la lista muestra todas las entidades en [!INCLUDE[prod_short](includes/prod_short.md)]. Sin embargo, no puede crear plantillas para todas las entidades. Si el nombre de una entidad contiene caracteres especiales, como **/**, **.**, **_**, o **-**, no puede crear una plantilla para este. El nombre de la entidad se muestra en la columna **Título de objeto**

Cuando está configurando la plantilla en Word, en la pestaña **Correspondencia** puede agregar campos de combinación seleccionando **Insertar campo combinación**.

> [!NOTE]
> No puede usar campos de combinación si el nombre del campo contiene 40 caracteres o más. Por ejemplo, no puede usar el campo Company__Information_Customs_Permit_Date porque tiene 40 caracteres. 

Cuando su plantilla de Word esté lista, en la página **Plantillas de Word** puede elegir **Aplicar** para generar los documentos. Puede crear un documento que contenga secciones para cada entidad o dividir la operación para crear un nuevo documento para cada entidad.

## <a name="to-create-a-word-template"></a>Para crear una plantilla de Word
1. Elija el icono ![Bombilla que abre la función Dígame.](media/ui-search/search_small.png "Dígame qué desea hacer") , escriba **Plantillas de Word** y luego elija el enlace relacionado.
2. Siga los pasos de la guía de configuración asistida. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="see-also"></a>Consulte también
[Administrar diseños de informes y documentos](ui-manage-report-layouts.md)  
