---
title: "Configurar información para contactos | Documentos de Microsoft"
description: "Describe las tareas para especificar información y códigos, por ejemplo, sobre grupos de industria y relaciones de negocio, antes de configurar los contactos."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, prospect
ms.date: 12/07/2018
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: 8a73de1aa2f4a0f633c401ea341bb7bde6579723
ms.openlocfilehash: 1f186a1eb1386d1f54b27a7ee9a9b3445c19e469
ms.contentlocale: es-es
ms.lasthandoff: 12/11/2018

---
# <a name="setting-up-contacts"></a>Configurar contactos
Al crear contactos, puede especificar información como, por ejemplo, la industria a la que pertenecen las empresas de contacto y sus relaciones de negocio con los contactos.

Antes de crear los contactos y los detalles de registro de sus relaciones de negocio, debe configurar los códigos que utilizará para asignar esta información a las empresas y personas de contacto. Se pueden configurar códigos para grupos de correo, grupos de industria, relaciones de negocio, orígenes Web, niveles de organización y responsabilidades del cargo.

Una vez configurada esta información, resultará mucho más fácil organizar la información de contactos y se podrá llevar a cabo la búsqueda de contactos para cada grupo específico de forma más eficaz. Cada grupo de su empresa podrá buscar esta información, logrando así una comunicación más satisfactoria con los contactos.

En relación con la configuración de sus contactos, debe configurar relaciones de negocio con los contactos, por ejemplo, referencia, banco, consultora y proveedor de servicios. Para obtener más información, consulte [Configurar relaciones de negocio en empresas de contacto](marketing-business-relations.md).

## <a name="setting-up-industry-groups-for-contact-companies"></a>Configurar grupos de industria para empresas de contacto
Puede usar grupos industria para indicar el tipo de industria al que pertenecen sus contactos, por ejemplo, la industria de fabricación o la industria del automóvil.

El uso de grupos industria en contactos es un proceso que consta de dos pasos. Primero, debe definir el código del grupo de industria. Solo debe realzar este paso una vez para cada grupo de industria. Una vez tenga código de grupo de industria, puede comenzar a asignar el código a empresas de contacto.

> [!NOTE]  
>   Si desea sincronizar sus contactos con proveedores, clientes o bancos en otras partes de la aplicación, se recomienda configurar una relación de negocio para ellos.

### <a name="to-define-an-industry-group-code"></a>Para definir un código de grupo de industria
El código de grupo de industria define el tipo o la categoría del grupo, como ADVERT para publicidad o PRESS para televisión y radio. Puede tener varios códigos de grupo de industria. Para definir los grupos de industria, puede usar la página **Grupos industria**.

1. Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Grupos industria** y luego elija el enlace relacionado.
2. Seleccione la acción **Nuevo** e introduzca un código y una descripción. El código admite un máximo de 11 caracteres y puede ser cualquier combinación de números y letras.

### <a name="AssignIndustryGroupContact"></a> Para asignar grupos de industria a un contacto
No puede asignar grupos de industria a una persona de contacto, solo a empresas.

1. Abra el contacto.
2. Elija la acción **Empresa** y, a continuación, elija la acción **Grupos de industria**. Se abrirá la página **Grupos industria contacto**.
3. En el campo **Código de grupos de industria**, seleccione el grupo de industria que desea asignar.

Repita estos pasos para asignar todos los grupos de industria que desee. También puede asignar grupos de industria desde la lista de contactos con el mismo procedimiento.

Aparece automáticamente el número de grupos de industrias asignados al contacto del campo **N.º grupos industrias** en la sección **Segmentación** en la página **Contacto**.

Después de asignar grupos de industria a sus contactos, puede utilizar esa información para seleccionar contactos para sus segmentos. Para obtener más información, vea [Agregar contactos a segmentos](marketing-add-contact-segment.md).

## <a name="setting-up-mailing-groups-for-contacts"></a>Configurar grupos de correo para contactos
Puede usar grupos de correo para identificar grupos de contactos que quiere que reciban la misma información. Por ejemplo, puede configurar un grupo de direcciones para los contactos a los que desea enviar una notificación de un movimiento de oficina u otro grupo para enviar regalos de vacaciones.

El uso de grupos de correo en contactos es un proceso que consta de dos pasos. Primero, debe definir el código del grupo de correo. Solo debe realzar este paso una vez para cada grupo de correo. Una vez tenga código de grupo de correo, puede comenzar a asignar el código a empresas de contacto.

### <a name="to-define-mailing-group-codes"></a>Para definir códigos de grupo de correo
El código de grupo de correo define el tipo o la categoría del grupo, como MOVE para movimiento de oficina o GIFT para regalo de vacaciones. Puede tener varios códigos de grupo de industria. Para definir los grupos de industria, puede usar la página **Grupos de correo**.

1. Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Grupos de correo** y luego elija el enlace relacionado.
2. Seleccione la acción **Nuevo** e introduzca un código y una descripción. El código admite un máximo de 11 caracteres y puede ser cualquier combinación de números y letras.

### <a name="AssignMailGroupContact"></a> Para asignar grupos de correo a un contacto
1. Abra el contacto.
2. Elija la acción **Grupos de correo**. Se abrirá la página **Grupos correo contacto**.
3. En el campo **Código de grupos de correo**, seleccione el grupo de correo que desea asignar.

Repita estos pasos para asignar todos los grupos de direcciones que desee. También puede asignar grupos de correo desde la lista de contactos con el mismo procedimiento.

Aparece automáticamente el número de grupos de direcciones asignados al contacto del campo **N.º grupos direcciones** en la sección **Segmentación** en la página **Contacto**.

Después de asignar grupos de direcciones a sus contactos puede usar esa información para seleccionar contactos para sus segmentos. Para obtener más información, vea [Agregar contactos a segmentos](marketing-add-contact-segment.md).

## <a name="setting-up-alternate-addresses-for-contacts"></a>Configurar dirección alternativa para contactos
Puede asignar una dirección alternativa a la que pueda enviar correo e información en ocasiones a sus contactos, por ejemplo, a su casa de verano. También puede asignar uno o varios rangos de fechas para cada dirección alternativa especificada para sus contactos para especificar cuándo es válida una dirección.

### <a name="to-assign-an-alternate-address"></a>Para asignar direcciones alternativas
1. Abra el contacto.
2. Elija la acción **Dirección alternativa** y, a continuación, elija **Ficha**. Se abre la página **Lista dir. alt. contacto**.
3. Escriba una nueva dirección alternativa y rellene los campos de la página **Dirección de contacto alternativa**.

Repita estos pasos para asignar todas las direcciones alternativas que desee. Para cada dirección alternativa puede especificar uno o varios rangos de fechas.

También puede asignar direcciones alternativas, con el mismo procedimiento, en la página de la lista de contactos.

### <a name="to-assign-an-alternate-address-date-range"></a>Para asignar un intervalo de fechas de direcciones alternativas
1. Abra el contacto.
2. Elija la acción **Dirección alternativa** y, a continuación, elija **Rango de fechas**. Se abre la página **Rangos fecha dir. alt. cont.**
3. Elija la acción **Nuevo**.
4. En el campo **Cód. dirección alt. contacto**, seleccione una dirección alternativa para este contacto y, a continuación, rellene los campos **Fecha de inicio** y **Fecha de finalización**.

Repita estos pasos para asignar todos los rangos fechas que desee.

## <a name="setting-up-job-responsibilities-for-contact-persons"></a>Configurar responsabilidades cargo para las personas de contacto
Puede agregar información sobre las responsabilidades cargo de las personas de contacto para indicar que son responsables en su empresa, por ejemplo, en TI, gestión o producción. Puede usar esta información al introducir información sobre sus contactos.

El uso de las responsabilidades cargo en contactos es un proceso que consta de dos pasos. Primero, debe definir el código de la responsabilidad cargo. Solo debe realzar este paso una vez para cada una. Una vez tenga un código de responsabilidad cargo, puede empezar a asignarlo a sus personas de contacto.

### <a name="to-define-a-job-responsibility-code"></a>Para definir un código de responsabilidad de cargo
El código de responsabilidad cargo define el tipo o la categoría del trabajo, por ejemplo MARKETING o COMPRA. Puede tener varios códigos de responsabilidad. Para definir la responsabilidad cargo, use la página **Responsabilidades cargo**.

1. Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Responsabilidades cargo** y luego elija el enlace relacionado.
2. Seleccione la acción **Nuevo** e introduzca un código y una descripción. El código admite un máximo de 11 caracteres y puede ser cualquier combinación de números y letras.

### <a name="to-assign-job-responsibilities-to-a-contact-person"></a>Para asignar responsabilidades de cargo a una persona de contacto
No puede asignar responsabilidades cargo a contactos que sean empresas.

1. Abra la persona de contacto.
2. Elija la acción **Persona** y, a continuación, elija la acción **Responsabilidades cargo**. Aparecerá la página **Cargos contactos**.
3. En el campo **Cód. cargo contacto**, seleccione la responsabilidad cargo que desea asignar.

Repita estos pasos para asignar todas las responsabilidades del cargo que desee. También puede asignar responsabilidades cargo de la lista de contactos siguiendo el mismo procedimiento.

El número de responsabilidades cargo que ha asignado al contacto se muestra en el campo **N.º responsabilidades cargo** en la sección **Segmentación** en la página **Contacto**.

Después de asignar responsabilidades cargo a sus contactos puede usar esa información para seleccionar contactos para sus segmentos. Para obtener más información, vea [Agregar contactos a segmentos](marketing-add-contact-segment.md).

## <a name="setting-up-organizational-levels-for-contact-persons"></a>Configurar niveles de organización para personas de contacto
Puede usar niveles de organización en sus contactos para especificar su posición en la empresa, por ejemplo, alta gestión. Puede usar esta información al introducir información sobre sus contactos.

El uso de niveles de organización en contactos es un proceso que consta de dos pasos. Primero, debe definir el código de nivel de organización. Solo debe realizar este paso una vez para cada nivel de organización. Una vez tenga código de nivel de organización, puede comenzar a asignar el código a personas de contacto.

### <a name="to-define-an-organizational-level-code"></a>Para definir un código de nivel de organización
El código de nivel de organización define el tipo o la categoría de nivel de organización, por ejemplo DIRGEN o DIRFIN. Puede tener varios códigos de nivel de organización. Para definir el nivel de organización, use la página **Niveles de organización**.

1. Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Niveles organización** y luego elija el enlace relacionado.
2. Seleccione la acción **Nuevo** e introduzca un código y una descripción. El código admite un máximo de 11 caracteres y puede ser cualquier combinación de números y letras.

### <a name="to-assign-organizational-levels-to-a-contact-person"></a>Para asignar niveles de organización a una persona de contacto
Solo puede asignar niveles de organización a personas de contacto, no a empresas de contacto. Sólo puede asignar un nivel organización a cada contacto.

1. Abra el contacto.
2. En el campo **Niveles de organización**, seleccione el código que desea asignar.

Después de asignar niveles organización a sus contactos, puede utilizar esta información para crear segmentos.

Después de asignar responsabilidades cargo a sus contactos puede usar esa información para seleccionar contactos para sus segmentos. Para obtener más información, vea [Agregar contactos a segmentos](marketing-add-contact-segment.md).

## <a name="setting-up-web-sources-for-contact-companies"></a>Configurar enlaces web para empresas de contacto
Puede usar enlaces web con sus empresas de contacto para identificar, por ejemplo, los motores de búsqueda y los sitios web de Internet que quiere usar para buscar información sobre los contactos. Al asignar enlaces web, especifica el motor de búsqueda y la palabra clave que la aplicación usará para buscar la información solicitada.

El uso de enlaces web en contactos es un proceso que consta de dos pasos. Primero, debe definir el código del enlace web. Solo debe realizar este paso una vez para cada enlace web. Una vez tenga código de enlace web, puede comenzar a asignar el código a personas de contacto.

### <a name="to-define-a-web-source-code"></a>Para definir un código de enlace Web
1. Elija el icono ![bombilla que abre la función Dígame](media/ui-search/search_small.png "Dígame que desea hacer"), escriba **Enlaces web** y luego elija el enlace relacionado.
2. Elija la acción **Nuevo**.
3. Rellene los campos **Código**, **Descripción** y **URL**.

    Escriba %1 en el campo **Dirección URL** para insertar un marcador de posición para una palabra de búsqueda en la URL. Al ejecutar al enlace web desde una ficha de contacto, %1 se reemplaza con la palabra de búsqueda, por ejemplo, el nombre de la empresa, especificada en la página **Enlaces web de contactos**.

Repita estos pasos para configurar todos los orígenes web que desee.

### <a name="to-assign-web-sources-to-a-contact-company"></a>Para asignar enlaces Web a una empresa de contacto
Al asignar enlaces web, especifica el motor de búsqueda y la palabra clave que la aplicación usará para buscar la información solicitada.

1. Abra el contacto.
2. Elija la acción **Empresa** y, a continuación, elija la acción **Enlaces web**. Se abre la página **Enlaces web contacto**.
3. En el campo **Código de enlace web**, elija el enlace web que desea asignar.
4. Escriba en el campo **Busca palabra**, escriba la palabra de búsqueda que desea que use el sistema para buscar la información.

Repita estos pasos para asignar todos los orígenes web que desee.

También puede asignar orígenes web, con el mismo procedimiento, en la página **Lista contactos**.

## <a name="see-also"></a>Consulte también
[Gestionar contactos](marketing-contacts.md)  
[Administrar oportunidades de venta](marketing-manage-sales-opportunities.md)  
[Trabajar con [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

