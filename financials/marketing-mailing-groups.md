---
title: Configurar los grupos de correo para contactos | Documentos de Microsoft
description: Describe grupos de correo para contactos en Financials
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: marketing, campaign, promo, prospect
ms.date: 03/28/2017
ms.author: jswymer
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: fc29f5a6238373db3e862058eb327398e624882e
ms.contentlocale: es-es
ms.lasthandoff: 05/04/2017


---
# <a name="setting-up-mailing-groups-for-contacts"></a>Configurar grupos de correo para contactos
Puede usar grupos de correo para identificar grupos de contactos que quiere que reciban la misma información. Por ejemplo, puede configurar un grupo de direcciones para los contactos a los que desea enviar una notificación de un movimiento de oficina u otro grupo para enviar regalos de vacaciones.

El uso de grupos de correo en contactos es un proceso que consta de dos pasos. Primero, debe definir el código del grupo de correo. Solo debe realzar este paso una vez para cada grupo de correo. Una vez tenga código de grupo de correo, puede comenzar a asignar el código a empresas de contacto.

## <a name="defining-mailing-group-codes"></a>Definir códigos de grupo de correo
El código de grupo de correo define el tipo o la categoría del grupo, como MOVE para movimiento de oficina o GIFT para regalo de vacaciones. Puede tener varios códigos de grupo de industria. Para definir los grupos de industria, pude usar la ventana **Grupos de correo**.

1. En la esquina superior derecha, seleccione el icono **Buscar página o informe** ![Buscar página o informe](media/ui-search/search_small.png "Icono Buscar página o informe"), especifique **Grupos de correo** y elija el vínculo relacionado.
2. Seleccione la acción **Nuevo** e introduzca un código y una descripción. El código admite un máximo de 11 caracteres y puede ser cualquier combinación de números y letras.

## <a name="AssignMailGroupContact"></a> Para asignar grupos de correo a un contacto
1. Abra el contacto.
2. Elija la acción **Grupos de correo**. Se abrirá la ventana **Grupos direcciones contacto**.
3. En el campo **Código de grupos de correo**, seleccione el grupo de correo que desea asignar.

Repita estos pasos para asignar todos los grupos de direcciones que desee. También puede asignar grupos de correo desde la lista de contactos con el mismo procedimiento.

Aparece automáticamente el número de grupos de direcciones asignados al contacto del campo **N.º grupos direcciones** en la sección **Segmentación** en la ventana **Contacto**.

Después de asignar grupos de direcciones a sus contactos puede usar esa información para seleccionar contactos para sus segmentos. Para obtener más información, vea [Procedimiento: Agregar contactos a segmentos](marketing-add-contact-segment.md).

## <a name="see-also"></a>Consulte también
[Crear empresas de contacto](marketing-create-contact-companies.md)  
[Crear personas de contacto](marketing-create-contact-persons.md)  
[Trabajar con Financials](ui-work-product.md)

