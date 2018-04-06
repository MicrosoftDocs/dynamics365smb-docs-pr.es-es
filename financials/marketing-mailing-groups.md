---
title: Configurar grupos de correo para contactos | Documentos de Microsoft
description: "Puede usar grupos de correo para identificar grupos de contactos que deben recibir la misma información, por ejemplo, para una campaña de marketing o una promoción."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: marketing, campaign, promo, prospect
ms.date: 06/06/2017
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 7402899cb7fe369503eee1b451dc652180e96264
ms.contentlocale: es-es
ms.lasthandoff: 03/22/2018

---
# <a name="set-up-mailing-groups-for-contacts"></a>Configurar grupos de correo para contactos
Puede usar grupos de correo para identificar grupos de contactos que quiere que reciban la misma información. Por ejemplo, puede configurar un grupo de direcciones para los contactos a los que desea enviar una notificación de un movimiento de oficina u otro grupo para enviar regalos de vacaciones.

El uso de grupos de correo en contactos es un proceso que consta de dos pasos. Primero, debe definir el código del grupo de correo. Solo debe realzar este paso una vez para cada grupo de correo. Una vez tenga código de grupo de correo, puede comenzar a asignar el código a empresas de contacto.

## <a name="to-define-mailing-group-codes"></a>Para definir códigos de grupo de correo
El código de grupo de correo define el tipo o la categoría del grupo, como MOVE para movimiento de oficina o GIFT para regalo de vacaciones. Puede tener varios códigos de grupo de industria. Para definir los grupos de industria, pude usar la ventana **Grupos de correo**.

1. Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Grupos de correo** y, a continuación, seleccione el vínculo relacionado.
2. Seleccione la acción **Nuevo** e introduzca un código y una descripción. El código admite un máximo de 11 caracteres y puede ser cualquier combinación de números y letras.

## <a name="AssignMailGroupContact"></a> Para asignar grupos de correo a un contacto
1. Abra el contacto.
2. Elija la acción **Grupos de correo**. Se abrirá la ventana **Grupos direcciones contacto**.
3. En el campo **Código de grupos de correo**, seleccione el grupo de correo que desea asignar.

Repita estos pasos para asignar todos los grupos de direcciones que desee. También puede asignar grupos de correo desde la lista de contactos con el mismo procedimiento.

Aparece automáticamente el número de grupos de direcciones asignados al contacto del campo **N.º grupos direcciones** en la sección **Segmentación** en la ventana **Contacto**.

Después de asignar grupos de direcciones a sus contactos puede usar esa información para seleccionar contactos para sus segmentos. Para obtener más información, vea [Agregar contactos a segmentos](marketing-add-contact-segment.md).

## <a name="see-also"></a>Consulte también
[Crear empresas de contacto](marketing-create-contact-companies.md)  
[Crear personas de contacto](marketing-create-contact-persons.md)  
[Trabajar con Financials](ui-work-product.md)

