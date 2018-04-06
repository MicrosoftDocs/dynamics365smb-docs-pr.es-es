---
title: "Definir los códigos de relaciones de negocio en contactos | Documentos de Microsoft"
description: Utilice las relaciones de negocio en Finance and Operations, Business edition como ayuda con el marketing y para indicar las relaciones de ese tipo con los clientes potenciales y los clientes, por ejemplo, un banco o un proveedor de servicios.
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: marketing, prospect, contact, client, customer
ms.date: 06/06/2017
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: a72563f5057a1f9136a2d2b3aced6f028dc24051
ms.contentlocale: es-es
ms.lasthandoff: 03/22/2018

---
# <a name="setting-up-business-relations-on-contact-companies"></a>Configurar relaciones de negocio en empresas de contacto
Puede usar relaciones de negocio se usan para indicar las relaciones de ese tipo con los contactos, por ejemplo, referencia, banco, consultora, proveedor de servicios, etc.

El uso relaciones de negocio en contactos es un proceso que consta de dos pasos. Primero, debe definir el código de relación de negocio. Solo debe realizar este paso una vez para cada relación de negocio. Una vez tenga un código de relación de negocio, puede comenzar a asignar el código a empresas de contacto.

> [!NOTE]  
>   Si desea sincronizar sus contactos con proveedores, clientes o bancos en otras partes de la aplicación, se recomienda configurar una relación de negocio para ellos.

## <a name="to-define-a-business-relation-code"></a>Para definir un código de relación de negocio
El código de relación de negocio define una categoría o un tipo de relación de negocio, como BANCO o ABO. Puede tener varios códigos de relación de negocio. Para definir relaciones de negocio, use la ventana **Relaciones de negocio**.

1. Seleccione el icono ![Buscar página o informe](media/ui-search/search_small.png "icono Buscar página o informe"), escriba **Relaciones negocio** y, a continuación, seleccione el vínculo relacionado.
2. Seleccione la acción **Nuevo** e introduzca un código y una descripción. El código admite un máximo de 11 caracteres y puede ser cualquier combinación de números y letras.

## <a name="AssignBusRelContact"></a> Para asignar relaciones de negocio a un contacto
No puede asignar relaciones de contacto a una persona de contacto, solo a empresas.

1. Abra el contacto.
2. Seleccione la acción **Empresa** y, a continuación, seleccione la acción **Relaciones de negocio**.

    Se abre la ventana **Relaciones de negocio de contacto**.
3. En el campo **Cód. relación negocio**, seleccione la relación de negocio que desea asignar.

Repita estos pasos para asignar todos las relaciones de negocio que desee. También puede asignar relaciones de negocio desde la lista de contactos con el mismo procedimiento.

Aparece automáticamente el número de relaciones de negocio asignadas al contacto del campo **N.º de relaciones de negocio** en la sección **Segmentación** de la ventana **Contacto**.

Después de asignar relaciones de negocio a sus contactos, puede utilizar esa información para seleccionar contactos para sus segmentos. Para obtener más información, vea [Agregar contactos a segmentos](marketing-add-contact-segment.md).

## <a name="see-also"></a>Consulte también
[Crear empresas de contacto](marketing-create-contact-companies.md)  
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

