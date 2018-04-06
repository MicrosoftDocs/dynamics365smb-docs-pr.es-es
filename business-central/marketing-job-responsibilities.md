---
title: Configurar responsabilidades de cargo para contactos | Documentos de Microsoft
description: "Puede definir una responsabilidad de cargo y asignarla a un contacto para indicar las tareas de las que es responsable que su contacto en su empresa, por ejemplo, TI o producción."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: task, to-do, relationship, prospect
ms.date: 06/06/2017
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 8c62aea1e830b1b37e470fdf7ffbe8227bec41f6
ms.contentlocale: es-es
ms.lasthandoff: 03/22/2018

---
# <a name="set-up-job-responsibilities-for-contact-persons"></a>Configurar responsabilidades cargo para las personas de contacto.
Puede agregar información sobre las responsabilidades cargo de las personas de contacto para indicar que son responsables en su empresa, por ejemplo, en TI, gestión o producción. Puede usar esta información al introducir información sobre sus contactos.

El uso de las responsabilidades cargo en contactos es un proceso que consta de dos pasos. Primero, debe definir el código de la responsabilidad cargo. Solo debe realzar este paso una vez para cada una. Una vez tenga un código de responsabilidad cargo, puede empezar a asignarlo a sus personas de contacto.

## <a name="to-define-a-job-responsibility-code"></a>Para definir un código de responsabilidad de cargo
El código de responsabilidad cargo define el tipo o la categoría del trabajo, por ejemplo MARKETING o COMPRA. Puede tener varios códigos de responsabilidad. Para definir la responsabilidad cargo, use la ventana **Responsabilidades cargo**.

1. Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Responsabilidades cargo** y, a continuación, seleccione el vínculo relacionado.
2. Seleccione la acción **Nuevo** e introduzca un código y una descripción. El código admite un máximo de 11 caracteres y puede ser cualquier combinación de números y letras.

## <a name="to-assign-job-responsibilities-to-a-contact-person"></a>Para asignar responsabilidades de cargo a una persona de contacto
No puede asignar responsabilidades cargo a contactos que sean empresas.

1. Abra la persona de contacto.
2. Elija la acción **Persona** y, a continuación, elija la acción **Responsabilidades cargo**. Aparecerá la ventana **Cargos contactos**.
3. En el campo **Cód. cargo contacto**, seleccione la responsabilidad cargo que desea asignar.

Repita estos pasos para asignar todas las responsabilidades del cargo que desee. También puede asignar responsabilidades cargo de la lista de contactos siguiendo el mismo procedimiento.

El número de responsabilidades cargo que ha asignado al contacto se muestra en el campo **N.º responsabilidades cargo** en la sección **Segmentación** en la ventana **Contacto**.

Después de asignar responsabilidades cargo a sus contactos puede usar esa información para seleccionar contactos para sus segmentos. Para obtener más información, vea [Agregar contactos a segmentos](marketing-add-contact-segment.md).

## <a name="see-also"></a>Consulte también
[Crear personas de contacto](marketing-create-contact-persons.md)  
[Crear empresas de contacto](marketing-create-contact-companies.md)  
[Trabajar con Financials](ui-work-product.md)

